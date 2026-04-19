# Armor system

* **TBD** for now, system assumes linear pen vs speed. This is not super realistic. For now, lets leave it.

## Overview

* Game uses armor system that is split into 2 slots
    * Head
    * Body
* Game distinguishes which direction hit came from
* For the direction hit came from armor value is checked against projectile remaining penetration (bullet loses speed going threw air, environment, armor)

## Protected areas

### Head protection

* Head protection (usually helmet) consists of 2 potential protections
    * Base protection
        * Left
        * Right
        * Back
        * Top - if helmet headshot was [grazing shoot](COMBAT_DETAILS.md#grazing-hit)
    * Face protection

### Body protection

* Front protection - base protection
* Back protection - one level lower that base protection
* Sides - also one level lower if present

## Armor level

Armor level ranges from 1 to 10. This scale is linear. Each of components mentioned above can have different armor level.

## Penetration mechanics

When hit is scored against armored part of character there is check of remaining bullet penetration vs armor level

* Matching current effective armor level with current bullet penetration gives 100% chance to pen
* If armor is at 100%, 1 pen level below current effective armor gives 0% chance to pen
* Everything in between is linear
* Armor damage lowers the 0% pen threshold
    * % of armor damaged lowers 0% threshold down by % for base armor level
    * At 0% damage the 0% threshold is `effective_armor_lvl - 1`
    * At 100% damage the 0% threshold is `-1`
    * Example: level 8 armor normally has 0% chance to pen for pen 7. At 50% damage it loses 50% of 8 levels for the 0% threshold, so the threshold moves from 7 to 3.
        * So for level 8 armor with 50% damage we have 100% chance to pen for pen 8, 0% for pen 3, and linear probability in between

### Variables

* armor_lvl - base armor level - for example 8
* armor_dmg - damaged fraction of armor, for example `0.25` for 25% damage
* is_side_or_back_armor - use `1` for side/back armor, otherwise `0`; this drops base armor by 1 for the calc
* bullet_base_pen - for example 8
* bullet_base_pen_speed - for example at speed 800 m/s - so in above example bullet pen would be 8 at 800 m/s
* bullet_current_speed - current speed of the bullet, for example 700 m/s

### Pen formula

Derived values:

* `effective_armor_lvl = armor_lvl - is_side_or_back_armor`
* `current_bullet_pen = bullet_base_pen * bullet_current_speed / bullet_base_pen_speed`
* `zero_pen_threshold = (effective_armor_lvl - 1) - armor_lvl * armor_dmg`

Final penetration chance:

* `pen_chance = clamp((current_bullet_pen - zero_pen_threshold) / (effective_armor_lvl - zero_pen_threshold), 0, 1)`

Where:

* `clamp(x, 0, 1) = max(0, min(1, x))`
* `pen_chance = 0` means 0% chance to pen
* `pen_chance = 1` means 100% chance to pen

Worked example:

* `armor_lvl = 8`
* `armor_dmg = 0.50`
* `is_side_or_back_armor = 0`
* `bullet_base_pen = 8`
* `bullet_base_pen_speed = 800`
* `bullet_current_speed = 700`
* `effective_armor_lvl = 8`
* `current_bullet_pen = 8 * 700 / 800 = 7`
* `zero_pen_threshold = (8 - 1) - 8 * 0.50 = 3`
* `pen_chance = (7 - 3) / (8 - 3) = 0.8`, so the bullet has 80% chance to pen

## Armor damage

* Penetrating by any round does 25% of armor damage
* Non pen shoot destroys `(effective_armor_lvl - current_bullet_pen)/current_bullet_pen/4`

### Examples

* Pen 3 bullet hits lvl 6 armor, damages (6-3)/6/2 *100% = 12.5%
* Pen 1 `bullet

### Speed lose on pen

* Bullet loses pen of equivalent to half of armor level of penetrated armor

### Examples

* Experimental AP 7.62x51 has 12.5 pen @ velocity 800 m/s has 900 m/s speed (effectively around 14 pen)
    * When hitting lvl 2 armor loses 1 level of pen (64 m/s)
* Pen 8 bullet hits lvl 7 armor
    * Penetrates, looses 3.5 pen

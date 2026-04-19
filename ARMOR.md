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

* Penetrating the same level as current bullet power will have 100% change to pen
* Penetrating 1 level lower will have 0% change if armor is at 100%
* Rest is linear - 0% (for armor level 1 above current bullet pen) to 100% (the same pen level as armor)
* Armor damage lowers the 0% pen threshold
  * % of armor damaged lowers 0% threshold down by % for base armor level
  * 0% armor is the same as -1 armor level (penned 100% by lvl 0 bullet) and 100% armor is armor_lvl - 1
  * Example will be easier. Lvl 8 normally would have 0% change of pen for lvl 7. At 50% it is going to lose 50% of 8 levels for 0% pen.
    * So for lvl 8 armor with 50% damage we have 100% change to pen for lvl 8 pen bullet, 0% for 3 pen bullet, and linear probability in between

### Variables

* armor_lvl - base armor level - for example 8
* armor_dmg - % of armor that is damaged, for example 25% damage
* is_side_or_back_armor - if it is, will drop base armor by 1 for calc 
* bullet_base_pen - for example 8
* bullet_base_pen_speed - for example at speed 800 m/s - so in above example bullet pen would be 8 at 800 m/s
* bullet_current_speed - current speed of the bullet, for example 700 m/s

### Pen formula

**TODO**

## Armor damage

* Penetrating by any round does 25% of armor damage
* Non pen shoot destroys (armor_level - current_bullet_pen)/current_bullet_pen/4 * 100 %

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

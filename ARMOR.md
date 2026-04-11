# Armor system

* Game uses armor system that is split into 2 slots
  * Head
  * Torso
* Game distinguishes which direction hit came from
* For the direction hit came from armor value is checked against projectile remaining penetration

## Protected areas

### Head protection

* Head protection (usually helmet) consists of 2 potential protection layers
* Base helmet protection cover character
  * Left
  * Right
  * Back
  * Top - if helmet headshot was [grazing shoot](COMBAT_DETAILS.md#grazing-hit)

### Torso protection

* Torso protection level is separate for
  * Front - usually strongest
  * Back
  * Sides

## Armor level

Armor level ranges from 1 to 10. This scale is linear. Each of components mentioned above can have different armor level.

## Penetration mechanics

* When hit is scored against armored part of character there is check of remaining bullet penetration vs armor level
  * Penetrating the same level as current bullet power will have 100% change to pen
  * Penetrating 1 level lower will have 0% change
  * Rest is linear - 0% (for armor level 1 above current bullet pen) to 100% (the same pen level as armor)
* Bullet can lose speed traveling threw air and different materials, see [environment penetration](./COMBAT_DETAILS.md#environment-penetration)

## Armor damage

Hitting armor and not penetrating it will result in armor damage

TODO

### Lose of pen

TODO

### Fragmentation

If armor level 4 or higher bullet has a change of fracture on pen

* This will stop the bullet but will lose 

### Examples

* Experimental AP 7.62x51 has 12.5 pen @ velocity 800 m/s
TODO

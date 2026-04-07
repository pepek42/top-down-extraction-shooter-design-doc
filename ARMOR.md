# Armor system

Game uses armor system that is split into 2 layers
* Head
* Torso

Basic mechanics
* Game distinguishes which direction hit came from
* For the direction hit came from armor value is checked against projectile remaining penetration

## Head protection

* Head protection (usually helmet) consists of 2 potential protection layers
* Base helmet protection cover character
  * Left
  * Right
  * Back
  * Top - if helmet headshot was [grazing shoot](COMBAT_DETAILS.md#grazing-hit)

## Torso protection

Torso protection level is separate for front, back and sides

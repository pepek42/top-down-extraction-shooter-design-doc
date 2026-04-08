# Combat details

## Hit types

### Body shoot

### Grazing hit

### Headshot

## Weapon types

* Pistols - can be effective at close range against unarmored targets
* SMG - similar to pistols but better recoil control and faster rate of fire
* PDW - similar to SMG but better penetration at cost of stopping power
* AR - versatile, can shoot range of ammo types, lacks effectiveness at very long ranges both in accuracy and pen
* LMG - TODO
* DMR - TODO
* Shotgun - TODO
* TODO

### Example calibers:

* 5.56x45, 5.45x39, .300 - AR/carabin/LMG/Civilian rifles
* 9x19, .45 - pistol/SMG
* 7.62x51, 7.62x54 - DMR/Battle Rifle/Sniper Rifles
* 7.62x39 - AR/Assault Carabin
* 12 GA - shotguns
* .277 - modern AR/LMG
* 5.7, 4.7 - PDW/Pistol

## Possible ammo types

* Civilian - lower pen, lower accuracy
* Match - better accuracy
* Hollow point (HP) - bed pen, high damage
* Military - reasonable pen for given caliber
* Tracer - visible on screen and by enemies, can be combined with other types, usually slightly lower pen
* AP - high pen/muzzle velocity for given caliber
* Experimental - really high pen/muzzle velocity for given caliber

## Environment penetration

* Penetration system works for environment in addition to [armor](ARMOR.md#penetration-mechanics)
* Different environment obstacles will have different resistance. For example:
  * Stone wall is penetrable by medium to high caliber AP
  * Wooden wall will stop 9x19 rounds and will significantly reduce speed of AP round

## Armor penetration

Characters can wear head/body armor that will potentially stop bullets. See more in [armor doc](ARMOR.md#penetration-mechanics)

## Character penetration

When character is shot (armor is defeated) projectile can slow down or stop completely inside character. Expected result is close to reality. For example

* If unprotected enemy is shot with 9x19 hollow point bullet in the center of mass bullet is not expected to penetrate
* If unprotected enemy is grazed with 9x19 hollow point bullet it will still significantly slow down bullet
* If unprotected enemy is shoot with 7.52x51 experimental bullet we expect little slow down
* If heavily armored enemy shot with 5.56x45 AP round - round may fragment dealing extra damage and not penetrating but it can also penetrate

Grazing shot will go threw smaller amount of character compared to full body shot.

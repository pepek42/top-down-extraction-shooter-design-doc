# Health system

* Hit points base - 100 HP base
* 3 types of hits
    * Headshot - huge damage multiplayer, player need to point directly on enemy to occur, random chance for enemies
    * Normal hit - middle of the target, normal bullet damage
    * Grazing hit - hit far from enemy center, reduced damage (simulates limb damage)
* Bleeding status
* Stunned status - for example from larger caliber rounds bouncing of helmet or from explosions
* Broken bone status - from grazing hits
    * Leg - slow down
    * Hand - inaccurate fire

## Health damage

* Bullet energy is deposited in target
* High pen AP bullet will do less damage compared to FMJ or hollow point but AP will usually carry more energy overall so it will have high damage
* [grazing hit](./COMBAT_DETAILS.md#grazing-hit) will do less damage compared to normal damage

### Examples

**NON-FINAL VALUES** - just for reference

* 300 damage AP 7.62x51 (could penetrate multiple targets) will do
    * 100 damage to unarmored target
    * 50 damage with grazing shot to unarmored target
    * 60 damage to heavily armored target
* 80 damage 9x19 hollow point will do
    * 80 damage to target (will not penetrate it)

## Health items

All items will do all of mentioned things in one use if applicable

* Bandage
  * Stops bleeds
  * Stacks up to 10
* Splint
  * Fixes fractures
  * Stacks up to 10
* Simple med kit
  * Restores 25 HP
  * Stacks up to 5
* Med kit
  * Restores 50 HP
  * Stops bleeds
  * Stacks up to 5
* Advanced med kit
  * Restores 75 HP
  * Stops bleeds
  * Fixes fractures
  * Stacks up to 5

### Stims

All stims stack up to 5

* Adrenaline
  * Slow motion effect (50%) able to use for **TBD** 10 seconds (5s IRL) withing 5 min
* Health steam
  * +50 HP
* Bleed stim
  * Stops bleed and prevents bleed for 5 min
* Morphine
  * Pain resistance for 5 min
* Regen stim
  * Regenerates 1 HP/second for 2 min

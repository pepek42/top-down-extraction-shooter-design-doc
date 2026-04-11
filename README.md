# Game design doc

Game is top down light extraction tactical shooter. In the future there is a plan to make it blend with tactical strategy game. Main goal of a player is to survive a map:
* Extract
* Clear the map

## Design goals

Main design goals are explained in [design goals doc](./DESIGN_GOALS.md)

## Combat

### Weapons

Game offers different weapons with different calibers, ammo types, attachments.

More detailed description in [combat](./COMBAT_DETAILS.md)

### Armor system

Game offers armored vests, rigs and helmets with face shields. More detailed description in [armor](./ARMOR.md)


## Health system

* Hit points base - 100 HP base
* Health damage decreased by
* 3 types of hits
  * Headshot - huge damage multiplayer
  * Normal hit - middle of the target
  * Grazing hit - reduced damage. Half or target radius is still full damage, further from the center that r/2 decreases damage from full to no damage
* Bleeding status
* Stunned status - for example from larger caliber rounds bouncing of helmet or from explosions

## Maps

* Maps can be predefined or dynamic (randomly generated with pattern). More details in TODO

## Items and slots

* Items need slot to be extracted and stored in hideout stash
* None of the items take more than one slot
* Smaller items can stack in single slot

## Hideout

### Upgrades

* Player can upgrade most stations

### Stash

*

### Player loadout

### Squad management

## Raid selection screen

* There are 2 types of map to choose from - handcrafted and dynamically created
* Map are described in [maps](./MAPS.md)
* On the left screen there is current player loadout
* Each map has
* On the right screen there is map selection, player can see
  * Map name
  * Standard loot quality/enemy strength
  * Current loot/enemy multiplayer

## Raid

* Instead of looting player will be awarder potential loot they can extract with at extraction zone
* Loot quality is determined by number

### Enemies

* [Factions](./LORE.md#factions)
* [AI](./AI.md)

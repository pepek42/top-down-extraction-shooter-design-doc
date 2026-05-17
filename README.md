# Game design doc

Game is top down light extraction tactical shooter with tactical strategy elements.

## Design goals

Main design goals are explained in [design goals doc](./DESIGN_GOALS.md)

## Combat

### Weapons

Game offers different weapons with different calibers, ammo types, attachments.

More detailed description in [combat](./COMBAT_DETAILS.md)

### Armor system

Game offers armored vests, rigs and helmets with face shields. More detailed description in [armor](PROTECTIVE_GEAR.md)



## Items and slots

* Items need slot to be extracted and stored in hideout stash
* None of the items take more than one slot
* Smaller items can stack in single slot

## Raid selection screen

* There are 2 types of map to choose from - handcrafted and dynamically created
* Map are described in [maps](./MAPS.md)
* On the left screen there is current player loadout
* Each map has configurable difficulty modifiers
* On the right screen there is map selection, player can see
    * Map name
    * Standard loot quality/enemy strength
    * Current loot/enemy multiplayer

## Raid

* Instead of looting player will be awarded potential loot they can extract with at extraction zone
* Loot quality is determined by cleared point of interest count and their loot type and quality

### Enemies

* [Factions](./LORE.md#factions)
* [AI](./AI.md)

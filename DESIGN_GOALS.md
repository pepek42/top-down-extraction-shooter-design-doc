# Design goals

Game tries to be fun extraction looter shooter with following goals:

* Minimizing looting part down to bear minimum
* Simplifying extraction
* Improving loadout management
* Providing allies allowing for bolder engagements design

See [inspirations](./INSPIRATIONS.md) for more details

## 2D vs 3D

As I have no artistic skills 2D is much more possible to do. Although Ravenfield like extraction shooter would be cool it is out of my reach in terms of art and game dev skills.

## Combat feel

Combat should be realistic with simplified medical system (but still more advanced compared to many games).

### Goal

* Realistic top down shooter
* More tactical gameplay, where planning, slower approach matters
* Realistic weapons with bullet penetration, suppressive fire

### Potential issues

* Realistic AI - hard to do
* Performance - lots of calculation

## Looting

Current extraction looter shooters usually force you to pick items on the spot and cluttering inventory. This is fun at first, but finding low tier items over and over in mid/late game feels like wast of time. Streamlining loot process would allow looting to scale up.

### Goal

Make flexible looting system that still fulfils all the game needs

* Allow to resupply player during combat when standing next to bodies
* Provide some high/rare items in raid to create tension should I extract with it or should I go after gun fight/clearing point of interest
* Still provide some filler loot for base upgrade and so on

### Potential issues

* This creates 3 stage looting system that is not very intuitive as it is not very realistic
* Most players will not expect such a system, looting containers is industry standard
* Harder to implement

## Extraction

* Player can extract or clear map
* Surviving will mean lower quality/amount of loot when extracted to chose from
* Enemies also can extract to live another day

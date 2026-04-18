# AI behaviour

Goal of AI to recreate human behavior with drive to survive while fulling mission objectives.

## AI tiers

### Low tier troops

* Guards
* Low tier patrols
* Poorly equipped human waves
* Disorganised and demoralized regulars

### Mid-tier troops

* Freshly trained, but better equipped regulars
* More seasoned but lacking equipment regulars
* Organised, support each other

### High tier troops

* Well-trained and well-equipped
* Will use advanced tactics, cooperation

### Elit troops

* Special forces
* Highly trained
* Very coordinated with little verbal communication

## Behaviours

Goal of AI is to create realistic, dynamic world. Ideally AI would be smart and resourceful. AI is expected to

| What                                      | AI level starting to use it                                             |
|-------------------------------------------|-------------------------------------------------------------------------|
| Use suppressive fire                      | [Mid-tier troops](#mid-tier-troops) (more in panic at this tier)        |
| Use cover                                 | [Mid-tier troops](#mid-tier-troops) (more in panic at this tier)        |
| Use room clearing technics                | [High tier troops](#high-tier-troops)                                   |
| Use fire and maneuver                     | [High tier troops](#high-tier-troops)                                   |
| Would fear for its life trying to retreat | [Low tier troops](#low-tier-troops)                                     |
| Would relay info to other allies          | [Mid-tier troops](#mid-tier-troops)                                     |
| Could listen for footsteps/gun shots      | [Mid-tier troops](#mid-tier-troops)                                     |
| Shot tracking skills                      | [Low-tier troops](#low-tier-troops) very week, higher will do it better | 

Examples

* Low tier troops being shoot at from long range with suppressed weapon
    * Go into panic mode, look for cover, refuse to peek out/or look frantically exposing, having very time spotting anything
* Elit troops being shoot at from long range with suppressed weapon
  * Quickly identifying approximate direction of fire, even if not very audible
  * Returning blind fire trying to get into cover
  * Returning more fire in general direction while trying to identify targets
* Elit troops assaulting building
  * Making alternative entrance with rocket luncher/C4
  * Flooding room with explosives/flashes
  * Going in guns blazing
* Mid-tier troops assaulting building
    * Maybe throwing some granadas/flashes
    * Going in trying to identify/shoot targets one by one

## AI morale

AI is going to be afraid of their life.
* Enemy AI depending on level may get bogged down
* Player squads will have higher base morale
* Squad also has morale, if to many squad members are going to be pinned down they may just fire up smoke grenades and try to leave

## Ally/Enemy AI

Both hostile and rival AI will be divided into squads that will have their overall objectives like:
* Patrol
* Defend (including defend to last man)
* Assault
* Aggressive recon

When taking combat losses, taking heavy fire them may decide to retreat and either:
* Extract
* Attack again
* Hold different position

## Subordinates

* **TBD** Squad AI is very hard to do to follow player orders. How to solve this issue? Possible solutions
    * Significantly lower detection of player squad soldiers for enemy AI?
    * Add active pause so that player can better manage squad members and not be at mercy of AI?
* Player is able to give high level orders to their squad and other player organization squads.
  * For example player may do pincer attack on enemy positions from 2 sides
* When trying to fulfil player order squad will behave similarly as ally/enemy AU
* Player may divide their squad into sub squad for example to better cover movement of one sub squad with other squad

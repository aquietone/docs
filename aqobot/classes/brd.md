# AQOBot Bard

The script provides support for Bards level 110+. 

## Song Rotations

Choose between 3 different sets of songs for the Bard to use:  

* `melee` -- Plays songs which are beneficial to melee classes  

    1. Aria  
    2. Spiteful Lyric  
    3. Song of Suffering  
    4. War March  
    5. Pulse  
    6. Dirge  

* `meleedot` -- Plays songs which are beneficial to melee classes as well as DoT songs  

    1. Chant of Flame  
    2. Aria  
    3. War March  
    4. Chant of Disease  
    5. Song of Suffering  
    6. Pulse  
    7. Dirge  
    8. Change of Frost  
  
* `caster` -- Plays songs which are beneficial to caster classes  

    1. Aria  
    2. Arcane  
    3. Fire Debuff Aria  
    4. Song of Suffering  
    5. War March  
    6. Psalm of Potency  
    7. Pulse  
    8. Dirge  

All 3 spell sets will also use:  

* Yelinak's Insult (Synergy nuke)  
* Composite  
* Crescendo  
* Slumber Mez  
* Wave Mez  

## Other Abilities

The Bard will also use the following on cooldown:  

AAs:  

* Cacophony  
* Boastful Bellow  
* Lyrical Prankster  
* Song of Stone  

Abilities:  

* Intimidation  
* Kick  

Discs:  

* Reflexive Rebuttal  

Items:  

* Charm clicky  

## Burns

The following will be activated when burn conditions are met:

AAs:  

* Quick Time  
* Funeral Dirge
* Spire of the Minstrels
* Bladed Song
* Dance of Blades
* Flurry of Notes
* Frenzied Kicks  

Discs:  

* Thousand Blades  

Items:  

* Chest clicky
* Rage of Rolfron clicky

## Defensives

Shield of Notes and Hymn of the Last Stand will be used when HP is low, as well as Fading Memories if enabled.  

## Downtime

* Selos will be kept up at all times  
* Familiar, mount and illusion keyring clicks will be kept up at all times  
* Rallying Solo will be used if low on mana or endurance  

## Pulling

* Attempt to use Staff of Viral Flux for pulling if the Bard has it  
* Otherwise, uses Sonic Disturbance or auto attack depending on distance to mob  

## Modes

The Bard should work in any of the available modes.

## Mezzing

Single target and AOE mezzing are both supported and can be toggled on or off. 

## Settings

| **Name** | **Description** | **Example** |
| :-- | :----- | :--- |
| **Spell Set** | Refer to common settings Spell Set. Available options for bard: `melee`, `caster`, `meleedot` | `/brd spellset meleedot` |
| **Mez ST** | Use single target mez on adds within camp radius | `/brd mezst off` |
| **Mez AE** | Use AE Mez if 3 or more mobs are within camp radius | `/brd mezae on` |
| **Use Epic** | Options: `always`, `burn`, `shm` or `never`. Will always use epic and fierce eye together. shm means only use when Prophet's Gift of the Ruchu is up | `/brd useepic always` |
| **Use Fade** | Fades if you are on ToT or Percent HP below 50 or aggro above 70% on target. Not really tested this one at all | `/brd usefade on` |
| **Rally Group** | Not implemented | |
| **BYOS** | Disables attempts to mem the currently selected spell set, but currently will only try to play the songs listed in the currently selected spell set. Mostly just put this in atm so I can swap some gems on Shei mission | `/brd byos on` |
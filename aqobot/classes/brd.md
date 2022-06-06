# AQOBot Bard

The script provides support for Bards level 110+. 

## Song Rotations

The Bard will use the following songs:

| **Name** | **Usage** |
| :--- | :--- |
| **Aura** | Swapped in as needed |
| **Aria** | Always up |
| **Song of Suffering** | Always up |
| **War March** | Always up |
| **Pulse** | Always up |
| **Yelinak's Insult** | Used every 3-4 casts for Synergy proc |
| **Composite** | Used on CD |
| **Crescendo** | Used on CD |
| **Dirge** | Used on CD |
| **Slumber Mez** | Used when 2 or more mobs are in camp and single target mez is enabled |
| **Wave Mez** | Used when AE count is exceeded and AE mez is enabled |

In addition to the songs above, the spell set can be configured with one of three options to use songs which fit the group composition.  

### melee

Plays additional songs which are beneficial to melee classes:  

| **Name** | **Usage** |
| :--- | :--- |
| **Spiteful Lyric** | Always up |

### meleedot 

Plays DoT songs:  

| **Name** | **Usage** |
| :--- | :--- |
| **Chant of Flame** | Used in combat |
| **Chant of Disease** | Used in combat |
| **Change of Frost** | Used in combat |
  
### caster

Plays additional songs which are beneficial to caster classes:  

| **Name** | **Usage** |
| :--- | :--- |
| **Arcane** | Always up |
| **Fire Debuff Aria** | Always up |
| **Psalm of Potency** | Always up | 

## Other Abilities

The Bard will also use the following:  

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
* Aura will be kept up at all times  
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
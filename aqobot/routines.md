# Routines

The main loop for each class iterates through several routines, taking appropriate actions based on the current conditions.  
The order is defined per class in each of the class files in `aqo/classes` as `class.classOrder`.

## Assist

When running in an assist mode, characters will continuously check whether they meet the conditions to assist on the configured main assists current target.  

### Assist Modes

* **group**: Uses the `${Me.GroupAssistTarget}` TLO to get the target of the configured group main assist.  
* **raid1**: Uses the `${Me.RaidAssistTarget[1]}` TLO to get the target of the configured raid main assist.  
* **raid2**: Uses the `${Me.RaidAssistTarget[2]}` TLO to get the target of the configured raid main assist.  
* **raid3**: Uses the `${Me.RaidAssistTarget[3]}` TLO to get the target of the configured raid main assist.  
* **manual**: Uses `/assist` command to manually assist the configured chase target. This is a weird hack for raid setting in EMU where the above roles do not function.  

### Assist Conditions

* Target is an NPC
* Target is within the configured `CAMPRADIUS` when a camp is set  
* Target is within `CAMPRADIUS` distance of the character when a camp is not set  
* Target is below the configured `AUTOASSISTAT` percent HP  

### Switch With MA

By default, characters will always follow the main assist when they switch targets. This can be disabled by turning off `SWITCHWITHMA`.

### Stick

The following stick command is used: `/stick moveback behind ${Target.MaxRangeTo}*.75 uw`

## Tank

When running in a tank mode, characters will continously scan for mobs to be tanked within their configured `CAMPRADIUS`. AOE aggro abilities will be used depending on the number of mobs within the camp but the tank will not automatically switch targets to obtain aggro on adds.

## Pull

When running in a pull mode, characters will continuously scan for mobs to be pulled within their configured `PULLRADIUS`. New mobs will be pulled when not in combat and the pull conditions are met.

### Pull Conditions

* **Pull Radius**: Only pull mobs which are within x radius of the camp or character  
* **Pull Z Low**: Only pull mobs which are within x distance below the camp or character  
* **Pull Z High**: Only pull mobs which are within x distance above the camp character  
* **Pull Min Level**: Only pull mobs which are at or above level  
* **Pull Max Level**: Only pull mobs which are at or below level  
* **Group Watch**: Watch the specified character (none, self, healer) to decide whether to hold pulls to med  
* **Med Mana**: Hold pulls to med mana if the character specified by group watch is below the med mana threshold  
* **Med Endurance**: Hold pulls to med endurance if the character specified by group watch is below the med endurance threshold  

## Camp

The following modes will create a camp, which characters will stay within the configured `CAMPRADIUS` of at all times, except when going out to pull mobs:  

* assist  
* tank  
* pullertank  

## Chase

When running in chase mode, characters will use nav to stay within the configured `CHASEDISTANCE` of the `CHASETARGET`.

## Mash

Spams all available DPS skills, disciplines and AA's.

## AOE

Spams all available AOE DPS skills, disciplines and AA's when `USEAOE` is enabled.

## Cast

The cast routine for each class will attempt to find the current best spell available to be cast in combat.  
For example, necromancers will first check if alliance is ready and enough necromancers are present, otherwise find the next strongest DoT that is not already applied to the current target before moving on to try nukes or swarm pets.

## Burn

Each class is configured with a set of abilities to be used when burn conditions are met.

### Burn Conditions

* **Burn Always**: The burn routine will always be entered during combat, so that burn abilities are used on cooldown.  
* **Burn Count**: The burn routine will be entered when at least `BURNCOUNT` number of mobs are in camp.  
* **Burn All Named**: The burn routine will be entered whenever the current target is a named. This uses the predefined list of named mobs in `aqo/data` folder rather than relying on `${Target.Named}`.  
* **Burn Percent**: The burn routine will be entered during combat on any mob, as soon as it is below a certain percent HP. Basically the same as burn always but preventing burning immediately on engage.  

## Heal

The heal routine will prioritize healing the most important, most injured characters first.

### Heal Priority

* Tank  
* Self  
* Group Members / Pets  
* Extended Target  
* Group HoT  

### Heal Percents

* **Heal Percent**: The percent HP to begin casting regular heals on an injured character.  
* **Panic Heal Percent**: The percent HP to begin casting emergency heals on an injured character.  
* **HoT Heal Percent**: The percent HP to begin casting single target HoTs if enabled.  
* **Group Heal Percent**: The percent HP to begin casting group heals.  
* **Group Heal Minimum**: The minimum number of players at or below the group heal percent to trigger using a group heal.  

## Mez

Bards and Enchanters will attempt to single target or AE mez adds within the camp radius when `MEZST` or `MEZAE` are enabled.

## Buff

### Self Buffs

Characters will maintain their configured self buffs during down time.

### Combat Buffs

Characters will apply combat buffs as available during combat.

### Single Target Buffs

Some classes have single target buffs configured such as ferocity or other short duration temporary buffs, which will be cast on specific classes present in the group.

### Pet Buffs

Characters will maintain their configured pet buffs during down time.

### Buff Begging

Most classes which can cast buffs will have aliases setup so that others may request buffs.

## Recover

Characters will use configured recover abilities when mana or endurance is below the configured recover percent.

## Rest

Manages sitting down to med when not in combat and mana or endurance is below 60%.

## Pet

Manages summoning a pet as necessary, when not in combat.
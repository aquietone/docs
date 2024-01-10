# TLO

AQO Bot settings can be accessed via the `AQO` TLO:

## General Settings

| DataType | Member           | Type     | Description                                                        | Example                             |
|----------|------------------|----------|--------------------------------------------------------------------|-------------------------------------|
| AQOType  | ToString         | string   | Output the current status and mode of AQO                          | /echo ${AQO}                        |
|          | Paused           | boolean  | Output the current paused value                                    | /echo ${AQO.Paused}                 |
|          | Mode             | string   | The mode to run as: 0,manual,1,assist,2,chase,3,vorpal,4,tank,5,pullertank,6,puller,7,huntertank | /echo ${AQO.Mode} |
|          | ChaseTarget      | string   | Name of the person to chase in chase mode. Its using an exact match spawn search for PC's only | /echo ${AQO.ChaseTarget} |
|          | ChaseDistance    | int      | Distance threshold to trigger chasing the chase target | /echo ${AQO.ChaseDistance} |
|          | ChasePaused      | bool     | Chase the chase target while paused | /echo ${AQO.ChasePaused} |
|          | CampRadius       | int      | The radius within which you will assist on mobs | /echo ${AQO.CampRadius} |
|          | Assist           | string   | Who to assist. Group MA, Raid MA 1, 2 or 3 | /echo ${AQO.Assist} |
|          | AutoAssistAt     | int      | Mob Percent HP to begin assisting | /echo ${AQO.AutoAssistAt} |
|          | AssistNames      | string   | Comma separated, ordered list of names to assist, mainly for manual assist mode in raids. | /echo ${AQO.AssistNames} |
|          | SwitchWithMA     | bool     | Swap targets if the MA swaps targets | /echo ${AQO.SwitchWithMA} |
|          | NukeManaMin      | int      | Minimum mana threshold to pause casting nukes | /echo ${AQO.NukeManaMin} |
|          | DoTManaMin       | int      | Minimum mana threshold to pause casting DoTs | /echo ${AQO.DoTManaMin} |
|          | LootMobs         | bool     | Toggle looting of mob corpses on or off for emu | /echo ${AQO.LootMobs} |
|          | LootCombat       | bool     | Toggle looting of mob corpses during combat on or off for emu | /echo ${AQO.LootCombat} |
|          | MainTank         | bool     | Toggle use of tanking abilities in case main tank role doesn\'t work, like on emu | /echo ${AQO.MainTank} |
|          | ResistStopCount  | int      | The number of resists after which to stop trying casting a spell on a mob | /echo ${AQO.ResistStopCount} |
|          | Timestamps       | bool     | Enable timestamps on log messages | /echo ${AQO.Timestamps} |

## Heal Settings

| DataType | Member         | Type    | Description                                                        | Example                             |
|----------|----------------|---------|--------------------------------------------------------------------|-------------------------------------|
| AQOType  | HealPct        | int     | The Percent HP to begin casting normal heals on a character | /echo ${AQO.HealPct} |
|          | PanicHealPct   | int     | The Percent HP to begin casting panic heals on a character | /echo ${AQO.PanicHealPct} |
|          | GroupHealPct   | int     | The Percent HP to begin casting group heals | /echo ${AQO.GroupHealPct} |
|          | GroupHealMin   | int     | The number of group members which must be injured to begin casting group heals | /echo ${AQO.GroupHealMin} |
|          | HoTHealPct     | int     | The Percent HP to begin casting HoTs on a character | /echo ${AQO.HoTHealPct} |
|          | RezGroup       | bool    | Toggle rezzing of group members | /echo ${AQO.RezGroup} |
|          | RezRaid        | bool    | Toggle rezzing of raid members | /echo ${AQO.RezRaid} |
|          | RezInCombat    | bool    | Toggle use of rez abilities during combat | /echo ${AQO.RezInCombat} |
|          | PriorityTarget | string  | For EMU, where group main tank role is unreliable, assign a character name to treat like the main tank | /echo ${AQO.PriorityTarget} |
|          | XTargetHeal    | bool    | Toggle healing of PCs on XTarget | /echo ${AQO.XTargetHeal} |

## Burn Settings

| DataType | Member        | Type   | Description                                                        | Example                             |
|----------|---------------|--------|--------------------------------------------------------------------|-------------------------------------|
| AQOType  | BurnAlways    | bool   | Burn routine is always entered and burn abilities are used as available. Its not great, it doesn't attempt to line up CDs or anything | /echo ${AQO.BurnAlways} |
|          | BurnPct       | int    | Same as Burn Always, but only after mob HP is below this percent | /echo ${AQO.BurnPct} |
|          | BurnAllNamed  | bool   | Enter burn routine when ${Target.Named} is true. Kinda sucks with ToL zones since so many akhevan trash mobs return true | /echo ${AQO.BurnAllNamed} |
|          | BurnCount     | int    | Enter burn routine when greater than or equal to this number of mobs are within camp radius | /echo ${AQO.BurnCount} |
|          | UseGlyph      | bool   | Toggle use of Glyph of Destruction on burns | /echo ${AQO.UseGlyph} |
|          | UseIntensity  | bool   | Toggle use of Intensity of the Resolute Veteran AA on burns | /echo ${AQO.UseIntensity} |

## Pull Settings

| DataType | Member         | Type    | Description                                                        | Example                             |
|----------|----------------|---------|--------------------------------------------------------------------|-------------------------------------|
| AQOType  | PullWith       | string  | How to pull mobs. May be one of melee, ranged, spell | /echo ${AQO.PullWith} |
|          | PullRadius     | int     | The radius within which you will pull mobs when in a puller role | /echo ${AQO.PullRadius} |
|          | PullHigh       | int     | The upper Z radius for pulling mobs when in a puller role | /echo ${AQO.PullHigh} |
|          | PullLow        | int     | The lower Z radius for pulling mobs when in a puller role | /echo ${AQO.PullLow} |
|          | PullArc        | int     | The pull arc, centered around the direction the character is currently facing, to pull mobs from | /echo ${AQO.PullArc} |
|          | PullMinLevel   | int     | The minimum level mob to pull when in a puller role | /echo ${AQO.PullMinLevel} |
|          | PullMaxLevel   | int     | The maxmimum level mob to pull when in a puller role | /echo ${AQO.PullMaxLevel} |
|          | GroupWatchWho  | string  | Who to watch mana/endurance for, to decide whether to hold pulls and med | /echo ${AQO.GroupWatchWho} |
|          | GroupStayClose | bool    | Toggle whether puller should hold pulls if a group member is not with the group | /echo ${AQO.GroupStayClose} |

## Rest Settings

| DataType | Member           | Type  | Description                                                        | Example                             |
|----------|------------------|-------|--------------------------------------------------------------------|-------------------------------------|
| AQOType  | RecoverPct       | int   | Percent mana or endurance to trigger recover abilities | /echo ${AQO.RecoverPct} |
|          | MedCombat        | bool  | Toggle whether to med during combat. If on, character will still heal, tank, cc, debuff and buff, just not assist. | /echo ${AQO.MedCombat} |
|          | MedHPStart       | int   | The Percent HP to begin medding at | /echo ${AQO.MedHPStart} |
|          | MedHPStop        | int   | The Percent HP to stop medding at | /echo ${AQO.MedHPStop} |
|          | MedManaStart     | int   | The Percent Mana to begin medding at | /echo ${AQO.MedManaStart} |
|          | MedManaStop      | int   | The Percent Mana to stop medding at | /echo ${AQO.MedManaStop} |
|          | MedEndStart      | int   | The Percent Endurance to begin medding at | /echo ${AQO.MedEndStart} |
|          | MedEndStop       | int   | The Percent Endurance to stop medding at | /echo ${AQO.MedEndStop} |
|          | ManastoneStart   | int   | Percent Mana to begin spamming manastone (EMU only) | /echo ${AQO.ManastoneStart} |
|          | ManastoneStop    | int   | Minimum Percent HP to begin spamming manastone (EMU only) | /echo ${AQO.ManastopStop} |
|          | ManastoneStartHP | int   | Percent HP to stop spamming manastone (EMU only) | /echo ${AQO.ManastoneStartHP} |
|          | ManastoneStopHP  | int   | Duration, in seconds, to spam manastone (EMU only) | /echo ${AQO.ManastoneStopHP} |

## Display Settings

| DataType | Member    | Type    | Description                                                        | Example                             |
|----------|-----------|---------|--------------------------------------------------------------------|-------------------------------------|
|          | Theme     | string  | Pick a UI color scheme | /echo ${AQO.Theme} |
|          | Opacity   | number  | Set the window opacity | /echo ${AQO.Opacity} |
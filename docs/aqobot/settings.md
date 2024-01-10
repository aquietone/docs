# Settings

## Common Settings

| **Name** | **Description** | **Example** |
| :---| :--- | :--- |
| **Mode** | Manual, Assist or Chase. (Other modes still a work in progress.. pullertank sort of works on warrior as of writing) | `/aqo mode 0` |
| **Camp Radius** | The radius within which you will assist on mobs | `/aqo campradius 60` |
| **Chase Target** | Type in a PC name of the person to chase in chase mode. Its using an exact match spawn search for PC's only | `/aqo chasetarget ${Group.MainAssist}` |
| **Chase Distance** | Distance threshold to trigger chasing the chase target | `/aqo chasedistance 30` |
| **ChasePaused** | Chase the chase target while paused | `/aqo chasepaused on` |
| **Assist** | Who to assist. Group MA, Raid MA 1, 2 or 3 | `/aqo assist group` |
| **Auto Assist At** | Mob Percent HP to begin assisting | `/aqo autoassistat 98` |
| **Switch With MA** | Swap targets if the MA swaps targets. A bit odd, but this will also trigger manual mode to assist... makes it a bit like a vorpal mode? assists without chasing or setting a camp | `/aqo switchwithma on` |
| **NukeManaMin** | Minimum mana threshold to pause casting nukes | `/aqo nukemanamin 15` |
| **DoTManaMin** | Minimum mana threshold to pause casting DoTs | `/aqo dotmanamin 15` |
| **Spell Set** | Set the spell set to be loaded, different classes have different options | `/aqo spellset standard` |
| **Use Alliance** | Toggle whether to attempt using alliance spells | `/aqo usealliance on` |
| **Main Tank** | For EMU, where group main tank role is unreliable, toggle use of main tank abilities | `/aqo maintank on` |
| **Loot Mobs** | For EMU, where there is no Advanced Loot, toggle looting of mobs | `/aqo lootmobs on` |
| **LootCombat** | For EMU, toggle looting of mob corpses during combat on or off for emu | `/aqo lootcombat on` |
| **ResistStopCount** | The number of resists after which to stop trying casting a spell on a mob | `/aqo resiststopcount 3` |
| **Timestamps** | Enable timestamps on log messages | `/aqo timestamps on` |

## Heal Settings

| **Name** | **Description** | **Example** |
| :---| :--- | :--- |
| **Heal Percent** | The Percent HP to begin casting normal heals on a character | `/aqo healpct 85` |
| **Panic Heal Percent** | The Percent HP to begin casting `panic` heals on a character | `/aqo panichealpct 30` |
| **Group Heal Percent** | The Percent HP to begin casting group heals | `/aqo grouphealpct 70` |
| **Group Heal Min** | The number of group members which must be injured to begin casting group heals | `/aqo grouphealmin 2` |
| **HoT Heal Percent** | The Percent HP to begin casting HoTs on a character | `/aqo hothealpct 95` |
| **Priority Target** | For EMU, where group main tank role is unreliable, assign a character name to treat like the main tank | `/aqo prioritytarget <name>` |
| **Rez Group** | Toggle rezzing of group members | `/aqo rezgroup on` |
| **Rez Raid** | Toggle rezzing of raid members | `/aqo rezraid on` |
| **Rez In Combat** | Toggle use of rez abilities during combat | `/aqo rezincombat on` |
| **XTargetHeal** | Toggle healing of PCs on XTarget | `/aqo xtargetheal on` |

## Burn Settings

| **Name** | **Description** | **Example** |
| :---| :--- | :--- |
| **Burn Always** | Burn routine is always entered and burn abilities are used as available. Its not great, it doesn't attempt to line up CDs or anything | `/aqo burnalways off` |
| **Burn All Named** | Enter burn routine when ${Target.Named} is true. Kinda sucks with ToL zones since so many akhevan trash mobs return true | `/aqo burnallnamed on` |
| **Burn Count** | Enter burn routine when greater than or equal to this number of mobs are within camp radius | `/aqo burncount 5` |
| **Burn Percent** | Same as Burn Always, but only after mob HP is below this percent | `/aqo burnpct 95` |
| **Use Glyph** | Toggle use of Glyph of Destruction on burns | `/aqo useglyph on` |
| **Use Intensity** | Toggle use of Intensity of the Resolute Veteran AA on burns | `/aqo useintensity on` |

## Pull Settings

| **Name** | **Description** | **Example** |
| :---| :--- | :--- |
| **Pull Radius** | The radius within which you will pull mobs when in a puller role | `/aqo pullradius 250` |
| **Pull Z Low** | The lower Z radius for pulling mobs when in a puller role | `/aqo pulllow 10` |
| **Pull Z High** | The upper Z radius for pulling mobs when in a puller role | `/aqo pullhigh 25` |
| **Pull Min Level** | The minimum level mob to pull when in a puller role | `/aqo pullminlevel 115` |
| **Pull Max Level** | The maxmimum level mob to pull when in a puller role | `/aqo pullmaxlevel 124` |
| **Pull Arc** | The pull arc, centered around the direction the character is currently facing, to pull mobs from | `/aqo pullarc 360` |
| **PullWith** | How to pull mobs. May be one of melee, ranged, spell | `/aqo pullwith melee` |
| **Group Watch Who** | Who to watch mana/endurance for, to decide whether to hold pulls and med | `/aqo groupwatchwho <healer,self,none>` |
| **GroupStayClose** | Toggle whether puller should hold pulls if a group member is not with the group | `/aqo groupstayclose on` |

## Rest Settings

| **Name** | **Description** | **Example** |
| :---| :--- | :--- |
| **Recover Percent** | Percent mana or endurance to trigger recover abilities | `/aqo recoverpct 40` |
| **MedCombat** | Toggle whether to med during combat. If on, character will still heal, tank, cc, debuff and buff, just not assist. | `/aqo medcombat on` |
| **MedHPStart** | The Percent HP to begin medding at | `/aqo medhpstart 50` |
| **MedHPStop** | The Percent HP to stop medding at | `/aqo medhpstop 80` |
| **Med Mana Start** | The Percent Mana to begin medding at | `/aqo medmanastart 5` |
| **Med Mana Stop** | The Percent Mana to stop medding at | `/aqo medmanastop 30` |
| **Med End Start** | The Percent Endurance to begin medding at | `/aqo medendstart 5` |
| **Med End Stop** | The Percent Endurance to stop medding at | `/aqo medendstop 30` |
| **ManastoneStart** | Percent Mana to begin spamming manastone (EMU only) | `/aqo manastonestart 50` |
| **ManastoneStop** | Minimum Percent HP to begin spamming manastone (EMU only) | `/aqo manastonestop 90` |
| **ManastoneStartHP** | Percent HP to stop spamming manastone (EMU only) | `/aqo manastonestarthp 50` |
| **ManastoneStopHP** | Duration, in seconds, to spam manastone (EMU only) | `/aqo manastonestophp 30` |

## Display Settings

| **Name** | **Description** | **Example** |
| :---| :--- | :--- |
| **Theme** | Pick a UI color scheme | `/aqo theme teal` |
| **Opacity** | Set the window opacity | `/aqo opacity 100` |
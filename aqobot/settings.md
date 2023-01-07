# Settings

## Common Settings

| **Name** | **Description** | **Example** |
| :---| :--- | :--- |
| **Mode** | Manual, Assist or Chase. (Other modes still a work in progress.. pullertank sort of works on warrior as of writing) | `/aqo mode 0` |
| **Camp Radius** | The radius within which you will assist on mobs | `/aqo campradius 60` |
| **Chase Target** | Type in a PC name of the person to chase in chase mode. Its using an exact match spawn search for PC's only | `/aqo chasetarget ${Group.MainAssist}` |
| **Chase Distance** | Distance threshold to trigger chasing the chase target | `/aqo chasedistance 30` |
| **Assist** | Who to assist. Group MA, Raid MA 1, 2 or 3 | `/aqo assist group` |
| **Auto Assist At** | Mob Percent HP to begin assisting | `/aqo autoassistat 98` |
| **Switch With MA** | Swap targets if the MA swaps targets. A bit odd, but this will also trigger manual mode to assist... makes it a bit like a vorpal mode? assists without chasing or setting a camp | `/aqo switchwithma on` |
| **Spell Set** | Set the spell set to be loaded, different classes have different options | `/aqo spellset standard` |
| **Use Alliance** | Toggle whether to attempt using alliance spells | `/aqo usealliance on` |
| **Main Tank** | For EMU, where group main tank role is unreliable, toggle use of main tank abilities | `/aqo maintank on` |
| **Recover Percent** | Percent mana or endurance to trigger recover abilities | `/aqo recoverpct 40` |
| **Loot Mobs** | For EMU, where there is no Advanced Loot, toggle looting of mobs | `/aqo lootmobs on` |

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
| **Pull Arc** | The maxmimum level mob to pull when in a puller role | `/aqo pullarc 360` |
| **Group Watch Who** | The maxmimum level mob to pull when in a puller role | `/aqo groupwatchwho <healer|self|none>` |
| **Med Mana Start** | The maxmimum level mob to pull when in a puller role | `/aqo medmanastart 5` |
| **Med Mana Stop** | The maxmimum level mob to pull when in a puller role | `/aqo medmanastop 30` |
| **Med End Start** | The maxmimum level mob to pull when in a puller role | `/aqo medendstart 5` |
| **Med End Stop** | The maxmimum level mob to pull when in a puller role | `/aqo medendstop 30` |

## Heal Settings

| **Name** | **Description** | **Example** |
| :---| :--- | :--- |
| **Heal Percent** | The maxmimum level mob to pull when in a puller role | `/aqo healpct 85` |
| **Panic Heal Percent** | The maxmimum level mob to pull when in a puller role | `/aqo panichealpct 30` |
| **Group Heal Percent** | The maxmimum level mob to pull when in a puller role | `/aqo grouphealpct 70` |
| **Group Heal Min** | The maxmimum level mob to pull when in a puller role | `/aqo grouphealmin 2` |
| **HoT Heal Percent** | The maxmimum level mob to pull when in a puller role | `/aqo hothealpct 95` |
| **Priority Target** | The maxmimum level mob to pull when in a puller role | `/aqo prioritytarget <name>` |
| **Rez Group** | The maxmimum level mob to pull when in a puller role | `/aqo rezgroup on` |
| **Rez Raid** | The maxmimum level mob to pull when in a puller role | `/aqo rezraid on` |
| **Rez In Combat** | The maxmimum level mob to pull when in a puller role | `/aqo rezincombat on` |

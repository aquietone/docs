# Settings

## Common Settings

| **Name** | **Description** | **Example** |
| :---| :--- | :--- |
| **Mode** | Manual, Assist or Chase. (Other modes still a work in progress.. pullertank sort of works on warrior as of writing) | `/docommand /${Me.Class.ShortName} mode 0` |
| **Camp Radius** | The radius within which you will assist on mobs | `/docommand /${Me.Class.ShortName} campradius 60` |
| **Chase Target** | Type in a PC name of the person to chase in chase mode. Its using an exact match spawn search for PC's only | `/docommand /${Me.Class.ShortName} chasetarget ${Group.MainAssist}` |
| **Chase Distance** | Distance threshold to trigger chasing the chase target | `/docommand /${Me.Class.ShortName} chasedistance 30` |
| **Assist** | Who to assist. Group MA, Raid MA 1, 2 or 3 | `/docommand /${Me.Class.ShortName} assist group` |
| **Auto Assist At** | Mob Percent HP to begin assisting | `/docommand /${Me.Class.ShortName} autoassistat 98` |
| **Switch With MA** | Swap targets if the MA swaps targets. A bit odd, but this will also trigger manual mode to assist... makes it a bit like a vorpal mode? assists without chasing or setting a camp | `/docommand /${Me.Class.ShortName} switchwithma on` |
| **Spell Set** | Set the spell set to be loaded, different classes have different options | `/docommand /${Me.Class.ShortName} spellset standard` |
| **Use Alliance** | Toggle whether to attempt using alliance spells | `/docommand /${Me.Class.ShortName} usealliance on` |

## Burn Settings

| **Name** | **Description** | **Example** |
| :---| :--- | :--- |
| **Burn Always** | Burn routine is always entered and burn abilities are used as available. Its not great, it doesn't attempt to line up CDs or anything | `/docommand /${Me.Class.ShortName} burnalways off` |
| **Burn All Named** | Enter burn routine when ${Target.Named} is true. Kinda sucks with ToL zones since so many akhevan trash mobs return true | `/docommand /${Me.Class.ShortName} burnallnamed on` |
| **Burn Count** | Enter burn routine when greater than or equal to this number of mobs are within camp radius | `/docommand /${Me.Class.ShortName} burncount 5` |
| **Burn Percent** | Same as Burn Always, but only after mob HP is below this percent | `/docommand /${Me.Class.ShortName} burnpercent 95` |

## Pull Settings

| **Name** | **Description** | **Example** |
| :---| :--- | :--- |
| **Pull Radius** | The radius within which you will pull mobs when in a puller role | `/docommand /${Me.Class.ShortName} radius 250` |
| **Pull Z Low** | The lower Z radius for pulling mobs when in a puller role | `/docommand /${Me.Class.ShortName} zlow 10, /docommand /${Me.Class.ShortName} zradius 50` |
| **Pull Z High** | The upper Z radius for pulling mobs when in a puller role | `/docommand /${Me.Class.ShortName} zhigh 25`, `/docommand /${Me.Class.ShortName} zradius 50` |
| **Pull Min Level** | The minimum level mob to pull when in a puller role | `/docommand /${Me.Class.ShortName} levelmin 115` |
| **Pull Max Level** | The maxmimum level mob to pull when in a puller role | `/docommand /${Me.Class.ShortName} levelmax 124` |

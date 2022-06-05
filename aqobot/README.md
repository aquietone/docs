# AQOBot

[View Repo](https://gitlab.com/aquietone/aqobot){target=_blank}  
[Download](https://gitlab.com/aquietone/aqobot/-/archive/main/aqobot-main.zip){target=_blank}  

EverQuest class automation Lua scripts for MacroQuest.

![](../images/aqobot/aqobot.png)

## Overview

Provides a CWTN-like interface for bard, necro, ranger, shadow knight and warrior (so far) class automation with assist and chase modes, pre-configured spells, discs, AAs and abilities to use, and a UI to control a handful of settings.  

Each of the class files, `brd.lua`, `nec.lua`, `rng.lua`, `shd.lua` and `war.lua` includes a number of tables for spells, AAs, discs and items. Hopefully its clear from the naming which are for burns, which are standard rotations, mash abilities, etc.

## Installation

1. Clone the repo or download the zip file linked above.  
2. Move `aqo.lua` and the `aqo` folder into the MQ `lua` folder  

## Commands

- `/lua run aqo` -- Start the script  
- `/docommand /${Me.Class.ShortName} mode 0` -- To set mode to manual  
- `/docommand /${Me.Class.ShortName} mode 1` -- To set mode to assist  
- `/docommand /${Me.Class.ShortName} mode 2` -- To set mode to chase  
- `/docommand /${Me.Class.ShortName} pause on` -- To pause  
- `/docommand /${Me.Class.ShortName} pause off` -- To resume  
- `/docommand /${Me.Class.ShortName} show` -- To show the UI  
- `/docommand /${Me.Class.ShortName} hide` -- To hide the UI  
- `/docommand /${Me.Class.ShortName} burnnow` -- To enable burns on demand  
- `/docommand /${Me.Class.ShortName} setting_name setting_value` -- To set the value of `setting_name` to `setting_value`  
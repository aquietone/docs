# AQOBot

[View Repo](https://github.com/aquietone/aqobot){target=_blank}  
[Download - EMU](https://github.com/aquietone/aqobot/releases/tag/aqo-nightly){target=_blank}  
[Download - Live Servers (Outdated)](https://github.com/aquietone/aqobot/archive/refs/heads/main.zip){target=_blank}  

EverQuest class automation Lua scripts for MacroQuest. 

!!! info
    I originally began writing these for live servers but stopped playing on live a few months into ToL expansion.
    At that time, necromancer, bard, shadow knight, warrior and ranger were mostly functional.
    The Live Servers download includes what was developed up to that point.  

    Since then I have been playing on EMU servers and so all new additions have been on the `emu` branch, which includes many more classes but those only include abilities up to level 70.  

![](../images/aqobot/aqo_console_tab_b.png) ![](../images/aqobot/aqo_skills_tab.png)

## Overview

Provides a CWTN-like interface for class automation with assist and chase modes, pre-configured spells, discs, AAs and abilities to use, and a UI to control a handful of settings.  

Each of the class files found in `aqo/classes` folder includes a number of tables for spells, AAs, discs and items. Hopefully its clear from the naming which are for burns, which are standard rotations, mash abilities, etc.

!!! Features
    * Full group automation with tanking, pulling, assisting, chasing and hunting roles.
    * In-game configuration through UI and command line.
    * Predefined lists of abilities for healing, tanking, DPS'ing, burning, etc.
    * Add your own clickies with `/addclicky`
    * Buff begging
    * Automated looting and selling capabilities

## Installation

1. Clone the repo or download the zip file linked above.  
2. Move the `aqo` folder into the MQ `lua` folder  

## Usage

`/lua run aqo`

## Images

![](../images/aqobot/aqo_console_tab.png) ![](../images/aqobot/aqo_general_tab.png)
![](../images/aqobot/aqo_skills_tab.png) ![](../images/aqobot/aqo_heals_tab.png)
![](../images/aqobot/aqo_burn_tab.png) ![](../images/aqobot/aqo_pull_tab.png)
![](../images/aqobot/aqo_rest_tab.png) ![](../images/aqobot/aqo_display_tab.png)
![](../images/aqobot/aqo_debug_tab.png)
![](../images/aqobot/aqo_ability_inspector.png) ![](../images/aqobot/aqo_state_inspector.png) ![](../images/aqobot/aqo_clicky_manager.png)
![](../images/aqobot/helpcmd.png) ![](../images/aqobot/helpui.png)

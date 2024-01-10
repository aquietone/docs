# Getting Started

## MacroQuest

Check out [MacroQuest](https://docs.macroquest.org/) if you are interested in building it for yourself, otherwise head to [RedGuides](https://redguides.com) for a more streamlined experience.

## Lua Scripts

MacroQuest added support for [Lua](https://www.lua.org/) scripts as an alternative to the existing macro scripting language. In addition to all the capabilities available to macros, these also have the ability to use [ImGui](https://github.com/ocornut/imgui) to create new UI windows to go with the scripts.

## Installing a Lua Script

### Manual Install
Lua scripts may come packaged as either a single `.lua` file download such as `eval.lua` or as a zipped folder such as `boxhud.zip`.  

* Downloads consisting of a single `.lua` file should be placed directly into the MQ `lua` folder, or wherever the resource specific install instructions instruct for files to be placed.  
* Downloads consisting of a zip file should be unzipped, and the resulting folder should be placed into the MQ `lua` folder, or wherever the resource specific install instructions instruct for files to be placed.

### RedGuides Launcher
1. Navigate to the resource page for a given Lua script, such as BoxHUD, and click the `Watch` button on the `Overview` tab.  
2. Open the RedGuides Launcher and install the Lua resource from the `Lua` tab.

> NOTE: Some scripts may perform additional install steps when they are run, such as prompting the user to accept the download of a separate `dll` file such as `lfs.dll`.

## Running a Lua Script

* `/lua run scriptname` where `scriptname` is the launch script for the resource, such as `eval` or the name of the unzipped folder such as `boxhud`.

## Autostart Lua Scripts

### For *ALL* Characters:

1. Right click your MQ tray icon in the taskbar and select `Open Folder` > `Config`  
2. Create a new file `ingame.cfg`, or open it if you already have one.  
3. Add the line `/lua run scriptname` where `scriptname` is the script you want to run, such as `boxhud` or `lem`.  
4. Save and close the file.  
5. Test in game by running `/loadcfg ingame.cfg` or by logging in a character.  

### For a *SPECIFIC* Character:

1. Right click your MQ tray icon in the taskbar and select `Open Folder` > `Config`  
2. Create a new file `server_Character.cfg`, or open it if you already have one, where `server` is replaced with your EQ server short name, and `Character` is replaced with your character name. For example, `rizlona_Dudebro.cfg`.  
3. Add the line `/lua run scriptname` where `scriptname` is the script you want to run, such as `maui` or `luabard`.  
4. Save and close the file.  
5. Test in game by running `/loadcfg server_Character.cfg` or log in the character.  

> NOTE: If you created `ingame.cfg` or `server_Character.cfg` using `Notepad`, like by right clicking in your config folder and selecting `New` > `Text Document`, then the file was probably saved with the wrong file extension, like `ingame.cfg.txt`. You will need to remove the `.txt` file extension before it will work.

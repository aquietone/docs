# Commands

* `/lua run aqo` -- Start the script  

The script binds both `/aqo` and `/${Me.Class.ShortName}` commands, the latter for compatibility with CWTN plugins and use of `cwtn`/`cwtna` aliases.  
For example, as a necromancer, the following command formats all have the same result:  

* `/aqo mode 0`  
* `/nec mode 0`  
* `/docommand /${Me.Class.ShortName} mode 0`  

All commands documented from this point forward will be shown with `/aqo` for simplicity.  

* `/aqo mode <0|manual|1|assist|2|chase|3|vorpal|4|tank|5|pullertank|6|puller|7|huntertank>` -- To set the mode. e.g. to set to chase mode, `/aqo mode chase` or `/aqo mode 2`.  
* `/aqo pause <1|true|on|0|false|off>` -- To pause or resume the script. e.g. to pause, `/aqo pause 1`.  
* `/aqo <show|hide>` -- To show or hide the UI window.  
* `/aqo resetcamp` -- To reset the centerpoint of the camp to your current location.  
* `/aqo burnnow` -- To enable burns on demand.  
* `/aqo addclicky <mash|burn|buff|heal>` -- Adds the currently held item to the clicky group specified.  
* `/aqo removeclicky` -- Removes the currently held item from clickies.  
* `/aqo ignore` -- Adds the targeted mob to the ignore list for the current zone.  
* `/aqo unignore` -- Removes the targeted mob from the ignore list for the current zone.  
* `/aqo sell` -- Sells items marked to be sold to the targeted or already opened vendor.  
* `/aqo <setting_name> <setting_value>` -- To set the value of `setting_name` to `setting_value`.  
* `/aqo update` -- Downloads the latest source zip.  
* `/aqo docs` -- Launches the documentation site in a browser window.  
* `/aqo restart` -- Restart the lua script.

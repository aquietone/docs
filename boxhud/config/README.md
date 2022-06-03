# Configuration

Boxhud configuration is stored in a separate Lua file per character, within the Boxhud folder. It shouldn't be necessary to open the file for anything, as all the configuration can be done in game, but if you want to keep a backup or your settings, or find it easier to edit the file to add configuration, it is stored in lua/boxhud/settings/boxhud-settings-charactername.lua.

By default, boxhud-settings.lua is included with the script. Upon startup, it will be copied to the character specific file boxhud-settings-charactername.lua.
An existing boxhud-settings-charactername.lua will always take precedence over boxhud-settings.lua.

Configuration is recommended to be done using the Configuration tab in the HUD. All options can be edited in the appropriate settings lua file for a character, but its easier to visualize the settings in game.

When editing settings in the configuration tab, each individual item (column, property or tab) is saved immediately to the settings file when clicking the save button for the item.

Boxhud configuration is broken up into 4 main sections: Properties, Columns, Tabs and Windows.
- Properties define what data you want to watch in the HUD. These can include DanNet observed properties, NetBots properties and Spawn properties.
- Columns define the display settings for a given property, such as whether it should only show for characters in the same zone as you, or whether it is a percentage value. They can also be used to define value mappings to display different text based on the value returned for a property.
- Tabs define a group of columns to be displayed together.
- Windows define the UI windows that will be drawn. By default, there is only one window, but more windows can be added which each can watch different DanNet peer groups or include different tabs.
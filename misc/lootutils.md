# Lootutils

A Lua port of NinjAdvLoot.inc. It handles looting, selling and banking tradeskill items using the same INI configuration as the macro include did.

Some settings were ported over from the old include, some not. I only kept working on the script until it was far enough along for my own purposes.

Usage:

```lua
local loot = require('lootutils.lua')

-- main loop of your own script
while true do
  loot.lootMobs()
end
```

```lua
local do_sell = false

-- bind callback for your script, accepting a 'sell' command like '/myscript sell'
local function cmd_callback(command)
  if command == 'sell' then
    do_sell = true
  end
end

-- main loop of your own script
while true do
  if do_sell then loot.sellStuff() end
end
```

The script can also be run standalone with a loop, or as a run once and exit.

More details are provided in the script.

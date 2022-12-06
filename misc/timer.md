# Lua Timer Library

Provides a simple timer implementation.

Usage:

```lua
local mq = require('mq')
local timer = require('timer')

local myTimer = timer:new(5)
-- Start time defaults to 0 rather than current time, so timers start expired
-- Why? Just because I guess.
myTimer:reset()

print(os.time())
while not myTimer:timer_expired() do
  mq.delay(1000)
end
print(os.time())

print('Waited 5 seconds until myTimer expired')
```

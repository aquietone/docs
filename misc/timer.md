# Lua Timer Library

Provides a simple timer implementation.

Usage:

```lua
local mq = require('mq')
local timer = require('timer')

local myTimer = timer:new(5)

print(os.time())
while not myTimer:timer_expired() do
  mq.delay(1000)
end
print(os.time())

print('Waited 5 seconds until myTimer expired')
```

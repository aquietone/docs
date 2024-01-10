# Debugger

[View Repo](https://github.com/aquietone/misclua){target=_blank}  
[Download](https://raw.githubusercontent.com/aquietone/misclua/main/debugger.lua)  

![](../images/debugger/debugger.png)

## Overview

This lua script is meant to be used in a broader script, providing a debug window that outputs the current stack trace and local variables and highlights when variables change.

## Installation

Download the zip and extract it, placing `debugger.lua` into your own scripts folder to be used as a module.

## Usage

```lua
-- Include the module to your script
local Debugger = require('debugger')

-- Create a new instance of debugger and enable it
local debugFunctionValues = Debugger.new('Functions')
debugFunctionLocals:Enable()

local function some_function(input1, input2, input3)
    local x
    -- Pass local variables of the current function to the debugger instance
    debugFunctionLocals:SetFunctionLocals('some_function', debugFunctionLocals:getlocals())
end

-- Create a new instance of debugger and enable it
local debugTableValues = Debugger.new('Tables')
debugTableValues:Enable()

local some_table = {a_value=1, nested_table={b_value=100000}}
-- Pass a table variable to the debugger
debugTableValues:AddWatchedTable('some_table', some_table)

-- Generate some data that changes over time so the debugger has something to show
while true do
    mq.delay(1000)
    some_table.a_value = some_table.a_value + 1
    some_table.nested_table.b_value = some_table.nested_table.b_value - 1
    some_function(some_table.a_value, some_table.nested_table.b_value, some_table)
end
```
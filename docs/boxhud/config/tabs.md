# Tab Configuration

Tabs define the individual tabs which can be switched between in BoxHUD. For example, the default tabs are `General`, `Macro` and `XP`.  
Each tab includes a name and list of columns to be included in that tab, for example:

```lua
{
    Name='General',
    Columns={
        {
            Name='HP%',
            ...
        }
    }
},
```

Tabs can be configured directly in the HUD configuration tab:

![](../../images/boxhud/addtab.png)

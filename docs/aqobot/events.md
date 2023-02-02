# AQOBot Events

Events are used for several features, including buff begging (requesting buffs from a character running aqo) and broadcasting worn gear.  

Each event below will trigger when someone tells you via group, raid, guild or a direct tell due to the `#*#`.  
Buff request events must come from a character who is in your group, raid or guild and is in the same zone.  
Gear request events can come from anyone, and **responses will be in guild chat**. I play on EMU, with my own guild for my characters, so for me this is fine. If you were playing on live, you would probably not want to use this.  

## Buff Requests

Buff requests will trigger off of the following text events:  

* `#1# tells #*#, \'#2#\'` Where `#1#` is the name of the character requesting the buff and `#2#` is the buff being requested.  

The set of available buffs which can be requested can be found in each class lua file by searching for `addRequestAlias`, or by requesting `list buffs`, e.g. `/tell someone list buffs`.  
Requested buff names can also be prefixed with `tranquil` or `mgb` such as `tranquilaego` to trigger the use of `Tranquil Blessings` or `Mass Group Buff` AA's before casting the buff.  

* `#1# tells #*#, \'tranquil\'` Command the character to use their `Tranquil Blessings` AA.

## Gear Information

* `'#*# tells #*#, \'gear #2#\'`

This event can be used to have characters broadcast their gear so that you can easily review who has what in a given slot. Its basically the same thing as `/status` command for outputting gear.  

Valid Slot Names:  

- earrings  
- rings  
- leftear  
- rightear  
- leftfinger  
- rightfinger  
- face  
- head  
- neck  
- shoulder  
- chest  
- feet  
- arms  
- leftwrist  
- rightwrist  
- wrists  
- charm  
- powersource  
- mainhand  
- offhand  
- ranged  
- ammo  
- legs  
- waist  
- hands  
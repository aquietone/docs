# General Settings

## PeerSource
This can be set to `dannet` or `netbots` to specify whether the list of peers to display in the HUD should come from `MQ2DanNet` or `MQ2NetBots`.

## RefreshInterval
Configure the delay for polling observed properties. Used in `mq.delay()` call.
Default: `250` (0.25 seconds)

## StaleDataTimeout
Configure the time in seconds before stale entries are removed from the displayed data.
Default: `60`

## Text Colors
The colors of various parts of the HUD are configurable under General Settings in the configuration tab:

1638001012645.png

The default color will be for any column that doesn't fall under any of the other categories.  
`Low`, `Medium` and `High` threshold colors are for columns with number values that have 1 or 2 thresholds defined.
Name, Name invis and Name not in zone colors are for the Name column only.
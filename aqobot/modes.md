# Modes

Characters may run under 1 of 7 different modes at any given time. Modes shamelessly borrowed from CWTN plugins.

## Manual

Characters in manual mode will not attempt to do anything on their own when out of combat except cast buffs. If a character enters combat (you manually turn on attack), then they will enter into combat routines as if they had assisted.

## Assist

Characters in assist mode will remain within the configured camp and assist the main assist on any mob within the camp radius as long as the assist conditions are met.

## Chase

Characters in chase mode will stay within the configured chase distance of the chase target at all times, and assist the main assist on any mob within the configured `CAMPRADIUS` distance from the character.

## Vorpal

Characters in vorpal mode will not attempt to stay within a configured camp, but also will not chase the chase target. They will assist on mobs within the configured `CAMPRADIUS` distance from the character, but otherwise must be moved around through some other means between combat.

## Tank

Characters in tank mode will engage new mobs that enter the camp radius.

## PullerTank

Characters in puller tank mode will engage mobs that enter the camp radius, and pull mobs within the configured pull radius when there are no mobs in camp.

## HunterTank

Characters in hunter tank mode will continuously move to and engage mobs in place within the configured pull radius.
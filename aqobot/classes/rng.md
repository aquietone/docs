# AQOBot Ranger

The script provides support for level 120 Rangers. 

## Settings

| **Name** | **Description** | **Example** |
| :-- | :----- | :--- |
| **Use Melee** | Control whether to melee mobs. If you only ever want to ranged, then leave this off | `/rng usemelee on` |
| **Use Range** | Control whether to bow mobs. If you only ever want to melee, then leave this off. If ranged is enabled, ranged will always take precedence over melee | `/rng userange on` |
| **Use Unity (Azia)** | Buff self with Wildstalker's Unity (Azia) AA. Cannot be enabled at the same time as Beza | `/rng useunityazia on` |
| **Use Unity (Beza)** | Buff self with Wildstalker's Unity (Beza) AA. Cannot be enabled at the same time as Azia | `/rng useunitybeza on` |
| **Buff Group** | Cast shout and enrichment buffs on group. Does not cope well with blocked buffs but hopefully checks stacking properly otherwise | `/rng buffgroup on` |
| **Use Regen** | Cast regen buff on self | `/rng useregen on` |
| **DS Tank** |  Cast DS on the group main tank | `/rng dstank on` |
| **Use Poison Arrows** | Buff self with Poison Arrows AA. Cannot be enabled at the same time as Flaming Arrows | `/rng usepoisonarrow on` |
| **Use Flaming Arrows** | Buff self with Flaming Arrows AA. Cannot be enabled at the same time as Poison Arrows | `/rng usefirearrow on` |
| **Use DoT** | Controls whether to cast the high mana cost DoT on mobs. My rangers gear is bad, so dotting all the things is expensive | `/rng usedot on` |
| **Use Nukes** | Controls whether to cast nukes on mobs | `/rng nuke on` |
| **Use Dispel** | Controls whether to dispel mobs. Will use Entropy of Nature AA on mobs above 90% HP when enabled | `/rng usedispel on` |
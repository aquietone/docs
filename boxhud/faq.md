# FAQ

Q. Why can't `lfs.dll` be found when starting the script?

A. If the script errors loading `lfs.dll`, then you may need to install the [VC Redist package from Microsoft](https://www.microsoft.com/en-us/download/details.aspx?id=48145&e6b34bbe-475b-1abd-2c51-b5034bcdd6d2=True)


Q. What builds does this run on?

A. Currently this only works on MQ for live and test.


Q. Boxhud fails to start with error `Could not find script at path C`

A. Make sure you downloaded the resource and added the files to your lua folder


Q. Why are buttons not responding or the window can't be moved around?

A. Most likely a bug with ImGui and mouse inputs, and it thinks a mouse button is stuck pressed. Cycle through clicking all the buttons on your mouse.


Q. Why are values not updating properly for one or more characters?

A. Crashes, going LD, relogging, etc seem to screw up DanNet observers sometimes, and they don't appear to be removed properly or don't get added back properly when the character comes back online. Either go to the Admin tab on boxhud and reload the observers for the misbehaving character or reload the dannet plugin on the character running boxhud and it should hopefully fix the issue.


Q. Can boxhud be launched at startup?

A. To Run the script at login for a given character:


1. If you don't already have a character config file for the character which will run boxhud, create a file in your next/config folder like `servername_Charactername.cfg`, for example, `rizlona_Aquietone.cfg`
2. Add the following line to the file:

```ini
/timed 100 /lua run boxhud
```

Q. Why does boxhud cause characters macros to throw errors about undefined variables?

A. By default, Boxhud will observe each configured property on all characters. Observing a property which doesn't exist on a character, for example, observing CWTN.Mode on a Bard, will cause undefined variable errors when trying to run a macro on the Bard. To avoid this, filters should be applied to the property to define which characters the property should be observed for.
For example, when adding the property CWTN.Mode, the DependsOnName and DependsOnValue fields can be set to restrict what classes CWTN.Mode will be observed for:

```ini
Property: CWTN.Mode
DependsOnName: Me.Class.ShortName
DependsOnValue: clr,shm,war,shd,mnk,rog,ber
```

Note that the observer is created from the character that is running boxhud, so if your driver toon is running boxhud and trying to observe CWTN.Mode on the bard, you would need to fix the property on boxhud on your driver toon to not observe the property for bards.


Q. Why does boxhud still cause characters macros to throw errors about undefined variables even after limiting what classes the property applies to?

A. If you swap toons, like going from an enchanter to a bard on the same account, DanNet still seems to think its trying to watch whatever properties it was watching before you swapped characters. Boxhud on your driver toon doesn't know you swapped toons on some other account to try and resolve it for you automatically. Try reloading the dannet plugin on the swapped character.


Q. Should anything and everything be added to boxhud?

A. Try to just add vital information that is frequently updated. No need to go adding a bunch of static info about characters that will rarely ever change. For ideas of what can be added, check out the MQ TLO documentation here: [MacroQuest Docs](https://docs.macroquest.org/reference/top-level-objects/){.new-tab}
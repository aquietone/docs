# FAQ

**Q. Why wasn't the previous level INI copied forward after leveling?**  
A. If you start the MuleAssist macro and it doesn't find your current level INI, it will generate a new empty current level INI. If this happens, and then you start MAUI, then MAUI will just find this new empty current level INI and read it, rather than copying a previous level INI. In order for MAUI to copy an old INI for you, there must NOT already be a current level INI, empty or otherwise.  

**Q. How to make MAUI launch at login?**  
A. Refer to overview or instructions tabs.  

**Q. Why can't lfs.dll be found when starting the script?**  
A. If the script errors loading lfs.dll, then you may need to install the [VC Redist package from Microsoft](https://www.microsoft.com/en-us/download/details.aspx?id=48145&e6b34bbe-475b-1abd-2c51-b5034bcdd6d2=True){target=_blank}  
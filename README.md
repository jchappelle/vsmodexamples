# Vintage Story Server Mod Samples and Boilerplate

This repository contains 2 sample mods and a neatly configured Visual Studio project that let's you start Vintage Story and test your mod 
directly from within Visual Studio.
- You might need to fix the path to the refence VintagestoryAPI.dll. It always ships with the game. The default installation path is %appdata%/Vintagestory
- In the Projects settings->Debug the full path to Vintagestory.exe is configured. Please adjust this one to your install path.
- There is a post build event that copies the .dll and .pdb files into %appdata%/VintageStory/Mods. You only need to touch that one if you installed vintage story somewhere else
- A command line argument /flatworld is set in the Debug tab as well. It cause Vintagestory to automatically start a superflat creative world for you to test the mod. A few other command line args are available
  - */flatworld* - always creates a new flat world
  - */flatworld:test*  - open a world named "test", if it doesn't exists it will create a  new flat world
  - */stdworld*   - always creates a new standard world generator world
  - */stdworld:test*  - open a world named "test", if it doesn't exists it will create a new world using the standard worldgenerator
- A tiny mod RedirectLogs.cs is included that redirects the log output into the visual studio output window for developement and testing. You should not ship your mod with this one. 
- Even [Edit&Continue](https://msdn.microsoft.com/en-us/library/bcew296c.aspx) should work just fine \o/

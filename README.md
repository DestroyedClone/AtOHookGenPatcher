# BepInEx.MonoMod.HookGenPatcher

Generates [MonoMod.RuntimeDetour.HookGen's](https://github.com/MonoMod/MonoMod) `MMHOOK` file during the [BepInEx](https://github.com/BepInEx/BepInEx) preloader phase. 

Installation:
Put in `BepInEx\patchers` folder.
Make sure the `MonoMod.exe` and `MonoMod.RuntimeDetour.HookGen.exe` files are also present.

**This project is not officially linked with BepInEx nor with MonoMod.**

License:
You may freely distribute this for any purpose. Note that MonoMod files are needed for succesful execution, and different licensing rules may apply to those.

## See also:
[LighterPatcher](https://github.com/harbingerofme/LighterPatcher) which is designed to easy the load on the game when having particularily large MMHOOK files by stripping unneeded types. LighterPatcher and HookGenPatcher work in conjuction with each other to prevent multiple runs.

## Differences between source
- Only things for the *releases* have been updated, since I'm not sure how to recompile the plugin or if it's necessary.
- Fixed Initializer error by packing release with different monomod
` [Error  :   BepInEx] Failed to run Initializer of BepInEx.MonoMod.HookGenPatcher.HookGenPatcher: System.IO.FileNotFoundException: Could not load file or assembly 'MonoMod, Version=20.5.21.5, Culture=neutral, PublicKeyToken=null' or one of its dependencies.
File name: 'MonoMod, Version=20.5.21.5, Culture=neutral, PublicKeyToken=null'
  at BepInEx.Preloader.Patching.AssemblyPatcher.InitializePatchers () [0x0001e] in <fc9d7fbc6dcb44cf87be11d8d92ae161>:0 `
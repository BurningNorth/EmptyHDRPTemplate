# Empty HDRP Template
An empty HDRP project template for Unity 2020.3 LTS.
-----
In an ideal world, starting a new High Definition RP project in Unity would mean simply creating the project, deleting all the sample content, and getting to work. Unfortunately, the default template includes a number of project-wide settings that directly reference the sample assets, which can cause unexpected behavior if you just delete those assets.

Untangling this stuff takes less than an hour, but if you're like me and you like to spin up lots of quick prototype projects in rapid succession, it gets tedious real fast. So instead, I created this *actually* empty HDRP project in Unity 2020.3.2f1. You can fork this repo if you want, but you may prefer to just [download the zip archive](https://github.com/BurningNorth/EmptyHDRPTemplate/archive/refs/heads/main.zip) so you can start a fresh repo for your own project.

From the Unity Hub, I created a **High Definition RP** project and made the following changes:

- Added the `UserSettings` folder to .gitignore (GitHub's premade .gitignore for Unity doesn't include this)
- Moved **HDRP\*Quality.asset** files from `Assets/SampleSceneAssets/Settings` to `Assets/HDRPDefaultResources/Settings`
- Moved **VolumeGlobal.asset** from `Assets/SampleSceneAssets/Settings/Volumes` to `Assets/HDRPDefaultResources/Settings/Volumes` and renamed it to **DefaultVolumeProfile.asset**
- Replaced the contents of **Diffusion Profile List** with default assets from the HDRP package
- Changed **Fixed Timestep** from `0.02` to `0.01666667` to match the 60Hz tick rate elsewhere in the engine
- Created **BlankScene.unity** in `Assets/Scenes` from the **Basic Outdoors** template
- Deleted **SampleScene.unity** and the `Assets/SampleSceneAssets` folder
- Deleted a missing AudioImporter preset from **Preset Manager**

At the time of writing this README, the entire project is under 700 KB on disk. That's quite an improvement over the 100+ MB just for the Assets folder of the High Definition RP template! I hope this encourages you to try more quick, silly things in Unity, without having to repeat this process every time you start.

:heart: **George Kokoris (Burning North)**

## Installation
### Easy Method

* Ensure you have the latest verion of [BeatSaberModManager](https://github.com/affederaffe/BeatSaberModManager/releases) or [ModAssistant](https://github.com/Assistant/ModAssistant/releases)
* Launch the mod installer
* Select the checkbox for Custom Platforms
* Click Install
### Manual Method

* Ensure your game is patched with BSIPA (ModAssistant does this for you)
* Place the CustomPlatforms.dll in your Beat Saber\Plugins directory

After a relaunch, your Beat Saber folder should look like this:

```
| Beat Saber
  | Plugins
    | CustomPlatforms.dll             <-- 
  | CustomPlatforms		      <--
    | <.plat files>		      <--
  | IPA
  | Beat Saber.exe
  | (other files and folders)
```

## Controls

Visit the Platforms Menu page ingame to change your platform for different gamemodes

## Adding More Platforms

Place platforms (.plat) files in the "BeatSaber\CustomPlatforms" folder.
Your installed platforms will be available after a few seconds.
A possible source for platforms is [ModelSaber](https://modelsaber.com/Platforms/?pc).

## Creating New Platforms

There's a comprehensive guide at https://bsmg.wiki/models/platforms-guide.html written by Emma.
The following are the basic steps:

1. Download the Unity project from [Releases](https://github.com/affederaffe/CustomPlatforms/releases/latest), unzip it.

2. Open the Unity project
The project was created and tested in version [2019.3.15f1](https://unity3d.com/get-unity/download/archive), other versions may not be supported.

3. Create an empty GameObject and attach a "Custom Platform" component to it.
Fill out the fields for your name and the name of the platform.  You can also toggle the visibility of default environment parts if you need to make room for your platform.
Add an icon for your platform by importing an image, settings it to Sprite/UI in import settings, and dragging it into the icon field of your CustomPlatform

4. Create your custom platform as a child of this root object
You can use most of the built-in Unity components, custom shaders and materials, custom meshes, animators, etc.

1. When you are finished, select the root object you attached the "Custom Platform" component to.
In the inspector, click "Export". Navigate to your CustomPlatforms folder, and press save.

6. Share your custom platform with other players by uploading the Platforms' .plat file

## Building
1. Clone the repository with ```git clone https://github.com/affederaffe/CustomPlatforms.git```
2. Go to the ```./CustomPlatforms/Plugin/CustomFloorPlugin``` direcory and create a ```CustomFloorPlugin.csproj.user``` file, see the example below
3. Open the solution file in the ```Plugins``` directory with e.g. VisualStudio or Jetbrains Rider and build the project

#### Example csproj.user File:
```xml
<?xml version="1.0" encoding="utf-8"?>
<Project ToolsVersion="Current" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  <PropertyGroup>
    <BeatSaberDir>Full\Path\To\Beat Saber</BeatSaberDir>
  </PropertyGroup>
</Project>
```

## Hall of Fame (Credits for major rework contributions)
#### AkaRaiden - (The QA Department, Beta Tester, Tome of Wisdom)
  - Without him this would have taken so much more time than it did.

#### Rolo - (The Master Mind, Inventor CustomPlatforms)
  - Went out of her way to help me clean up after six people messed with this.

#### Panics - (Chief Investigator)
  - Helped me get an initial grasp on the damage.

#### Tiruialon - (Top-Cat)
  - Thank you for your contributions!
 
#### boulders2000 - (Bug Hunter)
  - Stopped counting how many bugreports he sent.

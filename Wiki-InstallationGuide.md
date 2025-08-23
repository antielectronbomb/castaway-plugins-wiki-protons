## Intro

Page under construction

> ## Content
> - [Needed files](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Installing-the-Weapon-Reverts-Plugin#needed-files)
> - [Installation](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Installing-the-Weapon-Reverts-Plugin#installation)
>	- [Source Dedicated Server](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Installing-the-Weapon-Reverts-Plugin#source-dedicated-server)
>	- [MetaMod and SourceMod](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Installing-the-Weapon-Reverts-Plugin#metamod-and-sourcemod)
>	- [Compiling](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Installing-the-Weapon-Reverts-Plugin#compiling)
> - [See also](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Installing-the-Weapon-Reverts-Plugin#see-also)

## Needed Files
- 32 bit server/sourcemod - 64 bit not currently supported
- TF2Items: https://forums.alliedmods.net/forumdisplay.php?f=146
- TF2Attributes: https://github.com/FlaminSarge/tf2attributes
- TFUtils: https://github.com/nosoop/SM-TFUtils
- TF2 Condition Hooks: https://github.com/Scags/TF2-Condition-Hooks
	- Modified source file (!!!Use this or it will not work!!!): https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/blob/master/scripting/tf2condhooks.sp
	- Gamedata (!!!Use this or it will not work!!!): https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/blob/master/gamedata/tf2.condmgr.txt
- Source Scramble: https://github.com/nosoop/SMExt-SourceScramble

## Installation

### Source Dedicated Server
1. This video guide (recommended for the non-technically inclined): https://youtu.be/mc0kx3JUeKg
2. TF2 Wiki Dedicated Server Guide
	- (Windows): https://wiki.teamfortress.com/wiki/Windows_dedicated_server
    - (Linux): https://wiki.teamfortress.com/wiki/Linux_dedicated_server

### MetaMod and SourceMod
- SourceMod: https://www.sourcemod.net/downloads.php?branch=stable
- MetaMod: https://www.sourcemm.net/downloads.php?branch=master&all=1

- Extract files to your corresponding server folder. Here's a video guide on installing SourceMod plugins
https://youtu.be/QF7urRJIgrE

### Compiling
#### Pre-compiled
- See Actions page, click the latest workflow (topmost), go to Artifacts, download either 1.12 or 1.13 depending on what SourceMod version you have.

#### Manual compiling
- For the Castaway version, you will need to manually compile the reverts.sp file into reverts.smx using the built-in SourceMod compiler program. 
	- You can compile plugins in Windows by pressing right-click in the Explorer and opening CMD, then typing "spcomp WIN32= reverts.sp". 
	- For Linux, I am assuming you know how to do this.
- The files and folders that matter in the Castaway GitHub are: cfg, configs, gamedata, scripting (which contains reverts.sp), & translations (which contains the reverts.phrases.txt).

### Running the Server

## See also
- [Useful Links on Running the Reverts Plugin in Your Own Server](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Useful-Links-on-How-to-Run-TF2-Weapon-Reverts-in-Your-Own-Server)

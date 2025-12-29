## Intro

<img alt="image" src="https://github.com/user-attachments/assets/0f5a02c1-a05b-4418-9e70-834048f14fd8" />

An example of a server running the Extended Weapon Reverts plugin

> ## Content
> - [Needed files](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Installing-the-Weapon-Reverts-Plugin#needed-files)
> - [Installation](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Installing-the-Weapon-Reverts-Plugin#installation)
>	- [Source Dedicated Server](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Installing-the-Weapon-Reverts-Plugin#source-dedicated-server)
>	- [MetaMod and SourceMod](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Installing-the-Weapon-Reverts-Plugin#metamod-and-sourcemod)
>	- [Compiling](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Installing-the-Weapon-Reverts-Plugin#compiling)
> - [See also](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Installing-the-Weapon-Reverts-Plugin#see-also)
> - [Additional Notes](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Installing-the-Weapon-Reverts-Plugin#additional-notes)

## Needed Files
- 32 bit server/sourcemod - 64 bit not currently supported
- TF2Items (**Only copy-paste the files, compiling tf2items_manager.sp is NOT needed**): https://forums.alliedmods.net/forumdisplay.php?f=146
- TF2Attributes (must be compiled): https://github.com/FlaminSarge/tf2attributes
- TFUtils (must be compiled): https://github.com/nosoop/SM-TFUtils
- TF2 Condition Hooks (must be compiled): https://github.com/Scags/TF2-Condition-Hooks
	- Modified source file (!!!Use this or it will not work!!!): https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/blob/master/scripting/tf2condhooks.sp
	- Gamedata (!!!Use this or it will not work!!!): https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/blob/master/gamedata/tf2.condmgr.txt
- Source Scramble (must be compiled): https://github.com/nosoop/SMExt-SourceScramble
- More Colors (the include file is needed): https://forums.alliedmods.net/showthread.php?t=185016

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

- Regardless of which method you use for compiling, make sure you have the needed dependencies installed.
- Obviously, you need to install both SourceMod and MetaMod.
- Next are the **dependencies that need to be compiled from their respective .sp files**. These are:
	- TF2Attributes
	- TFUtils
	- TF2 Condition Hooks
	- Source Scramble
- After that, you need to install the other dependencies. Installation is just a simple copy-paste, and there is no need for compiling their .sp files:
	- TF2Items
	- More Colors
- Once you have the dependencies installed, you may proceed to run the pre-compiled plugin, or compile the reverts.sp plugin yourself. Compiling it yourself is recommended.

#### Pre-compiled
- See Actions page, click the latest workflow (topmost), go to Artifacts, download either 1.12 or 1.13 depending on what SourceMod version you have.

#### Manual compiling
- For the Castaway version, you will need to manually compile the reverts.sp file into reverts.smx using the built-in SourceMod compiler program. 
	- You can compile plugins in Windows by pressing right-click in the Explorer and opening CMD, then typing `spcomp WIN32= reverts.sp`. 
	- For Linux, I am assuming you know how to do this.
	- In case TF2 updates and it breaks the weapon reverts plugin, try disabling memory patch reverts first `NO_MEMPATCHES=`, as these reverts are most likely to break when TF2 items:
		- `spcomp NO_MEMPATCHES= reverts.sp`
			- If the plugin does work after disabling memory patches, make sure you notify to this GitHub via Issues (or better yet, a Pull Request that fixes the error) since that means the gamedata folder will need updating.
- The files and folders that matter in the Castaway GitHub and **must be installed** are: 
	- cfg
	- configs
	- gamedata
	- scripting (which contains reverts.sp)
	- translations (which contains the reverts.phrases.txt)
- **COPY PASTE EVERYTHING. ALWAYS COPY AND PASTE ALL THE FOLDERS MENTIONED ABOVE.** Most errors when trying to install the weapon reverts plugin is because the other folders like the translations folder wasn't installed.
- **If you do not follow the above instructions, you will get missing file errors.** All folders must be copied and pasted.

### Running the Server & Checking the Plugin
- Once installation is complete, you may now try running the plugin on your server.
- When first starting up the server, make sure you pay extra attention to the server console for any errors that may pop up.
- After the server loads in all the plugins and such, type the following commands:
	- `sm version` - Check if you have SourceMod in the server. Should be either version 1.12 or version 1.13.
	- `sm plugins list` - Check for `"TF2 Weapon Reverts Extended" (x.x.x-<OS NAME HERE>32) by Bakugo, NotnHeavy, random, huutti, VerdiusArcana, MindfulProtons, EricZhang456` somewhere in the list. 
	- If the server is on Windows, it should state Windows at the end, and for Linux, it should state Linux at the end.
		- Additionally, check for the following plugins in the plugins list (version numbers should be the latest as much as possible):
		- `"TF2 Utils" (x.x.x) by nosoop`
		- `"Source Scramble Manager" (x.x.x) by nosoop`
		- `"[TF2] Condition Manager" (x.x.x) by Scag` (this corresponds to TF2 Condition Hooks mentioned earlier)
		- `"[TF2] TF2Attributes" (x.x.x) by FlaminSarge`
	- Once these plugins are listed, the reverts plugin should be hopefully be installed without problems.
- Next, confirm if the memory patch weapon reverts work correctly. Connect to the server you set up.
	- When you spawn in the game, the description for a reverted weapon should pop up in the text chat.
	- Type `!reverts` in text chat to see if the menu works and test out the options. If your game runs on a supported language, the info should display in the corresponding language.
	- Type `!revertsinfo` or `sm_revertsinfo` to see the full list of weapons currently reverted in the Developer Console.
	- The fastest way to check is to switch to the Sandvich (assuming the plugin uses the default settings), taking some self-damage by jumping off a high ledge (or via hurtme with sv_cheats 1), dropping the Sandvich via alt-fire, then picking it up to see if it heals you.
	- Another quick way to check if the memory patches work is to go Sniper, use any Sniper Rifle primary, scope in, shoot, then jump immediately to test out the Sniper Jump Scope revert. If you're able to jump immediately after firing a scoped shot, the memory patches should be working correctly.
	- If you want to fully test out all the memory patch based reverts, try testing out these weapons and see if their behavior matches the reverts description:
	- Make sure you have the weapon you want to test out enabled. Check out the [weapon reverts list](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Revert-List) for their cvar keys.
		- All Flamethrowers
		- All Miniguns
		- All Sniper Rifles
		- Cozy Camper
		- Crusaders Crossbow
		- Dalokohs Bar (Variant 1)
		- Disciplinary Action
		- Dragon's Fury
		- Gunslinger
		- Iron Bomber
		- Mad Milk
		- Quick-Fix
		- _This list of memory patch based reverts might not be updated. Check out reverts.sp and look for [reverts that are inside #if and #endif lines](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/blob/64fc6663707a776aa5ebcdb01530c1ee34587ab2/scripting/reverts.sp#L573)._
- Finally, after confirming everything works as intended, you may now want to set up which weapons you want to be reverted. Check out the [weapon reverts list](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Revert-List) and the [available reverted weapon server config pre-sets](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Config-Presets)

### Additional notes
- The weapon reverts plugin is not fully tested on Mann vs. Machine mode and in Freaky Fair. The plugin technically works in those modes, but there will be bugs.
- Make sure the specifications of your TF2 server can handle the reverts plugin. The plugin might use _some_ resources, especially when bundled with other plugins. Always check the CPU and RAM usage of your server.
- Hard-restarting the server in case bugs pop up with the reverts plugin over time may fix those bugs.
- If there are any problems that come up, please go to the [Castaway.tf Steam Group Forums and list your problem in this thread](https://steamcommunity.com/groups/castawaytf/discussions/0/601891815092704779/). 
- Running the server on Linux is recommended over running it on Windows with the plugin. Windows servers tend to have issues.

## See also
- [Useful Links on Running the Reverts Plugin in Your Own Server](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Useful-Links-on-How-to-Run-TF2-Weapon-Reverts-in-Your-Own-Server)

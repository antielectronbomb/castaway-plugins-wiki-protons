## Purpose
[File can be found here](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/blob/master/scripting/reverts.sp)

This plugin is the main feature of this repo. It features weapon reverts to various eras, in hopes of getting weapons in their most fun state.

By default all reverts are on, but they can be toggled off using cvars (see below).

Additionally, certain weapons have different variants for reverting to different time periods. This is also controlled with cvars.

> ### Contents
> * [Purpose](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-(reverts.sp)#purpose)
> * [Installation and Set-up](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-(reverts.sp)#installation-and-set-up)
>	* [Dependencies](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-(reverts.sp)#dependencies)
>	* [CVars](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-(reverts.sp)#cvars)
>	* [Variants](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-(reverts.sp)#variants)
>	* [Compiling](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-(reverts.sp)#compiling)
> * [Memory Patches](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-(reverts.sp)#memory-patches)
> 	* [Reverts that use memory patches](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-(reverts.sp)#reverts-that-use-memory-patches)
> * [Contributing/Modding](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-(reverts.sp)#contributingmodding)
> 	* [Reverts requiring special code](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-(reverts.sp)#reverts-requiring-special-code)
> * [See also](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-(reverts.sp)#see-also)

## Installation and Set-up
Before installing the Weapon Reverts plug-in, first make sure the following dependencies are installed first in your server:
### Dependencies
- 32 bit server/sourcemod - 64 bit not currently supported
- [TF2Items](https://github.com/nosoop/SMExt-TF2Items)
- [TF2Attributes](https://github.com/FlaminSarge/tf2attributes)
- [TF2Utils](https://github.com/nosoop/SM-TFUtils)
- [TF2 Condition Hooks](https://github.com/Scags/TF2-Condition-Hooks) ([modified source file](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/blob/master/scripting/tf2condhooks.sp), [gamedata](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/blob/master/gamedata/tf2.condmgr.txt)) - Make sure to use the modified source file and gamedata, as these are the updated versions that should work with the plugin.
- [Source Scramble](https://github.com/nosoop/SMExt-SourceScramble) - Only required if using the memory patches (see [below](#Memory-Patches) for more info)

### CVars
To start off with, create the file `tf/cfg/sourcemod/reverts.cfg` on your server. 

You may also use [preset weapon reverts config files](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Config-Presets) which also contain templates for selecting what weapon reverts you wish to use.

Each revert can be modified using a cvar like so:
```cfg
sm_reverts__item_<name> 0/1/2/etc.
```
- 0: Off
- 1: On (default, don't need to put a line for this)
- 2: Variant #1
- 3: Variant #2
- etc.

To get the name to use, consult [reverts.sp](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/blob/master/scripting/reverts.sp) and scroll down to the `ItemDefine` block. You will find lines like this:
```sourcepawn
ItemDefine("Ambassador", "ambassador", "Reverted to pre-inferno, deals full headshot damage (102) at all ranges", CLASSFLAG_SPY, Wep_Ambassador);
```
The second parameter, in this case "ambassador", will be used for the cvar. So, to disable the ambassador revert, you would do the following in your `reverts.cfg`:
```cfg
sm_reverts__item_ambassador 0
```
All weapon reverts are defined in the `ItemDefine` block, so you can use it as a quick check to see all available reverts.
### Variants
Some weapons have variants. Variants can be controlled by setting the cvar to a number greater than 1. As of writing this, no item has more than 1 variant, meaning you'll only need to put 2 at most for given item.

Example:
```sourcepawn
ItemDefine("Axtinguisher", "axtinguish", "Reverted to pre-love&war, always deals 195 damage crits to burning targets, no speedboost on kill", CLASSFLAG_PYRO, Wep_Axtinguisher);
ItemVariant(Wep_Axtinguisher, "Reverted to pre-toughbreak, crits from behind, minicrits from front, no speedboost on kill");
```
This means that the Axtinguisher has one variant. The base version, the one shown in the `ItemDefine`, is variant 0, which means you don't need to set anything to use it. Although it's redundant, the cvar would look like this:
```cfg
sm_reverts__item_axtinguisher 1
```
The variant identifier is the nth `ItemVariant` declaration starting from 1 (the base version is variant 0).

In this case, the variant has a value of 1, meaning to use it you would set the following in your `reverts.cfg`:
```cfg
sm_reverts__item_axtinguisher 2
```
### Compiling
By default the plugin will compile for Linux, and will work on Linux servers with no additional adjustments. 

Since the Linux and Windows server binaries are different, the memory patches are necessarily different and have different byte changes. As such, you will need to compile the plugin for your specific server architecture.

As mentioned above, the default behavior is to compile for Linux. To compile for windows, uncomment the following line near the top of `reverts.sp`:
```
//#define WIN32
```
Alternatively, you can simply pass `WIN32=` as a command line argument when compiling the plugin.

The github repo also automatically compiles the reverts plugin each time there is a commit. As of writing this, there is no link to where these can be downloaded.

## Memory Patches
Certain reverts require memory patches to function. These are more involved reverts that require code changes and can't be accomplished simply with attribute changes. These reverts are done using the source scramble plugin, and make targeted byte changes to the server binary.

As such, these reverts are prone to breaking if there are any TF2 updates that have code updates. Not all updates will result in breakage, but if they do, memory patches can be disabled by commenting out the following line at the top of the `reverts.sp` file:
```
#define MEMORY_PATCHES
```
Alternatively, you can simply pass `NO_MEMPATCHES=` as a command line argument when compiling the plugin.
### Reverts that use memory patches
- Heavy Minigun ramp up (All miniguns)
- Cozy Camper
- Dragon's Fury
- Disciplinary Action
- Quick-Fix
- Wrangler
- Rescue Ranger
## Contributing/Modding
There are a few things to note if you want to set up a new weapon revert or variant.

For regular weapons, there are 4 locations you will need to edit for the plugin to function correctly:

**1 - Weapon Enum**

Near the top there is an enum used for identifying weapons for use later in the code. Preferably alphabetized, and make sure `NUM_ITEMS` is always the last value in the enum.

**2 - ItemDefine**

To actually initialize the weapon you'll need an `ItemDefine` call. There's a block in `OnPluginStart` where these are all performed. Also preferably alphabetized. 
ItemDefine params:
1. Name of the revert. Used in any info like chat messages or console info dumps
2. Revert cvar identifier. This is used for the name of the cvar that can be used to toggle the revert on/off
3. Description. Preferably include the time period of the revert, describes what exactly the revert does
4. Class Flags. This identifies which weapon this revert is for. Used for revert info dumping
5. Weapon Enum

ItemVariant params:
1. Weapon Enum
2. Description. Used in place of the base description

**3 - OnGiveNamedItem (attributes)**

This section is where you set the actual attributes for your reverted weapon.

When adding a new item, make sure to get the weapon's index. It can be found in `tf/scripts/item/items_game.txt`, though there is a helpful page on the AlliedModder's wiki which lists all item indexes in a more readable and searchable format. [Link to the AlliedModders page](https://wiki.alliedmods.net/Team_fortress_2_item_definition_indexes). Note that weapon reskins, and sometimes different weapon qualities, will be considered different indexes, so ensure you note down all of them.

Make sure to follow the pattern provided by the other items, set the `NumAttributes` correctly, and ensure the indexes in `SetAttribute` are unique. 

The following is what a well formed attribute block looks like:
```sourcepawn
case 450: { if (ItemIsEnabled(Wep_Atomizer)) {
	item1 = TF2Items_CreateItem(0);
	TF2Items_SetFlags(item1, (OVERRIDE_ATTRIBUTES|PRESERVE_ATTRIBUTES));
	TF2Items_SetNumAttributes(item1, 4);
	TF2Items_SetAttribute(item1, 0, 5, 1.30); // fire rate penalty
	TF2Items_SetAttribute(item1, 1, 138, 0.80); // dmg penalty vs players
	TF2Items_SetAttribute(item1, 2, 250, 0.0); // air dash count
	TF2Items_SetAttribute(item1, 3, 773, 1.0); // single wep deploy time increased
}}
```

**4 - OnGameEvent - post_inventory_application (caching block)**

This block is what tells the plugin which reverts a player has equipped. It is used for any weapons that have special code related reverts that aren't handled just by attributes, but also for information dumps.

Ensure you use the correct enum, and that all the correct weapon indexes are checked. See the above section for more info on indexes.

An example of a well formed cache case:
```sourcepawn
case 38, 47, 1000: player_weapons[client][Wep_Axtinguisher] = true;
```
Once you have done all of the above, your weapon should be good to go.

### Reverts requiring special code
If your weapon requires any special code, there are a few functions you can use for determining whether a player has a weapon or not and whether the weapon is enabled or not.

The `player_weapons` array can be used to determine if a player has a reverted weapon in their loadout, without needing to loop over their weapons. This method of checking is fast and should ideally be done near the start of an `if` statement to save on CPU, especially inside of functions that are called frequently.

Below is an example of checking if an item is enabled, and then checking if a player has the weapon equipped at all:
```sourcepawn
if(
	ItemIsEnabled(Wep_RocketJumper) &&
	victim == attacker &&
	damage_custom == TF_DMG_CUSTOM_TAUNTATK_GRENADE &&
	player_weapons[victim][Wep_RocketJumper]
) {
```

Item Variants can be acquired with `GetItemVariant`. This returns one less than the value of the cvar, which means that a value of `0` would be the base weapon with no variant, and a value of `1` would mean the first variant is active. This can be used in place of ItemIsEnabled if a weapon has variants.

Below is an example of checking for the base revert of the Soda Popper, the non-variant:
```sourcepawn
if (
	GetItemVariant(Wep_SodaPopper) == 0 &&
	players[client].is_under_hype
) {
```

## See also
* [Weapon Reverts Plugin Changelog](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Changelog)
* [Server Config Presets](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Config-Presets) - A guide on using preset weapon revert config files for toggling which weapon reverts you want on your own server as well as a template for creating your weapon reverts config
* [Weapon Reverts List & Other Cvars](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Revert-List) - Full detailed list of all weapon reverts available in the plugin, as well as linked historical references for each weapon.
# Extended Weapon Reverts Plugin Changelog
[![Weapon Reverts Plugin](https://github.com/user-attachments/assets/e010c79e-ebe2-41fb-838e-6398b9de5a6b)](https://www.youtube.com/watch?v=HWenueVOXZ0)

> ## Contents
> **Clicking on a month will jump to the earliest change log of that month.**
>
> **Specific dates can be selected by expanding the Pages box on the right side of the screen.**
>
> **2025**
> * [December 2025](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Changelog#december-2-2025)
> * [November 2025](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Changelog#november-4-2025)
> * [October 2025](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Changelog#october-1-2025)
> * [September 2025](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Changelog#september-1-2025)
> * [August 2025](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Changelog#august-1-2025)
> * [July 2025](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Changelog#july-1-2025)
> * [June 2025](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Changelog#june-2-2025)
> * [May 2025](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Changelog#may-1-2025)
> * [April 2025](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Changelog#april-4-2025)
> * [March 2025](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Changelog#march-9-2025)
> * [February 2025](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Changelog#february-2-2025)
> * [January 2025](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Changelog#january-10-2025)
>
> **2024**
> * [December 2024](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Changelog#december-12-2024)
> * [November 2024](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Changelog#november-11-2024)
> * [October 2024](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Changelog#october-10-2024)
>
> **[See also](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Changelog#see-also)**

## Changelog

_**NOTE: [Plugin] means a change applied to the weapon reverts plugin itself. [Server] means a change applied to the Castaway.tf game servers. [Plugin/Server] means changes are applied to both.**_

### December 29, 2025
- **[Server] Reverted for a trial period the Sandvich to pre-February 14, 2012, Blutsauger to release, Buff Banner to release, Equalizer/Escape Plan to pre-Hatless Update, Wrangler to pre-Love & War, and Rescue Ranger to pre-Tough Break.**
- **[Plugin] Fixed reverted Shortstop autoreload bug for shoveless variants by forcing a reload whenever alt-fire is pressed.**
- **[Plugin] Fixed reverted Ambassador long-range headshots not counting towards the headshot score. This only applies to every first headshot after the 1.0 s accuracy cooldown.**
- **[Plugin] Fully reverted the projectile hitboxes for both the Pomson 6000 and Righteous Bison variants back to the original 48x48x48 hammer units sized projectile cube hitbox.**
- **[Plugin] Edited the Release Pomson 6000 variant reverts info to include that it is supposed to fully drain the cloak meter of any Spy who is cloaked and/or disguised (does not fully drain against undisguised and uncloaked Spies), which was a historical bug. This means the full drain cloak bug is kept intentionally for historical accuracy.**
- **[Plugin] Added pre-February 14, 2008 quickscope revert for all Sniper Rifles. All Sniper Rifles are able to instantly do quickscope critical hit headshots even if the headshot occurs in less than 0.2 seconds.**
- **[Plugin] Added pre-Classless Update Sandman variant. Full stuns, can stun invulnerable players, stun victims receive 50% damage, no health penalty, no double jump, 15 sec ball recharge time.**
- **[Plugin] Added pre-Manniversary Persian Persuader variant. Picks up ammo as health (including metal from dropped ammo, 120 HP per drop, this means more HP from dropped weapons and building gibs), +100% charge recharge rate, no max ammo penalty, and can gain ammo from dispensers/carts.**
- **[Plugin] Cleaned up code**
- **[Plugin] Updated localization files, updated cfgs**

### December 25, 2025
- **[Plugin] Use new attribute to adjust the Tomislav firing sound pitch while retaining the visual inspectpanel attributes.**
- **[Plugin] Fixed being able to visually airblast (from the perspective of other players) right after spawning with the no-airblast variants of the Backburner.**

### December 19, 2025
- **[Plugin] Added historically accurate variant for reverted Amputator. This variant does not give Uber when healing via the taunt.**
- **[Plugin/Server] Huntsman taunt bug revert now uses a weapon revert cvar instead of a general cvar setting.**
- **[Plugin] Code cleanup**
- **[Plugin/Server] Updated localization files**

### December 14, 2025
- **[Plugin] Updated gamedata file for Windows. The plugin should work again in Windows servers.**

### December 10, 2025
- **[Plugin/Server] Fixed the plugin not working properly due to the recent Smissmas update.**
- **[Plugin/Server] Corrected Pre-Gun Mettle Dead Ringer cloak _armor_ duration from 6.5 s to 6.0 s (this does not affect the cloak time itself) (research done by num-get).**
	- Using the 2014 build of TF2, the Dead Ringer cloak used to flicker during the last quarter second of the duration.
	- The old Dead Ringer had a total cloak duration of 6.25 seconds, 6 seconds of super armor, and a quarter second of normal cloak. 100 / ( 10 * 1.6 ) = 6.25s
	- See this [pull request](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/pull/337) for more info.
- **[Plugin/Server] Added Huntsman staring contest bug revert.**
	- Spam the taunt button with another enemy Sniper and be stunned forever with the other Sniper until one Sniper gets tired of repeatedly pressing the taunt button and loses!
- **[Plugin] Updated localization files**

### December 7, 2025
- **[Plugin] Added pre-2012 Sandvich revert variant**
	- *Reverted to pre-2012, can heal self by throwing the Sandvich*
- **[Plugin] Updated localization files**

### December 3, 2025
- **[Plugin] Reworked B.A.S.E. Jumper revert, see [this](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/pull/333) for more information**

### December 2, 2025
- **[Server] Re-enabled Concheror revert and disabled Short Circuit revert on the Castaway.tf servers.**

### November 27, 2025
- **[Plugin/Server] Fixed Spy disguises not working properly which causes the disguised Spy to be in the reference pose. See this [issue](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/issues/27) for more information.**

### November 26, 2025
- **[Plugin] Added Sandvich revert**
  - *Reverted to pre-Engineer Update, heal yourself by eating/throwing the Sandvich, can be eaten forever unless thrown which must then be recharged via resupply or health kits*
- **[Plugin] Reverted Tomislav variants pre-Love&War have higher pitched weapon sounds**
  - Added a pre-Love&War variant
    - *Reverted to pre-love&war, 10% faster spinup, no accuracy bonus, 20% higher pitched weapon sounds*
  - Added a variant that only reverts the sound while keeping the vanilla stats
    - *Reverted only the firing sounds to pre-love&war, 20% higher pitched weapon sounds*
- **[Plugin] Added pre-Jungle Inferno Direct Hit variant (now the base version)**
  - *Reverted to pre-inferno, deals minicrits to airblasted targets again*
- **[Plugin] Added pre-Tough Break Sentry Gun revert**
  - *Reverted to pre-toughbreak, sentry is active immediately after being unsapped*
- **[Plugin] Added a mempatch-only ConVar that reverts cloak behaviour so spy can taunt and cloak (i.e old fence taunt cloak bug)**
- **[Plugin] Various code improvements!**
  - Cleaned up code for the 2009 Ambassador variants (no headshot cooldown, penetrates targets)
  - Equalizer damage bonus is now applied via attribute, fixes modified damage not being applied against everything and prevents code duplication
  - Rewrote Buffalo Steak Sandvich movespeed modification. Release Steak now functions correctly on speed boosts and with Eviction Notice's speed boost.
  - Phlog revert no longer uses the taunt DHook and all condition-related code is handled in the TF2CondHooks OnAddCond forward.
    - Post-Tough Break Phlogistinator's invuln and knockback immunity has the correct duration now.
  - Cleaned up code for Rescue Ranger revert
- **[Server] Enabled release Backburner revert (+50 HP, no airblast) on the Castaway.tf servers for a trial period.**

### November 20, 2025
- **[Plugin/Server] Fixed Quick-Fix uber sound loop bug which was caused by the Phlogistinator revert.**
- **[Plugin] Reworked Soda Popper Minicrits and Reserve Shooter code along with general code clean ups**
- **[Plugin] Added new reverts/variants**
	- **Rescue Ranger**
		- Pre-Tough Break Rescue Ranger
			- Reverted to pre-toughbreak, heals +75 flat for no metal cost (same 100 metal cost for long-range pickups)
	- **Ambassador**
		- Release Ambassador (May 21, 2009 to May 25, 2009)
			- Mini-crits on Headshots
			- No cooldowns
			- Penetrates enemy players
		- May 26, 2009 Ambassador (May 26, 2009 to June 23, 2009)
			- Crits on headshots
			- No cooldowns
			- Penetrates enemy players
	- **Dead Ringer**
		- Release Dead Ringer
			- Reverted to release, 90% dmg resist for 6.5s, no speedboost, no drain on early decloak, no afterburn immunity after feign
		- Pre-January 6, 2010 Dead Ringer
			- Reverted to pre-Jan 6, 2010; can fully pick up ammo, 90% dmg resist for 6.5s, no speedboost, up to 4%% drain on early decloak, no afterburn immunity after feign
	- **Blutsauger**
		- Release Blutsauger
			- Reverted to release, no passive health regen penalty, no random crits
	- **Tide Turner**
		- Pre-Smissmas 2014 Tide Turner
			- Reverted to pre-Smissmas 2014, can deal full crits, 25% blast and fire resist, crit after bash, no debuff removal, full bash dmg at end of charge, 100% charge on kill, no charge penalty when damaged
	- **Direct Hit**
		- Pre-December 22, 2009 Direct Hit
			- Reverted to pre-December 22, 2009; mini-crits all airborne and floating underwater targets regardless of cause; explosive jumps not needed for mini-crits
	- **Grenade Kamikaze Taunt Kill**
		- With Release Gunboats, the grenade taunt deals only 64 damage to the user
		- With Equalizer/Escape Plan without Release Gunboats and with taunt weapon switching turned on, the grenade taunt deals only 256 damage to the user (this means the user can survive the grenade taunt when overhealed)
	- **Dalokohs Bar**
		- Imported from NotnHeavy's
		- Pre-Gun Mettle Dalokohs Bar
			- Reverted to pre-gunmettle, instantly recharge after eating, cannot be dropped for health pick-ups via alt-fire
	- **Buff Banner**
		- Release Buff Banner
			- Reverted to release, +40% longer buff effect duration (from 10 sec to 14 sec), requires 1000 damage points (from 600 dmg)
	- **Scorch Shot**
		- Gun Mettle (pre-July 6, 2015) Scorch Shot
			- Reverted to pre-July 6, 2015 patch; no -35% self damage force penalty (higher blast jumping)
- **[Plugin] Updated localization files**

### November 12, 2025
- **[Server] Re-enabled the pre-Gun Mettle Short Circuit revert on the servers.**

### November 10, 2025
- **[Plugin] Added pre-JI Crusader's Crossbow revert (full uber gain on heal regardless if target recently took damage)**
- **[Plugin] Added pre-May 2025 Thermal Thruster revert (bunny hop stomping)**
- **[Plugin] Slightly reworked code for Righteous Bison revert**
- **[Plugin] Old Dead Ringer no longer has the passive 20% cloak resistance after the feign buffs expire**
- **[Server] Enabled Fists of Steel (release), Gunslinger (release) and Short Circuit (December 2013) reverts on the Castaway.tf servers for a trial period.**
- **[Server] Disabled the Concheror revert on the Castaway.tf servers.**

### November 4, 2025
- **[Plugin] Reworked Persian Persuader ammo conversion to health. Now activates crit boost from crit pumpkins as expected.**
- **[Plugin] Reverted Beggar's Bazooka (release) cannot gain ammo from Dispensers at all.**
- **[Plugin] Gunboats revert is now disabled by default.**
- **[Plugin] Updated localization files**

### October 26, 2025
- **[Plugin] Fixed pre-Gun Mettle Natascha inexplicably having spun-up damage resistance**
- **[Plugin] Pre-MyM Short Circuit: Slowed firing interval to 0.67 s (from 0.5 s), shows particle effects when alt-fire hits a player**
- **[Plugin] Grenade Launcher revert hit location damage variance happens only on the vertical axis**
- **[Plugin] Minor code refactoring**
- **[Plugin] Updated localization files**

### October 21, 2025
- **[Server] Enabled Gunslinger revert (Pre-Gun Mettle) for a trial period.**
- **[Server] Re-enabled Short Circuit revert (Pre-Gun Mettle), kept Phlogistinator revert (Pre-Tough Break).**
- **[Server] Disabled Darwin's Danger Shield revert (release).**
- **[Server] Enabled Sniper Rifle scope jump revert.**

### October 19, 2025
- **[Plugin] Fixed mini-crit resist for reverted Brass Beast and Natascha.**

### October 10, 2025
- **[Plugin] Added reverts for all Grenade Launchers (pre-Smissmas 2014), Iron Bomber (pre-2022) and Gunslinger (pre-Gun Mettle and release).**
- **[Plugin] Minigun ramp-up and Wrangler reverts are now available patchless.**
- **[Plugin] Refactored code for Stickybomb, Dead Ringer and Phlogistinator reverts.**
- **[Plugin] Reverted Loch-n-Load's (pre-Smissmas 2014) +/- 15% random variance on damage has been moved to the Grenade Launcher revert and only applies when random damage spread is enabled.**

### October 1, 2025
- **[Plugin/Server] Added reverts for all Flamethrowers (pre-Blue Moon) and Stickybomb Launchers (pre-Love & War).**
- **[Server] Enabled reverts for Darwin's Danger Shield (release) and Phlogistinator (pre-Tough Break) on the Castaway.tf servers for a trial period.**
- **[Server] Disabled the Short Circuit (pre-Gun Mettle) revert on the Castaway.tf servers for a trial period. The servers now use the vanilla Short Circuit.**

### September 28, 2025
- **[Plugin] Added Sniper Rifle revert (pre-2014).**
- **[Plugin] Added revert variants for Bushwacka (Pre-Gun Mettle), Rescue Ranger (Release), and Reserve Shooter (Release).**
- **[Plugin] Fixed issues with some weapons and did general technical improvements to some reverted weapons.**
  - Changed how 'full-regen' (Amputator and Concheror) reverts behave. Previously they faked the game state for Mann vs Machine, now they increase the regeneration amount for the current frame.
  - Dead Ringer revert (pre-Gun Mettle) no longer overshoots the cloak meter when gaining cloak from ammo.
  - Sandman revert (pre-WAR! Update) has proper ball damage on the first hit. Previously the damage was reduced by 25%.
  - Powerjack reverts preserve the attribute as seen in the inspect panel.
  - Cleaner's Carbine revert (release) uses the 'Crikey' meter to indicate remaining crit-boost duration.
  - Fixed reverted Phlogistinator gaining MMMPH way faster than intended.
  - Sydney Sleeper reverts:
    - Pre-Blue Moon: Now has the Jarate icon when scoped in and proper teammate extinguishing.
    - Release: Now uses proper random-crit rampup and random crits obey the server's setting.
  - Reverted Razorback now has the entity removed when backstabbed. This is basically how the old Razorback functioned.
  - Persian Persuader revert (pre-Tough Break) can no longer gain ammo from Dispensers.
  - Major code cleanup!
- **[Plugin] The option for the old (pre-Jungle Inferno) fall damage sound effects is now disabled by default.**
- **[Plugin] Updated weapon descriptions.**
- **[Plugin] Updated localization files.**

### September 19, 2025
- **[Plugin] The item key for Phlogistinator was changed from "phlogistinator" to "phlog".**

### September 13, 2025
- **[Plugin/Server] Short Circuit projectile destruction now ignores spawn room barriers. This makes clearing sticky traps with the reverted Short Circuit more effective.**
- **[Plugin/Server] Fixed a bug where Heavies spun up with the reverted Brass Beast/Natascha were invulnerable to Sentry Gun fire.**

### September 1, 2025
- **[Plugin] Some weapon reverts are now disabled by default.**
- **[Plugin] Added Phlogistinator revert variants.**
	- *Pyromania Phlogistinator (Variant 0)*
		- Video reference: https://www.youtube.com/watch?v=D5Et9qhxDvQ
		- Wiki: https://wiki.teamfortress.com/w/index.php?title=Phlogistinator&oldid=1968959
		- MMMPH meter requires 225 damage
		- Instantly restores health to max during activation
		- -10% damage penalty
		- No invulnerability on MMMPH
		- 75% damage resistance while taunting (25% against crits)
	- *Tough Break Phlogistinator (Variant 1)*
		- Video reference: https://www.youtube.com/watch?v=9cMTp4xd1R8
		- Wiki: https://wiki.teamfortress.com/w/index.php?title=Phlogistinator&oldid=2035615
		- MMMPH meter requires 225 damage
		- Instantly restores health to max during activation
		- Invulnerability lingers a bit right after taunt ends (NOTE: I eyeballed the duration for this. I estimated it to be 3.5 s of Uber. No idea what actually was the duration)
	- *Release Phlogistinator (Variant 2)*
		- Wiki: https://wiki.teamfortress.com/w/index.php?title=Phlogistinator&oldid=967378
		- MMMPH meter requires 225 damage
		- Instantly restores health to max during activation
		- No invulnerability on MMMPH
		- 90% damage resistance while taunting (30% against crits)
		- Can survive taunt kills while activating MMMPH
		- 13 seconds long MMMPH crit buff 
			- (13 seconds according to the wiki, but the changelogs say 12 seconds. I chose 13 because it accounts for the taunt duration)
	- *March 15, 2012 Phlogistinator (Variant 3)*
		- Wiki: https://wiki.teamfortress.com/w/index.php?title=Phlogistinator&oldid=1055749
		- MMMPH meter requires 225 damage
		- Instantly restores health to max during activation
		- No invulnerability on MMMPH
		- 90% damage resistance while taunting (30% against crits)
		- -10% damage penalty
		- Can survive taunt kills while activating MMMPH
- **Updated localization files**

### August 22, 2025
- **[Plugin/Server] Added Eureka Effect revert, which simply resupplies the player when teleporting to spawn.**
  - This is not historically accurate, as it simply reverts a change from the [August 27, 2015 patch](https://wiki.teamfortress.com/wiki/August_27,_2015_Patch), which also removed the resupplying upon teleporting to spawn.
    - *August 27, 2015 Patch*
    - *Fixed the Engineer losing revenge Crits and picked-up weapons after using the Eureka Effect to teleport back to base.*
    - *[Undocumented] As a result of the revenge Crits fix, the Eureka Effect no longer replenishes health and ammunition. Effects such as fire, Jarate, Mad Milk, etc. are no longer removed.*
- **[Plugin/Server] Shield bash damage with reverted Demoman shields is now historically accurate.**
  - Reverted bash damage was 50 base + 10 per head collected (up to 5 heads), for up to 100 damage. Splendid Screen increases the damage by 70%, allowing for up to 170 damage.
  - Shield bash damage for Splendid Screen was not scaled by charge depleted, dealing full bash damage at point blank.
- **[Plugin] Added Red-Tape Recorder revert (release)**
  - Red-Tape Recorder - Reverted to release, faster downgrade speed on upgraded enemy buildings (1.6 s)
- Updated localization files

### August 17, 2025
- **[Plugin] Rescue Ranger revert is now available when using the patchless version of the reverts plugin.**
- **[Plugin] Added pre-Jungle Inferno Rescue Ranger variant**
  - Rescue Ranger - Reverted to pre-inferno, no metal cost for healing buildings
- **[Plugin/Server] Fixed a bug where the healing amount displayed was negative when healing buildings with reverted Rescue Ranger**
- **[Plugin] Fixed the reverted Rescue Ranger fully healing un-reverted wrangled sentries**
- **[Plugin] Fixed the vanilla Rescue Ranger not fully healing reverted wrangled sentries**
- **[Plugin] Fixed vanilla Half-Zatoichi not having increased range when swords revert is enabled**
- **Updated localization files**

### August 16, 2025
- **[Plugin/Server] Added Amputator and Concheror reverts**
  - Amputator - Reverted to pre-toughbreak, regenerates +3 HP/s flat when active regardless if user recently took damage
  - Concheror - Reverted to pre-toughbreak, regenerates +2 HP/s flat regardless if user recently took damage

### August 13, 2025
- **Reverted Dead Ringer ("old-style", pre-GM and post-release variants) changes:**
  - No longer plays the speed boost sound or shows the "ubered" visual effect when under feigning buffs (90% damage resistance and no cloak flickering).
    - The speed boost sound might still play sometimes but shouldn't in the majority of cases.
  - Full 90% damage resistance when below 50% cloak meter and under feign buffs. Previously the vanilla feign buff was used which decreased damage resistance below 50% cloak meter.

### August 10, 2025
- **[Plugin/Server] Reverted pre-Jungle Inferno Atomizer now shows purple smoke on both double and triple jumps for historical accuracy.**
  - Purple smoke was first added to the revert when the pre-Blue Moon Atomizer variant was added, and only showed on triple jumps.
- **[Plugin] Reverted Brass Beast/Natascha no longer resist vanilla Enforcer.**
- **Updated localization files**

### August 9, 2025
- **[Plugin/Server] Reverted Shortstop changes:**
  - Moved shove removal code to DHook, should fix any issues caused by previous method
  - Alt-fire shove for reverted Shortstop is now toggleable via cvar (`sm_reverts__enable_shortstop_shove`, disabled by default) instead of revert variants
- **Reverted Chargin' Targe and Tide Turner descriptions now list that they can only deal bash damage at 60% depleted (near end-of-charge).**
- **[Plugin] Added following revert variants:**
  - Pre-Blue Moon Axtinguisher
  - Pre-Tough Break Beggar's Bazooka
  - Pre-Tough Break Cleaner's Carbine
  - Post-Release Dead Ringer
  - Pre-Jungle Inferno Gloves of Running Urgently
  - Pre-WAR! Update Sandman
  - Release Shortstop
  - Release Splendid Screen
- **Updated localization files**

### August 5, 2025
- **[Plugin] Historical Pomson 6000 variants now uses the old historical damage formula/mechanics.**

### August 1, 2025
- **Fixed a bug with the reverted Air Strike where the rocket blast radius became 0.**
- **[Plugin] Added pre-Love & War Wrangler variant**
	- *Pre-Love & War Wrangler*
		- Fully repair and refill while shield is up
		- Sentry active in 1 second on death
		- No damage falloff beyond scan range
		- Damage based on the Engineer's position, not the Sentry Gun.
- **Updated localization files**

### July 29, 2025
- **Updated reverted Short Circuit to use a destruction blacklist.**
  - Now it destroys all projectiles except syringes, Righteous Bison/Pomson 6000 energy beams, grappling hooks and spell projectiles. In a nutshell, anything that Pyro can reflect should also be destroyed by the Short Circuit.
- **Fixed a plugin startup issue when using the plugin with memory patches disabled.**
- **Reverted Special Delivery item set now allows the Unarmed Combat and Festive Holy Mackerel melee weapons.**
- **Updated Polish translation.**

### July 25, 2025
- **[Plugin] Added Rocket Jumper revert variants.**
	- *Release Rocket Jumper*
		- No self blast damage including from Equalizer/Escape Plan taunt and from pumpkin bombs
		- Wearer can pick up intel
		- Random crits (yes, I know its useless but funny)
		- Wearer emits hurt sounds when hit by own rockets
	- *December 22, 2010 Rocket Jumper*
		- 100% fire, bullet, explosive dmg vulnerabilities
		- No self inflicted blast damage taken from your own weapons and pumpkin bombs you exploded
		- Can cap intel
		- Random crits
		- Wearer emits hurt sounds when hit by own rockets
	- *October 27, 2010 Rocket Jumper*
		- -100 max hp
		- No self inflicted blast damage taken from your own weapons and pumpkin bombs you exploded
		- Can cap intel
		- Random crits
		- Wearer emits hurt sounds when hit by own rockets
- **[Plugin] Added Sticky Jumper revert variants.**
	- *Release Day 2 Sticky Jumper*
		- +200% max primary ammo on wearer
		- No self inflicted blast damage taken from your own weapons and pumpkin bombs you exploded
		- -100% damage done
		- -75 max health on wearer
		- Can capture intel
		- Random crits
		- Wearer emits hurt sounds when hit by own stickies
	- *December 22, 2010 Sticky Jumper*
		- +200% max primary ammo on wearer
		- No self inflicted blast damage taken from your own weapons and pumpkin bombs you exploded
		- -100% damage done
		- 100% fire, bullet, explosive dmg vulnerabilities
		- Can capture intel
		- Random crits
		- Wearer emits hurt sounds when hit by own stickies
- **[Plugin] Added Smissmas 2013 Short Circuit variant**
	- Reverted to Smissmas 2013, primary fire destroys projectiles (fires rapidly, costs 5 metal), can pick up metal from dispensers when active
- **Other information regarding the Jumper reverts**
	- Updated StkJumper_Pre2013_Intel item description from Pyromania Update to Manniversary Update (no increased damage vulns, 8 stickies, caps intel)
	- Historical Note: May 31, 2012 was when the no intel attribute was added for both jumper weapons.
	- Note: hurtme console command does not work whenever the Jumper weapon variants are enabled and are equipped.
- **Updated server cfgs**
- **Updated Finnish and French localizations**
- **Plugin now uses methodmap API for dhook and event [(PR #222)](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/pull/222)**

### July 24, 2025
- **[Plugin/Server] Added release Mad Milk revert**
	- *Release Mad Milk*
		- Players heal 75% of the damage done to an enemy covered with milk.
		- Can be used to extinguish fires. (does not reduce cooldown)
- **[Plugin/Server] Added reverts for Cow Mangler 5000**
	- *Release Cow Mangler 5000*
		- 5 shots in clip (Full reload time average: ~4.93 seconds)
		- Cannot be crit-boosted
		- No random critical hits
	- *Pre-Summer Event 2013 Cow Mangler 5000*
		- 5 shots in clip (Full reload time average: ~5.14 seconds)
		- Cannot be crit-boosted
		- -10% dmg penalty
		- 5% slower reload time
		- No random critical hits
- **[Plugin] Added revert variants for Sydney Sleeper**
	- *Pre-Gun Mettle Sydney Sleeper*
		- +25% charge rate
		- On Hit: Jarate applied to target for 8 seconds
		- No random critical hits
		- No headshots and no headshot bonuses
	- *Release Sydney Sleeper*
		- No charge rate increase. Same charge rate as Stock Sniper Rifle
		- On Hit: Jarate applied to target for 8 seconds, even against UberCharged enemies.
		- Random critical hits enabled*
		- No headshots and no headshot bonuses
		- Penetrates enemy players at 100% charge**
			- *The random crit mechanic is not accurate - the random crits don't follow crit ramp-up mechanics
			- **According to old Wiki pages the release Sydney Sleeper should penetrate when above 75% charge, but the Machina attribute is used for now
- **[Plugin] Added pre-Gun Mettle Natascha variant**
	- *Pre-Gun Mettle Natascha*
		- On Hit: 100% chance to slow target (no distance falloff)
		- +50% max primary ammo on wearer
		- -25% damage penalty
		- 30% slower spin up time
		- No damage resistance when spun up
- **[Plugin] Added pre-Blue Moon Atomizer variant**
	- *Pre-Blue Moon Atomizer*
		- Grants Triple Jump while deployed. (does not have to be fully deployed)
		- Melee attacks mini-crit while airborne.
		- -15% damage vs players
		- This weapon deploys 50% slower
- **Reverted Short Circuit changes:**
	- Now destroys Crusader's Crossbow bolts and Dragon's Fury fireballs.
	- Now has particle effects for destroying projectiles.
- **Reverted Pomson 6000 and Righteous Bison changes:** 
	- No longer ignores the Fists of Steel ranged damage resistance and also now deals knock-back on hit to enemies.
	- Both weapons' projectiles no longer collides with other projectiles.
- **[Server] Enabled the reverted Special Delivery item set bonus on the Castaway.tf servers for a trial period.**
- **[Server] Enabled the reverted Mad Milk on the Castaway.tf servers.**
- **[Server] Disabled the Quickiebomb Launcher revert and release Pomson 6000 revert (now using the regular variant) on the Castaway.tf servers.**
- **Updated Traditional Chinese localization file.**
- **Renamed `sm_reverts__extras` to `sm_reverts__show_moonshot` and added a toggle for it in the reverts menu.**

### July 14, 2025
- **Changed pre-Gun Mettle Short Circuit alt-fire behavior and fixed not being switched when run out of metal (however, it causes client prediction issues with alt-fire).**
- **Fixed Pre-Gun Mettle Pomson 6000 projectiles not passing through friendly buildings. Its projectiles should now pass through friendly buildings as it was historically.**
- **Updated localization files**
	- Added initial support for Japanese and Traditional Chinese. Both are unfinished, especially Japanese.
	- Corrected !toggleinfo typo in the Polish translation.

### July 13, 2025
- **Enabled the pre-Gun Mettle Short Circuit revert on the Castaway.tf servers for a trial period.**
- **Updated Polish translation.**

### July 10, 2025
- **Release Pomson 6000 variant no longer drains more than intended at mid/long range.**
- **Pre-Gun Mettle Dead Ringer now correctly compensates for Pomson drain on initial hit.**
  - This only matters when pre-Gun Mettle Dead Ringer and vanilla Pomson are used.
- **Updated Finnish and French translation.**
- **[Server] Enabled the pre-Tough Break Jag, release Pomson 6000 and pre-MyM Quickiebomb Launcher reverts on the Castaway.tf servers for a trial period.**

### July 8, 2025
- **Reverted Righteous Bison and Pomson 6000 now use proper untyped damage rather than piercing damage resistances.**
	- No longer ignores general damage resistances from e.g. Battalion's Backup and Spy's cloak.
	- Bullet and ranged resistances are still ignored.
- **Reverted Pomson 6000 now applies Cloak/ÜberCharge drain after damage is applied.**
	- Should fix any and all cases where Dead Ringer does not trigger feign upon being hit by the Pomson 6000 projectile.
- **Fixed reverted Dead Ringer not being able to tank 5 backstabs from max health.**
- **Added French translation.**
- **Updated Simplified Chinese translation.**

### July 7, 2025
- **Fixed reverted Equalizer, Loose Cannon and Ullapool Caber not applying correct damage to buildings.**
- **Fixed a bug where reverted Ambassador long-range headshots apply incorrect damage vs spun up revert Brass Beast/Natascha Heavies**
- **Updated Simplified Chinese translation.**

### July 6, 2025
- **Reverted Righteous Bison and Pomson 6000 now ignores damage resistances for historical accuracy.**
	- Both weapons used to have the "Untyped" damage type before Tough Break. Weapons with the Untyped damage type are not considered bullet/fire/explosive/melee damage.
	- An example of a vanilla weapon with Untyped damage is the Flying Guillotine on its first hit. Bleed damage is also an example of Untyped damage.
	- This means that the Bison and Pomson can now pierce through Vaccinator bullet resistance. Previously, both weapons had the Bullet damage type. Now, it should act like Untyped damage type.
		- Technically, both weapons still use "Bullet" damage types since the piercing attribute that ignores resistances is used instead. The piercing attribute mostly mimics the mechanics of Untyped damage.
- **Added Polish language support**

### July 5, 2025
- **Fixed revert Shortstop w/ no shove having issues when reloading**
	- Not totally fixed. There are some client prediction issues and weapon sounds breaking when secondary attack is held.
- **[Plugin] Added pre-Tough Break weapon switch time cvar. This gives 34% longer weapon switch to all weapons.**
	- Set sm_reverts__pre_toughbreak_switch to 1 to enable this feature.
- **Fixed the reverted Sydney Sleeper gaining headshot kills when not crit-boosted.**
- **Updated reverts cfgs.**
- **Updated item loadout descriptions and its Finnish translation.**

### July 1, 2025
- **Fixed reverted Pomson 6000 not giving correct cloak drain amounts with vanilla DR, pre-JI and pre-TB Dead Ringer variants from medium to long ranges.**
- **[Plugin] Added Pre-Jungle Inferno and Pre-Tough Break Dead Ringer variants**
    - **Dead Ringer (Pre-Jungle Inferno)**
    - https://wiki.teamfortress.com/w/index.php?title=Dead_Ringer&oldid=2026559
		- Same stats as modern Dead Ringer
		- Has 3 second speedboost on Feign
		- Can regenerate cloak with ammo packs only if uncloaked
		- 35% less cloak from ammo packs
	- **Dead Ringer (Pre-Tough Break)**
    - https://wiki.teamfortress.com/w/index.php?title=Dead_Ringer&oldid=1948244
		- Same stats as modern Dead Ringer
		- Has 3 second speedboost on Feign
        - Can regenerate cloak with ammo packs only if uncloaked
        - 35% less cloak from ammo packs
        - 50% initial damage resistance on feign (instead of 75%)


### June 28, 2025
- **Reverted Righteous Bison and Pomson 6000 variants now lights up the Huntsman arrows of friendly Snipers.**
- **[Plugin] Added Saharan Spy variant that removes the +40% cloak from L'Etranger if the set is equipped (L'Etranger & YER)**
	- Set bonus and +40% cloak removal from L'Etranger does not activate if the Spy uses L'Etranger and Wanga Prick.
- **Updated pre-Gun Mettle server config file.**

### June 27, 2025
- **[Plugin] Added release Backburner weapon revert variant**
    - **Release Backburner**
        - +50 max hp on wearer (225 hp, max overheal of 335 hp)
        - No airblast
- **[Plugin] Added two (2) Fists of Steel revert variants**
	- **Fists of Steel (Pre-Tough Break)**
		- https://wiki.teamfortress.com/w/index.php?title=Fists_of_Steel&oldid=1931106
		- -40% damage from ranged sources while active
		- 20% longer weapon switch
		- +100% damage from melee sources while active
		- No healing and holster penalties
	- **Fists of Steel (Release/Pre-Hatless Update)**
		- https://wiki.teamfortress.com/w/index.php?title=Fists_of_Steel&oldid=457190
		- -60% damage from ranged sources while active
		- +100% damage from melee sources while active
		- No healing and holster penalties
- **[Plugin] Added more historically accurate Pomson 6000 revert variant**
	- **Pomson 6000 (Pre-Gun Mettle, more historically accurate)**
		- Increased hitbox size (same as Bison)
		- ***Projectile does not pass through teammates***
		- No uber & cloak drain fall-off at any range
		- *Note: damage type isn't yet untyped damage.*

### June 26, 2025
- **Fixed another bug where reverted Dead Ringer would lose 70% cloak on hit by the Pomson at close ranges**
- **Added preset weapon revert configs for use by server owners, as well as starting templates for their use**

### June 25, 2025
- **[Plugin] Added pre-Tough Break and pre-Gun Mettle Jag reverts**
- **[Plugin] Added more revert variants for Crit-a-Cola**
- **Fixed reverted Dead Ringer cloak drain bug on feign with Pomson 6000 whenever the Spy is far away from the Engineer**

### June 24, 2025
- **Updated Chinese (Simplified) language support to be more full**
- **Optimized Dragon's Fury memory patch. Gamedata folder must be updated to ensure the plugin works correctly.**
- **[Plugin] Restored the following item set bonuses:**
    - Scout (Special Delivery)
    - Pyro (Gas Jockey's Gear)
    - Demoman (Expert's Ordnance)
    - Heavy (Hibernating Bear)
    - Sniper (Croc-o-Style Kit)

### June 23, 2025
- **Added Finnish language support**

### June 22, 2025
- **Added multilingual support for the weapon reverts plugin.**
- **Added initial Simplified Chinese support**
- **[Plugin] Added pre-Gun Mettle Shortstop variant**
  - *Shortstop (Pre-Gun Mettle)*
    - +20% bonus healing from health packs while active
    - 40% Increase in push force taken from damage and airblast at all times
    - Shares reserve ammo with pistol
    - 50% slower reload speed (same as modern version)
    - Shove can be toggled via cvar
- **[Plugin] Added release Buffalo Steak Sandvich variants**
  - *Buffalo Steak Sandvich (Release)*
    - When under effects:
      - Move speed increased to 310.5 HU/s
      - No damage vulnerability modifier
      - Instead, damage taken are mini-crits to the user (+35% damage vulnerability)
      - When combined with the GRU, move speed stacks and increases to 403.50 HU/s (run as fast as the Scout, just a tiny bit faster)
         - Speed should exactly be 403.65 HU/s historically, but due to rounding, it gets rounded down to 403.50 HU/s (according to cl_showpos 1)
  - Buffalo Steak Sandvich (Pre-Summer 2013)
    - Same stats as the release Steak, but without the speed stacking effect with the GRU

### June 17, 2025
- **[Plugin] Added the following revert variants (can be toggled via server cvar):**
  - *Tomislav (Release)*
    - +75% faster spin-up time, no accuracy bonus
  - *Enforcer (Release)*
    - No firing speed penalty
    - +20% damage bonus regardless if disguised or not
    - Random crits enabled
    - +0.5 s increased time to fully cloak penalty
    - No piercing
  - *Eviction Notice (Gun Mettle)*
    - +50% faster firing speed
    - Gain a speed boost on hit
    - -60% damage penalty
    - No increased move speed bonus
    - No damage vulnerability penalty
  - *Pomson 6000 (Release)*
    - Projectile goes through enemies
    - Projectile can hit enemies multiple times
    - Acts like Righteous Bison projectile
    - Note: does not ignore Vaccinator resistances yet (need to find out how to turn into Untyped damage)
  - *Gloves of Running Urgently (Release)*
    - No health drain penalty
    - No mark-for-death
    - 50% dmg penalty
    - -6hp/s while active, can jump a bit higher for every -6 hp lost per second
  - *Powerjack (Release)*
      - No faster move speed while active
      - Kills restore 75 health with overheal
      - +25% damage bonus
      - No random crits
  - *Powerjack (Hatless Update)*
      - No faster move speed while active
      - Kills restore 75 health with overheal
      - 25% melee vuln while active
  - *Equalizer (Release and Pre-Hatless Update)*
     - **For reference, this is the pre-Pyromania Equalizer currently used in the server** 
        - 107 dmg at 1 hp
           - https://wiki.teamfortress.com/w/index.php?title=Equalizer&oldid=1048826
     - **Pre-Hatless Update Equalizer (pre-April 14, 2010)** 
        - 113 dmg at 1 hp (does not one shot light classes since RDS is turned off by default)
           - IF -+15% RANDOM DAMAGE SPREAD IS TURNED ON: 
              - MAX 129 DMG (one-shots 125HP classes)
              - MIN 96 DMG
           - https://wiki.teamfortress.com/w/index.php?title=Equalizer&oldid=456483
     - **Release Equalizer (damage numbers shown assume 200 max HP)**
        - 125 dmg at 58 hp (one-shots unbuffed Scout, Spy, stock Engineer, and Sniper)
        - 150 dmg at 20 hp (one-shots unbuffed Medics)
        - 162 dmg at 1 hp (two-shots unbuffed Heavies)
           - This and the pre-Hatless Update versions of the Equalizer (and with random damage spread on by default back then) are what got stuck inside the collective consciousness of the TF2 community, and it didn't help _that certain popular figures who never experienced them and did not do enough research_ just regurgitated the old memories of these versions of the Equalizer. Remember to not trust anyone, and always do your own research.
           - https://web.archive.org/web/20100328111803/http://www.tf2wiki.net:80/wiki/Equalizer
  - *Baby Face's Blaster (Release)*
    - 40% more accurate
    - On Hit: Builds Boost
    - Run at up to double speed at maximum Boost
    - -30% damage penalty
    - 35% slower move speed on wearer
    - Boost resets on jump
- **Added the following reverts (disabled on Castaway as of the time of this writing):**
  - *Gunboats (Release)*
    - -75% blast self-damage
  - *Quickiebomb Launcher (Tough Break)*
    - -0.2 sec faster bomb arm time
    - Max charge time decreased by 50%
    - Up to +25% damage based on charge
    - Able to destroy enemy stickybombs
    - -25% clip size
    - -15% damage penalty
    - Stickybombs fizzle 4 seconds after landing

### June 14, 2025
- **Fixed reverted shields to have the historically correct shield bash sounds**

### June 9, 2025
- **[Server] Enabled the revert for pre-Pyromania Equalizer and Escape Plan, which merges the two back to one weapon.**
  - *The Equalizer and Escape Plan*
    - Damage and move speed increase as the user becomes injured
    - No mark-for-death when active
    - Blocks healing (from Medics) when in use
- **[Server] Re-enabled the alt-fire shove on the Shortstop due to issues with reloading the weapon.**

### June 8, 2025
- **[Plugin/Server] Added revert variant for pre-Gun Mettle Short Circuit**
 - *The Short Circuit (Pre-Gun Mettle)*
   - *Primary fire destroys projectiles, costs 5 metal per shot, 15 metal per projectile destroyed*
   - *No metal from dispensers when active, no alt-fire*

### June 7, 2025
- **[Server] Removed the alt-fire shove from the Shortstop, which makes it fully historically accurate to the pre-Manniversary version.**
- **[Plugin] Added revert variants for the following:**
  - *Axtinguisher (pre-Tough Break)*
  - *Backburner (119th Update)*
  - *Darwin's Danger Shield (release/pre-2013)*
  - *Loch-n-Load (pre-Smissmas 2014)*
  - *Pretty Boy's Pocket Pistol (pre-Blue Moon)*
  - *Reserve Shooter (pre-Jungle Inferno)*


### June 6,  2025
- **Added support for revert variants.**
- **[Plugin] Added a Soda Popper variant (pre-MyM)**
  - *The Soda Popper (pre-MyM)*
    - +50% faster firing speed
    - 25% faster reload time
    - -66% clip size
    - Builds Hype as you run.
    - When full, Alt-Fire to activate Hype mode for
    - multiple air jumps.
    - This weapon reloads its entire clip at once

### June 3, 2025
- **[Plugin/Server] Reverted the Gloves of Running Urgently to pre-Tough Break**
  - *The Gloves of Running Urgently*
    - When weapon is active:
    - +30% faster move speed on wearer
    - -25% damage penalty
    - You are marked for death while active, and for short period after switching weapons
  - **The previously used revert was pre-Jungle Inferno which had a 50% increase in the time to holster the weapon.**
- **Wrangler shield now fades after 1 second if the Engineer dies with the Wrangler deployed.**

### June 2, 2025
- **[Plugin/Server] Reverted the Reserve Shooter to pre-Tough Break**
  - *The Reserve Shooter*
    - Mini-crits all airborne targets for 5 seconds after being deployed
    - 15% faster weapon switch
    - -34% clip size
  - **The previously used revert was pre-Jungle Inferno which mini-crit on players launched into the air (including from airblast) and not simply being in the air from e.g. jumping.**

### May 31, 2025
- **[Server] Disabled the Darwin's Danger Shield and Tomislav reverts. The server now uses the modern versions of these items.**

### May 28, 2025
- **[Plugin/Server] Short Circuit revert is now more accurate to the pre-MyM version, with alt-fire costing 15 metal at a 0.5 second interval and dealing 20 damage to players. Previous version cost 10 metal at a 0.25 second interval and dealt 10 damage to players.**

### May 25, 2025
- **Fixed reverted Persian Persuader not removing afterburn and bleed when picking up ammo packs as health, and increased pickup volume for dropped ammo packs.**
- **[Plugin/Server] Reverted the Buffalo Steak Sandvich to pre-Meet your Match**
  - *The Buffalo Steak Sandvich*
    - +10% damage vulnerability while active
    - +35% faster move speed while active
    - Effect lasts 16 seconds.

### May 24, 2025
- **[Server] Six (6) weapons have been reverted in this update.**
- **Fixed Spy-cicle picking up ammo packs when melted while the Spy's cloak and primary ammo are full.**
- **Reverted the Dalokohs Bar to be able to overheal up to 400 HP again (Gun Mettle Update).**
  - **Note: if the GRU is not reverted, the Dalokohs Bar and GRU overheal exploit may occur**
  - *The Dalokohs Bar*
    - Adds +50 max health for 30 seconds
    - Eat to gain up to 100 health.
    - Can gain overheal up to 400 health when eaten.

- **[Plugin/Server] Reverted the Shortstop to its most historically accurate version while keeping the modern shove mechanic (pre-Manniversary Update).**
  - *The Shortstop*
    - No push force increase penalty taken from damage and airblast
    - No reload speed penalty
    - Shares secondary pistol ammo reserve
      - Has a 36 max ammo reserve that is shared with any of the Scout's secondary pistols
      
- **[Plugin/Server] Reverted the Persian Persuader to pre-Tough Break.**
  - *The Persian Persuader*
    - +100% increase in charge recharge rate
    - All ammo collected becomes health
      - HP gained from each ammo pack size:
        - Large = +40, Medium = +20, Small = +10
    - No random critical hits
    - This weapon has a large melee range
      
- **[Plugin/Server] Reverted the Tomislav to pre-Pyromania**
  - *The Tomislav*
    - 40% faster spin up time
    - No accuracy bonus
    - Silent Killer: No barrel spin sound
    - 20% slower firing speed
      
- **[Plugin/Server] Reverted the Darwin's Danger Shield to pre-Jungle Inferno**
  - *The Darwin's Danger Shield*
    - +25 max health on wearer
    - +15% bullet damage resistance on wearer
    - 20% explosive damage vulnerability on wearer
    - No afterburn immunity
      
- **[Plugin/Server] Reverted the Bushwacka to release**
  - *The Bushwacka*
    - Crits whenever it would normally mini-crit
    - 20% fire damage vulnerability on wearer (instead of overall vulnerability)
    - Has random crits enabled

### May 20, 2025
- **Fixed reverted Sydney Sleeper showing the headshot kill icon and giving a headshot point when shooting enemies in the head (when not crit-boosted).**
  - Historically, the reverted Sydney Sleeper did not have the ability to score headshots.
- **Fixed reverted Enforcer not dealing bonus damage when undisguised to buildings.**
- **[Plugin/Server] Added a cvar for reverting the fall damage hurt sound to pre-Jungle Inferno (cvar_old_falldmg_sfx).**
  - By default, this cvar revert is enabled.

### May 18, 2025
- **Fixed reverted B.A.S.E. Jumper fire updraft bonus not working**

### May 15, 2025
- **[Plugin/Server] Reverted the shield charge mechanics and stats for the Splendid Screen to pre-Tough Break.**
  - Right after impacting an enemy with a shield charge, the Demoman is able to do a critical melee hit from any distance, even at close range.
    - See this video for a clearer example (start at 3:55): https://youtu.be/DByy2z7VLzI?si=DZAkfYb3b24rkBAv&t=235
  - The reverted Splendid Screen can still do shield bash damage at any distance, but it does not have the +50% charge recharge rate bonus anymore and only has +15% explosive damage resistance on wearer compared to the current vanilla version.
  - Charging with The Splendid Screen does not remove debuffs anymore (Afterburn, Jarate, Mad Milk, Bleed & Gas) from the wearer.
    - *The Splendid Screen*
    - *+20% fire damage resistance on wearer*
    - *+15% explosive damage resistance on wearer*
    - *+70% increase in charge impact damage*
    - *Alt-Fire: Charge toward your enemies.*
    - *Gain a critical melee strike after impacting an enemy.*
    - *Shield bashes cause damage to the enemy.*
- **[Plugin] Added a cvar for reverting the Rocket Jumper and Sticky Jumper to be able to capture enemy flags again (cvar_jumper_flag_run).**
  - By default, this cvar revert is disabled.
- **Updated ItemDefine descriptions for the Pomson 6000 and the Panic Attack.**

### May 11, 2025
- **[Plugin/Server] Reverted the shield charge mechanics for the Chargin' Targe and the Tide Turner.**
  - Right after impacting an enemy with a shield charge, the Demoman is able to do a critical melee hit from any distance, even at close range.
    - See this video for a clearer example (start at 3:55): https://youtu.be/DByy2z7VLzI?si=DZAkfYb3b24rkBAv&t=235
  - However, both the Chargin' Targe and the Tide Turner are not able to deal shield bash damage at any distance and must be at the end of the charge to deal shield bash damage.
  - Charging with The Chargin' Targe and the Tide Turner does not remove debuffs anymore (Afterburn, Jarate, Mad Milk, Bleed & Gas) from the wearer.
    - *The Chargin' Targe and The Tide Turner*
    - *Alt-Fire: Charge toward your enemies.*
    - *Gain a critical melee strike after impacting an enemy.*

### May 9, 2025
- **Fixed the Big Earner's 3-second speedboost being extended by the reverted Dead Ringer on feign death.**
- **Fixed the duration reduction of Spies under Dead Ringer when being damaged by weapons such as the Ullapool Caber and the Enforcer.**
- **Made the damage resistance attribute of the reverted Brass Beast (and the Natascha) to be more historically accurate.**
  - The damage resistance percentage now depends on what type of damage is dealt onto the Heavy. For normal damage, 20% damage resistance is applied. For mini-crit damage received, 14.7% damage resistance is applied. For critical hit damage received, 6.7% damage resistance is applied.
- **Damage resistance sounds now play when the Heavy is hit while spinning up the reverted Brass Beast and the reverted Natascha.**
- **[Plugin/Server] Reverted Natascha to pre-Meet your Match. The 20% damage resistance when spun up now applies regardless of current HP.**
  - *The Natascha*
    - On Hit: 100% chance to slow target
    - 20% damage resistance when spun up
    - -25% damage penalty
    - 30% slower spin up time

### May 1, 2025
- **Updated reverts.txt offsets in the gamedata folder, fixing the Soldier's rocket kills showing up as headshots, the reverted Short Circuit's alt-fire using the modern energy ball, and the Thermal Thruster playing a parachute sound on use.**
  - For context, TF2 had a recent patch which affected the weapon reverts plug-in.
- **Updated the reverted Crit-a-Cola's damage vulnerability attribute to be more historically accurate.**
  - The 10% damage vulnerability should only apply to normal damage. Mini-crit and critical hit damage does not get modified by the 10% damage vulnerability attribute. This means Scouts don't die faster to mini-crits and critical hits now.
- **Fixed the reverted Black Box's heal-on-hit attribute to work again.**

### April 28, 2025
- **Added Windows port for the weapon reverts plugin. The plugin should now work out of the box for Windows servers.**
- **[Plugin/Server] Reverted the Quick-Fix to have 25% increased Uber build rate, and to be able to capture objectives while under the effects of its Uber for both the healer and patient.**

### April 26, 2025
- **[Plugin/Server] The reverted Tide Turner's blast and fire damage resistances have been updated to 25% each to be more historically accurate (pre-Tough Break).**
  - *The Tide Turner*
     - +25% fire damage resistance on wearer
     - +25% explosive damage resistance on wearer
     - Full turning control while charging
     - Melee kills refill 75% of your charge meter
     - Taking damage while shield charging reduces remaining charging time
- **[Plugin/Server] The reverted Soda Popper's visuals have been updated to be more historically accurate to its release version. When the Hype meter is full, the glow now shows up as a Mini-Crits glow instead of a purple glow.**
  - The purple glow will only appear if the Scout equips the Crit-a-Cola or the Bonk! Atomic Punch due to how the game technically handles Mini-Crit conditions.

### April 23, 2025
- **Crit-a-Cola no longer marks the user for death for a few frames anymore.**

### April 21, 2025
- **[Plugin/Server] The Dead Ringer is now reverted to its most accurate state before Gun Mettle. 90% damage resistance for up to 6.5 seconds that gets reduced by damage received. This Dead Ringer is now able to tank 5 backstabs and 8 stickybombs from 125 HP, and 14 stickybombs when using the Kunai at 200 HP. The previous version of the revert would only tank 1 backstab and up to 4 to 5 stickybombs.**
- **Fixed reverted Powerjack bug where the Pyro gets healed when an enemy dies to afterburn while the Powerjack is the active weapon. It should only heal due to melee kills by the Powerjack.**

### April 17, 2025
- **Fixed reverted Black Box overheal bug where hitting an enemy removes the Soldier's overheal.**
- **[Plugin/Server] Ball recharge time for the reverted Sandman is now 15 seconds long for historical accuracy (pre-Jungle Inferno).**
- **[Plugin/Server] Claidheamh Mor +0.5s charge time increase now applies passively.**
- **[Plugin/Server] Reverted Powerjack to pre-Gun Mettle version, same stats as the modern one but with +75 HP on kill with overheal.**
	- *The Powerjack*
	  - When weapon is active:
	  - +15% faster move speed on wearer
	  - +75 health restored on kill
	  - Health restoration can overheal
	  - 20% damage vulnerability on wearer

### April 5, 2025
- **[Plugin/Server] Reverted Black Box to pre-gunmettle, flat +15 per hit, uncapped**
  - *The Black Box*
    - On Hit: +15 health
    - -25% clip size
- **Fixed cases where stuns from e.g. Sandman ended instantly**

### April 4, 2025
- **[Server] Disabled Scottish Resistance revert. The server now uses the modern Scottish Resistance version.**
- **[Plugin/Server] Reverted the following weapons:**
  - Wrangler to pre-Gun Mettle (shield values only)
  - Rescue Ranger to pre-Gun Mettle
  - Disciplinary Action to pre-Meet your Match
  - Razorback to pre-Jungle Inferno
  - Warrior's Spirit to pre-Tough Break
  - Cozy Camper to pre-Meet your Match
  - Dragons Fury (to its more accurate release version)
  - Ramp up for all Heavy Miniguns (pre-Love and War)
  - Deploy and holster speeds for all Demoman swords (pre-Tough Break)

### March 26, 2025
- **[Plugin/Server] Reverted Rocket Jumper self-explosion damage immunity.**
- **Taunting with the Equalizer or Escape Plan while using the Rocket Jumper:**
  - No longer kills the Soldier
  - Leaves Soldier’s health intact and knocks them upward

### March 19, 2025
- **[Plugin/Server] Reverted Brass Beast to the pre-Meet your Match version.**
  - *The Brass Beast*
    - +20% damage bonus
    - 20% damage resistance when spun up
    - 50% slower spin up time
    - -60% slower move speed while deployed

### March 9, 2025
- **[Plugin/Server] Restored Saharan Spy Item Set Bonus (does not require Familiar Fez)**
  - *The Saharan Spy*
    - L'Etranger
    - Your Eternal Reward
  - **Item Set Bonus:**
    - Reduced decloak sound volume
    - 0.5 sec longer Cloak blink time

### February 24, 2025
- **[Plugin/Server] Changed Backburner to Hatless Update version**
  - *The Backburner*
    - 100% critical hits from behind
    - Extinguishing teammates restores 20 health
    - 10% increased damage
    - +150% airblast cost
- **[Plugin/Server] Reverted Cleaner's Carbine to release version**
  - *The Cleaner's Carbine*
    - On Kill: 3 seconds of 100% critical chance
    - -20% clip size
    - 35% slower firing speed
    - No random critical hits

### February 20, 2025
- **Fixed the Crit-a-Cola marking the user for death when attacking with an all-class melee (weapon class "saxxy")**

### February 12, 2025
- **[Plugin/Server] Reverted Backburner to 119th Update version**
  - *The Backburner*
    - 100% critical hits from behind
    - Extinguishing teammates restores 20 health
    - 20% increased damage
    - No airblast

### February 2, 2025
- **[Plugin/Server] Reverted Claidheamh Mòr to pre-Tough Break**
  - *The Claidheamh Mòr*
    - 0.5 sec increase in charge duration
    - Melee kills refill 25% of your charge meter
    - No random critical hits
    - -15 max health on wearer
    - This weapon has a large melee range and deploys and holsters slower
  - *Note: deploy and holster speeds weren't changed in this patch.*
- **Fixed extra damage taken with the Eviction Notice when equipped but not deployed**

### January 20, 2025
- **[Plugin/Server] Reverted Tribalman's Shiv to release version**
  - *The Tribalman's Shiv*
    - On Hit: Bleed for 8 seconds
    - -35% damage penalty

### January 11, 2025
- **[Server] Disabled airblast revert — using current vanilla airblast version**

### January 10, 2025
- **Fixed some cases where the Crit-a-Cola marked the user for death on attack**
- **Fixed reflected Sandman balls not stunning**
- **Fixed Spy-cicle fireproof duration incorrectly being 3 seconds (changed to 2 seconds)**

### December 29, 2024
- **[Plugin/Server] Reverted Pretty Boy's Pocket Pistol to release**
  - *Pretty Boy's Pocket Pistol*
    - +15 max health on wearer
    - Wearer never takes falling damage
    - 25% slower firing speed
    - 50% fire damage vulnerability on wearer

### December 28, 2024
- **[Server] Reverted Loch-n-Load back to post-Smissmas 2014 / pre-Gun Mettle Update**
  - *The Loch-n-Load*
    - +20% damage bonus
    - +25% projectile speed
    - -25% clip size (3 pipes in clip)
    - -25% explosion radius
    - Launched bombs shatter on surfaces

### December 26, 2024
- **[Server] Reverted Scottish Resistance to release**
  - *The Scottish Resistance*
    - +50% max secondary ammo on wearer
    - +6 max pipebombs out
    - Detonates stickybombs near crosshair
    - Able to destroy enemy stickybombs
    - 0.4 sec slower bomb arm time
- **[Plugin/Server] Reverted Loch-n-Load to pre-Smissmas 2014**
  - *The Loch-n-Load*
    - +20% damage bonus
    - +25% projectile speed
    - -50% clip size (2 pipes in clip)
    - +25% damage to self
    - Launched bombs shatter on surfaces
  - **Note: when this was implemented, the grenade tumbling attribute was not included, so this reverted version was historically inaccurate.**
    - Historically, the grenade tumbling attribute in the pre-Smissmas 2014 Loch-n-Load was not only a visual difference, but also slowed down the old Loch-n-Load's projectile speed.
      - See video for a demonstration of the grenade tumbling attribute affecting projectile speed: https://youtu.be/ACfafLuLmy8?t=143
      - This is caused by the Source physics engine including air resistance with projectiles.
   
### December 12, 2024
- **All Castaway.tf servers now use Bakugo's Weapon Reverts plugin.**

### November 14, 2024
- **[Plugin/Server] Crit-a-Cola has been reverted to pre-Meet your Match around this time.**
  - *The Crit-a-Cola*
    - While under the effects, +25% movement speed, your attacks mini-crit, and damage taken increased by 10%.
- **[Plugin/Server] Panic Attack has been reverted to pre-Jungle Inferno around this time.**
  - *The Panic Attack*
    - 50% faster reload time
    - This weapon deploys 50% faster
    - Fire rate increases as health decreases
    - Hold fire to load up to 4 shells
    - Weapon spread increases as health decreases

### November 11, 2024
- **Changed the plugin used for the Weapon Reverts servers (Bakugo's Weapon Reverts instead of NotnHeavy's Pre-Gun Mettle Reverts). Instead of a blanket gun-mettle revert, it selectively reverts weapons. It also doesn't cause lag.**

### October 10, 2024
- **Some Castaway.tf servers now uses the blanket Pre-Gun Mettle reverts plugin made by NotnHeavy.**

## See also
[Back to top](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Changelog#contents)

- [Castaway Server CVars](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Castaway-Server-CVars)
- [Weapon Reverts List & Other Cvars](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Revert-List)
- [Server Config Presets](https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins/wiki/Weapon-Reverts-Config-Presets)
- _[Castaway.tf Weapon Reverts Thread (External link)](https://steamcommunity.com/groups/castawaytf/discussions/0/591756872987516258/)_

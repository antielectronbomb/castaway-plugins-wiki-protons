List of Potential Weapons to Revert:
- Pre-Gun Mettle Vaccinator (import from NotnHeavy's, but difficult)
- Pre-Jungle Inferno Flamethrower Mechanics (NotnHeavy's plugin needs to be fixed)
- Bazaar Bargain Revert (import from NotnHeavy's) (is it even worth it??)
- (OK) Sandvich/Lunchbox plate drops being able to be picked up by the owner as health
- FaN revert (3 shots?? wtf are you sure about this)
- (OK) Crossbow Revert (revert most recent nerf) where it gave you more uber when you healed someone
	- https://wiki.teamfortress.com/w/index.php?title=Crusader%27s_Crossbow&oldid=2261465
	- huutti says to mempatch this: https://github.com/ValveSoftware/source-sdk-2013/blob/master/src/game/server/tf/tf_projectile_arrow.cpp#L1275
	- todo: find out if theres a way to do this without a mempatch
- (OK) Release Blutsauger (no one uses this but okay)
- (OK) Release Ambassador (May 21, 2009 to May 25, 2009)
	- Mini-crits on Headshots
	- No cooldowns
	- Penetrates enemy players
- (OK) May 26, 2009 Ambassador (May 26, 2009 to June 23, 2009)
	- Crits on headshots
	- No cooldowns
	- Penetrates enemy players
		this damn line is making things hard: https://github.com/ValveSoftware/source-sdk-2013/blob/68c8b82fdcb41b8ad5abde9fe1f0654254217b8e/src/game/shared/tf/tf_weapon_revolver.cpp#L107
		OK first shots become normal dmg beyond 1200 hammer units ffs
		also consecutive rapid fire headshots don't count towards the headshots point for some reason
- (OK, didn't need to use flame particle hitbox)ACTUALLY reverting Pomson and Bison to use flame particle hitbox
- (OK) Pre-Gun Mettle Dalokohs Bar (can be eaten infinitely, no overheal, cannot be thrown)
	- or was is the release version?
- (OK) Release and pre-2010 Dead Ringer
- (done by huutti) Release/Pre-Classless Update Sandman
- Release Detonator(?) (can be imported from NotnHeavy but not sure if worth it)
- Pre-2008 Grenade Launcher
- Pre-2008 Rocket Launcher
- 2007 Medigun(?)
- Pocket Pistol variants(?)
- (OK) 2007 Sniper Rifle quickscope revert (likely mempatch)
- 2007 Stickybombs rampup(?)
- (OK) Release Buff Banner (1000 dmg needed for 14 sec buff)(?)
- (OK) Release Direct Hit
- (OK) Release/Pre-Smissmas 2014 Tide Turner
- (OK) Release Gunboats survives kamikaze taunt (see https://wiki.teamfortress.com/w/index.php?title=Grenade_(taunt)&oldid=91783)
	- Video reference (64 self damage): https://www.youtube.com/watch?v=AFKThrW_VK4
- (OK) Pre-Mann-Conomy Update Equalizer grenade taunt survivable when overhealed (self damage is 256; see https://wiki.teamfortress.com/w/index.php?title=Grenade_(taunt)&oldid=91783)
- (OK) Pre-2008 Sniper Rifle 200ms Quickscope Revert

Class Mechanics Reverts:
- Pre-Gun Mettle Engineer Mechanics
- Old Medic self-regeneration mechanics

Miscellaneous:
- (OK) Fencing while cloaked bug revert https://www.youtube.com/watch?v=L_aFprOzvUA
- Spycicle fencing taunt
- (OK) Huntsman Skewer taunt loop with another Huntsman sniper
- Taunt camera being slow when taunt ends from third to first person (REQUIRES CLIENT CHANGE, MAKE A PR IN OFFICIAL SOURCE SDK)
	- See example: https://youtu.be/Jrf5DAwTUcg
- Bombonomicon instant explosion on death revert (currently has a delay)
	- See example: https://youtu.be/JKmiRRvT7lY
	- Another example: https://youtu.be/DM07WDWlSoI
- Tomislav client-side firing sound revert (REQUIRES CLIENT CHANGE, MAKE A PR IN OFFICIAL SOURCE SDK)
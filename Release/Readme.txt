DESCRIPTION
These are the files needed in TF2 for configuration for "fortress assault."
They are mostly just config files to streamline the paricipation process for clients,
for conveniance sake however, server cfg files are included as well (they won't overide any existing configs by default)
Additionally, the "Fortress Assault" folder contains other documentation that you may be interested in

INSTALATION:
TLDR: extract or copy the "tf" folder from this archives "Team Fortress 2" folder into your Team Fortress 2 files
1) Using any zip file extractor, extract the files into an empty folder
2) Copy the "tf" folder (inside of the Team Fortress 2 Folder)
3) Locate TF2 in your Steam Library. From the list; "right click/manage/browse local files"
4) Paste the "tf" folder in the folder that pops up
NOTE: If you already have METAMOD installed for TF2, you'll want to skip any file overwrites or delete the ADDON folder being copied before continueing
5) Locate your My Games (usually in Documents) [NOT the installation folder through steam]
6) Paste the "Tabletop Simulator" folder into the "My Games" folder

	HOST:
	You'll want to copy the files inside tf/cfg/sv into the tf/cfg. NOTE: This will override any server
	settings you may have set up! If you have settings you want to keep either paste the lines in
	this server.cfg file at the bottom of yours and disable them (using //) when not in use or keep separate files

	PLAYER:
	To be prepared, its recommended you download the map files in advance. Use the console (~ key 
	by default) and enter in the commands in '' apostrophes below. Visiting the worksop maps below
	will automatically download them into your gamefiles

		WORKSHOP MAPS
		koth_bagel, goto by entering 'exec fa/map_koth_bagel' or located on steam at workshop/2056802978
		koth_2fort,goto by entering 'exec fa/map_koth_2fort located on steam at workshop/2134517733 or 
		koth_trenchfoot, goto by entering 'exec fa/map_koth_trenchfoot' or located on steam at workshop/731436616 or 
		
		NON-WORKSHOP MAPS [NOTE: No download neccesary, these are inlcuded in this archive]
		koth_basalt, goto by entering 'map koth_basalt_rc2' or located at https://tf2maps.net/downloads/basalt.606/download?version=613		
		arena_hardhat, goto by entering 'map arena_hardhat_b2a' or located at https://tf2maps.net/downloads/hardhat.691/download?version=714
		cp_furnacepoint, goto by entering 'map workshop/454147907' or located at workshop/454147907

USAGE:
	CLIENT:
	1) Open up the console and enter 'exec fa'
	2) That's it, that's all you need to do

	HOST:
	You'll want to study up on Servers. TF2 wiki provides a decent overview as to their operation:
	https://wiki.teamfortress.com/wiki/Servers
	I have noticed some instability with listen servers, so if its possible I'd reccomend a
	dedicated server

	1) FIRST TIME ONLY: Navigate to your cfg folder (Team Fortress 2/tf/cfg), and open up the "server.cfg" file and 
	configure your password as desired for the server, you will need to share this with other
	players in order for them to join, so you may want to jot it down
		NOTE: to see the servers current password after it's launched use sv_password in the console
	2) Open up fa_start.cfg, and replace the teams here with their appropriote number (SEE setting up bot teams below)
	Additionally, if the map has no timelimit by default you can re-enable mp_timelimit & end_at_timelimit 
	to force onein. Note that it may not be reflected in the HUD
	3) Open up bots/classlimits.cfg and update as neccesary if players have unlocked any support
	4) Open up bots/blu_defend_stand.cfg and input blue teams desired bot configuration
	5) Startup your server on the desired map (using either the 'map' command or the ui)
	6) NO ACTION NEEDED: On map load the server should start in tournament mode
		NOTE: There is some buginess with bots and tournament mode, if you get issues with 
		them staying in spawn, go into fa_setup.cfg, and use // to disable the mp_tournament
		setting. Then restart the process
	7) Once all players have joined, open up your console and type 'exec fa_start' to add the bots and start the round
	8) On map end you may have to forcably change the map (This is a bug with Tournament mode, there is no workaround)
	use 'Changelevel' command to move to a different map. Alternatively, just use
	NOTE: By default, you will return to tr_walkway if the changelevel does work, this can be changed by editing mapcyclye_fa.txt
	
	TO SET UP BOTS
	1) Study up on bot commands: https://wiki.teamfortress.com/wiki/Bots
	2) Use the standard files to create new squads. It's recomended you copy the standard configs
	and rename as you desire to keep the defaults in
	3) Update fa_start.cfg with the 2 squads to be used in the upcoming battle and any additional settings you want to tweak for the match

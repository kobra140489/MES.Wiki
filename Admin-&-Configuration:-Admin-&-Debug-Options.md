These commands can be used to force spawn random or specific spawn groups, enable debug mode, get data on loaded spawngroups / active players / active NPCs / etc, and much more. These are chat commands only, so there are no accompanying XML configs.

Here is a list of command categories:

[**BehaviorDebug**](#BehaviorDebug)  
[**Debug**](#Debug)  
[**Info**](#Info)  
[**Spawn**](#Spawn)  
[**SpawnDebug**](#SpawnDebug)  

# BehaviorDebug

|Setting:|Enable or Disable Logging|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.BehaviorDebug.Value1.Value2`|
|Description:|This chat command allows you to enable various forms of logging for Behavior Related events. This can help you troubleshoot issues.|
|Allowed Value1:|`Action`<br />`AutoPilot`<br />`BehaviorMode`<br />`BehaviorSetup`<br />`BehaviorSpecific`<br />`Chat`<br />`Command`<br />`Condition`<br />`Collision`<br />`Dev`<br />`Error`<br />`GameLog` (enable this to write enabled events to game log)<br />`General`<br />`Owner`<br />`Settings`<br />`Spawn`<br />`Startup`<br />`TargetAcquisition`<br />`TargetEvaluation`<br />`Thrust`<br />`Trigger`<br />`Weapon`<br />`Target`|
|Allowed Value2:|`true`<br />`false`|

# Debug

|Setting:|Change Counter|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.Debug.ChangeCounter.Value1.Value2`|
|Description:|This chat command .|

|Setting:|Clear All Timeouts|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.Debug.ClearAllTimeouts`|
|Description:|This chat command .|

|Setting:|Clear Ship Inventory|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.Debug.ClearShipInventory`|
|Description:|This chat command .|

|Setting:|Clear Static Encounters|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.Debug.ClearStaticEncounters`|
|Description:|This chat command .|

|Setting:|Clear Timeouts At Position|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.Debug.ClearTimeoutsAtPosition`|
|Description:|This chat command .|

|Setting:|Clear Unique Encounters|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.Debug.ClearUniqueEncounters`|
|Description:|This chat command .|

|Setting:|Create KPL|
|:----|:----|
|XML:|`N/A`|
|Chat Command 1:|`/MES.Debug.CreateKPL.FactionValue`|
|Chat Command 2:|`/MES.Debug.CreateKPL.FactionValue.RadiusValue`|
|Chat Command 3:|`/MES.Debug.CreateKPL.FactionValue.RadiusValue.DurationValue`|
|Chat Command 4:|`/MES.Debug.CreateKPL.FactionValue.RadiusValue.DurationValue.MaxEncounterValue`|
|Description:|This chat command .|

|Setting:|Remove All Npcs|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.Debug.RemoveAllNpcs`|
|Description:|This chat command .|

|Setting:|Reset Reputation|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.Debug.ResetReputation.Value`|
|Description:|This chat command .|

|Setting:|Unlock Admin Blocks|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.Debug.UnlockAdminBlocks`|
|Description:|This chat command .|

# Info

|Setting:|Get Active NPCs|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.Info.GetActiveNpcs`|
|Description:|This chat command will gather a list of all Active NPC grids identified by the mod and save it to your clipboard.|

|Setting:|Get All Profiles|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.Info.GetAllProfiles`|
|Description:|This chat command will gather a list of all MES Profiles and save it to your clipboard.|

|Setting:|Get Block Definitions|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.Info.GetBlockDefinitions`|
|Description:|This chat command will gather a list of all currently loaded block definition data and save it to your clipboard.|

|Setting:|Get Colors From Grid|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.Info.GetColorsFromGrid`|
|Description:|This chat command will gather a list of all colors from blocks on a particular grid and save it to your clipboard. You must be sitting in a seat of the grid you want to collect data from.|

|Setting:|Get Eligible Spawns At Position|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.Info.GetEligibleSpawnsAtPosition`<br />`/MES.GESAP`|
|Description:|This chat command will gather a list of all Spawn Groups that are eligible to spawn at your position and saves it to your clipboard.|

|Setting:|Get Logging|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.Info.GetLogging.Value1.Value2`|
|Description:|This chat command will copy logged data from a particular logging type and save it to your clipboard. `Value1` is replaced with `BehaviorDebug` or `SpawnDebug`. `Value2` is replaced with any of the logging types from the respective logging types in `Value1`. |

|Setting:|Get Players|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.Info.GetPlayers`|
|Description:|This chat command will collect data on all players currently in the session and save it to your clipboard. |

|Setting:|Get Threat Score|
|:----|:----|
|XML:|`N/A`|
|Chat Command 1:|`/MES.Info.GetThreatScore`<br />`/MES.GTS`|
|Chat Command 2:|`/MES.Info.GetThreatScore.Value`<br />`/MES.GTS.Value`|
|Description:|This chat command will get the current Threat Score near your position and save it to your clipboard. By default, a range of `5000` meters is checked. You can provide a custom distance by replacing the `Value` text in Chat Command 2|

# Spawn

|Setting:|Spawn Space Cargo Ship|
|:----|:----|
|XML:|`N/A`|
|Chat Command 1:|`/MES.Spawn.SpaceCargoShip`<br />`/MES.SSCS`|
|Chat Command 2:|`/MES.Spawn.SpaceCargoShip.Value`<br />`/MES.SSCS.Value`|
|Description:|This chat command allows you to spawn a Space Cargo Ship near your player character. This spawn will obey the rules you have set for encounters to appear in that area. Chat Command 1 will spawn a random group from whatever groups are available. Chat Command 2 allows you to specify the Spawn Group you want to spawn, just replace `Value` with the SubtypeId of the Spawn Group you want to spawn.|

|Setting:|Spawn Random Encounter|
|:----|:----|
|XML:|`N/A`|
|Chat Command 1:|`/MES.Spawn.RandomEncounter`<br />`/MES.SRE`|
|Chat Command 2:|`/MES.Spawn.RandomEncounter.Value`<br />`/MES.SRE.Value`|
|Description:|This chat command allows you to spawn a Random Encounter near your player character. This spawn will obey the rules you have set for encounters to appear in that area. Chat Command 1 will spawn a random group from whatever groups are available. Chat Command 2 allows you to specify the Spawn Group you want to spawn, just replace `Value` with the SubtypeId of the Spawn Group you want to spawn.|

|Setting:|Spawn Boss Encounter|
|:----|:----|
|XML:|`N/A`|
|Chat Command 1:|`/MES.Spawn.BossEncounter`<br />`/MES.SBE`|
|Chat Command 2:|`/MES.Spawn.BossEncounter.Value`<br />`/MES.SBE.Value`|
|Description:|This chat command allows you to spawn a Boss Encounter near your player character. This spawn will obey the rules you have set for encounters to appear in that area. Chat Command 1 will spawn a random group from whatever groups are available. Chat Command 2 allows you to specify the Spawn Group you want to spawn, just replace `Value` with the SubtypeId of the Spawn Group you want to spawn.|

|Setting:|Spawn Planetary Cargo Ship|
|:----|:----|
|XML:|`N/A`|
|Chat Command 1:|`/MES.Spawn.PlanetaryCargoShip`<br />`/MES.SPCS`|
|Chat Command 2:|`/MES.Spawn.PlanetaryCargoShip.Value`<br />`/MES.SPCS.Value`|
|Description:|This chat command allows you to spawn a Planetary Cargo Ship near your player character. This spawn will obey the rules you have set for encounters to appear in that area. Chat Command 1 will spawn a random group from whatever groups are available. Chat Command 2 allows you to specify the Spawn Group you want to spawn, just replace `Value` with the SubtypeId of the Spawn Group you want to spawn.|

|Setting:|Spawn Planetary Installation|
|:----|:----|
|XML:|`N/A`|
|Chat Command 1:|`/MES.Spawn.PlanetaryInstallation`<br />`/MES.SPI`|
|Chat Command 2:|`/MES.Spawn.PlanetaryInstallation.Value`<br />`/MES.SPI.Value`|
|Description:|This chat command allows you to spawn a Planetary Installation near your player character. This spawn will obey the rules you have set for encounters to appear in that area. Chat Command 1 will spawn a random group from whatever groups are available. Chat Command 2 allows you to specify the Spawn Group you want to spawn, just replace `Value` with the SubtypeId of the Spawn Group you want to spawn.|

|Setting:|Activate Wave Spawner|
|:----|:----|
|XML:|`N/A`|
|Chat Command 1:|`/MES.Spawn.WaveSpawner.Space`|
|Chat Command 2:|`/MES.Spawn.WaveSpawner.Planet`|
|Chat Command 3:|`/MES.Spawn.WaveSpawner.Creature`|
|Description:|This chat command allows you to immediately start a Wave Spawning Event for all players in the current session, regardless of whether or not the specific Wave Spawner is enabled in the world. Depending on the chat command you use, you can start Wave Spawning events for Space Cargo Ships, Planetary Cargo Ships, or Creatures/Bots. These events will honor whatever Wave Spawner settings are currently in place in your config files.|

# SpawnDebug


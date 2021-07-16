These commands can be used to force spawn random or specific spawn groups, enable debug mode, get data on loaded spawngroups / active players / active NPCs / etc, and much more. These are chat commands only:

[**BehaviorDebug**](#BehaviorDebug)
[**Debug**](#Debug)
[**Info**](#Info)
[**Spawn**](#Spawn)
[**SpawnDebug**](#SpawnDebug)

# Info

|Setting:|Get Active NPCs|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.Info.GetActiveNpcs`|
|Description:|This chat command will gather a list of all Active NPC grids identified by the mod and save it to your clipboard.|

|Setting:|Get Eligible Spawns At Position|
|:----|:----|
|XML:|`N/A`|
|Chat Command:|`/MES.Info.GetEligibleSpawnsAtPosition`<br />`/MES.GESAP`|
|Description:|This chat command will gather a list of all Spawn Groups that are eligible to spawn at your position and saves it to your clipboard.|


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
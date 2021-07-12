These settings can be found in each of the encounter types configuration files. The settings listed here control the circumstances for when grids of that type should be removed from the game by the clean-up process.

For the chat commands, replace `EncounterType` with any of the types of encounter from the other configurations (eg: `SpaceCargoShips`, `RandomEncounters`, etc)

The settings you can modify are listed below:

|Setting:|UseCleanupSettings|
|:----|:----|
|XML:|`<UseCleanupSettings>Value</UseCleanupSettings>`|
|Chat Command:|`/MES.Settings.EncounterType.UseCleanupSettings.Value`|
|Description:|This setting allows you to specify if the clean-up process should include encounters from this configuration file type. `Value` can be `true` or `false`|

|Setting:|CleanupUseDistance|
|:----|:----|
|XML:|`<CleanupUseDistance>Value</CleanupUseDistance>`|
|Chat Command:|`/MES.Settings.EncounterType.CleanupUseDistance.Value`|
|Description:|This setting allows you to specify if the clean-up process for this encounter type should remove grids that are too far away from players. `Value` can be `true` or `false`|

|Setting:|CleanupUseTimer|
|:----|:----|
|XML:|`<CleanupUseTimer>Value</CleanupUseTimer>`|
|Chat Command:|`/MES.Settings.EncounterType.CleanupUseTimer.Value`|
|Description:|This setting allows you to specify if the clean-up process for this encounter type should remove grids after a certain amount of time. `Value` can be `true` or `false`|

|Setting:|CleanupUseBlockLimit|
|:----|:----|
|XML:|`<CleanupUseBlockLimit>Value</CleanupUseBlockLimit>`|
|Chat Command:|`/MES.Settings.EncounterType.CleanupUseBlockLimit.Value`|
|Description:|This setting allows you to specify if the clean-up process for this encounter type should remove grids that exceed a certain block count. `Value` can be `true` or `false`|

|Setting:|CleanupDistanceStartsTimer|
|:----|:----|
|XML:|`<CleanupDistanceStartsTimer>Value</CleanupDistanceStartsTimer>`|
|Chat Command:|`/MES.Settings.EncounterType.CleanupDistanceStartsTimer.Value`|
|Description:|This setting allows you to specify if the clean-up process for this encounter type should start the clean-up timer for the grid after a player is outside the clean-up distance. `CleanupUseDistance` and `CleanupUseTimer` must both be set to `true` for this feature to work. `Value` can be `true` or `false`|

|Setting:|CleanupResetTimerWithinDistance|
|:----|:----|
|XML:|`<CleanupResetTimerWithinDistance>Value</CleanupResetTimerWithinDistance>`|
|Chat Command:|`/MES.Settings.EncounterType.CleanupResetTimerWithinDistance.Value`|
|Description:|This setting allows you to specify if `CleanupDistanceStartsTimer` is set to `true` and the player is within the clean-up distance limit, then the clean-up timer for that grid will reset to 0. `CleanupDistanceStartsTimer` must be set to `true` for this feature to work. `Value` can be `true` or `false`|

|Setting:|CleanupDistanceTrigger|
|:----|:----|
|XML:|`<CleanupDistanceTrigger>Value</CleanupDistanceTrigger>`|
|Chat Command:|`/MES.Settings.EncounterType.CleanupDistanceTrigger.Value`|
|Description:|This setting allows you to specify the maximum distance from the nearest player before the grid is removed if `CleanupUseDistance` is set to `true`. `Value` can be any number higher than `0`.|

|Setting:|CleanupTimerTrigger|
|:----|:----|
|XML:|`<CleanupTimerTrigger>Value</CleanupTimerTrigger>`|
|Chat Command:|`/MES.Settings.EncounterType.CleanupTimerTrigger.Value`|
|Description:|This setting allows you to specify the time limit (in seconds) before a grid is removed if `CleanupUseTimer` is set to true. `Value` can be set to any integer number higher than `0`|

|Setting:|CleanupBlockLimitTrigger|
|:----|:----|
|XML:|`<CleanupBlockLimitTrigger>Value</CleanupBlockLimitTrigger>`|
|Chat Command:|`/MES.Settings.EncounterType.CleanupBlockLimitTrigger.Value`|
|Description:|This setting allows you to specify the maximum amount of blocks a grid is allowed to have. Grids with a higher block count will be removed if `CleanupUseBlockLimit` is set to `true`. `Value` can be set to any integer number higher than `0`|

|Setting:|CleanupIncludeUnowned|
|:----|:----|
|XML:|`<CleanupIncludeUnowned>Value</CleanupIncludeUnowned>`|
|Chat Command:|`/MES.Settings.EncounterType.CleanupIncludeUnowned.Value`|
|Description:|This setting allows you to specify if unowned grids spawned by the spawner should also be included in the clean-up process. `Value` can be set to `true` or `false`.|

|Setting:|CleanupUnpoweredOverride|
|:----|:----|
|XML:|`<CleanupUnpoweredOverride>Value</CleanupUnpoweredOverride>`|
|Chat Command:|`/MES.Settings.EncounterType.CleanupUnpoweredOverride.Value`|
|Description:|This setting allows you to specify if different Distance and Timer values should be used if the target grid is unpowered. `Value` can be set to `true` or `false`.|

|Setting:|CleanupUnpoweredDistanceTrigger|
|:----|:----|
|XML:|`<CleanupUnpoweredDistanceTrigger>Value</CleanupUnpoweredDistanceTrigger>`|
|Chat Command:|`/MES.Settings.EncounterType.CleanupUnpoweredDistanceTrigger.Value`|
|Description:|This setting allows you to specify the maximum distance from the nearest player before the unpowered grid is removed if `CleanupUseDistance` and `CleanupUnpoweredOverride` is set to `true`. `Value` can be any number higher than `0`.|

|Setting:|CleanupUnpoweredTimerTrigger|
|:----|:----|
|XML:|`<CleanupUnpoweredTimerTrigger>Value</CleanupUnpoweredTimerTrigger>`|
|Chat Command:|`/MES.Settings.EncounterType.CleanupUnpoweredTimerTrigger.Value`|
|Description:|This setting allows you to specify the time limit (in seconds) before the unpowered grid is removed if `CleanupUseTimer` and `CleanupUnpoweredOverride` is set to true. `Value` can be set to any integer number higher than `0`|

|Setting:|UseBlockDisable|
|:----|:----|
|XML:|`<UseBlockDisable>Value</UseBlockDisable>`|
|Chat Command:|`/MES.Settings.EncounterType.UseBlockDisable.Value`|
|Description:|This setting allows you to specify if certain blocks on the NPC grid should be disabled after spawning. `Value` can be set to `true` or `false`|

|Setting:|DisableAirVent|
|:----|:----|
|XML:|`<DisableAirVent>Value</DisableAirVent>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableAirVent.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableAntenna|
|:----|:----|
|XML:|`<DisableAntenna>Value</DisableAntenna>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableAntenna.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableArtificialMass|
|:----|:----|
|XML:|`<DisableArtificialMass>Value</DisableArtificialMass>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableArtificialMass.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableAssembler|
|:----|:----|
|XML:|`<DisableAssembler>Value</DisableAssembler>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableAssembler.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableBattery|
|:----|:----|
|XML:|`<DisableBattery>Value</DisableBattery>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableBattery.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableBeacon|
|:----|:----|
|XML:|`<DisableBeacon>Value</DisableBeacon>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableBeacon.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableCollector|
|:----|:----|
|XML:|`<DisableCollector>Value</DisableCollector>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableCollector.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableConnector|
|:----|:----|
|XML:|`<DisableConnector>Value</DisableConnector>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableConnector.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableConveyorSorter|
|:----|:----|
|XML:|`<DisableConveyorSorter>Value</DisableConveyorSorter>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableConveyorSorter.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableDecoy|
|:----|:----|
|XML:|`<DisableDecoy>Value</DisableDecoy>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableDecoy.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableDrill|
|:----|:----|
|XML:|`<DisableDrill>Value</DisableDrill>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableDrill.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableJumpDrive|
|:----|:----|
|XML:|`<DisableJumpDrive>Value</DisableJumpDrive>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableJumpDrive.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableGasGenerator|
|:----|:----|
|XML:|`<DisableGasGenerator>Value</DisableGasGenerator>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableGasGenerator.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableGasTank|
|:----|:----|
|XML:|`<DisableGasTank>Value</DisableGasTank>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableGasTank.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableGatlingGun|
|:----|:----|
|XML:|`<DisableGatlingGun>Value</DisableGatlingGun>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableGatlingGun.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableGatlingTurret|
|:----|:----|
|XML:|`<DisableGatlingTurret>Value</DisableGatlingTurret>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableGatlingTurret.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableGravityGenerator|
|:----|:----|
|XML:|`<DisableGravityGenerator>Value</DisableGravityGenerator>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableGravityGenerator.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableGrinder|
|:----|:----|
|XML:|`<DisableGrinder>Value</DisableGrinder>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableGrinder.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableGyro|
|:----|:----|
|XML:|`<DisableGyro>Value</DisableGyro>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableGyro.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableInteriorTurret|
|:----|:----|
|XML:|`<DisableInteriorTurret>Value</DisableInteriorTurret>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableInteriorTurret.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableLandingGear|
|:----|:----|
|XML:|`<DisableLandingGear>Value</DisableLandingGear>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableLandingGear.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableLaserAntenna|
|:----|:----|
|XML:|`<DisableLaserAntenna>Value</DisableLaserAntenna>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableLaserAntenna.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableLcdPanel|
|:----|:----|
|XML:|`<DisableLcdPanel>Value</DisableLcdPanel>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableLcdPanel.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableLightBlock|
|:----|:----|
|XML:|`<DisableLightBlock>Value</DisableLightBlock>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableLightBlock.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableMedicalRoom|
|:----|:----|
|XML:|`<DisableMedicalRoom>Value</DisableMedicalRoom>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableMedicalRoom.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableMergeBlock|
|:----|:----|
|XML:|`<DisableMergeBlock>Value</DisableMergeBlock>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableMergeBlock.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableMissileTurret|
|:----|:----|
|XML:|`<DisableMissileTurret>Value</DisableMissileTurret>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableMissileTurret.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableOxygenFarm|
|:----|:----|
|XML:|`<DisableOxygenFarm>Value</DisableOxygenFarm>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableOxygenFarm.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableParachuteHatch|
|:----|:----|
|XML:|`<DisableParachuteHatch>Value</DisableParachuteHatch>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableParachuteHatch.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisablePiston|
|:----|:----|
|XML:|`<DisablePiston>Value</DisablePiston>`|
|Chat Command:|`/MES.Settings.EncounterType.DisablePiston.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableProgrammableBlock|
|:----|:----|
|XML:|`<DisableProgrammableBlock>Value</DisableProgrammableBlock>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableProgrammableBlock.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableProjector|
|:----|:----|
|XML:|`<DisableProjector>Value</DisableProjector>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableProjector.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableReactor|
|:----|:----|
|XML:|`<DisableReactor>Value</DisableReactor>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableReactor.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableRefinery|
|:----|:----|
|XML:|`<DisableRefinery>Value</DisableRefinery>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableRefinery.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableRocketLauncher|
|:----|:----|
|XML:|`<DisableRocketLauncher>Value</DisableRocketLauncher>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableRocketLauncher.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableReloadableRocketLauncher|
|:----|:----|
|XML:|`<DisableReloadableRocketLauncher>Value</DisableReloadableRocketLauncher>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableReloadableRocketLauncher.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableRotor|
|:----|:----|
|XML:|`<DisableRotor>Value</DisableRotor>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableRotor.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableSensor|
|:----|:----|
|XML:|`<DisableSensor>Value</DisableSensor>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableSensor.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableSolarPanel|
|:----|:----|
|XML:|`<DisableSolarPanel>Value</DisableSolarPanel>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableSolarPanel.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableSoundBlock|
|:----|:----|
|XML:|`<DisableSoundBlock>Value</DisableSoundBlock>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableSoundBlock.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableSpaceBall|
|:----|:----|
|XML:|`<DisableSpaceBall>Value</DisableSpaceBall>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableSpaceBall.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableTimerBlock|
|:----|:----|
|XML:|`<DisableTimerBlock>Value</DisableTimerBlock>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableTimerBlock.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableThruster|
|:----|:----|
|XML:|`<DisableThruster>Value</DisableThruster>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableThruster.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableWelder|
|:----|:----|
|XML:|`<DisableWelder>Value</DisableWelder>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableWelder.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

|Setting:|DisableUpgradeModule|
|:----|:----|
|XML:|`<DisableUpgradeModule>Value</DisableUpgradeModule>`|
|Chat Command:|`/MES.Settings.EncounterType.DisableUpgradeModule.Value`|
|Description:|This setting allows you to specify if the block type listed in the setting name should be disabled. `Value` can be set to `true` or `false`.|

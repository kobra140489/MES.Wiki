SpawnGroups are definitions that provide rules about an NPC encounter to the Modular Encounters Systems Spawning Mechanism.

The SpawnGroups that the Modular Encounters Systems uses utilize the `<Description>` tags to define many custom rules and modifications to a spawned entity. This includes conditions for when the encounter is allowed to spawn, and manipulations that are applied to the prefabs (grids) before they are spawned into the world.



[**Conditions**](#)  
[**Economy**](#Economy)  
[**Faction**](#Faction)  
[**Manipulations**](#)  
[**Misc**](#Misc)  
[**Replenishment**](#)  

# Conditions



# Economy

<!-- InitializeStoreBlocks  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|InitializeStoreBlocks|
|:----|:----|
|Tag Format:|`[InitializeStoreBlocks:Value]`|
|Description:|If set to `true`, any Store Blocks on this grid will be populated with all items in inventory the Store Block is connected to.|
|Allowed Values:|`true`<br>`false`|
|Default Value(s):|`false`|
|Multiple Tag Allowed:|No|

<!-- ContainerTypesForStoreOrders  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ContainerTypesForStoreOrders|
|:----|:----|
|Tag Format:|`[ContainerTypesForStoreOrders:Value1,Value2,Value3,etc]`|
|Description:|This tag allows you to specify the names of ContainerType definitions that are randomly selected to populate the Store Block Sell Screen on your NPC Grid.|
|Allowed Values:|Any ContainerType SubtypeId<br>If providing multiple values, use comma with no spaces as shown in `Tag Format`|
|Default Value(s):|`none`|
|Multiple Tag Allowed:|No|


# Faction

<!-- FactionOwner  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|FactionOwner|
|:----|:----|
|Tag Format:|`[FactionOwner:Value]`|
|Description:|This tag allows you to assign a SpawnGroup to be owned by a specific NPC faction. Factions with human players cannot be assigned. To assign a faction, replace Value with the Faction Tag you want to use. Eg: `SPRT`, `SPID`, etc. You can also remove ownership all together by providing `Nobody` as your value. If your provided tag cannot be found (IE: there's no NPC faction with that tag), the SpawnGroup will be set to be owned by `Nobody`. Default value is `SPRT` if tag is not included.|
|Allowed Values:|Any Valid FactionTag or `Nobody`|
|Default Value(s):|`SPRT`|
|Multiple Tag Allowed:|No|

<!-- UseRandomMinerFaction  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|UseRandomMinerFaction|
|:----|:----|
|Tag Format:|`[UseRandomMinerFaction:Value]`|
|Description:|If set to `true`, the spawned prefabs in this SpawnGroup will use a random NPC faction that is designated as a Miner Faction.|
|Allowed Values:|`true`<br>`false`|
|Default Value(s):|`false`|
|Multiple Tag Allowed:|No|

<!-- UseRandomBuilderFaction  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|UseRandomBuilderFaction|
|:----|:----|
|Tag Format:|`[UseRandomBuilderFaction:Value]`|
|Description:|If set to `true`, the spawned prefabs in this SpawnGroup will use a random NPC faction that is designated as a Builder Faction.|
|Allowed Values:|`true`<br>`false`|
|Default Value(s):|`false`|
|Multiple Tag Allowed:|No|

<!-- UseRandomTraderFaction  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|UseRandomTraderFaction|
|:----|:----|
|Tag Format:|`[UseRandomTraderFaction:Value]`|
|Description:|If set to `true`, the spawned prefabs in this SpawnGroup will use a random NPC faction that is designated as a Trader Faction.|
|Allowed Values:|`true`<br>`false`|
|Default Value(s):|`false`|
|Multiple Tag Allowed:|No|


# Manipulations  




# Misc

<!-- IgnoreCleanupRules  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|IgnoreCleanupRules|
|:----|:----|
|Tag Format:|`[IgnoreCleanupRules:Value]`|
|Description:|This tag specifies if a SpawnGroup should be ignored by the mod Clean-Up rules (this does not include path despawn for Cargo Ship Type Spawns).|
|Allowed Values:|`true`<br>`false`|
|Default Value(s):|`false`|
|Multiple Tag Allowed:|No|

<!-- PauseAutopilotAtPlayerDistance  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|PauseAutopilotAtPlayerDistance|
|:----|:----|
|Tag Format:|`[PauseAutopilotAtPlayerDistance:Value]`|
|Description:|If player is within this distance from a Cargo Ship using Auto-Pilot, the ship will come to a stop. It will resume travel once the player is outside of this distance.|
|Allowed Values:|Any Number Greater Than `0`|
|Default Value(s):|`-1`|
|Multiple Tag Allowed:|No|


# Replenishment

<!-- ReplenishSystems  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ReplenishSystems|
|:----|:----|
|Tag Format:|`[ReplenishSystems:Value]`|
|Description:|This tag specifies if the prefabs in a SpawnGroup should have their weapons, parachutes, and reactors restocked with ammo and fuel on spawn.|
|Allowed Values:|`true`<br>`false`|
|Default Value(s):|`false`|
|Multiple Tag Allowed:|No|

<!-- ReplenishProfiles-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ReplenishProfiles|
|:----|:----|
|Tag Format:|`[ReplenishProfiles:Value]`|
|Description:|This tag specifies one or more Replenishment Profile IDs that are used to determine what kinds of replenishment limits the grid will receive.|
|Allowed Values:|Any Replenishment Profile SubtypeId|
|Default Value(s):|`N/A`|
|Multiple Tag Allowed:|Yes|

<!-- IgnoreGlobalReplenishProfiles-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|IgnoreGlobalReplenishProfiles|
|:----|:----|
|Tag Format:|`[IgnoreGlobalReplenishProfiles:Value]`|
|Description:|This tag specifies if grid replenishment should ignore any Global Replenishment Profiles that are present in the game world.|
|Allowed Values:|`true`<br>`false`|
|Default Value(s):|`false`|
|Multiple Tag Allowed:|No|

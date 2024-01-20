Filter players for certain actions ,or use it as an extra condition for Events, Trigger and Spawnconditions

### Used for some tags in
[Event Actions](https://github.com/MeridiusIX/Modular-Encounters-Systems/wiki/Event-Action#Players) 



Here's an example of how a Player Condition Profile definition is setup:
```
<EntityComponent xsi:type="MyObjectBuilder_InventoryComponentDefinition">
      <Id>
          <TypeId>Inventory</TypeId>
          <SubtypeId>PlayerConditionProfile-AHEFriendly</SubtypeId>
      </Id>
      <Description>
	[MES Player Condition]
	
	[CheckPlayerReputation:true]
	[CheckReputationwithFaction:AHE]
	[MinPlayerReputation:500]
	[MaxPlayerReputation:1500]
      </Description> 
    </EntityComponent>
```




<!--AllowOverrides  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|AllowOverrides|
|:----|:----|
|Tag Format:|`[AllowOverrides:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--AllPlayersMatchThisCondition  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|AllPlayersMatchThisCondition|
|:----|:----|
|Tag Format:|`[AllPlayersMatchThisCondition:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--UseFailCondition  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|UseFailCondition|
|:----|:----|
|Tag Format:|`[UseFailCondition:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--UseAnyPassingCondition  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|UseAnyPassingCondition|
|:----|:----|
|Tag Format:|`[UseAnyPassingCondition:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--CheckPlayerReputation  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|CheckPlayerReputation|
|:----|:----|
|Tag Format:|`[CheckPlayerReputation:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--CheckReputationwithFaction  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|CheckReputationwithFaction|
|:----|:----|
|Tag Format:|`[CheckReputationwithFaction:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding `:`, `[`, `]`|
|Multiple Tag Allowed:|yes|
<!--MinPlayerReputation  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|MinPlayerReputation|
|:----|:----|
|Tag Format:|`[MinPlayerReputation:Value]`|
|Description:|nan|
|Allowed Values:|Any interger |
|Multiple Tag Allowed:|yes|
<!--MaxPlayerReputation  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|MaxPlayerReputation|
|:----|:----|
|Tag Format:|`[MaxPlayerReputation:Value]`|
|Description:|nan|
|Allowed Values:|Any interger|
|Multiple Tag Allowed:|yes|
<!--CheckLastRespawnShipName  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|CheckLastRespawnShipName|
|:----|:----|
|Tag Format:|`[CheckLastRespawnShipName:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--LastRespawnShipName  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|LastRespawnShipName|
|:----|:----|
|Tag Format:|`[LastRespawnShipName:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding `:`, `[`, `]`|
|Multiple Tag Allowed:|no|
<!--CheckPlayerTags  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|CheckPlayerTags|
|:----|:----|
|Tag Format:|`[CheckPlayerTags:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--IncludedPlayerTag  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|IncludedPlayerTag|
|:----|:----|
|Tag Format:|`[IncludedPlayerTag:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding `:`, `[`, `]`|
|Multiple Tag Allowed:|yes|
<!--ExcludedPlayerTag  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ExcludedPlayerTag|
|:----|:----|
|Tag Format:|`[ExcludedPlayerTag:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding `:`, `[`, `]`|
|Multiple Tag Allowed:|yes|
<!--CheckPlayerNear  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|CheckPlayerNear|
|:----|:----|
|Tag Format:|`[CheckPlayerNear:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--PlayerNearCoords  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|PlayerNearCoords|
|:----|:----|
|Tag Format:|`[PlayerNearCoords:Value]`|
|Description:|nan|
|Allowed Values:|A Vector3D Value in the following format:<br />`{X:# Y:# Z:#}`<br />.|
|Multiple Tag Allowed:|no|
<!--PlayerNearDistanceFromCoords  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|PlayerNearDistanceFromCoords|
|:----|:----|
|Tag Format:|`[PlayerNearDistanceFromCoords:Value]`|
|Description:|nan|
|Allowed Values:|Any interger equal or greater than 0|
|Multiple Tag Allowed:|no|
<!--PlayerNearMinDistanceFromCoords  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|PlayerNearMinDistanceFromCoords|
|:----|:----|
|Tag Format:|`[PlayerNearMinDistanceFromCoords:Value]`|
|Description:|nan|
|Allowed Values:|Any interger equal or greater than 0|
|Multiple Tag Allowed:|no|
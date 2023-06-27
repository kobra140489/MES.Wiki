These profile are what execute specified actions when the conditions in a Event Profile are satisfied. It is important that you use a unique SubtypeId for each Action Profile you create, otherwise they may not work correctly.

Here is an example of how an Event Action Profile definition is setup:

```
<?xml version="1.0"?>
<Definitions xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <EntityComponents>

    <EntityComponent xsi:type="MyObjectBuilder_InventoryComponentDefinition">
      <Id>
          <TypeId>Inventory</TypeId>
          <SubtypeId>TAG-EventAction-Example</SubtypeId>
      </Id>
      <Description>

	  [MES Event Action]
      
          [UseChatBroadcast:true]
          [ChatData:RAI-ExampleChatProfile]

	  [ChangeBooleans:true]
	  [SetBooleansTrue:SomeRandomBool]	
      </Description>
      
    </EntityComponent>

  </EntityComponents>
</Definitions>
```


<!--DebugHudMessage  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|DebugHudMessage|
|:----|:----|
|Tag Format:|`[DebugHudMessage:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding `:`, `[`, `]`|
|Multiple Tag Allowed:|no|
<!--ChangeBooleans  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ChangeBooleans|
|:----|:----|
|Tag Format:|`[ChangeBooleans:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--SetBooleansTrue  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|SetBooleansTrue|
|:----|:----|
|Tag Format:|`[SetBooleansTrue:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding `:`, `[`, `]`|
|Multiple Tag Allowed:|yes|
<!--SetBooleansFalse  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|SetBooleansFalse|
|:----|:----|
|Tag Format:|`[SetBooleansFalse:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding `:`, `[`, `]`|
|Multiple Tag Allowed:|yes|
<!--ChangeCounters  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ChangeCounters|
|:----|:----|
|Tag Format:|`[ChangeCounters:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--IncreaseCounters  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|IncreaseCounters|
|:----|:----|
|Tag Format:|`[IncreaseCounters:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding `:`, `[`, `]`|
|Multiple Tag Allowed:|yes|
<!--DecreaseCounters  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|DecreaseCounters|
|:----|:----|
|Tag Format:|`[DecreaseCounters:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding `:`, `[`, `]`|
|Multiple Tag Allowed:|yes|
<!--IncreaseCountersAmount  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|IncreaseCountersAmount|
|:----|:----|
|Tag Format:|`[IncreaseCountersAmount:Value]`|
|Description:|nan|
|Allowed Values:|Any interger equal or greater than 0|
|Multiple Tag Allowed:|yes|
<!--DecreaseCountersAmount  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|DecreaseCountersAmount|
|:----|:----|
|Tag Format:|`[DecreaseCountersAmount:Value]`|
|Description:|nan|
|Allowed Values:|Any interger equal or greater than 0|
|Multiple Tag Allowed:|yes|
<!--SetCounters  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|SetCounters|
|:----|:----|
|Tag Format:|`[SetCounters:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding `:`, `[`, `]`|
|Multiple Tag Allowed:|yes|
<!--SetCountersAmount  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|SetCountersAmount|
|:----|:----|
|Tag Format:|`[SetCountersAmount:Value]`|
|Description:|nan|
|Allowed Values:|Any interger equal or greater than 0|
|Multiple Tag Allowed:|yes|
<!--UseChatBroadcast  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|UseChatBroadcast|
|:----|:----|
|Tag Format:|`[UseChatBroadcast:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--ChatData  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ChatData|
|:----|:----|
|Tag Format:|`[ChatData:Value]`|
|Description:|nan|
|Allowed Values:|Any behaviour Chat Profile SubtypeId|
|Multiple Tag Allowed:|yes|
<!--SpawnEncounter  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|SpawnEncounter|
|:----|:----|
|Tag Format:|`[SpawnEncounter:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--SpawnCoords-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|SpawnCoords|
|:----|:----|
|Tag Format:|`[SpawnCoords:Value]`|
|Description:|nan|
|Allowed Values:|A Vector3D Value in the following format:<br />`{X:# Y:# Z:#}`<br />Replace `#` with values in meters.|
|Multiple Tag Allowed:|yes|
<!--SpawnFactionTags  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|SpawnFactionTags|
|:----|:----|
|Tag Format:|`[SpawnFactionTags:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding `:`, `[`, `]`|
|Multiple Tag Allowed:|yes|
<!--Spawner  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Spawner|
|:----|:----|
|Tag Format:|`[Spawner:Value]`|
|Description:|nan|
|Allowed Values:|Any behaviour Spawner Profile SubtypeId|
|Multiple Tag Allowed:|no|
<!--ChangeZoneAtPosition  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ChangeZoneAtPosition|
|:----|:----|
|Tag Format:|`[ChangeZoneAtPosition:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|yes|
<!--ZoneNames  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ZoneNames|
|:----|:----|
|Tag Format:|`[ZoneNames:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding `:`, `[`, `]`|
|Multiple Tag Allowed:|yes|
<!--ZoneCoords  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ZoneCoords|
|:----|:----|
|Tag Format:|`[ZoneCoords:Value]`|
|Description:|nan|
|Allowed Values:|A Vector3D Value in the following format:<br />`{X:# Y:# Z:#}`<br />Replace `#` with values in meters.|
|Multiple Tag Allowed:|yes|
<!--ZoneToggleActiveModes  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ZoneToggleActiveModes|
|:----|:----|
|Tag Format:|`[ZoneToggleActiveModes:Value]`|
|Description:|true will activate it. false will set disable it|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|yes|
<!--AddGPSForAll  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|AddGPSForAll|
|:----|:----|
|Tag Format:|`[AddGPSForAll:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--RemoveGPSForAll  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|RemoveGPSForAll|
|:----|:----|
|Tag Format:|`[RemoveGPSForAll:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--UseGPSObjective  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|UseGPSObjective|
|:----|:----|
|Tag Format:|`[UseGPSObjective:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--GPSNames  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|GPSNames|
|:----|:----|
|Tag Format:|`[GPSNames:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding `:`, `[`, `]`|
|Multiple Tag Allowed:|yes|
<!--GPSDescriptions  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|GPSDescriptions|
|:----|:----|
|Tag Format:|`[GPSDescriptions:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding `:`, `[`, `]`|
|Multiple Tag Allowed:|yes|
<!--GPSCoords-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|GPSCoords|
|:----|:----|
|Tag Format:|`[GPSCoords:Value]`|
|Description:|nan|
|Allowed Values:|A Vector3D Value in the following format:<br />`{X:# Y:# Z:#}`<br />Replace `#` with values in meters.|
|Multiple Tag Allowed:|yes|
<!--GPSColors  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|GPSColors|
|:----|:----|
|Tag Format:|`[GPSColors:Value]`|
|Description:|nan|
|Allowed Values:|A Vector3D Value in the following format:<br />`{X:# Y:# Z:#}`<br />.|
|Multiple Tag Allowed:|yes|
<!--ToggleEvents  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ToggleEvents|
|:----|:----|
|Tag Format:|`[ToggleEvents:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--ToggleEventIds  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ToggleEventIds|
|:----|:----|
|Tag Format:|`[ToggleEventIds:Value]`|
|Description:|nan|
|Allowed Values:|Any Event Profile SubtypeId|
|Multiple Tag Allowed:|yes|
<!--ToggleEventIdModes  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ToggleEventIdModes|
|:----|:----|
|Tag Format:|`[ToggleEventIdModes:Value]`|
|Description:|true will activate it. false will set disable it|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|yes|
<!--ToggleEventTags  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ToggleEventTags|
|:----|:----|
|Tag Format:|`[ToggleEventTags:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding `:`, `[`, `]`|
|Multiple Tag Allowed:|yes|
<!--ToggleEventTagModes  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ToggleEventTagModes|
|:----|:----|
|Tag Format:|`[ToggleEventTagModes:Value]`|
|Description:|true will activate it. false will set disable it|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|yes|
<!--ResetCooldownTimeOfEvents  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ResetCooldownTimeOfEvents|
|:----|:----|
|Tag Format:|`[ResetCooldownTimeOfEvents:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--ResetEventCooldownIds  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ResetEventCooldownIds|
|:----|:----|
|Tag Format:|`[ResetEventCooldownIds:Value]`|
|Description:|nan|
|Allowed Values:|Any Event Profile SubtypeId|
|Multiple Tag Allowed:|yes|
<!--ResetEventCooldownTags  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ResetEventCooldownTags|
|:----|:----|
|Tag Format:|`[ResetEventCooldownTags:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding characters ": [ ]"|
|Multiple Tag Allowed:|yes|
<!--ActivateCustomAction  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ActivateCustomAction|
|:----|:----|
|Tag Format:|`[ActivateCustomAction:Value]`|
|Description:|nan|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|no|
<!--CustomActionName  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|CustomActionName|
|:----|:----|
|Tag Format:|`[CustomActionName:Value]`|
|Description:|nan|
|Allowed Values:|Any name string excluding `:`, `[`, `]`|
|Multiple Tag Allowed:|no|
<!--CustomActionArguments  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|CustomActionArguments|
|:----|:----|
|Tag Format:|`[CustomActionArguments:Value]`|
|Description:|nan|
|Allowed Values:|t.b.d|
|Multiple Tag Allowed:|yes|
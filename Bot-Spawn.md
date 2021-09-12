Bot Spawn Profiles in Modular Encounters Systems allow you to specify a set of rules for how a bot is configured before it is spawned by the AiEnabled mod.

Here's an example of how a Bot Spawn Profile Definition is setup:

```
<?xml version="1.0"?>
<Definitions xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <EntityComponents>

    <EntityComponent xsi:type="MyObjectBuilder_InventoryComponentDefinition">
      <Id>
          <TypeId>Inventory</TypeId>
          <SubtypeId>MES-ExampleBotSpawnProfile</SubtypeId>
      </Id>
      <Description>

      [MES Bot Spawn]
      
      [BotType:Police_Bot]
      [BotDisplayName:Combat Bot]
      
      </Description>
      
    </EntityComponent>

  </EntityComponents>
</Definitions>
```

Below are all of the eligible tags you can use in your Bot Spawn Profiles:

<!--BotType-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|BotType|
|:----|:----|
|Tag Format:|`[BotType:Value]`|
|Description:|This tag specifies the type of bot that will be spawned.|
|Allowed Values:|Any Bot Character SubtypeId|
|Multiple Tag Allowed:|No|

<!--BotBehavior-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|BotBehavior|
|:----|:----|
|Tag Format:|`[BotBehavior:Value]`|
|Description:|This tag specifies the behavior that the spawned bot will use. If this tag is not defined, then it will use the default behavior that AiEnabled would use when spawning a bot of the selected type.|
|Allowed Values:|Any AiEnabled Behavior Role|
|Multiple Tag Allowed:|No|

<!--BotDisplayName-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|BotDisplayName|
|:----|:----|
|Tag Format:|`[BotDisplayName:Value]`|
|Description:|This tag specifies the Display Name of the spawned bot.|
|Allowed Values:|Any Name|
|Multiple Tag Allowed:|No|

<!--Color-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Color|
|:----|:----|
|Tag Format:|`[Color:Value]`|
|Description:|Specifies the ColorMaskHSV of the spawned bot character.|
|Allowed Values:|Any Vector3 Value using this format<br />`{X:0 Y:0 Z:0}`|
|Multiple Tag Allowed:|No|

Trigger Profiles in Rival AI are used to watch for specific events that happen near/to your current NPC grid, and then trigger an **Action Profile** if the conditions are satisfied. This allows for a wide variety of **If THIS, Do THAT** type of behavior. You can attach your Trigger Profiles to any Behavior Profile by adding a `[Triggers:Value]` tag to the Behavior and replace `Value` with the SubtypeId of your Trigger Profile. Example:

`[Triggers:RAI-ExampleTriggerProfile]`

Multiple Trigger Profiles can be attached to a single behavior as well, just include additional `[Triggers:Value]` lines in your Behavior Profile. It is important that you use a unique SubtypeId for each Trigger Profile you create, otherwise they may not work correctly.

Here is an example of how a Trigger Profile definition is setup:

```
<?xml version="1.0"?>
<Definitions xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <EntityComponents>

    <EntityComponent xsi:type="MyObjectBuilder_InventoryComponentDefinition">
      <Id>
          <TypeId>Inventory</TypeId>
          <SubtypeId>RAI-ExampleTriggerProfile</SubtypeId>
      </Id>
      <Description>

      [RivalAI Trigger]
      
      </Description>
      
    </EntityComponent>

  </EntityComponents>
</Definitions>
```

All Trigger Profiles require the `Type` tag. This is what determines what sort of conditions the Trigger watches for. Here is a list of all the available Types and their descriptions.

|Type:|Description:|
|:----|:----|
|`AcquiredTarget`|A trigger that activates when the NPC has acquired a target|
|`BehaviorTriggerA`|A trigger that is executed when behavior specific events happen (see Behavior Specific Tags for details)|
|`BehaviorTriggerB`|A trigger that is executed when behavior specific events happen (see Behavior Specific Tags for details)|
|`BehaviorTriggerC`|A trigger that is executed when behavior specific events happen (see Behavior Specific Tags for details)|
|`BehaviorTriggerD`|A trigger that is executed when behavior specific events happen (see Behavior Specific Tags for details)|
|`BehaviorTriggerE`|A trigger that is executed when behavior specific events happen (see Behavior Specific Tags for details)|
|`BehaviorTriggerF`|A trigger that is executed when behavior specific events happen (see Behavior Specific Tags for details)|
|`CommandReceived`|A command listener that executes actions if another NPC Behavior broadcasts a correct Command Code|
|`Compromised`|A trigger that is activated when the Remote Control block stops working.|
|`Damage`|A damage watcher that executes actions when damage to the NPC is detected.|
|`Despawn`|A trigger that is activated when the NPC is despawned by RivalAI.|
|`DespawnMES`|A trigger that is activated when the NPC is despawned by the Modular Encounters Spawner.|
|`HasTarget`|A trigger that will activate while NPC has a valid target.|
|`LostTarget`|A trigger that activates when the NPC has lost a target.|
|`Manual`|A trigger that activates when specifically called from another Action Profile.|
|`NoTarget`|A trigger that will activate while NPC has no valid target.|
|`NoWeapon`|A block watcher that executes actions if all weapons on the NPC grid becomes non-fireable|
|`PlayerFar`|A proximity watcher that executes actions if players are outside a certain range.|
|`PlayerKnownLocation`|A trigger that will activate if the NPC is inside a Known Player Location belonging to its own faction.|
|`PlayerNear`|A proximity watcher that executes actions if players come within a certain range.|
|`Retreat`|A trigger that will activate if the Retreat BehaviorMode is activated on an NPC.|
|`SensorActive`|A proximity watcher that executes actions if a named Sensor Block is currently Activated.|
|`SensorIdle`|A proximity watcher that executes actions if a named Sensor Block is currently Idle.|
|`Session`|A trigger that only activates once per session (ie: when the encounter spawns or when the game loads/reloads).|
|`TargetFar`|A proximity watcher that executes actions if a target is outside a certain range.|
|`TargetInSafezone`|A target watcher that executes actions if a target moves into a SafeZone|
|`TargetNear`|A proximity watcher that executes actions if a target come within a certain range.|
|`Timer`|A basic timer trigger that executes actions after the cooldown time limit has passed.|
|`TurretTarget`|A turret target watcher that executes actions when a turret acquires a target.|
|`Weather`|A trigger that will execute if the NPC is within one or more specified Weather Systems.|

***

Below are the tags you are able to use in your Trigger Profiles. Please note that some tags are only compatible with certain Trigger Types. Those tags are identified in the `Compatible Types:` section of each tag description.

<!--Type  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Type|
|:----|:----|
|Tag Format:|`[Type:Value]`|
|Description:|This tag specifies the type of Trigger this profile should use.|
|Allowed Values:|`See Table Above For Allowed Values`|
|Compatible Types:|`All`|
|Multiple Tag Allowed:|No|

<!--UseTrigger  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|UseTrigger|
|:----|:----|
|Tag Format:|`[UseTrigger:Value]`|
|Description:|This tag specifies if an attached Trigger Profile should be used / active.|
|Allowed Values:|`true`<br>`false`|
|Compatible Types:|`All`|
|Multiple Tag Allowed:|No|

<!--TargetDistance  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|TargetDistance|
|:----|:----|
|Tag Format:|`[TargetDistance:Value]`|
|Description:|This tag specifies the distance a player / target must be within before the Trigger activates.|
|Allowed Values:|Any number greater than `0`|
|Compatible Types:|`PlayerNear`<br>`PlayerFar`<br>`TargetNear`<br>`TargetFar`|
|Multiple Tag Allowed:|No|

<!--AllowTargetFarWithoutTarget-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|AllowTargetFarWithoutTarget|
|:----|:----|
|Tag Format:|`[AllowTargetFarWithoutTarget:Value]`|
|Description:|Determines if the Trigger type `TargetFar` can activate if the behavior does not currently have a target.|
|Allowed Values:|`true`<br>`false`|
|Compatible Types:|`TargetFar`|
|Multiple Tag Allowed:|No|

<!--InsideAntenna  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|InsideAntenna|
|:----|:----|
|Tag Format:|`[InsideAntenna:Value]`|
|Description:|This tag specifies if a target must be within the range of an active Antenna on the NPC grid before activating. Please note that you should still define a `TargetDistance` distance tag if using this.|
|Allowed Values:|`true`<br>`false`|
|Compatible Types:|`PlayerNear`<br>`PlayerFar`|
|Multiple Tag Allowed:|No|

<!--InsideAntennaName  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|InsideAntennaName|
|:----|:----|
|Tag Format:|`[InsideAntennaName:Value]`|
|Description:|This tag specifies the specific block name the antenna must have if using the `InsideAntenna` tag.|
|Allowed Values:|Any Text Value|
|Compatible Types:|`PlayerNear`<br>`PlayerFar`|
|Multiple Tag Allowed:|No|

<!--PlayerNearPositionOffset  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|PlayerNearPositionOffset|
|:----|:----|
|Tag Format:|`[PlayerNearPositionOffset:Value]`|
|Description:|This tag specifies an X,Y,Z offset from where the NPC Remote Control is location that is used for `PlayerNear` calculations instead of just the block's position.|
|Allowed Values:|Vector3D Value (Example below)</br >`{X:0 Y:0 Z:0}`</br >X -+ = Left/Right</br >Y -+ = Down/Up</br >Z -+ = Back/Forward|
|Compatible Types:|`PlayerNear`<br>`PlayerFar`|
|Multiple Tag Allowed:|No|

<!--MinCooldownMs  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|MinCooldownMs|
|:----|:----|
|Tag Format:|`[MinCooldownMs:Value]`|
|Description:|This tag specifies the minimum time (in milliseconds) that a trigger must wait before it can be triggered again.|
|Allowed Values:|Any integer higher than `0`<br />Must be lower than `MaxCooldownMs`|
|Compatible Types:|`All`|
|Multiple Tag Allowed:|No|

<!--MaxCooldownMs  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|MaxCooldownMs|
|:----|:----|
|Tag Format:|`[MaxCooldownMs:Value]`|
|Description:|This tag specifies the maximum time (in milliseconds) that a trigger must wait before it can be triggered again.|
|Allowed Values:|Any integer higher than `0`<br />Must be higher than `MinCooldownMs`|
|Compatible Types:|`All`|
|Multiple Tag Allowed:|No|

<!--StartsReady  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|StartsReady|
|:----|:----|
|Tag Format:|`[StartsReady:Value]`|
|Description:|This tag specifies if the trigger timer is ready to activate when the NPC loads.|
|Allowed Values:|`true`<br>`false`|
|Compatible Types:|`All`|
|Multiple Tag Allowed:|No|

<!--MaxActions  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|MaxActions|
|:----|:----|
|Tag Format:|`[MaxActions:Value]`|
|Description:|This tag specifies how many times this trigger is allowed to activate its Actions.|
|Allowed Values:|Any integer higher than `0`<br />`-1` for no limit|
|Compatible Types:|`All`|
|Multiple Tag Allowed:|No|

<!--ActionExecution  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ActionExecution|
|:----|:----|
|Tag Format:|`[ActionExecution:Value]`|
|Description:|This tag specifies how triggers with Multiple Action Profiles will execute. `All` will execute every Action at once when the trigger is activated. `Sequential` will process Actions one at a time per activation of Trigger. `Random` will select a random Action to execute when the Trigger is activated.|
|Allowed Values:|`All`<br />`Sequential`<br />`Random`|
|Compatible Types:|`All`|
|Multiple Tag Allowed:|No|

<!--Actions  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Actions|
|:----|:----|
|Tag Format:|`[Actions:Value]`|
|Description:|This tag specifies which Action Profile will be executed when the Trigger Profile conditions are satisfied.|
|Allowed Values:|Any Action Profile SubtypeId|
|Compatible Types:|`All`|
|Multiple Tag Allowed:|Yes|

<!--DamageTypes  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|DamageTypes|
|:----|:----|
|Tag Format:|`[DamageTypes:Value]`|
|Description:|This tag specifies the types of Damage that can activate a Trigger Profile using the Damage Type. Below you will find the vanilla damage types - you are not limited to these exclusively, since some modded weapons define their own custom damage types as well.|
|Allowed Values:|`Any`, `Unknown`, `Explosion`, `Rocket`, `Bullet`, <br />`Mine`, `Environment`, `Drill`, `Radioactivity`, `Deformation`, <br />`Suicide`, `Fall`, `Weapon`, `Fire`, `Squeez`, <br />`Grind`, `Weld`, `Asphyxia`, `LowPressure`, `Bolt`, <br />`Destruction`, `Debug`, `Wolf`, `Spider`, `Temperature`|
|Compatible Types:|`Damage`|
|Multiple Tag Allowed:|Yes|

<!--ExcludedDamageTypes-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ExcludedDamageTypes|
|:----|:----|
|Tag Format:|`[ExcludedDamageTypes:Value]`|
|Description:|This tag specifies the types of Damage that should be excluded from being able to activate the trigger if you use the `Any` value in your `DamageTypes` tag.|
|Allowed Values:|`Unknown`, `Explosion`, `Rocket`, `Bullet`, <br />`Mine`, `Environment`, `Drill`, `Radioactivity`, `Deformation`, <br />`Suicide`, `Fall`, `Weapon`, `Fire`, `Squeez`, <br />`Grind`, `Weld`, `Asphyxia`, `LowPressure`, `Bolt`, <br />`Destruction`, `Debug`, `Wolf`, `Spider`, `Temperature`|
|Compatible Types:|`Damage`|
|Multiple Tag Allowed:|Yes|

<!--MinPlayerReputation  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|MinPlayerReputation|
|:----|:----|
|Tag Format:|`[MinPlayerReputation:Value]`|
|Description:|This tag specifies the minimum reputation a nearby player must have with the current NPC.|
|Allowed Values:|Any integer between `-1500` and `1500`<br />Must be lower than `MaxPlayerReputation`|
|Compatible Types:|`PlayerNear`<br>`PlayerFar`|
|Multiple Tag Allowed:|No|

<!--MaxPlayerReputation  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|MaxPlayerReputation|
|:----|:----|
|Tag Format:|`[MaxPlayerReputation:Value]`|
|Description:|This tag specifies the maximum reputation a nearby player must have with the current NPC.|
|Allowed Values:|Any integer between `-1500` and `1500`<br />Must be higher than `MinPlayerReputation`|
|Compatible Types:|`PlayerNear`<br>`PlayerFar`|
|Multiple Tag Allowed:|No|

<!--AllPlayersMustMatchReputation  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|AllPlayersMustMatchReputation|
|:----|:----|
|Tag Format:|`[AllPlayersMustMatchReputation:Value]`|
|Description:|This tag specifies if all players within the range of the `CustomReputationRangeCheck` value must match the minimum and maximum reputation values. IF they do not, then the trigger will fail to execute.|
|Allowed Values:|`true`<br>`false`|
|Compatible Types:|`PlayerNear`<br>`PlayerFar`|
|Multiple Tag Allowed:|No|

<!--CustomReputationRangeCheck  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|CustomReputationRangeCheck|
|:----|:----|
|Tag Format:|`[CustomReputationRangeCheck:Value]`|
|Description:|This tag specifies the range that is used to check player reputations if `AllPlayersMustMatchReputation` is `true`.|
|Allowed Values:|Any Number Greater Than `0`|
|Compatible Types:|`PlayerNear`<br>`PlayerFar`|
|Multiple Tag Allowed:|No|

<!--Conditions  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Conditions|
|:----|:----|
|Tag Format:|`[Conditions:Value]`|
|Description:|This tag specifies allows you to provide a SubtypeId of a Condition Profile that can be used to perform further checks before the Trigger is activated.|
|Allowed Values:|Any Condition Profile SubtypeId|
|Compatible Types:|`All`|
|Multiple Tag Allowed:|No|

<!--ConditionCheckResetsTimer  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ConditionCheckResetsTimer|
|:----|:----|
|Tag Format:|`[ConditionCheckResetsTimer:Value]`|
|Description:|Specifies if a ConditionCheck (whether successful or not) resets the Cooldown timer for the current Trigger.|
|Allowed Values:|`true`<br>`false`|
|Compatible Types:|`All`|
|Multiple Tag Allowed:|No|

<!--CommandReceiveCode  -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|CommandReceiveCode|
|:----|:----|
|Tag Format:|`[CommandReceiveCode:Value]`|
|Description:|Specifies a code that must be received via Antenna Broadcast (codes are sent via Action Profiles) before the Trigger can be activated.|
|Allowed Values:|Any string text excluding `:`, `[`, `]`|
|Compatible Types:|`CommandReceived`|
|Multiple Tag Allowed:|No|

<!--SensorName-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|SensorName|
|:----|:----|
|Tag Format:|`[SensorName:Value]`|
|Description:|Specifies the name of a Sensor Block that is used for triggers that activate using sensors.|
|Allowed Values:|Any string text excluding `:`, `[`, `]`|
|Compatible Types:|`SensorActive`<br />`SensorIdle`|
|Multiple Tag Allowed:|No|

<!--DespawnTypeFromSpawner-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|DespawnTypeFromSpawner|
|:----|:----|
|Tag Format:|`[DespawnTypeFromSpawner:Value]`|
|Description:|Specifies the type of Despawn Request from the Modular Encounters Spawner required to activate the trigger.|
|Allowed Values:|`Any`<br />`PathEnd`<br />`CleanUp`|
|Compatible Types:|`DespawnMES`|
|Multiple Tag Allowed:|No|
<!--  -->

<!--WeatherTypes-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|WeatherTypes|
|:----|:----|
|Tag Format:|`[WeatherTypes:Value]`|
|Description:|This tag specifies the types of Weather that are allowed to activate a Trigger using the `Weather` type.|
|Allowed Values:|Any Weather SubtypeId|
|Compatible Types:|`Weather`|
|Multiple Tag Allowed:|Yes|

<!--ToggleWithTriggerProfile-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ToggleWithTriggerProfile|
|:----|:----|
|Tag Format:|`[ToggleWithTriggerProfile:Value]`|
|Description:|Specifies the name of another attached trigger profile that will have its `UseTrigger` value turned on when this trigger activates. The `UseTrigger` value of this trigger is simultanously turned off.|
|Allowed Values:|Any Trigger Profile SubtypeId|
|Compatible Types:|`All`|
|Multiple Tag Allowed:|No|

<!--ToggledProfileResetsCooldown-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ToggledProfileResetsCooldown|
|:----|:----|
|Tag Format:|`[ToggledProfileResetsCooldown:Value]`|
|Description:|Specifies if the trigger that is enabled while using `ToggleWithTriggerProfile` should have its cooldown timer reset at the same time.|
|Allowed Values:|`true`<br>`false`|
|Compatible Types:|`All`|
|Multiple Tag Allowed:|No|

<!--UseFailCondition-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|UseFailCondition|
|:----|:----|
|Tag Format:|`[UseFailCondition:Value]`|
|Description:|Specifies if the trigger should instead activate only when its `Type` condition (any any attached Condition Profiles) do not pass their checks. This does not apply to the trigger Cooldown as a fail condition.|
|Allowed Values:|`true`<br>`false`|
|Compatible Types:|`All`|
|Multiple Tag Allowed:|No|

<!--UseElseActions-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|UseElseActions|
|:----|:----|
|Tag Format:|`[UseElseActions:Value]`|
|Description:|Specifies if the trigger should instead execute a separate set of Actions when its `Type` condition (any any attached Condition Profiles) do not pass their checks. This does not apply to the trigger Cooldown as a fail condition.|
|Allowed Values:|`true`<br>`false`|
|Compatible Types:|`All`|
|Multiple Tag Allowed:|No|

<!--ElseActions-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ElseActions|
|:----|:----|
|Tag Format:|`[Actions:Value]`|
|Description:|This tag specifies which Action Profiles will be executed when the Trigger Profile conditions are NOT satisfied if also using the `UseElseActions` tag.|
|Allowed Values:|Any Action Profile SubtypeId|
|Compatible Types:|`All`|
|Multiple Tag Allowed:|Yes|

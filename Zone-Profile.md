Zones (formerly Territories) are pre-defined locations in the game world that can be used to control what encounters are allowed to spawn and when. Zone Profiles do not attach to SpawnGroups or any other profile.

Here is an example of how a Zone is defined:

```
<?xml version="1.0"?>
<Definitions xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <EntityComponents>

    <EntityComponent xsi:type="MyObjectBuilder_InventoryComponentDefinition">
      <Id>
        <TypeId>Inventory</TypeId>
        <SubtypeId>MES-Zone-PirateZone</SubtypeId>
      </Id>
      <Description>

        [MES Zone]

        [PublicName:Pirate Space]

        [Active:true]
        [Persistent:true]
        [Strict:true]

        [Coordinates:{X:1 Y:1 Z:1}]
        [Radius:25000]

      </Description>

    </EntityComponent>
    
  </EntityComponents>
</Definitions>
```

Below are the types of tags you can include in your Zone Profile:

<!--Active-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Active|
|:----|:----|
|Tag Format:|`[Active:Value]`|
|Description:|This tag specifies if the Zone should be active in the game world or not.|
|Allowed Values:|`true`<br>`false`|
|Default Value(s):|`false`|
|Multiple Tag Allowed:|No|

<!--Persistent-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Persistent|
|:----|:----|
|Tag Format:|`[Persistent:Value]`|
|Description:|This tag determines if a Zone should persist in the game world between saves, reloads, etc.|
|Allowed Values:|`true`<br>`false`|
|Default Value(s):|`false`|
|Multiple Tag Allowed:|No|

<!--Strict-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Strict|
|:----|:----|
|Tag Format:|`[Strict:Value]`|
|Description:|This tag determines if encounters must be able to spawn in this zone in order to spawn at all.|
|Allowed Values:|`true`<br>`false`|
|Default Value(s):|`false`|
|Multiple Tag Allowed:|No|

<!--NoSpawnZone-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|NoSpawnZone|
|:----|:----|
|Tag Format:|`[NoSpawnZone:Value]`|
|Description:|This tag determines if the Zone should be considered a No Spawn Zone, preventing any type of encounter from spawning.|
|Allowed Values:|`true`<br>`false`|
|Default Value(s):|`false`|
|Multiple Tag Allowed:|No|

<!--PublicName-->


<!--UseLimitedFactions-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|UseLimitedFactions|
|:----|:----|
|Tag Format:|`[UseLimitedFactions:Value]`|
|Description:|This tag determines if the Zone should only allow encounters from certain factions to spawn within it.|
|Allowed Values:|`true`<br>`false`|
|Default Value(s):|`false`|
|Multiple Tag Allowed:|No|

<!--Factions-->


<!--Coordinates-->


<!--Radius-->


<!--PlanetaryZone-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|PlanetaryZone|
|:----|:----|
|Tag Format:|`[PlanetaryZone:Value]`|
|Description:|This tag determines if a zone should be dynamically calculated based on provided planetary details.|
|Allowed Values:|`true`<br>`false`|
|Default Value(s):|`false`|
|Multiple Tag Allowed:|No|

<!--PlanetName-->


<!--Direction-->


<!--HeightOffset-->


<!--ScaleZoneRadiusWithPlanet NOT YET-->


<!--IntendedPlanetSize NOT YET-->

<!--UseAllowedSpawnGroups-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|UseAllowedSpawnGroups|
|:----|:----|
|Tag Format:|`[UseAllowedSpawnGroups:Value]`|
|Description:|This tag determines if only a list of specific SpawnGroups should be allowed to spawn in this Zone.|
|Allowed Values:|`true`<br>`false`|
|Default Value(s):|`false`|
|Multiple Tag Allowed:|No|

<!--AllowedSpawnGroups-->


<!--UseRestrictedSpawnGroups-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|UseRestrictedSpawnGroups|
|:----|:----|
|Tag Format:|`[UseRestrictedSpawnGroups:Value]`|
|Description:|This tag determines if certain SpawnGroups should not be allowed to spawn while in this Zone.|
|Allowed Values:|`true`<br>`false`|
|Default Value(s):|`false`|
|Multiple Tag Allowed:|No|

<!--RestrictedSpawnGroups-->


<!--UseAllowedModIDs-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|UseAllowedModIDs|
|:----|:----|
|Tag Format:|`[UseAllowedModIDs:Value]`|
|Description:|This tag determines if only SpawnGroups belonging to certain Mod IDs are allowed to spawn in this Zone.|
|Allowed Values:|`true`<br>`false`|
|Default Value(s):|`false`|
|Multiple Tag Allowed:|No|

<!--AllowedModIDs-->


<!--UseRestrictedModIDs-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|UseRestrictedModIDs|
|:----|:----|
|Tag Format:|`[UseRestrictedModIDs:Value]`|
|Description:|This tag determines if SpawnGroups belonging to certain Mod IDs should not be allowed to spawn in this Zone.|
|Allowed Values:|`true`<br>`false`|
|Default Value(s):|`false`|
|Multiple Tag Allowed:|No|

<!--RestrictedModIDs-->


<!--UseZoneAnnounce-->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|UseZoneAnnounce|
|:----|:----|
|Tag Format:|`[UseZoneAnnounce:Value]`|
|Description:|This tag determines if players should receive an alert if they enter or leave this Zone.|
|Allowed Values:|`true`<br>`false`|
|Default Value(s):|`false`|
|Multiple Tag Allowed:|No|

<!--ZoneEnterAnnounce-->


<!--ZoneLeaveAnnounce-->


<!--FlashZoneRadius NOT YET-->


<!--XXX-->


<!--XXX-->


<!--XXX-->


<!--XXX-->


<!--XXX-->


<!--XXX-->


<!--XXX-->


<!--XXX-->


<!--XXX-->


<!--XXX-->


<!--XXX-->


<!--XXX-->


<!--XXX-->


<!--XXX-->


<!--XXX-->


<!--XXX-->


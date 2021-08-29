Loot Profiles in the Modular Encounter Systems mod allow you to define rules for how Cargo Containers on your NPC Grids are assigned a Container Type definition. These profiles are attached to `Manipulation` profiles.

Here is an example of how a Loot Profile is setup:

```
<?xml version="1.0"?>
<Definitions xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <EntityComponents>

    <EntityComponent xsi:type="MyObjectBuilder_InventoryComponentDefinition">
      <Id>
          <TypeId>Inventory</TypeId>
          <SubtypeId>MES-ExampleLoot</SubtypeId>
      </Id>
      <Description>

      [MES Loot]
      [ContainerBlockTypes:MyObjectBuilder_CargoContainer/LargeBlockSmallContainer]
      [ContainerTypes:SomeContainerTypeId]
      [MinBlocks:2]
      [MaxBlocks:4]
      [AppendNameToBlock:true]
      [AppendedName: (Loot)]
      
      </Description>
      
    </EntityComponent>

  </EntityComponents>
</Definitions>
```

It's worth noting that these profiles will only target Cargo blocks that do not have a ContainerType already defined, so if you've already defined them manually, then those blocks will be unchanged.

Below you can find all the tags that can be used in your Loot Profile:

<!-- ContainerBlockTypes -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ContainerBlockTypes|
|:----|:----|
|Tag Format:|`[ContainerBlockTypes:Value]`|
|Description:|This tag specifies the types of Cargo Container Blocks that should be targeted by the Loot Profile.|
|Allowed Values:|Any block MyDefinitionId<br />eg: `MyObjectBuilder_CargoContainer/LargeBlockSmallContainer`|
|Multiple Tag Allowed:|Yes|

<!-- ContainerTypes -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|ContainerTypes|
|:----|:----|
|Tag Format:|`[ContainerTypes:Value]`|
|Description:|This tag specifies the name(s) of the ContainerType definitions that you want to apply to your cargo containers. If you provide multiple values, then each time a ContainerType is assigned, it will do so by picking 1 at random from the list you have provided.|
|Allowed Values:|Any ContainerType SubtypeId|
|Multiple Tag Allowed:|Yes|

<!-- MinBlocks -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|MinBlocks|
|:----|:----|
|Tag Format:|`[MinBlocks:Value]`|
|Description:|This tag specifies the minimum number of Cargo Blocks that will be targeted by the Loot Profile.|
|Allowed Values:|Any Integer Greater Or Equal To `0`<br />Value must be less than `MaxBlocks `|
|Multiple Tag Allowed:|No|

<!-- MaxBlocks -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|MaxBlocks|
|:----|:----|
|Tag Format:|`[MaxBlocks:Value]`|
|Description:|This tag specifies the maximum number of Cargo Blocks that will be targeted by the Loot Profile.|
|Allowed Values:|Any Integer Greater Or Equal To `0`<br />Value must be greater than `MinBlocks`|
|Multiple Tag Allowed:|No|

<!-- AppendNameToBlock -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|AppendNameToBlock|
|:----|:----|
|Tag Format:|`[AppendNameToBlock:Value]`|
|Description:|This tag specifies if additional text should be added to the end of the names of cargo blocks that are modified by this Loot Profile.|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|No|

<!-- AppendedName -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|AppendedName|
|:----|:----|
|Tag Format:|`[AppendedName:Value]`|
|Description:|This tag specifies the name that is appended to the end of cargo block names if `AppendNameToBlock` is `true`|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|No|

<!-- MatchBlocksContainingName -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|MatchBlocksContainingName |
|:----|:----|
|Tag Format:|`[MatchBlocksContainingName:Value]`|
|Description:|This tag specifies if the Loot Profile should be restricted to Cargo Blocks that partially or fully match the block name given in the `MatchedName` tag.|
|Allowed Values:|`true`<br>`false`|
|Multiple Tag Allowed:|No|

<!-- MatchedName -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|MatchedName |
|:----|:----|
|Tag Format:|`[MatchedName:Value]`|
|Description:|This tag specifies the partial or full name of the block that must be matched for it to be eligible for use by this profile.|
|Allowed Values:|Any Block Name|
|Multiple Tag Allowed:|No|

<!-- Chance -->
|Tag:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Chance|
|:----|:----|
|Tag Format:|`[Chance:Value]`|
|Description:|This tag specifies the chance (out of 100) that this profile will be used.|
|Allowed Values:|Any Integer Between `0 - 100`|
|Multiple Tag Allowed:|No|

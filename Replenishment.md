Replenishment profiles in the Modular Encounter Systems mod allow you to define rules for how grids inventories will be treated while using the `[ReplenishSystems:true]` tag in your SpawnGroups. With these profiles, you can define limits for certain item types to prevent overfilling of resources like fuel or ammo.

Here is an example of how a Replenishment Profile is setup:

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
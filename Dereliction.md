Dereliction Profiles allow you to apply block degradation to selected blocks to achieve a 'derelict' appearance on grids. Dereliction profiles are attached to `Manipulation` profiles.

Here is an example of how a Dereliction Profile is setup:

```
<?xml version="1.0"?>
<Definitions xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <EntityComponents>

    <EntityComponent xsi:type="MyObjectBuilder_InventoryComponentDefinition">
      <Id>
          <TypeId>Inventory</TypeId>
          <SubtypeId>MES-ExampleDereliction</SubtypeId>
      </Id>
      <Description>

      [MES Dereliction]
      
      </Description>
      
    </EntityComponent>

  </EntityComponents>
</Definitions>
```

These profiles attach to Manipulation Profiles using the `[DerelictionProfiles:YourDerelictionProfileIdHere]` tag.

[The rest of this section is under constuction]
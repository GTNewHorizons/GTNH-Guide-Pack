---
item_ids:
  - gregtech:gt.blockmachines:15313
  - gregtech:gt.blockmachines:15443
  - gregtech:gt.blockmachines:15447
  - gregtech:gt.blockmachines:15442
  - gregtech:gt.blockmachines:15446
bindings:
  - {type: "betterquesting", id: "AAAAAAAAAAAAAAAAAAAKbw=="}
navigation:
  title: Data Bank
  parent: ./multiblocks_index.md
  icon: gregtech:gt.blockmachines:15313
  position: -7001
---
# Data Bank
<GameScene interactive={true} wrap="square" align="right" width="220" height="200">
  <ImportStructureLib controller="gregtech:gt.blockmachines:15313" />
</GameScene>

The <ItemLink id="gregtech:gt.blockmachines:15313" showIcon="left" /> is a ZPM tier multiblock for sharing data sticks with [<ItemLink id="gregtech:gt.blockmachines:1170" showIcon="left" />](./assembly_line.md) through <ItemLink id="gregtech:gt.blockmachines:15470" showIcon="left" /> and <ItemLink id="gregtech:gt.blockmachines:15442" showIcon="left" />. 

The basic structure of the Data Bank supports up to 14 data access hatches or 224 data sticks, and by daisy-chaining, a Data Bank Network can provide an infinite amount of recipe data across multiple assembly lines. Given the number of assembly line recipes in GTNH, the Data Bank is practically mandatory for progression and saves from having to scan any item more than once. The only cost is a power requirement that scales with the number of data access hatches and data bank transmission connectors.

<Template name="properties" 
  tier="ZPM"
  size="3x5x3"
  power="any"
  oc="none"
  reqMaintenance
/>

## Crafting and Construction
### Crafting
<RecipesFor id="gregtech:gt.blockmachines:15313" handlerId="gt.recipe.fakeAssemblylineProcess" />

<RecipesFor id="tectech:gt.blockcasingsTT:2" />

<RecipesFor id="tectech:gt.blockcasingsTT" />

<RecipesFor id="tectech:gt.blockcasingsTT:1" handlerId="gt.recipe.assembler" />

### Structure

The Data Bank is surrounded on either side with heat vents. There is no mandatory air surrounding them. Multi-amp and laser energy hatches are supported although not really necessary because the maximum power usage is fixed, and increasing power beyond it doesn't give any benefits. 

The Data Bank can be rotated or flipped.

Use the <ItemLink id="structurelib:item.structurelib.constructableTrigger" showIcon="left" /> to visualize/build the structure.

Unique to the Data Bank is the <ItemLink id="gregtech:gt.blockmachines:15443" showIcon="left" /> which is effectively an optical transmission connector that shares data stick information instead of computation. The information travels through optical fiber cable to an <ItemLink id="gregtech:gt.blockmachines:15442" showIcon="left" /> on an [<ItemLink id="gregtech:gt.blockmachines:1170" showIcon="left" />](./assembly_line.md), or another Data Bank for daisy-chaining. The cables and hatches must be painted to connect and only one pair of hatches are allowed on the same set of cables.

| Component | Quantity and placement |
| --- | --- |
| <ItemLink id="gregtech:gt.blockmachines:15313" showIcon="left" /> | 1, Front center, 2nd layer |
| <ItemLink id="tectech:gt.blockcasingsTT:2" showIcon="left" /> | 18, Surrounds either side of the machine |
| <ItemLink id="tectech:gt.blockcasingsTT" showIcon="left" /> | 0-6, Around Controller |
| <ItemLink id="tectech:gt.blockcasingsTT:1" showIcon="left" /> | 3-16 |
| <ItemImage id="gregtech:gt.blockmachines:15443" /><Tooltip label="Data Bank Transmission Connector">Normal or Wireless</Tooltip> | 1+, Can replace any outer <ItemLink id="tectech:gt.blockcasingsTT:1" showIcon="left" /> | 
| <ItemImage id="gregtech:gt.blockmachines:15442" /><Tooltip label="Assembly Line Reception Connector">Normal or Wireless</Tooltip> | 0+, Can replace any outer <ItemLink id="tectech:gt.blockcasingsTT:1" showIcon="left" /> | 
| [<ItemImage id="gregtech:gt.blockmachines:145" noTooltip />Data Access Hatch](./assembly_line.md#data-access-hatches) | 1+, Can replace any outer <ItemLink id="tectech:gt.blockcasingsTT:1" showIcon="left" /> |
| <ItemImage id="gregtech:gt.blockmachines:41" noTooltip /><Tooltip label="Energy Hatch">Can use Regular, Multi-Amp, Laser</Tooltip> | 1+, Can replace any <ItemLink id="tectech:gt.blockcasingsTT" showIcon="left" /> |
| <ItemImage id="gregtech:gt.blockmachines:90" noTooltip />Maintenance Hatch | 1+, Can replace any <ItemLink id="tectech:gt.blockcasingsTT" showIcon="left" /> |

### Wallsharing

Data Banks may wallshare each of their sides to save on casings and hatches. However, that does not include data bank transmission connectors because that does NOT properly concatenate the data--one set of data sticks overwrites the other. Assembly line reception connectors are perfectly fine to share for splitting data.


## Usage
Start by adding data access hatches to the Data Bank and fill them with scanned data sticks, or those containing recipes from a [<ItemLink id="gregtech:gt.blockmachines:15331" showIcon="left" />](./research_station.md).

Next, add a data bank transmission connector to the structure to share ALL contained data through optical fiber cable to an assembly line reception connector. Again, the cables must be painted to connect and only one pair of hatches are allowed on a set of cables. However, a Data Bank can have multiple data bank transmission connectors to service multiple [<ItemLink id="gregtech:gt.blockmachines:1170" showIcon="left" />](./assembly_line.md)s simultaneously.

The power consumption of a Data Bank depends on both the number and type of hatches built into the structure. If there are NO assembly line reception connectors then it follows the "Master" equation below. If there are ANY assembly line reception connectors then it follows the "Slave" equation below and they are counted as data access hatches.
<Latex formula="\text{EU/t}=(1 + \text{Data Access Hatches(+ Reception)} \times \text{Transmission Connectors}) \times \begin{cases} 2048, & \text{Master} \\ 32768, & \text{Slave} \end{cases}" scale="0.6" />

| Data Bank | Purpose |: Hatches :||| Power Consumption | Amps |
| --- | --- | --- | --- | --- | --- | --- |
| ^^ | ^^ | Data Access | Reception | Transmission | ^^ | ^^ |
| Master | General | 14 | 0 | 1 | 30,720 EU/t | 0.23A ZPM |
| Master | General | 8 | 0 | 7 | 116,736 EU/t | 0.89A ZPM |
| Slave | Concatenating | 13 | 1 | 1 | 491,520 EU/t | 3.75A ZPM |
| Slave | Splitting | 0 | 1 | 8 | 294,912 EU/t | 2.25A ZPM |

> [!TIP]
> In the early stages of ZPM, there may not always be enough power to keep the Data Bank running. In this case, you can save power by using [covers](/misc/covers.md) to detect [<ItemLink id="gregtech:gt.blockmachines:1170" showIcon="left" />](./assembly_line.md)'s state, and turn the Data Bank on by using a [<ItemLink id="gregtech:gt.metaitem.01:32730" showIcon="left" />](/misc/covers.md#machine-controller) to make the Data Bank draw power only when the Assembly Line requires recipes to operate.

### Daisy-Chaining
Eventually, more than 224 data sticks AND more than just a few [<ItemLink id="gregtech:gt.blockmachines:1170" showIcon="left" />](./assembly_line.md)s are going to be needed. The solution is daisy-chaining Data Banks to share any number of data sticks with any number of Assembly Lines.

Check the example game scene below for more details.
<GameScene width="450" height="300">
  <ImportStructure 
    name="concat_bank_1" 
    src="/assets/structures/multiblocks/data_bank/concat_bank.snbt" 
    offsetY="2"
  />
  <ImportStructure 
    name="concat_bank_2" 
    src="/assets/structures/multiblocks/data_bank/concat_bank.snbt" 
    offsetY="2"
    offsetZ="4"
  />
  <ImportStructure 
    name="splitting_bank_1" 
    src="/assets/structures/multiblocks/data_bank/splitting_bank.snbt" 
    offsetZ="8"
  />
  <ImportStructure 
    name="splitting_bank_2" 
    src="/assets/structures/multiblocks/data_bank/splitting_bank.snbt" 
    offsetZ="12"
  />
  <ImportPonder src="/assets/ponders/multiblocks/data_bank/daisy_chaining.json" />
</GameScene>

### Wireless Hatches
The <ItemLink id="gregtech:gt.blockmachines:15447" showIcon="left" /> and <ItemLink id="gregtech:gt.blockmachines:15446" showIcon="left" /> are both unlocked in UEV. They are N:M hatches (which can completely eliminate daisy-chaining) for sharing data across any distance without any optical fiber cable, although a single transmission connector is all that is needed for any number of [<ItemLink id="gregtech:gt.blockmachines:1170" showIcon="left" />](./assembly_line.md).

## References
- [GTNH Wiki : Data Bank](https://wiki.gtnewhorizons.com/wiki/Data_Bank)

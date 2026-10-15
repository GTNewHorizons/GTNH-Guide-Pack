---
item_ids:
  - gregtech:gt.blockmachines:15300
quest_ids:
  - AAAAAAAAAAAAAAAAAAAKqw==
  - AAAAAAAAAAAAAAAAAAAKqg==
navigation:
  title: Active Transformer
  parent: ./multiblocks_index.md
  icon: gregtech:gt.blockmachines:15300
  position: -7001
---

# Active Transformer

<GameScene interactive={true} wrap="square" align="right" width="220" height="200">
  <ImportStructureLib controller="gregtech:gt.blockmachines:15300" />
</GameScene>

The <ItemLink id="gregtech:gt.blockmachines:15300" showIcon="left" /> (AT) is a ZPM-tier multiblock for transforming power from any voltage tier to any other voltage tier with virtually unlimited amperage throughput. 

The AT is a direct upgrade from singleblock transformers and buck converters because it supports multi-amp and laser energy/dynamo hatches, can change input/output volatage without creating new machine, and supports multiple input/outputs with different voltages. 

The only downside is that there is a 0.004% power loss for all EU that passes through the machine. 

| Property | Details |
| --- | --- |
| Unlock tier | ZPM |
| Structure size | 3×3×3 |
| Power | Any Energy Hatches + Dynamo Hatches are allowed, include Multi-Amp and Laser Hatches. |
| Maintenance and pollution | No pollution, nor the maintenence needed. |


## Crafting and Construction

### Crafting
<RecipesFor id="gregtech:gt.blockmachines:15300" handlerId="gt.recipe.assembler"/>

<RecipesFor id="tectech:gt.blockcasingsTT" handlerId="gt.recipe.assembler" />

The AT consists of a single type of casing around a <ItemLink id="gregtech:gt.blockcasings:15" showIcon="left" />(You can press <KeyBind id="nei.options.keys.recipe.recipe" /> while hover mouse over Item link to see the recipes for this). Place the controller on the center of any faces, and fill with Energy/Dynamo Hatches for energy I/O.

### Structure

| Component | Quantity and placement |
| --- | --- |
| <ItemLink id="gregtech:gt.blockmachines:15300" showIcon="left" /> | 1, at center of any faces. |
| <ItemLink id="tectech:gt.blockcasingsTT" showIcon="left" /> | 5-24 |
| <ItemImage id="gregtech:gt.blockmachines:41" noTooltip /><Tooltip label="Energy Hatch">Can use Regular, Multi-Amp, Laser</Tooltip> | 1+, Any casing. |
| <ItemImage id="gregtech:gt.blockmachines:31" noTooltip /><Tooltip label="Dynamo Hatch">Can use Regular, Multi-Amp, Laser</Tooltip> | 0+, Any casing. |

### Wallsharing

ATs may wallshare each of their sides to save on casings and even split power. At full throughput, the input EU/t is divided evenly between ATs sharing the same energy hatch or laser target hatch. If one is full or no longer consumes power then the difference is split amongst the remaining ATs.

## Usage
The AT receives power from Energy Hatches and outputs power via Dynamo Hatches, similar to the [<ItemLink id="gregtech:gt.blockmachines:13106" showIcon="left" />](./lapotronic_supercapacitor.md). The voltage and amperage does NOT matter. 

This means that your input/output voltage and amperage are entirely influenced only by the Energy/Dynamo Hatches’ voltage and maximum amperage, and that no exceed power is voided or new power is generated.

Since ATs can have multiple inputs and outputs, they can integrate multiple power supplies into a single unit or distribute integrated power across multiple machines through several Dynamo Hatches or Laser Source Hatches.

In particular, since <ItemLink id="gregtech:gt.blockmachines:15466" showIcon="left" /> cannot be used until UHV+, AT is primarily used to adjust the direction of the laser power grid.

## References
- [GTNH Wiki: Active Transformer](https://wiki.gtnewhorizons.com/wiki/Active_Transformer)

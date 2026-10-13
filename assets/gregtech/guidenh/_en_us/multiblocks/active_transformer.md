---
item_ids:
  - gregtech:gt.blockmachines:15300
navigation:
  title: Active Transformer
  parent: ./multiblocks_index.md
  icon: gregtech:gt.blockmachines:15300
  position: -7001
---

# Active Transformer

<GameScene interactive={true} wrap="square" align="right" width="320" height="300">
  <ImportStructureLib controller="gregtech:gt.blockmachines:15300" />
</GameScene>

The <ItemLink id="gregtech:gt.blockmachines:15300" showIcon="left" /> (AT) is a ZPM-tier multiblock for transforming power from any voltage tier to any other voltage tier with virtually unlimited amperage throughput. 

The AT is a direct upgrade from singleblock transformers and buck converters because it supports multi-amp and laser energy/dynamo hatches. 

The only downside is that there is a 0.004% power loss for all EU that passes through the machine. 

The AT is primarily used for routing lasers to mega multiblocks and around a base. Use <ItemLink id="gregtech:gt.blockmachines:15466" showIcon="left" /> in UHV+ to freely change their direction without having to build additional AT.


| Property | Details |
| --- | --- |
| Unlock tier | ZPM |
| Structure size | 3×3×3 |
| Power | Any Energy Hatches + Dynamo Hatches are allowed, include Multi-Amp and Laser Hatches. |
| Maintenance and pollution | No pollution, nor the maintenence needed. |


## Crafting and Construction

### Crafting

The current recipes for the controller and High Power Casing are shown below.

<RecipesFor id="gregtech:gt.blockmachines:15300" />

<RecipesFor id="tectech:gt.blockcasingsTT" />

The AT consists of a single type of casing around a <ItemLink id="gregtech:gt.blockcasings:15" showIcon="left" />. Place the controller on the center of any faces, and fill with Energy/Dynamo Hatches for energy I/O.

### Structure

| Component | Quantity and placement |
| --- | --- |
| <ItemLink id="gregtech:gt.blockmachines:15300" showIcon="left" /> | 1, at center of any faces. |
| <ItemLink id="tectech:gt.blockcasingsTT" showIcon="left" /> | 5-24 |
| Energy Hatch | 1+, Any casing. |
| Dynamo Hatch | 0+, Any casing. |

### Wallsharing

ATs may wallshare each of their sides to save on casings and even split power. At full throughput, the input EU/t is divided evenly between ATs sharing the same energy hatch or laser target hatch. If one is full or no longer consumes power then the difference is split amongst the remaining ATs.

## Usage
The AT receives power from Energy Hatches and outputs power via Dynamo Hatches, similar to the [<ItemLink id="gregtech:gt.blockmachines:13106" showIcon="left" />](./lapotronic_supercapacitor.md). The voltage and amperage does NOT matter. 

For example, an AT can have one 16,384A UEV laser target hatch as input and sixteen 1,024A UV laser source hatches as output. Excess power is neither consumed nor voided. 

However, there is a 0.004% power loss for all EU that passes through the machine, which is practically negligible except when the demand/consumption is 100% of the total input. Don't forget that there is also a max amperage/s power loss for each laser source hatch.

The AT is very forgiving when it comes to hot-swapping components. The machine does NOT explode and even provides a grace period of at least 60 seconds before the structure unforms. However, breaking energy hatches voids any power stored in their buffer.

## References
- [GTNH Wiki: Active Transformer](https://wiki.gtnewhorizons.com/wiki/Active_Transformer)

---
item_ids:
  - gregtech:gt.blockmachines:31021
quest_ids:
  - AAAAAAAAAAAAAAAAAAALzw==
  - AAAAAAAAAAAAAAAAAAAMQQ==
navigation:
  title: Dangote Distillus
  parent: ./multiblocks_index.md
  icon: gregtech:gt.blockmachines:31021
  position: -5001
---
# Dangote Distillus
<GameScene interactive={true} wrap="square" align="right" width="220" height="200">
  <ImportStructureLib controller="gregtech:gt.blockmachines:31021" />
</GameScene>

The <ItemLink id="gregtech:gt.blockmachines:31021" showIcon="left" /> is an IV tier multiblock for distilling fluids into its constituent fractions simultaneously. 

The Dangote is a direct upgrade from the [<ItemLink id="gregtech:gt.blockmachines:1126" showIcon="left" />](./distillation_tower.md) because it runs at 300% speed and offers a fixed 12 parallels.  
The other option to upgrade the Distillation Tower is the [<ItemLink id="gregtech:gt.blockmachines:15516" showIcon="left" />](./mega_distillation_tower.md) which supports Multi-Amp and Laser hatches, but it only outperforms the Dangote if it can take full advantage of its 256 parallels (3+ overclocks).

The Dangote also has an alternate distillery mode which operates like [<ItemLink id="gregtech:gt.blockmachines:531" showIcon="left">Singleblock Distillery</ItemLink>](/singleblock/distillery.md). In this mode the Dangote runs at 200% speed, only uses 15% of the EU/t normally required, creates no pollution and offers a huge number of parallels per voltage tier.  

> [!NOTE]
> The Dangote Distillus operates almost the same as [<ItemLink id="gregtech:gt.blockmachines:1126" showIcon="left" />](./distillation_tower.md) and [<ItemLink id="gregtech:gt.blockmachines:531" showIcon="left">Singleblock Distillery</ItemLink>](/singleblock/distillery.md). The only differences are the Dangote's speed bonus and parallels, so this guide mostly explains the Dangote's unique mechanisms rather than how each mode operates.
> 
> If you need detailed information, please check [Distillation Tower Guide](./distillation_tower.md) and [distillery singleblock guide](/singleblock/distillery.md) for how each machine works and when to use.

<Template 
  name="properties" 
  tier="IV" 
  size="3x3x3-12"
  reqMaintenance
  pollution="480" 
  reqMuffler 
/>

## Crafting and Construction
### Crafting

<RecipesFor id="gregtech:gt.blockmachines:31021" />

<RecipesFor id="gregtech:gt.blockcasings4:1" />

### Structure

The Dangote consists of a single type of casing and has no tiered components.  

The only structural difference between the Dangote and the [<ItemLink id="gregtech:gt.blockmachines:1126" showIcon="left" />](./distillation_tower.md) is the addition of the muffler hatch and a much lower minimum casing requirement. Similar to DT, Dangote can't be rotated or flipped.

The height ranges from 3-12 layers depending on the number of outputs in DT mode. Every layer above the first requires at least ONE output hatch, one layer for each of the different output fluids. For example, distilling raw oil yields four different fluids which means the structure must be at least 5 layers tall with an output hatch on layers 2-5.  
Also, the Dangote's height determines its parallels in Distillery mode - increasing the height gives the Dangote more parallels.

Multi-amp and laser energy hatches are not supported, but there can be multiple regular energy hatches for overclocking. 

Use the <ItemLink id="structurelib:item.structurelib.constructableTrigger" showIcon="left" /> to visualize/build the structure with subchannel "height" to specify the total height of the structure.

#### Base Structure (3 layers tall)

| Component | Quantity and placement |
| --- | --- |
| <ItemLink id="gregtech:gt.blockmachines:31021" showIcon="left" /> | 1, Front bottom center |
| <ItemLink id="gregtech:gt.blockcasings4:1" showIcon="left" /> | 7-19 |
| <ItemImage id="gregtech:gt.blockmachines:41" noTooltip /><Tooltip label="Energy Hatch">Only Regular Hatches allowed</Tooltip> | 1+, Can replace any <ItemLink id="gregtech:gt.blockcasings4:1" showIcon="left" /> |
| <ItemImage id="gregtech:gt.blockmachines:90" noTooltip />Maintenance Hatch | 1+, Can replace any <ItemLink id="gregtech:gt.blockcasings4:1" showIcon="left" /> |
| <ItemImage id="gregtech:gt.blockmachines:91" noTooltip />Muffler Hatch | 1, Can replace <ItemLink id="gregtech:gt.blockcasings4:1" showIcon="left" /> at the topmost layer |
| <ItemImage id="gregtech:gt.blockmachines:71" noTooltip />Input Bus | 0+, Can replace <ItemLink id="gregtech:gt.blockcasings4:1" showIcon="left" /> at the 1st layer |
| <ItemImage id="gregtech:gt.blockmachines:51" noTooltip />Input Hatch | 1+, Can replace <ItemLink id="gregtech:gt.blockcasings4:1" showIcon="left" /> at the 1st layer |
| <ItemImage id="gregtech:gt.blockmachines:81" noTooltip />Output Bus | 0+, Can replace <ItemLink id="gregtech:gt.blockcasings4:1" showIcon="left" /> at the 1st layer |
| <ItemImage id="gregtech:gt.blockmachines:61" noTooltip />Output Hatch | 2+, Can replace any <ItemLink id="gregtech:gt.blockcasings4:1" showIcon="left" /> except 1st layer, require at least 1 per layer |

#### Additional layers (maximum height 12)
| Component | Quantity and placement |
| --- | --- |
| <ItemLink id="gregtech:gt.blockcasings4:1" showIcon="left" /> | 7 |
| <ItemImage id="gregtech:gt.blockmachines:61" noTooltip />Output Hatch | 1+, Can replace any <ItemLink id="gregtech:gt.blockcasings4:1" showIcon="left" /> |

<br />

> [!NOTE]
> You should move your Muffler Hatch to the top layer when increasing the height of the Dangote.
> 
> Also, it is possible to move or place additional Energy Hatches or Maintenance Hatches on newly placed layers if you want.

### Wallsharing

Dangotes may wallshare each of their sides to save on casings and buses/hatches. That includes the many output hatches and maintenance hatch. No recipe uses more than 1A of power so it is possible to share one energy hatch between two machines.

<Template name="wallshare_energy_warning" />

## Usage
As mentioned before, the Dangote has two operating modes, listed below. Switch modes in the GUI of the controller (<FloatingImage src="gregtech:textures/gui/overlay_button/machine_mode_distilling.png" wrap="inline" x={0} y={0} w={16} h={16} scaleX={3.0} scaleY={3.0} />/<FloatingImage src="gregtech:textures/gui/overlay_button/machine_mode_tower.png" wrap="inline" x={0} y={0} w={16} h={16} scaleX={3.0} scaleY={3.0} />) or by right-clicking the controller with a screwdriver.

- _Distillation Tower Mode_ - Produces all constituent fractions simultaneously. Runs at 300% speed and offers a fixed 12 parallels. Increase the height to output more fluid types.
- _Distillery Mode_ - Produces only one fraction at a time. Runs at 200% speed, only uses 15% of the EU/t normally required, and offers <Latex formula="2 \times \lfloor \text{Height}/3 \rfloor" scale="0.7" /> parallels per voltage tier, as seen in the following table.

| Height | Parallels vs. Voltage Tier in Distillery Mode |||||||||||||||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ^^ | LV | MV | HV | EV | IV | LuV | ZPM | UV | UHV | UEV | UIV | UMV | UXV | MAX | MAX+ |
| 3 | 2 | 4 | 6 | 8 | 10 | 12 | 14 | 16 | 18 | 20 | 22 | 24 | 26 | 28 | 30 |
| 4 | 2 | 4 | 6 | 8 | 10 | 12 | 14 | 16 | 18 | 20 | 22 | 24 | 26 | 28 | 30 |
| 5 | 2 | 4 | 6 | 8 | 10 | 12 | 14 | 16 | 18 | 20 | 22 | 24 | 26 | 28 | 30 |
| 6 | 4 | 8 | 12 | 16 | 20 | 24 | 28 | 32 | 36 | 40 | 44 | 48 | 52 | 56 | 60 |
| 7 | 4 | 8 | 12 | 16 | 20 | 24 | 28 | 32 | 36 | 40 | 44 | 48 | 52 | 56 | 60 |
| 8 | 4 | 8 | 12 | 16 | 20 | 24 | 28 | 32 | 36 | 40 | 44 | 48 | 52 | 56 | 60 |
| 9 | 6 | 12 | 18 | 24 | 30 | 36 | 42 | 48 | 54 | 60 | 66 | 72 | 78 | 84 | 90 |
| 10 | 6 | 12 | 18 | 24 | 30 | 36 | 42 | 48 | 54 | 60 | 66 | 72 | 78 | 84 | 90 |
| 11 | 6 | 12 | 18 | 24 | 30 | 36 | 42 | 48 | 54 | 60 | 66 | 72 | 78 | 84 | 90 |
| 12 | 8 | 16 | 24 | 32 | 40 | 48 | 56 | 64 | 72 | 80 | 88 | 96 | 104 | 112 | 120 |

## References
- [GTNH Wiki : Dangote Distillus](https://wiki.gtnewhorizons.com/wiki/Dangote_Distillus)

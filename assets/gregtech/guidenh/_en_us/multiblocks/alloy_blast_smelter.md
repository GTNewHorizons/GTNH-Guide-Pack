---
item_ids:
  - gregtech:gt.blockmachines:810
navigation:
  title: Alloy Blast Smelter
  parent: ./multiblocks_index.md
  icon: gregtech:gt.blockmachines:810
  position: -5001
quest_ids:
  - AAAAAAAAAAAAAAAAAAAFiA==
---

# Alloy Blast Smelter

<GameScene interactive={true} wrap="square" align="right" width="320" height="300">
  <ImportStructureLib controller="gregtech:gt.blockmachines:810" />
</GameScene>

The Alloy Blast Smelter (ABS) is an IV tier multiblock for smelting dusts into molten alloys. Many of the basic alloys can also be made in the [Industrial Mixing Machine](./industrial_mixing_machine.md) and [Zyngen](./zyngen.md), but it is significantly more efficient and faster to smelt them directly in the ABS. Tougher alloys such as indalloy 140 don't even have a choice and must be smelted in the ABS. 

There are no tiered components or any sort of bonuses and there is no tier skipping, even when overclocking with multiple energy hatches. 

The minimum casing requirement is very low to allow for many buses/hatches since there are 12 unique programmed circuits out of the 72 recipes. The ABS is superseded by the [Mega Alloy Blast Smelter](./mega_alloy_blast_smelter.md) in UV.

| Property | Details |
| --- | --- |
| Unlock tier | IV |
| Structure size(LxWxH) | 3x3x4 |
| Power | Regular Energy hatch |
| Overclocks | Imperfect |
| Maintenance and pollution | Requires maintenance, produces 200 gibbi/s pollution, require Muffler Hatch |

## Crafting and Construction

You need controller and casings to form ABS. 
Current recipes for the required controller and casings are listed below.

<RecipesFor id="gregtech:gt.blockmachines:810" />

<RecipesFor id="miscutils:miscutils.blockcasings:14" />

<RecipesFor id="miscutils:miscutils.blockcasings:15" />

| Component | Quantity and placement |
| --- | --- |
| <ItemLink id="gregtech:gt.blockmachines:810" showIcon="left" /> | 1, Front Bottom Center |
| <ItemLink id="miscutils:miscutils.blockcasings:14" showIcon="left" /> | 16, 2nd-3rd layer with a hole in the center  |
| <ItemLink id="miscutils:miscutils.blockcasings:15" showIcon="left" /> | 3-13, Fills 1st and 4th layer  |
| Energy Hatch | 1+, Any <ItemLink id="miscutils:miscutils.blockcasings:15" showIcon="left" /> |
| Maintenance Hatch | 1, Any <ItemLink id="miscutils:miscutils.blockcasings:15" showIcon="left" /> |
| Muffler Hatch | 1, Any <ItemLink id="miscutils:miscutils.blockcasings:15" showIcon="left" /> |
| Input Bus | 1+, Any <ItemLink id="miscutils:miscutils.blockcasings:15" showIcon="left" /> |
| Input Hatch | 0+, Any <ItemLink id="miscutils:miscutils.blockcasings:15" showIcon="left" /> |
| Output Hatch | 1+, <ItemLink id="miscutils:miscutils.blockcasings:15" showIcon="left" /> |

### Wallsharing

ABS may wallshare each of their sides to save on casings, coils, and buses/hatches. However, reducing the number of unique input buses may not be very helpful considering the sheer amount of programmed circuits in the recipes.

## Usage

The following tables list all 72 recipes by their voltage tier and programmed circuit (PC). In total, there are 12 unique programmed circuits to be spread out across 8 input buses if the last few are combined. Some are also not very useful until after the [Mega Alloy Blast Smelter](./mega-alloy-blast-smelter.md) is unlocked.

Input separation<FloatingImage src="gregtech:textures/gui/overlay_button/input_separation_on.png" wrap="inline" x={0} y={0} w={48} h={48} /> should be enabled on the ABS to prevent SOLID ingredients in different input buses from being used in the same recipe, including any programmed circuits. That means a single ABS with many input buses can support many different programmed circuits simultaneously. Just don't forget to stay above the minimum number of casing blocks. FLUID ingredients are always shared regardless of input separation, unless the input hatch is colored.

### Recipes organized by Voltage Tier

#### LV

| PC | Molten Alloy | ABS Only |
| -- | ----------------------------------------------- | -------- |
| 2 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1054" /> | No |
| 2 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1033" /> | No |
| 2 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1056" /> | No |
| 3 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1034" /> | No |
| 4 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1079" /> | No |
| 4 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1061" /> | No |
| 4 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1096" /> | No |

#### MV

| PC | Molten Alloy | ABS Only |
| -- | ------------ | -------- |
| 2 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1057" /> | No |
| 2 | <ItemLink id="NotEnoughItems:neiFluidDisplay:346" /> | No |
| 2 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1341" /> | No |
| 3 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1095" /> | No |
| 5 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1035" /> | Yes |
| 5 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1040" /> | No |
| 5 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1041" /> | Yes |
| 5 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1042" /> | Yes |
| 6 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1061" /> | No |
| 7 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1043" /> | Yes |

#### HV

| PC | Molten Alloy | ABS Only |
| -- | ------------ | -------- |
| 2 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1030" /> | No |
| 2 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1031" /> | No |
| 2 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1055" /> | No |
| 2 | <ItemLink id="NotEnoughItems:neiFluidDisplay:624" /> | No |
| 3 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1032" /> | No |
| 4 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1050" /> | No |
| 4 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1036" /> | No |
| 4 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1037" /> | No |
| 4 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1051" /> | No |
| 4 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1045" /> | No |
| 5 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1046" /> | Yes |
| 6 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1047" /> | Yes |

#### EV

| PC | Molten Alloy | ABS Only |
| -- | ------------ | -------- |
| 2 | <ItemLink id="NotEnoughItems:neiFluidDisplay:1065" /> | No |
TODO: Need more writings...

## References

- [GTNH Wiki: Alloy Blast Smelter](https://wiki.gtnewhorizons.com/wiki/Alloy_Blast_Smelter)

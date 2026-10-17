---
item_ids:
  - gregtech:gt.blockmachines:1170
quest_ids:
  - AAAAAAAAAAAAAAAAAAAFhA==
navigation:
  title: Assembly Line
  parent: ./multiblocks_index.md
  icon: gregtech:gt.blockmachines:1170
  position: -5001
---
# Assembly Line

<GameScene interactive={true} wrap="square" align="right" width="320" height="300">
  <ImportStructureLib controller="gregtech:gt.blockmachines:1170" />
</GameScene>

The <ItemLink id="gregtech:gt.blockmachines:1170" showIcon="left" /> (assline or AL) is an IV tier multiblock for crafting LuV+ tier components. 

The machine is built as a series of slices and inputs must be inserted in the exact order in which they appear in NEI. 

Recipes are also NOT implied and must be explicitly shared with the AL via <ItemLink id="gregtech:gt.metaitem.01:32708" showIcon="left" />. This is unlike any multiblock the player has encountered up to this point and requires more advanced techniques for automation. For normal assembler recipes, see the [<ItemLink id="gregtech:gt.blockmachines:32018" showIcon="left" />](./precise_auto_assembler_mt-3662.md). 

The AL is generally superseded by the [<ItemLink id="gregtech:gt.blockmachines:13532" showIcon="left" />](./advanced_assembly_line.md) with its parallel processing and support for multi-amp and laser energy hatches, but it is not recommended to switch right away because the power demand is much higher, the automation is more complex, and it cannot tier skip.

| Property | Details |
| --- | --- |
| Unlock tier | IV |
| Size(LxWxH) | 3 x 5-16 x 4 |
| Power | Regular Energy Hatches |
| Overclocks | Imperfect |
| Maintenance and pollution | Need Maintenance, produces no pollution, and does not need a Muffler Hatch |

## Crafting and Construction

### Crafting

You need the controller and various Assembly Line related casings to form the AL.
Current recipes for the required controller and casings are listed below.

<RecipesFor id="gregtech:gt.blockmachines:1170" handlerBlacklist="gt.recipe.scanner" />

<RecipesFor id="gregtech:gt.blockcasings3:10" />

<RecipesFor id="gregtech:gt.blockcasings2" handlerBlacklist="codechicken.nei.recipe.ShapelessRecipeHandler" />

<RecipesFor id="gregtech:gt.blockcasings2:5" />

<RecipesFor id="gregtech:gt.blockcasings2:9" />

### Structure

The AL is built as a series of slices with an input bus at the bottom center of each one to hold a single unique input. The total number of slices required therefore depends on the total number of inputs in the recipe. For example, the LuV motor has five solid inputs and therefore needs five slices to craft. The order in which the ingredients are inserted is the same order in which they appear in NEI.

The AL can be built left-to-right or right-to-left. The direction only affects the ordering of the input buses. The slice with the controller is always the front and therefore the location of the first input. 

The glass can be any tier and has no effect on the operation of the machine. 

Multi-amp and laser energy hatches are not supported, but there can be multiple regular energy hatches for overclocking. The AL can only tier skip ONE time (ie. IV energy hatches can run up to LuV recipes). 

Use the <ItemLink id="structurelib:item.structurelib.constructableTrigger" showIcon="left" /> to visualize/build the structure with subchannel "glass" to specify the tier of the glass and subchannel "length" to specify the number of slices $$(\text{Slices} = \text{Length} + 4)$$.

The input buses can be any tier but it is recommended to use <ItemLink id="gregtech:gt.blockmachines:70" showIcon="left" /> because their limited capacity(1 slot) is very useful for automation. 

<ItemLink id="gregtech:gt.blockmachines:2711" showIcon="left" /> set to auto-pull and linked input buses do <Color id="red">**NOT**</Color> work if they make more than one item type visible per slice. 

At max length, the output bus should replace a solid steel machine casing on layer 1 of the last slice instead of replacing the final input bus. 

Only four input hatches are required because no recipe uses more than four fluids, and <ItemImage id="gregtech:gt.blockmachines:200" /> Quadruple input hatches do <Color id="red">**NOT**</Color> work, but there can be gaps between the input hatches if necessary.

#### Base Structure (Minimum requirements)
| Component | Quantity and placement |
| --- | --- |
| <ItemLink id="gregtech:gt.blockmachines:1170" showIcon="left" /> | First slice, 3rd layer |
| <ItemImage id="bartworks:BW_TieredGlass" /> Any tiered glass | 10, Both sides of 2nd layer |
| <ItemLink id="gregtech:gt.blockcasings3:10" showIcon="left" /> | 8, Both sides of 3rd layer |
| <ItemLink id="gregtech:gt.blockcasings2" showIcon="left" /> | 4-8, Both sides of 1st layer and center of 4th layer |
| <ItemLink id="gregtech:gt.blockcasings2:5" showIcon="left" /> | 5, Center of 2nd layer |
| <ItemLink id="gregtech:gt.blockcasings2:9" showIcon="left" /> | 5, Center of 3rd layer |
| Energy Hatch | 1+, Any 4th layer Casing |
| Maintenance Hatch | Any 1st layer side casings |
| Data Access Hatch | 1, Any both sides of 3rd layer but <Color id="red">**NOT**</Color> on first slice |
| Input Bus | 5, Center of 1st layer. |
| Input Hatch | 1-4, Any 1st layer side casings |
| Output Bus | 1, Any 1st layer on last slice |

#### Each Additional Slice

<GameScene interactive={true} wrap="square" align="right" width="170" height="130">
  <Block id="gregtech:gt.blockmachines:71" />
  <Block id="gregtech:gt.blockcasings2" x="-1"/>
  <Block id="gregtech:gt.blockcasings2" x="1"/>
  <Block id="gregtech:gt.blockcasings2:5" y="1" />
  <Block id="gregtech:gt.blockglass1:10" y="1" x="-1" />
  <Block id="gregtech:gt.blockglass1:10" y="1" x="1" />
  <Block id="gregtech:gt.blockcasings2:9" y="2" />
  <Block id="gregtech:gt.blockcasings3:10" y="2" x="-1" />
  <Block id="gregtech:gt.blockcasings3:10" y="2" x="1" />
  <Block id="gregtech:gt.blockcasings2" y="3"/>
</GameScene>

Each additional slice (1 length) requires these blocks:

| Component | Quantity and placement |
| --- | --- |
| <ItemImage id="bartworks:BW_TieredGlass" /> Any tiered glass | 2, Both sides of 2nd layer |
| <ItemLink id="gregtech:gt.blockcasings3:10" showIcon="left" /> | 2, Both sides of 3rd layer |
| <ItemLink id="gregtech:gt.blockcasings2" showIcon="left" /> | 3, Both sides of 1st layer and center of 4th layer |
| <ItemLink id="gregtech:gt.blockcasings2:5" showIcon="left" /> | 1, Center of 2nd layer |
| <ItemLink id="gregtech:gt.blockcasings2:9" showIcon="left" /> | 1, Center of 3rd layer |
| Input Bus | 1, Center of 1st layer. |

### Wallshare

ALs may wallshare each of their sides to save on casings, glass, and buses/hatches. That includes any input hatches, maintenance hatches, data access hatches, and output buses. Sharing a data access hatch is particuarly valuable for saving TPS and reducing the amount of data sticks needed

## Usage

### Scanning Recipes

Simply inserting the inputs of a recipe into the AL (and in the correct order) is not enough for the machine to start processing. Recipes must be explicitly shared with the AL via <ItemLink id="gregtech:gt.metaitem.01:32708" showIcon="left" /> scanned with the necessary information in a singleblock scanner.

To scan the recipe for an <ItemLink id="gregtech:gt.metaitem.01:32606" showIcon="left" />, for example, insert both an IV motor and data stick into a scanner, as seen in the recipe below. The output is a data stick specifically for LuV motors and goes in the Data Access Hatch on the AL. The IV motor is consumed in the process. All data stick recipes and the items to scan for them are visible through NEI. Note that recipes may change with updates of GTNH and would require the player to update their data sticks.

<Recipe id="gregtech:gt.metaitem.01:32606" handlerId="gt.recipe.scanner" /> 

Later in the game, the scanner is replaced by the [<ItemLink id="gregtech:gt.blockmachines:15331" showIcon="left" />](./research_station.md) and [<ItemLink id="gregtech:gt.blockmachines:15311" showIcon="left" />](./quantum_computer.md). These two multiblocks work together to unlock the recipes for some of the most advanced items in GTNH.

### Data Access Hatches
There are four types of data access hatches, listed below. There can only be one per AL but they can be safely wallshared between machines.

- <ItemLink id="gregtech:gt.blockmachines:145" showIcon="left" /> - Holds up to four data sticks
- <ItemLink id="gregtech:gt.blockmachines:146" showIcon="left" /> - Holds up to sixteen data sticks
- <ItemLink id="gregtech:gt.blockmachines:147" showIcon="left" /> - Holds up to sixteen data sticks and allows for input/output of data sticks.
- <ItemLink id="gregtech:gt.blockmachines:15442" showIcon="left" /> - Reads any number of data sticks from a [<ItemLink id="gregtech:gt.blockmachines:15313" showIcon="left" />](./data_bank.md).

### Troubleshooting

1. **No Valid Recipe Found.** There are numerous reasons for this error such as missing items, missing fluids, ingredients in the wrong order, more than one output bus, etc. Check that all items are in the correct input bus/hatch.

1. **No Data Sticks Found.** The controller cannot find any data sticks. Either the data access hatch is empty or the data sticks are not scanned with a recipe. Holding shift shows what item the data stick is scanned with, similar to an AE2 pattern.

1. **Recipes keep overlapping.** You likely forgot to either insert a blocking card or enable blocking mode on an interface that stores patterns.


## References

- [GTNH Wiki: Assembly Line](https://wiki.gtnewhorizons.com/wiki/Assembly_Line)

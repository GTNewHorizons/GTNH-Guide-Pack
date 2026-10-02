---
item_ids:
  - gregtech:gt.blockmachines:13532
navigation:
  title: Advanced Assembly Line
  parent: ./multiblocks_index.md
  icon: gregtech:gt.blockmachines:13532
  position: -5001
quest_ids:
  - ZIotzqvnRiKu1_1Hb9i1dg==
---

# Advanced Assembly Line

<GameScene interactive={true} wrap="square" align="right" width="320" height="300">
  <ImportStructureLib controller="gregtech:gt.blockmachines:13532" />
</GameScene>

The <ItemLink id="gregtech:gt.blockmachines:13532" showIcon="left" /> (AAL) is an IV tier multiblock for running Assembly Line recipes in parallel by leveraging item pipelining; ingredients are consumed slice-by-slice instead of all at once, much like a real Assembly Line. That means the maximum number of parallels corresponds to the number of solid ingredients in a recipe. The AAL also supports multi-amp and laser energy hatches for serious overclocking, but CANNOT tier skip like the regular Assembly Line. Overclocks above the named voltage tiers are considered laser overclocks and scale much worse than imperfect overclocks.

Although craftable at the same time as the Assembly Line, it is not recommended to switch right away for multiple reasons. 
1. The AAL is much more complicated than the Assembly Line and is prone to getting stuck if not set up correctly. 
1. Parallelism costs a tremendous amount of power which may be difficult to support without laser infrastructure. 
1. Automation is much more expensive since it requires significantly more AE2 components. 
1. The Assembly Line is still needed for tier skipping.

| Property | Details |
| --- | --- |
| Unlock tier | IV |
| Structure size (LxWxH) | 3x5-16x4 |
| Power | Any Energy Hatches allowed, including Multi-amp and Laser Hatches. |
| Maintenance and pollution | Requires Maintenance, produces no pollution, and does not need a muffler hatch |
| Overclocks | Unique, explained below |

## Crafting and Construction

### Crafting
You need the controller and various Assembly Line related casings to form the AAL.
Current recipes for the required controller and casings are listed below.

<RecipesFor id="gregtech:gt.blockmachines:13532" handlerBlacklist="gt.recipe.scanner" />

<RecipesFor id="gregtech:gt.blockcasings3:10" />

<RecipesFor id="gregtech:gt.blockcasings2" handlerBlacklist="codechicken.nei.recipe.ShapelessRecipeHandler" />

<RecipesFor id="gregtech:gt.blockcasings2:5" />

<RecipesFor id="gregtech:gt.blockcasings2:9" />

### Structure
The only structural difference between the AAL and the Assembly Line is the controller. The glass can be any tier and has no effect on the operation of the machine. Multi-amp and laser energy hatches are supported for serious overclocking, but there is no tier skipping (i.e. UV energy hatches cannot run UHV recipes). Use the Multiblock Structure Hologram Projector to visualize/build the structure with subchannel "glass" to specify the tier of the glass and subchannel "length" to specify the number of slices $$(\text{Slices} = \text{Length} + 4)$$

#### Base Structure (Minimum requirements)
| Component | Quantity and placement |
| --- | --- |
| <ItemLink id="gregtech:gt.blockmachines:13532" showIcon="left" /> | First slice, 3rd layer |
| Any tiered glass | 10, Both sides of 2nd layer |
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
| Any tiered glass | 2, Both sides of 2nd layer |
| <ItemLink id="gregtech:gt.blockcasings3:10" showIcon="left" /> | 2, Both sides of 3rd layer |
| <ItemLink id="gregtech:gt.blockcasings2" showIcon="left" /> | 3, Both sides of 1st layer and center of 4th layer |
| <ItemLink id="gregtech:gt.blockcasings2:5" showIcon="left" /> | 1, Center of 2nd layer |
| <ItemLink id="gregtech:gt.blockcasings2:9" showIcon="left" /> | 1, Center of 3rd layer |
| Input Bus | 1, Center of 1st layer. |

#### Wallsharing

AALs may wallshare each of their sides to save on casings, glass, and buses/hatches. That includes any input hatches, maintenance hatches, data access hatches, and output buses. Sharing a data access hatch is particularly valuable for saving TPS and reducing the amount of Data Banks needed.

## Usage

The AAL starts processing once the contents of the buses/hatches align with a stored data stick, much like the regular [Assembly Line](./assembly_line.md). Every recipe must pass through N slices on the machine, where N is the number of solid ingredients. Each slice takes T = (base duration / N) seconds to process the ONE type of item in its input bus before continuing to the next slice for the next item. This repeats until all ingredients are consumed and the final product is sent to the output bus for retrieval. All fluids are consumed at the very start of processing.

The AAL supports parallel processing by allowing the next recipe to begin once the first slice is done with the first recipe. This creates a staggered pattern that allows every slice to work simultaneously, if there are enough resources available.

If the next slice is missing the required item in its input bus, the current slice enters the STUCK state which halts the entire machine until the missing item is found/returned. The status light on the face of the controller turns orange to indicate that the machine is STUCK. Use WAILA to locate where exactly the problem occurred.

TODO - this is where explain scene required.

### Laser Overclocks

The energy consumption of the AAL is the number of active slices times the base EU/t, similar to parallels. The AAL then runs up to N imperfect overclocks where N is the difference between the voltage tier of the lowest tier energy hatch and the voltage tier of the recipe. Further overclocks are all laser overclocks, which consume more power and scale even worse than an imperfect overclock. The first one is 2x speed for 4.3x the power and each additional one increases the power multiplier by 0.3, scaling infinitely until each slice is only one tick long.

- Imperfect Overclocks - 2x speed for 4.0x power (2/4.0).
- 1st Laser Overclock - 2x speed for 4.3x power (2/4.3).
- 2nd Laser Overclock - 2x speed for 4.6x power (2/4.6).
- 3rd Laser Overclock - 2x speed for 4.9x power (2/4.9).
The increased power cost of laser overclocks means that upgrading the energy hatch(es) is not always going to overclock the machine. It all depends on the recipe's base EU/t and the maximum number of parallels. 

Consider the UIV field generator recipe as an example. There can be up to 14 slices active simultaneously and each one consumes 15/16A of UEV power for a total of 13.1A. That means a 16A UEV energy hatch is enough to cover the base cost of the recipe, but does not grant any laser overclocks. Upgrading to a 64A energy hatch grants one laser overclock because that is greater than 13.1 x 4.3 = 56.4A, but upgrading to a 256A energy hatch does NOT grant a second laser overclock because that is less than 56.4 x 4.6 = 259A. The following table lists the amperage needed for a given number of laser overclocks for on-tier recipes (i.e. UEV recipes with one UEV laser energy hatch) that consume 15/16A of power.


| Slices | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 4 | 64 | 256 | 1,024 | 4,096 | 16,384 | 65,536 | 1,048,576 | 4,194,304 | 
| 5 | 64 | 256 | 1,024 | 4,096 | 16,384 | 262,144 | 1,048,576 | 4,194,304 | 
| 6 | 64 | 256 | 1,024 | 4,096 | 16,384 | 262,144 | 1,048,576 | 4,194,304 |
| 7 | 64 | 256 | 1,024 | 4,096 | 65,536 | 262,144 | 1,048,576 | 4,194,304 | 
| 8 | 64 | 256 | 1,024 | 4,096 | 65,536 | 262,144 | 1,048,576 | 16,777,216 | 
| 9 | 64 | 256 | 1,024 | 16,384 | 65,536 | 262,144 | 1,048,576 | 16,777,216 | 
| 10 | 64 | 256 | 1,024 | 16,384 | 65,536 | 262,144 | 1,048,576 | 16,777,216 | 
| 11 | 64 | 256 | 1,024 | 16,384 | 65,536 | 262,144 | 1,048,576 | 16,777,216 |
| 12 | 64 | 256 | 4,096 | 16,384 | 65,536 | 262,144 | 1,048,576 | 16,777,216 |
| 13 | 64 | 256 | 4,096 | 16,384 | 65,536 | 262,144 | 1,048,576 | 16,777,216 |
| 14 | 64 | 1,024 | 4,096 | 16,384 | 65,536 | 262,144 | 1,048,576 | 16,777,216 |
| 15 | 64 | 1,024 | 4,096 | 16,384 | 65,536 | 262,144 | 1,048,576 | 16,777,216 |
| 16 | 256 | 1,024 | 4,096 | 16,384 | 65,536 | 262,144 | 1,048,576 | 16,777,216 |


## References

- [GTNH Wiki: Advanced Assembly Line](https://wiki.gtnewhorizons.com/wiki/Advanced_Assembly_Line)

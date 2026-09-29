---
navigation:
  title: Breaking Changes
  parent: index.md
  icon: Botania:cosmetic:31
author: Skorched
date: 2026-06-17
---

# Breaking Changes
As with most major updates, a lot of care has been taken to make updating from the previous version as seamless as possible. Unfortunately, to make substantial changes, there will always be some things that cannot easily transfer. This page is designed to highlight some of those issues, so that people updating in existing bases can highlight problems more easily.

## Contents:
[Crop Changes](#crop-changes)
[Titanium Tetrachloride](#titanium-tetrachloride)
[Methane](#methane)
[Cast Iron](#cast-iron)
[Steel Recipes](#steel-recipes)
[Recipe Changes](#recipe-changes)
[Crucible Decay](#crucible-decay)
[Existing Multiblock Changes](#existing-multiblock-changes)
[Tiered Glass](#tiered-glass)

# Crop Changes
This update introduces [CropsNH](./crops/crops.md), a replacement for <Color id="RED">IC2 Crops</Color> designed to alleviate some of the issues it had. As such, there are a few changes to how they operate. Existing IC2 seeds will automatically convert to CropsNH seeds, however many of the seeds will now have either a <Color id="GREEN">"sub-soil"</Color> requirements and/or changes to recipes involving them.

# Titanium Tetrachloride
The recipe for <Color id="GREEN">Titanium Tetrachloride</Color> when using pure titanium dust has changed from being 10 seconds at HV, to 80 seconds at EV. This means that if your line was running on a HV reactor, it will no longer run.

# Methane
The recipe for <Color id="GREEN">Methane</Color> now takes 10 times longer. This is not directly breaking, as it runs at the same tier as previous, however any passive setup will now be more likely to bottleneck around methane.

# Cast Iron
<Color id="RED">Wrought Iron</Color> has been removed, with <Color id="GREEN">Cast Iron</Color> taking its place. It has a different method of making it beyond the "nugget recipe", using carbon to create the alloy. Other than the name and recipe changes, it is effectively a 1:1 replacement in terms of progression.
<RecipeFor id="gregtech:gt.metaitem.01:11304" input="gregtech:gt.metaitem.01:2032"/>

# Steel Recipes
All recipes for steel from iron now require some form of carbon. As an example, in the <Color id="GREEN">Electric Blast Furnace</Color>, you can either use cast iron with oxygen (where the carbon is in the cast iron), or smelt iron dust, carbon, and oxygen together directly.

# Recipe Changes
A wide variety of recipes have been changed, TODO

# Crucible Decay
The decay within a <Color id="GREEN">Crucible</Color> when over the 200 essentia limit is now percentage based. This means that the higher you are over that threshold, the faster that decay will be. This is not a "direct" breaking change, but may limit high-throughput alchemy using a crucible directly.

# Existing Multiblock Changes
Fixing some previous mistakes, a handful of structures have been changed in a minor way to make them symmetrical. This list includes:
- Forge of the Gods
- Antimatter Forge
- Antimatter Generator

# Tiered Glass
All <Color id="GREEN">Glass-Tiered</Color> multis now need the correct glass for the hatch right up to UXV, instead of the previous mechanic of having "caps" at which you unlocked all hatches. This excludes a few structures, such as the <ItemLink id="gregtech:gt.blockmachines:13106" icon="right"/> and the <ItemLink id="gregtech:gt.blockmachines:31150" icon="right"/>. Alongside this change, <ItemLink id="bartworks:BW_GlasBlocks:15" icon="right"/> and <ItemLink id="bartworks:BW_GlasBlocks2" icon="right"/> have been downtiered to UEV and UIV respectively. UMV glass now also requires the <ItemLink id="gregtech:gt.blockmachines:15411" icon="right"/>.

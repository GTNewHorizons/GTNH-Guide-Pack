---
item_ids:
  - gregtech:gt.blockmachines:15754
navigation:
  title: Bose-Einstein Condensate Entanglement Apparatus
  parent: bec.md
  icon: gregtech:gt.blockmachines:15754
categories:
    - New Multiblocks
    - Bose-Einstein Condensate
author: Skorched
date: 2026-06-27
---

# Bose-Einstein Condensate Entanglement Apparatus
<GameScene wrap="square" align="right">
  <ImportStructureLib controller="gregtech:gt.blockmachines:15754" />
</GameScene>
The <Color id="GREEN">Bose-Einstein Condensate Entanglement Apparatus (BECEA)</Color> is a UMV tier multiblock for the generation of <Color id="RED">Entangled Condensates</Color>. It is a relatively simple multiblock mechanically, taking in a molten resource, and generating the relevant condensate for use in the rest of the BEC system. The resulting <Color id="RED">Entangled Condensate</Color> can only be transferred via a <ItemLink id="gregtech:gt.blockmachines:15475" icon="right"/>. They will be processed even if there is no space in the network. Other than being transferred via BEC conduits, they can only be stored in a [Bose-Einstein Condensate Containment Field](./containment_field.md). The <Color id="GREEN">BECEA</Color> consumes as much condensate as possible, depending on how much EU/t is supplied to the machine. Processing time is the max duration of all active recipes. The <Color id="GREEN">BECEA</Color> supports <Color id="BLUE">Multi-Amp and Laser Energy Hatches</Color>.

## Construction:
The <Color id="GREEN">BECEA</Color> is a relatively straight forward multiblock in it's construction, having no tiered components. The <ItemLink id="gregtech:gt.blockmachines:15476" icon="right"/> must be placed in the center of the final "slice" of the structure (the point of the "teardrop" shape), and all other buses/hatches must be replacing Electromagnetically-Isolated Casings on the opposite side. Note that "regular" output hatches cannot be used to collect the output condensates, requiring the use of the Bose-Einstein Condensate Hatch. <Color id="GREEN">Multi-Amp and Laser Energy Hatches</Color> are supported. Use the <ItemLink id="structurelib:item.structurelib.constructableTrigger" /> <ItemImage id="structurelib:item.structurelib.constructableTrigger" /> to visualize/build the structure. 

### Requires:
- 236 <ItemLink id="gregtech:gt.blockcasings.bec:3" icon="right"/>
- 232-233 <ItemLink id="gregtech:gt.blockcasings.bec:2" icon="right"/>
- 216 <ItemLink id="gregtech:gt.blockcasings.bec" icon="right"/>
- 184 <ItemLink id="gregtech:gt.blockcasings.bec:4" icon="right"/>
- 144-160 <ItemLink id="gregtech:gt.blockcasings.bec:1" icon="right"/>
- 148 <ItemLink id="gregtech:gt.blockglass1:9" icon="right"/>
- 101 <ItemLink id="gregtech:gt.blockcasings.bec:5" icon="right"/>
- 0+ Energy Hatch (any Electromagnetically-Isolated Casing in first slice) <ItemImage id="gregtech:gt.blockmachines:40" />
- 0+ Input Bus (any Electromagnetically-Isolated Casing in first slice) <ItemImage id="gregtech:gt.blockmachines:70" />
- 0+ Input Hatch (any Electromagnetically-Isolated Casing in first slice) <ItemImage id="gregtech:gt.blockmachines:50" />
- 0-1 <ItemLink id="gregtech:gt.blockmachines:15476" icon="right"/> (Center casing in final slice)

## Usage:
The actual mechanics of the <Color id="GREEN">BECEA</Color> itself are incredibly straight forward; put fluid in, get condensate out! There are however a couple of things to be aware of. Each entanglement recipe has two aspects shown in NEI, <Color id="BLUE">Quota Required</Color>, and <Color id="RED">Entanglement Duration</Color>, as shown below:
<RecipeFor id="gregtech:entangled_hypogen" input="miscutils:molten.hypogen"/>

### Quota Required:
This is simply the amount of EU required to perform one "recipe". This means that the more energy you can provide for the multiblock, the more parallels you will get on the production. The <Color id="GREEN">BECEA</Color> will consume as much molten material to create condensate as possible depending on how much EU/t is provided.

### Entanglement Duration:
This is the "processing time" of this one specific recipe. The <Color id="GREEN">BECEA</Color> processing time is simply calculated to be the maximum duration of all active recipes based on the amount of input fluid, and the amount of stored EU.

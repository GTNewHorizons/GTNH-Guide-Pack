---
item_ids:
  - gregtech:gt.blockmachines:15755
navigation:
  title: Bose-Einstein Condensate Containment Field
  parent: bec.md
  icon: gregtech:gt.blockmachines:15755
categories:
    - New Multiblocks
    - Bose-Einstein Condensate
author: Skorched
date: 2026-06-28
---

# Bose-Einstein Condensate Containment Field
<GameScene wrap="square" align="right">
  <ImportStructureLib controller="gregtech:gt.blockmachines:15755" />
</GameScene>
The <Color id="GREEN">Bose-Einstein Condensate Containment Field (BECCF)</Color> is a UMV tier multiblock for the storage of Bose-Einstein Condensates at the cost of power. The storage capacity of the multiblock is determined by the <Color id="RED">Field Strength</Color>, configurable in the controller's panel. For each unit of field strength, the multiblock can store 1L of condensate at the cost of 1 EU/t. If multiple containment fields are present on a network, any injected condensate is split based on their capacities. Any excess condensate beyond the storage capacity **can** be inserted, but it will be quickly <Color id="RED">voided</Color>. When a containment field is overfilled, 11% is voided per second. If the containment field shuts down, whether manually or through power loss, the entirety of it's contents will be voided. The <Color id="GREEN">Multi-Amp and Laser Energy Hatches</Color> are supported.

## Construction:
The <Color id="GREEN">BECCF</Color> has no tiered components. <ItemLink id="gregtech:gt.blockmachines:15476" icon="right"/> are able to be placed on the center block of each side of the machine in the center. Note that "regular" input hatches cannot be used to collect the condensates, requiring the use of the Bose-Einstein Condensate Hatch. Energy Hatches and Bose-Einstein Condensate Detector Hatches can replace any Electromagnetically-Isolated Casing on the structure. <Color id="GREEN">Multi-Amp and Laser Energy Hatches</Color> are supported. Use the <ItemLink id="structurelib:item.structurelib.constructableTrigger" /> <ItemImage id="structurelib:item.structurelib.constructableTrigger" /> to visualize/build the structure. 

### Requires:
- 1236 <ItemLink id="gregtech:gt.blockglass1:9" icon="right"/>
- 1045 <ItemLink id="gregtech:gt.blockcasings.bec" icon="right"/>
- 896 <ItemLink id="gregtech:gt.blockcasings.bec:3" icon="right"/>
- 568 <ItemLink id="gregtech:gt.blockcasings.bec:4" icon="right"/>
- 508 <ItemLink id="gregtech:gt.blockcasings.bec:6" icon="right"/>
- 439-443 <ItemLink id="gregtech:gt.blockcasings.bec:2" icon="right"/>
- 328-344 <ItemLink id="gregtech:gt.blockcasings.bec:1" icon="right"/>
- 292 <ItemLink id="gregtech:gt.blockcasings.bec:5" icon="right"/>
- 0+ Energy Hatch (any Electromagnetically-Isolated Casing) <ItemImage id="gregtech:gt.blockmachines:40" />
- 0+ <ItemLink id="gregtech:gt.blockmachines:15476" icon="right"/> (Fine-Structure Constant Manipulators on center of each side)
- 0+ <ItemLink id="gregtech:gt.blockmachines:15761" icon="right"/> (any Electromagnetically-Isolated Casing)

## Usage:
The <Color id="GREEN">BECCF</Color> is mechanically very simple. It stores condensates, and exposes them via the hatches to [Observation Arrays](./observation_array.md) on the network.

The storage capacity of the <Color id="GREEN">BECCF</Color> is detemined by the <Color id="RED">Field Strength</Color>, which is configurable in the parameters within the controller. For each unit of field strength set, the <Color id="GREEN">BECCF</Color> can hold 1L of condensate at the cost of consuming 1 EU/t.

If multiple <Color id="GREEN">BECCFs</Color> are present on a single network, the injected condensate is split based on the ratio of the capacities available in the containment fields.

Excess condensate **can** be inserted into a filled containment field, however this should be avoided at all costs as the excess will be voided at a rate of 11% per second.

> [!WARNING]
> If a <Color id="RED">BECCF</Color> is shut down at **any** point, it's contents will be <Color id="RED">**voided**</Color>

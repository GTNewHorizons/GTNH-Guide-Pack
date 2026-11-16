---
item_ids:
  - gregtech:gt.blockmachines:15751
quest_ids:
  - bLz_cD33RE24mtOb2aLxXg==
navigation:
  title: Decay Warehouse
  parent: ./multiblocks_index.md
  icon: gregtech:gt.blockmachines:15751
  position: -5001
---
# Decay Warehouse
<GameScene interactive={true} wrap="square" align="right" width="220" height="200">
  <ImportStructureLib controller="gregtech:gt.blockmachines:15751" />
</GameScene>

The <ItemLink id="gregtech:gt.blockmachines:15751" showIcon="left" /> is an IV tier multiblock for accelerating the decay of radioactive isotopes. The Decay Warehouse is an improved, batch-processing version of the <ItemLink id="miscutils:blockDecayablesChest" showIcon="left" /> because it can hold significantly more isotopes and increases their decay rate based on the amount inside the machine, although the decay chest can process isotopes individually.  
The total capacity of the Decay Warehouse equals the capacity of the super/quantum chest at the center of the structure divided by 400.  
Power is only consumed when items are pulled from the input bus or pushed to the output bus; no power is consumed while the machine is running.

<Template name="properties" 
  tier="IV"
  size="5x5x3"
  oc="none"
  reqMaintenance
/>

## Crafting and Construction
### Crafting
<RecipesFor id="gregtech:gt.blockmachines:15751" />
<RecipesFor id="gregtech:gt.blockcasings3:12" />

### Structure 
The Decay Warehouse has one tiered component. The super/quantum chest determines the total capacity of the machine. 

The water fills the interior of the structure and must be placed manually, but it does not all have to be source blocks. 

The Decay Warehouse can be rotated or flipped.

Use the <ItemLink id="structurelib:item.structurelib.constructableTrigger" showIcon="left" /> to visualize/build the structure.

| Component | Quantity and placement |
| --- | --- |
| <ItemLink id="gregtech:gt.blockmachines:15751" showIcon="left" /> | 1, Front center, 2nd layer |
| <ItemLink id="gregtech:gt.blockcasings3:12" showIcon="left" /> | 48-52 |
| <ItemLink id="NotEnoughItems:neiFluidDisplay:1" showIcon="left" /> | 17, Filling the interior |
| <ItemImage id="gregtech:gt.blockmachines:135" noTooltip />&9Tiered&r Super/Quantum Chest | 1 |
| <ItemImage id="gregtech:gt.blockmachines:41" noTooltip /><Tooltip label="Energy Hatch">Only Regular Hatches allowed</Tooltip> | 1+, Can replace any <ItemLink id="gregtech:gt.blockcasings3:12" showIcon="left" /> |
| <ItemImage id="gregtech:gt.blockmachines:90" noTooltip />Maintenance Hatch | 1, Can replace any <ItemLink id="gregtech:gt.blockcasings3:12" showIcon="left" /> |
| <ItemImage id="gregtech:gt.blockmachines:71" noTooltip />Input Bus | 1+, Can replace any <ItemLink id="gregtech:gt.blockcasings3:12" showIcon="left" /> |
| <ItemImage id="gregtech:gt.blockmachines:81" noTooltip />Output Bus | 1+, Can replace any <ItemLink id="gregtech:gt.blockcasings3:12" showIcon="left" /> |

### Wallsharing

Decay Warehouses may wallshare each of their sides to save on casings and buses/hatches. The machine never consumes more than 1A of power so it is possible to share one energy hatch between two machines.

## Usage

The Decay Warehouse has two operating modes, listed below. Do NOT try to insert isotopes through the super/quantum chest, and only ONE isotope is allowed inside the machine at any given time.  
View the contents of the internal inventory and the current decay rate in the GUI of the controller, by right-clicking the controller with a Portable Scanner, or by using an industrial information panel.  
Void the contents of the internal inventory by breaking the controller or by right-clicking the controller with a plunger.

- _Normal_ - Pulls isotopes (from the input bus) into the machine, and pushes decay products to the output bus.
- _Exporting_ - Pushes isotopes to the output bus, if necessary.

Isotopes only decay while inside the internal inventory of the Decay Warehouse. The machine takes 512 EU/t to pull/push items, and no power is consumed while the machine is processing isotopes.

The decay rate of the stored isotopes scales with the amount inside the machine and their original half-life, as seen in the following equation. Therefore, the Decay Warehouse should be stocked as much as possible to keep the decay rate high.

<Latex formula="\text{Decay Rate} = \text{Amount} \times (1 - e^{-\ln(2)/\text{Half-Life}})" scale="0.7" />

The table below shows the Decay Warehouse's capacity for each chest placed in the center.

| Tier | Inventory | Max Isotopes |
| --- | --- | --- |
| LV | <ItemLink id="gregtech:gt.blockmachines:135" showIcon="left" /> | 10,000 |
| MV | <ItemLink id="gregtech:gt.blockmachines:136" showIcon="left" /> | 20,000 |
| HV | <ItemLink id="gregtech:gt.blockmachines:137" showIcon="left" /> | 40,000 |
| EV | <ItemLink id="gregtech:gt.blockmachines:138" showIcon="left" /> | 80,000 |
| IV | <ItemLink id="gregtech:gt.blockmachines:139" showIcon="left" /> | 160,000 |
| LuV | <ItemLink id="gregtech:gt.blockmachines:125" showIcon="left" /> | 320,000 |
| ZPM | <ItemLink id="gregtech:gt.blockmachines:126" showIcon="left" /> | 640,000 |
| UV | <ItemLink id="gregtech:gt.blockmachines:127" showIcon="left" /> | 1,280,000 |
| UHV | <ItemLink id="gregtech:gt.blockmachines:128" showIcon="left" /> | 2,560,000 |
| UEV | <ItemLink id="gregtech:gt.blockmachines:129" showIcon="left" /> | 5,368,709 |
{: widths="50,,80" }

## References
- [GTNH Wiki - Decay Warehouse](https://wiki.gtnewhorizons.com/wiki/Decay_Warehouse)

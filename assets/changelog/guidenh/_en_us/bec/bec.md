---
navigation:
  title: Bose-Einstein Condensate System
  parent: /index.md
  icon: gregtech:gt.cell.entangled_neutronium
---
# Bose-Einstein Condensate System
Getting bored of having the same old 4 states of matter? No?! Well that's a shame, you're getting one! Introducing the all new <Color id="GREEN">Bose-Einstein Condensate (BEC)</Color> set of multiblocks and recipes!

Don't worry, you **do not** need a PhD in Condensed Matter Physics to understand this, you just unfortunately need the ability to read! This addition in 2.9 adds a variety of multiblocks that all revolve around a new fluid type, <Color id="GREEN">BEC</Color>. Although technically a fluid, it can only be generated using the <Color id="GREEN">BEC</Color> network of multis, so the automation is not as direct as most other systems. This page intends to give a brief overview of the system as a whole, as well as directing to relevant pages.

## BEC Network
This update adds the new <ItemLink id="gregtech:gt.blockmachines:15475" icon="right"/>, which is the backbone of your network. By connecting multiple <Color id="GREEN">BEC</Color> multiblocks together using these conduits, you create a <Color id="BLUE">BEC Network</Color>. This is functionally similar to an Applied Energistics network in terms of distribution of condensates. Condensates exist in a somewhat precarious state, needing very specific conditions just to exist. As such, they can only exist within the BEC network, offering a new set of requirements for automation.

## Nanites
Nanites are of critical importance in the <Color id="GREEN">BEC</Color> system, being used for assembly primarily. [Teleportation Nodes](./teleportation_node.md) use progress points instead of a traditional "timer" for its recipes. Each nanite in the [Observation Array](./observation_array.md) provides one progress point per tick to all nodes connected to that array. Several things can be done to reduce this speed, but the primary goal is to have as many nanites in the array as possible at any time, to gain as many progress points per tick as possible. If the tier of nanite used is insufficient for a given recipe or step, the node will not make any progress. Conversely, higher tier nanites will not provide **any** bonuses to the progress, so swapping between the "minimum viable" nanites is recommended where possible.

## Unrequested Condensates
Assembly will <Color id="RED">slow down</Color> when there are unrequested condensates on the network. When there are 3 or more of these, any recipe will fail entirely. Puasing a node with a controller hatch will prevent it from failing, as no assembly is taking place.

## Automation
As mentioned previously, the automation of <Color id="GREEN">BEC</Color> fluids is not as trivial as other mechanics in the pack. As such, a few useful hatches have been added as tools for your automation needs:
- [Condensate Detector Hatch](./condensate_detector_hatch.md)
- [Nanite Detector Hatch](./nanite_detector_hatch.md)
- [Teleportation Node Controller Hatch](./teleportation_controller_hatch.md)

Since condensates can only exist within the BEC network, these hatches are crucial to a successful automation.

## Multiblocks
There are a handful of multiblocks added for the creation and manipulation of <Color id="GREEN">BEC</Color> fluids, as linked below:
- [Bose-Einstein Condensate Entanglement Apparatus](./entanglement_apparatus.md)
- [Bose-Einstein Condensate Containment Field](./containment_field.md)
- [Bose-Einstein Condensate Maxwell Gate](./maxwell_gate.md)
- [Bose-Einstein Condensate Observation Array](./observation_array.md)
- [Observation Array Teleportation Node](./teleportation_node.md)


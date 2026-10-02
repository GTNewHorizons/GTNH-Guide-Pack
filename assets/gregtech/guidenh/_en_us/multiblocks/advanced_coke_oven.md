---
item_ids:
  - Railcraft:machine.alpha:12
navigation:
  title: Advanced Coke Oven 
  parent: ./multiblocks_index.md
  icon: Railcraft:machine.alpha:12
  position: -2001
quest_ids:
  - AAAAAAAAAAAAAAAAAAAMHw==
---

# Advanced Coke Oven

<GameScene interactive={true} wrap="square" align="right" width="320" height="300">
  <ImportStructureLib controller="Railcraft:machine.alpha:12" />
</GameScene>

The Advanced Coke Oven (ACO) is an MV tier multiblock for burning logs into charcoal. 

The ACO is a direct upgrade to the basic [Coke Oven](./coke_oven.md) because it is 90x faster, but it requires a burnable fuel such as the very charcoal that it produces and it does not produce creosote oil. Therefore, the ACO's maximum output is 1 charcoal per second, but its net output is 15 charcoal per 16 seconds. 

The ACO does not consume power and is initially faster than the [Pyrolyse Oven](./pyrolyse_oven.md), but that quickly changes as better heating coils and energy hatches are unlocked. 

The ACO is superseded by the [Industrial Coke Oven](./industrial_coke_oven.md) in EV.

| Property | Details |
| --- | --- |
| Unlock tier | MV |
| Structure size (LxWxH) | 3x3x4 |
| Maintenance and pollution | No maintenance Required, produces 80 gibbi/s of pollution |

## Crafting and Construction
The ACO consists of a single type of block and does not have a controller or any buses/hatches. The Multiblock Structure Hologram Projector does not visualize/build the structure, but it is very easy to build.

<RecipesFor id="dreamcraft:AdvancedCokeOvenBrick" handlerId="gt.recipe.blastfurnace" />

<RecipesFor id="Railcraft:machine.alpha:12" />

### Structure

| Component | Quantity and placement |
| --- | --- |
| <ItemLink id="Railcraft:machine.alpha:12" showIcon="left" /> | 34, 3x3x4 with hollow rectangle |

### Wallsharing
As a Railcraft multiblock, **the ACO cannot wallshare any part of its structure** and must be at least one block apart from other ACOs to form.

## Usage

The ACO produces one charcoal per second from logs. That is 90x faster than the basic [Coke Oven](./coke_oven.md), but it requires a burnable fuel such as the very charcoal that it produces and it does not produce creosote oil. Charcoal has a burntime of 1600 ticks which fuels the ACO for 16 seconds, resulting in a net loss of only 1/16 of the total output. The ACO can also turn coal into coal coke, sugar charcoal into sugar coke, and cactus charcoal into cactus coke (1 second each).

Inputs can be inserted into any block on any side of the structure and outputs can be extracted from any block on any side of the structure. The ACO does not auto-pull from adjacent inventories but it does auto-push. It is highly recommended to create a feedback loop that prioritizes re-inserting the charcoal before storing it elsewhere. For example, the following image uses an item conduit with SELF-FEED enabled and differing priority levels.

## References

- [GTNH Wiki: Advanced Coke Oven](https://wiki.gtnewhorizons.com/wiki/Advanced_Coke_Oven)

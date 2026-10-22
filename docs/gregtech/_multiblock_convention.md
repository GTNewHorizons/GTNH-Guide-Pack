---
---

# Multiblock Document Convention

*This document is for only document writers + developers. Normal users don't need to read this, and will not be shown on navigation bar.*

## Frontmatter
Frontmatter should follow these orders.
1. `item_ids`
1. `quest_ids`
1. `navigation`
    1. `title`
    1. `parent`
    1. `icon`
    1. `position`

## Document Layout
Document is written in following orders.
1. H1 with **Multiblock Name** itself
1. `<GameScene>` using `<ImportStructureLib>` with `width="220"` and `height="200"`(this is for low-resolution user, I've checked 1920x1080).
1. The Machine name described with `<ItemLink>`(If there is no representative controller block for the multiblock, it must be replaced using `ItemImage` and the multiblock name - like [Advanced Coke Oven](./advanced_coke_oven.md)), including abbreviations, followed by simple summary that describes what this machine will do, compare description with other machines(what this supersedes, what other supersedes this, or what machine behaves similar), special notes for this machine, etc.
1. Machine property mostly from wiki, with following order:
    1. Unlock Tier
    1. Structure Size(LxWxH) - can pass (LxWxH) when It is cube shaped - has same length/width/height.
    1. Power - `Regular`, `Any Hatches allowed, includes Multi-Amp and Laser Hatches`, `Regular, but upgrading tier can unlock restrictions`, `None`, or `Lower than 4A`(for Turbine generators).
    1. Overclocks - `Imperfect`, `Perfect`, `Unique` or `None`. can link related documents on here.
    1. Maintenance - `Need Maintenance`, or `No maintenance needed`.
    1. Pollution - `Produces no pollution`, `Produces N gibbl/s pollution`, or `Produces N gibbl/s pollution, and require Muffler Hatch`.
1. Crafting and Construction on H2
    1. Crafting - Recipes for controller and casings using `<RecipesFor />`. should filter unrelated/irrevelent recipes.
    1. Structure - notify this MB can rotatable or not, and write Wiki-style table that lists up Quantity and placement. should use `<ItemLink>` If possible, all Hatches/Buses include Energy/Dynamo use `LV` Tier `<ItemImage noTooltip>`, with `ToolTip` to describe limitation or special restrictions.
       Quantity should be described as `Number +` or `From-To` format, like `1+`, `1`, or `1-10` for example.
       Placement instruction like replaceable casings or position instruction should follow after quantity.
    1. Wallshare Explaination
1. Usage that describes machine's behavior + statictics with graphs/tables and gamescenes for detailed information. 
1. References

### Crafting and Construction - Structure Template
| <ItemImage id="gregtech:gt.blockmachines:41" noTooltip /><Tooltip label="Energy Hatch">Hatch Limit explaination</Tooltip> | N+, |
| <ItemImage id="gregtech:gt.blockmachines:90" noTooltip />Maintenance Hatch | N+, |
| <ItemImage id="gregtech:gt.blockmachines:91" noTooltip />Muffler Hatch | N+, |
| <ItemImage id="gregtech:gt.blockmachines:71" noTooltip />Input Bus | N+, |
| <ItemImage id="gregtech:gt.blockmachines:51" noTooltip />Input Hatch | N+,|
| <ItemImage id="gregtech:gt.blockmachines:81" noTooltip />Output Bus | N+, |
| <ItemImage id="gregtech:gt.blockmachines:61" noTooltip />Output Hatch | N+, |

## Convention
- All **Multiblock Reference** should use `ItemLink` with markdown link, to make user clearly know which block this link points to and what this block is.
- Navigation position follow multiblock's tier position - for example, IV multiblock use `-5001`, and ZPM use `-7001`, to make lower tier multiblocks appears on top.
- All documents must comply with the rules described at `CONTRIBUTING.md` which is in project root.

---
navigation:
  parent: /items-blocks-index.md
  title: 无线终端
  icon: appliedenergistics2:item.ToolWirelessTerminal
categories:
- tools
item_ids:
- appliedenergistics2:item.ToolWirelessTerminal
- ae2fc:wireless_interface_terminal
- ae2fc:wireless_fluid_pattern_terminal
- ae2fc:wireless_level_terminal
- ae2wct:wirelessCraftingTerminal
- ae2fc:wireless_ultra_terminal
---

# 无线终端系统

<Row>
  <ItemImage id="appliedenergistics2:item.ToolWirelessTerminal" scale="4" />
  <ItemImage id="ae2wct:wirelessCraftingTerminal" scale="4" />
  <ItemImage id="ae2fc:wireless_ultra_terminal" scale="4" />
</Row>

<Row>
  <ItemImage id="ae2fc:wireless_interface_terminal" scale="4" />
  <ItemImage id="ae2fc:wireless_fluid_pattern_terminal" scale="4" />
  <ItemImage id="ae2fc:wireless_level_terminal" scale="4" />
</Row>

无线终端是常规[有线终端](terminals.md)的便携版本，界面功能完全一致，但使用[升级卡](upgrade_cards.md)插槽替代<ItemLink id="appliedenergistics2:item.ItemViewCell" />（显示元件）插槽。

绑定网络方法：将终端放入已连接网络的<ItemLink id="appliedenergistics2:tile.BlockWireless" />（ME无线访问点）右上角插槽（带有无线终端图标的槽位）。

需处于<ItemLink id="appliedenergistics2:tile.BlockWireless" />的信号范围内方可使用，可在<ItemLink id="appliedenergistics2:tile.BlockCharger" />（充能器）中补充能量。

# 基础无线终端

<ItemImage id="appliedenergistics2:item.ToolWirelessTerminal" scale="4" />

便携式基础终端！可在<ItemLink id="appliedenergistics2:tile.BlockWireless" />覆盖范围内访问[网络存储](../ae2-mechanics/import-export-storage.md)并提交[自动合成](../ae2-mechanics/autocrafting.md)请求。

## 界面说明

详见[终端系统](terminals.md)

## 合成配方

<RecipeFor id="appliedenergistics2:item.ToolWirelessTerminal" />

# 无线合成终端

<ItemImage id="ae2wct:wirelessCraftingTerminal" scale="4" />

在基础无线终端功能上增加合成网格，可自动从[网络存储](../ae2-mechanics/import-export-storage.md)补充材料。Shift+点击输出槽需谨慎！

## 界面说明

详见[终端系统](terminals.md)

## 升级卡支持

支持以下[升级卡](upgrade_cards.md)：
* <ItemLink id="ae2wct:infinityBoosterCard" />：在任意世界
* <ItemLink id="ae2wct:magnetCard" />：提升电池容量


## 合成配方

<RecipeFor id="ae2wct:wirelessCraftingTerminal" />

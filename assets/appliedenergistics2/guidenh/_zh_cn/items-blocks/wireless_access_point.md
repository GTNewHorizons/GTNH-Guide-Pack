---
navigation:
  parent: /items-blocks-index.md
  title: ME无线访问点
  icon: appliedenergistics2:tile.BlockWireless
categories:
- devices
item_ids:
- appliedenergistics2:tile.BlockWireless
- appliedenergistics2:item.ItemMultiMaterial:42
---

# ME无线访问点

<ItemImage id="appliedenergistics2:tile.BlockWireless" scale="4" />

允许通过<ItemLink id="appliedenergistics2:item.ToolWirelessTerminal" />（无线终端）进行无线访问。覆盖范围和能耗取决于安装的<ItemLink id="appliedenergistics2:item.ItemMultiMaterial:42" />（无线信号增幅器）数量。

一个网络中可以存在任意数量的无线访问点，每个访问点可安装多个增幅器，通过调整配置优化能耗和覆盖范围。

注意：增幅卡所增加的范围及耗电并不线性关系，而是指数级关系！

需要占用[频道](../ae2-mechanics/channels.md)。

同时用于绑定[无线终端](wireless_terminals.md)。

# 无线信号增幅器

<ItemImage id="appliedenergistics2:item.ItemMultiMaterial:42" scale="2" />

用于扩展无线访问点的信号覆盖范围。

## 合成配方

<RecipeFor id="appliedenergistics2:tile.BlockWireless" />

<RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:42" />
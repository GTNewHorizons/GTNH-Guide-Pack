---
navigation:
  parent: /items-blocks-index.md
  title: ME成型面板
  icon: appliedenergistics2:item.ItemMultiPart:320
categories:
- devices
item_ids:
- appliedenergistics2:item.ItemMultiPart:320
---


# 成型面板

<ItemImage id="appliedenergistics2:item.ItemMultiPart:320" scale="4" />


成型面板用于放置方块和丢弃物品。使用它一般需要构建一个[子网](../ae2-mechanics/subnetworks.md),当AE子网中的成型面板优先级高于所有存储设备时，进入子网的物品会被成型面板放置或丢弃。**使用时请确保在领地插件中启用假玩家权限**

成型面板属于[线缆子部件](../ae2-mechanics/cables-subparts.md)。



## 过滤设置

默认情况下会放置/丢弃所有物品。在过滤槽中放入物品将启用白名单模式，仅允许指定物品被放置。

即使未实际拥有某物品，仍可通过JEI/REI将其拖入过滤槽。

右键点击流体容器（如桶或储罐）可设置流体过滤器而非容器物品本身。

## 优先级

点击GUI右上角的扳手图标可设置优先级。物品进入网络时将优先存入最高优先级的存储设备。

## 可安装升级

成型面板支持以下[升级卡](upgrade_cards.md)：
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:27" />：增加过滤槽数量
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:29" />：支持按耐久度过滤或忽略物品NBT
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:31" />：将过滤模式从白名单切换为黑名单

## 合成配方

<RecipeFor id="appliedenergistics2:item.ItemMultiPart:320" />
---
navigation:
  parent: /items-blocks-index.md
  title: ME存储总线
  icon: appliedenergistics2:item.ItemMultiPart:220
categories:
- devices
item_ids:
- appliedenergistics2:item.ItemMultiPart:220
- ae2fc:part_fluid_storage_bus
- thaumicenergistics:part.base:2
---

# 存储总线

<Row gap="20">
<ItemImage id="appliedenergistics2:item.ItemMultiPart:220" scale="4" />
<ItemImage id="ae2fc:part_fluid_storage_bus" scale="4" />
<ItemImage id="thaumicenergistics:part.base:2" scale="4" />
</Row>

>*当你第一次获得存储总线时会获得<Color color="#aa00fffc">成就:无限潜能</Color>，这是你第一次瞥见AE自动化的冰山一角*

存储总线能将相邻的容器接入AE网络存储中。

基于AE2"通过设备交互实现复合功能"的设计理念，存储总线并非只能用于存储。通过[子网络](../ae2-mechanics/subnetworks.md)将存储总线设置为网络中唯一的存储设备，可将其作为物品传输的源头或终点。

存储总线属于[线缆子部件](../ae2-mechanics/cables-subparts.md)。

## 过滤功能

默认情况下总线会存储所有物品。在过滤槽中放置物品可设为白名单模式，仅允许存储指定物品。

即使当前未拥有某物品，仍可通过JEI/REI将物品或流体拖入过滤槽（流体需通过容器设置）。

右键使用流体容器（如桶或储罐）可将流体设为过滤器而非容器本身。

## 优先级

通过点击GUI右上角的扳手图标设置优先级。
物品进入网络时会优先存入最高优先级的存储。当多个存储优先级相同时，若某个存储已存在该物品，则优先选择该存储。
物品取出时会优先从最低优先级的存储提取。该机制使高优先级存储被优先填充，低优先级存储被优先清空。

## 设置选项

* 可根据相邻容器当前内容进行分区（过滤）
* 可设置是否允许网络查看总线无法提取的容器内物品
* 可设置为双向、仅存入或仅取出模式

## 升级卡支持

存储总线支持以下[升级卡](upgrade_cards.md)：

* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:27" />：增加过滤槽数量
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:29" />：支持按耐久度过滤或忽略物品NBT
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:31" />：将过滤模式从白名单切换为黑名单
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:55" />：用于对矿典的过滤，最大字节上限为256个字符，2.9.0现在字节上限增大到1024个字符了 __感谢youkoaona吧__

## 合成配方

<RecipeFor id="appliedenergistics2:item.ItemMultiPart:220" />
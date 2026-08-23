---
navigation:
  parent: /items-blocks-index.md
  title: ME-IO端口
  icon: appliedenergistics2:tile.BlockIOPort
categories:
- devices
item_ids:
- appliedenergistics2:tile.BlockIOPort
---

# ME IO端口

<ItemImage id="appliedenergistics2:tile.BlockIOPort" scale="4" />

IO端口可用于快速将物品在网络存储与端口中的[存储元件](./storage_cells.md)之间转移。

可使用<ItemLink id="appliedenergistics2:item.ToolCertusQuartzWrench" />旋转设备方向。

## 设置项

* 可配置当元件为空/已满/操作完成时自动移至输出槽
  * 前两种模式可以望文生义，第三种模式的逻辑为：如果一次转移物品的量小于当前IO端口对应的单次转移量，即会判定为传输完成，加速卡会提高这个转移量。
* GUI中央箭头可设置传输方向：从元件到网络存储，或反向传输

## 可安装升级

IO端口支持以下[升级卡](upgrade_cards.md)：
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:30" /> 提升单次操作传输量

## 合成配方

<RecipeFor id="appliedenergistics2:tile.BlockIOPort" />

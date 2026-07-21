---
navigation:
  parent: /items-blocks-index.md
  title: ME标准发信器
  icon: appliedenergistics2:item.ItemMultiPart:280
categories:
- devices
item_ids:
- appliedenergistics2:item.ItemMultiPart:280
---

# ME标准发信器

<ItemImage id="appliedenergistics2:item.ItemMultiPart:280" scale="4" />

ME标准发信器会根据[网络存储](../ae2-mechanics/import-export-storage.md)中指定物品的数量发出红石信号。

另有一种ME能源发信器，会根据网络中存储的[能源](../ae2-mechanics/energy.md)量发出红石信号。

即使未实际拥有某物品，仍可通过JEI/REI将其拖入过滤槽。

右键点击流体容器（如桶或储罐）可设置流体过滤器而非容器物品本身。

该设备属于[线缆子部件](../ae2-mechanics/cable-subparts.md)。

与其他[设备](../ae2-mechanics/devices.md)不同，标准发信器*无需*占用[频道](../ae2-mechanics/channels.md)。

## 设置项

* 可切换"大于等于"或"小于"模式
* 安装<ItemLink id="appliedenergistics2:item.ItemMultiMaterial:53" />后，可启用"合成时发信"或"发信触发合成"模式

## 可安装升级

标准发信器支持以下[升级卡](upgrade_cards.md)：
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:29" /> 启用按耐久度过滤或忽略物品NBT
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:53" /> 启用合成相关功能

## 合成控制功能

安装<ItemLink id="appliedenergistics2:item.ItemMultiMaterial:53" />后，发信器将启用合成控制模式：

**模式一：合成时发信**  
当<ItemLink id="appliedenergistics2:tile.BlockInterface" />正在合成指定物品时发出红石信号。适用于按需启动高耗能设备。

**模式二：发信触发合成**  
创建虚拟[合成样板](patterns.md)（需确保网络中不存在该物品的实际样板）。当发信器激活时，系统会认为该物品"即将被合成"，适用于：
- 无限资源农场（如无原料输入的自动化生产）
- 处理递归配方（如"1圆石=2圆石"的复制机）
- 概率性产出设备（如非100%成功率的机器）

## 合成配方

<RecipeFor id="appliedenergistics2:item.ItemMultiPart:280" />

<RecipeFor id="appliedenergistics2:item.ItemMultiPart:280" />
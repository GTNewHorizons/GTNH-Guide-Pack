---
navigation:
  parent: /items-blocks-index.md
  title: ME箱子
  icon: appliedenergistics2:tile.BlockChest
categories:
- devices
item_ids:
- appliedenergistics2:tile.BlockChest
---

# ME箱子

<ItemImage id="appliedenergistics2:tile.BlockChest" scale="4"/>

ME箱子集成了<ItemLink id="appliedenergistics2:item.ItemMultiPart:380" />、<ItemLink id="appliedenergistics2:tile.BlockDrive" />和<ItemLink id="appliedenergistics2:tile.BlockEnergyAcceptor" />，相当于微型网络。由于仅支持单个[存储元件](../items-blocks/storage_cells.md)，其独立存储能力有限。

核心功能：通过内置终端直接管理插入的存储元件。主网络中的[设备](../ae2-mechanics/devices.md)可通过[网络存储](../ae2-mechanics/import-export-storage.md)访问ME箱子内容。

## 

* **顶部面**：打开集成终端（仅允许存入物品）
* **其他面**：显示存储元件插槽和优先级设置（支持物流设备存取）
* 使用<ItemLink id="appliedenergistics2:item.ToolCertusQuartzWrench" />调整设备朝向

<GameScene width="250" height="190" zoom="4" background="transparent">
<ImportStructure src="../assets/structures/chest_color.snbt" />
<IsometricCamera yaw="135" pitch="30" />
</GameScene>

## 技术参数

* 内置小型AE能源缓冲（未连接[能源元件](../items-blocks/energy_cells.md)时，高频存取可能断电）
* 使用<ItemLink id="appliedenergistics2:item.ToolColorApplicator" />可改变终端颜色
* 支持与普通终端相同的设置（不支持<ItemLink id="appliedenergistics2:item.ItemViewCell" />）

## 元件状态指示灯

| 颜色   | 状态描述                  |
| :----- | :----------------------- |
| 绿色   | 元件为空                  |
| 蓝色   | 元件有存储内容            |
| 橙色   | [类型容量](../ae2-mechanics/bytes-and-types.md)已满 |
| 红色   | [存储容量](../ae2-mechanics/bytes-and-types.md)已满 |
| 黑色   | 断电或未分配[频道](../ae2-mechanics/channels.md) |

## 优先级设置

点击元件插槽界面右上角扳手图标设置优先级：
- **存入逻辑**：物品优先进入最高优先级存储
- **同类优先**：同优先级时优先已有该物品的存储
- **分区优先**：分区元件在同优先级组中视为已包含物品
- **取出逻辑**：优先从最低优先级存储提取

## 合成配方

<RecipeFor id="appliedenergistics2:tile.BlockChest" />
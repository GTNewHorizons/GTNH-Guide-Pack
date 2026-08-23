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
* 使用<ItemLink id="appliedenergistics2:item.ToolColorApplicator" />可改变终端颜色
* ME箱子可以用来给染色器填充颜料。


## 合成配方

<RecipeFor id="appliedenergistics2:tile.BlockChest" />
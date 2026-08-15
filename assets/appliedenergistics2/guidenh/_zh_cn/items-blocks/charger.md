---
navigation:
  parent: /items-blocks-index.md
  title: 充能器
  icon: appliedenergistics2:tile.BlockCharger
categories:
- machines
item_ids:
- appliedenergistics2:tile.BlockCharger
---

# 充能器

<ItemImage id="appliedenergistics2:tile.BlockCharger" scale="4" />

核心功能：
- 为兼容工具充能
- 将<ItemLink id="gregtech:gt.metaitem.01:8516" />转化为<ItemLink id="appliedenergistics2:item.ItemMultiMaterial:1" />

## 技术参数

* 能量接口：顶部/底部（支持AE2线缆或FE能源导管）
* 兼容能源：AE2能源（AE）或其他能源
* 物品存取：任意面（仅允许取出成品，无需过滤）
* 方向调整：使用<ItemLink id="appliedenergistics2:item.ToolCertusQuartzWrench" />旋转设备朝向

## 主要用途

* 制作充能水晶：<ItemImage id="gregtech:gt.metaitem.01:8516" /><ItemLink id="gregtech:gt.metaitem.01:8516" /> → <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:1" />
* 制作陨石罗盘：<ItemImage id="minecraft:compass" /><ItemLink id="minecraft:compass" /> → <ItemLink id="appliedenergistics2:tile.BlockSkyCompass" />
* 村民职业工作站

## 手动充能

~~在顶部/底部安装<ItemLink id="appliedenergistics2:item.ItemMultiMaterial:46" />，右键转动曲柄直至物品完成充能。~~

## 简易自动化示例

通过调整朝向实现半自动化供料：

<GameScene zoom="4" background="transparent">
  <ImportStructure src="../assets/structures/charger_hopper.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

## 合成配方

<RecipeFor id="appliedenergistics2:tile.BlockCharger" />
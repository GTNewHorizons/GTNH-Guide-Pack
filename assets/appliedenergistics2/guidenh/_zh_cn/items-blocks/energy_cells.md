---
navigation:
  parent: /items-blocks-index.md
  title: 能源元件
  icon: appliedenergistics2:tile.BlockDenseEnergyCell
categories:
- network infrastructure
item_ids:
- appliedenergistics2:tile.BlockEnergyCell
- appliedenergistics2:tile.BlockDenseEnergyCell
- appliedenergistics2:tile.BlockCreativeEnergyCell
- appliedenergistics2:item.ItemMultiPart:690
---

# 能源元件

<Row gap="20">
  <BlockImage id="appliedenergistics2:tile.BlockEnergyCell" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockDenseEnergyCell" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockCreativeEnergyCell" scale="4" />
</Row>

该设备可为网络提供额外的[能源存储](../ae2-mechanics/energy.md)。适当的能源缓冲有助于缓解物品大量存取时的瞬时能耗波动，更大的存储容量可使网络在无能源输入时（如太阳能板夜间停运）持续运行，或应对[空间存储系统](../ae2-mechanics/spatial-io.md)的瞬时高能耗。

## 充能指示条

<Row>
<BlockImage id="appliedenergistics2:tile.BlockEnergyCell" scale="4" />
</Row>

元件侧面的指示条显示当前储能状态：

*   0 条：储能低于25%
*   1 条：储能25%-50%
*   2 条：储能50%-75%
*   3 条：储能75%-99%
*   4 条：储能99%以上

## 元件类型

*   <ItemLink id="appliedenergistics2:tile.BlockEnergyCell" />：基础型号，可存储20万AE能源，足以应对常规网络操作中的能耗波动
*   <ItemLink id="appliedenergistics2:tile.BlockDenseEnergyCell" />：致密型号，可存储160万AE能源，适用于依赖储能运行网络或处理大型[空间存储系统](../ae2-mechanics/spatial-io.md)的瞬时高负载
*   <ItemLink id="appliedenergistics2:tile.BlockCreativeEnergyCell" />：创造模式专用，提供无限能源

## 配方

<Row>
  <RecipeFor id="appliedenergistics2:tile.BlockEnergyCell" />

  <RecipeFor id="appliedenergistics2:tile.BlockDenseEnergyCell" />
</Row>

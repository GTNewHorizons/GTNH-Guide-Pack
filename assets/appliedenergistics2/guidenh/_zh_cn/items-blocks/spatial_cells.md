---
navigation:
  parent: /items-blocks-index.md
  title: 空间存储元件
  icon: appliedenergistics2:item.ItemSpatialStorageCell.2Cubed
categories:
- tools
item_ids:
- appliedenergistics2:item.ItemSpatialStorageCell.2Cubed
- appliedenergistics2:item.ItemSpatialStorageCell.16Cubed
- appliedenergistics2:item.ItemSpatialStorageCell.128Cubed
---

<Row>
<ItemImage id="appliedenergistics2:item.ItemSpatialStorageCell.2Cubed" scale="4"/>
<ItemImage id="appliedenergistics2:item.ItemSpatialStorageCell.16Cubed" scale="4"/>
<ItemImage id="appliedenergistics2:item.ItemSpatialStorageCell.128Cubed" scale="4"/>
</Row>

空间存储元件是[空间IO系统](../ae2-mechanics/spatial-io.md)运行的存储介质，空间IO系统运行时，操作范围的体积必须小于等于所用的空间存储元件的容量。空间存储元件有三个等级，容量分别是2、16、128立方米。

空间存储元件内部实质上是一个独立的维度，空间塔的工作原理是将已选择范围内的整个空间与元件中的同样大小的空间进行交换。当第一次使用一个新的空间存储元件时，元件会创建一个和其体积规格大小一致的维度。也就是说可以看作每个新的空间存储元件中都是充满空气方块的，第一次使用空间塔进行空间交换会将存储元件中对应大小的空气交换出来。

<Color id="RED">空间存储元件一经使用，你就不能重置、格式化或调整空间存储元件的尺寸。如果想使用不同的尺寸，请制作一个新的元件。</Color>

# 空间存储元件

空间存储元件用于[存储物理空间区域](../ae2-mechanics/spatial-io.md)，需在<ItemLink id="appliedenergistics2:tile.BlockSpatialIOPort" />（空间IO端口）中使用。

与普通[存储元件](../items-blocks/storage_cells.md)不同，空间存储元件**无法重新格式化**。

**特别注意：空间存储元件一经使用，其尺寸将永久固定，无法重置、重设或调整大小！** 如需不同尺寸，请制作新元件。

## 合成配方

<Row>
    <Recipe id="appliedenergistics2:item.ItemSpatialStorageCell.2Cubed" handlerId="Shapeless" />
    <Recipe id="appliedenergistics2:item.ItemSpatialStorageCell.16Cubed" handlerId="Shapeless" />
    <Recipe id="appliedenergistics2:item.ItemSpatialStorageCell.128Cubed" handlerId="Shapeless" />
</Row>

# 元件外壳

空间存储元件可通过"空间组件+外壳"或"外壳包裹组件"两种方式合成：

<Row>
    <Recipe id="appliedenergistics2:item.ItemSpatialStorageCell.2Cubed" />
    <Recipe id="appliedenergistics2:item.ItemSpatialStorageCell.2Cubed" handlerId="Shapeless" />
</Row>

单独合成元件外壳配方：

<RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:39" />

# 空间组件

空间组件是空间存储元件的核心部件，每级组件的存储维度提升8倍：

<Row>
    <RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:32" />
    <RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:33" />
    <RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:34" />
</Row>

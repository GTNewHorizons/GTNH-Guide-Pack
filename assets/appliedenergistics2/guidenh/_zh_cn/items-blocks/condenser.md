---
navigation:
  parent: /items-blocks-index.md
  title: 物质聚合器
  icon: appliedenergistics2:tile.BlockCondenser
  position: 310
categories:
- machines
item_ids:
- appliedenergistics2:tile.BlockCondenser
---
<ItemImage id="appliedenergistics2:tile.BlockCondenser" scale="4"/>

物质聚合器不需要消耗能量就能运作可以将输入进它的垃圾销毁或转化为<ItemLink id="appliedenergistics2:item.ItemMultiMaterial:6" showIcon="left" />或<ItemLink id="appliedenergistics2:item.ItemMultiMaterial:47" showIcon="left" />。前者是<ItemLink id="appliedenergistics2:item.ToolMassCannon" showIcon="left" />的弹药，后者是[量子环](../ae2-mechanics/quantum-bridge.md)系统的重要物品。


## 工作模式配置

### 垃圾桶模式
* 直接销毁所有输入物品

### 物质球模式
* 需在顶部插槽放置存储组件（如<ItemLink id="appliedenergistics2:item.ItemBasicStorageCell.1k" />）
* 每256个物品/桶流体合成1个物质球
* 推荐使用1k存储组件（8192字节容量）

### 物质奇点模式
* 需在顶部插槽放置存储组件（如<ItemLink id="appliedenergistics2:item.ItemBasicStorageCell.1k" />）
* 每256,000个物品/桶流体合成1个奇点
* 推荐使用64k存储组件（524,288字节容量）
* 也可以通入流体，125mb流体算作1物品。

## 合成配方

<RecipeFor id="appliedenergistics2:tile.BlockCondenser" />
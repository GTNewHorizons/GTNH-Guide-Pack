---
navigation:
  parent: /items-blocks-index.md
  title: 基础卡
  icon: appliedenergistics2:item.ItemMultiMaterial:25
  position: 410
categories:
- tools
item_ids:
- appliedenergistics2:item.ItemMultiMaterial:25
- appliedenergistics2:item.ItemMultiMaterial:26
- appliedenergistics2:item.ItemMultiMaterial:27
- appliedenergistics2:item.ItemMultiMaterial:53
- appliedenergistics2:item.ItemMultiMaterial:64
- appliedenergistics2:item.ItemMultiMaterial:68
---

# 基础卡

<Column>
  <Row>
    <ItemImage id="appliedenergistics2:item.ItemMultiMaterial:26" scale="2" />

    <ItemImage id="appliedenergistics2:item.ItemMultiMaterial:27" scale="2" />

    <ItemImage id="appliedenergistics2:item.ItemMultiMaterial:68" scale="2" />
	
    <ItemImage id="appliedenergistics2:item.ItemMultiMaterial:53" scale="2" />   
	
    <ItemImage id="appliedenergistics2:item.ItemMultiMaterial:64" scale="2" />
  </Row>
</Column>
升级卡会改变AE2设备和机器的行为，提高其速度、改善其过滤能力、启用红石控制等。

## 卡组件

<Row>
  <ItemImage id="appliedenergistics2:item.ItemMultiMaterial:25" scale="2" />

  <ItemImage id="appliedenergistics2:item.ItemMultiMaterial:28" scale="2" />
</Row>

查看 [高级卡](../ae2-mechanics/upgrade_card.md).

由基础卡或高级卡作为基底合成

<Row>
  <RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:25" />

  <RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:28" />
</Row>

## 红石卡

<ItemImage id="appliedenergistics2:item.ItemMultiMaterial:26" scale="2" />

红石卡为设备添加红石控制功能，在其 GUI 中增加一个切换按钮，用于在不同红石条件之间切换。

<RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:26" />

## 容量卡

<ItemImage id="appliedenergistics2:item.ItemMultiMaterial:27" scale="2" />

容量卡增加输入总线、输出总线、存储总线以及成型面板的过滤槽位数量。

<RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:27" />

## 溢出销毁卡

<ItemImage id="appliedenergistics2:item.ItemMultiMaterial:68" scale="2" />

溢出销毁卡可应用于<ItemLink id="appliedenergistics2:tile.BlockCellWorkbench" />中的[存储元件](storage_cells.md)，当元件已满时会删除传入的物品。（请确保对你的元件进行[分区](cell_workbench.md)！）与均分卡结合使用时，如果元件中特定物品的分区已满，即使其他物品的分区仍有空间，该物品也会被销毁。

<RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:68" />

## 合成卡

<ItemImage id="appliedenergistics2:item.ItemMultiMaterial:53" scale="2" />

合成卡使设备可以向你的[自动合成](../ae2-mechanics/autocrafting.md)系统发送合成请求，以获取所需的物品。

<RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:53" />

## 粘性卡

<ItemImage id="appliedenergistics2:item.ItemMultiMaterial:64" scale="2" />

在此元件上分区的任何物品、流体和要素只能存储在带有粘滞卡的元件或存储总线中，不会存储在网络中的其他地方。

<RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:64" />
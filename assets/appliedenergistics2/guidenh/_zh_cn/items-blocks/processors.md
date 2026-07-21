---
navigation:
  parent: /items-blocks-index.md
  title: 处理器
  icon: appliedenergistics2:item.ItemMultiMaterial:23
categories:
- misc ingredients blocks
item_ids:
- appliedenergistics2:item.ItemMultiMaterial:16
- appliedenergistics2:item.ItemMultiMaterial:17
- appliedenergistics2:item.ItemMultiMaterial:18
- appliedenergistics2:item.ItemMultiMaterial:20
- appliedenergistics2:item.ItemMultiMaterial:22
- appliedenergistics2:item.ItemMultiMaterial:23
- appliedenergistics2:item.ItemMultiMaterial:24

---

# 处理器系统

<Row>
  <ItemImage id="appliedenergistics2:item.ItemMultiMaterial:22" scale="4" />

  <ItemImage id="appliedenergistics2:item.ItemMultiMaterial:23" scale="4" />

  <ItemImage id="appliedenergistics2:item.ItemMultiMaterial:24" scale="4" />
</Row>

处理器是AE2[设备](../ae2-mechanics/devices.md)和机器的核心组件，也是首个重要的自动化挑战。共有三种类型，分别使用金锭、<ItemLink id="appliedenergistics2:item.ItemMultiMaterial:0" />和钻石制造。需通过[压印模板](presses.md)在<ItemLink id="appliedenergistics2:tile.BlockInscriber" />中经过多步骤工艺完成（通常需要一系列压印器和过滤管道协同工作）。

## 生产工艺流程

<Column gap="5">
  1. **收集基础材料**：硅、红石、金锭、赛特斯石英水晶、钻石

  <RecipeFor id="gregtech:gt.metaitem.01:17856" />

  <br />

2. **预制印刷电路组件**

  <Row>
    <RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:20" />

    <RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:16" />
  </Row>

  <Row>
    <RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:17" />

    <RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:18" />
  </Row>

  <br />

3. **最终组装成型**

  <Row>
    <RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:23" />

    <RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:23" />

    <RecipeFor id="appliedenergistics2:item.ItemMultiMaterial:24" />
  </Row>
</Column>
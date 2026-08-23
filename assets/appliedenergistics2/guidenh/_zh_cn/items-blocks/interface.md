---
navigation:
  parent: /items-blocks-index.md
  title: 接口
  icon: appliedenergistics2:tile.BlockInterface
item_ids:
  - appliedenergistics2:tile.BlockInterface
  - appliedenergistics2:item.ItemMultiPart:440
  - appliedenergistics2:item.ItemMultiPart:471
categories:
- devices
---


# ME接口

<Row gap="20">
<BlockImage id="appliedenergistics2:tile.BlockInterface" scale="4" />
<ItemImage id="appliedenergistics2:item.ItemMultiPart:440" scale="4" />
<ItemImage id="appliedenergistics2:item.ItemMultiPart:471" scale="4" />
</Row>

接口的作用类似于小型箱体/流体储罐，能够根据槽位设置从网络存储中自动补充或清空物品。其单游戏刻可处理多达9组物品，若搭配高速管道可实现快速输入输出。

另一个重要特性是，接口最多可存储9种不同流体（普通储罐仅能存1种），同时兼具物品存储功能。本质上它们是带有增强功能的箱体/复合储罐，断开网络连接时仍可作为普通容器使用。上方9个槽位定义需要维持的库存物品

## 自动合成
ME接口是[自动合成](../ae2-mechanics/autocrafting.md)系统的发配端。所有的自动合成原料都从ME接口发配到目的地。

## 变体类型

接口有两种形态：标准版和扁平版/[子部件](../ae2-mechanics/cables-subparts.md)：

* **标准接口**：允许所有面进行物品存取，并提供全向网络连接
* **扁平接口**：作为线缆子部件，可密集排布。仅允许正面存取物品，且不提供正面网络连接

两者可通过合成相互转换。

## 可安装升级

接口支持以下[升级卡](upgrade_cards.md)：
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:29" /> 启用模糊匹配（按耐久或忽略NBT）
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:53" /> 启用自动合成请求，优先从存储提取，不足时触发[自动合成](../ae2-mechanics/autocrafting.md)

## 优先级设置

点击GUI右上角扳手设置优先级，高优先级接口优先获取物品。

## 合成配方
<Row>
<Recipe id="appliedenergistics2:tile.BlockInterface" />
<RecipeFor id="appliedenergistics2:item.ItemMultiPart:440" />
</Row>
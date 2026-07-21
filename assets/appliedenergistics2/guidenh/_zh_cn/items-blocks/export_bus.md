---
navigation:
  parent: /items-blocks-index.md
  title: ME输出总线
  icon: appliedenergistics2:item.ItemMultiPart:260
categories:
- devices
item_ids:
- appliedenergistics2:item.ItemMultiPart:260
- ae2fc:part_fluid_export
- thaumicenergistics:part.base:3
---

<Row>

<ItemImage id="appliedenergistics2:item.ItemMultiPart:260" scale="4" />

<ItemImage id="ae2fc:part_fluid_export" scale="4" />

<ItemImage id="thaumicenergistics:part.base:3" scale="4" />
</Row>


# ME流体输出总线

该设备从[网络存储](../ae2-mechanics/import-export-storage.md)中提取物品和流体（安装扩展模块后可支持更多类型），并推送至连接的容器。

为优化性能，当总线近期无操作时会进入"休眠模式"降低运行频率。成功输出后将加速至全速模式（每秒4次操作）。

属于[线缆子部件](../ae2-mechanics/cable-subparts.md)。

## 过滤设置

默认状态下不输出任何物品。在过滤槽中放入物品将建立白名单机制，仅允许指定物品输出。

可通过NEI将物品或流体直接拖入过滤槽（无需实际持有该物品）。

手持流体容器（如桶或储罐）右键点击可设置流体过滤（而非容器本身）。

## 升级支持

支持以下[升级卡](upgrade_cards.md)：

* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:27" /> 增加过滤槽数量
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:29" /> 提升单次操作传输量
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:31" /> 将过滤模式切换为黑名单
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:53" />：向[自动合成系统](../ae2-mechanics/autocrafting.md)发起合成请求，可配置优先使用现存物品或强制合成新物品
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:26" /> 添加红石控制（高电平激活/低电平激活/脉冲激活）

## 传输速率

| 加速卡数量 | 每次操作传输量 |
|:-----------|:--------------|
| 0          | 1             |
| 1          | 8             |
| 2          | 32            |
| 3          | 64            |
| 4          | 96            |

## 配方

<RecipeFor id="appliedenergistics2:item.ItemMultiPart:260" />
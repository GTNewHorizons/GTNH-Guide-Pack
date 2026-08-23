---
navigation:
  parent: /items-blocks-index.md
  title: ME二合一接口
  icon: ae2fc:fluid_interface
item_ids:
  - ae2fc:fluid_interface
  - ae2fc:part_fluid_interface
  - ae2fc:part_fluid_p2p_interface
categories:
- devices
---


# ME二合一接口

<Row gap="20">
<BlockImage id="ae2fc:fluid_interface" scale="4" />
<ItemImage id="ae2fc:part_fluid_interface" scale="4" 
<ItemImage id="ae2fc:part_fluid_p2p_interface" scale="4" />
</Row>

二合一接口和[接口](./interface.md)类似，但是可以处理流体。其中有流体槽位可以实现和接口相同的拉取功能，外部也能从二合一接口访问到AE网络中的流体。

## 设置项

* UI上方槽位定义需要维持的库存物品
* 点击UI右上角的接口图标切换至流体配置界面
* 使用流体容器右键（如桶）可设置流体过滤

## 可安装升级

接口支持以下[升级卡](upgrade_cards.md)：
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:29" /> 启用模糊匹配（按耐久或忽略NBT）
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:53" /> 启用自动合成请求，优先从存储提取，不足时触发[自动合成](../ae2-mechanics/autocrafting.md)

## 优先级设置

点击GUI右上角扳手设置优先级，高优先级接口会被AE网络优先存入物品。

## 流体封包
二合一接口依然保留了发配流体封包的能力。

## 合成配方

<Recipe id="ae2fc:fluid_interface" />

<RecipeFor id="ae2fc:part_fluid_interface" />
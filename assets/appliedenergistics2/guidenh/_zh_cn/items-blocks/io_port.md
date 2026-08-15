---
navigation:
  parent: /items-blocks-index.md
  title: ME-IO端口
  icon: appliedenergistics2:tile.BlockIOPort
categories:
- devices
item_ids:
- appliedenergistics2:tile.BlockIOPort
---

# ME IO端口

<ItemImage id="appliedenergistics2:tile.BlockIOPort" scale="4" />

IO端口可用于快速将[存储元件](../items-blocks/storage_cells.md)与[网络存储](../ae2-mechanics/import-export-storage.md)之间进行数据转移。

可使用<ItemLink id="appliedenergistics2:item.ToolCertusQuartzWrench" />旋转设备方向。

## 设置项

* 可配置当元件为空/已满/操作完成时自动移至输出槽
* 安装<ItemLink id="appliedenergistics2:item.ItemMultiMaterial:26" />后支持红石触发条件设置
* GUI中央箭头可设置传输方向：从元件到网络存储，或反向传输

## 可安装升级

IO端口支持以下[升级卡](upgrade_cards.md)：
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:30" /> 提升单次操作传输量
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:26" /> 添加红石控制（高电平激活/低电平激活/脉冲激活）

频率：冷状态5tick(0.25s)操作一次，随即进入热状态1tick(0.05s)操作一次。
速度：操作一次转移 256*(2^加速卡数量) 物品。  即最速是40960物品/s

## 合成配方

<RecipeFor id="appliedenergistics2:tile.BlockIOPort" />

利用这些特性，甚至可以（仅举例）：（流体也可以）(一般生存中都比较无用……)

1、将“数字化”的物品自动“实质化”(针对所有物品，无序标记) ：ME-IO端口所在网络仅使用存储总线进行物品存储，设置成将硬盘的内容导出；

2、在一定数量范围内抽取出网络中所有可抽取的物品：ME-IO端口设置为将网络中的内容写入元件，工序完成后到输出格；

3、自动压缩同类物品存储占用字节；

4、高速管道：ME物品传输。

5、打包机：将多个物品打包为1个，而后可以解压。

6、搭配元件工作台对存放杂物的元件进行“磁盘整理”。
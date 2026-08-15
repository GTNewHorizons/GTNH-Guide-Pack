---
navigation:
  parent: /items-blocks-index.md
  title: 线缆
  icon: appliedenergistics2:item.ItemMultiPart:36
categories:
- network infrastructure
item_ids:
- appliedenergistics2:item.ItemMultiPart
- appliedenergistics2:item.ItemMultiPart:1
- appliedenergistics2:item.ItemMultiPart:2
- appliedenergistics2:item.ItemMultiPart:3
- appliedenergistics2:item.ItemMultiPart:4
- appliedenergistics2:item.ItemMultiPart:5
- appliedenergistics2:item.ItemMultiPart:6
- appliedenergistics2:item.ItemMultiPart:7
- appliedenergistics2:item.ItemMultiPart:8
- appliedenergistics2:item.ItemMultiPart:9
- appliedenergistics2:item.ItemMultiPart:10
- appliedenergistics2:item.ItemMultiPart:11
- appliedenergistics2:item.ItemMultiPart:12
- appliedenergistics2:item.ItemMultiPart:13
- appliedenergistics2:item.ItemMultiPart:14
- appliedenergistics2:item.ItemMultiPart:15
- appliedenergistics2:item.ItemMultiPart:16

- appliedenergistics2:item.ItemMultiPart:20
- appliedenergistics2:item.ItemMultiPart:21
- appliedenergistics2:item.ItemMultiPart:22
- appliedenergistics2:item.ItemMultiPart:23
- appliedenergistics2:item.ItemMultiPart:24
- appliedenergistics2:item.ItemMultiPart:25
- appliedenergistics2:item.ItemMultiPart:26
- appliedenergistics2:item.ItemMultiPart:27
- appliedenergistics2:item.ItemMultiPart:28
- appliedenergistics2:item.ItemMultiPart:29
- appliedenergistics2:item.ItemMultiPart:30
- appliedenergistics2:item.ItemMultiPart:31
- appliedenergistics2:item.ItemMultiPart:32
- appliedenergistics2:item.ItemMultiPart:33
- appliedenergistics2:item.ItemMultiPart:34
- appliedenergistics2:item.ItemMultiPart:35
- appliedenergistics2:item.ItemMultiPart:36

- appliedenergistics2:item.ItemMultiPart:40
- appliedenergistics2:item.ItemMultiPart:41
- appliedenergistics2:item.ItemMultiPart:42
- appliedenergistics2:item.ItemMultiPart:43
- appliedenergistics2:item.ItemMultiPart:44
- appliedenergistics2:item.ItemMultiPart:45
- appliedenergistics2:item.ItemMultiPart:46
- appliedenergistics2:item.ItemMultiPart:47
- appliedenergistics2:item.ItemMultiPart:48
- appliedenergistics2:item.ItemMultiPart:49
- appliedenergistics2:item.ItemMultiPart:50
- appliedenergistics2:item.ItemMultiPart:51
- appliedenergistics2:item.ItemMultiPart:52
- appliedenergistics2:item.ItemMultiPart:53
- appliedenergistics2:item.ItemMultiPart:54
- appliedenergistics2:item.ItemMultiPart:55
- appliedenergistics2:item.ItemMultiPart:56

- appliedenergistics2:item.ItemMultiPart:520
- appliedenergistics2:item.ItemMultiPart:521
- appliedenergistics2:item.ItemMultiPart:522
- appliedenergistics2:item.ItemMultiPart:523
- appliedenergistics2:item.ItemMultiPart:524
- appliedenergistics2:item.ItemMultiPart:525
- appliedenergistics2:item.ItemMultiPart:526
- appliedenergistics2:item.ItemMultiPart:527
- appliedenergistics2:item.ItemMultiPart:528
- appliedenergistics2:item.ItemMultiPart:529
- appliedenergistics2:item.ItemMultiPart:530
- appliedenergistics2:item.ItemMultiPart:531
- appliedenergistics2:item.ItemMultiPart:532
- appliedenergistics2:item.ItemMultiPart:533
- appliedenergistics2:item.ItemMultiPart:534
- appliedenergistics2:item.ItemMultiPart:535
- appliedenergistics2:item.ItemMultiPart:536

---

<GameScene zoom="3" background="transparent">
  <ImportStructure src="../assets/structures/cables.snbt" />
  <IsometricCamera yaw="135" pitch="30" />
</GameScene>

ME网络可通过相邻的ME兼容设备建立，而线缆是扩展ME网络覆盖范围的主要方式。

不同颜色的线缆可防止相邻线缆自动连接，优化[频道](../ae2-mechanics/channels.md)分配。线缆颜色同时影响所连接终端的配色（福鲁伊克斯色线缆可连接所有颜色）。

**重要提示：频道分配与线缆颜色无关**

## 给新手的建议

**若您不熟悉频道机制，请优先使用智能线缆和致密智能线缆。它们可直观显示频道路径，帮助理解网络结构。**

## 功能说明

**这些线缆并非传统意义上的物流管道。** 它们没有内部存储，设备之间通过线缆建立网络连接而非物品传输。

---

## 玻璃线缆

<ItemImage id="appliedenergistics2:item.ItemMultiPart:16" scale="4" />

<ItemLink id="appliedenergistics2:item.ItemMultiPart:16" />是最基础的线缆，支持能量传输和8个[频道](../ae2-mechanics/channels.md)。提供17种配色（默认福鲁伊克斯色），可用染料染色。

染色方法：
- 工作台：8个同类型线缆+任意染料
- 游戏内：使用兼容的染色工具
- 浸入水桶可褪色

可升级为<ItemLink id="appliedenergistics2:item.ItemMultiPart:36" />（包层线缆）或<ItemLink id="appliedenergistics2:item.ItemMultiPart:56" />（智能线缆）

<RecipeFor id="appliedenergistics2:item.ItemMultiPart:16" />

<RecipeFor id="appliedenergistics2:item.ItemMultiPart:11" />

---

## 包层线缆

<ItemImage id="appliedenergistics2:item.ItemMultiPart:36" scale="4" />

与玻璃线缆功能相同，仅外观差异。可通过红石和荧石升级为<ItemLink id="appliedenergistics2:item.ItemMultiPart:536" />（致密包层线缆）

<Recipe id="appliedenergistics2:item.ItemMultiPart:36" />

<RecipeFor id="appliedenergistics2:item.ItemMultiPart:31" />

---

## 致密线缆

<ItemImage id="appliedenergistics2:item.ItemMultiPart:536" scale="4" />

高容量线缆，支持32个频道。使用时需注意：
1. 无法直接连接设备总线
2. 需通过普通线缆中转
3. 频道优先选择最短致密路径

<Recipe id="appliedenergistics2:item.ItemMultiPart:536" />

<RecipeFor id="aappliedenergistics2:item.ItemMultiPart:531" />

---

## 智能线缆

<Row>
<GameScene zoom="6" background="transparent">
  <ImportStructure src="../assets/structures/fluix_smart_cable.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

可视化诊断功能：
- 普通智能线缆：前4个频道显示线缆颜色，后4个显示白色条纹
- 致密智能线缆：每条纹代表4个频道
- 含控制器的网络：显示频道实际路径
- 临时网络：显示全网已用频道数

<Recipe id="appliedenergistics2:item.ItemMultiPart:56" />

<Recipe id="appliedenergistics2:item.ItemMultiPart:76" />

<RecipeFor id="appliedenergistics2:item.ItemMultiPart:71" />
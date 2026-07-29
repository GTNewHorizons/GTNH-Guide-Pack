---
item_ids:
    gregtech:gt.blockmachines:1000
navigation:
    title: 工业高炉
    parent: ./tier-lv-index.md
    icon: gregtech:gt.blockmachines:1000
quest_ids:
    - AAAAAAAAAAAAAAAAAAAATQ
---

# 工业高炉

<GameScene interactive={true} wrap="square" align="right" width="380" height="300" >
  <ImportStructure src="/assets/structures/ebf_ponder.snbt" />
  <ImportPonder src="/assets/ponders/ebf_ponder.json" />
</GameScene>

## <ItemImage id="gregtech:gt.blockmachines:1000"/> 工业高炉

```filetree
|-- **来源**：         [GregTech5u](https://github.com/GTNewHorizons/GT5-Unofficial/blob/master/src/main/java/gregtech/common/tileentities/machines/multi/MTEElectricBlastFurnace.java)
|-- **机器类型**：     高炉
|-- **阶段**：         [LV](./tier-lv-index.md)
|-- **详情**
|   |-- **尺寸**：                   3x3x4
|   |-- **能源仓**：                 普通
|   |-- **[超频](../../tierskipping-overcloking-parallels/overclocking.md)**：有损
|   \-- **污染**：                   400 gibbl/s
|-- [Wiki 页面](https://wiki.gtnewhorizons.com/wiki/Electric_Blast_Furnace)
\-- 任务：<QuestLink id="AAAAAAAAAAAAAAAAAAAATQ==" />
```

<ItemImage id="gregtech:gt.blockmachines:1000" /> **工业高炉**（**EBF**）是一台 [LV](./tier-lv-index.md) 阶段的[多方块机器](/gtnh-basics/multiblocks.md)，用于以高于普通熔炉的温度将粉末熔炼成锭。

它是 <ItemImage id="gregtech:gt.blockmachines:140" /> **砖高炉** 的直接升级版，因为它使用电力而不是可燃燃料，并且能够处理更高阶段的材料。

结构中的加热线圈决定机器的炉温上限，能源仓则决定供电电压。提升这两者，既能解锁新配方，也能让工业高炉进一步[超频](../../tierskipping-overcloking-parallels/overclocking.md)。

工业高炉也遵循多方块的通用规则：需要通过消声仓排放污染，会偶尔出现维护问题，并且在跳电时吞掉原料。物品和流体分别通过总线与仓室输入输出。

<RecipesFor id="gregtech:gt.blockmachines:1000" input="gregtech:gt.blockcasings:11" />

# 搭建

工业高炉的顶层和底层由 <ItemImage id="gregtech:gt.blockcasings:11" /> **耐热机械方块** 构成，中间两层则使用加热线圈。

加热线圈决定工业高炉的热容量，并且整台机器中的线圈必须是同一等级，结构才能成型。

总线和仓室只能替换底层的耐热机械方块，只有消声仓例外，它必须位于顶层中央。另一个例外是输出仓：放在底层时收集液体产物，放在顶层时收集气体产物。能够回收多少气体，取决于消声仓的等级。

工业高炉以能源仓的[电压阶段](../../power/voltage-tiers.md)运行；安装两只同级能源仓后，就能升压到下一阶段。

使用 <ItemLink id="structurelib:item.structurelib.constructableTrigger" showIcon="left" /> 可以投影或自动搭建结构；其中子信道 `coil` 用于指定加热线圈等级。

| 需求 |
|:-----|
| 1 个 <ItemImage id="gregtech:gt.blockmachines:1000" /> **工业高炉**（控制器） |
| 16 个 <ItemImage id="gregtech:gt.blockcasings5" /> **加热线圈**[^one] |
| 0-15 个 <ItemImage id="gregtech:gt.blockcasings:11" /> **耐热机械方块** |
| 1+ 个 <ItemImage id="gregtech:gt.blockmachines:41" /> **能源仓**（任意底层外壳） |
| 1 个 <ItemImage id="gregtech:gt.blockmachines:90" /> **维护仓**（任意底层外壳） |
| 1 个 <ItemImage id="gregtech:gt.blockmachines:91" /> **消声仓**（顶层中央外壳） |
| 0+ 个 <ItemImage id="gregtech:gt.blockmachines:71" /> **输入总线**（任意底层外壳） |
| 0+ 个 <ItemImage id="gregtech:gt.blockmachines:51" /> **输入仓**（任意底层外壳） |
| 0+ 个 <ItemImage id="gregtech:gt.blockmachines:81" /> **输出总线**（任意底层外壳） |
| 0+ 个 <ItemImage id="gregtech:gt.blockmachines:61" /> **输出仓**（任意顶层/底层外壳） |
[^one]: 这是一个**分级**部件。

> [!WARNING]
> 工业高炉不支持多安能源仓和激光靶仓。

## 共用

<GameScene interactive={true} width="240" height="240" zoom="1.2" wrap="square" align="right" >
  <ImportStructure src="/assets/structures/quad_ebf.snbt" />
  <ImportStructure src="/assets/structures/side_qebf.snbt" x="-8" />
  <RemoveBlocks id="Railcraft:residual.heat" />
</GameScene>

工业高炉的四个侧面都可以共用，以节省外壳、线圈和总线/仓室。

并排搭建、共享侧壁的工业高炉最常见也最值得推荐，因为它能大幅减少加热线圈消耗，降低增建新高炉的成本。

例如，四台并排共用的工业高炉总共只需要 42 个加热线圈，而不是完整独立搭建时的 64 个。它的主要缺点，是升级线圈时比较麻烦，因为所有被共用的线圈仍然必须保持同一等级，结构才会形成。

共用维护仓、输出总线和输入仓也很实用，但**不要**共用能源仓。工业高炉经常需要通过双仓升压到更高阶段，这会让两只能源仓吃满 4A；如果把这份输入再分给另一台机器，基本必然导致其中一台跳电。

如果你不想把物流放在机器正下方，也可以用扳手把控制器旋转 90 度，横着建造并排工业高炉，让所有总线和仓室更方便接触。

> [!CAUTION]
> GregTech 多方块有几种常见风险，会导致跳电甚至爆炸：
> * 不要让工业高炉淋雨。
> * 不要用方块、线缆或管道堵住消声仓。
> * 不要让能源仓承受超出其阶段的电压。
> * 整个配方期间都要保持供电稳定。
> * 如果开启了溢出保护，要保证输出空间足够。

# 使用

当结构成型且维护问题都处理完之后，工业高炉就可以投入使用了。不过此时虽然玩家通常只有 LV 能源仓，工业高炉却没有真正的 LV 配方；处理 <ItemImage id="gregtech:gt.metaitem.01:11305" /> 钢和 <ItemImage id="gregtech:gt.metaitem.01:11019" /> 铝至少都需要 MV 级功率。

解决办法是在结构里安装两只能源仓，让机器通过[超频](../../tierskipping-overcloking-parallels/overclocking.md)升到下一电压阶段。普通能源仓平时通常只会拉取 1A，但在这种场景下它们最多可拉取 2A。因此，两只能源仓合计可以拉取 4A LV，也就是相当于 1A MV。

想持续稳定地提供 4A 电流，附近至少需要四台[单方块](../../singleblock/index.md) <ItemImage id="gregtech:gt.blockmachines:1115" /> 蒸汽轮机。钢和铝的基础配方只需 120 EU/t，因此允许存在一定线损，但余地并不大。

下面给出两种常见的供电方式。两种方式都默认你**没有**使用超导线，因为超导线无论距离和安培数如何都没有线损。

## 方案一：尽量压低线损

<GameScene interactive={true} width="240" height="240" zoom="1.5">
  <ImportStructure src="/assets/structures/powering_ebf_1.snbt" />
  <RemoveBlocks id="Railcraft:residual.heat" />
</GameScene>

把<u>四台</u>蒸汽轮机尽量贴近能源仓摆放。

* 只需要四台蒸汽轮机。
* 基本不能顺手再带其他机器。
* 线损最低。

## 方案二：用电池箱缓冲线损

<GameScene interactive={true} width="240" height="240" zoom="1.5">
  <ImportStructure src="/assets/structures/powering_ebf_2.snbt" />
  <RemoveBlocks id="Railcraft:residual.heat" />
</GameScene>

在能源仓附近放一个 4 格或以上的 <ItemImage id="gregtech:gt.blockmachines:171" /> **电池箱**，用更多蒸汽轮机来补偿线损。

* 需要五台或更多蒸汽轮机。
* 还要准备电池和大电流线缆。
* 可以顺便给其他机器供电。
* 总线损更高。

## 热容量

结构中的加热线圈决定工业高炉的热容量，也就决定了它能运行哪些配方。用 <ItemImage id="gregtech:gt.metaitem.01:32762" /> **便携式扫描仪** 右键控制器，可以查看当前热容量；在 [NEI](/introduction/introduction-index.md) 中则可以看到每个配方要求的最低热容量。

例如，白铜线圈工业高炉的热容量为 1,801K，足够熔炼钢（1,000K）和铝（1,300K），但**不足以**处理 <ItemImage id="gregtech:gt.metaitem.01:11856" /> 太阳能级硅（2,273K）。此外，从 MV 往上，每高一个电压阶段，还会额外获得 +100K 的炉温奖励，如下图所示：

<LineChart title="Heat Bonus" categories="LV,MV,HV,EV,IV,LuV,ZPM,UV,UHV,UEV,UIV,UMV,UXV,MAX,MAX+" yAxisUnit="K" width="600">
  <Series name="Heat" data="0,0,100,200,300,400,500,600,700,800,900,1000,1100,1200,1300" color="#E15759"/>
</LineChart>

当机器热容量高于配方最低要求时，会获得两种独立收益。第一种是每高出 900K，就获得一次 **5% 乘算耗电减免**。第二种是每高出 1,800K，就把一次有损超频转化为一次[无损超频](../../tierskipping-overcloking-parallels/overclocking.md#perfect-overclocking-44)。后者尤其强，因为工业高炉默认只会进行有损超频。

> [!NOTE]
> *有损超频*：功率 4 倍，速度 2 倍（4/2）。
> *无损超频*：功率 4 倍，速度 4 倍（4/4）。

例如，用 HV 电力和 <ItemImage id="gregtech:gt.blockcasings5:2" /> **镍铬合金线圈** 来熔炼 <ItemImage id="TConstruct:materials:12" /> **生铝**（1,300K）。使用氮气时，该配方基础耗能为 144,000 EU，耗时 60 秒，也就是 120 EU/t。此时工业高炉热容量为 3,701K，正好比配方最低需求高出 2,401K，因此能获得两次 5% 耗电减免和一次无损超频。最终结果是总耗能只有 130,200 EU，耗时 15 秒，功率约为 `120 EU/t x 0.95 x 0.95 x 4 = 434 EU/t`。

> [!TIP]
> * 工业高炉可以安装不止一个输入总线/输入仓，这对于存放氢气、氧气、氮气、氦气等多种输入流体很有帮助。解锁 EV 后，四联输入仓尤其好用。
> * 随着需求增加，强烈建议多建几台工业高炉。GTNH 故意把很多配方做得很慢，就是为了推动你扩张基础设施。
> * 同一种材料往往不止一个高炉配方，记得定期在 [NEI](/introduction/introduction-index.md) 里翻一翻。例如大多数锭都能使用不同惰性气体来加速熔炼，而钢也可以用熟铁粉配方来大幅降低时间和能耗。
> * 一台使用熟铁粉配方并由 MV 供电的工业高炉，做钢的速度大约相当于 48 台砖高炉，而且还能继续超频。

# 故障排查

## 结构不完整

先检查最低搭建要求是否满足：外壳数量、一个维护仓、一个消声仓，以及至少一个能源仓。如果这些都没问题，就在控制器 GUI 里手动触发一次结构检查。还要确认机器内部没有塞进任何本不该存在的方块，例如不可见光源。

## 无法启动

先确认配方是否正确，包括物品、流体和编程电路。再检查消声仓是否被方块、线缆或管道堵住。这个问题有时也可能单纯是完全没供上电，因此还要检查电线是否接好、蒸汽轮机朝向是否正确。

## 运行一瞬间后停机并吞料

先检查供电是否足够。常见原因是线损过高，或者蒸汽轮机数量不够。若使用进阶消声仓，还要确认其中装有空气滤网。

## 输出空间不足

检查输出总线/输出仓是否已经满了。也有可能是该配方还会产生气体，而气体输出必须从**顶层**输出仓排出；液体输出则必须走**底层**输出仓。如果某一种副产物并不重要，也可以考虑开启物品、流体或双重溢出销毁。

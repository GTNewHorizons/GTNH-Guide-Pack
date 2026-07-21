---
navigation:
  parent: /items-blocks-index.md
  title: 合成存储器（存储器/协处理器/监控器/单元）
  icon: appliedenergistics2:tile.BlockSingularityCraftingStorage
categories:
- devices
item_ids:
- appliedenergistics2:tile.BlockCraftingUnit
- appliedenergistics2:tile.BlockCraftingMonitor
- appliedenergistics2:tile.BlockCraftingUnit:1
- appliedenergistics2:tile.BlockCraftingUnit:2
- appliedenergistics2:tile.BlockCraftingUnit:3
- appliedenergistics2:tile.BlockAdvancedCraftingUnit:0
- appliedenergistics2:tile.BlockAdvancedCraftingUnit:1
- appliedenergistics2:tile.BlockAdvancedCraftingUnit:2
- appliedenergistics2:tile.BlockAdvancedCraftingUnit:3
- appliedenergistics2:tile.BlockCraftingStorage
- appliedenergistics2:tile.BlockCraftingStorage:1
- appliedenergistics2:tile.BlockCraftingStorage:2
- appliedenergistics2:tile.BlockCraftingStorage:3
- appliedenergistics2:tile.BlockAdvancedCraftingStorage
- appliedenergistics2:tile.BlockAdvancedCraftingStorage:1
- appliedenergistics2:tile.BlockAdvancedCraftingStorage:2
- appliedenergistics2:tile.BlockAdvancedCraftingStorage:3
- appliedenergistics2:tile.BlockSingularityCraftingStorage
---

# 合成CPU多方块结构（存储器/协处理器/监控器/单元）

<GameScene width="350" height="220" zoom="4" background="transparent">
  <ImportStructure src="../assets/structures/crafting_cpus.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

<Row>
  <BlockImage id="appliedenergistics2:tile.BlockCraftingStorage:1" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockCraftingUnit:1" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockCraftingMonitor" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockCraftingUnit:0" scale="4" />
</Row>

合成CPU负责管理[自动合成](../ae2-mechanics/autocrafting.md)任务，存储中间产物并影响合成规模与效率。每个CPU同时只能处理一个任务，多个任务需要多个CPU结构。

## 核心功能

* 存储合成过程的中间产物
* 通过右键点击查看合成进度
* 可配置接收玩家请求/自动化请求/二者兼有
* 最低配置：单个1k合成存储器

## 构造规则

必须构建为无空隙的实心长方体结构，至少包含1个合成存储器组件。

---

# 合成单元

<BlockImage id="appliedenergistics2:tile.BlockCraftingUnit" scale="4" />

（可选）用于填充CPU结构空间，也是其他组件的合成原料。

<RecipeFor id="appliedenergistics2:tile.BlockCraftingUnit" />

---

# 合成存储器

<Row>
  <BlockImage id="appliedenergistics2:tile.BlockCraftingStorage:0" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockCraftingStorage:1" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockCraftingStorage:2" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockCraftingStorage:3" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockAdvancedCraftingStorage:0" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockAdvancedCraftingStorage:1" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockAdvancedCraftingStorage:2" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockAdvancedCraftingStorage:3" scale="4" />
</Row>

（必需）提供1k/4k/16k/64k/256k存储容量，决定CPU可处理的合成任务复杂度。

<Column>
  <Row>
    <RecipeFor id="appliedenergistics2:tile.BlockCraftingStorage:0" />

    <RecipeFor id="appliedenergistics2:tile.BlockCraftingStorage:1" />

    <RecipeFor id="appliedenergistics2:tile.BlockCraftingStorage:2" />

    <RecipeFor id="appliedenergistics2:tile.BlockCraftingStorage:3" />
  </Row>

  <Row>
    <RecipeFor id="appliedenergistics2:tile.BlockAdvancedCraftingStorage" />

    <RecipeFor id="appliedenergistics2:tile.BlockAdvancedCraftingStorage:1" />

    <RecipeFor id="appliedenergistics2:tile.BlockAdvancedCraftingStorage:2" />

    <RecipeFor id="appliedenergistics2:tile.BlockAdvancedCraftingStorage:3" />
  </Row>
</Column>

---

# 并行处理单元

<BlockImage id="appliedenergistics2:tile.BlockCraftingUnit:1" scale="4" />

（可选）提升<ItemLink id="appliedenergistics2:tile.BlockInterface" />的原料分发频率，适配高速处理设备（如被多个<ItemLink id="appliedenergistics2:tile.BlockMolecularAssembler" />环绕的样板供应器）。

<RecipeFor id="appliedenergistics2:tile.BlockCraftingUnit:1" />

---

# 合成监控器

<BlockImage id="appliedenergistics2:tile.BlockCraftingMonitor" scale="4" />

（可选）显示当前CPU处理的合成任务，支持<ItemLink id="appliedenergistics2:item.ToolColorApplicator" />染色。

<RecipeFor id="appliedenergistics2:tile.BlockCraftingMonitor" />
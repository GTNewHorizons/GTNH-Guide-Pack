---
navigation:
  parent: /items-blocks-index.md
  title: 破坏面板
  icon: appliedenergistics2:item.ItemMultiPart:300
categories:
- devices
item_ids:
- appliedenergistics2:item.ItemMultiPart:300
- appliedenergistics2:item.ItemMultiPart:301
---

# ME破坏面板

<GameScene zoom="8" background="transparent" interactive={false}>
<ImportStructure src="../assets/structures/annihilation_plane.snbt" />
</GameScene>

ME破坏面板具备破坏方块与收集物品的功能，其工作原理类似<ItemLink id="appliedenergistics2:item.ItemMultiPart:240" />，将物品存入[网络存储](../ae2-mechanics/import-export-storage.md)。物品需接触面板正面方可被收集，不作用于区域范围。

可为其附加镐类附魔：时运附魔可用于[自动化矿物处理](../example-setups/ore-fortuner.md)（需整合包支持）；精准采集按预期工作；效率降低能耗；耐久提供免耗能概率。

属于[线缆组件](../ae2-mechanics/cable-subparts.md)。

**请确保在领地插件中启用假人权限**

## 过滤机制

仅当破坏产物可存入网络时，破坏面板才会执行操作。通常需构建[子网](../ae2-mechanics/subnetworks.md)，通过<ItemLink id="appliedenergistics2:item.ItemMultiPart:220" />或[存储元件](../items-blocks/storage_cells.md)[分区](cell_workbench.md)实现过滤。

<GameScene width="300" height="200" zoom="6" interactive={true}>
  <ImportStructure src="../assets/structures/annihilation_filtering.snbt" />

  <DiamondAnnotation pos="1 0.5 0.5" color="#00ff00">
        过滤目标方块的掉落物
  </DiamondAnnotation>

  <DiamondAnnotation pos=".5 0.5 2.5" color="#00ff00">
        对掉落物进行存储分区
  </DiamondAnnotation>

  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

过滤依据为*最终掉落物*。例如要过滤破坏<ItemLink id="etfuturum:amethyst_cluster_2:6" />，需为面板附加精准采集，否则未成熟阶段无掉落物时将不受限制。

## 合成配方

<RecipeFor id="appliedenergistics2:item.ItemMultiPart:300" />

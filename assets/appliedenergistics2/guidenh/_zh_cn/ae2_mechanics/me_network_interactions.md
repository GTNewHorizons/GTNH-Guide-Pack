---
navigation:
  parent: /ae2_mechanics_index.md
  title: 网络之间的交互
  icon: appliedenergistics2:item.ItemMultiPart:16
---

# 网络交互

# 独立的 ME 网络
在原版 AE2 中，一个 ME 网络是由[线缆](./channels.md)和其他可传递频道的部件连接起来的一组设备。理论上，哪怕只有一根线缆，也可以算是一个网络。

一个 ME 网络最关键的特征，就是它所有的线缆和设备都从同一组控制器获取[频道](./channels.md)。

由此可以推导出：如果两个网络之间没有通过线缆或其他可传递频道的设备直接连接，它们就不会彼此传递频道，可以视为彼此独立的 ME 网络。

* 很自然地，两个物理上相距很远、且没有通过[无线接入器](../items_blocks/wireless_connectors.md)或[量子环](./quantum_bridge.md)连接的网络，彼此独立。
* 两个只通过 <ItemLink id="appliedenergistics2:item.ItemMultiPart:140" showIcon="left"/> 或 <ItemLink id="appliedenergistics2:item.ItemMultiPart:120" showIcon="left"/> 连接的 ME 网络，也同样视为独立网络。石英纤维只传递能源不传递频道，而线缆锚既不传递能源也不传递频道，仅用于隔开相邻线缆。不同颜色的线缆之间同样不会连接，详见[频道](./channels.md)。

# 网络之间的交互
网络除了相互独立，还可以产生相互联系，这种联系可以非常多样化与灵活，是绝大多数AE自动化系统的基础。广义上，只要两个独立的ME网络发生了互相的影响，就可以视作网络交互，[P2P](./p2p_tunnels.md)中利用MEP2P通道传递频道就是一种网络交互。ME网络之间的交互基本依赖于[接口](../items-blocks/interface.md)与[存储总线](../items-blocks/storage_bus.md)。二者的特性给了网络交互中不同网络不同的地位。

> 另见：[子网络](./subnetworks.md)

ME 网络之间的交互，主要依赖于 [ME接口](../items_blocks/interface.md) 和 [ME存储总线](../items_blocks/storage_bus.md)。正是它们的工作方式，决定了不同网络在交互中的分工。

通常来说，两个ME网络有以下结构。

<GameScene zoom="4" width="400" rotateY={0} rotateX={0}>
  <ImportStructure src="../assets/structures/network_interaction_basic_interacton.snbt" />
</GameScene>

由于 ME接口 和 ME存储总线 的工作机制，蓝色网络通常是被访问的一方，白色网络通常是主动访问的一方。在这种结构里，白色网络会把蓝色网络当成一个大型“容器”，从而对它进行[读取或写入](./import_export_storage.md)。

## 嵌套交互
上文中的结构可以套娃，构成层层嵌套的形式，但需要注意这种形式适用范围较窄，不当的使用将会造成极大的硬件资源消耗！

<GameScene zoom="3" width="400" rotateY={0} rotateX={0}>
  <ImportStructure src="../assets/structures/network_interaction_nesting_interacton.snbt" />
</GameScene>

## 网络互读
当两个网络通过存储总线可以互相读取内容时，就代表这两个ME网络互读了，互读有时是一种技术性调整方案以满足某些特殊需求，但绝大多数情况下互读只会造成资源存储的混乱，并且会严重影响游戏性能。

<GameScene zoom="3" width="400" rotateY={0} rotateX={0}>
  <ImportStructure src="../assets/structures/network_interaction_network_read.snbt" />
</GameScene>

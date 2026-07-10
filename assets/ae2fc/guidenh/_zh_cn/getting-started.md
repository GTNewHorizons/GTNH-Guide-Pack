---
navigation:
  parent: index.md
  title: 快速开始
  icon: appliedenergistics2:item.ItemMultiMaterial:1
  position: 99
---

# AE2 Fluid Crafting Rework

# 前言
每个人都喜欢AE2的自动合成，但AE2在1.16以及之前都不支持直接以流体为有效的合成材料，因此必须将流体放入容器中或使用虚拟物品来编辑配
方。这导致涉及流体的AE合成总是让低版本玩家苦不堪言。
不过，现在时代变了！使用AE2FluidCrafting，你将可以自由使用流体配方。

# 用法

在你的网络里连接上一个~~ME流体离散器(MEFluidDiscretizer)~~，就可以让ME系统在合成时识别流体原料。
在ME流体样板终端(MEFluid PatternTerminal)里编写样板。带有流体原料的样板会变为特殊的编码样板(Encoded Pattern)。
把编写的样板放进接口，带流体的样板要放进ME二合一接口(MEDual Interface)。
就这样，现在试试请求合成吧。

# 额外补充

虽然本模组的前置中并没有NEI/JEI，但支持它们自动填充流体样板，为了更方便地编码流体，推荐和NEI/JEI一同使用。

# 1.7.10

兼容任何版本的AE2(应用能源2和应用能源2非官方版都有效）。
另有一个GTNH特供版的AE2流体合成套件重置GTNH版，仅兼容应用能源2非官方版。
特供版拥有[EC2]更多存储单元2的全部功能，并且优化更好，其还移植了部分LazyAE2的部分功能。
因此更加推荐使用此版本。
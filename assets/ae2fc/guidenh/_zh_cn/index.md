---
navigation:
  title: AE2流体合成套件重置（AE2 Fluid Crafting Rework）
  icon: guidenh:guide
  position: 49
  
  item_ids:
  - guidenh:guide
---

# 什么是AE2流体合成套件重置（AE2 Fluid Crafting Rework）？

# AE2流体合成套件重置（AE2 Fluid Crafting Rework）？


由Prim制作的AE附属模组(~~击毙EC2的一把好手~~)，模组加入了大量便于进行流体合成的方块和物品，包括流体终端、原材料缓存仓、ME二合一接口、~~ME流体离散器~~等。
现版本已支持waila显示速度,流体储量,具体以waila为准

- [快速开始](getting-started.md)
- [物品与方块](items-blocks-index.md)
- [AE2 机制](ae2-mechanics/ae2-mechanics-index.md)
- [技巧与实用实例](tricks-example.md)

# 怎么使用本指南

- 将鼠标移至最左侧从导航栏中寻找更多内容。
- 许多页面有像下面一样的可交互场景，你可以：
  - 用鼠标左键旋转，右键平移场景，使用鼠标滚轮或侧面的按钮放大缩小或重置场景。
  - 使用侧面的按钮开关网格。
  - 使用侧面的按钮开关方块统计，点击统计中的物品会高亮场景中的相同物品。
  - 将鼠标放置在场景的方块上可以查看方块tooltip。
  - 将鼠标放置在场景的各种高亮注解（菱形注解、线注解、方块注解等）上可以查看注解的内容。

<GameScene zoom="4" interactive={true}>
  <ImportStructure src="assets/structures/autocraft_setup_greebles.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
  <BlockAnnotation pos="2 0 2" color="#ff0000" alwaysOnTop={true}>
  这是一个红色高亮方块注解。
  </BlockAnnotation>
  <BoxAnnotation min="5 4 2" max="6 3 4" color="#00ff2f" thickness="0.8">
  这是一个绿色盒子注解。
  </BoxAnnotation>
  <LineAnnotation from="7 1 2" to="7 4 2" color="#FFD24C" thickness="0.8">
  这是一根黄色线注解。
  </LineAnnotation>
  <DiamondAnnotation pos="3.5 2.5 2.5" color="#0400ff">
  这是一个蓝色菱形注解。
  </DiamondAnnotation>
  <TextAnnotation pos="0.5 2 2.5" color="#00ffcc">
  这是一个青色文本气泡
  </TextAnnotation>
</GameScene>

---
navigation:
  title: Ponder调试
  position: 200
---

<GameScene zoom="2" width="400" height="200" rotateY={200} offsetX={-120} offsetY={-60}  allowLayerSlider={false}>
    <ImportStructure src="../assets/structures/spatial_io-dimension.snbt" />
    <BoxAnnotation min="-3 2 -2" max="-6 5 1" color="#EE3333" thickness="1">
    空间存储元件维度
    </BoxAnnotation>
    <ImportPonder src="/assets/ponder/spatial_io-dimension.json" />
</GameScene>

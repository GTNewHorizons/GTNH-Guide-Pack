---
navigation:
  parent: ../ae2-mechanics-index.md
  title: ME网络连接
  icon: appliedenergistics2:item.ItemMultiPart:16
quest_ids:
  - AAAAAAAAAAAAAAAAAAAFMQ==
  - tM8pT_W3RCqZNDAovERxFg==
---

# ME网络连接

# 什么是独立的AE网络？
在AE2原版的定义中，一个AE网络是由通过可以传递频道的[线缆](./channels.md)与设备连接的设备组。理论上讲讲，一根线缆就可以是一个网络。设备与线缆在一个AE网络内的特征是它们都从同一组控制器获取[频道](./channels.md)。

由上文可以推导出来，不经由线缆与设备相互连接的网络互相不传递频道，被视为两个独立的AE网络。

* 很自然的，在物理上相隔甚远并且没有经过[无线接入器](../items-blocks/wireless_connectors.md)或[量子环](./quantum-bridge.md)连接的两个网络是独立的。
* 两个仅由<ItemLink id="appliedenergistics2:item.ItemMultiPart:140" showIcon="Left"/>或<ItemLink id="appliedenergistics2:item.ItemMultiPart:120" showIcon="Left"/>连接的AE网络也被视为两个独立的网络，因为石英纤维只传导能量而不传导频道、线缆锚则既不传导能量也不传导频道，仅用作分隔两根相邻的线缆（不同颜色的线缆不会相互连接，具体特性查看[线缆](./channels.md)）。

# 网络连接
## 有线连接
* 同一个AE网络里的设备可以通过线缆传递频道有线连接、也可以通过设备本身向其相邻的线缆与设备传递频道。通过设备最多可以传递8个频道，等效与普通线缆。

* 通过P2P通道 - ME可以传递频道进行有线连接。具体信息参考[P2P](./p2p_tunnels.md)。

* 在GTNH中，ME仓室(<ItemLink id="gregtech:gt.blockmachines:2718" showIcon="Left"/>、<ItemLink id="gregtech:gt.blockmachines:2717" showIcon="Left"/>、<ItemLink id="gregtech:gt.blockmachines:2710" showIcon="Left"/>或<ItemLink id="gregtech:gt.blockmachines:2713" showIcon="Left"/>等)可以通过使用<ItemLink id="gregtech:gt.metatool.01:26" showIcon="Left"/>右键打开临近连接模式，这样它们就可以像AE设备一样向临近的其他ME仓室或AE设备、线缆传递频道。这种连接方式同样最多传递8个频道。

## 无线连接
* GTNH中加入了AE2 Stuff模组，其中提供了<ItemLink id="ae2stuff:Wireless" showIcon="Left"/>与<ItemLink id="ae2stuff:Wireless:17" showIcon="Left"/>，每对可以无线传递最多32个频道，<Color id="RED">不能跨维度连接</Color>，使用<ItemLink id="ae2stuff:WirelessKit" showIcon="Left"/>与<ItemLink id="ae2stuff:AdvWirelessKit" showIcon="Left"/>可以将它们配对。前者为1对1连接，后者像[P2P通道](./p2p_tunnels.md)一样可以一对多连接。无线接入器在刚刚建立AE网络的电压阶段可能对电网造成很大负担，请提前计算耗电。具体信息参考任务书页面《<QuestLink id="AAAAAAAAAAAAAAAAAAAFMQ==" show_tooltip="false" />》


* AE2原版提供了一种无线连接网络的方式————量子环，每对可以无线传递最多32个频道，<Color id="GREEN">可以跨维度连接</Color>，具体用法参考[量子环](./quantum-bridge.md)页面。

* <ItemLink id="RIO:tile.remote_interface" showIcon="Left"/>是RemoteIO模组中的方块。远程接口类似矢量变幻接口/幻灵接口，可以远程代理一个方块，代理时其拥有目标方块的所有功能，<Color id="GREEN">可以跨维度连接</Color>，其造价在跨空间组网方案中科技要求最高，要求能够制作<ItemLink id="dreamcraft:CircuitIV" showIcon="Left"/>与<ItemLink id="gregtech:gt.metaitem.01:32654" showIcon="Left"/>。
  * 手持<ItemLink id="RIO:item.chip.location" showIcon="Left"/>（合成时电路板需冲压为任意电路板）,Shift+右键点击ME控制器。
  * 在目的地放置远程接口，手持定位芯片，右键点击接口方块，载入目标。
  * 手持<ItemLink id="RIO:item.chip.transfer:20" showIcon="Left"/>右键远程接口。操作完后远程接口即可传输频道 

---
description: >-
  当应用发布并安装到影见设备之后可能会出现各种难以排查的异常，这时候你就需要使用远程调试功能，远程调试功能会将影见设备当前的应用数据同步到UnityEditor中，便于开发者进行调试。
---

# 教程3：使用远程调试功能

使用方法如下：

1. 启用“远程调试”功能：

        在开发者工具窗口中，设置页面启用远程调试功能，如下图：

![](https://lh6.googleusercontent.com/CIB0ophh5MYNBdvamZPnRWviYgqx1xmB2I4Jf7FxseMUv5CXatwhJIGgBmj6C858Gb-6zWyoiM9CbxDz6HZqn8n5g-VVG-ynhOLti46iS5RqzqNiecqSwe1u1bwR5gMgGhD1lNHg)

2. 配置ip及端口号

当启用远程调试功能后，场景中的AURA\(Clone\)物体上将会出现RemoteDebug组件，如下图。将开发者电脑的局域网ip输入ip文本框内，port文本框中可输入开发者电脑中任意未被占用的端口号。

![](https://lh5.googleusercontent.com/7TWdCkmt-9Sw4vzHoic43mdzJc5WKNDmCK_bhUUICrg6DGIxCjdvL15g5MN4r2OMCaBw4F9HHK79gLvMe7eXeVPJn40JVq65JXwcfe6PqAuPMpFlDrGiihzFxAl0NBjP8K0tAqSI)

3. 发布应用并安装到影见设备中

4. 确保影见设备和开发者电脑连入同一个局域网

5. 在影见上运行刚刚安装的应用

6. 在UnityEditor中运行工程

7. 当前已经进入了远程调试模式，可以放置模具开始调试

_**注意：如果按照上面的步骤操作后，UnityEditor中并没有与影见端联动（联动的效果如下图所示，Game视图左侧会有数据显示），请确保开发者电脑的防火墙已关闭，并重新执行第4-6步操作。**_

![](https://lh5.googleusercontent.com/Hle_njNAdtmi2i5_iFnkfhzoQ-_7N7qoUGKrWqfPMsOTWohF0W2lem2B6RSow1Ja0aMyw06KUaM95bTApYP4VXIG7XxV_f8gzQAx2n2_xSwrNvsf9as5SesgHdweCQC_zQ_QNaU6)

  



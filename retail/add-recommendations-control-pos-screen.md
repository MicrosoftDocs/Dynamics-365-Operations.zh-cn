---
title: "添加一控件。建议在 POS 设备的交易记录页"
description: "本主题介绍 Microsoft Dynamics 365 中介绍如何向添加建议控制到已销售点 (POS) 设备的屏幕交易记录使用屏幕布局设计器操作。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2377b1639a3c95fe6bba4754c4069cc12043e3d3
ms.lasthandoff: 03/31/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>添加一控件。建议在 POS 设备的交易记录页

本主题介绍 Microsoft Dynamics 365 中介绍如何向添加建议控制到已销售点 (POS) 设备的屏幕交易记录使用屏幕布局设计器操作。

如果某工序时，可以使用 Microsoft Dynamics 365 可以查看有关您的设备 POS 产品的建议。 *Recommendations*是物料基于的采购历史记录、为感物料兴趣其利息和物料可以是客户的在线购买和其他客户砖在和泥商店。 使用屏幕布局设计器，为了查看产品建议，您需要添加交易记录控制到屏幕。

## <a name="open-layout-designer"></a>打开设计器版式
1.  **是零售和商务** &gt; **的设置渠道** &gt; **的设置 POS ** &gt; ** ** &gt; ** ** POS 屏幕布局。
2.  使用快速查找要添加筛选器屏幕控制。 例如，可筛选**屏幕布局 ID **值，使用“F2CP16 字段：9M”。
3.  在列表中，找到并选择所需记录。 例如，选择“名称：F2CP16: 9M 屏幕布局 ID:F2CP16: 9M”。
4.  **单击"设计器**版式。
5.  按照提示启动布局设计器。 在提示输入凭据，请输入正在使用的相同凭据，在屏幕布局设计器版式从** **页开始。
6.  在登录时，这个页面类似于下面。 布局根据为您的商店进行的自定义将不同。

[] (![screenlayout PIC 1![。/media/screenlayout PIC1.png)](。/media/screenlayout PIC 1.png 选择显示选项)
-----------------------

有以下两个的配置选项。 选择在您的商店的最佳的选项，并且按照剩余的说明完成设置控制。 两个选项如下：
-   建议始终可见的。
-   A ** **建议选项卡显示在网格以在屏幕的权限。

#### <a name="to-make-recommendations-always-visible"></a>为其提供建议始终可见

1.  减少交易记录行明细信息"区域的高度、高度和客户，以便其在左侧面板相同。[] (。/media/picture-2.png)![[] (screenlayout PIC 2 /media/picture-2.png。/media/screenlayout PIC2.png)](。/media/screenlayout PIC2.png)
2.  从左侧的菜单，请拖放建议用于控制针对在交易记录行明细信息"区域和中心在底部的按钮网格间屏幕的交易记录。 尺寸调整更改它成为该空格的控制。[] (。/media/picture-3.png)![[] (screenlayout PIC 3 /media/picture-3.png。/media/screenlayout PIC3.png)](。/media/screenlayout PIC3.png)
3.  ** X **单击"保存并退出该布局设计器"。
4.  在工序的 Dynamics 365，为**零售和商务** &gt; **零售 IT ** &gt; ** **分配计划。
5.  在"列表，选择 1090 ** **登记。
6.  单击** **立即运行。

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>添加建议选项卡上分配给按钮网格以在屏幕的权限

1.  右键单击在空白间距低于在仅在右侧的页面中的按钮网格的最后一选项卡下。
2.  **自定义**请单击。[] (![图片。/media/picture-5.png)](。/media/picture-5.png)
3.  单击** **新的选项卡。
4.  查找您添加的新的选项卡。 您可能需要下移。
5.  **在下拉选择** **内容，建议的产品**。 [] (![图片。/media/picture-6.png)](。/media/picture-6.png)
6.  **在标签** "字段中，键入名称。建议选项卡。 例如，键入“建议的产品”。
7.  ** **在"图像"字段中，选择该图像出现在"选项卡。
8.  Click **OK**. 将出现新的选项卡显示按钮网格。
9.  ** X **单击"保存并退出该布局设计器"。
10. 在工序的 Dynamics 365，为**零售和商务** &gt; **零售 IT ** &gt; ** **分配计划。
11. 在"列表，选择 1090 ** **登记。
12. 单击** **立即运行。


<a name="see-also"></a>请参阅
--------

[个性化的产品建议概览] (产品 recommendations.md 个性化)



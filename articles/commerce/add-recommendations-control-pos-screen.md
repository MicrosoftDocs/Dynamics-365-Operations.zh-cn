---
title: 向交易记录屏幕添加建议
description: 此主题介绍如何使用 Microsoft Dynamics 365 Commerce 中的屏幕布局设计器，向销售点 (POS) 设备的交易记录屏幕添加建议控件。
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 760e6e093dbe0ba6b2781f90af7fbb614c492b93
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454571"
---
# <a name="add-recommendations-to-the-transaction-screen"></a>向交易记录屏幕添加建议

[!include [banner](includes/banner.md)]


此主题介绍如何使用 Microsoft Dynamics 365 Commerce 中的屏幕布局设计器，向销售点 (POS) 设备的交易记录屏幕添加建议控件。 有关产品建议的详细信息，请参阅[“POS 中的产品建议”一文](product.md)。


使用 Commerce 时，可以在 POS 设备上显示产品建议。 若要显示产品建议，需要使用屏幕布局设计器向交易记录屏幕添加控件。 

## <a name="open-layout-designer"></a>打开布局设计器

1. 转至 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS** &gt; **屏幕布局**。
2. 使用快速筛选查找要为其添加控件的屏幕。 例如，使用值 **F2CP16:9M** 在**屏幕布局 ID** 字段中筛选。
3. 在列表中，找到并选择所需记录。 例如，选择**名称: F2CP16:9M 屏幕布局 ID: F2CP16:9M**。
4. 单击**布局设计器**。
5. 按照提示启动布局设计器。 在提示输入凭据时，输入从**屏幕布局**页启动布局设计器时使用的相同凭据。
6. 在登录时，将显示如下页面。 布局将由为您的商店执行的自定义决定。


    [![布局设计器](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>选择显示选项

可用配置选项有两个。 选择最适合您的商店的选项，然后按照其余说明完成控件的设置。 这两个选项是：

- 始终显示建议。
- 在屏幕右侧的网格中显示**建议**选项卡。

### <a name="make-recommendations-always-visible"></a>始终显示建议


1. 缩小交易记录行明细区域的高度，使其与其左侧的客户面板高度相同。


    [![减少的交易记录行详细信息区域高度](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. 将建议控件从左侧菜单拖放到交易记录屏幕底部中央的交易记录行明细与按钮窗格之间。 调整控件大小，使其适合该空间。

    [![添加到布局中的建议控件](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)


3. 单击 **X** 保存并退出布局设计器。
4. 在 Commerce 中，转至 **Retail 和 Commerce** &gt; **Retail 和 Commerce IT** &gt; **分配计划**。
5. 在列表中，选择 **1090 收银机**。
6. 单击**立即运行**。


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>向屏幕右侧的按钮网格添加“建议”选项卡

1. 在页面右侧按钮网格中最后一个选项卡下空白区域中右键单击。

2. 单击**自定义**。

    [![自定义 - 选项卡控件对话框](./media/pic-5.png)](./media/pic-5.png)

3. 单击**新建选项卡**。
4. 找到刚添加的新选项卡。 您可能需要向下滚动。
5. 在**目录**下拉菜单中，选择**建议的产品**。

    [![在“目录”字段中选择“建议的产品”](./media/pic-6.png)](./media/pic-6.png)

6. 在**标签**字段，键入建议选项卡的名称。例如，键入“建议的产品”。
7. 在**图像**字段中，选择要在该选项卡上显示的图像。
8. 单击 **确定**。 将在按钮网格中显示新选项卡。
9. 单击 **X** 保存并退出布局设计器。
10. 在 Commerce 中，转至 **Retail 和 Commerce** &gt; **Retail 和 Commerce IT** &gt; **分配计划**。
11. 在列表中，选择 **1090 收银机**。
12. 单击**立即运行**。

## <a name="additional-resources"></a>其他资源

[产品建议概览](product-recommendations.md)

[在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage](enable-adls-environment.md)

[启用产品建议](enable-product-recommendations.md)

[启用个性化建议](personalized-recommendations.md)

[选择退出个性化产品建议](personalization-gdpr.md)

[在 POS 上添加产品建议](product.md)

[调整 AI-ML 建议结果](modify-product-recommendation-results.md)

[手动创建策划的建议](create-editorial-recommendation-lists.md)

[使用演示数据创建建议](product-recommendations-demo-data.md)

[产品建议常见问题](faq-recommendations.md)

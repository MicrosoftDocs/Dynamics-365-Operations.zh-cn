---
title: "Microsoft Dynamics 365 的现有库存量将工作区应用的工序"
description: "现有库存量将工作区可帮助您和任何时候任何位置了解到移动预留和可用库存。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 85058f55-e566-40e2-9234-42d3e4fe5ff6
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 2ad48765528e1d1c6e7c90417b54a248ec79f546
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Microsoft Dynamics 365 的现有库存量将工作区应用的工序

现有库存量将工作区可帮助您和任何时候任何位置了解到移动预留和可用库存。 

<a name="prerequisites"></a>先决条件
-------------

| 必备项                                                         | 说明                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 工序闻悉移动电话平台的 Microsoft Dynamics 365 | 工序将 [] (/dynamics365/operations/dev 平台的 itpro/mobile apps/mobile 平台 Dynamics /dynamics365/operations/dev)                                   |
| 工序的 Dynamics 365                                          | 具有操作平台的更新版本的工序 3 的环境 (2016 年 11 月 Microsoft Dynamics 365 和 Microsoft Dynamics 1611) |
| 3215650 KB 修补程序                                                    | 修补程序安装可以在您的 Microsoft Dynamics 365 中提供。工序的工作区。                                       |
| 安装了工序的 Dynamics 365 应用的移动设备 | 下载工序的 Dynamics 365 应用从您所移动应用商店。                                                                           |

## <a name="introduction"></a>简介
通常，公司在此期间中每天有多个装运和库存多个收货。 这些更改通常更改现有库存量状态。 现有库存量将工作区能让您看到现有库存量，跨公司状态，以便您可以了解最新的成在您所移动设备) 库存数据。 无论您是该仓库，采购，销售、制造或管理工作或者具有其他角色，您可以任何时候和任何位置访问现有库存量数据。 将工作区提供现有量状态的即时一视图跨设施上，让您查看在当前预留设施、材料和未预留的现有库存量中的现有库存量。 还可以输入物料编号查询现有库存量，并执行现有产品或款式的已筛选的搜索。 具体而言，该工作区提供这些功能：

-   您可以搜索副产品编号或产品名称查找产品查看现有库存量为状态。
-   对于所选产品，可以查看以下信息：
    -   现有库存量按站点
    -   现有库存量按仓库
    -   现有库存量按位置
    -   现有库存量按批次 (为批次控制产品)
    -   现有库存量按库存状态

<!-- -->

-   产品现有库存量以下方式显示：
    -   "按实际库存 (此查看表示总金额。)
    -   "按中预留的实际 (此查看预留) 表示的金额。
    -   "按实际可用 (此查看表示没有可用金额的预留。)

## <a name="get-started"></a>开始
开始在您的移动设备：

1.  从您的商店，移动应用请下载和安装 Microsoft Dynamics 365 应用的工序。
2.  开始在您的设备上应用。
3.  输入您的 Dynamics 365 URL。
4.  输入公司登录。 例如，输入 USMF ** **。
5.  首次登录的实例，则将提示您输入用户名和密码。您的 Microsoft Dynamics 365 数据的会计的。 输入您的凭据。 在登录后，您为公司查看可用工作区。

若要查看您在移动应用的工作区，必须首先过帐预期工作区到 Dynamics 365 应用的工序。

1.  的工序启动 Dynamics 365。
2.  **是系统管理** &gt; **设置** &gt; ** **系统参数。
3.  **选择请管理移动应用**。
4.  选择工作区发布到移动平台。
5.  **选择请过帐工作区**。
6.  刷新您的设备查看过帐工作区的。

## <a name="view-the-onhand-inventory-for-a-product"></a>查看产品的 onhand 库存
1.  在您移动的设备上，选择现有库存量** **工作区。
2.  **选择查看现有量物料**的。 您看到加载到您的应用为使用产品脱机的列表。 默认情况下，则 50 个物料将加载，不过，您还可以更改此编号。 有关详细信息，请参阅此长度中读取先的指南。
3.  如果您的项目不在该列表中，选择为详细** **搜索满足在 Dynamics 365 中的联机搜索操作。 搜索副产品或切换副产品编号来搜索名称。
4.  选择项目。 如果物料具有一幅图像，查看图像。
5.  选择以下选项之一以查看现有库存量状态：
    -   按站点查看现有量
    -   按仓库查看现有量
    -   按库位查看现有量
    -   查看现有量每个批次 (为批次控制产品)
    -   查看每个现有量库存状态

    产品现有库存量以下方式显示：
    -   "按实际库存 (此查看表示总金额。)
    -   "按中预留的实际 (此查看预留) 表示的金额。
    -   "按实际可用 (此查看表示没有可用金额的预留。)





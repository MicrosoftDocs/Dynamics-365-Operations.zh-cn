---
title: "Microsoft Dynamics 365 for Operations 应用程序的销售订单移动工作区"
description: "通过销售订单移动工作区，您可以随时随地掌握销售订单的最新信息。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: dbc6dc39-b535-42d3-9fbd-4724597388ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 851c53e1c53fb37488ed86e25e3ede83ca0541db
ms.lasthandoff: 03/31/2017


---

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Microsoft Dynamics 365 for Operations 应用程序的销售订单移动工作区

通过销售订单移动工作区，您可以随时随地掌握销售订单的最新信息。 

<a name="prerequisites"></a>先决条件
-------------

| 必备项                                                         | 说明                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 了解 Microsoft Dynamics 365 for Operations 移动平台 | [Dynamics 365 for Operations 移动平台](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | 确保使用的环境中已安装了 Microsoft Dynamics 365 for Operations 版本 1611 和 Microsoft Dynamics for Operations 平台更新 3（2016 年 11 月）。 |
| 修补程序 KB 3215650                                                    | 安装此修补程序以启用 Microsoft Dynamics 365 for Operations 中提供的工作区。                                                                       |
| 已安装了 Dynamics 365 for Operations 应用程序的移动设备 | 从移动应用商店下载 Dynamics 365 for Operations 应用程序。                                                                                                      |

## <a name="overview"></a>概览
此移动工作区访问 Dynamics 365 for Operations 应用程序，供您查看有关每个销售订单的详细信息，如订单状态、客户联系信息和订单员联系信息。 此移动工作区提供销售订单的即时视图。 您可以按客户查看销售订单，查看所有销售订单，或查看有关特定销售订单的信息。 此移动工作区提供两种视图来帮助您深入分析销售订单。

### <a name="view-all-sales-orders"></a>查看所有销售订单

此视图列出所有销售订单。

-   请使用以下筛选器之一选择要查看的销售订单。
    -   按销售订单搜索
    -   按客户帐户搜索
    -   按客户名称搜索
    -   按状态搜索
    -   按发布状态搜索
    -   按创建日期和时间搜索

<!-- -->

-   选择销售订单之后，可以查看特定订单的详细信息。 具体而言，可以查看：
    -   客户名称和地址信息
    -   不同的销售订单日期，如要求装运日期和已确认的装运日期
    -   订单员联系信息
    -   客户联系信息
    -   订单行
    -   显示销售订单的装运方式和装运时间的装运

### <a name="view-orders-for-a-customer-"></a>查看客户 ** ** 的订单

此视图按客户列出销售订单。

-   使用以下筛选器之一查看某个客户的订单。
    -   按名称:搜索
    -   按帐户搜索

<!-- -->

-   选择客户后，您可以查看：
    -   客户名称和组
    -   客户联系信息
    -   客户销售订单和及其详细信息：
        -   客户名称和地址信息
        -   不同的销售订单日期
        -   订单员联系信息
        -   客户联系信息
        -   订单行
        -   显示销售订单的装运方式和装运时间的装运

## <a name="get-started"></a>开始
执行以下步骤开始在移动设备上使用销售订单移动工作区。

1.  在移动应用商店中，下载并安装 Microsoft Dynamics 365 for Operations 应用程序。
2.  在设备上启动应用程序。
3.  输入您的 Dynamics 365 URL。
4.  输入要登录的公司。 例如，输入 **USMF**。
5.  首次登录时，系统将提示您提供您的 Microsoft Dynamics 365 for Operations 帐户用户名和密码。 输入凭据。 登录后，您将看到您的公司的可用工作区。

若要在移动应用程序中查看工作区，必须先将所需工作区发布到 Dynamics 365 for Operations 应用程序。

1.  启动 Dynamics 365 for Operations。
2.  转到**系统管理** &gt; **设置** &gt; **系统参数**。
3.  选择**管理移动应用程序**。
4.  选择要发布到移动平台的工作区。
5.  选择**发布工作区**。
6.  刷新设备以查看发布的工作区。

## <a name="view-information-about-sales-orders-for-a-customer"></a>查看有关客户的销售订单的信息
1.  在移动设备上，选择**销售订单**工作区。
2.  选择**查看客户的订单**。
3.  使用 **帐户** 或 **客户名称** 信息查找所需客户。
4.  选择客户。
5.  选择**联系信息**或**销售订单**。
6.  如果已选择**销售订单**，将显示该客户的销售订单列表。
7.  选择**销售订单**。
8.  可在此处查看有关销售订单行、装运、客户联系信息和订单员联系信息的信息。





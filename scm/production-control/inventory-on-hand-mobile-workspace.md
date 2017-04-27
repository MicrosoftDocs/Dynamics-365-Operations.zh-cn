---
title: "Microsoft Dynamics 365 for Operations 应用程序的现有库存量移动工作区"
description: "现有库存量移动工作区可帮助您随时随地从移动角度洞察预留库存和可用库存。"
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

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Microsoft Dynamics 365 for Operations 应用程序的现有库存量移动工作区

现有库存量移动工作区可帮助您随时随地从移动角度洞察预留库存和可用库存。 

<a name="prerequisites"></a>先决条件
-------------

| 必备项                                                         | 说明                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 了解 Microsoft Dynamics 365 for Operations 移动平台 | [Dynamics 365 for Operations 移动平台](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 for Operations                                          | 已安装了 Microsoft Dynamics 365 for Operations 版本 1611 和 Microsoft Dynamics for Operations 平台更新 3（2016 年 11 月）的环境 |
| 修补程序 KB 3215650                                                    | 安装此修补程序以启用 Microsoft Dynamics 365 for Operations 中提供的工作区。                                       |
| 已安装了 Dynamics 365 for Operations 应用程序的移动设备 | 从移动应用商店下载 Dynamics 365 for Operations 应用程序。                                                                           |

## <a name="introduction"></a>简介
公司的库存通常每天有多次装运和多次收货。 这些活动不断改变现有库存状态。 可通过现有库存量移动工作区查看跨公司现有库存状态，以便您在所选移动设备上洞察最新的库存数据。 无论在处理仓库、采购销售、制造或管理，还是充当其他角色，都可以随时随地访问现有库存数据。 此移动工作区提供跨多个设施的现有状态的即时视图，可供您查看跨设施的现有库存量、当前物料预留情况，以及未预留的库存量。 也可以输入物料编号以查询现有库存量，并对现有产品或变型执行筛选搜索。 特别是，此移动工作区提供以下功能：

-   可以按产品编号或产品名称搜索，以便找到要查看其现有库存状态的产品。
-   对于所选产品，可以查看以下信息：
    -   按站点的现有库存量
    -   按仓库的现有库存量
    -   按位置的现有库存量
    -   按批次的现有库存量（对于批量控制的产品）
    -   按库存状态的现有库存量

<!-- -->

-   按照以下方式显示产品的现有库存量：
    -   按物理库存（此视图显示总金额。）
    -   按物理预留（此视图显示预留金额。）
    -   按物理可用量（此视图显示无预留的可用金额。）

## <a name="get-started"></a>开始
若要在移动设备上开始：

1.  从移动应用商店中下载并安装 Microsoft Dynamics 365 for Operations 应用程序。
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

## <a name="view-the-onhand-inventory-for-a-product"></a>查看产品的现有库存量
1.  在移动设备上，选择**现有库存量**工作区。
2.  选择**检查物料的现有库存量**。 将看到加载到您的应用程序中供脱机使用的产品的列表。 默认情况下，将加载 50 个物料，但是您可以更改此数字。 有关详细信息，请参阅预习手册。
3.  如果列表中不包含您的物料，请选择**搜索更多**，在 Dynamics 365 for Operations 中执行联机搜索。 按产品编号搜索，或切换到按产品名搜索。
4.  选择项目。 如果物料有图像，将显示该图像。
5.  选择以下选项之一查看现有库存状态：
    -   按站点查看现有库存量
    -   按仓库查看现有库存量
    -   按位置查看现有库存量
    -   按批次查看现有库存量（对于批次控制的产品）
    -   按库存状态查看现有库存量

    按照以下方式显示产品的现有库存量：
    -   按物理库存（此视图显示总金额。）
    -   按物理预留（此视图显示预留金额。）
    -   按物理可用量（此视图显示无预留的可用金额。）





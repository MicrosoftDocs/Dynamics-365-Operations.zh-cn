---
title: "Microsoft Dynamics 365 for Operations 应用程序的成本控制移动工作区"
description: "成本中心经理随时随地可通过成本控制移动工作区查看成本中心性能。"
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 53 - 04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 84740472-494f-444c-9b74-f83b7342fd25
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 8136efb1d2669c39fcc0f80b60e80ecae983d5d8
ms.lasthandoff: 03/31/2017


---

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Microsoft Dynamics 365 for Operations 应用程序的成本控制移动工作区

成本中心经理随时随地可通过成本控制移动工作区查看成本中心性能。 

<a name="prerequisites"></a>先决条件
-------------

| 必备项                                                         | 说明                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 了解 Microsoft Dynamics 365 for Operations 移动平台 | [Dynamics 365 for Operations 移动平台](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | 确保使用的环境中已安装了 Microsoft Dynamics 365 for Operations 版本 1611 和 Microsoft Dynamics for Operations 平台更新 3（2016 年 11 月）。 |
| 修补程序 KB 3215650                                                    | 安装此修补程序以启用 Microsoft Dynamics 365 for Operations 中提供的工作区。                                                                       |
| 已安装了 Dynamics 365 for Operations 应用程序的移动设备 | 从移动应用商店下载 Dynamics 365 for Operations 应用程序。                                                                                                      |

## <a name="introduction"></a>简介
成本控制移动工作区通过比较实际成本与预算成本，提供成本中心当前绩效的即时视图。 可以向下钻取单个成本元素的状态。

### <a name="example"></a>示例

员工收到国际会议的邀请。 组织必须承担所有出差费用。 员工询问经理是否可参加此会议。 经理使用自己的手机快速打开成本控制移动工作区，查看是否有员工参加此会议的预算。

### <a name="data-security"></a>数据安全

成本控制工作区中的数据受到用户凭据的保护。 只有成本中心经理才能查看自己的成本中心的数据。 访问级别安全在成本核算模板内管理。 成本会计员定义成本核算模块中的成本控制移动工作区配置。 此工作区发布到 Microsoft Dynamics 365 for Operations 应用程序之后，可在 Dynamics 365 for Operations 移动应用程序中使用。 这确保组织中的所有成本中心经理均可以相同格式查看数据。

### <a name="actions-views-and-links"></a>操作、视图和链接

Dynamics 365 for Operations 应用程序的成本控制移动工作区提供以下操作、视图和链接：

-   行动 
    -   选择**配置**以选择布局。
    -   选择**成本对象**以选择要对其筛选数据的成本中心。 **注释：**将根据成本核算模块中授予的访问权显示列表。

<!-- -->

-   可以根据**操作**下的选择和成本核算模块中的配置查看“卡”中的以下信息。 请注意，金额以相同格式选择：“实际值”、“预算”、“差异”和“差异百分比”。 
    -   实际值与预算（当前期间）
    -   实际值与已修订的预算（当前期间）
    -   实际值与预算（上一期间）
    -   实际值与已修订的预算（上一期间）
    -   实际值与预算（本年迄今）
    -   实际值与已修订的预算（本年迄今）

<!-- -->

-   链接
    -   当前期间的详细信息。
    -   上一期间的详细信息。
    -   本年迄今的详细信息。

选择其中一个链接时，将显示一个“按成本的卡”元素。 “卡”中的金额以以下格式显示：“实际值”、“预算差异”、“预算差异百分比”、“已修订的预算”、“已修订的预算差异”和“已修订的预算差异百分比”。  [![成本控制](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>开始
执行以下步骤开始在移动设备上使用成本控制移动应用程序。

1.  在移动应用商店中，下载并安装 Microsoft Dynamics 365 for Operations 应用程序。
2.  在设备上启动应用程序。
3.  输入您的 Dynamics 365 URL。
4.  输入要登录的公司。 例如，输入 **USMF**。
5.  首次登录时，系统将提示您提供您的 Microsoft Dynamics 365 for Operations 帐户用户名和密码。 输入凭据。 登录后，您将看到您的公司的可用工作区。

若要在移动应用程序中查看工作区，必须先将所需工作区发布到 Dynamics 365 for Operations 应用程序。

1.  启动 Dynamics 365 for Operations。
2.  转到**系统管理** &gt; **设置** &gt; **系统参数**。
3.  选择**管理移动应用程序**。
4.  选择要发布到移动平台的 **成本控制** 工作区。
5.  选择**发布工作区**。
6.  刷新设备以查看发布的工作区。

## <a name="view-the-performance-of-your-cost-center"></a>查看成本中心的绩效
1.  在移动设备上，选择**成本控制**工作区。
2.  选择**成本对象控制**。
3.  单击**操作**。
4.  单击**选择配置**以选择成本控制布局。
5.  单击**完成**。
6.  单击**操作**。
7.  单击**选择成本对象**以启动为您授予了访问权限的成本中心。
8.  单击**完成**。
9.  查看成本中心的整体绩效。
10. 单击**当前期间的详细信息**。
11. 查看单个成本元素的绩效。
12. 也可以搜索特定成本元素。




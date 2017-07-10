---
title: "销售订单移动工作区"
description: "此主题提供有关销售订单移动工作区的信息。 此工作区帮助您随时随地掌握最新的销售订单。"
author: Mirzaab
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: a0edbad63c51d111d7c8985aa7fdf7312da6149d
ms.openlocfilehash: 1a05c6c12d4b6d98886e418aadcc0bdb2c2fc8ef
ms.contentlocale: zh-cn
ms.lasthandoff: 06/13/2017


---

# <a name="sales-orders-mobile-workspace"></a>销售订单移动工作区

[!include[banner](../includes/banner.md)]

此主题提供有关**销售订单**移动工作区的信息。 此工作区帮助您随时随地掌握最新的销售订单。 

将此工作区用于与 Microsoft Dynamics 365 for Unified Operations 移动应用一起使用。

## <a name="overview"></a>概览
**销售订单**移动工作区可以让您查看有关各销售订单的详细信息。 此信息包括订单状态、客户的联系信息和订单员的联系信息。 **销售订单**移动工作区提供销售订单的即时视图。 您可以查看所有销售订单，按客户查看销售订单，或查看有关特定销售订单的信息。 

此移动工作区提供两种视图来帮助您深入分析销售订单。

### <a name="view-all-sales-orders"></a>查看所有销售订单
此视图列出所有销售订单。

-   请使用以下筛选器之一选择要查看的销售订单：

    -   按销售订单搜索
    -   按客户帐户搜索
    -   按客户名称搜索
    -   按状态搜索
    -   按发布状态搜索
    -   按创建日期和时间搜索
    
-   选择销售订单之后，可以查看特定订单的详细信息。 特别是，您可以查看以下信息：

    -   客户名称和地址信息
    -   各个销售订单日期，如要求装运日期和确认装运日期
    -   订单员的联系信息
    -   客户联系信息
    -   订单行
    -   显示销售订单的装运方式和装运时间的装运

### <a name="view-orders-for-a-customer"></a>查看客户的订单
此视图按客户列出销售订单。

-   使用以下筛选器之一查看某个客户的订单：

    -   按名称:搜索
    -   按帐户搜索

-   在选择某一客户后，您可以查看以下信息：

    -   客户名称和组
    -   客户联系信息
    -   客户销售订单和及其详细信息：
    
        -   客户名称和地址信息
        -   不同的销售订单日期
        -   订单员的联系信息
        -   客户联系信息
        -   订单行
        -   显示销售订单的装运方式和装运时间的装运

## <a name="prerequisites"></a>必备项
先决条件根据为您的组织部署的 Microsoft Dynamics 365 版本不同。

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a>使用 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 2017 年 7 月更新时的先决条件 
如果已经为您的组织部署 Dynamics 365 for Finance and Operations Enterprise Edition 2017 年 7 月更新，系统管理员必须发布**销售订单**移动工作区。 有关说明，请查阅 [发布移动工作区](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace)。

### <a name="prerequisites-if-you-use-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>使用带平台更新 3 或更高版本的 Dynamics 365 for Operations 版本 1611 时的先决条件
如果已经为您的组织部署带平台更新 3 或更高版本的 Dynamics 365 for Operations 版本 1611，系统管理员必须完成以下先决条件。 

<table>
<thead>
<tr class="header">
<th>必备项</th>
<th>角色</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>实现 KB 4013633。</td>
<td>系统管理员</td>

<td>KB 4013633 是包含<strong>销售订单</strong>移动工作区的 X++ 更新或元数据修补程序。 若要实施 KB 4013633，系统管理员必须遵循这些步骤。
<ol>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">从 Microsoft Dynamics Lifecycle Services (LCS) 下载元数据修补程序</a>。</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">安装元数据修补程序</a>。</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">创建</a>包含 <strong>SCMMobile</strong> 模型的可部署包，然后将可部署包上载到 LCS。</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">应用可部署包</a>。</li>

</ol></td>
</tr>
<tr class="even">
<td>发布<strong>销售订单</strong>移动工作区。</td>
<td>系统管理员</td>
<td>请查阅<a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">发布移动工作区</a>。</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>下载并安装移动应用
下载并安装 Dynamics 365 for Unified Operations 移动应用：

-   [适用于 Android 手机](https://go.microsoft.com/fwlink/?linkid=850662)
-   [适用于 iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>登录到移动应用

1.  在移动设备上启动应用程序。
2.  输入您的 Dynamics 365 URL。
3.  首次登录时，将提示您输入您的用户名和密码。 输入凭据。
4.  登录后，将显示您的公司的可用工作区。 请注意，如果您的系统管理员以后发布新工作区，您必须刷新移动工作区列表。

[![下拉以刷新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-sales-order-mobile-workspace"></a>通过使用此销售订单移动工作区查看有关客户销售订单的信息

1.  在移动设备上，选择**销售订单**工作区。
2.  选择**查看客户的订单**。
3.  使用帐户或客户名称信息查找客户。
4.  选择客户。
5.  选择**联系信息**或**销售订单**。 如果您选择**销售订单**，将显示该客户的销售订单列表。
6.  选择**销售订单**。 现在可以查看有关销售订单行的信息、有关装运的信息、客户联系信息和订单员联系信息。


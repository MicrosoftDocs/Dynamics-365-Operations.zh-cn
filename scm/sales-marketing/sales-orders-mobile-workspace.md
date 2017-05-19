---
title: "销售订单移动工作区"
description: "此主题提供有关销售订单移动工作区的信息，用于 Microsoft Dynamics 365 for Operations 移动应用。 此工作区帮助您随时随地掌握最新的销售订单。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 119b80e5d8067ffbf75d8b067f4803558c2c94b0
ms.contentlocale: zh-cn
ms.lasthandoff: 04/25/2017


---

# <a name="sales-orders-mobile-workspace"></a>销售订单移动工作区

[!include[banner](../includes/banner.md)]


此主题提供有关销售订单移动工作区的信息，用于 Microsoft Dynamics 365 for Operations 移动应用。 此工作区帮助您随时随地掌握最新的销售订单。 

<a name="overview-of-the-sales-orders-mobile-workspace"></a>销售订单移动工作区概览
---------------------------------------------

**销售订单**移动工作区访问 Microsoft Dynamics 365 for Operations，并允许您查看有关各销售订单的详细信息。 此信息包括订单状态、客户的联系信息和订单员的联系信息。 **销售订单**移动工作区提供销售订单的即时视图。 您可以查看所有销售订单，按客户查看销售订单，或查看有关特定销售订单的信息。 此移动工作区提供两种视图来帮助您深入分析销售订单。

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
在使用**销售订单**移动工作区之前，请确保您的系统管理员具备以下先决条件。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>必备项</th>
<th>角色</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>必须实施具有工序平台更新 3 或更高版本的 Dynamics 365 for Operations 版本 1611。</td>
<td>系统管理员</td>
<td>如果您尚未在您的组织中部署 Dynamics 365 for Operations，系统管理员应看到<a href="http://ax.help.dynamics.com/en/wiki/deploy-an-ax7-demo-environment/">部署 Microsoft Dynamics 365 for Operations 演示环境</a>。</td>
</tr>
<tr class="even">
<td>必须实施 KB 4013633。</td>
<td>系统管理员</td>
<td>KB 4013633（X++ 更新或元数据修补程序）包含用于供应链管理的四个移动工作区。 若要实施 KB 4013633，系统管理员必须遵循这些步骤：
<ol>
<li>从 Microsoft Dynamics Lifecycle Services (LCS) 下载 KB 4013633。</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">安装元数据修补程序</a>。</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">创建</a>包含 <strong>SCMMobile</strong> 模型的可部署包，然后将可部署包上载到 LCS。</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">将可部署包</a>应用到您的 Dynamics 365 for Operations 系统。</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>销售订单</strong>移动工作区必须发布到 Dynamics 365 for Operations 移动应用。</td>
<td>系统管理员</td>
<td><ol>
<li>在在您的浏览器中启动 Dynamics 365 for Operations。</li>
<li>在<strong>系统参数</strong>页面，选择<strong>管理移动工作区</strong>。</li>
<li>选择<strong>销售订单</strong>工作区。</li>
<li>单击<strong>发布移动工作区</strong>。</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>下载并安装 Dynamics 365 for Operations 移动应用
从移动应用商店中下载并安装 Dynamics 365 for Operations 移动应用。

-   Android：[Google Play Store 中的 Dynamics 365 for Operations](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   iPhone：[iTunes 应用商店中的 Dynamics 365 for Operations](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>登录到 Dynamics 365 for Operations 移动应用
1.  在移动设备上启动应用程序。
2.  输入 Dynamics 365 for Operations URL。
3.  输入要登录的公司。 例如，输入 **USMF**。
4.  首次登录时，系统将提示您提供您的 Dynamics 365 for Operations 帐户用户名和密码。 输入凭据。
5.  登录后，您将看到您的公司的可用工作区。 请注意，如果您的系统管理员以后发布新工作区，您可以下拉刷新移动工作区列表。 

    [![下拉以刷新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-mobile-workspace"></a>通过使用此移动工作区查看有关客户销售订单的信息
1.  在移动设备上，选择**销售订单**工作区。
2.  选择**查看客户的订单**。
3.  使用帐户或客户名称信息查找客户。
4.  选择客户。
5.  选择**联系信息**或**销售订单**。 如果您选择**销售订单**，将显示该客户的销售订单列表。
6.  选择**销售订单**。 现在可以查看有关销售订单行的信息、有关装运的信息、客户联系信息和订单员联系信息。






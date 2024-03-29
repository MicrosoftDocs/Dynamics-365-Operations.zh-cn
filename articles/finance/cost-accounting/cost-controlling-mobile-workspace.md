---
title: 成本控制移动工作区
description: 本文提供有关成本控制移动工作区的信息。 此工作区让成本中心经理可以在任何时候任何位置查看有关成本中心绩效的信息。
author: AndersGirke
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMMobileCostObjectOverviewDetailsCurrentPeriod, CAMMobileCostObjectList, CAMMobileCostObjectOverviewDetailsPreviousPeriod, CAMMobileCostObjectOverview, CAMMobileCostObjectOverviewDetailsYearToDate, CAMMobileCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 2d6d3fdcc0b0387a92f138b0ba7cf537f473b91a
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069554"
---
# <a name="cost-controlling-mobile-workspace"></a>成本控制移动工作区

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

本文提供有关 **成本控制** 移动工作区的信息。 此工作区让成本中心经理可以在任何时候任何位置查看有关成本中心绩效的信息。

此工作区应该与财务和运营 (Dynamics 365) 移动应用结合使用。

## <a name="overview"></a>概述
**成本控制** 移动工作区通过比较实际成本与预算成本，提供成本中心当前绩效的即时视图。 可以向下钻取单个成本元素的状态。

例如，员工收到国际会议的邀请，但组织必须支付所有差旅费。 员工询问经理是否可参加此会议。 经理使用自己的移动设备打开 **成本控制** 移动工作区，查看她是否有员工参加此会议的预算。

### <a name="data-security"></a>数据安全
**成本控制** 移动工作区中的数据通过用户凭据加以保护。 成本中心经理只能查看自己成本中心的数据。 访问级别安全在 **成本核算** 模板内管理。

成本会计员定义 **成本核算** 模块中的 **成本控制** 移动工作区的配置。 此工作区发布到移动应用之后，可在此应用程序中使用。 因此，组织中的所有成本中心经理均可以相同格式查看数据。

### <a name="actions-views-and-links"></a>操作、视图和链接
**成本控制** 移动工作区提供以下操作、视图和链接：

-   **操作：**

    -   使用 **选择配置** 选择布局。
    -   使用 **选择成本对象** 选择要筛选数据的成本中心。
    
        > [!NOTE]
        > 显示在列表中的成本中心取决于 **成本核算** 模块中授予的访问权限。

-   **视图：** 基于选择的操作和 **成本核算** 模块中的配置，可以查看卡中的以下信息：

    -   实际值与预算(当前期间)
    -   实际值与已修订的预算(当前期间)
    -   实际值与预算（上一期间）
    -   实际值与已修订的预算（上一期间）
    -   实际值与预算（本年迄今）
    -   实际值与已修订的预算（本年迄今）

    以下金额在每个卡显示：实际值、预算、差异和差异百分比。

-   **链接：**

    -   当前期间的详细信息
    -   上一期间的详细信息
    -   本年迄今的详细信息

    当您选择链接时，为各成本要素显示卡。 将显示每个卡中的以下金额：“实际值”、“预算差异”、“预算差异百分比”、“已修订的预算”、“已修订的预算差异”和“已修订的预算差异百分比”。
    
    [![成本元素的卡。](./media/Cost-controlling.png)](./media/Cost-controlling.png)

## <a name="prerequisites"></a>先决条件
先决条件根据为您的组织部署的 Microsoft Dynamics 365 版本不同。

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a>使用 Microsoft Dynamics 365 Finance 的先决条件
如果已经为您的组织部署 Finance，系统管理员必须发布 **成本控制** 移动工作区。 有关说明，请查阅 [发布移动工作区](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md)。

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>使用带平台更新 3 或更高版本的版本 1611 时的先决条件
如果已经为您的组织部署带平台更新 3 或更高版本的版本 1611，系统管理员必须完成以下先决条件。

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

<td>KB 4013633 是包含<strong>成本控制</strong>移动工作区的 X++ 更新或元数据修补程序。 若要实施 KB 4013633，系统管理员必须遵循这些步骤。
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">从 Microsoft Dynamics Lifecycle Services (LCS) 下载元数据修补程序</a>。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">安装元数据修补程序</a>。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">创建</a>包含 <strong>SCMMobile</strong> 模型的可部署包，然后将可部署包上载到 LCS。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">应用可部署包</a>。</li>

</ol></td>
</tr>
<tr class="even">
<td>发布<strong>成本控制</strong>移动工作区。</td>
<td>系统管理员</td>
<td>请查阅<a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">发布移动工作区</a>。</td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a>下载并安装移动应用
下载并安装财务和运营 (Dynamics 365) 移动应用：

-   [适用于 Android 手机](https://go.microsoft.com/fwlink/?linkid=850662)
-   [适用于 iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>登录到移动应用

1.  在移动设备上启动应用程序。
2.  输入您的 Dynamics 365 URL。
3.  首次登录时，将提示您输入您的用户名和密码。 输入凭据。
4.  登录后，将显示您的公司的可用工作区。 请注意，如果您的系统管理员以后发布新工作区，您必须刷新移动工作区列表。

[![下拉以刷新。](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a>使用成本控制移动工作区查看成本中心的绩效

1.  在移动设备上，选择 **成本控制** 工作区。
2.  选择 **成本对象控制**。
3.  选择 **操作**。
4.  选择 **选择配置** 以选择成本控制布局。
5.  选择 **完成**。
6.  选择 **操作**。
7.  选择 **选择成本对象** 以选择为您授予了访问权限的成本中心。
8.  选择 **完成**。
9.  查看成本中心的整体绩效。
10. 选择 **当前期间的详细信息** 链接。
11. 查看单个成本元素的绩效。
12. 也可以搜索特定成本元素。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]


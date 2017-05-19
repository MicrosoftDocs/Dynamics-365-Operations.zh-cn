---
title: "成本控制移动工作区"
description: "此主题提供有关成本控制移动工作区的信息，用于 Microsoft Dynamics 365 for Operations 移动应用。 此工作区让成本中心经理可以在任何时候任何位置查看有关成本中心绩效的信息。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 31a9650774b2ddb70827ffa210154ca10c761236
ms.contentlocale: zh-cn
ms.lasthandoff: 04/25/2017


---

# <a name="cost-controlling-mobile-workspace"></a>成本控制移动工作区

[!include[banner](../includes/banner.md)]


此主题提供有关成本控制移动工作区的信息，用于 Microsoft Dynamics 365 for Operations 移动应用。 此工作区让成本中心经理可以在任何时候任何位置查看有关成本中心绩效的信息。 

<a name="overview-of-the-cost-controlling-mobile-workspace"></a>成本控制移动工作区概览
-------------------------------------------------

**成本控制**移动工作区通过比较实际成本与预算成本，提供成本中心当前绩效的即时视图。 可以向下钻取单个成本元素的状态。 例如，员工收到国际会议的邀请，但组织必须支付所有差旅费。 员工询问经理是否可参加此会议。 经理使用自己的移动设备打开**成本控制**移动工作区，查看她是否有员工参加此会议的预算。

### <a name="data-security"></a>数据安全

**成本控制**移动工作区中的数据通过用户凭据加以保护。 成本中心经理只能查看自己成本中心的数据。 访问级别安全在**成本核算**模板内管理。 成本会计员定义**成本核算**模块中的**成本控制**移动工作区的配置。 此工作区发布到 Microsoft Dynamics 365 for Operations 移动应用之后，可在此应用程序中使用。 因此，组织中的所有成本中心经理均可以相同格式查看数据。

### <a name="actions-views-and-links"></a>操作、视图和链接

Dynamics 365 for Operations 应用程序的**成本控制**移动工作区提供以下操作、视图和链接：

-   **操作：**
    -   使用**选择配置**选择布局。
    -   使用**选择成本对象**选择要筛选数据的成本中心。 **注意：**显示在列表中的成本中心取决于**成本核算**模块中授予的访问权限。
-   **视图：**基于选择的操作和**成本核算**模块中的配置，可以查看卡中的以下信息。
    -   实际值与预算（当前期间）
    -   实际值与已修订的预算（当前期间）
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
    
    [![成本元素的卡](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="prerequisites"></a>必备项
在使用**成本控制**移动工作区之前，请确保您的系统管理员具备以下先决条件。

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
<td><strong>成本控制</strong>移动工作区必须发布到 Dynamics 365 for Operations 移动应用。</td>
<td>系统管理员</td>
<td><ol>
<li>在在您的浏览器中启动 Dynamics 365 for Operations。</li>
<li>在<strong>系统参数</strong>页面，选择<strong>管理移动工作区</strong>。</li>
<li>选择<strong>成本对象概览</strong>工作区。</li>
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

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a>使用成本控制移动工作区查看成本中心的绩效
1.  在移动设备上，选择**成本控制**工作区。
2.  选择**成本对象控制**。
3.  选择**操作**。
4.  选择**选择配置**以选择成本控制布局。
5.  选择**完成**。
6.  选择**操作**。
7.  选择**选择成本对象**以选择为您授予了访问权限的成本中心。
8.  选择**完成**。
9.  查看成本中心的整体绩效。
10. 选择**当前期间的详细信息**链接。
11. 查看单个成本元素的绩效。
12. 也可以搜索特定成本元素。






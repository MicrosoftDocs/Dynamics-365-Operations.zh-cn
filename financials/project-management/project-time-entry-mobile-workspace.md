---
title: "Dynamics 365 for Operations 应用程序的项目时间条目移动工作区"
description: "此主题提供有关项目时间条目移动工作区的信息。 此工作区让用户可以使用其移动设备根据项目输入和保存时间。"
author: annbe
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e3e0be36c045acc3750efbb739d79d81ab937c65
ms.contentlocale: zh-cn
ms.lasthandoff: 04/25/2017


---

# <a name="project-time-entry-mobile-workspace"></a>项目时间条目移动工作区

[!include[banner](../includes/banner.md)]

"[!include[banner](../includes/banner.md)]"


此主题提供有关 Dynamics 365 for Operations 移动应用的项目时间条目移动工作区的信息。 此工作区让用户可以使用其移动设备根据项目输入和保存时间。

<a name="overview-of-the-project-time-entry-mobile-workspace"></a>项目时间条目移动工作区概览
---------------------------------------------------

作为其日常工作的一部分，项目资源通常是在现场或出差。 **项目时间条目**移动工作区让用户可以在所选择的移动设备上根据项目输入计费或非计费时间。 因此，项目资源可以随时随地记录时间条目。 他们还可以查看已记录的时间条目。 

特别是，**项目时间条目**移动工作区提供以下功能：

-   对于任何选择的日期，输入在特定任务上所用的工时数。
-   按项目名称或客户搜索查找为其输入时间的项目。
-   指定您所用时间的类别和活动。
-   将项目时间记录为计费或非计费。
-   可以选择输入任何外部或内部注释。

若要实施**项目时间条目**移动工作区，请参阅此主题的以下部分。

## <a name="prerequisites"></a>必备项
在实施**项目时间条目**移动工作区之前，请确保您的系统管理员完成以下先决条件。

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
<td>必须实施具有工序平台更新 3 或更高版本的 Microsoft Dynamics 365 for Operations 版本 1611。</td>
<td>系统管理员</td>
<td>如果您尚未在您的组织中部署 Dynamics 365 for Operations，系统管理员应看到<a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">部署 Microsoft Dynamics 365 for Operations 演示环境</a>。</td>
</tr>
<tr class="even">
<td>必须实施 KB 4018050。</td>
<td>系统管理员</td>
<td>KB 4018050 是包含<strong>项目时间条目</strong>移动工作区的 X++ 更新或元数据修补程序。 若要实施 KB 4018050，系统管理员必须遵循这些步骤。
<ol>
<li>从 Microsoft Dynamics Lifecycle Services (LCS) 下载 KB 4018050。</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">安装元数据修补程序</a>。</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">创建</a>包含 <strong>ApplicationSuite</strong> 和 <strong>ProjectMobile</strong> 模型的可部署包，然后将可部署包上载到 LCS。</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">将可部署包</a>应用到您的 Dynamics 365 for Operations 系统。</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>项目时间条目</strong>移动工作区必须发布到 Dynamics 365 for Operations 移动应用。</td>
<td>系统管理员</td>
<td><ol>
<li>在在您的浏览器中启动 Dynamics 365 for Operations。</li>
<li>在<strong>系统参数</strong>页面，在<strong>管理移动工作区</strong>选项卡，选择<strong>项目时间条目</strong>工作区。</li>
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

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>通过使用项目时间条目移动工作区输入时间
1.  在移动设备上，选择**项目时间条目**工作区。
2.  选择**时间条目**。 您看到当前周的日历日期。
3.  对于所选日期，选择**操作**&gt;**新条目**。
4.  输入要记录的小时数。
5.  为时间条目选择项目。 将看到加载到您的应用程序中供脱机使用的项目的列表。 默认情况下，加载 50 项，但是开发人员可以更改此数字。 有关详细信息，开发人员应参阅[Dynamics 365 for Operations 移动平台](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)。
6.  如果列表中不包含您的项目，请选择**搜索**，在 Dynamics 365 for Operations 中执行联机搜索。 按名称搜索，或切换到按项目名称或客户搜索。
7.  选择类别。 将看到加载到您的应用程序中供脱机使用的类别的列表。 默认情况下，加载 50 项，但是开发人员可以更改此数字。 有关详细信息，开发人员应参阅[Dynamics 365 for Operations 移动平台](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)。
8.  如果列表中不包含您的类别，请选择**搜索**，在 Dynamics 365 for Operations 中执行联机搜索。 按类别搜索，或切换到按类别名称搜索。
9.  选择活动。 将看到加载到您的应用程序中供脱机使用的活动的列表。 默认情况下，加载 50 项，但是开发人员可以更改此数字。 有关详细信息，开发人员应参阅[Dynamics 365 for Operations 移动平台](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)。
10. 如果列表中不包含您的活动，请选择**搜索**，在 Dynamics 365 for Operations 中执行联机搜索。 按活动编号搜索，或切换到按用途搜索。
11. 选择记录属性
12. 可选：输入任何外部和内部注释。
13. 选择**完成**。







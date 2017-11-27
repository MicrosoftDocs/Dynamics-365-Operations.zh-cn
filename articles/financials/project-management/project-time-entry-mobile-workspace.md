---
title: "项目时间条目移动工作区"
description: "此主题提供有关项目时间条目移动工作区的信息。 此工作区让用户可以使用其移动设备根据项目输入和保存时间。"
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8185be069a552105073958d5144ad402ddae6b9f
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="project-time-entry-mobile-workspace"></a>项目时间条目移动工作区

[!include[banner](../includes/banner.md)]

此主题提供有关**项目时间条目**移动工作区的信息。 此工作区让用户可以使用其移动设备根据项目输入和保存时间。

将此工作区用于与 Microsoft Dynamics 365 for Unified Operations 移动应用一起使用。 

## <a name="overview"></a>概览
作为其日常工作的一部分，项目资源通常是在现场或出差。 **项目时间条目**移动工作区让用户可以在所选择的移动设备上根据项目输入计费或非计费时间。 因此，项目资源可以随时随地记录时间条目。 他们还可以查看已记录的时间条目。 

具体而言，在**项目时间条目**移动工作区中，用户可以执行以下任务：

-   对于任何选择的日期，输入在特定任务上所用的工时数。
-   按项目名称或客户搜索查找为其输入时间的项目。
-   指定您所用时间的类别和活动。
-   将项目时间记录为计费或非计费。
-   可以选择输入任何外部或内部注释。

## <a name="prerequisites"></a>必备项
先决条件根据为您的组织部署的 Microsoft Dynamics 365 版本不同。

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>使用 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月）时的先决条件 
如果已经为您的组织部署 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月），系统管理员必须发布**项目时间条目**移动工作区。 有关说明，请查阅 [发布移动工作区](../../dev-itpro/mobile-apps/publish-mobile-workspace.md)。

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>使用带平台更新 3 或更高版本的 Microsoft Dynamics 365 for Operations 版本 1611 时的先决条件
如果已经为您的组织部署带平台更新 3 或更高版本的 Microsoft Dynamics 365 for Operations 版本 1611，系统管理员必须完成以下先决条件。 

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

<td>实现 KB 4018050。</td>
<td>系统管理员</td>
<td>KB 4018050 是包含<strong>项目时间条目</strong>移动工作区的 X++ 更新或元数据修补程序。 若要实施 KB 4018050，系统管理员必须遵循这些步骤。
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">从 Microsoft Dynamics Lifecycle Services (LCS) 下载元数据修补程序</a>。</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">安装元数据修补程序</a>。</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">创建</a>包含 <strong>ApplicationSuite</strong> 和 <strong>ProjectMobile</strong> 模型的可部署包，然后将可部署包上载到 LCS。</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">应用可部署包</a>。</li>

</ol></td>
</tr>
<tr class="even">
<td>发布<strong>项目时间条目</strong>移动工作区。</td>
<td>系统管理员</td>
<td>请查阅<a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">发布移动工作区</a>。</td>
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

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>通过使用项目时间条目移动工作区输入时间
1.  在移动设备上，选择**项目时间条目**工作区。
2.  选择**时间条目**。 此时将显示当前周的日历日期。
3.  对于所选日期，选择**操作**&gt;**新条目**。
4.  输入要记录的小时数。
5.  为时间条目选择项目。 列表显示加载到您的应用程序中供脱机使用的项目。 默认情况下，加载 50 项，但是开发人员可以更改此数字。 有关详细信息，请参阅 [移动平台](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)。
6.  如果您的项目不在该列表中，请选择**搜索**。 按名称搜索，或切换到按项目名称或客户搜索。
7.  选择类别。 列表显示加载到您的应用程序中供脱机使用的类别。 默认情况下，加载 50 项，但是开发人员可以更改此数字。 有关详细信息，请参阅 [移动平台](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)。
8.  如果您的类别不在该列表中，请选择**搜索**。 按类别搜索，或切换到按类别名称搜索。
9.  选择活动。 列表显示加载到您的应用程序中供脱机使用的活动。 默认情况下，加载 50 项，但是开发人员可以更改此数字。 有关详细信息，请参阅 [移动平台](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)。
10. 如果您的活动不在该列表中，请选择**搜索**。 按活动编号搜索，或切换到按用途搜索。

11. 选择记录属性
12. 可选：输入任何外部和内部注释。
13. 选择**完成**。


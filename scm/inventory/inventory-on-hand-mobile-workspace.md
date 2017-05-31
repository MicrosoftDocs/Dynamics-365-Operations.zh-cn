---
title: "现有库存量移动工作区"
description: "此主题提供有关现有库存量移动工作区的信息，用于 Microsoft Dynamics 365 for Operations 移动应用。 此工作区可帮助您随时随地从移动角度洞察预留库存和可用库存。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7387df37e047d5ab7a90b696a6ffa249094499c4
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="inventory-on-hand-mobile-workspace"></a>现有库存量移动工作区

[!include[banner](../includes/banner.md)]


此主题提供有关现有库存量移动工作区的信息，用于 Microsoft Dynamics 365 for Operations 移动应用。 此工作区可帮助您随时随地从移动角度洞察预留库存和可用库存。

<a name="overview-of-the-inventory-on-hand-mobile-workspace"></a>现有库存量移动工作区概览
--------------------------------------------------

公司的库存通常每天有多次装运和多次收货。 这些活动不断改变现有库存状态。 可通过**现有库存量**移动工作区查看跨公司现有库存状态，以便您在所选移动设备上洞察最新的库存数据。 无论在处理仓库、采购销售、制造或管理，还是充当其他角色，都可以随时随地访问现有库存数据。 

此移动工作区提供跨多个设施的现有量状态的即时视图。 它让您查看跨多个设施的现有量视图、当前物料预留情况，以及未预留的现有库存量。 也可以输入物料编号以查询现有库存量，并可对现有产品或变型执行筛选搜索。 

特别是，此移动工作区提供以下功能：

-   可以按产品编号或产品名称搜索，以便找到要查看其现有库存状态的产品。

-   对于所选产品，可以查看以下信息：
    -   按站点的现有库存量
    -   按仓库的现有库存量
    -   按位置的现有库存量
    -   按批次的现有库存量（对于批量控制的产品）
    -   按库存状态的现有库存量
    
-   按照以下方式显示产品的现有库存量：
    -   按物理库存（此视图显示总金额。）
    -   按物理预留（此视图显示预留金额。）
    -   按物理可用量（此视图显示无预留的可用金额。）

## <a name="prerequisites"></a>必备项
在使用**现有库存量**移动工作区之前，请确保您的系统管理员具备以下先决条件。

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
<td>如果您尚未在您的组织中部署 Dynamics 365 for Operations，系统管理员应看到<a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">部署 Microsoft Dynamics 365 for Operations 演示环境</a>。</td>
</tr>
<tr class="even">
<td>必须实施 KB 4013633。</td>
<td>系统管理员</td>
<td>KB 4013633（X++ 更新或元数据修补程序）包含用于供应链管理的四个移动工作区。 若要实施 KB 4013633，系统管理员必须遵循这些步骤：
<ol>
<li>从 Microsoft Dynamics Lifecycle Services (LCS) 下载 KB 4013633。</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">安装元数据修补程序</a>。</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">创建</a>包含 <strong>SCMMobile</strong> 模型的可部署包，然后将可部署包上载到 LCS。</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">将可部署包</a>应用到您的 Dynamics 365 for Operations 系统。</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>现有库存量</strong>移动工作区必须发布到 Dynamics 365 for Operations 移动应用。</td>
<td>系统管理员</td>
<td><ol>
<li>在在您的浏览器中启动 Dynamics 365 for Operations。</li>
<li>在<strong>系统参数</strong>页面，选择<strong>管理移动工作区</strong>。</li>
<li>选择<strong>现有库存量</strong>工作区</li>
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

## <a name="view-the-onhand-inventory-for-a-product-by-using-the-inventory-onhand-mobile-workspace"></a>使用现有库存量移动工作区查看产品的现有库存量
1.  在移动设备上，选择**现有库存量**工作区。
2.  选择**检查物料的现有库存量**。 将看到加载到您的应用程序中供脱机使用的产品的列表。 默认情况下，加载 50 项，但是开发人员可以更改此数字。 有关详细信息，开发人员应参阅[Dynamics 365 for Operations 移动平台](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)。
3.  如果列表中不包含您的物料，请选择**搜索更多**，在 Dynamics 365 for Operations 中执行联机搜索。 按产品编号搜索，或切换到按产品名搜索。
4.  选择项目。 如果物料有图像，将显示该图像。
5.  选择以下选项之一查看现有库存量状态：
    -   按站点查看现有库存量
    -   按仓库查看现有库存量
    -   按位置查看现有库存量
    -   按批次查看现有库存量（对于批次控制的产品）
    -   按库存状态查看现有库存量

    按照以下方式显示产品的现有库存量：
    -   按物理库存（此视图显示总金额。）
    -   按物理预留（此视图显示预留金额。）
    -   按物理可用量（此视图显示无预留的可用金额。）







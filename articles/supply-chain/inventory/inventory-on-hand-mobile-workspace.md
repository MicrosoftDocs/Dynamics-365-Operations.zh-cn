---
title: 现有库存量移动工作区
description: 本文提供有关现有库存量移动工作区的信息。 此工作区可帮助您随时随地从移动角度洞察预留库存和可用库存。
author: yufeihuang
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yufeihuang
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 640a45e29627ffe56535c7d05419309688e8ecb6
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069807"
---
# <a name="inventory-on-hand-mobile-workspace"></a>现有库存量移动工作区

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

本文提供有关 **现有库存量** 移动工作区的信息。 此工作区可帮助您随时随地洞察预留库存和可用库存。

此工作区应该与财务和运营 (Dynamics 365) 移动应用结合使用。

## <a name="overview"></a>概述
公司的库存通常每天有多次装运和多次收货。 这些活动不断改变现有库存状态。 可通过 **现有库存量** 移动工作区查看跨公司现有库存状态，以便您在所选移动设备上洞察最新的库存数据。 无论在处理仓库、采购销售、制造或管理，还是充当其他角色，都可以随时随地访问现有库存数据。 

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

## <a name="prerequisites"></a>先决条件
先决条件根据为您的组织部署的 Supply Chain Management 版本不同。

### <a name="prerequisites-if-you-use-supply-chain-management"></a>使用 Supply Chain Management 时的先决条件
如果已经为您的组织部署 Supply Chain Management，系统管理员必须发布 **现有库存** 移动工作区。 有关说明，请查阅 [发布移动工作区](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md)。

### <a name="prerequisites-if-you-use-platform-update-3-or-later"></a>使用平台更新 3 或更高版本时的先决条件 
如果已经为您的组织部署平台更新 3 或更高版本，系统管理员必须完成以下先决条件。 

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

<td>KB 4013633 是包含<strong>现有库存量</strong>移动工作区的 X++ 更新或元数据修补程序。 若要实施 KB 4013633，系统管理员必须遵循这些步骤。
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">从 Microsoft Dynamics Lifecycle Services (LCS) 下载元数据修补程序</a>。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">安装元数据修补程序</a>。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">创建</a>包含 <strong>SCMMobile</strong> 模型的可部署包，然后将可部署包上载到 LCS。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">应用可部署包</a>。</li>

</ol></td>
</tr>
<tr class="even">
<td>发布<strong>现有库存量</strong>移动工作区。</td>
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

## <a name="view-the-on-hand-inventory-for-a-product-by-using-the-inventory-on-hand-mobile-workspace"></a>使用现有库存量移动工作区查看产品的现有库存量

1.  在移动设备上，选择 **现有库存量** 工作区。

2.  选择 **检查物料的现有库存量**。 将看到加载到您的应用程序中供脱机使用的产品的列表。 默认情况下，加载 50 项，但是开发人员可以更改此数字。 有关详细信息，开发人员应参阅 [移动平台](../../fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)。
3.  如果您的物料不在该列表中，请选择 **搜索更多**。 按产品编号搜索，或切换到按产品名搜索。

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]


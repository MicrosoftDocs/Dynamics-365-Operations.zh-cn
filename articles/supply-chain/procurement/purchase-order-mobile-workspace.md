---
title: 采购订单审核移动工作区
description: 此主题提供有关采购订单审核移动工作区的信息，以便您查看采购订单和通过操作作出响应。 例如，您可以审核或拒绝采购订单。
author: Henrikan
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fc88f20b50e034f2f27b7e2576fe6a4bb3486e23
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570553"
---
# <a name="purchase-order-approval-mobile-workspace"></a>采购订单审核移动工作区

[!include [banner](../includes/banner.md)]

此主题提供有关 **采购订单审核** 移动工作区的信息。 此工作区可让您查看采购订单和通过操作作出响应。 例如，您可以审核或拒绝采购订单。
 
## <a name="overview"></a>概览 
要求审核的采购订单通过审核工作流。 工作流可能包括要求一个或多个人员采取操作的不同步骤。 例如，人员可能必须完成任务或审核采购订单。 

**采购订单审核** 移动工作区能让您轻松地从移动设备查看和响应采购订单。 此工作区还可以让您执行可从客户端执行的相同工作流操作。

## <a name="prerequisites"></a>先决条件
先决条件根据为您的组织部署的 Supply Chain Management 版本不同。

### <a name="prerequisites-if-you-use-supply-chain-management"></a>使用 Supply Chain Management 时的先决条件 
如果已经为您的组织部署 Supply Chain Management，系统管理员必须发布 **采购订单审核** 移动工作区。 有关说明，请查阅 [发布移动工作区](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md)。

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
<td>实现 KB 4017918。</td>
<td>系统管理员</td>
<td>KB 4017918 是包含<strong>采购订单审核</strong>移动工作区的 X++ 更新或元数据修补程序。 若要实施 KB 4017918，系统管理员必须遵循这些步骤。
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">从 Microsoft Dynamics Lifecycle Services (LCS) 下载元数据修补程序</a>。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">安装元数据修补程序</a>。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">创建</a>包含 <strong>SCMMobile</strong> 模型的可部署包，然后将可部署包上载到 LCS。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">应用可部署包</a>。</li>
</ol></td>
</tr>
<tr class="even">
<td>发布<strong>采购订单审核</strong>移动工作区。</td>
<td>系统管理员</td>
<td>请查阅<a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">发布移动工作区</a>。</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>下载并安装移动应用
下载并安装 Finance and Operations 移动应用：

- [适用于 Android 手机](https://go.microsoft.com/fwlink/?linkid=850662)
- [适用于 iPhones](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a>登录到移动应用

1. 在移动设备上启动应用程序。
2. 输入您的 Microsoft Dynamics 365 URL。
3. 首次登录时，将提示您输入您的用户名和密码。 输入凭据。
4. 登录后，将显示您的公司的可用工作区。 请注意，如果您的系统管理员以后发布新工作区，您必须刷新移动工作区列表。

![可用工作区列表中的采购订单审批工作区。](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a>查看分配给您的订单
1. 在移动设备上，选择 **采购订单审核** 工作区。
2. 选择 **分配给我的订单** 以查看要求您在采购订单审核工作流中对其执行操作的所有采购订单。
3. 选择订单。 在 **订单明细** 页，您将看到订单头信息和行。 还可以从工作流任务查找指南。
4. 选择 **会计分配** 以打开 **标头会计分配** 页。
5. 返回到 **订单明细** 页，然后选择行。 从订单行明细还可以探索特定行的会计分配。

## <a name="complete-an-action-on-the-purchase-order"></a>完成对采购订单的操作
在查看分配给您的采购订单和阅读工作流说明后，应准备执行操作。

1. 在移动设备上，选择 **采购订单审核** 工作区。
2. 选择 **分配给我的订单** 以查看要求您在采购订单审核工作流中对其执行操作的所有采购订单。
3. 选择一个订单，然后查看详细信息页。
4. 选择 **操作** 以显示可用操作。 可用操作取决于分配给您的任务。

    | 任务操作    | 审核行为  |
    |----------------|------------------|
    | 已完成       | 审核          |
    | 退回         | 拒绝           |
    | 请求更改 | 请求更改   |
    | 委托人       | 委托人         |

5. 选择相应的操作。
6. 在 **完成任务** 页输入注释。 请注意，如果选择 **委托** 操作，必须选择要委托任务的用户。
7. 选择 **完成**。 刷新您的工作区后，采购订单不再显示在列表中。 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
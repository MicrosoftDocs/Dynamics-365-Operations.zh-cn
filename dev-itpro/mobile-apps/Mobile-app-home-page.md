---
title: "移动应用主页"
description: "此主题描述 Microsoft Dynamics 365 for Unified Operations 移动应用，并提供可以帮助您在组织中实施此应用的资源的链接。"
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: 663a03dc37cc1631bd285a76ef564993a34ed057
ms.contentlocale: zh-cn
ms.lasthandoff: 06/20/2017


---

# <a name="mobile-app-home-page"></a>移动应用主页

[!include[banner](../includes/banner.md)]

此主题描述 Microsoft Dynamics 365 for Unified Operations 移动应用，并提供可以帮助您在组织中实施此应用的资源的链接。

> [!NOTE]
> 此移动应用以前称为 *Microsoft Dynamics 365 for Finance and Operations*。

<a name="overview"></a>概览
--------

此移动应用让您的组织可以允许移动设备使用此应用的业务流程。 在您的 IT 管理员为您的组织启用此移动工作区后，用户可以登录到此应用并立即开始从其移动设备运行业务流程。 此移动应用包括可帮助提高生产率的以下功能：

- 用户可以查看、编辑并对业务数据进行操作，即使他们具有间歇的网络或其移动设备完全脱机。 在设备重新建立网络连接后，脱机数据操作自动与 Dynamics 365 for Finance and Operations Enterprise Edition 或 Microsoft Dynamics 365 for Finance and Operations 同步。
- IT 管理员或开发人员可以构建和发布为组织量身定制的移动工作区。 此应用使用您现有的代码资产。 因此，无需再次实施您的验证过程、业务逻辑或安全配置。
- IT 管理员或开发人员通过使用包含在 Web 客户端内的指向-点击工作区设计器轻松设计移动工作区。
- 通过使用业务逻辑可扩展性框架，IT 管理员或开发人员可以有选择地优化工作区的脱机功能。 由于数据在设备脱机时继续处理，移动方案仍然丰富、可变，即使设备没有固定的网络连接。

## <a name="elements-of-the-mobile-app"></a>移动应用的元素
移动应用的导航包括四个基本的概念：仪表板、工作区、页面和操作。 

[![移动应用的导航概念](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

1. 当您启动应用后，转到**仪表板**。
2. 在仪表板上，可以看到已发布的**工作区**。
3. 在各个工作区，您可看到该工作区可用的**页面**的列表。
4. 进入页面后，可以执行若干操作。 下面举了一些示例加以说明：

    - 查看详细数据。
    - 导航到相关数据的其他页面，如实体详细信息或行。
    - 参阅对该页面可用的**操作**列表。 操作允许您创建或编辑现有数据。

## <a name="implementation-process"></a>实施流程
下图显示实现由 Microsoft 和自定义移动工作区提供的两个移动工作区的流程。 

![移动应用实现流程](./media/Mobile-implementation-process-5.png)

下表包括可以帮助您实现由 Microsoft 和自定义移动工作区提供的两个移动工作区的资源的链接。 第一列的数字对应上一图中已编号的步骤。

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>步骤</th>
<th>角色</th>
<th>行动</th>
<th>帮助您完成操作的资源</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>系统管理员</td>
<td>实现 Finance and Operations 或您的组织中的 Finance and Operations。</td>
<td><ul><li>如果尚未部署 Microsoft Dynamics 365 的一个版本，请参阅<a href="../deployment/deploy-demo-environment.md">部署演示环境</a>。</li><li>若要查看可以使用的移动工作区的列表，请参阅<a href="mobile-workspaces-released.md">最近发布的移动工作区</a>。</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>系统管理员</td>
<td><strong>如果您使用的是 Microsoft Dynamics 365 for Finance and Operations 版本 1611：</strong>下载并安装启用 Microsoft 提供的移动工作区的 KB。</td>
<td>有关详细信息，请参阅以下主题：
<ul>

<li><a href="/dynamics365/unified-operations/financials/cost-accounting/cost-controlling-mobile-workspace">成本控制移动工作区</a></li>
<li><a href="/dynamics365/unified-operations/supply-chain/inventory/inventory-on-hand-mobile-workspace">现有库存量移动工作区</a></li>
<li><a href="/dynamics365/unified-operations/supply-chain/sales-marketing/sales-orders-mobile-workspace">销售订单移动工作区</a></li>
<li><a href="/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">供应商协作移动工作区</a></li>
<li><a href="/dynamics365/unified-operations/financials/project-management/project-time-entry-mobile-workspace">项目时间条目移动工作区</a></li>
<li><a href="/dynamics365/unified-operations/financials/expense-management/expense-management-mobile-workspace">费用管理移动工作区</a></li>

</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>系统管理员</td>
<td>发布 Microsoft 提供的移动工作区。</td>
<td><a href="publish-mobile-workspace.md">发布移动工作区</a>
</td>
</tr>
<tr class="even">
<td>4</td>
<td>开发商或独立软件供应商 (ISV)</td>
<td>使用移动框架创建自定义移动工作区。</td>
<td><ul>
<li><a href="mobile-platform.md">移动框架</a></li>
<li><a href="http://ax.help.dynamics.com/en/wiki/operations-mobile-workspace-x-apis/">工作区 X++ API</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ISV / 独立软件供应商</td>
<td>创建包含自定义移动工作区的可部署包，并上载包到 Microsoft Dynamics Lifecycle Services (LCS)。</td>
<td><a href="../deployment/create-apply-deployable-package.md">创建可部署包</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>系统管理员</td>
<td>应用包含独立软件供应商 (ISV) 提供的自定义工作区的可部署包。</td>
<td><a href="../deployment/apply-deployable-package-system.md">应用可部署包</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>系统管理员</td>
<td>发布 ISV 提供的自定义移动工作区。</td>
<td><a href="publish-mobile-workspace.md">发布移动工作区</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>用户</td>
<td>下载并安装移动应用。</td>
<td><ul>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850662">适用于 Android 手机</a></li>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850663">适用于 iPhones</a></li></ul>
</td>
</tr>
<tr class="odd">
<td>9</td>
<td>用户</td>
<td>登录并使用移动应用。 此应用中包括系统管理员已发布的移动工作区。</td>
<td>若要查看由 Microsoft 提供的移动工作区的列表，请参阅<a href="mobile-workspaces-released.md">最近发布的移动工作区</a>。
</td>
</tr>
</tbody>
</table>


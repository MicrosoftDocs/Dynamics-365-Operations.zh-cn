---
title: 发票审核移动工作区
description: 此主题提供有关发票审核移动工作区的信息。
author: abruer
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ac56dd8f6ecda669f32b298649da45634c5d83c9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360760"
---
# <a name="invoice-approvals-mobile-workspace"></a>发票审核移动工作区

[!include [banner](../includes/banner.md)]

此主题提供有关 **发票审核** 移动工作区的信息。 此工作区提供通过供应商发票抬头工作流程分配给您的发票的列表。 

此工作区应该与 Finance and Operations 移动应用结合使用。

## <a name="overview"></a>概览

**发票审核** 移动工作区让应付帐款职员和经理能够查看已作为供应商发票抬头工作流程的一部分分配给他们的发票。 您可以查看发票信息，甚至还可以查看行和分配详细信息，以帮助您做出合理的审核决定。 从工作区可以执行操作以通过工作流程移动发票。 

## <a name="prerequisites"></a>必备项

在使用此移动工作区之前，必须满足以下先决条件。

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
<td>必须在您的组织中部署 Microsoft Dynamics 365 Finance。</td>
<td>系统管理员</td>
<td>请查阅<a href="../deployment/deploy-demo-environment.md">部署演示环境</a>。
</td>
</tr>
<tr class="even">
<td>必须发布<strong>发票审核</strong>移动工作区。</td>
<td>系统管理员</td>
<td>请查阅<a href="publish-mobile-workspace.md">发布移动工作区</a>。</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>下载并安装移动应用

下载并安装 Finance and Operations 移动应用：

-   [适用于 Android 手机](https://go.microsoft.com/fwlink/?linkid=850662)
-   [适用于 iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>登录到移动应用

1.  在移动设备上启动应用程序。
2.  输入您的 Microsoft Dynamics 365 URL。
3.  首次登录时，将提示您输入您的用户名和密码。 输入凭据。
4.  登录后，将显示您的公司的可用工作区。 请注意，如果您的系统管理员以后发布新工作区，您必须刷新移动工作区列表。

    [![下拉以刷新。](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a>使用发票审核移动工作区审核发票
1.  在移动设备上，选择 **发票审核** 工作区。
2.  通过供应商发票抬头工作流程选择已经分配给您的发票。
3.  在 **发票详细信息** 页，查看发票抬头信息，如供应商和日期信息。
4.  选择发票上的一行以在 **发票行明细** 视图中查看关于它的更多详细信息。
5.  在 **发票行明细** 视图中，选择 **分配** 以查看行分配。 此处可以查看发票行的核算。 显示的信息包括财务维度和主科目。
6.  在 **发票详细信息** 页，选择 **分配** 以显示所有分配。 此处可以查看整个发票的核算。 显示的信息包括财务维度和主科目。 
7.  选择 **附件** 以查看附加到发票的所有附注或文件。
8.  在 **发票详细信息** 页，选择相应的工作流操作完成您的审核流程。
9.  选择 **完成**。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
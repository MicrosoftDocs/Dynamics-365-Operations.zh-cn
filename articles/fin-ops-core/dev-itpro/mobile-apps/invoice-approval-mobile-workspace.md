---
title: 发票审核移动工作区
description: 本文提供有关发票审核移动工作区的信息。
author: abruer
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4cc05d9fcea129cfb2ed8ed8df4bd4034a1fed4c
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066381"
---
# <a name="invoice-approvals-mobile-workspace"></a>发票审核移动工作区

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../includes/mobile-app-deprecation-banner.md)]

本文提供有关 **发票审核** 移动工作区的信息。 此工作区提供通过供应商发票抬头工作流程分配给您的发票的列表。 

此工作区应该与财务和运营移动应用程序结合使用。

## <a name="overview"></a>概述

**发票审核** 移动工作区让应付帐款职员和经理能够查看已作为供应商发票抬头工作流程的一部分分配给他们的发票。 您可以查看发票信息，甚至还可以查看行和分配详细信息，以帮助您做出合理的审核决定。 从工作区可以执行操作以通过工作流程移动发票。 

## <a name="prerequisites"></a>必备项

在使用此移动工作区之前，必须满足以下先决条件。

<table>
<thead>
<tr class="header">
<th>先决条件</th>
<th>角色</th>
<th>Description</th>
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

下载并安装财务和运营移动应用程序：

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


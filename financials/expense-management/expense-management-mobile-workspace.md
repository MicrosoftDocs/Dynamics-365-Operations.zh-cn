---
title: "费用管理移动工作区"
description: "此主题提供有关费用管理移动工作区的信息，用于 Microsoft Dynamics 365 for Operations 移动应用。 此工作区让用户能够捕获和上载收据，以便以后可以将其附加到支出报表。 移动工作区还允许用户使用附加的收据快速创建支出行。"
author: annbe
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: end user, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4e3202de8e5288bbd52e8c28922374de147cc99f
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="expense-management-mobile-workspace"></a>费用管理移动工作区

[!include[banner](../includes/banner.md)]


此主题提供有关费用管理移动工作区的信息，用于 Microsoft Dynamics 365 for Operations 移动应用。 此工作区让用户能够捕获和上载收据，以便以后可以将其附加到支出报表。 移动工作区还允许用户使用附加的收据快速创建支出行。

<a name="overview-of-the-expense-management-mobile-workspace"></a>费用管理移动工作区概览
---------------------------------------------------

很多组织要求收据副本附加到员工为获得补偿提交的差旅相关或业务相关的支出报表。 **费用管理**移动工作区让用户可以通过使用附加的收据照片在所选择的移动设备上快速创建新的支出行。 或者，用户可以捕获收据照片，然后以后再将其附加到支出报表。 具体而言，**费用管理**移动工作区支持用户：

-   拍摄收据照片，并上载到 Microsoft Dynamics 365 for Operations。 用户以后可以将该照片附加到支出报表。
-   作为捕获的收据上载文件。 用户以后可以将该文件附加到支出报表。
-   通过使用附加的收据创建新支出行。 用户以后可以将行项添加到支出报表，并提交进行审核和补偿。

本主题的其余部分说明如何实施和使用**费用管理**移动工作区。

## <a name="prerequisites"></a>必备项
在实施**费用管理**移动工作区之前，请确保您的系统管理员完成以下先决条件。

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
<td>必须实施 KB 4019015。</td>
<td>系统管理员</td>
<td>KB 4019015（X++ 更新或元数据修补程序）包含用于供应链管理的四个移动工作区。 若要实施 KB 4019015，系统管理员必须遵循这些步骤：
<ol>
<li>从 Microsoft Dynamics Lifecycle Services (LCS) 下载 KB 4019015。</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">安装元数据修补程序</a>。</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">创建</a>包含 <strong>ApplicationSuite</strong> 和 <strong>ExpenseMobile</strong> 模型的可部署包，然后将可部署包上载到 LCS。</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">将可部署包</a>应用到您的 Dynamics 365 for Operations 系统。</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>费用管理</strong>移动工作区必须发布到 Dynamics 365 for Operations 移动应用。</td>
<td>系统管理员</td>
<td><ol>
<li>在在您的浏览器中启动 Dynamics 365 for Operations。</li>
<li>在<strong>系统参数</strong>页面，选择<strong>管理移动工作区</strong>。</li>
<li>选择<strong>费用管理</strong>工作区。</li>
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

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>通过使用费用管理移动工作区捕获收据
1.  在移动设备上，选择**费用管理**工作区。
2.  选择**捕获收据**。
3.  选择**拍照**或**选择图像**。
4.  如果您选择了**拍照**，请执行以下步骤：
    1.  已将您带到移动设备的照相机，以便您可以拍摄收据照片。 在您完成拍照片时，请单击**确定**接受照片。
    2.  可选：为照片输入一个名称，并且输入任何注释。

     **或者：**如果您选择了**选择图像**，请执行以下步骤：
    1.  在列表中选择一个图像。
    2.  可选：为图像输入一个名称，并且输入任何注释。

5.  选择**完成**。

## <a name="quick-expense-entry-by-using-the-expense-management-mobile-workspace"></a>通过使用费用管理移动工作区快速输入费用
1.  在移动设备上，选择**费用管理**工作区。
2.  选择**快速输入费用**。
3.  选择支出类别。 将看到加载到您的应用程序中供脱机使用的支出类别的列表。 默认情况下，最多加载 50 项，但是开发人员可以更改此数字。 有关详细信息，开发人员应参阅[Dynamics 365 for Operations 移动平台](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)。 如果列表中不包含您的类别，请选择**搜索**，在 Dynamics 365 for Operations 中执行联机搜索。 按支出类别搜索，或切换到按支出类型搜索。
4.  输入支出的交易记录日期。
5.  可选：输入支出商家。
6.  输入支出金额。
7.  选择支出币种。 将看到加载到您的应用程序中供脱机使用的币种代码的列表。 默认情况下，最多加载 400 个币种，但是开发人员可以更改此数字。 有关详细信息，开发人员应参阅[Dynamics 365 for Operations 移动平台](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)。 如果列表中不包含您的币种，请选择**搜索**，在 Dynamics 365 for Operations 中执行联机搜索。 按币种搜索，或切换到按名称搜索。
8.  选择**拍照**或**选择图像**。
9.  如果选择了**拍照**，会将您带到移动设备的照相机，以便您可以拍摄收据照片。 在您完成拍照片时，请单击**确定**接受照片。  或者，如果您选择了**选择图像**，则在列表中选择一个图像。
10. 选择**完成**。







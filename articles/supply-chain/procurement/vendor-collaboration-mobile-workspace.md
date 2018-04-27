---
title: "供应商协作移动工作区"
description: "此主题提供有关供应商协作移动工作区的信息。 此工作区帮助您的供应商实时了解已经发送给他们进行审核的采购订单的最新信息。 它们还可以查看有关新的和更新的采购订单和联系人的信息。"
author: mkirknel
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: mkirknel
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 83fcf1d0432d5afa71d6f9d7d22cea5a583777bf
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="vendor-collaboration-mobile-workspace"></a>供应商协作移动工作区

[!INCLUDE [banner](../includes/banner.md)]

此主题提供有关**供应商协作**移动工作区的信息。 此工作区帮助您的供应商实时了解已经发送给他们进行审核的采购订单的最新信息。 它们还可以查看有关新的和更新的采购订单和联系人的信息。

将此工作区用于与 Microsoft Dynamics 365 for Unified Operations 移动应用一起使用。

## <a name="overview"></a>概览 
**供应商协作**移动工作区通知供应商有关新采购订单的信息，以便供应商可以在 Microsoft Dynamics 365 for Finance and Operations Web 客户端中查看和响应采购订单。 

>[!NOTE]
> 此移动工作区将用作供应商协作 Web 界面的补充，但不代替后者。 

您的供应商可以使用**供应商协作**移动工作区查看发送给他们进行审核的新采购订单。 其中显示采购订单信息，如产品、数量和请求的交货日期。 根据各供应商的配置决定是否显示价格信息。 

作为供应商登录的用户将看到已响应了哪些采购订单，以及哪些采购订单仍在等待客户操作。 例如，采购订单可能正在等待客户操作，因为供应商建议了其他交货日期，但客户尚未同意该日期。 供应商还将看到已确认但尚未交货的采购订单的列表。 

若要响应采购订单，供应商必须使用在 Web 客户端中提供的供应商协作 Web 界面。 供应商也可以在此处获取有关订单的更多信息，如票据附件、按行的交货地址，以及供应商的相关费用。 

具有特殊安全角色的供应商可以查看为供应商帐户注册了哪些联系人。 通过相同的安全角色，供应商可以查看已提交的任何用户请求的状态。 

必须使用 Web 客户端中的供应商协作 Web 界面创建新联系人和提交新用户请求。 

**供应商协作**移动工作区使供应商可以执行这些任务：

-   查看发送给供应商的新采购订单。
-   查看供应商已响应的采购订单和正在等待客户操作的采购订单。
-   查看已确认但尚未完全收货的采购订单。
-   查看为供应商帐户注册的联系人信息。 （此任务需要其他的安全角色。）
-   查看关于供应商已提交的用户请求的信息和跟踪请求的状态。 （此任务需要其他的安全角色。）

## <a name="prerequisites"></a>必备项
先决条件根据为您的组织部署的 Microsoft Dynamics 365 版本不同。

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a>使用 Microsoft Dynamics 365 for Finance and Operations 的先决条件 
如果已经为您的组织部署 Microsoft Dynamics 365 for Finance and Operations，系统管理员必须发布**供应商协作**移动工作区。 有关说明，请查阅 [发布移动工作区](../../dev-itpro/mobile-apps/publish-mobile-workspace.md)。

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
<td>如果您正在使用平台更新 3，则必须实施 KB 3216943。</td>
<td>系统管理员</td>
<td>KB 3216943 是您使用平台更新 3 时必需的二进制更新。 要实施此 KB，系统管理员必须遵循这些步骤。
<ol>
<li>从 Microsoft Dynamics Lifecycle Services (LCS) 下载 KB 3216943。</li>
<li>安装交货为可部署包的二进制更新。 有关如何应用可部署包的信息，请参阅 <a href="../../dev-itpro/deployment/apply-deployable-package-system.md">应用可部署包</a>。</li>
</ol></td>
</tr>
<tr class="even">
<td>必须实施 KB 4013633。</td>
<td>系统管理员</td>
<td>KB 4013633 是包含<strong>现有库存量</strong>移动工作区的 X++ 更新或元数据修补程序。 若要实施 KB 4013633，系统管理员必须遵循这些步骤。
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">从 LCS 下载元数据修补程序</a>。</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">安装元数据修补程序</a>。</li><li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">创建</a>包含 <strong>SCMMobile</strong> 模型的可部署包，然后将可部署包上载到 LCS。</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">应用可部署包</a>。</li>
</ol></td>
</tr>
<tr class="odd">
<td>必须发布<strong>供应商协作</strong>移动工作区。</td><td>系统管理员</td>
<td>请查阅<a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">发布移动工作区</a>。</td>
</tr>
<tr class="even">
<td>供应商用户必须有权访问 Web 客户端中的供应商协作 Web 界面和设置供应商协作用户。</td><td>专业采购人员和系统管理员</td>
<td>请按照以下主题中的步骤设置和使用供应商协作 Web 界面。
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">使用供应商协作与外部供应商合作</a></li>
<li><a href="manage-vendor-collaboration-users.md">管理供应商协作用户</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">设置和维护供应商协作</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">使用供应商协作在 Finance and Operations 中与客户合作</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>下载并安装移动应用

下载并安装 Dynamics 365 for Unified Operations 移动应用：

-   [适用于 Android 手机](https://go.microsoft.com/fwlink/?linkid=850662)
-   [适用于 iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>登录到移动应用
1.  在移动设备上启动应用程序。
2.  输入您的 Microsoft Dynamics 365 URL。
4.  首次登录时，将提示您输入您的用户名和密码。 输入凭据。
5.  登录后，将显示您的公司的可用工作区。 请注意，如果您的系统管理员以后发布新工作区，您必须刷新移动工作区列表。

    [![下拉以刷新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="use-the-vendor-collaboration-mobile-workspace"></a>使用供应商协作移动工作区
当您选择**供应商协作**工作区时，您将看到以下选项。

![供应商协作移动工作区](./media/vendor-collaboration-mobile-app.png)

**供应商协作**工作区包括以下页面。

### <a name="contacts"></a>联系人
**联系人**页面将显示已为供应商帐户设置的所有联系人。 显示联系人的姓名、要电子邮件地址和用户别名（如果联系人具有别名）。 此页还显示联系人的用户帐户是否有效。 在您选择联系人时，将会看到联系人详细信息，例如该人士作为其联系人的法人。 您还可以查看联系信息，如电话号码或备选电子邮件地址。

### <a name="user-requests"></a>用户请求
可通过**用户请求**页面查看您已通过供应商协作 Web 界面提交的所有用户请求。 还可以跟踪这些请求的状态。 选择用户请求时，可以查看请求的内容，添加或停用用户，更改安全性，以及查看为用户注册了哪些安全角色。

### <a name="purchase-orders-ready-for-review"></a>准备就绪可供审核的采购订单
可通过**准备就绪可供审核的采购订单**页面查看客户已发送但尚未响应的采购订单。 可查看有关此类订单的选定信息，如请求了哪些产品和何时交货。 根据供应商的配置决定是否显示价格信息。

还可查看采购订单是否有附注或附件。 但是，要打开注释和附件，必须使用 Web 客户端中的供应商协作 Web 界面。 选择**采购订单行**以查看所有行及其明细。 对于每行，将有一个指示器显示是否有注释或附件，或者交货地址是否与抬头中所示的交货地址不同。

若要响应采购订单，必须使用 Web 客户端中的供应商协作 Web 界面。

### <a name="awaiting-customer-action"></a>正在等待客户操作
可通过**正在等待客户操作**页面查找您或您公司中有权访问供应商协作的其他人已响应的采购订单。 仅当客户必须对采购订单执行以下操作之一时，才在此列表中显示采购订单。

-   如果已拒绝了采购订单，客户必须更新或取消原始订单，然后再重新发送。 再次发送采购订单后，将不再显示在**正在等待客户操作**页上。
-   如果接受了带更改的采购订单，客户必须更新原始订单并重新发送供审核，或根据请求的更改更新订单并立即确认。 在两种情况下，采购订单都不再显示在**正在等待客户操作**页上。
-   如果采购订单已被接受但仍显示在**正在等待客户操作**页上，则在接受采购订单时未自动确认采购订单。 它现在在等待采购代理将订单状态更改为**已确认**。 一旦供应商接受了订单，通常将把采购订单视为客户与供应商之间的协议。 因此，更新至**已确认**状态通常只是一种形式。

选择采购订单后，将显示有关响应的更多详细信息。 可查看每行的行明细和响应。 行状态显示已提供了以下响应中的哪些响应：

-   已接受
-   已拒绝
-   已接受更改
-   已替代/替代
-   拆分为计划/计划行

请注意，**交货**字段设置为**是**或**否**以指示行是否要完全交货。 行可能因为以下原因而无法交货：

- 行被拒绝。
- 已进行替换，且预计原始行不会按照已接收订单中的请求交货。
- 行拆分为多个计划行，且预计原始行不会按照已接收订单中的请求交货。

显示已对订单行响应做出的任何更改。 但是不显示已上载的注释和附件。 要查看注释和附件，必须使用 Web 客户端中的供应商协作 Web 界面。

### <a name="open-confirmed-orders"></a>打开已确认的订单
客户确认了采购订单之后（即采购订单的状态已更改为**已确认**），将显示在未结已确认订单中。 它将一直留在列表中，直到客户将其登记为已收货。


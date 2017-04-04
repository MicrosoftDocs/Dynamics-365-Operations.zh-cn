---
title: "Microsoft Dynamics 的 365 个供应商协作移动应用工序的工作区"
description: "供应商协作将工作区，您的供应商可以掌握最新。送给他们进行审核和显示有关新和更新采购订单和联系人信息的采购订单。"
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 36 - 37
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: fe8e912d-8446-4584-8a24-d8892e9028cd
ms.search.region: global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 9f441508b745d22218316128572c9ec6aeb7207b
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Microsoft Dynamics 的 365 个供应商协作移动应用工序的工作区

供应商协作将工作区，您的供应商可以掌握最新。送给他们进行审核和显示有关新和更新采购订单和联系人信息的采购订单。

<a name="prerequisites"></a>先决条件
-------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>必备项</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>工序闻悉移动电话平台的 Microsoft Dynamics 365</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">工序移动电话平台的 Dynamics 365</a></td>
</tr>
<tr class="even">
<td>工序的 Dynamics 365</td>
<td>请确保已经使用具有工序的工序平台的更新版本 3 的环境 (2016 年 11 月 Microsoft Dynamics 365 和 Microsoft Dynamics 1611)。</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">安装了工序的 Dynamics 365 应用的移动设备</span></td>
<td><span style="color: #000000;">下载工序的 Dynamics 365 应用从您所移动应用商店。</span></td>
</tr>
<tr class="even">
<td>3215650 KB 修补程序</td>
<td>修补程序安装可以在 Dynamics 365 提供要为工序的工作区。</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">3216943 KB 修补程序</span></span></td>
<td>设置启用新的供应商协作移动电话工作区。</td>
</tr>
<tr class="even">
<td>供应商必须有权用户访问供应商协作 Web 界面的 Dynamics 中的工序和 365 设置供应商协作用户。</td>
<td>按照以下主题介绍的设置步骤和与供应商协作 Web 界面一起使用。
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">使用供应商工作与外部供应商协作</a></li>
<li><a href="manage-vendor-collaboration-users.md">管理供应商协作用户</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">设置和维护供应商协作</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">使用供应商协作使用 Dynamics 的客户 365 的工序</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>概览
供应商协作将工作区维护供应商收到与新的采购订单，以使它们可以查看和响应 Dynamics 中 365 的采购订单。工序网络客户端。  

**注释：**应将使用工作区以添加权限供应商协作 Web 界面，而不是更改。  

供应商协作将工作区，您的供应商可以显示发送以供审核新采购订单。 它显示采购订单信息，例如产品、数量和请求交货日期。 价格信息根据配置，可为每个供应商。  

在用户登录为供应商，都查看哪些采购订单响应到，或哪些采购订单仍等待客户"操作。 供应商可能已经授予客户不建议的采购订单，因此等待操作客户的另一个交货日期。 供应商也将看到确认，但尚未交货采购订单的列表。  

若要响应采购订单，供应商必须使用作为可用在 Dynamics 365。工序网络客户端供应商协作 Web 界面。 这也是供应商。获取有关订单的更多信息，如记录的附件，文档与供应商的交货地址。行和费用的位置。  

特定的安全角色，联系人为供应商帐户注册的供应商进行查看。 相同的安全角色，供应商可以查看提交所有用户请求的状态。  

在 Dynamics 中可用 365。工序网络客户端供应商协作界面必须执行新联系人创建和提交新的用户请求。  

将工作区，您的供应商可以：

-   查看新采购订单发送给供应商。
-   查看响应到的供应商采购订单并等待操作客户。
-   查看"确认的状态而非已完全收到的采购订单。
-   查看为供应商帐户注册的联系人信息 (要求一个附加的安全角色。)
-   显示信息并按照供应商提交用户请求的状态 (要求一个附加的安全角色。)

## <a name="get-started"></a>开始
开始在您的移动设备：

1.  在您移动应用的商店，请下载和安装 Microsoft Dynamics 365 应用的工序。
2.  开始在您的设备上应用。
3.  输入您的 Dynamics 365 URL。
4.  输入公司登录。 例如，输入 USMF ** **。
5.  首次登录的实例，则将提示您输入用户名和密码。您的 Microsoft Dynamics 365 数据的会计的。 

在应用登录后，工作区不可见。 若要查看您在移动应用的工作区，必须首先过帐预期工作区到 Dynamics 365 应用的工序。 您需要系统管理权限过帐工作区。

1.  的工序启动 Dynamics 365。
2.  **是系统管理** &gt; **设置** &gt; ** **系统参数。
3.  **选择请管理移动应用**。
4.  选择工作区**供应商协作**发布到移动平台。
5.  **选择请过帐工作区**。
6.  刷新您的设备查看过帐工作区的。
7.  **选择供应商协作**工作区。 将以下页面。

[![供应商协作] (移动应用。/media/vendor 协作移动 app.png)](。/media/vendor 协作移动 app.png)

## <a name="contacts"></a>联系人
**联系人**页可以查看为供应商帐户设置的所有联系人。 如果有联系人的姓名、它显示主要电子邮件别名，和用户。 它还查看联系人的用户帐户是有效的。 在您选择联系人时，将会看到哪些信息，如联系人详细的法人人员为联系人和联系信息 (如电话号码或不同的电子邮件地址。

## <a name="user-requests"></a>用户请求
**用户请求**页面可以查看供应商协作您通过 Web 界面而提交的所有用户请求和遵守状态。 当您选择用户请求时，您可以看到就，添加请求或停用用户，更改安全，并且查看哪些安全角色用户请求。

## <a name="purchase-orders-ready-for-review"></a>采购订单可供审核
**采购订单可供审核**页面可以查看按客户发送的所有采购订单和已回答。 您可以查看与该订单有关，产品什么时候的所选信息请求和交货。 如果已经为供应商，配置价格信息才可用。  

可以查看采购订单是否存在或注释附加。 若要打开附件，您可以在该 Web 客户端需要使用供应商协作。 **选择采购订单行**看到具有详细信息的所有行。 请注意，对于每个行，指示器显示是否具有或注释附加或者，如果具有不同的交货地址在标题上显示。  

若要响应采购订单，所以必须使用供应商协作 Web 客户端。

## <a name="awaiting-customer-action"></a>正在等待客户操作
**客户正在等待操作**页可以找到您或某人在您的公司中也访问供应商协作的，响应的采购订单。 如果客户需要对采购订单的以下操作之一，采购订单可见{{在此：in}}列表。

-   如果拒绝采购订单，客户或需要更新该发送的订单并再次发送，或者取消订单并重新发送。 采购订单时再次发送，则它从**客户正在等待操作**页面将消失。
-   如果接受了含有更改采购订单，客户需要更新原始订单和供审核未能发出，或根据更改更新它并立即确认它。 在这两种情况下，采购订单从**客户正在等待操作**页面将消失。
-   如果采购订单已接受和显示在**客户正在等待操作**页，它是，因为采购订单自动在未确认，接受该完成。 等待它一个采购代理订单更改为"已确认"。 通常，接受供应商采购订单订单，将认为在客户和供应商之间的协议。 将给确认采购订单的状态有"窗体。

选择采购订单，通过附加详细信息显示有关响应。 您可以为每一查看行明细和响应。 查看授予以下哪些行状态响应。

-   已接受
-   已拒绝
-   已接受更改
-   覆盖/替代
-   拆分计划到/计划中的行

注意指示器显示**传递** =yes/no，用于指示行不会交付。 这可能适合，因为该行，或者拒绝覆盖原始行不会交付的位置，或拆分为多个行计划和原始行的预期行不{{按照：as_requested_in}}该接收的订单要求的交货。  

进行的任何更改将响应订单行显示，除上载的注释和附件，则将使用供应商协作 Web 界面，则您可看到一列。

## <a name="open-confirmed-orders"></a>打开命令的确认
当采购订单按客户确认，也就是说采购订单更改为确认状态。打开的，确认的顺序将与下面。 在列表将维护，直到该接收由登记为客户。



---
title: "Microsoft Dynamics 365 for Operations 应用程序的供应商协作移动工作区"
description: "通过供应商协作移动工作区，供应商可以掌握已发送给其审核的采购订单的最新信息，以及查看有关新的和更新后的采购订单和联系人的信息。"
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

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Microsoft Dynamics 365 for Operations 应用程序的供应商协作移动工作区

通过供应商协作移动工作区，供应商可以掌握已发送给其审核的采购订单的最新信息，以及查看有关新的和更新后的采购订单和联系人的信息。

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
<td>了解 Microsoft Dynamics 365 for Operations 移动平台</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Dynamics 365 for Operations 移动平台</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 for Operations</td>
<td>确保使用的环境中已安装了 Microsoft Dynamics 365 for Operations 版本 1611 和 Microsoft Dynamics for Operations 平台更新 3（2016 年 11 月）。</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">已安装了 Dynamics 365 for Operations 应用程序的移动设备</span></td>
<td><span style="color: #000000;">从移动应用商店下载 Dynamics 365 for Operations 应用程序。</span></td>
</tr>
<tr class="even">
<td>修补程序 KB 3215650</td>
<td>安装此修补程序以启用 Dynamics 365 for Operations 中提供的工作区。</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">修补程序 KB 3216943</span> </span></td>
<td>安装此修补程序以启用供应商协作移动工作区。</td>
</tr>
<tr class="even">
<td>供应商用户必须有权访问 Dynamics 365 for Operations 中的供应商协作 Web 界面和设置供应商协作用户。</td>
<td>请执行以下主题中介绍的步骤设置和使用供应商协作 Web 界面。
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">使用供应商协作与外部供应商合作</a></li>
<li><a href="manage-vendor-collaboration-users.md">管理供应商协作用户</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">设置和维护供应商协作</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">使用供应商协作在 Dynamics 365 for Operations 中与客户合作</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>概览
供应商协作移动工作区通知供应商有关新采购订单的信息，以便供应商可以在 Dynamics 365 for Operations Web 客户端中查看和响应采购订单。  

**注释：**此移动工作区将用作供应商协作 Web 界面的补充，但不代替后者。  

通过供应商协作移动工作区，供应商可以查看发送供审核的新采购订单。 其中显示采购订单信息，如产品、数量和请求的交货日期。 根据各供应商的配置决定是否显示价格信息。  

用户作为供应商登录时，将看到已响应了哪些采购订单，或者哪些采购订单仍在等待客户操作。 供应商可能已建议了尚未与客户达成一致的其他交货日期，因此采购订单在等待客户操作。 供应商还将看到已配置但尚未交货的采购订单的列表。  

若要响应采购订单，供应商必须运行 Dynamics 365 for Operations Web 客户端中提供的供应商协作 Web 界面。 供应商也可以在此处获取有关订单的更多信息，如票据附件、按行的交货地址，以及供应商的相关费用。  

通过使用特殊的安全角色，供应商可以查看为供应商帐户注册了哪些联系人。 通过相同的安全角色，供应商可以查看已提交的任何用户请求的状态。  

新建联系人和提交新用户请求必须在 Dynamics 365 for Operations Web 客户端中提供的供应商协作界面内进行。  

通过此移动工作区，供应商可以：

-   查看发送给供应商的采购订单。
-   查看供应商已响应的采购订单和正在等待客户操作的采购订单。
-   查看已确认状态的采购订单和尚未完全收货的采购订单。
-   查看为供应商帐户注册的联系人信息（需要额外的安全角色）。
-   查看信息和跟踪供应商提交的用户请求的状态（需要额外的安全角色）。

## <a name="get-started"></a>开始
若要在移动设备上开始：

1.  在移动应用商店中，下载并安装 Microsoft Dynamics 365 for Operations 应用程序。
2.  在设备上启动应用程序。
3.  输入您的 Dynamics 365 URL。
4.  输入要登录的公司。 例如，输入 **USMF**。
5.  首次登录时，系统将提示您提供您的 Microsoft Dynamics 365 for Operations 帐户用户名和密码。 

登录此应用程序之后，将不显示任何工作区。 若要在移动应用程序中查看工作区，必须先将所需工作区发布到 Dynamics 365 for Operations 应用程序。 需要系统管理权限才能发布此工作区。

1.  启动 Dynamics 365 for Operations。
2.  转到**系统管理** &gt; **设置** &gt; **系统参数**。
3.  选择**管理移动应用程序**。
4.  选择**供应商协作**工作区以发布到移动平台。
5.  选择“**发布工作区**”。
6.  刷新设备以查看发布的工作区。
7.  选择**供应商协作**工作区。 将显示以下页面。

[![供应商协作移动应用](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>联系人
**联系人**页面将显示已为供应商帐户设置的所有联系人。 其中显示联系人姓名、主要电子邮件，以及用户别名（如果有）。 还显示联系人的用户帐户是否有效。 选择联系人时，将显示联系人详细信息（如该人是哪些法人的联系人），以及联系信息（如电话号码或其他电子邮件地址）。

## <a name="user-requests"></a>用户请求
可通过**用户请求**页面查看您已通过供应商协作 Web 界面提交的所有用户请求，并跟踪状态。 选择用户请求时，可以查看请求的内容，添加或停用用户，更改安全性，以及查看为用户注册了哪些安全角色。

## <a name="purchase-orders-ready-for-review"></a>准备就绪可供审核的采购订单
可通过**准备就绪可供审核的采购订单**页面查看客户已发送但尚未被回应的采购订单。 可查看有关此类订单的选定信息，如请求了哪些产品和何时交货。 仅当为供应商配置了价格信息，才显示价格信息。  

可查看采购订单是否有通知或附件。 若要打开附件，需要使用 Web 客户端中的供应商协作。 选择**采购订单行**以查看所有行和明细。 请注意，对于每行，将有一个指示器显示是否有通知或附件，或者是否有与抬头中所示不同的交货地址。  

若要响应采购订单，必须使用供应商协作 Web 客户端。

## <a name="awaiting-customer-action"></a>正在等待客户操作
可通过**正在等待客户操作**页面查找您或您公司中也有权访问协作的某人已响应的采购订单。 仅当客户需要对采购订单执行以下操作之一时，才在此列表中显示采购订单。

-   如果已拒绝了采购订单，客户需要更新发送的订单，然后再次发送，或者取消订单并重新发送。 再次发送采购订单后，采购订单将从**正在等待客户操作**页面中消失。
-   如果接受了带更改的采购订单，客户需要更新原始订单并重新发送供审核，或根据更改更新订单并立即确认。 在两种情况下，采购订单都将从**正在等待客户操作**页面中消失。
-   如果采购订单已被接受且在**正在等待客户操作**页面中显示，这是因为执行接受时，未自动确认采购订单。 它在等待采购代理将订单更改为“已确认”。 一旦供应商接受了订单，通常将把采购订单视为客户与供应商之间的协议。 将采购订单的状态设置为“已确认”是一项正式行为。

如果选择采购订单，将显示有关响应的更多详细信息。 可查看每行的行明细和响应。 行状态显示已提供了以下响应中的哪些。

-   已接受
-   已拒绝
-   已接受更改
-   已替代/替代
-   拆分为计划/计划行

请注意，一个指示器显示**交货**=是/否，用于指示行尚未交货。 这可能是因为拒绝或替换了符合以下条件的行：不应为原始行交货，或者行已拆分为多个计划行，并且原始行不应按照所接收订单中的请求交货。  

将显示对订单行响应所做任何更改，除了更新后的通知和附件，可通过使用供应商协作 Web 界面查看这些通知和附件。

## <a name="open-confirmed-orders"></a>开立已确认的订单
客户确认了采购订单之后（即采购订单的状态已更改为“已确认”），将在已确认但未结订单中显示该采购订单。 它将一直留在列表中，直到客户将其登记为已收货。



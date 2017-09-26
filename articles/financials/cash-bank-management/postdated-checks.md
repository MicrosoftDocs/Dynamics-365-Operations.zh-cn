---
title: "远期支票"
description: "本文提供有关 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中远期支票的支持的信息。 远期支票是签发用于在将来时间进行付款和收款的支票。 因此，支票在指定日期前不能兑现。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 45d28110ca93875eb534c69886ac2074ea4fe737
ms.openlocfilehash: 6a535b5f1192b7c27383cb8ece53f76a9c76f047
ms.contentlocale: zh-cn
ms.lasthandoff: 08/09/2017

---

# <a name="postdated-checks"></a>远期支票

[!include[banner](../includes/banner.md)]


本文提供有关 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中远期支票的支持的信息。 远期支票是签发用于在将来时间进行付款和收款的支票。 因此，支票在指定日期前不能兑现。

Microsoft Dynamics 365 for Finance and Operations 支持应收帐款和应付帐款中远期支票的完整管理周期，如下表中所示。
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>方案</th>
<th>明细</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>设置远期支票</td>
<td>您必须设置新的付款方式，并为已签发支票、收到的支票和预缴税金的结算帐户指定付款流程。</td>
</tr>
<tr class="even">
<td>为供应商登记和过帐远期支票</td>
<td>登记您向供应商签发的远期支票的详细信息。 在过帐付款时，识别供应商负债，不过，银行帐户不是贷方。 相反，结算帐户用于此目的。 </td>
</tr>
<tr class="odd">
<td>为客户登记和过帐远期支票</td>
<td>登记您从客户处接收的远期支票的详细信息。 在过帐付款时，应收客户是贷方，但银行帐户不是借方。 相反，结算帐户用于此目的。</td>
</tr>
<tr class="even">
<td>为客户或供应商登记和过帐更换远期支票</td>
<td>
如果您给供应商或从客户处收到的原始支票已丢失或损坏，您可以签发替代远期支票给供应商。 当您登记该支票的详细信息后，提供参考给该原始支票并指示新支票是原始支票的替代。 您也可以过账替代支票。</td>
</tr>
<tr class="odd">
<td>将客户远期支票转移到供应商</td>
<td>当您从客户处接收了一张远期发票时，您可以将该支票作为付款转移到供应商。</td>
</tr>
<tr class="even">
<td>结算客户或供应商的远期支票</td>
<td>当支票最后到期时，结算过帐到客户或供应商的过渡帐户的远期支票。 在结算支票时，银行根据之前使用的结算帐户为最后借方或贷方。</td>
</tr>
<tr class="odd">
<td>取消供应商的远期支票</td>
<td>您可以在以下情况下取消已过帐的远期支票: - 银行退回了支票。
- 该支票被应用于不正确的发票。
- 现金支付是针对发票而存在的。
</td>
</tr>
<tr class="even">
<td>停止远期支票付款</td>
<td>您可以停止对签发给供应商的远期支票的付款，原因可以是资金不足、与供应商的协议更改、供应商提供残次货物或货物返还给了供应商等。 您只能停止未清算的支票上的付款。</td>
</tr>
</tbody>
</table>



有关详细信息，请参阅以下主题：

[设置远期支票](tasks/set-up-postdated-checks.md)

[为客户登记和过帐远期支票](tasks/register-post-postdated-check-customer.md)

[结算客户的远期支票](tasks/settle-postdated-check-customer.md)

[为供应商登记和过帐远期支票](tasks/register-post-postdated-check-vendor.md) 

[结算供应商的远期支票](tasks/settle-postdated-check-vendor.md)





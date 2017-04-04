---
title: "远期支票"
description: "文章此日期为远期提供有关支持的工序信息签入的 Microsoft Dynamics 365。 远期支票是签发用于在将来时间进行付款和收款的支票。 因此，支票在指定日期前不能兑现。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 7349771b7f9a1ad4cd5b239f1d10bd3229d2d0df
ms.lasthandoff: 03/31/2017


---

# <a name="postdated-checks"></a>远期支票

文章此日期为远期提供有关支持的工序信息签入的 Microsoft Dynamics 365。 远期支票是签发用于在将来时间进行付款和收款的支票。 因此，支票在指定日期前不能兑现。

如下表所示，工序 365 的 Microsoft Dynamics 支持远期日期的完整周期管理签入，应收帐款和应付帐款。
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
<td>登记您向供应商签发的远期支票的详细信息。 在过帐付款时，供应商负债中具结，银行账户，但不为贷方。 相反，结算帐户用于此目的。</td>
</tr>
<tr class="odd">
<td>为客户登记和过帐远期支票</td>
<td>登记您从客户处接收的远期支票的详细信息。 在过帐付款时，应客户收取的是贷方，银行账户，但不为借记。 相反，结算帐户用于此目的。</td>
</tr>
<tr class="even">
<td>登记和过帐客户或供应商进行的更改远期支票的日期</td>
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
<td>在这些情况下您可以取消某一过帐的远期支票的日期：支票-返回已由银行。
- 检查应用于发票不正确。
- 现金支付。支票支付
</td>
</tr>
<tr class="even">
<td>一远期支票的止付的日期</td>
<td>您可以停止对签发给供应商的远期支票的付款，原因可以是资金不足、与供应商的协议更改、供应商提供残次货物或货物返还给了供应商等。 您只能止付对于尚未清除的支票。</td>
</tr>
</tbody>
</table>






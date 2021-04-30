---
title: 应计预订
description: 使用服务预订，您可以在费用交易记录开票日期后的期间中手动计入收入。
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a2b581c8ae52f4c379e8e511dc898a8d106d149
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908052"
---
# <a name="accruing-subscriptions"></a>应计预订 

[!include [banner](../includes/banner.md)]


使用服务预订，您可以在费用交易记录开票日期后的期间中手动计入收入。

为您为预订费用设置的发票期间创建应计期间，并且应计期间基于预订的期间代码。

您可以计入或冲销应计收入。

## <a name="reverse-accruals-of-credit-amounts"></a>贷方金额冲销应计

如果您贷记已开票的预订金额，则可以使用两种方法冲销应计金额：

  - 在创建交易记录的贷方通知单方案之前，您可以逐个冲销每个应计收入交易记录。 此方法是手动方法。 手动

  - 您可以具有在过帐贷方通知单的日期或在应计的原始过帐日期冲销的应计金额。

有关详细信息，请参阅[预订参数（窗体）](/dynamicsax-2012//subscription-parameters-form)。

## <a name="setup-requirements"></a>设置需求

若要应计收入，请确保满足以下数据要求：

## <a name="account-setup"></a>帐户设置

必须在 **项目** 模块中设置 **WIP - 预订** 和 **应计收入 - 预订** 科目。

在您过帐应计收入时，**WIP - 预订** 科目使用应计金额借记，而 **应计收入 - 预订** 科目使用应计金额贷记。

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a>为预订收入应计设置帐户

1.  单击 **项目管理与核算** \> **设置** \> **过帐** \> **分类帐记帐设置**。

2.  单击 **收入科目** 选项卡中，选择 **WIP - 预订** 或 **应计收入 - 预订** 设置科目。

## <a name="subscription-group-setup"></a>预订组设置

为了能够为预订应计收入，必须选中 **应计收入** 复选框。 这在附加到预订组的 **预订组** 窗体中找到。 单击 **服务管理** \> **设置** \> **服务预订** \> **预订组**。

## <a name="enable-revenue-accrual-on-a-subscription-group"></a>针对预订组启用收入应计

1.  单击 **服务管理** \> **设置** \> **服务预订** \> **预订组**。

## <a name="periods"></a>期间

您必须设置开票期间代码。 除非您想在您用于开票的同一时间间隔内应计收入，否则，还必须设置应计期间。

下表提供为每个开票期设置应计期间的概览:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>开票期</p></th>
<th><p>应计期间</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>年</strong></p></td>
<td><ul>
<li><p><strong>年</strong></p></li>
<li><p><strong>季度</strong></p></li>
<li><p><strong>月</strong></p></li>
<li><p><strong>天</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>季度</strong></p></td>
<td><ul>
<li><p><strong>季度</strong></p></li>
<li><p><strong>月</strong></p></li>
<li><p><strong>天</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>月</strong></p></td>
<td><ul>
<li><p><strong>月</strong></p></li>
<li><p><strong>天</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>周</strong></p></td>
<td><ul>
<li><p><strong>天</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>天</strong></p></td>
<td><ul>
<li><p><strong>天</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>

设置开票期间是整个预订组设置的一部分。 您可以决定是否也要设置预订组的应计期间。 如果您设置预订组的应计期间，在 **期间代码** 字段提供此期间。 当您应计预订收入时，此字段在 **应计预订收入** 窗体中找到。 但是，应计期间是与预订组有关的可选信息。


> [!NOTE]
> <P>可使用以下路径打开<STRONG>应计预订收入</STRONG>窗体。 单击<STRONG>服务管理</STRONG> &gt; <STRONG>定期</STRONG> &gt; <STRONG>服务预订</STRONG> &gt; <STRONG>应计预订收入</STRONG>。</P>


## <a name="transactions"></a>交易

在您过帐应计收入时，您可以控制创建分录的数量。 在预订时，如果分类帐交易记录应创建为合计或每行，则定义。

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a>指定要为应计交易记录显示的过帐明细的级别

1.  单击 **项目管理与核算** \> **设置** \> **项目管理与核算参数**。

2.  在 **财务** 选项卡的 **发票** 字段中，选择 **总计** 或 **行**。


## <a name="see-also"></a>请参阅

[应计预订收入](accrue-subscription-revenue.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
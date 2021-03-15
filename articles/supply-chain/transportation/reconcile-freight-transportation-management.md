---
title: 在运输管理中对运费进行对帐
description: 本主题介绍了运费对帐流程。
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac07155e4dde77689b1994abfb8b30f45d5a5a30
ms.sourcegitcommit: b6686265314499056690538eaa95ca51cff7c720
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5014500"
---
# <a name="reconcile-freight-in-transportation-management"></a>在运输管理中对运费进行对帐

[!include [banner](../includes/banner.md)]

本主题介绍了运费对帐流程。

可以手动完成运费对帐或可以设置为自动发生。 若要使用自动运费对帐，您必须设置审计主数据，在其中可以定义确定自动匹配哪些运费帐单的条件。

## <a name="the-freight-reconciliation-process"></a>运费对帐流程

运费费率由与相关装运承运人相关的费率引擎来计算。 确认负荷后，将生成运费帐单，运费费率被转移到该帐单。 运费费率作为其他费用分摊到相关的原始凭证（采购订单、销售订单和/或转移单），根据用于常规计费流程的设置。 从装运承运人收到运费发票后，就立即可以开始运费对帐流程（这也称为匹配流程）。 可以以电子方式或使用纸张接收发票。 如果使用纸张接收发票，可以通过将运费帐单作为模板使用来生成电子发票。

[![运费对帐流程](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>手动对帐

如果要手动对帐运费，必须将每个发票行与已开票负荷的运费帐单行匹配。 您在 **运费帐单和发票匹配** 页进行此匹配。 如果发票行上的金额与运费帐单金额不匹配，则必须选择上差异对帐原因。 如果有多个对帐原因，您可以在它们之间拆分不匹配的金额。 对帐原因确定如何在总帐中过帐差异金额。 当对帐所计算的整个发票金额时，将金额提交供审批，然后过帐日记帐。 下图显示了如何生成运费发票和执行运费对帐。

[![运费对帐任务](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)

## <a name="automatic-reconciliation"></a>自动对帐

若要使用自动对帐，您必须指定对帐计划和发票，以及要使用的装运承运人。 发票行和运费帐单的匹配根据审计主数据和运费帐单类型的设置进行。 运行自动对帐后，必须处理所有系统不能匹配的发票。 然后，您必须手动处理这些发票，然后才能过帐所有付款发票。

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a>使用自动或手动对帐将运费帐单与运费发票进行匹配

*匹配* 是查找与每个运费发票相对应的运费帐单的流程。 这可以通过逐一匹配发票行（手动匹配）或一次匹配所有可用发票（自动匹配）来完成。

### <a name="auto-matching"></a>自动匹配

将多个运费发票与同一运费帐单匹配时，自动匹配的流程如下：

1. 所有未匹配的运费发票按金额排序，金额最大的在最前面。
1. 逐一匹配运费发票，直到运费帐单上没有剩余正金额。
1. 根据审计主数据的设置和运费发票上的剩余金额，设置剩余金额。

### <a name="manual-matching"></a>手动匹配

所有带有正金额的运费帐单都可以进行匹配。 与自动匹配相似，用户只能将带有负金额的运费发票与未完全匹配的运费帐单进行匹配。

### <a name="example"></a>示例

假设您有一个金额为 1500 的运费帐单 (FB)，并且已为该运费帐单创建了三个运费发票，每个发票有一个发票行，并进行了以下设置：

- 原始运费帐单 (FB)：金额 1500
- 发票 1 (Inv1)：金额 1000
- 发票 2 (Inv2)：金额 600
- 发票 3 (Inv3)：金额 -100

#### <a name="automatic-matching-result"></a>自动匹配结果

自动匹配将按以下顺序执行：

1. 按金额降序排列所有运费发票：Inv1 -> Inv2 -> Inv3。
1. 将 Inv1 与 FB 匹配。 Inv1 匹配了 1000，FB 有 500 剩余金额，因此状态设置为 *部分匹配*。
1. 将 Inv2 与 FB 匹配。 Inv2 匹配了 500，FB 有 0 剩余，因此状态设置为 *完全匹配*。
1. 由于 FB 现在已完全匹配，因此不会处理 Inv3。

#### <a name="manual-matching-result"></a>手动匹配结果

对于手动匹配，结果因匹配的顺序而异，如以下示例案例所示。

##### <a name="manual-matching-case-1"></a>手动匹配案例 1

进行本示例的手动匹配的一种方法如下：

1. 将 FB 与 Inv1 匹配。 FB 有 500 剩余金额，因此状态设置为 *部分匹配*。
1. 将 Inv2 与 FB 匹配。 Inv2 匹配了 500，FB 有 0 剩余，因此状态设置为 *完全匹配*。
1. 手动匹配 Inv3 时，您将找不到任何未匹配的运费帐单。

此案例与自动匹配基本相同

##### <a name="manual-matching-case-2"></a>手动匹配案例 2

进行本示例的手动匹配的另一种方法如下：

1. 将 Inv3 与 FB 匹配。 现在 FB 有 1600 剩余金额，这与在 1500 的基础上减去负 100 相同。 FB 和 Inv3 都有匹配数量 -100。
1. 依次将 Inv1 和 Inv 2 与 FB 匹配。 FB 完全匹配。

如此示例所示，仅带有负金额的运费发票应手动匹配。 这样可以确保始终可以将带有负金额的运费发票与未完全匹配的运费帐单进行匹配，因为这让您可以控制匹配顺序。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
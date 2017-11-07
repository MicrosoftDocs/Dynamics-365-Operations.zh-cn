---
title: "在运输管理中对运费进行对帐"
description: "本文介绍了运费对帐流程。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0e9dd669ff08c02a8bbb1f83e19dfa62298f317b
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="reconcile-freight-in-transportation-management"></a>在运输管理中对运费进行对帐

[!include[banner](../includes/banner.md)]


本文介绍了运费对帐流程。

可以手动完成运费对帐或可以设置为自动发生。 若要使用自动运费对帐，您必须设置审计主数据，在其中可以定义确定自动匹配哪些运费帐单的条件。

## <a name="the-freight-reconciliation-process"></a>运费对帐流程
运费费率由与相关装运承运人相关的费率引擎来计算。 确认负荷后，将生成运费帐单，运费费率被转移到该帐单。 运费费率作为其他费用分摊到相关的原始凭证（采购订单、销售订单和/或转移单），根据用于常规计费流程的设置。 从装运承运人收到运费发票后，就立即可以开始运费对帐流程（这也称为匹配流程）。 可以以电子方式或使用纸张接收发票。 如果使用纸张接收发票，可以通过将运费帐单作为模板使用来生成电子发票。 

[![运费对帐流程](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>手动对帐
如果要手动对帐运费，必须将每个发票行与已开票负荷的运费帐单行匹配。 您在**运费帐单和发票匹配**页进行此匹配。 如果发票行上的金额与运费帐单金额不匹配，则必须选择上差异对帐原因。 如果有多个对帐原因，您可以在它们之间拆分不匹配的金额。 对帐原因确定如何在总帐中过帐差异金额。 当对帐所计算的整个发票金额时，将金额提交供审批，然后过帐日记帐。 下图显示了如何在 Microsoft Dynamics 365 for Finance and Operations 中生成运费发票和执行运费对帐。 
[![Dynamics AX 中的运费对帐任务](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)
## <a name="automatic-reconciliation"></a>自动对帐
若要使用自动对帐，您必须指定对帐计划和发票，以及要使用的装运承运人。 发票行和运费帐单的匹配根据审计主数据和运费帐单类型的设置进行。 运行自动对帐后，必须处理所有系统不能匹配的发票。 然后，您必须手动处理这些发票，然后才能过帐所有付款发票。





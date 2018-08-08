---
title: "在运输管理中对运费进行对帐"
description: "本文介绍了运费对帐流程。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 1f92808f904ba93513e20b74bd2b597712cb93d4
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="6f007-103">在运输管理中对运费进行对帐</span><span class="sxs-lookup"><span data-stu-id="6f007-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f007-104">本文介绍了运费对帐流程。</span><span class="sxs-lookup"><span data-stu-id="6f007-104">This article describes the freight reconciliation process.</span></span>

<span data-ttu-id="6f007-105">可以手动完成运费对帐或可以设置为自动发生。</span><span class="sxs-lookup"><span data-stu-id="6f007-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="6f007-106">若要使用自动运费对帐，您必须设置审计主数据，在其中可以定义确定自动匹配哪些运费帐单的条件。</span><span class="sxs-lookup"><span data-stu-id="6f007-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="6f007-107">运费对帐流程</span><span class="sxs-lookup"><span data-stu-id="6f007-107">The freight reconciliation process</span></span>
<span data-ttu-id="6f007-108">运费费率由与相关装运承运人相关的费率引擎来计算。</span><span class="sxs-lookup"><span data-stu-id="6f007-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="6f007-109">确认负荷后，将生成运费帐单，运费费率被转移到该帐单。</span><span class="sxs-lookup"><span data-stu-id="6f007-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="6f007-110">运费费率作为其他费用分摊到相关的原始凭证（采购订单、销售订单和/或转移单），根据用于常规计费流程的设置。</span><span class="sxs-lookup"><span data-stu-id="6f007-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="6f007-111">从装运承运人收到运费发票后，就立即可以开始运费对帐流程（这也称为匹配流程）。</span><span class="sxs-lookup"><span data-stu-id="6f007-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="6f007-112">可以以电子方式或使用纸张接收发票。</span><span class="sxs-lookup"><span data-stu-id="6f007-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="6f007-113">如果使用纸张接收发票，可以通过将运费帐单作为模板使用来生成电子发票。</span><span class="sxs-lookup"><span data-stu-id="6f007-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span> 

<span data-ttu-id="6f007-114">[![运费对帐流程](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="6f007-114">[![Freight reconcilation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="6f007-115">手动对帐</span><span class="sxs-lookup"><span data-stu-id="6f007-115">Manual reconciliation</span></span>
<span data-ttu-id="6f007-116">如果要手动对帐运费，必须将每个发票行与已开票负荷的运费帐单行匹配。</span><span class="sxs-lookup"><span data-stu-id="6f007-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="6f007-117">您在**运费帐单和发票匹配**页进行此匹配。</span><span class="sxs-lookup"><span data-stu-id="6f007-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="6f007-118">如果发票行上的金额与运费帐单金额不匹配，则必须选择上差异对帐原因。</span><span class="sxs-lookup"><span data-stu-id="6f007-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="6f007-119">如果有多个对帐原因，您可以在它们之间拆分不匹配的金额。</span><span class="sxs-lookup"><span data-stu-id="6f007-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="6f007-120">对帐原因确定如何在总帐中过帐差异金额。</span><span class="sxs-lookup"><span data-stu-id="6f007-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="6f007-121">当对帐所计算的整个发票金额时，将金额提交供审批，然后过帐日记帐。</span><span class="sxs-lookup"><span data-stu-id="6f007-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="6f007-122">下图显示了如何在 Microsoft Dynamics 365 for Finance and Operations 中生成运费发票和执行运费对帐。</span><span class="sxs-lookup"><span data-stu-id="6f007-122">The following illustration shows how to generate a freight invoice and do freight reconciliation in Microsoft Dynamics 365 for Finance and Operations.</span></span> 
<span data-ttu-id="6f007-123">[![Dynamics AX 中的运费对帐任务](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="6f007-123">[![Freight reconcilation tasks in Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>
## <a name="automatic-reconciliation"></a><span data-ttu-id="6f007-124">自动对帐</span><span class="sxs-lookup"><span data-stu-id="6f007-124">Automatic reconciliation</span></span>
<span data-ttu-id="6f007-125">若要使用自动对帐，您必须指定对帐计划和发票，以及要使用的装运承运人。</span><span class="sxs-lookup"><span data-stu-id="6f007-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="6f007-126">发票行和运费帐单的匹配根据审计主数据和运费帐单类型的设置进行。</span><span class="sxs-lookup"><span data-stu-id="6f007-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="6f007-127">运行自动对帐后，必须处理所有系统不能匹配的发票。</span><span class="sxs-lookup"><span data-stu-id="6f007-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="6f007-128">然后，您必须手动处理这些发票，然后才能过帐所有付款发票。</span><span class="sxs-lookup"><span data-stu-id="6f007-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>





---
title: 为有直接借记授权单的客户创建付款
description: 此过程显示如何为有直接借记配置和有要付款发票的客户生成 ISO20022 直接借记付款文件。
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 129c5291a29994f91ef325aa9b9a3b54a0e958d6
ms.sourcegitcommit: 807dec193cd163c9f5d949e744cfde40f2eb24b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2019
ms.locfileid: "2468947"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a><span data-ttu-id="13470-103">为有直接借记授权单的客户创建付款</span><span class="sxs-lookup"><span data-stu-id="13470-103">Create payments for a customer who have direct debit mandates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="13470-104">此过程显示如何为有直接借记配置和有要付款发票的客户生成 ISO20022 直接借记付款文件。</span><span class="sxs-lookup"><span data-stu-id="13470-104">This procedure shows how to generate an ISO20022 direct debit payment file for a customer who has direct debit configured and an invoice to be paid.</span></span> <span data-ttu-id="13470-105">创建和过帐发票是可选操作。</span><span class="sxs-lookup"><span data-stu-id="13470-105">Creating and posting an invoice is optional.</span></span> <span data-ttu-id="13470-106">可以在生成付款文件之前在日记帐中选择授权单，而不是创建要付款的发票，为客户预付款方案提供支持。</span><span class="sxs-lookup"><span data-stu-id="13470-106">Instead of having an invoice to be paid you can select a mandate in a journal prior to generating a payment file, to support a customer prepayment scenario.</span></span>



<span data-ttu-id="13470-107">用于创建此过程的演示数据公司是 DEMF。</span><span class="sxs-lookup"><span data-stu-id="13470-107">The demo data company used to create this procedure is DEMF.</span></span>



<span data-ttu-id="13470-108">这是五个用于演示使用电子申报配置的客户付款流程的过程中的第五个。</span><span class="sxs-lookup"><span data-stu-id="13470-108">This is the fifth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span> <span data-ttu-id="13470-109">必须先完成前面的任务，才能完成此任务。</span><span class="sxs-lookup"><span data-stu-id="13470-109">Before you can complete this task, you must complete the earlier tasks.</span></span> <span data-ttu-id="13470-110">您首先必须导入客户付款电子申报配置，配置付款方式和设置您的公司和客户信息。</span><span class="sxs-lookup"><span data-stu-id="13470-110">You must first import customer payment electronic reporting configurations, configure method of payments, and set up your company and customer information.</span></span> 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a><span data-ttu-id="13470-111">过帐具有直接借记信息的普通发票</span><span class="sxs-lookup"><span data-stu-id="13470-111">Post a free text invoice with direct debit information</span></span>
1. <span data-ttu-id="13470-112">转到“应收账款”>“发票”>“所有普通发票”。</span><span class="sxs-lookup"><span data-stu-id="13470-112">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="13470-113">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="13470-113">Click New.</span></span>
3. <span data-ttu-id="13470-114">在“客户帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="13470-114">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="13470-115">例如，选择“DE-010”。</span><span class="sxs-lookup"><span data-stu-id="13470-115">For example, select DE-010.</span></span>  
4. <span data-ttu-id="13470-116">在“付款方式”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="13470-116">In the Method of payment field, enter or select a value.</span></span>
    * <span data-ttu-id="13470-117">例如，</span><span class="sxs-lookup"><span data-stu-id="13470-117">For example.</span></span> <span data-ttu-id="13470-118">选择“电子”。</span><span class="sxs-lookup"><span data-stu-id="13470-118">select Electronic.</span></span>  
5. <span data-ttu-id="13470-119">在“直接借记授权 ID”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="13470-119">In the Direct debit mandate ID field, enter or select a value.</span></span>
6. <span data-ttu-id="13470-120">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="13470-120">Click Add line.</span></span>
7. <span data-ttu-id="13470-121">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="13470-121">In the Description field, type a value.</span></span>
8. <span data-ttu-id="13470-122">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="13470-122">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="13470-123">在“单位价格”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="13470-123">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="13470-124">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="13470-124">Click Post.</span></span>
11. <span data-ttu-id="13470-125">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="13470-125">Click OK.</span></span>

## <a name="create-a-payment"></a><span data-ttu-id="13470-126">创建付款</span><span class="sxs-lookup"><span data-stu-id="13470-126">Create a payment</span></span>
1. <span data-ttu-id="13470-127">转到“应收账款”>“付款”>“付款日记帐”。</span><span class="sxs-lookup"><span data-stu-id="13470-127">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="13470-128">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="13470-128">Click New.</span></span>
3. <span data-ttu-id="13470-129">在“名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="13470-129">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="13470-130">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="13470-130">Click Lines.</span></span>
5. <span data-ttu-id="13470-131">单击“付款方案”。</span><span class="sxs-lookup"><span data-stu-id="13470-131">Click Payment proposal.</span></span>
6. <span data-ttu-id="13470-132">单击”创建付款方案“。</span><span class="sxs-lookup"><span data-stu-id="13470-132">Click Create payment proposal.</span></span>
7. <span data-ttu-id="13470-133">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="13470-133">Expand the Records to include section.</span></span>
8. <span data-ttu-id="13470-134">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="13470-134">Click Filter.</span></span>
9. <span data-ttu-id="13470-135">在列表中，选择“客户交易”表和“付款方式”字段的行。</span><span class="sxs-lookup"><span data-stu-id="13470-135">In the list, select the row for the Customer transactions table and the Method of payment field.</span></span>
    * <span data-ttu-id="13470-136">您可以为选择要支付的电子交易应用任何条件。</span><span class="sxs-lookup"><span data-stu-id="13470-136">You can apply any criteria for selecting customer transactions to pay.</span></span> <span data-ttu-id="13470-137">对于本示例，请使用“电子”充当支付方法筛选交易。</span><span class="sxs-lookup"><span data-stu-id="13470-137">For this example, use Electronic as a method of payment to filter transactions.</span></span>  
10. <span data-ttu-id="13470-138">在“标准”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="13470-138">In the Criteria field, enter or select a value.</span></span>
11. <span data-ttu-id="13470-139">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="13470-139">Click OK.</span></span>
12. <span data-ttu-id="13470-140">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="13470-140">Click OK.</span></span>
13. <span data-ttu-id="13470-141">单击”创建付款“。</span><span class="sxs-lookup"><span data-stu-id="13470-141">Click Create payments.</span></span>

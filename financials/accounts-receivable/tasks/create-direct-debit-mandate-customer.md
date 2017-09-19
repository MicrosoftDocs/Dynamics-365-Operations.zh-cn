--- 
title: "为客户创建直接借记授权单"
description: "此任务指南向您演示如何创建直接借记授权并将其使用在发票上。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d01c7c19925a3c7064ab3f845b92b610b162066c
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="cea21-103">为客户创建直接借记授权单</span><span class="sxs-lookup"><span data-stu-id="cea21-103">Create a direct debit mandate for a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cea21-104">此任务指南向您演示如何创建直接借记授权并将其使用在发票上。</span><span class="sxs-lookup"><span data-stu-id="cea21-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="cea21-105">创建银行帐户</span><span class="sxs-lookup"><span data-stu-id="cea21-105">Create a bank account</span></span>
1. <span data-ttu-id="cea21-106">转到“应付帐款”>“客户”>“所有客户”。</span><span class="sxs-lookup"><span data-stu-id="cea21-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="cea21-107">例如，选择 US-001。</span><span class="sxs-lookup"><span data-stu-id="cea21-107">For example, select US-001</span></span>
3. <span data-ttu-id="cea21-108">在“操作窗格”上，单击“客户”。</span><span class="sxs-lookup"><span data-stu-id="cea21-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="cea21-109">单击“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="cea21-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="cea21-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="cea21-110">Click New.</span></span>
6. <span data-ttu-id="cea21-111">在“银行帐户”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cea21-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="cea21-112">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cea21-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="cea21-113">在“IBAN”字段，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cea21-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="cea21-114">在“货币”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cea21-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="cea21-115">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="cea21-115">Click Save.</span></span>
11. <span data-ttu-id="cea21-116">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cea21-116">Close the page.</span></span>
12. <span data-ttu-id="cea21-117">转至“现金和银行管理”>“银行帐户”>“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="cea21-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="cea21-118">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="cea21-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="cea21-119">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="cea21-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="cea21-120">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="cea21-120">Click Edit.</span></span>
16. <span data-ttu-id="cea21-121">展开”其他识别“部分。</span><span class="sxs-lookup"><span data-stu-id="cea21-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="cea21-122">在“直接借记 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cea21-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="cea21-123">在“IBAN”字段，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cea21-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="cea21-124">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cea21-124">Close the page.</span></span>
20. <span data-ttu-id="cea21-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cea21-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="cea21-126">定义电子付款方式</span><span class="sxs-lookup"><span data-stu-id="cea21-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="cea21-127">转到“应收帐款”>“付款设置”>“付款方式”。</span><span class="sxs-lookup"><span data-stu-id="cea21-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="cea21-128">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="cea21-128">Click New.</span></span>
3. <span data-ttu-id="cea21-129">在“付款方式”字段中，输入值。</span><span class="sxs-lookup"><span data-stu-id="cea21-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="cea21-130">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cea21-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cea21-131">直接借记授权的付款方式的付款类型必须为“电子付款”。</span><span class="sxs-lookup"><span data-stu-id="cea21-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="cea21-132">在“需要授权”字段选择“是”。</span><span class="sxs-lookup"><span data-stu-id="cea21-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="cea21-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cea21-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="cea21-134">向客户添加一个直接借记授权。</span><span class="sxs-lookup"><span data-stu-id="cea21-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="cea21-135">转到“应付帐款”>“客户”>“所有客户”。</span><span class="sxs-lookup"><span data-stu-id="cea21-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="cea21-136">例如，选择 US-001。</span><span class="sxs-lookup"><span data-stu-id="cea21-136">For example, select US-001</span></span>
3. <span data-ttu-id="cea21-137">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="cea21-137">Click Edit.</span></span>
4. <span data-ttu-id="cea21-138">展开“默认付款”部分。</span><span class="sxs-lookup"><span data-stu-id="cea21-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="cea21-139">在“付款方式”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cea21-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="cea21-140">展开“默认付款”部分。</span><span class="sxs-lookup"><span data-stu-id="cea21-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="cea21-141">展开“直接借记授权”部分。</span><span class="sxs-lookup"><span data-stu-id="cea21-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="cea21-142">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="cea21-142">Click Add.</span></span>
9. <span data-ttu-id="cea21-143">在“银行帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cea21-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="cea21-144">在“贷方银行帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cea21-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="cea21-145">输入您预期为此授权付款处理的数字。</span><span class="sxs-lookup"><span data-stu-id="cea21-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="cea21-146">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cea21-146">Click OK.</span></span>
13. <span data-ttu-id="cea21-147">单击“打印”。</span><span class="sxs-lookup"><span data-stu-id="cea21-147">Click Print.</span></span>
14. <span data-ttu-id="cea21-148">点击“授权单报告”。</span><span class="sxs-lookup"><span data-stu-id="cea21-148">Click Mandate report.</span></span>
15. <span data-ttu-id="cea21-149">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cea21-149">Close the page.</span></span>
16. <span data-ttu-id="cea21-150">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="cea21-150">Click Edit.</span></span>
17. <span data-ttu-id="cea21-151">在“签署日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="cea21-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="cea21-152">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="cea21-152">Click Yes.</span></span>
19. <span data-ttu-id="cea21-153">输入授权单的签署位置。</span><span class="sxs-lookup"><span data-stu-id="cea21-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="cea21-154">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cea21-154">Click OK.</span></span>
21. <span data-ttu-id="cea21-155">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cea21-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="cea21-156">创建一个包含授权的普通发票</span><span class="sxs-lookup"><span data-stu-id="cea21-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="cea21-157">转到“应收帐款”>“发票”>“所有普通发票”。</span><span class="sxs-lookup"><span data-stu-id="cea21-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="cea21-158">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="cea21-158">Click New.</span></span>
3. <span data-ttu-id="cea21-159">选择您已添加了授权的客户。</span><span class="sxs-lookup"><span data-stu-id="cea21-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="cea21-160">在“直接借记授权 ID”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cea21-160">In the Direct debit mandate ID field, enter or select a value.</span></span>


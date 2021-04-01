---
title: 为客户创建直接借记授权单
description: 此任务指南向您演示如何创建直接借记授权并将其使用在发票上。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ef9beae6769c361680832d81ddda00e1237d3297
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241626"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="fcd4d-103">为客户创建直接借记授权单</span><span class="sxs-lookup"><span data-stu-id="fcd4d-103">Create a direct debit mandate for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fcd4d-104">此任务指南向您演示如何创建直接借记授权并将其使用在发票上。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="fcd4d-105">创建银行帐户</span><span class="sxs-lookup"><span data-stu-id="fcd4d-105">Create a bank account</span></span>
1. <span data-ttu-id="fcd4d-106">在 **导航窗格** 中，转到 **模块 > 应收帐款 > 客户 > 所有客户**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="fcd4d-107">在列表中，选择一个记录。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-107">In the list, select a record.</span></span> <span data-ttu-id="fcd4d-108">例如，选择 US-001。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-108">For example, select US-001</span></span>
3. <span data-ttu-id="fcd4d-109">在操作窗格上，单击 **客户**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-109">On the Action Pane, click **Customer**.</span></span>
4. <span data-ttu-id="fcd4d-110">单击 **银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-110">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="fcd4d-111">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-111">Click **New**.</span></span>
6. <span data-ttu-id="fcd4d-112">在 **银行帐户** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-112">In the **Bank account** field, type a value.</span></span>
7. <span data-ttu-id="fcd4d-113">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="fcd4d-114">在 **IBAN** 字段，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-114">In the **IBAN** field, type a value.</span></span>
9. <span data-ttu-id="fcd4d-115">在 **货币** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-115">In the **Currency** field, type a value.</span></span>
10. <span data-ttu-id="fcd4d-116">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-116">Click **Save**.</span></span>
11. <span data-ttu-id="fcd4d-117">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-117">Close the page.</span></span>
12. <span data-ttu-id="fcd4d-118">在 **导航窗格** 中，转到 **模块 > 现金和银行管理 > 银行帐户 > 银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-118">In the **Navigation pane**, go to **Modules > Cash and bank management > Bank accounts > Bank accounts**.</span></span>
13. <span data-ttu-id="fcd4d-119">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-119">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="fcd4d-120">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-120">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="fcd4d-121">单击 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-121">Click **Edit**.</span></span>
16. <span data-ttu-id="fcd4d-122">展开 **其他识别** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-122">Expand the **Additional identification** fastTab.</span></span>
17. <span data-ttu-id="fcd4d-123">在 **直接借记 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-123">In the **Direct debit ID** field, type a value.</span></span>
18. <span data-ttu-id="fcd4d-124">在 **IBAN** 字段，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-124">In the **IBAN** field, type a value.</span></span>
19. <span data-ttu-id="fcd4d-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-125">Close the page.</span></span>
20. <span data-ttu-id="fcd4d-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-126">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="fcd4d-127">定义电子付款方式</span><span class="sxs-lookup"><span data-stu-id="fcd4d-127">Define the electronic payment method</span></span>
1. <span data-ttu-id="fcd4d-128">在 **导航窗格** 中，转到 **模块 > 应收帐款 > 付款设置 > 付款方式**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-128">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="fcd4d-129">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-129">Click **New**.</span></span>
3. <span data-ttu-id="fcd4d-130">在 **付款方式** 字段中，输入值。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-130">In the **Method of payment** field, type a value.</span></span>
4. <span data-ttu-id="fcd4d-131">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="fcd4d-132">在 **付款类型** 字段中，输入“电子付款”。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-132">In the **Payment type** field, enter 'Electronic payment'.</span></span> <span data-ttu-id="fcd4d-133">直接借记授权的付款方式的付款类型必须为“电子付款”。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-133">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="fcd4d-134">在 **需要授权** 字段选择“是”。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-134">Select Yes in the **Require mandate** field.</span></span>
7. <span data-ttu-id="fcd4d-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-135">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="fcd4d-136">向客户添加一个直接借记授权。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-136">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="fcd4d-137">在 **导航窗格** 中，转到 **模块 > 应收帐款 > 客户 > 所有客户**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-137">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="fcd4d-138">在列表中，选择一个记录。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-138">In the list, select a record.</span></span> <span data-ttu-id="fcd4d-139">例如，选择 US-001。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-139">For example, select US-001</span></span>
3. <span data-ttu-id="fcd4d-140">单击 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-140">Click **Edit**.</span></span>
4. <span data-ttu-id="fcd4d-141">展开 **默认付款** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-141">Expand the **Payment defaults** fastTab.</span></span>
5. <span data-ttu-id="fcd4d-142">在 **付款方式** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-142">In the **Method of payment** field, enter or select a value.</span></span>
6. <span data-ttu-id="fcd4d-143">展开 **默认付款** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-143">Expand the **Payment defaults** fastTab.</span></span>
7. <span data-ttu-id="fcd4d-144">展开 **直接借记授权** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-144">Expand the **Direct debit mandates** fastTab.</span></span>
8. <span data-ttu-id="fcd4d-145">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-145">Click **Add**.</span></span>
9. <span data-ttu-id="fcd4d-146">在 **银行帐户** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-146">In the **Bank account** field, enter or select a value.</span></span>
10. <span data-ttu-id="fcd4d-147">在 **贷方银行帐户** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-147">In the **Creditor bank account** field, enter or select a value.</span></span>
11. <span data-ttu-id="fcd4d-148">在 **付款频率** 字段中，输入您预期为此授权付款处理的数字。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-148">In the **Payment frequency** field, enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="fcd4d-149">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-149">Click **OK**.</span></span>
13. <span data-ttu-id="fcd4d-150">单击 **打印**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-150">Click **Print**.</span></span>
14. <span data-ttu-id="fcd4d-151">点击 **授权单报告**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-151">Click **Mandate report**.</span></span>
15. <span data-ttu-id="fcd4d-152">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-152">Close the page.</span></span>
16. <span data-ttu-id="fcd4d-153">单击 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-153">Click **Edit**.</span></span>
17. <span data-ttu-id="fcd4d-154">在 **签署日期** 字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-154">In the **Signature date** field, enter a date.</span></span>
18. <span data-ttu-id="fcd4d-155">单击 **是**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-155">Click **Yes**.</span></span>
19. <span data-ttu-id="fcd4d-156">输入授权单的签署位置。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-156">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="fcd4d-157">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-157">Click **OK**.</span></span>
21. <span data-ttu-id="fcd4d-158">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-158">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="fcd4d-159">创建一个包含授权的普通发票</span><span class="sxs-lookup"><span data-stu-id="fcd4d-159">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="fcd4d-160">在 **导航窗格** 中，转到 **模块 > 应收帐款 > 发票 > 所有普通发票**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-160">In the **Navigation pane**, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="fcd4d-161">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-161">Click **New**.</span></span>
3. <span data-ttu-id="fcd4d-162">选择您已添加了授权的客户。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-162">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="fcd4d-163">在 **直接借记授权 ID** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fcd4d-163">In the **Direct debit mandate ID** field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
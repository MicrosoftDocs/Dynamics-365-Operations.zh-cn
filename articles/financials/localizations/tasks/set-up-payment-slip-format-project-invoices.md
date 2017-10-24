--- 
title: "设置项目发票的付款单格式"
description: "企业通常将打印的付款单附加到发票上以帮助客户，并提供用于过帐和结算的付款参考。"
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 02/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 9700571110a1b488e250dd8ee7b8c5c8f15cbc01
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-payment-slip-format-for-project-invoices"></a><span data-ttu-id="ea014-103">设置项目发票的付款单格式</span><span class="sxs-lookup"><span data-stu-id="ea014-103">Set up payment slip format for project invoices</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ea014-104">企业通常将打印的付款单附加到发票上以帮助客户，并提供用于过帐和结算的付款参考。</span><span class="sxs-lookup"><span data-stu-id="ea014-104">Businesses commonly attach printed payment slips to invoices to assist customers and provide a payment reference for posting and settlement.</span></span> <span data-ttu-id="ea014-105">除了销售发票和普通发票，付款单可用于项目或服务发票，催款单、利息单和帐户对账单。</span><span class="sxs-lookup"><span data-stu-id="ea014-105">The payment slip can be used for project or service invoices, collection letters, interest notes, and account statements, in addition to sales invoices and free text invoices.</span></span> <span data-ttu-id="ea014-106">若要处理付款单，首先设置您的债权人标识号和付款单附件格式。</span><span class="sxs-lookup"><span data-stu-id="ea014-106">To process payment slips, first set up your creditor identification number and payment slip attachment formats.</span></span>

<span data-ttu-id="ea014-107">该程序适用于 DEMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="ea014-107">This procedure uses the DEMF demo company.</span></span> 

<span data-ttu-id="ea014-108">该功能可用于首选地址在丹麦的法人。</span><span class="sxs-lookup"><span data-stu-id="ea014-108">This functionality is available for legal entities whose primary address is in Denmark.</span></span>


## <a name="set-up-a-creditor-id-number"></a><span data-ttu-id="ea014-109">设置债权人 ID 号</span><span class="sxs-lookup"><span data-stu-id="ea014-109">Set up a creditor ID number</span></span>
1. <span data-ttu-id="ea014-110">转至“组织管理”>“组织”>“法人”。</span><span class="sxs-lookup"><span data-stu-id="ea014-110">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="ea014-111">展开或折叠“银行帐户信息”部分。</span><span class="sxs-lookup"><span data-stu-id="ea014-111">Expand or collapse the Bank account information section.</span></span>
3. <span data-ttu-id="ea014-112">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="ea014-112">Click Edit.</span></span>
4. <span data-ttu-id="ea014-113">在“FI 债权人 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ea014-113">In the FI-Creditor ID field, type a value.</span></span>
5. <span data-ttu-id="ea014-114">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea014-114">Click Save.</span></span>
6. <span data-ttu-id="ea014-115">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ea014-115">Close the page.</span></span>

## <a name="set-up-a-payment-slip-format-for-invoices-notes-letters-and-statements"></a><span data-ttu-id="ea014-116">为发票、本票、字母和报表设置付款单格式</span><span class="sxs-lookup"><span data-stu-id="ea014-116">Set up a payment slip format for invoices, notes, letters, and statements</span></span>
1. <span data-ttu-id="ea014-117">转到应收帐项目>设置>表格>表格设置。</span><span class="sxs-lookup"><span data-stu-id="ea014-117">Go to Accounts receivable > Setup > Forms > Form setup.</span></span>
2. <span data-ttu-id="ea014-118">单击“发票”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ea014-118">Click the Invoice tab.</span></span>
3. <span data-ttu-id="ea014-119">在客户发票字段中“关联付款附件”，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="ea014-119">In the Associated payment attachment on customer invoice field, select an option.</span></span>
    * <span data-ttu-id="ea014-120">None： 不打印付账单。</span><span class="sxs-lookup"><span data-stu-id="ea014-120">None – Do not print a payment slip.</span></span> <span data-ttu-id="ea014-121">如果付款金额是以除了丹麦克朗 (DKK) 的币种表示，则选择此选项。</span><span class="sxs-lookup"><span data-stu-id="ea014-121">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="ea014-122">FIK 751： 如果打算在付账单上手写付款金额和付款日期，就打印FIK 751 付账单。</span><span class="sxs-lookup"><span data-stu-id="ea014-122">FIK 751 – Print an FIK 751 payment slip if you intend to manually write the payment amount and due date on the payment slip.</span></span>   <span data-ttu-id="ea014-123">FIK 752： 如果打算用电脑生成的带有打印好的付款金额及日期的付款帐单，就打印FIK 752 付账单。</span><span class="sxs-lookup"><span data-stu-id="ea014-123">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
4. <span data-ttu-id="ea014-124">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea014-124">Click Save.</span></span>
5. <span data-ttu-id="ea014-125">单击“普通文本发票”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ea014-125">Click the Free text invoice tab.</span></span>
6. <span data-ttu-id="ea014-126">在“普通文本发票的相关付款附件”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="ea014-126">In the Associated payment attachment on free text invoice field, select an option.</span></span>
    * <span data-ttu-id="ea014-127">None： 不打印付账单。</span><span class="sxs-lookup"><span data-stu-id="ea014-127">None – Do not print a payment slip.</span></span> <span data-ttu-id="ea014-128">如果付款金额是以除了丹麦克朗 (DKK) 的币种表示，则选择此选项。</span><span class="sxs-lookup"><span data-stu-id="ea014-128">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="ea014-129">FIK 751： 如果打算在付账单上手写付款金额和付款日期，就打印FIK 751 付账单。</span><span class="sxs-lookup"><span data-stu-id="ea014-129">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="ea014-130">FIK 752： 如果打算用电脑生成的带有打印好的付款金额及日期的付款帐单，就打印FIK 752 付账单。</span><span class="sxs-lookup"><span data-stu-id="ea014-130">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
7. <span data-ttu-id="ea014-131">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea014-131">Click Save.</span></span>
8. <span data-ttu-id="ea014-132">单击“利息单”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ea014-132">Click the Interest note tab.</span></span>
9. <span data-ttu-id="ea014-133">在利息单字段中“关联付款附件”，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="ea014-133">In the Associated payment attachment on interest note field, select an option.</span></span>
    * <span data-ttu-id="ea014-134">None： 不打印付账单。</span><span class="sxs-lookup"><span data-stu-id="ea014-134">None – Do not print a payment slip.</span></span> <span data-ttu-id="ea014-135">如果付款金额是以除了丹麦克朗 (DKK) 的币种表示，则选择此选项。</span><span class="sxs-lookup"><span data-stu-id="ea014-135">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="ea014-136">FIK 751： 如果打算在付账单上手写付款金额和付款日期，就打印FIK 751 付账单。</span><span class="sxs-lookup"><span data-stu-id="ea014-136">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="ea014-137">FIK 752： 如果打算用电脑生成的带有打印好的付款金额及日期的付款帐单，就打印FIK 752 付账单。</span><span class="sxs-lookup"><span data-stu-id="ea014-137">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
10. <span data-ttu-id="ea014-138">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea014-138">Click Save.</span></span>
11. <span data-ttu-id="ea014-139">单击“收款单”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ea014-139">Click the Collection letter tab.</span></span>
12. <span data-ttu-id="ea014-140">在收款单字段中“关联付款附件”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="ea014-140">In the Associated payment attachment on collection letter field, select an option.</span></span>
    * <span data-ttu-id="ea014-141">None： 不打印付账单。</span><span class="sxs-lookup"><span data-stu-id="ea014-141">None – Do not print a payment slip.</span></span> <span data-ttu-id="ea014-142">如果付款金额是以除了丹麦克朗 (DKK) 的币种表示，则选择此选项。</span><span class="sxs-lookup"><span data-stu-id="ea014-142">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="ea014-143">FIK 751： 如果打算在付账单上手写付款金额和付款日期，就打印FIK 751 付账单。</span><span class="sxs-lookup"><span data-stu-id="ea014-143">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="ea014-144">FIK 752： 如果打算用电脑生成的带有打印好的付款金额及日期的付款帐单，就打印FIK 752 付账单。</span><span class="sxs-lookup"><span data-stu-id="ea014-144">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
13. <span data-ttu-id="ea014-145">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea014-145">Click Save.</span></span>
14. <span data-ttu-id="ea014-146">单击“会计财务报表”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ea014-146">Click the Account statement tab.</span></span>
15. <span data-ttu-id="ea014-147">在会计财务报表字段中“关联付款附件”，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="ea014-147">In the Associated payment attachment on account statement field, select an option.</span></span>
    * <span data-ttu-id="ea014-148">None： 不打印付账单。</span><span class="sxs-lookup"><span data-stu-id="ea014-148">None – Do not print a payment slip.</span></span> <span data-ttu-id="ea014-149">如果付款金额是以除了丹麦克朗 (DKK) 的币种表示，则选择此选项。</span><span class="sxs-lookup"><span data-stu-id="ea014-149">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="ea014-150">FIK 751： 如果打算在付账单上手写付款金额和付款日期，就打印FIK 751 付账单。</span><span class="sxs-lookup"><span data-stu-id="ea014-150">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="ea014-151">FIK 752： 如果打算用电脑生成的带有打印好的付款金额及日期的付款帐单，就打印FIK 752 付账单。</span><span class="sxs-lookup"><span data-stu-id="ea014-151">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
16. <span data-ttu-id="ea014-152">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea014-152">Click Save.</span></span>
17. <span data-ttu-id="ea014-153">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ea014-153">Close the page.</span></span>


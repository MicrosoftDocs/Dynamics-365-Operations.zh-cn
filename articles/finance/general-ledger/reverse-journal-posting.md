---
title: 冲销日记帐过帐
description: 此主题介绍用于冲销凭证交易记录列表中或财务日记帐中的凭证的功能。
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d18b71c1fc7f3f0c39172bd9edf19b4e60a2bf8
ms.sourcegitcommit: cfaad79bcb1460ee0e7ad5a2c596f9199e14c53a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/08/2020
ms.locfileid: "2944420"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="5cfb9-103">冲销日记帐过帐</span><span class="sxs-lookup"><span data-stu-id="5cfb9-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5cfb9-104">此主题介绍用于冲销整个日记帐或冲销凭证交易记录列表中的一个或多个凭证（而不考虑其来源）的 Microsoft Dynamics 365 Finance 功能。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="5cfb9-105">冲销日记帐</span><span class="sxs-lookup"><span data-stu-id="5cfb9-105">Reversing journals</span></span>

<span data-ttu-id="5cfb9-106">可分别冲销日记帐行。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="5cfb9-107">通过冲销日记帐过帐，也可以冲销整个财务日记帐。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="5cfb9-108">若要冲销日记帐：</span><span class="sxs-lookup"><span data-stu-id="5cfb9-108">To reverse a journal:</span></span> 

- <span data-ttu-id="5cfb9-109">打开财务日记帐并筛选过帐的日记帐。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="5cfb9-110">选择页面顶部的**冲销**菜单。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="5cfb9-111">将看到凭证总数和凭证行，以及正在冲销的行的总量</span><span class="sxs-lookup"><span data-stu-id="5cfb9-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="5cfb9-112">如果选择**是**，则使用现有交易记录日期，如果选择**否**，则输入新交易记录日期。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="5cfb9-113">在某些情况下，原始交易记录的期间可能已关闭，您必须为冲销输入新的交易记录日期。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="5cfb9-114">如果选择**否**，请为冲销输入交易记录日期。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="5cfb9-115">输入要添加到冲销交易记录的注释。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="5cfb9-116">选择**冲销**按钮。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="5cfb9-117">将冲销交易记录。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="5cfb9-118">如果凭证包含超过 100 行，则将使用批处理流程运行冲销流程。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="5cfb9-119">可通过查看批处理作业中的注释查看结果。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="5cfb9-120">无法冲销的所有交易记录都将在批处理作业历史记录中列出。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="5cfb9-121">如果凭证包含 100 行或更少，将立即运行冲销流程。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="5cfb9-122">将在对话框中提供结果，其中显示不能冲销的所有凭证，以及不能冲销的原因。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="5cfb9-123">选择**确定**关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="5cfb9-124">冲销凭证交易记录列表中的凭证。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="5cfb9-125">也可以重新所有子分类帐的**凭证交易记录列表**中的凭证。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="5cfb9-126">此外，还可以同时冲销多个凭证。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="5cfb9-127">若要冲销一个或多个凭证：</span><span class="sxs-lookup"><span data-stu-id="5cfb9-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="5cfb9-128">选择页面顶部的**冲销**菜单</span><span class="sxs-lookup"><span data-stu-id="5cfb9-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="5cfb9-129">将看到凭证总数和凭证行，以及正在冲销的行的总量。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="5cfb9-130">如果选择**是**，则使用现有交易记录日期，如果选择**否**，则输入新交易记录日期。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="5cfb9-131">在某些情况下，原始交易记录的期间可能已关闭，您必须输入新的交易记录日期来冲销它。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="5cfb9-132">如果选择**否**，请为冲销输入交易记录日期。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="5cfb9-133">输入描述冲销交易的注释。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="5cfb9-134">选择**冲销**按钮。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="5cfb9-135">将冲销交易记录。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="5cfb9-136">如果有超过 100 个凭证行，则将使用批处理流程运行冲销流程。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="5cfb9-137">可通过查看批处理作业中的注释查看结果。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="5cfb9-138">无法冲销的所有交易记录都将在批处理作业历史记录中记录。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="5cfb9-139">如果凭证行数量为 100 行或更少，将立即运行冲销流程。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="5cfb9-140">将在对话框中显示结果，其中显示不能冲销的所有凭证，以及原因。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="5cfb9-141">选择**确定**关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="5cfb9-142">仅当交易记录符合进行冲销的业务规则时，才可以冲销交易记录。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="5cfb9-143">使用本主题中介绍的功能无法撤销供应商付款。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="5cfb9-144">必须按照[冲销供应商付款](https://docs.microsoft.com/en-us/dynamics365/finance/accounts-payable/reverse-vendor-payment)中列出的步骤来冲销供应商付款。</span><span class="sxs-lookup"><span data-stu-id="5cfb9-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](https://docs.microsoft.com/en-us/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span></span>


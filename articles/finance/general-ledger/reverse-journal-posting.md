---
title: 冲销日记帐过帐
description: 此主题介绍用于冲销凭证交易记录列表中或财务日记帐中的凭证的功能。
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
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
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248577"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="bd5a7-103">冲销日记帐过帐</span><span class="sxs-lookup"><span data-stu-id="bd5a7-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd5a7-104">此主题介绍用于冲销整个日记帐或冲销凭证交易记录列表中的一个或多个凭证（而不考虑其来源）的 Microsoft Dynamics 365 Finance 功能。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal or reverse one or more vouchers from the voucher transaction list regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="bd5a7-105">冲销日记帐</span><span class="sxs-lookup"><span data-stu-id="bd5a7-105">Reversing journals</span></span>

<span data-ttu-id="bd5a7-106">可分别冲销日记帐行。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="bd5a7-107">通过冲销日记帐过帐，也可以冲销整个财务日记帐。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="bd5a7-108">若要冲销日记帐：</span><span class="sxs-lookup"><span data-stu-id="bd5a7-108">To reverse a journal:</span></span> 
- <span data-ttu-id="bd5a7-109">打开财务日记帐并筛选过帐的日记帐</span><span class="sxs-lookup"><span data-stu-id="bd5a7-109">Open the financial journal and filter on posted journals</span></span>
- <span data-ttu-id="bd5a7-110">单击页面顶部的“冲销”菜单</span><span class="sxs-lookup"><span data-stu-id="bd5a7-110">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="bd5a7-111">将看到凭证总数和凭证行，以及正在冲销的行的总量</span><span class="sxs-lookup"><span data-stu-id="bd5a7-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="bd5a7-112">如果选择“是”，则使用现有交易记录日期，如果选择“否”，则输入新交易记录日期。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-112">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="bd5a7-113">在某些情况下，原始交易记录的期间可能已关闭，您希望为冲销输入新的交易记录日期。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-113">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="bd5a7-114">如果选择“否”，请为冲销输入交易记录日期。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-114">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="bd5a7-115">输入要添加到冲销交易记录的注释</span><span class="sxs-lookup"><span data-stu-id="bd5a7-115">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="bd5a7-116">单击“冲销”按钮</span><span class="sxs-lookup"><span data-stu-id="bd5a7-116">Click the Reverse button</span></span>

<span data-ttu-id="bd5a7-117">将冲销交易记录。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="bd5a7-118">如果凭证行数量超过 100 行，则将使用批处理流程运行冲销流程。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-118">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="bd5a7-119">可通过查看运行的批处理作业中的注释，查看冲销结果。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-119">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="bd5a7-120">将把所有失败记录到批处理作业历史记录中。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-120">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="bd5a7-121">如果凭证行数量为 100 行或更少，将立即运行冲销流程。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-121">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="bd5a7-122">将在对话框中提供结果，其中显示不能冲销的所有凭证和不能冲销的原因。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-122">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="bd5a7-123">单击“确定”关闭该对话框。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-123">Click on Ok to close the dialog.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="bd5a7-124">冲销凭证交易记录列表中的凭证。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="bd5a7-125">也可以重新所有子分类帐的**凭证交易记录列表**中的凭证。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="bd5a7-126">此外，还可以同时冲销多个凭证。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="bd5a7-127">若要冲销一个或多个凭证：</span><span class="sxs-lookup"><span data-stu-id="bd5a7-127">To reverse one or more vouchers:</span></span> 
- <span data-ttu-id="bd5a7-128">单击页面顶部的“冲销”菜单</span><span class="sxs-lookup"><span data-stu-id="bd5a7-128">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="bd5a7-129">将看到凭证总数和凭证行，以及正在冲销的行的总量</span><span class="sxs-lookup"><span data-stu-id="bd5a7-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="bd5a7-130">如果选择“是”，则使用现有交易记录日期，如果选择“否”，则输入新交易记录日期。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-130">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="bd5a7-131">在某些情况下，原始交易记录的期间可能已关闭，您希望为冲销输入新的交易记录日期。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-131">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="bd5a7-132">如果选择“否”，请为冲销输入交易记录日期。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-132">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="bd5a7-133">输入要添加到冲销交易记录的注释</span><span class="sxs-lookup"><span data-stu-id="bd5a7-133">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="bd5a7-134">单击“冲销”按钮</span><span class="sxs-lookup"><span data-stu-id="bd5a7-134">Click the Reverse button</span></span>

<span data-ttu-id="bd5a7-135">将冲销交易记录。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="bd5a7-136">如果凭证行数量超过 100 行，则将使用批处理流程运行冲销流程。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-136">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="bd5a7-137">可通过查看运行的批处理作业中的注释，查看冲销结果。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-137">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="bd5a7-138">将把所有失败记录到批处理作业历史记录中。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-138">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="bd5a7-139">如果凭证行数量为 100 行或更少，将立即运行冲销流程。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-139">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="bd5a7-140">将在对话框中提供结果，其中显示不能冲销的所有凭证和不能冲销的原因。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-140">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="bd5a7-141">单击“确定”关闭该对话框。</span><span class="sxs-lookup"><span data-stu-id="bd5a7-141">Click on Ok to close the dialog.</span></span>


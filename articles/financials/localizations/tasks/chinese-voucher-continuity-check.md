--- 
title: "中国式凭证连续性检查"
description: "每个凭证类型的中国式凭证号必须从 1 开始并且具有连续性，才能结转会计期间。"
author: ShylaThompson
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: China (PRC)
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8197773d2994964b4534b9220de0557d4cef3bef
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="chinese-voucher-continuity-check"></a><span data-ttu-id="0b747-103">中国式凭证连续性检查</span><span class="sxs-lookup"><span data-stu-id="0b747-103">Chinese voucher continuity check</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0b747-104">每个凭证类型的中国式凭证号必须从 1 开始并且具有连续性，才能结转会计期间。</span><span class="sxs-lookup"><span data-stu-id="0b747-104">Before you can close a fiscal period, the Chinese voucher numbers for each voucher type must start at 1 and be sequential.</span></span>
<span data-ttu-id="0b747-105">此过程显示如何检查会计期间中的所有已过帐凭证，以及如何将中国式凭证号连续编号。</span><span class="sxs-lookup"><span data-stu-id="0b747-105">This procedure shows how to check all posted vouchers in a fiscal period and renumber the Chinese voucher numbers to to be sequential.</span></span> <span data-ttu-id="0b747-106">此过程是会计期间结转流程的一部分，因此只能为“暂停”会计期间运行。</span><span class="sxs-lookup"><span data-stu-id="0b747-106">This process is part of the fiscal period closing process, so it can only be run for On hold fiscal periods.</span></span> <span data-ttu-id="0b747-107">第一个子任务逐步演示如何停止会计期间。</span><span class="sxs-lookup"><span data-stu-id="0b747-107">The first sub task walks you through stopping a fiscal period.</span></span> 

<span data-ttu-id="0b747-108">本流程是用演示公司 CNMF 数据生成的。</span><span class="sxs-lookup"><span data-stu-id="0b747-108">This procedure was created using the demo data company CNMF.</span></span> <span data-ttu-id="0b747-109">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="0b747-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="stop-a-fiscal-period"></a><span data-ttu-id="0b747-110">停止某一会计期间</span><span class="sxs-lookup"><span data-stu-id="0b747-110">Stop a fiscal period</span></span>
1. <span data-ttu-id="0b747-111">转到“总帐”>“日历”>“分类帐日历”。</span><span class="sxs-lookup"><span data-stu-id="0b747-111">Go to General ledger > Calendars > Ledger calendars.</span></span>
2. <span data-ttu-id="0b747-112">在“会计年度”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0b747-112">In the Fiscal year field, enter or select a value.</span></span>
3. <span data-ttu-id="0b747-113">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="0b747-113">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="0b747-114">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0b747-114">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="0b747-115">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="0b747-115">Click Edit.</span></span>
6. <span data-ttu-id="0b747-116">单击“停止期间”。</span><span class="sxs-lookup"><span data-stu-id="0b747-116">Click Stop period.</span></span>
7. <span data-ttu-id="0b747-117">单击“验证”。</span><span class="sxs-lookup"><span data-stu-id="0b747-117">Click Validate.</span></span>
8. <span data-ttu-id="0b747-118">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0b747-118">Click OK.</span></span>
9. <span data-ttu-id="0b747-119">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0b747-119">Click OK.</span></span>

## <a name="check-whether-posted-vouchers-have-continuity-voucher-numbers"></a><span data-ttu-id="0b747-120">检查已过帐凭证是否有连续性凭证号</span><span class="sxs-lookup"><span data-stu-id="0b747-120">Check whether posted vouchers have continuity voucher numbers</span></span>
1. <span data-ttu-id="0b747-121">转到“总帐”>“查询和报表”>“凭证事务”。</span><span class="sxs-lookup"><span data-stu-id="0b747-121">Go to General ledger > Inquiries and reports > Voucher transactions.</span></span>
2. <span data-ttu-id="0b747-122">在“标准”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0b747-122">In the Criteria field, enter or select a value.</span></span>
3. <span data-ttu-id="0b747-123">在“标准”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0b747-123">In the Criteria field, enter or select a value.</span></span>
4. <span data-ttu-id="0b747-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0b747-124">Click OK.</span></span>

## <a name="run-the-chinese-voucher-continuity-check-process"></a><span data-ttu-id="0b747-125">运行中国式凭证连续性检查流程</span><span class="sxs-lookup"><span data-stu-id="0b747-125">Run the Chinese voucher continuity check process</span></span>
1. <span data-ttu-id="0b747-126">转到“总帐”>“定期任务”>“中国式凭证连续性检查”。</span><span class="sxs-lookup"><span data-stu-id="0b747-126">Go to General ledger > Periodic tasks > Chinese voucher continuity check.</span></span>
2. <span data-ttu-id="0b747-127">在“打印重新编号结果”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="0b747-127">Select Yes in the Print out the result of renumbering field.</span></span>
3. <span data-ttu-id="0b747-128">在“期间开始”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="0b747-128">In the Period start field, enter a date.</span></span>
4. <span data-ttu-id="0b747-129">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0b747-129">Click OK.</span></span>
5. <span data-ttu-id="0b747-130">转到“总帐”>“查询和报表”>“凭证连续性检查日志”。</span><span class="sxs-lookup"><span data-stu-id="0b747-130">Go to General ledger > Inquiries and reports > Voucher continuity check log.</span></span>



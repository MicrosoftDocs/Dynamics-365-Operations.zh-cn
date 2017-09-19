--- 
title: "处理分类帐分配日记帐"
description: "使用“处理分配请求”页面以创建可在过帐至总帐前检查和审核，或直接过帐至总帐的分配日记帐。"
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7d299657758b1e1322aef07bfe8c71f7bf00b0ca
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="291c8-103">处理分类帐分配日记帐</span><span class="sxs-lookup"><span data-stu-id="291c8-103">Process ledger allocation journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="291c8-104">使用“处理分配请求”页面以创建可在过帐至总帐前检查和审核，或直接过帐至总帐的分配日记帐。</span><span class="sxs-lookup"><span data-stu-id="291c8-104">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="291c8-105">必须至少有一个有效的分类帐分配规则才能创建分配日记帐。</span><span class="sxs-lookup"><span data-stu-id="291c8-105">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="291c8-106">此任务使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="291c8-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="291c8-107">转到总分类记账>分配>处理分配请求。</span><span class="sxs-lookup"><span data-stu-id="291c8-107">Go to General ledger > Allocations > Process allocation request.</span></span>
2. <span data-ttu-id="291c8-108">在“规则”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="291c8-108">In the Rule field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="291c8-109">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="291c8-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="291c8-110">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="291c8-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="291c8-111">在“截止日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="291c8-111">In the As of date field, enter a date.</span></span>
    * <span data-ttu-id="291c8-112">“截止日期”非常重要，因为根据规则分类账是数据源头。</span><span class="sxs-lookup"><span data-stu-id="291c8-112">The As of Date is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="291c8-113">这个日期决定分配被包括哪个分类账平衡表。</span><span class="sxs-lookup"><span data-stu-id="291c8-113">This date controls which ledger balances to include for allocation.</span></span>     <span data-ttu-id="291c8-114">在“零资源“字段， 选“停止”。</span><span class="sxs-lookup"><span data-stu-id="291c8-114">In the Zero source field select Stop.</span></span> <span data-ttu-id="291c8-115">这将停止分配过程，然后显示一条信息说”选择了零资源数“。</span><span class="sxs-lookup"><span data-stu-id="291c8-115">This will  Stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  
6. <span data-ttu-id="291c8-116">在“方案选项”字段中，选择“仅方案”。</span><span class="sxs-lookup"><span data-stu-id="291c8-116">In the Proposal options field, select 'Proposal only'.</span></span>
    * <span data-ttu-id="291c8-117">选择“仅方案”会在将分配过帐至总帐前，检查并选择性审核“分配”日记帐中的结果。</span><span class="sxs-lookup"><span data-stu-id="291c8-117">Select Proposal only to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
7. <span data-ttu-id="291c8-118">在“GL 过帐日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="291c8-118">In the GL posting date field, enter a date.</span></span>
8. <span data-ttu-id="291c8-119">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="291c8-119">Click OK.</span></span>
9. <span data-ttu-id="291c8-120">转到总分类记账>分配>分配日记账。</span><span class="sxs-lookup"><span data-stu-id="291c8-120">Go to General ledger > Allocations > Allocation journals.</span></span>
10. <span data-ttu-id="291c8-121">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="291c8-121">Click Lines.</span></span>
11. <span data-ttu-id="291c8-122">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="291c8-122">Click Post.</span></span>
12. <span data-ttu-id="291c8-123">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="291c8-123">Click Post.</span></span>


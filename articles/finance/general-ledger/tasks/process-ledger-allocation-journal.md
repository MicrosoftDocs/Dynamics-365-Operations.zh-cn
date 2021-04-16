---
title: 处理分类帐分配日记帐
description: 此主题介绍如何在 Dynamics 365 Finance 中处理分配请求。
author: aprilolson
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e89aa21f988d50bc1a922e053be0ff2dcd196268
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834400"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="b54a6-103">处理分类帐分配日记帐</span><span class="sxs-lookup"><span data-stu-id="b54a6-103">Process ledger allocation journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b54a6-104">此主题介绍如何处理分配请求。</span><span class="sxs-lookup"><span data-stu-id="b54a6-104">This topic explains how to process an allocation request.</span></span> <span data-ttu-id="b54a6-105">使用“处理分配请求”页面以创建可在过帐至总帐前检查和审核，或直接过帐至总帐的分配日记帐。</span><span class="sxs-lookup"><span data-stu-id="b54a6-105">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="b54a6-106">必须至少有一个有效的分类帐分配规则才能创建分配日记帐。</span><span class="sxs-lookup"><span data-stu-id="b54a6-106">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="b54a6-107">此任务使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="b54a6-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="b54a6-108">在导航窗格中，转到 **模块 > 总帐 > 分配 > 处理分配请求**。</span><span class="sxs-lookup"><span data-stu-id="b54a6-108">In the navigation pane, go to **Modules > General ledger > Allocations > Process allocation request**.</span></span>
2. <span data-ttu-id="b54a6-109">在 **规则** 字段中，在下拉菜单中选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b54a6-109">In the **Rule** field, select the desired record in the drop-down menu.</span></span>
3. <span data-ttu-id="b54a6-110">在 **截止日期** 字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="b54a6-110">In the **As of date** field, enter a date.</span></span>

    - <span data-ttu-id="b54a6-111">**截止日期** 非常重要，因为根据规则分类帐是数据源头。</span><span class="sxs-lookup"><span data-stu-id="b54a6-111">The **As of Date** is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="b54a6-112">这个日期决定分配被包括哪个分类帐平衡表。</span><span class="sxs-lookup"><span data-stu-id="b54a6-112">This date controls which ledger balances to include for allocation.</span></span>  
    - <span data-ttu-id="b54a6-113">在 **零资源** 字段中，选择 **停止**。</span><span class="sxs-lookup"><span data-stu-id="b54a6-113">In the **Zero source** field select **Stop**.</span></span> <span data-ttu-id="b54a6-114">这将停止分配过程，然后显示一条信息说”选择了零资源数“。</span><span class="sxs-lookup"><span data-stu-id="b54a6-114">This will stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  

4. <span data-ttu-id="b54a6-115">在 **方案选项** 字段中，选择 **仅方案**。</span><span class="sxs-lookup"><span data-stu-id="b54a6-115">In the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="b54a6-116">选择 **仅方案** 会在将分配过帐至总帐前，检查并选择性审核“分配”日记帐中的结果。</span><span class="sxs-lookup"><span data-stu-id="b54a6-116">Select **Proposal only** to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
5. <span data-ttu-id="b54a6-117">在“GL 过帐日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="b54a6-117">In the GL posting date field, enter a date.</span></span>
6. <span data-ttu-id="b54a6-118">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b54a6-118">Select **OK**.</span></span>
7. <span data-ttu-id="b54a6-119">在导航窗格中，转到 **模块 > 总帐 > 分配 > 分配日记帐**。</span><span class="sxs-lookup"><span data-stu-id="b54a6-119">In the navigation pane, go to **Modules > General ledger > Allocations > Allocation journals**.</span></span>
8. <span data-ttu-id="b54a6-120">选择 **行**。</span><span class="sxs-lookup"><span data-stu-id="b54a6-120">Select **Lines**.</span></span>
9. <span data-ttu-id="b54a6-121">选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="b54a6-121">Select **Post**.</span></span>
10. <span data-ttu-id="b54a6-122">选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="b54a6-122">Select **Post**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
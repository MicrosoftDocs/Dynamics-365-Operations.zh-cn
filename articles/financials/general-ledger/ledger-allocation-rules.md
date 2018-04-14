---
title: "分类帐分配规则"
description: "本文提供有关分类帐分配规则的信息。 介绍这些分配规则的各个组件和可为其使用的分配方法。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e5eb9d79fee7ec2e288db24aee9535d6414fdeed
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="ledger-allocation-rules"></a><span data-ttu-id="ca05e-104">分类帐分配规则</span><span class="sxs-lookup"><span data-stu-id="ca05e-104">Ledger allocation rules</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="ca05e-105">本文提供有关分类帐分配规则的信息。</span><span class="sxs-lookup"><span data-stu-id="ca05e-105">This article provides information about ledger allocation rules.</span></span> <span data-ttu-id="ca05e-106">介绍这些分配规则的各个组件和可为其使用的分配方法。</span><span class="sxs-lookup"><span data-stu-id="ca05e-106">It describes the various components of these allocation rules and the allocation methods that can be used for them.</span></span>

<span data-ttu-id="ca05e-107">分类帐分配规则用于自动计算并生成分配日记帐和科目分录，以便分配分类帐余额或固定金额。</span><span class="sxs-lookup"><span data-stu-id="ca05e-107">Ledger allocation rules are used to automatically calculate and generate allocation journals and account entries for the allocation of ledger balances or fixed amounts.</span></span> <span data-ttu-id="ca05e-108">分配方法可以是可变的，也可以是固定的。</span><span class="sxs-lookup"><span data-stu-id="ca05e-108">Allocation methods can be variable or fixed.</span></span> <span data-ttu-id="ca05e-109">以下分配方法可用于分类帐分配规则：</span><span class="sxs-lookup"><span data-stu-id="ca05e-109">The following allocation methods can be used for ledger allocation rules:</span></span>

-   <span data-ttu-id="ca05e-110">**基础** – 此可变方法在分配取决于实际分类帐余额时使用，基于筛选条件。</span><span class="sxs-lookup"><span data-stu-id="ca05e-110">**Basis** – This variable method is used when the allocation depends on the actual ledger balance, based on filter criteria.</span></span> <span data-ttu-id="ca05e-111">例如，可以基于每个部门的销售额相对于各部门总销售额的比例分配公司广告成本。</span><span class="sxs-lookup"><span data-stu-id="ca05e-111">For example, advertising expenses can be allocated based on each department's sales in proportion to the total departmental sales.</span></span>
-   <span data-ttu-id="ca05e-112">**“固定百分比”**和**“固定权重”**– 对于这些方法，分配百分比或权重是直接针对规则定义的。</span><span class="sxs-lookup"><span data-stu-id="ca05e-112">**Fixed percentage** and **Fixed weight** – For these methods, the allocation percentage or weight is defined directly for the rule.</span></span> <span data-ttu-id="ca05e-113">例如，可以分配广告支出，以便部门 A 收到 70% 的广告支出，部门 B 收到 30%。</span><span class="sxs-lookup"><span data-stu-id="ca05e-113">For example, advertising expenses can be allocated so that Department A receives 70 percent of the advertising expense and Department B receives 30 percent.</span></span>
-   <span data-ttu-id="ca05e-114">**平均** – 此方法将金额平均分配给每个定义的目标。</span><span class="sxs-lookup"><span data-stu-id="ca05e-114">**Equally** – This method distributes the amount equally to each defined destination.</span></span> <span data-ttu-id="ca05e-115">例如，如果为部门 A 和部门 B 定义了目标，则可以分配广告支出以便部门 A 和部门 B 收到 50% 的广告支出。</span><span class="sxs-lookup"><span data-stu-id="ca05e-115">For example, if destinations are defined for Department A and Department B, advertising expenses can be allocated so that both Department A and Department B receive 50 percent of the advertising expense.</span></span>

<span data-ttu-id="ca05e-116">如果“基础”用作分配规则的分配方法，则您还必须定义单独的分类帐分配基础规则。</span><span class="sxs-lookup"><span data-stu-id="ca05e-116">If Basis is used as the allocation method for an allocation rule, you must also define separate ledger allocation basis rules.</span></span> <span data-ttu-id="ca05e-117">“处理分配请求”流程允许用户在过帐或删除已计算的分摊之前，处理分类帐分配规则和预览生成的分配日记帐分录。</span><span class="sxs-lookup"><span data-stu-id="ca05e-117">The "Process allocation request" process lets users process the ledger allocation rule and preview the resulting allocation journal entries before they either post or delete the calculated allocations.</span></span>

## <a name="components-of-ledger-allocation-rules"></a><span data-ttu-id="ca05e-118">分类帐分配规则的组成部分</span><span class="sxs-lookup"><span data-stu-id="ca05e-118">Components of ledger allocation rules</span></span>
<span data-ttu-id="ca05e-119">每个分配规则都具有四个组成部分：常规、来源、目标和对方。</span><span class="sxs-lookup"><span data-stu-id="ca05e-119">Each allocation rule has four components: general, source, destination, and offset.</span></span> <span data-ttu-id="ca05e-120">一个附加的组成部分，即分类帐分配基础规则，在“基础”用作分配方法时是必需的。</span><span class="sxs-lookup"><span data-stu-id="ca05e-120">An additional component, ledger allocation bases rules, is required if Basis is used as the allocation method.</span></span> <span data-ttu-id="ca05e-121">每个组成部分都提供处理分配所需的信息的重要部分。</span><span class="sxs-lookup"><span data-stu-id="ca05e-121">Each component provides a critical piece of the information that is required in order to process allocations.</span></span>

-   <span data-ttu-id="ca05e-122">**常规** – 此组成部分是用户指定选项的位置，例如分配方法、内部公司规则设置以及规则是否处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="ca05e-122">**General** – This component is where the user specifies options such as the allocation method, intercompany rule settings, and whether the rule is active.</span></span>
-   <span data-ttu-id="ca05e-123">**来源** – 此组成部分是用户为分配指定源数据的位置。</span><span class="sxs-lookup"><span data-stu-id="ca05e-123">**Source** – This component is where the user specifies the source data for the allocation.</span></span> <span data-ttu-id="ca05e-124">分配可以基于分类帐余额（**数据源** = **分类帐**）或固定金额（**数据源** = **固定值**）。</span><span class="sxs-lookup"><span data-stu-id="ca05e-124">Allocation can be based on ledger balances (**Data source** = **Ledger**) or fixed amounts (**Data source** = **Fixed value**).</span></span> <span data-ttu-id="ca05e-125">当**“数据源”**设置为**“分类帐”**时，必须为分类帐分配规则定义来源筛选条件（例如，对于广告支出）。</span><span class="sxs-lookup"><span data-stu-id="ca05e-125">When **Data source** is set to **Ledger**, source filter criteria must be defined for the ledger allocation rule (for example, for the advertising expenses).</span></span>
-   <span data-ttu-id="ca05e-126">**目标** – 此组成部分定义应如何分配和考虑分配计算的结果。</span><span class="sxs-lookup"><span data-stu-id="ca05e-126">**Destination** – This component defines how the result of the allocation calculation should be distributed and accounted for.</span></span> <span data-ttu-id="ca05e-127">例如，每个部门可以有一个目标行。</span><span class="sxs-lookup"><span data-stu-id="ca05e-127">For example, there can be one destination line for each department.</span></span>
-   <span data-ttu-id="ca05e-128">**对方** – 此组成部分定义应如何为平衡目标条目的对方条目确定主科目和维度。</span><span class="sxs-lookup"><span data-stu-id="ca05e-128">**Offset** – This component defines how main accounts and dimensions should be determined for the offset entries that balance the destination entries.</span></span> <span data-ttu-id="ca05e-129">通常会使用用户定义的选项，而不是给予来源的帐户和维度。</span><span class="sxs-lookup"><span data-stu-id="ca05e-129">User-defined options are typically used instead of accounts and dimensions that are based on the source.</span></span> <span data-ttu-id="ca05e-130">当**“数据源”**设置为**“固定值”**时，**“来源”**将不能用作选项。</span><span class="sxs-lookup"><span data-stu-id="ca05e-130">When **Data source** is set to **Fixed value**, **Source** can't be used as an option.</span></span>
-   <span data-ttu-id="ca05e-131">**分类帐分配基础规则** – 这些规则使用自己的源筛选条件来确定应为分配使用哪个分类帐余额（例如，每个部门的收入）。</span><span class="sxs-lookup"><span data-stu-id="ca05e-131">**Ledger allocation basis rules** – These rules use their own source filter criteria to determine which ledger balances should be used for allocation (for example, the revenue per department).</span></span> <span data-ttu-id="ca05e-132">每个分配基础规则可以用于多个分配规则。</span><span class="sxs-lookup"><span data-stu-id="ca05e-132">Each allocation basis rule can be used with multiple allocation rules.</span></span>






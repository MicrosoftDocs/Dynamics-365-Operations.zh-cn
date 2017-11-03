---
title: "处理分配"
description: "本文提供有关分配、在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中处理分配的选项，以及如何在预算计划中使用它们的信息。 分配用于跨多个会计科目组合分配金额。 它们帮助确保向核算的正确对象计入费用或收入。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cb12e24fcb8e8c91f90b91e2fdb3039dd1735ca3
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="process-allocations"></a><span data-ttu-id="74e90-105">处理分配</span><span class="sxs-lookup"><span data-stu-id="74e90-105">Process allocations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="74e90-106">本文提供有关分配、在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中处理分配的选项，以及如何在预算计划中使用它们的信息。</span><span class="sxs-lookup"><span data-stu-id="74e90-106">This article provides information about allocations, the options for processing them in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, and how they can be used in budget planning.</span></span> <span data-ttu-id="74e90-107">分配用于跨多个会计科目组合分配金额。</span><span class="sxs-lookup"><span data-stu-id="74e90-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="74e90-108">它们帮助确保向核算的正确对象计入费用或收入。</span><span class="sxs-lookup"><span data-stu-id="74e90-108">They help guarantee that expenses or revenue is charged to the correct object in accounting.</span></span>

<span data-ttu-id="74e90-109">Microsoft Dynamics 365 for Finance and Operations 提供以下功能支持此流程：</span><span class="sxs-lookup"><span data-stu-id="74e90-109">Microsoft Dynamics 365 for Finance and Operations provides the following capabilities to support this process:</span></span>

-   <span data-ttu-id="74e90-110">通过在会计分配中使用“分解”操作，或者通过将财务维度默认模板应用到文档，手动分配交易记录金额。</span><span class="sxs-lookup"><span data-stu-id="74e90-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="74e90-111">有关详细信息，请参阅[会计分配](../accounts-payable/accounting-distributions.md)。</span><span class="sxs-lookup"><span data-stu-id="74e90-111">For more information, see [Accounting distributions.](../accounts-payable/accounting-distributions.md)</span></span>
-   <span data-ttu-id="74e90-112">将基于在单个主科目中定义的分配期限自动分配交易记录。</span><span class="sxs-lookup"><span data-stu-id="74e90-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="74e90-113">分配科目条目将基于百分比和目标会计科目为每个日记帐生成，只要会计条目满足定义为源会计科目的条件。</span><span class="sxs-lookup"><span data-stu-id="74e90-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span>
-   <span data-ttu-id="74e90-114">将基于分类帐分配规则自动分配分类帐余额或固定金额。</span><span class="sxs-lookup"><span data-stu-id="74e90-114">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="74e90-115">使用分配日记帐定期处理分类帐分配规则。</span><span class="sxs-lookup"><span data-stu-id="74e90-115">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> 

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="74e90-116">预算计划中的分配</span><span class="sxs-lookup"><span data-stu-id="74e90-116">Allocations in budget planning</span></span>

<span data-ttu-id="74e90-117">分类帐分配规则可以为预算计划使用。</span><span class="sxs-lookup"><span data-stu-id="74e90-117">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="74e90-118">当您在预算计划中使用分类帐分配规则时，分配规则的作用方式与其在分类帐中相同，但是源数据和目标数据来自预算计划。</span><span class="sxs-lookup"><span data-stu-id="74e90-118">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="74e90-119">您可以手动选择分类帐分配规则供预算计划使用。</span><span class="sxs-lookup"><span data-stu-id="74e90-119">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="74e90-120">或者，您可以使用作为工作流程的一部分运行的分配计划。</span><span class="sxs-lookup"><span data-stu-id="74e90-120">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="74e90-121">您不能为预算计划使用内部公司的分类帐分配规则。</span><span class="sxs-lookup"><span data-stu-id="74e90-121">You can’t use intercompany ledger allocation rules for budget planning.</span></span>







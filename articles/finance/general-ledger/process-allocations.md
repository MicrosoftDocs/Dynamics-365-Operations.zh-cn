---
title: 处理分配
description: 本文提供有关分配、在 Microsoft Dynamics 365 Finance 中处理分配的选项，以及如何在预算计划中使用它们的信息。 分配用于跨多个会计科目组合分配金额。 它们帮助确保向核算的正确对象计入费用或收入。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a715fe2ae0cb32e523248ffb15bdde4b36bd01d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990206"
---
# <a name="process-allocations"></a><span data-ttu-id="b67d3-105">处理分配</span><span class="sxs-lookup"><span data-stu-id="b67d3-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b67d3-106">本文提供有关分配、处理分配的选项，以及如何在预算计划中使用它们的信息。</span><span class="sxs-lookup"><span data-stu-id="b67d3-106">This article provides information about allocations, the options for processing them, and how they can be used in budget planning.</span></span> <span data-ttu-id="b67d3-107">分配用于跨多个会计科目组合分配金额。</span><span class="sxs-lookup"><span data-stu-id="b67d3-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="b67d3-108">它们帮助确保向核算的正确对象计入费用或收入。</span><span class="sxs-lookup"><span data-stu-id="b67d3-108">They help ensure that expenses or revenues are charged to the correct object in accounting.</span></span>

<span data-ttu-id="b67d3-109">以下功能支持此流程：</span><span class="sxs-lookup"><span data-stu-id="b67d3-109">The following capabilities support this process:</span></span>

-   <span data-ttu-id="b67d3-110">通过在会计分配中使用“分解”操作，或者通过将财务维度默认模板应用到文档，手动分配交易记录金额。</span><span class="sxs-lookup"><span data-stu-id="b67d3-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="b67d3-111">有关详细信息，请参阅[会计分配](../accounts-payable/accounting-distributions.md)。</span><span class="sxs-lookup"><span data-stu-id="b67d3-111">For more information, see [Accounting distributions](../accounts-payable/accounting-distributions.md).</span></span>
-   <span data-ttu-id="b67d3-112">将基于在单个主科目中定义的分配期限自动分配交易记录。</span><span class="sxs-lookup"><span data-stu-id="b67d3-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="b67d3-113">分配科目条目将基于百分比和目标会计科目为每个日记帐生成，只要会计条目满足定义为源会计科目的条件。</span><span class="sxs-lookup"><span data-stu-id="b67d3-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span> <span data-ttu-id="b67d3-114">有关详细信息，请参阅[主科目分摊条件](../general-ledger/main-account-allocation-terms.md)</span><span class="sxs-lookup"><span data-stu-id="b67d3-114">For more information, see [Main account allocation terms](../general-ledger/main-account-allocation-terms.md)</span></span>
-   <span data-ttu-id="b67d3-115">将基于分类帐分配规则自动分配分类帐余额或固定金额。</span><span class="sxs-lookup"><span data-stu-id="b67d3-115">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="b67d3-116">使用分配日记帐定期处理分类帐分配规则。</span><span class="sxs-lookup"><span data-stu-id="b67d3-116">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> <span data-ttu-id="b67d3-117">有关详细信息，请参阅[分配规则](../general-ledger/ledger-allocation-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="b67d3-117">For more information, see [Allocation rules](../general-ledger/ledger-allocation-rules.md).</span></span>

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="b67d3-118">预算计划中的分配</span><span class="sxs-lookup"><span data-stu-id="b67d3-118">Allocations in budget planning</span></span>

<span data-ttu-id="b67d3-119">分类帐分配规则可以为预算计划使用。</span><span class="sxs-lookup"><span data-stu-id="b67d3-119">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="b67d3-120">当您在预算计划中使用分类帐分配规则时，分配规则的作用方式与其在分类帐中相同，但是源数据和目标数据来自预算计划。</span><span class="sxs-lookup"><span data-stu-id="b67d3-120">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="b67d3-121">您可以手动选择分类帐分配规则供预算计划使用。</span><span class="sxs-lookup"><span data-stu-id="b67d3-121">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="b67d3-122">或者，您可以使用作为工作流程的一部分运行的分配计划。</span><span class="sxs-lookup"><span data-stu-id="b67d3-122">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="b67d3-123">您不能为预算计划使用内部公司的分类帐分配规则。</span><span class="sxs-lookup"><span data-stu-id="b67d3-123">You can’t use intercompany ledger allocation rules for budget planning.</span></span>


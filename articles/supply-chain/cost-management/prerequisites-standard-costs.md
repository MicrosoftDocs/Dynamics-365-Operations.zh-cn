---
title: "针对标准成本的先决条件"
description: "本主题介绍使用标准成本的基本步骤。"
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: d5a4a4e49ef1cee923011ddab24497c65f85c1e3
ms.contentlocale: zh-cn
ms.lasthandoff: 08/08/2018

---

# <a name="prerequisites-for-standard-costs"></a><span data-ttu-id="1e2c4-103">针对标准成本的先决条件</span><span class="sxs-lookup"><span data-stu-id="1e2c4-103">Prerequisites for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e2c4-104">本主题介绍使用标准成本的基本步骤。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="1e2c4-105">后续步骤取决于公司的运营。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="1e2c4-106">例如，对于非制造环境、不使用工艺路线的制造环境和使用工艺路线的制造环境，这些步骤有所不同。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="1e2c4-107">若要设置标准成本，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="1e2c4-108">**1. 为标准成本创建一个物料模型组。**</span><span class="sxs-lookup"><span data-stu-id="1e2c4-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="1e2c4-109">使用**物料模型组**页面为标准成本创建一个新组，并且分配**标准成本**的库存模型。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="1e2c4-110">该物料模型组的标识符应该有意义，例如**标准成本**。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="1e2c4-111">选中复选框以指示该组应该允许财务负库存，并且应该过帐物理库存和财务库存。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="1e2c4-112">此标准成本组将分配给物料。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="1e2c4-113">**2. 定义与标准成本差异相关的会计科目。**</span><span class="sxs-lookup"><span data-stu-id="1e2c4-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="1e2c4-114">使用**会计科目表**页面可以定义与标准成本差异相关的会计科目。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="1e2c4-115">这些会计科目必须首先定义，然后才能在**过帐**页面中分配它们。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="1e2c4-116">这些会计科目可以反映物料组和成本组。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="1e2c4-117">**3. 将会计科目分配到与标准成本差异相关的物料过帐。**</span><span class="sxs-lookup"><span data-stu-id="1e2c4-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="1e2c4-118">使用**过帐**页面可以分配与标准成本差异相关的会计科目。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="1e2c4-119">您可以按物料（或者物料组）和按成本组（或者成本组类型）指定某一差异的会计科目，或者指定该会计科目应用于所有物料和所有成本组。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="1e2c4-120">这些选项对应于针对表、组和全部的成本关系。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="1e2c4-121">定义物料过帐规则前，可使用**交易记录组合**页启用成本关系（针对表、组和全部）。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="1e2c4-122">**4. 定义与标准成本差异相关的库存参数。**</span><span class="sxs-lookup"><span data-stu-id="1e2c4-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="1e2c4-123">使用**库存会计政策设置 > 参数**页面中的**库存会计**选项卡可以定义与标准成本有关的两个成本控制参数。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-123">Use the **Inventory accounting** tab on the **Inventory accounting policies setup > Parameters** page to define two cost control parameters that are related to standard costs.</span></span>

    -  <span data-ttu-id="1e2c4-124">在**成本细分**字段中，选择**无**或**子分类帐**。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="1e2c4-125">如果选择**子分类帐**，则该成本分解为*有效*成本分解。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="1e2c4-126">对于跨标准成本物料的多级产品结构计算、保留和查看成本组细分，有效成本细分十分重要。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="1e2c4-127">在成本细分有效时，您可以采用单个级别、多个级别或总计格式，报告和分析每个成本组的库存、在制品 (WIP) 和所售货物成本 (COGS)。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="1e2c4-128">成本分解有效时，如果激活制造物料的成本，将把成本组分解存储在物料的成本记录内。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="1e2c4-129">如果选择**无**，将不为标准成本物料维护成本组分解。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="1e2c4-130">也就是说，制造物料的标准成本将不进行成本组分解，而是作为单一金额计算和维护。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="1e2c4-131">制造组件的成本组成将聚合为这个单一金额。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="1e2c4-132">在**与标准的差异**字段中，选择**汇总**或**按成本组**。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="1e2c4-133">如果选择**按成本组**，您可以按成本组标识采购价差异和生产差异。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="1e2c4-134">也可以帮您标识四类生产差异：批次规模、数量、价格和替换差异。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="1e2c4-135">如果选择**汇总**，则不能按成本组标识差异，也不能标识四种类型的生产差异。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="1e2c4-136">只能查看汇总的生产差异。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="1e2c4-137">与标准差异有关的策略独立于成本细分策略。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="1e2c4-138">也就是说，您可以选择**没有**成本细分策略，并且选择按成本组差异，以便仍将捕获按成本组的生产差异。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="1e2c4-139">**5. 为标准成本创建成本计算版本。**</span><span class="sxs-lookup"><span data-stu-id="1e2c4-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="1e2c4-140">使用**成本计算版本设置**页面可为标准成本创建一个或多个成本计算版本。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="1e2c4-141">每一成本计算版本都必须用**标准成本**的成本计算类型指定，并且必须允许内容包括成本数据。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="1e2c4-142">**6. 准备现有客户以使用标准成本。**</span><span class="sxs-lookup"><span data-stu-id="1e2c4-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="1e2c4-143">想要将其现有物料更改为标准成本库存模型的客户必须使用**标准成本转换**页面。</span><span class="sxs-lookup"><span data-stu-id="1e2c4-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="1e2c4-144">相关主题</span><span class="sxs-lookup"><span data-stu-id="1e2c4-144">Related topics</span></span>
--------

[<span data-ttu-id="1e2c4-145">标准成本转换概览</span><span class="sxs-lookup"><span data-stu-id="1e2c4-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)

### <a name="blogs"></a><span data-ttu-id="1e2c4-146">博客</span><span class="sxs-lookup"><span data-stu-id="1e2c4-146">Blogs</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="1e2c4-147">社区博客</span><span class="sxs-lookup"><span data-stu-id="1e2c4-147">Community blogs</span></span>

- [<span data-ttu-id="1e2c4-148">如何在 Dynamics 365 for Finance and Operations 中为直接材料设置标准成本</span><span class="sxs-lookup"><span data-stu-id="1e2c4-148">How to set up standard costs for direct materials in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [<span data-ttu-id="1e2c4-149">Dynamics 365 for Finance and Operations 中的标准直接人工成本</span><span class="sxs-lookup"><span data-stu-id="1e2c4-149">Standard direct labor costs in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)


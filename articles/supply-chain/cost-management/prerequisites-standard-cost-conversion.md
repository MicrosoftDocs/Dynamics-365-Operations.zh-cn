---
title: 用于标准成本转换的先决条件
description: 本主题讨论在运行标准成本转换前需执行的任务。
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 50891
ms.assetid: 73af66cf-c924-45be-837a-a648dbd05a31
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b78cfb2c6f0462a86cf3785038c5fe4e5d63b9cf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809678"
---
# <a name="prerequisites-for-a-standard-cost-conversion"></a><span data-ttu-id="12a9f-103">用于标准成本转换的先决条件</span><span class="sxs-lookup"><span data-stu-id="12a9f-103">Prerequisites for a standard cost conversion</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12a9f-104">本主题讨论在运行标准成本转换前需执行的任务。</span><span class="sxs-lookup"><span data-stu-id="12a9f-104">This topic discusses tasks to perform before you run a standard cost conversion.</span></span> 

<span data-ttu-id="12a9f-105">在运行标准成本转换前，请执行这些步骤：</span><span class="sxs-lookup"><span data-stu-id="12a9f-105">Before you run a standard cost conversion, follow these steps:</span></span>

1.  <span data-ttu-id="12a9f-106">为标准成本定义一个 **物料模型组**。</span><span class="sxs-lookup"><span data-stu-id="12a9f-106">Define an **item model group** for standard costs.</span></span> <span data-ttu-id="12a9f-107">使用“物料模型组”页可以创建具有标准成本库存模型的物料模型组。</span><span class="sxs-lookup"><span data-stu-id="12a9f-107">Use the Item model groups page to create an item model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="12a9f-108">在设置标准成本转换时，您将此物料模型组分配给要转换的物料。</span><span class="sxs-lookup"><span data-stu-id="12a9f-108">When setting up a standard cost conversion, you assign this item model group to the items that are being converted.</span></span>
2.  <span data-ttu-id="12a9f-109">将某一 **成本组** 分配给每个物料。</span><span class="sxs-lookup"><span data-stu-id="12a9f-109">Assign a **cost group** to each item.</span></span>
    -   <span data-ttu-id="12a9f-110">分配给采购物料的成本组可以充当分配与标准成本相关的会计科目的基础。</span><span class="sxs-lookup"><span data-stu-id="12a9f-110">The cost group that is assigned to a purchased item can act as the basis for assigning ledger accounts that are related to standard costs.</span></span> <span data-ttu-id="12a9f-111">这可能包括为采购价差异分配会计科目。</span><span class="sxs-lookup"><span data-stu-id="12a9f-111">This can include assigning ledger accounts for purchase price variances.</span></span> <span data-ttu-id="12a9f-112">在制造环境中，分配给采购组件的成本组还在制造物料的计算成本中提供成本细分。</span><span class="sxs-lookup"><span data-stu-id="12a9f-112">In a manufacturing environment, the cost group that is assigned to purchased components also provides cost segmentation in the calculated costs of a manufactured item.</span></span>
    -   <span data-ttu-id="12a9f-113">分配给某一制造物料的成本组可以充当分配与标准成本相关的会计科目的基础，例如为生产差异分配会计科目。</span><span class="sxs-lookup"><span data-stu-id="12a9f-113">The cost group that is assigned to a manufactured item can act as the basis for assigning ledger accounts that are related to standard costs, such as assigning ledger accounts for production variances.</span></span>

3.  <span data-ttu-id="12a9f-114">在某一制造物料具有固定成本时将某一 **标准订单数量** 分配给该制造物料。</span><span class="sxs-lookup"><span data-stu-id="12a9f-114">Assign a **standard order quantity** to a manufactured item when it has constant costs.</span></span> <span data-ttu-id="12a9f-115">制造物料的标准订单数量充当用于摊销或按比例分配、固定成本的会计批次规模。</span><span class="sxs-lookup"><span data-stu-id="12a9f-115">The standard order quantity for a manufactured item acts as an accounting lot size for amortizing, or prorating, constant costs.</span></span> <span data-ttu-id="12a9f-116">这些可以包括工艺路线工序的设置时间或物料清单 (BOM) 的固定组件数量。</span><span class="sxs-lookup"><span data-stu-id="12a9f-116">These can include setup times in routing operations or a constant component quantity in a bill of material (BOM).</span></span>
4.  <span data-ttu-id="12a9f-117">分配与标准成本相关的 **总帐科目**，尤其是重估差异。</span><span class="sxs-lookup"><span data-stu-id="12a9f-117">Assign **general ledger accounts** that are related to standard costs, especially the revaluation variance.</span></span> <span data-ttu-id="12a9f-118">使用 **过帐** 页（**库存管理** &gt; **设置**）可以分配与标准成本相关的总帐科目。</span><span class="sxs-lookup"><span data-stu-id="12a9f-118">Use the **Posting** page (**Inventory management** &gt; **Setup**) to assign general ledger accounts that are related to standard costs.</span></span> <span data-ttu-id="12a9f-119">至少对于标准成本转换流程，您必须为所有物料和所有成本组的重估差异分配科目。</span><span class="sxs-lookup"><span data-stu-id="12a9f-119">As a minimum for the standard cost conversion process, you must assign the account for the revaluation variance for all items and all cost groups.</span></span> <span data-ttu-id="12a9f-120">使用 **会计科目表** 页可以定义标准成本所需的总帐科目。</span><span class="sxs-lookup"><span data-stu-id="12a9f-120">Use the **Chart of accounts** page to define the general ledger accounts that will be needed for standard costs.</span></span> <span data-ttu-id="12a9f-121">使用 **交易记录组合** 页可以在您定义物料过帐规则前启用成本关系（针对表、组和全部）。</span><span class="sxs-lookup"><span data-stu-id="12a9f-121">Use the **Transaction combinations** page to enable cost relations (for tables, groups, and all) before you define the item posting rules.</span></span>
5.  <span data-ttu-id="12a9f-122">定义与标准成本相关的库存参数。</span><span class="sxs-lookup"><span data-stu-id="12a9f-122">Define the inventory parameters that are related to standard costs.</span></span> <span data-ttu-id="12a9f-123">使用 **库存和仓库管理参数** 页上的 **编号规则** 选项卡可以将编号规则分配给重估凭证。</span><span class="sxs-lookup"><span data-stu-id="12a9f-123">Use the **Number sequences** tab on the **Inventory and warehouse management parameters** page to assign a number sequence to revaluation vouchers.</span></span> <span data-ttu-id="12a9f-124">在标准成本转换导致物料的库存成本发生变化时，生成重估凭证。</span><span class="sxs-lookup"><span data-stu-id="12a9f-124">A revaluation voucher is generated when the standard cost conversion creates a change of an item's inventory value.</span></span> <span data-ttu-id="12a9f-125">使用 **库存和仓库管理参数** 页可以定义成本控制参数（**库存会计** 选项卡上）以定义与标准成本相关的两个参数。</span><span class="sxs-lookup"><span data-stu-id="12a9f-125">Use the **Inventory and warehouse management parameters** page to define Cost Control parameters (on the **Inventory accounting** tab) to define two parameters that are related to standard costs.</span></span>
    -   <span data-ttu-id="12a9f-126">使用 **成本细分** 字段可以选择“否”或“子分类帐”。</span><span class="sxs-lookup"><span data-stu-id="12a9f-126">Use the **Cost breakdown** field to select No or Sub ledger.</span></span> <span data-ttu-id="12a9f-127">“子分类帐”的选择称作有效成本细分。</span><span class="sxs-lookup"><span data-stu-id="12a9f-127">The selection of Sub ledger is termed an active cost breakdown.</span></span> <span data-ttu-id="12a9f-128">对于跨标准成本物料的多级产品结构计算、保留和查看成本组细分，有效成本细分十分重要。</span><span class="sxs-lookup"><span data-stu-id="12a9f-128">An active cost breakdown is very important for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="12a9f-129">在成本细分有效时，您可以采用单个级别，多个级别或总计格式报告和分析以下：</span><span class="sxs-lookup"><span data-stu-id="12a9f-129">When the cost breakdown is active, you can report and analyze the following in a single level, multi-level, or total format:</span></span>
        1.  <span data-ttu-id="12a9f-130">库存</span><span class="sxs-lookup"><span data-stu-id="12a9f-130">Inventory</span></span>
        2.  <span data-ttu-id="12a9f-131">在制品 (WIP)</span><span class="sxs-lookup"><span data-stu-id="12a9f-131">Work in process (WIP)</span></span>
        3.  <span data-ttu-id="12a9f-132">每个成本组的所售货物成本 (COGS)</span><span class="sxs-lookup"><span data-stu-id="12a9f-132">Cost of goods sold (COGS) per cost group</span></span>

        <span data-ttu-id="12a9f-133">有效成本细分意味着如果启用制造物料的成本，其结果将存储在物料的成本记录内的成本组细分中。</span><span class="sxs-lookup"><span data-stu-id="12a9f-133">An active cost breakdown means that if you enable a manufactured item's cost, the result will be stored in the cost group segmentation in the item's cost record.</span></span> <span data-ttu-id="12a9f-134">如果未在 **成本细分** 字段中放值，则不会为标准成本物料维护成本组细分。</span><span class="sxs-lookup"><span data-stu-id="12a9f-134">If you put no value in the **Cost breakdown** field, the cost group segmentation will not be maintained for standard cost items.</span></span> <span data-ttu-id="12a9f-135">也就是说，制造物料的标准成本将作为没有成本组细分的单个金额计算和维护，并且制造组件的成本份额将聚合到此单个金额中。</span><span class="sxs-lookup"><span data-stu-id="12a9f-135">That is, a manufactured item's standard cost will be calculated and maintained as a single amount without cost group segmentation, and the cost contributions of manufactured components will be aggregated into the single amount.</span></span>
    -   <span data-ttu-id="12a9f-136">使用 **与标准的差异** 字段选择汇总的成本组或各成本组。</span><span class="sxs-lookup"><span data-stu-id="12a9f-136">Use the **Variances to standard** field to select summarized or per cost group.</span></span> <span data-ttu-id="12a9f-137">按成本组的选择使您能够按成本组标识采购价差异和生产差异。</span><span class="sxs-lookup"><span data-stu-id="12a9f-137">The selection of per cost group enables you to identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="12a9f-138">这也可以帮您标识四类生产差异（批次规模、数量、价格和替换差异）。</span><span class="sxs-lookup"><span data-stu-id="12a9f-138">This also enables you to identify the four types of production variances (the lot size, quantity, price, and substitution variances).</span></span> <span data-ttu-id="12a9f-139">选择汇总将意味着您不能按成本组标识差异，并且不能标识四种类型的生产差异。</span><span class="sxs-lookup"><span data-stu-id="12a9f-139">If you select summarized, you cannot identify variances by cost group, and you cannot identify the four types of production variances.</span></span> <span data-ttu-id="12a9f-140">您只能查看汇总的生产差异。</span><span class="sxs-lookup"><span data-stu-id="12a9f-140">You can only view a summarized production variance.</span></span> <span data-ttu-id="12a9f-141">与标准差异有关的策略独立于成本细分策略。</span><span class="sxs-lookup"><span data-stu-id="12a9f-141">The policy about variance to standard is independent of the cost breakdown policy.</span></span> <span data-ttu-id="12a9f-142">也就是说，您可以选择没有成本细分策略，并且选择按成本组差异，以便仍将捕获按成本组的生产差异。</span><span class="sxs-lookup"><span data-stu-id="12a9f-142">That is, you can select a cost breakdown policy of none, and select variances per cost group, so that production variances by cost group will still be captured.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
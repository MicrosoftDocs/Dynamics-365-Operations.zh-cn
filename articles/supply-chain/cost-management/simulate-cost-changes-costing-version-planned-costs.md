---
title: "通过将成本计算版本用于计划成本，模拟成本变化"
description: "本文说明您如何使用针对计划成本的某一单独成本计算版本模拟成本变化对制造物料的计算成本的影响。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 78183
ms.assetid: 1e41953f-cdb9-4598-b776-46e49383a773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 3ef3cdb2ede2c30609db4addfc10b819629cdc64
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="simulate-cost-changes-by-using-a-costing-version-for-planned-costs"></a><span data-ttu-id="949d7-103">通过将成本计算版本用于计划成本，模拟成本变化</span><span class="sxs-lookup"><span data-stu-id="949d7-103">Simulate cost changes by using a costing version for planned costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="949d7-104">本文说明您如何使用针对计划成本的某一单独成本计算版本模拟成本变化对制造物料的计算成本的影响。</span><span class="sxs-lookup"><span data-stu-id="949d7-104">This article explains how you can simulate the effects of cost changes on a manufactured item’s calculated costs by using a separate costing version for planned costs.</span></span>

<span data-ttu-id="949d7-105">您可以使用针对计划成本的某一单独成本计算版本模拟成本变化对制造物料的计算成本的影响。</span><span class="sxs-lookup"><span data-stu-id="949d7-105">You can simulate the effects of cost changes on the calculated costs of a manufactured item by using a separate costing version for planned costs.</span></span> <span data-ttu-id="949d7-106">使用此单独的成本计算版本来输入反映增加的成本变化的未决成本记录，以及计算对制造物料的成本影响。</span><span class="sxs-lookup"><span data-stu-id="949d7-106">Use this separate costing version to enter pending cost records that reflect incremental cost changes, and to calculate the cost impact on manufactured items.</span></span> <span data-ttu-id="949d7-107">由于有效成本回退原则将用于物料清单 (BOM) 计算，只有增加的成本变化必须输入。</span><span class="sxs-lookup"><span data-stu-id="949d7-107">Because the Active costs fallback principle will be used in the bill of materials (BOM) calculations, only the incremental cost changes must be entered.</span></span>

## <a name="guidelines-for-defining-the-simulation-costing-version"></a><span data-ttu-id="949d7-108">用于定义模拟成本计算版本的准则</span><span class="sxs-lookup"><span data-stu-id="949d7-108">Guidelines for defining the simulation costing version</span></span>
<span data-ttu-id="949d7-109">在定义模拟成本计算版本时遵循以下准则：</span><span class="sxs-lookup"><span data-stu-id="949d7-109">Use the following guidelines when you define the costing version for simulations:</span></span>

-   <span data-ttu-id="949d7-110">分配**计划成本**的成本计算类型。</span><span class="sxs-lookup"><span data-stu-id="949d7-110">Assign a costing type of **Planned costs**.</span></span>
-   <span data-ttu-id="949d7-111">为成本计算版本分配有意义的标识符，如**模拟**。</span><span class="sxs-lookup"><span data-stu-id="949d7-111">Assign a meaningful identifier for the costing version, such as **Simulation**.</span></span>
-   <span data-ttu-id="949d7-112">请确保内容包括成本记录。</span><span class="sxs-lookup"><span data-stu-id="949d7-112">Make sure that the content includes cost records.</span></span>
-   <span data-ttu-id="949d7-113">允许输入成本记录。</span><span class="sxs-lookup"><span data-stu-id="949d7-113">Allow the entry of cost records.</span></span> <span data-ttu-id="949d7-114">不要阻止未决成本的输入。</span><span class="sxs-lookup"><span data-stu-id="949d7-114">Don't block the entry of pending costs.</span></span>
-   <span data-ttu-id="949d7-115">允许输入所有站点的成本记录。</span><span class="sxs-lookup"><span data-stu-id="949d7-115">Allow the entry of cost records for all sites.</span></span> <span data-ttu-id="949d7-116">如果指定某个站点，将限制成本记录的输入为该站。</span><span class="sxs-lookup"><span data-stu-id="949d7-116">If you specify a site, you will limit the entry of cost records to that site.</span></span>
-   <span data-ttu-id="949d7-117">阻止激活未决成本。</span><span class="sxs-lookup"><span data-stu-id="949d7-117">Prevent the activation of pending costs.</span></span> <span data-ttu-id="949d7-118">在模拟成本计算版本中，仅必须为成本记录输入未决成本。</span><span class="sxs-lookup"><span data-stu-id="949d7-118">Only pending costs must be entered for cost records in the simulation costing version.</span></span>
-   <span data-ttu-id="949d7-119">不要输入“开始”日期。</span><span class="sxs-lookup"><span data-stu-id="949d7-119">Don't enter a "from" date.</span></span> <span data-ttu-id="949d7-120">将为使用模拟成本计算版本的每个物料清单计算输入计算日期。</span><span class="sxs-lookup"><span data-stu-id="949d7-120">A calculation date will be entered for each BOM calculation that uses the simulation costing version.</span></span>
-   <span data-ttu-id="949d7-121">指定**当前有效**的回退原则。</span><span class="sxs-lookup"><span data-stu-id="949d7-121">Specify a fallback principle of **Current active**.</span></span> <span data-ttu-id="949d7-122">该回退原则支持出于模拟目的输入增加的成本变化，但使用当前有效的成本作为所有其他成本记录的来源。</span><span class="sxs-lookup"><span data-stu-id="949d7-122">The fallback principle enables incremental cost changes to be entered for simulation purposes but uses the current active costs as the source for all other cost records.</span></span> <span data-ttu-id="949d7-123">我们假定对于所有其他成本记录都存在所有当前有效的成本。</span><span class="sxs-lookup"><span data-stu-id="949d7-123">We assume that all current active costs exist for all other cost records.</span></span>
-   <span data-ttu-id="949d7-124">指定**版本成本价**的成本价模型，但不限制计算。</span><span class="sxs-lookup"><span data-stu-id="949d7-124">Specify a cost price model of **Version cost price**, but don't restrict calculations.</span></span> <span data-ttu-id="949d7-125">例如，该模拟还可以使用**物料清单计算组**成本价模型，以便指示采购物料的成本份额数据来源。</span><span class="sxs-lookup"><span data-stu-id="949d7-125">For example, the simulations can also use the **BOM calculation group** cost price model to indicate the source of cost contribution data for purchased items.</span></span>
-   <span data-ttu-id="949d7-126">指定**多级**分解模式，但不限制计算。</span><span class="sxs-lookup"><span data-stu-id="949d7-126">Specify an explosion mode of **Multilevel**, but don't restrict calculations.</span></span> <span data-ttu-id="949d7-127">这些模拟可以使用其他分解模式。</span><span class="sxs-lookup"><span data-stu-id="949d7-127">The simulations can use other explosion modes.</span></span>

## <a name="costing-versions"></a><span data-ttu-id="949d7-128">成本计算版本</span><span class="sxs-lookup"><span data-stu-id="949d7-128">Costing versions</span></span>
<span data-ttu-id="949d7-129">以下场景说明如何使用模拟成本计算版本来模拟成本变化的影响。</span><span class="sxs-lookup"><span data-stu-id="949d7-129">The following scenarios illustrate how the simulation costing version is used to simulate the impact of cost changes.</span></span> <span data-ttu-id="949d7-130">在输入模拟的成本变化前，请删除模板成本计算版本内的未决成本记录，以便您具有明确的起始点。</span><span class="sxs-lookup"><span data-stu-id="949d7-130">Before you enter a simulated cost change, delete the pending cost records in the simulation costing version, so that you have a clean starting point.</span></span> <span data-ttu-id="949d7-131">使用**物料价格**页查看和删除与物料价格和成本类别价格相关的未决成本记录。</span><span class="sxs-lookup"><span data-stu-id="949d7-131">Use the **Item price** page to view and delete the pending cost records that are related to item prices and cost category prices.</span></span>

-   <span data-ttu-id="949d7-132">模拟某一采购物料的成本变化。</span><span class="sxs-lookup"><span data-stu-id="949d7-132">Simulate the cost change for a purchased item.</span></span> <span data-ttu-id="949d7-133">例如，成本变化可能反映关键采购材料成本的预期增减。</span><span class="sxs-lookup"><span data-stu-id="949d7-133">For example, the cost change might reflect an expected increase or decrease in the cost of critical purchased materials.</span></span> <span data-ttu-id="949d7-134">若要为某一采购物料定义不同成本，请使用**物料价格**页输入模拟成本计算版本内的未决成本记录。</span><span class="sxs-lookup"><span data-stu-id="949d7-134">To define the different cost for a purchased item, use the **Item price** page to enter a pending cost record in the simulation costing version.</span></span>
-   <span data-ttu-id="949d7-135">模拟某一成本类别的成本变化。</span><span class="sxs-lookup"><span data-stu-id="949d7-135">Simulate the cost change for a cost category.</span></span> <span data-ttu-id="949d7-136">例如，成本变化可以反映人工费率的预期增减，或者工序资源的小时工资率的增减。</span><span class="sxs-lookup"><span data-stu-id="949d7-136">For example, the cost change might reflect an expected increase or decrease in labor rates, or in the hourly rates for operations resources.</span></span> <span data-ttu-id="949d7-137">若要为某一成本类别定义不同成本，请使用**成本类别价格**页输入模拟成本计算版本内的未决成本记录。</span><span class="sxs-lookup"><span data-stu-id="949d7-137">To define the different cost for a cost category, use the **Cost category price** page to enter a pending cost record in the simulation costing version.</span></span>
-   <span data-ttu-id="949d7-138">模拟间接成本计算公式中的成本变化。</span><span class="sxs-lookup"><span data-stu-id="949d7-138">Simulate the cost change in an indirect cost calculation formula.</span></span> <span data-ttu-id="949d7-139">例如，成本变化可以反映制造开销中的预期增减。</span><span class="sxs-lookup"><span data-stu-id="949d7-139">For example, the cost change might reflect an expected increase or decrease in manufacturing overhead.</span></span> <span data-ttu-id="949d7-140">若要定义间接成本计算公式中的变化，请使用**成本计算单设置**页输入模拟成本计算版本中的未决成本记录，以及验证并保存该变化。</span><span class="sxs-lookup"><span data-stu-id="949d7-140">To define the change in an indirect cost calculation formula, use the **Costing sheet setup** page to enter a pending cost record in the simulation of costing version, and to validate and save the change.</span></span>

<span data-ttu-id="949d7-141">在输入模拟成本变化后，计算受成本变化影响的制造物料的成本。</span><span class="sxs-lookup"><span data-stu-id="949d7-141">After you enter the simulated cost changes, calculate the costs for manufactured items that are affected by the cost changes.</span></span> <span data-ttu-id="949d7-142">使用**计算**页来用于模拟成本计算版本，并且标识将受成本变化影响的所选制造物料。</span><span class="sxs-lookup"><span data-stu-id="949d7-142">Use the **Calculation** page for the simulation costing version, and identify the selected manufactured items that will be affected by the cost changes.</span></span> <span data-ttu-id="949d7-143">如果您没有选择特定物料，物料清单计算将适用于所有制造物料。</span><span class="sxs-lookup"><span data-stu-id="949d7-143">The BOM calculations apply to all manufactured items unless you select specific items.</span></span> <span data-ttu-id="949d7-144">或者，您可以使用物料清单计算选项来用于用途更新。</span><span class="sxs-lookup"><span data-stu-id="949d7-144">Alternatively, you can use the BOM calculation option for where-used updates.</span></span> <span data-ttu-id="949d7-145">查看模拟成本计算版本中的物料成本记录，以便分析模拟成本变化是如何影响所选制造物料的成本的。</span><span class="sxs-lookup"><span data-stu-id="949d7-145">View the item cost records in the simulation costing version to analyze how the simulated cost changes affected the costs of the selected manufactured items.</span></span> <span data-ttu-id="949d7-146">使用**物料价格**页和**计算物料成本**页可以查看和分析成本。</span><span class="sxs-lookup"><span data-stu-id="949d7-146">Use the **Item price** page and the **Calculate item cost** page to view and analyze the costs.</span></span>





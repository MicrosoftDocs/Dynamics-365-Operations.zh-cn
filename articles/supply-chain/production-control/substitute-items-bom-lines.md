---
title: "生产中的物料替换"
description: "本主题描述如何在生产流程中替换物料。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdBOM
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 70171
ms.assetid: ce3b11ef-550e-49b7-8942-2607c2ec3c5c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3ebf0582af5a9feec89625ec7b34432e50cf3c7b
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="material-substitution-in-manufacturing"></a><span data-ttu-id="c61d1-103">生产中的物料替换</span><span class="sxs-lookup"><span data-stu-id="c61d1-103">Material substitution in manufacturing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c61d1-104">本主题描述如何在生产流程中替换物料。</span><span class="sxs-lookup"><span data-stu-id="c61d1-104">This topic describes how to substitute materials during the production process.</span></span> 

<span data-ttu-id="c61d1-105">有三种方法可用于在生产流程中替换物料：</span><span class="sxs-lookup"><span data-stu-id="c61d1-105">There are three methods for substituting materials during the production process:</span></span>

-   <span data-ttu-id="c61d1-106">按照日期，即，在特定日期之后将一个物料替换为另一个物料时</span><span class="sxs-lookup"><span data-stu-id="c61d1-106">By date, when one material is substituted for another after a specific date</span></span>
-   <span data-ttu-id="c61d1-107">在主计划期间，即，因为物料的库存不足，将其替换为不同的物料时</span><span class="sxs-lookup"><span data-stu-id="c61d1-107">During master planning, when a material in a formula is substituted with a different material, because it's out of stock</span></span>
-   <span data-ttu-id="c61d1-108">在生产期间，即，当物料意外地库存不足并且被替换为不同物料时</span><span class="sxs-lookup"><span data-stu-id="c61d1-108">During production, when a material is unexpectedly out of stock and is substituted with a different material</span></span>

## <a name="substituting-material-by-date"></a><span data-ttu-id="c61d1-109">按日期替换物料</span><span class="sxs-lookup"><span data-stu-id="c61d1-109">Substituting material by date</span></span>
<span data-ttu-id="c61d1-110">请考虑以下方案：公司正在制造的机器包含将要在两个月内从供应商的目录到期的组件。</span><span class="sxs-lookup"><span data-stu-id="c61d1-110">Consider following scenario: A machine that a company is manufacturing contains a component that will expire from the vendor's catalog in two months.</span></span> <span data-ttu-id="c61d1-111">从到期日期开始，供应商将提供可替换旧组件的新组件。</span><span class="sxs-lookup"><span data-stu-id="c61d1-111">From the expiration date onward, the vendor will offer a new component that can be substituted for the old component.</span></span> <span data-ttu-id="c61d1-112">开始日期和结束日期可以在物料清单行上设置。</span><span class="sxs-lookup"><span data-stu-id="c61d1-112">From and to validity dates can be set up on bill of materials (BOM) lines.</span></span> <span data-ttu-id="c61d1-113">对于本示例，您通过在**“结束日期”**字段中输入到期日期将旧组件设置为到期。</span><span class="sxs-lookup"><span data-stu-id="c61d1-113">For this example, you set up the old component to expire by entering the expiration date in the **To-date** field.</span></span> <span data-ttu-id="c61d1-114">然后，在物料清单上，您设置新的替换组件，以便它从旧组件到期那天后生效。</span><span class="sxs-lookup"><span data-stu-id="c61d1-114">Then, on the BOM, you set up the new, replacement component so that it's valid from the day after the old component expires.</span></span> <span data-ttu-id="c61d1-115">为此，请在**“开始日期”**字段中输入开始日期。</span><span class="sxs-lookup"><span data-stu-id="c61d1-115">To do this, enter the start date in the **From-date** field.</span></span>

## <a name="substituting-material-by-planning"></a><span data-ttu-id="c61d1-116">按计划替换物料</span><span class="sxs-lookup"><span data-stu-id="c61d1-116">Substituting material by planning</span></span>
<span data-ttu-id="c61d1-117">只有当您使用配方时，而不是当您使用物料清单时，您才可以在计划期间替换物料。</span><span class="sxs-lookup"><span data-stu-id="c61d1-117">You can substitute materials during planning only when you're using formulas, not when you're using a BOM.</span></span> <span data-ttu-id="c61d1-118">请考虑以下方案：食品制造公司正在根据具有 20 种成分的配方制造调味汁。</span><span class="sxs-lookup"><span data-stu-id="c61d1-118">Consider following scenario: A food manufacturing company is making a sauce from a formula that has 20 ingredients.</span></span> <span data-ttu-id="c61d1-119">配方中的一种成分可由其他两种成分之一替换。</span><span class="sxs-lookup"><span data-stu-id="c61d1-119">One ingredient in the formula can be substituted by one of two other ingredients.</span></span> <span data-ttu-id="c61d1-120">但是，因为这两种成分比首选成分贵，所以只有当这种首选成分的库存不足时，才使用替换。</span><span class="sxs-lookup"><span data-stu-id="c61d1-120">However, because these two ingredients are more expensive than the preferred ingredient, substitution is used only if the preferred ingredient is out of stock.</span></span> <span data-ttu-id="c61d1-121">可以被替换的物料叫做 A，而可以替换它的两个物料叫做 B 和 C。按计划的物料替换是由配方行上的**“计划组”**和**“优先级”**字段控制的。</span><span class="sxs-lookup"><span data-stu-id="c61d1-121">The material that can be substituted is called A, whereas the two materials that can replace it are called B and C. Material substitution by planning is controlled by the **Plan group** and **Priority** fields on the formula lines.</span></span> <span data-ttu-id="c61d1-122">对于本示例，您可为三个物料创建配方行，并将配方行与相同计划组关联。</span><span class="sxs-lookup"><span data-stu-id="c61d1-122">For this example, you create formula lines for the three materials, and associate the formula lines with the same plan group.</span></span> <span data-ttu-id="c61d1-123">在设置中，物料 A 的配方行具有最高优先级（编号最小），物料 C 的配方行具有最低优先级，物料 B 的配方行具有介于其他两行的优先级之间的优先级。</span><span class="sxs-lookup"><span data-stu-id="c61d1-123">In the setup, the formula line for material A has the highest priority (lowest number), the formula line for material C has the lowest priority, and the formula line for material B has a priority that is between the priority of the other two lines.</span></span> <span data-ttu-id="c61d1-124">如果您对成品有要求，则主计划首先确定是否可以满足物料 A 的需求。</span><span class="sxs-lookup"><span data-stu-id="c61d1-124">If you have demand for the finished item, master planning first determines whether the demand for material A can be covered.</span></span> <span data-ttu-id="c61d1-125">如果无法满足该需求，则主计划按优先级别顺序查看物料 B 和 C。</span><span class="sxs-lookup"><span data-stu-id="c61d1-125">If the demand can't be covered, master planning looks at materials B and C, in order of priority.</span></span> <span data-ttu-id="c61d1-126">如果物料 B 是现有库存物料，则在为配方形成计划批次订单后会使用它。</span><span class="sxs-lookup"><span data-stu-id="c61d1-126">If material B is on hand, it will be used after a planned batch order is firmed for the formula.</span></span> <span data-ttu-id="c61d1-127">如果这些物料都不是现有库存物料，主计划会为物料 A 创建一个计划订单。**注释：**当您在计划组中设置配方行时，应仅在具有最高优先级的物料上指定数量。</span><span class="sxs-lookup"><span data-stu-id="c61d1-127">If none of the materials are on hand, master planning creates a planned order for material A. **Note:** When you set up formula lines in a plan group, you should specify a quantity only on the material that has the highest priority.</span></span> <span data-ttu-id="c61d1-128">此数量将用于计算计划中的所有物料的需求，甚至具有更低优先级的物料。</span><span class="sxs-lookup"><span data-stu-id="c61d1-128">This quantity will be used to calculate the demand of all materials in the plan, even the materials that have lower priority.</span></span> <span data-ttu-id="c61d1-129">您不能在计划组中的更低优先级物料上指定不同的数量。</span><span class="sxs-lookup"><span data-stu-id="c61d1-129">You can't specify different quantities on lower-priority items in the plan group.</span></span>

## <a name="substituting-material-during-production"></a><span data-ttu-id="c61d1-130">在生产期间替换物料</span><span class="sxs-lookup"><span data-stu-id="c61d1-130">Substituting material during production</span></span>
<span data-ttu-id="c61d1-131">请考虑以下情况：一块金属板是焊接操作所必需的。</span><span class="sxs-lookup"><span data-stu-id="c61d1-131">Consider the following scenario: A piece of metal plate is required for a welding operation.</span></span> <span data-ttu-id="c61d1-132">在操作期间，仓库工作人员通知机器操作员板子的库存不足。</span><span class="sxs-lookup"><span data-stu-id="c61d1-132">During the operation, a warehouse worker informs the machine operator that the plate is out of stock.</span></span> <span data-ttu-id="c61d1-133">但是，板子可替换为稍厚的板子是确定无疑的。</span><span class="sxs-lookup"><span data-stu-id="c61d1-133">However, it's decided that the plate can be substituted with a plate that is slightly thicker.</span></span> <span data-ttu-id="c61d1-134">这样，操作就可以完成。</span><span class="sxs-lookup"><span data-stu-id="c61d1-134">That way, the operation can be finalized.</span></span> <span data-ttu-id="c61d1-135">物料可以添加到未结生产订单的物料清单中。</span><span class="sxs-lookup"><span data-stu-id="c61d1-135">Material can be added to the BOM for an open production order.</span></span> <span data-ttu-id="c61d1-136">如果生产订单具有状态**“已开始”**，则在用户向生产物料清单中添加新物料时，系统会要求用户重新估计该订单。</span><span class="sxs-lookup"><span data-stu-id="c61d1-136">If the production order has a status of **Started**, users are asked to re-estimate the order when they add a new item to the production BOM.</span></span> <span data-ttu-id="c61d1-137">在添加物料后，可以为新物料创建新的领料单。</span><span class="sxs-lookup"><span data-stu-id="c61d1-137">After the material is added, a new picking list can be created for the new item.</span></span> <span data-ttu-id="c61d1-138">您不必向生产物料清单中添加新的物料。</span><span class="sxs-lookup"><span data-stu-id="c61d1-138">You don't have to add the new material to the production BOM.</span></span> <span data-ttu-id="c61d1-139">相反，您可以直接将其添加到生产领料单。</span><span class="sxs-lookup"><span data-stu-id="c61d1-139">Instead, you can add it directly to the production picking list.</span></span> <span data-ttu-id="c61d1-140">然后，当过帐领料单时，系统会将物料添加到生产物料清单中。</span><span class="sxs-lookup"><span data-stu-id="c61d1-140">Then, when the picking list is posted, the system adds the material to the production BOM.</span></span>





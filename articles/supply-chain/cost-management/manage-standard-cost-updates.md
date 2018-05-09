---
title: "管理标准成本更新"
description: "可以使用两种不同的方法管理对标准成本数据的更新 - 单版本方法或双版本方法。"
author: AndersGirke
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3e1d9831b84af96d34150544c660d59f9c720539
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="manage-standard-cost-updates"></a><span data-ttu-id="8bc96-103">管理标准成本更新</span><span class="sxs-lookup"><span data-stu-id="8bc96-103">Manage standard cost updates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8bc96-104">可以使用两种不同的方法管理对标准成本数据的更新 - 单版本方法或双版本方法。</span><span class="sxs-lookup"><span data-stu-id="8bc96-104">Updates to standard cost data can be managed by using two different approaches - the one-version approach or the two-version approach.</span></span> 

<span data-ttu-id="8bc96-105">单版本方法使用包含所有成本记录的单个成本计算版本。</span><span class="sxs-lookup"><span data-stu-id="8bc96-105">The one-version approach uses a single costing version that contains all cost records.</span></span> <span data-ttu-id="8bc96-106">这些记录包括原始成本和所有成本更新。</span><span class="sxs-lookup"><span data-stu-id="8bc96-106">These records include the original costs and all cost updates.</span></span>

<span data-ttu-id="8bc96-107">双版本方法使用包含原始成本记录的一个版本，以及包含所有成本更新记录的第二个版本。</span><span class="sxs-lookup"><span data-stu-id="8bc96-107">The two-version approach uses one version that contains records of the original costs and a second version that contains records of all cost updates.</span></span> <span data-ttu-id="8bc96-108">双版本方法的主要优点是清晰地描述以及跟踪单独的成本计算版本中的成本更新，同时不影响原始成本计算版本。</span><span class="sxs-lookup"><span data-stu-id="8bc96-108">A primary advantage of the two-version approach is the clear delineation and tracking of cost updates in a separate costing version, without affecting the original costing version.</span></span> <span data-ttu-id="8bc96-109">双版本方法来标识倍数增量更新，一次增量更新具有单独的成本计算版本来包含增量成本记录。</span><span class="sxs-lookup"><span data-stu-id="8bc96-109">The two-version approach can be used to identify multiple incremental updates, where each incremental update has a separate costing version that contains the incremental cost records.</span></span> 

<span data-ttu-id="8bc96-110">**示例**</span><span class="sxs-lookup"><span data-stu-id="8bc96-110">**Example**</span></span> 

<span data-ttu-id="8bc96-111">以下示例阐释了如何将单版本方法和双版本方法用于更新制造环境中的标准成本。</span><span class="sxs-lookup"><span data-stu-id="8bc96-111">The following example illustrates how the one-version and two-version approaches can be used for updating standard costs in a manufacturing environment.</span></span> <span data-ttu-id="8bc96-112">例如，反应新物料或错误更正的更新。</span><span class="sxs-lookup"><span data-stu-id="8bc96-112">For example, updates that reflect new items or error corrections.</span></span> <span data-ttu-id="8bc96-113">假定单个成本计算版本表示了当年的标准成本。</span><span class="sxs-lookup"><span data-stu-id="8bc96-113">Assume that a single costing version represents the standard costs for the current year.</span></span> <span data-ttu-id="8bc96-114">此版本的标识符是 2016-STD。</span><span class="sxs-lookup"><span data-stu-id="8bc96-114">The identifier for this version is 2016-STD.</span></span> <span data-ttu-id="8bc96-115">版本 2016-STD 包含了所有物料的当前有效成本。</span><span class="sxs-lookup"><span data-stu-id="8bc96-115">Version 2016-STD contains the current active costs for all items.</span></span> <span data-ttu-id="8bc96-116">此外，它包含在 2016 年初已知的所有工艺路线相关的成本类别和开销计算公式。</span><span class="sxs-lookup"><span data-stu-id="8bc96-116">Additionally, it contains all routing-related cost categories and overhead calculation formulas that were known at the start of the year 2016.</span></span> <span data-ttu-id="8bc96-117">2016-STD 是原始成本计算版本。</span><span class="sxs-lookup"><span data-stu-id="8bc96-117">2016-STD is the original costing version.</span></span>

-   <span data-ttu-id="8bc96-118">**“用于成本数据更新的单版本方法”** − 在单版本方法中，原始成本计算版本 2016-STD 包含了所有成本记录。</span><span class="sxs-lookup"><span data-stu-id="8bc96-118">**One-version approach to cost data updates** − In the one-version approach, the original costing version 2016-STD contains all cost records.</span></span> <span data-ttu-id="8bc96-119">成本更新将在 2016-STD 中记录并设置为“未决”状态。</span><span class="sxs-lookup"><span data-stu-id="8bc96-119">Cost updates are recorded in 2016-STD and are set to a status of ”Pending.”</span></span> <span data-ttu-id="8bc96-120">可以手动为新的采购物料输入未决成本，或者，可为制造物料计算它们以反映更正。</span><span class="sxs-lookup"><span data-stu-id="8bc96-120">The pending costs can be manually entered for new purchased items, or they can be calculated for a manufactured item to reflect corrections.</span></span> <span data-ttu-id="8bc96-121">当使用单版本方法时，BOM 计算不需要回退数据源，因为在该成本计算版本中包含了所有有效成本。</span><span class="sxs-lookup"><span data-stu-id="8bc96-121">When the one-version approach is used, the BOM calculations do not require a fallback data source because all active costs are contained in the costing version.</span></span> <span data-ttu-id="8bc96-122">在未决成本变得有效后，原始成本计算版本 2016-STD 将再次包含所有当前有效成本。</span><span class="sxs-lookup"><span data-stu-id="8bc96-122">After the pending costs become active, the original costing version 2016-STD will again contain all the current active costs.</span></span>
-   <span data-ttu-id="8bc96-123">**“用于成本数据更新的双版本方法”** − 双版本方法需要一个只包含成本更新的附加成本计算版本。</span><span class="sxs-lookup"><span data-stu-id="8bc96-123">**Two-version approach to cost data updates** − The two-version approach requires an additional costing version that contains only the cost updates.</span></span> <span data-ttu-id="8bc96-124">此版本的标识符是 2016-STD-CHANGES。</span><span class="sxs-lookup"><span data-stu-id="8bc96-124">The identifier for this version is 2016-STD-CHANGES.</span></span> <span data-ttu-id="8bc96-125">成本更新记录在 2016-STD-CHANGES 中，并将设置为“未决”状态。</span><span class="sxs-lookup"><span data-stu-id="8bc96-125">Cost updates are recorded in 2016-STD-CHANGES and are set to a status of “Pending.”</span></span> <span data-ttu-id="8bc96-126">使用双版本方法，针对已制造物料的未决成本的 BOM 计算需要回退数据源。</span><span class="sxs-lookup"><span data-stu-id="8bc96-126">With the two-version approach, the BOM calculations of pending costs for manufactured items require a fallback data source.</span></span> <span data-ttu-id="8bc96-127">这是因为附加的成本计算版本 2016-STD-CHANGES 只包含了成本数据的子集。</span><span class="sxs-lookup"><span data-stu-id="8bc96-127">This is because the additional costing version 2016-STD-CHANGES contains only a subset of cost data.</span></span> <span data-ttu-id="8bc96-128">该回退可以表示为有效成本或成本计算版本 2016-STD，因为当它未包括在 2016-STD-CHANGES 中时，有效成本和成本计算版本 2016-STD 都标识了成本数据的来源。</span><span class="sxs-lookup"><span data-stu-id="8bc96-128">The fallback can be expressed as the active costs or as the costing version 2016-STD, because both identify the source of cost data when it is not included in 2016-STD-CHANGES.</span></span> <span data-ttu-id="8bc96-129">在未决成本变得有效后，附加的成本计算版本 2016-STD-CHANGES 将包含反映这些更新的当前有效的成本，而原始成本计算版本 2016-STD 将不改变。</span><span class="sxs-lookup"><span data-stu-id="8bc96-129">After the pending costs become active, the costing version 2016-STD-CHANGES will contain the current active costs that reflect the updates, whereas the original costing version 2016-STD will be untouched.</span></span> <span data-ttu-id="8bc96-130">当使用双版本方法时，应该针对原始成本计算版本设置锁定策略以阻止更新。</span><span class="sxs-lookup"><span data-stu-id="8bc96-130">When the two-version approach is used, blocking policies for the original costing version should be set up to prevent updates.</span></span> <span data-ttu-id="8bc96-131">应该为附加成本计算版本设置相同的锁定策略，除了锁定策略的开始数据和选择性使用，以允许更新。</span><span class="sxs-lookup"><span data-stu-id="8bc96-131">Identical blocking policies should be set up for the additional costing version, except for the specified from-date and the selective use of blocking policies to allow for updates.</span></span> <span data-ttu-id="8bc96-132">指定的开始日期应该用每个更改批处理进行更新，以便反映计划的激活日期。</span><span class="sxs-lookup"><span data-stu-id="8bc96-132">The specified from-date should be updated with each batch of changes to reflect the scheduled activation date.</span></span>

<span data-ttu-id="8bc96-133">此示例使用了一个附加成本计算版本来管理整个 2016 年的更新。</span><span class="sxs-lookup"><span data-stu-id="8bc96-133">This example used one additional costing version for managing updates throughout the year 2016.</span></span> <span data-ttu-id="8bc96-134">可以使用更多的成本计算版本，例如使用单独的版本来用于各个更新批处理。</span><span class="sxs-lookup"><span data-stu-id="8bc96-134">More than one additional costing version can be used, such as a separate version for each batch of updates.</span></span> <span data-ttu-id="8bc96-135">当使用了多个附加成本计算时，必须用有效成本表示回调，因为有效成本分散在多个成本计算版本中。</span><span class="sxs-lookup"><span data-stu-id="8bc96-135">When more than one additional costing is used, the fallback must be expressed as the active costs, because the active costs are spread over multiple costing versions.</span></span>







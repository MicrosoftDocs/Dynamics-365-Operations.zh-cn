---
title: 计划优化拟合分析
description: 本主题说明如何根据计划优化功能的能力来验证当前的设置和数据。
author: ChristianRytt
manager: AnnBe
ms.date: 1030/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 26b067f8526df16474c0ab52d0abf816170ff5cb
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773910"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="a06db-103">计划优化拟合分析</span><span class="sxs-lookup"><span data-stu-id="a06db-103">Planning Optimization fit analysis</span></span>

<span data-ttu-id="a06db-104">要查看您当前的设置和数据与计划优化功能之间的兼容性，请转到**主计划** \> **设置** \> **计划优化拟合分析**，然后选择**运行分析**。</span><span class="sxs-lookup"><span data-stu-id="a06db-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="a06db-105">如果分析发现任何不一致之处，则会在同一页面上列出。</span><span class="sxs-lookup"><span data-stu-id="a06db-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="a06db-106">（分析可能需要几分钟运行。）</span><span class="sxs-lookup"><span data-stu-id="a06db-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="a06db-107">如果发现不一致，您仍然可以使用计划优化。</span><span class="sxs-lookup"><span data-stu-id="a06db-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="a06db-108">拟合分析的结果仅显示计划服务不支持您当前设置的地方。</span><span class="sxs-lookup"><span data-stu-id="a06db-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="a06db-109">换言之，它们显示某些流程可能被忽略或不被支持的地方。</span><span class="sxs-lookup"><span data-stu-id="a06db-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="a06db-110">分析结果：示例 1</span><span class="sxs-lookup"><span data-stu-id="a06db-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="a06db-111">**功能：** 生产</span><span class="sxs-lookup"><span data-stu-id="a06db-111">**Feature:** Production</span></span>
- <span data-ttu-id="a06db-112">**问题：** BOM 级别大于零的物料：56</span><span class="sxs-lookup"><span data-stu-id="a06db-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="a06db-113">**说明：** 拟合分析发现有 56 个物料的物料清单 (BOM) 设置用于生产。</span><span class="sxs-lookup"><span data-stu-id="a06db-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="a06db-114">由于当前版本的计划优化不支持生产，因此计划优化将生成计划采购订单，而不是计划生产订单。</span><span class="sxs-lookup"><span data-stu-id="a06db-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="a06db-115">它还将显示警告，列出受影响的物料。</span><span class="sxs-lookup"><span data-stu-id="a06db-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="a06db-116">分析结果：示例 2</span><span class="sxs-lookup"><span data-stu-id="a06db-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="a06db-117">**功能：** 操作</span><span class="sxs-lookup"><span data-stu-id="a06db-117">**Feature:** Actions</span></span>
- <span data-ttu-id="a06db-118">**问题：** 启用了操作计算的覆盖范围组：6</span><span class="sxs-lookup"><span data-stu-id="a06db-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="a06db-119">**说明：** 拟合分析发现了六个启用了操作计算的覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="a06db-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="a06db-120">由于当前版本的计划优化不支持操作，因此在主计划期间将不会生成任何操作。</span><span class="sxs-lookup"><span data-stu-id="a06db-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="a06db-121">相关资源</span><span class="sxs-lookup"><span data-stu-id="a06db-121">Related resources</span></span>

[<span data-ttu-id="a06db-122">计划优化概述</span><span class="sxs-lookup"><span data-stu-id="a06db-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="a06db-123">开始使用计划优化</span><span class="sxs-lookup"><span data-stu-id="a06db-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="a06db-124">查看计划历史记录和计划日志</span><span class="sxs-lookup"><span data-stu-id="a06db-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="a06db-125">将筛选器应用于计划</span><span class="sxs-lookup"><span data-stu-id="a06db-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="a06db-126">取消计划作业</span><span class="sxs-lookup"><span data-stu-id="a06db-126">Cancel a planning job</span></span>](cancel-planning-job.md)

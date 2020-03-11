---
title: 将筛选器应用于计划
description: 本主题说明使用计划优化功能时如何对计划使用筛选器。
author: ChristianRytt
manager: AnnBe
ms.date: 01/08/2020
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
ms.openlocfilehash: ca28953846b4f1978a453d2ab2aa9759e4f45221
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076101"
---
# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="3a3c2-103">将筛选器应用于计划</span><span class="sxs-lookup"><span data-stu-id="3a3c2-103">Apply filters to a plan</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3a3c2-104">使用计划优化功能时，可以将筛选器应用于计划。</span><span class="sxs-lookup"><span data-stu-id="3a3c2-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="3a3c2-105">**计划筛选器**将始终在主计划运行期间应用。</span><span class="sxs-lookup"><span data-stu-id="3a3c2-105">The **Plan filter** will always be applied during a master planning run.</span></span> <span data-ttu-id="3a3c2-106">当您要将计划限制为特定的项目组并确保没有其他项目作为生成的主计划的一部分包含时，**计划筛选器**很有用。</span><span class="sxs-lookup"><span data-stu-id="3a3c2-106">A **Plan filter** is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="3a3c2-107">如果应用了**计划筛选器**，并且在主计划运行期间也应用了运行时筛选器，则计划运行中仅包括两个筛选器的交集。</span><span class="sxs-lookup"><span data-stu-id="3a3c2-107">If a **Plan filter** is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

<span data-ttu-id="3a3c2-108">使用计划优化时，可以从**主计划**访问**计划筛选器**。</span><span class="sxs-lookup"><span data-stu-id="3a3c2-108">The **Plan filter** can be accessed from **Master plans** when Planning Optimization is used.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="3a3c2-109">示例场景</span><span class="sxs-lookup"><span data-stu-id="3a3c2-109">Example scenario</span></span>

<span data-ttu-id="3a3c2-110">设置了一个包含项目 A、B 和 C 的计划筛选器。然后为同一计划运行主计划运行，但是应用了不同的运行时筛选器：</span><span class="sxs-lookup"><span data-stu-id="3a3c2-110">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="3a3c2-111">**包含项目 D 的运行时筛选器：** 未计划项目，因为计划筛选器和运行时筛选器之间没有交集。</span><span class="sxs-lookup"><span data-stu-id="3a3c2-111">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="3a3c2-112">**包含项目 A 和 D 的运行时筛选器：** 在计划运行中仅包含项目 A，因为项目 D 不是计划筛选器的一部分。</span><span class="sxs-lookup"><span data-stu-id="3a3c2-112">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="3a3c2-113">**包含物料 B 的运行时筛选器：** 在计划运行中仅包含物料 B，保留物料 A 的先前计划输出。</span><span class="sxs-lookup"><span data-stu-id="3a3c2-113">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="3a3c2-114">**包含所有物料的运行时筛选器（空筛选器）：** 计划运行中包含物料 A、B 和 C，物料 A 和 B 的先前计划输出将被覆盖。</span><span class="sxs-lookup"><span data-stu-id="3a3c2-114">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="3a3c2-115">您应该避免在**主计划参数**页面上被选为**当前动态主计划**的计划上设置计划筛选器。</span><span class="sxs-lookup"><span data-stu-id="3a3c2-115">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="3a3c2-116">否则，动态主计划功能将仅限于筛选后的物料。</span><span class="sxs-lookup"><span data-stu-id="3a3c2-116">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="3a3c2-117">例如，如果针对不是计划筛选器一部分的物料更新了净需求，则不会生成结果。</span><span class="sxs-lookup"><span data-stu-id="3a3c2-117">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="3a3c2-118">相关资源</span><span class="sxs-lookup"><span data-stu-id="3a3c2-118">Related resources</span></span>

[<span data-ttu-id="3a3c2-119">计划优化概述</span><span class="sxs-lookup"><span data-stu-id="3a3c2-119">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="3a3c2-120">开始使用计划优化</span><span class="sxs-lookup"><span data-stu-id="3a3c2-120">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="3a3c2-121">计划优化拟合分析</span><span class="sxs-lookup"><span data-stu-id="3a3c2-121">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="3a3c2-122">查看计划历史记录和计划日志</span><span class="sxs-lookup"><span data-stu-id="3a3c2-122">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="3a3c2-123">取消计划作业</span><span class="sxs-lookup"><span data-stu-id="3a3c2-123">Cancel a planning job</span></span>](cancel-planning-job.md)

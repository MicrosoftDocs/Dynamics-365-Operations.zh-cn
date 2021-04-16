---
title: 计划优化概述
description: 本主题提供计划优化功能的概述。
author: ChristianRytt
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 5ecfa8ac4db050ee1e38f3b420d81beba19b9409
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812947"
---
# <a name="planning-optimization-overview"></a><span data-ttu-id="5b891-103">计划优化概述</span><span class="sxs-lookup"><span data-stu-id="5b891-103">Planning Optimization overview</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b891-104">Microsoft Dynamics 365 Supply Chain Management 的计划优化加载项使主计划计算可以在 Dynamics 365 Supply Chain Management 和相关的 SQL 数据库之外进行。</span><span class="sxs-lookup"><span data-stu-id="5b891-104">The Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management enables master planning calculation to occur outside Dynamics 365 Supply Chain Management and the related SQL database.</span></span> <span data-ttu-id="5b891-105">与计划优化功能相关的好处包括在主计划运行期间改进的性能以及对 SQL 数据库的影响最小。</span><span class="sxs-lookup"><span data-stu-id="5b891-105">The benefits that are associated with the Planning Optimization functionality include improved performance and minimal impact on SQL database during master planning runs.</span></span> <span data-ttu-id="5b891-106">即使在工作时间内也可以进行快速的计划运行，因此规划员可以立即对需求或参数更改做出反应。</span><span class="sxs-lookup"><span data-stu-id="5b891-106">Quick planning runs can be done even during office hours, so that planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="5b891-107">若要使用计划优化，必须从 Microsoft Dynamics Lifecycle Services (LCS) 中的项目安装计划优化加载项，并在 Supply Chain Management 中启用计划优化功能。</span><span class="sxs-lookup"><span data-stu-id="5b891-107">To use Planning Optimization, you must install the Planning Optimization Add-in from your project in Microsoft Dynamics Lifecycle Services (LCS) and turn on the Planning Optimization functionality in Supply Chain Management.</span></span> <span data-ttu-id="5b891-108">有关详细信息，请参阅[开始使用计划优化](get-started.md)。</span><span class="sxs-lookup"><span data-stu-id="5b891-108">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="5b891-109">下图显示了在工作时间内运行计划优化的好处。</span><span class="sxs-lookup"><span data-stu-id="5b891-109">The following illustration shows the advantage of running Planning Optimization during office hours.</span></span>

![在工作时间内运行计划优化的好处](media/PlanningOptimization1.png)

## <a name="improved-performance"></a><span data-ttu-id="5b891-111">性能提升</span><span class="sxs-lookup"><span data-stu-id="5b891-111">Improved performance</span></span>

<span data-ttu-id="5b891-112">计划优化可用于涉及长期运行的主计划的场景。</span><span class="sxs-lookup"><span data-stu-id="5b891-112">Planning Optimization can be used in scenarios that involve long-running master plans.</span></span> <span data-ttu-id="5b891-113">它是专门为涉及大量数据的快速计算而设计的。</span><span class="sxs-lookup"><span data-stu-id="5b891-113">It's specifically designed for very fast calculations that involve very large volumes of data.</span></span> <span data-ttu-id="5b891-114">由于它是作为超级可扩展的多租户服务构建的，因此多个实例可以同时协同工作来计算计划。</span><span class="sxs-lookup"><span data-stu-id="5b891-114">Because it's built as a hyper-scalable multitenant service, multiple instances can work together simultaneously to calculate the plan.</span></span> <span data-ttu-id="5b891-115">此外，计划服务还可以从系统中删除主计划的负荷，并使用可最大程度减少服务器负荷的数据流。</span><span class="sxs-lookup"><span data-stu-id="5b891-115">Additionally, the planning service removes the load of master planning from your system and works with a data stream that minimizes the server load.</span></span>

<span data-ttu-id="5b891-116">计划优化可以帮助您实现以下目标：</span><span class="sxs-lookup"><span data-stu-id="5b891-116">Planning Optimization can help you achieve the following goals:</span></span>

- <span data-ttu-id="5b891-117">通过缩短运行时间来提高计划性能。</span><span class="sxs-lookup"><span data-stu-id="5b891-117">Improve planning performance through a shorter runtime.</span></span>
- <span data-ttu-id="5b891-118">减少主计划运行期间对其他流程的影响。</span><span class="sxs-lookup"><span data-stu-id="5b891-118">Reduce the impact on other processes during the master planning run.</span></span>
- <span data-ttu-id="5b891-119">进行更频繁的计划运行。</span><span class="sxs-lookup"><span data-stu-id="5b891-119">Do more frequent planning runs.</span></span> <span data-ttu-id="5b891-120">（不限于日常运行。）</span><span class="sxs-lookup"><span data-stu-id="5b891-120">(You aren't limited to daily runs.)</span></span>
- <span data-ttu-id="5b891-121">放心未来的业务增长不会使计划系统超负荷。</span><span class="sxs-lookup"><span data-stu-id="5b891-121">Be confident that future business growth won't overload the planning system.</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="5b891-122">体系结构和数据流</span><span class="sxs-lookup"><span data-stu-id="5b891-122">Architecture and data flow</span></span>

<span data-ttu-id="5b891-123">从 LCS 安装计划优化加载项后，将建立到计划优化服务的安全连接。</span><span class="sxs-lookup"><span data-stu-id="5b891-123">When the Planning Optimization Add-in is installed from LCS, a secure connection to the Planning Optimization service is established.</span></span> <span data-ttu-id="5b891-124">服务与相关的 Supply Chain Management 实例位于相同的数据中心国家或地区。</span><span class="sxs-lookup"><span data-stu-id="5b891-124">The service is located in the same data center country or region as the related Supply Chain Management instance.</span></span> <span data-ttu-id="5b891-125">设置计划优化后，运行主计划时，主数据和交易记录数据将从 Supply Chain Management 发送到计划优化服务。</span><span class="sxs-lookup"><span data-stu-id="5b891-125">After Planning Optimization is set up, when master planning is run, master data and transactional data are sent from Supply Chain Management to the Planning Optimization service.</span></span>

<span data-ttu-id="5b891-126">如果卸载了计划优化加载项，则会删除计划优化服务中的所有相关数据。</span><span class="sxs-lookup"><span data-stu-id="5b891-126">If the Planning Optimization Add-in is uninstalled, all related data in the Planning Optimization service is removed.</span></span>

### <a name="high-level-data-flow-for-regeneration-runs"></a><span data-ttu-id="5b891-127">用于重新生成运行的高级数据流</span><span class="sxs-lookup"><span data-stu-id="5b891-127">High-level data flow for regeneration runs</span></span>

1. <span data-ttu-id="5b891-128">Supply Chain Management 客户端发送信号从“计划优化”请求计划运行。</span><span class="sxs-lookup"><span data-stu-id="5b891-128">The Supply Chain Management client sends a signal to request a planning run from Planning Optimization.</span></span>
2. <span data-ttu-id="5b891-129">“计划优化”通过集成的连接器请求所需的数据。</span><span class="sxs-lookup"><span data-stu-id="5b891-129">Planning Optimization requests the required data via the integrated connector.</span></span>
3. <span data-ttu-id="5b891-130">SQL 数据库通过连接器将请求的有关设置、主数据和交易记录数据的信息发送到“计划优化”。</span><span class="sxs-lookup"><span data-stu-id="5b891-130">The SQL database sends the requested information about setup, master, and transactional data to Planning Optimization via the connector.</span></span> <span data-ttu-id="5b891-131">连接器在 Supply Chain Management 和计划优化服务之间转换信息。</span><span class="sxs-lookup"><span data-stu-id="5b891-131">The connector translates information between Supply Chain Management and the Planning Optimization service.</span></span>
4. <span data-ttu-id="5b891-132">计划优化服务将与计划相关的数据保存在内存中，并进行所需的计算。</span><span class="sxs-lookup"><span data-stu-id="5b891-132">The Planning Optimization service holds planning-related data in memory and does the required calculations.</span></span>
5. <span data-ttu-id="5b891-133">计划结果通过连接器发送到 Supply Chain Management 数据库。</span><span class="sxs-lookup"><span data-stu-id="5b891-133">The planning result is sent to the Supply Chain Management database via the connector.</span></span> <span data-ttu-id="5b891-134">结果包括计划订单和限定标准信息等信息。</span><span class="sxs-lookup"><span data-stu-id="5b891-134">The results include information such as planned orders and pegging information.</span></span> <span data-ttu-id="5b891-135">“计划优化”向 Supply Chain Management 发送信号，指示计划运行已完成。</span><span class="sxs-lookup"><span data-stu-id="5b891-135">Planning Optimization sends a signal to Supply Chain Management to indicate that the planning run has been completed.</span></span> <span data-ttu-id="5b891-136">它还发送任何相关的消息和警告。</span><span class="sxs-lookup"><span data-stu-id="5b891-136">It also sends any relevant messages and warnings.</span></span>

<span data-ttu-id="5b891-137">下图显示数据流。</span><span class="sxs-lookup"><span data-stu-id="5b891-137">The following illustration shows the data flow.</span></span>

![用于重新生成运行的数据流](media/PlanningOptimization2.png)

## <a name="related-resources"></a><span data-ttu-id="5b891-139">相关资源</span><span class="sxs-lookup"><span data-stu-id="5b891-139">Related resources</span></span>

[<span data-ttu-id="5b891-140">开始使用计划优化</span><span class="sxs-lookup"><span data-stu-id="5b891-140">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="5b891-141">计划优化拟合分析</span><span class="sxs-lookup"><span data-stu-id="5b891-141">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="5b891-142">查看计划历史记录和计划日志</span><span class="sxs-lookup"><span data-stu-id="5b891-142">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="5b891-143">将筛选器应用于计划</span><span class="sxs-lookup"><span data-stu-id="5b891-143">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="5b891-144">取消计划作业</span><span class="sxs-lookup"><span data-stu-id="5b891-144">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
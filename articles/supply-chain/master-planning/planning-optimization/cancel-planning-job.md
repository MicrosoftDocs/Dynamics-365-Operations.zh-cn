---
title: 取消计划作业
description: 本主题说明如何取消使用“计划优化”功能的活动计划作业。
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
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
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773912"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a><span data-ttu-id="3d1a8-103">取消计划作业</span><span class="sxs-lookup"><span data-stu-id="3d1a8-103">Cancel a planning job</span></span>

<span data-ttu-id="3d1a8-104">在 Microsoft Dynamics 365 Supply Chain Management 中，您可以取消使用“计划优化”功能的活动计划作业。</span><span class="sxs-lookup"><span data-stu-id="3d1a8-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning Optimization functionality.</span></span>

<span data-ttu-id="3d1a8-105">要取消活动的计划作业，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="3d1a8-105">To cancel an active planning job, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="3d1a8-106">仅活动作业可以取消。</span><span class="sxs-lookup"><span data-stu-id="3d1a8-106">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="3d1a8-107">转到**主计划 \> 设置 \> 计划**。</span><span class="sxs-lookup"><span data-stu-id="3d1a8-107">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="3d1a8-108">为计划运行选择适当的计划。</span><span class="sxs-lookup"><span data-stu-id="3d1a8-108">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="3d1a8-109">选择**历史记录**。</span><span class="sxs-lookup"><span data-stu-id="3d1a8-109">Select **History**.</span></span>
4. <span data-ttu-id="3d1a8-110">选择要取消的计划作业。</span><span class="sxs-lookup"><span data-stu-id="3d1a8-110">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="3d1a8-111">选择**取消**。</span><span class="sxs-lookup"><span data-stu-id="3d1a8-111">Select **Cancel**.</span></span>

<span data-ttu-id="3d1a8-112">作业状态将为**正在取消**，直到计划优化服务确认该作业已被取消。</span><span class="sxs-lookup"><span data-stu-id="3d1a8-112">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="3d1a8-113">然后，状态将更改为**已取消**。</span><span class="sxs-lookup"><span data-stu-id="3d1a8-113">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="3d1a8-114">要查看状态更改，您必须通过选择**刷新**按钮刷新页面。</span><span class="sxs-lookup"><span data-stu-id="3d1a8-114">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="related-resources"></a><span data-ttu-id="3d1a8-115">相关资源</span><span class="sxs-lookup"><span data-stu-id="3d1a8-115">Related resources</span></span>

[<span data-ttu-id="3d1a8-116">计划优化概述</span><span class="sxs-lookup"><span data-stu-id="3d1a8-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="3d1a8-117">开始使用计划优化</span><span class="sxs-lookup"><span data-stu-id="3d1a8-117">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="3d1a8-118">计划优化拟合分析</span><span class="sxs-lookup"><span data-stu-id="3d1a8-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="3d1a8-119">查看计划历史记录和计划日志</span><span class="sxs-lookup"><span data-stu-id="3d1a8-119">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="3d1a8-120">将筛选器应用于计划</span><span class="sxs-lookup"><span data-stu-id="3d1a8-120">Apply filters to a plan</span></span>](plan-filters.md)

---
title: 查看计划历史记录和计划日志
description: 本主题说明如何查看由计划优化功能触发的计划作业的历史记录。
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187239"
---
# <a name="view-plan-history-and-planning-logs"></a><span data-ttu-id="d2266-103">查看计划历史记录和计划日志</span><span class="sxs-lookup"><span data-stu-id="d2266-103">View plan history and planning logs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d2266-104">本主题说明如何在 Microsoft Dynamics 365 Supply Chain Management 中查看由计划优化功能触发的计划作业的历史记录。</span><span class="sxs-lookup"><span data-stu-id="d2266-104">This topic explains how to view the history of planning jobs that are triggered by the Planning Optimization functionality in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="d2266-105">要查看计划的历史记录，请依次转到 **主计划** \> **设置** \> **计划** \> **主计划** 并选择 **历史记录** 打开计划。</span><span class="sxs-lookup"><span data-stu-id="d2266-105">To view the history for a plan, open the plan by going to **Master planning** \> **Setup** \> **Plans** \> **Master plans** and selecting **History**.</span></span> <span data-ttu-id="d2266-106">历史记录列出了所选计划的所有作业。</span><span class="sxs-lookup"><span data-stu-id="d2266-106">The history lists all the jobs for the selected plan.</span></span> <span data-ttu-id="d2266-107">该列表包括已完成和活动的作业。</span><span class="sxs-lookup"><span data-stu-id="d2266-107">The list includes completed and active jobs.</span></span>

<span data-ttu-id="d2266-108">计划优化主计划运行的作业历史记录最多只能为每个主计划保留 60 条记录。</span><span class="sxs-lookup"><span data-stu-id="d2266-108">The history of jobs for Planning Optimization master planning runs keeps only up to 60 records per master plan.</span></span> <span data-ttu-id="d2266-109">每当您运行新的主计划计算时，该计划的最早历史记录都会删除。</span><span class="sxs-lookup"><span data-stu-id="d2266-109">Whenever you run a new master planning calculation, that plan's earliest history record is deleted.</span></span>

<span data-ttu-id="d2266-110">除了查看作业的开始时间和状态之外，您还可以查看特定作业的日志。</span><span class="sxs-lookup"><span data-stu-id="d2266-110">In addition to seeing the start time and status of jobs, you can view the log for a specific job.</span></span> <span data-ttu-id="d2266-111">日志包含其他信息和警告。</span><span class="sxs-lookup"><span data-stu-id="d2266-111">The log includes additional information and warnings.</span></span> <span data-ttu-id="d2266-112">并非所有作业都有日志。</span><span class="sxs-lookup"><span data-stu-id="d2266-112">Not all jobs have a log.</span></span> <span data-ttu-id="d2266-113">要查看作业的日志，请选择 **日志**。</span><span class="sxs-lookup"><span data-stu-id="d2266-113">To view the log for a job, select **Log**.</span></span> <span data-ttu-id="d2266-114">日志条目仅在作业完成之日起存储 30 天，之后它们将自动删除。</span><span class="sxs-lookup"><span data-stu-id="d2266-114">Log entries are only stored for 30 days after the date the job finished, after that they are automatically deleted.</span></span>

## <a name="related-resources"></a><span data-ttu-id="d2266-115">相关资源</span><span class="sxs-lookup"><span data-stu-id="d2266-115">Related resources</span></span>

- [<span data-ttu-id="d2266-116">计划优化概览</span><span class="sxs-lookup"><span data-stu-id="d2266-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)
- [<span data-ttu-id="d2266-117">开始使用计划优化</span><span class="sxs-lookup"><span data-stu-id="d2266-117">Get started with Planning Optimization</span></span>](get-started.md)
- [<span data-ttu-id="d2266-118">计划优化拟合分析</span><span class="sxs-lookup"><span data-stu-id="d2266-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
- [<span data-ttu-id="d2266-119">将筛选器应用于计划</span><span class="sxs-lookup"><span data-stu-id="d2266-119">Apply filters to a plan</span></span>](plan-filters.md)
- [<span data-ttu-id="d2266-120">取消计划作业</span><span class="sxs-lookup"><span data-stu-id="d2266-120">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
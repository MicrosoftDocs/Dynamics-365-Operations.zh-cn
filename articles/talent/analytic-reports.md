---
title: 使用 Attract 中的分析报表
description: 本主题介绍了 Microsoft Dynamics 365 Talent - Attract 中招聘流程见解的分析报表
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: 081988e8b8cfe1e2ddb533247b678ba38a07f5f1
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092215"
---
# <a name="use-analytic-reports-in-attract"></a><span data-ttu-id="df49c-103">使用 Attract 中的分析报表</span><span class="sxs-lookup"><span data-stu-id="df49c-103">Use analytic reports in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="df49c-104">Microsoft Dynamics 365 Talent: Attract 中的分析报表提供现成的 (OOTB) 解决方案以获取招聘流程见解。</span><span class="sxs-lookup"><span data-stu-id="df49c-104">Analytic reports in Microsoft Dynamics 365 Talent: Attract provide an out-of-the-box (OOTB) solution for hiring process insights.</span></span> <span data-ttu-id="df49c-105">可用功能包括：</span><span class="sxs-lookup"><span data-stu-id="df49c-105">Availabe features include:</span></span>

- <span data-ttu-id="df49c-106">**工作分析：** 单击工作类的**分析**选项卡可查看该工作的申请人的指标。</span><span class="sxs-lookup"><span data-stu-id="df49c-106">**Job analytics:** Click the **Analytics** tab within a job for metrics on the job's applicants.</span></span>
- <span data-ttu-id="df49c-107">**分析中心：** 单击左侧导航中的**分析**可查看工作的聚合指标。</span><span class="sxs-lookup"><span data-stu-id="df49c-107">**Analytics hub:** Click **Analytics** on the left navigation for aggregated metrics across jobs.</span></span>
- <span data-ttu-id="df49c-108">**用户特定安全性：** 对报表的访问由 Attract [角色](security-attract.md) 和工作参与者角色控制。</span><span class="sxs-lookup"><span data-stu-id="df49c-108">**User-specific security:** Access to reports is controlled by Attract [role](security-attract.md) and job participant role.</span></span>
- <span data-ttu-id="df49c-109">**交叉筛选：** 单击报表内的视觉对象可查看按所选数据筛选的其他指标。</span><span class="sxs-lookup"><span data-stu-id="df49c-109">**Cross-filtering:** Click visuals within a report to view other metrics filtered by selected data.</span></span>

>[!NOTE] 
>- <span data-ttu-id="df49c-110">此功能现在处于[预览](access-preview-feature.md)阶段。</span><span class="sxs-lookup"><span data-stu-id="df49c-110">This feature is currently in [preview](access-preview-feature.md).</span></span> <span data-ttu-id="df49c-111">若要尝试，必须安装[**综合招聘加载项**](attract-comprehensive-hiring.md)。</span><span class="sxs-lookup"><span data-stu-id="df49c-111">To try it, you must have the [**Comprehensive Hiring Add-On**](attract-comprehensive-hiring.md).</span></span>
>- <span data-ttu-id="df49c-112">所有公共预览报表均以英语显示。</span><span class="sxs-lookup"><span data-stu-id="df49c-112">All public preview reports are displayed in English.</span></span>
>- <span data-ttu-id="df49c-113">报表每隔 3 小时刷新。</span><span class="sxs-lookup"><span data-stu-id="df49c-113">Reports refresh every 3 hours.</span></span> <span data-ttu-id="df49c-114">上次刷新时间（本地时区内）位于报表顶部。</span><span class="sxs-lookup"><span data-stu-id="df49c-114">The last refresh time (in the local timezone) is located at the top of the report.</span></span> <span data-ttu-id="df49c-115">刷新次数为近似值，由数据量和您所在地区的资源负荷决定。</span><span class="sxs-lookup"><span data-stu-id="df49c-115">Refresh times are an approximation and vary based on data volume and resource load in your region.</span></span>

## <a name="job-analytics"></a><span data-ttu-id="df49c-116">工作分析</span><span class="sxs-lookup"><span data-stu-id="df49c-116">Job Analytics</span></span>

<span data-ttu-id="df49c-117">工作分析报表提供工作招聘流程的快照。</span><span class="sxs-lookup"><span data-stu-id="df49c-117">Job Analytics reports are a snapshot of the hiring process for a job.</span></span>  <span data-ttu-id="df49c-118">关键指标包括：</span><span class="sxs-lookup"><span data-stu-id="df49c-118">Key metrics include:</span></span>

- <span data-ttu-id="df49c-119">有效申请人（按阶段）</span><span class="sxs-lookup"><span data-stu-id="df49c-119">Active applicants by stage</span></span>
- <span data-ttu-id="df49c-120">申请人来源</span><span class="sxs-lookup"><span data-stu-id="df49c-120">Applicant source</span></span>
- <span data-ttu-id="df49c-121">申请人类型（内部或外部）</span><span class="sxs-lookup"><span data-stu-id="df49c-121">Applicant type (internal or external)</span></span>

## <a name="analytics-hub"></a><span data-ttu-id="df49c-122">分析中心</span><span class="sxs-lookup"><span data-stu-id="df49c-122">Analytics Hub</span></span>

<span data-ttu-id="df49c-123">分析中心报表聚合工作数据以展示招聘流程的趋势。</span><span class="sxs-lookup"><span data-stu-id="df49c-123">Analytics Hub reports aggregate data across jobs to surface trends in the hiring process.</span></span> <span data-ttu-id="df49c-124">Attract 中包含两种 OOTB 报表：管道汇总和漏斗图分析。</span><span class="sxs-lookup"><span data-stu-id="df49c-124">Attract includes two OOTB reports: Pipeline Summary and Funnel Analysis.</span></span>

### <a name="pipeline-summary"></a><span data-ttu-id="df49c-125">管道汇总</span><span class="sxs-lookup"><span data-stu-id="df49c-125">Pipeline Summary</span></span>

<span data-ttu-id="df49c-126">管道汇总报表聚合开放工作的数据。</span><span class="sxs-lookup"><span data-stu-id="df49c-126">The Pipeline Summary report aggregates data for open jobs.</span></span> <span data-ttu-id="df49c-127">关键指标包括：</span><span class="sxs-lookup"><span data-stu-id="df49c-127">Key metrics include:</span></span>

- <span data-ttu-id="df49c-128">所有工作的申请人（按阶段）</span><span class="sxs-lookup"><span data-stu-id="df49c-128">Applicants across all jobs by stage</span></span>
- <span data-ttu-id="df49c-129">申请人来源</span><span class="sxs-lookup"><span data-stu-id="df49c-129">Applicant source</span></span>
- <span data-ttu-id="df49c-130">开放工作（按资历级别）</span><span class="sxs-lookup"><span data-stu-id="df49c-130">Open jobs by seniority level</span></span>

### <a name="funnel-analysis"></a><span data-ttu-id="df49c-131">漏斗图分析</span><span class="sxs-lookup"><span data-stu-id="df49c-131">Funnel Analysis</span></span>

<span data-ttu-id="df49c-132">漏斗图分析报表聚合已作为已填充而关闭的工作的数据。</span><span class="sxs-lookup"><span data-stu-id="df49c-132">The Funnel Analysis report aggregates data for jobs that have been closed as filled.</span></span> <span data-ttu-id="df49c-133">关键指标包括：</span><span class="sxs-lookup"><span data-stu-id="df49c-133">Key metrics include:</span></span>

- <span data-ttu-id="df49c-134">聘用时间</span><span class="sxs-lookup"><span data-stu-id="df49c-134">Time to hire</span></span>
- <span data-ttu-id="df49c-135">转换指标（不确定）</span><span class="sxs-lookup"><span data-stu-id="df49c-135">Conversion metrics (on hover)</span></span>
- <span data-ttu-id="df49c-136">聘约接受率</span><span class="sxs-lookup"><span data-stu-id="df49c-136">Offer acceptance rate</span></span>

<span data-ttu-id="df49c-137">注意：若需最精确的聘用时间报告，建议使用[聘约管理](offer-setup.md)，这是一项综合招聘加载项的一项功能。</span><span class="sxs-lookup"><span data-stu-id="df49c-137">Note: For the most accurate time to hire reporting, it is recommended that you use [Offer management](offer-setup.md), a feature available as part of the Comprehensive Hiring Add-On.</span></span>

>[!TIP] 
><span data-ttu-id="df49c-138">可尝试将光标悬停在视觉对象上方以查看更多信息。</span><span class="sxs-lookup"><span data-stu-id="df49c-138">Try hovering over visuals for additional information.</span></span> <span data-ttu-id="df49c-139">例如，将光标悬停在**有效的申请人**视觉对象上方将显示平均阶段天数。</span><span class="sxs-lookup"><span data-stu-id="df49c-139">For example, hovering over **Active applicants** visuals will display the average days in stage.</span></span> <span data-ttu-id="df49c-140">分析此信息可提供对减少招聘时间至关重要的见解，并让招聘人员重点关注减少各阶段所用时间的方法。</span><span class="sxs-lookup"><span data-stu-id="df49c-140">Analyzing this information can provide insights critical to reducing time to hire and enable recruiters to focus on ways to reduce the time spent in each stage.</span></span>

## <a name="user-specific-security"></a><span data-ttu-id="df49c-141">用户特定安全性</span><span class="sxs-lookup"><span data-stu-id="df49c-141">User-specific security</span></span>

<span data-ttu-id="df49c-142">Attract 报表可供管理员、全部阅读、招聘人员和招聘经理[角色](security-attract.md)访问。</span><span class="sxs-lookup"><span data-stu-id="df49c-142">Attract reports are accessible for Admin, Read All, Recruiter, and Hiring Manager [roles](security-attract.md).</span></span> <span data-ttu-id="df49c-143">未分配的用户不能访问分析报表页面（工作分析或分析中心）。</span><span class="sxs-lookup"><span data-stu-id="df49c-143">Unassigned users do not have access to either of the analytic report pages (Job Analytics or Analytics Hub).</span></span>

<span data-ttu-id="df49c-144">工作分析报表显示所选工作的数据。</span><span class="sxs-lookup"><span data-stu-id="df49c-144">Job Analytics reports display data for the selected job.</span></span> <span data-ttu-id="df49c-145">分析中心报表聚合用户可查看的所有工作的数据。</span><span class="sxs-lookup"><span data-stu-id="df49c-145">Analytics Hub reports aggregate data across all jobs a user can view.</span></span> <span data-ttu-id="df49c-146">可查看“工作”页面上的“我的工作”和“所有工作”的用户在分析中心内的可用视图相同。</span><span class="sxs-lookup"><span data-stu-id="df49c-146">Users that can view both My jobs and All jobs on the Jobs page have the same views available in the Analytics Hub.</span></span>

## <a name="cross-filter"></a><span data-ttu-id="df49c-147">交叉筛选</span><span class="sxs-lookup"><span data-stu-id="df49c-147">Cross-filter</span></span>

<span data-ttu-id="df49c-148">Power BI 其中一项重要功能是报表页面中的所有视觉对象的互连方式。</span><span class="sxs-lookup"><span data-stu-id="df49c-148">One of the great features of Power BI is the way all visuals on a report page are interconnected.</span></span> <span data-ttu-id="df49c-149">如果选择其中一个视觉对象上的数据点，页面中包含该数据的其他所有视觉对象将根据所选内容变化。</span><span class="sxs-lookup"><span data-stu-id="df49c-149">If you select a data point on one of the visuals, all the other visuals on the page that contain that data change, based on that selection.</span></span> <span data-ttu-id="df49c-150">有关详细信息及示例，请参阅 [Power BI 报告中视觉对象如何相互交叉筛选](https://docs.microsoft.com/power-bi/consumer/end-user-interactions)。</span><span class="sxs-lookup"><span data-stu-id="df49c-150">Find out more and see an example in [How visuals cross-filter each other in a Power BI report](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span></span>

## <a name="export-to-excel"></a><span data-ttu-id="df49c-151">导出至 Excel</span><span class="sxs-lookup"><span data-stu-id="df49c-151">Export to Excel</span></span>

<span data-ttu-id="df49c-152">若要使用 Excel 查看报表数据，可单击视觉对象上的选项菜单（三个点），然后选择**导出基础数据**。</span><span class="sxs-lookup"><span data-stu-id="df49c-152">To view report data in Excel, you can click the options menu (three dots) on a visual and select **Export underlying data**.</span></span> <span data-ttu-id="df49c-153">导出的数据将按照 Attract 中的用户权限进行筛选。</span><span class="sxs-lookup"><span data-stu-id="df49c-153">Exported data will export as filtered, respecting user permissions in Attract.</span></span> <span data-ttu-id="df49c-154">有关详细信息，请参阅[从可视化项导出数据](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data)。</span><span class="sxs-lookup"><span data-stu-id="df49c-154">For more information, see [Export data from visualizations](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span></span>

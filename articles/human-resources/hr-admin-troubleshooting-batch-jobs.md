---
title: 通过将批处理作业安排到非营业时间优化性能
description: 此主题介绍如何通过将批处理作业安排到非营业时间来解决 Microsoft Dynamics 365 Human Resources 的性能问题。
author: andreabichsel
manager: AnnBe
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 452a87cf5ba6c1ac73636584d75b2ec2ac555e02
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527757"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="feaa8-103">通过将批处理作业安排到非营业时间优化性能</span><span class="sxs-lookup"><span data-stu-id="feaa8-103">Optimize performance by scheduling batch jobs after hours</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="feaa8-104">发货</span><span class="sxs-lookup"><span data-stu-id="feaa8-104">Issue</span></span>

<span data-ttu-id="feaa8-105">如果在典型营业时间长时间运行批处理作业，Microsoft Dynamics 365 Human Resources 可能会遇到性能问题。</span><span class="sxs-lookup"><span data-stu-id="feaa8-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="feaa8-106">解决方法</span><span class="sxs-lookup"><span data-stu-id="feaa8-106">Resolution</span></span>

<span data-ttu-id="feaa8-107">将以下批处理作业安排到非工作时间。</span><span class="sxs-lookup"><span data-stu-id="feaa8-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="feaa8-108">我们还建议检查频繁运行的批处理作业的频率。</span><span class="sxs-lookup"><span data-stu-id="feaa8-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="feaa8-109">如果可以，减少批处理作业的周期。</span><span class="sxs-lookup"><span data-stu-id="feaa8-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="feaa8-110">在许多情况下，默认频率就足够了。</span><span class="sxs-lookup"><span data-stu-id="feaa8-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="feaa8-111">以下批处理作业应该在夜间或非营业时间运行。</span><span class="sxs-lookup"><span data-stu-id="feaa8-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="feaa8-112">务必检查这些定期批处理作业的时区。</span><span class="sxs-lookup"><span data-stu-id="feaa8-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="feaa8-113">某些批处理作业可能使用太平洋标准时间 (PST)。</span><span class="sxs-lookup"><span data-stu-id="feaa8-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="feaa8-114">批处理作业</span><span class="sxs-lookup"><span data-stu-id="feaa8-114">Batch job</span></span> | <span data-ttu-id="feaa8-115">本币</span><span class="sxs-lookup"><span data-stu-id="feaa8-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="feaa8-116">批处理作业历史记录清理</span><span class="sxs-lookup"><span data-stu-id="feaa8-116">Batch job history cleanup</span></span> | <span data-ttu-id="feaa8-117">每月 1 次</span><span class="sxs-lookup"><span data-stu-id="feaa8-117">1 time per month</span></span> |
| <span data-ttu-id="feaa8-118">出口暂存清除</span><span class="sxs-lookup"><span data-stu-id="feaa8-118">Export staging cleanup</span></span> | <span data-ttu-id="feaa8-119">每天 1 次</span><span class="sxs-lookup"><span data-stu-id="feaa8-119">1 time per day</span></span> |
| <span data-ttu-id="feaa8-120">Common Data Service 集成缺失的请求同步</span><span class="sxs-lookup"><span data-stu-id="feaa8-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="feaa8-121">每天 1 次</span><span class="sxs-lookup"><span data-stu-id="feaa8-121">1 time per day</span></span> |
| <span data-ttu-id="feaa8-122">需要在非工作时间定期运行的数据库压缩系统作业</span><span class="sxs-lookup"><span data-stu-id="feaa8-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="feaa8-123">每天 1 次</span><span class="sxs-lookup"><span data-stu-id="feaa8-123">1 time per day</span></span> |
| <span data-ttu-id="feaa8-124">需要在非工作时间定期运行的数据库索引重建系统作业</span><span class="sxs-lookup"><span data-stu-id="feaa8-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="feaa8-125">每天 1 次</span><span class="sxs-lookup"><span data-stu-id="feaa8-125">1 time per day</span></span> |

1. <span data-ttu-id="feaa8-126">在 Human Resources 中，选择 **系统管理**。</span><span class="sxs-lookup"><span data-stu-id="feaa8-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="feaa8-127">在 **搜索** 栏中，搜索上面的一个批处理作业。</span><span class="sxs-lookup"><span data-stu-id="feaa8-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="feaa8-128">选择 **在后台运行**，然后选择 **重复执行**。</span><span class="sxs-lookup"><span data-stu-id="feaa8-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![设置重复执行](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="feaa8-130">在 **定义重复项** 下，将 **开始日期** 和 **开始时间** 设置为在下班时间或周末进行。</span><span class="sxs-lookup"><span data-stu-id="feaa8-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="feaa8-131">选择 **无结束日期**。</span><span class="sxs-lookup"><span data-stu-id="feaa8-131">Select **No end date**.</span></span> 

   ![定义重复执行的开始日期和时间](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="feaa8-133">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="feaa8-133">Select **OK**.</span></span>

6. <span data-ttu-id="feaa8-134">如果需要，更改 **在后台运行** 下的其他任何参数，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="feaa8-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="feaa8-135">其他资源</span><span class="sxs-lookup"><span data-stu-id="feaa8-135">Additional resources</span></span>

[<span data-ttu-id="feaa8-136">使用自动清理任务优化性能</span><span class="sxs-lookup"><span data-stu-id="feaa8-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)

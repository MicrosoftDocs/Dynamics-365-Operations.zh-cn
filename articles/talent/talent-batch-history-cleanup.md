---
title: 使用自动清理任务优化性能
description: 此主题介绍如何通过清理批处理作业历史记录来解决 Microsoft Dynamics 365 Talent 的某些性能问题。
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a053c9094151f4e12e4aadc533dd272258779540
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832574"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="b605d-103">使用自动清理任务优化性能</span><span class="sxs-lookup"><span data-stu-id="b605d-103">Optimize performance with auto cleanup tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b605d-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="b605d-104">**Issue**</span></span>

<span data-ttu-id="b605d-105">如果批处理作业历史记录变得太大，Microsoft Dynamics 365 Talent 可能遇到性能问题。</span><span class="sxs-lookup"><span data-stu-id="b605d-105">Microsoft Dynamics 365 Talent can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="b605d-106">**原因**</span><span class="sxs-lookup"><span data-stu-id="b605d-106">**Cause**</span></span>

<span data-ttu-id="b605d-107">经常运行的批处理作业可能导致批处理作业历史记录增长到无法持续。</span><span class="sxs-lookup"><span data-stu-id="b605d-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="b605d-108">这可能导致性能问题。</span><span class="sxs-lookup"><span data-stu-id="b605d-108">This can cause performance issues.</span></span> 

<span data-ttu-id="b605d-109">**解决方法**</span><span class="sxs-lookup"><span data-stu-id="b605d-109">**Resolution**</span></span>

<span data-ttu-id="b605d-110">安排自动任务以清理批处理作业历史记录。</span><span class="sxs-lookup"><span data-stu-id="b605d-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="b605d-111">建议将任务设置为每周运行一次，但是您的清理频率可能需要更大或更小，具体取决于您的环境。</span><span class="sxs-lookup"><span data-stu-id="b605d-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="b605d-112">以下过程中包含我们建议的设置，但是您可以根据自己的需要更改这些设置。</span><span class="sxs-lookup"><span data-stu-id="b605d-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="b605d-113">在 Talent 中，选择**系统管理**。</span><span class="sxs-lookup"><span data-stu-id="b605d-113">In Talent, select **System administration**.</span></span>

2. <span data-ttu-id="b605d-114">在**搜索**栏中，输入**批处理作业历史记录清理**。</span><span class="sxs-lookup"><span data-stu-id="b605d-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![搜索批处理作业历史记录清理](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="b605d-116">在**历史记录限制(天)** 中，输入 **30**。</span><span class="sxs-lookup"><span data-stu-id="b605d-116">In **History limit (days)**, enter **30**.</span></span>

   ![将历史记录限制设置为 30](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="b605d-118">选择**在后台运行**，然后选择**重复执行**。</span><span class="sxs-lookup"><span data-stu-id="b605d-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![设置重复执行](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="b605d-120">在**定义重复项**下，将**开始日期**和**开始时间**设置为在下班时间或周末进行，然后选择**无结束日期**。</span><span class="sxs-lookup"><span data-stu-id="b605d-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![定义重复执行的开始日期和时间](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="b605d-122">在**重复执行模式**下，选择**天**，然后将**指定间隔过后重复**设置为 **7**。</span><span class="sxs-lookup"><span data-stu-id="b605d-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![设置每周重复清理](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="b605d-124">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b605d-124">Select **OK**.</span></span>

8. <span data-ttu-id="b605d-125">根据需要更改**在后台运行**下的其他任何参数，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b605d-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>


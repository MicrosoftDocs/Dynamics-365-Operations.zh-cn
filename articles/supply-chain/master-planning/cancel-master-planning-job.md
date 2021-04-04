---
title: 取消主计划作业
description: 本主题说明如何取消使用内置计划功能的活动计划作业。
author: ChristianRytt
manager: tfehr
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3d5dad766f4c01e993dd77dd762595b29208c6cb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264738"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="dd27b-103">取消主计划作业</span><span class="sxs-lookup"><span data-stu-id="dd27b-103">Cancel a master planning job</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd27b-104">在 Microsoft Dynamics 365 Supply Chain Management 中，有多个选项可用于取消主计划作业。</span><span class="sxs-lookup"><span data-stu-id="dd27b-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="dd27b-105">例如，如果主计划作业是被错误开始的或运行时间比预期长，您想要结束它，您可能希望取消主计划作业。</span><span class="sxs-lookup"><span data-stu-id="dd27b-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="dd27b-106">取消计划作业的最佳方法是从 **未完成的计划流程** 页进行。</span><span class="sxs-lookup"><span data-stu-id="dd27b-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="dd27b-107">只有未在几分钟内完成从 **未完成的计划流程** 页取消主计划作业时，才应使用 **批处理作业** 和 **增强的批处理作业** 页面的替代选项。</span><span class="sxs-lookup"><span data-stu-id="dd27b-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="dd27b-108">首选取消选项</span><span class="sxs-lookup"><span data-stu-id="dd27b-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="dd27b-109">从 **未完成的计划流程** 页取消主计划作业</span><span class="sxs-lookup"><span data-stu-id="dd27b-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="dd27b-110">转到 **主计划 > 查询和报表 > 主计划 > 未完成的计划流程**。</span><span class="sxs-lookup"><span data-stu-id="dd27b-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="dd27b-111">选择具有您要取消的计划流程的行。</span><span class="sxs-lookup"><span data-stu-id="dd27b-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="dd27b-112">单击 **取消**。</span><span class="sxs-lookup"><span data-stu-id="dd27b-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="dd27b-113">其他取消选项</span><span class="sxs-lookup"><span data-stu-id="dd27b-113">Additional cancel options</span></span>
<span data-ttu-id="dd27b-114">仅当未在几分钟内从 **未完成的计划流程** 页取消主计划作业时，才应使用这些选项。</span><span class="sxs-lookup"><span data-stu-id="dd27b-114">These should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="dd27b-115">从 **批处理作业** 页删除主计划作业</span><span class="sxs-lookup"><span data-stu-id="dd27b-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="dd27b-116">转到 **系统管理 > 查询 > 批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="dd27b-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="dd27b-117">选择具有您要删除的计划作业的行。</span><span class="sxs-lookup"><span data-stu-id="dd27b-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="dd27b-118">单击 **删除**。</span><span class="sxs-lookup"><span data-stu-id="dd27b-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="dd27b-119">从 **增强的批处理作业** 页中止主计划作业任务</span><span class="sxs-lookup"><span data-stu-id="dd27b-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="dd27b-120">转到 **系统管理 > 查询 > 批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="dd27b-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="dd27b-121">如果作业 ID 未显示在列表中，请单击 **切换到增强窗体**，或继续下一步。</span><span class="sxs-lookup"><span data-stu-id="dd27b-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="dd27b-122">打开批处理作业。</span><span class="sxs-lookup"><span data-stu-id="dd27b-122">Open the batch job.</span></span> <span data-ttu-id="dd27b-123">单击具有您要结束的任务的批处理作业的 **作业 ID**。</span><span class="sxs-lookup"><span data-stu-id="dd27b-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="dd27b-124">在 **批处理任务** 中，选择要结束的任务。</span><span class="sxs-lookup"><span data-stu-id="dd27b-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="dd27b-125">单击 **更改状态**，选择 **取消**，然后单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="dd27b-125">Click **Change status**, choose **Canceling** and click **OK**.</span></span>
6. <span data-ttu-id="dd27b-126">在 **批处理任务** 快速选项卡中，单击 **中止**。</span><span class="sxs-lookup"><span data-stu-id="dd27b-126">On the **Batch tasks** FastTab, click **Abort**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
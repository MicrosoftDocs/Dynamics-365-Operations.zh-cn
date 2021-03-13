---
title: 取消计划作业
description: 本主题说明如何取消使用“计划优化”功能的活动计划作业。
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 7cee11e6d9e8bc2fe83f5369554ae9ff9ee2b741
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008208"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="e1a52-103">取消计划作业</span><span class="sxs-lookup"><span data-stu-id="e1a52-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e1a52-104">在 Microsoft Dynamics 365 Supply Chain Management 中，您可以取消使用“计划优化”功能的活动计划作业。</span><span class="sxs-lookup"><span data-stu-id="e1a52-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="e1a52-105">如果在直接从用户界面（而不是后台）触发了计划优化作业后在对话框中选择 **取消**，不会取消该计划优化作业。</span><span class="sxs-lookup"><span data-stu-id="e1a52-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="e1a52-106">即使收到“已取消操作”之类警告，您仍然需要通过以下步骤通过计划优化取消计划作业。</span><span class="sxs-lookup"><span data-stu-id="e1a52-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="e1a52-107">要取消活动的计划作业，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="e1a52-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="e1a52-108">仅活动作业可以取消。</span><span class="sxs-lookup"><span data-stu-id="e1a52-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="e1a52-109">转到 **主计划 \> 设置 \> 计划**。</span><span class="sxs-lookup"><span data-stu-id="e1a52-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="e1a52-110">为计划运行选择适当的计划。</span><span class="sxs-lookup"><span data-stu-id="e1a52-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="e1a52-111">选择 **历史记录**。</span><span class="sxs-lookup"><span data-stu-id="e1a52-111">Select **History**.</span></span>
4. <span data-ttu-id="e1a52-112">选择要取消的计划作业。</span><span class="sxs-lookup"><span data-stu-id="e1a52-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="e1a52-113">选择 **取消**。</span><span class="sxs-lookup"><span data-stu-id="e1a52-113">Select **Cancel**.</span></span>

<span data-ttu-id="e1a52-114">作业状态将为 **正在取消**，直到计划优化服务确认该作业已被取消。</span><span class="sxs-lookup"><span data-stu-id="e1a52-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="e1a52-115">然后，状态将更改为 **已取消**。</span><span class="sxs-lookup"><span data-stu-id="e1a52-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="e1a52-116">要查看状态更改，您必须通过选择 **刷新** 按钮刷新页面。</span><span class="sxs-lookup"><span data-stu-id="e1a52-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1a52-117">其他资源</span><span class="sxs-lookup"><span data-stu-id="e1a52-117">Additional resources</span></span>

[<span data-ttu-id="e1a52-118">计划优化概览</span><span class="sxs-lookup"><span data-stu-id="e1a52-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="e1a52-119">开始使用计划优化</span><span class="sxs-lookup"><span data-stu-id="e1a52-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="e1a52-120">计划优化拟合分析</span><span class="sxs-lookup"><span data-stu-id="e1a52-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="e1a52-121">查看计划历史记录和计划日志</span><span class="sxs-lookup"><span data-stu-id="e1a52-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="e1a52-122">将筛选器应用于计划</span><span class="sxs-lookup"><span data-stu-id="e1a52-122">Apply filters to a plan</span></span>](plan-filters.md)

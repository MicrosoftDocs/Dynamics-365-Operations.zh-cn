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
ms.openlocfilehash: 5aadf7fb94bb2d836892064837f9cb1c5790d657
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238006"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="7f8fc-103">取消计划作业</span><span class="sxs-lookup"><span data-stu-id="7f8fc-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f8fc-104">在 Microsoft Dynamics 365 Supply Chain Management 中，您可以取消使用“计划优化”功能的活动计划作业。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="7f8fc-105">如果在直接从用户界面（而不是后台）触发了计划优化作业后在对话框中选择 **取消**，不会取消该计划优化作业。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="7f8fc-106">即使收到“已取消操作”之类警告，您仍然需要通过以下步骤通过计划优化取消计划作业。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="7f8fc-107">要取消活动的计划作业，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="7f8fc-108">仅活动作业可以取消。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="7f8fc-109">转到 **主计划 \> 设置 \> 计划**。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="7f8fc-110">为计划运行选择适当的计划。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="7f8fc-111">选择 **历史记录**。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-111">Select **History**.</span></span>
4. <span data-ttu-id="7f8fc-112">选择要取消的计划作业。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="7f8fc-113">选择 **取消**。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-113">Select **Cancel**.</span></span>

<span data-ttu-id="7f8fc-114">作业状态将为 **正在取消**，直到计划优化服务确认该作业已被取消。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="7f8fc-115">然后，状态将更改为 **已取消**。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="7f8fc-116">要查看状态更改，您必须通过选择 **刷新** 按钮刷新页面。</span><span class="sxs-lookup"><span data-stu-id="7f8fc-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f8fc-117">其他资源</span><span class="sxs-lookup"><span data-stu-id="7f8fc-117">Additional resources</span></span>

[<span data-ttu-id="7f8fc-118">计划优化概览</span><span class="sxs-lookup"><span data-stu-id="7f8fc-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="7f8fc-119">开始使用计划优化</span><span class="sxs-lookup"><span data-stu-id="7f8fc-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="7f8fc-120">计划优化拟合分析</span><span class="sxs-lookup"><span data-stu-id="7f8fc-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="7f8fc-121">查看计划历史记录和计划日志</span><span class="sxs-lookup"><span data-stu-id="7f8fc-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="7f8fc-122">将筛选器应用于计划</span><span class="sxs-lookup"><span data-stu-id="7f8fc-122">Apply filters to a plan</span></span>](plan-filters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
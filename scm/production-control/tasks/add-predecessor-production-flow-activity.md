--- 
title: "将前导活动添加到生产流活动"
description: "在生产流版本中，必须为所有活动排序。"
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 352c601e9de00d08bf994807d445fe91c8278557
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="36555-103">将前导活动添加到生产流活动</span><span class="sxs-lookup"><span data-stu-id="36555-103">Add a predecessor to a production flow activity</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="36555-104">在生产流版本中，必须为所有活动排序。</span><span class="sxs-lookup"><span data-stu-id="36555-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="36555-105">一个活动可以有一个或多个前导活动或后续活动。</span><span class="sxs-lookup"><span data-stu-id="36555-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="36555-106">此过程显示如何将前导活动关联到活动。</span><span class="sxs-lookup"><span data-stu-id="36555-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="36555-107">若要执行此任务，需要草稿版本至少有两个可连接的活动的生产流。</span><span class="sxs-lookup"><span data-stu-id="36555-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="36555-108">若要了解详细信息，请阅读白皮书“lean manufacturing 中的生产流和活动”。</span><span class="sxs-lookup"><span data-stu-id="36555-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="36555-109">找到生产流和版本</span><span class="sxs-lookup"><span data-stu-id="36555-109">Find the production flow and version</span></span>
1. <span data-ttu-id="36555-110">转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。</span><span class="sxs-lookup"><span data-stu-id="36555-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="36555-111">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="36555-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="36555-112">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="36555-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="36555-113">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="36555-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="36555-114">单击“活动”。</span><span class="sxs-lookup"><span data-stu-id="36555-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="36555-115">选择活动和添加前导活动</span><span class="sxs-lookup"><span data-stu-id="36555-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="36555-116">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="36555-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="36555-117">单击“添加前导活动”。</span><span class="sxs-lookup"><span data-stu-id="36555-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="36555-118">在“活动”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="36555-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="36555-119">在“周期时间比率”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="36555-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="36555-120">活动关系的默认周期时间比率为 1。</span><span class="sxs-lookup"><span data-stu-id="36555-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="36555-121">这假设两个活动按照相同的速度或单位产品生产时间运行。</span><span class="sxs-lookup"><span data-stu-id="36555-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="36555-122">如果前导活动按照较高的速度（较低的单位产品生产时间）运行，则比率应低于 1，如果前导活动以较慢的速度（较高的单位产品生产时间）运行，则周期时间比率大于 1。</span><span class="sxs-lookup"><span data-stu-id="36555-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="36555-123">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="36555-123">Click OK.</span></span>


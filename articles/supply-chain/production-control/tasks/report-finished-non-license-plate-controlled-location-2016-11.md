--- 
title: "报告为已完工入库到非牌照控制的库位"
description: "此任务指南显示报告为完工入库到非牌照控制的位置的示例。"
author: ChristianRytt
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: dcf78f54422f8c17e4965cc5d664cd9bdbc3f440
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---
# <a name="report-as-finished-to-a-plate-controlled-location"></a><span data-ttu-id="cd1d6-103">报告为已完工入库到非牌照控制的库位</span><span class="sxs-lookup"><span data-stu-id="cd1d6-103">Report as finished to a plate-controlled location</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd1d6-104">此任务指南显示报告为完工入库到非牌照控制的位置的示例。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="cd1d6-105">一个适用的工作策略是此任务的先决条件。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="cd1d6-106">以前的任务指南显示工作策略的设置。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="cd1d6-107">此任务指南需要 Dynamics AX 应用程序 7.0.1 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="cd1d6-108">设置输出库位</span><span class="sxs-lookup"><span data-stu-id="cd1d6-108">Set up an output location</span></span>
1. <span data-ttu-id="cd1d6-109">转到“组织管理”>“资源”>“资源组”。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="cd1d6-110">在列表中选择资源组 '5102'。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="cd1d6-111">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-111">Click Edit.</span></span>
4. <span data-ttu-id="cd1d6-112">在“输出仓库”字段中，输入 '51'。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="cd1d6-113">在“输出库位”字段中，输入 '001'。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="cd1d6-114">库位 001 不是牌照控制的位置。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="cd1d6-115">只有当库位存在适用的工作策略时，您才可以设置非牌照控制的输出位置。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="cd1d6-116">创建生产订单并报告为已完工入库</span><span class="sxs-lookup"><span data-stu-id="cd1d6-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="cd1d6-117">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-117">Close the page.</span></span>
2. <span data-ttu-id="cd1d6-118">转到“生产控制”>“生产订单”>“全部生产订单”。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="cd1d6-119">单击“新建生产订单”。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-119">Click New production order.</span></span>
4. <span data-ttu-id="cd1d6-120">在“物料编号”字段中输入 'L0101'。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="cd1d6-121">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-121">Click Create.</span></span>
6. <span data-ttu-id="cd1d6-122">在“操作窗格”中，单击“生产订单”。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="cd1d6-123">单击“估计”。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-123">Click Estimate.</span></span>
8. <span data-ttu-id="cd1d6-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-124">Click OK.</span></span>
9. <span data-ttu-id="cd1d6-125">单击“开始”。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-125">Click Start.</span></span>
10. <span data-ttu-id="cd1d6-126">单击“常规”选项卡。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-126">Click the General tab.</span></span>
11. <span data-ttu-id="cd1d6-127">在“自动物料清单消耗量”字段中，选择“从不”。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="cd1d6-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-128">Click OK.</span></span>
13. <span data-ttu-id="cd1d6-129">单击“完工入库”。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-129">Click Report as finished.</span></span>
14. <span data-ttu-id="cd1d6-130">单击“常规”选项卡。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-130">Click the General tab.</span></span>
15. <span data-ttu-id="cd1d6-131">在“接受错误”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="cd1d6-132">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-132">Click OK.</span></span>
17. <span data-ttu-id="cd1d6-133">在“操作窗格”中，单击“仓库”。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="cd1d6-134">单击“工作详细信息”。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-134">Click Work details.</span></span>
    * <span data-ttu-id="cd1d6-135">在生产订单报告为完工入库时，尚未为储存生成工作。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="cd1d6-136">发生这种情况是因为将工作策略定义为在产品 L0101 报告为已完工入库到库位 001 时阻止生成工作。</span><span class="sxs-lookup"><span data-stu-id="cd1d6-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  



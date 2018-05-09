--- 
title: "完成已发布基础产品的基本设置"
description: "该过程会显示在基础产品可用于物料清单版本之前，如何完成所需的最低设置。"
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 35ca13f157537087346a5bcf9c6ccdd659a0d772
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="0fd05-103">完成已发布基础产品的基本设置</span><span class="sxs-lookup"><span data-stu-id="0fd05-103">Complete basic setup of a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0fd05-104">该过程会显示在基础产品可用于物料清单版本之前，如何完成所需的最低设置。</span><span class="sxs-lookup"><span data-stu-id="0fd05-104">This procedure shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="0fd05-105">这是八个过程中第三个说明如何构建基于维度的配置组合的过程。</span><span class="sxs-lookup"><span data-stu-id="0fd05-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="0fd05-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="0fd05-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="0fd05-107">转到“产品信息管理”>“产品”>“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="0fd05-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="0fd05-108">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="0fd05-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0fd05-109">选择您已在第二个过程中发布的基础产品。</span><span class="sxs-lookup"><span data-stu-id="0fd05-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="0fd05-110">此基础产品是使用基于维度的配置技术创建的。</span><span class="sxs-lookup"><span data-stu-id="0fd05-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="0fd05-111">在操作窗格上，单击“产品”。</span><span class="sxs-lookup"><span data-stu-id="0fd05-111">On the Action Pane, click Product.</span></span>
4. <span data-ttu-id="0fd05-112">单击“维度组”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="0fd05-112">Click Dimension groups to open the drop dialog.</span></span>
5. <span data-ttu-id="0fd05-113">在“存储维度组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="0fd05-113">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0fd05-114">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="0fd05-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0fd05-115">存储维度组确定哪些存储维度用于产品交易记录。</span><span class="sxs-lookup"><span data-stu-id="0fd05-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="0fd05-116">选择该过程适用的站点。</span><span class="sxs-lookup"><span data-stu-id="0fd05-116">Select Site for this procedure.</span></span>  
7. <span data-ttu-id="0fd05-117">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="0fd05-117">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="0fd05-118">在“跟踪维度组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="0fd05-118">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="0fd05-119">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="0fd05-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0fd05-120">跟踪维度组确定哪些跟踪维度用于产品交易记录。</span><span class="sxs-lookup"><span data-stu-id="0fd05-120">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="0fd05-121">针对该过程选择“无”。</span><span class="sxs-lookup"><span data-stu-id="0fd05-121">Select None for this procedure.</span></span>  
10. <span data-ttu-id="0fd05-122">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="0fd05-122">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="0fd05-123">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0fd05-123">Click OK.</span></span>
12. <span data-ttu-id="0fd05-124">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="0fd05-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="0fd05-125">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="0fd05-125">Click Edit.</span></span>
    * <span data-ttu-id="0fd05-126">打开“已发布产品详情”窗体以继续执行设置任务。</span><span class="sxs-lookup"><span data-stu-id="0fd05-126">Open the Released product details form to continue the setup task.</span></span>  
14. <span data-ttu-id="0fd05-127">在“物料模型组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="0fd05-127">In the Item model group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="0fd05-128">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="0fd05-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0fd05-129">物料模型组包含决定在进行物料收货和发货时如何控制和处理物料的设置。</span><span class="sxs-lookup"><span data-stu-id="0fd05-129">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="0fd05-130">它们还决定着如何计算物料消耗量。</span><span class="sxs-lookup"><span data-stu-id="0fd05-130">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="0fd05-131">选择该过程适用的 FIFO。</span><span class="sxs-lookup"><span data-stu-id="0fd05-131">Select   FIFO for this procedure.</span></span>  
16. <span data-ttu-id="0fd05-132">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="0fd05-132">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="0fd05-133">展开或折叠“管理成本”部分。</span><span class="sxs-lookup"><span data-stu-id="0fd05-133">Expand or collapse the Manage costs section.</span></span>
18. <span data-ttu-id="0fd05-134">在“物料组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="0fd05-134">In the Item group field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="0fd05-135">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="0fd05-135">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0fd05-136">物料组基于物料特征将库存物料分成不同的组，可用于管理库存。</span><span class="sxs-lookup"><span data-stu-id="0fd05-136">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="0fd05-137">选择该过程适用的 CarAudio。</span><span class="sxs-lookup"><span data-stu-id="0fd05-137">Select   CarAudio for this procedure.</span></span>  
20. <span data-ttu-id="0fd05-138">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="0fd05-138">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="0fd05-139">在操作窗格上，单击“计划”。</span><span class="sxs-lookup"><span data-stu-id="0fd05-139">On the Action Pane, click Plan.</span></span>
22. <span data-ttu-id="0fd05-140">点击默认订单设置。</span><span class="sxs-lookup"><span data-stu-id="0fd05-140">Click Default order settings.</span></span>
23. <span data-ttu-id="0fd05-141">在“默认订单类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="0fd05-141">In the Default order type field, select an option.</span></span>
    * <span data-ttu-id="0fd05-142">选择“生产”以指定此基础产品的默认值供应选项将会生产它。</span><span class="sxs-lookup"><span data-stu-id="0fd05-142">Select Production to specify that the default supply option for this product master is to produce it.</span></span>  
24. <span data-ttu-id="0fd05-143">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0fd05-143">Close the page.</span></span>
25. <span data-ttu-id="0fd05-144">关闭“已发布产品详情”窗体。</span><span class="sxs-lookup"><span data-stu-id="0fd05-144">Close the Released product details form.</span></span>



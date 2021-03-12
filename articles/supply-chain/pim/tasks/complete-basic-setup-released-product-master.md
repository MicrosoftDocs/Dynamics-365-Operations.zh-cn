---
title: 完成已发布基础产品的基本设置
description: 本主题显示在基础产品可用于物料清单版本之前，如何完成所需的最低设置。
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 668b60efa55fa553cf308d5bfc5da7e23f460366
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987021"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="cf39a-103">完成已发布基础产品的基本设置</span><span class="sxs-lookup"><span data-stu-id="cf39a-103">Complete basic setup of a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cf39a-104">本主题显示在基础产品可用于物料清单版本之前，如何完成所需的最低设置。</span><span class="sxs-lookup"><span data-stu-id="cf39a-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="cf39a-105">这是八个过程中第三个说明如何构建基于维度的配置组合的过程。</span><span class="sxs-lookup"><span data-stu-id="cf39a-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="cf39a-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="cf39a-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="cf39a-107">转到 **导航窗格 > 模块 > 产品信息管理 > 产品 > 已发放产品**。</span><span class="sxs-lookup"><span data-stu-id="cf39a-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="cf39a-108">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="cf39a-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="cf39a-109">选择您已在第二个过程中发布的基础产品。</span><span class="sxs-lookup"><span data-stu-id="cf39a-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="cf39a-110">此基础产品是使用基于维度的配置技术创建的。</span><span class="sxs-lookup"><span data-stu-id="cf39a-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="cf39a-111">在操作窗格上，选择 **产品**。</span><span class="sxs-lookup"><span data-stu-id="cf39a-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="cf39a-112">单击 **维度组** 以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="cf39a-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="cf39a-113">在 **存储维度组** 字段中，选择下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="cf39a-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="cf39a-114">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="cf39a-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="cf39a-115">存储维度组确定哪些存储维度用于产品交易记录。</span><span class="sxs-lookup"><span data-stu-id="cf39a-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="cf39a-116">选择该过程适用的 **站点**。</span><span class="sxs-lookup"><span data-stu-id="cf39a-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="cf39a-117">在 **跟踪维度组** 字段中，选择下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="cf39a-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="cf39a-118">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="cf39a-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="cf39a-119">跟踪维度组确定哪些跟踪维度用于产品交易记录。</span><span class="sxs-lookup"><span data-stu-id="cf39a-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="cf39a-120">针对该过程选择 **无**。</span><span class="sxs-lookup"><span data-stu-id="cf39a-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="cf39a-121">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="cf39a-121">Click **OK**.</span></span>
10. <span data-ttu-id="cf39a-122">单击 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="cf39a-122">Click **Edit**.</span></span>
11. <span data-ttu-id="cf39a-123">在 **物料模型组** 字段中，选择下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="cf39a-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="cf39a-124">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="cf39a-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="cf39a-125">物料模型组包含决定在进行物料收货和发货时如何控制和处理物料的设置。</span><span class="sxs-lookup"><span data-stu-id="cf39a-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="cf39a-126">它们还决定着如何计算物料消耗量。</span><span class="sxs-lookup"><span data-stu-id="cf39a-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="cf39a-127">选择该过程适用的 **FIFO**。</span><span class="sxs-lookup"><span data-stu-id="cf39a-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="cf39a-128">展开 **管理成本** 部分。</span><span class="sxs-lookup"><span data-stu-id="cf39a-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="cf39a-129">在 **物料组** 字段中，选择下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="cf39a-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="cf39a-130">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="cf39a-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="cf39a-131">物料组基于物料特征将库存物料分成不同的组，可用于管理库存。</span><span class="sxs-lookup"><span data-stu-id="cf39a-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="cf39a-132">选择该过程适用的 **CarAudio**。</span><span class="sxs-lookup"><span data-stu-id="cf39a-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="cf39a-133">在操作窗格上，选择 **计划**。</span><span class="sxs-lookup"><span data-stu-id="cf39a-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="cf39a-134">选择 **默认订单设置**。</span><span class="sxs-lookup"><span data-stu-id="cf39a-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="cf39a-135">在 **默认订单类型** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="cf39a-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="cf39a-136">选择 **生产** 以指定此基础产品的默认值供应选项将会生产它。</span><span class="sxs-lookup"><span data-stu-id="cf39a-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="cf39a-137">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="cf39a-137">Select **Save**.</span></span>
20. <span data-ttu-id="cf39a-138">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cf39a-138">Close the page.</span></span>
21. <span data-ttu-id="cf39a-139">关闭 **已发布产品详情** 窗体。</span><span class="sxs-lookup"><span data-stu-id="cf39a-139">Close the **Released product details** form.</span></span>


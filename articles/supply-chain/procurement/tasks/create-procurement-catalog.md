---
title: 创建采购目录
description: 本主题介绍如何创建采购目录。
author: mkirknel
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55bc7479ca9ba3ca86e23b5bee106ef169c40077
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836366"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="f9d3b-103">创建采购目录</span><span class="sxs-lookup"><span data-stu-id="f9d3b-103">Create a procurement catalog</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9d3b-104">本主题介绍如何创建采购目录。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-104">This topic explains how to create a procurement catalog.</span></span> <span data-ttu-id="f9d3b-105">此任务通常由采购专业人员完成。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="f9d3b-106">您还将了解员工在创建申请时如何使用目录。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="f9d3b-107">系统中必须已有采购类别层次结构，才能创建目录。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="f9d3b-108">新目录继承层次结构，以及其中的所有产品。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="f9d3b-109">可在采购类别层次结构可用的演示数据公司 USMF 中使用此指南，以及使用前面的步骤中使用的示例。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="f9d3b-110">确保存在采购类别层次结构。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="f9d3b-111">转到**导航窗格 > 模块 > 采购 > 采购目录**。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-111">Go to **navigation pane > Modules > Procurement and sourcing > Procurement categories**.</span></span> <span data-ttu-id="f9d3b-112">USMF 演示数据公司中可使用采购目录层次结构，并且产品已添加到**办公设备/计算机**类别。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the **Office machines/Computers** category.</span></span> <span data-ttu-id="f9d3b-113">如果您正在运行该过程以作为任务指南，并且要浏览类别，您需要解锁该指南。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-113">If you’re running this procedure as a task guide, you’ll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="f9d3b-114">如果层次结构不可用，可通过单击**新建**创建。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-114">If a hierarchy was not available, you’d create it by clicking **New**.</span></span> <span data-ttu-id="f9d3b-115">此操作只能执行一次。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-115">This can only be done once.</span></span>  
2. <span data-ttu-id="f9d3b-116">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="f9d3b-117">创建目录</span><span class="sxs-lookup"><span data-stu-id="f9d3b-117">Create a catalog</span></span>
1. <span data-ttu-id="f9d3b-118">转到**导航窗格 > 模块 > 采购 > 目录 > 采购目录**。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-118">Go to **navigation pane > Modules > Procurement and sourcing > Catalogs > Procurement catalogs**.</span></span>
2. <span data-ttu-id="f9d3b-119">选择**新采购目录**以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-119">Select **New procurement catalog** to open the drop dialog.</span></span>
3. <span data-ttu-id="f9d3b-120">在**名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-120">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="f9d3b-121">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-121">Select **OK**.</span></span>
5. <span data-ttu-id="f9d3b-122">在树中，展开**企业采购类别**。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-122">In the tree, expand **CORP PROCUREMENT CATEGORIES**.</span></span>
6. <span data-ttu-id="f9d3b-123">在树中，展开**办公设备**。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-123">In the tree, expand **OFFICE MACHINES**.</span></span>
7. <span data-ttu-id="f9d3b-124">在树中，选择**计算机**。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-124">In the tree, select **Computers**.</span></span>

  - <span data-ttu-id="f9d3b-125">列表中将显示采购类别中的产品。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="f9d3b-126">如果要向类别添加产品，需要在**采购列表层次结构**页或**物料详细信息**页中执行此操作。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-126">If you want to add a product to the category you need to do this on the **Procurement category hierarchy** page or on the **Item details** page.</span></span>  
  - <span data-ttu-id="f9d3b-127">**默认**更新类型确定已添加到采购类别层次结构的新产品是否在目录中立即显示。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-127">The **Default** update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="f9d3b-128">如果更新类型设置为**动态**，将立即显示更改。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-128">If the update type is set to **Dynamic**, changes are visible immediately.</span></span> <span data-ttu-id="f9d3b-129">如果更新类型为**静态**，则新产品仅在已重新发布目录后对使用该目录的人员显示。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-129">If the update type is **Static**, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="f9d3b-130">页面顶部的操作窗格中支持**发布**操作。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-130">The **Publish** action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="f9d3b-131">如果从采购类别层次结构删除产品，无论**默认**更新类型字段中是哪个值，都将立即显示更改。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the **Default** update type field.</span></span>  

8. <span data-ttu-id="f9d3b-132">在操作窗格上，选择**类别导航**并确保选择**启用**。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-132">On the Action Pane, select **Category navigation** and ensure that **Enable** is selected.</span></span>
9. <span data-ttu-id="f9d3b-133">选择**启用目录**。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-133">Select **Activate catalog**.</span></span>
10. <span data-ttu-id="f9d3b-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-134">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="f9d3b-135">显示目录</span><span class="sxs-lookup"><span data-stu-id="f9d3b-135">Make the catalog visible</span></span>
1. <span data-ttu-id="f9d3b-136">转到**导航窗格 > 模块 > 采购 > 设置 > 策略 > 采购策略**。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-136">Go to **navigation pane > Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="f9d3b-137">选择**采购政策 USMF**。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-137">Select **Procurement Policy USMF**.</span></span> <span data-ttu-id="f9d3b-138">您需要连接到您的用户配置文件的工作人员获准订购其产品的法人选择采购政策。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-138">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="f9d3b-139">在 USMF 演示数据中，Admin 用户连接到工人 **Julia Funderburk**，而默认情况下该工人可订购 USMF 中的产品。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-139">In the USMF demo data, the Admin user is connected to the worker called **Julia Funderburk**, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="f9d3b-140">选择您刚创建的目录。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-140">Select the catalog that you’ve just created.</span></span>
4. <span data-ttu-id="f9d3b-141">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-141">Select **OK**.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="f9d3b-142">使用目录</span><span class="sxs-lookup"><span data-stu-id="f9d3b-142">Use the catalog</span></span>
1. <span data-ttu-id="f9d3b-143">转到**导航窗格 > 模块 > 采购 > 采购申请 > 所有采购申请**。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-143">Go to **navigation pane > Modules > Procurement and sourcing > Purchase requisitions > All purchase requisitions**.</span></span>
2. <span data-ttu-id="f9d3b-144">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-144">Select **New**.</span></span>
3. <span data-ttu-id="f9d3b-145">在**名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-145">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="f9d3b-146">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-146">Select **OK**.</span></span>
5. <span data-ttu-id="f9d3b-147">选择**添加产品**。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-147">Select **Add products**.</span></span>
6. <span data-ttu-id="f9d3b-148">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-148">In the list, find and select the desired record.</span></span> <span data-ttu-id="f9d3b-149">您可以使用左侧的类别层次结构或列表顶部的筛选器筛选产品。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-149">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="f9d3b-150">选择**添加到行**。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-150">Select **Add to lines**.</span></span>
8. <span data-ttu-id="f9d3b-151">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="f9d3b-151">Select **OK**.</span></span>


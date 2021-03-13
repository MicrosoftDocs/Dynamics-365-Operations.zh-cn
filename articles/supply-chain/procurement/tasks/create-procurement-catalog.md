---
title: 创建采购目录
description: 本主题介绍如何创建采购目录。
author: RichardLuan
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eaf8b8d8b369aa704344d6984a0f111af6e4285b
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016469"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="c6212-103">创建采购目录</span><span class="sxs-lookup"><span data-stu-id="c6212-103">Create a procurement catalog</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c6212-104">本主题介绍如何创建采购目录。</span><span class="sxs-lookup"><span data-stu-id="c6212-104">This topic explains how to create a procurement catalog.</span></span> <span data-ttu-id="c6212-105">此任务通常由采购专业人员完成。</span><span class="sxs-lookup"><span data-stu-id="c6212-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="c6212-106">您还将了解员工在创建申请时如何使用目录。</span><span class="sxs-lookup"><span data-stu-id="c6212-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="c6212-107">系统中必须已有采购类别层次结构，才能创建目录。</span><span class="sxs-lookup"><span data-stu-id="c6212-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="c6212-108">新目录继承层次结构，以及其中的所有产品。</span><span class="sxs-lookup"><span data-stu-id="c6212-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="c6212-109">可在采购类别层次结构可用的演示数据公司 USMF 中使用此指南，以及使用前面的步骤中使用的示例。</span><span class="sxs-lookup"><span data-stu-id="c6212-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="c6212-110">确保存在采购类别层次结构。</span><span class="sxs-lookup"><span data-stu-id="c6212-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="c6212-111">转到 **导航窗格 > 模块 > 采购 > 采购目录**。</span><span class="sxs-lookup"><span data-stu-id="c6212-111">Go to **navigation pane > Modules > Procurement and sourcing > Procurement categories**.</span></span> <span data-ttu-id="c6212-112">USMF 演示数据公司中可使用采购目录层次结构，并且产品已添加到 **办公设备/计算机** 类别。</span><span class="sxs-lookup"><span data-stu-id="c6212-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the **Office machines/Computers** category.</span></span> <span data-ttu-id="c6212-113">如果您正在运行该过程以作为任务指南，并且要浏览类别，您需要解锁该指南。</span><span class="sxs-lookup"><span data-stu-id="c6212-113">If you're running this procedure as a task guide, you'll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="c6212-114">如果层次结构不可用，可通过单击 **新建** 创建。</span><span class="sxs-lookup"><span data-stu-id="c6212-114">If a hierarchy was not available, you'd create it by clicking **New**.</span></span> <span data-ttu-id="c6212-115">此操作只能执行一次。</span><span class="sxs-lookup"><span data-stu-id="c6212-115">This can only be done once.</span></span>  
2. <span data-ttu-id="c6212-116">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c6212-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="c6212-117">创建目录</span><span class="sxs-lookup"><span data-stu-id="c6212-117">Create a catalog</span></span>
1. <span data-ttu-id="c6212-118">转到 **导航窗格 > 模块 > 采购 > 目录 > 采购目录**。</span><span class="sxs-lookup"><span data-stu-id="c6212-118">Go to **navigation pane > Modules > Procurement and sourcing > Catalogs > Procurement catalogs**.</span></span>
2. <span data-ttu-id="c6212-119">选择 **新采购目录** 以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="c6212-119">Select **New procurement catalog** to open the drop dialog.</span></span>
3. <span data-ttu-id="c6212-120">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c6212-120">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="c6212-121">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c6212-121">Select **OK**.</span></span>
5. <span data-ttu-id="c6212-122">在树中，展开 **企业采购类别**。</span><span class="sxs-lookup"><span data-stu-id="c6212-122">In the tree, expand **CORP PROCUREMENT CATEGORIES**.</span></span>
6. <span data-ttu-id="c6212-123">在树中，展开 **办公设备**。</span><span class="sxs-lookup"><span data-stu-id="c6212-123">In the tree, expand **OFFICE MACHINES**.</span></span>
7. <span data-ttu-id="c6212-124">在树中，选择 **计算机**。</span><span class="sxs-lookup"><span data-stu-id="c6212-124">In the tree, select **Computers**.</span></span>

  - <span data-ttu-id="c6212-125">列表中将显示采购类别中的产品。</span><span class="sxs-lookup"><span data-stu-id="c6212-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="c6212-126">如果要向类别添加产品，需要在 **采购列表层次结构** 页或 **物料详细信息** 页中执行此操作。</span><span class="sxs-lookup"><span data-stu-id="c6212-126">If you want to add a product to the category you need to do this on the **Procurement category hierarchy** page or on the **Item details** page.</span></span>  
  - <span data-ttu-id="c6212-127">**默认** 更新类型确定已添加到采购类别层次结构的新产品是否在目录中立即显示。</span><span class="sxs-lookup"><span data-stu-id="c6212-127">The **Default** update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="c6212-128">如果更新类型设置为 **动态**，将立即显示更改。</span><span class="sxs-lookup"><span data-stu-id="c6212-128">If the update type is set to **Dynamic**, changes are visible immediately.</span></span> <span data-ttu-id="c6212-129">如果更新类型为 **静态**，则新产品仅在已重新发布目录后对使用该目录的人员显示。</span><span class="sxs-lookup"><span data-stu-id="c6212-129">If the update type is **Static**, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="c6212-130">页面顶部的操作窗格中支持 **发布** 操作。</span><span class="sxs-lookup"><span data-stu-id="c6212-130">The **Publish** action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="c6212-131">如果从采购类别层次结构删除产品，无论 **默认** 更新类型字段中是哪个值，都将立即显示更改。</span><span class="sxs-lookup"><span data-stu-id="c6212-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the **Default** update type field.</span></span>  

8. <span data-ttu-id="c6212-132">在操作窗格上，选择 **类别导航** 并确保选择 **启用**。</span><span class="sxs-lookup"><span data-stu-id="c6212-132">On the Action Pane, select **Category navigation** and ensure that **Enable** is selected.</span></span>
9. <span data-ttu-id="c6212-133">选择 **启用目录**。</span><span class="sxs-lookup"><span data-stu-id="c6212-133">Select **Activate catalog**.</span></span>
10. <span data-ttu-id="c6212-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c6212-134">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="c6212-135">显示目录</span><span class="sxs-lookup"><span data-stu-id="c6212-135">Make the catalog visible</span></span>
1. <span data-ttu-id="c6212-136">转到 **导航窗格 > 模块 > 采购 > 设置 > 策略 > 采购策略**。</span><span class="sxs-lookup"><span data-stu-id="c6212-136">Go to **navigation pane > Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="c6212-137">选择 **采购政策 USMF**。</span><span class="sxs-lookup"><span data-stu-id="c6212-137">Select **Procurement Policy USMF**.</span></span> <span data-ttu-id="c6212-138">您需要连接到您的用户配置文件的工作人员获准订购其产品的法人选择采购政策。</span><span class="sxs-lookup"><span data-stu-id="c6212-138">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="c6212-139">在 USMF 演示数据中，Admin 用户连接到工人 **Julia Funderburk**，而默认情况下该工人可订购 USMF 中的产品。</span><span class="sxs-lookup"><span data-stu-id="c6212-139">In the USMF demo data, the Admin user is connected to the worker called **Julia Funderburk**, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="c6212-140">选择您刚创建的目录。</span><span class="sxs-lookup"><span data-stu-id="c6212-140">Select the catalog that you've just created.</span></span>
4. <span data-ttu-id="c6212-141">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c6212-141">Select **OK**.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="c6212-142">使用目录</span><span class="sxs-lookup"><span data-stu-id="c6212-142">Use the catalog</span></span>
1. <span data-ttu-id="c6212-143">转到 **导航窗格 > 模块 > 采购 > 采购申请 > 所有采购申请**。</span><span class="sxs-lookup"><span data-stu-id="c6212-143">Go to **navigation pane > Modules > Procurement and sourcing > Purchase requisitions > All purchase requisitions**.</span></span>
2. <span data-ttu-id="c6212-144">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="c6212-144">Select **New**.</span></span>
3. <span data-ttu-id="c6212-145">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c6212-145">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="c6212-146">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c6212-146">Select **OK**.</span></span>
5. <span data-ttu-id="c6212-147">选择 **添加产品**。</span><span class="sxs-lookup"><span data-stu-id="c6212-147">Select **Add products**.</span></span>
6. <span data-ttu-id="c6212-148">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="c6212-148">In the list, find and select the desired record.</span></span> <span data-ttu-id="c6212-149">您可以使用左侧的类别层次结构或列表顶部的筛选器筛选产品。</span><span class="sxs-lookup"><span data-stu-id="c6212-149">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="c6212-150">选择 **添加到行**。</span><span class="sxs-lookup"><span data-stu-id="c6212-150">Select **Add to lines**.</span></span>
8. <span data-ttu-id="c6212-151">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c6212-151">Select **OK**.</span></span>


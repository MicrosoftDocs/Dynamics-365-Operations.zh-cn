---
title: 创建基础产品
description: 为预定义变型创建基础产品。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae2290cf8da4387155de7790dd3db88b34eb6e96
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150071"
---
# <a name="create-a-product-master"></a><span data-ttu-id="17da0-103">创建基础产品</span><span class="sxs-lookup"><span data-stu-id="17da0-103">Create a product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17da0-104">为预定义变型创建基础产品。</span><span class="sxs-lookup"><span data-stu-id="17da0-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="17da0-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="17da0-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="17da0-106">此过程专门针对产品设计人员。</span><span class="sxs-lookup"><span data-stu-id="17da0-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="17da0-107">新建基础产品</span><span class="sxs-lookup"><span data-stu-id="17da0-107">Create a new product master</span></span>
1. <span data-ttu-id="17da0-108">转到**导航窗格 > 模块 > 产品信息管理 > 产品 > 基础产品**。</span><span class="sxs-lookup"><span data-stu-id="17da0-108">Go to **Navigation pane > Modules > Product information management > Products > Product masters**.</span></span>
2. <span data-ttu-id="17da0-109">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="17da0-109">Click **New**.</span></span>
3. <span data-ttu-id="17da0-110">在**产品编号**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="17da0-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="17da0-111">其编号必须是唯一的。</span><span class="sxs-lookup"><span data-stu-id="17da0-111">The number must be unique.</span></span> <span data-ttu-id="17da0-112">可在**产品编号**字段设置编号规则。</span><span class="sxs-lookup"><span data-stu-id="17da0-112">A number sequence can be set for the **Product number** field.</span></span> <span data-ttu-id="17da0-113">在这种情况下，用户不必输入一个值。</span><span class="sxs-lookup"><span data-stu-id="17da0-113">In this case, the user doesn't have to enter a value.</span></span>
4. <span data-ttu-id="17da0-114">在**产品名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="17da0-114">In the **Product name** field, type a value.</span></span> <span data-ttu-id="17da0-115">输入产品的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="17da0-115">Enter a descriptive product name.</span></span> <span data-ttu-id="17da0-116">该值默认为搜索名称，不过用户可以更改。</span><span class="sxs-lookup"><span data-stu-id="17da0-116">The value defaults to the search name, but this can be changed by the user.</span></span>
5. <span data-ttu-id="17da0-117">在**产品维度组**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="17da0-117">In the **Product dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="17da0-118">产品维度组确定可用于创建产品变型的 4 个产品维度。</span><span class="sxs-lookup"><span data-stu-id="17da0-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="17da0-119">此示例使用颜色和大小组。</span><span class="sxs-lookup"><span data-stu-id="17da0-119">This example uses a group with color and size.</span></span>
6. <span data-ttu-id="17da0-120">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="17da0-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="17da0-121">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="17da0-121">In the list, click the link in the selected row.</span></span> <span data-ttu-id="17da0-122">默认**配置技术**是“预定义变型”。</span><span class="sxs-lookup"><span data-stu-id="17da0-122">The default **Configuration technology** is 'Predefined variant'.</span></span> <span data-ttu-id="17da0-123">这将在此示例中使用。</span><span class="sxs-lookup"><span data-stu-id="17da0-123">This will be used for this example.</span></span>
8. <span data-ttu-id="17da0-124">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="17da0-124">Click **OK**.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="17da0-125">选择产品维度组</span><span class="sxs-lookup"><span data-stu-id="17da0-125">Select product dimension groups</span></span>
1. <span data-ttu-id="17da0-126">在**颜色组**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="17da0-126">In the **Color group** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="17da0-127">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="17da0-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="17da0-128">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="17da0-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="17da0-129">在**大小组**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="17da0-129">In the **Size group** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="17da0-130">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="17da0-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="17da0-131">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="17da0-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="17da0-132">添加维度组</span><span class="sxs-lookup"><span data-stu-id="17da0-132">Add dimension groups</span></span>
1. <span data-ttu-id="17da0-133">在**操作窗格**上，单击**产品**。</span><span class="sxs-lookup"><span data-stu-id="17da0-133">On the **Action Pane**, click **Product**.</span></span>
2. <span data-ttu-id="17da0-134">单击**维度组**以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="17da0-134">Click **Dimension groups** to open the drop dialog.</span></span>
3. <span data-ttu-id="17da0-135">在**存储维度组**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="17da0-135">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="17da0-136">存储维度帮助您控制物料存储方式和库存提取方式。</span><span class="sxs-lookup"><span data-stu-id="17da0-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="17da0-137">例如，存储维度可包括站点和仓库。</span><span class="sxs-lookup"><span data-stu-id="17da0-137">For example, a storage dimension can include Site and Warehouse.</span></span>
4. <span data-ttu-id="17da0-138">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="17da0-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="17da0-139">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="17da0-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="17da0-140">在**跟踪维度组**字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="17da0-140">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="17da0-141">跟踪维度组确定可以添加到产品中的跟踪维度。</span><span class="sxs-lookup"><span data-stu-id="17da0-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="17da0-142">例如，批号和序列号用于跟踪库存物料。</span><span class="sxs-lookup"><span data-stu-id="17da0-142">For example, the batch number and serial number are used to track inventory items.</span></span>
7. <span data-ttu-id="17da0-143">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="17da0-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="17da0-144">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="17da0-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="17da0-145">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="17da0-145">Click **OK**.</span></span>
10. <span data-ttu-id="17da0-146">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="17da0-146">Click **Save**.</span></span>
11. <span data-ttu-id="17da0-147">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="17da0-147">Close the page.</span></span>


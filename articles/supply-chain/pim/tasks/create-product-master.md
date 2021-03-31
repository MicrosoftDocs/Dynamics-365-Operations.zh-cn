---
title: 创建基础产品
description: 为预定义变型创建基础产品。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d580d323409d84bab66dc03d39e084f5ee0cfc64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218481"
---
# <a name="create-a-product-master"></a><span data-ttu-id="520fd-103">创建基础产品</span><span class="sxs-lookup"><span data-stu-id="520fd-103">Create a product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="520fd-104">为预定义变型创建基础产品。</span><span class="sxs-lookup"><span data-stu-id="520fd-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="520fd-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="520fd-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="520fd-106">此过程专门针对产品设计人员。</span><span class="sxs-lookup"><span data-stu-id="520fd-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="520fd-107">新建基础产品</span><span class="sxs-lookup"><span data-stu-id="520fd-107">Create a new product master</span></span>
1. <span data-ttu-id="520fd-108">转到 **导航窗格 > 模块 > 产品信息管理 > 产品 > 基础产品**。</span><span class="sxs-lookup"><span data-stu-id="520fd-108">Go to **Navigation pane > Modules > Product information management > Products > Product masters**.</span></span>
2. <span data-ttu-id="520fd-109">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="520fd-109">Click **New**.</span></span>
3. <span data-ttu-id="520fd-110">在 **产品编号** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="520fd-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="520fd-111">其编号必须是唯一的。</span><span class="sxs-lookup"><span data-stu-id="520fd-111">The number must be unique.</span></span> <span data-ttu-id="520fd-112">可在 **产品编号** 字段设置编号规则。</span><span class="sxs-lookup"><span data-stu-id="520fd-112">A number sequence can be set for the **Product number** field.</span></span> <span data-ttu-id="520fd-113">在这种情况下，用户不必输入一个值。</span><span class="sxs-lookup"><span data-stu-id="520fd-113">In this case, the user doesn't have to enter a value.</span></span>
4. <span data-ttu-id="520fd-114">在 **产品名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="520fd-114">In the **Product name** field, type a value.</span></span> <span data-ttu-id="520fd-115">输入产品的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="520fd-115">Enter a descriptive product name.</span></span> <span data-ttu-id="520fd-116">该值默认为搜索名称，不过用户可以更改。</span><span class="sxs-lookup"><span data-stu-id="520fd-116">The value defaults to the search name, but this can be changed by the user.</span></span>
5. <span data-ttu-id="520fd-117">在 **产品维度组** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="520fd-117">In the **Product dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="520fd-118">产品维度组确定可用于创建产品变型的 4 个产品维度。</span><span class="sxs-lookup"><span data-stu-id="520fd-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="520fd-119">此示例使用颜色和大小组。</span><span class="sxs-lookup"><span data-stu-id="520fd-119">This example uses a group with color and size.</span></span>
6. <span data-ttu-id="520fd-120">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="520fd-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="520fd-121">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="520fd-121">In the list, click the link in the selected row.</span></span> <span data-ttu-id="520fd-122">默认 **配置技术** 是“预定义变型”。</span><span class="sxs-lookup"><span data-stu-id="520fd-122">The default **Configuration technology** is 'Predefined variant'.</span></span> <span data-ttu-id="520fd-123">这将在此示例中使用。</span><span class="sxs-lookup"><span data-stu-id="520fd-123">This will be used for this example.</span></span>
8. <span data-ttu-id="520fd-124">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="520fd-124">Click **OK**.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="520fd-125">选择产品维度组</span><span class="sxs-lookup"><span data-stu-id="520fd-125">Select product dimension groups</span></span>
1. <span data-ttu-id="520fd-126">在 **颜色组** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="520fd-126">In the **Color group** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="520fd-127">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="520fd-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="520fd-128">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="520fd-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="520fd-129">在 **大小组** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="520fd-129">In the **Size group** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="520fd-130">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="520fd-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="520fd-131">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="520fd-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="520fd-132">添加维度组</span><span class="sxs-lookup"><span data-stu-id="520fd-132">Add dimension groups</span></span>
1. <span data-ttu-id="520fd-133">在 **操作窗格** 上，单击 **产品**。</span><span class="sxs-lookup"><span data-stu-id="520fd-133">On the **Action Pane**, click **Product**.</span></span>
2. <span data-ttu-id="520fd-134">单击 **维度组** 以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="520fd-134">Click **Dimension groups** to open the drop dialog.</span></span>
3. <span data-ttu-id="520fd-135">在 **存储维度组** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="520fd-135">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="520fd-136">存储维度帮助您控制物料存储方式和库存提取方式。</span><span class="sxs-lookup"><span data-stu-id="520fd-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="520fd-137">例如，存储维度可包括站点和仓库。</span><span class="sxs-lookup"><span data-stu-id="520fd-137">For example, a storage dimension can include Site and Warehouse.</span></span>
4. <span data-ttu-id="520fd-138">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="520fd-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="520fd-139">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="520fd-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="520fd-140">在 **跟踪维度组** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="520fd-140">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="520fd-141">跟踪维度组确定可以添加到产品中的跟踪维度。</span><span class="sxs-lookup"><span data-stu-id="520fd-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="520fd-142">例如，批号和序列号用于跟踪库存物料。</span><span class="sxs-lookup"><span data-stu-id="520fd-142">For example, the batch number and serial number are used to track inventory items.</span></span>
7. <span data-ttu-id="520fd-143">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="520fd-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="520fd-144">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="520fd-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="520fd-145">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="520fd-145">Click **OK**.</span></span>
10. <span data-ttu-id="520fd-146">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="520fd-146">Click **Save**.</span></span>
11. <span data-ttu-id="520fd-147">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="520fd-147">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
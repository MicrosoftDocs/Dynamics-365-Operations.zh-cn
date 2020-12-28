---
title: 创建产品分类的层次结构
description: 该过程会显示如何创建新类别层次结构，和分配商品代码层次结构类型。
author: ShylaThompson
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, EcoResProductCategory, EcoResCategorySearchList, EcoResCategoryHierarchyFactbox, EcoResCategoryFriendlyName, EcoResCategoryAddProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 439df63a4f8f0cc1c030554d18f80e9934c88b00
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423000"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="07621-103">创建产品分类的层次结构</span><span class="sxs-lookup"><span data-stu-id="07621-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07621-104">该过程会显示如何创建新类别层次结构，和分配商品代码层次结构类型。</span><span class="sxs-lookup"><span data-stu-id="07621-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="07621-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="07621-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="07621-106">该过程专门面向类别经理。</span><span class="sxs-lookup"><span data-stu-id="07621-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="07621-107">创建新类别层次结构</span><span class="sxs-lookup"><span data-stu-id="07621-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="07621-108">转到 **导航窗格 > 模块 > 产品信息管理 > 设置 > 类别和属性 > 类别层次结构**。</span><span class="sxs-lookup"><span data-stu-id="07621-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="07621-109">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="07621-109">Click **New**.</span></span>
3. <span data-ttu-id="07621-110">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="07621-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="07621-111">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="07621-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="07621-112">单击 **创建**。</span><span class="sxs-lookup"><span data-stu-id="07621-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="07621-113">建立层次结构</span><span class="sxs-lookup"><span data-stu-id="07621-113">Build the hierarchy</span></span>
1. <span data-ttu-id="07621-114">单击 **新** 类别节点。</span><span class="sxs-lookup"><span data-stu-id="07621-114">Click **New** category node.</span></span>
2. <span data-ttu-id="07621-115">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="07621-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="07621-116">在 **代码** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="07621-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="07621-117">在 **易记名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="07621-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="07621-118">单击 **新** 类别节点。</span><span class="sxs-lookup"><span data-stu-id="07621-118">Click **New** category node.</span></span>
6. <span data-ttu-id="07621-119">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="07621-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="07621-120">在 **代码** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="07621-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="07621-121">在 **易记名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="07621-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="07621-122">单击 **新** 类别节点。</span><span class="sxs-lookup"><span data-stu-id="07621-122">Click **New** category node.</span></span>
10. <span data-ttu-id="07621-123">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="07621-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="07621-124">在 **代码** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="07621-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="07621-125">在 **易记名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="07621-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="07621-126">单击 **新** 类别节点。</span><span class="sxs-lookup"><span data-stu-id="07621-126">Click **New** category node.</span></span>
14. <span data-ttu-id="07621-127">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="07621-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="07621-128">在 **代码** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="07621-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="07621-129">在 **易记名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="07621-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="07621-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="07621-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="07621-131">对层次结构进行分类</span><span class="sxs-lookup"><span data-stu-id="07621-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="07621-132">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="07621-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="07621-133">在 **操作窗格** 上单击 **类别层次结构**。</span><span class="sxs-lookup"><span data-stu-id="07621-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="07621-134">单击 **关联层次结构类型**。</span><span class="sxs-lookup"><span data-stu-id="07621-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="07621-135">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="07621-135">Click **New**.</span></span>
5. <span data-ttu-id="07621-136">在 **类别层次结构类型** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="07621-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="07621-137">选择 **用于产品分类的商品代码类别层次结构类型**。</span><span class="sxs-lookup"><span data-stu-id="07621-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="07621-138">在 **类别层次结构** 字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="07621-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="07621-139">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="07621-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="07621-140">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="07621-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="07621-141">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="07621-141">Close the page.</span></span>


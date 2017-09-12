--- 
title: "为预定义的产品变型创建产品编号"
description: "此指南显示如何为预定义的产品变型设置产品编号命名法，以及如何将其分配给适当的产品维度组。"
author: BibiSp
manager: AnnBe
ms.date: 09/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6294e4608b31c37aa713e3a7a2028b409b5a8366
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a><span data-ttu-id="daa08-103">为预定义的产品变型创建产品编号</span><span class="sxs-lookup"><span data-stu-id="daa08-103">Create a product number for predefined product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="daa08-104">此指南显示如何为预定义的产品变型设置产品编号命名法，以及如何将其分配给适当的产品维度组。</span><span class="sxs-lookup"><span data-stu-id="daa08-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="daa08-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="daa08-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="daa08-106">将为“颜色和大小”产品维度组分配新产品编号命名法。</span><span class="sxs-lookup"><span data-stu-id="daa08-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="daa08-107">此任务通常由产品设计师完成。</span><span class="sxs-lookup"><span data-stu-id="daa08-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="daa08-108">创建产品编号命名法</span><span class="sxs-lookup"><span data-stu-id="daa08-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="daa08-109">单击“产品变型模型定义”。</span><span class="sxs-lookup"><span data-stu-id="daa08-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="daa08-110">单击“产品命名法”。</span><span class="sxs-lookup"><span data-stu-id="daa08-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="daa08-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="daa08-111">Click New.</span></span>
4. <span data-ttu-id="daa08-112">在"名称"字段中，输入可帮助识别目标产品维度组的命名法名称，如 ColorSize。</span><span class="sxs-lookup"><span data-stu-id="daa08-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="daa08-113">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="daa08-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="daa08-114">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="daa08-114">Click Add.</span></span>
7. <span data-ttu-id="daa08-115">单击“基础产品编号”。</span><span class="sxs-lookup"><span data-stu-id="daa08-115">Click Product master number.</span></span>
8. <span data-ttu-id="daa08-116">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="daa08-116">Click Add.</span></span>
9. <span data-ttu-id="daa08-117">单击“文本常量”。</span><span class="sxs-lookup"><span data-stu-id="daa08-117">Click Text constant.</span></span>
10. <span data-ttu-id="daa08-118">在“文本”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="daa08-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="daa08-119">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="daa08-119">Click Add.</span></span>
12. <span data-ttu-id="daa08-120">单击“颜色”。</span><span class="sxs-lookup"><span data-stu-id="daa08-120">Click Color.</span></span>
13. <span data-ttu-id="daa08-121">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="daa08-121">Click Add.</span></span>
14. <span data-ttu-id="daa08-122">单击“文本常量”。</span><span class="sxs-lookup"><span data-stu-id="daa08-122">Click Text constant.</span></span>
15. <span data-ttu-id="daa08-123">在“文本”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="daa08-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="daa08-124">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="daa08-124">Click Add.</span></span>
17. <span data-ttu-id="daa08-125">单击"大小"。</span><span class="sxs-lookup"><span data-stu-id="daa08-125">Click Size.</span></span>
18. <span data-ttu-id="daa08-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="daa08-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="daa08-127">为基础产品分配命名法</span><span class="sxs-lookup"><span data-stu-id="daa08-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="daa08-128">单击“产品维度组”。</span><span class="sxs-lookup"><span data-stu-id="daa08-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="daa08-129">选择“SizeCol”产品维度组。</span><span class="sxs-lookup"><span data-stu-id="daa08-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="daa08-130">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="daa08-130">Click Edit.</span></span>
4. <span data-ttu-id="daa08-131">在“使用命名法”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="daa08-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="daa08-132">在“产品变型编号命名法”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="daa08-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="daa08-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="daa08-133">Close the page.</span></span>



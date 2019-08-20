---
title: 为预定义的产品变型创建产品编号命名法
description: 此指南显示如何为预定义的产品变型设置产品编号命名法，以及如何将其分配给适当的产品维度组。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a2e61fd99cb80a1a9cc3d8e985fb0f14e3c2fc2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844673"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="c1714-103">为预定义的产品变型创建产品编号命名法</span><span class="sxs-lookup"><span data-stu-id="c1714-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c1714-104">此指南显示如何为预定义的产品变型设置产品编号命名法，以及如何将其分配给适当的产品维度组。</span><span class="sxs-lookup"><span data-stu-id="c1714-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="c1714-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="c1714-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c1714-106">将为“颜色和大小”产品维度组分配新产品编号命名法。</span><span class="sxs-lookup"><span data-stu-id="c1714-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="c1714-107">此任务通常由产品设计师完成。</span><span class="sxs-lookup"><span data-stu-id="c1714-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="c1714-108">创建产品编号命名法</span><span class="sxs-lookup"><span data-stu-id="c1714-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="c1714-109">单击“产品变型模型定义”。</span><span class="sxs-lookup"><span data-stu-id="c1714-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="c1714-110">单击“产品命名法”。</span><span class="sxs-lookup"><span data-stu-id="c1714-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="c1714-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="c1714-111">Click New.</span></span>
4. <span data-ttu-id="c1714-112">在"名称"字段中，输入可帮助识别目标产品维度组的命名法名称，如 ColorSize。</span><span class="sxs-lookup"><span data-stu-id="c1714-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="c1714-113">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c1714-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="c1714-114">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c1714-114">Click Add.</span></span>
7. <span data-ttu-id="c1714-115">单击“基础产品编号”。</span><span class="sxs-lookup"><span data-stu-id="c1714-115">Click Product master number.</span></span>
8. <span data-ttu-id="c1714-116">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c1714-116">Click Add.</span></span>
9. <span data-ttu-id="c1714-117">单击“文本常量”。</span><span class="sxs-lookup"><span data-stu-id="c1714-117">Click Text constant.</span></span>
10. <span data-ttu-id="c1714-118">在“文本”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c1714-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="c1714-119">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c1714-119">Click Add.</span></span>
12. <span data-ttu-id="c1714-120">单击“颜色”。</span><span class="sxs-lookup"><span data-stu-id="c1714-120">Click Color.</span></span>
13. <span data-ttu-id="c1714-121">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c1714-121">Click Add.</span></span>
14. <span data-ttu-id="c1714-122">单击“文本常量”。</span><span class="sxs-lookup"><span data-stu-id="c1714-122">Click Text constant.</span></span>
15. <span data-ttu-id="c1714-123">在“文本”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c1714-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="c1714-124">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c1714-124">Click Add.</span></span>
17. <span data-ttu-id="c1714-125">单击"大小"。</span><span class="sxs-lookup"><span data-stu-id="c1714-125">Click Size.</span></span>
18. <span data-ttu-id="c1714-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c1714-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="c1714-127">为基础产品分配命名法</span><span class="sxs-lookup"><span data-stu-id="c1714-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="c1714-128">单击“产品维度组”。</span><span class="sxs-lookup"><span data-stu-id="c1714-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="c1714-129">选择“SizeCol”产品维度组。</span><span class="sxs-lookup"><span data-stu-id="c1714-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="c1714-130">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="c1714-130">Click Edit.</span></span>
4. <span data-ttu-id="c1714-131">在“使用命名法”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="c1714-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="c1714-132">在“产品变型编号命名法”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c1714-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="c1714-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c1714-133">Close the page.</span></span>


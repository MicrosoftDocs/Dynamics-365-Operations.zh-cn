---
title: 为预定义的产品变型创建产品编号命名法
description: 本主题介绍如何为预定义的产品变型设置产品编号命名法，以及如何将其分配给适当的产品维度组。
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c69dc3f8e70c3b0a760f54d2251757ac997a432
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841615"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="f0ec5-103">为预定义的产品变型创建产品编号命名法</span><span class="sxs-lookup"><span data-stu-id="f0ec5-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f0ec5-104">本主题介绍如何为预定义的产品变型设置产品编号命名法，以及如何将其分配给适当的产品维度组。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="f0ec5-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f0ec5-106">将为“颜色和大小”产品维度组分配新产品编号命名法。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="f0ec5-107">此任务通常由产品设计师完成。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="f0ec5-108">创建产品编号命名法</span><span class="sxs-lookup"><span data-stu-id="f0ec5-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="f0ec5-109">选择 **产品变型定义**。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="f0ec5-110">选择 **产品命名法**。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="f0ec5-111">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-111">Select **New**.</span></span>
4. <span data-ttu-id="f0ec5-112">在 **名称** 字段中，输入可帮助识别目标产品维度组的命名法名称，如 `ColorSize`。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="f0ec5-113">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="f0ec5-114">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-114">Select **Add**.</span></span>
7. <span data-ttu-id="f0ec5-115">选择 **基础产品** 编号。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="f0ec5-116">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-116">Select **Add**.</span></span>
9. <span data-ttu-id="f0ec5-117">选择 **文本常量**。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="f0ec5-118">在 **文本** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="f0ec5-119">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-119">Select **Add**.</span></span>
12. <span data-ttu-id="f0ec5-120">选择 **颜色**。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-120">Select **Color**.</span></span>
13. <span data-ttu-id="f0ec5-121">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-121">Select **Add**.</span></span>
14. <span data-ttu-id="f0ec5-122">选择 **文本常量**。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="f0ec5-123">在 **文本** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="f0ec5-124">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-124">Select **Add**.</span></span>
17. <span data-ttu-id="f0ec5-125">选择 **大小**。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-125">Select **Size**.</span></span>
18. <span data-ttu-id="f0ec5-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="f0ec5-127">为基础产品分配命名法</span><span class="sxs-lookup"><span data-stu-id="f0ec5-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="f0ec5-128">选择 **产品维度组**。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="f0ec5-129">选择 **SizeCol 产品维度组**。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="f0ec5-130">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-130">Select **Edit**.</span></span>
4. <span data-ttu-id="f0ec5-131">在 **使用命名法** 字段中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="f0ec5-132">在 **产品变型编号命名法** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="f0ec5-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f0ec5-133">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
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
ms.openlocfilehash: 4bb73854f52525c0722683086d1b4f1dd7173306
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920649"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="902f1-103">为预定义的产品变型创建产品编号命名法</span><span class="sxs-lookup"><span data-stu-id="902f1-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="902f1-104">本主题介绍如何为预定义的产品变型设置产品编号命名法，以及如何将其分配给适当的产品维度组。</span><span class="sxs-lookup"><span data-stu-id="902f1-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="902f1-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="902f1-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="902f1-106">将为“颜色和大小”产品维度组分配新产品编号命名法。</span><span class="sxs-lookup"><span data-stu-id="902f1-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="902f1-107">此任务通常由产品设计师完成。</span><span class="sxs-lookup"><span data-stu-id="902f1-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="902f1-108">创建产品编号命名法</span><span class="sxs-lookup"><span data-stu-id="902f1-108">Create a product number nomenclature</span></span>

1. <span data-ttu-id="902f1-109">转到 **产品信息管理 \> 设置 \> 产品命名法**。</span><span class="sxs-lookup"><span data-stu-id="902f1-109">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="902f1-110">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="902f1-110">Select **New**.</span></span>
1. <span data-ttu-id="902f1-111">在 **名称** 字段中，输入可帮助识别目标产品维度组的命名法名称，如 `ColorSize`。</span><span class="sxs-lookup"><span data-stu-id="902f1-111">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
1. <span data-ttu-id="902f1-112">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="902f1-112">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="902f1-113">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="902f1-113">Select **Add**.</span></span>
1. <span data-ttu-id="902f1-114">选择 **基础产品** 编号。</span><span class="sxs-lookup"><span data-stu-id="902f1-114">Select **Product master** number.</span></span>
1. <span data-ttu-id="902f1-115">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="902f1-115">Select **Add**.</span></span>
1. <span data-ttu-id="902f1-116">选择 **文本常量**。</span><span class="sxs-lookup"><span data-stu-id="902f1-116">Select **Text constant**.</span></span>
1. <span data-ttu-id="902f1-117">在 **文本** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="902f1-117">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="902f1-118">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="902f1-118">Select **Add**.</span></span>
1. <span data-ttu-id="902f1-119">选择 **颜色**。</span><span class="sxs-lookup"><span data-stu-id="902f1-119">Select **Color**.</span></span>
1. <span data-ttu-id="902f1-120">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="902f1-120">Select **Add**.</span></span>
1. <span data-ttu-id="902f1-121">选择 **文本常量**。</span><span class="sxs-lookup"><span data-stu-id="902f1-121">Select **Text constant**.</span></span>
1. <span data-ttu-id="902f1-122">在 **文本** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="902f1-122">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="902f1-123">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="902f1-123">Select **Add**.</span></span>
1. <span data-ttu-id="902f1-124">选择 **大小**。</span><span class="sxs-lookup"><span data-stu-id="902f1-124">Select **Size**.</span></span>
1. <span data-ttu-id="902f1-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="902f1-125">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="902f1-126">为基础产品分配命名法</span><span class="sxs-lookup"><span data-stu-id="902f1-126">Assign the nomenclature to a product master</span></span>

1. <span data-ttu-id="902f1-127">选择 **产品维度组**。</span><span class="sxs-lookup"><span data-stu-id="902f1-127">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="902f1-128">选择 **SizeCol 产品维度组**。</span><span class="sxs-lookup"><span data-stu-id="902f1-128">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="902f1-129">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="902f1-129">Select **Edit**.</span></span>
4. <span data-ttu-id="902f1-130">在 **使用命名法** 字段中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="902f1-130">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="902f1-131">在 **产品变型编号命名法** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="902f1-131">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="902f1-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="902f1-132">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
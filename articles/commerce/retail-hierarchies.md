---
title: Commerce 层次结构
description: 本文介绍 Dynamics 365 Commerce 中的层次结构。
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
audience: Application User
ms.reviewer: josaw
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 94b391ab5028f76debb75d25ac9469e25361cb12
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979608"
---
# <a name="commerce-hierarchies"></a><span data-ttu-id="866b0-103">Commerce 层次结构</span><span class="sxs-lookup"><span data-stu-id="866b0-103">Commerce hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="866b0-104">本文介绍 Dynamics 365 Commerce 中的层次结构。</span><span class="sxs-lookup"><span data-stu-id="866b0-104">This article describes hierarchies in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="866b0-105">您可以创建类别层次结构来组织通过渠道销售的产品。</span><span class="sxs-lookup"><span data-stu-id="866b0-105">You can create a category hierarchy to organize the products that you sell through your channels.</span></span> <span data-ttu-id="866b0-106">您可以使用产品层次结构来对产品进行分类或分组。</span><span class="sxs-lookup"><span data-stu-id="866b0-106">You can use product hierarchies to categorize or group products.</span></span> <span data-ttu-id="866b0-107">然后，可以使用这些产品来创建产品分类和客户会员计划。</span><span class="sxs-lookup"><span data-stu-id="866b0-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="866b0-108">您还可以分配产品特性和属性，分配定价结构，将产品包括在产品促销中，以及将产品用于报告。</span><span class="sxs-lookup"><span data-stu-id="866b0-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="866b0-109">您可以创建一个类别层次结构以表示组织中的所有产品和类别，然后为多个目的使用该类别层次结构。</span><span class="sxs-lookup"><span data-stu-id="866b0-109">You can create one category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="866b0-110">或者，您可以为特殊用途创建多个类别层次结构，例如产品促销。</span><span class="sxs-lookup"><span data-stu-id="866b0-110">Alternatively, you can create multiple category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="866b0-111">在创建产品层次结构时，必须分配类别层次结构类型以标识类别层次结构的用途。</span><span class="sxs-lookup"><span data-stu-id="866b0-111">When you create a product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="866b0-112">例如，仅当您在线或在销售点 (POS) 按类别浏览产品时，分配了 **商业导航层次结构** 类型的产品层次结构才会被引用。</span><span class="sxs-lookup"><span data-stu-id="866b0-112">For example, only product hierarchies that are assigned the **Commerce navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="hierarchy-types"></a><span data-ttu-id="866b0-113">层次结构类型</span><span class="sxs-lookup"><span data-stu-id="866b0-113">Hierarchy types</span></span>

<span data-ttu-id="866b0-114">下表列出了可用的类别层次结构的类型以及每个类型的一般用途。</span><span class="sxs-lookup"><span data-stu-id="866b0-114">The following table lists the types of category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="866b0-115">类别层次结构类型</span><span class="sxs-lookup"><span data-stu-id="866b0-115">Category hierarchy type</span></span>       | <span data-ttu-id="866b0-116">目的</span><span class="sxs-lookup"><span data-stu-id="866b0-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="866b0-117">产品层次结构</span><span class="sxs-lookup"><span data-stu-id="866b0-117">Product hierarchy</span></span>      | <span data-ttu-id="866b0-118">使用此层次结构类型定义您的组织的整个产品层次结构。</span><span class="sxs-lookup"><span data-stu-id="866b0-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="866b0-119">您可以为促销活动，定价和促销、报告和分类计划使用此层次结构类型。</span><span class="sxs-lookup"><span data-stu-id="866b0-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="866b0-120">只有一个产品层次结构可以分配此层次结构类型。</span><span class="sxs-lookup"><span data-stu-id="866b0-120">Only one product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="866b0-121">补充层次结构</span><span class="sxs-lookup"><span data-stu-id="866b0-121">Supplemental hierarchy</span></span> | <span data-ttu-id="866b0-122">为您要创建的任何附加类别层次结构使用此层次结构类型。</span><span class="sxs-lookup"><span data-stu-id="866b0-122">Use this hierarchy type for any additional category hierarchies that you want to create.</span></span> <span data-ttu-id="866b0-123">例如，在春天，有游泳衣的促销。</span><span class="sxs-lookup"><span data-stu-id="866b0-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="866b0-124">因此，您可以在单独的类别层次结构包括您的游泳衣产品并应用促销价到不同产品类别。</span><span class="sxs-lookup"><span data-stu-id="866b0-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="866b0-125">导航层次结构</span><span class="sxs-lookup"><span data-stu-id="866b0-125">Navigation hierarchy</span></span>   | <span data-ttu-id="866b0-126">使用此层次结构类型可将产品分组并组织到类别，以便在线或在 POS 中浏览产品。</span><span class="sxs-lookup"><span data-stu-id="866b0-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="866b0-127">通过使用类别层次结构组织产品，可以在类别级别设置和维护产品属性和特性。</span><span class="sxs-lookup"><span data-stu-id="866b0-127">By using a category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="866b0-128">这些特性和属性包括产品维度和 POS 设置。</span><span class="sxs-lookup"><span data-stu-id="866b0-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="866b0-129">自动分配给类别的所有产品继承您定义的属性和属性。</span><span class="sxs-lookup"><span data-stu-id="866b0-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="866b0-130">您可以在所选类别的多个产品中同时复制所有产品的属性设置。</span><span class="sxs-lookup"><span data-stu-id="866b0-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>

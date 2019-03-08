---
title: 设置零售产品
description: 本文介绍如何在 Microsoft Dynamics 365 for Retail 中设置零售产品。
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailProductAndCategoryWorkspace, EcoResProductDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 991546424a95463315eaa73c2776d0defe66def5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "357396"
---
# <a name="set-up-retail-products"></a><span data-ttu-id="b9c28-103">设置零售产品</span><span class="sxs-lookup"><span data-stu-id="b9c28-103">Set up retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b9c28-104">本文介绍如何在 Microsoft Dynamics 365 for Retail 中设置零售产品。</span><span class="sxs-lookup"><span data-stu-id="b9c28-104">This article describes how to set up retail products in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="b9c28-105">您必须在 Dynamics 365 for Retail 中创建和配置产品，然后才能将产品投入零售渠道中转售。</span><span class="sxs-lookup"><span data-stu-id="b9c28-105">Before you can offer products for resale in your retail channels, you must create and configure the products in Dynamics 365 for Retail.</span></span> <span data-ttu-id="b9c28-106">零售在 Dynamics 365 for Retail 中使用产品功能来创建基础产品中的组织产品。</span><span class="sxs-lookup"><span data-stu-id="b9c28-106">Retail uses the product features in Dynamics 365 for Retail to create organization-wide products in the product master.</span></span> <span data-ttu-id="b9c28-107">您可以创建产品，定义产品属性和特性和分配到零售类别层次结构。</span><span class="sxs-lookup"><span data-stu-id="b9c28-107">You can create the products, define the product properties and attributes, and assign the products to retail category hierarchies.</span></span> <span data-ttu-id="b9c28-108">若要使产品在零售通道中可用和添加到有效的分类，您必须发放到产品中可用的法人。</span><span class="sxs-lookup"><span data-stu-id="b9c28-108">To make the products available to your retail channels and add them to an active assortment, you must release the products to the legal entities where they are available.</span></span> <span data-ttu-id="b9c28-109">若要通过使用零售渠道销售产品，请完成以下任务。</span><span class="sxs-lookup"><span data-stu-id="b9c28-109">To set up the products that you sell by using retail channels, complete the following tasks.</span></span>

1. <span data-ttu-id="b9c28-110">定义零售产品层次结构。</span><span class="sxs-lookup"><span data-stu-id="b9c28-110">Define a retail product hierarchy.</span></span> <span data-ttu-id="b9c28-111">通过使用在 Dynamics 365 for Retail 中的类别层次结构功能，您可以定义零售类别层次结构分组和分类您分配给零售渠道的产品。</span><span class="sxs-lookup"><span data-stu-id="b9c28-111">By using the category hierarchy features in Dynamics 365 for Retail, you can define retail category hierarchies to group and categorize the products that you distribute to your retail channels.</span></span> <span data-ttu-id="b9c28-112">用户定义和系统特性可以在类别级别定义。</span><span class="sxs-lookup"><span data-stu-id="b9c28-112">User-defined and system attributes can be defined at the category level.</span></span> <span data-ttu-id="b9c28-113">然后，分配给类别的所有产品继承这些特性。</span><span class="sxs-lookup"><span data-stu-id="b9c28-113">Then, all products that are assigned to the category inherit those attributes.</span></span> <span data-ttu-id="b9c28-114">可以定义多个类别层次结构，并且每个产品可以分配给多个层次结构。</span><span class="sxs-lookup"><span data-stu-id="b9c28-114">Multiple category hierarchies can be defined, and each product can be assigned to multiple hierarchies.</span></span> <span data-ttu-id="b9c28-115">不过，在单个层次结构，每个产品只能分配到一个类别。</span><span class="sxs-lookup"><span data-stu-id="b9c28-115">However, in a single hierarchy, each product can be assigned to only one category.</span></span>
2. <span data-ttu-id="b9c28-116">添加产品和产品变型到基础产品。</span><span class="sxs-lookup"><span data-stu-id="b9c28-116">Add products and product variants to the product master.</span></span> <span data-ttu-id="b9c28-117">产品添加到基础产品表示产品的全局列表。</span><span class="sxs-lookup"><span data-stu-id="b9c28-117">Products that are added to the product master represent a global list of products.</span></span> <span data-ttu-id="b9c28-118">您可以手动添加产品，一次一个，或可以从供应商导入产品数据。</span><span class="sxs-lookup"><span data-stu-id="b9c28-118">You can add products manually, one at a time, or you can import product data from your vendors.</span></span>
3. <span data-ttu-id="b9c28-119">向法人发布产品。</span><span class="sxs-lookup"><span data-stu-id="b9c28-119">Release the products to legal entities.</span></span> <span data-ttu-id="b9c28-120">已发放到的那些法人产品在您的零售渠道可用。</span><span class="sxs-lookup"><span data-stu-id="b9c28-120">Only products that have been released to legal entities can be made available to your retail channels.</span></span> <span data-ttu-id="b9c28-121">在您第一次定义产品时，您可以定义它在组织级别。</span><span class="sxs-lookup"><span data-stu-id="b9c28-121">When you first define a product, you define it on an organization-wide level.</span></span> <span data-ttu-id="b9c28-122">可以选择发放产品到一个或多个法人。</span><span class="sxs-lookup"><span data-stu-id="b9c28-122">You can then select one or more legal entities to release the product to.</span></span> <span data-ttu-id="b9c28-123">产品然后将可用于跨您的组织的多个零售渠道。</span><span class="sxs-lookup"><span data-stu-id="b9c28-123">The product then becomes available to multiple retail channels across your organization.</span></span> <span data-ttu-id="b9c28-124">您可以使用此功能创建产品一次，在一个位置添加和更新产品特性和属性，然后跨组织将产品分发到可用的零售渠道。</span><span class="sxs-lookup"><span data-stu-id="b9c28-124">You can use this functionality to create a product one time, add and update product attributes and properties in one place, and then distribute the product across your organization, to the retail channels where it's available.</span></span>
4. <span data-ttu-id="b9c28-125">将产品添加到分类。</span><span class="sxs-lookup"><span data-stu-id="b9c28-125">Add products to assortments.</span></span> <span data-ttu-id="b9c28-126">分类表示在零售渠道提供产品的集合。</span><span class="sxs-lookup"><span data-stu-id="b9c28-126">An assortment represents a collection of products that you offer in your retail channels.</span></span> <span data-ttu-id="b9c28-127">您可以定义一个或多个分类，并且每个产品可以分配给一个或多个分类。</span><span class="sxs-lookup"><span data-stu-id="b9c28-127">You can define one or more assortments, and each product can be assigned to one or more assortments.</span></span> <span data-ttu-id="b9c28-128">要分配产品到零售渠道，则分配分类到这些零售渠道。</span><span class="sxs-lookup"><span data-stu-id="b9c28-128">To assign products to retail channels, you assign the assortments to those retail channels.</span></span> <span data-ttu-id="b9c28-129">创建分类时，您可以添加尚未发放到法人的产品。</span><span class="sxs-lookup"><span data-stu-id="b9c28-129">When you create an assortment, you can add products that haven't yet been released to a legal entity.</span></span> <span data-ttu-id="b9c28-130">但是，这些产品可以在零售渠道可用前，您必须发放到产品到法人。</span><span class="sxs-lookup"><span data-stu-id="b9c28-130">However, you must release the products to a legal entity before those products can be made available to the retail channels.</span></span>
5. <span data-ttu-id="b9c28-131">将产品添加到导航层次结构。</span><span class="sxs-lookup"><span data-stu-id="b9c28-131">Add products to navigation hierarchies.</span></span> <span data-ttu-id="b9c28-132">在产品可在线或在销售点 (POS) 浏览之前，它们必须在零售导航层次结构中进行分类。</span><span class="sxs-lookup"><span data-stu-id="b9c28-132">Before products can be browsed online or in point of sale (POS), they must be categorized in a Retail navigation hierarchy.</span></span>
6. <span data-ttu-id="b9c28-133">将产品添加到目录。</span><span class="sxs-lookup"><span data-stu-id="b9c28-133">Add products to catalogs.</span></span> <span data-ttu-id="b9c28-134">尽管此步骤对 POS 是可选的，在线商店需要产品至少包含在一个目录中。</span><span class="sxs-lookup"><span data-stu-id="b9c28-134">Although this step is optional for POS, online stores require that products be included in at least one catalog.</span></span>

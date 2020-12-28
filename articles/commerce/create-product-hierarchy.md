---
title: 创建新产品层次结构
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新产品层次结构。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 724ec2e5af7837d574298d662911cd9c6ee9e9f2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410411"
---
# <a name="create-a-new-product-hierarchy"></a><span data-ttu-id="2b11f-103">创建新产品层次结构</span><span class="sxs-lookup"><span data-stu-id="2b11f-103">Create a new product hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2b11f-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新产品层次结构。</span><span class="sxs-lookup"><span data-stu-id="2b11f-104">This topic describes how to create a new product hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2b11f-105">概览</span><span class="sxs-lookup"><span data-stu-id="2b11f-105">Overview</span></span>

<span data-ttu-id="2b11f-106">Dynamics 365 Commerce 支持多种零售渠道。</span><span class="sxs-lookup"><span data-stu-id="2b11f-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="2b11f-107">这些零售渠道包括在线商店、呼叫中心和零售商店（亦称实体商店）。</span><span class="sxs-lookup"><span data-stu-id="2b11f-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="2b11f-108">每个零售商店渠道都可以有自己的付款方式、价格组、销售点 (POS) 收银机、收入帐户和支出帐户以及职员。</span><span class="sxs-lookup"><span data-stu-id="2b11f-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="2b11f-109">您必须先设置所有这些元素，然后才能创建零售商店渠道。</span><span class="sxs-lookup"><span data-stu-id="2b11f-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="2b11f-110">商业产品层次结构用于定义您的组织的整个产品层次结构。</span><span class="sxs-lookup"><span data-stu-id="2b11f-110">A Commerce product hierarchy is used to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="2b11f-111">您可以为促销活动、定价和促销、报告和分类计划使用此商业产品层次结构。</span><span class="sxs-lookup"><span data-stu-id="2b11f-111">You can use a Commerce product hierarchy for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="2b11f-112">只能为每个组织分配一个商业产品层次结构。</span><span class="sxs-lookup"><span data-stu-id="2b11f-112">Only one Commerce product hierarchy can be assigned per organization.</span></span>

## <a name="create-and-configure-a-product-hierarchy"></a><span data-ttu-id="2b11f-113">创建和配置产品层次结构</span><span class="sxs-lookup"><span data-stu-id="2b11f-113">Create and configure a product hierarchy</span></span>

<span data-ttu-id="2b11f-114">要创建和配置商业产品层次结构，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2b11f-114">To create and configure a Commerce product hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="2b11f-115">在导航窗格中，转到 **模块 \> Retail 和 Commerce \> 产品和类别 \> 商业产品层次结构**。</span><span class="sxs-lookup"><span data-stu-id="2b11f-115">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="2b11f-116">如果还不存在层次结构，则在 **操作窗格** 上选择 **新建** 以创建层次结构的根。</span><span class="sxs-lookup"><span data-stu-id="2b11f-116">If no hierachy exists yet, on the **Action pane**, select **New** to create the root of the hierarchy.</span></span>
1. <span data-ttu-id="2b11f-117">在 **常规** 下面：</span><span class="sxs-lookup"><span data-stu-id="2b11f-117">Under **General**:</span></span>
    1. <span data-ttu-id="2b11f-118">在 **名称** 框中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="2b11f-118">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="2b11f-119">在 **描述** 框中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="2b11f-119">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="2b11f-120">在 **友好名称** 框中，输入友好名称。</span><span class="sxs-lookup"><span data-stu-id="2b11f-120">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="2b11f-121">将 **有效** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="2b11f-121">Set **Active** to **Yes**.</span></span>

## <a name="add-hierarchy-nodes"></a><span data-ttu-id="2b11f-122">添加层次结构节点</span><span class="sxs-lookup"><span data-stu-id="2b11f-122">Add hierarchy nodes</span></span>

<span data-ttu-id="2b11f-123">若要添加层次结构节点，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2b11f-123">To add hierarchy nodes, follow these steps.</span></span>

1. <span data-ttu-id="2b11f-124">在操作窗格上选择 **编辑类别层次结构**。</span><span class="sxs-lookup"><span data-stu-id="2b11f-124">On the action pane, select **Edit category hierarchy**.</span></span>
1. <span data-ttu-id="2b11f-125">选择要向其添加新节点的父节点，然后选择 **新类别节点**。</span><span class="sxs-lookup"><span data-stu-id="2b11f-125">Select the parent node you want to add a new node to, and then select **New category node**.</span></span>
1. <span data-ttu-id="2b11f-126">在 **常规** 部分中，提供 **名称**、**描述**、**友好名称** 和 **关键字**。</span><span class="sxs-lookup"><span data-stu-id="2b11f-126">In the **General** section provide a **Name**, **Description**, **Friendly name** and **Keywords**.</span></span>
1. <span data-ttu-id="2b11f-127">在 **常规** 下面：</span><span class="sxs-lookup"><span data-stu-id="2b11f-127">Under **General**:</span></span>
    1. <span data-ttu-id="2b11f-128">在 **名称** 框中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="2b11f-128">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="2b11f-129">在 **描述** 框中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="2b11f-129">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="2b11f-130">在 **友好名称** 框中，输入友好名称。</span><span class="sxs-lookup"><span data-stu-id="2b11f-130">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="2b11f-131">在 **关键字** 框中，输入相关关键字。</span><span class="sxs-lookup"><span data-stu-id="2b11f-131">In the **Keywords** box, enter relevant keywords.</span></span>
    1. <span data-ttu-id="2b11f-132">在 **显示顺序** 框中，输入显示顺序编号（可选）。</span><span class="sxs-lookup"><span data-stu-id="2b11f-132">In the **Display order** box, enter a number for the display order (optional).</span></span>
1. <span data-ttu-id="2b11f-133">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="2b11f-133">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="2b11f-134">重复上述步骤以添加其他节点。</span><span class="sxs-lookup"><span data-stu-id="2b11f-134">Repeat the steps above to add additional nodes.</span></span>

<span data-ttu-id="2b11f-135">下图显示了新产品层次结构节点的创建过程。</span><span class="sxs-lookup"><span data-stu-id="2b11f-135">The following image shows the creation of a new product hierarchy node.</span></span>

![创建产品层次结构](media/create-product-hierarchy.png)

## <a name="other-settings"></a><span data-ttu-id="2b11f-137">其他设置</span><span class="sxs-lookup"><span data-stu-id="2b11f-137">Other settings</span></span>

<span data-ttu-id="2b11f-138">类别属性组也可以根据需要分配给每个组。</span><span class="sxs-lookup"><span data-stu-id="2b11f-138">Category attribute groups can also be assigned to each group as required.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="2b11f-139">其他资源</span><span class="sxs-lookup"><span data-stu-id="2b11f-139">Additional resources</span></span>

[<span data-ttu-id="2b11f-140">Commerce 层次结构</span><span class="sxs-lookup"><span data-stu-id="2b11f-140">commerce hierarchies</span></span>](retail-hierarchies.md)

[<span data-ttu-id="2b11f-141">管理产品类别和产品</span><span class="sxs-lookup"><span data-stu-id="2b11f-141">Manage product categories and products </span></span>](category-management-product-creation.md)

[<span data-ttu-id="2b11f-142">更改促销实体的排序顺序</span><span class="sxs-lookup"><span data-stu-id="2b11f-142">Change the sort order for merchandizing entities</span></span>](custom-order-categories-nav-retail-prod-hierarchy.md)

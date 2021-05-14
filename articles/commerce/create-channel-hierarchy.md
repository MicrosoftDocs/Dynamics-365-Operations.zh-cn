---
title: 创建渠道导航层次结构
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建渠道导航层次结构。
author: samjarawan
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5df46de9dadfa0b7160a9b340ef36fdf963a0ad3
ms.sourcegitcommit: 6c2f5c3b038f696532c335e20b0fbafa155d6858
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951900"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="1a9f9-103">创建渠道导航层次结构</span><span class="sxs-lookup"><span data-stu-id="1a9f9-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1a9f9-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建渠道导航层次结构。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1a9f9-105">概览</span><span class="sxs-lookup"><span data-stu-id="1a9f9-105">Overview</span></span>

<span data-ttu-id="1a9f9-106">渠道导航层次结构用于按类别归组和组织产品，以便可以在线或在销售点 (POS) 中浏览产品。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="1a9f9-107">创建渠道导航层次结构</span><span class="sxs-lookup"><span data-stu-id="1a9f9-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="1a9f9-108">若要创建渠道导航层次结构，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="1a9f9-109">在导航窗格中，转到 **模块 \> Retail 和 Commerce \> 产品和类别 \> 渠道导航类别**。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="1a9f9-110">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="1a9f9-111">在 **名称** 框中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="1a9f9-112">在 **描述** 框中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="1a9f9-113">选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-113">Select **Create**.</span></span>
1. <span data-ttu-id="1a9f9-114">在操作窗格中，选择 **新类别节点** 以创建根节点。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="1a9f9-115">在 **名称** 框中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="1a9f9-116">在 **描述** 框中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="1a9f9-117">在 **友好名称** 框中，输入友好名称。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="1a9f9-118">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="1a9f9-119">下图显示了根节点示例。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-119">The following image shows a example root node.</span></span>

![示例根节点](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="1a9f9-121">创建导航类别节点</span><span class="sxs-lookup"><span data-stu-id="1a9f9-121">Create navigation category nodes</span></span>

<span data-ttu-id="1a9f9-122">若要创建任何其他导航类别节点以表示渠道上的产品类别，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="1a9f9-123">在导航窗格中，选择要将类别添加到的父节点。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="1a9f9-124">在操作窗格上选择 **新建类别模式**。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="1a9f9-125">在 **名称** 框中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="1a9f9-126">在 **描述** 框中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="1a9f9-127">在 **友好名称** 框中，输入友好名称。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="1a9f9-128">在 **显示顺序** 框中，输入显示顺序（可选）。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="1a9f9-129">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="1a9f9-130">下图显示了完成的渠道导航层次结构的示例。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![示例渠道层次结构](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="1a9f9-132">向类别节点添加产品</span><span class="sxs-lookup"><span data-stu-id="1a9f9-132">Add products to category nodes</span></span>

<span data-ttu-id="1a9f9-133">要将产品添加到类别节点，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="1a9f9-134">选择类别节点。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-134">Select a category node.</span></span>
1. <span data-ttu-id="1a9f9-135">在 **产品** 下面，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="1a9f9-136">使用产品编号或产品名称找到要添加的新产品，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="1a9f9-137">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="1a9f9-138">将产品添加到渠道导航层次结构内的节点并不能让产品在所选渠道上显示，这些产品也必须归类为某个渠道。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a channel.</span></span> <span data-ttu-id="1a9f9-139">有关分类的详细信息，请参阅[分类管理](assortments.md)。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-139">For more information on assortments, see [Assortment management](assortments.md).</span></span>

<span data-ttu-id="1a9f9-140">下图显示了添加有产品的节点示例。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-140">The following image shows an example node with products added.</span></span>

![添加到类别节点的产品](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="1a9f9-142">将产品属性组添加到类别节点</span><span class="sxs-lookup"><span data-stu-id="1a9f9-142">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="1a9f9-143">必须先创建属性组，然后才能将其添加到渠道导航层次结构内的节点。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-143">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="1a9f9-144">要将产品属性组添加到类别节点，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-144">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="1a9f9-145">选择类别节点。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-145">Select a category node.</span></span>
1. <span data-ttu-id="1a9f9-146">在 **产品属性组** 下面，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-146">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="1a9f9-147">找到您要添加的属性组，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-147">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="1a9f9-148">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="1a9f9-149">下图显示了添加有产品属性组的示例节点。</span><span class="sxs-lookup"><span data-stu-id="1a9f9-149">The following image shows a sample node with product attribute groups added.</span></span>

![节点上的产品属性组](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="1a9f9-151">其他资源</span><span class="sxs-lookup"><span data-stu-id="1a9f9-151">Additional resources</span></span>

[<span data-ttu-id="1a9f9-152">设置分类</span><span class="sxs-lookup"><span data-stu-id="1a9f9-152">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="1a9f9-153">管理属性和属性组</span><span class="sxs-lookup"><span data-stu-id="1a9f9-153">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

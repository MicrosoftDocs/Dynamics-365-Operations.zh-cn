---
title: 创建渠道导航层次结构
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建渠道导航层次结构。
author: samjarawan
ms.date: 01/27/2020
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
ms.openlocfilehash: 358f3d40c7a21184c20da342d6b2bf72dd4e7bbd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795827"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="99d5a-103">创建渠道导航层次结构</span><span class="sxs-lookup"><span data-stu-id="99d5a-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="99d5a-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建渠道导航层次结构。</span><span class="sxs-lookup"><span data-stu-id="99d5a-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="99d5a-105">概览</span><span class="sxs-lookup"><span data-stu-id="99d5a-105">Overview</span></span>

<span data-ttu-id="99d5a-106">渠道导航层次结构用于按类别归组和组织产品，以便可以在线或在销售点 (POS) 中浏览产品。</span><span class="sxs-lookup"><span data-stu-id="99d5a-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="99d5a-107">创建渠道导航层次结构</span><span class="sxs-lookup"><span data-stu-id="99d5a-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="99d5a-108">若要创建渠道导航层次结构，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="99d5a-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="99d5a-109">在导航窗格中，转到 **模块 \> Retail 和 Commerce \> 产品和类别 \> 渠道导航类别**。</span><span class="sxs-lookup"><span data-stu-id="99d5a-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="99d5a-110">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="99d5a-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="99d5a-111">在 **名称** 框中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="99d5a-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="99d5a-112">在 **描述** 框中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="99d5a-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="99d5a-113">选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="99d5a-113">Select **Create**.</span></span>
1. <span data-ttu-id="99d5a-114">在操作窗格中，选择 **新类别节点** 以创建根节点。</span><span class="sxs-lookup"><span data-stu-id="99d5a-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="99d5a-115">在 **名称** 框中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="99d5a-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="99d5a-116">在 **描述** 框中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="99d5a-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="99d5a-117">在 **友好名称** 框中，输入友好名称。</span><span class="sxs-lookup"><span data-stu-id="99d5a-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="99d5a-118">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="99d5a-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="99d5a-119">下图显示了根节点示例。</span><span class="sxs-lookup"><span data-stu-id="99d5a-119">The following image shows a example root node.</span></span>

![示例根节点](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="99d5a-121">创建导航类别节点</span><span class="sxs-lookup"><span data-stu-id="99d5a-121">Create navigation category nodes</span></span>

<span data-ttu-id="99d5a-122">若要创建任何其他导航类别节点以表示渠道上的产品类别，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="99d5a-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="99d5a-123">在导航窗格中，选择要将类别添加到的父节点。</span><span class="sxs-lookup"><span data-stu-id="99d5a-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="99d5a-124">在操作窗格上选择 **新建类别模式**。</span><span class="sxs-lookup"><span data-stu-id="99d5a-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="99d5a-125">在 **名称** 框中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="99d5a-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="99d5a-126">在 **描述** 框中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="99d5a-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="99d5a-127">在 **友好名称** 框中，输入友好名称。</span><span class="sxs-lookup"><span data-stu-id="99d5a-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="99d5a-128">在 **显示顺序** 框中，输入显示顺序（可选）。</span><span class="sxs-lookup"><span data-stu-id="99d5a-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="99d5a-129">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="99d5a-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="99d5a-130">下图显示了完成的渠道导航层次结构的示例。</span><span class="sxs-lookup"><span data-stu-id="99d5a-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![示例渠道层次结构](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="99d5a-132">向类别节点添加产品</span><span class="sxs-lookup"><span data-stu-id="99d5a-132">Add products to category nodes</span></span>

<span data-ttu-id="99d5a-133">要将产品添加到类别节点，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="99d5a-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="99d5a-134">选择类别节点。</span><span class="sxs-lookup"><span data-stu-id="99d5a-134">Select a category node.</span></span>
1. <span data-ttu-id="99d5a-135">在 **产品** 下面，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="99d5a-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="99d5a-136">使用产品编号或产品名称找到要添加的新产品，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="99d5a-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="99d5a-137">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="99d5a-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="99d5a-138">将产品添加到渠道导航层次结构内的节点并不能让产品在所选渠道上显示，这些产品也必须归类为某种产品。</span><span class="sxs-lookup"><span data-stu-id="99d5a-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a product.</span></span>

<span data-ttu-id="99d5a-139">下图显示了添加有产品的节点示例。</span><span class="sxs-lookup"><span data-stu-id="99d5a-139">The following image shows an example node with products added.</span></span>

![添加到类别节点的产品](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="99d5a-141">将产品属性组添加到类别节点</span><span class="sxs-lookup"><span data-stu-id="99d5a-141">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="99d5a-142">必须先创建属性组，然后才能将其添加到渠道导航层次结构内的节点。</span><span class="sxs-lookup"><span data-stu-id="99d5a-142">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="99d5a-143">要将产品属性组添加到类别节点，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="99d5a-143">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="99d5a-144">选择类别节点。</span><span class="sxs-lookup"><span data-stu-id="99d5a-144">Select a category node.</span></span>
1. <span data-ttu-id="99d5a-145">在 **产品属性组** 下面，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="99d5a-145">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="99d5a-146">找到您要添加的属性组，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="99d5a-146">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="99d5a-147">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="99d5a-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="99d5a-148">下图显示了添加有产品属性组的示例节点。</span><span class="sxs-lookup"><span data-stu-id="99d5a-148">The following image shows a sample node with product attribute groups added.</span></span>

![节点上的产品属性组](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="99d5a-150">其他资源</span><span class="sxs-lookup"><span data-stu-id="99d5a-150">Additional resources</span></span>

[<span data-ttu-id="99d5a-151">设置分类</span><span class="sxs-lookup"><span data-stu-id="99d5a-151">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="99d5a-152">管理属性和属性组</span><span class="sxs-lookup"><span data-stu-id="99d5a-152">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
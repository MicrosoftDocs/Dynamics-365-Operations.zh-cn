---
title: 在 Commerce 中创建新产品
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新产品。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3b578c1bdfe1c6b4bf66cc85cc09ed906fb812a8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965296"
---
# <a name="create-a-new-product-in-commerce"></a><span data-ttu-id="1a766-103">在 Commerce 中创建新产品</span><span class="sxs-lookup"><span data-stu-id="1a766-103">Create a new product in Commerce</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1a766-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新产品。</span><span class="sxs-lookup"><span data-stu-id="1a766-104">This topic describes how to create a new product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1a766-105">概览</span><span class="sxs-lookup"><span data-stu-id="1a766-105">Overview</span></span>

<span data-ttu-id="1a766-106">产品主要由产品编号、名称和描述定义。</span><span class="sxs-lookup"><span data-stu-id="1a766-106">A product is primarily defined by a product number, name, and description.</span></span> <span data-ttu-id="1a766-107">但是也需要其他数据以描述产品或服务：</span><span class="sxs-lookup"><span data-stu-id="1a766-107">However, other data is also required in order to describe a product or service:</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="1a766-108">创建新产品</span><span class="sxs-lookup"><span data-stu-id="1a766-108">Create a new product</span></span>

1. <span data-ttu-id="1a766-109">在导航窗格中，转到 **模块 \> Retail 和 Commerce \> 产品和类别 \> 产品(按类别)**。</span><span class="sxs-lookup"><span data-stu-id="1a766-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Products by category**.</span></span>
1. <span data-ttu-id="1a766-110">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="1a766-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="1a766-111">在 **产品类别** 下拉列表中，选择 **项目** 或 **服务**。</span><span class="sxs-lookup"><span data-stu-id="1a766-111">In the **Product type** drop-down list, select either **Item** or **Service**.</span></span>
1. <span data-ttu-id="1a766-112">在 **产品子类型** 下拉列表中，选择 **产品**（如果产品没有任何变型）或 **基础产品**（如果产品将有变型）。</span><span class="sxs-lookup"><span data-stu-id="1a766-112">In the **Product subtype** drop-down list, select either **Product** (if the product will have no variants) or **Product master** (if the product will have variants).</span></span>
1. <span data-ttu-id="1a766-113">在 **产品编号** 框中，输入产品编号（如果尚未预先填充）。</span><span class="sxs-lookup"><span data-stu-id="1a766-113">In the **Product number** box, enter a product number if one is not already prepopulated.</span></span>
1. <span data-ttu-id="1a766-114">在 **产品名称** 框中，输入产品名称。</span><span class="sxs-lookup"><span data-stu-id="1a766-114">In the **Product name** box, enter a product name.</span></span>
1. <span data-ttu-id="1a766-115">在 **搜索名称** 框中，输入搜索名称。</span><span class="sxs-lookup"><span data-stu-id="1a766-115">In the **Search name** box, enter a search name.</span></span>
1. <span data-ttu-id="1a766-116">在 **零售类别** 下拉列表中，选择适当的类别。</span><span class="sxs-lookup"><span data-stu-id="1a766-116">In the **Retail category** drop-down list, select an appropriate category.</span></span>
1. <span data-ttu-id="1a766-117">如果产品是套件，请针对 **产品套件** 选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="1a766-117">If the product is a kit, select **Yes** for **Product kit**.</span></span>
1. <span data-ttu-id="1a766-118">如果产品子类型是基础产品，请设置 **产品维度组** 以包括支持的变型。</span><span class="sxs-lookup"><span data-stu-id="1a766-118">If the product subtype is product master, set the **Product dimension group** to include the supported variants.</span></span> <span data-ttu-id="1a766-119">选项包括 **颜色**、**大小**、**样式** 和 **配置**。</span><span class="sxs-lookup"><span data-stu-id="1a766-119">Options include **Color**, **Size**, **Style**, and **Configuration**.</span></span> <span data-ttu-id="1a766-120">如果需要，您可能需要创建其他产品维度组。</span><span class="sxs-lookup"><span data-stu-id="1a766-120">You may need to create additional product dimension groups if needed.</span></span>
1. <span data-ttu-id="1a766-121">在 **配置技术** 下拉列表中，选择适当的选项。</span><span class="sxs-lookup"><span data-stu-id="1a766-121">In the **Configuration technology** drop-down list, select an appropriate option.</span></span>
1. <span data-ttu-id="1a766-122">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1a766-122">Select **OK**.</span></span>

<span data-ttu-id="1a766-123">下图显示了添加的产品示例。</span><span class="sxs-lookup"><span data-stu-id="1a766-123">The following image shows an example product being added.</span></span>

![创建产品](media/create-new-product.png)

<span data-ttu-id="1a766-125">添加产品后，可以为其设置其他数据，例如 **产品描述**、**变型组**、**维度组**、**产品属性** 和 **相关产品**。</span><span class="sxs-lookup"><span data-stu-id="1a766-125">Once a product is added, additional data can be set for it, such as **Product description**, **Variant groups**, **Dimension groups**, **Product attributes**, and **Related products**.</span></span>

<span data-ttu-id="1a766-126">下图显示了产品的其他详细信息。</span><span class="sxs-lookup"><span data-stu-id="1a766-126">The following image shows a product's additional details.</span></span>

![产品详细信息](media/create-new-product-2.png)

### <a name="create-product-variants"></a><span data-ttu-id="1a766-128">创建产品变型</span><span class="sxs-lookup"><span data-stu-id="1a766-128">Create product variants</span></span>

<span data-ttu-id="1a766-129">如果产品子类型是 **基础产品**，则需要创建特定变型。</span><span class="sxs-lookup"><span data-stu-id="1a766-129">If the product subtype is **Product master**, specific variants will need to be created.</span></span> 

<span data-ttu-id="1a766-130">要创建产品变型，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1a766-130">To create product variants, follow these steps.</span></span>

1. <span data-ttu-id="1a766-131">在操作窗格上，选择 **产品变型**。</span><span class="sxs-lookup"><span data-stu-id="1a766-131">On the action pane, select **Product variants**.</span></span>
1. <span data-ttu-id="1a766-132">如果在操作窗格上选择了变型组，请选择\**变型建议*。</span><span class="sxs-lookup"><span data-stu-id="1a766-132">If variant groups have been selected on the action pane, select \**Variant suggestions*.</span></span>
1. <span data-ttu-id="1a766-133">选择您要为该产品支持的变型。</span><span class="sxs-lookup"><span data-stu-id="1a766-133">Select the variants you would like to support for the product.</span></span>
1. <span data-ttu-id="1a766-134">选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="1a766-134">Select **Create**.</span></span>

## <a name="release-a-product"></a><span data-ttu-id="1a766-135">发布产品</span><span class="sxs-lookup"><span data-stu-id="1a766-135">Release a product</span></span>

<span data-ttu-id="1a766-136">要销售产品，必须先将其发布给法人。</span><span class="sxs-lookup"><span data-stu-id="1a766-136">To sell a product it must first be released to a legal entity.</span></span>

1. <span data-ttu-id="1a766-137">从产品页面中，选择 **发布产品**。</span><span class="sxs-lookup"><span data-stu-id="1a766-137">From the product page, select **Release products**.</span></span>

    ![发布产品](media/create-new-product-3.png)

1. <span data-ttu-id="1a766-139">选择要发布的产品，然后选择 **下一个**。</span><span class="sxs-lookup"><span data-stu-id="1a766-139">Select the product to release, and then select **Next**.</span></span>

    ![选择要发布的产品](media/create-new-product-4.png)

1. <span data-ttu-id="1a766-141">选择要发布的产品变型集，然后选择 **下一个**。</span><span class="sxs-lookup"><span data-stu-id="1a766-141">Select the set of product variants to release, and then select **Next**.</span></span>

    ![选择要发布的变型](media/create-new-product-5.png)

1. <span data-ttu-id="1a766-143">选择法人，然后选择 **下一个**。</span><span class="sxs-lookup"><span data-stu-id="1a766-143">Select the legal entity, and then select **Next**.</span></span>

    ![选择法人](media/create-new-product-6.png)

1. <span data-ttu-id="1a766-145">选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="1a766-145">Select **Finish**.</span></span>

    ![完成产品发布](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a><span data-ttu-id="1a766-147">配置发布的产品</span><span class="sxs-lookup"><span data-stu-id="1a766-147">Configure a released product</span></span>

<span data-ttu-id="1a766-148">发布产品后，将需要进一步的配置，包括为产品添加价格。</span><span class="sxs-lookup"><span data-stu-id="1a766-148">Once a product is released, it will then require further configuration that includes adding a price to the product.</span></span>

1. <span data-ttu-id="1a766-149">在导航窗格中，转到 **模块 \> Retail 和 Commerce \> 产品和类别 \> 已发布的产品(按类别)**。</span><span class="sxs-lookup"><span data-stu-id="1a766-149">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="1a766-150">选择已发布产品的产品类别节点，然后从产品列表中选择产品。</span><span class="sxs-lookup"><span data-stu-id="1a766-150">Select the product category node for the product that was released, and then select the product from the product list.</span></span>
1. <span data-ttu-id="1a766-151">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="1a766-151">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="1a766-152">在 **采购** 部分，配置所有必需的属性，包括 **单位**、**价钱** 和 **数量**。</span><span class="sxs-lookup"><span data-stu-id="1a766-152">In the **Purchase** section, configure any required properties including **Unit**, **Price**,  and **Quantity**.</span></span>
1. <span data-ttu-id="1a766-153">在操作窗格上，选择 **验证** 以确保没有报告字段缺失错误。</span><span class="sxs-lookup"><span data-stu-id="1a766-153">On the action pane, select **Validate** to ensure that no errors are reported for missing fields.</span></span>
1. <span data-ttu-id="1a766-154">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1a766-154">On the action pane, select **Save**.</span></span>

<span data-ttu-id="1a766-155">下图显示了一个已发布产品的配置示例。</span><span class="sxs-lookup"><span data-stu-id="1a766-155">The following image shows an example configuration for a released product.</span></span>

![配置发布的产品](media/create-new-product-8.png)

## <a name="additional-resources"></a><span data-ttu-id="1a766-157">其他资源</span><span class="sxs-lookup"><span data-stu-id="1a766-157">Additional resources</span></span>

[<span data-ttu-id="1a766-158">创建法人</span><span class="sxs-lookup"><span data-stu-id="1a766-158">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="1a766-159">创建变型组</span><span class="sxs-lookup"><span data-stu-id="1a766-159">Create a variant group</span></span>](create-variant-group.md) 

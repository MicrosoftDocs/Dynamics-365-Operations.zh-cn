---
title: 为仓库交易配置产品筛选器
description: 本主题描述了如何配置产品筛选器和筛选器编码为仓库中的库存物料分类。 您也可以使用筛选器指定可以订购特殊物料的客户，以及可以从特定供应商采购哪些物料。
author: Mirzaab
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSFilters,WHSFilterGroupTable,EcoResProductDetailsExtended,WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 922ff818e069f41c139cc00db9161dc6e113888b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973727"
---
# <a name="configure-product-filters-for-warehouse-transactions"></a><span data-ttu-id="9a204-104">为仓库交易配置产品筛选器</span><span class="sxs-lookup"><span data-stu-id="9a204-104">Configure product filters for warehouse transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a204-105">本主题描述了如何配置产品筛选器和筛选器编码为仓库中的库存物料分类。</span><span class="sxs-lookup"><span data-stu-id="9a204-105">This topic describes how to configure product filters and filter codes to categorize inventory items in a warehouse.</span></span> <span data-ttu-id="9a204-106">您也可以使用筛选器指定可以订购特殊物料的客户，以及可以从特定供应商采购哪些物料。</span><span class="sxs-lookup"><span data-stu-id="9a204-106">You can also use filters to specify which customers can order a particular item and which items can be purchased from a particular vendor.</span></span>

<span data-ttu-id="9a204-107">此外，您还可以设置并使用产品筛选器自动组织仓库中的库存物料并将已筛选物料组合到筛选器组。</span><span class="sxs-lookup"><span data-stu-id="9a204-107">Additionally, you can set up and use product filters to automatically organize inventory items in a warehouse and combine filtered items into filter groups.</span></span> <span data-ttu-id="9a204-108">筛选器可用于将物料分类以执行处理、购买和销售流程。</span><span class="sxs-lookup"><span data-stu-id="9a204-108">Filters can be used to put items into categories for handling, purchasing, and selling processes.</span></span> <span data-ttu-id="9a204-109">当处理方式基于重量或处理限制时，您可能需要将物料分组在一起或将它们彼此分开。</span><span class="sxs-lookup"><span data-stu-id="9a204-109">You might want to group items together or separate them from each other when the way that they are handled is based on weight or handling restrictions.</span></span> <span data-ttu-id="9a204-110">您还可以指定可以向其购买或出售物料的客户或供应商。</span><span class="sxs-lookup"><span data-stu-id="9a204-110">You can also specify which customers or vendors an item can be purchased from or sold to.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9a204-111">先决条件</span><span class="sxs-lookup"><span data-stu-id="9a204-111">Prerequisites</span></span>

<span data-ttu-id="9a204-112">下表显示必须先就绪然后才能开始的先决条件。</span><span class="sxs-lookup"><span data-stu-id="9a204-112">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="9a204-113">必备项</span><span class="sxs-lookup"><span data-stu-id="9a204-113">Prerequisite</span></span> | <span data-ttu-id="9a204-114">描述</span><span class="sxs-lookup"><span data-stu-id="9a204-114">Instructions</span></span> |
|---|---|
| <span data-ttu-id="9a204-115">在开始在 **已发布产品详细信息** 页上配置产品之前，必须为产品的存储维度组打开仓库处理。</span><span class="sxs-lookup"><span data-stu-id="9a204-115">Before you start to configure products on the **Released product details** page, you must turn on warehouse processing for the product's storage dimension group.</span></span> | <span data-ttu-id="9a204-116">转到 **产品信息管理 \> 设置 \> 维度和变型组 \> 存储维度组**，选择或创建一个存储维度组，将其 **使用仓库管理流程** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="9a204-116">Go to **Product information management \> Setup \> Dimension and variant groups \> Storage dimension groups**, and select or create a storage dimension group where the **Use warehouse management processes** option is set to *Yes*.</span></span> |
| <span data-ttu-id="9a204-117">如果要使用客户筛选器和/或供应商筛选器，则必须在“仓库管理”参数中启用它们的使用。</span><span class="sxs-lookup"><span data-stu-id="9a204-117">If you will use customer filters and/or vendor filters, you must enable their use in Warehouse management parameters.</span></span> | <span data-ttu-id="9a204-118">转到 **仓库管理 \> 设置 \> 仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="9a204-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span> <span data-ttu-id="9a204-119">在 **产品筛选器** 选项卡上，将 **启用客户筛选器** 和/或 **启用供应商筛选器** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="9a204-119">On the **Product filters** tab, set the **Enable customer filters** and/or **Enable vendor filters** option  to *Yes*.</span></span> |

## <a name="set-up-product-filters"></a><span data-ttu-id="9a204-120">设置产品筛选器</span><span class="sxs-lookup"><span data-stu-id="9a204-120">Set up product filters</span></span>

<span data-ttu-id="9a204-121">产品筛选器最多提供 10 个 **筛选器标题** 特征，这些特征是枚举值。</span><span class="sxs-lookup"><span data-stu-id="9a204-121">Product filters provide up to 10 **Filter title** characteristics, which are enumeration (enum) values.</span></span> <span data-ttu-id="9a204-122">创建产品筛选器时，可以选择这些枚举值。</span><span class="sxs-lookup"><span data-stu-id="9a204-122">These enum values are available for selection when you create a product filter.</span></span> <span data-ttu-id="9a204-123">枚举值 *代码 1* 到 *代码 10* 是系统定义的，表示物料的特定特征或属性。</span><span class="sxs-lookup"><span data-stu-id="9a204-123">The enum values *Code 1* through *Code 10* are system-defined and represent a specific characteristic or attribute of an item.</span></span> <span data-ttu-id="9a204-124">例如，*代码 1* 可能表示具有危险材料分类的物料。</span><span class="sxs-lookup"><span data-stu-id="9a204-124">For example, *Code 1* might represent items that have a hazardous material classification.</span></span> <span data-ttu-id="9a204-125">*代码 2* 可能表示只有供应商可以购买的物料。</span><span class="sxs-lookup"><span data-stu-id="9a204-125">*Code 2* might represent items that only vendors can purchase.</span></span> <span data-ttu-id="9a204-126">然后，产品筛选器定义与 **筛选器标题** 值关联的特定 **筛选器代码** 值。</span><span class="sxs-lookup"><span data-stu-id="9a204-126">Product filters then define the specific **Filter code** value that is associated with a **Filter title** value.</span></span>

1. <span data-ttu-id="9a204-127">转到 **仓库管理 \> 设置 \> 产品筛选器 \> 产品筛选器**。</span><span class="sxs-lookup"><span data-stu-id="9a204-127">Go to **Warehouse management \> Setup \> Product filters \> Product filters**.</span></span>
1. <span data-ttu-id="9a204-128">在操作窗格上，选择 **新建** 向网格添加产品筛选器。</span><span class="sxs-lookup"><span data-stu-id="9a204-128">On the Action Pane, select **New** to add a product filter to the grid.</span></span>
1. <span data-ttu-id="9a204-129">在 **筛选器标题** 字段中，选择一个值。</span><span class="sxs-lookup"><span data-stu-id="9a204-129">In the **Filter title** field, select a value.</span></span>
1. <span data-ttu-id="9a204-130">在 **筛选器代码** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a204-130">In the **Filter code** field, enter a value.</span></span>

    <span data-ttu-id="9a204-131">![设置产品筛选器](media/Product_Filters10.png "设置产品筛选器")</span><span class="sxs-lookup"><span data-stu-id="9a204-131">![Setting up a product filter](media/Product_Filters10.png "Setting up a product filter")</span></span>

1. <span data-ttu-id="9a204-132">在 **描述** 字段中，为代码输入名称。</span><span class="sxs-lookup"><span data-stu-id="9a204-132">In the **Description** field, enter a name for the code.</span></span> <span data-ttu-id="9a204-133">例如，*代码 2* 可能表示供应商。</span><span class="sxs-lookup"><span data-stu-id="9a204-133">For example, *Code 2* might represent vendors.</span></span> <span data-ttu-id="9a204-134">然后，您可以为特定供应商或供应商组创建产品筛选器。</span><span class="sxs-lookup"><span data-stu-id="9a204-134">You can then create a product filter for a specific vendor or group of vendors.</span></span> <span data-ttu-id="9a204-135">有关详细信息，请参阅本主题后面的[设置供应商筛选器代码](#vendor-product-filters)部分。</span><span class="sxs-lookup"><span data-stu-id="9a204-135">For more information, see the [Setup vendor filter codes](#vendor-product-filters) section later in this topic.</span></span>

    <span data-ttu-id="9a204-136">![设置产品筛选器](media/Product_Filters.png "设置产品筛选器")</span><span class="sxs-lookup"><span data-stu-id="9a204-136">![Set of product filters](media/Product_Filters.png "Set of product filters")</span></span>

## <a name="set-up-product-filter-groups"></a><span data-ttu-id="9a204-137">设置产品筛选器组</span><span class="sxs-lookup"><span data-stu-id="9a204-137">Set up product filter groups</span></span>

<span data-ttu-id="9a204-138">您可以使用筛选器组分组筛选代码。</span><span class="sxs-lookup"><span data-stu-id="9a204-138">You can use filter groups to group filter codes.</span></span> <span data-ttu-id="9a204-139">当组用于位置指令中的查询，而您要搜索组而不是一系列代码时，此功能非常有用。</span><span class="sxs-lookup"><span data-stu-id="9a204-139">This capability is helpful when a group is used in a query in a location directive, and you want to search for the group instead of a series of codes.</span></span> <span data-ttu-id="9a204-140">每个筛选器组与一个物料组关联。</span><span class="sxs-lookup"><span data-stu-id="9a204-140">Each filter group is associated with an item group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a204-141">并非所有产品筛选器组都可用于大于 *代码 4*（即 *代码 5* 到 *代码 10*）的筛选器代码。</span><span class="sxs-lookup"><span data-stu-id="9a204-141">Not all product filter groups are available for filter codes that are higher than *Code 4* (that is, *Code 5* through *Code 10*).</span></span> <span data-ttu-id="9a204-142">例如，对于已发布产品，尽管将添加所有产品筛选器代码，但是不会更新筛选器代码的分组。</span><span class="sxs-lookup"><span data-stu-id="9a204-142">For example, for released products, although all the product filter codes will be added, the grouping of filter codes won't be updated.</span></span> <span data-ttu-id="9a204-143">此行为可能会在更高版本中更新。</span><span class="sxs-lookup"><span data-stu-id="9a204-143">This behavior might be updated in later releases.</span></span>

<span data-ttu-id="9a204-144">若要设置筛选器组，请执行这些步骤。</span><span class="sxs-lookup"><span data-stu-id="9a204-144">To set up filter groups, follow these steps.</span></span>

1. <span data-ttu-id="9a204-145">转到 **仓库管理 \> 设置 \> 产品筛选器 \> 产品筛选器组**。</span><span class="sxs-lookup"><span data-stu-id="9a204-145">Go to **Warehouse management \> Setup \> Product filters \> Product filter groups**.</span></span>
1. <span data-ttu-id="9a204-146">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="9a204-146">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9a204-147">在 **组 1** 和 **组 2** 字段中，输入要用于对物料分类的名称。</span><span class="sxs-lookup"><span data-stu-id="9a204-147">In the **Group 1** and **Group 2** fields, enter the names that will be used to categorize items.</span></span>
1. <span data-ttu-id="9a204-148">在 **详细信息** 快速选项卡上，选择 **新建** 添加行。</span><span class="sxs-lookup"><span data-stu-id="9a204-148">On the **Details** FastTab, select **New** to add a line.</span></span>
1. <span data-ttu-id="9a204-149">在 **开始日期/时间** 和 **结束日期/时间** 字段中，输入筛选器组的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="9a204-149">In the **Start date/time** and **End date/time** fields, enter start and end dates for the filter group.</span></span>
1. <span data-ttu-id="9a204-150">在 **物料组** 字段中，选择产品筛选器应该应用的物料组。</span><span class="sxs-lookup"><span data-stu-id="9a204-150">In the **Item group** field, select the item group that the product filter should apply to.</span></span>
1. <span data-ttu-id="9a204-151">在 **代码 1** 到 **代码 10** 字段中，根据需要选择要包含在组中的筛选器代码。</span><span class="sxs-lookup"><span data-stu-id="9a204-151">In the **Code 1** through **Code 10** fields, select the filter codes to include in the group, as required.</span></span>

    <span data-ttu-id="9a204-152">![物料组](media/ProdFilterGroup.png "物料组")</span><span class="sxs-lookup"><span data-stu-id="9a204-152">![Item group](media/ProdFilterGroup.png "Item group")</span></span>

> [!NOTE]
> <span data-ttu-id="9a204-153">如果您在关闭页面时收到错误消息，一个代码设置将会丢失。</span><span class="sxs-lookup"><span data-stu-id="9a204-153">If you receive an error message when you close the page, a code setup might be missing.</span></span> <span data-ttu-id="9a204-154">在 **物料组** 页上，您可以通过选中 **为物料组分配筛选器代码 1**、**为物料组分配筛选器代码 2** 等复选框来让代码成为物料组的强制代码。</span><span class="sxs-lookup"><span data-stu-id="9a204-154">On the **Item groups** page, you can make the codes mandatory for an item group by selecting the **Assign filter code 1 for item group**, **Assign filter code 2 for item group**, and so on, check boxes.</span></span>

## <a name="set-up-filter-codes-on-item-groups"></a><span data-ttu-id="9a204-155">设置物料组的筛选器代码</span><span class="sxs-lookup"><span data-stu-id="9a204-155">Set up filter codes on item groups</span></span>

<span data-ttu-id="9a204-156">通过设置物料组的筛选器代码，您可以让这些代码成为附加到该物料组的产品的必需代码。</span><span class="sxs-lookup"><span data-stu-id="9a204-156">By setting up filter codes on an item group, you can make the codes that are required for products that are attached to that item group.</span></span>

<span data-ttu-id="9a204-157">要设置物料组的筛选器代码，请按以下步骤进行操作。</span><span class="sxs-lookup"><span data-stu-id="9a204-157">To set up filter codes on item groups, follow these steps.</span></span>

1. <span data-ttu-id="9a204-158">转到 **库存管理 \> 设置 \> 库存 \> 物料组**。</span><span class="sxs-lookup"><span data-stu-id="9a204-158">Go to **Inventory management \> Setup \> Inventory \> Item groups**.</span></span>
1. <span data-ttu-id="9a204-159">在“操作窗格”中，选择 **新建** 创建物料组。</span><span class="sxs-lookup"><span data-stu-id="9a204-159">On the Action Pane, select **New** to create an item group.</span></span>
1. <span data-ttu-id="9a204-160">在 **物料组** 字段中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="9a204-160">In the **Item group** field, enter a name.</span></span>
1. <span data-ttu-id="9a204-161">在 **名称** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="9a204-161">In the **Name** field, enter a description.</span></span>
1. <span data-ttu-id="9a204-162">在 **仓库** 快速选项卡上，在 **需要筛选器** 部分，选中必须为与物料组关联的产品指定的筛选器代码的复选框。</span><span class="sxs-lookup"><span data-stu-id="9a204-162">On the **Warehouse** FastTab, in the **Filter required** section, select the check boxes for the filter codes that must be specified for products that are associated with the item group.</span></span>

    <span data-ttu-id="9a204-163">要更新已发布的产品，打开它的 **已发布产品详细信息** 页，然后在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="9a204-163">To update a released product, open its **Released product details** page, and then, on the Action Pane, select **Edit**.</span></span> <span data-ttu-id="9a204-164">然后，与代码关联的筛选器将在 **仓库** 快速选项卡上可用。</span><span class="sxs-lookup"><span data-stu-id="9a204-164">The filters that are associated with codes then become available on the **Warehouse** FastTab.</span></span>

    <span data-ttu-id="9a204-165">![物料组](media/ItemGroup10.png "物料组")</span><span class="sxs-lookup"><span data-stu-id="9a204-165">![Item groups](media/ItemGroup10.png "Item groups")</span></span>

1. <span data-ttu-id="9a204-166">在 **物料组筛选器** 部分，选中必须与要作为物料默认筛选器组的筛选器组匹配的筛选器的复选框。</span><span class="sxs-lookup"><span data-stu-id="9a204-166">In the **Item group filter** section, select the check boxes for the filters that must match for the filter group to be the default filter group for an item.</span></span>

    <span data-ttu-id="9a204-167">例如，如果选择了 **使用筛选器代码 1** 和 **使用筛选器代码 2** 复选框，物料的筛选器代码 1 和筛选器代码 2 必须与物料组的筛选器组的设置相匹配，这时才可以选择筛选器组。</span><span class="sxs-lookup"><span data-stu-id="9a204-167">For example, if the **Use filter code 1** and **Use filter code 2** check boxes are selected, both filter code 1 and filter code 2 of the item must match the setup of the filter group for the item group before the filter group can be selected.</span></span> <span data-ttu-id="9a204-168">创建新物料时，所选筛选器组将是 **已发布产品详细信息** 页的 **仓库** 快速选项卡上 **组 1** 和 **组 2** 字段中的默认筛选器组。</span><span class="sxs-lookup"><span data-stu-id="9a204-168">When you create a new item, the selected filter group will be the default filter group in the **Group 1** and **Group 2** fields on the **Warehouse** FastTab of the **Released product details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a204-169">产品筛选器代码仅对使用高级仓库管理的物料启用。</span><span class="sxs-lookup"><span data-stu-id="9a204-169">Product filter codes are enabled only for items that use advanced warehouse management.</span></span>

## <a name="specify-filter-codes-for-released-products"></a><span data-ttu-id="9a204-170">指定已发布产品的筛选器代码</span><span class="sxs-lookup"><span data-stu-id="9a204-170">Specify filter codes for released products</span></span>

<span data-ttu-id="9a204-171">请按照以下步骤指定已发布产品的筛选器代码。</span><span class="sxs-lookup"><span data-stu-id="9a204-171">Follow these steps to specify filter codes for released products.</span></span> <span data-ttu-id="9a204-172">例如，您可以使用筛选器代码对特定供应商购买的危险产品进行分组。</span><span class="sxs-lookup"><span data-stu-id="9a204-172">For example, you can use filter codes to group hazardous products that specific vendors purchase.</span></span>

1. <span data-ttu-id="9a204-173">转到 **产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="9a204-173">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="9a204-174">在操作窗格上，选择 **新建** 创建产品。</span><span class="sxs-lookup"><span data-stu-id="9a204-174">On the Action Pane, select **New** to create a product.</span></span>
1. <span data-ttu-id="9a204-175">在 **新建已发布产品** 对话框中，输入创建新产品的基础所需的数据，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="9a204-175">In the **New released product** dialog box, enter the data that is required to create the base of a new product, and then select **OK**.</span></span>

    <span data-ttu-id="9a204-176">除非已为筛选器代码配置了附加到产品的物料组，否则筛选器代码不会启用。</span><span class="sxs-lookup"><span data-stu-id="9a204-176">Product filter codes aren't enabled unless the item group that is attached to the product has been configured for filter codes.</span></span>

    <span data-ttu-id="9a204-177">有关详细信息，请参阅[创建新产品](../pim/tasks/create-new-product.md)。</span><span class="sxs-lookup"><span data-stu-id="9a204-177">For more information, see [Create a new product](../pim/tasks/create-new-product.md).</span></span>

1. <span data-ttu-id="9a204-178">在 **仓库** 快速选项卡上的 **产品筛选器代码** 部分，根据需要为 **代码 1** 到 **代码 10** 字段选择筛选器代码，以为产品指定筛选器代码。</span><span class="sxs-lookup"><span data-stu-id="9a204-178">On the **Warehouse** FastTab, in the **Product filter codes** section, select filter codes for the **Code 1** through **Code 10** fields, as required, to specify filter codes for the product.</span></span>

## <a name="set-up-generally-available-items"></a><span data-ttu-id="9a204-179">设置普遍可用的物料</span><span class="sxs-lookup"><span data-stu-id="9a204-179">Set up generally available items</span></span>

<span data-ttu-id="9a204-180">您可以将特定库存物料设置为仅对客户、仅对供应商或同时对二者可用。</span><span class="sxs-lookup"><span data-stu-id="9a204-180">You can make specific inventory items available only for customers, only for vendors, or for both customers and vendors.</span></span>

> [!NOTE]
> <span data-ttu-id="9a204-181">客户和供应商筛选器不适用于被设置为普遍可用的物料。</span><span class="sxs-lookup"><span data-stu-id="9a204-181">Customer and vendor filters don't apply to any item that is set up as generally available.</span></span>

<span data-ttu-id="9a204-182">要设置普遍可用的物料，请按以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="9a204-182">To set up generally available items, follow these steps.</span></span>

1. <span data-ttu-id="9a204-183">转到 **仓库管理 \> 设置 \> 产品筛选器 \> 普遍可用的产品**。</span><span class="sxs-lookup"><span data-stu-id="9a204-183">Go to **Warehouse management \> Setup \> Product filters \> Generally available products**.</span></span>
1. <span data-ttu-id="9a204-184">在操作窗格上，选择 **新建** 创建记录。</span><span class="sxs-lookup"><span data-stu-id="9a204-184">On the Action Pane, select **New** to create a record.</span></span>
1. <span data-ttu-id="9a204-185">在 **客户或供应商** 字段中，选择 *客户*、*供应商* 或 *所有*，让物料对客户、供应商或同时对二者可用。</span><span class="sxs-lookup"><span data-stu-id="9a204-185">In the **Customer or vendor** field, select *Customer*, *Vendor*, or *All* to make the items available for customers, vendors, or both.</span></span>
1. <span data-ttu-id="9a204-186">在 **开始日期/时间** 字段中，输入物料可用的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="9a204-186">In the **Start date/time** field, enter the date and time when the item will become available.</span></span>
1. <span data-ttu-id="9a204-187">在 **物料组** 字段中，选择物料组。</span><span class="sxs-lookup"><span data-stu-id="9a204-187">In the **Item group** field, select an item group.</span></span>
1. <span data-ttu-id="9a204-188">在 **代码 1** 到 **代码 10** 字段中，选择限制普遍可用的物料的筛选器代码。</span><span class="sxs-lookup"><span data-stu-id="9a204-188">In the **Code 1** through **Code 10** fields, select the filter codes to limit the items that are generally available.</span></span>

    <span data-ttu-id="9a204-189">在您选择物料组时，请将该物料组设置为普遍可用。</span><span class="sxs-lookup"><span data-stu-id="9a204-189">When you select an item group, you set that group of items as generally available.</span></span> <span data-ttu-id="9a204-190">通过选择这些字段中的筛选器代码，限制可用的物料。</span><span class="sxs-lookup"><span data-stu-id="9a204-190">By selecting filter codes in these fields, you limit the items that are available.</span></span>

## <a name="set-up-customer-product-filters"></a><span data-ttu-id="9a204-191">设置客户产品筛选器</span><span class="sxs-lookup"><span data-stu-id="9a204-191">Set up customer product filters</span></span>

<span data-ttu-id="9a204-192">您可以使用此可选过程指定应该对客户可用的物料，以及通过 **普遍可用的物料** 页上的筛选器设置使其可用的物料。</span><span class="sxs-lookup"><span data-stu-id="9a204-192">You can use this optional procedure to specify items that should be available for a customer in addition to the items that are made available via the filter setup on the **Generally available items** page.</span></span> <span data-ttu-id="9a204-193">您可以为单个客户设置多个筛选器。</span><span class="sxs-lookup"><span data-stu-id="9a204-193">You can set up multiple filters for a single customer.</span></span>

<span data-ttu-id="9a204-194">要设置客户筛选器代码，请按以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="9a204-194">To set up customer filter codes, follow these steps.</span></span>

1. <span data-ttu-id="9a204-195">转到 **销售和市场营销 \> 客户 \> 所有客户**。</span><span class="sxs-lookup"><span data-stu-id="9a204-195">Go to **Sales and marketing \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="9a204-196">选择一个客户。</span><span class="sxs-lookup"><span data-stu-id="9a204-196">Select a customer.</span></span>
1. <span data-ttu-id="9a204-197">在操作窗格的 **客户** 选项卡上，在 **设置** 组中，选择 **产品筛选器**。</span><span class="sxs-lookup"><span data-stu-id="9a204-197">On the Action Pane, on the **Customer** tab, in the **Set up** group, select **Product filters**.</span></span>
1. <span data-ttu-id="9a204-198">在 **产品筛选器代码** 页的操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="9a204-198">On the **Product filter codes** page, on the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9a204-199">在 **开始日期/时间** 和 **结束日期/时间** 字段中，输入所选物料组的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="9a204-199">In the **Start date/time** and **End date/time** fields, enter start and end dates for the selected item group.</span></span>
1. <span data-ttu-id="9a204-200">在 **物料组** 字段中，选择物料组。</span><span class="sxs-lookup"><span data-stu-id="9a204-200">In the **Item group** field, select an item group.</span></span>
1. <span data-ttu-id="9a204-201">在 **代码 1** 到 **代码 10** 字段中，选择筛选器代码，用作限制所选物料组中对客户可用的物料的条件。</span><span class="sxs-lookup"><span data-stu-id="9a204-201">In the **Code 1** through **Code 10** fields, select the filter codes to use as criteria to limit the items that are available for customers in the selected item group.</span></span> <span data-ttu-id="9a204-202">您必须为为物料组设置的每个筛选器代码进行选择。</span><span class="sxs-lookup"><span data-stu-id="9a204-202">You must make a selection for every filter code that is set up for the item group.</span></span>

## <a name="set-up-vendor-product-filters"></a><a name="vendor-product-filters"></a><span data-ttu-id="9a204-203">设置供应商产品筛选器</span><span class="sxs-lookup"><span data-stu-id="9a204-203">Set up vendor product filters</span></span>

<span data-ttu-id="9a204-204">您可以使用此可选过程指定应该对供应商可用的物料，以及通过 **普遍可用的物料** 页上的筛选器设置使其可用的物料。</span><span class="sxs-lookup"><span data-stu-id="9a204-204">You can use this optional procedure to specify items that should be available for a vendor in addition to the items that are made available via the filter setup on the **Generally available items** page.</span></span> <span data-ttu-id="9a204-205">您可以为单个供应商设置多个筛选器。</span><span class="sxs-lookup"><span data-stu-id="9a204-205">You can set up multiple filters for a single vendor.</span></span>

<span data-ttu-id="9a204-206">要设置供应商筛选器代码，请按以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="9a204-206">To set up vendor filter codes, follow these steps.</span></span>

1. <span data-ttu-id="9a204-207">转到 **采购 \> 供应商 \> 所有供应商**。</span><span class="sxs-lookup"><span data-stu-id="9a204-207">Go to **Procurement and sourcing \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="9a204-208">选择某一供应商。</span><span class="sxs-lookup"><span data-stu-id="9a204-208">Select a vendor.</span></span>
1. <span data-ttu-id="9a204-209">在操作窗格的 **供应商** 选项卡上，在 **设置** 组中，选择 **产品筛选器**。</span><span class="sxs-lookup"><span data-stu-id="9a204-209">On the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Product filters**.</span></span>
1. <span data-ttu-id="9a204-210">在 **筛选器代码** 页的操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="9a204-210">On the **Filter codes** page, on the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9a204-211">在 **开始日期/时间** 和 **结束日期/时间** 字段中，输入所选物料组的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="9a204-211">In the **Start date/time** and **End date/time** fields, enter start and end dates for the selected item group.</span></span>
1. <span data-ttu-id="9a204-212">在 **物料组** 字段中，选择物料组。</span><span class="sxs-lookup"><span data-stu-id="9a204-212">In the **Item group** field, select an item group.</span></span>
1. <span data-ttu-id="9a204-213">在 **代码 1** 到 **代码 10** 字段中，选择筛选器代码，用作限制所选物料组中对供应商可用的物料的条件。</span><span class="sxs-lookup"><span data-stu-id="9a204-213">In the **Code 1** through **Code 10** fields, select the filter codes to use as criteria to limit the items that are available for vendors in the selected item group.</span></span> <span data-ttu-id="9a204-214">您必须为为物料组设置的每个筛选器代码进行选择。</span><span class="sxs-lookup"><span data-stu-id="9a204-214">You must make a selection for every filter code that is set up for the item group.</span></span>

> [!NOTE]
> <span data-ttu-id="9a204-215">供应商产品筛选器的设置适用于为关联的存储维度组启用了仓库管理流程的已发布产品。</span><span class="sxs-lookup"><span data-stu-id="9a204-215">The setup of vendor product filters applies to released products where warehouse management processes are enabled for the associated storage dimension group.</span></span> <span data-ttu-id="9a204-216">筛选器代码用于确定系统在创建采购订单行时是否允许用户从给定供应商处购买给定物料。</span><span class="sxs-lookup"><span data-stu-id="9a204-216">The filter codes are used to determine whether the system will allow users to purchase a given item from a given vendor when they create purchase order lines.</span></span> <span data-ttu-id="9a204-217">Microsoft Dynamics 365 Supply Chain Management 有两种处理供应商审批的方法。</span><span class="sxs-lookup"><span data-stu-id="9a204-217">Microsoft Dynamics 365 Supply Chain Management has two methods for handling vendor approval.</span></span> <span data-ttu-id="9a204-218">如果存在一个或多个 **核准供应商检查方法** 字段设置为 *仅警告* 或 *不允许* 的已发布产品，两种供应商审批方法都可以为这些物料启用。</span><span class="sxs-lookup"><span data-stu-id="9a204-218">If one or more released products exist where the **Approved vendor check method** field is set to *Warning only* or *Not allowed*, both vendor approval methods could be enabled for those items.</span></span> <span data-ttu-id="9a204-219">这种情况可能会在用户创建采购订单行时导致问题。</span><span class="sxs-lookup"><span data-stu-id="9a204-219">This situation might cause issues when users create purchase order lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="9a204-220">请参阅</span><span class="sxs-lookup"><span data-stu-id="9a204-220">See also</span></span>

[<span data-ttu-id="9a204-221">有关详细信息，请参阅博客文章“WMS 仓库筛选器代码”</span><span class="sxs-lookup"><span data-stu-id="9a204-221">For more information see the blog post WMS-Warehouse Filter Codes</span></span>](http://blog.dynamics-for-operations.com/2017/09/26/wms-warehouse-filter-codes/)

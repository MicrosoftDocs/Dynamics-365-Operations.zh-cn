---
title: 配置库存缓冲区和库存级别
description: 本主题说明如何在 Microsoft Dynamics 365 Commerce 上配置确定库存可用性消息的库存缓冲区和库存级别。
author: boycezhu
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: ea6844307e63b351ef914134b7d8392b0910019a
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478380"
---
# <a name="configure-inventory-buffers-and-inventory-levels"></a><span data-ttu-id="37e42-103">配置库存缓冲区和库存级别</span><span class="sxs-lookup"><span data-stu-id="37e42-103">Configure inventory buffers and inventory levels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="37e42-104">本主题说明如何在 Microsoft Dynamics 365 Commerce 上配置确定有关库存可用性的消息的库存缓冲区和库存级别。</span><span class="sxs-lookup"><span data-stu-id="37e42-104">This topic explains how to configure inventory buffers and inventory levels that determine the messaging about inventory availability on Microsoft Dynamics 365 Commerce sites.</span></span>

<span data-ttu-id="37e42-105">Dynamics 365 Commerce 总部保留库存数据和各个渠道，如销售点 (POS) 应用程序、电子商务店面，以及其他以异步方式拉取和推送库存的自定义集成应用程序。</span><span class="sxs-lookup"><span data-stu-id="37e42-105">Dynamics 365 Commerce headquarters holds inventory data and various channels such as point of sale (POS) applications, e-Commerce storefronts, and other custom integrated applications that pull and push inventory around in an asynchronous manner.</span></span> <span data-ttu-id="37e42-106">因此，通过 Commerce 总部的现有库存量页面、POS 用户界面 (UI) 以及通过电子商务库存可用性 API 获取的可用库存值，并不总是 100% 实时准确的。</span><span class="sxs-lookup"><span data-stu-id="37e42-106">Therefore, the available inventory values that are obtained through the on-hand inventory page in Commerce headquarters, through the POS user interface (UI), and through e-Commerce inventory availability APIs aren't always 100-percent accurate in real time.</span></span>

<span data-ttu-id="37e42-107">许多零售商不会在电子商务店面中显示实际的库存值，而更愿意仅显示有关库存可用性状态的消息（例如，“有货”或“库存不足”），来告知客户某商品是可以购买还是有可能脱销。</span><span class="sxs-lookup"><span data-stu-id="37e42-107">Instead of showing actual inventory values in e-Commerce storefronts, many retailers prefer just to show messaging about inventory availability status (for example, "Available" or "Out of stock") to inform customers whether an item is available for purchase or potentially out of stock.</span></span> <span data-ttu-id="37e42-108">对于这种方法，确定库存可用性消息传递的库存缓冲区和库存级别必须可用并进行配置。</span><span class="sxs-lookup"><span data-stu-id="37e42-108">For this approach, inventory buffers and inventory levels that determine the inventory availability messaging must be made available and configured.</span></span>

## <a name="prerequisite-turn-on-the-inventory-buffers-and-inventory-levels-feature"></a><span data-ttu-id="37e42-109">先决条件：打开库存缓冲区和库存级别功能</span><span class="sxs-lookup"><span data-stu-id="37e42-109">Prerequisite: Turn on the inventory buffers and inventory levels feature</span></span>

<span data-ttu-id="37e42-110">库存缓冲区和库存级别的功能通过 Commerce 总部中的“功能管理”加以控制。</span><span class="sxs-lookup"><span data-stu-id="37e42-110">The feature for inventory buffers and inventory levels is controlled through Feature management in Commerce headquarters.</span></span> <span data-ttu-id="37e42-111">若要打开此功能，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="37e42-111">To turn on the feature, follow these steps.</span></span>

1. <span data-ttu-id="37e42-112">转到 **系统管理** \> **工作区** \> **功能管理**。</span><span class="sxs-lookup"><span data-stu-id="37e42-112">Go to **System administration** \> **Workspaces** \> **Feature management**.</span></span>
1. <span data-ttu-id="37e42-113">搜索 **启用库存缓冲区和库存级别** 功能，选择此行，然后选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="37e42-113">Search for the **Enable inventory buffers and inventory levels** feature, select its row, and then select **Enable now**.</span></span>

<span data-ttu-id="37e42-114">启用此功能后，您可以在 **Retail 和 Commerce \> 库存管理** 处找到库存级别。</span><span class="sxs-lookup"><span data-stu-id="37e42-114">After the feature is turned on, you can find inventory levels at **Retail and Commerce \> Inventory management**.</span></span>

## <a name="create-and-configure-an-inventory-level-profile"></a><span data-ttu-id="37e42-115">创建和配置库存级别配置文件</span><span class="sxs-lookup"><span data-stu-id="37e42-115">Create and configure an inventory level profile</span></span>

<span data-ttu-id="37e42-116">*库存级别配置文件* 确定是将给定的产品数量状态视为现货、缺货还是其他某个自定义状态。</span><span class="sxs-lookup"><span data-stu-id="37e42-116">An *inventory level profile* determines whether a given product quantity status is considered in stock, out of stock, or some other custom status.</span></span> <span data-ttu-id="37e42-117">您可以为每个法人创建和配置多个库存级别配置文件。</span><span class="sxs-lookup"><span data-stu-id="37e42-117">You can create and configure multiple inventory level profiles per legal entity.</span></span> <span data-ttu-id="37e42-118">每个配置文件由一组库存级别组成，每个级别由 *范围*、*代码* 和 *标签* 定义。</span><span class="sxs-lookup"><span data-stu-id="37e42-118">Each profile consists of a set of inventory levels, and each level is defined by a *range*, a *code*, and a *label*.</span></span>

- <span data-ttu-id="37e42-119">**范围** – 每个范围由 *开始数量* 和 *结束数量* 定义。</span><span class="sxs-lookup"><span data-stu-id="37e42-119">**Range** – Each range is defined by a *start quantity* and an *end quantity*.</span></span> <span data-ttu-id="37e42-120">如果数量值大于范围的开始数量且不大于结束数量，该数量值位于范围内。</span><span class="sxs-lookup"><span data-stu-id="37e42-120">A quantity value falls in a range if it's more than the start quantity of that range and not more than the end quantity.</span></span>
- <span data-ttu-id="37e42-121">**代码** – 代码是代表级别的内部缩写。</span><span class="sxs-lookup"><span data-stu-id="37e42-121">**Code** – A code is an internal abbreviation that represents the level.</span></span> <span data-ttu-id="37e42-122">直接与库存 API 集成的客户可以使用代码为给定的库存级别构建其他逻辑。</span><span class="sxs-lookup"><span data-stu-id="37e42-122">Customers who directly integrate with the inventory APIs can use codes to build additional logic for a given inventory level.</span></span> <span data-ttu-id="37e42-123">例如，当产品的库存级别代码为 **OOS**（“库存不足”）时，客户可以关闭产品的购买功能。</span><span class="sxs-lookup"><span data-stu-id="37e42-123">For example, they can turn off the purchase capability for a product when its inventory level code is **OOS** ("out of stock").</span></span>
- <span data-ttu-id="37e42-124">**标签** – 标签是一个有意义的面向客户的消息，向电子商务站点的客户传达库存级别。</span><span class="sxs-lookup"><span data-stu-id="37e42-124">**Label** – A label is a meaningful customer-facing message that conveys an inventory level to customers on an e-Commerce site.</span></span>

### <a name="create-an-inventory-level-profile"></a><span data-ttu-id="37e42-125">创建库存级别配置文件</span><span class="sxs-lookup"><span data-stu-id="37e42-125">Create an inventory level profile</span></span>

<span data-ttu-id="37e42-126">要创建库存级别配置文件，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="37e42-126">To create an inventory level profile, follow these steps.</span></span>

1. <span data-ttu-id="37e42-127">转到 **Retail 和 Commerce** \> **库存管理** \> **库存级别**。</span><span class="sxs-lookup"><span data-stu-id="37e42-127">Go to **Retail and Commerce** \> **Inventory management** \> **Inventory levels**.</span></span>
1. <span data-ttu-id="37e42-128">在操作窗格上，选择 **新建**，然后在 **配置文件 ID** 和 **描述** 字段中输入值。</span><span class="sxs-lookup"><span data-stu-id="37e42-128">On the Action Pane, select **New**, and then enter values in the **Profile ID** and **Description** fields.</span></span>
1. <span data-ttu-id="37e42-129">在 **范围** 快速选项卡上，选择 **添加** 添加新级别，然后在该级别的 **开始数量**、**结束数量**、**代码** 和 **标签** 列中输入值。</span><span class="sxs-lookup"><span data-stu-id="37e42-129">On the **Ranges** FastTab, select **Add** to add a new level, and then enter values in the **Start quantity**, **End quantity**, **Code**, and **Label** columns for that level.</span></span> <span data-ttu-id="37e42-130">重复此步骤添加更多级别。</span><span class="sxs-lookup"><span data-stu-id="37e42-130">Repeat this step to add more levels.</span></span> <span data-ttu-id="37e42-131">根据需要，您可以编辑数据网格中的值，也可以选择 **删除** 删除级别。</span><span class="sxs-lookup"><span data-stu-id="37e42-131">As you require, you can edit the values in the data grid, or you can select **Delete** to remove a level.</span></span>
1. <span data-ttu-id="37e42-132">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="37e42-132">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="37e42-133">创建新的配置文件后，将自动初始化两个库存级别：</span><span class="sxs-lookup"><span data-stu-id="37e42-133">When a new profile is created, two inventory levels are automatically initialized:</span></span>

- <span data-ttu-id="37e42-134">**OOS** –“库存不足”级别，范围的下限为负无穷大。</span><span class="sxs-lookup"><span data-stu-id="37e42-134">**OOS** – The "out of stock" level, where the lower bound of the range is negative infinity.</span></span> <span data-ttu-id="37e42-135">此级别的开始数量和代码无法编辑。</span><span class="sxs-lookup"><span data-stu-id="37e42-135">The start quantity and code can't be edited for this level.</span></span>
- <span data-ttu-id="37e42-136">**AVAIL** –“有货”级别，范围的上限为无穷大。</span><span class="sxs-lookup"><span data-stu-id="37e42-136">**AVAIL** – The "available" level, where the upper bound of the range is infinity.</span></span> <span data-ttu-id="37e42-137">此级别的结束数量和代码无法编辑。</span><span class="sxs-lookup"><span data-stu-id="37e42-137">The end quantity and code can't be edited for this level.</span></span>

> [!NOTE]
> <span data-ttu-id="37e42-138">此配置文件定义中的范围之间不能有间隔或重叠。</span><span class="sxs-lookup"><span data-stu-id="37e42-138">There can be no gaps or overlap between ranges in the profile definition.</span></span>

<span data-ttu-id="37e42-139">您可以使用操作窗格上的 **翻译** 按钮配置标签消息的本地化字符串。</span><span class="sxs-lookup"><span data-stu-id="37e42-139">You can use the **Translations** button on the Action Pane to configure localized strings for the label message.</span></span> <span data-ttu-id="37e42-140">然后，必须运行 **1110**（**全局配置**）配送计划作业来将本地化的字符串同步到渠道。</span><span class="sxs-lookup"><span data-stu-id="37e42-140">You must then run the **1110** (**Global configuration**) distribution schedule job to sync the localized strings to channels.</span></span>

### <a name="configure-an-inventory-level-profile"></a><span data-ttu-id="37e42-141">配置库存级别配置文件</span><span class="sxs-lookup"><span data-stu-id="37e42-141">Configure an inventory level profile</span></span>

<span data-ttu-id="37e42-142">您可以在产品类别级别或单个产品级别配置库存级别配置文件。</span><span class="sxs-lookup"><span data-stu-id="37e42-142">You can configure an inventory level profile at either the product category level or the individual product level.</span></span> <span data-ttu-id="37e42-143">为产品配置库存级别配置文件时，库存级别基于链接的配置文件中定义的范围确定。</span><span class="sxs-lookup"><span data-stu-id="37e42-143">When an inventory level profile is configured for a product, the inventory level is determined based on the ranges that are defined in the linked profile.</span></span> <span data-ttu-id="37e42-144">否则，“有货”或“库存不足”库存级别将基于产品是否有正现有数量确定。</span><span class="sxs-lookup"><span data-stu-id="37e42-144">Otherwise, the "available" or "out of stock" inventory level is determined based on whether the product has a positive on-hand quantity.</span></span>

<span data-ttu-id="37e42-145">要为类别配置库存级别配置文件，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="37e42-145">To configure an inventory level profile for a category, follow these steps.</span></span>

1. <span data-ttu-id="37e42-146">转到 **Retail 和 Commerce** \> **产品和类别** \> **商业产品层次结构**。</span><span class="sxs-lookup"><span data-stu-id="37e42-146">Go to **Retail and Commerce** \> **Products and categories** \> **Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="37e42-147">选择要为其配置库存级别配置文件的类别。</span><span class="sxs-lookup"><span data-stu-id="37e42-147">Select the category to configure an inventory level profile for.</span></span>
1. <span data-ttu-id="37e42-148">在 **销售产品属性** 快速选项卡上，选择一个法人。</span><span class="sxs-lookup"><span data-stu-id="37e42-148">On the **Sell product properties** FastTab, select a legal entity.</span></span>
1. <span data-ttu-id="37e42-149">在 **商务库存** 部分，在 **库存级别配置文件** 字段中，选择预定义的库存级别配置文件之一。</span><span class="sxs-lookup"><span data-stu-id="37e42-149">In the **Commerce inventory** section, in the **Inventory level profile** field, select one of the predefined inventory level profiles.</span></span>

<span data-ttu-id="37e42-150">您可以使用操作窗格上的 **更新产品** 按钮将类别级别的配置文件的值传播到类别的基础产品。</span><span class="sxs-lookup"><span data-stu-id="37e42-150">You can use the **Update products** button on the Action Pane to propagate the value of the category-level profile to the category's underlying products.</span></span> <span data-ttu-id="37e42-151">有关详细信息，请参阅[管理产品类别和产品](category-management-product-creation.md)。</span><span class="sxs-lookup"><span data-stu-id="37e42-151">For more information, see [Manage product categories and products](category-management-product-creation.md).</span></span>

<span data-ttu-id="37e42-152">要为已发布产品配置库存级别配置文件，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="37e42-152">To configure an inventory level profile for a released product, follow these steps.</span></span>

1. <span data-ttu-id="37e42-153">转至 **Retail 和 Commerce** \> **产品和类别** \> **按类别发布的产品**。</span><span class="sxs-lookup"><span data-stu-id="37e42-153">Go to **Retail and Commerce** \> **Products and categories** \> **Released products by category**.</span></span>
1. <span data-ttu-id="37e42-154">选择一个产品，然后打开其产品详细信息页。</span><span class="sxs-lookup"><span data-stu-id="37e42-154">Select a product, and then open its product details page.</span></span>
1. <span data-ttu-id="37e42-155">在 **销售** 快速选项卡上，在 **商务库存** 部分，在 **库存级别配置文件** 字段中，选择预定义的库存级别配置文件之一。</span><span class="sxs-lookup"><span data-stu-id="37e42-155">On the **Sell** FastTab, in the **Commerce inventory** section, in the **Inventory level profile** field, select one of the predefined inventory level profiles.</span></span>

<span data-ttu-id="37e42-156">创建新产品后，**库存级别配置文件** 字段与许多其他产品级属性一样，将被设置为为与产品关联的类别配置的值。</span><span class="sxs-lookup"><span data-stu-id="37e42-156">When a new product is created, the **Inventory level profile** field, like many other product-level attributes, will be set to the value that is configured for the category that the product is associated with.</span></span>

> [!NOTE]
> <span data-ttu-id="37e42-157">库存级别配置文件是特定于法人的属性。</span><span class="sxs-lookup"><span data-stu-id="37e42-157">The inventory level profile is a legal entity–specific attribute.</span></span> <span data-ttu-id="37e42-158">对于同一类别或产品，库存级别配置文件的值在各个法人之间可能会不同。</span><span class="sxs-lookup"><span data-stu-id="37e42-158">For the same category or product, the inventory level profile value can vary across legal entities.</span></span>

<span data-ttu-id="37e42-159">要将库存级别配置文件的配置同步到渠道，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="37e42-159">To sync the configurations of inventory level profiles to channels, follow these steps.</span></span>

1. <span data-ttu-id="37e42-160">转到 **Retail 和 Commerce** \> **Retail 和 Commerce IT** \> **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="37e42-160">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="37e42-161">运行 **1040**（**产品**）分配计划。</span><span class="sxs-lookup"><span data-stu-id="37e42-161">Run the **1040** (**Product**) distribution schedule.</span></span>

## <a name="configure-an-inventory-buffer"></a><span data-ttu-id="37e42-162">配置库存缓冲区</span><span class="sxs-lookup"><span data-stu-id="37e42-162">Configure an inventory buffer</span></span>

<span data-ttu-id="37e42-163">*库存缓冲区* 是用户定义的值，它从原始数量中减去商品的额外数量来计算估计数量。</span><span class="sxs-lookup"><span data-stu-id="37e42-163">The *inventory buffer* is a user-defined value that subtracts the additional quantity of an item from the original quantity to calculate the estimated quantity.</span></span> <span data-ttu-id="37e42-164">此估计数量为零售商提供一个安全的缓冲空间，让他们不会因销售比实际的现有库存量更多的产品而超额销售产品。</span><span class="sxs-lookup"><span data-stu-id="37e42-164">This estimated quantity gives retailers a safe buffer so that they don't oversell a product by selling more than its actual on-hand inventory.</span></span> <span data-ttu-id="37e42-165">您可以在产品类别级别或单个产品级别配置库存缓冲区。</span><span class="sxs-lookup"><span data-stu-id="37e42-165">You can configure the inventory buffer at either the product category level or the individual product level.</span></span> <span data-ttu-id="37e42-166">如果未指定库存缓冲区，将使用默认值 **0**（零）。</span><span class="sxs-lookup"><span data-stu-id="37e42-166">If no inventory buffer is specified, the default value of **0** (zero) is used.</span></span>

<span data-ttu-id="37e42-167">要为类别配置库存缓冲区，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="37e42-167">To configure the inventory buffer for a category, follow these steps.</span></span>

1. <span data-ttu-id="37e42-168">转到 **Retail 和 Commerce** \> **产品和类别** \> **商业产品层次结构**。</span><span class="sxs-lookup"><span data-stu-id="37e42-168">Go to **Retail and Commerce** \> **Products and categories** \> **Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="37e42-169">选择要为其配置库存缓冲区的类别。</span><span class="sxs-lookup"><span data-stu-id="37e42-169">Select the category to configure the inventory buffer for.</span></span>
1. <span data-ttu-id="37e42-170">在 **销售产品属性** 快速选项卡上，选择一个法人。</span><span class="sxs-lookup"><span data-stu-id="37e42-170">On the **Sell product properties** FastTab, select a legal entity.</span></span>
1. <span data-ttu-id="37e42-171">在 **商务库存** 部分，在 **库存缓冲区** 字段中，输入一个正值。</span><span class="sxs-lookup"><span data-stu-id="37e42-171">In the **Commerce inventory** section, in the **Inventory buffer** field, enter a positive value.</span></span>

<span data-ttu-id="37e42-172">您可以使用操作窗格上的 **更新产品** 按钮将类别级别缓冲区的值传播到类别的基础产品。</span><span class="sxs-lookup"><span data-stu-id="37e42-172">You can use the **Update products** button on the Action Pane to propagate the value of the category-level buffer to the category's underlying products.</span></span> <span data-ttu-id="37e42-173">有关详细信息，请参阅[管理产品类别和产品](category-management-product-creation.md)。</span><span class="sxs-lookup"><span data-stu-id="37e42-173">For more information, see [Manage product categories and products](category-management-product-creation.md).</span></span>

<span data-ttu-id="37e42-174">要为已发布产品配置库存缓冲区，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="37e42-174">To configure the inventory buffer for a released product, follow these steps.</span></span>

1. <span data-ttu-id="37e42-175">转至 **Retail 和 Commerce** \> **产品和类别** \> **按类别发布的产品**。</span><span class="sxs-lookup"><span data-stu-id="37e42-175">Go to **Retail and Commerce** \> **Products and categories** \> **Released products by category**.</span></span>
1. <span data-ttu-id="37e42-176">选择一个产品，然后打开其产品详细信息页。</span><span class="sxs-lookup"><span data-stu-id="37e42-176">Select a product, and then open its product details page.</span></span>
1. <span data-ttu-id="37e42-177">在 **销售** 快速选项卡上，在 **商务库存** 部分，在 **库存缓冲区** 字段中，输入一个正值。</span><span class="sxs-lookup"><span data-stu-id="37e42-177">On the **Sell** FastTab, in the **Commerce inventory** section, in the **Inventory buffer** field, enter a positive value.</span></span>

<span data-ttu-id="37e42-178">创建新产品后，**库存缓冲区** 字段将被设置为为与产品关联的类别配置的值。</span><span class="sxs-lookup"><span data-stu-id="37e42-178">When a new product is created, the **Inventory buffer** field will be set to the value that is configured for the category that the product is associated with.</span></span>

> [!NOTE]
> <span data-ttu-id="37e42-179">如果为产品同时配置了库存缓冲区和库存级别配置文件，该产品的估计数量（即原始数量减去缓冲值）将用于范围计算来确定库存级别。</span><span class="sxs-lookup"><span data-stu-id="37e42-179">If both the inventory buffer and inventory level profiles are configured for a product, the product's estimated quantity (that is, the original quantity minus the buffer value) will be used for range calculation to determine the inventory level.</span></span>

<span data-ttu-id="37e42-180">要将库存缓冲区的配置同步到渠道，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="37e42-180">To sync the configurations of inventory buffers to channels, follow these steps.</span></span>

1. <span data-ttu-id="37e42-181">转到 **Retail 和 Commerce** \> **Retail 和 Commerce IT** \> **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="37e42-181">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="37e42-182">运行 **1040**（**产品**）分配计划。</span><span class="sxs-lookup"><span data-stu-id="37e42-182">Run the **1040** (**Product**) distribution schedule.</span></span>

## <a name="use-inventory-buffers-and-inventory-levels-in-e-commerce-scenario"></a><span data-ttu-id="37e42-183">在电子商务方案中使用库存缓冲区和库存级别</span><span class="sxs-lookup"><span data-stu-id="37e42-183">Use inventory buffers and inventory levels in e-Commerce scenario</span></span>

<span data-ttu-id="37e42-184">Commerce 站点构建器使用 Commerce 总部中的库存缓冲区和库存级别功能来确定电子商务站点的库存可用性消息。</span><span class="sxs-lookup"><span data-stu-id="37e42-184">Commerce site builder uses the inventory buffer and inventory level capabilities in Commerce headquarters to determine inventory availability messaging on e-Commerce sites.</span></span> <span data-ttu-id="37e42-185">有关详细信息，请参阅[应用库存设置](inventory-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="37e42-185">For more information, see [Apply inventory settings](inventory-settings.md).</span></span>

<span data-ttu-id="37e42-186">或者，如果您与第三方电子商务解决方案集成，则可以使用 **GetEstimatedAvailability** 和 **GetEstimatedProductWarehouseAvailability** API 来在您的电子商务方案中显示产品的库存可用性。</span><span class="sxs-lookup"><span data-stu-id="37e42-186">Alternatively, if you integrate with a third-party e-Commerce solution, you can use the **GetEstimatedAvailability** and **GetEstimatedProductWarehouseAvailability** APIs to show inventory availability for a product in your e-Commerce scenario.</span></span> <span data-ttu-id="37e42-187">有关这些 API 的详细信息，请参阅[计算零售渠道的库存可用性](calculated-inventory-retail-channels.md)。</span><span class="sxs-lookup"><span data-stu-id="37e42-187">For more information about these APIs, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="37e42-188">库存缓冲区和库存级别的引入，使这些 API 可以返回基于总可用值和可用实际值确定的库存级别代码和标签消息。</span><span class="sxs-lookup"><span data-stu-id="37e42-188">The introduction of inventory buffers and inventory levels enables these APIs to return inventory level codes and label messages that are determined based on total available and available physical values.</span></span> <span data-ttu-id="37e42-189">API 可以进一步配置为确定库存量是否与消息一起返回，以及可用数量是否减掉库存缓冲值。</span><span class="sxs-lookup"><span data-stu-id="37e42-189">The APIs can be further configured to determine whether the inventory quantity is returned together with the message, and whether the available quantity is reduced by the inventory buffer value.</span></span>

<span data-ttu-id="37e42-190">要配置产品可用性 API 的响应，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="37e42-190">To configure the response of the product availability APIs, follow these steps.</span></span>

1. <span data-ttu-id="37e42-191">转到 **Retail 和 Commerce** \> **总部设置** \> **参数** \> **Commerce 参数**。</span><span class="sxs-lookup"><span data-stu-id="37e42-191">Go to **Retail and commerce** \> **Headquarters setup** \> **Parameters** \> **Commerce parameters**.</span></span>
1. <span data-ttu-id="37e42-192">在 **商店库存** 部分，在 **库存** 选项卡上，在 **电子商务产品可用性 API** 字段中，选择一个值。</span><span class="sxs-lookup"><span data-stu-id="37e42-192">In the **Store inventory** section, on the **Inventory** tab, in the **Product availability APIs for e-Commerce** field, select a value.</span></span>
1. <span data-ttu-id="37e42-193">要将设置应用于渠道，请运行 **1110**（**全局配置**）配送计划作业。</span><span class="sxs-lookup"><span data-stu-id="37e42-193">To apply the settings to channels, run the **1110** (**Global configuration**) distribution schedule job.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="37e42-194">其他资源</span><span class="sxs-lookup"><span data-stu-id="37e42-194">Additional resources</span></span>

[<span data-ttu-id="37e42-195">管理产品类别和产品</span><span class="sxs-lookup"><span data-stu-id="37e42-195">Manage product categories and products</span></span>](category-management-product-creation.md)

[<span data-ttu-id="37e42-196">应用库存设置</span><span class="sxs-lookup"><span data-stu-id="37e42-196">Apply inventory settings</span></span>](inventory-settings.md)

[<span data-ttu-id="37e42-197">计算零售渠道的库存现有量</span><span class="sxs-lookup"><span data-stu-id="37e42-197">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

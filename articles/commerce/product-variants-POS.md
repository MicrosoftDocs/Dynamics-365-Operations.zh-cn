---
title: 销售点 (POS) 中的库存查找
description: 本主题介绍可用于在销售点 (POS) 中查看库存信息的选项。
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: 1d6133d80d7674a1d896bc19a743a6bd4d0fb40f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021784"
---
# <a name="inventory-lookup-in-the-point-of-sale-pos"></a><span data-ttu-id="da21d-103">销售点 (POS) 中的库存查找</span><span class="sxs-lookup"><span data-stu-id="da21d-103">Inventory lookup in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="da21d-104">销售点 (POS) 库存查找通过连接商店、POS 和后端管理系统，帮助零售商获得卓越的实时运营体验和洞察体验。</span><span class="sxs-lookup"><span data-stu-id="da21d-104">Inventory lookup in the point of sale (POS) helps retailers achieve real-time operational excellence and gain insights by connecting stores, the POS, and the back office.</span></span> <span data-ttu-id="da21d-105">此功能提供精确的商店和配送中心产品库存实时视图。</span><span class="sxs-lookup"><span data-stu-id="da21d-105">This functionality provides an accurate real-time view of product inventory across stores and distribution centers.</span></span> <span data-ttu-id="da21d-106">还通过实时改进库存规划，帮助零售商提高效率和节约成本。</span><span class="sxs-lookup"><span data-stu-id="da21d-106">It also helps retailers drive additional efficiencies and cost savings by improving inventory planning in real time.</span></span>

<span data-ttu-id="da21d-107">精确的组织库存实时视图可帮助店员提供及时、优秀的客户服务。</span><span class="sxs-lookup"><span data-stu-id="da21d-107">An accurate real-time view of inventory across an organization helps store associates provide timely, superior customer service.</span></span> <span data-ttu-id="da21d-108">最重要的时间是客户准备好做出采购决定的时间。</span><span class="sxs-lookup"><span data-stu-id="da21d-108">The moment that matters most is the moment when the customer is ready to make a purchase decision.</span></span> <span data-ttu-id="da21d-109">商店收银员掌握实时库存信息至关重要，因为这样可以准确地做出产品交付和交货承诺。</span><span class="sxs-lookup"><span data-stu-id="da21d-109">It's important that cashiers in the store have real-time inventory information at their fingertips, so that they can accurately promise product delivery and pickup.</span></span>

<span data-ttu-id="da21d-110">可以从 **Retail Modern POS** 工作区或 **Retail Cloud POS** 工作区打开**库存查找**页。</span><span class="sxs-lookup"><span data-stu-id="da21d-110">You can open the **Inventory lookup** page from the **Retail Modern POS** workspace or the **Retail Cloud POS** workspace.</span></span>

![POS 主页中的“库存查找”磁贴](media/POSHomepage.png)

<span data-ttu-id="da21d-112">可在**库存查找**页中使用数字键盘输入产品编号。</span><span class="sxs-lookup"><span data-stu-id="da21d-112">On the **Inventory lookup** page, you can use the numeric keyboard to enter a product number.</span></span> <span data-ttu-id="da21d-113">然后可以查看多个商店和仓库的现有数量。</span><span class="sxs-lookup"><span data-stu-id="da21d-113">You can then view the on-hand quantity for multiple stores and warehouses.</span></span>

![标准库存查找页](media/InventoryLookUp.png)

<span data-ttu-id="da21d-115">还将显示各处的**已预留**数量和**已订购**数量。</span><span class="sxs-lookup"><span data-stu-id="da21d-115">**Reserved** and **Ordered** quantities are also shown for each location.</span></span>

- <span data-ttu-id="da21d-116">**已预留** – 此数量指的是来自后端管理系统的所在位置指定产品编号的**实际预留**值。</span><span class="sxs-lookup"><span data-stu-id="da21d-116">**Reserved** – This quantity refers to the **Physical reserved** value from the back office for the specified product number at the location.</span></span>
- <span data-ttu-id="da21d-117">**已订购** – 此数量指的是来自后端管理系统的所在位置指定产品编号的**订购总量**值。</span><span class="sxs-lookup"><span data-stu-id="da21d-117">**Ordered** – This quantity refers to the **Ordered in total** value from the back office for the specified product number at the location.</span></span>

## <a name="locations-that-inventory-availability-information-is-shown-for"></a><span data-ttu-id="da21d-118">显示的库存可用性信息所属的位置</span><span class="sxs-lookup"><span data-stu-id="da21d-118">Locations that inventory availability information is shown for</span></span>

<span data-ttu-id="da21d-119">位置列表中包含两类实体：</span><span class="sxs-lookup"><span data-stu-id="da21d-119">The list of locations includes two types of entities:</span></span>

- <span data-ttu-id="da21d-120">**商店** – 此列表显示使用商店定位符组为总部中的当前商店配置的商店。</span><span class="sxs-lookup"><span data-stu-id="da21d-120">**Stores** – The list shows stores that are configured by using the store locator group for the current store in the Headquarters.</span></span>
- <span data-ttu-id="da21d-121">**配送中心** – 可以在 Commerce 中配置各种配送中心（如仓库）。</span><span class="sxs-lookup"><span data-stu-id="da21d-121">**Distribution centers** – Various types of distribution centers (such as warehouses) can be configured in Commerce.</span></span> <span data-ttu-id="da21d-122">但是，此列表仅显示**标准**默认类型的配送中心的库存可用性信息。</span><span class="sxs-lookup"><span data-stu-id="da21d-122">However, the list shows inventory availability information only for distribution centers of the **Standard** default type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="da21d-123">不对 POS 显示**运输**、**检验**和**在途货物**类型的仓库的库存可用性信息。</span><span class="sxs-lookup"><span data-stu-id="da21d-123">Inventory availability information isn't shown for warehouses of the **Transit**, **Quarantine**, and **Goods in Route** types for the POS.</span></span>

<span data-ttu-id="da21d-124">在**库存查找**页中，除了每家商店的当前现货数量、保留数量和订购数量，还可以查看可承诺 (ATP) 数量。</span><span class="sxs-lookup"><span data-stu-id="da21d-124">On the **Inventory lookup** page, you can view available to promise (ATP) quantities for each store, in addition to the current on-hand quantities, reserved quantities, and ordered quantities.</span></span> <span data-ttu-id="da21d-125">选择要查看的 ATP 信息所属商店，然后选择**显示商店可用性**。</span><span class="sxs-lookup"><span data-stu-id="da21d-125">Select the store to view the ATP information for, and then select **Show store availability**.</span></span>

![ATP 数量](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a><span data-ttu-id="da21d-127">打开基于维度的矩阵视图以显示所有变型</span><span class="sxs-lookup"><span data-stu-id="da21d-127">Opening the Dimension based matrix view to show all variants</span></span>

<span data-ttu-id="da21d-128">在基础产品的**产品详细信息**页中或**库存查找**页中，从页面底部应用栏选择**查看所有变型**。</span><span class="sxs-lookup"><span data-stu-id="da21d-128">On the **Product details** page of a product master, or on the **Inventory lookup** page, select **View all variants** from the app-bar at bottom of the page.</span></span> <span data-ttu-id="da21d-129">首次启动时这些页面中的**基于维度的矩阵**视图显示当前商店所有产品变型的库存可用性信息。</span><span class="sxs-lookup"><span data-stu-id="da21d-129">The **Dimension based matrix** view for the initial launch from these pages shows the inventory availability information for all variants of a product for the current store.</span></span>

> [!NOTE]
> <span data-ttu-id="da21d-130">**查看所有变型**按钮仅适用于具有产品变型的物料基础产品。</span><span class="sxs-lookup"><span data-stu-id="da21d-130">The **View all variants** button is available only for item product masters that have product variants.</span></span> <span data-ttu-id="da21d-131">不适用于独立产品或套件。</span><span class="sxs-lookup"><span data-stu-id="da21d-131">It isn't available for standalone products or kits.</span></span>

![“库存查找”页上的“查看所有变型”按钮](media/StandardToMatrix.png)

<span data-ttu-id="da21d-133">选择基础产品**产品详细信息**页或**库存查找**页上的**查看所有变型**，但不选择位置，以便转至**基于维度的矩阵**视图以查看当前商店所有产品变型的库存可用性信息。</span><span class="sxs-lookup"><span data-stu-id="da21d-133">Select **View all variants** on the **Product details** page of a product master, or on the **Inventory lookup** page, without selecting a location, to go to the **Dimension based matrix** view to view the inventory availability information for all variants of a product for the current store.</span></span>

![“库存查找”页的“基于维度的矩阵”视图](media/Matrix.png)

> [!NOTE]
> <span data-ttu-id="da21d-135">在上图中，维度按字母顺序显示，因为没有为所选产品配置维度的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="da21d-135">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="da21d-136">在**基于维度的矩阵**视图中，右下角的产品变型单元中包含现有量值。</span><span class="sxs-lookup"><span data-stu-id="da21d-136">In the **Dimension based matrix** view, the cells for the product variants include an on-hand value in the lower-right corner.</span></span> <span data-ttu-id="da21d-137">下表介绍各个值的含义。</span><span class="sxs-lookup"><span data-stu-id="da21d-137">The following table explains the meaning of the various values.</span></span>

| <span data-ttu-id="da21d-138">现有量值</span><span class="sxs-lookup"><span data-stu-id="da21d-138">On-hand value</span></span>                            | <span data-ttu-id="da21d-139">说明</span><span class="sxs-lookup"><span data-stu-id="da21d-139">Description</span></span> |
|------------------------------------------|-------------|
| <span data-ttu-id="da21d-140">大于 0（零）的数值</span><span class="sxs-lookup"><span data-stu-id="da21d-140">Numeric value that is more than 0 (zero)</span></span> | <span data-ttu-id="da21d-141">已将一个变型发放到所选位置，而您可以执行该单元中的更多操作。</span><span class="sxs-lookup"><span data-stu-id="da21d-141">A variant has been released to the selected location, and you can perform additional actions in the cell.</span></span> <span data-ttu-id="da21d-142">（这些操作将在本主题的后面部分进行更详细的描述。）</span><span class="sxs-lookup"><span data-stu-id="da21d-142">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="da21d-143">**0**（零）</span><span class="sxs-lookup"><span data-stu-id="da21d-143">**0** (zero)</span></span>                             | <span data-ttu-id="da21d-144">已将一个变型发放到所选位置，但是物料在所选位置不可用。</span><span class="sxs-lookup"><span data-stu-id="da21d-144">A variant has been released to the selected location, but the item isn't available in selected location.</span></span> <span data-ttu-id="da21d-145">但是，可以执行该单元中的其他操作。</span><span class="sxs-lookup"><span data-stu-id="da21d-145">However, you can perform additional actions in the cell.</span></span> <span data-ttu-id="da21d-146">（这些操作将在本主题的后面部分进行更详细的描述。）</span><span class="sxs-lookup"><span data-stu-id="da21d-146">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="da21d-147">**不可用**或停用的单元</span><span class="sxs-lookup"><span data-stu-id="da21d-147">**n/a** or an inactive cell</span></span>              | <span data-ttu-id="da21d-148">尚未将一个变型发放到所选位置，所以不能执行该单元中的更多操作。</span><span class="sxs-lookup"><span data-stu-id="da21d-148">A variant hasn't been released to the selected location, and you can't perform additional actions in the cell.</span></span> |

<span data-ttu-id="da21d-149">也可以通过选择要使用的新维度更改维度的数据透视。</span><span class="sxs-lookup"><span data-stu-id="da21d-149">You can also change the pivot for dimensions by selecting the new dimension to use.</span></span>

![更改数据透视](media/ChangePivot.png)

![已更改的数据透视](media/PivotChanged.png)

> [!NOTE]
> <span data-ttu-id="da21d-152">在前面的图，所选产品的维度显示顺序是自定义的（不按字母）。</span><span class="sxs-lookup"><span data-stu-id="da21d-152">In the preceding illustrations, the display order of the dimensions for the selected product is custom (non-alphabetic).</span></span> <span data-ttu-id="da21d-153">而是基于后端管理系统中设置的维度显示顺序。</span><span class="sxs-lookup"><span data-stu-id="da21d-153">It's based on the dimension display order that is set in the back office.</span></span>

<span data-ttu-id="da21d-154">此外，在**基于维度的矩阵**视图中，可以执行更多操作以帮助提高店员的工作效率。</span><span class="sxs-lookup"><span data-stu-id="da21d-154">Additionally, in the **Dimension based matrix** view, more actions can be performed to help boost a store associate's productivity.</span></span> <span data-ttu-id="da21d-155">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="da21d-155">Here are some examples:</span></span>

- <span data-ttu-id="da21d-156">更改商店位置以查找其他位置所有产品变型的库存可用性。</span><span class="sxs-lookup"><span data-stu-id="da21d-156">Change the store location to look up the inventory availability of all product variants at other locations.</span></span> <span data-ttu-id="da21d-157">这些位置包括商店定位符组中的其他商店和**标准**默认类型的配送中心。</span><span class="sxs-lookup"><span data-stu-id="da21d-157">These locations include other stores in the store locator group and distribution centers of the **Standard** default type.</span></span>
- <span data-ttu-id="da21d-158">通过使用现金提货、商店内提货或发货到地址将单个产品变型卖给客户。</span><span class="sxs-lookup"><span data-stu-id="da21d-158">Sell an individual product variant to a customer by using cash and carry, in-store pickup, or shipment to an address.</span></span>
- <span data-ttu-id="da21d-159">为客户提供特定位置单个产品变型的 ATP 信息。</span><span class="sxs-lookup"><span data-stu-id="da21d-159">Provide the customer with ATP information for an individual product variant at a specific location.</span></span>

![更多变型操作磁贴](media/VariantActions.png)

> [!NOTE]
> <span data-ttu-id="da21d-161">在上图中，维度按字母顺序显示，因为没有为所选产品配置维度的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="da21d-161">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="da21d-162">下表提供有关更多可用操作的详细信息。</span><span class="sxs-lookup"><span data-stu-id="da21d-162">The following table provides more information about the additional actions that are available.</span></span>

| <span data-ttu-id="da21d-163">行动</span><span class="sxs-lookup"><span data-stu-id="da21d-163">Action</span></span>               | <span data-ttu-id="da21d-164">说明</span><span class="sxs-lookup"><span data-stu-id="da21d-164">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="da21d-165">立即销售</span><span class="sxs-lookup"><span data-stu-id="da21d-165">Sell now</span></span>             | <span data-ttu-id="da21d-166">将所选物料变型添加到交易记录中，并将用户重定向到交易记录屏幕。</span><span class="sxs-lookup"><span data-stu-id="da21d-166">Add the selected item variant to the transaction, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="da21d-167">（如果所选位置是配送中心，则此操作不可用。）</span><span class="sxs-lookup"><span data-stu-id="da21d-167">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="da21d-168">在商店中提货</span><span class="sxs-lookup"><span data-stu-id="da21d-168">Pick up in store</span></span>     | <span data-ttu-id="da21d-169">为将从所选位置领取的产品变型创建客户订单，然后将用户重定向到交易记录屏幕。</span><span class="sxs-lookup"><span data-stu-id="da21d-169">Create a customer order for the product variant that will be picked up from the selected location, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="da21d-170">（如果所选位置是配送中心，则此操作不可用。）</span><span class="sxs-lookup"><span data-stu-id="da21d-170">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="da21d-171">装运产品</span><span class="sxs-lookup"><span data-stu-id="da21d-171">Ship product</span></span>         | <span data-ttu-id="da21d-172">为将从所选位置发货的产品变型创建客户订单，然后将用户重定向到交易记录屏幕。</span><span class="sxs-lookup"><span data-stu-id="da21d-172">Create a customer order for the product variant that will be shipped from the selected location, and redirect the user to the transaction screen.</span></span> |
| <span data-ttu-id="da21d-173">可用性</span><span class="sxs-lookup"><span data-stu-id="da21d-173">Availability</span></span>         | <span data-ttu-id="da21d-174">显示所选位置所选变型组合的 ATP 信息。</span><span class="sxs-lookup"><span data-stu-id="da21d-174">Show the ATP information for the selected variant combination for the selected location.</span></span> |
| <span data-ttu-id="da21d-175">显示所有位置</span><span class="sxs-lookup"><span data-stu-id="da21d-175">Show all locations</span></span>   | <span data-ttu-id="da21d-176">切换到标准库存查找视图，并突出显示商店定位符组中所有商店内和**标准/默认**类型的配送中心内的物料变型的库存可用性信息。</span><span class="sxs-lookup"><span data-stu-id="da21d-176">Switch to the standard inventory lookup view, and highlight inventory availability information for the item variant across all stores in the store locator group, and also in distribution centers of the **Standard/Default** type.</span></span> |
| <span data-ttu-id="da21d-177">查看产品详细信息</span><span class="sxs-lookup"><span data-stu-id="da21d-177">View product details</span></span> | <span data-ttu-id="da21d-178">将用户重定向到关联的基础产品的**产品详细信息**页。</span><span class="sxs-lookup"><span data-stu-id="da21d-178">Redirect the user to the **Product details** page of the associated product master.</span></span> |
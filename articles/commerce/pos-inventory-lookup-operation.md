---
title: POS 中的库存查找操作
description: 本主题介绍如何使用 Dynamics 365 Commerce 销售点 (POS) 中的库存查找操作查看产品跨商店和仓库的现有库存量的可用性。
author: boycezhu
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: 873c6413c14d2ee8315c149ee9c495bb59dbd930
ms.sourcegitcommit: 11ca5863175150b6c39f47a9322caa2186727a26
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025440"
---
# <a name="inventory-lookup-operation-in-pos"></a><span data-ttu-id="41504-103">POS 中的库存查找操作</span><span class="sxs-lookup"><span data-stu-id="41504-103">Inventory lookup operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="41504-104">本主题介绍如何使用 Dynamics 365 Commerce 销售点 (POS) 中的库存查找操作查看产品跨商店和仓库的现有库存量的可用性。</span><span class="sxs-lookup"><span data-stu-id="41504-104">This topic describes how to use the inventory lookup operation in Dynamics 365 Commerce point of sale (POS) to view the on-hand inventory availability of products across stores and warehouses.</span></span>

<span data-ttu-id="41504-105">精确的组织库存视图可帮助店员提供及时、高效的客户服务。</span><span class="sxs-lookup"><span data-stu-id="41504-105">An accurate view of inventory across an organization helps store associates provide timely, effective customer service.</span></span> <span data-ttu-id="41504-106">最重要的时间是客户准备好做出采购决定的时间。</span><span class="sxs-lookup"><span data-stu-id="41504-106">The moment that matters most is the moment when a customer is ready to make a purchase decision.</span></span> <span data-ttu-id="41504-107">零售商店的收银员掌握实时或准实时的库存信息至关重要，因为这样可以准确地做出产品交付和交货承诺。</span><span class="sxs-lookup"><span data-stu-id="41504-107">It's important that cashiers in a retail store have real-time or near real-time inventory information at their fingertips, so that they can accurately promise product delivery and pickup.</span></span>

<span data-ttu-id="41504-108">通过将商店与 Commerce headquarters 连接，Commerce POS 中的库存查找操作可以帮助零售商实现卓越的运营并获得见解。</span><span class="sxs-lookup"><span data-stu-id="41504-108">The inventory lookup operation in Commerce POS helps retailers achieve operational excellence and gain insights by connecting stores with Commerce headquarters.</span></span> <span data-ttu-id="41504-109">此功能提供跨商店和仓库的产品库存可用性视图。</span><span class="sxs-lookup"><span data-stu-id="41504-109">This functionality provides an inventory availability view of products across stores and warehouses.</span></span> <span data-ttu-id="41504-110">还通过实时改进库存规划，帮助零售商提高效率和节约成本。</span><span class="sxs-lookup"><span data-stu-id="41504-110">It also helps retailers drive additional efficiencies and cost savings by improving inventory planning in real time.</span></span>

<span data-ttu-id="41504-111">当从 POS 应用程序启动库存查询操作时，POS 收银员使用数字键盘输入产品编号来查询库存信息。</span><span class="sxs-lookup"><span data-stu-id="41504-111">When the inventory lookup operation is started from the POS application, the POS cashier uses the numeric keyboard to enter a product number to query its inventory information.</span></span> <span data-ttu-id="41504-112">如果输入的产品有变型，收银员可以选择维度或其他值来检查特定产品变型的库存信息。</span><span class="sxs-lookup"><span data-stu-id="41504-112">If the product entered has variants, the cashier can optionally select dimensions or other values to check inventory information of a specific product variant.</span></span>

## <a name="inventory-lookup-list-view-for-individual-products"></a><span data-ttu-id="41504-113">各个产品的库存查找列表视图</span><span class="sxs-lookup"><span data-stu-id="41504-113">Inventory lookup list view for individual products</span></span>

<span data-ttu-id="41504-114">对于单个产品，库存查询操作提供库存查找列表视图，其中显示某个位置列表的以下产品信息：</span><span class="sxs-lookup"><span data-stu-id="41504-114">For an individual product, the inventory lookup operation provides an inventory lookup list view showing the following product information for a list of locations:</span></span>

- <span data-ttu-id="41504-115">**库存** - 指产品的“实际可用”数量。</span><span class="sxs-lookup"><span data-stu-id="41504-115">**Inventory** - Refers to the "available physical" quantity of a product.</span></span>
- <span data-ttu-id="41504-116">**已预留** - 指从总部检索的“实际预留”数量。</span><span class="sxs-lookup"><span data-stu-id="41504-116">**Reserved** - Refers to the "physical reserved" quantity retrieved from headquarters.</span></span>
- <span data-ttu-id="41504-117">**已订购** - 指从总部检索的“订购总量”。</span><span class="sxs-lookup"><span data-stu-id="41504-117">**Ordered** - Refers to the "ordered in total" quantity retrieved from headquarters.</span></span>
- <span data-ttu-id="41504-118">**单位** - 指在总部配置的库存度量单位。</span><span class="sxs-lookup"><span data-stu-id="41504-118">**Unit** - Refers to the inventory unit of measure configured in headquarters.</span></span>

<span data-ttu-id="41504-119">位置列表视图包括在当前商店链接到的履行组中配置的所有商店和仓库，如以下示例图像所示。</span><span class="sxs-lookup"><span data-stu-id="41504-119">The list view of locations includes all stores and warehouses that are configured in the fulfillment groups that the current store is linked to, as shown in the following example image.</span></span>

![库存查找操作列表视图](media/inventory-lookup-list-view.png)

<span data-ttu-id="41504-121">POS 应用栏上提供以下操作：</span><span class="sxs-lookup"><span data-stu-id="41504-121">The following actions are available on the POS app bar:</span></span>

- <span data-ttu-id="41504-122">**排序** - 此操作让 POS 用户可以根据各个条件对列表视图中的数据进行排序。</span><span class="sxs-lookup"><span data-stu-id="41504-122">**Sort** - This action lets the POS user sort the data in the list view based on various criteria.</span></span> <span data-ttu-id="41504-123">基于位置的排序是默认排序选项。</span><span class="sxs-lookup"><span data-stu-id="41504-123">Location-based sorting is the default sort option.</span></span> 
  - <span data-ttu-id="41504-124">**地理位置**（对比当前商店，从最近位置到最远位置）</span><span class="sxs-lookup"><span data-stu-id="41504-124">**Geo location** (from the closest location to the farthest location, compared with the current store)</span></span>
  - <span data-ttu-id="41504-125">**名称**（升序或降序）</span><span class="sxs-lookup"><span data-stu-id="41504-125">**Name** (in ascending or descending order)</span></span>
  - <span data-ttu-id="41504-126">**商店编号**（升序或降序）</span><span class="sxs-lookup"><span data-stu-id="41504-126">**Store number** (in ascending or descending order)</span></span>
  - <span data-ttu-id="41504-127">**库存**（降序）</span><span class="sxs-lookup"><span data-stu-id="41504-127">**Inventory** (in descending order)</span></span>
  - <span data-ttu-id="41504-128">**已预留**（降序）</span><span class="sxs-lookup"><span data-stu-id="41504-128">**Reserved** (in descending order)</span></span>
  - <span data-ttu-id="41504-129">**已订购**（降序）</span><span class="sxs-lookup"><span data-stu-id="41504-129">**Ordered** (in descending order)</span></span>
- <span data-ttu-id="41504-130">**筛选** - 通过此操作，POS 用户可以查看特定位置的筛选数据。</span><span class="sxs-lookup"><span data-stu-id="41504-130">**Filter** - This action lets the POS user view filtered data for a specific location.</span></span>
- <span data-ttu-id="41504-131">**显示商店可用性** - 此操作让 POS 用户可以查看所选商店中产品的可承诺 (ATP) 数量。</span><span class="sxs-lookup"><span data-stu-id="41504-131">**Show store availability** - This action lets the POS user view the available-to-promise (ATP) quantities for a product in the selected store.</span></span>
- <span data-ttu-id="41504-132">**显示商店位置** - 此操作将打开一个单独的页面来显示所选商店的地图视图、地址和商店营业时间。</span><span class="sxs-lookup"><span data-stu-id="41504-132">**Show store location** - This action opens a separate page to show the map view, address, and store hours for the selected store.</span></span>
- <span data-ttu-id="41504-133">**店内提货** - 此操作为将从所选商店提货的产品创建客户订单，然后将用户重定向到交易屏幕。</span><span class="sxs-lookup"><span data-stu-id="41504-133">**Pick up in store** - This action creates a customer order for the product that will be picked up from the selected store, and redirects the user to the transaction screen.</span></span>
- <span data-ttu-id="41504-134">**装运产品** - 此操作为将从所选商店装运的产品创建客户订单，然后将用户重定向到交易屏幕。</span><span class="sxs-lookup"><span data-stu-id="41504-134">**Ship product** - This action creates a customer order for the product that will be shipped from the selected store, and redirects the user to the transaction screen.</span></span>
- <span data-ttu-id="41504-135">**查看所有变型** - 对于具有变型的产品，此操作从列表视图切换为显示该产品所有变型的库存信息的矩阵视图。</span><span class="sxs-lookup"><span data-stu-id="41504-135">**View all variants** - For a product with variants, this action switches from a list view to a matrix view that displays inventory information for all variants of the product.</span></span>
- <span data-ttu-id="41504-136">**添加到交易** - 此操作将产品添加到购物车，并将用户重定向到交易屏幕。</span><span class="sxs-lookup"><span data-stu-id="41504-136">**Add to transaction** - This action adds the product to the cart and redirects the user to the transaction screen.</span></span>

> [!NOTE]
> <span data-ttu-id="41504-137">对于基于位置的排序，位置与当前商店之间的距离由 Commerce headquarters 中定义的坐标（纬度和经度）确定。</span><span class="sxs-lookup"><span data-stu-id="41504-137">For a location-based sort, the distance between a location and current store is determined by the coordinates (latitude and longitude) defined in Commerce headquarters.</span></span> <span data-ttu-id="41504-138">对于商店，位置信息在与商店关联的运营单位的主要地址中定义。</span><span class="sxs-lookup"><span data-stu-id="41504-138">For a store, the location information is defined in the primary address of the operating unit associated with the store.</span></span> <span data-ttu-id="41504-139">对于非商店仓库，位置信息在仓库地址中定义。</span><span class="sxs-lookup"><span data-stu-id="41504-139">For a non-store warehouse, the location information is defined in the warehouse address.</span></span> <span data-ttu-id="41504-140">如果当前商店没有正确定义坐标，基于位置的排序选项将在列表顶部显示当前商店，然后按名称对其他位置进行排序。</span><span class="sxs-lookup"><span data-stu-id="41504-140">If the current store doesn't have coordinates properly defined, the location-based sort option will display the current store at the top of the list and then sort other locations by name.</span></span>

> [!NOTE]
> <span data-ttu-id="41504-141">**显示商店可用性**、**显示商店位置**、**店内提货** 和 **装运产品** 操作对非商店位置不可用。</span><span class="sxs-lookup"><span data-stu-id="41504-141">The **Show store availability**, **Show store location**, **Pick up in store**, and **Ship product** actions are not available for non-store locations.</span></span>

## <a name="inventory-lookup-matrix-view-for-variants"></a><span data-ttu-id="41504-142">变型的库存查找矩阵视图</span><span class="sxs-lookup"><span data-stu-id="41504-142">Inventory lookup matrix view for variants</span></span>

<span data-ttu-id="41504-143">对于具有变型的基础产品，库存查找操作还提供基于维度的矩阵视图，该视图显示选定位置基础产品的所有变型的库存可用性信息。</span><span class="sxs-lookup"><span data-stu-id="41504-143">For a master product with variants, the inventory lookup operation also provides a dimension-based matrix view that displays inventory availability information for all variants of the master product at a selected location.</span></span> <span data-ttu-id="41504-144">默认情况下，矩阵视图显示当前商店的数据。</span><span class="sxs-lookup"><span data-stu-id="41504-144">By default, the matrix view shows data for the current store.</span></span> <span data-ttu-id="41504-145">您可以使用应用栏上的 **商店** 操作查找当前商店链接到的履行组中配置的其他商店的库存信息。</span><span class="sxs-lookup"><span data-stu-id="41504-145">You can use the **Store** action on the app bar to look up inventory information at other stores configured in the fulfillment groups that the current store is linked to.</span></span>

<span data-ttu-id="41504-146">以下示例图像显示了 POS 中的库存查找矩阵视图。</span><span class="sxs-lookup"><span data-stu-id="41504-146">The following example image shows the inventory lookup matrix view in POS.</span></span>

![库存查找操作矩阵视图](media/inventory-lookup-matrix-view.png)

<span data-ttu-id="41504-148">在此矩阵视图中，每个单元代表一个单独的变型，在右下角显示现有库存量（实际可用）值，在左上角显示 **已预留**（实际预留）和 **已订购**（订购总量）值。</span><span class="sxs-lookup"><span data-stu-id="41504-148">In the matrix view, each cell represents an individual variant, and displays an on-hand inventory (available physical) value in the lower-right corner, as well as **reserved** (physical reserved) and **ordered** (ordered in total) values in the upper-left corner.</span></span> <span data-ttu-id="41504-149">下表说明各个现有值的含义。</span><span class="sxs-lookup"><span data-stu-id="41504-149">The following table explains the meaning of the various on-hand values.</span></span>

| <span data-ttu-id="41504-150">现有量值</span><span class="sxs-lookup"><span data-stu-id="41504-150">On-hand value</span></span>                            | <span data-ttu-id="41504-151">说明</span><span class="sxs-lookup"><span data-stu-id="41504-151">Description</span></span> |
|------------------------------------------|-------------|
| <span data-ttu-id="41504-152">大于 0（零）的数值</span><span class="sxs-lookup"><span data-stu-id="41504-152">Numeric value that is more than 0 (zero)</span></span> | <span data-ttu-id="41504-153">已将一个变型发放到所选位置，而您可以执行该单元中的更多操作。</span><span class="sxs-lookup"><span data-stu-id="41504-153">A variant has been released to the selected location, and you can perform additional actions in the cell.</span></span> |
| <span data-ttu-id="41504-154">**0**（零）</span><span class="sxs-lookup"><span data-stu-id="41504-154">**0** (zero)</span></span>                             | <span data-ttu-id="41504-155">已将一个变型发放到所选位置，但是物料在所选位置不可用。</span><span class="sxs-lookup"><span data-stu-id="41504-155">A variant has been released to the selected location, but the item isn't available at the selected location.</span></span> <span data-ttu-id="41504-156">您可以在单元中执行其他操作。</span><span class="sxs-lookup"><span data-stu-id="41504-156">You can perform additional actions in the cell.</span></span> |
| <span data-ttu-id="41504-157">**不可用** 或停用的单元</span><span class="sxs-lookup"><span data-stu-id="41504-157">**n/a**, or an inactive cell</span></span>              | <span data-ttu-id="41504-158">尚未将一个变型发放到所选位置，所以不能执行该单元中的更多操作。</span><span class="sxs-lookup"><span data-stu-id="41504-158">A variant hasn't been released to the selected location, and you can't perform additional actions in the cell.</span></span> |

<span data-ttu-id="41504-159">矩阵视图中维度值的显示顺序基于 Commerce headquarters 中的维度显示顺序配置。</span><span class="sxs-lookup"><span data-stu-id="41504-159">The display order of the dimension values in the matrix view is based on the dimension display order configuration in Commerce headquarters.</span></span> <span data-ttu-id="41504-160">您可以通过选择要使用的新维度来更改维度显示顺序配置。</span><span class="sxs-lookup"><span data-stu-id="41504-160">You can change the dimension display order configuration by selecting a new dimension to use.</span></span> 

<span data-ttu-id="41504-161">以下操作在矩阵视图单元中可用：</span><span class="sxs-lookup"><span data-stu-id="41504-161">The following actions are available in the matrix view cell:</span></span>

- <span data-ttu-id="41504-162">**立即销售** - 此操作将所选变型添加到购物车，并将用户重定向到交易屏幕。</span><span class="sxs-lookup"><span data-stu-id="41504-162">**Sell now** - This action adds the selected variant to the cart, and redirects the user to the transaction screen.</span></span>
- <span data-ttu-id="41504-163">**店内提货** - 此操作为将从所选商店提货的所选变型创建客户订单，然后将用户重定向到交易屏幕。</span><span class="sxs-lookup"><span data-stu-id="41504-163">**Pick up in store** - This action creates a customer order for the selected variant that will be picked up from the selected store, and redirects the user to the transaction screen.</span></span>
- <span data-ttu-id="41504-164">**装运产品** - 此操作为将从所选商店装运的所选变型创建客户订单，然后将用户重定向到交易屏幕。</span><span class="sxs-lookup"><span data-stu-id="41504-164">**Ship product** - This action creates a customer order for the selected variant that will be shipped from the selected store, and redirects the user to the transaction screen.</span></span>
- <span data-ttu-id="41504-165">**可用性** - 此操作将用户带到一个单独页面，其中显示所选商店中所选变型的 ATP 数量。</span><span class="sxs-lookup"><span data-stu-id="41504-165">**Availability** - This action takes the user to a separate page showing the ATP quantities for the selected variant in the selected store.</span></span>
- <span data-ttu-id="41504-166">**显示所有位置** - 此操作将切换到标准库存可用性列表视图，该视图显示所选变型的库存信息。</span><span class="sxs-lookup"><span data-stu-id="41504-166">**Show all locations** - This action switches to the standard inventory availability list view showing the inventory information for the selected variant.</span></span>
- <span data-ttu-id="41504-167">**查看产品详细信息** - 此操作将用户重定向到所选变型的产品详细信息页 (PDP)。</span><span class="sxs-lookup"><span data-stu-id="41504-167">**View product details** - This action redirects the user to the product details page (PDP) of the selected variant.</span></span>

## <a name="access-inventory-lookup-from-other-pages-in-pos"></a><span data-ttu-id="41504-168">从 POS 中的其他页面访问库存查找</span><span class="sxs-lookup"><span data-stu-id="41504-168">Access inventory lookup from other pages in POS</span></span>

<span data-ttu-id="41504-169">POS 用户可以从 POS 中的其他页面访问库存查找操作。</span><span class="sxs-lookup"><span data-stu-id="41504-169">POS users can access the inventory lookup operation from other pages in POS.</span></span>

<span data-ttu-id="41504-170">以下示例图像显示了来自 POS 中的 PDP 的库存查找结果。</span><span class="sxs-lookup"><span data-stu-id="41504-170">The following example image shows inventory lookup results from a PDP in POS.</span></span>

![产品详细信息页中的查找库存](media/inventory-lookup-from-product-details-page.png)

<span data-ttu-id="41504-172">在基础产品的 PDP 上，您可以使用应用栏上的 **查看所有变型** 操作启动库存查找矩阵视图，该视图显示当前商店中产品所有变型的库存可用性信息。</span><span class="sxs-lookup"><span data-stu-id="41504-172">On the PDP of a master product, you can use the **View all variants** action on the app bar to launch the inventory lookup matrix view that displays inventory availability information for the current store for all variants of a product.</span></span> <span data-ttu-id="41504-173">对于单个产品，PDP 显示当前商店中该产品的现有库存量（实际可用）值。</span><span class="sxs-lookup"><span data-stu-id="41504-173">For an individual product, the PDP displays the on-hand inventory (available physical) value of that product for the current store.</span></span> <span data-ttu-id="41504-174">此外，您还可以选择 **其他商店库存** 链接启动库存查找操作，来检查产品在其他商店或仓库中的库存可用性。</span><span class="sxs-lookup"><span data-stu-id="41504-174">Additionally, you can select the **Other stores inventory** link to launch the inventory lookup operation to check the inventory availability of a product across other stores or warehouses.</span></span>

> [!NOTE]
> <span data-ttu-id="41504-175">PDP 上的 **查看所有变型** 操作仅对具有变型的基础产品可用。</span><span class="sxs-lookup"><span data-stu-id="41504-175">The **View all variants** action on the PDP is available only for master products that have variants.</span></span> <span data-ttu-id="41504-176">对特定产品或套件不可用。</span><span class="sxs-lookup"><span data-stu-id="41504-176">It isn't available for specific products or kits.</span></span>

<span data-ttu-id="41504-177">您可以将库存查找操作配置为在 POS 交易屏幕上的按钮网格中显示为一个链接。</span><span class="sxs-lookup"><span data-stu-id="41504-177">You can configure the inventory lookup operation to appear as a link in the button grid on the POS transaction screen.</span></span> <span data-ttu-id="41504-178">配置后，当用户选择购物车行，然后选择 **库存查找** 按钮，将显示所选产品的库存查找列表视图。</span><span class="sxs-lookup"><span data-stu-id="41504-178">After configuration, when the user selects a cart line and then selects the **Inventory lookup** button, the inventory lookup list view for the selected product will be displayed.</span></span> <span data-ttu-id="41504-179">有关如何使用 POS 屏幕布局设计器工具配置按钮网格的详细信息，请参阅 [POS 用户界面视觉效果配置](pos-screen-layouts.md)。</span><span class="sxs-lookup"><span data-stu-id="41504-179">For more information about how to configure button grids using POS screen layout designer tool, see [POS user interface visual configurations](pos-screen-layouts.md).</span></span>

## <a name="inventory-lookup-with-channel-side-calculation"></a><span data-ttu-id="41504-180">使用渠道端计算的库存查找</span><span class="sxs-lookup"><span data-stu-id="41504-180">Inventory lookup with channel-side calculation</span></span>

<span data-ttu-id="41504-181">在 Commerce release 10.0.9 及更低版本中，库存查找操作中的 **实际可用** 值通过实时服务调用从 Commerce headquarters 检索。</span><span class="sxs-lookup"><span data-stu-id="41504-181">In Commerce release 10.0.9 and earlier, the **available physical** value in the inventory lookup operation is retrieved from Commerce headquarters via a real-time service call.</span></span> <span data-ttu-id="41504-182">在 Commerce 版本 10.0.10 及更高版本中，您可以配置 POS 库存查找操作，来在 Commerce 服务器上使用渠道端计算确定可用的实际值，这可以通过考虑尚未同步到总部的交易数据提供更可靠、更准确的现有库存量估计。</span><span class="sxs-lookup"><span data-stu-id="41504-182">In Commerce release 10.0.10 and later, you can configure the POS inventory lookup operation to use channel-side calculation on the Commerce server to determine the available physical value, which can provide a more reliable and more accurate estimate of the on-hand inventory by factoring in the transactional data that is not yet synchronized to headquarters.</span></span> <span data-ttu-id="41504-183">有关总部中的渠道端库存计算和相关 POS 配置的详细信息，请参阅[计算零售渠道的库存可用性](calculated-inventory-retail-channels.md)。</span><span class="sxs-lookup"><span data-stu-id="41504-183">For more information about channel-side inventory calculation and related POS configuration in headquarters, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="41504-184">其他资源</span><span class="sxs-lookup"><span data-stu-id="41504-184">Additional resources</span></span>

[<span data-ttu-id="41504-185">POS 用户界面视觉效果配置</span><span class="sxs-lookup"><span data-stu-id="41504-185">POS user interface visual configurations</span></span>](pos-screen-layouts.md)

[<span data-ttu-id="41504-186">计算零售渠道的库存现有量</span><span class="sxs-lookup"><span data-stu-id="41504-186">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

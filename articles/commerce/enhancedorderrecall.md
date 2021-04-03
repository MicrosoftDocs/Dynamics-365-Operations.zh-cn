---
title: POS 中的撤回订单操作
description: 本主题说明了可用于 POS 中改进的订单撤回页面的功能。
author: hhainesms
manager: annbe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 174821fce4baf81e4298da4b066f855bfec98ca5
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585122"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="90013-103">POS 中的撤回订单操作</span><span class="sxs-lookup"><span data-stu-id="90013-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="90013-104">Commerce 销售点 (POS) 中的 **撤回订单** 操作提供更新的订单搜索和筛选功能以及订单特定信息。</span><span class="sxs-lookup"><span data-stu-id="90013-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="90013-105">Commerce 版本 10.0.15 及更高版本中提供此功能。</span><span class="sxs-lookup"><span data-stu-id="90013-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="90013-106">若要启用此功能，请在 Commerce Headquarters 的 **功能管理** 工作区中打开 **改进的 POS 中的撤回订单操作** 功能。</span><span class="sxs-lookup"><span data-stu-id="90013-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="90013-107">启用该功能后，请考虑在 POS 中更新您的[屏幕布局](pos-screen-layouts.md)以利用某些已更改的功能。</span><span class="sxs-lookup"><span data-stu-id="90013-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="90013-108">**撤回订单** 操作按钮的配置使组织可以使用预定义的显示来部署操作。</span><span class="sxs-lookup"><span data-stu-id="90013-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![按钮网格配置](media/recallorderbuttongrid.png)

<span data-ttu-id="90013-110">显示选项如下。</span><span class="sxs-lookup"><span data-stu-id="90013-110">The display options are as follows.</span></span>
- <span data-ttu-id="90013-111">**无** – 此选项将部署操作，而不显示任何特定内容。</span><span class="sxs-lookup"><span data-stu-id="90013-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="90013-112">当用户使用此配置打开操作时，将提示他们搜索和查找订单，或从预定义的订单筛选器中进行选择。</span><span class="sxs-lookup"><span data-stu-id="90013-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="90013-113">**履行订单** – 当用户启动该操作时，将自动运行查询以搜索并显示用户当前商店要履行的订单列表。</span><span class="sxs-lookup"><span data-stu-id="90013-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the user's current store.</span></span> <span data-ttu-id="90013-114">这些订单配置为店内取货或商店发货，而这些订单行尚未领料或包装。</span><span class="sxs-lookup"><span data-stu-id="90013-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="90013-115">**提货订单** – 当用户启动该操作时，将自动运行查询以搜索并显示配置为在用户的当前商店店内取货的订单列表。</span><span class="sxs-lookup"><span data-stu-id="90013-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="90013-116">**装运订单** – 当用户启动该操作时，将自动运行查询以搜索并显示配置为从用户的当前商店装运的订单列表。</span><span class="sxs-lookup"><span data-stu-id="90013-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="90013-117">当从 POS 启动 **撤回订单** 操作时，如果显示配置为 **无**，用户将能够采用以下一种方法搜索和检索订单。</span><span class="sxs-lookup"><span data-stu-id="90013-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="90013-118">扫描订单条码。</span><span class="sxs-lookup"><span data-stu-id="90013-118">Scan order barcodes.</span></span> <span data-ttu-id="90013-119">这将搜索订单号、渠道引用和收据 ID 字段以查找匹配项。</span><span class="sxs-lookup"><span data-stu-id="90013-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="90013-120">在 AppBar 上选择 **搜索订单** 或 **搜索和筛选** 图标，以使用筛选机制来查找符合筛选条件的订单。</span><span class="sxs-lookup"><span data-stu-id="90013-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="90013-121">从 **显示订单** 下拉菜单的预定义筛选器中进行选择（履行订单、提货订单或转运订单）。</span><span class="sxs-lookup"><span data-stu-id="90013-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="90013-123">应用搜索条件后，应用程序将显示匹配的销售订单列表。</span><span class="sxs-lookup"><span data-stu-id="90013-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span> <span data-ttu-id="90013-124">重要的是要注意，使用搜索/筛选选项时，检索到的订单不必是链接到用户当前商店的订单。</span><span class="sxs-lookup"><span data-stu-id="90013-124">It's important to note that when using the search/filter options, the orders retrieved do not have to be orders linked to the user's current store.</span></span> <span data-ttu-id="90013-125">该搜索过程将检索并显示与搜索条件匹配的任何客户订单，即使该订单已创建或者设置为由另一个商店/渠道或仓库位置来完成。</span><span class="sxs-lookup"><span data-stu-id="90013-125">This search process will retrieve and display any customer order that matches the search criteria, even if the order was created or set to be fulfilled by another store/channel or warehouse location.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="90013-127">用户可以在列表上选择一个订单以查看其他详细信息。</span><span class="sxs-lookup"><span data-stu-id="90013-127">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="90013-128">屏幕右侧的信息面板显示所选订单的具体信息，包括订单行详细信息、交货详细信息和履行详细信息。</span><span class="sxs-lookup"><span data-stu-id="90013-128">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="90013-129">用户可以从 AppBar 中选择一个操作。</span><span class="sxs-lookup"><span data-stu-id="90013-129">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="90013-130">根据订单的状态，某些操作可能无法启用。</span><span class="sxs-lookup"><span data-stu-id="90013-130">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="90013-131">**退货** – 启动为选定客户订单上的任何已开票产品创建退货的过程。</span><span class="sxs-lookup"><span data-stu-id="90013-131">**Return** – Initiates the process of creating a return for any of the invoiced products on the selected customer order.</span></span>

- <span data-ttu-id="90013-132">**取消** – 对所选销售订单发起完全取消。</span><span class="sxs-lookup"><span data-stu-id="90013-132">**Cancel** – Issue a full cancellation of the selected sales order.</span></span> <span data-ttu-id="90013-133">此选项不适用于通过呼叫中心渠道发起的订单，也不能用于部分取消订单。</span><span class="sxs-lookup"><span data-stu-id="90013-133">This option will not be available for orders initiated through a call center channel and cannot be used to partially cancel an order.</span></span>

- <span data-ttu-id="90013-134">**履行** – 将用户转到订单履行页面，该页面将针对所选订单进行预筛选。</span><span class="sxs-lookup"><span data-stu-id="90013-134">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="90013-135">仅显示打开以供用户的商店履行所选订单的订单行。</span><span class="sxs-lookup"><span data-stu-id="90013-135">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="90013-136">**编辑** – 允许用户更改所选的客户订单。</span><span class="sxs-lookup"><span data-stu-id="90013-136">**Edit** – Allows users to make changes to the selected customer order.</span></span> <span data-ttu-id="90013-137">仅在[某些情况](customer-orders-overview.md#edit-an-existing-customer-order)可编辑订单。</span><span class="sxs-lookup"><span data-stu-id="90013-137">Orders are only editable in [certain scenarios](customer-orders-overview.md#edit-an-existing-customer-order).</span></span>

- <span data-ttu-id="90013-138">**提货** – 如果订单有一个或多个指定用于在用户当前商店提货的行，则此选项将可用。</span><span class="sxs-lookup"><span data-stu-id="90013-138">**Pick up** – This option will be available if the order has one or more lines designated for pickup at the user's current store.</span></span> <span data-ttu-id="90013-139">此操作将启动提货流程，使用户可以选择要提货的产品并创建提货销售交易。</span><span class="sxs-lookup"><span data-stu-id="90013-139">This operation launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>

## <a name="add-notifications-to-the-recall-order-operation"></a><span data-ttu-id="90013-140">向撤回订单操作添加通知</span><span class="sxs-lookup"><span data-stu-id="90013-140">Add notifications to the recall order operation</span></span>

<span data-ttu-id="90013-141">在 10.0.18 版本和更高版本中，如果需要，您可以为 **订单撤回** 操作配置 POS 通知和动态磁贴预警。</span><span class="sxs-lookup"><span data-stu-id="90013-141">In version 10.0.18 and later, you can configure POS notifications and live tile alerts for the **Order Recall** operation if desired.</span></span> <span data-ttu-id="90013-142">有关更多信息，请参见[在销售点 (POS) 显示订单通知](notifications-pos.md)。</span><span class="sxs-lookup"><span data-stu-id="90013-142">For more information, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>  

[!INCLUDE[footer-include](../includes/footer-banner.md)]

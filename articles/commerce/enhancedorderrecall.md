---
title: POS 中的撤回订单操作
description: 本主题说明了可用于 POS 中改进的订单撤回页面的功能。
author: hhainesms
manager: annbe
ms.date: 10/09/2020
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
ms.openlocfilehash: 21e8045d754006345f5ad68e1e67579386c6df4a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010066"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="67dc3-103">POS 中的撤回订单操作</span><span class="sxs-lookup"><span data-stu-id="67dc3-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="67dc3-104">Commerce 销售点 (POS) 中的 **撤回订单** 操作提供更新的订单搜索和筛选功能以及订单特定信息。</span><span class="sxs-lookup"><span data-stu-id="67dc3-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="67dc3-105">Commerce 版本 10.0.15 及更高版本中提供此功能。</span><span class="sxs-lookup"><span data-stu-id="67dc3-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="67dc3-106">若要启用此功能，请在 Commerce Headquarters 的 **功能管理** 工作区中打开 **改进的 POS 中的撤回订单操作** 功能。</span><span class="sxs-lookup"><span data-stu-id="67dc3-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="67dc3-107">启用该功能后，请考虑在 POS 中更新您的[屏幕布局](pos-screen-layouts.md)以利用某些已更改的功能。</span><span class="sxs-lookup"><span data-stu-id="67dc3-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="67dc3-108">**撤回订单** 操作按钮的配置使组织可以使用预定义的显示来部署操作。</span><span class="sxs-lookup"><span data-stu-id="67dc3-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![按钮网格配置](media/recallorderbuttongrid.png)

<span data-ttu-id="67dc3-110">显示选项如下。</span><span class="sxs-lookup"><span data-stu-id="67dc3-110">The display options are as follows.</span></span>
- <span data-ttu-id="67dc3-111">**无** – 此选项将部署操作，而不显示任何特定内容。</span><span class="sxs-lookup"><span data-stu-id="67dc3-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="67dc3-112">当用户使用此配置打开操作时，将提示他们搜索和查找订单，或从预定义的订单筛选器中进行选择。</span><span class="sxs-lookup"><span data-stu-id="67dc3-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="67dc3-113">**履行订单** – 当用户启动该操作时，将自动运行查询以搜索并显示商店要履行的订单列表。</span><span class="sxs-lookup"><span data-stu-id="67dc3-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the store.</span></span> <span data-ttu-id="67dc3-114">这些订单配置为店内取货或商店发货，而这些订单行尚未领料或包装。</span><span class="sxs-lookup"><span data-stu-id="67dc3-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="67dc3-115">**提货订单** – 当用户启动该操作时，将自动运行查询以搜索并显示配置为在用户的当前商店店内取货的订单列表。</span><span class="sxs-lookup"><span data-stu-id="67dc3-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="67dc3-116">**装运订单** – 当用户启动该操作时，将自动运行查询以搜索并显示配置为从用户的当前商店装运的订单列表。</span><span class="sxs-lookup"><span data-stu-id="67dc3-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="67dc3-117">当从 POS 启动 **撤回订单** 操作时，如果显示配置为 **无**，用户将能够采用以下一种方法搜索和检索订单。</span><span class="sxs-lookup"><span data-stu-id="67dc3-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="67dc3-118">扫描订单条码。</span><span class="sxs-lookup"><span data-stu-id="67dc3-118">Scan order barcodes.</span></span> <span data-ttu-id="67dc3-119">这将搜索订单号、渠道引用和收据 ID 字段以查找匹配项。</span><span class="sxs-lookup"><span data-stu-id="67dc3-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="67dc3-120">在 AppBar 上选择 **搜索订单** 或 **搜索和筛选** 图标，以使用筛选机制来查找符合筛选条件的订单。</span><span class="sxs-lookup"><span data-stu-id="67dc3-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="67dc3-121">从 **显示订单** 下拉菜单的预定义筛选器中进行选择（履行订单、提货订单或转运订单）。</span><span class="sxs-lookup"><span data-stu-id="67dc3-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="67dc3-123">应用搜索条件后，应用程序将显示匹配的销售订单列表。</span><span class="sxs-lookup"><span data-stu-id="67dc3-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="67dc3-125">用户可以在列表上选择一个订单以查看其他详细信息。</span><span class="sxs-lookup"><span data-stu-id="67dc3-125">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="67dc3-126">屏幕右侧的信息面板显示所选订单的具体信息，包括订单行详细信息、交货详细信息和履行详细信息。</span><span class="sxs-lookup"><span data-stu-id="67dc3-126">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="67dc3-127">用户可以从 AppBar 中选择一个操作。</span><span class="sxs-lookup"><span data-stu-id="67dc3-127">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="67dc3-128">根据订单的状态，某些操作可能无法启用。</span><span class="sxs-lookup"><span data-stu-id="67dc3-128">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="67dc3-129">**退货** – 对与所选客户订单相关的一张或多张发票执行退货。</span><span class="sxs-lookup"><span data-stu-id="67dc3-129">**Return** – Executes a return for one or more invoices related to the selected customer order.</span></span>

- <span data-ttu-id="67dc3-130">**取消** – 对所选销售订单发起完全取消。</span><span class="sxs-lookup"><span data-stu-id="67dc3-130">**Cancel** – Issue a full cancellation of the selected sales order.</span></span>

- <span data-ttu-id="67dc3-131">**履行** – 将用户转到订单履行页面，该页面将针对所选订单进行预筛选。</span><span class="sxs-lookup"><span data-stu-id="67dc3-131">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="67dc3-132">仅显示打开以供用户的商店履行所选订单的订单行。</span><span class="sxs-lookup"><span data-stu-id="67dc3-132">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="67dc3-133">**编辑** – 允许用户更改所选的客户订单。</span><span class="sxs-lookup"><span data-stu-id="67dc3-133">**Edit** – Allows users to make changes to the selected customer order.</span></span>

- <span data-ttu-id="67dc3-134">**提货** – 启动提货流程，使用户可以选择要提货的产品并创建提货销售交易。</span><span class="sxs-lookup"><span data-stu-id="67dc3-134">**Pick up** – Launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>

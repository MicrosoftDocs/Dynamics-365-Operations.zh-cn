---
title: 在 POS 中处理客户订单提货
description: 本主题说明销售点 (POS) 应用程序中用于处理客户订单提货的功能。
author: Hhainesms
manager: annbe
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 2156542ed0932fab6fb4fa4035e009ad89eeb18f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003745"
---
# <a name="process-customer-order-pickups-in-pos"></a><span data-ttu-id="aa5ef-103">在 POS 中处理客户订单提货</span><span class="sxs-lookup"><span data-stu-id="aa5ef-103">Process customer order pickups in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aa5ef-104">当创建要在商店提货的[客户订单](customer-orders-overview.md)时，商店用户可以使用销售点 (POS) 应用程序开始库存提货。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-104">When a [customer order](customer-orders-overview.md) is created for store pickup, a store user can use the point of sale (POS) application to start the pickup of inventory.</span></span> <span data-ttu-id="aa5ef-105">POS 将根据需要运行最终付款捕获。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-105">POS will run the final payment capture as required.</span></span> <span data-ttu-id="aa5ef-106">另外还将完成提货数量的库存和财务过帐。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-106">It will also complete the inventory and financial posting for the quantities that are picked up.</span></span>

<span data-ttu-id="aa5ef-107">如果您是商店用户，可以使用 POS 中的 **撤回订单** 操作或 **订单履行** 操作来执行提货。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-107">If you're a store user, you can perform the pickup by using either the **Recall order** operation or the **Order fulfillment** operation in POS.</span></span> <span data-ttu-id="aa5ef-108">要让 **提货** 操作可用，您必须首先执行以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="aa5ef-108">To make the **Pick up** operation available, you must first follow one of these steps:</span></span>

- <span data-ttu-id="aa5ef-109">要使用 **撤回订单** 操作，搜索并选择将要提货的订单。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-109">To use the **Recall order** operation, search for and select the order that will be picked up.</span></span>
- <span data-ttu-id="aa5ef-110">要使用 **订单履行** 操作，搜索并选择一个或多个订单行。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-110">To use the **Order fulfillment** operation, search for and select one or more order lines.</span></span>

<span data-ttu-id="aa5ef-111">如果未将所选订单或订单行配置为在该特定商店提货，或者订单已完全提货，**提货** 操作将不可用。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-111">If the selected order or order lines aren't configured for pickup at that specific store, or if the order has already been fully picked up, the **Pick up** operation will be unavailable.</span></span>

![提货操作](media/pickupoperation.png)

<span data-ttu-id="aa5ef-113">在 Microsoft Dynamics 365 Commerce 版本 10.0.17 及更高版本中，可以通过 Commerce headquarters 中的“功能管理”打开 **销售点中改进的提货订单处理用户体验** 功能。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-113">In Microsoft Dynamics 365 Commerce version 10.0.17 and later, the **Improved user experience for pick up order processing in Point of Sale** feature can be turned on through Feature management in Commerce headquarters.</span></span> <span data-ttu-id="aa5ef-114">如果此功能关闭，用户则无法选择提货数量。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-114">If this feature is turned off, users can't select pickup quantities.</span></span> <span data-ttu-id="aa5ef-115">默认情况下，为行订购的全部数量是要提货的数量。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-115">By default, the full quantity that was ordered for the line is the quantity that will be picked up.</span></span> <span data-ttu-id="aa5ef-116">此体验可能会存在问题，因为用户在通过订单履行执行提货时可能会忘记选择其中一些要提货的产品。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-116">This experience can be problematic, because users might forget to select some items for pickup when they perform the pickup through order fulfillment.</span></span>

<span data-ttu-id="aa5ef-117">**销售点中改进的提货订单处理用户体验** 功能让用户可以更进一步地控制对要提货的产品的选择以及要提货的产品的数量。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-117">The **Improved user experience for pick up order processing in Point of Sale** feature gives users more control over the selection of products that will be picked up and the quantity of those products that will be picked up.</span></span> <span data-ttu-id="aa5ef-118">在选择 **提货** 之前，用户无需先在订单履行页面上选择销售订单的每一行。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-118">Users don't have to select every line of the sales order on the order fulfillment page before they select **Pick up**.</span></span> <span data-ttu-id="aa5ef-119">可以提货的所有产品都会显示。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-119">All the items that can be picked up will be shown.</span></span> <span data-ttu-id="aa5ef-120">用户可以为提货指定多个行，即使只选择了一个产品行。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-120">Users can specify multiple lines for pickup even if only one product line is selected.</span></span>

<span data-ttu-id="aa5ef-121">当 **销售点中改进的提货订单处理用户体验** 功能打开时，选择 **提货** 操作，**提货** 对话框将出现。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-121">When the **Improve user experience for pick up order processing in Point of Sale** feature is turned on, and you select the **Pick up** operation, the **Pick up** dialog box appears.</span></span> <span data-ttu-id="aa5ef-122">在那里，您可以选择要提货的产品和数量。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-122">There, you can select the items and quantities that will be picked up.</span></span> <span data-ttu-id="aa5ef-123">默认情况下，任何具有处于已提货或已包装状态的库存的订购数量都会被视为符合提货条件。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-123">By default, any ordered quantity that has inventory in a picked or packed state is considered eligible for pickup.</span></span> <span data-ttu-id="aa5ef-124">默认情况下，该数量设置为提货数量。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-124">By default, that quantity is set as the pickup quantity.</span></span> <span data-ttu-id="aa5ef-125">您可以更改输入的数量，前提是该数量不是 0（零）且不超过所选行的未结总数量（即未开票）。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-125">You can change the quantity that was entered, provided that the quantity isn't 0 (zero) and doesn't exceed the total open (that is, non-invoiced) quantity for the selected line.</span></span>

![提货对话框](media/pickupselect.png)

<span data-ttu-id="aa5ef-127">选择要提货的数量后，选择 **提货**，将出现交易页面。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-127">After you select the quantities that will be picked up and then select **Pick up**, the transaction page appears.</span></span> <span data-ttu-id="aa5ef-128">如果[全渠道付款](omni-channel-payments.md)功能已打开，并且有预授权的信用卡付款记录在案，您必须进行付款。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-128">If the [omni-channel payments](omni-channel-payments.md) feature is turned on, and there are pre-authorized credit card payments on file, you must apply the payment.</span></span>

<span data-ttu-id="aa5ef-129">在交易页面上，系统通过计算所选提货产品的应付总额，然后减去任何先前应用的存款或授权的信用卡付款来计算应付金额。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-129">On the transaction page, the system calculates the amounts that are due by calculating the total that is due for the selected pickup items and then subtracting any previously applied deposits or authorized credit card payments.</span></span> <span data-ttu-id="aa5ef-130">您必须处理付款才能完成提货交易。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-130">You must process payment to complete the pickup transaction.</span></span> <span data-ttu-id="aa5ef-131">如果交易页面的 [屏幕布局](pos-screen-layouts.md)配置被配置为包括 **完成交易** 操作，并且没有应付金额，您无需选择付款方式即可完成交易。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-131">If the [screen layout](pos-screen-layouts.md) of the transaction page is configured so that it includes the **Conclude transaction** operation, and no amount is due, you can complete the transaction without selecting a payment method.</span></span> <span data-ttu-id="aa5ef-132">如果 **完成交易** 操作不可用，您可以选择 **总计** 窗格中的 **$0.00 应付金额** 链接来完成交易，而无需选择付款方式。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-132">If the **Conclude transaction** operation isn't available, you can select the **$0.00 amount due** link in the **Totals** pane to conclude the transaction without having to select a payment method.</span></span>

![客户订单提货交易的交易页面](media/pickupcart.png)

## <a name="changing-pickup-lines-or-quantities"></a><span data-ttu-id="aa5ef-134">更改提货行或数量</span><span class="sxs-lookup"><span data-stu-id="aa5ef-134">Changing pickup lines or quantities</span></span>

<span data-ttu-id="aa5ef-135">如果在选择了要提货的产品后必须更改提货数量，可以选择 **设置数量**。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-135">If you must change the pickup quantity after you've selected the items that will be picked up, you can select **Set quantity**.</span></span> <span data-ttu-id="aa5ef-136">您不能将提货数量设置为 **0**（零）或将其增加到超过订购行剩余的未开票数量的值。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-136">You can't set the pickup quantity to **0** (zero) or increase it to a value that exceeds the non-invoiced quantity that remains for the ordered line.</span></span> <span data-ttu-id="aa5ef-137">要从交易购物车中删除提货行，请选择 **取消交易**。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-137">To remove a pickup line from the transaction cart, select **Void transaction**.</span></span> <span data-ttu-id="aa5ef-138">当前交易将停止，**提货** 操作的流将重新启动。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-138">The current transaction will be stopped, and the flow for the **Pick up** operation will be restarted.</span></span>

<span data-ttu-id="aa5ef-139">如果 **销售点中改进的提货订单处理用户体验** 功能打开，组织可以在交易页面的屏幕布局中为 **更改提货行** 操作添加按钮。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-139">If the **Improve user experience for pick up order processing in Point of Sale** feature is turned on, organizations can add a button for the **Change pickup lines** operation to the screen layout of the transaction page.</span></span> <span data-ttu-id="aa5ef-140">在 POS 中创建提货交易购物车并选择产品后，如果您必须更改提货产品但又不想要取消整个交易，您可以选择 **更改提货行**。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-140">After you create the pickup transaction cart in POS and select items, you can select **Change pickup lines** if you must change the pickup items but don't want to void the whole transaction.</span></span> <span data-ttu-id="aa5ef-141">在出现的 **更改提货行** 对话框中，您可以更改提货产品和数量。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-141">In the **Change pickup lines** dialog box that appears, you can change the pickup items and quantities.</span></span> <span data-ttu-id="aa5ef-142">交易购物车然后会更新以反映您的更改。</span><span class="sxs-lookup"><span data-stu-id="aa5ef-142">The transaction cart is then updated to reflect your changes.</span></span>

![更改提货产品对话框](media/pickupchange.png)

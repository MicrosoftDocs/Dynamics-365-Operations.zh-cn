---
title: 为客户订单启用多种提货交货方式
description: 本主题介绍 Microsoft Dynamics 365 Commerce 中的功能，可让您创建要在商店提货的客户订单。
author: hhainesms
manager: annbe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 38413f96eec97e93beb6998871a40c7ef755073c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251275"
---
# <a name="enable-multiple-pickup-delivery-modes-for-customer-orders"></a><span data-ttu-id="fbff0-103">为客户订单启用多种提货交货方式</span><span class="sxs-lookup"><span data-stu-id="fbff0-103">Enable multiple pickup delivery modes for customer orders</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="fbff0-104">在 Microsoft Dynamics 365 Commerce 版本 10.0.16 及更高版本中，组织可以定义多种交货方式，以供购物者或销售助理创建将在商店提货的订单时进行选择。</span><span class="sxs-lookup"><span data-stu-id="fbff0-104">In Microsoft Dynamics 365 Commerce version 10.0.16 and later, organizations can define multiple modes of delivery that shoppers or sales associates can choose among when they create an order that will be picked up at a store.</span></span> <span data-ttu-id="fbff0-105">这样，组织可以向购物者提供多种提货选项。</span><span class="sxs-lookup"><span data-stu-id="fbff0-105">In this way, organizations can provide multiple pickup options to their shoppers.</span></span> <span data-ttu-id="fbff0-106">例如，许多零售商现在针对其订单向购物者提供店内提货或懒人提货的选项。</span><span class="sxs-lookup"><span data-stu-id="fbff0-106">For example, many retailers now offer shoppers the choice of in-store pickup or curbside pickup for their orders.</span></span> <span data-ttu-id="fbff0-107">Commerce 支持配置这些不同的提货交货方式。</span><span class="sxs-lookup"><span data-stu-id="fbff0-107">Commerce supports the configuration of these different pickup delivery modes.</span></span> <span data-ttu-id="fbff0-108">然后，用户可以在任何受支持的 Commerce 渠道（电子商务、呼叫中心或商店）中创建客户订单时利用它们。</span><span class="sxs-lookup"><span data-stu-id="fbff0-108">Users can then take advantage of them when they create customer orders in any supported Commerce channel (e-commerce, call center, or store).</span></span>

## <a name="enable-and-configure-pickup-delivery-modes"></a><span data-ttu-id="fbff0-109">启用和配置多种提货交货方式</span><span class="sxs-lookup"><span data-stu-id="fbff0-109">Enable and configure pickup delivery modes</span></span>

<span data-ttu-id="fbff0-110">若要使用此功能，请在 Commerce 总部中在 **功能管理** 工作区中打开 **支持多种提货交货方式** 功能。</span><span class="sxs-lookup"><span data-stu-id="fbff0-110">To use this functionality, turn on the **Support for multiple pickup delivery modes** feature in the **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="fbff0-111">打开该功能后，需要其他配置。</span><span class="sxs-lookup"><span data-stu-id="fbff0-111">After you turn on the feature, additional configuration is required.</span></span>

<span data-ttu-id="fbff0-112">在 Commerce 版本 10.0.15 及更早版本中，组织只能定义一种交货方式作为指定的提货交货方式。</span><span class="sxs-lookup"><span data-stu-id="fbff0-112">In Commerce version 10.0.15 and earlier, organizations can define only one mode of delivery as the designated pickup delivery mode.</span></span> <span data-ttu-id="fbff0-113">此定义在 **Commerce 参数** 页面上完成。</span><span class="sxs-lookup"><span data-stu-id="fbff0-113">This definition is done on the **Commerce parameters** page.</span></span> <span data-ttu-id="fbff0-114">在版本 10.0.16 及更高版本中，当您打开 **支持多种提货交货方式** 功能时，之前在 **Commerce 参数** 页面上定义为提货交货方式的交货方式将自动复制到提货交货方式的新配置中。</span><span class="sxs-lookup"><span data-stu-id="fbff0-114">In version 10.0.16 and later, when you turn on the **Support for multiple pickup delivery modes** feature, the mode of delivery that was previously defined as the pickup delivery mode on the **Commerce parameters** page is automatically copied into the new configuration for pickup delivery modes.</span></span>

![Commerce 参数页面上的提货交货方式](media/multiplepickupparameter.png)

<span data-ttu-id="fbff0-116">打开 **支持多种提货交货方式** 功能后，您可以在 **Commerce 参数** 页面的 **客户订单** 选项卡上，在 **交货方式** 快速选项卡的 **提货交货方式** 网格中，定义多种提货交货方式。</span><span class="sxs-lookup"><span data-stu-id="fbff0-116">After you turn on the **Support for multiple pickup delivery modes** feature, you can define multiple pickup delivery modes in the **Pickup mode of delivery** grid on the **Modes of delivery** FastTab on the **Customer orders** tab of the **Commerce parameters** page.</span></span>

<span data-ttu-id="fbff0-117">**自提交货方式** 和 **电子交货方式** 字段以及 **仅显示装运订单的承运人模式选项** 选项已重新位于此快速选项卡上。</span><span class="sxs-lookup"><span data-stu-id="fbff0-117">The **Carry Out mode of delivery** and **Electronic mode of delivery** fields, and the **Show only carrier mode options for ship orders** option, have been relocated to this FastTab.</span></span>

<span data-ttu-id="fbff0-118">在配置其他提货交货方式之前，必须先定义交货方式。</span><span class="sxs-lookup"><span data-stu-id="fbff0-118">Before you configure additional pickup delivery modes, you must define the modes of delivery.</span></span> <span data-ttu-id="fbff0-119">在 Commerce 总部的 **交货方式** 页面中，添加应视为提货交货方式的交货方式。</span><span class="sxs-lookup"><span data-stu-id="fbff0-119">On the **Modes of delivery** page in Commerce headquarters, add the modes of delivery that should be considered pickup delivery modes.</span></span> <span data-ttu-id="fbff0-120">确保所有配置均已完成。</span><span class="sxs-lookup"><span data-stu-id="fbff0-120">Make sure that all configuration is completed.</span></span> <span data-ttu-id="fbff0-121">例如，确保交货方式链接到适当的渠道和物料。</span><span class="sxs-lookup"><span data-stu-id="fbff0-121">For example, make sure that the mode of delivery is linked to appropriate channels and items.</span></span> <span data-ttu-id="fbff0-122">完成后，运行 **处理交货方式** 作业以在交货方式、渠道和物料之间创建关系。</span><span class="sxs-lookup"><span data-stu-id="fbff0-122">When you've finished, run the **Process delivery modes** job to create the relationships among the mode of delivery, channels, and items.</span></span> <span data-ttu-id="fbff0-123">在作业完成运行后，在 Commerce 总部中打开 **配送计划** 页面，然后运行 **1120** 配送作业，以确保使用新的交货方式配置更新相关的 Commerce 渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="fbff0-123">When the job has finished running, open the **Distribution schedule** page in Commerce headquarters, and run the **1120** distribution job to ensure that the relevant Commerce channel databases are updated with your new delivery mode configuration.</span></span>

![懒人提货的交货方式的示例](media/pickupmodes.png)

<span data-ttu-id="fbff0-125">定义其他提货交货方式后，在 **Commerce 参数** 页面上将它们添加到 **提货交货方式** 网格。</span><span class="sxs-lookup"><span data-stu-id="fbff0-125">After you define the additional pickup delivery modes, add them to the **Pickup mode of delivery** grid on the **Commerce parameters** page.</span></span> <span data-ttu-id="fbff0-126">然后，运行适当的配送作业，以使用配置更改更新相关的 Commerce 渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="fbff0-126">Then run the appropriate distribution jobs to update the relevant Commerce channel databases with the configuration change.</span></span>

> [!NOTE]
> <span data-ttu-id="fbff0-127">除了在打开 **支持多种提货交货方式** 功能时复制到 **提货交货方式** 网格的现有提货交货方式外，对于您创建的每个其他提货交货方式配置，您应该配置新的交货方式。</span><span class="sxs-lookup"><span data-stu-id="fbff0-127">Apart from the existing pickup delivery mode that is copied to the **Pickup mode of delivery** grid when you turn on the **Support for multiple pickup delivery modes** feature, for every additional pickup delivery mode configuration that you create, you should configure new modes of delivery.</span></span> <span data-ttu-id="fbff0-128">当您将交货方式添加到 **提货交货方式** 网格时，Commerce 会验证是否有任何活动的未结销售行已使用它们。</span><span class="sxs-lookup"><span data-stu-id="fbff0-128">When you add modes of delivery to the **Pickup mode of delivery** grid, Commerce validates whether any active open sales lines already use them.</span></span> <span data-ttu-id="fbff0-129">如果找到任何未结销售行，您将收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="fbff0-129">If any open sales lines are found, you receive an error message.</span></span> <span data-ttu-id="fbff0-130">直到使用交货方式的所有未结销售行已结算（已开票或已取消），才将其视为提货交货方式。</span><span class="sxs-lookup"><span data-stu-id="fbff0-130">Modes of delivery aren't considered pickup delivery modes until all open sales lines that use them have been closed (either invoiced or canceled).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fbff0-131">在 **Commerce 参数** 页面上定义多种提货交货方式后，**支持多种提货交货方式** 功能将成为强制性功能，无法再关闭。</span><span class="sxs-lookup"><span data-stu-id="fbff0-131">After you define more than one pickup delivery mode on the **Commerce parameters** page, the **Support for multiple pickup delivery modes** feature becomes mandatory and can no longer be turned off.</span></span> <span data-ttu-id="fbff0-132">如果必须关闭此功能，请从 **提货交货方式** 窗格中删除除一个之外的所有提货交货方式。</span><span class="sxs-lookup"><span data-stu-id="fbff0-132">If you must turn off the feature, remove all but one pickup delivery mode from the **Pickup mode of delivery** grid.</span></span> <span data-ttu-id="fbff0-133">如果仅定义了一种提货交货方式，该功能将不再视为强制性功能，并且可以关闭。</span><span class="sxs-lookup"><span data-stu-id="fbff0-133">When only one pickup delivery mode is defined, the feature is longer considered mandatory and can be turned off.</span></span>

### <a name="e-commerce-site-configurations"></a><span data-ttu-id="fbff0-134">电子商务站点配置</span><span class="sxs-lookup"><span data-stu-id="fbff0-134">E-commerce site configurations</span></span>

<span data-ttu-id="fbff0-135">当打开 **支持多种提货交货方式** 功能时，电子商务页面上的以下模块将显示新的提货交货方式，配置如下：</span><span class="sxs-lookup"><span data-stu-id="fbff0-135">When the **Support for multiple pickup delivery modes** feature is turned on, the following modules on e-commerce pages show the new pickup delivery modes as configured:</span></span>

- <span data-ttu-id="fbff0-136">购买框</span><span class="sxs-lookup"><span data-stu-id="fbff0-136">Buy box</span></span>
- <span data-ttu-id="fbff0-137">商店选择器</span><span class="sxs-lookup"><span data-stu-id="fbff0-137">Store selector</span></span>
- <span data-ttu-id="fbff0-138">购物车</span><span class="sxs-lookup"><span data-stu-id="fbff0-138">Cart</span></span>
- <span data-ttu-id="fbff0-139">选择信息</span><span class="sxs-lookup"><span data-stu-id="fbff0-139">Pickup information</span></span>
- <span data-ttu-id="fbff0-140">订单确认</span><span class="sxs-lookup"><span data-stu-id="fbff0-140">Order confirmation</span></span>
- <span data-ttu-id="fbff0-141">订单明细</span><span class="sxs-lookup"><span data-stu-id="fbff0-141">Order details</span></span>

<span data-ttu-id="fbff0-142">若要使提货交货方式可用，无需在电子商务页面上执行其他步骤。</span><span class="sxs-lookup"><span data-stu-id="fbff0-142">No additional steps are required on e-commerce pages to make the pickup delivery modes available.</span></span>

## <a name="work-with-multiple-pickup-delivery-modes"></a><span data-ttu-id="fbff0-143">使用多种提货交货方式</span><span class="sxs-lookup"><span data-stu-id="fbff0-143">Work with multiple pickup delivery modes</span></span>

<span data-ttu-id="fbff0-144">如果多种提货交货方式可用于渠道，当客户购买将要提货的产品时，将为他们提供增强的体验。</span><span class="sxs-lookup"><span data-stu-id="fbff0-144">When multiple pickup delivery modes are available for a channel, an enhanced experience is provided to customers when they shop for products that will be picked up.</span></span> 

- <span data-ttu-id="fbff0-145">在电子商务渠道中，购物者可以选择任何可用的有效提货交货方式。</span><span class="sxs-lookup"><span data-stu-id="fbff0-145">In e-commerce channels, shoppers can select any valid pickup delivery mode that is available.</span></span> <span data-ttu-id="fbff0-146">例如，零售商定义两种提货交货方式（店内提货和懒人提货），二者均在 **提货交货方式** 网格中配置，并且对订单履行渠道和购物者当前购买的产品均有效。</span><span class="sxs-lookup"><span data-stu-id="fbff0-146">For example, a retailer defines two pickup delivery modes (in-store pickup and curbside pickup), both are configured in the **Pickup mode of delivery** grid, and both are valid for the order fulfillment channel and the product that a shopper is currently purchasing.</span></span> <span data-ttu-id="fbff0-147">在这种情况下，购物者可以选择他们喜欢的提货交货方式。</span><span class="sxs-lookup"><span data-stu-id="fbff0-147">In this case, the shopper can select their preferred pickup delivery mode.</span></span> <span data-ttu-id="fbff0-148">然后，当在 Commerce 总部中创建订单时，所选的提货交货方式将成为链接到销售订单行的交货方式。</span><span class="sxs-lookup"><span data-stu-id="fbff0-148">The selected pickup delivery mode then becomes the mode of delivery that is linked to the sales order line when the order is created in Commerce headquarters.</span></span>

    ![在电子商务中选择提货选项](media/pickupecommerce.png)

- <span data-ttu-id="fbff0-150">在商店渠道中，如果通过销售点 (POS) 应用程序创建提货的客户订单，将提示销售助理在可用的提货交货方式（如果已配置方式）中进行选择。</span><span class="sxs-lookup"><span data-stu-id="fbff0-150">In store channels, if a customer order for pickup is created through the point of sale (POS) application, the sales associate is prompted to choose among the available pickup delivery modes, if any have been configured.</span></span> <span data-ttu-id="fbff0-151">如果只有一种有效的提货交货方式可用于渠道和物料，则不会提示销售助理选择它。</span><span class="sxs-lookup"><span data-stu-id="fbff0-151">If only one valid pickup delivery mode is available for the channel and item, the sales associate isn't prompted to select it.</span></span> <span data-ttu-id="fbff0-152">相反，可用提货交货方式将自动应用到订单行。</span><span class="sxs-lookup"><span data-stu-id="fbff0-152">Instead, the available pickup delivery mode is automatically applied to the order lines.</span></span>

    ![在 POS 应用程序中选择提货选项](media/pickuppos.png)

- <span data-ttu-id="fbff0-154">在呼叫中心渠道中，当用户创建提货订单时，他们可以手动选择链接到呼叫中心渠道的任何定义的提货交货方式。</span><span class="sxs-lookup"><span data-stu-id="fbff0-154">In call center channels, when users create pickup orders, they can manually select any defined pickup delivery mode that is linked to the call center channel.</span></span> <span data-ttu-id="fbff0-155">然后，系统验证是否可以在订购要链接到它的物料时使用所选的提货交货方式。</span><span class="sxs-lookup"><span data-stu-id="fbff0-155">The system then validates that the selected pickup delivery mode can be used when the item that is being linked to it is ordered.</span></span> <span data-ttu-id="fbff0-156">当在呼叫中心渠道中选择提货交货方式时，必须将销售订单行链接到有效的商店仓库。</span><span class="sxs-lookup"><span data-stu-id="fbff0-156">When a pickup delivery mode is selected in call center channels, the sales order lines must be linked to a valid store warehouse.</span></span> <span data-ttu-id="fbff0-157">如果在呼叫中心销售行上定义了非商店仓库，无法在该销售行上设置提货交货方式。</span><span class="sxs-lookup"><span data-stu-id="fbff0-157">If a non-store warehouse is defined on a call center sales line, a pickup delivery mode can't be set on that sales line.</span></span>
- <span data-ttu-id="fbff0-158">销售助理可以在 POS 应用程序中使用 **订单撤回** 或 **订单履行** 操作，以检索提货的订单或订单行的列表。</span><span class="sxs-lookup"><span data-stu-id="fbff0-158">Sales associates can use the **Order recall** or **Order fulfillment** operation in the POS application to retrieve a list of orders or order lines for pickup.</span></span> <span data-ttu-id="fbff0-159">如果销售助理使用预定义的搜索筛选器显示将在当前商店中提货的所有订单，将修改查询以确保搜索结果包括使用任何提货交货方式的所有符合资格的订单。</span><span class="sxs-lookup"><span data-stu-id="fbff0-159">If a sales associate uses a predefined search filter to show all orders that will be picked up at the current store, the queries are modified to ensure that the search results include all eligible orders that use any pickup delivery mode.</span></span> <span data-ttu-id="fbff0-160">POS 用户还可以使用现有筛选器将订单列表缩小到特定的提货交货方式。</span><span class="sxs-lookup"><span data-stu-id="fbff0-160">POS users can also use existing filters to narrow down the list of orders to a specific pickup delivery mode.</span></span> <span data-ttu-id="fbff0-161">例如，他们只能显示懒人提货的订单。</span><span class="sxs-lookup"><span data-stu-id="fbff0-161">For example, they can show only orders for curbside pickup.</span></span>

    ![适用于撤回订单列表的提货交货方式的筛选器](media/pickuprecallorder.png)

## <a name="considerations-for-distributed-order-management"></a><span data-ttu-id="fbff0-163">分配的订单管理 (DOM) 的注意事项</span><span class="sxs-lookup"><span data-stu-id="fbff0-163">Considerations for distributed order management</span></span>

<span data-ttu-id="fbff0-164">Commerce 中的[分配的订单管理 (DOM)](https://docs.microsoft.com/dynamics365/commerce/dom) 功能会忽略标记为商店提货的所有销售行。</span><span class="sxs-lookup"><span data-stu-id="fbff0-164">The [distributed order management (DOM)](https://docs.microsoft.com/dynamics365/commerce/dom) features in Commerce ignore any sales lines that are marked for store pickup.</span></span> <span data-ttu-id="fbff0-165">这些功能已更新，以确保链接到已配置的提货交货方式的销售行会绕过 DOM 逻辑，并且不会重新分配到新的履行仓库。</span><span class="sxs-lookup"><span data-stu-id="fbff0-165">These features have been updated to ensure that sales lines that are linked to configured pickup delivery modes bypass the DOM logic and won't be reallocated to a new fulfillment warehouse.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
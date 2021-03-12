---
title: 设置在线渠道
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新的在线渠道。
author: samjarawan
manager: annbe
ms.date: 07/02/2020
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
ms.openlocfilehash: 89a28d6d4f435b9cf0c39afc64c3caaf0b24ba19
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993620"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="5f52d-103">设置在线渠道</span><span class="sxs-lookup"><span data-stu-id="5f52d-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5f52d-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新的在线渠道。</span><span class="sxs-lookup"><span data-stu-id="5f52d-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5f52d-105">概览</span><span class="sxs-lookup"><span data-stu-id="5f52d-105">Overview</span></span>

<span data-ttu-id="5f52d-106">Dynamics 365 Commerce 支持多种零售渠道。</span><span class="sxs-lookup"><span data-stu-id="5f52d-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="5f52d-107">这些零售渠道包括在线商店、呼叫中心和零售商店（亦称实体商店）。</span><span class="sxs-lookup"><span data-stu-id="5f52d-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="5f52d-108">除了在其零售商店中购买外，在线商店还使客户可以选择从零售商的在线商店中购买产品。</span><span class="sxs-lookup"><span data-stu-id="5f52d-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="5f52d-109">要在 Commerce 中创建在线商店，必须首先创建在线渠道。</span><span class="sxs-lookup"><span data-stu-id="5f52d-109">To create an online store in Commerce, you must first create an online channel.</span></span> <span data-ttu-id="5f52d-110">在创建新在线渠道之前，请确保已完成[渠道设置先决条件](channels-prerequisites.md)。</span><span class="sxs-lookup"><span data-stu-id="5f52d-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

<span data-ttu-id="5f52d-111">必须至少在 Commerce 中创建一个在线商店，才能创建新站点。</span><span class="sxs-lookup"><span data-stu-id="5f52d-111">Before you can create a new site, at least one online store must be created in Commerce.</span></span> <span data-ttu-id="5f52d-112">有关详细信息，请参阅[创建电子商务站点](create-ecommerce-site.md)。</span><span class="sxs-lookup"><span data-stu-id="5f52d-112">For more information, see [Create an e-Commerce site](create-ecommerce-site.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="5f52d-113">创建和配置新在线渠道</span><span class="sxs-lookup"><span data-stu-id="5f52d-113">Create and configure a new online channel</span></span>

<span data-ttu-id="5f52d-114">要创建和配置新在线渠道，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="5f52d-114">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="5f52d-115">在导航窗格中，转到 **模块 \> 渠道 \> 在线商店**。</span><span class="sxs-lookup"><span data-stu-id="5f52d-115">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="5f52d-116">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="5f52d-116">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5f52d-117">在 **名称** 字段中，为新渠道提供名称。</span><span class="sxs-lookup"><span data-stu-id="5f52d-117">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="5f52d-118">在 **法人** 下拉列表中，输入适当的法人。</span><span class="sxs-lookup"><span data-stu-id="5f52d-118">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="5f52d-119">在 **仓库** 下拉列表中，输入适当的仓库。</span><span class="sxs-lookup"><span data-stu-id="5f52d-119">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="5f52d-120">在 **商店时区** 字段中，选择适当的时区。</span><span class="sxs-lookup"><span data-stu-id="5f52d-120">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="5f52d-121">在 **货币** 字段中，选择适当的货币。</span><span class="sxs-lookup"><span data-stu-id="5f52d-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="5f52d-122">在 **默认客户** 字段中，请提供有效的默认客户。</span><span class="sxs-lookup"><span data-stu-id="5f52d-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="5f52d-123">在 **客户通讯簿** 字段中，提供有效的通讯簿。</span><span class="sxs-lookup"><span data-stu-id="5f52d-123">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="5f52d-124">在 **功能配置文件** 字段中，选择功能配置文件（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="5f52d-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="5f52d-125">在 **电子邮件通知配置文件** 字段中，请提供有效的电子邮件通知配置文件。</span><span class="sxs-lookup"><span data-stu-id="5f52d-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="5f52d-126">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="5f52d-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5f52d-127">下图显示了新在线渠道的创建过程。</span><span class="sxs-lookup"><span data-stu-id="5f52d-127">The following image shows the creation of a new online channel.</span></span>

![新在线渠道](media/channel-setup-online-1.png)

<span data-ttu-id="5f52d-129">下图显示了一个在线渠道示例。</span><span class="sxs-lookup"><span data-stu-id="5f52d-129">The following image shows an example online channel.</span></span>

![在线渠道示例](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="5f52d-131">设置语言</span><span class="sxs-lookup"><span data-stu-id="5f52d-131">Set up languages</span></span>

<span data-ttu-id="5f52d-132">如果您的电子商务站点将支持多种语言，请展开 **语言** 部分，并根据需要添加其他语言。</span><span class="sxs-lookup"><span data-stu-id="5f52d-132">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="5f52d-133">设置付款帐户</span><span class="sxs-lookup"><span data-stu-id="5f52d-133">Set up payment account</span></span>

<span data-ttu-id="5f52d-134">从 **付款帐户** 部分中，您可以添加第三方付款提供商。</span><span class="sxs-lookup"><span data-stu-id="5f52d-134">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="5f52d-135">有关设置 Adyen Payment Connector 的信息，请参阅[适用于 Adyen 的 Dynamics 365 Payment Connector](../retail/dev-itpro/adyen-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="5f52d-135">For information on setting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-setup"></a><span data-ttu-id="5f52d-136">其他渠道设置</span><span class="sxs-lookup"><span data-stu-id="5f52d-136">Additional channel setup</span></span>

<span data-ttu-id="5f52d-137">在线渠道设置所需的其他任务包括设置付款方式、交货方式和履行组分配。</span><span class="sxs-lookup"><span data-stu-id="5f52d-137">Additional tasks that are required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="5f52d-138">下图显示了 **设置** 选项卡上的 **交货方式**、**付款方式** 和 **履行组分配** 设置选项。</span><span class="sxs-lookup"><span data-stu-id="5f52d-138">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![其他在线渠道设置操作](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="5f52d-140">设置付款方式</span><span class="sxs-lookup"><span data-stu-id="5f52d-140">Set up payment methods</span></span>

<span data-ttu-id="5f52d-141">要设置付款方式，请针对此渠道支持的每种付款类型执行这些步骤。</span><span class="sxs-lookup"><span data-stu-id="5f52d-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="5f52d-142">在操作窗格上，选择 **设置** 选项卡，然后选择 **付款方式**。</span><span class="sxs-lookup"><span data-stu-id="5f52d-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="5f52d-143">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="5f52d-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5f52d-144">在导航窗格中，选择所需的付款方式。</span><span class="sxs-lookup"><span data-stu-id="5f52d-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="5f52d-145">在 **常规** 部分，提供 **操作名称** 并配置任何其他所需的设置。</span><span class="sxs-lookup"><span data-stu-id="5f52d-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="5f52d-146">根据付款类型的要求配置任何其他设置。</span><span class="sxs-lookup"><span data-stu-id="5f52d-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="5f52d-147">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="5f52d-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5f52d-148">下图显示了现金支付方式的示例。</span><span class="sxs-lookup"><span data-stu-id="5f52d-148">The following image shows an example of a cash payment method.</span></span>

![付款方法示例](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="5f52d-150">设置交货方式</span><span class="sxs-lookup"><span data-stu-id="5f52d-150">Set up modes of delivery</span></span>

<span data-ttu-id="5f52d-151">您可以从 **操作窗格** 上的 **设置** 选项卡中选择 **交货方式** 来查看已配置的交货方式。</span><span class="sxs-lookup"><span data-stu-id="5f52d-151">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="5f52d-152">要更改或添加交货方式，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="5f52d-152">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="5f52d-153">在导航窗格中，转到 **模块 \> 库存管理 \> 交货方式**。</span><span class="sxs-lookup"><span data-stu-id="5f52d-153">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="5f52d-154">在操作窗格上，选择 **新增** 以创建新的交货方式，或选择现有方式。</span><span class="sxs-lookup"><span data-stu-id="5f52d-154">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="5f52d-155">在 **零售渠道** 部分，选择 **添加行** 以添加渠道。</span><span class="sxs-lookup"><span data-stu-id="5f52d-155">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="5f52d-156">使用组织节点添加渠道而不是单独添加每个渠道可以简化渠道添加操作。</span><span class="sxs-lookup"><span data-stu-id="5f52d-156">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="5f52d-157">下图显示了交货方式的示例。</span><span class="sxs-lookup"><span data-stu-id="5f52d-157">The following image shows an example of a mode of delivery.</span></span>

![设置交货方式](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="5f52d-159">设置履行组分配</span><span class="sxs-lookup"><span data-stu-id="5f52d-159">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="5f52d-160">若要设置履行组分配，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="5f52d-160">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="5f52d-161">在操作窗格上，选择 **设置** 选项卡，然后选择 **履行组分配**。</span><span class="sxs-lookup"><span data-stu-id="5f52d-161">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="5f52d-162">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="5f52d-162">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5f52d-163">在 **履行组** 下拉列表中，选择一个履行组。</span><span class="sxs-lookup"><span data-stu-id="5f52d-163">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="5f52d-164">在 **描述** 下拉列表中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="5f52d-164">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="5f52d-165">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="5f52d-165">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5f52d-166">下图显示了履行组分配设置的示例。</span><span class="sxs-lookup"><span data-stu-id="5f52d-166">The following image shows an example of a fulfillment group assignment setup.</span></span>

![设置履行组分配](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="5f52d-168">其他资源</span><span class="sxs-lookup"><span data-stu-id="5f52d-168">Additional resources</span></span>

[<span data-ttu-id="5f52d-169">渠道概览</span><span class="sxs-lookup"><span data-stu-id="5f52d-169">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="5f52d-170">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="5f52d-170">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="5f52d-171">设置零售渠道</span><span class="sxs-lookup"><span data-stu-id="5f52d-171">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="5f52d-172">设置呼叫中心渠道</span><span class="sxs-lookup"><span data-stu-id="5f52d-172">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="5f52d-173">适用于 Adyen 的 Dynamics 365 付款连接器</span><span class="sxs-lookup"><span data-stu-id="5f52d-173">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)

---
title: 设置呼叫中心渠道
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新的呼叫中心渠道。
author: samjarawan
manager: annbe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: bdaabad39484cb12537bc5f94c34dcb2575a5b2f
ms.sourcegitcommit: ef27189efc15ce79c3c31ce2e41ef8a606fc5429
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410405"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="4b161-103">设置呼叫中心渠道</span><span class="sxs-lookup"><span data-stu-id="4b161-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4b161-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新的呼叫中心渠道。</span><span class="sxs-lookup"><span data-stu-id="4b161-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4b161-105">概览</span><span class="sxs-lookup"><span data-stu-id="4b161-105">Overview</span></span>


<span data-ttu-id="4b161-106">在 Dynamics 365 Commerce 中，呼叫中心是一种可在应用程序中定义的 Commerce 渠道。</span><span class="sxs-lookup"><span data-stu-id="4b161-106">In Dynamics 365 Commerce, a call center is a type of Commerce channel that can be defined in the application.</span></span> <span data-ttu-id="4b161-107">为呼叫中心实体定义渠道使系统能够将特定数据和订单处理默认值绑定到销售订单。</span><span class="sxs-lookup"><span data-stu-id="4b161-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="4b161-108">虽然一家公司可以在 Commerce 中定义多个呼叫中心渠道，还是请务必注意，只能将一位用户链接到一个呼叫中心渠道。</span><span class="sxs-lookup"><span data-stu-id="4b161-108">While a company can define multiple call center channels in Commerce, it is important to note that an individual user may only be linked to one call center channel.</span></span> 

<span data-ttu-id="4b161-109">在创建新呼叫中心渠道之前，请确保已完成[渠道设置先决条件](channels-prerequisites.md)。</span><span class="sxs-lookup"><span data-stu-id="4b161-109">Before you create a new call center channel, ensure that you have completed the [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="4b161-110">创建和配置新呼叫中心渠道</span><span class="sxs-lookup"><span data-stu-id="4b161-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="4b161-111">要创建和配置新呼叫中心渠道，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="4b161-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="4b161-112">在导航窗格中，转到 **Retail 和 Commerce \> 渠道 \> 呼叫中心 \> 所有呼叫中心**。</span><span class="sxs-lookup"><span data-stu-id="4b161-112">In the navigation pane, go to **Retail and Commerce \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="4b161-113">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="4b161-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4b161-114">在**名称**字段中，为新渠道提供名称。</span><span class="sxs-lookup"><span data-stu-id="4b161-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="4b161-115">从下拉列表中选择适当的**法人**。</span><span class="sxs-lookup"><span data-stu-id="4b161-115">Select the appropriate **Legal entity** from the drop-down.</span></span>
1. <span data-ttu-id="4b161-116">从下拉列表中选择适当的**仓库**位置。</span><span class="sxs-lookup"><span data-stu-id="4b161-116">Select the appropriate **Warehouse** location from the drop-down.</span></span> <span data-ttu-id="4b161-117">除非在客户或物料级别定义了其他默认位置，否则将把此位置用作为此呼叫中心渠道创建的销售订单中的默认位置。</span><span class="sxs-lookup"><span data-stu-id="4b161-117">This location will be used as the default on sales orders created for this call center channel, unless other defaults have been defined at the customer or item level.</span></span>
1. <span data-ttu-id="4b161-118">在**默认客户**字段中，请提供有效的默认客户。</span><span class="sxs-lookup"><span data-stu-id="4b161-118">In the **Default customer** field, provide a valid default customer.</span></span> <span data-ttu-id="4b161-119">在创建新的客户记录时，此数据用于帮助自动填充默认值。</span><span class="sxs-lookup"><span data-stu-id="4b161-119">This data is used to assist in auto-populating defaults when new customer records are created.</span></span> <span data-ttu-id="4b161-120">创建呼叫中心订单时，建议不要为默认客户创建订单。</span><span class="sxs-lookup"><span data-stu-id="4b161-120">When creating call center orders, it is not advisable to create orders for the default customer.</span></span>
1. <span data-ttu-id="4b161-121">在**电子邮件通知配置文件**字段中，请提供有效的电子邮件通知配置文件。</span><span class="sxs-lookup"><span data-stu-id="4b161-121">In the **Email notification profile** field, provide a valid email notification profile.</span></span> <span data-ttu-id="4b161-122">如果创建并处理呼叫中心订单，将使用电子邮件通知配置文件和有关客户的订单状态的信息对客户触发自动化电子邮件预警。</span><span class="sxs-lookup"><span data-stu-id="4b161-122">As call center orders are created and processed, the email notification profile is used to trigger automated email alerts to customers with information about their order status.</span></span>
1. <span data-ttu-id="4b161-123">提供**价格覆盖**信息代码。</span><span class="sxs-lookup"><span data-stu-id="4b161-123">Provide a **Price override** info code.</span></span> <span data-ttu-id="4b161-124">您可能首先需要为此创建一个信息代码。</span><span class="sxs-lookup"><span data-stu-id="4b161-124">You may need to create an info code for this first.</span></span> <span data-ttu-id="4b161-125">此信息代码提供一组原因代码，在呼叫中心订单中使用价格覆盖功能时，将提示用户在这些原因代码中进行选择。</span><span class="sxs-lookup"><span data-stu-id="4b161-125">This info code provides the set of reason codes that the user will be prompted to choose from when using the price override functionality on a call center order.</span></span>
1. <span data-ttu-id="4b161-126">提供一个**保留代码**信息代码。</span><span class="sxs-lookup"><span data-stu-id="4b161-126">Provide a **Hold code** info code.</span></span> <span data-ttu-id="4b161-127">您可能首先需要为此创建一个信息代码。</span><span class="sxs-lookup"><span data-stu-id="4b161-127">You may need to create an info code for this first.</span></span> <span data-ttu-id="4b161-128">此信息代码提供一组可选原因代码，在暂停订单时，将提示用户在这些原因代码中进行选择。</span><span class="sxs-lookup"><span data-stu-id="4b161-128">This info code provides the set of optional reason codes that the user will be prompted to choose from when placing an order on hold.</span></span>
1. <span data-ttu-id="4b161-129">提供一个**贷记**信息代码。</span><span class="sxs-lookup"><span data-stu-id="4b161-129">Provide a **Credit** info code.</span></span> <span data-ttu-id="4b161-130">您可能首先需要为此创建一个信息代码。</span><span class="sxs-lookup"><span data-stu-id="4b161-130">You may need to create an info code for this first.</span></span> <span data-ttu-id="4b161-131">此信息代码提供一组原因代码，供用户在因为客户服务原因使用呼叫中心的订单贷记功能向客户提供杂项退款时选择。</span><span class="sxs-lookup"><span data-stu-id="4b161-131">This info code provides the set of reason codes that the user can choose from when using the order credit functionality of call center to give misc refunds to the customer for customer service reasons.</span></span>
1. <span data-ttu-id="4b161-132">可选：在**财务维度**快速选项卡上设置财务维度。</span><span class="sxs-lookup"><span data-stu-id="4b161-132">Optional: set up financial dimensions on the **Financial dimensions** FastTab.</span></span> <span data-ttu-id="4b161-133">此处输入的维度将充当此呼叫中心渠道中创建的任何销售订单中的默认维度。</span><span class="sxs-lookup"><span data-stu-id="4b161-133">The dimensions entered here will default on any sales order created in this call center channel.</span></span>
1. <span data-ttu-id="4b161-134">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="4b161-134">Click **Save**.</span></span>

<span data-ttu-id="4b161-135">下图显示了新呼叫中心渠道的创建过程。</span><span class="sxs-lookup"><span data-stu-id="4b161-135">The following image shows the creation of a new call center channel.</span></span>

![新呼叫中心渠道](media/channel-setup-callcenter-1.png)

<span data-ttu-id="4b161-137">下图显示了一个呼叫中心渠道示例。</span><span class="sxs-lookup"><span data-stu-id="4b161-137">The following image shows an example call center channel.</span></span>

![呼叫中心渠道示例](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="4b161-139">其他渠道设置</span><span class="sxs-lookup"><span data-stu-id="4b161-139">Additional channel setup</span></span>

<span data-ttu-id="4b161-140">呼叫中心渠道设置所需的其他任务包括设置付款方式和交货方式。</span><span class="sxs-lookup"><span data-stu-id="4b161-140">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="4b161-141">下图显示了**设置**选项卡上的**交货方式**和**付款方式**设置选项。</span><span class="sxs-lookup"><span data-stu-id="4b161-141">The following image shows **Modes of delivery** and **Payment methods** setup options on the **Set up** tab.</span></span>

![其他呼叫中心渠道设置操作](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="4b161-143">设置付款方式</span><span class="sxs-lookup"><span data-stu-id="4b161-143">Set up payment methods</span></span>

<span data-ttu-id="4b161-144">要设置付款方式，请针对此渠道支持的每种付款类型执行这些步骤。</span><span class="sxs-lookup"><span data-stu-id="4b161-144">To set up payment methods, follow these steps for each payment type supported on this channel.</span></span> <span data-ttu-id="4b161-145">用户需要在预定义的付款方式中进行选择以将其链接到呼叫中心渠道。</span><span class="sxs-lookup"><span data-stu-id="4b161-145">Users will be required to select from pre-defined payment methods to link them to the call center channel.</span></span> <span data-ttu-id="4b161-146">设置呼叫中心付款方式之前，请首先在 **Retail 和 Commerce \> 渠道设置 \> 付款方式 \> 付款方式**中设置主付款方式。</span><span class="sxs-lookup"><span data-stu-id="4b161-146">Before setting up your call center payment methods, first set up your master methods of payment in **Retail and Commerce \> Channel setup \> Payment methods \> Payment methods**.</span></span>

1. <span data-ttu-id="4b161-147">在操作窗格上，选择**设置**选项卡，然后选择**付款方式**。</span><span class="sxs-lookup"><span data-stu-id="4b161-147">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="4b161-148">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="4b161-148">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4b161-149">在导航窗格中，从预定义的可用付款中选择付款方式。</span><span class="sxs-lookup"><span data-stu-id="4b161-149">In the navigation pane, select a payment method from the pre-defined payments available.</span></span>
1. <span data-ttu-id="4b161-150">根据付款类型的要求配置任何其他设置。</span><span class="sxs-lookup"><span data-stu-id="4b161-150">Configure any additional settings as required for the payment type.</span></span> <span data-ttu-id="4b161-151">对于信用卡、礼品卡或会员卡，需要通过选择**卡设置**功能进行额外设置。</span><span class="sxs-lookup"><span data-stu-id="4b161-151">For credit cards, gift cards, or loyalty cards, additional setup is required by selecting the **Card setup** function.</span></span> 
1. <span data-ttu-id="4b161-152">在**过帐**部分中为付款类型设置正确的过帐科目。</span><span class="sxs-lookup"><span data-stu-id="4b161-152">Configure proper posting accounts for the payment type in the **Posting** section.</span></span>
1. <span data-ttu-id="4b161-153">在操作窗格上，单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="4b161-153">On the action pane, click **Save**.</span></span>

<span data-ttu-id="4b161-154">下图显示了现金支付方式的示例。</span><span class="sxs-lookup"><span data-stu-id="4b161-154">The following image shows an example of a cash payment method.</span></span>

![付款方法示例](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="4b161-156">设置交货方式</span><span class="sxs-lookup"><span data-stu-id="4b161-156">Set up modes of delivery</span></span>

<span data-ttu-id="4b161-157">您可以从**操作窗格**上的**设置**选项卡中选择**交货方式**来查看已配置的交货方式。</span><span class="sxs-lookup"><span data-stu-id="4b161-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="4b161-158">若要更改或添加要与呼叫中心渠道关联的交货方式，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="4b161-158">To change or add a mode of delivery to be associated to the call center channel, follow these steps.</span></span>

1. <span data-ttu-id="4b161-159">在呼叫中心的交货方式窗体中，选择**更改交货方式**</span><span class="sxs-lookup"><span data-stu-id="4b161-159">From the Call center modes of delivery form, select **Manage modes of delivery**</span></span>
1. <span data-ttu-id="4b161-160">在操作窗格上，选择**新增**以创建新的交货方式，或选择现有方式。</span><span class="sxs-lookup"><span data-stu-id="4b161-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="4b161-161">在**零售渠道**部分，单击**添加行**以添加呼叫中心渠道。</span><span class="sxs-lookup"><span data-stu-id="4b161-161">In the **Retail channels** section, click **Add line** to add the call center channel.</span></span> <span data-ttu-id="4b161-162">使用组织节点添加渠道而不是单独添加每个渠道可以简化渠道添加操作。</span><span class="sxs-lookup"><span data-stu-id="4b161-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>
1. <span data-ttu-id="4b161-163">确保已经在**产品**快速选项卡和**地址**快速选项卡上为交货方式配置了数据。</span><span class="sxs-lookup"><span data-stu-id="4b161-163">Ensure the mode of delivery has been configured with data on the **Products** FastTab and the **Addresses** FastTab.</span></span> <span data-ttu-id="4b161-164">如果交货方式无有效产品或交货地址，在录入订单期间选择产品或交货地址将出错。</span><span class="sxs-lookup"><span data-stu-id="4b161-164">If no products or delivery addresses are valid for the mode of delivery, choosing it during order entry will result in errors.</span></span>
1. <span data-ttu-id="4b161-165">对呼叫中心交货方式配置进行了任何更改之后，必须运行**流程交货方式**作业以分解更改矩阵。</span><span class="sxs-lookup"><span data-stu-id="4b161-165">After any changes have been made to the call center mode of delivery configurations, the **Process delivery modes** job must be run to explode the change matrix.</span></span> <span data-ttu-id="4b161-166">可以通过导航到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 流程交货方式**找到该作业。</span><span class="sxs-lookup"><span data-stu-id="4b161-166">This job can be found by navigating to **Retail and Commerce \> Retail and Commerce IT \> Process delivery modes**.</span></span>

<span data-ttu-id="4b161-167">下图显示了交货方式的示例。</span><span class="sxs-lookup"><span data-stu-id="4b161-167">The following image shows an example of a mode of delivery.</span></span>

![设置交货方式](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a><span data-ttu-id="4b161-169">设置渠道用户</span><span class="sxs-lookup"><span data-stu-id="4b161-169">Set up channel users</span></span>

<span data-ttu-id="4b161-170">若要从 Commerce Headquarters 创建链接到呼叫中心渠道的销售订单，必须将创建该销售订单的用户链接到呼叫中心渠道。</span><span class="sxs-lookup"><span data-stu-id="4b161-170">To create a sales order that is linked to the call center channel from Commerce Headquarters, the user creating the sales order must be linked to the call center channel.</span></span> <span data-ttu-id="4b161-171">用户不能将 Commerce Headquarters 中创建的销售订单手动链接到呼叫中心渠道。</span><span class="sxs-lookup"><span data-stu-id="4b161-171">The user can not manually link a sales order created in Commerce Headquarters to the call center channel.</span></span> <span data-ttu-id="4b161-172">此链接是系统的，并且基于用户和用户与呼叫中心渠道之间的关系。</span><span class="sxs-lookup"><span data-stu-id="4b161-172">The link is systematic, and is based on the user and the user's relationship to the call center channel.</span></span> <span data-ttu-id="4b161-173">一个用户只能链接到一个呼叫中心频道。</span><span class="sxs-lookup"><span data-stu-id="4b161-173">A user may only be linked to one call center channel.</span></span>

1. <span data-ttu-id="4b161-174">在操作窗格上，选择**渠道**选项卡，然后选择**渠道用户**。</span><span class="sxs-lookup"><span data-stu-id="4b161-174">On the action pane, select the **Channel** tab, and then select **Channel users**.</span></span>
1. <span data-ttu-id="4b161-175">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="4b161-175">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4b161-176">从下拉选择列表中选择一个现有**用户 ID**，以便将此用户链接到呼叫中心渠道</span><span class="sxs-lookup"><span data-stu-id="4b161-176">Choose an existing **User ID** from the dropdown selection list to link this user to the call center channel</span></span>

<span data-ttu-id="4b161-177">完成渠道用户设置并且用户在 Commerce Headquarters 中创建新的销售订单之后，将把该销售订单链接到该用户关联的呼叫中心渠道。</span><span class="sxs-lookup"><span data-stu-id="4b161-177">After the channel user setup is done and the user creates a new sales order in Commerce Headquarters, the sales order will be linked to their associated call center channel.</span></span> <span data-ttu-id="4b161-178">将对销售订单系统地应用此渠道的所有配置。</span><span class="sxs-lookup"><span data-stu-id="4b161-178">Any configurations for this channel will be applied systematically to the sales order.</span></span> <span data-ttu-id="4b161-179">用户可以通过查看销售订单标题中的渠道名称应用来确定销售订单链接到了哪个呼叫中心渠道。</span><span class="sxs-lookup"><span data-stu-id="4b161-179">A user can confirm which call center channel the sales order is linked to by viewing the channel name reference on the sales order header.</span></span>


### <a name="set-up-price-groups"></a><span data-ttu-id="4b161-180">设置价格组</span><span class="sxs-lookup"><span data-stu-id="4b161-180">Set up price groups</span></span>

<span data-ttu-id="4b161-181">价格组是可选的，但如果使用价格组，则可以控制向在呼叫中心渠道中下订单的客户提供哪些销售价。</span><span class="sxs-lookup"><span data-stu-id="4b161-181">Price groups are optional, but if used, can control which sales prices will be offered to customers placing orders in the call center channel.</span></span> <span data-ttu-id="4b161-182">如果尚未为客户配置价格组，或者如果不向销售订单应用目录价格组（通过使用呼叫中心订单标题中的**源代码 ID** 字段），则使用渠道价格组查找物料价格。</span><span class="sxs-lookup"><span data-stu-id="4b161-182">If a price group has not been configured for the customer, or if catalog price groups are not being applied to the sales order (using the **Source code ID** field on the call center order header), then the channel price group is used to locate item prices.</span></span> <span data-ttu-id="4b161-183">如果在呼叫中心渠道中找不到价格组，则使用默认物料主价格。</span><span class="sxs-lookup"><span data-stu-id="4b161-183">If a price group is not found on the call center channel, the default item master prices are used.</span></span> 

<span data-ttu-id="4b161-184">若要设置价格组，请执行以下操作。</span><span class="sxs-lookup"><span data-stu-id="4b161-184">To set up a price group, do the following.</span></span>

1. <span data-ttu-id="4b161-185">在操作窗格上，单击**渠道**选项卡，然后选择**价格组**。</span><span class="sxs-lookup"><span data-stu-id="4b161-185">On the action pane, click the **Channel** tab, and then select **Price groups**.</span></span>
1. <span data-ttu-id="4b161-186">在操作窗格中，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="4b161-186">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="4b161-187">从下拉选择列表中选择一个**零售价格组**。</span><span class="sxs-lookup"><span data-stu-id="4b161-187">Select a **Retail price group** from the dropdown selection list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4b161-188">其他资源</span><span class="sxs-lookup"><span data-stu-id="4b161-188">Additional resources</span></span>

[<span data-ttu-id="4b161-189">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="4b161-189">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="4b161-190">呼叫中心销售功能</span><span class="sxs-lookup"><span data-stu-id="4b161-190">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="4b161-191">设置呼叫中心订单处理选项</span><span class="sxs-lookup"><span data-stu-id="4b161-191">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="4b161-192">呼叫中心目录</span><span class="sxs-lookup"><span data-stu-id="4b161-192">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="4b161-193">设置和使用欺诈预警</span><span class="sxs-lookup"><span data-stu-id="4b161-193">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="4b161-194">设置呼叫中心的连续性计划</span><span class="sxs-lookup"><span data-stu-id="4b161-194">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)

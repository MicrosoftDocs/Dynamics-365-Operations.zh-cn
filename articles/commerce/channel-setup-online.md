---
title: 设置在线渠道
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新的在线渠道。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.openlocfilehash: 9b7a2b8fd157df8b39e9e227d188a3802cacb4e3
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002419"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="15741-103">设置在线渠道</span><span class="sxs-lookup"><span data-stu-id="15741-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="15741-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新的在线渠道。</span><span class="sxs-lookup"><span data-stu-id="15741-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="15741-105">概览</span><span class="sxs-lookup"><span data-stu-id="15741-105">Overview</span></span>

<span data-ttu-id="15741-106">Dynamics 365 Commerce 支持多种零售渠道。</span><span class="sxs-lookup"><span data-stu-id="15741-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="15741-107">这些零售渠道包括在线商店、呼叫中心和零售商店（亦称实体商店）。</span><span class="sxs-lookup"><span data-stu-id="15741-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="15741-108">除了在其零售商店中购买外，在线商店还使客户可以选择从零售商的在线商店中购买产品。</span><span class="sxs-lookup"><span data-stu-id="15741-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="15741-109">要在 Commerce 中创建在线商店，必须首先创建在线渠道。</span><span class="sxs-lookup"><span data-stu-id="15741-109">To create an online store in Commerce, you must first create an online channel.</span></span> 

<span data-ttu-id="15741-110">在创建新在线渠道之前，请确保已完成[渠道设置先决条件](channels-prerequisites.md)。</span><span class="sxs-lookup"><span data-stu-id="15741-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="15741-111">创建和配置新在线渠道</span><span class="sxs-lookup"><span data-stu-id="15741-111">Create and configure a new online channel</span></span>

<span data-ttu-id="15741-112">要创建和配置新在线渠道，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="15741-112">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="15741-113">在导航窗格中，转到**模块 \> 渠道 \> 在线商店**。</span><span class="sxs-lookup"><span data-stu-id="15741-113">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="15741-114">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="15741-114">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="15741-115">在**名称**字段中，为新渠道提供名称。</span><span class="sxs-lookup"><span data-stu-id="15741-115">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="15741-116">在**法人**下拉列表中，输入适当的法人。</span><span class="sxs-lookup"><span data-stu-id="15741-116">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="15741-117">在**仓库**下拉列表中，输入适当的仓库。</span><span class="sxs-lookup"><span data-stu-id="15741-117">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="15741-118">在**商店时区**字段中，选择适当的时区。</span><span class="sxs-lookup"><span data-stu-id="15741-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="15741-119">在**货币**字段中，选择适当的货币。</span><span class="sxs-lookup"><span data-stu-id="15741-119">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="15741-120">在**默认客户**字段中，请提供有效的默认客户。</span><span class="sxs-lookup"><span data-stu-id="15741-120">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="15741-121">在**客户通讯簿**字段中，提供有效的通讯簿。</span><span class="sxs-lookup"><span data-stu-id="15741-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="15741-122">在**功能配置文件**字段中，选择功能配置文件（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="15741-122">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="15741-123">在**电子邮件通知配置文件**字段中，请提供有效的电子邮件通知配置文件。</span><span class="sxs-lookup"><span data-stu-id="15741-123">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="15741-124">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="15741-124">On the action pane, select **Save**.</span></span>

<span data-ttu-id="15741-125">下图显示了新在线渠道的创建过程。</span><span class="sxs-lookup"><span data-stu-id="15741-125">The following image shows the creation of a new online channel.</span></span>

![新在线渠道](media/channel-setup-online-1.png)

<span data-ttu-id="15741-127">下图显示了一个在线渠道示例。</span><span class="sxs-lookup"><span data-stu-id="15741-127">The following image shows an example online channel.</span></span>

![在线渠道示例](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="15741-129">设置语言</span><span class="sxs-lookup"><span data-stu-id="15741-129">Set up languages</span></span>

<span data-ttu-id="15741-130">如果您的电子商务站点将支持多种语言，请展开**语言**部分，并根据需要添加其他语言。</span><span class="sxs-lookup"><span data-stu-id="15741-130">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="15741-131">设置付款帐户</span><span class="sxs-lookup"><span data-stu-id="15741-131">Set up payment account</span></span>

<span data-ttu-id="15741-132">从**付款帐户**部分中，您可以添加第三方付款提供商。</span><span class="sxs-lookup"><span data-stu-id="15741-132">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="15741-133">有关设置 Adyen 付款连接器的信息，请参阅[适用于 Adyen 的 Dynamics 365 付款连接器](../retail/dev-itpro/adyen-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="15741-133">For information on settting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-set-up"></a><span data-ttu-id="15741-134">其他渠道设置</span><span class="sxs-lookup"><span data-stu-id="15741-134">Additional channel set up</span></span>

<span data-ttu-id="15741-135">在线渠道设置所需的其他任务包括设置付款方式、交货方式和履行组分配。</span><span class="sxs-lookup"><span data-stu-id="15741-135">Additional tasks required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="15741-136">下图显示了**设置**选项卡上的**交货方式**、**付款方式**和**履行组分配**设置选项。</span><span class="sxs-lookup"><span data-stu-id="15741-136">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![其他在线渠道设置操作](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="15741-138">设置付款方式</span><span class="sxs-lookup"><span data-stu-id="15741-138">Set up payment methods</span></span>

<span data-ttu-id="15741-139">要设置付款方式，请针对此渠道支持的每种付款类型执行这些步骤。</span><span class="sxs-lookup"><span data-stu-id="15741-139">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="15741-140">在操作窗格上，选择**设置**选项卡，然后选择**付款方式**。</span><span class="sxs-lookup"><span data-stu-id="15741-140">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="15741-141">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="15741-141">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="15741-142">在导航窗格中，选择所需的付款方式。</span><span class="sxs-lookup"><span data-stu-id="15741-142">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="15741-143">在**常规**部分，提供**操作名称**并配置任何其他所需的设置。</span><span class="sxs-lookup"><span data-stu-id="15741-143">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="15741-144">根据付款类型的要求配置任何其他设置。</span><span class="sxs-lookup"><span data-stu-id="15741-144">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="15741-145">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="15741-145">On the action pane, select **Save**.</span></span>

<span data-ttu-id="15741-146">下图显示了现金支付方式的示例。</span><span class="sxs-lookup"><span data-stu-id="15741-146">The following image shows an example of a cash payment method.</span></span>

![付款方法示例](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="15741-148">设置交货方式</span><span class="sxs-lookup"><span data-stu-id="15741-148">Set up modes of delivery</span></span>

<span data-ttu-id="15741-149">您可以从**操作窗格**上的**设置**选项卡中选择**交货方式**来查看已配置的交货方式。</span><span class="sxs-lookup"><span data-stu-id="15741-149">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="15741-150">要更改或添加交货方式，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="15741-150">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="15741-151">在导航窗格中，转到**模块 \> 库存管理 \> 交货方式**。</span><span class="sxs-lookup"><span data-stu-id="15741-151">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="15741-152">在操作窗格上，选择**新增**以创建新的交货方式，或选择现有方式。</span><span class="sxs-lookup"><span data-stu-id="15741-152">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="15741-153">在**零售渠道**部分，选择**添加行**以添加渠道。</span><span class="sxs-lookup"><span data-stu-id="15741-153">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="15741-154">使用组织节点添加渠道而不是单独添加每个渠道可以简化渠道添加操作。</span><span class="sxs-lookup"><span data-stu-id="15741-154">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="15741-155">下图显示了交货方式的示例。</span><span class="sxs-lookup"><span data-stu-id="15741-155">The following image shows an example of a mode of delivery.</span></span>

![设置交货方式](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="15741-157">设置履行组分配</span><span class="sxs-lookup"><span data-stu-id="15741-157">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="15741-158">若要设置履行组分配，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="15741-158">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="15741-159">在操作窗格上，选择**设置**选项卡，然后选择**履行组分配**。</span><span class="sxs-lookup"><span data-stu-id="15741-159">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="15741-160">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="15741-160">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="15741-161">在**履行组**下拉列表中，选择一个履行组。</span><span class="sxs-lookup"><span data-stu-id="15741-161">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="15741-162">在**描述**下拉列表中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="15741-162">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="15741-163">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="15741-163">On the action pane, select **Save**.</span></span>

<span data-ttu-id="15741-164">下图显示了履行组分配设置的示例。</span><span class="sxs-lookup"><span data-stu-id="15741-164">The following image shows an example of a fulfillment group assignment setup.</span></span>

![设置履行组分配](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="15741-166">其他资源</span><span class="sxs-lookup"><span data-stu-id="15741-166">Additional resources</span></span>

[<span data-ttu-id="15741-167">渠道概览</span><span class="sxs-lookup"><span data-stu-id="15741-167">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="15741-168">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="15741-168">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="15741-169">设置零售渠道</span><span class="sxs-lookup"><span data-stu-id="15741-169">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="15741-170">设置呼叫中心渠道</span><span class="sxs-lookup"><span data-stu-id="15741-170">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="15741-171">适用于 Adyen 的 Dynamics 365 付款连接器</span><span class="sxs-lookup"><span data-stu-id="15741-171">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)

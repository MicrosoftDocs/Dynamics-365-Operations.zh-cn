---
title: 设置呼叫中心渠道
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新的呼叫中心渠道。
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
ms.openlocfilehash: 42448bd54c00b8642b158f422e17d2b46ee25579
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057871"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="6b39e-103">设置呼叫中心渠道</span><span class="sxs-lookup"><span data-stu-id="6b39e-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6b39e-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新的呼叫中心渠道。</span><span class="sxs-lookup"><span data-stu-id="6b39e-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6b39e-105">概览</span><span class="sxs-lookup"><span data-stu-id="6b39e-105">Overview</span></span>

<span data-ttu-id="6b39e-106">在 Dynamics 365 Commerce 中，呼叫中心是一种可在应用程序中定义的渠道。</span><span class="sxs-lookup"><span data-stu-id="6b39e-106">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="6b39e-107">为呼叫中心实体定义渠道使系统能够将特定数据和订单处理默认值绑定到销售订单。</span><span class="sxs-lookup"><span data-stu-id="6b39e-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="6b39e-108">一家公司可在 Commerce 中定义多个呼叫中心渠道。</span><span class="sxs-lookup"><span data-stu-id="6b39e-108">A company can define multiple call center channels in Commerce.</span></span> 

<span data-ttu-id="6b39e-109">在创建新呼叫中心渠道之前，请确保已完成[渠道设置先决条件](channels-prerequisites.md)。</span><span class="sxs-lookup"><span data-stu-id="6b39e-109">Before you create a new call center channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="6b39e-110">创建和配置新呼叫中心渠道</span><span class="sxs-lookup"><span data-stu-id="6b39e-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="6b39e-111">要创建和配置新呼叫中心渠道，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="6b39e-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="6b39e-112">在导航窗格中，转到**模块 \> 渠道 \> 呼叫中心 \> 所有呼叫中心**。</span><span class="sxs-lookup"><span data-stu-id="6b39e-112">In the navigation pane, go to **Modules \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="6b39e-113">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="6b39e-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6b39e-114">在**名称**字段中，为新渠道提供名称。</span><span class="sxs-lookup"><span data-stu-id="6b39e-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="6b39e-115">从下拉列表中选择适当的**法人**。</span><span class="sxs-lookup"><span data-stu-id="6b39e-115">Select the appropriate **Legal entity** from the drop down.</span></span>
1. <span data-ttu-id="6b39e-116">从下拉列表中选择适当的**仓库**位置。</span><span class="sxs-lookup"><span data-stu-id="6b39e-116">Select the appropriate **Warehouse** location from the drop down.</span></span>
1. <span data-ttu-id="6b39e-117">在**默认客户**字段中，请提供有效的默认客户。</span><span class="sxs-lookup"><span data-stu-id="6b39e-117">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="6b39e-118">在**电子邮件通知配置文件**字段中，请提供有效的电子邮件通知配置文件。</span><span class="sxs-lookup"><span data-stu-id="6b39e-118">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="6b39e-119">提供**价格覆盖**信息代码。</span><span class="sxs-lookup"><span data-stu-id="6b39e-119">Provide a **Price override** info code.</span></span> <span data-ttu-id="6b39e-120">请注意，您可能首先需要为此创建一个信息代码。</span><span class="sxs-lookup"><span data-stu-id="6b39e-120">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="6b39e-121">提供一个**保留代码**信息代码。</span><span class="sxs-lookup"><span data-stu-id="6b39e-121">Provide a **Hold code** info code.</span></span> <span data-ttu-id="6b39e-122">请注意，您可能首先需要为此创建一个信息代码。</span><span class="sxs-lookup"><span data-stu-id="6b39e-122">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="6b39e-123">提供一个**贷记**信息代码。</span><span class="sxs-lookup"><span data-stu-id="6b39e-123">Provide a **Credit** info code.</span></span> <span data-ttu-id="6b39e-124">请注意，您可能首先需要为此创建一个信息代码。</span><span class="sxs-lookup"><span data-stu-id="6b39e-124">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="6b39e-125">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="6b39e-125">Select **Save**.</span></span>

<span data-ttu-id="6b39e-126">下图显示了新呼叫中心渠道的创建过程。</span><span class="sxs-lookup"><span data-stu-id="6b39e-126">The following image shows the creation of a new call center channel.</span></span>

![新呼叫中心渠道](media/channel-setup-callcenter-1.png)

<span data-ttu-id="6b39e-128">下图显示了一个呼叫中心渠道示例。</span><span class="sxs-lookup"><span data-stu-id="6b39e-128">The following image shows an example call center channel.</span></span>

![呼叫中心渠道示例](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="6b39e-130">其他渠道设置</span><span class="sxs-lookup"><span data-stu-id="6b39e-130">Additional channel setup</span></span>

<span data-ttu-id="6b39e-131">呼叫中心渠道设置所需的其他任务包括设置付款方式和交货方式。</span><span class="sxs-lookup"><span data-stu-id="6b39e-131">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="6b39e-132">下图显示了**设置**选项卡上的**交货方式**和**付款方式**设置选项。</span><span class="sxs-lookup"><span data-stu-id="6b39e-132">The following image shows **Modes of delivery** and **Payment methods** set up options on the **Set up** tab.</span></span>

![其他呼叫中心渠道设置操作](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="6b39e-134">设置付款方式</span><span class="sxs-lookup"><span data-stu-id="6b39e-134">Set up payment methods</span></span>

<span data-ttu-id="6b39e-135">要设置付款方式，请针对此渠道支持的每种付款类型执行这些步骤。</span><span class="sxs-lookup"><span data-stu-id="6b39e-135">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="6b39e-136">在操作窗格上，选择**设置**选项卡，然后选择**付款方式**。</span><span class="sxs-lookup"><span data-stu-id="6b39e-136">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="6b39e-137">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="6b39e-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6b39e-138">在导航窗格中，选择所需的付款方式。</span><span class="sxs-lookup"><span data-stu-id="6b39e-138">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="6b39e-139">在**常规**部分，提供**操作名称**并配置任何其他所需的设置。</span><span class="sxs-lookup"><span data-stu-id="6b39e-139">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="6b39e-140">根据付款类型的要求配置任何其他设置。</span><span class="sxs-lookup"><span data-stu-id="6b39e-140">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="6b39e-141">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="6b39e-141">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6b39e-142">下图显示了现金支付方式的示例。</span><span class="sxs-lookup"><span data-stu-id="6b39e-142">The following image shows an example of a cash payment method.</span></span>

![付款方法示例](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="6b39e-144">设置交货方式</span><span class="sxs-lookup"><span data-stu-id="6b39e-144">Set up modes of delivery</span></span>

<span data-ttu-id="6b39e-145">您可以从**操作窗格**上的**设置**选项卡中选择**交货方式**来查看已配置的交货方式。</span><span class="sxs-lookup"><span data-stu-id="6b39e-145">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="6b39e-146">要更改或添加交货方式，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="6b39e-146">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="6b39e-147">在导航窗格中，转到**模块 \> 库存管理 \> 交货方式**。</span><span class="sxs-lookup"><span data-stu-id="6b39e-147">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="6b39e-148">在操作窗格上，选择**新增**以创建新的交货方式，或选择现有方式。</span><span class="sxs-lookup"><span data-stu-id="6b39e-148">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="6b39e-149">在**零售渠道**部分，选择**添加行**以添加渠道。</span><span class="sxs-lookup"><span data-stu-id="6b39e-149">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="6b39e-150">使用组织节点添加渠道而不是单独添加每个渠道可以简化渠道添加操作。</span><span class="sxs-lookup"><span data-stu-id="6b39e-150">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="6b39e-151">下图显示了交货方式的示例。</span><span class="sxs-lookup"><span data-stu-id="6b39e-151">The following image shows an example of a mode of delivery.</span></span>

![设置交货方式](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a><span data-ttu-id="6b39e-153">其他资源</span><span class="sxs-lookup"><span data-stu-id="6b39e-153">Additional resources</span></span>

[<span data-ttu-id="6b39e-154">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="6b39e-154">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="6b39e-155">呼叫中心销售功能</span><span class="sxs-lookup"><span data-stu-id="6b39e-155">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="6b39e-156">设置呼叫中心订单处理选项</span><span class="sxs-lookup"><span data-stu-id="6b39e-156">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="6b39e-157">呼叫中心目录</span><span class="sxs-lookup"><span data-stu-id="6b39e-157">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="6b39e-158">设置和使用欺诈预警</span><span class="sxs-lookup"><span data-stu-id="6b39e-158">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="6b39e-159">设置呼叫中心的连续性计划</span><span class="sxs-lookup"><span data-stu-id="6b39e-159">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)

---
title: 设置零售渠道
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新的零售渠道。
author: samjarawan
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3f1f5dc2c8402d9b6b68a049f804932812eb74c0
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937526"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="24560-103">设置零售渠道</span><span class="sxs-lookup"><span data-stu-id="24560-103">Set up a retail channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="24560-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新的零售渠道。</span><span class="sxs-lookup"><span data-stu-id="24560-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="24560-105">Dynamics 365 Commerce 支持多种零售渠道。</span><span class="sxs-lookup"><span data-stu-id="24560-105">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="24560-106">这些零售渠道包括在线商店、呼叫中心和零售商店（亦称实体商店）。</span><span class="sxs-lookup"><span data-stu-id="24560-106">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="24560-107">每个零售商店渠道都可以有自己的付款方式、价格组、销售点 (POS) 收银机、收入帐户和支出帐户以及职员。</span><span class="sxs-lookup"><span data-stu-id="24560-107">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="24560-108">您必须先设置所有这些元素，然后才能创建零售商店渠道。</span><span class="sxs-lookup"><span data-stu-id="24560-108">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="24560-109">在创建零售渠道之前，请确保满足[渠道先决条件](channels-prerequisites.md)。</span><span class="sxs-lookup"><span data-stu-id="24560-109">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="24560-110">创建和配置新零售渠道</span><span class="sxs-lookup"><span data-stu-id="24560-110">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="24560-111">在导航窗格中，转到 **模块 \> 渠道 \> 商店 \> 所有商店**。</span><span class="sxs-lookup"><span data-stu-id="24560-111">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="24560-112">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="24560-112">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="24560-113">在 **名称** 字段中，为新渠道提供名称。</span><span class="sxs-lookup"><span data-stu-id="24560-113">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="24560-114">在 **商店编号** 字段中，提供唯一的商店编号。</span><span class="sxs-lookup"><span data-stu-id="24560-114">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="24560-115">该编号可以是字母数字，最多 10 个字符。</span><span class="sxs-lookup"><span data-stu-id="24560-115">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="24560-116">在 **法人** 下拉列表中，输入适当的法人。</span><span class="sxs-lookup"><span data-stu-id="24560-116">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="24560-117">在 **仓库** 下拉列表中，输入适当的仓库。</span><span class="sxs-lookup"><span data-stu-id="24560-117">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="24560-118">在 **商店时区** 字段中，选择适当的时区。</span><span class="sxs-lookup"><span data-stu-id="24560-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="24560-119">在 **销售税组** 下拉列表中，为商店选择适当的销售税组。</span><span class="sxs-lookup"><span data-stu-id="24560-119">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="24560-120">在 **货币** 字段中，选择适当的货币。</span><span class="sxs-lookup"><span data-stu-id="24560-120">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="24560-121">在 **客户通讯簿** 字段中，提供有效的通讯簿。</span><span class="sxs-lookup"><span data-stu-id="24560-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="24560-122">在 **默认客户** 字段中，请提供有效的默认客户。</span><span class="sxs-lookup"><span data-stu-id="24560-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="24560-123">在 **功能配置文件** 字段中，选择功能配置文件（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="24560-123">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="24560-124">在 **电子邮件通知配置文件** 字段中，请提供有效的电子邮件通知配置文件。</span><span class="sxs-lookup"><span data-stu-id="24560-124">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="24560-125">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="24560-125">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="24560-126">下图显示了新零售渠道的创建过程。</span><span class="sxs-lookup"><span data-stu-id="24560-126">The following image shows the creation of a new retail channel.</span></span>

![新零售渠道](media/channel-setup-retail-1.png)

<span data-ttu-id="24560-128">下图显示了一个零售渠道示例。</span><span class="sxs-lookup"><span data-stu-id="24560-128">The following image shows an example retail channel.</span></span>

![零售渠道示例](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="24560-130">其他设置</span><span class="sxs-lookup"><span data-stu-id="24560-130">Other settings</span></span>

<span data-ttu-id="24560-131">可以在 **报表/结算** 和 **杂项** 部分中根据零售商店的需求设置许多其他可选设置。</span><span class="sxs-lookup"><span data-stu-id="24560-131">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="24560-132">另外，请参阅 [销售点 (POS) 的屏幕布局](pos-screen-layouts.md)，了解有关在 **屏幕布局** 部分中设置默认屏幕布局的信息；参阅 [配置和安装 Retail 硬件工作站](retail-hardware-station-configuration-installation.md)，了解有关 **硬件工作站** 部分的设置信息。</span><span class="sxs-lookup"><span data-stu-id="24560-132">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="24560-133">下图显示了一个零售渠道设置配置示例。</span><span class="sxs-lookup"><span data-stu-id="24560-133">The following image shows an example retail channel setup configuration.</span></span>

![零售渠道配置示例](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="24560-135">其他渠道设置</span><span class="sxs-lookup"><span data-stu-id="24560-135">Additional channel set up</span></span>

<span data-ttu-id="24560-136">可以在操作窗格上 **设置** 部分下找到需要为渠道设置的其他项。</span><span class="sxs-lookup"><span data-stu-id="24560-136">There are additional items that need to be set up for a channel that can be found on the Action Pane under the **Set up** section.</span></span>

<span data-ttu-id="24560-137">在线渠道设置所需的其他任务包括设置付款方式、现金申报、交货方式、收入/费用帐户、部门、履行组分配和金库。</span><span class="sxs-lookup"><span data-stu-id="24560-137">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="24560-138">下图显示了 **设置** 选项卡上的各个其他零售渠道设置选项。</span><span class="sxs-lookup"><span data-stu-id="24560-138">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![设置渠道](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="24560-140">设置付款方式</span><span class="sxs-lookup"><span data-stu-id="24560-140">Set up payment methods</span></span>

<span data-ttu-id="24560-141">要设置付款方式，请针对此渠道支持的每种付款类型执行这些步骤。</span><span class="sxs-lookup"><span data-stu-id="24560-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="24560-142">在操作窗格上，选择 **设置** 选项卡，然后选择 **付款方式**。</span><span class="sxs-lookup"><span data-stu-id="24560-142">On the Action Pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="24560-143">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="24560-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="24560-144">在导航窗格中，选择所需的付款方式。</span><span class="sxs-lookup"><span data-stu-id="24560-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="24560-145">在 **常规** 部分，提供 **操作名称** 并配置任何其他所需的设置。</span><span class="sxs-lookup"><span data-stu-id="24560-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="24560-146">根据付款类型的要求配置任何其他设置。</span><span class="sxs-lookup"><span data-stu-id="24560-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="24560-147">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="24560-147">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="24560-148">下图显示了现金支付方式的示例。</span><span class="sxs-lookup"><span data-stu-id="24560-148">The following image shows an example of a cash payment method.</span></span>

![付款方法示例](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="24560-150">设置现金清点</span><span class="sxs-lookup"><span data-stu-id="24560-150">Set up cash declaration</span></span>

1. <span data-ttu-id="24560-151">在操作窗格上，选择 **设置** 选项卡，然后选择 **现金清点**。</span><span class="sxs-lookup"><span data-stu-id="24560-151">On the Action Pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="24560-152">在操作窗格上，选择 **新增**，然后创建所有适用的 **硬币** 和 **纸币** 面额。</span><span class="sxs-lookup"><span data-stu-id="24560-152">On the Action Pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="24560-153">下图显示了现金清点的示例。</span><span class="sxs-lookup"><span data-stu-id="24560-153">The following image shows an example of a cash declaration.</span></span>

![设置现金清点](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="24560-155">设置交货方式</span><span class="sxs-lookup"><span data-stu-id="24560-155">Set up modes of delivery</span></span>

<span data-ttu-id="24560-156">您可以从操作窗格上的 **设置** 选项卡中选择 **交货方式** 来查看已配置的交货方式。</span><span class="sxs-lookup"><span data-stu-id="24560-156">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the Action Pane.</span></span>  

<span data-ttu-id="24560-157">要更改或添加交货方式，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="24560-157">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="24560-158">在导航窗格中，转到 **模块 \> 库存管理 \> 交货方式**。</span><span class="sxs-lookup"><span data-stu-id="24560-158">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="24560-159">在操作窗格上，选择 **新建** 创建新的交货方式，或选择现有方式。</span><span class="sxs-lookup"><span data-stu-id="24560-159">On the Action Pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="24560-160">在 **零售渠道** 部分，选择 **添加行** 以添加渠道。</span><span class="sxs-lookup"><span data-stu-id="24560-160">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="24560-161">使用组织节点添加渠道而不是单独添加每个渠道可以简化渠道添加操作。</span><span class="sxs-lookup"><span data-stu-id="24560-161">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="24560-162">下图显示了交货方式的示例。</span><span class="sxs-lookup"><span data-stu-id="24560-162">The following image shows an example of a mode of delivery.</span></span>

![设置交货方式](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="24560-164">设置收入/支出帐户</span><span class="sxs-lookup"><span data-stu-id="24560-164">Set up income/expense account</span></span>

<span data-ttu-id="24560-165">要设置收入/支出帐户，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="24560-165">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="24560-166">在操作窗格上，选择 **设置** 选项卡，然后选择 **收入/支出帐户**。</span><span class="sxs-lookup"><span data-stu-id="24560-166">On the Action Pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="24560-167">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="24560-167">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="24560-168">在 **名称** 下面，输入名称。</span><span class="sxs-lookup"><span data-stu-id="24560-168">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="24560-169">在 **搜索名称** 下面，输入搜索名称。</span><span class="sxs-lookup"><span data-stu-id="24560-169">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="24560-170">在 **帐户类型** 下面，输入帐户类型。</span><span class="sxs-lookup"><span data-stu-id="24560-170">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="24560-171">根据需要在 **消息行 1**、**消息行 2**、**票单文本 1** 和 **票单文本 2** 中输入文字。</span><span class="sxs-lookup"><span data-stu-id="24560-171">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="24560-172">在 **过帐** 下面，输入过帐信息。</span><span class="sxs-lookup"><span data-stu-id="24560-172">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="24560-173">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="24560-173">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="24560-174">下图显示了收入/支出帐户的示例。</span><span class="sxs-lookup"><span data-stu-id="24560-174">The following image shows an example of an income/expense account.</span></span>

![设置收入/支出帐户](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="24560-176">设置部门</span><span class="sxs-lookup"><span data-stu-id="24560-176">Set up sections</span></span>

<span data-ttu-id="24560-177">要设置部门，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="24560-177">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="24560-178">在操作窗格上，选择 **设置** 选项卡，然后单击 **部门**。</span><span class="sxs-lookup"><span data-stu-id="24560-178">On the Action Pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="24560-179">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="24560-179">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="24560-180">在 **部门编号** 下面，输入部门编号。</span><span class="sxs-lookup"><span data-stu-id="24560-180">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="24560-181">在 **描述** 下面，输入描述。</span><span class="sxs-lookup"><span data-stu-id="24560-181">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="24560-182">在 **部门规模** 下面，输入部门规模。</span><span class="sxs-lookup"><span data-stu-id="24560-182">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="24560-183">根据需要针对 **常规** 和 **销售统计** 配置其他设置。</span><span class="sxs-lookup"><span data-stu-id="24560-183">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="24560-184">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="24560-184">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="24560-185">设置履行组分配</span><span class="sxs-lookup"><span data-stu-id="24560-185">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="24560-186">若要设置履行组分配，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="24560-186">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="24560-187">在操作窗格上，选择 **设置** 选项卡，然后选择 **履行组分配**。</span><span class="sxs-lookup"><span data-stu-id="24560-187">On the Action Pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="24560-188">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="24560-188">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="24560-189">在 **履行组** 下拉列表中，选择一个履行组。</span><span class="sxs-lookup"><span data-stu-id="24560-189">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="24560-190">在 **描述** 下拉列表中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="24560-190">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="24560-191">在操作窗格上，选择 **保存**</span><span class="sxs-lookup"><span data-stu-id="24560-191">On the Action Pane, select **Save**</span></span>

<span data-ttu-id="24560-192">下图显示了履行组分配设置的示例。</span><span class="sxs-lookup"><span data-stu-id="24560-192">The following image shows an example of a fulfillment group assignment setup.</span></span>

![设置履行组分配](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="24560-194">设置金库</span><span class="sxs-lookup"><span data-stu-id="24560-194">Set up safes</span></span>

<span data-ttu-id="24560-195">要设置金库，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="24560-195">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="24560-196">在操作窗格上，选择 **设置** 选项卡，然后单击 **金库**。</span><span class="sxs-lookup"><span data-stu-id="24560-196">On the Action Pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="24560-197">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="24560-197">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="24560-198">输入金库的名称</span><span class="sxs-lookup"><span data-stu-id="24560-198">Enter a name for the safe.</span></span>
1. <span data-ttu-id="24560-199">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="24560-199">On the Action Pane, select **Save**.</span></span>

### <a name="ensure-unique-transaction-ids"></a><span data-ttu-id="24560-200">确保交易 ID 是唯一的</span><span class="sxs-lookup"><span data-stu-id="24560-200">Ensure unique transaction IDs</span></span>

<span data-ttu-id="24560-201">从 Commerce 版本 10.0.18 开始，为销售点 (POS) 生成的交易 ID 采用序列形式，包括以下部分：</span><span class="sxs-lookup"><span data-stu-id="24560-201">As of the Commerce version 10.0.18 , transaction IDs generated for the point of sale (POS) are sequential and include the following parts:</span></span>

- <span data-ttu-id="24560-202">固定部分，商店 ID 和终端 ID 的串联。</span><span class="sxs-lookup"><span data-stu-id="24560-202">A fixed part, which is a concatenation of store ID and terminal ID.</span></span> 
- <span data-ttu-id="24560-203">序列部分，一个数字序列。</span><span class="sxs-lookup"><span data-stu-id="24560-203">A sequential part, which is a number sequence.</span></span> 

<span data-ttu-id="24560-204">具体来说，格式为 *{store}-{terminal}-{numbersequence}*。</span><span class="sxs-lookup"><span data-stu-id="24560-204">Specifically, the format is *{store}-{terminal}-{numbersequence}*.</span></span> 

<span data-ttu-id="24560-205">由于可以在脱机和联机模式下生成交易 ID，因此已经存在生成重复交易 ID 的情况。</span><span class="sxs-lookup"><span data-stu-id="24560-205">Because transaction IDs can be generated in offline and online modes, there have been instances of duplicate transaction IDs being generated.</span></span> <span data-ttu-id="24560-206">消除重复的交易 ID 需要进行大量的手动数据修复。</span><span class="sxs-lookup"><span data-stu-id="24560-206">Eliminating duplicate transaction IDs requires a lot of manual data fixing.</span></span> 

<span data-ttu-id="24560-207">在 Commerce 版本 10.0.19 中，交易 ID 格式已更新，删除了序列部分，改为使用通过计算自 1970 年以来的时间（以毫秒为单位）生成的 13 位数字。</span><span class="sxs-lookup"><span data-stu-id="24560-207">With Commerce version 10.0.19, the transaction ID format has been updated to remove the sequential part and instead uses a 13-digit number generated by calculating the time in milliseconds since 1970.</span></span> <span data-ttu-id="24560-208">进行此更改后，新的交易 ID 格式为 *{store}-{terminal}-{millisecondsSince1970}*。</span><span class="sxs-lookup"><span data-stu-id="24560-208">With this change, the new transaction ID format is *{store}-{terminal}-{millisecondsSince1970}*.</span></span> <span data-ttu-id="24560-209">此更新使交易 ID 不再序列化，确保交易 ID 始终是唯一的。</span><span class="sxs-lookup"><span data-stu-id="24560-209">This update makes the transaction ID non-sequential and ensures that transaction IDs are always unique.</span></span> 

> [!NOTE]
> <span data-ttu-id="24560-210">交易 ID 仅用于内部系统，因此不需要序列化。</span><span class="sxs-lookup"><span data-stu-id="24560-210">Transaction IDs are meant for internal system use only, so they are not required to be sequential.</span></span> <span data-ttu-id="24560-211">但是，很多国家/地区要求收据 ID 采用序列形式。</span><span class="sxs-lookup"><span data-stu-id="24560-211">However, many countries require receipt IDs to be sequential.</span></span>

<span data-ttu-id="24560-212">可以从 **功能管理** 工作区启用新交易 ID 格式功能。</span><span class="sxs-lookup"><span data-stu-id="24560-212">The new transaction ID format feature can be enabled from the **Feature management** workspace.</span></span> 

<span data-ttu-id="24560-213">若要启用新的交易 ID，请按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="24560-213">To enable the use of new transaction IDs, follow these steps:</span></span>

1. <span data-ttu-id="24560-214">在 Commerce Headquarters 中，转到 **系统管理 \> 工作区 \> 功能管理**。</span><span class="sxs-lookup"><span data-stu-id="24560-214">In Commerce headquarters, go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="24560-215">筛选“retail 和 commerce”模块。</span><span class="sxs-lookup"><span data-stu-id="24560-215">Filter for the "retail and commerce" module.</span></span>
1. <span data-ttu-id="24560-216">搜索 **启用新交易 ID 以避免交易 ID 重复** 功能名称。</span><span class="sxs-lookup"><span data-stu-id="24560-216">Search for the **Enable new transaction id to avoid duplicate transaction ids** feature name.</span></span>
1. <span data-ttu-id="24560-217">选择该功能，然后在右窗格中选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="24560-217">Select the feature, and then select **Enable Now** in the right pane.</span></span>  
1. <span data-ttu-id="24560-218">转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。</span><span class="sxs-lookup"><span data-stu-id="24560-218">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="24560-219">运行 **1070 渠道配置** 和 **1170 POS 任务录制器** 作业，将已启用的功能同步到商店。</span><span class="sxs-lookup"><span data-stu-id="24560-219">Run the **1070 Channel configuration** and **1170 POS task recorder** jobs to synchronize the enabled feature to the stores.</span></span>
1. <span data-ttu-id="24560-220">将更改发送到商店后，必须关闭 POS 终端，然后重新打开才能使用新交易 ID 格式。</span><span class="sxs-lookup"><span data-stu-id="24560-220">After the changes have been sent to the stores, POS terminals must be closed and reopened to use the new transaction ID format.</span></span> 

> [!NOTE]
> <span data-ttu-id="24560-221">启用新交易 ID 格式功能后，您将无法禁用此功能。</span><span class="sxs-lookup"><span data-stu-id="24560-221">After the new transaction ID format feature is enabled, you will not be able to disable this feature.</span></span> <span data-ttu-id="24560-222">如果必须禁用，请联系 Commerce 支持。</span><span class="sxs-lookup"><span data-stu-id="24560-222">If it must be disabled, please contact Commerce Support.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24560-223">其他资源</span><span class="sxs-lookup"><span data-stu-id="24560-223">Additional resources</span></span>

[<span data-ttu-id="24560-224">渠道概览</span><span class="sxs-lookup"><span data-stu-id="24560-224">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="24560-225">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="24560-225">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="24560-226">设置在线渠道</span><span class="sxs-lookup"><span data-stu-id="24560-226">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="24560-227">设置呼叫中心渠道</span><span class="sxs-lookup"><span data-stu-id="24560-227">Set up a call center channel</span></span>](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

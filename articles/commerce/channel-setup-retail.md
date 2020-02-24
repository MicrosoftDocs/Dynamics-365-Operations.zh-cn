---
title: 设置零售渠道
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新的零售渠道。
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
ms.openlocfilehash: 8ac01f36912fa5e8a09bb4f324ef272cec737aa1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002373"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="7d17d-103">设置零售渠道</span><span class="sxs-lookup"><span data-stu-id="7d17d-103">Set up a retail channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7d17d-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新的零售渠道。</span><span class="sxs-lookup"><span data-stu-id="7d17d-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7d17d-105">概览</span><span class="sxs-lookup"><span data-stu-id="7d17d-105">Overview</span></span>

<span data-ttu-id="7d17d-106">Dynamics 365 Commerce 支持多种零售渠道。</span><span class="sxs-lookup"><span data-stu-id="7d17d-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="7d17d-107">这些零售渠道包括在线商店、呼叫中心和零售商店（亦称实体商店）。</span><span class="sxs-lookup"><span data-stu-id="7d17d-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="7d17d-108">每个零售商店渠道都可以有自己的付款方式、价格组、销售点 (POS) 收银机、收入帐户和支出帐户以及职员。</span><span class="sxs-lookup"><span data-stu-id="7d17d-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="7d17d-109">您必须先设置所有这些元素，然后才能创建零售商店渠道。</span><span class="sxs-lookup"><span data-stu-id="7d17d-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="7d17d-110">在创建零售渠道之前，请确保满足[渠道先决条件](channels-prerequisites.md)。</span><span class="sxs-lookup"><span data-stu-id="7d17d-110">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="7d17d-111">创建和配置新零售渠道</span><span class="sxs-lookup"><span data-stu-id="7d17d-111">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="7d17d-112">在导航窗格中，转到**模块 \> 渠道 \> 商店 \> 所有商店**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-112">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="7d17d-113">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7d17d-114">在**名称**字段中，为新渠道提供名称。</span><span class="sxs-lookup"><span data-stu-id="7d17d-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="7d17d-115">在**商店编号**字段中，提供唯一的商店编号。</span><span class="sxs-lookup"><span data-stu-id="7d17d-115">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="7d17d-116">该编号可以是字母数字，最多 10 个字符。</span><span class="sxs-lookup"><span data-stu-id="7d17d-116">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="7d17d-117">在**法人**下拉列表中，输入适当的法人。</span><span class="sxs-lookup"><span data-stu-id="7d17d-117">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="7d17d-118">在**仓库**下拉列表中，输入适当的仓库。</span><span class="sxs-lookup"><span data-stu-id="7d17d-118">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="7d17d-119">在**商店时区**字段中，选择适当的时区。</span><span class="sxs-lookup"><span data-stu-id="7d17d-119">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="7d17d-120">在**销售税组**下拉列表中，为商店选择适当的销售税组。</span><span class="sxs-lookup"><span data-stu-id="7d17d-120">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="7d17d-121">在**货币**字段中，选择适当的货币。</span><span class="sxs-lookup"><span data-stu-id="7d17d-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="7d17d-122">在**客户通讯簿**字段中，提供有效的通讯簿。</span><span class="sxs-lookup"><span data-stu-id="7d17d-122">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="7d17d-123">在**默认客户**字段中，请提供有效的默认客户。</span><span class="sxs-lookup"><span data-stu-id="7d17d-123">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="7d17d-124">在**功能配置文件**字段中，选择功能配置文件（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="7d17d-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="7d17d-125">在**电子邮件通知配置文件**字段中，请提供有效的电子邮件通知配置文件。</span><span class="sxs-lookup"><span data-stu-id="7d17d-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="7d17d-126">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7d17d-127">下图显示了新零售渠道的创建过程。</span><span class="sxs-lookup"><span data-stu-id="7d17d-127">The following image shows the creation of a new retail channel.</span></span>

![新零售渠道](media/channel-setup-retail-1.png)

<span data-ttu-id="7d17d-129">下图显示了一个零售渠道示例。</span><span class="sxs-lookup"><span data-stu-id="7d17d-129">The following image shows an example retail channel.</span></span>

![零售渠道示例](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="7d17d-131">其他设置</span><span class="sxs-lookup"><span data-stu-id="7d17d-131">Other settings</span></span>

<span data-ttu-id="7d17d-132">可以在**报表/结算**和**杂项**部分中根据零售商店的需求设置许多其他可选设置。</span><span class="sxs-lookup"><span data-stu-id="7d17d-132">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="7d17d-133">另外，请参阅[销售点 (POS) 的屏幕布局](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)，了解有关在**屏幕布局**部分中设置默认屏幕布局的信息；参阅[配置和安装 Retail 硬件工作站](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation)，了解有关**硬件工作站**部分的设置信息。</span><span class="sxs-lookup"><span data-stu-id="7d17d-133">In addition, see [Screen layouts for the point of sale (POS)](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="7d17d-134">下图显示了一个零售渠道设置配置示例。</span><span class="sxs-lookup"><span data-stu-id="7d17d-134">The following image shows an example retail channel setup configuration.</span></span>

![零售渠道配置示例](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="7d17d-136">其他渠道设置</span><span class="sxs-lookup"><span data-stu-id="7d17d-136">Additional channel set up</span></span>

<span data-ttu-id="7d17d-137">可以在**操作窗格**上**设置**部分下面中找到需要为渠道设置的其他项。</span><span class="sxs-lookup"><span data-stu-id="7d17d-137">There are additional items that need to be set up for a channel that can be found on the **Action pane** under the **Set up** section.</span></span>

<span data-ttu-id="7d17d-138">在线渠道设置所需的其他任务包括设置付款方式、现金申报、交货方式、收入/费用帐户、部门、履行组分配和金库。</span><span class="sxs-lookup"><span data-stu-id="7d17d-138">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="7d17d-139">下图显示了**设置**选项卡上的各个其他零售渠道设置选项。</span><span class="sxs-lookup"><span data-stu-id="7d17d-139">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![设置渠道](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="7d17d-141">设置付款方式</span><span class="sxs-lookup"><span data-stu-id="7d17d-141">Set up payment methods</span></span>

<span data-ttu-id="7d17d-142">要设置付款方式，请针对此渠道支持的每种付款类型执行这些步骤。</span><span class="sxs-lookup"><span data-stu-id="7d17d-142">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="7d17d-143">在操作窗格上，选择**设置**选项卡，然后选择**付款方式**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-143">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="7d17d-144">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-144">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7d17d-145">在导航窗格中，选择所需的付款方式。</span><span class="sxs-lookup"><span data-stu-id="7d17d-145">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="7d17d-146">在**常规**部分，提供**操作名称**并配置任何其他所需的设置。</span><span class="sxs-lookup"><span data-stu-id="7d17d-146">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="7d17d-147">根据付款类型的要求配置任何其他设置。</span><span class="sxs-lookup"><span data-stu-id="7d17d-147">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="7d17d-148">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7d17d-149">下图显示了现金支付方式的示例。</span><span class="sxs-lookup"><span data-stu-id="7d17d-149">The following image shows an example of a cash payment method.</span></span>

![付款方法示例](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="7d17d-151">设置现金清点</span><span class="sxs-lookup"><span data-stu-id="7d17d-151">Set up cash declaration</span></span>

1. <span data-ttu-id="7d17d-152">在操作窗格上，选择**设置**选项卡，然后选择**现金清点**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-152">On the action pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="7d17d-153">在操作窗格上，选择**新增**，然后创建所有适用的**硬币**和**纸币**面额。</span><span class="sxs-lookup"><span data-stu-id="7d17d-153">On the action pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="7d17d-154">下图显示了现金清点的示例。</span><span class="sxs-lookup"><span data-stu-id="7d17d-154">The following image shows an example of a cash declaration.</span></span>

![设置现金清点](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="7d17d-156">设置交货方式</span><span class="sxs-lookup"><span data-stu-id="7d17d-156">Set up modes of delivery</span></span>

<span data-ttu-id="7d17d-157">您可以从**操作窗格**上的**设置**选项卡中选择**交货方式**来查看已配置的交货方式。</span><span class="sxs-lookup"><span data-stu-id="7d17d-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="7d17d-158">要更改或添加交货方式，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="7d17d-158">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="7d17d-159">在导航窗格中，转到**模块 \> 库存管理 \> 交货方式**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-159">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="7d17d-160">在操作窗格上，选择**新增**以创建新的交货方式，或选择现有方式。</span><span class="sxs-lookup"><span data-stu-id="7d17d-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="7d17d-161">在**零售渠道**部分，选择**添加行**以添加渠道。</span><span class="sxs-lookup"><span data-stu-id="7d17d-161">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="7d17d-162">使用组织节点添加渠道而不是单独添加每个渠道可以简化渠道添加操作。</span><span class="sxs-lookup"><span data-stu-id="7d17d-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="7d17d-163">下图显示了交货方式的示例。</span><span class="sxs-lookup"><span data-stu-id="7d17d-163">The following image shows an example of a mode of delivery.</span></span>

![设置交货方式](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="7d17d-165">设置收入/支出帐户</span><span class="sxs-lookup"><span data-stu-id="7d17d-165">Set up income/expense account</span></span>

<span data-ttu-id="7d17d-166">要设置收入/支出帐户，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="7d17d-166">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="7d17d-167">在操作窗格上，选择**设置**选项卡，然后选择**收入/支出帐户**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-167">On the action pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="7d17d-168">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-168">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7d17d-169">在**名称**下面，输入名称。</span><span class="sxs-lookup"><span data-stu-id="7d17d-169">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="7d17d-170">在**搜索名称**下面，输入搜索名称。</span><span class="sxs-lookup"><span data-stu-id="7d17d-170">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="7d17d-171">在**帐户类型**下面，输入帐户类型。</span><span class="sxs-lookup"><span data-stu-id="7d17d-171">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="7d17d-172">根据需要在**消息行 1**、**消息行 2**、**票单文本 1** 和**票单文本 2** 中输入文字。</span><span class="sxs-lookup"><span data-stu-id="7d17d-172">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="7d17d-173">在**过帐**下面，输入过帐信息。</span><span class="sxs-lookup"><span data-stu-id="7d17d-173">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="7d17d-174">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-174">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7d17d-175">下图显示了收入/支出帐户的示例。</span><span class="sxs-lookup"><span data-stu-id="7d17d-175">The following image shows an example of an income/expense account.</span></span>

![设置收入/支出帐户](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="7d17d-177">设置部门</span><span class="sxs-lookup"><span data-stu-id="7d17d-177">Set up sections</span></span>

<span data-ttu-id="7d17d-178">要设置部门，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="7d17d-178">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="7d17d-179">在操作窗格上，选择**设置**选项卡，然后单击**部门**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-179">On the action pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="7d17d-180">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-180">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7d17d-181">在**部门编号**下面，输入部门编号。</span><span class="sxs-lookup"><span data-stu-id="7d17d-181">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="7d17d-182">在**描述**下面，输入描述。</span><span class="sxs-lookup"><span data-stu-id="7d17d-182">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="7d17d-183">在**部门规模**下面，输入部门规模。</span><span class="sxs-lookup"><span data-stu-id="7d17d-183">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="7d17d-184">根据需要针对**常规**和**销售统计**配置其他设置。</span><span class="sxs-lookup"><span data-stu-id="7d17d-184">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="7d17d-185">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-185">On the action pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="7d17d-186">设置履行组分配</span><span class="sxs-lookup"><span data-stu-id="7d17d-186">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="7d17d-187">若要设置履行组分配，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="7d17d-187">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="7d17d-188">在操作窗格上，选择**设置**选项卡，然后选择**履行组分配**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-188">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="7d17d-189">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-189">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7d17d-190">在**履行组**下拉列表中，选择一个履行组。</span><span class="sxs-lookup"><span data-stu-id="7d17d-190">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="7d17d-191">在**描述**下拉列表中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="7d17d-191">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="7d17d-192">在操作窗格上，选择**保存**</span><span class="sxs-lookup"><span data-stu-id="7d17d-192">On the action pane, select **Save**</span></span>

<span data-ttu-id="7d17d-193">下图显示了履行组分配设置的示例。</span><span class="sxs-lookup"><span data-stu-id="7d17d-193">The following image shows an example of a fulfillment group assignment setup.</span></span>

![设置履行组分配](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="7d17d-195">设置金库</span><span class="sxs-lookup"><span data-stu-id="7d17d-195">Set up safes</span></span>

<span data-ttu-id="7d17d-196">要设置金库，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="7d17d-196">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="7d17d-197">在操作窗格上，选择**设置**选项卡，然后单击**金库**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-197">On the action pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="7d17d-198">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-198">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7d17d-199">输入金库的名称</span><span class="sxs-lookup"><span data-stu-id="7d17d-199">Enter a name for the safe.</span></span>
1. <span data-ttu-id="7d17d-200">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="7d17d-200">On the action pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d17d-201">其他资源</span><span class="sxs-lookup"><span data-stu-id="7d17d-201">Additional resources</span></span>

[<span data-ttu-id="7d17d-202">渠道概览</span><span class="sxs-lookup"><span data-stu-id="7d17d-202">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="7d17d-203">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="7d17d-203">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="7d17d-204">设置在线渠道</span><span class="sxs-lookup"><span data-stu-id="7d17d-204">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="7d17d-205">设置呼叫中心渠道</span><span class="sxs-lookup"><span data-stu-id="7d17d-205">Set up a call center channel</span></span>](channel-setup-callcenter.md)


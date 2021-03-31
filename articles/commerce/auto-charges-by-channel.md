---
title: 启用和配置按渠道自动收费
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中启用和配置按渠道自动收费。
author: gvrmohanreddy
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 834d90c8ec8515c6bced2d8a4fabc79b4e4e4c3e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211265"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a><span data-ttu-id="a0c8e-103">按渠道启用和配置自动费用</span><span class="sxs-lookup"><span data-stu-id="a0c8e-103">Enable and configure auto charges by channel</span></span>

<span data-ttu-id="a0c8e-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中启用和配置按渠道自动收费。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-104">This topic explains how to enable and configure automatic charges (auto charges) by channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a0c8e-105">概览</span><span class="sxs-lookup"><span data-stu-id="a0c8e-105">Overview</span></span>

<span data-ttu-id="a0c8e-106">有时可能必须为在特定省/直辖市/自治区州（如加利福尼亚州）所有或部分商店销售的一组产品收取回收费获取其他费用。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-106">You might have scenarios where recycling fees or other fees must be applied to a group of products that are sold in all or some stores in a specific state (for example, California).</span></span> <span data-ttu-id="a0c8e-107">可通过 Commerce 中的 **启用按渠道筛选自动收费** 功能指定按渠道自动收费（例如，特定实体店渠道）。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-107">The **Enable filter auto charges by channel** feature in Commerce lets you specify auto charges by channel (for example, a specific brick-and-mortar channel).</span></span> <span data-ttu-id="a0c8e-108">Dynamics 365 Commerce 版本 10.0.10 及更高版本中提供此功能。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-108">This feature is available in Dynamics 365 Commerce version 10.0.10 and later.</span></span>

<span data-ttu-id="a0c8e-109">若要启用和配置按渠道自动收费，必须完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="a0c8e-109">To enable and configure auto charges by channel, you must complete the following tasks:</span></span>

- <span data-ttu-id="a0c8e-110">开启 **启用筛选按渠道自动收费** 功能。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-110">Turn on the **Enable filter auto charges by channel** feature.</span></span>
- <span data-ttu-id="a0c8e-111">配置组织层次结构目的。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-111">Configure the organization hierarchy purpose.</span></span>
- <span data-ttu-id="a0c8e-112">定义按渠道自动收费。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-112">Define auto charges by channel.</span></span>

> [!NOTE]
> <span data-ttu-id="a0c8e-113">只有也开启了高级自动收费功能，**启用筛选按渠道自动收费** 功能才有效。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-113">The **Enable filter auto charges by channel** feature works only if the advanced auto charges feature is also turned on.</span></span> <span data-ttu-id="a0c8e-114">有关如何开启高级自动收费功能的信息，请参阅[全渠道高级自动收费](omni-auto-charges.md)。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-114">For information about how to turn on the advanced auto charges feature, see [Omni-channel advanced auto charges](omni-auto-charges.md).</span></span>

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a><span data-ttu-id="a0c8e-115">开启启用筛选按渠道自动收费功能</span><span class="sxs-lookup"><span data-stu-id="a0c8e-115">Turn on the Enable filter auto charges by channel feature</span></span>

<span data-ttu-id="a0c8e-116">若要在 Commerce 中启用按渠道自动收费，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-116">To enable auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="a0c8e-117">转到 **系统管理员 \> 工作区 \> 功能管理**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-117">Go to **System administrator \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="a0c8e-118">在 **未启用** 选项卡的 **功能名称** 列表中，找到并选中了 **启用筛选按渠道自动收费**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-118">On the **Not enabled** tab, in the **Feature name** list, find and select **Enable filter auto charges by channel**.</span></span>
1. <span data-ttu-id="a0c8e-119">在右下角，选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-119">In the lower-right corner, select **Enable now**.</span></span> <span data-ttu-id="a0c8e-120">此功能在启用之后，将在 **所有** 选项卡中显示。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-120">After the feature has been turned on, it will appear in the list on the **All** tab.</span></span>
1. <span data-ttu-id="a0c8e-121">转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-121">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="a0c8e-122">在左窗格中，找到并选择 **1110**（**全局配置**）作业。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-122">In the left pane, find and select the **1110** (**Global configuration**) job.</span></span>
1. <span data-ttu-id="a0c8e-123">在操作窗格上，选择 **立即运行** 传播配置更改。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-123">On the Action Pane, select **Run now** to propagate the configuration changes.</span></span>

> [!WARNING]
> <span data-ttu-id="a0c8e-124">如果要在已使用 **启用筛选按渠道自动收费** 功能之后将其关闭，**自动收费** 下的 **零售渠道关系** 字段将不再显示，而您将失去所有现有配置。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-124">If you turn off the **Enable filter auto charges by channel** feature after you've already used it, the **Retail channel relation** field under **Auto charges** will no longer appear, and you will lose all existing configurations.</span></span> <span data-ttu-id="a0c8e-125">如果删除 **零售渠道关系** 配置导致自动收费规则重复出现，尝试关闭此功能将失败。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-125">If removal of the **Retail channel relation** configurations will cause auto charges rules to be duplicated, an attempt to turn off the feature will fail.</span></span> <span data-ttu-id="a0c8e-126">关闭此功能之前，请务必检查所有自动收费功能并进行所有必需更改。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-126">Before you turn off the feature, be sure to review all auto charges rules and make any required changes.</span></span>

## <a name="configure-the-organization-hierarchy-purpose"></a><span data-ttu-id="a0c8e-127">配置组织层次结构目的</span><span class="sxs-lookup"><span data-stu-id="a0c8e-127">Configure the organization hierarchy purpose</span></span>

<span data-ttu-id="a0c8e-128">已创建了一个名称为 **零售自动收费** 的新组织层次结构目的，用于管理按渠道自动收费层次结构。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-128">A new organization hierarchy purpose that is named **Retail auto charge** has been created to manage the hierarchy for auto charges by channel.</span></span>

<span data-ttu-id="a0c8e-129">若要在 Commerce 中为组织层次结构目的分配默认层次结构，请执行以下操作。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-129">To assign a default hierarchy to an organization hierarchy purpose in Commerce, follow these steps.</span></span>
        
1. <span data-ttu-id="a0c8e-130">转到 **组织管理 \> 组织 \> 组织层次结构目的**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-130">Go to **Organization administration \> Organizations \> Organization hierarchy purposes**.</span></span>
1. <span data-ttu-id="a0c8e-131">在左窗格中，选择 **零售自动收费**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-131">In the left pane, select **Retail auto charge**.</span></span>
1. <span data-ttu-id="a0c8e-132">在 **分配的层次结构** 下，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-132">Under **Assigned hierarchies**, select **Add**.</span></span>
1. <span data-ttu-id="a0c8e-133">在 **组织层次结构** 对话框中，选择一个组织层次结构（例如，**零售商店(按地区)**），然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-133">In the **Organization hierarchies** dialog box, select an organization hierarchy (for example, **Retail Stores by Region**), and then select **OK**.</span></span>
1. <span data-ttu-id="a0c8e-134">在 **分配的层次结构** 下，选择 **设置为默认值**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-134">Under **Assigned hierarchies**, select **Set as default**.</span></span>
1. <span data-ttu-id="a0c8e-135">转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="a0c8e-136">在左窗格中，找到并选择 **1040**（**产品**）作业。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-136">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="a0c8e-137">在操作窗格上，选择 **立即运行**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-137">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="a0c8e-138">重复前两个步骤运行 **1070**（**渠道配置**）和 **1110**（**全局配置**）作业。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-138">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>

![配置零售自动收费组织层次结构目的](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a><span data-ttu-id="a0c8e-140">定义按渠道自动收费</span><span class="sxs-lookup"><span data-stu-id="a0c8e-140">Define auto charges by channel</span></span>

<span data-ttu-id="a0c8e-141">开启 **启用按渠道筛选自动收费** 功能并配置 **零售自动收费** 组织层次结构目的之后，可以按订单头级别或订单行级别定义按渠道自动收费。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-141">After you've turned on the **Enable filter auto charges by channel** feature and configured the **Retail auto charge** organization hierarchy purpose, auto charges by channel can be defined at either the order header level or the order line level.</span></span>

<span data-ttu-id="a0c8e-142">若要在 Commerce 中定义按渠道自动收费，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-142">To define auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="a0c8e-143">转到 **应收帐款 \> 费用设置 \> 自动费用**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-143">Go to **Accounts receivable \> Charges setup \> Auto charges**.</span></span>
1. <span data-ttu-id="a0c8e-144">在左窗格的 **级别** 字段中，选择 **头** 或 **行**，具体取决于您的业务要求。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-144">In the left pane, in the **Level** field, select either **Header** or **Line**, depending on your business requirements.</span></span>
1. <span data-ttu-id="a0c8e-145">在 **零售渠道代码** 字段中，选择相应渠道代码（例如，**表** 或 **组**）。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-145">In the **Retail channel code** field, select the appropriate channel code (for example, **Table** or **Group**).</span></span> <span data-ttu-id="a0c8e-146">如果使用默认设置 **所有**，则将把费用规则应用于所有渠道。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-146">If the default setting, **All**, is used, charge rules are applied to all channels.</span></span>

    - <span data-ttu-id="a0c8e-147">如果选择 **组**，请确保在 **Retail 和 Commerce \> 渠道设置 \> 费用 \> 零售渠道费用组** 中创建零售渠道费用组。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-147">If you select **Group**, make sure that a retail channel charges group is created at **Retail and Commerce \> Channel setup \> Charges \> Retail channel charge groups**.</span></span>
    - <span data-ttu-id="a0c8e-148">如果选择 **表**，则可在 **零售渠道关系** 字段中选择特定渠道（如 **San Francisco**）。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-148">If you select **Table**, you can select a specific channel (for example, **San Francisco**) in the **Retail channel relation** field.</span></span>

1. <span data-ttu-id="a0c8e-149">转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-149">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="a0c8e-150">在左窗格中，找到并选择 **1040**（**产品**）作业。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-150">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="a0c8e-151">在操作窗格上，选择 **立即运行**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-151">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="a0c8e-152">重复前两个步骤运行 **1070**（**渠道配置**）和 **1110**（**全局配置**）作业。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-152">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>
    
![渠道定义的自动收费](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a><span data-ttu-id="a0c8e-154">示例场景</span><span class="sxs-lookup"><span data-stu-id="a0c8e-154">Example scenario</span></span>

<span data-ttu-id="a0c8e-155">以下示例概述配置产品以便在通过 San Francisco 实体店渠道销售产品时收取回收费需要执行的步骤。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-155">The following example outlines the steps that are required to configure a product so that recycling fees are charged when the product is sold through a San Francisco brick-and-mortar channel.</span></span> <span data-ttu-id="a0c8e-156">此示例还显示自动费用在 Commerce 销售点 (POS) 应用程序中如何显示。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-156">The example also shows how the auto charges appear in the Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="a0c8e-157">组织定义一个名称为 **RECYCLE** 的费用代码，如下图中所示。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-157">The organization defines a charges code that is named **RECYCLE**, as shown in the following illustration.</span></span>

![RECYCLE 费用代码](media/Auto-charges-charge-code.png)

<span data-ttu-id="a0c8e-159">将在行级别创建一项自动费用。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-159">An auto charge is created at the line level.</span></span> <span data-ttu-id="a0c8e-160">它具有以下配置：</span><span class="sxs-lookup"><span data-stu-id="a0c8e-160">It has the following configuration:</span></span>

- <span data-ttu-id="a0c8e-161">**帐户代码** 字段设置为 **所有**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-161">The **Account code** field is set to **All**.</span></span>
- <span data-ttu-id="a0c8e-162">**物料代码** 字段设置为 **表**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-162">The **Item code** field is set to **Table**.</span></span>
- <span data-ttu-id="a0c8e-163">**物料关系** 字段设置为物料 ID **91001**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-163">The **Item relation** field is set to product ID **91001**.</span></span>
- <span data-ttu-id="a0c8e-164">**交货方式代码** 字段设置为 **所有**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-164">The **Mode of delivery code** field is set to **All**.</span></span>
- <span data-ttu-id="a0c8e-165">**零售渠道代码** 字段设置为 **表**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-165">The **Retail channel code** field is set to **Table**.</span></span>
- <span data-ttu-id="a0c8e-166">**零售渠道关系** 字段设置为 **San Francisco** 商店。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-166">The **Retail channel relation** field is set to the **San Francisco** store.</span></span>

<span data-ttu-id="a0c8e-167">将创建一个自动费用行。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-167">An auto charges line is created.</span></span> <span data-ttu-id="a0c8e-168">它具有以下配置：</span><span class="sxs-lookup"><span data-stu-id="a0c8e-168">It has the following configuration:</span></span>

- <span data-ttu-id="a0c8e-169">**货币** 字段设置为 **USD**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-169">The **Currency** field is set to **USD**.</span></span>
- <span data-ttu-id="a0c8e-170">**费用代码** 字段设置为 **RECYCLE**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-170">The **Charges code** field is set to **RECYCLE**.</span></span>
- <span data-ttu-id="a0c8e-171">**类别** 字段将设置为 **固定**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-171">The **Category** field is set to **Fixed**.</span></span>
- <span data-ttu-id="a0c8e-172">**费用** 字段设置为 **$6.25**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-172">The **Charges** field is set to **$6.25**.</span></span>

![行级别自动费用和自动费用行的配置](media/Auto-charges-recyclingfee-line-fee.png)

<span data-ttu-id="a0c8e-174">在 POS 应用程序中，将在 **San Francisco** 商店渠道中创建一个销售订单。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-174">In the POS application, a sales order is created in the **San Francisco** store channel.</span></span> <span data-ttu-id="a0c8e-175">**费用** 行显示回收费为 **$6.25**。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-175">The **Charges** line shows the recycling fee of **$6.25**.</span></span>

<span data-ttu-id="a0c8e-176">可通过在 POS 应用程序中选择 **交易记录选项 \> 费用 \> 管理费用** 查看这笔回收费的费用代码和说明。</span><span class="sxs-lookup"><span data-stu-id="a0c8e-176">By selecting **Transaction options \> Charges \> Manage charges** in the POS application, you can view the charges code and description for the recycling fee.</span></span>

![POS 应用程序中的回收费](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a><span data-ttu-id="a0c8e-178">其他资源</span><span class="sxs-lookup"><span data-stu-id="a0c8e-178">Additional resources</span></span>

[<span data-ttu-id="a0c8e-179">全渠道高级自动费用</span><span class="sxs-lookup"><span data-stu-id="a0c8e-179">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="a0c8e-180">将标头费用按比例分配给匹配的销售行</span><span class="sxs-lookup"><span data-stu-id="a0c8e-180">Prorate header charges to matching sales lines</span></span>](pro-rate-charges-matching-lines.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
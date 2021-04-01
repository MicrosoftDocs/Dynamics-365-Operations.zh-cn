---
title: 使用销售组跟踪销售点 (POS) 中的佣金
description: 零售业中经常由与客户打交道的销售员跟踪销售 — 提供协助、追加销售、交叉销售和处理交易记录。
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7e4820fa02ce66198e1f363ae46f944e3f24146c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243857"
---
# <a name="track-commissions-in-the-point-of-sale-pos-by-using-sales-groups"></a><span data-ttu-id="37cbc-103">使用销售组跟踪销售点 (POS) 中的佣金</span><span class="sxs-lookup"><span data-stu-id="37cbc-103">Track commissions in the point of sale (POS) by using sales groups</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="37cbc-104">零售业中经常由与客户打交道的销售员跟踪销售 — 提供协助、追加销售、交叉销售和处理交易记录。</span><span class="sxs-lookup"><span data-stu-id="37cbc-104">It's a common retail practice to track sales by the associate who worked with the customer by—providing assistance, up-selling, cross-selling, and processing the transaction.</span></span>

<span data-ttu-id="37cbc-105">销售代表跟踪销售是销售员销售能力的一种度量，而收银员销售则是速度和效率的度量。</span><span class="sxs-lookup"><span data-stu-id="37cbc-105">Tracking sales by sales representative is a measure of the associates selling abilities, while sales by cashier is a measure of speed and efficiency.</span></span> <span data-ttu-id="37cbc-106">通常也通过销售代表跟踪的销售来计算佣金或其他激励。</span><span class="sxs-lookup"><span data-stu-id="37cbc-106">Sales tracked by sales representative are also often used to calculate commissions or other incentives.</span></span>

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a><span data-ttu-id="37cbc-107">在 POS 中将工作人员配置为销售代表</span><span class="sxs-lookup"><span data-stu-id="37cbc-107">Configuring a worker to be a sales representative in POS</span></span>

<span data-ttu-id="37cbc-108">将工作人员添加到销售组时，其即可享受佣金，并可以在系统中识别为销售代表。</span><span class="sxs-lookup"><span data-stu-id="37cbc-108">When a worker is added to a sales group, they become eligible for commission and can be identified as a sales representative in the system.</span></span> <span data-ttu-id="37cbc-109">不属于销售组的工作人员没有资格享受佣金，并且不能在销售点 (POS) 应用程序中的作为销售代表列出。</span><span class="sxs-lookup"><span data-stu-id="37cbc-109">A worker who isn't in a sales group isn't eligible for commission and won't be listed as a sales representative in the point of sale (POS) application.</span></span> <span data-ttu-id="37cbc-110">在 POS 中，销售代表列表派生自至少包含一个为商店分配的工作人员的所有销售组。</span><span class="sxs-lookup"><span data-stu-id="37cbc-110">In POS, the list of sales representatives is derived from all sales groups that contain at least one worker assigned to the store.</span></span> <span data-ttu-id="37cbc-111">此列表在 POS 中显示为销售组 ID 和名称的组合（ID：名称）。</span><span class="sxs-lookup"><span data-stu-id="37cbc-111">The list is shown in POS as a combination of Sales group ID and Name (ID : Name).</span></span> <span data-ttu-id="37cbc-112">可以为工作人员配置默认销售组，以便支持满足以下条件的方案：零售商选择自动在 POS 行中设置销售代表。</span><span class="sxs-lookup"><span data-stu-id="37cbc-112">A default sales group can be assigned to workers to support scenarios where the retailer chooses to set the sales representative on POS lines automatically.</span></span> <span data-ttu-id="37cbc-113">用户可从工作人员所属任何销售组进行选择。</span><span class="sxs-lookup"><span data-stu-id="37cbc-113">Users can select from any sales group that the worker is a member of.</span></span>

## <a name="functionality-profile-settings"></a><span data-ttu-id="37cbc-114">功能配置文件设置</span><span class="sxs-lookup"><span data-stu-id="37cbc-114">Functionality profile settings</span></span>

<span data-ttu-id="37cbc-115">商店有一些功能配置文件设置可用于确定 POS 中涉及销售代表的流和流程。</span><span class="sxs-lookup"><span data-stu-id="37cbc-115">There are a number of functionality profile settings for a store that will determine the flow and process in POS that involve sales representatives.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="37cbc-116">配置文件</span><span class="sxs-lookup"><span data-stu-id="37cbc-116">Profile</span></span></th>
<th><span data-ttu-id="37cbc-117">说明</span><span class="sxs-lookup"><span data-stu-id="37cbc-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="37cbc-118">默认为出纳(如果可用)</span><span class="sxs-lookup"><span data-stu-id="37cbc-118">Default to cashier when available</span></span></td>
<td><span data-ttu-id="37cbc-119">如果启用此选项，POS 将自动使用当前收银员的默认销售组填充交易记录行。</span><span class="sxs-lookup"><span data-stu-id="37cbc-119">If this option is enabled, POS will automatically populate transaction lines with the current cashier's default sales group.</span></span> <span data-ttu-id="37cbc-120">如果不为收银员指定默认销售组，则不设置此值。</span><span class="sxs-lookup"><span data-stu-id="37cbc-120">If a cashier doesn't have a default sales group specified, the value won't be set.</span></span> <span data-ttu-id="37cbc-121">用户仍然可以通过使用 POS 按钮网格按钮手动设置销售组。</span><span class="sxs-lookup"><span data-stu-id="37cbc-121">A user could still manually set the sales group by using a POS button grid button.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="37cbc-122">销售代表的提示</span><span class="sxs-lookup"><span data-stu-id="37cbc-122">Prompt for sales representative</span></span></td>
<td><span data-ttu-id="37cbc-123">此选项包含三个可能的值：</span><span class="sxs-lookup"><span data-stu-id="37cbc-123">This option has three possible values:</span></span>
<ul>
<li><span data-ttu-id="37cbc-124"><strong>否</strong> – 如果选择此选项，则不提示用户选择销售组。</span><span class="sxs-lookup"><span data-stu-id="37cbc-124"><strong>No</strong> – If this option is selected, the user won't be prompted to select a sales group.</span></span> <span data-ttu-id="37cbc-125">仍然可以通过使用收银员的默认销售组设置此值，或通过使用 POS 按钮网格按钮手动设置。</span><span class="sxs-lookup"><span data-stu-id="37cbc-125">The value could still be set by using a cashier's default Sales group or manually by using a POS button grid button.</span></span></li>
<li><span data-ttu-id="37cbc-126"><strong>交易记录开始</strong> – 如果选择此选项，并且不启用<strong>默认为收银员</strong>选项或当前收银员无默认销售组，将在每个交易记录开始时提示用户选择销售组。</span><span class="sxs-lookup"><span data-stu-id="37cbc-126"><strong>Start of transaction</strong> – If this option is selected, and either the <strong>Default to cashier</strong> option isn't enabled or the current cashier doesn't have a default sales group, the user will be prompted to select a sales group at the beginning of each transaction.</span></span> <span data-ttu-id="37cbc-127">从该提示选择销售组将把所有后续行默认设置为所选销售组。</span><span class="sxs-lookup"><span data-stu-id="37cbc-127">Selecting a sales group from this prompt will default all subsequent lines to the selected sales group.</span></span> <span data-ttu-id="37cbc-128">用户仍然可以通过使用 POS 按钮网格按钮手动设置销售组。</span><span class="sxs-lookup"><span data-stu-id="37cbc-128">A user could still manually set the sales group by using a POS button grid button.</span></span></li>
<li><span data-ttu-id="37cbc-129"><strong>对于每行</strong> – 如果选择此选项，并且不启用<strong>默认为收银员</strong>选项或当前收银员无默认销售组，将在添加每行后提示用户选择销售组。</span><span class="sxs-lookup"><span data-stu-id="37cbc-129"><strong>For each line</strong> – If this option is selected, and either the <strong>Default to cashier</strong> option isn't enabled or the current cashier doesn't have a default sales group, the user will be prompted to select a sales group after adding each line.</span></span> <span data-ttu-id="37cbc-130">用户仍然可以通过使用 POS 按钮网格按钮手动设置销售组。</span><span class="sxs-lookup"><span data-stu-id="37cbc-130">A user could still manually set the Sales group by using a POS button grid button.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="37cbc-131">需要</span><span class="sxs-lookup"><span data-stu-id="37cbc-131">Require</span></span></td>
<td><span data-ttu-id="37cbc-132">此选项仅适用于 POS 配置为提示需要指定销售代表时。</span><span class="sxs-lookup"><span data-stu-id="37cbc-132">This option is only applicable when POS is configured to prompt for a sales representative.</span></span> <span data-ttu-id="37cbc-133">如果启用，将要求用户先选择销售组，才能继续操作。</span><span class="sxs-lookup"><span data-stu-id="37cbc-133">If enabled, the user will be required to choose a sales group before continuing.</span></span> <span data-ttu-id="37cbc-134">否则，将提示用户，但是可以取消并在不进行选择的情况下继续操作。</span><span class="sxs-lookup"><span data-stu-id="37cbc-134">Otherwise, the user will be prompted, but can cancel and continue without making a selection.</span></span> <span data-ttu-id="37cbc-135">添加行之后，拥有足够权限的用户仍然可以从行中删除销售组。</span><span class="sxs-lookup"><span data-stu-id="37cbc-135">After the line is added, a user with sufficient permissions could still remove the sales group from the line.</span></span> <span data-ttu-id="37cbc-136">此方案中不实施“需要销售代表”。</span><span class="sxs-lookup"><span data-stu-id="37cbc-136">"Require sales representative" is not enforced in this situation.</span></span></td>
</tr>
</tbody>
</table>

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a><span data-ttu-id="37cbc-137">在 POS 交易记录屏幕中显示销售代表信息</span><span class="sxs-lookup"><span data-stu-id="37cbc-137">Displaying the Sales representative information on the POS transactions screen</span></span>

<span data-ttu-id="37cbc-138">可使用屏幕布局设计器和为商店、收银机或工作人员指定的屏幕布局配置 POS 交易记录屏幕布局和内容。</span><span class="sxs-lookup"><span data-stu-id="37cbc-138">The POS transaction screen layout and contents are configurable using the screen layout designer and assigned screen layouts to stores, registers, or workers.</span></span> <span data-ttu-id="37cbc-139">可将 **销售代表** 字段添加到“收据”窗格的“行”选项卡。</span><span class="sxs-lookup"><span data-stu-id="37cbc-139">The **Sales representative** field can be added to the Lines tab of the Receipt pane.</span></span>  <span data-ttu-id="37cbc-140">这将为交易记录屏幕中的各行显示指定销售组的 ID。</span><span class="sxs-lookup"><span data-stu-id="37cbc-140">This will display the ID of the specified Sales group for each line on the transaction screen.</span></span>

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a><span data-ttu-id="37cbc-141">向 POS 按钮网格添加销售代表操作</span><span class="sxs-lookup"><span data-stu-id="37cbc-141">Adding Sales representative operations to POS button grids</span></span>

<span data-ttu-id="37cbc-142">POS 允许用户配置按钮网格，按钮网格包含在屏幕布局中，用于访问 POS 操作。</span><span class="sxs-lookup"><span data-stu-id="37cbc-142">POS allows users to configure button grids, which are included in screen layouts to provide access to POS operations.</span></span> <span data-ttu-id="37cbc-143">可将以下 POS 操作分配给属于销售代表的按钮网格按钮。</span><span class="sxs-lookup"><span data-stu-id="37cbc-143">The following POS operations can be assigned to button grid buttons that pertain to Sales representatives.</span></span>

| <span data-ttu-id="37cbc-144">工序</span><span class="sxs-lookup"><span data-stu-id="37cbc-144">Operation</span></span>                                 | <span data-ttu-id="37cbc-145">说明</span><span class="sxs-lookup"><span data-stu-id="37cbc-145">Description</span></span> |
|-------------------------------------------|-------------|
| <span data-ttu-id="37cbc-146">设置行上的销售代表</span><span class="sxs-lookup"><span data-stu-id="37cbc-146">Set sales representative on line</span></span>          | <span data-ttu-id="37cbc-147">此 POS 操作显示符合商店条件的销售组（ID：名称）的列表。</span><span class="sxs-lookup"><span data-stu-id="37cbc-147">This POS operation displays a list of eligible Sales groups (ID : Name) for the store.</span></span> <span data-ttu-id="37cbc-148">从此列表中选择一个销售组将在当前交易记录行中设置值。</span><span class="sxs-lookup"><span data-stu-id="37cbc-148">Selecting a Sales group from this list will set the value on the current transaction line.</span></span> |
| <span data-ttu-id="37cbc-149">清除行上的销售代表</span><span class="sxs-lookup"><span data-stu-id="37cbc-149">Clear sales representative on line</span></span>        | <span data-ttu-id="37cbc-150">此 POS 操作从当前交易记录行删除当前销售组值。</span><span class="sxs-lookup"><span data-stu-id="37cbc-150">This POS operation removes the current Sales group value from the current transaction line.</span></span> |
| <span data-ttu-id="37cbc-151">设置交易记录上的销售代表</span><span class="sxs-lookup"><span data-stu-id="37cbc-151">Set sales representative on transaction</span></span>   | <span data-ttu-id="37cbc-152">此 POS 操作显示符合商店条件的销售组（ID：名称）的列表。</span><span class="sxs-lookup"><span data-stu-id="37cbc-152">This POS operation displays a list of eligible Sales groups (ID : Name) for the store.</span></span> <span data-ttu-id="37cbc-153">从此列表中选择一个销售组将在当前交易记录中设置默认值。</span><span class="sxs-lookup"><span data-stu-id="37cbc-153">Selecting a Sales group from this list will set the default value on the current transaction.</span></span> <span data-ttu-id="37cbc-154">将设置未为其分配销售组的任何现有行，以及以后添加的任何行。</span><span class="sxs-lookup"><span data-stu-id="37cbc-154">Any existing lines without a sales group assigned will be set, as well as any subsequently added lines.</span></span> |
| <span data-ttu-id="37cbc-155">清除交易记录上的销售代表</span><span class="sxs-lookup"><span data-stu-id="37cbc-155">Clear sales representative on transaction</span></span> | <span data-ttu-id="37cbc-156">此 POS 操作从当前交易记录删除当前默认销售组值。</span><span class="sxs-lookup"><span data-stu-id="37cbc-156">This POS operation removes the current default Sales group value from the current transaction.</span></span> <span data-ttu-id="37cbc-157">不影响交易记录中已有的任何行。</span><span class="sxs-lookup"><span data-stu-id="37cbc-157">It does not impact any lines already existing in the transaction.</span></span> |

## <a name="calculating-commissions"></a><span data-ttu-id="37cbc-158">计算佣金</span><span class="sxs-lookup"><span data-stu-id="37cbc-158">Calculating commissions</span></span>

<span data-ttu-id="37cbc-159">对账单过帐或销售订单过帐时，将为指定销售组中的工作人员计算佣金。</span><span class="sxs-lookup"><span data-stu-id="37cbc-159">Commission is calculated for the workers in the specified sales groups at the time of statement posting or sales order posting.</span></span> <span data-ttu-id="37cbc-160">将根据交易记录中客户和/或产品的销售组和关联佣金计算设置中定义的工作人员佣金份额，确定佣金金额。</span><span class="sxs-lookup"><span data-stu-id="37cbc-160">The commission amount is determined based on the worker's commission share, as defined in the sales group and the associated commission calculation settings for the customer and/or products on the transaction.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
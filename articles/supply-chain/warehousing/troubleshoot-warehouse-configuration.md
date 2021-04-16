---
title: 仓库配置疑难解答
description: 此主题介绍如何解决配置 Microsoft Dynamics 365 Supply Chain Management 时可能遇到的常见问题。
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1dbd947f0740d22e0f79e6d5c272beb64715c8a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814384"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="76877-103">仓库配置疑难解答</span><span class="sxs-lookup"><span data-stu-id="76877-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76877-104">此主题介绍如何解决配置 Microsoft Dynamics 365 Supply Chain Management 时可能遇到的常见问题。</span><span class="sxs-lookup"><span data-stu-id="76877-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="76877-105">我收到以下错误消息：“牌照或位置无效。”</span><span class="sxs-lookup"><span data-stu-id="76877-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="76877-106">问题描述</span><span class="sxs-lookup"><span data-stu-id="76877-106">Issue description</span></span>

<span data-ttu-id="76877-107">当您扫描牌照 ID 或位置时，会收到此错误消息。</span><span class="sxs-lookup"><span data-stu-id="76877-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="76877-108">解决问题</span><span class="sxs-lookup"><span data-stu-id="76877-108">Issue resolution</span></span>

<span data-ttu-id="76877-109">请确保牌照 ID 未在别处保留。</span><span class="sxs-lookup"><span data-stu-id="76877-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="76877-110">当用户在仓库管理移动应用中扫描的值既是有效库位又是有效牌照 ID 时，过去常会发生此问题。</span><span class="sxs-lookup"><span data-stu-id="76877-110">This issue used to occur when the value that a user scanned in the Warehouse Management mobile app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="76877-111">但是，此问题已在版本 10.0.11 中解决。</span><span class="sxs-lookup"><span data-stu-id="76877-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="76877-112">我收到以下错误消息：“必须为此位置指定牌照。”</span><span class="sxs-lookup"><span data-stu-id="76877-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="76877-113">问题描述</span><span class="sxs-lookup"><span data-stu-id="76877-113">Issue description</span></span>

<span data-ttu-id="76877-114">如果您使用启用了高级仓库管理 (WMS) 的仓库创建转移单，然后在工作完成后尝试确认装运，这时会收到此错误消息。</span><span class="sxs-lookup"><span data-stu-id="76877-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="76877-115">解决问题</span><span class="sxs-lookup"><span data-stu-id="76877-115">Issue resolution</span></span>

<span data-ttu-id="76877-116">**默认收货位置** 字段在“来源”仓库的中转仓库中是空白的。</span><span class="sxs-lookup"><span data-stu-id="76877-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="76877-117">要解决此问题，请在中转仓库中指定默认收货位置。</span><span class="sxs-lookup"><span data-stu-id="76877-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="76877-118">请确保此位置是由牌照控制的。</span><span class="sxs-lookup"><span data-stu-id="76877-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="76877-119">我收到以下错误消息：“您无法为库存状态更改创建工作模板行，因为工作类型无效。</span><span class="sxs-lookup"><span data-stu-id="76877-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="76877-120">请选择其他工作类型。”</span><span class="sxs-lookup"><span data-stu-id="76877-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="76877-121">问题描述</span><span class="sxs-lookup"><span data-stu-id="76877-121">Issue description</span></span>

<span data-ttu-id="76877-122">对于工作模板，您无法在 **工作模板详细信息** 部分的 **工作类型** 列中选择 *库存状态更改*。</span><span class="sxs-lookup"><span data-stu-id="76877-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="76877-123">解决问题</span><span class="sxs-lookup"><span data-stu-id="76877-123">Issue resolution</span></span>

<span data-ttu-id="76877-124">此为有意行为。</span><span class="sxs-lookup"><span data-stu-id="76877-124">This behavior is by design.</span></span> <span data-ttu-id="76877-125">*库存状态更改* 工作类型仅由系统流程使用。</span><span class="sxs-lookup"><span data-stu-id="76877-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="76877-126">无法进行配置。</span><span class="sxs-lookup"><span data-stu-id="76877-126">It can't be configured.</span></span> <span data-ttu-id="76877-127">由于工作类型列表固定为枚举，因此无法将多余条目从 **工作类型** 下拉菜单中筛选掉。</span><span class="sxs-lookup"><span data-stu-id="76877-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="76877-128">我收到以下错误消息：“数量对于单位 1% 无效。”</span><span class="sxs-lookup"><span data-stu-id="76877-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="76877-129">问题描述</span><span class="sxs-lookup"><span data-stu-id="76877-129">Issue description</span></span>

<span data-ttu-id="76877-130">如果存在一个位置有多个牌照的领料工作，此数量对于 *个* 单位将无效。</span><span class="sxs-lookup"><span data-stu-id="76877-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="76877-131">解决问题</span><span class="sxs-lookup"><span data-stu-id="76877-131">Issue resolution</span></span>

<span data-ttu-id="76877-132">请验证已发布产品或产品变型上的 **单位序列组 ID** 和 **单位转换** 字段是否设置正确。</span><span class="sxs-lookup"><span data-stu-id="76877-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="76877-133">请注意，此错误消息在版本 10.0.15 中已得到改进（请参阅 [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)）。</span><span class="sxs-lookup"><span data-stu-id="76877-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="76877-134">新错误消息是“数量无效。</span><span class="sxs-lookup"><span data-stu-id="76877-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="76877-135">预期为 %1 %2。”</span><span class="sxs-lookup"><span data-stu-id="76877-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="76877-136">在销售订单放置工作的位置指令中，多 SKU 选项不会评估多个位置指令操作。</span><span class="sxs-lookup"><span data-stu-id="76877-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="76877-137">问题描述</span><span class="sxs-lookup"><span data-stu-id="76877-137">Issue description</span></span>

<span data-ttu-id="76877-138">选择了 **多 SKU** 选项时，*销售订单* 工作订单类型和 *放置* 工作类型的位置指令不会评估多个位置指令操作。</span><span class="sxs-lookup"><span data-stu-id="76877-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="76877-139">只会评估第一个位置指令操作。</span><span class="sxs-lookup"><span data-stu-id="76877-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="76877-140">解决问题</span><span class="sxs-lookup"><span data-stu-id="76877-140">Issue resolution</span></span>

<span data-ttu-id="76877-141">一项新功能 *评估多 SKU 位置指令的所有操作* 已在版本 10.0.15 中添加（请参阅 [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)）。</span><span class="sxs-lookup"><span data-stu-id="76877-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="76877-142">此功能可评估多 SKU 位置指令的所有操作。</span><span class="sxs-lookup"><span data-stu-id="76877-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="76877-143">如果您需要此功能，请使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)将它打开。</span><span class="sxs-lookup"><span data-stu-id="76877-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-management-mobile-app-to-do-partial-picking"></a><span data-ttu-id="76877-144">我无法使用仓库管理移动应用进行部分领料。</span><span class="sxs-lookup"><span data-stu-id="76877-144">I can't use the Warehouse Management mobile app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="76877-145">问题描述</span><span class="sxs-lookup"><span data-stu-id="76877-145">Issue description</span></span>

<span data-ttu-id="76877-146">对于销售订单和转移单，不能跳过物料，进行部分领料。</span><span class="sxs-lookup"><span data-stu-id="76877-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="76877-147">解决问题</span><span class="sxs-lookup"><span data-stu-id="76877-147">Issue resolution</span></span>

<span data-ttu-id="76877-148">在 **移动设备菜单项** 页上，为设置为处理销售订单或转移订单的每个菜单项，将 **常规** 快速选项卡上的 **允许拆分工作** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="76877-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="76877-149">如何对部分数量工作进行库存状态更改？</span><span class="sxs-lookup"><span data-stu-id="76877-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="76877-150">问题描述</span><span class="sxs-lookup"><span data-stu-id="76877-150">Issue description</span></span>

<span data-ttu-id="76877-151">您要对批处理的部分数量进行库存状态更改。</span><span class="sxs-lookup"><span data-stu-id="76877-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="76877-152">解决问题</span><span class="sxs-lookup"><span data-stu-id="76877-152">Issue resolution</span></span>

<span data-ttu-id="76877-153">若要使工作人员能够进行此更改，您可以为仓库管理移动应用创建菜单项。</span><span class="sxs-lookup"><span data-stu-id="76877-153">To enable workers to make this change, you can create a menu item for the Warehouse Management mobile app.</span></span> <span data-ttu-id="76877-154">在 **移动设备菜单项** 页上，创建（或编辑）具有以下设置的菜单项：</span><span class="sxs-lookup"><span data-stu-id="76877-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="76877-155">\**模式：\*\*\*工作*</span><span class="sxs-lookup"><span data-stu-id="76877-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="76877-156">**使用现有工作**：*否*</span><span class="sxs-lookup"><span data-stu-id="76877-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="76877-157">**工作创建流程**：*移动*</span><span class="sxs-lookup"><span data-stu-id="76877-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="76877-158">**显示库存状态**：*是*</span><span class="sxs-lookup"><span data-stu-id="76877-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="76877-159">您可以根据需要在页面上设置其他字段。</span><span class="sxs-lookup"><span data-stu-id="76877-159">You can set other fields on the page as you require.</span></span>

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a><span data-ttu-id="76877-160">位置模板的码头管理配置文件未阻止库存类型的混合。</span><span class="sxs-lookup"><span data-stu-id="76877-160">The dock management profile of a location profile is not preventing inventory types from being mixed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="76877-161">问题描述</span><span class="sxs-lookup"><span data-stu-id="76877-161">Issue description</span></span>

<span data-ttu-id="76877-162">您正在使用 *装运合并政策*。</span><span class="sxs-lookup"><span data-stu-id="76877-162">You are using *shipment consolidation policies*.</span></span> <span data-ttu-id="76877-163">您已经为 *位置模板* 设置了 *码头管理配置文件*，但是在创建工作时，库存类型在最终位置混合。</span><span class="sxs-lookup"><span data-stu-id="76877-163">You have set up a *dock management profile* for a *location profile*, but when work is created, the inventory types are mixed at the final location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="76877-164">解决问题</span><span class="sxs-lookup"><span data-stu-id="76877-164">Issue resolution</span></span>

<span data-ttu-id="76877-165">码头管理配置文件需要工作提前拆分。</span><span class="sxs-lookup"><span data-stu-id="76877-165">Dock management profiles require work to be split up front.</span></span> <span data-ttu-id="76877-166">换言之，码头管理配置文件预期工作标题不会有多个放置位置。</span><span class="sxs-lookup"><span data-stu-id="76877-166">In other words, the dock management profile expects that a work header won't have multiple put locations.</span></span>

<span data-ttu-id="76877-167">要让码头管理配置文件有效地管理库存的混合，必须设置工作标题分解。</span><span class="sxs-lookup"><span data-stu-id="76877-167">For the dock management profile to effectively manage the mixing of inventory, a work header break must be set up.</span></span>

<span data-ttu-id="76877-168">在此示例中，我们配置了码头管理配置文件，以将 **不应混合的库存类型** 设置为 *装运 ID*，然后我们将为其设置工作标题分解：</span><span class="sxs-lookup"><span data-stu-id="76877-168">In this example our dock management profile is configured such that **Inventory types that should not be mixed** is set to *Shipment ID*, and we'll set up a work header break for it:</span></span>

1. <span data-ttu-id="76877-169">转到 **仓库管理 \> 设置 \> 工作 \> 工作模板**。</span><span class="sxs-lookup"><span data-stu-id="76877-169">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="76877-170">选择要编辑的 **工作订单类型**（例如，*采购订单*）。</span><span class="sxs-lookup"><span data-stu-id="76877-170">Select the **Work order type** to edit (for example, *Purchase orders*).</span></span>
1. <span data-ttu-id="76877-171">选择要编辑的工作模板。</span><span class="sxs-lookup"><span data-stu-id="76877-171">Select the work template to edit.</span></span>
1. <span data-ttu-id="76877-172">在操作窗格上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="76877-172">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="76877-173">打开 **排序** 选项卡，添加具有以下设置的行：</span><span class="sxs-lookup"><span data-stu-id="76877-173">Open the **Sorting** tab and add a row with the following settings:</span></span>
    - <span data-ttu-id="76877-174">**表** - *临时工作交易*</span><span class="sxs-lookup"><span data-stu-id="76877-174">**Table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="76877-175">**派生表** - *临时工作交易*</span><span class="sxs-lookup"><span data-stu-id="76877-175">**Derived table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="76877-176">**字段** - *装运 ID*</span><span class="sxs-lookup"><span data-stu-id="76877-176">**Field** - *Shipment ID*</span></span>
1. <span data-ttu-id="76877-177">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="76877-177">Select **OK**.</span></span>
1. <span data-ttu-id="76877-178">您将返回 **工作模板** 页。</span><span class="sxs-lookup"><span data-stu-id="76877-178">You return to the **Work templates** page.</span></span> <span data-ttu-id="76877-179">在“操作窗格”中选择 **工作标题中断**。</span><span class="sxs-lookup"><span data-stu-id="76877-179">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="76877-180">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="76877-180">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="76877-181">选中与 **字段名称** 装 *运 ID* 关联的复选框。</span><span class="sxs-lookup"><span data-stu-id="76877-181">Select the check box associated with the **Field name** *Shipment ID*.</span></span>
1. <span data-ttu-id="76877-182">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="76877-182">On the Action Pane, select **Save**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: 自动分配费用
description: Microsoft Dynamics 365 Supply Chain Management 中的费用功能帮助您自动将费用分配给采购订单或销售订单。
author: dasani-madipalli
manager: tfehr
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 8067285237127bd43e8ff24166a15506cc0426f4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983158"
---
# <a name="automatic-allocation-of-charges"></a><span data-ttu-id="d611d-103">自动分配费用</span><span class="sxs-lookup"><span data-stu-id="d611d-103">Automatic allocation of charges</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d611d-104">基于您与之合作的客户或所销售的物料，您可能需要应用特定的附加费用。</span><span class="sxs-lookup"><span data-stu-id="d611d-104">Based on the customer that you're working with or the item that you're selling, you might want to apply specific additional charges.</span></span> <span data-ttu-id="d611d-105">Microsoft Dynamics 365 Supply Chain Management 中的 *费用* 功能帮助您自动将费用分配给采购订单或销售订单。</span><span class="sxs-lookup"><span data-stu-id="d611d-105">The *charges* feature in Microsoft Dynamics 365 Supply Chain Management helps you automatically allocate charges to purchase orders or sales orders.</span></span>

<span data-ttu-id="d611d-106">在创建销售订单或采购订单时将自动应用自动费用。</span><span class="sxs-lookup"><span data-stu-id="d611d-106">Automatic charges, or auto charges, are automatically applied when you create a sales order or a purchase order.</span></span> <span data-ttu-id="d611d-107">您可以定义特定供应商、客户、供应商组或物料的自动费用。</span><span class="sxs-lookup"><span data-stu-id="d611d-107">You can define auto charges for specific vendors, customers, groups of vendors, or items.</span></span> <span data-ttu-id="d611d-108">还可以定义适用于所有供应商、客户或物料的自动费用。</span><span class="sxs-lookup"><span data-stu-id="d611d-108">You can also define auto charges that apply to all vendors, customers, or items.</span></span>

## <a name="set-up-charges-codes"></a><span data-ttu-id="d611d-109">设置费用代码</span><span class="sxs-lookup"><span data-stu-id="d611d-109">Set up charges codes</span></span>

<span data-ttu-id="d611d-110">若要分配费用，您必须首先定义费用代码。</span><span class="sxs-lookup"><span data-stu-id="d611d-110">To allocate charges, you must first define charges codes.</span></span>

1. <span data-ttu-id="d611d-111">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="d611d-111">Follow one of these steps:</span></span>

    - <span data-ttu-id="d611d-112">对于采购订单：转到 **应付帐款 \> 费用设置 \> 费用代码**。</span><span class="sxs-lookup"><span data-stu-id="d611d-112">For purchase orders: Go to **Accounts payable \> Charges setup \> Charges code**.</span></span>
    - <span data-ttu-id="d611d-113">对于销售订单：转到 **应收帐款 \> 费用设置 \> 费用代码**。</span><span class="sxs-lookup"><span data-stu-id="d611d-113">For sales orders: Go to **Accounts receivable \> Charges setup \> Charges code**.</span></span>

1. <span data-ttu-id="d611d-114">在“操作”窗格中，选择 **新建** 以创建费用代码。</span><span class="sxs-lookup"><span data-stu-id="d611d-114">On the Action Pane, select **New** to create a charges code.</span></span>
1. <span data-ttu-id="d611d-115">在新记录的标题中，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="d611d-115">In the header of the new record, set the following fields:</span></span>

    - <span data-ttu-id="d611d-116">**费用代码** – 输入费用的代码。</span><span class="sxs-lookup"><span data-stu-id="d611d-116">**Charges code** – Enter a code for the charges.</span></span>
    - <span data-ttu-id="d611d-117">**描述** – 输入费用的描述。</span><span class="sxs-lookup"><span data-stu-id="d611d-117">**Description** – Enter a description of the charges.</span></span>
    - <span data-ttu-id="d611d-118">**物料销售税组** – 选择一个物料销售税组（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="d611d-118">**Item sales tax group** – Select an item sales tax group, if applicable.</span></span>
    - <span data-ttu-id="d611d-119">**按比例分配** – 如果您想要按比例分配费用，将此选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="d611d-119">**Prorate** – Set this option to *Yes* if you want to prorate your charges.</span></span> <span data-ttu-id="d611d-120">此选项仅适用于销售订单。</span><span class="sxs-lookup"><span data-stu-id="d611d-120">This option is available only for sales orders.</span></span>
    - <span data-ttu-id="d611d-121">**最大金额** – 输入费用代码允许的最大金额。</span><span class="sxs-lookup"><span data-stu-id="d611d-121">**Maximum amount** – Enter the maximum amount that is allowed for the charges code.</span></span> <span data-ttu-id="d611d-122">此字段用于验证供应商发票的费用。</span><span class="sxs-lookup"><span data-stu-id="d611d-122">This field is used to validate charges for vendor invoices.</span></span> <span data-ttu-id="d611d-123">仅适用于采购订单。</span><span class="sxs-lookup"><span data-stu-id="d611d-123">It's available only for purchase orders.</span></span>

        > [!NOTE]
        > <span data-ttu-id="d611d-124">若要打开用于验证采购订单费用的功能，请转到 **应付帐款 \> 设置 \> 应付帐款参数**。</span><span class="sxs-lookup"><span data-stu-id="d611d-124">To turn on the functionality for validating charges for purchase orders, go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span> <span data-ttu-id="d611d-125">在 **发票验证** 快速选项卡上的 **发票验证** 部分中，将 **启用发票匹配验证** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="d611d-125">On the **Invoice validation** FastTab, in the **Invoice validation** section, set the **Enable invoice matching validation** option to *Yes*.</span></span>

1. <span data-ttu-id="d611d-126">**过帐** 快速选项卡包括 **借方** 和 **贷方** 部分。</span><span class="sxs-lookup"><span data-stu-id="d611d-126">The **Posting** FastTab includes **Debit** and **Credit** sections.</span></span> <span data-ttu-id="d611d-127">设置以下字段，具体取决于要将费用过帐到的分类帐：</span><span class="sxs-lookup"><span data-stu-id="d611d-127">Set the following fields, depending on the ledger that you want to post the charges to:</span></span>

    - <span data-ttu-id="d611d-128">**类型** – 选择要过帐到的帐户类型（*分类帐*、*客户* 或 *物料*）。</span><span class="sxs-lookup"><span data-stu-id="d611d-128">**Type** – Select the type of account that you're posting to (*Ledger*, *Customer*, or *Item*).</span></span>
    - <span data-ttu-id="d611d-129">**过帐** – 选择要创建的过帐类型（例如 *代理人费用* 或 *客户结算*）。</span><span class="sxs-lookup"><span data-stu-id="d611d-129">**Posting** – Select the type of postings to create (such as *Broker fee* or *Customer settlement*).</span></span>
    - <span data-ttu-id="d611d-130">**帐户** – 选择要为其过帐的帐户。</span><span class="sxs-lookup"><span data-stu-id="d611d-130">**Account** – Select the account to post the charge for.</span></span>

1. <span data-ttu-id="d611d-131">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="d611d-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-charge-groups"></a><span data-ttu-id="d611d-132">创建费用组</span><span class="sxs-lookup"><span data-stu-id="d611d-132">Create charge groups</span></span>

<span data-ttu-id="d611d-133">费用组自动将特定费用分配给一组客户或供应商。</span><span class="sxs-lookup"><span data-stu-id="d611d-133">Charge groups automatically allocate specific charges to a group of customers or vendors.</span></span> <span data-ttu-id="d611d-134">以下子部分介绍了如何创建和分配这些费用组。</span><span class="sxs-lookup"><span data-stu-id="d611d-134">The following subsections describe how to create and assign these charge groups.</span></span>

### <a name="charge-groups-for-purchase-orders"></a><span data-ttu-id="d611d-135">采购订单的费用组</span><span class="sxs-lookup"><span data-stu-id="d611d-135">Charge groups for purchase orders</span></span>

<span data-ttu-id="d611d-136">若要创建采购订单的费用组，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d611d-136">To create charge groups for purchase orders, follow these steps.</span></span>

1. <span data-ttu-id="d611d-137">转到 **应付帐款 \> 费用设置 \> 供应商费用组**。</span><span class="sxs-lookup"><span data-stu-id="d611d-137">Go to **Accounts payable \> Charges setup \> Vendor charges group**.</span></span>
1. <span data-ttu-id="d611d-138">在“操作”窗格上，选择 **新建** 以向网格添加一行，然后设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="d611d-138">On the Action Pane, select **New** to add a row to the grid, and then set the following fields:</span></span>

    - <span data-ttu-id="d611d-139">**费用组** – 输入费用组的名称。</span><span class="sxs-lookup"><span data-stu-id="d611d-139">**Charges group** – Enter the name of the charge group.</span></span>
    - <span data-ttu-id="d611d-140">**描述** – 输入费用组的描述。</span><span class="sxs-lookup"><span data-stu-id="d611d-140">**Description** – Enter a description of the charge group.</span></span>

1. <span data-ttu-id="d611d-141">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="d611d-141">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="d611d-142">转到 **应付帐款 \> 供应商 \> 所有供应商**，然后打开现有供应商或创建新供应商。</span><span class="sxs-lookup"><span data-stu-id="d611d-142">Go to **Accounts payable \> Vendors \> All vendors**, and either open an existing vendor or create a new vendor.</span></span>
1. <span data-ttu-id="d611d-143">在 **采购订单默认值** 快速选项卡上的 **采购订单** 部分中，将 **费用组** 字段设置为您刚创建的费用组。</span><span class="sxs-lookup"><span data-stu-id="d611d-143">On the **Purchase order defaults** FastTab, in the **Purchase order** section, set the **Charges group** field to the charge group that you just created.</span></span>

### <a name="charge-groups-for-sales-orders"></a><span data-ttu-id="d611d-144">销售订单的费用组</span><span class="sxs-lookup"><span data-stu-id="d611d-144">Charge groups for sales orders</span></span>

<span data-ttu-id="d611d-145">若要创建销售订单的费用组，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d611d-145">To create charge groups for sales orders, follow these steps.</span></span>

1. <span data-ttu-id="d611d-146">转到 **应收帐款 \> 费用设置 \> 客户费用组**。</span><span class="sxs-lookup"><span data-stu-id="d611d-146">Go to **Accounts receivable \> Charges setup \> Customer charge groups**.</span></span>
1. <span data-ttu-id="d611d-147">在“操作”窗格上，选择 **新建** 以向网格添加一行，然后设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="d611d-147">On the Action Pane, select **New** to add a row to the grid, and then set the following fields:</span></span>

    - <span data-ttu-id="d611d-148">**费用组** – 输入费用组的名称。</span><span class="sxs-lookup"><span data-stu-id="d611d-148">**Charges group** – Enter the name of the charge group.</span></span>
    - <span data-ttu-id="d611d-149">**描述** – 输入费用组的描述。</span><span class="sxs-lookup"><span data-stu-id="d611d-149">**Description** – Enter a description of the charge group.</span></span>

1. <span data-ttu-id="d611d-150">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="d611d-150">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="d611d-151">转到 **应收帐款 \> 客户 \> 所有客户**，或者打开现有客户或创建新客户。</span><span class="sxs-lookup"><span data-stu-id="d611d-151">Go to **Accounts receivable \> Customers \> All customers**, and either open an existing customer or create a new customer.</span></span>
1. <span data-ttu-id="d611d-152">在 **采购订单默认值** 快速选项卡上的 **销售订单** 部分中，将 **费用组** 字段设置为您刚创建的费用组。</span><span class="sxs-lookup"><span data-stu-id="d611d-152">On the **Purchase order defaults** FastTab, in the **Sales order** section, set the **Charges group** field to the charge group that you just created.</span></span>

## <a name="define-auto-charges"></a><span data-ttu-id="d611d-153">定义自动费用</span><span class="sxs-lookup"><span data-stu-id="d611d-153">Define auto charges</span></span>

<span data-ttu-id="d611d-154">在设置费用代码后，请按照以下步骤定义自动费用。</span><span class="sxs-lookup"><span data-stu-id="d611d-154">After your charges codes are set up, follow these steps to define the auto charges.</span></span>

1. <span data-ttu-id="d611d-155">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="d611d-155">Follow one of these steps:</span></span>

    - <span data-ttu-id="d611d-156">对于采购订单：转到 **采购 \> 设置 \> 费用 \> 自动费用**。</span><span class="sxs-lookup"><span data-stu-id="d611d-156">For purchase orders: Go to **Procurement and sourcing \> Setup \> Charges \> Automatic charges**.</span></span>
    - <span data-ttu-id="d611d-157">对于销售订单：转到 **应收帐款 \> 设置 \> 费用设置 \> 自动费用**。</span><span class="sxs-lookup"><span data-stu-id="d611d-157">For sales orders: Go to **Accounts receivable \> Setup \> Charges setup \> Auto charges**.</span></span>

1. <span data-ttu-id="d611d-158">在列表窗格的 **级别** 字段中，选择您的自动费用适用的级别：</span><span class="sxs-lookup"><span data-stu-id="d611d-158">In the list pane, in the **Level** field, select the level where your auto charge applies:</span></span>

    - <span data-ttu-id="d611d-159">*主* – 将费用应用到订单头。</span><span class="sxs-lookup"><span data-stu-id="d611d-159">*Main* – Apply charges to the order header.</span></span>
    - <span data-ttu-id="d611d-160">*行* – 将费用应用到订单行。</span><span class="sxs-lookup"><span data-stu-id="d611d-160">*Line* – Apply charges to the order lines.</span></span>

1. <span data-ttu-id="d611d-161">选择现有的自动费用进行编辑，或选择 **新** 以定义新的自动费用。</span><span class="sxs-lookup"><span data-stu-id="d611d-161">Select an existing auto charge to edit it, or select **New** to define a new auto charge.</span></span>
1. <span data-ttu-id="d611d-162">在 **帐户代码** 列表中，选择以下值之一以指定将受影响的帐户范围：</span><span class="sxs-lookup"><span data-stu-id="d611d-162">In the **Account code** list, select one of the following values to specify the scope of accounts that will be affected:</span></span>

    - <span data-ttu-id="d611d-163">*表* – 将费用分配给特定客户或供应商。</span><span class="sxs-lookup"><span data-stu-id="d611d-163">*Table* – Assign charges to a specific customer or vendor.</span></span>
    - <span data-ttu-id="d611d-164">*组* – 将费用分配给杂项费用组。</span><span class="sxs-lookup"><span data-stu-id="d611d-164">*Group* – Assign charges to a miscellaneous charges group.</span></span>
    - <span data-ttu-id="d611d-165">*所有* – 将费用分配给所有客户或供应商。</span><span class="sxs-lookup"><span data-stu-id="d611d-165">*All* – Assign charges to all customers or vendors.</span></span>

1. <span data-ttu-id="d611d-166">如果将 **帐户代码** 字段设置为 *表*，在 **客户关系** 或 **供应商关系** 字段中，选择特定客户或供应商。</span><span class="sxs-lookup"><span data-stu-id="d611d-166">In the **Customer relation** or **Vendor relation** field, select a specific customer or vendor if you set the **Account code** field to *Table*.</span></span> <span data-ttu-id="d611d-167">如果将 **帐户代码** 字段设置为 *组*，选择客户或供应商费用组。</span><span class="sxs-lookup"><span data-stu-id="d611d-167">If you set the **Account code** field to *Group*, select a customer or vendor charges group.</span></span>
1. <span data-ttu-id="d611d-168">在 **物料代码** 字段中，选择以下值之一以指定将受影响的物料范围。</span><span class="sxs-lookup"><span data-stu-id="d611d-168">In the **Item code** field, select one of the following values to specify the scope of items that will be affected.</span></span> <span data-ttu-id="d611d-169">仅当在行级别上定义自动费用时才可以选择物料代码。</span><span class="sxs-lookup"><span data-stu-id="d611d-169">You can select an item code only when you define auto charges at the line level.</span></span>

    - <span data-ttu-id="d611d-170">*表* – 将费用分配给特定物料。</span><span class="sxs-lookup"><span data-stu-id="d611d-170">*Table* – Assign charges to a specific item.</span></span>
    - <span data-ttu-id="d611d-171">*组* – 将费用分配给物料费用组。</span><span class="sxs-lookup"><span data-stu-id="d611d-171">*Group* – Assign charges to an item charges group.</span></span>
    - <span data-ttu-id="d611d-172">*所有* – 将费用分配给所有物料。</span><span class="sxs-lookup"><span data-stu-id="d611d-172">*All* – Assign charges to all items.</span></span>

1. <span data-ttu-id="d611d-173">如果将 **物料代码** 字段设置为 *表*，在 **物料关系** 字段中，选择特定物料。</span><span class="sxs-lookup"><span data-stu-id="d611d-173">In the **Item relation** field, select a specific item if you set the **Item code** field to *Table*.</span></span> <span data-ttu-id="d611d-174">如果将 **物料代码** 字段设置为 *组*，选择物料费用组。</span><span class="sxs-lookup"><span data-stu-id="d611d-174">If you set the **Item code** field to *Group*, select an item charges group.</span></span>
1. <span data-ttu-id="d611d-175">**仅适用于销售订单：** 在 **交货方式代码** 字段中，选择以下值之一以指定将受影响的交货方式的范围：</span><span class="sxs-lookup"><span data-stu-id="d611d-175">**For sales orders only:** In the **Mode of delivery code** field, select one of the following values to specify the scope of delivery modes that will be affected:</span></span>

    - <span data-ttu-id="d611d-176">*表* – 将费用分配给特定的交货方式。</span><span class="sxs-lookup"><span data-stu-id="d611d-176">*Table* – Assign charges to a specific mode of delivery.</span></span>
    - <span data-ttu-id="d611d-177">*组* – 将费用分配给交货方式组。</span><span class="sxs-lookup"><span data-stu-id="d611d-177">*Group* – Assign charges to a mode of delivery group.</span></span>
    - <span data-ttu-id="d611d-178">*所有* – 将费用分配给所有交货方式。</span><span class="sxs-lookup"><span data-stu-id="d611d-178">*All* – Assign charges to all modes of delivery.</span></span>

1. <span data-ttu-id="d611d-179">**仅适用于销售订单：** 如果将 **交货方式代码** 字段设置为 *表*，在 **交货方式关系** 字段中，选择特定的交货方式。</span><span class="sxs-lookup"><span data-stu-id="d611d-179">**For sales orders only:** In the **Mode of delivery relation** field, select a specific mode of delivery if you set the **Mode of delivery code** field to *Table*.</span></span> <span data-ttu-id="d611d-180">如果将 **交货方式代码** 字段设置为 *组*，选择交货方式组。</span><span class="sxs-lookup"><span data-stu-id="d611d-180">If you set the **Mode of delivery code** field to *Group*, select a mode of delivery group.</span></span>
1. <span data-ttu-id="d611d-181">在 **行** 快速选项卡上，定义将在应用自动费用时使用的费用和费用比率。</span><span class="sxs-lookup"><span data-stu-id="d611d-181">On the **Lines** FastTab, define the charges and the charges rates that will be used when the current auto charge is applied.</span></span> <span data-ttu-id="d611d-182">您可以使用此快速选项卡上的工具栏根据需要添加任意数量的行。</span><span class="sxs-lookup"><span data-stu-id="d611d-182">You can use the toolbar on this FastTab to add as many lines as you require.</span></span> <span data-ttu-id="d611d-183">对于每一行，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="d611d-183">For each line, set the following fields:</span></span>

    - <span data-ttu-id="d611d-184">**货币** – 选择应该用于计算费用的货币。</span><span class="sxs-lookup"><span data-stu-id="d611d-184">**Currency** – Select the currency that should be used to calculate the charge.</span></span>
    - <span data-ttu-id="d611d-185">**费用代码** – 选择费用的代码。</span><span class="sxs-lookup"><span data-stu-id="d611d-185">**Charges code** – Select the code for the charge.</span></span>
    - <span data-ttu-id="d611d-186">**类别** – 选择以下值之一：</span><span class="sxs-lookup"><span data-stu-id="d611d-186">**Category** – Select one of the following values:</span></span>

        - <span data-ttu-id="d611d-187">*固定* – 该费用在行上作为固定金额输入。</span><span class="sxs-lookup"><span data-stu-id="d611d-187">*Fixed* – The charge is entered as a fixed amount on the line.</span></span> <span data-ttu-id="d611d-188">固定费用可同时用于订单头和订单行中的费用。</span><span class="sxs-lookup"><span data-stu-id="d611d-188">Fixed charges can be used on charges both in the order header and on the order lines.</span></span>
        - <span data-ttu-id="d611d-189">*件* – 费用基于单位计算。</span><span class="sxs-lookup"><span data-stu-id="d611d-189">*Pcs* – The charge is based on the unit.</span></span> <span data-ttu-id="d611d-190">这些费用只能用于订单行。</span><span class="sxs-lookup"><span data-stu-id="d611d-190">These charges can be used only on order lines.</span></span> <span data-ttu-id="d611d-191">它们将在您计算订单合计时出现。</span><span class="sxs-lookup"><span data-stu-id="d611d-191">They will appear when you calculate the order total.</span></span>
        - <span data-ttu-id="d611d-192">*百分比* – 该费用在行上作为百分比输入。</span><span class="sxs-lookup"><span data-stu-id="d611d-192">*Percent* – The charge is entered as a percentage on the line.</span></span> <span data-ttu-id="d611d-193">百分比费用可同时用于订单头和订单行中的费用。</span><span class="sxs-lookup"><span data-stu-id="d611d-193">Percentage charges can be used on charges both in the order header and on the order lines.</span></span>
        - <span data-ttu-id="d611d-194">*内部公司百分比* – 该费用在内部公司订单的行上作为百分比输入。</span><span class="sxs-lookup"><span data-stu-id="d611d-194">*Intercompany percent* – The charge is entered as a percentage on the line for intercompany orders.</span></span> <span data-ttu-id="d611d-195">内部公司百分比费用仅可用于订单行。</span><span class="sxs-lookup"><span data-stu-id="d611d-195">Intercompany percentage charges can be used only on order lines.</span></span>
        - <span data-ttu-id="d611d-196">*外部* – 通过与一个或多个装运承运人关联的第三方服务计算该费用。</span><span class="sxs-lookup"><span data-stu-id="d611d-196">*External* – The charge is calculated by a third-party service that is associated with one or more shipping carriers.</span></span>

    - <span data-ttu-id="d611d-197">**费用值** – 根据您选择的类别输入费用值。</span><span class="sxs-lookup"><span data-stu-id="d611d-197">**Charges value** – Enter the charge value, based on the category that you selected.</span></span>
    - <span data-ttu-id="d611d-198">**费用货币代码** – 如果您要使用在 **货币** 字段中指定的货币以外的货币，请指定费用的货币。</span><span class="sxs-lookup"><span data-stu-id="d611d-198">**Charges currency code** – Specify a currency for the charge if you want to use a currency other than the currency that you specified in the **Currency** field.</span></span> <span data-ttu-id="d611d-199">如果将所选费用代码的 **借方类型** 或 **贷方类型** 字段设置为 *分类帐帐户* 或 *物料*，仅可以使用不同的货币。</span><span class="sxs-lookup"><span data-stu-id="d611d-199">You can use a different currency only if the **Debit type** or **Credit type** field is set to either *Ledger account* or *Item* for the selected charges code.</span></span>
    - <span data-ttu-id="d611d-200">**起始金额** – 指定将自动费用应用到的开始金额。</span><span class="sxs-lookup"><span data-stu-id="d611d-200">**From amount** – Specify a starting amount to apply the auto charge to.</span></span> <span data-ttu-id="d611d-201">在此情况下，金额引用订单合计。</span><span class="sxs-lookup"><span data-stu-id="d611d-201">In this context, the amount refers to the order total.</span></span>
    - <span data-ttu-id="d611d-202">**终止金额** – 指定将自动费用应用到的结束金额。</span><span class="sxs-lookup"><span data-stu-id="d611d-202">**To amount** – Specify the ending amount to apply the auto charge to.</span></span> <span data-ttu-id="d611d-203">在此情况下，金额引用订单合计。</span><span class="sxs-lookup"><span data-stu-id="d611d-203">In this context, the amount refers to the order total.</span></span>
    - <span data-ttu-id="d611d-204">**销售税组** – 指定销售税组。</span><span class="sxs-lookup"><span data-stu-id="d611d-204">**Sales tax group** – Specify a sales tax group.</span></span>
    - <span data-ttu-id="d611d-205">**站点** 和 **仓库** – 如果仅针对特定的站点和仓库应用费用，指定站点和仓库。</span><span class="sxs-lookup"><span data-stu-id="d611d-205">**Site** and **Warehouse** – Specify a site and warehouse if charges should be applied only for a specific site and warehouse.</span></span>
    - <span data-ttu-id="d611d-206">**保留** – 选中此复选框以在完成开票后保留这些费用交易记录，以便每次为所选客户帐户创建新发票时应用该费用。</span><span class="sxs-lookup"><span data-stu-id="d611d-206">**Keep** – Select this check box to keep the charges transactions after invoicing is completed, so that the charge will be applied every time that you create a new invoice for the selected customer account.</span></span>

1. <span data-ttu-id="d611d-207">**仅适用于销售订单：** 如果您想要计算分层费用，请参阅[销售订单上的分层费用](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-tiered-charges-on-sales-orders)以获取相关信息。</span><span class="sxs-lookup"><span data-stu-id="d611d-207">**For sales orders only:** If you want to calculate tiered charges, see [Tiered charges on sales orders](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-tiered-charges-on-sales-orders) for information.</span></span>

## <a name="allocate-charges-from-the-header-to-a-line"></a><span data-ttu-id="d611d-208">将费用从标头分配到行</span><span class="sxs-lookup"><span data-stu-id="d611d-208">Allocate charges from the header to a line</span></span>

<span data-ttu-id="d611d-209">以下过程显示了如何将标头级费用分配到行。</span><span class="sxs-lookup"><span data-stu-id="d611d-209">The following procedure shows how to allocate header-level charges to a line.</span></span> <span data-ttu-id="d611d-210">在开始此过程之前，您应该已经有 *固定金额* 类型的标头级费用和将应用该费用的订单。</span><span class="sxs-lookup"><span data-stu-id="d611d-210">Before you start this procedure, you should already have a header-level charge of the *fixed amount* type and an order where that charge is applied.</span></span> <span data-ttu-id="d611d-211">此外，该订单应该已包括至少一个行项。</span><span class="sxs-lookup"><span data-stu-id="d611d-211">Additionally, the order should already include at least one line item.</span></span>

1. <span data-ttu-id="d611d-212">打开采购订单或费用订单。</span><span class="sxs-lookup"><span data-stu-id="d611d-212">Open the purchase order or charge order.</span></span>
1. <span data-ttu-id="d611d-213">在“操作”窗格上，请按照下列步骤之一操作：</span><span class="sxs-lookup"><span data-stu-id="d611d-213">On the Action Pane, follow one of these steps:</span></span>

    - <span data-ttu-id="d611d-214">对于采购订单：在 **购买** 选项卡上的 **费用** 组中，选择 **分配费用**。</span><span class="sxs-lookup"><span data-stu-id="d611d-214">For purchase orders: On the **Purchase** tab, in the **Charges** group, select **Allocate charges**.</span></span>
    - <span data-ttu-id="d611d-215">对于销售订单：在 **销售** 选项卡上的 **费用** 组中，选择 **分配费用**。</span><span class="sxs-lookup"><span data-stu-id="d611d-215">For sales orders: On the **Sell** tab, in the **Charges** group, select **Allocate charges**.</span></span>

1. <span data-ttu-id="d611d-216">在 **将费用分配给订单行** 对话框中，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="d611d-216">In the **Allocate charges to order lines** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="d611d-217">**费用分配** – 选择以下值之一以指定应如何分配费用：</span><span class="sxs-lookup"><span data-stu-id="d611d-217">**Charges allocation** – Select one of the following values to specify how the charges should be allocated:</span></span>

        - <span data-ttu-id="d611d-218">*净额* – 根据每行金额相对于总净额分配费用。</span><span class="sxs-lookup"><span data-stu-id="d611d-218">*Net amount* – Allocate charges according to each line amount relative to the total net amount.</span></span>
        - <span data-ttu-id="d611d-219">*数量* – 根据每行的单位数量相对于单位总数分配费用。</span><span class="sxs-lookup"><span data-stu-id="d611d-219">*Quantity* – Allocate charges according to the number of units for each line relative to the total number of units.</span></span>
        - <span data-ttu-id="d611d-220">*每行* – 根据总行数平均分配费用。</span><span class="sxs-lookup"><span data-stu-id="d611d-220">*Per line* – Allocate charges equally among the total number of lines.</span></span>

    - <span data-ttu-id="d611d-221">**将费用分配给行** – 选择一个值以指定是应该将费用分配给所有行、仅分配给正数行还是仅分配给负数行。</span><span class="sxs-lookup"><span data-stu-id="d611d-221">**Allocate charges to lines** – Select a value to specify whether charges should be allocated to all lines, to positive lines only, or to negative lines only.</span></span>
    - <span data-ttu-id="d611d-222">**分配所有** – 选中此复选框以将费用分配给订单行，即使费用代码具有借方类型而不是 *物料*。</span><span class="sxs-lookup"><span data-stu-id="d611d-222">**Allocate all** – Select this check box to allocate charges to order lines even if the charges code has a debit type other than *Item*.</span></span>
    - <span data-ttu-id="d611d-223">**已收货** – 选中此复选框以将费用仅分配给已收货的订单行。</span><span class="sxs-lookup"><span data-stu-id="d611d-223">**Received** – Select this check box to allocate charges only to received order lines.</span></span>
    - <span data-ttu-id="d611d-224">**已贮存** – 选中此复选框以将费用仅分配给库存订单行。</span><span class="sxs-lookup"><span data-stu-id="d611d-224">**Stocked** – Select this check box to allocate charges to only inventoried order lines.</span></span>
    - <span data-ttu-id="d611d-225">**显示所选内容并清除特定行** – 选中此复选框以从此分配中排除特定行。</span><span class="sxs-lookup"><span data-stu-id="d611d-225">**Show selections and clear specific lines** – Select this check box to exclude specific lines from this allocation.</span></span> <span data-ttu-id="d611d-226">当选中此复选框时，将打开 **选择要从分配中排除的行** 网格。</span><span class="sxs-lookup"><span data-stu-id="d611d-226">When you select this check box, the **Choose lines to exclude from allocation** grid is opened.</span></span> <span data-ttu-id="d611d-227">此网格仅包括与 **将费用分配给行** 和 **已贮存** 设置中定义的条件相匹配的行。</span><span class="sxs-lookup"><span data-stu-id="d611d-227">This grid includes only lines that match the criteria that are defined by the **Allocate charges to lines** and **Stocked** settings.</span></span> <span data-ttu-id="d611d-228">例如，如果将 **将费用分配给行** 字段设置为 *正数行* 并选中 **已贮存** 复选框，则网格仅显示正数行和库存行。</span><span class="sxs-lookup"><span data-stu-id="d611d-228">For example, if you set the **Allocate charges to lines** field to *Positive lines* and select the **Stocked** check box, the grid shows only lines that are both positive and inventoried.</span></span> <span data-ttu-id="d611d-229">此外，网格将自动筛选掉已收到全部数量的所有行。</span><span class="sxs-lookup"><span data-stu-id="d611d-229">In addition, the grid automatically filters out any lines that the full quantity has already been received for.</span></span> <span data-ttu-id="d611d-230">打开网格后，对于应该从分配中排除的每个行，清除 **包括** 复选框。</span><span class="sxs-lookup"><span data-stu-id="d611d-230">While the grid is open, clear the **Include** check box for each line that should be excluded from allocation.</span></span> 

        > [!IMPORTANT]
        > <span data-ttu-id="d611d-231">当使用 **选择要从分配中排除的行** 网格时，请确保在选择 **分配** 之前将网格保持打开状态。</span><span class="sxs-lookup"><span data-stu-id="d611d-231">When you work with the **Choose lines to exclude from allocation** grid, be sure to leave the grid open until you select **Allocate**.</span></span> <span data-ttu-id="d611d-232">如果在选择 **分配** 之前关闭网格，您在网格中的设置将丢失。</span><span class="sxs-lookup"><span data-stu-id="d611d-232">If you close the grid before you select **Allocate**, your settings in the grid will be lost.</span></span> <span data-ttu-id="d611d-233">因此，将根据您先前定义的条件分配费用。</span><span class="sxs-lookup"><span data-stu-id="d611d-233">Therefore, charges will be allocated based on the criteria that you previously defined.</span></span>

1. <span data-ttu-id="d611d-234">选择 **分配** 以应用设置并关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="d611d-234">Select **Allocate** to apply your settings and close the dialog box.</span></span>

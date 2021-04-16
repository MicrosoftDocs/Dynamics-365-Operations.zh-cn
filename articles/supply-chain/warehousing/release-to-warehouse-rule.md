---
title: 发放到仓库规则
description: 本主题介绍“发放到仓库规则”功能，该功能用于在发放到仓库期间提供灵活性。 其添加了一个配置选项，用于控制系统是否允许发放部分保留的订单行。
author: mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 77714d6bda27d8d29b10177dd87e61839295e47e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823255"
---
# <a name="release-to-warehouse-rule"></a><span data-ttu-id="31ebe-104">发放到仓库规则</span><span class="sxs-lookup"><span data-stu-id="31ebe-104">Release to warehouse rule</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31ebe-105">*发放到仓库规则* 功能在发放到仓库期间提供灵活性。</span><span class="sxs-lookup"><span data-stu-id="31ebe-105">The *Release to warehouse rule* feature provides flexibility during release to the warehouse.</span></span> <span data-ttu-id="31ebe-106">其为每个仓库添加一个配置选项。</span><span class="sxs-lookup"><span data-stu-id="31ebe-106">It adds a configuration option for each warehouse.</span></span> <span data-ttu-id="31ebe-107">可使用此选项指定是否可为该仓库发放部分预留订单行。</span><span class="sxs-lookup"><span data-stu-id="31ebe-107">You can use this option to specify whether partially reserved order lines can be released for that warehouse.</span></span> <span data-ttu-id="31ebe-108">此功能与高级越库配送功能在以下情况下一起工作：根据供应源标记订单行数量中的一部分，但是可以在仓库中处理其余部分。</span><span class="sxs-lookup"><span data-stu-id="31ebe-108">The feature works together with advanced cross-docking functionality in situations where part of an order line quantity is marked against a supply source, but the remaining part can be processed in the warehouse.</span></span> <span data-ttu-id="31ebe-109">因此，可以发放行，以便仓库继续处理可用库存数量。</span><span class="sxs-lookup"><span data-stu-id="31ebe-109">Therefore, the line can be released so that warehouse processing of the available inventory quantity can continue.</span></span>

## <a name="turn-on-and-initialize-the-release-to-warehouse-rule-feature"></a><span data-ttu-id="31ebe-110">开启和初始化发放到仓库规则功能</span><span class="sxs-lookup"><span data-stu-id="31ebe-110">Turn on and initialize the Release to warehouse rule feature</span></span>

### <a name="turn-on-the-feature"></a><span data-ttu-id="31ebe-111">开启功能</span><span class="sxs-lookup"><span data-stu-id="31ebe-111">Turn on the feature</span></span>

<span data-ttu-id="31ebe-112">*仓库发放规则* 功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="31ebe-112">Before you can use the *Warehouse release rule* feature, it must be turned on in your system.</span></span> <span data-ttu-id="31ebe-113">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="31ebe-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="31ebe-114">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="31ebe-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="31ebe-115">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="31ebe-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="31ebe-116">**功能名称**：*仓库发放规则*</span><span class="sxs-lookup"><span data-stu-id="31ebe-116">**Feature name:** *Warehouse release rule*</span></span>

### <a name="initialize-the-feature"></a><span data-ttu-id="31ebe-117">初始化功能</span><span class="sxs-lookup"><span data-stu-id="31ebe-117">Initialize the feature</span></span>

<span data-ttu-id="31ebe-118">在系统中开启该功能后，必须对其进行初始化，以便将规则设置为所有仓库的正确初始状态。</span><span class="sxs-lookup"><span data-stu-id="31ebe-118">After the feature is turned on in your system, you must initialize it to set the rule to the correct initial state for all warehouses.</span></span>

- <span data-ttu-id="31ebe-119">对于未启用仓库管理的仓库，此规则最初设置为 **不适用**。</span><span class="sxs-lookup"><span data-stu-id="31ebe-119">For warehouses that aren't enabled for warehouse management, the rule is initially set to **Not applicable**.</span></span>
- <span data-ttu-id="31ebe-120">对于启用了仓库管理的仓库，此规则最初设置为 **允许部分预留**</span><span class="sxs-lookup"><span data-stu-id="31ebe-120">For warehouses that are enabled for warehouse management, the rule is initially set to **Allow partial reservation**</span></span>

<span data-ttu-id="31ebe-121">若要初始化此功能并为所有仓库设置发放到仓库规则，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="31ebe-121">To initialize the feature and set the release to warehouse rule for all warehouses, follow these steps.</span></span>

1. <span data-ttu-id="31ebe-122">转到 **仓库管理 \> 设置 \> 仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="31ebe-122">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="31ebe-123">在 **仓库管理参数** 页面 **常规** 选项卡上的 **公司信息** 部分中，选择 **初始化发放到仓库** 规则的链接。</span><span class="sxs-lookup"><span data-stu-id="31ebe-123">On the **Warehouse management parameters** page, on the **General** tab, in the **Company information** section, select the link for the **Initialize release to warehouse** rule.</span></span> <span data-ttu-id="31ebe-124">（如果不显示此链接，说明未开启或已初始化此功能。）</span><span class="sxs-lookup"><span data-stu-id="31ebe-124">(If this link isn't shown, either the feature isn't turned on or it has already been initialized.)</span></span>
1. <span data-ttu-id="31ebe-125">提示确认操作时，选择 **是** 初始化此功能。</span><span class="sxs-lookup"><span data-stu-id="31ebe-125">When you're prompted to confirm the action, select **Yes** to initialize the feature.</span></span>

## <a name="set-the-release-to-warehouse-rule-for-each-warehouse"></a><a name="set-option-warehouse"></a><span data-ttu-id="31ebe-126">为每个仓库设置发放到仓库规则</span><span class="sxs-lookup"><span data-stu-id="31ebe-126">Set the release to warehouse rule for each warehouse</span></span>

<span data-ttu-id="31ebe-127">开启并初始化此功能之后，您的所有仓库都将具有初始设置，如上一部分中所述。</span><span class="sxs-lookup"><span data-stu-id="31ebe-127">After the feature is turned on and initialized, all your warehouses will have an initial setting, as described in the previous section.</span></span> <span data-ttu-id="31ebe-128">可以执行以下步骤更改单个仓库的此设置。</span><span class="sxs-lookup"><span data-stu-id="31ebe-128">You can change this setting for individual warehouses by following these steps.</span></span>

1. <span data-ttu-id="31ebe-129">转到 **仓库管理 \> 设置 \> 仓库 \> 仓库**。</span><span class="sxs-lookup"><span data-stu-id="31ebe-129">Go to **Warehouse management \> Setup \> Warehouse \> Warehouses**.</span></span>
1. <span data-ttu-id="31ebe-130">选择要配置的仓库。</span><span class="sxs-lookup"><span data-stu-id="31ebe-130">Select the warehouse to configure.</span></span>
1. <span data-ttu-id="31ebe-131">选择 **编辑** 将页面设置为编辑模式。</span><span class="sxs-lookup"><span data-stu-id="31ebe-131">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="31ebe-132">在 **仓库** 快速选项卡的 **预留** 部分中，**库存预留要求** 字段控制是否允许部分下达订单。</span><span class="sxs-lookup"><span data-stu-id="31ebe-132">On the **Warehouse** FastTab, in the **Reservations** section, the **Requirement for inventory reservation** field controls whether partial release of orders is allowed.</span></span> <span data-ttu-id="31ebe-133">选择以下值之一：</span><span class="sxs-lookup"><span data-stu-id="31ebe-133">Select one of the following values:</span></span>

    - <span data-ttu-id="31ebe-134">**不适用** – 首次开启和初始化此功能时，将把该值自动分配给未启用仓库管理的所有仓库。</span><span class="sxs-lookup"><span data-stu-id="31ebe-134">**Not applicable** – When the feature is first turned on and initialized, this value is automatically assigned to all warehouses that aren't enabled for warehouse management.</span></span> <span data-ttu-id="31ebe-135">不能更改该设置。</span><span class="sxs-lookup"><span data-stu-id="31ebe-135">It can't be changed.</span></span> <span data-ttu-id="31ebe-136">该值不适用于启用了仓库管理的仓库。</span><span class="sxs-lookup"><span data-stu-id="31ebe-136">This value isn't available for warehouses that are enabled for warehouse management.</span></span>
    - <span data-ttu-id="31ebe-137">**允许部分预留** – 如果预留了任何数量，则可下达订单。</span><span class="sxs-lookup"><span data-stu-id="31ebe-137">**Allow partial reservation** – Orders can be released when any quantity is reserved.</span></span> <span data-ttu-id="31ebe-138">系统将评估是否应该为高级越库配送标记未预留数量，并将根据需要标记该数量。</span><span class="sxs-lookup"><span data-stu-id="31ebe-138">The system will evaluate whether the unreserved quantity should be marked for advanced cross-docking and will mark that quantity as required.</span></span> <span data-ttu-id="31ebe-139">如果不存在标记，系统将仅为预留数量创建工作。</span><span class="sxs-lookup"><span data-stu-id="31ebe-139">If no marking exists, the system will create work only for the reserved quantity.</span></span> <span data-ttu-id="31ebe-140">首次开启和初始化此功能时，将把该值自动分配给已启用仓库管理的所有仓库。</span><span class="sxs-lookup"><span data-stu-id="31ebe-140">When the feature is first turned on and initialized, this value is automatically assigned to all warehouses that are enabled for warehouse management.</span></span> <span data-ttu-id="31ebe-141">该值不适用于未启用仓库管理的仓库。</span><span class="sxs-lookup"><span data-stu-id="31ebe-141">This value isn't available for warehouses that aren't enabled for warehouse management.</span></span>
    - <span data-ttu-id="31ebe-142">**需要全部预留** – 仅当预留所有数量，才能下达订单。</span><span class="sxs-lookup"><span data-stu-id="31ebe-142">**Require full reservation** – Orders can be released only if the whole quantity is reserved.</span></span> <span data-ttu-id="31ebe-143">如果没有为越库配送物理预留或计划所有数量，则不能发放。</span><span class="sxs-lookup"><span data-stu-id="31ebe-143">They can't be released if the total quantity isn't either physically reserved or planned for cross-docking.</span></span> <span data-ttu-id="31ebe-144">该值不适用于未启用仓库管理的仓库。</span><span class="sxs-lookup"><span data-stu-id="31ebe-144">This value isn't available for warehouses that aren't enabled for warehouse management.</span></span>

1. <span data-ttu-id="31ebe-145">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="31ebe-145">Select **Save**.</span></span>

## <a name="scenarios"></a><span data-ttu-id="31ebe-146">方案</span><span class="sxs-lookup"><span data-stu-id="31ebe-146">Scenarios</span></span>

<span data-ttu-id="31ebe-147">此部分提供两个场景，可用于了解此功能及其用法。</span><span class="sxs-lookup"><span data-stu-id="31ebe-147">This section provides two scenarios that you can work through to learn what the feature does and how to use it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="31ebe-148">提供示例数据</span><span class="sxs-lookup"><span data-stu-id="31ebe-148">Make sample data available</span></span>

<span data-ttu-id="31ebe-149">若要使用此处指定的示例记录和值完成这些场景，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="31ebe-149">To work through these scenarios by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="31ebe-150">此外，开始前，还必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="31ebe-150">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="31ebe-151">使用生产系统时，也可以将这些场景用作使用此功能的指导。</span><span class="sxs-lookup"><span data-stu-id="31ebe-151">You can also use these scenarios as guidance for the feature when you work on a production system.</span></span> <span data-ttu-id="31ebe-152">但是，在此情况下，必须替换为您自己的值，而您可能会缺少标准演示数据提供的某些类型的必需记录。</span><span class="sxs-lookup"><span data-stu-id="31ebe-152">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-1-require-full-release-no-planned-cross-docking"></a><a name="scenario1"></a><span data-ttu-id="31ebe-153">场景 1：需要完全发放（未计划越库配送）</span><span class="sxs-lookup"><span data-stu-id="31ebe-153">Scenario 1: Require full release (no planned cross-docking)</span></span>

<span data-ttu-id="31ebe-154">此场景显示该功能对设置为 **需要完全预留** 的仓库的作用。</span><span class="sxs-lookup"><span data-stu-id="31ebe-154">This scenario shows how the feature works for warehouses that are set to **Require full reservation**.</span></span>

1. <span data-ttu-id="31ebe-155">转到 **仓库管理 \> 设置 \> 仓库 \> 仓库**。</span><span class="sxs-lookup"><span data-stu-id="31ebe-155">Go to **Warehouse management \> Setup \> Warehouse \> Warehouses**.</span></span>
1. <span data-ttu-id="31ebe-156">对于仓库 _62_，将 **库存预留要求** 字段设置为 **需要完全预留**，如本主题前面的[为每个仓库设置发放到仓库规则](#set-option-warehouse)部分中所述。</span><span class="sxs-lookup"><span data-stu-id="31ebe-156">For warehouse _62_, set the **Requirement for inventory reservation** field to **Require full reservation**, as described in the [Set the release to warehouse rule for each warehouse](#set-option-warehouse) section earlier in this topic.</span></span>
1. <span data-ttu-id="31ebe-157">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="31ebe-157">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="31ebe-158">选择 **新建** 以创建新的销售订单。</span><span class="sxs-lookup"><span data-stu-id="31ebe-158">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="31ebe-159">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="31ebe-159">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="31ebe-160">在 **客户** 快速选项卡上，将 **客户帐户** 字段设置为 _US-004_。</span><span class="sxs-lookup"><span data-stu-id="31ebe-160">On the **Customer** FastTab, set the **Customer account** field to _US-004_.</span></span>
    - <span data-ttu-id="31ebe-161">在 **常规** 快速选项卡上，将 **仓库** 字段设置为 _62_。</span><span class="sxs-lookup"><span data-stu-id="31ebe-161">On the **General** FastTab, set the **Warehouse** field to _62_.</span></span>

1. <span data-ttu-id="31ebe-162">选择 **确定** 创建新销售订单，然后关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="31ebe-162">Select **OK** to create the new sales order and close the dialog box.</span></span>
1. <span data-ttu-id="31ebe-163">将打开您的新销售订单。</span><span class="sxs-lookup"><span data-stu-id="31ebe-163">Your new sales order is opened.</span></span> <span data-ttu-id="31ebe-164">其在 **销售订单行** 部分的网格中添加一个新的空行。</span><span class="sxs-lookup"><span data-stu-id="31ebe-164">It includes an empty line in the grid in the **Sales order lines** section.</span></span> <span data-ttu-id="31ebe-165">在这个行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="31ebe-165">On this line, set the following values:</span></span>

    - <span data-ttu-id="31ebe-166">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="31ebe-166">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="31ebe-167">**数量：** *2*</span><span class="sxs-lookup"><span data-stu-id="31ebe-167">**Quantity:** *2*</span></span>

1. <span data-ttu-id="31ebe-168">选择 **添加行** 添加新行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="31ebe-168">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="31ebe-169">\**物料编号：\*\*\*A0002*</span><span class="sxs-lookup"><span data-stu-id="31ebe-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="31ebe-170">**数量：** *2*</span><span class="sxs-lookup"><span data-stu-id="31ebe-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="31ebe-171">选择第一个订单行，然后在网格上方的 **库存** 菜单中选择 **预留**。</span><span class="sxs-lookup"><span data-stu-id="31ebe-171">Select the first order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="31ebe-172">在 **预留** 页中，选择 **预留批次** 在仓库中预留所选行的全部数量。</span><span class="sxs-lookup"><span data-stu-id="31ebe-172">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="31ebe-173">关闭 **预留** 页回到销售订单。</span><span class="sxs-lookup"><span data-stu-id="31ebe-173">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="31ebe-174">请勿预留第二个订单行。</span><span class="sxs-lookup"><span data-stu-id="31ebe-174">Don't reserve the second order line.</span></span>
1. <span data-ttu-id="31ebe-175">在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="31ebe-175">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="31ebe-176">请注意，您将收到以下错误消息：“必须物理预留所有数量。”</span><span class="sxs-lookup"><span data-stu-id="31ebe-176">Notice that you receive the following error message: "The full quantity must be physically reserved."</span></span> <span data-ttu-id="31ebe-177">因此，系统不会为订单创建任何工作、装运或负荷。</span><span class="sxs-lookup"><span data-stu-id="31ebe-177">Therefore, the system doesn't create any work, shipment, or load for the order.</span></span>

    > [!NOTE]
    > <span data-ttu-id="31ebe-178">如果部分预留第二行，将收到相同错误消息。</span><span class="sxs-lookup"><span data-stu-id="31ebe-178">You will receive the same error message if you partially reserve the second line.</span></span>

### <a name="scenario-2-allow-partial-release"></a><span data-ttu-id="31ebe-179">场景 2：允许部分发放</span><span class="sxs-lookup"><span data-stu-id="31ebe-179">Scenario 2: Allow partial release</span></span>

<span data-ttu-id="31ebe-180">此场景显示该功能对设置为 **允许部分发放** 的仓库的作用。</span><span class="sxs-lookup"><span data-stu-id="31ebe-180">This scenario shows how the feature works for warehouses that are set to **Allow partial release**.</span></span>

1. <span data-ttu-id="31ebe-181">转到 **仓库管理 \> 设置 \> 仓库 \> 仓库**。</span><span class="sxs-lookup"><span data-stu-id="31ebe-181">Go to **Warehouse management \> Setup \> Warehouse \> Warehouses**.</span></span>
1. <span data-ttu-id="31ebe-182">对于仓库 _62_，将 **库存预留要求** 字段设置为 **允许部分预留**，如本主题前面的[为每个仓库设置发放到仓库规则](#set-option-warehouse)部分中所述。</span><span class="sxs-lookup"><span data-stu-id="31ebe-182">For warehouse _62_, set the **Requirement for inventory reservation** field to **Allow partial reservation**, as described in the [Set the release to warehouse rule for each warehouse](#set-option-warehouse) section earlier in this topic.</span></span>
1. <span data-ttu-id="31ebe-183">如您在 [前一个场景](#scenario1)中执行的操作，转到 **销售和市场营销 \> 销售订单 \> 所有销售订单**，然后为仓库 _62_ 中的客户帐户 _US-004_ 创建一个销售订单。</span><span class="sxs-lookup"><span data-stu-id="31ebe-183">As you did in the [previous scenario](#scenario1), go to **Sales and marketing \> Sales orders \> All sales orders**, and create a sales order for customer account _US-004_ from warehouse _62_.</span></span> <span data-ttu-id="31ebe-184">添加下面的两个订单行：</span><span class="sxs-lookup"><span data-stu-id="31ebe-184">Add the following two order lines:</span></span>

    - <span data-ttu-id="31ebe-185">**行 1：** 将 **物料编号** 字段设置为 _A0001_，将 **数量** 字段设置为 _2_，将 **单位** 字段设置为 _件_。</span><span class="sxs-lookup"><span data-stu-id="31ebe-185">**Line 1:** Set the **Item number** field to _A0001_, the **Quantity** field to _2_, and the **Unit** field to _Pcs_.</span></span>
    - <span data-ttu-id="31ebe-186">**行 2：** 将 **物料编号** 字段设置为 _A0002_，将 **数量** 字段设置为 _2_，将 **单位** 字段设置为 _件_。</span><span class="sxs-lookup"><span data-stu-id="31ebe-186">**Line 2:** Set the **Item number** field to _A0002_, the **Quantity** field to _2_, and the **Unit** field to _Pcs_.</span></span>

1. <span data-ttu-id="31ebe-187">如您在[前一个场景](#scenario1)中执行的操作，为订单行 1 预留所有数量，但是不预留订单行 2。</span><span class="sxs-lookup"><span data-stu-id="31ebe-187">As you did in the [previous scenario](#scenario1), reserve the full quantity for order line 1, but don't reserve order line 2.</span></span>
1. <span data-ttu-id="31ebe-188">在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="31ebe-188">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="31ebe-189">请注意，这次不会收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="31ebe-189">Notice that you don't receive an error message this time.</span></span> <span data-ttu-id="31ebe-190">相反，系统将根据需要创建工作、装运和负荷，然后显示结果。</span><span class="sxs-lookup"><span data-stu-id="31ebe-190">Instead, the system creates work, shipments, and loads as required, and shows the results.</span></span>
1. <span data-ttu-id="31ebe-191">若要查看装运、负荷和工作信息，请使用网格上方 **仓库** 菜单中的选项：</span><span class="sxs-lookup"><span data-stu-id="31ebe-191">To view the shipment, load, and work information, use the options on the **Warehouse** menu above the grid:</span></span>

    - <span data-ttu-id="31ebe-192">**行 1：** 可使用三个选项：**装运详细信息**、**负荷详细信息** 和 **工作详细信息**。</span><span class="sxs-lookup"><span data-stu-id="31ebe-192">**Line 1:** Three options are available: **Shipment details**, **Load details**, and **Work details**.</span></span> <span data-ttu-id="31ebe-193">选择每个选项查看将订单下达到仓库时创建的装运、负荷和工作的详细信息。</span><span class="sxs-lookup"><span data-stu-id="31ebe-193">Select each option to view the details of the shipment, load, and work that were created when the order was released to the warehouse.</span></span>
    - <span data-ttu-id="31ebe-194">**行 2：** 只能使用 **工作详细信息** 选项。</span><span class="sxs-lookup"><span data-stu-id="31ebe-194">**Line 2:** Only the **Work details** option is available.</span></span> <span data-ttu-id="31ebe-195">选择该选项，然后注意未创建任何工作，因为未预留任何库存。</span><span class="sxs-lookup"><span data-stu-id="31ebe-195">Select it, and notice that no work has been created, because no inventory was reserved.</span></span> <span data-ttu-id="31ebe-196">因此，未创建任何装运或负荷。</span><span class="sxs-lookup"><span data-stu-id="31ebe-196">Therefore, no shipment or load was created either.</span></span>

> [!NOTE]
> <span data-ttu-id="31ebe-197">部分预留第二行时，结果应该相同。</span><span class="sxs-lookup"><span data-stu-id="31ebe-197">The same result is expected when the second line is partially reserved.</span></span> <span data-ttu-id="31ebe-198">在此情况下，将为预留行数量创建工作，但是不会为未预留数量创建。</span><span class="sxs-lookup"><span data-stu-id="31ebe-198">In this case, work will be created for the reserved line quantity but not for the unreserved quantity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
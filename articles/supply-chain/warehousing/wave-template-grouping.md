---
title: 波次模板分组
description: 波次模板分组功能让系统使用波次模板设置根据定义的条件确定如何拆分已发放行和将其分配给新波次或现有波次。 在根据特定条件创建了波次，但是经理希望自动，而不是手动创建波次的仓库中，此功能可能非常有用。
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 520338683443105ffd1df7fc2569cd95a5f50879
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245122"
---
# <a name="wave-template-grouping"></a><span data-ttu-id="a691b-104">波次模板分组</span><span class="sxs-lookup"><span data-stu-id="a691b-104">Wave template grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a691b-105">波次模板分组功能让系统使用[波次模板](tasks/configure-wave-processing.md)设置根据定义的条件确定如何拆分已发放行和将其分配给新波次或现有波次。</span><span class="sxs-lookup"><span data-stu-id="a691b-105">Wave template grouping enables the system to use [wave template](tasks/configure-wave-processing.md) setups to determine, based on criteria that you define, how it should split released lines and assign them to new or existing waves.</span></span> <span data-ttu-id="a691b-106">在根据特定条件创建了波次，但是经理希望自动，而不是手动创建波次的仓库中，此功能可能非常有用。</span><span class="sxs-lookup"><span data-stu-id="a691b-106">This feature can be useful in warehouses where waves are created based on specific criteria, but where managers prefer to create waves automatically instead of manually.</span></span> <span data-ttu-id="a691b-107">其让系统将新发放的每个装运添加到找到具有匹配分组字段的第一个波次。</span><span class="sxs-lookup"><span data-stu-id="a691b-107">It enables the system to add each newly released shipment to the first wave that it finds that has matching grouping field values.</span></span> <span data-ttu-id="a691b-108">卢沟未找到匹配项，系统将为新装运创建新波次。</span><span class="sxs-lookup"><span data-stu-id="a691b-108">If no match is found, the system creates a new wave for the new shipment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a691b-109">工作类型 *生产原材料领料* 或 *看板领料* 不支持波次模板分组功能。</span><span class="sxs-lookup"><span data-stu-id="a691b-109">Wave template grouping isn't supported for the work types *production raw material picking* or *Kanban picking*.</span></span> <span data-ttu-id="a691b-110">这是因为波次分组基于装运，而这些工作类型不使用装运。</span><span class="sxs-lookup"><span data-stu-id="a691b-110">This is because wave grouping is based on shipments and these work types don't use shipments.</span></span>

## <a name="turn-on-the-wave-template-grouping-feature"></a><span data-ttu-id="a691b-111">开启波次模板分组功能</span><span class="sxs-lookup"><span data-stu-id="a691b-111">Turn on the Wave template grouping feature</span></span>

<span data-ttu-id="a691b-112">*波次模板分组* 功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="a691b-112">Before you can use the *Wave template grouping* feature, it must be turned on in your system.</span></span> <span data-ttu-id="a691b-113">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="a691b-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="a691b-114">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="a691b-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a691b-115">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="a691b-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a691b-116">**功能名称**：*波次模板分组*</span><span class="sxs-lookup"><span data-stu-id="a691b-116">**Feature name:** *Wave template grouping*</span></span>

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a><span data-ttu-id="a691b-117">设置波次模板以使用波次模板分组功能</span><span class="sxs-lookup"><span data-stu-id="a691b-117">Set a wave template to use wave template grouping</span></span>

<span data-ttu-id="a691b-118">若要启用波次模板分组功能，请执行以下步骤设置[波次模板](tasks/configure-wave-processing.md)。</span><span class="sxs-lookup"><span data-stu-id="a691b-118">To make wave template grouping available, follow these steps to set up your [wave template](tasks/configure-wave-processing.md).</span></span>

1. <span data-ttu-id="a691b-119">转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。</span><span class="sxs-lookup"><span data-stu-id="a691b-119">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="a691b-120">在左侧窗格中，选择要设置的波次模板。</span><span class="sxs-lookup"><span data-stu-id="a691b-120">In the left pane, select the wave template to set up.</span></span> <span data-ttu-id="a691b-121">如果准备使用演示数据完成本主题后文的场景，请选择 **62 装运默认** 模板。</span><span class="sxs-lookup"><span data-stu-id="a691b-121">If you're preparing to work through the scenario later in this topic by using demo data, select the **62 Shipping default** template.</span></span>
1. <span data-ttu-id="a691b-122">选择 **编辑** 将页面设置为编辑模式。</span><span class="sxs-lookup"><span data-stu-id="a691b-122">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="a691b-123">在 **常规** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="a691b-123">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="a691b-124">**自动创建波次**：*是*</span><span class="sxs-lookup"><span data-stu-id="a691b-124">**Automate wave creation:** *Yes*</span></span>
    - <span data-ttu-id="a691b-125">**分配给未结波次**：*是*</span><span class="sxs-lookup"><span data-stu-id="a691b-125">**Assign to open waves:** *Yes*</span></span>
    - <span data-ttu-id="a691b-126">**在发布到仓库时处理波次**：*否*</span><span class="sxs-lookup"><span data-stu-id="a691b-126">**Process wave at release to warehouse:** *No*</span></span>

1. <span data-ttu-id="a691b-127">在操作窗格上，选择 **编辑查询** 打开查询对话框。</span><span class="sxs-lookup"><span data-stu-id="a691b-127">On the Action Pane, select **Edit query** to open the query dialog box.</span></span>
1. <span data-ttu-id="a691b-128">在查询对话框中 **排序** 选项卡上，查看排序条件，并确保有规则中包含要用于为波次分组的字段。</span><span class="sxs-lookup"><span data-stu-id="a691b-128">In the query dialog box, on the **Sorting** tab, review the sorting criteria, and make sure that there is a rule that includes the field that you want to use to group your waves.</span></span>

    <span data-ttu-id="a691b-129">如果准备使用演示数据完成此场景，请添加包含以下值的行：</span><span class="sxs-lookup"><span data-stu-id="a691b-129">If you're preparing to work through the scenario by using demo data, add a row that has the following values:</span></span>

    - <span data-ttu-id="a691b-130">**表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="a691b-130">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="a691b-131">**派生表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="a691b-131">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="a691b-132">**字段**：*承运人服务*</span><span class="sxs-lookup"><span data-stu-id="a691b-132">**Field:** *Carrier service*</span></span>

        > [!NOTE]
        > <span data-ttu-id="a691b-133">选择此值之后，可能会收到以下消息：“承运人服务字段不是索引字段。</span><span class="sxs-lookup"><span data-stu-id="a691b-133">After you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="a691b-134">是否要为其添加排序？”</span><span class="sxs-lookup"><span data-stu-id="a691b-134">Do you want to add sorting on this?"</span></span> <span data-ttu-id="a691b-135">选择 **是** 添加排序。</span><span class="sxs-lookup"><span data-stu-id="a691b-135">Select **Yes** to add sorting.</span></span>

    - <span data-ttu-id="a691b-136">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="a691b-136">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="a691b-137">选择 **确定** 保存更改并关闭查询对话框。</span><span class="sxs-lookup"><span data-stu-id="a691b-137">Select **OK** to save your changes and close the query dialog box.</span></span>
1. <span data-ttu-id="a691b-138">在操作窗格上，选择 **波次模板分组**。</span><span class="sxs-lookup"><span data-stu-id="a691b-138">On the Action Pane, select **Wave template grouping**.</span></span>
1. <span data-ttu-id="a691b-139">根据需要在 **波次模板分组** 页面中，选中要用于将订单行分组为波次的每行的 **分组依据** 复选框。</span><span class="sxs-lookup"><span data-stu-id="a691b-139">On the **Wave template grouping** page, select the **Group by** check box for each row that you want to use to group your order lines into waves, as required.</span></span> <span data-ttu-id="a691b-140">如果准备使用演示数据完成此场景，请选中 *承运人服务* 行的 **分组依据** 复选框。</span><span class="sxs-lookup"><span data-stu-id="a691b-140">If you're preparing to work through the scenario by using demo data, select the **Group by** check box for the *Carrier service* row.</span></span>
1. <span data-ttu-id="a691b-141">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="a691b-141">Select **Save**.</span></span>
1. <span data-ttu-id="a691b-142">关闭 **波次模板分组** 页。</span><span class="sxs-lookup"><span data-stu-id="a691b-142">Close the **Wave template grouping** page.</span></span>
1. <span data-ttu-id="a691b-143">选择 **保存** 以保存您的模板。</span><span class="sxs-lookup"><span data-stu-id="a691b-143">Select **Save** to save your template.</span></span>

## <a name="scenario"></a><span data-ttu-id="a691b-144">应用场景</span><span class="sxs-lookup"><span data-stu-id="a691b-144">Scenario</span></span>

<span data-ttu-id="a691b-145">此部分提供脚本，可用于了解此功能执行的操作及其用法。</span><span class="sxs-lookup"><span data-stu-id="a691b-145">This section provides a script that you can work through to learn what this feature does and how to work with it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="a691b-146">提供示例数据</span><span class="sxs-lookup"><span data-stu-id="a691b-146">Make sample data available</span></span>

<span data-ttu-id="a691b-147">若要使用此处指定的示例记录和值完成此场景，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="a691b-147">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="a691b-148">此外，开始前，还必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="a691b-148">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="a691b-149">使用生产系统时，也可以将此场景用作使用此功能的指导。</span><span class="sxs-lookup"><span data-stu-id="a691b-149">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="a691b-150">但是，在此情况下，必须替换为您自己的值，而您可能会缺少标准演示数据提供的某些类型的必需记录。</span><span class="sxs-lookup"><span data-stu-id="a691b-150">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-wave-template-grouping"></a><span data-ttu-id="a691b-151">场景：波次模板分组</span><span class="sxs-lookup"><span data-stu-id="a691b-151">Scenario: Wave template grouping</span></span>

<span data-ttu-id="a691b-152">此场景显示如何使用波次模板分组功能根据波次模板中定义的分组条件自动创建多个波次。</span><span class="sxs-lookup"><span data-stu-id="a691b-152">This scenario shows how to use wave template grouping to automatically create multiple waves, based on grouping criteria that are defined in a wave template.</span></span> <span data-ttu-id="a691b-153">在此场景中，系统中将波次模板设置成为每个承运人服务创建一个波次。</span><span class="sxs-lookup"><span data-stu-id="a691b-153">In this scenario, the wave template is set up in the system to create one wave per carrier service.</span></span>

<span data-ttu-id="a691b-154">首先，按照本主题前面的[设置波次模板以使用波次模板分组功能](#set-up-template)部分中的介绍准备波次模板。</span><span class="sxs-lookup"><span data-stu-id="a691b-154">Before you begin, prepare your wave template as described in the [Set a wave template to use wave template grouping](#set-up-template) section earlier in this topic.</span></span> <span data-ttu-id="a691b-155">如果要为此场景使用演示数据，请务必使用该过程中推荐的演示数据值。</span><span class="sxs-lookup"><span data-stu-id="a691b-155">If you will be working with demo data for this scenario, be sure to use the demo data values that are suggested in that procedure.</span></span> <span data-ttu-id="a691b-156">此设置将根据为每个销售订单设置的承运人服务为波次分组。</span><span class="sxs-lookup"><span data-stu-id="a691b-156">This setup will group your waves according to the carrier service that is set for each sales order.</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="a691b-157">创建销售订单 1</span><span class="sxs-lookup"><span data-stu-id="a691b-157">Create sales order 1</span></span>

1. <span data-ttu-id="a691b-158">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="a691b-158">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a691b-159">选择 **新建** 以创建新的销售订单。</span><span class="sxs-lookup"><span data-stu-id="a691b-159">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="a691b-160">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="a691b-160">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a691b-161">在 **客户** 快速选项卡上，将 **客户帐户** 字段设置为 *US-004*。</span><span class="sxs-lookup"><span data-stu-id="a691b-161">On the **Customer** FastTab, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="a691b-162">在 **常规** 快速选项卡上，将 **仓库** 字段设置为 *62*。</span><span class="sxs-lookup"><span data-stu-id="a691b-162">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="a691b-163">选择 **确定** 创建销售订单，然后关闭 **创建销售订单** 对话框。</span><span class="sxs-lookup"><span data-stu-id="a691b-163">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="a691b-164">将在 **行** 视图中打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="a691b-164">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="a691b-165">记下销售订单编号。</span><span class="sxs-lookup"><span data-stu-id="a691b-165">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="a691b-166">切换到 **标题** 视图。</span><span class="sxs-lookup"><span data-stu-id="a691b-166">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="a691b-167">在 **交货** 快速选项卡的 **运输** 部分中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="a691b-167">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="a691b-168">**装运承运人**：*空运货物*</span><span class="sxs-lookup"><span data-stu-id="a691b-168">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="a691b-169">**承运人服务**：*航运*</span><span class="sxs-lookup"><span data-stu-id="a691b-169">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="a691b-170">切换回 **行** 视图。</span><span class="sxs-lookup"><span data-stu-id="a691b-170">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="a691b-171">在 **销售订单行** 部分中，选择 **添加行** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="a691b-171">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="a691b-172">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="a691b-172">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a691b-173">\**物料编号：\*\*\*A0002*</span><span class="sxs-lookup"><span data-stu-id="a691b-173">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="a691b-174">**数量：** *2*</span><span class="sxs-lookup"><span data-stu-id="a691b-174">**Quantity:** *2*</span></span>

1. <span data-ttu-id="a691b-175">选择新订单行，然后在网格上方的 **库存** 菜单中选择 **预留**。</span><span class="sxs-lookup"><span data-stu-id="a691b-175">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="a691b-176">在 **预留** 页中操作窗格上，选择 **预留批次** 在仓库中预留所选行的全部数量。</span><span class="sxs-lookup"><span data-stu-id="a691b-176">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="a691b-177">关闭 **预留** 页回到销售订单。</span><span class="sxs-lookup"><span data-stu-id="a691b-177">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="a691b-178">在“操作窗格”上的 **仓库** 选项卡上，在 **操作** 组中，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="a691b-178">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="a691b-179">将收到参考消息，其中显示该订单的装运和波次。</span><span class="sxs-lookup"><span data-stu-id="a691b-179">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="a691b-180">记下波次 ID 编号和装运 ID 编号。</span><span class="sxs-lookup"><span data-stu-id="a691b-180">Make a note of the wave ID number and the shipment ID numbers.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a><span data-ttu-id="a691b-181">查看从销售订单 1 创建的波次</span><span class="sxs-lookup"><span data-stu-id="a691b-181">View the wave that was created from sales order 1</span></span>

1. <span data-ttu-id="a691b-182">转到 **仓库管理 \> 出站波次 \> 装运波次 \> 所有波次**。</span><span class="sxs-lookup"><span data-stu-id="a691b-182">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="a691b-183">选择从销售订单创建的波次 ID。</span><span class="sxs-lookup"><span data-stu-id="a691b-183">Select the wave ID that was created from the sales order.</span></span>
1. <span data-ttu-id="a691b-184">选择波次 ID 链接打开波次详细信息页。</span><span class="sxs-lookup"><span data-stu-id="a691b-184">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="a691b-185">请注意，已经将装运添加到了 **波次行** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="a691b-185">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="a691b-186">创建销售订单 2</span><span class="sxs-lookup"><span data-stu-id="a691b-186">Create sales order 2</span></span>

1. <span data-ttu-id="a691b-187">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="a691b-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a691b-188">选择 **新建** 以创建新的销售订单。</span><span class="sxs-lookup"><span data-stu-id="a691b-188">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="a691b-189">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="a691b-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a691b-190">在 **客户** 快速选项卡上，将 **客户帐户** 字段设置为 *US-005*。</span><span class="sxs-lookup"><span data-stu-id="a691b-190">On the **Customer** FastTab, set the **Customer account** field to *US-005*.</span></span>
    - <span data-ttu-id="a691b-191">在 **常规** 快速选项卡上，将 **仓库** 字段设置为 *62*。</span><span class="sxs-lookup"><span data-stu-id="a691b-191">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="a691b-192">选择 **确定** 创建销售订单，然后关闭 **创建销售订单** 对话框。</span><span class="sxs-lookup"><span data-stu-id="a691b-192">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="a691b-193">将在 **行** 视图中打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="a691b-193">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="a691b-194">记下销售订单编号。</span><span class="sxs-lookup"><span data-stu-id="a691b-194">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="a691b-195">切换到 **标题** 视图。</span><span class="sxs-lookup"><span data-stu-id="a691b-195">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="a691b-196">在 **交货** 快速选项卡的 **运输** 部分中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="a691b-196">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="a691b-197">**装运承运人**：*运花*</span><span class="sxs-lookup"><span data-stu-id="a691b-197">**Shipping carrier:** *Flower moving*</span></span>
    - <span data-ttu-id="a691b-198">**承运人服务**：*标准*</span><span class="sxs-lookup"><span data-stu-id="a691b-198">**Carrier service:** *Std*</span></span>

1. <span data-ttu-id="a691b-199">切换回 **行** 视图。</span><span class="sxs-lookup"><span data-stu-id="a691b-199">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="a691b-200">在 **销售订单行** 部分中，选择 **添加行** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="a691b-200">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="a691b-201">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="a691b-201">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a691b-202">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="a691b-202">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="a691b-203">**数量：** *1*</span><span class="sxs-lookup"><span data-stu-id="a691b-203">**Quantity:** *1*</span></span>

1. <span data-ttu-id="a691b-204">选择新订单行，然后在网格上方的 **库存** 菜单中选择 **预留**。</span><span class="sxs-lookup"><span data-stu-id="a691b-204">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="a691b-205">在 **预留** 页中操作窗格上，选择 **预留批次** 在仓库中预留所选行的全部数量。</span><span class="sxs-lookup"><span data-stu-id="a691b-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="a691b-206">关闭 **预留** 页回到销售订单。</span><span class="sxs-lookup"><span data-stu-id="a691b-206">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="a691b-207">在“操作窗格”上的 **仓库** 选项卡上，在 **操作** 组中，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="a691b-207">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="a691b-208">将收到参考消息，其中显示该订单的装运和波次。</span><span class="sxs-lookup"><span data-stu-id="a691b-208">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="a691b-209">记下波次 ID 编号和装运 ID 编号。</span><span class="sxs-lookup"><span data-stu-id="a691b-209">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="a691b-210">请注意，此波次 ID 与第一个销售订单的波次 ID 不同。</span><span class="sxs-lookup"><span data-stu-id="a691b-210">Notice that the wave ID differs from the wave ID of the first sales order.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a><span data-ttu-id="a691b-211">查看从销售订单 2 创建的波次</span><span class="sxs-lookup"><span data-stu-id="a691b-211">View the wave that was created from sales order 2</span></span>

1. <span data-ttu-id="a691b-212">转到 **仓库管理 \> 出站波次 \> 装运波次 \> 所有波次**。</span><span class="sxs-lookup"><span data-stu-id="a691b-212">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="a691b-213">选择从第二个销售订单创建的波次 ID。</span><span class="sxs-lookup"><span data-stu-id="a691b-213">Select the wave ID that was created from the second sales order.</span></span>
1. <span data-ttu-id="a691b-214">选择波次 ID 链接打开波次详细信息页。</span><span class="sxs-lookup"><span data-stu-id="a691b-214">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="a691b-215">请注意，已经将装运添加到了 **波次行** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="a691b-215">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

<span data-ttu-id="a691b-216">为此装运创建了一个新波次，因为其使用的承运人服务与第一个销售订单使用的不同。</span><span class="sxs-lookup"><span data-stu-id="a691b-216">A new wave was created for this shipment, because it uses a different carrier service than the first sales order.</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="a691b-217">创建销售订单 3</span><span class="sxs-lookup"><span data-stu-id="a691b-217">Create sales order 3</span></span>

1. <span data-ttu-id="a691b-218">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="a691b-218">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a691b-219">选择 **新建** 以创建新的销售订单。</span><span class="sxs-lookup"><span data-stu-id="a691b-219">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="a691b-220">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="a691b-220">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a691b-221">在 **客户** 快速选项卡上，将 **客户帐户** 字段设置为 *US-006*。</span><span class="sxs-lookup"><span data-stu-id="a691b-221">On the **Customer** FastTab, set the **Customer account** field to *US-006*.</span></span>
    - <span data-ttu-id="a691b-222">在 **常规** 快速选项卡上，将 **仓库** 字段设置为 *62*。</span><span class="sxs-lookup"><span data-stu-id="a691b-222">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="a691b-223">选择 **确定** 创建销售订单，然后关闭 **创建销售订单** 对话框。</span><span class="sxs-lookup"><span data-stu-id="a691b-223">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="a691b-224">将在 **行** 视图中打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="a691b-224">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="a691b-225">记下销售订单编号。</span><span class="sxs-lookup"><span data-stu-id="a691b-225">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="a691b-226">切换到 **标题** 视图。</span><span class="sxs-lookup"><span data-stu-id="a691b-226">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="a691b-227">在 **交货** 快速选项卡的 **运输** 部分中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="a691b-227">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="a691b-228">**装运承运人**：*空运货物*</span><span class="sxs-lookup"><span data-stu-id="a691b-228">**Shipping carrier:** *Air Cargo*</span></span>
    - <span data-ttu-id="a691b-229">**承运人服务**：*航运*</span><span class="sxs-lookup"><span data-stu-id="a691b-229">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="a691b-230">切换回 **行** 视图。</span><span class="sxs-lookup"><span data-stu-id="a691b-230">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="a691b-231">在 **销售订单行** 部分中，选择 **添加行** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="a691b-231">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="a691b-232">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="a691b-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a691b-233">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="a691b-233">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="a691b-234">**数量：** *1*</span><span class="sxs-lookup"><span data-stu-id="a691b-234">**Quantity:** *1*</span></span>

1. <span data-ttu-id="a691b-235">选择新订单行，然后在网格上方的 **库存** 菜单中选择 **预留**。</span><span class="sxs-lookup"><span data-stu-id="a691b-235">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="a691b-236">在 **预留** 页中操作窗格上，选择 **预留批次** 在仓库中预留所选行的全部数量。</span><span class="sxs-lookup"><span data-stu-id="a691b-236">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="a691b-237">关闭 **预留** 页回到销售订单。</span><span class="sxs-lookup"><span data-stu-id="a691b-237">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="a691b-238">在“操作窗格”上的 **仓库** 选项卡上，在 **操作** 组中，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="a691b-238">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="a691b-239">将收到参考消息，其中显示该订单的装运和波次。</span><span class="sxs-lookup"><span data-stu-id="a691b-239">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="a691b-240">记下波次 ID 编号和装运 ID 编号。</span><span class="sxs-lookup"><span data-stu-id="a691b-240">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="a691b-241">已将装运分配给了第一个销售订单的现有波次。</span><span class="sxs-lookup"><span data-stu-id="a691b-241">The shipment has been assigned to the existing wave from the first sales order.</span></span>

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a><span data-ttu-id="a691b-242">查看销售订单 1 和 3 的波次</span><span class="sxs-lookup"><span data-stu-id="a691b-242">View the wave for sales orders 1 and 3</span></span>

1. <span data-ttu-id="a691b-243">转到 **仓库管理 \> 出站波次 \> 装运波次 \> 所有波次**。</span><span class="sxs-lookup"><span data-stu-id="a691b-243">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="a691b-244">选择从第三个销售订单创建的波次 ID。</span><span class="sxs-lookup"><span data-stu-id="a691b-244">Select the wave ID that was created from the third sales order.</span></span>
1. <span data-ttu-id="a691b-245">选择波次 ID 链接打开波次详细信息页。</span><span class="sxs-lookup"><span data-stu-id="a691b-245">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="a691b-246">请注意，已经将装运添加到了 **波次行** 快速选项卡，以及第一个销售订单的装运。</span><span class="sxs-lookup"><span data-stu-id="a691b-246">Notice that the shipment has been added to the **Wave lines** FastTab, together with the shipment for the first sales order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
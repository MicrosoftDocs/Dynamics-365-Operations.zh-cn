---
title: 从作业卡设备报告完工入库
description: 本主题介绍如何配置系统，以让作业卡设备的用户可以将生产订单中的成品报告到库存。
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403254"
---
# <a name="report-as-finished-from-the-job-card-device"></a><span data-ttu-id="407e7-103">从作业卡设备报告完工入库</span><span class="sxs-lookup"><span data-stu-id="407e7-103">Report as finished from the job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="407e7-104">工作人员使用作业卡设备上的**报告进度**页面报告生产作业已完成的数量。</span><span class="sxs-lookup"><span data-stu-id="407e7-104">Workers use the **Report progress** page on the job card device to report quantities that have been completed for a production job.</span></span>

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a><span data-ttu-id="407e7-105">控制是否将报告为完工入库的数量添加到库存中</span><span class="sxs-lookup"><span data-stu-id="407e7-105">Control whether quantities that are reported as finished are added to inventory</span></span>

<span data-ttu-id="407e7-106">若要控制是否以及如何将最后工序中报告为完工入库的数量添加到库存中，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="407e7-106">To control whether and how the quantities that are reported as finished on the last operation should be added to inventory, follow these steps.</span></span>

1. <span data-ttu-id="407e7-107">转到**产品控制 \> 设置 \> 制造执行 \> 生产订单默认值**。</span><span class="sxs-lookup"><span data-stu-id="407e7-107">Go to **Product control \> Setup \> Manufacturing execution \> Production order defaults**.</span></span>
1. <span data-ttu-id="407e7-108">在**完工入库**选项卡上，将**联机更新已完成的报告**字段设置为以下值之一：</span><span class="sxs-lookup"><span data-stu-id="407e7-108">On the **Report as finished** tab, set the **Update finished report on-line** field to one of the following values:</span></span>

    - <span data-ttu-id="407e7-109">**无** – 在最后工序中报告数量后，不会将任何数量添加到库存。</span><span class="sxs-lookup"><span data-stu-id="407e7-109">**No** – No quantity will be added to inventory when quantities are reported on the last operation.</span></span> <span data-ttu-id="407e7-110">生产订单的状态永远不会更改。</span><span class="sxs-lookup"><span data-stu-id="407e7-110">The status of the production order will never change.</span></span>
    - <span data-ttu-id="407e7-111">**状态 + 数量** – 生产订单的状态将更改为*完工入库*，数量将报告为已完工入库。</span><span class="sxs-lookup"><span data-stu-id="407e7-111">**Status + Quantity** – The status of the production order will change to *Reported as finished*, and the quantity will be reported as finished to inventory.</span></span>
    - <span data-ttu-id="407e7-112">**数量** – 数量将报告为已完工入库，但生产订单的状态永远不会更改。</span><span class="sxs-lookup"><span data-stu-id="407e7-112">**Quantity** – The quantity will be reported as finished to inventory, but the status of the production order will never change.</span></span>
    - <span data-ttu-id="407e7-113">**状态** – 仅生产订单的状态将更改。</span><span class="sxs-lookup"><span data-stu-id="407e7-113">**Status** – Only the status of the production order will change.</span></span> <span data-ttu-id="407e7-114">在最后工序中报告数量后，不会将任何数量添加到库存。</span><span class="sxs-lookup"><span data-stu-id="407e7-114">No quantities will be added to inventory when quantities are reported on the last operation.</span></span>

> [!NOTE]
> <span data-ttu-id="407e7-115">如果报告为完工入库的工序未定义为最后工序，将不会在库存中跟踪数量。</span><span class="sxs-lookup"><span data-stu-id="407e7-115">Quantities aren't tracked in inventory if the operations that they are reported as finished on aren't defined as the last operation.</span></span> <span data-ttu-id="407e7-116">但是，这些数量可用于查看进度。</span><span class="sxs-lookup"><span data-stu-id="407e7-116">However, those quantities can be used to view progress.</span></span> <span data-ttu-id="407e7-117">另外还可以包含在规则中，帮助控制工作人员是否可以在达到上一个工序报告数量的定义阈值之前开始下一个工序。</span><span class="sxs-lookup"><span data-stu-id="407e7-117">They can also be included in rules that control whether workers can start the next operation before a defined threshold of reported quantities on the previous operation is reached.</span></span> <span data-ttu-id="407e7-118">您可以在**生产订单默认值**页面的**数量验证**选项卡上定义这些规则。</span><span class="sxs-lookup"><span data-stu-id="407e7-118">You can define these rules on the **Quantity validation** tab of the **Production order defaults** page.</span></span>

<span data-ttu-id="407e7-119">有关如何使用**生产订单默认值**页面的详细信息，请参阅[制造执行中的生产参数](production-parameters-manufacturing-execution.md)。</span><span class="sxs-lookup"><span data-stu-id="407e7-119">For more information about how to work with the **Production order defaults** page, see [Production parameters in Manufacturing execution](production-parameters-manufacturing-execution.md).</span></span>

## <a name="report-batch-controlled-items-as-finished"></a><span data-ttu-id="407e7-120">将批次控制物料报告为完工入库</span><span class="sxs-lookup"><span data-stu-id="407e7-120">Report batch-controlled items as finished</span></span>

<span data-ttu-id="407e7-121">作业卡设备支持三种方案来报告批物料。</span><span class="sxs-lookup"><span data-stu-id="407e7-121">The job card device supports three scenarios for reporting on batch items.</span></span> <span data-ttu-id="407e7-122">这些方案既适用于高级仓库流程支持的物料，也适用于高级仓库流程不支持的物料。</span><span class="sxs-lookup"><span data-stu-id="407e7-122">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="407e7-123">**手动分配的批号：** 工作人员输入自定义批号。</span><span class="sxs-lookup"><span data-stu-id="407e7-123">**Manually assigned batch numbers:** Workers enter a custom batch number.</span></span> <span data-ttu-id="407e7-124">此批号可能来自系统未知的外部来源。</span><span class="sxs-lookup"><span data-stu-id="407e7-124">This batch number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="407e7-125">**预定义的批号：** 工作人员在生产订单下达到作业卡设备之前，系统自动生成的批号列表中选择一个批号。</span><span class="sxs-lookup"><span data-stu-id="407e7-125">**Predefined batch numbers:** Workers select a batch number in a list of batch numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="407e7-126">**固定批号：** 工作人员不输入或选择批号。</span><span class="sxs-lookup"><span data-stu-id="407e7-126">**Fixed batch numbers:** Workers don't enter or select a batch number.</span></span> <span data-ttu-id="407e7-127">系统会在生产订单下达之前自动向其分配批号。</span><span class="sxs-lookup"><span data-stu-id="407e7-127">Instead, the system automatically assigns a batch number to the production order before it's released.</span></span>

<span data-ttu-id="407e7-128">若要启用每个方案，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="407e7-128">To enable each scenario, follow these steps.</span></span>

1. <span data-ttu-id="407e7-129">转到**产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="407e7-129">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="407e7-130">选择要配置的产品。</span><span class="sxs-lookup"><span data-stu-id="407e7-130">Select the product to configure.</span></span>
1. <span data-ttu-id="407e7-131">在**管理库存**快速选项卡上，在**批号组**字段中，选择为支持您的方案而设置的跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="407e7-131">On the **Manage inventory** FastTab, in the **Batch number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="407e7-132">默认情况下，如果批号未分配给批次控制产品，作业卡设备将在报告完工入库期间为批号提供手动输入。</span><span class="sxs-lookup"><span data-stu-id="407e7-132">By default, if no batch number group is assigned to a batch-controlled product, the job card device provides manual entry for the batch number during reporting as finished.</span></span>

<span data-ttu-id="407e7-133">以下各小节介绍如何设置跟踪号组，以支持批次物料报告的三种方案。</span><span class="sxs-lookup"><span data-stu-id="407e7-133">The following subsections describe how to set up tracking number groups to support each of the three scenarios for reporting on batch items.</span></span>

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a><span data-ttu-id="407e7-134">在作业卡设备上启用批号报告</span><span class="sxs-lookup"><span data-stu-id="407e7-134">Enable batch number reporting on the job card device</span></span>

<span data-ttu-id="407e7-135">要让您的作业卡设备在报告完工入库过程中接受批号，您必须使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)启用以下功能（按此顺序）：</span><span class="sxs-lookup"><span data-stu-id="407e7-135">To enable your job card devices to accept a batch number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="407e7-136">改进的作业卡设备中“报告进度”对话框的用户体验</span><span class="sxs-lookup"><span data-stu-id="407e7-136">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="407e7-137">允许在从作业卡设备（预览）报告为完工入库时输入批号和序列号</span><span class="sxs-lookup"><span data-stu-id="407e7-137">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device (Preview)</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a><span data-ttu-id="407e7-138">设置让工作人员可以手动分配批号的跟踪号组</span><span class="sxs-lookup"><span data-stu-id="407e7-138">Set up a tracking number group that lets workers manually assign a batch number</span></span>

<span data-ttu-id="407e7-139">要允许手动分配批号，请按以下步骤设置跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="407e7-139">To allow for manually assigned batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="407e7-140">转到**库存管理 \> 设置 \> 维度 \> 跟踪号组**。</span><span class="sxs-lookup"><span data-stu-id="407e7-140">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="407e7-141">创建或选择要设置的跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="407e7-141">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="407e7-142">在**常规**快速选项卡上，将**手动**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="407e7-142">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="407e7-143">![跟踪号组页面](media/tracking-number-group-manual.png "跟踪号组页面")</span><span class="sxs-lookup"><span data-stu-id="407e7-143">![Tracking number groups page](media/tracking-number-group-manual.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="407e7-144">根据需要设置其他值，然后选择此跟踪号组作为要使用此方案的已发布产品的批号组。</span><span class="sxs-lookup"><span data-stu-id="407e7-144">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="407e7-145">使用此方案时，作业卡设备上的**报告进度**页面提供的**批号**字段是一个文本框，工作人员可以在其中输入任何值。</span><span class="sxs-lookup"><span data-stu-id="407e7-145">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value.</span></span>

<span data-ttu-id="407e7-146">![具有手动批号字段的报告进度页面](media/job-card-device-batch-manual.png "具有手动批处理号字段的报告进度页面")</span><span class="sxs-lookup"><span data-stu-id="407e7-146">![Report progress page with a field for manual batch numbers](media/job-card-device-batch-manual.png "Report progress page with a field for manual batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a><span data-ttu-id="407e7-147">设置提供预定义批号列表的跟踪号组</span><span class="sxs-lookup"><span data-stu-id="407e7-147">Set up a tracking number group that provides a list of predefined batch numbers</span></span>

<span data-ttu-id="407e7-148">要提供预定义批号列表，请按以下步骤设置跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="407e7-148">To provide a list of predefined batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="407e7-149">转到**库存管理 \> 设置 > 维度 \> 跟踪号组**。</span><span class="sxs-lookup"><span data-stu-id="407e7-149">Go to **Inventory management \> Setup > Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="407e7-150">创建或选择要设置的跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="407e7-150">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="407e7-151">在**常规**快速选项卡上，将**仅用于库存交易记录**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="407e7-151">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="407e7-152">使用**按数量**字段根据您输入的值按数量拆分批号。</span><span class="sxs-lookup"><span data-stu-id="407e7-152">Use the **Per qty.** field to split batch numbers per quantity, based on the value that you enter.</span></span> <span data-ttu-id="407e7-153">例如，您有一个十件产品的生产订单，**按数量**字段设置为 *2*。</span><span class="sxs-lookup"><span data-stu-id="407e7-153">For example, you have a production order for ten pieces, and the **Per qty.** field is set to *2*.</span></span> <span data-ttu-id="407e7-154">在这种情况下，将在生产订单创建时向其分配五个批号。</span><span class="sxs-lookup"><span data-stu-id="407e7-154">In this case, five batch numbers will be assigned to the production order when it's created.</span></span>

    <span data-ttu-id="407e7-155">![跟踪号组页面](media/tracking-number-group-predefined.png "跟踪号组页面")</span><span class="sxs-lookup"><span data-stu-id="407e7-155">![Tracking number groups page](media/tracking-number-group-predefined.png "The Tracking number groups page")</span></span>

1. <span data-ttu-id="407e7-156">根据需要设置其他值，然后选择此跟踪号组作为要使用此方案的已发布产品的批号组。</span><span class="sxs-lookup"><span data-stu-id="407e7-156">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="407e7-157">使用此方案时，作业卡设备上的**报告进度**页面提供的**批处理号**字段是一个下拉列表，工作人员必须在其中选择预定义值。</span><span class="sxs-lookup"><span data-stu-id="407e7-157">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="407e7-158">![具有预定义批号列表的报告进度页面](media/job-card-device-batch-predefined.png "具有预定义批号列表的报告进度页面")</span><span class="sxs-lookup"><span data-stu-id="407e7-158">![Report progress page with a list of predefined batch numbers](media/job-card-device-batch-predefined.png "Report progress page with a list of predefined batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a><span data-ttu-id="407e7-159">设置自动分配批号的跟踪号组</span><span class="sxs-lookup"><span data-stu-id="407e7-159">Set up a tracking number group that automatically assigns batch numbers</span></span>

<span data-ttu-id="407e7-160">如果应在没有工作人员输入的情况下自动分配批号，请按照以下步骤设置跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="407e7-160">If batch numbers should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="407e7-161">转到**库存管理 \> 设置 \> 维度 \> 跟踪号组**。</span><span class="sxs-lookup"><span data-stu-id="407e7-161">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="407e7-162">创建或选择要设置的跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="407e7-162">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="407e7-163">在**常规**快速选项卡上，将**仅用于库存交易记录**选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="407e7-163">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="407e7-164">将**手动**选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="407e7-164">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="407e7-165">![跟踪号组页面](media/tracking-number-group-fixed.png "跟踪号组页面")</span><span class="sxs-lookup"><span data-stu-id="407e7-165">![Tracking number groups page](media/tracking-number-group-fixed.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="407e7-166">根据需要设置其他值，然后选择此跟踪号组作为要使用此方案的已发布产品的批号组。</span><span class="sxs-lookup"><span data-stu-id="407e7-166">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="407e7-167">使用此方案时，作业卡设备上的**报告进度**页面提供的**批处理号**字段将显示一个值，但工作人员不能进行编辑。</span><span class="sxs-lookup"><span data-stu-id="407e7-167">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span>

<span data-ttu-id="407e7-168">![具有固定批号的报告进度页面](media/job-card-device-batch-fixed.png "具有固定批号的报告进度页面")</span><span class="sxs-lookup"><span data-stu-id="407e7-168">![Report progress page with a fixed batch number](media/job-card-device-batch-fixed.png "Report progress page with a fixed batch number")</span></span>

## <a name="report-as-finished-to-a-license-plate"></a><span data-ttu-id="407e7-169">报告为已完工入库到牌照</span><span class="sxs-lookup"><span data-stu-id="407e7-169">Report as finished to a license plate</span></span>

<span data-ttu-id="407e7-170">高级仓库流程可以使用牌照维度来跟踪为此目的设置的仓库位置的库存。</span><span class="sxs-lookup"><span data-stu-id="407e7-170">Advanced warehouse processes can use the license plate dimension to track inventory on warehouse locations that have been set up for this purpose.</span></span> <span data-ttu-id="407e7-171">在这种情况下，工作人员报告完工入库数量时需要牌照编号。</span><span class="sxs-lookup"><span data-stu-id="407e7-171">In this case, the license plate number is required when a worker reports quantities as finished.</span></span>

### <a name="enable-license-plate-reporting-and-label-printing"></a><span data-ttu-id="407e7-172">启用牌照报告和标签打印</span><span class="sxs-lookup"><span data-stu-id="407e7-172">Enable license plate reporting and label printing</span></span>

<span data-ttu-id="407e7-173">要使用本节介绍的功能，必须使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)启用以下功能（按此顺序）：</span><span class="sxs-lookup"><span data-stu-id="407e7-173">To use the features that are described in this section, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="407e7-174">用于报告为完工入库的牌照已添加作业卡设备</span><span class="sxs-lookup"><span data-stu-id="407e7-174">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="407e7-175">在作业卡设备中报告为完工入库时，启用牌照编号的自动生成</span><span class="sxs-lookup"><span data-stu-id="407e7-175">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>
1. <span data-ttu-id="407e7-176">从作业卡设备打印标签</span><span class="sxs-lookup"><span data-stu-id="407e7-176">Print label from Job Card Device</span></span>

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a><span data-ttu-id="407e7-177">设置报告为已完工入库到牌照</span><span class="sxs-lookup"><span data-stu-id="407e7-177">Set up reporting as finished to a license plate</span></span>

<span data-ttu-id="407e7-178">要控制工作人员在报告完工入库数量后是应该重用现有牌照还是生成新牌照，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="407e7-178">To control whether workers should reuse an existing license plate or generate a new license plate when they report quantities as finished, follow these steps.</span></span>

1. <span data-ttu-id="407e7-179">转到**生产控制 \> 设置 \> 制造执行 \> 为设备配置作业卡**。</span><span class="sxs-lookup"><span data-stu-id="407e7-179">Go to **Production control \> Setup \> Manufacturing execution \> Configure job card for devices**.</span></span>
2. <span data-ttu-id="407e7-180">为每个设备设置以下选项：</span><span class="sxs-lookup"><span data-stu-id="407e7-180">Set the following options for each device:</span></span>

    - <span data-ttu-id="407e7-181">**生成牌照** – 将此项设置为**是**将为每次报告完工入库生成新牌照。</span><span class="sxs-lookup"><span data-stu-id="407e7-181">**Generate license plate** – Set this option to **Yes** to generate a new license plate for each report as finished.</span></span> <span data-ttu-id="407e7-182">如果应为每次报告完工入库使用现有牌照，则设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="407e7-182">Set it to **No** if an existing license plate should be used for each report as finished.</span></span>
    - <span data-ttu-id="407e7-183">**打印标签** – 如果工作人员必须为每次报告完工入库打印牌照标签，将此项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="407e7-183">**Print label** – Set this option to **Yes** if the worker must print a license plate label for each report as finished.</span></span> <span data-ttu-id="407e7-184">如果不需要标签，则设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="407e7-184">Set it to **No** if no label is required.</span></span> 

<span data-ttu-id="407e7-185">![配置设备的作业卡页面](media/config-job-card-raf.png "配置设备的作业卡页面")</span><span class="sxs-lookup"><span data-stu-id="407e7-185">![Configure job card for devices page](media/config-job-card-raf.png "Configure job card for devices page")</span></span>

> [!NOTE]
> <span data-ttu-id="407e7-186">要配置标签，转到**仓库管理 \> 设置 \> 文档路径 \> 文档路径**。</span><span class="sxs-lookup"><span data-stu-id="407e7-186">To configure the label, go to **Warehouse management \> Setup \> Document routing \> Document routing**.</span></span> <span data-ttu-id="407e7-187">有关详细信息，请参阅[启用牌照标签打印](../warehousing/tasks/license-plate-label-printing.md)。</span><span class="sxs-lookup"><span data-stu-id="407e7-187">For more information, see [Enable license plate label printing](../warehousing/tasks/license-plate-label-printing.md).</span></span>

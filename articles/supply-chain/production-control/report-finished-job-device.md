---
title: 从作业卡设备报告完工入库
description: 本主题介绍如何配置系统，以让作业卡设备的用户可以将生产订单中的成品报告到库存。
author: johanhoffmann
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: bd21bdf532e1e607e66bb8f5ef032f0855c99612
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811622"
---
# <a name="report-as-finished-from-the-job-card-device"></a><span data-ttu-id="bba32-103">从作业卡设备报告完工入库</span><span class="sxs-lookup"><span data-stu-id="bba32-103">Report as finished from the job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bba32-104">工作人员使用作业卡设备上的 **报告进度** 页面报告生产作业已完成的数量。</span><span class="sxs-lookup"><span data-stu-id="bba32-104">Workers use the **Report progress** page on the job card device to report quantities that have been completed for a production job.</span></span> <span data-ttu-id="bba32-105">本主题介绍如何设置各个选项，来确立工作人员使用此页面报告完工入库的方法以及接下来要执行的事项。</span><span class="sxs-lookup"><span data-stu-id="bba32-105">This topic describes how to set up various options that establish how workers can report as finished using this page and what happens next.</span></span> <span data-ttu-id="bba32-106">选项包括：</span><span class="sxs-lookup"><span data-stu-id="bba32-106">Options include:</span></span>

- <span data-ttu-id="bba32-107">控制是否以及如何将报告为完工入库的数量添加到库存中。</span><span class="sxs-lookup"><span data-stu-id="bba32-107">Control whether and how quantities that are reported as finished are added to inventory.</span></span>
- <span data-ttu-id="bba32-108">控制在报告完工入库时是否以及如何生成和应用批号。</span><span class="sxs-lookup"><span data-stu-id="bba32-108">Control whether and how batch numbers are generated and applied when reporting as finished.</span></span>
- <span data-ttu-id="bba32-109">控制在报告完工入库时是否以及如何生成和应用序列号。</span><span class="sxs-lookup"><span data-stu-id="bba32-109">Control whether and how serial numbers are generated and applied when reporting as finished.</span></span>
- <span data-ttu-id="bba32-110">控制是否以及如何向牌照报告完工入库。</span><span class="sxs-lookup"><span data-stu-id="bba32-110">Control whether and how to report as finished to a license plate.</span></span>

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a><span data-ttu-id="bba32-111">控制是否将报告为完工入库的数量添加到库存中</span><span class="sxs-lookup"><span data-stu-id="bba32-111">Control whether quantities that are reported as finished are added to inventory</span></span>

<span data-ttu-id="bba32-112">若要控制是否以及如何将最后工序中报告为完工入库的数量添加到库存中，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="bba32-112">To control whether and how the quantities that are reported as finished on the last operation should be added to inventory, follow these steps.</span></span>

1. <span data-ttu-id="bba32-113">转到 **产品控制 \> 设置 \> 制造执行 \> 生产订单默认值**。</span><span class="sxs-lookup"><span data-stu-id="bba32-113">Go to **Product control \> Setup \> Manufacturing execution \> Production order defaults**.</span></span>
1. <span data-ttu-id="bba32-114">在 **完工入库** 选项卡上，将 **联机更新已完成的报告** 字段设置为以下值之一：</span><span class="sxs-lookup"><span data-stu-id="bba32-114">On the **Report as finished** tab, set the **Update finished report on-line** field to one of the following values:</span></span>

    - <span data-ttu-id="bba32-115">**无** – 在最后工序中报告数量后，不会将任何数量添加到库存。</span><span class="sxs-lookup"><span data-stu-id="bba32-115">**No** – No quantity will be added to inventory when quantities are reported on the last operation.</span></span> <span data-ttu-id="bba32-116">生产订单的状态永远不会更改。</span><span class="sxs-lookup"><span data-stu-id="bba32-116">The status of the production order will never change.</span></span>
    - <span data-ttu-id="bba32-117">**状态 + 数量** – 生产订单的状态将更改为 *完工入库*，数量将报告为已完工入库。</span><span class="sxs-lookup"><span data-stu-id="bba32-117">**Status + Quantity** – The status of the production order will change to *Reported as finished*, and the quantity will be reported as finished to inventory.</span></span>
    - <span data-ttu-id="bba32-118">**数量** – 数量将报告为已完工入库，但生产订单的状态永远不会更改。</span><span class="sxs-lookup"><span data-stu-id="bba32-118">**Quantity** – The quantity will be reported as finished to inventory, but the status of the production order will never change.</span></span>
    - <span data-ttu-id="bba32-119">**状态** – 仅生产订单的状态将更改。</span><span class="sxs-lookup"><span data-stu-id="bba32-119">**Status** – Only the status of the production order will change.</span></span> <span data-ttu-id="bba32-120">在最后工序中报告数量后，不会将任何数量添加到库存。</span><span class="sxs-lookup"><span data-stu-id="bba32-120">No quantities will be added to inventory when quantities are reported on the last operation.</span></span>

> [!NOTE]
> <span data-ttu-id="bba32-121">如果报告为完工入库的工序未定义为最后工序，将不会在库存中跟踪数量。</span><span class="sxs-lookup"><span data-stu-id="bba32-121">Quantities aren't tracked in inventory if the operations that they are reported as finished on aren't defined as the last operation.</span></span> <span data-ttu-id="bba32-122">但是，这些数量可用于查看进度。</span><span class="sxs-lookup"><span data-stu-id="bba32-122">However, those quantities can be used to view progress.</span></span> <span data-ttu-id="bba32-123">另外还可以包含在规则中，帮助控制工作人员是否可以在达到上一个工序报告数量的定义阈值之前开始下一个工序。</span><span class="sxs-lookup"><span data-stu-id="bba32-123">They can also be included in rules that control whether workers can start the next operation before a defined threshold of reported quantities on the previous operation is reached.</span></span> <span data-ttu-id="bba32-124">您可以在 **生产订单默认值** 页面的 **数量验证** 选项卡上定义这些规则。</span><span class="sxs-lookup"><span data-stu-id="bba32-124">You can define these rules on the **Quantity validation** tab on the **Production order defaults** page.</span></span>

<span data-ttu-id="bba32-125">有关如何使用 **生产订单默认值** 页面的详细信息，请参阅[制造执行中的生产参数](production-parameters-manufacturing-execution.md)。</span><span class="sxs-lookup"><span data-stu-id="bba32-125">For more information about how to work with the **Production order defaults** page, see [Production parameters in Manufacturing execution](production-parameters-manufacturing-execution.md).</span></span>

## <a name="report-batch-controlled-items-as-finished"></a><span data-ttu-id="bba32-126">将批次控制物料报告为完工入库</span><span class="sxs-lookup"><span data-stu-id="bba32-126">Report batch-controlled items as finished</span></span>

<span data-ttu-id="bba32-127">作业卡设备支持三种方案来报告批物料。</span><span class="sxs-lookup"><span data-stu-id="bba32-127">The job card device supports three scenarios for reporting on batch items.</span></span> <span data-ttu-id="bba32-128">这些方案既适用于高级仓库流程支持的物料，也适用于高级仓库流程不支持的物料。</span><span class="sxs-lookup"><span data-stu-id="bba32-128">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="bba32-129">**手动分配的批号** - 工作人员输入自定义批号。</span><span class="sxs-lookup"><span data-stu-id="bba32-129">**Manually assigned batch numbers** - Workers enter a custom batch number.</span></span> <span data-ttu-id="bba32-130">此批号可能来自系统未知的外部来源。</span><span class="sxs-lookup"><span data-stu-id="bba32-130">This batch number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="bba32-131">**预定义的批号** - 工作人员在生产订单下达到作业卡设备之前，系统自动生成的批号列表中选择一个批号。</span><span class="sxs-lookup"><span data-stu-id="bba32-131">**Predefined batch numbers** - Workers select a batch number in a list of batch numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="bba32-132">**固定批号** - 工作人员不输入或选择批号。</span><span class="sxs-lookup"><span data-stu-id="bba32-132">**Fixed batch numbers** - Workers don't enter or select a batch number.</span></span> <span data-ttu-id="bba32-133">系统会在生产订单下达之前自动向其分配批号。</span><span class="sxs-lookup"><span data-stu-id="bba32-133">Instead, the system automatically assigns a batch number to the production order before it's released.</span></span>


### <a name="enable-the-feature-on-your-system"></a><span data-ttu-id="bba32-134">在系统中启用此功能</span><span class="sxs-lookup"><span data-stu-id="bba32-134">Enable the feature on your system</span></span>

<span data-ttu-id="bba32-135">要让您的作业卡设备在报告完工入库过程中接受批号，您必须使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)启用以下功能（按此顺序）：</span><span class="sxs-lookup"><span data-stu-id="bba32-135">To enable your job card devices to accept a batch number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="bba32-136">改进的作业卡设备中“报告进度”对话框的用户体验</span><span class="sxs-lookup"><span data-stu-id="bba32-136">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="bba32-137">允许在从作业卡设备报告为完工入库时输入批号和序列号</span><span class="sxs-lookup"><span data-stu-id="bba32-137">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device</span></span>

### <a name="configure-products-that-require-batch-number-reporting"></a><span data-ttu-id="bba32-138">配置需要报告批号的产品</span><span class="sxs-lookup"><span data-stu-id="bba32-138">Configure products that require batch number reporting</span></span>

<span data-ttu-id="bba32-139">要使产品支持任何可用的批次控制方案，请按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="bba32-139">To enable a product to support any of the available batch-controlled scenarios, follow these steps:</span></span>

1. <span data-ttu-id="bba32-140">转到 **产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="bba32-140">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="bba32-141">选择要配置的产品。</span><span class="sxs-lookup"><span data-stu-id="bba32-141">Select the product to configure.</span></span>
1. <span data-ttu-id="bba32-142">在 **管理库存** 快速选项卡上，在 **批号组** 字段中，选择为支持您的方案而设置的跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-142">On the **Manage inventory** FastTab, in the **Batch number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="bba32-143">默认情况下，如果批号未分配给批次控制产品，作业卡设备将在报告完工入库期间为批号提供手动输入。</span><span class="sxs-lookup"><span data-stu-id="bba32-143">By default, if no batch number group is assigned to a batch-controlled product, the job card device provides manual entry for the batch number during reporting as finished.</span></span>

<span data-ttu-id="bba32-144">以下各节介绍如何设置跟踪号组，以支持批次物料报告的三种方案。</span><span class="sxs-lookup"><span data-stu-id="bba32-144">The following sections describe how to set up tracking number groups to support each of the three scenarios for reporting on batch items.</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a><span data-ttu-id="bba32-145">设置让工作人员可以手动分配批号的跟踪号组</span><span class="sxs-lookup"><span data-stu-id="bba32-145">Set up a tracking number group that lets workers manually assign a batch number</span></span>

<span data-ttu-id="bba32-146">要允许手动分配批号，请按以下步骤设置跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-146">To allow for manually assigned batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="bba32-147">转到 **库存管理 \> 设置 \> 维度 \> 跟踪号组**。</span><span class="sxs-lookup"><span data-stu-id="bba32-147">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="bba32-148">创建或选择要设置的跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-148">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="bba32-149">在 **常规** 快速选项卡上，将 **手动** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="bba32-149">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="bba32-150">![手动批号的跟踪号组](media/tracking-number-group-manual.png "手动批号的跟踪号组")</span><span class="sxs-lookup"><span data-stu-id="bba32-150">![A tracking number group for manual batch numbers](media/tracking-number-group-manual.png "A tracking number group for manual batch numbers")</span></span>

1. <span data-ttu-id="bba32-151">根据需要设置其他值，然后选择此跟踪号组作为要使用此方案的已发布产品的批号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-151">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="bba32-152">使用此方案时，作业卡设备上的 **报告进度** 页面提供的 **批号** 字段是一个文本框，工作人员可以在其中输入任何值。</span><span class="sxs-lookup"><span data-stu-id="bba32-152">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value.</span></span>

<span data-ttu-id="bba32-153">![具有手动批号字段的报告进度页面](media/job-card-device-batch-manual.png "具有手动批处理号字段的报告进度页面")</span><span class="sxs-lookup"><span data-stu-id="bba32-153">![Report progress page with a field for manual batch numbers](media/job-card-device-batch-manual.png "Report progress page with a field for manual batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a><span data-ttu-id="bba32-154">设置提供预定义批号列表的跟踪号组</span><span class="sxs-lookup"><span data-stu-id="bba32-154">Set up a tracking number group that provides a list of predefined batch numbers</span></span>

<span data-ttu-id="bba32-155">要提供预定义批号列表，请按以下步骤设置跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-155">To provide a list of predefined batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="bba32-156">转到 **库存管理 \> 设置 > 维度 \> 跟踪号组**。</span><span class="sxs-lookup"><span data-stu-id="bba32-156">Go to **Inventory management \> Setup > Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="bba32-157">创建或选择要设置的跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-157">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="bba32-158">在 **常规** 快速选项卡上，将 **仅用于库存交易记录** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="bba32-158">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="bba32-159">使用 **按数量** 字段根据您输入的值按数量拆分批号。</span><span class="sxs-lookup"><span data-stu-id="bba32-159">Use the **Per qty** field to split batch numbers per quantity, based on the value that you enter.</span></span> <span data-ttu-id="bba32-160">例如，您有一个十件产品的生产订单，**按数量** 字段设置为 *2*。</span><span class="sxs-lookup"><span data-stu-id="bba32-160">For example, you have a production order for ten pieces, and the **Per qty** field is set to *2*.</span></span> <span data-ttu-id="bba32-161">在这种情况下，将在生产订单创建时向其分配五个批号。</span><span class="sxs-lookup"><span data-stu-id="bba32-161">In this case, five batch numbers will be assigned to the production order when it's created.</span></span>

    <span data-ttu-id="bba32-162">![预定义批号的跟踪号组](media/tracking-number-group-predefined.png "预定义批号的跟踪号组")</span><span class="sxs-lookup"><span data-stu-id="bba32-162">![A tracking number group for predefined batch numbers](media/tracking-number-group-predefined.png "A tracking number group for predefined batch numbers")</span></span>

1. <span data-ttu-id="bba32-163">根据需要设置其他值，然后选择此跟踪号组作为要使用此方案的已发布产品的批号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-163">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="bba32-164">使用此方案时，作业卡设备上的 **报告进度** 页面提供的 **批处理号** 字段是一个下拉列表，工作人员必须在其中选择预定义值。</span><span class="sxs-lookup"><span data-stu-id="bba32-164">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="bba32-165">![具有预定义批号列表的报告进度页面](media/job-card-device-batch-predefined.png "具有预定义批号列表的报告进度页面")</span><span class="sxs-lookup"><span data-stu-id="bba32-165">![Report progress page with a list of predefined batch numbers](media/job-card-device-batch-predefined.png "Report progress page with a list of predefined batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a><span data-ttu-id="bba32-166">设置自动分配批号的跟踪号组</span><span class="sxs-lookup"><span data-stu-id="bba32-166">Set up a tracking number group that automatically assigns batch numbers</span></span>

<span data-ttu-id="bba32-167">如果应在没有工作人员输入的情况下自动分配批号，请按照以下步骤设置跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-167">If batch numbers should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="bba32-168">转到 **库存管理 \> 设置 \> 维度 \> 跟踪号组**。</span><span class="sxs-lookup"><span data-stu-id="bba32-168">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="bba32-169">创建或选择要设置的跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-169">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="bba32-170">在 **常规** 快速选项卡上，将 **仅用于库存交易记录** 选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="bba32-170">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="bba32-171">将 **手动** 选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="bba32-171">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="bba32-172">![固定批号的跟踪号组](media/tracking-number-group-fixed.png "固定批号的跟踪号组")</span><span class="sxs-lookup"><span data-stu-id="bba32-172">![A tracking number group for fixed batch numbers](media/tracking-number-group-fixed.png "A tracking number group for fixed batch numbers")</span></span>

1. <span data-ttu-id="bba32-173">根据需要设置其他值，然后选择此跟踪号组作为要使用此方案的已发布产品的批号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-173">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="bba32-174">使用此方案时，作业卡设备上的 **报告进度** 页面提供的 **批处理号** 字段将显示一个值，但工作人员不能进行编辑。</span><span class="sxs-lookup"><span data-stu-id="bba32-174">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span>

<span data-ttu-id="bba32-175">![具有固定批号的报告进度页面](media/job-card-device-batch-fixed.png "具有固定批号的报告进度页面")</span><span class="sxs-lookup"><span data-stu-id="bba32-175">![Report progress page with a fixed batch number](media/job-card-device-batch-fixed.png "Report progress page with a fixed batch number")</span></span>

## <a name="report-serial-controlled-items-as-finished"></a><span data-ttu-id="bba32-176">将序列控制物料报告为完工入库</span><span class="sxs-lookup"><span data-stu-id="bba32-176">Report serial-controlled items as finished</span></span>

<span data-ttu-id="bba32-177">作业卡设备支持三种方案来报告序列控制物料。</span><span class="sxs-lookup"><span data-stu-id="bba32-177">The job card device supports three scenarios for reporting on serial-controlled items.</span></span> <span data-ttu-id="bba32-178">这些方案既适用于高级仓库流程支持的物料，也适用于高级仓库流程不支持的物料。</span><span class="sxs-lookup"><span data-stu-id="bba32-178">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="bba32-179">**手动分配的序列号** - 工作人员输入自定义序列号。</span><span class="sxs-lookup"><span data-stu-id="bba32-179">**Manually assigned serial numbers** - Workers enter a custom serial number.</span></span> <span data-ttu-id="bba32-180">此序列号可能来自系统未知的外部来源。</span><span class="sxs-lookup"><span data-stu-id="bba32-180">This serial number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="bba32-181">**预定义序列号** - 工作人员在生产订单下达到作业卡设备之前，系统自动生成的序列号列表中选择一个序列号。</span><span class="sxs-lookup"><span data-stu-id="bba32-181">**Predefined serial numbers** - Workers select a serial number in a list of serial numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="bba32-182">**固定序列号** - 工作人员不输入或选择序列号。</span><span class="sxs-lookup"><span data-stu-id="bba32-182">**Fixed serial number** - Workers don't enter or select a serial number.</span></span> <span data-ttu-id="bba32-183">系统会在生产订单下达之前自动向其分配序列号。</span><span class="sxs-lookup"><span data-stu-id="bba32-183">Instead, the system automatically assigns a serial number to the production order before it's released.</span></span>

### <a name="enable-the-feature-on-your-system"></a><span data-ttu-id="bba32-184">在系统中启用此功能</span><span class="sxs-lookup"><span data-stu-id="bba32-184">Enable the feature on your system</span></span>

<span data-ttu-id="bba32-185">要让您的作业卡设备在报告完工入库过程中接受序列号，您必须使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)启用以下功能（按此顺序）：</span><span class="sxs-lookup"><span data-stu-id="bba32-185">To enable your job card devices to accept a serial number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="bba32-186">改进的作业卡设备中“报告进度”对话框的用户体验</span><span class="sxs-lookup"><span data-stu-id="bba32-186">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="bba32-187">允许在从作业卡设备报告为完工入库时输入批号和序列号</span><span class="sxs-lookup"><span data-stu-id="bba32-187">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device</span></span>

### <a name="configure-products-that-require-serial-number-reporting"></a><span data-ttu-id="bba32-188">配置需要报告序列号的产品</span><span class="sxs-lookup"><span data-stu-id="bba32-188">Configure products that require serial-number reporting</span></span>

<span data-ttu-id="bba32-189">要使产品支持任何可用的序列控制方案，请按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="bba32-189">To enable a product to support any of the available serial-controlled scenarios, follow these steps:</span></span>

<span data-ttu-id="bba32-190">若要启用每个方案，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="bba32-190">To enable each scenario, follow these steps.</span></span>

1. <span data-ttu-id="bba32-191">转到 **产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="bba32-191">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="bba32-192">选择要配置的产品。</span><span class="sxs-lookup"><span data-stu-id="bba32-192">Select the product to configure.</span></span>
1. <span data-ttu-id="bba32-193">在 **管理库存** 快速选项卡上，在 **序列号组** 字段中，选择为支持您的方案而设置的跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-193">On the **Manage inventory** FastTab, in the **Serial number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="bba32-194">默认情况下，如果序列号未分配给序列控制产品，作业卡设备将在报告完工入库期间为序列号提供手动输入。</span><span class="sxs-lookup"><span data-stu-id="bba32-194">By default, if no serial number group is assigned to a serial-controlled product, the job card device provides manual entry for the serial number during reporting as finished.</span></span>

<span data-ttu-id="bba32-195">以下各节介绍如何设置跟踪号组，以支持序列控制物料报告的三种方案。</span><span class="sxs-lookup"><span data-stu-id="bba32-195">The following sections describe how to set up tracking number groups to support each of the three scenarios for reporting on serial-controlled items.</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-serial-number"></a><span data-ttu-id="bba32-196">设置让工作人员可以手动分配序列号的跟踪号组</span><span class="sxs-lookup"><span data-stu-id="bba32-196">Set up a tracking number group that lets workers manually assign a serial number</span></span>

<span data-ttu-id="bba32-197">要允许手动分配序列号，请按以下步骤设置跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-197">To allow for manually assigned serial numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="bba32-198">转到 **库存管理 \> 设置 \> 维度 \> 跟踪号组**。</span><span class="sxs-lookup"><span data-stu-id="bba32-198">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="bba32-199">创建或选择要设置的跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-199">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="bba32-200">在 **常规** 快速选项卡上，将 **手动** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="bba32-200">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="bba32-201">![跟踪号组页面，序列号](media/tracking-number-group-manual-serial.png "跟踪号组页面，序列号")</span><span class="sxs-lookup"><span data-stu-id="bba32-201">![Tracking number groups page, serial numbers](media/tracking-number-group-manual-serial.png "Tracking number groups page, serial numbers")</span></span>

1. <span data-ttu-id="bba32-202">根据需要设置其他值，然后选择此跟踪号组作为要使用此方案的已发布产品的序列号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-202">Set other values as you require, and then select this tracking number group as the serial number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="bba32-203">使用此方案时，作业卡设备上的 **报告进度** 页面提供的 **序列号** 字段是一个文本框，工作人员可以在其中输入任何序列号值。</span><span class="sxs-lookup"><span data-stu-id="bba32-203">When you use this scenario, the **Serial number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value for the serial number.</span></span> <span data-ttu-id="bba32-204">输入值后，它将被添加到序列号列表中。</span><span class="sxs-lookup"><span data-stu-id="bba32-204">On entering a value, it is added to the serial number list.</span></span> <span data-ttu-id="bba32-205">在此列表中，工作人员可以执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="bba32-205">In this list,  workers can do the following:</span></span>

- <span data-ttu-id="bba32-206">要将序列号标记为报废，请选择相应行的 **报废** 按钮。</span><span class="sxs-lookup"><span data-stu-id="bba32-206">To mark a serial number as scrapped, select the **Scrap** button for the appropriate row.</span></span> <span data-ttu-id="bba32-207">系统将提示工作人员提供 **错误原因**。</span><span class="sxs-lookup"><span data-stu-id="bba32-207">The worker will be prompted to provide an **Error cause**.</span></span>
- <span data-ttu-id="bba32-208">要删除序列号，请选择相应行的 **删除** 按钮。</span><span class="sxs-lookup"><span data-stu-id="bba32-208">To delete a serial number, select the **Delete** button for the appropriate row.</span></span>

<span data-ttu-id="bba32-209">![具有手动序列号字段的报告进度页面](media/job-card-device-serial-manual.png "具有手动序列号字段的报告进度页面")</span><span class="sxs-lookup"><span data-stu-id="bba32-209">![Report progress page with a field for manual serial numbers](media/job-card-device-serial-manual.png "Report progress page with a field for manual serial numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-serial-numbers"></a><span data-ttu-id="bba32-210">设置提供预定义序列号列表的跟踪号组</span><span class="sxs-lookup"><span data-stu-id="bba32-210">Set up a tracking number group that provides a list of predefined serial numbers</span></span>

<span data-ttu-id="bba32-211">要提供预定义序列号列表，请按以下步骤设置跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-211">To provide a list of predefined serial numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="bba32-212">转到 **库存管理 \> 设置 \> 维度 \> 跟踪号组**。</span><span class="sxs-lookup"><span data-stu-id="bba32-212">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="bba32-213">创建或选择要设置的跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-213">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="bba32-214">在 **常规** 快速选项卡上，将 **仅用于库存交易记录** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="bba32-214">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="bba32-215">使用 **按数量** 字段按数量一拆分序列号。</span><span class="sxs-lookup"><span data-stu-id="bba32-215">Use the **Per qty** field to split serial numbers per quantity of one.</span></span>

    <span data-ttu-id="bba32-216">![预定义序列号的跟踪号组](media/tracking-number-group-predefined-sn.png "预定义序列号的跟踪号组")</span><span class="sxs-lookup"><span data-stu-id="bba32-216">![A tracking number group for predefined serial numbers](media/tracking-number-group-predefined-sn.png "A tracking number group for predefined serial numbers")</span></span>

1. <span data-ttu-id="bba32-217">根据需要设置其他值，然后选择此跟踪号组作为要使用此方案的已发布产品的序列号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-217">Set other values as you require, and then select this tracking number group as the serial number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="bba32-218">使用此方案时，作业卡设备上的 **报告进度** 页面提供的 **序列号** 字段是一个下拉列表，工作人员必须在其中选择预定义值。</span><span class="sxs-lookup"><span data-stu-id="bba32-218">When you use this scenario, the **Serial number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="bba32-219">![具有预定义序列号列表的报告进度页面](media/job-card-device-serial-predefined.png "具有预定义序列号列表的报告进度页面")</span><span class="sxs-lookup"><span data-stu-id="bba32-219">![Report progress page with a list of predefined serial numbers](media/job-card-device-serial-predefined.png "Report progress page with a list of predefined serial numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-serial-numbers"></a><span data-ttu-id="bba32-220">设置自动分配序列号的跟踪号组</span><span class="sxs-lookup"><span data-stu-id="bba32-220">Set up a tracking number group that automatically assigns serial numbers</span></span>

<span data-ttu-id="bba32-221">如果应在没有工作人员输入的情况下自动分配序列号，请按照以下步骤设置跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-221">If a serial number should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="bba32-222">转到 **库存管理 \> 设置 \> 维度 \> 跟踪号组**。</span><span class="sxs-lookup"><span data-stu-id="bba32-222">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="bba32-223">创建或选择要设置的跟踪号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-223">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="bba32-224">在 **常规** 快速选项卡上，将 **仅用于库存交易记录** 选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="bba32-224">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="bba32-225">将 **手动** 选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="bba32-225">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="bba32-226">![固定序列号的跟踪号组](media/tracking-number-group-fixed-sn.png "固定序列号的跟踪号组")</span><span class="sxs-lookup"><span data-stu-id="bba32-226">![A tracking number group for fixed serial numbers](media/tracking-number-group-fixed-sn.png "A tracking number group for fixed serial numbers")</span></span>

1. <span data-ttu-id="bba32-227">根据需要设置其他值，然后选择此跟踪号组作为要使用此方案的已发布产品的序列号组。</span><span class="sxs-lookup"><span data-stu-id="bba32-227">Set other values as you require, and then select this tracking number group as the serial number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="bba32-228">使用此方案时，作业卡设备上的 **报告进度** 页面提供的 **序列号** 字段将显示一个值，但工作人员不能进行编辑。</span><span class="sxs-lookup"><span data-stu-id="bba32-228">When you use this scenario, the **Serial number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span> <span data-ttu-id="bba32-229">此方案仅在为数量为一件序列号控制物料创建生产订单时有用。</span><span class="sxs-lookup"><span data-stu-id="bba32-229">This scenario is only relevant when a production order is created for a quantity of one piece of a serial number-controlled item.</span></span>

<span data-ttu-id="bba32-230">![具有固定序列号的报告进度页面](media/job-card-device-serial-fixed.png "具有固定序列号的报告进度页面")</span><span class="sxs-lookup"><span data-stu-id="bba32-230">![Report progress page with a fixed serial number](media/job-card-device-serial-fixed.png "Report progress page with a fixed serial numbers")</span></span>

## <a name="report-as-finished-to-a-license-plate"></a><span data-ttu-id="bba32-231">报告为已完工入库到牌照</span><span class="sxs-lookup"><span data-stu-id="bba32-231">Report as finished to a license plate</span></span>

<span data-ttu-id="bba32-232">高级仓库流程可以使用牌照维度来跟踪为此目的设置的仓库位置的库存。</span><span class="sxs-lookup"><span data-stu-id="bba32-232">Advanced warehouse processes can use the license plate dimension to track inventory on warehouse locations that have been set up for this purpose.</span></span> <span data-ttu-id="bba32-233">在这种情况下，工作人员报告完工入库数量时需要牌照编号。</span><span class="sxs-lookup"><span data-stu-id="bba32-233">In this case, the license plate number is required when a worker reports quantities as finished.</span></span>

### <a name="enable-license-plate-reporting-and-label-printing"></a><span data-ttu-id="bba32-234">启用牌照报告和标签打印</span><span class="sxs-lookup"><span data-stu-id="bba32-234">Enable license plate reporting and label printing</span></span>

<span data-ttu-id="bba32-235">要使用本节介绍的功能，必须使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)启用以下功能（按此顺序）：</span><span class="sxs-lookup"><span data-stu-id="bba32-235">To use the features that are described in this section, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="bba32-236">用于报告为完工入库的牌照已添加作业卡设备</span><span class="sxs-lookup"><span data-stu-id="bba32-236">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="bba32-237">在作业卡设备中报告为完工入库时，启用牌照编号的自动生成</span><span class="sxs-lookup"><span data-stu-id="bba32-237">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>
1. <span data-ttu-id="bba32-238">从作业卡设备打印标签</span><span class="sxs-lookup"><span data-stu-id="bba32-238">Print label from Job Card Device</span></span>

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a><span data-ttu-id="bba32-239">设置报告为已完工入库到牌照</span><span class="sxs-lookup"><span data-stu-id="bba32-239">Set up reporting as finished to a license plate</span></span>

<span data-ttu-id="bba32-240">要控制工作人员在报告完工入库数量后是应该重用现有牌照还是生成新牌照，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="bba32-240">To control whether workers should reuse an existing license plate or generate a new license plate when they report quantities as finished, follow these steps.</span></span>

1. <span data-ttu-id="bba32-241">转到 **生产控制 \> 设置 \> 制造执行 \> 为设备配置作业卡**。</span><span class="sxs-lookup"><span data-stu-id="bba32-241">Go to **Production control \> Setup \> Manufacturing execution \> Configure job card for devices**.</span></span>
2. <span data-ttu-id="bba32-242">为每个设备设置以下选项：</span><span class="sxs-lookup"><span data-stu-id="bba32-242">Set the following options for each device:</span></span>

    - <span data-ttu-id="bba32-243">**生成牌照** – 将此项设置为 **是** 将为每次报告完工入库生成新牌照。</span><span class="sxs-lookup"><span data-stu-id="bba32-243">**Generate license plate** – Set this option to **Yes** to generate a new license plate for each report as finished.</span></span> <span data-ttu-id="bba32-244">如果应为每次报告完工入库使用现有牌照，则设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="bba32-244">Set it to **No** if an existing license plate should be used for each report as finished.</span></span>
    - <span data-ttu-id="bba32-245">**打印标签** – 如果工作人员必须为每次报告完工入库打印牌照标签，将此项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="bba32-245">**Print label** – Set this option to **Yes** if the worker must print a license plate label for each report as finished.</span></span> <span data-ttu-id="bba32-246">如果不需要标签，则设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="bba32-246">Set it to **No** if no label is required.</span></span> 

<span data-ttu-id="bba32-247">![配置设备的作业卡页面](media/config-job-card-raf.png "配置设备的作业卡页面")</span><span class="sxs-lookup"><span data-stu-id="bba32-247">![Configure job card for devices page](media/config-job-card-raf.png "Configure job card for devices page")</span></span>

> [!NOTE]
> <span data-ttu-id="bba32-248">要配置标签，转到 **仓库管理 \> 设置 \> 文档路径 \> 文档路径**。</span><span class="sxs-lookup"><span data-stu-id="bba32-248">To configure the label, go to **Warehouse management \> Setup \> Document routing \> Document routing**.</span></span> <span data-ttu-id="bba32-249">有关详细信息，请参阅[启用牌照标签打印](../warehousing/tasks/license-plate-label-printing.md)。</span><span class="sxs-lookup"><span data-stu-id="bba32-249">For more information, see [Enable license plate label printing](../warehousing/tasks/license-plate-label-printing.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
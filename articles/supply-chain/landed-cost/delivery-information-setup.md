---
title: 交货信息设置
description: 本主题介绍如何为登陆成本模块设置交货信息。
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMPortTable, ITMLeadTimeTable, ITMLegTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 4cb1207916c40a18cf5b295baa913ae2d7198a05
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841883"
---
# <a name="delivery-information-setup"></a><span data-ttu-id="dfbbd-103">交货信息设置</span><span class="sxs-lookup"><span data-stu-id="dfbbd-103">Delivery information setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dfbbd-104">本主题介绍如何为 **登陆成本** 模块设置交货信息。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-104">This topic describes how to set up delivery information for the **Landed cost** module.</span></span>

## <a name="shipping-ports"></a><span data-ttu-id="dfbbd-105">装运港口</span><span class="sxs-lookup"><span data-stu-id="dfbbd-105">Shipping ports</span></span>

<span data-ttu-id="dfbbd-106">装运港口确定货物发运和到达的地点。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-106">Shipping ports identify where goods are being shipped from and to.</span></span> <span data-ttu-id="dfbbd-107">对于每个航行，基于为航行船只选择的行程定义“到达”港口和“发运”港口。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-107">For each voyage, a "to" port and a "from" port are defined, based on the journey that is selected for the voyage vessel.</span></span> <span data-ttu-id="dfbbd-108">装运港口用于建立行程的支线以及航行活动。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-108">Shipping ports are used to build the legs of a journey and also the voyage activities.</span></span> <span data-ttu-id="dfbbd-109">它们通常使用实际装运港口所在的城市以及国家或地区的名称来定义。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-109">They are typically defined by using the name of the city and the country or region where the physical shipping port is located.</span></span>

<span data-ttu-id="dfbbd-110">要使用装运港口，请转到 **登陆成本 \> 交货信息设置 \> 装运港口**。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-110">To work with shipping ports, go to **Landed cost \> Delivery information setup \> Shipping ports**.</span></span> <span data-ttu-id="dfbbd-111">您可以在那里查看、添加和删除装运港口的记录。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-111">There, you can view, add, and remove records for your shipping ports.</span></span> <span data-ttu-id="dfbbd-112">下表说明了可用于每个记录的字段。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-112">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="dfbbd-113">字段</span><span class="sxs-lookup"><span data-stu-id="dfbbd-113">Field</span></span> | <span data-ttu-id="dfbbd-114">说明</span><span class="sxs-lookup"><span data-stu-id="dfbbd-114">Description</span></span> |
|---|---|
| <span data-ttu-id="dfbbd-115">装运港口</span><span class="sxs-lookup"><span data-stu-id="dfbbd-115">Shipping port</span></span> | <span data-ttu-id="dfbbd-116">为装运港口输入唯一标识名称/编号。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-116">Enter a unique identification name/number for the shipping port.</span></span> |
| <span data-ttu-id="dfbbd-117">说明</span><span class="sxs-lookup"><span data-stu-id="dfbbd-117">Description</span></span> | <span data-ttu-id="dfbbd-118">输入装运港口的描述。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-118">Enter a description of the shipping port.</span></span> |

## <a name="tracking-control-center"></a><a name="tracking-control-center"></a><span data-ttu-id="dfbbd-119">跟踪控制中心</span><span class="sxs-lookup"><span data-stu-id="dfbbd-119">Tracking control center</span></span>

<span data-ttu-id="dfbbd-120">当装运集装箱从一个支线到达下一个支线时，您使用跟踪控制中心来设置与航行关联的提前期、状态更新和信息流。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-120">You use the Tracking control center to set up the lead times, status updates, and flow of information that is associated with a voyage as the shipping containers move from one leg to the next.</span></span> <span data-ttu-id="dfbbd-121">创建跟踪控制记录时，它将与航行行程的特定支线关联。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-121">When you create a tracking control record, it's associated with a specific leg of a journey for a voyage.</span></span> <span data-ttu-id="dfbbd-122">将航行更新支线时，关联的记录将按定义更新和填充。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-122">When a voyage updates a leg, the associated record will be updated and filled in as defined.</span></span> <span data-ttu-id="dfbbd-123">您可以从 **所有航行** 页更新各个航行的跟踪信息。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-123">You can update tracking information for individual voyages from the **All voyages** page.</span></span>

<span data-ttu-id="dfbbd-124">要打开跟踪控制中心，请转到 **登陆成本 \> 交货信息设置 \> 跟踪控制中心**。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-124">To open the Tracking control center, go to **Landed cost \> Delivery information setup \> Tracking control center**.</span></span>

<span data-ttu-id="dfbbd-125">跟踪控制中心显示三个页面视图之一，具体取决于在列表窗格的 **创建类型** 字段中选择的值：*空白*、*提前期* 或 *状态更新*。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-125">The Tracking control center shows one of three page views, depending on the value that is selected in the **Create type** field in the list pane: *Blank*, *Lead time*, or *Status update*.</span></span> <span data-ttu-id="dfbbd-126">每个创建类型将更新一组不同的信息，这些信息与从起始点到最终目的地的航行的进度关联。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-126">Each create type updates a different set of information that is associated with the progress of a voyage from the point of origin to the final destination.</span></span>

### <a name="common-rule-settings"></a><span data-ttu-id="dfbbd-127">通用规则设置</span><span class="sxs-lookup"><span data-stu-id="dfbbd-127">Common rule settings</span></span>

<span data-ttu-id="dfbbd-128">下表显示了跟踪控制中心中可用于所有三个创建类型的字段。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-128">The following table shows the fields that are available for all three create types in the Tracking control center.</span></span>

| <span data-ttu-id="dfbbd-129">字段</span><span class="sxs-lookup"><span data-stu-id="dfbbd-129">Field</span></span> | <span data-ttu-id="dfbbd-130">说明</span><span class="sxs-lookup"><span data-stu-id="dfbbd-130">Description</span></span> |
|---|---|
| <span data-ttu-id="dfbbd-131">源表、源字段</span><span class="sxs-lookup"><span data-stu-id="dfbbd-131">Source table, Source field</span></span> | <span data-ttu-id="dfbbd-132">这些字段确定数据库中的源表和字段。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-132">These fields identify a source table and field in the database.</span></span> <span data-ttu-id="dfbbd-133">规则将在字段中加载值，然后以规则的其他设置定义的方式使用它。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-133">The rule will load the value in the field and then use it in the way that is defined by other settings of the rule.</span></span> |
| <span data-ttu-id="dfbbd-134">目标表、目标字段</span><span class="sxs-lookup"><span data-stu-id="dfbbd-134">Target table, Target field</span></span> | <span data-ttu-id="dfbbd-135">这些字段确定数据库中的目标表和字段。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-135">These fields identify a destination table and field in the database.</span></span> <span data-ttu-id="dfbbd-136">规则将在字段中加载值，然后以规则的其他设置定义的方式使用它（或覆盖）。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-136">The rule will load the value in the field and then use it (or overwrite it) in the way that is defined by other settings of the rule.</span></span> |
| <span data-ttu-id="dfbbd-137">活动</span><span class="sxs-lookup"><span data-stu-id="dfbbd-137">Activity</span></span> | <span data-ttu-id="dfbbd-138">此字段确定应该应用于规则匹配的装运集装箱的活动类型。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-138">This field identifies the type of activity that should be applied to a shipping container that is matched by a rule.</span></span> |
| <span data-ttu-id="dfbbd-139">匹配条件</span><span class="sxs-lookup"><span data-stu-id="dfbbd-139">Matching criteria</span></span> | <span data-ttu-id="dfbbd-140">此字段确定系统如何确定规则的匹配项。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-140">This field determines how the system identifies a match for a rule.</span></span> <span data-ttu-id="dfbbd-141">在每种情况下，系统会检查源表和目标表中的数据，以确定是否应该以及何时在目标表中更新某个字段。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-141">In each instance, the system reviews the data in the source and destination tables to determine whether and when a field should be updated in the target table.</span></span><p><span data-ttu-id="dfbbd-142">例如，源表是 *航行*，目标表是 *采购订单头* 或 *采购订单行*。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-142">For example, the source table is *Voyages*, and the target table is *Purchase header* or *Purchase lines*.</span></span> <span data-ttu-id="dfbbd-143">*航行* 表的 **发运港口** 值为 *香港特别行政区*，*采购订单头* 表的 **发运港口** 值为 *上海*。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-143">The *Voyages* table has a **From port** value of *Hong Kong*, and the *Purchase header* table has a **From port** value of *Shanghai*.</span></span> <span data-ttu-id="dfbbd-144">然后一个规则将创建，将 *香港特别行政区* 作为“发运”港口。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-144">A rule is then created that has *Hong Kong* as the "from" port.</span></span> <span data-ttu-id="dfbbd-145">在这种情况下，**匹配条件** 字段的值将以以下方式工作：</span><span class="sxs-lookup"><span data-stu-id="dfbbd-145">In this case, the values of the **Matching criteria** field will work in the following way:</span></span></p><ul><li><span data-ttu-id="dfbbd-146">**二者** – 目标字段不会更新，因为两个港口中有一个不匹配。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-146">**Both** – The target field won't be updated, because one of the two ports don't match.</span></span></li><li><span data-ttu-id="dfbbd-147">**源** – 目标字段将更新，因为源表的“发运”港口为 *香港特别行政区*。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-147">**Source** – The target field will be updated, because the source table's "from" port is *Hong Kong*.</span></span></li><li><span data-ttu-id="dfbbd-148">**目标** – 目标字段不会更新，因为目标表的“发运”港口为 *上海*（不是 *香港特别行政区*）。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-148">**Target** – The target field won't be updated, because the destination table's "from" port is *Shanghai* (not *Hong Kong*).</span></span></li></ul> |
| <span data-ttu-id="dfbbd-149">复制操作</span><span class="sxs-lookup"><span data-stu-id="dfbbd-149">Copy action</span></span> | <span data-ttu-id="dfbbd-150">可用值为 *复制* 和 *默认*。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-150">The available values are *Copy* and *Default*.</span></span> <span data-ttu-id="dfbbd-151">选择 *复制* 可将源字段中的值复制到目标字段。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-151">Select *Copy* to copy the value in the source field to the destination field.</span></span> <span data-ttu-id="dfbbd-152">选择 *默认* 可为目标字段设置静态值。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-152">Select *Default* to set a static value for the destination field.</span></span> |
| <span data-ttu-id="dfbbd-153">默认值</span><span class="sxs-lookup"><span data-stu-id="dfbbd-153">Default</span></span> | <span data-ttu-id="dfbbd-154">当 **复制操作** 字段设置为 *默认* 时，**默认** 字段定义目标字段的默认值。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-154">When the **Copy action** field is set to *Default*, the **Default** field defines the default value of the destination field.</span></span> <span data-ttu-id="dfbbd-155">例如，如果操作与港口更新相关，并且 **复制操作** 字段设置为 *默认*，**默认** 字段将确定港口。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-155">For example, if the action is related to a port update, and the **Copy action** field is set to *Default*, the **Default** field identifies a port.</span></span> |
| <span data-ttu-id="dfbbd-156">支线</span><span class="sxs-lookup"><span data-stu-id="dfbbd-156">Leg</span></span> | <span data-ttu-id="dfbbd-157">此字段确定发生指定操作（如装载或报关）的行程的支线。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-157">This field identifies the leg of the journey that the specified action occurs for, such as loading or customs.</span></span> |
| <span data-ttu-id="dfbbd-158">服务提供商</span><span class="sxs-lookup"><span data-stu-id="dfbbd-158">Service provider</span></span> | <span data-ttu-id="dfbbd-159">如果特定服务提供商用于行程的当前状态更新/支线，此字段确定服务提供商。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-159">If a specific service provider is used for the current status update/leg of the journey, this field identifies the service provider.</span></span> <span data-ttu-id="dfbbd-160">服务提供商在供应商帐户中定义。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-160">Service providers are defined in the vendor account.</span></span> |

### <a name="lead-time-rules"></a><span data-ttu-id="dfbbd-161">提前期规则</span><span class="sxs-lookup"><span data-stu-id="dfbbd-161">Lead time rules</span></span>

<span data-ttu-id="dfbbd-162">提前期是指完成航行行程的一个定义的支线，航行所需的估计时间。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-162">The lead time is the estimated time that a voyage will require to complete a defined leg of a journey for a voyage.</span></span> <span data-ttu-id="dfbbd-163">行程每个支线的提前期用于计算航行的估计交货日期。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-163">The lead time of each leg of a journey is used to calculate the estimated delivery date of the voyage.</span></span> <span data-ttu-id="dfbbd-164">该日期然后将输入到航行中每个采购订单行上的 **确认交货日期** 字段。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-164">That date is then entered in the **Confirmed delivery date** field on every purchase line in the voyage.</span></span>

<span data-ttu-id="dfbbd-165">您使用提前期规则来管理日期的更新。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-165">You use lead time rules to manage updates of dates.</span></span> <span data-ttu-id="dfbbd-166">当行程模板用于航行时，活动将自动生成。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-166">Activities are automatically generated when a journey template is used for a voyage.</span></span>

<span data-ttu-id="dfbbd-167">要将提前期规则添加到跟踪控制中心，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-167">To add a lead time rule to the Tracking control center, follow these steps.</span></span>

1. <span data-ttu-id="dfbbd-168">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="dfbbd-168">Follow one of these steps:</span></span>

    - <span data-ttu-id="dfbbd-169">转到 **登陆成本 \> 多支线行程设置 \> 支线**。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-169">Go to **Landed cost \> Multi-leg journey setup \> Legs**.</span></span> <span data-ttu-id="dfbbd-170">选择要为其设置提前期的支线，然后在操作窗格上选择 **跟踪控制中心**。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-170">Select the leg that you want to set up lead times for, and then, on the Action Pane, select **Tracking control center**.</span></span> <span data-ttu-id="dfbbd-171">跟踪控制中心已预加载有关选定支线的信息。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-171">The Tracking control center is preloaded with information about the selected leg.</span></span>
    - <span data-ttu-id="dfbbd-172">转到 **登陆成本 \> 交货信息设置 \> 跟踪控制中心**。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-172">Go to **Landed cost \> Delivery information setup \> Tracking control center**.</span></span> <span data-ttu-id="dfbbd-173">然后，您必须在此过程的步骤 4 中手动选择一个支线。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-173">You must then manually select a leg in step 4 of this procedure.</span></span>

1. <span data-ttu-id="dfbbd-174">在列表窗格中，将 **创建类型** 字段设置为 *提前期*。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-174">In the list pane, set the **Create type** field to *Lead time*.</span></span>
1. <span data-ttu-id="dfbbd-175">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-175">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dfbbd-176">如果在步骤 1 中您是从跟踪控制中心开始的，则将 **支线** 字段设置为要为其创建提前期规则的支线。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-176">If you started from the Tracking control center in step 1, set the **Leg** field to the leg that you want to create a lead time rule for.</span></span> <span data-ttu-id="dfbbd-177">如果您是从 **支线** 页开始的，**支线** 字段会预设为您在打开跟踪控制中心之前选择的字段。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-177">If you started from the **Legs** page, the **Leg** field is preset to the leg that you selected before you opened the Tracking control center.</span></span>

    <span data-ttu-id="dfbbd-178">根据 **支线** 字段的值，将自动设置几个字段，如下所示：</span><span class="sxs-lookup"><span data-stu-id="dfbbd-178">Based on the value of the **Leg** field, several fields are automatically set, as shown here:</span></span>

    - <span data-ttu-id="dfbbd-179">**源表**：*集装箱活动*</span><span class="sxs-lookup"><span data-stu-id="dfbbd-179">**Source table:** *Container activities*</span></span>
    - <span data-ttu-id="dfbbd-180">**源字段**：*开始日期*</span><span class="sxs-lookup"><span data-stu-id="dfbbd-180">**Source field:** *Start date*</span></span>
    - <span data-ttu-id="dfbbd-181">**目标表**：*集装箱活动*</span><span class="sxs-lookup"><span data-stu-id="dfbbd-181">**Target table:** *Container activities*</span></span>
    - <span data-ttu-id="dfbbd-182">**目标字段**：*估计结束日期*</span><span class="sxs-lookup"><span data-stu-id="dfbbd-182">**Target field:** *Estimated end date*</span></span>

1. <span data-ttu-id="dfbbd-183">在 **活动** 字段中，选择当前规则应该应用的活动。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-183">In the **Activity** field, select the activity that the current rule should apply to.</span></span>
1. <span data-ttu-id="dfbbd-184">在 **提前期** 字段中，输入在触发当前规则时应该应用的提前期（以天为单位）。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-184">In the **Lead time** field, enter the lead time (in days) that should be applied when the current rule is triggered.</span></span>

### <a name="status-update-rules"></a><span data-ttu-id="dfbbd-185">状态更新规则</span><span class="sxs-lookup"><span data-stu-id="dfbbd-185">Status update rules</span></span>

<span data-ttu-id="dfbbd-186">**创建类型** 字段设置为 *状态更新* 的记录将更新采购订单行的状态，或航行、装运集装箱或帐页级别的状态。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-186">Records where the **Create type** field is set to *Status update* will update the status of purchase order lines, or the status at the voyage, shipping container, or folio level.</span></span> <span data-ttu-id="dfbbd-187">状态可以独立设置。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-187">The statuses can be independently set.</span></span> <span data-ttu-id="dfbbd-188">使用它们可以通知用户或部门航行的阶段信息（如收到单据或货物正在运输中）。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-188">Use them to inform the user or department about the stage of a voyage (such as documents received or goods in transit).</span></span>

<span data-ttu-id="dfbbd-189">当 **创建类型** 字段设置为 *状态更新* 时，跟踪控制中心将包括一个 **行** 快速选项卡，您可以在其中定义成本区域和航行的更新状态。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-189">When the **Create type** field is set to *Status update*, the Tracking control center includes a **Lines** FastTab where you can define a cost area and the updated status of the voyage.</span></span> <span data-ttu-id="dfbbd-190">例如，您有一个行，其中 **成本区域** 字段设置为 *集装箱*，**航行状态** 字段设置为 *在途货物*。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-190">For example, you have a line where the **Cost area** field is set to *Container*, and the **Voyage status** field is set to *Goods in transit*.</span></span> <span data-ttu-id="dfbbd-191">在这种情况下，当订单完成指定支线时，装运集装箱的 **航行状态** 字段将更新为 *在途货物*。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-191">In this case, when an order completes the specified leg, the **Voyage status** field of the shipping container will be updated to *Goods in Transit*.</span></span>

<span data-ttu-id="dfbbd-192">状态更新会一直在航行行和与该航行关联的采购订单行提供航行的状态。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-192">Status updates provide the status of a voyage throughout the voyage lines and purchase order lines that are associated with that voyage.</span></span> <span data-ttu-id="dfbbd-193">在航行从港口、航行和海关到目的地仓库的整个行程中，航行记录的 **航行状态** 字段提供物料所在阶段的快速视图。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-193">As a voyage moves through its journey from the port, sailing, and customs, to the destination warehouse, the **Voyage status** field of the voyage record provides a quick view of the stage that the items are at.</span></span>

<span data-ttu-id="dfbbd-194">要将状态更新规则添加到跟踪控制中心，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-194">To add a status update rule to the Tracking control center, follow these steps.</span></span>

1. <span data-ttu-id="dfbbd-195">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="dfbbd-195">Follow one of these steps:</span></span>

    - <span data-ttu-id="dfbbd-196">转到 **登陆成本 \> 多支线行程设置 \> 支线**。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-196">Go to **Landed cost \> Multi-leg journey setup \> Legs**.</span></span> <span data-ttu-id="dfbbd-197">选择要为其设置状态更新的支线，然后在操作窗格上选择 **跟踪控制中心**。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-197">Select the leg that you want to set up a status update for, and then, on the Action Pane, select **Tracking control center**.</span></span> <span data-ttu-id="dfbbd-198">跟踪控制中心已预加载有关选定支线的信息。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-198">The Tracking control center is preloaded with information about the selected leg.</span></span>
    - <span data-ttu-id="dfbbd-199">转到 **登陆成本 \> 交货信息设置 \> 跟踪控制中心**。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-199">Go to **Landed cost \> Delivery information setup \> Tracking control center**.</span></span> <span data-ttu-id="dfbbd-200">然后，您必须在此过程的步骤 4 中手动选择一个支线。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-200">You must then manually select a leg in step 4 of this procedure.</span></span>

1. <span data-ttu-id="dfbbd-201">在列表窗格中，将 **创建类型** 字段设置为 *状态更新*。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-201">In the list pane, set the **Create type** field to *Status update*.</span></span>
1. <span data-ttu-id="dfbbd-202">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-202">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dfbbd-203">如果在步骤 1 中您是从跟踪控制中心开始的，则将 **支线** 字段设置为要为其创建状态更新规则的支线。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-203">If you started from the Tracking control center in step 1, set the **Leg** field to the leg that you want to create a status update rule for.</span></span> <span data-ttu-id="dfbbd-204">如果您是从 **支线** 页开始的，**支线** 字段会预设为您在打开跟踪控制中心之前选择的字段。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-204">If you started from the **Legs** page, the **Leg** field is preset to the leg that you selected before you opened the Tracking control center.</span></span>

    <span data-ttu-id="dfbbd-205">根据 **支线** 字段的值，将自动设置几个字段，如下所示：</span><span class="sxs-lookup"><span data-stu-id="dfbbd-205">Based on the value of the **Leg** field, several fields are automatically set, as shown here:</span></span>

    - <span data-ttu-id="dfbbd-206">**源表**：*集装箱活动*</span><span class="sxs-lookup"><span data-stu-id="dfbbd-206">**Source table:** *Container activities*</span></span>
    - <span data-ttu-id="dfbbd-207">**源字段**：*实际结束日期*</span><span class="sxs-lookup"><span data-stu-id="dfbbd-207">**Source field:** *Actual end date*</span></span>
    - <span data-ttu-id="dfbbd-208">**目标表：** 此字段留为空白。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-208">**Target table:** This field is left blank.</span></span>
    - <span data-ttu-id="dfbbd-209">**目标字段：** 此字段留为空白。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-209">**Target field:** This field is left blank.</span></span>

1. <span data-ttu-id="dfbbd-210">在 **活动** 字段中，选择您的规则应该应用的活动。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-210">In the **Activity** field, select the activity that your rule should apply to.</span></span>
1. <span data-ttu-id="dfbbd-211">在 **行** 快速选项卡上，输入每个成本区域的状态更新。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-211">On the **Lines** FastTab, enter the status updates for each cost area.</span></span>

### <a name="blank-type-rules"></a><span data-ttu-id="dfbbd-212">空白类型规则</span><span class="sxs-lookup"><span data-stu-id="dfbbd-212">Blank type rules</span></span>

<span data-ttu-id="dfbbd-213">您使用 **创建类型** 值为 *空白* 的记录基于另一个字段的数据替代或输入字段值。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-213">You use records that have a **Create type** value of *Blank* to override or enter a field value, based on the data of another field.</span></span> <span data-ttu-id="dfbbd-214">“登陆成本”中的字段将根据在跟踪控制中心中设置的规则覆盖 Microsoft Dynamics 365 Supply Chain Management 的其他区域的数据。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-214">A field from Landed cost will overwrite data in other areas of Microsoft Dynamics 365 Supply Chain Management, based on rules that are set up in the Tracking control center.</span></span>

1. <span data-ttu-id="dfbbd-215">转到 **登陆成本 \> 交货信息设置 \> 跟踪控制中心**。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-215">Go to **Landed cost \> Delivery information setup \> Tracking control center**.</span></span>
1. <span data-ttu-id="dfbbd-216">在列表窗格中，将 **创建类型** 字段设置为 *空白*。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-216">In the list pane, set the **Create type** field to *Blank*.</span></span>
1. <span data-ttu-id="dfbbd-217">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-217">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dfbbd-218">根据您的规则要求定义源和目标值、匹配条件、复制操作以及其他相关参数。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-218">Define the source and destination values, matching criteria, copy action, and other relevant parameters, as required for your rule.</span></span>

### <a name="required-tracking-control-setup"></a><span data-ttu-id="dfbbd-219">所需的跟踪控制设置</span><span class="sxs-lookup"><span data-stu-id="dfbbd-219">Required tracking control setup</span></span>

<span data-ttu-id="dfbbd-220">对于每个行程模板，必须在跟踪控制中心设置两个记录。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-220">For every journey template, two records must be set up in the Tracking control center.</span></span> <span data-ttu-id="dfbbd-221">这两个记录的 **创建类型** 值都为 *空白*，它们在所有登陆成本实施中使用。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-221">Both these records have a **Create type** value of *Blank* and are used in all Landed cost implementations.</span></span> <span data-ttu-id="dfbbd-222">它们帮助确保以预期方式为航行和相关采购订单行更新采购确认日期和在途货物预期日期。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-222">They help ensure that the purchase confirmed date and goods in transit expected dates are updated for voyages and on related purchase order lines in the expected way.</span></span>

<span data-ttu-id="dfbbd-223">更新采购订单行需要第一个记录。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-223">The first record is required to update purchase lines.</span></span> <span data-ttu-id="dfbbd-224">它必须具有以下设置：</span><span class="sxs-lookup"><span data-stu-id="dfbbd-224">It must have the following settings:</span></span>

- <span data-ttu-id="dfbbd-225">**源表**：*集装箱活动*</span><span class="sxs-lookup"><span data-stu-id="dfbbd-225">**Source table:** *Container activities*</span></span>
- <span data-ttu-id="dfbbd-226">**源字段**：*估计结束日期*</span><span class="sxs-lookup"><span data-stu-id="dfbbd-226">**Source field:** *Estimated end date*</span></span>
- <span data-ttu-id="dfbbd-227">**目标表**：*采购订单行*</span><span class="sxs-lookup"><span data-stu-id="dfbbd-227">**Target table:** *Purchase lines*</span></span>
- <span data-ttu-id="dfbbd-228">**目标字段**：*确认或交货日期*</span><span class="sxs-lookup"><span data-stu-id="dfbbd-228">**Target field:** *Confirmed or delivery date*</span></span>

<span data-ttu-id="dfbbd-229">更新在途货物交易需要第二个记录。</span><span class="sxs-lookup"><span data-stu-id="dfbbd-229">The second record is required to update goods in transit transactions.</span></span> <span data-ttu-id="dfbbd-230">它必须具有以下设置：</span><span class="sxs-lookup"><span data-stu-id="dfbbd-230">It must have the following settings:</span></span>

- <span data-ttu-id="dfbbd-231">**源表**：*集装箱活动*</span><span class="sxs-lookup"><span data-stu-id="dfbbd-231">**Source table:** *Container activities*</span></span>
- <span data-ttu-id="dfbbd-232">**源字段**：*估计结束日期*</span><span class="sxs-lookup"><span data-stu-id="dfbbd-232">**Source field:** *Estimated end date*</span></span>
- <span data-ttu-id="dfbbd-233">**目标表**：*在途货物订单*</span><span class="sxs-lookup"><span data-stu-id="dfbbd-233">**Target table:** *Goods in transit order*</span></span>
- <span data-ttu-id="dfbbd-234">**目标字段**：*预期日期*</span><span class="sxs-lookup"><span data-stu-id="dfbbd-234">**Target field:** *Expected date*</span></span>

---
title: 多支线行程设置
description: 本主题介绍如何为登陆成本模块设置多支线行程。
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMLegTable, ITMJourneyTable, ITMActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 45e32c59c79389bcab15dd07d1bbd33d7ff34340
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021556"
---
# <a name="multi-leg-journey-setup"></a><span data-ttu-id="bf91f-103">多支线行程设置</span><span class="sxs-lookup"><span data-stu-id="bf91f-103">Multi-leg journey setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bf91f-104">本主题介绍如何为 **登陆成本** 模块设置多支线行程。</span><span class="sxs-lookup"><span data-stu-id="bf91f-104">This topic describes how to set up multi-leg journeys for the **Landed cost** module.</span></span>

## <a name="legs"></a><span data-ttu-id="bf91f-105">支线</span><span class="sxs-lookup"><span data-stu-id="bf91f-105">Legs</span></span>

<span data-ttu-id="bf91f-106">支线用于标识行程的各个单独部分。</span><span class="sxs-lookup"><span data-stu-id="bf91f-106">Legs are used to identify separate parts of a journey.</span></span> <span data-ttu-id="bf91f-107">每个支线通过选择“到达”和“发运”装运港口以及用于该支线的运输方法来建立。</span><span class="sxs-lookup"><span data-stu-id="bf91f-107">Each leg is built by selecting the "to" and "from" shipping ports, and the transportation method that is used for that leg.</span></span> <span data-ttu-id="bf91f-108">提前期可以与每个支线关联。</span><span class="sxs-lookup"><span data-stu-id="bf91f-108">Lead times can be associated with each leg.</span></span> <span data-ttu-id="bf91f-109">提前期可以帮助跟踪装运，还可以用于计算航行中货物的估计交货日期。</span><span class="sxs-lookup"><span data-stu-id="bf91f-109">Lead times can help track a shipment and can also be used to calculate the estimated delivery date of the goods on a voyage.</span></span> <span data-ttu-id="bf91f-110">另外，当行程的某个支线完成时，可以通过跟踪控制设置更新航行、装运集装箱和关联的采购订单行的状态。</span><span class="sxs-lookup"><span data-stu-id="bf91f-110">Additionally, when a leg of a journey is completed, the status of the voyage, shipping container, and associated purchase order lines can be updated through the tracking control setup.</span></span> <span data-ttu-id="bf91f-111">支线可以由单个行程模板使用，也可以由多个行程模板重复使用。</span><span class="sxs-lookup"><span data-stu-id="bf91f-111">Legs can be used by a single journey template, or they can be reused by multiple journey templates.</span></span> <span data-ttu-id="bf91f-112">通常将集装箱装载、海关和当地运输设置为支线，支线使用非特定装运港口。</span><span class="sxs-lookup"><span data-stu-id="bf91f-112">Container loading, customs, and local transport are generally set up as legs, and a non-specific shipping port is used for them.</span></span>

<span data-ttu-id="bf91f-113">要使用支线，转到 **登陆成本 \> 多支线行程设置 \> 支线**。</span><span class="sxs-lookup"><span data-stu-id="bf91f-113">To work with legs, go to **Landed cost \> Multi-leg journey setup \> Legs**.</span></span> <span data-ttu-id="bf91f-114">在那里，您可以查看、打开、创建和删除支线的记录。</span><span class="sxs-lookup"><span data-stu-id="bf91f-114">There, you can view, open, create, and delete records for legs.</span></span> <span data-ttu-id="bf91f-115">下表说明了可用于每个记录的字段。</span><span class="sxs-lookup"><span data-stu-id="bf91f-115">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="bf91f-116">字段</span><span class="sxs-lookup"><span data-stu-id="bf91f-116">Field</span></span> | <span data-ttu-id="bf91f-117">说明</span><span class="sxs-lookup"><span data-stu-id="bf91f-117">Description</span></span> |
|---|---|
| <span data-ttu-id="bf91f-118">支线</span><span class="sxs-lookup"><span data-stu-id="bf91f-118">Leg</span></span> | <span data-ttu-id="bf91f-119">为行程支线输入唯一标识名称/编号。</span><span class="sxs-lookup"><span data-stu-id="bf91f-119">Enter a unique identification name/number for the journey leg.</span></span> |
| <span data-ttu-id="bf91f-120">说明</span><span class="sxs-lookup"><span data-stu-id="bf91f-120">Description</span></span> | <span data-ttu-id="bf91f-121">输入行程支线的描述。</span><span class="sxs-lookup"><span data-stu-id="bf91f-121">Enter a description of the journey leg.</span></span> <span data-ttu-id="bf91f-122">通常，此描述标识“到达”和“发运”港口，或行程的步骤。</span><span class="sxs-lookup"><span data-stu-id="bf91f-122">Typically, this description identifies the "to" and "from" ports, or the step of the journey.</span></span> |
| <span data-ttu-id="bf91f-123">发运港口</span><span class="sxs-lookup"><span data-stu-id="bf91f-123">From port</span></span> | <span data-ttu-id="bf91f-124">在支线中输入货物的起始点。</span><span class="sxs-lookup"><span data-stu-id="bf91f-124">Enter the point of origin of the goods on the leg.</span></span> |
| <span data-ttu-id="bf91f-125">目标港口</span><span class="sxs-lookup"><span data-stu-id="bf91f-125">To port</span></span> | <span data-ttu-id="bf91f-126">在支线中输入货物的目的地。</span><span class="sxs-lookup"><span data-stu-id="bf91f-126">Enter the point of destination of the goods on the leg.</span></span> |
| <span data-ttu-id="bf91f-127">交货方法</span><span class="sxs-lookup"><span data-stu-id="bf91f-127">Delivery method</span></span> | <span data-ttu-id="bf91f-128">输入支线的运输方式。</span><span class="sxs-lookup"><span data-stu-id="bf91f-128">Enter the method of transport for the leg.</span></span> |

## <a name="journey-templates"></a><span data-ttu-id="bf91f-129">行程模板</span><span class="sxs-lookup"><span data-stu-id="bf91f-129">Journey templates</span></span>

<span data-ttu-id="bf91f-130">行程模板定义在航行中货物行进的两个港口之间的多支线行程。</span><span class="sxs-lookup"><span data-stu-id="bf91f-130">A journey template defines the multi-leg journey between two ports that goods travel during a voyage.</span></span> <span data-ttu-id="bf91f-131">行程的各个支线将合并，来确定将货物从供应商的起始点运输到最终仓库目的地所需要的时间量。</span><span class="sxs-lookup"><span data-stu-id="bf91f-131">The legs of the journey are combined to identify the amount of time that will be required for goods to travel from the vendor's point of origin to the final warehouse destination.</span></span> <span data-ttu-id="bf91f-132">当将支线按特定顺序放在行程模板上时，提前期将确定每个支线的日期以及航行、集装箱和航行的采购订单行的状态。</span><span class="sxs-lookup"><span data-stu-id="bf91f-132">When the legs are put on the journey template in a specific order, the lead times will identify the date of each leg and status of the voyage, container, and purchase lines for the voyage.</span></span> <span data-ttu-id="bf91f-133">您将使用[跟踪控制中心](delivery-information-setup.md)设置与构成行程模板的每个支线关联的提前期。</span><span class="sxs-lookup"><span data-stu-id="bf91f-133">You use the [Tracking control center](delivery-information-setup.md) to set up the lead times that are associated with each leg that makes up the journey template.</span></span> <span data-ttu-id="bf91f-134">设置航行的自动成本时，也会使用行程模板。</span><span class="sxs-lookup"><span data-stu-id="bf91f-134">The journey template is also used when the automatic costs of a voyage are set up.</span></span> <span data-ttu-id="bf91f-135">定义行程后，可以在自动成本页面定义与货物的运输关联的成本。</span><span class="sxs-lookup"><span data-stu-id="bf91f-135">When a journey is defined, the cost that is associated with the transport of the goods can be defined on the auto costs page.</span></span>

<span data-ttu-id="bf91f-136">要使用行程模板，转到 **登陆成本 \> 多支线行程设置 \> 行程模板**。</span><span class="sxs-lookup"><span data-stu-id="bf91f-136">To work with journey templates, go to **Landed cost \> Multi-leg journey setup \> Journey templates**.</span></span> <span data-ttu-id="bf91f-137">在那里，您可以查看、打开、创建和删除行程模板。</span><span class="sxs-lookup"><span data-stu-id="bf91f-137">There, you can view, open, create, and delete journey templates.</span></span>

<span data-ttu-id="bf91f-138">对于每个行程模板，在标头上设置以下字段。</span><span class="sxs-lookup"><span data-stu-id="bf91f-138">For each journey template, set the following fields on the header.</span></span>

| <span data-ttu-id="bf91f-139">字段</span><span class="sxs-lookup"><span data-stu-id="bf91f-139">Field</span></span> | <span data-ttu-id="bf91f-140">说明</span><span class="sxs-lookup"><span data-stu-id="bf91f-140">Description</span></span> |
|---|---|
| <span data-ttu-id="bf91f-141">行程模板</span><span class="sxs-lookup"><span data-stu-id="bf91f-141">Journey template</span></span> | <span data-ttu-id="bf91f-142">为行程模板输入唯一标识名称/编号。</span><span class="sxs-lookup"><span data-stu-id="bf91f-142">Enter a unique identification name/number for the journey template.</span></span> <span data-ttu-id="bf91f-143">行程模板通常描述行程的起始点和目的地。</span><span class="sxs-lookup"><span data-stu-id="bf91f-143">The journey template typically describes the point of origin and point of destination for the journey.</span></span> |
| <span data-ttu-id="bf91f-144">说明</span><span class="sxs-lookup"><span data-stu-id="bf91f-144">Description</span></span> | <span data-ttu-id="bf91f-145">输入行程模板的描述。</span><span class="sxs-lookup"><span data-stu-id="bf91f-145">Enter a description of the journey template.</span></span> <span data-ttu-id="bf91f-146">此描述通常指示“到达”港口和“发运”港口以及行进类型。</span><span class="sxs-lookup"><span data-stu-id="bf91f-146">The description typically indicates the "to" and "from" ports, and the type of travel.</span></span> |

<span data-ttu-id="bf91f-147">在 **行** 部分，为行程的每个支线添加一行，并按顺序放置行。</span><span class="sxs-lookup"><span data-stu-id="bf91f-147">In the **Lines** section, add a line for each leg of the journey, and put the lines in order.</span></span> <span data-ttu-id="bf91f-148">使用工具栏上的 **向上** 和 **下** 箭头可更改行的顺序。</span><span class="sxs-lookup"><span data-stu-id="bf91f-148">Use the **Up** and **Down** arrows on the toolbar to change the order of the lines.</span></span> <span data-ttu-id="bf91f-149">下表说明了可用于每个行的字段。</span><span class="sxs-lookup"><span data-stu-id="bf91f-149">The following table describes the fields that are available for each line.</span></span>

| <span data-ttu-id="bf91f-150">字段</span><span class="sxs-lookup"><span data-stu-id="bf91f-150">Field</span></span> | <span data-ttu-id="bf91f-151">说明</span><span class="sxs-lookup"><span data-stu-id="bf91f-151">Description</span></span> |
|---|---|
| <span data-ttu-id="bf91f-152">支线</span><span class="sxs-lookup"><span data-stu-id="bf91f-152">Leg</span></span> | <span data-ttu-id="bf91f-153">选择要添加到行程中的支线。</span><span class="sxs-lookup"><span data-stu-id="bf91f-153">Select a leg to add to the journey.</span></span> |
| <span data-ttu-id="bf91f-154">说明</span><span class="sxs-lookup"><span data-stu-id="bf91f-154">Description</span></span> | <span data-ttu-id="bf91f-155">支线的描述。</span><span class="sxs-lookup"><span data-stu-id="bf91f-155">The description of the leg.</span></span> |
| <span data-ttu-id="bf91f-156">发运港口</span><span class="sxs-lookup"><span data-stu-id="bf91f-156">From port</span></span> | <span data-ttu-id="bf91f-157">作为支线中货物的起始点的港口。</span><span class="sxs-lookup"><span data-stu-id="bf91f-157">The port that is the point of origin of the goods on the leg.</span></span> <span data-ttu-id="bf91f-158">此港口是“到达”港口，用于确定航行的自动成本。</span><span class="sxs-lookup"><span data-stu-id="bf91f-158">This port is the "to" port that is used to determine the auto costs for a voyage.</span></span> |
| <span data-ttu-id="bf91f-159">目标港口</span><span class="sxs-lookup"><span data-stu-id="bf91f-159">To port</span></span> | <span data-ttu-id="bf91f-160">支线中货物的最终目标港口。</span><span class="sxs-lookup"><span data-stu-id="bf91f-160">The final destination port of the goods on the leg.</span></span> |
| <span data-ttu-id="bf91f-161">交货模式</span><span class="sxs-lookup"><span data-stu-id="bf91f-161">Mode of delivery</span></span> | <span data-ttu-id="bf91f-162">用于支线的交货方式。</span><span class="sxs-lookup"><span data-stu-id="bf91f-162">The mode of delivery that is used for the leg.</span></span> |
| <span data-ttu-id="bf91f-163">行程发运港口</span><span class="sxs-lookup"><span data-stu-id="bf91f-163">Journey from port</span></span> | <span data-ttu-id="bf91f-164">如果为支线指定的港口用于确定自动成本，请选中此复选框将其标识为“行程发运”港口。</span><span class="sxs-lookup"><span data-stu-id="bf91f-164">If the port that is specified for the leg is used to determine the auto costs, select this check box to identify it as the "journey from" port.</span></span> <span data-ttu-id="bf91f-165">此港口将显示在航行标头上。</span><span class="sxs-lookup"><span data-stu-id="bf91f-165">This port will be shown on the voyage header.</span></span> |
| <span data-ttu-id="bf91f-166">行程目标港口</span><span class="sxs-lookup"><span data-stu-id="bf91f-166">Journey to port</span></span> | <span data-ttu-id="bf91f-167">如果为支线指定的港口用于确定自动成本，请选中此复选框将其标识为“行程到达”港口。</span><span class="sxs-lookup"><span data-stu-id="bf91f-167">If the port that is specified for the leg is used to determine the auto costs, select this check box to identify it as the "journey to" port.</span></span> <span data-ttu-id="bf91f-168">此港口将显示在航行标头上。</span><span class="sxs-lookup"><span data-stu-id="bf91f-168">This port will be shown on the voyage header.</span></span> |
| <span data-ttu-id="bf91f-169">装运公司</span><span class="sxs-lookup"><span data-stu-id="bf91f-169">Shipping company</span></span> | <span data-ttu-id="bf91f-170">选择用于支线的装运公司。</span><span class="sxs-lookup"><span data-stu-id="bf91f-170">Select the shipping company that is used for the leg.</span></span> |

## <a name="activities"></a><span data-ttu-id="bf91f-171">活动</span><span class="sxs-lookup"><span data-stu-id="bf91f-171">Activities</span></span>

<span data-ttu-id="bf91f-172">**活动** 页上的设置确定可能在支线的目标港口发生的活动的类型。</span><span class="sxs-lookup"><span data-stu-id="bf91f-172">The settings on the **Activities** page establish the types of activities that can occur at the destination port of a leg.</span></span> <span data-ttu-id="bf91f-173">在 **所有装运集装箱** 页上工作的用户在估算每个活动的持续时间以及记录实际持续时间以进行比较时，可以在这些值中进行选择。</span><span class="sxs-lookup"><span data-stu-id="bf91f-173">Users who work on the **All shipping containers** page can select among these values when they estimate the duration of each activity and record the actual duration for comparison purposes.</span></span>

<span data-ttu-id="bf91f-174">要设置活动，转到 **登陆成本 \> 多支线行程设置 \> 活动**。</span><span class="sxs-lookup"><span data-stu-id="bf91f-174">To set up your activities, go to **Landed cost \> Multi-leg journeys setup \> Activities**.</span></span> <span data-ttu-id="bf91f-175">在那里，您可以使用操作窗格上的按钮添加、删除和编辑活动。</span><span class="sxs-lookup"><span data-stu-id="bf91f-175">There, you can add, remove, and edit activities by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="bf91f-176">下表说明了可用于网格中每个活动的字段。</span><span class="sxs-lookup"><span data-stu-id="bf91f-176">The following table describes the fields that are available for each activity in the grid.</span></span>

| <span data-ttu-id="bf91f-177">字段</span><span class="sxs-lookup"><span data-stu-id="bf91f-177">Field</span></span> | <span data-ttu-id="bf91f-178">说明</span><span class="sxs-lookup"><span data-stu-id="bf91f-178">Description</span></span> |
|---|---|
| <span data-ttu-id="bf91f-179">活动</span><span class="sxs-lookup"><span data-stu-id="bf91f-179">Activity</span></span> | <span data-ttu-id="bf91f-180">活动的名称。</span><span class="sxs-lookup"><span data-stu-id="bf91f-180">The name of the activity.</span></span> |
| <span data-ttu-id="bf91f-181">说明</span><span class="sxs-lookup"><span data-stu-id="bf91f-181">Description</span></span> | <span data-ttu-id="bf91f-182">活动的描述。</span><span class="sxs-lookup"><span data-stu-id="bf91f-182">A description of the activity.</span></span> |
| <span data-ttu-id="bf91f-183">装运公司</span><span class="sxs-lookup"><span data-stu-id="bf91f-183">Shipping company</span></span> | <span data-ttu-id="bf91f-184">与活动关联的装运公司的供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="bf91f-184">The vendor account of the shipping company that is associated with the activity.</span></span> |

---
title: 创建工作订单
description: 本主题介绍如何在资产管理中创建工作订单。
author: johanhoffmann
manager: tfehr
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 876aef9f3f470490bb385e1861c837dcfa82db69
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131785"
---
# <a name="creating-work-orders"></a><span data-ttu-id="76402-103">创建工作订单</span><span class="sxs-lookup"><span data-stu-id="76402-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="76402-104">计划了预防性维护作业之后，接下来需要为这些作业创建工作订单。</span><span class="sxs-lookup"><span data-stu-id="76402-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="76402-105">您可以使用其中一个维护安排完成此步骤。</span><span class="sxs-lookup"><span data-stu-id="76402-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="76402-106">维护安排中的计划作业可以采用不同类型，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="76402-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="76402-107">引用类型</span><span class="sxs-lookup"><span data-stu-id="76402-107">Reference type</span></span> | <span data-ttu-id="76402-108">说明</span><span class="sxs-lookup"><span data-stu-id="76402-108">Description</span></span> |
|---|---|
| <span data-ttu-id="76402-109">维护计划</span><span class="sxs-lookup"><span data-stu-id="76402-109">Maintenance plans</span></span> | <span data-ttu-id="76402-110">基于 *时间* 或 *计数器* 维护计划类型的预防性维护作业。</span><span class="sxs-lookup"><span data-stu-id="76402-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="76402-111">维护阶段</span><span class="sxs-lookup"><span data-stu-id="76402-111">Maintenance rounds</span></span> | <span data-ttu-id="76402-112">其中包含多个需要相似维护类型的资产的预防性维护作业。</span><span class="sxs-lookup"><span data-stu-id="76402-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="76402-113">维护请求</span><span class="sxs-lookup"><span data-stu-id="76402-113">Maintenance request</span></span> | <span data-ttu-id="76402-114">手动创建的资产的维护或维修请求。</span><span class="sxs-lookup"><span data-stu-id="76402-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="76402-115">此请求可以转换为工作订单。</span><span class="sxs-lookup"><span data-stu-id="76402-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="76402-116">根据维护安排创建工作订单</span><span class="sxs-lookup"><span data-stu-id="76402-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="76402-117">要创建基于维护安排的工作订单，请遵循以下步骤。</span><span class="sxs-lookup"><span data-stu-id="76402-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="76402-118">打开以下页面之一，具体取决于您要如何为工作订单选择计划项目：</span><span class="sxs-lookup"><span data-stu-id="76402-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="76402-119">所有维护安排（**资产管理 \> 管理计划 \> 所有维护安排**）</span><span class="sxs-lookup"><span data-stu-id="76402-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="76402-120">打开维护安排行（**资产管理 \> 管理计划 \> 打开维护安排行**）</span><span class="sxs-lookup"><span data-stu-id="76402-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="76402-121">打开维护安排池（**资产管理 \> 管理计划 \> 打开维护安排池**）</span><span class="sxs-lookup"><span data-stu-id="76402-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="76402-122">在网格中，选中要为其创建工作订单的每个计划性维护作业的复选框。</span><span class="sxs-lookup"><span data-stu-id="76402-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="76402-123">然后，在操作窗格中，选择 **工作订单**。</span><span class="sxs-lookup"><span data-stu-id="76402-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="76402-124">**创建工作订单** 对话框将出现。</span><span class="sxs-lookup"><span data-stu-id="76402-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="76402-125">**维护预测工时数** 字段将显示所选行的预测工时总数。</span><span class="sxs-lookup"><span data-stu-id="76402-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![创建工作订单对话框](media/18-preventive-maintenance.png)

1. <span data-ttu-id="76402-127">在 **参数** 部分，指定应创建的工作订单的数量。</span><span class="sxs-lookup"><span data-stu-id="76402-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="76402-128">选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="76402-128">Select one of the following options:</span></span>

    - <span data-ttu-id="76402-129">**每行一个工作订单** – 每个维护安排行创建一个工作订单。</span><span class="sxs-lookup"><span data-stu-id="76402-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="76402-130">**每个以下对象一个工作订单** – 创建将根据您选择此选项时可用的其他选项的设置进行分组的工作订单。</span><span class="sxs-lookup"><span data-stu-id="76402-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="76402-131">在 **工作订单类型** 字段中，选择要用于所有创建的工作订单的工作订单类型。</span><span class="sxs-lookup"><span data-stu-id="76402-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="76402-132">选择 **确定** 根据您的设置创建工作订单。</span><span class="sxs-lookup"><span data-stu-id="76402-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="76402-133">对在维护计划运行时自动创建的工作订单行进行分组</span><span class="sxs-lookup"><span data-stu-id="76402-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

> [!IMPORTANT]
> <span data-ttu-id="76402-134">本节中介绍的功能作为预览版的一部分提供。</span><span class="sxs-lookup"><span data-stu-id="76402-134">The functionality that is described in this section is available as part of a preview release.</span></span> <span data-ttu-id="76402-135">内容和功能可能会发生变化。</span><span class="sxs-lookup"><span data-stu-id="76402-135">The content and the functionality are subject to change.</span></span> <span data-ttu-id="76402-136">有关预览版的详细信息，请参阅 [One Version 服务更新常见问题](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version)。</span><span class="sxs-lookup"><span data-stu-id="76402-136">For more information about preview releases, see [One version service updates FAQ](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).</span></span>

<span data-ttu-id="76402-137">使用此功能，您可以根据维护计划，为在系统设置为自动生成工作订单时对单个工作订单下的工作订单行进行分组定义规则。</span><span class="sxs-lookup"><span data-stu-id="76402-137">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="76402-138">以前，自动生成的工作订单只能包含一行。</span><span class="sxs-lookup"><span data-stu-id="76402-138">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="76402-139">但是，现在您可以按资产、资产类型或功能位置等对工作订单进行分组。</span><span class="sxs-lookup"><span data-stu-id="76402-139">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="76402-140">（手动生成的工作订单可能已经通过这种方式完成了分组，如本主题上一节中所述。）</span><span class="sxs-lookup"><span data-stu-id="76402-140">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="76402-141">为自动生成的工作订单启用分组</span><span class="sxs-lookup"><span data-stu-id="76402-141">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="76402-142">此功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="76402-142">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="76402-143">管理员可以使用[功能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。</span><span class="sxs-lookup"><span data-stu-id="76402-143">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="76402-144">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="76402-144">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="76402-145">**模块**：*资产管理*</span><span class="sxs-lookup"><span data-stu-id="76402-145">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="76402-146">**功能名称**：*（预览）在运行维护计划时为分组工作订单应用规则*</span><span class="sxs-lookup"><span data-stu-id="76402-146">**Feature name:** *(Preview) Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="76402-147">为自动生成的工作订单设置分组</span><span class="sxs-lookup"><span data-stu-id="76402-147">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="76402-148">要为自动生成的工作订单设置分组，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="76402-148">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="76402-149">转到 **资产管理 \> 设置 \> 预防性维护 \> 维护计划**。</span><span class="sxs-lookup"><span data-stu-id="76402-149">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="76402-150">对于要在其中生成分组工作订单的每个计划，按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="76402-150">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="76402-151">在列表窗格中选择该计划。</span><span class="sxs-lookup"><span data-stu-id="76402-151">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="76402-152">在 **行** 快速选项卡上，确保选中每行上的 **自动创建** 复选框。</span><span class="sxs-lookup"><span data-stu-id="76402-152">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="76402-153">转到 **资产管理 \> 定期 \> 预防性维护 \> 安排维护计划**。</span><span class="sxs-lookup"><span data-stu-id="76402-153">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="76402-154">在 **安排维护计划** 对话框中的 **期间** 部分，为计划指定时间范围（查找为之生成工作的计划性维护作业时要提前多长时间）。</span><span class="sxs-lookup"><span data-stu-id="76402-154">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="76402-155">将 **从计划自动创建工作订单** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="76402-155">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="76402-156">在 **工作订单** 部分，选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="76402-156">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="76402-157">**每行一个工作订单** – 每个维护安排行创建一个工作订单。</span><span class="sxs-lookup"><span data-stu-id="76402-157">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="76402-158">（此选项提供的功能与 *在运行维护计划时为分组工作订单应用规则* 功能关闭时可用的功能相同。）</span><span class="sxs-lookup"><span data-stu-id="76402-158">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="76402-159">**每个以下对象一个工作订单** – 创建将根据您选择此选项时可用的其他选项的设置进行分组的工作订单。</span><span class="sxs-lookup"><span data-stu-id="76402-159">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="76402-160">如果您希望仅在运行某些维护计划时应用这些选项，在 **要包括的记录** 快速选项卡上，根据需要添加筛选器，就像您可能对 Microsoft Dynamics 365 Supply Chain Management 中的其他批处理作业所做的那样。</span><span class="sxs-lookup"><span data-stu-id="76402-160">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="76402-161">在 **在后台运行** 快速选项卡上，根据需要设置批处理和计划选项，就像您可能在 Supply Chain Management 中对其他批处理作业所做的那样。</span><span class="sxs-lookup"><span data-stu-id="76402-161">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="76402-162">选择 **确定** 运行和/或计划选定的维护计划。</span><span class="sxs-lookup"><span data-stu-id="76402-162">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>

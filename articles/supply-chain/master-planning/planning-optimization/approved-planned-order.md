---
title: 查看、管理和审核计划订单
description: 此主题介绍如何在计划优化中查看、管理和审核计划订单。
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 71ec26bea2063bcf8b6d302a7ece804b3ac934b3
ms.sourcegitcommit: 3673eeca1ada0f3e4ec277176515a946706f8a41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304359"
---
# <a name="view-manage-and-approve-planned-orders"></a><span data-ttu-id="23d89-103">查看、管理和审核计划订单</span><span class="sxs-lookup"><span data-stu-id="23d89-103">View, manage, and approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23d89-104">此主题介绍如何在计划优化中查看、管理和审核计划订单。</span><span class="sxs-lookup"><span data-stu-id="23d89-104">This topic provides information about how to view, manage, and approve planned orders in Planning Optimization.</span></span>

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a><span data-ttu-id="23d89-105">查看和管理计划订单</span><span class="sxs-lookup"><span data-stu-id="23d89-105">View and manage planned orders</span></span>

<span data-ttu-id="23d89-106">您可以在任何计划订单列表页上查看和管理计划订单。</span><span class="sxs-lookup"><span data-stu-id="23d89-106">You can view and manage planned orders on any planned orders list page.</span></span> <span data-ttu-id="23d89-107">根据要处理的计划订单的类型，转到以下位置之一：</span><span class="sxs-lookup"><span data-stu-id="23d89-107">Go to one of the following places, depending on the type of planned orders that you want to work with:</span></span>

- <span data-ttu-id="23d89-108">主计划 \> 工作区 \> 主计划</span><span class="sxs-lookup"><span data-stu-id="23d89-108">Master planning \> Workspaces \> Master planning</span></span>
- <span data-ttu-id="23d89-109">主计划 \> 主计划 \> 计划订单</span><span class="sxs-lookup"><span data-stu-id="23d89-109">Master planning \> Master planning \> Planned orders</span></span>
- <span data-ttu-id="23d89-110">生产控制 \> 生产订单 \> 计划生产订单</span><span class="sxs-lookup"><span data-stu-id="23d89-110">Production control \> Production orders \> Planned production orders</span></span>
- <span data-ttu-id="23d89-111">采购 \> 采购订单 \> 计划采购订单</span><span class="sxs-lookup"><span data-stu-id="23d89-111">Procurement and sourcing \> Purchase orders \> Planned purchase orders</span></span>
- <span data-ttu-id="23d89-112">库存管理 \> 入站订单 \> 计划转移</span><span class="sxs-lookup"><span data-stu-id="23d89-112">Inventory management \> Inbound orders \> Planned transfers</span></span>
- <span data-ttu-id="23d89-113">库存管理 \> 出站订单 \> 计划转移</span><span class="sxs-lookup"><span data-stu-id="23d89-113">Inventory management \> Outbound orders \> Planned transfers</span></span>

## <a name="view-and-edit-the-status-of-planned-orders"></a><span data-ttu-id="23d89-114">查看和编辑计划订单的状态</span><span class="sxs-lookup"><span data-stu-id="23d89-114">View and edit the status of planned orders</span></span>

<span data-ttu-id="23d89-115">您可以使用每个计划订单的 **状态** 字段来帮助跟踪进度或更改计划订单的处理方式。</span><span class="sxs-lookup"><span data-stu-id="23d89-115">You can use the **Status** field of each planned order to help track your progress or change how a planned order will be processed.</span></span> <span data-ttu-id="23d89-116">提供以下 **状态** 值：</span><span class="sxs-lookup"><span data-stu-id="23d89-116">The following **Status** values are available:</span></span>

- <span data-ttu-id="23d89-117">**未处理** – 当主计划生成计划订单时，它们将获得此状态。</span><span class="sxs-lookup"><span data-stu-id="23d89-117">**Unprocessed** – When master planning generates planned orders, they are given this status.</span></span> <span data-ttu-id="23d89-118">具有此状态的计划订单将在下一次计划运行期间删除。</span><span class="sxs-lookup"><span data-stu-id="23d89-118">Planned orders that have this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="23d89-119">**已完成** – 此状态指示计划订单已完成。</span><span class="sxs-lookup"><span data-stu-id="23d89-119">**Completed** – This status indicates that the planned order has been completed.</span></span> <span data-ttu-id="23d89-120">如果您决定不确认某一计划订单，可以将其状态手动更改为 *已完成*。</span><span class="sxs-lookup"><span data-stu-id="23d89-120">If you decide not to firm a planned order, you can manually change its status to *Completed*.</span></span> <span data-ttu-id="23d89-121">请注意，系统以相同的方式对待 *未处理* 和 *已完成* 状态。</span><span class="sxs-lookup"><span data-stu-id="23d89-121">Note that the system treats the *Unprocessed* and *Completed* statuses in the same way.</span></span>
- <span data-ttu-id="23d89-122">**已审核** – 此状态指示计划订单已审核，可以确认。</span><span class="sxs-lookup"><span data-stu-id="23d89-122">**Approved** – This status indicates that the planned order is approved for firming.</span></span> <span data-ttu-id="23d89-123">如果要确认计划订单，可将其状态更改为 *已审核*。</span><span class="sxs-lookup"><span data-stu-id="23d89-123">If you want to firm a planned order, you can change its status to *Approved*.</span></span> <span data-ttu-id="23d89-124">如果要保留对计划订单所做的编辑，或者打算确认计划订单，请将其状态更改为 *已审核*。</span><span class="sxs-lookup"><span data-stu-id="23d89-124">If you want to keep the edits that have been made to a planned order, or if you're planning to firm a planned order, change its status to *Approved*.</span></span> <span data-ttu-id="23d89-125">状态为 *已审核* 的计划订单将被主计划视为固定供应和预期供应。</span><span class="sxs-lookup"><span data-stu-id="23d89-125">Planned orders that have a status of *Approved* are considered fixed and expected supply by master planning.</span></span> <span data-ttu-id="23d89-126">因此，在之后的主计划运行中不会对其进行修改或删除。</span><span class="sxs-lookup"><span data-stu-id="23d89-126">Therefore, they aren't modified or deleted during later master planning runs.</span></span> <span data-ttu-id="23d89-127">为实现此行为，计划逻辑会在主计划期间将状态为 *已审核* 的计划订单从旧计划版本复制到新计划版本。</span><span class="sxs-lookup"><span data-stu-id="23d89-127">To achieve this behavior, the planning logic copies planned orders that have a status of *Approved* from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="23d89-128">请注意，状态为 *已审核* 的计划订单仅在特定主计划内视为供应。</span><span class="sxs-lookup"><span data-stu-id="23d89-128">Note that planned orders that have a status of *Approved* are considered supply only within the specific master plan.</span></span>

<span data-ttu-id="23d89-129">要更改单个计划订单的状态，[打开任何计划订单列表页](#view-planned-orders)，打开订单，然后执行以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="23d89-129">To change the status of a single planned order, [open any planned orders list page](#view-planned-orders), open the order, and then follow one of these steps:</span></span>

- <span data-ttu-id="23d89-130">在 **常规** 快速选项卡上，更改 **状态** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="23d89-130">On the **General** FastTab, change the value of the **Status** field.</span></span>
- <span data-ttu-id="23d89-131">在操作窗格的 **计划订单** 选项卡上，在 **流程** 组中，选择 **更改状态**。</span><span class="sxs-lookup"><span data-stu-id="23d89-131">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="23d89-132">在操作窗格上，选择 **审核** 将订单标记为已审核。</span><span class="sxs-lookup"><span data-stu-id="23d89-132">On the Action Pane, select **Approve** to mark the order as approved.</span></span>

<span data-ttu-id="23d89-133">要同时更改多个计划订单的状态，[打开任何计划订单列表页](#view-planned-orders)，选中要更改的每个订单的复选框，然后执行以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="23d89-133">To change the status of several planned orders at the same time, [open any planned orders list page](#view-planned-orders), select the check box for each order that you want to change, and then follow one of these steps:</span></span>

- <span data-ttu-id="23d89-134">在操作窗格的 **计划订单** 选项卡上，在 **流程** 组中，选择 **更改状态**。</span><span class="sxs-lookup"><span data-stu-id="23d89-134">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="23d89-135">在操作窗格上，选择 **审核** 将订单标记为已审核。</span><span class="sxs-lookup"><span data-stu-id="23d89-135">On the Action Pane, select **Approve** to mark the orders as approved.</span></span>

## <a name="approve-planned-orders"></a><span data-ttu-id="23d89-136">审核计划订单</span><span class="sxs-lookup"><span data-stu-id="23d89-136">Approve planned orders</span></span>

<span data-ttu-id="23d89-137">审核计划订单是从计划订单创建确认订单过程中的可选步骤。</span><span class="sxs-lookup"><span data-stu-id="23d89-137">Approval of planned orders is an optional step in the process of creating a firmed order from a planned order.</span></span>

<span data-ttu-id="23d89-138">下图显示了如何使用分配给每个计划订单的 **状态** 值来实施审核工作流。</span><span class="sxs-lookup"><span data-stu-id="23d89-138">The following illustration shows how you can use the **Status** value that is assigned to each planned order to implement an approval workflow.</span></span> <span data-ttu-id="23d89-139">要实施审核流程，请按照上一节中所述为每个计划订单手动调整 **状态** 值。</span><span class="sxs-lookup"><span data-stu-id="23d89-139">To implement an approval process, manually adjust the **Status** value for each planned order as described in the previous section.</span></span>

![计划订单流](media/approved-planned-orders-1.png)

> [!TIP]
> <span data-ttu-id="23d89-141">我们建议您审核所有修改的计划订单。</span><span class="sxs-lookup"><span data-stu-id="23d89-141">We recommend that you approve any modified planned orders.</span></span> <span data-ttu-id="23d89-142">否则，所做编辑将被下一次计划运行忽略和覆盖。</span><span class="sxs-lookup"><span data-stu-id="23d89-142">Otherwise, the edits will be ignored and overwritten by the next planning run.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="23d89-143">其他资源</span><span class="sxs-lookup"><span data-stu-id="23d89-143">Additional resources</span></span>

- [<span data-ttu-id="23d89-144">确定计划订单</span><span class="sxs-lookup"><span data-stu-id="23d89-144">Firm planned orders</span></span>](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

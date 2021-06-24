---
title: 取消销售订单时不能减少数量
description: 取消销售订单时不能减少数量。
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230828"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a><span data-ttu-id="027b9-103">取消销售订单时不能减少数量</span><span class="sxs-lookup"><span data-stu-id="027b9-103">The quantity can't be reduced when a sales order is canceled</span></span>

<span data-ttu-id="027b9-104">错误代码：SYS138831</span><span class="sxs-lookup"><span data-stu-id="027b9-104">Error code: SYS138831</span></span>

## <a name="symptoms"></a><span data-ttu-id="027b9-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="027b9-105">Symptoms</span></span>

<span data-ttu-id="027b9-106">系统将显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="027b9-106">The system shows the following error message:</span></span>

> <span data-ttu-id="027b9-107">数量不能减少。</span><span class="sxs-lookup"><span data-stu-id="027b9-107">The quantity cannot be reduced.</span></span> <span data-ttu-id="027b9-108">订单上的库存交易数量太少，因为数量或部分数量由输出订单或生产订单引用，或者针对其他交易进行标记。</span><span class="sxs-lookup"><span data-stu-id="027b9-108">The number of inventory transactions on order is too low because the quantity or part of it is referenced by an output order or a production order or is marked against other transactions.</span></span>

## <a name="cause"></a><span data-ttu-id="027b9-109">原因</span><span class="sxs-lookup"><span data-stu-id="027b9-109">Cause</span></span>

<span data-ttu-id="027b9-110">如果工作与销售订单相关联，在取消和冲销工作之前，您不能取消销售订单。</span><span class="sxs-lookup"><span data-stu-id="027b9-110">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="027b9-111">即使与销售订单关联的工作已关闭，此要求也适用。</span><span class="sxs-lookup"><span data-stu-id="027b9-111">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

## <a name="resolution"></a><span data-ttu-id="027b9-112">解决方法</span><span class="sxs-lookup"><span data-stu-id="027b9-112">Resolution</span></span>

<span data-ttu-id="027b9-113">若要解决此问题，请完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="027b9-113">To fix this issue, complete the following tasks:</span></span>

1. <span data-ttu-id="027b9-114">取消未结工作。</span><span class="sxs-lookup"><span data-stu-id="027b9-114">Cancel open work.</span></span>
1. <span data-ttu-id="027b9-115">删除负荷。</span><span class="sxs-lookup"><span data-stu-id="027b9-115">Delete the load.</span></span>
1. <span data-ttu-id="027b9-116">减少领料数量。</span><span class="sxs-lookup"><span data-stu-id="027b9-116">Reduce the picked quantity.</span></span>

### <a name="cancel-open-work"></a><span data-ttu-id="027b9-117">取消未结工作</span><span class="sxs-lookup"><span data-stu-id="027b9-117">Cancel open work</span></span>

<span data-ttu-id="027b9-118">若要取消未结工作，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="027b9-118">To cancel open work, follow these steps.</span></span>

1. <span data-ttu-id="027b9-119">转到 **仓库管理 \> 定期任务 \> 清理 \> 取消工作**。</span><span class="sxs-lookup"><span data-stu-id="027b9-119">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="027b9-120">在 **工作 ID** 字段中，指定您要取消的当前的 **工作状态** 值为 *打开*、*进行中*、*已取消*、*已合并* 或 *已关闭* 的工作的 ID。</span><span class="sxs-lookup"><span data-stu-id="027b9-120">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="027b9-121">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="027b9-121">Select **OK**.</span></span>
1. <span data-ttu-id="027b9-122">选择 **是** 确认要取消该工作。</span><span class="sxs-lookup"><span data-stu-id="027b9-122">Select **Yes** to confirm that you want to cancel the work.</span></span>

### <a name="delete-the-load"></a><span data-ttu-id="027b9-123">删除负荷</span><span class="sxs-lookup"><span data-stu-id="027b9-123">Delete the load</span></span>

<span data-ttu-id="027b9-124">若要删除负荷，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="027b9-124">To delete a load, follow these steps.</span></span>

1. <span data-ttu-id="027b9-125">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="027b9-125">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="027b9-126">打开相关销售订单。</span><span class="sxs-lookup"><span data-stu-id="027b9-126">Open the relevant sales order.</span></span>
1. <span data-ttu-id="027b9-127">在 **销售订单行** 快速选项卡上，选择 **仓库 \> 工作详细信息**。</span><span class="sxs-lookup"><span data-stu-id="027b9-127">On the **Sales order lines** FastTab, select **Warehouse \> Work details**.</span></span>
1. <span data-ttu-id="027b9-128">在 **工作** 页面的操作窗格上，在 **工作** 选项卡上的 **工作** 组中，选择 **取消工作**。</span><span class="sxs-lookup"><span data-stu-id="027b9-128">On the **Work** page, on the Action Pane, on the **Work** tab, in the **Work** group, select **Cancel work**.</span></span>
1. <span data-ttu-id="027b9-129">确认 **工作状态** 字段设置为 *已取消*。</span><span class="sxs-lookup"><span data-stu-id="027b9-129">Confirm that the **Work status** field is set to *Canceled*.</span></span>
1. <span data-ttu-id="027b9-130">关闭 **工作** 页面。</span><span class="sxs-lookup"><span data-stu-id="027b9-130">Close the **Work** page.</span></span>
1. <span data-ttu-id="027b9-131">在销售订单详细信息页面的 **销售订单行** 快速选项卡上，选择 **仓库 \> 加载详细信息**。</span><span class="sxs-lookup"><span data-stu-id="027b9-131">On the sales order details page, on the **Sales order lines** FastTab, select **Warehouse \> Load details**.</span></span>
1. <span data-ttu-id="027b9-132">在操作窗格上，选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="027b9-132">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="027b9-133">选择 **是** 以确认要删除负荷。</span><span class="sxs-lookup"><span data-stu-id="027b9-133">Select **Yes** to confirm that you want to delete the load.</span></span>
1. <span data-ttu-id="027b9-134">关闭 **负荷** 页面。</span><span class="sxs-lookup"><span data-stu-id="027b9-134">Close the **Load** page.</span></span>

### <a name="reduce-the-picked-quantity"></a><span data-ttu-id="027b9-135">减少领料数量</span><span class="sxs-lookup"><span data-stu-id="027b9-135">Reduce the picked quantity</span></span>

<span data-ttu-id="027b9-136">取消所有工作后，请按照以下步骤减少领料数量。</span><span class="sxs-lookup"><span data-stu-id="027b9-136">After all work has been canceled, follow these steps to reduce the picked quantity.</span></span>

1. <span data-ttu-id="027b9-137">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="027b9-137">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="027b9-138">打开相关销售订单。</span><span class="sxs-lookup"><span data-stu-id="027b9-138">Open the relevant sales order.</span></span>
1. <span data-ttu-id="027b9-139">在 **销售订单行** 快速选项卡上，从工具栏中选择 **更新行 \> 领料**。</span><span class="sxs-lookup"><span data-stu-id="027b9-139">On the **Sales order lines** FastTab, select **Update line \> Pick** from the toolbar.</span></span>
1. <span data-ttu-id="027b9-140">在 **领料** 页面的 **交易** 部分中，选择 **发放状态** 字段设置为 *已领料* 的行。</span><span class="sxs-lookup"><span data-stu-id="027b9-140">On the **Pick** page, in the **Transactions** section, select the line where the **Issue status** field is set to *Picked*.</span></span>
1. <span data-ttu-id="027b9-141">在 **交易** 部分中，从工具栏中选择 **添加领料行**。</span><span class="sxs-lookup"><span data-stu-id="027b9-141">In the **Transactions** section, select **Add picking line** from the toolbar.</span></span>
1. <span data-ttu-id="027b9-142">在 **领料行** 部分中，从工具栏中选择 **确认全部领料**。</span><span class="sxs-lookup"><span data-stu-id="027b9-142">In the **Picking lines** section, select **Confirm pick all** from the toolbar.</span></span>
1. <span data-ttu-id="027b9-143">关闭 **领料** 页面。</span><span class="sxs-lookup"><span data-stu-id="027b9-143">Close the **Pick** page.</span></span>
1. <span data-ttu-id="027b9-144">在销售订单详细信息页面的操作窗格上，在 **销售订单** 选项卡的 **维护** 组中，选择 **取消**。</span><span class="sxs-lookup"><span data-stu-id="027b9-144">On the sales order details page, on the Action Pane, on the **Sales order** tab, in the **Maintain** group, select **Cancel**.</span></span>
1. <span data-ttu-id="027b9-145">选择 **是** 以确认要取消销售订单。</span><span class="sxs-lookup"><span data-stu-id="027b9-145">Select **Yes** to confirm that you want to cancel the sales order.</span></span>

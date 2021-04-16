---
title: 登陆成本查询
description: 本主题介绍如何查找和使用可用于登陆成本模块的各个类型的查询。
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMLine, ITMItemTracking, ITMContainerActivityTracking, ITMContainerTracking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 22a2e76780adb43b053b6cf7fd08411a4a60aeac
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823353"
---
# <a name="landed-cost-inquiries"></a><span data-ttu-id="dd2f9-103">登陆成本查询</span><span class="sxs-lookup"><span data-stu-id="dd2f9-103">Landed cost inquiries</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="voyage-line-inquiries"></a><span data-ttu-id="dd2f9-104">航行行查询</span><span class="sxs-lookup"><span data-stu-id="dd2f9-104">Voyage line inquiries</span></span>

<span data-ttu-id="dd2f9-105">**航行行** 查询显示所有与库存有关的航行行。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-105">The **Voyage lines** inquiry shows all voyage lines as they pertain to inventory.</span></span> <span data-ttu-id="dd2f9-106">此查询可以用作筛选器来帮助您查找物料、采购订单或其他有用的信息。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-106">This inquiry can be used as a filter to help you find an item, purchase order, or other useful piece of information.</span></span> <span data-ttu-id="dd2f9-107">它还可以用于确定可能在一个或多个航行中的物料的预期交货日期。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-107">It can also be used to identify the expected delivery date of an item that might be on one or more voyages.</span></span> <span data-ttu-id="dd2f9-108">通过这种方式，它可以帮助您管理预期库存接收。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-108">In this way, it can help you manage expected inventory receiving.</span></span>

<span data-ttu-id="dd2f9-109">要打开此查询，请转到 **登陆成本 \> 查询 \> 航行行**。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-109">To open this inquiry, go to **Landed cost \> Inquiries \> Voyage lines**.</span></span>

### <a name="overview-tab"></a><span data-ttu-id="dd2f9-110">“概览”选项卡</span><span class="sxs-lookup"><span data-stu-id="dd2f9-110">Overview tab</span></span>

<span data-ttu-id="dd2f9-111">**航行行** 查询页的 **概览** 选项卡包括一个网格，其中显示有关每个相关航行行的基本信息。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-111">The **Overview** tab of the **Voyage lines** inquiry page includes a grid that shows basic information about each relevant voyage line.</span></span> <span data-ttu-id="dd2f9-112">下表描述了网格中的列。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-112">The following table describes the columns in the grid.</span></span>

| <span data-ttu-id="dd2f9-113">列</span><span class="sxs-lookup"><span data-stu-id="dd2f9-113">Column</span></span> | <span data-ttu-id="dd2f9-114">说明</span><span class="sxs-lookup"><span data-stu-id="dd2f9-114">Description</span></span> |
|---|---|
| <span data-ttu-id="dd2f9-115">**物料编号**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-115">**Item number**</span></span> | <span data-ttu-id="dd2f9-116">航行行的物料。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-116">The item for the voyage line.</span></span> |
| <span data-ttu-id="dd2f9-117">**参考**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-117">**Reference**</span></span> | <span data-ttu-id="dd2f9-118">订单的类型（采购订单或转移单）。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-118">The type of order (purchase order or transfer order).</span></span> |
| <span data-ttu-id="dd2f9-119">**数值**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-119">**Number**</span></span> | <span data-ttu-id="dd2f9-120">采购订单编号或转移单号。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-120">The purchase order number or transfer order number.</span></span> |
| <span data-ttu-id="dd2f9-121">**帐页**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-121">**Folio**</span></span> | <span data-ttu-id="dd2f9-122">与航行行关联的帐页。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-122">The folio that is associated with the voyage line.</span></span> |
| <span data-ttu-id="dd2f9-123">**装运集装箱**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-123">**Shipping container**</span></span> | <span data-ttu-id="dd2f9-124">与航行行关联的装运集装箱。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-124">The shipping container that is associated with the voyage line.</span></span> |
| <span data-ttu-id="dd2f9-125">**航行**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-125">**Voyage**</span></span> | <span data-ttu-id="dd2f9-126">与航行行关联的航行。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-126">The voyage that is associated with the voyage line.</span></span> |
| <span data-ttu-id="dd2f9-127">**数量**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-127">**Quantity**</span></span> | <span data-ttu-id="dd2f9-128">航行行的物料的数量。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-128">The quantity of the item for the voyage line.</span></span> |
| <span data-ttu-id="dd2f9-129">（其他维度）</span><span class="sxs-lookup"><span data-stu-id="dd2f9-129">(Other dimensions)</span></span> | <span data-ttu-id="dd2f9-130">您可以根据需要显示其他维度的列。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-130">You can show columns for additional dimensions as you require.</span></span> <span data-ttu-id="dd2f9-131">这些维度包括批处理号、库存状态和仓库。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-131">Those dimensions include batch number, inventory status, and warehouse.</span></span> <span data-ttu-id="dd2f9-132">在操作窗格上，选择 **库存 \> 显示维度** 打开一个对话框，您可以在其中选择要包括的维度。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-132">On the Action Pane, select **Inventory \> Display dimensions** to open a dialog box where you can select the dimensions to include.</span></span> |

### <a name="general-tab"></a><span data-ttu-id="dd2f9-133">常规选项卡</span><span class="sxs-lookup"><span data-stu-id="dd2f9-133">General tab</span></span>

<span data-ttu-id="dd2f9-134">选择 **常规** 选项卡查看有关当前在 **概览** 选项卡上选择的行的更多信息。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-134">Select the **General** tab to view more information about the line that is currently selected on the **Overview** tab.</span></span>

### <a name="dimensions-tab"></a><span data-ttu-id="dd2f9-135">“维度”选项卡</span><span class="sxs-lookup"><span data-stu-id="dd2f9-135">Dimensions tab</span></span>

<span data-ttu-id="dd2f9-136">选择 **维度** 选项卡可以查看当前在 **概览** 选项卡上选择的行的所有可用维度的值，不论您选择在该选项卡上显示哪些维度。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-136">Select the **Dimensions** tab to view values for all available dimensions for the line that is currently selected on the **Overview** tab, regardless of the dimensions that you've selected to show on that tab.</span></span>

## <a name="cost-estimate-inquiries"></a><span data-ttu-id="dd2f9-137">成本估计查询</span><span class="sxs-lookup"><span data-stu-id="dd2f9-137">Cost estimate inquiries</span></span>

<span data-ttu-id="dd2f9-138">每次您生成成本估计时，估计都会添加到 **成本估计** 查询页。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-138">Every time that you generate a cost estimate, the estimate is added to the **Cost estimates** inquiry page.</span></span> <span data-ttu-id="dd2f9-139">有关如何生成、查看和使用成本估计（包括查询页上的估计）的完整详细信息，请参阅[估计和管理登陆成本](estimate-manage-landed-costs.md)。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-139">For complete details about how to generate, view, and work with cost estimates (including estimates on the inquiry page), see [Estimate and manage landed costs](estimate-manage-landed-costs.md).</span></span>

## <a name="item-tracking"></a><span data-ttu-id="dd2f9-140">物料跟踪</span><span class="sxs-lookup"><span data-stu-id="dd2f9-140">Item tracking</span></span>

<span data-ttu-id="dd2f9-141">使用 **物料追踪** 页可以查看未结采购订单行及其当前状态。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-141">Use the **Item tracking** page to view open purchase orders lines and their current status.</span></span> <span data-ttu-id="dd2f9-142">行不一定必须与航行关联才能显示在此处。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-142">Lines don't have to be associated with a voyage to appear here.</span></span> <span data-ttu-id="dd2f9-143">但是，如果物料与航行关联，物料跟踪记录行将显示航行 ID。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-143">However, if an item is associated with a voyage, the item tracking record line shows the voyage ID.</span></span>

<span data-ttu-id="dd2f9-144">要打开此页面，请转到 **登陆成本 \> 查询 \> 跟踪 \> 物料跟踪**。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-144">To open this page, go to **Landed cost \> Inquiries \> Tracking \> Item tracking**.</span></span>

<span data-ttu-id="dd2f9-145">由于您的系统可能包含大量的采购订单行，因此 **物料跟踪** 页最初未显示记录。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-145">Because your system probably contains a very large number of purchase order lines, the **Item tracking** page initially shows no records.</span></span> <span data-ttu-id="dd2f9-146">首先使用页面顶部的筛选器字段定义您要查找的采购订单行集。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-146">Start by using the filter fields at the top of the page to define the set of purchase order lines that you're looking for.</span></span> <span data-ttu-id="dd2f9-147">然后在操作窗格上选择 **更新** 生成列表。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-147">Then select **Update** on the Action Pane to generate the list.</span></span> <span data-ttu-id="dd2f9-148">您可以使用星号 (\*) 作为任何筛选器字段中的通配符。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-148">You can use an asterisk (\*) as a wildcard character in any of the filter fields.</span></span> <span data-ttu-id="dd2f9-149">例如，要查找名称中包含“DVD”一词的物料的所有采购订单行，请将 **类型** 字段设置为 **产品名称**，然后在 **字段值** 字段中输入 *\*DVD\**。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-149">For example, to find all purchase order lines for items that include the word "DVD" in their name, set the **Type** field to **Product name**, and enter *\*DVD\** in the **Field value** field.</span></span>

> [!NOTE]
> <span data-ttu-id="dd2f9-150">当前，延期交货仅包括销售订单。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-150">Currently, backorders include only sales orders.</span></span> <span data-ttu-id="dd2f9-151">销售报价单未显示或被视为延期交货。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-151">Sales quotations aren't shown or considered backorders.</span></span>

<span data-ttu-id="dd2f9-152">下表描述了 **物料跟踪** 页上网格中的列。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-152">The following table describes the columns in the grid on the **Item tracking** page.</span></span>

| <span data-ttu-id="dd2f9-153">列</span><span class="sxs-lookup"><span data-stu-id="dd2f9-153">Column</span></span> | <span data-ttu-id="dd2f9-154">说明</span><span class="sxs-lookup"><span data-stu-id="dd2f9-154">Description</span></span> |
|---|---|
| <span data-ttu-id="dd2f9-155">**目标港口**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-155">**To port**</span></span> | <span data-ttu-id="dd2f9-156">最终目的地。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-156">The final destination.</span></span> |
| <span data-ttu-id="dd2f9-157">**已确认**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-157">**Confirmed**</span></span> | <span data-ttu-id="dd2f9-158">采购订单行的确认日期。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-158">The confirmed date of the purchase order line.</span></span> |
| <span data-ttu-id="dd2f9-159">**交货日期**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-159">**Delivery Date**</span></span> | <span data-ttu-id="dd2f9-160">采购订单行的交货日期。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-160">The delivery date of the purchase order line.</span></span> |
| <span data-ttu-id="dd2f9-161">**航行**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-161">**Voyage**</span></span> | <span data-ttu-id="dd2f9-162">如果行与航行关联，为航行 ID。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-162">If the line is associated with a voyage, the voyage ID.</span></span> |
| <span data-ttu-id="dd2f9-163">**装运集装箱**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-163">**Shipping Container**</span></span> | <span data-ttu-id="dd2f9-164">如果行附加到装运集装箱，为集装箱 ID。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-164">If the line is attached to a shipping container, the container ID.</span></span> |
| <span data-ttu-id="dd2f9-165">**装运港口**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-165">**Shipping port**</span></span> | <span data-ttu-id="dd2f9-166">当前港口，基于未为与采购订单行关联的装运集装箱设置实际日期的跟踪窗体中的第一个支线。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-166">The current port, based on the first leg in the tracking form where no actual date is set for the shipping container that is associated with the purchase order line.</span></span> |
| <span data-ttu-id="dd2f9-167">**活动**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-167">**Activity**</span></span> | <span data-ttu-id="dd2f9-168">当前活动，基于未为与采购订单行关联的装运集装箱设置实际日期的跟踪窗体中的第一个支线。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-168">The current activity, based on the first leg in the tracking form where no actual date is set for the shipping container that is associated with the purchase order line.</span></span> |
| <span data-ttu-id="dd2f9-169">**估计结束日期**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-169">**Estimated end date**</span></span> | <span data-ttu-id="dd2f9-170">预期在目标仓库接收航行的日期。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-170">The date when the voyage is expected to be received at the destination warehouse.</span></span> |
| <span data-ttu-id="dd2f9-171">**姓名**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-171">**Name**</span></span> | <span data-ttu-id="dd2f9-172">供应商的名称。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-172">The name of the vendor.</span></span> |
| <span data-ttu-id="dd2f9-173">**航行状态**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-173">**Voyage Status**</span></span> | <span data-ttu-id="dd2f9-174">附加到采购订单行的装运状态。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-174">The shipment status that is attached to the purchase order line.</span></span> |
| <span data-ttu-id="dd2f9-175">**物料编号**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-175">**Item number**</span></span> | <span data-ttu-id="dd2f9-176">采购订单行的物料编号。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-176">The item number for the purchase order line.</span></span> |
| <span data-ttu-id="dd2f9-177">**外部**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-177">**External**</span></span> | <span data-ttu-id="dd2f9-178">供应商物料名称。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-178">The vendor's item name.</span></span> |
| <span data-ttu-id="dd2f9-179">**产品名称**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-179">**Product Name**</span></span> | <span data-ttu-id="dd2f9-180">采购订单行的物料的名称。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-180">The name of the item for the purchase order line.</span></span> |
| <span data-ttu-id="dd2f9-181">**数量**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-181">**Quantity**</span></span> | <span data-ttu-id="dd2f9-182">采购订单行的采购订单行数量。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-182">The purchase order line quantity for the purchase order line.</span></span> |
| <span data-ttu-id="dd2f9-183">**单位**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-183">**Unit**</span></span> | <span data-ttu-id="dd2f9-184">采购订单行的度量单位。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-184">The unit of measure for the purchase order line.</span></span> |
| <span data-ttu-id="dd2f9-185">**参考**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-185">**Reference**</span></span> | <span data-ttu-id="dd2f9-186">订单的类型（采购订单或转移单）</span><span class="sxs-lookup"><span data-stu-id="dd2f9-186">The type of order (purchase order or transfer order)</span></span> |
| <span data-ttu-id="dd2f9-187">**参考编号**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-187">**Reference number**</span></span> | <span data-ttu-id="dd2f9-188">采购订单编号或转移单号。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-188">The purchase order number or transfer order number.</span></span> |
| <span data-ttu-id="dd2f9-189">**延期交货**</span><span class="sxs-lookup"><span data-stu-id="dd2f9-189">**Backorder**</span></span> | <span data-ttu-id="dd2f9-190">符号表示物料有销售延期交货。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-190">A symbol indicates that there are sales backorders for the item.</span></span> |
| <span data-ttu-id="dd2f9-191">（其他维度）</span><span class="sxs-lookup"><span data-stu-id="dd2f9-191">(Other dimensions)</span></span> | <span data-ttu-id="dd2f9-192">您可以根据需要显示其他维度的列。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-192">You can show columns for additional dimensions as you require.</span></span> <span data-ttu-id="dd2f9-193">这些维度包括批处理号、库存状态和仓库。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-193">Those dimensions include batch number, inventory status, and warehouse.</span></span> <span data-ttu-id="dd2f9-194">在操作窗格上，选择 **显示维度** 打开一个对话框，您可以在其中选择要包括的维度。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-194">On the Action Pane, select **Display dimensions** to open a dialog box where you can select the dimensions to include.</span></span> |

### <a name="related-information-about-backorders"></a><span data-ttu-id="dd2f9-195">延期交货的相关信息</span><span class="sxs-lookup"><span data-stu-id="dd2f9-195">Related information about backorders</span></span>

<span data-ttu-id="dd2f9-196">要查看有关延期交货的详细信息，请选择页面右侧的 **相关信息** 选项卡，然后选择 **延期交货**。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-196">To view more information about backorders, select the **Related information** tab on the right side of the page, and then select **Backorders**.</span></span> <span data-ttu-id="dd2f9-197">要查看有关特定延期交货的详细信息，请选择它的行，然后选择 **更多** 链接。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-197">To view even more information about a specific backorder, select the row for it, and then select the **More** link.</span></span>

## <a name="individual-shipping-container-tracking"></a><span data-ttu-id="dd2f9-198">单个装运集装箱跟踪</span><span class="sxs-lookup"><span data-stu-id="dd2f9-198">Individual shipping container tracking</span></span>

<span data-ttu-id="dd2f9-199">**单个装运集装箱跟踪** 查询提供一个筛选器，可让您查找一个装运集装箱，然后确定该集装箱中的所有航行行。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-199">The **Individual shipping container tracking** inquiry provides a filter that lets you find a shipping container and then identify all the voyage lines in that container.</span></span>

<span data-ttu-id="dd2f9-200">要打开此查询，请转到 **登陆成本 \> 查询 \> 跟踪 \> 单个装运集装箱跟踪**。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-200">To open this inquiry, go to **Landed cost \> Inquiries \> Tracking \> Individual shipping container tracking**.</span></span>

## <a name="multiple-shipping-container-tracking"></a><span data-ttu-id="dd2f9-201">多个装运集装箱跟踪</span><span class="sxs-lookup"><span data-stu-id="dd2f9-201">Multiple shipping container tracking</span></span>

<span data-ttu-id="dd2f9-202">**多个装运集装箱跟踪** 查询提供一个筛选器，可让您查找装运集装箱集合，然后确定这些集装箱中的所有航行行。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-202">The **Multiple shipping container tracking** inquiry provides a filter that lets you find a collection of shipping containers and then identify all the voyage lines in those containers.</span></span>

<span data-ttu-id="dd2f9-203">要打开此查询，请转到 **登陆成本 \> 查询 \> 跟踪 \> 多个装运集装箱跟踪**。</span><span class="sxs-lookup"><span data-stu-id="dd2f9-203">To open this inquiry, go to **Landed cost \> Inquiries \> Tracking \> Multiple shipping container tracking**.</span></span>

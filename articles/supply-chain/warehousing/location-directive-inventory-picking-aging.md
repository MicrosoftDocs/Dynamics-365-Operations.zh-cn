---
title: 库位指令库存领料帐龄
description: 本主题说明在领料过程中如何使用先进先出 (FIFO) 和后进先出 (LIFO) 位置指令策略。
author: mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSWorkTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: f8d5e4d82c66d178ceafcdbfb3eb9a941172aa01
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004619"
---
# <a name="location-directive-inventory-picking-aging"></a><span data-ttu-id="44900-103">库位指令库存领料帐龄</span><span class="sxs-lookup"><span data-stu-id="44900-103">Location directive inventory picking aging</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44900-104">本主题说明在领料过程中如何使用先进先出 (FIFO) 和后进先出 (LIFO) 位置指令策略。</span><span class="sxs-lookup"><span data-stu-id="44900-104">This topic explains how to use first in, first out (FIFO) and last in, first out (LIFO) location directive strategies during picking.</span></span> <span data-ttu-id="44900-105">这些策略与为位置记录的帐龄日期结合用来跟踪库存初次进入仓库的时间。</span><span class="sxs-lookup"><span data-stu-id="44900-105">These strategies work in conjunction with the aging dates that are recorded for locations to track when inventory first entered the warehouse.</span></span> <span data-ttu-id="44900-106">*位置指令库存领料帐龄* 功能使用位置上的日期来确定帐龄。</span><span class="sxs-lookup"><span data-stu-id="44900-106">The *Location directive inventory picking aging* feature uses the date on the location to determine aging.</span></span> <span data-ttu-id="44900-107">*仓库位置状态* 功能根据牌照上的日期更新位置上的日期。</span><span class="sxs-lookup"><span data-stu-id="44900-107">The *Warehouse location status* feature updates the date on the location, based on the date from the license plate.</span></span>

<span data-ttu-id="44900-108">您可以使用 FIFO 和 LIFO 策略根据库存进入仓库的日期来装运批量跟踪物料和非批量跟踪物料。</span><span class="sxs-lookup"><span data-stu-id="44900-108">You can use FIFO and LIFO strategies to ship both batch-tracked items and non-batch-tracked items, based on the date when the inventory entered the warehouse.</span></span> <span data-ttu-id="44900-109">此功能对于无法使用到期日期进行分类的非批量跟踪库存特别有用。</span><span class="sxs-lookup"><span data-stu-id="44900-109">This capability can be especially useful for non-batch-tracked inventory, where an expiration date isn't available to use for sorting.</span></span>

<span data-ttu-id="44900-110">在仓库中初次收到或创建库存时，系统会更新相关牌照，以将当前日期显示为帐龄日期。</span><span class="sxs-lookup"><span data-stu-id="44900-110">When inventory is first received or created in the warehouse, the system updates the relevant license plate so that the current date is shown as the aging date.</span></span> <span data-ttu-id="44900-111">然后，位置指令策略会使用此日期来识别仓库中最旧或最新的库存。</span><span class="sxs-lookup"><span data-stu-id="44900-111">This date is then used by the location directive strategies to identify the oldest or newest inventory in the warehouse.</span></span> <span data-ttu-id="44900-112">如果将库存移动到牌照未跟踪的位置，该位置本身会使用帐龄信息更新，然后此策略将使用此信息。</span><span class="sxs-lookup"><span data-stu-id="44900-112">If inventory is moved to a location that isn't tracked by license plate, the location itself is updated with aging information, and this information will then be used by the strategies.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="44900-113">开启功能</span><span class="sxs-lookup"><span data-stu-id="44900-113">Turn on the feature</span></span>

<span data-ttu-id="44900-114">要使此功能可用，请在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中按此顺序打开以下功能：</span><span class="sxs-lookup"><span data-stu-id="44900-114">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), in this order:</span></span>

1. <span data-ttu-id="44900-115">仓库库位状态</span><span class="sxs-lookup"><span data-stu-id="44900-115">Warehouse location status</span></span>
1. <span data-ttu-id="44900-116">库位指令库存领料帐龄</span><span class="sxs-lookup"><span data-stu-id="44900-116">Location directive inventory picking aging</span></span>

## <a name="feature-requirements"></a><span data-ttu-id="44900-117">功能要求</span><span class="sxs-lookup"><span data-stu-id="44900-117">Feature requirements</span></span>

<span data-ttu-id="44900-118">要使用此功能，必须将用于存储库存的每个 [位置模板](tasks/create-location-profile.md)的 **启用位置状态** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="44900-118">To use this feature, you must set the **Enable location status** option set to *Yes* for every [location profile](tasks/create-location-profile.md) that is used to store inventory.</span></span> <span data-ttu-id="44900-119">要为位置模板设置此选项，请转到 **仓库管理 \> 设置 \> 仓库 \> 位置模板**，选择位置模板。</span><span class="sxs-lookup"><span data-stu-id="44900-119">To set this option for a location profile, go to **Warehouse management \> Setup \> Warehouse \> Location profiles**, and select the location profile.</span></span> <span data-ttu-id="44900-120">您可以在 **常规** 快速选项卡上找到此选项。</span><span class="sxs-lookup"><span data-stu-id="44900-120">You can find the option on the **General** FastTab.</span></span>

## <a name="feature-scenarios"></a><span data-ttu-id="44900-121">功能方案</span><span class="sxs-lookup"><span data-stu-id="44900-121">Feature scenarios</span></span>

<span data-ttu-id="44900-122">本节提供演示如何设置和使用 FIFO 和 LIFO 策略的示例。</span><span class="sxs-lookup"><span data-stu-id="44900-122">This section provides examples that show how to set up and use FIFO and LIFO strategies.</span></span>

> [!TIP]
> <span data-ttu-id="44900-123">本节提供了两个方案，一种用于 FIFO，一种用于 LIFO。</span><span class="sxs-lookup"><span data-stu-id="44900-123">This section provides two scenarios, one for FIFO and one for LIFO.</span></span> <span data-ttu-id="44900-124">所提供的过程假定您将按顺序执行这两个方案。</span><span class="sxs-lookup"><span data-stu-id="44900-124">The procedures that are provided assume that you will do both scenarios, in order.</span></span> <span data-ttu-id="44900-125">我们建议您两个方案全部执行，这样可以体验两个策略之间的差异。</span><span class="sxs-lookup"><span data-stu-id="44900-125">We recommend that you do both scenarios, so that you can experience the differences between the two strategies.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="44900-126">提供示例数据</span><span class="sxs-lookup"><span data-stu-id="44900-126">Make sample data available</span></span>

<span data-ttu-id="44900-127">若要使用此处指定的示例记录和值完成这些场景，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="44900-127">To work through these scenarios by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="44900-128">此外，开始前，还必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="44900-128">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="44900-129">您还可以将这些方案用作在生产系统上使用此功能的指导。</span><span class="sxs-lookup"><span data-stu-id="44900-129">You can also use these scenarios as guidance for using the feature on a production system.</span></span> <span data-ttu-id="44900-130">但是，如果是这样，您必须替换这里介绍的每个设置中的自己的值。</span><span class="sxs-lookup"><span data-stu-id="44900-130">However, in that case, you must substitute your own values for each setting that is described here.</span></span>

### <a name="set-up-the-scenarios"></a><a name="demo-set-up"></a><span data-ttu-id="44900-131">设置方案</span><span class="sxs-lookup"><span data-stu-id="44900-131">Set up the scenarios</span></span>

<span data-ttu-id="44900-132">演示数据需要设置并进行库存调整来支持方案。</span><span class="sxs-lookup"><span data-stu-id="44900-132">The demo data requires setup and inventory adjustments to support the scenarios.</span></span> <span data-ttu-id="44900-133">请按照以下步骤创建演练 FIFO 和 LIFO 方案所需的库存数据。</span><span class="sxs-lookup"><span data-stu-id="44900-133">Follow these steps to create the inventory data that is required to work through the FIFO and LIFO scenarios.</span></span>

1. <span data-ttu-id="44900-134">登录到安装了演示数据的系统，然后选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="44900-134">Sign in to a system where demo data is installed, and select the **USMF** legal entity.</span></span>
1. <span data-ttu-id="44900-135">转到 **仓库管理 \> 设置 \> 仓库 \> 货位模板**。</span><span class="sxs-lookup"><span data-stu-id="44900-135">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="44900-136">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="44900-136">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="44900-137">在位置模板列表中，选择 **FLOOR-05**。</span><span class="sxs-lookup"><span data-stu-id="44900-137">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="44900-138">在 **常规** 快速选项卡上，将 **启用位置状态** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="44900-138">On the **General** FastTab, set the **Enable location status** option to *Yes*.</span></span>
1. <span data-ttu-id="44900-139">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="44900-139">Select **Save**.</span></span>
1. <span data-ttu-id="44900-140">转到 **库存管理 \> 设置 \> 位置指令**。</span><span class="sxs-lookup"><span data-stu-id="44900-140">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="44900-141">在位置指令列表中，选择 **63 领料集装化**。</span><span class="sxs-lookup"><span data-stu-id="44900-141">In the list of location directives, select **63 Pick containerization**.</span></span>
1. <span data-ttu-id="44900-142">选择 **编辑** 将页面设置为编辑模式。</span><span class="sxs-lookup"><span data-stu-id="44900-142">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="44900-143">在 **位置指令操作** 快速选项卡上，找到 **序列号** 字段设置为 *1* 的行，然后执行以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="44900-143">On the **Location directive actions** FastTab, find the line where the **Sequence number** field is set to *1*, and follow one of these steps:</span></span>

    - <span data-ttu-id="44900-144">如果您要设置 FIFO 方案，请将 **策略** 字段的值更改为 *位置帐龄 FIFO*。</span><span class="sxs-lookup"><span data-stu-id="44900-144">If you're setting up a FIFO scenario, change the value of the **Strategy** field to *Location aging FIFO*.</span></span>
    - <span data-ttu-id="44900-145">如果您要设置 LIFO 方案，请将 **策略** 字段的值更改为 *位置帐龄 LIFO*。</span><span class="sxs-lookup"><span data-stu-id="44900-145">If you're setting up a LIFO scenario, change the value of the **Strategy** field to *Location aging LIFO*.</span></span>

1. <span data-ttu-id="44900-146">在 **位置指令操作** 快速选项卡上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="44900-146">On the **Location directive actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="44900-147">在查询对话框的 **范围** 选项卡上，选择 **添加** 添加一行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="44900-147">In the query dialog box, on the **Range** tab, select **Add** to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="44900-148">**表：** *位置*</span><span class="sxs-lookup"><span data-stu-id="44900-148">**Table:** *Locations*</span></span>
    - <span data-ttu-id="44900-149">**派生表**：*货位*</span><span class="sxs-lookup"><span data-stu-id="44900-149">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="44900-150">**字段：** *区域 ID*</span><span class="sxs-lookup"><span data-stu-id="44900-150">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="44900-151">**条件**：*场地*</span><span class="sxs-lookup"><span data-stu-id="44900-151">**Criteria:** *Floor*</span></span>

1. <span data-ttu-id="44900-152">选择 **确定** 应用设置并关闭查询对话框。</span><span class="sxs-lookup"><span data-stu-id="44900-152">Select **OK** to apply your settings and close the query dialog box.</span></span>
1. <span data-ttu-id="44900-153">选择 **保存** 保存对位置指令的更改。</span><span class="sxs-lookup"><span data-stu-id="44900-153">Select **Save** to save your changes to the location directive.</span></span>
1. <span data-ttu-id="44900-154">在移动设备上或 PC 上的 *Dynamics 365 for Finance and Operations - 仓储* 应用中，按照以下步骤从仓库位置删除现有库存以支持方案：</span><span class="sxs-lookup"><span data-stu-id="44900-154">On a mobile device or in the *Dynamics 365 for Finance and Operations - Warehousing* app on your PC, follow these steps to remove existing inventory from the warehouse location to support the scenarios:</span></span>

    1. <span data-ttu-id="44900-155">使用适当的用户 ID 和密码登录到仓库 *63*。</span><span class="sxs-lookup"><span data-stu-id="44900-155">Sign in to warehouse *63* by using the appropriate user ID and password.</span></span>
    1. <span data-ttu-id="44900-156">在主菜单上，选择 **质量**。</span><span class="sxs-lookup"><span data-stu-id="44900-156">On the main menu, select **Quality**.</span></span>
    1. <span data-ttu-id="44900-157">在 **质量管理** 菜单上，选择 **报废**。</span><span class="sxs-lookup"><span data-stu-id="44900-157">On the **Quality management** menu, select **Scrap**.</span></span>
    1. <span data-ttu-id="44900-158">在 **报废** 页面上，选择 **位置/牌照** 字段，然后输入 *63\_1*。</span><span class="sxs-lookup"><span data-stu-id="44900-158">On the **Scrap** page, select the **LOC/LP** field, and then enter *63\_1*.</span></span>
    1. <span data-ttu-id="44900-159">选择 **Enter** 或 **确定**。</span><span class="sxs-lookup"><span data-stu-id="44900-159">Select **Enter** or **OK**.</span></span>
    1. <span data-ttu-id="44900-160">选择 **Enter** 或 **确定** 确认要 **调出** 的 **报废** 详细信息。</span><span class="sxs-lookup"><span data-stu-id="44900-160">Confirm the **Scrap** details for **Adjustment out** by selecting **Enter** or **OK**.</span></span>

    <span data-ttu-id="44900-161">调整完牌照库存后，您将收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="44900-161">When the license plate inventory is adjusted out, you receive a "Work Completed" message.</span></span>

    <span data-ttu-id="44900-162">在演示数据中，这些步骤将库存保留在两个位置。</span><span class="sxs-lookup"><span data-stu-id="44900-162">These steps leave inventory in two locations in the demo data.</span></span> <span data-ttu-id="44900-163">每个位置有不同的帐龄日期。</span><span class="sxs-lookup"><span data-stu-id="44900-163">Each location has a different aging date.</span></span> <span data-ttu-id="44900-164">位置 *FL-001* 的帐龄日期为 2017 年 4 月 15 日，位置 *FL-002* 的帐龄日期为 2017 年 1 月 29 日。</span><span class="sxs-lookup"><span data-stu-id="44900-164">Location *FL-001* has an aging date of April 15, 2017, and location *FL-002* has an aging date of January 29, 2017.</span></span> <span data-ttu-id="44900-165">两个位置均包含物料 *A0001*。</span><span class="sxs-lookup"><span data-stu-id="44900-165">Both locations contain item *A0001*.</span></span>

    <span data-ttu-id="44900-166">要查看此数据，请转到 **库存管理 \> 查询和报表 \> 现有量列表**，然后筛选仓库 *63* 和物料 *A0001*。</span><span class="sxs-lookup"><span data-stu-id="44900-166">To view this data, go to **Inventory management \> Inquiries and reports \> On-hand list**, and then filter on warehouse *63* and item *A0001*.</span></span> <span data-ttu-id="44900-167">在 **位置** 字段设置为 *FL-001* 或 *FL-002* 的行中，选择 **实际库存** 值为正值的行，然后在“操作窗格”上，选择 **事务**。</span><span class="sxs-lookup"><span data-stu-id="44900-167">In the rows where the **Location** field is set to *FL-001* or *FL-002*, select a line that has a positive **Physical inventory** value, and then, on the Action Pane, select **Transactions**.</span></span> <span data-ttu-id="44900-168">**实际日期** 字段将显示与前面提到的帐龄日期之一对应的日期。</span><span class="sxs-lookup"><span data-stu-id="44900-168">The **Physical date** field will show a date that corresponds to one of the previously mentioned aging dates.</span></span>

### <a name="scenario-1-set-up-and-use-fifo-location-aging"></a><a name="fifo-demo"></a><span data-ttu-id="44900-169">方案 1：设置和使用 FIFO 位置帐龄</span><span class="sxs-lookup"><span data-stu-id="44900-169">Scenario 1: Set up and use FIFO location aging</span></span>

<span data-ttu-id="44900-170">FIFO 策略查找包含最早帐龄日期的位置，然后根据该帐龄日期分配领料。</span><span class="sxs-lookup"><span data-stu-id="44900-170">The FIFO strategy finds the location that contains the oldest aging date, and it allocates picking based on that aging date.</span></span>

1. <span data-ttu-id="44900-171">如果您还未进行此设置，请准备此方案所需的[示例数据](#demo-set-up)。</span><span class="sxs-lookup"><span data-stu-id="44900-171">If you haven't already done so, [prepare the sample data](#demo-set-up) that is required for this scenario.</span></span>
1. <span data-ttu-id="44900-172">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="44900-172">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="44900-173">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="44900-173">Select **New**.</span></span>
1. <span data-ttu-id="44900-174">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="44900-174">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="44900-175">在 **客户** 快速选项卡上，将 **客户帐户** 字段设置为 *US-001*。</span><span class="sxs-lookup"><span data-stu-id="44900-175">On the **Customer** FastTab, set the **Customer account** field to *US-001*.</span></span>
    - <span data-ttu-id="44900-176">在 **常规** 快速选项卡上，将 **仓库** 字段设置为 *63*。</span><span class="sxs-lookup"><span data-stu-id="44900-176">On the **General** FastTab, set the **Warehouse** field to *63*.</span></span>

1. <span data-ttu-id="44900-177">选择 **确定** 创建销售订单，然后关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="44900-177">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="44900-178">将打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="44900-178">The new sales order is opened.</span></span> <span data-ttu-id="44900-179">它将在 **销售订单行** 快速选项卡上的网格中包含一个新的空行。</span><span class="sxs-lookup"><span data-stu-id="44900-179">It includes a new, empty row in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="44900-180">对于此订单行，将 **物料编号** 字段设置为 *A0001*，将 **数量** 字段设置为 *1*。</span><span class="sxs-lookup"><span data-stu-id="44900-180">For this order line, set the **Item number** field to *A0001* and the **Quantity** field to *1*.</span></span>
1. <span data-ttu-id="44900-181">在网格上方的 **库存** 菜单中，选择 **预留**。</span><span class="sxs-lookup"><span data-stu-id="44900-181">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="44900-182">在 **预留** 页上，选择 **预留批次** 在选定仓库的库存中预留此物料的订购数量。</span><span class="sxs-lookup"><span data-stu-id="44900-182">On the **Reservation** page, select **Reserve lot** to reserve the ordered quantity of this item from inventory at the selected warehouse.</span></span>
1. <span data-ttu-id="44900-183">关闭 **预留** 页面。</span><span class="sxs-lookup"><span data-stu-id="44900-183">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="44900-184">在 **销售订单** 页面上的“操作窗格”上，在 **仓库** 选项卡上的 **操作** 组中，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="44900-184">On the **Sales order** page, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span> <span data-ttu-id="44900-185">您将收到信息性消息。</span><span class="sxs-lookup"><span data-stu-id="44900-185">You receive informational messages.</span></span> <span data-ttu-id="44900-186">系统将创建一个装运，将其添加到新负荷，然后创建所需工作。</span><span class="sxs-lookup"><span data-stu-id="44900-186">The system creates a shipment, adds it to a new load, and creates the required work.</span></span>
1. <span data-ttu-id="44900-187">在 **销售订单行** 快速选项卡上，在 **仓库** 菜单上，选择 **工作详细信息** 打开为此销售订单创建的工作。</span><span class="sxs-lookup"><span data-stu-id="44900-187">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Work details** to open the work that was created for this sales order.</span></span> <span data-ttu-id="44900-188">请注意，**工作类型** 值为 *领料* 的行将显示 **位置** 值 *FL-002*。</span><span class="sxs-lookup"><span data-stu-id="44900-188">Notice that the line where the **Work type** value is *Pick* shows a **Location** value of *FL-002*.</span></span> <span data-ttu-id="44900-189">此位置包含具有最早帐龄日期 (FIFO) 的牌照。</span><span class="sxs-lookup"><span data-stu-id="44900-189">This location contains the license plate that has the oldest aging date (FIFO).</span></span>
1. <span data-ttu-id="44900-190">选择 **仓库 \> 装运详细信息**。</span><span class="sxs-lookup"><span data-stu-id="44900-190">Select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="44900-191">在\**_常规_* 快速选项卡上，记下波次 ID，以便在方案 2 中使用。</span><span class="sxs-lookup"><span data-stu-id="44900-191">On the \**_General_* FastTab, make a note of the wave ID, so that you can use it in scenario 2.</span></span>

### <a name="scenario-2-set-up-and-use-lifo-location-aging"></a><span data-ttu-id="44900-192">方案 2：设置和使用 LIFO 位置帐龄</span><span class="sxs-lookup"><span data-stu-id="44900-192">Scenario 2: Set up and use LIFO location aging</span></span>

<span data-ttu-id="44900-193">LIFO 策略查找包含最新帐龄日期的位置，然后根据该帐龄日期分配领料。</span><span class="sxs-lookup"><span data-stu-id="44900-193">The LIFO strategy finds the location that contains the newest aging date, and it allocates picking based on that aging date.</span></span> <span data-ttu-id="44900-194">在方案 2 中，您将编辑方案 1 (FIFO) 的设置，并重用在该方案期间创建的销售订单和波次。</span><span class="sxs-lookup"><span data-stu-id="44900-194">In scenario 2, you will edit the setup for scenario 1 (FIFO), and reuse the sales order and wave that were created during that scenario.</span></span>

1. <span data-ttu-id="44900-195">在开始此方案之前，请按照[上一节](#fifo-demo)中所述设置并完成整个 FIFO 方案。</span><span class="sxs-lookup"><span data-stu-id="44900-195">Before you start this scenario, set up and complete the full FIFO scenario as described in the [previous section](#fifo-demo).</span></span> <span data-ttu-id="44900-196">在此方案中，您将重用波次以及为该方案创建的大多数设置。</span><span class="sxs-lookup"><span data-stu-id="44900-196">In this scenario, you will reuse the wave and most of the setup that were created for that scenario.</span></span>
1. <span data-ttu-id="44900-197">编辑 **63 领料集装化** 位置指令，使其使用 *位置帐龄 LIFO* 策略，如[设置方案](#demo-set-up)过程的第一部分所述。</span><span class="sxs-lookup"><span data-stu-id="44900-197">Edit the **63 Pick containerization** location directive so that it uses the *Location aging LIFO* strategy, as described in the first part of the [Set up the scenarios](#demo-set-up) procedure.</span></span>

    <span data-ttu-id="44900-198">接下来，您将修改在方案 1 中为销售订单创建的波次，使其使用 *位置帐龄 LIFO* 策略。</span><span class="sxs-lookup"><span data-stu-id="44900-198">Next, you will modify the wave that was created for the sales order in scenario 1, so that is uses the *Location aging LIFO* strategy.</span></span>

1. <span data-ttu-id="44900-199">转到 **仓库管理 \> 出站波次 \> 装运波次 \> 所有波次**。</span><span class="sxs-lookup"><span data-stu-id="44900-199">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="44900-200">选择并打开包含您为 FIFO 方案创建的订单的波次。</span><span class="sxs-lookup"><span data-stu-id="44900-200">Select and open the wave that contains the order that you created for the FIFO scenario.</span></span>
1. <span data-ttu-id="44900-201">在“操作窗格”上的 **工作** 选项卡上，选择 **取消** 取消为 FIFO 方案创建的工作。</span><span class="sxs-lookup"><span data-stu-id="44900-201">On the Action Pane, on the **Work** tab, select **Cancel** to cancel the work that you created for the FIFO scenario.</span></span>
1. <span data-ttu-id="44900-202">在“操作窗格”的 **波次** 选项卡的 **波次** 组中，选择 **处理**。</span><span class="sxs-lookup"><span data-stu-id="44900-202">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Process**.</span></span>
1. <span data-ttu-id="44900-203">处理完成后，在“操作窗格”上的 **波次** 选项卡上，在 **相关信息** 组中，选择 **工作** 打开为此波次创建的工作。</span><span class="sxs-lookup"><span data-stu-id="44900-203">When the processing is completed, on the Action Pane, on the **Wave** tab, in the **Related information** group, select **Work** to open the work that was created for this wave.</span></span>
1. <span data-ttu-id="44900-204">在 **工作** 页面上的 **概览** 选项卡上，应该有两行。</span><span class="sxs-lookup"><span data-stu-id="44900-204">On the **Work** page, on the **Overview** tab, there should be two lines.</span></span> <span data-ttu-id="44900-205">选择 **工作状态** 字段设置为 *打开* 的行。</span><span class="sxs-lookup"><span data-stu-id="44900-205">Select the line where the **Work status** field is set to *Open*.</span></span>
1. <span data-ttu-id="44900-206">请注意，**工作类型** 值为 *领料* 的行将显示 **位置** 值 *FL-001*。</span><span class="sxs-lookup"><span data-stu-id="44900-206">Notice that the line where the **Work type** value is *Pick* shows a **Location** value of *FL-001*.</span></span> <span data-ttu-id="44900-207">此位置包含具有最新帐龄日期 (LIFO) 的牌照。</span><span class="sxs-lookup"><span data-stu-id="44900-207">This location contains the license plate that has the newest aging date (LIFO).</span></span>

<span data-ttu-id="44900-208">在这些方案中，您已经看到了位置帐龄策略如何根据所选策略，将工作定向到具有最早库存或最新库存的库存位置。</span><span class="sxs-lookup"><span data-stu-id="44900-208">In these scenarios, you've seen how the location aging strategy directs work to the inventory location that has either the oldest inventory or the newest inventory, depending on the selected strategy.</span></span>

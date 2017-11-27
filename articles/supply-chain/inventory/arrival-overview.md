---
title: "到达概览"
description: "本主题提供有关“到达概览”功能的信息。 “到达概览”页是此功能的一部分，提供预期作为到货物料到达的所有物料的概览。"
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSArrivalOverview, WMSArrivalOverviewProfile, WMSJournalTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9c174dc7bf61ffab0d20c7685a29007e0b6e2e7e
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="arrival-overview"></a><span data-ttu-id="e8ea8-104">到达概览</span><span class="sxs-lookup"><span data-stu-id="e8ea8-104">Arrival overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e8ea8-105">本主题提供有关“到达概览”功能的信息。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-105">This topic provides information about the Arrival overview feature.</span></span> <span data-ttu-id="e8ea8-106">“到达概览”页是此功能的一部分，提供预期作为到货物料到达的所有物料的概览。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-106">The Arrival overview page is part of this feature and provides an overview of all items that are expected to arrive as incoming items.</span></span>

<span data-ttu-id="e8ea8-107">**到达概览**页提供所有预期到货物料的概览。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-107">The **Arrival overview** page provides an overview of all expected incoming items.</span></span> <span data-ttu-id="e8ea8-108">它还显示可根据概览初始化的到达。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-108">It also shows arrivals that can be initialized based on the overview.</span></span> <span data-ttu-id="e8ea8-109">本主题重点介绍接收过程。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-109">This topic focuses on the receiving process.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="e8ea8-110">业务方案</span><span class="sxs-lookup"><span data-stu-id="e8ea8-110">Business scenario</span></span>
<span data-ttu-id="e8ea8-111">在入站流程中考虑以下方案。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-111">Consider the following scenario in the inbound processes.</span></span>

<span data-ttu-id="e8ea8-112">[![业务方案](./media/arrival-overview-scenario.png)](./media/arrival-overview-scenario.png)</span><span class="sxs-lookup"><span data-stu-id="e8ea8-112">[![Business scenario](./media/arrival-overview-scenario.png)](./media/arrival-overview-scenario.png)</span></span>

<span data-ttu-id="e8ea8-113">Sammy，一名验收员，希望了解预期当天将收到的物料。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-113">Sammy, a receiving clerk, wants to know what is expected to be received on the current day.</span></span> <span data-ttu-id="e8ea8-114">在**到达概览**页，Sammy 可以获得当前任务的概览和数量、体积、重量、不同订单类型的粗略估计，等等。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-114">On the **Arrival overview** page, Sammy can get an overview of the current tasks, and a rough estimate of quantities, volume, weight, different order types, and so on.</span></span> <span data-ttu-id="e8ea8-115">然后，交货到达进货台中的一个，Sammy 接收交货列表。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-115">Later, a delivery arrives at one of the inbound docks, and Sammy receives a list of the delivery.</span></span> <span data-ttu-id="e8ea8-116">在**到达概览**页，Sammy 可以执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="e8ea8-116">On the **Arrival overview** page, Sammy can perform the following tasks:</span></span>

-   <span data-ttu-id="e8ea8-117">标识匹配的收货订单，以及将收货登记为**在进行中**。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-117">Identify the matching receipt order, and register the receipt as **In progress**.</span></span> <span data-ttu-id="e8ea8-118">登记所需的行自动生成，收货可以被监控，即使交易尚未过帐为**已登记**。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-118">The lines that are required for a registration are automatically generated, and the receipt can be monitored, even though the transactions haven't yet been posted as **Registered**.</span></span>
-   <span data-ttu-id="e8ea8-119">访问相应的到达日记帐参考（即**物料到达**日记帐或**生产输入**日记帐），并且还标识准备好物料收货更新的日记帐。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-119">Access the appropriate arrival journal reference (that is, the **Item arrival** journal or the **Production input** journal), and identify journals that are ready for a product receipt update.</span></span>

## <a name="arrival-overview-page"></a><span data-ttu-id="e8ea8-120">到货概览页</span><span class="sxs-lookup"><span data-stu-id="e8ea8-120">Arrival overview page</span></span>
<span data-ttu-id="e8ea8-121">若要打开**到达概览**页，单击**库存管理**&gt;**入站订单**&gt;**到达概览**。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-121">To open the **Arrival overview** page, click **Inventory management** &gt; **Inbound orders** &gt; **Arrival overview**.</span></span> <span data-ttu-id="e8ea8-122">可以查看预期将收到的订单的列表。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-122">You can view a list of orders that are expected to be received.</span></span> <span data-ttu-id="e8ea8-123">概览划分为标题和行。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-123">The overview is divided into a header and lines.</span></span> <span data-ttu-id="e8ea8-124">标题信息按订单类型、预期收货日期和交货目的地分组。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-124">The header information is grouped by the order type, expected receipt date, and delivery destination.</span></span> <span data-ttu-id="e8ea8-125">在为到达选择标题行时，与收货参考相关的所有明细行将为页面行详细信息部门的到达选择。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-125">When a header line is selected for arrival, all the detail lines that are related to the receipt reference are selected for arrival in the line details part of the page.</span></span> <span data-ttu-id="e8ea8-126">在所有相关日记帐行过帐后，此信息不显示。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-126">When all related journal lines have been posted, this information isn't shown.</span></span>

### <a name="arrival-overview-profiles"></a><span data-ttu-id="e8ea8-127">到货概览配置文件</span><span class="sxs-lookup"><span data-stu-id="e8ea8-127">Arrival overview profiles</span></span>

<span data-ttu-id="e8ea8-128">**到达概览**页提供预期到达的物料的概览及预期到达的日期。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-128">The **Arrival overview** page provides an overview of items that are expected to arrive and the date when they are expected to arrive.</span></span> <span data-ttu-id="e8ea8-129">作为到达过程的一部分，可以使用多组个人设置。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-129">As part of the arrival process, multiple sets of personal settings can be used.</span></span> <span data-ttu-id="e8ea8-130">单个用户可以在**到达概览配置文件**页定义个人设置。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-130">Individual users can define their personal settings on the **Arrival overview profiles** page.</span></span>

### <a name="set-up-item-arrival"></a><span data-ttu-id="e8ea8-131">设置物料到达</span><span class="sxs-lookup"><span data-stu-id="e8ea8-131">Set up item arrival</span></span>

<span data-ttu-id="e8ea8-132">在我们的示例中，Sammy 想要在将用于接收站点 1 生产的成品的位置设置新计算机。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-132">In our example, Sammy wants to set up a new computer at a location that will be used to receive finished goods that come from production at Site 1.</span></span> <span data-ttu-id="e8ea8-133">在**到达概览配置文件**页，Sammy 创建名为**站点 1 生产**的新设置，并指定以下设置。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-133">On the **Arrival overview profiles** page, Sammy creates a new setup that is named **Site 1 production** and specifies the following settings.</span></span>

1.  <span data-ttu-id="e8ea8-134">在**到货选项**快速选项卡上，在**范围**字段组中，输入有关要包括在概览中的日间隔和仓库的信息。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-134">On the **Arrival options** FastTab, in the **Range** field group, enter information about a day interval and the warehouses to include in the overview.</span></span>
2.  <span data-ttu-id="e8ea8-135">在**到货选项**快速选项卡上，在**日记帐**字段组中，输入接收仓库、库位和日记帐名称（物料到达/生产输入）。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-135">On the **Arrival options** FastTab, in the **Journal** field group, enter a receiving warehouse, a location, and a journal name (item arrival/production input).</span></span>
3.  <span data-ttu-id="e8ea8-136">在**到货查询详细信息**快速选项卡上，在**站点**字段组中，在**限制到站点**字段中，输入在概览区域限制视图的站点。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-136">On the **Arrival query details** FastTab, in the **Site** field group, in the **Restrict to site** field, enter a site to limit the view in the overview area.</span></span>
4.  <span data-ttu-id="e8ea8-137">在**到货查询详细信息**快速选项卡上，在**显示的交易记录类型**字段组中，将**生产订单**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-137">On the **Arrival query details** FastTab, in the **Transaction types shown** field group, set the **Production orders** option to **Yes**.</span></span>
5.  <span data-ttu-id="e8ea8-138">如果视图应在启动时自动更新，在**到货查询详细信息**快速选项卡上，在**杂项**组中，将**启动时更新**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-138">On the **Arrival query details** FastTab, in the **Miscellaneous** group, set the **Update on startup** option to **Yes** if the view should be automatically updated at startup.</span></span> <span data-ttu-id="e8ea8-139">如果应在范围值更改时自动更新视图，将**范围更改时更新**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-139">Set the **Update on range change** option to **Yes** if the view should be automatically updated when range values are changed.</span></span>

<span data-ttu-id="e8ea8-140">对于此示例，**到达概览**页的**到货选项**快速选项卡上的**到货概览配置文件名称**字段设置为**站点 1 生产**。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-140">For this example, the **Arrival overview profile name** field on the **Arrival options** FastTab of the **Arrival overview** page is set to **Site 1 production**.</span></span>

### <a name="prerequisites-for-arrival-journals"></a><span data-ttu-id="e8ea8-141">到达日记帐的先决条件</span><span class="sxs-lookup"><span data-stu-id="e8ea8-141">Prerequisites for arrival journals</span></span>

<span data-ttu-id="e8ea8-142">若要从**到达概览**页自动创建到达日记帐，您必须在**到货选项**快速选项卡上的**日记帐**字段组中定义相应的信息。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-142">To automatically create arrival journals from the **Arrival overview** page, you must define appropriate information in the **Journal** field group on the **Arrival options** FastTab.</span></span>

-   <span data-ttu-id="e8ea8-143">必须指定创建日记帐的日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-143">You must specify a journal name to create a journal.</span></span>

<span data-ttu-id="e8ea8-144">[![指定日记帐名称](./media/arrival-overview-journal.png)](./media/arrival-overview-journal.png)</span><span class="sxs-lookup"><span data-stu-id="e8ea8-144">[![Specifying a journal name](./media/arrival-overview-journal.png)](./media/arrival-overview-journal.png)</span></span>

-   <span data-ttu-id="e8ea8-145">如果您在**仓库**和**库位**字段中指定值，那些值在日记帐行上应用。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-145">If you specify values in the **Warehouse** and **Location** fields, those values are applied on the journal lines.</span></span> <span data-ttu-id="e8ea8-146">如果未指定值，系统将使用来自在库存交易记录中所指定维度的值。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-146">If you don't specify values, the system uses the values from the dimension that is specified on the inventory transactions.</span></span>

#### <a name="items-that-are-received-from-one-expected-receipt-order"></a><span data-ttu-id="e8ea8-147">从一个预期收货订单接收的物料</span><span class="sxs-lookup"><span data-stu-id="e8ea8-147">Items that are received from one expected receipt order</span></span>

<span data-ttu-id="e8ea8-148">在**收货**快速选项卡上，Sammy 选择一行，然后单击**开始到达**。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-148">On the **Receipts** FastTab, Sammy selects a line and then clicks **Start arrival**.</span></span> <span data-ttu-id="e8ea8-149">在指定范围中，并且具有要登记数量的所有相关行将被自动选择。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-149">All related lines that are in the specified range and that have a quantity to register are automatically selected.</span></span> <span data-ttu-id="e8ea8-150">物料到达日记帐生成，其预期收货订单和日记帐之间匹配。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-150">An item arrival journal is generated that has a match between the expected receipt order and the journal.</span></span> <span data-ttu-id="e8ea8-151">数量在创建的所有行中自动初始化。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-151">The quantity is automatically initialized on all lines that are created.</span></span>

#### <a name="items-that-are-received-from-more-than-one-expected-receipt-order"></a><span data-ttu-id="e8ea8-152">从多个预期收货订单接收的物料</span><span class="sxs-lookup"><span data-stu-id="e8ea8-152">Items that are received from more than one expected receipt order</span></span>

<span data-ttu-id="e8ea8-153">在**收货**快速选项卡上，Sammy 选择多个行，然后单击**开始到达**。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-153">On the **Receipts** FastTab, Sammy selects multiple lines and then clicks **Start arrival**.</span></span> <span data-ttu-id="e8ea8-154">物料到达日记帐生成，其所有预期收货订单和日记帐之间匹配。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-154">An item arrival journal is generated that has a match between all the expected receipt orders and the journal.</span></span> <span data-ttu-id="e8ea8-155">所有行在一个物料到达日记帐标头中创建，并且数量将自动初始化。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-155">All lines are created on one item arrival journal header, and the quantity is automatically initialized.</span></span>

### <a name="receive-items-from-one-or-more-expected-receipt-orders"></a><span data-ttu-id="e8ea8-156">从一个或多个预期收货订单接收物料</span><span class="sxs-lookup"><span data-stu-id="e8ea8-156">Receive items from one or more expected receipt orders</span></span>

#### <a name="view-information"></a><span data-ttu-id="e8ea8-157">查看信息</span><span class="sxs-lookup"><span data-stu-id="e8ea8-157">View information</span></span>

<span data-ttu-id="e8ea8-158">为获取日期间隔内的预期收货概览，Sammy 在**到达概览**页的**到货选项**快速选项卡的字段中输入以下信息，然后单击**更新**更新视图：</span><span class="sxs-lookup"><span data-stu-id="e8ea8-158">To get an overview of expected receipts in a date interval, Sammy enters the following information in the fields on the **Arrival options** FastTab on the **Arrival overview** page and then clicks **Update** to update the view:</span></span>

-   <span data-ttu-id="e8ea8-159">到货概览配置文件名称：**查询**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-159">Arrival overview profile name: **Inquiry**</span></span>
-   <span data-ttu-id="e8ea8-160">显示行：**全部**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-160">Show lines: **All**</span></span>
-   <span data-ttu-id="e8ea8-161">后推天数：（空白）</span><span class="sxs-lookup"><span data-stu-id="e8ea8-161">Days back: (Blank)</span></span>
-   <span data-ttu-id="e8ea8-162">前推天数：**0**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-162">Days forward: **0**</span></span>
-   <span data-ttu-id="e8ea8-163">仓库：**GW, MW**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-163">Warehouses: **GW, MW**</span></span>

<span data-ttu-id="e8ea8-164">Sammy 可以查看以下信息：</span><span class="sxs-lookup"><span data-stu-id="e8ea8-164">Sammy can view the following information:</span></span>

-   <span data-ttu-id="e8ea8-165">系统日期的所有相关收货订单，从其（**InventTrans.StatusDate** 间隔）后推的无限天数，仓库 MW 和 MW 的收货，不论状态如何。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-165">All related receipt orders for the system date and an infinite number of days back from it (the **InventTrans.StatusDate** interval), and receipts to warehouses GW and MW, regardless of status.</span></span>
-   <span data-ttu-id="e8ea8-166">多个订单的详细行信息。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-166">Detailed line information for more than one order.</span></span> <span data-ttu-id="e8ea8-167">Sammy 可以在概览中选择多个标题行，然后单击**示所有所选行**来查看所有选定订单的对应行的详细信息。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-167">Sammy can select multiple header lines in the overview and then click **Show all selected** to view all the corresponding line detail information for all selected orders.</span></span>
-   <span data-ttu-id="e8ea8-168">有关特定采购订单的信息。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-168">Information about a specific purchase order.</span></span> <span data-ttu-id="e8ea8-169">若要只显示与概览中的具体参考编号相关的信息，Sammy 可以在**帐号**字段中输入一个帐号，在**参考编号**字段中输入一个订单编号。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-169">To show only information that is related to a specific reference number in the overview, Sammy can enter an account number in the **Account number** field and an order number in the **Reference number** field.</span></span>
-   <span data-ttu-id="e8ea8-170">已为其创建物料到达日记帐但尚未过帐的所有订单行的到期登记任务的概览。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-170">An overview of the registration tasks that are due for all the order lines that an item arrival journal has been created for but hasn't yet been posted.</span></span> <span data-ttu-id="e8ea8-171">若要查看此信息，Sammy 可以在**显示行**字段选择**在进行中**。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-171">To view this information, Sammy can select **In progress** in the **Show lines** field.</span></span>

### <a name="update-journals"></a><span data-ttu-id="e8ea8-172">更新日记帐</span><span class="sxs-lookup"><span data-stu-id="e8ea8-172">Update journals</span></span>

<span data-ttu-id="e8ea8-173">若要登记到期要处理的一个或多个订单行，Sammy 可以在概览网格或在行网格中选择该行，然后单击**日记帐**&gt;**显示收货的到达**。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-173">To register one or more order lines that are due to be processed, Sammy can select the lines in the overview grid or in the line grid, and then click **Journals** &gt; **Show arrivals from receipts**.</span></span> <span data-ttu-id="e8ea8-174">显示与行匹配的物料到达标题。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-174">The item arrival headers that match the lines are shown.</span></span> <span data-ttu-id="e8ea8-175">若要更新登记的物料的采购订单产品收货，Sammy 可以访问准备好更新的物料到达日记帐标题。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-175">To update the purchase order product receipt for the registered items, Sammy can access the item arrival journal headers that are ready for update.</span></span> <span data-ttu-id="e8ea8-176">若要访问这些物料到达日记帐标题，单击**日记帐**&gt;**物料收货就绪日记帐**。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-176">To access these item arrival journal headers, he clicks **Journals** &gt; **Product receipt ready journals**.</span></span> <span data-ttu-id="e8ea8-177">显示准备好在指定仓库范围内进行物料收货更新的所有标题行。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-177">All the header lines that are ready for product receipt update in the specified warehouse range are shown.</span></span> <span data-ttu-id="e8ea8-178">（显示的标题行与日间隔无关）。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-178">(The header lines that are shown aren't related to the day interval).</span></span>

### <a name="start-an-arrival-registration"></a><span data-ttu-id="e8ea8-179">开始到达登记</span><span class="sxs-lookup"><span data-stu-id="e8ea8-179">Start an arrival registration</span></span>

<span data-ttu-id="e8ea8-180">通过在**到达概览**页选择多个行，Sammy 可以开始多个收货参考的到达。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-180">By selecting multiple lines on the **Arrival overview** page, Sammy can start an arrival of more than one receipt reference.</span></span> <span data-ttu-id="e8ea8-181">当他从收货概览选择某一行，将选择相应的行的详细信息。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-181">When he selects a line from the receipts overview, the corresponding line details are selected.</span></span> <span data-ttu-id="e8ea8-182">如果存在要登记的数量，则**开始到达**按钮可用。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-182">If a quantity for registration exists, the **Start arrival** button is available.</span></span> <span data-ttu-id="e8ea8-183">Sammy 可以使用以下两种方法来开始到达登记：</span><span class="sxs-lookup"><span data-stu-id="e8ea8-183">Sammy can use two methods to start the arrival registration:</span></span>

-   <span data-ttu-id="e8ea8-184">若要筛选页，以便页面只显示符合特定条件的记录，在**供应商参考**字段中，扫描供应商的参考编号，如交货通知的条码。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-184">To filter the page so that it shows only records that meet specific criteria, in the **Vendor reference** field, scan a reference number from a vendor, such as the bar code for a delivery note.</span></span>
-   <span data-ttu-id="e8ea8-185">在**到达概览**页的概览部分或详细信息部分，手动选择或取消为到达登记进行的记录选择。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-185">In the overview part or the details part of the **Arrival overview** page, manually select or cancel the selection of records for arrival registration.</span></span> <span data-ttu-id="e8ea8-186">然后，在 Sammy 单击**开始到达**时，所选记录将在物料到达日记帐中自动创建。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-186">Then, when Sammy clicks **Start arrival**, the selected records are automatically created in an item arrival journal.</span></span> <span data-ttu-id="e8ea8-187">记录包括行信息，并分配所有唯一字段信息。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-187">The records include line information, and all unique field information is assigned.</span></span>

## <a name="update-arrival-information-and-process-a-product-receipt"></a><span data-ttu-id="e8ea8-188">更新到达信息并处理物料收货</span><span class="sxs-lookup"><span data-stu-id="e8ea8-188">Update arrival information and process a product receipt</span></span>
<span data-ttu-id="e8ea8-189">在登记所有货物后，仓库经理或采购经理可以使用要添加到实际成本的物料收货更新接收的物料。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-189">When all goods have been registered, the warehouse manager or purchasing manager can update the received items with a product receipt to add the physical cost.</span></span> <span data-ttu-id="e8ea8-190">若要更新到达信息并过帐物料收货，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-190">To update arrival information and post a product receipt, follow these steps.</span></span>

1.  <span data-ttu-id="e8ea8-191">单击**库存管理**&gt;**入站订单**&gt;**到达概览**。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-191">Click **Inventory management** &gt; **Inbound orders** &gt; **Arrival overview**.</span></span>
2.  <span data-ttu-id="e8ea8-192">在**到达概览**页，单击**日记帐**&gt;**物料收货就绪日记帐**显示准备好物料收货更新的日记帐的列表。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-192">On the **Arrival overview** page, click **Journals** &gt; **Product receipt ready journals** to show a list of the journals that are ready for product receipt update.</span></span>
3.  <span data-ttu-id="e8ea8-193">选择必须更新的日记帐，然后单击**功能**&gt;**物料收货**。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-193">Select the journals that must be updated, and then click **Functions** &gt; **Product receipt**.</span></span>
4.  <span data-ttu-id="e8ea8-194">在**过帐**页，输入物料收货编号（如果日记帐中尚未显示），然后单击**确定**处理物料收货。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-194">On the **Posting** page, enter the product receipt number, if it isn't already available on the journal, and then click **OK** to process the product receipt.</span></span>

## <a name="summary"></a><span data-ttu-id="e8ea8-195">汇总</span><span class="sxs-lookup"><span data-stu-id="e8ea8-195">Summary</span></span>
<span data-ttu-id="e8ea8-196">**到达概览**页可以帮助仓库经理和仓库工作人员获得必须在入站流程期间完成的预期工作的概览。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-196">The **Arrival overview** page can help the warehouse manager and warehouse workers achieve an overview of expected work that must be done as part of an inbound process.</span></span> <span data-ttu-id="e8ea8-197">此页还可能用于开始物料到达流程，帮助保证物料首次进入仓库即受到跟踪。</span><span class="sxs-lookup"><span data-stu-id="e8ea8-197">The page can also be used to start the item arrival process, to help guarantee that items are tracked at the first entry into the warehouse.</span></span>


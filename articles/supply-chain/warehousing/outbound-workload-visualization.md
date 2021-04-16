---
title: 出站工作负荷可视化
description: 本主题提供有关出库工作负荷可视化的信息。 此功能使仓库经理和主管可以创建自定义工作负荷图表，该图表可用于监视当前工作的进度和剩余工作量。 仓库经理可以根据需要创建多个视图并设置自动刷新。
author: Mirzaab
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-08-28
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: f1a405f5bbf8728876213e6c726ae41ebf809626
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810478"
---
# <a name="outbound-workload-visualization"></a><span data-ttu-id="43b1d-105">出站工作负荷可视化</span><span class="sxs-lookup"><span data-stu-id="43b1d-105">Outbound workload visualization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43b1d-106">可通过 **出库工作负荷可视化** 页面访问的高级设置功能使仓库经理和主管可以创建自定义工作负荷图表，该图表可用于监视当前工作的进度和剩余工作量。</span><span class="sxs-lookup"><span data-stu-id="43b1d-106">Advanced setup capabilities that are accessible from the **Outbound workload visualization** page let warehouse managers and supervisors create custom workload charts that can be used to monitor the progress of current work and the amount of it that remains.</span></span> <span data-ttu-id="43b1d-107">仓库经理可以根据需要创建多个视图并设置自动刷新。</span><span class="sxs-lookup"><span data-stu-id="43b1d-107">Warehouse managers can create multiple views and set up automatic refresh as they require.</span></span> <span data-ttu-id="43b1d-108">出库工作负荷可视化适合显示在仓库绩效页面上。</span><span class="sxs-lookup"><span data-stu-id="43b1d-108">Outbound workload visualizations are suitable for display on warehouse performance pages.</span></span>

<span data-ttu-id="43b1d-109">此功能可用于跟踪领料工作的进度。</span><span class="sxs-lookup"><span data-stu-id="43b1d-109">This functionality can be used to track the progress of picking work.</span></span> <span data-ttu-id="43b1d-110">该功能将与人工管理集成，如果设置了人工管理，出库工作负荷可视化可以显示所显示（筛选）的领料工作剩余小时数的计算结果。</span><span class="sxs-lookup"><span data-stu-id="43b1d-110">The feature is integrated with labor management, and if labor management is set up, outbound workload visualizations can show a calculation of the number of hours that remain for the picking work that is shown (filtered).</span></span>

## <a name="turn-on-the-outbound-workload-visualization-feature"></a><span data-ttu-id="43b1d-111">打开出库工作负荷可视化功能</span><span class="sxs-lookup"><span data-stu-id="43b1d-111">Turn on the Outbound workload visualization feature</span></span>

<span data-ttu-id="43b1d-112">此功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="43b1d-112">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="43b1d-113">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置以检查功能状态和打开功能。</span><span class="sxs-lookup"><span data-stu-id="43b1d-113">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="43b1d-114">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="43b1d-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="43b1d-115">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="43b1d-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="43b1d-116">\**功能名称：\*\*\*出库工作负荷可视化*</span><span class="sxs-lookup"><span data-stu-id="43b1d-116">**Feature name:** *Outbound workload visualization*</span></span>

## <a name="set-up-outbound-workload-visualizations"></a><span data-ttu-id="43b1d-117">设置出库工作负荷可视化</span><span class="sxs-lookup"><span data-stu-id="43b1d-117">Set up outbound workload visualizations</span></span>

<span data-ttu-id="43b1d-118">若要设置可视化，请创建筛选器（视图）的集合并设计每个筛选器，以使其显示不同类型的分析。</span><span class="sxs-lookup"><span data-stu-id="43b1d-118">To set up your visualizations, you create a collection of filters (views) and design each filter so that it shows a different type of analysis.</span></span> <span data-ttu-id="43b1d-119">您使用 **配置筛选器** 页面设计筛选器。</span><span class="sxs-lookup"><span data-stu-id="43b1d-119">You use the **Configure filters** page to design the filters.</span></span>

<span data-ttu-id="43b1d-120">若要设置出库工作负荷可视化，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="43b1d-120">To set up an outbound workload visualization, follow these steps.</span></span>

1. <span data-ttu-id="43b1d-121">转到 **仓库管理 \> 仓库监视报表 \> 出库工作负荷可视化**。</span><span class="sxs-lookup"><span data-stu-id="43b1d-121">Go to **Warehouse management \> Warehouse monitoring reports \> Outbound workload visualization**.</span></span>

    <span data-ttu-id="43b1d-122">将显示 **出库工作负荷可视化** 页面。</span><span class="sxs-lookup"><span data-stu-id="43b1d-122">The **Outbound workload visualization** page appears.</span></span> <span data-ttu-id="43b1d-123">创建某些筛选器后，此页面将显示您的可视化。</span><span class="sxs-lookup"><span data-stu-id="43b1d-123">After you create some filters, this page will show your visualization.</span></span> <span data-ttu-id="43b1d-124">您可以根据需要创建任意多的筛选器。</span><span class="sxs-lookup"><span data-stu-id="43b1d-124">You can create as many filters as you want.</span></span> <span data-ttu-id="43b1d-125">您创建的所有筛选器都保存在您的用户帐户下，以便以后使用。</span><span class="sxs-lookup"><span data-stu-id="43b1d-125">All the filters that you create are saved under your user account, so that you can use them later.</span></span> <span data-ttu-id="43b1d-126">换句话说，每个用户都将拥有自己创建的筛选器集。</span><span class="sxs-lookup"><span data-stu-id="43b1d-126">In other words, each user will have their own set of filters that they created.</span></span> <span data-ttu-id="43b1d-127">这些筛选器不会与其他用户共享。</span><span class="sxs-lookup"><span data-stu-id="43b1d-127">Those filters won't be shared with other users.</span></span>

1. <span data-ttu-id="43b1d-128">在 **出库工作负荷可视化** 页面上，在操作窗格的 **筛选器** 选项卡上，选择 **配置筛选器**。</span><span class="sxs-lookup"><span data-stu-id="43b1d-128">On the **Outbound workload visualization** page, on the Action Pane, on the **Filters** tab, select **Configure filters**.</span></span>
1. <span data-ttu-id="43b1d-129">在 **配置筛选器** 页面上的操作窗格上，选择 **新建** 以添加筛选器，然后为其设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="43b1d-129">On the **Configure filters** page, on the Action Pane, select **New** to add a filter, and then set the following fields for it:</span></span>

    - <span data-ttu-id="43b1d-130">**X 轴组表** – 选择包含应该用于对 X 轴值进行分组的字段的表。</span><span class="sxs-lookup"><span data-stu-id="43b1d-130">**X-axis group table** – Select the table that contains the field that should be used to group the X-axis values.</span></span>
    - <span data-ttu-id="43b1d-131">**X 轴组字段** – 从您在 **X 轴组表** 字段中选择的表的字段中，选择应该用于对 X 轴值进行分组的字段。</span><span class="sxs-lookup"><span data-stu-id="43b1d-131">**X-axis group field** – From among the fields of the table that you selected in the **X-axis group table** field, select the field that should be used to group the X-axis values.</span></span>
    - <span data-ttu-id="43b1d-132">**X 轴值表** – 选择包含应该用于进一步分析组的字段的表。</span><span class="sxs-lookup"><span data-stu-id="43b1d-132">**X-axis value table** – Select the table that contains the field that should be used to further analyze the groups.</span></span>
    - <span data-ttu-id="43b1d-133">**X 轴值字段** – 从您在 **X 轴值表** 字段中选择的表的字段中，选择提供应该对每个组分析的值的字段。</span><span class="sxs-lookup"><span data-stu-id="43b1d-133">**X-axis value field** – From among the fields of the table that you selected in the **X-axis value table** field, select the field that provides the values that should be analyzed for each group.</span></span>
    - <span data-ttu-id="43b1d-134">**自动刷新** – 选择是否应自动刷新可视化。</span><span class="sxs-lookup"><span data-stu-id="43b1d-134">**Auto-refresh** – Select whether the visualization should automatically be refreshed.</span></span>
    - <span data-ttu-id="43b1d-135">**刷新间隔（分钟）**– 输入自动刷新之间的分钟数。</span><span class="sxs-lookup"><span data-stu-id="43b1d-135">**Refresh interval (minutes)** – Enter the number of minutes between automatic refreshes.</span></span>
    - <span data-ttu-id="43b1d-136">**显示级别** – 选择图表是否应显示未结行或未结标题计数。</span><span class="sxs-lookup"><span data-stu-id="43b1d-136">**Display level** – Select whether the chart should show open lines or open header counts.</span></span>
    - <span data-ttu-id="43b1d-137">**领料类型** – 如果您将 **显示级别** 字段设置为 _未结行_，选择图表中未结工作行的计数应包括初始领料还是暂存领料，或者同时包括初始领料和暂存领料。</span><span class="sxs-lookup"><span data-stu-id="43b1d-137">**Picking type** – If you set the **Display level** field to _Open lines_, select whether the count of open work lines in the chart should include initial picks, staged picks, or both initial picks and staged picks.</span></span>
    - <span data-ttu-id="43b1d-138">**站点** – 选择要为其加载图表的站点。</span><span class="sxs-lookup"><span data-stu-id="43b1d-138">**Site** – Select the site to load the chart for.</span></span>
    - <span data-ttu-id="43b1d-139">**仓库** – 选择要为其加载图表的仓库。</span><span class="sxs-lookup"><span data-stu-id="43b1d-139">**Warehouse** – Select the warehouse to load the chart for.</span></span>
    - <span data-ttu-id="43b1d-140">**包括天数** – 输入过去应为其生成图表的天数。</span><span class="sxs-lookup"><span data-stu-id="43b1d-140">**Days to include** – Enter the number of days in the past that the chart should be generated for.</span></span>
    - <span data-ttu-id="43b1d-141">**工作订单类型** – 选择要筛选的出库工作订单类型。</span><span class="sxs-lookup"><span data-stu-id="43b1d-141">**Work order type** – Select the outbound work order types to filter on.</span></span>

    <span data-ttu-id="43b1d-142">![配置筛选器页面](media/work-viz-filters-1.png "配置筛选器页面")</span><span class="sxs-lookup"><span data-stu-id="43b1d-142">![Configure filters page](media/work-viz-filters-1.png "Configure filters page")</span></span>

1. <span data-ttu-id="43b1d-143">关闭 **配置筛选器** 页面以返回到 **出库工作负荷可视化** 页面。</span><span class="sxs-lookup"><span data-stu-id="43b1d-143">Close the **Configure filters** page to return to the **Outbound workload visualizations** page.</span></span>

    <span data-ttu-id="43b1d-144">现在，**出库工作负荷可视化** 页面将根据您的新筛选器设置显示数据。</span><span class="sxs-lookup"><span data-stu-id="43b1d-144">The **Outbound workload visualizations** page now shows data, based on your new filter settings.</span></span> <span data-ttu-id="43b1d-145">您的新筛选器现在可用，并在 **筛选** 字段中选择。</span><span class="sxs-lookup"><span data-stu-id="43b1d-145">Your new filter is now available and is selected in the **Filter** field.</span></span> <span data-ttu-id="43b1d-146">图表顶部提供以下字段：</span><span class="sxs-lookup"><span data-stu-id="43b1d-146">The following fields are available at the top of the chart:</span></span>

    - <span data-ttu-id="43b1d-147">**筛选器** – 该字段包括您到目前为止创建的所有筛选器。</span><span class="sxs-lookup"><span data-stu-id="43b1d-147">**Filter** – This field includes all the filters that you've created so far.</span></span> <span data-ttu-id="43b1d-148">选择一个筛选器以在图表中查看其数据。</span><span class="sxs-lookup"><span data-stu-id="43b1d-148">Select a filter to view its data in the chart.</span></span>
    - <span data-ttu-id="43b1d-149">**上次刷新** – 此字段显示上次更新图表中的信息的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="43b1d-149">**Last refreshed** – This field shows the date and time when the information in the chart was last updated.</span></span>
    - <span data-ttu-id="43b1d-150">**估计/实际时间** – 如果在系统中设置了人工标准，将此选项设置为 *是* 以在图表的每一列顶部显示累计的估计领料时间。</span><span class="sxs-lookup"><span data-stu-id="43b1d-150">**Estimated/actual time** – If labor standards are set up in your system, set this option to *Yes* to show accumulated estimated picking times at the top of each column in the chart.</span></span> <span data-ttu-id="43b1d-151">如果您不使用人工标准，则此选项不可用。</span><span class="sxs-lookup"><span data-stu-id="43b1d-151">If you aren't using labor standards, this option is unavailable.</span></span>

    <span data-ttu-id="43b1d-152">![可视化示例](media/work-viz-chart.png "可视化示例")</span><span class="sxs-lookup"><span data-stu-id="43b1d-152">![Example visualization](media/work-viz-chart.png "Example visualization")</span></span>

1. <span data-ttu-id="43b1d-153">选择图表中的任何栏以查看关联的工作行详细信息。</span><span class="sxs-lookup"><span data-stu-id="43b1d-153">Select any bar in the chart to view the associated work line details.</span></span>

    <span data-ttu-id="43b1d-154">![工作行详细信息](media/work-viz-work-details.png "工作行详细信息")</span><span class="sxs-lookup"><span data-stu-id="43b1d-154">![Work line details](media/work-viz-work-details.png "Work line details")</span></span>

## <a name="example-outbound-workload-visualization-for-zones"></a><span data-ttu-id="43b1d-155">示例：区域的出库工作负荷可视化</span><span class="sxs-lookup"><span data-stu-id="43b1d-155">Example: Outbound workload visualization for zones</span></span>

<span data-ttu-id="43b1d-156">对于此示例，您想要设置一个可视化，用于显示每个区域的工作行以及每个工作行的状态（_未结_、_已结_ 或 _已取消_）。</span><span class="sxs-lookup"><span data-stu-id="43b1d-156">For this example, you want to set up a visualization that shows work lines for each zone, and the status of each work line (_Open_, _Closed_, or _Canceled_).</span></span> <span data-ttu-id="43b1d-157">在这种情况下，您可以设置具有以下设置的筛选器：</span><span class="sxs-lookup"><span data-stu-id="43b1d-157">In this case, you can set up a filter that has the following settings:</span></span>

- <span data-ttu-id="43b1d-158">**筛选器名称** – 输入此筛选器的名称（例如 _区域与工作状态_）。</span><span class="sxs-lookup"><span data-stu-id="43b1d-158">**Filter name** – Enter a name for this filter (such as _Zone vs. work status_).</span></span>
- <span data-ttu-id="43b1d-159">**描述** – 输入此筛选器的简短描述（例如 _区域与工作状态_）。</span><span class="sxs-lookup"><span data-stu-id="43b1d-159">**Description** – Enter a short description for this filter (such as _Zone vs. work status_).</span></span>
- <span data-ttu-id="43b1d-160">**X 轴组表** – 选择 _库位_。</span><span class="sxs-lookup"><span data-stu-id="43b1d-160">**X-axis group table** – Select _Locations._</span></span>
- <span data-ttu-id="43b1d-161">**X 轴组** – 选择 _区域 ID_。</span><span class="sxs-lookup"><span data-stu-id="43b1d-161">**X-axis group** – Select _Zone ID_.</span></span>
- <span data-ttu-id="43b1d-162">**X 轴值表** – 选择 _工作_，因为您要按区域查看工作。</span><span class="sxs-lookup"><span data-stu-id="43b1d-162">**X-axis value table** – Select _Work_, because you want to view work per zone.</span></span>
- <span data-ttu-id="43b1d-163">**X 轴值字段** – 选择 _工作状态_，因为您要查看工作状态。</span><span class="sxs-lookup"><span data-stu-id="43b1d-163">**X-axis value field** – Select _Work status_, because you want to view work status.</span></span>
- <span data-ttu-id="43b1d-164">**自动刷新** – 选择是否应自动刷新可视化。</span><span class="sxs-lookup"><span data-stu-id="43b1d-164">**Auto refresh** – Select whether the visualization should automatically be refreshed.</span></span>
- <span data-ttu-id="43b1d-165">**领料类型** – 选择 _初始领料和暂存领料_，因为您要同时包括初始领料和暂存库位中的领料。</span><span class="sxs-lookup"><span data-stu-id="43b1d-165">**Picking type** – Select _Initial picks and staged picks_, because you want to include both initial picks and picks from staging locations.</span></span> <span data-ttu-id="43b1d-166">换句话说，您本质上希望包括您拥有的所有领料工作行。</span><span class="sxs-lookup"><span data-stu-id="43b1d-166">In other words, you essentially want to include all the pick work lines that you have.</span></span>
- <span data-ttu-id="43b1d-167">**显示级别** – 选择 _未结行_，因为您要查看每行（而不是每个工作标题）的信息。</span><span class="sxs-lookup"><span data-stu-id="43b1d-167">**Display level** – Select _Open lines_, because you want to view the information per line, not per work header.</span></span>

<span data-ttu-id="43b1d-168">下图显示生成图表的示例。</span><span class="sxs-lookup"><span data-stu-id="43b1d-168">The following illustration shows an example of the resulting chart.</span></span>

<span data-ttu-id="43b1d-169">![区域与工作状态可视化](media/work-viz-chart.png "区域与工作状态可视化")</span><span class="sxs-lookup"><span data-stu-id="43b1d-169">![Zone vs. work status visualization](media/work-viz-chart.png "Zone vs. work status visualization")</span></span>

<span data-ttu-id="43b1d-170">此图表显示两个名为 **FLOOR** 和 **BULK** 的区域，再加上一个名为 **Blank** 的区域。</span><span class="sxs-lookup"><span data-stu-id="43b1d-170">This chart shows two zones that are named **FLOOR** and **BULK**, plus a zone that is named **Blank**.</span></span> <span data-ttu-id="43b1d-171">**Blank** 区域表示不是任何区域成员的所有工作行。</span><span class="sxs-lookup"><span data-stu-id="43b1d-171">The **Blank** zone represents all work lines that aren't members of any zones.</span></span> <span data-ttu-id="43b1d-172">该图表始终将所有不相关的筛选数据显示为 **Blank**，以提供尽可能多的可见性。</span><span class="sxs-lookup"><span data-stu-id="43b1d-172">The chart always shows all unrelated filtered data as **Blank**, to provide as much visibility as possible.</span></span> <span data-ttu-id="43b1d-173">在 **FLOOR** 区域中，图表显示三个已结行和四个未结行。</span><span class="sxs-lookup"><span data-stu-id="43b1d-173">In the **FLOOR** zone, the chart shows three closed lines and four open lines.</span></span> <span data-ttu-id="43b1d-174">在 **BULK** 区域中，图表显示四个已结行、一个未结行和 24 个已取消行。</span><span class="sxs-lookup"><span data-stu-id="43b1d-174">In the **BULK** zone, the chart shows four closed lines, one open line, and 24 canceled lines.</span></span> <span data-ttu-id="43b1d-175">最后，图表显示八个已结行，它们不属于任何区域，因此作为 **Blank** 列出。</span><span class="sxs-lookup"><span data-stu-id="43b1d-175">Finally, the chart shows eight closed lines that aren't part of any zone and are therefore listed as **Blank**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: 供应商发票条目工作区
description: 本主题介绍了如何设置与供应商发票相关并且显示通过 Microsoft Power BI 提供的信息的工作区。
author: abruer
manager: AnnBe
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2020-09-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a4ba676d9b6df69cf0a91862bcc4d2837b7cb69e
ms.sourcegitcommit: 0efa93f11847a2b75d13cd0a49e716c76130ec44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/14/2020
ms.locfileid: "4440913"
---
# <a name="vendor-invoice-entry-workspace"></a><span data-ttu-id="43efa-103">供应商发票条目工作区</span><span class="sxs-lookup"><span data-stu-id="43efa-103">Vendor invoice entry workspace</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="43efa-104">本主题介绍了如何设置与供应商发票相关并且显示通过 Microsoft Power BI 提供的信息的工作区。</span><span class="sxs-lookup"><span data-stu-id="43efa-104">This topic explains how to set up the workspace that is related to vendor invoices and that shows the information that is available through Microsoft Power BI.</span></span> <span data-ttu-id="43efa-105">此工作区中的供应商发票信息针对特定用户进行筛选，并以图形格式显示。</span><span class="sxs-lookup"><span data-stu-id="43efa-105">The vendor invoice information in this workspace is filtered for specific users and is shown in a graphical format.</span></span>

## <a name="overview"></a><span data-ttu-id="43efa-106">概览</span><span class="sxs-lookup"><span data-stu-id="43efa-106">Overview</span></span>

<span data-ttu-id="43efa-107">**供应商发票条目** 工作区显示与供应商发票处理相关的信息。</span><span class="sxs-lookup"><span data-stu-id="43efa-107">The **Vendor invoice entry** workspace shows information that is related to vendor invoice processing.</span></span> <span data-ttu-id="43efa-108">它包括 **我的工作** 视图和 **分析 - 所有公司** 页面。</span><span class="sxs-lookup"><span data-stu-id="43efa-108">It includes a **My work** view and an **Analytics - All companies** page.</span></span> <span data-ttu-id="43efa-109">**我的工作** 视图显示汇总磁贴、供应商交易记录网格和相关供应商信息。</span><span class="sxs-lookup"><span data-stu-id="43efa-109">The **My work** view shows summary tiles, vendor transaction grids, and related vendor information.</span></span> <span data-ttu-id="43efa-110">**分析 - 所有公司** 页面使用 Power BI 的功能显示与供应商发票相关的可视化。</span><span class="sxs-lookup"><span data-stu-id="43efa-110">The **Analytics - All companies** page uses the capabilities of Power BI to show visualizations that are related to vendor invoices.</span></span>

## <a name="set-up-the-workspace-to-show-power-bi-content"></a><span data-ttu-id="43efa-111">设置工作区以显示 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="43efa-111">Set up the workspace to show Power BI content</span></span>

<span data-ttu-id="43efa-112">您必须先完成此设置，然后才能在 **供应商发票条目** 工作区的 Power BI 可视化中显示数据。</span><span class="sxs-lookup"><span data-stu-id="43efa-112">You must complete this setup before data can be shown in Power BI visualizations in the **Vendor invoice entry** workspace.</span></span>

1. <span data-ttu-id="43efa-113">在 **功能管理** 工作区中，筛选列表以查找 **供应商发票自动化** 功能。</span><span class="sxs-lookup"><span data-stu-id="43efa-113">In the **Feature management** workspace, filter the list to find the **Vendor invoice automation** feature.</span></span>
3. <span data-ttu-id="43efa-114">选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="43efa-114">Select **Enable now**.</span></span>
4. <span data-ttu-id="43efa-115">为了确保整个发票处理流程都不需要人工干预，请设置供应商发票工作流。</span><span class="sxs-lookup"><span data-stu-id="43efa-115">To ensure that invoices can be processed from beginning to end without requiring manual intervention, set up a vendor invoice workflow.</span></span> <span data-ttu-id="43efa-116">若要设置工作流，请转到 **应付帐款 \> 设置 \> 应付帐款工作流**。</span><span class="sxs-lookup"><span data-stu-id="43efa-116">To set up a workflow, go to **Accounts payable \> Setup \> Accounts payable workflows**.</span></span>
5. <span data-ttu-id="43efa-117">转到 **应付帐款 \> 设置 \> 应付帐款参数**，然后选择 **供应商发票自动化** 选项卡。有关详细信息，请参阅[供应商发票自动化的设置选项](vnd-invoice-set-up-options.md)。</span><span class="sxs-lookup"><span data-stu-id="43efa-117">Go to **Accounts payable \> Setup \> Accounts payable parameters**, and select the **Vendor invoice automation** tab. For more information, see [Setup options for vendor invoice automation](vnd-invoice-set-up-options.md).</span></span>
6. <span data-ttu-id="43efa-118">将 **自动将导入的发票提交到工作流** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="43efa-118">Set the **Automatically submit imported invoices to workflow** option to **Yes**.</span></span>
7. <span data-ttu-id="43efa-119">如果应自动匹配物料收货，将 **自动将物料收货与发票行进行匹配** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="43efa-119">If product receipts should automatically be matched, set the **Automatically match product receipts to invoices lines** option to **Yes**.</span></span>
8. <span data-ttu-id="43efa-120">查看其余的可选设置，然后根据组织的要求进行配置。</span><span class="sxs-lookup"><span data-stu-id="43efa-120">Review the remaining, optional settings, and configure them according to your organization's requirements.</span></span>
9. <span data-ttu-id="43efa-121">转到 **系统管理 \> 设置 \> 系统参数**，设置 **系统币种** 和 **系统汇率** 字段。</span><span class="sxs-lookup"><span data-stu-id="43efa-121">Go to **System administration \> Setup \> System parameters**, and set the **System currency** and **System exchange rate** fields.</span></span>
10. <span data-ttu-id="43efa-122">转到 **总帐 \> 设置 \> 分类帐** 并设置 **会计币种** 和 **汇率类型** 字段。</span><span class="sxs-lookup"><span data-stu-id="43efa-122">Go to **General ledger \> Setup \> Ledger**, and set the **Accounting currency** and **Exchange rate type** fields.</span></span>
11. <span data-ttu-id="43efa-123">转到 **总帐 \> 币种 \> 币种汇率**，然后输入交易币种和会计币种之间以及会计币种和系统币种之间的汇率。</span><span class="sxs-lookup"><span data-stu-id="43efa-123">Go to **General ledger \> Currencies \> Currency exchange rates**, and enter the exchange rates between the transaction currency and the accounting currency, and between the accounting currency and the system currency.</span></span>
12. <span data-ttu-id="43efa-124">转到 **系统管理 \> 设置 \> 实体商店**，查找 **供应商发票自动化度量**。</span><span class="sxs-lookup"><span data-stu-id="43efa-124">Go to **System administration \> Setup \> Entity store**, and look for **Vendor invoice automation measure**.</span></span> <span data-ttu-id="43efa-125">选择 **刷新**。</span><span class="sxs-lookup"><span data-stu-id="43efa-125">Select **Refresh**.</span></span>

<span data-ttu-id="43efa-126">若要查看工作区中显示的信息，您必须具有应付帐款经理或应付帐款职员安全角色。</span><span class="sxs-lookup"><span data-stu-id="43efa-126">To view the information that displayed in the workspace, you must have the Accounts payable manager or Accounts payable clerk security role.</span></span>

## <a name="my-work-view"></a><span data-ttu-id="43efa-127">我的工作视图</span><span class="sxs-lookup"><span data-stu-id="43efa-127">My work view</span></span>

### <a name="company-selection"></a><span data-ttu-id="43efa-128">公司选择</span><span class="sxs-lookup"><span data-stu-id="43efa-128">Company selection</span></span>

<span data-ttu-id="43efa-129">当 **自动化供应商发票** 功能打开时，**公司** 字段显示在工作区的顶部。</span><span class="sxs-lookup"><span data-stu-id="43efa-129">When the **Automate vendor invoices** feature is turned on, a **Company** field appears at the top of the workspace.</span></span> <span data-ttu-id="43efa-130">**公司** 字段中的选择会影响工作区中显示的所有信息。</span><span class="sxs-lookup"><span data-stu-id="43efa-130">The selection in the **Company** field affects all the information displayed in the workspace.</span></span> <span data-ttu-id="43efa-131">默认情况下，该视图显示您登录的公司的信息。</span><span class="sxs-lookup"><span data-stu-id="43efa-131">By default, the view shows information for the company that you signed in to.</span></span> <span data-ttu-id="43efa-132">通过在 **公司** 字段中选择不同的公司，您可以在工作区上显示该公司的信息。</span><span class="sxs-lookup"><span data-stu-id="43efa-132">By selecting a different company in the **Company** field, you can show information for that company on the workspace.</span></span> <span data-ttu-id="43efa-133">然后，您可以在工作区中选择一个磁贴以转到所选公司的相关页面。</span><span class="sxs-lookup"><span data-stu-id="43efa-133">You can then select a tile in the workspace to go the related page in the selected company.</span></span>

### <a name="summary-tiles"></a><span data-ttu-id="43efa-134">汇总磁贴</span><span class="sxs-lookup"><span data-stu-id="43efa-134">Summary tiles</span></span>

<span data-ttu-id="43efa-135">**我的工作** 视图的 **待定发票汇总** 部分中的磁贴概述了供应商发票的状态。</span><span class="sxs-lookup"><span data-stu-id="43efa-135">The tiles in the **Summary of pending invoices** section of the **My work** view give an overview of the state of your vendor invoices.</span></span> <span data-ttu-id="43efa-136">您可以看到尚未过帐的日记帐和处于暂停状态的发票。</span><span class="sxs-lookup"><span data-stu-id="43efa-136">You can see journals that aren't yet posted and invoices that are on hold.</span></span> <span data-ttu-id="43efa-137">此外，还有与供应商发票自动化功能关联的四个磁贴：</span><span class="sxs-lookup"><span data-stu-id="43efa-137">In addition, there are the four tiles that are associated with the Vendor invoice automation feature:</span></span>

- <span data-ttu-id="43efa-138">需要手动收货匹配</span><span class="sxs-lookup"><span data-stu-id="43efa-138">Manual receipt match needed</span></span>
- <span data-ttu-id="43efa-139">匹配验证未成功</span><span class="sxs-lookup"><span data-stu-id="43efa-139">Matching validation not successful</span></span>
- <span data-ttu-id="43efa-140">未提交到工作流的账单</span><span class="sxs-lookup"><span data-stu-id="43efa-140">Invoices not submitted to workflow</span></span>
- <span data-ttu-id="43efa-141">未导入的账单</span><span class="sxs-lookup"><span data-stu-id="43efa-141">Invoices not imported</span></span>

<span data-ttu-id="43efa-142">（这四个磁贴要求在功能管理中打开供应商发票自动化功能。）</span><span class="sxs-lookup"><span data-stu-id="43efa-142">(These four tiles require that the Vendor invoice automation feature be turned on in Feature management.)</span></span>

<span data-ttu-id="43efa-143">若要使用 **恢复供应商发票** 磁贴，必须在应付帐款参数中打开该功能。</span><span class="sxs-lookup"><span data-stu-id="43efa-143">To use the **Recover vendor invoices** tile, the feature must be turned on in Accounts payable parameters.</span></span> <span data-ttu-id="43efa-144">转到 **应付帐款 \> 应付帐款参数**，然后在 **发票** 选项卡上，将 **允许恢复供应商发票** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="43efa-144">Go to **Accounts payable \> Accounts payable parameters**, and then, on the **Invoice** tab, set the **Allow vendor invoice recovery** option to **Yes**.</span></span>

<span data-ttu-id="43efa-145">打开该功能后，您还将在称为 **日记帐** 的部分中在工作区上将三个磁贴组合在一起。</span><span class="sxs-lookup"><span data-stu-id="43efa-145">When the feature is turned on, you will also three tiles grouped together on the workspace in a section called **Journals**.</span></span> <span data-ttu-id="43efa-146">这些磁贴名为 **日记帐**、**日记帐 - 分配给我** 和 **发票池**。</span><span class="sxs-lookup"><span data-stu-id="43efa-146">The tiles are titled **Journals**, **Journals - Assigned to me**, and **Invoice pool**.</span></span> 

<span data-ttu-id="43efa-147">**待定发票汇总** 部分中的信息适用于设置为您登录的默认公司的公司。</span><span class="sxs-lookup"><span data-stu-id="43efa-147">The information in the **Summary of pending invoices** section is for the company that is set as the default company for your sign-in.</span></span>

### <a name="creating-new-records"></a><span data-ttu-id="43efa-148">创建新记录</span><span class="sxs-lookup"><span data-stu-id="43efa-148">Creating new records</span></span>

<span data-ttu-id="43efa-149">若要创建新的发票记录，请选择 **新建**，然后在列表中选择以下记录类型之一：</span><span class="sxs-lookup"><span data-stu-id="43efa-149">To create a new invoice record, select **New**, and then select one of the following record types in the list:</span></span>

- <span data-ttu-id="43efa-150">供应商账单</span><span class="sxs-lookup"><span data-stu-id="43efa-150">Vendor invoice</span></span>
- <span data-ttu-id="43efa-151">账单日记帐</span><span class="sxs-lookup"><span data-stu-id="43efa-151">Invoice journal</span></span>
- <span data-ttu-id="43efa-152">全球账单日记帐</span><span class="sxs-lookup"><span data-stu-id="43efa-152">Global invoice journal</span></span>
- <span data-ttu-id="43efa-153">账单登记簿</span><span class="sxs-lookup"><span data-stu-id="43efa-153">Invoice register</span></span>
- <span data-ttu-id="43efa-154">账单审核</span><span class="sxs-lookup"><span data-stu-id="43efa-154">Invoice approval</span></span>

<span data-ttu-id="43efa-155">请注意，您创建的记录基于公司筛选器，而不是您登录的公司。</span><span class="sxs-lookup"><span data-stu-id="43efa-155">Note that the record that you create is based on the company filter, not the company that you're signed in to.</span></span> <span data-ttu-id="43efa-156">例如，您登录到 **UMSF** 公司，但公司筛选器设置为 **GBSI**。</span><span class="sxs-lookup"><span data-stu-id="43efa-156">For example, you're signed in to the **UMSF** company, but the company filter is set to **GBSI**.</span></span> <span data-ttu-id="43efa-157">在这种情况下，当您选择 **新建**，然后在列表中选择记录类型时，该记录将在 GBSI 公司中创建。</span><span class="sxs-lookup"><span data-stu-id="43efa-157">In this case, when you select **New** and then select a record type in the list, the record is created in the GBSI company.</span></span>

### <a name="documents-not-invoiced-grids"></a><span data-ttu-id="43efa-158">未开票的单据网格</span><span class="sxs-lookup"><span data-stu-id="43efa-158">Documents not invoiced grids</span></span>

<span data-ttu-id="43efa-159">**未开票的单据** 部分包含显示正在等待供应商发票的单据的网格。</span><span class="sxs-lookup"><span data-stu-id="43efa-159">The **Documents not invoiced** section contains grids that show documents that are awaiting vendor invoices.</span></span>

<span data-ttu-id="43efa-160">**未结采购订单** 网格显示所有尚未完全开票的采购订单。</span><span class="sxs-lookup"><span data-stu-id="43efa-160">The **Open purchase orders** grid shows all purchase orders that aren't yet fully invoiced.</span></span> <span data-ttu-id="43efa-161">您可以使用 **当前发票** 按钮为采购订单创建供应商发票。</span><span class="sxs-lookup"><span data-stu-id="43efa-161">You can use the **Invoice now** button to create a vendor invoice for a purchase order.</span></span> <span data-ttu-id="43efa-162">您可以使用 **当前预付款发票** 按钮为采购订单创建预付款发票。</span><span class="sxs-lookup"><span data-stu-id="43efa-162">You can use the **Prepayment invoice now** button to create a prepayment invoice for a purchase order.</span></span>

<span data-ttu-id="43efa-163">**物料收货** 网格显示尚未完全开票的采购收货交易。</span><span class="sxs-lookup"><span data-stu-id="43efa-163">The **Product receipts** grid shows purchase receipt transactions that aren't yet fully invoiced.</span></span> <span data-ttu-id="43efa-164">您可以使用 **当前发票** 按钮为采购订单创建供应商发票。</span><span class="sxs-lookup"><span data-stu-id="43efa-164">You can use the **Invoice now** button to create a vendor invoice for a purchase order.</span></span>

<span data-ttu-id="43efa-165">**待定供应商发票** 网格显示所有尚未提交到工作流系统的供应商发票。</span><span class="sxs-lookup"><span data-stu-id="43efa-165">The **Pending vendor invoices** grid shows all vendor invoices that haven't been submitted to the workflow system.</span></span> <span data-ttu-id="43efa-166">您可以使用 **搜索** 字段和/或公司筛选器搜索特定的供应商发票。</span><span class="sxs-lookup"><span data-stu-id="43efa-166">You can use the **Search** field and/or the company filter to search for a specific vendor invoice.</span></span> <span data-ttu-id="43efa-167">您可以使用 **编辑** 按钮以编辑显示在网格中的交易。</span><span class="sxs-lookup"><span data-stu-id="43efa-167">You can use the **Edit** button to edit a transaction that appears in the grid.</span></span>

<span data-ttu-id="43efa-168">在 **查找采购订单** 网格上，您可以使用 **搜索** 字段以搜索特定的采购订单。</span><span class="sxs-lookup"><span data-stu-id="43efa-168">On the **Find purchase order** grid, you can use the **Search** field to search for a specific purchase order.</span></span>

### <a name="related-information"></a><span data-ttu-id="43efa-169">相关信息</span><span class="sxs-lookup"><span data-stu-id="43efa-169">Related information</span></span>

<span data-ttu-id="43efa-170">您可以使用工作区右侧的链接查看有关过帐发票的信息。</span><span class="sxs-lookup"><span data-stu-id="43efa-170">You can view information about posted invoices by using the links on the right side of the workspace.</span></span> <span data-ttu-id="43efa-171">这些链接包括 **未结供应商发票**、**发票日记帐** 和 **发票历史记录和匹配详细信息**。</span><span class="sxs-lookup"><span data-stu-id="43efa-171">These links include **Open vendor invoices**, **Invoice journal**, and **Invoice history and matching details**.</span></span> <span data-ttu-id="43efa-172">在 **供应商** 部分中，您可以访问显示处于暂停状态的所有供应商的筛选列表，也可以使用 **所有供应商** 链接。</span><span class="sxs-lookup"><span data-stu-id="43efa-172">In the **Vendors** section, you can access a filtered list that shows all vendors that are on hold, or you can use the **All vendors** link.</span></span> <span data-ttu-id="43efa-173">**所有采购订单** 和 **未结预付款** 链接也可用。</span><span class="sxs-lookup"><span data-stu-id="43efa-173">**All purchase orders** and **Open prepayments** links are also available.</span></span>

### <a name="analytics--all-companies-page"></a><span data-ttu-id="43efa-174">分析 – 所有公司页面</span><span class="sxs-lookup"><span data-stu-id="43efa-174">Analytics – All companies page</span></span>

<span data-ttu-id="43efa-175">当在 **应付帐款参数** 页面上将 **自动将导入的发票提交到工作流** 选项设置为 **是** 时，您可以查看自动化分析。</span><span class="sxs-lookup"><span data-stu-id="43efa-175">When the **Automatically submit imported invoices to workflow** option is set to **Yes** on the **Accounts payable parameters** page, you can view automation analytics.</span></span> <span data-ttu-id="43efa-176">**分析 - 所有公司** 页面提供重要的指标，例如正在由审批者和公司审批的供应商发票。</span><span class="sxs-lookup"><span data-stu-id="43efa-176">The **Analytics - All companies** page provides important metrics, such as vendor invoices that are in approval by approver and by company.</span></span> <span data-ttu-id="43efa-177">此页面包含五个报告页面。</span><span class="sxs-lookup"><span data-stu-id="43efa-177">This page contains five report pages.</span></span> <span data-ttu-id="43efa-178">一个页面提供概述，其他页面提供有关应付帐款自动化指标的详细信息。</span><span class="sxs-lookup"><span data-stu-id="43efa-178">One page provides an overview, and the other pages provide details about Accounts payable automation metrics.</span></span>

<span data-ttu-id="43efa-179">下表显示在每个报表页上可用的可视化项。</span><span class="sxs-lookup"><span data-stu-id="43efa-179">The following table shows the visualizations that are available on each report page.</span></span>

| <span data-ttu-id="43efa-180">报表页</span><span class="sxs-lookup"><span data-stu-id="43efa-180">Report page</span></span>                    | <span data-ttu-id="43efa-181">可视化</span><span class="sxs-lookup"><span data-stu-id="43efa-181">Visualizations</span></span> |
|--------------------------------|----------------|
| <span data-ttu-id="43efa-182">供应商发票概述</span><span class="sxs-lookup"><span data-stu-id="43efa-182">Vendor invoice overview</span></span>        | <ul><li><span data-ttu-id="43efa-183">系统币种中自动化的待定供应商发票</span><span class="sxs-lookup"><span data-stu-id="43efa-183">Pending vendor invoices in automation in system currency</span></span></li><li><span data-ttu-id="43efa-184">导入失败的发票</span><span class="sxs-lookup"><span data-stu-id="43efa-184">Invoices that failed to import</span></span></li><li><span data-ttu-id="43efa-185">工作流中的发票</span><span class="sxs-lookup"><span data-stu-id="43efa-185">Invoices in workflow</span></span></li><li><span data-ttu-id="43efa-186">最近 30 天的非接触式发票</span><span class="sxs-lookup"><span data-stu-id="43efa-186">Touchless invoices last 30 days</span></span></li><li><span data-ttu-id="43efa-187">最近 30 天的自动化发票总数</span><span class="sxs-lookup"><span data-stu-id="43efa-187">Total automated invoices last 30 days</span></span></li><li><span data-ttu-id="43efa-188">系统币种中未结发票的余额</span><span class="sxs-lookup"><span data-stu-id="43efa-188">Balance of open invoices in system currency</span></span></li><li><span data-ttu-id="43efa-189">最近 30 天的失败原因</span><span class="sxs-lookup"><span data-stu-id="43efa-189">Reasons for failures, last 30 days</span></span></li><li><span data-ttu-id="43efa-190">自动处理的过帐发票的百分比</span><span class="sxs-lookup"><span data-stu-id="43efa-190">Percent of posted invoices that were processed automatically</span></span></li><li><span data-ttu-id="43efa-191">发票处理天数</span><span class="sxs-lookup"><span data-stu-id="43efa-191">Days to process an invoice</span></span></ul></li> |
| <span data-ttu-id="43efa-192">自动化状态</span><span class="sxs-lookup"><span data-stu-id="43efa-192">Automation status</span></span>              | <ul><li><span data-ttu-id="43efa-193">最近 30 天的非接触式发票</span><span class="sxs-lookup"><span data-stu-id="43efa-193">Touchless invoices last 30 days</span></span></li><li><span data-ttu-id="43efa-194">最近 30 天的非接触式发票（按公司）</span><span class="sxs-lookup"><span data-stu-id="43efa-194">Touchless invoices last 30 days by company</span></span></li><li><span data-ttu-id="43efa-195">最近 30 天的非接触式发票（按供应商组）</span><span class="sxs-lookup"><span data-stu-id="43efa-195">Touchless invoices last 30 days by vendor group</span></span></li><li><span data-ttu-id="43efa-196">自动处理的过帐发票的百分比</span><span class="sxs-lookup"><span data-stu-id="43efa-196">Percent of posted invoices that were processed automatically</span></span></li><li><span data-ttu-id="43efa-197">发票处理天数</span><span class="sxs-lookup"><span data-stu-id="43efa-197">Days to process an invoice</span></span></li></ul> |
| <span data-ttu-id="43efa-198">导入失败的发票</span><span class="sxs-lookup"><span data-stu-id="43efa-198">Invoices that failed to import</span></span> | <ul><li><span data-ttu-id="43efa-199">导入失败的发票</span><span class="sxs-lookup"><span data-stu-id="43efa-199">Invoices that failed to import</span></span></li><li><span data-ttu-id="43efa-200">导入失败的发票（按公司）</span><span class="sxs-lookup"><span data-stu-id="43efa-200">Invoices that failed to import by company</span></span></li></ul> |
| <span data-ttu-id="43efa-201">自动化失败的原因</span><span class="sxs-lookup"><span data-stu-id="43efa-201">Reasons for automation failure</span></span> | <ul><li><span data-ttu-id="43efa-202">失败的发票</span><span class="sxs-lookup"><span data-stu-id="43efa-202">Invoices failed</span></span></li><li><span data-ttu-id="43efa-203">失败的发票（按公司）</span><span class="sxs-lookup"><span data-stu-id="43efa-203">Invoices failed by company</span></span></li><li><span data-ttu-id="43efa-204">失败的发票（按供应商组）</span><span class="sxs-lookup"><span data-stu-id="43efa-204">Invoices failed by vendor group</span></span></li></ul> |
| <span data-ttu-id="43efa-205">工作流状态</span><span class="sxs-lookup"><span data-stu-id="43efa-205">Workflow status</span></span>                | <ul><li><span data-ttu-id="43efa-206">工作流中的发票</span><span class="sxs-lookup"><span data-stu-id="43efa-206">Invoices in workflow</span></span></li><li><span data-ttu-id="43efa-207">供应商发票工作流实例</span><span class="sxs-lookup"><span data-stu-id="43efa-207">Vendor invoice workflow instances</span></span></li><li><span data-ttu-id="43efa-208">分配（按审批者）</span><span class="sxs-lookup"><span data-stu-id="43efa-208">Assignment per approver</span></span></li><li><span data-ttu-id="43efa-209">供应商发票工作流（按公司）</span><span class="sxs-lookup"><span data-stu-id="43efa-209">Vendor invoice workflow per company</span></span></li><li><span data-ttu-id="43efa-210">工作流中的平均天数(按审批人)</span><span class="sxs-lookup"><span data-stu-id="43efa-210">Average days in workflow by approver</span></span></li></ul> |

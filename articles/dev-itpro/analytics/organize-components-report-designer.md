---
title: "整理报表设计器中的报表组件"
description: "在您设计构建基块并生成报表后，组织这些对象以便用户更容易地找到它们，这种方法非常有用。 本文介绍了如何组织现有报表、构建基块和报表设计器中的对象。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 850a40cc29f51521636c01f6ac1cfa54d3bd7798
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="06a8f-104">整理报表设计器中的报表组件</span><span class="sxs-lookup"><span data-stu-id="06a8f-104">Organize report components in report designer</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="06a8f-105">在您设计构建基块并生成报表后，组织这些对象以便用户更容易地找到它们，这种方法非常有用。</span><span class="sxs-lookup"><span data-stu-id="06a8f-105">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="06a8f-106">本文介绍了如何组织现有报表、构建基块和报表设计器中的对象。</span><span class="sxs-lookup"><span data-stu-id="06a8f-106">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="06a8f-107">您可以在报表设计器中重命名文件夹、报表、构建基块和其他对象以帮助整理您的文件。</span><span class="sxs-lookup"><span data-stu-id="06a8f-107">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="06a8f-108">根据重命名的对象的类型，您可能必须更新与该对象的关联。</span><span class="sxs-lookup"><span data-stu-id="06a8f-108">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="06a8f-109">在报表设计器中重命名文件夹或构建基块</span><span class="sxs-lookup"><span data-stu-id="06a8f-109">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="06a8f-110">在报表设计器中，您可以重命名文件夹、报表、列定义、行定义和报告结构树定义。</span><span class="sxs-lookup"><span data-stu-id="06a8f-110">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span> <span data-ttu-id="06a8f-111">**注意︰**重命名一个构建基块时，您必须更新使用构建基块的所有报告定义。</span><span class="sxs-lookup"><span data-stu-id="06a8f-111">**Note:** When you rename a building block, you must update any reporting definitions that use the building block.</span></span> <span data-ttu-id="06a8f-112">否则，不能生成新的报表。</span><span class="sxs-lookup"><span data-stu-id="06a8f-112">Otherwise, a new report can't be generated.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="06a8f-113">在报表设计器中重命名文件夹或构建基块</span><span class="sxs-lookup"><span data-stu-id="06a8f-113">Rename a folder or building block in Report Designer</span></span>

1.  <span data-ttu-id="06a8f-114">在报表设计器中，使用导航窗格找到要重命名的文件夹或对象。</span><span class="sxs-lookup"><span data-stu-id="06a8f-114">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2.  <span data-ttu-id="06a8f-115">右键单击该文件夹或对象，然后单击**“重命名”**。</span><span class="sxs-lookup"><span data-stu-id="06a8f-115">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="06a8f-116">导航窗格中的**名称**字段将变为可用。</span><span class="sxs-lookup"><span data-stu-id="06a8f-116">The **Name** field in the navigation pane becomes available.</span></span>
3.  <span data-ttu-id="06a8f-117">键入新名称，然后按 Enter。</span><span class="sxs-lookup"><span data-stu-id="06a8f-117">Type a new name, and then press Enter.</span></span>
4.  <span data-ttu-id="06a8f-118">如果构建基块是行定义、列定义或报告结构树定义，则必须更新与其关联的其他构建基块。</span><span class="sxs-lookup"><span data-stu-id="06a8f-118">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="06a8f-119">右键单击在步骤 3 中重命名的构建基块，选择**关联**，然后选择列表中的某个项目以更新它。</span><span class="sxs-lookup"><span data-stu-id="06a8f-119">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5.  <span data-ttu-id="06a8f-120">重复步骤 4，直到所有关联项目都已更新。</span><span class="sxs-lookup"><span data-stu-id="06a8f-120">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="06a8f-121">创建和管理报表组</span><span class="sxs-lookup"><span data-stu-id="06a8f-121">Create and manage report groups</span></span>
<span data-ttu-id="06a8f-122">您可以对报表定义进行分组以同时生成多个报表。</span><span class="sxs-lookup"><span data-stu-id="06a8f-122">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="06a8f-123">要创建、修改、删除和生成报表组，您必须具有设计人员或管理员角色。</span><span class="sxs-lookup"><span data-stu-id="06a8f-123">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="06a8f-124">具有生成人员角色的用户可生成报表组，还可修改为报告组设置的用户报表定义。</span><span class="sxs-lookup"><span data-stu-id="06a8f-124">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="06a8f-125">创建报表组</span><span class="sxs-lookup"><span data-stu-id="06a8f-125">Create a report group</span></span>

1.  <span data-ttu-id="06a8f-126">在报表设计器中，单击导航窗格中的**报表组**。</span><span class="sxs-lookup"><span data-stu-id="06a8f-126">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="06a8f-127">在**文件**菜单上，单击**新建** &gt; **报表组定义**在查看器窗口中打开一个新报告组。</span><span class="sxs-lookup"><span data-stu-id="06a8f-127">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="06a8f-128">或者，单击工具栏上的**报表组**按钮 ![报表组](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "报表组")。</span><span class="sxs-lookup"><span data-stu-id="06a8f-128">Alternatively, click the **Report Group** button ![Report Group](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Report Group") on the toolbar.</span></span>
3.  <span data-ttu-id="06a8f-129">单击**报表组**选项卡。要覆盖用于生成此报表的各个报表定义的相关信息，请选中**覆盖各个报表定义中的公司、详细信息和日期设置**复选框。</span><span class="sxs-lookup"><span data-stu-id="06a8f-129">Click the **Report Group** tab. To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="06a8f-130">公司名称、详细级别、临时设置和日期信息将自动输入，但您仍可以进行更新。</span><span class="sxs-lookup"><span data-stu-id="06a8f-130">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4.  <span data-ttu-id="06a8f-131">如果要生成显示申报币种的多个报表，请选中**包含所有申报币种**复选框。</span><span class="sxs-lookup"><span data-stu-id="06a8f-131">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="06a8f-132">然后您可以通过在查看报表时单击 Web 查看器上的**币种**按钮来访问多个视图。</span><span class="sxs-lookup"><span data-stu-id="06a8f-132">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5.  <span data-ttu-id="06a8f-133">在**组中的报表**字段中，单击**添加**以选择要包含在报表组中的报表。</span><span class="sxs-lookup"><span data-stu-id="06a8f-133">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="06a8f-134">要在**添加**对话框中选择多个报表，请在按住 Ctrl 键的同时选择报表。</span><span class="sxs-lookup"><span data-stu-id="06a8f-134">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="06a8f-135">完成选择报告后，单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="06a8f-135">When you've finished selecting reports, click **OK**.</span></span>
6.  <span data-ttu-id="06a8f-136">单击**文件** &gt; **保存**以保存新报表组。</span><span class="sxs-lookup"><span data-stu-id="06a8f-136">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="06a8f-137">修改报表组</span><span class="sxs-lookup"><span data-stu-id="06a8f-137">Modify a report group</span></span>

1.  <span data-ttu-id="06a8f-138">在报表设计器中，单击导航窗格中的**报表组**。</span><span class="sxs-lookup"><span data-stu-id="06a8f-138">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="06a8f-139">双击要修改的报表组。</span><span class="sxs-lookup"><span data-stu-id="06a8f-139">Double-click the report group to modify.</span></span>
3.  <span data-ttu-id="06a8f-140">在**报表组**选项卡上，进行所需的更改。</span><span class="sxs-lookup"><span data-stu-id="06a8f-140">On the **Report Group** tab, make the changes that you want.</span></span>
4.  <span data-ttu-id="06a8f-141">在**文件**菜单中，单击**保存**保存修改过的报表组，或者单击工具栏中的**保存**按钮 ![保存](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "保存")。</span><span class="sxs-lookup"><span data-stu-id="06a8f-141">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Save") on the toolbar.</span></span>

<span data-ttu-id="06a8f-142">**注意：**如果您已计划了报表以便它们以设置的间隔生成，则可以覆盖这些设置并立即生成报表。</span><span class="sxs-lookup"><span data-stu-id="06a8f-142">**Note:** If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="06a8f-143">生成报表组报表</span><span class="sxs-lookup"><span data-stu-id="06a8f-143">Generate a report group report</span></span>

1.  <span data-ttu-id="06a8f-144">在报表设计器中，单击导航窗格中的**报表组**。</span><span class="sxs-lookup"><span data-stu-id="06a8f-144">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="06a8f-145">打开要生成的报表组。</span><span class="sxs-lookup"><span data-stu-id="06a8f-145">Open the report group to generate.</span></span>
3.  <span data-ttu-id="06a8f-146">单击**生成报表**按钮![生成报表](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "生成报表")以生成报表。</span><span class="sxs-lookup"><span data-stu-id="06a8f-146">Click the **Generate Report** button ![Generate Report](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="06a8f-147">删除报表组</span><span class="sxs-lookup"><span data-stu-id="06a8f-147">Delete a report group</span></span>

1.  <span data-ttu-id="06a8f-148">在报表设计器中，单击导航窗格中的**报表组**。</span><span class="sxs-lookup"><span data-stu-id="06a8f-148">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="06a8f-149">右键单击要删除的报表组，然后选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="06a8f-149">Right-click the report group to delete, and then select **Delete**.</span></span>
3.  <span data-ttu-id="06a8f-150">当出现一条确认消息时，请单击**是**。</span><span class="sxs-lookup"><span data-stu-id="06a8f-150">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="06a8f-151">“报表组”选项卡控件</span><span class="sxs-lookup"><span data-stu-id="06a8f-151">Report Group tab controls</span></span>
<span data-ttu-id="06a8f-152">下表描述**报表组**选项卡的控件。</span><span class="sxs-lookup"><span data-stu-id="06a8f-152">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06a8f-153">控件</span><span class="sxs-lookup"><span data-stu-id="06a8f-153">Control</span></span></th>
<th><span data-ttu-id="06a8f-154">说明</span><span class="sxs-lookup"><span data-stu-id="06a8f-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06a8f-155">覆盖各个报表定义中的公司、详细信息和日期设置</span><span class="sxs-lookup"><span data-stu-id="06a8f-155">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="06a8f-156">选中此复选框可覆盖此报表组中的报表的各个报表定义（仅用于生成这些报表）。</span><span class="sxs-lookup"><span data-stu-id="06a8f-156">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06a8f-157">公司名称</span><span class="sxs-lookup"><span data-stu-id="06a8f-157">Company name</span></span></td>
<td><span data-ttu-id="06a8f-158">选择要用于报表的公司。</span><span class="sxs-lookup"><span data-stu-id="06a8f-158">Select the company to use for the reports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06a8f-159">详细程度</span><span class="sxs-lookup"><span data-stu-id="06a8f-159">Detail level</span></span></td>
<td><span data-ttu-id="06a8f-160">指定报表中包含的详细信息级别。</span><span class="sxs-lookup"><span data-stu-id="06a8f-160">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="06a8f-161">“财务”<strong></strong>− 高级别的摘要报表。</span><span class="sxs-lookup"><span data-stu-id="06a8f-161"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="06a8f-162">您无法深化到科目和维度（通过报告结构树添加的帐户和维度除外）。</span><span class="sxs-lookup"><span data-stu-id="06a8f-162">You can&#39;t drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="06a8f-163"><strong>财务 &amp; 科目</strong> - 包含高度概括性汇总和科目详细信息的报表。</span><span class="sxs-lookup"><span data-stu-id="06a8f-163"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="06a8f-164"><strong>财务、科目 &amp; 交易记录</strong> - 包含高度概括性汇总和交易记录详细信息的报表。</span><span class="sxs-lookup"><span data-stu-id="06a8f-164"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06a8f-165">临时信息</span><span class="sxs-lookup"><span data-stu-id="06a8f-165">Provisional</span></span></td>
<td><span data-ttu-id="06a8f-166">指定报表中包含的活动的类型。</span><span class="sxs-lookup"><span data-stu-id="06a8f-166">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="06a8f-167"><strong>仅限过账活动</strong> − 仅包括财务数据中已过帐的交易记录和余额。</span><span class="sxs-lookup"><span data-stu-id="06a8f-167"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="06a8f-168"><strong>已过帐和未过账的活动</strong> − 包括财务数据中输入的和已过帐的所有交易记录和余额。</span><span class="sxs-lookup"><span data-stu-id="06a8f-168"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="06a8f-169"><strong>仅限未过账活动</strong> − 仅包括财务数据中已输入但尚未过帐的交易记录。</span><span class="sxs-lookup"><span data-stu-id="06a8f-169"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06a8f-170">包括所有申报币种</span><span class="sxs-lookup"><span data-stu-id="06a8f-170">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="06a8f-171">在 Microsoft Dynamics ERP 系统中配置的所有其他申报币种均在此处列出。</span><span class="sxs-lookup"><span data-stu-id="06a8f-171">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="06a8f-172">选择此复选框以生成使用指定的币种的其他报表。</span><span class="sxs-lookup"><span data-stu-id="06a8f-172">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="06a8f-173">若要在 Web 查看器中查看这些报表，请单击“币种”<strong></strong>，然后选择一种货币。</span><span class="sxs-lookup"><span data-stu-id="06a8f-173">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06a8f-174">不与报表定义一起保存的日期信息</span><span class="sxs-lookup"><span data-stu-id="06a8f-174">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="06a8f-175">基准期间</span><span class="sxs-lookup"><span data-stu-id="06a8f-175">Base period</span></span></li>
<li><span data-ttu-id="06a8f-176">基准年</span><span class="sxs-lookup"><span data-stu-id="06a8f-176">Base year</span></span></li>
<li><span data-ttu-id="06a8f-177">覆盖的期间</span><span class="sxs-lookup"><span data-stu-id="06a8f-177">Period covered</span></span></li>
</ul>
<span data-ttu-id="06a8f-178">只有默认基准期间设置与报表定义一起保存。</span><span class="sxs-lookup"><span data-stu-id="06a8f-178">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06a8f-179">与报表定义一起保存的日期信息</span><span class="sxs-lookup"><span data-stu-id="06a8f-179">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="06a8f-180">报表日期</span><span class="sxs-lookup"><span data-stu-id="06a8f-180">Report date</span></span></li>
<li><span data-ttu-id="06a8f-181">默认基准期间</span><span class="sxs-lookup"><span data-stu-id="06a8f-181">Default base period</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06a8f-182">组中的报表</span><span class="sxs-lookup"><span data-stu-id="06a8f-182">Reports in group</span></span></td>
<td><span data-ttu-id="06a8f-183">添加、删除和重新排序报表组中的报表。</span><span class="sxs-lookup"><span data-stu-id="06a8f-183">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="06a8f-184">若要将报表定义添加到报表组，请双击该报表组以将其打开，然后单击“添加”<strong></strong>。</span><span class="sxs-lookup"><span data-stu-id="06a8f-184">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="06a8f-185">选择要包含在报表组中的报表，然后单击“确定”<strong></strong>。</span><span class="sxs-lookup"><span data-stu-id="06a8f-185">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="06a8f-186">若要从报表组删除报表，选中该报表，然后单击“删除”<strong></strong>。</span><span class="sxs-lookup"><span data-stu-id="06a8f-186">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="06a8f-187">要修改生成报表的顺序，请在列表中选择一个报表，然后单击<strong>上移</strong>或<strong>下移</strong>。</span><span class="sxs-lookup"><span data-stu-id="06a8f-187">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="06a8f-188">请参阅</span><span class="sxs-lookup"><span data-stu-id="06a8f-188">See also</span></span>
--------

[<span data-ttu-id="06a8f-189">财务申报</span><span class="sxs-lookup"><span data-stu-id="06a8f-189">Financial reporting</span></span>](financial-reporting-intro.md)





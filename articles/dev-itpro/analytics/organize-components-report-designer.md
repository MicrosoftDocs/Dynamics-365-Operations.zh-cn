---
title: 整理报表设计器中的报表组件
description: 在您设计构建基块并生成报表后，组织这些对象以便用户更容易地找到它们，这种方法非常有用。 本文介绍了如何组织现有报表、构建基块和报表设计器中的对象。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
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
ms.openlocfilehash: 3f2b34cccfd84a9e4bb76e7a1da64e5cefa9982e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551735"
---
# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="61ce0-104">整理报表设计器中的报表组件</span><span class="sxs-lookup"><span data-stu-id="61ce0-104">Organize report components in report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61ce0-105">在您设计构建基块并生成报表后，组织这些对象以便用户更容易地找到它们，这种方法非常有用。</span><span class="sxs-lookup"><span data-stu-id="61ce0-105">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="61ce0-106">本文介绍了如何组织现有报表、构建基块和报表设计器中的对象。</span><span class="sxs-lookup"><span data-stu-id="61ce0-106">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="61ce0-107">您可以在报表设计器中重命名文件夹、报表、构建基块和其他对象以帮助整理您的文件。</span><span class="sxs-lookup"><span data-stu-id="61ce0-107">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="61ce0-108">根据重命名的对象的类型，您可能必须更新与该对象的关联。</span><span class="sxs-lookup"><span data-stu-id="61ce0-108">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="61ce0-109">在报表设计器中重命名文件夹或构建基块</span><span class="sxs-lookup"><span data-stu-id="61ce0-109">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="61ce0-110">在报表设计器中，你可以重命名文件夹、报表定义、行定义、列定义和报告树定义。</span><span class="sxs-lookup"><span data-stu-id="61ce0-110">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="61ce0-111">在报表设计器中重命名文件夹或构建基块</span><span class="sxs-lookup"><span data-stu-id="61ce0-111">Rename a folder or building block in Report Designer</span></span>

1. <span data-ttu-id="61ce0-112">在报表设计器中，使用导航窗格找到要重命名的文件夹或对象。</span><span class="sxs-lookup"><span data-stu-id="61ce0-112">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2. <span data-ttu-id="61ce0-113">右键单击该文件夹或对象，然后单击**重命名**。</span><span class="sxs-lookup"><span data-stu-id="61ce0-113">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="61ce0-114">导航窗格中的**名称**字段将变为可用。</span><span class="sxs-lookup"><span data-stu-id="61ce0-114">The **Name** field in the navigation pane becomes available.</span></span>
3. <span data-ttu-id="61ce0-115">键入新名称，然后按 Enter。</span><span class="sxs-lookup"><span data-stu-id="61ce0-115">Type a new name, and then press Enter.</span></span>
4. <span data-ttu-id="61ce0-116">如果构建基块是行定义、列定义或报告结构树定义，则必须更新与其关联的其他构建基块。</span><span class="sxs-lookup"><span data-stu-id="61ce0-116">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="61ce0-117">右键单击在步骤 3 中重命名的构建基块，选择**关联**，然后选择列表中的某个项目以更新它。</span><span class="sxs-lookup"><span data-stu-id="61ce0-117">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5. <span data-ttu-id="61ce0-118">重复步骤 4，直到所有关联项目都已更新。</span><span class="sxs-lookup"><span data-stu-id="61ce0-118">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="61ce0-119">创建和管理报表组</span><span class="sxs-lookup"><span data-stu-id="61ce0-119">Create and manage report groups</span></span>
<span data-ttu-id="61ce0-120">您可以对报表定义进行分组以同时生成多个报表。</span><span class="sxs-lookup"><span data-stu-id="61ce0-120">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="61ce0-121">要创建、修改、删除和生成报表组，您必须具有设计人员或管理员角色。</span><span class="sxs-lookup"><span data-stu-id="61ce0-121">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="61ce0-122">具有生成人员角色的用户可生成报表组，还可修改为报告组设置的用户报表定义。</span><span class="sxs-lookup"><span data-stu-id="61ce0-122">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="61ce0-123">创建报表组</span><span class="sxs-lookup"><span data-stu-id="61ce0-123">Create a report group</span></span>

1. <span data-ttu-id="61ce0-124">在报表设计器中，单击导航窗格中的**报表组**。</span><span class="sxs-lookup"><span data-stu-id="61ce0-124">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="61ce0-125">在**文件**菜单上，单击**新建** &gt; **报表组定义**在查看器窗口中打开一个新报告组。</span><span class="sxs-lookup"><span data-stu-id="61ce0-125">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="61ce0-126">或者，单击工具栏上的**报表组**按钮 ![报表组](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "报表组")。</span><span class="sxs-lookup"><span data-stu-id="61ce0-126">Alternatively, click the **Report Group** button ![Report Group](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Report Group") on the toolbar.</span></span>
3. <span data-ttu-id="61ce0-127">单击**报表组**选项卡。要覆盖用于生成此报表的各个报表定义的相关信息，请选中**覆盖各个报表定义中的公司、详细信息和日期设置**复选框。</span><span class="sxs-lookup"><span data-stu-id="61ce0-127">Click the **Report Group** tab. To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="61ce0-128">公司名称、详细级别、临时设置和日期信息将自动输入，但您仍可以进行更新。</span><span class="sxs-lookup"><span data-stu-id="61ce0-128">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4. <span data-ttu-id="61ce0-129">如果要生成显示申报币种的多个报表，请选中**包含所有申报币种**复选框。</span><span class="sxs-lookup"><span data-stu-id="61ce0-129">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="61ce0-130">然后您可以通过在查看报表时单击 Web 查看器上的**币种**按钮来访问多个视图。</span><span class="sxs-lookup"><span data-stu-id="61ce0-130">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5. <span data-ttu-id="61ce0-131">在**组中的报表**字段中，单击**添加**以选择要包含在报表组中的报表。</span><span class="sxs-lookup"><span data-stu-id="61ce0-131">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="61ce0-132">要在**添加**对话框中选择多个报表，请在按住 Ctrl 键的同时选择报表。</span><span class="sxs-lookup"><span data-stu-id="61ce0-132">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="61ce0-133">完成选择报告后，单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="61ce0-133">When you've finished selecting reports, click **OK**.</span></span>
6. <span data-ttu-id="61ce0-134">单击**文件** &gt; **保存**以保存新报表组。</span><span class="sxs-lookup"><span data-stu-id="61ce0-134">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="61ce0-135">修改报表组</span><span class="sxs-lookup"><span data-stu-id="61ce0-135">Modify a report group</span></span>

1. <span data-ttu-id="61ce0-136">在报表设计器中，单击导航窗格中的**报表组**。</span><span class="sxs-lookup"><span data-stu-id="61ce0-136">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="61ce0-137">双击要修改的报表组。</span><span class="sxs-lookup"><span data-stu-id="61ce0-137">Double-click the report group to modify.</span></span>
3. <span data-ttu-id="61ce0-138">在**报表组**选项卡上，进行所需的更改。</span><span class="sxs-lookup"><span data-stu-id="61ce0-138">On the **Report Group** tab, make the changes that you want.</span></span>
4. <span data-ttu-id="61ce0-139">在**文件**菜单中，单击**保存**保存修改过的报表组，或者单击工具栏中的**保存**按钮 ![保存](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "保存")。</span><span class="sxs-lookup"><span data-stu-id="61ce0-139">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Save") on the toolbar.</span></span>

> <span data-ttu-id="61ce0-140">[注意] 如果您已计划了报表以便它们以设置的间隔生成，则可以覆盖这些设置并立即生成报表。</span><span class="sxs-lookup"><span data-stu-id="61ce0-140">[NOTE] If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="61ce0-141">生成报表组报表</span><span class="sxs-lookup"><span data-stu-id="61ce0-141">Generate a report group report</span></span>

1. <span data-ttu-id="61ce0-142">在报表设计器中，单击导航窗格中的**报表组**。</span><span class="sxs-lookup"><span data-stu-id="61ce0-142">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="61ce0-143">打开要生成的报表组。</span><span class="sxs-lookup"><span data-stu-id="61ce0-143">Open the report group to generate.</span></span>
3. <span data-ttu-id="61ce0-144">单击**生成报表**按钮![生成报表](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "生成报表")以生成报表。</span><span class="sxs-lookup"><span data-stu-id="61ce0-144">Click the **Generate Report** button ![Generate Report](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="61ce0-145">删除报表组</span><span class="sxs-lookup"><span data-stu-id="61ce0-145">Delete a report group</span></span>

1. <span data-ttu-id="61ce0-146">在报表设计器中，单击导航窗格中的**报表组**。</span><span class="sxs-lookup"><span data-stu-id="61ce0-146">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="61ce0-147">右键单击要删除的报表组，然后选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="61ce0-147">Right-click the report group to delete, and then select **Delete**.</span></span>
3. <span data-ttu-id="61ce0-148">当出现一条确认消息时，请单击**是**。</span><span class="sxs-lookup"><span data-stu-id="61ce0-148">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="61ce0-149">“报表组”选项卡控件</span><span class="sxs-lookup"><span data-stu-id="61ce0-149">Report Group tab controls</span></span>
<span data-ttu-id="61ce0-150">下表描述**报表组**选项卡的控件。</span><span class="sxs-lookup"><span data-stu-id="61ce0-150">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="61ce0-151">控件</span><span class="sxs-lookup"><span data-stu-id="61ce0-151">Control</span></span></th>
<th><span data-ttu-id="61ce0-152">说明</span><span class="sxs-lookup"><span data-stu-id="61ce0-152">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61ce0-153">覆盖各个报表定义中的公司、详细信息和日期设置</span><span class="sxs-lookup"><span data-stu-id="61ce0-153">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="61ce0-154">选中此复选框可覆盖此报表组中的报表的各个报表定义（仅用于生成这些报表）。</span><span class="sxs-lookup"><span data-stu-id="61ce0-154">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61ce0-155">公司名称</span><span class="sxs-lookup"><span data-stu-id="61ce0-155">Company name</span></span></td>
<td><span data-ttu-id="61ce0-156">选择要用于报表的公司。</span><span class="sxs-lookup"><span data-stu-id="61ce0-156">Select the company to use for the reports.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61ce0-157">详细程度</span><span class="sxs-lookup"><span data-stu-id="61ce0-157">Detail level</span></span></td>
<td><span data-ttu-id="61ce0-158">指定报表中包含的详细信息级别。</span><span class="sxs-lookup"><span data-stu-id="61ce0-158">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="61ce0-159"><strong>财务</strong>− 高级别的摘要报表。</span><span class="sxs-lookup"><span data-stu-id="61ce0-159"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="61ce0-160">您无法深化到科目和维度（通过报告结构树添加的帐户和维度除外）。</span><span class="sxs-lookup"><span data-stu-id="61ce0-160">You can&#39;t drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="61ce0-161"><strong>财务 &amp; 科目</strong> - 包含高度概括性汇总和科目详细信息的报表。</span><span class="sxs-lookup"><span data-stu-id="61ce0-161"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="61ce0-162"><strong>财务、科目 &amp; 交易记录</strong> - 包含高度概括性汇总和交易记录详细信息的报表。</span><span class="sxs-lookup"><span data-stu-id="61ce0-162"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="61ce0-163">临时信息</span><span class="sxs-lookup"><span data-stu-id="61ce0-163">Provisional</span></span></td>
<td><span data-ttu-id="61ce0-164">指定报表中包含的活动的类型。</span><span class="sxs-lookup"><span data-stu-id="61ce0-164">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="61ce0-165"><strong>仅限过账活动</strong> − 仅包括财务数据中已过帐的交易记录和余额。</span><span class="sxs-lookup"><span data-stu-id="61ce0-165"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="61ce0-166"><strong>已过帐和未过账的活动</strong> − 包括财务数据中输入的和已过帐的所有交易记录和余额。</span><span class="sxs-lookup"><span data-stu-id="61ce0-166"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="61ce0-167"><strong>仅限未过账活动</strong> − 仅包括财务数据中已输入但尚未过帐的交易记录。</span><span class="sxs-lookup"><span data-stu-id="61ce0-167"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="61ce0-168">包括所有申报币种</span><span class="sxs-lookup"><span data-stu-id="61ce0-168">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="61ce0-169">在 Microsoft Dynamics ERP 系统中配置的所有其他申报币种均在此处列出。</span><span class="sxs-lookup"><span data-stu-id="61ce0-169">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="61ce0-170">选择此复选框以生成使用指定的币种的其他报表。</span><span class="sxs-lookup"><span data-stu-id="61ce0-170">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="61ce0-171">若要在 Web 查看器中查看这些报表，请单击<strong>币种</strong>，然后选择一种货币。</span><span class="sxs-lookup"><span data-stu-id="61ce0-171">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61ce0-172">不与报表定义一起保存的日期信息</span><span class="sxs-lookup"><span data-stu-id="61ce0-172">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="61ce0-173">基准期间</span><span class="sxs-lookup"><span data-stu-id="61ce0-173">Base period</span></span></li>
<li><span data-ttu-id="61ce0-174">基准年</span><span class="sxs-lookup"><span data-stu-id="61ce0-174">Base year</span></span></li>
<li><span data-ttu-id="61ce0-175">覆盖的期间</span><span class="sxs-lookup"><span data-stu-id="61ce0-175">Period covered</span></span></li>
</ul>
<span data-ttu-id="61ce0-176">只有默认基准期间设置与报表定义一起保存。</span><span class="sxs-lookup"><span data-stu-id="61ce0-176">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61ce0-177">与报表定义一起保存的日期信息</span><span class="sxs-lookup"><span data-stu-id="61ce0-177">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="61ce0-178">报表日期</span><span class="sxs-lookup"><span data-stu-id="61ce0-178">Report date</span></span></li>
<li><span data-ttu-id="61ce0-179">默认基准期间</span><span class="sxs-lookup"><span data-stu-id="61ce0-179">Default base period</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="61ce0-180">组中的报表</span><span class="sxs-lookup"><span data-stu-id="61ce0-180">Reports in group</span></span></td>
<td><span data-ttu-id="61ce0-181">添加、删除和重新排序报表组中的报表。</span><span class="sxs-lookup"><span data-stu-id="61ce0-181">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="61ce0-182">若要将报表定义添加到报表组，请双击该报表组以将其打开，然后单击<strong>添加</strong>。</span><span class="sxs-lookup"><span data-stu-id="61ce0-182">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="61ce0-183">选择要包含在报表组中的报表，然后单击<strong>确定</strong>。</span><span class="sxs-lookup"><span data-stu-id="61ce0-183">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="61ce0-184">若要从报表组删除报表，选中该报表，然后单击<strong>删除</strong>。</span><span class="sxs-lookup"><span data-stu-id="61ce0-184">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="61ce0-185">要修改生成报表的顺序，请在列表中选择一个报表，然后单击<strong>上移</strong>或<strong>下移</strong>。</span><span class="sxs-lookup"><span data-stu-id="61ce0-185">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="61ce0-186">其他资源</span><span class="sxs-lookup"><span data-stu-id="61ce0-186">Additional resources</span></span>

[<span data-ttu-id="61ce0-187">财务申报</span><span class="sxs-lookup"><span data-stu-id="61ce0-187">Financial reporting</span></span>](financial-reporting-intro.md)

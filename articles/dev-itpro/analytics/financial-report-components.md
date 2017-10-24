---
title: "财务报表组件"
description: "本文介绍如何在财务报告中使用报表定义的组件或构建基块。 这些构造基块包括行定义、列定义和报告树定义。 本文章介绍了如何组织和锁定构建基块，以及如何使用构建基块组。"
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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 074a2f377c16d47e95343dae3ebec6cbba4d5050
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="financial-report-components"></a><span data-ttu-id="f547d-105">财务报表组件</span><span class="sxs-lookup"><span data-stu-id="f547d-105">Financial report components</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f547d-106">本文介绍如何在财务报告中使用报表定义的组件或构建基块。</span><span class="sxs-lookup"><span data-stu-id="f547d-106">This article describes how the components, or building blocks, of report definitions are used in financial reporting.</span></span> <span data-ttu-id="f547d-107">这些构造基块包括行定义、列定义和报告树定义。</span><span class="sxs-lookup"><span data-stu-id="f547d-107">These building blocks include row definitions, column definitions, and reporting tree definitions.</span></span> <span data-ttu-id="f547d-108">本文章介绍了如何组织和锁定构建基块，以及如何使用构建基块组。</span><span class="sxs-lookup"><span data-stu-id="f547d-108">The article explains how to organize and lock building blocks, and how to work with building block groups.</span></span> 

<span data-ttu-id="f547d-109">财务报表设计器的设计理念是将信息分解为最小的组件或构建基块，然后根据需要混合和匹配组件。</span><span class="sxs-lookup"><span data-stu-id="f547d-109">The design philosophy behind financial report designer is to break information down into the smallest component or building block, and then mix and match the components as required.</span></span> <span data-ttu-id="f547d-110">因此，您的报表格式独立于您的财务数据，您可以更改报表的设计，而无需修改 Microsoft Dynamics ERP 系统中的财务数据。</span><span class="sxs-lookup"><span data-stu-id="f547d-110">Therefore, your report formatting is separate from your financial data, and you can change the design of a report without modifying the financial data in your Microsoft Dynamics ERP system.</span></span> <span data-ttu-id="f547d-111">通过使用此构建基块方法，您可以组合文本、金额和计算，以生成所需的报表。</span><span class="sxs-lookup"><span data-stu-id="f547d-111">By using this building block approach, you can combine text, amounts, and calculations to produce the reports that you require.</span></span> <span data-ttu-id="f547d-112">此外，这种灵活性通过方便您以各种方式查看操作来激发创造力。</span><span class="sxs-lookup"><span data-stu-id="f547d-112">Additionally, this flexibility encourages creativity by making it easy for you to view your operations in different ways.</span></span> <span data-ttu-id="f547d-113">报表定义的单个构建基块类似于一个三维电子表格，但前者具有更多功能。</span><span class="sxs-lookup"><span data-stu-id="f547d-113">The individual building blocks of a report definition are similar to a three-dimensional spreadsheet, but they have more power.</span></span> <span data-ttu-id="f547d-114">报表定义指定应用于报表的行定义、列定义和可选报告树定义。</span><span class="sxs-lookup"><span data-stu-id="f547d-114">A report definition specifies the row definition, column definition, and optional reporting tree definition that should be used for the report.</span></span> <span data-ttu-id="f547d-115">它还包含有关存储生成的报表的位置以及如果设置报表格式的信息。</span><span class="sxs-lookup"><span data-stu-id="f547d-115">It also includes information about where to store the report that is generated and how to format it.</span></span> <span data-ttu-id="f547d-116">为了实现更好的可重用性和共享，您可以创建构建基块组，这是一个与公司关联的现有报表定义、行定义、列定义、报告树定义以及维度集的集合。</span><span class="sxs-lookup"><span data-stu-id="f547d-116">For better reusability and sharing, you can create a building block group, which is a collection of existing report definitions, row definitions, column definitions, reporting tree definitions, and dimension sets that are associated with a company in.</span></span>

## <a name="building-blocks-of-a-report"></a><span data-ttu-id="f547d-117">报表的构建基块</span><span class="sxs-lookup"><span data-stu-id="f547d-117">Building blocks of a report</span></span>
| <span data-ttu-id="f547d-118">构建基块</span><span class="sxs-lookup"><span data-stu-id="f547d-118">Building block</span></span>            | <span data-ttu-id="f547d-119">说明</span><span class="sxs-lookup"><span data-stu-id="f547d-119">Description</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="f547d-120">有关详细信息</span><span class="sxs-lookup"><span data-stu-id="f547d-120">For more information</span></span>                                                                                                 |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f547d-121">行定义</span><span class="sxs-lookup"><span data-stu-id="f547d-121">Row definition</span></span>            | <span data-ttu-id="f547d-122">行定义定义报表上的描述性行（例如薪金或销售额）。</span><span class="sxs-lookup"><span data-stu-id="f547d-122">A row definition defines the descriptive lines (for example, salaries or sales) on a report.</span></span> <span data-ttu-id="f547d-123">它还列出了段值和每个行项中包含值的维度并且包含行格式设置和计算。</span><span class="sxs-lookup"><span data-stu-id="f547d-123">It also lists the segment values or dimensions that contain the values for each line item, and includes row formatting and calculations.</span></span>                                                    | [<span data-ttu-id="f547d-124">行定义</span><span class="sxs-lookup"><span data-stu-id="f547d-124">Row definitions</span></span>](row-definitions-financial-reporting.md)                       |
| <span data-ttu-id="f547d-125">列定义</span><span class="sxs-lookup"><span data-stu-id="f547d-125">Column definition</span></span>         | <span data-ttu-id="f547d-126">列定义定义从财务维度中提取数据时要使用的期间。</span><span class="sxs-lookup"><span data-stu-id="f547d-126">A column definition defines the period to use when data is extracted from the financial dimensions.</span></span> <span data-ttu-id="f547d-127">它还包含列格式设置和计算。</span><span class="sxs-lookup"><span data-stu-id="f547d-127">It also includes column formatting and calculations.</span></span>                                                                                                                                 | [<span data-ttu-id="f547d-128">列定义</span><span class="sxs-lookup"><span data-stu-id="f547d-128">Column definitions</span></span>](column-definitions-financial-reports.md)         |
| <span data-ttu-id="f547d-129">报告树定义</span><span class="sxs-lookup"><span data-stu-id="f547d-129">Reporting tree definition</span></span> | <span data-ttu-id="f547d-130">报告树定义类似于组织结构图。</span><span class="sxs-lookup"><span data-stu-id="f547d-130">A reporting tree definition resembles an organizational chart.</span></span> <span data-ttu-id="f547d-131">它包含单个报告单元，这些单元在图表中表示每个框。</span><span class="sxs-lookup"><span data-stu-id="f547d-131">It contains individual reporting units that represent each box in the chart.</span></span> <span data-ttu-id="f547d-132">这些单位可以是财务数据中的单个部门，也可以是汇总其他报告单位数据的较高级别的单位。</span><span class="sxs-lookup"><span data-stu-id="f547d-132">The units can be either individual departments from the financial data or higher-level units that summarize data from other reporting units.</span></span> | [<span data-ttu-id="f547d-133">报告树定义</span><span class="sxs-lookup"><span data-stu-id="f547d-133">Reporting tree definitions</span></span>](financial-reporting-tree-definitions.md) |
| <span data-ttu-id="f547d-134">报表定义</span><span class="sxs-lookup"><span data-stu-id="f547d-134">Report definition</span></span>         | <span data-ttu-id="f547d-135">报表定义使用行定义、列定义和可选报告树定义构建报表。</span><span class="sxs-lookup"><span data-stu-id="f547d-135">A report definition uses a row definition, a column definition, and an optional reporting tree definition to build a report.</span></span> <span data-ttu-id="f547d-136">它还提供了可以用于自定义报表的其他选项和设置。</span><span class="sxs-lookup"><span data-stu-id="f547d-136">It also provides additional options and settings that you can use to customize a report.</span></span>                                                                    | [<span data-ttu-id="f547d-137">报表定义</span><span class="sxs-lookup"><span data-stu-id="f547d-137">Report definition</span></span>](design-financial-report-definitions.md)                  |

<span data-ttu-id="f547d-138">如果您是初次设计报表，您可能需要使用报表向导来快速创建您可稍后自定义的报表定义。</span><span class="sxs-lookup"><span data-stu-id="f547d-138">If you're new to designing reports, you might find want to use the report wizard to quickly create a report definition that you can customize later.</span></span> <span data-ttu-id="f547d-139">如果您在设计报表方面有经验且希望报表设计具有更多灵活性，则可以组合新构建基块或现有构建基块来创建新的报表定义。</span><span class="sxs-lookup"><span data-stu-id="f547d-139">If you have experience with designing reports and want more flexibility for report design, you can combine new or existing building blocks to create a new report definition.</span></span> <span data-ttu-id="f547d-140">您不必完全了解所有可用的生成质量报表的报表定义选项。</span><span class="sxs-lookup"><span data-stu-id="f547d-140">You don't have to fully understand all the available report definition options to produce quality reports.</span></span> <span data-ttu-id="f547d-141">随着您逐渐了解设计报表，您就可以扩展报表定义以利用更多高级功能。</span><span class="sxs-lookup"><span data-stu-id="f547d-141">As you become familiar with designing reports, you can expand your report definitions to take advantage of more advanced features.</span></span> <span data-ttu-id="f547d-142">在创建了一个基本报表后，您可以自定义报表定义和该报表定义中的任何构建基块。</span><span class="sxs-lookup"><span data-stu-id="f547d-142">After you've created a basic report, you can customize the report definition and any of the building blocks in the report definition.</span></span>

## <a name="organize-the-building-blocks"></a><span data-ttu-id="f547d-143">组织构建基块</span><span class="sxs-lookup"><span data-stu-id="f547d-143">Organize the building blocks</span></span>
<span data-ttu-id="f547d-144">在报表设计器中使用文件夹组织您的构建基块。</span><span class="sxs-lookup"><span data-stu-id="f547d-144">Use folders to organize your building blocks in Report Designer.</span></span> <span data-ttu-id="f547d-145">所有文件夹特定于其包含的构建基块的类型。</span><span class="sxs-lookup"><span data-stu-id="f547d-145">All folders are specific to the type of building block that they contain.</span></span> <span data-ttu-id="f547d-146">例如，包含行定义的所有文件夹位于报表设计器的**行定义**窗格中。</span><span class="sxs-lookup"><span data-stu-id="f547d-146">For example, all folders that contain row definitions are located in the **Row Definitions** pane in Report Designer.</span></span>

### <a name="create-a-folder"></a><span data-ttu-id="f547d-147">创建文件夹</span><span class="sxs-lookup"><span data-stu-id="f547d-147">Create a folder</span></span>

1.  <span data-ttu-id="f547d-148">在报表设计器中，选择要在导航窗格中组织的构建基块的类型。</span><span class="sxs-lookup"><span data-stu-id="f547d-148">In Report Designer, select the type of building block to organize in the navigation pane.</span></span> <span data-ttu-id="f547d-149">登录，要对行定义进行排序，请单击**“行定义”**。</span><span class="sxs-lookup"><span data-stu-id="f547d-149">For example, to sort a row definition, click **Row Definitions**.</span></span>
2.  <span data-ttu-id="f547d-150">在导航窗格中，选择将在其下创建新文件夹的现有文件夹，然后完成以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="f547d-150">In the navigation pane, select the existing folder to create the new folder under, and then follow one of these steps:</span></span>
    -   <span data-ttu-id="f547d-151">右键单击父文件夹，然后单击**新建文件夹**。</span><span class="sxs-lookup"><span data-stu-id="f547d-151">Right-click the parent folder, and then click **New Folder**.</span></span>
    -   <span data-ttu-id="f547d-152">选择父文件夹，单击**文件**，然后选单击**新建文件夹**。</span><span class="sxs-lookup"><span data-stu-id="f547d-152">Select the parent folder, click **File**, and then click **New Folder**.</span></span>

3.  <span data-ttu-id="f547d-153">当新文件夹显示时，输入新文件夹的名称，然后按 Enter。</span><span class="sxs-lookup"><span data-stu-id="f547d-153">When the new folder appears, enter the name of the new folder, and then press Enter.</span></span>

## <a name="lock-a-building-block"></a><span data-ttu-id="f547d-154">锁定构建基块</span><span class="sxs-lookup"><span data-stu-id="f547d-154">Lock a building block</span></span>
<span data-ttu-id="f547d-155">您可以创建密码来锁定和帮助保护构建基块。</span><span class="sxs-lookup"><span data-stu-id="f547d-155">You can create a password to lock and help protect a building block.</span></span> <span data-ttu-id="f547d-156">通过这种方法，可向一个报表组件添加一层安全性，而不确保整个系统安全。</span><span class="sxs-lookup"><span data-stu-id="f547d-156">In this way you can add a level of security to a report component without securing the whole system.</span></span> <span data-ttu-id="f547d-157">密码可帮助保护构建基块信息，此信息对于您的月底报告流程非常重要。</span><span class="sxs-lookup"><span data-stu-id="f547d-157">A password can help protect building block information that is important to your month-end reporting process.</span></span> <span data-ttu-id="f547d-158">任何角色的用户均可以锁定构建基块。</span><span class="sxs-lookup"><span data-stu-id="f547d-158">A user in any role can lock a building block.</span></span> <span data-ttu-id="f547d-159">但是，其他用户始终具有访问锁定组件的只读访问权限。</span><span class="sxs-lookup"><span data-stu-id="f547d-159">However, other users always have read-only access to a locked component.</span></span> <span data-ttu-id="f547d-160">用户可以打开、更改并保存新名称下锁定的组件。</span><span class="sxs-lookup"><span data-stu-id="f547d-160">Users can open, change, and save the locked component under a new name.</span></span> <span data-ttu-id="f547d-161">具有管理员角色的用户可以始终访问和更改锁定的构建基块。</span><span class="sxs-lookup"><span data-stu-id="f547d-161">A user who has the role of administrator can always access and change a locked building block.</span></span>
1.  <span data-ttu-id="f547d-162">在报表设计器中，打开要锁定的报表组件，例如行定义、列定义、报表定义或报告树定义。</span><span class="sxs-lookup"><span data-stu-id="f547d-162">In Report Designer, open the report component to lock, such as a row definition, column definition, report definition, or reporting tree definition.</span></span>
2.  <span data-ttu-id="f547d-163">在**工具**菜单上，单击**保护/取消保护**。</span><span class="sxs-lookup"><span data-stu-id="f547d-163">On the **Tools** menu, click **Protect/Unprotect**.</span></span> <span data-ttu-id="f547d-164">您还可以单击工具栏中的**保护/取消保护**（锁定图标）。</span><span class="sxs-lookup"><span data-stu-id="f547d-164">You can also click **Protect/Unprotect** (the lock icon) on the toolbar.</span></span>
3.  <span data-ttu-id="f547d-165">在**保护**对话框中，输入并确认密码，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="f547d-165">In the **Protect** dialog box, enter and confirm a password, and then click **OK**.</span></span> <span data-ttu-id="f547d-166">工具栏中的锁定图标在锁定打开的构建基块时突出显示。</span><span class="sxs-lookup"><span data-stu-id="f547d-166">The lock icon on the toolbar is highlighted when an open building block is locked.</span></span>

<span data-ttu-id="f547d-167">要解锁锁定的构建基块，请打开该构建基块，然后单击工具栏上的**保护/取消保护**。</span><span class="sxs-lookup"><span data-stu-id="f547d-167">To unlock a locked building block, open the building block, and then click **Protect/Unprotect** on the toolbar.</span></span> <span data-ttu-id="f547d-168">或者，在**工具**菜单上，单击**取消保护**。</span><span class="sxs-lookup"><span data-stu-id="f547d-168">Alternatively, on the **Tools** menu, click **Unprotect**.</span></span>

## <a name="building-block-groups"></a><span data-ttu-id="f547d-169">构建基块组</span><span class="sxs-lookup"><span data-stu-id="f547d-169">Building block groups</span></span>

<span data-ttu-id="f547d-170">构建基块是您为报表创建的行定义、列定义、报告树定义和报表定义。</span><span class="sxs-lookup"><span data-stu-id="f547d-170">Building blocks are the row definitions, column definitions, reporting tree definitions, and report definitions that you create for a report.</span></span> <span data-ttu-id="f547d-171">构建基块组是与公司关联的定义和维度的集合。</span><span class="sxs-lookup"><span data-stu-id="f547d-171">Building block groups are collections of the definitions and dimension sets that are associated with a company.</span></span> <span data-ttu-id="f547d-172">构建基块组可特定于公司，或者多个公司可共享相同的一组构建基块。</span><span class="sxs-lookup"><span data-stu-id="f547d-172">Building block groups can be company-specific, or several companies can share the same set of building blocks.</span></span> <span data-ttu-id="f547d-173">如果您的有些公司拥有具有不同会计科目表，则可能需要针对每个公司使用不同的构建基块组。</span><span class="sxs-lookup"><span data-stu-id="f547d-173">If some of your companies have a different chart of accounts, you might want to use a different building block group for each company.</span></span> <span data-ttu-id="f547d-174">或者，您可能需要对所有单独的构建基块进行命名以反映与其兼容的公司。</span><span class="sxs-lookup"><span data-stu-id="f547d-174">Alternatively, you might want to name all your individual building blocks to reflect the company that they are compatible with.</span></span>
### <a name="create-a-building-block-group"></a><span data-ttu-id="f547d-175">创建构建基块组</span><span class="sxs-lookup"><span data-stu-id="f547d-175">Create a building block group</span></span>

1.  <span data-ttu-id="f547d-176">在报表设计器中，在**公司**菜单上，单击**构建基块组**。</span><span class="sxs-lookup"><span data-stu-id="f547d-176">In Report Designer, on the **Company** menu, click **Building block groups**.</span></span>
2.  <span data-ttu-id="f547d-177">在“构建基块组”****对话框中，单击“新建”****。</span><span class="sxs-lookup"><span data-stu-id="f547d-177">In the **Building block groups** dialog box, click **New**.</span></span>
3.  <span data-ttu-id="f547d-178">为构建基块组输入唯一名称和描述。</span><span class="sxs-lookup"><span data-stu-id="f547d-178">Enter a unique name and description for the building block group.</span></span> <span data-ttu-id="f547d-179">每个字段最多可以包含 256 个字符。</span><span class="sxs-lookup"><span data-stu-id="f547d-179">Each field can contain a maximum of 256 characters.</span></span> <span data-ttu-id="f547d-180">（此数字包括空格）。</span><span class="sxs-lookup"><span data-stu-id="f547d-180">(This number includes spaces.)</span></span>
4.  <span data-ttu-id="f547d-181">单击**确定**以创建新的构建基块组。</span><span class="sxs-lookup"><span data-stu-id="f547d-181">Click **OK** to create the new building block group.</span></span>

### <a name="assign-a-building-block-group"></a><span data-ttu-id="f547d-182">分配构建基块组</span><span class="sxs-lookup"><span data-stu-id="f547d-182">Assign a building block group</span></span>

<span data-ttu-id="f547d-183">创建块组后，您必须将其分配到至少一个公司。</span><span class="sxs-lookup"><span data-stu-id="f547d-183">After you a create block group, you must assign it to at least one company.</span></span> <span data-ttu-id="f547d-184">然后，您可以创建报表、行、列和报告树定义并将它们保存在构建基块组中。</span><span class="sxs-lookup"><span data-stu-id="f547d-184">You can then create report, row, column, and reporting tree definitions, and save them in the building block group.</span></span> <span data-ttu-id="f547d-185">在启动以下程序之前，您必须关闭所有构建基块。</span><span class="sxs-lookup"><span data-stu-id="f547d-185">You must close all building blocks before you start the following procedure.</span></span>
1.  <span data-ttu-id="f547d-186">在报表设计器的**“公司”**菜单上，单击**“公司”**。</span><span class="sxs-lookup"><span data-stu-id="f547d-186">In Report Designer, on the **Company** menu, click **Companies**.</span></span>
2.  <span data-ttu-id="f547d-187">在“公司”****对话框中，选择要向其分配构建基块组的公司。</span><span class="sxs-lookup"><span data-stu-id="f547d-187">In the **Companies** dialog box, select the company to assign a building block group to.</span></span>
3.  <span data-ttu-id="f547d-188">单击“修改”****。</span><span class="sxs-lookup"><span data-stu-id="f547d-188">Click **Modify**.</span></span>
4.  <span data-ttu-id="f547d-189">在**“修改公司”**对话框中的**“构建基块组”**字段中，选择要分配到公司的构建基块组，或者单击**“新建”**以创建新的构建基块组。</span><span class="sxs-lookup"><span data-stu-id="f547d-189">In the **Modify Company** dialog box, in the **Building block group** field, select the building block group to assign to the company, or click **New** to create a new building block group.</span></span>
5.  <span data-ttu-id="f547d-190">单击**“确定”**以分配构建基块组。</span><span class="sxs-lookup"><span data-stu-id="f547d-190">Click **OK** to assign the building block group.</span></span>
6.  <span data-ttu-id="f547d-191">单击**关闭**以关闭**公司**对话框。</span><span class="sxs-lookup"><span data-stu-id="f547d-191">Click **Close** to close the **Companies** dialog box.</span></span> <span data-ttu-id="f547d-192">您选择的构建基块组现已分配到该公司。</span><span class="sxs-lookup"><span data-stu-id="f547d-192">The building block group that you selected is now assigned to the company.</span></span> <span data-ttu-id="f547d-193">现在，所有将创建的新行定义、列定义等将成为分配到此公司的构建基块组的一部分。</span><span class="sxs-lookup"><span data-stu-id="f547d-193">Now, all new row definitions, column definitions, and so on, that are created will be part of the building block group that is assigned to this company.</span></span> <span data-ttu-id="f547d-194">您还可以从其他系统中导入 .tdbx 文件或报表。</span><span class="sxs-lookup"><span data-stu-id="f547d-194">You can also import a .tdbx file or report from another system.</span></span>

### <a name="view-a-building-block-group"></a><span data-ttu-id="f547d-195">查看构建基块组</span><span class="sxs-lookup"><span data-stu-id="f547d-195">View a building block group</span></span>

<span data-ttu-id="f547d-196">构建基块组已创建并使用后，您可以查看分配给它的所有构建基块。</span><span class="sxs-lookup"><span data-stu-id="f547d-196">After a building block group has been created and is being used, you can view all the building blocks that are assigned to it.</span></span> <span data-ttu-id="f547d-197">此外可以导出或导入构建基块组，并对构建基块组执行额外的维护。</span><span class="sxs-lookup"><span data-stu-id="f547d-197">You can also export or import a building block group, and perform additional maintenance on building block groups.</span></span>
1.  <span data-ttu-id="f547d-198">在报表设计器中，在**“公司”**菜单上，单击**“构建基块组”**。</span><span class="sxs-lookup"><span data-stu-id="f547d-198">In Report Designer, on the **Company** menu, click **Building Block Groups**.</span></span>
2.  <span data-ttu-id="f547d-199">在**“构建基块组”**对话框中，选择要查看的构建基块。</span><span class="sxs-lookup"><span data-stu-id="f547d-199">In the **Building Block Groups** dialog box, select the building block to view.</span></span>
3.  <span data-ttu-id="f547d-200">单击**查看**以打开**查看构建基块组**对话框，您或以在其中查看构建基块组的内容。</span><span class="sxs-lookup"><span data-stu-id="f547d-200">Click **View** to open the **View Building Block Group** dialog box, where you can view the contents of the building block group.</span></span>
4.  <span data-ttu-id="f547d-201">单击**“关闭”**以关闭此对话框。</span><span class="sxs-lookup"><span data-stu-id="f547d-201">Click **Close** to close the dialog boxes.</span></span>

### <a name="save-a-building-block-group-under-a-new-name"></a><span data-ttu-id="f547d-202">在新名称下保存构建基块组</span><span class="sxs-lookup"><span data-stu-id="f547d-202">Save a building block group under a new name</span></span>

<span data-ttu-id="f547d-203">您可以在新名称下保存现有构建基块组。</span><span class="sxs-lookup"><span data-stu-id="f547d-203">You can save an existing building block group under a new name.</span></span> <span data-ttu-id="f547d-204">然后，可以修改新的构建基块组，无需更改原始构建基块组。</span><span class="sxs-lookup"><span data-stu-id="f547d-204">You can then modify the new building block group without changing the original building block group.</span></span>
1.  <span data-ttu-id="f547d-205">在报表设计器中的“公司”****菜单上，单击“构建基块组”****。</span><span class="sxs-lookup"><span data-stu-id="f547d-205">In Report Designer, on the **Company** menu, click **Building Block Groups**.</span></span>
2.  <span data-ttu-id="f547d-206">在**构建基块组**对话框中，选择要在新名称下保存的构建基块组。</span><span class="sxs-lookup"><span data-stu-id="f547d-206">In the **Building Block Groups** dialog box, select the building block group to save under a new name.</span></span>
3.  <span data-ttu-id="f547d-207">单击**“另存为”**。</span><span class="sxs-lookup"><span data-stu-id="f547d-207">Click **Save As**.</span></span>
4.  <span data-ttu-id="f547d-208">为构建基块组输入新的名称和描述。</span><span class="sxs-lookup"><span data-stu-id="f547d-208">Enter a new name and description for the building block group.</span></span>
5.  <span data-ttu-id="f547d-209">单击“**OK**”。</span><span class="sxs-lookup"><span data-stu-id="f547d-209">Click **OK**.</span></span> <span data-ttu-id="f547d-210">新的构建基块组会显示在**“构建基块组”**对话框中。</span><span class="sxs-lookup"><span data-stu-id="f547d-210">The new building block group appears in the **Building Block Groups** dialog box.</span></span>

### <a name="export-a-building-block-group"></a><span data-ttu-id="f547d-211"> 导出构建基块组</span><span class="sxs-lookup"><span data-stu-id="f547d-211">Export a building block group</span></span>

<span data-ttu-id="f547d-212">您可以导出构建基块组或构建基块组中的特定报表构建基块。</span><span class="sxs-lookup"><span data-stu-id="f547d-212">You can export a building block group or specific report building blocks in a building block group.</span></span> <span data-ttu-id="f547d-213">您可以将导出的构建基块组用作备份。</span><span class="sxs-lookup"><span data-stu-id="f547d-213">You can use the exported building block group as a backup.</span></span> <span data-ttu-id="f547d-214">您还可以复制构建基块组或 Finance and Operations 安装之间的导出数据。</span><span class="sxs-lookup"><span data-stu-id="f547d-214">You can also copy the exported data between building block groups or Finance and Operations installations.</span></span> <span data-ttu-id="f547d-215">报表设计器包括引用的字体样式和维度集以及构建基块组。</span><span class="sxs-lookup"><span data-stu-id="f547d-215">Report designer includes the referenced font styles and dimension sets together with the building block group.</span></span>
1.  <span data-ttu-id="f547d-216">在报表设计器中，在**“公司”**菜单上，单击**“构建基块组”**。</span><span class="sxs-lookup"><span data-stu-id="f547d-216">In Report Designer, on the **Company** menu, click **Building Block Groups**.</span></span>
2.  <span data-ttu-id="f547d-217">在“构建基块组”****对话框中，选择要导出的构建基块组，然后单击“导出”****。</span><span class="sxs-lookup"><span data-stu-id="f547d-217">In the **Building Block Groups** dialog box, select the building block group to export, and then click **Export**.</span></span>
3.  <span data-ttu-id="f547d-218">在**“导出”**对话框中，选择要导出的报表定义：</span><span class="sxs-lookup"><span data-stu-id="f547d-218">In the **Export** dialog box, select the report definitions to export:</span></span>
    -   <span data-ttu-id="f547d-219">要导出您的所有报表定义和关联的构建基块，请单击**“全选”**。</span><span class="sxs-lookup"><span data-stu-id="f547d-219">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="f547d-220">要导出特定报表、行、列、树或维度集，请单击相应选项卡，然后选择要导出的项。</span><span class="sxs-lookup"><span data-stu-id="f547d-220">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="f547d-221">按住 Ctrl 键选择选项卡上的多个项目。**注意：**当您选择要导出的报表时，系统将选择关联的行、列、树和维度集。</span><span class="sxs-lookup"><span data-stu-id="f547d-221">Press and hold the Ctrl key to select multiple items on a tab. **Note:** When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="f547d-222">在已完成选择要导出的项后，请单击**导出**。</span><span class="sxs-lookup"><span data-stu-id="f547d-222">When you've finished selecting items to export, click **Export**.</span></span>
5.  <span data-ttu-id="f547d-223">在**“另存为”**对话框中，选择要将构建基块组导出到的位置。</span><span class="sxs-lookup"><span data-stu-id="f547d-223">In the **Save As** dialog box, select a location to export the building block group to.</span></span>
6.  <span data-ttu-id="f547d-224">在**“文件名称”**字段中，输入该文件的名称。</span><span class="sxs-lookup"><span data-stu-id="f547d-224">In the **File Name** field, enter a name for the file.</span></span> <span data-ttu-id="f547d-225">报表设计器会自动添加一个 .tdbx 文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="f547d-225">Report designer automatically adds a .tdbx file name extension.</span></span>
7.  <span data-ttu-id="f547d-226">单击“**保存**”。</span><span class="sxs-lookup"><span data-stu-id="f547d-226">Click **Save**.</span></span> <span data-ttu-id="f547d-227">构建基块组将保存到指定的位置。</span><span class="sxs-lookup"><span data-stu-id="f547d-227">The building block group is saved to the location that you specified.</span></span>

### <a name="import-a-building-block-group"></a><span data-ttu-id="f547d-228"> 导入构建基块组</span><span class="sxs-lookup"><span data-stu-id="f547d-228">Import a building block group</span></span>

<span data-ttu-id="f547d-229">您可以将构建基块组导入现有的构建基块组，或者您可以为数据创建新的构建基块组。</span><span class="sxs-lookup"><span data-stu-id="f547d-229">You can import a building block group into an existing building block group, or you can create a new building block group for the data.</span></span> <span data-ttu-id="f547d-230">所有导入的构建基块组保留其原始字体样式和公司引用，并包含相关维度集。</span><span class="sxs-lookup"><span data-stu-id="f547d-230">All imported building block groups retain their original font styles and company references, and include the relevant dimension sets.</span></span>
1.  <span data-ttu-id="f547d-231">在报表设计器中，在**“公司”**菜单上，单击**“构建基块组”**。</span><span class="sxs-lookup"><span data-stu-id="f547d-231">In Report Designer, on the **Company** menu, click **Building Block Groups**.</span></span>
2.  <span data-ttu-id="f547d-232">在“构建基块组”****对话框中，选择要将构建基块组导入到的构建基块，然后单击“导入”****。</span><span class="sxs-lookup"><span data-stu-id="f547d-232">In the **Building Block Groups** dialog box, select the building block to import a building block group into, and then click **Import**.</span></span>
3.  <span data-ttu-id="f547d-233">在“打开”****对话框中，选择要导入的构建基块组，然后单击“打开”****。</span><span class="sxs-lookup"><span data-stu-id="f547d-233">In the **Open** dialog box, select the building block group to import, and then click **Open**.</span></span>
4.  <span data-ttu-id="f547d-234">在**“导入”**对话框中，选择要导入的报表定义：</span><span class="sxs-lookup"><span data-stu-id="f547d-234">In the **Import** dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="f547d-235">要导入所有报表定义和支持构建基块，请单击**全选**。</span><span class="sxs-lookup"><span data-stu-id="f547d-235">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="f547d-236">要导入特定报表、行、列、树或维度集，请选择要导入的报表、行、列、树或维度集。</span><span class="sxs-lookup"><span data-stu-id="f547d-236">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

5.  <span data-ttu-id="f547d-237">在已完成选择要导入的项后，请单击**导入**。</span><span class="sxs-lookup"><span data-stu-id="f547d-237">When you've finished selecting items to import, click **Import**.</span></span>

### <a name="undo-a-checkout-of-a-building-block"></a><span data-ttu-id="f547d-238">撤消构建基块的签出</span><span class="sxs-lookup"><span data-stu-id="f547d-238">Undo a checkout of a building block</span></span>

<span data-ttu-id="f547d-239">当打开一个构建基块时，其他用户可以以只读模式访问该构建基块。</span><span class="sxs-lookup"><span data-stu-id="f547d-239">When you open a building block, other users have read-only access that building block.</span></span> <span data-ttu-id="f547d-240">有时，用户会忘记关闭构建基块或在没有关闭构建基块的情况下关闭其系统。</span><span class="sxs-lookup"><span data-stu-id="f547d-240">Sometimes, users forget to close a building block, or they shut down their system without closing the building block.</span></span> <span data-ttu-id="f547d-241">因此，要仍然签出构建基块，这样其他用户就无法打开它。</span><span class="sxs-lookup"><span data-stu-id="f547d-241">Therefore, the building block remains checked out, and no other users can open it.</span></span> <span data-ttu-id="f547d-242">在这类情况下，财务报告管理员可以使用**已签出的项目**对话框签入用户将其留为已签出状态的构建基块。**注意：**您必须具有管理员角色才能使用**已签出的项目**对话框签入构建基块。</span><span class="sxs-lookup"><span data-stu-id="f547d-242">In these situations, a financial reporting administrator can use the **Checked Out Items** dialog box to check in building blocks that users have left checked out. **Note:** You must have the role of administrator to check in building blocks by using the **Checked Out Items** dialog box.</span></span>
1.  <span data-ttu-id="f547d-243">在报表设计器中，在**“工具”**菜单上，单击**“已签出项”**。</span><span class="sxs-lookup"><span data-stu-id="f547d-243">In Report Designer, on the **Tools** menu, click **Checked Out Items**.</span></span>
2.  <span data-ttu-id="f547d-244">在“已签出的项目”****对话框中，选中“显示来自所有用户的项目”****。</span><span class="sxs-lookup"><span data-stu-id="f547d-244">In the **Checked Out Items** dialog box, select **Show items from all users**.</span></span> <span data-ttu-id="f547d-245">该列表将更新为显示所有签出的构建基块，以及签出这些构建基块的用户。</span><span class="sxs-lookup"><span data-stu-id="f547d-245">The list is updated to display all building blocks that are checked out and the users who have checked them out.</span></span>
3.  <span data-ttu-id="f547d-246">选择构建基块，然后单击**“撤消签出”**。</span><span class="sxs-lookup"><span data-stu-id="f547d-246">Select a building block, and then click **Undo Checkout**.</span></span>
4.  <span data-ttu-id="f547d-247">单击**“是”**以签入构建基块。</span><span class="sxs-lookup"><span data-stu-id="f547d-247">Click **Yes** to check in the building block.</span></span>

# <a name="see-also"></a><span data-ttu-id="f547d-248">请参阅</span><span class="sxs-lookup"><span data-stu-id="f547d-248">See also</span></span>

[<span data-ttu-id="f547d-249">财务申报</span><span class="sxs-lookup"><span data-stu-id="f547d-249">Financial reporting</span></span>](financial-reporting-intro.md)




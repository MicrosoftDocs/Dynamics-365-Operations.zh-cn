---
title: "财务报表设计器中的行定义"
description: "行定义是报表组件或构建基块，在财务报表上指定每一行的内容。 可将行定义与列定义、报告结构树定义和报表定义组合以创建可由多个公司使用的构建基块组。"
author: aprilolson
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
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ea1386bc06c0e91a2d1f23dd05794ca6ff99106a
ms.contentlocale: zh-cn
ms.lasthandoff: 08/08/2018

---

# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="557f9-104">财务报表设计器中的行定义</span><span class="sxs-lookup"><span data-stu-id="557f9-104">Row definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="557f9-105">行定义是报表组件或构建基块，在财务报表上指定每一行的内容。</span><span class="sxs-lookup"><span data-stu-id="557f9-105">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="557f9-106">可将行定义与列定义、报告结构树定义和报表定义组合以创建可由多个公司使用的构建基块组。</span><span class="sxs-lookup"><span data-stu-id="557f9-106">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

<a name="create-a-row-definition"></a><span data-ttu-id="557f9-107">创建行定义</span><span class="sxs-lookup"><span data-stu-id="557f9-107">Create a row definition</span></span>
-----------------------

1.  <span data-ttu-id="557f9-108">在报表设计器的导航窗格中，单击**行定义**。</span><span class="sxs-lookup"><span data-stu-id="557f9-108">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2.  <span data-ttu-id="557f9-109">在**文件**菜单上，单击**新建**，然后单击**行定义**。</span><span class="sxs-lookup"><span data-stu-id="557f9-109">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="557f9-110">有关每个单元格内容的详细信息，请参阅[修改行定义单元格](modify-row-definition-cells-financial-reporting.md)。</span><span class="sxs-lookup"><span data-stu-id="557f9-110">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="557f9-111">打开行定义</span><span class="sxs-lookup"><span data-stu-id="557f9-111">Open a row definition</span></span>
1.  <span data-ttu-id="557f9-112">在报表设计器的导航窗格中，单击**行定义**。</span><span class="sxs-lookup"><span data-stu-id="557f9-112">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2.  <span data-ttu-id="557f9-113">双击要打开的行定义的名称。</span><span class="sxs-lookup"><span data-stu-id="557f9-113">Double-click the name of the row definition to open.</span></span>
3.  <span data-ttu-id="557f9-114">要查看与行定义关联的任何构建基块，请右键单击行定义，然后选择**关联**。</span><span class="sxs-lookup"><span data-stu-id="557f9-114">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="557f9-115"> 行定义的内容</span><span class="sxs-lookup"><span data-stu-id="557f9-115">Contents of a row definition</span></span>
<span data-ttu-id="557f9-116">行定义最多可以包含 20,000 个财务维度行并且可以包含以下信息：</span><span class="sxs-lookup"><span data-stu-id="557f9-116">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

-   <span data-ttu-id="557f9-117">通过创建节标题、行和空格为报表添加意义的描述性文本，如**现金**或**总收入**</span><span class="sxs-lookup"><span data-stu-id="557f9-117">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
-   <span data-ttu-id="557f9-118">财务数据的链接，可以在 Microsoft Dynamics 365 for Finance and Operations 中包含维度值**注意：** 您可设置行定义以在每次生成报表时从财务维度系统中拉取数据。</span><span class="sxs-lookup"><span data-stu-id="557f9-118">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 for Finance and Operations **Note:** You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>
-   <span data-ttu-id="557f9-119">基于链接的财务数据的行汇总和公式</span><span class="sxs-lookup"><span data-stu-id="557f9-119">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="557f9-120">通常，行定义中的每个行包含下列类型的信息：</span><span class="sxs-lookup"><span data-stu-id="557f9-120">Usually, each row in a row definition contains one of the following types of information:</span></span>

-   <span data-ttu-id="557f9-121">对财务维度系统的引用</span><span class="sxs-lookup"><span data-stu-id="557f9-121">References to the financial dimensions system</span></span>
-   <span data-ttu-id="557f9-122">基于数据的汇总或计算</span><span class="sxs-lookup"><span data-stu-id="557f9-122">Totals or calculations that are based on the data</span></span>
-   <span data-ttu-id="557f9-123">格式设置</span><span class="sxs-lookup"><span data-stu-id="557f9-123">Formatting</span></span>

<span data-ttu-id="557f9-124">有两种方法可以在行定义中输入信息︰</span><span class="sxs-lookup"><span data-stu-id="557f9-124">There are two methods for entering information in a row definition:</span></span>

-   <span data-ttu-id="557f9-125">在新行定义中手动输入行信息。</span><span class="sxs-lookup"><span data-stu-id="557f9-125">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="557f9-126">有关详细信息，请参阅[修改行定义单元格](modify-row-definition-cells-financial-reporting.md)。</span><span class="sxs-lookup"><span data-stu-id="557f9-126">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
-   <span data-ttu-id="557f9-127">使用报表设计器可以直接从财务维度拉取行信息。</span><span class="sxs-lookup"><span data-stu-id="557f9-127">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="557f9-128">有关详细信息，请参阅[修改行定义单元格](modify-row-definition-cells-financial-reporting.md)中的“相关/行/单位”部分。</span><span class="sxs-lookup"><span data-stu-id="557f9-128">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="557f9-129"> 在行定义中添加维度</span><span class="sxs-lookup"><span data-stu-id="557f9-129">Add dimensions in a row definition</span></span>
<span data-ttu-id="557f9-130">维度是数据和值的交集。</span><span class="sxs-lookup"><span data-stu-id="557f9-130">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="557f9-131">可在报表设计器中对数据和值进行分组。</span><span class="sxs-lookup"><span data-stu-id="557f9-131">You can group data and values in report designer.</span></span> <span data-ttu-id="557f9-132">然后可以进一步分类和分析交易记录。</span><span class="sxs-lookup"><span data-stu-id="557f9-132">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="557f9-133">您可使用**从维度插入行**对话框同时向行定义添加多个行。</span><span class="sxs-lookup"><span data-stu-id="557f9-133">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="557f9-134">此对话框将针对每个维度显示一列。</span><span class="sxs-lookup"><span data-stu-id="557f9-134">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="557f9-135">下表描述了您可以为每个维度指定的信息。</span><span class="sxs-lookup"><span data-stu-id="557f9-135">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="557f9-136">选项</span><span class="sxs-lookup"><span data-stu-id="557f9-136">Option</span></span>                | <span data-ttu-id="557f9-137">说明</span><span class="sxs-lookup"><span data-stu-id="557f9-137">Description</span></span>                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="557f9-138">维度</span><span class="sxs-lookup"><span data-stu-id="557f9-138">Dimension</span></span>             | <span data-ttu-id="557f9-139">标识要添加到行定义的维度的模式。</span><span class="sxs-lookup"><span data-stu-id="557f9-139">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="557f9-140">此模式在维度的每个位置包含一个与号 (\#) 或数字符号 (#)。</span><span class="sxs-lookup"><span data-stu-id="557f9-140">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="557f9-141">通常，对“主科目”维度使用所有与号，对其他维度使用所有数字符号。</span><span class="sxs-lookup"><span data-stu-id="557f9-141">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="557f9-142">维度范围起始值</span><span class="sxs-lookup"><span data-stu-id="557f9-142">Dimension Range Start</span></span> | <span data-ttu-id="557f9-143">要添加到行定义中的此维度的第一个值。</span><span class="sxs-lookup"><span data-stu-id="557f9-143">The first value for this dimension to add to the row definition.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="557f9-144">维度范围结束值</span><span class="sxs-lookup"><span data-stu-id="557f9-144">Dimension Range End</span></span>   | <span data-ttu-id="557f9-145">要添加到行定义的此维度的最后一个值。</span><span class="sxs-lookup"><span data-stu-id="557f9-145">The last value for this dimension to add to the row definition.</span></span>                                                                                                                                                                                                                  |

<span data-ttu-id="557f9-146">要向行定义添加维度，请完成下列步骤。</span><span class="sxs-lookup"><span data-stu-id="557f9-146">To add dimensions to a row definition, follow these steps.</span></span>

1.  <span data-ttu-id="557f9-147">在报表设计器中，单击**行定义**，然后打开行定义以修改。</span><span class="sxs-lookup"><span data-stu-id="557f9-147">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2.  <span data-ttu-id="557f9-148">在**编辑**菜单上，单击**从维度插入行**。</span><span class="sxs-lookup"><span data-stu-id="557f9-148">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3.  <span data-ttu-id="557f9-149">在**从维度插入行**对话框的**维度**行中，选择要转移到行定义的维度所在的单元格，然后单击**所有 &&&**。</span><span class="sxs-lookup"><span data-stu-id="557f9-149">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4.  <span data-ttu-id="557f9-150">要将行定义限制到特定维度值范围，请在**维度范围起始值**单元格中输入起始维度值，然后在**维度范围结束值**单元格中输入结束维度值。</span><span class="sxs-lookup"><span data-stu-id="557f9-150">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="557f9-151">要包括所选维度的所有值，请将这些单元格保留为空。</span><span class="sxs-lookup"><span data-stu-id="557f9-151">To include all values for the selected dimension, leave these cells empty.</span></span> <span data-ttu-id="557f9-152">**注意：** 维度范围中的通配符（\* 或 ?）可能不会返回您想要的结果，具体取决于 ERP 数据库整理数据的方式。</span><span class="sxs-lookup"><span data-stu-id="557f9-152">**Note:** Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>
5.  <span data-ttu-id="557f9-153">在**起始行代码**字段中指定要添加到行定义的第一个维度值的行代码。</span><span class="sxs-lookup"><span data-stu-id="557f9-153">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6.  <span data-ttu-id="557f9-154">在**每行的增量**字段中指定连续的行代码之间的间距。</span><span class="sxs-lookup"><span data-stu-id="557f9-154">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="557f9-155">例如，如果第一个行代码为 100，而增量值为 30，则第一批新的行具有代码 100、130、160、190 和 220。</span><span class="sxs-lookup"><span data-stu-id="557f9-155">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="557f9-156">使用为插入新的格式和公式行提供足够空间的增量值。</span><span class="sxs-lookup"><span data-stu-id="557f9-156">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7.  <span data-ttu-id="557f9-157">单击**OK**。</span><span class="sxs-lookup"><span data-stu-id="557f9-157">Click **OK**.</span></span> <span data-ttu-id="557f9-158">对于每个选定维度值，向行定义添加一行。</span><span class="sxs-lookup"><span data-stu-id="557f9-158">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="557f9-159"> 在行定义中调整运行化整</span><span class="sxs-lookup"><span data-stu-id="557f9-159">Adjust rounding in a row definition</span></span>
<span data-ttu-id="557f9-160">当您具有金额已化整的资产负债表时，总额可能不均衡。</span><span class="sxs-lookup"><span data-stu-id="557f9-160">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="557f9-161">例如，如果使用资产负债表报表中的舍入选项，同时报表定义也指定舍入。</span><span class="sxs-lookup"><span data-stu-id="557f9-161">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="557f9-162">您可以使用行定义中的**舍入调整**选项以平衡资产负债表中的金额。</span><span class="sxs-lookup"><span data-stu-id="557f9-162">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="557f9-163">您可以关闭舍入，或在报表定义的**设置**选项卡上进行修改。</span><span class="sxs-lookup"><span data-stu-id="557f9-163">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="557f9-164">下表显示如何化整金额。</span><span class="sxs-lookup"><span data-stu-id="557f9-164">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="557f9-165">在此表中，第 100 行和第 200 行的汇总在启用化整的情况下不同。</span><span class="sxs-lookup"><span data-stu-id="557f9-165">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="557f9-166">行代码</span><span class="sxs-lookup"><span data-stu-id="557f9-166">Row code</span></span> | <span data-ttu-id="557f9-167">未化整的金额</span><span class="sxs-lookup"><span data-stu-id="557f9-167">Amounts without rounding</span></span> | <span data-ttu-id="557f9-168">化整到千分位的金额</span><span class="sxs-lookup"><span data-stu-id="557f9-168">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="557f9-169">100</span><span class="sxs-lookup"><span data-stu-id="557f9-169">100</span></span>      | <span data-ttu-id="557f9-170">3,600</span><span class="sxs-lookup"><span data-stu-id="557f9-170">3,600</span></span>                    | <span data-ttu-id="557f9-171">4</span><span class="sxs-lookup"><span data-stu-id="557f9-171">4</span></span>                                       |
| <span data-ttu-id="557f9-172">200</span><span class="sxs-lookup"><span data-stu-id="557f9-172">200</span></span>      | <span data-ttu-id="557f9-173">3,700</span><span class="sxs-lookup"><span data-stu-id="557f9-173">3,700</span></span>                    | <span data-ttu-id="557f9-174">4</span><span class="sxs-lookup"><span data-stu-id="557f9-174">4</span></span>                                       |
| <span data-ttu-id="557f9-175">总计</span><span class="sxs-lookup"><span data-stu-id="557f9-175">Total</span></span>    | <span data-ttu-id="557f9-176">7,300</span><span class="sxs-lookup"><span data-stu-id="557f9-176">7,300</span></span>                    | <span data-ttu-id="557f9-177">8</span><span class="sxs-lookup"><span data-stu-id="557f9-177">8</span></span>                                       |

<span data-ttu-id="557f9-178">要在资产负债表中调整化整，请完成下列步骤。</span><span class="sxs-lookup"><span data-stu-id="557f9-178">To adjust rounding in a balance sheet, follow these steps.</span></span>

1.  <span data-ttu-id="557f9-179">在报表设计器中，单击**行定义**，然后打开行定义以修改。</span><span class="sxs-lookup"><span data-stu-id="557f9-179">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2.  <span data-ttu-id="557f9-180">在**编辑**菜单上，单击**舍入调整**。</span><span class="sxs-lookup"><span data-stu-id="557f9-180">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3.  <span data-ttu-id="557f9-181">在**化整调整**对话框中，输入下列值：</span><span class="sxs-lookup"><span data-stu-id="557f9-181">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>
    -   <span data-ttu-id="557f9-182">**舍入调整行** – 应调整以平衡资产负债表的行的行代码。</span><span class="sxs-lookup"><span data-stu-id="557f9-182">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    -   <span data-ttu-id="557f9-183">**总资产行** - 资产负债表中包含总资产的行的行代码。</span><span class="sxs-lookup"><span data-stu-id="557f9-183">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    -   <span data-ttu-id="557f9-184">**总债务和权益行** - 资产负债表中包含总债务和权益的行的行代码。</span><span class="sxs-lookup"><span data-stu-id="557f9-184">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    -   <span data-ttu-id="557f9-185">**调整金额限制** – 通过自动调整指定限制的正整数。</span><span class="sxs-lookup"><span data-stu-id="557f9-185">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="557f9-186">此金额将与实际化整差异的绝对值相比。</span><span class="sxs-lookup"><span data-stu-id="557f9-186">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    <span data-ttu-id="557f9-187">**注意：** 这些行代码必须链接到您的财务数据。</span><span class="sxs-lookup"><span data-stu-id="557f9-187">**Note:** These row codes must be linked to your financial data.</span></span> <span data-ttu-id="557f9-188">换言之，行的**链接到财务维度**单元格中必须具有维度值。</span><span class="sxs-lookup"><span data-stu-id="557f9-188">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="557f9-189">请**勿**引用描述 (**DESC**)、计算 (**CALC**) 或汇总 (**TOT**) 行。</span><span class="sxs-lookup"><span data-stu-id="557f9-189">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="557f9-190">资产负债表中的金额现在将在启用化整时均匀平衡。</span><span class="sxs-lookup"><span data-stu-id="557f9-190">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span> <span data-ttu-id="557f9-191">**注意：** 将基于为报表定义指定的**化整精度**选项应用调整限制。</span><span class="sxs-lookup"><span data-stu-id="557f9-191">**Note:** The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="557f9-192">例如，如果您选择将报表舍入到千分位并在**调整金额限制**字段中输入 **2**，则当**舍入调整行**字段中标识的值增加或减少 2,000 以上时，您将收到一条警告消息。</span><span class="sxs-lookup"><span data-stu-id="557f9-192">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="557f9-193">设置行和列文本的格式</span><span class="sxs-lookup"><span data-stu-id="557f9-193">Format row and column text</span></span>
<span data-ttu-id="557f9-194">您可以通过更改字体和格式文本来自定义报表的外观。</span><span class="sxs-lookup"><span data-stu-id="557f9-194">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="557f9-195">以下各节描述如何设置报表行和列的外观。</span><span class="sxs-lookup"><span data-stu-id="557f9-195">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="557f9-196">管理字体样式</span><span class="sxs-lookup"><span data-stu-id="557f9-196">Manage font styles</span></span>

<span data-ttu-id="557f9-197">您可以创建和修改报表的字体样式。</span><span class="sxs-lookup"><span data-stu-id="557f9-197">You can create and modify font styles for your report.</span></span> <span data-ttu-id="557f9-198">然后可以将这些样式应用到文档中，或应用到报表中的特定行或列。</span><span class="sxs-lookup"><span data-stu-id="557f9-198">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="557f9-199">创建字体样式</span><span class="sxs-lookup"><span data-stu-id="557f9-199">Create a font style</span></span></td>
<td><ol>
<li><span data-ttu-id="557f9-200">在报表设计器的<strong>格式</strong>菜单上，单击<strong>样式和格式</strong>。</span><span class="sxs-lookup"><span data-stu-id="557f9-200">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="557f9-201">在<strong>样式和格式</strong>对话框中单击<strong>新建</strong>，然后为新样式输入一个唯一名称。</span><span class="sxs-lookup"><span data-stu-id="557f9-201">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="557f9-202">选择字体，然后单击<strong>确定</strong>。</span><span class="sxs-lookup"><span data-stu-id="557f9-202">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="557f9-203">修改字体样式</span><span class="sxs-lookup"><span data-stu-id="557f9-203">Modify a font style</span></span></td>
<td><ol>
<li><span data-ttu-id="557f9-204">在报表设计器的<strong>格式</strong>菜单上，单击<strong>样式和格式</strong>。</span><span class="sxs-lookup"><span data-stu-id="557f9-204">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="557f9-205">在<strong>样式和格式</strong>对话框中选择要修改的样式，然后单击<strong>修改</strong>。</span><span class="sxs-lookup"><span data-stu-id="557f9-205">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="557f9-206">选择字体，然后单击<strong>确定</strong>。</span><span class="sxs-lookup"><span data-stu-id="557f9-206">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="557f9-207">应用字体样式</span><span class="sxs-lookup"><span data-stu-id="557f9-207">Apply a font style</span></span></td>
<td><ol>
<li><span data-ttu-id="557f9-208">在报表设计器中，在定义或列定义中，或在页眉和页脚中，选择一个或多个行单元格。</span><span class="sxs-lookup"><span data-stu-id="557f9-208">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="557f9-209">在工具栏的<strong>样式</strong>列表中，选择字体样式。</span><span class="sxs-lookup"><span data-stu-id="557f9-209">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="557f9-210">设置行文本的格式</span><span class="sxs-lookup"><span data-stu-id="557f9-210">Format row text</span></span>

<span data-ttu-id="557f9-211">在行定义中指定的格式将覆盖列定义和报表定义中指定的格式。</span><span class="sxs-lookup"><span data-stu-id="557f9-211">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="557f9-212">可以通过使用格式工具栏上的控件来修改文本格式。</span><span class="sxs-lookup"><span data-stu-id="557f9-212">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="557f9-213">这些控件是标准的 Microsoft Windows 控件。</span><span class="sxs-lookup"><span data-stu-id="557f9-213">These controls are standard Microsoft Windows controls.</span></span>

1.  <span data-ttu-id="557f9-214">在报表设计器中，打开要修改的行定义。</span><span class="sxs-lookup"><span data-stu-id="557f9-214">In Report Designer, open the row definition to modify.</span></span>
2.  <span data-ttu-id="557f9-215">选择要设置格式的单元格。</span><span class="sxs-lookup"><span data-stu-id="557f9-215">Select the cells to format.</span></span> <span data-ttu-id="557f9-216">要选择多个单元格，请在选择单元格的同时按住 Ctrl 键。</span><span class="sxs-lookup"><span data-stu-id="557f9-216">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3.  <span data-ttu-id="557f9-217">单击要应用的格式的工具栏按钮。</span><span class="sxs-lookup"><span data-stu-id="557f9-217">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="557f9-218">例如，要缩进行，请选择行，然后单击工具栏中的**增加缩进**![增加缩进](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "增加缩进")。</span><span class="sxs-lookup"><span data-stu-id="557f9-218">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="557f9-219">在设计报表时调整列</span><span class="sxs-lookup"><span data-stu-id="557f9-219">Adjust columns while you design reports</span></span>

<span data-ttu-id="557f9-220">为了便于在行定义中查看正在处理的列，您可调整列宽，还可以在视图窗格中隐藏（最小化）或显示列。</span><span class="sxs-lookup"><span data-stu-id="557f9-220">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="557f9-221">您所做的修改只影响屏幕上列的外观。</span><span class="sxs-lookup"><span data-stu-id="557f9-221">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="557f9-222">它们并不影响报表中的列格式。</span><span class="sxs-lookup"><span data-stu-id="557f9-222">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="557f9-223">更改列在视图窗格中的宽度</span><span class="sxs-lookup"><span data-stu-id="557f9-223">Change the width of a column in the view pane</span></span>

1.  <span data-ttu-id="557f9-224">在报表设计器中，打开要修改的行定义。</span><span class="sxs-lookup"><span data-stu-id="557f9-224">In Report Designer, open the row definition to modify.</span></span>
2.  <span data-ttu-id="557f9-225">在**格式**菜单上，选择**列宽**。</span><span class="sxs-lookup"><span data-stu-id="557f9-225">On the **Format** menu, select **Column Width**.</span></span>
3.  <span data-ttu-id="557f9-226">在**列宽**对话框中，输入值，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="557f9-226">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="557f9-227">或者，您还可拖动列标题单元格的右边界来更改列宽。</span><span class="sxs-lookup"><span data-stu-id="557f9-227">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="557f9-228">在视图窗格中隐藏列</span><span class="sxs-lookup"><span data-stu-id="557f9-228">Hide columns in the view pane</span></span>

1.  <span data-ttu-id="557f9-229">在报表设计器中，打开要修改的行定义。</span><span class="sxs-lookup"><span data-stu-id="557f9-229">In Report Designer, open the row definition to modify.</span></span>
2.  <span data-ttu-id="557f9-230">选择要最小化的一列或多列。</span><span class="sxs-lookup"><span data-stu-id="557f9-230">Select the column or columns to minimize.</span></span>
3.  <span data-ttu-id="557f9-231">右键单击，然后单击**隐藏**。</span><span class="sxs-lookup"><span data-stu-id="557f9-231">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="557f9-232">在视图窗格中显示所有隐藏列</span><span class="sxs-lookup"><span data-stu-id="557f9-232">Show all hidden columns in the view pane</span></span>

1.  <span data-ttu-id="557f9-233">在报表设计器中，打开要修改的行定义。</span><span class="sxs-lookup"><span data-stu-id="557f9-233">In Report Designer, open the row definition to modify.</span></span>
2.  <span data-ttu-id="557f9-234">右键单击要显示的最小化列，然后单击**取消隐藏**。</span><span class="sxs-lookup"><span data-stu-id="557f9-234">Right-click the minimized column to display, and then click **Unhide**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="557f9-235">其他资源</span><span class="sxs-lookup"><span data-stu-id="557f9-235">Additional resources</span></span>
--------

[<span data-ttu-id="557f9-236">财务申报</span><span class="sxs-lookup"><span data-stu-id="557f9-236">Financial reporting</span></span>](financial-reporting-intro.md)





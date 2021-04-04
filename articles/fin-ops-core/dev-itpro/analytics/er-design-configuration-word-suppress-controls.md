---
title: 禁止在生成的报告中使用 Word 内容控件
description: 本主题说明如何配置电子报告 (ER) 格式，以在禁止使用内容控件的地方生成 Microsoft Word 文件形式的报告。
author: NickSelin
manager: AnnBe
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 81ad25514154dd8982aa4f849f0b2bfeb85270f7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562110"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a><span data-ttu-id="98e3f-103">禁止在生成的报告中使用 Word 内容控件</span><span class="sxs-lookup"><span data-stu-id="98e3f-103">Suppress Word content controls in generated reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98e3f-104">要生成 Microsoft Word 文档形式的报告，必须将报告的模板设计为 Word 文档。</span><span class="sxs-lookup"><span data-stu-id="98e3f-104">To generate reports as Microsoft Word documents, you must design a template for the reports as a Word document.</span></span> <span data-ttu-id="98e3f-105">此模板必须包含 Word 内容控件作为将在运行时填充的数据的占位符。</span><span class="sxs-lookup"><span data-stu-id="98e3f-105">This template must contain Word content controls as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="98e3f-106">要将创建的 Word 文档用作报表的模板，可以[配置](er-design-configuration-word.md)一个新的[电子报告 (ER)](general-electronic-reporting.md) [解决方案](er-quick-start1-new-solution.md)。</span><span class="sxs-lookup"><span data-stu-id="98e3f-106">To use the Word document that is created as a template for your reports, you can [configure](er-design-configuration-word.md) a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="98e3f-107">此解决方案必须包含一个包含 ER [格式](general-electronic-reporting.md#FormatComponentOutbound)组件的 ER [配置](general-electronic-reporting.md#Configuration)。</span><span class="sxs-lookup"><span data-stu-id="98e3f-107">The solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="98e3f-108">必须配置这种 ER 格式才能使用设计的模板来生成报告。</span><span class="sxs-lookup"><span data-stu-id="98e3f-108">This ER format must be configured to use the designed template for report generation.</span></span>

<span data-ttu-id="98e3f-109">在 10.0.6 版及更高版本的 Dynamics 365 Finance 中，您可以以 ER 格式配置公式，以在生成的文档中禁止使用某些 Word 内容控件。</span><span class="sxs-lookup"><span data-stu-id="98e3f-109">In version 10.0.6 and later of Dynamics 365 Finance, you can configure formulas in your ER format to suppress some Word content controls in generated documents.</span></span>

<span data-ttu-id="98e3f-110">以下步骤说明了分配有系统管理员或电子报告功能顾问角色的用户如何配置 ER 格式，以生成 Word 文件形式的报告，并在使用 Word 模板配置的已生成报告中禁止使用某些内容控件。</span><span class="sxs-lookup"><span data-stu-id="98e3f-110">The following steps explain how a user who is assigned to the System administrator or Electronic reporting functional consultant role can configure an ER format that generates reports as Word files and suppresses some of the content controls in the generated reports that have been configured by using a Word template.</span></span>

<span data-ttu-id="98e3f-111">这些步骤可以在 GBSI 公司完成。</span><span class="sxs-lookup"><span data-stu-id="98e3f-111">These steps can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="98e3f-112">先决条件</span><span class="sxs-lookup"><span data-stu-id="98e3f-112">Prerequisites</span></span>

<span data-ttu-id="98e3f-113">若要完成这些步骤，首先必须完成下面任务指南中的步骤：</span><span class="sxs-lookup"><span data-stu-id="98e3f-113">To complete these steps, you must first complete the steps in the following task guides:</span></span>

- [<span data-ttu-id="98e3f-114">设计以 OPENXML 格式生成报表的配置</span><span class="sxs-lookup"><span data-stu-id="98e3f-114">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="98e3f-115">重复使用带有 Excel 模板的电子报告配置以 Word 格式生成报表</span><span class="sxs-lookup"><span data-stu-id="98e3f-115">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)

<span data-ttu-id="98e3f-116">完成这些任务指南的步骤时，将准备以下项目：</span><span class="sxs-lookup"><span data-stu-id="98e3f-116">When you complete the steps of these task guides, the following items are prepared:</span></span>

- <span data-ttu-id="98e3f-117">一种配置为以 Word 格式生成文档的 **样本工作表报告** ER 格式</span><span class="sxs-lookup"><span data-stu-id="98e3f-117">A **Sample worksheet report** ER format that is configured to generate a document in Word format</span></span>
- <span data-ttu-id="98e3f-118">一种标记为 **可运行** 的 [草稿](general-electronic-reporting.md#component-versioning)版本的 **样本工作表报告** ER 格式</span><span class="sxs-lookup"><span data-stu-id="98e3f-118">A [draft](general-electronic-reporting.md#component-versioning) version of the **Sample worksheet report** ER format that is marked as **Runnable**</span></span>
- <span data-ttu-id="98e3f-119">一种配置为使用 **样本工作表报告** ER 格式进行供应商付款处理的 **电子** 付款方式</span><span class="sxs-lookup"><span data-stu-id="98e3f-119">An **Electronic** method of payments that is configured to use the **Sample worksheet report** ER format for vendor payment processing</span></span>

<span data-ttu-id="98e3f-120">您还必须为同一个报表下载和保存以下模板：</span><span class="sxs-lookup"><span data-stu-id="98e3f-120">You must also download and save the following template for the sample report:</span></span>

- [<span data-ttu-id="98e3f-121">付款报表绑定模板 2 (SampleVendPaymDocReportBounded2.docx)</span><span class="sxs-lookup"><span data-stu-id="98e3f-121">Bounded Template 2 of Payment Report (SampleVendPaymDocReportBounded2.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a><span data-ttu-id="98e3f-122">查看下载的 Word 模板</span><span class="sxs-lookup"><span data-stu-id="98e3f-122">Review the downloaded Word template</span></span>

1. <span data-ttu-id="98e3f-123">在 Word 桌面应用程序中，打开您先前下载的 **SampleVendPaymDocReportBounded2.docx** 模板文件。</span><span class="sxs-lookup"><span data-stu-id="98e3f-123">In the Word desktop application, open the **SampleVendPaymDocReportBounded2.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="98e3f-124">验证模板文件是否包含摘要部分，该部分显示所处理付款中已满足的每种货币代码的总付款额。</span><span class="sxs-lookup"><span data-stu-id="98e3f-124">Verify that the template file contains a summary section that shows the total payment amounts for every currency code that has been met in the processed payments.</span></span>

    - <span data-ttu-id="98e3f-125">摘要部分位于 Word 文档的单独表中。</span><span class="sxs-lookup"><span data-stu-id="98e3f-125">The summary section resides in a separate table of the Word document.</span></span>
    - <span data-ttu-id="98e3f-126">该表的第一行将表列标题作为节标题。</span><span class="sxs-lookup"><span data-stu-id="98e3f-126">The first row of this table holds the table columns headings as the section header.</span></span>
    - <span data-ttu-id="98e3f-127">该表的第二行将重复的内容控件保留为节详细信息。</span><span class="sxs-lookup"><span data-stu-id="98e3f-127">The second row of this table holds the repeating content control as the section details.</span></span>
    - <span data-ttu-id="98e3f-128">此内容控件已映射到 **报告** 自定义 XML 部件的 **SummaryLines** 字段。</span><span class="sxs-lookup"><span data-stu-id="98e3f-128">This content control is mapped to the **SummaryLines** field of the **Report** custom XML part.</span></span>
    - <span data-ttu-id="98e3f-129">根据此映射，内容控件与可编辑 ER 格式的 **SummaryLines** 元素关联。</span><span class="sxs-lookup"><span data-stu-id="98e3f-129">Based on this mapping, the content control is associated with the **SummaryLines** element of the editable ER format.</span></span>

    > [!NOTE]
    > <span data-ttu-id="98e3f-130">重复内容控件由 **SummaryLines** 键标记，此键与已映射到的自定义 XML 部件的字段相匹配。</span><span class="sxs-lookup"><span data-stu-id="98e3f-130">The repeating content control is tagged by the **SummaryLines** key that matches the field of the custom XML part that it has been mapped to.</span></span>

    ![Word 模板布局](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="98e3f-132">选择现有 ER 报表配置</span><span class="sxs-lookup"><span data-stu-id="98e3f-132">Select the existing ER report configuration</span></span>

<span data-ttu-id="98e3f-133">对于以下步骤，您将重复使用在完成前面提到的任务指南中的步骤时配置的现有 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="98e3f-133">For the following steps, you will reuse the existing ER configuration that you configured when you completed the steps in the previously mentioned task guides.</span></span>

1. <span data-ttu-id="98e3f-134">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-134">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="98e3f-135">选择 **申报配置**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-135">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="98e3f-136">在 **配置** 页的配置树中，展开 **付款模型**，选择 **示例工作表报表**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-136">On the **Configurations** page, in the configuration tree, expand **Payment model**, and select **Sample worksheet report**.</span></span>
4. <span data-ttu-id="98e3f-137">选择 **设计器** 以编辑所选 ER 格式的草稿版本。</span><span class="sxs-lookup"><span data-stu-id="98e3f-137">Select **Designer** to edit the draft version of the selected ER format.</span></span>

## <a name="replace-the-current-template-with-the-new-template"></a><span data-ttu-id="98e3f-138">将当前模板替换为新模板</span><span class="sxs-lookup"><span data-stu-id="98e3f-138">Replace the current template with the new template</span></span>

<span data-ttu-id="98e3f-139">目前使用 SampleVendPaymDocReportBounded.docx 文件作为模板生成 Word 格式的输出。</span><span class="sxs-lookup"><span data-stu-id="98e3f-139">Currently, the SampleVendPaymDocReportBounded.docx file is used as a template to generate the output in Word format.</span></span> <span data-ttu-id="98e3f-140">在以下步骤中，您将此 Word 模板替换为前面下载的新 Word 模板，即 SampleVendPaymDocReportBounded2.docx。</span><span class="sxs-lookup"><span data-stu-id="98e3f-140">In the following steps, you will replace this Word template with the new Word template, SampleVendPaymDocReportBounded2.docx, that you downloaded earlier.</span></span>

1. <span data-ttu-id="98e3f-141">在 **格式设计器** 页上，选择 **附件**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-141">On the **Format designer** page, select **Attachments**.</span></span>
2. <span data-ttu-id="98e3f-142">在 **附件** 页上，选择 **删除** 删除现有的模板。</span><span class="sxs-lookup"><span data-stu-id="98e3f-142">On the **Attachments** page, select **Delete** to remove the existing template.</span></span>
3. <span data-ttu-id="98e3f-143">选择 **是** 以确认删除。</span><span class="sxs-lookup"><span data-stu-id="98e3f-143">Select **Yes** to confirm the deletion.</span></span>
4. <span data-ttu-id="98e3f-144">选择 **新建** \> **文件**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-144">Select **New** \> **File**.</span></span>
5. <span data-ttu-id="98e3f-145">选择 **浏览**，然后浏览到并选择您先前下载的 **SampleVendPaymDocReportBounded2.docx** 文件。</span><span class="sxs-lookup"><span data-stu-id="98e3f-145">Select **Browse**, and browse to and select the **SampleVendPaymDocReportBounded2.docx** file that you downloaded earlier.</span></span>
6. <span data-ttu-id="98e3f-146">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-146">Select **OK**.</span></span>
7. <span data-ttu-id="98e3f-147">关闭 **附件** 页。</span><span class="sxs-lookup"><span data-stu-id="98e3f-147">Close the **Attachments** page.</span></span>
8. <span data-ttu-id="98e3f-148">在 **格式设计器** 页面上的 **模板** 字段中，输入或选择 **SampleVendPaymDocReportBounded2.docx** 文件。</span><span class="sxs-lookup"><span data-stu-id="98e3f-148">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReportBounded2.docx** file.</span></span>

## <a name="run-the-format-to-create-word-output"></a><span data-ttu-id="98e3f-149">运行此格式以创建 Word 输出</span><span class="sxs-lookup"><span data-stu-id="98e3f-149">Run the format to create Word output</span></span>

1. <span data-ttu-id="98e3f-150">转到 **应付帐款** \> **付款** \> **付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-150">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="98e3f-151">在 **供应商付款** 页面上的 **列表** 选项卡上，选择所有付款。</span><span class="sxs-lookup"><span data-stu-id="98e3f-151">On the **Vendor payments** page, on the **List** tab, select all the payments.</span></span>
3. <span data-ttu-id="98e3f-152">选择 **付款状态**\>**无**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-152">Select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="98e3f-153">选择 **生成付款**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-153">Select **Generate payments**.</span></span>
5. <span data-ttu-id="98e3f-154">在 **付款方式** 字段中，选择 **电子**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-154">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="98e3f-155">在 **银行帐户** 字段中，选择 **GBSI OPER**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-155">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="98e3f-156">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-156">Select **OK**.</span></span>
8. <span data-ttu-id="98e3f-157">在 **电子报告参数** 对话框中，选择 **确定**，并分析生成的输出。</span><span class="sxs-lookup"><span data-stu-id="98e3f-157">In the **Electronic report parameters** dialog box, select **OK**, and analyze the generated output.</span></span>

    ![供应商付款页上要进行处理的付款](./media/er-design-configuration-word-suppress-controls-image2.gif)

    <span data-ttu-id="98e3f-159">输出以 Word 格式显示，并包含摘要部分。</span><span class="sxs-lookup"><span data-stu-id="98e3f-159">The output is presented in Word format and contains the summary section.</span></span>

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a><span data-ttu-id="98e3f-160">配置可编辑格式以禁止显示摘要部分</span><span class="sxs-lookup"><span data-stu-id="98e3f-160">Configure the editable format to suppress the summary section</span></span>

<span data-ttu-id="98e3f-161">如果要在生成的文档中禁止显示摘要部分，则必须根据运行此 ER 格式的用户的要求来修改可编辑的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="98e3f-161">If you want to suppress the summary section in a generated document, based on the request of a user who runs this ER format, you must modify the editable ER format.</span></span>

1. <span data-ttu-id="98e3f-162">转到 **组织管理**\>**工作区**\>**电子报告**，然后打开 ER 格式的草稿版本进行编辑。</span><span class="sxs-lookup"><span data-stu-id="98e3f-162">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**, and open the draft version of the ER format for editing.</span></span>
2. <span data-ttu-id="98e3f-163">选择 **申报配置**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-163">Select **Reporting configurations**.</span></span> 
3. <span data-ttu-id="98e3f-164">在 **配置** 页上的配置树中，展开 **付款模型** \> **示例工作表报表**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-164">On the **Configurations** page, in the configuration tree, expand **Payment model** \> **Sample worksheet report**.</span></span>
4. <span data-ttu-id="98e3f-165">选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-165">Select **Designer**.</span></span>
5. <span data-ttu-id="98e3f-166">在 **格式设计器** 页面上，展开 **Word**，然后选择 **SummaryLines**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-166">On the **Format designer** page, expand **Word**, and select **SummaryLines**.</span></span>
6. <span data-ttu-id="98e3f-167">在 **映射** 选项卡上，添加一个新的数据源以在运行时询问用户是否应禁止显示摘要部分：</span><span class="sxs-lookup"><span data-stu-id="98e3f-167">On the **Mapping** tab, add a new data source to ask the user, at runtime, whether the summary section should be suppressed:</span></span>

    1. <span data-ttu-id="98e3f-168">选择 **添加根**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-168">Select **Add root**.</span></span>
    2. <span data-ttu-id="98e3f-169">在 **添加数据源** 对话框中，选择 **常规\用户输入参数** 以打开 **用户输入参数数据源属性** 对话框。</span><span class="sxs-lookup"><span data-stu-id="98e3f-169">In the **Add data source** dialog box, select **General\User input parameter** to open the **'User input parameter' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="98e3f-170">在 **名称** 字段中，输入 **uipSuppress**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-170">In the **Name** field, enter **uipSuppress**.</span></span>
    4. <span data-ttu-id="98e3f-171">在 **标签** 字段中，输入 **禁止显示摘要部分**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-171">In the **Label** field, enter **Suppress summary section**.</span></span>
    5. <span data-ttu-id="98e3f-172">在 **操作数据类型名称** 字段中，选择或输入 **NoYes**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-172">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="98e3f-173">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-173">Select **OK**.</span></span>

7. <span data-ttu-id="98e3f-174">添加 **NoYes** 应用程序枚举类型的新数据源：</span><span class="sxs-lookup"><span data-stu-id="98e3f-174">Add a new data source of the **NoYes** application enumeration type:</span></span>

    1. <span data-ttu-id="98e3f-175">选择 **添加根**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-175">Select **Add root**.</span></span>
    2. <span data-ttu-id="98e3f-176">在 **添加数据源** 对话框中，选择 **Dynamics 365 for Operations\枚举**，以打开 **枚举数据源属性** 对话框。</span><span class="sxs-lookup"><span data-stu-id="98e3f-176">In the **Add data source** dialog box, select **Dynamics 365 for Operations\Enumeration** to open the **'Enumeration' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="98e3f-177">在 **名称** 字段中，输入 **enumNoYes**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-177">In the **Name** field, enter **enumNoYes**.</span></span>
    4. <span data-ttu-id="98e3f-178">在 **标签** 字段中，输入 **禁止显示选项**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-178">In the **Label** field, enter **Suppress options**.</span></span>
    5. <span data-ttu-id="98e3f-179">在 **操作数据类型名称** 字段中，选择或输入 **NoYes**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-179">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="98e3f-180">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-180">Select **OK**.</span></span>

8. <span data-ttu-id="98e3f-181">对于所选 **SummaryLines** 格式元素，配置公式以指定何时应禁止使用与所选格式元素关联的 Word 内容控件：</span><span class="sxs-lookup"><span data-stu-id="98e3f-181">For the selected **SummaryLines** format element, configure the formula to specify when the Word content control that is associated with the selected format element should be suppressed:</span></span>

    1. <span data-ttu-id="98e3f-182">在 **映射** 选项卡上的 **已移除** 部分，选择 **编辑** 以打开 **[公式设计器](general-electronic-reporting-formula-designer.md)** 页。</span><span class="sxs-lookup"><span data-stu-id="98e3f-182">On the **Mapping** tab, in the **Removed** section, select **Edit** to open the **[Formula designer](general-electronic-reporting-formula-designer.md)** page.</span></span>
    2. <span data-ttu-id="98e3f-183">在 **公式** 字段中，输入公式 `uipSuppress = enumNoYes.Yes`。</span><span class="sxs-lookup"><span data-stu-id="98e3f-183">In the **Formula** field, enter the formula `uipSuppress = enumNoYes.Yes`.</span></span>
    3. <span data-ttu-id="98e3f-184">选择 **保存**，然后关闭 **公式设计器** 页面。</span><span class="sxs-lookup"><span data-stu-id="98e3f-184">Select **Save**, and close the **Formula designer** page.</span></span>

        > [!NOTE]
        > <span data-ttu-id="98e3f-185">**在所有其他格式元素都运行之后**，此公式将应用于生成的文档。</span><span class="sxs-lookup"><span data-stu-id="98e3f-185">This formula will be applied to a generated document **after all other format elements are run**.</span></span> <span data-ttu-id="98e3f-186">为了应用此公式，会在生成的文档中查找一个被标记为配置公式所针对的格式元素（在本例中为 **SummaryLines**）的 Word 内容控件。</span><span class="sxs-lookup"><span data-stu-id="98e3f-186">To apply this formula, a Word content control that is tagged as a format element that the formula is configured for (**SummaryLines** in this case) is found in a generated document.</span></span> <span data-ttu-id="98e3f-187">然后，将该内容控件以及保存它的 Word 表中的行一起完全删除。</span><span class="sxs-lookup"><span data-stu-id="98e3f-187">That content control is then completely removed, together with the row in the Word table that holds it.</span></span> <span data-ttu-id="98e3f-188">摘要部分的详细信息行将从生成的文档中删除。</span><span class="sxs-lookup"><span data-stu-id="98e3f-188">The details row of the summary section is removed from the generated document.</span></span>
        >
        > <span data-ttu-id="98e3f-189">在设计时，您可以对格式元素配置 **已移除** 公式，即使您使用的 Word 模板中的内容控件没有与配置 **已移除** 属性所针对的格式元素名称相匹配的标签。</span><span class="sxs-lookup"><span data-stu-id="98e3f-189">At design time, you might configure the **Removed** formula for a format element, even though no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span> <span data-ttu-id="98e3f-190">在设计时验证格式时，您会收到关于这种不一致的[警告](er-components-inspections.md#i14)。</span><span class="sxs-lookup"><span data-stu-id="98e3f-190">When you validate the format at design time, you receive a [warning](er-components-inspections.md#i14) about this inconsistency.</span></span>
        >
        > <span data-ttu-id="98e3f-191">在运行时，如果您使用的 Word 模板中的内容控件没有与配置 **已移除** 属性所针对的格式元素名称相匹配的标签，则会引发异常。</span><span class="sxs-lookup"><span data-stu-id="98e3f-191">At runtime, an exception is thrown if no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span>

    4. <span data-ttu-id="98e3f-192">在 **映射** 选项卡上的 **已移除** 部分，将 **随父项一起** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-192">On the **Mapping** tab, in the **Removed** section, set the **With parent** option to **Yes**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="98e3f-193">您必须将此选项设置为 **是**，才能将整个 Word 表作为包含摘要部分详细信息的行的父对象删除。</span><span class="sxs-lookup"><span data-stu-id="98e3f-193">You must set this option to **Yes** to remove the whole Word table as the parent object of the row that holds the summary section details.</span></span> <span data-ttu-id="98e3f-194">如果将此选项设置为 **否**，则节标题行会保留在生成的文档中。</span><span class="sxs-lookup"><span data-stu-id="98e3f-194">If you set this option to **No**, the section header row remains in the generated document.</span></span>

9. <span data-ttu-id="98e3f-195">选择 **保存** 以保存对可编辑格式所做的更改。</span><span class="sxs-lookup"><span data-stu-id="98e3f-195">Select **Save** to save your changes to the editable format.</span></span>

    ![以 Word 格式生成的输出](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a><span data-ttu-id="98e3f-197">运行修改的格式以创建 Word 输出</span><span class="sxs-lookup"><span data-stu-id="98e3f-197">Run the modified format to create Word output</span></span>

1. <span data-ttu-id="98e3f-198">转到 **应付帐款** \> **付款** \> **付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-198">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="98e3f-199">选择所创建的付款日记帐，然后选择 **行**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-199">Select the payment journal that you created, and then select **Lines**.</span></span>
3. <span data-ttu-id="98e3f-200">在 **供应商付款** 页上，选择所有行，然后选择 **支付状态**\>**无**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-200">On the **Vendor payments** page, select all the rows, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="98e3f-201">选择 **生成付款**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-201">Select **Generate payments**.</span></span>
5. <span data-ttu-id="98e3f-202">在 **付款方式** 字段中，选择 **电子**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-202">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="98e3f-203">在 **银行帐户** 字段中，选择 **GBSI OPER**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-203">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="98e3f-204">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-204">Select **OK**.</span></span>
8. <span data-ttu-id="98e3f-205">在 **电子报告参数** 对话框内的 **禁止显示摘要部分** 字段中，选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="98e3f-205">In the **Electronic report parameters** dialog box, in the **Suppress summary section** field, select **Yes**.</span></span>
9. <span data-ttu-id="98e3f-206">选择 **确定**，并分析生成的输出。</span><span class="sxs-lookup"><span data-stu-id="98e3f-206">Select **OK**, and analyze the generated output.</span></span>

    ![以 Word 格式生成的输出](./media/er-design-configuration-word-suppress-controls-image4.gif)

    <span data-ttu-id="98e3f-208">请注意，该输出不包含摘要部分，因为它已被禁止显示。</span><span class="sxs-lookup"><span data-stu-id="98e3f-208">Notice that the output doesn't contain the summary section, because it has been suppressed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98e3f-209">其他资源</span><span class="sxs-lookup"><span data-stu-id="98e3f-209">Additional resources</span></span>

- [<span data-ttu-id="98e3f-210">设计以 OPENXML 格式生成报表的配置</span><span class="sxs-lookup"><span data-stu-id="98e3f-210">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="98e3f-211">设计新的电子报告配置以生成 Word 格式的报表</span><span class="sxs-lookup"><span data-stu-id="98e3f-211">Design a new ER configuration to generate reports in Word format</span></span>](er-design-configuration-word.md)
- [<span data-ttu-id="98e3f-212">重复使用带有 Excel 模板的电子报告配置以 Word 格式生成报表</span><span class="sxs-lookup"><span data-stu-id="98e3f-212">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="98e3f-213">检查配置的 ER 组件以防止运行时问题</span><span class="sxs-lookup"><span data-stu-id="98e3f-213">Inspect the configured ER component to prevent runtime issues</span></span>](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
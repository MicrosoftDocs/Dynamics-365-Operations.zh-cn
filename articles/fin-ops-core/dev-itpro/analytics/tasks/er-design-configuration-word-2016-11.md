---
title: 重用带有 Excel 模板的 ER 配置以 Word 格式生成报表
description: 本主题介绍如何配置设计为以 Excel 工作簿形式生成报表的报表格式，来以 Word 文档形式生成报表。
author: NickSelin
manager: AnnBe
ms.date: 01/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 601896bad72b079759b1a07efba8717101e94362
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569303"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a><span data-ttu-id="0f2b4-103">重用带有 Excel 模板的 ER 配置以 Word 格式生成报表</span><span class="sxs-lookup"><span data-stu-id="0f2b4-103">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0f2b4-104">要以 Microsoft Word 文档形式生成报表，您可以[配置](../er-design-configuration-word.md)一个新的[电子报告 (ER)](../general-electronic-reporting.md) [格式](../general-electronic-reporting.md#FormatComponentOutbound)。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-104">To generate reports as Microsoft Word documents, you can [configure](../er-design-configuration-word.md) a new [Electronic reporting (ER)](../general-electronic-reporting.md) [format](../general-electronic-reporting.md#FormatComponentOutbound).</span></span> <span data-ttu-id="0f2b4-105">或者，您可以重用最初设计为以 Excel 工作簿形式生成报表的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-105">Alternatively, you can reuse an ER format that was originally designed to generate reports as Excel workbooks.</span></span> <span data-ttu-id="0f2b4-106">在这种情况下，您必须用 Word 模板替换 Excel 模板。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-106">In this case, you must replace the Excel template with a Word template.</span></span>

<span data-ttu-id="0f2b4-107">以下过程说明具有系统管理员角色或电子报告开发人员角色的用户，如何通过重用设计为以 Excel 文件形式生成报表的 ER 格式，来将 ER 格式配置为以 Word 文件形式生成报表。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-107">The following procedures show how a user in either the System administrator role or the Electronic reporting developer role can configure an ER format to generate reports as Word files by reusing an ER format that was designed to generate reports as Excel files.</span></span>

<span data-ttu-id="0f2b4-108">这些过程可以在 GBSI 公司中完成。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-108">These procedures can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0f2b4-109">先决条件</span><span class="sxs-lookup"><span data-stu-id="0f2b4-109">Prerequisites</span></span>

<span data-ttu-id="0f2b4-110">要完成这些过程，您必须首先按照[设计用于以 OPENXML 格式生成报表的配置](er-design-reports-openxml-2016-11.md)任务指南中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-110">To complete these procedures, you must first follow the steps in the [Design a configuration for generating reports in OPENXML format](er-design-reports-openxml-2016-11.md) task guide.</span></span>

<span data-ttu-id="0f2b4-111">您还必须为同一个报表下载以下模板并保存到本地：</span><span class="sxs-lookup"><span data-stu-id="0f2b4-111">You must also download and locally save the following templates for the sample report:</span></span>

- [<span data-ttu-id="0f2b4-112">付款报表模板 (SampleVendPaymDocReport.docx)</span><span class="sxs-lookup"><span data-stu-id="0f2b4-112">Template of Payment Report (SampleVendPaymDocReport.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="0f2b4-113">付款报表绑定模板 (SampleVendPaymDocReportBounded.docx)</span><span class="sxs-lookup"><span data-stu-id="0f2b4-113">Bounded Template of Payment Report (SampleVendPaymDocReportBounded.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

<span data-ttu-id="0f2b4-114">这些过程针对的是 Dynamics 365 for Operations 版本 1611（2016 年 11 月）中添加的功能。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-114">These procedures are for a feature that was added in Dynamics 365 for Operations version 1611 (November 2016).</span></span>

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="0f2b4-115">选择现有 ER 报表配置</span><span class="sxs-lookup"><span data-stu-id="0f2b4-115">Select the existing ER report configuration</span></span>

1. <span data-ttu-id="0f2b4-116">在 Dynamics 365 Finance 中，转到 **组织管理** \> **工作区** \> **电子报告**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-116">In Dynamics 365 Finance, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0f2b4-117">确保 **Litware, Inc.** 配置提供程序已选择 **有效**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-117">Make sure that the **Litware, Inc.** configuration provider is selected as **Active**.</span></span> <span data-ttu-id="0f2b4-118">否则，请按照[创建配置提供程序并将其标记为有效](er-configuration-provider-mark-it-active-2016-11.md)任务指南中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-118">If it isn't, follow the steps in the [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) task guide.</span></span>
3. <span data-ttu-id="0f2b4-119">选择 **申报配置**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-119">Select **Reporting configurations**.</span></span> <span data-ttu-id="0f2b4-120">您将重用设计为以 OPENXML 格式生成报表输出的现有 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-120">You will reuse the existing ER configuration that was designed to generate the report output in OPENXML format.</span></span>
4. <span data-ttu-id="0f2b4-121">在 **配置** 页的左侧窗格的配置树中，展开 **付款模型**，选择 **示例工作表报表**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-121">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and select **Sample worksheet report**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0f2b4-122">所选 ER 格式的草稿版本可以在 **版本** 快速选项卡上编辑。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-122">The draft version of the selected ER format can be edited on the **Versions** FastTab.</span></span>

5. <span data-ttu-id="0f2b4-123">选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-123">Select **Designer**.</span></span>
6. <span data-ttu-id="0f2b4-124">在 **格式设计器** 页上，注意根格式元素的标题指示当前正在使用 Excel 模板。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-124">On the **Format designer** page, notice that the title of the root format element indicates that an Excel template is currently used.</span></span>

![选择现有配置](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a><span data-ttu-id="0f2b4-126">查看下载的 Word 模板</span><span class="sxs-lookup"><span data-stu-id="0f2b4-126">Review the downloaded Word template</span></span>

1. <span data-ttu-id="0f2b4-127">在 Word 桌面应用程序中，打开您先前下载的 **SampleVendPaymDocReport.docx** 模板文件。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-127">In the Word desktop application, open the **SampleVendPaymDocReport.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="0f2b4-128">确认此模板仅包含要作为 ER 输出生成的文档的布局。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-128">Verify that the template contains only the layout of the document that you want to generate as ER output.</span></span>

![桌面应用程序中的 Word 模板布局](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a><span data-ttu-id="0f2b4-130">将 Excel 模板替换为 Word 模板并添加自定义 XML 部件</span><span class="sxs-lookup"><span data-stu-id="0f2b4-130">Replace the Excel template with the Word template and add a custom XML part</span></span>

<span data-ttu-id="0f2b4-131">目前使用 Excel 文档作为模板生成 OPENXML 格式的输出。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-131">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="0f2b4-132">您将此模板替换为前面下载的 Word 模板文件 SampleVendPaymDocReport.docx。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-132">You will replace this template with the SampleVendPaymDocReport.docx Word template file that you downloaded earlier.</span></span> <span data-ttu-id="0f2b4-133">您还将通过添加自定义 XML 部件扩展 Work 模板。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-133">You will also extend the Word template by adding a custom XML part.</span></span>

1. <span data-ttu-id="0f2b4-134">在 Finance 中，在 **格式设计器** 页的 **格式** 选项卡上，选择 **附件**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-134">In Finance, on the **Format designer** page, on the **Format** tab, select **Attachments**.</span></span>
2. <span data-ttu-id="0f2b4-135">在 **附件** 页上，选择 **删除** 删除现有的 Excel 模板。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-135">On the **Attachments** page, select **Delete** to remove the existing Excel template.</span></span> <span data-ttu-id="0f2b4-136">选择 **是** 确认更改。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-136">Select **Yes** to confirm the change.</span></span>
3. <span data-ttu-id="0f2b4-137">选择 **新建** \> **文件**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-137">Select **New** \> **File**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0f2b4-138">您必须选择已在 ER 参数中[配置](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)的文档类型来存储 ER 格式的模板。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-138">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

4. <span data-ttu-id="0f2b4-139">选择 **浏览**，然后浏览到并选择您先前下载的 **SampleVendPaymDocReport.docx** 文件。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-139">Select **Browse**, and then browse to and select the **SampleVendPaymDocReport.docx** file that you downloaded earlier.</span></span>
5. <span data-ttu-id="0f2b4-140">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-140">Select **OK**.</span></span>
6. <span data-ttu-id="0f2b4-141">关闭 **附件** 页。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-141">Close the **Attachments** page.</span></span>
7. <span data-ttu-id="0f2b4-142">在 **格式设计器** 页上，在 **模板** 字段中，输入或选择 **SampleVendPaymDocReport.docx** 文件以使用该 Word 模板而不是以前使用的 Excel 模板。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-142">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReport.docx** file to use that Word template instead of the Excel template that was previously used.</span></span>
8. <span data-ttu-id="0f2b4-143">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-143">Select **Save**.</span></span>

    <span data-ttu-id="0f2b4-144">除了存储配置更改之外，**保存** 操作还会更新附加的 Word 模板。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-144">In addition to storing configuration changes, the **Save** action updates the attached Word template.</span></span> <span data-ttu-id="0f2b4-145">所设计格式的层次结构采用名称 **报表**、作为新的自定义 XML 部件添加到附加的 Word 文档。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-145">The hierarchical structure of the designed format is added to the attached Word document as a new custom XML part that is named **Report**.</span></span> <span data-ttu-id="0f2b4-146">附加的 Word 模板包含要作为 ER 输出生成的文档的布局，以及 ER 将在运行时输入到该模板中的数据的结构。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-146">The attached Word template contains the layout of the document that will be generated as ER output and the structure of data that ER will enter in that template at runtime.</span></span>

9. <span data-ttu-id="0f2b4-147">注意根格式元素的标题指示当前正在使用 Word 模板。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-147">Notice that the title of the root format element indicates that a Word template is currently used.</span></span>

    ![将 Excel 模板替换为 Word 模板并添加自定义 XML 部件](../media/er-design-configuration-word-2016-11-image03.gif)

10. <span data-ttu-id="0f2b4-149">在 **格式** 选项卡中，选择 **附件**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-149">On the **Format** tab, select **Attachments**.</span></span>

<span data-ttu-id="0f2b4-150">您现在可以将 **报表** 自定义 XML 部件的元素映射到 Word 文档的内容控件。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-150">You can now map the elements of the **Report** custom XML part to the content controls of the Word document.</span></span>

<span data-ttu-id="0f2b4-151">如果您熟悉此流程：将 Word 文档设计为包含映射到[自定义 XML 部件](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019)的元素的[内容控件](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word)的表单，请完成下一个过程中的所有步骤来创建文档。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-151">If you're familiar with the process of designing Word documents as forms that contain [content controls](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) that are mapped to elements of [custom XML parts](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), complete all steps in the next procedure to create the document.</span></span> <span data-ttu-id="0f2b4-152">有关详细信息，请参阅[在 Word 中创建用户填写或打印的表单](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b)。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-152">For more information, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span></span> <span data-ttu-id="0f2b4-153">否则，请跳过下一个过程。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-153">Otherwise, skip the next procedure.</span></span>

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a><span data-ttu-id="0f2b4-154">获取具有自定义 XML 部件的 Word 文档并进行数据映射</span><span class="sxs-lookup"><span data-stu-id="0f2b4-154">Get a Word document that has a custom XML part and do data mapping</span></span>

1. <span data-ttu-id="0f2b4-155">在 Finance 中，在 **附件** 页上，选择 **打开** 从 Finance 下载所选模板并将其本地存储为 Word 文档。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-155">In Finance, on the **Attachments** page, select **Open** to download the selected template from Finance and store it locally as a Word document.</span></span>
3. <span data-ttu-id="0f2b4-156">在 Word 桌面应用程序中，打开刚才下载的文档。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-156">In the Word desktop application, open the document that you just downloaded.</span></span>
4. <span data-ttu-id="0f2b4-157">在 **开发人员** 选项卡上，选择 **XML 映射窗格**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-157">On the **Developer** tab, select **XML Mapping Pane**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0f2b4-158">如果 **开发人员** 选项卡没有出现在功能区上，请自定义功能区来进行添加。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-158">If the **Developer** tab doesn't appear on the ribbon, customize the ribbon to add it.</span></span>

5. <span data-ttu-id="0f2b4-159">在 **XML 映射** 窗格中的 **自定义 XML 部件** 字段中，选择 **报表** 自定义 XML 部件。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-159">In the **XML Mapping** pane, in the **Custom XML Part** field, select the **Report** custom XML part.</span></span>
6. <span data-ttu-id="0f2b4-160">将所选的 **报表** 自定义 XML 部件的元素与 Word 文档的内容控件进行映射。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-160">Map the elements of the selected **Report** custom XML part and the content controls of the Word document.</span></span>
7. <span data-ttu-id="0f2b4-161">将更新的 Word 文档本地保存为 **SampleVendPaymDocReportBounded.docx**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-161">Save the updated Word document locally as **SampleVendPaymDocReportBounded.docx**.</span></span>

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="0f2b4-162">查看将自定义 XML 部件映射到内容控件的 Word 模板</span><span class="sxs-lookup"><span data-stu-id="0f2b4-162">Review the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="0f2b4-163">在 Word 桌面应用程序中，打开 **SampleVendPaymDocReportBounded.docx** 模板文件。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-163">In the Word desktop application, open the **SampleVendPaymDocReportBounded.docx** template file.</span></span>
2. <span data-ttu-id="0f2b4-164">确认此模板包含要作为 ER 输出生成的文档的布局。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-164">Verify that the template contains the layout of the document that you want to generate as ER output.</span></span> <span data-ttu-id="0f2b4-165">用作 ER 将在运行时在此模板中输入的数据的占位符的内容控件，基于在 **报表** 自定义 XML 部件的元素与 Word 文档的内容控件之间配置的映射。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-165">The content controls that are used as placeholders for data that ER will enter in this template at runtime are based on the mappings that are configured between elements of the **Report** custom XML part and the content controls of the Word document.</span></span>

![桌面应用程序中的 Word 模板预览](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="0f2b4-167">上载将自定义 XML 部件映射到内容控件的 Word 模板</span><span class="sxs-lookup"><span data-stu-id="0f2b4-167">Upload the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="0f2b4-168">在 Finance 中，在 **附件** 页上，选择 **删除** 删除在 **报表** 自定义 XML 部件的元素与内容控件之间没有映射的 Word 模板。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-168">In Finance, on the **Attachments** page, select **Delete** to remove the Word template that has no mappings between elements of the **Report** custom XML part and content controls.</span></span> <span data-ttu-id="0f2b4-169">选择 **是** 确认更改。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-169">Select **Yes** to confirm the change.</span></span>
2. <span data-ttu-id="0f2b4-170">选择 **新建**\>**文件**，添加一个包含 **报表** 自定义 XML 部件的元素与内容控件之间的映射的新模板文件。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-170">Select **New** \> **File** to add a new template file that contains mappings between elements of the **Report** custom XML part and content controls.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0f2b4-171">您必须选择已在 ER 参数中[配置](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)的文档类型来存储 ER 格式的模板。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-171">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

3. <span data-ttu-id="0f2b4-172">选择 **浏览**，然后浏览到并选择您通过完成 [获取具有自定义 XML 部件的 Word 以进行数据映射](#get-word-doc)一节中的过程下载或准备的 **SampleVendPaymDocReportBounded.docx** 文件。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-172">Select **Browse**, and then browse to and select the **SampleVendPaymDocReportBounded.docx** file that you downloaded or prepared by completing the procedure in the [Get a Word that has a custom XML part to do data mapping](#get-word-doc) section.</span></span>
4. <span data-ttu-id="0f2b4-173">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-173">Select **OK**.</span></span>
5. <span data-ttu-id="0f2b4-174">关闭 **附件** 页。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-174">Close the **Attachments** page.</span></span>
6. <span data-ttu-id="0f2b4-175">在 **格式设计器** 页上，在 **模板** 字段中，选择您刚才下载的文档。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-175">On the **Format designer** page, in the **Template** field, select the document that you just downloaded.</span></span>
7. <span data-ttu-id="0f2b4-176">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-176">Select **Save**.</span></span>
8. <span data-ttu-id="0f2b4-177">关闭 **格式设计器** 页。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-177">Close the **Format designer** page.</span></span>

## <a name="mark-the-configured-format-as-runnable"></a><span data-ttu-id="0f2b4-178">将配置的格式标记为可运行</span><span class="sxs-lookup"><span data-stu-id="0f2b4-178">Mark the configured format as runnable</span></span>

<span data-ttu-id="0f2b4-179">要运行可编辑格式的草稿版本，您必须先使其[可运行](../er-quick-start2-customize-report.md#MarkFormatRunnable)。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-179">To run the draft version of the editable format, you must make it [runnable](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span></span>

1. <span data-ttu-id="0f2b4-180">在 Finance 中，在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-180">In Finance, on the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
2. <span data-ttu-id="0f2b4-181">在 **使用参数** 对话框中，将 **运行设置** 选项设置为 **是**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-181">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
3. <span data-ttu-id="0f2b4-182">根据需要，选择 **编辑** 以使当前页面可供编辑。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-182">Select **Edit** to make the current page editable, as required.</span></span>
4. <span data-ttu-id="0f2b4-183">对于当前选择的 **示例工作表报表** 配置，将 **运行草稿** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-183">For the currently selected **Sample worksheet report** configuration, set the **Run Draft** option to **Yes**.</span></span>
5. <span data-ttu-id="0f2b4-184">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-184">Select **Save**.</span></span>

## <a name="run-the-format-to-create-output-in-word-format"></a><span data-ttu-id="0f2b4-185">运行格式以 Word 格式创建输出</span><span class="sxs-lookup"><span data-stu-id="0f2b4-185">Run the format to create output in Word format</span></span>

1. <span data-ttu-id="0f2b4-186">在 Finance 中，转到 **应付帐款** \> **付款** \> **付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-186">In Finance, go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="0f2b4-187">在您之前输入的付款日记帐中，选择 **行**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-187">In a payment journal that you entered earlier, select **Lines**.</span></span>
3. <span data-ttu-id="0f2b4-188">在 **供应商付款** 页上，选择网格中的所有行。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-188">On the **Vendor payments** page, select all rows in the grid.</span></span>
4. <span data-ttu-id="0f2b4-189">选择 **付款状态**\>**无**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-189">Select **Payment status** \> **None**.</span></span>

    ![供应商付款页上要进行处理的付款](../media/er-design-configuration-word-2016-11-image05.png)

5. <span data-ttu-id="0f2b4-191">在操作窗格上，选择 **生成付款**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-191">On the Action Pane, select **Generate payments**.</span></span>
6. <span data-ttu-id="0f2b4-192">在出现的对话框中，执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="0f2b4-192">In the dialog box that appears, follow these steps:</span></span>

    1. <span data-ttu-id="0f2b4-193">在 **付款方式** 字段中，选择 **电子**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-193">In the **Method of payment** field, select **Electronic**.</span></span>
    2. <span data-ttu-id="0f2b4-194">在 **银行帐户** 字段中，选择 **GBSI OPER**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-194">In the **Bank account** field, select **GBSI OPER**.</span></span>
    3. <span data-ttu-id="0f2b4-195">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-195">Select **OK**.</span></span>

7. <span data-ttu-id="0f2b4-196">在 **电子申报参数** 对话框中，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-196">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="0f2b4-197">生成的输出以 Word 格式表示，其中包含处理的付款的详细信息。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-197">The generated output is presented in Word format and contains the details of the processed payments.</span></span> <span data-ttu-id="0f2b4-198">分析生成的输出。</span><span class="sxs-lookup"><span data-stu-id="0f2b4-198">Analyze the generated output.</span></span>

    ![以 Word 格式生成的输出](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a><span data-ttu-id="0f2b4-200">其他资源</span><span class="sxs-lookup"><span data-stu-id="0f2b4-200">Additional resources</span></span>

- [<span data-ttu-id="0f2b4-201">设计新 ER 配置以生成 Word 格式的报表</span><span class="sxs-lookup"><span data-stu-id="0f2b4-201">Design a new ER configuration to generate reports in Word format</span></span>](../er-design-configuration-word.md)
- [<span data-ttu-id="0f2b4-202">使用 ER 在您生成的文档中嵌入图像和形状</span><span class="sxs-lookup"><span data-stu-id="0f2b4-202">Embed images and shapes in documents that you generate by using ER</span></span>](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
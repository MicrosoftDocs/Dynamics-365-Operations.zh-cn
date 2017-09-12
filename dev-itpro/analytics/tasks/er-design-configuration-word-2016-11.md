--- 
title: "针对电子申报 (ER) 设计用于生成 Microsoft Word 格式的报表的配置"
description: "以下步骤说明属于系统管理员或电子申报开发人员的用户如何配置电子申报 (ER) 格式，以便生成 Microsoft Word 文件格式的报表。"
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 950133ad73fd609938a64c3df16c34439ab860c1
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="design-a-configuration-for-generating-reports-in-microsoft-word-format-for-electronic-reporting-er"></a><span data-ttu-id="95c5f-103">针对电子申报 (ER) 设计用于生成 Microsoft Word 格式的报表的配置</span><span class="sxs-lookup"><span data-stu-id="95c5f-103">Design a configuration for generating reports in Microsoft Word format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="95c5f-104">以下步骤说明属于系统管理员或电子申报开发人员的用户如何配置电子申报 (ER) 格式，以便生成 Microsoft Word 文件格式的报表。</span><span class="sxs-lookup"><span data-stu-id="95c5f-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="95c5f-105">这些步骤可以在 GBSI 公司执行。</span><span class="sxs-lookup"><span data-stu-id="95c5f-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="95c5f-106">为了完成这些步骤，您首先必须完成任务指南“创建用于以 OPENXML 格式生成报表的 ER 配置”中的步骤。</span><span class="sxs-lookup"><span data-stu-id="95c5f-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="95c5f-107">您还必须提前为同一个报表下载以下模板并保存到本地：</span><span class="sxs-lookup"><span data-stu-id="95c5f-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

<span data-ttu-id="95c5f-108">http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReport.docx</span><span class="sxs-lookup"><span data-stu-id="95c5f-108">http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReport.docx</span></span>

<span data-ttu-id="95c5f-109">http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReportBounded.docx</span><span class="sxs-lookup"><span data-stu-id="95c5f-109">http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReportBounded.docx</span></span>

<span data-ttu-id="95c5f-110">此过程针对 Microsoft Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="95c5f-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="95c5f-111">选择现有 ER 报表配置</span><span class="sxs-lookup"><span data-stu-id="95c5f-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="95c5f-112">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-112">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="95c5f-113">确保配置提供商“Litware 公司”</span><span class="sxs-lookup"><span data-stu-id="95c5f-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="95c5f-114">已选中为有效。</span><span class="sxs-lookup"><span data-stu-id="95c5f-114">is selected as active.</span></span>  
2. <span data-ttu-id="95c5f-115">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-115">Click Reporting configurations.</span></span>
    * <span data-ttu-id="95c5f-116">我们将重复使用最初为生成 OPENXML 格式的报表输出而设计的现有 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="95c5f-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="95c5f-117">在树结构中，展开“付款模型”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="95c5f-118">在树结构中，选择“付款模型\示例工作表报表”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="95c5f-119">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="95c5f-120">将 Excel 模板替换为 Word 模板</span><span class="sxs-lookup"><span data-stu-id="95c5f-120">Replace the Excel template with the Word template</span></span>
    * <span data-ttu-id="95c5f-121">目前使用 Excel 文档作为模板生成 OPENXML 格式的输出。</span><span class="sxs-lookup"><span data-stu-id="95c5f-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="95c5f-122">我们将导入 Word 格式的报表模板。</span><span class="sxs-lookup"><span data-stu-id="95c5f-122">We will import the report’s template in Word format.</span></span>  
1. <span data-ttu-id="95c5f-123">单击“附加”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-123">Click Attachments.</span></span>
    * <span data-ttu-id="95c5f-124">将现有 Excel 模板替换为前面下载的 Word 模板 SampleVendPaymDocReport.docx。</span><span class="sxs-lookup"><span data-stu-id="95c5f-124">Replace the existing Excel template with the Word template that you downloaded earlier, SampleVendPaymDocReport.docx.</span></span> <span data-ttu-id="95c5f-125">请注意，此模板中仅包含要作为 ER 输出生成的文档的布局。</span><span class="sxs-lookup"><span data-stu-id="95c5f-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="95c5f-126">单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-126">Click Delete.</span></span>
3. <span data-ttu-id="95c5f-127">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-127">Click Yes.</span></span>
4. <span data-ttu-id="95c5f-128">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-128">Click New.</span></span>
5. <span data-ttu-id="95c5f-129">单击“文件”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-129">Click File.</span></span>
6. <span data-ttu-id="95c5f-130">单击浏览。</span><span class="sxs-lookup"><span data-stu-id="95c5f-130">Click Browse.</span></span> <span data-ttu-id="95c5f-131">导航到前面下载的 SampleVendPaymDocReport.docx 并选中。</span><span class="sxs-lookup"><span data-stu-id="95c5f-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="95c5f-132">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-132">Click OK.</span></span>
    * <span data-ttu-id="95c5f-133">选择上一步中下载的模板。</span><span class="sxs-lookup"><span data-stu-id="95c5f-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="95c5f-134">在“模板”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="95c5f-134">In the Template field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="95c5f-135">通过添加自定义 XML 部件扩展 Work 模板</span><span class="sxs-lookup"><span data-stu-id="95c5f-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="95c5f-136">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-136">Click Save.</span></span>
    * <span data-ttu-id="95c5f-137">除了存储配置更改之外，“保存”操作还会更新附加的 Word 模板。</span><span class="sxs-lookup"><span data-stu-id="95c5f-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="95c5f-138">所设计格式的结构采用名称“报表”并作为新的自定义 XML 的一部分移植到附加的 Word 文档。</span><span class="sxs-lookup"><span data-stu-id="95c5f-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="95c5f-139">请注意，附加的 Word 模板中不仅包含要作为 ER 输出生成的文档的布局，还包含 ER 将在运行时填充到此模板中的数据的结构。</span><span class="sxs-lookup"><span data-stu-id="95c5f-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="95c5f-140">单击“附加”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-140">Click Attachments.</span></span>
    * <span data-ttu-id="95c5f-141">现在需要将自定义 XML 部件“报表”的元素绑定到 Word 文档部件。</span><span class="sxs-lookup"><span data-stu-id="95c5f-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    * <span data-ttu-id="95c5f-142">如果您熟悉可设计为包含与自定义 XML 部件的元素绑定的内容控件的窗体的 Word 文档，请执行下一个子任务的所有步骤以创建此类文档。</span><span class="sxs-lookup"><span data-stu-id="95c5f-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="95c5f-143">有关更多详细信息，请访问链接 https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US。</span><span class="sxs-lookup"><span data-stu-id="95c5f-143">For more details, see this link https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span></span> <span data-ttu-id="95c5f-144">否则，请跳过下一子任务的所有步骤。</span><span class="sxs-lookup"><span data-stu-id="95c5f-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="95c5f-145">让包含自定义 XML 部件的 Word 执行数据绑定</span><span class="sxs-lookup"><span data-stu-id="95c5f-145">Get Word with custom XML part to do data bindings</span></span>
    * <span data-ttu-id="95c5f-146">在 Word 中打开此文档并执行以下操作：- 打开“Word 开发人员”选项卡（如果尚未启用此选项卡，请自定义功能区）。</span><span class="sxs-lookup"><span data-stu-id="95c5f-146">Open this document in Word and do the following:  - Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>  <span data-ttu-id="95c5f-147">- 选择“XML 映射”窗格。</span><span class="sxs-lookup"><span data-stu-id="95c5f-147">- Select XML mapping pane.</span></span>  <span data-ttu-id="95c5f-148">- 在查找中选择自定义 XML 部件“报表”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-148">- Select the ‘Report’ custom XML part in the lookup.</span></span>  <span data-ttu-id="95c5f-149">- 执行所选自定义 XML 部件的元素与 Word 文档的内容控件之间的映射。</span><span class="sxs-lookup"><span data-stu-id="95c5f-149">- Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="95c5f-150">- 将更新后的 Word 文档保存到本地驱动器。</span><span class="sxs-lookup"><span data-stu-id="95c5f-150">- Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="95c5f-151">上传包含绑定到内容控件的自定义 XML 部件的 Word 模板</span><span class="sxs-lookup"><span data-stu-id="95c5f-151">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="95c5f-152">单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-152">Click Delete.</span></span>
2. <span data-ttu-id="95c5f-153">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-153">Click Yes.</span></span>
    * <span data-ttu-id="95c5f-154">添加新模板。</span><span class="sxs-lookup"><span data-stu-id="95c5f-154">Add a new template.</span></span> <span data-ttu-id="95c5f-155">如果完成了前面的子任务中的步骤，请选择已准备并保存到本地的 Word 文档。</span><span class="sxs-lookup"><span data-stu-id="95c5f-155">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="95c5f-156">否则，选择之前下载的 SampleVendPaymDocReportBounded.docx MS Word 模板。</span><span class="sxs-lookup"><span data-stu-id="95c5f-156">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="95c5f-157">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-157">Click New.</span></span>
4. <span data-ttu-id="95c5f-158">单击“文件”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-158">Click File.</span></span>
5. <span data-ttu-id="95c5f-159">单击浏览。</span><span class="sxs-lookup"><span data-stu-id="95c5f-159">Click Browse.</span></span> <span data-ttu-id="95c5f-160">导航到前面下载的 SampleVendPaymDocReportBounded.docx 并选中。</span><span class="sxs-lookup"><span data-stu-id="95c5f-160">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="95c5f-161">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-161">Click OK.</span></span>
6. <span data-ttu-id="95c5f-162">在“模板”字段中，选择上一步中下载的文档。</span><span class="sxs-lookup"><span data-stu-id="95c5f-162">In the Template field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="95c5f-163">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-163">Click Save.</span></span>
8. <span data-ttu-id="95c5f-164">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="95c5f-164">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="95c5f-165">执行格式以创建 Word 输出</span><span class="sxs-lookup"><span data-stu-id="95c5f-165">Execute the format to create Word output</span></span>
1. <span data-ttu-id="95c5f-166">在操作窗格上，单击“配置”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-166">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="95c5f-167">单击“用户参数”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-167">Click User parameters.</span></span>
3. <span data-ttu-id="95c5f-168">在“运行设置”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-168">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="95c5f-169">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-169">Click OK.</span></span>
5. <span data-ttu-id="95c5f-170">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-170">Click Edit.</span></span>
6. <span data-ttu-id="95c5f-171">在“运行草稿”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-171">Select Yes in the Run Draft field.</span></span>
7. <span data-ttu-id="95c5f-172">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-172">Click Save.</span></span>
8. <span data-ttu-id="95c5f-173">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="95c5f-173">Close the page.</span></span>
9. <span data-ttu-id="95c5f-174">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="95c5f-174">Close the page.</span></span>
10. <span data-ttu-id="95c5f-175">转至“应付帐款”>“付款”>“付款日记帐”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-175">Go to Accounts payable > Payments > Payment journal.</span></span>
11. <span data-ttu-id="95c5f-176">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-176">Click Lines.</span></span>
12. <span data-ttu-id="95c5f-177">在列表中，标记或取消标记所有行。</span><span class="sxs-lookup"><span data-stu-id="95c5f-177">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="95c5f-178">单击“付款状态”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-178">Click Payment status.</span></span>
14. <span data-ttu-id="95c5f-179">单击“无”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-179">Click None.</span></span>
15. <span data-ttu-id="95c5f-180">点击”生成付款“。</span><span class="sxs-lookup"><span data-stu-id="95c5f-180">Click Generate payments.</span></span>
16. <span data-ttu-id="95c5f-181">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-181">Click OK.</span></span>
17. <span data-ttu-id="95c5f-182">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="95c5f-182">Click OK.</span></span>
    * <span data-ttu-id="95c5f-183">分析生成的输出。</span><span class="sxs-lookup"><span data-stu-id="95c5f-183">Analyze the generated output.</span></span> <span data-ttu-id="95c5f-184">请注意，创建的输出以 Word 格式表示，并且其中包含处理的付款的详细信息。</span><span class="sxs-lookup"><span data-stu-id="95c5f-184">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  



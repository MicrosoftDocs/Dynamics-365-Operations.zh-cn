---
title: 设计 ER 配置以填写 PDF 模板
description: 本主题介绍如何设计电子申报 (ER) 格式以填写 PDF 模板。
author: NickSelin
manager: AnnBe
ms.date: 04/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1ab6b6ae8a301e24751653dd74fad66417723360
ms.sourcegitcommit: 0400bfd66e98af50e64444a1c102575099a9312f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/09/2019
ms.locfileid: "1539172"
---
# <a name="design-er-configurations-to-fill-in-pdf-templates"></a><span data-ttu-id="a2d7c-103">设计 ER 配置以填写 PDF 模板</span><span class="sxs-lookup"><span data-stu-id="a2d7c-103">Design ER configurations to fill in PDF templates</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a2d7c-104">本主题中的过程为示例，用于演示**系统管理员**角色或**电子申报开发人员**角色的用户如何通过将可填写 PDF 文档用作报表模板来配置用于生成 PDF 文件格式报表的电子申报 (ER) 格式。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-104">The procedures in this topic are examples that show how a user in either the **System administrator** role or the **Electronic reporting developer** role can configure an Electronic reporting (ER) format that generates reports as PDF files by using fillable PDF documents as report templates.</span></span> <span data-ttu-id="a2d7c-105">Microsoft Dynamics 365 for Finance and Operations 或 Regulatory Configuration Services (RCS) 的任何公司都可以执行这些步骤。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-105">These steps can be performed in any company of Microsoft Dynamics 365 for Finance and Operations or Regulatory Configuration Services (RCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a2d7c-106">先决条件</span><span class="sxs-lookup"><span data-stu-id="a2d7c-106">Prerequisites</span></span>

<span data-ttu-id="a2d7c-107">首先，您必须具有下列访问权限类型之一，具体取决于您用于完成本主题中的过程的服务。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-107">Before you begin, you must have one of the following types of access, depending on the service that you use to complete the procedures in this topic:</span></span>

- <span data-ttu-id="a2d7c-108">访问 Finance and Operations 的以下其中一个角色：</span><span class="sxs-lookup"><span data-stu-id="a2d7c-108">Access to Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="a2d7c-109">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="a2d7c-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="a2d7c-110">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="a2d7c-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="a2d7c-111">系统管理员</span><span class="sxs-lookup"><span data-stu-id="a2d7c-111">System administrator</span></span>

- <span data-ttu-id="a2d7c-112">访问 RCS 的以下其中一个角色：</span><span class="sxs-lookup"><span data-stu-id="a2d7c-112">Access to RCS for one of the following roles:</span></span>

    - <span data-ttu-id="a2d7c-113">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="a2d7c-113">Electronic reporting developer</span></span>
    - <span data-ttu-id="a2d7c-114">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="a2d7c-114">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="a2d7c-115">系统管理员</span><span class="sxs-lookup"><span data-stu-id="a2d7c-115">System administrator</span></span>

<span data-ttu-id="a2d7c-116">还必须完成[创建一个配置提供程序，并标记其为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-116">You must also complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

<span data-ttu-id="a2d7c-117">最后，必须从 [CustomerSource](https://go.microsoft.com/fwlink/?linkid=874111) 下载下列文件。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-117">Finally, you must download the following files from [CustomerSource](https://go.microsoft.com/fwlink/?linkid=874111).</span></span>

| <span data-ttu-id="a2d7c-118">内容描述</span><span class="sxs-lookup"><span data-stu-id="a2d7c-118">Content description</span></span>                       | <span data-ttu-id="a2d7c-119">文件名</span><span class="sxs-lookup"><span data-stu-id="a2d7c-119">File name</span></span>                                     |
|-------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="a2d7c-120">报表第一页的模板</span><span class="sxs-lookup"><span data-stu-id="a2d7c-120">Template for the first page of the report</span></span> | [<span data-ttu-id="a2d7c-121">IntrastatReportTemplate1.pdf</span><span class="sxs-lookup"><span data-stu-id="a2d7c-121">IntrastatReportTemplate1.pdf</span></span>](https://mbs.microsoft.com/Files/public/CS)                  |
| <span data-ttu-id="a2d7c-122">报表其他页的模板</span><span class="sxs-lookup"><span data-stu-id="a2d7c-122">Template for other pages of the report</span></span>    | [<span data-ttu-id="a2d7c-123">IntrastatReportTemplate2.pdf</span><span class="sxs-lookup"><span data-stu-id="a2d7c-123">IntrastatReportTemplate2.pdf</span></span>](https://mbs.microsoft.com/Files/public/CS/AX/IntrastatReportTemplate2.pdf)                  |
| <span data-ttu-id="a2d7c-124">示例 ER 格式 - PDF</span><span class="sxs-lookup"><span data-stu-id="a2d7c-124">Sample ER format - PDF</span></span>                          | [<span data-ttu-id="a2d7c-125">Intrastat report (PDF).version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="a2d7c-125">Intrastat report (PDF).version.1.1.xml</span></span>](https://mbs.microsoft.com/Files/public/CS/AX/IntrastatreportPDFversion11.xml)        |
| <span data-ttu-id="a2d7c-126">示例 ER 格式 - Excel</span><span class="sxs-lookup"><span data-stu-id="a2d7c-126">Sample ER format - Excel</span></span>                          | [<span data-ttu-id="a2d7c-127">Intrastat (import from Excel).version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="a2d7c-127">Intrastat (import from Excel).version.1.1.xml</span></span>](https://mbs.microsoft.com/Files/public/CS/AX/IntrastatimportfromExcelversion11.xml) |
| <span data-ttu-id="a2d7c-128">示例数据集</span><span class="sxs-lookup"><span data-stu-id="a2d7c-128">Sample dataset</span></span>                            | [<span data-ttu-id="a2d7c-129">Intrastat sample data.xlsx</span><span class="sxs-lookup"><span data-stu-id="a2d7c-129">Intrastat sample data.xlsx</span></span>](https://mbs.microsoft.com/Files/public/CS/AX/Intrastatsampledata.xlsx)                    |

## <a name="design-the-format-configuration"></a><span data-ttu-id="a2d7c-130">设计 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="a2d7c-130">Design the format configuration</span></span>

### <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="a2d7c-131">访问 Microsoft 提供的配置列表</span><span class="sxs-lookup"><span data-stu-id="a2d7c-131">Get access to the list of configurations provided by Microsoft</span></span>

1. <span data-ttu-id="a2d7c-132">转到**组织管理 \> 工作区 \> 电子申报**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-132">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="a2d7c-133">确保提供商 **Litware 公司**可用且标记为有效。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-133">Make sure that the **Litware, Inc.** provider is available and marked as active.</span></span>
3. <span data-ttu-id="a2d7c-134">在 **Microsoft** 提供商的磁贴中，选择**存储库**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-134">On the tile for the **Microsoft** provider, select **Repositories**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a2d7c-135">如果已存在类型为 **LCS** 的存储库，请跳过此过程的其余步骤。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-135">If a repository of the **LCS** type already exists, skip the remaining steps of this procedure.</span></span>

4. <span data-ttu-id="a2d7c-136">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-136">Select **Add**.</span></span>
5. <span data-ttu-id="a2d7c-137">在下拉对话框中的**配置存储库类型**字段组中，选择 **LCS** 选项。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-137">In the drop-down dialog box, in the **Configuration repository type** field group, select the **LCS** option.</span></span>
6. <span data-ttu-id="a2d7c-138">选择**创建存储库**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-138">Select **Create repository**.</span></span>
7. <span data-ttu-id="a2d7c-139">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-139">Select **OK**.</span></span>

### <a name="get-the-model-configurations-provided-by-microsoft"></a><span data-ttu-id="a2d7c-140">获取 Microsoft 提供的模型配置</span><span class="sxs-lookup"><span data-stu-id="a2d7c-140">Get the model configurations provided by Microsoft</span></span>

1. <span data-ttu-id="a2d7c-141">在**配置存储库**页左侧，选择**显示筛选器**按钮（漏洞符号）。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-141">On the left side of the **Configuration repositories** page, select the **Show filters** button (the funnel symbol).</span></span>
2. <span data-ttu-id="a2d7c-142">在**类型**字段中添加 **LCS** 值的筛选器，然后使用**开头为**运算符。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-142">Add a filter for a value of **LCS** in the **Type** field, and use the **begins with** operator.</span></span>
3. <span data-ttu-id="a2d7c-143">选择**应用**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-143">Select **Apply**.</span></span>
4. <span data-ttu-id="a2d7c-144">选择**打开**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-144">Select **Open**.</span></span>
5. <span data-ttu-id="a2d7c-145">在树中，选择**内部统计模型**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-145">In the tree, select **Intrastat model**.</span></span>
6. <span data-ttu-id="a2d7c-146">在**版本**快速选项卡中，选择版本 **1**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-146">On the **Versions** FastTab, select version **1**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a2d7c-147">如果**版本**快速选项卡上的**导入**按钮不可用，请跳过此过程中的其余步骤。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-147">If the **Import** button on the **Versions** FastTab is unavailable, skip the remaining steps of this procedure.</span></span>

7. <span data-ttu-id="a2d7c-148">选择**导入**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-148">Select **Import**.</span></span>
8. <span data-ttu-id="a2d7c-149">选择**是**确认导入所选版本的**内部统计模型**模型配置。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-149">Select **Yes** to confirm the import of the selected version of the **Intrastat model** model configuration.</span></span>

### <a name="create-a-new-format-configuration"></a><span data-ttu-id="a2d7c-150">创建新的格式配置</span><span class="sxs-lookup"><span data-stu-id="a2d7c-150">Create a new format configuration</span></span>

1. <span data-ttu-id="a2d7c-151">在**电子申报**工作区中，选择**报告配置**磁贴。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-151">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="a2d7c-152">在树中，选择**内部统计模型**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-152">In the tree, select **Intrastat model**.</span></span>
3. <span data-ttu-id="a2d7c-153">选择**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-153">Select **Create configuration**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a2d7c-154">如果**创建配置**按钮不可用，必须在可从**电子申报**工作区打开的**电子申报参数**页中开启设计模式。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-154">If the **Create configuration** button isn't available, you must turn on design mode on the **Electronic reporting parameters** page that can be opened from the **Electronic reporting** workspace.</span></span>

4. <span data-ttu-id="a2d7c-155">在下拉对话框中的**新建**字段组中，选择**基于数据模型内部统计的格式**选项。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-155">In the drop-down dialog box, in the **New** field group, select the **Format based on data model Intrastat** option.</span></span>
5. <span data-ttu-id="a2d7c-156">在**名称** 字段中，输入 **Intrastat report (PDF)**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-156">In the **Name** field, enter **Intrastat report (PDF)**.</span></span>
6. <span data-ttu-id="a2d7c-157">在**说明**字段中，输入 **PDF 格式的内部统计报表**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-157">In the **Description** field, enter **Intrastat report in PDF format**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a2d7c-158">将自动输入有效配置提供商。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-158">The active configuration provider is automatically entered.</span></span> <span data-ttu-id="a2d7c-159">此提供商可以维护此配置。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-159">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="a2d7c-160">尽管其他提供商可以使用此配置，但不能对其进行维护。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-160">Although other providers can use this configuration, they won't be able to maintain it.</span></span>

7. <span data-ttu-id="a2d7c-161">可选：在**格式类型**字段中，可选择电子文档的具体格式。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-161">Optional: In the **Format type** field, you can select a specific format of electronic document.</span></span> <span data-ttu-id="a2d7c-162">如果选择 **PDF**，设计时，ER Operations 设计器将仅提供仅适用于以 PDF 格式生成的文档的格式元素（**PDF\文件**、**PDF\PDF 合并器**等）。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-162">If you select **PDF**, at design time, the ER Operations designer will offer just the format elements that are applicable only to documents that are generated in PDF format (**PDF\File**, **PDF\PDF Merger**, etc.).</span></span> <span data-ttu-id="a2d7c-163">如果将此字段留空，将在设计时添加第一个格式元素期间在 ER Operations 设计器中指定电子文档的格式。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-163">If you leave this field blank, a format of electronic document will be specified at design time in the ER Operations designer when a first format element will be added.</span></span> <span data-ttu-id="a2d7c-164">例如，如果添加 **Excel\File** 作为第一个格式元素，ER Operations 设计器将仅提供仅适用于以 Excel 格式生成的文档的格式元素（**Excel\单元格**、**Excel\区域**等）。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-164">For example, if you add the **Excel\File** as the first format element, the ER Operations designer will offer you just the format elements that are applicable only to documents that are generated in Excel format (**Excel\Cell**, **Excel\Range**, etc.).</span></span> <span data-ttu-id="a2d7c-165">格式。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-165">format.</span></span>
8. <span data-ttu-id="a2d7c-166">选择**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-166">Select **Create configuration**.</span></span>

<span data-ttu-id="a2d7c-167">将创建新的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-167">A new ER format configuration is created.</span></span> <span data-ttu-id="a2d7c-168">可使用此配置的草稿版本来存储为了生成 PDF 格式的电子文档而设计的 ER 格式组件。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-168">You can use the draft version of this configuration to store the ER format component that is designed to generate electronic documents in PDF format.</span></span>

### <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="a2d7c-169">设计电子单据的格式</span><span class="sxs-lookup"><span data-stu-id="a2d7c-169">Design the format of an electronic document</span></span>

<span data-ttu-id="a2d7c-170">接下来，在创建的 ER 格式配置中，将设计用于生成 PDF 格式的**内部统计控件**报表的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-170">Next, in the ER format configuration that you created, you will design the ER format that generates the **Intrastat control** report in PDF format.</span></span> <span data-ttu-id="a2d7c-171">此报表第一页显示报表摘要和报告的外贸交易记录的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-171">The first page of this report must show a summary of the report and details of the foreign trade transactions that are reported on.</span></span> <span data-ttu-id="a2d7c-172">其他页必须仅显示报告的外贸交易记录的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-172">The other pages must show only details of the foreign trade transactions that are reported on.</span></span> <span data-ttu-id="a2d7c-173">由于生成的报表页必须采用不同布局，所以将在 ER 格式中使用 PDF 格式的两个不同模板。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-173">Because the report pages that are generated must have different layouts, two different templates in PDF format will be used in the ER format.</span></span>

<span data-ttu-id="a2d7c-174">在任何 PDF 查看器中，打开下载的 PDF 模板。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-174">In any PDF viewer, open the PDF templates that you downloaded.</span></span> <span data-ttu-id="a2d7c-175">请注意，每个模板中包含多个必须填写的字段。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-175">Notice that each template contains multiple fields that must be filled in.</span></span> <span data-ttu-id="a2d7c-176">在每个模板中，外贸交易记录的详细信息表示为 42 行，每行九个字段。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-176">In each template, details of foreign trade transactions are presented as 42 rows, each of which has nine fields.</span></span> <span data-ttu-id="a2d7c-177">行号在每个字段名称的默认显示（如**日期 1**…**日期 42** 和 **商品 1**…**商品 42**）。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-177">The row number appears at the end of each field's name (for example, **Date 1**…**Date 42** and **Commodity 1**…**Commodity 42**).</span></span>

<span data-ttu-id="a2d7c-178">下图显示报表第一页的 PDF 模板。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-178">The following illustration shows the PDF template for the first page of the report.</span></span>

![模板 1](media/rcs-ger-filloutpdf-template1.png)

<span data-ttu-id="a2d7c-180">下图显示报表其他页的 PDF 模板。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-180">The following illustration shows the PDF template for other pages of the report.</span></span>

![模板 2](media/rcs-ger-filloutpdf-template2.png)

1. <span data-ttu-id="a2d7c-182">在**配置**页上，选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-182">On the **Configurations** page, select **Designer**.</span></span>
2. <span data-ttu-id="a2d7c-183">选择**添加根**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-183">Select **Add root**.</span></span>
3. <span data-ttu-id="a2d7c-184">在下拉对话框中的树中，选择 **PDF \> PDF 合并器**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-184">In the drop-down dialog box, in the tree, select **PDF \> PDF Merger**.</span></span>

    <span data-ttu-id="a2d7c-185">如果格式的根元素选择 **PDF 合并器**元素，则在运行时生成的所有 PDF 文档都将合并为一个最终的 PDF 文档。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-185">When you select the **PDF Merger** element as the root element of the format, all PDF documents that are generated at run time will be merged into a single final PDF document.</span></span> <span data-ttu-id="a2d7c-186">如果仅需要一个 PDF 模板来使用您设计的 ER 格式生成需要的所有文档，根元素可选择 **PDF 文件**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-186">If you need only one PDF template to generate all the required documents by using the ER format that you design, you can select **PDF file** as the root element.</span></span>

4. <span data-ttu-id="a2d7c-187">在**名称**字段中，输入**输出**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-187">In the **Name** field, enter **Output**.</span></span>
5. <span data-ttu-id="a2d7c-188">在**语言首选项**字段中，选择**用户首选项**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-188">In the **Language preferences** field, select **User preference**.</span></span> <span data-ttu-id="a2d7c-189">将使用运行报表的用户的首选语言生成报表。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-189">The report will be generated in the preferred language of the user who runs it.</span></span>
6. <span data-ttu-id="a2d7c-190">在**区域性首选项**字段中，选择**用户首选项**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-190">In the **Culture preferences** field, select **User preference**.</span></span> <span data-ttu-id="a2d7c-191">将根据运行报表的用户的首选区域设置来设置报表页中显示的值和日期。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-191">Values and dates that are presented on the pages of the report will be formatted based on the preferred locale of the user who runs the report.</span></span>
7. <span data-ttu-id="a2d7c-192">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-192">Select **OK**.</span></span>
8. <span data-ttu-id="a2d7c-193">在操作窗格上的**导入**选项卡上，选择**从 PDF 导入**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-193">On the Action Pane, on the **Import** tab, select **Import from PDF**.</span></span>

    <span data-ttu-id="a2d7c-194">将可填写 PDF 文档作为此 ER 格式的模板导入时，将根据导入的 PDF 文档的结构以设计的格式自动创建所有必需的 ER 格式元素（**PDF 文件**、**字段组**和**字段**元素）。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-194">When a fillable PDF document is imported as a template for this ER format, all the required ER format elements (**PDF file**, **Field group**, and **Field** elements) are automatically created in the format that is designed, based on the structure of the PDF document that is imported.</span></span>

9. <span data-ttu-id="a2d7c-195">选择**浏览**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-195">Select **Browse**.</span></span> <span data-ttu-id="a2d7c-196">导航到并选择之前作为先决条件下载的 **IntrastatReportTemplate1.pdf** 文件。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-196">Navigate to and select the **IntrastatReportTemplate1.pdf** file that you downloaded earlier as a prerequisite.</span></span>
10. <span data-ttu-id="a2d7c-197">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-197">Select **OK**.</span></span>

    <span data-ttu-id="a2d7c-198">将加载所选文件，并填写**从 PDF 导入**对话框中的**模板**字段。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-198">The selected file is loaded, and the **Template** field in the **Import from PDF** dialog box is filled in.</span></span>

11. <span data-ttu-id="a2d7c-199">将**组字段**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-199">Set the **Group fields** option to **Yes**.</span></span> <span data-ttu-id="a2d7c-200">如果所选 PDF 文档中包含任何字段组，将使用这些字段组来为创建的 ER 格式元素分组。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-200">If the selected PDF document contains any field groups, they will be used to group the ER format elements that are created.</span></span> <span data-ttu-id="a2d7c-201">将为此目的创建一个**字段组**格式元素。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-201">A **Field group** format element will be created for this purpose.</span></span>

    <span data-ttu-id="a2d7c-202">如果此选项设置为**否**，将把所需 ER 格式元素创建为创建的 **PDF 文件**格式元素下嵌套的元素的简单列表。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-202">If this option is set to **No**, the required ER format elements will be created as a flat list of elements that are nested under the **PDF File** format element that is created.</span></span>

12. <span data-ttu-id="a2d7c-203">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-203">Select **OK**.</span></span>

    ![“从 PDF 导入”对话框](media/rcs-ger-filloutpdf-importtemplate.png)

13. <span data-ttu-id="a2d7c-205">在树中，展开**输出**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-205">In the tree, expand **Output**.</span></span>

    <span data-ttu-id="a2d7c-206">请注意，已自动创建了 **PDF 文件**组件来管理运行时生成的报表的第一页的创建。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-206">Notice that the **PDF File** component has been automatically created to manage the creation of the first page of the report that is generated at run time.</span></span>

14. <span data-ttu-id="a2d7c-207">在树中，展开**输出 \> PDF 文件**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-207">In the tree, expand **Output \> PDF File**.</span></span>

    <span data-ttu-id="a2d7c-208">请注意，已根据前面导入的可填写 PDF 文档的结构使用此 Er 格式自动创建了结构化的格式元素列表。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-208">Notice that the structured list of format elements has been automatically created in this ER format, based on the structure of the fillable PDF document that you imported earlier.</span></span>

15. <span data-ttu-id="a2d7c-209">在树中，选择**输出 \> PDF 文件**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-209">In the tree, select **Output \> PDF File**.</span></span>
16. <span data-ttu-id="a2d7c-210">在**名称**字段中，输入**第 1 页**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-210">In the **Name** field, enter **Page 1**.</span></span>

    <span data-ttu-id="a2d7c-211">此格式将用于生成**内部统计控件**报表的第一页。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-211">This format element will be used to generate the first page of the **Intrastat control** report.</span></span> <span data-ttu-id="a2d7c-212">此页将显示报表摘要和外贸交易记录的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-212">That page will show a summary of the report and details of foreign trade transactions.</span></span>

    <span data-ttu-id="a2d7c-213">如果使**语言首选项**字段留空，**PDF 合并器**父元素的**语言首选项**设置将决定通过使用此格式元素生成的报表的语言。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-213">If you leave the **Language preferences** field blank, the **Language preferences** setting of the parent **PDF Merger** element will determine the language of the report that is generated by using this format element.</span></span> <span data-ttu-id="a2d7c-214">可选择其他值替换父元素的设置。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-214">You can select another value to override the setting of the parent element.</span></span>

    <span data-ttu-id="a2d7c-215">如果使**区域性首选项**字段留空，**PDF 合并器**父元素的**区域性首选项**设置将决定通过使用此格式元素生成的报表的语言。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-215">If you leave the **Culture preferences** field blank, the **Culture preferences** setting of the parent **PDF Merger** element will determine the locale of the report that is generated by using this format element.</span></span> <span data-ttu-id="a2d7c-216">区域设置决定报表页中的值和日期的格式。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-216">The locale determines the format of values and dates on the pages of the report.</span></span> <span data-ttu-id="a2d7c-217">可选择其他值替换父元素的设置。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-217">You can select another value to override the setting of the parent element.</span></span>

17. <span data-ttu-id="a2d7c-218">在操作窗格中，选择**导入**选项卡。请注意，**从 PDF 更新**按钮已变为可用于所选格式元素 **PDF 文件**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-218">On the Action Pane, select the **Import** tab. Notice that the **Update from PDF** button has become available for selected format element, **PDF File**.</span></span>

    <span data-ttu-id="a2d7c-219">可使用此按钮将更新后的 PDF 模板导入到编辑后的格式。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-219">You can use this button to import the updated PDF template to the edited format.</span></span> <span data-ttu-id="a2d7c-220">导入更新后的 PDF 模板时，将相应更改格式元素列表：</span><span class="sxs-lookup"><span data-stu-id="a2d7c-220">When the updated PDF template is imported, the list of format elements will be changed accordingly:</span></span>

    - <span data-ttu-id="a2d7c-221">对于更新后的 PDF 模板中的任何新字段，将使用编辑后的 ER 格式创建新的格式元素。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-221">For any new fields in the updated PDF template, new format elements are created in the edited ER format.</span></span>
    - <span data-ttu-id="a2d7c-222">如果更新后的 PDF 模板中不再包含与编辑后的 ER 格式的任何现有格式元素对应的字段，将从 ER 格式删除这些格式元素。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-222">If the updated PDF template no longer includes fields that correspond to any existing format elements in the edited ER format, those format elements are deleted from the ER format.</span></span>

18. <span data-ttu-id="a2d7c-223">在**格式**选项卡中，选择**附件**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-223">On the **Format** tab, select **Attachments**.</span></span>

    <span data-ttu-id="a2d7c-224">请注意，导入的 PDF 文档已附加到编辑后的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-224">Notice that the imported PDF document is attached to the edited ER format.</span></span>

    ![PDF 附件预览](media/rcs-ger-filloutpdf-attachedtemplate.png)

19. <span data-ttu-id="a2d7c-226">继续设计此格式，方法是导入第二个 PDF 模板，向数据源添加必要的绑定等。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-226">Continue to design this format by importing the second PDF template, adding necessary bindings to data sources, and so on.</span></span>
20. <span data-ttu-id="a2d7c-227">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-227">Select **Save**.</span></span>
21. <span data-ttu-id="a2d7c-228">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-228">Close the page.</span></span>
22. <span data-ttu-id="a2d7c-229">选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-229">Select **Delete**.</span></span>
23. <span data-ttu-id="a2d7c-230">选择**是**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-230">Select **Yes**.</span></span>

<span data-ttu-id="a2d7c-231">若要了解如何使用 **PDF 合并器**、**PDF 文件**、**字段组**和**字段**格式元素生成 PDF 格式的文档，可导入和分析示例 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-231">To learn how new **PDF Merger**, **PDF File**, **Field group** and **Field** format elements can be used to generate documents in PDF format, you can import and analyze the sample ER format.</span></span>

### <a name="import-the-format-configuration"></a><span data-ttu-id="a2d7c-232">导入格式配置</span><span class="sxs-lookup"><span data-stu-id="a2d7c-232">Import the format configuration</span></span>

<span data-ttu-id="a2d7c-233">接下来，将导入之前下载的示例 ER 格式以生成 PDF 格式的**内部统计控件**报表。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-233">Next, you will import the sample ER format that you previously downloaded to generate the **Intrastat control** report in PDF format.</span></span> <span data-ttu-id="a2d7c-234">报表第一页显示报表摘要和报告的外贸交易记录的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-234">The first page of the report must show a summary of the report and details of the foreign trade transactions that are reported on.</span></span> <span data-ttu-id="a2d7c-235">其他页必须仅显示报告的外贸交易记录的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-235">The other pages must show only details of the foreign trade transactions that are reported on.</span></span>

1. <span data-ttu-id="a2d7c-236">在**配置**页中，选择**交换 \> 从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-236">On the **Configurations** page, select **Exchange \> Load from XML file**.</span></span>
2. <span data-ttu-id="a2d7c-237">选择**浏览**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-237">Select **Browse**.</span></span> <span data-ttu-id="a2d7c-238">导航到并选择之前作为先决条件下载的 **Intrastat report (PDF).version.1.1.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-238">Navigate to and select the **Intrastat report (PDF).version.1.1.xml** file that you downloaded earlier as a prerequisite.</span></span>
3. <span data-ttu-id="a2d7c-239">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-239">Select **OK**.</span></span>

## <a name="analyze-the-format-configuration"></a><span data-ttu-id="a2d7c-240">分析格式配置</span><span class="sxs-lookup"><span data-stu-id="a2d7c-240">Analyze the format configuration</span></span>

### <a name="format-layout"></a><span data-ttu-id="a2d7c-241">格式布局</span><span class="sxs-lookup"><span data-stu-id="a2d7c-241">Format layout</span></span>

1. <span data-ttu-id="a2d7c-242">在**配置**页上的树中，选择**内部统计模型 \> 内部统计报表 (PDF)**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-242">On the **Configurations** page, in the tree, select **Intrastat model \> Intrastat report (PDF)**.</span></span>
2. <span data-ttu-id="a2d7c-243">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-243">Select **Designer**.</span></span>
3. <span data-ttu-id="a2d7c-244">选择**显示详细信息**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-244">Select **Show details**.</span></span>
4. <span data-ttu-id="a2d7c-245">在树中，展开**输出：PDF 合并器**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-245">In the tree, expand **Output: PDF Merger**.</span></span>

    <span data-ttu-id="a2d7c-246">请注意，此 ER 格式中包含两个 **PDF 文件**元素，其中每个使用一个不同的 PDF 模板。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-246">Notice that this ER format contains two **PDF File** elements, each of which uses a different PDF template.</span></span> <span data-ttu-id="a2d7c-247">一个模板用于生成 PDF 格式的报表第一页，另一个模板用于生成其他页。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-247">One template is used to generate the first page of the report in PDF format, and the other template is used to generate the other pages.</span></span>

5. <span data-ttu-id="a2d7c-248">在树中，展开**输出：PDF 合并器 \> 第 1 页：PDF 文件 (IntrastatReportTemplate1)**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-248">In the tree, expand **Output: PDF Merger \> Page 1: PDF File (IntrastatReportTemplate1)**.</span></span>
6. <span data-ttu-id="a2d7c-249">在树中，展开**输出：PDF 合并器 \> 第 N 页：PDF 文件 (IntrastatReportTemplate2)**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-249">In the tree, expand **Output: PDF Merger \> Page N: PDF File (IntrastatReportTemplate2)**.</span></span>

    <span data-ttu-id="a2d7c-250">请注意，由于这两个 PDF 模板的内容不同，所以这两个 **PDF 文件**元素的嵌套格式元素的结构也不同。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-250">Notice that, because the content of the two PDF templates differs, the structure of the nested format elements for the two **PDF File** elements also differs.</span></span>

### <a name="format-mapping"></a><span data-ttu-id="a2d7c-251">格式映射</span><span class="sxs-lookup"><span data-stu-id="a2d7c-251">Format mapping</span></span>

1. <span data-ttu-id="a2d7c-252">在**格式设计器**页中，选择**映射**选项卡。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-252">On the **Format designer** page, select the **Mapping** tab.</span></span>
2. <span data-ttu-id="a2d7c-253">在树中，展开**分页 \> 页面**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-253">In the tree, expand **Paging \> Pages**.</span></span>

    ![其中展开了模型树的配方设计器页](media/rcs-ger-filloutpdf-reviewformat.png)

    <span data-ttu-id="a2d7c-255">注意以下详细信息：</span><span class="sxs-lookup"><span data-stu-id="a2d7c-255">Note the following details:</span></span>

    - <span data-ttu-id="a2d7c-256">**PDF 文件**类型的**输出 \> 第 1 页**格式元素为绑定到任何数据源，并且此格式元素的 **Enabled** 表达式为空。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-256">The **Output \> Page 1** format element of the **PDF File** type isn't bound to any data source, and the **Enabled** expression of this format element is empty.</span></span> <span data-ttu-id="a2d7c-257">因此，运行时生成单个 PDF 文档期间，**IntrastatReportTemplate1** PDF 模板仅填充一次。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-257">Therefore, at run time, the **IntrastatReportTemplate1** PDF template will be filled in only one time when an individual PDF document is generated.</span></span>
    - <span data-ttu-id="a2d7c-258">**PDF 文件**类型的**输出 \> 第 N 页**格式元素绑定到**记录列表**类型的 **Paging.PageN** 数据源，并且此格式元素的 **Enabled** 表达式为空。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-258">The **Output \> Page N** format element of the **PDF File** type is bound to the **Paging.PageN** data source of the **Record list** type, and the **Enabled** expression of this format element is empty.</span></span> <span data-ttu-id="a2d7c-259">因此，运行时生成单个 PDF 文档期间，将为绑定的记录列表中的每个记录填充 **IntrastatReportTemplate2** PDF 模板。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-259">Therefore, at run time, the **IntrastatReportTemplate2** PDF template will be filled in for each record from the bound record list when an individual PDF document is generated.</span></span>
    - <span data-ttu-id="a2d7c-260">因为**第 1 页：PDF 文件**和**第 N 页：PDF 文件**格式元素是**输出：PDF 合并器**格式元素的子代，所以将把填写的所有 PDF 文档合并为一个最终的 PDF 文档。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-260">Because the **Page 1: PDF File** and **Page N: PDF File** format elements are children of the **Output: PDF Merger** format element, all PDF documents that are filled in will be merged into a single final PDF document.</span></span>
    - <span data-ttu-id="a2d7c-261">**Paging.Page1** 和 **Paging.PageN** 数据源配置为 **Paging.Pages** 数据源中的记录的筛选器。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-261">The **Paging.Page1** and **Paging.PageN** data sources are configured as filters of records from the **Paging.Pages** data source.</span></span> <span data-ttu-id="a2d7c-262">配置此数据源是为了将整组外贸交易记录拆分为批次。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-262">This data source is configured to split the whole set of foreign trade transactions into batches.</span></span> <span data-ttu-id="a2d7c-263">每个批次最多包含 42 条记录。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-263">Each batch contains up to 42 records.</span></span> <span data-ttu-id="a2d7c-264">下面的 ER 表达式用于将交易记录拆分为批次：</span><span class="sxs-lookup"><span data-stu-id="a2d7c-264">The following ER expression is used to split the transactions into batches:</span></span>

        <span data-ttu-id="a2d7c-265">SPLITLIST(Totals.CommodityRecord,42)</span><span class="sxs-lookup"><span data-stu-id="a2d7c-265">SPLITLIST(Totals.CommodityRecord,42)</span></span>

    - <span data-ttu-id="a2d7c-266">**Paging.Pages** 数据源中包含 **Paging.Pages.Enumerated** 元素，用于返回批次中包含的每个记录的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-266">The **Paging.Pages** data source contains the **Paging.Pages.Enumerated** element that returns the details of each record that is included in a batch.</span></span> <span data-ttu-id="a2d7c-267">这些详细信息中包含该记录在当前批次（**Paging.Pages.Enumerated.Number** 字段）中的序号。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-267">These details include the record's sequence in the current batch (the **Paging.Pages.Enumerated.Number** field).</span></span> <span data-ttu-id="a2d7c-268">**Paging.Pages.Enumerated.Number** 字段在 **PDF 字段**格式元素的 **Name** 表达式中用于动态生成基于批次中的交易记录号的字段名。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-268">The **Paging.Pages.Enumerated.Number** field is used in the **Name** expression of **PDF Field** format elements to dynamically generate a field name that is based on the transaction number in a batch.</span></span> <span data-ttu-id="a2d7c-269">然后将生成的字段名用于填写所用 PDF 模板中的正确 PDF 字段。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-269">The field name that is generated is then used to fill in the correct PDF field in the PDF template that is used.</span></span>
    - <span data-ttu-id="a2d7c-270">**PDF 组**类型的**输出 \> 第 N 页 \> 详细信息 2** 格式元素绑定到**记录列表**类型的 **Paging.PageN.Enumerated** 数据源（如果使用的是**相对路径**视图模式，则为 **\@.Enumerated**）。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-270">The **Output \> Page N \> Details 2** format element of the **PDF Group** type is bound to the **Paging.PageN.Enumerated** data source (or **\@.Enumerated** if the **Relative path** view mode is used) of the **Record list** type.</span></span> <span data-ttu-id="a2d7c-271">因此，在运行时，将为绑定的记录列表中的每个记录填写此 PDF 组的嵌套元素。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-271">Therefore, at run time, the nested elements of this PDF group will be filled in for each record from the bound record list.</span></span> <span data-ttu-id="a2d7c-272">这样，最终在为 **Paging.PageN.Enumerated** 列表的 42 个记录中的第 N 个填写以下 PDF 字段时，将生成单个 PDF 行：日期 N、方向 N、商品 N 等。因此，在这方面，此**字段组**格式元素的行为类似 **XML \> 序列**和**文本 \> 序列**格式元素的行为类似。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-272">In this way, individual PDF lines are virtually generated when for each Nth of 42 records of the **Paging.PageN.Enumerated** list the following PDF fields are filled in: Date N, Direction N, Commodity N, etc. Therefore, in this respect, the behavior of this **Field group** format element resembles the behavior of the **XML \> Sequence** and **Text \> Sequence** format elements.</span></span>

3. <span data-ttu-id="a2d7c-273">在树中，展开**输出 \> 第 N 页\> 详细信息 2**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-273">In the tree, expand **Output \> Page N \> Details2**.</span></span>
4. <span data-ttu-id="a2d7c-274">在树中，选择**输出 \> 第 N 页\> 详细信息 2 \> PageFooter**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-274">In the tree, select **Output \> Page N \> Details2 \> PageFooter**.</span></span>

    <span data-ttu-id="a2d7c-275">请注意，此格式元素的**名称**属性定义为 **PageFooter**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-275">Notice that the **Name** attribute of this format element is defined as **PageFooter**.</span></span> <span data-ttu-id="a2d7c-276">另请注意，格式元素的 **Name** 表达式为空。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-276">Also notice that the **Name** expression of the format element is empty.</span></span>

5. <span data-ttu-id="a2d7c-277">在树中，选择**输出 \> 第 N 页\> 详细信息 2 \> Correction 1**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-277">In the tree, select **Output \> Page N \> Details2 \> Correction 1**.</span></span>

    <span data-ttu-id="a2d7c-278">请注意，此格式元素的**名称**属性定义为 **Correction 1**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-278">Notice that the **Name** attribute of this format element is defined as **Correction 1**.</span></span> <span data-ttu-id="a2d7c-279">另请注意，格式元素的 **Name** 表达式定义为 **Paging.FldName("Correction",\@.Number)**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-279">Also notice that the **Name** expression of the format element is defined as **Paging.FldName("Correction",\@.Number)**.</span></span>

![其中选择了映射的格式设计器](media/rcs-ger-filloutpdf-reviewformat2.png)

<span data-ttu-id="a2d7c-281">请注意，**字段**格式元素用于填写定义为 **PDF 文件**格式父元素的模板的可填写 PDF 文档的单个字段。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-281">Note that the **Field** format element is used to fill in an individual field of a fillable PDF document that is defined as a template of the parent **PDF File** format element.</span></span> <span data-ttu-id="a2d7c-282">**PDF 文件**格式元素或其嵌套元素（如果有任何嵌套元素）的绑定指定在相应 PDF 字段中输入的值。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-282">The binding of the **PDF File** format element or its nested elements, if it has any nested elements, specifies the value that is entered in corresponding PDF fields.</span></span> <span data-ttu-id="a2d7c-283">**字段**格式元素的不同属性可用于指定单个格式元素填充哪个 PDF 字段：</span><span class="sxs-lookup"><span data-stu-id="a2d7c-283">Different properties of the **Field** format element can be used to specify which PDF field is filled in by an individual format element:</span></span>

- <span data-ttu-id="a2d7c-284">**格式**选项卡上的格式元素的 **Name** 属性</span><span class="sxs-lookup"><span data-stu-id="a2d7c-284">On the **Format** tab, the **Name** attribute of the format element</span></span>
- <span data-ttu-id="a2d7c-285">**映射**选项卡上的格式元素的 **Name** 表达式</span><span class="sxs-lookup"><span data-stu-id="a2d7c-285">On the **Mapping** tab, the **Name** expression of the format element</span></span>

<span data-ttu-id="a2d7c-286">因为这两个属性是**字段**格式元素的可选属性，所以将把下列规则应用于目标 PDF 字段：</span><span class="sxs-lookup"><span data-stu-id="a2d7c-286">Because both properties are optional for a **Field** format element, the following rules are applied to specify the target PDF field:</span></span>

- <span data-ttu-id="a2d7c-287">如果 **Name** 属性为空，而 **Name** 表达式在运行时返回空字符串，则在运行时引发异常以通知用户在正用于填写 PDF 文档的 PDF 模板中无法找到 PDF 字段。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-287">If the **Name** attribute is blank, and the **Name** expression returns an empty string at run time, an exception is thrown at run time to notify the user that a PDF field can't be found in the PDF template that is being used to fill in the PDF document.</span></span>
- <span data-ttu-id="a2d7c-288">如果定义了 **Name** 属性，并且 **Name** 表达式为空，则将填写与格式元素的 **Name** 属性同名的 PDF 字段。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-288">If the **Name** attribute is defined, and the **Name** expression is blank, the PDF field that has the same name as the **Name** attribute of the format element is filled in.</span></span>
- <span data-ttu-id="a2d7c-289">如果定义了 **Name** 属性，并且配置了 **Name** 表达式，则将填写与格式元素的 **Name** 表达式返回的值同名的 PDF 字段。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-289">If the **Name** attribute is defined, and the **Name** expression is configured, the PDF field that the same name as the value that is returned by the **Name** expression of the format element is filled in.</span></span>

> [!NOTE]
> <span data-ttu-id="a2d7c-290">可按照下面的方法选择的内容填写 PDF 复选框：</span><span class="sxs-lookup"><span data-stu-id="a2d7c-290">A PDF check box can be filled in as selected in the following ways:</span></span>
>
> - <span data-ttu-id="a2d7c-291">如果相应的**字段**格式元素绑定到值为 **True** 的**布尔值**数据类型的数据源字段</span><span class="sxs-lookup"><span data-stu-id="a2d7c-291">When the corresponding **Field** format element is bound to a data source field of the **Boolean** data type that has the **True** value</span></span>
> - <span data-ttu-id="a2d7c-292">如果相应的**字段**格式元素中包含绑定到文本值为 **1**、**True** 或 **Yes** 的数据源字段的嵌套**字符串**格式元素</span><span class="sxs-lookup"><span data-stu-id="a2d7c-292">When the corresponding **Field** format element contains a nested **String** format element that is bound to a data source field that has a text value of **1**, **True**, or **Yes**</span></span>

## <a name="run-the-format-configuration"></a><span data-ttu-id="a2d7c-293">运行格式配置</span><span class="sxs-lookup"><span data-stu-id="a2d7c-293">Run the format configuration</span></span>

### <a name="import-the-format-configuration"></a><span data-ttu-id="a2d7c-294">导入格式配置</span><span class="sxs-lookup"><span data-stu-id="a2d7c-294">Import the format configuration</span></span>

<span data-ttu-id="a2d7c-295">接下来，将加载**内部统计（从 Excel 导入）** 示例 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-295">Next, you will load the **Intrastat (import from Excel)** sample ER format.</span></span> <span data-ttu-id="a2d7c-296">此格式用于解析用户选择来模拟外贸交易记录的 Microsoft Excel 工作簿。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-296">This format is designed to parse a user-selected Microsoft Excel workbook that simulates foreign trade transactions.</span></span>

1. <span data-ttu-id="a2d7c-297">在**配置**页中，选择**交换 \> 从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-297">On the **Configurations** page, select **Exchange \> Load from XML file**.</span></span>
2. <span data-ttu-id="a2d7c-298">选择**浏览**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-298">Select **Browse**.</span></span> <span data-ttu-id="a2d7c-299">导航到并选择之前作为先决条件下载的 **Intrastat (import from Excel).version.1.1.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-299">Navigate to and select the **Intrastat (import from Excel).version.1.1.xml** file that you downloaded earlier as a prerequisite.</span></span>
3. <span data-ttu-id="a2d7c-300">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-300">Select **OK**.</span></span>
4. <span data-ttu-id="a2d7c-301">在树中，选择**内部统计模型 \> 内部统计（从 Excel 导入）**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-301">In the tree, select **Intrastat model \> Intrastat (import from Excel)**.</span></span>
5. <span data-ttu-id="a2d7c-302">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-302">Select **Edit**.</span></span>
6. <span data-ttu-id="a2d7c-303">将**模型映射的默认值**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-303">Set the **Default for model mapping** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a2d7c-304">如果之前将**内部统计模型**配置或**内部统计模型**配置下嵌套的另一个配置的**模型映射的默认值**选项设置为**是**，请将此选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-304">If you previously set the **Default for model mapping** option to **Yes** for the **Intrastat model** configuration or another configuration that is nested under the **Intrastat model** configuration, set this option to **No**.</span></span>

    <span data-ttu-id="a2d7c-305">如果**模型映射的默认值**选项设置为**是**，则将导入的**内部统计（从 Excel 导入）** ER 格式指定为**内部统计报表 (PDF)** 格式配置的默认数据源。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-305">When the **Default for model mapping** option is set to **Yes**, the imported **Intrastat (import from Excel)** ER format is assigned as the default data source for the **Intrastat report (PDF)** format configuration.</span></span> <span data-ttu-id="a2d7c-306">然后，在运行**内部统计报表 (PDF)** 格式配置时，**内部统计（从 Excel 导入）** ER 格式解析的 Excel 工作簿的内容将模拟必须报告的外贸交易记录。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-306">Then, when the **Intrastat report (PDF)** format configuration is run, the content of the Excel workbook that is parsed by the **Intrastat (import from Excel)** ER format will simulate foreign trade transactions that must be reported.</span></span> <span data-ttu-id="a2d7c-307">下图显示了一个 Excel 工作簿的示例。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-307">The following illustration shows an example of an Excel workbook.</span></span>

    ![包含示例数据的 Excel 工作簿](media/rcs-ger-filloutpdf-excelworkbook.png)

### <a name="run-the-format-configuration"></a><span data-ttu-id="a2d7c-309">运行格式配置</span><span class="sxs-lookup"><span data-stu-id="a2d7c-309">Run the format configuration</span></span>

1. <span data-ttu-id="a2d7c-310">在**配置**页上的树中，选择**内部统计模型 \> 内部统计报表 (PDF)**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-310">On the **Configurations** page, in the tree, select **Intrastat model \> Intrastat report (PDF)**.</span></span>
2. <span data-ttu-id="a2d7c-311">选择**运行**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-311">Select **Run**.</span></span>
3. <span data-ttu-id="a2d7c-312">选择**浏览**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-312">Select **Browse**.</span></span> <span data-ttu-id="a2d7c-313">导航到并选择之前作为先决条件下载的 **Intrastat sample data.xlsx** 文件。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-313">Navigate to and select the **Intrastat sample data.xlsx** file that you downloaded earlier as a prerequisite.</span></span>
4. <span data-ttu-id="a2d7c-314">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-314">Select **OK**.</span></span>
5. <span data-ttu-id="a2d7c-315">在**报表方向**字段中，选择**双向**以填写来自生成的 PDF 报表中导入的 Excel 工作簿内的所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-315">In the **Report direction** field, select **Both** to fill in all transactions from the imported Excel workbook in the PDF report that is generated.</span></span>
6. <span data-ttu-id="a2d7c-316">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-316">Select **OK**.</span></span>
7. <span data-ttu-id="a2d7c-317">查看生成的 PDF 文档。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-317">Review the PDF document that is generated.</span></span>

<span data-ttu-id="a2d7c-318">下图显示生成的报表的第一页的示例。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-318">The follow illustration shows an example of the first page of the report that is generated.</span></span>

![生成的报表的第一页](media/rcs-ger-filloutpdf-generatedreport.png)

<span data-ttu-id="a2d7c-320">下图显示生成的报表的另一页的示例。</span><span class="sxs-lookup"><span data-stu-id="a2d7c-320">The follow illustration shows an example of another page of the report that is generated.</span></span>

![生成的报表的另一页](media/rcs-ger-filloutpdf-generatedreport2.png)

## <a name="additional-resources"></a><span data-ttu-id="a2d7c-322">其他资源</span><span class="sxs-lookup"><span data-stu-id="a2d7c-322">Additional resources</span></span>

- [<span data-ttu-id="a2d7c-323">ER 设计以 OPENXML 格式生成报表的配置</span><span class="sxs-lookup"><span data-stu-id="a2d7c-323">ER Design a configuration for generating reports in OPENXML format</span></span>](tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="a2d7c-324">设计 ER 配置以生成 Microsoft Word 格式的报表</span><span class="sxs-lookup"><span data-stu-id="a2d7c-324">Design ER configurations to generate reports in Microsoft WORD format</span></span>](tasks/er-design-configuration-word-2016-11.md)

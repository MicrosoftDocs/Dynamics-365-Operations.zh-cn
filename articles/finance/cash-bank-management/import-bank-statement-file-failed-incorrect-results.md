---
title: 银行对账单文件导入故障排除
description: 银行的银行对帐单文件与 Microsoft Dynamics 365 Finance 支持的布局匹配非常重要。 由于银行对账单的限制标准，大多数集成将正确工作。 但是，有时报表文件不能导入或有错误结果。 通常，这些问题由银行对账单文件中的小差异引起。 此文章说明如何修复这些差异和解决问题。
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14f0e480b93e663f81db5a1edb2ae71b559bb05e
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188551"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="3ec6b-107">银行对账单文件导入故障排除</span><span class="sxs-lookup"><span data-stu-id="3ec6b-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ec6b-108">银行的银行对帐单文件与 Microsoft Dynamics 365 Finance 支持的布局匹配非常重要。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-108">It's important that the bank statement file from the bank matches the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="3ec6b-109">由于银行对账单的限制标准，大多数集成将正确工作。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="3ec6b-110">但是，有时报表文件不能导入或有错误结果。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="3ec6b-111">通常，这些问题由银行对账单文件中的小差异引起。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="3ec6b-112">此文章说明如何修复这些差异和解决问题。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-112">This article explains how to fix these differences and resolve the issues.</span></span>

## <a name="what-is-the-error"></a><span data-ttu-id="3ec6b-113">错误是什么？</span><span class="sxs-lookup"><span data-stu-id="3ec6b-113">What is the error?</span></span>

<span data-ttu-id="3ec6b-114">在尝试导入银行对账单文件后，请转到数据管理作业历史记录及其执行详细信息查找错误。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="3ec6b-115">错误可以通过指定报表、余额或报表行提供帮助。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="3ec6b-116">但是，不大可能提供足够的信息来帮助您确定导致问题的字段或元素。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

> [!NOTE]
> <span data-ttu-id="3ec6b-117">导入的银行对帐单只能在单个时间点重叠。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-117">Imported bank statements can overlap only for single a point in time.</span></span>  <span data-ttu-id="3ec6b-118">例如，如果对帐单于 2021 年 1 月 1 日凌晨 12:00 结束，则下一个对帐单的开始日期可能是 2021 年 1 月 1 日凌晨 12:00（即凌晨 12:00:00）。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-118">For example, if a statement ends at 12:00 AM on January 1, 2021, then beginning date for the next statement can be 12:00 AM on Jarnuary 1, 2021 12:00:00 AM.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="3ec6b-119">有哪些差异？</span><span class="sxs-lookup"><span data-stu-id="3ec6b-119">What are the differences?</span></span>
<span data-ttu-id="3ec6b-120">比较银行文件布局定义与 Finance 导入定义，注意字段和元素中的任何差异。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-120">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="3ec6b-121">比较银行对账单文件与相关示例 Finance 文件。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-121">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="3ec6b-122">在 ISO20022 文件中，应易于查看任何差异。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-122">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="3ec6b-123">导入的银行对帐单中时区不同</span><span class="sxs-lookup"><span data-stu-id="3ec6b-123">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="3ec6b-124">导入文件中的日期时间值可能与 Finance and Operations 中显示的日期时间值不同。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-124">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="3ec6b-125">若要避免此项差异，请在 **配置数据源** 页中输入时区首选项。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-125">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="3ec6b-126">有关输入时区首选项的详细信息，请参阅[设置高级银行对帐导入流程](set-up-advanced-bank-reconciliation-import-process.md)。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-126">For more information about entering a time zone preference, see [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>

## <a name="transformations"></a><span data-ttu-id="3ec6b-127">转换</span><span class="sxs-lookup"><span data-stu-id="3ec6b-127">Transformations</span></span>
<span data-ttu-id="3ec6b-128">通常，必须在三个转换之一中进行更改。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-128">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="3ec6b-129">每个转换为特定标准写入。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-129">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="3ec6b-130">资源名称</span><span class="sxs-lookup"><span data-stu-id="3ec6b-130">Resource name</span></span>                                         | <span data-ttu-id="3ec6b-131">文件名</span><span class="sxs-lookup"><span data-stu-id="3ec6b-131">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="3ec6b-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="3ec6b-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="3ec6b-133">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="3ec6b-133">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="3ec6b-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="3ec6b-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="3ec6b-135">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="3ec6b-135">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="3ec6b-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="3ec6b-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="3ec6b-137">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="3ec6b-137">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="3ec6b-138">调试转换</span><span class="sxs-lookup"><span data-stu-id="3ec6b-138">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="3ec6b-139">调整 BAI2 和 MT940 文件</span><span class="sxs-lookup"><span data-stu-id="3ec6b-139">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="3ec6b-140">BAI2 和 MT940 文件是基于文本的文件，并需要调整以支持可扩展样式表语言转换 (XSLT) 调试。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-140">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="3ec6b-141">当文件导入时，此程序进行此调整。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-141">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="3ec6b-142">创建 XML 文件，并且将以下文本复制到其中。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-142">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="3ec6b-143">复制银行对账单文件的内容，并且将其粘贴到 XML 文件，以便替换 **PASTESTATEMENTFILEHERE**。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-143">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="3ec6b-144">调试 XSLT</span><span class="sxs-lookup"><span data-stu-id="3ec6b-144">Debug the XSLT</span></span>

<span data-ttu-id="3ec6b-145">有关详细信息，请参阅<https://msdn.microsoft.com/library/ms255605.aspx>。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-145">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="3ec6b-146">启动 Microsoft Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-146">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="3ec6b-147">创建控制台申请。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-147">Create a console application.</span></span>
3.  <span data-ttu-id="3ec6b-148">打开相应的 XSLT。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-148">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="3ec6b-149">单击 XLST 及其属性页。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-149">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="3ec6b-150">设置对银行对账单文件位置的输入。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-150">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="3ec6b-151">定义输出的位置和文件名。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-151">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="3ec6b-152">设置必需的断点。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-152">Set the required break points.</span></span>
8.  <span data-ttu-id="3ec6b-153">在菜单上，单击 **XML** &gt; **启动 XSLT 调试**。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-153">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="3ec6b-154">设置 XSLT 输出格式</span><span class="sxs-lookup"><span data-stu-id="3ec6b-154">Format the XSLT output</span></span>

<span data-ttu-id="3ec6b-155">转换运行时，它会创建可以在 Visual Studio 中查看的输出文件。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-155">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="3ec6b-156">使用 Ctrl+A、Ctrl+K 和 Ctrl+D 快速设置输出文件的格式。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-156">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="3ec6b-157">调整转换</span><span class="sxs-lookup"><span data-stu-id="3ec6b-157">Adjust the transformation</span></span>

<span data-ttu-id="3ec6b-158">调整转换以获取银行对账单文件中的相应字段或元素。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-158">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="3ec6b-159">然后将该字段或元素映射到相应的 Finance 元素。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-159">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="3ec6b-160">借方/贷方指示符</span><span class="sxs-lookup"><span data-stu-id="3ec6b-160">Debit/credit indicator</span></span>

<span data-ttu-id="3ec6b-161">有时，借方可能导入为贷方，贷方可能导入为借方。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-161">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="3ec6b-162">为了解决此问题，您必须更改相应的 XSLT。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-162">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="3ec6b-163">如果银行对账单来自多个银行，请确保它们使用同一借方/贷方方法或创建单独的转换。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-163">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="3ec6b-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator 模板</span><span class="sxs-lookup"><span data-stu-id="3ec6b-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="3ec6b-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit 模板</span><span class="sxs-lookup"><span data-stu-id="3ec6b-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="3ec6b-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator 模板</span><span class="sxs-lookup"><span data-stu-id="3ec6b-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="3ec6b-167">银行对账单格式和技术布局的示例</span><span class="sxs-lookup"><span data-stu-id="3ec6b-167">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="3ec6b-168">下表列出了高级银行对帐导入文件技术布局定义的示例和三个相关银行对账单示例文件。</span><span class="sxs-lookup"><span data-stu-id="3ec6b-168">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="3ec6b-169">您可以从此处下载示例文件和技术布局：[导入文件示例](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span><span class="sxs-lookup"><span data-stu-id="3ec6b-169">You can download the example files and technical layouts here: [Import file examples](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span></span>  

| <span data-ttu-id="3ec6b-170">技术布局定义</span><span class="sxs-lookup"><span data-stu-id="3ec6b-170">Technical layout definition</span></span>                             | <span data-ttu-id="3ec6b-171">银行对账单示例文件</span><span class="sxs-lookup"><span data-stu-id="3ec6b-171">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="3ec6b-172">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="3ec6b-172">DynamicsAXMT940Layout</span></span>                                   | [<span data-ttu-id="3ec6b-173">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="3ec6b-173">MT940StatementExample</span></span>](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| <span data-ttu-id="3ec6b-174">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="3ec6b-174">DynamicsAXISO20022Layout</span></span>                                | [<span data-ttu-id="3ec6b-175">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="3ec6b-175">ISO20022StatementExample</span></span>](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| <span data-ttu-id="3ec6b-176">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="3ec6b-176">DynamicsAXBAI2Layout</span></span>                                    | [<span data-ttu-id="3ec6b-177">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="3ec6b-177">BAI2StatementExample</span></span>](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

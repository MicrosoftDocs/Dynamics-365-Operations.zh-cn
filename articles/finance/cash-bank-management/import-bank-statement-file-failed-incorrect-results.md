---
title: 银行对账单文件导入故障排除
description: 银行的银行对帐单文件与 Microsoft Dynamics 365 Finance 支持的布局匹配非常重要。 由于银行对账单的限制标准，大多数集成将正确工作。 但是，有时报表文件不能导入或有错误结果。 通常，这些问题由银行对账单文件中的小差异引起。 此文章说明如何修复这些差异和解决问题。
author: panolte
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: ac82a269e8f7773c58517ef017576c82c52039cb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253955"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="bf036-107">银行对账单文件导入故障排除</span><span class="sxs-lookup"><span data-stu-id="bf036-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf036-108">银行的银行对帐单文件与 Microsoft Dynamics 365 Finance 支持的布局匹配非常重要。</span><span class="sxs-lookup"><span data-stu-id="bf036-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="bf036-109">由于银行对账单的限制标准，大多数集成将正确工作。</span><span class="sxs-lookup"><span data-stu-id="bf036-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="bf036-110">但是，有时报表文件不能导入或有错误结果。</span><span class="sxs-lookup"><span data-stu-id="bf036-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="bf036-111">通常，这些问题由银行对账单文件中的小差异引起。</span><span class="sxs-lookup"><span data-stu-id="bf036-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="bf036-112">此文章说明如何修复这些差异和解决问题。</span><span class="sxs-lookup"><span data-stu-id="bf036-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="bf036-113">错误是什么？</span><span class="sxs-lookup"><span data-stu-id="bf036-113">What is the error?</span></span>
------------------

<span data-ttu-id="bf036-114">在尝试导入银行对账单文件后，请转到数据管理作业历史记录及其执行详细信息查找错误。</span><span class="sxs-lookup"><span data-stu-id="bf036-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="bf036-115">错误可以通过指定报表、余额或报表行提供帮助。</span><span class="sxs-lookup"><span data-stu-id="bf036-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="bf036-116">但是，不大可能提供足够的信息来帮助您确定导致问题的字段或元素。</span><span class="sxs-lookup"><span data-stu-id="bf036-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="bf036-117">有哪些差异？</span><span class="sxs-lookup"><span data-stu-id="bf036-117">What are the differences?</span></span>
<span data-ttu-id="bf036-118">比较银行文件布局定义与 Finance 导入定义，注意字段和元素中的任何差异。</span><span class="sxs-lookup"><span data-stu-id="bf036-118">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="bf036-119">比较银行对账单文件与相关示例 Finance 文件。</span><span class="sxs-lookup"><span data-stu-id="bf036-119">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="bf036-120">在 ISO20022 文件中，应易于查看任何差异。</span><span class="sxs-lookup"><span data-stu-id="bf036-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="bf036-121">导入的银行对帐单中时区不同</span><span class="sxs-lookup"><span data-stu-id="bf036-121">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="bf036-122">导入文件中的日期时间值可能与 Finance and Operations 中显示的日期时间值不同。</span><span class="sxs-lookup"><span data-stu-id="bf036-122">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="bf036-123">若要避免此项差异，请在 **配置数据源** 页中输入时区首选项。</span><span class="sxs-lookup"><span data-stu-id="bf036-123">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="bf036-124">有关输入时区首选项的详细信息，请参阅[设置高级银行对帐导入流程](set-up-advanced-bank-reconciliation-import-process.md)。</span><span class="sxs-lookup"><span data-stu-id="bf036-124">See [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md) for more information about entering a time zone preference.</span></span>

## <a name="transformations"></a><span data-ttu-id="bf036-125">转换</span><span class="sxs-lookup"><span data-stu-id="bf036-125">Transformations</span></span>
<span data-ttu-id="bf036-126">通常，必须在三个转换之一中进行更改。</span><span class="sxs-lookup"><span data-stu-id="bf036-126">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="bf036-127">每个转换为特定标准写入。</span><span class="sxs-lookup"><span data-stu-id="bf036-127">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="bf036-128">资源名称</span><span class="sxs-lookup"><span data-stu-id="bf036-128">Resource name</span></span>                                         | <span data-ttu-id="bf036-129">文件名</span><span class="sxs-lookup"><span data-stu-id="bf036-129">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="bf036-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="bf036-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="bf036-131">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="bf036-131">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="bf036-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="bf036-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="bf036-133">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="bf036-133">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="bf036-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="bf036-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="bf036-135">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="bf036-135">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="bf036-136">调试转换</span><span class="sxs-lookup"><span data-stu-id="bf036-136">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="bf036-137">调整 BAI2 和 MT940 文件</span><span class="sxs-lookup"><span data-stu-id="bf036-137">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="bf036-138">BAI2 和 MT940 文件是基于文本的文件，并需要调整以支持可扩展样式表语言转换 (XSLT) 调试。</span><span class="sxs-lookup"><span data-stu-id="bf036-138">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="bf036-139">当文件导入时，此程序进行此调整。</span><span class="sxs-lookup"><span data-stu-id="bf036-139">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="bf036-140">创建 XML 文件，并且将以下文本复制到其中。</span><span class="sxs-lookup"><span data-stu-id="bf036-140">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="bf036-141">复制银行对账单文件的内容，并且将其粘贴到 XML 文件，以便替换 **PASTESTATEMENTFILEHERE**。</span><span class="sxs-lookup"><span data-stu-id="bf036-141">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="bf036-142">调试 XSLT</span><span class="sxs-lookup"><span data-stu-id="bf036-142">Debug the XSLT</span></span>

<span data-ttu-id="bf036-143">有关详细信息，请参阅<https://msdn.microsoft.com/library/ms255605.aspx>。</span><span class="sxs-lookup"><span data-stu-id="bf036-143">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="bf036-144">启动 Microsoft Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="bf036-144">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="bf036-145">创建控制台申请。</span><span class="sxs-lookup"><span data-stu-id="bf036-145">Create a console application.</span></span>
3.  <span data-ttu-id="bf036-146">打开相应的 XSLT。</span><span class="sxs-lookup"><span data-stu-id="bf036-146">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="bf036-147">单击 XLST 及其属性页。</span><span class="sxs-lookup"><span data-stu-id="bf036-147">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="bf036-148">设置对银行对账单文件位置的输入。</span><span class="sxs-lookup"><span data-stu-id="bf036-148">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="bf036-149">定义输出的位置和文件名。</span><span class="sxs-lookup"><span data-stu-id="bf036-149">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="bf036-150">设置必需的断点。</span><span class="sxs-lookup"><span data-stu-id="bf036-150">Set the required break points.</span></span>
8.  <span data-ttu-id="bf036-151">在菜单上，单击 **XML** &gt; **启动 XSLT 调试**。</span><span class="sxs-lookup"><span data-stu-id="bf036-151">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="bf036-152">设置 XSLT 输出格式</span><span class="sxs-lookup"><span data-stu-id="bf036-152">Format the XSLT output</span></span>

<span data-ttu-id="bf036-153">转换运行时，它会创建可以在 Visual Studio 中查看的输出文件。</span><span class="sxs-lookup"><span data-stu-id="bf036-153">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="bf036-154">使用 Ctrl+A、Ctrl+K 和 Ctrl+D 快速设置输出文件的格式。</span><span class="sxs-lookup"><span data-stu-id="bf036-154">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="bf036-155">调整转换</span><span class="sxs-lookup"><span data-stu-id="bf036-155">Adjust the transformation</span></span>

<span data-ttu-id="bf036-156">调整转换以获取银行对账单文件中的相应字段或元素。</span><span class="sxs-lookup"><span data-stu-id="bf036-156">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="bf036-157">然后将该字段或元素映射到相应的 Finance 元素。</span><span class="sxs-lookup"><span data-stu-id="bf036-157">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="bf036-158">借方/贷方指示符</span><span class="sxs-lookup"><span data-stu-id="bf036-158">Debit/credit indicator</span></span>

<span data-ttu-id="bf036-159">有时，借方可能导入为贷方，贷方可能导入为借方。</span><span class="sxs-lookup"><span data-stu-id="bf036-159">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="bf036-160">为了解决此问题，您必须更改相应的 XSLT。</span><span class="sxs-lookup"><span data-stu-id="bf036-160">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="bf036-161">如果银行对账单来自多个银行，请确保它们使用同一借方/贷方方法或创建单独的转换。</span><span class="sxs-lookup"><span data-stu-id="bf036-161">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="bf036-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator 模板</span><span class="sxs-lookup"><span data-stu-id="bf036-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="bf036-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit 模板</span><span class="sxs-lookup"><span data-stu-id="bf036-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="bf036-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator 模板</span><span class="sxs-lookup"><span data-stu-id="bf036-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="bf036-165">银行对账单格式和技术布局的示例</span><span class="sxs-lookup"><span data-stu-id="bf036-165">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="bf036-166">下表列出了高级银行对帐导入文件技术布局定义的示例和三个相关银行对账单示例文件。</span><span class="sxs-lookup"><span data-stu-id="bf036-166">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="bf036-167">您可以从此处下载示例文件和技术布局：https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="bf036-167">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="bf036-168">技术布局定义</span><span class="sxs-lookup"><span data-stu-id="bf036-168">Technical layout definition</span></span>                             | <span data-ttu-id="bf036-169">银行对账单示例文件</span><span class="sxs-lookup"><span data-stu-id="bf036-169">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="bf036-170">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="bf036-170">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="bf036-171">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="bf036-171">MT940StatementExample</span></span>                |
| <span data-ttu-id="bf036-172">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="bf036-172">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="bf036-173">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="bf036-173">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="bf036-174">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="bf036-174">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="bf036-175">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="bf036-175">BAI2StatementExample</span></span>                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
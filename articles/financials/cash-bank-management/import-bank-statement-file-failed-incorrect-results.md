---
title: 银行对账单文件导入故障排除
description: 银行的银行对帐单文件与 Microsoft Dynamics 365 for Finance and Operations 支持的布局匹配非常重要。 由于银行对账单的限制标准，大多数集成将正确工作。 但是，有时报表文件不能导入或有错误结果。 通常，这些问题由银行对账单文件中的小差异引起。 此文章说明如何修复这些差异和解决问题。
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4006bf35673e3bb61bcf11619ecc68d295f29eb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "324437"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="7ce1f-107">银行对账单文件导入故障排除</span><span class="sxs-lookup"><span data-stu-id="7ce1f-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ce1f-108">银行的银行对帐单文件与 Microsoft Dynamics 365 for Finance and Operations 支持的布局匹配非常重要。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 for Finance and Operations supports.</span></span> <span data-ttu-id="7ce1f-109">由于银行对账单的限制标准，大多数集成将正确工作。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="7ce1f-110">但是，有时报表文件不能导入或有错误结果。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="7ce1f-111">通常，这些问题由银行对账单文件中的小差异引起。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="7ce1f-112">此文章说明如何修复这些差异和解决问题。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="7ce1f-113">错误是什么？</span><span class="sxs-lookup"><span data-stu-id="7ce1f-113">What is the error?</span></span>
------------------

<span data-ttu-id="7ce1f-114">在尝试导入银行对账单文件后，请转到数据管理作业历史记录及其执行详细信息查找错误。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="7ce1f-115">错误可以通过指定报表、余额或报表行提供帮助。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="7ce1f-116">但是，不大可能提供足够的信息来帮助您确定导致问题的字段或元素。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="7ce1f-117">有哪些差异？</span><span class="sxs-lookup"><span data-stu-id="7ce1f-117">What are the differences?</span></span>
<span data-ttu-id="7ce1f-118">比较银行文件布局定义与 Finance and Operations 导入定义，注意字段和元素中的任何差异。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-118">Compare the bank file layout definition to the Finance and Operations import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="7ce1f-119">比较银行对账单文件与相关示例 Finance and Operations 文件。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-119">Compare the bank statement file to the related sample Finance and Operations file.</span></span> <span data-ttu-id="7ce1f-120">在 ISO20022 文件中，应易于查看任何差异。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="transformations"></a><span data-ttu-id="7ce1f-121">转换</span><span class="sxs-lookup"><span data-stu-id="7ce1f-121">Transformations</span></span>
<span data-ttu-id="7ce1f-122">通常，必须在三个转换之一中进行更改。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-122">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="7ce1f-123">每个转换为特定标准写入。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-123">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="7ce1f-124">资源名称</span><span class="sxs-lookup"><span data-stu-id="7ce1f-124">Resource name</span></span>                                         | <span data-ttu-id="7ce1f-125">文件名</span><span class="sxs-lookup"><span data-stu-id="7ce1f-125">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="7ce1f-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="7ce1f-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="7ce1f-127">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="7ce1f-127">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="7ce1f-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="7ce1f-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="7ce1f-129">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="7ce1f-129">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="7ce1f-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="7ce1f-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="7ce1f-131">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="7ce1f-131">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="7ce1f-132">调试转换</span><span class="sxs-lookup"><span data-stu-id="7ce1f-132">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="7ce1f-133">调整 BAI2 和 MT940 文件</span><span class="sxs-lookup"><span data-stu-id="7ce1f-133">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="7ce1f-134">BAI2 和 MT940 文件是基于文本的文件，并需要调整以支持可扩展样式表语言转换 (XSLT) 调试。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-134">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="7ce1f-135">当文件导入时，此程序进行此调整。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-135">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="7ce1f-136">创建 XML 文件，并且将以下文本复制到其中。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-136">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="7ce1f-137">复制银行对账单文件的内容，并且将其粘贴到 XML 文件，以便替换 **PASTESTATEMENTFILEHERE**。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-137">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="7ce1f-138">调试 XSLT</span><span class="sxs-lookup"><span data-stu-id="7ce1f-138">Debug the XSLT</span></span>

<span data-ttu-id="7ce1f-139">有关详细信息，请参阅<https://msdn.microsoft.com/en-us/library/ms255605.aspx>。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-139">For more information, see <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="7ce1f-140">启动 Microsoft Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-140">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="7ce1f-141">创建控制台申请。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-141">Create a console application.</span></span>
3.  <span data-ttu-id="7ce1f-142">打开相应的 XSLT。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-142">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="7ce1f-143">单击 XLST 及其属性页。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-143">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="7ce1f-144">设置对银行对账单文件位置的输入。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-144">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="7ce1f-145">定义输出的位置和文件名。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-145">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="7ce1f-146">设置必需的断点。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-146">Set the required break points.</span></span>
8.  <span data-ttu-id="7ce1f-147">在菜单上，单击 **XML** &gt; **启动 XSLT 调试**。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-147">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="7ce1f-148">设置 XSLT 输出格式</span><span class="sxs-lookup"><span data-stu-id="7ce1f-148">Format the XSLT output</span></span>

<span data-ttu-id="7ce1f-149">转换运行时，它会创建可以在 Visual Studio 中查看的输出文件。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-149">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="7ce1f-150">使用 Ctrl+A、Ctrl+K 和 Ctrl+D 快速设置输出文件的格式。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-150">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="7ce1f-151">调整转换</span><span class="sxs-lookup"><span data-stu-id="7ce1f-151">Adjust the transformation</span></span>

<span data-ttu-id="7ce1f-152">调整转换以获取银行对账单文件中的相应字段或元素。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-152">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="7ce1f-153">然后将该字段或元素映射到相应的 Finance and Operations 元素。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-153">Then map that field or element to the appropriate Finance and Operations element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="7ce1f-154">借方/贷方指示符</span><span class="sxs-lookup"><span data-stu-id="7ce1f-154">Debit/credit indicator</span></span>

<span data-ttu-id="7ce1f-155">有时，借方可能导入为贷方，贷方可能导入为借方。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-155">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="7ce1f-156">为了解决此问题，您必须更改相应的 XSLT。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-156">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="7ce1f-157">如果银行对账单来自多个银行，请确保它们使用同一借方/贷方方法或创建单独的转换。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-157">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="7ce1f-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator 模板</span><span class="sxs-lookup"><span data-stu-id="7ce1f-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="7ce1f-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit 模板</span><span class="sxs-lookup"><span data-stu-id="7ce1f-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="7ce1f-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator 模板</span><span class="sxs-lookup"><span data-stu-id="7ce1f-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="7ce1f-161">银行对账单格式和技术布局的示例</span><span class="sxs-lookup"><span data-stu-id="7ce1f-161">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="7ce1f-162">下表列出了高级银行对帐导入文件技术布局定义的示例和三个相关银行对账单示例文件。</span><span class="sxs-lookup"><span data-stu-id="7ce1f-162">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="7ce1f-163">您可以从此处下载示例文件和技术布局：https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="7ce1f-163">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="7ce1f-164">技术布局定义</span><span class="sxs-lookup"><span data-stu-id="7ce1f-164">Technical layout definition</span></span>                             | <span data-ttu-id="7ce1f-165">银行对账单示例文件</span><span class="sxs-lookup"><span data-stu-id="7ce1f-165">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="7ce1f-166">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="7ce1f-166">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="7ce1f-167">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="7ce1f-167">MT940StatementExample</span></span>                |
| <span data-ttu-id="7ce1f-168">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="7ce1f-168">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="7ce1f-169">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="7ce1f-169">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="7ce1f-170">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="7ce1f-170">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="7ce1f-171">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="7ce1f-171">BAI2StatementExample</span></span>                 |






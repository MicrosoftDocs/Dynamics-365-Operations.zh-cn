---
title: 设置和生成付款确认文件
description: 本主题说明如何设置付款确认和生成付款确认文件。
author: abruer
manager: AnnBe
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 0c44d172e8ed9cdb9c26501b3f4eb9fef4f8cf0b
ms.sourcegitcommit: 4f668b23f5bfc6d6502858850d2ed59d7a79cfbb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2020
ms.locfileid: "3059393"
---
# <a name="set-up-and-generate-positive-pay-files"></a><span data-ttu-id="ff4c9-103">设置和生成付款确认文件</span><span class="sxs-lookup"><span data-stu-id="ff4c9-103">Set up and generate positive pay files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff4c9-104">本主题说明如何设置付款确认和生成付款确认文件。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-104">This topic explains how to set up positive pay and generate positive pay files.</span></span> 

<span data-ttu-id="ff4c9-105">设置付款确认以生成提供给银行的支票电子列表。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-105">Set up positive pay to generate an electronic list of checks that is provided to the bank.</span></span> <span data-ttu-id="ff4c9-106">然后，当支票提交给银行时，银行将支票与支票的列表进行对比。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-106">Then, when a check is presented to the bank, the bank compares it with the list of checks.</span></span> <span data-ttu-id="ff4c9-107">如果支票与列表中的支票相匹配，银行将清算支票。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-107">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="ff4c9-108">如果支票与列表中的支票不匹配，银行将保留支票以供审查。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-108">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

## <a name="security-for-positive-pay-files"></a><span data-ttu-id="ff4c9-109">付款确认文件的安全</span><span class="sxs-lookup"><span data-stu-id="ff4c9-109">Security for positive pay files</span></span>
<span data-ttu-id="ff4c9-110">付款确认文件可以包含有关收款人和支票金额的敏感信息。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-110">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="ff4c9-111">因此，请您务必自文件生成时便使用相应的安全措施，直到它们由银行接收。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-111">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="ff4c9-112">付款确认文件下载到您的 Web 浏览器指定的位置。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-112">Positive pay files are downloaded to the location that is specified by your web browser.</span></span> <span data-ttu-id="ff4c9-113">由于付款确认文件可能包含敏感信息，务必确保仅授权用户可以在 Microsoft Dynamics 365 Finance 中生成和查看此信息。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-113">Because positive pay files can contain sensitive information, it's important that only authorized users have access to generate and view this information in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="ff4c9-114">请使用下表帮助您确定所需权限。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-114">Use the following table to help you determine the privileges that are required.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff4c9-115">任务</span><span class="sxs-lookup"><span data-stu-id="ff4c9-115">Task</span></span></th>
<th><span data-ttu-id="ff4c9-116">特权</span><span class="sxs-lookup"><span data-stu-id="ff4c9-116">Privilege</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ff4c9-117">从<strong>银行帐户</strong>列表页或<strong>银行帐户</strong>页生成付款确认文件。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-117">Generate positive pay files from the <strong>Bank accounts</strong> list page or the <strong>Bank accounts</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="ff4c9-118"><strong>维护银行付款确认信息</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="ff4c9-118"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="ff4c9-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="ff4c9-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff4c9-120">从<strong>生成付款确认文件</strong>页生成多个法人和银行帐户的付款确认文件。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-120">Generate positive pay files for multiple legal entities and bank accounts from the <strong>Generate a positive pay file</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="ff4c9-121"><strong>维护银行付款确认信息</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="ff4c9-121"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="ff4c9-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="ff4c9-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff4c9-123">在<strong>付款确认文件摘要</strong>页查看付款确认文件。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-123">View positive pay files on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="ff4c9-124"><strong>查看多个法人的银行付款确认信息</strong> (BankPositivePayView)</span><span class="sxs-lookup"><span data-stu-id="ff4c9-124"><strong>View bank positive pay information for multiple legal entities</strong> (BankPositivePayView)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff4c9-125">在<strong>付款确认文件摘要</strong>页确认银行付款确认文件。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-125">Confirm a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="ff4c9-126"><strong>确认付款确认文件</strong> (BankPositivePayConfirm)</span><span class="sxs-lookup"><span data-stu-id="ff4c9-126"><strong>Confirm positive payment file</strong> (BankPositivePayConfirm)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff4c9-127">在<strong>付款确认文件摘要</strong>页撤回银行付款确认文件。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-127">Recall a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="ff4c9-128"><strong>撤回付款确认文件</strong> (BankPositivePayRecall)</span><span class="sxs-lookup"><span data-stu-id="ff4c9-128"><strong>Recall positive pay file</strong> (BankPositivePayRecall)</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a><span data-ttu-id="ff4c9-129">设置付款确认格式</span><span class="sxs-lookup"><span data-stu-id="ff4c9-129">Set up a positive pay format</span></span>
<span data-ttu-id="ff4c9-130">通过使用数据实体创建付款确认文件。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-130">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="ff4c9-131">在您生成付款确认文件之前，必须设置要用于将检查信息转化为可与银行通信的格式的转换输入格式。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-131">Before you can generate a positive pay file, you must set up a transformation input format that will be used to translate the check information into a format that can communicate with the bank.</span></span> <span data-ttu-id="ff4c9-132">在**付款确认格式**页上，您可以创建文件格式标识符和描述。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-132">On the **Positive pay format** page, you can create a file format identifier and a description.</span></span> <span data-ttu-id="ff4c9-133">转换输入格式必须采用 XML 类型。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-133">The transformation input format must be of the XML type.</span></span> <span data-ttu-id="ff4c9-134">特定格式取决于您使用的转换文件。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-134">The specific format depends on the transformation file that you're using.</span></span> <span data-ttu-id="ff4c9-135">例如，提供的可扩展样式表语言转换 (XSLT) 文件使用 **XML-元素**格式。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-135">For example, the sample Extensible Stylesheet Language Transformations (XSLT) file that is provided uses the **XML-Element** format.</span></span> <span data-ttu-id="ff4c9-136">使用**上载用于转换的文件**操作指定您的银行所需的格式的转换文件的位置。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-136">Use the **Upload file used for transformation** action to specify the location of the transform file for the format that your bank requires.</span></span>

## <a name="example-xslt-file-for-positive-pay-file"></a><span data-ttu-id="ff4c9-137">示例：付款确认文件的 XSLT 文件</span><span class="sxs-lookup"><span data-stu-id="ff4c9-137">Example: XSLT file for positive pay file</span></span>

```xml
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:msxsl="urn:schemas-microsoft-com:xslt" exclude-result-prefixes="msxsl xslthelper" xmlns="urn:iso:std:iso:20022:tech:xsd:pain.001.001.02" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xslthelper="http://schemas.microsoft.com/BizTalk/2003/xslthelper">
  <xsl:output method="xml" omit-xml-declaration="no" version="1.0" encoding="utf-8"/>
  <xsl:template match="/">
    <xsl:value-of select="'
'" />
    <Document>
      <xsl:value-of select="'
'" />
      <!--Header Begin-->
      <xsl:value-of select='string("Vendor ID,Vendor Name,Voided,Document Type,Check Date,Check Number,Check Amount,Checkbook ID,Vendor Class ID,Posted Date")'/>
      <xsl:value-of select="'
'" />
      <!--Header End-->
      <xsl:for-each select="Document/BANKPOSITIVEPAYEXPORTENTITY">
        <!--Cheque Detail begin-->
        <xsl:value-of select='RECIPIENTACCOUNTNUM/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='BANKNEGINSTRECIPIENTNAME/text()'/>
        <xsl:value-of select="','" />
        <xsl:choose>
          <xsl:when test='CHEQUESTATUS/text()=normalize-space("Void") or CHEQUESTATUS/text()=normalize-space("Rejected") or CHEQUESTATUS/text()=normalize-space("Cancelled")'>
            <xsl:value-of select='string("Yes")'/>
          </xsl:when>
          <xsl:when test='CHEQUESTATUS/text()=normalize-space("Payment")'>
            <xsl:value-of select='string("No")'/>
          </xsl:when>
          <xsl:otherwise>
            <xsl:value-of select='string(" ")'/>
          </xsl:otherwise>
        </xsl:choose>
        <xsl:value-of select="','" />
        <xsl:value-of select='string("Payment")'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='TRANSDATE/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='CHEQUENUM/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='AMOUNTCUR/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='string("BOA-#1812")'/>
        <xsl:value-of select="','" />
        <xsl:choose>
          <xsl:when test='RECIPIENTTYPE/text()=normalize-space("Vend")'>
            <xsl:value-of select='VENDGROUP/text()'/>
          </xsl:when>
          <xsl:otherwise>
            <xsl:value-of select='CUSTGROUP/text()'/>
          </xsl:otherwise>
        </xsl:choose>
        <xsl:value-of select="','" />
        <xsl:value-of select='TRANSDATE/text()'/>
        <xsl:value-of select="'
'" />
      </xsl:for-each>
    </Document>
  </xsl:template>
</xsl:stylesheet>
```

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a><span data-ttu-id="ff4c9-138">将付款确认格式分配到银行帐户</span><span class="sxs-lookup"><span data-stu-id="ff4c9-138">Assign the positive pay format to a bank account</span></span>
<span data-ttu-id="ff4c9-139">对于您想要生成付款确认信息的每个银行帐户，您必须分配在前一部分中指定的付款确认格式。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-139">For each bank account that you want to generate positive pay information for, you must assign the positive pay format that you specified in the previous section.</span></span> <span data-ttu-id="ff4c9-140">在**银行帐户**页上，选择与银行帐户对应的付款确认格式。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-140">On the **Bank accounts** page, select the positive pay format that corresponds to the bank account.</span></span> <span data-ttu-id="ff4c9-141">在**付款确认开始日期**字段中，输入第一个日期以生成付款确认文件。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-141">In the **Positive pay start date** field, enter the first date to generate positive pay files.</span></span> <span data-ttu-id="ff4c9-142">您务必在此字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-142">It's important that you enter a date in this field.</span></span> <span data-ttu-id="ff4c9-143">否则，您生成的第一个付款确认文件将包括已为此银行帐户创建的所有支票。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-143">Otherwise, the first positive pay file that you generate will include all checks that have ever been created for this bank account.</span></span>

## <a name="assign-a-number-sequence-for-positive-pay-files"></a><span data-ttu-id="ff4c9-144">分配付款确认文件的编号规则</span><span class="sxs-lookup"><span data-stu-id="ff4c9-144">Assign a number sequence for positive pay files</span></span>
<span data-ttu-id="ff4c9-145">每个付款确认文件必须具有唯一编号。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-145">Each positive pay file must have a unique number.</span></span> <span data-ttu-id="ff4c9-146">使用**现金和银行管理参数**页上的**编号规则**选项卡为付款确认文件创建编号规则。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-146">Use the **Number sequences** tab on the **Cash and bank management parameters** page to create a number sequence for positive pay files.</span></span>

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a><span data-ttu-id="ff4c9-147">生成单个银行帐户的付款确认文件</span><span class="sxs-lookup"><span data-stu-id="ff4c9-147">Generate a positive pay file for a single bank account</span></span>
<span data-ttu-id="ff4c9-148">您可以生成用于一个法人或一个银行帐户的付款确认文件。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-148">You can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="ff4c9-149">有关如何同时生成用于多个法人和银行帐户的付款确认文件，请参阅下一部分。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-149">For information about how to generate positive pay files for multiple legal entities and bank accounts at the same time, see the next section.</span></span> <span data-ttu-id="ff4c9-150">若要生成单个法人和单个银行帐户的付款确认文件，从**银行帐户**页打开**生成付款确认文件**对话框。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-150">To generate a positive pay file for a single legal entity and a single bank account, open the **Generate a positive pay file** dialog box from the **Bank accounts** page.</span></span> <span data-ttu-id="ff4c9-151">在字段**截止日期**中，输入在付款确认文件中的最后支票日期。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-151">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="ff4c9-152">所有在该支票日期结束前未包括在一个付款确认文件中的支票将包括在该文件中。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-152">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a><span data-ttu-id="ff4c9-153">生成多个银行帐户的付款确认文件</span><span class="sxs-lookup"><span data-stu-id="ff4c9-153">Generate a positive pay file for multiple bank accounts</span></span>
<span data-ttu-id="ff4c9-154">若要生成多个银行帐户的付款确认文件，使用**生成付款确认文件**定期任务。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-154">To generate a positive pay file for multiple bank accounts, use the **Generate a positive pay file** periodic task.</span></span> <span data-ttu-id="ff4c9-155">选择文件的付款确认格式，并指定是为所有法人还是所选法人生成文件。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-155">Select the positive pay format for the file, and specify whether to generate the file for all legal entities or for a selected legal entity.</span></span> <span data-ttu-id="ff4c9-156">您还可以为使用指定的付款确认格式的所有银行帐户或为所选银行帐户生成付款确认文件。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-156">You can also generate the positive pay file for all bank accounts that use the specified positive pay format or for a selected bank account.</span></span> <span data-ttu-id="ff4c9-157">在字段**截止日期**中，输入在付款确认文件中的最后支票日期。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-157">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="ff4c9-158">所有在该支票日期结束前未包括在一个付款确认文件中的支票将包括在该文件中。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-158">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="view-the-results-of-positive-pay-file-generation"></a><span data-ttu-id="ff4c9-159">查看付款确认文件的生成结果</span><span class="sxs-lookup"><span data-stu-id="ff4c9-159">View the results of positive pay file generation</span></span>
<span data-ttu-id="ff4c9-160">在付款确认文件生成后，您可以在**付款确认文件摘要**页上查看结果。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-160">After the positive pay file is generated, you can view the results on the **Positive pay file summary** page.</span></span> <span data-ttu-id="ff4c9-161">若要查看单个支票的详细信息，使用**付款确认文件**详细信息页。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-161">To view the details of the individual checks, use the **Positive pay file** details page.</span></span>

## <a name="confirm-a-positive-pay-file"></a><span data-ttu-id="ff4c9-162">确认付款确认文件</span><span class="sxs-lookup"><span data-stu-id="ff4c9-162">Confirm a positive pay file</span></span>
<span data-ttu-id="ff4c9-163">当付款确认文件中列出的支票支付后，您将从银行收到一个确认编号。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-163">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="ff4c9-164">然后，您可以确认付款确认文件。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-164">You can then confirm the positive pay file.</span></span> <span data-ttu-id="ff4c9-165">在**付款确认文件**页上，选择状态为**已创建**的付款确认文件，然后选择**输入确认**操作。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-165">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Enter confirmation** action.</span></span> <span data-ttu-id="ff4c9-166">在确认付款确认文件时，记录您从银行收到的确认编号。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-166">When you confirm a positive pay file, the confirmation number that you received from the bank is recorded.</span></span>

## <a name="recall-a-positive-pay-file"></a><span data-ttu-id="ff4c9-167">撤回付款确认文件</span><span class="sxs-lookup"><span data-stu-id="ff4c9-167">Recall a positive pay file</span></span>
<span data-ttu-id="ff4c9-168">如果您必须更改付款确认文件，您可以撤消它。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-168">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="ff4c9-169">在**付款确认文件**页上，选择状态为**已创建**的付款确认文件，然后选择**撤回**操作。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-169">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Recall** action.</span></span> <span data-ttu-id="ff4c9-170">对于付款确认文件中的每一张支票，将重置指示该支票是否包括在一个付款确认文件中的字段。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-170">For each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span> <span data-ttu-id="ff4c9-171">然后，您可以创建包括已撤消支票的新的付款确认文件。</span><span class="sxs-lookup"><span data-stu-id="ff4c9-171">You can then create a new positive pay file that includes the check that was recalled.</span></span>




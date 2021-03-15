---
title: 设置和生成付款确认文件
description: 本主题说明如何设置付款确认和生成付款确认文件。
author: panolte
manager: AnnBe
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 0984710220171f36a520e471c6c55bf12d97675b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972011"
---
# <a name="set-up-and-generate-positive-pay-files"></a>设置和生成付款确认文件

[!include [banner](../includes/banner.md)]

本主题说明如何设置付款确认和生成付款确认文件。 

设置付款确认以生成提供给银行的支票电子列表。 然后，当支票提交给银行时，银行将支票与支票的列表进行对比。 如果支票与列表中的支票相匹配，银行将清算支票。 如果支票与列表中的支票不匹配，银行将保留支票以供审查。

## <a name="security-for-positive-pay-files"></a>付款确认文件的安全
付款确认文件可以包含有关收款人和支票金额的敏感信息。 因此，请您务必自文件生成时便使用相应的安全措施，直到它们由银行接收。 付款确认文件下载到您的 Web 浏览器指定的位置。 由于付款确认文件可能包含敏感信息，务必确保仅授权用户可以在 Microsoft Dynamics 365 Finance 中生成和查看此信息。 请使用下表帮助您确定所需权限。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>任务</th>
<th>特权</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>从<strong>银行帐户</strong>列表页或<strong>银行帐户</strong>页生成付款确认文件。</td>
<td><ul>
<li><strong>维护银行付款确认信息</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>从<strong>生成付款确认文件</strong>页生成多个法人和银行帐户的付款确认文件。</td>
<td><ul>
<li><strong>维护银行付款确认信息</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>在<strong>付款确认文件摘要</strong>页查看付款确认文件。</td>
<td><strong>查看多个法人的银行付款确认信息</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>在<strong>付款确认文件摘要</strong>页确认银行付款确认文件。</td>
<td><strong>确认付款确认文件</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>在<strong>付款确认文件摘要</strong>页撤回银行付款确认文件。</td>
<td><strong>撤回付款确认文件</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a>设置付款确认格式
通过使用数据实体创建付款确认文件。 在您生成付款确认文件之前，必须设置要用于将检查信息转化为可与银行通信的格式的转换输入格式。 在 **付款确认格式** 页上，您可以创建文件格式标识符和描述。 转换输入格式必须采用 XML 类型。 特定格式取决于您使用的转换文件。 例如，提供的可扩展样式表语言转换 (XSLT) 文件使用 **XML-元素** 格式。 使用 **上载用于转换的文件** 操作指定您的银行所需的格式的转换文件的位置。

## <a name="example-xslt-file-for-positive-pay-file"></a>示例：付款确认文件的 XSLT 文件

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

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a>将付款确认格式分配到银行帐户
对于您想要生成付款确认信息的每个银行帐户，您必须分配在前一部分中指定的付款确认格式。 在 **银行帐户** 页上，选择与银行帐户对应的付款确认格式。 在 **付款确认开始日期** 字段中，输入第一个日期以生成付款确认文件。 您务必在此字段中输入日期。 否则，您生成的第一个付款确认文件将包括已为此银行帐户创建的所有支票。

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>分配付款确认文件的编号规则
每个付款确认文件必须具有唯一编号。 使用 **现金和银行管理参数** 页上的 **编号规则** 选项卡为付款确认文件创建编号规则。

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>生成单个银行帐户的付款确认文件
您可以生成用于一个法人或一个银行帐户的付款确认文件。 有关如何同时生成用于多个法人和银行帐户的付款确认文件，请参阅下一部分。 若要生成单个法人和单个银行帐户的付款确认文件，从 **银行帐户** 页打开 **生成付款确认文件** 对话框。 在字段 **截止日期** 中，输入在付款确认文件中的最后支票日期。 所有在该支票日期结束前未包括在一个付款确认文件中的支票将包括在该文件中。

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>生成多个银行帐户的付款确认文件
若要生成多个银行帐户的付款确认文件，使用 **生成付款确认文件** 定期任务。 选择文件的付款确认格式，并指定是为所有法人还是所选法人生成文件。 您还可以为使用指定的付款确认格式的所有银行帐户或为所选银行帐户生成付款确认文件。 在字段 **截止日期** 中，输入在付款确认文件中的最后支票日期。 所有在该支票日期结束前未包括在一个付款确认文件中的支票将包括在该文件中。

## <a name="view-the-results-of-positive-pay-file-generation"></a>查看付款确认文件的生成结果
在付款确认文件生成后，您可以在 **付款确认文件摘要** 页上查看结果。 若要查看单个支票的详细信息，使用 **付款确认文件** 详细信息页。

## <a name="confirm-a-positive-pay-file"></a>确认付款确认文件
当付款确认文件中列出的支票支付后，您将从银行收到一个确认编号。 然后，您可以确认付款确认文件。 在 **付款确认文件** 页上，选择状态为 **已创建** 的付款确认文件，然后选择 **输入确认** 操作。 在确认付款确认文件时，记录您从银行收到的确认编号。

## <a name="recall-a-positive-pay-file"></a>撤回付款确认文件
如果您必须更改付款确认文件，您可以撤消它。 在 **付款确认文件** 页上，选择状态为 **已创建** 的付款确认文件，然后选择 **撤回** 操作。 对于付款确认文件中的每一张支票，将重置指示该支票是否包括在一个付款确认文件中的字段。 然后，您可以创建包括已撤消支票的新的付款确认文件。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: "银行对账单文件导入故障排除"
description: "银行的银行对帐单文件与 Microsoft Dynamics 365 for Finance and Operations 支持的布局匹配非常重要。 由于银行对账单的限制标准，大多数集成将正确工作。 但是，有时报表文件不能导入或有错误结果。 通常，这些问题由银行对账单文件中的小差异引起。 此文章说明如何修复这些差异和解决问题。"
author: twheeloc
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: c408f30c783d58766ab93b13c589079c3ef375de
ms.contentlocale: zh-cn
ms.lasthandoff: 03/26/2018

---

# <a name="bank-statement-file-import-troubleshooting"></a>银行对账单文件导入故障排除

[!include[banner](../includes/banner.md)]


银行的银行对帐单文件与 Microsoft Dynamics 365 for Finance and Operations 支持的布局匹配非常重要。 由于银行对账单的限制标准，大多数集成将正确工作。 但是，有时报表文件不能导入或有错误结果。 通常，这些问题由银行对账单文件中的小差异引起。 此文章说明如何修复这些差异和解决问题。

<a name="what-is-the-error"></a>错误是什么？
------------------

在尝试导入银行对账单文件后，请转到数据管理作业历史记录及其执行详细信息查找错误。 错误可以通过指定报表、余额或报表行提供帮助。 但是，不大可能提供足够的信息来帮助您确定导致问题的字段或元素。

## <a name="what-are-the-differences"></a>有哪些差异？
比较银行文件布局定义与 Finance and Operations 导入定义，注意字段和元素中的任何差异。 比较银行对账单文件与相关示例 Finance and Operations 文件。 在 ISO20022 文件中，应易于查看任何差异。

## <a name="transformations"></a>转换
通常，必须在三个转换之一中进行更改。 每个转换为特定标准写入。

| 资源名称                                         | 文件名                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>调试转换
### <a name="adjust-the-bai2-and-mt940-files"></a>调整 BAI2 和 MT940 文件

BAI2 和 MT940 文件是基于文本的文件，并需要调整以支持可扩展样式表语言转换 (XSLT) 调试。 当文件导入时，此程序进行此调整。

1.  创建 XML 文件，并且将以下文本复制到其中。

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  复制银行对账单文件的内容，并且将其粘贴到 XML 文件，以便替换 **PASTESTATEMENTFILEHERE**。

### <a name="debug-the-xslt"></a>调试 XSLT

有关详细信息，请参阅<https://msdn.microsoft.com/en-us/library/ms255605.aspx>。

1.  启动 Microsoft Visual Studio。
2.  创建控制台申请。
3.  打开相应的 XSLT。
4.  单击 XLST 及其属性页。
5.  设置对银行对账单文件位置的输入。
6.  定义输出的位置和文件名。
7.  设置必需的断点。
8.  在菜单上，单击 **XML** &gt; **启动 XSLT 调试**。

### <a name="format-the-xslt-output"></a>设置 XSLT 输出格式

转换运行时，它会创建可以在 Visual Studio 中查看的输出文件。 使用 Ctrl+A、Ctrl+K 和 Ctrl+D 快速设置输出文件的格式。

### <a name="adjust-the-transformation"></a>调整转换

调整转换以获取银行对账单文件中的相应字段或元素。 然后将该字段或元素映射到相应的 Finance and Operations 元素。

### <a name="debitcredit-indicator"></a>借方/贷方指示符

有时，借方可能导入为贷方，贷方可能导入为借方。 为了解决此问题，您必须更改相应的 XSLT。 如果银行对账单来自多个银行，请确保它们使用同一借方/贷方方法或创建单独的转换。

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator 模板
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit 模板
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator 模板

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>银行对账单格式和技术布局的示例
下表列出了高级银行对帐导入文件技术布局定义的示例和三个相关银行对账单示例文件。 您可以从此处下载示例文件和技术布局：https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| 技术布局定义                             | 银行对账单示例文件          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |







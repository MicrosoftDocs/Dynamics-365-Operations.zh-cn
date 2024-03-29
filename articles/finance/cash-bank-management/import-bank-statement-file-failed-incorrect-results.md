---
title: 银行对帐单文件导入疑难解答
description: 本文说明如何解决这些由银行对账单文件中的小差异引起的问题。
author: angelad116
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44658ea48b9f7dae76c34c5f3d8828c9e8c4ac32
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151751"
---
# <a name="bank-statement-file-import-troubleshooting"></a>银行对帐单文件导入疑难解答

[!include [banner](../includes/banner.md)]

>[!NOTE]
>此功能将于 2022 年 9 月弃用，新用户应使用电子报告。

银行的银行对帐单文件与 Microsoft Dynamics 365 Finance 支持的布局匹配非常重要。 由于银行对账单的限制标准，大多数集成将正确工作。 但是，有时报表文件不能导入或有错误结果。 通常，这些问题由银行对账单文件中的小差异引起。 此文章说明如何修复这些差异和解决问题。

## <a name="what-is-the-error"></a>错误是什么？

在尝试导入银行对账单文件后，请转到数据管理作业历史记录及其执行详细信息查找错误。 错误可以通过指定报表、余额或报表行提供帮助。 但是，不大可能提供足够的信息来帮助您确定导致问题的字段或元素。

> [!NOTE]
> 导入的银行对帐单只能在单个时间点重叠。  例如，如果对帐单于 2021 年 1 月 1 日凌晨 12:00 结束，则下一个对帐单的开始日期可能是 2021 年 1 月 1 日凌晨 12:00（即凌晨 12:00:00）。

## <a name="what-are-the-differences"></a>有哪些差异？
比较银行文件布局定义与 Finance 导入定义，注意字段和元素中的任何差异。 比较银行对账单文件与相关示例 Finance 文件。 在 ISO20022 文件中，应易于查看任何差异。

## <a name="time-zone-differences-on-imported-bank-statements"></a>导入的银行对帐单中时区不同
导入文件中的日期时间值可能与财务和运营中显示的日期时间值不同。 若要避免此项差异，请在 **配置数据源** 页中输入时区首选项。 有关输入时区首选项的详细信息，请参阅[设置高级银行对帐导入流程](set-up-advanced-bank-reconciliation-import-process.md)。

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

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  复制银行对账单文件的内容，并且将其粘贴到 XML 文件，以便替换 **PASTESTATEMENTFILEHERE**。

### <a name="debug-the-xslt"></a>调试 XSLT

有关详细信息，请参阅<https://msdn.microsoft.com/library/ms255605.aspx>。

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

调整转换以获取银行对账单文件中的相应字段或元素。 然后将该字段或元素映射到相应的 Finance 元素。

### <a name="debitcredit-indicator"></a>借方/贷方指示符

有时，借方可能导入为贷方，贷方可能导入为借方。 为了解决此问题，您必须更改相应的 XSLT。 如果银行对账单来自多个银行，请确保它们使用同一借方/贷方方法或创建单独的转换。

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator 模板
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit 模板
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator 模板

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>银行对账单格式和技术布局的示例
下表列出了高级银行对帐导入文件技术布局定义的示例和三个相关银行对账单示例文件。 您可以从此处下载示例文件和技术布局：[导入文件示例](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| 技术布局定义                             | 银行对账单示例文件          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]


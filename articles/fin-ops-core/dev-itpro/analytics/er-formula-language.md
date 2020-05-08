---
title: 电子申报公式语言
description: 本主题提供有关如何在电子申报 (ER) 中使用公式语言的信息。
author: NickSelin
manager: kfend
ms.date: 12/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 79b4640a23d4fc78ade4de57e4071abe6c9ecb56
ms.sourcegitcommit: 0d7b700950b1f95dc030ceab5bbdfd4fe1f79ace
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284348"
---
# <a name="electronic-reporting-formula-language"></a>电子申报公式语言

[!include [banner](../includes/banner.md)]

电子申报 (ER) 提供了强大的数据换算体验。 [ER 公式设计器](general-electronic-reporting-formula-designer.md)中用于表达所需数据操作的语言类似于 Microsoft Excel 中的公式语言。

## <a name="basic-syntax"></a>基本语法

ER 表达式可以包含任意或所有以下元素：

- [常量](#Constants)
- [运算符](#Operators)
- [参考](#References)
- [路径](#Paths)
- [功能](#Functions)

## <a name=""></a><a name="Constants">常量</a>

您可以在设计表达式时使用文本和数值常量（即未计算的值）。 例如，表达式 `VALUE ("100") + 20` 使用数值常量 **20** 和字符串常量 **"100"**，返回数值 **120**。

ER 公式设计器支持转义序列。 因此，可以指定应以不同方式处理的表达式字符串。 例如，表达式 `"Leo Tolstoy ""War and Peace"" Volume 1"` 返回文本字符串 **Leo Tolstoy "War and Peace" Volume 1**。

## <a name=""></a><a name="Operators">运算符</a>

下表显示您可以用于执行基本算术运算的算术运算符，例如加、减、乘和除。

| 操作员 | 含义               | 示例     |
|----------|-----------------------|-------------|
| +        | 增加额              | `1+2`       |
| -        | 减法，负 | `5-2`, `-1` |
| \*       | 乘        | `7\*8`      |
| /        | 分部              | `9/3`       |

下表显示支持的比较运算符。 您可以使用这些运算符比较两个值。

| 操作员 | 含义                  | 示例      |
|----------|--------------------------|--------------|
| =        | 相等                    | `X=Y`        |
| &gt;     | 大于             | `X>Y`        |
| &lt;     | 小于                | `X<Y`        |
| &gt;=    | 大于等于 | `X>=Y`       |
| &lt;=    | 小于等于    | `X<=Y`       |
| &lt;&gt; | 不等于             | `X<>Y`       |

也可以将星号 (&) 用作文本连接运算符。 这样就可以将一个或多个文本字符串联接或连接为一段文本。

| 操作员 | 含义     | 示例                                               |
|----------|-------------|-------------------------------------------------------|
| &        | 连接 | `"Nothing to print:" & " " & "no records found"`      |

### <a name="operator-precedence"></a>运算符优先级

复合表达式部分评估的顺序很重要。 例如，表达式 `1 + 4 / 2` 的结果根据先执行加还是除运算有所不同。 您可以使用括号明确定义表达式如何进行评估。 例如，要指示应首先执行加运算，您可以将之前的表达式更改为 `(1 + 4) / 2`。 如果不在表达式中明确指定运算顺序，顺序将基于分配给支持的运算符的默认优先级。 下表显示分配给每个运算符的优先级。 有较高优先级的运算符（例如，7）在具有较低优先级的运算符之前进行评估（例如，1）。

| 优先级 | 运算符      | 语法                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | 分组       | ( … )                                                                   |
| 6          | 成员访问  | … 。 …                                                                   |
| 5          | 函数调用  | … ( … )                                                                 |
| 4          | 乘 | … \* …<br>… / …                                                         |
| 3          | 加法的       | … + …<br>… - …                                                          |
| 2          | 比较     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | 分隔     | … , …                                                                   |

如果表达式中包含多个具有相同优先级的连续运算符，将从左到右执行这些运算。 例如，表达式 `1 + 6 / 2 \* 3 > 5` 返回 **true**。 我们建议您使用括号明确指示评估表达式中所需的运算顺序，以使表达式更便于读取和维护。

## <a name=""></a><a name="References">参考</a>

在表达式设计期间当前 ER 组件的所有数据源均可用作指定引用。 当前的 ER 组件可以是模型映射或格式。 例如，当前的 ER 模型映射包含数据源 **ReportingDate** 数据源，该数据源返回 *DateTime* 数据类型的值。 若要获取在生成文档中正确格式化的值，您可以按照如下方法在表达式中引用数据源：`DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")`。

不代表字母的引用数据源的名称中的所有字符必须前加单引号 (')。 如果引用数据源的名称包含至少一个不代表字母的符号，名称必须以单引号括起。 例如，这些非字母符号可以是标点符号或其他书面符号。 下面举了一些示例加以说明：

- **今日日期和时间**数据源必须在 ER 表达式中引用，如下所示：`'Today''s date & time'`。
- **Customers** 数据源的 **name()** 方法必须在 ER 表达式中引用，如下所示：`Customers.'name()'`。

如果应用程序数据源的方法有参数，则使用下面的语法调用这些方法：

- 如果 **System** 数据源的 **isLanguageRTL** 方法具有 *String* 数据类型的 **EN-US** 参数，则该方法必须在 ER 表达式中引用为 `System.isLanguageRTL("EN-US")`。
- 当方法名称仅包含一个字母数字符号时，引号不是必需的。 但是，如果名称中包含括号，则它们是表方法所必需的。

当 **System** 数据源被添加到引用**全局**应用程序类的 ER 映射时，表达式 `System.isLanguageRTL("EN-US ")` 返回*布尔*值 **FALSE**。 修改后的表达式 `System.isLanguageRTL("AR")` 返回*布尔*值 **TRUE**。

可限制值传递到此类型方法的参数的方式：

- 只有常量可传递到此类型的方法。 常量的值定义为设计时间。
- 此类型的参数仅支持原始（基本）数据类型。 原始数据类型包括*整数*、*实数*、*布尔值*、*字符串*。

## <a name=""></a><a name="Paths">路径</a>

在表达式引用结构化的数据源时，可以使用路径定义选择该数据源的特定基本元素。 点字符 (.) 用于分离结构化数据源的各个元素。 例如，当前的 ER 模型映射包含 **InvoiceTransactions** 数据源，并且该数据源返回记录列表。 **InvoiceTransactions** 记录结构包含 **AmountDebit** 和 **AmountCredit** 字段，并且这两个字段都将返回数值。 因此，您可以设计以下表达式来计算开票金额：`InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit`。 此表达式中的 `InvoiceTransactions.AmountDebit` 构造是用于访问*记录列表*类型的 **InvoiceTransactions** 数据源的 **AmountDebit** 字段的路径。

### <a name="relative-path"></a>相对路径

如果结构化数据源的路径以“at”符号 (@) 开头，它是相对路径。 显示的是“at”符号，而不是所使用的层次结构树结构的绝对路径的其余部分。 下图显示了一个示例。 在这里，绝对路径 `Ledger.'accountingCurrency()'` 表示来自**分类帐**数据源的记帐币种值已输入到数据模型的 **AccountingCurrency** 字段中。

![ER 模型映射设计器页面上的绝对路径的示例](./media/ER-FormulaLanguage-AbsolutePath.png)

下图中的示例显示了如何使用相对路径。 相对路径 `@.AccountNum` 表示 **Intrastat** 数据源（在数据模型层次结构树中的 **AccountNum** 字段上方显示一个级别）的 **AccountNum** 字段用于在数据模型的 **AccountNum** 字段中输入客户或供应商帐号。

![ER 模型映射设计器页面上的相对路径的示例](./media/ER-FormulaLanguage-RelativePath1.png)

绝对路径的其余部分还显示在 [ER 公式编辑器](general-electronic-reporting-formula-designer.md)中。

![ER 公式设计器页面上绝对路径的其余部分](./media/ER-FormulaLanguage-RelativePath2.png)

## <a name=""></a><a name="Functions">功能</a>

ER 内置函数可以在 ER 表达式中使用。 根据调用函数参数的列表，可将表达式上下文（即当前 ER 模型映射或 ER 格式）的所有数据源用作调用函数的参数，以便与调用函数的参数列表保持一致。 也可以将常量用作调用函数的参数。 例如，当前的 ER 模型映射包含 **InvoiceTransactions** 数据源，并且该数据源返回记录列表。 **InvoiceTransactions** 记录结构包含 **AmountDebit** 和 **AmountCredit** 字段，并且这两个字段都将返回数值。 因此，若要计算发票金额，可以设计使用内置的 ER 舍入函数的以下表达式：`ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)`。

设计 ER 模型映射和 ER 报表时，可以使用以下类别的 ER 函数：

- [日期和时间函数](er-functions-category-datetime.md)
- [列表函数](er-functions-category-list.md)
- [逻辑函数](er-functions-category-logical.md)
- [数学函数](er-functions-category-mathematical.md)
- [记录函数](er-functions-category-record.md)
- [文本函数](er-functions-category-text.md)
- [数据收集功能](er-functions-category-data-collection.md)
- [其他（业务域特定的）函数](er-functions-category-other.md)
- [类型转换函数](er-functions-category-type-conversion.md)

## <a name="functions-list-extension"></a>函数的列表扩展

ER 允许您扩展 ER 表达式中使用的函数列表的功能。 需要执行一些工程工作。 有关详细信息，请参阅[扩展电子申报 (ER) 功能的列表](general-electronic-reporting-formulas-list-extension.md)。

## <a name="compound-expressions"></a>复合表达式

如果数据类型匹配，您可以创建使用不同类别函数的复合表达式。 将函数一起使用时，将一个函数的输出数据类型与另一函数所需的输入数据类型匹配。 例如，为避免在将字段绑定到 ER 格式元素时可能出现的“列表为空”错误，请将[列表](er-functions-category-list.md)类别的函数与[逻辑](er-functions-category-logical.md)类别的函数组合，如下例所示。 在这里，公式使用 [IF](er-functions-logical-if.md) 函数测试 **IntrastatTotals** 列表在从该列表返回所需聚合的值之前是否为空。 如果 **IntrastatTotals** 列表为空，公式将返回 **0**（零）。

```vb
IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="multiple-solutions"></a>多种解决方案

通常，通过使用不同类别的函数或相同类别的不同函数，您可以通过多种方式获得相同的数据换算结果。 例如，也可以使用[列表](er-functions-category-list.md)类别的 [COUNT](er-functions-list-count.md) 函数来配置前一个表达式。

```vb
IF(COUNT (IntrastatTotals)=0, 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="additional-resources"></a>其他资源

[电子申报概览](general-electronic-reporting.md)

[电子报告中的配方设计器](general-electronic-reporting-formula-designer.md)

[扩展电子报告功能的列表](general-electronic-reporting-formulas-list-extension.md)

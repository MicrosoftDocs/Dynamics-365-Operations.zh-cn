---
title: 电子申报公式支持的原始数据类型
description: 本主题提供有关电子申报 (ER) 公式支持的原始数据类型的信息。
author: NickSelin
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e1c70dd0fa89c6cc5a8b4778b073d1cf4a3dadd
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355314"
---
# <a name="supported-primitive-data-types-for-electronic-reporting-formulas"></a>电子申报公式支持的原始数据类型

[!include [banner](../includes/banner.md)]

本主题提供有关[电子申报 (ER)](general-electronic-reporting.md) 表达式支持的原始数据类型的信息。 下面是原始数据类型的列表：

- [布尔](#boolean)
- [日期](#date)
- [日期/时间](#datetime)
- [枚举](#enumeration)
- [guid](#guid)
- [整数](#integer)
- [int64](#int64)
- [实数](#real)
- [字符串](#string)

## <a name="boolean"></a><a name="boolean"></a>布尔

*布尔* 原始数据类型包含评估为 *true* 或 *false* 的值。 您可以在预计 *布尔* 表达式的情况下，使用保留的文本关键字 **True** 和 **False**。 默认值为 *false*。

*布尔* 的内部表示为 *整数*。 *整数* 值 0（零）评估为 *false*，所有其他 *整数* 值评估为 *true*。 当您 [验证](general-electronic-reporting-formula-designer.md#TestFormula)在 [ER 公式设计器](er-advanced-formula-editor.md)中返回 *布尔* 的配置表达式时，如果表达式返回 *false*，测试结果窗格显示 *0*（零）。 否则，测试结果窗格显示 *1*。

*布尔* 没有隐式转换。 但是，您可以使用 [TEXT](er-functions-text-text.md) 函数将 *布尔* 显式转换为 *字符串*。

- *false* 值转换为文本字符串 **False**。
- *true* 值转换为文本字符串 **True**。

> [!NOTE]
> 此转换不依赖于提供的语言和文化[上下文](er-design-multilingual-reports.md)。

比较 [运算符](er-formula-language.md#Operators)是唯一可以与 *布尔* 数据类型一起使用的运算符类型。 以下运算符可用于比较两个 *布尔* 值：\<\> 和 =。

## <a name="date"></a><a name="date"></a>日期

*日期* 原始数据类型包含日、月和年。 可以使用以下函数启动日期：

- [DATEVALUE](er-functions-datetime-datevalue.md)
- [NULLDATE](er-functions-datetime-nulldate.md)
- [SESSIONTODAY](er-functions-datetime-sessiontoday.md)
- [TODAY](er-functions-datetime-today.md)

*日期* 数据类型可以保留 1900 年 1 月 1 日和 2154 年 12 月 31 日之间的日期。 默认值为 **null**，内部表示为 1900 年 1 月 1 日的日期。

*数据* 没有隐式转换。 但是，您可以使用以下显式转换函数：

- [DATEFORMAT](er-functions-datetime-dateformat.md)
- [DATETODATETIME](er-functions-datetime-datetodatetime.md)
- [TEXT](er-functions-text-text.md)

[ADDDAYS](er-functions-datetime-adddays.md) 函数可让您从日期中添加和减去天数。 通过这种方式，您可以将特定天数的日期移动到将来和过去。 [DAYS](er-functions-datetime-days.md) 函数可让您将日期相互减去并计算天数差异。 有关转换 *日期* 值的详细信息，请参阅[日期和时间类别中的 ER 函数列表](er-functions-category-datetime.md)。

比较 [运算符](er-formula-language.md#Operators)是唯一可以与 *日期* 数据类型一起使用的运算符类型。 以下运算符可用于比较两个 *日期* 值：\<\>、\<, \<=, =, \> 和 \>=。

## <a name="datetime"></a><a name="datetime"></a>DateTime

*日期/时间* 原始数据类型结合 *日期* 类型和一个表示自午夜以来经过的时间的值。 时间以小时、分钟、秒和秒的分数表示。 *日期/时间* 值还保留与时区相关的信息。

*日期/时间* 数据类型可以保留 1900 年 1 月 1 日（1900-01-01T00:00:00.0000000+00:00，采用往返[格式](/dotnet/standard/base-types/standard-date-and-time-format-strings)）和 2154 年 12 月 31 日（2154/12/31T11:59:59.9999999+00:00，采用往返格式）之间的日期。 *日期/时间* 的最小时间单位是千万分之一秒。

> [!NOTE]
> 当针对小时使用 **hh** [说明符](/dotnet/standard/base-types/standard-date-and-time-format-strings)时，高于 12:59:59:9999999 的时间值不能解释为有效时间。
>
> 当针对小时使用 **HH** 说明符时，高于 23:59:59:9999999 的时间值不能解释为有效时间。

默认值为 **null**，内部表示为 1900 年 1 月 1 日的日期（1900-01-01T00:00:00.0000000+00:00，采用往返格式）。

可以使用以下函数启动日期/时间：

- [DATETIMEVALUE](er-functions-datetime-datetimevalue.md)
- [NULNULLDATETIMELDATE](er-functions-datetime-nulldatetime.md)
- [SESSIONNOW](er-functions-datetime-sessionnow.md)
- [NOW](er-functions-datetime-now.md)

*日期/时间* 没有隐式转换。 但是，您可以使用以下显式转换函数：

- [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md)
- [TEXT](er-functions-text-text.md)

有关转换 *日期/时间* 值的详细信息，请参阅[日期和时间类别中的 ER 函数列表](er-functions-category-datetime.md)。

比较 [运算符](er-formula-language.md#Operators)是唯一可以与 *日期/时间* 数据类型一起使用的运算符类型。 以下运算符可用于比较两个 *日期/时间* 值：\<\>、\<, \<=, =, \> 和 \>=。

## <a name="enumeration"></a><a name="enumeration"></a>枚举

*枚举* 原始数据类型是文本的列表。 您可以使用在应用程序[源代码](../dev-ref/xpp-data-primitive.md#enum)中定义的枚举。 您还可以在 ER [数据模型](general-electronic-reporting.md#data-model-and-model-mapping-components)和 ER [格式](general-electronic-reporting.md#FormatComponentOutbound)组件中引入自己的枚举。

应用程序 *枚举* 可用于任何 ER 模型映射和 ER 格式的表达式中。

下图显示了您可以如何将 **CustVendCorrectiveReasonCode** 模型枚举添加到可编辑的 ER 数据模型。

[![在 ER 数据模型设计器中配置模型枚举。](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)

模型 *枚举* 可用于已在引入了 *枚举* 的数据模型下创建的任何 ER 模型映射和 ER 格式的表达式中。

下图显示了您可以如何将 **Natura 冲销费用子类别的列表** 格式枚举添加到可编辑的 ER 格式。

[![在 ER 格式设计器中配置格式枚举。](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)

格式 *枚举* 仅可用于引入了 *枚举* 的 ER 格式的表达式中。

您必须使用适当类型的 ER 数据源，将特定枚举作为常量或作为值（运行 ER 解决方案的用户在运行时在对话框中定义）引入到配置的 ER 组件。

- 可以使用 **Dynamics 365 for Operations \ 枚举** 和 **常规 \ 用户输入参数** 数据源访问应用程序枚举。 下图显示了您可以如何将引用 **NoYes** 应用程序枚举的 **appenumNoYes** 和 **uipNoYes** 数据源添加到可编辑的 ER 格式。

    [![在 ER 格式设计器中添加应用程序枚举数据源。](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)

- 可以使用 **数据模型 \ 枚举** 和 **数据模型 \ 枚举用户输入参数** 数据源访问数据模型枚举。 下图显示了您可以如何将引用 **CustVendCorrectiveReasonCode** 数据模型枚举的 **CustVendCorrectiveReasonCode** 数据源添加到可编辑的 ER 格式。

    [![在 ER 格式设计器中添加模型枚举数据源。](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)

- 可以使用 **格式 \ 枚举** 和 **格式 \ 枚举用户输入参数** 数据源访问格式枚举。 下图显示了您可以如何将引用 **Natura 冲销费用子类别** 格式枚举的 **NaturaReverseCharge** 数据源添加到可编辑的 ER 格式。

    [![在 ER 格式设计器中添加格式枚举数据源。](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)

*枚举* 没有隐式转换。 但是，您可以使用 [TEXT](er-functions-text-text.md) 转换函数将 *枚举* 转换为文本字符串。 此转换与语言无关。 若要了解您可以如何将 *枚举* 值与特定于语言的相应标签相关联，请参阅 [LISTOFFIELDS](er-functions-list-listoffields.md) 和 [GETENUMVALUEBYNAME](er-functions-text-getenumvaluebyname.md) 函数的使用示例。

比较 [运算符](er-formula-language.md#Operators)是唯一可以与 *枚举* 数据类型一起使用的运算符类型。 以下运算符可用于比较两个 *枚举* 值：\<\> 和 =。

## <a name="guid"></a><a name="guid"></a>Guid

*guid* 原始数据类型保留全局唯一标识符 (GUID) 值。 GUID 是可用于所有计算机和网络的值，只需要唯一标识符即可。 该数字不太可能重复。 有效的 GUID 满足以下所有规范：

- 必须有 32 个十六进制数字。
- 此外，必须在以下位置嵌入四个破折号：8-4-4-4-12。
- 此外，可以选择在字符串的开头和结尾添加大括号 \{\}。 例如，**\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}** 和 **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** 都是有效的 GUID 字符串。
- 因此，总共必须有 36 或 38 个字符，具体取决于是否添加大括号。
- 用作十六进制数字的字母可以是大写 (A–F)、小写 (a–f) 或大小写混合。

可以使用以下显式转换函数：

- [GUIDVALUE](er-functions-text-guidvalue.md)
- [TEXT](er-functions-text-text.md)

比较 [运算符](er-formula-language.md#Operators)是唯一可以与 *guid* 数据类型一起使用的运算符类型。 以下运算符可用于比较两个 *guid* 值：\<\> 和 =。

## <a name="integer"></a><a name="integer"></a>整数

*整数* 原始数据类型表示没有小数位的数字。 整数用作重复语句中的控制变量或记录列表中的索引。

*整数* 文本是直接在 ER [表达式](general-electronic-reporting-formula-designer.md#formula-designer-overview)（公式）中输入的整数，例如 **12345**。 *整数* 是 32 位宽。 默认值为 **0**，内部表示是一个长数字。 *整数* 会自动转换为 *实数*.

此外，可以使用以下显式转换函数：

- [INTVALUE](er-functions-conversion-intvalue.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

*整数* 的范围为 \[-2,147,483,647 : 2,147,483,647\]。 此范围的所有整数都可用作文本。

所有比较和数学 [运算符](er-formula-language.md#Operators)都可以与 *整数* 数据类型一起使用。

## <a name="int64"></a><a name="int64"></a>Int64

*int64* 原始数据类型表示没有小数位的数字。 *Int64* 值用作重复语句中的控制变量或记录标识符。

*int64* 是 64 位宽。 默认值为 **0**，内部表示是一个长数字。 *int64* 会自动转换为 *实数*.

此外，可以使用以下显式转换函数：

- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

*int64* 的范围为 \[-9,223,372,036,854,775,807 : 9,223,372,036,854,775,807\]。

所有比较和数学 [运算符](er-formula-language.md#Operators)都可以与 *int64* 数据类型一起使用。

## <a name="real"></a><a name="real"></a>实数

除了整数之外，*实数* 原始数据类型也可以保留十进制值。 您可以在预计 *实数* 的任何位置使用十进制文本。 十进制文本是在代码中直接输入的十进制，例如 **2.19**。

> [!NOTE]
> 在 ER 表达式中，句点 (.) 始终用作十进制分隔符。

实数可用于所有表达式，并且可与比较运算符和算术运算符一起使用。 *实数* 具有 16 位有效数字的精度。 *实数* 的默认值为 **0.0**，内部表示为二进制编码数字 (BCD)。 BCD 编码可以精确表示 0.1 的倍数的值。 *实数* 变量的范围为 -(10)<sup>127</sup> 到 (10)<sup>127</sup>。 在 ER 表达式中，此范围内的所有实数都可以用作文本。

*实数* 没有隐式转换。 但是，您可以使用以下函数显式将 *实数* 转换为其他数据类型，并将其他数据类型转换为 *实数*：

- [INTVALUE](er-functions-conversion-intvalue.md)
- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)
- [VALUE](er-functions-conversion-value.md)

所有比较和数学 [运算符](er-formula-language.md#Operators)都可以与 *实数* 数据类型一起使用。

## <a name="string"></a><a name="string"></a>字符串

*字符串* 原始数据类型表示用作文本、帐号、地址和电话号码的字符串序列。

*字符串* 文本是字符，用双引号 ("") 引起来。 可以在 ER 表达式中预计 *字符串* 值的任何位置使用 *字符串* 文本。 您可以在逻辑表达式中使用字符串，例如比较。 还可以使用 **\&** 运算符或 [CONCATENATE](er-functions-text-concatenate.md) 函数串联 *字符串* 值。

> [!NOTE]
> 如果串联两个 *字符串* 值，并且想要生成的 *字符串* 跨越多行，请在值之间使用换行符分隔符。 对于 TEXT 输出，此分隔符可以是使用 [CHAR](er-functions-text-char.md)(10) 或 CHAR(13) 表达式生成的字符。 对于 HTML，它可以是 **\<br\>** 标记。

*字符串* 的默认值为没有字符的空白文本字符串，内部表示为字符列表。

字符串没有自动转换。 但是，可以使用以下显式转换函数：

- [CHAR](er-functions-text-char.md)
- [FORMAT](er-functions-text-format.md)
- [LEFT](er-functions-text-left.md)
- [LEN](er-functions-text-len.md)
- [MID](er-functions-text-mid.md)
- [PADLEFT](er-functions-text-padleft.md)
- [REPLACE](er-functions-text-replace.md)
- [RIGHT](er-functions-text-right.md)
- [TEXT](er-functions-text-text.md)
- [TRANSLATE](er-functions-text-translate.md)
- [TRIM](er-functions-text-trim.md)
- [UPPER](er-functions-text-upper.md)

有关转换 *字符串* 值的详细信息，请参阅[文本类别的 ER 函数列表](er-functions-category-text.md)。

*字符串* 可以保留无限数量的字符。

所有比较 [运算符](er-formula-language.md#Operators)都可以与 *字符串* 数据类型一起使用。

## <a name="additional-resources"></a>其他资源

- [电子申报概览](general-electronic-reporting.md)
- [电子申报公式语言](er-formula-language.md)
- [支持的复合数据类型](er-formula-supported-data-types-composite.md)

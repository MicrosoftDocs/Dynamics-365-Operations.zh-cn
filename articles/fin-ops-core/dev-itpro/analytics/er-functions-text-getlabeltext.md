---
title: GETLABELTEXT ER 函数
description: 本文提供有关 GETLABELTEXT 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 03/18/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: dad87548518b77f2def1cf2383a21607f45170e1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285930"
---
# <a name="getlabeltext-er-function"></a>GETLABELTEXT ER 函数

[!include [banner](../includes/banner.md)]

`GETLABELTEXT` 函数搜索特定标签以返回一个 *[字符串](er-formula-supported-data-types-primitive.md#string)* 值，该值表示使用指定语言对指定标签的翻译。

## <a name="syntax"></a>语法

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>参数

### <a name="label-id"></a>标签 ID

`label id`：*字符串* 或 *标签 ID*

以下标签类型之一的有效 ID：

- [电子报告 (ER)](general-electronic-reporting.md) 标签
- Microsoft Dynamics 365 Finance 标签

#### <a name="usage-notes"></a>使用说明

此参数只能通过使用以下支持的模式之一定义为常量：

- 对于 ER 标签：

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- 对于 Finance 标签：

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> 在设计时，如果使用提供的标签 ID 找不到标签，将会在 **[公式设计器](er-advanced-formula-editor.md)** 页面上显示验证错误消息。

### <a name="language"></a>语言

`language`：*字符串*

表示语言代码的字符串。

#### <a name="usage-notes"></a>使用说明

此参数可以定义为文本常量或返回 *字符串* 值的数据源字段的路径。

> [!NOTE]
> 在设计时，如果在提供的 `language` 参数定义为文本常量时使用该参数找不到语言代码，将会显示验证错误消息。
>
> 在运行时，如果使用提供的 `language` 参数找不到语言代码，将返回指定标签的 `EN-US` 系统语言的翻译。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example-1-system-label"></a><a name=example-1></a>示例 1：系统标签

表达式 `GETLABELTEXT (@"SYS70894", "en-us")` 和 `GETLABELTEXT ("SYS70894", "en-us")` 返回 `@SYS70894` 应用程序标签的英文翻译“Nothing to print”。

## <a name="example-2-er-label"></a><a name=example-2></a>示例 2：ER 标签

您开始编辑从 **ISO20022 贷方转帐 (DE)** 配置 [派生](er-quick-start2-customize-report.md#DeriveProvidedFormat)的 ER [配置](general-electronic-reporting.md#Configuration)，输入 *[计算字段](er-calculated-field-ds-performance.md)* 类型的新数据源，并为此数据源配置表达式 `GETLABELTEXT(@"GER_LABEL:VendorName", "de")`。 在这种情况下，在运行时，数据源会返回最初在基本 **ISO20022 贷方转帐 (DE)** ER 配置中配置的 `@GER_LABEL:VendorName` ER 标签的德语翻译“Kreditorenname”。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)

[在电子报告中设计多语言报告](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: GETENUMVALUEBYNAME ER 函数
description: 本文提供有关 GETENUMVALUEBYNAME 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 09/23/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1ebadd72dda296de67ac041957cffb9ab407b7c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858703"
---
# <a name="getenumvaluebyname-er-function"></a>GETENUMVALUEBYNAME ER 函数

[!include [banner](../includes/banner.md)]

`GETENUMVALUEBYNAME` 函数通过使用指定为 *字符串* 值的枚举名称在指定的枚举数据源中搜索特定的 *枚举* 值。 如果找到 *枚举* 值，函数将返回此值。 否则，此函数将返回 **空** 枚举值。

## <a name="syntax"></a>语法

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>参数

`enumeration data source path`：*枚举*

下列枚举类型之一的数据源的有效路径：

- 电子申报 (ER) 模型枚举
- ER 格式枚举
- Microsoft Dynamics 365 Finance 枚举

`enumeration value text`：*字符串*

代表单个枚举值的名称的字符串值。

## <a name="return-values"></a>返回值

可空 *枚举*

生成的枚举值。

## <a name="usage-notes"></a>使用说明

如果使用指定为 *字符串* 值的枚举值的名称未找到 *枚举* 值，不会引发异常。

## <a name="example-1"></a>示例 1

在下图中，数据模型中引入了 **ReportDirection** 枚举。 请注意，为枚举值定义标签。

![数据模型枚举的可用值。](./media/ER-data-model-enumeration-values.PNG)

下图显示以下详细信息：

- **$Direction** 数据源在 ER 报表中配置。 此数据源是根据 **ReportDirection** 模型枚举配置的。
- `$IsArrivals` 表达式设计为将基于模型枚举的 **$Direction** 数据源用作此函数的参数。
- 此比较表达式的值为 **TRUE**。

![数据模型枚举的示例。](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a>示例 2

`GETENUMVALUEBYNAME` 和 [`LISTOFFIELDS`](er-functions-list-listoffields.md) 函数可让您作为文本值提取支持的枚举的值和标签。 （支持的枚举有应用程序枚举、数据模型枚举和格式枚举。）

在下图中，模型映射中引入了 **TransType** 数据源。 此数据源引用 **LedgerTransType** 应用程序枚举。

![引用应用程序枚举的模型映射的数据源。](./media/er-functions-text-getenumvaluebyname-example2-1.png)

下图显示了在模型映射中配置的 **TransTypeList** 数据源。 此数据源是根据 **TransType** 应用程序枚举配置的。 `LISTOFFIELDS` 函数用于将所有枚举值作为包含字段的记录列表返回。 这样，每个枚举值的详细信息都将公开。

> [!NOTE]
> 将使用 `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` 表达式为 **TransTypeList** 数据源配置 **EnumValue** 字段。 此字段为此列表中的每个记录返回枚举值。

![作为记录列表返回选定枚举的所有枚举值的模型映射的数据源。](./media/er-functions-text-getenumvaluebyname-example2-2.png)

下图显示了在模型映射中配置的 **VendTrans** 数据源。 此数据源从 **VendTrans** 应用程序表返回供应商交易记录。 每个交易记录的分类帐类型由 **TransType** 字段的值定义。

> [!NOTE]
> 将使用 `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` 表达式为 **VendTrans** 数据源配置 **TransTypeTitle** 字段。 此字段以文本形式返回当前交易记录的枚举值的标签（如果此枚举值可用）。 否则，将返回一个空字符串值。
>
> **TransTypeTitle** 字段将绑定到数据模型的 **LedgerType** 字段，让此信息可以在使用该数据模型作为数据源的每个 ER 格式中使用。

![返回供应商交易的模型映射的数据源。](./media/er-functions-text-getenumvaluebyname-example2-3.png)

下图显示了如何使用[数据源调试器](er-debug-data-sources.md)测试配置的模型映射。

![使用数据源调试器测试配置的模型映射。](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

数据模型的 **LedgerType** 字段预期将公开交易记录类型的标签。

如果您计划将这种方法用于大量交易记录数据，则必须考虑执行性能。 有关详细信息，请参阅[跟踪 ER 格式的执行以解决性能问题](trace-execution-er-troubleshoot-perf.md)。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)

[跟踪电子申报格式的执行以解决性能问题](trace-execution-er-troubleshoot-perf.md)

[LISTOFFIELDS ER 函数](er-functions-list-listoffields.md)

[FIRSTORNULL ER 函数](er-functions-list-firstornull.md)

[WHERE ER 函数](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
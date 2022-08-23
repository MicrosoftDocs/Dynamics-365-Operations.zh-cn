---
title: JSONVALUE ER 函数
description: 本文提供有关 JSONVALUE 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 10/25/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: fba1141bce91fd7c9da3cd21aef13ce99329f379
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267954"
---
# <a name="jsonvalue-er-function"></a>JSONVALUE ER 函数

[!include [banner](../includes/banner.md)]

`JSONVALUE` 函数分析在指定路径访问且格式为 JavaScript Object Notation (JSON) 的数据，并提取具有指定 ID 的标量值。 然后将提取的标量值返回为 *字符串* 值。

## <a name="syntax"></a>语法

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>参数

`input`：*字符串*

包含 JSON 数据的 *字符串* 类型的数据源的有效路径。

`path`：*字符串*

JSON 数据的标量值的标识符。 使用正斜杠 (/) 分隔相关 JSON 节点的名称。 使用括号 (\[\]) 表示法指定 JSON 数组中特定值的索引。 请注意，此索引使用了从零开始的编号。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example-1"></a>示例 1

**JsonField** 数据源包含 JSON 格式的以下数据：**{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**。 在此例中，表达式 `JSONVALUE (JsonField, "BuildNumber")` 返回 *字符串* 数据类型的以下值：**"7.3.1234.1"**。

## <a name="example-2"></a>示例 2

*计算字段* 类型的 **JsonField** 数据源包含以下表达式：`"{""workers"": [ {""name"": ""Adam"", ""age"": 30, ""emails"": [""AdamS@Contoso.com"", ""AdamS@Hotmail.com"" ]}, { ""name"": ""John"", ""age"": 21, ""emails"": [""JohnS@Contoso.com"", ""JohnS@Aol.com""]}]}"`

此表达式配置为返回一个 [*字符串*](er-formula-supported-data-types-primitive.md#string)值，此值以 JSON 格式表示以下数据。

```json
{
    "workers": [
        {
            "name": "Adam",
            "age": 30,
            "emails": [ "AdamS@Contoso.com", "AdamS@Hotmail.com" ]
        },
        {
            "name": "John",
            "age": 21,
            "emails": [ "JohnS@Contoso.com", "JohnS@Aol.com" ]
        }
    ]
}
```

在此例中，表达式 `JSONVALUE(json, "workers/[1]/emails/[0]")` 返回 *字符串* 数据类型的以下值：`JohnS@Contoso.com`。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

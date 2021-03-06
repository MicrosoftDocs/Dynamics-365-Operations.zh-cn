---
title: JSONVALUE ER 函数
description: 本主题提供有关 JSONVALUE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/11/2019
ms.topic: article
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
ms.openlocfilehash: e8336e43a236e3f3b875fb3cb81bc139507673c2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746355"
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

JSON 数据的标量值的标识符。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example"></a>示例

**JsonField** 数据源包含 JSON 格式的以下数据：**{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**。 在此例中，表达式 `JSONVALUE (JsonField, "BuildNumber")` 返回 *字符串* 数据类型的以下值：**"7.3.1234.1"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
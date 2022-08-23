---
title: EMPTYRECORD ER 函数
description: 本文提供有关 EMPTYRECORD 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 5046a1cb43f12863ddbdf241e8ba72071d1016ce
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280146"
---
# <a name="emptyrecord-er-function"></a>EMPTYRECORD ER 函数

[!include [banner](../includes/banner.md)]

`EMPTYRECORD` 函数返回与指定记录列表或记录具有相同结构的空 *容器（记录）* 值。

## <a name="syntax"></a>语法

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a>参数

`list`：*记录列表* 或 *容器（记录）*

*记录列表* 或 *容器（记录）* 类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*容器（记录）*

生成的记录值。

## <a name="usage-notes"></a>使用说明

> [!NOTE] 
> null 记录为其中的所有字符串都有空值的记录。 空值对于数字来说为 **0**（零），对于字符串来说为空字符串，依此类推。

## <a name="example"></a>示例

`EMPTYRECORD (SPLIT ("abc", 1))` 返回具有与 `SPLIT` 函数返回的列表相同结构的新空记录。 有关详细信息，请参阅 [SPLIT](er-functions-list-split.md)。

## <a name="additional-resources"></a>其他资源

[记录函数](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

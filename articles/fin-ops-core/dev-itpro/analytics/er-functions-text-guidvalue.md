---
title: GUIDVALUE ER 函数
description: 本主题提供有关 GUIDVALUE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 8b4c65063cd22b5370ca6000a32c6fd1cc9ce6b6
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743823"
---
# <a name="guidvalue-er-function"></a>GUIDVALUE ER 函数

[!include [banner](../includes/banner.md)]

`GUIDVALUE` 函数将*字符串*类型的指定输入转换为 *GUID* 类型的数据项。

## <a name="syntax"></a>语法

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a>参数

`input`：*字符串*

*字符串*类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*GUID*

生成的全局唯一标识符 (GUID) 值。

## <a name="usage-notes"></a>使用说明

若要执行反向转换（即，将指定的 *GUID* 数据类型的输入转换为*字符串*数据类型的数据项），您可以使用 [TEXT](er-functions-text-text.md) 函数。

## <a name="example"></a>示例

在模型映射中定义以下数据源：

- 包含表达式 `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")` 的*计算字段*类型的 **myID** 数据源
- 引用 UserInfo 表的*表记录*类型的 **Users** 数据源

然后，您可以使用 `FILTER (Users, Users.objectId = myID)` 等表达式来按 *GUID* 数据类型的 **objectId** 字段筛选 UserInfo 表。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)

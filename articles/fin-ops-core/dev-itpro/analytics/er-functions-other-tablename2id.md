---
title: TABLENAME2ID ER 函数
description: 本文提供有关 TABLENAME2ID 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: b5deea69d5c43be599ccf02c0344ba8d662a6e0f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886840"
---
# <a name="tablename2id-er-function"></a>TABLENAME2ID ER 函数

[!include [banner](../includes/banner.md)]

`TABLENAME2ID` 函数作为 *整数* 值返回指定表名称的表 ID 的数字表示。

## <a name="syntax"></a>语法

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a>参数

`text`：*字符串*

代表有效表名的文本值。

## <a name="return-values"></a>返回值

*整数*

生成的数字值。

## <a name="usage-notes"></a>使用说明

在 Microsoft Dynamics 365 Finance 的不同实例中，执行此函数可能产生不同的结果，即使使用相同的公司名称。

## <a name="example"></a>示例

`TABLENAME2ID ("Intrastat")` 将返回 **1510**。

## <a name="additional-resources"></a>其他资源

[其他（业务域特定的）函数](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
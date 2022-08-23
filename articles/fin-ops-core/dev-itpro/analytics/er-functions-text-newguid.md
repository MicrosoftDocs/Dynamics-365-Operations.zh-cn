---
title: NEWGUID ER 函数
description: 本文提供有关 NEWGUID 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 381dbcbe816c189c1966ffe962020d5aa2b1f3eb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274763"
---
# <a name="newguid-er-function"></a>NEWGUID ER 函数

[!include [banner](../includes/banner.md)]

`NEWGUID` 函数生成一个新的全局唯一标识符 (GUID) 并将其作为 *[GUID](er-formula-supported-data-types-primitive.md#guid)* 值返回。

## <a name="syntax"></a>语法

```vb
NEWGUID ()
```

## <a name="return-values"></a>返回值

*GUID*

生成的 GUID 值。

## <a name="example"></a>示例

`NEWGUID()` 始终返回新的 *GUID* 值，如 **3afcf7ff-af10-ec11-b6e6-000d3a13209e**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

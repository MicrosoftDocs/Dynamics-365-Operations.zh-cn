---
title: NEWGUID ER 函数
description: 本主题提供有关 NEWGUID 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 5856a4d765f5136ecb11a34e0255c1ba88818f2c
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647922"
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

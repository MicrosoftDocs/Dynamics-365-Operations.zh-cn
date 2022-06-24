---
title: 容器类别的 ER 函数列表
description: 本文提供有关电子报告 (ER) 支持的容器函数的信息。
author: NickSelin
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 5c86b0ae6cbf4ac6515491b55390d42c371eae4b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883808"
---
# <a name="list-of-er-functions-in-the-container-category"></a>容器类别的 ER 函数列表

[!include [banner](../includes/banner.md)]

[电子报告 (ER)](general-electronic-reporting.md) 容器 [函数](er-formula-language.md#Functions)可用于执行涉及 *容器* 数据类型的数据源的操作。 当处理数据表示二进制大型对象 (BLOB) 格式的二进制数据的集合时，将发生这些操作。 本文提供这些函数的概要。

## <a name="list-of-supported-functions"></a>支持的函数列表

| 函数 | 说明 |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | 此函数返回一个 *容器* 值，此值由从表示二进制到文本编码方案 Base64 组的指定 ASCII 字符串解码的二进制内容组成。 |

## <a name="additional-resources"></a>其他资源

[电子申报概览](general-electronic-reporting.md)

[电子报告中的配方设计器](general-electronic-reporting-formula-designer.md)

[电子申报公式语言](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

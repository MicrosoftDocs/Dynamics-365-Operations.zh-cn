---
title: 容器类别的 ER 函数列表
description: 本文提供有关电子报告 (ER) 支持的容器函数的信息。
author: kfend
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: f07c3645f824fc2fe8ca156c8cf06840e993a9a5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282642"
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

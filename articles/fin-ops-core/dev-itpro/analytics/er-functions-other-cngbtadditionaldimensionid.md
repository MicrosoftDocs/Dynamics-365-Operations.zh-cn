---
title: CN_GBT_ADDITIONALDIMENSIONID ER 函数
description: 本文提供有关 CN_GBT_ADDITIONALDIMENSIONID 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 0ed2593f865a4764b1c6172722d701a0a10ba5f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281743"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a>CN_GBT_ADDITIONALDIMENSIONID ER 函数

[!include [banner](../includes/banner.md)]

`CN_GBT_ADDITIONALDIMENSIONID` 函数返回 *字符串* 值，该值表示从指定字符串获取的单个财务维度 ID。 指定的字符串将所有维度显示为逗号分隔的 ID 列表。

## <a name="syntax"></a>语法

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a>参数

`text`：*字符串*

将所有维度显示为逗号分隔的 ID 列表的 *字符串* 值。

`number`：整数

定义指定字符串中所请求维度的序列代码的 *整数* 值。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example"></a>示例

`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` 返回 **"CC"**。

## <a name="additional-resources"></a>其他资源

[其他（业务域特定的）函数](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: SUMIF ER 函数
description: 本主题提供有关 SUMIF 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 04/27/2020
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
ms.openlocfilehash: 60cf85ac0ffcdb163c12670efa3dcc7e9f05cb16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747099"
---
# <a name="sumif-er-function"></a>SUMIF ER 函数

[!include [banner](../includes/banner.md)]

`SUMIF` 函数返回一个 *实数* 值，此值表示格式元素的绑定返回的以及在格式运行期间使用格式元素生成传出文档时收集的值的总和，并且满足指定条件。 条件包含一个键范围和一个键值。

## <a name="syntax"></a>语法

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a>参数

`key name for summing`：*字符串*

由在电子申报 (ER) 格式组件的 **已收集的数据键名** 属性中配置的表达式返回的值，组件的绑定值必须用于求和。

可以为 ER 格式组件（位于 **收集输出详细信息** 选项已打开的 **常见\\文件** 组件下）的 **序列** 组件或 **XML 元素** 组件配置 **已收集的数据键值** 属性。

## <a name="return-values"></a>返回值

*实数*

生成的数字值。

## <a name="usage-notes"></a>使用说明

在当前的 **常见\\文件** 组件的 **收集输出详细信息** 选项关闭时，此函数返回 **0**（零）值。

在 `condition range` 参数中，通配符 **"\*"** 可用于表示多个字符。

在 `condition value` 参数中，通配符 **"\*"** 可用于表示多个字符。

## <a name="example"></a>示例

有关如何使用此函数的详细信息，请参阅 [盘点和合计格式输出的 ER 使用数据](tasks/er-format-counting-summing-1.md)任务指南，这是 **购置/开发 IT 服务/解决方案组件** 业务流程的一部分。

有关使用此函数的更多信息和示例，请参阅[推迟执行 ER 格式的序列元素](er-defer-sequence-element.md#Example)和[推迟执行 ER 格式的 XML 元素](er-defer-xml-element.md#Example)。

## <a name="additional-resources"></a>其他资源

[数据收集功能](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: COLLECTEDLIST ER 函数
description: 本主题提供有关 COLLECTEDLIST 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 4650cfce76b1c2a66df820fa7660c9c421411343
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916491"
---
# <a name="COLLECTEDLIST">COLLECTEDLIST ER 函数</a>

[!include [banner](../includes/banner.md)]

`COLLECTEDLIST` 函数返回一个*记录列表*值，此值包含格式元素的**已收集的数据键值**属性返回的以及在格式运行期间使用格式元素生成传出文档时收集的值，并且满足指定条件。 每个条件包含一个键范围和一个键值。

## <a name="syntax"></a>语法

```
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a>参数

`condition 1 range`：*字符串*

由在电子申报 (ER) 格式组件的**已收集的数据键名**属性中配置的表达式返回的值。 此参数是强制性的。

`condition 1 value`：*字符串*

由在 ER 格式组件的**已收集的数据键值**属性中配置的表达式返回的值。 此参数是强制性的。

`condition N range`：*字符串*

由在 ER 格式组件的**已收集的数据键名**属性中配置的表达式返回的值。 其他参数是可选的。

`condition N value`：*字符串*

由在 ER 格式组件的**已收集的数据键值**属性中配置的表达式返回的值。 其他参数是可选的。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="usage-notes"></a>使用说明

可以为 ER 格式组件（位于**收集输出详细信息**选项已打开的**常见\\文件**组件下）的**序列**组件或 **XML 元素**组件配置**已收集的数据键名**和**已收集的数据键值**属性。

在当前的**常见\\文件**组件的**收集输出详细信息**选项关闭时，此函数返回一个空列表。

在 `condition range` 参数中，通配符 **"\*"** 可用于表示多个字符。

在 `condition value` 参数中，通配符 **"\*"** 可用于表示多个字符。

## <a name="example"></a>示例

有关如何使用此函数的详细信息，请参阅[盘点和合计格式输出的 ER 使用数据](tasks/er-format-counting-summing-1.md)任务指南，这是**购置/开发 IT 服务/解决方案组件**业务流程的一部分。

## <a name="additional-resources"></a>其他资源

[数据收集功能](er-functions-category-data-collection.md)

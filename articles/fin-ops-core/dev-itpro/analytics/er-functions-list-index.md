---
title: INDEX ER 函数
description: 本文提供有关 INDEX 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 05/20/2021
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
ms.openlocfilehash: 051a2818d862c3bc517e8c20a1742c2599c3bba6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854776"
---
# <a name="index-er-function"></a>INDEX ER 函数

[!include [banner](../includes/banner.md)]

`INDEX` 函数返回使用指定列表中的指定数字索引选择的 *容器（记录）* 值。 如果索引超出了指定列表中的记录范围，将引发异常。

## <a name="syntax"></a>语法

```vb
INDEX (list, index)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表* 数据类型的数据源的有效路径。

`index`：*整数*

指示所需记录在指定列表中的位置的数字索引。

> [!NOTE]
> 由于此函数使用从一开始的编号，因此指定值 **1** 将返回指定列表的第一条记录。

## <a name="return-values"></a>返回值

*容器（记录）*

生成的记录值。

## <a name="example-1"></a>示例 1

如果输入 *计算字段* 类型的数据源 **DS**，而该数据源中包含表达式 `SPLIT ("A|B|C", "|")`，则表达式 `DS.Value` 将返回此记录列表的第二条记录的文本值 **"B"**。 表达式 `INDEX (SPLIT ("A|B|C", "|"), 2).Value` 也会返回文本值 **"B"**。

## <a name="example-2"></a>示例 2

如果输入 *计算字段* 类型的数据源 **DS**，并且它包含表达式 `SPLIT ("A|B|C", "|")`，表达式 `INDEX (SPLIT ("A|B|C", "|"), 4).Value` 将在运行时引发异常。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

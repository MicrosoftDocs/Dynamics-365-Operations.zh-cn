---
title: INDEX ER 函数
description: 本主题提供有关 INDEX 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: a7fe2cbb5421da3c6dd1d044316b276836c5e5c1
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917296"
---
# <a name="INDEX">INDEX ER 函数</a>

[!include [banner](../includes/banner.md)]

`INDEX` 函数返回使用指定列表中的指定数字索引选择的*容器（记录）* 值。 如果索引超出了指定列表中的记录范围，将引发异常。

## <a name="syntax"></a>语法

```
INDEX (list, index)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表*数据类型的数据源的有效路径。

`index`：*整数*

指示所需记录在指定列表中的位置的数字索引。

## <a name="return-values"></a>返回值

*容器（记录）*

生成的记录值。

## <a name="example-1"></a>示例 1

如果输入*计算字段*类型的数据源 **DS**，而该数据源中包含表达式 `SPLIT ("A|B|C", "|")`，则表达式 `DS.Value` 将返回此记录列表的第二条记录的文本值 **"B"**。 表达式 `INDEX (SPLIT ("A|B|C", "|"), 2).Value` 也会返回文本值 **"B"**。

## <a name="example-2"></a>示例 2

如果输入*计算字段*类型的数据源 **DS**，并且它包含表达式 `SPLIT ("A|B|C", "|")`，表达式 `INDEX (SPLIT ("A|B|C", "|"), 4).Value` 将在运行时引发异常。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)

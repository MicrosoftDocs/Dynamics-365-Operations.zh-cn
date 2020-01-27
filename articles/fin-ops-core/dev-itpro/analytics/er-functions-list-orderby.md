---
title: ORDERBY ER 函数
description: 本主题提供有关 ORDERBY 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: a6aed53dcad6d402fc2ca61ae0687016cdb3af5b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916192"
---
# <a name="ORDERBY">ORDERBY ER 函数</a>

[!include [banner](../includes/banner.md)]

在根据指定的参数对指定列表进行排序之后，`ORDERBY` 函数将指定列表返回为*记录列表*值。 可将这些变量定义为表达式。

## <a name="syntax"></a>语法

```
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表*数据类型的数据源的有效路径。

`expression 1`：*字段*

被调用函数的 `list` 参数引用的数据源字段的有效路径。 引用的字段必须是原始数据类型的字段。 此参数是必需的。

`expression N`：*字段*

被调用函数的 `list` 参数引用的数据源字段的有效路径。 引用的字段必须是原始数据类型的字段。 其他参数是可选的。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="example-1"></a>示例 1

如果输入*计算字段*类型的数据源 **DS**，并且它包含表达式 `SPLIT ("C|B|A", "|")`，表达式 `FIRST( ORDERBY( DS, DS. Value)).Value` 将返回文本值 **"A"**。

## <a name="example-2"></a>示例 2

如果**供应商**配置为引用 VendTable 表的电子申报 (ER) 数据源，表达式 `ORDERBY (Vendors, Vendors.'name()')` 将返回按名称升序排序的供应商列表。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)

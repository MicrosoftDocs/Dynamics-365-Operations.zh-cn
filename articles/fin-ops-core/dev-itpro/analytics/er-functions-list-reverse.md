---
title: REVERSE ER 函数
description: 本主题提供有关 REVERSE 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 3343ad788cef29a79f9b110bf29809cd5f0e5c63
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917227"
---
# <a name="REVERSE">REVERSE ER 函数</a>

[!include [banner](../includes/banner.md)]

`REVERSE` 函数以相反的排序顺序将指定列表返回为*记录列表*值。

## <a name="syntax"></a>语法

```
REVERSE (list)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表*数据类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="example-1"></a>示例 1

如果输入*计算字段*类型的数据源 **DS**，并且它包含表达式 `SPLIT ("C|B|A", "|")`，表达式 `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` 将返回文本值 **"C"**。

## <a name="example-2"></a>示例 2

如果**供应商**配置为引用 VendTable 表的电子申报 (ER) 数据源，表达式 `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` 将返回按名称降序排序的供应商列表。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)

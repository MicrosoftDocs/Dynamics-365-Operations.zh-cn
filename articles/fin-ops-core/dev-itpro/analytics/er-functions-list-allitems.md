---
title: ALLITEMS ER 函数
description: 本主题提供有关 ALLITEMS 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 5ddcf989bdfd1d1f5d0a412a2ffefe0e3037ca79
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746715"
---
# <a name="allitems-er-function"></a>ALLITEMS ER 函数

[!include [banner](../includes/banner.md)]

`ALLITEMS` 函数作为内存内选择运行，作为代表与指定路径匹配的所有项目的记录列表返回一个新的平展 *记录列表* 值。

## <a name="syntax"></a>语法

```vb
ALLITEMS (path)
```

## <a name="arguments"></a>参数

`path`：*记录列表*

*记录列表* 数据类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="usage-notes"></a>使用说明

路径必须定义为 *记录列表* 数据类型的数据源元素的有效数据源路径。 路径字符串和日期等数据元素应会在电子申报 (ER) 表达式生成器中设计时引发错误。

我们不建议您对可能包含大量数据的交易记录数据源使用此函数。 而是考虑使用 [ALLTEMSQUERY](er-functions-list-allitemsquery.md) 函数。

## <a name="example-1"></a>示例 1

如果输入 `SPLIT("abcdef" , 2)` 作为数据源 **DS**，表达式 `COUNT( ALLITEMS (DS))` 将返回 **3**。

## <a name="example-2"></a>示例 2

如果输入 **Vend** 作为引用 VendTable 应用程序表的 *记录列表* 数据类型的数据源，表达式 `ALLITEMS (Vend.'<Relations'.ContactPerson)` 将返回具有 **ContactPerson** 表结构并包含可以使用 **ContactPerson.ContactForParty == VendTable.Party** 关系访问的所有联系人，且可用于所引用供应商表中的所有供应商的记录的平展列表。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
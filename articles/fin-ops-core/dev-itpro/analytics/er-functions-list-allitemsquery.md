---
title: ALLITEMSQUERY ER 函数
description: 本主题提供有关 ALLITEMSQUERY 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 56ac956cdfe28d282b8a80d7caec34a50eca5dbe
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559595"
---
# <a name="allitemsquery-er-function"></a>ALLITEMSQUERY ER 函数

[!include [banner](../includes/banner.md)]

`ALLITEMSQUERY` 函数返回一个联接的 SQL 查询。 它返回一个新的平展 *记录列表* 值，此值由代表与指定路径匹配的所有项目的记录的列表组成。

## <a name="syntax"></a>语法

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a>参数

`path`：*记录列表*

*记录列表* 数据类型的数据源的有效路径。 必须包含至少一个关系。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="usage-notes"></a>使用说明

指定的路径必须定义为 *记录列表* 数据类型的数据源元素的有效数据源路径。 同样必须包含至少一个关系。 路径 *字符串* 和 *日期* 等数据元素应会在电子申报 (ER) 表达式生成器中设计时引发错误。

当此函数应用于 *记录列表* 数据类型的数据源，且该数据源引用可以使用 SQL 直接调用的应用程序对象（例如，表、实体或查询）时，它将作为连接的 SQL 查询运行。 否则，它将作为 [ALLITEMS](er-functions-list-allitems.md) 函数在内存内运行。

## <a name="example"></a>示例

在模型映射中定义以下数据源：

- 引用 CustInvoiceTable 表的 *表记录* 类型的 **CustInv** 数据源
- 包含表达式 `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")` 的 *计算字段* 类型的 **FilteredInv** 数据源
- 包含表达式 `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)` 的 *计算字段* 类型的 **JourLines**

运行模型映射以调用 **JourLines** 数据源时，将运行以下 SQL 语句：

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
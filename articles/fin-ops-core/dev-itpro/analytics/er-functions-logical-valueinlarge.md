---
title: VALUEINLARGE ER 函数
description: 本主题提供有关 VALUEINLARGE 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 26a7148a4caa80a191688145bac625bdf0bf83b2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686898"
---
# <a name="valueinlarge-er-function"></a>VALUEINLARGE ER 函数

[!include [banner](../includes/banner.md)]

`VALUEINLARGE` 函数确定指定的 *Int64* 或 *整数* 类型的输入是否匹配指定列表中任何指定项目的值。 如果指定的输入与为指定列表的至少一条记录运行指定表达式的结果匹配，此函数将返回 *布尔* 值 **TRUE**。 否则，返回 *布尔* 值 **FALSE**。 要了解与 `VALUEIN` 函数的区别，请参阅本主题后面的[使用说明](#usage_note)一节。

## <a name="syntax"></a>语法

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a>参数

`input`：*字段*

*记录列表* 类型的数据源项的有效路径。 将匹配此项目的值。

`list`：*记录列表*

*记录列表* 数据类型的数据源的有效路径。

`list item expression`：*表达式*

指向或包含应用于匹配的指定列表的一个字段的有效条件表达式。

## <a name="return-values"></a>返回值

*Boolean*

生成的 *布尔* 值。

## <a name=""></a><a name="usage_note">使用说明</a>

当指定的输入表示其调用可翻译为直接 SQL 语句的数据源项的 *Int64* 或 *整数* 类型（可转换为直接SQL语句的调用）时，指定的列表将转换为临时 SQL 表，匹配将通过执行单个 `EXISTS JOIN` 查询在数据库中执行。 否则，此函数将用作 [`VALUEIN`](er-functions-logical-valuein.md) 函数。

当指定的输入表示设计为 *Int64* 和 *整数* 类型以外的项目的数据源项时，在设计时将发生错误，通知您 `VALUEINLARGE` 函数不适用于配置的 ER 表达式。

当执行 `VALUEINLARGE` 函数表达式并在此执行范围内使用多个临时表时，会发生运行时错误。

## <a name="example"></a>示例

在模型映射中定义以下数据源：

- *表记录* 类型的 **In** 数据源。
    - 此数据源引用 **内部统计** 表。
    - **跨公司** 选项将设置为 **否**。
- *计算字段* 类型的 **InMemory** 数据源。
    - 此数据源包含表达式 `WHERE (In, In.Port <> "")`。
- *计算字段* 类型的 **InFiltered** 数据源。
    - 此数据源包含表达式 `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`。

在公司 **DEMF** 的上下文下调用数据源 **InFiltered** 时，将在应用程序数据库中创建新的临时表，在记录标识代码的内存列表中收集的项将插入此表中，并生成以下 SQL 语句以返回 **内部统计** 表的筛选记录。

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a>其他资源

[逻辑函数](er-functions-category-logical.md)

[VALUEIN 函数](er-functions-logical-valuein.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
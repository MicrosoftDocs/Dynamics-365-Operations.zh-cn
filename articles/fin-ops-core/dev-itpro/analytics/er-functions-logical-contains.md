---
title: CONTAINS ER 函数
description: 本文提供有关 CONTAINS 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: de009dc1bfd790689ef892c103eaffedb8aeb7d3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900213"
---
# <a name="contains-er-function"></a>CONTAINS ER 函数

[!include [banner](../includes/banner.md)]

`CONTAINS` 函数确定指定的输入是否包含指定文本。 如果指定的输入包含指定的文本，此函数将返回一个 **TRUE** *布尔* 值。 否则，返回 *布尔* 值 **FALSE**。

## <a name="syntax"></a>语法

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a>参数

`input`：*字符串*

*字符串* 类型或字符串常量的数据源项的有效路径，其值可能包含第二个参数。

`search text`：*字符串*

*字符串* 数据类型或字符串常量的数据源的有效路径，其值可能包含在第一个参数中。

## <a name="return-values"></a>返回值

*Boolean*

生成的 *布尔* 值。

## <a name="usage-notes"></a>使用说明

仅在 [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) 中配置了相关映射以访问 [Microsoft Dataverse](/power-platform/admin/data-integrator) 时，此函数才可用于指定 [FILTER](er-functions-list-filter.md) 函数的条件表达式。 否则，在设计时会引发异常。 您收到的消息建议您使用 [WHERE](er-functions-list-where.md) 函数而不是 `FILTER` 函数。

## <a name="example-1"></a>示例 1

表达式 `CONTAINS ("abc", "d")` 返回 **FALSE**，而表达式 `CONTAINS ("abc", "C")` 返回 **TRUE**。

## <a name="example-2"></a>示例 2

如果 **模型** 数据源的 **地址** 字段的值包含字符串 **DEU**，则表达式 `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` 返回 **TRUE**。 否则，它将返回 **FALSE**。

## <a name="additional-resources"></a>其他资源

[逻辑函数](er-functions-category-logical.md)

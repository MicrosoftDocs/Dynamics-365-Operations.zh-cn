---
title: ENDSWITH ER 函数
description: 本主题提供有关 ENDSWITH 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
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
ms.openlocfilehash: 1155bb5446f0370d9a5c4b035a767aaeb1d46ee1
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048886"
---
# <a name="endswith-er-function"></a>ENDSWITH ER 函数

[!include [banner](../includes/banner.md)]

`ENDSWITH` 函数确定指定的输入是否以指定文本结尾。 如果指定的输入以指定文本结尾，此函数将返回一个 **TRUE** *布尔* 值。 否则，返回 *布尔* 值 **FALSE**。

## <a name="syntax"></a>语法

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a>参数

`input`：*字符串*

*字符串* 类型或字符串常量的数据源项的有效路径，其值可能以第二个参数为结尾。

`start text`：*字符串*

*字符串* 数据类型或字符串常量的数据源的有效路径，其值可能在第一个参数的末尾。

## <a name="return-values"></a>返回值

*Boolean*

生成的 *布尔* 值。

## <a name="usage-notes"></a>使用说明

仅在 [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) 中配置了相关映射以访问 [Microsoft Dataverse](/power-platform/admin/data-integrator) 时，此函数才可用于指定 [FILTER](er-functions-list-filter.md) 函数的条件表达式。 否则，在设计时会引发异常。 您收到的消息建议您使用 [WHERE](er-functions-list-where.md) 函数而不是 `FILTER` 函数。

## <a name="example-1"></a>示例 1

表达式 `ENDSWITH ("abc", "d")` 返回 **FALSE**，而表达式 `ENDSWITH ("abc", "C")` 返回 **TRUE**。

## <a name="example-2"></a>示例 2

如果 **模型** 数据源的 **地址** 字段的值以字符串 **USA** 结尾，则表达式 `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` 返回 **TRUE**。 否则，它将返回 **FALSE**。

## <a name="additional-resources"></a>其他资源

[逻辑函数](er-functions-category-logical.md)

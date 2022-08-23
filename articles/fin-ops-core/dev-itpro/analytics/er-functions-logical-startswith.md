---
title: STARTSWITH ER 函数
description: 本文提供有关 STARTSWITH 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 010646d2ab96d9a326ffb01c369726790b6377a6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287209"
---
# <a name="startswith-er-function"></a>STARTSWITH ER 函数

[!include [banner](../includes/banner.md)]

`STARTSWITH` 函数确定指定的输入是否以指定文本开头。 如果指定的输入以指定文本开头，此函数将返回一个 **TRUE** *布尔* 值。 否则，返回 *布尔* 值 **FALSE**。

## <a name="syntax"></a>语法

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a>参数

`input`：*字符串*

*字符串* 类型或字符串常量的数据源项的有效路径，其值可能以第二个参数为开头。

`start text`：*字符串*

*字符串* 数据类型或字符串常量的数据源的有效路径，其值可能在第一个参数的开头。

## <a name="return-values"></a>返回值

*Boolean*

生成的 *布尔* 值。

## <a name="usage-notes"></a>使用说明

仅在 [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) 中配置了相关映射以访问 [Microsoft Dataverse](/power-platform/admin/data-integrator) 时，此函数才可用于指定 [FILTER](er-functions-list-filter.md) 函数的条件表达式。 否则，在设计时会引发异常。 您收到的消息建议您使用 [WHERE](er-functions-list-where.md) 函数而不是 `FILTER` 函数。

## <a name="example-1"></a>示例 1

表达式 `STARTSWITH ("abc", "d")` 返回 **FALSE**，而表达式 `STARTSWITH ("abc", "A")` 返回 **TRUE**。

## <a name="example-2"></a>示例 2

如果 **模型** 数据源的 **地址** 字段的值以符串 **123 Coffee Street** 为开头，则表达式 `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` 返回 **TRUE**。 否则，它将返回 **FALSE**。

## <a name="additional-resources"></a>其他资源

[逻辑函数](er-functions-category-logical.md)

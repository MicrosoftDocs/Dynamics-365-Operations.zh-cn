---
title: LIST ER 函数
description: 本文提供有关 LIST 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 758462e577c89379fd9b3d68337048488821eb25
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881179"
---
# <a name="list-er-function"></a>LIST ER 函数

[!include [banner](../includes/banner.md)]

`LIST` 函数返回一个 *记录列表* 值，此值由根据指定参数创建的新记录列表组成。

## <a name="syntax"></a>语法

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a>参数

`record 1`：*容器（记录）*

对 *记录* 数据类型的数据源的引用。 此参数是必需的。

`record N`：*容器（记录）*

对 *记录* 数据类型的数据源的引用。 其他参数是可选的。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="usage-notes"></a>使用说明

创建的列表的结构仅包含在参数中提到的每个记录的结构中显示的字段。

## <a name="example"></a>示例

您输入 *容器* 类型的数据源 **记录 1**。 此数据源包含 *计算字段* 类型的以下嵌套字段：

- **代码：** 此字段包含返回 *字符串* 类型的的值的表达式。
- **金额：** 此字段包含返回 *实数* 类型的的值的表达式。

然后，您输入 *容器* 类型的数据源 **记录 2**。 此数据源包含 *计算字段* 类型的以下嵌套字段：

- **金额：** 此字段包含返回 *实数* 类型的的值的表达式。
- **IsValid：** 此字段包含返回 *布尔值* 类型的的值的表达式。

在此例中，表达式 `LIST('Record 1', 'Record 2')` 返回包含两个记录的新列表。 此列表的结构由一个 *实数* 类型的 **金额** 字段组成，因为此字段是被调用函数每个参数中显示的唯一字段。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
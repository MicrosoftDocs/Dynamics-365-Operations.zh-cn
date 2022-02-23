---
title: LIST ER 函数
description: 本主题提供有关 LIST 电子申报 (ER) 函数如何使用的信息。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7f8e701ec2836206d2299abba5e5b8542b4cf92
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683079"
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

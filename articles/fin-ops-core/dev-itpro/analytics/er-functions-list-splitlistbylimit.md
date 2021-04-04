---
title: SPLITLISTBYLIMIT ER 函数
description: 本主题提供有关 SPLITLISTBYLIMIT 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 119ad3c363913ddaf3d6b890e36989d03e91b3c0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565096"
---
# <a name="splitlistbylimit-er-function"></a>SPLITLISTBYLIMIT ER 函数

[!include [banner](../includes/banner.md)]

`SPLITLISTBYLIMIT` 函数将指定列表拆分为新的子列表（批次）列表。 每个批次中的记录数是动态计算的。 然后此函数作为包含批次的新 *记录列表* 值返回结果。

## <a name="syntax"></a>语法

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表* 数据类型的数据源的有效路径。

`limit value`：*整数* 或 *实数*

用于将原始列表拆分为多个批次的限制的最大值。

`limit source`：*字段*

指定列表中 *整数* 或 *实数* 类型的字段的有效路径。 此字段的值定义在总和中增加的步骤。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="usage-notes"></a>使用说明

返回的批次列表包含以下元素：

- **值**：*列表*

    属于当前批次的记录的列表。

- **BatchNumber**：*整数*

    返回列表中当前批次的编号。

如果限值源超过定义的限值时，限值不适用于原始列表的单个项目。

## <a name="example"></a>示例

下图显示电子申报 (ER) 格式。

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

下图显示用于该格式的数据源。

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

下图显示运行该格式的结果。 在此情况下，输出为商品项目的简单列表。

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

在以下图中，调整了同一个格式，以显示单个批次必须包括总重量不应超过限值 9 的商品的批次中的商品物料的列表。

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

下图显示运行调整后的格式的结果。

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> 此限值不适用于原始列表的最后一个物料，因为其限值源（**重量**）的值 (**11**) 超出定义的限值 (**9**)。 要在生成报表期间忽略子列表，请根据需要使用 `WHERE` 函数或相应格式元素的 **Enabled** 表达式。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
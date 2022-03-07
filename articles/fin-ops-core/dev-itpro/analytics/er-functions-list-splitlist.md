---
title: SPLITLIST ER 函数
description: 本主题提供有关 SPLITLIST 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 03/15/2021
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
ms.openlocfilehash: ef0b548173a01cc5a15fcfb743dfb29397c1349b3c2926fa6401399459d07026
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776114"
---
# <a name="splitlist-er-function"></a>SPLITLIST ER 函数

[!include [banner](../includes/banner.md)]

`SPLITLIST` 函数将指定的列表拆分为多个子列表（或批次），每个批次包含指定的记录数。 然后作为包含批次的新 *记录列表* 值返回结果。

## <a name="syntax-1"></a>语法 1

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a>语法 2

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表* 数据类型的数据源的有效路径。

`number`：*整数*

每个批次的最大记录数。

`on-demand reading flag`：*布尔值*

指定是否应按需生成子列表元素的 *布尔* 值。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="usage-notes"></a>使用说明

返回的批次列表包含以下元素：

 - **值：** *列表*

    属于当前批次的记录的列表。

- **BatchNumber：** *整数*

    返回列表中当前批次的编号。

当按需读取标志设置为 **True** 时，根据请求生成子列表，这允许减少内存消耗，但如果不按顺序使用元素，可能导致性能下降。

## <a name="example"></a>示例

下图中，将创建一个 **行** 数据源以充当具有三条记录的记录列表。 此列表分为多个批次，每个批次中最多包含两条记录。

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

下图显示设计的格式布局。 在此格式布局中，创建了与 **行** 数据源的绑定，以便生成 XML 格式的输出。 此输出为各批次及其中的记录提供单个节点。

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

下图显示运行设计的格式的结果。

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

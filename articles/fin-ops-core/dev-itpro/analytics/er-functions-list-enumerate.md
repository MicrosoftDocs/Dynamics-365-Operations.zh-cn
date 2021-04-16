---
title: ENUMERATE ER 函数
description: 本主题提供有关 ENUMERATE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
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
ms.openlocfilehash: b05448b57d3b08af61144dacdfa2a4e1ba30d009
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746643"
---
# <a name="enumerate-er-function"></a>ENUMERATE ER 函数

[!include [banner](../includes/banner.md)]

`ENUMERATE` 函数返回一个新的 *记录列表* 值，此值由指定列表的枚举记录组成。

## <a name="syntax"></a>语法

```vb
ENUMERATE (list)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表* 数据类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="usage-notes"></a>使用说明

返回的枚举记录列表包含以下其他元素：

- 字段的记录（**值** 组件）
- 当前记录索引（**编号** 组件）

## <a name="example"></a>示例

在下图中中，**枚举** 数据源创建为引用 VendTable 表的 **供应商** 数据源的供应商记录的枚举列表。

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

下图显示电子申报 (ER) 格式。 在此格式布局中，创建了数据绑定，以便生成 XML 格式的输出。 此输出将单个供应商表示为枚举的节点。

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

下图显示运行设计的格式的结果。

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
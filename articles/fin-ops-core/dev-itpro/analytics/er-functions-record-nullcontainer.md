---
title: NULLCONTAINER ER 函数
description: 本文提供有关 NULLCONTAINER 电子报告 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 8da2a30cf2839adabf7b5ea4916f44999aa05758
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850949"
---
# <a name="nullcontainer-er-function"></a>NULLCONTAINER ER 函数

[!include [banner](../includes/banner.md)]

`NULLCONTAINER` 函数返回与指定记录列表或记录具有相同结构的空 *容器（记录）* 值。

## <a name="syntax"></a>语法

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a>参数

`list`：*记录列表* 或 *容器（记录）*

*记录列表* 或 *容器（记录）* 类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*容器（记录）*

生成的记录值。

## <a name="usage-notes"></a>使用说明

> [!NOTE] 
> 此函数已废弃。 请改用 `EMPTYRECORD` 函数。 有关详细信息，请参阅 [EMPTYRECORD](er-functions-record-emptyrecord.md)。

## <a name="example"></a>示例

`NULLCONTAINER (SPLIT ("abc", 1))` 返回具有与 `SPLIT` 函数返回的列表相同结构的新空记录。 有关详细信息，请参阅 [SPLIT](er-functions-list-split.md)。

## <a name="additional-resources"></a>其他资源

[记录函数](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
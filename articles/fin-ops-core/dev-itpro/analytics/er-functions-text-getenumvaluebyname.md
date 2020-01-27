---
title: GETENUMVALUEBYNAME ER 函数
description: 本主题提供有关 GETENUMVALUEBYNAME 电子申报 (ER) 函数如何使用的信息。
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ded0c62b4556b21e731cd9b98db2863ec6ec442
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916836"
---
# <a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER 函数</a>

[!include [banner](../includes/banner.md)]

`GETENUMVALUEBYNAME` 函数通过使用指定为*字符串*值的枚举名称在指定的枚举数据源中搜索特定的*枚举*值。 如果找到*枚举*值，函数将返回此值。 否则，此函数将返回**空**枚举值。

## <a name="syntax"></a>语法

```
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>参数

`enumeration data source path`：*枚举*

下列枚举类型之一的数据源的有效路径：

- 电子申报 (ER) 模型枚举
- ER 格式枚举
- Microsoft Dynamics 365 Finance 枚举

`enumeration value text`：*字符串*

代表单个枚举值的名称的字符串值。

## <a name="return-values"></a>返回值

可空*枚举*

生成的枚举值。

## <a name="usage-notes"></a>使用说明

如果使用指定为*字符串*值的枚举值的名称未找到*枚举*值，不会引发异常。

## <a name="example"></a>示例

在下图中，数据模型中引入了 **ReportDirection** 枚举。 请注意，为枚举值定义标签。

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

下图显示以下详细信息：

- **$Direction** 数据源在 ER 报表中配置。 此数据源是根据 **ReportDirection** 模型枚举配置的。
- `$IsArrivals` 表达式设计为将基于模型枚举的 **$Direction** 数据源用作此函数的参数。
- 此比较表达式的值为 **TRUE**。

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)

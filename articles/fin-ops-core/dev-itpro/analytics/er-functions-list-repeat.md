---
title: REPEAT ER 函数
description: 本文提供有关如何使用 REPEAT 电子报告 (ER) 函数的信息。
author: NickSelin
ms.date: 08/01/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-06-01
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: c56139a3c63b03f907b1dcbf4365990d2a13c35a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220683"
---
# <a name="repeat-er-function"></a>REPEAT ER 函数

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

`REPEAT` 函数可生成一个记录，该记录包含具有与指定输入匹配的值的字段。 然后，它返回重复指定次数的记录的新 *记录列表*。

## <a name="syntax"></a>语法

```vb
REPEAT (item, number)
```

## <a name="arguments"></a>参数

`item`：任何支持的[原始](er-formula-supported-data-types-primitive.md)或[组合](er-formula-supported-data-types-composite.md)数据类型

要重复的值。

`number`：*整数*

重复次数。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="usage-notes"></a>使用说明

返回的重复记录列表公开了以下字段：

- 指定值（`Item` 字段）
- 当前记录索引（`Number` 字段）

> [!NOTE]
> 由于此函数使用从一开始的编号，因此，对于所生成列表的第一条记录，`Number` 字段的值为 **1**。

您可以使用此函数乘以现有数据，以便您可以使用 [Regression suite automation tool (RSAT)](../perf-test/rsat/rsat-overview.md) 对[电子报告 (ER)](general-electronic-reporting.md) 解决方案执行性能和容量测试。

## <a name="example"></a>示例

您希望生成 XML 格式的文档，该文档包含的 `Party` XML 元素必须与运行时在对话框内数据条目字段中指定的元素数一样多，然后才能开始执行 ER 报告格式。

下图显示 ER [格式](er-overview-components.md#format-component)。 在此格式中，将添加单个 `Party`XML 元素以公开单个当事方的属性。

<a href="./media/er-repeat-function-1.png"><img src="./media/er-repeat-function-1.png" alt="Format structure on the Format tab of the Format designer page." class="alignnone size-full" width="929" height="548" /></a>

下图显示了以下配置的数据源：

- 表示单个当事方的 `Party` 数据源。 `Party.Value` 字段用于公开单个文本值。
- `NumberOfRepeats` [数据源](er-user-input-parameter-data-sources.md)，此数据源用于在运行时在对话框中提供数据输入字段，以便您可以指定应在生成的文档中输入的当事方数。
- `Party2` 数据源，此数据源将 `Party` 记录重复 `NumberOfRepeats` 数据源中指定的次数。

<a href="./media/er-repeat-function-2.png"><img src="./media/er-repeat-function-2.png" alt="Configured data sources on the Mapping tab of the Format designer page." class="alignnone size-full" width="1044" height="411" /></a>

下图显示了为生成 XML 格式的输出而创建的可编辑 ER 格式的数据绑定。 此输出将单个相关方表示为枚举的节点。

<a href="./media/er-repeat-function-3.png"><img src="./media/er-repeat-function-3.png" alt="Configured data bindings on the Mapping tab of the Format designer page." class="alignnone size-full" width="1051" height="417" /></a>

下图显示运行设计格式时的结果，`NumberOfRepeats` 数据源的值被指定为 **5**。

<a href="./media/er-repeat-function-4.png"><img src="./media/er-repeat-function-4.png" alt="Result of running the format on a new web browser tab." class="alignnone wp-image-290711 size-full" width="400" height="380" /></a>

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

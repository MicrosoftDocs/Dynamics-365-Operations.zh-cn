---
title: QRCODE ER 函数
description: 本文提供有关 QRCODE 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 12/10/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 9de62eefb82942ccc72e81bd9bf36eed07c99dba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287179"
---
# <a name="qrcode-er-function"></a>QRCODE ER 函数

[!include [banner](../includes/banner.md)]

`QRCODE` 函数返回一个 *容器* 值，该值以二进制格式显示指定字符串的快速响应代码（QR 代码）图像。

## <a name="syntax"></a>语法

```vb
QRCODE (text)
```

## <a name="arguments"></a>参数

`text`：*字符串*

代表原始文本的 *字符串* 值。

## <a name="return-values"></a>返回值

*容器*

生成的二进制流。

## <a name="example"></a>示例

您可以配置电子申报 (ER) 格式以使用预定义的模板使用 Microsoft Office 格式（Excel 工作簿或 Word 文档）生成传出文档。 此模板可能包含 **图片** 对象（Excel 工作簿）或 **图片内容控制**（Word 文档）作为 QR 代码图像的占位符。 您需要将已配置的 ER 格式添加到用于填充此占位符的 **单元格** 元素。 要指定将哪些信息存储在 QR 代码中，您需要为此 **单元格** 元素定义绑定。 例如，您可以将此绑定配置为包含以下表达式：

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

运行配置的 ER 格式时，**model.ListOfShelfLabels** 数据源的 **LabelText** 字段的文本值将用于生成 QR 代码图像。 此图像将替换用于生成出站文档的文档模板中的 QR 代码图像占位符。 扫描生成的文档的此图像时，将返回从 **model.ListOfShelfLabels** 数据源的 **LabelText** 字段获取的文本。 有关详细信息，请参阅[使用 ER 在您生成的文档中嵌入图像和形状](electronic-reporting-embed-images-shapes.md)。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

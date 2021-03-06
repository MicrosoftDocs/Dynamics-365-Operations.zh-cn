---
title: CHAR ER 函数
description: 本主题提供有关 CHAR 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: f83dfe19e442b9e81d63a2b1dd3dd44aa2f594bc
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891175"
---
# <a name="char-er-function"></a>CHAR ER 函数

[!include [banner](../includes/banner.md)]

`CHAR` 函数返一个 *字符串* 值，该值表示指定 Unicode 数值引用的单个字符。

## <a name="syntax"></a>语法

```vb
CHAR (number)
```

## <a name="arguments"></a>参数

`number`：*整数*

与预期的单个字符相对应的数字。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="usage-notes"></a>使用说明

此函数返回的字符串取决于在父 **FILE** 格式元素中选择的编码。 有关支持的编码的列表，请参阅[编码类](/dotnet/api/system.text.encoding)。

## <a name="example"></a>示例

`CHAR (255)` 返回 **"ÿ"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
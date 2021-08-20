---
title: FORMATELEMENTNAME ER 函数
description: 本主题提供有关 FORMATELEMENTNAME 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 72977edfbe06e0d68d9226c9c25fa0633e7951d22438e053ae2a7cf4ef9a5848
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764481"
---
# <a name="formatelementname-er-function"></a>FORMATELEMENTNAME ER 函数

[!include [banner](../includes/banner.md)]

`FORMATELEMENTNAME` 函数返回一个 *字符串* 值，此值代表当前电子申报 (ER) 格式元素的名称。

## <a name="syntax"></a>语法

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="usage-notes"></a>使用说明

可以在为 ER 格式组件（来自位于 **收集输出详细信息** 选项已打开的 **常见\\文件** 组件下的 **文本** 组）的 **已收集的数据键名** 和 **已收集的数据键值** 属性配置的 ER 表达式中调用此函数。

## <a name="example"></a>示例

有关如何使用此函数的详细信息，请参阅 [盘点和合计格式输出的 ER 使用数据](tasks/er-format-counting-summing-1.md)任务指南，这是 **购置/开发 IT 服务/解决方案组件** 业务流程的一部分。

## <a name="additional-resources"></a>其他资源

[数据收集功能](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
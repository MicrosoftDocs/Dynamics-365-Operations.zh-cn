---
title: TEXT ER 函数
description: 本主题提供有关 TEXT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: c26d0c4c8c6290bd2dbb10a288bbd59941a8d98e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915548"
---
# <a name="TEXT">TEXT ER 函数</a>

[!include [banner](../includes/banner.md)]

在将指定的数字转换为根据当前应用程序实例的服务器区域设置设定格式的文本字符串后，`TEXT` 函数将该数字作为*字符串*值返回。

## <a name="syntax"></a>语法

```
TEXT (number)
```

## <a name="arguments"></a>参数

`number`：*整数*或*实数*

必须转换为文本字符串的数字。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="usage-notes"></a>使用说明

对于*实数*类型的值，字符串转换被限制为两位小数。

## <a name="example"></a>示例

如果将 Microsoft Dynamics 365 Finance 实例的服务器区域定义为 **EN-US**，`TEXT (NOW ())` 将返回当前 Finance 会话日期 2015 年 12 月 17 日为文本字符串 **"12/17/2015 07:59:23 AM"**。 `TEXT (1/3)` 将返回 **"0.33"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)

---
title: TABLENAME2ID ER 函数
description: 本主题提供有关 TABLENAME2ID 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 951de1d1505508ebb6abeff5b80ecef10573e117
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041254"
---
# <a name="TABLENAME2ID">TABLENAME2ID ER 函数</a>

[!include [banner](../includes/banner.md)]

`TABLENAME2ID` 函数作为*整数*值返回指定表名称的表 ID 的数字表示。

## <a name="syntax"></a>语法

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a>参数

`text`：*字符串*

代表有效表名的文本值。

## <a name="return-values"></a>返回值

*整数*

生成的数字值。

## <a name="usage-notes"></a>使用说明

在 Microsoft Dynamics 365 Finance 的不同实例中，执行此函数可能产生不同的结果，即使使用相同的公司名称。

## <a name="example"></a>示例

`TABLENAME2ID ("Intrastat")` 将返回 **1510**。

## <a name="additional-resources"></a>其他资源

[其他（业务域特定的）函数](er-functions-category-other.md)

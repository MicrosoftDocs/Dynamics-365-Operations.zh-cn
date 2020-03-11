---
title: SESSIONTODAY ER 函数
description: 本主题提供有关 SESSIONTODAY 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 483ff46a27068bc2d70c80a848f0329861c914b3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042250"
---
# <span data-ttu-id="2163c-103"><a name="SESSIONTODAY">SESSIONTODAY ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="2163c-103"><a name="SESSIONTODAY">SESSIONTODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2163c-104">`SESSIONTODAY` 函数返回一个*日期*值，此值表示当前应用程序会话的日期。</span><span class="sxs-lookup"><span data-stu-id="2163c-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="2163c-105">语法</span><span class="sxs-lookup"><span data-stu-id="2163c-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="2163c-106">返回值</span><span class="sxs-lookup"><span data-stu-id="2163c-106">Return values</span></span>

<span data-ttu-id="2163c-107">*日期*</span><span class="sxs-lookup"><span data-stu-id="2163c-107">*Date*</span></span>

<span data-ttu-id="2163c-108">生成的日期值。</span><span class="sxs-lookup"><span data-stu-id="2163c-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="2163c-109">示例</span><span class="sxs-lookup"><span data-stu-id="2163c-109">Example</span></span>

<span data-ttu-id="2163c-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` 根据所选的德国区域性和指定格式，返回当前应用程序会话的日期/时间值 2015 年 12 月 24 日为字符串 **"24-12-2015"**。</span><span class="sxs-lookup"><span data-stu-id="2163c-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2163c-111">其他资源</span><span class="sxs-lookup"><span data-stu-id="2163c-111">Additional resources</span></span>

[<span data-ttu-id="2163c-112">日期和时间函数</span><span class="sxs-lookup"><span data-stu-id="2163c-112">Date and time functions</span></span>](er-functions-category-datetime.md)

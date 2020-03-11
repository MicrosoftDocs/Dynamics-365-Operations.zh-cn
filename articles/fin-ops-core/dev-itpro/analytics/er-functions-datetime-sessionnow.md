---
title: SESSIONNOW ER 函数
description: 本主题提供有关 SESSIONNOW 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 5489fab61791654c2e583fc11b27aba09fb90c86
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042289"
---
# <span data-ttu-id="9d2fd-103"><a name="">SESSIONNOW ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="9d2fd-103"><a name="">SESSIONNOW ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d2fd-104">`SESSIONNOW` 函数返回一个*日期时间*值，此值表示当前应用程序会话的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="9d2fd-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d2fd-105">语法</span><span class="sxs-lookup"><span data-stu-id="9d2fd-105">Syntax</span></span>

```vb
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="9d2fd-106">返回值</span><span class="sxs-lookup"><span data-stu-id="9d2fd-106">Return values</span></span>

<span data-ttu-id="9d2fd-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="9d2fd-107">*DateTime*</span></span>

<span data-ttu-id="9d2fd-108">生成的日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="9d2fd-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="9d2fd-109">示例</span><span class="sxs-lookup"><span data-stu-id="9d2fd-109">Example</span></span>

<span data-ttu-id="9d2fd-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` 根据所选的德国区域性和指定格式，返回当前应用程序会话的日期/时间值 2015 年 12 月 24 日为 **"24.12.2015"**。</span><span class="sxs-lookup"><span data-stu-id="9d2fd-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9d2fd-111">其他资源</span><span class="sxs-lookup"><span data-stu-id="9d2fd-111">Additional resources</span></span>

[<span data-ttu-id="9d2fd-112">日期和时间函数</span><span class="sxs-lookup"><span data-stu-id="9d2fd-112">Date and time functions</span></span>](er-functions-category-datetime.md)

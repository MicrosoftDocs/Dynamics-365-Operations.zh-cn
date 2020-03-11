---
title: NULLDATETIME ER 函数
description: 本主题提供有关 NULLDATETIME 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 3cd4c152d4e220a2f6315265ed5e44d148134279
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042243"
---
# <span data-ttu-id="9cfcd-103"><a name="NULLDATETIME">NULLDATETIME ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="9cfcd-103"><a name="NULLDATETIME">NULLDATETIME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9cfcd-104">`NULLDATETIME` 函数返回一个*日期时间*值，此值表示协调世界时（格林威治标准时间 \[GMT\]）的**空**日期/时间值（1900 年 1 月 1 日）。</span><span class="sxs-lookup"><span data-stu-id="9cfcd-104">The `NULLDATETIME` function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="9cfcd-105">语法</span><span class="sxs-lookup"><span data-stu-id="9cfcd-105">Syntax</span></span>

```vb
NULLDATETIME ()
```

## <a name="return-values"></a><span data-ttu-id="9cfcd-106">返回值</span><span class="sxs-lookup"><span data-stu-id="9cfcd-106">Return values</span></span>

<span data-ttu-id="9cfcd-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="9cfcd-107">*DateTime*</span></span>

<span data-ttu-id="9cfcd-108">生成的日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="9cfcd-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="9cfcd-109">示例</span><span class="sxs-lookup"><span data-stu-id="9cfcd-109">Example</span></span>

<span data-ttu-id="9cfcd-110">当由在**语言和国家/地区首选项**部分具有时区值 **(GMT) 协调世界时**的应用程序用户启动的流程中调用时，`DATETIMEFORMAT( NULLDATETIME(), "O")` 返回字符串值 **1900-01-01T00:00:00.0000000+00:00**。</span><span class="sxs-lookup"><span data-stu-id="9cfcd-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` returns the string value **1900-01-01T00:00:00.0000000+00:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT) Coordinated Universal Time** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9cfcd-111">其他资源</span><span class="sxs-lookup"><span data-stu-id="9cfcd-111">Additional resources</span></span>

[<span data-ttu-id="9cfcd-112">日期和时间函数</span><span class="sxs-lookup"><span data-stu-id="9cfcd-112">Date and time functions</span></span>](er-functions-category-datetime.md)

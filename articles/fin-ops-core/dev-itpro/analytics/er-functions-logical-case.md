---
title: CASE ER 函数
description: 本主题提供有关 CASE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 69b76a06bcd3ba002d9543447e60afa14d5a6ce6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687018"
---
# <a name="case-er-function"></a><span data-ttu-id="6321f-103">CASE ER 函数</span><span class="sxs-lookup"><span data-stu-id="6321f-103">CASE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6321f-104">`CASE` 函数根据指定的替代选项评估指定表达式的值，并返回等于指定表达式值的第一个选项的结果。</span><span class="sxs-lookup"><span data-stu-id="6321f-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="6321f-105">否则，如果将默认结果指定为被调用函数最后一个参数（前面没有选项），则返回可选默认结果。</span><span class="sxs-lookup"><span data-stu-id="6321f-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="6321f-106">返回的值可以是任何受支持的数据类型的值。</span><span class="sxs-lookup"><span data-stu-id="6321f-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="6321f-107">语法</span><span class="sxs-lookup"><span data-stu-id="6321f-107">Syntax</span></span>

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="6321f-108">参数</span><span class="sxs-lookup"><span data-stu-id="6321f-108">Arguments</span></span>

<span data-ttu-id="6321f-109">`expression`：*原始数据类型*（布尔值、数字或文本）</span><span class="sxs-lookup"><span data-stu-id="6321f-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="6321f-110">返回原始数据类型的值的有效表达式。</span><span class="sxs-lookup"><span data-stu-id="6321f-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="6321f-111">`option 1`：*原始数据类型*（布尔值、数字或文本）</span><span class="sxs-lookup"><span data-stu-id="6321f-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="6321f-112">一个有效表达式，返回与被调用函数的 `expression` 参数相同的原始数据类型的值。</span><span class="sxs-lookup"><span data-stu-id="6321f-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="6321f-113">此参数是必需的。</span><span class="sxs-lookup"><span data-stu-id="6321f-113">This argument is required.</span></span>

<span data-ttu-id="6321f-114">`result 1`：*任何受支持的数据类型*</span><span class="sxs-lookup"><span data-stu-id="6321f-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="6321f-115">返回的结果与前面的选项相对应。</span><span class="sxs-lookup"><span data-stu-id="6321f-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="6321f-116">此参数是必需的。</span><span class="sxs-lookup"><span data-stu-id="6321f-116">This argument is required.</span></span>

<span data-ttu-id="6321f-117">`option N`：*原始数据类型*（布尔值、数字或文本）</span><span class="sxs-lookup"><span data-stu-id="6321f-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="6321f-118">一个有效表达式，返回与被调用函数的 `expression` 参数相同的原始数据类型的值。</span><span class="sxs-lookup"><span data-stu-id="6321f-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="6321f-119">此参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="6321f-119">This argument is optional.</span></span>

<span data-ttu-id="6321f-120">`result N`：*任何受支持的数据类型*</span><span class="sxs-lookup"><span data-stu-id="6321f-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="6321f-121">返回的结果与前面的选项相对应。</span><span class="sxs-lookup"><span data-stu-id="6321f-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="6321f-122">此参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="6321f-122">This argument is optional.</span></span>

<span data-ttu-id="6321f-123">`default result`：*任何受支持的数据类型*</span><span class="sxs-lookup"><span data-stu-id="6321f-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="6321f-124">如果没有匹配项，应返回的结果。</span><span class="sxs-lookup"><span data-stu-id="6321f-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="6321f-125">此参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="6321f-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="6321f-126">返回值</span><span class="sxs-lookup"><span data-stu-id="6321f-126">Return values</span></span>

<span data-ttu-id="6321f-127">*任何受支持的数据类型*</span><span class="sxs-lookup"><span data-stu-id="6321f-127">*Any of the supported data types*</span></span>

<span data-ttu-id="6321f-128">生成的任何受支持数据类型的值。</span><span class="sxs-lookup"><span data-stu-id="6321f-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6321f-129">使用说明</span><span class="sxs-lookup"><span data-stu-id="6321f-129">Usage notes</span></span>

<span data-ttu-id="6321f-130">如果没有匹配项，并且未定义可选的默认结果，将在运行时引发异常。</span><span class="sxs-lookup"><span data-stu-id="6321f-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="6321f-131">必须使用相同的数据类型指定所有结果。</span><span class="sxs-lookup"><span data-stu-id="6321f-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="6321f-132">如果配置结果的数据类型不匹配，则会在设计时引发异常。</span><span class="sxs-lookup"><span data-stu-id="6321f-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="6321f-133">如果第一个结果值与第 *N* 个结果值是 *容器（记录）* 或 *记录列表* 数据类型的值，结果只包含两个值中都存在的字段。</span><span class="sxs-lookup"><span data-stu-id="6321f-133">If the first result value and the *N* th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="6321f-134">示例</span><span class="sxs-lookup"><span data-stu-id="6321f-134">Example</span></span>

<span data-ttu-id="6321f-135">如果当前应用程序会话日期在 10 月到 12 月之间，`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` 将返回字符串 **"WINTER"**。</span><span class="sxs-lookup"><span data-stu-id="6321f-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="6321f-136">否则，它返回一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="6321f-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6321f-137">其他资源</span><span class="sxs-lookup"><span data-stu-id="6321f-137">Additional resources</span></span>

[<span data-ttu-id="6321f-138">逻辑函数</span><span class="sxs-lookup"><span data-stu-id="6321f-138">Logical functions</span></span>](er-functions-category-logical.md)

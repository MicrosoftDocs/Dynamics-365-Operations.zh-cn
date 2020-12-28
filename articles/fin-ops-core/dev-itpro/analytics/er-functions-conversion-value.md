---
title: VALUE ER 函数
description: 本主题提供有关 VALUE 电子申报 (ER) 函数如何使用的信息。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56b32a802674725347ab496d3a09b99c8f04446d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681200"
---
# <a name="value-er-function"></a><span data-ttu-id="d421e-103">VALUE ER 函数</span><span class="sxs-lookup"><span data-stu-id="d421e-103">VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d421e-104">`VALUE` 函数返回一个 *实数* 值，该值从指定的字符串转换而来。</span><span class="sxs-lookup"><span data-stu-id="d421e-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="d421e-105">语法</span><span class="sxs-lookup"><span data-stu-id="d421e-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="d421e-106">参数</span><span class="sxs-lookup"><span data-stu-id="d421e-106">Arguments</span></span>

<span data-ttu-id="d421e-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="d421e-107">`text`: *String*</span></span>

<span data-ttu-id="d421e-108">必须转换为数字值的字符串值。</span><span class="sxs-lookup"><span data-stu-id="d421e-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="d421e-109">返回值</span><span class="sxs-lookup"><span data-stu-id="d421e-109">Return values</span></span>

<span data-ttu-id="d421e-110">*实数*</span><span class="sxs-lookup"><span data-stu-id="d421e-110">*Real*</span></span>

<span data-ttu-id="d421e-111">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="d421e-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d421e-112">使用说明</span><span class="sxs-lookup"><span data-stu-id="d421e-112">Usage notes</span></span>

<span data-ttu-id="d421e-113">逗号和点字符 (.) 被视为小数分隔符，前导连字符 (-) 用作负号。</span><span class="sxs-lookup"><span data-stu-id="d421e-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="d421e-114">如果指定字符串中包含其他非数值字符，将在运行时引发异常。</span><span class="sxs-lookup"><span data-stu-id="d421e-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="d421e-115">示例 1</span><span class="sxs-lookup"><span data-stu-id="d421e-115">Example 1</span></span>

<span data-ttu-id="d421e-116">`VALUE ("1 234,56")` 引发异常。</span><span class="sxs-lookup"><span data-stu-id="d421e-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="d421e-117">示例 2</span><span class="sxs-lookup"><span data-stu-id="d421e-117">Example 2</span></span>

<span data-ttu-id="d421e-118">`VALUE ("1234,56")` 将返回 **1234.56**。</span><span class="sxs-lookup"><span data-stu-id="d421e-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d421e-119">其他资源</span><span class="sxs-lookup"><span data-stu-id="d421e-119">Additional resources</span></span>

[<span data-ttu-id="d421e-120">类型转换函数</span><span class="sxs-lookup"><span data-stu-id="d421e-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)

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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c90772ca1e93500ac45cc52ba92d4169c4d29bad
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042611"
---
# <span data-ttu-id="19bc8-103"><a name="VALUE">VALUE ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="19bc8-103"><a name="VALUE">VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19bc8-104">`VALUE` 函数返回一个*实数*值，该值从指定的字符串转换而来。</span><span class="sxs-lookup"><span data-stu-id="19bc8-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="19bc8-105">语法</span><span class="sxs-lookup"><span data-stu-id="19bc8-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="19bc8-106">参数</span><span class="sxs-lookup"><span data-stu-id="19bc8-106">Arguments</span></span>

<span data-ttu-id="19bc8-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="19bc8-107">`text`: *String*</span></span>

<span data-ttu-id="19bc8-108">必须转换为数字值的字符串值。</span><span class="sxs-lookup"><span data-stu-id="19bc8-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="19bc8-109">返回值</span><span class="sxs-lookup"><span data-stu-id="19bc8-109">Return values</span></span>

<span data-ttu-id="19bc8-110">*实数*</span><span class="sxs-lookup"><span data-stu-id="19bc8-110">*Real*</span></span>

<span data-ttu-id="19bc8-111">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="19bc8-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="19bc8-112">使用说明</span><span class="sxs-lookup"><span data-stu-id="19bc8-112">Usage notes</span></span>

<span data-ttu-id="19bc8-113">逗号和点字符 (.) 被视为小数分隔符，前导连字符 (-) 用作负号。</span><span class="sxs-lookup"><span data-stu-id="19bc8-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="19bc8-114">如果指定字符串中包含其他非数值字符，将在运行时引发异常。</span><span class="sxs-lookup"><span data-stu-id="19bc8-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="19bc8-115">示例 1</span><span class="sxs-lookup"><span data-stu-id="19bc8-115">Example 1</span></span>

<span data-ttu-id="19bc8-116">`VALUE ("1 234,56")` 引发异常。</span><span class="sxs-lookup"><span data-stu-id="19bc8-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="19bc8-117">示例 2</span><span class="sxs-lookup"><span data-stu-id="19bc8-117">Example 2</span></span>

<span data-ttu-id="19bc8-118">`VALUE ("1234,56")` 将返回 **1234.56**。</span><span class="sxs-lookup"><span data-stu-id="19bc8-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19bc8-119">其他资源</span><span class="sxs-lookup"><span data-stu-id="19bc8-119">Additional resources</span></span>

[<span data-ttu-id="19bc8-120">类型转换函数</span><span class="sxs-lookup"><span data-stu-id="19bc8-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)

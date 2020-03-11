---
title: INT64VALUE ER 函数
description: 本主题提供有关 INT64VALUE 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 7fcb8a617507801d82d16175e9e86c9193091a12
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042680"
---
# <span data-ttu-id="b53a0-103"><a name="INT64VALUE">INT64VALUE ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="b53a0-103"><a name="INT64VALUE">INT64VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b53a0-104">`INT64VALUE` 函数返回一个 *Int64* 值，该值表示指定的字符串。</span><span class="sxs-lookup"><span data-stu-id="b53a0-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b53a0-105">语法 1</span><span class="sxs-lookup"><span data-stu-id="b53a0-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="b53a0-106">语法 2</span><span class="sxs-lookup"><span data-stu-id="b53a0-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="b53a0-107">参数</span><span class="sxs-lookup"><span data-stu-id="b53a0-107">Arguments</span></span>

<span data-ttu-id="b53a0-108">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="b53a0-108">`text`: *String*</span></span>

<span data-ttu-id="b53a0-109">必须转换为 *Int64* 数字的文本值。</span><span class="sxs-lookup"><span data-stu-id="b53a0-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="b53a0-110">`number`：*实数*或*整数*</span><span class="sxs-lookup"><span data-stu-id="b53a0-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="b53a0-111">必须转换为 *Int64* 数字的*实数*或*整数*数字值。</span><span class="sxs-lookup"><span data-stu-id="b53a0-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="b53a0-112">返回值</span><span class="sxs-lookup"><span data-stu-id="b53a0-112">Return values</span></span>

<span data-ttu-id="b53a0-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="b53a0-113">*Int64*</span></span>

<span data-ttu-id="b53a0-114">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="b53a0-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b53a0-115">使用说明</span><span class="sxs-lookup"><span data-stu-id="b53a0-115">Usage notes</span></span>

<span data-ttu-id="b53a0-116">将截断所有小数部分。</span><span class="sxs-lookup"><span data-stu-id="b53a0-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="b53a0-117">示例 1</span><span class="sxs-lookup"><span data-stu-id="b53a0-117">Example 1</span></span>

<span data-ttu-id="b53a0-118">`INT64VALUE ("22565422744")` 返回 *Int64* 值 **22565422744**。</span><span class="sxs-lookup"><span data-stu-id="b53a0-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b53a0-119">示例 2</span><span class="sxs-lookup"><span data-stu-id="b53a0-119">Example 2</span></span>

<span data-ttu-id="b53a0-120">`INT64VALUE ( VALUE("22565422744.77"))` 返回 *Int64* 值 **22565422744**。</span><span class="sxs-lookup"><span data-stu-id="b53a0-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b53a0-121">其他资源</span><span class="sxs-lookup"><span data-stu-id="b53a0-121">Additional resources</span></span>

[<span data-ttu-id="b53a0-122">类型转换函数</span><span class="sxs-lookup"><span data-stu-id="b53a0-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)

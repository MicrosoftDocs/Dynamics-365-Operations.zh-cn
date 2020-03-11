---
title: POWER ER 函数
description: 本主题提供有关 POWER 电子申报 (ER) 函数如何使用的信息。
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c57222d7fcc133faa679bab43431272c984c9d8b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041622"
---
# <span data-ttu-id="88167-103"><a name="POWER">POWER ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="88167-103"><a name="POWER">POWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88167-104">`POWER` 函数返回一个*实数*值，其代表将指定正数提高到指定幂的结果的值。</span><span class="sxs-lookup"><span data-stu-id="88167-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="88167-105">语法</span><span class="sxs-lookup"><span data-stu-id="88167-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="88167-106">参数</span><span class="sxs-lookup"><span data-stu-id="88167-106">Arguments</span></span>

<span data-ttu-id="88167-107">`number`：*实数*或*整数*</span><span class="sxs-lookup"><span data-stu-id="88167-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="88167-108">必须提高到指定幂的数值。</span><span class="sxs-lookup"><span data-stu-id="88167-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="88167-109">`power`：*实数*或*整数*</span><span class="sxs-lookup"><span data-stu-id="88167-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="88167-110">代表特定幂的数值。</span><span class="sxs-lookup"><span data-stu-id="88167-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="88167-111">返回值</span><span class="sxs-lookup"><span data-stu-id="88167-111">Return values</span></span>

<span data-ttu-id="88167-112">*实数*</span><span class="sxs-lookup"><span data-stu-id="88167-112">*Real*</span></span>

<span data-ttu-id="88167-113">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="88167-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="88167-114">示例 1</span><span class="sxs-lookup"><span data-stu-id="88167-114">Example 1</span></span>

<span data-ttu-id="88167-115">`POWER (10, 2)` 将返回 **100**。</span><span class="sxs-lookup"><span data-stu-id="88167-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="88167-116">示例 2</span><span class="sxs-lookup"><span data-stu-id="88167-116">Example 2</span></span>

<span data-ttu-id="88167-117">`POWER (4, 0.5)` 将返回 **2**。</span><span class="sxs-lookup"><span data-stu-id="88167-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="88167-118">其他资源</span><span class="sxs-lookup"><span data-stu-id="88167-118">Additional resources</span></span>

[<span data-ttu-id="88167-119">数学函数</span><span class="sxs-lookup"><span data-stu-id="88167-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)

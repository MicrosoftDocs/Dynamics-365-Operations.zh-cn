---
title: POWER ER 函数
description: 本主题提供有关 POWER 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9c45e7f9b47a3f0ff4445b1dd160def0ada3a56e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570414"
---
# <a name="power-er-function"></a><span data-ttu-id="80fc0-103">POWER ER 函数</span><span class="sxs-lookup"><span data-stu-id="80fc0-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80fc0-104">`POWER` 函数返回一个 *实数* 值，其代表将指定正数提高到指定幂的结果的值。</span><span class="sxs-lookup"><span data-stu-id="80fc0-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="80fc0-105">语法</span><span class="sxs-lookup"><span data-stu-id="80fc0-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="80fc0-106">参数</span><span class="sxs-lookup"><span data-stu-id="80fc0-106">Arguments</span></span>

<span data-ttu-id="80fc0-107">`number`：*实数* 或 *整数*</span><span class="sxs-lookup"><span data-stu-id="80fc0-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="80fc0-108">必须提高到指定幂的数值。</span><span class="sxs-lookup"><span data-stu-id="80fc0-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="80fc0-109">`power`：*实数* 或 *整数*</span><span class="sxs-lookup"><span data-stu-id="80fc0-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="80fc0-110">代表特定幂的数值。</span><span class="sxs-lookup"><span data-stu-id="80fc0-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="80fc0-111">返回值</span><span class="sxs-lookup"><span data-stu-id="80fc0-111">Return values</span></span>

<span data-ttu-id="80fc0-112">*实数*</span><span class="sxs-lookup"><span data-stu-id="80fc0-112">*Real*</span></span>

<span data-ttu-id="80fc0-113">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="80fc0-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="80fc0-114">示例 1</span><span class="sxs-lookup"><span data-stu-id="80fc0-114">Example 1</span></span>

<span data-ttu-id="80fc0-115">`POWER (10, 2)` 将返回 **100**。</span><span class="sxs-lookup"><span data-stu-id="80fc0-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="80fc0-116">示例 2</span><span class="sxs-lookup"><span data-stu-id="80fc0-116">Example 2</span></span>

<span data-ttu-id="80fc0-117">`POWER (4, 0.5)` 将返回 **2**。</span><span class="sxs-lookup"><span data-stu-id="80fc0-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="80fc0-118">其他资源</span><span class="sxs-lookup"><span data-stu-id="80fc0-118">Additional resources</span></span>

[<span data-ttu-id="80fc0-119">数学函数</span><span class="sxs-lookup"><span data-stu-id="80fc0-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
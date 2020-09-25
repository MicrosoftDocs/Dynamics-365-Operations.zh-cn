---
title: NOT ER 函数
description: 本主题提供有关 NOT 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: af588c3714069040fa339d3121e6eb404b9be979
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744639"
---
# <a name="not-er-function"></a><span data-ttu-id="98b47-103">NOT ER 函数</span><span class="sxs-lookup"><span data-stu-id="98b47-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98b47-104">`NOT` 函数作为*布尔*值返回指定条件的冲销逻辑值。</span><span class="sxs-lookup"><span data-stu-id="98b47-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="98b47-105">语法</span><span class="sxs-lookup"><span data-stu-id="98b47-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="98b47-106">参数</span><span class="sxs-lookup"><span data-stu-id="98b47-106">Arguments</span></span>

<span data-ttu-id="98b47-107">`condition`：*布尔值*</span><span class="sxs-lookup"><span data-stu-id="98b47-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="98b47-108">必须冲销的有效条件表达式。</span><span class="sxs-lookup"><span data-stu-id="98b47-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="98b47-109">返回值</span><span class="sxs-lookup"><span data-stu-id="98b47-109">Return values</span></span>

<span data-ttu-id="98b47-110">*布尔值*</span><span class="sxs-lookup"><span data-stu-id="98b47-110">*Boolean*</span></span>

<span data-ttu-id="98b47-111">生成的*布尔*值。</span><span class="sxs-lookup"><span data-stu-id="98b47-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="98b47-112">示例</span><span class="sxs-lookup"><span data-stu-id="98b47-112">Example</span></span>

<span data-ttu-id="98b47-113">`NOT (TRUE)` 返回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="98b47-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98b47-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="98b47-114">Additional resources</span></span>

[<span data-ttu-id="98b47-115">逻辑函数</span><span class="sxs-lookup"><span data-stu-id="98b47-115">Logical functions</span></span>](er-functions-category-logical.md)

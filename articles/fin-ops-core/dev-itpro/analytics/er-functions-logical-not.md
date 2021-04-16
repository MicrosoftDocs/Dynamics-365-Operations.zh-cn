---
title: NOT ER 函数
description: 本主题提供有关 NOT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
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
ms.openlocfilehash: 7c10ed61b97dcd4d4a66a530bb3d08c539659233
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751697"
---
# <a name="not-er-function"></a><span data-ttu-id="f8e30-103">NOT ER 函数</span><span class="sxs-lookup"><span data-stu-id="f8e30-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8e30-104">`NOT` 函数作为 *布尔* 值返回指定条件的冲销逻辑值。</span><span class="sxs-lookup"><span data-stu-id="f8e30-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8e30-105">语法</span><span class="sxs-lookup"><span data-stu-id="f8e30-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="f8e30-106">参数</span><span class="sxs-lookup"><span data-stu-id="f8e30-106">Arguments</span></span>

<span data-ttu-id="f8e30-107">`condition`：*布尔值*</span><span class="sxs-lookup"><span data-stu-id="f8e30-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="f8e30-108">必须冲销的有效条件表达式。</span><span class="sxs-lookup"><span data-stu-id="f8e30-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="f8e30-109">返回值</span><span class="sxs-lookup"><span data-stu-id="f8e30-109">Return values</span></span>

<span data-ttu-id="f8e30-110">*布尔值*</span><span class="sxs-lookup"><span data-stu-id="f8e30-110">*Boolean*</span></span>

<span data-ttu-id="f8e30-111">生成的 *布尔* 值。</span><span class="sxs-lookup"><span data-stu-id="f8e30-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="f8e30-112">示例</span><span class="sxs-lookup"><span data-stu-id="f8e30-112">Example</span></span>

<span data-ttu-id="f8e30-113">`NOT (TRUE)` 返回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="f8e30-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8e30-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="f8e30-114">Additional resources</span></span>

[<span data-ttu-id="f8e30-115">逻辑函数</span><span class="sxs-lookup"><span data-stu-id="f8e30-115">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
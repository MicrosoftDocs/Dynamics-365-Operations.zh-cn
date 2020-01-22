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
ms.openlocfilehash: b15277dba26dc7864193b11a127944daca6b989f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916031"
---
# <span data-ttu-id="04d90-103"><a name="NOT">NOT ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="04d90-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04d90-104">`NOT` 函数作为*布尔*值返回指定条件的冲销逻辑值。</span><span class="sxs-lookup"><span data-stu-id="04d90-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="04d90-105">语法</span><span class="sxs-lookup"><span data-stu-id="04d90-105">Syntax</span></span>

```
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="04d90-106">参数</span><span class="sxs-lookup"><span data-stu-id="04d90-106">Arguments</span></span>

<span data-ttu-id="04d90-107">`condition`：*布尔值*</span><span class="sxs-lookup"><span data-stu-id="04d90-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="04d90-108">必须冲销的有效条件表达式。</span><span class="sxs-lookup"><span data-stu-id="04d90-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="04d90-109">返回值</span><span class="sxs-lookup"><span data-stu-id="04d90-109">Return values</span></span>

<span data-ttu-id="04d90-110">*布尔值*</span><span class="sxs-lookup"><span data-stu-id="04d90-110">*Boolean*</span></span>

<span data-ttu-id="04d90-111">生成的*布尔*值。</span><span class="sxs-lookup"><span data-stu-id="04d90-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="04d90-112">示例</span><span class="sxs-lookup"><span data-stu-id="04d90-112">Example</span></span>

<span data-ttu-id="04d90-113">`NOT (TRUE)` 返回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="04d90-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="04d90-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="04d90-114">Additional resources</span></span>

[<span data-ttu-id="04d90-115">逻辑函数</span><span class="sxs-lookup"><span data-stu-id="04d90-115">Logical functions</span></span>](er-functions-category-logical.md)

---
title: COUNT ER 函数
description: 本主题提供有关 COUNT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 2d29b82a8c3b108f7651e6d593cb17e7ec8ca872
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916238"
---
# <span data-ttu-id="edba0-103"><a name="COUNT">COUNT ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="edba0-103"><a name="COUNT">COUNT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="edba0-104">`COUNT` 函数返回一个表示指定列表中的记录数的*整数*值（如果列表不为空）。</span><span class="sxs-lookup"><span data-stu-id="edba0-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="edba0-105">如果列表为空，此函数返回 **0**（零）。</span><span class="sxs-lookup"><span data-stu-id="edba0-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="edba0-106">语法</span><span class="sxs-lookup"><span data-stu-id="edba0-106">Syntax</span></span>

```
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="edba0-107">参数</span><span class="sxs-lookup"><span data-stu-id="edba0-107">Arguments</span></span>

<span data-ttu-id="edba0-108">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="edba0-108">`list`: *Record list*</span></span>

<span data-ttu-id="edba0-109">*记录列表*数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="edba0-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="edba0-110">返回值</span><span class="sxs-lookup"><span data-stu-id="edba0-110">Return values</span></span>

<span data-ttu-id="edba0-111">*整数*</span><span class="sxs-lookup"><span data-stu-id="edba0-111">*Integer*</span></span>

<span data-ttu-id="edba0-112">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="edba0-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="edba0-113">示例</span><span class="sxs-lookup"><span data-stu-id="edba0-113">Example</span></span>

<span data-ttu-id="edba0-114">`COUNT (SPLIT("abcd" , 3))` 返回 **2**，因为本示例中使用的 `SPLIT` 函数创建一个包含两个记录的列表。</span><span class="sxs-lookup"><span data-stu-id="edba0-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="edba0-115">其他资源</span><span class="sxs-lookup"><span data-stu-id="edba0-115">Additional resources</span></span>

[<span data-ttu-id="edba0-116">列表函数</span><span class="sxs-lookup"><span data-stu-id="edba0-116">List functions</span></span>](er-functions-category-list.md)

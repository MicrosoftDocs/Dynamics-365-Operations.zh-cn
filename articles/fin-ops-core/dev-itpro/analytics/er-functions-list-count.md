---
title: COUNT ER 函数
description: 本主题提供有关 COUNT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: a0b780051684ef52d06a9baf78d9b513d9ac1f0e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746619"
---
# <a name="count-er-function"></a><span data-ttu-id="366ac-103">COUNT ER 函数</span><span class="sxs-lookup"><span data-stu-id="366ac-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="366ac-104">`COUNT` 函数返回一个表示指定列表中的记录数的 *整数* 值（如果列表不为空）。</span><span class="sxs-lookup"><span data-stu-id="366ac-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="366ac-105">如果列表为空，此函数返回 **0**（零）。</span><span class="sxs-lookup"><span data-stu-id="366ac-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="366ac-106">语法</span><span class="sxs-lookup"><span data-stu-id="366ac-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="366ac-107">参数</span><span class="sxs-lookup"><span data-stu-id="366ac-107">Arguments</span></span>

<span data-ttu-id="366ac-108">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="366ac-108">`list`: *Record list*</span></span>

<span data-ttu-id="366ac-109">*记录列表* 数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="366ac-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="366ac-110">返回值</span><span class="sxs-lookup"><span data-stu-id="366ac-110">Return values</span></span>

<span data-ttu-id="366ac-111">*整数*</span><span class="sxs-lookup"><span data-stu-id="366ac-111">*Integer*</span></span>

<span data-ttu-id="366ac-112">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="366ac-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="366ac-113">示例</span><span class="sxs-lookup"><span data-stu-id="366ac-113">Example</span></span>

<span data-ttu-id="366ac-114">`COUNT (SPLIT("abcd" , 3))` 返回 **2**，因为本示例中使用的 `SPLIT` 函数创建一个包含两个记录的列表。</span><span class="sxs-lookup"><span data-stu-id="366ac-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="366ac-115">其他资源</span><span class="sxs-lookup"><span data-stu-id="366ac-115">Additional resources</span></span>

[<span data-ttu-id="366ac-116">列表函数</span><span class="sxs-lookup"><span data-stu-id="366ac-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
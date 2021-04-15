---
title: EMPTYLIST ER 函数
description: 本主题提供有关 EMPTYLIST 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 1e2a92d9951c3ad27503cf82f1b45026f16c3835
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746667"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="64723-103">EMPTYLIST ER 函数</span><span class="sxs-lookup"><span data-stu-id="64723-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64723-104">`EMPTYLIST` 函数通过使用指定的列表作为列表结构的来源返回空 *记录列表* 值。</span><span class="sxs-lookup"><span data-stu-id="64723-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="64723-105">语法</span><span class="sxs-lookup"><span data-stu-id="64723-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="64723-106">参数</span><span class="sxs-lookup"><span data-stu-id="64723-106">Arguments</span></span>

<span data-ttu-id="64723-107">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="64723-107">`list`: *Record list*</span></span>

<span data-ttu-id="64723-108">*记录列表* 数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="64723-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="64723-109">返回值</span><span class="sxs-lookup"><span data-stu-id="64723-109">Return values</span></span>

<span data-ttu-id="64723-110">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="64723-110">*Record list*</span></span>

<span data-ttu-id="64723-111">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="64723-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="64723-112">示例</span><span class="sxs-lookup"><span data-stu-id="64723-112">Example</span></span>

<span data-ttu-id="64723-113">`EMPTYLIST (SPLIT ("abc", 1))` 返回具有与使用的 `SPLIT` 函数返回的列表相同结构的新空列表。</span><span class="sxs-lookup"><span data-stu-id="64723-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64723-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="64723-114">Additional resources</span></span>

[<span data-ttu-id="64723-115">列表函数</span><span class="sxs-lookup"><span data-stu-id="64723-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
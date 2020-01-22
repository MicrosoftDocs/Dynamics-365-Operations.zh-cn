---
title: EMPTYLIST ER 函数
description: 本主题提供有关 EMPTYLIST 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: a60bc948ff6223b6e3acccd0ba40bf64f238aac2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917388"
---
# <span data-ttu-id="bde6d-103"><a name="EMPTYLIST">EMPTYLIST ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="bde6d-103"><a name="EMPTYLIST">EMPTYLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bde6d-104">`EMPTYLIST` 函数通过使用指定的列表作为列表结构的来源返回空*记录列表*值。</span><span class="sxs-lookup"><span data-stu-id="bde6d-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="bde6d-105">语法</span><span class="sxs-lookup"><span data-stu-id="bde6d-105">Syntax</span></span>

```
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="bde6d-106">参数</span><span class="sxs-lookup"><span data-stu-id="bde6d-106">Arguments</span></span>

<span data-ttu-id="bde6d-107">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="bde6d-107">`list`: *Record list*</span></span>

<span data-ttu-id="bde6d-108">*记录列表*数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="bde6d-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="bde6d-109">返回值</span><span class="sxs-lookup"><span data-stu-id="bde6d-109">Return values</span></span>

<span data-ttu-id="bde6d-110">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="bde6d-110">*Record list*</span></span>

<span data-ttu-id="bde6d-111">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="bde6d-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="bde6d-112">示例</span><span class="sxs-lookup"><span data-stu-id="bde6d-112">Example</span></span>

<span data-ttu-id="bde6d-113">`EMPTYLIST (SPLIT ("abc", 1))` 返回具有与使用的 `SPLIT` 函数返回的列表相同结构的新空列表。</span><span class="sxs-lookup"><span data-stu-id="bde6d-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bde6d-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="bde6d-114">Additional resources</span></span>

[<span data-ttu-id="bde6d-115">列表函数</span><span class="sxs-lookup"><span data-stu-id="bde6d-115">List functions</span></span>](er-functions-category-list.md)

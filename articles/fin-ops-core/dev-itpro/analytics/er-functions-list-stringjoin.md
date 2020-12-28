---
title: STRINGJOIN ER 函数
description: 本主题提供有关 STRINGJOIN 电子申报 (ER) 函数如何使用的信息。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 586dbcb98d237325188f4b0384580613ab7a9347
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683719"
---
# <a name="stringjoin-er-function"></a><span data-ttu-id="d88fe-103">STRINGJOIN ER 函数</span><span class="sxs-lookup"><span data-stu-id="d88fe-103">STRINGJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d88fe-104">`STRINGJOIN` 函数返回由指定列表中的指定字段的连接值组成的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="d88fe-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="d88fe-105">这些值可以通过指定分隔符分隔。</span><span class="sxs-lookup"><span data-stu-id="d88fe-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="d88fe-106">语法</span><span class="sxs-lookup"><span data-stu-id="d88fe-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="d88fe-107">参数</span><span class="sxs-lookup"><span data-stu-id="d88fe-107">Arguments</span></span>

<span data-ttu-id="d88fe-108">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="d88fe-108">`list`: *Record list*</span></span>

<span data-ttu-id="d88fe-109">*记录列表* 数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="d88fe-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="d88fe-110">`field`：*字段*</span><span class="sxs-lookup"><span data-stu-id="d88fe-110">`field`: *Field*</span></span>

<span data-ttu-id="d88fe-111">指定列表中 *字符串* 数据类型的字段的有效路径。</span><span class="sxs-lookup"><span data-stu-id="d88fe-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="d88fe-112">`delimiter`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="d88fe-112">`delimiter`: *String*</span></span>

<span data-ttu-id="d88fe-113">用于分隔子字符串的分隔符。</span><span class="sxs-lookup"><span data-stu-id="d88fe-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="d88fe-114">返回值</span><span class="sxs-lookup"><span data-stu-id="d88fe-114">Return values</span></span>

<span data-ttu-id="d88fe-115">*字符串*</span><span class="sxs-lookup"><span data-stu-id="d88fe-115">*String*</span></span>

<span data-ttu-id="d88fe-116">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="d88fe-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d88fe-117">示例</span><span class="sxs-lookup"><span data-stu-id="d88fe-117">Example</span></span>

<span data-ttu-id="d88fe-118">如果输入 `SPLIT("abc" , 1)` 作为数据源 **DS**，表达式 `STRINGJOIN (DS, DS.Value, "-")` 将返回 **"a-b-c"**。</span><span class="sxs-lookup"><span data-stu-id="d88fe-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d88fe-119">其他资源</span><span class="sxs-lookup"><span data-stu-id="d88fe-119">Additional resources</span></span>

[<span data-ttu-id="d88fe-120">列表函数</span><span class="sxs-lookup"><span data-stu-id="d88fe-120">List functions</span></span>](er-functions-category-list.md)

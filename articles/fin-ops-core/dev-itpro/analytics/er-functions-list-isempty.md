---
title: ISEMPTY ER 函数
description: 本主题提供有关 ISEMPTY 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 5dbba375104b57f9fb09ed4e330d85181ec0dff8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684875"
---
# <a name="isempty-er-function"></a><span data-ttu-id="3cebe-103">ISEMPTY ER 函数</span><span class="sxs-lookup"><span data-stu-id="3cebe-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3cebe-104">`ISEMPTY` 函数返回一个 *布尔* 值 **TRUE**（如果指定列表未包含记录）。</span><span class="sxs-lookup"><span data-stu-id="3cebe-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="3cebe-105">否则，返回 *布尔* 值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="3cebe-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cebe-106">语法</span><span class="sxs-lookup"><span data-stu-id="3cebe-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="3cebe-107">参数</span><span class="sxs-lookup"><span data-stu-id="3cebe-107">Arguments</span></span>

<span data-ttu-id="3cebe-108">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="3cebe-108">`list`: *Record list*</span></span>

<span data-ttu-id="3cebe-109">*记录列表* 数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="3cebe-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="3cebe-110">返回值</span><span class="sxs-lookup"><span data-stu-id="3cebe-110">Return values</span></span>

<span data-ttu-id="3cebe-111">*布尔值*</span><span class="sxs-lookup"><span data-stu-id="3cebe-111">*Boolean*</span></span>

<span data-ttu-id="3cebe-112">生成的 *布尔* 值。</span><span class="sxs-lookup"><span data-stu-id="3cebe-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="3cebe-113">示例 1</span><span class="sxs-lookup"><span data-stu-id="3cebe-113">Example 1</span></span>

<span data-ttu-id="3cebe-114">如果输入 *计算字段* 类型的数据源 **DS**，并且它包含表达式 `SPLIT ("A|B|C", "|")`，表达式 `ISEMPTY(DS)` 将返回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="3cebe-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="3cebe-115">示例 2</span><span class="sxs-lookup"><span data-stu-id="3cebe-115">Example 2</span></span>

<span data-ttu-id="3cebe-116">表达式 `ISEMPTY (SPLIT ("",1))` 返回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="3cebe-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3cebe-117">其他资源</span><span class="sxs-lookup"><span data-stu-id="3cebe-117">Additional resources</span></span>

[<span data-ttu-id="3cebe-118">列表函数</span><span class="sxs-lookup"><span data-stu-id="3cebe-118">List functions</span></span>](er-functions-category-list.md)

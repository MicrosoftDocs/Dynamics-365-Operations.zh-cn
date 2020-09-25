---
title: FIRST ER 函数
description: 本主题提供有关 FIRST 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 3ed0e0aaf29e2a67a4842d71121f1adc24f524f7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745217"
---
# <a name="first-er-function"></a><span data-ttu-id="d28bf-103">FIRST ER 函数</span><span class="sxs-lookup"><span data-stu-id="d28bf-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d28bf-104">`FIRST` 函数返回指定列表的第一条记录为*容器（记录）* 值（如果该列表不为空）。</span><span class="sxs-lookup"><span data-stu-id="d28bf-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="d28bf-105">如果列表为空，此函数将引发异常。</span><span class="sxs-lookup"><span data-stu-id="d28bf-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="d28bf-106">语法</span><span class="sxs-lookup"><span data-stu-id="d28bf-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="d28bf-107">参数</span><span class="sxs-lookup"><span data-stu-id="d28bf-107">Arguments</span></span>

<span data-ttu-id="d28bf-108">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="d28bf-108">`list`: *Record list*</span></span>

<span data-ttu-id="d28bf-109">*记录列表*数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="d28bf-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d28bf-110">返回值</span><span class="sxs-lookup"><span data-stu-id="d28bf-110">Return values</span></span>

<span data-ttu-id="d28bf-111">*容器（记录）*</span><span class="sxs-lookup"><span data-stu-id="d28bf-111">*Container (record)*</span></span>

<span data-ttu-id="d28bf-112">生成的记录值。</span><span class="sxs-lookup"><span data-stu-id="d28bf-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="d28bf-113">示例 1</span><span class="sxs-lookup"><span data-stu-id="d28bf-113">Example 1</span></span>

<span data-ttu-id="d28bf-114">表达式 `FIRST(SPLIT("ABC",1)).Value` 返回文本值 **"A"**。</span><span class="sxs-lookup"><span data-stu-id="d28bf-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d28bf-115">示例 2</span><span class="sxs-lookup"><span data-stu-id="d28bf-115">Example 2</span></span>

<span data-ttu-id="d28bf-116">表达式 `FIRST(SPLIT("",1)).Value` 在运行时引发异常。</span><span class="sxs-lookup"><span data-stu-id="d28bf-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d28bf-117">其他资源</span><span class="sxs-lookup"><span data-stu-id="d28bf-117">Additional resources</span></span>

[<span data-ttu-id="d28bf-118">列表函数</span><span class="sxs-lookup"><span data-stu-id="d28bf-118">List functions</span></span>](er-functions-category-list.md)

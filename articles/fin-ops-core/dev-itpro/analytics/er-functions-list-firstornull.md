---
title: FIRSTORNULL ER 函数
description: 本主题说明 FIRSTORNULL 电子申报 (ER) 函数如何使用
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: e360812c5b0dbfb8df4ab279bf3e0050acebbb25
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745187"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="bac86-103">FIRSTORNULL ER 函数</span><span class="sxs-lookup"><span data-stu-id="bac86-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bac86-104">`FIRSTORNULL` 函数返回指定列表的第一条记录为*容器（记录）* 值（如果该记录不为空）。</span><span class="sxs-lookup"><span data-stu-id="bac86-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="bac86-105">如果记录为空，此函数将返回空*容器（记录）* 值。</span><span class="sxs-lookup"><span data-stu-id="bac86-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="bac86-106">语法</span><span class="sxs-lookup"><span data-stu-id="bac86-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="bac86-107">参数</span><span class="sxs-lookup"><span data-stu-id="bac86-107">Arguments</span></span>

<span data-ttu-id="bac86-108">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="bac86-108">`list`: *Record list*</span></span>

<span data-ttu-id="bac86-109">*记录列表*数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="bac86-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="bac86-110">返回值</span><span class="sxs-lookup"><span data-stu-id="bac86-110">Return values</span></span>

<span data-ttu-id="bac86-111">*容器（记录）*</span><span class="sxs-lookup"><span data-stu-id="bac86-111">*Container (record)*</span></span>

<span data-ttu-id="bac86-112">生成的记录值。</span><span class="sxs-lookup"><span data-stu-id="bac86-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="bac86-113">示例</span><span class="sxs-lookup"><span data-stu-id="bac86-113">Example</span></span>

<span data-ttu-id="bac86-114">表达式 `FIRSTORNULL(SPLIT("",1)).Value` 返回一个空字符串 (**""**)。</span><span class="sxs-lookup"><span data-stu-id="bac86-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bac86-115">其他资源</span><span class="sxs-lookup"><span data-stu-id="bac86-115">Additional resources</span></span>

[<span data-ttu-id="bac86-116">列表函数</span><span class="sxs-lookup"><span data-stu-id="bac86-116">List functions</span></span>](er-functions-category-list.md)

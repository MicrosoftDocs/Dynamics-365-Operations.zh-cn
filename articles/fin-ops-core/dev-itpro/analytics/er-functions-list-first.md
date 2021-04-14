---
title: FIRST ER 函数
description: 本主题提供有关 FIRST 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: d30c8481866ccf3f7080197b37586a0460a4ad2c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746571"
---
# <a name="first-er-function"></a><span data-ttu-id="f44e9-103">FIRST ER 函数</span><span class="sxs-lookup"><span data-stu-id="f44e9-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f44e9-104">`FIRST` 函数返回指定列表的第一条记录为 *容器（记录）* 值（如果该列表不为空）。</span><span class="sxs-lookup"><span data-stu-id="f44e9-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="f44e9-105">如果列表为空，此函数将引发异常。</span><span class="sxs-lookup"><span data-stu-id="f44e9-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="f44e9-106">语法</span><span class="sxs-lookup"><span data-stu-id="f44e9-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="f44e9-107">参数</span><span class="sxs-lookup"><span data-stu-id="f44e9-107">Arguments</span></span>

<span data-ttu-id="f44e9-108">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="f44e9-108">`list`: *Record list*</span></span>

<span data-ttu-id="f44e9-109">*记录列表* 数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="f44e9-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f44e9-110">返回值</span><span class="sxs-lookup"><span data-stu-id="f44e9-110">Return values</span></span>

<span data-ttu-id="f44e9-111">*容器（记录）*</span><span class="sxs-lookup"><span data-stu-id="f44e9-111">*Container (record)*</span></span>

<span data-ttu-id="f44e9-112">生成的记录值。</span><span class="sxs-lookup"><span data-stu-id="f44e9-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="f44e9-113">示例 1</span><span class="sxs-lookup"><span data-stu-id="f44e9-113">Example 1</span></span>

<span data-ttu-id="f44e9-114">表达式 `FIRST(SPLIT("ABC",1)).Value` 返回文本值 **"A"**。</span><span class="sxs-lookup"><span data-stu-id="f44e9-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f44e9-115">示例 2</span><span class="sxs-lookup"><span data-stu-id="f44e9-115">Example 2</span></span>

<span data-ttu-id="f44e9-116">表达式 `FIRST(SPLIT("",1)).Value` 在运行时引发异常。</span><span class="sxs-lookup"><span data-stu-id="f44e9-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f44e9-117">其他资源</span><span class="sxs-lookup"><span data-stu-id="f44e9-117">Additional resources</span></span>

[<span data-ttu-id="f44e9-118">列表函数</span><span class="sxs-lookup"><span data-stu-id="f44e9-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
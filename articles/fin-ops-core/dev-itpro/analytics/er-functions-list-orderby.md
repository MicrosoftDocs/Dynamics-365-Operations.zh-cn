---
title: ORDERBY ER 函数
description: 本主题提供有关 ORDERBY 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 0a6b5cddc325625dc5b3d677ffcc1da1f8b829cd
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041944"
---
# <span data-ttu-id="c0548-103"><a name="ORDERBY">ORDERBY ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="c0548-103"><a name="ORDERBY">ORDERBY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0548-104">在根据指定的参数对指定列表进行排序之后，`ORDERBY` 函数将指定列表返回为*记录列表*值。</span><span class="sxs-lookup"><span data-stu-id="c0548-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="c0548-105">可将这些变量定义为表达式。</span><span class="sxs-lookup"><span data-stu-id="c0548-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0548-106">语法</span><span class="sxs-lookup"><span data-stu-id="c0548-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="c0548-107">参数</span><span class="sxs-lookup"><span data-stu-id="c0548-107">Arguments</span></span>

<span data-ttu-id="c0548-108">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="c0548-108">`list`: *Record list*</span></span>

<span data-ttu-id="c0548-109">*记录列表*数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="c0548-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="c0548-110">`expression 1`：*字段*</span><span class="sxs-lookup"><span data-stu-id="c0548-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="c0548-111">被调用函数的 `list` 参数引用的数据源字段的有效路径。</span><span class="sxs-lookup"><span data-stu-id="c0548-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="c0548-112">引用的字段必须是原始数据类型的字段。</span><span class="sxs-lookup"><span data-stu-id="c0548-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="c0548-113">此参数是必需的。</span><span class="sxs-lookup"><span data-stu-id="c0548-113">This argument is required.</span></span>

<span data-ttu-id="c0548-114">`expression N`：*字段*</span><span class="sxs-lookup"><span data-stu-id="c0548-114">`expression N`: *Field*</span></span>

<span data-ttu-id="c0548-115">被调用函数的 `list` 参数引用的数据源字段的有效路径。</span><span class="sxs-lookup"><span data-stu-id="c0548-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="c0548-116">引用的字段必须是原始数据类型的字段。</span><span class="sxs-lookup"><span data-stu-id="c0548-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="c0548-117">其他参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="c0548-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="c0548-118">返回值</span><span class="sxs-lookup"><span data-stu-id="c0548-118">Return values</span></span>

<span data-ttu-id="c0548-119">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="c0548-119">*Record list*</span></span>

<span data-ttu-id="c0548-120">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="c0548-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="c0548-121">示例 1</span><span class="sxs-lookup"><span data-stu-id="c0548-121">Example 1</span></span>

<span data-ttu-id="c0548-122">如果输入*计算字段*类型的数据源 **DS**，并且它包含表达式 `SPLIT ("C|B|A", "|")`，表达式 `FIRST( ORDERBY( DS, DS. Value)).Value` 将返回文本值 **"A"**。</span><span class="sxs-lookup"><span data-stu-id="c0548-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="c0548-123">示例 2</span><span class="sxs-lookup"><span data-stu-id="c0548-123">Example 2</span></span>

<span data-ttu-id="c0548-124">如果**供应商**配置为引用 VendTable 表的电子申报 (ER) 数据源，表达式 `ORDERBY (Vendors, Vendors.'name()')` 将返回按名称升序排序的供应商列表。</span><span class="sxs-lookup"><span data-stu-id="c0548-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0548-125">其他资源</span><span class="sxs-lookup"><span data-stu-id="c0548-125">Additional resources</span></span>

[<span data-ttu-id="c0548-126">列表函数</span><span class="sxs-lookup"><span data-stu-id="c0548-126">List functions</span></span>](er-functions-category-list.md)

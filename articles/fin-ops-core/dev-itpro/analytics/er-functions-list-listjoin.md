---
title: LISTJOIN ER 函数
description: 本主题提供有关 LISTJOIN 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28f03e5e6af0f252a994f2e54b57a5ef654f4e67
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682235"
---
# <a name="listjoin-er-function"></a><span data-ttu-id="8c8a9-103">LISTJOIN ER 函数</span><span class="sxs-lookup"><span data-stu-id="8c8a9-103">LISTJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c8a9-104">`LISTJOIN` 函数返回一个 *记录列表* 值，此值表示根据指定参数创建的记录的新连接列表。</span><span class="sxs-lookup"><span data-stu-id="8c8a9-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c8a9-105">语法</span><span class="sxs-lookup"><span data-stu-id="8c8a9-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="8c8a9-106">参数</span><span class="sxs-lookup"><span data-stu-id="8c8a9-106">Arguments</span></span>

<span data-ttu-id="8c8a9-107">`list 1`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="8c8a9-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="8c8a9-108">对 *记录列表* 数据类型的数据源的引用。</span><span class="sxs-lookup"><span data-stu-id="8c8a9-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="8c8a9-109">此参数是强制性的。</span><span class="sxs-lookup"><span data-stu-id="8c8a9-109">This argument is mandatory.</span></span>

<span data-ttu-id="8c8a9-110">`list N`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="8c8a9-110">`list N`: *Record list*</span></span>

<span data-ttu-id="8c8a9-111">对 *记录列表* 数据类型的数据源的引用。</span><span class="sxs-lookup"><span data-stu-id="8c8a9-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="8c8a9-112">其他参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="8c8a9-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="8c8a9-113">返回值</span><span class="sxs-lookup"><span data-stu-id="8c8a9-113">Return values</span></span>

<span data-ttu-id="8c8a9-114">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="8c8a9-114">*Record list*</span></span>

<span data-ttu-id="8c8a9-115">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="8c8a9-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8c8a9-116">使用说明</span><span class="sxs-lookup"><span data-stu-id="8c8a9-116">Usage notes</span></span>

<span data-ttu-id="8c8a9-117">创建的列表的结构仅包含在参数中提到的每个记录列表的结构中显示的字段。</span><span class="sxs-lookup"><span data-stu-id="8c8a9-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="8c8a9-118">示例</span><span class="sxs-lookup"><span data-stu-id="8c8a9-118">Example</span></span>

<span data-ttu-id="8c8a9-119">您输入 `Container` 类型的数据源 **记录 1**。</span><span class="sxs-lookup"><span data-stu-id="8c8a9-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="8c8a9-120">此数据源包含 `Calculated field` 类型的以下嵌套字段：</span><span class="sxs-lookup"><span data-stu-id="8c8a9-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="8c8a9-121">**代码**：此字段包含返回 `String` 类型的值的表达式。</span><span class="sxs-lookup"><span data-stu-id="8c8a9-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="8c8a9-122">**金额**：此字段包含返回 `Real` 类型的值的表达式。</span><span class="sxs-lookup"><span data-stu-id="8c8a9-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="8c8a9-123">然后输入 `Container` 类型的数据源 **记录 2**。</span><span class="sxs-lookup"><span data-stu-id="8c8a9-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="8c8a9-124">此数据源包含 `Calculated field` 类型的以下嵌套字段：</span><span class="sxs-lookup"><span data-stu-id="8c8a9-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="8c8a9-125">**金额**：此字段包含返回 `Real` 类型的值的表达式。</span><span class="sxs-lookup"><span data-stu-id="8c8a9-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="8c8a9-126">**IsValid**：此字段包含返回 `Boolean` 类型的值的表达式。</span><span class="sxs-lookup"><span data-stu-id="8c8a9-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

![ER 模型映射设计器页面](./media/er-functions-list-listjoin-image1.gif)

<span data-ttu-id="8c8a9-128">在此例中，表达式 `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` 返回包含两个记录的新列表。</span><span class="sxs-lookup"><span data-stu-id="8c8a9-128">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span>

![带有两个记录的 ER 模型映射设计器页面](./media/er-functions-list-listjoin-image2.gif)

<span data-ttu-id="8c8a9-130">此列表的结构由一个 `Real` 类型的 **金额** 字段组成，因为此字段是被调用函数每个参数中显示的唯一字段。</span><span class="sxs-lookup"><span data-stu-id="8c8a9-130">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

![ER 模型映射设计器页面金额字段](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a><span data-ttu-id="8c8a9-132">其他资源</span><span class="sxs-lookup"><span data-stu-id="8c8a9-132">Additional resources</span></span>

[<span data-ttu-id="8c8a9-133">列表函数</span><span class="sxs-lookup"><span data-stu-id="8c8a9-133">List functions</span></span>](er-functions-category-list.md)

[<span data-ttu-id="8c8a9-134">调试已执行 ER 格式的数据源以分析数据流和转换</span><span class="sxs-lookup"><span data-stu-id="8c8a9-134">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>](er-debug-data-sources.md)

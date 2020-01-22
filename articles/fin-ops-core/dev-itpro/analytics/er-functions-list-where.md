---
title: WHERE ER 函数
description: 本主题提供有关 WHERE 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 50d90697f522f3c4d7b62190928008b6d923ffc6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916077"
---
# <span data-ttu-id="967bd-103"><a name="WHERE">WHERE ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="967bd-103"><a name="WHERE">WHERE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="967bd-104">在根据指定的参数对指定列表进行筛选之后，`WHERE` 函数将指定的条件返回为*记录列表*值。</span><span class="sxs-lookup"><span data-stu-id="967bd-104">The `WHERE` function returns the specified list as a *Record list* value after it has been filtered according to the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="967bd-105">语法</span><span class="sxs-lookup"><span data-stu-id="967bd-105">Syntax</span></span>

```
WHERE (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="967bd-106">参数</span><span class="sxs-lookup"><span data-stu-id="967bd-106">Arguments</span></span>

<span data-ttu-id="967bd-107">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="967bd-107">`list`: *Record list*</span></span>

<span data-ttu-id="967bd-108">*记录列表*数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="967bd-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="967bd-109">`condition`：*布尔值*</span><span class="sxs-lookup"><span data-stu-id="967bd-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="967bd-110">用于筛选指定列表的记录的有效的条件表达式。</span><span class="sxs-lookup"><span data-stu-id="967bd-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="967bd-111">返回值</span><span class="sxs-lookup"><span data-stu-id="967bd-111">Return values</span></span>

<span data-ttu-id="967bd-112">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="967bd-112">*Record list*</span></span>

<span data-ttu-id="967bd-113">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="967bd-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="967bd-114">使用说明</span><span class="sxs-lookup"><span data-stu-id="967bd-114">Usage notes</span></span>

<span data-ttu-id="967bd-115">此函数与 [FILTER](er-functions-list-filter.md) 函数不同，因为指定条件适用于在内存中呈现的*记录列表*类型的任何电子申报 (ER) 数据源。</span><span class="sxs-lookup"><span data-stu-id="967bd-115">This function differs from the [FILTER](er-functions-list-filter.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="967bd-116">如果为此函数配置的参数（`list` 和 `condition`）允许将此请求转换为直接 SQL 调用，在设计时会引发警告消息。</span><span class="sxs-lookup"><span data-stu-id="967bd-116">If the arguments that are configured for this function (`list` and `condition`) allow this request to be translated to the direct SQL call, a warning message is thrown at design time.</span></span> <span data-ttu-id="967bd-117">此消息通知用户，如果使用 [FILTER](er-functions-list-filter.md) 函数而不是 `WHERE`，性能可能会提高。</span><span class="sxs-lookup"><span data-stu-id="967bd-117">This message informs the user that performance might be improved if the [FILTER](er-functions-list-filter.md) function is used instead of `WHERE`.</span></span>

## <a name="example-1"></a><span data-ttu-id="967bd-118">示例 1</span><span class="sxs-lookup"><span data-stu-id="967bd-118">Example 1</span></span>

<span data-ttu-id="967bd-119">如果**供应商**配置为引用 VendTable 表的 ER 数据源，表达式 `WHERE (Vendors, Vendors.VendGroup = "40")` 将返回仅包含属于供应商组 40 的供应商的列表。</span><span class="sxs-lookup"><span data-stu-id="967bd-119">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `WHERE (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="967bd-120">示例 2</span><span class="sxs-lookup"><span data-stu-id="967bd-120">Example 2</span></span>

<span data-ttu-id="967bd-121">如果输入*计算字段*类型的数据源 **DS**，而该数据源中包含表达式 `SPLIT ("A|B|C", "|")`，则表达式 `WHERE( DS, DS.Value = "B")` 将返回仅在**值**字段中包含文本 **"B"** 的一条记录的列表。</span><span class="sxs-lookup"><span data-stu-id="967bd-121">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `WHERE( DS, DS.Value = "B")` returns a list of only one record that contains the text **"B"** in the **Value** field.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="967bd-122">其他资源</span><span class="sxs-lookup"><span data-stu-id="967bd-122">Additional resources</span></span>

[<span data-ttu-id="967bd-123">列表函数</span><span class="sxs-lookup"><span data-stu-id="967bd-123">List functions</span></span>](er-functions-category-list.md)

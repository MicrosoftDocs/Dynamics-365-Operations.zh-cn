---
title: INDEX ER 函数
description: 本主题提供有关 INDEX 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 051e22daa3fe2d6c328e36403201d940f724bd29
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745169"
---
# <a name="index-er-function"></a><span data-ttu-id="81196-103">INDEX ER 函数</span><span class="sxs-lookup"><span data-stu-id="81196-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81196-104">`INDEX` 函数返回使用指定列表中的指定数字索引选择的*容器（记录）* 值。</span><span class="sxs-lookup"><span data-stu-id="81196-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="81196-105">如果索引超出了指定列表中的记录范围，将引发异常。</span><span class="sxs-lookup"><span data-stu-id="81196-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="81196-106">语法</span><span class="sxs-lookup"><span data-stu-id="81196-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="81196-107">参数</span><span class="sxs-lookup"><span data-stu-id="81196-107">Arguments</span></span>

<span data-ttu-id="81196-108">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="81196-108">`list`: *Record list*</span></span>

<span data-ttu-id="81196-109">*记录列表*数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="81196-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="81196-110">`index`：*整数*</span><span class="sxs-lookup"><span data-stu-id="81196-110">`index`: *Integer*</span></span>

<span data-ttu-id="81196-111">指示所需记录在指定列表中的位置的数字索引。</span><span class="sxs-lookup"><span data-stu-id="81196-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="81196-112">返回值</span><span class="sxs-lookup"><span data-stu-id="81196-112">Return values</span></span>

<span data-ttu-id="81196-113">*容器（记录）*</span><span class="sxs-lookup"><span data-stu-id="81196-113">*Container (record)*</span></span>

<span data-ttu-id="81196-114">生成的记录值。</span><span class="sxs-lookup"><span data-stu-id="81196-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="81196-115">示例 1</span><span class="sxs-lookup"><span data-stu-id="81196-115">Example 1</span></span>

<span data-ttu-id="81196-116">如果输入*计算字段*类型的数据源 **DS**，而该数据源中包含表达式 `SPLIT ("A|B|C", "|")`，则表达式 `DS.Value` 将返回此记录列表的第二条记录的文本值 **"B"**。</span><span class="sxs-lookup"><span data-stu-id="81196-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="81196-117">表达式 `INDEX (SPLIT ("A|B|C", "|"), 2).Value` 也会返回文本值 **"B"**。</span><span class="sxs-lookup"><span data-stu-id="81196-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="81196-118">示例 2</span><span class="sxs-lookup"><span data-stu-id="81196-118">Example 2</span></span>

<span data-ttu-id="81196-119">如果输入*计算字段*类型的数据源 **DS**，并且它包含表达式 `SPLIT ("A|B|C", "|")`，表达式 `INDEX (SPLIT ("A|B|C", "|"), 4).Value` 将在运行时引发异常。</span><span class="sxs-lookup"><span data-stu-id="81196-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81196-120">其他资源</span><span class="sxs-lookup"><span data-stu-id="81196-120">Additional resources</span></span>

[<span data-ttu-id="81196-121">列表函数</span><span class="sxs-lookup"><span data-stu-id="81196-121">List functions</span></span>](er-functions-category-list.md)

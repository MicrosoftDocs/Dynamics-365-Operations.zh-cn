---
title: REVERSE ER 函数
description: 本主题提供有关 REVERSE 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 895d5f13f065b2188f245d081fa69e7e63555dde
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686432"
---
# <a name="reverse-er-function"></a><span data-ttu-id="4b72b-103">REVERSE ER 函数</span><span class="sxs-lookup"><span data-stu-id="4b72b-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b72b-104">`REVERSE` 函数以相反的排序顺序将指定列表返回为 *记录列表* 值。</span><span class="sxs-lookup"><span data-stu-id="4b72b-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b72b-105">语法</span><span class="sxs-lookup"><span data-stu-id="4b72b-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="4b72b-106">参数</span><span class="sxs-lookup"><span data-stu-id="4b72b-106">Arguments</span></span>

<span data-ttu-id="4b72b-107">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="4b72b-107">`list`: *Record list*</span></span>

<span data-ttu-id="4b72b-108">*记录列表* 数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="4b72b-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="4b72b-109">返回值</span><span class="sxs-lookup"><span data-stu-id="4b72b-109">Return values</span></span>

<span data-ttu-id="4b72b-110">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="4b72b-110">*Record list*</span></span>

<span data-ttu-id="4b72b-111">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="4b72b-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="4b72b-112">示例 1</span><span class="sxs-lookup"><span data-stu-id="4b72b-112">Example 1</span></span>

<span data-ttu-id="4b72b-113">如果输入 *计算字段* 类型的数据源 **DS**，并且它包含表达式 `SPLIT ("C|B|A", "|")`，表达式 `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` 将返回文本值 **"C"**。</span><span class="sxs-lookup"><span data-stu-id="4b72b-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="4b72b-114">示例 2</span><span class="sxs-lookup"><span data-stu-id="4b72b-114">Example 2</span></span>

<span data-ttu-id="4b72b-115">如果 **供应商** 配置为引用 VendTable 表的电子申报 (ER) 数据源，表达式 `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` 将返回按名称降序排序的供应商列表。</span><span class="sxs-lookup"><span data-stu-id="4b72b-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4b72b-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="4b72b-116">Additional resources</span></span>

[<span data-ttu-id="4b72b-117">列表函数</span><span class="sxs-lookup"><span data-stu-id="4b72b-117">List functions</span></span>](er-functions-category-list.md)

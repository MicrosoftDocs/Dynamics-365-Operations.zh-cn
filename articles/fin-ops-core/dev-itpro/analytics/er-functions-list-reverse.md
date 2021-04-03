---
title: REVERSE ER 函数
description: 本主题提供有关 REVERSE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
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
ms.openlocfilehash: f76582bc8b752fe0322bee8917d8649ed1c024ba
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567358"
---
# <a name="reverse-er-function"></a><span data-ttu-id="1e753-103">REVERSE ER 函数</span><span class="sxs-lookup"><span data-stu-id="1e753-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e753-104">`REVERSE` 函数以相反的排序顺序将指定列表返回为 *记录列表* 值。</span><span class="sxs-lookup"><span data-stu-id="1e753-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e753-105">语法</span><span class="sxs-lookup"><span data-stu-id="1e753-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="1e753-106">参数</span><span class="sxs-lookup"><span data-stu-id="1e753-106">Arguments</span></span>

<span data-ttu-id="1e753-107">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="1e753-107">`list`: *Record list*</span></span>

<span data-ttu-id="1e753-108">*记录列表* 数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="1e753-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="1e753-109">返回值</span><span class="sxs-lookup"><span data-stu-id="1e753-109">Return values</span></span>

<span data-ttu-id="1e753-110">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="1e753-110">*Record list*</span></span>

<span data-ttu-id="1e753-111">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="1e753-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="1e753-112">示例 1</span><span class="sxs-lookup"><span data-stu-id="1e753-112">Example 1</span></span>

<span data-ttu-id="1e753-113">如果输入 *计算字段* 类型的数据源 **DS**，并且它包含表达式 `SPLIT ("C|B|A", "|")`，表达式 `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` 将返回文本值 **"C"**。</span><span class="sxs-lookup"><span data-stu-id="1e753-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="1e753-114">示例 2</span><span class="sxs-lookup"><span data-stu-id="1e753-114">Example 2</span></span>

<span data-ttu-id="1e753-115">如果 **供应商** 配置为引用 VendTable 表的电子申报 (ER) 数据源，表达式 `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` 将返回按名称降序排序的供应商列表。</span><span class="sxs-lookup"><span data-stu-id="1e753-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e753-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="1e753-116">Additional resources</span></span>

[<span data-ttu-id="1e753-117">列表函数</span><span class="sxs-lookup"><span data-stu-id="1e753-117">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
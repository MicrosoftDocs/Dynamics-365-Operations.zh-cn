---
title: FILTER ER 函数
description: 本主题提供有关 FILTER 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 55fa3d4ad4427e2a45f7c5fce679c50a91c40b6d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679430"
---
# <a name="filter-er-function"></a><span data-ttu-id="0285e-103">FILTER ER 函数</span><span class="sxs-lookup"><span data-stu-id="0285e-103">FILTER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0285e-104">`FILTER` 函数在查询更改以针对指定条件进行筛选后作为 *记录列表* 值返回指定列表。</span><span class="sxs-lookup"><span data-stu-id="0285e-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="0285e-105">语法</span><span class="sxs-lookup"><span data-stu-id="0285e-105">Syntax</span></span>

```vb
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="0285e-106">参数</span><span class="sxs-lookup"><span data-stu-id="0285e-106">Arguments</span></span>

<span data-ttu-id="0285e-107">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="0285e-107">`list`: *Record list*</span></span>

<span data-ttu-id="0285e-108">*记录列表* 数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="0285e-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="0285e-109">`condition`：*布尔值*</span><span class="sxs-lookup"><span data-stu-id="0285e-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="0285e-110">用于筛选指定列表的记录的有效的条件表达式。</span><span class="sxs-lookup"><span data-stu-id="0285e-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="0285e-111">返回值</span><span class="sxs-lookup"><span data-stu-id="0285e-111">Return values</span></span>

<span data-ttu-id="0285e-112">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="0285e-112">*Record list*</span></span>

<span data-ttu-id="0285e-113">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="0285e-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0285e-114">使用说明</span><span class="sxs-lookup"><span data-stu-id="0285e-114">Usage notes</span></span>

<span data-ttu-id="0285e-115">此函数与 [WHERE](er-functions-list-where.md) 函数不同，因为指定条件适用于数据库级别的 *表格记录* 类型的任何电子申报 (ER) 数据源。</span><span class="sxs-lookup"><span data-stu-id="0285e-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="0285e-116">可使用表格和关系定义列表和条件。</span><span class="sxs-lookup"><span data-stu-id="0285e-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="0285e-117">如果为此函数配置的一个或两个参数（`list` 和 `condition`）不允许将此请求转换为直接 SQL 调用，在设计时会引发异常。</span><span class="sxs-lookup"><span data-stu-id="0285e-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="0285e-118">此异常通知用户 `list` 或 `condition` 不能用于查询数据库。</span><span class="sxs-lookup"><span data-stu-id="0285e-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="0285e-119">示例 1</span><span class="sxs-lookup"><span data-stu-id="0285e-119">Example 1</span></span>

<span data-ttu-id="0285e-120">如果 **供应商** 配置为引用 VendTable 表的 ER 数据源，表达式 `FILTER (Vendors, Vendors.VendGroup = "40")` 将返回仅包含属于供应商组 40 的供应商的列表。</span><span class="sxs-lookup"><span data-stu-id="0285e-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="0285e-121">示例 2</span><span class="sxs-lookup"><span data-stu-id="0285e-121">Example 2</span></span>

<span data-ttu-id="0285e-122">如果 **供应商** 配置为引用 VendTable 表的 ER 数据源，并且配置为 ER 数据源的 **parmVendorBankGroup** 返回 *字符串* 数据类型的值，表达式 `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` 将返回仅包含属于特定银行组的供应商帐户的列表。</span><span class="sxs-lookup"><span data-stu-id="0285e-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="0285e-123">示例 3</span><span class="sxs-lookup"><span data-stu-id="0285e-123">Example 3</span></span>

<span data-ttu-id="0285e-124">输入 *计算字段* 类型的数据源 **DS**，它包含表达式 `SPLIT ("A,B,C", ",")`。</span><span class="sxs-lookup"><span data-stu-id="0285e-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="0285e-125">然后输入另一个表达式 `FILTER( DS, DS.Value = "B")`。</span><span class="sxs-lookup"><span data-stu-id="0285e-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="0285e-126">当您尝试在 ER 公式设计器中保存此表达式时，将引发以下异常：“验证错误：FILTER 函数的列表表达式不可查询。”</span><span class="sxs-lookup"><span data-stu-id="0285e-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0285e-127">其他资源</span><span class="sxs-lookup"><span data-stu-id="0285e-127">Additional resources</span></span>

[<span data-ttu-id="0285e-128">列表函数</span><span class="sxs-lookup"><span data-stu-id="0285e-128">List functions</span></span>](er-functions-category-list.md)

---
title: CONTAINS ER 函数
description: 本主题提供有关 CONTAINS 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: a31d89f036a6e821bea2b6733c0c646145d2a47c
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048862"
---
# <a name="contains-er-function"></a><span data-ttu-id="0a0f8-103">CONTAINS ER 函数</span><span class="sxs-lookup"><span data-stu-id="0a0f8-103">CONTAINS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a0f8-104">`CONTAINS` 函数确定指定的输入是否包含指定文本。</span><span class="sxs-lookup"><span data-stu-id="0a0f8-104">The `CONTAINS` function determines whether the specified input contains the specified text.</span></span> <span data-ttu-id="0a0f8-105">如果指定的输入包含指定的文本，此函数将返回一个 **TRUE** *布尔* 值。</span><span class="sxs-lookup"><span data-stu-id="0a0f8-105">It returns a *Boolean* value of **TRUE** if the specified input contains the specified text.</span></span> <span data-ttu-id="0a0f8-106">否则，返回 *布尔* 值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="0a0f8-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a0f8-107">语法</span><span class="sxs-lookup"><span data-stu-id="0a0f8-107">Syntax</span></span>

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a><span data-ttu-id="0a0f8-108">参数</span><span class="sxs-lookup"><span data-stu-id="0a0f8-108">Arguments</span></span>

<span data-ttu-id="0a0f8-109">`input`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="0a0f8-109">`input`: *String*</span></span>

<span data-ttu-id="0a0f8-110">*字符串* 类型或字符串常量的数据源项的有效路径，其值可能包含第二个参数。</span><span class="sxs-lookup"><span data-stu-id="0a0f8-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might contain the second argument.</span></span>

<span data-ttu-id="0a0f8-111">`search text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="0a0f8-111">`search text`: *String*</span></span>

<span data-ttu-id="0a0f8-112">*字符串* 数据类型或字符串常量的数据源的有效路径，其值可能包含在第一个参数中。</span><span class="sxs-lookup"><span data-stu-id="0a0f8-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be contained in the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="0a0f8-113">返回值</span><span class="sxs-lookup"><span data-stu-id="0a0f8-113">Return values</span></span>

<span data-ttu-id="0a0f8-114">*Boolean*</span><span class="sxs-lookup"><span data-stu-id="0a0f8-114">*Boolean*</span></span>

<span data-ttu-id="0a0f8-115">生成的 *布尔* 值。</span><span class="sxs-lookup"><span data-stu-id="0a0f8-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0a0f8-116">使用说明</span><span class="sxs-lookup"><span data-stu-id="0a0f8-116">Usage notes</span></span>

<span data-ttu-id="0a0f8-117">仅在 [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) 中配置了相关映射以访问 [Microsoft Dataverse](/power-platform/admin/data-integrator) 时，此函数才可用于指定 [FILTER](er-functions-list-filter.md) 函数的条件表达式。</span><span class="sxs-lookup"><span data-stu-id="0a0f8-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="0a0f8-118">否则，在设计时会引发异常。</span><span class="sxs-lookup"><span data-stu-id="0a0f8-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="0a0f8-119">您收到的消息建议您使用 [WHERE](er-functions-list-where.md) 函数而不是 `FILTER` 函数。</span><span class="sxs-lookup"><span data-stu-id="0a0f8-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="0a0f8-120">示例 1</span><span class="sxs-lookup"><span data-stu-id="0a0f8-120">Example 1</span></span>

<span data-ttu-id="0a0f8-121">表达式 `CONTAINS ("abc", "d")` 返回 **FALSE**，而表达式 `CONTAINS ("abc", "C")` 返回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="0a0f8-121">The expression `CONTAINS ("abc", "d")` returns **FALSE**, whereas the expression `CONTAINS ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0a0f8-122">示例 2</span><span class="sxs-lookup"><span data-stu-id="0a0f8-122">Example 2</span></span>

<span data-ttu-id="0a0f8-123">如果 **模型** 数据源的 **地址** 字段的值包含字符串 **DEU**，则表达式 `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` 返回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="0a0f8-123">The expression `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` returns **TRUE** if the value of the **Address** field of the **model** data source contains the string **DEU**.</span></span> <span data-ttu-id="0a0f8-124">否则，它将返回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="0a0f8-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0a0f8-125">其他资源</span><span class="sxs-lookup"><span data-stu-id="0a0f8-125">Additional resources</span></span>

[<span data-ttu-id="0a0f8-126">逻辑函数</span><span class="sxs-lookup"><span data-stu-id="0a0f8-126">Logical functions</span></span>](er-functions-category-logical.md)

---
title: STARTSWITH ER 函数
description: 本主题提供有关 STARTSWITH 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 22e99d9e131410820abd12536b8d4f3e868c6863
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557501"
---
# <a name="startswith-er-function"></a><span data-ttu-id="50969-103">STARTSWITH ER 函数</span><span class="sxs-lookup"><span data-stu-id="50969-103">STARTSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50969-104">`STARTSWITH` 函数确定指定的输入是否以指定文本开头。</span><span class="sxs-lookup"><span data-stu-id="50969-104">The `STARTSWITH` function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="50969-105">如果指定的输入以指定文本开头，此函数将返回一个 **TRUE** *布尔* 值。</span><span class="sxs-lookup"><span data-stu-id="50969-105">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="50969-106">否则，返回 *布尔* 值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="50969-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="50969-107">语法</span><span class="sxs-lookup"><span data-stu-id="50969-107">Syntax</span></span>

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a><span data-ttu-id="50969-108">参数</span><span class="sxs-lookup"><span data-stu-id="50969-108">Arguments</span></span>

<span data-ttu-id="50969-109">`input`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="50969-109">`input`: *String*</span></span>

<span data-ttu-id="50969-110">*字符串* 类型或字符串常量的数据源项的有效路径，其值可能以第二个参数为开头。</span><span class="sxs-lookup"><span data-stu-id="50969-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might start with the second argument.</span></span>

<span data-ttu-id="50969-111">`start text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="50969-111">`start text`: *String*</span></span>

<span data-ttu-id="50969-112">*字符串* 数据类型或字符串常量的数据源的有效路径，其值可能在第一个参数的开头。</span><span class="sxs-lookup"><span data-stu-id="50969-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the beginning of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="50969-113">返回值</span><span class="sxs-lookup"><span data-stu-id="50969-113">Return values</span></span>

<span data-ttu-id="50969-114">*Boolean*</span><span class="sxs-lookup"><span data-stu-id="50969-114">*Boolean*</span></span>

<span data-ttu-id="50969-115">生成的 *布尔* 值。</span><span class="sxs-lookup"><span data-stu-id="50969-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="50969-116">使用说明</span><span class="sxs-lookup"><span data-stu-id="50969-116">Usage notes</span></span>

<span data-ttu-id="50969-117">仅在 [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) 中配置了相关映射以访问 [Microsoft Dataverse](../data-entities/data-integration-cds.md) 时，此函数才可用于指定 [FILTER](er-functions-list-filter.md) 函数的条件表达式。</span><span class="sxs-lookup"><span data-stu-id="50969-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="50969-118">否则，在设计时会引发异常。</span><span class="sxs-lookup"><span data-stu-id="50969-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="50969-119">您收到的消息建议您使用 [WHERE](er-functions-list-where.md) 函数而不是 `FILTER` 函数。</span><span class="sxs-lookup"><span data-stu-id="50969-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="50969-120">示例 1</span><span class="sxs-lookup"><span data-stu-id="50969-120">Example 1</span></span>

<span data-ttu-id="50969-121">表达式 `STARTSWITH ("abc", "d")` 返回 **FALSE**，而表达式 `STARTSWITH ("abc", "A")` 返回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="50969-121">The expression `STARTSWITH ("abc", "d")` returns **FALSE**, whereas the expression `STARTSWITH ("abc", "A")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="50969-122">示例 2</span><span class="sxs-lookup"><span data-stu-id="50969-122">Example 2</span></span>

<span data-ttu-id="50969-123">如果 **模型** 数据源的 **地址** 字段的值以符串 **123 Coffee Street** 为开头，则表达式 `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` 返回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="50969-123">The expression `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returns **TRUE** if the value of the **Address** field of the **model** data source starts with the string **123 Coffee Street**.</span></span> <span data-ttu-id="50969-124">否则，它将返回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="50969-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="50969-125">其他资源</span><span class="sxs-lookup"><span data-stu-id="50969-125">Additional resources</span></span>

[<span data-ttu-id="50969-126">逻辑函数</span><span class="sxs-lookup"><span data-stu-id="50969-126">Logical functions</span></span>](er-functions-category-logical.md)

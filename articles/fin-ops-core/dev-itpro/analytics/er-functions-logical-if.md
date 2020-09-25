---
title: IF ER 函数
description: 本主题提供有关 IF 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 87e252a2751beeecb51e512cae38b271c1456fae
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744687"
---
# <a name="if-er-function"></a><span data-ttu-id="9a37a-103">IF ER 函数</span><span class="sxs-lookup"><span data-stu-id="9a37a-103">IF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a37a-104">如果满足指定条件，`IF` 函数返回第一个指定值。</span><span class="sxs-lookup"><span data-stu-id="9a37a-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="9a37a-105">否则，返回第二个指定值。</span><span class="sxs-lookup"><span data-stu-id="9a37a-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="9a37a-106">返回的值可以是任何受支持的数据类型的值。</span><span class="sxs-lookup"><span data-stu-id="9a37a-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a37a-107">语法</span><span class="sxs-lookup"><span data-stu-id="9a37a-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="9a37a-108">参数</span><span class="sxs-lookup"><span data-stu-id="9a37a-108">Arguments</span></span>

<span data-ttu-id="9a37a-109">`condition`：*布尔值*</span><span class="sxs-lookup"><span data-stu-id="9a37a-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="9a37a-110">必须测试的有效条件表达式。</span><span class="sxs-lookup"><span data-stu-id="9a37a-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="9a37a-111">`first value`：*任何受支持的数据类型*</span><span class="sxs-lookup"><span data-stu-id="9a37a-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="9a37a-112">满足条件时返回的结果。</span><span class="sxs-lookup"><span data-stu-id="9a37a-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="9a37a-113">`second value`：*任何受支持的数据类型*</span><span class="sxs-lookup"><span data-stu-id="9a37a-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="9a37a-114">不满足条件时返回的结果。</span><span class="sxs-lookup"><span data-stu-id="9a37a-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="9a37a-115">返回值</span><span class="sxs-lookup"><span data-stu-id="9a37a-115">Return values</span></span>

<span data-ttu-id="9a37a-116">*任何受支持的数据类型*</span><span class="sxs-lookup"><span data-stu-id="9a37a-116">*Any of the supported data types*</span></span>

<span data-ttu-id="9a37a-117">生成的任何受支持数据类型的值。</span><span class="sxs-lookup"><span data-stu-id="9a37a-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9a37a-118">使用说明</span><span class="sxs-lookup"><span data-stu-id="9a37a-118">Usage notes</span></span>

<span data-ttu-id="9a37a-119">必须使用相同的数据类型指定 `first value` 和 `second value` 参数。</span><span class="sxs-lookup"><span data-stu-id="9a37a-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="9a37a-120">如果配置值的数据类型不匹配，则会在设计时引发异常。</span><span class="sxs-lookup"><span data-stu-id="9a37a-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="9a37a-121">如果第一个值与第二个值是*容器（记录）* 或*记录列表*数据类型的值，结果只包含两个值中都存在的字段。</span><span class="sxs-lookup"><span data-stu-id="9a37a-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="9a37a-122">示例</span><span class="sxs-lookup"><span data-stu-id="9a37a-122">Example</span></span>

<span data-ttu-id="9a37a-123">`IF (1=2, "condition is met", "condition is not met")` 返回字符串 **"condition is not met"**。</span><span class="sxs-lookup"><span data-stu-id="9a37a-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9a37a-124">其他资源</span><span class="sxs-lookup"><span data-stu-id="9a37a-124">Additional resources</span></span>

[<span data-ttu-id="9a37a-125">逻辑函数</span><span class="sxs-lookup"><span data-stu-id="9a37a-125">Logical functions</span></span>](er-functions-category-logical.md)

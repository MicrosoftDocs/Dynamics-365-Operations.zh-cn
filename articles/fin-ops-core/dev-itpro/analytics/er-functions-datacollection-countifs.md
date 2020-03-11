---
title: COUNTIFS ER 函数
description: 本主题提供有关 COUNTIFS 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 9627c7835c8f3f1b6aedc1f691470dc29a11d6b5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042542"
---
# <span data-ttu-id="95029-103"><a name="COUNTIFS">COUNTIFS ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="95029-103"><a name="COUNTIFS">COUNTIFS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95029-104">`COUNTIFS` 函数返回一个*整数*值，此值表示在格式运行期间使用格式元素生成传出文档时收集的格式元素的数量，此值将满足指定条件。</span><span class="sxs-lookup"><span data-stu-id="95029-104">The `COUNTIFS` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="95029-105">每个条件包含一个键范围和一个键值。</span><span class="sxs-lookup"><span data-stu-id="95029-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="95029-106">语法</span><span class="sxs-lookup"><span data-stu-id="95029-106">Syntax</span></span>

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="95029-107">参数</span><span class="sxs-lookup"><span data-stu-id="95029-107">Arguments</span></span>

<span data-ttu-id="95029-108">`condition 1 range`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="95029-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="95029-109">由在电子申报 (ER) 格式组件的**已收集的数据键名**属性中配置的表达式返回的值。</span><span class="sxs-lookup"><span data-stu-id="95029-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="95029-110">此参数是强制性的。</span><span class="sxs-lookup"><span data-stu-id="95029-110">This argument is mandatory.</span></span>

<span data-ttu-id="95029-111">`condition 1 value`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="95029-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="95029-112">由在 ER 格式组件的**已收集的数据键值**属性中配置的表达式返回的值。</span><span class="sxs-lookup"><span data-stu-id="95029-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="95029-113">此参数是强制性的。</span><span class="sxs-lookup"><span data-stu-id="95029-113">This argument is mandatory.</span></span>

<span data-ttu-id="95029-114">`condition N range`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="95029-114">`condition N range`: *String*</span></span>

<span data-ttu-id="95029-115">由在 ER 格式组件的**已收集的数据键名**属性中配置的表达式返回的值。</span><span class="sxs-lookup"><span data-stu-id="95029-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="95029-116">其他参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="95029-116">These additional arguments are optional.</span></span>

<span data-ttu-id="95029-117">`condition N value`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="95029-117">`condition N value`: *String*</span></span>

<span data-ttu-id="95029-118">由在 ER 格式组件的**已收集的数据键值**属性中配置的表达式返回的值。</span><span class="sxs-lookup"><span data-stu-id="95029-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="95029-119">其他参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="95029-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="95029-120">返回值</span><span class="sxs-lookup"><span data-stu-id="95029-120">Return values</span></span>

<span data-ttu-id="95029-121">*整数*</span><span class="sxs-lookup"><span data-stu-id="95029-121">*Integer*</span></span>

<span data-ttu-id="95029-122">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="95029-122">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="95029-123">使用说明</span><span class="sxs-lookup"><span data-stu-id="95029-123">Usage notes</span></span>

<span data-ttu-id="95029-124">可以为 ER 格式组件（位于**收集输出详细信息**选项已打开的**常见\\文件**组件下）的**序列**组件或 **XML 元素**组件配置**已收集的数据键名**和**已收集的数据键值**属性。</span><span class="sxs-lookup"><span data-stu-id="95029-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="95029-125">在当前的**常见\\文件**组件的**收集输出详细信息**选项关闭时，此函数返回 **0**（零）值。</span><span class="sxs-lookup"><span data-stu-id="95029-125">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="95029-126">在 `condition range` 参数中，通配符 **"\*"** 可用于表示多个字符。</span><span class="sxs-lookup"><span data-stu-id="95029-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="95029-127">在 `condition value` 参数中，通配符 **"\*"** 可用于表示多个字符。</span><span class="sxs-lookup"><span data-stu-id="95029-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="95029-128">示例</span><span class="sxs-lookup"><span data-stu-id="95029-128">Example</span></span>

<span data-ttu-id="95029-129">有关如何使用此函数的详细信息，请参阅[盘点和合计格式输出的 ER 使用数据](tasks/er-format-counting-summing-1.md)任务指南，这是**购置/开发 IT 服务/解决方案组件**业务流程的一部分。</span><span class="sxs-lookup"><span data-stu-id="95029-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95029-130">其他资源</span><span class="sxs-lookup"><span data-stu-id="95029-130">Additional resources</span></span>

[<span data-ttu-id="95029-131">数据收集功能</span><span class="sxs-lookup"><span data-stu-id="95029-131">Data collection functions</span></span>](er-functions-category-data-collection.md)

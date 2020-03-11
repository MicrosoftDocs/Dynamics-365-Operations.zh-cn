---
title: COUNTIF ER 函数
description: 本主题提供有关 COUNTIF 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 188f79e10610f8cb5281cfee351ab0eef48dccd2
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042565"
---
# <span data-ttu-id="ec065-103"><a name="COUNTIF">COUNTIF ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="ec065-103"><a name="COUNTIF">COUNTIF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec065-104">`COUNTIF` 函数返回一个*整数*值，此值表示在格式运行期间使用格式元素生成传出文档时收集的格式元素的数量，此值将满足指定条件。</span><span class="sxs-lookup"><span data-stu-id="ec065-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="ec065-105">条件包含一个键范围和一个键值。</span><span class="sxs-lookup"><span data-stu-id="ec065-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec065-106">语法</span><span class="sxs-lookup"><span data-stu-id="ec065-106">Syntax</span></span>

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="ec065-107">参数</span><span class="sxs-lookup"><span data-stu-id="ec065-107">Arguments</span></span>

<span data-ttu-id="ec065-108">`condition range`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="ec065-108">`condition range`: *String*</span></span>

<span data-ttu-id="ec065-109">由在电子申报 (ER) 格式组件的**已收集的数据键名**属性中配置的表达式返回的值。</span><span class="sxs-lookup"><span data-stu-id="ec065-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="ec065-110">`condition value`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="ec065-110">`condition value`: *String*</span></span>

<span data-ttu-id="ec065-111">由在 ER 格式组件的**已收集的数据键值**属性中配置的表达式返回的值。</span><span class="sxs-lookup"><span data-stu-id="ec065-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="ec065-112">返回值</span><span class="sxs-lookup"><span data-stu-id="ec065-112">Return values</span></span>

<span data-ttu-id="ec065-113">*整数*</span><span class="sxs-lookup"><span data-stu-id="ec065-113">*Integer*</span></span>

<span data-ttu-id="ec065-114">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="ec065-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ec065-115">使用说明</span><span class="sxs-lookup"><span data-stu-id="ec065-115">Usage notes</span></span>

<span data-ttu-id="ec065-116">可以为 ER 格式组件（位于**收集输出详细信息**选项已打开的**常见\\文件**组件下）的**序列**组件或 **XML 元素**组件配置**已收集的数据键名**和**已收集的数据键值**属性。</span><span class="sxs-lookup"><span data-stu-id="ec065-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="ec065-117">在当前的**常见\\文件**组件的**收集输出详细信息**选项关闭时，此函数返回 **0**（零）值。</span><span class="sxs-lookup"><span data-stu-id="ec065-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="ec065-118">在 `condition range` 参数中，通配符 **"\*"** 可用于表示多个字符。</span><span class="sxs-lookup"><span data-stu-id="ec065-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="ec065-119">在 `condition value` 参数中，通配符 **"\*"** 可用于表示多个字符。</span><span class="sxs-lookup"><span data-stu-id="ec065-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="ec065-120">示例</span><span class="sxs-lookup"><span data-stu-id="ec065-120">Example</span></span>

<span data-ttu-id="ec065-121">有关如何使用此函数的详细信息，请参阅[盘点和合计格式输出的 ER 使用数据](tasks/er-format-counting-summing-1.md)任务指南，这是**购置/开发 IT 服务/解决方案组件**业务流程的一部分。</span><span class="sxs-lookup"><span data-stu-id="ec065-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec065-122">其他资源</span><span class="sxs-lookup"><span data-stu-id="ec065-122">Additional resources</span></span>

[<span data-ttu-id="ec065-123">数据收集功能</span><span class="sxs-lookup"><span data-stu-id="ec065-123">Data collection functions</span></span>](er-functions-category-data-collection.md)

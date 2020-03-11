---
title: SUMIF ER 函数
description: 本主题提供有关 SUMIF 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 374569d3bbe59f1b96eee9c789b97b7b2a6004bf
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042473"
---
# <span data-ttu-id="b79fe-103"><a name="SUMIF">SUMIF ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="b79fe-103"><a name="SUMIF">SUMIF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b79fe-104">`SUMIF` 函数返回一个*实数*值，此值表示格式元素的绑定返回的以及在格式运行期间使用格式元素生成传出文档时收集的值的总和，并且满足指定条件。</span><span class="sxs-lookup"><span data-stu-id="b79fe-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="b79fe-105">条件包含一个键范围和一个键值。</span><span class="sxs-lookup"><span data-stu-id="b79fe-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b79fe-106">语法</span><span class="sxs-lookup"><span data-stu-id="b79fe-106">Syntax</span></span>

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="b79fe-107">参数</span><span class="sxs-lookup"><span data-stu-id="b79fe-107">Arguments</span></span>

<span data-ttu-id="b79fe-108">`key name for summing`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="b79fe-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="b79fe-109">由在电子申报 (ER) 格式组件的**已收集的数据键名**属性中配置的表达式返回的值，组件的绑定值必须用于求和。</span><span class="sxs-lookup"><span data-stu-id="b79fe-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="b79fe-110">可以为 ER 格式组件（位于**收集输出详细信息**选项已打开的**常见\\文件**组件下）的**序列**组件或 **XML 元素**组件配置**已收集的数据键值**属性。</span><span class="sxs-lookup"><span data-stu-id="b79fe-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="b79fe-111">返回值</span><span class="sxs-lookup"><span data-stu-id="b79fe-111">Return values</span></span>

<span data-ttu-id="b79fe-112">*实数*</span><span class="sxs-lookup"><span data-stu-id="b79fe-112">*Real*</span></span>

<span data-ttu-id="b79fe-113">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="b79fe-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b79fe-114">使用说明</span><span class="sxs-lookup"><span data-stu-id="b79fe-114">Usage notes</span></span>

<span data-ttu-id="b79fe-115">在当前的**常见\\文件**组件的**收集输出详细信息**选项关闭时，此函数返回 **0**（零）值。</span><span class="sxs-lookup"><span data-stu-id="b79fe-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="b79fe-116">在 `condition range` 参数中，通配符 **"\*"** 可用于表示多个字符。</span><span class="sxs-lookup"><span data-stu-id="b79fe-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="b79fe-117">在 `condition value` 参数中，通配符 **"\*"** 可用于表示多个字符。</span><span class="sxs-lookup"><span data-stu-id="b79fe-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="b79fe-118">示例</span><span class="sxs-lookup"><span data-stu-id="b79fe-118">Example</span></span>

<span data-ttu-id="b79fe-119">有关如何使用此函数的详细信息，请参阅[盘点和合计格式输出的 ER 使用数据](tasks/er-format-counting-summing-1.md)任务指南，这是**购置/开发 IT 服务/解决方案组件**业务流程的一部分。</span><span class="sxs-lookup"><span data-stu-id="b79fe-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b79fe-120">其他资源</span><span class="sxs-lookup"><span data-stu-id="b79fe-120">Additional resources</span></span>

[<span data-ttu-id="b79fe-121">数据收集功能</span><span class="sxs-lookup"><span data-stu-id="b79fe-121">Data collection functions</span></span>](er-functions-category-data-collection.md)

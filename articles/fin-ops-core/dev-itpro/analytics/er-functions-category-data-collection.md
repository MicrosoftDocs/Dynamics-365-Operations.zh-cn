---
title: 数据收集类别的 ER 函数列表
description: 本主题提供有关电子申报 (ER) 支持的数据收集函数的信息。
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 31b5e7b08a3de77d461fff5e42164975e53dfe1e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748055"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="b76c0-103">数据收集类别的 ER 函数列表</span><span class="sxs-lookup"><span data-stu-id="b76c0-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b76c0-104">电子申报 (ER) 数据收集函数用于根据已经以 **文本** 或 **Xml** 格式生成的输出数据，以正在运行的 ER 格式进行计数和求和。</span><span class="sxs-lookup"><span data-stu-id="b76c0-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="b76c0-105">此方法用于帮助提高运行的 ER 格式的性能，以在生成的文档中输入运行总计值，以及其他目的。</span><span class="sxs-lookup"><span data-stu-id="b76c0-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="b76c0-106">本主题提供这些函数的概要。</span><span class="sxs-lookup"><span data-stu-id="b76c0-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="b76c0-107">支持的函数列表</span><span class="sxs-lookup"><span data-stu-id="b76c0-107">List of supported functions</span></span>

| <span data-ttu-id="b76c0-108">职能</span><span class="sxs-lookup"><span data-stu-id="b76c0-108">Function</span></span> | <span data-ttu-id="b76c0-109">说明</span><span class="sxs-lookup"><span data-stu-id="b76c0-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="b76c0-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="b76c0-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="b76c0-111">此函数返回一个 *记录列表* 值，此值包含格式元素的 **已收集的数据键值** 属性返回的以及在格式运行期间使用格式元素生成传出文档时收集的值，并且满足指定条件。</span><span class="sxs-lookup"><span data-stu-id="b76c0-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="b76c0-112">每个条件包含一个键范围和一个键值。</span><span class="sxs-lookup"><span data-stu-id="b76c0-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="b76c0-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="b76c0-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="b76c0-114">此函数返回一个 *整数* 值，此值表示在格式运行期间使用格式元素生成传出文档时收集的格式元素的数量，此值将满足指定条件。</span><span class="sxs-lookup"><span data-stu-id="b76c0-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="b76c0-115">条件包含一个键范围和一个键值。</span><span class="sxs-lookup"><span data-stu-id="b76c0-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="b76c0-116">CountIF</span><span class="sxs-lookup"><span data-stu-id="b76c0-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="b76c0-117">此函数返回一个 *整数* 值，此值表示在格式运行期间使用格式元素生成传出文档时收集的格式元素的数量，此值将满足指定条件。</span><span class="sxs-lookup"><span data-stu-id="b76c0-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="b76c0-118">每个条件包含一个键范围和一个键值。</span><span class="sxs-lookup"><span data-stu-id="b76c0-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="b76c0-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="b76c0-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="b76c0-120">此函数返回一个 *字符串* 值，此值代表当前 (ER) 格式元素的名称。</span><span class="sxs-lookup"><span data-stu-id="b76c0-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="b76c0-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="b76c0-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="b76c0-122">此函数返回一个 *实数* 值，此值表示格式元素的绑定返回的以及在格式运行期间使用格式元素生成传出文档时收集的值的总和，并且满足指定条件。</span><span class="sxs-lookup"><span data-stu-id="b76c0-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="b76c0-123">条件包含一个键范围和一个键值。</span><span class="sxs-lookup"><span data-stu-id="b76c0-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="b76c0-124">SumIF</span><span class="sxs-lookup"><span data-stu-id="b76c0-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="b76c0-125">此函数返回一个 *实数* 值，此值表示格式元素的绑定返回的以及在格式运行期间使用格式元素生成传出文档时收集的值的总和，并且满足指定条件。</span><span class="sxs-lookup"><span data-stu-id="b76c0-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="b76c0-126">每个条件包含一个键范围和一个键值。</span><span class="sxs-lookup"><span data-stu-id="b76c0-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="b76c0-127">其他资源</span><span class="sxs-lookup"><span data-stu-id="b76c0-127">Additional resources</span></span>

[<span data-ttu-id="b76c0-128">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="b76c0-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="b76c0-129">电子报告中的配方设计器</span><span class="sxs-lookup"><span data-stu-id="b76c0-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="b76c0-130">电子申报公式语言</span><span class="sxs-lookup"><span data-stu-id="b76c0-130">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
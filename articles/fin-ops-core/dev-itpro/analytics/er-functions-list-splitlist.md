---
title: SPLITLIST ER 函数
description: 本主题提供有关 SPLITLIST 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 03/15/2021
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
ms.openlocfilehash: 99e199e238b3132622a8b305895637b430e8f6d2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745561"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="a5fd6-103">SPLITLIST ER 函数</span><span class="sxs-lookup"><span data-stu-id="a5fd6-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5fd6-104">`SPLITLIST` 函数将指定的列表拆分为多个子列表（或批次），每个批次包含指定的记录数。</span><span class="sxs-lookup"><span data-stu-id="a5fd6-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="a5fd6-105">然后作为包含批次的新 *记录列表* 值返回结果。</span><span class="sxs-lookup"><span data-stu-id="a5fd6-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="a5fd6-106">语法 1</span><span class="sxs-lookup"><span data-stu-id="a5fd6-106">Syntax 1</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a><span data-ttu-id="a5fd6-107">语法 2</span><span class="sxs-lookup"><span data-stu-id="a5fd6-107">Syntax 2</span></span>

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a><span data-ttu-id="a5fd6-108">参数</span><span class="sxs-lookup"><span data-stu-id="a5fd6-108">Arguments</span></span>

<span data-ttu-id="a5fd6-109">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="a5fd6-109">`list`: *Record list*</span></span>

<span data-ttu-id="a5fd6-110">*记录列表* 数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="a5fd6-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="a5fd6-111">`number`：*整数*</span><span class="sxs-lookup"><span data-stu-id="a5fd6-111">`number`: *Integer*</span></span>

<span data-ttu-id="a5fd6-112">每个批次的最大记录数。</span><span class="sxs-lookup"><span data-stu-id="a5fd6-112">The maximum number of records per batch.</span></span>

<span data-ttu-id="a5fd6-113">`on-demand reading flag`：*布尔值*</span><span class="sxs-lookup"><span data-stu-id="a5fd6-113">`on-demand reading flag`: *Boolean*</span></span>

<span data-ttu-id="a5fd6-114">指定是否应按需生成子列表元素的 *布尔* 值。</span><span class="sxs-lookup"><span data-stu-id="a5fd6-114">A *Boolean* value that specifies whether elements of sublists should be generated on demand.</span></span>

## <a name="return-values"></a><span data-ttu-id="a5fd6-115">返回值</span><span class="sxs-lookup"><span data-stu-id="a5fd6-115">Return values</span></span>

<span data-ttu-id="a5fd6-116">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="a5fd6-116">*Record list*</span></span>

<span data-ttu-id="a5fd6-117">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="a5fd6-117">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a5fd6-118">使用说明</span><span class="sxs-lookup"><span data-stu-id="a5fd6-118">Usage notes</span></span>

<span data-ttu-id="a5fd6-119">返回的批次列表包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="a5fd6-119">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="a5fd6-120">**值：** *列表*</span><span class="sxs-lookup"><span data-stu-id="a5fd6-120">**Value:** *List*</span></span>

    <span data-ttu-id="a5fd6-121">属于当前批次的记录的列表。</span><span class="sxs-lookup"><span data-stu-id="a5fd6-121">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="a5fd6-122">**BatchNumber：** *整数*</span><span class="sxs-lookup"><span data-stu-id="a5fd6-122">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="a5fd6-123">返回列表中当前批次的编号。</span><span class="sxs-lookup"><span data-stu-id="a5fd6-123">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="a5fd6-124">当按需读取标志设置为 **True** 时，根据请求生成子列表，这允许减少内存消耗，但如果不按顺序使用元素，可能导致性能下降。</span><span class="sxs-lookup"><span data-stu-id="a5fd6-124">When the on-demand reading flag is set to **True**, sublists are generated upon request which allows for a reduction in memory consumption but may cause performance degradation if elements aren't used sequentially.</span></span>

## <a name="example"></a><span data-ttu-id="a5fd6-125">示例</span><span class="sxs-lookup"><span data-stu-id="a5fd6-125">Example</span></span>

<span data-ttu-id="a5fd6-126">下图中，将创建一个 **行** 数据源以充当具有三条记录的记录列表。</span><span class="sxs-lookup"><span data-stu-id="a5fd6-126">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="a5fd6-127">此列表分为多个批次，每个批次中最多包含两条记录。</span><span class="sxs-lookup"><span data-stu-id="a5fd6-127">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="a5fd6-128">下图显示设计的格式布局。</span><span class="sxs-lookup"><span data-stu-id="a5fd6-128">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="a5fd6-129">在此格式布局中，创建了与 **行** 数据源的绑定，以便生成 XML 格式的输出。</span><span class="sxs-lookup"><span data-stu-id="a5fd6-129">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="a5fd6-130">此输出为各批次及其中的记录提供单个节点。</span><span class="sxs-lookup"><span data-stu-id="a5fd6-130">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="a5fd6-131">下图显示运行设计的格式的结果。</span><span class="sxs-lookup"><span data-stu-id="a5fd6-131">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="a5fd6-132">其他资源</span><span class="sxs-lookup"><span data-stu-id="a5fd6-132">Additional resources</span></span>

[<span data-ttu-id="a5fd6-133">列表函数</span><span class="sxs-lookup"><span data-stu-id="a5fd6-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

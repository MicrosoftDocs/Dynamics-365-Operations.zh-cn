---
title: SPLITLISTBYLIMIT ER 函数
description: 本主题提供有关 SPLITLISTBYLIMIT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
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
ms.openlocfilehash: eb492560a453ec59bb82d24dd6717f409bd8b257
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745537"
---
# <a name="splitlistbylimit-er-function"></a><span data-ttu-id="53a8e-103">SPLITLISTBYLIMIT ER 函数</span><span class="sxs-lookup"><span data-stu-id="53a8e-103">SPLITLISTBYLIMIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53a8e-104">`SPLITLISTBYLIMIT` 函数将指定列表拆分为新的子列表（批次）列表。</span><span class="sxs-lookup"><span data-stu-id="53a8e-104">The `SPLITLISTBYLIMIT` function splits the specified list into a new list of sublists (batches).</span></span> <span data-ttu-id="53a8e-105">每个批次中的记录数是动态计算的。</span><span class="sxs-lookup"><span data-stu-id="53a8e-105">The number of records in each batch is dynamically calculated.</span></span> <span data-ttu-id="53a8e-106">然后此函数作为包含批次的新 *记录列表* 值返回结果。</span><span class="sxs-lookup"><span data-stu-id="53a8e-106">The function then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="53a8e-107">语法</span><span class="sxs-lookup"><span data-stu-id="53a8e-107">Syntax</span></span>

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a><span data-ttu-id="53a8e-108">参数</span><span class="sxs-lookup"><span data-stu-id="53a8e-108">Arguments</span></span>

<span data-ttu-id="53a8e-109">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="53a8e-109">`list`: *Record list*</span></span>

<span data-ttu-id="53a8e-110">*记录列表* 数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="53a8e-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="53a8e-111">`limit value`：*整数* 或 *实数*</span><span class="sxs-lookup"><span data-stu-id="53a8e-111">`limit value`: *Integer* or *Real*</span></span>

<span data-ttu-id="53a8e-112">用于将原始列表拆分为多个批次的限制的最大值。</span><span class="sxs-lookup"><span data-stu-id="53a8e-112">The maximum value of the limit that is used to split the original list into batches.</span></span>

<span data-ttu-id="53a8e-113">`limit source`：*字段*</span><span class="sxs-lookup"><span data-stu-id="53a8e-113">`limit source`: *Field*</span></span>

<span data-ttu-id="53a8e-114">指定列表中 *整数* 或 *实数* 类型的字段的有效路径。</span><span class="sxs-lookup"><span data-stu-id="53a8e-114">The valid path of a field of the *Integer* or *Real* type in the specified list.</span></span> <span data-ttu-id="53a8e-115">此字段的值定义在总和中增加的步骤。</span><span class="sxs-lookup"><span data-stu-id="53a8e-115">The value of this field defines the step that the total sum is increased on.</span></span>

## <a name="return-values"></a><span data-ttu-id="53a8e-116">返回值</span><span class="sxs-lookup"><span data-stu-id="53a8e-116">Return values</span></span>

<span data-ttu-id="53a8e-117">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="53a8e-117">*Record list*</span></span>

<span data-ttu-id="53a8e-118">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="53a8e-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="53a8e-119">使用说明</span><span class="sxs-lookup"><span data-stu-id="53a8e-119">Usage notes</span></span>

<span data-ttu-id="53a8e-120">返回的批次列表包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="53a8e-120">The list of batches that is returned contains the following elements:</span></span>

- <span data-ttu-id="53a8e-121">**值**：*列表*</span><span class="sxs-lookup"><span data-stu-id="53a8e-121">**Value**: *List*</span></span>

    <span data-ttu-id="53a8e-122">属于当前批次的记录的列表。</span><span class="sxs-lookup"><span data-stu-id="53a8e-122">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="53a8e-123">**BatchNumber**：*整数*</span><span class="sxs-lookup"><span data-stu-id="53a8e-123">**BatchNumber**: *Integer*</span></span>

    <span data-ttu-id="53a8e-124">返回列表中当前批次的编号。</span><span class="sxs-lookup"><span data-stu-id="53a8e-124">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="53a8e-125">如果限值源超过定义的限值时，限值不适用于原始列表的单个项目。</span><span class="sxs-lookup"><span data-stu-id="53a8e-125">The limit isn't applied to a single item of the original list if the limit source exceeds the defined limit.</span></span>

## <a name="example"></a><span data-ttu-id="53a8e-126">示例</span><span class="sxs-lookup"><span data-stu-id="53a8e-126">Example</span></span>

<span data-ttu-id="53a8e-127">下图显示电子申报 (ER) 格式。</span><span class="sxs-lookup"><span data-stu-id="53a8e-127">The following illustration shows an Electronic reporting (ER) format.</span></span>

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

<span data-ttu-id="53a8e-128">下图显示用于该格式的数据源。</span><span class="sxs-lookup"><span data-stu-id="53a8e-128">The following illustration shows the data sources that are used for the format.</span></span>

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

<span data-ttu-id="53a8e-129">下图显示运行该格式的结果。</span><span class="sxs-lookup"><span data-stu-id="53a8e-129">The following illustration shows the result when the format is run.</span></span> <span data-ttu-id="53a8e-130">在此情况下，输出为商品项目的简单列表。</span><span class="sxs-lookup"><span data-stu-id="53a8e-130">In this case, the output is a flat list of commodity items.</span></span>

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

<span data-ttu-id="53a8e-131">在以下图中，调整了同一个格式，以显示单个批次必须包括总重量不应超过限值 9 的商品的批次中的商品物料的列表。</span><span class="sxs-lookup"><span data-stu-id="53a8e-131">In the following illustrations, the same format has been adjusted so that it presents the list of commodity items in batches if a single batch must include commodities and the total weight should not exceed a limit of 9.</span></span>

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

<span data-ttu-id="53a8e-132">下图显示运行调整后的格式的结果。</span><span class="sxs-lookup"><span data-stu-id="53a8e-132">The following illustration shows the result when the adjusted format is run.</span></span>

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> <span data-ttu-id="53a8e-133">此限值不适用于原始列表的最后一个物料，因为其限值源（**重量**）的值 (**11**) 超出定义的限值 (**9**)。</span><span class="sxs-lookup"><span data-stu-id="53a8e-133">The limit isn't applied to the last item of the original list, because the value (**11**) of the limit source (**weight**) exceeds the defined limit (**9**).</span></span> <span data-ttu-id="53a8e-134">要在生成报表期间忽略子列表，请根据需要使用 `WHERE` 函数或相应格式元素的 **Enabled** 表达式。</span><span class="sxs-lookup"><span data-stu-id="53a8e-134">To ignore sublists during report generation, use either the `WHERE` function or the **Enabled** expression of the corresponding format element, as you require.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53a8e-135">其他资源</span><span class="sxs-lookup"><span data-stu-id="53a8e-135">Additional resources</span></span>

[<span data-ttu-id="53a8e-136">列表函数</span><span class="sxs-lookup"><span data-stu-id="53a8e-136">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
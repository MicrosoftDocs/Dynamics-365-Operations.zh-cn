---
title: SPLITLIST ER 函数
description: 本主题提供有关 SPLITLIST 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
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
ms.openlocfilehash: af8c413726ca8d9f92eff18807e7fa9002fc9d37
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559130"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="1a0b7-103">SPLITLIST ER 函数</span><span class="sxs-lookup"><span data-stu-id="1a0b7-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a0b7-104">`SPLITLIST` 函数将指定的列表拆分为多个子列表（或批次），每个批次包含指定的记录数。</span><span class="sxs-lookup"><span data-stu-id="1a0b7-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="1a0b7-105">然后作为包含批次的新 *记录列表* 值返回结果。</span><span class="sxs-lookup"><span data-stu-id="1a0b7-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a0b7-106">语法</span><span class="sxs-lookup"><span data-stu-id="1a0b7-106">Syntax</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="1a0b7-107">参数</span><span class="sxs-lookup"><span data-stu-id="1a0b7-107">Arguments</span></span>

<span data-ttu-id="1a0b7-108">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="1a0b7-108">`list`: *Record list*</span></span>

<span data-ttu-id="1a0b7-109">*记录列表* 数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="1a0b7-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="1a0b7-110">`number`：*整数*</span><span class="sxs-lookup"><span data-stu-id="1a0b7-110">`number`: *Integer*</span></span>

<span data-ttu-id="1a0b7-111">每个批次的最大记录数。</span><span class="sxs-lookup"><span data-stu-id="1a0b7-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="1a0b7-112">返回值</span><span class="sxs-lookup"><span data-stu-id="1a0b7-112">Return values</span></span>

<span data-ttu-id="1a0b7-113">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="1a0b7-113">*Record list*</span></span>

<span data-ttu-id="1a0b7-114">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="1a0b7-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1a0b7-115">使用说明</span><span class="sxs-lookup"><span data-stu-id="1a0b7-115">Usage notes</span></span>

<span data-ttu-id="1a0b7-116">返回的批次列表包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="1a0b7-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="1a0b7-117">**值：** *列表*</span><span class="sxs-lookup"><span data-stu-id="1a0b7-117">**Value:** *List*</span></span>

    <span data-ttu-id="1a0b7-118">属于当前批次的记录的列表。</span><span class="sxs-lookup"><span data-stu-id="1a0b7-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="1a0b7-119">**BatchNumber：** *整数*</span><span class="sxs-lookup"><span data-stu-id="1a0b7-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="1a0b7-120">返回列表中当前批次的编号。</span><span class="sxs-lookup"><span data-stu-id="1a0b7-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="1a0b7-121">示例</span><span class="sxs-lookup"><span data-stu-id="1a0b7-121">Example</span></span>

<span data-ttu-id="1a0b7-122">下图中，将创建一个 **行** 数据源以充当具有三条记录的记录列表。</span><span class="sxs-lookup"><span data-stu-id="1a0b7-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="1a0b7-123">此列表分为多个批次，每个批次中最多包含两条记录。</span><span class="sxs-lookup"><span data-stu-id="1a0b7-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="1a0b7-124">下图显示设计的格式布局。</span><span class="sxs-lookup"><span data-stu-id="1a0b7-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="1a0b7-125">在此格式布局中，创建了与 **行** 数据源的绑定，以便生成 XML 格式的输出。</span><span class="sxs-lookup"><span data-stu-id="1a0b7-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="1a0b7-126">此输出为各批次及其中的记录提供单个节点。</span><span class="sxs-lookup"><span data-stu-id="1a0b7-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="1a0b7-127">下图显示运行设计的格式的结果。</span><span class="sxs-lookup"><span data-stu-id="1a0b7-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="1a0b7-128">其他资源</span><span class="sxs-lookup"><span data-stu-id="1a0b7-128">Additional resources</span></span>

[<span data-ttu-id="1a0b7-129">列表函数</span><span class="sxs-lookup"><span data-stu-id="1a0b7-129">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
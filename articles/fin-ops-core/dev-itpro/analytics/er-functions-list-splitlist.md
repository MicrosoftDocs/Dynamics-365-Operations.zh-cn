---
title: SPLITLIST ER 函数
description: 本主题提供有关 SPLITLIST 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 56ef02e3ea0ca2207ccdc79468a9ea4c1fbe8f95
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041875"
---
# <span data-ttu-id="02c4a-103"><a name="SPLITLIST">SPLITLIST ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="02c4a-103"><a name="SPLITLIST">SPLITLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02c4a-104">`SPLITLIST` 函数将指定的列表拆分为多个子列表（或批次），每个批次包含指定的记录数。</span><span class="sxs-lookup"><span data-stu-id="02c4a-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="02c4a-105">然后作为包含批次的新*记录列表*值返回结果。</span><span class="sxs-lookup"><span data-stu-id="02c4a-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="02c4a-106">语法</span><span class="sxs-lookup"><span data-stu-id="02c4a-106">Syntax</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="02c4a-107">参数</span><span class="sxs-lookup"><span data-stu-id="02c4a-107">Arguments</span></span>

<span data-ttu-id="02c4a-108">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="02c4a-108">`list`: *Record list*</span></span>

<span data-ttu-id="02c4a-109">*记录列表*数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="02c4a-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="02c4a-110">`number`：*整数*</span><span class="sxs-lookup"><span data-stu-id="02c4a-110">`number`: *Integer*</span></span>

<span data-ttu-id="02c4a-111">每个批次的最大记录数。</span><span class="sxs-lookup"><span data-stu-id="02c4a-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="02c4a-112">返回值</span><span class="sxs-lookup"><span data-stu-id="02c4a-112">Return values</span></span>

<span data-ttu-id="02c4a-113">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="02c4a-113">*Record list*</span></span>

<span data-ttu-id="02c4a-114">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="02c4a-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="02c4a-115">使用说明</span><span class="sxs-lookup"><span data-stu-id="02c4a-115">Usage notes</span></span>

<span data-ttu-id="02c4a-116">返回的批次列表包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="02c4a-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="02c4a-117">**值：** *列表*</span><span class="sxs-lookup"><span data-stu-id="02c4a-117">**Value:** *List*</span></span>

    <span data-ttu-id="02c4a-118">属于当前批次的记录的列表。</span><span class="sxs-lookup"><span data-stu-id="02c4a-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="02c4a-119">**BatchNumber：** *整数*</span><span class="sxs-lookup"><span data-stu-id="02c4a-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="02c4a-120">返回列表中当前批次的编号。</span><span class="sxs-lookup"><span data-stu-id="02c4a-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="02c4a-121">示例</span><span class="sxs-lookup"><span data-stu-id="02c4a-121">Example</span></span>

<span data-ttu-id="02c4a-122">下图中，将创建一个**行**数据源以充当具有三条记录的记录列表。</span><span class="sxs-lookup"><span data-stu-id="02c4a-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="02c4a-123">此列表分为多个批次，每个批次中最多包含两条记录。</span><span class="sxs-lookup"><span data-stu-id="02c4a-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="02c4a-124">下图显示设计的格式布局。</span><span class="sxs-lookup"><span data-stu-id="02c4a-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="02c4a-125">在此格式布局中，创建了与**行**数据源的绑定，以便生成 XML 格式的输出。</span><span class="sxs-lookup"><span data-stu-id="02c4a-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="02c4a-126">此输出为各批次及其中的记录提供单个节点。</span><span class="sxs-lookup"><span data-stu-id="02c4a-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="02c4a-127">下图显示运行设计的格式的结果。</span><span class="sxs-lookup"><span data-stu-id="02c4a-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="02c4a-128">其他资源</span><span class="sxs-lookup"><span data-stu-id="02c4a-128">Additional resources</span></span>

[<span data-ttu-id="02c4a-129">列表函数</span><span class="sxs-lookup"><span data-stu-id="02c4a-129">List functions</span></span>](er-functions-category-list.md)

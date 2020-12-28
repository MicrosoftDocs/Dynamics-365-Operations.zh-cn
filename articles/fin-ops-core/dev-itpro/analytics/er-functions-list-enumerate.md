---
title: ENUMERATE ER 函数
description: 本主题提供有关 ENUMERATE 电子申报 (ER) 函数如何使用的信息。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34ebbec94644276be4ef9beb1c77638606dd37a0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679454"
---
# <a name="enumerate-er-function"></a><span data-ttu-id="e121e-103">ENUMERATE ER 函数</span><span class="sxs-lookup"><span data-stu-id="e121e-103">ENUMERATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e121e-104">`ENUMERATE` 函数返回一个新的 *记录列表* 值，此值由指定列表的枚举记录组成。</span><span class="sxs-lookup"><span data-stu-id="e121e-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="e121e-105">语法</span><span class="sxs-lookup"><span data-stu-id="e121e-105">Syntax</span></span>

```vb
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="e121e-106">参数</span><span class="sxs-lookup"><span data-stu-id="e121e-106">Arguments</span></span>

<span data-ttu-id="e121e-107">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="e121e-107">`list`: *Record list*</span></span>

<span data-ttu-id="e121e-108">*记录列表* 数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="e121e-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="e121e-109">返回值</span><span class="sxs-lookup"><span data-stu-id="e121e-109">Return values</span></span>

<span data-ttu-id="e121e-110">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="e121e-110">*Record list*</span></span>

<span data-ttu-id="e121e-111">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="e121e-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e121e-112">使用说明</span><span class="sxs-lookup"><span data-stu-id="e121e-112">Usage notes</span></span>

<span data-ttu-id="e121e-113">返回的枚举记录列表包含以下其他元素：</span><span class="sxs-lookup"><span data-stu-id="e121e-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="e121e-114">字段的记录（**值** 组件）</span><span class="sxs-lookup"><span data-stu-id="e121e-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="e121e-115">当前记录索引（**编号** 组件）</span><span class="sxs-lookup"><span data-stu-id="e121e-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="e121e-116">示例</span><span class="sxs-lookup"><span data-stu-id="e121e-116">Example</span></span>

<span data-ttu-id="e121e-117">在下图中中，**枚举** 数据源创建为引用 VendTable 表的 **供应商** 数据源的供应商记录的枚举列表。</span><span class="sxs-lookup"><span data-stu-id="e121e-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="e121e-118">下图显示电子申报 (ER) 格式。</span><span class="sxs-lookup"><span data-stu-id="e121e-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="e121e-119">在此格式布局中，创建了数据绑定，以便生成 XML 格式的输出。</span><span class="sxs-lookup"><span data-stu-id="e121e-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="e121e-120">此输出将单个供应商表示为枚举的节点。</span><span class="sxs-lookup"><span data-stu-id="e121e-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="e121e-121">下图显示运行设计的格式的结果。</span><span class="sxs-lookup"><span data-stu-id="e121e-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="e121e-122">其他资源</span><span class="sxs-lookup"><span data-stu-id="e121e-122">Additional resources</span></span>

[<span data-ttu-id="e121e-123">列表函数</span><span class="sxs-lookup"><span data-stu-id="e121e-123">List functions</span></span>](er-functions-category-list.md)

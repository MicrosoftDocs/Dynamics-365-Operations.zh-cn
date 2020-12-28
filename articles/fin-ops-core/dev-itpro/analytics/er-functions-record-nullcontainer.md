---
title: NULLCONTAINER ER 函数
description: 本主题提供有关 NULLCONTAINER 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: c1932116b67cef79622f0f6152b168b5961a72c7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683024"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="014c1-103">NULLCONTAINER ER 函数</span><span class="sxs-lookup"><span data-stu-id="014c1-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="014c1-104">`NULLCONTAINER` 函数返回与指定记录列表或记录具有相同结构的空 *容器（记录）* 值。</span><span class="sxs-lookup"><span data-stu-id="014c1-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="014c1-105">语法</span><span class="sxs-lookup"><span data-stu-id="014c1-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="014c1-106">参数</span><span class="sxs-lookup"><span data-stu-id="014c1-106">Arguments</span></span>

<span data-ttu-id="014c1-107">`list`：*记录列表* 或 *容器（记录）*</span><span class="sxs-lookup"><span data-stu-id="014c1-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="014c1-108">*记录列表* 或 *容器（记录）* 类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="014c1-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="014c1-109">返回值</span><span class="sxs-lookup"><span data-stu-id="014c1-109">Return values</span></span>

<span data-ttu-id="014c1-110">*容器（记录）*</span><span class="sxs-lookup"><span data-stu-id="014c1-110">*Container (record)*</span></span>

<span data-ttu-id="014c1-111">生成的记录值。</span><span class="sxs-lookup"><span data-stu-id="014c1-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="014c1-112">使用说明</span><span class="sxs-lookup"><span data-stu-id="014c1-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="014c1-113">此函数已废弃。</span><span class="sxs-lookup"><span data-stu-id="014c1-113">This function is obsolete.</span></span> <span data-ttu-id="014c1-114">请改用 `EMPTYRECORD` 函数。</span><span class="sxs-lookup"><span data-stu-id="014c1-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="014c1-115">有关详细信息，请参阅 [EMPTYRECORD](er-functions-record-emptyrecord.md)。</span><span class="sxs-lookup"><span data-stu-id="014c1-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="014c1-116">示例</span><span class="sxs-lookup"><span data-stu-id="014c1-116">Example</span></span>

<span data-ttu-id="014c1-117">`NULLCONTAINER (SPLIT ("abc", 1))` 返回具有与 `SPLIT` 函数返回的列表相同结构的新空记录。</span><span class="sxs-lookup"><span data-stu-id="014c1-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="014c1-118">有关详细信息，请参阅 [SPLIT](er-functions-list-split.md)。</span><span class="sxs-lookup"><span data-stu-id="014c1-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="014c1-119">其他资源</span><span class="sxs-lookup"><span data-stu-id="014c1-119">Additional resources</span></span>

[<span data-ttu-id="014c1-120">记录函数</span><span class="sxs-lookup"><span data-stu-id="014c1-120">Record functions</span></span>](er-functions-category-record.md)

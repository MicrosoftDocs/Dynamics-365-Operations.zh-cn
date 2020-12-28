---
title: EMPTYRECORD ER 函数
description: 本主题提供有关 EMPTYRECORD 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: d50b31fcbbb99050fca46b0a5ce10cc3fd243691
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684803"
---
# <a name="emptyrecord-er-function"></a><span data-ttu-id="663dd-103">EMPTYRECORD ER 函数</span><span class="sxs-lookup"><span data-stu-id="663dd-103">EMPTYRECORD ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="663dd-104">`EMPTYRECORD` 函数返回与指定记录列表或记录具有相同结构的空 *容器（记录）* 值。</span><span class="sxs-lookup"><span data-stu-id="663dd-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="663dd-105">语法</span><span class="sxs-lookup"><span data-stu-id="663dd-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="663dd-106">参数</span><span class="sxs-lookup"><span data-stu-id="663dd-106">Arguments</span></span>

<span data-ttu-id="663dd-107">`list`：*记录列表* 或 *容器（记录）*</span><span class="sxs-lookup"><span data-stu-id="663dd-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="663dd-108">*记录列表* 或 *容器（记录）* 类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="663dd-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="663dd-109">返回值</span><span class="sxs-lookup"><span data-stu-id="663dd-109">Return values</span></span>

<span data-ttu-id="663dd-110">*容器（记录）*</span><span class="sxs-lookup"><span data-stu-id="663dd-110">*Container (record)*</span></span>

<span data-ttu-id="663dd-111">生成的记录值。</span><span class="sxs-lookup"><span data-stu-id="663dd-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="663dd-112">使用说明</span><span class="sxs-lookup"><span data-stu-id="663dd-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="663dd-113">null 记录为其中的所有字符串都有空值的记录。</span><span class="sxs-lookup"><span data-stu-id="663dd-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="663dd-114">空值对于数字来说为 **0**（零），对于字符串来说为空字符串，依此类推。</span><span class="sxs-lookup"><span data-stu-id="663dd-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="663dd-115">示例</span><span class="sxs-lookup"><span data-stu-id="663dd-115">Example</span></span>

<span data-ttu-id="663dd-116">`EMPTYRECORD (SPLIT ("abc", 1))` 返回具有与 `SPLIT` 函数返回的列表相同结构的新空记录。</span><span class="sxs-lookup"><span data-stu-id="663dd-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="663dd-117">有关详细信息，请参阅 [SPLIT](er-functions-list-split.md)。</span><span class="sxs-lookup"><span data-stu-id="663dd-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="663dd-118">其他资源</span><span class="sxs-lookup"><span data-stu-id="663dd-118">Additional resources</span></span>

[<span data-ttu-id="663dd-119">记录函数</span><span class="sxs-lookup"><span data-stu-id="663dd-119">Record functions</span></span>](er-functions-category-record.md)

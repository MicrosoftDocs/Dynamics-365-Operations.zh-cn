---
title: LISTOFFIRSTITEM ER 函数
description: 本主题提供有关 LISTOFFIRSTITEM 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 069ec0c6d5578ca6ab68814adf325bd79e73b9e8
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745049"
---
# <a name="listoffirstitem-er-function"></a><span data-ttu-id="fe3fe-103">LISTOFFIRSTITEM ER 函数</span><span class="sxs-lookup"><span data-stu-id="fe3fe-103">LISTOFFIRSTITEM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe3fe-104">`LISTOFFIRSTITEM` 函数返回一个*记录列表*值，此值仅包含指定列表的第一条记录。</span><span class="sxs-lookup"><span data-stu-id="fe3fe-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe3fe-105">语法</span><span class="sxs-lookup"><span data-stu-id="fe3fe-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="fe3fe-106">参数</span><span class="sxs-lookup"><span data-stu-id="fe3fe-106">Arguments</span></span>

<span data-ttu-id="fe3fe-107">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="fe3fe-107">`list`: *Record list*</span></span>

<span data-ttu-id="fe3fe-108">*记录列表*数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="fe3fe-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="fe3fe-109">返回值</span><span class="sxs-lookup"><span data-stu-id="fe3fe-109">Return values</span></span>

<span data-ttu-id="fe3fe-110">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="fe3fe-110">*Record list*</span></span>

<span data-ttu-id="fe3fe-111">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="fe3fe-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="fe3fe-112">示例</span><span class="sxs-lookup"><span data-stu-id="fe3fe-112">Example</span></span>

<span data-ttu-id="fe3fe-113">表达式 `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` 返回文本值 **"A"**。</span><span class="sxs-lookup"><span data-stu-id="fe3fe-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe3fe-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="fe3fe-114">Additional resources</span></span>

[<span data-ttu-id="fe3fe-115">列表函数</span><span class="sxs-lookup"><span data-stu-id="fe3fe-115">List functions</span></span>](er-functions-category-list.md)

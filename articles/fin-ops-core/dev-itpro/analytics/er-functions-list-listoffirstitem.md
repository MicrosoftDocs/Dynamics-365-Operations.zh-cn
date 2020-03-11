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
ms.openlocfilehash: 8cd48732280c9af0b89129a32b42285207f97fb7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041967"
---
# <span data-ttu-id="6079a-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="6079a-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6079a-104">`LISTOFFIRSTITEM` 函数返回一个*记录列表*值，此值仅包含指定列表的第一条记录。</span><span class="sxs-lookup"><span data-stu-id="6079a-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="6079a-105">语法</span><span class="sxs-lookup"><span data-stu-id="6079a-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="6079a-106">参数</span><span class="sxs-lookup"><span data-stu-id="6079a-106">Arguments</span></span>

<span data-ttu-id="6079a-107">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="6079a-107">`list`: *Record list*</span></span>

<span data-ttu-id="6079a-108">*记录列表*数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="6079a-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="6079a-109">返回值</span><span class="sxs-lookup"><span data-stu-id="6079a-109">Return values</span></span>

<span data-ttu-id="6079a-110">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="6079a-110">*Record list*</span></span>

<span data-ttu-id="6079a-111">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="6079a-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="6079a-112">示例</span><span class="sxs-lookup"><span data-stu-id="6079a-112">Example</span></span>

<span data-ttu-id="6079a-113">表达式 `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` 返回文本值 **"A"**。</span><span class="sxs-lookup"><span data-stu-id="6079a-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6079a-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="6079a-114">Additional resources</span></span>

[<span data-ttu-id="6079a-115">列表函数</span><span class="sxs-lookup"><span data-stu-id="6079a-115">List functions</span></span>](er-functions-category-list.md)

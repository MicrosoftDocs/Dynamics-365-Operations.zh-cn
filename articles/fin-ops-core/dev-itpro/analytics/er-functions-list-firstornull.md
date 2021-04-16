---
title: FIRSTORNULL ER 函数
description: 本主题说明 FIRSTORNULL 电子申报 (ER) 函数如何使用
author: NickSelin
ms.date: 11/29/2019
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
ms.openlocfilehash: 1ccc094fc468470ffc857c729b6d8402796785d7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753208"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="d0b28-103">FIRSTORNULL ER 函数</span><span class="sxs-lookup"><span data-stu-id="d0b28-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0b28-104">`FIRSTORNULL` 函数返回指定列表的第一条记录为 *容器（记录）* 值（如果该记录不为空）。</span><span class="sxs-lookup"><span data-stu-id="d0b28-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="d0b28-105">如果记录为空，此函数将返回空 *容器（记录）* 值。</span><span class="sxs-lookup"><span data-stu-id="d0b28-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0b28-106">语法</span><span class="sxs-lookup"><span data-stu-id="d0b28-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="d0b28-107">参数</span><span class="sxs-lookup"><span data-stu-id="d0b28-107">Arguments</span></span>

<span data-ttu-id="d0b28-108">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="d0b28-108">`list`: *Record list*</span></span>

<span data-ttu-id="d0b28-109">*记录列表* 数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="d0b28-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d0b28-110">返回值</span><span class="sxs-lookup"><span data-stu-id="d0b28-110">Return values</span></span>

<span data-ttu-id="d0b28-111">*容器（记录）*</span><span class="sxs-lookup"><span data-stu-id="d0b28-111">*Container (record)*</span></span>

<span data-ttu-id="d0b28-112">生成的记录值。</span><span class="sxs-lookup"><span data-stu-id="d0b28-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="d0b28-113">示例</span><span class="sxs-lookup"><span data-stu-id="d0b28-113">Example</span></span>

<span data-ttu-id="d0b28-114">表达式 `FIRSTORNULL(SPLIT("",1)).Value` 返回一个空字符串 (**""**)。</span><span class="sxs-lookup"><span data-stu-id="d0b28-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d0b28-115">其他资源</span><span class="sxs-lookup"><span data-stu-id="d0b28-115">Additional resources</span></span>

[<span data-ttu-id="d0b28-116">列表函数</span><span class="sxs-lookup"><span data-stu-id="d0b28-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
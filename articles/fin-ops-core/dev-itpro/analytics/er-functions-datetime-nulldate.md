---
title: NULLDATE ER 函数
description: 本主题提供有关 NULLDATE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 79d37247653aa297fdee2c770180916b9a9a5fc5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563454"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="b542b-103">NULLDATE ER 函数</span><span class="sxs-lookup"><span data-stu-id="b542b-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b542b-104">`NULLDATE` 函数返回一个表示 **空** 日期（1900 年 1 月 1 日）的 *日期* 值。</span><span class="sxs-lookup"><span data-stu-id="b542b-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="b542b-105">语法</span><span class="sxs-lookup"><span data-stu-id="b542b-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="b542b-106">返回值</span><span class="sxs-lookup"><span data-stu-id="b542b-106">Return values</span></span>

<span data-ttu-id="b542b-107">*日期*</span><span class="sxs-lookup"><span data-stu-id="b542b-107">*Date*</span></span>

<span data-ttu-id="b542b-108">生成的日期值。</span><span class="sxs-lookup"><span data-stu-id="b542b-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="b542b-109">示例 1</span><span class="sxs-lookup"><span data-stu-id="b542b-109">Example 1</span></span>

<span data-ttu-id="b542b-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` 基于指定的自定义格式返回 **空** 日期 1900 年 1 月 1 日为 **"1900-01-01"**。</span><span class="sxs-lookup"><span data-stu-id="b542b-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="b542b-111">示例 2</span><span class="sxs-lookup"><span data-stu-id="b542b-111">Example 2</span></span>

<span data-ttu-id="b542b-112">当 **DocumentDate** 字段的值等于 **空** 日期时，表达式 `IF( Invoice.DocumentDate = NULLDATE(), true, false)` 返回 **True**。</span><span class="sxs-lookup"><span data-stu-id="b542b-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="b542b-113">在此示例中，**Invoice** 为 **Finance/Table 记录** 类型的电子申报 (ER) 数据源，引用 CustInvoiceJour 表。</span><span class="sxs-lookup"><span data-stu-id="b542b-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b542b-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="b542b-114">Additional resources</span></span>

[<span data-ttu-id="b542b-115">日期和时间函数</span><span class="sxs-lookup"><span data-stu-id="b542b-115">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: NULLDATE ER 函数
description: 本主题提供有关 NULLDATE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 7761342c6759c11591e06fc7c32f0ddd8bef407a
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916307"
---
# <span data-ttu-id="6463e-103"><a name="NULLDATE">NULLDATE ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="6463e-103"><a name="NULLDATE">NULLDATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6463e-104">`NULLDATE` 函数返回一个表示**空**日期（1900 年 1 月 1 日）的*日期*值。</span><span class="sxs-lookup"><span data-stu-id="6463e-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="6463e-105">语法</span><span class="sxs-lookup"><span data-stu-id="6463e-105">Syntax</span></span>

```
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="6463e-106">返回值</span><span class="sxs-lookup"><span data-stu-id="6463e-106">Return values</span></span>

<span data-ttu-id="6463e-107">*日期*</span><span class="sxs-lookup"><span data-stu-id="6463e-107">*Date*</span></span>

<span data-ttu-id="6463e-108">生成的日期值。</span><span class="sxs-lookup"><span data-stu-id="6463e-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="6463e-109">示例 1</span><span class="sxs-lookup"><span data-stu-id="6463e-109">Example 1</span></span>

<span data-ttu-id="6463e-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` 基于指定的自定义格式返回**空**日期 1900 年 1 月 1 日为 **"1900-01-01"**。</span><span class="sxs-lookup"><span data-stu-id="6463e-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="6463e-111">示例 2</span><span class="sxs-lookup"><span data-stu-id="6463e-111">Example 2</span></span>

<span data-ttu-id="6463e-112">当 **DocumentDate** 字段的值等于**空**日期时，表达式 `IF( Invoice.DocumentDate = NULLDATE(), true, false)` 返回 **True**。</span><span class="sxs-lookup"><span data-stu-id="6463e-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="6463e-113">在此示例中，**Invoice** 为 **Finance/Table 记录**类型的电子申报 (ER) 数据源，引用 CustInvoiceJour 表。</span><span class="sxs-lookup"><span data-stu-id="6463e-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6463e-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="6463e-114">Additional resources</span></span>

[<span data-ttu-id="6463e-115">日期和时间函数</span><span class="sxs-lookup"><span data-stu-id="6463e-115">Date and time functions</span></span>](er-functions-category-datetime.md)

---
title: DATETODATETIME ER 函数
description: 本主题提供有关 DATETODATETIME 电子申报 (ER) 函数如何使用的信息。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c5ad1d304f0914a9ddbca951cdb7419dbcc1f46
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682431"
---
# <a name="datetodatetime-er-function"></a><span data-ttu-id="a984d-103">DATETODATETIME ER 函数</span><span class="sxs-lookup"><span data-stu-id="a984d-103">DATETODATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a984d-104">`DATETODATETIME` 函数返回一个 *日期时间* 值，此值从给定日期/时间值转换为协调世界时（格林威治标准时间 \[GMT\]）的日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="a984d-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="a984d-105">语法</span><span class="sxs-lookup"><span data-stu-id="a984d-105">Syntax</span></span>

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="a984d-106">参数</span><span class="sxs-lookup"><span data-stu-id="a984d-106">Arguments</span></span>

<span data-ttu-id="a984d-107">`date`：*日期*</span><span class="sxs-lookup"><span data-stu-id="a984d-107">`date`: *Date*</span></span>

<span data-ttu-id="a984d-108">代表要转换的日期的日期值。</span><span class="sxs-lookup"><span data-stu-id="a984d-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="a984d-109">返回值</span><span class="sxs-lookup"><span data-stu-id="a984d-109">Return values</span></span>

<span data-ttu-id="a984d-110">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="a984d-110">*DateTime*</span></span>

<span data-ttu-id="a984d-111">生成的日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="a984d-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="a984d-112">示例 1</span><span class="sxs-lookup"><span data-stu-id="a984d-112">Example 1</span></span>

<span data-ttu-id="a984d-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` 返回当前 Microsoft Dynamics 365 Finance 会话的日期，2015 年 12 月 24 日返回为 **12/24/2015 12:00:00 AM**。</span><span class="sxs-lookup"><span data-stu-id="a984d-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="a984d-114">在此示例中，**CompInfo** 为 **Finance and Operations/Table** 类型，引用 CompanyInfo 表的电子申报 (ER) 数据源。</span><span class="sxs-lookup"><span data-stu-id="a984d-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="a984d-115">示例 2</span><span class="sxs-lookup"><span data-stu-id="a984d-115">Example 2</span></span>

<span data-ttu-id="a984d-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` 返回日期/时间值 **11/12/2019 12:00:00 AM**。</span><span class="sxs-lookup"><span data-stu-id="a984d-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a984d-117">其他资源</span><span class="sxs-lookup"><span data-stu-id="a984d-117">Additional resources</span></span>

[<span data-ttu-id="a984d-118">日期和时间函数</span><span class="sxs-lookup"><span data-stu-id="a984d-118">Date and time functions</span></span>](er-functions-category-datetime.md)

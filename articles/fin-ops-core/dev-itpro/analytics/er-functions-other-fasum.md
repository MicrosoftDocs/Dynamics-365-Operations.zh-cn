---
title: FA_SUM ER 函数
description: 本主题提供有关 FA_SUM 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 03bed091350b39601edb22b5af6bda5a83af47eb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041346"
---
# <span data-ttu-id="ed74f-103"><a name="FA_SUM">FA_SUM ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="ed74f-103"><a name="FA_SUM">FA_SUM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed74f-104">`FA_SUM` 函数返回*容器（记录）* 值，该值由指定固定资产项目的固定资产金额、价值模型代码和日期期限组成。</span><span class="sxs-lookup"><span data-stu-id="ed74f-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed74f-105">语法</span><span class="sxs-lookup"><span data-stu-id="ed74f-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="ed74f-106">参数</span><span class="sxs-lookup"><span data-stu-id="ed74f-106">Arguments</span></span>

<span data-ttu-id="ed74f-107">`fixed asset code`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="ed74f-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="ed74f-108">一个*字符串*值，表示要为其计算余额的固定资产项目的代码。</span><span class="sxs-lookup"><span data-stu-id="ed74f-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="ed74f-109">`value model code`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="ed74f-109">`value model code`: *String*</span></span>

<span data-ttu-id="ed74f-110">一个*字符串*值，表示要为其计算余额的价值模型的代码。</span><span class="sxs-lookup"><span data-stu-id="ed74f-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="ed74f-111">`start date`：*日期*</span><span class="sxs-lookup"><span data-stu-id="ed74f-111">`start date`: *Date*</span></span>

<span data-ttu-id="ed74f-112">表示固定资产金额计算期间的开始日期的*日期*值。</span><span class="sxs-lookup"><span data-stu-id="ed74f-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="ed74f-113">`end date`：*日期*</span><span class="sxs-lookup"><span data-stu-id="ed74f-113">`end date`: *Date*</span></span>

<span data-ttu-id="ed74f-114">表示固定资产金额计算期间的结束日期的*日期*值。</span><span class="sxs-lookup"><span data-stu-id="ed74f-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="ed74f-115">返回值</span><span class="sxs-lookup"><span data-stu-id="ed74f-115">Return values</span></span>

<span data-ttu-id="ed74f-116">*容器（记录）*</span><span class="sxs-lookup"><span data-stu-id="ed74f-116">*Container (record)*</span></span>

<span data-ttu-id="ed74f-117">生成的记录值。</span><span class="sxs-lookup"><span data-stu-id="ed74f-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="ed74f-118">示例</span><span class="sxs-lookup"><span data-stu-id="ed74f-118">Example</span></span>

<span data-ttu-id="ed74f-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` 返回已为 **Current** 价值模型准备的期间为 **Date1** 到 **Date2** 的固定资产 **COMP-000001** 的数据容器。</span><span class="sxs-lookup"><span data-stu-id="ed74f-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ed74f-120">其他资源</span><span class="sxs-lookup"><span data-stu-id="ed74f-120">Additional resources</span></span>

[<span data-ttu-id="ed74f-121">其他（业务域特定的）函数</span><span class="sxs-lookup"><span data-stu-id="ed74f-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

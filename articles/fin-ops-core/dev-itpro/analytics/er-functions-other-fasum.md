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
ms.openlocfilehash: 32eb07689598a3b6c852f272b480106670b88cd0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916974"
---
# <span data-ttu-id="b22fc-103"><a name="FA_SUM">FA_SUM ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="b22fc-103"><a name="FA_SUM">FA_SUM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b22fc-104">`FA_SUM` 函数返回*容器（记录）* 值，该值由指定固定资产项目的固定资产金额、价值模型代码和日期期限组成。</span><span class="sxs-lookup"><span data-stu-id="b22fc-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="b22fc-105">语法</span><span class="sxs-lookup"><span data-stu-id="b22fc-105">Syntax</span></span>

```
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="b22fc-106">参数</span><span class="sxs-lookup"><span data-stu-id="b22fc-106">Arguments</span></span>

<span data-ttu-id="b22fc-107">`fixed asset code`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="b22fc-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="b22fc-108">一个*字符串*值，表示要为其计算余额的固定资产项目的代码。</span><span class="sxs-lookup"><span data-stu-id="b22fc-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="b22fc-109">`value model code`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="b22fc-109">`value model code`: *String*</span></span>

<span data-ttu-id="b22fc-110">一个*字符串*值，表示要为其计算余额的价值模型的代码。</span><span class="sxs-lookup"><span data-stu-id="b22fc-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="b22fc-111">`start date`：*日期*</span><span class="sxs-lookup"><span data-stu-id="b22fc-111">`start date`: *Date*</span></span>

<span data-ttu-id="b22fc-112">表示固定资产金额计算期间的开始日期的*日期*值。</span><span class="sxs-lookup"><span data-stu-id="b22fc-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="b22fc-113">`end date`：*日期*</span><span class="sxs-lookup"><span data-stu-id="b22fc-113">`end date`: *Date*</span></span>

<span data-ttu-id="b22fc-114">表示固定资产金额计算期间的结束日期的*日期*值。</span><span class="sxs-lookup"><span data-stu-id="b22fc-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="b22fc-115">返回值</span><span class="sxs-lookup"><span data-stu-id="b22fc-115">Return values</span></span>

<span data-ttu-id="b22fc-116">*容器（记录）*</span><span class="sxs-lookup"><span data-stu-id="b22fc-116">*Container (record)*</span></span>

<span data-ttu-id="b22fc-117">生成的记录值。</span><span class="sxs-lookup"><span data-stu-id="b22fc-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="b22fc-118">示例</span><span class="sxs-lookup"><span data-stu-id="b22fc-118">Example</span></span>

<span data-ttu-id="b22fc-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` 返回已为 **Current** 价值模型准备的期间为 **Date1** 到 **Date2** 的固定资产 **COMP-000001** 的数据容器。</span><span class="sxs-lookup"><span data-stu-id="b22fc-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b22fc-120">其他资源</span><span class="sxs-lookup"><span data-stu-id="b22fc-120">Additional resources</span></span>

[<span data-ttu-id="b22fc-121">其他（业务域特定的）函数</span><span class="sxs-lookup"><span data-stu-id="b22fc-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

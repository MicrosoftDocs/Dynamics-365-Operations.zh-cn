---
title: FA_BALANCE ER 函数
description: 本主题提供有关 FA_BALANCE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: ec78b9c5bf800503023315eb893076486b0a1fb0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744311"
---
# <a name="fa_balance-er-function"></a><span data-ttu-id="99f5c-103">FA_BALANCE ER 函数</span><span class="sxs-lookup"><span data-stu-id="99f5c-103">FA_BALANCE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99f5c-104">`FA_BALANCE` 函数返回 *容器（记录）* 值，该值由指定固定资产项目的固定资产余额、价值模型代码、报告年度和报告日期数据组成。</span><span class="sxs-lookup"><span data-stu-id="99f5c-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="99f5c-105">语法</span><span class="sxs-lookup"><span data-stu-id="99f5c-105">Syntax</span></span>

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="99f5c-106">参数</span><span class="sxs-lookup"><span data-stu-id="99f5c-106">Arguments</span></span>

<span data-ttu-id="99f5c-107">`fixed asset code`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="99f5c-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="99f5c-108">一个 *字符串* 值，表示要为其计算余额的固定资产项目的代码。</span><span class="sxs-lookup"><span data-stu-id="99f5c-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="99f5c-109">`value model code`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="99f5c-109">`value model code`: *String*</span></span>

<span data-ttu-id="99f5c-110">一个 *字符串* 值，表示要为其计算余额的价值模型的代码。</span><span class="sxs-lookup"><span data-stu-id="99f5c-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="99f5c-111">`reporting year`：*枚举值*</span><span class="sxs-lookup"><span data-stu-id="99f5c-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="99f5c-112">定义余额计算期间的 **AssetYear** 应用程序枚举的枚举值。</span><span class="sxs-lookup"><span data-stu-id="99f5c-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="99f5c-113">`reporting date`：*日期*</span><span class="sxs-lookup"><span data-stu-id="99f5c-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="99f5c-114">定义余额计算日期的 *日期* 值。</span><span class="sxs-lookup"><span data-stu-id="99f5c-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="99f5c-115">返回值</span><span class="sxs-lookup"><span data-stu-id="99f5c-115">Return values</span></span>

<span data-ttu-id="99f5c-116">*容器（记录）*</span><span class="sxs-lookup"><span data-stu-id="99f5c-116">*Container (record)*</span></span>

<span data-ttu-id="99f5c-117">生成的记录值。</span><span class="sxs-lookup"><span data-stu-id="99f5c-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="99f5c-118">示例</span><span class="sxs-lookup"><span data-stu-id="99f5c-118">Example</span></span>

<span data-ttu-id="99f5c-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` 返回已在当前应用程序会话日期为价值模型 **Current** 准备的固定资产 **COMP-000001** 的余额的数据容器。</span><span class="sxs-lookup"><span data-stu-id="99f5c-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="99f5c-120">其他资源</span><span class="sxs-lookup"><span data-stu-id="99f5c-120">Additional resources</span></span>

[<span data-ttu-id="99f5c-121">其他（业务域特定的）函数</span><span class="sxs-lookup"><span data-stu-id="99f5c-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
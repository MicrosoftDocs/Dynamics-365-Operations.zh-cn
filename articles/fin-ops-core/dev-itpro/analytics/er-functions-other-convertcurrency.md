---
title: CONVERTCURRENCY ER 函数
description: 本主题提供有关 CONVERTCURRENCY 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 0f0d5bace9b62cf6f0d7576744a6cc271666bf73
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567632"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="83f2a-103">CONVERTCURRENCY ER 函数</span><span class="sxs-lookup"><span data-stu-id="83f2a-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83f2a-104">`CONVERTCURRENCY` 函数返回一个 *实数* 值，该值表示通过使用指定日期的指定公司的设置，将指定的货币金额从指定源币种转换为指定目标币种的结果。</span><span class="sxs-lookup"><span data-stu-id="83f2a-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="83f2a-105">语法</span><span class="sxs-lookup"><span data-stu-id="83f2a-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="83f2a-106">参数</span><span class="sxs-lookup"><span data-stu-id="83f2a-106">Arguments</span></span>

<span data-ttu-id="83f2a-107">`amount`：*整数* 或 *实数*</span><span class="sxs-lookup"><span data-stu-id="83f2a-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="83f2a-108">表示必须转换的货币金额的数字值。</span><span class="sxs-lookup"><span data-stu-id="83f2a-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="83f2a-109">`source currency`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="83f2a-109">`source currency`: *String*</span></span>

<span data-ttu-id="83f2a-110">源币种的代码。</span><span class="sxs-lookup"><span data-stu-id="83f2a-110">The code of the source currency.</span></span>

<span data-ttu-id="83f2a-111">`target currency`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="83f2a-111">`target currency`: *String*</span></span>

<span data-ttu-id="83f2a-112">目标币种的代码。</span><span class="sxs-lookup"><span data-stu-id="83f2a-112">The code of the target currency.</span></span>

<span data-ttu-id="83f2a-113">`date`：*日期*</span><span class="sxs-lookup"><span data-stu-id="83f2a-113">`date`: *Date*</span></span>

<span data-ttu-id="83f2a-114">代表用于确定转换汇率的日期的 *日期* 值。</span><span class="sxs-lookup"><span data-stu-id="83f2a-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="83f2a-115">`company`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="83f2a-115">`company`: *String*</span></span>

<span data-ttu-id="83f2a-116">表示提供转换所用设置的公司的代码的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="83f2a-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="83f2a-117">返回值</span><span class="sxs-lookup"><span data-stu-id="83f2a-117">Return values</span></span>

<span data-ttu-id="83f2a-118">*实数*</span><span class="sxs-lookup"><span data-stu-id="83f2a-118">*Real*</span></span>

<span data-ttu-id="83f2a-119">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="83f2a-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="83f2a-120">示例</span><span class="sxs-lookup"><span data-stu-id="83f2a-120">Example</span></span>

<span data-ttu-id="83f2a-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` 基于 **DEMF** 公司的设置返回当前会话日期一欧元的等额美元。</span><span class="sxs-lookup"><span data-stu-id="83f2a-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="83f2a-122">其他资源</span><span class="sxs-lookup"><span data-stu-id="83f2a-122">Additional resources</span></span>

[<span data-ttu-id="83f2a-123">其他（业务域特定的）函数</span><span class="sxs-lookup"><span data-stu-id="83f2a-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
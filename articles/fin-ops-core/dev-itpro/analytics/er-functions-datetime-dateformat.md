---
title: DATEFORMAT ER 函数
description: 本主题提供有关 DATEFORMAT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 1fa6bdef2168112aeb17e0edb9f9a6d1b3bd45c0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684923"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="67ead-103">DATEFORMAT ER 函数</span><span class="sxs-lookup"><span data-stu-id="67ead-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67ead-104">`DATEFORMAT` 函数返回一个 *字符串* 值，此值以指定格式和指定的[区域性](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes)（可选）将给定日期值显示为文本。</span><span class="sxs-lookup"><span data-stu-id="67ead-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="67ead-105">有关支持格式的信息，请参阅[标准](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx)和[自定义](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx)。</span><span class="sxs-lookup"><span data-stu-id="67ead-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="67ead-106">语法 1</span><span class="sxs-lookup"><span data-stu-id="67ead-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="67ead-107">语法 2</span><span class="sxs-lookup"><span data-stu-id="67ead-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="67ead-108">参数</span><span class="sxs-lookup"><span data-stu-id="67ead-108">Arguments</span></span>

<span data-ttu-id="67ead-109">`date`：*日期*</span><span class="sxs-lookup"><span data-stu-id="67ead-109">`date`: *Date*</span></span>

<span data-ttu-id="67ead-110">代表要设定格式的日期的日期值。</span><span class="sxs-lookup"><span data-stu-id="67ead-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="67ead-111">`format`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="67ead-111">`format`: *String*</span></span>

<span data-ttu-id="67ead-112">输出字符串的格式。</span><span class="sxs-lookup"><span data-stu-id="67ead-112">The format of the output string.</span></span>

<span data-ttu-id="67ead-113">`culture`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="67ead-113">`culture`: *String*</span></span>

<span data-ttu-id="67ead-114">用于设定格式的区域性。</span><span class="sxs-lookup"><span data-stu-id="67ead-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="67ead-115">返回值</span><span class="sxs-lookup"><span data-stu-id="67ead-115">Return values</span></span>

<span data-ttu-id="67ead-116">*字符串*</span><span class="sxs-lookup"><span data-stu-id="67ead-116">*String*</span></span>

<span data-ttu-id="67ead-117">生成的字符串值。</span><span class="sxs-lookup"><span data-stu-id="67ead-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="67ead-118">使用说明</span><span class="sxs-lookup"><span data-stu-id="67ead-118">Usage notes</span></span>

<span data-ttu-id="67ead-119">当区域性未被定义为被调用函数的参数时，`culture` 由调用上下文定义。</span><span class="sxs-lookup"><span data-stu-id="67ead-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="67ead-120">例如，如果对于配置为使用德国区域性的 **FILE** 元素，以电子申报 (ER) 格式使用语法 1 调用 `DATEFORMAT` 函数，则将使用德国区域性完成转换。</span><span class="sxs-lookup"><span data-stu-id="67ead-120">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="67ead-121">默认 `culture` 值为 **EN-US**。</span><span class="sxs-lookup"><span data-stu-id="67ead-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="67ead-122">示例 1</span><span class="sxs-lookup"><span data-stu-id="67ead-122">Example 1</span></span>

<span data-ttu-id="67ead-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` 根据指定的自定义格式返回当前应用程序服务器日期 2015 年 12 月 24 日为字符串 **"24-12-2015"**。</span><span class="sxs-lookup"><span data-stu-id="67ead-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="67ead-124">示例 2</span><span class="sxs-lookup"><span data-stu-id="67ead-124">Example 2</span></span>

<span data-ttu-id="67ead-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` 根据所选的德国区域性和指定格式，返回当前应用程序会话的日期/时间值 2015 年 12 月 24 日为字符串 **"24-12-2015"**。</span><span class="sxs-lookup"><span data-stu-id="67ead-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string  **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67ead-126">其他资源</span><span class="sxs-lookup"><span data-stu-id="67ead-126">Additional resources</span></span>

[<span data-ttu-id="67ead-127">日期和时间函数</span><span class="sxs-lookup"><span data-stu-id="67ead-127">Date and time functions</span></span>](er-functions-category-datetime.md)

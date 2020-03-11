---
title: DATETIMEFORMAT ER 函数
description: 本主题提供有关 DATETIMEFORMAT 电子申报 (ER) 函数如何使用的信息。
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e550b0c7634c7aac3f8c597a1c1eac3f8125e3b
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070705"
---
# <span data-ttu-id="bd72f-103"><a name="DATETIMEFORMAT">DATETIMEFORMAT ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="bd72f-103"><a name="DATETIMEFORMAT">DATETIMEFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd72f-104">`DATETIMEFORMAT` 函数返回一个*字符串*值，此值以指定格式和指定的[区域性](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes)（可选）将给定日期/时间值显示为文本。</span><span class="sxs-lookup"><span data-stu-id="bd72f-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="bd72f-105">有关支持格式的信息，请参阅[标准](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx)和[自定义](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx)。</span><span class="sxs-lookup"><span data-stu-id="bd72f-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="bd72f-106">语法 1</span><span class="sxs-lookup"><span data-stu-id="bd72f-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="bd72f-107">语法 2</span><span class="sxs-lookup"><span data-stu-id="bd72f-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="bd72f-108">参数</span><span class="sxs-lookup"><span data-stu-id="bd72f-108">Arguments</span></span>

<span data-ttu-id="bd72f-109">`datetime`：*日期时间*</span><span class="sxs-lookup"><span data-stu-id="bd72f-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="bd72f-110">表示要设定格式的日期和时间的日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="bd72f-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="bd72f-111">`format`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="bd72f-111">`format`: *String*</span></span>

<span data-ttu-id="bd72f-112">输出字符串的格式。</span><span class="sxs-lookup"><span data-stu-id="bd72f-112">The format of the output string.</span></span>

<span data-ttu-id="bd72f-113">`culture`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="bd72f-113">`culture`: *String*</span></span>

<span data-ttu-id="bd72f-114">用于设定格式的区域性。</span><span class="sxs-lookup"><span data-stu-id="bd72f-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="bd72f-115">返回值</span><span class="sxs-lookup"><span data-stu-id="bd72f-115">Return values</span></span>

<span data-ttu-id="bd72f-116">*字符串*</span><span class="sxs-lookup"><span data-stu-id="bd72f-116">*String*</span></span>

<span data-ttu-id="bd72f-117">生成的字符串值。</span><span class="sxs-lookup"><span data-stu-id="bd72f-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bd72f-118">使用说明</span><span class="sxs-lookup"><span data-stu-id="bd72f-118">Usage notes</span></span>

<span data-ttu-id="bd72f-119">当区域性未被定义为被调用函数的参数时，`culture` 由调用上下文定义。</span><span class="sxs-lookup"><span data-stu-id="bd72f-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="bd72f-120">例如，如果对于配置为使用德国区域性的 **FILE** 元素，以电子申报 (ER) 格式使用语法 1 调用 `DATETIMEFORMAT` 函数，则将使用德国区域性完成转换。</span><span class="sxs-lookup"><span data-stu-id="bd72f-120">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="bd72f-121">默认 `culture` 值为 **EN-US**。</span><span class="sxs-lookup"><span data-stu-id="bd72f-121">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="bd72f-122">当 `DATETIMEFORMAT` 函数转换给定的日期/时间值时，它将考虑正在运行 ER 格式（调用该函数的上下文的 ER 格式）的应用程序用户的时区设置。</span><span class="sxs-lookup"><span data-stu-id="bd72f-122">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="bd72f-123">示例 1</span><span class="sxs-lookup"><span data-stu-id="bd72f-123">Example 1</span></span>

<span data-ttu-id="bd72f-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` 根据指定的自定义格式返回当前应用程序服务器日期/时间值 2015 年 12 月 24 日为 **"24-12-2015"**。</span><span class="sxs-lookup"><span data-stu-id="bd72f-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="bd72f-125">示例 2</span><span class="sxs-lookup"><span data-stu-id="bd72f-125">Example 2</span></span>

<span data-ttu-id="bd72f-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` 根据所选的德国区域性和指定格式，返回当前应用程序会话的日期/时间值 2015 年 12 月 24 日为 **"24.12.2015"**。</span><span class="sxs-lookup"><span data-stu-id="bd72f-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="bd72f-127">示例 3</span><span class="sxs-lookup"><span data-stu-id="bd72f-127">Example 3</span></span>

<span data-ttu-id="bd72f-128">当由在**语言和国家/地区首选项**部分具有时区值 **(GMT-08:00)太平洋时间(美国和加拿大)** 的应用程序用户启动的流程中调用时，`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` 返回字符串值 **2019-11-12T08:00:00.0000000-08:00**。</span><span class="sxs-lookup"><span data-stu-id="bd72f-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bd72f-129">其他资源</span><span class="sxs-lookup"><span data-stu-id="bd72f-129">Additional resources</span></span>

[<span data-ttu-id="bd72f-130">日期和时间函数</span><span class="sxs-lookup"><span data-stu-id="bd72f-130">Date and time functions</span></span>](er-functions-category-datetime.md)

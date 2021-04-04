---
title: TRIM ER 函数
description: 本主题提供有关 TRIM 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: b671ef72a3558c17fb16db939770394b225656da
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560028"
---
# <a name="trim-er-function"></a><span data-ttu-id="2afec-103">TRIM ER 函数</span><span class="sxs-lookup"><span data-stu-id="2afec-103">TRIM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2afec-104">在删除前导和尾随空格以及删除单词之间的多个空格之后，`TRIM` 函数作为 *字符串* 值返回指定的文本字符串。</span><span class="sxs-lookup"><span data-stu-id="2afec-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2afec-105">语法</span><span class="sxs-lookup"><span data-stu-id="2afec-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="2afec-106">参数</span><span class="sxs-lookup"><span data-stu-id="2afec-106">Arguments</span></span>

<span data-ttu-id="2afec-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="2afec-107">`text`: *String*</span></span>

<span data-ttu-id="2afec-108">*字符串* 类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="2afec-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="2afec-109">返回值</span><span class="sxs-lookup"><span data-stu-id="2afec-109">Return values</span></span>

<span data-ttu-id="2afec-110">*字符串*</span><span class="sxs-lookup"><span data-stu-id="2afec-110">*String*</span></span>

<span data-ttu-id="2afec-111">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="2afec-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="2afec-112">示例</span><span class="sxs-lookup"><span data-stu-id="2afec-112">Example</span></span>

<span data-ttu-id="2afec-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` 返回 **"Sample text"**。</span><span class="sxs-lookup"><span data-stu-id="2afec-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2afec-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="2afec-114">Additional resources</span></span>

[<span data-ttu-id="2afec-115">文本函数</span><span class="sxs-lookup"><span data-stu-id="2afec-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
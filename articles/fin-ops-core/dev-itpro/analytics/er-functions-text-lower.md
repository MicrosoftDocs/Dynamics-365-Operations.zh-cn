---
title: LOWER ER 函数
description: 本主题提供有关 LOWER 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: e684883d4262e4c3cd8a84d0a1c6f1d685bb650b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746283"
---
# <a name="lower-er-function"></a><span data-ttu-id="63149-103">LOWER ER 函数</span><span class="sxs-lookup"><span data-stu-id="63149-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63149-104">在将指定的文本字符串转换为小写字母后，`LOWER` 函数作为 *字符串* 值返回该字符串。</span><span class="sxs-lookup"><span data-stu-id="63149-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="63149-105">语法</span><span class="sxs-lookup"><span data-stu-id="63149-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="63149-106">参数</span><span class="sxs-lookup"><span data-stu-id="63149-106">Arguments</span></span>

<span data-ttu-id="63149-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="63149-107">`text`: *String*</span></span>

<span data-ttu-id="63149-108">指定文本的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="63149-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="63149-109">返回值</span><span class="sxs-lookup"><span data-stu-id="63149-109">Return values</span></span>

<span data-ttu-id="63149-110">*字符串*</span><span class="sxs-lookup"><span data-stu-id="63149-110">*String*</span></span>

<span data-ttu-id="63149-111">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="63149-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="63149-112">示例</span><span class="sxs-lookup"><span data-stu-id="63149-112">Example</span></span>

<span data-ttu-id="63149-113">`LOWER ("Sample")` 返回 **"sample"**。</span><span class="sxs-lookup"><span data-stu-id="63149-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="63149-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="63149-114">Additional resources</span></span>

[<span data-ttu-id="63149-115">文本函数</span><span class="sxs-lookup"><span data-stu-id="63149-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: LEN ER 函数
description: 本主题提供有关 LEN 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
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
ms.openlocfilehash: fce4b5311d84364310b76545a775f1cc8db2fd70
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569960"
---
# <a name="len-er-function"></a><span data-ttu-id="476fd-103">LEN ER 函数</span><span class="sxs-lookup"><span data-stu-id="476fd-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="476fd-104">`LEN` 函数作为 *整数* 值在指定的字符串中返回字符数量。</span><span class="sxs-lookup"><span data-stu-id="476fd-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="476fd-105">语法</span><span class="sxs-lookup"><span data-stu-id="476fd-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="476fd-106">参数</span><span class="sxs-lookup"><span data-stu-id="476fd-106">Arguments</span></span>

<span data-ttu-id="476fd-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="476fd-107">`text`: *String*</span></span>

<span data-ttu-id="476fd-108">指定文本的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="476fd-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="476fd-109">返回值</span><span class="sxs-lookup"><span data-stu-id="476fd-109">Return values</span></span>

<span data-ttu-id="476fd-110">*整数*</span><span class="sxs-lookup"><span data-stu-id="476fd-110">*Integer*</span></span>

<span data-ttu-id="476fd-111">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="476fd-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="476fd-112">示例</span><span class="sxs-lookup"><span data-stu-id="476fd-112">Example</span></span>

<span data-ttu-id="476fd-113">`LEN ("Sample")` 将返回 **6**。</span><span class="sxs-lookup"><span data-stu-id="476fd-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="476fd-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="476fd-114">Additional resources</span></span>

[<span data-ttu-id="476fd-115">文本函数</span><span class="sxs-lookup"><span data-stu-id="476fd-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
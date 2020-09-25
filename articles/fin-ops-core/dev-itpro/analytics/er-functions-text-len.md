---
title: LEN ER 函数
description: 本主题提供有关 LEN 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: e51e181de53cd185679110e99b9f89695bacdf92
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744255"
---
# <a name="len-er-function"></a><span data-ttu-id="18ce7-103">LEN ER 函数</span><span class="sxs-lookup"><span data-stu-id="18ce7-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18ce7-104">`LEN` 函数作为*整数*值在指定的字符串中返回字符数量。</span><span class="sxs-lookup"><span data-stu-id="18ce7-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="18ce7-105">语法</span><span class="sxs-lookup"><span data-stu-id="18ce7-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="18ce7-106">参数</span><span class="sxs-lookup"><span data-stu-id="18ce7-106">Arguments</span></span>

<span data-ttu-id="18ce7-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="18ce7-107">`text`: *String*</span></span>

<span data-ttu-id="18ce7-108">指定文本的*字符串*值。</span><span class="sxs-lookup"><span data-stu-id="18ce7-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="18ce7-109">返回值</span><span class="sxs-lookup"><span data-stu-id="18ce7-109">Return values</span></span>

<span data-ttu-id="18ce7-110">*整数*</span><span class="sxs-lookup"><span data-stu-id="18ce7-110">*Integer*</span></span>

<span data-ttu-id="18ce7-111">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="18ce7-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="18ce7-112">示例</span><span class="sxs-lookup"><span data-stu-id="18ce7-112">Example</span></span>

<span data-ttu-id="18ce7-113">`LEN ("Sample")` 将返回 **6**。</span><span class="sxs-lookup"><span data-stu-id="18ce7-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18ce7-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="18ce7-114">Additional resources</span></span>

[<span data-ttu-id="18ce7-115">文本函数</span><span class="sxs-lookup"><span data-stu-id="18ce7-115">Text functions</span></span>](er-functions-category-text.md)

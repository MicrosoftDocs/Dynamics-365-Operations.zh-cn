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
ms.openlocfilehash: 3e0ba19e762574dde4f9038b87ce352d13f714f4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041047"
---
# <span data-ttu-id="b0ec0-103"><a name="LEN">LEN ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="b0ec0-103"><a name="LEN">LEN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0ec0-104">`LEN` 函数作为*整数*值在指定的字符串中返回字符数量。</span><span class="sxs-lookup"><span data-stu-id="b0ec0-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0ec0-105">语法</span><span class="sxs-lookup"><span data-stu-id="b0ec0-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="b0ec0-106">参数</span><span class="sxs-lookup"><span data-stu-id="b0ec0-106">Arguments</span></span>

<span data-ttu-id="b0ec0-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="b0ec0-107">`text`: *String*</span></span>

<span data-ttu-id="b0ec0-108">指定文本的*字符串*值。</span><span class="sxs-lookup"><span data-stu-id="b0ec0-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="b0ec0-109">返回值</span><span class="sxs-lookup"><span data-stu-id="b0ec0-109">Return values</span></span>

<span data-ttu-id="b0ec0-110">*整数*</span><span class="sxs-lookup"><span data-stu-id="b0ec0-110">*Integer*</span></span>

<span data-ttu-id="b0ec0-111">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="b0ec0-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="b0ec0-112">示例</span><span class="sxs-lookup"><span data-stu-id="b0ec0-112">Example</span></span>

<span data-ttu-id="b0ec0-113">`LEN ("Sample")` 将返回 **6**。</span><span class="sxs-lookup"><span data-stu-id="b0ec0-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b0ec0-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="b0ec0-114">Additional resources</span></span>

[<span data-ttu-id="b0ec0-115">文本函数</span><span class="sxs-lookup"><span data-stu-id="b0ec0-115">Text functions</span></span>](er-functions-category-text.md)

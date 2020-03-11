---
title: LOWER ER 函数
description: 本主题提供有关 LOWER 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 6784384bac31d8c7cdc9c6f71b7dbab79c15a934
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041093"
---
# <span data-ttu-id="df85e-103"><a name="LOWER">LOWER ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="df85e-103"><a name="LOWER">LOWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df85e-104">在将指定的文本字符串转换为小写字母后，`LOWER` 函数作为*字符串*值返回该字符串。</span><span class="sxs-lookup"><span data-stu-id="df85e-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="df85e-105">语法</span><span class="sxs-lookup"><span data-stu-id="df85e-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="df85e-106">参数</span><span class="sxs-lookup"><span data-stu-id="df85e-106">Arguments</span></span>

<span data-ttu-id="df85e-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="df85e-107">`text`: *String*</span></span>

<span data-ttu-id="df85e-108">指定文本的*字符串*值。</span><span class="sxs-lookup"><span data-stu-id="df85e-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="df85e-109">返回值</span><span class="sxs-lookup"><span data-stu-id="df85e-109">Return values</span></span>

<span data-ttu-id="df85e-110">*字符串*</span><span class="sxs-lookup"><span data-stu-id="df85e-110">*String*</span></span>

<span data-ttu-id="df85e-111">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="df85e-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="df85e-112">示例</span><span class="sxs-lookup"><span data-stu-id="df85e-112">Example</span></span>

<span data-ttu-id="df85e-113">`LOWER ("Sample")` 返回 **"sample"**。</span><span class="sxs-lookup"><span data-stu-id="df85e-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df85e-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="df85e-114">Additional resources</span></span>

[<span data-ttu-id="df85e-115">文本函数</span><span class="sxs-lookup"><span data-stu-id="df85e-115">Text functions</span></span>](er-functions-category-text.md)

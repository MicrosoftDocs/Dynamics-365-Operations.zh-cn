---
title: CHAR ER 函数
description: 本主题提供有关 CHAR 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 7813b0c6002e47aef6a8c119c72728a49584401b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041220"
---
# <span data-ttu-id="d570a-103"><a name="CHAR">CHAR ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="d570a-103"><a name="CHAR">CHAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d570a-104">`CHAR` 函数返一个*字符串*值，该值表示指定 Unicode 数值引用的单个字符。</span><span class="sxs-lookup"><span data-stu-id="d570a-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="d570a-105">语法</span><span class="sxs-lookup"><span data-stu-id="d570a-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="d570a-106">参数</span><span class="sxs-lookup"><span data-stu-id="d570a-106">Arguments</span></span>

<span data-ttu-id="d570a-107">`number`：*整数*</span><span class="sxs-lookup"><span data-stu-id="d570a-107">`number`: *Integer*</span></span>

<span data-ttu-id="d570a-108">与预期的单个字符相对应的数字。</span><span class="sxs-lookup"><span data-stu-id="d570a-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="d570a-109">返回值</span><span class="sxs-lookup"><span data-stu-id="d570a-109">Return values</span></span>

<span data-ttu-id="d570a-110">*字符串*</span><span class="sxs-lookup"><span data-stu-id="d570a-110">*String*</span></span>

<span data-ttu-id="d570a-111">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="d570a-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d570a-112">使用说明</span><span class="sxs-lookup"><span data-stu-id="d570a-112">Usage notes</span></span>

<span data-ttu-id="d570a-113">此函数返回的字符串取决于在父 **FILE** 格式元素中选择的编码。</span><span class="sxs-lookup"><span data-stu-id="d570a-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="d570a-114">有关支持的编码的列表，请参阅[编码类](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx)。</span><span class="sxs-lookup"><span data-stu-id="d570a-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="d570a-115">示例</span><span class="sxs-lookup"><span data-stu-id="d570a-115">Example</span></span>

<span data-ttu-id="d570a-116">`CHAR (255)` 返回 **"ÿ"**。</span><span class="sxs-lookup"><span data-stu-id="d570a-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d570a-117">其他资源</span><span class="sxs-lookup"><span data-stu-id="d570a-117">Additional resources</span></span>

[<span data-ttu-id="d570a-118">文本函数</span><span class="sxs-lookup"><span data-stu-id="d570a-118">Text functions</span></span>](er-functions-category-text.md)

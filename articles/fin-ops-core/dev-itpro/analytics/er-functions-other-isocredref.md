---
title: ISOCREDREF ER 函数
description: 本主题提供有关 ISOCREDREF 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: d6e5d025e7de15c27b19711ea5b597d75bdf3d41
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744087"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="8af83-103">ISOCREDREF ER 函数</span><span class="sxs-lookup"><span data-stu-id="8af83-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8af83-104">`ISOCREDREF` 函数基于指定发票编号的数字和字母符号返回一个*字符串*值，该值表示国际标准化组织 (ISO) 贷方引用。</span><span class="sxs-lookup"><span data-stu-id="8af83-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="8af83-105">语法</span><span class="sxs-lookup"><span data-stu-id="8af83-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="8af83-106">参数</span><span class="sxs-lookup"><span data-stu-id="8af83-106">Arguments</span></span>

<span data-ttu-id="8af83-107">`invoice number digits`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="8af83-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="8af83-108">代表发票编号数字的文本值。</span><span class="sxs-lookup"><span data-stu-id="8af83-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="8af83-109">返回值</span><span class="sxs-lookup"><span data-stu-id="8af83-109">Return values</span></span>

<span data-ttu-id="8af83-110">*字符串*</span><span class="sxs-lookup"><span data-stu-id="8af83-110">*String*</span></span>

<span data-ttu-id="8af83-111">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="8af83-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8af83-112">使用说明</span><span class="sxs-lookup"><span data-stu-id="8af83-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="8af83-113">若要从不是 ISO 兼容的字母表中清除符号，`invoice number digits` 参数必须在传递给此函数前转换。</span><span class="sxs-lookup"><span data-stu-id="8af83-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="8af83-114">示例</span><span class="sxs-lookup"><span data-stu-id="8af83-114">Example</span></span>

<span data-ttu-id="8af83-115">`ISOCredRef ("VEND-200002")` 将返回 **"RF23VEND-200002"**。</span><span class="sxs-lookup"><span data-stu-id="8af83-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8af83-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="8af83-116">Additional resources</span></span>

[<span data-ttu-id="8af83-117">其他（业务域特定的）函数</span><span class="sxs-lookup"><span data-stu-id="8af83-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

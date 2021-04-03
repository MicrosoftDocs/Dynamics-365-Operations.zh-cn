---
title: MOD_97 ER 函数
description: 本主题提供有关 MOD_97 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 618cb2b101dd0b1c91b3b1538ef3f87c21e4a70a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563334"
---
# <a name="mod_97-er-function"></a><span data-ttu-id="7fa97-103">MOD_97 ER 函数</span><span class="sxs-lookup"><span data-stu-id="7fa97-103">MOD_97 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7fa97-104">`MOD_97` 函数基于指定发票编号的数字返回 *字符串* 值，该值作为 MOD97 表达式表示贷方引用。</span><span class="sxs-lookup"><span data-stu-id="7fa97-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fa97-105">语法</span><span class="sxs-lookup"><span data-stu-id="7fa97-105">Syntax</span></span>

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="7fa97-106">参数</span><span class="sxs-lookup"><span data-stu-id="7fa97-106">Arguments</span></span>

<span data-ttu-id="7fa97-107">`invoice number digits`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="7fa97-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="7fa97-108">代表发票编号数字的文本值。</span><span class="sxs-lookup"><span data-stu-id="7fa97-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="7fa97-109">返回值</span><span class="sxs-lookup"><span data-stu-id="7fa97-109">Return values</span></span>

<span data-ttu-id="7fa97-110">*字符串*</span><span class="sxs-lookup"><span data-stu-id="7fa97-110">*String*</span></span>

<span data-ttu-id="7fa97-111">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="7fa97-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="7fa97-112">示例</span><span class="sxs-lookup"><span data-stu-id="7fa97-112">Example</span></span>

<span data-ttu-id="7fa97-113">`MOD_97 ("VEND-200002")` 将返回 **"20000285"**。</span><span class="sxs-lookup"><span data-stu-id="7fa97-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7fa97-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="7fa97-114">Additional resources</span></span>

[<span data-ttu-id="7fa97-115">其他（业务域特定的）函数</span><span class="sxs-lookup"><span data-stu-id="7fa97-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
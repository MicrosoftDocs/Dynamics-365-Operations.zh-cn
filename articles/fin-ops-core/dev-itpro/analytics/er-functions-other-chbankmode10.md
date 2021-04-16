---
title: CH_BANK_MOD_10 ER 函数
description: 本主题提供有关 CH_BANK_MOD_10 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
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
ms.openlocfilehash: 92750ca7e7396077d8c56c3b336f495c228dddce
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744407"
---
# <a name="ch_bank_mod_10-er-function"></a><span data-ttu-id="72ba9-103">CH_BANK_MOD_10 ER 函数</span><span class="sxs-lookup"><span data-stu-id="72ba9-103">CH_BANK_MOD_10 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72ba9-104">`CH_BANK_MOD_10` 函数基于指定发票编号的数字返回 *字符串* 值，该值作为 MOD10 表达式表示贷方引用。</span><span class="sxs-lookup"><span data-stu-id="72ba9-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="72ba9-105">语法</span><span class="sxs-lookup"><span data-stu-id="72ba9-105">Syntax</span></span>

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="72ba9-106">参数</span><span class="sxs-lookup"><span data-stu-id="72ba9-106">Arguments</span></span>

<span data-ttu-id="72ba9-107">`invoice number digits`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="72ba9-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="72ba9-108">代表发票编号数字的文本值。</span><span class="sxs-lookup"><span data-stu-id="72ba9-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="72ba9-109">返回值</span><span class="sxs-lookup"><span data-stu-id="72ba9-109">Return values</span></span>

<span data-ttu-id="72ba9-110">*字符串*</span><span class="sxs-lookup"><span data-stu-id="72ba9-110">*String*</span></span>

<span data-ttu-id="72ba9-111">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="72ba9-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="72ba9-112">示例</span><span class="sxs-lookup"><span data-stu-id="72ba9-112">Example</span></span>

<span data-ttu-id="72ba9-113">`CH_BANK_MOD_10 ("VEND-200002")` 将返回 **3**。</span><span class="sxs-lookup"><span data-stu-id="72ba9-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72ba9-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="72ba9-114">Additional resources</span></span>

[<span data-ttu-id="72ba9-115">其他（业务域特定的）函数</span><span class="sxs-lookup"><span data-stu-id="72ba9-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
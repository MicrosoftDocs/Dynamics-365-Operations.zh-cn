---
title: TABLENAME2ID ER 函数
description: 本主题提供有关 TABLENAME2ID 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 0f94d00d9d40830d895e906ffbaa2a236f1efc43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746547"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="9b49c-103">TABLENAME2ID ER 函数</span><span class="sxs-lookup"><span data-stu-id="9b49c-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b49c-104">`TABLENAME2ID` 函数作为 *整数* 值返回指定表名称的表 ID 的数字表示。</span><span class="sxs-lookup"><span data-stu-id="9b49c-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b49c-105">语法</span><span class="sxs-lookup"><span data-stu-id="9b49c-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="9b49c-106">参数</span><span class="sxs-lookup"><span data-stu-id="9b49c-106">Arguments</span></span>

<span data-ttu-id="9b49c-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="9b49c-107">`text`: *String*</span></span>

<span data-ttu-id="9b49c-108">代表有效表名的文本值。</span><span class="sxs-lookup"><span data-stu-id="9b49c-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="9b49c-109">返回值</span><span class="sxs-lookup"><span data-stu-id="9b49c-109">Return values</span></span>

<span data-ttu-id="9b49c-110">*整数*</span><span class="sxs-lookup"><span data-stu-id="9b49c-110">*Integer*</span></span>

<span data-ttu-id="9b49c-111">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="9b49c-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9b49c-112">使用说明</span><span class="sxs-lookup"><span data-stu-id="9b49c-112">Usage notes</span></span>

<span data-ttu-id="9b49c-113">在 Microsoft Dynamics 365 Finance 的不同实例中，执行此函数可能产生不同的结果，即使使用相同的公司名称。</span><span class="sxs-lookup"><span data-stu-id="9b49c-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="9b49c-114">示例</span><span class="sxs-lookup"><span data-stu-id="9b49c-114">Example</span></span>

<span data-ttu-id="9b49c-115">`TABLENAME2ID ("Intrastat")` 将返回 **1510**。</span><span class="sxs-lookup"><span data-stu-id="9b49c-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b49c-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="9b49c-116">Additional resources</span></span>

[<span data-ttu-id="9b49c-117">其他（业务域特定的）函数</span><span class="sxs-lookup"><span data-stu-id="9b49c-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
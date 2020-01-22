---
title: GETCURRENTCOMPANY ER 函数
description: 本主题提供有关 GETCURRENTCOMPANY 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: a0b4c93a4705cd0e382b9b6c7af1d199beeceabe
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915985"
---
# <span data-ttu-id="06970-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="06970-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06970-104">`GETCURRENTCOMPANY` 函数返回表示用户目前已登录到的法人（公司）的代码的*字符串*值。</span><span class="sxs-lookup"><span data-stu-id="06970-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="06970-105">语法</span><span class="sxs-lookup"><span data-stu-id="06970-105">Syntax</span></span>

```
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="06970-106">返回值</span><span class="sxs-lookup"><span data-stu-id="06970-106">Return values</span></span>

<span data-ttu-id="06970-107">*字符串*</span><span class="sxs-lookup"><span data-stu-id="06970-107">*String*</span></span>

<span data-ttu-id="06970-108">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="06970-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="06970-109">示例</span><span class="sxs-lookup"><span data-stu-id="06970-109">Example</span></span>

<span data-ttu-id="06970-110">`GETCURRENTCOMPANY ()` 为已登录 **Contoso Entertainment System USA** 公司的用户返回 **USMF**。</span><span class="sxs-lookup"><span data-stu-id="06970-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06970-111">其他资源</span><span class="sxs-lookup"><span data-stu-id="06970-111">Additional resources</span></span>

[<span data-ttu-id="06970-112">其他（业务域特定的）函数</span><span class="sxs-lookup"><span data-stu-id="06970-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

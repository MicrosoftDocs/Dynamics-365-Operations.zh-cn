---
title: CN_GBT_ADDITIONALDIMENSIONID ER 函数
description: 本主题提供有关 CN_GBT_ADDITIONALDIMENSIONID 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 2395a1932e543e35ced28a2a6e56ab44835de19a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041530"
---
# <span data-ttu-id="4cbee-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="4cbee-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4cbee-104">`CN_GBT_ADDITIONALDIMENSIONID` 函数返回*字符串*值，该值表示从指定字符串获取的单个财务维度 ID。</span><span class="sxs-lookup"><span data-stu-id="4cbee-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="4cbee-105">指定的字符串将所有维度显示为逗号分隔的 ID 列表。</span><span class="sxs-lookup"><span data-stu-id="4cbee-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cbee-106">语法</span><span class="sxs-lookup"><span data-stu-id="4cbee-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="4cbee-107">参数</span><span class="sxs-lookup"><span data-stu-id="4cbee-107">Arguments</span></span>

<span data-ttu-id="4cbee-108">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="4cbee-108">`text`: *String*</span></span>

<span data-ttu-id="4cbee-109">将所有维度显示为逗号分隔的 ID 列表的*字符串*值。</span><span class="sxs-lookup"><span data-stu-id="4cbee-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="4cbee-110">`number`：整数</span><span class="sxs-lookup"><span data-stu-id="4cbee-110">`number`: Integer</span></span>

<span data-ttu-id="4cbee-111">定义指定字符串中所请求维度的序列代码的*整数*值。</span><span class="sxs-lookup"><span data-stu-id="4cbee-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="4cbee-112">返回值</span><span class="sxs-lookup"><span data-stu-id="4cbee-112">Return values</span></span>

<span data-ttu-id="4cbee-113">*字符串*</span><span class="sxs-lookup"><span data-stu-id="4cbee-113">*String*</span></span>

<span data-ttu-id="4cbee-114">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="4cbee-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="4cbee-115">示例</span><span class="sxs-lookup"><span data-stu-id="4cbee-115">Example</span></span>

<span data-ttu-id="4cbee-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` 返回 **"CC"**。</span><span class="sxs-lookup"><span data-stu-id="4cbee-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4cbee-117">其他资源</span><span class="sxs-lookup"><span data-stu-id="4cbee-117">Additional resources</span></span>

[<span data-ttu-id="4cbee-118">其他（业务域特定的）函数</span><span class="sxs-lookup"><span data-stu-id="4cbee-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

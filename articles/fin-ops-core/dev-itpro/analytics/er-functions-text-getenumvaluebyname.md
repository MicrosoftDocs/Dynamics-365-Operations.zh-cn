---
title: GETENUMVALUEBYNAME ER 函数
description: 本主题提供有关 GETENUMVALUEBYNAME 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 87613978c149b5d41aefc58f9896424229819626
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041152"
---
# <span data-ttu-id="becdd-103"><a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="becdd-103"><a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="becdd-104">`GETENUMVALUEBYNAME` 函数通过使用指定为*字符串*值的枚举名称在指定的枚举数据源中搜索特定的*枚举*值。</span><span class="sxs-lookup"><span data-stu-id="becdd-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="becdd-105">如果找到*枚举*值，函数将返回此值。</span><span class="sxs-lookup"><span data-stu-id="becdd-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="becdd-106">否则，此函数将返回**空**枚举值。</span><span class="sxs-lookup"><span data-stu-id="becdd-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="becdd-107">语法</span><span class="sxs-lookup"><span data-stu-id="becdd-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="becdd-108">参数</span><span class="sxs-lookup"><span data-stu-id="becdd-108">Arguments</span></span>

<span data-ttu-id="becdd-109">`enumeration data source path`：*枚举*</span><span class="sxs-lookup"><span data-stu-id="becdd-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="becdd-110">下列枚举类型之一的数据源的有效路径：</span><span class="sxs-lookup"><span data-stu-id="becdd-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="becdd-111">电子申报 (ER) 模型枚举</span><span class="sxs-lookup"><span data-stu-id="becdd-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="becdd-112">ER 格式枚举</span><span class="sxs-lookup"><span data-stu-id="becdd-112">ER format enumeration</span></span>
- <span data-ttu-id="becdd-113">Microsoft Dynamics 365 Finance 枚举</span><span class="sxs-lookup"><span data-stu-id="becdd-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="becdd-114">`enumeration value text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="becdd-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="becdd-115">代表单个枚举值的名称的字符串值。</span><span class="sxs-lookup"><span data-stu-id="becdd-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="becdd-116">返回值</span><span class="sxs-lookup"><span data-stu-id="becdd-116">Return values</span></span>

<span data-ttu-id="becdd-117">可空*枚举*</span><span class="sxs-lookup"><span data-stu-id="becdd-117">Nullable *Enum*</span></span>

<span data-ttu-id="becdd-118">生成的枚举值。</span><span class="sxs-lookup"><span data-stu-id="becdd-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="becdd-119">使用说明</span><span class="sxs-lookup"><span data-stu-id="becdd-119">Usage notes</span></span>

<span data-ttu-id="becdd-120">如果使用指定为*字符串*值的枚举值的名称未找到*枚举*值，不会引发异常。</span><span class="sxs-lookup"><span data-stu-id="becdd-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example"></a><span data-ttu-id="becdd-121">示例</span><span class="sxs-lookup"><span data-stu-id="becdd-121">Example</span></span>

<span data-ttu-id="becdd-122">在下图中，数据模型中引入了 **ReportDirection** 枚举。</span><span class="sxs-lookup"><span data-stu-id="becdd-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="becdd-123">请注意，为枚举值定义标签。</span><span class="sxs-lookup"><span data-stu-id="becdd-123">Notice that labels are defined for the enumeration values.</span></span>

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="becdd-124">下图显示以下详细信息：</span><span class="sxs-lookup"><span data-stu-id="becdd-124">The following illustration shows these details:</span></span>

- <span data-ttu-id="becdd-125">**$Direction** 数据源在 ER 报表中配置。</span><span class="sxs-lookup"><span data-stu-id="becdd-125">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="becdd-126">此数据源是根据 **ReportDirection** 模型枚举配置的。</span><span class="sxs-lookup"><span data-stu-id="becdd-126">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="becdd-127">`$IsArrivals` 表达式设计为将基于模型枚举的 **$Direction** 数据源用作此函数的参数。</span><span class="sxs-lookup"><span data-stu-id="becdd-127">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="becdd-128">此比较表达式的值为 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="becdd-128">The value of this comparison expression is **TRUE**.</span></span>

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a><span data-ttu-id="becdd-129">其他资源</span><span class="sxs-lookup"><span data-stu-id="becdd-129">Additional resources</span></span>

[<span data-ttu-id="becdd-130">文本函数</span><span class="sxs-lookup"><span data-stu-id="becdd-130">Text functions</span></span>](er-functions-category-text.md)

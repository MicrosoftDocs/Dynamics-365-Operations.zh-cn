---
title: TABLENAME2ID ER 函数
description: 本主题提供有关 TABLENAME2ID 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 77d889f75f38b3c07855a96bf65f1456ac2f42e2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915801"
---
# <span data-ttu-id="8528e-103"><a name="TABLENAME2ID">TABLENAME2ID ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="8528e-103"><a name="TABLENAME2ID">TABLENAME2ID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8528e-104">`TABLENAME2ID` 函数作为*整数*值返回指定表名称的表 ID 的数字表示。</span><span class="sxs-lookup"><span data-stu-id="8528e-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8528e-105">语法</span><span class="sxs-lookup"><span data-stu-id="8528e-105">Syntax</span></span>

```
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="8528e-106">参数</span><span class="sxs-lookup"><span data-stu-id="8528e-106">Arguments</span></span>

<span data-ttu-id="8528e-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="8528e-107">`text`: *String*</span></span>

<span data-ttu-id="8528e-108">代表有效表名的文本值。</span><span class="sxs-lookup"><span data-stu-id="8528e-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="8528e-109">返回值</span><span class="sxs-lookup"><span data-stu-id="8528e-109">Return values</span></span>

<span data-ttu-id="8528e-110">*整数*</span><span class="sxs-lookup"><span data-stu-id="8528e-110">*Integer*</span></span>

<span data-ttu-id="8528e-111">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="8528e-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8528e-112">使用说明</span><span class="sxs-lookup"><span data-stu-id="8528e-112">Usage notes</span></span>

<span data-ttu-id="8528e-113">在 Microsoft Dynamics 365 Finance 的不同实例中，执行此函数可能产生不同的结果，即使使用相同的公司名称。</span><span class="sxs-lookup"><span data-stu-id="8528e-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="8528e-114">示例</span><span class="sxs-lookup"><span data-stu-id="8528e-114">Example</span></span>

<span data-ttu-id="8528e-115">`TABLENAME2ID ("Intrastat")` 将返回 **1510**。</span><span class="sxs-lookup"><span data-stu-id="8528e-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8528e-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="8528e-116">Additional resources</span></span>

[<span data-ttu-id="8528e-117">其他（业务域特定的）函数</span><span class="sxs-lookup"><span data-stu-id="8528e-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

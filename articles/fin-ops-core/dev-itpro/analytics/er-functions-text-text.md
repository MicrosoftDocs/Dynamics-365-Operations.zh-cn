---
title: TEXT ER 函数
description: 本主题提供有关 TEXT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: c26d0c4c8c6290bd2dbb10a288bbd59941a8d98e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915548"
---
# <span data-ttu-id="44705-103"><a name="TEXT">TEXT ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="44705-103"><a name="TEXT">TEXT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44705-104">在将指定的数字转换为根据当前应用程序实例的服务器区域设置设定格式的文本字符串后，`TEXT` 函数将该数字作为*字符串*值返回。</span><span class="sxs-lookup"><span data-stu-id="44705-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="44705-105">语法</span><span class="sxs-lookup"><span data-stu-id="44705-105">Syntax</span></span>

```
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="44705-106">参数</span><span class="sxs-lookup"><span data-stu-id="44705-106">Arguments</span></span>

<span data-ttu-id="44705-107">`number`：*整数*或*实数*</span><span class="sxs-lookup"><span data-stu-id="44705-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="44705-108">必须转换为文本字符串的数字。</span><span class="sxs-lookup"><span data-stu-id="44705-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="44705-109">返回值</span><span class="sxs-lookup"><span data-stu-id="44705-109">Return values</span></span>

<span data-ttu-id="44705-110">*字符串*</span><span class="sxs-lookup"><span data-stu-id="44705-110">*String*</span></span>

<span data-ttu-id="44705-111">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="44705-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="44705-112">使用说明</span><span class="sxs-lookup"><span data-stu-id="44705-112">Usage notes</span></span>

<span data-ttu-id="44705-113">对于*实数*类型的值，字符串转换被限制为两位小数。</span><span class="sxs-lookup"><span data-stu-id="44705-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="44705-114">示例</span><span class="sxs-lookup"><span data-stu-id="44705-114">Example</span></span>

<span data-ttu-id="44705-115">如果将 Microsoft Dynamics 365 Finance 实例的服务器区域定义为 **EN-US**，`TEXT (NOW ())` 将返回当前 Finance 会话日期 2015 年 12 月 17 日为文本字符串 **"12/17/2015 07:59:23 AM"**。</span><span class="sxs-lookup"><span data-stu-id="44705-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="44705-116">`TEXT (1/3)` 将返回 **"0.33"**。</span><span class="sxs-lookup"><span data-stu-id="44705-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="44705-117">其他资源</span><span class="sxs-lookup"><span data-stu-id="44705-117">Additional resources</span></span>

[<span data-ttu-id="44705-118">文本函数</span><span class="sxs-lookup"><span data-stu-id="44705-118">Text functions</span></span>](er-functions-category-text.md)

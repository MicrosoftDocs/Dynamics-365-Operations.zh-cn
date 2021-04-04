---
title: TEXT ER 函数
description: 本主题提供有关 TEXT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 5da7375020be827f432ba97740da37abe48962fc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560053"
---
# <a name="text-er-function"></a><span data-ttu-id="3e046-103">TEXT ER 函数</span><span class="sxs-lookup"><span data-stu-id="3e046-103">TEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e046-104">在将指定的数字转换为根据当前应用程序实例的服务器区域设置设定格式的文本字符串后，`TEXT` 函数将该数字作为 *字符串* 值返回。</span><span class="sxs-lookup"><span data-stu-id="3e046-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e046-105">语法</span><span class="sxs-lookup"><span data-stu-id="3e046-105">Syntax</span></span>

```vb
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="3e046-106">参数</span><span class="sxs-lookup"><span data-stu-id="3e046-106">Arguments</span></span>

<span data-ttu-id="3e046-107">`number`：*整数* 或 *实数*</span><span class="sxs-lookup"><span data-stu-id="3e046-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="3e046-108">必须转换为文本字符串的数字。</span><span class="sxs-lookup"><span data-stu-id="3e046-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="3e046-109">返回值</span><span class="sxs-lookup"><span data-stu-id="3e046-109">Return values</span></span>

<span data-ttu-id="3e046-110">*字符串*</span><span class="sxs-lookup"><span data-stu-id="3e046-110">*String*</span></span>

<span data-ttu-id="3e046-111">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="3e046-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3e046-112">使用说明</span><span class="sxs-lookup"><span data-stu-id="3e046-112">Usage notes</span></span>

<span data-ttu-id="3e046-113">对于 *实数* 类型的值，字符串转换被限制为两位小数。</span><span class="sxs-lookup"><span data-stu-id="3e046-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="3e046-114">示例</span><span class="sxs-lookup"><span data-stu-id="3e046-114">Example</span></span>

<span data-ttu-id="3e046-115">如果将 Microsoft Dynamics 365 Finance 实例的服务器区域定义为 **EN-US**，`TEXT (NOW ())` 将返回当前 Finance 会话日期 2015 年 12 月 17 日为文本字符串 **"12/17/2015 07:59:23 AM"**。</span><span class="sxs-lookup"><span data-stu-id="3e046-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="3e046-116">`TEXT (1/3)` 将返回 **"0.33"**。</span><span class="sxs-lookup"><span data-stu-id="3e046-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e046-117">其他资源</span><span class="sxs-lookup"><span data-stu-id="3e046-117">Additional resources</span></span>

[<span data-ttu-id="3e046-118">文本函数</span><span class="sxs-lookup"><span data-stu-id="3e046-118">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
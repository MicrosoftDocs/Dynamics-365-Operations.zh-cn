---
title: 业务域特定类别的 ER 函数列表
description: 本主题提供有关电子申报 (ER) 支持的业务域特定函数的信息。
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
ms.openlocfilehash: 5a1d9869584d0f98e2ce00b1bca669395b43ca6f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916583"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a><span data-ttu-id="b1fd4-103">业务域特定类别的 ER 函数列表</span><span class="sxs-lookup"><span data-stu-id="b1fd4-103">List of ER functions in the business domain–specific category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1fd4-104">电子申报 (ER) 域特定函数可用于执行特定于 Microsoft Dynamics 365 Finance 实现的计算和数据访问请求。</span><span class="sxs-lookup"><span data-stu-id="b1fd4-104">Electronic reporting (ER) domain-specific functions can be used to perform calculations and data access requests that are specific to the implementation of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="b1fd4-105">本主题提供这些函数的概要。</span><span class="sxs-lookup"><span data-stu-id="b1fd4-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="b1fd4-106">支持的函数列表</span><span class="sxs-lookup"><span data-stu-id="b1fd4-106">List of supported functions</span></span>

| <span data-ttu-id="b1fd4-107">职能</span><span class="sxs-lookup"><span data-stu-id="b1fd4-107">Function</span></span>| <span data-ttu-id="b1fd4-108">说明</span><span class="sxs-lookup"><span data-stu-id="b1fd4-108">Description</span></span> |
|---------|-------------|
| [<span data-ttu-id="b1fd4-109">CH_Bank_Mod_10</span><span class="sxs-lookup"><span data-stu-id="b1fd4-109">CH_Bank_Mod_10</span></span>](er-functions-other-chbankmode10.md) | <span data-ttu-id="b1fd4-110">此函数基于指定发票编号的数字返回*字符串*值，该值作为 MOD10 表达式表示贷方引用。</span><span class="sxs-lookup"><span data-stu-id="b1fd4-110">This function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span> |
| [<span data-ttu-id="b1fd4-111">CN_GBT_AdditionalDimensionID</span><span class="sxs-lookup"><span data-stu-id="b1fd4-111">CN_GBT_AdditionalDimensionID</span></span>](er-functions-other-cngbtadditionaldimensionid.md) | <span data-ttu-id="b1fd4-112">此函数返回*字符串*值，该值表示从指定字符串获取的单个财务维度 ID。</span><span class="sxs-lookup"><span data-stu-id="b1fd4-112">This function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="b1fd4-113">指定的字符串将所有维度显示为逗号分隔的 ID 列表。</span><span class="sxs-lookup"><span data-stu-id="b1fd4-113">The specified string presents all dimensions as a comma-separated list of IDs.</span></span> |
| [<span data-ttu-id="b1fd4-114">ConvertCurrency</span><span class="sxs-lookup"><span data-stu-id="b1fd4-114">ConvertCurrency</span></span>](er-functions-other-convertcurrency.md) | <span data-ttu-id="b1fd4-115">此函数返回一个*实数*值，该值表示通过使用指定日期的指定公司的设置，将指定的货币金额从指定源币种转换为指定目标币种的结果。</span><span class="sxs-lookup"><span data-stu-id="b1fd4-115">This function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span> |
| [<span data-ttu-id="b1fd4-116">CurCredRef</span><span class="sxs-lookup"><span data-stu-id="b1fd4-116">CurCredRef</span></span>](er-functions-other-curcredref.md) | <span data-ttu-id="b1fd4-117">此函数基于指定发票编号的数字返回表示贷方引用的*字符串*值。</span><span class="sxs-lookup"><span data-stu-id="b1fd4-117">This function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span> |
| [<span data-ttu-id="b1fd4-118">FA_Balance</span><span class="sxs-lookup"><span data-stu-id="b1fd4-118">FA_Balance</span></span>](er-functions-other-fabalance.md) | <span data-ttu-id="b1fd4-119">此函数返回*容器（记录）* 值，该值由指定固定资产项目的固定资产余额、价值模型代码、报告年度和报告日期数据组成。</span><span class="sxs-lookup"><span data-stu-id="b1fd4-119">This function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span> |
| [<span data-ttu-id="b1fd4-120">FA_Sum</span><span class="sxs-lookup"><span data-stu-id="b1fd4-120">FA_Sum</span></span>](er-functions-other-fasum.md) | <span data-ttu-id="b1fd4-121">此函数返回*容器（记录）* 值，该值由指定固定资产项目的固定资产金额、价值模型代码和日期期限组成。</span><span class="sxs-lookup"><span data-stu-id="b1fd4-121">This function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span> |
| [<span data-ttu-id="b1fd4-122">GetCurrentCompany</span><span class="sxs-lookup"><span data-stu-id="b1fd4-122">GetCurrentCompany</span></span>](er-functions-other-getcurrentcompany.md) | <span data-ttu-id="b1fd4-123">此函数返回表示用户目前已登录到的法人（公司）的代码的*字符串*值。</span><span class="sxs-lookup"><span data-stu-id="b1fd4-123">This function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span> |
| [<span data-ttu-id="b1fd4-124">ISOCredRef</span><span class="sxs-lookup"><span data-stu-id="b1fd4-124">ISOCredRef</span></span>](er-functions-other-isocredref.md) | <span data-ttu-id="b1fd4-125">此函数基于指定发票编号的数字和字母符号返回一个*字符串*值，该值表示国际标准化组织 (ISO) 贷方引用。</span><span class="sxs-lookup"><span data-stu-id="b1fd4-125">This function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span> |
| [<span data-ttu-id="b1fd4-126">IsValidCharacterISO7064</span><span class="sxs-lookup"><span data-stu-id="b1fd4-126">IsValidCharacterISO7064</span></span>](er-functions-other-isvalidchariso7064.md) | <span data-ttu-id="b1fd4-127">如果指定字符串表示有效的国际银行帐号 (IBAN)，此函数返回*布尔*值 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="b1fd4-127">This function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="b1fd4-128">否则，返回*布尔*值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="b1fd4-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="b1fd4-129">Mod_97</span><span class="sxs-lookup"><span data-stu-id="b1fd4-129">Mod_97</span></span>](er-functions-other-mod97.md) | <span data-ttu-id="b1fd4-130">此函数基于指定发票编号的数字返回*字符串*值，该值作为 MOD97 表达式表示贷方引用。</span><span class="sxs-lookup"><span data-stu-id="b1fd4-130">This function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span> |
| [<span data-ttu-id="b1fd4-131">NumSeqValue</span><span class="sxs-lookup"><span data-stu-id="b1fd4-131">NumSeqValue</span></span>](er-functions-other-numseqvalue.md) | <span data-ttu-id="b1fd4-132">此函数根据指定的编号规则、作用域和作用域 ID 返回一个*字符串*值，该值表示新生成的编号规则值。</span><span class="sxs-lookup"><span data-stu-id="b1fd4-132">This function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="b1fd4-133">作用域 ID 等于运行 ER 格式的上下文提供的公司代码。</span><span class="sxs-lookup"><span data-stu-id="b1fd4-133">The scope ID equals the company code that is supplied by the context that the ER format is run under.</span></span> |
| [<span data-ttu-id="b1fd4-134">RoundAmount</span><span class="sxs-lookup"><span data-stu-id="b1fd4-134">RoundAmount</span></span>](er-functions-other-roundamount.md) | <span data-ttu-id="b1fd4-135">此函数返回一个*实数*值，该值表示根据指定的舍入规则将指定的金额舍入到指定小数位数的结果。</span><span class="sxs-lookup"><span data-stu-id="b1fd4-135">This function returns a *Real* value that represents the result of rounding the specified amount to the specified number of decimal places according to the specified rounding rule.</span></span> |
| [<span data-ttu-id="b1fd4-136">TableName2ID</span><span class="sxs-lookup"><span data-stu-id="b1fd4-136">TableName2ID</span></span>](er-functions-other-tablename2id.md) | <span data-ttu-id="b1fd4-137">此函数作为*整数*值返回指定表名称的表 ID 的数字表示。</span><span class="sxs-lookup"><span data-stu-id="b1fd4-137">This function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="b1fd4-138">其他资源</span><span class="sxs-lookup"><span data-stu-id="b1fd4-138">Additional resources</span></span>

[<span data-ttu-id="b1fd4-139">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="b1fd4-139">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="b1fd4-140">电子报告中的配方设计器</span><span class="sxs-lookup"><span data-stu-id="b1fd4-140">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="b1fd4-141">电子申报公式语言</span><span class="sxs-lookup"><span data-stu-id="b1fd4-141">Electronic reporting formula language</span></span>](er-formula-language.md)

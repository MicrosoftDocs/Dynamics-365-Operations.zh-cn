---
title: 业务域特定类别的 ER 函数列表
description: 本文提供有关电子报告 (ER) 支持的业务域特定函数的信息。
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: d9df826dcc0b672977d4d8af1feb985ab9a0ab7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879940"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a>业务域特定类别的 ER 函数列表

[!include [banner](../includes/banner.md)]

电子报告 (ER) 域特定函数可用于执行特定于 Microsoft Dynamics 365 Finance 实现的计算和数据访问请求。 本文提供这些函数的概要。

## <a name="list-of-supported-functions"></a>支持的函数列表

| 职能| 说明 |
|---------|-------------|
| [CH_Bank_Mod_10](er-functions-other-chbankmode10.md) | 此函数基于指定发票编号的数字返回 *字符串* 值，该值作为 MOD10 表达式表示贷方引用。 |
| [CN_GBT_AdditionalDimensionID](er-functions-other-cngbtadditionaldimensionid.md) | 此函数返回 *字符串* 值，该值表示从指定字符串获取的单个财务维度 ID。 指定的字符串将所有维度显示为逗号分隔的 ID 列表。 |
| [ConvertCurrency](er-functions-other-convertcurrency.md) | 此函数返回一个 *实数* 值，该值表示通过使用指定日期的指定公司的设置，将指定的货币金额从指定源币种转换为指定目标币种的结果。 |
| [CurCredRef](er-functions-other-curcredref.md) | 此函数基于指定发票编号的数字返回表示贷方引用的 *字符串* 值。 |
| [FA_Balance](er-functions-other-fabalance.md) | 此函数返回 *容器（记录）* 值，该值由指定固定资产项目的固定资产余额、价值模型代码、报告年度和报告日期数据组成。 |
| [FA_Sum](er-functions-other-fasum.md) | 此函数返回 *容器（记录）* 值，该值由指定固定资产项目的固定资产金额、价值模型代码和日期期限组成。 |
| [GetCurrentCompany](er-functions-other-getcurrentcompany.md) | 此函数返回表示用户目前已登录到的法人（公司）的代码的 *字符串* 值。 |
| [ISOCredRef](er-functions-other-isocredref.md) | 此函数基于指定发票编号的数字和字母符号返回一个 *字符串* 值，该值表示国际标准化组织 (ISO) 贷方引用。 |
| [IsValidCharacterISO7064](er-functions-other-isvalidchariso7064.md) | 如果指定字符串表示有效的国际银行帐号 (IBAN)，此函数返回 *布尔* 值 **TRUE**。 否则，返回 *布尔* 值 **FALSE**。 |
| [Mod_97](er-functions-other-mod97.md) | 此函数基于指定发票编号的数字返回 *字符串* 值，该值作为 MOD97 表达式表示贷方引用。 |
| [NumSeqValue](er-functions-other-numseqvalue.md) | 此函数根据指定的编号规则、作用域和作用域 ID 返回一个 *字符串* 值，该值表示新生成的编号规则值。 作用域 ID 等于运行 ER 格式的上下文提供的公司代码。 |
| [RoundAmount](er-functions-other-roundamount.md) | 此函数返回一个 *实数* 值，该值表示根据指定的舍入规则将指定的金额舍入到指定小数位数的结果。 |
| [TableName2ID](er-functions-other-tablename2id.md) | 此函数作为 *整数* 值返回指定表名称的表 ID 的数字表示。 |

## <a name="additional-resources"></a>其他资源

[电子申报概览](general-electronic-reporting.md)

[电子报告中的配方设计器](general-electronic-reporting-formula-designer.md)

[电子申报公式语言](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
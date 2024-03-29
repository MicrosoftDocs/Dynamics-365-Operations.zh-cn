---
title: 合并公司中的币种重估
description: 本文描述如何重估合并公司中的币种。
author: aprilolson
ms.date: 10/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: twheeloc
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c05ef0d4d05d5113d3b858dafe49ee9c1c7211d9
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779654"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a>合并公司中的币种重估

[!include [banner](../includes/banner.md)]

将一个记帐币种的数据与另一个记帐币种的数据合并时，如果汇率发生更改，则仍必须运行币种重估，以便准确重估帐户余额。 在最初合并数据时，使用 **币种折算** 选项卡可选择合并过程中用于折算的初始汇率。 在输入新的汇率后（例如，在下一个月），您必须重估帐户余额。 随后，将根据新的汇率和日期更新或有利润或损失。 以下示例说明了该过程中创建的会计条目。

## <a name="company-setup"></a>公司设置
-   **源/运营公司 (USMF)** – 美元 (USD) 用作会计和申报币种。
-   **合并的公司 (CON)** – 欧元 (EUR) 用作会计和申报币种。
    -   **已实现利润** – 会计科目 801500
    -   **已有损失** – 会计科目 801600
    -   **或有利润** – 会计科目 801600
    -   **或有损失** – 会计科目 801400

## <a name="original-transactions"></a>原始交易记录
### <a name="cash-receipt-transactions-in-usmf"></a>USMF 中的现金收据交易记录

| 日期       | 分类帐帐户               | 货币 | 时长 |
|------------|------------------------------|----------|--------|
| 2020 年 10 月 11 日 | 110110 – 现金                | USD      | 500    |
| 2020 年 10 月 11 日 | 130100 – 应收帐款 | USD      | -500   |

## <a name="exchange-rates"></a>汇率

| 原始币种 | 目标币种 | 开始日期 | 汇率 |
|---------------|-------------|------------|---------------|
| EUR           | USD         | 2020 年 10 月 1 日  | 200           |
| EUR           | USD         | 2020 年 11 月 1 日  | 150           |
| EUR           | USD         | 2017 年 12 月 1 日  | 100           |

## <a name="perform-the-consolidation-for-october-2020"></a>执行合并（2020 年 10 月）
### <a name="balances-in-the-consolidation-company"></a>合并公司中的余额

| 分类帐帐户 | 货币 | 金额 | 计算    |
|----------------|----------|--------|----------------|
| 110110         | 欧元      | 250    | 500 美元 × 50%  |
| 130100         | 欧元      | -250   | -500 美元 × 50% |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2020-through-november-30-2020"></a>执行科目的币种重估（2020 年 10 月 1 日 - 2020 年 11 月 30 日）
### <a name="balances-in-the-consolidation-company"></a>合并公司中的余额

| 分类帐帐户 | 货币 | 金额  | 计算                        |
|----------------|----------|---------|------------------------------------|
| 110110         | 欧元      | 333.33  | 原金额为 500 × 66.6667%  |
| 130100         | 欧元      | -333.33 | 原金额为 -500 × 66.6667% |
| 801400         | 欧元      | 83.33   | 333.33 – 250                       |
| 801600         | 欧元      | -83.33  | -333.33 – (-250)                   |

您将看到申报币种金额的其他交易记录。

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2020-through-december-31-2020"></a>执行科目的币种重估（2020 年 10 月 1 日 - 2020 年 12 月 31 日）
### <a name="balances-in-the-consolidation-company"></a>合并公司中的余额

| 分类帐帐户 | 货币 | 金额  | 计算                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         | 欧元      | 500.00  | 原金额为 500 × 1                           |
| 130100         | 欧元      | -500.00 | 原金额为 -500 × 1                          |
| 801400         | 欧元      | 250     | 500 – 333.33 = 166.67 166.67 + 83.33 = 250           |
| 801600         | 欧元      | -250    | -500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

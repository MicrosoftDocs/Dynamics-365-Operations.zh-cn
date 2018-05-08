---
title: "合并公司中的币种重估"
description: "此主题描述如何重估合并公司中的币种。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 27059b0d2a781453a7594bdc430005df6ea5c167
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a>合并公司中的币种重估

[!include [banner](../includes/banner.md)]

将一个记帐币种的数据与另一个记帐币种的数据合并时，如果汇率发生更改，则仍必须运行币种重估，以便准确重估帐户余额。 在最初合并数据时，使用**“币种折算”**选项卡可选择合并过程中用于折算的初始汇率。 在输入新的汇率后（例如，在下一个月），您必须重估帐户余额。 随后，将根据新的汇率和日期更新或有利润或损失。 以下示例说明了该过程中创建的会计条目。

## <a name="company-setup"></a>公司设置
-   **源/运营公司 (USMF)** – 美元 (USD) 用作会计和申报币种。
-   **合并的公司 (CON)** – 欧元 (EUR) 用作会计和申报币种。
    -   **已实现利润** – 会计科目 801500
    -   **已有损失** – 会计科目 801600
    -   **或有利润** – 会计科目 801600
    -   **或有损失** – 会计科目 801400

## <a name="original-transactions"></a>原始交易记录
### <a name="cash-receipt-transactions-in-usmf"></a>USMF 中的现金收据交易记录

| 日期       | 会计科目               | 货币 | 金额 |
|------------|------------------------------|----------|--------|
| 10/11/2015 | 110110 – 现金                | 美元      | 500    |
| 10/11/2015 | 130100 – 应收账款 | 美元      | -500   |

## <a name="exchange-rates"></a>汇率

| 原始币种 | 目标币种 | 开始日期 | 汇率 |
|---------------|-------------|------------|---------------|
| 欧元           | 美元         | 10/1/2015  | 200           |
| 欧元           | 美元         | 11/1/2015  | 150           |
| 欧元           | 美元         | 12/1/2012  | 100           |

## <a name="perform-the-consolidation-for-october-2015"></a>执行合并（2015 年 10 月）
### <a name="balances-in-the-consolidation-company"></a>合并公司中的余额

| 会计科目 | 货币 | 金额 | 计算    |
|----------------|----------|--------|----------------|
| 110110         | 欧元      | 250    | 500 美元 × 50%  |
| 130100         | 欧元      | -250   | -500 美元 × 50% |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a>执行科目的币种重估（2015 年 10 月 1 日 - 2015 年 11 月 30 日）
### <a name="balances-in-the-consolidation-company"></a>合并公司中的余额

| 会计科目 | 货币 | 金额  | 计算                        |
|----------------|----------|---------|------------------------------------|
| 110110         | 欧元      | 333.33  | 原金额为 500 × 66.6667%  |
| 130100         | 欧元      | -333.33 | 原金额为 -500 × 66.6667% |
| 801400         | 欧元      | 83.33   | 333.33 – 250                       |
| 801600         | 欧元      | -83.33  | -333.33 – (-250)                   |

您将看到申报币种金额的其他交易记录。

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a>执行科目的币种重估（2015 年 10 月 1 日 - 2015 年 12 月 31 日）
### <a name="balances-in-the-consolidation-company"></a>合并公司中的余额

| 会计科目 | 货币 | 金额  | 计算                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         | 欧元      | 500.00  | 原金额为 500 × 1                           |
| 130100         | 欧元      | -500.00 | 原金额为 -500 × 1                          |
| 801400         | 欧元      | 250     | 500 – 333.33 = 166.67 166.67 + 83.33 = 250           |
| 801600         | 欧元      | -250    | -500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250 |







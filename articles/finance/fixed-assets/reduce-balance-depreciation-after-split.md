---
title: 减少拆分后的余额折旧
description: 本文描述固定资产中使用减少余额方法拆分资产后用于计算折旧的方法。
author: moaamer
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 539967a9a73da91f6b49c1bb89f404267ae0a804
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883291"
---
# <a name="reduce-balance-depreciation-after-a-split"></a>减少拆分后的余额折旧

[!include [banner](../includes/banner.md)]

本文描述固定资产中使用减少余额方法将资产拆分为另一资产后用于计算折旧的方法。 在资产帐簿中配置的折旧年份是会计年度。 有关详细信息，请参阅[减少余额折旧](reduce-balance-depreciation.md)和[拆分固定资产](tasks/split-fixed-asset.md)。

如果在晚于资产的购置期间的会计期间拆分固定资产，减少的余额折旧将考虑前一年的资产帐面净值 (NBV)。 还将考虑从拆分资产的交易中产生的购置和折旧调整交易。 此行为假定资产在一个会计年度中购置，在下一会计年度中拆分。 拆分后必须为原始资产折旧的金额反映资产拆分之前资产的资产 NBV，以及为拆分过帐的购置和折旧调整交易。

例如，以下条件有效：

- 会计期间为 6 月 30 日至 7 月 1 日。
- 减少的余额百分比为 18％，并于 2019 年 6 月以 10,000 美元的购置价购置了一项资产。
- 第一个会计年度的折旧等于 18,000 美元，每月的折旧等于 150 美元，然后资产折旧到 2019 年 11 月，金额为 738.75 美元。
- 在 2019 年 11 月，此资产的 80％ 被拆分为另一项固定资产。

[![减少拆分后的余额折旧。](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)

原始资产的折旧额为 1,822.25 美元。 该金额等于拆分交易过帐之前的 NBV（9,111.25 美元）加上拆分交易过帐期间产生的购置调整（-8,000 美元），再加上拆分交易期间产生的折旧调整（711 美元）。 因此，第二年的折旧为 (1,822.25×18％) ÷12 = 27.33 美元。

第一年新固定资产的折旧额为 (8,000×18％) ÷12 = 120 美元。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

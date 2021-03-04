---
title: 折旧方法和惯例
description: 本文提供 Microsoft Dynamics 365 Finance 支持的折旧惯例和折旧方法的概览。
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3370db28f551b5ce4a9b49342cb0c0b2f3945c0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440861"
---
# <a name="depreciation-methods-and-conventions"></a>折旧方法和惯例

[!include [banner](../includes/banner.md)]

本文提供支持的折旧惯例和折旧方法的概览。

您可以选择不同的折旧法和惯例。 这些方法的目的是将固定资产的可折旧价值分摊到各会计期间中。 固定资产的可折旧价值是购置价格减去残值（如果有）。 

如果您在使用折旧惯例并且修改某一资产的最后折旧开始日期（将跳过某些折旧），则最后一年的折旧可能高于或低于预期。 按最后折旧开始日期的修改影响的折旧期间的数目，调整折旧。

例如，如果您在超过三年后使用半年折旧惯例，则折旧通常在 3 1/2 年发生。 如果您在这一 3 1/2 年的期间中更改最后折旧开始日期，则折旧的最后一年会移出影响的期间外。 如果您按三个月移动日期，则最后一年将有九个月值得折旧，而正常情况下是有六个月值得折旧。

您可以从以下折旧惯例中进行选择。


-   半年
-   全月
-   季度中间
-   月中间(月的第 1 天)
-   月中间(月的第 15 天)
-   半年(年度开始)
-   半年(下一年)

可以从以下计算方法中进行选择。
-   直线法
-   余额递减法
-   手动
-   系数
-   消耗量法
-   直线法(剩余年限)
-   200% 余额递减法
-   175% 余额递减法
-   150% 余额递减法
-   125% 余额递减法





<a name="additional-resources"></a>其他资源
--------

[固定资产折旧](fixed-asset-depreciation.md)

[直线法使用年限折旧](Straight-line-service-life-depreciation.md)

[余额递减法折旧](reduce-balance-depreciation.md)

[手动折旧](manual-depreciation.md)

[因素/系数折旧](factor-depreciation.md)

[工作量法折旧](consumption-depreciation.md)

[剩余年限法折旧](straight-line-life-remaining-depreciation.md)

[125% 余额递减法](125-percent-reducing-balance-depreciation.md)

[150% 余额递减法](150-percent-reducing-balance-depreciation.md)

[175% 余额递减法](175-percent-reducing-balance-depreciation.md)

[200% 余额递减法](200-percent-reducing-balance-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
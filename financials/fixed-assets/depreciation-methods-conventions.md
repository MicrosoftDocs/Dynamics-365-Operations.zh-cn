---
title: "折旧方法和惯例"
description: "本文提供 Microsoft Dynamics 365 for Operations 支持的折旧惯例和折旧方法的概览。"
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 4b32cd8cbd270424d0790e242d75dc214ffea123
ms.contentlocale: zh-cn
ms.lasthandoff: 04/25/2017


---

# <a name="depreciation-methods-and-conventions"></a>折旧方法和惯例

[!include[banner](../includes/banner.md)]


本文提供 Microsoft Dynamics 365 for Operations 支持的折旧惯例和折旧方法的概览。

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

 



<a name="see-also"></a>请参阅
--------

[固定资产折旧](fixed-asset-depreciation.md)

[直线法折旧](Straight-line-service-life-depreciation.md)

[余额递减法](reduce-balance-depreciation.md)

[手动折旧](manual-depreciation.md)

[因素/系数折旧](factor-depreciation.md)

[工作量法折旧](consumption-depreciation.md)

[剩余年限法折旧](straight-line-life-remaining-depreciation.md)

[125% 余额递减法](125-percent-reducing-balance-depreciation.md)

[150% 余额递减法](150-percent-reducing-balance-depreciation.md)

[175% 余额递减法](175-percent-reducing-balance-depreciation.md)

[200% 余额递减法](200-percent-reducing-balance-depreciation.md)





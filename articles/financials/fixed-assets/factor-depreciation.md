---
title: "因素/系数折旧"
description: "本文提供系数折旧法的概览。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 44fa540c31e5302ccf0a65b44b3c45a4c1e1fd1f
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="factor-depreciation"></a>因素/系数折旧

[!include [banner](../includes/banner.md)]

本文提供系数折旧法的概览。

系数是用于对资产进行折旧的百分比。 在您设置固定资产折旧模板并在**折旧模板**页的**方法**字段中选择**系数**时，可以设置累进、非累进或直线折旧法：

-   在累进折旧法中，折旧金额将增加每个折旧期间。
-   在非累进折旧法中，每个期间的折旧金额将随着时间减少。
-   在直线折旧法中，在每个期间中折旧都相同。

下面的规则和示例指示您如何为每种折旧类型设置系数。 

> [!NOTE] 
> 当您在**方法**字段中选择**系数**时，**系数**字段和**间隔**字段将显示。

## <a name="progressive-depreciation"></a>累进折旧
**系数**字段中的值大于 **50**。

### <a name="example"></a>示例

购置价格为 100,000，系数为 70，使用年限为 10 年，并且折旧在 1 月 1 日开始。 只为使用年限的前 6 年显示折旧金额和帐面净额。

| 年 | 期间      | 折旧金额 | 帐面净值 |
|------|-------------|---------------------|-----------------------|
| 1    | 12 月 31 日 | 307.69              | 99,692.31             |
| 2    | 12 月 31 日 | 1,447.21            | 98,245.10             |
| 3    | 12 月 31 日 | 3,104.50            | 95,140.60             |
| 4    | 12 月 31 日 | 5,150.21            | 89,990.39             |
| 5    | 12 月 31 日 | 7,522.95            | 82,467.44             |
| 6    | 12 月 31 日 | 10,184.06           | 72,283.38             |

## <a name="digressive-depreciation"></a>非累进折旧
**系数**字段中的值小于 **50**。

### <a name="example"></a>示例

购置价格为 100,000，系数为 20，使用年限为 10 年，并且折旧在 1 月 1 日开始。 只为使用年限的前 6 年显示折旧金额和帐面净额。

| 年 | 期间      | 折旧金额 | 帐面净值 |
|------|-------------|---------------------|-----------------------|
| 1    | 12 月 31 日 | 56,080.43           | 43,919.57             |
| 2    | 12 月 31 日 | 10,665.70           | 33,253.87             |
| 3    | 12 月 31 日 | 7,156.22            | 26,097.65             |
| 4    | 12 月 31 日 | 5,538.06            | 20,559.59             |
| 5    | 12 月 31 日 | 4,579.89            | 15,979.70             |
| 6    | 12 月 31 日 | 3,937.36            | 12,042.34             |

## <a name="straight-line-depreciation"></a>直线折旧法
**系数**字段中的值等于 **50**。 在此情况下，折旧在每个期间中都相同，并且您应该考虑在其他字段中指定的值的意义，如[直线法折旧](straight-line-service-life-depreciation.md)中所述。





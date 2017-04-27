---
title: "工作量法折旧"
description: "本文提供消耗量折旧方法的概览。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 7fa432ebfc433b6396589df053b2b485b2ec6dbd
ms.lasthandoff: 03/31/2017


---

# <a name="consumption-depreciation"></a>工作量法折旧

[!include[banner](../includes/banner.md)]


本文提供消耗量折旧方法的概览。

如果您为固定资产设置折旧模板，并在“折旧模板”****页上的“方法”****字段中选择“消耗量”****，则会根据使用率将固定资产分配给折旧模板。 您不必在“折旧模板”****页上设置百分比和时间间隔。 在您创建使用“消耗量”方法的折旧模板后，可以通过多种方式设置折旧方法。

## <a name="set-up-and-use-consumption-depreciation"></a>设置和使用工作量法折旧
1.  在“折旧模板”****页上，创建折旧模板。 对于工作量法计算，折旧模板必须有 ID 和名称，以及必须在“方法”****字段中选择“消耗量”****。
2.  在“消耗系数”****页上，设置消耗系数。 每个消耗系数都必须具有 ID 和名称，以及指定为数量或百分比的消耗系数。
3.  在“工作量单位”****页上，设置工作量单位。 每个消耗单位都必须具有 ID 和名称。 折旧单位用于计算“工作量法折旧”****页上的工作量法折旧。 单位的示例为千米 (km)、千克 (kg) 和小时。
4.  在“固定资产”****页上，设置各个固定资产。 对于每个固定资产，选择具有折旧模板的价值模型和折旧帐簿。 如果您有使用基于“消耗量”方法折旧模版的固定资产，则必须为工作量法折旧设置值模型或折旧帐簿。 此设置是在“价值模型”****页的“折旧”****选项卡或“折旧模板”****的“常规”****快速选项卡上完成的。 您可以将同一价值模型用于多个固定资产。 对于每个固定资产，选择具有折旧模板的价值模型和折旧帐簿。 您不能直接在“固定资产”****页上添加或修改折旧模板。 您只能在“折旧帐簿”****上修改折旧模板。
5.  在“价值模型”****页或“折旧帐簿”****页上，在“工作量法折旧”****字段组中，在以下字段中输入信息：
    -   消耗系数
    -   单位
    -   单位折旧额
    -   估计消耗量

    “已过帐的消耗量”****字段按单位显示已为固定资产和价值模型组合或固定资产折旧帐簿过帐的工作量法折旧。 不能在此字段中手动更新值。

## <a name="examples"></a>示例
### <a name="example-1"></a>示例 1

为 1 月 31 日设置以下消耗系数：

-   数量为 1,000。
-   为固定资产指定的单位折旧价格为 1.5。

1 月 31 日的折旧方案如下：数量 × 单位折旧 1,000 × 1.5 = 1,500。如果为固定资产指定的系数是百分比系数，则在“估计消耗量”****字段中为固定资产的价值模型估计的数量会乘以为所选结束日期设置的百分比。 然后，生成的数量建议作为期间的折旧数量。

### <a name="example-2"></a>示例 2

为 1 月 31 日设置以下工作量法折旧系数：

-   百分比为 10%。
-   为固定资产指定的单位折旧价格为 1.5。
-   固定资产的估计数量为 2,000。

1 月 31 日的折旧方案如下：估计数量 × 百分比 × 单位折旧 2,000 × .10 × 1.5 = 300





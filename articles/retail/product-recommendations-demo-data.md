---
title: 全渠道产品建议演示数据
description: 此文档旨在使用预填充的可自定义演示数据提供有关如何在 1 级单盒环境中利用全渠道产品建议的指导。
author: bebeale
manager: AnnBe
ms.date: 12/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 31aa5dbd2fa814fd572024a4ae36b9d9b46a2fb0
ms.sourcegitcommit: 398c0652acde12c953de007d06055456d6e0a516
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/02/2019
ms.locfileid: "2872318"
---
# <a name="omni-channel-product-recommendations-demo-data"></a>全渠道产品建议演示数据

此文档旨在使用预填充的可自定义演示数据提供有关如何在 1 级单盒环境中利用全渠道产品建议的指导。

全渠道产品建议提供一组以编辑身份策划或以编程方式生成的已排序产品列表。 可以在多种方案中使用这些列表，具体取决于业务需要。 有关产品建议列表的详细信息，请参阅[产品建议概述](../commerce/product-recommendations.md)。

对于 2 级及更高 Dynamics 环境，将根据客户数据自动计算产品建议。
使用产品建议演示数据不会禁用环境中已设置的任何产品建议解决方案和与其使用关联的任何成本。

对于 1 级环境，产品建议仅基于 csv 文件中存储的静态演示数据。

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>在环境中启用产品建议演示数据

客户需要将 **Dynamics 365 Commerce 预览演示扩展**部署到相应环境，这将自动启用产品建议演示数据。

## <a name="default-demo-data"></a>默认演示数据
每个 Onebox 类型的环境都自带一组预加载的产品建议演示数据，这些数据存储在以逗号分隔的 **‘reco_demo_data.csv’** 文件中，该文件与此文档位于 Retail Server 上的同一个文件夹中。

此数据与以下列一起结构化

| 列名         | 限定          | 说明                                                                                                                                 | 可能的值                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | 演示数据点要生成的特定产品建议列表类型。                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | 预期在其中出现产品建议的特定运营单位编号。                                        |                                                                              |
| 类别            |                    |    应该为其返回特定列表的类别。 如果不指定任何类别，则列表仅针对导航层次结构顶部。    |                                                                              |
| SeedItemId          |                    |    对于需要种子的列表（RecoPeopleAlsoBuy 和 RecoCart），为这些列表应为其显示更多产品的产品。            |                                                                              |
| ItemIds             | :heavy_check_mark: | 要作为结果返回且以 **‘;’** 分隔的一个或多个产品。                                                                  |                                                                              |


## <a name="customize-demo-data"></a>自定义演示数据
客户可编辑包含在总部配置的任何产品和类别信息的默认演示数据。 更新 CSV 之后，返回给客户的产品建议将立即体现更改。

此扩展中包含一个数据文件，称为 RecoMockDataset.csv，供客户控制用于增强模拟建议结果的数据集。 可以使用 **ext.Recommendations.DemoFilePath** 设置通过扩展名配置来控制文件名。 这样就可以为客户提供多个可通过配置轻松切换的数据集。

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>其他资源

[产品建议概述](../commerce/product-recommendations.md)

[环境计划](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)

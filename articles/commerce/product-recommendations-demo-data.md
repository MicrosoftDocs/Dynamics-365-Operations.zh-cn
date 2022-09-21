---
title: 使用演示数据创建建议
description: 本文使用预填充的可自定义演示数据提供有关如何在 1 级单盒环境中利用全渠道产品建议的指导。
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7e3df414b3c16c28b6f5ca04f765d91c1312ada4
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459960"
---
# <a name="create-recommendations-with-demo-data"></a>使用演示数据创建建议

[!include [banner](includes/banner.md)]

本文使用预填充的可自定义演示数据提供有关如何在 1 级单盒环境中利用全渠道产品建议的指导。

全渠道产品建议提供一组以编辑身份策划或以编程方式生成的产品列表。 可以在多种方案中使用这些列表，具体取决于业务需要。 有关产品建议列表的详细信息，请参阅[产品建议概述](product-recommendations.md)。

对于 2 级及更高 Dynamics 365 环境，将根据客户数据自动计算产品建议。 使用产品建议演示数据不会禁用环境中已设置的任何产品建议解决方案和与其使用关联的任何成本。

对于 1 级环境，产品建议仅基于 .csv 文件中存储的静态演示数据。

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>在环境中启用产品建议演示数据
若要启用产品建议演示日期，需要将 Dynamics 365 Commerce 预览演示扩展部署到相应环境。 这将自动启用产品建议演示数据。

## <a name="default-demo-data"></a>默认演示数据
每个 OneBox 类型的环境都自带一组预加载的产品建议演示数据，这些数据存储在以逗号分隔的“reco_demo_data.csv”文件中，该文件位于 Commerce Scale Unit 上。

此数据与以下列一起结构化。

| 列名         | 强制          | 说明                                                                                                                                 | 可能的值                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | 演示数据点要生成的特定产品建议列表类型。                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li><li>RecoPicks</li><li>RecoSimilarVisual</li><li>RecoSimilarTextual</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | 预期在其中出现产品建议的特定运营单位编号。                                        |                                                                              |
| 类别            |                    |    应该为其返回特定列表的类别。 如果不指定任何类别，则列表仅针对导航层次结构顶部。    |                                                                              |
| SeedItemId          |                    |    对于需要种子的列表（RecoPeopleAlsoBuy 和 RecoCart），为这些列表应为其显示更多产品的产品。            |                                                                              |
| CustomerId          |                    |    对于需要客户标识的列表 (RecoPicks)。  默认值“0”适用于所有客户。          |                                                                              |
| ItemIds             | :heavy_check_mark: | 要作为结果返回且以“;”分隔的一个或多个产品。                                                                  |                                                                              |

## <a name="customize-demo-data"></a>自定义演示数据
您可编辑包含在总部配置的任何产品和类别信息的默认演示数据。 更新 .csv 之后，返回给客户的产品建议将立即体现更改。

此扩展中包含一个数据文件，称为 RecoMockDataset.csv，供您控制用于增强模拟建议结果的数据集。 可以使用 **ext.Recommendations.DemoFilePath** 设置通过扩展名配置来控制文件名。 这样就可以为您提供多个可通过配置轻松切换的数据集。


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a>其他资源

[产品建议概览](product-recommendations.md)

[在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage](enable-adls-environment.md)

[启用产品建议](enable-product-recommendations.md)

[启用个性化建议](personalized-recommendations.md)

[选择退出个性化产品建议](personalization-gdpr.md)

[启用“购买类似外观”建议](shop-similar-looks.md)

[在 POS 上添加产品建议](product.md)

[向交易记录屏幕添加建议](add-recommendations-control-pos-screen.md)

[调整 AI-ML 建议结果](modify-product-recommendation-results.md)

[手动创建策划的建议](create-editorial-recommendation-lists.md)

[产品建议常见问题](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

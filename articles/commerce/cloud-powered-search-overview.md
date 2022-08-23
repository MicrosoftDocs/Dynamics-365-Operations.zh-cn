---
title: 云助力的搜索概览
description: 本文概述 Microsoft Dynamics 365 Commerce 中的云助力搜索。
author: ashishmsft
ms.date: 02/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.assetid: ''
ms.openlocfilehash: ed80ff42ea5c6e6a904ea2855953d006f66aad37
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273658"
---
# <a name="cloud-powered-search-overview"></a>云助力的搜索概览

[!include [banner](includes/banner.md)]

本文概述 Microsoft Dynamics 365 Commerce 中的云助力搜索。

产品发现功能有助于确保客户通过浏览类别，搜索和筛选，快速、轻松地找到产品。 零售商将产品发现视为跨由 Cloud Scale Unit (CSU) 提供支持的渠道（如电子商务和销售点 (POS)）进行客户交互的主要工具。

客户习惯了 Web 搜索引擎几乎即时响应，精美的电子商务网站，社交应用，键入搜索词时显示自动建议，分面导航和突出显示。 如果客户无法在一个电子商务商店中快速找到要查找的产品，将立即转到其他电子商务商店。

Commerce 中的云助力产品发现功能可帮助零售商继续提高 CSU 提供支持的渠道的客户保留和转化率。

Commerce 搜索体验的功能已改进，可以帮助零售商改善产品发现功能。 同时，这些功能提供电子商务流量所需可扩展性和性能。

## <a name="browse-and-search"></a>浏览和搜索

搜索相关性和性能是全渠道体验中的关键因素，因为产品发现主要依赖搜索功能检索信息和对内容进行导航。 高效、有效的浏览器和搜索体验可帮助提高转换。

下图显示典型浏览和搜索功能的示例。

![搜索登陆页面。](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>分面导航和选项汇总 

分面导航可帮助客户通过筛选链接到单词集中的单词的优化器，更轻松地浏览内容。 客户选择并应用优化器之后，将显示选项汇总。 

可使用分面导航为单词集中的不同单词配置不同优化器，不必创建更多页。 

下图显示一个示例，其中在搜索中使用分面导航。

![选项汇总。](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>沉浸式自动建议

当前自动建议功能显示触发搜索匹配的关键字的关键字。 Commerce 中的新增强通常让客户可以在完成键入前发现产品的链接。

Commerce 也支持各种类别中使用关键字匹配功能。 客户可使用此功能查看类别中的匹配关键字的数量，并在其他类别中触发关键字搜索。

下图显示正在使用沉浸式自动建议的示例。

![沉浸式自动建议。](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>排序

利用排序功能，客户可按条件（如价格、产品名和产品号）对类别结果进行排序、搜索和浏览。 如果您在环境中启用[产品建议](product-recommendations.md)，客户还可以根据高级排序条件（如新品、畅销品和趋势）对结果进行排序。


> [!NOTE]
> 从版本 10.0.8 开始可使用这些云助力的搜索功能。 确保在 **Commerce 参数 > 配置参数** 中将“ProductSearch.UseAzureSearch”条目设置为“true”。 
![云助力搜索的配置参数。](./media/CloudPoweredSearchConfigurationParameters.png)
>Commerce SSK 版本 9.35+ 和 Dynamics 365 Commerce 10.0.20 版本提供高级排序选项（如新品、畅销品和趋势）。  


## <a name="additional-resources"></a>其他资源

[默认类别登陆页面和搜索结果页面概览](category-search-page-overview.md)

[管理 SEO 元数据](manage-seo-metadata.md)


[!INCLUDE [footer-include](../includes/footer-banner.md)]

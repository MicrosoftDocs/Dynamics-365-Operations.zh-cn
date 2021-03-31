---
title: 云助力的搜索概览
description: 此主题概述 Microsoft Dynamics 365 Commerce 中的云助力搜索。
author: ashishmsft
manager: annbe
ms.date: 06/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2e94338cb55f3298d0a33d7b086480f16e83f271
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220648"
---
# <a name="cloud-powered-search-overview"></a>云助力的搜索概览


[!include [banner](includes/banner.md)]

此主题概述 Microsoft Dynamics 365 Commerce 中的云助力搜索。

## <a name="overview"></a>概览

产品发现功能有助于确保客户通过浏览类别，搜索和筛选，快速、轻松地找到产品。 零售商将产品发现视为所有渠道中的主要客户互动工具。

客户习惯了 Web 搜索引擎几乎即时响应，精美的电子商务网站，社交应用，键入搜索词时显示自动建议，分面导航和突出显示。 如果客户在一个电子商务商店中无法足够快找到查找的产品，将立即转到其他电子商务商店。

Dynamics 365 Commerce 中的云助力产品发现功能可帮助零售商继续提高所有渠道（电子商务渠道和销售点 (POS) 渠道）中的客户保留和转换率。

Dynamics 365 Commerce 搜索体验的功能已改进，可以帮助零售商改善产品发现功能。 同时，这些功能提供电子商务流量所需可扩展性和性能。

## <a name="browse-and-search"></a>浏览和搜索

搜索相关性和性能是全渠道体验中的关键因素，因为产品发现主要依赖搜索功能检索信息和对内容进行导航。 高效、有效的浏览器和搜索体验可帮助提高转换。

下图显示典型浏览和搜索功能的示例。

![搜索登陆页](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>分面导航和选项汇总 

分面导航可帮助客户通过筛选链接到单词集中的单词的优化器，更轻松地浏览内容。 客户选择并应用优化器之后，将显示选项汇总。 

可使用分面导航为单词集中的不同单词配置不同优化器，不必创建更多页。 

下图显示一个示例，其中在搜索中使用分面导航。

![选项汇总](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>沉浸式自动建议

当前自动建议功能仅显示触发搜索匹配的关键字的关键字。 Dynamics 365 Commerce 中的新增强通常让客户可以在完成键入前发现产品的链接。

Dynamics 365 Commerce 也支持各种类别中使用关键字匹配功能。 客户可使用此功能查看类别中的匹配关键字的数量，并在其他类别中触发关键字搜索。

下图显示正在使用沉浸式自动建议的示例。

![沉浸式自动建议](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>排序

客户可使用 Dynamics 365 Commerce 中的增强排序功能按条件（如价格、产品名和产品号）对搜索结果进行排序、搜索和浏览。 客户还可以基于产品是新产品、最畅销产品还是最近添加的产品对结果排序。

>[!NOTE]
>从版本 10.0.8 开始可使用这些云助力的搜索功能。 确保 **Commerce 参数 > 配置参数** 下有一个条目是“ProductSearch.UseAzureSearch 设置为 true”。 
![云助力搜索的配置参数](./media/CloudPoweredSearchConfigurationParameters.png)

## <a name="additional-resources"></a>其他资源

[默认类别登陆页面和搜索结果页面概览](category-search-page-overview.md)

[管理 SEO 元数据](manage-seo-metadata.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: 默认类别登陆页面和搜索结果页面概览
description: 此主题概述 Dynamics 365 Commerce 中的默认类别登陆页和搜索结果页。
author: ashishmsft
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f380f3f56727d927d7cd328fef3c9d999afa2873
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794341"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a>默认类别登陆页面和搜索结果页面概览

[!include [banner](includes/banner.md)]

此主题概述 Microsoft Dynamics 365 Commerce 电子商务中的默认类别登陆页和搜索结果页。

## <a name="default-category-landing-page"></a>默认类别登陆页面

默认类别登陆页是网站用户选择导航层次结构中的类别时将把他们带到的页面。 类别页用于浏览，也可以对已分类产品进行排序和优化。

![默认类别登陆页面](./media/SimpleCategoryLandingDressCategory.png)

页面顶部是显示所有产品类别的页眉和促销经理已分类的其他页面。 配置渠道导航层次结构时进行配置。 页面底部是页脚，其中包含购物者可能感兴趣的各主题的快速链接。

以下组件对类别至关重要：

- **产品放置磁贴** 显示配置导航层次结构时促销经理定义的产品。
- **优化器和选项摘要** 是提供计数且可用于优化项的筛选器。 配置与渠道类别和产品属性有关的元数据时，促销经理配置这些。
- 网站访问者使用 **排序选项** 对产品排序。 默认情况下，可使用以下排序选项：

    - 价格 – 从低到高
    - 价格 – 从高到低
    - 产品名称 – \[A-Z\]
    - 产品名称 – \[Z-A\]
    - 评分 – 从低到高
    - 评分 – 从高到低

- 网站访问者可使用 **分页** 从一页已分类产品结果移到另一页。
- **总计数** 提供类别中定义的产品总数。

## <a name="enrich-a-category-landing-page"></a>丰富类别登陆页面

如果希望类别登陆页中包含特定类别定制程度更深的体验，可以“扩充”该类别的类别登陆页。 例如，可添加市场营销视频和某些类别故事分享吸引购物者的注意。 有关详细信息，请参阅[扩充类别登陆页](enrich-category-page.md)。

![扩充的类别登陆页面](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a>自动建议和搜索结果页

网站用户可通过从导航层次结构转到类别或通过在搜索字段中输入搜索词，浏览站点。

只要用户开始在搜索字段中键入，就可以体验沉浸式自动建议功能以建议搜索词。

下面是可以显示的一些建议类型：

- **关键字** 用于在所有产品中查找归类为渠道的项。
- **产品** 提供产品详细信息页的直接链接。
- **作用域类别搜索建议** 列举各类别，可供用户在特定类别中搜索关键字。

![沉浸式自动建议](./media/ImmersiveAutoSuggestUX.png)

当用户选择一个关键字或作用域类别搜索建议时，或当没有所输入搜索词的建议时，将把用户重定向到搜索结果页。 然后，用户可浏览、排序和优化搜索结果列以查找所需项。

![搜索登录](./media/SearchLanding.png)

以下组件对搜索结果页至关重要：

- **产品放置磁贴** 显示用户搜索的产品。 默认情况下，这些磁贴按用户搜索的云助力搜索相关性分数排序。
- **优化器和选项摘要** 是提供计数且可用于优化项的筛选器。 配置“渠道类别和产品属性”元数据时，促销经理配置这些。
- 网站访问者使用 **排序选项** 对产品排序。 默认情况下，可使用以下排序选项：

    - 价格 – 从低到高
    - 价格 – 从高到低
    - 产品名称 – \[A-Z\]
    - 产品名称 – \[Z-A\]
    - 评分 – 从低到高
    - 评分 – 从高到低
    - 默认

- 网站访问者可使用 **分页** 从一页已分类产品结果移到另一页。
- **总计数** 提供类别中定义且与搜索条件匹配的产品的总数。

>[!NOTE]
>从版本 10.0.8 开始可使用这些云助力的搜索功能。 确保 **Commerce 参数 > 配置参数** 下有一个条目是“ProductSearch.UseAzureSearch 设置为 true”。 
![云助力搜索的配置参数](./media/CloudPoweredSearchConfigurationParameters.png)

## <a name="additional-resources"></a>其他资源

[云助力的搜索概览](cloud-powered-search-overview.md)

[主页概览](quick-tour-home-page.md)

[产品详细信息页面概览](quick-tour-pdp.md)

[购物车和结账页面概览](quick-tour-cart-checkout.md)

[帐户管理页面概览](quick-tour-account-management.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
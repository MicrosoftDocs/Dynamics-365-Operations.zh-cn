---
title: 配置评分和评价
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中配置电子商务站点以显示客户评分和评价。
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0612b32e7751b32ad851f627a53bce2ac491870f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770473"
---
# <a name="configure-ratings-and-reviews"></a>配置评分和评价

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中配置电子商务站点以显示客户评分和评价。

## <a name="overview"></a>概览

电子商务网站中的评分和评价可帮助客户在做出采购决定之前了解产品，方法是对其显示其他客户对这些产品的看法。 对于电子商务网站，评分和评价也是用于收集有关产品的客户反馈的机制。 

评分在产品列表页、类别列表页、搜索结果页和其他站点页中显示。 评分直方图和产品评价在产品详细信息页 (PDP) 中显示。 客户可使用**撰写评价**按钮提交产品的评分和评价。

## <a name="ratings-and-reviews-modules-on-pdps"></a>PDP 中的评分和评价模块 

PDP 中的三个模块显示评分和评价摘要：

- 撰写评价模块
- 产品评级列表模块
- 评分直方图模块
 
下图显示评分和评价模块在 PDP 上的外观。

![PDP 上的评分和评价模块](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> 有关如何优化 PDP 模板和布局，以便在电子商务站点中的多个 PDP 之间共享评分和评价模块的配置的信息，请参阅[模板和布局概述](templates-layouts-overview.md)。

下图显示 Dynamics 365 Commerce 中**添加模块**对话框如何显示评分和评价模块。

![“添加模块”对话框](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>撰写评价模块

撰写评价模块中有一个**撰写评价**按钮，供用户登录，分配评分和撰写产品评价。 用户可使用此模块编辑之前提交的评分或评价。 此模块通常在 PDP 上的评分直方图和产品评价列表模块上方显示。

下图显示当客户选择**撰写评价**时显示的**撰写评价**对话框。 客户可使用此对话框提交评分和评价。

![“撰写评价”对话框](media/rnr-eCommerce-write-review-module.png)

下表显示需要在制作工具中配置的撰写评价模块属性。

| 属性名称 | 值        | 属性描述                 |
|---------------|--------------|--------------------------------------|
| 姓名          | 撰写评价 | 撰写评价模块的名称。 |

### <a name="ratings-histogram-module"></a>评分直方图模块

评分直方图模块显示评分直方图。 此模块通常在 PDP 中撰写评论模块与产品评论列表模块之间显示。

评分直方图模块不需要配置。 只需在 PDP 模板中添加此模块。 

下图显示将评分和评价模块配置为在 PDP 中显示时，PDP 模板在 Dynamics 365 Commerce 中的外观。

![将评分或评价配置为在 PDP 中显示时的 PDP 模板](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>产品评级列表模块

产品评级列表模块显示产品评级列表和排序、筛选和分页选项。 此模块通常在 PDP 中的评分直方图模块后显示。

下表显示需要在制作工具中配置的产品评价列表模块属性。

| 属性名称              | 值 | 属性描述 |
|----------------------------|-------| ---------------------|
| 每页显示的评论 | 10    | PDP 中应该同时显示的评论数量。 包括**下一页**和**上一页**按钮，以便用户在多页评论之间切换。 |

#### <a name="ratings-histogram--summary-view"></a>评分直方图 – 摘要视图

产品评论列表模块中有一个插槽，可在其中添加评分直方图模块。 下图显示如何在 Dynamics 365 Commerce 中的产品评论列表模块内添加评分直方图模块。

![在产品评论列表模块中添加评分直方图模块](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>配置站点以显示评分和评价

评分或评价的配置值（如租户 ID、评论文本长度和评论标题长度）在站点级别配置。 

若要配置站点以显示评分或评价，请执行以下步骤。 

1. 转到**主 \> 站点**。
1. 选择站点的名称。 
1. 转到**站点管理 \> 扩展性**。 
1. 在**评论文本最大长度**字段中，输入评论文本可包含的最大字符数（例如，**1000**）。 
1. 在**评论标题最大长度**字段中，输入评论标题可包含的最大字符数（例如，**55**）。 
1. 选择**保存并发布**。 

下图显示此配置在 Dynamics 365 Commerce 中的显示效果。

![配置站点以显示评分和评价](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>将产品评分链接到 PDP 的“评论”部分

将在 PDP 顶部的产品标题下显示产品评分。 可将产品评分配置为链接到同一个 PDP 的**评论**部分。 

若要将产品评分链接到 PDP 的**评论**部分，请执行以下步骤。

1. 打开 PDP 模板。 
1. 转到**购买框容器模块设置**。
1. 在**购买框**下，选择**产品评分**，然后选中**链接单击以显示完整评论模块**复选框。

下图显示此配置在 Dynamics 365 Commerce 中的显示效果。

![将产品评分链接到 PDP 的“评论”部分](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>配置隐私和政策页的链接

若要配置隐私和政策页的链接，请执行以下步骤。

1. 转到**主 \> 站点**。
1. 选择站点的名称。 
1. 转到**站点管理 \> 扩展性**
1. 在**路由**选项卡中 **RNR 隐私和政策**下，选择**添加链接**。 如果已经输入了链接，但希望将其替换，请选择该链接。 
1. 在**添加链接**对话框中，选择隐私和政策页的链接，然后选择**确定**。 
1. 选择**保存并发布**。 

下图显示此配置在 Dynamics 365 Commerce 中的显示效果。

![配置隐私和政策页的链接](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a>其他资源

[评分和评价概览](ratings-reviews-overview.md)

[选择使用评分和评价](opt-in-ratings-reviews.md)

[管理评分和评价](manage-reviews.md)

[在 Dynamics 365 Retail 中同步产品评分](sync-product-ratings.md)

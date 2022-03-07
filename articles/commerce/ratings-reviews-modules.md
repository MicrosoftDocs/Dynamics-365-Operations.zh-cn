---
title: 评分和评价模块
description: 此主题介绍 Microsoft Dynamics 365 Commerce 中产品详细信息页上使用的评分和评论模块。
author: gvrmohanreddy
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: 66ee2d4185cad45b70b19fb474c64ae77a2868e835b20d5275e21610c0150370
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761554"
---
# <a name="ratings-and-reviews-modules"></a>评分和评价模块

[!include [banner](includes/banner.md)]

此主题介绍 Microsoft Dynamics 365 Commerce 中产品详细信息页 (PDP) 上使用的评分和评论模块。

电子商务网站中的评分和评价可帮助客户在做出采购决定之前了解产品，也是收集客户对产品的反馈的机制。 

评分在产品列表页、类别列表页、搜索结果页和其他站点页中显示。 

评分直方图和产品评价在 PDP 中显示。 客户可使用 **撰写评价** 按钮提交产品的评分和评价。 这些 PDP 功能受评分和评价模块控制。

## <a name="ratings-and-reviews-modules-on-pdps"></a>PDP 中的评分和评价模块 

PDP 中的三个模块显示评分和评价摘要：
- 撰写评价模块
- 产品评级列表模块
- 评分直方图模块
 
下图显示评分和评价模块在 PDP 上的外观。

![PDP 上的评分和评价模块。](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> 有关如何优化 PDP 模板和布局，以便在电子商务站点中的多个 PDP 之间共享评分和评价模块的配置的信息，请参阅[模板和布局概述](templates-layouts-overview.md)。

下图显示 Dynamics 365 Commerce 中 **添加模块** 对话框如何显示评分和评价模块。
![“添加模块”对话框。](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>撰写评价模块

撰写评价模块中有一个 **撰写评价** 按钮，供用户登录，分配评分和撰写产品评价。 用户可使用此模块编辑之前提交的评分或评价。 此模块通常在 PDP 上的评分直方图和产品评价列表模块上方显示。
下图显示当客户选择 **撰写评价** 时显示的 **撰写评价** 对话框。 客户可使用此对话框提交评分和评价。

![“撰写评价”对话框。](media/rnr-eCommerce-write-review-module.png)

下表显示需要在制作工具中配置的撰写评价模块属性。

| 属性名称 | 值        | 属性描述                 |
|---------------|--------------|--------------------------------------|
| 姓名          | 撰写评价 | 撰写评价模块的名称。 |

### <a name="ratings-histogram-module"></a>评分直方图模块

评分直方图模块显示评分直方图。 此模块通常在 PDP 中撰写评论模块与产品评论列表模块之间显示。
评分直方图模块不需要配置。 只需在 PDP 模板中添加此模块。 下图显示将评分和评价模块配置为在 PDP 中显示时，PDP 模板在 Dynamics 365 Commerce 中的外观。
![将评分或评价配置为在 PDP 中显示时的 PDP 模板。](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>产品评级列表模块

产品评级列表模块显示产品评级列表和排序、筛选和分页选项。 此模块通常在 PDP 中的评分直方图模块后显示。
下表显示需要在制作工具中配置的产品评价列表模块属性。

| 属性名称              | 值 | 属性描述 |
|----------------------------|-------| ---------------------|
| 每页显示的评论 | 10    | PDP 中应该同时显示的评论数量。 包括 **下一页** 和 **上一页** 按钮，以便用户在多页评论之间切换。 |

#### <a name="ratings-histogram--summary-view"></a>评分直方图 – 摘要视图

产品评论列表模块中有一个插槽，可在其中添加评分直方图模块。 下图显示如何在 Dynamics 365 Commerce 中的产品评论列表模块内添加评分直方图模块。

![在产品评价列表模块中添加评分直方图模块。](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a>其他资源

[模块库概览](starter-kit-overview.md)

[容器模块](add-container-module.md)

[购物车模块](add-cart-module.md)

[结帐模块](add-checkout-module.md)

[订单确认模块](order-confirmation-module.md)

[页眉模块](author-header-module.md)

[页脚模块](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
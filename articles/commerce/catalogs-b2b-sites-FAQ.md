---
title: B2B 的 Commerce 目录常见问题解答
description: 本主题提供有关 Microsoft Dynamics 365 Commerce 目录的常见问题的解答。
author: ashishmsft
ms.date: 05/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 5bdc7dfcb0e48aa85db2db4d178c5bf62ea0411b
ms.sourcegitcommit: bca0cb730307948368a9aabe322cf963688ed8b1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/19/2022
ms.locfileid: "8782854"
---
# <a name="commerce-catalogs-for-b2b-faq"></a>B2B 的 Commerce 目录常见问题解答

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

本主题提供有关 Microsoft Dynamics 365 Commerce [企业到企业 (B2B) 目录](catalogs-b2b-sites.md) 的常见问题的解答。

## <a name="why-cant-i-configure-a-catalog-specific-navigation-hierarchy-or-see-an-option-to-associate-a-customer-hierarchy"></a>为什么我无法配置特定于目录的导航层次结构或无法看到用于关联客户层次结构的选项？

请确保在 Commerce Headquarters 的 **功能管理** 工作区中启用了 **允许对零售渠道使用多个目录** 功能。 此外，请确保您的环境使用的是 Commerce 版本 10.0.27 或更高版本。

## <a name="can-i-view-the-catalog-specific-hierarchy-and-enrich-category-pages-in-commerce-site-builder"></a>我可以在 Commerce 站点生成器中查看特定于目录的层次结构并扩充类别页面吗？

可以，有权访问站点生成器中的 **产品** 页面的 Commerce 站点生成器用户可以选择目录并查看特定于目录的层次结构。 从 **产品** 页面中，用户还可以扩充目录中特定类别的类别页面。 有关详细信息，请参阅[扩充类别登陆页](enrich-category-page.md)。 如果您想拥有特定于某个目录的扩充内容，我们建议您为该目录准备一个独特且唯一的导航层次结构。

## <a name="can-a-b2b-shopper-purchase-from-multiple-catalogs-in-a-single-checkout"></a>B2B 购物者可以在一次结帐中从多个目录中购买吗？

可以，允许在一次结帐中从多个目录购买。 B2B 购物者可以使用购物车视图中的目录指示器来确定从哪些目录添加了哪些商品。

## <a name="if-a-b2b-shopper-purchases-the-same-item-from-different-catalogs-what-is-the-expected-behavior"></a>如果 B2B 购物者从不同的目录购买相同的商品，那么预期行为是什么？

尽管给定用户可能会在给定时间访问多个目录，但期望这些目录中的产品将是互斥的。 换句话说，理想情况下，同一产品不应出现在给定用户的多个目录中。

但是，如果出现相同产品属于多个目录的情况，系统将为该产品维护多个购物车行。 每个目录将有一个单独的行。 结帐时不会合并来自两个不同目录的相同产品。

## <a name="when-a-b2b-shopper-is-shopping-is-there-any-validation-for-catalog-availability"></a>当 B2B 购物者购物时，是否有任何目录可用性验证？

是。 仅当购物车中的所有商品都来自有效目录时，才允许 B2B 购物者进行结帐。 如果任何购物车商品来自过期或取消的目录，则将删除它们，并通知用户。

## <a name="during-the-shopping-experience-are-search-and-product-discovery-including-related-and-recommended-product-collections-catalog-specific"></a>在购物体验期间，搜索和产品发现（包括相关和推荐的产品集合）是否特定于目录？

是。 一旦用户选择了一个特定目录，整个购物旅程就变成了特定于目录的旅程。 此旅程包括产品发现体验，例如搜索建议、搜索结果、类别结果、优化器、定价、属性和推荐产品（例如新产品、畅销产品、新潮产品、经常一起购买的产品和相关产品）。

## <a name="can-a-b2b-shopper-purchase-from-the-default-assortment-catalogid0"></a>B2B 购物者可以从默认分类 (catalogID=0) 中购买吗？

不可以，不允许 B2B 购物者从默认分类中进行购买。 此分类仅用于匿名浏览。 如果 B2B 购物者缺少目录分配（等待他们的管理层进行更新），那么他们将无法看到他们可以从中进行选择的任何目录，并且不会看到任何类别层次结构。

## <a name="can-marketing-content-be-curated-for-a-product-that-is-specific-to-a-catalog"></a>可以为特定于目录的产品策划市场营销内容吗？

目前，仅在站点和渠道级别支持产品扩充。 换言之，如果扩充产品，则该产品将在多个目录之间共享，并且该产品的相应产品详细信息页 (PDP) 将以相同方式呈现在给定站点的所有目录中。

## <a name="is-catalog-support-available-for-both-b2b-and-business-to-consumer-b2c-online-channels"></a>目录支持是否适用于 B2B 和企业对消费者 (B2C) 在线渠道？

目前，Commerce 目录仅适用于 B2B 渠道。

## <a name="can-we-set-up-catalog-specific-upsellcross-sell-items"></a>我们可以设置特定于目录的向上销售/交叉销售商品吗？

当前，仅支持相关产品功能。 但是，向上销售和交叉销售商品配置可用于呼叫中心。

呼叫中心也只支持以下功能：

- 目录源代码
- 使用源 ID 跟踪成本和响应率
- 目录特定的订单和商品脚本
- 目录页分析
- 目录请求
- 付款计划
- 基于源代码的免费产品

## <a name="can-we-use-catalog-source-codes-for-b2b-orders-through-the-e-commerce-portal"></a>我们可以通过电子商务门户针对 B2B 订单使用目录源代码吗？

否。 仅呼叫中心渠道支持目录源代码。

## <a name="additional-resources"></a>其他资源

[为 B2B 站点创建 Commerce 目录](catalogs-b2b-sites.md)

[Commerce 目录对 B2B 自定义的可扩展性影响](catalogs-b2b-sites-dev.md)

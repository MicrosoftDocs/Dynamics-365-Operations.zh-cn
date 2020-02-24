---
title: 产品建议常见问题
description: 此主题介绍可用于诊断与产品建议或其结果有关的流程和工具。
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7951f92ef68a7a782f2874d7b73d7e45eba0afba
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003019"
---
# <a name="product-recommendations-faq"></a>产品建议常见问题


[!include [banner](includes/banner.md)]

此主题介绍可用于诊断与[产品建议](product-recommendations.md)或其结果有关的流程和工具。

## <a name="best-practices"></a>最佳实践
请务必利用基础产品和变型概念。 对父产品的变型合理分组可帮助列表算法和服务创建更好的模型。 此外，此服务只能处理一个产品实例，而不是将所有关系密切的变型放到一个列表中。 将所有关系密切的变型放到一个列表中后，可能会产生错误结果或重复结果。

## <a name="why-are-products-missing-from-my-recommendation-lists"></a>我的建议列表中为什么缺少产品？

如果产品建议列表中缺少项，通常是因为存在产品配置问题。 例如，产品开始日期或结束日期不正确，维度配置不当，或产品不在正确的渠道分类中等。

如果基于人工智能-机器学习 (AI-ML) 的建议列表中缺少某项，可能是因为该项不符合建议列表的条件，或该项的购买交易数量不足，导致建议列表无法显示该项。

建议执行以下检查步骤：
1. **确保总部已启用产品建议。** 有关如何启用此服务的详细信息，请参阅[启用产品建议](enable-product-recommendations.md)。
1. **确保设置关键产品属性。** 例如，必须将产品分类设置为**包括**。
1. **对于新分类产品，可能最多需要 3 小时，才会在新列表中开始显示该产品。**
1. **如果“热门”、“最畅销”、“用户还喜欢”或“人气组合”中仍然不显示某个产品，说明该产品的交易数量可能不足。** 在此情况下，可以登录进行更多交易，更新默认建议列表参数，或通过手动干预修改建议产品列表结果。 有关建议参数的详细信息，请参阅[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。
1. **确保产品满足列表的建议条件。** 有关产品建议参数的详细信息，请参阅[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a>如何避免返回质量不佳的建议结果？

建议列表需要大量交易记录才能生成结果。 因此，用户务必提供完整的历史交易数据。

此外，交易不足或较少的产品通常没有**用户还喜欢**或**人气组合**结果，并且不再**热门**或**最畅销**建议列表中显示。 每种新产品或购买数量较小的老产品可能经常发生这种情况。 受欢迎的新品很容易克服这个问题。

建议执行以下步骤：
1. **确保产品满足该列表的建议条件。** 有关产品建议参数的详细信息，请参阅“修改基于 AI-ML 的产品建议结果”。
1. **如果产品是新产品，请考虑修改建议列表，直到该产品具有更多交易。** 有关如何修改建议列表结果的详细信息，请参阅[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。


- **确保产品满足该列表的建议条件。** 有关产品建议参数的详细信息，请参阅[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。
- **如果产品是新产品，请考虑修改建议列表，直到该产品具有更多交易**。 有关如何修改建议列表结果的详细信息，请参阅[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a>无法删除某个产品，但是商店中仍然可以看到该产品？

如果需要提高业务，可以调整通过算法生成的类别。 但是，如果从建议列表中删除某个产品，商店中仍然可以发现该产品。 有关如何修改产品建议结果的详细信息，请参阅[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。

如果必须阻止商店中发现某项，必须将**项分类**值设置为**排除**。

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a>如何向电子商务页面添加列表？

有关如何向电子商务网站添加产品建议页面的信息，请参阅[向页面添加产品建议列表](add-reco-list-to-page.md)。

## <a name="how-do-i-enable-recommendations-on-pos"></a>如何在 POS 上启用建议？

启用产品建议之后，需要向控制 POS 屏幕添加建议面板。 有关如何向 POS 设备布局添加建议面板的详细信息，请参阅[本功能文档](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)。

## <a name="additional-resources"></a>其他资源

[产品建议概览](product-recommendations.md)

[启用产品建议](enable-product-recommendations.md)

[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)

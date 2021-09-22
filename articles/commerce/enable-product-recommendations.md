---
title: 启用产品建议
description: 此主题介绍如何做出基于 Microsoft Dynamics 365 Commerce 客户可用的人工智能-机器学习 (AI-ML) 的产品建议。
author: bebeale
ms.date: 08/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4a7be82b3a40aba621693f080ff41767fdaea474
ms.sourcegitcommit: 98061a5d096ff4b9078d1849e2ce6dd7116408d1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2021
ms.locfileid: "7466308"
---
# <a name="enable-product-recommendations"></a>启用产品建议

[!include [banner](includes/banner.md)]

此主题介绍如何做出基于 Microsoft Dynamics 365 Commerce 客户可用的人工智能-机器学习 (AI-ML) 的产品建议。 有关产品建议列表的详细信息，请参阅[产品建议概述](product-recommendations.md)。

## <a name="recommendations-pre-check"></a>预检查建议

1. 确保您拥有有效的 Dynamics 365 Commerce 建议许可证。
1. 确保实体存储已连接到客户负责的 Azure Data Lake Storage Gen2 帐户。 有关详细信息，请参阅[确保已购买 Azure Data Lake Storage 并已在环境中成功验证](enable-ADLS-environment.md)。
1. 确认 Azure AD 标识配置中包含建议的实体。 下面是有关如何执行此操作的详细信息。
1. 确保已计划实体存储每日刷新到 Azure Data Lake Storage Gen2。 有关更多信息，请参阅[确保实体存储刷新已自动化](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)。
1. 为实体存储启用 RetailSale 度量。 有关设置此流程的详细信息，请参阅[使用度量](/dynamics365/ai/customer-insights/pm-measures)。

完成上述步骤后，就可以启用建议。

## <a name="azure-ad-identity-configuration"></a>Azure AD 标识配置

只有运行服务架构 (IaaS) 配置的客户才需要执行此步骤。 对于在 Azure Service Fabric 上运行的客户来说，Azure AD 标识配置是自动的，但是建议您验证该设置的配置是否正确。

### <a name="setup"></a>设置

1. 在 Commerce Headquarters 中，搜索 **Azure Active Directory 应用程序** 页面。
1. 检查 **RecommendationSystemApplication-1** 是否有条目。 如果不存在条目，请使用以下信息创建一个：

    - **客户端 ID**：d37b07e8-dd1c-4514-835d-8b918e6f9727
    - **名称**：RecommendationSystemApplication-1
    - **用户 ID**：RetailServiceAccount

1. 保存并关闭页面。 

## <a name="turn-on-recommendations"></a>开启建议

若要开启产品建议，请执行以下步骤。

1. 在 Commerce headquarters 中，搜索 **功能管理**。
1. 选择 **所有** 查看可用功能列表。 
1. 在搜索框中，输入 **建议**。
1. 选择 **产品建议** 功能。
1. 在 **产品建议** 属性窗格中，选择 **立即启用**。

![打开建议。](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> - 上面的过程开始生成产品建议列表。 可能需要几小时，列表才可用，并且可以在销售点 (POS) 或 Dynamics 365 Commerce 中查看。
> - 此配置不会启用所有建议功能。 个性化建议、“购买相似外观产品”和“购买相似说明产品”之类高级功能由专门的功能管理条目控制。 有关在 Commerce Headquarters 中启用这些功能的信息，请参阅[启用个性化建议 ](personalized-recommendations.md)、[启用“购买相似外观产品”建议](shop-similar-looks.md)和[启用“购买相似说明产品”建议](shop-similar-description.md)。

## <a name="configure-recommendation-list-parameters"></a>配置建议列表参数

默认情况下，基于 AI-ML 的产品建议列表提供建议的值。 可更改默认建议值以适合业务流程。 若要详细了解如何更改默认参数，请转到[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。

## <a name="include-recommendations-in-e-commerce-experiences"></a>在电子商务体验中加入建议

在 Commerce Headquarters 中启用建议后，就可以配置用于显示电子商务体验建议结果的 Commerce 模块。 有关详细信息，请参阅[产品集合模块](product-collection-module-overview.md)。

## <a name="show-recommendations-on-pos-devices"></a>在 POS 设备中显示建议

在 Commerce Headquarters 启用建议之后，必须使用布局工具将建议面板添加到控制 POS 屏幕中。 要了解此过程，请参阅[向 POS 设备上的交易屏幕添加建议控件](add-recommendations-control-pos-screen.md)。 

## <a name="enable-personalized-recommendations"></a>启用个性化建议

在 Dynamics 365 Commerce 中，零售商可以提供个性化的产品建议（也称为个性化）。 通过这种方式，可以将个性化的建议引入到在线和销售点的客户体验中。 当个性化功能打开时，系统可以将用户的购买和产品信息相关联，以生成个性化的产品建议。

若要详细了解个性化推荐，请参阅[启用个性化建议](personalized-recommendations.md)。

## <a name="additional-resources"></a>其他资源

[产品建议概览](product-recommendations.md)

[在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage](enable-adls-environment.md)

[启用个性化建议](personalized-recommendations.md)

[启用“购买类似外观”建议](shop-similar-looks.md)

[选择退出个性化产品建议](personalization-gdpr.md)

[在 POS 中添加产品建议](product.md)

[向交易记录屏幕添加建议](add-recommendations-control-pos-screen.md)

[调整 AI-ML 建议结果](modify-product-recommendation-results.md)

[手动创建策划的建议](create-editorial-recommendation-lists.md)

[使用演示数据创建建议](product-recommendations-demo-data.md)

[产品建议常见问题](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

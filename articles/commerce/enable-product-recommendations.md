---
title: 启用产品建议
description: 此主题介绍如何做出基于 Microsoft Dynamics 365 Commerce 客户可用的人工智能-机器学习 (AI-ML) 的产品建议。
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
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
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b201e5481cfaf5bb6cd64a89cdb6b5a91f31447f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410369"
---
# <a name="enable-product-recommendations"></a>启用产品建议

[!include [banner](includes/banner.md)]

此主题介绍如何做出基于 Microsoft Dynamics 365 Commerce 客户可用的人工智能-机器学习 (AI-ML) 的产品建议。 有关产品建议列表的详细信息，请参阅[产品建议概述](product-recommendations.md)。

## <a name="recommendations-pre-check"></a>预检查建议

启用之前，请注意，仅对已将存储过渡为使用 Azure Data Lake Storage 的 Commerce 客户支持产品推荐。 

启用建议前，必须先在后端启用以下配置：

1. 确保已购买 Azure Data Lake Storage 并已在环境中成功验证。 有关详细信息，请参阅[确保已购买 Azure Data Lake Storage 并已在环境中成功验证](enable-ADLS-environment.md)。
2. 确保实体存储刷新已自动化。 有关更多信息，请参阅[确保实体存储刷新已自动化](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)。
3. 确认 Azure AD 标识配置中包含建议的实体。 下面是有关如何执行此操作的详细信息。

此外，请确保已启用 RetailSale 度量。 若要详细了解此设置流程，请参阅[使用度量](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)。

## <a name="azure-ad-identity-configuration"></a>Azure AD 标识配置

运行服务架构 (IaaS) 配置的所有客户都需要执行此步骤。 对于运行 Service Fabric (SF) 的客户，此步骤应该是自动步骤，我们建议您验证配置的设置是否正确。

### <a name="setup"></a>设置

1. 从后端搜索 **Azure Active Directory 应用程序** 页面。
2. 验证是否有“RecommendationSystemApplication-1”的条目。

如果该条目不存在，请添加具有以下信息的新条目：

- **客户端 ID** - d37b07e8-dd1c-4514-835d-8b918e6f9727
- **名称** - RecommendationSystemApplication-1
- **用户 ID** - RetailServiceAccount

保存并关闭页面。 

## <a name="turn-on-recommendations"></a>开启建议

若要开启产品建议，请执行以下步骤。

1. 在 Commerce headquarters 中，搜索 **功能管理**。
1. 选择 **所有** 查看可用功能列表。 
1. 在搜索框中，输入 **建议**。
1. 选择 **产品建议** 功能。
1. 在 **产品建议** 属性窗格中，选择 **立即启用**。

![开启建议](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> 此过程开始生成产品建议列表。 可能需要几小时，列表才可用，并且可以在销售点 (POS) 或 Dynamics 365 Commerce 中查看。

## <a name="configure-recommendation-list-parameters"></a>配置建议列表参数

默认情况下，基于 AI-ML 的产品建议列表提供建议的值。 可更改默认建议值以适合业务流程。 若要详细了解如何更改默认参数，请转到[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。

## <a name="show-recommendations-on-pos-devices"></a>在 POS 设备中显示建议

在 Commerce 后端启用建议之后，必须使用布局工具将建议面板添加到控制 POS 屏幕中。 要了解此过程，请参阅[向 POS 设备上的交易屏幕添加建议控件](add-recommendations-control-pos-screen.md)。 

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


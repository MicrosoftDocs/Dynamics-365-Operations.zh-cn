---
title: 雇用个性化产品建议
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中让个性化产品建议可以为客户所用。
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8a61ef0720839d371701f2f0a1fdec7e85a5feb7
ms.sourcegitcommit: d3b970c3b93d8be12886b1c5a6bf91f0b33726dd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/19/2020
ms.locfileid: "3700858"
---
# <a name="enable-personalized-recommendations"></a>启用个性化建议

[!include [banner](includes/banner.md)]

本主题介绍如何在 Microsoft Dynamics 365 Commerce 中让个性化产品建议可以为客户所用。

## <a name="overview"></a>概览

在 Dynamics 365 Commerce 中，零售商可以提供个性化的产品建议（也称为个性化）。 通过这种方式，可以将个性化的建议引入到在线和销售点 (POS) 的客户体验中。 当个性化功能打开时，系统可以将用户的购买和产品信息相关联，以生成个性化的产品建议。

## <a name="personalization-prerequisites"></a>个性化的先决条件

在向客户提供个性化的产品建议之前，请注意，仅支持为已将存储迁移到 Azure Data Lake Store 的 Commerce 用户提供产品建议。 零售商必须先[打开产品建议](enable-product-recommendations.md)，然后客户才能够收到个性化产品建议。

> [!NOTE]
> 通过打开产品建议，您还可以打开个性化。 但是，如果关闭个性化，不会关闭其他类型的产品建议。

有关产品建议的详细信息，请参阅[产品建议概述](product-recommendations.md)。

## <a name="turn-on-personalization"></a>打开个性化

若要打开个性化，请执行以下步骤。

1. 在 Commerce headquarters 中，搜索**功能管理**。
1. 选择**所有**查看可用功能列表。 
1. 在搜索框中，输入**建议**。
1. 选择**个性化产品建议**功能。
1. 在**个性化产品建议**属性窗格中，选择**立即启用**。

![打开个性化](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> 打开个性化时，将启动生成个性化产品建议列表的过程。 这些列表最多可能需要一天时间完成在线以及在 POS 上提供和显示。

## <a name="personalized-lists"></a>个性化列表

除了允许现有的计算机生成的列表的个性化外，建议服务还允许在线和 POS 上的产品发现体验的个性化。

打开个性化后，零售商可以在线向购买者显示个性化的“为您推荐”列表或在 POS 终端上显示“为客户推荐”列表。 此外，零售商可以将个性化应用于现有产品建议列表，并为经过身份验证的用户提供一般数据保护条例 (GDPR) 退出体验。 如果关闭个性化，还将关闭这些功能。

### <a name="online-picks-for-you-lists"></a>在线“为您推荐”列表

“为您推荐”列表是一个人工智能机器学习 (AI-ML) 列表，它向经过身份验证的用户显示建议产品的个性化列表。 此列表基于用户的全渠道购买历史记录。 个性化建议会随着用户进行更多购买而动态更新。 这种类型的列表还支持类别筛选，以便零售商可以根据导航层次结构显示首选商品。

必须满足以下用户要求，“为您推荐”列表才可以出现在任何电子商务页面上：

- 用户必须登录。 匿名用户将看不到个性化推荐。
- 用户必须在其帐户中至少进行了一次购买。
- 用户必须选择接收个性化建议。

下图显示了在线商店页面上的“为您推荐”列表的示例。

![在线“为您推荐”列表](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a>POS 上的“为客户推荐”列表

为了增强客户服务体验，零售商可以通过添加有上下文的“为客户推荐”列表来个性化现有的客户详细信息页面。

下图显示了 POS 终端上的“为客户推荐”列表的示例。

![POS 上的“为客户推荐”列表](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a>将个性化应用于现有建议列表

零售商可以将个性化应用于现有建议列表，例如“新品”、“热门”、“最畅销”、“用户也喜欢”和“人气组合”。 将个性化应用于现有列表后，登录用户先前购买的商品将从这些列表中删除。 对于匿名用户和选择不接收个性化建议的用户，将显示现有列表的默认版本。 因此，零售商不必手动维护单独的页面体验。

例如，在下图中，某登录用户已经购买了出现在“热门 - 默认”列表中的黑色手表和棕色工作靴。 因此，用户将看到新产品，而不是这些产品，如“热门 - 个性化”列表中所示。

![应用个性化](./media/applypersonalization.png)

要在 Commerce 站点构建器中将个性化应用到现有建议列表，请按照下列步骤操作。

1. 打开一个包含产品集合模块的现有站点构建器页面。
1. 在左侧导航窗格中，选择该产品集合模块。
1. 在左侧导航窗格中，在**产品**下，选择列表。
1. 在**选择产品列表配置**对话框，在**类型**下，选择列表类型。
1. 选择**应用个性化**复选框，然后选择**确定**。

    ![将个性化应用于热门列表](./media/ApplyPersonalizationToTrending.PNG)

1. 保存页面，完成编辑，然后发布。 页面发布后，登录用户将看到个性化的热门列表。

## <a name="additional-resources"></a>其他资源

[产品建议概览](product-recommendations.md)

[在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage](enable-adls-environment.md)

[启用产品建议](enable-product-recommendations.md)

[启用“购买类似外观”建议](shop-similar-looks.md)

[选择退出个性化产品建议](personalization-gdpr.md)

[在 POS 中添加产品建议](product.md)

[向交易记录屏幕添加建议](add-recommendations-control-pos-screen.md)

[调整 AI-ML 建议结果](modify-product-recommendation-results.md)

[手动创建策划的建议](create-editorial-recommendation-lists.md)

[使用演示数据创建建议](product-recommendations-demo-data.md)

[产品建议常见问题](faq-recommendations.md)

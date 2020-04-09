---
title: 启用产品建议
description: 此主题介绍如何做出基于 Microsoft Dynamics 365 Commerce 客户可用的人工智能-机器学习 (AI-ML) 的产品建议。
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
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
ms.openlocfilehash: d8a579be5df3c5e7718a6fb4720341f3bd01a64c
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154405"
---
# <a name="enable-product-recommendations"></a>启用产品建议

[!include [banner](includes/banner.md)]

此主题介绍如何做出基于 Microsoft Dynamics 365 Commerce 客户可用的人工智能-机器学习 (AI-ML) 的产品建议。 有关产品建议列表的详细信息，请参阅[产品建议概述](product-recommendations.md)。

## <a name="recommendations-pre-check"></a>预检查建议

启用之前，请注意，仅对已将存储过渡为使用 Azure Data Lake Storage (ADLS) 的 Commerce 客户支持产品推荐。 

有关启用 ADLS 的步骤，请参见[如何在 Dynamics 365 环境中启用 ADLS](enable-ADLS-environment.md)。

此外，请确保已启用 RetailSale 度量。 若要详细了解此设置流程，请转到[此处](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)。


## <a name="turn-on-recommendations"></a>开启建议

若要开启产品建议，请执行以下步骤。

1. 转到 **Retail 和 Commerce &gt; 产品建议 &gt; 建议参数**。
1. 在共享参数列表中，选择**建议列表**。
1. 将**启用建议**选项设置为**是**。

![启用产品建议](./media/enableproductrecommendations.png)

> [!NOTE]
> 此过程开始生成产品建议列表。 最多可能需要多个小时，列表才可用，并且可以在销售点 (POS) 或 Dynamics 365 Commerce 中查看。

## <a name="configure-recommendation-list-parameters"></a>配置建议列表参数

默认情况下，基于 AI-ML 的产品建议列表提供建议的值。 可更改默认建议值以适合业务流程。 若要详细了解如何更改默认参数，请转到[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。

## <a name="show-recommendations-on-pos-devices"></a>在 POS 设备中显示建议

在 Commerce 后端启用建议之后，必须使用布局工具将建议面板添加到控制 POS 屏幕中。 要了解此过程，请参阅[向 POS 设备上的交易屏幕添加建议控件](add-recommendations-control-pos-screen.md)。 

## <a name="enable-personalized-recommendations"></a>启用个性化建议

要了解有关如何接收个性化推荐的更多信息，请参见[启用个性化建议](personalized-recommendations.md)。

## <a name="additional-resources"></a>其他资源

[产品建议概览](product-recommendations.md)

[在 Dynamics 365 Commerce 环境中启用 ADLS](enable-adls-environment.md)

[启用个性化建议](personalized-recommendations.md)

[选择退出个性化产品建议](personalization-gdpr.md)

[在 POS 中添加产品建议](product.md)

[向交易记录屏幕添加建议](add-recommendations-control-pos-screen.md)

[调整 AI-ML 建议结果](modify-product-recommendation-results.md)

[手动创建策划的建议](create-editorial-recommendation-lists.md)

[使用演示数据创建建议](product-recommendations-demo-data.md)

[产品建议常见问题](faq-recommendations.md)


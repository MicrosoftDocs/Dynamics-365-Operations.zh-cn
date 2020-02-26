---
title: 启用产品建议
description: 此主题介绍如何做出基于 Microsoft Dynamics 365 Commerce 客户可用的人工智能-机器学习 (AI-ML) 的产品建议。
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
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024948"
---
# <a name="enable-product-recommendations"></a>启用产品建议

[!include [banner](includes/banner.md)]

此主题介绍如何做出基于 Microsoft Dynamics 365 Commerce 客户可用的人工智能-机器学习 (AI-ML) 的产品建议。 有关产品建议列表的详细信息，请参阅[产品建议概述](product-recommendations.md)。

## <a name="recommendations-pre-check"></a>预检查建议

启用之前，请注意，仅对已将存储过渡为使用 Azure Data Lake Storage (ADLS) 的 Commerce 客户支持产品推荐。 

有关启用 ADLS 的步骤，请参见[如何在 Dynamics 365 环境中启用 ADLS](enable-ADLS-environment.md)。

此外，请确保已启用 RetailSale 度量。 若要详细了解此设置流程，请转到[此处](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)。


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

[启用个性化建议](personalized-recommendations.md)

[向页面添加建议列表](add-reco-list-to-page.md)

[向 POS 设备添加建议面板](add-recommendations-control-pos-screen.md)

[产品集合模块概览](product-collection-module-overview.md)

[在 Dynamics 365 环境中启用 ADLS](enable-ADLS-environment.md)


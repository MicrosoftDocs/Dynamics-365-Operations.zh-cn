---
title: 手动创建策划的建议
description: 此主题介绍商家如何为 Microsoft Dynamics 365 Commerce 客户手动创建和管理产品列表。
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e9ce8887f3cd7da0e250d3b0ffe96b222953de44
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965345"
---
# <a name="manually-create-curated-recommendations"></a>手动创建策划的建议

[!include [banner](includes/banner.md)]

此主题介绍商家如何为 Microsoft Dynamics 365 Commerce 客户手动创建和管理产品建议列表。

精选列表是人员创建和精选的单项内容的集合。  

## <a name="create-a-new-list"></a>创建新列表

若要创建精选产品建议列表，请执行以下步骤。

1. 转到 **Retail 和 Commerce &gt; 产品建议 &gt; 建议列表**。
1. 选择 **新建**。
1. 在 **列表 ID** 字段中，输入一个值。
1. 在 **列表名称** 字段中，输入一个值。
    - **列表名称** 是将在 **产品集合** 模块的精选列表部分中显示的列表标题。
1. 若要向列表添加产品，请选择 **添加产品**。
1. 若要更改列表中的产品顺序，请在 **显示顺序** 列中输入一个值。
    - 如果两个产品的显示顺序值相同，则这两个结果的最终顺序可能与后端不同。
1. 选择 **保存** 以保存该列表。

## <a name="example-list"></a>示例列表

![后端的示例精选列表](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a>其他资源

[产品建议概览](product-recommendations.md)

[在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage](enable-adls-environment.md)

[启用产品建议](enable-product-recommendations.md)

[启用个性化建议](personalized-recommendations.md)

[选择退出个性化产品建议](personalization-gdpr.md)

[启用“购买类似外观”建议](shop-similar-looks.md)

[在 POS 上添加产品建议](product.md)

[向交易记录屏幕添加建议](add-recommendations-control-pos-screen.md)

[调整 AI-ML 建议结果](modify-product-recommendation-results.md)

[使用演示数据创建建议](product-recommendations-demo-data.md)

[产品建议常见问题](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
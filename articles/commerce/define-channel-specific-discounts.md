---
title: 定义渠道特定的折扣
description: 零售商通常为不同渠道设置不同折扣。 本文回顾您为特定渠道创建折扣所需了解的概念。
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.industry: Retail
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
ms.openlocfilehash: f426503a6897a73010b77082f4277b65545bfcc3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273546"
---
# <a name="define-channel-specific-discounts"></a>定义特定于渠道的折扣

[!include [banner](includes/banner.md)]

本文回顾您为特定渠道创建折扣所需了解的概念。

## <a name="channel-specific-discounts"></a>渠道特定的折扣

零售商通常为不同渠道提供不同折扣。 这样做可以应对市场情况或对付竞争零售商。

Commerce 使用价格组来定义渠道特定的折扣。 价格组可分配给以下一个或多个实体：渠道、目录、隶属关系和会员计划。 本文讨论渠道，不过，相同的概念适用于目录折扣、隶属关系折扣和会员折扣。

## <a name="price-groups"></a>价格组

[![价格组。](./media/price-groups-1024x608.png)](./media/price-groups.png)

上图说明可以位于交易记录上的实体（渠道、目录、隶属关系、客户、会员卡）和可以配置的不同折扣类型之间的关系。 所有交易记录都在渠道中进行，因此，要确保渠道存在于交易记录上。 剩余的实体是可选的。 在每个主数据页上，都有一个指向相关价格组的链接，您可以根据需要在其中查看和添加价格组。 价格组用于将四个不同类型的实体关联到折扣、价格调整和贸易协议。 我们建议您针对如何命名价格组以使其组织有序规划一种策略。 一个选项是使用字母或数字前缀或后缀来区分不同类型。 例如，渠道价格组的 1-xxxxx 和目录价格组的 2-xxxxx。 有四个查询页侧重于每个可以具有与其关联的折扣的商业实体。

- **渠道价格组** - 此页显示每个价格组的彼此链接的渠道和折扣的列表。
- **目录价格组** – 此页显示每个价格组的彼此链接的目录和折扣的列表。
- **会员价格组** – 此页显示每个价格组的彼此链接的会员计划和折扣的列表。
- **隶属关系价格组** – 此页显示每个价格组的彼此链接的隶属关系和折扣的列表。

## <a name="example-channel-discount-set-up"></a>渠道折扣设置示例

以下示例说明在设置渠道折扣中涉及的任务。

1. 对于本示例，您有一个名为 **Houston** 的渠道，您打算创建名为 **返回学校** 的新折扣。
2. 由于价格和折扣策略包括渠道折扣的可能性，因此在您创建渠道时，您始终创建渠道特定的价格组。
3. 您可以有价格组 **Houston-PG**，它分配给 **Houston** 渠道。
4. 在您创建新的 **返回学校** 折扣后，需要单击 **折扣** 页顶部的 **价格组**。 **折扣价格组** 页将打开。 接下来，单击 **新建**，选择 **Houston-PG** 价格组。
5. 现在您可以启用折扣并将其推送到渠道。

## <a name="additional-resources"></a>其他资源

[价格调整和折扣](price-adjustments-discounts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

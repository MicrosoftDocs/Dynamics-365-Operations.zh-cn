---
title: 订单确认模块
description: 此主题介绍订单确认模块和如何在 Microsoft Dynamics 365 Commerce 中创建该模块。
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698318"
---
# <a name="order-confirmation-module"></a>订单确认模块

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍订单确认模块和如何在 Microsoft Dynamics 365 Commerce 中创建该模块。

## <a name="overview"></a>概览

订单确认模块用于在下订单后在订单确认页面中显示确认消息。 订单确认模块显示结帐期间提供的订单确认编号和客户电子邮件地址。

当结帐期间下订单时，将把订单确认编号和客户电子邮件地址作为页面 URL 中的查询字符串传递到订单确认页。 订单确认模块将收到此信息，并在订单确认页显示订单状态。 订单确认模块需要此页面上下文才能提供订单状态。

## <a name="order-confirmation-module-properties"></a>订单确认模块属性

| 属性名称 | 值 | 说明 |
|---------------|--------|-------------|
| 标题       | 标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**） | 订单确认模块可以有标题。 默认情况下，将 **H2** 标题标记用于标题。 但是，可更改此标记以满足辅助功能要求。 |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a>订单确认页面模块中可以使用的模块 

- **建议** – 可将建议模块放到订单确认页中，以便向客户推荐其他产品。
- **市场营销** – 市场营销模块可以向订单确认页添加市场营销内容。

## <a name="create-an-order-confirmation-page-module"></a>创建订单确认页模块

1. 创建一个名称为**订单确认模板**的页面模板。
1. 在默认页的**主**插槽中，添加一个订单确认模块。
1. 在订单确认模块中，添加一个建议模块。
1. 保存并预览模板。 不应显示此订单确认模块，因为它需要订单确认编号的上下文。
1. 签入模板，然后发布。
1. 使用您刚才创建的订单确认模板创建一个名称为**订单确认页**的页面。
1. 向页面大纲添加默认页。
1. 在**页眉**插槽中，添加一个页眉片段。
1. 在**页脚**插槽中，添加一个页脚片段。
1. 在**主**插槽中，添加一个订单确认模块。
1. 在订单确认模块的属性窗格中，添加标题**订单确认**。
1. 在订单确认模块下，添加一个建议模块，然后将其配置为使用**新品**和**最畅销**设置。
1. 保存并预览页面，签入，然后发布。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[容器模块](add-container-module.md)

[购买框模块](add-buy-box.md)

[购物车模块](add-cart-module.md)

[结帐模块](add-checkout-module.md)

[页眉模块](author-header-module.md)

[页脚模块](author-footer-module.md)

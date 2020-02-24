---
title: 订单详细信息模块
description: 此主题介绍订单详细信息模块和如何在 Microsoft Dynamics 365 Commerce 中使用该模块。
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026009"
---
# <a name="order-details-module"></a>订单详细信息模块


[!include [banner](includes/banner.md)]

此主题介绍订单详细信息模块和如何在 Microsoft Dynamics 365 Commerce 中使用该模块。

## <a name="overview"></a>概览

下订单之后，将使用订单详细信息模块显示订单确认详细信息。 它显示订单确认 ID、订单联系人信息和其他订单详细信息，例如购买的商品、付款信息和装运方式。

## <a name="order-confirmation-module-properties"></a>订单确认模块属性

| 属性名称  | 值 | 说明 |
|----------------|--------|-------------|
| 标题        | 标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**） | 订单确认模块可以有标题。 默认情况下，将 **H2** 标题标记用于标题。 但是，可更改此标记以满足辅助功能要求。 |
| 联系人号码 | 文本 | 可以为与订单相关的问题提供联系人号码。 |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>订单详细信息页面中可以使用的模块

创建订单详细信息页面时，除了订单详细信息模块外，您还可以添加其他相关模块。 下面举了一些示例加以说明：

- **建议模块** – 可将建议模块放到订单详细信息页中，以便向客户推荐其他产品。
- **市场营销模块** – 可以将任何市场营销模块添加到订单详细信息页面以显示市场营销内容。

## <a name="create-an-order-details-page-module"></a>创建订单详细信息页模块

1. 创建一个名称为**订单详细信息模板**的页面模板。
1. 在默认页的**主**插槽中，添加一个订单详细信息模块。
1. 在订单详细信息模块中，添加一个建议模块。
1. 保存并预览模板。 不会显示此订单详细信息模块，因为它需要订单确认编号的上下文。
1. 编辑完模板，然后发布。
1. 使用您刚才创建的订单详细信息模板创建一个名称为**订单详细信息页**的页面。
1. 向页面大纲添加默认页。
1. 在**页眉**插槽中，添加一个页眉片段。
1. 在**页脚**插槽中，添加一个页脚片段。
1. 在**主**插槽中，添加一个订单详细信息模块。
1. 在订单详细信息模块的属性窗格中，添加标题**订单详细信息**。
1. 在订单详细信息模块下，添加一个建议模块，然后将其配置为使用**新品**和**最畅销**设置。
1. 保存并预览页面。
1. 编辑完页面，然后发布。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[容器模块](add-container-module.md)

[购买框模块](add-buy-box.md)

[购物车模块](add-cart-module.md)

[结帐模块](add-checkout-module.md)

[页眉模块](author-header-module.md)

[页脚模块](author-footer-module.md)

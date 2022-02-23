---
title: 订单确认模块
description: 本主题介绍订单确认模块和如何在 Microsoft Dynamics 365 Commerce 中使用它们。
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bf33ebf9c0c5136f40fcd7e1012988d186c4169b
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/07/2020
ms.locfileid: "4410649"
---
# <a name="order-confirmation-module"></a>订单确认模块

[!include [banner](includes/banner.md)]

本主题介绍订单确认模块和如何在 Microsoft Dynamics 365 Commerce 中使用它们。

## <a name="overview"></a>概览

下订单之后，将使用订单确认模块显示订单确认详细信息。 它显示订单确认 ID、订单联系人信息和其他订单详细信息，例如购买的物料、付款信息、提货选项和装运方式。

## <a name="order-confirmation-module-properties"></a>订单确认模块属性

| 属性名称  | 值 | 说明 |
|----------------|--------|-------------|
| 标题        | 标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**） | 订单确认模块可以有标题。 默认情况下，将 **H2** 标题标记用于标题。 但是，可更改此标记以满足辅助功能要求。 |
| 联系人号码 | 文本 | 可以为与订单相关的问题提供联系人号码。 |
| 显示提货时隙信息 | 真或假 | 此属性在 Dynamics 365 Commerce 10.0.15 及更高版本中提供。 当为 true 时，将显示为提货物料提供的提货时隙信息|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a>订单确认页面上可以使用的模块

创建订单确认页面时，除了订单确认模块外，您还可以添加其他相关模块。 下面举了一些示例加以说明：

- **建议模块** – 可将建议模块添加到订单确认页面，以便向客户推荐其他产品。
- **市场营销模块** – 可以将任何市场营销模块添加到订单确认页面以显示市场营销内容。

## <a name="add-an-order-confirmation-module-to-a-page"></a>向页面添加订单确认模块

若要向新页面添加订单确认模块和设置必需的属性，请执行以下步骤。

1. 转到 **模板**，选择 **新建** 创建新模板。
1. 在 **新建模板** 对话框的 **模板名称** 下，输入名称 **订单确认模板**，然后选择 **确定**。
1. 在 **正文** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **默认页面** 模块，然后选择 **确定**。
1. 在 **默认页** 模块的 **主** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **订单确认** 模块，然后选择 **确定**。
1. 选择 **保存**，然后选择 **预览** 预览模板。 不显示此订单确认模块，因为它需要订单确认编号的上下文。
1. 选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。
1. 转到 **页面**，选择 **新建** 创建新页面。
1. 在 **选择模板** 对话框中，选择 **订单确认模板**。 在 **页面名称** 下，输入 **订单确认页面**，然后选择 **确定**。
1. 在 **默认页** 模块的 **主** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **订单确认** 模块，然后选择 **确定**。
1. 在订单确认模块的属性窗格中，选择铅笔符号旁边的 **标题**。
1. 在 **标题** 对话框的 **标题文本** 字段中，输入标题文本 **订单确认**，然后选择 **确定**。
1. 选择 **保存**，然后选择 **预览** 以预览页面。
1. 选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。

## <a name="additional-resources"></a>其他资源

[购物车模块](add-cart-module.md)

[购物车图标模块](cart-icon-module.md)

[结帐模块](add-checkout-module.md)

[付款模块](payment-module.md)

[收货地址模块](ship-address-module.md)

[交付选项模块](delivery-options-module.md)

[提货信息模块](pickup-info-module.md)

[礼品卡模块](add-giftcard.md)

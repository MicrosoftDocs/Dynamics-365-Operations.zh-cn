---
title: 结帐模块
description: 此主题介绍如何向页面添加结帐模块和设置必需的属性。
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bd1d66fc39872019fc38dbbfb56dc3015d57d0dd
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411176"
---
# <a name="checkout-module"></a>结帐模块


[!include [banner](includes/banner.md)]

此主题介绍如何向页面添加结帐模块和设置必需的属性。

## <a name="overview"></a>概览

结帐模块是承载创建订单所需全部模块的特殊容器。 它提供分步流程，供客户输入与采购有关的所有信息。 它捕获送货地址、送货方式和帐单信息。 它还提供订单摘要以及与客户订单相关的其他信息。

结帐模块基于购物车 ID 显示数据。 此购物车 ID 保存为浏览器 cookie。 需要购物车 ID 才能在结帐模块中显示信息，如订单中的项、总量和折扣。 

下图显示了结帐页上的 Fabrikam 结帐模块的示例。

![结帐模块的示例](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a>结帐模块属性

结帐模块显示订单摘要，并提供下达订单的功能。 为了收集下达订单之前所需的所有客户信息，必须将其他模块添加到结帐模块。 因此，零售商可以根据自己的需求灵活地将自定义模块添加到结帐流程，或排除模块。

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>结帐模块中可使用的模块

- **装运地址** – 客户可使用此模块为订单添加或选择装运地址。 如果客户已登录，则显示以前为该客户保存的所有地址。 然后，客户可在这些地址中进行选择。 客户也可以添加新地址。 装运地址用于订单中需要装运的所有项。 不能针对单个明细项进行自定义。 将针对每个国家或地区定义装运地址格式，而该模块则实施国家/地区特定的规则。 虽然此模块不提供地址验证，但是可以通过自定义设置来实施地址验证。 如果订单中仅包含将在商店提货的项，则自动隐藏此模块。

    下图显示了结帐页上的装运地址模块的示例。

    ![装运地址模块示例](./media/ecommerce-shippingaddress.PNG)

- **交货选项** – 客户可使用此模块为订单选择交货选项。 交货选项基于装运地址。 如果更改装运地址，则必须重新检索交货选项。 如果订单中仅包含将在商店提货的项，则自动隐藏此模块。

    下图显示了结帐页上的交货选项模块的示例。

    ![交付选项模块示例](./media/ecommerce-deliveryoptions.PNG)

- **结帐分区容器** – 此模块是可在其中放置多个模块以在结帐流程中创建分区的容器。 例如，可以将所有与付款有关的模块放在此容器内，以便使其显示为一个分区。 此模块仅影响流程的布局。
- **礼品卡** – 客户可通过此模块使用礼品卡支付订单。 它仅支持 Microsoft Dynamics 365 Commerce 礼品卡。 可以为一个订单应用一张或多张礼品卡。 如果礼品卡的余额不足以支付购物车中的金额，可以将礼品卡与其他付款方式结合使用。 仅当客户已登录，才能兑换礼品卡。
- **积分** – 客户可通过此模块使用积分支付订单。 它提供可用积分和到期积分的摘要，并可供客户选择要兑换的积分数。 如果客户未登录或不是会员，或者如果购物车中的总金额为 0（零），将自动隐藏此模块。
- **付款** – 客户可通过此模块使用信用卡支付订单。 如果积分或礼品卡足以支付购物车中的总金额或总金额为 0（零），将自动隐藏此模块。 Adyen 付款连接器针对此模块提供信用卡集成。 有关如何使用此连接器的详细信息，请参阅[适用于 Adyen 的 Dynamics 365 付款连接器](dev-itpro/adyen-connector.md)。
- **记帐地址** – 此模块可供客户提供记帐信息。 此信息和信用卡信息一起由 Adyen 使用。 此模块中有一个选项供客户将其记帐地址用作装运地址。

    下图显示了结帐页面上的礼品卡、会员积分、付款和帐单地址模块的示例。

    ![礼品卡、会员积分、付款和帐单地址模块的示例](./media/ecommerce-payments.PNG)

- **联系信息** – 此模块可供客户为订单添加或更改联系信息（电子邮件地址）。

- **文本块** – 此模块中包含内容管理系统 (CMS) 驱动的所有消息。 例如，可能包含消息“订单问题请致电 1-800-Fabrikam”。 

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit 交互

大多数结帐信息（如装运地址和装运方式）存储在购物车中，并作为订单的一部分处理。 唯一例外是信用卡信息。 此信息直接使用 Adyen 付款连接器处理。 将为付款授权，但不收费。

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a>向页面添加结帐模块和设置必需的属性

若要向新页面添加结帐模块和设置必需的属性，请执行以下步骤。

1. 转到**页面片段**，选择**新建**创建新片段。
1. 在**新建页面片段**对话框中，选择**结帐**模块。
1. 在**页面片段名称**下，输入名称**结帐片段**，然后选择**确定**。
1. 选择**结帐模块**插槽。
1. 在右侧的属性窗格中，选择铅笔符号，在字段中输入标题文本，然后选择复选标记符号。
1. 在**结帐信息**插槽中，选择省略号 (**...**)，然后选择**添加模块**。
1. 在**添加模块**对话框中，选择**装运地址**、**交付选项**、**结帐部分容器**和**联系人信息**模块，然后选择**确定**。
1. 在**结帐部分容器**模块，选择省略号 (**...**)，然后选择**添加模块**。
1. 在**添加模块**对话框中，选择**礼品卡**、**会员**和**付款**模块，然后选择**确定**。 这样，就可以确保所有付款方式在一个分区中一起显示。
1. 选择**保存**，然后选择**预览**预览片段。 预览中可能不显示某些没有购物车上下文的模块。
1. 选择**完成编辑**签入片段，然后选择**发布**进行发布。
1. 创建一个使用新结帐片段的模板。
1. 创建一个使用新模板的结帐页。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[容器模块](add-container-module.md)

[购买框模块](add-buy-box.md)

[购物车模块](add-cart-module.md)

[订单确认模块](order-confirmation-module.md)

[页眉模块](author-header-module.md)

[页脚模块](author-footer-module.md)

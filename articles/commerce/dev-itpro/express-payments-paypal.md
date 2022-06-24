---
title: 配置 PayPal 快速付款
description: 本文介绍如何为 PayPal 配置快速付款，以在 Microsoft Dynamics 365 Commerce 中启用更快的结帐功能。
author: BrianShook
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: b69b7384992fb86370ff6881824a7d2c9a77d2c4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905274"
---
# <a name="configure-express-payments-for-paypal"></a>配置 PayPal 快速付款

[!include [banner](../includes/banner.md)]

本文介绍如何为 PayPal 配置快速付款，以在 Microsoft Dynamics 365 Commerce 中启用更快的结帐功能。

## <a name="key-terms"></a>重要术语

| 条款 | Description |
|---|---|
| PayPal 钱包 | PayPal 连接器支持的客户体验和集成。 它也称为 PayPal 按钮。 |
| 电子钱包 | 一种不包含传统付款特征的付款类型，例如用于区分信用卡和借记卡类型的银行标识号 (BIN) 范围和到期日期。 |
| 快速付款 | 使用支持的付款方式时支持更快结帐行为的 Commerce 模块。 本文介绍如何使用 PayPal 快速付款模块。 |

Dynamics 365 Commerce 为 PayPal 钱包提供了现成的集成。 配置了面向 PayPal 的 Dynamics 365 Payment Connector 后，PayPal 按钮在联机订单结帐期间会显示为一种可选的付款方式。 当用户选择 PayPal 时，会指示他们直接通过 PayPal 完成付款，然后返回到在线店面以完成其订单。 利用 PayPal 购物车结帐功能，客户可以使用其付款帐户信息预先填写结帐表格，以便他们可以更快地完成结帐流程。

Commerce 已添加快速付款模块以方便快速结帐。 快速付款模块可用于可包含在结帐或购物车页面上的片段中。 配置 PayPal 后，面向 PayPal 的 Dynamics 365 Payment Connector 的相同连接器引用将用于快速付款选项和常规结帐选项。

## <a name="paypal-checkout-in-commerce"></a>Commerce 中的 PayPal 结帐

### <a name="prerequisites"></a>先决条件

为您的环境设置 PayPal 钱包，如[面向 PayPal 的 Dynamics 365 Payment Connector](../paypal.md) 中所述。

如果您在常规结帐流（用户手动输入他们的帐户信息而不使用付款快速预填充操作）中使用 PayPal 作为一个选项，请按照[付款模块](../payment-module.md)中的设置说明进行操作。

### <a name="payment-express-module-with-paypal"></a>PayPal 快速付款模块

快速付款模块将与支持的付款方式搭配使用，通过在结帐过程中预填写站点客户付款服务帐户信息，为站点客户提供更快结帐的选项。 快速付款模块使用配置的支付连接器在结帐表单中预先填写用户帐户详细信息，例如地址、联系信息和选择的付款方式。

使用 PayPal 快速结帐功能，并且用户在结帐页面的快速付款部分中选择 PayPal 按钮时，将打开 PayPal 付款 iFrame 窗口。 然后，用户登录到他们的 PayPal 帐户，以使用他们的帐户送货地址、帐单邮寄地址、电子邮件地址和选择的 PayPal 付款方式来支付交易费用。

用户在 PayPal 窗口中完成操作后，他们将返回到 Commerce 站点结帐页面，在该页面中，结帐表单已预先填写了他们选择的详细信息。 在快速付款流中，将为用户预先填写返回的送货地址可用的第一个送货选项。 然后，用户可以选择查看订单并更改结帐订单详细信息，然后再选择 **下达订单** 以完成订单。

### <a name="add-the-payment-express-module-with-paypal-to-a-fragment"></a>将 PayPal 快速付款模块添加到片段中

要在 Commerce 站点生成器中将 PayPal 快速付款模块添加到片段中，请执行以下步骤。

1. 导航到您的站点。
1. 在右侧导航窗格中，选择 **片段**，然后选择 **新建**。
1. 在 **新片段** 对话框中，查找并选择 **快速付款** 模块，然后在 **片段名称** 下，输入片段的名称（例如，**快速结帐**）。
1. 选择 **确定** 以创建片段。
1. 在大纲视图中，选择您创建的快速付款模块的插槽。
1. 在属性窗格中，选择 **标题**。
1. 在 **标题** 对话框内的 **标题文本** 字段中，输入您要为站点快速结帐部分显示的标题文本（例如 **快速结帐**）。
1. 在 **标题级别** 下面，选择标题级别（例如 **H2**）。
1. 选择 **确定**。
1. 在属性窗格内的 **iFrame 的高度** 字段中，输入或调整 iFrame 元素的高度（例如 **60**）。
1. 在 **支持的支付方式** 字段中，输入 **PayPal**。
1. 选择 **保存**，选择 **完成编辑** 签入片段，然后选择 **发布** 进行发布。

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>将快速付款片段添加到结帐页面

若要在站点生成器中将快速付款片段添加到结帐页面，请执行以下步骤。

1. 导航到您的站点。
1. 在左侧导航窗格中，选择 **页面**，然后选择站点的结帐页面。
1. 选择 **编辑** 以编辑页面。
1. 在 **主要** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **选择模块** 对话框中，选择 **容器** 模块，然后选择 **确定**。

    > [!NOTE]
    > 如果包含结帐片段的容器模块已存在，请移动快速付款部分，使其显示在 **主要** 插槽中现有结帐容器的上方。 然后，快速付款部分将呈现在普通结帐容器上方。 若要上下移动容器模块，请选择省略号 (**...**)，然后选择 **上移** 或 **下移**。

1. 在 **容器** 属性窗格中，我们建议您按以下方式配置属性设置：

    - **容器布局** - 选择 **堆积**。
    - **宽度** - 选择 **填充容器**。
    - **显示的子项** - 选择 **三个**。

1. 在 **容器** 插槽中，选择省略号 (**...**)，然后选择 **添加片段**。
1. 在 **选择片段** 对话框中，查找并选择您创建的快速付款片段，然后选择 **确定**。
1. 选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>将快速付款片段添加到购物车页面

若要在站点生成器中将快速付款片段添加到购物车页面，请执行以下步骤。

1. 导航到您的站点。
1. 在左侧导航窗格中，选择 **页面**，然后选择站点的购物车页面。
1. 选择 **编辑** 以编辑页面。
1. 在 **主要** 插槽中，查找包含 **购物车** 模块的容器。 **购物车** 模块将包含 **快速付款** 插槽。
1. 选择 **快速付款** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **选择模块** 对话框中，选择 **快速付款** 模块，然后选择 **确定**。
1. 在属性窗格内的 **支持的支付方式** 字段中，输入 **Paypal**。
1. 选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。

### <a name="modes-of-delivery"></a>交货模式

当快速付款模块配置为使用 PayPal 时，将预先填写针对为 PayPal 帐户选择的送货地址返回的第一个送货选项。 用户可以根据需要更改送货地址。

交货模式的顺序在 Commerce Headquarters 中渠道的 **交货模式** 部分中进行配置。 有关详细信息，请参阅[设置交货方式](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)。

结帐模块还将在结账期间呈现交货模式时使用交货选项模块。 有关详细信息，请参阅[交货选项模块](../delivery-options-module.md)。

交货模式将添加到 Commerce Headquarters 内的在线商店列表中。 转到 **Retail 和 Commerce \> 渠道 \> 在线商店**，然后为您的商店选择渠道 ID。 然后选择 **设置 \> 交货模式**。 将在站点上以类似方式显示在配置中显示的模块交货模式。 若要添加或删除零售渠道或产品的交货模式，请在“操作”窗格上选择 **管理交货模式**。

## <a name="additional-resources"></a>其他资源

[付款常见问题](payments-retail.md)

[结帐模块](../add-checkout-module.md)

[付款模块](../payment-module.md)

[设置交货模式](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[交付选项模块](../delivery-options-module.md)

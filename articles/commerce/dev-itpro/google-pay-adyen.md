---
title: 配置 Google Pay 与 Adyen
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中配置 Google Pay 和 Adyen。
author: BrianShook
ms.date: 07/05/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: cdf950fc7b3720543d93e108d4e3c3c2ab254e09
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838383"
---
# <a name="configure-google-pay-with-adyen"></a>配置 Google Pay 与 Adyen

[!include [banner](../includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中配置 Google Pay 和 Adyen。

在使用 Adyen 付款网关服务时，Dynamics 365 Commerce 会为 Google Pay 提供现存的集成。 Google Pay 是一种数字钱包付款方式，它使用 Google Pay 商家帐户并与 Adyen 支付服务相协调。 配置后，Google Pay 按钮可在联机订单结账期间用作可选付款方式。 当用户在支持的浏览器或设备中选择 **Google Pay** 时，将指示他们直接通过 Google Pay 服务完成付款。 然后，他们将返回到在线店面以完成订单。

将 Google Pay 与 Commerce 中的快速结账模块一起使用时，用户的付款账户信息会自动预填充到结账表单中，以帮助用户更快地完成结账流程。 Commerce 包含一个快速付款模块，可实现快速结账行为。 快速付款模块可用于包含在结帐或购物车页面上的片段中。 配置 PayPal 后，除了使用面向 Adyen 的 Dynamics 365 Payment Connector 之外，还使用面向 Google Pay 的 Dynamics 365 Payment Connector 的连接器引用，以启用快速付款和定期结帐选项。 还可以为 Google Pay 配置 Adyen 付款终端和 Commerce 销售点 (POS) 以供店内使用。

## <a name="key-terms"></a>重要术语

| 条款 | Description |
|---|---|
| Google Pay | Google Pay 又称 Google Pay“按钮”，是一种通过 Adyen 连接器支持的钱包付款服务。 它可以实现 Dynamics Google Pay Connector 支持的客户体验和集成。 |
| 电子钱包 | 一种不包含传统付款特征的付款类型，例如用于区分信用卡和借记卡类型的银行标识号 (BIN) 范围和到期日期。 |
| 快速付款模块 | 一个通过支持的付款方式支持更快结帐行为的 Dynamics 365 Commerce 模块。 |

## <a name="prerequisites"></a>先决条件

在 Commerce 中使用 Google Pay 与 Adyen 需要 Google 商家帐户。 有关如何设置 Google 商家帐户的信息，请参阅 [Google Pay 上的 Adyen 文档](https://docs.adyen.com/payment-methods/google-pay/)和 Google 的[集成核对清单](https://developers.google.com/pay/api/web/guides/test-and-deploy/integration-checklist)。

Google 付款方式还必须与您的 Adyen 帐户集成。 有关集成链接说明，请参阅 [Adyen Google Pay](https://www.adyen.com/payment-methods/google-pay)。

您还必须在 Dynamics 365 Commerce Headquarters 中启用增强型钱包功能。 转到 **工作区 \> 功能管理**，搜索 **增强型钱包支持和付款改进** 功能，选择该功能，然后选择 **启用**。 启用此功能后，运行 **1110** 分发计划以使更改在所有渠道中都可用。

## <a name="map-the-google-pay-payment-method"></a>映射 Google Pay 付款方式

Google Pay 是一种数字钱包付款方式。 有关如何设置 Google Pay 付款映射的信息，请参阅[钱包付款支持](../wallets.md)。

若要将 Google Pay 付款方式映射到 POS 和在线渠道的卡支付方式，请按照以下步骤操作。

1. 在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> 渠道设置 \> 付款方式 \> 卡类型**。
1. 选择 **新建** 以为 Google Pay 添加行。
1. 在 **ID** 字段中，输入 **GooglePay**。
1. 在 **电子付款名称** 字段中，输入 **Google Pay**。
1. 在 **类型** 字段中，输入 **钱包**。
1. 在 **签发方** 字段中，输入 **Google**。
1. 在操作窗格上，选择 **处理器映射** 以打开 **处理器付款映射方法** 对话框。
1. 在 **未映射的处理器付款方式** 下面，您将看到未映射的处理器付款方式的列表，每个付款方式都与适当的连接器配对。 若要将未映射的 Google Pay 处理器付款方式映射到卡支付方式，请按照以下步骤对每种卡支付方式执行以下步骤：

    1. 在 **卡支付方式** 下面，选择卡支付方式。
    1. 在 **未映射的处理器付款方式** 列中，选择 **面向 Adyen 的 Dynamics 365 Payment Connector** 连接器（供在 POS 上使用）和 **面向 Google Pay 的 Dynamics 365 Payment Connector** 连接器（供在线渠道使用）。
    1. 选择 **添加**。 选定内容将添加到 **映射的处理器付款方式** 列。

1. 当您映射完付款方式时，选择 **保存**。
1. 在 **卡类型** 页面上，选择 **保存**。

## <a name="configure-a-commerce-online-store-for-google-pay"></a>为 Google Pay 配置 Commerce 在线商店

若要配置 Commerce 在线商店以使用 Google Pay，请执行以下步骤。

1. 在 Commerce headquarters 中，转到 **Retail 和 Commerce \> 渠道 \> 在线商店**。
1. 通过选择渠道的 **零售渠道 ID** 值来选择站点的在线商店渠道。
1. 在 **付款帐户** 快速选项卡上的 **连接器** 下面，确认已列出 **面向 Adyen 的 Dynamics 365 Payment Connector** 连接器。 如果未列出它，请按照[设置面向 Adyen 的 Dynamics 365 Payment Connector](adyen-connector-setup.md) 中的说明进行添加。

    > [!NOTE]
    > 在大多数情况下，**面向 Adyen 的 Dynamics 365 Payment Connector** 连接器必须列为渠道的第一个连接器（第一个连接器也称为主要连接器）。 在它之后，必须列出将使用的其他连接器，例如 **面向 PayPal 的 Dynamics 365 Payment Connector** 和 **面向 GooglePay 的 Dynamics 365 Payment Connector** 连接器。

1. 添加了 **面向 Adyen 的 Dynamics 365 Payment Connector** 连接器后，选择 **添加**，以添加 **面向 GooglePay 的 Dynamics 365 Payment Connector** 连接器。 然后为连接器设置以下属性。

    | 字段                  | Description | 必填 | 自动设置 | 示例值 |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | 程序集名称          | 面向 GooglePay 的 Dynamics 365 Payment Connector 的程序集的名称。 | 是 | 是 | *二进制名称* |
    | 服务帐户 ID     | 商家属性设置的唯一标识符。 此标识符印在支付交易上，并标识下游流程（例如开票）应使用的商家属性。 | 是 | 是 | *GUID* |
    | Google 商家 ID     | 输入分配给您的 Google 商家帐户的 Google 商家 ID。 生产环境需要此属性，但对于测试环境是可选的。 有关详细信息，请访问 <https://pay.google.com/>。 | 是 | 否 | *数字标识符* |
    | 商户帐户 ID    | 输入唯一的 Adyen 商家标识符。 当您按照[向 Adyen 注册](adyen-connector-setup.md#sign-up-with-adyen)中的描述向 Adyen 注册时，会提供此值。 | 是 | 否 | *商家标识符* |
    | 云 API 密钥          | 输入 Adyen 云 API 密钥。 若要获取此密钥，请按照[如何获取 API 密钥](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key)中的说明操作。 | 是 | 否 | "abcdefg" |
    | 网关环境    | 要映射到的 Adyen 网关环境。 可能的值为 **测试** 和 **实时**。 您应该仅为生产设备和交易将此字段设置为 **实时**。 | 是 | 是 | “实时” |
    | 支持的货币   | 连接器应处理的货币。 在卡存在的情况下，将交易请求发送到付款终端后，Adyen 可以通过[动态货币转换](https://www.adyen.com/pos-payments/dynamic-currency-conversion)支持其他货币。 联系 Adyen 支持部门以获取支持的货币列表。 | 是 | 是 | "USD;EUR" |
    | 支持的支付方式 | 连接器应处理的支付方式。 | 是 | 是 | "GooglePay" |

1. 设置完连接器属性后，运行 **1070（渠道配置）** 分发计划作业。


### <a name="use-the-payment-express-module-with-google-pay"></a>将快速付款模块与 Google Pay 搭配使用

Commerce 快速付款模块将与支持的付款方式搭配使用，通过在结帐过程中使用站点客户付款服务帐户信息，为站点客户提供更快结帐的选项。 快速付款模块引用配置的连接器按钮，并返回用户选择的订单详细信息（地址、联系信息和付款方式）以预填写结帐表单。

将快速付款模块与 Google Pay 一起使用时，如果客户在 **快速付款** 部分中选择 Google Pay 按钮，则会打开 Google Pay iframe 窗口。 以后，用户可以登录到他们的 Google 帐户，以使用他们的帐户送货地址、帐单邮寄地址、电子邮件地址和选择的 Google Pay 付款方式来支付交易费用。

当用户在 Google Pay 窗口中完成操作时，他们将返回到 Commerce 站点结帐页面，在该页面中，结帐表单已预先填写了他们的 Google Pay 帐户详细信息。 用户从 Google Pay 窗口返回到结帐页面后，他们将看到以下详细信息：

- 在快速付款流中，将为客户预先选择返回的送货地址可用的第一个送货选项。
- 使用 Google Pay 后，不会返回联系人电子邮件地址。 来宾结帐用户必须在结帐页面的联系人部分中输入电子邮件地址。 登录的用户将从他们的 Dynamics 客户帐户（他们用于身份验证的主要电子邮件地址）中自动填写他们的联系数据。

客户可以选择查看订单并更改结帐订单详细信息，然后再选择 **下达订单** 以完成订单。

### <a name="configure-google-pay-in-site-builder"></a>在站点生成器中配置 Google Pay 

在配置 Google Pay 片段或页面之前，您必须确保在 Commerce 站点生成器中设置了站点的内容安全策略。

若要确保在站点生成器中设置您的内容安全策略，请按照以下步骤操作。

1. 在您的站点中，转到 **站点设置 \> 扩展**。
1. 在 **内容安全策略** 选项卡上，针对 `*.google.com` 向 **child-src**、**connect-src**、**frame-ancestors**、**frame-src**、**img-src**、**script-src** 和 **style-src** 指令添加一行。
1. 当您完成时，选择 **保存并发布**。

### <a name="configure-the-payment-express-fragment-with-google-pay-in-site-builder"></a>在站点生成器中配置 Google Pay 的快速付款片段

若要设置 Google Pay 的快速付款片段，请按照以下步骤操作。

1. 在站点生成器中，转到 **片段**。
1. 选择 **新建**。
1. 在 **新建片段** 对话框中，选择 **容器** 模块，输入片段名称（例如 **快速结帐**），然后选择 **确定**。 
1. 选择新片段的 **默认容器** 插槽。
1. 在右侧的属性窗格中，设置容器模块的属性：

    - **标题** - 输入要为您网站的快速结帐部分显示的标题（例如 **快速结帐**）。
    - **容器布局** - 选择 **流**。
    - **宽度** - 选择 **填充容器**。
    - **显示的子项** - 选择 **三**，以指定结帐页面的快速结帐部分（例如，文本框、PayPal 快速付款和 Google Pay 快速付款）的一行中可容纳的子项数量。
    - **CSS 类名称** - 输入 **msc-express-payment-container**（必需）。

    > [!IMPORTANT]
    > - **CSS 类名称** 值必须设置为 **msc-express-payment-container**，才能在结帐期间控制容器的行为。 此行为包括隐藏、折叠和其他在结帐流期间应用于快速结帐部分的操作。 **msc-express-payment-container** 类使用与模块库结帐模块一起发布的默认操作。
    > - 可以根据 **CSS 类名称** 包含其他样式。 如果您自定义模块的行为，并且将结帐模块中相同的模块库编码行为用作快速结帐行为，请交叉检查样式控件。

1. 在 **默认容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **选择模块** 对话框中，选择 **快速付款** 模块，然后选择 **确定**。
1. 在 **快速付款** 模块属性窗格中，输入或调整以像素为单位的 **iFrame 的高度** 值（例如 **60**）。
1. 在 **支持的支付方式** 字段中，输入 **GooglePay**。 该值必须与连接器中为渠道设置的 **支持的支付方式** 字符串匹配（如本文前面的[为 Google Pay 配置 Commerce 在线商店](#configure-a-commerce-online-store-for-google-pay)部分中所述）。

    > [!NOTE]
    > 您可以重复步骤 6 到 9 以添加其他付款方式的 **快速付款** 模块。 将 **支持的支付方式** 值与其他已配置的付款类型（例如 **Paypal**）保持一致。

1. 可选：您可以将文本块模块添加到默认容器模块以包含说明或披露信息。 添加模块后，在属性窗格内的 **富文本** 字段中输入所需的文本。 您可以通过选择 **文本块** 插槽中的省略号 (**...**)，然后选择 **上移** 或 **下移**，将文本放在快速付款模块的上方或下方。
1. 选择 **保存** 以保存您更改，然后选择 **完成编辑**。
1. 选择 **发布** 发布此片段。

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>将快速付款片段添加到结帐页面

若要将快速付款片段添加到结帐页面，请执行以下步骤。

1. 在站点生成器中，转到 **页面**，然后选择站点的结帐页面。
1. 选择 **编辑**。
1. 在 **主要插槽** 中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **选择模块** 对话框中，选择 **容器** 模块，然后选择 **确定**。
1. 在右侧的属性窗格中，设置容器模块的属性：

    - **容器布局** - 选择 **堆积**。
    - **宽度** - 选择 **填充容器**。
    - **显示的子项** - 选择 **三**，以指定结帐页面的快速结帐部分（例如，文本框、PayPal 快速付款和 Google Pay 快速付款）的一行中可容纳的子项数量。

1. 在 **容器** 模块插槽中，选择省略号 (**...**)，然后选择 **添加片段**。
1. 在 **选择片段** 对话框中，选择您创建的快速付款片段，然后选择 **确定**。
1. 选择 **保存** 以保存您更改，然后选择 **完成编辑**。
1. 选择 **发布** 发布此页面。

> [!NOTE]
> 如果结帐页面已经包含一个具有结帐片段的容器，并且您希望将快速支付模块呈现在普通结帐容器之上，则可以选择 **主要插槽** 中的省略号 (**...**)，然后选择 **上移** 或 **下移**，将其放在现有结帐的上方或下方。

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>将快速付款片段添加到购物车页面

若要将快速付款片段添加到购物车页面，请执行以下步骤。

1. 在站点生成器中，转到 **页面**，然后选择站点的购物车页面。
2. 选择 **编辑**。
3. 在大纲视图中，展开树视图中的 **主插槽**，并查找包含 **购物车** 模块的容器。
4. 在 **购物车** 模块中，选择 **快速付款** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。
5. 在 **选择模块** 对话框中，选择 **快速付款** 模块，然后选择 **确定**。
6. 选择 **快速付款** 模块插槽。 然后，在右侧的属性窗格中，在 **支持的支付方式** 下面，输入 **GooglePay**。 该值必须与连接器中为渠道设置的 **支持的支付方式** 字符串匹配（如本文前面的[为 Google Pay 配置 Commerce 在线商店](#configure-a-commerce-online-store-for-google-pay)部分中所述）。
1. 选择 **保存** 以保存您更改，然后选择 **完成编辑**。
1. 选择 **发布** 发布此页面。

用户最多可在购物车 **快速付款** 插槽中包括三个受支持的 **快速付款** 模块（换句话说，包含三个可用的受支持付款选项）。

### <a name="set-up-google-pay-as-an-option-in-the-checkout-payment-section"></a>在结帐付款部分中将 Google Pay 设置为选项

您可以在结帐付款部分中将 Google Pay 设置为纯付款非快速功能的一个选项。 此结帐窗体将由用户填写，Google Pay 付款页面将仅为 Google Pay 的付款准备结帐。 Google 帐户信息将不可用于覆盖填写的结帐详细信息。

> [!NOTE]
> 以下过程假定您的站点使用一个配置有提货信息、装运地址、交货选项、联系信息、可选条款和条件以及结帐元素部分的结帐片段。 默认模块库结帐模块通过包含文本块、会员积分、礼品卡和付款模块的结帐部分容器发布。 有关详细信息，请参阅[付款模块](../payment-module.md)。

若要在结帐页面的 **付款方式** 部分中将 Google Pay 设置为常规付款选项，请按照以下步骤操作。

1. 在站点生成器中，转到 **片段**，然后选择站点的结帐片段。
1. 选择 **编辑**。
1. 在 **结帐信息** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **选择模块** 对话框中，选择 **付款** 模块，然后选择 **确定**。
1. 在右侧的 **付款** 模块属性窗格中，设置容器模块的属性：

    - **标题** - 输入要为您网站的快速结帐部分显示的标题（例如 **Google Pay**）。
    - **iFrame 的高度** - 将此值更改为以像素为单位的首选设计高度（例如 **75**）。 
    - **支持的支付方式** - 输入 **GooglePay** 以匹配 Commerce Headquarters 中 Google Pay 连接器配置。
    - **是主要付款** - 请清除此复选框。 （通常为 Adyen 结帐模块启用了此属性。）
    - **付款样式替代** - Google Pay 配置不支持此属性。
    - **使用连接器 ID** - 如果页面上使用了多个付款连接器，则必须选择此属性。

1. 通过选择 **付款** 插槽中的省略号 (**...**)，然后选择 **上移** 或 **下移**，将此模块放在其他付款模块的上方或下方。
1. 选择 **保存** 以保存您更改，然后选择 **完成编辑**。
1. 选择 **发布**。

### <a name="modes-of-delivery"></a>交货模式

对于使用 Google Pay 的快速付款模块，将预先选择针对从 Google Pay 帐户中选择的送货地址返回的第一个交货选项。 用户有机会将装运地址调整为其他选项（如果需要）。

在 Commerce Headquarters 的渠道 **交货方式** 页面上配置了在快速付款模块中显示交货方式的顺序。 在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> 渠道 \> 在线商店**，并为您的商店选择 **零售渠道 ID** 值。 在“操作”窗格上的 **设置** 选项卡中，选择 **交货方式**。 列出的送货方式将在快速付款模块中以相同顺序显示。 在“操作”窗格上选择 **管理交货模式**，以添加或删除零售渠道或产品的交付方式。 有关如何设置交货方式的详细信息，请参阅[设置交货方式](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)。

结帐模块还在结帐期间呈现交货模式时使用交货选项模块。 有关详细信息，请参阅[交货选项模块](../delivery-options-module.md)。

交货方式在添加到在线商店中的 **交货方式** 列表时显示。

## <a name="configure-commerce-pos-for-google-pay"></a>为 Google Pay 配置 Commerce POS

POS 配置将硬件配置文件的 **EFT 服务** 字段的设置用于面向 Adyen 的 Dynamics 365 Payment Connector。 有关如何在 Commerce Headquarters 中为面向 Adyen 的 Dynamics 365 Payment Connector 配置电子资金转移 (EFT) 服务的信息，请参阅[设置 Dynamics 365 POS 硬件配置文件](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile)。

Adyen 连接器的处理器映射捕获 Google Pay 在 POS 终端上使用的钱包卡类型。

## <a name="additional-resources"></a>其他资源

[付款常见问题](payments-retail.md)

[结帐模块](../add-checkout-module.md)

[付款模块](../payment-module.md)

---
title: 在 Dynamics 365 Commerce 中使用 Adyen 设置 Apple Pay
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中使用 Adyen 设置 Apple Pay。
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: 0949b9d7a4b181605d43956932b4fc095940bd64
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780349"
---
# <a name="set-up-apple-pay-with-adyen-in-dynamics-365-commerce"></a>在 Dynamics 365 Commerce 中使用 Adyen 设置 Apple Pay

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中使用 Adyen 设置 Apple Pay。

## <a name="key-terms"></a>重要术语

| 条款 | Description |
|---|---|
| Apple Pay | Apple Pay 又称 Apple Pay“按钮”，是一种通过 Adyen 连接器支持的钱包付款服务。 它可以实现 Microsoft Dynamics 365 Apple Pay 连接器支持的客户体验和集成。 |
| 电子钱包 | 一种不包含传统付款特征的付款类型，例如用于区分信用卡和借记卡类型的银行标识号 (BIN) 范围和到期日期。 |

在使用 Adyen 付款网关服务时，Dynamics 365 Commerce 会为 Apple Pay 提供现存的集成。 Apple Pay 是一种数字钱包付款方式，它使用 Apple Pay 商家帐户并与 Adyen 支付服务相协调。 配置后，Apple Pay 按钮将成一种可选择的付款方式，是在线商店订单结帐页面的一部分。 Apple Pay 按钮仅作为受支持的 Apple Pay 设备的付款选项显示。 当用户在支持的浏览器或设备中选择 **Apple Pay** 时，将被定向到 Apple Pay 服务直接完成付款。 然后，他们将返回到在线店面完成订单。

除了适用于 Adyen 的 Dynamics 365 付款连接器外，还使用适用于 Apple Pay 的 Dynamics 365 付款连接器的连接器引用在站点上支持 Apple Pay 和信用卡付款。 另外还可以将 Apple Pay 配置为在具有 Adyen 付款终端的商店中使用，这些终端将适用于 Adyen 的 Dynamics 365 付款连接器与商业销售点 (POS) 结合使用。 在这种情况下，适用于 Adyen 的 Dynamics 365 付款连接器通过终端处理 Apple 付款设备点击。

## <a name="prerequisites"></a>先决条件

在 Commerce 中通过 Adyen 使用 Apple Pay 需要 Apple 商家帐户。 有关如何在您的测试客户区域设置 Apple Pay 的信息，请参阅 [Apple Pay 插件集成](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#set-up-apple-pay)。 有关准备好在生产环境中上线时应完成哪些事项的信息，请参阅[上线](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live)。

Apple 付款方式还必须与您的 Adyen 帐户集成。 Adyen 可以帮助您设置付款方式，还可以帮助确保您将使用证书的域被指定可通过证书使用。

要在 Commerce headquarters 中启用增强型钱包功能标志，转到 **工作区 \> 功能管理**，搜索 **增强型钱包支持和付款改进** 功能。 选择此功能，然后然后选择 **启用**。 启用此功能后，运行 **1110** 分发计划以使更改在所有渠道中都可用。

## <a name="map-the-apple-pay-payment-method"></a>映射 Apple Pay 付款方式

Apple Pay 是一种数字钱包付款方式。 有关如何设置 Apple Pay 付款映射的信息，请参阅[钱包付款支持](../wallets.md)。

要在 Commerce headquarters 中映射 Apple Pay 付款方式，请按照下列步骤操作。

1. 转到 **Retail 和 Commerce \> 渠道设置 \> 付款方式 \> 卡类型**。
1. 选择 **新建** 为 Apple Pay 添加一行，然后设置以下值：

    - **ID：** ApplePay
    - **电子支付名称：** Apple Pay
    - **类型：** 电子钱包
    - **发行商：** Apple

1. 选择 **处理器映射** 打开 **处理器付款映射方法** 对话框。 **未映射的处理器付款方式** 列将列出每个可用连接器（Adyen、PayPal 和 Apple）支持的付款方式。
1. 为 **适用于 Adyen 的 Dynamics 365 付款连接器** 连接器（用于 POS）和 **适用于 Apple Pay 的 Dynamics 365 付款连接器** 连接器（用于在线渠道）映射所需的支持付款方式。
1. 对于每个映射行，在 **未映射的处理器付款方式** 列中，选择要支持的行，然后选择 **添加** 将选择的行移动到 **映射的处理器付款方式** 列。
1. 选择 **确定**，然后在 **卡类型** 页面上，选择 **保存**。

## <a name="set-up-the-apple-pay-certificate-for-your-site"></a>为您的站点设置 Apple Pay 证书

对于每个站点，您必须按照 [Adyen Apple Pay 文档](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live)中的说明上载域关联文件（也称为 Apple Pay 证书）。 您可以使用 Commerce 站点构建器将域关联文件上载到您的站点的媒体库。

要在站点构建器中设置 Apple Pay 证书，请按照下列步骤操作。

1. 从 [Adyen](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live) 下载证书（域关联文件）。
1. 为域关联文件添加 .txt 扩展名。
1. 在站点构建器中，将域关联文件[上载](../upload-serve-static-files.md)到您的站点的媒体库。
1. 转到 **URL**。
1. 选择 **新建 \> 新建 URL**。
1. 在 **新建 URL** 对话框中，选择 **媒体库资产**。
1. 在 **URL 路径** 字段中，输入 URL 路径（如果尚未输入）。 在域基 URL 之后，输入以下必需的 Apple 字符串：`<domain>/.well-known/apple-developer-merchantid-domain-association.txt`。
1. 选择 **下一步**。 媒体库将显示所有上载的 **文档** (.txt) 类型的媒体资产。
1. 选择应为您先前定义的对 URL 的请求提供的域关联文件。
1. 选择 **创建**。

此时，您创建的 URL 处于草稿状态。 发布 URL，完成设置过程。 在您发布 URL 之前，URL 指向的文件不会返回。

## <a name="configure-a-commerce-online-store-for-apple-pay"></a>为 Commerce 在线商店配置 Apple Pay

要为 Commerce 在线商店配置 Apple Pay，请执行以下步骤。

1. 在 Commerce headquarters 中，转到 **Retail 和 Commerce \> 渠道 \> 在线商店**。
1. 选择站点的在线商店渠道的 **零售渠道 ID** 值。
1. 在 **付款帐户** 快速选项卡上，如果尚未设置 **适用于 Adyen 的 Dynamics 365 付款连接器** 连接器，按照[设置适用于 Adyen 的 Dynamics 365 付款连接器](adyen-connector-setup.md)中的说明添加此连接器。
1. 配置 Adyen 连接器后，选择 **添加** 添加 **适用于 Apple Pay 的 Dynamics 365 付款连接器** 连接器。
1. 输入连接器商家属性的值。

    | 属性               | Description | 必填 | 自动设置 | 示例值 |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | 程序集名称          | 适用于 Apple Pay 的 Dynamics 365 付款连接器的程序集的名称。 | 是 | 是 | 二进制名称 |
    | 服务帐户 ID     | 商家属性设置的唯一标识符。 此标识符印在支付交易上，并标识下游流程（例如开票）应使用的商家属性。 | 是 | 是 | GUID |
    | 商家帐户 ID    | 输入唯一的 Adyen 商家标识符。 当您按照[向 Adyen 注册](adyen-connector-setup.md#sign-up-with-adyen)中的描述向 Adyen 注册时，会提供此值。 | 是 | 否 | MerchantIdentifier |
    | 云 API 密钥          | 输入 Adyen 云 API 密钥。 您可以按照[如何获取 API 密钥](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key)中的说明获取此密钥。 | 是 | 否 | abcdefg |
    | 网关环境    | 输入要映射到的 Adyen 网关环境。 可能的值为 **测试** 和 **实时**。 您应该仅为生产设备和交易将此字段设置为 **实时**。 | 是 | 是 | 实时 |
    | 支持的货币   | 输入连接器应处理的货币。 在卡存在的情况下，将交易请求发送到付款终端后，Adyen 可以通过[动态货币转换](https://www.adyen.com/pos-payments/dynamic-currency-conversion)支持其他货币。 联系 Adyen 支持部门获取支持的货币列表。 | 是 | 是 | USD;EUR |
    | 支持的支付方式 | 输入连接器应处理的支付方式。 | 是 | 是 | ApplePay |

1. 输入商家信息后，运行 **1070** 渠道配置分配计划作业。

## <a name="configure-commerce-pos-for-apple-pay"></a>为 Commerce POS 配置 Apple Pay

POS 配置将硬件配置文件的 **EFT 服务** 字段的配置用于适用于 Adyen 的 Dynamics 365 付款连接器。 在 Commerce headquarters 中，为适用于 Adyen 的 Dynamics 365 付款连接器配置 EFT 服务，如[“设置 Dynamics 365 POS 硬件配置文件”一节](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile)中所述。

确保将 **ApplePay** 添加到 **支持的支付方式** 字段中的支付方式列表中。 使用分号 (;) 分隔列表中的支付方式。

Adyen 连接器的处理器映射将捕获 Apple Pay 在 POS 终端上使用的钱包卡类型。

### <a name="configure-content-security-policies-in-site-builder"></a>在站点构建器中配置内容安全策略

在配置片段或页面以使用 Apple Pay 之前，您必须确保在 Commerce 站点构建器中为您的站点配置了内容安全策略 (CSP)。

要在站点构建器中配置内容安全策略，请按照以下步骤操作。

1. 转到 **站点设置 \> 扩展**。
1. 在 **内容安全策略** 选项卡上，选择 **添加**，将包含 `https://applepay.cdn-apple.com/jsapi/v1/apple-pay-sdk.js` 的行添加到 **child-src**、**connect-src**、**frame-src**、**img-src**、**script-src** 和 **style-src** 部分。
1. 完成后，选择 **保存并发布** 提交更改。

### <a name="set-up-apple-pay-as-a-checkout-payment-option"></a>将 Apple Pay 设置为结帐付款选项

要在您的站点的（非快速）结帐页面上将 Apple Pay 设置为结帐付款选项，请按照以下步骤操作。

1. 在站点构建器中，转到 **片段**，选择站点的结帐片段。
1. 选择 **编辑**。
1. 在 **结帐部分容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **选择模块** 对话框中，选择 **Apple Pay** 模块，然后选择 **确定**。
1. 选择 **保存**。
1. 选择 **完成编辑** 签入片段，然后选择 **发布** 进行发布。

**Apple Pay** 模块的设置内置在模块中，与为 Commerce headquarters 中的在线渠道设置的已配置的适用于 Apple Pay 的 Dynamics 365 付款连接器连接。

### <a name="apple-pay-payment-behavior"></a>Apple Pay 付款行为

**Apple Pay** 付款按钮仅在支持的 Apple Pay 设备（支持 Apple Pay 的 iPhone、iPad 和 Safari 浏览器）上显示。 如果用户不使用这些设备，**Apple Pay** 付款按钮将在视图中隐藏。

当用户选择 **Apple Pay** 付款按钮时，将出现 **Apple Pay** 对话框。 在那里，用户可以通过他们的 Apple Pay 设备或浏览器进行身份验证。 **Apple Pay** 对话框会显示用户针对其 Apple Wallet 配置的订单金额和付款方式的摘要。 用户可以查看这些详细信息，然后选择 **支付** 完成付款。 付款完成后，用户将被定向到 **订单完成** 站点页面，页面上将显示已完成交易的详细订单摘要。

## <a name="additional-resources"></a>其他资源

[付款常见问题](payments-retail.md)

[结帐模块](../add-checkout-module.md)

[付款模块](../payment-module.md)

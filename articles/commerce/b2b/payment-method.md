---
title: 配置 B2B 电子商务站点的客户帐户付款方式
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中配置客户帐户付款方式。 另外还介绍了信用额度如何影响企业到企业 (B2B) 电子商务站点的分期付款捕获。
author: josaw1
ms.date: 04/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: b8424920c3a177e01b71fc1c288b7acdd97ef191
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272009"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>配置 B2B 电子商务站点的客户帐户付款方式

[!include [banner](../../includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中配置客户帐户付款方式。 另外还介绍了信用额度如何影响企业到企业 (B2B) 电子商务站点的分期付款捕获。

零售商可以接受各种类型的付款来交换其在电子商务渠道中销售的产品和服务。 设置系统时，必须在 Dynamics 365 Commerce 中配置零售商接受的每种付款类型。 B2B 电子商务站点必须支持客户帐户（或“分期付款”）付款方式。 

## <a name="prerequisites"></a>先决条件

1. 在 Commerce headquarters 中添加客户帐户付款方式。
2. 将客户帐户付款方式与电子商务渠道关联。
3. 确保在 Commerce headquarters 中，在 **Retail 和 Commerce \> 客户 \> 所有客户 \> 付款默认值** 中为客户启用了 **Allow on account** 属性。

    > [!NOTE]
    > 如果应允许所有客户启用分期付款付款方式，对于与 B2B 站点关联的渠道的默认客户，您可以将 **Allow on account** 属性设置为 **是**。 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>在 Commerce 站点构建器中启用客户帐户付款方式 

要在 Commerce 站点构建器中启用客户帐户付款方式，请按照下列步骤操作。

1. 转到 **站点设置 \> 扩展**。
1. 将 **启用客户帐户付款** 属性设置为 **为 B2B 客户启用**。 
1. 选择 **保存并发布**。

> [!NOTE]
> 新站点设置仅在更新 app.settings.json 文件后才会生效。 有关详细信息，请参阅 [SDK 和模块库更新](../e-commerce-extensibility/sdk-updates.md)。

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>在 B2B 电子商务站点的结帐页上启用客户帐户付款方式

要在 B2B 电子商务站点的结帐页上启用客户帐户付款方式，请按照以下步骤操作。

1. 在 Commerce 站点构建器中，找到并编辑包含 B2B 电子商务站点的结帐模块的结帐页面或片段。
1. 在 **结帐部分容器** 插槽中，选择 **添加模块**，然后添加 **客户帐户付款** 模块。
1. 选择省略号 (**...**)，然后根据需要选择 **上移** 或 **下移**，来放置 **客户帐户付款** 模块。
1. 选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>确认已启用并发布客户帐户付款方式

要确认已启用客户帐户付款方式，请按照下列步骤操作。

1. 登录电子商务站点。
1. 向购物车添加产品。
1. 转到结帐页。 您应该会看到新的 **客户帐户** 付款方式。

## <a name="work-with-credit-limits"></a>使用信用额度

在 B2B 站点上启用客户帐户付款功能后，组织通常需要在订单捕获过程中显示有关信用额度和信用额度余额的信息。 客户的信用额度由 Commerce headquarters 中客户记录的 **信用和收款** 快速选项卡上的 **Credit limit** 属性定义。 但是，在 B2B 场景中，客户下的订单通常应该向客户所属组织的帐户开票。 因此，您必须将客户记录的 **发票和交货** 上的 **Invoice account** 属性设置为组织的客户帐户 ID。 然后，当客户在 B2B 站点上下订单时，订单会开票给组织。 B2B 站点还将使用组织的信用额度，而不是客户记录中定义的信用额度。

B2B 网站上显示的信用额度计算和余额取决于 Commerce headquarters 中 **Credit limit type** 属性的设置。 此属性的位置会有所不同，具体取决于 **功能管理** 工作区中是否启用了 **信用管理** 功能：

- 如果启用了 **信用管理** 功能，此属性位于 **信用和收款 \> 设置 \> 信用和收款参数 \> 信用** 下的 **信用额度** 快速选项卡。 
- 如果禁用了 **信用管理** 功能，此属性位于 **应收帐款 \> 设置 \> 应收帐款参数 \> 信用等级** 的 **信用等级** 下。

**Credit limit type** 属性支持的值为 **None**、**Balance**、**Balance + packing slip or product receipt** 和 **Balance + All**。 有关这些值的详细信息，请参阅[信用额度类型值](/dynamics365/supply-chain/sales-marketing/credit-limits-customers)。

> [!NOTE]
> 我们建议您将 **Credit limit type** 属性设置为 **Balance + packaging slip or product slip**，这样未结销售订单不会参与余额计算。 然后，如果您的客户将来下订单，他们就不必担心这些订单会影响他们当前的余额。

影响分期付款订单的另一个属性是 **Mandatory credit limit** 属性，它位于客户记录的 **信用和收款** 快速选项卡上。 通过将特定客户的此属性设置为 **Yes**，您可以强制系统检查他们的信用额度，即使 **Credit limit type** 属性已设置为 **None**，指定不应检查任何客户的信用额度。

目前，使用分期付款方式的客户支付的金额不能超过订单的剩余信用余额。 例如，如果客户的剩余信用余额为 $1,000，但订单价值为 $1,200，客户使用分期付款方式只能支付 $1,000。 因此，客户必须使用其他一些付款方式来支付其余金额。 在未来的版本中，Commerce 配置将允许用户在下订单时花费超出其信用额度。

**信用和收款** 模块具有新的信用管理功能。 要启用这些功能，请在 **功能管理** 工作区中启用 **信用管理** 功能。 其中一项新功能允许根据锁定规则暂停销售订单。 在进一步分析之后，信用经理角色可以释放或拒绝订单。 但是，暂停销售订单的功能不适用于 Commerce 订单，因为销售订单通常有预付款，而 **信用管理** 功能并不完全支持预付款场景。 

无论是否启用 **信用管理** 功能，如果在订单履行过程中客户余额超过信用额度，销售订单都不会被暂停。 Commerce 会生成警告消息或错误消息，具体取决于 **信用额度** 快速选项卡上 **在超出信用额度时显示的消息** 字段的值。

**Exclude from credit management** 属性阻止 Commerce 销售订单被暂停，位于销售订单标头中（**Retail 和 Commerce \> 客户 \> 所有销售订单**）。 如果 Commerce 销售订单的此属性设置为 **Yes**（默认值），订单将被从信用管理的暂停工作流中排除。 虽然此属性被命名为 **Exclude from credit management**，但在订单履行期间仍将使用定义的信用额度。 订单只是不会被暂停。

未来的 Commerce 版本计划提供基于锁定规则暂停 Commerce 销售订单的功能。 在支持该功能之前，如果您必须强制 Commerce 销售订单通过新的信用管理流，您可以在 Visual Studio 解决方案中自定义以下 XML 文件。 在文件中，修改逻辑，将 **CredManExcludeSalesOrder** 标志设置为 **否**。 这样，默认情况下，Commerce 销售订单的 **Exclude from credit management** 属性将设置为 **No**。

- RetailCreateCustomerOrderExtensions_CredMan_Extension.xml
- RetailCallCenterOrderExtensions_CredMan_Extension.xml

如果 **CredManExcludeSalesOrder** 标志设置为 **否**，当 B2B 客户可以使用销售点 (POS) 应用程序从商店购买商品时，过帐现金和结转交易记录可能会失败。 例如，现金付款类型有一个锁定规则，B2B 客户在商店中使用现金购买了一些商品。 在这种情况下，生成的销售订单将无法成功开票，因为它将被暂停。 因此，过帐将失败。 出于此原因，我们建议您在实现此自定义后进行端到端测试。

## <a name="additional-resources"></a>其他资源

[建立 B2B 电子商务站点](set-up-b2b-site.md)

[使用客户层次结构管理 B2B 业务合作伙伴](partners-customer-hierarchies.md)

[在 B2B 电子商务站点上管理业务合作伙伴用户](manage-b2b-users.md)

[设置 B2B 电子商务站点的产品数量限制](quantity-limits.md)

[SDK 和模块库更新](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

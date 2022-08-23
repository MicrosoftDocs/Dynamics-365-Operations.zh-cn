---
title: 礼品卡模块
description: 本文介绍礼品卡模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 93e2a6608b6d3190df7df1d8f85fd9d7e1c18692
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280550"
---
# <a name="gift-card-module"></a>礼品卡模块

[!include [banner](includes/banner.md)]

本文介绍礼品卡模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

结帐模块中可以使用礼品卡模块接受礼品卡，这是电子商务交易中的一种常用付款方式。 礼品卡模块支持 Dynamics 365、SVS 和 Givex 礼品卡。 SVS 和 Givex 礼品卡通过 Adyen 支付方兑换。 有关支持外部礼品卡（如 SVS 和 Givex）的详细信息，请参阅[对外部礼品卡的支持](./dev-itpro/gift-card.md)。

> [!NOTE]
> 在结帐流中兑换 SVS 和 Givex 礼品卡的支持在 Dynamics 365 Commerce 10.0.11 版本中提供。 

有两种礼品卡模块：

- **礼品卡** – 可以在结帐页面中使用此模块兑换礼品卡作为支付方式。 
- **礼品卡余额检查** – 任何页面中都可以使用此模块检查礼品卡的余额。 Commerce 版本 10.0.14 及更高版本中提供此模块。

> [!NOTE]
> 对礼品卡余额检查模块的支持在 Dynamics 365 Commerce 10.0.14 版本中提供。

下图显示了结帐页上的礼品卡模块的示例。

![礼品卡模块的示例。](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>模块属性

- **显示其他字段** – 此属性定义除了礼品卡编号（默认始终显示），还应该显示礼品卡的哪些字段。 例如，某些礼品卡支持显示个人标识号 (PIN)，其他则支持显示 PIN 和到期日期。 错误，还可以将此属性设置为“无”，这将仅显示礼品卡编号，不显示其他字段。

    支持以下值：

    - PIN
    - 到期日期
    - PIN 和到期日期 
    - 否

- **为来宾用户启用** - 启用此属性后，来宾用户可以兑换或检查礼品卡上的余额。 此属性要求在 Commerce Headquarters 中启用礼品卡的匿名（来宾）访问权限。 有关详细信息，请参阅[为来宾结帐启用礼品卡付款](#enable-gift-card-payments-for-guest-checkout)。

> [!IMPORTANT]
> **为来宾用户启用** 属性从 Commerce 版本 10.0.21 版开始可用。 它要求安装 Commerce 模块库包版本 9.31。

## <a name="site-settings-for-gift-card-modules"></a>礼品卡模块的站点设置

在 Commerce 站点构建器中 **站点设置 \> 扩展** 下，有一个礼品卡模块设置，名称为 **支持的礼品卡类型**。 此设置支持三个值：
- **Dynamics 365 礼品卡** – 如果应用此设置，则礼品卡模块仅允许兑换 Dynamics 365 礼品卡。 此设置仅支持 e-Commerce 站点中的已登录用户。
- **SVS 和 Givex 礼品卡** – 如果应用此设置，则礼品卡模块仅允许兑换 SVS 和 Givex 礼品卡。 此设置支持 e-Commerce 站点中的已登录用户和匿名用户。
- **Dynamics 365、SVS 和 Givex 礼品卡** – 如果应用此设置，则礼品卡模块允许兑换 Dynamics 365、SVS 和 Givex 礼品卡。 此设置仅支持 e-Commerce 站点中的已登录用户。

> [!IMPORTANT]
> 这些设置在 Dynamics 365 Commerce 10.0.11 版本中可用，仅在您需要 SVS 或 Givex 礼品卡支持时才需要。 如果要从旧版本的 Dynamics 365 Commerce 更新，必须手动更新 appsettings.json 文件。 有关更新 appsettings.json 文件的说明，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a>扩展内部礼品卡以用于电子商务店面

默认情况下，内部礼品卡未针对电子商务店面进行优化。 因此，在允许使用内部礼品卡付款之前，应通过扩展对它们进行配置，以帮助使其更加安全。 在允许内部礼品卡用于生产之前，应扩展以下礼品卡区域：

- **礼品卡编号** – 编号规则用于为内部礼品卡生成礼品卡编号。 由于可以轻松预测编号规则，因此您应该扩展礼品卡编号的生成，以将随机的密码安全的字符串用于发布的礼品卡编号。
- **GetBalance** – **GetBalance** API 用于查找礼品卡余额。 默认情况下，此 API 是公共的。 如果不需要 PIN 来查找礼品卡余额，则存在暴力攻击可以使用 **GetBalance** API 尝试查找具有余额的礼品卡编号的风险。 通过同时实现内部礼品卡的 PIN 要求和 API 限制，您可以帮助缓解风险。
- **PIN** – 默认情况下，内部礼品卡不支持 PIN。 您应该扩展内部礼品卡，以需要 PIN 才能查找余额。 此功能还可用于在连续的错误尝试输入 PIN 后锁定礼品卡。

## <a name="enable-gift-card-payments-for-guest-checkout"></a>为来宾结帐启用礼品卡付款

默认情况下，来宾（匿名）结帐不启用礼品卡付款。 若要启用，请执行以下步骤。

1. 在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS \> POS 操作**。
1. 选择并按住（或右键单击）网格的标头，然后选择 **插入列**。
1. 在 **插入列** 对话框中，选中 **AllowAnonymousAccess** 复选框。
1. 选择 **更新**。
1. 对于操作 **520**（礼品卡余额）和 **214**，将 **AllowAnonymousAccess** 值设置为 **1**。
1. 选择 **保存**。
1. 运行 **1090** 计划程序作业将更改同步到渠道数据库。 

## <a name="add-a-gift-card-module-to-a-page"></a>向页面添加礼品卡模块

有关如何向结帐页添加礼品卡模块和设置必需属性的说明，请参阅[结帐模块](add-checkout-module.md)。

## <a name="additional-resources"></a>其他资源

[购物车模块](add-cart-module.md)

[购物车图标模块](cart-icon-module.md)

[结帐模块](add-checkout-module.md)

[付款模块](payment-module.md)

[收货地址模块](ship-address-module.md)

[交付选项模块](delivery-options-module.md)

[提货信息模块](pickup-info-module.md)

[订单详细信息模块](order-confirmation-module.md)

[对外部礼品卡的支持](./dev-itpro/gift-card.md)

[SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

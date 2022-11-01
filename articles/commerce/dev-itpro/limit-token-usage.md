---
title: 限制付款令牌的使用
description: 本文介绍限制付款令牌在 Microsoft Dynamics 365 Commerce 中如何使用的功能。
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 8092ab0724f33f21759aa84d25e0bdcb5b2ad5dd
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709643"
---
# <a name="limit-payment-token-usage"></a>限制付款令牌的使用

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

本文介绍限制付款令牌在 Microsoft Dynamics 365 Commerce 中如何使用的功能。 令牌的使用仅限于销售订单范围，或者，如果客户授予同意，令牌将存储为存档卡。

## <a name="key-terms"></a>重要术语

| 条款 | Description |
|---|---|
| 标志 | Dynamics 365 系统中存储用于交易目的的付款引用的引用 XML blob。 |
| 存档卡 | 保存的协定将来在 Dynamics 365 系统或付款网关中使用的卡引用令牌，特定于客户的帐户。 |

付款令牌的使用限制适用于任何使用采用定期令牌的付款网关服务的环境。 现成的[适用于 Adyen 的 Dynamics 365 付款连接器](adyen-connector.md)使用循环付款令牌执行后续的订单操作，如授权调整和重新授权。

为了帮助控制这些定期付款令牌在整个系统中的使用方式，**将付款令牌限制为仅用于订单上下文** 功能将定期令牌的使用限制为系统中的销售订单范围。 启用后，此功能将对 Commerce headquarters 用户界面 (UI) 进行修改：更新付款输入页面，并限制选择过去的客户付款引用来用于新交易实例的功能。

此功能有助于满足某些支付发卡机构（如 Visa）的使用规则。 在 [Visa 核心规则和 Visa 产品与服务规则](https://usa.visa.com/content/dam/VCOM/download/about-visa/visa-rules-public.pdf)中，Visa 规定除非持卡人另外同意，否则付款令牌的使用应限制在交易范围内。

**将付款令牌限制为仅用于订单上下文** 功能仅在您使用采用循环付款令牌引用的付款网关服务时才有用。

## <a name="enable-the-feature"></a>启用功能

要启用 **将付款令牌限制为仅用于订单上下文** 功能，在您的环境的 Commerce headquarters 中，转到 **工作区 \> 功能管理**，在列表中找到并选择 **将付款令牌限制为仅用于订单上下文**，然后选择 **立即启用**。

## <a name="limit-payment-token-usage"></a>限制付款令牌的使用

启用此功能后，用于付款方式捕获的 Commerce headquarters 页面将更新它们引用为客户存档的客户付款方式的方式。 此更新主要会影响两个操作区域：

- 如何代表客户输入存档的客户卡
- 如何存储客户的付款信息用于将来的销售订单付款输入

当客户通过 Commerce 渠道交易时，付款详细信息存储时会带有销售订单上下文。 销售订单上下文将限制付款令牌，让它不会用作根据 Commerce headquarters 中新的或经过编辑的销售订单付款的付款页面的客户记录的付款引用。

### <a name="payment-form-changes"></a>付款窗体更改

当呼叫中心或 Commerce headquarters 用户根据销售订单为客户处理付款时，付款页面会显示付款方式选择详细信息。 当 **将付款令牌限制为仅用于订单上下文** 功能启用时，如果用户在付款页面选择加号 (**+**)，将只显示保存的“存档卡”记录。 更改需要呼叫中心或 Commerce headquarters 用户输入客户在填写 **输入客户付款信息** 进行新销售订单交易时提供的完整付款详细信息。

**编号** 字段的值列表仅包括与具有存档卡的客户关联的卡引用。 列表中将筛选掉任何不属于销售订单范围的过去的付款引用。

**编号** 字段下的加号 (**+**) 仍然可用，可用于输入客户为与正在处理的销售订单关联的交易提供的付款信息。

### <a name="how-cards-on-file-work"></a>存档卡的工作原理

启用 **将付款令牌限制为仅用于订单上下文** 功能时，存档卡是根据客户记录保存的循环付款令牌，不限于销售订单范围。 Commerce headquarters 用户在填写付款页面以进行新的销售订单付款时，存档卡可以让用户快速引用。 此令牌引用仅适用于 Dynamics 365 环境。 对于使用允许用户保存付款方式以备将来在付款 iFrame 模块中使用的付款网关服务的在线渠道，付款网关会将这些引用安全地存储为对 Dynamics 365 存档卡的单独引用。

例如，如果在线渠道中使用了适用于 Adyen 的 Dynamics 365 Commerce Dynamics 365 付款连接器，在付款 iFrame 模块中输入信用卡信息的客户在通过身份验证后，只能看到网关服务保存的用于下次在线购买的卡引用。 他们不会作为付款 iFrame 模块中的选项看到 Dynamics 365 环境存储的存档卡。 同样，当购物者通过呼叫中心下订单时，他们在线保存的卡引用不会作为选项提供给呼叫中心用户。 呼叫中心用户只会看到 Dynamics 365 系统（经客户同意）中之前保存的用于未来订单的存档卡引用。

Commerce headquarters 用户可以转到 **Retail 和 Commerce \> 客户**，选择客户帐户记录，来为客户保存存档卡。 在 **客户 \> 设置** 部分，有权处理支付页面的用户可以使用 **信用卡** 输入页面输入将存档以用于将来交易的付款卡。 此操作有助于在为客户处理未来的销售订单付款时节省时间。 呼叫中心和 Commerce headquarters 用户应仅在客户同意将卡引用用于未来交易时输入存档卡的卡详细信息。

Commerce headquarters 付款页面底部的 **保存以备将来使用** 复选框允许用户保存存档卡以备将来使用。 仅当客户同意将存档卡用于未来交易时，才应使用此复选框。 您可以使用 Commerce headquarters 中 **呼叫中心参数** 页面的 **付款** 选项卡上的 **允许客户存档卡** 选项来显示或限制 **保存以备将来使用** 复选框。 当此选项设置为 **是** 时，有权处理付款页面的 Commerce headquarters 用户可以使用 **保存以备将来使用** 复选框保存存档卡。 当此选项设置为 **否** 时，有权处理付款页面的 Commerce headquarters 用户无法使用此复选框。 如果您的公司希望限制定期令牌在 Commerce headquarters 中的使用，但还不希望允许在没有确保客户授予同意的程序的情况下保存存档卡，可以使用 **允许客户存档卡** 选项。

### <a name="commerce-headquarters-pages-where-the-recurring-token-restrictions-are-enforced"></a>执行定期令牌限制的 Commerce headquarters 页面

启用此功能后，令牌限制范围会影响 Commerce headquarters 的以下区域：

- **销售订单 \> 付款 \> 输入客户付款** 中的客户付款信息
- 连续性订单
- 分期付款
- 应收帐款信用卡帐款

### <a name="manage-payment-tokens-archiving-or-removal"></a>管理付款令牌（存档或删除）

在启用 **将付款令牌限制为仅用于订单上下文** 功能标志之前（或在禁用此功能时）创建的付款令牌在系统中将保持“范围外”，这些令牌可以在 Commerce headquarters 付款页上的选择列表中引用。 这些令牌可以在 Commerce headquarters 中以两种方式定期删除：

- 使用 **存档信用卡交易记录数据** 页面设置定期清除或存档付款令牌的作业。 如果将 **删除数据而不存档** 选项设置为 **是**，符合 **最短交易时间（天）** 设置的令牌将被删除。 有关详细信息，请参阅[存档信用卡交易记录数据](archive-cc-data.md)。
- 使用新的 **清除信用卡令牌** 页面（**应收帐款 \> 查询和报表 \> 清理 \> 清除信用卡令牌**），您可以在此页面运行或设置删除付款令牌的批处理作业。 设置以下参数：

    - **最短令牌期限（天）** 值必须为 90 天或更长。
    - **在后台运行** 设置可用于定义 **定期** 或 **警报** 设置。
    - 可以分配批处理组来运行特定组的任务。
    - 如果 **专用** 选项设置为 **是**，则只有创建作业的用户可以运行作业。
    - **关键作业** 选项的 **是** 设置可确保系统主动跟踪作业的状态。

已删除的令牌无法检索。 将 **最短令牌期限（天）** 字段设置为适合您环境的最长交易期限的范围（从授权到捕获或退款）。

## <a name="additional-resources"></a>其他资源

[付款常见问题](payments-retail.md)

[结帐模块](../add-checkout-module.md)

[付款模块](../payment-module.md)

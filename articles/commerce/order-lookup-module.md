---
title: 订单查找模块
description: 本文介绍订单查找模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。
author: bicyclingfool
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 8c60ed0c334bf09916dd633302c6d813ea6f16b6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281446"
---
# <a name="order-lookup-module"></a>订单查找模块

[!include [banner](includes/banner.md)]

本文介绍订单查找模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。

订单查找模块提供了一个窗体，客户可以使用该窗体查找自己在电子商务站点中下达的订单。 其作为[启用来宾结帐订单查找](order-lookup-guest.md)功能的一部分使用。 订单查找模块可用于查找通过电子商务站点、零售销售点 (POS) 或呼叫中心提交的订单。 该窗体可以检索来宾用户和注册用户提交的订单。

下图显示了订单查找模块呈现的窗体的一个示例。 当客户填写此窗体并选择 **查找您的订单** 时，将把其重定向到订单详细信息页。

![页面上的订单查找模块的窗体。](./media/OrderLookup_module.PNG)

## <a name="order-lookup-module-properties"></a>订单查找模块属性

| 属性名称     | 值     | 说明 |
|-------------------|-----------|-------------|
| 标题           | 文本      | 窗体顶部显示的标题（例如，“查找您的订单”）。 |
| 富文本         | 富文本 | 标题下方显示的可选说明性文本。 |
| 订单状态类型 | 枚举      | <p>除了订单确认 ID 之外，还选择窗体将从客户处请求的信息类型。 当前支持以下值：</p><ul><li><b>电子邮件</b> – 窗体将包含一个字段，客户可以在下达订单时在这里输入自己使用的电子邮件地址。</li><li><b>无</b> – 除了订单确认 ID，窗体不索取其他任何信息。</li></ul> |

## <a name="add-an-order-lookup-module-to-a-page"></a>向页面添加订单查找模块

可将订单查找模块添加到电子商务站点的任何页面主体中。 如果要使用订单查找模块启用来宾结帐订单查找功能，请务必将其添加到不需要用户登录的页面。 若要在 Commerce 站点构建器树视图中查找页面的 **需要登录?** 设置，请选择 **默认页面(必需)** 槽 ，然后查看右窗格底部。

## <a name="additional-resources"></a>其他资源

[启用来宾结帐订单查找功能](order-lookup-guest.md)

[模块库概览](starter-kit-overview.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

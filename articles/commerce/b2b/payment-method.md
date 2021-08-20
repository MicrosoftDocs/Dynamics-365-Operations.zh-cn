---
title: 配置 B2B 电子商务站点的客户帐户付款方式
description: 本主题介绍如何为企业到企业 (B2B) 电子商务站点配置客户帐户付款方式。
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 628f3b3b2d86154190dfdcc82b8b391c2facce103f607519514c65b5fba26653
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738045"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>配置 B2B 电子商务站点的客户帐户付款方式

[!include [banner](../../includes/banner.md)]

本主题介绍如何为企业到企业 (B2B) 电子商务站点配置客户帐户付款方式。

零售商可以接受各种类型的付款来交换其在电子商务渠道中销售的产品和服务。 设置系统时，必须在 Microsoft Dynamics 365 Commerce 中配置零售商接受的每种付款类型。 B2B 电子商务站点必须支持客户帐户（或“分期付款”）付款方式。 

## <a name="prerequisites"></a>先决条件

1. 在 Commerce headquarters 中添加客户帐户付款方式。
2. 将客户帐户付款方式与电子商务渠道关联。
3. 确保在 Commerce headquarters 中，在 **Retail 和 Commerce \> 客户 \> 所有客户 \> 付款默认值** 中为客户启用了 **允许分期付款**。 同时确保在 Commerce headquarters 中，在 **Retail 和 Commerce \> 客户 \> 所有客户 \> 信用和收款** 中为客户正确设置了 **信用额度** 参数。 

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

## <a name="additional-resources"></a>其他资源

[建立 B2B 电子商务站点](set-up-b2b-site.md)

[为 B2B 组织创建组织建模层次结构](org-model.md)

[在 B2B 电子商务站点上管理业务合作伙伴用户](manage-b2b-users.md)

[设置 B2B 电子商务站点的产品数量限制](quantity-limits.md)

[SDK 和模块库更新](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: 电子商务数字礼品卡
description: 本主题介绍数字礼品卡如何在 Microsoft Dynamics 365 Commerce 的电子商务实现中工作。 另外还概述了重要的配置步骤。
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: cbfa84770e4671fdf289e168345d8b815caee4f7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230550"
---
# <a name="e-commerce-digital-gift-cards"></a>电子商务数字礼品卡

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

本主题介绍数字礼品卡如何在 Microsoft Dynamics 365 Commerce 的电子商务实现中工作。 另外还概述了重要的配置步骤。

在 Dynamics 365 Commerce 中，数字礼品卡的购买流与系统中其他产品的购买流相同。 无需配置其他模块。 如果将多个礼品卡添加到购物车中，礼品卡商品不会在单个销售行上聚合。 需要此行为，是因为每个销售行使用单独的礼品卡号开票。

Dynamics 365 Commerce 10.0.16 版本及更高版本中支持购买数字礼品卡。

下图显示了 Fabrikam 电子商务站点上数字礼品卡的产品详细信息页面 (PDP) 的示例。

![Fabrikam 电子商务站点上数字礼品卡 PDP 的示例](./media/GiftcardPDP.PNG)

## <a name="turn-on-the-digital-gift-card-feature-in-commerce-headquarters"></a>在 Commerce headquarters 中打开数字礼品卡功能

要让数字礼品卡的购买流在 Dynamics 365 Commerce 中运行，必须在 Commerce headquarters 中打开 **通过电子商务功能购买礼品卡** 功能。 您可以在 Commerce headquarters 中的 **功能管理** 工作区中找到此功能，如下图所示。

![Commerce headquarters 中的“功能管理”工作区](./media/Featureflag.PNG)

## <a name="configure-a-digital-gift-card-in-commerce-headquarters"></a>在 Commerce headquarters 中配置数字礼品卡

数字礼品卡产品应在 Commerce headquarters 中配置。 流程类似于其他产品的流程。 但是，以下重要步骤特定于购买礼品卡的配置。 有关如何创建和配置产品的详细信息，请参阅[在 Commerce 中创建新产品](create-new-product-commerce.md)。

- 在 **新建产品** 对话框中配置数字礼品卡产品时，将 **产品类别** 字段设置为 **服务**。 （要打开此对话框，转到 **零售和商业 \> 产品和类别 \> 产品(按类别)**，选择 **新建**。）在下订单之前，不会检查 **服务** 类型的产品的可用库存。 有关详细信息，请参阅[创建新产品](create-new-product-commerce.md#create-a-new-product)。
- 在 **Commerce 参数** 页上的 **过帐** 选项卡上，**礼品卡产品** 字段必须设置为 **数字礼品卡**，如下图所示。 如果产品是外部礼品卡，请参阅[对外部礼品卡的支持](./dev-itpro/gift-card.md)了解详细信息。

    ![Commerce headquarters 中的礼品卡产品字段](./media/PostGiftcard.png)

- 如果礼品卡必须支持多个预定义金额（例如，$25、$50 和 $100），**尺寸** 维度应用于设置这些预定义金额。 每个预定义金额是一个变型。 有关详细信息，请参阅[产品维度](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json)。
- 如果客户必须能够为礼品卡指定自定义金额，请首先设置允许自定义金额的变型。 接下来，从 **类别中的已发布产品** 页打开产品，然后在 **Commerce** 快速选项卡上，将 **键入价格** 字段设置为 **必须键入新价格**，如下图所示。 此设置可确保客户在 PDP 上浏览产品时可以输入价格。

    ![Commerce headquarters 中的“键入价格”字段](./media/KeyInPrice.png)

- 数字礼品卡的交货方式必须设置为 **电子**。 在 **交货方式** 页上（**零售和商业 \> 渠道设置 \> 交货方式**），在列表窗格中选择 **电子** 交货方式，然后将数字礼品卡产品添加到 **产品** 快速选项卡上的网格中，如下图所示。 有关详细信息，请参阅[设置交货方式](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)。

    ![Commerce headquarters 中“交货方式”页上的数字礼品卡产品](./media/ElectronicMode.PNG)

- 确保已创建在线功能配置文件，并将其与 Commerce headquarters 中的在线商店关联。 在功能配置文件中，将 **聚合产品** 选项设置为 **是**。 此设置将确保聚合除礼品卡以外的所有商品。 有关详细信息，请参阅[创建在线功能配置文件](online-functionality-profile.md)。
- 要确保为礼品卡开票后客户能够收到电子邮件，在 **电子邮件通知配置文件** 页上创建新的电子邮件通知类型，并将 **电子邮件通知类型** 字段设置为 **发放礼品卡**。 有关详细信息，请参阅[设置电子邮件通知配置文件](email-notification-profiles.md)。

## <a name="add-product-images-to-the-commerce-site-builder-media-library"></a>将产品图像添加到 Commerce 站点构建器媒体库

您必须将数字礼品卡产品的产品图像添加到 Commerce 站点构建器媒体库中。 确保礼品卡图像文件的文件名遵循您的站点的产品图像的命名约定。 有关详细信息，请参阅[上载图像](dam-upload-images.md)。

## <a name="configure-a-custom-amount-for-a-digital-gift-card-in-commerce-site-builder"></a>在 Commerce 站点构建器中为数字礼品卡配置自定义金额

如果将数字礼品卡配置为允许自定义金额，还必须在您的站点的 PDP 上使用的[购买框模块](add-buy-box.md)中启用此行为。 购买框模块支持允许自定义金额的模块配置。 您还可以定义自定义金额允许的最小和最大金额。

要在 Commerce 站点构建器中为数字礼品卡配置自定义金额，请按照以下步骤操作。

1. 转到您的站点的 PDP 上使用的购买框模块。 此购买框模块可以在片段、模板或页面中实现。
1. 选择 **编辑**。
1. 在右侧的属性窗格中，选中 **允许自定义价格** 复选框。
1. 可选：要定义自定义金额的最小和最大金额，在 **最低价格** 和 **最高价格** 下输入金额。
1. 选择 **完成编辑**，然后选择 **发布**。

## <a name="additional-resources"></a>其他资源

[购买框模块](add-buy-box.md)

[结帐模块](add-checkout-module.md)

[购物车模块](add-cart-module.md)

[在 Commerce 中创建新产品](create-new-product-commerce.md)

[设置交货模式](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[产品维度](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json)

[设置电子邮件通知配置文件](email-notification-profiles.md)

[创建在线功能配置文件](online-functionality-profile.md)

[对外部礼品卡的支持](./dev-itpro/gift-card.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
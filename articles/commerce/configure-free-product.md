---
title: 配置产品以进行免费购买
description: 本主题介绍如何配置产品，以可以在 Microsoft Dynamics 365 Commerce 中免费购买。
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2ad96a3dde93a48694aee418ecfbbd33dc9830d6
ms.sourcegitcommit: 6bf9e18989e6d77497a9dda1c362f324b3c2fbf2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/27/2021
ms.locfileid: "7713877"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>配置产品以进行免费购买

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

本主题介绍如何配置产品，以可以在 Microsoft Dynamics 365 Commerce 中免费购买。

## <a name="configure-the-product"></a>配置产品

要在 Dynamics 365 Commerce 中免费销售产品，必须将其价格设置为 0（零）。 此外，您必须配置产品的 **免费有效** 设置。

要在 Commerce Headquarters 中配置 **免费有效** 设置，请按照以下步骤操作。

1. 转到 **Retail 和 Commerce \> 产品和类别 \> 按类别发布的产品**。
1. 转到要免费销售的产品。 
1. 在产品页面的 **Commerce** 部分，将 **免费有效** 选项设置为 **是**。

下图显示了产品的一个示例，其中 **免费有效** 选项设置为 **是**。

![将“免费有效”选项设置为“是”的产品的示例。](./media/Zero-price.png)

## <a name="configure-the-online-stores-functionality-profile"></a>配置在线商店的功能配置文件

您应该为您的在线商店配置功能配置文件的 **允许不付款结帐** 设置，以允许没有付款的交易，然后才可以处理免费交易。 有关如何创建功能配置文件的信息，请参阅[创建在线功能配置文件](online-functionality-profile.md)。

要在 Commerce Headquarters 中配置 **允许不付款结帐** 设置，请按照以下步骤操作。

1. 转到 **Retail 和 Commerce \> 渠道设置 \> 在线商店设置**。
1. 在商店的功能配置文件页面上，在 **结帐**，将 **允许不付款结帐** 选项设置为 **是**。

下图显示了在线商店配置文件的一个示例，其中 **允许不付款结帐** 选项设置为 **是**。

![在线商店配置文件的一个示例，其中“允许不付款结帐”选项设置为是。](./media/Zero-price-profile.png)

## <a name="additional-resources"></a>其他资源

[零售销售价格管理](price-management.md)

[创建在线功能配置文件](online-functionality-profile.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

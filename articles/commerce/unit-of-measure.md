---
title: 应用度量单位设置
description: 本文介绍度量单位设置，并介绍如何在 Microsoft Dynamics 365 Commerce 中应用这些设置。
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 7a7be6395a8bfce38e84f850bd792f358941c18a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275533"
---
# <a name="apply-unit-of-measure-settings"></a>应用度量单位设置

[!include [banner](includes/banner.md)]

本文介绍度量单位设置，并介绍如何在 Microsoft Dynamics 365 Commerce 中应用这些设置。

产品可以按不同的单位出售，如“每个”、“对”和“一打”。 在 Commerce headquarters 中，可以为产品定义销售度量单位，并在电子商务站点上显示。 例如，如果零售商既单个销售又成打销售产品，则可以将可用的度量单位与其他产品信息一起显示。

在下图中的示例中，已在 Commerce headquarters 中为产品配置了销售度量单位 **ea**（每个）。

![在 Commerce Headquarters 中配置了度量单位的产品的示例。](./media/Productunit-headquarters.PNG)

> [!NOTE]
> 从 Commerce 版本 10.0.19 开始提供应用和显示度量单位的支持。

## <a name="unit-of-measure-settings"></a>度量单位设置

度量单位显示设置是在 Commerce 站点构建器中定义：**站点设置 \> 扩展 \> 为产品显示度量单位**。 支持三种设置：

- **不显示** – 选择此设置后，电子商务站点将不会为产品显示度量单位。 此行为是默认行为。
- **在产品购买体验中显示** – 选择此设置后，度量单位将显示在产品详细信息、购物车、结帐、订单历史记录和订单详细信息页上。
- **在产品浏览和购买体验中显示** – 选择此设置后，度量单位将显示在产品购买体验页面以及产品浏览体验期间。 作为此行为的一部分，度量单位将显示在搜索结果和产品集合模块中。

> [!IMPORTANT]
> 度量单位显示设置自 Commerce 版本 10.0.19 开始可用。 如果要从旧版本的 Commerce 更新，必须手动更新 appsettings.json 文件。 有关说明，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。

## <a name="modules-that-use-unit-of-measure-settings"></a>使用度量单位设置的模块

使用度量单位设置的模块包括购买框、愿望列表、购物车、购物车图标、搜索结果容器、产品集合、结帐和订单详细信息模块。

在下图的示例中，产品详细信息页 (PDP) 为产品显示了度量单位 (**ea**)。

![显示度量单位的 PDP 的示例。](./media/Productunit-PDP.png)

在下图的示例中，产品集合模块为产品显示了度量单位 (**ea**)。

![显示度量单位的产品集合模块的示例。](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a>其他资源

[模块库概览](starter-kit-overview.md)

[购物车模块](add-cart-module.md)

[购买框模块](add-buy-box.md)

[帐户管理页面和模块](account-management.md)

[SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

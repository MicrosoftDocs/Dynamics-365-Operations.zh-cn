---
title: 应用“将产品添加到购物车”设置
description: 本主题介绍“将产品添加到购物车”设置和如何在 Microsoft Dynamics 365 Commerce 中应用它们。
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6299a1c815978ab9f748b6110980e673e1fbae927ed08a5e2e080f89ef063115
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712806"
---
# <a name="apply-add-product-to-cart-settings"></a>应用“将产品添加到购物车”设置

[!include [banner](includes/banner.md)]

本主题介绍 **将产品添加到购物车** 设置和如何在 Microsoft Dynamics 365 Commerce 中应用它们。

当在 Dynamics 365 Commerce 电子商务站点上将产品添加到购物车时，将支持不同的工作流。 例如，站点用户可能会转到购物车页面。 或者，用户可能留在当前页面上，但会收到确认产品已添加到购物车的通知。

若要支持不同的工作流，**将产品添加到购物车** 字段将在 Commerce 站点构建器中的 **设置 \> 扩展** 中可用。 选择以下设置选项之一来实现相应的工作流：

- **导航到购物车页面** – 当用户将物料添加到购物车时，他们将转到购物车页面。
- **显示通知** – 当用户将物料添加到购物车时，他们将收到一条确认通知并且可以继续在产品详细信息页面 (PDP) 上浏览。
- **显示迷你购物车** – 当用户将物料添加到购物车时，将显示迷你购物车内容。 用户可以查看购物车中的所有物料，如果准备就绪，他们可以继续结帐。
- **使用通知模块显示通知** – 当用户将物料添加到购物车时，使用通知模块显示确认通知。 若要使此设置选项起作用，必须将通知模块添加到页面标题。
- **不导航到购物车页面** – 当用户将物料添加到购物车时，他们将留在当前页面。

下图显示了站点构建器中 **将产品添加到购物车** 设置选项的示例。

![站点构建器中将产品添加到购物车设置选项的示例](./media/AW_sitesettings.PNG)

> [!IMPORTANT]
> - **将产品添加到购物车** 站点设置从 Dynamics 365 Commerce 版本 10.0.11 发行版本开始提供。 如果要从旧版本的 Dynamics 365 Commerce 更新，必须手动更新 appsettings.json 文件。 有关如何更新 appsettings.json 文件的信息，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。
> - **显示迷你购物车** 设置选项从 Dynamics 365 Commerce 版本 10.0.20 发行版本开始提供。 如果要从旧版本的 Dynamics 365 Commerce 更新，必须手动更新 appsettings.json 文件。 有关如何更新 appsettings.json 文件的信息，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。

下图显示了 Fabrikam 站点上“已添加到购物车”确认通知的示例。

![Fabrikam 站点上“已添加到购物车”确认通知的示例](./media/ecommerce-addtocart-notifications.PNG)

下图显示了 Adventure Works 站点上“已添加到购物车”确认通知的示例。

![Adventure Works 站点上“已添加到购物车”确认通知的示例](./media/AW_minicart.PNG)

## <a name="additional-resources"></a>其他资源

[模块库概览](starter-kit-overview.md)

[购买框模块](add-buy-box.md)

[商店选择器模块](store-selector.md)

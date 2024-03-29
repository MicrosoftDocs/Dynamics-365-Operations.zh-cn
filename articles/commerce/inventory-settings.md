---
title: 应用库存设置
description: 本文介绍库存设置，并介绍如何在 Microsoft Dynamics 365 Commerce 中应用这些设置。
author: anupamar-ms
ms.date: 08/31/2022
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
ms.openlocfilehash: 49310a44f8b9c636734e04d4eed9445384b55791
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405312"
---
# <a name="apply-inventory-settings"></a>应用库存设置

[!include [banner](includes/banner.md)]

本文介绍库存设置，并介绍如何在 Microsoft Dynamics 365 Commerce 中应用这些设置。

库存设置指定在将产品添加到购物车之前是否应该检查库存。 另外还定义与库存相关的促销消息，如“有存货”和“仅剩几个”。 这些设置可确保如果库存不足就不能购买产品。

Dynamics 365 Commerce 提供对产品现有量的估计。 有关如何计算估计现有量的信息，请参阅[计算零售渠道的库存现有量](calculated-inventory-retail-channels.md)。

在 Commerce 站点构建器中，可以为产品或类别定义库存阈值和范围。 它们确定库存是分类为有存货、低库存还是库存不足。 有关详细信息，请参阅[配置库存缓冲区和库存级别](inventory-buffers-levels.md)。

> [!NOTE]
> 对库存阈值和范围的支持在 Dynamics 365 Commerce 10.0.12 版本中提供。

## <a name="inventory-settings"></a>库存设置

在 Commerce 中，库存设置在站点构建器中的 **站点设置 \> 扩展 \> 库存管理** 处定义。 有六种库存设置，其中一种已过时（已弃用）：

- **在应用中启用存货检查** – 此设置打开产品库存检查。 然后，商店模块中的购买框、购物车和提货将检查产品库存，并且仅在有库存时允许将产品添加到购物车中。
- **库存级别确定条件** – 此设置定义如何计算库存级别。 可用值为 **总可用量**、**实际可用量** 和 **库存不足阈值**。 在 Commerce 中，可以为每个产品和类别定义库存阈值和范围。 库存 API 返回 **总可用量** 属性和 **实际可用量** 属性的产品库存信息。 零售商决定是应该使用 **总可用量** 还是 **实际可用量** 值来确定库存盘点，以及有存货和库存不足状态的相应范围。

    **库存级别确定条件** 设置的 **库存不足阈值** 值是旧的（旧版）已过时的值。 选择它后，库存盘点将根据 **总可用量** 值的结果确定，但阈值由稍后介绍的 **库存不足阈值** 数字设置定义。 此阈值设置将应用于整个电子商务站点的所有产品。 如果库存低于阈值数字，则视为产品库存不足。 否则，视为有存货。 **库存不足阈值** 值的能力是有限的，我们不建议您在版本 10.0.12 及更高版本中使用它。

- **多个仓库的库存级别** – 此设置可以针对默认仓库或多个仓库计算库存级别。 **基于单个仓库** 选项将基于默认仓库计算库存级别。 或者，电子商务站点可以指向多个仓库以推进履行。 在这种情况下，**基于装运和提货仓库的聚合** 选项用于指示存货可用性。 例如，当客户购买物料并选择“装运”作为交货方式时，可以从履行组中具有可用库存的任何仓库装运物料。 如果履行组中的任何可用装运仓库有库存，产品详细信息页 (PDP) 将为装运显示“有存货”消息。 

    > [!IMPORTANT] 
    > **多个仓库的库存级别** 设置从 Commerce 版本 10.0.19 开始可用。 如果要从旧版本的 Commerce 更新，必须手动更新 appsettings.json 文件。 有关说明，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。

- **产品列表页的库存设置** – 此设置定义库存不足产品在产品集合和搜索结果模块呈现的产品列表中的显示方式。 可用值有 **与其他产品一起按顺序显示**、**从列表中隐藏库存不足产品** 和 **在列表末尾显示库存不足产品**。 要使用此设置，您必须首先在 Commerce Headquarters 中配置一些必备设置。 有关详细信息，请参阅[库存感知产品列表](inventory-aware-product-listing.md)。

    > [!IMPORTANT] 
    > **产品列表页的库存设置** 设置从 Commerce 版本 10.0.20 开始可用。 如果要从旧版本的 Commerce 更新，必须手动更新 appsettings.json 文件。 有关说明，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。

- **库存范围** – 此设置定义在站点模块上显示的库存范围消息。 仅当为 **库存级别确定条件** 选择了 **总可用量** 值或 **实际可用量** 值时，此设置才适用。 可用值有 **所有**、**低库存和库存不足** 和 **库存不足**。

    - 选择 **所有** 时，将显示所有库存范围的消息，从有存货（“有货”消息）到库存不足（“库存不足”消息）。
    - 选择 **低库存和库存不足** 时，将显示除有存货（“有货”消息）以外的所有库存范围的消息。
    - 选择 **库存不足** 时，将仅显示“库存不足”消息。

- **库存不足阈值** – 这是一个旧的数字设置，只有在为 **库存级别确定条件** 设置选择了 **库存不足阈值** 值时才会生效。

> [!IMPORTANT] 
> 这些设置在 Dynamics 365 Commerce 10.0.12 版本中提供。 如果要从旧版本的 Dynamics 365 Commerce 更新，必须手动更新 appsettings.json 文件。 有关更新 appsettings.json 文件的说明，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。

## <a name="modules-that-use-inventory-settings"></a>使用库存设置的模块

购买框、愿望列表、商店选择器、购物车和购物车图标模块使用库存设置显示库存范围和消息。

在下图的示例中，PDP 显示有存货（“可用”）消息。

![显示有存货消息的 PDP 模块的示例。](./media/pdp-InStock.png)

在下图的示例中，PDP 显示有“库存不足”消息。

![显示库存不足消息的 PDP 模块的示例。](./media/pdp-outofstock.png)

在下图的示例中，购物车显示有存货（“可用”）消息。

![显示有存货消息的购物车模块的示例。](./media/cart-instock.png)

## <a name="additional-resources"></a>其他资源

[模块库概览](starter-kit-overview.md)

[配置库存缓冲区和库存级别](inventory-buffers-levels.md)

[购物车模块](add-cart-module.md)

[购买框模块](add-buy-box.md)

[帐户管理页面和模块](account-management.md)

[商店选择器模块](store-selector.md)

[SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: 应用库存设置
description: 本主题介绍库存设置，并介绍如何在 Microsoft Dynamics 365 Commerce 中应用这些设置。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 77a3bde12fd047e15d7730903416cdb5263a8cd9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972801"
---
# <a name="apply-inventory-settings"></a>应用库存设置

[!include [banner](includes/banner.md)]

本主题介绍库存设置，并介绍如何在 Microsoft Dynamics 365 Commerce 中应用这些设置。

## <a name="overview"></a>概览

库存设置指定在将产品添加到购物车之前是否应该检查库存。 另外还定义与库存相关的促销消息，如“有存货”和“仅剩几个”。 这些设置可确保如果库存不足就不能购买产品。

Dynamics 365 Commerce 提供对产品现有量的估计。 有关如何计算估计现有量的信息，请参阅[计算零售渠道的库存现有量](calculated-inventory-retail-channels.md)。

在 Commerce 站点构建器中，可以为产品或类别定义库存阈值和范围。 它们确定库存是分类为有存货、低库存还是库存不足。 有关详细信息，请参阅[配置库存缓冲区和库存级别](inventory-buffers-levels.md)。

> [!NOTE]
> 对库存阈值和范围的支持在 Dynamics 365 Commerce 10.0.12 版本中提供。

## <a name="inventory-settings"></a>库存设置

在 Commerce 中，库存设置在站点构建器中的 **站点设置 \> 扩展 \> 库存管理** 处定义。 有四种库存设置，其中一种已过时（已弃用）：

- **在应用中启用存货检查** – 此设置打开产品库存检查。 然后，商店模块中的购买框、购物车和提货将检查产品库存，并且仅在有库存时允许将产品添加到购物车中。
- **库存级别确定条件** – 此设置定义如何计算库存级别。 可用值为 **总可用量**、**实际可用量** 和 **库存不足阈值**。 在 Commerce 中，可以为每个产品和类别定义库存阈值和范围。 库存 API 返回 **总可用量** 属性和 **实际可用量** 属性的产品库存信息。 零售商决定是应该使用 **总可用量** 还是 **实际可用量** 值来确定库存盘点，以及有存货和库存不足状态的相应范围。

    **库存级别确定条件** 设置的 **库存不足阈值** 值是旧的（旧版）已过时的值。 选择它后，库存盘点将根据 **总可用量** 值的结果确定，但阈值由稍后介绍的 **库存不足阈值** 数字设置定义。 此阈值设置将应用于整个电子商务站点的所有产品。 如果库存低于阈值数字，则视为产品库存不足。 否则，视为有存货。 **库存不足阈值** 值的能力是有限的，我们不建议您在版本 10.0.12 及更高版本中使用它。

- **库存范围** – 此设置定义在站点模块上显示消息的库存范围。 仅当为 **库存级别确定条件** 选择了 **总可用量** 值或 **实际可用量** 值时，此设置才适用。 可用值有 **所有**、**低库存和库存不足** 和 **库存不足**。

    - 选择 **所有** 时，将显示所有库存范围的消息，从有存货（“有货”消息）到库存不足（“库存不足”消息）。
    - 选择 **低库存和库存不足** 时，将显示除有存货（“有货”消息）以外的所有库存范围的消息。
    - 选择 **库存不足** 时，将仅显示“库存不足”消息。

- **库存不足阈值** – 这是一个旧的数字设置，只有在为 **库存级别确定条件** 设置选择了 **库存不足阈值** 值时才会生效。

> [!IMPORTANT] 
> 这些设置在 Dynamics 365 Commerce 10.0.12 版本中提供。 如果要从旧版本的 Dynamics 365 Commerce 更新，必须手动更新 appsettings.json 文件。 有关更新 appsettings.json 文件的说明，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。

## <a name="modules-that-use-inventory-settings"></a>使用库存设置的模块

购买框、愿望列表、商店选择器、购物车和购物车图标模块使用库存设置显示库存范围和消息。

下图显示了产品详细信息页面 (PDP) 的示例，该页面显示有存货（“有货”）消息。

![显示有存货消息的 PDP 模块的示例](./media/pdp-InStock.png)

下图显示了显示“库存不足”消息的 PDP 示例。

![显示库存不足消息的 PDP 模块的示例](./media/pdp-outofstock.png)

下图显示了显示有存货（“有货”）消息的购物车的示例。

![显示有存货消息的购物车模块的示例](./media/cart-instock.png)

## <a name="additional-resources"></a>其他资源

[模块库概述](starter-kit-overview.md)

[配置库存缓冲区和库存级别](inventory-buffers-levels.md)

[购物车模块](add-cart-module.md)

[购买框模块](add-buy-box.md)

[帐户管理页面和模块](account-management.md)

[商店选择器模块](store-selector.md)

[SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md)

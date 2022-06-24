---
title: 产品维度
description: 产品有五个维度 - 颜色、配置、尺寸、样式和版本。 您在维度组中合并产品维度，并将维度组分配给基础产品。 产品维度的组合确定如何定义产品变型。
author: t-benebo
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle, EcoResVersionNameLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: acfd9be044818ab0f40171c25a8fc9e760173aa8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867918"
---
# <a name="product-dimensions"></a>产品维度

[!include [banner](../includes/banner.md)]

产品有五个维度：颜色、配置、尺寸、样式和版本。 您在维度组中合并产品维度，并将维度组分配给基础产品。 产品维度的组合确定如何定义产品变型。

产品维度是用于标识产品变型的特性。 您可以使用产品维度的组合来定义产品变型。 必须至少为基础产品定义一个产品维度，以便创建产品变型。

## <a name="product-variants"></a>产品变型

产品变型也称作物料。 物料是有形产品，与服务不同。 也可以使用服务类型定义产品主数据。 使用服务类型，您可以指定包含服务的产品变型。 例如，您可以为咨询工作指定产品主数据，为高级顾问和初级顾问执行的工作指定产品变型。

## <a name="product-dimensions"></a>产品维度

产品变型可以基于产品维度值生成。

可以在以下位置创建尺寸、颜色和样式维度的产品维度值：

- **尺寸** 页面（**产品信息管理 \> 设置 \> 维度和变型组 \> 尺寸**）
- **颜色** 页面（**产品信息管理 \> 设置 \> 维度和变型组 \> 颜色**）
- **样式** 页面（**产品信息管理 \> 设置 \> 维度和变型组 \> 样式**）

通常使用产品配置器或基于维度的配置器创建配置维度的产品维度值。 

产品版本通常是在产品在其生命周期内演进时针对特定版本创建的。 本文后面将详细介绍产品版本。

产品维度还可以在 **产品维度** 页中创建和维护，可从以下位置访问该页：

- 转到 **产品信息管理 \> 产品 \> 基础产品**。 在操作窗格上，选择 **产品维度**。
- 转到 **产品信息管理 \> 产品 \> 所有产品和产品主数据**。 选择基础产品。 在操作窗格上，选择 **产品维度**。
- 转到 **产品信息管理 \> 已发布产品**。 选择基础产品。 在操作窗格的 **产品** 选项卡上，在 **产品主数据** 组中，选择 **产品维度**。

为物料可创建的变型数受限于可能的产品维度组合数。

> [!TIP]
> 例如，当您在订单行上使用产品时，您选择产品维度来标识要使用的产品变型。

## <a name="example"></a>示例

一家公司销售牛仔裤。 物料 *牛仔裤* 使用颜色和尺寸产品维度。 销售的牛仔裤有三种不同的颜色和六种不同的尺寸。 颜色有蓝色、黑色和棕色。 尺寸有 XS、S、M、L、XL 和 XXL。 并非所有尺寸都提供三种颜色。 如果所有组合都可用，那么将有 18 种不同类型的牛仔裤。 但是，在此示例中，仅生成以下九个产品变型组合。

| 颜色 | 大小 |
|-------|------|
| 蓝色  | XS   |
| 蓝色  | 六    |
| 蓝色  | 一    |
| 黑色 | 一    |
| 黑色 | L    |
| 黑色 | XL   |
| 褐色 | L    |
| 褐色 | XL   |
| 褐色 | XXL  |

## <a name="the-version-product-dimension"></a>版本产品维度

版本是用于帮助您维护和跟踪整个供应链中产品的多个版本的产品维度。 对于在不断缩短的产品生命周期、质量和可靠性要求提高，以及对产品安全的关注增加的世界中经营业务的制造商，如果要取得成功，版本跟踪至关重要。

作为标准产品维度，版本的行为类似于现有产品尺寸（尺寸、样式、颜色和配置）。 因此，除了跟踪产品版本，您还可以将其用于其他目的。

### <a name="turn-on-the-version-dimension"></a><a name="enable-version-dim"></a>打开版本维度

#### <a name="before-you-turn-on-the-version-dimension"></a>在打开版本维度之前

当您打开版本维度时，如果您安装了向库存维度添加自定义的其他解决方案，某些功能可能会被破坏或无法按预期工作。 为了使版本维度正常工作，您可能必须更新这些解决方案，让它们在对库存维度的引用中包括版本维度。

在测试解决方案与版本维度的兼容性时，请关注以下要素：

1. **功能：** 最重要的是，必须评估涉及库存维度的所有自定义，以确保它们可以与版本维度一起使用。
1. **对库存维度的引用：** 注意对库存维度的引用（即明确引用尺寸的地方）。 对 `InventDimId` 的引用应该是自动完成的，但是要注意对样式或颜色的引用。 例如，请确保检查以下要素：

    - 扩展类中的 API 调用
    - 扩展代码中对特定库存维度的所有引用（此代码必须将版本维度与样式、颜色和尺寸维度安排在一起。）

1. **对过时 API 调用的引用：** 在引入版本维度时，Microsoft 已经尝试尽可能让更少的 API 过时。 当您打开 **产品维度 - 版本** 配置键时，极少数已过时的 API 会发出警告。 在生产系统中打开版本维度之前，必须在扩展解决方案中修复对这些 API 的调用。 以下是特定于版本的过时 API：

    - RetailTransactionServiceInventory::getProductRecordId
    - EcoResProductNumberIdentifiedProductVariantEntity::find
    - EGAISAlcoholProduction_RU::findByItemDim
    - PCVariantConfiguration::findByProductMasterAndDimensions

1. **地图：** 如果有任何地图使用库存维度，则必须更新这些地图的相应的关系映射，以使其包含版本维度。 在扩展模型或表扩展中，查找字段包含库存维度的表。
1. **Microsoft Dynamics 365 Commerce 功能：** 打开后，版本维度将出现在 Dynamics 365 Supply Chain Management 中特定于 Commerce 的代码中。 但是，Commerce 渠道数据库、销售点 (POS) 或电子商务应用程序尚不支持版本维度。 这些特定于 Commerce 的应用程序将不支持用户按版本维度销售/装运或退回/接收库存。 库存可用性查询功能不会在 Commerce 应用中按版本维度识别库存。 此行为类似于当前整个 Commerce 中的配置维度的行为。

#### <a name="turn-on-the-version-dimension"></a>打开版本维度

版本维度只有在系统中打开之后才能使用。 此任务需要管理员权限。

1. 转到 **系统管理 \> 工作区 \> 功能管理**。
1. 打开名为 *产品维度版本* 的功能。 （有关详细信息，请参阅[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。）
1. 将您的系统设置为[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)。
1. 转到 **系统管理 \> 设置 \> 许可证配置**。
1. 在 **配置键** 选项卡上，展开 **贸易**，选中 **产品维度 - 版本** 的复选框。
1. 关闭[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)。

### <a name="areas-where-the-version-dimension-isnt-supported"></a>版本维度不受支持的区域

以下区域不支持版本维度（您仍然可以使用这些区域，但无法向其中添加版本化产品(使用版本维度的产品)）。 例如，您不能将版本化物料添加到供应商目录。 这是因为将使用版本维度的产品添加到这些区域会导致中断性变更。

- 成本对象月报表
- 成本对象报表缓存
- 按物料划分的 MCR 销售统计信息
- 供应商目录
- EcoResProductDimensionGroupEntity

此外，Commerce 中的订单创建和订单处理功能（例如，POS、呼叫中心和电子商务订单）也不支持版本维度。 对于何时增强 Commerce 订单以支持版本维度没有确定的时间线。

### <a name="functional-characteristics-of-the-version-dimension"></a>版本维度的功能特征

版本维度的工作方式与其他产品维度相同。 但是，由于特定的性质，并且由于目的是维护和跟踪产品的多个版本，因此它的行为略有不同。 以下是一些异同点：

- **没有版本组。**

    虽然尺寸、颜色和样式（颜色组、尺寸组和样式组）存在组概念，但是不存在版本组概念。 通过组，您可以预定义适用的值，以比如在为产品分配颜色组时，产品可以使用该颜色组中的所有颜色。 此概念不适用于版本维度，因为产品采用的版本不是在创建产品时预定义的。 而是根据需要在产品的生命周期内创建的。 通常，如果产品的形式、适合度和功能保持不变，将创建新版本而不是新产品。

- **产品变型建议的工作方式与目前相同。**

    产品变型建议将为所有版本维度值创建建议，就像为其他维度创建建议一样。 创建和发布版本化产品的流程与使用其他维度的产品相同。 当您创建版本化产品时，第一个版本 (V1) 将创建为产品维度，并会发布变型。 当产品更改，需要新版本时，将增加新版本值 (V2)，并发布所需的变型。 预期不会为产品预先创建所有版本（V1、V2 和 V3）。

> [!IMPORTANT]
> 如果您打开并使用版本维度，某些引用库存维度的解决方案可能会如预期的停止工作。 要确认并解决这些问题，请与独立软件供应商 (ISV) 联系，告知受影响的解决方案。 有关详细信息，请参阅[启用版本维度](#enable-version-dim)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
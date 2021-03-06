---
title: 购买框模块
description: 此主题介绍购买框模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: dce3c8adcd2926e60d001bddb5c278fac6860268
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796214"
---
# <a name="buy-box-module"></a>购买框模块

[!include [banner](includes/banner.md)]

此主题介绍购买框模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

术语 *购买框* 通常指的是产品详细信息页中的“第一屏”区域，用于承载进行产品购买所需全部最重要信息。 （“第一屏”区域在首次加载页面时显示，所以用户不必向下滚动即可看到。）

购买框模块是特殊容器，用于承载产品详细信息页购买框区域中显示的所有模块。

产品详细信息页的 URL 中包含产品 ID。 显示购买框模块所需全部信息派生自此产品 ID。 如果不提供产品 ID，则不能在页面中正确显示购买框模块。 因此，购买框模块只能在具有产品上下文的页面上使用。 要在没有产品上下文的页面（例如，主页或市场营销页面）上使用它，您必须进行其他自定义。

下图显示了产品详细信息页上的购买框模块的示例。

![购买框模块的示例](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a>购买框模块属性和插槽 

在产品详细信息页，购买框拆分为两个区域：左侧媒体区域，右侧内容区域。 默认情况下，媒体区域列的宽度与内容区域列的宽度之比为 2:1。 在移动设备上，这两个区域堆叠，所以一个区域在另一个区域下方显示。 主题可用于自定义列宽和堆叠等级。

购买框模块呈现产品的标题、描述、价格和等级。 还可以让客户选择具有不同产品属性（例如尺寸、样式和颜色）的产品变型。 如果选择了产品变型，将更新购买框中的其他属性（如产品描述和图像）以反映变型信息。 

提供数量选择器，以便客户可以指定要购买的商品数量。 可以在站点设置中定义可以购买的最大数量。

客户还可以从购买框中执行一些操作，例如将产品添加到购物车，将产品添加到其愿望列表以及选择取货地点。 可以在产品或产品变型上执行这些操作。 要将产品添加到愿望列表中，客户必须先登录。

主题可用于删除或更改购买框产品属性和操作控件的顺序。 

## <a name="module-properties"></a>模块属性

- **标题标签** – 此属性定义产品标题的标题标签。 如果购买框位于页面顶部，则此属性应设置为 **h1** 以达到可访问性标准。 

- **启用“购买相似外观产品”建议** - 此属性允许购买框显示与最近所查看商品外观类似的产品的链接。 Commerce 版本 10.0.13 及更高版本中提供此功能。

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>购买框模块中可使用的模块

- **媒体库** – 此模块用于展示产品详细信息页上的产品图像。 有关此模块的详细信息，请参阅[媒体库模块](media-gallery-module.md)。
- **商店选择器** – 此模块显示附近可提货的商店的列表。 它使用户可以输入位置来查找附近的商店。 有关此模块的详细信息，请参阅[商店选择器模块](store-selector.md)。
- **社交共享** - 可将此模块添加到购买框，以便允许用户在社交媒体中共享产品信息。 有关详细信息，请参阅[社交共享模块](social-share-module.md)。

## <a name="buy-box-module-settings"></a>购买框模块设置

以下购买框模块设置可以在 **站点设置 \> 扩展** 中配置：

- **购物车行数量限制** – 此属于用于指定可以添加到购物车的每种项的最大数量。 例如，一位零售商可能决定一笔交易中只能出售每种产品 10 件。
- **库存** – 有关如何应用库存设置的信息，请参阅[应用库存设置](inventory-settings.md)。
- **将产品添加到购物车** - 此属性用于指定将物料添加到购物车后的行为。 可能的值为 **导航到购物车页面**、**不导航到购物车页面** 和 **显示通知**。 当此值设置为 **导航到购物车页面** 时，用户将在添加物料后转到购物车页面。 当此值设置为 **不导航到购物车页面** 时，用户在添加物料后不会转到购物车页面。 当此值设置为 **显示通知** 时，会向用户显示一条确认通知，用户可以继续在产品详细信息页面上浏览。 

> [!IMPORTANT]
> **将产品添加到购物车** 站点设置在 Dynamics 365 Commerce 10.0.11 版本中可用。 如果要从旧版本的 Dynamics 365 Commerce 更新，必须手动更新 appsettings.json 文件。 有关更新 appsettings.json 文件的说明，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。 

下图显示了 Fabrikam 站点上“已添加到购物车”确认通知的示例。

![通知模块示例](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit 交互

购买框模块使用 Commerce Scale Unit 应用程序编程接口 (API) 检索产品信息。 产品详细信息页中的产品 ID 用于检索所有信息。

## <a name="add-a-buy-box-module-to-a-page"></a>向页面添加购买框模块

若要向新页面添加购买框模块和设置必需的属性，请执行以下步骤。

1. 转到 **片段**，选择 **新建** 创建新片段。
1. 在 **新建片段** 对话框中，选择 **购买框** 模块。
1. 在 **片段名称** 下，输入名称 **购买框片段**，然后选择 **确定**。
1. 在购买框模块的 **媒体库** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **媒体库** 模块，然后选择 **确定**。
1. 在购买框模块的 **商店选择器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **商店选择器** 模块，然后选择 **确定**。
1. 选择 **保存**，选择 **完成编辑** 签入片段，然后选择 **发布** 进行发布。
1. 转到 **模板**，选择 **新建** 创建新模板。
1. 在 **新建模板** 对话框的 **模板名称** 下，输入 **PDP 模板**，然后选择 **确定**。
1. 在 **正文** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **默认页面** 模块，然后选择 **确定**。
1. 在默认页的 **主** 插槽中，选择省略号 (**...**)，然后选择 **添加片段**。
1. 在 **选择片段** 对话框中，选择您之前创建的 **购买框片段** 片段，然后选择 **确定**。
1. 选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。
1. 转到 **页面**，选择 **新建** 创建新页面。
1. 在 **选择模板** 对话框中，选择 **PDP 模板** 模板。 在 **页面名称** 下，输入 **PDP 页面**，然后选择 **确定**。
1. 在新页面的 **主** 插槽中，选择省略号 (**...**)，然后选择 **添加片段**。
1. 在 **选择片段** 对话框中，选择您之前创建的 **购买框片段** 片段，然后选择 **确定**。
1. 保存并预览页面。 在上一页的 URL 中添加查询字符串参数 **?productid=&lt;product id&gt;**。 这样，将把产品上下文用于加载和显示上一页。
1. 选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。 应该会在产品详细信息页显示一个购买框。

## <a name="additional-resources"></a>其他资源

[模块库概述](starter-kit-overview.md)

[商店选择器模块](store-selector.md)

[媒体库模块](media-gallery-module.md)

[容器模块](add-container-module.md)

[购物车模块](add-cart-module.md)

[结帐模块](add-checkout-module.md)

[订单确认模块](order-confirmation-module.md)

[标题模块](author-header-module.md)

[页脚模块](author-footer-module.md)

[社交共享模块](social-share-module.md)

[计算零售渠道的库存现有量](calculated-inventory-retail-channels.md)

[SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
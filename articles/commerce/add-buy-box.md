---
title: 购买框模块
description: 此主题介绍购买框模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 095374c14cddf1ae3608ae1427a7144b3e7ca7b2
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269743"
---
# <a name="buy-box-module"></a>购买框模块


[!include [banner](includes/banner.md)]

此主题介绍购买框模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

术语*购买框*通常指的是产品详细信息页中的“第一屏”区域，用于承载进行产品购买所需全部最重要信息。 （“第一屏”区域在首次加载页面时显示，所以用户不必向下滚动即可看到。）

购买框模块是特殊容器，用于承载产品详细信息页购买框区域中显示的所有模块。

产品详细信息页的 URL 中包含产品 ID。 显示购买框模块所需全部信息派生自此产品 ID。 如果不提供产品 ID，则不能在页面中正确显示购买框模块。 因此，购买框模块只能在具有产品上下文的页面上使用。 要在没有产品上下文的页面（例如，主页或市场营销页面）上使用它，您必须进行其他自定义。

## <a name="buy-box-module-properties-and-slots"></a>购买框模块属性和插槽 

在产品详细信息页，购买框拆分为两个区域：左侧媒体区域，右侧内容区域。 默认情况下，媒体区域列的宽度与内容区域列的宽度之比为 2:1。 在移动设备上，这两个区域堆叠，所以一个区域在另一个区域下方显示。 主题可用于自定义列宽和堆叠等级。

购买框模块呈现产品的标题、描述、价格和等级。 还可以让客户选择具有不同产品属性（例如尺寸、样式和颜色）的产品变型。 如果选择了产品变型，将更新购买框中的其他属性（如产品描述和图像）以反映变型信息。 

提供数量选择器，以便客户可以指定要购买的商品数量。 可以在站点设置中定义可以购买的最大数量。

客户还可以从购买框中执行一些操作，例如将产品添加到购物车，将产品添加到其愿望列表以及选择取货地点。 可以在产品或产品变型上执行这些操作。 要将产品添加到愿望列表中，客户必须先登录。

主题可用于删除或更改购买框产品属性和操作控件的顺序。 

## <a name="module-properties"></a>模块属性

- **标题标签** – 此属性定义产品标题的标题标签。 如果购买框位于页面顶部，则此属性应设置为 **h1** 以达到可访问性标准。 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>购买框模块中可使用的模块

- **媒体库** – 此模块用于展示产品详细信息页上的产品图像。 它可以支持一到多个图像。 还支持缩略图。 缩略图可以水平排列（作为图像下的一行），或垂直排列（作为图像旁边的一列）。 可将媒体库模块添加到购买框模块中的**媒体**插槽。 它当前仅支持图像。 
- **商店选择器** – 此模块显示附近可提货的商店的列表。 它使用户可以输入位置来查找附近的商店。 有关此模块的详细信息，请参阅[商店选择器模块](store-selector.md)。

## <a name="buy-box-module-settings"></a>购买框模块设置

购买框模块中有可在**站点设置 \> 扩展**中配置的三个设置：

- **最大数量** – 此属于用于指定可以添加到购物车的每种项的最大数量。 例如，一位零售商可能决定一笔交易中只能出售每种产品 10 件。
- **库存检查** – 如果此值设置为 **True**，则只有在购买框模块确信某种项有现货时，才能将此项添加到购物车中。 将在物料发货时和在商店中提货时执行库存检查。 如果此值设置为 **False**，则向购物车添加项和下订单前，不进行库存检查。 有关如何配置后端库存设置的信息，请参阅[计算零售渠道的库存现有量](calculated-inventory-retail-channels.md)。

- **库存缓冲区** – 此属性用于指定库存的缓冲区号。 库存会被实时维护，如果多位客户下订单，则很难维持精确的库存计数。 进行库存检查时，如果库存比缓冲区数量少，则将产品视为库存不足。 因此，当通过多个渠道快速进行销售，导致库存计数无法充分同步时，出售库存不足的项的风险较低。

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit 交互

购买框模块使用 Commerce Scale Unit API 检索产品信息。 产品详细信息页中的产品 ID 用于检索所有信息。

## <a name="add-a-buy-box-module-to-a-page"></a>向页面添加购买框模块

若要向新页面添加购买框模块和设置必需的属性，请执行以下步骤。

1. 创建一个名称为**购买框片段**的片段，然后向其添加一个购买框模块。
1. 在该购买框模块的**媒体**插槽中，添加一个媒体库模块。
1. 在购买框模块的**商店选择器**插槽中，添加商店选择器模块。
1. 选择**保存**，选择**完成编辑**签入片段，然后选择**发布**进行发布。
1. 为产品详细信息页创建一个模块，然后命名为 **PDP 模板**。
1. 添加默认页。
1. 在默认页的**主**插槽中，添加一个购买框片段。
1. 选择**保存**，选择**完成编辑**签入模板，然后选择**发布**进行发布。
1. 使用您刚才创建的模板创建一个名称为 **PDP 页**的页面。
1. 在新页的**主**插槽中，添加一个购买框片段。
1. 保存并预览页面。 在上一页的 URL 中添加查询字符串参数 **?productid=&lt;product id&gt;**。 这样，将把产品上下文用于加载和显示上一页。
1. 选择**保存**，选择**完成编辑**签入页面，然后选择**发布**进行发布。 应该会在产品详细信息页显示一个购买框。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[商店选择器模块](store-selector.md)

[容器模块](add-container-module.md)

[购物车模块](add-cart-module.md)

[购物车图标模块](cart-icon-module.md)

[结账模块](add-checkout-module.md)

[订单确认模块](order-confirmation-module.md)

[标题模块](author-header-module.md)

[页脚模块](author-footer-module.md)

[计算零售渠道的库存现有量](calculated-inventory-retail-channels.md)

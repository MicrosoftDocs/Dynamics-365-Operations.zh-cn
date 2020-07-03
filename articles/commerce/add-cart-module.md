---
title: 购物车模块
description: 此主题介绍购物车模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3ba46fd90507a9cf8da92598c8449a2e553da352
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411265"
---
# <a name="cart-module"></a>购物车模块

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍购物车模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

购物车模块显示客户继续结帐之前已添加到购物车中的物品。 此模块还显示订单摘要，并让客户可以应用或删除促销代码。

购物车模块支持登录结帐和访客结帐。 它还支持**返回购物**链接。 您可以在**站点设置 \> 扩展 \> 路由**中为此链接配置路由。

购物车模块根据购物车 ID 呈现数据，购物车 ID 是整个站点可用的浏览器 cookie。 

下图显示了 Fabrikam 站点上购物车页面的示例。

![购物车模块的示例](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a>购物车模块属性和插槽

购物车模块有一个**标题**属性，此属性可以设置为**购物袋**和**购物车中的商品**之类的值。 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>购物车模块中可使用的模块

- **文本块** – 此模块支持购物车模块中的自定义消息。 消息由内容管理系统 (CMS) 驱动。 可以添加任何消息，如“订单问题请致电 1-800-Fabrikam”。
- **商店选择器** – 此模块显示附近可提货的商店的列表。 它使用户可以输入位置来查找附近的商店。 有关此模块的详细信息，请参阅[商店选择器模块](store-selector.md)。

## <a name="module-properties"></a>模块属性

以下购物车模块设置可以在**站点设置 \> 扩展**中配置：

- **最大数量** – 此属于用于指定可以添加到购物车的每种项的最大数量。 例如，一位零售商可能决定一笔交易中只能出售每种产品 10 件。
- **库存** – 有关如何应用库存设置的信息，请参阅[应用库存设置](inventory-settings.md)。
- **返回购物** – 该属性用于指定**返回购物**链接的路由。 可以在站点级别配置路由，让零售商可以将客户带回到站点的主页或其他任何页面。

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit 交互

购物车模块使用 Commerce Scale Unit API 检索产品信息。 浏览器 cookie 中的购物车 ID 用于从 Commerce Scale Unit 检索所有产品信息。

## <a name="add-a-cart-module-to-a-page"></a>向页面添加购物车模块

若要向新页面添加购物车模块和设置必需的属性，请执行以下步骤。

1. 转到**页面片段**，选择**新建**创建新片段。
1. 在**新建页面片段**对话框中，选择**购物车**模块。
1. 在**页面片段名称**下，输入名称**购物车片段**，然后选择**确定**。
1. 选择**购物车**插槽。
1. 在右侧的属性窗格中，选择铅笔符号，在字段中输入标题文本，然后选择复选标记符号。
1. 在**购物车**插槽中，选择省略号 (**...**)，然后选择**添加模块**。
1. 在**添加模块**对话框中，选择**商店选择器**模块，然后选择**确定**。
1. 选择**保存**，选择**完成编辑**签入片段，然后选择**发布**进行发布。
1. 转到**模板**，选择**新建**创建新模板。
1. 在**新建模板**对话框的**模板名称**下，为模板输入名称。
1. 在大纲树中，选择**正文**插槽，选择省略号 (**...**)，然后选择**添加片段**。
1. 在**选择页面片段**对话框中，选择**购物车片段**片段，然后选择**确定**。
1. 选择**保存**，选择**完成编辑**签入模板，然后选择**发布**进行发布。
1. 转到**页面**，选择**新建**创建新页面。
1. 在**选择模板**对话框中，选择您创建的模板，输入页面名称，然后选择**确定**。
1. 选择**保存**，然后选择**预览**以预览页面。
1. 选择**完成编辑**签入页面，然后选择**发布**进行发布。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[容器模块](add-container-module.md)

[商店选择器模块](store-selector.md)

[购买框模块](add-buy-box.md)

[购物车图标模块](cart-icon-module.md)

[结账模块](add-checkout-module.md)

[订单确认模块](order-confirmation-module.md)

[标题模块](author-header-module.md)

[页脚模块](author-footer-module.md)

[计算零售渠道的库存现有量](calculated-inventory-retail-channels.md)

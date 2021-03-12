---
title: 为客户订单启用多种提货交货方式
description: 本主题介绍 Microsoft Dynamics 365 Commerce 中的功能，可让您创建要在商店提货的客户订单。
author: hhainesms
manager: annbe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 768b20ecc8d15353258c9b3af69b897957d3de60
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594944"
---
# <a name="enable-multiple-pickup-delivery-modes-for-customer-orders"></a>为客户订单启用多种提货交货方式

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

在 Microsoft Dynamics 365 Commerce 版本 10.0.16 及更高版本中，组织可以定义多种交货方式，以供购物者或销售助理创建将在商店提货的订单时进行选择。 这样，组织可以向购物者提供多种提货选项。 例如，许多零售商现在针对其订单向购物者提供店内提货或懒人提货的选项。 Commerce 支持配置这些不同的提货交货方式。 然后，用户可以在任何受支持的 Commerce 渠道（电子商务、呼叫中心或商店）中创建客户订单时利用它们。

## <a name="enable-and-configure-pickup-delivery-modes"></a>启用和配置多种提货交货方式

若要使用此功能，请在 Commerce 总部中在 **功能管理** 工作区中打开 **支持多种提货交货方式** 功能。 打开该功能后，需要其他配置。

在 Commerce 版本 10.0.15 及更早版本中，组织只能定义一种交货方式作为指定的提货交货方式。 此定义在 **Commerce 参数** 页面上完成。 在版本 10.0.16 及更高版本中，当您打开 **支持多种提货交货方式** 功能时，之前在 **Commerce 参数** 页面上定义为提货交货方式的交货方式将自动复制到提货交货方式的新配置中。

![Commerce 参数页面上的提货交货方式](media/multiplepickupparameter.png)

打开 **支持多种提货交货方式** 功能后，您可以在 **Commerce 参数** 页面的 **客户订单** 选项卡上，在 **交货方式** 快速选项卡的 **提货交货方式** 网格中，定义多种提货交货方式。

**自提交货方式** 和 **电子交货方式** 字段以及 **仅显示装运订单的承运人模式选项** 选项已重新位于此快速选项卡上。

在配置其他提货交货方式之前，必须先定义交货方式。 在 Commerce 总部的 **交货方式** 页面中，添加应视为提货交货方式的交货方式。 确保所有配置均已完成。 例如，确保交货方式链接到适当的渠道和物料。 完成后，运行 **处理交货方式** 作业以在交货方式、渠道和物料之间创建关系。 在作业完成运行后，在 Commerce 总部中打开 **配送计划** 页面，然后运行 **1120** 配送作业，以确保使用新的交货方式配置更新相关的 Commerce 渠道数据库。

![懒人提货的交货方式的示例](media/pickupmodes.png)

定义其他提货交货方式后，在 **Commerce 参数** 页面上将它们添加到 **提货交货方式** 网格。 然后，运行适当的配送作业，以使用配置更改更新相关的 Commerce 渠道数据库。

> [!NOTE]
> 除了在打开 **支持多种提货交货方式** 功能时复制到 **提货交货方式** 网格的现有提货交货方式外，对于您创建的每个其他提货交货方式配置，您应该配置新的交货方式。 当您将交货方式添加到 **提货交货方式** 网格时，Commerce 会验证是否有任何活动的未结销售行已使用它们。 如果找到任何未结销售行，您将收到错误消息。 直到使用交货方式的所有未结销售行已结算（已开票或已取消），才将其视为提货交货方式。

> [!IMPORTANT]
> 在 **Commerce 参数** 页面上定义多种提货交货方式后，**支持多种提货交货方式** 功能将成为强制性功能，无法再关闭。 如果必须关闭此功能，请从 **提货交货方式** 窗格中删除除一个之外的所有提货交货方式。 如果仅定义了一种提货交货方式，该功能将不再视为强制性功能，并且可以关闭。

### <a name="e-commerce-site-configurations"></a>电子商务站点配置

当打开 **支持多种提货交货方式** 功能时，电子商务页面上的以下模块将显示新的提货交货方式，配置如下：

- 购买框
- 商店选择器
- 购物车
- 选择信息
- 订单确认
- 订单明细

若要使提货交货方式可用，无需在电子商务页面上执行其他步骤。

## <a name="work-with-multiple-pickup-delivery-modes"></a>使用多种提货交货方式

如果多种提货交货方式可用于渠道，当客户购买将要提货的产品时，将为他们提供增强的体验。 

- 在电子商务渠道中，购物者可以选择任何可用的有效提货交货方式。 例如，零售商定义两种提货交货方式（店内提货和懒人提货），二者均在 **提货交货方式** 网格中配置，并且对订单履行渠道和购物者当前购买的产品均有效。 在这种情况下，购物者可以选择他们喜欢的提货交货方式。 然后，当在 Commerce 总部中创建订单时，所选的提货交货方式将成为链接到销售订单行的交货方式。

    ![在电子商务中选择提货选项](media/pickupecommerce.png)

- 在商店渠道中，如果通过销售点 (POS) 应用程序创建提货的客户订单，将提示销售助理在可用的提货交货方式（如果已配置方式）中进行选择。 如果只有一种有效的提货交货方式可用于渠道和物料，则不会提示销售助理选择它。 相反，可用提货交货方式将自动应用到订单行。

    ![在 POS 应用程序中选择提货选项](media/pickuppos.png)

- 在呼叫中心渠道中，当用户创建提货订单时，他们可以手动选择链接到呼叫中心渠道的任何定义的提货交货方式。 然后，系统验证是否可以在订购要链接到它的物料时使用所选的提货交货方式。 当在呼叫中心渠道中选择提货交货方式时，必须将销售订单行链接到有效的商店仓库。 如果在呼叫中心销售行上定义了非商店仓库，无法在该销售行上设置提货交货方式。
- 销售助理可以在 POS 应用程序中使用 **订单撤回** 或 **订单履行** 操作，以检索提货的订单或订单行的列表。 如果销售助理使用预定义的搜索筛选器显示将在当前商店中提货的所有订单，将修改查询以确保搜索结果包括使用任何提货交货方式的所有符合资格的订单。 POS 用户还可以使用现有筛选器将订单列表缩小到特定的提货交货方式。 例如，他们只能显示懒人提货的订单。

    ![适用于撤回订单列表的提货交货方式的筛选器](media/pickuprecallorder.png)

## <a name="considerations-for-distributed-order-management"></a>分配的订单管理 (DOM) 的注意事项

Commerce 中的[分配的订单管理 (DOM)](https://docs.microsoft.com/dynamics365/commerce/dom) 功能会忽略标记为商店提货的所有销售行。 这些功能已更新，以确保链接到已配置的提货交货方式的销售行会绕过 DOM 逻辑，并且不会重新分配到新的履行仓库。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
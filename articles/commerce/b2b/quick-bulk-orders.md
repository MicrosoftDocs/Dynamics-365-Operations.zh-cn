---
title: 快速完成 B2B 网站下单
description: 本主题介绍使企业到企业 (B2B) 站点用户可以快速完成批量和重复下单的 Microsoft Dynamics 365 Commerce 功能。
author: shajain
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 8ac4833b2ca05e90b4019ffdfc4b669c542b0cf6
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686538"
---
# <a name="place-b2b-website-orders-quickly"></a>快速完成 B2B 网站下单

[!include [banner](../../includes/banner.md)]

本主题介绍使企业到企业 (B2B) 站点用户可以快速完成批量和重复下单的 Microsoft Dynamics 365 Commerce 功能。

Dynamics 365 Commerce B2B 电子商务网站允许用户执行标准操作，如通过搜索和浏览发现新产品、查看产品详细信息、将商品添加到购物车以及结帐。但是，企业对消费者 (B2C) 站点的客户通常只订购少量的商品且仅订购一次，而 B2B 客户通常订购大量商品并会多次再次订购。 因为这些客户通常确切地知道他们想要购买什么商品，所以他们通常会跳过产品发现阶段，直接进行订购。 为了满足这些客户的需求，Commerce B2B 电子商务网站提供了各种功能，帮助他们快速下订单。

## <a name="bulk-order-by-item-number"></a>按物料编号批量订购

Commerce B2B 电子商务网站允许站点用户通过输入产品物料编号和所需数量来将商品添加到购物车。

下图显示了按产品物料编号快速输入订单的示例。

![按产品物料编号快速输入订单。](../media/QuickAddByItem.png)

## <a name="bulk-order-by-variant"></a>按变型批量订购

Commerce B2B 电子商务网站让站点用户可以在单个视图中快速添加同一产品的不同变型，该视图按尺寸、颜色和样式显示库存可用性。 此外，站点用户还可以通过选择 **输入所有数量** 轻松地为所有有存货产品输入相同的数量。

下图显示了使用“输入所有数量”功能快速输入订单的示例。

![使用“输入所有数量”功能快速输入订单。](../media/MatrixView.png)

## <a name="use-order-templates-for-quick-order-entry"></a>使用订单模板快速输入订单

B2B 网站上的买方经常一起订购特定商品。 例如，如果您正在为建筑工地下订单，您可能希望同时订购衬衫、夹克、裤子、鞋子和帽子。 如果您正在为医院下订单，那里的医生、护士和清洁人员有不同的制服，您可能希望将每种制服类型组合在一起来更方便地订购。 对于这些类型的场景，Commerce B2B 站点支持创建订单模板。 站点用户可以创建任意数量的自定义模板，然后根据需要从这些模板中订购全部或部分商品。

下图显示了订单模板的示例。

![订单模板的示例。](../media/OrderTemplateHeader.png)

下图显示了订单模板的详细信息视图示例。

![订单模板的详细信息视图的示例。](../media/OrderTemplateLines.png)

## <a name="reorder-from-order-history"></a>从订单历史记录再次订购

Commerce B2B 电子商务网站让站点用户可以从他们的订单历史记录快速再次订购商品。 站点用户可以从他们的订单历史记录购买选定的商品，也可以将所有以前购买的商品添加到购物车中。

下图显示了用户订单历史记录的示例以及从其再次订购商品的选项。

![从订单历史记录再次订购。](../media/Reorder.png)

本主题仅介绍了 Commerce B2B 站点帮助用户快速查找、订购和再次订购所需产品的一些方式。 更多功能正在开发中，可以进一步简化捕获批量订单的流程。

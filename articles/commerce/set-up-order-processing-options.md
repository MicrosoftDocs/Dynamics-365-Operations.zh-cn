---
title: 设置呼叫中心渠道
description: 本文提供有关如何使用 Dynamics 365 Commerce 来处理呼叫中心的订单的信息。
author: josaw1
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCROrderParameters, MCRSalesTableOrderHistory, SalesOrderProcessingWorkspace
audience: Application User
ms.reviewer: josaw
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c6d21385d956534c799af5b9e20a54c9970da368
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854863"
---
# <a name="set-up-call-center-channels"></a>设置呼叫中心渠道

[!include [banner](includes/banner.md)]

一家公司可在 Dynamics 365 Commerce 中定义多个呼叫中心渠道。 呼叫中心渠道在 **Retail 和 Commerce** \> **渠道** \> **呼叫中心** \> **所有呼叫中心** 中配置，并特定于法人。

创建新的呼叫中心渠道之后，系统将自动为其分配运营单位编号。 由于呼叫中心创建为运营单位，所以用户可将呼叫中心渠道链接至各种 Commerce 功能，如分类、目录和特定交货方式。

可以为呼叫中心渠道配置默认仓库。 然后，在该渠道中创建销售订单时，将在销售订单头中自动输入默认仓库，除非已对为销售订单选择的客户定义了另一个仓库。 在此情况下，默认输入该客户的仓库。

用户必须链接至呼叫中心渠道，才能使用呼叫中心的功能。 将把用户创建的所有销售订单自动链接至该用户的呼叫中心渠道。 现在，不能将一位用户同时链接至多个呼叫中心渠道。

也可以为呼叫中心渠道配置电子邮件通知配置文件。 此配置文件定义将电子邮件发送到通过呼叫中心渠道下单的客户时使用的电子邮件模板组。 可以配置针对系统事件（如提交订单或为订单发货）的电子邮件触发器。

必须为渠道定义正确的[付款方式](/dynamics365/unified-operations/retail/work-with-payments)和交货方式，才能通过呼叫中心渠道正确处理销售订单。

可以在呼叫中心渠道级别定义与将链接到该渠道创建的订单的财务维度有关的其他默认值。

## <a name="options-for-order-processing-behavior"></a>订单处理行为的选项

呼叫中心配置中的三项设置对针对该呼叫中心创建的销售订单的可用特性和功能效果显著：**启用订单完成**、**启用直接销售** 和 **启用价格订单控制**。

### <a name="enable-order-completion"></a>启用订单完成

呼叫中心渠道的 **启用订单完成** 设置对为该渠道输入的销售订单的订单处理流程效果显著。 如果开启了此设置，则所有销售订单先运行一组验证规则，才能予以确认。 这些规则的运行方法是选择销售订单页操作窗格上添加的 **完成** 按钮。 必须为开启了 **启用订单完成** 设置后创建的所有销售订单执行订单完成流程。 此流程实施付款和付款验证逻辑的捕获。 除了实施付款，订单提交流程还可以触发系统中配置的[欺诈检查](/dynamics365/unified-operations/retail/set-up-fraud-alerts)。 将保留付款失败或未通过欺诈验证的订单，解决了导致保留的问题之前，不能发放此类订单进行更进一步的处理（如拣货或发货）。

在为呼叫中心渠道开启了 **启用订单完成** 设置后，如果在销售订单中输入了行项，而渠道用户尝试关闭或离开销售订单窗体但未先选择 **完成**，系统将通过通过打开销售订单概括页并要求用户正确提交订单，实施订单完成流程。 如果不能与付款一起正确提交订单，则用户可使用[订单保留](/dynamics365/unified-operations/retail/work-with-order-holds)功能保留订单。 如果用户要尝试取消订单，则必须正确取消，方法是使用“取消”功能或“删除”功能，具体取决于用户的安全设置允许的功能。

如果为呼叫中心渠道开启了 **启用订单完成** 设置，将在订单中跟踪 **付款状态** 字段。 提交销售订单时，系统将计算 **付款状态**。 仅允许系统对已审核付款状态的订单执行更多订单处理步骤，如拣货和发货。 如果拒绝了付款，将为详细订单状态启用 **请勿处理** 标志，从而保留订单，直到解决了付款问题。

此外，如果开启了 **启用订单完成** 设置，则当用户创建销售订单且处于行项录入模式时，主销售订单头上的 **来源** 字段将可用。 **来源** 字段用于在直接营销销售场景中捕获[目录源代码](/dynamics365/unified-operations/retail/call-center-catalogs)。 然后，此代码可促成特价和促销。

即使关闭了 **启用订单完成** 设置，用户仍然可以为销售订单应用源代码。 但是，必须首先打开销售订单头详细信息以访问 **来源** 字段。 换言之，还需要单击几次。 同样的行为适用于发货完成和已加速的订单之类功能。 这些功能可用于呼叫中心中创建的所有订单。 但是，如果开启了 **启用订单完成** 设置，则用户在行录入视图中时，可在销售订单头中看到这些功能的配置。 无需深入到销售订单头详细信息，即可找到相应设置和字段。

> [!NOTE]
> 启用 **全渠道 Commerce 订单付款** 功能后，呼叫中心 **启用订单完成** 按钮将在 **Retail 和 Commerce \> 渠道 \> 呼叫中心** 的 **常规** 快速选项卡上在总部中隐藏。

### <a name="enable-direct-selling"></a>启用直接销售

如果为呼叫中心渠道开启了 **启用直接销售** 设置，则用户可利用 Commerce 的追加销售和交叉销售功能。 在此情况下，订单录入期间将显示弹出窗口，并推荐呼叫中心用户可向客户提供的其他产品。 推荐的产品基于销售订单行中刚输入的产品。 现在，在物料级别为产品或目录配置追加销售和交叉销售推荐。 如果为呼叫中心渠道关闭了 **启用直接销售** 设置，则订单录入期间不显示弹出窗口，即使为正在订购的物料定义了有效的追加销售或交叉销售也不例外。

如果开启了 **启用直接销售** 设置，也将开启销售订单录入页的脚本和图像功能。 在此情况下，订单录入期间该页右侧的信息面板可用。 此面板可显示与常规订单录入流程有关的脚本，应用的目录源代码，或与正在订购的物料有关的脚本。 此外，如果在产品设置中为正在订购的物料定义了图像，则图像面板可显示这些物料的产品图像。

### <a name="enable-order-price-control"></a>启用订单价格控制

如果开启了 **启用订单价格控制** 设置，则只有授权用户可在订单录入期间更改无论的销售价格。 更改应在定义的容差范围内。 未获得正确授权的用户必须改为申请价格更改。 然后，将通过系统的审核和批准工作流处理该申请。

## <a name="channel-users"></a>渠道用户

定义呼叫中心渠道时，必须将渠道用户链接到呼叫中心。 否则不能在系统中使用呼叫中心。 用户登录 Commerce 并在与订单录入有关的页面中输入销售订单或退货单时，将针对呼叫中心渠道的配置验证其用户 ID。 如果用户已链接到特定呼叫中心渠道，则用户创建的订单将继承该渠道的特性和默认值。

默认情况下，将在销售订单头上为呼叫中心用户创建的所有订单开启 **销售** 标志。 然后，这些订单可利用系统的商业特定价格和促销功能。


未链接到呼叫中心渠道的用户则使用 Microsoft Dynamics 365 Finance 的标准订单录入功能。 系统将不会把这些用户通过销售订单录入窗体输入的订单识别为 Commerce 订单。 此外，这些用户输入的这些订单将不应用任何订单完成处理规则、定价逻辑，或可在呼叫中心渠道配置或呼叫中心系统参数中定义的其他订单验证。

完成呼叫中心渠道配置和渠道用户定义之后，要帮助确保所需系统行为，请务必在 **Retail 和 Commerce** \> **渠道设置** \> **呼叫中心设置** \> **呼叫中心参数** 中定义所有必需的呼叫中心参数。 请确保还定义相关编号规则。

> [!NOTE]
> 要使用呼叫中心功能，**多次收货** 的配置键必须启用。 可以在 **系统管理** \> **设置** \> **许可证配置** 下的 **贸易配置** 键中找到此配置键。 由于呼叫中心功能会根据在销售订单行级别配置的交货地址执行各种验证，因此这是必需的。 



[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: 在销售点 (POS) 启用客户登记通知
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 销售点 (POS) 启用客户登记通知。
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b42dc7766f8a69a7409c28d21b49cc96eca18dd4
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271417"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>在销售点 (POS) 启用客户登记通知

[!include [banner](includes/banner.md)]

本主题介绍如何在 Microsoft Dynamics 365 Commerce 销售点 (POS) 启用客户登记通知。

在“订单可提货”电子邮件中，组织可以提供一个链接或按钮，让客户通知商店他们已经到达商店位置，在等待包裹出来。 然后，客户将收到登记确认，商店将在其 POS 应用程序中收到作为任务的通知。 此任务作为提醒销售助理将订单交到客户车辆处的提示。 因此，客户不必进入商店。

客户登记工作流也可以配置为从客户那里收集其他信息，如他们的停车位编号、车辆的品牌、型号和颜色以及交货说明。 零售商店服务员可以使用这些信息来推进订单履行。

## <a name="enable-customer-check-in"></a>启用客户登记

启用客户登记功能后，Commerce 会生成一个订单确认 ID（也称为渠道引用 ID）。 另外还会为通过销售点 (POS) 或呼叫中心渠道创建的订单生成订单确认 ID。 

要在 Commerce headquarters 中启用客户登记功能，请按照以下步骤操作。

1. 转到 **工作区 \> 功能管理**。
2. 搜索 **跨渠道生成一致的渠道引用 ID 格式** 功能。 
3. 选择该功能，然后在属性窗格中选择 **立即启用**。 

## <a name="create-a-check-in-confirmation-page"></a>创建登记确认页面

在您的电子商务站点上，您必须创建一个新页面，用作登记确认体验。 通过额外配置，此页面还可以包含一个表单，从客户那里收集其他信息来推进订单履行。 有关如何设置此页面和模块的信息，请参阅[客户登记模块](check-in-pickup-module.md)。

## <a name="configure-the-transactional-email-template"></a>配置交易电子邮件模板

您必须在模板上添加 **我在这里** 链接或按钮，指向客户在订单准备好可以提货时收到的交易电子邮件。 客户将使用此链接或按钮通知商店，他们已经到达，可以提货。 

将此链接或按钮添加到映射到 **包装已完成** 通知类型和您用于路边订单履行的交货方式的模板中。 在模板中，创建一个 HTML 链接或按钮，指向您创建的登记确认页面的 URL。 下面是一个示例。

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
有关如何配置电子邮件模板的详细信息，请参阅[按交货模式自定义交易电子邮件](customize-email-delivery-mode.md)。 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>POS 中将创建登记确认任务

在客户通知商店他们在现场可以提货时，他们会收到登记确认通知，POS 中的任务列表中将为客户提货的商店创建一个任务。 此任务包含履行订单所需的所有客户和订单信息。 在任务中，说明字段显示通过其他信息表单从客户那里收集的所有信息。 

## <a name="additional-resources"></a>其他资源

[提货登记模块](check-in-pickup-module.md)

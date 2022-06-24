---
title: 启用销售点 (POS) 中的客户签入通知
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 销售点 (POS) 启用客户登记通知。
author: bicyclingfool
ms.date: 12/03/2021
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
ms.openlocfilehash: ae53657c95128eae793f670bd9dbc31d9fac0fe4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885137"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>启用销售点 (POS) 中的客户签入通知

[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 销售点 (POS) 启用客户登记通知。

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

将此链接或按钮添加到映射到 **包装已完成** 通知类型和您用于路边订单履行的交货方式的模板中。 在模板中，创建一个 HTML 链接或按钮，指向您创建的登记确认页面的 URL，并包含参数名称和值，如以下示例所示。

`<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%confirmationid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>`

有关如何配置电子邮件模板的详细信息，请参阅[按交货模式自定义交易电子邮件](customize-email-delivery-mode.md)。 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>POS 中将创建登记确认任务

在客户通知商店他们到场提货后，登记页面会显示一条确认消息和一个包含客户订单确认 ID 的可选 QR 码。 同时，将在 POS 中的任务列表中为客户提货的商店创建一个任务。 该任务包含履行订单所需的所有客户和订单信息。 任务的说明字段显示通过其他信息表单从客户那里收集的所有信息。

## <a name="end-to-end-testing"></a>端到端测试

客户登记需要将特定参数和值传递到登记页面，然后传递到客户登记 API。 因此，最简单的方法是在可以创建和打包测试订单的环境中测试此功能。 这样，可以生成具有包含所需参数名称和值的 URL 的“订单可提货”电子邮件。

要测试客户登记功能，请按照这些步骤操作。

1. 创建客户登记页面，然后添加和配置客户登记模块。 有关详细信息，请参阅[提货登记模块](check-in-pickup-module.md)。 
1. 签入页面，但不发布。
1. 将以下链接添加到由交货提货方式的打包完成通知类型调用的电子邮件模板。 有关详细信息，请参阅[创建交易事件的电子邮件模板](email-templates-transactions.md)。

    - **对于预生产 (UAT) 环境：** 添加本文前面[配置交易电子邮件模板](#configure-the-transactional-email-template)一节中的代码片段。
    - **对于生产环境：** 添加以下注释代码，以便现有客户不受影响。

        `<!-- https://[DOMAIN]/[CHECK_IN_PAGE]?channelReferenceId=%confirmationid%&channelId=%pickupchannelid%&packingSlipId=%packingslipid%&preview=inprogress -->`

1. 创建已指定交货提货方式的订单。
1. 当您收到由打包完成通知类型触发的电子邮件时，通过打开包含您之前添加的 URL 的登记页面来测试登记流。 由于 URL 包含 `&preview=inprogress` 标志，系统会提示您进行身份验证，然后才能查看页面。
1. 输入配置模块所需的任何其他信息。
1. 验证登记确认视图是否正确显示。
1. 为将要提货的商店打开 POS 终端。
1. 选择 **要提货的订单** 磁贴，验证订单是否出现。
1. 验证在登记模块中配置的任何其他信息是否出现在详细信息窗格中。

在您从头到尾验证客户登记功能可以正常工作后，按照以下步骤操作。

1. 发布登记页面。
1. 如果您在生产环境中进行测试，请在“订单可提货”电子邮件模板中取消对 URL 的注释，以显示 **我在这里** 链接或按钮。 然后重新上载模板。

## <a name="additional-resources"></a>其他资源

[提货登记模块](check-in-pickup-module.md)

[按交货模式自定义事务电子邮件](customize-email-delivery-mode.md)

[创建交易事件的电子邮件模板](email-templates-transactions.md)

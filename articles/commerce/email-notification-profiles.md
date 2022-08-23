---
title: 设置电子邮件通知配置文件
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中创建电子邮件通知配置文件。
author: bicyclingfool
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: db6c46d471e3b54982132df3e4819236833cf4a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292127"
---
# <a name="set-up-an-email-notification-profile"></a>设置电子邮件通知配置文件

[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中创建电子邮件通知配置文件。

创建渠道时，可以设置电子邮件通知配置文件。 电子邮件通知配置文件定义销售交易记录事件（如订单已创建、订单已包装和订单已开票事件），您将为这些事件向客户发送通知。 

有关其他电子邮件配置信息，请参阅[配置和发送电子邮件](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)。



## <a name="create-an-email-template"></a>创建电子邮件模板

必须先在 Commerce Headquarters 中为您要支持的每个通知类型创建组织电子邮件模板，然后才能启用电子邮件通知类型。 此模板针对每个支持的语言定义电子邮件主题、发件人、默认语言和电子邮件正文。

若要创建电子邮件模板，请执行以下步骤。

1. 在导航窗格中，转到 **模块 \> Retail and Commerce \> 总部设置 \> 参数 \> 组织电子邮件模板**。
1. 在操作窗格上，选择 **新建**。
1. 在 **电子邮件 ID** 字段中，输入 ID 以帮助识别此模板。
1. 在 **发件人名称** 字段中，输入发件人姓名。
1. 在 **电子邮件描述** 中，输入有意义的描述。
1. 在 **发件人电子邮件** 中，输入发件人电子邮件地址。
1. 在 **常规** 部分，为电子邮件模板选择默认语言。 当指定语言的本地化模板不存在时，将使用默认语言。
1. 展开 **电子邮件内容** 部分并选择 **新建** 以创建模板内容。 对于每个内容项，选择语言并提供电子邮件主题行。 如果电子邮件有正文，请确保选中 **有正文** 框。
1. 在操作窗格上，选择 **电子邮件** 以提供电子邮件正文模板。

下图显示了一些示例电子邮件模板设置。

![电子邮件模板设置。](media/email-template.png)

有关如何创建电子邮件模板的详细信息，请参阅[创建交易事件的电子邮件模板](email-templates-transactions.md)。 

## <a name="create-an-email-notification-profile"></a>创建电子邮件通知配置文件

要在 Headquarters 中创建电子邮件通知配置文件，请按照下列步骤操作。

1. 在导航窗格中，转到 **模块 \> Retail and Commerce \> 总部设置 \> Commerce 电子邮件通知配置文件**。
1. 在操作窗格上，选择 **新建**。
1. 在 **电子邮件通知配置文件** 字段中，输入名称以标识配置文件。
1. 在 **描述** 字段中，输入相关描述。
1. 将 **有效** 开关设置为 **是**。

## <a name="add-a-notification-type"></a>添加通知类型

若要创建电子邮件事件，请执行以下步骤。

1. 在导航窗格中，转到 **模块 \> Retail and Commerce \> 总部设置 \> Commerce 电子邮件通知配置文件**。
1. 在 **零售电子邮件通知设置** 下面，选择 **新建**。
1. 从下拉列表中选择合适的 **电子邮件通知类型**。
1. 从 **电子邮件 ID** 下拉列表中选择上面创建的电子邮件模板。
1. 选中 **有效** 复选框。
1. 在操作窗格上，选择 **保存**。

下图显示了一些示例事件通知设置。

![事件通知设置。](media/email-notification-profile.png)


## <a name="schedule-a-recurring-email-notification-process-job"></a>计划定期电子邮件通知流程作业

要发送电子邮件通知，您必须运行 **处理零售订单电子邮件通知** 作业。

要在 Headquarters 设置批处理作业以发送交易电子邮件，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 电子邮件和通知 \> 发送电子邮件通知**。
1. 在 **处理零售订单电子邮件通知** 对话框中，选择 **定期**。
1. 在 **定义定期** 对话框中，选择 **无结束日期**。
1. 在 **定期模式** 下，选择 **分钟**，然后将 **计数** 字段设置为 **1**。 这些设置将确保电子邮件通知被尽快处理。
1. 选择 **确定** 返回 **处理零售订单电子邮件通知** 对话框。
1. 选择 **确定** 完成作业设置。

## <a name="next-steps"></a>后续步骤

必须先配置出站邮件服务，然后才能发送电子邮件。 有关详细信息，请参阅[配置和发送电子邮件](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)。

## <a name="additional-resources"></a>其他资源

[配置和发送电子邮件](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[渠道概览](channels-overview.md)

[渠道设置先决条件](channels-prerequisites.md)

[组织和组织层次结构概览](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

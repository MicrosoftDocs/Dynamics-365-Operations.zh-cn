---
title: 设置电子邮件通知配置文件
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建电子邮件通知配置文件。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9e5d90eaf1815bbe54b0bea40d92a0a993a23b75
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113797"
---
# <a name="set-up-an-email-notification-profile"></a>设置电子邮件通知配置文件


[!include [banner](includes/banner.md)]

本主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建电子邮件通知配置文件。

## <a name="overview"></a>概览

在创建渠道之前，您需要设置一个配置文件，以确保可以针对各种事件发送电子邮件通知，例如订单创建、订单运送状态和付款失败。

有关其他电子邮件配置信息，请参阅[配置和发送电子邮件](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)。

## <a name="create-an-email-notification-profile"></a>创建电子邮件通知配置文件

要创建电子邮件通知配置文件，请按照下列步骤操作。

1. 在导航窗格中，转到**模块 \> Retail and Commerce \> 总部设置 \> Commerce 电子邮件通知配置文件**。
1. 在操作窗格中，单击**新建**。
1. 在**电子邮件通知配置文件**字段中，输入名称以标识配置文件。
1. 在**描述**字段中，输入相关描述。
1. 将**有效**开关设置为**是**。

### <a name="create-an-email-template"></a>创建电子邮件模板

在创建电子邮件通知之前，您必须创建一个组织电子邮件模板，其中包含发件人电子邮件信息和电子邮件模板。

若要创建电子邮件模板，请执行以下步骤。

1. 在导航窗格中，转到**模块 \> Retail and Commerce \> 总部设置 \> 参数 \> 组织电子邮件模板**。
1. 在操作窗格上，选择**新建**。
1. 在**电子邮件 ID** 字段中，输入 ID 以帮助识别此模板。
1. 在**发件人名称**字段中，输入发件人姓名。
1. 在**电子邮件描述**中，输入有意义的描述。
1. 在**发件人电子邮件**中，输入发件人电子邮件地址。
1. 在**常规**部分中，填写所需的所有可选信息（例如电子邮件优先级）。
1. 展开**电子邮件内容**部分并选择**新建**以创建模板内容。 对于每个内容项，选择语言并提供电子邮件主题行。 如果电子邮件有正文，请确保选中**有正文**框。
1. 在操作窗格上，选择**电子邮件**以提供电子邮件正文模板。

下图显示了一些示例电子邮件模板设置。

![电子邮件模板设置](media/email-template.png)

### <a name="create-an-email-event"></a>创建电子邮件事件

若要创建电子邮件事件，请执行以下步骤。

1. 在导航窗格中，转到**模块 \> Retail and Commerce \> 总部设置 \> Commerce 电子邮件通知配置文件**。
1. 在列表中，找到并选择所需记录。 
1. 从**电子邮件 ID** 下拉列表中选择电子邮件模板。
1. 从下拉列表中选择合适的**电子邮件通知类型**。
1. 选中**有效**复选框。
1. 在操作窗格上，选择**保存**。

下图显示了一些示例事件通知设置。

![事件通知设置](media/email-notification-profile.png)

## <a name="additional-resources"></a>其他资源

[配置和发送电子邮件](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[渠道概览](channels-overview.md)

[渠道设置先决条件](channels-prerequisites.md)

[组织和组织层次结构概览](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

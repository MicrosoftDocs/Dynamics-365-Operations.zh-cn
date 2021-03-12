---
title: 通过电子邮件发送的客户端预警通知
description: 此主题提供有关如何设置在预定义事件发生时发送电子邮件通知的规则的信息。
author: tjvass
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a1d520584e331631bb5a6a88ba6c9a8b50b3d29e
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798615"
---
# <a name="client-alert-notifications-by-email"></a>通过电子邮件发送的客户端预警通知

[!include [banner](../includes/banner.md)]

您可以定义在预定义事件发生时监控筛选出的数据视图和自动发送电子邮件通知的自定义预警规则。 发送电子邮件通知的选项可用于所有支持的预警类型，也可为现有的预警规则打开。

您可以使用内置控件创建监控筛选出的系统批处理作业视图的预警规则。 通过监视 **状态** 字段值，还可以配置在批处理作业失败时发送电子邮件的预警规则。 在创建这些预警规则后，您不必再检查报表了解对业务数据所作的更改。 您可以让智能更改检测服务为您执行监控。

客户端预警依靠通过与 Microsoft Office 的集成提供的电子邮件子系统。 我们建议您使用简单邮件传输协议 (SMTP) 提供程序，以使电子邮件分发不必依靠本地的邮件客户端。

若要通过电子邮件发送通知，客户必须配置集成的电子邮件服务。 电子邮件通知代表警报所有者发送到收件人。

有关如何配置电子邮件的详细信息，请参阅[配置和发送电子邮件](../organization-administration/configure-email.md)。

以下图像显示 **创建预警规则** 对话框，其现在包括 **发送电子邮件** 选项。

[![创建将“发送电子邮件”选项设置为“是”的预警规则对话框](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> 在 **发送电子邮件** 选项设置为 **是** 时，预警通知将继续从操作中心提供。

## <a name="alert-notification-email-templates"></a>预警通知电子邮件模板

此服务通过使用提供预警通知基本详细信息的预定义电子邮件模板发送电子邮件通知。

以下图像显示通过电子邮件收到预警通知时预警通知的结构。

[![用户记录创建、字段更改和模板删除的基于模板的预警通知](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)

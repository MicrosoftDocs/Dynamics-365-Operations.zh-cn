---
title: 使得用户能够接收工作流相关的电子邮件消息
description: 在工作流相关事件发生时，您可以配置系统将电子邮件消息发送给用户。
author: jasongre
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3207727c8deba97eebfd7516e9600238e5e79b3d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747241"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>使得用户能够接收工作流相关的电子邮件消息

[!include [banner](../../includes/banner.md)]

在工作流相关事件发生时，您可以配置系统将电子邮件消息发送给用户。 例如，当分配文档供审核时，可以将电子邮件消息发送给用户。 创建此程序的演示数据公司是 USMF。

1. 转到 **导航窗格 > 模块 > 系统管理 > 用户 > 用户**。
2. 在列表中，找到并选择所需记录。
3. 在 **操作窗格** 上，单击 **用户选项**。
4. 单击 **工作流** 选项卡。确保展开 **通知** 部分。 在 **通知** 部分中，可以指定您希望程序如何通知用户有关工作流相关事件。  
5. 在 **行项工作流通知类型** 字段中，选择一个选项。
    - 分组 – 行项的通知分组到单个电子邮件消息中。
    - 单独 – 针对每个行项发送电子邮件消息。  
    - 如果您希望用户在客户端中接收通知，则选中 **以电子邮件形式发送通知** 复选框。  
6. 单击 **保存**。
7. 关闭该页面。

> [!NOTE]
> 工作流电子邮件模板源自系统电子邮件模板或组织电子邮件模板，具体取决于工作流是系统级（不是公司特定）还是组织级（公司特定）工作流。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
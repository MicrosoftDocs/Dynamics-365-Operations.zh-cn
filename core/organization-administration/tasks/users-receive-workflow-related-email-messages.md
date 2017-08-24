--- 
title: "使得用户能够接收工作流相关的电子邮件消息"
description: "在工作流相关事件发生时，您可以配置系统将电子邮件消息发送给用户。"
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 76ae3b1f479733f7e3a738fd43e52134bda7069a
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>使得用户能够接收工作流相关的电子邮件消息

[!include[task guide banner](../../includes/task-guide-banner.md)]

在工作流相关事件发生时，您可以配置系统将电子邮件消息发送给用户。 例如，当分配文档供审核时，可以将电子邮件消息发送给用户。 创建此程序的演示数据公司是 USMF。

1. 转到“系统管理”>“用户”>“用户”。
2. 在列表中，找到并选择所需记录。
3. 单击“用户选项”。
4. 单击“工作流”选项卡。
    * 确保已展开“通知”部分。     在“通知”部分中，可以指定您希望程序如何通知用户有关工作流相关事件。  
5. 在“行项工作流通知类型”字段中，选择一个选项。
    * 分组 – 行项的通知分组到单个电子邮件消息中。    单独 – 针对每个行项发送电子邮件消息。  
    * 如果您希望用户在客户端中接收通知，则选中“以电子邮件形式发送通知”复选框。  
6. 单击“保存”。
7. 关闭该页面。



--- 
title: "配置系统以向用户发送与工作流有关的电子邮件"
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 04d90c9ded1ba7fb1ceac4ff1d54f54f6c43f9e9
ms.contentlocale: zh-cn
ms.lasthandoff: 08/08/2018

---
# <a name="configure-the-system-to-send-workflow-related-email-to-users"></a>配置系统以向用户发送与工作流有关的电子邮件

[!include [task guide banner](../../includes/task-guide-banner.md)]

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



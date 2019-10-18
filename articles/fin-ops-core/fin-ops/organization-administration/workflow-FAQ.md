---
title: 工作流常见问题
description: 本主题解答有关工作流系统的常见问题。
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14aa9b56da005e8e3ca121589d0e22c60f34343b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189767"
---
# <a name="workflow-faq"></a>工作流常见问题

[!include [banner](../includes/banner.md)]

本主题解答有关工作流系统的常见问题。

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>为什么在拒绝一个工作项后会收到多个通知？
如果拒绝了某个工作项，该工作项的状态将为已完成但被拒绝。 将再创建一个工作项，并将其分配给发起方。 这意味着将向被拒绝工作项的发起方发送一个通知，并向“更改请求的”工作项分配给的用户发送一个单独的通知。 

每个通知都针对一个不同的工作项，但是因为相似，所以可能造成混乱。 我们在想办法在将来的版本中改进这个问题。

## <a name="why-are-my-workflow-exports-failing"></a>我在导出工作流时为什么失败了？
这是现有工作流导出功能的一项限制，它会阻止超过 48 个字符的工作流名称。 使用超过 48 个字符的名称可能会导致“服务器未能对请求进行身份验证”错误，以及/或者阻止导出无文件类型的文件。 以下博客文章提供了有关[工作流导出疑难解答](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting)的更多详细信息。

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>工作流的提交者是否也可以审核工作流？
可以。如果按照这种方式配置，工作流的提交者也可以审核工作流。 若要避免此行为，请将**工作流参数 > 常规 > 审核人 > 不允许提交者进行审核**设置为**是**。

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>是否可向工作流添加预警以向用户提供通知？
下面是向工作流添加预警以提供通知时需要注意的一些关键方面：
- 预警与工作流通知机制
    - 可以为录制更改设置预警。 工作流将更改录制，这样就可以设置与工作流导致的录制更改有关的预警。 但是，因为工作流具有不同的内置通知选项，所以使用预警的效果不理想。
- 来自工作流的标准通知 
    - 工作流有内置电子邮件通知。 客户可以配置通知，以便向用户发送电子邮件。 这些通知不会为用户生成操作中心消息。
    - 将来的更新中，将添加操作中心消息，以便为用户分配工作流工作项。 
- 向工作流添加通知
    - 可以为特定用户创建操作中心消息，如使用 X++ 从工作流创建的消息。
    - [工作流具有业务事件](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow)，可供客户用于触发具有客户在寻找的通知的流。   

总之，如果在为用户分配工作流工作项时，该用户未收到来自操作中心的正确通知，请利用[工作流业务事件](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow)和 Microsoft Flow 提供更多通知或不同通知。
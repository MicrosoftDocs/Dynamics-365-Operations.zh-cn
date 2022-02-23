---
title: 工作流常见问题
description: 本主题解答有关工作流系统的常见问题。
author: ChrisGarty
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58aa4a6d313a78e88c2858637d6de167895ec534
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797383"
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
可以。如果按照这种方式配置，工作流的提交者也可以审核工作流。 若要避免此行为，请将 **系统管理 > 工作流 > 工作流参数 > 常规 > 审核人 > 不允许提交者进行审核** 设置为 **是**。

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

总之，如果在为用户分配工作流工作项时，该用户未收到来自操作中心的正确通知，请利用[工作流业务事件](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow)和 Microsoft Power Automate 提供更多通知或不同通知。

## <a name="why-is-workflow-editor-not-able-to-start-under-ad-fs"></a>为什么工作流编辑器在 AD FS 下无法启动？
在升级的环境中的 Active Directory 联合身份验证服务 (AD FS) 下运行时，工作流编辑器可能无法启动。 如果是这样，请确保 URL“https://dynamicsaxworkfloweditor/”已添加到 ADFS 设置中的属性 **Microsoft Dynamics 365 for Operations On-premises - 工作流 - 本机应用程序**。

## <a name="why-am-i-getting-sql-deadlocks-on-workflow-processing"></a>为什么在处理工作流时遇到了 SQL 死锁？ 
**工作流参数** 页中 **每个批处理任务的工作流项目数** 的默认字段值为 0。 值为 0 将导致默认值更改为每个批次 20 个项目。 调整此值时，请务必小心，因为每个批次的项目数太大 (> 40) 可能导致 SQL 死锁。

## <a name="what-is-the-workflow-enhanced-error-feature"></a>什么是“工作流增强错误”功能？
版本 10.0.13 中的“工作流增强错误”功能添加了错误代码来区分不同的工作流错误类。 报告的错误消息大致相似，只有微小差异，以使它们更清晰。

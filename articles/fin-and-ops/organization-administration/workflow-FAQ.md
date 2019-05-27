---
title: 工作流常见问题
description: 本主题解答有关 Microsoft Dynamics 365 for Finance and Operations 中的工作流系统的常见问题。
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509283"
---
# <a name="workflow-system"></a>工作流系统

[!include [banner](../includes/banner.md)]

本主题解答有关 Microsoft Dynamics 365 for Finance and Operations 中的工作流系统的常见问题。

## <a name="notifications"></a>通知

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>为什么在拒绝一个工作项后会收到多个通知？
如果拒绝了某个工作项，该工作项的状态将为已完成但被拒绝。 将再创建一个工作项，并将其分配给发起方。 这意味着将向被拒绝工作项的发起方发送一个通知，并向“更改请求的”工作项分配给的用户发送一个单独的通知。 

每个通知都针对一个不同的工作项，但是因为相似，所以可能造成混乱。 我们在想办法在将来的版本中改进这个问题。

### <a name="why-are-my-workflow-exports-failing"></a>我在导出工作流时为什么失败了？
这是现有工作流导出功能的一项限制，它会阻止超过 48 个字符的工作流名称。 使用超过 48 个字符的名称可能会导致“服务器未能对请求进行身份验证”错误，以及/或者阻止导出无文件类型的文件。 以下博客文章提供了有关[工作流导出疑难解答](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting)的更多详细信息。

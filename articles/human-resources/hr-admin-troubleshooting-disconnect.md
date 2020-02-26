---
title: 客户端断开连接
description: 本文说明如果客户与其环境断开并且不知道原因该如何做。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.article: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 73f0c31d5153a82651ed77aa37bc10966ce7c9b1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008194"
---
# <a name="client-disconnects"></a>客户端断开连接

**环境详细信息** 

此问题可能在所有环境中发生。
 
**故障** 

客户与其环境断开并且不知道原因。 客户收到以下错误消息之一：

- 我们已丢失您的连接。 请单击“关闭”以继续操作。
- 您的网络连接似乎已中断，请单击“重试”以再次尝试。

**红色标志**

当用户处于实现阶段，跨生产和测试环境比较信息，并忘记了在会话之间移动时，经常会发生此问题。 如果用户在此阶段，他们很可能会遇到此问题。

**发货** 

**浏览器类型：** Google Chrome、Internet Explorer 和 Microsoft Edge

当同一用户和相同浏览器类型的两个不同会话同时打开时，Microsoft Dynamics 365 Human Resources 将断开用户。 （例如，用户 A 在 Chrome 中同时查看环境 1 和环境 2。）用户是否打开不同的浏览器窗口或不同选项卡不受影响。 如果同一用户凭据被用于在相同浏览器类型中同时登录到环境 1 和环境 2，Human Resources 将断开其中一个会话。

**解决方案**

请确保一个指定浏览器类型一次只有一个环境打开。 用户可以打开同一个环境的多个会话（即，同一浏览器中的多个选项卡）。

要同时在两个环境之间跳转的用户应该在不同的浏览器类型中打开每个环境。 （例如，用户 A 可以在 Chrome 中查看环境 1，在 Microsoft Edge 中查看环境 2。）

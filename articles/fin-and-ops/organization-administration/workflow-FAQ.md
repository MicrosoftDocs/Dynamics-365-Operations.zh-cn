---
title: 工作流常见问题
description: 本主题解答有关 Microsoft Dynamics 365 for Finance and Operations 中的工作流系统的常见问题。
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
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
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/01/2019
ms.locfileid: "773197"
---
# <a name="workflow-system"></a>工作流系统

[!include [banner](../includes/banner.md)]

本主题解答有关 Microsoft Dynamics 365 for Finance and Operations 中的工作流系统的常见问题。

## <a name="notifications"></a>通知

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>为什么在拒绝一个工作项后会收到多个通知？
如果拒绝了某个工作项，该工作项的状态将为已完成但被拒绝。 将再创建一个工作项，并将其分配给发起方。 这意味着将向被拒绝工作项的发起方发送一个通知，并向“更改请求的”工作项分配给的用户发送一个单独的通知。 

每个通知都针对一个不同的工作项，但是因为相似，所以可能造成混乱。 我们在想办法在将来的版本中改进这个问题。

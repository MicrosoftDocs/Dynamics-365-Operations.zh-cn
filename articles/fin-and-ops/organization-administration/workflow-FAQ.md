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
# <a name="workflow-system"></a><span data-ttu-id="5f157-103">工作流系统</span><span class="sxs-lookup"><span data-stu-id="5f157-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f157-104">本主题解答有关 Microsoft Dynamics 365 for Finance and Operations 中的工作流系统的常见问题。</span><span class="sxs-lookup"><span data-stu-id="5f157-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="5f157-105">通知</span><span class="sxs-lookup"><span data-stu-id="5f157-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="5f157-106">为什么在拒绝一个工作项后会收到多个通知？</span><span class="sxs-lookup"><span data-stu-id="5f157-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="5f157-107">如果拒绝了某个工作项，该工作项的状态将为已完成但被拒绝。</span><span class="sxs-lookup"><span data-stu-id="5f157-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="5f157-108">将再创建一个工作项，并将其分配给发起方。</span><span class="sxs-lookup"><span data-stu-id="5f157-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="5f157-109">这意味着将向被拒绝工作项的发起方发送一个通知，并向“更改请求的”工作项分配给的用户发送一个单独的通知。</span><span class="sxs-lookup"><span data-stu-id="5f157-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="5f157-110">每个通知都针对一个不同的工作项，但是因为相似，所以可能造成混乱。</span><span class="sxs-lookup"><span data-stu-id="5f157-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="5f157-111">我们在想办法在将来的版本中改进这个问题。</span><span class="sxs-lookup"><span data-stu-id="5f157-111">We are looking at ways to improve this in a future release.</span></span>

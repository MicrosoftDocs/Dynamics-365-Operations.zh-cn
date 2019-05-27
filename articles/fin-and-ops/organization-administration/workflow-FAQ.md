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
# <a name="workflow-system"></a><span data-ttu-id="132d2-103">工作流系统</span><span class="sxs-lookup"><span data-stu-id="132d2-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="132d2-104">本主题解答有关 Microsoft Dynamics 365 for Finance and Operations 中的工作流系统的常见问题。</span><span class="sxs-lookup"><span data-stu-id="132d2-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="132d2-105">通知</span><span class="sxs-lookup"><span data-stu-id="132d2-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="132d2-106">为什么在拒绝一个工作项后会收到多个通知？</span><span class="sxs-lookup"><span data-stu-id="132d2-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="132d2-107">如果拒绝了某个工作项，该工作项的状态将为已完成但被拒绝。</span><span class="sxs-lookup"><span data-stu-id="132d2-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="132d2-108">将再创建一个工作项，并将其分配给发起方。</span><span class="sxs-lookup"><span data-stu-id="132d2-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="132d2-109">这意味着将向被拒绝工作项的发起方发送一个通知，并向“更改请求的”工作项分配给的用户发送一个单独的通知。</span><span class="sxs-lookup"><span data-stu-id="132d2-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="132d2-110">每个通知都针对一个不同的工作项，但是因为相似，所以可能造成混乱。</span><span class="sxs-lookup"><span data-stu-id="132d2-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="132d2-111">我们在想办法在将来的版本中改进这个问题。</span><span class="sxs-lookup"><span data-stu-id="132d2-111">We are looking at ways to improve this in a future release.</span></span>

### <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="132d2-112">我在导出工作流时为什么失败了？</span><span class="sxs-lookup"><span data-stu-id="132d2-112">Why are my workflow exports failing?</span></span>
<span data-ttu-id="132d2-113">这是现有工作流导出功能的一项限制，它会阻止超过 48 个字符的工作流名称。</span><span class="sxs-lookup"><span data-stu-id="132d2-113">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="132d2-114">使用超过 48 个字符的名称可能会导致“服务器未能对请求进行身份验证”错误，以及/或者阻止导出无文件类型的文件。</span><span class="sxs-lookup"><span data-stu-id="132d2-114">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="132d2-115">以下博客文章提供了有关[工作流导出疑难解答](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting)的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="132d2-115">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>

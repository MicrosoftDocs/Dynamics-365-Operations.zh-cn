---
title: 客户端断开连接
description: 本文说明如果客户与环境断开并且不知道原因时该如何做。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fcb7e5e3230aee9f6c04e4854c8eea836ae14c7f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053411"
---
# <a name="client-disconnects"></a><span data-ttu-id="39af2-103">客户端断开连接</span><span class="sxs-lookup"><span data-stu-id="39af2-103">Client disconnects</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="39af2-104">**环境详细信息**</span><span class="sxs-lookup"><span data-stu-id="39af2-104">**Environment details**</span></span> 

<span data-ttu-id="39af2-105">此问题可能在所有环境中发生。</span><span class="sxs-lookup"><span data-stu-id="39af2-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="39af2-106">**故障**</span><span class="sxs-lookup"><span data-stu-id="39af2-106">**Symptom**</span></span> 

<span data-ttu-id="39af2-107">客户与环境断开并且不知道原因。</span><span class="sxs-lookup"><span data-stu-id="39af2-107">The customer is disconnected from the environment and doesn't know why.</span></span> <span data-ttu-id="39af2-108">客户收到以下错误消息之一：</span><span class="sxs-lookup"><span data-stu-id="39af2-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="39af2-109">我们已丢失您的连接。</span><span class="sxs-lookup"><span data-stu-id="39af2-109">We've lost your connection.</span></span> <span data-ttu-id="39af2-110">请单击“关闭”以继续操作。</span><span class="sxs-lookup"><span data-stu-id="39af2-110">Click Close to continue working.</span></span>
- <span data-ttu-id="39af2-111">您的网络连接似乎已中断，请单击“重试”以再次尝试。</span><span class="sxs-lookup"><span data-stu-id="39af2-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="39af2-112">**红色标志**</span><span class="sxs-lookup"><span data-stu-id="39af2-112">**Red flag**</span></span>

<span data-ttu-id="39af2-113">当用户处于实现阶段，跨生产和测试环境比较信息，并忘记了在会话之间移动时，经常会发生此问题。</span><span class="sxs-lookup"><span data-stu-id="39af2-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="39af2-114">如果用户在此阶段，他们很可能会遇到此问题。</span><span class="sxs-lookup"><span data-stu-id="39af2-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="39af2-115">**发货**</span><span class="sxs-lookup"><span data-stu-id="39af2-115">**Issue**</span></span> 

<span data-ttu-id="39af2-116">**浏览器类型：** Google Chrome、Internet Explorer 和 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="39af2-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="39af2-117">当同一用户和相同浏览器类型的两个不同会话同时打开时，Microsoft Dynamics 365 Human Resources 将断开用户。</span><span class="sxs-lookup"><span data-stu-id="39af2-117">Microsoft Dynamics 365 Human Resources disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="39af2-118">（例如，用户 A 在 Chrome 中同时查看环境 1 和环境 2。）用户是否打开不同的浏览器窗口或不同选项卡不受影响。</span><span class="sxs-lookup"><span data-stu-id="39af2-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="39af2-119">如果同一用户凭据被用于在相同浏览器类型中同时登录到环境 1 和环境 2，Human Resources 将断开其中一个会话。</span><span class="sxs-lookup"><span data-stu-id="39af2-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Human Resources disconnects one of the sessions.</span></span>

<span data-ttu-id="39af2-120">**解决方案**</span><span class="sxs-lookup"><span data-stu-id="39af2-120">**Solution**</span></span>

<span data-ttu-id="39af2-121">请确保一个指定浏览器类型一次只有一个环境打开。</span><span class="sxs-lookup"><span data-stu-id="39af2-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="39af2-122">用户可以打开同一个环境的多个会话（即，同一浏览器中的多个选项卡）。</span><span class="sxs-lookup"><span data-stu-id="39af2-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="39af2-123">要同时在两个环境之间跳转的用户应该在不同的浏览器类型中打开每个环境。</span><span class="sxs-lookup"><span data-stu-id="39af2-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="39af2-124">（例如，用户 A 可以在 Chrome 中查看环境 1，在 Microsoft Edge 中查看环境 2。）</span><span class="sxs-lookup"><span data-stu-id="39af2-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
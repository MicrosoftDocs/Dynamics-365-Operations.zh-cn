---
title: 仓库补货疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理仓库补货时可能遇到的常见问题。
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e4d87e85520c2b6f2346fddf3b985d4e17fe35cb
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644865"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="ab741-103">仓库补货疑难解答</span><span class="sxs-lookup"><span data-stu-id="ab741-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab741-104">此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理仓库补货时可能遇到的常见问题。</span><span class="sxs-lookup"><span data-stu-id="ab741-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="ab741-105">我收到以下错误消息：“工作 %1 无法解锁，它有未完成的补货工作。”</span><span class="sxs-lookup"><span data-stu-id="ab741-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ab741-106">问题描述</span><span class="sxs-lookup"><span data-stu-id="ab741-106">Issue description</span></span>

<span data-ttu-id="ab741-107">领料工作由于有依赖的补货工作被锁定。</span><span class="sxs-lookup"><span data-stu-id="ab741-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ab741-108">解决问题</span><span class="sxs-lookup"><span data-stu-id="ab741-108">Issue resolution</span></span>

<span data-ttu-id="ab741-109">当您使用波次需求补货时，如果必须为某个领料位置补货以满足源订单需求，系统将同时创建补货工作和领料工作。</span><span class="sxs-lookup"><span data-stu-id="ab741-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="ab741-110">但是，会锁定领料工作，直到补货工作完成。</span><span class="sxs-lookup"><span data-stu-id="ab741-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="ab741-111">此行为是有意的，因为除非补货工作完成，否则领料位置会没有足够的库存。</span><span class="sxs-lookup"><span data-stu-id="ab741-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="ab741-112">请完成补货工作，然后再处理领料工作。</span><span class="sxs-lookup"><span data-stu-id="ab741-112">Complete the replenishment work, and then process the picking work.</span></span>

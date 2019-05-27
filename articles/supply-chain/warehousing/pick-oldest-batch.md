---
title: 在移动设备上领取最早的批次
description: 此主题描述如何从移动设备设置和应用领取最早批次的选项。
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a592425ed28f591783ec45bdfd61574bb889557
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558276"
---
# <a name="pick-oldest-batch-on-a-mobile-device"></a><span data-ttu-id="9abf7-103">在移动设备上领取最早的批次</span><span class="sxs-lookup"><span data-stu-id="9abf7-103">Pick oldest batch on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9abf7-104">您可以通过移动设备菜单访问配置**领取最早的批次**，它将允许您强制或警告仓库工作人员领取其当前库位中的最早批次。</span><span class="sxs-lookup"><span data-stu-id="9abf7-104">You can access the configuration **Pick oldest batch** via a mobile device menu and it allows you to force or warn warehouse workers to pick the oldest batch in their current location.</span></span>  

## <a name="where-it-applies"></a><span data-ttu-id="9abf7-105">适用情况</span><span class="sxs-lookup"><span data-stu-id="9abf7-105">Where it applies</span></span>
<span data-ttu-id="9abf7-106">领取最早的批次在移动设备菜单项上配置并影响领取物料下的批次。</span><span class="sxs-lookup"><span data-stu-id="9abf7-106">Pick oldest batch is configured on mobile device menu items and effects the pick for batch below items.</span></span>

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a><span data-ttu-id="9abf7-107">如何设置领取最早的批次配置</span><span class="sxs-lookup"><span data-stu-id="9abf7-107">How to set up the configuration for Pick oldest batch</span></span> 
<span data-ttu-id="9abf7-108">对于设置为使用现有工作的物料，可以从移动设备菜单将**领取最早的批次**设置为**无**、**警告**或**强制**。</span><span class="sxs-lookup"><span data-stu-id="9abf7-108">For items that are set to use existing work, **Pick oldest batch** can be set to **None**, **Warn**, or **Force** from a mobile device menu.</span></span>

<span data-ttu-id="9abf7-109">**无**：工作人员不会收到任何消息，且允许他们领取其库位中的任何批次。</span><span class="sxs-lookup"><span data-stu-id="9abf7-109">**None**: Workers will not receive any messages and they will be allowed to pick any batch in their location.</span></span>

<span data-ttu-id="9abf7-110">**警告**和**强制**：当工作人员选择批次时，具有最早到期日期的批次的列表将显示在批次控制上方。</span><span class="sxs-lookup"><span data-stu-id="9abf7-110">**Warn** and **Force**:  A list of the batch(es) with the oldest expiration date will be displayed above the batch control when the worker selects a batch.</span></span> <span data-ttu-id="9abf7-111">如果库位受牌照控制，具有最早批次的牌照的列表将显示在牌照控制上方。</span><span class="sxs-lookup"><span data-stu-id="9abf7-111">If the location is license plate controlled, a list of license plates that have the oldest batch will be displayed above the license plate control.</span></span> 
-   <span data-ttu-id="9abf7-112">**警告**：如果工作人员选择显示的列表中没有的牌照或批次，控制将为空白，且将显示具有更早的批次可供选择的警告。</span><span class="sxs-lookup"><span data-stu-id="9abf7-112">**Warn**: If a worker chooses a license plate or batch that is not on the shown list, the control will be blanked and a warning will be shown that there is an older batch to select.</span></span> <span data-ttu-id="9abf7-113">要允许继续执行工作，工作人员可以再次选择同一个牌照或批次。</span><span class="sxs-lookup"><span data-stu-id="9abf7-113">To be allowed to continue the work, the worker can select the same license plate or batch again.</span></span>  
-   <span data-ttu-id="9abf7-114">**强制**：工作人员将继续收到具有更早的批次可供领取的消息。</span><span class="sxs-lookup"><span data-stu-id="9abf7-114">**Force**: Workers will continue to receive the message that there is an older batch to pick.</span></span>

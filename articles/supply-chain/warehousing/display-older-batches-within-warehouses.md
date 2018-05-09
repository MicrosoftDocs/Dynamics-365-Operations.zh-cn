---
title: "在移动设备上配置“显示仓库内的更早批次”"
description: "本主题介绍如何设置移动设备以显示早于当前工作行位置的批次的位置列表。"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 27fbf57ba7114ca773f2a80de51b36b4e63c6dd6
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a><span data-ttu-id="f97c8-103">在移动设备上配置“显示仓库内的更早批次”</span><span class="sxs-lookup"><span data-stu-id="f97c8-103">Configure Display older batches within warehouse on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f97c8-104">**显示仓库内的更早批次**配置让你能够显示早于当前工作行位置的批次的位置列表。</span><span class="sxs-lookup"><span data-stu-id="f97c8-104">The **Display older batches within warehouse** configuration lets you display a list of locations with batches older than the current location of the work line.</span></span> <span data-ttu-id="f97c8-105">显示的位置的列表包括与位置中的更早批次以及各批次的到期日期和物理库存有关的信息。</span><span class="sxs-lookup"><span data-stu-id="f97c8-105">The list of locations that are displayed includes information about the older batches in the location with the expiration date and the physical inventory of each batch.</span></span> <span data-ttu-id="f97c8-106">你可以选择从新位置领料或继续从当前位置领料。</span><span class="sxs-lookup"><span data-stu-id="f97c8-106">You can choose to pick from a new location or to continue picking from the current location.</span></span> 
- <span data-ttu-id="f97c8-107">从新位置领料 - 如果你选择一个要从中领料的新位置，当前工作行将更新为使用新位置且新位置的工作将照常进行。</span><span class="sxs-lookup"><span data-stu-id="f97c8-107">Pick from a new location - If you select a new location to pick from, the  current work line will be updated to use the new location and work will continue as usual with the new location.</span></span> <span data-ttu-id="f97c8-108">为了使新位置生效，它必须具有用于整个工作行的足够的可用数量。</span><span class="sxs-lookup"><span data-stu-id="f97c8-108">For the new location to be valid, it must have enough available quantity for the whole work line.</span></span> <span data-ttu-id="f97c8-109">如果无法提供需要的数量，则不会更新工作行，且将显示列表。</span><span class="sxs-lookup"><span data-stu-id="f97c8-109">If the required quantity is not available, the work line will not be updated, and the list will display.</span></span> 
- <span data-ttu-id="f97c8-110">继续从当前位置领料 - 如果继续使用当前的工作行位置，则工作行的数量将继续从原始位置领料。</span><span class="sxs-lookup"><span data-stu-id="f97c8-110">Continue picking from the current location - If you continue with the current work line location, the quantities for the work line will continue to be picked from the original location.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="f97c8-111">适用情况</span><span class="sxs-lookup"><span data-stu-id="f97c8-111">Where it applies</span></span>
<span data-ttu-id="f97c8-112">“显示仓库内的更早批次”在移动设备菜单项上配置并影响领取物料下的批次。</span><span class="sxs-lookup"><span data-stu-id="f97c8-112">Display older batches within warehouse is configured on mobile device menu items and affects the pick for batch below items.</span></span>

## <a name="set-up-display-older-batches-within-warehouse"></a><span data-ttu-id="f97c8-113">设置“显示仓库内的更早批次”</span><span class="sxs-lookup"><span data-stu-id="f97c8-113">Set up Display older batches within warehouse</span></span>
<span data-ttu-id="f97c8-114">当**领取最早的批次**选项设置为**警告**时，**显示仓库内的更早批次**配置在移动设备菜单项上可用。</span><span class="sxs-lookup"><span data-stu-id="f97c8-114">The **Display older batches within warehouse** configuration is available on mobile device menu items when the **Pick oldest batch** option is set to **Warn**.</span></span>

- <span data-ttu-id="f97c8-115">在**仓库管理** > **设置** > **移动设备** > **移动设备菜单项**下，对菜单项将**使用现有工作**设置为**是**，然后在**领取最早的批次**字段中选择**警告**。</span><span class="sxs-lookup"><span data-stu-id="f97c8-115">Under **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**, set **Use existing work** to **Yes** for the menu item, and select **Warn** in the **Pick oldest batch** field.</span></span> 



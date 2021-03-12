---
title: 对未结工作列表的系统分组
description: 此主题描述如何在移动设备上筛选未结工作列表。
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 826920980bdd2d30337c92553bd0367b119f676c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977330"
---
# <a name="system-grouping-on-an-open-work-list"></a><span data-ttu-id="ababb-103">对未结工作列表的系统分组</span><span class="sxs-lookup"><span data-stu-id="ababb-103">System grouping on an open work list</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ababb-104">通过使用系统分组字段可以筛选未结工作列表，而不必编辑移动设备菜单项。</span><span class="sxs-lookup"><span data-stu-id="ababb-104">By using a system grouping field, you can filter an open work list without having to edit the mobile device menu item.</span></span>
<span data-ttu-id="ababb-105">适用时，系统分组可用于在单个工作标题字段上筛选工作列表。</span><span class="sxs-lookup"><span data-stu-id="ababb-105">Where it applies, system grouping works for filtering a work list on a single work header field.</span></span> <span data-ttu-id="ababb-106">无法使用系统分组筛选行级别字段。</span><span class="sxs-lookup"><span data-stu-id="ababb-106">You cannot use system grouping to filter on line level fields.</span></span>

## <a name="set-up-system-grouping-on-an-open-work-list"></a><span data-ttu-id="ababb-107">对未结工作列表设置系统分组</span><span class="sxs-lookup"><span data-stu-id="ababb-107">Set up system grouping on an open work list</span></span>
<span data-ttu-id="ababb-108">使用这些步骤对未结工作列表设置系统分组。</span><span class="sxs-lookup"><span data-stu-id="ababb-108">Use these steps to set up system grouping on an open work list.</span></span>

-   <span data-ttu-id="ababb-109">从移动设备菜单项选择 **模式：间接** 和 **活动代码：显示未结工作列表**。</span><span class="sxs-lookup"><span data-stu-id="ababb-109">From a mobile device menu item, select **Mode: Indirect** and **Activity Code: Display open work list**.</span></span> <span data-ttu-id="ababb-110">以下选项可用。</span><span class="sxs-lookup"><span data-stu-id="ababb-110">The following options become available.</span></span> <span data-ttu-id="ababb-111">对未结工作列表设置系统分组需要这些选项。</span><span class="sxs-lookup"><span data-stu-id="ababb-111">These options are required for system grouping on an open work list.</span></span> 

|        <span data-ttu-id="ababb-112">选项</span><span class="sxs-lookup"><span data-stu-id="ababb-112">Option</span></span>         |                                                                                                                                                                                                                                                                         <span data-ttu-id="ababb-113">说明</span><span class="sxs-lookup"><span data-stu-id="ababb-113">Description</span></span>                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ababb-114">允许系统分组</span><span class="sxs-lookup"><span data-stu-id="ababb-114">Allow system grouping</span></span> |                                                                                                                                                                                                                                                 <span data-ttu-id="ababb-115">启用对所选工作列表进行系统分组菜单项。</span><span class="sxs-lookup"><span data-stu-id="ababb-115">Enables system groping for a selected work list menu item.</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ababb-116">系统分组字段</span><span class="sxs-lookup"><span data-stu-id="ababb-116">System grouping field</span></span> | <span data-ttu-id="ababb-117">仅当<strong>允许系统工作</strong>设置为<strong>是</strong>时可用。</span><span class="sxs-lookup"><span data-stu-id="ababb-117">Available only if <strong>Allow system work</strong> is set to <strong>Yes</strong>.</span></span> <span data-ttu-id="ababb-118">选择决定如何为工作人员对领料工作进行分组的字段。</span><span class="sxs-lookup"><span data-stu-id="ababb-118">Select the field that determines how picking work will be grouped for workers.</span></span> <span data-ttu-id="ababb-119">例如，如果您选择<strong>ShipmentId</strong>字段，工作人员将扫描装运 ID 来对领料工作进行分组。</span><span class="sxs-lookup"><span data-stu-id="ababb-119">For example, if you select the <strong>ShipmentId</strong> field, the worker will scan the shipment ID to group the picking work.</span></span> <span data-ttu-id="ababb-120">然后将装运的所有工作分配给工作人员。</span><span class="sxs-lookup"><span data-stu-id="ababb-120">All work for the shipment is then assigned to the worker.</span></span> <span data-ttu-id="ababb-121">此字段要求您创建一个菜单项从而使用系统分组现有工作。</span><span class="sxs-lookup"><span data-stu-id="ababb-121">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="ababb-122">使用<strong>系统分组标签</strong>字段通知工作人员要扫描的内容。</span><span class="sxs-lookup"><span data-stu-id="ababb-122">Use the <strong>System grouping label</strong> field to inform the worker what to scan.</span></span> |
| <span data-ttu-id="ababb-123">系统分组标签</span><span class="sxs-lookup"><span data-stu-id="ababb-123">System grouping label</span></span> |                       <span data-ttu-id="ababb-124">仅当<strong>允许系统工作</strong>设置为<strong>是</strong>时可用。</span><span class="sxs-lookup"><span data-stu-id="ababb-124">Available only if <strong>Allow system work</strong> is set to <strong>Yes</strong>.</span></span> <span data-ttu-id="ababb-125">输入信息通知工作人员对领料工作分组时要扫描的内容。</span><span class="sxs-lookup"><span data-stu-id="ababb-125">Enter information for the worker about what to scan when picking work is grouped.</span></span> <span data-ttu-id="ababb-126">例如，如果您使用 <strong>ShipmentId</strong> 字段按照装运分组领料工作，您可以在字段中输入装运 ID。</span><span class="sxs-lookup"><span data-stu-id="ababb-126">For example, if you use the <strong>ShipmentId</strong> field to group picking work by shipment, you might enter Shipment ID in the field.</span></span> <span data-ttu-id="ababb-127">此字段要求您创建一个菜单项从而使用系统分组现有工作。</span><span class="sxs-lookup"><span data-stu-id="ababb-127">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="ababb-128">您还必须在<strong>系统分组</strong>字段中选择要按其分组的字段。</span><span class="sxs-lookup"><span data-stu-id="ababb-128">You must also select the field to group by in the <strong>System grouping</strong> field.</span></span>                       |


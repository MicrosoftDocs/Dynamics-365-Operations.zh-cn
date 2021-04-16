---
title: 设置移动设备菜单项以提供领料行概览
description: 本主题说明如何定义何时向在移动设备上处理仓库工作的仓库工作人员显示所有工作行的列表。 对于经常需要在工作订单中查看领料行概览以便可以优化领料顺序的仓库工作人员，此功能会很有用。
author: MarkusFogelberg
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6eaba6da313f398c8d30f9a26c959ee971812e21
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818864"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a><span data-ttu-id="f4c4b-104">设置移动设备菜单项以提供领料行概览</span><span class="sxs-lookup"><span data-stu-id="f4c4b-104">Set up a mobile device menu item to provide a pick line overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4c4b-105">本主题说明如何为用于处理领料工作的移动设备菜单项配置与领料行概览相关的选项。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-105">This topic explains how to configure options that are related to the pick line overview for mobile device menu items that are used to process picking work.</span></span> <span data-ttu-id="f4c4b-106">领料行概览让仓库工作人员可以查看与其当前任务相关的所有工作行的列表并从中进行选择。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-106">The pick line overview lets warehouse workers view and select from a list of all the work lines that are related to their current task.</span></span> <span data-ttu-id="f4c4b-107">此功能可以帮助工作人员优化领料顺序。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-107">This capability can help workers optimize their picking sequence.</span></span> <span data-ttu-id="f4c4b-108">此功能提供的选项可代替标准 **跳过** 按钮，该按钮让工作人员可以固定的顺序每次循环浏览一行。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-108">The feature provides options that replace the standard **Skip** button that lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="f4c4b-109">（不过，使用该按钮的选项仍然可用。）</span><span class="sxs-lookup"><span data-stu-id="f4c4b-109">(However, the option to use that button is still available.)</span></span>

<span data-ttu-id="f4c4b-110">管理员可以单独配置每个菜单项，以控制仓库管理移动应用显示领料行概览的方式、时间和位置。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-110">Admins can configure each menu item individually to control how, when, and where the Warehouse Management mobile app presents the pick line overview.</span></span>

## <a name="turn-on-the-work-pick-line-overview-feature"></a><span data-ttu-id="f4c4b-111">打开工作领料行概览功能</span><span class="sxs-lookup"><span data-stu-id="f4c4b-111">Turn on the Work pick line overview feature</span></span>

<span data-ttu-id="f4c4b-112">此功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-112">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="f4c4b-113">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="f4c4b-114">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="f4c4b-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f4c4b-115">**模块：**_仓库管理_</span><span class="sxs-lookup"><span data-stu-id="f4c4b-115">**Module:** _Warehouse management_</span></span>
- <span data-ttu-id="f4c4b-116">**功能名称**：_工作领料行概览_</span><span class="sxs-lookup"><span data-stu-id="f4c4b-116">**Feature name:** _Work pick line overview_</span></span>

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a><span data-ttu-id="f4c4b-117">配置菜单项以显示所有工作行的列表</span><span class="sxs-lookup"><span data-stu-id="f4c4b-117">Configure menu items to show a list of all work lines</span></span>

<span data-ttu-id="f4c4b-118">要设置移动设备菜单项以提供领料行概览，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-118">To set up a mobile device menu item to provide a pick line overview, follow these steps.</span></span>

1. <span data-ttu-id="f4c4b-119">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-119">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="f4c4b-120">选择或创建与领料工作相关的菜单项，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f4c4b-120">Select or create a menu item that is related to picking work, and set the following values:</span></span>

    - <span data-ttu-id="f4c4b-121">\**模式：\*\*\*工作*</span><span class="sxs-lookup"><span data-stu-id="f4c4b-121">**Mode:** *Work*</span></span>
    - <span data-ttu-id="f4c4b-122">**使用现有工作**：*是*</span><span class="sxs-lookup"><span data-stu-id="f4c4b-122">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="f4c4b-123">**导向方式**：*用户导向* 或 *系统导向*</span><span class="sxs-lookup"><span data-stu-id="f4c4b-123">**Directed by:** *User directed* or *System directed*</span></span>

    <span data-ttu-id="f4c4b-124">有关如何创建菜单项以及如何使用 **移动设备菜单项** 页上提供的各种设置的详细信息，请参阅[为仓库工作设置移动设备](configure-mobile-devices-warehouse.md)。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-124">For more information about how to create menu items and use the various settings that are available on the **Mobile device menu items** page, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

1. <span data-ttu-id="f4c4b-125">在 **常规** 快速选项卡上，通过将 **显示工作行列表** 字段设置为以下值之一来配置功能：</span><span class="sxs-lookup"><span data-stu-id="f4c4b-125">On the **General** FastTab, configure the feature by setting the **Show work line list** field to one of the following values:</span></span>

    - <span data-ttu-id="f4c4b-126">**仅根据要求显示** – 工作人员可以选择通过选择仓库管理移动应用中的 **跳至** 按钮来查看领料行列表。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-126">**Show only upon request** – Workers can choose to view the pick line list by selecting the **Skip to** button in the Warehouse Management mobile app.</span></span>
    - <span data-ttu-id="f4c4b-127">**在每次领料开始时显示** – 工作人员在每次开始或完成领料行时会看到列表。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-127">**Show at the start of every pick** – Workers see the list every time that they start or finish a pick line.</span></span> <span data-ttu-id="f4c4b-128">他们还可以通过选择仓库管理移动应用中的 **跳至** 按钮来再次查看列表。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-128">They can also view the list again by selecting the **Skip to** button in the Warehouse Management mobile app.</span></span>
    - <span data-ttu-id="f4c4b-129">**仅在第一次领料开始时显示** – 工作人员每次开始新的领料工作时都会看到列表，但在每行之后不会看到。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-129">**Show at the start of the first pick only** – Workers see the list every time that they start new picking work, but not after each line.</span></span> <span data-ttu-id="f4c4b-130">他们还可以通过选择仓库管理移动应用中的 **跳至** 按钮来再次查看列表。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-130">They can also view the list again by selecting the **Skip to** button in the Warehouse Management mobile app.</span></span>
    - <span data-ttu-id="f4c4b-131">**从不显示** – 标准 **跳至** 按钮显示在仓库管理移动应用中，工作行列表的显示将关闭。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-131">**Never show** – The standard **Skip** button appears in the Warehouse Management mobile app, and display of the work line list is turned off.</span></span> <span data-ttu-id="f4c4b-132">**跳至** 按钮让工作人员可以按固定的顺序每次循环浏览一行。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-132">The **Skip** button lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="f4c4b-133">他们还可以根据需要多次循环浏览列表，直到处理完所有行。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-133">They can also cycle through the list as many times as they require, until all lines have been processed.</span></span>

1. <span data-ttu-id="f4c4b-134">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-134">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="f4c4b-135">如果将 **显示工作行列表** 字段设置为除 *从不显示* 以外的任何值，操作窗格上的 **字段列表** 按钮将变为可用。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-135">If you set the **Show work line list** field to any value except *Never show*, the **Field list** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="f4c4b-136">在操作窗格上，选择 **字段列表**。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-136">On the Action Pane, select **Field list**.</span></span>
1. <span data-ttu-id="f4c4b-137">在 **字段列表** 页面上，配置仓库管理移动应用为列表中的每一行显示的信息。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-137">On the **Field list** page, configure the information that the Warehouse Management mobile app shows for each line in the list.</span></span>

    - <span data-ttu-id="f4c4b-138">**主要控件** 字段始终设置为 *LineNum*。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-138">The **Primary control** field is always set to *LineNum*.</span></span> <span data-ttu-id="f4c4b-139">因此，列表中的每一行都以行号开头。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-139">Therefore, each row in the list begins with a line number.</span></span>
    - <span data-ttu-id="f4c4b-140">使用其余的 **显示字段** 字段来根据需要添加其他显示字段，最多可添加七个。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-140">Use the remaining **Display field** fields to add up to seven additional display fields, as you require.</span></span> <span data-ttu-id="f4c4b-141">每个 **显示字段** 字段中，选择工作行字段的名称。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-141">In each **Display field** field, select the name of a work line field.</span></span> <span data-ttu-id="f4c4b-142">然后每行将为该字段显示一个值。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-142">Each line will then show a value for that field.</span></span> <span data-ttu-id="f4c4b-143">这些值将按照您在此处选择的顺序显示。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-143">The values will be shown in the order that you select here.</span></span> <span data-ttu-id="f4c4b-144">如果七个值您不是全部需要，可以将某些 **显示字段** 字段保留为空白。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-144">You can leave some of the **Display field** fields blank if you don't require all seven values.</span></span>

1. <span data-ttu-id="f4c4b-145">在操作窗格上选择 **保存**，然后关闭 **字段列表** 页。</span><span class="sxs-lookup"><span data-stu-id="f4c4b-145">On the Action Pane, select **Save**, and then close the **Field list** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
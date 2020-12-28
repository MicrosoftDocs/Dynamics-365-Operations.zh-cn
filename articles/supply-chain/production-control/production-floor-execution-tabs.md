---
title: 设计生产车间执行界面
description: 此主题介绍如何为每个配置设计用户界面内容。
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 81c5c83128bb81523dee6ede549eece7b0d80e30
ms.sourcegitcommit: d9d1ddce6a334ade8b32b5ea3ac4c1e1a8f72715
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664264"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="0814b-103">设计生产车间执行界面</span><span class="sxs-lookup"><span data-stu-id="0814b-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="0814b-104">您可以为生产车间执行界面使用的每个配置设计用户界面内容。</span><span class="sxs-lookup"><span data-stu-id="0814b-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="0814b-105">例如，一个工作单元中的工作人员可能需要能够在生产车间打开作业说明，而在另一个工作单元，则不需要说明。</span><span class="sxs-lookup"><span data-stu-id="0814b-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="0814b-106">在这种情况下，应创建两个配置，一个带有打开文档附件的按钮，另一个没有此按钮。</span><span class="sxs-lookup"><span data-stu-id="0814b-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="0814b-107">设计选项卡</span><span class="sxs-lookup"><span data-stu-id="0814b-107">Design a tab</span></span>

<span data-ttu-id="0814b-108">在 **配置生产车间执行** 页上，您可以通过选择操作窗格上的 **设计选项卡** 来创建和配置选项卡。</span><span class="sxs-lookup"><span data-stu-id="0814b-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="0814b-109">每个选项卡分为四个部分，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="0814b-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="0814b-110">![选项卡布局](media/pfe-tab-layout.png "选项卡布局")</span><span class="sxs-lookup"><span data-stu-id="0814b-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="0814b-111">图中显示了以下元素：</span><span class="sxs-lookup"><span data-stu-id="0814b-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="0814b-112">主工具栏</span><span class="sxs-lookup"><span data-stu-id="0814b-112">Primary toolbar</span></span>
1. <span data-ttu-id="0814b-113">辅助工具栏</span><span class="sxs-lookup"><span data-stu-id="0814b-113">Secondary toolbar</span></span>
1. <span data-ttu-id="0814b-114">主视图</span><span class="sxs-lookup"><span data-stu-id="0814b-114">Main view</span></span>
1. <span data-ttu-id="0814b-115">详细视图</span><span class="sxs-lookup"><span data-stu-id="0814b-115">Detailed view</span></span>

<span data-ttu-id="0814b-116">要创建和配置新选项卡，请按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="0814b-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="0814b-117">转到 **生产控制 &gt; 设置 &gt; 制造执行**。</span><span class="sxs-lookup"><span data-stu-id="0814b-117">Go to **Production control &gt; Setup &gt; Manufacturing execution**.</span></span>

1. <span data-ttu-id="0814b-118">在操作窗格上选择 **设计选项卡** 打开 **设计选项卡** 页。</span><span class="sxs-lookup"><span data-stu-id="0814b-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="0814b-119">![设计选项卡页](media/pfe-design-tabs.png "设计选项卡页")</span><span class="sxs-lookup"><span data-stu-id="0814b-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="0814b-120">在操作窗格上选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="0814b-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="0814b-121">在页面标题中进行以下设置：</span><span class="sxs-lookup"><span data-stu-id="0814b-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="0814b-122">**选项卡名称** - 为选项卡指定名称。</span><span class="sxs-lookup"><span data-stu-id="0814b-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="0814b-123">**主视图** - 在两个预定义的作业列表（*活动作业* 或 *所有作业*）之间进行选择。</span><span class="sxs-lookup"><span data-stu-id="0814b-123">**Main view** - Select between the two pre-defined job lists (*Active jobs* or *All jobs*).</span></span>
    - <span data-ttu-id="0814b-124">**详细信息视图** - 在空白值或 **作业详细信息** 之间选择。</span><span class="sxs-lookup"><span data-stu-id="0814b-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="0814b-125">如果选择空白值，选项卡中将没有详细视图。如果选择 **作业详细信息**，详细视图将包含在主视图中的作业列表中选择的作业的详细描述。</span><span class="sxs-lookup"><span data-stu-id="0814b-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="0814b-126">在 **主工具栏** 部分，选择哪些按钮应该在主工具栏中可用。</span><span class="sxs-lookup"><span data-stu-id="0814b-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="0814b-127">**可用操作** 列显示可以添加的所有按钮的列表。</span><span class="sxs-lookup"><span data-stu-id="0814b-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="0814b-128">**所选操作** 列显示当前配置中包含的所有按钮的列表。</span><span class="sxs-lookup"><span data-stu-id="0814b-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="0814b-129">根据需要在列之间使用按钮在列之间移动所选项。</span><span class="sxs-lookup"><span data-stu-id="0814b-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="0814b-130">使用 **所选操作** 列旁边的向上和向下按钮控制按钮在用户界面的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="0814b-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="0814b-131">在 **辅助工具栏** 部分，选择哪些按钮应该在辅助工具栏中可用。</span><span class="sxs-lookup"><span data-stu-id="0814b-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="0814b-132">**可用操作** 列显示可以添加的所有按钮的列表。</span><span class="sxs-lookup"><span data-stu-id="0814b-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="0814b-133">**所选操作** 列显示当前配置中包含的所有按钮的列表。</span><span class="sxs-lookup"><span data-stu-id="0814b-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="0814b-134">根据需要在列之间使用按钮在列之间移动所选项。</span><span class="sxs-lookup"><span data-stu-id="0814b-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="0814b-135">使用 **所选操作** 列旁边的向上和向下按钮控制按钮在用户界面的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="0814b-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="0814b-136">将选项卡与配置关联</span><span class="sxs-lookup"><span data-stu-id="0814b-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="0814b-137">设计完所需的所有选项卡后，可以将它们与配置关联。</span><span class="sxs-lookup"><span data-stu-id="0814b-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="0814b-138">转到 **生产控制 &gt; 设置 &gt; 配置生产车间执行**。</span><span class="sxs-lookup"><span data-stu-id="0814b-138">Go to **Production control &gt; Setup &gt; Configure production floor execution**.</span></span>

    <span data-ttu-id="0814b-139">![配置生产车间执行](media/pfe-config-prod-floor-execution.png "配置生产车间执行")</span><span class="sxs-lookup"><span data-stu-id="0814b-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="0814b-140">在 **选项卡选择** 快速选项卡上，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="0814b-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="0814b-141">一个新行将添加到网格中。</span><span class="sxs-lookup"><span data-stu-id="0814b-141">A new row is added to the grid.</span></span> <span data-ttu-id="0814b-142">对于这个新行，选择要添加到配置中的选项卡的名称。</span><span class="sxs-lookup"><span data-stu-id="0814b-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="0814b-143">根据需要继续添加其他选项卡。</span><span class="sxs-lookup"><span data-stu-id="0814b-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="0814b-144">根据需要使用工具栏上的 **上移** 和 **下移** 按钮排列选项卡。</span><span class="sxs-lookup"><span data-stu-id="0814b-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="0814b-145">选项卡将按照以上屏幕截图中显示的顺序从左到右显示（顶部的选项卡显示在左侧）。</span><span class="sxs-lookup"><span data-stu-id="0814b-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>

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
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 786ea9a3da98e9f1812b007d4301cb47680e6894
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2021
ms.locfileid: "5077570"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="6baa1-103">设计生产车间执行界面</span><span class="sxs-lookup"><span data-stu-id="6baa1-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6baa1-104">您可以为生产车间执行界面使用的每个配置设计用户界面内容。</span><span class="sxs-lookup"><span data-stu-id="6baa1-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="6baa1-105">例如，一个工作单元中的工作人员可能需要能够在生产车间打开作业说明，而在另一个工作单元，则不需要说明。</span><span class="sxs-lookup"><span data-stu-id="6baa1-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="6baa1-106">在这种情况下，应创建两个配置，一个带有打开文档附件的按钮，另一个没有此按钮。</span><span class="sxs-lookup"><span data-stu-id="6baa1-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="6baa1-107">设计选项卡</span><span class="sxs-lookup"><span data-stu-id="6baa1-107">Design a tab</span></span>

<span data-ttu-id="6baa1-108">在 **配置生产车间执行** 页上，您可以通过选择操作窗格上的 **设计选项卡** 来创建和配置选项卡。</span><span class="sxs-lookup"><span data-stu-id="6baa1-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="6baa1-109">每个选项卡分为四个部分，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="6baa1-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="6baa1-110">![选项卡布局](media/pfe-tab-layout.png "选项卡布局")</span><span class="sxs-lookup"><span data-stu-id="6baa1-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="6baa1-111">图中显示了以下元素：</span><span class="sxs-lookup"><span data-stu-id="6baa1-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="6baa1-112">主工具栏</span><span class="sxs-lookup"><span data-stu-id="6baa1-112">Primary toolbar</span></span>
1. <span data-ttu-id="6baa1-113">辅助工具栏</span><span class="sxs-lookup"><span data-stu-id="6baa1-113">Secondary toolbar</span></span>
1. <span data-ttu-id="6baa1-114">主视图</span><span class="sxs-lookup"><span data-stu-id="6baa1-114">Main view</span></span>
1. <span data-ttu-id="6baa1-115">详细视图</span><span class="sxs-lookup"><span data-stu-id="6baa1-115">Detailed view</span></span>

<span data-ttu-id="6baa1-116">要创建和配置新选项卡，请按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="6baa1-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="6baa1-117">转到 **生产控制 &gt; 设置 &gt; 制造执行**。</span><span class="sxs-lookup"><span data-stu-id="6baa1-117">Go to **Production control &gt; Setup &gt; Manufacturing execution**.</span></span>

1. <span data-ttu-id="6baa1-118">在操作窗格上选择 **设计选项卡** 打开 **设计选项卡** 页。</span><span class="sxs-lookup"><span data-stu-id="6baa1-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="6baa1-119">![设计选项卡页](media/pfe-design-tabs.png "设计选项卡页")</span><span class="sxs-lookup"><span data-stu-id="6baa1-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="6baa1-120">在操作窗格上选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="6baa1-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="6baa1-121">在页面标题中进行以下设置：</span><span class="sxs-lookup"><span data-stu-id="6baa1-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="6baa1-122">**选项卡名称** - 为选项卡指定名称。</span><span class="sxs-lookup"><span data-stu-id="6baa1-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="6baa1-123">**主视图** - 在两个预定义的作业列表（*活动作业*、*所有作业* 或 *我的机器*）之间进行选择。</span><span class="sxs-lookup"><span data-stu-id="6baa1-123">**Main view** - Select between the two pre-defined job lists (*Active jobs*, *All jobs*, or *My machine*).</span></span>
    - <span data-ttu-id="6baa1-124">**详细信息视图** - 在空白值或 **作业详细信息** 之间选择。</span><span class="sxs-lookup"><span data-stu-id="6baa1-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="6baa1-125">如果选择空白值，选项卡中将没有详细视图。如果选择 **作业详细信息**，详细视图将包含在主视图中的作业列表中选择的作业的详细描述。</span><span class="sxs-lookup"><span data-stu-id="6baa1-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="6baa1-126">在 **主工具栏** 部分，选择哪些按钮应该在主工具栏中可用。</span><span class="sxs-lookup"><span data-stu-id="6baa1-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="6baa1-127">**可用操作** 列显示可以添加的所有按钮的列表。</span><span class="sxs-lookup"><span data-stu-id="6baa1-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="6baa1-128">**所选操作** 列显示当前配置中包含的所有按钮的列表。</span><span class="sxs-lookup"><span data-stu-id="6baa1-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="6baa1-129">根据需要在列之间使用按钮在列之间移动所选项。</span><span class="sxs-lookup"><span data-stu-id="6baa1-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="6baa1-130">使用 **所选操作** 列旁边的向上和向下按钮控制按钮在用户界面的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="6baa1-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="6baa1-131">在 **辅助工具栏** 部分，选择哪些按钮应该在辅助工具栏中可用。</span><span class="sxs-lookup"><span data-stu-id="6baa1-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="6baa1-132">**可用操作** 列显示可以添加的所有按钮的列表。</span><span class="sxs-lookup"><span data-stu-id="6baa1-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="6baa1-133">**所选操作** 列显示当前配置中包含的所有按钮的列表。</span><span class="sxs-lookup"><span data-stu-id="6baa1-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="6baa1-134">根据需要在列之间使用按钮在列之间移动所选项。</span><span class="sxs-lookup"><span data-stu-id="6baa1-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="6baa1-135">使用 **所选操作** 列旁边的向上和向下按钮控制按钮在用户界面的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="6baa1-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="6baa1-136">将选项卡与配置关联</span><span class="sxs-lookup"><span data-stu-id="6baa1-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="6baa1-137">设计完所需的所有选项卡后，可以将它们与配置关联。</span><span class="sxs-lookup"><span data-stu-id="6baa1-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="6baa1-138">转到 **生产控制 &gt; 设置 &gt; 配置生产车间执行**。</span><span class="sxs-lookup"><span data-stu-id="6baa1-138">Go to **Production control &gt; Setup &gt; Configure production floor execution**.</span></span>

    <span data-ttu-id="6baa1-139">![配置生产车间执行](media/pfe-config-prod-floor-execution.png "配置生产车间执行")</span><span class="sxs-lookup"><span data-stu-id="6baa1-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="6baa1-140">在 **选项卡选择** 快速选项卡上，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="6baa1-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="6baa1-141">一个新行将添加到网格中。</span><span class="sxs-lookup"><span data-stu-id="6baa1-141">A new row is added to the grid.</span></span> <span data-ttu-id="6baa1-142">对于这个新行，选择要添加到配置中的选项卡的名称。</span><span class="sxs-lookup"><span data-stu-id="6baa1-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="6baa1-143">根据需要继续添加其他选项卡。</span><span class="sxs-lookup"><span data-stu-id="6baa1-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="6baa1-144">根据需要使用工具栏上的 **上移** 和 **下移** 按钮排列选项卡。</span><span class="sxs-lookup"><span data-stu-id="6baa1-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="6baa1-145">选项卡将按照以上屏幕截图中显示的顺序从左到右显示（顶部的选项卡显示在左侧）。</span><span class="sxs-lookup"><span data-stu-id="6baa1-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>

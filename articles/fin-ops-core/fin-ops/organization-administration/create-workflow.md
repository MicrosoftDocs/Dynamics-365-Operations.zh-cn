---
title: 创建工作流概览
description: 本主题介绍如何创建工作流。
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: a643be553f3fcdfbe53f2024982a596e498830a8
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811280"
---
# <a name="create-workflows-overview"></a><span data-ttu-id="a18ea-103">创建工作流概览</span><span class="sxs-lookup"><span data-stu-id="a18ea-103">Create workflows overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a18ea-104">本主题介绍如何创建工作流。</span><span class="sxs-lookup"><span data-stu-id="a18ea-104">This topic explains how to create a workflow.</span></span>

## <a name="open-the-workflow-editor"></a><span data-ttu-id="a18ea-105">打开工作流编辑器</span><span class="sxs-lookup"><span data-stu-id="a18ea-105">Open the workflow editor</span></span>

<span data-ttu-id="a18ea-106">您正在使用的模块将确定可以创建的工作流的类型。</span><span class="sxs-lookup"><span data-stu-id="a18ea-106">The module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="a18ea-107">按照以下步骤选择工作流的类型，以创建并打开工作流编辑器。</span><span class="sxs-lookup"><span data-stu-id="a18ea-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1. <span data-ttu-id="a18ea-108">打开要为其创建新工作流的模块。</span><span class="sxs-lookup"><span data-stu-id="a18ea-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="a18ea-109">例如，要为采购申请创建工作流，单击**采购**。</span><span class="sxs-lookup"><span data-stu-id="a18ea-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2. <span data-ttu-id="a18ea-110">单击**设置**&gt;**\[模块名称\]工作流**。</span><span class="sxs-lookup"><span data-stu-id="a18ea-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3. <span data-ttu-id="a18ea-111">在显示的列表页上的“操作窗格”上，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="a18ea-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4. <span data-ttu-id="a18ea-112">在**创建工作流**页面上，选择要创建的工作流类型，然后单击**创建工作流**。</span><span class="sxs-lookup"><span data-stu-id="a18ea-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="a18ea-113">将显示工作流编辑器。</span><span class="sxs-lookup"><span data-stu-id="a18ea-113">The workflow editor appears.</span></span> <span data-ttu-id="a18ea-114">您现在可以使用以下过程来设计工作流。</span><span class="sxs-lookup"><span data-stu-id="a18ea-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="a18ea-115">将工作流元素拖到画布上</span><span class="sxs-lookup"><span data-stu-id="a18ea-115">Drag workflow elements onto the canvas</span></span>

<span data-ttu-id="a18ea-116">工作流编辑器的**工作流元素**区域包含您可以添加到工作流的元素。</span><span class="sxs-lookup"><span data-stu-id="a18ea-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="a18ea-117">要在工作流中添加元素，将元素拖到画布上。</span><span class="sxs-lookup"><span data-stu-id="a18ea-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="a18ea-118">连接元素</span><span class="sxs-lookup"><span data-stu-id="a18ea-118">Connect the elements</span></span>

<span data-ttu-id="a18ea-119">要将一个工作流元素连接到另一个元素，则将指针悬停在该元素上方，直到连接点显示。</span><span class="sxs-lookup"><span data-stu-id="a18ea-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="a18ea-120">单击连接点并将其复制到另一个元素。</span><span class="sxs-lookup"><span data-stu-id="a18ea-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="a18ea-121">确保连接所有元素。</span><span class="sxs-lookup"><span data-stu-id="a18ea-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="a18ea-122">配置工作流的属性</span><span class="sxs-lookup"><span data-stu-id="a18ea-122">Configure the properties of the workflow</span></span>

<span data-ttu-id="a18ea-123">按照以下步骤配置工作流的属性。</span><span class="sxs-lookup"><span data-stu-id="a18ea-123">Follow these steps to configure the properties of the workflow.</span></span>

1. <span data-ttu-id="a18ea-124">单击画布，确保未选择任何工作流元素。</span><span class="sxs-lookup"><span data-stu-id="a18ea-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2. <span data-ttu-id="a18ea-125">单击**属性**以打开工作流的**属性**页面。</span><span class="sxs-lookup"><span data-stu-id="a18ea-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3. <span data-ttu-id="a18ea-126">按照[配置工作流属性](configure-workflow-properties.md)主题中的步骤进行操作。</span><span class="sxs-lookup"><span data-stu-id="a18ea-126">Follow the procedures in the [Configure workflow properties](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="a18ea-127">配置工作流元素</span><span class="sxs-lookup"><span data-stu-id="a18ea-127">Configure the elements of the workflow</span></span>

<span data-ttu-id="a18ea-128">配置您拖到画布中的各个元素。</span><span class="sxs-lookup"><span data-stu-id="a18ea-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="a18ea-129">有关如何配置各个工作流元素的信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="a18ea-129">For information about how to configure each workflow element, see the following topics:</span></span>

- [<span data-ttu-id="a18ea-130">配置工作流中的手动任务</span><span class="sxs-lookup"><span data-stu-id="a18ea-130">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
- [<span data-ttu-id="a18ea-131">配置工作流中的自动化任务</span><span class="sxs-lookup"><span data-stu-id="a18ea-131">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
- [<span data-ttu-id="a18ea-132">配置工作流中的审核流程</span><span class="sxs-lookup"><span data-stu-id="a18ea-132">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
- [<span data-ttu-id="a18ea-133">配置工作流中的审核步骤</span><span class="sxs-lookup"><span data-stu-id="a18ea-133">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
- [<span data-ttu-id="a18ea-134">配置工作流中的手动决策</span><span class="sxs-lookup"><span data-stu-id="a18ea-134">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
- [<span data-ttu-id="a18ea-135">配置工作流中的有条件决策</span><span class="sxs-lookup"><span data-stu-id="a18ea-135">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
- [<span data-ttu-id="a18ea-136">配置工作流中的并行分支</span><span class="sxs-lookup"><span data-stu-id="a18ea-136">Configure parallel branches in a workflow</span></span>](configure-parallel-activity-workflow.md)
- [<span data-ttu-id="a18ea-137">配置并行分支</span><span class="sxs-lookup"><span data-stu-id="a18ea-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
- [<span data-ttu-id="a18ea-138">配置行项工作流</span><span class="sxs-lookup"><span data-stu-id="a18ea-138">Configure line-item workflows</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="a18ea-139">解决任何错误或警告</span><span class="sxs-lookup"><span data-stu-id="a18ea-139">Resolve any errors or warnings</span></span>

<span data-ttu-id="a18ea-140">位于工作流编辑器底部的**错误和警告**窗格显示为工作流生成的消息。</span><span class="sxs-lookup"><span data-stu-id="a18ea-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="a18ea-141">要查找出现错误或警告的元素，请双击错误或警告消息。</span><span class="sxs-lookup"><span data-stu-id="a18ea-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="a18ea-142">必须解决所有错误和警告，然后才能激活工作流。</span><span class="sxs-lookup"><span data-stu-id="a18ea-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="a18ea-143">保存并激活工作流</span><span class="sxs-lookup"><span data-stu-id="a18ea-143">Save and activate the workflow</span></span>

<span data-ttu-id="a18ea-144">在您准备好保存和激活工作流时，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="a18ea-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1. <span data-ttu-id="a18ea-145">单击**保存并关闭**以关闭工作流编辑器并打开**保存工作流**页面。</span><span class="sxs-lookup"><span data-stu-id="a18ea-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2. <span data-ttu-id="a18ea-146">输入有关已对此工作流进行的更改的注释，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="a18ea-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3. <span data-ttu-id="a18ea-147">如果解决了所有错误和警告，将显示**激活工作流**页面。</span><span class="sxs-lookup"><span data-stu-id="a18ea-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="a18ea-148">选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="a18ea-148">Select one of the following options:</span></span>

    - <span data-ttu-id="a18ea-149">要激活工作流的此版本，请单击**激活新版本**。</span><span class="sxs-lookup"><span data-stu-id="a18ea-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="a18ea-150">当工作流处于活动状态下时，用户可向其提交文档进行处理。</span><span class="sxs-lookup"><span data-stu-id="a18ea-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    - <span data-ttu-id="a18ea-151">如果不希望激活该版本，请单击**不激活新版本**。</span><span class="sxs-lookup"><span data-stu-id="a18ea-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="a18ea-152">您可以在以后激活工作流。</span><span class="sxs-lookup"><span data-stu-id="a18ea-152">You can activate the workflow later.</span></span>

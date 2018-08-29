---
title: "创建工作流"
description: "本主题介绍如何创建工作流。"
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 0edf6f1a97b3bbd074168a3cb8bb5c2375492b71
ms.contentlocale: zh-cn
ms.lasthandoff: 08/08/2018

---

# <a name="create-workflows"></a><span data-ttu-id="5a9a2-103">创建工作流</span><span class="sxs-lookup"><span data-stu-id="5a9a2-103">Create workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a9a2-104">本主题介绍如何创建工作流。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-104">This topic explains how to create a workflow.</span></span>

<a name="open-the-workflow-editor"></a><span data-ttu-id="5a9a2-105">打开工作流编辑器</span><span class="sxs-lookup"><span data-stu-id="5a9a2-105">Open the workflow editor</span></span>
------------------------

<span data-ttu-id="5a9a2-106">您使用的 Microsoft Dynamics 365 for Finance and Operations 模块将确定可以创建的工作流类型。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-106">The Microsoft Dynamics 365 for Finance and Operations module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="5a9a2-107">按照以下步骤选择工作流的类型，以创建并打开工作流编辑器。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1.  <span data-ttu-id="5a9a2-108">打开要为其创建新工作流的模块。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="5a9a2-109">例如，要为采购申请创建工作流，单击**采购**。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2.  <span data-ttu-id="5a9a2-110">单击**设置**&gt;**\[模块名称\]工作流**。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3.  <span data-ttu-id="5a9a2-111">在显示的列表页上的“操作窗格”上，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4.  <span data-ttu-id="5a9a2-112">在**创建工作流**页面上，选择要创建的工作流类型，然后单击**创建工作流**。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="5a9a2-113">将显示工作流编辑器。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-113">The workflow editor appears.</span></span> <span data-ttu-id="5a9a2-114">您现在可以使用以下过程来设计工作流。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="5a9a2-115">将工作流元素拖到画布上</span><span class="sxs-lookup"><span data-stu-id="5a9a2-115">Drag workflow elements onto the canvas</span></span>
<span data-ttu-id="5a9a2-116">工作流编辑器的**工作流元素**区域包含您可以添加到工作流的元素。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="5a9a2-117">要在工作流中添加元素，将元素拖到画布上。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="5a9a2-118">连接元素</span><span class="sxs-lookup"><span data-stu-id="5a9a2-118">Connect the elements</span></span>
<span data-ttu-id="5a9a2-119">要将一个工作流元素连接到另一个元素，则将指针悬停在该元素上方，直到连接点显示。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="5a9a2-120">单击连接点并将其复制到另一个元素。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="5a9a2-121">确保连接所有元素。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="5a9a2-122">配置工作流的属性</span><span class="sxs-lookup"><span data-stu-id="5a9a2-122">Configure the properties of the workflow</span></span>
<span data-ttu-id="5a9a2-123">按照以下步骤配置工作流的属性。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-123">Follow these steps to configure the properties of the workflow.</span></span>

1.  <span data-ttu-id="5a9a2-124">单击画布，确保未选择任何工作流元素。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2.  <span data-ttu-id="5a9a2-125">单击**属性**以打开工作流的**属性**页面。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3.  <span data-ttu-id="5a9a2-126">按照“[配置工作流的属性](configure-workflow-properties.md)”主题中的步骤进行操作。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-126">Follow the procedures in the [Configure the properties of a workflow](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="5a9a2-127">配置工作流元素</span><span class="sxs-lookup"><span data-stu-id="5a9a2-127">Configure the elements of the workflow</span></span>
<span data-ttu-id="5a9a2-128">配置您拖到画布中的各个元素。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="5a9a2-129">有关如何配置各个工作流元素的信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="5a9a2-129">For information about how to configure each workflow element, see the following topics:</span></span>

-   [<span data-ttu-id="5a9a2-130">配置手动任务</span><span class="sxs-lookup"><span data-stu-id="5a9a2-130">Configure a manual task</span></span>](configure-manual-task-workflow.md)
-   [<span data-ttu-id="5a9a2-131">配置自动化任务</span><span class="sxs-lookup"><span data-stu-id="5a9a2-131">Configure an automated task</span></span>](configure-automated-task-workflow.md)
-   [<span data-ttu-id="5a9a2-132">配置审核流程</span><span class="sxs-lookup"><span data-stu-id="5a9a2-132">Configure an approval process</span></span>](configure-approval-process-workflow.md)
-   [<span data-ttu-id="5a9a2-133">配置审核步骤</span><span class="sxs-lookup"><span data-stu-id="5a9a2-133">Configure an approval step</span></span>](configure-approval-step-workflow.md)
-   [<span data-ttu-id="5a9a2-134">配置手动决策</span><span class="sxs-lookup"><span data-stu-id="5a9a2-134">Configure a manual decision</span></span>](configure-manual-decision-workflow.md)
-   [<span data-ttu-id="5a9a2-135">配置条件决策</span><span class="sxs-lookup"><span data-stu-id="5a9a2-135">Configure a conditional decision</span></span>](configure-conditional-decision-workflow.md)
-   [<span data-ttu-id="5a9a2-136">配置并行活动</span><span class="sxs-lookup"><span data-stu-id="5a9a2-136">Configure a parallel activity</span></span>](configure-parallel-activity-workflow.md)
-   [<span data-ttu-id="5a9a2-137">配置一个并行分支</span><span class="sxs-lookup"><span data-stu-id="5a9a2-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
-   [<span data-ttu-id="5a9a2-138">配置行项工作流</span><span class="sxs-lookup"><span data-stu-id="5a9a2-138">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="5a9a2-139">解决任何错误或警告</span><span class="sxs-lookup"><span data-stu-id="5a9a2-139">Resolve any errors or warnings</span></span>
<span data-ttu-id="5a9a2-140">位于工作流编辑器底部的**错误和警告**窗格显示为工作流生成的消息。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="5a9a2-141">要查找出现错误或警告的元素，请双击错误或警告消息。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="5a9a2-142">必须解决所有错误和警告，然后才能激活工作流。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="5a9a2-143">保存并激活工作流</span><span class="sxs-lookup"><span data-stu-id="5a9a2-143">Save and activate the workflow</span></span>
<span data-ttu-id="5a9a2-144">在您准备好保存和激活工作流时，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1.  <span data-ttu-id="5a9a2-145">单击**保存并关闭**以关闭工作流编辑器并打开**保存工作流**页面。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2.  <span data-ttu-id="5a9a2-146">输入有关已对此工作流进行的更改的注释，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3.  <span data-ttu-id="5a9a2-147">如果解决了所有错误和警告，将显示**激活工作流**页面。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="5a9a2-148">选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="5a9a2-148">Select one of the following options:</span></span>
    -   <span data-ttu-id="5a9a2-149">要激活工作流的此版本，请单击**激活新版本**。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="5a9a2-150">当工作流处于活动状态下时，用户可向其提交文档进行处理。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    -   <span data-ttu-id="5a9a2-151">如果不希望激活该版本，请单击**不激活新版本**。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="5a9a2-152">您可以在以后激活工作流。</span><span class="sxs-lookup"><span data-stu-id="5a9a2-152">You can activate the workflow later.</span></span>







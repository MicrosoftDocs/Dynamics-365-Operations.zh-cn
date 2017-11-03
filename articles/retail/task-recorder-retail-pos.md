---
title: "POS 的任务录制器和帮助"
description: "此主题介绍如何在 Retail Modern POS 和 Cloud POS 中使用任务录制器。"
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a527136f77b65ef5a43576291e38cb168dbbd322
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="task-recorder-and-help-for-pos"></a><span data-ttu-id="b3fb9-103">POS 的任务录制器和帮助</span><span class="sxs-lookup"><span data-stu-id="b3fb9-103">Task recorder and Help for POS</span></span>

<span data-ttu-id="b3fb9-104">此主题介绍如何在 Retail Modern POS 和 Cloud POS 中使用任务录制器。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-104">This topic describes how to use Task recorder in Retail Modern POS and Cloud POS.</span></span>

<a name="overview"></a><span data-ttu-id="b3fb9-105">概览</span><span class="sxs-lookup"><span data-stu-id="b3fb9-105">Overview</span></span>
--------

<span data-ttu-id="b3fb9-106">Retail Modern POS 或 Cloud POS 中的任务录制器是一个新解决方案，注重高响应性。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-106">Task recorder in Retail Modern POS or Cloud POS is a new solution that was built with a focus on high responsiveness.</span></span> <span data-ttu-id="b3fb9-107">它提供灵活的应用程序编程接口 (API) 以实现可扩展性，并提供与业务流程录制的使用者的无缝集成。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-107">It provides a flexible application programming interface (API) for extensibility and seamless integration with consumers of business process recordings.</span></span> <span data-ttu-id="b3fb9-108">此外，还提供了任务录制器与Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) 上的业务流程建模器 (BPM) 工具的集成。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-108">Additionally, Task recorder integration with the Business process modeler (BPM) tool on Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) has been brought forward.</span></span> <span data-ttu-id="b3fb9-109">因此，用户能够继续从录制生成丰富的业务流程图来分析和设计自己的应用程序。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-109">Therefore, users can continue to produce rich business process diagrams from recordings to analyze and design their applications.</span></span>

## <a name="architecture"></a><span data-ttu-id="b3fb9-110">体系结构</span><span class="sxs-lookup"><span data-stu-id="b3fb9-110">Architecture</span></span>
<span data-ttu-id="b3fb9-111">任务录制器可以在客户端非常精确地录制用户操作。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-111">Task recorder can record user actions in the client with exact fidelity.</span></span> <span data-ttu-id="b3fb9-112">每一项控制都会被全面感知，以通知任务录制器用户操作的执行。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-112">Each control is instrumented to notify Task recorder about the execution of a user action.</span></span> <span data-ttu-id="b3fb9-113">控制通知任务录制器发生的事件，并实时传递相应用户操作的所有相关信息。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-113">The control notifies Task recorder that an event occurred and passes along all pertinent information about the corresponding user action in real time.</span></span> <span data-ttu-id="b3fb9-114">通过此信息，任务录制器可以捕获用户是操作的类型（如按钮单击、值输入或导航），以及所有与用户操作相关的数据（如输入数据值和类型、表单上下文或记录上下文）。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-114">From this information, Task recorder can capture the type of user action (such as a button click, value entry, or navigation) and any data that is related to the user action (such as the input data value and type, form context, or record context).</span></span> <span data-ttu-id="b3fb9-115">任务录制器继续显示包含足够详细信息的信息，以帮助保证录制播放可以准确地执行录制的操作，就如同用户在执行。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-115">Task recorder persists the information with enough detail to help guarantee that a playback of the recording can perform the recorded actions exactly as the user performed them.</span></span> <span data-ttu-id="b3fb9-116">（Retail modern POS 或 Cloud POS 尚未实现播放功能。）</span><span class="sxs-lookup"><span data-stu-id="b3fb9-116">(The playback feature isn't yet implemented at Retail modern POS or Cloud POS.)</span></span>

## <a name="basic-configuration"></a><span data-ttu-id="b3fb9-117">基本配置</span><span class="sxs-lookup"><span data-stu-id="b3fb9-117">Basic configuration</span></span>
<span data-ttu-id="b3fb9-118">要在 POS 启用任务录制，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-118">To enable task recording in POS, follow these steps.</span></span>

1.  <span data-ttu-id="b3fb9-119">单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **收银机**。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-119">Click **Retail** &gt; **Channel Setup** &gt; **POS Setup** &gt; **Registers**.</span></span>
2.  <span data-ttu-id="b3fb9-120">单击收银机启用任务录制。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-120">Click the register to enable task recording on.</span></span>
3.  <span data-ttu-id="b3fb9-121">在**收银机**选项卡，在**常规**快速选项卡，将**启用任务录制**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-121">On the **Register** tab, on the **General** FastTab, set the **Enable task recording** option to **Yes**.</span></span>
4.  <span data-ttu-id="b3fb9-122">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-122">Click **Save**.</span></span>
5.  <span data-ttu-id="b3fb9-123">转到**零售** &gt; **零售 IT** &gt; **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-123">Go to **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
6.  <span data-ttu-id="b3fb9-124">选择**收银机 (1090)** 作业，然后单击**立即运行**。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-124">Select the **Registers (1090)** job, and then click **Run now**.</span></span>

## <a name="create-a-recording"></a><span data-ttu-id="b3fb9-125">创建录制</span><span class="sxs-lookup"><span data-stu-id="b3fb9-125">Create a recording</span></span>
<span data-ttu-id="b3fb9-126">执行以下步骤使用任务录制器创建新录制。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-126">Follow these steps to create a new recording using Task recorder.</span></span>

1.  <span data-ttu-id="b3fb9-127">启动 Retail Modern POS 或 Cloud POS，并登录。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-127">Start Retail Modern POS or Cloud POS, and sign in.</span></span>
2.  <span data-ttu-id="b3fb9-128">在**设置**页，在**任务录制器**部分，单击**打开任务录制器**。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-128">On the **Settings** page, in the **Task Recorder** section, click **Open task recorder**.</span></span> <span data-ttu-id="b3fb9-129">**任务录制器**窗格出现。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-129">The **Task recorder** pane appears.</span></span> <span data-ttu-id="b3fb9-130">在开始新录制前，您可以单击右上角的**关闭**按钮 (**X**) 关闭**任务录制器**窗格。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-130">You can click the **Close** button (**X**) in the upper-right corner to close the **Task recorder** pane before you begin a new recording.</span></span> <span data-ttu-id="b3fb9-131">若要重新打开窗格，请重复执行步骤 2。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-131">To reopen the pane, repeat step 2.</span></span>
<span data-ttu-id="b3fb9-132">[![任务录制器窗格](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span><span class="sxs-lookup"><span data-stu-id="b3fb9-132">[![Task recorder pane](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span></span>

3.  <span data-ttu-id="b3fb9-133">输入录制的名称和描述，然后单击**开始**。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-133">Enter a name and description for the recording, and then click **Start**.</span></span> <span data-ttu-id="b3fb9-134">单击**开始**后，录制会话随即开始。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-134">The recording session begins as soon as you click **Start**.</span></span>

<span data-ttu-id="b3fb9-135">**注意：**，如果您在录制正在进行时单击右上角的**关闭**按钮 (**X**)，**任务录制器**窗格将关闭，但录制会话不会结束。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-135">**Note:** If you click the **Close** button (**X**) in the upper-right corner while recording is in progress, the **Task recorder** pane is closed, but the recording session isn't ended.</span></span> <span data-ttu-id="b3fb9-136">若要重新打开任务录制器窗格，单击屏幕顶部的**帮助**按钮（问号）。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-136">To reopen the Task recorder pane, click the **Help** button (question mark) at the top of the screen.</span></span> 

<span data-ttu-id="b3fb9-137">[![问号](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="b3fb9-137">[![Question mark](./media/help.jpg)](./media/help.jpg)</span></span>

4.  <span data-ttu-id="b3fb9-138">单击**开始**后，任务录制器进入录制模式。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-138">After you click **Start**, Task recorder enters recording mode.</span></span> <span data-ttu-id="b3fb9-139">**任务录制器**窗格显示与录制流程相关的信息和控制。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-139">The **Task recorder** pane shows information and controls that are related to the recording process.</span></span>
5.  <span data-ttu-id="b3fb9-140">执行您希望在 Retail Modern POS 或 Cloud POS 用户界面 (UI) 执行的操作。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-140">Perform the actions that you want to perform in the Retail Modern POS or Cloud POS user interface (UI).</span></span>
6.  <span data-ttu-id="b3fb9-141">若要结束录制会话，单击**停止**。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-141">To end the recording session, click **Stop**.</span></span>

## <a name="download-options"></a><span data-ttu-id="b3fb9-142">下载选项</span><span class="sxs-lookup"><span data-stu-id="b3fb9-142">Download options</span></span>
<span data-ttu-id="b3fb9-143">在结束录制会话后，多个选项将显示，以便您可以下载您的录制。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-143">After you end the recording session, several options are shown, so that you can download your recording.</span></span> 
<span data-ttu-id="b3fb9-144">[![下载选项](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span><span class="sxs-lookup"><span data-stu-id="b3fb9-144">[![Download options](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span></span>

### <a name="save-to-this-pc"></a><span data-ttu-id="b3fb9-145">保存到此 PC</span><span class="sxs-lookup"><span data-stu-id="b3fb9-145">Save to this PC</span></span>

<span data-ttu-id="b3fb9-146">您可以使用录制包播放任务指南、维护录制或者编辑录制中的注释。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-146">You can use the recording package to play a Task guide, maintain the recording, or edit the annotations in the recording.</span></span> <span data-ttu-id="b3fb9-147">（Retail Modern POS 和 Cloud POS 尚未实现此功能。）</span><span class="sxs-lookup"><span data-stu-id="b3fb9-147">(This feature isn't yet implemented in Retail Modern POS and Cloud POS.)</span></span>

### <a name="export-as-word-document"></a><span data-ttu-id="b3fb9-148">导出为 Word 文档</span><span class="sxs-lookup"><span data-stu-id="b3fb9-148">Export as Word document</span></span>

<span data-ttu-id="b3fb9-149">您可以将录制作为 Microsoft Word 文档保存。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-149">You can save the recording as a Microsoft Word document.</span></span> <span data-ttu-id="b3fb9-150">此文档将包含录制的步骤和捕获的屏幕快照。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-150">The document will contain the recorded steps and the screenshots that were captured.</span></span>

### <a name="save-as-developer-recording"></a><span data-ttu-id="b3fb9-151">另存为开发人员录制</span><span class="sxs-lookup"><span data-stu-id="b3fb9-151">Save as developer recording</span></span>

<span data-ttu-id="b3fb9-152">原始录制文件对于开发人员方案（如测试代码生成）很有用。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-152">The raw recording file will be useful for developer scenarios such as test code generation.</span></span> <span data-ttu-id="b3fb9-153">（此功能尚未实现。）</span><span class="sxs-lookup"><span data-stu-id="b3fb9-153">(This feature isn't yet implemented.)</span></span>

## <a name="recording-controls"></a><span data-ttu-id="b3fb9-154">录制控制</span><span class="sxs-lookup"><span data-stu-id="b3fb9-154">Recording controls</span></span>
### <a name="recording-controlsmediacontrolsjpgmediacontrolsjpg"></a><span data-ttu-id="b3fb9-155">[![录制控制](./media/controls.jpg)](./media/controls.jpg)</span><span class="sxs-lookup"><span data-stu-id="b3fb9-155">[![Recording controls](./media/controls.jpg)](./media/controls.jpg)</span></span>

### <a name="stop"></a><span data-ttu-id="b3fb9-156">停止</span><span class="sxs-lookup"><span data-stu-id="b3fb9-156">Stop</span></span>

<span data-ttu-id="b3fb9-157">单击**停止**可结束录制会话。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-157">Click **Stop** to end the recording session.</span></span> <span data-ttu-id="b3fb9-158">请注意，会话在结束后不能重新启动。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-158">Note that you can't restart a session after you end it.</span></span> <span data-ttu-id="b3fb9-159">因此，在结束之前请确保录制已完成。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-159">Therefore, make sure that the recording is completed before you end it.</span></span>

### <a name="pause"></a><span data-ttu-id="b3fb9-160">暂停</span><span class="sxs-lookup"><span data-stu-id="b3fb9-160">Pause</span></span>

<span data-ttu-id="b3fb9-161">单击**暂停**可临时停止（暂停）录制会话并继续执行操作。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-161">Click **Pause** to temporarily stop (pause) the recording session and continue with the operation.</span></span> <span data-ttu-id="b3fb9-162">在单击**暂停**后执行的步骤不会被录制。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-162">Steps that you perform after you click **Pause** aren't recorded.</span></span>

### <a name="continue"></a><span data-ttu-id="b3fb9-163">继续</span><span class="sxs-lookup"><span data-stu-id="b3fb9-163">Continue</span></span>

<span data-ttu-id="b3fb9-164">要恢复录制会话，在暂停后单击**继续**。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-164">To resume the recording session after you've paused it, click **Continue**.</span></span>

### <a name="capture-screenshots"></a><span data-ttu-id="b3fb9-165">捕获屏幕快照</span><span class="sxs-lookup"><span data-stu-id="b3fb9-165">Capture screenshots</span></span>

<span data-ttu-id="b3fb9-166">任务录制器可以在您录制业务流程时捕获 Retail Modern POS UI 的屏幕快照。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-166">Task recorder can capture screenshots of the Retail Modern POS UI as you record a business process.</span></span> <span data-ttu-id="b3fb9-167">如果您将录制下载为 Word 文档，任务录制器将使用屏幕快照。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-167">Task recorder uses the screenshots if you download the recording as a Word document.</span></span> <span data-ttu-id="b3fb9-168">若要开启屏幕快照捕获功能，将**捕捉屏幕快照**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-168">To turn on the screenshot capture feature, set the **Capture screenshot** option to **Yes**.</span></span> 

#### <a name="note"></a><span data-ttu-id="b3fb9-169">单据</span><span class="sxs-lookup"><span data-stu-id="b3fb9-169">Note</span></span>
> <span data-ttu-id="b3fb9-170">Cloud POS 不支持捕获屏幕快照功能。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-170">Capture screenshot functionality is not supported in Cloud POS.</span></span>

### <a name="start-task-and-end-task"></a><span data-ttu-id="b3fb9-171">开始任务和结束任务</span><span class="sxs-lookup"><span data-stu-id="b3fb9-171">Start task and End task</span></span>

<span data-ttu-id="b3fb9-172">可以通过使用**开始任务**和**结束****任务**按钮来指定一组已分组步骤的开始和结束。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-172">You can specify the beginning and end of a set of grouped steps by using the **Start task** and **End** **task** buttons.</span></span> <span data-ttu-id="b3fb9-173">单击**开始任务**添加“开始任务”步骤，然后执行组中应包括的步骤。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-173">Click **Start task** to add a “Start Task” step, and then perform the steps that should be included in the group.</span></span> <span data-ttu-id="b3fb9-174">在您完成该组步骤的执行后，单击**结束任务**。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-174">After you've finished performing the steps for the group, click **End task**.</span></span> <span data-ttu-id="b3fb9-175">任务帮助您组织您的过程。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-175">Tasks help you organize your procedures.</span></span> <span data-ttu-id="b3fb9-176">任务可以嵌套在其他任务内。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-176">Tasks can be nested within other tasks.</span></span> <span data-ttu-id="b3fb9-177">这样，您就可以更好地组织非常长的复杂业务流程。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-177">In this way, you can better organize very long and complex business processes.</span></span>

## <a name="adding-annotations"></a><span data-ttu-id="b3fb9-178">添加注释</span><span class="sxs-lookup"><span data-stu-id="b3fb9-178">Adding annotations</span></span>
<span data-ttu-id="b3fb9-179">注释是您在录制中添加到步骤的其他文本。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-179">An annotation is additional text that you add to a step in a recording.</span></span> <span data-ttu-id="b3fb9-180">例如，您可以使用注释为用户提供更多上下文或说明。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-180">For example, you can use annotations to give the user more context or instructions.</span></span> <span data-ttu-id="b3fb9-181">您可以在一个步骤之前或之后添加注释。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-181">You can add annotations before or after a step.</span></span> <span data-ttu-id="b3fb9-182">您可以通过单击步骤右侧的**编辑**按钮（铅笔符号）将注释添加到任何步骤。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-182">You can add an annotation to any step by clicking the **Edit** button (pencil symbol) to the right of the step.</span></span> 

<span data-ttu-id="b3fb9-183">[![编辑步骤的按钮](./media/annotate.jpg)](./media/annotate.jpg)</span><span class="sxs-lookup"><span data-stu-id="b3fb9-183">[![Edit button for a step](./media/annotate.jpg)](./media/annotate.jpg)</span></span>

### <a name="texts-and-notes"></a><span data-ttu-id="b3fb9-184">文本和注释</span><span class="sxs-lookup"><span data-stu-id="b3fb9-184">Texts and notes</span></span>

<span data-ttu-id="b3fb9-185">您可以使用**文本**和**注释**字段来添加应与任务指南中的步骤关联的文本。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-185">You can use the **Texts** and **Notes** fields to add text that should be associated with a step in a Task guide.</span></span>
<span data-ttu-id="b3fb9-186">[![文本和注释字段](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span><span class="sxs-lookup"><span data-stu-id="b3fb9-186">[![Text and Notes fields](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span></span>

#### <a name="text"></a><span data-ttu-id="b3fb9-187">文本</span><span class="sxs-lookup"><span data-stu-id="b3fb9-187">Text</span></span>

<span data-ttu-id="b3fb9-188">在**文本**字段中输入的文本将在任务指南的步骤文本*上方*显示。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-188">Text that you enter in the **Text** field appears *above* the step text in the Task guide.</span></span> <span data-ttu-id="b3fb9-189">此位置适合您希望用户在完成步骤前阅读的文本。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-189">This location is appropriate for text that you want the user to read before he or she completes the step.</span></span>

#### <a name="notes"></a><span data-ttu-id="b3fb9-190">注释</span><span class="sxs-lookup"><span data-stu-id="b3fb9-190">Notes</span></span>

<span data-ttu-id="b3fb9-191">在**注释**字段中输入的文本将在任务指南的步骤文本*下方*显示。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-191">Text that you enter in the **Notes** field appears *below* the step text in the Task guide.</span></span> <span data-ttu-id="b3fb9-192">若要阅读注释文本，用户必须在弹出窗口中展开步骤文本。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-192">To read the note text, the user must expand the step text in the pop-up window.</span></span> <span data-ttu-id="b3fb9-193">此位置适合可能对用户有用，但用户完成操作所不需要的可选阅读材料或其他信息。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-193">This location is appropriate for optional reading material or other information that might be useful to the user, but that the user doesn't require in order to complete the action.</span></span>

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a><span data-ttu-id="b3fb9-194">Retail Modern POS 和 Cloud POS 中的帮助</span><span class="sxs-lookup"><span data-stu-id="b3fb9-194">Help in Retail Modern POS and Cloud POS</span></span>
<span data-ttu-id="b3fb9-195">要在 Retail Modern POS 和 Cloud POS 的“帮助”窗格中显示您自己的自定义任务录制以便它们可作为文本查看，您必须将任务录制保存到自己的 BPM 库，然后更新帮助系统参数以指向您的 BPM 库。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-195">To show your own custom task recordings in the Help pane of Retail Modern POS and Cloud POS so that they can be viewed as text, you must save your task recordings to your own BPM library, and then update your Help system parameters to point to your BPM library.</span></span> <span data-ttu-id="b3fb9-196">有关更多信息，请参阅 [连接帮助系统](../fin-and-ops/get-started/help-connect.md)。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-196">For more information, see [Connecting the Help system](../fin-and-ops/get-started/help-connect.md).</span></span> <span data-ttu-id="b3fb9-197">Retail Modern POS 和 Cloud POS 帮助实时搜索 LCS。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-197">Retail Modern POS and Cloud POS Help searches LCS in real time.</span></span> <span data-ttu-id="b3fb9-198">它搜索在 Microsoft Dynamics 365 for Retail 帮助系统参数中选择的所有 BPM 库，并显示相关结果。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-198">It searches across all the BPM libraries that are selected in the Microsoft Dynamics 365 for Retail Help system parameters and shows the relevant results.</span></span> <span data-ttu-id="b3fb9-199">若要访问**帮助**菜单，单击屏幕顶部的**帮助**按钮（问号），然后在搜索框中键入流程名称并点击搜索按钮。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-199">To access the **Help** menu, click the **Help** button (question mark) at the top of the screen and then in the search box type your process name and hit the search button.</span></span> 

<span data-ttu-id="b3fb9-200">[![帮助按钮](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="b3fb9-200">[![Help button](./media/help.jpg)](./media/help.jpg)</span></span> 

<span data-ttu-id="b3fb9-201">当您在搜索结果中单击任务指南时，可以作为帮助主题查看步骤或将步骤导出到 Word 文档。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-201">When you click a Task guide in the search results, you can either view the steps as a Help topic or export the steps to a Word document.</span></span> 
#### <a name="note"></a><span data-ttu-id="b3fb9-202">单据</span><span class="sxs-lookup"><span data-stu-id="b3fb9-202">Note</span></span>
> <span data-ttu-id="b3fb9-203">Retail Modern POS 和 Cloud POS 中的帮助不会根据您所处的窗体或正在执行的操作提供任务指南。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-203">Help in Retail Modern POS and Cloud POS will not bring up task guides according to what form you're on or operation you're doing.</span></span> <span data-ttu-id="b3fb9-204">您必须输入在搜索框中键入流程名称，然后单击**搜索**。</span><span class="sxs-lookup"><span data-stu-id="b3fb9-204">You have to type the process name in the search box and then click **Search**.</span></span>



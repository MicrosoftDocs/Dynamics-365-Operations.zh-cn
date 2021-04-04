---
title: 配置工作流中的手动任务
description: 本主题说明如何配置手动任务的属性。
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee759cbf51555a32045e74f40138a04f330d7eb2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559465"
---
# <a name="configure-manual-tasks-in-a-workflow"></a><span data-ttu-id="5272c-103">配置工作流中的手动任务</span><span class="sxs-lookup"><span data-stu-id="5272c-103">Configure manual tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5272c-104">本主题说明如何配置手动任务的属性。</span><span class="sxs-lookup"><span data-stu-id="5272c-104">This topic explains how to configure the properties for a manual task.</span></span>

<span data-ttu-id="5272c-105">要配置手动任务，在工作流编辑器中，右键单击任务，然后单击 **属性** 打开 **属性** 页面。</span><span class="sxs-lookup"><span data-stu-id="5272c-105">To configure a manual task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="5272c-106">然后使用以下过程配置手动任务的属性。</span><span class="sxs-lookup"><span data-stu-id="5272c-106">Then use the following procedures to configure the properties for the manual task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="5272c-107">为任务命名</span><span class="sxs-lookup"><span data-stu-id="5272c-107">Name the task</span></span>

<span data-ttu-id="5272c-108">按照以下为手动任务输入名称。</span><span class="sxs-lookup"><span data-stu-id="5272c-108">Follow these steps to enter a name for the manual task.</span></span>

1. <span data-ttu-id="5272c-109">在左侧窗格中，单击 **基本设置**。</span><span class="sxs-lookup"><span data-stu-id="5272c-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="5272c-110">在 **名称** 字段中，为该任务输入唯一名称。</span><span class="sxs-lookup"><span data-stu-id="5272c-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="5272c-111">输入主题行和说明</span><span class="sxs-lookup"><span data-stu-id="5272c-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="5272c-112">必须为分配到任务的用户提供主题行和说明。</span><span class="sxs-lookup"><span data-stu-id="5272c-112">You must provide a subject line and instructions to users who are assigned to the task.</span></span> <span data-ttu-id="5272c-113">例如，如果您在为采购申请配置任务，则分配到该任务的用户在 **采购申请** 页面看到主题行和说明。</span><span class="sxs-lookup"><span data-stu-id="5272c-113">For example, if you're configuring a task for purchase requisitions, the user who is assigned to the task sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="5272c-114">主题行显示在页面的消息栏中。</span><span class="sxs-lookup"><span data-stu-id="5272c-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="5272c-115">然后用户可单击消息栏中的图标查看说明。</span><span class="sxs-lookup"><span data-stu-id="5272c-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="5272c-116">按照以下步骤输入主题行和说明。</span><span class="sxs-lookup"><span data-stu-id="5272c-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="5272c-117">在左侧窗格中，单击 **基本设置**。</span><span class="sxs-lookup"><span data-stu-id="5272c-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="5272c-118">在 **工作项主题** 字段中，输入主题行。</span><span class="sxs-lookup"><span data-stu-id="5272c-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="5272c-119">要个性化主题行，可以插入占位符。</span><span class="sxs-lookup"><span data-stu-id="5272c-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="5272c-120">向用户显示主题行时，占位符由适当的数据代替。</span><span class="sxs-lookup"><span data-stu-id="5272c-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="5272c-121">按照以下步骤插入占位符：</span><span class="sxs-lookup"><span data-stu-id="5272c-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="5272c-122">在文本框中，单击应该出现占位符的位置。</span><span class="sxs-lookup"><span data-stu-id="5272c-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="5272c-123">单击 **插入占位符**。</span><span class="sxs-lookup"><span data-stu-id="5272c-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="5272c-124">在出现的列表中，选择要插入的占位符。</span><span class="sxs-lookup"><span data-stu-id="5272c-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="5272c-125">单击 **插入**。</span><span class="sxs-lookup"><span data-stu-id="5272c-125">Click **Insert**.</span></span>

4. <span data-ttu-id="5272c-126">若要添加主题行的翻译，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="5272c-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="5272c-127">单击 **翻译**。</span><span class="sxs-lookup"><span data-stu-id="5272c-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="5272c-128">在出现的页面上，单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5272c-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="5272c-129">在出现的列表中，选择您输入文本使用的语言。</span><span class="sxs-lookup"><span data-stu-id="5272c-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="5272c-130">在 **已翻译的文本** 字段中，输入文本。</span><span class="sxs-lookup"><span data-stu-id="5272c-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="5272c-131">如果要对文本进行个性化设置，可以如步骤 3 所述插入占位符。</span><span class="sxs-lookup"><span data-stu-id="5272c-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="5272c-132">单击 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="5272c-132">Click **Close**.</span></span>

5. <span data-ttu-id="5272c-133">在 **工作项说明** 字段中，输入说明。</span><span class="sxs-lookup"><span data-stu-id="5272c-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="5272c-134">要对说明进行个性化设置，可以插入占位符。</span><span class="sxs-lookup"><span data-stu-id="5272c-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="5272c-135">向用户显示说明时，占位符由适当的数据代替。</span><span class="sxs-lookup"><span data-stu-id="5272c-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="5272c-136">按照以下步骤插入占位符：</span><span class="sxs-lookup"><span data-stu-id="5272c-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="5272c-137">在文本框中，单击应该出现占位符的位置。</span><span class="sxs-lookup"><span data-stu-id="5272c-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="5272c-138">单击 **插入占位符**。</span><span class="sxs-lookup"><span data-stu-id="5272c-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="5272c-139">在出现的列表中，选择要插入的占位符。</span><span class="sxs-lookup"><span data-stu-id="5272c-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="5272c-140">单击 **插入**。</span><span class="sxs-lookup"><span data-stu-id="5272c-140">Click **Insert**.</span></span>

7. <span data-ttu-id="5272c-141">若要添加说明的翻译，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="5272c-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="5272c-142">单击 **翻译**。</span><span class="sxs-lookup"><span data-stu-id="5272c-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="5272c-143">在出现的页面上，单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5272c-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="5272c-144">在出现的列表中，选择您输入文本使用的语言。</span><span class="sxs-lookup"><span data-stu-id="5272c-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="5272c-145">在 **已翻译的文本** 字段中，输入文本。</span><span class="sxs-lookup"><span data-stu-id="5272c-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="5272c-146">如果要对文本进行个性化设置，可以如步骤 6 所述插入占位符。</span><span class="sxs-lookup"><span data-stu-id="5272c-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="5272c-147">单击 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="5272c-147">Click **Close**.</span></span>

## <a name="assign-the-task"></a><span data-ttu-id="5272c-148">分配任务</span><span class="sxs-lookup"><span data-stu-id="5272c-148">Assign the task</span></span>

<span data-ttu-id="5272c-149">按照以下步骤来指定应向手动任务分配的人员。</span><span class="sxs-lookup"><span data-stu-id="5272c-149">Follow these steps to specify who the manual task should be assigned to.</span></span>

1. <span data-ttu-id="5272c-150">在左窗格中，单击 **分配**。</span><span class="sxs-lookup"><span data-stu-id="5272c-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="5272c-151">在 **分配类型** 选项卡上，选择下表中的选项之一，然后按照该选项的其他步骤转到步骤 3。</span><span class="sxs-lookup"><span data-stu-id="5272c-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="5272c-152">选项</span><span class="sxs-lookup"><span data-stu-id="5272c-152">Option</span></span></th>
    <th><span data-ttu-id="5272c-153">向其分配任务的用户</span><span class="sxs-lookup"><span data-stu-id="5272c-153">Users that the task is assigned to</span></span></th>
    <th><span data-ttu-id="5272c-154">附加步骤</span><span class="sxs-lookup"><span data-stu-id="5272c-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="5272c-155">参与者</span><span class="sxs-lookup"><span data-stu-id="5272c-155">Participant</span></span></td>
    <td><span data-ttu-id="5272c-156">分配到特定组或角色的用户</span><span class="sxs-lookup"><span data-stu-id="5272c-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5272c-157">在您选择<strong>参与者</strong>后，在选项卡<strong>基于角色</strong>上，在<strong>参与者类型</strong>列表中，选择要向其分配任务的组或角色的类型。</span><span class="sxs-lookup"><span data-stu-id="5272c-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the task to.</span></span></li>
    <li><span data-ttu-id="5272c-158">在<strong>参与者</strong>列表中，选择向其分配任务的组或角色的类型。</span><span class="sxs-lookup"><span data-stu-id="5272c-158">In the <strong>Participant</strong> list, select the group or role to assign the task to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5272c-159">层次结构</span><span class="sxs-lookup"><span data-stu-id="5272c-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="5272c-160">特定组织层次结构中的用户</span><span class="sxs-lookup"><span data-stu-id="5272c-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5272c-161">在您选择<strong>层次结构</strong>后，在选项卡<strong>层次结构选择</strong>上，在<strong>层次结构类型</strong>列表中，选择要向其分配任务的层次结构的类型。</span><span class="sxs-lookup"><span data-stu-id="5272c-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the task to.</span></span></li>
    <li><span data-ttu-id="5272c-162">系统必须从层次结构中检索一系列用户姓名。</span><span class="sxs-lookup"><span data-stu-id="5272c-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="5272c-163">这些姓名代表可向其分配任务的用户。</span><span class="sxs-lookup"><span data-stu-id="5272c-163">These names represent users that the task can be assigned to.</span></span> <span data-ttu-id="5272c-164">按照以下步骤指定系统检索的用户名范围的起点和终点：</span><span class="sxs-lookup"><span data-stu-id="5272c-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="5272c-165">若要指定起点，请在<strong>启动自</strong>列表中选择一名人员。</span><span class="sxs-lookup"><span data-stu-id="5272c-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="5272c-166">若要指定终点，请单击<strong>添加条件</strong>。</span><span class="sxs-lookup"><span data-stu-id="5272c-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="5272c-167">然后输入一个确定系统停止检索姓名的层次结构的条件。</span><span class="sxs-lookup"><span data-stu-id="5272c-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="5272c-168">在<strong>层次结构选项</strong>选项卡上，指定应向其分配任务的范围内的用户：</span><span class="sxs-lookup"><span data-stu-id="5272c-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="5272c-169"><strong>分配给所有检索到的用户</strong> – 此任务将分配给范围内的所有用户。</span><span class="sxs-lookup"><span data-stu-id="5272c-169"><strong>Assign to all users retrieved</strong> – The task is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="5272c-170"><strong>仅分配给最后检索到的用户</strong> – 此任务将分配给范围内的最后一名用户。</span><span class="sxs-lookup"><span data-stu-id="5272c-170"><strong>Assign only to last user retrieved</strong> – The task is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="5272c-171"><strong>排除满足以下条件的用户</strong> – 此任务不分配给满足特定条件的范围内的用户。</span><span class="sxs-lookup"><span data-stu-id="5272c-171"><strong>Exclude users with the following condition</strong> – The task isn't assigned to users in the range who meet a specific condition.</span></span> <span data-ttu-id="5272c-172">单击<strong>添加条件</strong>以指定条件。</span><span class="sxs-lookup"><span data-stu-id="5272c-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5272c-173">工作流用户</span><span class="sxs-lookup"><span data-stu-id="5272c-173">Workflow user</span></span></td>
    <td><span data-ttu-id="5272c-174">当前工作流中的用户</span><span class="sxs-lookup"><span data-stu-id="5272c-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="5272c-175">在您选择<strong>工作流用户</strong>后，在选项卡<strong>工作流用户</strong>上，在<strong>工作流用户</strong>列表中，选择参与工作流的用户。</span><span class="sxs-lookup"><span data-stu-id="5272c-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5272c-176">用户</span><span class="sxs-lookup"><span data-stu-id="5272c-176">User</span></span></td>
    <td><span data-ttu-id="5272c-177">特定用户</span><span class="sxs-lookup"><span data-stu-id="5272c-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5272c-178">在选择<strong>用户</strong>后，单击<strong>用户</strong>选项卡。</span><span class="sxs-lookup"><span data-stu-id="5272c-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="5272c-179"><strong>可用用户</strong>列表包含所有用户。</span><span class="sxs-lookup"><span data-stu-id="5272c-179">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="5272c-180">选择要向其分配任务的用户，然后将这些用户移动到<strong>所选用户</strong>列表。</span><span class="sxs-lookup"><span data-stu-id="5272c-180">Select the users to assign the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5272c-181">队列</span><span class="sxs-lookup"><span data-stu-id="5272c-181">Queue</span></span></td>
    <td><span data-ttu-id="5272c-182">工作项队列</span><span class="sxs-lookup"><span data-stu-id="5272c-182">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5272c-183">在选择<strong>队列</strong>后，单击<strong>基于队列</strong>选项卡。</span><span class="sxs-lookup"><span data-stu-id="5272c-183">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="5272c-184">要将任务分配到特定的队列，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="5272c-184">To assign the task to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="5272c-185">在<strong>队列类型</strong>列表中，选择<strong>工作项队列</strong>。</span><span class="sxs-lookup"><span data-stu-id="5272c-185">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="5272c-186">在<strong>队列名称</strong>列表中，选择该队列。</span><span class="sxs-lookup"><span data-stu-id="5272c-186">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="5272c-187">如果特定条件应确定将任务分配到的队列，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="5272c-187">If a specific condition should determine which queue the task is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="5272c-188">在<strong>队列类型</strong>列表中，选择<strong>条件工作项队列</strong>。</span><span class="sxs-lookup"><span data-stu-id="5272c-188">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="5272c-189">在<strong>队列名称</strong>列表中，选择<strong>条件队列</strong>。</span><span class="sxs-lookup"><span data-stu-id="5272c-189">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="5272c-190">此选项仅用于几个工作流，如案例管理。</span><span class="sxs-lookup"><span data-stu-id="5272c-190">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="5272c-191">在 **时间限制** 选项卡上，在 **持续时间** 字段中，指定指定用户必须在多长时间内完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-191">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="5272c-192">选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="5272c-192">Select one of the following options:</span></span>

    - <span data-ttu-id="5272c-193">**小时** – 输入用户必须在几小时内完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-193">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="5272c-194">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="5272c-194">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="5272c-195">**天** – 输入用户必须在几天内完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-195">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="5272c-196">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="5272c-196">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="5272c-197">**周** – 输入用户必须在几周内完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-197">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="5272c-198">**月** – 选择用户必须在哪一天和哪一周前完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-198">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="5272c-199">例如，您可能希望用户在当月第三周的周五之前完成此任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-199">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="5272c-200">**年** – 选择用户必须在哪一天、哪一周和哪一月前完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-200">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="5272c-201">例如，您可能希望用户在十二月的第三周的周五之前完成此任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-201">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

    <span data-ttu-id="5272c-202">如果用户未在分配的时间内完成任务，则任务逾期。</span><span class="sxs-lookup"><span data-stu-id="5272c-202">If the user doesn't complete the task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="5272c-203">逾期的任务可以基于您在此页面 **呈报** 区域中选择的选项呈报。</span><span class="sxs-lookup"><span data-stu-id="5272c-203">A task that is overdue can be escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-the-task-is-overdue"></a><span data-ttu-id="5272c-204">指定任务逾期时采取的行动</span><span class="sxs-lookup"><span data-stu-id="5272c-204">Specify what happens when the task is overdue</span></span>

<span data-ttu-id="5272c-205">如果用户未在分配的时间内完成手动任务，则任务逾期。</span><span class="sxs-lookup"><span data-stu-id="5272c-205">If a user doesn't complete the manual task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="5272c-206">可呈报逾期的任务，或自动将该单据分配给其他用户。</span><span class="sxs-lookup"><span data-stu-id="5272c-206">A task that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="5272c-207">如果任务逾期，请执行以下步骤进行呈报。</span><span class="sxs-lookup"><span data-stu-id="5272c-207">Follow these steps to escalate the task if it's overdue.</span></span>

1. <span data-ttu-id="5272c-208">在左窗格中，单击 **呈报**。</span><span class="sxs-lookup"><span data-stu-id="5272c-208">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="5272c-209">选择 **使用呈报路线** 复选框创建呈报路线。</span><span class="sxs-lookup"><span data-stu-id="5272c-209">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="5272c-210">系统自动将任务分配给呈报路线中列出的用户。</span><span class="sxs-lookup"><span data-stu-id="5272c-210">The system automatically assigns the task to the users who are listed in the escalation path.</span></span> <span data-ttu-id="5272c-211">例如，下表显示呈报路线。</span><span class="sxs-lookup"><span data-stu-id="5272c-211">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="5272c-212">序列</span><span class="sxs-lookup"><span data-stu-id="5272c-212">Sequence</span></span> | <span data-ttu-id="5272c-213">呈报路线</span><span class="sxs-lookup"><span data-stu-id="5272c-213">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="5272c-214">1</span><span class="sxs-lookup"><span data-stu-id="5272c-214">1</span></span>        | <span data-ttu-id="5272c-215">分配给：Donna</span><span class="sxs-lookup"><span data-stu-id="5272c-215">Assign to: Donna</span></span>     |
    | <span data-ttu-id="5272c-216">2</span><span class="sxs-lookup"><span data-stu-id="5272c-216">2</span></span>        | <span data-ttu-id="5272c-217">分配给：Erin</span><span class="sxs-lookup"><span data-stu-id="5272c-217">Assign to: Erin</span></span>      |
    | <span data-ttu-id="5272c-218">3</span><span class="sxs-lookup"><span data-stu-id="5272c-218">3</span></span>        | <span data-ttu-id="5272c-219">最后操作：拒绝</span><span class="sxs-lookup"><span data-stu-id="5272c-219">Final action: Reject</span></span> |

    <span data-ttu-id="5272c-220">在此示例中，系统将逾期任务分配给 Donna。</span><span class="sxs-lookup"><span data-stu-id="5272c-220">In this example, the system assigns the overdue task to Donna.</span></span> <span data-ttu-id="5272c-221">如果 Donna 未在分配的时间内完成任务，则系统将任务分配给 Erin。</span><span class="sxs-lookup"><span data-stu-id="5272c-221">If Donna doesn't complete the task in the allotted time, the system assigns the task to Erin.</span></span> <span data-ttu-id="5272c-222">如果 Erin 未在分配的时间内完成任务，则系统会拒绝提请处理的文档。</span><span class="sxs-lookup"><span data-stu-id="5272c-222">If Erin doesn't complete the task in the allotted time, the system rejects the document that was submitted for processing.</span></span>

3. <span data-ttu-id="5272c-223">要将用户添加到呈报路线中，单击 **添加呈报**。</span><span class="sxs-lookup"><span data-stu-id="5272c-223">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="5272c-224">在 **分配类型** 选项卡上，选择下表中的选项之一，然后按照该选项的其他步骤转到步骤 4。</span><span class="sxs-lookup"><span data-stu-id="5272c-224">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="5272c-225">选项</span><span class="sxs-lookup"><span data-stu-id="5272c-225">Option</span></span></th>
    <th><span data-ttu-id="5272c-226">任务呈报到的用户</span><span class="sxs-lookup"><span data-stu-id="5272c-226">Users that the task is escalated to</span></span></th>
    <th><span data-ttu-id="5272c-227">附加步骤</span><span class="sxs-lookup"><span data-stu-id="5272c-227">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="5272c-228">层次结构</span><span class="sxs-lookup"><span data-stu-id="5272c-228">Hierarchy</span></span></td>
    <td><span data-ttu-id="5272c-229">特定组织层次结构中的用户</span><span class="sxs-lookup"><span data-stu-id="5272c-229">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5272c-230">在您选择<strong>层次结构</strong>后，在选项卡<strong>层次结构选择</strong>上，在<strong>层次结构类型</strong>列表中，选择要向其呈报任务的层次结构的类型。</span><span class="sxs-lookup"><span data-stu-id="5272c-230">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the task to.</span></span></li>
    <li><span data-ttu-id="5272c-231">系统必须从层次结构中检索一系列用户姓名。</span><span class="sxs-lookup"><span data-stu-id="5272c-231">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="5272c-232">这些姓名代表可向其呈报任务的用户。</span><span class="sxs-lookup"><span data-stu-id="5272c-232">These names represent users that the task can be escalated to.</span></span> <span data-ttu-id="5272c-233">按照以下步骤指定系统检索的用户名范围的起点和终点：</span><span class="sxs-lookup"><span data-stu-id="5272c-233">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="5272c-234">若要指定起点，请在<strong>启动自</strong>列表中选择一名人员。</span><span class="sxs-lookup"><span data-stu-id="5272c-234">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="5272c-235">若要指定终点，请单击<strong>添加条件</strong>。</span><span class="sxs-lookup"><span data-stu-id="5272c-235">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="5272c-236">然后输入一个确定系统停止检索姓名的层次结构的条件。</span><span class="sxs-lookup"><span data-stu-id="5272c-236">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="5272c-237">在<strong>层次结构选项</strong>选项卡上，指定应向其呈报任务的范围内的用户：</span><span class="sxs-lookup"><span data-stu-id="5272c-237">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="5272c-238"><strong>分配给所有检索到的用户</strong> – 此任务将呈报给范围内的所有用户。</span><span class="sxs-lookup"><span data-stu-id="5272c-238"><strong>Assign to all users retrieved</strong> – The task is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="5272c-239"><strong>仅分配给最后检索到的用户</strong> – 此任务将呈报给范围内的最后一名用户。</span><span class="sxs-lookup"><span data-stu-id="5272c-239"><strong>Assign only to last user retrieved</strong> – The task is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="5272c-240"><strong>排除满足以下条件的用户</strong> – 此任务不呈报给满足特定条件的范围内的用户。</span><span class="sxs-lookup"><span data-stu-id="5272c-240"><strong>Exclude users with the following condition</strong> – This task isn't escalated to users in the range who meet a specific condition.</span></span> <span data-ttu-id="5272c-241">单击<strong>添加条件</strong>以指定条件。</span><span class="sxs-lookup"><span data-stu-id="5272c-241">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5272c-242">工作流用户</span><span class="sxs-lookup"><span data-stu-id="5272c-242">Workflow user</span></span></td>
    <td><span data-ttu-id="5272c-243">当前工作流中的用户</span><span class="sxs-lookup"><span data-stu-id="5272c-243">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="5272c-244">在您选择<strong>工作流用户</strong>后，在选项卡<strong>工作流用户</strong>上，在<strong>工作流用户</strong>列表中，选择参与工作流的用户。</span><span class="sxs-lookup"><span data-stu-id="5272c-244">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5272c-245">用户</span><span class="sxs-lookup"><span data-stu-id="5272c-245">User</span></span></td>
    <td><span data-ttu-id="5272c-246">特定用户</span><span class="sxs-lookup"><span data-stu-id="5272c-246">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5272c-247">在选择<strong>用户</strong>后，单击<strong>用户</strong>选项卡。</span><span class="sxs-lookup"><span data-stu-id="5272c-247">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="5272c-248"><strong>可用用户</strong>列表包含所有用户。</span><span class="sxs-lookup"><span data-stu-id="5272c-248">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="5272c-249">选择要向其呈报任务的用户，然后将这些用户移动到<strong>所选用户</strong>列表。</span><span class="sxs-lookup"><span data-stu-id="5272c-249">Select the users to escalate the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="5272c-250">在 **时间限制** 选项卡上，在 **持续时间** 字段中，指定指定用户必须在多长时间内完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-250">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="5272c-251">选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="5272c-251">Select one of the following options:</span></span>

    - <span data-ttu-id="5272c-252">**小时** – 输入用户必须在几小时内完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-252">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="5272c-253">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="5272c-253">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="5272c-254">**天** – 输入用户必须在几天内完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-254">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="5272c-255">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="5272c-255">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="5272c-256">**周** – 输入用户必须在几周内完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-256">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="5272c-257">**月** – 选择用户必须在哪一天和哪一周前完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-257">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="5272c-258">例如，您可能希望用户在当月第三周的周五之前完成此任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-258">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="5272c-259">**年** – 选择用户必须在哪一天、哪一周和哪一月前完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-259">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="5272c-260">例如，您可能希望用户在十二月的第三周的周五之前完成此任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-260">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

5. <span data-ttu-id="5272c-261">对每个应添加到呈报路线的用户重复第 3 步到第 4 步。</span><span class="sxs-lookup"><span data-stu-id="5272c-261">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="5272c-262">您可以更改用户的顺序。</span><span class="sxs-lookup"><span data-stu-id="5272c-262">You can change the order of the users.</span></span>
6. <span data-ttu-id="5272c-263">如果呈报路线中的用户未在分配的时间内完成任务，则系统对该任务采取操作。</span><span class="sxs-lookup"><span data-stu-id="5272c-263">If the users in the escalation path don't complete the task in the allotted time, the system takes action on the task.</span></span> <span data-ttu-id="5272c-264">若要指定系统执行的操作，选择 **操作** 行，然后，在 **结束操作** 选项卡上，选择一项操作。</span><span class="sxs-lookup"><span data-stu-id="5272c-264">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a><span data-ttu-id="5272c-265">指定系统何时对任务采取操作</span><span class="sxs-lookup"><span data-stu-id="5272c-265">Specify when the system automatically acts on the task</span></span>

<span data-ttu-id="5272c-266">可以配置系统在满足特定条件时对手动任务采取操作。</span><span class="sxs-lookup"><span data-stu-id="5272c-266">You can configure the system to take action on the manual task if specific conditions are met.</span></span> <span data-ttu-id="5272c-267">例如，某个任务要求支出报表部门的成员审查与支出报表一起提交的收据。</span><span class="sxs-lookup"><span data-stu-id="5272c-267">For example, a task requires that a member of the Expense reports department review the receipts that are submitted together with an expense report.</span></span> <span data-ttu-id="5272c-268">根据公司政策，此任务必须在支出报表的总金额超过 100 美元时执行。</span><span class="sxs-lookup"><span data-stu-id="5272c-268">According to company policy, this task must be performed if the total amount of the expense report is more than USD 100.</span></span> <span data-ttu-id="5272c-269">在这种情况下，您可以将系统配置为在总金额 < 100 时自动将任务标记为 **完成**。</span><span class="sxs-lookup"><span data-stu-id="5272c-269">In this scenario, you can configure the system to automatically mark the task as **Complete** when the total amount is less than 100.</span></span> <span data-ttu-id="5272c-270">按照以下步骤指定系统何时对手动任务采取操作。</span><span class="sxs-lookup"><span data-stu-id="5272c-270">Follow these steps to specify when the system takes action on the manual task.</span></span>

1. <span data-ttu-id="5272c-271">在左窗格中，单击 **自动操作**。</span><span class="sxs-lookup"><span data-stu-id="5272c-271">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="5272c-272">选中 **启用自动操作** 复选框。</span><span class="sxs-lookup"><span data-stu-id="5272c-272">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="5272c-273">单击 **添加条件**。</span><span class="sxs-lookup"><span data-stu-id="5272c-273">Click **Add condition**.</span></span>
4. <span data-ttu-id="5272c-274">输入条件。</span><span class="sxs-lookup"><span data-stu-id="5272c-274">Enter a condition.</span></span>
5. <span data-ttu-id="5272c-275">输入需要的任何其他条件。</span><span class="sxs-lookup"><span data-stu-id="5272c-275">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="5272c-276">要验证输入的条件是否正确配置，请按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="5272c-276">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="5272c-277">单击 **测试**。</span><span class="sxs-lookup"><span data-stu-id="5272c-277">Click **Test**.</span></span>
    2. <span data-ttu-id="5272c-278">在 **测试工作流条件** 页面，在 **验证条件** 区域，选择一条记录。</span><span class="sxs-lookup"><span data-stu-id="5272c-278">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="5272c-279">单击 **测试**。</span><span class="sxs-lookup"><span data-stu-id="5272c-279">Click **Test**.</span></span> <span data-ttu-id="5272c-280">系统对该记录进行评估，判断其是否符合您定义的条件。</span><span class="sxs-lookup"><span data-stu-id="5272c-280">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="5272c-281">单击 **确定** 或 **取消** 返回到 **属性** 页面。</span><span class="sxs-lookup"><span data-stu-id="5272c-281">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

7. <span data-ttu-id="5272c-282">在 **自动完成操作** 列表中选择系统应对任务采取的操作。</span><span class="sxs-lookup"><span data-stu-id="5272c-282">In the **Auto complete action** list, select the action that the system should take on the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="5272c-283">指定发送通知的时间</span><span class="sxs-lookup"><span data-stu-id="5272c-283">Specify when notifications are sent</span></span>

<span data-ttu-id="5272c-284">您可以在委托、呈报、完成、拒绝或更改此手动任务后向相关人员发送通知。</span><span class="sxs-lookup"><span data-stu-id="5272c-284">You can send notifications to people when a manual task has been delegated, escalated, completed, or rejected, or when a change has been requested.</span></span> <span data-ttu-id="5272c-285">按照以下步骤指定发送通知的时间以通知发送给哪些人员。</span><span class="sxs-lookup"><span data-stu-id="5272c-285">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="5272c-286">在左窗格中，单击 **通知**。</span><span class="sxs-lookup"><span data-stu-id="5272c-286">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="5272c-287">选中应针对其发送通知的事件旁边的复选框：</span><span class="sxs-lookup"><span data-stu-id="5272c-287">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="5272c-288">**委托** – 将任务分配给其他用户。</span><span class="sxs-lookup"><span data-stu-id="5272c-288">**Delegate** – The task has been assigned to another user.</span></span>
    - <span data-ttu-id="5272c-289">**呈报** – 所分配用户未在分配的时间内完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-289">**Escalate** – The assigned user hasn't completed the task in the allotted time.</span></span>
    - <span data-ttu-id="5272c-290">**完成** – 所分配用户完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-290">**Complete** – The assigned user has completed the task.</span></span>
    - <span data-ttu-id="5272c-291">**拒绝** – 所分配用户拒绝提交的文档。</span><span class="sxs-lookup"><span data-stu-id="5272c-291">**Reject** – The assigned user has rejected the document that was submitted.</span></span>
    - <span data-ttu-id="5272c-292">**请求更改** – 所分配用户请求对提交的文档进行更改。</span><span class="sxs-lookup"><span data-stu-id="5272c-292">**Request change** – The assigned user has requested a change to the document that was submitted.</span></span>

3. <span data-ttu-id="5272c-293">为您在第 2 步中选择的事件选择行。</span><span class="sxs-lookup"><span data-stu-id="5272c-293">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="5272c-294">在 **通知文本** 选项卡上，在文本框中输入通知的文本。</span><span class="sxs-lookup"><span data-stu-id="5272c-294">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="5272c-295">要对通知进行个性化设置，可以插入占位符。</span><span class="sxs-lookup"><span data-stu-id="5272c-295">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="5272c-296">向用户显示通知时，占位符由适当的信息代替。</span><span class="sxs-lookup"><span data-stu-id="5272c-296">Placeholders are replaced with appropriate information when the notification is shown to users.</span></span> <span data-ttu-id="5272c-297">按照以下步骤插入占位符：</span><span class="sxs-lookup"><span data-stu-id="5272c-297">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="5272c-298">在文本框中，单击应该出现占位符的位置。</span><span class="sxs-lookup"><span data-stu-id="5272c-298">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="5272c-299">单击 **插入占位符**。</span><span class="sxs-lookup"><span data-stu-id="5272c-299">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="5272c-300">在出现的列表中，选择要插入的占位符。</span><span class="sxs-lookup"><span data-stu-id="5272c-300">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="5272c-301">单击 **插入**。</span><span class="sxs-lookup"><span data-stu-id="5272c-301">Click **Insert**.</span></span>

6. <span data-ttu-id="5272c-302">若要添加通知的翻译，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="5272c-302">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="5272c-303">单击 **翻译**。</span><span class="sxs-lookup"><span data-stu-id="5272c-303">Click **Translations**.</span></span>
    2. <span data-ttu-id="5272c-304">在出现的页面上，单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5272c-304">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="5272c-305">在出现的列表中，选择您输入文本使用的语言。</span><span class="sxs-lookup"><span data-stu-id="5272c-305">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="5272c-306">在 **已翻译的文本** 字段中，输入文本。</span><span class="sxs-lookup"><span data-stu-id="5272c-306">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="5272c-307">如果要对文本进行个性化设置，可以如步骤 5 所述插入占位符。</span><span class="sxs-lookup"><span data-stu-id="5272c-307">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="5272c-308">单击 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="5272c-308">Click **Close**.</span></span>

7. <span data-ttu-id="5272c-309">在 **接收人** 选项卡上，指定向谁发送通知。</span><span class="sxs-lookup"><span data-stu-id="5272c-309">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="5272c-310">选择下表中的选项之一，然后按照该选项的其他步骤转到第 8 步。</span><span class="sxs-lookup"><span data-stu-id="5272c-310">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="5272c-311">选项</span><span class="sxs-lookup"><span data-stu-id="5272c-311">Option</span></span></th>
    <th><span data-ttu-id="5272c-312">通知收件人。</span><span class="sxs-lookup"><span data-stu-id="5272c-312">Notification recipients</span></span></th>
    <th><span data-ttu-id="5272c-313">附加步骤</span><span class="sxs-lookup"><span data-stu-id="5272c-313">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="5272c-314">参与者</span><span class="sxs-lookup"><span data-stu-id="5272c-314">Participant</span></span></td>
    <td><span data-ttu-id="5272c-315">分配到特定组或角色的用户</span><span class="sxs-lookup"><span data-stu-id="5272c-315">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5272c-316">在您选择<strong>参与者</strong>后，在选项卡<strong>基于角色</strong>上，在<strong>参与者类型</strong>列表中，选择要向其发送通知的组或角色的类型。</span><span class="sxs-lookup"><span data-stu-id="5272c-316">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="5272c-317">在<strong>参与者</strong>列表中，选择向其发送通知的组或角色。</span><span class="sxs-lookup"><span data-stu-id="5272c-317">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5272c-318">工作流用户</span><span class="sxs-lookup"><span data-stu-id="5272c-318">Workflow user</span></span></td>
    <td><span data-ttu-id="5272c-319">当前工作流中的用户</span><span class="sxs-lookup"><span data-stu-id="5272c-319">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="5272c-320">在您选择<strong>工作流用户</strong>后，在选项卡<strong>工作流用户</strong>上，在<strong>工作流用户</strong>列表中，选择参与工作流的用户。</span><span class="sxs-lookup"><span data-stu-id="5272c-320">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5272c-321">用户</span><span class="sxs-lookup"><span data-stu-id="5272c-321">User</span></span></td>
    <td><span data-ttu-id="5272c-322">特定用户</span><span class="sxs-lookup"><span data-stu-id="5272c-322">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5272c-323">在选择<strong>用户</strong>后，单击<strong>用户</strong>选项卡。</span><span class="sxs-lookup"><span data-stu-id="5272c-323">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="5272c-324"><strong>可用用户</strong>列表包含所有用户。</span><span class="sxs-lookup"><span data-stu-id="5272c-324">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="5272c-325">选择向其发送通知的用户，然后将这些用户移动到<strong>所选用户</strong>列表中。</span><span class="sxs-lookup"><span data-stu-id="5272c-325">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="5272c-326">对您在第 2 步中选择的每个事件重复 第 3 步到第 7 步。</span><span class="sxs-lookup"><span data-stu-id="5272c-326">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="5272c-327">设置时间限制</span><span class="sxs-lookup"><span data-stu-id="5272c-327">Set a time limit</span></span>

<span data-ttu-id="5272c-328">如果必须在特定时间内完成手动任务，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="5272c-328">Follow these steps if the manual task must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="5272c-329">您在此过程中选择的选项将覆盖您在页面的 **分配** 和 **呈报** 区域选择的选项。</span><span class="sxs-lookup"><span data-stu-id="5272c-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="5272c-330">在左侧窗格中，单击 **高级设置**。</span><span class="sxs-lookup"><span data-stu-id="5272c-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="5272c-331">选中 **为工作流元素设置时间限制** 复选框。</span><span class="sxs-lookup"><span data-stu-id="5272c-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="5272c-332">在 **持续时间** 字段中，指定必须在何时完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-332">In the **Duration** field, specify when the task must be completed.</span></span> <span data-ttu-id="5272c-333">选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="5272c-333">Select one of the following options:</span></span>

    - <span data-ttu-id="5272c-334">**小时** – 输入必须在几小时内完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-334">**Hours** – Enter the number of hours that the task must be completed in.</span></span> <span data-ttu-id="5272c-335">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="5272c-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="5272c-336">**天** – 输入必须在几天内完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-336">**Days** – Enter the number of days that the task must be completed in.</span></span> <span data-ttu-id="5272c-337">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="5272c-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="5272c-338">**周** – 输入必须在几周内完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-338">**Weeks** – Enter the number of weeks that the task must be completed in.</span></span>
    - <span data-ttu-id="5272c-339">**月** – 选择必须在哪一天和哪一周前完成任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-339">**Months** – Select the day and week that the task must be completed by.</span></span> <span data-ttu-id="5272c-340">例如，您可能希望任务在当月第三周的周五之前完成。</span><span class="sxs-lookup"><span data-stu-id="5272c-340">For example, you might want the task to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="5272c-341">**年** – 选择任务必须在哪一天、哪一周和哪一月前完成。</span><span class="sxs-lookup"><span data-stu-id="5272c-341">**Years** – Select the day, week, and month that the task must be completed by.</span></span> <span data-ttu-id="5272c-342">例如，您可能希望任务在十二月的第三周的周五之前完成。</span><span class="sxs-lookup"><span data-stu-id="5272c-342">For example, you might want the task to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="5272c-343">如果超出时间限制，系统将对任务采取操作。</span><span class="sxs-lookup"><span data-stu-id="5272c-343">If the time limit is exceeded, the system takes action on the task.</span></span> <span data-ttu-id="5272c-344">在 **操作** 列表中选择系统应采取的操作。</span><span class="sxs-lookup"><span data-stu-id="5272c-344">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="5272c-345">指定用户可以采取的操作</span><span class="sxs-lookup"><span data-stu-id="5272c-345">Specify which actions are available to the user</span></span>

<span data-ttu-id="5272c-346">将手动任务分配给某一用户后，该用户必须对任务采取操作。</span><span class="sxs-lookup"><span data-stu-id="5272c-346">When the manual task is assigned to a user, the user must take action on the task.</span></span> <span data-ttu-id="5272c-347">按照以下步骤指定用户可对任务采取操作。</span><span class="sxs-lookup"><span data-stu-id="5272c-347">Follow these steps to specify which actions the user can take on the task.</span></span>

> [!NOTE]
> <span data-ttu-id="5272c-348">可用操作将随任务的设计而变化。</span><span class="sxs-lookup"><span data-stu-id="5272c-348">The actions that are available vary, depending on the design of the task.</span></span>

1. <span data-ttu-id="5272c-349">在左侧窗格中，单击 **高级设置**。</span><span class="sxs-lookup"><span data-stu-id="5272c-349">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="5272c-350">如果用户应该能够将任务标记为 **完成**，则选中 **完成** 复选框。</span><span class="sxs-lookup"><span data-stu-id="5272c-350">Select the **Complete** check box if the user should be able to mark the task as **Complete**.</span></span>
3. <span data-ttu-id="5272c-351">如果用户应该能够提交的文档，则选中 **拒绝** 复选框。</span><span class="sxs-lookup"><span data-stu-id="5272c-351">Select the **Reject** check box if the user should be able to reject the document that was submitted.</span></span>
4. <span data-ttu-id="5272c-352">如果用户应该能够对所提交的文档请求更改，则选中 **请求更改** 复选框。</span><span class="sxs-lookup"><span data-stu-id="5272c-352">Select the **Request change** check box if the user should be able to request changes to the document that was submitted.</span></span>
5. <span data-ttu-id="5272c-353">如果用户应该能够将此任务分配给其他用户，则请选中 **委托** 复选框。</span><span class="sxs-lookup"><span data-stu-id="5272c-353">Select the **Delegate** check box if the user should be able to assign the task to another user.</span></span>
6. <span data-ttu-id="5272c-354">如果用户应该能够将任务分配给工作项队列中的其他用户，则选中 **重新分配** 复选框。</span><span class="sxs-lookup"><span data-stu-id="5272c-354">Select the **Reassign** check box if the user should be able to reassign the task to another user in the work item queue.</span></span>
7. <span data-ttu-id="5272c-355">如果用户应该能够将任务分配给工作项队列，则选中 **下达** 复选框。</span><span class="sxs-lookup"><span data-stu-id="5272c-355">Select the **Release** check box if the user should be able to reassign the task to the work item queue.</span></span> <span data-ttu-id="5272c-356">其他用户可以完成该任务。</span><span class="sxs-lookup"><span data-stu-id="5272c-356">Another user can then complete the task.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
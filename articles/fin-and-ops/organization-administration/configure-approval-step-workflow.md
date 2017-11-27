---
title: "配置工作流中的审核步骤"
description: "本主题说明如何配置审核步骤的属性。"
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d2fc157b54401463bbabf1e3f6d5dddc6bda9631
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="configure-an-approval-step-in-a-workflow"></a><span data-ttu-id="6753a-103">配置工作流中的审核步骤</span><span class="sxs-lookup"><span data-stu-id="6753a-103">Configure an approval step in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6753a-104">本主题说明如何配置审核步骤的属性。</span><span class="sxs-lookup"><span data-stu-id="6753a-104">This topic explains how to configure the properties of an approval step.</span></span>

<span data-ttu-id="6753a-105">要配置审核步骤，在“工作流”编辑器中，右键单击审核步骤，然后单击**属性**打开**属性**页面。</span><span class="sxs-lookup"><span data-stu-id="6753a-105">To configure an approval step in the workflow editor, right-click the approval step, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="6753a-106">然后使用以下过程配置审核步骤的属性。</span><span class="sxs-lookup"><span data-stu-id="6753a-106">Then use the following procedures to configure the properties of the approval step.</span></span>

## <a name="name-the-step"></a><span data-ttu-id="6753a-107">为步骤命名</span><span class="sxs-lookup"><span data-stu-id="6753a-107">Name the step</span></span>
<span data-ttu-id="6753a-108">按照以下为审核步骤输入名称。</span><span class="sxs-lookup"><span data-stu-id="6753a-108">Follow these steps to enter a name for the approval step.</span></span>

1.  <span data-ttu-id="6753a-109">在左侧窗格中，单击**基本设置**。</span><span class="sxs-lookup"><span data-stu-id="6753a-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="6753a-110">在**名称**字段中，为审核步骤输入唯一名称。</span><span class="sxs-lookup"><span data-stu-id="6753a-110">In the **Name** field, enter a unique name for the approval step.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="6753a-111">输入主题行和说明</span><span class="sxs-lookup"><span data-stu-id="6753a-111">Enter a subject line and instructions</span></span>
<span data-ttu-id="6753a-112">必须为分配到审核步骤的用户提供主题行和说明。</span><span class="sxs-lookup"><span data-stu-id="6753a-112">You must provide a subject line and instructions to users who are assigned to the approval step.</span></span> <span data-ttu-id="6753a-113">例如，如果您在为采购申请配置审核步骤，则分配到该步骤的用户在**采购申请**页面看到主题行和说明。</span><span class="sxs-lookup"><span data-stu-id="6753a-113">For example, if you're configuring an approval step for purchase requisitions, the user who is assigned to the step sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="6753a-114">主题行显示在页面的消息栏中。</span><span class="sxs-lookup"><span data-stu-id="6753a-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="6753a-115">然后用户可单击消息栏中的图标查看说明。</span><span class="sxs-lookup"><span data-stu-id="6753a-115">The user can then click the icon in the message bar to see the instructions.</span></span> <span data-ttu-id="6753a-116">按照以下步骤输入主题行和说明。</span><span class="sxs-lookup"><span data-stu-id="6753a-116">Follow these steps to enter a subject line and instructions.</span></span>

1.  <span data-ttu-id="6753a-117">在左侧窗格中，单击**基本设置**。</span><span class="sxs-lookup"><span data-stu-id="6753a-117">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="6753a-118">在**工作项主题**字段中，输入主题行。</span><span class="sxs-lookup"><span data-stu-id="6753a-118">In the **Work item subject** field, enter the subject line.</span></span>
3.  <span data-ttu-id="6753a-119">要个性化主题行，可以插入占位符。</span><span class="sxs-lookup"><span data-stu-id="6753a-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="6753a-120">向用户显示主题行时，占位符由适当的数据代替。</span><span class="sxs-lookup"><span data-stu-id="6753a-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="6753a-121">按照以下步骤插入占位符：</span><span class="sxs-lookup"><span data-stu-id="6753a-121">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="6753a-122">在文本框中，单击应该出现占位符的位置。</span><span class="sxs-lookup"><span data-stu-id="6753a-122">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="6753a-123">单击**插入占位符**。</span><span class="sxs-lookup"><span data-stu-id="6753a-123">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="6753a-124">在出现的列表中，选择要插入的占位符。</span><span class="sxs-lookup"><span data-stu-id="6753a-124">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="6753a-125">单击“**插入**”。</span><span class="sxs-lookup"><span data-stu-id="6753a-125">Click **Insert**.</span></span>

4.  <span data-ttu-id="6753a-126">若要添加主题行的翻译，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="6753a-126">To add translations of the subject line, follow these steps:</span></span>
    1.  <span data-ttu-id="6753a-127">单击**翻译**。</span><span class="sxs-lookup"><span data-stu-id="6753a-127">Click **Translations**.</span></span>
    2.  <span data-ttu-id="6753a-128">在出现的页面上，单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="6753a-128">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="6753a-129">在出现的列表中，选择您输入文本使用的语言。</span><span class="sxs-lookup"><span data-stu-id="6753a-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="6753a-130">在**已翻译的文本**字段中，输入文本。</span><span class="sxs-lookup"><span data-stu-id="6753a-130">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="6753a-131">如果要对文本进行个性化设置，可以如步骤 3 所述插入占位符。</span><span class="sxs-lookup"><span data-stu-id="6753a-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6.  <span data-ttu-id="6753a-132">单击**“关闭”**。</span><span class="sxs-lookup"><span data-stu-id="6753a-132">Click **Close**.</span></span>

5.  <span data-ttu-id="6753a-133">在**工作项说明**字段中，输入说明。</span><span class="sxs-lookup"><span data-stu-id="6753a-133">In the **Work item instructions** field, enter the instructions.</span></span>
6.  <span data-ttu-id="6753a-134">要对说明进行个性化设置，可以插入占位符。</span><span class="sxs-lookup"><span data-stu-id="6753a-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="6753a-135">向用户显示说明时，占位符由适当的数据代替。</span><span class="sxs-lookup"><span data-stu-id="6753a-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="6753a-136">按照以下步骤插入占位符：</span><span class="sxs-lookup"><span data-stu-id="6753a-136">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="6753a-137">在文本框中，单击应该出现占位符的位置。</span><span class="sxs-lookup"><span data-stu-id="6753a-137">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="6753a-138">单击**插入占位符**。</span><span class="sxs-lookup"><span data-stu-id="6753a-138">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="6753a-139">在出现的列表中，选择要插入的占位符。</span><span class="sxs-lookup"><span data-stu-id="6753a-139">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="6753a-140">单击“**插入**”。</span><span class="sxs-lookup"><span data-stu-id="6753a-140">Click **Insert**.</span></span>

7.  <span data-ttu-id="6753a-141">若要添加说明的翻译，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="6753a-141">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="6753a-142">单击**翻译**。</span><span class="sxs-lookup"><span data-stu-id="6753a-142">Click **Translations**.</span></span>
    2.  <span data-ttu-id="6753a-143">在出现的页面上，单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="6753a-143">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="6753a-144">在出现的列表中，选择您输入文本使用的语言。</span><span class="sxs-lookup"><span data-stu-id="6753a-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="6753a-145">在**已翻译的文本**字段中，输入文本。</span><span class="sxs-lookup"><span data-stu-id="6753a-145">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="6753a-146">如果要对文本进行个性化设置，可以如步骤 6 所述插入占位符。</span><span class="sxs-lookup"><span data-stu-id="6753a-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6.  <span data-ttu-id="6753a-147">单击**“关闭”**。</span><span class="sxs-lookup"><span data-stu-id="6753a-147">Click **Close**.</span></span>

## <a name="assign-the-approval-step"></a><span data-ttu-id="6753a-148">分配审核步骤</span><span class="sxs-lookup"><span data-stu-id="6753a-148">Assign the approval step</span></span>
<span data-ttu-id="6753a-149">按照以下步骤来指定应向审核步骤分配的人员。</span><span class="sxs-lookup"><span data-stu-id="6753a-149">Follow these steps to specify who the approval step should be assigned to.</span></span>

1.  <span data-ttu-id="6753a-150">在左窗格中，单击**分配**。</span><span class="sxs-lookup"><span data-stu-id="6753a-150">In the left pane, click **Assignment**.</span></span>
2.  <span data-ttu-id="6753a-151">在**分配类型**选项卡上，选择下表中的选项之一，然后按照该选项的其他步骤转到步骤 3。</span><span class="sxs-lookup"><span data-stu-id="6753a-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="6753a-152">选项</span><span class="sxs-lookup"><span data-stu-id="6753a-152">Option</span></span></th>
    <th><span data-ttu-id="6753a-153">被分配审核步骤的用户</span><span class="sxs-lookup"><span data-stu-id="6753a-153">Users that the approval step is assigned to</span></span></th>
    <th><span data-ttu-id="6753a-154">附加步骤</span><span class="sxs-lookup"><span data-stu-id="6753a-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="6753a-155">参与者</span><span class="sxs-lookup"><span data-stu-id="6753a-155">Participant</span></span></td>
    <td><span data-ttu-id="6753a-156">分配到特定组或角色的用户</span><span class="sxs-lookup"><span data-stu-id="6753a-156">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6753a-157">在您选择<strong>参与者</strong>后，在选项卡<strong>基于角色</strong>上，在<strong>参与者类型</strong>列表中，选择要被分配步骤的组或角色的类型。</span><span class="sxs-lookup"><span data-stu-id="6753a-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the step to.</span></span></li>
    <li><span data-ttu-id="6753a-158">在<strong>参与者</strong>列表中，选择向其分配步骤的组或角色的类型。</span><span class="sxs-lookup"><span data-stu-id="6753a-158">In the <strong>Participant</strong> list, select the group or role to assign the step to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="6753a-159">层次结构</span><span class="sxs-lookup"><span data-stu-id="6753a-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="6753a-160">特定组织层次结构中的用户</span><span class="sxs-lookup"><span data-stu-id="6753a-160">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6753a-161">在您选择<strong>层次结构</strong>后，在选项卡<strong>层次结构选择</strong>上，在<strong>层次结构类型</strong>列表中，选择要向其分配步骤的层次结构的类型。</span><span class="sxs-lookup"><span data-stu-id="6753a-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the step to.</span></span></li>
    <li><span data-ttu-id="6753a-162">系统必须从层次结构中检索一系列用户姓名。</span><span class="sxs-lookup"><span data-stu-id="6753a-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="6753a-163">这些姓名代表可向其分配步骤的用户。</span><span class="sxs-lookup"><span data-stu-id="6753a-163">These names represent users that the step can be assigned to.</span></span> <span data-ttu-id="6753a-164">按照以下步骤指定系统检索的用户名范围的起点和终点：</span><span class="sxs-lookup"><span data-stu-id="6753a-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="6753a-165">若要指定起点，请在<strong>启动自</strong>列表中选择一名人员。</span><span class="sxs-lookup"><span data-stu-id="6753a-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="6753a-166">若要指定终点，请单击“<strong>添加条件</strong>”。</span><span class="sxs-lookup"><span data-stu-id="6753a-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="6753a-167">然后输入一个确定系统停止检索姓名的层次结构的条件。</span><span class="sxs-lookup"><span data-stu-id="6753a-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="6753a-168">在<strong>层次结构选项</strong>选项卡上，指定应向其分配步骤的范围内的用户：</span><span class="sxs-lookup"><span data-stu-id="6753a-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the step should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="6753a-169"><strong>分配给所有检索到的用户</strong> – 此步骤将分配给范围内的所有用户。</span><span class="sxs-lookup"><span data-stu-id="6753a-169"><strong>Assign to all users retrieved</strong> – The step is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="6753a-170"><strong>仅分配给最后检索到的用户</strong> – 此步骤将分配给范围内的最后一名用户。</span><span class="sxs-lookup"><span data-stu-id="6753a-170"><strong>Assign only to last user retrieved</strong> – The step is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="6753a-171"><strong>排除满足以下条件的用户</strong> – 此步骤不分配给满足特定条件的范围内的所有用户。</span><span class="sxs-lookup"><span data-stu-id="6753a-171"><strong>Exclude users with the following condition</strong> – The step isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="6753a-172">单击“<strong>添加条件</strong>”以指定条件。</span><span class="sxs-lookup"><span data-stu-id="6753a-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="6753a-173">工作流用户</span><span class="sxs-lookup"><span data-stu-id="6753a-173">Workflow user</span></span></td>
    <td><span data-ttu-id="6753a-174">当前工作流中的用户</span><span class="sxs-lookup"><span data-stu-id="6753a-174">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="6753a-175">在您选择<strong>工作流用户</strong>后，在选项卡<strong>工作流用户</strong>上，在<strong>工作流用户</strong>列表中，选择参与工作流的用户。</span><span class="sxs-lookup"><span data-stu-id="6753a-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="6753a-176">用户</span><span class="sxs-lookup"><span data-stu-id="6753a-176">User</span></span></td>
    <td><span data-ttu-id="6753a-177">特定的 Microsoft Dynamics 365 for Finance and Operations 用户</span><span class="sxs-lookup"><span data-stu-id="6753a-177">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6753a-178">在选择<strong>用户</strong>后，单击<strong>用户</strong>选项卡。</span><span class="sxs-lookup"><span data-stu-id="6753a-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="6753a-179"><strong>可用用户</strong>列表包含所有 Finance and Operations 用户。</span><span class="sxs-lookup"><span data-stu-id="6753a-179">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="6753a-180">选择要向其分配步骤的用户，然后将这些用户移动到<strong>所选用户</strong>列表。</span><span class="sxs-lookup"><span data-stu-id="6753a-180">Select the users to assign the step to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

3.  <span data-ttu-id="6753a-181">在**时间限制**选项卡上，在**持续时间**字段中，指定指定用户必须在多长时间内对到达审核步骤的文档采取行动或进行响应。</span><span class="sxs-lookup"><span data-stu-id="6753a-181">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents that reach the approval step.</span></span> <span data-ttu-id="6753a-182">选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="6753a-182">Select one of the following options:</span></span>
    -   <span data-ttu-id="6753a-183">**小时** – 输入用户必须响应的小时数。</span><span class="sxs-lookup"><span data-stu-id="6753a-183">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="6753a-184">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="6753a-184">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="6753a-185">**天** – 输入用户必须响应的天数。</span><span class="sxs-lookup"><span data-stu-id="6753a-185">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="6753a-186">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="6753a-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="6753a-187">**周** – 输入用户必须响应的周数。</span><span class="sxs-lookup"><span data-stu-id="6753a-187">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    -   <span data-ttu-id="6753a-188">**月** – 选择用户必须在哪一天和哪一周之前响应。</span><span class="sxs-lookup"><span data-stu-id="6753a-188">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="6753a-189">例如，您可能希望用户在该月的第三周的星期五之前进行响应。</span><span class="sxs-lookup"><span data-stu-id="6753a-189">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="6753a-190">**年** – 选择用户必须在哪一天、哪一周和哪一月之前响应。</span><span class="sxs-lookup"><span data-stu-id="6753a-190">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="6753a-191">例如，您可能希望用户在十二月的第三周的星期五之前进行响应。</span><span class="sxs-lookup"><span data-stu-id="6753a-191">For example, you might want the user to respond by Friday of the third week of December.</span></span>

    <span data-ttu-id="6753a-192">如果用户未在分配的时间内对文档进行操作，则该文档逾期。</span><span class="sxs-lookup"><span data-stu-id="6753a-192">If the user doesn't take action on the document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="6753a-193">逾期的文件基于您在此页面**呈报**区域中选择的选项呈报。</span><span class="sxs-lookup"><span data-stu-id="6753a-193">A document that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>
4.  <span data-ttu-id="6753a-194">如果您将审核步骤分配给多个用户或用户组，在**完成策略**选项卡上选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="6753a-194">If you assigned the approval step to multiple users or a group of users, on the **Completion policy** tab, select one of the following options:</span></span>
    -   <span data-ttu-id="6753a-195">“**单个审核人**”– 应用到文档的操作将由第一个响应的人员决定。</span><span class="sxs-lookup"><span data-stu-id="6753a-195">**Single approver** – The action that is applied to the document is determined by the first person who responds.</span></span> <span data-ttu-id="6753a-196">例如，Sam 提交了一份 15,000 美元的支出报表。</span><span class="sxs-lookup"><span data-stu-id="6753a-196">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="6753a-197">该支出报表当前分配给 Sue、Jo 和 Bill。</span><span class="sxs-lookup"><span data-stu-id="6753a-197">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="6753a-198">如果 Sue 是第一个响应该文档的人员，则她采取的操作将应用到该文档。</span><span class="sxs-lookup"><span data-stu-id="6753a-198">If Sue is the first person who responds to the document, the action that she takes is applied to the document.</span></span> <span data-ttu-id="6753a-199">如果素心拒绝了单据，该单据将被拒绝并发还建豪。</span><span class="sxs-lookup"><span data-stu-id="6753a-199">If Sue rejects the document, it's rejected and sent back to Sam.</span></span> <span data-ttu-id="6753a-200">如果 Sue 批准了文档，该文档将发送给 Ann 进行审核。</span><span class="sxs-lookup"><span data-stu-id="6753a-200">If Sue approves the document, it's sent to Ann for approval.</span></span> 
    
    ![具有审核流程的工作流](./media/workflow_multipleusersinstep.gif)
    
    -   <span data-ttu-id="6753a-202">“**大多数审核人**”– 应用到文档的操作将由大多数响应的人员决定。</span><span class="sxs-lookup"><span data-stu-id="6753a-202">**Majority of approvers** – The action that is applied to the document is determined when most of the approvers respond.</span></span> <span data-ttu-id="6753a-203">例如，Sam 提交了一份 15,000 美元的支出报表。</span><span class="sxs-lookup"><span data-stu-id="6753a-203">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="6753a-204">该支出报表当前分配给 Sue、Jo 和 Bill。</span><span class="sxs-lookup"><span data-stu-id="6753a-204">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="6753a-205">如果前两个响应的审核人是 Sue 和 Jo，则他们采取的操作将应用到该文档。</span><span class="sxs-lookup"><span data-stu-id="6753a-205">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document.</span></span>
        -   <span data-ttu-id="6753a-206">如果 Sue 批准了文档，但 Jo 拒绝了文档，则该文档将被拒绝并发还给 Sam。</span><span class="sxs-lookup"><span data-stu-id="6753a-206">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        -   <span data-ttu-id="6753a-207">如果 Sue 和 Jo 都批准了文档，该文档将发送给 Ann 进行审核。</span><span class="sxs-lookup"><span data-stu-id="6753a-207">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>
    -   <span data-ttu-id="6753a-208">**审核人的百分比** – 应用到文档的操作将由特定百分比的响应审核人决定。</span><span class="sxs-lookup"><span data-stu-id="6753a-208">**Percentage of approvers** – The action that is applied to the document is determined when a specific percentage of the approvers respond.</span></span> <span data-ttu-id="6753a-209">例如，Sam 提交了一份 15,000 美元的支出报表。</span><span class="sxs-lookup"><span data-stu-id="6753a-209">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="6753a-210">支出报表当前分配给 Sue、Jo 和 Bill，并且，您输入 **50** 作为百分比。</span><span class="sxs-lookup"><span data-stu-id="6753a-210">The expense report is currently assigned to Sue, Jo, and Bill, and you entered **50** as the percentage.</span></span> <span data-ttu-id="6753a-211">如果 Sue 和 Jo 是前两个响应的审核人，则他们执行的操作应用到文档，因为它们满足 50% 的审核人的要求。</span><span class="sxs-lookup"><span data-stu-id="6753a-211">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document, because they meet the requirement for 50 percent of approvers.</span></span>
        -   <span data-ttu-id="6753a-212">如果 Sue 批准了文档，但 Jo 拒绝了文档，则该文档将被拒绝并发还给 Sam。</span><span class="sxs-lookup"><span data-stu-id="6753a-212">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        -   <span data-ttu-id="6753a-213">如果 Sue 和 Jo 都批准了文档，该文档将发送给 Ann 进行审核。</span><span class="sxs-lookup"><span data-stu-id="6753a-213">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>
    -   <span data-ttu-id="6753a-214">“**所有审核人**”– 所有审核人都必须审核该文档。</span><span class="sxs-lookup"><span data-stu-id="6753a-214">**All approvers** – All the approvers must approve the document.</span></span> <span data-ttu-id="6753a-215">否则，工作流不能继续。</span><span class="sxs-lookup"><span data-stu-id="6753a-215">Otherwise, the workflow can't continue.</span></span> <span data-ttu-id="6753a-216">例如，Sam 提交了一份 15,000 美元的支出报表。</span><span class="sxs-lookup"><span data-stu-id="6753a-216">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="6753a-217">该支出报表当前分配给 Sue、Jo 和 Bill。</span><span class="sxs-lookup"><span data-stu-id="6753a-217">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="6753a-218">如果 Sue 和 Jo 批准了文档，而 Bill 拒绝了文档，该文档将被拒绝并发还 Sam。</span><span class="sxs-lookup"><span data-stu-id="6753a-218">If Sue and Joe approve the document, but Bill rejects it, the document is rejected and sent back to Sam.</span></span> <span data-ttu-id="6753a-219">如果Sue、Jo 和 Bill 都批准了文档，该文档将发送给 Ann 进行审核。</span><span class="sxs-lookup"><span data-stu-id="6753a-219">If Sue, Jo, and Bill all approve the document, it's sent to Ann for approval.</span></span>

## <a name="specify-when-the-approval-step-is-required"></a><span data-ttu-id="6753a-220">指定何时需要审核步骤</span><span class="sxs-lookup"><span data-stu-id="6753a-220">Specify when the approval step is required</span></span>
<span data-ttu-id="6753a-221">可指定何时需要审核步骤。</span><span class="sxs-lookup"><span data-stu-id="6753a-221">You can specify when the approval step is required.</span></span> <span data-ttu-id="6753a-222">可能始终需要审核步骤，或者可能仅在满足特定条件是需要。</span><span class="sxs-lookup"><span data-stu-id="6753a-222">The approval step can always be required, or it can be required only if specific conditions are met.</span></span>

### <a name="the-approval-step-is-always-required"></a><span data-ttu-id="6753a-223">始终需要审核步骤</span><span class="sxs-lookup"><span data-stu-id="6753a-223">The approval step is always required</span></span>

<span data-ttu-id="6753a-224">如果始终需要审核，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6753a-224">Follow these steps if the approval step is always required.</span></span>

1.  <span data-ttu-id="6753a-225">在左窗格中，单击**条件**。</span><span class="sxs-lookup"><span data-stu-id="6753a-225">In the left pane, click **Condition**.</span></span>
2.  <span data-ttu-id="6753a-226">选择“**始终执行此步骤**”选项。</span><span class="sxs-lookup"><span data-stu-id="6753a-226">Select the **Always run this step** option.</span></span>

### <a name="the-approval-step-is-required-in-specific-conditions"></a><span data-ttu-id="6753a-227">在特定条件下需要审核步骤</span><span class="sxs-lookup"><span data-stu-id="6753a-227">The approval step is required in specific conditions</span></span>

<span data-ttu-id="6753a-228">可能仅在满足特定条件时才需要您正在配置的审核步骤。</span><span class="sxs-lookup"><span data-stu-id="6753a-228">The approval step that you're configuring might be required only if specific conditions are met.</span></span> <span data-ttu-id="6753a-229">例如，如果您在配置采购申请工作流的审核步骤，您可能值想要审核步骤仅在采购申请金额大于 10,000 美元时发生。</span><span class="sxs-lookup"><span data-stu-id="6753a-229">For example, if you're configuring an approval step for a purchase requisition workflow, you might want the approval step to occur only if the amount of the purchase requisition is more than USD 10,000.</span></span> <span data-ttu-id="6753a-230">按照以下步骤指定何时需要审核步骤。</span><span class="sxs-lookup"><span data-stu-id="6753a-230">Follow these steps to specify when the approval step is required.</span></span>

1.  <span data-ttu-id="6753a-231">在左窗格中，单击**条件**。</span><span class="sxs-lookup"><span data-stu-id="6753a-231">In the left pane, click **Condition**.</span></span>
2.  <span data-ttu-id="6753a-232">选择“**仅当满足以下条件时运行此步骤**”选项。</span><span class="sxs-lookup"><span data-stu-id="6753a-232">Select the **Run this step only when the following condition is met** option.</span></span>
3.  <span data-ttu-id="6753a-233">输入条件。</span><span class="sxs-lookup"><span data-stu-id="6753a-233">Enter a condition.</span></span>
4.  <span data-ttu-id="6753a-234">输入需要的任何其他条件。</span><span class="sxs-lookup"><span data-stu-id="6753a-234">Enter any additional conditions that are required.</span></span>
5.  <span data-ttu-id="6753a-235">要验证输入的条件是否正确配置，请按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="6753a-235">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="6753a-236">单击“**测试**”。</span><span class="sxs-lookup"><span data-stu-id="6753a-236">Click **Test**.</span></span>
    2.  <span data-ttu-id="6753a-237">在**测试工作流条件**页面，在**验证条件**区域，选择一条记录。</span><span class="sxs-lookup"><span data-stu-id="6753a-237">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="6753a-238">单击“**测试**”。</span><span class="sxs-lookup"><span data-stu-id="6753a-238">Click **Test**.</span></span> <span data-ttu-id="6753a-239">系统对该记录进行评估，判断其是否符合您定义的条件。</span><span class="sxs-lookup"><span data-stu-id="6753a-239">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="6753a-240">单击**确定**或**取消**返回到**属性**页面。</span><span class="sxs-lookup"><span data-stu-id="6753a-240">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-what-happens-when-the-document-is-overdue"></a><span data-ttu-id="6753a-241">指定文档逾期时采取的行动</span><span class="sxs-lookup"><span data-stu-id="6753a-241">Specify what happens when the document is overdue</span></span>
<span data-ttu-id="6753a-242">如果用户未在分配的时间内对文档进行操作，则该文档逾期。</span><span class="sxs-lookup"><span data-stu-id="6753a-242">If a user doesn't take action on a document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="6753a-243">可呈报逾期的文档，或自动将该文档分配给其他用户进行审核。</span><span class="sxs-lookup"><span data-stu-id="6753a-243">A document that is overdue can be escalated, or automatically assigned to another user for approval.</span></span> <span data-ttu-id="6753a-244">如果文档逾期，请执行以下步骤进行呈报。</span><span class="sxs-lookup"><span data-stu-id="6753a-244">Follow these steps to escalate the document if it's overdue.</span></span>

1.  <span data-ttu-id="6753a-245">在左窗格中，单击**呈报**。</span><span class="sxs-lookup"><span data-stu-id="6753a-245">In the left pane, click **Escalation**.</span></span>
2.  <span data-ttu-id="6753a-246">选择**使用呈报路线**复选框创建呈报路线。</span><span class="sxs-lookup"><span data-stu-id="6753a-246">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="6753a-247">系统自动将文档分配给呈报路线中列出的用户。</span><span class="sxs-lookup"><span data-stu-id="6753a-247">The system automatically assigns the document to the users who are listed in the escalation path.</span></span> <span data-ttu-id="6753a-248">例如，下表显示呈报路线。</span><span class="sxs-lookup"><span data-stu-id="6753a-248">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="6753a-249">序列</span><span class="sxs-lookup"><span data-stu-id="6753a-249">Sequence</span></span> | <span data-ttu-id="6753a-250">呈报路线</span><span class="sxs-lookup"><span data-stu-id="6753a-250">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="6753a-251">1</span><span class="sxs-lookup"><span data-stu-id="6753a-251">1</span></span>        | <span data-ttu-id="6753a-252">分配给：Donna</span><span class="sxs-lookup"><span data-stu-id="6753a-252">Assign to: Donna</span></span>     |
    | <span data-ttu-id="6753a-253">2</span><span class="sxs-lookup"><span data-stu-id="6753a-253">2</span></span>        | <span data-ttu-id="6753a-254">分配给：Erin</span><span class="sxs-lookup"><span data-stu-id="6753a-254">Assign to: Erin</span></span>      |
    | <span data-ttu-id="6753a-255">3</span><span class="sxs-lookup"><span data-stu-id="6753a-255">3</span></span>        | <span data-ttu-id="6753a-256">最后操作：拒绝</span><span class="sxs-lookup"><span data-stu-id="6753a-256">Final action: Reject</span></span> |

    <span data-ttu-id="6753a-257">在此示例中，系统将逾期文档分配给 Donna。</span><span class="sxs-lookup"><span data-stu-id="6753a-257">In this example, the system assigns the overdue document to Donna.</span></span> <span data-ttu-id="6753a-258">如果 Donna 未在分配的时间内响应，则系统将此文档分配给 Erin。</span><span class="sxs-lookup"><span data-stu-id="6753a-258">If Donna doesn't respond in the allotted time, the system assigns the document to Erin.</span></span> <span data-ttu-id="6753a-259">如果 Erin 未在分配的时间内响应，则系统拒绝该文档。</span><span class="sxs-lookup"><span data-stu-id="6753a-259">If Erin doesn't respond in the allotted time, the system rejects the document.</span></span>
3.  <span data-ttu-id="6753a-260">要将用户添加到呈报路线中，单击**添加呈报**。</span><span class="sxs-lookup"><span data-stu-id="6753a-260">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="6753a-261">在**分配类型**选项卡上，选择下表中的选项之一，然后按照该选项的其他步骤转到步骤 4。</span><span class="sxs-lookup"><span data-stu-id="6753a-261">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="6753a-262">选项</span><span class="sxs-lookup"><span data-stu-id="6753a-262">Option</span></span></th>
    <th><span data-ttu-id="6753a-263">文档呈报到的用户</span><span class="sxs-lookup"><span data-stu-id="6753a-263">Users that the document is escalated to</span></span></th>
    <th><span data-ttu-id="6753a-264">附加步骤</span><span class="sxs-lookup"><span data-stu-id="6753a-264">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="6753a-265">层次结构</span><span class="sxs-lookup"><span data-stu-id="6753a-265">Hierarchy</span></span></td>
    <td><span data-ttu-id="6753a-266">特定组织层次结构中的用户</span><span class="sxs-lookup"><span data-stu-id="6753a-266">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6753a-267">在您选择<strong>层次结构</strong>后，在选项卡<strong>层次结构选择</strong>上，在<strong>层次结构类型</strong>列表中，选择要向其呈报文档的层次结构的类型。</span><span class="sxs-lookup"><span data-stu-id="6753a-267">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the document to.</span></span></li>
    <li><span data-ttu-id="6753a-268">系统必须从层次结构中检索一系列用户姓名。</span><span class="sxs-lookup"><span data-stu-id="6753a-268">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="6753a-269">这些姓名代表可向其呈报文档的用户。</span><span class="sxs-lookup"><span data-stu-id="6753a-269">These names represent users that the document can be escalated to.</span></span> <span data-ttu-id="6753a-270">按照以下步骤指定系统检索的用户名范围的起点和终点：</span><span class="sxs-lookup"><span data-stu-id="6753a-270">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="6753a-271">若要指定起点，请在<strong>启动自</strong>列表中选择一名人员。</span><span class="sxs-lookup"><span data-stu-id="6753a-271">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="6753a-272">若要指定终点，请单击“<strong>添加条件</strong>”。</span><span class="sxs-lookup"><span data-stu-id="6753a-272">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="6753a-273">然后输入一个确定系统停止检索姓名的层次结构的条件。</span><span class="sxs-lookup"><span data-stu-id="6753a-273">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="6753a-274">在<strong>层次结构选项</strong>选项卡上，指定应向其呈报文档的范围内的用户：</span><span class="sxs-lookup"><span data-stu-id="6753a-274">On the <strong>Hierarchy options</strong> tab, specify which users in the range the document should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="6753a-275"><strong>分配给所有检索到的用户</strong> – 文档将呈报给范围内的所有用户。</span><span class="sxs-lookup"><span data-stu-id="6753a-275"><strong>Assign to all users retrieved</strong> – The document is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="6753a-276"><strong>仅分配给最后检索到的用户</strong> – 文档将呈报给范围内的最后一名用户。</span><span class="sxs-lookup"><span data-stu-id="6753a-276"><strong>Assign only to last user retrieved</strong> – The document is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="6753a-277"><strong>排除满足以下条件的用户</strong> – 文档不呈报给满足特定条件的范围内的所有用户。</span><span class="sxs-lookup"><span data-stu-id="6753a-277"><strong>Exclude users with the following condition</strong> – The document isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="6753a-278">单击“<strong>添加条件</strong>”以指定条件。</span><span class="sxs-lookup"><span data-stu-id="6753a-278">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="6753a-279">工作流用户</span><span class="sxs-lookup"><span data-stu-id="6753a-279">Workflow user</span></span></td>
    <td><span data-ttu-id="6753a-280">当前工作流中的用户</span><span class="sxs-lookup"><span data-stu-id="6753a-280">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="6753a-281">在您选择<strong>工作流用户</strong>后，在选项卡<strong>工作流用户</strong>上，在<strong>工作流用户</strong>列表中，选择参与工作流的用户。</span><span class="sxs-lookup"><span data-stu-id="6753a-281">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="6753a-282">用户</span><span class="sxs-lookup"><span data-stu-id="6753a-282">User</span></span></td>
    <td><span data-ttu-id="6753a-283">特定 Finance and Operations 用户</span><span class="sxs-lookup"><span data-stu-id="6753a-283">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6753a-284">在选择<strong>用户</strong>后，单击<strong>用户</strong>选项卡。</span><span class="sxs-lookup"><span data-stu-id="6753a-284">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="6753a-285"><strong>可用用户</strong>列表包含所有 Finance and Operations 用户。</span><span class="sxs-lookup"><span data-stu-id="6753a-285">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="6753a-286">选择要向其呈报文档的用户，然后将这些用户移动到<strong>所选用户</strong>列表。</span><span class="sxs-lookup"><span data-stu-id="6753a-286">Select the users to escalate the document to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  <span data-ttu-id="6753a-287">在**时间限制**选项卡上，在**持续时间**字段中，指定指定用户必须在多长时间内对文档采取行动或进行响应。</span><span class="sxs-lookup"><span data-stu-id="6753a-287">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents.</span></span> <span data-ttu-id="6753a-288">选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="6753a-288">Select one of the following options:</span></span>
    -   <span data-ttu-id="6753a-289">**小时** – 输入用户必须响应的小时数。</span><span class="sxs-lookup"><span data-stu-id="6753a-289">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="6753a-290">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="6753a-290">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="6753a-291">**天** – 输入用户必须响应的天数。</span><span class="sxs-lookup"><span data-stu-id="6753a-291">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="6753a-292">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="6753a-292">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="6753a-293">**周** – 输入用户必须响应的周数。</span><span class="sxs-lookup"><span data-stu-id="6753a-293">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    -   <span data-ttu-id="6753a-294">**月** – 选择用户必须在哪一天和哪一周之前响应。</span><span class="sxs-lookup"><span data-stu-id="6753a-294">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="6753a-295">例如，您可能希望用户在该月的第三周的星期五之前进行响应。</span><span class="sxs-lookup"><span data-stu-id="6753a-295">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="6753a-296">**年** – 选择用户必须在哪一天、哪一周和哪一月之前响应。</span><span class="sxs-lookup"><span data-stu-id="6753a-296">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="6753a-297">例如，您可能希望用户在十二月的第三周的星期五之前进行响应。</span><span class="sxs-lookup"><span data-stu-id="6753a-297">For example, you might want the user to respond by Friday of the third week of December.</span></span>

5.  <span data-ttu-id="6753a-298">对每个应添加到呈报路线的用户重复第 3 步到第 4 步。</span><span class="sxs-lookup"><span data-stu-id="6753a-298">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="6753a-299">您可以更改用户的顺序。</span><span class="sxs-lookup"><span data-stu-id="6753a-299">You can change the order of the users.</span></span>
6.  <span data-ttu-id="6753a-300">如果呈报路线中的用户未在分配的时间内响应，则系统将自动对该文档采取操作。</span><span class="sxs-lookup"><span data-stu-id="6753a-300">If the users in the escalation path don't respond in the allotted time, the system automatically take action on the document.</span></span> <span data-ttu-id="6753a-301">若要指定系统执行的操作，选择**操作**行，然后，在**结束操作**选项卡上，选择一项操作。</span><span class="sxs-lookup"><span data-stu-id="6753a-301">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>






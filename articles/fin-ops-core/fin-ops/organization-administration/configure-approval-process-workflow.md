---
title: 配置工作流中的审核流程
description: 使用以下过程配置审核流程的属性。
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b09d09464eae932bf9caf4f2ea38cbbb3b4f0162
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190204"
---
# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="e8c2b-103">配置工作流中的审核流程</span><span class="sxs-lookup"><span data-stu-id="e8c2b-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8c2b-104">使用以下过程配置审核流程的属性。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="e8c2b-105">要配置审核流程，在“工作流”编辑器中，右键单击审核元素，然后单击**属性**以打开**属性**窗体。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-the-approval-process"></a><span data-ttu-id="e8c2b-106">为审核流程命名</span><span class="sxs-lookup"><span data-stu-id="e8c2b-106">Name the approval process</span></span>

<span data-ttu-id="e8c2b-107">按照以下步骤为审核流程输入名称。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-107">Follow these steps to enter a name for the approval process.</span></span>

1. <span data-ttu-id="e8c2b-108">在左侧窗格中，单击**基本设置**。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-108">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="e8c2b-109">在**名称**字段中，为该审核流程输入唯一名称。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="e8c2b-110">指定系统何时对文档采取操作</span><span class="sxs-lookup"><span data-stu-id="e8c2b-110">Specify when the system automatically acts on the document</span></span>

<span data-ttu-id="e8c2b-111">如果满足特定条件，可将系统配置为自动对对文档采取操作。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="e8c2b-112">例如，系统可审核总金额小于 100 美元的支出报表。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="e8c2b-113">按照以下步骤指定系统何时对文档采取操作。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-113">Follow these steps to specify when the system acts on the document.</span></span>

1. <span data-ttu-id="e8c2b-114">在左窗格中，单击**自动操作**。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-114">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="e8c2b-115">选中**启用自动操作**复选框。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-115">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="e8c2b-116">单击**添加条件**。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-116">Click **Add condition**.</span></span>
4. <span data-ttu-id="e8c2b-117">输入条件。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-117">Enter a condition.</span></span>
5. <span data-ttu-id="e8c2b-118">按需输入附加条件。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-118">Enter additional conditions, if necessary.</span></span>
6. <span data-ttu-id="e8c2b-119">要验证输入的条件是否正确配置，请完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="e8c2b-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="e8c2b-120">单击**测试**以打开**测试工作流条件**窗体。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="e8c2b-121">在该窗体的**验证条件**区域中选择某个记录。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-121">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="e8c2b-122">单击**测试**。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-122">Click **Test**.</span></span> <span data-ttu-id="e8c2b-123">系统对该记录进行评估，判断其是否符合您定义的条件。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="e8c2b-124">单击**确定**或**取消**返回到**属性**窗体。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7. <span data-ttu-id="e8c2b-125">在**自动完成操作**列表中选择系统应对文档采取的操作。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="e8c2b-126">指定发送通知的时间</span><span class="sxs-lookup"><span data-stu-id="e8c2b-126">Specify when notifications are sent</span></span>

<span data-ttu-id="e8c2b-127">您可以在审核、拒绝、委托、呈报或更改文档后向相关人员发送通知。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="e8c2b-128">按照以下步骤指定发送通知的时间以通知发送给哪些人员。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="e8c2b-129">在左窗格中，单击**通知**。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-129">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="e8c2b-130">选中要对其发送通知的事件旁边的复选框：</span><span class="sxs-lookup"><span data-stu-id="e8c2b-130">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="e8c2b-131">**委托**- 将文档分配给其他用户进行审核时。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    - <span data-ttu-id="e8c2b-132">**呈报**- 分配的用户未在分配的时间内对文档采取操作时。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    - <span data-ttu-id="e8c2b-133">**审核**- 已审核文档时。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-133">**Approve** – When a document has been approved.</span></span>
    - <span data-ttu-id="e8c2b-134">**拒绝**- 拒绝文档时。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-134">**Reject** – When a document has been rejected.</span></span>
    - <span data-ttu-id="e8c2b-135">**请求更改**- 分配的用户请求对提交的文档进行更改时。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3. <span data-ttu-id="e8c2b-136">为您在第 2 步中选择的事件选择行。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-136">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="e8c2b-137">单击**通知文本**选项卡。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-137">Click the **Notification text** tab.</span></span>
5. <span data-ttu-id="e8c2b-138">在文本框中，输入通知的文本。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-138">In the text box, enter the text for the notification.</span></span>
6. <span data-ttu-id="e8c2b-139">要对文本进行个性化设置，可以插入占位符，向用户显示时，该占位符由相应的数据替换。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="e8c2b-140">按照以下步骤插入占位符：</span><span class="sxs-lookup"><span data-stu-id="e8c2b-140">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="e8c2b-141">在消息文本中，单击应出现占位符的位置。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2. <span data-ttu-id="e8c2b-142">单击**插入占位符**。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-142">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="e8c2b-143">在显示的列表中，选择要插入的占位符。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="e8c2b-144">单击**插入**。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-144">Click **Insert**.</span></span>

7. <span data-ttu-id="e8c2b-145">要添加通知的翻译，请单击**翻译**。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="e8c2b-146">在显示在窗体中，执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="e8c2b-146">In the form that is displayed, follow these steps:</span></span>

    1. <span data-ttu-id="e8c2b-147">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-147">Click **Add**.</span></span>
    2. <span data-ttu-id="e8c2b-148">在显示的列表，选择您要输入的文本的语言。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3. <span data-ttu-id="e8c2b-149">在**已翻译的文本**文本框中输入文本。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-149">In the **Translated text** text box, enter the text.</span></span>
    4. <span data-ttu-id="e8c2b-150">要对文本进行个性化设置，插入占位符。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-150">To personalize the text, insert placeholders.</span></span>
    5. <span data-ttu-id="e8c2b-151">单击**关闭**。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-151">Click **Close**.</span></span>

8. <span data-ttu-id="e8c2b-152">单击**接收人**选项卡。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-152">Click the **Recipient** tab.</span></span>
9. <span data-ttu-id="e8c2b-153">指定通知发送给哪些人员。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="e8c2b-154">选择下表中的选项之一，然后按照该选项的其他步骤转到第 10 步。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="e8c2b-155">选项</span><span class="sxs-lookup"><span data-stu-id="e8c2b-155">Option</span></span></th>
    <th><span data-ttu-id="e8c2b-156">通知收件人。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="e8c2b-157">附加步骤</span><span class="sxs-lookup"><span data-stu-id="e8c2b-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="e8c2b-158"><strong>参与者</strong></span><span class="sxs-lookup"><span data-stu-id="e8c2b-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="e8c2b-159">分配到特定组或角色的用户</span><span class="sxs-lookup"><span data-stu-id="e8c2b-159">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="e8c2b-160">在选择<strong>参与者</strong>后，单击<strong>基于角色</strong>选项卡。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="e8c2b-161">在<strong>参与者类型</strong>列表中，选择向其发送通知的组或角色类型。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="e8c2b-162">在<strong>参与者</strong>列表中，选择向其发送通知的组或角色。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="e8c2b-163"><strong>工作流用户</strong></span><span class="sxs-lookup"><span data-stu-id="e8c2b-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="e8c2b-164">参与当前工作流的用户</span><span class="sxs-lookup"><span data-stu-id="e8c2b-164">Users who participate in the current workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="e8c2b-165">在选择<strong>工作流用户</strong>后，单击<strong>工作流用户</strong>选项卡。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="e8c2b-166">在<strong>工作流用户</strong>列表中，选择参与工作流的用户。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="e8c2b-167"><strong>用户</strong></span><span class="sxs-lookup"><span data-stu-id="e8c2b-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="e8c2b-168">特定用户</span><span class="sxs-lookup"><span data-stu-id="e8c2b-168">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="e8c2b-169">在选择<strong>用户</strong>后，单击<strong>用户</strong>选项卡。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="e8c2b-170">选择向其发送通知的用户，然后将这些用户移动到<strong>所选用户</strong>列表中。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-170">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="e8c2b-171">对您在第 2 步中选择的每个事件重复 第 3 步到第 9 步。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-171">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="e8c2b-172">指定最终审核人。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-172">Specify a final approver</span></span>

<span data-ttu-id="e8c2b-173">您可能想要为审核人是提交文档进行审核的人员的情景指定最终审核人。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-173">You may want to designate a final approver for scenarios where the approver is the person who submitted the document for approval.</span></span> <span data-ttu-id="e8c2b-174">按照以下步骤指定最终审核人。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-174">Follow these steps to specify a final approver.</span></span>

1. <span data-ttu-id="e8c2b-175">在左侧窗格中，单击**高级设置**。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-175">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="e8c2b-176">选中**使用最终审核人**复选框。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-176">Select the **Use final approver** check box.</span></span>
3. <span data-ttu-id="e8c2b-177">从列表中选择要作为最终审核人的用户。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-177">In the list, select the user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="e8c2b-178">设置时间限制</span><span class="sxs-lookup"><span data-stu-id="e8c2b-178">Set a time limit</span></span>

<span data-ttu-id="e8c2b-179">如果必须在特定时间内完成审核流程，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-179">Follow these steps if the approval process must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="e8c2b-180">在这些步骤中选择的选项将覆盖您在每个审核步骤的**分配**和**呈报**区域选择的选项。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-180">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span>

1. <span data-ttu-id="e8c2b-181">在左侧窗格中，单击**高级设置**。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-181">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="e8c2b-182">选中**为工作流元素** **设置时间限制**复选框。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-182">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3. <span data-ttu-id="e8c2b-183">在**持续时间**字段中，指定必须在何时完成审核流程。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-183">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="e8c2b-184">选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="e8c2b-184">Select one of the following options:</span></span>

    - <span data-ttu-id="e8c2b-185">**小时** – 输入必须在几小时内完成审核流程。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-185">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="e8c2b-186">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="e8c2b-187">**天** – 输入必须在几天内完成审核流程。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-187">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="e8c2b-188">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-188">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="e8c2b-189">**周** – 输入必须在几周内完成审核流程。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-189">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    - <span data-ttu-id="e8c2b-190">**月** – 选择必须在哪一周和哪一日前完成审核流程。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-190">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="e8c2b-191">例如，您可能希望在当月第三周的周五之前完成审核流程。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-191">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="e8c2b-192">**年** – 选择必须在哪一月、哪一周和哪一日前完成审核流程。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-192">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="e8c2b-193">例如，您可能希望在十二月的第三周的周五之前完成审核流程。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-193">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="e8c2b-194">如果超出时间限制，系统将对文档采取操作。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-194">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="e8c2b-195">在**操作**列表中选择系统应采取的操作。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-195">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="e8c2b-196">指定用户可以采取的操作</span><span class="sxs-lookup"><span data-stu-id="e8c2b-196">Specify which actions are available to the user</span></span>

<span data-ttu-id="e8c2b-197">将单据分配给用户进行审核后，该用户必须对该单据采取行动。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-197">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="e8c2b-198">按照以下步骤指定要对用户提交的文档采取什么操作。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-198">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>

1. <span data-ttu-id="e8c2b-199">在左侧窗格中，单击**高级设置**。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-199">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="e8c2b-200">如果用户可批准文档，请选中**审核**复选框。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-200">Select the **Approve** check box if the user can approve the document.</span></span>
3. <span data-ttu-id="e8c2b-201">如果用户可拒绝文档，请选中**拒绝**复选框。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-201">Select the **Reject** check box the user can reject the document.</span></span>
4. <span data-ttu-id="e8c2b-202">用户可以请求对文档进行更改时选中**请求更改**复选框。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-202">Select the **Request change** check box the user can request changes to the document.</span></span>
5. <span data-ttu-id="e8c2b-203">如果用户可以将文档分配给其他用户进行审核，请选中**委托**复选框。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-203">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

> [!NOTE]
> <span data-ttu-id="e8c2b-204">**从企业门户中的工作列表启用操作**复选框已被弃用。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-204">The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="e8c2b-205">配置审核步骤</span><span class="sxs-lookup"><span data-stu-id="e8c2b-205">Configure the approval steps</span></span>

<span data-ttu-id="e8c2b-206">审核流程包括多个审核步骤。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-206">An approval process consists of approval steps.</span></span> <span data-ttu-id="e8c2b-207">完成以下过程以将步骤添加到审核流程并配置这些步骤。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-207">Complete the following procedure to add steps the approval process and configure the steps.</span></span>

1. <span data-ttu-id="e8c2b-208">在工作流编辑器中，双击审核流程。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-208">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="e8c2b-209">工作流编辑器显示审核流程的步骤。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-209">The workflow editor displays the steps of the approval process.</span></span>
2. <span data-ttu-id="e8c2b-210">要添加审核步骤，请将步骤从**工作流元素**区域拖到画布。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-210">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3. <span data-ttu-id="e8c2b-211">要配置审核步骤，请参阅“[配置审核步骤](configure-approval-step-workflow.md)”。</span><span class="sxs-lookup"><span data-stu-id="e8c2b-211">To configure an approval step, see [Configure an approval step](configure-approval-step-workflow.md).</span></span>

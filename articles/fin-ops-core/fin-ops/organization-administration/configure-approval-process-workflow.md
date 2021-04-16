---
title: 配置工作流中的审核流程
description: 使用以下过程配置审核流程的属性。
author: ChrisGarty
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5738c5993c129f9bb4932180916befaf6f6377a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751792"
---
# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="37e6e-103">配置工作流中的审核流程</span><span class="sxs-lookup"><span data-stu-id="37e6e-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37e6e-104">使用以下过程配置审核流程的属性。</span><span class="sxs-lookup"><span data-stu-id="37e6e-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="37e6e-105">要配置审核流程，在“工作流”编辑器中，右键单击审核元素，然后单击 **属性** 以打开 **属性** 窗体。</span><span class="sxs-lookup"><span data-stu-id="37e6e-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-the-approval-process"></a><span data-ttu-id="37e6e-106">为审核流程命名</span><span class="sxs-lookup"><span data-stu-id="37e6e-106">Name the approval process</span></span>

<span data-ttu-id="37e6e-107">按照以下步骤为审核流程输入名称。</span><span class="sxs-lookup"><span data-stu-id="37e6e-107">Follow these steps to enter a name for the approval process.</span></span>

1. <span data-ttu-id="37e6e-108">在左侧窗格中，单击 **基本设置**。</span><span class="sxs-lookup"><span data-stu-id="37e6e-108">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="37e6e-109">在 **名称** 字段中，为该审核流程输入唯一名称。</span><span class="sxs-lookup"><span data-stu-id="37e6e-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="37e6e-110">指定系统何时对文档采取操作</span><span class="sxs-lookup"><span data-stu-id="37e6e-110">Specify when the system automatically acts on the document</span></span>

<span data-ttu-id="37e6e-111">如果满足特定条件，可将系统配置为自动对对文档采取操作。</span><span class="sxs-lookup"><span data-stu-id="37e6e-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="37e6e-112">例如，系统可审核总金额小于 100 美元的支出报表。</span><span class="sxs-lookup"><span data-stu-id="37e6e-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="37e6e-113">按照以下步骤指定系统何时对文档采取操作。</span><span class="sxs-lookup"><span data-stu-id="37e6e-113">Follow these steps to specify when the system acts on the document.</span></span>

1. <span data-ttu-id="37e6e-114">在左窗格中，单击 **自动操作**。</span><span class="sxs-lookup"><span data-stu-id="37e6e-114">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="37e6e-115">选中 **启用自动操作** 复选框。</span><span class="sxs-lookup"><span data-stu-id="37e6e-115">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="37e6e-116">单击 **添加条件**。</span><span class="sxs-lookup"><span data-stu-id="37e6e-116">Click **Add condition**.</span></span>
4. <span data-ttu-id="37e6e-117">输入条件。</span><span class="sxs-lookup"><span data-stu-id="37e6e-117">Enter a condition.</span></span>
5. <span data-ttu-id="37e6e-118">按需输入附加条件。</span><span class="sxs-lookup"><span data-stu-id="37e6e-118">Enter additional conditions, if necessary.</span></span>
6. <span data-ttu-id="37e6e-119">要验证输入的条件是否正确配置，请完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="37e6e-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="37e6e-120">单击 **测试** 以打开 **测试工作流条件** 窗体。</span><span class="sxs-lookup"><span data-stu-id="37e6e-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="37e6e-121">在该窗体的 **验证条件** 区域中选择某个记录。</span><span class="sxs-lookup"><span data-stu-id="37e6e-121">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="37e6e-122">单击 **测试**。</span><span class="sxs-lookup"><span data-stu-id="37e6e-122">Click **Test**.</span></span> <span data-ttu-id="37e6e-123">系统对该记录进行评估，判断其是否符合您定义的条件。</span><span class="sxs-lookup"><span data-stu-id="37e6e-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="37e6e-124">单击 **确定** 或 **取消** 返回到 **属性** 窗体。</span><span class="sxs-lookup"><span data-stu-id="37e6e-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7. <span data-ttu-id="37e6e-125">在 **自动完成操作** 列表中选择系统应对文档采取的操作。</span><span class="sxs-lookup"><span data-stu-id="37e6e-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="37e6e-126">指定发送通知的时间</span><span class="sxs-lookup"><span data-stu-id="37e6e-126">Specify when notifications are sent</span></span>

<span data-ttu-id="37e6e-127">您可以在审核、拒绝、委托、呈报或更改文档后向相关人员发送通知。</span><span class="sxs-lookup"><span data-stu-id="37e6e-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="37e6e-128">按照以下步骤指定发送通知的时间以通知发送给哪些人员。</span><span class="sxs-lookup"><span data-stu-id="37e6e-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="37e6e-129">在左窗格中，单击 **通知**。</span><span class="sxs-lookup"><span data-stu-id="37e6e-129">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="37e6e-130">选中要对其发送通知的事件旁边的复选框：</span><span class="sxs-lookup"><span data-stu-id="37e6e-130">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="37e6e-131">**委托**- 将文档分配给其他用户进行审核时。</span><span class="sxs-lookup"><span data-stu-id="37e6e-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    - <span data-ttu-id="37e6e-132">**呈报**- 分配的用户未在分配的时间内对文档采取操作时。</span><span class="sxs-lookup"><span data-stu-id="37e6e-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    - <span data-ttu-id="37e6e-133">**审核**- 已审核文档时。</span><span class="sxs-lookup"><span data-stu-id="37e6e-133">**Approve** – When a document has been approved.</span></span>
    - <span data-ttu-id="37e6e-134">**拒绝**- 拒绝文档时。</span><span class="sxs-lookup"><span data-stu-id="37e6e-134">**Reject** – When a document has been rejected.</span></span>
    - <span data-ttu-id="37e6e-135">**请求更改**- 分配的用户请求对提交的文档进行更改时。</span><span class="sxs-lookup"><span data-stu-id="37e6e-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3. <span data-ttu-id="37e6e-136">为您在第 2 步中选择的事件选择行。</span><span class="sxs-lookup"><span data-stu-id="37e6e-136">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="37e6e-137">单击 **通知文本** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="37e6e-137">Click the **Notification text** tab.</span></span>
5. <span data-ttu-id="37e6e-138">在文本框中，输入通知的文本。</span><span class="sxs-lookup"><span data-stu-id="37e6e-138">In the text box, enter the text for the notification.</span></span>
6. <span data-ttu-id="37e6e-139">要对文本进行个性化设置，可以插入占位符，向用户显示时，该占位符由相应的数据替换。</span><span class="sxs-lookup"><span data-stu-id="37e6e-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="37e6e-140">按照以下步骤插入占位符：</span><span class="sxs-lookup"><span data-stu-id="37e6e-140">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="37e6e-141">在消息文本中，单击应出现占位符的位置。</span><span class="sxs-lookup"><span data-stu-id="37e6e-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2. <span data-ttu-id="37e6e-142">单击 **插入占位符**。</span><span class="sxs-lookup"><span data-stu-id="37e6e-142">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="37e6e-143">在显示的列表中，选择要插入的占位符。</span><span class="sxs-lookup"><span data-stu-id="37e6e-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="37e6e-144">单击 **插入**。</span><span class="sxs-lookup"><span data-stu-id="37e6e-144">Click **Insert**.</span></span>

7. <span data-ttu-id="37e6e-145">要添加通知的翻译，请单击 **翻译**。</span><span class="sxs-lookup"><span data-stu-id="37e6e-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="37e6e-146">在显示在窗体中，执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="37e6e-146">In the form that is displayed, follow these steps:</span></span>

    1. <span data-ttu-id="37e6e-147">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="37e6e-147">Click **Add**.</span></span>
    2. <span data-ttu-id="37e6e-148">在显示的列表，选择您要输入的文本的语言。</span><span class="sxs-lookup"><span data-stu-id="37e6e-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3. <span data-ttu-id="37e6e-149">在 **已翻译的文本** 文本框中输入文本。</span><span class="sxs-lookup"><span data-stu-id="37e6e-149">In the **Translated text** text box, enter the text.</span></span>
    4. <span data-ttu-id="37e6e-150">要对文本进行个性化设置，插入占位符。</span><span class="sxs-lookup"><span data-stu-id="37e6e-150">To personalize the text, insert placeholders.</span></span>
    5. <span data-ttu-id="37e6e-151">单击 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="37e6e-151">Click **Close**.</span></span>

8. <span data-ttu-id="37e6e-152">单击 **接收人** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="37e6e-152">Click the **Recipient** tab.</span></span>
9. <span data-ttu-id="37e6e-153">指定通知发送给哪些人员。</span><span class="sxs-lookup"><span data-stu-id="37e6e-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="37e6e-154">选择下表中的选项之一，然后按照该选项的其他步骤转到第 10 步。</span><span class="sxs-lookup"><span data-stu-id="37e6e-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="37e6e-155">选项</span><span class="sxs-lookup"><span data-stu-id="37e6e-155">Option</span></span></th>
    <th><span data-ttu-id="37e6e-156">通知收件人。</span><span class="sxs-lookup"><span data-stu-id="37e6e-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="37e6e-157">附加步骤</span><span class="sxs-lookup"><span data-stu-id="37e6e-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="37e6e-158"><strong>参与者</strong></span><span class="sxs-lookup"><span data-stu-id="37e6e-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="37e6e-159">分配到特定组或角色的用户</span><span class="sxs-lookup"><span data-stu-id="37e6e-159">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="37e6e-160">在选择<strong>参与者</strong>后，单击<strong>基于角色</strong>选项卡。</span><span class="sxs-lookup"><span data-stu-id="37e6e-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="37e6e-161">在<strong>参与者类型</strong>列表中，选择向其发送通知的组或角色类型。</span><span class="sxs-lookup"><span data-stu-id="37e6e-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="37e6e-162">在<strong>参与者</strong>列表中，选择向其发送通知的组或角色。</span><span class="sxs-lookup"><span data-stu-id="37e6e-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="37e6e-163"><strong>工作流用户</strong></span><span class="sxs-lookup"><span data-stu-id="37e6e-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="37e6e-164">参与当前工作流的用户</span><span class="sxs-lookup"><span data-stu-id="37e6e-164">Users who participate in the current workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="37e6e-165">在选择<strong>工作流用户</strong>后，单击<strong>工作流用户</strong>选项卡。</span><span class="sxs-lookup"><span data-stu-id="37e6e-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="37e6e-166">在<strong>工作流用户</strong>列表中，选择参与工作流的用户。</span><span class="sxs-lookup"><span data-stu-id="37e6e-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="37e6e-167"><strong>用户</strong></span><span class="sxs-lookup"><span data-stu-id="37e6e-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="37e6e-168">特定用户</span><span class="sxs-lookup"><span data-stu-id="37e6e-168">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="37e6e-169">在选择<strong>用户</strong>后，单击<strong>用户</strong>选项卡。</span><span class="sxs-lookup"><span data-stu-id="37e6e-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="37e6e-170">选择向其发送通知的用户，然后将这些用户移动到<strong>所选用户</strong>列表中。</span><span class="sxs-lookup"><span data-stu-id="37e6e-170">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="37e6e-171">对您在第 2 步中选择的每个事件重复 第 3 步到第 9 步。</span><span class="sxs-lookup"><span data-stu-id="37e6e-171">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="37e6e-172">指定最终审核人。</span><span class="sxs-lookup"><span data-stu-id="37e6e-172">Specify a final approver</span></span>

<span data-ttu-id="37e6e-173">您可以为以下情况指定最终批准者：批准者是提交文档以供批准的人，并且正在使用“不允许提交者批准”。</span><span class="sxs-lookup"><span data-stu-id="37e6e-173">You can designate a final approver for scenarios where the approver is the person who submitted the document for approval and the "disallow approval by submitter" is being used.</span></span> <span data-ttu-id="37e6e-174">按照以下步骤指定最终审核人。</span><span class="sxs-lookup"><span data-stu-id="37e6e-174">Follow these steps to specify a final approver.</span></span>

1. <span data-ttu-id="37e6e-175">在工作流编辑器中，右键单击审核元素，然后选择 **属性** 以打开 **属性** 窗体。</span><span class="sxs-lookup"><span data-stu-id="37e6e-175">In the workflow editor, right-click the approval element, and then select **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="37e6e-176">在左侧窗格中，单击 **高级设置**。</span><span class="sxs-lookup"><span data-stu-id="37e6e-176">In the left pane, click **Advanced settings**.</span></span>
3. <span data-ttu-id="37e6e-177">选中 **使用最终审核人** 复选框。</span><span class="sxs-lookup"><span data-stu-id="37e6e-177">Select the **Use final approver** check box.</span></span>
4. <span data-ttu-id="37e6e-178">从列表中选择要作为最终审核人的用户。</span><span class="sxs-lookup"><span data-stu-id="37e6e-178">In the list, select a user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="37e6e-179">设置时间限制</span><span class="sxs-lookup"><span data-stu-id="37e6e-179">Set a time limit</span></span>

<span data-ttu-id="37e6e-180">如果必须在特定时间内完成审核流程，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="37e6e-180">Follow these steps if the approval process must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="37e6e-181">在这些步骤中选择的选项将覆盖您在每个审核步骤的 **分配** 和 **呈报** 区域选择的选项。</span><span class="sxs-lookup"><span data-stu-id="37e6e-181">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span>

1. <span data-ttu-id="37e6e-182">在左侧窗格中，单击 **高级设置**。</span><span class="sxs-lookup"><span data-stu-id="37e6e-182">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="37e6e-183">选中 **为工作流元素** **设置时间限制** 复选框。</span><span class="sxs-lookup"><span data-stu-id="37e6e-183">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3. <span data-ttu-id="37e6e-184">在 **持续时间** 字段中，指定必须在何时完成审核流程。</span><span class="sxs-lookup"><span data-stu-id="37e6e-184">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="37e6e-185">选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="37e6e-185">Select one of the following options:</span></span>

    - <span data-ttu-id="37e6e-186">**小时** – 输入必须在几小时内完成审核流程。</span><span class="sxs-lookup"><span data-stu-id="37e6e-186">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="37e6e-187">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="37e6e-187">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="37e6e-188">**天** – 输入必须在几天内完成审核流程。</span><span class="sxs-lookup"><span data-stu-id="37e6e-188">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="37e6e-189">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="37e6e-189">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="37e6e-190">**周** – 输入必须在几周内完成审核流程。</span><span class="sxs-lookup"><span data-stu-id="37e6e-190">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    - <span data-ttu-id="37e6e-191">**月** – 选择必须在哪一周和哪一日前完成审核流程。</span><span class="sxs-lookup"><span data-stu-id="37e6e-191">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="37e6e-192">例如，您可能希望在当月第三周的周五之前完成审核流程。</span><span class="sxs-lookup"><span data-stu-id="37e6e-192">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="37e6e-193">**年** – 选择必须在哪一月、哪一周和哪一日前完成审核流程。</span><span class="sxs-lookup"><span data-stu-id="37e6e-193">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="37e6e-194">例如，您可能希望在十二月的第三周的周五之前完成审核流程。</span><span class="sxs-lookup"><span data-stu-id="37e6e-194">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="37e6e-195">如果超出时间限制，系统将对文档采取操作。</span><span class="sxs-lookup"><span data-stu-id="37e6e-195">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="37e6e-196">在 **操作** 列表中选择系统应采取的操作。</span><span class="sxs-lookup"><span data-stu-id="37e6e-196">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="37e6e-197">指定用户可以采取的操作</span><span class="sxs-lookup"><span data-stu-id="37e6e-197">Specify which actions are available to the user</span></span>

<span data-ttu-id="37e6e-198">将单据分配给用户进行审核后，该用户必须对该单据采取行动。</span><span class="sxs-lookup"><span data-stu-id="37e6e-198">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="37e6e-199">按照以下步骤指定要对用户提交的文档采取什么操作。</span><span class="sxs-lookup"><span data-stu-id="37e6e-199">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>

1. <span data-ttu-id="37e6e-200">在左侧窗格中，单击 **高级设置**。</span><span class="sxs-lookup"><span data-stu-id="37e6e-200">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="37e6e-201">如果用户可批准文档，请选中 **审核** 复选框。</span><span class="sxs-lookup"><span data-stu-id="37e6e-201">Select the **Approve** check box if the user can approve the document.</span></span>
3. <span data-ttu-id="37e6e-202">如果用户可拒绝文档，请选中 **拒绝** 复选框。</span><span class="sxs-lookup"><span data-stu-id="37e6e-202">Select the **Reject** check box the user can reject the document.</span></span>
4. <span data-ttu-id="37e6e-203">用户可以请求对文档进行更改时选中 **请求更改** 复选框。</span><span class="sxs-lookup"><span data-stu-id="37e6e-203">Select the **Request change** check box the user can request changes to the document.</span></span>
5. <span data-ttu-id="37e6e-204">如果用户可以将文档分配给其他用户进行审核，请选中 **委托** 复选框。</span><span class="sxs-lookup"><span data-stu-id="37e6e-204">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

> [!NOTE]
> <span data-ttu-id="37e6e-205">**从企业门户中的工作列表启用操作** 复选框已被弃用。</span><span class="sxs-lookup"><span data-stu-id="37e6e-205">The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="37e6e-206">配置审核步骤</span><span class="sxs-lookup"><span data-stu-id="37e6e-206">Configure the approval steps</span></span>

<span data-ttu-id="37e6e-207">审核流程包括多个审核步骤。</span><span class="sxs-lookup"><span data-stu-id="37e6e-207">An approval process consists of approval steps.</span></span> <span data-ttu-id="37e6e-208">完成以下过程以将步骤添加到审核流程并配置这些步骤。</span><span class="sxs-lookup"><span data-stu-id="37e6e-208">Complete the following procedure to add steps the approval process and configure the steps.</span></span>

1. <span data-ttu-id="37e6e-209">在工作流编辑器中，双击审核流程。</span><span class="sxs-lookup"><span data-stu-id="37e6e-209">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="37e6e-210">工作流编辑器显示审核流程的步骤。</span><span class="sxs-lookup"><span data-stu-id="37e6e-210">The workflow editor displays the steps of the approval process.</span></span>
2. <span data-ttu-id="37e6e-211">要添加审核步骤，请将步骤从 **工作流元素** 区域拖到画布。</span><span class="sxs-lookup"><span data-stu-id="37e6e-211">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3. <span data-ttu-id="37e6e-212">要配置审核步骤，请参阅[配置工作流中的审核步骤](configure-approval-step-workflow.md)。</span><span class="sxs-lookup"><span data-stu-id="37e6e-212">To configure an approval step, see [Configure approval steps in a workflow](configure-approval-step-workflow.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: "在工作流中配置自动化任务"
description: "本主题说明如何配置自动化任务的属性。"
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 56e29bd2e875b8bb729e5dfe0c5ac03fc997ecbe
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="configure-an-automated-task-in-a-workflow"></a><span data-ttu-id="e0983-103">在工作流中配置自动化任务</span><span class="sxs-lookup"><span data-stu-id="e0983-103">Configure an automated task in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e0983-104">本主题说明如何配置自动化任务的属性。</span><span class="sxs-lookup"><span data-stu-id="e0983-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="e0983-105">要配置自动化任务，在工作流编辑器中，右键单击任务，然后单击**属性**打开**属性**页面。</span><span class="sxs-lookup"><span data-stu-id="e0983-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="e0983-106">然后使用以下过程配置自动化任务的属性。</span><span class="sxs-lookup"><span data-stu-id="e0983-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="e0983-107">为任务命名</span><span class="sxs-lookup"><span data-stu-id="e0983-107">Name the task</span></span>
<span data-ttu-id="e0983-108">按照以下为自动化任务输入名称。</span><span class="sxs-lookup"><span data-stu-id="e0983-108">Follow these steps to enter a name for the automated task.</span></span>

1.  <span data-ttu-id="e0983-109">在左侧窗格中，单击**基本设置**。</span><span class="sxs-lookup"><span data-stu-id="e0983-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="e0983-110">在**名称**字段中，为该任务输入唯一名称。</span><span class="sxs-lookup"><span data-stu-id="e0983-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="e0983-111">指定发送通知的时间</span><span class="sxs-lookup"><span data-stu-id="e0983-111">Specify when notifications are sent</span></span>
<span data-ttu-id="e0983-112">已允许或取消自动化任务时，您可以向人员发送通知。</span><span class="sxs-lookup"><span data-stu-id="e0983-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="e0983-113">按照以下步骤指定发送通知的时间以通知发送给哪些人员。</span><span class="sxs-lookup"><span data-stu-id="e0983-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1.  <span data-ttu-id="e0983-114">在左窗格中，单击**通知**。</span><span class="sxs-lookup"><span data-stu-id="e0983-114">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="e0983-115">选中要对其发送通知的事件旁边的复选框：</span><span class="sxs-lookup"><span data-stu-id="e0983-115">Select the check box next to the events to send notifications for:</span></span>
    -   <span data-ttu-id="e0983-116">“**执行**”– 在运行任务时发送通知。</span><span class="sxs-lookup"><span data-stu-id="e0983-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    -   <span data-ttu-id="e0983-117">“**已取消**”– 在取消任务时发送通知。</span><span class="sxs-lookup"><span data-stu-id="e0983-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3.  <span data-ttu-id="e0983-118">为您在第 2 步中选择的事件选择行。</span><span class="sxs-lookup"><span data-stu-id="e0983-118">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="e0983-119">在**通知文本**选项卡上，在文本框中输入通知的文本。</span><span class="sxs-lookup"><span data-stu-id="e0983-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5.  <span data-ttu-id="e0983-120">要对通知进行个性化设置，可以插入占位符。</span><span class="sxs-lookup"><span data-stu-id="e0983-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="e0983-121">向用户显示通知时，占位符由适当的数据代替。</span><span class="sxs-lookup"><span data-stu-id="e0983-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="e0983-122">按照以下步骤插入占位符：</span><span class="sxs-lookup"><span data-stu-id="e0983-122">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="e0983-123">在文本框中，单击应该出现占位符的位置。</span><span class="sxs-lookup"><span data-stu-id="e0983-123">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="e0983-124">单击**插入占位符**。</span><span class="sxs-lookup"><span data-stu-id="e0983-124">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="e0983-125">在出现的列表中，选择要插入的占位符。</span><span class="sxs-lookup"><span data-stu-id="e0983-125">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="e0983-126">单击“**插入**”。</span><span class="sxs-lookup"><span data-stu-id="e0983-126">Click **Insert**.</span></span>

6.  <span data-ttu-id="e0983-127">若要添加通知的翻译，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="e0983-127">To add translations of the notification, follow these steps:</span></span>
    1.  <span data-ttu-id="e0983-128">单击**翻译**。</span><span class="sxs-lookup"><span data-stu-id="e0983-128">Click **Translations**.</span></span>
    2.  <span data-ttu-id="e0983-129">在出现的页面上，单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="e0983-129">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="e0983-130">在出现的列表中，选择您输入文本使用的语言。</span><span class="sxs-lookup"><span data-stu-id="e0983-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="e0983-131">在**已翻译的文本**字段中，输入文本。</span><span class="sxs-lookup"><span data-stu-id="e0983-131">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="e0983-132">如果要对文本进行个性化设置，可以如步骤 5 所述插入占位符。</span><span class="sxs-lookup"><span data-stu-id="e0983-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6.  <span data-ttu-id="e0983-133">单击**“关闭”**。</span><span class="sxs-lookup"><span data-stu-id="e0983-133">Click **Close**.</span></span>

7.  <span data-ttu-id="e0983-134">在**接收人**选项卡上，指定向谁发送通知。</span><span class="sxs-lookup"><span data-stu-id="e0983-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="e0983-135">选择下表中的选项之一，然后按照该选项的其他步骤转到第 8 步。</span><span class="sxs-lookup"><span data-stu-id="e0983-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="e0983-136">选项</span><span class="sxs-lookup"><span data-stu-id="e0983-136">Option</span></span></th>
    <th><span data-ttu-id="e0983-137">通知收件人。</span><span class="sxs-lookup"><span data-stu-id="e0983-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="e0983-138">附加步骤</span><span class="sxs-lookup"><span data-stu-id="e0983-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="e0983-139">参与者</span><span class="sxs-lookup"><span data-stu-id="e0983-139">Participant</span></span></td>
    <td><span data-ttu-id="e0983-140">分配到特定组或角色的用户</span><span class="sxs-lookup"><span data-stu-id="e0983-140">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="e0983-141">在您选择<strong>参与者</strong>后，在选项卡<strong>基于角色</strong>上，在<strong>参与者类型</strong>列表中，选择要向其发送通知的组或角色的类型。</span><span class="sxs-lookup"><span data-stu-id="e0983-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="e0983-142">在<strong>参与者</strong>列表中，选择向其发送通知的组或角色。</span><span class="sxs-lookup"><span data-stu-id="e0983-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="e0983-143">工作流用户</span><span class="sxs-lookup"><span data-stu-id="e0983-143">Workflow user</span></span></td>
    <td><span data-ttu-id="e0983-144">参与当前工作流的用户</span><span class="sxs-lookup"><span data-stu-id="e0983-144">Users who participate in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="e0983-145">在您选择<strong>工作流用户</strong>后，在选项卡<strong>工作流用户</strong>上，在<strong>工作流用户</strong>列表中，选择参与工作流的用户。</span><span class="sxs-lookup"><span data-stu-id="e0983-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="e0983-146">用户</span><span class="sxs-lookup"><span data-stu-id="e0983-146">User</span></span></td>
    <td><span data-ttu-id="e0983-147">特定的 Microsoft Dynamics 365 for Finance and Operations 用户</span><span class="sxs-lookup"><span data-stu-id="e0983-147">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="e0983-148">在选择<strong>用户</strong>后，单击<strong>用户</strong>选项卡。</span><span class="sxs-lookup"><span data-stu-id="e0983-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="e0983-149"><strong>可用用户</strong>列表包含所有 Finance and Operations 用户。</span><span class="sxs-lookup"><span data-stu-id="e0983-149">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="e0983-150">选择向其发送通知的用户，然后将这些用户移动到<strong>所选用户</strong>列表中。</span><span class="sxs-lookup"><span data-stu-id="e0983-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="e0983-151">对您在第 2 步中选择的每个事件重复 第 3 步到第 7 步。</span><span class="sxs-lookup"><span data-stu-id="e0983-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>





---
title: 配置工作流中的手动决策
description: 本主题说明如何配置手动决策的属性。
author: ChrisGarty
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d351facbce02355ddb4bdf91d43d9df561e4f3b5
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798844"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="5b3c1-103">配置工作流中的手动决策</span><span class="sxs-lookup"><span data-stu-id="5b3c1-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b3c1-104">本主题说明如何配置手动决策的属性。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="5b3c1-105">要配置手动决策，在工作流编辑器中，右键单击“手动决策”，然后单击 **属性** 打开 **属性** 页面。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="5b3c1-106">然后使用以下过程配置手动决策的属性。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="5b3c1-107">为决策命名</span><span class="sxs-lookup"><span data-stu-id="5b3c1-107">Name the decision</span></span>

<span data-ttu-id="5b3c1-108">按照以下为手动决策输入名称。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="5b3c1-109">在左侧窗格中，单击 **基本设置**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="5b3c1-110">在 **名称** 字段中，为手动决策输入唯一名称。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="5b3c1-111">输入主题行和说明</span><span class="sxs-lookup"><span data-stu-id="5b3c1-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="5b3c1-112">必须为分配到手动决策的用户提供主题行和说明。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="5b3c1-113">例如，如果您在为采购申请配置决策，则分配到该决策的用户在 **采购申请** 页面看到主题行和说明。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="5b3c1-114">主题行显示在页面的消息栏中。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="5b3c1-115">然后用户可单击消息栏中的图标查看说明。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="5b3c1-116">按照以下步骤输入主题行和说明。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="5b3c1-117">在左侧窗格中，单击 **基本设置**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="5b3c1-118">在 **说明** 选项卡上，在 **工作项主题** 字段中，输入主题行。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="5b3c1-119">要个性化主题行，可以插入占位符。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="5b3c1-120">向用户显示主题行时，占位符由适当的数据代替。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="5b3c1-121">按照以下步骤插入占位符：</span><span class="sxs-lookup"><span data-stu-id="5b3c1-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="5b3c1-122">在文本框中，单击应该出现占位符的位置。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="5b3c1-123">单击 **插入占位符**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="5b3c1-124">在出现的列表中，选择要插入的占位符。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="5b3c1-125">单击 **插入**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-125">Click **Insert**.</span></span>

4. <span data-ttu-id="5b3c1-126">若要添加主题行的翻译，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="5b3c1-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="5b3c1-127">单击 **翻译**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="5b3c1-128">在出现的页面上，单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="5b3c1-129">在出现的列表中，选择您输入文本使用的语言。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="5b3c1-130">在 **已翻译的文本** 字段中，输入文本。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="5b3c1-131">如果要对文本进行个性化设置，可以如步骤 3 所述插入占位符。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="5b3c1-132">单击 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-132">Click **Close**.</span></span>

5. <span data-ttu-id="5b3c1-133">在 **工作项说明** 字段中，输入说明。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="5b3c1-134">要对说明进行个性化设置，可以插入占位符。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="5b3c1-135">向用户显示说明时，占位符由适当的数据代替。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="5b3c1-136">按照以下步骤插入占位符：</span><span class="sxs-lookup"><span data-stu-id="5b3c1-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="5b3c1-137">在文本框中，单击应该出现占位符的位置。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="5b3c1-138">单击 **插入占位符**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="5b3c1-139">在出现的列表中，选择要插入的占位符。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="5b3c1-140">单击 **插入**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-140">Click **Insert**.</span></span>

7. <span data-ttu-id="5b3c1-141">若要添加说明的翻译，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="5b3c1-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="5b3c1-142">单击 **翻译**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="5b3c1-143">在出现的页面上，单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="5b3c1-144">在出现的列表中，选择您输入文本使用的语言。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="5b3c1-145">在 **已翻译的文本** 字段中，输入文本。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="5b3c1-146">如果要对文本进行个性化设置，可以如步骤 6 所述插入占位符。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="5b3c1-147">单击 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="5b3c1-148">指定决策的可能结果</span><span class="sxs-lookup"><span data-stu-id="5b3c1-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="5b3c1-149">通常，将文档分配给决策者时，决策者将询问问题。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="5b3c1-150">该问题的答案通常是 **是** 或 **否** 或者是 **True** 或 **False**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="5b3c1-151">按照以下步骤指定手动决策的可能结果。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="5b3c1-152">在左侧窗格中，单击 **基本设置**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="5b3c1-153">在 **结果** 选项卡上，在 **结果 1** 字段中，输入结果的名称或者选项。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="5b3c1-154">若要添加结果的翻译，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="5b3c1-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="5b3c1-155">单击 **翻译**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="5b3c1-156">在出现的页面上，单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="5b3c1-157">在出现的列表中，选择您输入文本使用的语言。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="5b3c1-158">在 **已翻译的文本** 字段中，输入文本。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="5b3c1-159">单击 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-159">Click **Close**.</span></span>

4. <span data-ttu-id="5b3c1-160">在 **结果 2** 字段中，输入结果的名称或选项。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="5b3c1-161">若要添加结果的翻译，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="5b3c1-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="5b3c1-162">单击 **翻译**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="5b3c1-163">在出现的页面上，单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="5b3c1-164">在出现的列表中，选择您输入文本使用的语言。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="5b3c1-165">在 **已翻译的文本** 字段中，输入文本。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="5b3c1-166">单击 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="5b3c1-167">指定发送通知的时间</span><span class="sxs-lookup"><span data-stu-id="5b3c1-167">Specify when notifications are sent</span></span>

<span data-ttu-id="5b3c1-168">制定、委托、呈报决策时，您可以向人员发送通知。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="5b3c1-169">按照以下步骤指定发送通知的时间以通知发送给哪些人员。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="5b3c1-170">在左窗格中，单击 **通知**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="5b3c1-171">选中应针对其发送通知的事件旁边的复选框：</span><span class="sxs-lookup"><span data-stu-id="5b3c1-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="5b3c1-172">**\[选择 1\]** – 分配的用户选择了 **\[选择 1\]**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="5b3c1-173">**\[选择 2\]** – 分配的用户选择了 **\[选择 2\]**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="5b3c1-174">**委托** – 分配的用户将决策分配给其他用户。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="5b3c1-175">**呈报** – 分配的用户未在分配的时间内制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="5b3c1-176">为您在第 2 步中选择的事件选择行。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="5b3c1-177">在 **通知文本** 选项卡上，在文本框中输入通知的文本。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="5b3c1-178">要对通知进行个性化设置，可以插入占位符。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="5b3c1-179">向用户显示通知时，占位符由适当的数据代替。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="5b3c1-180">按照以下步骤插入占位符：</span><span class="sxs-lookup"><span data-stu-id="5b3c1-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="5b3c1-181">在文本框中，单击应该出现占位符的位置。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="5b3c1-182">单击 **插入占位符**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="5b3c1-183">在出现的列表中，选择要插入的占位符。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="5b3c1-184">单击 **插入**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-184">Click **Insert**.</span></span>

6. <span data-ttu-id="5b3c1-185">若要添加通知的翻译，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="5b3c1-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="5b3c1-186">单击 **翻译**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="5b3c1-187">在出现的页面上，单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="5b3c1-188">在出现的列表中，选择您输入文本使用的语言。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="5b3c1-189">在 **已翻译的文本** 字段中，输入文本。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="5b3c1-190">如果要对文本进行个性化设置，可以如步骤 5 所述插入占位符。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="5b3c1-191">单击 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-191">Click **Close**.</span></span>

7. <span data-ttu-id="5b3c1-192">在 **接收人** 选项卡上，指定向谁发送通知。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="5b3c1-193">选择下表中的选项之一，然后按照该选项的其他步骤转到第 8 步。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="5b3c1-194">选项</span><span class="sxs-lookup"><span data-stu-id="5b3c1-194">Option</span></span></th>
    <th><span data-ttu-id="5b3c1-195">通知收件人。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="5b3c1-196">附加步骤</span><span class="sxs-lookup"><span data-stu-id="5b3c1-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="5b3c1-197">参与者</span><span class="sxs-lookup"><span data-stu-id="5b3c1-197">Participant</span></span></td>
    <td><span data-ttu-id="5b3c1-198">分配到特定组或角色的用户</span><span class="sxs-lookup"><span data-stu-id="5b3c1-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5b3c1-199">在您选择<strong>参与者</strong>后，在选项卡<strong>基于角色</strong>上，在<strong>参与者类型</strong>列表中，选择要向其发送通知的组或角色的类型。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="5b3c1-200">在<strong>参与者</strong>列表中，选择向其发送通知的组。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5b3c1-201">工作流用户</span><span class="sxs-lookup"><span data-stu-id="5b3c1-201">Workflow user</span></span></td>
    <td><span data-ttu-id="5b3c1-202">当前工作流中的用户</span><span class="sxs-lookup"><span data-stu-id="5b3c1-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="5b3c1-203">在您选择<strong>工作流用户</strong>后，在选项卡<strong>工作流用户</strong>上，在<strong>工作流用户</strong>列表中，选择参与工作流的用户。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5b3c1-204">用户</span><span class="sxs-lookup"><span data-stu-id="5b3c1-204">User</span></span></td>
    <td><span data-ttu-id="5b3c1-205">特定用户</span><span class="sxs-lookup"><span data-stu-id="5b3c1-205">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5b3c1-206">在选择<strong>用户</strong>后，单击<strong>用户</strong>选项卡。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="5b3c1-207"><strong>可用用户</strong>列表包含所有用户。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-207">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="5b3c1-208">选择向其发送通知的用户，然后将这些用户移动到<strong>所选用户</strong>列表中。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="5b3c1-209">对您在第 2 步中选择的每个事件重复 第 3 步到第 7 步。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="5b3c1-210">分配决策</span><span class="sxs-lookup"><span data-stu-id="5b3c1-210">Assign a decision</span></span>

<span data-ttu-id="5b3c1-211">按照以下步骤指定应向手动决策分配的人员。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="5b3c1-212">在左窗格中，单击 **分配**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="5b3c1-213">在 **分配类型** 选项卡上，选择下表中的选项之一，然后按照该选项的其他步骤转到步骤 3。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="5b3c1-214">选项</span><span class="sxs-lookup"><span data-stu-id="5b3c1-214">Option</span></span></th>
    <th><span data-ttu-id="5b3c1-215">决策分配到的用户</span><span class="sxs-lookup"><span data-stu-id="5b3c1-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="5b3c1-216">附加步骤</span><span class="sxs-lookup"><span data-stu-id="5b3c1-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="5b3c1-217">参与者</span><span class="sxs-lookup"><span data-stu-id="5b3c1-217">Participant</span></span></td>
    <td><span data-ttu-id="5b3c1-218">分配到特定组或角色的用户</span><span class="sxs-lookup"><span data-stu-id="5b3c1-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5b3c1-219">在您选择<strong>参与者</strong>后，在选项卡<strong>基于角色</strong>上，在<strong>参与者类型</strong>列表中，选择要向其分配决策的组或角色的类型。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="5b3c1-220">在<strong>参与者</strong>列表中，选择向其分配决策的组或角色的类型。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5b3c1-221">层次结构</span><span class="sxs-lookup"><span data-stu-id="5b3c1-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="5b3c1-222">特定组织层次结构中的用户</span><span class="sxs-lookup"><span data-stu-id="5b3c1-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5b3c1-223">在您选择<strong>层次结构</strong>后，在选项卡<strong>层次结构选择</strong>上，在<strong>层次结构类型</strong>列表中，选择要向其分配决策的层次结构的类型。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="5b3c1-224">系统必须从层次结构中检索一系列用户姓名。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="5b3c1-225">这些姓名代表可向其分配决策的用户。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="5b3c1-226">按照以下步骤指定系统检索的用户名范围的起点和终点：</span><span class="sxs-lookup"><span data-stu-id="5b3c1-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="5b3c1-227">若要指定起点，请在<strong>启动自</strong>列表中选择一名人员。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="5b3c1-228">若要指定终点，请单击<strong>添加条件</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="5b3c1-229">然后输入一个确定系统停止检索姓名的层次结构的条件。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="5b3c1-230">在<strong>层次结构选项</strong>选项卡上，指定应向其分配决策的范围内的用户：</span><span class="sxs-lookup"><span data-stu-id="5b3c1-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="5b3c1-231"><strong>分配给所有检索到的用户</strong> – 此决策将分配给范围内的所有用户。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="5b3c1-232"><strong>仅分配给最后检索到的用户</strong> – 此决策将分配给范围内的最后一名用户。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="5b3c1-233"><strong>排除满足以下条件的用户</strong> – 此决策不分配给满足特定条件的范围内的所有用户。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="5b3c1-234">单击<strong>添加条件</strong>以指定条件。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5b3c1-235">工作流用户</span><span class="sxs-lookup"><span data-stu-id="5b3c1-235">Workflow user</span></span></td>
    <td><span data-ttu-id="5b3c1-236">当前工作流中的用户</span><span class="sxs-lookup"><span data-stu-id="5b3c1-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="5b3c1-237">在您选择<strong>工作流用户</strong>后，在选项卡<strong>工作流用户</strong>上，在<strong>工作流用户</strong>列表中，选择参与工作流的用户。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5b3c1-238">用户</span><span class="sxs-lookup"><span data-stu-id="5b3c1-238">User</span></span></td>
    <td><span data-ttu-id="5b3c1-239">特定用户</span><span class="sxs-lookup"><span data-stu-id="5b3c1-239">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5b3c1-240">在选择<strong>用户</strong>后，单击<strong>用户</strong>选项卡。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="5b3c1-241"><strong>可用用户</strong>列表包含所有用户。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-241">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="5b3c1-242">选择要向其分配决策的用户，然后将这些用户移动到<strong>所选用户</strong>列表。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="5b3c1-243">在 **时间限制** 选项卡上，在 **持续时间** 字段中，指定指定用户必须在多长时间内制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-243">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="5b3c1-244">选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="5b3c1-244">Select one of the following options:</span></span>

    - <span data-ttu-id="5b3c1-245">**小时** – 输入用户必须在几小时内制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-245">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="5b3c1-246">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-246">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="5b3c1-247">**天** – 输入用户必须在几天内制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-247">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="5b3c1-248">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-248">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="5b3c1-249">**周** – 输入用户必须在几周内制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-249">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="5b3c1-250">**月** – 选择用户必须在哪一天和哪一周前制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-250">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="5b3c1-251">例如，您可能希望用户在当月第三周的周五之前制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-251">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="5b3c1-252">**年** – 选择用户必须在哪一天、哪一周和哪一月前制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-252">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="5b3c1-253">例如，您可能希望用户在十二月的第三周的周五之前制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-253">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="5b3c1-254">如果用户未在分配的时间内制定决策，则决策逾期。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-254">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="5b3c1-255">逾期的决策基于您在此页面 **呈报** 区域中选择的选项呈报。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-255">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="5b3c1-256">指定决策逾期时执行的操作</span><span class="sxs-lookup"><span data-stu-id="5b3c1-256">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="5b3c1-257">如果用户未在分配的时间内制定决策，则决策逾期。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-257">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="5b3c1-258">可呈报逾期的决策，或自动将该单据分配给其他用户。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-258">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="5b3c1-259">如果决策逾期，请执行以下步骤进行呈报。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-259">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="5b3c1-260">在左窗格中，单击 **呈报**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-260">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="5b3c1-261">选择 **使用呈报路线** 复选框创建呈报路线。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-261">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="5b3c1-262">系统自动将决策分配给呈报路线中列出的用户。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-262">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="5b3c1-263">例如，下表显示呈报路线。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-263">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="5b3c1-264">序列</span><span class="sxs-lookup"><span data-stu-id="5b3c1-264">Sequence</span></span> | <span data-ttu-id="5b3c1-265">呈报路线</span><span class="sxs-lookup"><span data-stu-id="5b3c1-265">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="5b3c1-266">1</span><span class="sxs-lookup"><span data-stu-id="5b3c1-266">1</span></span>        | <span data-ttu-id="5b3c1-267">分配给：Donna</span><span class="sxs-lookup"><span data-stu-id="5b3c1-267">Assign to: Donna</span></span>           |
    | <span data-ttu-id="5b3c1-268">2</span><span class="sxs-lookup"><span data-stu-id="5b3c1-268">2</span></span>        | <span data-ttu-id="5b3c1-269">分配给：Erin</span><span class="sxs-lookup"><span data-stu-id="5b3c1-269">Assign to: Erin</span></span>            |
    | <span data-ttu-id="5b3c1-270">3</span><span class="sxs-lookup"><span data-stu-id="5b3c1-270">3</span></span>        | <span data-ttu-id="5b3c1-271">最后操作：\[选择 1\]</span><span class="sxs-lookup"><span data-stu-id="5b3c1-271">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="5b3c1-272">在此示例中，系统将逾期决策分配给 Donna。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-272">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="5b3c1-273">如果 Donna 未在分配的时间内制定决策，则系统将决策分配给 Erin。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-273">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="5b3c1-274">如果 Erin 未在分配的时间内制定决策，则系统选择 **\[选择 1\]** 作为决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-274">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="5b3c1-275">要将用户添加到呈报路线中，单击 **添加呈报**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-275">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="5b3c1-276">选择下表中的选项之一，然后按照该选项的其他步骤转到第 4 步。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-276">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="5b3c1-277">选项</span><span class="sxs-lookup"><span data-stu-id="5b3c1-277">Option</span></span></th>
    <th><span data-ttu-id="5b3c1-278">决策呈报到的用户</span><span class="sxs-lookup"><span data-stu-id="5b3c1-278">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="5b3c1-279">附加步骤</span><span class="sxs-lookup"><span data-stu-id="5b3c1-279">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="5b3c1-280">层次结构</span><span class="sxs-lookup"><span data-stu-id="5b3c1-280">Hierarchy</span></span></td>
    <td><span data-ttu-id="5b3c1-281">特定组织层次结构中的用户</span><span class="sxs-lookup"><span data-stu-id="5b3c1-281">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5b3c1-282">在您选择<strong>层次结构</strong>后，在选项卡<strong>层次结构选择</strong>上，在<strong>层次结构类型</strong>列表中，选择要向其呈报决策的层次结构的类型。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-282">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="5b3c1-283">系统必须从层次结构中检索一系列用户姓名。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-283">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="5b3c1-284">这些姓名代表可向其呈报决策的用户。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-284">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="5b3c1-285">按照以下步骤指定系统检索的用户名范围的起点和终点：</span><span class="sxs-lookup"><span data-stu-id="5b3c1-285">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="5b3c1-286">若要指定起点，请在<strong>启动自</strong>列表中选择一名人员。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-286">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="5b3c1-287">若要指定终点，请单击<strong>添加条件</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-287">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="5b3c1-288">然后输入一个确定系统停止检索姓名的层次结构的条件。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-288">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="5b3c1-289">在<strong>层次结构选项</strong>选项卡上，指定应向其呈报决策的范围内的用户：</span><span class="sxs-lookup"><span data-stu-id="5b3c1-289">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="5b3c1-290"><strong>分配给所有检索到的用户</strong> – 决策将呈报给范围内的所有用户。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-290"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="5b3c1-291"><strong>仅分配给最后检索到的用户</strong> – 决策将呈报给范围内的最后一名用户。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-291"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="5b3c1-292"><strong>排除满足以下条件的用户：</strong> – 此决策不呈报给满足特定条件的范围内的所有用户。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-292"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="5b3c1-293">单击<strong>添加条件</strong>以指定条件。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-293">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5b3c1-294">工作流用户</span><span class="sxs-lookup"><span data-stu-id="5b3c1-294">Workflow user</span></span></td>
    <td><span data-ttu-id="5b3c1-295">当前工作流中的用户</span><span class="sxs-lookup"><span data-stu-id="5b3c1-295">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="5b3c1-296">在您选择<strong>工作流用户</strong>后，在选项卡<strong>工作流用户</strong>上，在<strong>工作流用户</strong>列表中，选择参与工作流的用户。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-296">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5b3c1-297">用户</span><span class="sxs-lookup"><span data-stu-id="5b3c1-297">User</span></span></td>
    <td><span data-ttu-id="5b3c1-298">特定用户</span><span class="sxs-lookup"><span data-stu-id="5b3c1-298">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5b3c1-299">在选择<strong>用户</strong>后，单击<strong>用户</strong>选项卡。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-299">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="5b3c1-300"><strong>可用用户</strong>列表包含所有用户。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-300">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="5b3c1-301">选择要向其呈报决策的用户，然后将这些用户移动到<strong>所选用户</strong>列表。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-301">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="5b3c1-302">在 **时间限制** 选项卡上，在 **持续时间** 字段中，指定指定用户必须在多长时间内制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-302">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="5b3c1-303">选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="5b3c1-303">Select one of the following options:</span></span>

    - <span data-ttu-id="5b3c1-304">**小时** – 输入用户必须在几小时内制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-304">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="5b3c1-305">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-305">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="5b3c1-306">**天** – 输入用户必须在几天内制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-306">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="5b3c1-307">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-307">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="5b3c1-308">**周** – 输入用户必须在几周内制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-308">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="5b3c1-309">**月** – 选择用户必须在哪一天和哪一周前制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-309">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="5b3c1-310">例如，您可能希望用户在当月第三周的周五之前制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-310">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="5b3c1-311">**年** – 选择用户必须在哪一天、哪一周和哪一月前制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-311">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="5b3c1-312">例如，您可能希望用户在十二月的第三周的周五之前制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-312">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="5b3c1-313">对每个应添加到呈报路线的用户重复第 3 步到第 4 步。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-313">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="5b3c1-314">您可以更改用户的顺序。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-314">You can change the order of the users.</span></span>
6. <span data-ttu-id="5b3c1-315">如果呈报路线中的用户未在分配的时间内制定决策，则系统制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-315">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="5b3c1-316">若要指定系统选择的选项，选择 **操作** 行，然后，在 **结束操作** 选项卡上，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-316">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="5b3c1-317">设置时间限制</span><span class="sxs-lookup"><span data-stu-id="5b3c1-317">Set a time limit</span></span>

<span data-ttu-id="5b3c1-318">如果必须在特定时间制定决策，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-318">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="5b3c1-319">您在此过程中选择的选项将覆盖您在页面的 **分配** 和 **呈报** 区域选择的选项。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-319">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="5b3c1-320">在左侧窗格中，单击 **高级设置**。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-320">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="5b3c1-321">选中 **为工作流元素设置时间限制** 复选框。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-321">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="5b3c1-322">在 **持续时间** 字段中，指定必须在何时制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-322">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="5b3c1-323">选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="5b3c1-323">Select one of the following options:</span></span>

    - <span data-ttu-id="5b3c1-324">**小时** – 输入小时数。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-324">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="5b3c1-325">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-325">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="5b3c1-326">**天** – 输入天数。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-326">**Days** – Enter the number of days.</span></span> <span data-ttu-id="5b3c1-327">然后选择您的组织使用的日历，并输入有关您的组织的工作周的信息。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-327">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="5b3c1-328">**周** – 输入周数。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-328">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="5b3c1-329">**月** – 选择必须在哪一天和哪一周前制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-329">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="5b3c1-330">例如，您可能希望决策在当月第三周的周五之前制定。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-330">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="5b3c1-331">**年** – 选择决策必须在哪一天、哪一周和哪一月前制定。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-331">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="5b3c1-332">例如，您可能希望决策在十二月第三周的周五之前制定。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-332">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="5b3c1-333">如果超出时间限制，系统将制定决策。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-333">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="5b3c1-334">在 **操作** 列表中选择系统应选择的选项。</span><span class="sxs-lookup"><span data-stu-id="5b3c1-334">In the **Action** list, select the option that the system should select.</span></span>

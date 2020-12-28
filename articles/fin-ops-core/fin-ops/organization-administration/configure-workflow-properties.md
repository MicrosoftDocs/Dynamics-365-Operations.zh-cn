---
title: 配置工作流属性
description: 本主题说明如何配置工作流的各个属性。
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bd3c9bea010099f83d16dad70261bc2d46a1dac
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693274"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="334aa-103">配置工作流属性</span><span class="sxs-lookup"><span data-stu-id="334aa-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="334aa-104">本主题说明如何配置工作流的各个属性。</span><span class="sxs-lookup"><span data-stu-id="334aa-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="334aa-105">要配置工作流的属性，在工作流编辑器中打开工作流。</span><span class="sxs-lookup"><span data-stu-id="334aa-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="334aa-106">单击工作流编辑器的画布，并随后单击 **属性** 以打开 **属性** 页面。</span><span class="sxs-lookup"><span data-stu-id="334aa-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="334aa-107">然后可以使用以下过程配置工作流的各个属性。</span><span class="sxs-lookup"><span data-stu-id="334aa-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="334aa-108">为工作流命名</span><span class="sxs-lookup"><span data-stu-id="334aa-108">Name the workflow</span></span>

<span data-ttu-id="334aa-109">按照以下步骤为工作流输入名称。</span><span class="sxs-lookup"><span data-stu-id="334aa-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="334aa-110">在左侧窗格中，单击 **基本设置**。</span><span class="sxs-lookup"><span data-stu-id="334aa-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="334aa-111">在 **名称** 字段中，为工作流输入唯一名称。</span><span class="sxs-lookup"><span data-stu-id="334aa-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="334aa-112">例如，如果您运营所在的每个国家/地区创建采购申请工作流，则您可将采购申请工作流命名为 **丹麦采购申请** 或 **西班牙采购申请**。</span><span class="sxs-lookup"><span data-stu-id="334aa-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="334aa-113">指定工作流所有者</span><span class="sxs-lookup"><span data-stu-id="334aa-113">Specify the workflow owner</span></span>

<span data-ttu-id="334aa-114">工作流所有者是管理和维护此工作流的人员。</span><span class="sxs-lookup"><span data-stu-id="334aa-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="334aa-115">按照以下步骤来指定工作流所有者。</span><span class="sxs-lookup"><span data-stu-id="334aa-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="334aa-116">在左侧窗格中，单击 **基本设置**。</span><span class="sxs-lookup"><span data-stu-id="334aa-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="334aa-117">在 **所有者** 列表中，选择将要管理此工作流的人员的姓名。</span><span class="sxs-lookup"><span data-stu-id="334aa-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="334aa-118">选择电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="334aa-118">Select an email template</span></span>

<span data-ttu-id="334aa-119">按照以下步骤选择用于生成有关此工作流的通知消息的电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="334aa-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="334aa-120">在左侧窗格中，单击 **基本设置**。</span><span class="sxs-lookup"><span data-stu-id="334aa-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="334aa-121">在 **工作流通知的电子邮件模板** 列表中，选择该模板。</span><span class="sxs-lookup"><span data-stu-id="334aa-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="334aa-122">输入用户说明。</span><span class="sxs-lookup"><span data-stu-id="334aa-122">Enter instructions for users</span></span>

<span data-ttu-id="334aa-123">您可向提交文档供处理和审核的用户提供说明。</span><span class="sxs-lookup"><span data-stu-id="334aa-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="334aa-124">这些用户也称为 *发起方*。</span><span class="sxs-lookup"><span data-stu-id="334aa-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="334aa-125">例如，您正在创建采购申请工作流，并且输入说明。</span><span class="sxs-lookup"><span data-stu-id="334aa-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="334aa-126">这些说明随后可供在 **采购申请** 页中输入采购申请的用户查看。</span><span class="sxs-lookup"><span data-stu-id="334aa-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="334aa-127">要查看说明，发起方单击工作流消息栏中的图标。</span><span class="sxs-lookup"><span data-stu-id="334aa-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="334aa-128">按照以下步骤输入用户说明。</span><span class="sxs-lookup"><span data-stu-id="334aa-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="334aa-129">在左侧窗格中，单击 **基本设置**。</span><span class="sxs-lookup"><span data-stu-id="334aa-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="334aa-130">在 **提交说明** 字段中，输入说明。</span><span class="sxs-lookup"><span data-stu-id="334aa-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="334aa-131">要对说明进行个性化设置，可以插入占位符。</span><span class="sxs-lookup"><span data-stu-id="334aa-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="334aa-132">向用户显示说明时，占位符由适当的数据代替。</span><span class="sxs-lookup"><span data-stu-id="334aa-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="334aa-133">按照以下步骤插入占位符：</span><span class="sxs-lookup"><span data-stu-id="334aa-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="334aa-134">在 **提交说明** 字段中单击以指定应该出现占位符的位置。</span><span class="sxs-lookup"><span data-stu-id="334aa-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="334aa-135">单击 **插入占位符**。</span><span class="sxs-lookup"><span data-stu-id="334aa-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="334aa-136">在出现的列表中，选择要插入的占位符。</span><span class="sxs-lookup"><span data-stu-id="334aa-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="334aa-137">单击 **插入**。</span><span class="sxs-lookup"><span data-stu-id="334aa-137">Click **Insert**.</span></span>

4. <span data-ttu-id="334aa-138">若要添加说明的翻译，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="334aa-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="334aa-139">单击 **翻译**。</span><span class="sxs-lookup"><span data-stu-id="334aa-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="334aa-140">在出现的页面上，单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="334aa-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="334aa-141">在出现的列表中，选择您输入文本将使用的语言。</span><span class="sxs-lookup"><span data-stu-id="334aa-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="334aa-142">在 **已翻译的文本** 字段中，输入文本。</span><span class="sxs-lookup"><span data-stu-id="334aa-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="334aa-143">要对文本进行个性化设置，可以插入占位符。</span><span class="sxs-lookup"><span data-stu-id="334aa-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="334aa-144">有关如何输入占位符的说明，请参阅步骤 3。</span><span class="sxs-lookup"><span data-stu-id="334aa-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="334aa-145">单击 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="334aa-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a><span data-ttu-id="334aa-146">通过激活条件指定何时使用此工作流</span><span class="sxs-lookup"><span data-stu-id="334aa-146">Specify when this workflow is used through activation conditions</span></span>

<span data-ttu-id="334aa-147">可以创建基于同一工作流类型的多个工作流。</span><span class="sxs-lookup"><span data-stu-id="334aa-147">You can create multiple workflows that are based on the same workflow type.</span></span> <span data-ttu-id="334aa-148">有多个工作流基于同一类型时，必须使用激活条件指定何时使用各个工作流。</span><span class="sxs-lookup"><span data-stu-id="334aa-148">When you have multiple workflows that are based on the same type, you must specify when each workflow is used using activation conditions.</span></span> <span data-ttu-id="334aa-149">如果不满足激活条件，则使用默认工作流。</span><span class="sxs-lookup"><span data-stu-id="334aa-149">If activation conditions are not met, then the default workflow is used.</span></span> <span data-ttu-id="334aa-150">同样，如果为某个工作流类型仅定义一个工作流配置，则无论哪种激活条件，都将使用该工作流配置。</span><span class="sxs-lookup"><span data-stu-id="334aa-150">Similarly, if there is only one workflow configuration defined for a workflow type, then that workflow configuration will be used regardless of the activation conditions.</span></span>

<span data-ttu-id="334aa-151">例如，可以为您运营所在的每个国家/地区创建采用以下条件的采购申请工作流，如“丹麦采购申请”和“西班牙采购申请”：</span><span class="sxs-lookup"><span data-stu-id="334aa-151">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain, with the following conditions:</span></span>

- <span data-ttu-id="334aa-152">在以下情况下使用丹麦采购申请：国家/地区 = DK。</span><span class="sxs-lookup"><span data-stu-id="334aa-152">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="334aa-153">在以下情况下使用西班牙采购申请：国家/地区 = ES。</span><span class="sxs-lookup"><span data-stu-id="334aa-153">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="334aa-154">按照以下步骤可以指定在何时使用正在配置的工作流。</span><span class="sxs-lookup"><span data-stu-id="334aa-154">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="334aa-155">在左窗格中，单击 **启用**。</span><span class="sxs-lookup"><span data-stu-id="334aa-155">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="334aa-156">选中 **设置运行此工作流的条件** 复选框。</span><span class="sxs-lookup"><span data-stu-id="334aa-156">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="334aa-157">单击 **添加条件**。</span><span class="sxs-lookup"><span data-stu-id="334aa-157">Click **Add condition**.</span></span>
4. <span data-ttu-id="334aa-158">输入条件。</span><span class="sxs-lookup"><span data-stu-id="334aa-158">Enter a condition.</span></span>
5. <span data-ttu-id="334aa-159">输入需要的任何其他条件。</span><span class="sxs-lookup"><span data-stu-id="334aa-159">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="334aa-160">在工作流中运行一些目标记录来验证条件是否正确包含和排除了记录。</span><span class="sxs-lookup"><span data-stu-id="334aa-160">Run through the workflow with some target records to verify that the condition correctly includes and excludes records.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="334aa-161">指定发送通知的时间</span><span class="sxs-lookup"><span data-stu-id="334aa-161">Specify when notifications are sent</span></span>

<span data-ttu-id="334aa-162">提交文档进行处理时，将创建工作流实例。</span><span class="sxs-lookup"><span data-stu-id="334aa-162">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="334aa-163">您可以在启动、完成、终止或因错误停止基于此工作流的工作流实例时，向用户发送通知。</span><span class="sxs-lookup"><span data-stu-id="334aa-163">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="334aa-164">按照以下步骤指定何时发送通知。</span><span class="sxs-lookup"><span data-stu-id="334aa-164">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="334aa-165">在左窗格中，单击 **通知**。</span><span class="sxs-lookup"><span data-stu-id="334aa-165">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="334aa-166">为应触发通知的每个事件选中该复选框：</span><span class="sxs-lookup"><span data-stu-id="334aa-166">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="334aa-167">**已启动** – 在工作流实例启动时发送通知。</span><span class="sxs-lookup"><span data-stu-id="334aa-167">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="334aa-168">**已停止** – 在工作流实例因错误停止时发送通知。</span><span class="sxs-lookup"><span data-stu-id="334aa-168">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="334aa-169">**已完成** – 在完成工作流实例时发送通知。</span><span class="sxs-lookup"><span data-stu-id="334aa-169">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="334aa-170">**无法恢复** – 在工作流实例因无法恢复的错误停止时发送通知。</span><span class="sxs-lookup"><span data-stu-id="334aa-170">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="334aa-171">**已终止** – 在工作流终止时发送通知。</span><span class="sxs-lookup"><span data-stu-id="334aa-171">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="334aa-172">为您在第 2 步中选择的事件选择行。</span><span class="sxs-lookup"><span data-stu-id="334aa-172">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="334aa-173">在 **通知文本** 选项卡上，输入通知的文本。</span><span class="sxs-lookup"><span data-stu-id="334aa-173">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="334aa-174">要对文本进行个性化设置，可以插入占位符。</span><span class="sxs-lookup"><span data-stu-id="334aa-174">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="334aa-175">向用户显示文本时，占位符由适当的数据代替。</span><span class="sxs-lookup"><span data-stu-id="334aa-175">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="334aa-176">按照以下步骤插入占位符：</span><span class="sxs-lookup"><span data-stu-id="334aa-176">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="334aa-177">在字段中单击以指定应该出现占位符的位置。</span><span class="sxs-lookup"><span data-stu-id="334aa-177">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="334aa-178">单击 **插入占位符**。</span><span class="sxs-lookup"><span data-stu-id="334aa-178">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="334aa-179">在出现的列表中，选择要插入的占位符。</span><span class="sxs-lookup"><span data-stu-id="334aa-179">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="334aa-180">单击 **插入**。</span><span class="sxs-lookup"><span data-stu-id="334aa-180">Click **Insert**.</span></span>
    5. <span data-ttu-id="334aa-181">下面是要添加的常见 **通知文本** 占位符：“最近注释：%Workflow.Last note%”，用于显示上一步中的任何注释。</span><span class="sxs-lookup"><span data-stu-id="334aa-181">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="334aa-182">若要添加文本的翻译，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="334aa-182">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="334aa-183">单击 **翻译**。</span><span class="sxs-lookup"><span data-stu-id="334aa-183">Click **Translations**.</span></span>
    2. <span data-ttu-id="334aa-184">在出现的页面上，单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="334aa-184">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="334aa-185">在出现的列表中，选择您输入文本将使用的语言。</span><span class="sxs-lookup"><span data-stu-id="334aa-185">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="334aa-186">在 **已翻译的文本** 字段中，输入文本。</span><span class="sxs-lookup"><span data-stu-id="334aa-186">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="334aa-187">要对文本进行个性化设置，可以插入占位符。</span><span class="sxs-lookup"><span data-stu-id="334aa-187">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="334aa-188">有关如何输入占位符的说明，请参阅步骤 5。</span><span class="sxs-lookup"><span data-stu-id="334aa-188">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="334aa-189">单击 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="334aa-189">Click **Close**.</span></span>

7. <span data-ttu-id="334aa-190">在 **接收人** 选项卡上，使用以下选项指定谁应接收通知。</span><span class="sxs-lookup"><span data-stu-id="334aa-190">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="334aa-191">选项</span><span class="sxs-lookup"><span data-stu-id="334aa-191">Option</span></span></th>
    <th><span data-ttu-id="334aa-192">通知发送给这些用户</span><span class="sxs-lookup"><span data-stu-id="334aa-192">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="334aa-193">要发送通知，请执行以下步骤</span><span class="sxs-lookup"><span data-stu-id="334aa-193">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="334aa-194">参与者</span><span class="sxs-lookup"><span data-stu-id="334aa-194">Participant</span></span></td>
    <td><span data-ttu-id="334aa-195">分配到特定组或角色的用户</span><span class="sxs-lookup"><span data-stu-id="334aa-195">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="334aa-196">在<strong>接收人</strong>选项卡上，单击<strong>参与者</strong>。</span><span class="sxs-lookup"><span data-stu-id="334aa-196">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="334aa-197">在<strong>基于角色</strong>选项卡上，在<strong>参与者类型</strong>列表中，选择要向其发送通知的组或角色的类型。</span><span class="sxs-lookup"><span data-stu-id="334aa-197">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="334aa-198">在<strong>参与者</strong>列表中，选择向其发送通知的组或角色。</span><span class="sxs-lookup"><span data-stu-id="334aa-198">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="334aa-199">工作流用户</span><span class="sxs-lookup"><span data-stu-id="334aa-199">Workflow user</span></span></td>
    <td><span data-ttu-id="334aa-200">参与者此工作流的用户</span><span class="sxs-lookup"><span data-stu-id="334aa-200">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="334aa-201">在<strong>接收人</strong>选项卡上，单击<strong>工作流用户</strong>。</span><span class="sxs-lookup"><span data-stu-id="334aa-201">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="334aa-202">在<strong>工作流用户</strong>选项卡上，在<strong>工作流用户</strong>列表中，选择此工作流中的参与者。</span><span class="sxs-lookup"><span data-stu-id="334aa-202">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="334aa-203">用户</span><span class="sxs-lookup"><span data-stu-id="334aa-203">User</span></span></td>
    <td><span data-ttu-id="334aa-204">特定用户</span><span class="sxs-lookup"><span data-stu-id="334aa-204">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="334aa-205">在<strong>接收人</strong>选项卡上，单击<strong>用户</strong>。</span><span class="sxs-lookup"><span data-stu-id="334aa-205">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="334aa-206">在<strong>用户</strong>选项卡上，<strong>可用用户</strong>列表包含所有用户。</span><span class="sxs-lookup"><span data-stu-id="334aa-206">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="334aa-207">选择向其发送通知的用户，然后将这些用户移动到<strong>所选用户</strong>列表中。</span><span class="sxs-lookup"><span data-stu-id="334aa-207">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="334aa-208">对您在第 2 步中选择的每个事件重复 第 3 步到第 7 步。</span><span class="sxs-lookup"><span data-stu-id="334aa-208">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="334aa-209">输入有关对此工作流进行的更改的注释</span><span class="sxs-lookup"><span data-stu-id="334aa-209">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="334aa-210">要输入有关对此工作流所做更改的注释，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="334aa-210">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="334aa-211">在左窗格中，单击 **注释**。</span><span class="sxs-lookup"><span data-stu-id="334aa-211">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="334aa-212">在 **输入有关工作流的注释** 字段中，输入注释。</span><span class="sxs-lookup"><span data-stu-id="334aa-212">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="334aa-213">请查看您的注释。</span><span class="sxs-lookup"><span data-stu-id="334aa-213">Review your comments.</span></span> <span data-ttu-id="334aa-214">在添加注释后，您不能修改注释。</span><span class="sxs-lookup"><span data-stu-id="334aa-214">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="334aa-215">单击 **添加** 将注释添加到 **注释历史记录** 区域。</span><span class="sxs-lookup"><span data-stu-id="334aa-215">Click **Add** to add your comments to the **Comment history** area.</span></span>

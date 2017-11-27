---
title: "配置工作流的属性"
description: "本主题说明如何配置工作流的各个属性。"
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5c24f6555508272b65aeb81c5a16a0bd2407f1b4
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="configure-the-properties-of-a-workflow"></a><span data-ttu-id="c870e-103">配置工作流的属性</span><span class="sxs-lookup"><span data-stu-id="c870e-103">Configure the properties of a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c870e-104">本主题说明如何配置工作流的各个属性。</span><span class="sxs-lookup"><span data-stu-id="c870e-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="c870e-105">要配置工作流的属性，在工作流编辑器中打开工作流。</span><span class="sxs-lookup"><span data-stu-id="c870e-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="c870e-106">单击工作流编辑器的画布，并随后单击**属性**以打开**属性**页面。</span><span class="sxs-lookup"><span data-stu-id="c870e-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="c870e-107">然后可以使用以下过程配置工作流的各个属性。</span><span class="sxs-lookup"><span data-stu-id="c870e-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="c870e-108">为工作流命名</span><span class="sxs-lookup"><span data-stu-id="c870e-108">Name the workflow</span></span>
<span data-ttu-id="c870e-109">按照以下步骤为工作流输入名称。</span><span class="sxs-lookup"><span data-stu-id="c870e-109">Follow these steps to enter a name for the workflow.</span></span>

1.  <span data-ttu-id="c870e-110">在左侧窗格中，单击**基本设置**。</span><span class="sxs-lookup"><span data-stu-id="c870e-110">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="c870e-111">在“**名称**”字段中，为工作流输入唯一名称。</span><span class="sxs-lookup"><span data-stu-id="c870e-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="c870e-112">例如，如果您运营所在的每个国家/地区创建采购申请工作流，则您可将采购申请工作流命名为**丹麦采购申请**或**西班牙采购申请**。</span><span class="sxs-lookup"><span data-stu-id="c870e-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="c870e-113">指定工作流所有者</span><span class="sxs-lookup"><span data-stu-id="c870e-113">Specify the workflow owner</span></span>
<span data-ttu-id="c870e-114">工作流所有者是管理和维护此工作流的人员。</span><span class="sxs-lookup"><span data-stu-id="c870e-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="c870e-115">按照以下步骤来指定工作流所有者。</span><span class="sxs-lookup"><span data-stu-id="c870e-115">Follow these steps to specify the workflow owner.</span></span>

1.  <span data-ttu-id="c870e-116">在左侧窗格中，单击**基本设置**。</span><span class="sxs-lookup"><span data-stu-id="c870e-116">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="c870e-117">在**所有者**列表中，选择将要管理此工作流的人员的姓名。</span><span class="sxs-lookup"><span data-stu-id="c870e-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="c870e-118">选择电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="c870e-118">Select an email template</span></span>
<span data-ttu-id="c870e-119">按照以下步骤选择用于生成有关此工作流的通知消息的电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="c870e-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1.  <span data-ttu-id="c870e-120">在左侧窗格中，单击**基本设置**。</span><span class="sxs-lookup"><span data-stu-id="c870e-120">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="c870e-121">在**工作流通知的电子邮件模板**列表中，选择该模板。</span><span class="sxs-lookup"><span data-stu-id="c870e-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="c870e-122">输入用户说明。</span><span class="sxs-lookup"><span data-stu-id="c870e-122">Enter instructions for users</span></span>
<span data-ttu-id="c870e-123">您可向提交文档供处理和审核的用户提供说明。</span><span class="sxs-lookup"><span data-stu-id="c870e-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="c870e-124">这些用户也称为*发起方*。</span><span class="sxs-lookup"><span data-stu-id="c870e-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="c870e-125">例如，您正在创建采购申请工作流，并且输入说明。</span><span class="sxs-lookup"><span data-stu-id="c870e-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="c870e-126">这些说明随后可供在**采购申请**页中输入采购申请的用户查看。</span><span class="sxs-lookup"><span data-stu-id="c870e-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="c870e-127">要查看说明，发起方单击工作流消息栏中的图标。</span><span class="sxs-lookup"><span data-stu-id="c870e-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="c870e-128">按照以下步骤输入用户说明。</span><span class="sxs-lookup"><span data-stu-id="c870e-128">Follow these steps to enter instructions for users.</span></span>

1.  <span data-ttu-id="c870e-129">在左侧窗格中，单击**基本设置**。</span><span class="sxs-lookup"><span data-stu-id="c870e-129">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="c870e-130">在**提交说明**字段中，输入说明。</span><span class="sxs-lookup"><span data-stu-id="c870e-130">In the **Submission instructions** field, enter the instructions.</span></span>
3.  <span data-ttu-id="c870e-131">要对说明进行个性化设置，可以插入占位符。</span><span class="sxs-lookup"><span data-stu-id="c870e-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="c870e-132">向用户显示说明时，占位符由适当的数据代替。</span><span class="sxs-lookup"><span data-stu-id="c870e-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="c870e-133">按照以下步骤插入占位符：</span><span class="sxs-lookup"><span data-stu-id="c870e-133">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="c870e-134">在**提交说明**字段中单击以指定应该出现占位符的位置。</span><span class="sxs-lookup"><span data-stu-id="c870e-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="c870e-135">单击**插入占位符**。</span><span class="sxs-lookup"><span data-stu-id="c870e-135">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="c870e-136">在出现的列表中，选择要插入的占位符。</span><span class="sxs-lookup"><span data-stu-id="c870e-136">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="c870e-137">单击“**插入**”。</span><span class="sxs-lookup"><span data-stu-id="c870e-137">Click **Insert**.</span></span>

4.  <span data-ttu-id="c870e-138">若要添加说明的翻译，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="c870e-138">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="c870e-139">单击**翻译**。</span><span class="sxs-lookup"><span data-stu-id="c870e-139">Click **Translations**.</span></span>
    2.  <span data-ttu-id="c870e-140">在出现的页面上，单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="c870e-140">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="c870e-141">在出现的列表中，选择您输入文本将使用的语言。</span><span class="sxs-lookup"><span data-stu-id="c870e-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="c870e-142">在**已翻译的文本**字段中，输入文本。</span><span class="sxs-lookup"><span data-stu-id="c870e-142">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="c870e-143">要对文本进行个性化设置，可以插入占位符。</span><span class="sxs-lookup"><span data-stu-id="c870e-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="c870e-144">有关如何输入占位符的说明，请参阅步骤 3。</span><span class="sxs-lookup"><span data-stu-id="c870e-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6.  <span data-ttu-id="c870e-145">单击**“关闭”**。</span><span class="sxs-lookup"><span data-stu-id="c870e-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used"></a><span data-ttu-id="c870e-146">指定何时使用此工作流</span><span class="sxs-lookup"><span data-stu-id="c870e-146">Specify when this workflow is used</span></span>
<span data-ttu-id="c870e-147">可以创建基于同一类型的多个工作流。</span><span class="sxs-lookup"><span data-stu-id="c870e-147">You can create multiple workflows that are based on the same type.</span></span> <span data-ttu-id="c870e-148">例如，可以为您运营所在的每个国家/地区创建采购申请工作流，如“丹麦采购申请”和“西班牙采购申请”。</span><span class="sxs-lookup"><span data-stu-id="c870e-148">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain.</span></span> <span data-ttu-id="c870e-149">有多个工作流基于同一类型时，必须指定何时使用各个工作流。</span><span class="sxs-lookup"><span data-stu-id="c870e-149">When you have multiple workflows that are based on the same type, you must specify when each workflow is used.</span></span> <span data-ttu-id="c870e-150">继续上面的示例，您指定以下条件：</span><span class="sxs-lookup"><span data-stu-id="c870e-150">For the preceding example, you specify the following conditions:</span></span>

-   <span data-ttu-id="c870e-151">在以下情况下使用丹麦采购申请：国家/地区 = DK。</span><span class="sxs-lookup"><span data-stu-id="c870e-151">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
-   <span data-ttu-id="c870e-152">在以下情况下使用西班牙采购申请：国家/地区 = ES。</span><span class="sxs-lookup"><span data-stu-id="c870e-152">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="c870e-153">按照以下步骤可以指定在何时使用正在配置的工作流。</span><span class="sxs-lookup"><span data-stu-id="c870e-153">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1.  <span data-ttu-id="c870e-154">在左窗格中，单击**启用**。</span><span class="sxs-lookup"><span data-stu-id="c870e-154">In the left pane, click **Activation**.</span></span>
2.  <span data-ttu-id="c870e-155">选中**设置运行此工作流的条件**复选框。</span><span class="sxs-lookup"><span data-stu-id="c870e-155">Select the **Set the conditions for running this workflow** check box.</span></span>
3.  <span data-ttu-id="c870e-156">单击“**添加条件**”。</span><span class="sxs-lookup"><span data-stu-id="c870e-156">Click **Add condition**.</span></span>
4.  <span data-ttu-id="c870e-157">输入条件。</span><span class="sxs-lookup"><span data-stu-id="c870e-157">Enter a condition.</span></span>
5.  <span data-ttu-id="c870e-158">输入需要的任何其他条件。</span><span class="sxs-lookup"><span data-stu-id="c870e-158">Enter any additional conditions that are required.</span></span>
6.  <span data-ttu-id="c870e-159">要验证输入的条件是否正确设置，请按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="c870e-159">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="c870e-160">单击“**测试**”。</span><span class="sxs-lookup"><span data-stu-id="c870e-160">Click **Test**.</span></span>
    2.  <span data-ttu-id="c870e-161">在**测试工作流条件**页面，在**验证条件**区域，选择一条记录。</span><span class="sxs-lookup"><span data-stu-id="c870e-161">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="c870e-162">单击“**测试**”。</span><span class="sxs-lookup"><span data-stu-id="c870e-162">Click **Test**.</span></span> <span data-ttu-id="c870e-163">系统对该记录进行评估，判断其是否符合您指定的条件。</span><span class="sxs-lookup"><span data-stu-id="c870e-163">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="c870e-164">例如，如果您为西班牙创建采购申请工作流，页面的**验证条件**区域显示采购申请列表。</span><span class="sxs-lookup"><span data-stu-id="c870e-164">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="c870e-165">单击**测试**后，系统评估所选采购申请，以确定国家/地区是否为 ES。</span><span class="sxs-lookup"><span data-stu-id="c870e-165">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4.  <span data-ttu-id="c870e-166">单击**确定**或**取消**返回到**属性**页面。</span><span class="sxs-lookup"><span data-stu-id="c870e-166">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="c870e-167">指定发送通知的时间</span><span class="sxs-lookup"><span data-stu-id="c870e-167">Specify when notifications are sent</span></span>
<span data-ttu-id="c870e-168">提交文档进行处理时，将创建工作流实例。</span><span class="sxs-lookup"><span data-stu-id="c870e-168">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="c870e-169">您可以在启动、完成、终止或因错误停止基于此工作流的工作流实例时，向用户发送通知。</span><span class="sxs-lookup"><span data-stu-id="c870e-169">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="c870e-170">按照以下步骤指定何时发送通知。</span><span class="sxs-lookup"><span data-stu-id="c870e-170">Follow these steps to specify when notifications are sent.</span></span>

1.  <span data-ttu-id="c870e-171">在左窗格中，单击**通知**。</span><span class="sxs-lookup"><span data-stu-id="c870e-171">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="c870e-172">为应触发通知的每个事件选中该复选框：</span><span class="sxs-lookup"><span data-stu-id="c870e-172">Select the check box for each event that should trigger notifications:</span></span>
    -   <span data-ttu-id="c870e-173">**已启动** – 在工作流实例启动时发送通知。</span><span class="sxs-lookup"><span data-stu-id="c870e-173">**Started** – Send notifications when a workflow instance is started.</span></span>
    -   <span data-ttu-id="c870e-174">**已停止** – 在工作流实例因错误停止时发送通知。</span><span class="sxs-lookup"><span data-stu-id="c870e-174">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    -   <span data-ttu-id="c870e-175">**已完成** – 在完成工作流实例时发送通知。</span><span class="sxs-lookup"><span data-stu-id="c870e-175">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    -   <span data-ttu-id="c870e-176">**无法恢复** – 在工作流实例因无法恢复的错误停止时发送通知。</span><span class="sxs-lookup"><span data-stu-id="c870e-176">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    -   <span data-ttu-id="c870e-177">**已终止** – 在工作流终止时发送通知。</span><span class="sxs-lookup"><span data-stu-id="c870e-177">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3.  <span data-ttu-id="c870e-178">为您在第 2 步中选择的事件选择行。</span><span class="sxs-lookup"><span data-stu-id="c870e-178">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="c870e-179">在**通知文本**选项卡上，输入通知的文本。</span><span class="sxs-lookup"><span data-stu-id="c870e-179">On the **Notification text** tab, enter the text of the notification.</span></span>
5.  <span data-ttu-id="c870e-180">要对文本进行个性化设置，可以插入占位符。</span><span class="sxs-lookup"><span data-stu-id="c870e-180">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="c870e-181">向用户显示文本时，占位符由适当的数据代替。</span><span class="sxs-lookup"><span data-stu-id="c870e-181">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="c870e-182">按照以下步骤插入占位符：</span><span class="sxs-lookup"><span data-stu-id="c870e-182">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="c870e-183">在字段中单击以指定应该出现占位符的位置。</span><span class="sxs-lookup"><span data-stu-id="c870e-183">Click in the field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="c870e-184">单击**插入占位符**。</span><span class="sxs-lookup"><span data-stu-id="c870e-184">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="c870e-185">在出现的列表中，选择要插入的占位符。</span><span class="sxs-lookup"><span data-stu-id="c870e-185">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="c870e-186">单击“**插入**”。</span><span class="sxs-lookup"><span data-stu-id="c870e-186">Click **Insert**.</span></span>

6.  <span data-ttu-id="c870e-187">若要添加文本的翻译，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="c870e-187">To add translations of the text, follow these steps:</span></span>
    1.  <span data-ttu-id="c870e-188">单击**翻译**。</span><span class="sxs-lookup"><span data-stu-id="c870e-188">Click **Translations**.</span></span>
    2.  <span data-ttu-id="c870e-189">在出现的页面上，单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="c870e-189">On the page that appears, Click **Add**.</span></span>
    3.  <span data-ttu-id="c870e-190">在出现的列表中，选择您输入文本将使用的语言。</span><span class="sxs-lookup"><span data-stu-id="c870e-190">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="c870e-191">在**已翻译的文本**字段中，输入文本。</span><span class="sxs-lookup"><span data-stu-id="c870e-191">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="c870e-192">要对文本进行个性化设置，可以插入占位符。</span><span class="sxs-lookup"><span data-stu-id="c870e-192">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="c870e-193">有关如何输入占位符的说明，请参阅步骤 5。</span><span class="sxs-lookup"><span data-stu-id="c870e-193">For instructions about how to enter a placeholder, see step 5.</span></span>
    6.  <span data-ttu-id="c870e-194">单击**“关闭”**。</span><span class="sxs-lookup"><span data-stu-id="c870e-194">Click **Close**.</span></span>

7.  <span data-ttu-id="c870e-195">在**接收人**选项卡上，使用以下选项指定谁应接收通知。</span><span class="sxs-lookup"><span data-stu-id="c870e-195">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c870e-196">选项</span><span class="sxs-lookup"><span data-stu-id="c870e-196">Option</span></span></th>
    <th><span data-ttu-id="c870e-197">通知发送给这些用户</span><span class="sxs-lookup"><span data-stu-id="c870e-197">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="c870e-198">要发送通知，请执行以下步骤</span><span class="sxs-lookup"><span data-stu-id="c870e-198">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="c870e-199">参与者</span><span class="sxs-lookup"><span data-stu-id="c870e-199">Participant</span></span></td>
    <td><span data-ttu-id="c870e-200">分配到特定组或角色的用户</span><span class="sxs-lookup"><span data-stu-id="c870e-200">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="c870e-201">在<strong>接收人</strong>选项卡上，单击<strong>参与者</strong>。</span><span class="sxs-lookup"><span data-stu-id="c870e-201">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="c870e-202">在<strong>基于角色</strong>选项卡上，在<strong>参与者类型</strong>列表中，选择要向其发送通知的组或角色的类型。</span><span class="sxs-lookup"><span data-stu-id="c870e-202">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="c870e-203">在<strong>参与者</strong>列表中，选择向其发送通知的组或角色。</span><span class="sxs-lookup"><span data-stu-id="c870e-203">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="c870e-204">工作流用户</span><span class="sxs-lookup"><span data-stu-id="c870e-204">Workflow user</span></span></td>
    <td><span data-ttu-id="c870e-205">参与者此工作流的用户</span><span class="sxs-lookup"><span data-stu-id="c870e-205">Users who are participants in this workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="c870e-206">在<strong>接收人</strong>选项卡上，单击<strong>工作流用户</strong>。</span><span class="sxs-lookup"><span data-stu-id="c870e-206">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="c870e-207">在<strong>工作流用户</strong>选项卡上，在<strong>工作流用户</strong>列表中，选择此工作流中的参与者。</span><span class="sxs-lookup"><span data-stu-id="c870e-207">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="c870e-208">用户</span><span class="sxs-lookup"><span data-stu-id="c870e-208">User</span></span></td>
    <td><span data-ttu-id="c870e-209">特定 Finance and Operations 用户</span><span class="sxs-lookup"><span data-stu-id="c870e-209">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="c870e-210">在<strong>接收人</strong>选项卡上，单击<strong>用户</strong>。</span><span class="sxs-lookup"><span data-stu-id="c870e-210">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="c870e-211">在<strong>用户</strong>选项卡上，<strong>可用用户</strong>列表包含所有 Finance and Operations 用户。</span><span class="sxs-lookup"><span data-stu-id="c870e-211">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="c870e-212">选择向其发送通知的用户，然后将这些用户移动到<strong>所选用户</strong>列表中。</span><span class="sxs-lookup"><span data-stu-id="c870e-212">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="c870e-213">对您在第 2 步中选择的每个事件重复 第 3 步到第 7 步。</span><span class="sxs-lookup"><span data-stu-id="c870e-213">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="c870e-214">输入有关对此工作流进行的更改的注释</span><span class="sxs-lookup"><span data-stu-id="c870e-214">Enter comments about the changes that you made to the workflow</span></span>
<span data-ttu-id="c870e-215">要输入有关对此工作流所做更改的注释，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c870e-215">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1.  <span data-ttu-id="c870e-216">在左窗格中，单击**注释**。</span><span class="sxs-lookup"><span data-stu-id="c870e-216">In the left pane, click **Notes**.</span></span>
2.  <span data-ttu-id="c870e-217">在**输入有关工作流的注释**字段中，输入注释。</span><span class="sxs-lookup"><span data-stu-id="c870e-217">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3.  <span data-ttu-id="c870e-218">请查看您的注释。</span><span class="sxs-lookup"><span data-stu-id="c870e-218">Review your comments.</span></span> <span data-ttu-id="c870e-219">在添加注释后，您不能修改注释。</span><span class="sxs-lookup"><span data-stu-id="c870e-219">After you add comments, you can't modify them.</span></span>
4.  <span data-ttu-id="c870e-220">单击**添加**将注释添加到**注释历史记录**区域。</span><span class="sxs-lookup"><span data-stu-id="c870e-220">Click **Add** to add your comments to the **Comment history** area.</span></span>






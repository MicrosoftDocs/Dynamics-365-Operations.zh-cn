---
title: 波次执行通知
description: 本主题介绍波次执行通知并说明如何进行设置。
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 47f270b5fff37e8e231d8a9c4a011172df3d9385
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271369"
---
# <a name="wave-execution-notifications"></a><span data-ttu-id="9ffa0-103">波次执行通知</span><span class="sxs-lookup"><span data-stu-id="9ffa0-103">Wave execution notifications</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ffa0-104">*波次执行通知* 功能使用业务事件和操作中心来提供与波次执行相关的通知。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-104">The *Wave execution notifications* feature uses business events and the Action center to deliver notifications that are related to wave execution.</span></span> <span data-ttu-id="9ffa0-105">它使您可以指定生成通知的事件类型、生成通知的仓库以及接收通知的用户。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-105">It lets you specify the types of events that generate notifications, the warehouses that generate them, and the users who receive them.</span></span>

<span data-ttu-id="9ffa0-106">导航栏右侧的 **显示消息** 按钮（铃铛符号）指示操作中心消息何时对当前用户可用。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-106">The **Show messages** button (bell symbol) on the right side of the navigation bar indicates when an Action center message is available for the current user.</span></span> <span data-ttu-id="9ffa0-107">用户可以选择 **显示消息** 按钮以打开操作中心并查看消息。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-107">The user can select the **Show messages** button to open the Action center and review the messages.</span></span>

<span data-ttu-id="9ffa0-108">运行业务流程时，将发生业务事件。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-108">Business events occur when business processes are run.</span></span> <span data-ttu-id="9ffa0-109">业务流程由任务组成。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-109">Business processes are made up of tasks.</span></span> <span data-ttu-id="9ffa0-110">在业务流程中，参与其中的用户将执行业务操作以完成这些任务。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-110">During a business process, the users who participate in it perform business actions to complete those tasks.</span></span> <span data-ttu-id="9ffa0-111">业务事件提供一种机制，使外部系统可以从 Finance and Operations 应用程序中接收通知。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-111">Business events provide a mechanism that lets external systems receive notifications from Finance and Operations applications.</span></span> <span data-ttu-id="9ffa0-112">这样，系统可以执行业务操作以响应业务事件。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-112">In this way, the systems can perform business actions in response to the business events.</span></span> <span data-ttu-id="9ffa0-113">有关详细信息，请参阅[业务事件概述](../../fin-ops-core/dev-itpro/business-events/home-page.md)。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-113">For more information, see [Business events overview](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span></span>

## <a name="turn-on-the-wave-execution-notifications-feature"></a><span data-ttu-id="9ffa0-114">打开波次执行通知功能</span><span class="sxs-lookup"><span data-stu-id="9ffa0-114">Turn on the Wave execution notifications feature</span></span>

<span data-ttu-id="9ffa0-115">*波次执行通知* 功能只有在系统中打开之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-115">Before you can use the *Wave execution notifications* feature, it must be turned on in your system.</span></span> <span data-ttu-id="9ffa0-116">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="9ffa0-117">在那里，此功能以以下方式列出：</span><span class="sxs-lookup"><span data-stu-id="9ffa0-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="9ffa0-118">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="9ffa0-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="9ffa0-119">**功能名称**：*波次执行通知*</span><span class="sxs-lookup"><span data-stu-id="9ffa0-119">**Feature name:** *Wave execution notifications*</span></span>

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a><span data-ttu-id="9ffa0-120">场景：将波次批处理执行通知发送到操作中心</span><span class="sxs-lookup"><span data-stu-id="9ffa0-120">Scenario: Send wave batch execution notifications to the Action center</span></span>

<span data-ttu-id="9ffa0-121">此场景显示通过操作中心将有关波次批处理执行错误的通知发送给特定角色的端到端流。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-121">This scenario shows the end-to-end flow for sending notifications about wave batch execution errors to a specific role via the Action center.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="9ffa0-122">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="9ffa0-122">Make demo data available</span></span>

<span data-ttu-id="9ffa0-123">要采取此方案，必须安装演示数据，并且必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-123">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a><span data-ttu-id="9ffa0-124">确保在批处理模式下运行波次</span><span class="sxs-lookup"><span data-stu-id="9ffa0-124">Make sure that waves are run in batch mode</span></span>

1. <span data-ttu-id="9ffa0-125">转到 **仓库管理 \> 设置 \> 仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-125">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="9ffa0-126">在 **波次处理** 快速选项卡上，将 **批量处理波次** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-126">On the **Wave processing** FastTab, set the **Process waves in batch** option to *Yes*.</span></span>

> [!NOTE]
> <span data-ttu-id="9ffa0-127">如果要禁用波次批处理执行通知，请将 **禁用波次处理批处理通知** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-127">If you want to disable wave batch execution notifications, set the **Disable wave processing batch notifications** option to *Yes*.</span></span>

### <a name="configure-a-wave-notification-policy"></a><span data-ttu-id="9ffa0-128">配置波次通知策略</span><span class="sxs-lookup"><span data-stu-id="9ffa0-128">Configure a wave notification policy</span></span>

<span data-ttu-id="9ffa0-129">波次通知策略定义发送的通知类型和收到通知的用户。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-129">Wave notification policies define the types of notifications that are sent and the users who are notified.</span></span>

1. <span data-ttu-id="9ffa0-130">转到 **仓库管理 \> 设置 \> 波次 \> 波次通知策略**。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-130">Go to **Warehouse management \> Setup \> Waves \> Wave notification policies**.</span></span>
1. <span data-ttu-id="9ffa0-131">创建一个具有以下设置的记录：</span><span class="sxs-lookup"><span data-stu-id="9ffa0-131">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="9ffa0-132">**波次通知策略**：*24BatchError*</span><span class="sxs-lookup"><span data-stu-id="9ffa0-132">**Wave notification policy:** *24BatchError*</span></span>
    - <span data-ttu-id="9ffa0-133">**描述**：*仓库 24 波次批处理错误*</span><span class="sxs-lookup"><span data-stu-id="9ffa0-133">**Description:** *Warehouse 24 wave batch error*</span></span>
    - <span data-ttu-id="9ffa0-134">**发送以下通知**：*仅错误*</span><span class="sxs-lookup"><span data-stu-id="9ffa0-134">**Send notification on:** *Error only*</span></span>
    - <span data-ttu-id="9ffa0-135">**目标角色**：*系统管理员*</span><span class="sxs-lookup"><span data-stu-id="9ffa0-135">**To role:** *System administrator*</span></span>

        > [!NOTE]
        > <span data-ttu-id="9ffa0-136">由于此场景使用演示数据，因此为简单起见，选择 *系统管理员* 角色。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-136">Because this scenario uses demo data, the *System administrator* role is selected for the sake of simplicity.</span></span> <span data-ttu-id="9ffa0-137">由于您以系统管理员用户身份登录，因此您将收到通知。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-137">Therefore, because you're signed in as a system administrator user, you will receive the notifications.</span></span> <span data-ttu-id="9ffa0-138">但实际上，您通常应该选择一个更具体的角色（例如 *仓库经理*）来通知波次批处理执行错误。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-138">However, in practice, you should usually select a more specific role to notify about wave batch execution errors, such as *Warehouse manager*.</span></span>

1. <span data-ttu-id="9ffa0-139">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-139">On the Action Pane, select **Save**.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="9ffa0-140">配置波次模板</span><span class="sxs-lookup"><span data-stu-id="9ffa0-140">Configure a wave template</span></span>

<span data-ttu-id="9ffa0-141">波次模板使您可以将波次方法的特定实例链接到相应的波次标签模板。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-141">Wave templates let you link specific instances of wave methods to corresponding wave label templates.</span></span>

1. <span data-ttu-id="9ffa0-142">转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-142">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="9ffa0-143">在列表窗格中，将 **波次模板类型** 字段设置为 *装运*，然后为仓库 24 选择 *24 装运默认* 波次模板。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-143">In the list pane, set the **Wave template type** field to *Shipping*, and then select the *24 Shipping Default* wave template for warehouse 24.</span></span>
1. <span data-ttu-id="9ffa0-144">在 **常规** 快速选项卡上，将 **波次通知策略** 字段设置为 *24BatchError*。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-144">On the **General** FastTab, set the **Wave notification policy** field to *24BatchError*.</span></span>

### <a name="configure-a-work-template"></a><span data-ttu-id="9ffa0-145">配置工作模板</span><span class="sxs-lookup"><span data-stu-id="9ffa0-145">Configure a work template</span></span>

<span data-ttu-id="9ffa0-146">在波次执行期间使用工作模板生成工作。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-146">Work templates are used during wave execution to generate work.</span></span> <span data-ttu-id="9ffa0-147">对于这种情况，波次执行应触发错误。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-147">For this scenario, wave execution should trigger an error.</span></span> <span data-ttu-id="9ffa0-148">通过将工作模板查询设置为使用不存在的仓库，您将确保波次执行失败并因此发送通知。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-148">By setting the work template query to use a nonexistent warehouse, you will ensure that wave execution fails and therefore sends a notification.</span></span>

1. <span data-ttu-id="9ffa0-149">转到 **仓库管理 \> 设置 \> 工作 \> 工作模板**。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-149">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="9ffa0-150">在列表窗格中，将 **工作模板类型** 字段设置为 *销售订单*，然后为仓库 24 选择 *24 SO 阶段* 工作模板。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-150">In the list pane, set the **Work template type** field to *Sales orders* and then select the *24 SO Stage* work template for warehouse 24.</span></span>
1. <span data-ttu-id="9ffa0-151">在操作窗格上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-151">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="9ffa0-152">在查询编辑器对话框中，在 **范围** 选项卡上，编辑以下行（或添加行，如果不存在）：</span><span class="sxs-lookup"><span data-stu-id="9ffa0-152">In the query editor dialog box, on the **Range** tab, edit the following row (or add it if it doesn't exist):</span></span>

    - <span data-ttu-id="9ffa0-153">**表**：*临时工作事务*</span><span class="sxs-lookup"><span data-stu-id="9ffa0-153">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="9ffa0-154">**派生表**：*临时工作事务*</span><span class="sxs-lookup"><span data-stu-id="9ffa0-154">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="9ffa0-155">**字段**：*仓库*</span><span class="sxs-lookup"><span data-stu-id="9ffa0-155">**Field:** *Warehouse*</span></span>
    - <span data-ttu-id="9ffa0-156">**标准：** 将值从 *24* 更改为 *错误*。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-156">**Criteria:** Change the value from *24* to *Error*.</span></span>

1. <span data-ttu-id="9ffa0-157">选择 **确定**，然后确认更改。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-157">Select **OK**, and confirm the change.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="9ffa0-158">创建销售订单并将其下达到仓库</span><span class="sxs-lookup"><span data-stu-id="9ffa0-158">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="9ffa0-159">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-159">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="9ffa0-160">创建具有以下设置的销售订单：</span><span class="sxs-lookup"><span data-stu-id="9ffa0-160">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="9ffa0-161">**客户帐户**：*US-001*</span><span class="sxs-lookup"><span data-stu-id="9ffa0-161">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9ffa0-162">**仓库**：*24*</span><span class="sxs-lookup"><span data-stu-id="9ffa0-162">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="9ffa0-163">在 **销售订单行** 快速选项卡上，添加具有以下设置的销售订单行：</span><span class="sxs-lookup"><span data-stu-id="9ffa0-163">On the **Sales order lines** FastTab, add a sales order line that has the following settings:</span></span>

    - <span data-ttu-id="9ffa0-164">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="9ffa0-164">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="9ffa0-165">**数量：** *10*</span><span class="sxs-lookup"><span data-stu-id="9ffa0-165">**Quantity:** *10*</span></span>

    > [!NOTE]
    > <span data-ttu-id="9ffa0-166">这些物料和数量仅是示例。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-166">These items and quantities are only examples.</span></span> <span data-ttu-id="9ffa0-167">指定的仓库必须包含足够的存货。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-167">The specified warehouse must contain enough stock.</span></span>

1. <span data-ttu-id="9ffa0-168">在 **销售订单行** 快速选项卡上仍选择新行时，在工具栏上选择 **库存 \> 预留**。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-168">While the new line is still selected on the **Sales order lines** FastTab, select **Inventory \> Reservation** on the toolbar.</span></span>
1. <span data-ttu-id="9ffa0-169">在 **预留** 页的操作窗格中，选择 **预留批次**。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-169">On the **Reservation** page, on the Action Pane, select **Reserve lot**.</span></span> <span data-ttu-id="9ffa0-170">然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-170">Then close the page.</span></span>
1. <span data-ttu-id="9ffa0-171">在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-171">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

### <a name="notifications-from-wave-batch-job-execution"></a><span data-ttu-id="9ffa0-172">来自波次批处理作业执行的通知</span><span class="sxs-lookup"><span data-stu-id="9ffa0-172">Notifications from wave batch job execution</span></span>

<span data-ttu-id="9ffa0-173">根据业务事件的设置，您最终将收到有关波次执行失败的通知。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-173">Depending on the setup of your business events, you will eventually receive a notification about wave execution failure.</span></span> <span data-ttu-id="9ffa0-174">操作中心消息将类似于以下示例，并将包括指向失败波次的链接。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-174">The Action center message will resemble the following example and will include a link to the wave that failed.</span></span>

> <span data-ttu-id="9ffa0-175">**波次执行期间出错**</span><span class="sxs-lookup"><span data-stu-id="9ffa0-175">**Error during wave execution**</span></span>  
> <span data-ttu-id="9ffa0-176">执行波次 USMF-000000001 时出错。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-176">An error occurred while executing wave USMF-000000001.</span></span>  
> <span data-ttu-id="9ffa0-177">最新消息：没有为波次 USMF-000000001 创建任何工作。</span><span class="sxs-lookup"><span data-stu-id="9ffa0-177">Last messages: No Work was created for Wave USMF-000000001.</span></span>
>
> <span data-ttu-id="9ffa0-178">**状态**</span><span class="sxs-lookup"><span data-stu-id="9ffa0-178">**STATUS**</span></span>  
> <span data-ttu-id="9ffa0-179">可用</span><span class="sxs-lookup"><span data-stu-id="9ffa0-179">Active</span></span>
>
> <span data-ttu-id="9ffa0-180">打开波次详细信息</span><span class="sxs-lookup"><span data-stu-id="9ffa0-180">Open wave details</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

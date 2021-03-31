---
title: 库存操作故障排除
description: 此主题介绍如何解决使用库存操作时可能遇到的问题。
author: sherry-zheng
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: ee1bfbf1b5aa736e1ee5bd38403b6c94c2bd036b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224994"
---
# <a name="troubleshoot-inventory-operations"></a><span data-ttu-id="9fd48-103">库存操作故障排除</span><span class="sxs-lookup"><span data-stu-id="9fd48-103">Troubleshoot inventory operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9fd48-104">此主题介绍如何解决使用库存操作时可能遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="9fd48-104">This topic describes how to fix issues that you might encounter while you work with inventory operations.</span></span>

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a><span data-ttu-id="9fd48-105">我找不到库存日记帐的“工作流”下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="9fd48-105">I can't find the "Workflow" drop-down dialog box for inventory journals.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9fd48-106">问题描述</span><span class="sxs-lookup"><span data-stu-id="9fd48-106">Issue description</span></span>

<span data-ttu-id="9fd48-107">在日记帐页上找不到 **工作流** 下拉对话框，或相关的工作流操作不可用。</span><span class="sxs-lookup"><span data-stu-id="9fd48-107">You can't find the **Workflow** drop-down dialog box on the journal page, or related workflow operations aren't available.</span></span>

<span data-ttu-id="9fd48-108">发生此问题可能由于三个原因，如以下小节所述。</span><span class="sxs-lookup"><span data-stu-id="9fd48-108">This issue can occur for three reasons, as described in the following subsections.</span></span>

### <a name="issue-resolution-1"></a><span data-ttu-id="9fd48-109">解决问题 1</span><span class="sxs-lookup"><span data-stu-id="9fd48-109">Issue resolution 1</span></span>

<span data-ttu-id="9fd48-110">如果问题适用于所有用户，可能是由于未将审批工作流分配给日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="9fd48-110">If the issue applies to all users, it might be occurring because the approval workflow hasn't been assigned to the journal name.</span></span> <span data-ttu-id="9fd48-111">若要解决此问题，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="9fd48-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="9fd48-112">转到 **库存管理 &gt; 设置 &gt; 日记帐名称 &gt; 库存**。</span><span class="sxs-lookup"><span data-stu-id="9fd48-112">Go to **Inventory Management &gt; Setup &gt; Journal names &gt; Inventory**.</span></span>
1. <span data-ttu-id="9fd48-113">在列表窗格中，选择一个日记帐名称来打开其设置。</span><span class="sxs-lookup"><span data-stu-id="9fd48-113">In the list pane, select a journal name to open its settings.</span></span>
1. <span data-ttu-id="9fd48-114">在 **常规** 快速选项卡上，将 **审批工作流** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="9fd48-114">On the **General** FastTab, set the **Approval workflow** option to *Yes*.</span></span> <span data-ttu-id="9fd48-115">如果提示确认更改，选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="9fd48-115">If you're prompted to confirm the change, select **Yes**.</span></span>
1. <span data-ttu-id="9fd48-116">在 **工作流** 字段中，选择要用于所选日记帐名称的工作流。</span><span class="sxs-lookup"><span data-stu-id="9fd48-116">In the **Workflow** field, select the workflow that you want to use for the selected journal name.</span></span>

### <a name="issue-resolution-2"></a><span data-ttu-id="9fd48-117">解决问题 2</span><span class="sxs-lookup"><span data-stu-id="9fd48-117">Issue resolution 2</span></span>

<span data-ttu-id="9fd48-118">如果您的工作流使用自定义代码，在升级系统后可能会出现问题。</span><span class="sxs-lookup"><span data-stu-id="9fd48-118">If your workflow uses customized code, issues might occur after you upgrade the system.</span></span> <span data-ttu-id="9fd48-119">例如，在日记帐工作流中，**提交** 按钮可能为灰色，因此您无法选择它来审批提交。</span><span class="sxs-lookup"><span data-stu-id="9fd48-119">For example, in the journal workflow, the **Submit** button might be grayed out so you can't select it to approve a submission.</span></span>

<span data-ttu-id="9fd48-120">如果 **提交** 按钮是灰显，您的工作流可能已自定义，这意味着工作流的方法 `FormDataUtil` 中的 `canSubmitToWorkflow()` 已扩展。</span><span class="sxs-lookup"><span data-stu-id="9fd48-120">If the **Submit** button is grayed out, your workflow might have been customized, which means the method of the workflow, `canSubmitToWorkflow()` in `FormDataUtil`, has been extended.</span></span> <span data-ttu-id="9fd48-121">要解决此问题，更改您扩展 `canSubmitToWorkflow()` 方法的方式以使用以下示例中的结构。</span><span class="sxs-lookup"><span data-stu-id="9fd48-121">To fix this issue, change the way that you extend the method of the `canSubmitToWorkflow()` to use the structure in the following example.</span></span>

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a><span data-ttu-id="9fd48-122">解决问题 3</span><span class="sxs-lookup"><span data-stu-id="9fd48-122">Issue resolution 3</span></span>

<span data-ttu-id="9fd48-123">如果此问题仅适用于少数几个特定用户，有可能是这些用户没有对库存日记帐运行工作流操作所需的安全特权。</span><span class="sxs-lookup"><span data-stu-id="9fd48-123">If the issue applies only to a few specific users, those users might not have the security privileges that are required to run workflow operations on inventory journals.</span></span> <span data-ttu-id="9fd48-124">请验证是否每个受影响的用户都有 *维护库存日记帐工作流* 安全特权。</span><span class="sxs-lookup"><span data-stu-id="9fd48-124">Verify that each affected user has the *Maintain inventory journal workflow* security privilege.</span></span> <span data-ttu-id="9fd48-125">默认情况下，此特权分配给具有相同名称的职责，该职责适用于 *仓库工作人员* 和 *仓库经理* 角色。</span><span class="sxs-lookup"><span data-stu-id="9fd48-125">By default, this privilege is assigned to a duty that has same name, and that duty is applied to the *Warehouse worker* and *Warehouse manager* roles.</span></span>

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a><span data-ttu-id="9fd48-126">我的库存日记帐停留在系统锁定状态，工作流批处理作业不工作。</span><span class="sxs-lookup"><span data-stu-id="9fd48-126">My inventory journal remains in system-locked status, and the workflow batch job doesn't work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9fd48-127">问题描述</span><span class="sxs-lookup"><span data-stu-id="9fd48-127">Issue description</span></span>

<span data-ttu-id="9fd48-128">您的其中一个库存日记帐被某个操作锁定，没有解锁。</span><span class="sxs-lookup"><span data-stu-id="9fd48-128">One of your inventory journals is locked by some operation and isn't being released.</span></span> <span data-ttu-id="9fd48-129">例如，如果在过帐过程中发生未知错误（这是系统锁定操作），日记帐可能保持系统锁定状态。</span><span class="sxs-lookup"><span data-stu-id="9fd48-129">For example, if an unknown error occurs during posting (which is a system lock operation), the journal might remain in system-locked status.</span></span> <span data-ttu-id="9fd48-130">在这种情况下，工作流工作项处理程序在进行锁定验证时将抛出错误。</span><span class="sxs-lookup"><span data-stu-id="9fd48-130">In this case, the workflow work item handler will throw an error while it does lock validation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9fd48-131">解决问题</span><span class="sxs-lookup"><span data-stu-id="9fd48-131">Issue resolution</span></span>

<span data-ttu-id="9fd48-132">请登录到 Supply Chain Management 的 SQL Server 实例，检查 **InventJournalTable.SystemBlocked** 是否设置为 *1*。</span><span class="sxs-lookup"><span data-stu-id="9fd48-132">Sign in to the SQL Server instance for Supply Chain Management, and check whether **InventJournalTable.SystemBlocked** is set to *1*.</span></span> <span data-ttu-id="9fd48-133">如果是，请确保该日记帐不应该处于锁定状态，然后将 **InventJournalTable.SystemBlocked** 重置为 *0*。</span><span class="sxs-lookup"><span data-stu-id="9fd48-133">If it is, make sure that the journal should not be in locked status, and then reset **InventJournalTable.SystemBlocked** to *0*.</span></span>

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a><span data-ttu-id="9fd48-134">我的库存日记帐工作流一直没有完成，日记帐无法编辑或过帐。</span><span class="sxs-lookup"><span data-stu-id="9fd48-134">My inventory journal workflow is never completed, and the journal can't be edited or posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9fd48-135">问题描述</span><span class="sxs-lookup"><span data-stu-id="9fd48-135">Issue description</span></span>

<span data-ttu-id="9fd48-136">提交日记帐审批工作流后，工作流处理将停止响应，您无法编辑或处理日记帐。</span><span class="sxs-lookup"><span data-stu-id="9fd48-136">After you submit a journal approval workflow, workflow processing stops responding, and you can't edit or process your journals.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9fd48-137">解决问题</span><span class="sxs-lookup"><span data-stu-id="9fd48-137">Issue resolution</span></span>

<span data-ttu-id="9fd48-138">有几种原因可能导致工作流处理无法完成。</span><span class="sxs-lookup"><span data-stu-id="9fd48-138">There are several reasons why workflow processing might not be completed.</span></span> <span data-ttu-id="9fd48-139">请检查以下问题：</span><span class="sxs-lookup"><span data-stu-id="9fd48-139">Check for the following issues:</span></span>

- <span data-ttu-id="9fd48-140">转到 **库存管理 &gt; 设置 &gt; 库存管理工作流**，查看受影响的工作流的配置。</span><span class="sxs-lookup"><span data-stu-id="9fd48-140">Go to **Inventory management &gt; Setup &gt; Inventory management workflows**, and review the configuration of the affected workflow.</span></span> <span data-ttu-id="9fd48-141">有关详细信息，请参阅[库存日记帐审批工作流](inventory-journal-workflow.md)。</span><span class="sxs-lookup"><span data-stu-id="9fd48-141">For more information, see [Inventory journal approval workflows](inventory-journal-workflow.md).</span></span>
- <span data-ttu-id="9fd48-142">工作流可能遇到异常或错误。</span><span class="sxs-lookup"><span data-stu-id="9fd48-142">The workflow might be encountering an exception or error.</span></span> <span data-ttu-id="9fd48-143">查看受影响的工作流的工作项历史记录是否包含终止工作流的应用程序错误。</span><span class="sxs-lookup"><span data-stu-id="9fd48-143">Review the work item history of the affected workflow to see whether it includes an application error that terminates the workflow.</span></span>
- <span data-ttu-id="9fd48-144">库存日记帐只有在获得批准后才能进行更新或编辑。</span><span class="sxs-lookup"><span data-stu-id="9fd48-144">The inventory journal can be updated or edited only if it's approved.</span></span> <span data-ttu-id="9fd48-145">如果撤回可用，您可以尝试撤回日记帐。</span><span class="sxs-lookup"><span data-stu-id="9fd48-145">If recall is active, you can try to recall the journal.</span></span> <span data-ttu-id="9fd48-146">工作流批处理作业的执行可能由于多个原因被暂停。</span><span class="sxs-lookup"><span data-stu-id="9fd48-146">Execution of the workflow batch job might be suspended for multiple reasons.</span></span> <span data-ttu-id="9fd48-147">有些原因可能是由工作流框架问题引起的。</span><span class="sxs-lookup"><span data-stu-id="9fd48-147">Some of these reasons might be caused by the workflow framework issue.</span></span>

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a><span data-ttu-id="9fd48-148">库存日记帐工作流条件只能在日记帐级别应用，不能在行级别应用</span><span class="sxs-lookup"><span data-stu-id="9fd48-148">Inventory journal workflow conditions apply only at the journal level, not at the line level</span></span>

### <a name="issue-description"></a><span data-ttu-id="9fd48-149">问题描述</span><span class="sxs-lookup"><span data-stu-id="9fd48-149">Issue description</span></span>

<span data-ttu-id="9fd48-150">比如，如果您尝试对成本金额设置库存日记帐工作流条件，可能会遇到此问题。</span><span class="sxs-lookup"><span data-stu-id="9fd48-150">You might experience this issue if, for example, you try to set up an inventory journal workflow condition on the cost amount.</span></span> <span data-ttu-id="9fd48-151">您设置此条件，让步骤 1 仅在成本金额小于 100 时运行。</span><span class="sxs-lookup"><span data-stu-id="9fd48-151">You set up the condition so that step 1 is run only when the cost amount is less than 100.</span></span> <span data-ttu-id="9fd48-152">然后设置另一个条件，让步骤 2 仅在成本金额大于或等于 100 时运行。</span><span class="sxs-lookup"><span data-stu-id="9fd48-152">You then set up another condition so that step 2 is run only when the cost amount is more than or equal to 100.</span></span> <span data-ttu-id="9fd48-153">然后，在工作流运行时，工作流历史记录将仅显示一行，第一个条件始终计算为 *true*，无论提交什么值。</span><span class="sxs-lookup"><span data-stu-id="9fd48-153">Then, when the workflow is run, the workflow history shows only one line, and the first condition is always evaluated as *true*, regardless of the value that is submitted.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="9fd48-154">问题解决方法</span><span class="sxs-lookup"><span data-stu-id="9fd48-154">Issue workaround</span></span>

<span data-ttu-id="9fd48-155">在当前版本中，日记帐工作流条件只在日记帐级别应用，不在行级别应用。</span><span class="sxs-lookup"><span data-stu-id="9fd48-155">In the current release, inventory workflow conditions apply only at the journal level, not at the line level.</span></span> <span data-ttu-id="9fd48-156">此为有意行为。</span><span class="sxs-lookup"><span data-stu-id="9fd48-156">This behavior is by design.</span></span> <span data-ttu-id="9fd48-157">我们建议您仅对日记帐级属性设置条件。</span><span class="sxs-lookup"><span data-stu-id="9fd48-157">We recommend that you set your condition criteria only on journal-level attributes.</span></span>

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a><span data-ttu-id="9fd48-158">现有量列表页上的筛选器窗格没有按我预期的那样筛选结果。</span><span class="sxs-lookup"><span data-stu-id="9fd48-158">The filter pane on the On-hand list page doesn't filter results as I expect.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9fd48-159">问题描述</span><span class="sxs-lookup"><span data-stu-id="9fd48-159">Issue description</span></span>

<span data-ttu-id="9fd48-160">**现有量列表** 页上筛选器窗格中的筛选器没有按您预期的那样筛选结果。</span><span class="sxs-lookup"><span data-stu-id="9fd48-160">The filters in the filter pane on the **On-hand list** page don't filter results as you expect.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9fd48-161">解决问题</span><span class="sxs-lookup"><span data-stu-id="9fd48-161">Issue resolution</span></span>

<span data-ttu-id="9fd48-162">此为有意行为。</span><span class="sxs-lookup"><span data-stu-id="9fd48-162">This behavior is by design.</span></span>

<span data-ttu-id="9fd48-163"> *\*现有量列表** 页是从包含所有可用维度的详细现有库存量表组合而成的。</span><span class="sxs-lookup"><span data-stu-id="9fd48-163">The **On-hand list** page is assembled from a detailed on-hand inventory table that includes all available dimensions.</span></span> <span data-ttu-id="9fd48-164">但是，此页面上的列表是一个摘要。</span><span class="sxs-lookup"><span data-stu-id="9fd48-164">However, the list on this page is a summary.</span></span> <span data-ttu-id="9fd48-165">因此，它可能根据显示的维度通过聚合值来合并源表中的行。</span><span class="sxs-lookup"><span data-stu-id="9fd48-165">Therefore, it might combine rows from the source table by aggregating values according to the dimensions that are shown.</span></span>

<span data-ttu-id="9fd48-166">在筛选器窗格中设置的筛选器将应用于源表，不应用于聚合列表。</span><span class="sxs-lookup"><span data-stu-id="9fd48-166">Filters that are set up in the filter pane apply to the source table, not to the aggregated list.</span></span> <span data-ttu-id="9fd48-167">此行为有时会产生意外结果，如[这些示例](inventory-on-hand-list.md#examples)所示。</span><span class="sxs-lookup"><span data-stu-id="9fd48-167">This behavior can sometimes produce unexpected results, as shown in [these examples](inventory-on-hand-list.md#examples).</span></span>

<span data-ttu-id="9fd48-168">但是， [网格中提供的筛选器](inventory-on-hand-list.md#grid-filters) *应用* 于聚合列表。</span><span class="sxs-lookup"><span data-stu-id="9fd48-168">However, the [filters that are provided in the grid](inventory-on-hand-list.md#grid-filters) *do* apply to the aggregated list.</span></span> <span data-ttu-id="9fd48-169">这些筛选器既包括位于网格顶部的快速筛选器，也包括每个列标题的筛选器。</span><span class="sxs-lookup"><span data-stu-id="9fd48-169">These filters include both the QuickFilter at the top of the grid and the filter for each column heading.</span></span>

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a><span data-ttu-id="9fd48-170">单位和单位数量在库存日记帐中不能正常工作。</span><span class="sxs-lookup"><span data-stu-id="9fd48-170">The unit and unit quantity aren't working correctly in the inventory journal.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9fd48-171">问题描述</span><span class="sxs-lookup"><span data-stu-id="9fd48-171">Issue description</span></span>

<span data-ttu-id="9fd48-172">在库存日记帐中使用单位和数量时，您可能会遇到以下一个或两个问题：</span><span class="sxs-lookup"><span data-stu-id="9fd48-172">You might encounter one or both of the following issues when you work with units and quantities in an inventory journal:</span></span>

- <span data-ttu-id="9fd48-173">为已发布产品设置转换单位时，在库存日记帐中看不到单位或数量，也无法在库存日记帐中更改单位。</span><span class="sxs-lookup"><span data-stu-id="9fd48-173">You don't see units or unit quantities in the inventory journal while a unit of conversion is set up for the released product, and you can't change the unit in the inventory journal.</span></span>
- <span data-ttu-id="9fd48-174">您在库存日记帐中看到 **数量** 和 **单位** 字段，但是看不到 **单位数量** 字段。</span><span class="sxs-lookup"><span data-stu-id="9fd48-174">You see the **Quantity** and **Unit** fields in the inventory journal, but you don't see the **Unit quantity** field.</span></span> <span data-ttu-id="9fd48-175">如果您更改单位、输入数量和过帐日记帐，日记帐仍显示该数量的原始度量单位。</span><span class="sxs-lookup"><span data-stu-id="9fd48-175">If you change the unit, enter a quantity, and post the journal, the journal still shows the original unit of measurement for that quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9fd48-176">解决问题</span><span class="sxs-lookup"><span data-stu-id="9fd48-176">Issue resolution</span></span>

<span data-ttu-id="9fd48-177">若要解决此问题，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="9fd48-177">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="9fd48-178">在 **功能管理** 工作区，请确保 *在库存日记帐中使用度量单位和单位数量* 功能已开启。</span><span class="sxs-lookup"><span data-stu-id="9fd48-178">In the **Feature management** workspace, make sure that the *Using unit of measure and unit quantity in inventory journals* feature is turned on.</span></span> <span data-ttu-id="9fd48-179">此功能会将 **单位** 和 **单位数量** 字段添加到日记帐中。</span><span class="sxs-lookup"><span data-stu-id="9fd48-179">This feature adds the **Unit** and **Unit quantity** fields to the journal.</span></span>
1. <span data-ttu-id="9fd48-180">开启此功能后，通过以下方式使用 **数量**、**单位数量** 和 **单位** 字段：</span><span class="sxs-lookup"><span data-stu-id="9fd48-180">After the feature is turned on, use the **Quantity**, **Unit quantity**, and **Unit** fields in the following way:</span></span>

    - <span data-ttu-id="9fd48-181">**数量** – 使用为已发布产品定义的默认单位指定数量。</span><span class="sxs-lookup"><span data-stu-id="9fd48-181">**Quantity** – Specify the quantity by using the default unit that is defined for the released product.</span></span> <span data-ttu-id="9fd48-182">但是，默认单位本身不在此处显示。</span><span class="sxs-lookup"><span data-stu-id="9fd48-182">However, the default unit itself isn't shown here.</span></span> <span data-ttu-id="9fd48-183">如果在默认单位和 **单位** 字段中选择的单位之间设置了转换，**数量** 字段将根据 **单位数量** 和 **单位** 字段中的选择自动更新。</span><span class="sxs-lookup"><span data-stu-id="9fd48-183">If a conversion is set up between the default unit and the unit that is selected in the **Unit** field, the **Quantity** field is automatically updated, based on the selections in the **Unit quantity** and **Unit** fields.</span></span>
    - <span data-ttu-id="9fd48-184">**单位数量** – 使用在 **单位** 字段中选择的单位指定数量。</span><span class="sxs-lookup"><span data-stu-id="9fd48-184">**Unit quantity** – Specify the quantity by using the unit that is selected in the **Unit** field.</span></span>
    - <span data-ttu-id="9fd48-185">**单位** – 在 **单位数量** 字段中选择要应用于值的单位。</span><span class="sxs-lookup"><span data-stu-id="9fd48-185">**Unit** – Select the unit to apply to the value in the **Unit quantity** field.</span></span>

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a><span data-ttu-id="9fd48-186">我收到以下错误消息：“库存单位的最大小数位数为 0。”</span><span class="sxs-lookup"><span data-stu-id="9fd48-186">I receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

### <a name="issue-description"></a><span data-ttu-id="9fd48-187">问题描述</span><span class="sxs-lookup"><span data-stu-id="9fd48-187">Issue description</span></span>

<span data-ttu-id="9fd48-188">当您尝试过帐库存交易或库存预留时，收到以下错误消息：“库存单位的最大小数位数为 0。”</span><span class="sxs-lookup"><span data-stu-id="9fd48-188">When you try to post an inventory transaction or an inventory reservation, you receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

<span data-ttu-id="9fd48-189">当库存交易数量被指定为字段支持的精度级别以下的十进制值时，会发生此问题。</span><span class="sxs-lookup"><span data-stu-id="9fd48-189">This issue occurs when the inventory transaction quantity is specified as a decimal value that is below the level of precision that the field supports.</span></span> <span data-ttu-id="9fd48-190">例如，为库存交易指定了数量 *0.5*，但仅支持整数数量。</span><span class="sxs-lookup"><span data-stu-id="9fd48-190">For example, a quantity of *0.5* has been specified for an inventory transaction, but only integer quantities are supported.</span></span> <span data-ttu-id="9fd48-191">因此，值应为 *1*，而不是 *0.5*。</span><span class="sxs-lookup"><span data-stu-id="9fd48-191">Therefore, the value should be *1* instead of *0.5*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9fd48-192">解决问题</span><span class="sxs-lookup"><span data-stu-id="9fd48-192">Issue resolution</span></span>

1. <span data-ttu-id="9fd48-193">在 SQL Server 实例上运行以下脚本来舍入库存交易中的数量。</span><span class="sxs-lookup"><span data-stu-id="9fd48-193">Run the following script on your SQL Server instance to round quantities in the inventory transactions.</span></span> <span data-ttu-id="9fd48-194">此脚本将更正 **inventTrans** 表中的值。</span><span class="sxs-lookup"><span data-stu-id="9fd48-194">This script will correct values in the **inventTrans** table.</span></span>

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. <span data-ttu-id="9fd48-195">在 **修复错误** 选项打开时运行现有量一致性检查。</span><span class="sxs-lookup"><span data-stu-id="9fd48-195">Run an on-hand consistency check where the **fix error** option is turned on.</span></span> <span data-ttu-id="9fd48-196">此检查将更正 **inventSum** 表中的值。</span><span class="sxs-lookup"><span data-stu-id="9fd48-196">This check will correct values in the **inventSum** table.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9fd48-197">强烈建议您根据环境的需要仔细编辑脚本，在测试环境中进行测试，然后在生产环境中运行脚本之前检查结果数据。</span><span class="sxs-lookup"><span data-stu-id="9fd48-197">We strongly recommend that you carefully edit the script as required for your environment, test it in a test environment, and then check the resulting data before you run the script in a production environment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
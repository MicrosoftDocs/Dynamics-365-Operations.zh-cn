---
title: 离散制造疑难解答
description: 此主题介绍如何解决使用离散制造时可能遇到的问题。
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 604e0c3406b15d885991fcb067e93ef83533e3b0
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516732"
---
# <a name="troubleshoot-discrete-manufacturing"></a><span data-ttu-id="e4599-103">离散制造疑难解答</span><span class="sxs-lookup"><span data-stu-id="e4599-103">Troubleshoot discrete manufacturing</span></span>

<span data-ttu-id="e4599-104">此主题介绍如何解决使用离散制造时可能遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="e4599-104">This topic describes how to fix issues that you might encounter while you work with discrete manufacturing.</span></span>

## <a name="i-receive-the-following-error-message-warehouse-management-processes-are-currently-being-used-if-work-lines-are-not-yet-registered-you-can-cancel-the-created-work-and-any-load-or-shipment-lines-and-then-continue-with-the-picking-or-shipping-process"></a><span data-ttu-id="e4599-105">我收到以下错误消息：“仓库管理流程当前正在使用。</span><span class="sxs-lookup"><span data-stu-id="e4599-105">I receive the following error message: "Warehouse management processes are currently being used.</span></span> <span data-ttu-id="e4599-106">如果工作行尚未登记，您可以取消创建的工作以及所有负荷或装运行，然后继续领料或装运流程。”</span><span class="sxs-lookup"><span data-stu-id="e4599-106">If work lines are not yet registered, you can cancel the created work and any load or shipment lines, and then continue with the picking or shipping process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e4599-107">问题描述</span><span class="sxs-lookup"><span data-stu-id="e4599-107">Issue description</span></span>

<span data-ttu-id="e4599-108">如果您尝试预留或下达某个行的工作，但库存交易的状态为 *已领料*（指示物料已领取），这时会发生此问题。</span><span class="sxs-lookup"><span data-stu-id="e4599-108">This issue occurs if you try to reserve or release work for a line, but the inventory transaction has a status of *Picked*, which indicates that the material has been picked.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e4599-109">解决问题</span><span class="sxs-lookup"><span data-stu-id="e4599-109">Issue resolution</span></span>

<span data-ttu-id="e4599-110">若要解决此问题，请按照以下其中一个步骤操作。</span><span class="sxs-lookup"><span data-stu-id="e4599-110">To fix this issue, follow one of these steps.</span></span>

- <span data-ttu-id="e4599-111">将生产订单的状态更改回 *已估计* 或 *已下达*。</span><span class="sxs-lookup"><span data-stu-id="e4599-111">Change the status of the production order back to *Estimated* or *Released*.</span></span>
- <span data-ttu-id="e4599-112">打开相关生产订单的详细信息页面。</span><span class="sxs-lookup"><span data-stu-id="e4599-112">Open the details page for the relevant production order.</span></span> <span data-ttu-id="e4599-113">在操作窗格上的 **仓库** 选项卡上，在 **停止** 组中，选择 **停止并取消领料** 取消所有已领料交易的领料。</span><span class="sxs-lookup"><span data-stu-id="e4599-113">On the Action Pane, on the **Warehouse** tab, in the **Stop** group, select **Stop and unpick** to unpick all picked transactions.</span></span> <span data-ttu-id="e4599-114">然后选择 **删除停止** 以处理生产订单。</span><span class="sxs-lookup"><span data-stu-id="e4599-114">Then select **Remove stop** to process the production order.</span></span>

<span data-ttu-id="e4599-115">这里是对 *取消领料* 和 *停止* 功能的说明：</span><span class="sxs-lookup"><span data-stu-id="e4599-115">Here is an explanation of the *Unpick* and *Stop* functions:</span></span>

- <span data-ttu-id="e4599-116">**取消领料** – 此功能撤消状态从 *已领料* 一直到 *在单* 的物料清单 (BOM) 行和配方行的库存交易状态。</span><span class="sxs-lookup"><span data-stu-id="e4599-116">**Unpick** – This function reverses the status of inventory transactions for bill of materials (BOM) lines and formula lines that have a status from *Picked* through *On order*.</span></span> <span data-ttu-id="e4599-117">原材料领料工作完成后，行的状态将设置为 *已领料*。</span><span class="sxs-lookup"><span data-stu-id="e4599-117">When work for raw material picking is completed, the status of the lines is set to *Picked*.</span></span> <span data-ttu-id="e4599-118">此状态防止将生产订单重置为 *已创建* 状态。</span><span class="sxs-lookup"><span data-stu-id="e4599-118">This status prevents the production order from being reset to *Created* status.</span></span> <span data-ttu-id="e4599-119">在这种情况下，您可以使用 *取消领料* 功能从 *已领料* 状态恢复交易，然后将生产订单重置为 *已创建* 状态。</span><span class="sxs-lookup"><span data-stu-id="e4599-119">In this case, you can use the *Unpick* function to revert the transactions from *Picked* status and then reset the production order to *Created* status.</span></span>
- <span data-ttu-id="e4599-120">**停止** – 此功能在生产订单上设置 **已停止** 标记，以防止对订单进行任何状态更新。</span><span class="sxs-lookup"><span data-stu-id="e4599-120">**Stop** – This function sets a **Stopped** flag on the production order to prevent any status update on the order.</span></span> <span data-ttu-id="e4599-121">您可以在生产订单详细信息页的 **仓库** 快速选项卡上找到 **已停止** 标记。</span><span class="sxs-lookup"><span data-stu-id="e4599-121">You can find the **Stopped** flag on the **Warehouse** FastTab of the production order details page.</span></span>

> [!NOTE]
>
> - <span data-ttu-id="e4599-122">仅当为仓库流程启用的物料创建生产订单时，按钮才可见。</span><span class="sxs-lookup"><span data-stu-id="e4599-122">The buttons are visible only when the production order is created for items that are enabled for warehouse processes.</span></span>
> - <span data-ttu-id="e4599-123">**停止** 组仅在生产订单详细信息页的操作窗格上的 **仓库** 选项卡上可见。</span><span class="sxs-lookup"><span data-stu-id="e4599-123">The **Stop** group is visible only on the **Warehouse** tab on the Action Pane of the production order details page.</span></span> <span data-ttu-id="e4599-124">在 **生产订单** 列表页的 **仓库** 快速选项卡上不可见。</span><span class="sxs-lookup"><span data-stu-id="e4599-124">It isn't visible on the **Warehouse** FastTab of the **Production orders** list page.</span></span>

## <a name="the-matching-resource-name-isnt-updated-after-i-change-a-worker-name-in-the-global-address-book"></a><span data-ttu-id="e4599-125">我在全球通讯簿中更改工作人员姓名后，匹配的资源姓名不更新。</span><span class="sxs-lookup"><span data-stu-id="e4599-125">The matching resource name isn't updated after I change a worker name in the global address book.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e4599-126">问题描述</span><span class="sxs-lookup"><span data-stu-id="e4599-126">Issue description</span></span>

<span data-ttu-id="e4599-127">如果您在全球通讯簿中更改工作人员姓名，匹配的资源姓名不会在主资源组中更新。</span><span class="sxs-lookup"><span data-stu-id="e4599-127">If you change a worker name in the global address book, the matching resource name isn't updated in the resource group master.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e4599-128">解决问题</span><span class="sxs-lookup"><span data-stu-id="e4599-128">Issue resolution</span></span>

<span data-ttu-id="e4599-129">当前不支持此场景。</span><span class="sxs-lookup"><span data-stu-id="e4599-129">This scenario isn't currently supported.</span></span> <span data-ttu-id="e4599-130">若要解决此问题，您必须手动更新资源姓名。</span><span class="sxs-lookup"><span data-stu-id="e4599-130">To fix the issue, you must manually update the resource name.</span></span>

## <a name="when-i-create-a-new-production-order-i-dont-receive-the-following-message-insert-the-active-version-of-bill-of-material-and-route"></a><span data-ttu-id="e4599-131">我在创建新生产订单时，没有收到以下消息：“插入物料清单和工艺路线的有效版本？”</span><span class="sxs-lookup"><span data-stu-id="e4599-131">When I create a new production order, I don't receive the following message: "Insert the active version of bill of material and route?"</span></span>

### <a name="issue-description"></a><span data-ttu-id="e4599-132">问题描述</span><span class="sxs-lookup"><span data-stu-id="e4599-132">Issue description</span></span>

<span data-ttu-id="e4599-133">创建新的生产订单时，输入物料编号后，**站点** 和 **仓库** 字段将自动设置为在成品物料的 **默认订单设置** 页上定义的默认站点和仓库。</span><span class="sxs-lookup"><span data-stu-id="e4599-133">When you create a new production order, after you enter the item number, the **Site** and **Warehouse** fields are automatically set to the default site and warehouse that are defined on the **Default order settings** page for the finished goods item.</span></span> <span data-ttu-id="e4599-134">此外，有效的物料清单编号和工艺路线编号也将自动输入。</span><span class="sxs-lookup"><span data-stu-id="e4599-134">Additionally, the active BOM number and route number are automatically entered.</span></span> <span data-ttu-id="e4599-135">您不会收到以下提示您输入这些值的消息：</span><span class="sxs-lookup"><span data-stu-id="e4599-135">You don't receive the following message that prompts you for those values:</span></span>

> <span data-ttu-id="e4599-136">插入物料清单和工艺路线的有效版本？</span><span class="sxs-lookup"><span data-stu-id="e4599-136">Insert active version for bill of material and route?</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e4599-137">解决问题</span><span class="sxs-lookup"><span data-stu-id="e4599-137">Issue resolution</span></span>

<span data-ttu-id="e4599-138">如果您选择了在 **默认订单设置** 页上为其定义了站点和仓库的产品，则不会提示您插入物料清单和工艺路线编号。</span><span class="sxs-lookup"><span data-stu-id="e4599-138">You aren't prompted to insert BOM and route numbers if you select a product that a site and warehouse are defined for on the **Default order settings** page.</span></span> <span data-ttu-id="e4599-139">只有在没有为所选产品定义这些值时，才会提示您。</span><span class="sxs-lookup"><span data-stu-id="e4599-139">You're prompted only if those values aren't defined for the selected product.</span></span>

## <a name="production-orders-arent-shown-on-the-marking-page"></a><span data-ttu-id="e4599-140">生产订单没有显示在“标记”页上。</span><span class="sxs-lookup"><span data-stu-id="e4599-140">Production orders aren't shown on the Marking page.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e4599-141">问题描述</span><span class="sxs-lookup"><span data-stu-id="e4599-141">Issue description</span></span>

<span data-ttu-id="e4599-142">有些生产订单不会显示在 **标记** 页上。</span><span class="sxs-lookup"><span data-stu-id="e4599-142">Some production orders aren't shown on the **Marking** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e4599-143">解决问题</span><span class="sxs-lookup"><span data-stu-id="e4599-143">Issue resolution</span></span>

<span data-ttu-id="e4599-144">具有以下配置的产品不能进行标记。</span><span class="sxs-lookup"><span data-stu-id="e4599-144">Products that have the following configuration aren't available for marking.</span></span> <span data-ttu-id="e4599-145">因此，它们不会显示在 **标记** 页上：</span><span class="sxs-lookup"><span data-stu-id="e4599-145">Therefore, they won't be shown on the **Marking** page:</span></span>

- <span data-ttu-id="e4599-146">这些产品定义为 *实际称重* 类型的产品。</span><span class="sxs-lookup"><span data-stu-id="e4599-146">The products are defined as products of the *catch weight* type.</span></span>
- <span data-ttu-id="e4599-147">它们已启用高级仓库流程。</span><span class="sxs-lookup"><span data-stu-id="e4599-147">They are enabled for the advanced warehouse processes.</span></span>
- <span data-ttu-id="e4599-148">它们被配置为由 *标准成本* 原则控制。</span><span class="sxs-lookup"><span data-stu-id="e4599-148">They are configured to be controlled by the *Standard cost* principle.</span></span>

## <a name="when-i-try-to-end-a-production-order-i-receive-the-following-error-message-calculating-bom-consumptioncost-value-must-be-negative-upon-issue-from-inventory"></a><span data-ttu-id="e4599-149">当我尝试结束生产订单时，收到以下错误消息：“计算的物料清单 consumptionCost 值在从库存发货时必须为负。”</span><span class="sxs-lookup"><span data-stu-id="e4599-149">When I try to end a production order, I receive the following error message: "Calculating BOM consumptionCost value must be negative upon issue from inventory."</span></span>

<span data-ttu-id="e4599-150">此问题在版本 10.0.15 中已修复。</span><span class="sxs-lookup"><span data-stu-id="e4599-150">This issue was fixed in release 10.0.15.</span></span>

## <a name="when-the-status-of-a-production-order-is-changed-from-reported-as-finished-to-end-i-receive-the-following-error-messages-update-conflict-the-standard-cost-does-not-match-with-the-financial-inventory-value-after-the-update-and-a-critical-error-has-occurred-in-function-inventcostmovementcheckvariance"></a><span data-ttu-id="e4599-151">当生产订单的状态从“完工入库”更改为“结束”时，我收到以下错误消息：“更新冲突。</span><span class="sxs-lookup"><span data-stu-id="e4599-151">When the status of a production order is changed from Reported as finished to End, I receive the following error messages: "Update conflict.</span></span> <span data-ttu-id="e4599-152">标准成本与更新后的财务库存值不匹配”和“InventCostMovement.checkVariance 函数中发生严重错误”。</span><span class="sxs-lookup"><span data-stu-id="e4599-152">The standard cost does not match with the financial inventory value after the update" and "A critical error has occurred in function InventCostMovement.checkVariance."</span></span>

<span data-ttu-id="e4599-153">发生此问题的原因是基础数据被另一个流程更改。</span><span class="sxs-lookup"><span data-stu-id="e4599-153">This issue occurs because the underlying data was changed by another process.</span></span> <span data-ttu-id="e4599-154">此流程最多会尝试更新数据五次。</span><span class="sxs-lookup"><span data-stu-id="e4599-154">The process will try to update the data up to five times.</span></span> <span data-ttu-id="e4599-155">如果五次尝试后冲突仍然存在，您将收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="e4599-155">If the conflict still exists after five attempts, you will receive the following error messages:</span></span>

> <span data-ttu-id="e4599-156">更新冲突。</span><span class="sxs-lookup"><span data-stu-id="e4599-156">Update conflict.</span></span> <span data-ttu-id="e4599-157">标准成本在更新后与财务库存值不匹配。</span><span class="sxs-lookup"><span data-stu-id="e4599-157">The standard cost does not match with the financial inventory value after the update.</span></span>

> <span data-ttu-id="e4599-158">函数 InventCostMovement.checkVariance 中发生严重错误。</span><span class="sxs-lookup"><span data-stu-id="e4599-158">A critical error has occurred in function InventCostMovement.checkVariance.</span></span>

<span data-ttu-id="e4599-159">此为有意行为。</span><span class="sxs-lookup"><span data-stu-id="e4599-159">This behavior is by design.</span></span> <span data-ttu-id="e4599-160">要缓解此问题，请继续批处理作业。</span><span class="sxs-lookup"><span data-stu-id="e4599-160">To mitigate the issue, resume the batch job.</span></span> <span data-ttu-id="e4599-161">它应该完成运行。</span><span class="sxs-lookup"><span data-stu-id="e4599-161">It should finish running.</span></span>

<span data-ttu-id="e4599-162">如果批处理作业在您恢复后持续失败，请验证分类帐默认货币的舍入精度是否符合应用于 InventSum 表中的值的舍入要求。</span><span class="sxs-lookup"><span data-stu-id="e4599-162">If the batch job consistently fails after you resume it, verify that the rounding precision for the ledger's default currency is compliant with the rounding that is applied to values in the InventSum table.</span></span> <span data-ttu-id="e4599-163">如果舍入精度更改为不符合要求的值，您可能必须将其重新更改为符合要求的值。</span><span class="sxs-lookup"><span data-stu-id="e4599-163">If the rounding precision has been changed to a non-compliant value, you probably must change it back to a compliant value.</span></span> <span data-ttu-id="e4599-164">查找 **ModifiedDateTime**。</span><span class="sxs-lookup"><span data-stu-id="e4599-164">Look for **ModifiedDateTime**.</span></span> <span data-ttu-id="e4599-165">在这种情况下，此值通常会显示舍入精度最近已更改。</span><span class="sxs-lookup"><span data-stu-id="e4599-165">In this case, the value will typically show that the rounding precision was recently changed.</span></span>

## <a name="when-i-release-to-a-warehouse-i-receive-the-following-error-message-item-rm-could-not-be-fully-reserved-ensure-that-the-full-quantity-is-available-or-reserve-the-items-manually-if-the-reservation-field-on-the-bom-line-is-set-to-manual-or-started-could-not-release-the-order-to-warehouse-because-some-materials-could-not-be-reserved-however-the-status-is-updated-to-released"></a><span data-ttu-id="e4599-166">当我下达到仓库时，我收到以下错误消息：“物料 RM 无法完整预留。</span><span class="sxs-lookup"><span data-stu-id="e4599-166">When I release to a warehouse, I receive the following error message: "Item RM could not be fully reserved.</span></span> <span data-ttu-id="e4599-167">请确保全部数量都可用，或者如果物料清单行上的“预留”字段设置为“手动”或“已开始”，则手动预留物料。</span><span class="sxs-lookup"><span data-stu-id="e4599-167">Ensure that the full quantity is available, or reserve the items manually if the Reservation field on the BOM line is set to Manual or Started.</span></span> <span data-ttu-id="e4599-168">无法将订单下达到仓库，因为某些材料无法预留。”</span><span class="sxs-lookup"><span data-stu-id="e4599-168">Could not release the order to warehouse because some materials could not be reserved."</span></span> <span data-ttu-id="e4599-169">但是，状态会更新为“已下达”。</span><span class="sxs-lookup"><span data-stu-id="e4599-169">However, the status is updated to Released.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e4599-170">问题描述</span><span class="sxs-lookup"><span data-stu-id="e4599-170">Issue description</span></span>

<span data-ttu-id="e4599-171">如果在下达生产订单时，不是所有物料清单行项实际都可用，当生产订单上的 **发放到仓库** 策略设置为 *需要全部预留* 时，您将收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="e4599-171">If not all BOM line items are physically available when a production order is released, and the **Release to warehouse** policy is set to *Require full reservation* on the production order, you will receive the following error message:</span></span>

> <span data-ttu-id="e4599-172">物料 RM 无法完全预留。</span><span class="sxs-lookup"><span data-stu-id="e4599-172">Item RM could not be fully reserved.</span></span> <span data-ttu-id="e4599-173">请确保全部数量都可用，或者如果物料清单行上的“预留”字段设置为“手动”或“已开始”，则手动预留物料。</span><span class="sxs-lookup"><span data-stu-id="e4599-173">Ensure that the full quantity is available, or reserve the items manually if the Reservation field on the BOM line is set to Manual or Started.</span></span> <span data-ttu-id="e4599-174">无法将订单发放到仓库，因为某些材料无法预留。</span><span class="sxs-lookup"><span data-stu-id="e4599-174">Could not release the order to warehouse because some materials could not be reserved.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e4599-175">解决问题</span><span class="sxs-lookup"><span data-stu-id="e4599-175">Issue resolution</span></span>

<span data-ttu-id="e4599-176">此行为是有意设计的，属于正常工作。</span><span class="sxs-lookup"><span data-stu-id="e4599-176">This behavior is by design and is working as expected.</span></span>

## <a name="when-i-try-to-end-a-production-order-and-report-as-finished-i-receive-the-following-error-message-total-good-quantity-reported-as-finished-for-the-production-will-be-1-feedback-for-the-last-operation-is-000-in-total"></a><span data-ttu-id="e4599-177">当我尝试结束生产订单并报告完工入库时，我收到以下错误消息：“生产报告为完工入库的总计完好数量将是 %1。</span><span class="sxs-lookup"><span data-stu-id="e4599-177">When I try to end a production order and report as finished, I receive the following error message: "Total good quantity reported as finished for the production will be %1.</span></span> <span data-ttu-id="e4599-178">最后一道工序的反馈总计为 0.00 个。”</span><span class="sxs-lookup"><span data-stu-id="e4599-178">Feedback for the last operation is 0.00 in total."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e4599-179">问题描述</span><span class="sxs-lookup"><span data-stu-id="e4599-179">Issue description</span></span>

<span data-ttu-id="e4599-180">当您尝试在生产订单上过帐完工入库日记帐时，会收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="e4599-180">When you try to post a report as finished journal on a production order, you receive the following error message:</span></span>

> <span data-ttu-id="e4599-181">生产完工入库的完好数量合计将是 %1。</span><span class="sxs-lookup"><span data-stu-id="e4599-181">Total good quantity reported as finished for the production will be %1.</span></span> <span data-ttu-id="e4599-182">最后一道工序的反馈总计为 0.00 个。</span><span class="sxs-lookup"><span data-stu-id="e4599-182">Feedback for the last operation is 0.00 in total.</span></span>

### <a name="possible-cause"></a><span data-ttu-id="e4599-183">可能原因</span><span class="sxs-lookup"><span data-stu-id="e4599-183">Possible cause</span></span>

<span data-ttu-id="e4599-184">如果最后工序中过帐的数量不正确，将发生此问题。</span><span class="sxs-lookup"><span data-stu-id="e4599-184">This issue occurs if the quantities that were posted in the last operations were incorrect.</span></span> <span data-ttu-id="e4599-185">例如，如果生产已开始，但未分配必须开始的数量，工艺卡日记帐在过帐时将没有任何行。</span><span class="sxs-lookup"><span data-stu-id="e4599-185">For example, if production is started, but the quantity that must be started isn't allocated, the route card journal will be posted without any lines.</span></span> <span data-ttu-id="e4599-186">要确认情况，请打开生产订单，然后在操作窗格上的 **视图** 选项卡上，选择 **工艺卡**。</span><span class="sxs-lookup"><span data-stu-id="e4599-186">To confirm the situation, open the production order, and then, on the Action Pane, on the **View** tab, select **Route card**.</span></span>

### <a name="workaround"></a><span data-ttu-id="e4599-187">解决方法</span><span class="sxs-lookup"><span data-stu-id="e4599-187">Workaround</span></span>

<span data-ttu-id="e4599-188">您可以通过为日记帐未正确过帐的操作过帐其他日记帐来解决此问题。</span><span class="sxs-lookup"><span data-stu-id="e4599-188">You can fix this issue by posting additional journals for the operations that the journals weren't correctly posted for.</span></span> <span data-ttu-id="e4599-189">重新启动生产订单，然后选择过帐其他日记帐。</span><span class="sxs-lookup"><span data-stu-id="e4599-189">Restart the production order, and select to post the additional journals.</span></span> <span data-ttu-id="e4599-190">此操作不会启动生产订单，但会过帐日记帐。</span><span class="sxs-lookup"><span data-stu-id="e4599-190">This action won't start the production order, but it will post the journals.</span></span> <span data-ttu-id="e4599-191">然后，工艺卡应会显示已过帐的数量，您应该能够成功结束生产订单。</span><span class="sxs-lookup"><span data-stu-id="e4599-191">The route card should then show the quantities that were posted, and you should be able to end the production orders successfully.</span></span>

## <a name="can-i-report-a-production-order-as-finished-while-i-report-the-error-quantity-but-not-while-i-report-the-time-or-material-quantity"></a><span data-ttu-id="e4599-192">我可以在报告错误数量时将生产订单报告为完工入库，但在报告时间或物料数量时不这样报告吗？</span><span class="sxs-lookup"><span data-stu-id="e4599-192">Can I report a production order as finished while I report the error quantity, but not while I report the time or material quantity?</span></span>

<span data-ttu-id="e4599-193">您不能报告生产订单上的错误数量，除非您同时也报告了完好数量。</span><span class="sxs-lookup"><span data-stu-id="e4599-193">You can't report the error quantity on a production order unless you also report the good quantity.</span></span> <span data-ttu-id="e4599-194">**不** 支持此场景。</span><span class="sxs-lookup"><span data-stu-id="e4599-194">This scenario is **not** supported.</span></span> <span data-ttu-id="e4599-195">完工入库更新会在您尝试结束生产订单时最终失败，您将收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="e4599-195">The report as finished update will eventually fail when you try to end the production order, and you will receive the following error message:</span></span>

> <span data-ttu-id="e4599-196">缺少报告为完工入库的数量。</span><span class="sxs-lookup"><span data-stu-id="e4599-196">Missing report as finished quantity.</span></span>

## <a name="can-i-trace-the-serial-numbers-of-finished-goods-against-the-serial-numbers-of-consumed-goods"></a><span data-ttu-id="e4599-197">我可以根据消耗品的序列号跟踪成品的序列号吗？</span><span class="sxs-lookup"><span data-stu-id="e4599-197">Can I trace the serial numbers of finished goods against the serial numbers of consumed goods?</span></span>

<span data-ttu-id="e4599-198">您不能根据生产订单生产这些成品所消耗的物料的序列号来跟踪成品的序列号。</span><span class="sxs-lookup"><span data-stu-id="e4599-198">You can't trace the serial numbers of finished goods against the serial numbers of material that a production order consumes to make those finished goods.</span></span> <span data-ttu-id="e4599-199">当前不支持此场景。</span><span class="sxs-lookup"><span data-stu-id="e4599-199">This scenario isn't currently supported.</span></span> <span data-ttu-id="e4599-200">解决方法是创建数量为 1 的生产订单。</span><span class="sxs-lookup"><span data-stu-id="e4599-200">The workaround is to create production orders for a quantity of 1.</span></span>

---
title: 登陆成本报表
description: 本主题介绍如何查找和使用可用于登陆成本模块的各个类型的报表。
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 41588b7dc037f6d748bac818f8707540ce8afe8d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020951"
---
# <a name="landed-cost-reports"></a><span data-ttu-id="31365-103">登陆成本报表</span><span class="sxs-lookup"><span data-stu-id="31365-103">Landed cost reports</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="outstanding-invoices"></a><span data-ttu-id="31365-104">未清账单</span><span class="sxs-lookup"><span data-stu-id="31365-104">Outstanding invoices</span></span>

<span data-ttu-id="31365-105">未清发票报表包含与每个航行关联的各个成本级别的所有未清发票的列表。</span><span class="sxs-lookup"><span data-stu-id="31365-105">The outstanding invoices report contains a list of all outstanding invoices of the various cost levels that are associated with every voyage.</span></span> <span data-ttu-id="31365-106">它用于定期对航行和航行成本以及分类帐交易列表进行对帐。</span><span class="sxs-lookup"><span data-stu-id="31365-106">It's used to reconcile the voyage and voyage costs together with the ledger transactions list on a regular basis.</span></span> <span data-ttu-id="31365-107">为间接成本开票后，将从报表中将其删除。</span><span class="sxs-lookup"><span data-stu-id="31365-107">After an overhead cost has been invoiced, it's removed from the report.</span></span>

<span data-ttu-id="31365-108">若要生成未清发票报表，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="31365-108">To generate an outstanding invoices report, follow these steps.</span></span>

1. <span data-ttu-id="31365-109">转到 **登陆成本 \> 报表 \> 跟踪 \> 未清发票**。</span><span class="sxs-lookup"><span data-stu-id="31365-109">Go to **Landed cost \> Reports \> Tracking \> Outstanding invoices**.</span></span>
1. <span data-ttu-id="31365-110">在 **未清发票** 对话框中的 **截至日期** 字段中，指定一个日期。</span><span class="sxs-lookup"><span data-stu-id="31365-110">In the **Outstanding invoices** dialog box, in the **As at date** field, specify a date.</span></span> <span data-ttu-id="31365-111">在该日期或该日期之前未清的任何发票都将包含在输出中。</span><span class="sxs-lookup"><span data-stu-id="31365-111">Any invoice that was outstanding on or before that date will be included in the output.</span></span>
1. <span data-ttu-id="31365-112">在 **显示** 下，选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="31365-112">Under **Show**, select one of the following options:</span></span>

    - <span data-ttu-id="31365-113">**成本未开票** – 包括有估计成本值、但没有实际成本的已开票装运的成本。</span><span class="sxs-lookup"><span data-stu-id="31365-113">**Cost not invoiced** – Include costs for invoiced shipments that have an estimated cost value but no actual cost.</span></span>
    - <span data-ttu-id="31365-114">**存货未开票** – 包括已开票但采购订单尚未接收的成本。</span><span class="sxs-lookup"><span data-stu-id="31365-114">**Stock not invoiced** – Include costs that have been invoiced, but that the purchase order hasn't yet been received for.</span></span>
    - <span data-ttu-id="31365-115">**所有未开票** – 包括 **成本未开票** 选项和 **存货未开票** 选项的结果。</span><span class="sxs-lookup"><span data-stu-id="31365-115">**All not invoiced** – Include the results of both the **Cost not invoiced** option and the **Stock not invoiced** option.</span></span>

1. <span data-ttu-id="31365-116">将 **包括新成本** 选项设置为 *是*，将包括尚无实际成本且尚未接收库存的成本。</span><span class="sxs-lookup"><span data-stu-id="31365-116">Set the **Include new costs** option to *Yes* to include costs that don't yet have an actual cost, and that inventory hasn't been received for.</span></span> <span data-ttu-id="31365-117">如果将其设置为 *否*，报表将仅包括已开票的成本。</span><span class="sxs-lookup"><span data-stu-id="31365-117">If you set it to *No*, the report will include only costs that have been invoiced.</span></span>
1. <span data-ttu-id="31365-118">在 **视图** 部分，启用要包括在报表中的每个详细信息类型。</span><span class="sxs-lookup"><span data-stu-id="31365-118">In the **View** section, enable each type of detail that you want to include on the report.</span></span>
1. <span data-ttu-id="31365-119">与 Microsoft Dynamics 365 Supply Chain Management 中的其他类型报表一样，使用 **目标** 快速选项卡选择报表的输出格式。</span><span class="sxs-lookup"><span data-stu-id="31365-119">As you do for other types of reports in Microsoft Dynamics 365 Supply Chain Management, use the **Destination** FastTab to select the output format of the report.</span></span>
1. <span data-ttu-id="31365-120">与 Supply Chain Management 中的其他类型的报表一样，使用 **要包括的记录** 快速选项卡进一步限制将包含在报表中的记录。</span><span class="sxs-lookup"><span data-stu-id="31365-120">As you do for other types of reports in Supply Chain Management, use the **Records to include** FastTab to further limit the records that will be included on the report.</span></span>
1. <span data-ttu-id="31365-121">选择 **确定** 以生成报告。</span><span class="sxs-lookup"><span data-stu-id="31365-121">Select **OK** to generate the report.</span></span>

## <a name="activityprovider-analysis-reports"></a><span data-ttu-id="31365-122">活动/提供商分析报表</span><span class="sxs-lookup"><span data-stu-id="31365-122">Activity/provider analysis reports</span></span>

<span data-ttu-id="31365-123">活动/提供商分析报表让您可以查看每个提供商的时间估计的准确性。</span><span class="sxs-lookup"><span data-stu-id="31365-123">The activity/provider analysis reports let you review the accuracy of your time estimates for each provider.</span></span>

<span data-ttu-id="31365-124">若要生成活动/提供商分析报表，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="31365-124">To generate an activity/provider analysis report, follow these steps.</span></span>

1. <span data-ttu-id="31365-125">根据您要创建的报表的类型，按照下列步骤之一操作：</span><span class="sxs-lookup"><span data-stu-id="31365-125">Depending on the type of report that you want to create, follow one of these steps:</span></span>

    - <span data-ttu-id="31365-126">转到 **登陆成本 \> 报表 \> 按活动执行的活动/提供商分析**。</span><span class="sxs-lookup"><span data-stu-id="31365-126">Go to **Landed cost \> Reports \> Analysis of activity/provider by activity**.</span></span> <span data-ttu-id="31365-127">在这种情况下，时间估计将按活动分组。</span><span class="sxs-lookup"><span data-stu-id="31365-127">In this case, the time estimates will be grouped by activity.</span></span>
    - <span data-ttu-id="31365-128">转到 **登陆成本 \> 报表 \> 按提供商执行的活动/提供商分析**。</span><span class="sxs-lookup"><span data-stu-id="31365-128">Go to **Landed cost \> Reports \> Analysis of activity/provider by provider**.</span></span> <span data-ttu-id="31365-129">在这种情况下，时间估计将按提供商分组。</span><span class="sxs-lookup"><span data-stu-id="31365-129">In this case, the time estimates will be grouped by provider.</span></span>

    <span data-ttu-id="31365-130">**按活动执行的活动/提供商分析** 对话框或 **按提供商执行的活动/提供商分析** 对话框将出现。</span><span class="sxs-lookup"><span data-stu-id="31365-130">Either the **Analysis of activity/provider by activity** dialog box or the **Analysis of activity/provider by provider** dialog box appears.</span></span> <span data-ttu-id="31365-131">两个对话框提供相同的选项。</span><span class="sxs-lookup"><span data-stu-id="31365-131">Both dialog boxes provide the same options.</span></span>

1. <span data-ttu-id="31365-132">与 Supply Chain Management 中的其他类型报表一样，使用 **目标** 快速选项卡选择报表的输出格式。</span><span class="sxs-lookup"><span data-stu-id="31365-132">As you do for other types of reports in Supply Chain Management, use the **Destination** FastTab to select the output format of the report.</span></span>
1. <span data-ttu-id="31365-133">与 Supply Chain Management 中的其他类型的报表一样，使用 **要包括的记录** 快速选项卡进一步限制将包含在报表中的记录。</span><span class="sxs-lookup"><span data-stu-id="31365-133">As you do for other types of reports in Supply Chain Management, use the **Records to include** FastTab to further limit the records that will be included on the report.</span></span>
1. <span data-ttu-id="31365-134">选择 **确定** 以生成报告。</span><span class="sxs-lookup"><span data-stu-id="31365-134">Select **OK** to generate the report.</span></span>

## <a name="voyage-costing-reports"></a><span data-ttu-id="31365-135">航行成本计算报表</span><span class="sxs-lookup"><span data-stu-id="31365-135">Voyage costing reports</span></span>

<span data-ttu-id="31365-136">航行成本计算报表根据您在生成报表时选择的选项，显示物料的成本以及每个帐页、装运集装箱或航行的进口成本。</span><span class="sxs-lookup"><span data-stu-id="31365-136">The voyage costing reports show the cost of the items and the import costs per folio, shipping container, or voyage, depending on the options that you select when you generate the report.</span></span> <span data-ttu-id="31365-137">每个航行成本计算报表可以让您查看航行的估计成本与实际成本的比较，可以按几个确定因素分解。</span><span class="sxs-lookup"><span data-stu-id="31365-137">Each voyage costing report lets you view the estimated cost of a voyage versus the actual cost, and it can be broken down by the several identifying factors.</span></span>

<span data-ttu-id="31365-138">若要生成航行成本计算报表，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="31365-138">To generate a voyage costing report, follow these steps.</span></span>

1. <span data-ttu-id="31365-139">根据您要创建的报表的类型，按照下列步骤之一操作：</span><span class="sxs-lookup"><span data-stu-id="31365-139">Depending on the type of report that you want to create, follow one of these steps:</span></span>

    - <span data-ttu-id="31365-140">转到 **登陆成本 \> 报表 \> 成本计算 \> 按单个成本执行的航行成本计算**。</span><span class="sxs-lookup"><span data-stu-id="31365-140">Go to **Landed cost \> Reports \> Costing \> Voyage costing by individual cost**.</span></span> <span data-ttu-id="31365-141">在这种情况下，单个成本选项将按成本类型代码按成本区域显示进口成本。</span><span class="sxs-lookup"><span data-stu-id="31365-141">In this case, the individual cost option will show import costs per cost area per cost type code.</span></span>
    - <span data-ttu-id="31365-142">转到 **登陆成本 \> 报表 \> 成本计算 \> 按报告类别执行的航行成本计算**。</span><span class="sxs-lookup"><span data-stu-id="31365-142">Go to **Landed cost \> Reports \> Costing \> Voyage costing by reporting category**.</span></span> <span data-ttu-id="31365-143">在这种情况下，进口成本将分解为各个报告类别。</span><span class="sxs-lookup"><span data-stu-id="31365-143">In this case, the import cost will be broken down into the various reporting categories.</span></span> <span data-ttu-id="31365-144">成本类型按报告类别分组。</span><span class="sxs-lookup"><span data-stu-id="31365-144">Cost types are grouped by reporting categories.</span></span>

    <span data-ttu-id="31365-145">**按单个成本执行的航行成本计算** 对话框或 **按报告类别执行的航行成本计算** 对话框将出现。</span><span class="sxs-lookup"><span data-stu-id="31365-145">Either the **Voyage costing by individual cost** dialog box or the **Voyage costing by reporting category** dialog box appears.</span></span> <span data-ttu-id="31365-146">这些对话框比较相似。</span><span class="sxs-lookup"><span data-stu-id="31365-146">These dialog boxes are similar.</span></span> <span data-ttu-id="31365-147">此过程的其余部分说明了存在的所有差异。</span><span class="sxs-lookup"><span data-stu-id="31365-147">Any differences are noted in the rest of this procedure.</span></span>

1. <span data-ttu-id="31365-148">如果您打开了 **按报告类别执行的航行成本计算** 对话框，在 **成本** 字段中，选择以下值之一：</span><span class="sxs-lookup"><span data-stu-id="31365-148">If you opened the **Voyage costing by reporting category** dialog box, in the **Cost** field, select one of the following values:</span></span>

    - <span data-ttu-id="31365-149">**成本值** – 此值使用自动成本计算，或在成本区域手动创建。</span><span class="sxs-lookup"><span data-stu-id="31365-149">**Cost value** – The value is either calculated by using auto costs or manually created in the cost area.</span></span>
    - <span data-ttu-id="31365-150">**估计** – 接收货物后，设置估计成本。</span><span class="sxs-lookup"><span data-stu-id="31365-150">**Estimated** – After the goods have been received, the estimated cost is set.</span></span>
    - <span data-ttu-id="31365-151">**实际** – 订单开票后，实际成本设置为发票上的成本。</span><span class="sxs-lookup"><span data-stu-id="31365-151">**Actual** – After the order has been invoiced, the actual cost is set to the cost on the invoice.</span></span>
    - <span data-ttu-id="31365-152">**最佳** – 系统将使用前三个选项中最准确的一个。</span><span class="sxs-lookup"><span data-stu-id="31365-152">**Best** – The system will use whichever of the previous three options is most accurate.</span></span> <span data-ttu-id="31365-153">（我们建议您选择此选项。）</span><span class="sxs-lookup"><span data-stu-id="31365-153">(We recommend that you select this option.)</span></span>

1. <span data-ttu-id="31365-154">将 **按物料** 选项设置为 *是* 将显示每个物料的成本。</span><span class="sxs-lookup"><span data-stu-id="31365-154">Set the **Per item** option to *Yes* to show the cost of each item.</span></span> <span data-ttu-id="31365-155">设置为 *否* 将按航行显示成本。</span><span class="sxs-lookup"><span data-stu-id="31365-155">Set it to *No* to show costs per voyage.</span></span>
1. <span data-ttu-id="31365-156">在 **视图** 部分，选择要按其分解成本的类别。</span><span class="sxs-lookup"><span data-stu-id="31365-156">In the **View** section, select the categories to break down the cost by.</span></span>
1. <span data-ttu-id="31365-157">在 **维度** 部分，选择要包含在报表中的维度。</span><span class="sxs-lookup"><span data-stu-id="31365-157">In the **Dimensions** section, select the dimensions to include on the report.</span></span>
1. <span data-ttu-id="31365-158">与 Supply Chain Management 中的其他类型报表一样，使用 **目标** 快速选项卡选择报表的输出格式。</span><span class="sxs-lookup"><span data-stu-id="31365-158">As you do for other types of reports in Supply Chain Management, use the **Destination** FastTab to select the output format of the report.</span></span>
1. <span data-ttu-id="31365-159">与 Supply Chain Management 中的其他类型的报表一样，使用 **要包括的记录** 快速选项卡进一步限制将包含在报表中的记录。</span><span class="sxs-lookup"><span data-stu-id="31365-159">As you do for other types of reports in Supply Chain Management, use the **Records to include** FastTab to further limit the records that will be included on the report.</span></span>
1. <span data-ttu-id="31365-160">选择 **确定** 以生成报告。</span><span class="sxs-lookup"><span data-stu-id="31365-160">Select **OK** to generate the report.</span></span>

## <a name="shipping-container-receipts-list"></a><span data-ttu-id="31365-161">装运集装箱收货清单</span><span class="sxs-lookup"><span data-stu-id="31365-161">Shipping container receipts list</span></span>

<span data-ttu-id="31365-162">装运集装箱收货清单包含所有在预期日期或之前到期的未接收数量。</span><span class="sxs-lookup"><span data-stu-id="31365-162">The shipping container receipts list contains all unreceived quantities that are due on or before an expected date.</span></span> <span data-ttu-id="31365-163">仓库员工可以使用此报表来确定装运集装箱上的预期货物。</span><span class="sxs-lookup"><span data-stu-id="31365-163">Warehouse staff can use this report to identify the expected goods on a shipping container.</span></span> <span data-ttu-id="31365-164">它还可以用来在装运集装箱上接收货物时手动验证货物。</span><span class="sxs-lookup"><span data-stu-id="31365-164">It can also be used to manually validate goods as they are received on a shipping container.</span></span>

<span data-ttu-id="31365-165">要生成装运集装箱收货清单，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="31365-165">To generate a shipping container receipts list, follow these steps.</span></span>

1. <span data-ttu-id="31365-166">转到 **登陆成本 \> 报表 \> 跟踪 \> 装运集装箱收货清单**。</span><span class="sxs-lookup"><span data-stu-id="31365-166">Go to **Landed cost \> Reports \> Tracking \> Shipping container receipts list**.</span></span>
1. <span data-ttu-id="31365-167">在 **装运集装箱收货清单** 对话框中的 **预期日期** 字段中，指定一个日期。</span><span class="sxs-lookup"><span data-stu-id="31365-167">In the **Shipping container receipts list** dialog box, in the **Expected date** field, specify a date.</span></span> <span data-ttu-id="31365-168">在该日期或该日期之前未接收的任何数量都将包含在输出中。</span><span class="sxs-lookup"><span data-stu-id="31365-168">Any quantities that were unreceived on or before that date will be included in the output.</span></span>
1. <span data-ttu-id="31365-169">在 **维度** 部分，选择要包含在报表中的维度。</span><span class="sxs-lookup"><span data-stu-id="31365-169">In the **Dimensions** section, select the dimensions to include on the report.</span></span>
1. <span data-ttu-id="31365-170">与 Supply Chain Management 中的其他类型报表一样，使用 **目标** 快速选项卡选择报表的输出格式。</span><span class="sxs-lookup"><span data-stu-id="31365-170">As you do for other types of reports in Supply Chain Management, use the **Destination** FastTab to select the output format of the report.</span></span>
1. <span data-ttu-id="31365-171">与 Supply Chain Management 中的其他类型的报表一样，使用 **要包括的记录** 快速选项卡进一步限制将包含在报表中的记录。</span><span class="sxs-lookup"><span data-stu-id="31365-171">As you do for other types of reports in Supply Chain Management, use the **Records to include** FastTab to further limit the records that will be included on the report.</span></span>
1. <span data-ttu-id="31365-172">选择 **确定** 以生成报告。</span><span class="sxs-lookup"><span data-stu-id="31365-172">Select **OK** to generate the report.</span></span>

## <a name="expected-delivery-report"></a><span data-ttu-id="31365-173">预期交货报表</span><span class="sxs-lookup"><span data-stu-id="31365-173">Expected delivery report</span></span>

<span data-ttu-id="31365-174">预期交货报表包含有关航行、装运集装箱、帐页、物料和预期交货日期的基本信息。</span><span class="sxs-lookup"><span data-stu-id="31365-174">The expected delivery report contains basic information about the voyage, shipping container, folio, items, and expected date of delivery.</span></span>

<span data-ttu-id="31365-175">若要生成预期交货报表，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="31365-175">To generate an expected delivery report, follow these steps.</span></span>

1. <span data-ttu-id="31365-176">转到 **登陆成本 \> 报表 \> 跟踪 \> 预期交货**。</span><span class="sxs-lookup"><span data-stu-id="31365-176">Go to **Landed cost \> Reports \> Tracking \> Expected Delivery**.</span></span>
1. <span data-ttu-id="31365-177">在 **预期交货** 对话框的 **预期日期** 字段中，选择预计货物交付到最终目标仓库的日期。</span><span class="sxs-lookup"><span data-stu-id="31365-177">In the **Expected delivery** dialog box, in the **Expected date** field, select the date when delivery of the goods to the final destination warehouse is expected.</span></span> <span data-ttu-id="31365-178">日期为预期日期或在该日期之前的尚未接收的任何航行行都将包含在输出中。</span><span class="sxs-lookup"><span data-stu-id="31365-178">Any voyage line that has an expected date on or before that date, and that hasn't yet been received, will be included in the output.</span></span>
1. <span data-ttu-id="31365-179">可选：在 **供应商帐户** 字段中，选择一个供应商帐户以仅包括来自特定供应商的交货。</span><span class="sxs-lookup"><span data-stu-id="31365-179">Optional: In the **Vendor account** field, select a vendor account to include only deliveries from a specific vendor.</span></span>
1. <span data-ttu-id="31365-180">在 **维度** 部分，选择要包含在报表中的维度。</span><span class="sxs-lookup"><span data-stu-id="31365-180">In the **Dimensions** section, select the dimensions to include on the report.</span></span>
1. <span data-ttu-id="31365-181">与 Supply Chain Management 中的其他类型报表一样，使用 **目标** 快速选项卡选择报表的输出格式。</span><span class="sxs-lookup"><span data-stu-id="31365-181">As you do for other types of reports in Supply Chain Management, use the **Destination** FastTab to select the output format of the report.</span></span>
1. <span data-ttu-id="31365-182">与 Supply Chain Management 中的其他类型的报表一样，使用 **要包括的记录** 快速选项卡进一步限制将包含在报表中的记录。</span><span class="sxs-lookup"><span data-stu-id="31365-182">As you do for other types of reports in Supply Chain Management, use the **Records to include** FastTab to further limit the records that will be included on the report.</span></span>
1. <span data-ttu-id="31365-183">选择 **确定** 以生成报告。</span><span class="sxs-lookup"><span data-stu-id="31365-183">Select **OK** to generate the report.</span></span>

---
title: 使用情况管理仪表板
description: 本主题说明如何通过使用情况管理仪表板监视电子开票服务的使用情况并保持合规性。
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130498"
---
# <a name="usage-management-dashboard"></a><span data-ttu-id="2a5fc-103">使用情况管理仪表板</span><span class="sxs-lookup"><span data-stu-id="2a5fc-103">Usage management dashboard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a5fc-104">**使用情况管理** 仪表板帮助您监视电子开票服务的使用情况，从而帮助您的组织在其每月使用情况方面保持合规性。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-104">The **Usage management** dashboard helps you monitor usage of the Electronic Invoicing service, and therefore helps your organization remain compliant in terms of its monthly usage.</span></span> <span data-ttu-id="2a5fc-105">通过计算提交量并将其与获取的提交量进行比较来确定获取量和使用量之间的任何偏差，从而确定合规性。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-105">Compliance is determined by calculating the submission volume and comparing it with the acquired volume of submissions to identify any deviations between the acquired volume and the used volume.</span></span>

<span data-ttu-id="2a5fc-106">仪表板包括以下指标：</span><span class="sxs-lookup"><span data-stu-id="2a5fc-106">The dashboard includes the following indicators:</span></span>

- <span data-ttu-id="2a5fc-107">一个成本指标，可用于出于许可合规性目的监视消耗量：</span><span class="sxs-lookup"><span data-stu-id="2a5fc-107">One cost indicator that you can use to monitor consumption for licensing compliance purposes:</span></span>

    - <span data-ttu-id="2a5fc-108">每月使用情况(导出)</span><span class="sxs-lookup"><span data-stu-id="2a5fc-108">Usage per month (export)</span></span>

- <span data-ttu-id="2a5fc-109">三个运营指标，可用于出于管理目的跟踪电子开票服务的使用情况：</span><span class="sxs-lookup"><span data-stu-id="2a5fc-109">Three operational indicators that you can use to track usage of the Electronic Invoicing service for management purposes:</span></span>

    - <span data-ttu-id="2a5fc-110">按功能排列的使用情况</span><span class="sxs-lookup"><span data-stu-id="2a5fc-110">Usage by feature</span></span>
    - <span data-ttu-id="2a5fc-111">按环境排列的使用情况</span><span class="sxs-lookup"><span data-stu-id="2a5fc-111">Usage by environment</span></span>
    - <span data-ttu-id="2a5fc-112">每月使用情况(导入)</span><span class="sxs-lookup"><span data-stu-id="2a5fc-112">Usage per month (import)</span></span>

## <a name="measurement-scope"></a><span data-ttu-id="2a5fc-113">度量范围</span><span class="sxs-lookup"><span data-stu-id="2a5fc-113">Measurement scope</span></span>

- <span data-ttu-id="2a5fc-114">度量单位：</span><span class="sxs-lookup"><span data-stu-id="2a5fc-114">Unit of measure:</span></span> 

    <span data-ttu-id="2a5fc-115">**使用情况管理** 仪表板计入业务单据的提交和导入的电子发票。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-115">The **Usage management** dashboard counts the submission of business documents and imported electronic invoices.</span></span>

- <span data-ttu-id="2a5fc-116">组织:</span><span class="sxs-lookup"><span data-stu-id="2a5fc-116">Organization:</span></span> 

    <span data-ttu-id="2a5fc-117">计数由您的组织的租户 ID 汇总，而不管 Microsoft Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 的实例数或启用电子开票服务的法人数。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-117">Counting is summarized by the tenant ID of your organization, regardless of the number of instances of Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management, or the number of legal entities where the Electronic Invoicing service is enabled.</span></span>


## <a name="indicator-usage-per-month-export"></a><span data-ttu-id="2a5fc-118">指标：每月使用情况（导出）</span><span class="sxs-lookup"><span data-stu-id="2a5fc-118">Indicator: Usage per month (export)</span></span>

<span data-ttu-id="2a5fc-119">此指标提供有关您的组织在定义期间发出的电子发票的详细信息。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-119">This indicator provides details about the electronic invoices that your organization issues during a defined period.</span></span>

### <a name="scope"></a><span data-ttu-id="2a5fc-120">范围</span><span class="sxs-lookup"><span data-stu-id="2a5fc-120">Scope</span></span>
- <span data-ttu-id="2a5fc-121">从 Finance 和 Supply Chain Management 提交到电子开票服务的业务单据数，而不管这些业务单据包含的行数。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-121">The number of business documents that are submitted from Finance and Supply Chain Management to the Electronic Invoicing service, regardless of number of lines that those business documents contain.</span></span>
- <span data-ttu-id="2a5fc-122">由电子开票服务成功处理的已提交业务单据数。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-122">The number of submitted business documents that are successfully processed by the Electronic Invoicing service.</span></span> <span data-ttu-id="2a5fc-123">当在功能设置中定义的操作流完成时，将单据视为已成功处理。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-123">A document is considered successfully processed when the flow of actions that are defined in the feature setup is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="2a5fc-124">当电子发票提交到外部 Web 服务时，计入与 Web 服务处理的结果（接受、拒绝或架构验证错误）无关。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-124">When an electronic invoice is submitted to an external web service, counting is independent of the results of web service processing (accepted, rejected, or schema validation error).</span></span> <span data-ttu-id="2a5fc-125">如果 Web 服务收到并响应来自电子开票服务的请求，将提交视为有效计数。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-125">If the web service received and responded to the request from the Electronic Invoicing service, the submission is considered a valid counting.</span></span>

- <span data-ttu-id="2a5fc-126">**例外：** 如果将业务单据从 Finance 和 Supply Chain Management 重新提交到电子开票服务（例如，在需要重新提交相同的业务单据以更改电子发票状态的情况下），将不计入业务单据。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-126">**Exception:** Business documents aren't counted if they are resubmitted from Finance and Supply Chain Management to the Electronic Invoicing service, such as in the scenarios where a resubmission of the same business document is required to change the status of the electronic invoice.</span></span> <span data-ttu-id="2a5fc-127">例如，巴西电子发票（会计单据）的开具将计入为有效，但在请求取消时不计入。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-127">For example, issuance of a Brazilian electronic invoice (fiscal document) is counted as valid, but the cancellation request for it isn't counted.</span></span>


### <a name="calculation"></a><span data-ttu-id="2a5fc-128">计算</span><span class="sxs-lookup"><span data-stu-id="2a5fc-128">Calculation</span></span>

<span data-ttu-id="2a5fc-129">余额的计算方法如下：</span><span class="sxs-lookup"><span data-stu-id="2a5fc-129">The calculation of the balance is calculated as follows:</span></span>

<span data-ttu-id="2a5fc-130">余额 = 免费 + 已采购 - 已使用</span><span class="sxs-lookup"><span data-stu-id="2a5fc-130">Balance = Free + Purchased – Used</span></span>

<span data-ttu-id="2a5fc-131">其中：</span><span class="sxs-lookup"><span data-stu-id="2a5fc-131">Where:</span></span>

- <span data-ttu-id="2a5fc-132">免费：</span><span class="sxs-lookup"><span data-stu-id="2a5fc-132">Free:</span></span>
  
    <span data-ttu-id="2a5fc-133">客户每月可以免费提交的业务单据量。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-133">A free volume of business documents the customer can submit per month.</span></span> <span data-ttu-id="2a5fc-134">它包括可提交给电子开票服务的 100 个业务单据包。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-134">It includes a package of 100 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="2a5fc-135">免费量不会累积，任何剩余余额都不会转入下一个期间。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-135">Free volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="2a5fc-136">已采购：</span><span class="sxs-lookup"><span data-stu-id="2a5fc-136">Purchased:</span></span>
  
    <span data-ttu-id="2a5fc-137">可提交给电子开票服务的 1,000 个业务单据包。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-137">A package of 1,000 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="2a5fc-138">必须每月为您的组织购买此包。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-138">This package must be acquired for your organization on a monthly basis.</span></span> <span data-ttu-id="2a5fc-139">购买量不会累积，任何剩余余额都不会转入下一个期间。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-139">Purchased volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="2a5fc-140">已使用：</span><span class="sxs-lookup"><span data-stu-id="2a5fc-140">Used:</span></span> 

    <span data-ttu-id="2a5fc-141">根据定义的条件提交到电子开票服务的业务单据的计数。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-141">The count of business document submissions to the Electronic Invoicing service according to defined criteria.</span></span>
   
> [!IMPORTANT]
> <span data-ttu-id="2a5fc-142">如果您的组织计划超过每月的 100 个免费提交量，请购买峰值量以确保您始终遵守 Microsoft 电子开票服务许可策略。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-142">If your organization plans to exceed the monthly volume of 100 free submissions, purchase the peak volume to ensure that you remain compliant with the Microsoft licensing policy for the Electronic Invoicing service.</span></span>
>
> <span data-ttu-id="2a5fc-143">目前，必须根据购置日期手动输入购买量，以作为 1,000 个提交的多个包。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-143">Currently, purchased volume must be manually entered, according to the date of acquisition, as multiple packages of 1,000 submissions.</span></span>

## <a name="indicator-usage-by-feature"></a><span data-ttu-id="2a5fc-144">指标：按功能排列的使用情况</span><span class="sxs-lookup"><span data-stu-id="2a5fc-144">Indicator: Usage by feature</span></span>

<span data-ttu-id="2a5fc-145">该指标显示在定义的时间段内用于开具电子发票的电子开票功能的使用情况。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-145">This indicator shows the usage of electronic invoicing features for issuance of electronic invoices during a defined period.</span></span>

- <span data-ttu-id="2a5fc-146">计算：</span><span class="sxs-lookup"><span data-stu-id="2a5fc-146">Calculation:</span></span>
  
    <span data-ttu-id="2a5fc-147">已使用 = 在向电子开票服务提交业务单据期间使用的每个电子开票功能的次数。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-147">Used = The count of how many times each electronic invoicing feature was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-by-environment"></a><span data-ttu-id="2a5fc-148">指标：按环境排列的使用情况</span><span class="sxs-lookup"><span data-stu-id="2a5fc-148">Indicator: Usage by environment</span></span>

<span data-ttu-id="2a5fc-149">该指标显示在定义的时间段内电子开票服务环境的使用情况。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-149">This indicator shows the usage of electronic invoicing service environments during a defined period.</span></span>

- <span data-ttu-id="2a5fc-150">计算：</span><span class="sxs-lookup"><span data-stu-id="2a5fc-150">Calculation:</span></span>
    
    <span data-ttu-id="2a5fc-151">已使用 = 在向电子开票服务提交业务单据期间使用的每个电子开票服务环境的次数。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-151">Used = The count of how many times each electronic invoicing service environment was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-per-month-import"></a><span data-ttu-id="2a5fc-152">指标：每月使用情况（导入）</span><span class="sxs-lookup"><span data-stu-id="2a5fc-152">Indicator: Usage per month (import)</span></span>

<span data-ttu-id="2a5fc-153">该指标显示在定义的时间段内通过电子开票服务将电子发票导入 Finance 和 Supply Chain Management 的数量。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-153">This indicator shows the volume of importation of electronic invoices by Electronic Invoicing service into Finance and Supply Chain Management during a defined period.</span></span>

- <span data-ttu-id="2a5fc-154">范围：</span><span class="sxs-lookup"><span data-stu-id="2a5fc-154">Scope:</span></span>

    <span data-ttu-id="2a5fc-155">导入 Finance 和 Supply Chain Management 的电子发票，无论这些电子发票包含多少行。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-155">Electronic invoices that are imported into Finance and Supply Chain Management, regardless of the number of lines that those electronic invoices contain.</span></span>

- <span data-ttu-id="2a5fc-156">计算：</span><span class="sxs-lookup"><span data-stu-id="2a5fc-156">Calculation:</span></span>

    <span data-ttu-id="2a5fc-157">已接收 = 导入 Finance 和 Supply Chain Management 中的电子发票计数。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-157">Received = The count of imported electronic invoices into Finance and Supply Chain Management.</span></span>

## <a name="functions"></a><span data-ttu-id="2a5fc-158">功能</span><span class="sxs-lookup"><span data-stu-id="2a5fc-158">Functions</span></span>
### <a name="purchase"></a><span data-ttu-id="2a5fc-159">采购</span><span class="sxs-lookup"><span data-stu-id="2a5fc-159">Purchase</span></span>

<span data-ttu-id="2a5fc-160">在 **每月使用情况（导出）** 选项卡上，选择 **购买** 以手动登记获取的提交量。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-160">On the **Usage per month (export)** tab, select **Purchase** to manually register the amount of acquired submissions.</span></span>

<span data-ttu-id="2a5fc-161">对于给定的日期，选择 **新建**，然后输入针对该日期获取的 **包** 数。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-161">For a given date, select **New** and enter the number of **Packages** acquired for on that date.</span></span>

<span data-ttu-id="2a5fc-162">按如下所示计算 **数量**：</span><span class="sxs-lookup"><span data-stu-id="2a5fc-162">The **Quantity** is calculated as:</span></span>

<span data-ttu-id="2a5fc-163">数量 = 包 \* 1.000</span><span class="sxs-lookup"><span data-stu-id="2a5fc-163">Quantity = Packages \* 1.000</span></span>

<span data-ttu-id="2a5fc-164">计算的 **数量** 反映在指标 **每月使用情况（导出）** 的 **已采购** 中。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-164">The calculated **Quantity** reflects in the **Purchased** from the indicator **Usage per month (export)**.</span></span>

### <a name="update"></a><span data-ttu-id="2a5fc-165">更新</span><span class="sxs-lookup"><span data-stu-id="2a5fc-165">Update</span></span>

<span data-ttu-id="2a5fc-166">在操作窗格上，选择 **更新** 以刷新计算并更新页面和图表中显示的数据。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-166">On the Action Pane, select **Update** to refresh the calculation and update the data shown on the page and in the chart.</span></span>

### <a name="reset-history-data"></a><span data-ttu-id="2a5fc-167">重置历史记录数据</span><span class="sxs-lookup"><span data-stu-id="2a5fc-167">Reset history data</span></span>

<span data-ttu-id="2a5fc-168">在操作窗格上，选择 **重置历史数据** 以刷新从中计算指标的数据库。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-168">On the Action Pane, select **Reset history data** to refresh the database from where the indicators are calculated.</span></span>




> [!NOTE]
> <span data-ttu-id="2a5fc-169">**使用情况管理** 仪表板不显示货币金额。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-169">The **Usage management** dashboard doesn't show monetary amounts.</span></span> <span data-ttu-id="2a5fc-170">相反，它仅显示计数的提交和导入的单据的数量。</span><span class="sxs-lookup"><span data-stu-id="2a5fc-170">Instead, it shows only the volume of counted submissions and imported documents.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

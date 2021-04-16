---
title: 将账单提交至工作流系统并匹配物料收货行
description: 本主题介绍了将供应商发票提交到工作流系统，并自动将过帐的物料收货行与供应商发票进行匹配的流程。
author: abruer
ms.date: 09/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 84699746349024854a4eeb9cee62960ec38bc338
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827810"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines"></a><span data-ttu-id="bce1a-103">将账单提交至工作流系统并匹配物料收货行</span><span class="sxs-lookup"><span data-stu-id="bce1a-103">Submit invoices to the workflow system and match product receipt lines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bce1a-104">本主题介绍了将供应商发票提交到工作流系统，并自动将过帐的物料收货行与供应商发票进行匹配的流程。</span><span class="sxs-lookup"><span data-stu-id="bce1a-104">This topic explains the process of submitting vendor invoices to the workflow system and automatically matching posted product receipt lines to vendor invoices.</span></span>

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a><span data-ttu-id="bce1a-105">将导入的供应商发票提交到工作流系统，并将过帐的物料收货行与待处理的供应商发票行进行匹配</span><span class="sxs-lookup"><span data-stu-id="bce1a-105">Submitting imported vendor invoices to the workflow system and matching posted product receipt lines to pending vendor invoice lines</span></span>

<span data-ttu-id="bce1a-106">作为非接触式应付帐款开票流程的一部分，您可以让系统自动将导入的发票提交到工作流系统。</span><span class="sxs-lookup"><span data-stu-id="bce1a-106">As part of a touchless Accounts payable invoicing process, you can have the system automatically submit an imported invoice to the workflow system.</span></span> <span data-ttu-id="bce1a-107">您可以在 **应付帐款参数** 页面（**应付帐款 \> 设置 \> 应付帐款参数**）的 **供应商发票自动化** 选项卡上配置将导入的发票提交到工作流系统的流程。</span><span class="sxs-lookup"><span data-stu-id="bce1a-107">You can configure the process of submitting imported invoices to the workflow system on the **Vendor invoice automation** tab of the **Accounts payable parameters** page (**Accounts payable \> Setup \> Accounts payable parameters**).</span></span> <span data-ttu-id="bce1a-108">提交到工作流程将以您指定的频率（每小时或每天）在后台运行。</span><span class="sxs-lookup"><span data-stu-id="bce1a-108">The submit-to-workflow process will run in the background, at a frequency that you specify (either hourly or daily).</span></span>

<span data-ttu-id="bce1a-109">当您自动将发票提交到工作流系统时，必须从导入的发票开始。</span><span class="sxs-lookup"><span data-stu-id="bce1a-109">When you automatically submit invoices to the workflow system, you must begin with an imported invoice.</span></span> <span data-ttu-id="bce1a-110">为了确保整个发票处理流程都没有人工干预，您必须在工作流配置中包括自动化过帐任务。</span><span class="sxs-lookup"><span data-stu-id="bce1a-110">To ensure that the invoice can be processed from start to finish without manual intervention, you must include an automated posting task in the workflow configuration.</span></span> <span data-ttu-id="bce1a-111">可以将与采购订单 (PO) 相关的发票以及包含非 PO 采购类别和非贮存行的发票自动提交到工作流系统。</span><span class="sxs-lookup"><span data-stu-id="bce1a-111">Invoices that are related to purchase orders (POs), and invoices that contain a non-PO procurement category and non-stocked lines, can automatically be submitted to the workflow system.</span></span> <span data-ttu-id="bce1a-112">手动输入的发票必须手动提交到工作流系统。</span><span class="sxs-lookup"><span data-stu-id="bce1a-112">Invoices that are manually entered must be manually submitted to the workflow system.</span></span>

<span data-ttu-id="bce1a-113">工作流中的 **提交者** 值是在 **流程自动化** 页面上为 **将供应商发票提交到工作流** 后台任务输入的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="bce1a-113">The **Submitted by** value in the workflow is the user ID that was entered for the **Submit vendor invoices to workflow** background task on the **Process automation** page.</span></span> <span data-ttu-id="bce1a-114">具有该用户 ID 的用户将能够根据需要从工作流系统中撤回发票。</span><span class="sxs-lookup"><span data-stu-id="bce1a-114">The user who has that user ID will be able to recall the invoice from the workflow system as required.</span></span>

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a><span data-ttu-id="bce1a-115">将过帐的物料收货与具有三向匹配政策的发票行进行匹配</span><span class="sxs-lookup"><span data-stu-id="bce1a-115">Matching posted product receipts to invoice lines that have a three-way matching policy</span></span>

<span data-ttu-id="bce1a-116">作为非接触式应付帐款开票流程的一部分，系统可以自动将过帐的物料收货与发票行进行匹配。</span><span class="sxs-lookup"><span data-stu-id="bce1a-116">As part of a touchless Accounts payable invoicing process, the system can automatically match posted product receipts to invoice lines.</span></span> <span data-ttu-id="bce1a-117">必须为此任务定义三向匹配政策。</span><span class="sxs-lookup"><span data-stu-id="bce1a-117">A three-way matching policy must be defined for this task.</span></span> <span data-ttu-id="bce1a-118">如果已在 **功能管理** 页面上启用了 **供应商发票自动化** 功能，则此功能可用。</span><span class="sxs-lookup"><span data-stu-id="bce1a-118">This feature is available if the **Vendor invoice automation** feature has been enabled on the **Feature management** page.</span></span>

<span data-ttu-id="bce1a-119">将运行匹配流程，直到匹配的产品收货数量等于发票数量。</span><span class="sxs-lookup"><span data-stu-id="bce1a-119">The matching process will run until the matched product receipt quantity equals the invoice quantity.</span></span> <span data-ttu-id="bce1a-120">但是，如果单个发票行有多个产品收货，则需要多次运行该流程以实现全部数量匹配。</span><span class="sxs-lookup"><span data-stu-id="bce1a-120">However, if there are multiple product receipts for a single invoice line, you’ll need to run the process multiple times to achieve the full quantity match.</span></span> <span data-ttu-id="bce1a-121">您可以指定系统在得出流程失败的结论之前应尝试将产品收货与发票行进行匹配的最大次数。</span><span class="sxs-lookup"><span data-stu-id="bce1a-121">You can specify the maximum number of times that the system should try to match product receipts to an invoice line before it concludes that the process failed.</span></span> <span data-ttu-id="bce1a-122">该流程将以每小时或每天的频率在后台运行。</span><span class="sxs-lookup"><span data-stu-id="bce1a-122">The process will run in the background, either hourly or daily.</span></span> 

<span data-ttu-id="bce1a-123">您可以在将发票提交到工作流系统的流程中运行自动化匹配流程。</span><span class="sxs-lookup"><span data-stu-id="bce1a-123">You can run the automated matching process as part of the process for submitting invoices to the workflow system.</span></span> <span data-ttu-id="bce1a-124">或者，您可以将其作为独立流程运行。</span><span class="sxs-lookup"><span data-stu-id="bce1a-124">Alternatively, you can run it as a standalone process.</span></span> <span data-ttu-id="bce1a-125">在 **应付帐款参数** 页面（**应付帐款 \> 设置 \> 应付帐款参数**）的 **供应商发票自动化** 选项卡上配置将物料收货与发票行进行匹配流程的设置。</span><span class="sxs-lookup"><span data-stu-id="bce1a-125">The settings for the match-product-receipts-to-invoice-lines process are configured on the **Vendor invoice automation** tab of the **Accounts payable parameters** page (**Accounts payable \> Setup \> Accounts payable parameters**).</span></span>

<span data-ttu-id="bce1a-126">具有三向匹配政策的发票行（匹配的收货数量小于发票数量）将包括在自动匹配到物料收货流程中。</span><span class="sxs-lookup"><span data-stu-id="bce1a-126">Invoice lines that have a three-way matching policy, where the matched receipt quantity is less than the invoice quantity, will be included in the automated match-to-product-receipt process.</span></span>

<span data-ttu-id="bce1a-127">若要查看不属于自动提交到工作流程的发票的 **最近一次匹配** 状态，请从 **供应商发票** 页面中打开发票。</span><span class="sxs-lookup"><span data-stu-id="bce1a-127">To view the **Last match** status for invoices that aren't part of the automated submit-to-workflow process, open the invoice from the **Vendor invoices** page.</span></span> <span data-ttu-id="bce1a-128">当查看发票时，将更新匹配的验证信息。</span><span class="sxs-lookup"><span data-stu-id="bce1a-128">When you view the invoice, the matching validation information is updated.</span></span> <span data-ttu-id="bce1a-129">**最近一次匹配** 状态可以使用 **验证发票匹配** 后台任务自动更新。</span><span class="sxs-lookup"><span data-stu-id="bce1a-129">The **Last match** status can be updated automatically using the **Validate invoice matching** background task.</span></span> <span data-ttu-id="bce1a-130">您可以在 **流程自动化** 页的 **后台流程** 选项卡上配置自动更新 **最近一次匹配** 状态的流程（**系统管理 \> 设置 \> 流程自动化**）。</span><span class="sxs-lookup"><span data-stu-id="bce1a-130">You can configure the process of automatically updating the **Last match** status on the **Background processes** tab of the **Process automations** page (**System adminstration\> Setup\> Process automations**).</span></span>

<span data-ttu-id="bce1a-131">如果满足以下任一条件，将从自动化流程中排除发票行：</span><span class="sxs-lookup"><span data-stu-id="bce1a-131">An invoice line will be excluded from the automated processing if any of the following conditions are met:</span></span>

- <span data-ttu-id="bce1a-132">发票行的 **自动化收货匹配状态** 值为 **失败**。</span><span class="sxs-lookup"><span data-stu-id="bce1a-132">The **Automated receipt match status** value of the invoice line is **Failed**.</span></span>
- <span data-ttu-id="bce1a-133">发票正在使用中。</span><span class="sxs-lookup"><span data-stu-id="bce1a-133">The invoice is being used.</span></span>
- <span data-ttu-id="bce1a-134">发票在工作流系统中。</span><span class="sxs-lookup"><span data-stu-id="bce1a-134">The invoice is in the workflow system.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

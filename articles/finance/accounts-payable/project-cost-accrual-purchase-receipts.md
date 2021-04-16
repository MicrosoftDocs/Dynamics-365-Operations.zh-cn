---
title: 采购收据中的应计项目成本
description: 此主题介绍如何在 Microsoft Dynamics 365 Finance 中跟踪采购收据内的应计项目成本。
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 615e22234323e2235fba002c50f9ab9c230c021e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827882"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="18113-103">采购收据中的应计项目成本</span><span class="sxs-lookup"><span data-stu-id="18113-103">Project cost accrual on purchase receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18113-104">此主题介绍如何在 Microsoft Dynamics 365 Finance 中跟踪采购收据内的应计项目成本。</span><span class="sxs-lookup"><span data-stu-id="18113-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 Finance.</span></span> 

<span data-ttu-id="18113-105">项目的发票通常比货物和服务的交付时间晚，这可能对项目关键绩效指标 (KPI) 造成极大影响。</span><span class="sxs-lookup"><span data-stu-id="18113-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="18113-106">在财务报表和产品报表中跟踪这些交易记录的能力至关重要。</span><span class="sxs-lookup"><span data-stu-id="18113-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="18113-107">以下示例方案对此进行了说明。</span><span class="sxs-lookup"><span data-stu-id="18113-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="18113-108">Contoso Consulting 已启动了一个新的云部署项目。</span><span class="sxs-lookup"><span data-stu-id="18113-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="18113-109">创建了采购订单，以便为该项目购买一台计算机。</span><span class="sxs-lookup"><span data-stu-id="18113-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="18113-110">该计算机成本为 1500 美元，安装服务为 150 美元。</span><span class="sxs-lookup"><span data-stu-id="18113-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="18113-111">供应商已交货并安装了计算机，但是 Contoso Consulting 尚未收到发票。</span><span class="sxs-lookup"><span data-stu-id="18113-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="18113-112">项目经理希望在收到发票前看到 1650 美元的应计项目成本。</span><span class="sxs-lookup"><span data-stu-id="18113-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="18113-113">应在公司的月底财务报表中体现此成本。</span><span class="sxs-lookup"><span data-stu-id="18113-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="18113-114">需要同时在财务级和项目级为申报目的记录这笔应计成本。</span><span class="sxs-lookup"><span data-stu-id="18113-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="18113-115">可以为物料和采购类别跟踪产品收据的财务更新。</span><span class="sxs-lookup"><span data-stu-id="18113-115">The financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="18113-116">对于物料，请在 **应付帐款参数** 页面中选择 **将产品收据过帐到分类帐** 选项。</span><span class="sxs-lookup"><span data-stu-id="18113-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="18113-117">[![应付帐款参数页面](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="18113-117">[![Accounts payable parameters page](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="18113-118">对于采购类别，请在 **目录策略规则** 页面中选择 **采购** 策略，然后为各采购类别选择 **接收后的应计采购支出**。</span><span class="sxs-lookup"><span data-stu-id="18113-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="18113-119">[![类别策略规则页面](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="18113-119">[![Category policy rule page](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="18113-120">过帐与产品收据有关的凭证时，将使用 **过帐设置** 中的 **采购支出，未开具发票** 和 **采购应计** 科目。</span><span class="sxs-lookup"><span data-stu-id="18113-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>

<span data-ttu-id="18113-121">我们同样使用这个方案查看过帐产品收据对总帐和项目信息有何影响。</span><span class="sxs-lookup"><span data-stu-id="18113-121">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="18113-122">**步骤 1：** 为项目创建一个新采购订单并确认，以便记录采购费用为 1500 美元，安装服务费为 150 美元的一台计算机的购买。</span><span class="sxs-lookup"><span data-stu-id="18113-122">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="18113-123">[![创建新采购订单](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="18113-123">[![Create new purchase order](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="18113-124">确认了采购订单之后，将为该项目创建承诺成本的交易记录。</span><span class="sxs-lookup"><span data-stu-id="18113-124">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="18113-125">[![创建的交易记录](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="18113-125">[![Transactions created](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="18113-126">承诺成本的交易记录的 **交易记录来源** 字段设置为 **采购订单**。</span><span class="sxs-lookup"><span data-stu-id="18113-126">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="18113-127">创建并确认采购订单不会为项目创建交易记录。</span><span class="sxs-lookup"><span data-stu-id="18113-127">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="18113-128">**步骤 2：** 交付货物和服务，并登记产品收据。</span><span class="sxs-lookup"><span data-stu-id="18113-128">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="18113-129">过帐产品收据将生成凭证并过帐到分类帐。</span><span class="sxs-lookup"><span data-stu-id="18113-129">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="18113-130">凭证将把采购支出、未开票的科目和应计科目记入借方。</span><span class="sxs-lookup"><span data-stu-id="18113-130">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="18113-131">[![凭证交易记录](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="18113-131">[![Voucher transactions](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="18113-132">过帐产品收据将使用采购类别和产品的过帐设置，而不是项目类别的过帐设置。</span><span class="sxs-lookup"><span data-stu-id="18113-132">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="18113-133">需要调整此设置，才能正确体现对采购应计的财务影响。</span><span class="sxs-lookup"><span data-stu-id="18113-133">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="18113-134">可以在 **采购类别** 页面中将采购类别映射到项目类别。</span><span class="sxs-lookup"><span data-stu-id="18113-134">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="18113-135">[![采购类别页面](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="18113-135">[![Procurement category page](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="18113-136">**步骤 3：** 创建供应商形式发票。</span><span class="sxs-lookup"><span data-stu-id="18113-136">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="18113-137">过帐产品收据不影响项目信息。</span><span class="sxs-lookup"><span data-stu-id="18113-137">Posting a product receipt does not impact project information.</span></span> <span data-ttu-id="18113-138">解决方案是，过帐采购收据后立即生成供应商形式发票。</span><span class="sxs-lookup"><span data-stu-id="18113-138">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="18113-139">转至 **采购订单** 页面 &gt; **发票** 选项卡 &gt; **生成** &gt; **发票**。</span><span class="sxs-lookup"><span data-stu-id="18113-139">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="18113-140">这将创建一张待定发票单据，用于更新项目信息。</span><span class="sxs-lookup"><span data-stu-id="18113-140">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="18113-141">创建供应商形式发票将生成挂起项目交易记录。</span><span class="sxs-lookup"><span data-stu-id="18113-141">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="18113-142">[![挂起项目交易记录](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="18113-142">[![Pending project transactions](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="18113-143">在 **承诺成本** 页面中，将关闭步骤 1 中创建的记录，并创建新记录以体现待定供应商发票产生的成本承诺。</span><span class="sxs-lookup"><span data-stu-id="18113-143">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="18113-144">承诺成本的 **交易记录来源** 字段将设置为 **供应商发票**。</span><span class="sxs-lookup"><span data-stu-id="18113-144">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="18113-145">[![承诺成本页面](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="18113-145">[![Commited costs page](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="18113-146">实际供应商发票到达前，此供应商发票将保持待定状态。</span><span class="sxs-lookup"><span data-stu-id="18113-146">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
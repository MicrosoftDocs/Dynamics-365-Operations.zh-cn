---
title: 设置并使用被付后支付的供应商付款
description: 本主题说明如何创建“即收即付”(PWP) 条款，以便您可以基于客户付款来释放部分供应商付款。
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 390cec62d2790ed10892669e283f2283c6b8e686
ms.sourcegitcommit: 399f128d90b71bd836a1c8c0c8c257b7f9eeb39a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284105"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a><span data-ttu-id="5b7ac-103">设置并使用被付后支付的供应商付款</span><span class="sxs-lookup"><span data-stu-id="5b7ac-103">Set up and use pay-when-paid vendor payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b7ac-104">当您批准供应商作为转包商工作时，可能想要预扣给供应商的付款，直到客户向您支付项目的付款。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-104">When you approve a vendor to work as a subcontractor, you might want to withhold payment to the vendor until your customer pays you for the project.</span></span> <span data-ttu-id="5b7ac-105">要支持此场景，您可以设置供应商的采购订单 (PO) 时，请设置即收即付 (PWP) 条款。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-105">To support this scenario, you can set up pay-when-paid (PWP) terms when you set up the purchase order (PO) with the vendor.</span></span>

<span data-ttu-id="5b7ac-106">例如，客户支付项目发票上的金额时，您可以释放部分或全部供应商发票金额。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-106">For example, when a customer pays an amount on a project invoice, you can release some or all of the vendor invoice amount.</span></span> <span data-ttu-id="5b7ac-107">从客户收到特定百分比的相关付款后，只需设置指定将对供应商付款的 PWP 条款。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-107">Just set up PWP terms that specify that the vendor will be paid after you receive a percentage of the related payment from the customer.</span></span> <span data-ttu-id="5b7ac-108">如果从客户收到部分付款，您可以手动释放部分相关供应商发票的付款。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-108">If you receive partial payment from a customer, you can manually release some of the related vendor invoices for payment.</span></span>

<span data-ttu-id="5b7ac-109">以下示例概括介绍了使用 PWP 条款的流程。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-109">The following example outlines the process when PWP terms are used.</span></span>

## <a name="example"></a><span data-ttu-id="5b7ac-110">示例</span><span class="sxs-lookup"><span data-stu-id="5b7ac-110">Example</span></span>

<span data-ttu-id="5b7ac-111">您的组织同意向客户提供 100 台装有软件的计算机，每台计算机的价格为 150.00 美元 (USD)。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-111">Your organization agrees to provide a customer with 100 computers that have software installed, for a price of 150.00 US dollars (USD) per computer.</span></span> <span data-ttu-id="5b7ac-112">然后，您雇用供应商为您提供安装了软件的计算机。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-112">You then hire a vendor to provide you with the computers that have software installed.</span></span> <span data-ttu-id="5b7ac-113">根据协议，客户必须在支付您的组织之前审核计算机的质量。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-113">According to the agreement, the customer must approve the quality of the computers before it pays your organization.</span></span> <span data-ttu-id="5b7ac-114">您的组织的政策是在客户付款给您之前，不向供应商付款。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-114">Your organization's policy is to withhold payment to vendors until the customer has paid you.</span></span> <span data-ttu-id="5b7ac-115">因此，您设置项目，使其 PWP 百分比为 100%。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-115">Therefore, you set up the project so that it has a PWP percentage of 100 percent.</span></span>

<span data-ttu-id="5b7ac-116">供应商向您发送 100 台安装了软件的计算机以及 10,000.00 美元的发票。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-116">The vendor sends you the 100 computers that have software installed, together with an invoice for 10,000.00 USD.</span></span> <span data-ttu-id="5b7ac-117">由于 PWP 条款是为您的项目设置的，因此您不会在收到计算机后向供应商付款。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-117">Because PWP terms are set up for your project, you don't pay the vendor upon receipt of the computers.</span></span> <span data-ttu-id="5b7ac-118">而是将计算机以及 15,000.00 的发票发送给客户。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-118">Instead, you send the computers to the customer, together with an invoice for 15,000.00.</span></span> <span data-ttu-id="5b7ac-119">客户检查计算机并审核全额项目发票。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-119">The customer inspects the computers and approves the full amount of the project invoice.</span></span>

<span data-ttu-id="5b7ac-120">从客户处收到完全付款后，您向供应商支付供应商发票的全部金额 10,000.00。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-120">After you receive the full payment from the customer, you pay the vendor 10,000.00, the full amount of the vendor invoice.</span></span>

## <a name="set-up-pwp-terms-for-a-project"></a><span data-ttu-id="5b7ac-121">设置项目的 PWP 条款</span><span class="sxs-lookup"><span data-stu-id="5b7ac-121">Set up PWP terms for a project</span></span>

<span data-ttu-id="5b7ac-122">在为项目设置 PWP 条款时，必须以百分比形式指定在您向供应商付款之前客户必须向您支付的最低金额。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-122">When you set up PWP terms for a project, you must specify, as a percentage, the minimum amount that a customer must pay you for the project before you will pay the vendor.</span></span> <span data-ttu-id="5b7ac-123">阈值金额在项目的客户发票上自动计算。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-123">The threshold amount is automatically calculated on the customer invoices for the project.</span></span> <span data-ttu-id="5b7ac-124">请按照以下步骤为 PWP 条款设置阈值百分比。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-124">Follow these steps to set up the threshold percentage for PWP terms.</span></span>

1. <span data-ttu-id="5b7ac-125">转到**项目管理与核算** \> **项目** \> **全部项目**。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-125">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="5b7ac-126">查找并打开您要为其设置 PWP 条款的项目。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-126">Find and open the project that you want to set up PWP terms for.</span></span>
3. <span data-ttu-id="5b7ac-127">在**供应商协议**快速选项卡上，请选择**添加行**。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="5b7ac-128">在**帐户编码**字段中，选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="5b7ac-128">In the **Account code** field, select one of the following options:</span></span>

    - <span data-ttu-id="5b7ac-129">**表** – PWP条款适用于单个供应商。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-129">**Table** – The PWP terms apply to a single vendor.</span></span>
    - <span data-ttu-id="5b7ac-130">**组** – PWP条款在供应商组中适用于所有供应商。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-130">**Group** – The PWP terms apply to all vendors in a vendor group.</span></span>
    - <span data-ttu-id="5b7ac-131">**所有** – PWP 条款适用于所有供应商。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-131">**All** – The PWP terms apply to all vendors.</span></span>

4. <span data-ttu-id="5b7ac-132">如果您在上一步中选择了**表**或**组**，请在**供应商/供应商组**字段中，选择 PWP 条款适用的供应商或供应商组。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-132">If you selected **Table** or **Group** in the previous step, in the **Vendor/Vendor group** field, select the vendor or vendor group that the PWP terms apply to.</span></span> <span data-ttu-id="5b7ac-133">如果您在上一步中选择了**所有**，则无法编辑**供应商/供应商组**字段。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-133">If you selected **All** in the previous step, the **Vendor/Vendor group** field can't be edited.</span></span>
5. <span data-ttu-id="5b7ac-134">如果项目中为供应商设置了供应商保留期限，则在**供应商保留期限**字段中选择保留期限的规则 ID。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-134">If vendor retention terms are set up for the vendor in the project, in the **Vendor retention terms** field, select the rule ID for the retention terms.</span></span>
6. <span data-ttu-id="5b7ac-135">在**PWP 阈值百分比**字段中，输入项目的阈值百分比。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-135">In the **PWP threshold percentage** field, enter the threshold percentage for the project.</span></span> <span data-ttu-id="5b7ac-136">您输入项目的百分比定义在您向供应商付款之前客户必须支付您的最小金额。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-136">The percentage that you enter for the project defines the minimum amount that the customer must pay you before you will pay the vendor.</span></span>

## <a name="create-a-po-that-has-pwp-terms"></a><span data-ttu-id="5b7ac-137">创建具有 PWP 条款的采购订单</span><span class="sxs-lookup"><span data-stu-id="5b7ac-137">Create a PO that has PWP terms</span></span>

<span data-ttu-id="5b7ac-138">在您过帐来自供应商的发票时，如果供应商须遵守 PWP 条款，这些条款将在采购订单行中显示。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-138">When you post an invoice from a vendor, if the vendor is subject to PWP terms, those terms are shown on the PO lines.</span></span> <span data-ttu-id="5b7ac-139">要创建具有 PWP 条款的采购订单，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-139">To create a PO that has PWP terms, follow these steps.</span></span>

1. <span data-ttu-id="5b7ac-140">转到**采购** \> **采购订单** \> **所有采购订单**。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-140">Go to **Procurement and sourcing** \> **Purchase orders** \> **All purchase orders**.</span></span>
2. <span data-ttu-id="5b7ac-141">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-141">On the Action Pane, select **New**.</span></span> <span data-ttu-id="5b7ac-142">然后，在**创建采购订单**对话框中，输入所需信息，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-142">Then, in the **Create purchase order** dialog box, enter the required information, and select **OK**.</span></span>

    <span data-ttu-id="5b7ac-143">或者，在**所有采购订单**列表页打开现有采购订单。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-143">Alternatively, open an existing PO on the **All purchase orders** list page.</span></span>

4. <span data-ttu-id="5b7ac-144">在**采购订单**页面，在**采购订单行**快速选项卡上，请检查供应商的采购订单行的详细信息。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-144">On the **Purchase order** page, on the **Purchase order lines** FastTab, review the details of the PO line for the vendor.</span></span> <span data-ttu-id="5b7ac-145">**即收即付**选项将自动选择，**PWP 阈值百分比**字段中的值将自动从**项目**页面的 **PWP 阈值百分比**字段复制。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-145">The **Pay when paid** option is automatically selected, and the value in the **PWP threshold percentage** field is automatically copied from the **PWP threshold percentage** field on the **Projects** page.</span></span>
6. <span data-ttu-id="5b7ac-146">如果您不希望将 PWP 条款应用于供应商的采购订单行，请清除**即收即付**选项。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-146">If you don't want to apply PWP terms to the vendor for a PO line, clear the **Pay when paid** option.</span></span> <span data-ttu-id="5b7ac-147">在这种情况下，采购订单行的 **PWP 阈值百分比**字段将重置为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-147">In this case, the **PWP threshold percentage** field for the PO line will be reset to 0 (zero).</span></span>

## <a name="update-a-customer-payment-and-pay-the-vendor"></a><span data-ttu-id="5b7ac-148">更新客户付款并支付供应商</span><span class="sxs-lookup"><span data-stu-id="5b7ac-148">Update a customer payment and pay the vendor</span></span>

<span data-ttu-id="5b7ac-149">在供应商完成项目的工作并且向您发送发票时，您必须审核项目状态和客户发票以确定是否满足项目的 PWP 条款要求。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-149">When a vendor completes its work on a project and sends you an invoice, you must review the project status and customer invoices to determine whether the PWP terms have been met for the project.</span></span> <span data-ttu-id="5b7ac-150">如果满足供应商的 PWP 条款，基于项目的客户付款，您可以决定支付供应商发票的哪些行。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-150">If the PWP terms for the vendor were met, you can determine which lines on the vendor invoice to pay, based on the customer payments for the project.</span></span> <span data-ttu-id="5b7ac-151">如果您决定向供应商付款，即使 PWP 条款未满足，您也可以覆盖**即收即付供应商发票**页面的 PWP 条款。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-151">If you decide to pay the vendor even though the PWP terms weren't met, you can override the PWP terms on the **Vendor invoice with pay when paid** page.</span></span>

1. <span data-ttu-id="5b7ac-152">转到**项目管理与核算** \> **查询和报表** \> **保留查询** \> **即收即付供应商发票**。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-152">Go to **Project management and accounting** \> **Inquiries and reports** \> **Retention inquiries** \> **Vendor invoice with pay when paid**.</span></span>
2. <span data-ttu-id="5b7ac-153">在**即收即付供应商发票**页面，在搜索字段中，输入值查找您要查看的供应商发票，然后选择**搜索**。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-153">On the **Vendor invoices with pay when paid** page, in the search field, enter values to find the vendor invoice that you want to review, and then select **Search**.</span></span>
3. <span data-ttu-id="5b7ac-154">在**供应商发票行**快速选项卡上，选择您要更改的行。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-154">On the **Vendor invoice lines** FastTab, select the lines that you want to change.</span></span>
4. <span data-ttu-id="5b7ac-155">如果满足发票行的**即收即付**条件，选择**下达供应商付款**。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-155">If the **Pay when paid** conditions are met for the invoice line, select **Release vendor payment**.</span></span> <span data-ttu-id="5b7ac-156">**即收即付**选项将被清除，**准备好付款**字段的值将更改为**是**。</span><span class="sxs-lookup"><span data-stu-id="5b7ac-156">The **Pay when paid** option is cleared, and the value of the **Ready for payment** field is changed to **Yes**.</span></span>

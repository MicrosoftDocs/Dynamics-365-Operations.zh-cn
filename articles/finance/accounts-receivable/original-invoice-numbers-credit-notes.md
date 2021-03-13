---
title: 对贷方通知单中的原始账单的引用
description: 本主题说明如何在相关的贷方通知单中设置和打印原始发票编号。
author: ilkond
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 673288f04b33aa2a578f9e2e7913dbe7ac309644
ms.sourcegitcommit: 7cdec5469ff0da145ac4e01caf3287d0627ae2dc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2021
ms.locfileid: "5099994"
---
# <a name="references-to-original-invoices-in-credit-notes"></a><span data-ttu-id="59d21-103">对贷方通知单中的原始账单的引用</span><span class="sxs-lookup"><span data-stu-id="59d21-103">References to original invoices in credit notes</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="59d21-104">在某些国家和地区，法律要求打印的贷方通知单必须包含对原始发票的引用。</span><span class="sxs-lookup"><span data-stu-id="59d21-104">In some countries and regions, there is a legal requirement that printed credit notes include references to the original invoices.</span></span> <span data-ttu-id="59d21-105">本主题说明如何在相关的贷方通知单中设置和打印原始发票编号。</span><span class="sxs-lookup"><span data-stu-id="59d21-105">This topic explains how to set up and print the original invoice numbers in related credit notes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="59d21-106">先决条件</span><span class="sxs-lookup"><span data-stu-id="59d21-106">Prerequisites</span></span>

- <span data-ttu-id="59d21-107">在 **功能管理** 工作区，打开 **销售和项目发票报表的贷记开票版式** 功能。</span><span class="sxs-lookup"><span data-stu-id="59d21-107">In the **Feature management** workspace, turn on the **Credit invoicing layout for sales and project invoice reports** feature.</span></span> <span data-ttu-id="59d21-108">有关更多信息，请参见[功能管理概述](../../fin-and-ops/get-started/feature-management/feature-management-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="59d21-108">For more information, see [Feature management overview](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="59d21-109">必须在“打印管理”中配置所需文档的可打印格式。</span><span class="sxs-lookup"><span data-stu-id="59d21-109">The printable formats of the required documents must be configured in Print management.</span></span>

<span data-ttu-id="59d21-110">本主题中所述的功能适用于以下文档：</span><span class="sxs-lookup"><span data-stu-id="59d21-110">The functionality that is described in this topic applies to the following documents:</span></span>

<span data-ttu-id="59d21-111">**应收账款**</span><span class="sxs-lookup"><span data-stu-id="59d21-111">**Accounts receivable**</span></span>

- <span data-ttu-id="59d21-112">普通贷方通知单</span><span class="sxs-lookup"><span data-stu-id="59d21-112">Free text credit note</span></span>
- <span data-ttu-id="59d21-113">客户贷方通知单</span><span class="sxs-lookup"><span data-stu-id="59d21-113">Customer credit note</span></span>

<span data-ttu-id="59d21-114">**项目管理与核算**</span><span class="sxs-lookup"><span data-stu-id="59d21-114">**Project management and accounting**</span></span>

- <span data-ttu-id="59d21-115">项目贷方通知单</span><span class="sxs-lookup"><span data-stu-id="59d21-115">Project credit note</span></span>

## <a name="configure-accounts-receivable-parameters"></a><span data-ttu-id="59d21-116">配置应收帐款参数</span><span class="sxs-lookup"><span data-stu-id="59d21-116">Configure Accounts receivable parameters</span></span>

<span data-ttu-id="59d21-117">请执行以下步骤设置控制是否在相关的贷方通知单中打印对原始发票的引用的参数。</span><span class="sxs-lookup"><span data-stu-id="59d21-117">Follow these steps to set the parameter that controls whether references to the original invoices are printed in related credit notes.</span></span>

1. <span data-ttu-id="59d21-118">转到 **应收帐款** \> **设置** \> **应收帐款参数**。</span><span class="sxs-lookup"><span data-stu-id="59d21-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="59d21-119">在 **更新** 选项卡上，在 **发票** 快速选项卡上，将 **将贷记开票版式应用到销售和项目发票报表** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="59d21-119">On the **Updates** tab, on the **Invoice** FastTab, set the **Apply the credit invoicing layout into sales and project invoice reports** option to **Yes**.</span></span>

![配置应收帐款参数](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a><span data-ttu-id="59d21-121">定义对原始发票的引用</span><span class="sxs-lookup"><span data-stu-id="59d21-121">Define references to original invoices</span></span>

<span data-ttu-id="59d21-122">使用以下过程根据文档类型定义对原始发票的引用。</span><span class="sxs-lookup"><span data-stu-id="59d21-122">Use the following procedures to define references to original invoices, based on the document type.</span></span>

### <a name="free-text-credit-note"></a><span data-ttu-id="59d21-123">普通贷方通知单</span><span class="sxs-lookup"><span data-stu-id="59d21-123">Free text credit note</span></span>

1. <span data-ttu-id="59d21-124">转至 **应收帐款** \> **发票** \> **所有普通发票**。</span><span class="sxs-lookup"><span data-stu-id="59d21-124">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="59d21-125">创建新的贷方通知单，或选择现有的贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="59d21-125">Create a new credit note, or select an existing credit note.</span></span>
3. <span data-ttu-id="59d21-126">打开发票。</span><span class="sxs-lookup"><span data-stu-id="59d21-126">Open the invoice.</span></span>
4. <span data-ttu-id="59d21-127">在操作窗格上的 **发票** 选项卡上，在 **功能** 组中，选择 **贷记开票**。</span><span class="sxs-lookup"><span data-stu-id="59d21-127">On the Action Pane, on the **Invoice** tab, in the **Functions** group, select **Credit invoicing**.</span></span>
5. <span data-ttu-id="59d21-128">输入对原始发票的引用，然后选择更正原因。</span><span class="sxs-lookup"><span data-stu-id="59d21-128">Enter the reference to the original invoice, and select the reason for the correction.</span></span>

![定义普通发票的引用](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a><span data-ttu-id="59d21-130">客户贷方通知单</span><span class="sxs-lookup"><span data-stu-id="59d21-130">Customer credit note</span></span>

1. <span data-ttu-id="59d21-131">转到 **应收帐款** \> **订单** \> **所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="59d21-131">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="59d21-132">选择并打开必须更正的已开票的销售订单。</span><span class="sxs-lookup"><span data-stu-id="59d21-132">Select and open the invoiced sales order that must be corrected.</span></span>
3. <span data-ttu-id="59d21-133">在操作窗格上的 **销售** 选项卡上，在 **贷方通知单** 组中，选择 **贷方通知单**。</span><span class="sxs-lookup"><span data-stu-id="59d21-133">On the Action Pane, on the **Sell** tab, in the **Credit note** group, select **Credit note**.</span></span>
4. <span data-ttu-id="59d21-134">输入更正原因。</span><span class="sxs-lookup"><span data-stu-id="59d21-134">Enter the reason for the correction.</span></span> <span data-ttu-id="59d21-135">对原始发票的引用将自动建立。</span><span class="sxs-lookup"><span data-stu-id="59d21-135">The reference to the original invoice is automatically established.</span></span>

![定义销售订单的引用](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a><span data-ttu-id="59d21-137">项目贷方通知单</span><span class="sxs-lookup"><span data-stu-id="59d21-137">Project credit note</span></span>

1. <span data-ttu-id="59d21-138">转到 **项目管理和会计** \> **项目发票** \> **项目发票**。</span><span class="sxs-lookup"><span data-stu-id="59d21-138">Go to **Project management and accounting** \> **Project invoices** \> **Project invoices**.</span></span>
2. <span data-ttu-id="59d21-139">选择并打开必须更正的项目发票。</span><span class="sxs-lookup"><span data-stu-id="59d21-139">Select and open the project invoice that must be corrected.</span></span>
3. <span data-ttu-id="59d21-140">在操作窗格上的 **项目发票** 选项卡上，在 **功能** 组中，选择 **为贷方通知单选择**。</span><span class="sxs-lookup"><span data-stu-id="59d21-140">On the Action Pane, on the **Project invoice** tab, in the **Functions** group, select **Select for credit note**.</span></span>
4. <span data-ttu-id="59d21-141">选择 **贷记开票**。</span><span class="sxs-lookup"><span data-stu-id="59d21-141">Select **Credit invoicing**.</span></span>
5. <span data-ttu-id="59d21-142">输入更正原因。</span><span class="sxs-lookup"><span data-stu-id="59d21-142">Enter the reason for the correction.</span></span> <span data-ttu-id="59d21-143">对原始发票的引用将自动建立。</span><span class="sxs-lookup"><span data-stu-id="59d21-143">The reference to the original invoice is automatically established.</span></span>

![定义项目发票的引用](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a><span data-ttu-id="59d21-145">打印贷方通知单</span><span class="sxs-lookup"><span data-stu-id="59d21-145">Printing credit notes</span></span>

<span data-ttu-id="59d21-146">当您打印普通、客户和项目贷方通知单时，它们将包括对原始发票的引用和更正原因。</span><span class="sxs-lookup"><span data-stu-id="59d21-146">When you print free text, customer, and project credit notes, they will include the reference to the original invoice and the correction reason.</span></span>

![打印的贷方通知单](media/credit-note-FTI.jpg)

> [!NOTE]
> <span data-ttu-id="59d21-148">假设将打印对原始发票的引用，请确保正确配置文档的可打印格式。</span><span class="sxs-lookup"><span data-stu-id="59d21-148">Make sure that the printable formats of the documents are correctly configured, on the assumption that references to original invoices will be printed.</span></span>

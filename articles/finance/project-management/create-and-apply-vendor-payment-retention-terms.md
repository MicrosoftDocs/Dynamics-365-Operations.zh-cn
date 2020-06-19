---
title: 创建和应用供应商付款保留条款
description: 本主题提供有关如何设置和维护供应商付款保留条款的信息。
author: kfend
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410197"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="e9c6d-103">创建和应用供应商付款保留条款</span><span class="sxs-lookup"><span data-stu-id="e9c6d-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="e9c6d-104">当您的组织希望保留对供应商的部分付款时，为项目设置供应商付款保留条款非常有用。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="e9c6d-105">例如，当您希望将给供应商的付款保留到交付的产品符合您期望时。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="e9c6d-106">您可以在协商供应商合同时指定供应商付款保留条款。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="e9c6d-107">创建供应商付款保留条款</span><span class="sxs-lookup"><span data-stu-id="e9c6d-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="e9c6d-108">您可以输入要保留的供应商付款的百分比和发放以前保留的金额的百分比。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="e9c6d-109">金额将供应商发票自动保留，直到到达完成的合同中所指定的状态。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="e9c6d-110">在您设置保留条款后，您可以将其应用于该供应商的任何项目。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="e9c6d-111">使用以下步骤设置和维护供应商付款的保留条款。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="e9c6d-112">转到**项目管理与核算** > **保留** > **供应商付款保留条款**。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="e9c6d-113">选择**新**添加新的供应商保留条款。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="e9c6d-114">新条件的**规则 ID** 值自动输入。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="e9c6d-115">在**描述**字段中输入简短描述，然后在**条款**快速选项卡上，选择**添加行**为以下项输入条款值：</span><span class="sxs-lookup"><span data-stu-id="e9c6d-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="e9c6d-116">**已交货单位的百分比**：输入条款完成的百分比。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="e9c6d-117">金额将自动保留在供应商发票上，直到完成项目阶段与指定的百分比相等。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="e9c6d-118">例如，如果您输入 50.00，金额将保留，直到完成 50% 的项目。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="e9c6d-119">**要保留的百分比**：输入要保留的供应商发票金额的百分比。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="e9c6d-120">例如，如果您输入 10.00，那么供应商发票上的金额将保留 10%，直到项目达到您在**已交货单位的百分比**字段中设置的完成百分比。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="e9c6d-121">**要发放的百分比**：选择**添加行**以输入要为选定的项目完成级别发放的任何先前保留金额的百分比。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="e9c6d-122">如果您具有多个项目完成的不同级别里程碑，输入每个留成规则的单独的供应商留成条款行。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="e9c6d-123">每一行可以指定不同的保留百分比和项目完成的每个指定级别的不同发放百分比。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="e9c6d-124">为供应商创建供应商保留条款后，可以将其应用于项目。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="e9c6d-125">将供应商保留条款应用于项目</span><span class="sxs-lookup"><span data-stu-id="e9c6d-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="e9c6d-126">转到**项目管理与核算** > **项目** > **所有项目**，从项目列表页面打开一个项目。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="e9c6d-127">在**供应商协议**快速选项卡上，请选择**添加行**。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="e9c6d-128">在**帐户代码字段**中，选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="e9c6d-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="e9c6d-129">**表**：供应商保留条款应用于单个供应商。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="e9c6d-130">**组**：供应商留成条款在供应商组中应用于所有供应商。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="e9c6d-131">**所有**：供应商留成条款应用于所有供应商。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="e9c6d-132">在**供应商/供应商组字段**中，选择供应商保留条款应用的供应商或供应商组。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="e9c6d-133">如果您在上一步中已选择**所有**，则此字段不可用。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="e9c6d-134">在**供应商保留条款**字段中，选择在上一个过程中创建的供应商保留条款。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="e9c6d-135">如果项目还有为供应商设置的即收即付 (PWP) 条款，则在 **PWP 阈值百分比**字段中输入项目的阈值百分比。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="e9c6d-136">供应商留成条款也将在您为供应商创建的采购订单中显示。</span><span class="sxs-lookup"><span data-stu-id="e9c6d-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>

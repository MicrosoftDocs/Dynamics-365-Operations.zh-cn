---
title: 在会计年度末转移项目预算
description: 本文提供有关如何将剩余预算金额转移到未来年份以及创建预算登记详细信息的信息。
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
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
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172322"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="b65e8-103">在会计年度末转移项目预算</span><span class="sxs-lookup"><span data-stu-id="b65e8-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b65e8-104">在处理多年份项目时，您可能在会计年度末有剩余预算。</span><span class="sxs-lookup"><span data-stu-id="b65e8-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="b65e8-105">您可以将剩余预算金额转移到下一年份，并在关联的总帐科目中创建金额的预算登记详细信息。</span><span class="sxs-lookup"><span data-stu-id="b65e8-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="b65e8-106">在结转剩余金额之前，请查看并分析剩余预算金额。</span><span class="sxs-lookup"><span data-stu-id="b65e8-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="b65e8-107">查看并分析剩余预算金额</span><span class="sxs-lookup"><span data-stu-id="b65e8-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="b65e8-108">完成以下步骤来查看项目的年底预算金额，但不结转这些金额。</span><span class="sxs-lookup"><span data-stu-id="b65e8-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="b65e8-109">转到**项目管理与核算** > **定期** > **预算** > **结转预算**。</span><span class="sxs-lookup"><span data-stu-id="b65e8-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="b65e8-110">在**项目预算结转流程**页面上的**年末选项**选项卡，确认**结转剩余的项目预算金额**未启用。</span><span class="sxs-lookup"><span data-stu-id="b65e8-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="b65e8-111">在**参数**选项卡上的**项目预算年份**字段中，选择您想查看剩余预算金额的会计年度。</span><span class="sxs-lookup"><span data-stu-id="b65e8-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="b65e8-112">在**期初会计年度**字段中，选择您想查看剩余预算金额的会计年度。</span><span class="sxs-lookup"><span data-stu-id="b65e8-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="b65e8-113">在**从预测模型**字段中，选择**剩余预算**。</span><span class="sxs-lookup"><span data-stu-id="b65e8-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="b65e8-114">要包括符合您所选条件且没有剩余预算的项目，请选择**显示零剩余**。</span><span class="sxs-lookup"><span data-stu-id="b65e8-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="b65e8-115">在**选择预算**选项卡上，选择**检索所有预算**加载符合您所选条件的所有预算，然后选择**处理**。</span><span class="sxs-lookup"><span data-stu-id="b65e8-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="b65e8-116">要设计一个将预算的特定集加载到窗格中的数据库查询，请选择**检索选定预算**。</span><span class="sxs-lookup"><span data-stu-id="b65e8-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="b65e8-117">有关窗格中特定行的详细信息，请选择该行，然后选择**查看预算详细信息**或**查看科目**。</span><span class="sxs-lookup"><span data-stu-id="b65e8-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="b65e8-118">结转剩余预算金额</span><span class="sxs-lookup"><span data-stu-id="b65e8-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="b65e8-119">当您处理剩余预算金额时，您可以在总账中为您结转的金额创建交易记录。</span><span class="sxs-lookup"><span data-stu-id="b65e8-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="b65e8-120">要创建总账交易记录，请完成[结转预算金额并创建总账交易记录](#carry-forward)一节中的步骤。</span><span class="sxs-lookup"><span data-stu-id="b65e8-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="b65e8-121">结转的预算金额将转移到在**预测模型**页面中选择的作为结转预测模型的预测模型。</span><span class="sxs-lookup"><span data-stu-id="b65e8-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="b65e8-122">结转预算金额并创建总账交易记录</span><span class="sxs-lookup"><span data-stu-id="b65e8-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="b65e8-123">选择**项目管理与核算** > **定期** > **预算** > **结转预算**。</span><span class="sxs-lookup"><span data-stu-id="b65e8-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="b65e8-124">在**项目预算结转流程**页面，选择**年末**，然后启用**结转剩余项目预算金额**和**在总帐中创建预算登记分录**。</span><span class="sxs-lookup"><span data-stu-id="b65e8-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="b65e8-125">在**参量**选项卡上，在**项目参数**字段组中，选择以下各项：</span><span class="sxs-lookup"><span data-stu-id="b65e8-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="b65e8-126">**项目预算年份**：选择您想查看剩余预算金额的会计年度的开端。</span><span class="sxs-lookup"><span data-stu-id="b65e8-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="b65e8-127">**损益**：在总账中创建损益交易记录。</span><span class="sxs-lookup"><span data-stu-id="b65e8-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="b65e8-128">**WIP**：在总账中创建“进行中的工作 (WIP)”交易记录。</span><span class="sxs-lookup"><span data-stu-id="b65e8-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="b65e8-129">**工资**：在总账中创建工资分配交易记录。</span><span class="sxs-lookup"><span data-stu-id="b65e8-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="b65e8-130">在**总账**字段组中，提供以下信息：</span><span class="sxs-lookup"><span data-stu-id="b65e8-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="b65e8-131">在**期初会计年度**字段中，选择您想将项目的剩余预算金额转移到的会计年度。</span><span class="sxs-lookup"><span data-stu-id="b65e8-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="b65e8-132">默认值比**项目预算年份**字段中的值晚一年。</span><span class="sxs-lookup"><span data-stu-id="b65e8-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="b65e8-133">在**结转期间**字段中，选择您要在总账中创建预算登记详细信息的期间。</span><span class="sxs-lookup"><span data-stu-id="b65e8-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="b65e8-134">这是期初会计年度中典型的第一个期间。</span><span class="sxs-lookup"><span data-stu-id="b65e8-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="b65e8-135">在**复制位置/目标位置**字段组中，提供以下信息：</span><span class="sxs-lookup"><span data-stu-id="b65e8-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="b65e8-136">在**从预测模型**字段中，选择与您想针对这些项目转移的剩余预算金额相关联的项目预算预测模型。</span><span class="sxs-lookup"><span data-stu-id="b65e8-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="b65e8-137">在**到分类帐预算模型**字段中，选择与您想将其转移到总账的预算金额相关联的分类账预算模型。</span><span class="sxs-lookup"><span data-stu-id="b65e8-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="b65e8-138">选择**转移销售币种**使用在转移项目的预算金额时所创建的总账交易记录的项目销售币种。</span><span class="sxs-lookup"><span data-stu-id="b65e8-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="b65e8-139">如果未选择此选项，交易记录将使用记帐币种。</span><span class="sxs-lookup"><span data-stu-id="b65e8-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="b65e8-140">选择**显示零剩余**包括没有剩余预算额但满足您在底部窗格中显示的项目中选择的其他条件的项目。</span><span class="sxs-lookup"><span data-stu-id="b65e8-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="b65e8-141">在**选择预算**选项卡上，选择**检索所有预算**加载符合您所选条件的所有预算。</span><span class="sxs-lookup"><span data-stu-id="b65e8-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="b65e8-142">如果您想要设计一个将项目预算的特定集加载到窗格中的数据库查询，请选择**检索选定预算**。</span><span class="sxs-lookup"><span data-stu-id="b65e8-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="b65e8-143">对于每个您想处理的项目，选择该项目的行开头处的选项。</span><span class="sxs-lookup"><span data-stu-id="b65e8-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="b65e8-144">要选择全部或大部分项目，请选择左上角的复选标记。</span><span class="sxs-lookup"><span data-stu-id="b65e8-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="b65e8-145">要排除正在处理的项目，请清除该项目的复选标记。</span><span class="sxs-lookup"><span data-stu-id="b65e8-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="b65e8-146">要将所选项目的剩余预算金额转移到所选会计年度，并在总账中创建预算登记详细信息，请选择**处理**。</span><span class="sxs-lookup"><span data-stu-id="b65e8-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="b65e8-147">结转预算金额但不创建总账交易记录</span><span class="sxs-lookup"><span data-stu-id="b65e8-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="b65e8-148">转到**项目管理与核算** > **定期** > **预算** > **结转预算**。</span><span class="sxs-lookup"><span data-stu-id="b65e8-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="b65e8-149">在**项目预算结转流程**页面上的**年末选项**字段中，选择**结转剩余的项目预算金额**。</span><span class="sxs-lookup"><span data-stu-id="b65e8-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="b65e8-150">在**参数**组中的**项目预算年份**字段中，选择您想查看剩余预算金额的会计年度。</span><span class="sxs-lookup"><span data-stu-id="b65e8-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="b65e8-151">在**复制位置/目标位置**组中，提供以下信息：</span><span class="sxs-lookup"><span data-stu-id="b65e8-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="b65e8-152">在**从预测模型**字段中，选择与您想针对这些项目转移的剩余预算金额相关联的项目预算预测模型。</span><span class="sxs-lookup"><span data-stu-id="b65e8-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="b65e8-153">选择**显示零剩余**包括没有剩余预算金额但符合您所选的其他条件且的项目。</span><span class="sxs-lookup"><span data-stu-id="b65e8-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="b65e8-154">在**选择预算**组中，选择**检索所有预算**加载符合您所选条件的所有预算。</span><span class="sxs-lookup"><span data-stu-id="b65e8-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="b65e8-155">要设计一个将项目预算的特定集加载到窗格中的数据库查询，请选择**检索选定预算**。</span><span class="sxs-lookup"><span data-stu-id="b65e8-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="b65e8-156">对于每个您想处理的项目，选择该项目的行开头处的选项。</span><span class="sxs-lookup"><span data-stu-id="b65e8-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="b65e8-157">选择**处理**将所选项目的剩余预算金额转移到所选会计年度。</span><span class="sxs-lookup"><span data-stu-id="b65e8-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>


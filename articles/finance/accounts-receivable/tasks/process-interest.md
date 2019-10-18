---
title: 处理利息
description: 此过程将向您展示如何创建、打印和过帐利息单。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7170a7a14237058064ed3091e9437cae312e6bd5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188755"
---
# <a name="process-interest"></a><span data-ttu-id="f93ee-103">处理利息</span><span class="sxs-lookup"><span data-stu-id="f93ee-103">Process interest</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f93ee-104">此过程将向您展示如何创建、打印和过帐利息单。</span><span class="sxs-lookup"><span data-stu-id="f93ee-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="f93ee-105">此任务使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="f93ee-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="f93ee-106">在过帐模板设置利息。</span><span class="sxs-lookup"><span data-stu-id="f93ee-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="f93ee-107">在**导航窗格**中，转到**模块 > 信用和收款 > 设置 > 客户过帐模板**。</span><span class="sxs-lookup"><span data-stu-id="f93ee-107">In the **Navigation pane**, go to **Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="f93ee-108">单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="f93ee-108">Click **Edit**.</span></span>
3. <span data-ttu-id="f93ee-109">在**设置**快速选项卡的**利息代码**字段中，从下拉列表选择一个利息代码。</span><span class="sxs-lookup"><span data-stu-id="f93ee-109">In the **Setup fastTab**, in the **Interest code** field, select an interest code from the drop-down list.</span></span> <span data-ttu-id="f93ee-110">如果您不希望使用此过帐模板计算交易利息，则将此字段留空。</span><span class="sxs-lookup"><span data-stu-id="f93ee-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span> <span data-ttu-id="f93ee-111">**表单限制**快速选项卡可允许您更改处理利息的方法。</span><span class="sxs-lookup"><span data-stu-id="f93ee-111">The **Table restriction** fastTab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="f93ee-112">如果此字段设置为“是”，则根据此过帐模板计算利息。</span><span class="sxs-lookup"><span data-stu-id="f93ee-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="f93ee-113">计算利息</span><span class="sxs-lookup"><span data-stu-id="f93ee-113">Calculate interest</span></span>
1. <span data-ttu-id="f93ee-114">在**导航窗格**中，转到**模块 > 信用和收款 > 利息 > 创建利息单**。</span><span class="sxs-lookup"><span data-stu-id="f93ee-114">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Create interest notes**.</span></span>
2. <span data-ttu-id="f93ee-115">您必须为您将要计算的利息选择交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="f93ee-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="f93ee-116">此计算包含这些类型的所有开放交易。</span><span class="sxs-lookup"><span data-stu-id="f93ee-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="f93ee-117">如果将**利息**设置为“是”，您将在利息单中计算利息。</span><span class="sxs-lookup"><span data-stu-id="f93ee-117">If you set **Interest** to 'Yes', you will calculate interest on interest.</span></span> <span data-ttu-id="f93ee-118">您也许想要在包括这些交易之前，管理利息单中计算利息的法律。</span><span class="sxs-lookup"><span data-stu-id="f93ee-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
4. <span data-ttu-id="f93ee-119">在**开始日期**字段中，输入将计算的利息的开始日期。</span><span class="sxs-lookup"><span data-stu-id="f93ee-119">In the **From date** field, enter a date from which the interest will be calculated.</span></span> <span data-ttu-id="f93ee-120">如果您并未设定**开始日期**，则所有未过帐的利息单将会被取消，利息将从交易记录日期开始重新计算。</span><span class="sxs-lookup"><span data-stu-id="f93ee-120">If you do not specific a **From date**, then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>
5. <span data-ttu-id="f93ee-121">在**结束日期**字段中，输入将计算的利息的结束日期。</span><span class="sxs-lookup"><span data-stu-id="f93ee-121">In the **To date** field, enter a date to which the interest would be calculated.</span></span>
6. <span data-ttu-id="f93ee-122">在**使用的过帐模板来自**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="f93ee-122">In the **Use posting profile from** field, select an option.</span></span> <span data-ttu-id="f93ee-123">过帐模板选项有三个：</span><span class="sxs-lookup"><span data-stu-id="f93ee-123">There are three posting profile options:</span></span>
    - <span data-ttu-id="f93ee-124">帐户 – 使用分配给每个利息单的客户帐户的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="f93ee-124">Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span> 
    - <span data-ttu-id="f93ee-125">选择 – 使用在“过帐模板”字段中选择的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="f93ee-125">Select – Use the posting profile that you select in the Posting profile field.</span></span>
    - <span data-ttu-id="f93ee-126">交易记录 –使用来自为每张利息单计算出利息的交易记录的单独过帐模板。</span><span class="sxs-lookup"><span data-stu-id="f93ee-126">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="f93ee-127">未分配过帐模板的交易记录将使用“应收账款参数单”的“分类帐”和“销售税”所指定的过帐模板。</span><span class="sxs-lookup"><span data-stu-id="f93ee-127">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
7. <span data-ttu-id="f93ee-128">扩展**要包括的记录**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="f93ee-128">Expand the **Records to include** fastTab.</span></span>
8. <span data-ttu-id="f93ee-129">单击**筛选器**。</span><span class="sxs-lookup"><span data-stu-id="f93ee-129">Click **Filter**.</span></span>
9. <span data-ttu-id="f93ee-130">在**条件**字段中，输入“客户 ID”。</span><span class="sxs-lookup"><span data-stu-id="f93ee-130">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="f93ee-131">例如，输入 'US-001'。</span><span class="sxs-lookup"><span data-stu-id="f93ee-131">For example, enter 'US-001'.</span></span>
6. <span data-ttu-id="f93ee-132">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="f93ee-132">Click **OK**.</span></span>
7. <span data-ttu-id="f93ee-133">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="f93ee-133">Click **OK**.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="f93ee-134">打印利息单</span><span class="sxs-lookup"><span data-stu-id="f93ee-134">Print interest notes</span></span>
1. <span data-ttu-id="f93ee-135">在**导航窗格**中，转到**模块 > 信用和收款 > 利息 > 审核和处理利息单**。</span><span class="sxs-lookup"><span data-stu-id="f93ee-135">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Review and process interest notes**.</span></span>
2. <span data-ttu-id="f93ee-136">在**状态**字段中，选择“创建”。</span><span class="sxs-lookup"><span data-stu-id="f93ee-136">In the **Status** field, select 'Created'.</span></span>
3. <span data-ttu-id="f93ee-137">在**打印**字段中，选择“不打印”。</span><span class="sxs-lookup"><span data-stu-id="f93ee-137">In the **Printed** field, select 'Not printed'.</span></span>
4. <span data-ttu-id="f93ee-138">单击**打印**。</span><span class="sxs-lookup"><span data-stu-id="f93ee-138">Click **Print**.</span></span>
5. <span data-ttu-id="f93ee-139">扩展**要包括的记录**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="f93ee-139">Expand the **Records to include** fastTab.</span></span>
6. <span data-ttu-id="f93ee-140">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="f93ee-140">Click **OK**.</span></span>
7. <span data-ttu-id="f93ee-141">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f93ee-141">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="f93ee-142">过帐利息单</span><span class="sxs-lookup"><span data-stu-id="f93ee-142">Post the interest note</span></span>
1. <span data-ttu-id="f93ee-143">选择准备过帐的利息单（状态为“已创建”）。</span><span class="sxs-lookup"><span data-stu-id="f93ee-143">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="f93ee-144">单击**过帐**。</span><span class="sxs-lookup"><span data-stu-id="f93ee-144">Click **Post**.</span></span>
3. <span data-ttu-id="f93ee-145">输入利息单的过帐日期。</span><span class="sxs-lookup"><span data-stu-id="f93ee-145">Enter the posting date for the interest note.</span></span> <span data-ttu-id="f93ee-146">选择“是”可以为每张利息单创建一个总帐交易记录。</span><span class="sxs-lookup"><span data-stu-id="f93ee-146">Select Yes to create a general ledger transaction for each interest note.</span></span> <span data-ttu-id="f93ee-147">如果未选择“是”，应付给客户的所有利息单上的利息将累加起来，作为一笔交易记录过帐到总帐中。</span><span class="sxs-lookup"><span data-stu-id="f93ee-147">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="f93ee-148">扩展**要包括的记录**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="f93ee-148">Expand the **Records to include** fastTab.</span></span>
5. <span data-ttu-id="f93ee-149">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="f93ee-149">Click **OK**.</span></span>
6. <span data-ttu-id="f93ee-150">在**状态**字段中，选择“已过帐”。</span><span class="sxs-lookup"><span data-stu-id="f93ee-150">In the **Status** field, select 'Posted'.</span></span>


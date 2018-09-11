--- 
title: "创建内部公司计划"
description: "此过程显示如何创建内部公司计划。"
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 52042f345b901db8f4cd3afcec69607e11d8a1ce
ms.contentlocale: zh-cn
ms.lasthandoff: 09/11/2018

---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="79b90-103">创建内部公司计划</span><span class="sxs-lookup"><span data-stu-id="79b90-103">Create an intercompany plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79b90-104">此过程显示如何创建内部公司计划。</span><span class="sxs-lookup"><span data-stu-id="79b90-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="79b90-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="79b90-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="79b90-106">设置内部公司计划组</span><span class="sxs-lookup"><span data-stu-id="79b90-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="79b90-107">转到“内部公司计划组”。</span><span class="sxs-lookup"><span data-stu-id="79b90-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="79b90-108">“主计划”>“设置”>“内部公司计划组”</span><span class="sxs-lookup"><span data-stu-id="79b90-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="79b90-109">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="79b90-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="79b90-110">例如，使用值“10”在“名称”字段中进行筛选。</span><span class="sxs-lookup"><span data-stu-id="79b90-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="79b90-111">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="79b90-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="79b90-112">单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="79b90-112">Click Delete.</span></span>
    * <span data-ttu-id="79b90-113">必须执行此步骤，才能缩短运行的内部公司计划。</span><span class="sxs-lookup"><span data-stu-id="79b90-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="79b90-114">内部公司计划将从最低计划序列开始在运行计划组中的所有公司运行主计划。</span><span class="sxs-lookup"><span data-stu-id="79b90-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="79b90-115">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="79b90-115">Click Yes.</span></span>
6. <span data-ttu-id="79b90-116">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="79b90-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="79b90-117">创建内部公司计划</span><span class="sxs-lookup"><span data-stu-id="79b90-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="79b90-118">单击“内部公司主计划”。</span><span class="sxs-lookup"><span data-stu-id="79b90-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="79b90-119">这位于“主计划”工作区中。</span><span class="sxs-lookup"><span data-stu-id="79b90-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="79b90-120">在“内部公司计划组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="79b90-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="79b90-121">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="79b90-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="79b90-122">选择内部公司计划组 10。</span><span class="sxs-lookup"><span data-stu-id="79b90-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="79b90-123">在“内部公司计划迭代数”中，输入“2”。</span><span class="sxs-lookup"><span data-stu-id="79b90-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="79b90-124">内部公司计划组 10 有两个成员。</span><span class="sxs-lookup"><span data-stu-id="79b90-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="79b90-125">若要将延迟从源公司 (USMF) 传播到客户公司 (DEMF)，需要在两个公司内两次运行内部公司。</span><span class="sxs-lookup"><span data-stu-id="79b90-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="79b90-126">第一个迭代将传播需求，并在源公司 (USMF) 中识别延迟。</span><span class="sxs-lookup"><span data-stu-id="79b90-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="79b90-127">第二个迭代将把延迟从 USMF 传播到 DEMF。</span><span class="sxs-lookup"><span data-stu-id="79b90-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="79b90-128">在“第一个迭代”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="79b90-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="79b90-129">在“第一个迭代”字段中，选择“重新生成”。</span><span class="sxs-lookup"><span data-stu-id="79b90-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="79b90-130">在“后面的迭代”字段中，选择“重新生成”。</span><span class="sxs-lookup"><span data-stu-id="79b90-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="79b90-131">在“线程数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="79b90-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="79b90-132">这表示用于计划的并行线程数。</span><span class="sxs-lookup"><span data-stu-id="79b90-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="79b90-133">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="79b90-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="79b90-134">查看计划的结果</span><span class="sxs-lookup"><span data-stu-id="79b90-134">View the result of the plan</span></span>
1. <span data-ttu-id="79b90-135">在“计划”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="79b90-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="79b90-136">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="79b90-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="79b90-137">单击 StaticPlan 的链接。</span><span class="sxs-lookup"><span data-stu-id="79b90-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="79b90-138">您需要是 USMF 公司的。</span><span class="sxs-lookup"><span data-stu-id="79b90-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="79b90-139">单击“计划订单”。</span><span class="sxs-lookup"><span data-stu-id="79b90-139">Click Planned orders.</span></span>



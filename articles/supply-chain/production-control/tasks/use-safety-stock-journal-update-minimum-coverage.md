---
title: 使用安全存货日记帐更新最小覆盖范围
description: 此过程演示如何根据历史交易记录计算最低覆盖范围方案，然后使用这些方案更新物料覆盖范围。
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3b2916d6d2f24579fd9795c0e0bc548b6c2b747
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835763"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="140ba-103">使用安全存货日记帐更新最小覆盖范围</span><span class="sxs-lookup"><span data-stu-id="140ba-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="140ba-104">此过程演示如何根据历史交易记录计算最低覆盖范围方案，然后使用这些方案更新物料覆盖范围。</span><span class="sxs-lookup"><span data-stu-id="140ba-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="140ba-105">方法是使用安全存货日记帐。</span><span class="sxs-lookup"><span data-stu-id="140ba-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="140ba-106">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="140ba-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="140ba-107">这项任务供生产计划者用于帮助维护最低覆盖范围。</span><span class="sxs-lookup"><span data-stu-id="140ba-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="140ba-108">新建安全存货日记帐名称</span><span class="sxs-lookup"><span data-stu-id="140ba-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="140ba-109">转到“安全存货日记帐名称”。</span><span class="sxs-lookup"><span data-stu-id="140ba-109">Go to Safety stock journal names.</span></span>
2. <span data-ttu-id="140ba-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="140ba-110">Click New.</span></span>
3. <span data-ttu-id="140ba-111">在“名称”字段中，键入“材料”。</span><span class="sxs-lookup"><span data-stu-id="140ba-111">In the Name field, type 'Material'.</span></span>
4. <span data-ttu-id="140ba-112">在“描述”字段中，键入“材料”。</span><span class="sxs-lookup"><span data-stu-id="140ba-112">In the Description field, type 'Material'.</span></span>
5. <span data-ttu-id="140ba-113">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="140ba-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="140ba-114">创建安全库存日记帐</span><span class="sxs-lookup"><span data-stu-id="140ba-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="140ba-115">转到“安全存货计算”。</span><span class="sxs-lookup"><span data-stu-id="140ba-115">Go to Safety stock calculation.</span></span>
2. <span data-ttu-id="140ba-116">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="140ba-116">Click New.</span></span>
3. <span data-ttu-id="140ba-117">在“名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="140ba-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="140ba-118">选择您创建的安全存货日记帐名称，如“物料”。</span><span class="sxs-lookup"><span data-stu-id="140ba-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="140ba-119">单击“创建行”。</span><span class="sxs-lookup"><span data-stu-id="140ba-119">Click Create lines.</span></span>
5. <span data-ttu-id="140ba-120">在“开始日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="140ba-120">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="140ba-121">将日期设置为“2015-01-02”。</span><span class="sxs-lookup"><span data-stu-id="140ba-121">Set the date to '2015-01-02'.</span></span>  
6. <span data-ttu-id="140ba-122">在“结束日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="140ba-122">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="140ba-123">将日期设置为“2015-12-30”。</span><span class="sxs-lookup"><span data-stu-id="140ba-123">Set the date to '2015-12-30'.</span></span>  
7. <span data-ttu-id="140ba-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="140ba-124">Click OK.</span></span>
    * <span data-ttu-id="140ba-125">这将为包含库存交易记录的维度创建行。</span><span class="sxs-lookup"><span data-stu-id="140ba-125">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="140ba-126">计算方案</span><span class="sxs-lookup"><span data-stu-id="140ba-126">Calculate proposal</span></span>
1. <span data-ttu-id="140ba-127">单击“计算方案”。</span><span class="sxs-lookup"><span data-stu-id="140ba-127">Click Calculate proposal.</span></span>
2. <span data-ttu-id="140ba-128">选择“使用提前期的平均发货量”。</span><span class="sxs-lookup"><span data-stu-id="140ba-128">Select the Use average issue during lead time option.</span></span>
3. <span data-ttu-id="140ba-129">将“倍增系数”设置为“10”。</span><span class="sxs-lookup"><span data-stu-id="140ba-129">Set Multiplication factor to '10'.</span></span>
    * <span data-ttu-id="140ba-130">倍增系数用于调整此方案。</span><span class="sxs-lookup"><span data-stu-id="140ba-130">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="140ba-131">由于演示数据只有少量交易记录，所以您需要设置此系数才能生成切实可行的方案。</span><span class="sxs-lookup"><span data-stu-id="140ba-131">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="140ba-132">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="140ba-132">Click OK.</span></span>
    * <span data-ttu-id="140ba-133">向下滚动找到 M0002 和 M0003。</span><span class="sxs-lookup"><span data-stu-id="140ba-133">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="140ba-134">查看“计算所得的最低数量”列。</span><span class="sxs-lookup"><span data-stu-id="140ba-134">View the Calculated minimum quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="140ba-135">更新最小数量</span><span class="sxs-lookup"><span data-stu-id="140ba-135">Update minimum quantity</span></span>
1. <span data-ttu-id="140ba-136">在“新建最小数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="140ba-136">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="140ba-137">更新“新建最小数量”以匹配“计算所得的最低数量”中的值。</span><span class="sxs-lookup"><span data-stu-id="140ba-137">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="140ba-138">如果计算所得的最低数量为零，可以输入所需将来值。</span><span class="sxs-lookup"><span data-stu-id="140ba-138">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="140ba-139">例如，可以在此字段中输入拥有仓库 12 的 M0002 的计算所得最低数量。</span><span class="sxs-lookup"><span data-stu-id="140ba-139">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="140ba-140">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="140ba-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="140ba-141">例如，可以选择拥有仓库 12 的 M0002。</span><span class="sxs-lookup"><span data-stu-id="140ba-141">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="140ba-142">在“新建最小数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="140ba-142">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="140ba-143">更新“新建最小数量”以匹配“计算所得的最低数量”中的值。</span><span class="sxs-lookup"><span data-stu-id="140ba-143">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="140ba-144">如果计算所得的最低数量为零，可以输入所需将来值。</span><span class="sxs-lookup"><span data-stu-id="140ba-144">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="140ba-145">发布新的最小数量和验证结果</span><span class="sxs-lookup"><span data-stu-id="140ba-145">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="140ba-146">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="140ba-146">Click Post.</span></span>
2. <span data-ttu-id="140ba-147">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="140ba-147">Click OK.</span></span>
3. <span data-ttu-id="140ba-148">单击并打开“物料编号”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="140ba-148">Click to follow the link in the Item number field.</span></span>
4. <span data-ttu-id="140ba-149">单击并打开“物料编号”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="140ba-149">Click to follow the link in the Item number field.</span></span>
5. <span data-ttu-id="140ba-150">在操作窗格上，单击“计划”。</span><span class="sxs-lookup"><span data-stu-id="140ba-150">On the Action Pane, click Plan.</span></span>
6. <span data-ttu-id="140ba-151">单击“物料覆盖范围”。</span><span class="sxs-lookup"><span data-stu-id="140ba-151">Click Item coverage.</span></span>
    * <span data-ttu-id="140ba-152">请注意，已使用安全存货日记帐中的新最低数量更新了“最小数量”。</span><span class="sxs-lookup"><span data-stu-id="140ba-152">Notice that the Minimum quantity has been updated with the new minimum quantity from the safety stock journal.</span></span>  


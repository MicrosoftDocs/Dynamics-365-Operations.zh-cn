---
title: 使用安全存货日记帐更新最小覆盖范围
description: 此过程演示如何根据历史交易记录计算最低覆盖范围方案，然后使用这些方案更新物料覆盖范围。
author: ChristianRytt
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d69daf3d307ba72ff6017d91849e3d22bd0bd85
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210310"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="38287-103">使用安全存货日记帐更新最小覆盖范围</span><span class="sxs-lookup"><span data-stu-id="38287-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="38287-104">此过程演示如何根据历史交易记录计算最低覆盖范围方案，然后使用这些方案更新物料覆盖范围。</span><span class="sxs-lookup"><span data-stu-id="38287-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="38287-105">方法是使用安全存货日记帐。</span><span class="sxs-lookup"><span data-stu-id="38287-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="38287-106">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="38287-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="38287-107">这项任务供生产计划者用于帮助维护最低覆盖范围。</span><span class="sxs-lookup"><span data-stu-id="38287-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="38287-108">新建安全存货日记帐名称</span><span class="sxs-lookup"><span data-stu-id="38287-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="38287-109">在**导航窗格**中，转到**主计划 > 设置 > 安全存货日记帐名称**。</span><span class="sxs-lookup"><span data-stu-id="38287-109">In the **Navigation pane**, go to **Master planning > Setup > Safety stock journal names**.</span></span>
2. <span data-ttu-id="38287-110">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="38287-110">Click **New**.</span></span>
3. <span data-ttu-id="38287-111">在**名称**字段中，键入“材料”。</span><span class="sxs-lookup"><span data-stu-id="38287-111">In the **Name** field, type 'Material'.</span></span>
4. <span data-ttu-id="38287-112">在**描述**字段中，键入“材料”。</span><span class="sxs-lookup"><span data-stu-id="38287-112">In the **Description** field, type 'Material'.</span></span>
5. <span data-ttu-id="38287-113">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="38287-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="38287-114">创建安全库存日记帐</span><span class="sxs-lookup"><span data-stu-id="38287-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="38287-115">在**导航窗格**中，转到**主计划 > 主计划 > 运行 > 安全存货计算**。</span><span class="sxs-lookup"><span data-stu-id="38287-115">In the **Navigation pane**, go to **Master planning > Master planning > Run > Safety stock calculation**.</span></span>
2. <span data-ttu-id="38287-116">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="38287-116">Click **New**.</span></span>
3. <span data-ttu-id="38287-117">在**名称**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="38287-117">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="38287-118">选择您创建的安全存货日记帐名称，如“物料”。</span><span class="sxs-lookup"><span data-stu-id="38287-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="38287-119">单击**创建行**。</span><span class="sxs-lookup"><span data-stu-id="38287-119">Click **Create lines**.</span></span>
5. <span data-ttu-id="38287-120">在**开始日期**字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="38287-120">In the **From date** field, enter a date.</span></span>  
6. <span data-ttu-id="38287-121">在**结束日期**字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="38287-121">In the **To date** field, enter a date.</span></span>
7. <span data-ttu-id="38287-122">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="38287-122">Click **OK**.</span></span> <span data-ttu-id="38287-123">这将为包含库存交易记录的维度创建行。</span><span class="sxs-lookup"><span data-stu-id="38287-123">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="38287-124">计算方案</span><span class="sxs-lookup"><span data-stu-id="38287-124">Calculate proposal</span></span>
1. <span data-ttu-id="38287-125">单击**计算方案**。</span><span class="sxs-lookup"><span data-stu-id="38287-125">Click **Calculate proposal**.</span></span>
2. <span data-ttu-id="38287-126">选择**使用提前期的平均发货量**选项。</span><span class="sxs-lookup"><span data-stu-id="38287-126">Select the **Use average issue during lead time** option.</span></span>
3. <span data-ttu-id="38287-127">将**倍增系数**设置为“10”。</span><span class="sxs-lookup"><span data-stu-id="38287-127">Set **Multiplication factor** to '10'.</span></span> <span data-ttu-id="38287-128">倍增系数用于调整此方案。</span><span class="sxs-lookup"><span data-stu-id="38287-128">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="38287-129">由于演示数据只有少量交易记录，所以您需要设置此系数才能生成切实可行的方案。</span><span class="sxs-lookup"><span data-stu-id="38287-129">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="38287-130">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="38287-130">Click **OK**.</span></span> <span data-ttu-id="38287-131">向下滚动找到 M0002 和 M0003。</span><span class="sxs-lookup"><span data-stu-id="38287-131">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="38287-132">查看**计算所得的最低数量**列。</span><span class="sxs-lookup"><span data-stu-id="38287-132">View the **Calculated minimum** quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="38287-133">更新最小数量</span><span class="sxs-lookup"><span data-stu-id="38287-133">Update minimum quantity</span></span>
1. <span data-ttu-id="38287-134">在**新建最小数量**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="38287-134">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="38287-135">更新“新建最小数量”以匹配“计算所得的最低数量”中的值。</span><span class="sxs-lookup"><span data-stu-id="38287-135">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="38287-136">如果计算所得的最低数量为零，可以输入所需将来值。</span><span class="sxs-lookup"><span data-stu-id="38287-136">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="38287-137">例如，可以在此字段中输入拥有仓库 12 的 M0002 的计算所得最低数量。</span><span class="sxs-lookup"><span data-stu-id="38287-137">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="38287-138">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="38287-138">In the list, find and select the desired record.</span></span> <span data-ttu-id="38287-139">例如，可以选择拥有仓库 12 的 M0002。</span><span class="sxs-lookup"><span data-stu-id="38287-139">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="38287-140">在**新建最小数量**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="38287-140">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="38287-141">更新“新建最小数量”以匹配“计算所得的最低数量”中的值。</span><span class="sxs-lookup"><span data-stu-id="38287-141">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="38287-142">如果计算所得的最低数量为零，可以输入所需将来值。</span><span class="sxs-lookup"><span data-stu-id="38287-142">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="38287-143">发布新的最小数量和验证结果</span><span class="sxs-lookup"><span data-stu-id="38287-143">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="38287-144">单击**过帐**。</span><span class="sxs-lookup"><span data-stu-id="38287-144">Click **Post**.</span></span>
2. <span data-ttu-id="38287-145">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="38287-145">Click **OK**.</span></span>
3. <span data-ttu-id="38287-146">单击并打开**物料编号**字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="38287-146">Click to follow the link in the **Item number** field.</span></span>
4. <span data-ttu-id="38287-147">单击并打开**物料编号**字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="38287-147">Click to follow the link in the **Item number** field.</span></span>
5. <span data-ttu-id="38287-148">在**操作窗格**中，单击“计划”。</span><span class="sxs-lookup"><span data-stu-id="38287-148">On the **Action Pane**, click Plan.</span></span>
6. <span data-ttu-id="38287-149">单击**物料覆盖范围**。</span><span class="sxs-lookup"><span data-stu-id="38287-149">Click **Item coverage**.</span></span> <span data-ttu-id="38287-150">请注意，已使用安全存货日记帐中的新最低数量更新了**最小数量**。</span><span class="sxs-lookup"><span data-stu-id="38287-150">Notice that the **Minimum quantity** has been updated with the new minimum quantity from the safety stock journal.</span></span>  


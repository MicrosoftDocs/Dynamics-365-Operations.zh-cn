--- 
title: "设置自动装运对帐"
description: "此过程显示如何为自动货运对帐设置数据。"
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 97f0c4d8fe06ab2fc252b9543cb688306214c79f
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-automatic-freight-reconciliation"></a><span data-ttu-id="7d85d-103">设置自动装运对帐</span><span class="sxs-lookup"><span data-stu-id="7d85d-103">Set up automatic freight reconciliation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7d85d-104">此过程显示如何为自动货运对帐设置数据。</span><span class="sxs-lookup"><span data-stu-id="7d85d-104">This procedure shows how to set up data for automatic freight reconciliation.</span></span> <span data-ttu-id="7d85d-105">此操作通常由仓库经理完成。</span><span class="sxs-lookup"><span data-stu-id="7d85d-105">This is typically done by a warehouse manager.</span></span> <span data-ttu-id="7d85d-106">您可以在演示数据公司 USMF 中使用此过程。</span><span class="sxs-lookup"><span data-stu-id="7d85d-106">You can use this procedure in demo data company USMF.</span></span>


## <a name="set-up-the-freight-bill-type"></a><span data-ttu-id="7d85d-107">设置货运帐单类型</span><span class="sxs-lookup"><span data-stu-id="7d85d-107">Set up the freight bill type</span></span>
1. <span data-ttu-id="7d85d-108">转到“运输管理”>“设置”>“货运对帐”>“货运帐单类型”。</span><span class="sxs-lookup"><span data-stu-id="7d85d-108">Go to Transportation management > Setup > Freight reconciliation > Freight bill type.</span></span>
    * <span data-ttu-id="7d85d-109">货运帐单类型定义应如何匹配货运帐单和承运人发票。</span><span class="sxs-lookup"><span data-stu-id="7d85d-109">The freight bill type defines how freight bills and carrier invoices  should be matched.</span></span>  
2. <span data-ttu-id="7d85d-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7d85d-110">Click New.</span></span>
3. <span data-ttu-id="7d85d-111">在“货运帐单类型”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7d85d-111">In the Freight bill type field, type a value.</span></span>
4. <span data-ttu-id="7d85d-112">在“引擎程序集”字段中，键入“Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer”。</span><span class="sxs-lookup"><span data-stu-id="7d85d-112">In the Engine assembly field, type 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span></span>
    * <span data-ttu-id="7d85d-113">这是标准运输管理匹配引擎代码库。</span><span class="sxs-lookup"><span data-stu-id="7d85d-113">This is the standard Transportation management matching engine code library.</span></span>  
5. <span data-ttu-id="7d85d-114">在“引擎类”字段中，键入“Microsoft.Dynamics.Ax.Tms.dll”。</span><span class="sxs-lookup"><span data-stu-id="7d85d-114">In the Engine class field, type 'Microsoft.Dynamics.Ax.Tms.dll'.</span></span>
    * <span data-ttu-id="7d85d-115">这是标准运输管理匹配引擎类。</span><span class="sxs-lookup"><span data-stu-id="7d85d-115">This is the standard Transportation management matching engine class.</span></span>  
6. <span data-ttu-id="7d85d-116">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7d85d-116">Click New.</span></span>
7. <span data-ttu-id="7d85d-117">在"描述"字段中，选择在货运帐单和承运人发票上应匹配的值。</span><span class="sxs-lookup"><span data-stu-id="7d85d-117">In the Description field, choose the value that should match on the freight bill and the carrier invoice.</span></span>  
8. <span data-ttu-id="7d85d-118">在“需要匹配”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="7d85d-118">In the Match required field, select 'Yes'.</span></span>
    * <span data-ttu-id="7d85d-119">如果将此字段设置为“是”，则表示“描述”字段中选择的值在货运帐单和承运人发票上均匹配。</span><span class="sxs-lookup"><span data-stu-id="7d85d-119">If you set this field to Yes this means that the value selected in the Description field needs to match on both the freight bill and the carrier invoice.</span></span> <span data-ttu-id="7d85d-120">如果设置为“否”，此字段在其中一个上可以为空。</span><span class="sxs-lookup"><span data-stu-id="7d85d-120">If you set it to No, the field can be blank on one of these.</span></span>  
9. <span data-ttu-id="7d85d-121">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="7d85d-121">Click Save.</span></span>

## <a name="set-up-the-freight-bill-type-assignment"></a><span data-ttu-id="7d85d-122">设置货运帐单类型分配</span><span class="sxs-lookup"><span data-stu-id="7d85d-122">Set up the freight bill type assignment</span></span>
1. <span data-ttu-id="7d85d-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="7d85d-123">Close the page.</span></span>
2. <span data-ttu-id="7d85d-124">转到“运输管理”>“设置”>“货运对帐”>“货运帐单类型分配”。</span><span class="sxs-lookup"><span data-stu-id="7d85d-124">Go to Transportation management > Setup > Freight reconciliation > Freight bill type assignments.</span></span>
    * <span data-ttu-id="7d85d-125">运费帐单类型分配用于指定为特定承运人使用哪种货运帐单类型。</span><span class="sxs-lookup"><span data-stu-id="7d85d-125">The freight bill type assignment is used to specify which freight bill type is used for a particular carrier.</span></span>   
3. <span data-ttu-id="7d85d-126">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7d85d-126">Click New.</span></span>
4. <span data-ttu-id="7d85d-127">在“模式”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7d85d-127">In the Mode field, enter or select a value.</span></span>
5. <span data-ttu-id="7d85d-128">在“装运承运人”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7d85d-128">In the Shipping carrier field, enter or select a value.</span></span>
6. <span data-ttu-id="7d85d-129">在“货运帐单类型”字段中，选择您之前创建的货运帐单类型。</span><span class="sxs-lookup"><span data-stu-id="7d85d-129">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
7. <span data-ttu-id="7d85d-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="7d85d-130">Close the page.</span></span>

## <a name="set-up-the-audit-master"></a><span data-ttu-id="7d85d-131">设置审计主数据</span><span class="sxs-lookup"><span data-stu-id="7d85d-131">Set up the audit master</span></span>
1. <span data-ttu-id="7d85d-132">转到“运输管理”>“设置”>“货运对帐”>“审计主数据”。</span><span class="sxs-lookup"><span data-stu-id="7d85d-132">Go to Transportation management > Setup > Freight reconciliation > Audit master.</span></span>
    * <span data-ttu-id="7d85d-133">审计主数据定义自动货运对帐的容差限制。</span><span class="sxs-lookup"><span data-stu-id="7d85d-133">The audit master defines the tolerance limits for automatic freight reconciliation.</span></span> <span data-ttu-id="7d85d-134">它指定货运帐单和承运人发票上可以相差多少货币金额的情况下仍然允许对帐。</span><span class="sxs-lookup"><span data-stu-id="7d85d-134">It specifies by how much the monetary amounts on the freight bill and the carrier invoice can differ and still allow reconciliation to occur.</span></span> <span data-ttu-id="7d85d-135">还定义如何处理差异。</span><span class="sxs-lookup"><span data-stu-id="7d85d-135">It also defines how to handle discrepancies.</span></span>  
2. <span data-ttu-id="7d85d-136">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7d85d-136">Click New.</span></span>
3. <span data-ttu-id="7d85d-137">在“审计主数据 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7d85d-137">In the Audit master ID field, type a value.</span></span>
4. <span data-ttu-id="7d85d-138">在“装运承运人”字段中，选择您之前选择的同一位装运承运人。</span><span class="sxs-lookup"><span data-stu-id="7d85d-138">In the Shipping carrier  field, select the same shipping carrier as you did earlier.</span></span>
5. <span data-ttu-id="7d85d-139">在“货运帐单类型”字段中，选择您之前创建的货运帐单类型。</span><span class="sxs-lookup"><span data-stu-id="7d85d-139">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
6. <span data-ttu-id="7d85d-140">展开“容差”部分。</span><span class="sxs-lookup"><span data-stu-id="7d85d-140">Expand the Tolerance section.</span></span>
7. <span data-ttu-id="7d85d-141">在“最小容差级别”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="7d85d-141">In the Minimum tolerance level field, enter a number.</span></span>
8. <span data-ttu-id="7d85d-142">在“最大容差级别”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="7d85d-142">In the Maximum tolerance level field, enter a number.</span></span>
9. <span data-ttu-id="7d85d-143">展开“结果”部分。</span><span class="sxs-lookup"><span data-stu-id="7d85d-143">Expand the Result section.</span></span>
10. <span data-ttu-id="7d85d-144">在“超额支付原因代码”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7d85d-144">In the Overpayment reason code field, enter or select a value.</span></span>
    * <span data-ttu-id="7d85d-145">如果货运帐单和承运人发票上的货币金额不同，则只要差值在容差级别内，超额支付和未足额支付原因代码将指定应登记的差异金额。</span><span class="sxs-lookup"><span data-stu-id="7d85d-145">If the monetary amounts differ on the freight bill and the carrier invoice, the overpayment and underpayment reason codes specify the accounts that the difference should be registered on, as long as the difference is within the tolerance levels.</span></span>  
11. <span data-ttu-id="7d85d-146">在“未足额支付原因代码”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7d85d-146">In the Underpayment reason code field, enter or select a value.</span></span>
12. <span data-ttu-id="7d85d-147">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="7d85d-147">Close the page.</span></span>



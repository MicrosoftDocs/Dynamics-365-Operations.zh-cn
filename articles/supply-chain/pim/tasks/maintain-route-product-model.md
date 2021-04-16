---
title: 维护产品模型路线
description: 该过程的运行要求有现有的产品配置模型。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 022db87d0a26efa948a618344ed392ab638b8790
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817981"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="7c681-103">维护产品模型路线</span><span class="sxs-lookup"><span data-stu-id="7c681-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7c681-104">该过程的运行要求有现有的产品配置模型。</span><span class="sxs-lookup"><span data-stu-id="7c681-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="7c681-105">该过程使用演示公司 USMF 的高端扬声器模型向您介绍流程步骤。</span><span class="sxs-lookup"><span data-stu-id="7c681-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="7c681-106">添加一个路线运营</span><span class="sxs-lookup"><span data-stu-id="7c681-106">Add a route operation</span></span>
1. <span data-ttu-id="7c681-107">单击“产品变型模型定义”。</span><span class="sxs-lookup"><span data-stu-id="7c681-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="7c681-108">单击“产品配置模型”。</span><span class="sxs-lookup"><span data-stu-id="7c681-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="7c681-109">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="7c681-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7c681-110">为此次练习选择“高端扬声器模型”。</span><span class="sxs-lookup"><span data-stu-id="7c681-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="7c681-111">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7c681-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="7c681-112">展开“路线运营”部分。</span><span class="sxs-lookup"><span data-stu-id="7c681-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="7c681-113">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="7c681-113">Click Add.</span></span>
7. <span data-ttu-id="7c681-114">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7c681-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="7c681-115">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7c681-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="7c681-116">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="7c681-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="7c681-117">输入路线运营详细信息</span><span class="sxs-lookup"><span data-stu-id="7c681-117">Enter route operation details</span></span>
1. <span data-ttu-id="7c681-118">单击“路线运营详细信息”。</span><span class="sxs-lookup"><span data-stu-id="7c681-118">Click Route operation details.</span></span>
2. <span data-ttu-id="7c681-119">在“运营”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7c681-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="7c681-120">在“工序</span><span class="sxs-lookup"><span data-stu-id="7c681-120">In the Oper.</span></span> <span data-ttu-id="7c681-121">编号</span><span class="sxs-lookup"><span data-stu-id="7c681-121">No.</span></span> <span data-ttu-id="7c681-122">字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="7c681-122">field, enter a number.</span></span>
    * <span data-ttu-id="7c681-123">工序编号确定工艺路线序列。</span><span class="sxs-lookup"><span data-stu-id="7c681-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="7c681-124">工艺路线工序的每个属性可获得静态值或映射到一个属性。</span><span class="sxs-lookup"><span data-stu-id="7c681-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="7c681-125">映射到属性会导致值设为配置的一部分。</span><span class="sxs-lookup"><span data-stu-id="7c681-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="7c681-126">在“路线组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7c681-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="7c681-127">工艺路线组确定成本、消耗量和设置的重要行为。</span><span class="sxs-lookup"><span data-stu-id="7c681-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="7c681-128">单击“设置”选项卡。</span><span class="sxs-lookup"><span data-stu-id="7c681-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="7c681-129">单击“时间”选项卡。</span><span class="sxs-lookup"><span data-stu-id="7c681-129">Click the Times tab.</span></span>
7. <span data-ttu-id="7c681-130">在“进程数量“ 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="7c681-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="7c681-131">确定一次操作中将处理的量。</span><span class="sxs-lookup"><span data-stu-id="7c681-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="7c681-132">在“小时/时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="7c681-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="7c681-133">输入时间比。</span><span class="sxs-lookup"><span data-stu-id="7c681-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="7c681-134">选择“设置”复选框。</span><span class="sxs-lookup"><span data-stu-id="7c681-134">Select the Set check box.</span></span>
10. <span data-ttu-id="7c681-135">在“运行时间”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="7c681-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="7c681-136">确定您指定的数量的处理时间。</span><span class="sxs-lookup"><span data-stu-id="7c681-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="7c681-137">单击“资源要求”选项卡。</span><span class="sxs-lookup"><span data-stu-id="7c681-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="7c681-138">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="7c681-138">Click Add.</span></span>
13. <span data-ttu-id="7c681-139">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="7c681-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="7c681-140">在“要求类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="7c681-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="7c681-141">确定是否要指定必须拥有的特定资源或功能。</span><span class="sxs-lookup"><span data-stu-id="7c681-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="7c681-142">在“要求”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7c681-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="7c681-143">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="7c681-143">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
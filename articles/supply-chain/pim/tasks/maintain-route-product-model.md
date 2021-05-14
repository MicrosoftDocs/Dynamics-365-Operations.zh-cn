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
ms.openlocfilehash: 45c6b1e6e75645bb17ce4defa0bca0e6d2131b6e
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921257"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="ab8e6-103">维护产品模型路线</span><span class="sxs-lookup"><span data-stu-id="ab8e6-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ab8e6-104">该过程的运行要求有现有的产品配置模型。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="ab8e6-105">该过程使用演示公司 USMF 的高端扬声器模型向您介绍流程步骤。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>

## <a name="add-a-route-operation"></a><span data-ttu-id="ab8e6-106">添加一个路线运营</span><span class="sxs-lookup"><span data-stu-id="ab8e6-106">Add a route operation</span></span>

1. <span data-ttu-id="ab8e6-107">转到 **产品信息管理 \> 产品 \> 产品配置模型**。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="ab8e6-108">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ab8e6-109">为此次练习选择“高端扬声器模型”。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-109">Select the High end speaker model for this exercise.</span></span>  
1. <span data-ttu-id="ab8e6-110">在列表中，选择所选择行中的链接。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="ab8e6-111">展开 **工艺路线工序** 部分。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-111">Expand the **Route operations** section.</span></span>
1. <span data-ttu-id="ab8e6-112">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-112">Select **Add**.</span></span>
1. <span data-ttu-id="ab8e6-113">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="ab8e6-114">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="ab8e6-115">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-115">Select **Save**.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="ab8e6-116">输入路线运营详细信息</span><span class="sxs-lookup"><span data-stu-id="ab8e6-116">Enter route operation details</span></span>

1. <span data-ttu-id="ab8e6-117">选择 **工艺路线工序详细信息**。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-117">Select **Route operation details**.</span></span>
1. <span data-ttu-id="ab8e6-118">在 **工序** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-118">In the **Operation** field, enter or select a value.</span></span>
1. <span data-ttu-id="ab8e6-119">在 **工序编号**</span><span class="sxs-lookup"><span data-stu-id="ab8e6-119">In the **Oper. No.**</span></span> <span data-ttu-id="ab8e6-120">字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-120">field, enter a number.</span></span>
    * <span data-ttu-id="ab8e6-121">工序编号确定工艺路线序列。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-121">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="ab8e6-122">工艺路线工序的每个属性可获得静态值或映射到一个属性。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-122">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="ab8e6-123">映射到属性会导致值设为配置的一部分。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-123">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
1. <span data-ttu-id="ab8e6-124">在 **工艺路线组** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-124">In the **Route group** field, enter or select a value.</span></span>
    * <span data-ttu-id="ab8e6-125">工艺路线组确定成本、消耗量和设置的重要行为。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-125">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
1. <span data-ttu-id="ab8e6-126">选择 **设置** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-126">Select the **Setup** tab.</span></span>
1. <span data-ttu-id="ab8e6-127">选择 **时间** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-127">Select the **Times** tab.</span></span>
1. <span data-ttu-id="ab8e6-128">在 **处理数量** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-128">In the **Process qty.** field, enter a number.</span></span>
    * <span data-ttu-id="ab8e6-129">确定一次操作中将处理的量。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-129">Determine how many will be processed during one operation.</span></span>  
1. <span data-ttu-id="ab8e6-130">在 **小时/时间** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-130">In the **Hours/time** field, enter a number.</span></span>
    * <span data-ttu-id="ab8e6-131">输入时间比。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-131">Enter the time ratio.</span></span>  
1. <span data-ttu-id="ab8e6-132">选择 **设置** 复选框。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-132">Select the **Set** check box.</span></span>
1. <span data-ttu-id="ab8e6-133">在 **运行时间** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-133">In the **Run time** field, enter a number.</span></span>
    * <span data-ttu-id="ab8e6-134">确定您指定的数量的处理时间。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-134">Determine the processing time for the quantity that you have specified.</span></span>  
1. <span data-ttu-id="ab8e6-135">选择 **资源要求** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-135">Select the **Resource requirements** tab.</span></span>
1. <span data-ttu-id="ab8e6-136">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-136">Select **Add**.</span></span>
1. <span data-ttu-id="ab8e6-137">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-137">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ab8e6-138">在 **要求类型** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-138">In the **Requirement type** field, select an option.</span></span>
    * <span data-ttu-id="ab8e6-139">确定是否要指定必须拥有的特定资源或功能。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-139">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
1. <span data-ttu-id="ab8e6-140">在 **要求** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-140">In the **Requirement** field, enter or select a value.</span></span>
1. <span data-ttu-id="ab8e6-141">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="ab8e6-141">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: 创建基于维度的基础产品的物料清单
description: 对于此过程，您应该已经以八个记录的这个顺序完成之前的 4 个指南。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13053dd87242963586678b46c64493feb3383c4c
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920697"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="1b8f6-103">创建基于维度的基础产品的物料清单</span><span class="sxs-lookup"><span data-stu-id="1b8f6-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1b8f6-104">对于此过程，您应该已经以八个记录的这个顺序完成之前的 4 个指南。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="1b8f6-105">前 4 个记录设置完成此过程需要的数据。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="1b8f6-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="1b8f6-107">此任务通常由产品设计器处理。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-107">This task is typically handled by the product designer.</span></span>

## <a name="select-the-product"></a><span data-ttu-id="1b8f6-108">选择产品</span><span class="sxs-lookup"><span data-stu-id="1b8f6-108">Select the product</span></span>

1. <span data-ttu-id="1b8f6-109">转到 **产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="1b8f6-110">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1b8f6-111">使用您以此顺序在第一个任务指南中创建的基于维度的配置技术查找发布的基础产品。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-111">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
1. <span data-ttu-id="1b8f6-112">在操作窗格上，选择 **工程师**。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-112">On the Action Pane, select **Engineer**.</span></span>
1. <span data-ttu-id="1b8f6-113">选择 **物料清单版本**。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-113">Select **BOM versions**.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="1b8f6-114">创建新的物料清单和物料清单版本</span><span class="sxs-lookup"><span data-stu-id="1b8f6-114">Create new BOM and BOM version</span></span>

1. <span data-ttu-id="1b8f6-115">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-115">Select **New**.</span></span>
1. <span data-ttu-id="1b8f6-116">选择 **物料清单和物料清单版本**。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-116">Select **BOM and BOM version**.</span></span>
1. <span data-ttu-id="1b8f6-117">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-117">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="1b8f6-118">设置站点</span><span class="sxs-lookup"><span data-stu-id="1b8f6-118">Setting a site</span></span>  
    * <span data-ttu-id="1b8f6-119">在此过程中，我们不设置物料清单的特定站点。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-119">In this procedure we don't set a specific site for the BOM.</span></span>  
1. <span data-ttu-id="1b8f6-120">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-120">Select **OK**.</span></span>
1. <span data-ttu-id="1b8f6-121">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-121">Select **New**.</span></span>
    * <span data-ttu-id="1b8f6-122">在此过程中，我们将添加四行到物料清单。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-122">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="1b8f6-123">两行表示电缆选项，两行表示机柜选项。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-123">Two lines represent cable options and two lines represent cabinet options.</span></span>  
1. <span data-ttu-id="1b8f6-124">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-124">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="1b8f6-125">在 **物料编号** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-125">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="1b8f6-126">选择物料编号 A0001，HDMI 6' 电缆。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-126">Select item number A0001, HDMI 6' Cables.</span></span>  
1. <span data-ttu-id="1b8f6-127">在 **配置组** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-127">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="1b8f6-128">选择以此顺序在指南 4 中创建的电缆配置组。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-128">Select the cable configuration group created in guide 4 in this sequence.</span></span>  
1. <span data-ttu-id="1b8f6-129">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-129">Select **New**.</span></span>
    * <span data-ttu-id="1b8f6-130">选择物料编号 A0002，HDMI 12' 电缆。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-130">Select item number A0002, HDMI 12' Cables.</span></span>  
1. <span data-ttu-id="1b8f6-131">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-131">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="1b8f6-132">在 **物料编号** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-132">In the **Item number** field, enter or select a value.</span></span>
1. <span data-ttu-id="1b8f6-133">在 **配置组** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-133">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="1b8f6-134">再次选择电缆配置组。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-134">Select the cable configuration group again.</span></span>  
1. <span data-ttu-id="1b8f6-135">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-135">Select **New**.</span></span>
1. <span data-ttu-id="1b8f6-136">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-136">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="1b8f6-137">在 **物料编号** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-137">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="1b8f6-138">选择物料编号 D0002 机柜。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-138">Select item number D0002 Cabinet.</span></span>  
1. <span data-ttu-id="1b8f6-139">在 **配置组** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-139">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="1b8f6-140">选择此物料清单行的机柜配置组。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-140">Select the cabinet configuration group for this BOM line.</span></span>  
1. <span data-ttu-id="1b8f6-141">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-141">Select **New**.</span></span>
1. <span data-ttu-id="1b8f6-142">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-142">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="1b8f6-143">在 **物料编号** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-143">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="1b8f6-144">选择物料编号 M0007 StandardCabinet 作为最后的物料清单行。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-144">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
1. <span data-ttu-id="1b8f6-145">在 **配置组** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-145">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="1b8f6-146">选择最后物料清单行的机柜配置组。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-146">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="1b8f6-147">审核并启用</span><span class="sxs-lookup"><span data-stu-id="1b8f6-147">Approve and activate</span></span>

1. <span data-ttu-id="1b8f6-148">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-148">Close the page.</span></span>
1. <span data-ttu-id="1b8f6-149">选择 **审核**。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-149">Select **Approve**.</span></span>
1. <span data-ttu-id="1b8f6-150">在 **审核人** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-150">In the **Approved by** field, enter or select a value.</span></span>
1. <span data-ttu-id="1b8f6-151">在 **是否还要审核该物料清单?** 字段中选择 *是*。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-151">Select *Yes* in the **Do you also want to approve the bill of materials?** field.</span></span>
1. <span data-ttu-id="1b8f6-152">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-152">Select **OK**.</span></span>
1. <span data-ttu-id="1b8f6-153">选择 **激活**。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-153">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
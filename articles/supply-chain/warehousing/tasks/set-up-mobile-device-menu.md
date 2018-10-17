--- 
title: "设置用于完成采购订单类型工作的移动设备菜单项"
description: "此过程演示如何设置“移动设备”菜单项。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 326a0039d2769ee5f459a87c302c93604d2379aa
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a><span data-ttu-id="97207-103">设置用于完成采购订单类型工作的移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="97207-103">Set up a mobile device menu item for completing work of type Purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97207-104">此过程演示如何设置“移动设备”菜单项。</span><span class="sxs-lookup"><span data-stu-id="97207-104">This procedure shows how to set up a Mobile device menu item.</span></span> <span data-ttu-id="97207-105">在此示例中，此菜单项用于执行采购订单类型的工作。</span><span class="sxs-lookup"><span data-stu-id="97207-105">In this example, the menu item is used for performing work of type Purchase order.</span></span> <span data-ttu-id="97207-106">与此菜单项关联的工作类决定哪项工作有效。</span><span class="sxs-lookup"><span data-stu-id="97207-106">The work class that’s associated with the menu item determines which work is valid.</span></span> <span data-ttu-id="97207-107">您可以使用演示数据公司 USMF 运行此指南。</span><span class="sxs-lookup"><span data-stu-id="97207-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="97207-108">此过程通常由仓库经理执行。</span><span class="sxs-lookup"><span data-stu-id="97207-108">This procedure is typically carried out by a warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="97207-109">创建移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="97207-109">Create a mobile device menu item</span></span>
1. <span data-ttu-id="97207-110">转到“移动设备菜单项”。</span><span class="sxs-lookup"><span data-stu-id="97207-110">Go to Mobile device menu items.</span></span>
2. <span data-ttu-id="97207-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="97207-111">Click New.</span></span>
3. <span data-ttu-id="97207-112">在“菜单项名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="97207-112">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="97207-113">输入唯一值。</span><span class="sxs-lookup"><span data-stu-id="97207-113">Enter a unique value.</span></span> <span data-ttu-id="97207-114">例如，您可以键入 POMove。</span><span class="sxs-lookup"><span data-stu-id="97207-114">For example, you could type POMove.</span></span> <span data-ttu-id="97207-115">请记住此值，您稍后需要用到。</span><span class="sxs-lookup"><span data-stu-id="97207-115">Remember the value, you'll need it later.</span></span>  
4. <span data-ttu-id="97207-116">在“标题”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="97207-116">In the Title field, type a value.</span></span>
    * <span data-ttu-id="97207-117">这是标题，将在移动设备上显示。</span><span class="sxs-lookup"><span data-stu-id="97207-117">This is the title which will be displayed on the mobile device.</span></span> <span data-ttu-id="97207-118">例如，您可以键入 PO Move。</span><span class="sxs-lookup"><span data-stu-id="97207-118">For example, you could type PO Move.</span></span>  
5. <span data-ttu-id="97207-119">在“模式”字段中，选择“工作”。</span><span class="sxs-lookup"><span data-stu-id="97207-119">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="97207-120">在“使用现有工作”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="97207-120">Select Yes in the Use existing work field.</span></span>
    * <span data-ttu-id="97207-121">该移动设备菜单项用于执行现有的工作。</span><span class="sxs-lookup"><span data-stu-id="97207-121">This mobile device menu item is used to perform existing work.</span></span> <span data-ttu-id="97207-122">因此必须将此值设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="97207-122">Therefore you must set this value to Yes.</span></span>  
    * <span data-ttu-id="97207-123">“显示库存状态”字段确定是否向移动设备上的仓库工作人员显示现有库存的库存状态。</span><span class="sxs-lookup"><span data-stu-id="97207-123">The Display inventory status field determines whether the inventory status of the on-hand inventory will be displayed to the warehouse worker on the mobile device.</span></span>  
7. <span data-ttu-id="97207-124">在“主管”字段中，选择“系统分组”。</span><span class="sxs-lookup"><span data-stu-id="97207-124">In the Directed by field, select 'System grouping'.</span></span>
    * <span data-ttu-id="97207-125">在“主管”字段中进行了选择时，将在该页中的“常规”部分显示更多字段。</span><span class="sxs-lookup"><span data-stu-id="97207-125">When you select something in the Directed by field, additional fields appear in the General section on this page.</span></span> <span data-ttu-id="97207-126">显示的字段取决于您选择的内容。</span><span class="sxs-lookup"><span data-stu-id="97207-126">The fields that appear depend on what you selected.</span></span> <span data-ttu-id="97207-127">如果您选择“系统分组”，将添加两个新字段。</span><span class="sxs-lookup"><span data-stu-id="97207-127">When you select System grouping, two new fields are added.</span></span> <span data-ttu-id="97207-128">这些在下文中说明。</span><span class="sxs-lookup"><span data-stu-id="97207-128">These are explained below.</span></span>  
8. <span data-ttu-id="97207-129">在“系统分组”字段中，选择“WorkPoolId”。</span><span class="sxs-lookup"><span data-stu-id="97207-129">In the System grouping field, select 'WorkPoolId'.</span></span>
    * <span data-ttu-id="97207-130">当仓库工作人员打开该菜单项时，将要求他们扫描工作池 ID。</span><span class="sxs-lookup"><span data-stu-id="97207-130">When warehouse workers open this menu item, they’ll be asked to scan a Work pool ID.</span></span> <span data-ttu-id="97207-131">具有此工作池 ID 的所有工作订单以及具有添加到此菜单项的工作类之一的未结工作订单行将被推送到用户。</span><span class="sxs-lookup"><span data-stu-id="97207-131">All work orders with this Work pool ID and open work order lines with one of the work classes added to this menu item will be pushed to the user.</span></span>  
9. <span data-ttu-id="97207-132">在“系统分组标签”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="97207-132">In the System grouping label field, type a value.</span></span>
    * <span data-ttu-id="97207-133">这是将显示给移动设备用户的文本。</span><span class="sxs-lookup"><span data-stu-id="97207-133">This is the text displayed to the user on the mobile device.</span></span> <span data-ttu-id="97207-134">例如，您可以键入 Work pool。</span><span class="sxs-lookup"><span data-stu-id="97207-134">For example, you could type Work pool.</span></span>  
10. <span data-ttu-id="97207-135">在“放置时覆盖牌照”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="97207-135">Select Yes in the Override license plate during put field.</span></span>
    * <span data-ttu-id="97207-136">当物料放置在牌照控制位置时，此选项允许仓库工作人员覆盖目标牌照。</span><span class="sxs-lookup"><span data-stu-id="97207-136">This option allows warehouse workers to override the target license plate when items are put down on a license plate controlled location.</span></span>  
11. <span data-ttu-id="97207-137">在“入库组”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="97207-137">Select Yes in the Group put away field.</span></span>
    * <span data-ttu-id="97207-138">如果工作订单上的所有“放置”行都共享同一位置，则用户将收到一个用于所有行组合的“放置”指令。</span><span class="sxs-lookup"><span data-stu-id="97207-138">If all the Put lines on the work order share the same location, the user will receive one combined Put instruction for all lines.</span></span>  
    * <span data-ttu-id="97207-139">审计模板 ID：工作审计模板允许您指定菜单项的工作流程应该被中断，以便可以执行其他操作。</span><span class="sxs-lookup"><span data-stu-id="97207-139">Audit template ID: A work audit template allows you to specify that the work process for a menu item should be interrupted so that another operation can be performed.</span></span> <span data-ttu-id="97207-140">例如，如果一个菜单项适用于入站工作，则审计模板可能要求工作人员检查温度。</span><span class="sxs-lookup"><span data-stu-id="97207-140">For example, if this menu item is for inbound work, the audit template might require that the worker checks the temperature.</span></span> <span data-ttu-id="97207-141">审核模板中说明了流程被中断的点，例如，工作起始或结束点，或者状态改变时的点。</span><span class="sxs-lookup"><span data-stu-id="97207-141">The point at which the process is interrupted is specified on the audit template and can be, for example, when work is started or completed, or when its status changes.</span></span>  
12. <span data-ttu-id="97207-142">展开“工作类”部分。</span><span class="sxs-lookup"><span data-stu-id="97207-142">Expand the Work classes section.</span></span>
13. <span data-ttu-id="97207-143">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="97207-143">Click New.</span></span>
14. <span data-ttu-id="97207-144">在“工作类 ID”字段中，键入“采购”。</span><span class="sxs-lookup"><span data-stu-id="97207-144">In the Work class ID field, type 'Purchase'.</span></span>
    * <span data-ttu-id="97207-145">工作池限制该菜单项可以用于的工作。</span><span class="sxs-lookup"><span data-stu-id="97207-145">The work pool restricts the work that the menu item can be used for.</span></span> <span data-ttu-id="97207-146">在这种情况下，其将用于具有采购工作类 ID 的未结工作订单行。</span><span class="sxs-lookup"><span data-stu-id="97207-146">In this case it will be used for open work order lines that have the Purchase work class ID.</span></span>  
15. <span data-ttu-id="97207-147">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="97207-147">Click Save.</span></span>

## <a name="set-up-work-confirmation"></a><span data-ttu-id="97207-148">设置工作确认</span><span class="sxs-lookup"><span data-stu-id="97207-148">Set up work confirmation</span></span>
1. <span data-ttu-id="97207-149">单击“工作确认设置”。</span><span class="sxs-lookup"><span data-stu-id="97207-149">Click Work confirmation setup.</span></span>
2. <span data-ttu-id="97207-150">在“工作类型”字段中，选择“领料”。</span><span class="sxs-lookup"><span data-stu-id="97207-150">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="97207-151">选择“自动确认”复选框。</span><span class="sxs-lookup"><span data-stu-id="97207-151">Select the Auto confirm check box.</span></span>
    * <span data-ttu-id="97207-152">工作类型为“领料”的工作指令将会自动确认。</span><span class="sxs-lookup"><span data-stu-id="97207-152">The work instruction with work type Pick will be auto-confirmed.</span></span> <span data-ttu-id="97207-153">此指令不会向用户显示。</span><span class="sxs-lookup"><span data-stu-id="97207-153">This instruction will not be presented to the user.</span></span>  
4. <span data-ttu-id="97207-154">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="97207-154">Click New.</span></span>
5. <span data-ttu-id="97207-155">在“工作类型”字段中，选择“放置”。</span><span class="sxs-lookup"><span data-stu-id="97207-155">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="97207-156">选择“库位确认”复选框。</span><span class="sxs-lookup"><span data-stu-id="97207-156">Select the Location confirmation check box.</span></span>
    * <span data-ttu-id="97207-157">当放置物料时，仓库工作人员可能需要执行位置确认扫描。</span><span class="sxs-lookup"><span data-stu-id="97207-157">The warehouse worker will be asked to perform a confirmation scan of the location, when the item is put down.</span></span>  
7. <span data-ttu-id="97207-158">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="97207-158">Click Save.</span></span>
8. <span data-ttu-id="97207-159">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="97207-159">Close the page.</span></span>
9. <span data-ttu-id="97207-160">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="97207-160">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="97207-161">添加菜单项到一个移动设备菜单</span><span class="sxs-lookup"><span data-stu-id="97207-161">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="97207-162">转到“移动设备菜单”。</span><span class="sxs-lookup"><span data-stu-id="97207-162">Go to Mobile device menu.</span></span>
2. <span data-ttu-id="97207-163">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="97207-163">Click Edit.</span></span>
3. <span data-ttu-id="97207-164">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="97207-164">Use the Quick Filter to find records.</span></span> <span data-ttu-id="97207-165">例如，在“名称”字段中筛选值“入货”。</span><span class="sxs-lookup"><span data-stu-id="97207-165">For example, filter on the Name field with a value of 'inbound'.</span></span>
    * <span data-ttu-id="97207-166">您需要查找用于入站菜单项的菜单。</span><span class="sxs-lookup"><span data-stu-id="97207-166">You want to find the menu you use for inbound menu items.</span></span> <span data-ttu-id="97207-167">在 USMF 中，这称为入站。</span><span class="sxs-lookup"><span data-stu-id="97207-167">In USMF this is called Inbound.</span></span>  
4. <span data-ttu-id="97207-168">在树形图中，选择“一个值”。</span><span class="sxs-lookup"><span data-stu-id="97207-168">In the tree, select 'a value'.</span></span>
5. <span data-ttu-id="97207-169">单击向右箭头。</span><span class="sxs-lookup"><span data-stu-id="97207-169">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="97207-170">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="97207-170">Click Save.</span></span>
7. <span data-ttu-id="97207-171">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="97207-171">Close the page.</span></span>



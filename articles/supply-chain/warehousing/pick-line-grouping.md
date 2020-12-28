---
title: 领料行分组
description: 本主题概述领料行分组。
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b3497d43a500898207ed5154721ee0e3a327fb93
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4423332"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="7529b-103">领料行分组</span><span class="sxs-lookup"><span data-stu-id="7529b-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7529b-104">在领料行分组中，可以将具有相同物料和位置的多个工作行合并为一个领料，来在移动设备上向用户显示。</span><span class="sxs-lookup"><span data-stu-id="7529b-104">In pick line grouping, multiple work lines that have the same item and location can be combined into a single pick that is presented to the user on a mobile device.</span></span> <span data-ttu-id="7529b-105">这样，仓库工作人员可以收到可能的最有效的指令，而系统中工作行的必要分隔也会得以保持（例如，针对不同的容器和订单）。</span><span class="sxs-lookup"><span data-stu-id="7529b-105">Therefore, warehouse workers can receive the most efficient instructions that are possible, but the required separation of work lines in the system is also maintained (for example, for different containers and orders).</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="7529b-106">设置领料行分组</span><span class="sxs-lookup"><span data-stu-id="7529b-106">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="7529b-107">创建移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="7529b-107">Create a mobile device menu item</span></span>

1. <span data-ttu-id="7529b-108">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**，创建一个名为 **销售组行领料 – 用户导向** 的新菜单项。</span><span class="sxs-lookup"><span data-stu-id="7529b-108">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**, and create a new menu item that is named **Sales group line picking – User directed**.</span></span>
2. <span data-ttu-id="7529b-109">在 **移动设备菜单项** 下，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="7529b-109">Under **Mobile device menu items**, set the following values:</span></span>

    - <span data-ttu-id="7529b-110">在 **菜单项名称** 字段中，输入 **销售领料 - 组行**。</span><span class="sxs-lookup"><span data-stu-id="7529b-110">In the **Menu item name** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="7529b-111">在 **标题** 字段中，输入 **销售领料 - 组行**。</span><span class="sxs-lookup"><span data-stu-id="7529b-111">In the **Title** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="7529b-112">在 **模式** 字段中，选择 **工作**。</span><span class="sxs-lookup"><span data-stu-id="7529b-112">In the **Mode** field, select **Work**.</span></span>
    - <span data-ttu-id="7529b-113">将 **使用现有工作** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="7529b-113">Set the **Use existing work** option to **Yes**.</span></span>

3. <span data-ttu-id="7529b-114">在 **常规** 快速选项卡上，您可以设置以下值：</span><span class="sxs-lookup"><span data-stu-id="7529b-114">On the **General** FastTab, you can set the following values:</span></span>

    - <span data-ttu-id="7529b-115">在 **导向方式** 字段中，选择 **用户导向**。</span><span class="sxs-lookup"><span data-stu-id="7529b-115">In the **Directed by** field, select **User directed**.</span></span>
    - <span data-ttu-id="7529b-116">将 **生成牌照** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="7529b-116">Set the **Generate license plate** option to **Yes**.</span></span>
    - <span data-ttu-id="7529b-117">将 **组领料** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="7529b-117">Set the **Group pick** option to **Yes**.</span></span>

4. <span data-ttu-id="7529b-118">在 **工作类** 快速选项卡上，按照以下步骤为移动设备菜单项配置有效的工作类：</span><span class="sxs-lookup"><span data-stu-id="7529b-118">On the **Work classes** FastTab, follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="7529b-119">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="7529b-119">Select **New**.</span></span>
    2. <span data-ttu-id="7529b-120">在 **工作类 ID** 字段中，选择 **销售** 或 **SO 领料**，具体取决于您要使用的仓库。</span><span class="sxs-lookup"><span data-stu-id="7529b-120">In the **Work class ID** field, select **Sales** or **SO Pick**, depending on the warehouse that you will use.</span></span>
    3. <span data-ttu-id="7529b-121">在 **工作订单类型** 字段中，选择 **销售订单**。</span><span class="sxs-lookup"><span data-stu-id="7529b-121">In the **Work order type** field, select **Sales orders**.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="7529b-122">设置移动设备菜单</span><span class="sxs-lookup"><span data-stu-id="7529b-122">Set up a mobile device menu</span></span>

1. <span data-ttu-id="7529b-123">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单**。</span><span class="sxs-lookup"><span data-stu-id="7529b-123">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span> 
1. <span data-ttu-id="7529b-124">将刚才创建的菜单项添加到所需菜单。</span><span class="sxs-lookup"><span data-stu-id="7529b-124">Add the menu item that you just created to the desired menu.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="7529b-125">设置工作模板</span><span class="sxs-lookup"><span data-stu-id="7529b-125">Set up a work template</span></span>

1. <span data-ttu-id="7529b-126">转到 **仓库管理 \> 设置 \> 工作 \> 工作模板**。</span><span class="sxs-lookup"><span data-stu-id="7529b-126">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="7529b-127">查找此功能应使用的工作模板。</span><span class="sxs-lookup"><span data-stu-id="7529b-127">Find the work template that should be used with this function.</span></span> <span data-ttu-id="7529b-128">对于此示例，选择标准的 **51 Pick to stage** Contoso 工作模板。</span><span class="sxs-lookup"><span data-stu-id="7529b-128">For this example, select the standard **51 Pick to stage** Contoso work template.</span></span>
1. <span data-ttu-id="7529b-129">在菜单上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="7529b-129">On the menu, select **Edit query**.</span></span>
1. <span data-ttu-id="7529b-130">在 **排序** 选项卡上，选择 **添加**，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="7529b-130">On the **Sorting** tab, select **Add**, and then set the following values:</span></span>

    - <span data-ttu-id="7529b-131">在 **表** 字段中，选择 **临时工作交易记录**。</span><span class="sxs-lookup"><span data-stu-id="7529b-131">In the **Table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="7529b-132">在 **派生表** 字段中，选择 **临时工作交易记录**。</span><span class="sxs-lookup"><span data-stu-id="7529b-132">In the **Derived table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="7529b-133">在 **字段** 字段中，选择 **物料编号**。</span><span class="sxs-lookup"><span data-stu-id="7529b-133">In the **Field** field, select **Item number**.</span></span>
    - <span data-ttu-id="7529b-134">在 **搜索方向** 字段中，选择 **升序**。</span><span class="sxs-lookup"><span data-stu-id="7529b-134">In the **Search direction** field, select **Ascending**.</span></span>

> [!NOTE]
> <span data-ttu-id="7529b-135">为了使领料行分组功能正常工作，必须按物料 ID 对工作行进行排序。</span><span class="sxs-lookup"><span data-stu-id="7529b-135">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="7529b-136">如果具有相同物料的行没有逐个排序，将不会对它们分组。</span><span class="sxs-lookup"><span data-stu-id="7529b-136">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="7529b-137">示例</span><span class="sxs-lookup"><span data-stu-id="7529b-137">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="7529b-138">创建领料工作</span><span class="sxs-lookup"><span data-stu-id="7529b-138">Create picking work</span></span>

<span data-ttu-id="7529b-139">您必须先创建一些合格的出货工作，然后才能设置领料行分组。</span><span class="sxs-lookup"><span data-stu-id="7529b-139">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="7529b-140">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="7529b-140">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="7529b-141">选择 **新建** 以创建新的销售订单。</span><span class="sxs-lookup"><span data-stu-id="7529b-141">Select **New** to create a sales order.</span></span> 
3. <span data-ttu-id="7529b-142">在 **客户帐户** 字段中，选择任意客户。</span><span class="sxs-lookup"><span data-stu-id="7529b-142">In the **Customer account** field, select any customer.</span></span> 
4. <span data-ttu-id="7529b-143">在 **常规** 快速选项卡上的 **仓库** 字段中，选择 **51**。</span><span class="sxs-lookup"><span data-stu-id="7529b-143">On the **General** FastTab, in the **Warehouse** field, select **51**.</span></span> <span data-ttu-id="7529b-144">然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="7529b-144">Then select **OK**.</span></span>
5. <span data-ttu-id="7529b-145">在 **销售订单行** 下，添加以下六行：</span><span class="sxs-lookup"><span data-stu-id="7529b-145">Under **Sales order lines**, add the following six lines:</span></span>

    - <span data-ttu-id="7529b-146">**行 1：** 在 **物料编号** 字段中，选择 **M9200**。</span><span class="sxs-lookup"><span data-stu-id="7529b-146">**Line 1:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="7529b-147">在 **数量** 字段中，输入 **3**。</span><span class="sxs-lookup"><span data-stu-id="7529b-147">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="7529b-148">**行 2：** 在 **物料编号** 字段中，选择 **M9201**。</span><span class="sxs-lookup"><span data-stu-id="7529b-148">**Line 2:** In the **Item number** field, select **M9201**.</span></span> <span data-ttu-id="7529b-149">在 **数量** 字段中，输入 **3**。</span><span class="sxs-lookup"><span data-stu-id="7529b-149">In the **Quantity** field, enter **3**.</span></span> 
    - <span data-ttu-id="7529b-150">**行 3：** 在 **物料编号** 字段中，选择 **M9202**。</span><span class="sxs-lookup"><span data-stu-id="7529b-150">**Line 3:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="7529b-151">在 **数量** 字段中，输入 **2**。</span><span class="sxs-lookup"><span data-stu-id="7529b-151">In the **Quantity** field, enter **2**.</span></span> 
    - <span data-ttu-id="7529b-152">**行 4：** 在 **物料编号** 字段中，选择 **M9200**。</span><span class="sxs-lookup"><span data-stu-id="7529b-152">**Line 4:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="7529b-153">在 **数量** 字段中，输入 **1**。</span><span class="sxs-lookup"><span data-stu-id="7529b-153">In the **Quantity** field, enter **1**.</span></span> 
    - <span data-ttu-id="7529b-154">**行 5：** 在 **物料编号** 字段中，选择 **M9200**。</span><span class="sxs-lookup"><span data-stu-id="7529b-154">**Line 5:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="7529b-155">在 **数量** 字段中，输入 **3**。</span><span class="sxs-lookup"><span data-stu-id="7529b-155">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="7529b-156">**行 6：** 在 **物料编号** 字段中，选择 **M9202**。</span><span class="sxs-lookup"><span data-stu-id="7529b-156">**Line 6:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="7529b-157">在 **数量** 字段中，输入 **7**。</span><span class="sxs-lookup"><span data-stu-id="7529b-157">In the **Quantity** field, enter **7**.</span></span> 

    <span data-ttu-id="7529b-158">以下是每个物料的总数量的汇总：</span><span class="sxs-lookup"><span data-stu-id="7529b-158">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="7529b-159">**物料 M9200：** 各 7</span><span class="sxs-lookup"><span data-stu-id="7529b-159">**Item M9200:** 7 each</span></span>
    - <span data-ttu-id="7529b-160">**物料 M9201：** 各 3</span><span class="sxs-lookup"><span data-stu-id="7529b-160">**Item M9201:** 3 each</span></span>
    - <span data-ttu-id="7529b-161">**物料 M9202：** 各 9</span><span class="sxs-lookup"><span data-stu-id="7529b-161">**Item M9202:** 9 each</span></span>

6. <span data-ttu-id="7529b-162">在将订单下达到仓库之前，必须确保领料库位有满足所有订单上的所有物料的足够库存。</span><span class="sxs-lookup"><span data-stu-id="7529b-162">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="7529b-163">查看 **库位指令** 设置，确定用于销售订单领料的领料库位。</span><span class="sxs-lookup"><span data-stu-id="7529b-163">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span>
7. <span data-ttu-id="7529b-164">预留库存，并将其下达到仓库。</span><span class="sxs-lookup"><span data-stu-id="7529b-164">Reserve the inventory, and release it to the warehouse.</span></span> <span data-ttu-id="7529b-165">具有六行的工作 ID 已创建。</span><span class="sxs-lookup"><span data-stu-id="7529b-165">A work ID that has six lines is created.</span></span> <span data-ttu-id="7529b-166">这些行按物料编号排序。</span><span class="sxs-lookup"><span data-stu-id="7529b-166">The lines are sorted by item number.</span></span>

### <a name="run-the-mobile-device-flow"></a><span data-ttu-id="7529b-167">运行移动设备流</span><span class="sxs-lookup"><span data-stu-id="7529b-167">Run the mobile device flow</span></span>

1. <span data-ttu-id="7529b-168">在移动设备上，选择包含新的移动设备菜单项的菜单。</span><span class="sxs-lookup"><span data-stu-id="7529b-168">On the mobile device, select the menu that includes the new mobile device menu item.</span></span>
1. <span data-ttu-id="7529b-169">选择 **销售领料 – 组行** 菜单项，然后启动领料。</span><span class="sxs-lookup"><span data-stu-id="7529b-169">Select the **Sales Pick – Group line** menu item, and initiate the pick.</span></span>

    <span data-ttu-id="7529b-170">选择菜单并输入工作 ID 后，您将看到将物料 M9200 的所有领料行分组的领料步骤。</span><span class="sxs-lookup"><span data-stu-id="7529b-170">After you select the menu and enter the work ID, you see the pick step where all pick lines for item M9200 are grouped.</span></span> <span data-ttu-id="7529b-171">您会收到每个 M9200 物料领取 7 的指令。</span><span class="sxs-lookup"><span data-stu-id="7529b-171">You receive an instruction to pick 7 each of item M9200.</span></span>

1. <span data-ttu-id="7529b-172">确认领料步骤。</span><span class="sxs-lookup"><span data-stu-id="7529b-172">Confirm the pick step.</span></span> 
1. <span data-ttu-id="7529b-173">转到进行中的工作的客户端屏幕，注意查看物料 M9200 的所有三个领料行已同时关闭。</span><span class="sxs-lookup"><span data-stu-id="7529b-173">Go to the client screen of the work in process, and notice that all three pick lines for item M9200 were closed simultaneously.</span></span>

    <span data-ttu-id="7529b-174">工作行 4 已出现。</span><span class="sxs-lookup"><span data-stu-id="7529b-174">Work line 4 is presented.</span></span>

1. <span data-ttu-id="7529b-175">确认领料步骤。</span><span class="sxs-lookup"><span data-stu-id="7529b-175">Confirm the pick step.</span></span>

    <span data-ttu-id="7529b-176">移动设备上的最后一个领料步骤聚合了工作订单的最后两个领料行。</span><span class="sxs-lookup"><span data-stu-id="7529b-176">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>

1. <span data-ttu-id="7529b-177">完成每个 M9202 物料领取 9 的领料步骤。</span><span class="sxs-lookup"><span data-stu-id="7529b-177">Complete the pick step for 9 each of item M9202.</span></span>
1. <span data-ttu-id="7529b-178">确认放置步骤以及所有其他领料/放置对以完成工作。</span><span class="sxs-lookup"><span data-stu-id="7529b-178">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!NOTE]
> - <span data-ttu-id="7529b-179">只有处于序列中时工作行才会被分组。</span><span class="sxs-lookup"><span data-stu-id="7529b-179">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="7529b-180">不支持以下功能：</span><span class="sxs-lookup"><span data-stu-id="7529b-180">The following functionality isn't supported:</span></span>
>
>    - <span data-ttu-id="7529b-181">实际称重物料。</span><span class="sxs-lookup"><span data-stu-id="7529b-181">Catch-weight items.</span></span> <span data-ttu-id="7529b-182">如果工作中有任何实际称重物料，在开始领料之前您会收到一条错误消息。</span><span class="sxs-lookup"><span data-stu-id="7529b-182">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>    - <span data-ttu-id="7529b-183">单件领料。</span><span class="sxs-lookup"><span data-stu-id="7529b-183">Piece picking.</span></span>
>    - <span data-ttu-id="7529b-184">有未完成的补货工作的工作行。</span><span class="sxs-lookup"><span data-stu-id="7529b-184">Work lines that have unfinished replenishment work.</span></span>
>    - <span data-ttu-id="7529b-185">过量领料。</span><span class="sxs-lookup"><span data-stu-id="7529b-185">Over-picking.</span></span>
>    - <span data-ttu-id="7529b-186">物料重新分配的领料短缺</span><span class="sxs-lookup"><span data-stu-id="7529b-186">Short picking with item reallocation</span></span>

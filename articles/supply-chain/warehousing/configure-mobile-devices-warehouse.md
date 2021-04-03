---
title: 为仓库工作设置移动设备
description: 此主题介绍了如何配置仓库工作人员用于在移动设备上执行工作的菜单项。
author: MarkusFogelberg
manager: tfehr
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFSysDirSort, WHSWorkUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: 29941
ms.assetid: 6dff6313-dc6e-4f06-9c0c-dab24eefe4da
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db4c3a8c4bae226b5e154f4761e30b7341bc527b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232975"
---
# <a name="set-up-mobile-devices-for-warehouse-work"></a><span data-ttu-id="cedcb-103">为仓库工作设置移动设备</span><span class="sxs-lookup"><span data-stu-id="cedcb-103">Set up mobile devices for warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cedcb-104">此主题介绍了如何配置仓库工作人员用于在移动设备上执行工作的菜单项。</span><span class="sxs-lookup"><span data-stu-id="cedcb-104">This topic describes how to configure the menu items that warehouse workers use to perform work on a mobile device.</span></span>

> [!NOTE]
> <span data-ttu-id="cedcb-105">本主题适用于仓库管理中的功能。</span><span class="sxs-lookup"><span data-stu-id="cedcb-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="cedcb-106">它不适用于库存管理中的功能。</span><span class="sxs-lookup"><span data-stu-id="cedcb-106">It doesn't apply to features in Inventory management.</span></span> <span data-ttu-id="cedcb-107">显示在仓库移动设备的菜单中的菜单项在 **移动设备菜单项** 页上配置。</span><span class="sxs-lookup"><span data-stu-id="cedcb-107">The menu items that appear on the menus on a warehouse mobile device are configured on the **Mobile device menu items** page.</span></span> <span data-ttu-id="cedcb-108">由于菜单项可以放到不同的菜单上，配置菜单结构容易，以便只向特定用户显示特定类型的工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-108">Because the menu items can be put onto different menus, it's easy to configure menu structures so that only specific types of work are exposed to specific users.</span></span> <span data-ttu-id="cedcb-109">您可以配置菜单项执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="cedcb-109">You can configure menu items to perform the following tasks:</span></span>

- <span data-ttu-id="cedcb-110">处理查询或执行活动，如打印标签、生成牌照号码、开始生产订单或快速查找位置中的物料信息。</span><span class="sxs-lookup"><span data-stu-id="cedcb-110">Process an inquiry or perform an activity, such as printing a label, generating license plate numbers, starting a production order, or quickly looking up information about items in a location.</span></span>
- <span data-ttu-id="cedcb-111">通过另一流程创建要执行的工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-111">Create work that will be performed through another process.</span></span> <span data-ttu-id="cedcb-112">例如，接收采购订单物料可以创建另一名工人的入库工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-112">For example, receiving an item for a purchase order can create put-away work for another worker.</span></span>
- <span data-ttu-id="cedcb-113">执行由其他流程（现有工作）创建的工作，例如存储接收采购订单的物料时创建的工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-113">Perform work that was created by another process (existing work), such as put-away work that was created when an item was received for a purchase order.</span></span>

<span data-ttu-id="cedcb-114">若要创建活动或查询的菜单项，将 **模式** 字段设置为 **间接**。</span><span class="sxs-lookup"><span data-stu-id="cedcb-114">To create a menu item for an activity or inquiry, set the **Mode** field to **Indirect**.</span></span> <span data-ttu-id="cedcb-115">**活动代码** 选项的列表然后将可用，以便您可以选择菜单项针对的查询或活动的类型。</span><span class="sxs-lookup"><span data-stu-id="cedcb-115">A list of **Activity code** options then becomes available, so that you can select the type of inquiry or activity that the menu item is for.</span></span> <span data-ttu-id="cedcb-116">若要创建菜单项以生成仓库工作，将 **模式** 字段设置为 **工作**。</span><span class="sxs-lookup"><span data-stu-id="cedcb-116">To create a menu item to generate warehouse work, set the **Mode** field to **Work**.</span></span> <span data-ttu-id="cedcb-117">**工作创建流程** 选项的列表然后变得可用。</span><span class="sxs-lookup"><span data-stu-id="cedcb-117">A list of **Work creation process** options then becomes available.</span></span> <span data-ttu-id="cedcb-118">若要创建菜单项以处理现有的仓库工作，设置 **模式** 字段为 **工作**，然后设置 **使用现有工作** 选项为 **是**。</span><span class="sxs-lookup"><span data-stu-id="cedcb-118">To create a menu item to process existing warehouse work, set the **Mode** field to **Work**, and then set the **Use existing work** option to **Yes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="cedcb-119">其他字段可能可用于菜单项，具体取决于为菜单项选择的模式，以及菜单项是否用于执行现有工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-119">Additional fields might be available for menu items, depending on the mode that you select for the menu item, and whether the menu item is used to perform existing work.</span></span> <span data-ttu-id="cedcb-120">有关其他字段选择的信息，请参阅本主题后面的“其他菜单项选项”部分。</span><span class="sxs-lookup"><span data-stu-id="cedcb-120">For information about the additional field selections, see the “Additional menu item options” section later in this topic.</span></span>

## <a name="configure-menu-items-for-activities-and-inquiries"></a><span data-ttu-id="cedcb-121">配置活动和查询的菜单项</span><span class="sxs-lookup"><span data-stu-id="cedcb-121">Configure menu items for activities and inquiries</span></span>
<span data-ttu-id="cedcb-122">如果菜单项的 **模式** 字段设置为 **间接**，则可以创建菜单项以执行不创建工作的一般活动或查询。</span><span class="sxs-lookup"><span data-stu-id="cedcb-122">If the **Mode** field for a menu item is set to **Indirect**, you can create a menu item to perform a general activity or inquiry that doesn't create work.</span></span> <span data-ttu-id="cedcb-123">示例包括重新打印牌照标签，以及位置中物料查询。</span><span class="sxs-lookup"><span data-stu-id="cedcb-123">Examples include reprinting license plate labels and an inquiry about the items in a location.</span></span> <span data-ttu-id="cedcb-124">下表列出了可用的选项。</span><span class="sxs-lookup"><span data-stu-id="cedcb-124">The following table lists the options that are available.</span></span>

| <span data-ttu-id="cedcb-125">选项</span><span class="sxs-lookup"><span data-stu-id="cedcb-125">Option</span></span> | <span data-ttu-id="cedcb-126">描述</span><span class="sxs-lookup"><span data-stu-id="cedcb-126">Description</span></span> |
|---|---|
| <span data-ttu-id="cedcb-127">无</span><span class="sxs-lookup"><span data-stu-id="cedcb-127">None</span></span> | <span data-ttu-id="cedcb-128">此默认值无法启用一个活动或查询。</span><span class="sxs-lookup"><span data-stu-id="cedcb-128">This default value doesn't enable an activity or inquiry.</span></span> |
| <span data-ttu-id="cedcb-129">关于</span><span class="sxs-lookup"><span data-stu-id="cedcb-129">About</span></span> | <span data-ttu-id="cedcb-130">查看有关系统的信息，如版本编号、仓库 ID 以及当前登录的工作人员。</span><span class="sxs-lookup"><span data-stu-id="cedcb-130">View information about the system, such as the version number, the warehouse ID, and the worker who is currently logged on.</span></span> |
| <span data-ttu-id="cedcb-131">更改仓库</span><span class="sxs-lookup"><span data-stu-id="cedcb-131">Change warehouse</span></span> | <span data-ttu-id="cedcb-132">改变工作人员登录的仓库。</span><span class="sxs-lookup"><span data-stu-id="cedcb-132">Change the warehouse that a worker is logged on to.</span></span> |
| <span data-ttu-id="cedcb-133">位置查询</span><span class="sxs-lookup"><span data-stu-id="cedcb-133">Location inquiry</span></span> | <span data-ttu-id="cedcb-134">查看位置所有的物料和数量的相关信息。</span><span class="sxs-lookup"><span data-stu-id="cedcb-134">View information about all items and quantities for a location.</span></span> |
| <span data-ttu-id="cedcb-135">牌照查询</span><span class="sxs-lookup"><span data-stu-id="cedcb-135">License plate inquiry</span></span> | <span data-ttu-id="cedcb-136">查看牌照上的物料数量以及牌照的位置。</span><span class="sxs-lookup"><span data-stu-id="cedcb-136">View the quantity of items on a license plate and the location of the license plate.</span></span> |
| <span data-ttu-id="cedcb-137">开始生产订单</span><span class="sxs-lookup"><span data-stu-id="cedcb-137">Start production order</span></span> | <span data-ttu-id="cedcb-138">开始生产订单。</span><span class="sxs-lookup"><span data-stu-id="cedcb-138">Start a production order.</span></span> |
| <span data-ttu-id="cedcb-139">生产废料</span><span class="sxs-lookup"><span data-stu-id="cedcb-139">Production scrap</span></span> | <span data-ttu-id="cedcb-140">输入每个物料清单 (BOM) 行在生产过程中产生的废品数量。</span><span class="sxs-lookup"><span data-stu-id="cedcb-140">Enter the quantity of scrap that was created during production for each bill of materials (BOM) line.</span></span> |
| <span data-ttu-id="cedcb-141">最后一个生产托盘</span><span class="sxs-lookup"><span data-stu-id="cedcb-141">Production last pallet</span></span> | <span data-ttu-id="cedcb-142">指出已按照生产订单生产了最后一托盘的物料，且必须更新生产订单的状态为 **完工入库**。</span><span class="sxs-lookup"><span data-stu-id="cedcb-142">Indicate that the last pallet of items has been produced for a production order, and that the status of the production order must be updated to **Reported as finished**.</span></span> <span data-ttu-id="cedcb-143">在生产过程中未消耗的原材料状态将由 **已领料** 更改回 **在单**，并且物料可返回到库存。</span><span class="sxs-lookup"><span data-stu-id="cedcb-143">The status of the raw materials that were not consumed during production is change back from **Picked** to **On order**, and the items can be returned to inventory.</span></span> |
| <span data-ttu-id="cedcb-144">物料查询</span><span class="sxs-lookup"><span data-stu-id="cedcb-144">Item inquiry</span></span> | <span data-ttu-id="cedcb-145">扫描物料以确定其在仓库中的位置。</span><span class="sxs-lookup"><span data-stu-id="cedcb-145">Scan an item to determine where it is in the warehouse.</span></span> <span data-ttu-id="cedcb-146">查询将返回被扫描物料的所有位置和数量。</span><span class="sxs-lookup"><span data-stu-id="cedcb-146">The inquiry returns all locations and quantities for the scanned item.</span></span> |
| <span data-ttu-id="cedcb-147">重新打印标签</span><span class="sxs-lookup"><span data-stu-id="cedcb-147">Reprint label</span></span> | <span data-ttu-id="cedcb-148">重新打印牌照标签。</span><span class="sxs-lookup"><span data-stu-id="cedcb-148">Reprint a license plate label.</span></span> |
| <span data-ttu-id="cedcb-149">牌照生成</span><span class="sxs-lookup"><span data-stu-id="cedcb-149">License plate build</span></span> | <span data-ttu-id="cedcb-150">将同一位置的多个牌照合并，创建一个父牌照。</span><span class="sxs-lookup"><span data-stu-id="cedcb-150">Create a parent license plate by combining multiple license plates in the same location.</span></span> <span data-ttu-id="cedcb-151">如果您同时移动多个牌照，可以使用此选项。</span><span class="sxs-lookup"><span data-stu-id="cedcb-151">This option is useful if you move multiple license plates at the same time.</span></span> <span data-ttu-id="cedcb-152">当您移动父牌照之后，在从每个牌照中选择物料时，必须执行牌照中断休息。</span><span class="sxs-lookup"><span data-stu-id="cedcb-152">After the parent license plate is moved, you must perform a license plate break before you can pick items from each license plate.</span></span> <p></p><span data-ttu-id="cedcb-153">**提示：** 若要移动父牌照，您必须使用配置为创建移动工作的移动设备。</span><span class="sxs-lookup"><span data-stu-id="cedcb-153">**Tip:** To move a parent license plate, you must use a mobile device that is configured to create work for movements.</span></span> |
| <span data-ttu-id="cedcb-154">牌照分隔符</span><span class="sxs-lookup"><span data-stu-id="cedcb-154">License plate break</span></span> | <span data-ttu-id="cedcb-155">划分牌照生成，您才可以从生成中的牌照中领取物料。</span><span class="sxs-lookup"><span data-stu-id="cedcb-155">Break up a license plate build so that you can pick items from the license plates that were in the build.</span></span> |
| <span data-ttu-id="cedcb-156">驾驶员签入</span><span class="sxs-lookup"><span data-stu-id="cedcb-156">Driver check in</span></span> | <span data-ttu-id="cedcb-157">如果您正在使用“运输管理”，请通过扫描出站负载 ID、约会 ID 或者装运 ID，登记驾驶员到达。</span><span class="sxs-lookup"><span data-stu-id="cedcb-157">If you’re using Transportation management, register the arrival of a driver by scanning the outbound load ID, appointment ID, or shipment ID.</span></span> <span data-ttu-id="cedcb-158">对于此选项，负载必须分配给预约，并且负载的状态必须为 **已负载**。</span><span class="sxs-lookup"><span data-stu-id="cedcb-158">For this option, a load must be assigned to the appointment, and the status of the load must be **Loaded**.</span></span> |
| <span data-ttu-id="cedcb-159">驾驶员签出</span><span class="sxs-lookup"><span data-stu-id="cedcb-159">Driver check out</span></span> | <span data-ttu-id="cedcb-160">登记司机已完成他们的约会。</span><span class="sxs-lookup"><span data-stu-id="cedcb-160">Register that a driver has completed his or her appointment.</span></span> |
| <span data-ttu-id="cedcb-161">刷新编号规则缓存</span><span class="sxs-lookup"><span data-stu-id="cedcb-161">Flush number sequence cache</span></span> | <span data-ttu-id="cedcb-162">从数字序列缓存中删除数字序列号。</span><span class="sxs-lookup"><span data-stu-id="cedcb-162">Delete number sequence numbers from the number sequence cache.</span></span> <span data-ttu-id="cedcb-163">通常由系统管理员执行这类活动，从而在使用移动设备时解决缓存问题。</span><span class="sxs-lookup"><span data-stu-id="cedcb-163">This activity is typically performed by a system administrator to resolve caching issues when mobile devices are used.</span></span> |
| <span data-ttu-id="cedcb-164">更改批处置</span><span class="sxs-lookup"><span data-stu-id="cedcb-164">Change batch disposition</span></span> | <span data-ttu-id="cedcb-165">允许工作人员指定物料或批次的批处置代码。</span><span class="sxs-lookup"><span data-stu-id="cedcb-165">Allow a worker to specify a batch disposition code for an item and batch.</span></span> <span data-ttu-id="cedcb-166">这种选择将更新指定给批次的处置代码。</span><span class="sxs-lookup"><span data-stu-id="cedcb-166">This selection updates the disposition code that is specified for the batch.</span></span> |
| <span data-ttu-id="cedcb-167">显示未结工作列表</span><span class="sxs-lookup"><span data-stu-id="cedcb-167">Display open work list</span></span> | <span data-ttu-id="cedcb-168">显示可用的工作列表给特定用户。</span><span class="sxs-lookup"><span data-stu-id="cedcb-168">Show a list of available work to a particular user.</span></span> <span data-ttu-id="cedcb-169">用户可以选择要执行的工作和并将被定向到它。</span><span class="sxs-lookup"><span data-stu-id="cedcb-169">The user can then select work to perform and will be directed to it.</span></span> <span data-ttu-id="cedcb-170">应在具有尺寸为 7 英寸或更大尺寸的屏幕的平板设备上查看此列表。</span><span class="sxs-lookup"><span data-stu-id="cedcb-170">This list is intended to be viewed on tablet devices that have a screen size of 7 inches or more.</span></span> <span data-ttu-id="cedcb-171">当您选择此选项时，**编辑查询** 和 **字段列表** 菜单项将可用。</span><span class="sxs-lookup"><span data-stu-id="cedcb-171">When you select this option, the **Edit query** and **Field list** menu items become available.</span></span> <span data-ttu-id="cedcb-172">**编辑查询** 页允许您设置显示在列表中的工作的条件。</span><span class="sxs-lookup"><span data-stu-id="cedcb-172">The **Edit query** page lets you set up criteria for the work that appears in the list.</span></span> <span data-ttu-id="cedcb-173">**字段列表** 页允许您选择哪些字段显示在工作列表中。</span><span class="sxs-lookup"><span data-stu-id="cedcb-173">The **Field list** page lets you select what fields appear in the work list.</span></span> <span data-ttu-id="cedcb-174">例如，您可以减少显示的字段数量，以便用户可以更快速地选择最合适的工作项。</span><span class="sxs-lookup"><span data-stu-id="cedcb-174">For example, you can reduce the number of fields that appear, so that the user can more quickly select the most appropriate work item.</span></span> <span data-ttu-id="cedcb-175">在 **常规** 快速选项卡的 **每页记录数** 字段中，您还可以选择每页显示多少条工作记录。</span><span class="sxs-lookup"><span data-stu-id="cedcb-175">On the **General** FastTab, in the **Records per page** field, you can also select how many work records are shown per page.</span></span> <span data-ttu-id="cedcb-176">如果选中了 **允许用户按交易记录类型筛选工作** 选项，工作列表将包含 **筛选工作** 控制，用户可使用它来按交易记录类型筛选。</span><span class="sxs-lookup"><span data-stu-id="cedcb-176">If the **Allow users to filter work by transaction type** option is selected, the work list will include a **Filter work** control that the user can use to filter by transaction type.</span></span> <span data-ttu-id="cedcb-177">在工作列表中，用户只能看到他们有访问权限的工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-177">In the work list, users will see only work that they have permission to access.</span></span> <span data-ttu-id="cedcb-178">您必须确保用户具有一个或多个以用户为导向的菜单项的权限，这些菜单项支持他们应有权访问的特定工作类类型。</span><span class="sxs-lookup"><span data-stu-id="cedcb-178">You must make sure that users have permission for one or more user-directed menu items that support the specific work class types that they should be able to access.</span></span> <span data-ttu-id="cedcb-179">当用户试图执行列表中的工作时，也将验证权限。</span><span class="sxs-lookup"><span data-stu-id="cedcb-179">Permissions are verified when a user tries to perform work from the list.</span></span>|
| <span data-ttu-id="cedcb-180">从牌照创建转移单</span><span class="sxs-lookup"><span data-stu-id="cedcb-180">Create transfer order from license plates</span></span> | <span data-ttu-id="cedcb-181">允许仓库工作人员直接通过仓库应用创建和处理转移单。</span><span class="sxs-lookup"><span data-stu-id="cedcb-181">Allows warehouse workers create and process transfer orders directly from the warehouse app.</span></span> <span data-ttu-id="cedcb-182">仓库工作人员首先选择目标仓库，然后可以使用应用扫描一个或多个牌照。</span><span class="sxs-lookup"><span data-stu-id="cedcb-182">The warehouse workers start by selecting the destination warehouse and can then scan one or more license plates using the app.</span></span> <span data-ttu-id="cedcb-183">当仓库工作人员选择 **完成订单** 时，批处理作业将根据为这些牌照登记的现有库存创建所需的转移单和订单行。</span><span class="sxs-lookup"><span data-stu-id="cedcb-183">When the warehouse worker selects **Complete order**, a batch job will create the required transfer order and order lines based on the on-hand inventory registered for those license plates.</span></span> <span data-ttu-id="cedcb-184">有关详细信息，请参阅[通过仓库应用创建转移单](create-transfer-order-from-warehouse-app.md)</span><span class="sxs-lookup"><span data-stu-id="cedcb-184">For more information, see [Create transfer orders from the warehouse app](create-transfer-order-from-warehouse-app.md)</span></span>


## <a name="configure-menu-items-to-create-work-for-another-worker-or-process"></a><span data-ttu-id="cedcb-185">配置菜单项，从而为其他的工作人员或流程创建工作</span><span class="sxs-lookup"><span data-stu-id="cedcb-185">Configure menu items to create work for another worker or process</span></span>
<span data-ttu-id="cedcb-186">在移动设备上执行初始化操作之后，您可以设置菜单项，从而为另一工作人员创建工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-186">You can set up a menu item that creates work for another worker after an initial action is performed on the mobile device.</span></span> <span data-ttu-id="cedcb-187">例如，当一名工作人员使用移动设备接收物料时，可以为另外一名工作人员创建入库工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-187">For example, when one worker uses a mobile device to receive an item, put-away work is created for another worker.</span></span> <span data-ttu-id="cedcb-188">若要设置创建工作的菜单项，在 **移动设备菜单项** 页上，在 **模式** 字段中，选择 **工作**。</span><span class="sxs-lookup"><span data-stu-id="cedcb-188">To set up a menu item that creates work, on the **Mobile device menu items** page, in the **Mode** field, select **Work**.</span></span> <span data-ttu-id="cedcb-189">在下表中，**工作创建流程** 字段中的选项按工作订单类型排列。</span><span class="sxs-lookup"><span data-stu-id="cedcb-189">In the following table, the options in the **Work creation process** field are arranged by work order type.</span></span>


<table>
<tbody>
<tr>
<th><span data-ttu-id="cedcb-190">工作订单类型</span><span class="sxs-lookup"><span data-stu-id="cedcb-190">Work order type</span></span></th>
<th><span data-ttu-id="cedcb-191">选项</span><span class="sxs-lookup"><span data-stu-id="cedcb-191">Option</span></span></th>
<th><span data-ttu-id="cedcb-192">描述</span><span class="sxs-lookup"><span data-stu-id="cedcb-192">Description</span></span></th>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="cedcb-193">采购订单</span><span class="sxs-lookup"><span data-stu-id="cedcb-193">Purchase order</span></span></td>
<td><span data-ttu-id="cedcb-194">采购订单行接收</span><span class="sxs-lookup"><span data-stu-id="cedcb-194">Purchase order line receiving</span></span></td>
<td><span data-ttu-id="cedcb-195">通过使用采购订单号或采购订单行号来登记收货物料的数量，并为另个工作人员创建入库工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-195">Register the receipt of a quantity of an item by using the purchase order number and purchase order line number, and create put-away work for another worker.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-196">采购订单行接收和储存</span><span class="sxs-lookup"><span data-stu-id="cedcb-196">Purchase order line receiving and put away</span></span></td>
<td><span data-ttu-id="cedcb-197">通过使用采购订单号或采购订单行号来登记收货物料的数量，并将物料入库。</span><span class="sxs-lookup"><span data-stu-id="cedcb-197">Register the receipt of a quantity of an item by using the purchase order number and purchase order line number, and put the items away.</span></span> <span data-ttu-id="cedcb-198">同一个工作人员执行两项操作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-198">The same worker performs both actions.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-199">采购订单物料接收</span><span class="sxs-lookup"><span data-stu-id="cedcb-199">Purchase order item receiving</span></span></td>
<td><span data-ttu-id="cedcb-200">通过登记采购订单号或物料编号来登记采购订单的收货物料的数量，并为另个工作人员创建入库工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-200">Register the receipt of a quantity of an item for a purchase order by registering the purchase order number and item number, and create put-away work for another worker.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-201">采购订单物料接收和储存</span><span class="sxs-lookup"><span data-stu-id="cedcb-201">Purchase order item receiving and put away</span></span></td>
<td><span data-ttu-id="cedcb-202">通过登记采购订单编号登记采购订单的收货物料数量，并将物料入库。</span><span class="sxs-lookup"><span data-stu-id="cedcb-202">Register the receipt of a quantity of an item for a purchase order by registering the purchase order number, and put the item away.</span></span> <span data-ttu-id="cedcb-203">同一个工作人员执行两项操作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-203">The same worker performs both actions.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-204">牌照接收</span><span class="sxs-lookup"><span data-stu-id="cedcb-204">License plate receiving</span></span></td>
<td><span data-ttu-id="cedcb-205">通过使用牌照 ID 接收入站发货通知 (ASN)。</span><span class="sxs-lookup"><span data-stu-id="cedcb-205">Receive an inbound advance ship notice (ASN) by using the license plate ID.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-206">牌照接收和储存</span><span class="sxs-lookup"><span data-stu-id="cedcb-206">License plate receiving and put away</span></span></td>
<td><span data-ttu-id="cedcb-207">通过使用牌照 ID 接收和储存入站发货通知 (ASN)。</span><span class="sxs-lookup"><span data-stu-id="cedcb-207">Receive and put away an inbound advance ship notice (ASN) by using the license plate ID.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-208">加载物料接收</span><span class="sxs-lookup"><span data-stu-id="cedcb-208">Load item receiving</span></span></td>
<td><span data-ttu-id="cedcb-209">通过使用负载 ID 来登记收货的负载数量，并创建另一名工作人员的入库工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-209">Register the receipt of a quantity for a load by using the load ID, and create put-away work for another worker.</span></span> <span data-ttu-id="cedcb-210">物料编号和产品维度与接收的采购订单行相匹配。</span><span class="sxs-lookup"><span data-stu-id="cedcb-210">The item number and product dimensions match the receipt to the purchase order lines.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-211">加载物料接收和储存</span><span class="sxs-lookup"><span data-stu-id="cedcb-211">Load item receiving and put away</span></span></td>
<td><span data-ttu-id="cedcb-212">通过使用负载 ID 来登记接接收负载，并将物料入库。</span><span class="sxs-lookup"><span data-stu-id="cedcb-212">Register the receipt of a load by using the load ID, and put the items away.</span></span> <span data-ttu-id="cedcb-213">物料编号和产品维度与接收的采购订单行相匹配。</span><span class="sxs-lookup"><span data-stu-id="cedcb-213">The item number and product dimensions match the receipt to the purchase order lines.</span></span> <span data-ttu-id="cedcb-214">同一个工作人员执行两项操作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-214">The same worker performs both actions.</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cedcb-215">退货单</span><span class="sxs-lookup"><span data-stu-id="cedcb-215">Return order</span></span></td>
<td><span data-ttu-id="cedcb-216">正在接收退货单</span><span class="sxs-lookup"><span data-stu-id="cedcb-216">Return order receiving</span></span></td>
<td><span data-ttu-id="cedcb-217">通过登记 RMA 编号来登记收货的物料数量，并创建另一名工作人员的入库工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-217">Register the receipt of a quantity of an item by registering the RMA number, and create put-away work for another worker.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-218">退货单接收和储存</span><span class="sxs-lookup"><span data-stu-id="cedcb-218">Return order receiving and put away</span></span></td>
<td><span data-ttu-id="cedcb-219">通过登记 RMA 编号来登记收货的物料数量，并将物料入库。</span><span class="sxs-lookup"><span data-stu-id="cedcb-219">Register the receipt of a quantity of an item by registering the RMA number, and put the items away.</span></span> <span data-ttu-id="cedcb-220">同一个工作人员执行两项操作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-220">The same worker performs both actions.</span></span></td>
</tr>
<tr>
<td rowspan="6"><span data-ttu-id="cedcb-221">转移单</span><span class="sxs-lookup"><span data-stu-id="cedcb-221">Transfer order</span></span></td>
<td><span data-ttu-id="cedcb-222">转移单物料接收</span><span class="sxs-lookup"><span data-stu-id="cedcb-222">Transfer order item receiving</span></span></td>
<td><span data-ttu-id="cedcb-223">登记收货的物料数量，并创建另一名工作人员的入库工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-223">Register the receipt of a quantity of an item, and create put-away work for another worker.</span></span>

<span data-ttu-id="cedcb-224"><strong>注意：</strong>只有在从一个仓库装运物料时才能使用此选项，这在仓库管理流程中无法启用。</span><span class="sxs-lookup"><span data-stu-id="cedcb-224"><strong>Note:</strong> Use this option only if the items were shipped from a warehouse that isn't enabled for warehouse management processes.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-225">转移单物料接收和储存</span><span class="sxs-lookup"><span data-stu-id="cedcb-225">Transfer order item receiving and put away</span></span></td>
<td><span data-ttu-id="cedcb-226">登记收货的物料数量，并将物料入库。</span><span class="sxs-lookup"><span data-stu-id="cedcb-226">Register the receipt of a quantity of an item, and put the items away.</span></span> <span data-ttu-id="cedcb-227">同一个工作人员执行两项操作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-227">The same worker performs both actions.</span></span>

<span data-ttu-id="cedcb-228"><strong>注意：</strong>只有在从一个仓库装运物料时才能使用此选项，这在仓库管理流程中无法启用。</span><span class="sxs-lookup"><span data-stu-id="cedcb-228"><strong>Note:</strong> Use this option only if the items were shipped from a warehouse that isn't enabled for warehouse management processes.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-229">转移单行接收</span><span class="sxs-lookup"><span data-stu-id="cedcb-229">Transfer order line receiving</span></span></td>
<td><span data-ttu-id="cedcb-230">登记收货的物料数量，并创建另一名工作人员的入库工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-230">Register the receipt of a quantity of an item, and create put-away work for another worker.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-231">转移订单行接收和储存</span><span class="sxs-lookup"><span data-stu-id="cedcb-231">Transfer order line receiving and put away</span></span></td>
<td><span data-ttu-id="cedcb-232">登记收货的物料数量，并将物料入库。</span><span class="sxs-lookup"><span data-stu-id="cedcb-232">Register the receipt of a quantity of an item, and put the items away.</span></span> <span data-ttu-id="cedcb-233">同一个工作人员执行两项操作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-233">The same worker performs both actions.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-234">牌照接收</span><span class="sxs-lookup"><span data-stu-id="cedcb-234">License plate receiving</span></span></td>
<td><span data-ttu-id="cedcb-235">通过使用牌照 ID 接收入站发货通知 (ASN)。</span><span class="sxs-lookup"><span data-stu-id="cedcb-235">Receive an inbound advance ship notice (ASN) by using the license plate ID.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-236">牌照接收和储存</span><span class="sxs-lookup"><span data-stu-id="cedcb-236">License plate receiving and put away</span></span></td>
<td><span data-ttu-id="cedcb-237">通过使用牌照 ID 接收和储存入站发货通知 (ASN)。</span><span class="sxs-lookup"><span data-stu-id="cedcb-237">Receive and put away an inbound advance ship notice (ASN) by using the license plate ID.</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="cedcb-238">生产</span><span class="sxs-lookup"><span data-stu-id="cedcb-238">Production</span></span></td>
<td><span data-ttu-id="cedcb-239">完工入库</span><span class="sxs-lookup"><span data-stu-id="cedcb-239">Report as finished</span></span></td>
<td><span data-ttu-id="cedcb-240">登记已完工的成品数量，并为另一个工作人员创建入库工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-240">Register a quantity of a finished item that has been finished for a production, and create put-away work for another worker.</span></span> <span data-ttu-id="cedcb-241">这一数量包括预期生产的部分或全部产品。</span><span class="sxs-lookup"><span data-stu-id="cedcb-241">The quantity can be some or all of the quantity that was planned for production.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-242">完工入库并储存</span><span class="sxs-lookup"><span data-stu-id="cedcb-242">Report as finished and put away</span></span></td>
<td><span data-ttu-id="cedcb-243">登记已完工的成品数量，并将物料入库。</span><span class="sxs-lookup"><span data-stu-id="cedcb-243">Register a quantity of a finished item that has been finished for a production, and put the items away.</span></span> <span data-ttu-id="cedcb-244">这一数量包括预期生产的部分或全部产品。</span><span class="sxs-lookup"><span data-stu-id="cedcb-244">The quantity can be some or all of the quantity that was planned for production.</span></span> <span data-ttu-id="cedcb-245">同一个工作人员执行两项操作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-245">The same worker performs both actions.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-246">看板</span><span class="sxs-lookup"><span data-stu-id="cedcb-246">Kanban</span></span></td>
<td><span data-ttu-id="cedcb-247">说明看板已经完成，并创建另外一名工作人员的入库工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-247">Indicate that a kanban is completed, and create put-away work for another worker.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-248">看板储存</span><span class="sxs-lookup"><span data-stu-id="cedcb-248">Kanban put away</span></span></td>
<td><span data-ttu-id="cedcb-249">说明看板已经完成，并将物料入库。</span><span class="sxs-lookup"><span data-stu-id="cedcb-249">Indicate that a kanban is completed, and put away the items.</span></span> <span data-ttu-id="cedcb-250">同一个工作人员执行两项操作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-250">The same worker performs both actions.</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="cedcb-251">库存</span><span class="sxs-lookup"><span data-stu-id="cedcb-251">Inventory</span></span></td>
<td><span data-ttu-id="cedcb-252">移动</span><span class="sxs-lookup"><span data-stu-id="cedcb-252">Movement</span></span></td>
<td><span data-ttu-id="cedcb-253">登记物料从一个位置移动到另一个位置。</span><span class="sxs-lookup"><span data-stu-id="cedcb-253">Register that items have been moved from one location to another.</span></span> <span data-ttu-id="cedcb-254">工作人员详细说明物料移来的位置，以及要移动到的位置。</span><span class="sxs-lookup"><span data-stu-id="cedcb-254">The worker specifies the location that the items are moved from and where they are moved to.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-255">检验</span><span class="sxs-lookup"><span data-stu-id="cedcb-255">Quarantine</span></span></td>
<td><span data-ttu-id="cedcb-256">更改牌照现有库存的状态或者不提供已损坏或丢失库存物料的位置。</span><span class="sxs-lookup"><span data-stu-id="cedcb-256">Change the status of the on-hand inventory for a license plate or location to make damaged or missing inventory items unavailable.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-257">根据模板变动</span><span class="sxs-lookup"><span data-stu-id="cedcb-257">Movement by template</span></span></td>
<td><span data-ttu-id="cedcb-258">以半自动的方式将物料从一个位置移动到另一个位置。</span><span class="sxs-lookup"><span data-stu-id="cedcb-258">Move items from one location to another in a semi-automated manner.</span></span> <span data-ttu-id="cedcb-259">工作人员选择移动物料的起始位置，并且系统使用位置指令来确定物料要移动到的位置。</span><span class="sxs-lookup"><span data-stu-id="cedcb-259">The worker selects the location to move items from, the system uses the location directive to determine where to move the items to.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-260">仓库转移</span><span class="sxs-lookup"><span data-stu-id="cedcb-260">Warehouse transfer</span></span></td>
<td><span data-ttu-id="cedcb-261">登记物料从一个仓库移动到另一个仓库。</span><span class="sxs-lookup"><span data-stu-id="cedcb-261">Register that items have been transferred from one warehouse to another.</span></span> <span data-ttu-id="cedcb-262">此选项要求工作人员可以执行两个仓库的工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-262">This option requires that the worker be allowed to perform work in both warehouses.</span></span>

<span data-ttu-id="cedcb-263"><strong>注意：</strong>此菜单项需要默认的库存转移日记帐，其<strong>凭证签发</strong>字段需要设置为<strong>过帐</strong>。</span><span class="sxs-lookup"><span data-stu-id="cedcb-263"><strong>Note:</strong> This menu item requires a default inventory transfer journal where the <strong>Voucher draw</strong> field is set to <strong>Posting</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-264">牌照加载</span><span class="sxs-lookup"><span data-stu-id="cedcb-264">License plate loading</span></span></td>
<td><span data-ttu-id="cedcb-265">当您第一次设置仓库时，使用此选项。</span><span class="sxs-lookup"><span data-stu-id="cedcb-265">Use this option when you&#39;re setting up your warehouse for the first time.</span></span> <span data-ttu-id="cedcb-266">扫描仓库中所有位置的牌照。</span><span class="sxs-lookup"><span data-stu-id="cedcb-266">Scan all the license plates in all locations in the warehouse.</span></span> <span data-ttu-id="cedcb-267">位置必须是受牌照的控制。</span><span class="sxs-lookup"><span data-stu-id="cedcb-267">The locations must be license plate–controlled.</span></span> <span data-ttu-id="cedcb-268">如果<strong>序列号</strong>或<strong>批号</strong>在库存预留层次结构的上述<strong>库位</strong>中列出，将不能使用此选项。</span><span class="sxs-lookup"><span data-stu-id="cedcb-268">You can&#39;t use this option if <strong>Serial number</strong> or <strong>Batch number</strong> is listed above <strong>Location</strong> in the inventory reservation hierarchy.</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cedcb-269">周期盘点</span><span class="sxs-lookup"><span data-stu-id="cedcb-269">Cycle count</span></span></td>
<td><span data-ttu-id="cedcb-270">调入</span><span class="sxs-lookup"><span data-stu-id="cedcb-270">Adjustment in</span></span></td>
<td><span data-ttu-id="cedcb-271">增加库存中物料的数量。</span><span class="sxs-lookup"><span data-stu-id="cedcb-271">Increase the quantity of items in inventory.</span></span> <span data-ttu-id="cedcb-272">指定位置、牌照、物料、数量、度量单位和状态。</span><span class="sxs-lookup"><span data-stu-id="cedcb-272">Specify the location, license plate, item, quantity, unit of measure, and status.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-273">调出</span><span class="sxs-lookup"><span data-stu-id="cedcb-273">Adjustment out</span></span></td>
<td><span data-ttu-id="cedcb-274">减少库存中物料的数量。</span><span class="sxs-lookup"><span data-stu-id="cedcb-274">Reduce the quantity of items in inventory.</span></span> <span data-ttu-id="cedcb-275">指定位置、牌照、物料、数量、度量单位和库存状态。</span><span class="sxs-lookup"><span data-stu-id="cedcb-275">Specify the location, license plate, item, quantity, unit of measure, and status of the inventory.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cedcb-276">现货周期盘点</span><span class="sxs-lookup"><span data-stu-id="cedcb-276">Spot cycle counting</span></span></td>
<td><span data-ttu-id="cedcb-277">开始位置盘点。</span><span class="sxs-lookup"><span data-stu-id="cedcb-277">Start a count for a location.</span></span> <span data-ttu-id="cedcb-278">工作人员必须盘点一个位置的所有物料。</span><span class="sxs-lookup"><span data-stu-id="cedcb-278">The worker must count all items in the location.</span></span> <span data-ttu-id="cedcb-279">如果盘点的结果少于预期数量，缺失的数量将视为损失。</span><span class="sxs-lookup"><span data-stu-id="cedcb-279">When the result of a count is less than the expected quantity, the missing quantity is considered a loss.</span></span></td>
</tr>
</tbody>
</table>

## <a name="configure-menu-items-to-process-existing-work"></a><span data-ttu-id="cedcb-280">配置菜单项以处理现有的工作</span><span class="sxs-lookup"><span data-stu-id="cedcb-280">Configure menu items to process existing work</span></span>
<span data-ttu-id="cedcb-281">除了设置菜单项以创建仓库工作之外，您还可以设置菜单项来处理已创建的工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-281">In addition to setting up menu items to create warehouse work, you can set up menu items to process work that has already been created.</span></span> <span data-ttu-id="cedcb-282">设置 **模式** 字段为 **工作**，然后选择 **使用现有工作** 选项。</span><span class="sxs-lookup"><span data-stu-id="cedcb-282">Set the **Mode** field to **Work**, and select the **Use existing work** option.</span></span> <span data-ttu-id="cedcb-283">这些附加选项随后会显示在 **常规** 选项卡中。您可以通过在 **工作类** 快速选项卡上分配一个或多个工作类来控制对菜单项的访问。</span><span class="sxs-lookup"><span data-stu-id="cedcb-283">Some additional options then become available on the **General** tab. You can control access to the menu item by assigning one or more work classes on the **Work class** FastTab.</span></span> <span data-ttu-id="cedcb-284">工作类定义菜单项可处理的工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-284">The work classes define the work that the menu item can process.</span></span> <span data-ttu-id="cedcb-285">工作类还可用于授予访问权限给特定用户角色或给不同工序类型的单独处理。</span><span class="sxs-lookup"><span data-stu-id="cedcb-285">The work class can also be used to grant access to specific user roles or to separate processing for different types of operations.</span></span> <span data-ttu-id="cedcb-286">下表说明可用的选项。</span><span class="sxs-lookup"><span data-stu-id="cedcb-286">The following table describes the options that are available.</span></span> <span data-ttu-id="cedcb-287">可以在 **移动设备菜单项** 页中 **主管** 字段下选择此选项。</span><span class="sxs-lookup"><span data-stu-id="cedcb-287">The option can be chosen under the **Directed by** field in the **Mobile device menu items** page.</span></span> 

<table>




<thead>
<tr class="header">
<th><span data-ttu-id="cedcb-288">选项</span><span class="sxs-lookup"><span data-stu-id="cedcb-288">Option</span></span></th>
<th><span data-ttu-id="cedcb-289">说明</span><span class="sxs-lookup"><span data-stu-id="cedcb-289">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cedcb-290">无</span><span class="sxs-lookup"><span data-stu-id="cedcb-290">None</span></span></td>
<td><span data-ttu-id="cedcb-291">此默认值无法处理工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-291">This default value doesn&#39;t process work.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cedcb-292">系统导向的</span><span class="sxs-lookup"><span data-stu-id="cedcb-292">System directed</span></span></td>
<td><span data-ttu-id="cedcb-293">Supply Chain Management 控制分配给工作人员的工作类型，以及工作人员执行该工作的顺序。</span><span class="sxs-lookup"><span data-stu-id="cedcb-293">Supply Chain Management controls the type of work that is assigned to a worker and the order that the worker performs the work in.</span></span> <span data-ttu-id="cedcb-294">当您选择此选项时，您可以选择“操作”窗格上的<strong>系统导向的工作</strong>来打开<strong>系统导向的排序顺序</strong>页面，您可以在其中设置该工作的排序条件。</span><span class="sxs-lookup"><span data-stu-id="cedcb-294">When you select this option, you can sekect <strong>System-directed work</strong> on the Action Pane to open the <strong>System-directed sorting order</strong> page, where you can set up sorting criteria for the work.</span></span> <span data-ttu-id="cedcb-295">排序条件控制工作人员执行工作的顺序。</span><span class="sxs-lookup"><span data-stu-id="cedcb-295">The sorting criteria control the order that the worker performs the work in.</span></span> <span data-ttu-id="cedcb-296">您可以根据需要添加任意数目的条件。</span><span class="sxs-lookup"><span data-stu-id="cedcb-296">You can add as many criteria as you require.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cedcb-297">用户导向的</span><span class="sxs-lookup"><span data-stu-id="cedcb-297">User directed</span></span></td>
<td><span data-ttu-id="cedcb-298">工作人员选择执行的工作以及执行的顺序。</span><span class="sxs-lookup"><span data-stu-id="cedcb-298">The worker selects the work to perform and the order to perform it in.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cedcb-299">用户分组</span><span class="sxs-lookup"><span data-stu-id="cedcb-299">User grouping</span></span></td>
<td><span data-ttu-id="cedcb-300">工作人员可手动对工作分组。</span><span class="sxs-lookup"><span data-stu-id="cedcb-300">The worker manually groups work.</span></span> <span data-ttu-id="cedcb-301">例如，当一名工作人员同时在同一位置选择多个物料时，此选项很有用。</span><span class="sxs-lookup"><span data-stu-id="cedcb-301">This option is useful when, for example, a worker can pick multiple items at the same time in a location.</span></span> <span data-ttu-id="cedcb-302">当工作人员完成所需领料后，他或她可将物料入库。</span><span class="sxs-lookup"><span data-stu-id="cedcb-302">After the worker has finished picking all the required items, he or she can put the items away.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cedcb-303">系统分组</span><span class="sxs-lookup"><span data-stu-id="cedcb-303">System grouping</span></span></td>
<td><span data-ttu-id="cedcb-304">Supply Chain Management 根据指定的字段为工作人员进行工作分组。</span><span class="sxs-lookup"><span data-stu-id="cedcb-304">Supply Chain Management groups work for the worker, based on a specified field.</span></span> <span data-ttu-id="cedcb-305">例如，当工作人员扫描装运 ID、负载 ID 或者与每个工作单位链接的任何值时，分组领料工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-305">For example, picking work is grouped when a worker scans a shipment ID, load ID, or any value that can link each work unit.</span></span> <span data-ttu-id="cedcb-306">如果您选择此选项，需要下列字段：</span><span class="sxs-lookup"><span data-stu-id="cedcb-306">If you select this option, the following fields are required:</span></span>
<ul>
<li><span data-ttu-id="cedcb-307"><strong>系统分组字段</strong> - 选择工作人员需要用来扫描以分组工作的字段。</span><span class="sxs-lookup"><span data-stu-id="cedcb-307"><strong>System grouping field</strong> – Select the field that the worker scans to group the work.</span></span></li>
<li><span data-ttu-id="cedcb-308"><strong>系统分组标签</strong> - 输入文本，通知工作人员需要扫描哪些内容，才能将工作分组。</span><span class="sxs-lookup"><span data-stu-id="cedcb-308"><strong>System grouping label</strong> – Enter text to instruct the worker what to scan to group the work.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cedcb-309">已验证用户导向的</span><span class="sxs-lookup"><span data-stu-id="cedcb-309">Validated user directed</span></span></td>
<td><span data-ttu-id="cedcb-310">当工作与较大的实体（如负载或装运）有关联时，工作人员选择执行的工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-310">The worker selects the work to perform when work is associated with a larger entity, such as a load or shipment.</span></span> <span data-ttu-id="cedcb-311">工作人员确定物料领料的顺序。</span><span class="sxs-lookup"><span data-stu-id="cedcb-311">The worker determines the order that the items are picked in.</span></span> <span data-ttu-id="cedcb-312">如果您选择此选项，需要下列字段：</span><span class="sxs-lookup"><span data-stu-id="cedcb-312">If you select this option, the following fields are required:</span></span>
<ul>
<li><span data-ttu-id="cedcb-313"><strong>已验证用户导向的字段</strong> - 选择工作人员需要用来扫描以分组工作的字段。</span><span class="sxs-lookup"><span data-stu-id="cedcb-313"><strong>Validated user directed field</strong> – Select the field that the worker scans to group the work.</span></span></li>
<li><span data-ttu-id="cedcb-314"><strong>已验证用户导向的标签</strong> – 当领料工作是由系统分组时，输入文本告知工作人员需要扫描的内容。</span><span class="sxs-lookup"><span data-stu-id="cedcb-314"><strong>Validated user directed label</strong> – Enter text that instructs the worker what to scan when picking work is grouped by the system.</span></span></li>
</ul>
<span data-ttu-id="cedcb-315">例如，当多个托盘用于承载一个负载时，此选项很有用。</span><span class="sxs-lookup"><span data-stu-id="cedcb-315">This option is useful when, for example, multiple pallets are staged for a load.</span></span> <span data-ttu-id="cedcb-316">如果您在<strong>已验证用户导向的</strong>字段中选择 <strong>LoadId</strong>，工作人员可以领取与负载相关的任何托盘。</span><span class="sxs-lookup"><span data-stu-id="cedcb-316">If you select <strong>LoadId</strong> in the <strong>Validated User Directed</strong> field, the worker can pick any pallet that is associated with the load.</span></span> <span data-ttu-id="cedcb-317">如果工作人员扫描与负载没有关联的物料时，工作人员将收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="cedcb-317">The worker receives an error message if he or she scans an item that isn&#39;t associated with the load.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cedcb-318">群集领料</span><span class="sxs-lookup"><span data-stu-id="cedcb-318">Cluster picking</span></span></td>
<td><span data-ttu-id="cedcb-319">工作人员将工作分组成群集。</span><span class="sxs-lookup"><span data-stu-id="cedcb-319">The worker groups work into clusters.</span></span> <span data-ttu-id="cedcb-320">群集允许工作人员同时根据多个工作指令从单个位置领料。</span><span class="sxs-lookup"><span data-stu-id="cedcb-320">Clusters lets workers pick items from a single location for multiple work orders at the same time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cedcb-321">周期盘点分组</span><span class="sxs-lookup"><span data-stu-id="cedcb-321">Cycle count grouping</span></span></td>
<td><span data-ttu-id="cedcb-322">工作人员选择一个区域、工作池或地点，Supply Chain Management 将根据选择情况分配工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-322">The worker selects a zone, work pool, or location, and Supply Chain Management assigns work, based on the selection.</span></span> <span data-ttu-id="cedcb-323">如果您选择此选项，则可以单击操作窗格上的<strong>周期盘点</strong>，指定要显示的其他信息，您还可以指定在发现任何差异的情况下，工作人员需要重复盘点的次数。</span><span class="sxs-lookup"><span data-stu-id="cedcb-323">If you select this option, you can click <strong>Cycle counting</strong> on the Action Pane to specify additional information to display, and you can also specify the number of times that the worker must repeat the count if a difference is found.</span></span></td>
</tr>
 <tr class="odd">
<td><span data-ttu-id="cedcb-324">运输装载</span><span class="sxs-lookup"><span data-stu-id="cedcb-324">Transport loading</span></span></td>
<td><span data-ttu-id="cedcb-325">通过此功能，多位仓库工作人员可从相同或不同负荷将库存装载到装有已完全或部分装运的负荷的同一辆卡车上。</span><span class="sxs-lookup"><span data-stu-id="cedcb-325">This feature allows several warehouse workers to load inventory from the same or different loads onto the same truck, with loads that are fully or partially shipped.</span></span></td>
</tr>
</tbody>
</table>

## <a name="additional-menu-item-options"></a><span data-ttu-id="cedcb-326">附加菜单项选项</span><span class="sxs-lookup"><span data-stu-id="cedcb-326">Additional menu item options</span></span>
<span data-ttu-id="cedcb-327">其他菜单项选项在 **移动设备菜单项** 页可用。</span><span class="sxs-lookup"><span data-stu-id="cedcb-327">Additional menu items options are available on the **Mobile device menu items** page.</span></span> <span data-ttu-id="cedcb-328">选项根据您为其配置菜单项的流程而变化。</span><span class="sxs-lookup"><span data-stu-id="cedcb-328">The options vary, depending on the process that you’re configuring the menu item for.</span></span> 

<span data-ttu-id="cedcb-329">下表描述这些选项。</span><span class="sxs-lookup"><span data-stu-id="cedcb-329">The following table describes these options.</span></span>

<table>




<thead>
<tr class="header">
<th><span data-ttu-id="cedcb-330">字段</span><span class="sxs-lookup"><span data-stu-id="cedcb-330">Field</span></span></th>
<th><span data-ttu-id="cedcb-331">描述</span><span class="sxs-lookup"><span data-stu-id="cedcb-331">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cedcb-332">允许拆分工作</span><span class="sxs-lookup"><span data-stu-id="cedcb-332">Allow splitting of work</span></span></td>
<td><span data-ttu-id="cedcb-333">选择此选项可允许用户将工作指令项输入到多个目标牌照中。</span><span class="sxs-lookup"><span data-stu-id="cedcb-333">Select this option to let users put items for a work order into more than one target license plate.</span></span> <span data-ttu-id="cedcb-334">此选项很有用，例如，当一个目标牌照已满时，工作人员必须将剩余的物料添加到另一个牌照中。</span><span class="sxs-lookup"><span data-stu-id="cedcb-334">This option is useful when, for example, a target license plate is full, and the worker must add the remaining items to another license plate.</span></span> <span data-ttu-id="cedcb-335">工作人员可以选择<strong>已满</strong>，指示牌照已满，停止接收领料工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-335">The worker can select <strong>Full</strong> to indicate that the license plate is full and stop receiving picking work for it.</span></span> <span data-ttu-id="cedcb-336">然后将显示已领物料放置的位置，已经完成的领料工作将移到一个新的工作订单中。</span><span class="sxs-lookup"><span data-stu-id="cedcb-336">The put location for the picked items is then displayed, and the picking work that has already been completed is moved to a new work order.</span></span> <span data-ttu-id="cedcb-337">目标牌照的剩余领料工作仍然在原来的工作订单中。</span><span class="sxs-lookup"><span data-stu-id="cedcb-337">The remaining picking work for the target license plate stays on the original work order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cedcb-338">定位</span><span class="sxs-lookup"><span data-stu-id="cedcb-338">Anchoring</span></span></td>
<td><span data-ttu-id="cedcb-339">选择此选项可允许工作人员指定将会覆盖推荐暂存或负荷位置的位置。</span><span class="sxs-lookup"><span data-stu-id="cedcb-339">Select this option to let workers specify a location that overrides the suggested staging or loading location.</span></span> <span data-ttu-id="cedcb-340">所有剩余的入库工作将指向新的位置。</span><span class="sxs-lookup"><span data-stu-id="cedcb-340">All the remaining put-away work is directed to the new location.</span></span> <span data-ttu-id="cedcb-341">例如，当一名工作人员无法将订单 1 的物料放置到 1 号码头的暂存位置时，此选项很有用，因为此位置未清空之前的负荷。</span><span class="sxs-lookup"><span data-stu-id="cedcb-341">This option is useful when, for example, a worker who must put items for order 1 in a staging location by Dock 1 can’t, because a previous load hasn’t cleared the location.</span></span> <span data-ttu-id="cedcb-342">工作人员可以决定使用 2 号码头的暂存位置，而不是等待 1 号码头留出可以使用的暂存位置。</span><span class="sxs-lookup"><span data-stu-id="cedcb-342">Instead of waiting for the Dock 1 staging location to become available, the worker can decide to use the staging location for Dock 2.</span></span> <span data-ttu-id="cedcb-343">在此情况下，工作人员覆盖建议的暂存位置。</span><span class="sxs-lookup"><span data-stu-id="cedcb-343">In this case, the worker overrides the suggested staging location.</span></span> <span data-ttu-id="cedcb-344">工作订单中所有剩余物料的放置位置然后将更新到 2 号码头暂存位置。</span><span class="sxs-lookup"><span data-stu-id="cedcb-344">The put location for all remaining items for the work order is then updated to the Dock 2 staging location.</span></span> <span data-ttu-id="cedcb-345">如果选择此选项，则必须设置<strong>定位者</strong>字段。</span><span class="sxs-lookup"><span data-stu-id="cedcb-345">If you select this option, you must set the <strong>Anchor by</strong> field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cedcb-346">定位者</span><span class="sxs-lookup"><span data-stu-id="cedcb-346">Anchor by</span></span></td>
<td><span data-ttu-id="cedcb-347">如果您正在使用定位，必须指定要通过装运还是负载定位。</span><span class="sxs-lookup"><span data-stu-id="cedcb-347">If you&#39;re using anchoring, you must specify whether to anchor by shipment or by load.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cedcb-348">审计模板 ID</span><span class="sxs-lookup"><span data-stu-id="cedcb-348">Audit template ID</span></span></td>
<td><span data-ttu-id="cedcb-349">选择工作审核模板，这将中断此菜单项的工作流程，以便可以执行其他操作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-349">Select the work audit template that will interrupt the work process for this menu item so that another operation can be performed.</span></span> <span data-ttu-id="cedcb-350">例如，如果一个菜单项适用于入站工作，则审核模板可能要求工作人员检查交付的集装箱内的温度。</span><span class="sxs-lookup"><span data-stu-id="cedcb-350">For example, if this menu item is for inbound work, the audit template might require that the worker check the temperature in the delivery container.</span></span> <span data-ttu-id="cedcb-351">流程中断点在审计模板指定。</span><span class="sxs-lookup"><span data-stu-id="cedcb-351">The point at which the process is interrupted is specified on the audit template.</span></span> <span data-ttu-id="cedcb-352">例如，此点可以是工作开始或已完成时，或者当更改其状态时。</span><span class="sxs-lookup"><span data-stu-id="cedcb-352">This point can be, for example, when work is started or completed, or when its status changes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cedcb-353">群集配置文件 ID</span><span class="sxs-lookup"><span data-stu-id="cedcb-353">Cluster profile ID</span></span></td>
<td><span data-ttu-id="cedcb-354">选择群集配置文件，用于群集领料。</span><span class="sxs-lookup"><span data-stu-id="cedcb-354">Select the cluster profile to use for cluster picking.</span></span> <span data-ttu-id="cedcb-355">群集配置文件包括设置，如是否自动创建群集、可以分配的职位名称和工作单位数量、何时将群集分成单个的单位以及是否需要进行验证。</span><span class="sxs-lookup"><span data-stu-id="cedcb-355">The cluster profile includes settings such as whether to create clusters automatically, the names of positions and the number of work units that they can be assigned, when to break clusters into individual units, and whether verification is required.</span></span> <span data-ttu-id="cedcb-356">仅当在<strong>主管</strong>字段中选择<strong>群集领料</strong>时，此字段才可用。</span><span class="sxs-lookup"><span data-stu-id="cedcb-356">This field is available only if <strong>Cluster picking</strong> is selected in the <strong>Directed by</strong> field.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cedcb-357">先对总物料数进行计数</span><span class="sxs-lookup"><span data-stu-id="cedcb-357">Count total item quantity first</span></span></td>
<td><span data-ttu-id="cedcb-358">选择此选项可要求工作人员在盘点期间首先盘点出总数量。</span><span class="sxs-lookup"><span data-stu-id="cedcb-358">Select this option to require that a worker count the total quantity first during a count.</span></span> <span data-ttu-id="cedcb-359">如果发现差额，工作人员必须提供其他信息，如牌照编号、批编号和序列号。</span><span class="sxs-lookup"><span data-stu-id="cedcb-359">If a difference is found, the worker must provide additional information, such as the license plate number, batch number, and serial numbers.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cedcb-360">创建移动</span><span class="sxs-lookup"><span data-stu-id="cedcb-360">Create movement</span></span></td>
<td><span data-ttu-id="cedcb-361">选择此选项，允许工作人员在不需要立即执行工作的情况下，创建移动工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-361">Select this option to let a worker create work for a movement, but without requiring that the worker perform the work immediately.</span></span> <span data-ttu-id="cedcb-362">例如，如果已经完成质量检查，并且检查人员希望物料从质量检查区域转移，那么此选项很有用。</span><span class="sxs-lookup"><span data-stu-id="cedcb-362">This option is useful if, for example, a quality inspection has been completed, and the inspector wants the item to be moved from the quality inspection area.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cedcb-363">指令代码</span><span class="sxs-lookup"><span data-stu-id="cedcb-363">Directive code</span></span></td>
<td><span data-ttu-id="cedcb-364">若要使用一个特定的位置指令，选择与位置指令相关的指令代码。</span><span class="sxs-lookup"><span data-stu-id="cedcb-364">To use a specific location directive, select the directive code that is associated the location directive.</span></span> <span data-ttu-id="cedcb-365">当您创建工作且工作创建流程为<strong>根据模板变动</strong>时，此字段可用。</span><span class="sxs-lookup"><span data-stu-id="cedcb-365">This field is available when you create work and the work creation process is <strong>Movement by template</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cedcb-366">禁用周期盘点阈值</span><span class="sxs-lookup"><span data-stu-id="cedcb-366">Disable cycle count thresholds</span></span></td>
<td><span data-ttu-id="cedcb-367">选中此选项可以忽略周期盘点阀值。</span><span class="sxs-lookup"><span data-stu-id="cedcb-367">Select this option to ignore the cycle count thresholds.</span></span> <span data-ttu-id="cedcb-368">如果您选择了此选项，当超过阀值时，无法创建周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-368">If you select this option, cycle count work isn&#39;t created when threshold values are exceeded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cedcb-369">显示批次处置代码</span><span class="sxs-lookup"><span data-stu-id="cedcb-369">Display batch disposition code</span></span></td>
<td><span data-ttu-id="cedcb-370">选择此选项可显示批处置代码。</span><span class="sxs-lookup"><span data-stu-id="cedcb-370">Select this option to display batch disposition codes.</span></span> <span data-ttu-id="cedcb-371">例如，当您接收返货批次时，可以显示批处置代码。</span><span class="sxs-lookup"><span data-stu-id="cedcb-371">For example, you can display batch disposition codes when you receive a returned batch.</span></span> <span data-ttu-id="cedcb-372">工作人员然后可以评估批次的状态或质量，并选择恰当的代码。</span><span class="sxs-lookup"><span data-stu-id="cedcb-372">Workers can then evaluate the status or quality of a batch, and select the appropriate code.</span></span> <span data-ttu-id="cedcb-373">批次处置代码规则决定了该批次是否可用于其他仓库流程。</span><span class="sxs-lookup"><span data-stu-id="cedcb-373">The rules on the batch disposition code determine whether the batch will be available to other warehouse processes.</span></span> <span data-ttu-id="cedcb-374">如果您没有选择此选项，则使用以下批次处置代码之一：</span><span class="sxs-lookup"><span data-stu-id="cedcb-374">If you don&#39;t select this option, one of the following batch disposition codes is used:</span></span>
<ul>
<li><span data-ttu-id="cedcb-375">如果您收到新的批处理号，使用物料模型组中指定的批次处置代码。</span><span class="sxs-lookup"><span data-stu-id="cedcb-375">If you receive a new batch number, the default batch disposition code that is specified on the item model group.</span></span></li>
<li><span data-ttu-id="cedcb-376">使用已经分配给该批次的批次处置代码。</span><span class="sxs-lookup"><span data-stu-id="cedcb-376">The batch disposition code that is already assigned to the batch.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cedcb-377">显示处置代码</span><span class="sxs-lookup"><span data-stu-id="cedcb-377">Display disposition code</span></span></td>
<td><span data-ttu-id="cedcb-378">选择此选项可显示处置代码。</span><span class="sxs-lookup"><span data-stu-id="cedcb-378">Select this option to display disposition codes.</span></span> <span data-ttu-id="cedcb-379">例如，当您接收退货物料时，可以显示处置代码。</span><span class="sxs-lookup"><span data-stu-id="cedcb-379">For example, you can display disposition codes when you receive return items.</span></span> <span data-ttu-id="cedcb-380">工作人员然后可以评估物料的状态或质量，并选择恰当的代码。</span><span class="sxs-lookup"><span data-stu-id="cedcb-380">Workers can then evaluate the status or quality of the items, and select the appropriate code.</span></span> <span data-ttu-id="cedcb-381">处置代码规则决定了物料是否可用于其他仓库流程。</span><span class="sxs-lookup"><span data-stu-id="cedcb-381">The rules on the disposition code determine whether the items will be available to other warehouse processes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cedcb-382">显示库存状态</span><span class="sxs-lookup"><span data-stu-id="cedcb-382">Display inventory status</span></span></td>
<td><span data-ttu-id="cedcb-383">选中此选项可以显示仓库中的物料状态。</span><span class="sxs-lookup"><span data-stu-id="cedcb-383">Select this option to display the status of items in inventory.</span></span> <span data-ttu-id="cedcb-384">除周期盘点之外，此选项可用于使用现有工作的所有菜单项。</span><span class="sxs-lookup"><span data-stu-id="cedcb-384">This option is available for all menu items that use existing work, except cycle counting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cedcb-385">显示领料屏幕的摘要</span><span class="sxs-lookup"><span data-stu-id="cedcb-385">Display summary of pick screen</span></span></td>
<td><span data-ttu-id="cedcb-386">选中此选项可以显示适用于所选工作指令的选择工作汇总。</span><span class="sxs-lookup"><span data-stu-id="cedcb-386">Select this option to display a summary of picking work for the selected work order.</span></span> <span data-ttu-id="cedcb-387">在处理工作指令的第一个工作行之前，将显示此汇总。</span><span class="sxs-lookup"><span data-stu-id="cedcb-387">The summary is displayed until the first work line is processed for the work order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cedcb-388">生成牌照</span><span class="sxs-lookup"><span data-stu-id="cedcb-388">Generate license plate</span></span></td>
<td><span data-ttu-id="cedcb-389">选中此选项可以基于序列选择生成一个独特的牌照号码。</span><span class="sxs-lookup"><span data-stu-id="cedcb-389">Select this option to generate a unique license plate number, based on the number sequence selection.</span></span> <span data-ttu-id="cedcb-390">例如，您可以生成一个适用于采购订单中收货物料的牌照号码。</span><span class="sxs-lookup"><span data-stu-id="cedcb-390">For example, you can generate a license plate number for items that are received for purchase orders.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cedcb-391">组储存</span><span class="sxs-lookup"><span data-stu-id="cedcb-391">Group put away</span></span></td>
<td><span data-ttu-id="cedcb-392">选中此选项以便对入库工作进行分组。</span><span class="sxs-lookup"><span data-stu-id="cedcb-392">Select this option to group the put-away work.</span></span> <span data-ttu-id="cedcb-393">当您创建工作且工作创建流程为 Supply Chain Management 时，此选项可用。</span><span class="sxs-lookup"><span data-stu-id="cedcb-393">This option is available when the work was grouped either by the worker or by Supply Chain Management.</span></span> <span data-ttu-id="cedcb-394">当工作人员完成组中所有的领料工作时，将创建同一组的入库工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-394">When the worker has finished all the picking work in the group, put-away work is created for the same group.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cedcb-395">库存调整类型</span><span class="sxs-lookup"><span data-stu-id="cedcb-395">Inventory adjustment types</span></span></td>
<td><span data-ttu-id="cedcb-396">选择库存调整类型，这一类型决定用于过帐调整的库存盘点日记帐，并决定是否删除预留。</span><span class="sxs-lookup"><span data-stu-id="cedcb-396">Select the inventory adjustment type that determines the inventory counting journal that is used to post the adjustment, and whether to remove reservations.</span></span> <span data-ttu-id="cedcb-397">只有用于<strong>调入</strong>或<strong>调出</strong>工作创建流程时，此字段才可用。</span><span class="sxs-lookup"><span data-stu-id="cedcb-397">This field is available only for the <strong>Adjustment in</strong> or <strong>Adjustment out</strong> work creation process.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cedcb-398">覆盖批号</span><span class="sxs-lookup"><span data-stu-id="cedcb-398">Override batch number</span></span></td>
<td><span data-ttu-id="cedcb-399">选择此选项，允许报告生产订单已完成数量的工作人员输入批号，此批号与分配给生产订单的批号不同。</span><span class="sxs-lookup"><span data-stu-id="cedcb-399">Select this option to let workers who are reporting a quantity as finished for a production order enter a batch number that differs from the batch number that is assigned to the production order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cedcb-400">覆盖目标牌照</span><span class="sxs-lookup"><span data-stu-id="cedcb-400">Override target license plate</span></span></td>
<td><span data-ttu-id="cedcb-401">选择此选项可允许工作人员指定目标牌照编号，此目标牌照编号与建议的目标牌照不同。</span><span class="sxs-lookup"><span data-stu-id="cedcb-401">Select this option to let workers specify a target license plate number that differs from the suggested target license plate.</span></span> <span data-ttu-id="cedcb-402">当工作订单上的第一个领料是牌照上某个物料的整个数量时，可使用此选项。</span><span class="sxs-lookup"><span data-stu-id="cedcb-402">Use this option when the first pick for a work order is for the entire quantity of an item on a license plate.</span></span> <span data-ttu-id="cedcb-403">例如，当重用一个托盘时，此选项很有用。</span><span class="sxs-lookup"><span data-stu-id="cedcb-403">This option is useful when, for example, a pallet is reused.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cedcb-404">领料和装箱</span><span class="sxs-lookup"><span data-stu-id="cedcb-404">Pick and pack</span></span></td>
<td><span data-ttu-id="cedcb-405">选择此选项可允许工作人员将销售订单中的工作或者负荷合并到单个工作单位中。</span><span class="sxs-lookup"><span data-stu-id="cedcb-405">Select this option to let workers combine work for a sales order or load into a single work unit.</span></span> <span data-ttu-id="cedcb-406">工作人员只可针对销售订单或负荷执行工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-406">A worker can perform work only for the sales order or load.</span></span> <span data-ttu-id="cedcb-407">例如，当为销售订单创建了装载、装运和工作之后，您必须增加销售订单数量时，此选项很有用。</span><span class="sxs-lookup"><span data-stu-id="cedcb-407">This option is useful when, for example, you must increase a quantity for a sales order after the load, shipment, and work have been created for the sales order.</span></span> <span data-ttu-id="cedcb-408">当菜单项使用现有的工作时，此选项可用，且工作由用户或系统管理。</span><span class="sxs-lookup"><span data-stu-id="cedcb-408">This option is available when the menu item uses existing work, and the work is directed by the user or system.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cedcb-409">挑选最旧的批次</span><span class="sxs-lookup"><span data-stu-id="cedcb-409">Pick oldest batch</span></span></td>
<td><span data-ttu-id="cedcb-410">指明工作人员是否必须首先选择一个位置中最早的批次。</span><span class="sxs-lookup"><span data-stu-id="cedcb-410">Indicate whether the worker must pick the oldest batch in a location first.</span></span> <span data-ttu-id="cedcb-411">选项如下：</span><span class="sxs-lookup"><span data-stu-id="cedcb-411">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="cedcb-412"><strong>无</strong> - 工作人员可以领取位置中的任何批次。</span><span class="sxs-lookup"><span data-stu-id="cedcb-412"><strong>None</strong> – The worker can pick any batch in the location.</span></span> <span data-ttu-id="cedcb-413">工作人员不会收到消息。</span><span class="sxs-lookup"><span data-stu-id="cedcb-413">The worker receives no message.</span></span></li>
<li><span data-ttu-id="cedcb-414"><strong>警告</strong> - 工作人员可领取位置中的任何批次，但如果批次不是最早的，他们将收到警告信息。</span><span class="sxs-lookup"><span data-stu-id="cedcb-414"><strong>Warn</strong> – The worker can pick any batch in the location, but he or she receives a warning message if a batch isn&#39;t the oldest batch.</span></span></li>
<li><span data-ttu-id="cedcb-415"><strong>强制</strong> - 工作人员是否必须领取位置中最早的批次。</span><span class="sxs-lookup"><span data-stu-id="cedcb-415"><strong>Force</strong> – The worker must pick the oldest batch in the location.</span></span> <span data-ttu-id="cedcb-416">如果批次不是最早的批次，工作人员将收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="cedcb-416">The worker receives an error message if a batch isn&#39;t the oldest batch.</span></span> <span data-ttu-id="cedcb-417"><strong>注意：</strong>只有当<strong>批处理号</strong>低于分配给物料的预留层次结构中的<strong>位置</strong>时，此选项才具有相关性。</span><span class="sxs-lookup"><span data-stu-id="cedcb-417"><strong>Note:</strong> This option is relevant only if <strong>Batch number</strong> is lower than <strong>Location</strong> in the reservation hierarchy that is assigned to the item.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cedcb-418">打印标签</span><span class="sxs-lookup"><span data-stu-id="cedcb-418">Print label</span></span></td>
<td><span data-ttu-id="cedcb-419">选中此选项可以允许工作人员打印牌照标签。</span><span class="sxs-lookup"><span data-stu-id="cedcb-419">Select this option to let workers print license plate labels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cedcb-420">系统分组字段</span><span class="sxs-lookup"><span data-stu-id="cedcb-420">System grouping field</span></span></td>
<td><span data-ttu-id="cedcb-421">选择决定 Supply Chain Management 如何为工作人员领料工作进行分组的字段。</span><span class="sxs-lookup"><span data-stu-id="cedcb-421">Select the field that determine how Supply Chain Management will group picking work for workers.</span></span> <span data-ttu-id="cedcb-422">例如，如果您选择<strong>ShipmentId</strong>字段，工作人员将扫描装运 ID 来对领料工作进行分组。</span><span class="sxs-lookup"><span data-stu-id="cedcb-422">For example, if you select the <strong>ShipmentId</strong> field, the worker will scan the shipment ID to group the picking work.</span></span> <span data-ttu-id="cedcb-423">然后将装运的所有工作分配给工作人员。</span><span class="sxs-lookup"><span data-stu-id="cedcb-423">All work for the shipment is then assigned to the worker.</span></span> <span data-ttu-id="cedcb-424">此字段要求您创建一个菜单项从而使用系统分组现有工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-424">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="cedcb-425">您还必须在<strong>系统分组标签</strong>字段中输入文本以通知工作人员需要扫描哪些内容。</span><span class="sxs-lookup"><span data-stu-id="cedcb-425">You must also enter text in the <strong>System grouping label</strong> field to instruct the worker what to scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cedcb-426">系统分组标签</span><span class="sxs-lookup"><span data-stu-id="cedcb-426">System grouping label</span></span></td>
<td><span data-ttu-id="cedcb-427">输入文本，这些文本将通知工作人员当 Supply Chain Management 分组领料工作时，需要扫描的内容。</span><span class="sxs-lookup"><span data-stu-id="cedcb-427">Enter the text that will instruct the worker what to scan when picking work is grouped by Supply Chain Management.</span></span> <span data-ttu-id="cedcb-428">例如，如果您正在使用 <strong>ShipmentId</strong> 字段以按照装运分组领料工作，您可以在字段中输入<strong>装运 ID</strong>。</span><span class="sxs-lookup"><span data-stu-id="cedcb-428">For example, if you&#39;re using the <strong>ShipmentId</strong> field to group picking work by shipment, you might enter <strong>Shipment ID</strong> in the field.</span></span> <span data-ttu-id="cedcb-429">此字段要求您创建一个菜单项从而使用系统分组现有工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-429">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="cedcb-430">您还必须在<strong>系统分组</strong>字段中选择要按其分组的字段。</span><span class="sxs-lookup"><span data-stu-id="cedcb-430">You must also select the field to group by in the <strong>System grouping</strong> field.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cedcb-431">使用默认数据</span><span class="sxs-lookup"><span data-stu-id="cedcb-431">Use default data</span></span></td>
<td><span data-ttu-id="cedcb-432">选择此选项可启用操作窗格上的<strong>默认数据</strong>按钮，您可以在其中选择字段从而显示工作人员在日常工作中通常需要的数据。</span><span class="sxs-lookup"><span data-stu-id="cedcb-432">Select this option to enable the <strong>Default data</strong> button on the Action Pane, where you can select fields to display data that a worker typically requires in his or her daily work.</span></span> <span data-ttu-id="cedcb-433">例如，当一名工作人员经常从同一个位置领料时，此选项很有用。</span><span class="sxs-lookup"><span data-stu-id="cedcb-433">This option is useful if, for example, a worker often picks items from the same location.</span></span> <span data-ttu-id="cedcb-434">您可以选择<strong>源位置</strong>字段以默认显示位置。</span><span class="sxs-lookup"><span data-stu-id="cedcb-434">You can select the <strong>From location</strong> field to display the location by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cedcb-435">已验证用户导向的字段</span><span class="sxs-lookup"><span data-stu-id="cedcb-435">Validated User Directed Field</span></span></td>
<td><span data-ttu-id="cedcb-436">选择工作人员需要用来扫描以分组工作的字段。</span><span class="sxs-lookup"><span data-stu-id="cedcb-436">Select the field that the worker will scan to group the work.</span></span> <span data-ttu-id="cedcb-437">例如，如果您选择<strong>LoadId</strong>，工作人员可以挑选与所选负载相关的任何工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-437">For example, if you select <strong>LoadId</strong>, a worker can pick any work that is associated with a selected load.</span></span> <span data-ttu-id="cedcb-438">您还必须在<strong>已验证用户导向的标签</strong>字段中输入文本以通知工作人员需要扫描哪些内容。</span><span class="sxs-lookup"><span data-stu-id="cedcb-438">You must also enter text in the <strong>Validated User Directed Label</strong> field to instruct the worker what to scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cedcb-439">已验证用户导向的标签</span><span class="sxs-lookup"><span data-stu-id="cedcb-439">Validated User Directed Label</span></span></td>
<td><span data-ttu-id="cedcb-440">当领料工作是由已验证的用户指导字段分组时，输入文本告知工作人员需要扫描的内容。</span><span class="sxs-lookup"><span data-stu-id="cedcb-440">Enter the text that will instruct the worker what to scan when picking work is grouped by a validated user-directed field.</span></span> <span data-ttu-id="cedcb-441">例如，如果您正在使用<strong>LoadId</strong>字段来对负载的领料工作进行分组，您可以在字段中输入<strong>负载 ID</strong>。</span><span class="sxs-lookup"><span data-stu-id="cedcb-441">For example, if you’re using the <strong>LoadId</strong> field to group picking work for a load, you might enter <strong>Load ID</strong> in the field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cedcb-442">工作模板代码</span><span class="sxs-lookup"><span data-stu-id="cedcb-442">Work template code</span></span></td>
<td><span data-ttu-id="cedcb-443">选择用于创建工作流程的工作模板。</span><span class="sxs-lookup"><span data-stu-id="cedcb-443">Select the work template that will create the work for a process.</span></span> <span data-ttu-id="cedcb-444">例如，如果您接收了工作订单中的某个物料，那么会基于工作模板生成入库工作。</span><span class="sxs-lookup"><span data-stu-id="cedcb-444">For example, if you receive an item for a purchase order, the put-away work will be generated based on the work template.</span></span> <span data-ttu-id="cedcb-445">如果您未选择工作模板，那么 Supply Chain Management 将基于查询准则分配一个模板。</span><span class="sxs-lookup"><span data-stu-id="cedcb-445">If you don&#39;t select a work template, Supply Chain Management assigns a template, based on query criteria.</span></span> <span data-ttu-id="cedcb-446">有关工作模板的详细信息，请参阅<a href="control-warehouse-location-directives.md">使用工作模板和位置指令控制仓库工作</a>。</span><span class="sxs-lookup"><span data-stu-id="cedcb-446">For more information about work templates, see <a href="control-warehouse-location-directives.md">Controlling warehouse work with work templates and location directives</a>.</span></span></td>
<tr class="even">
<td><span data-ttu-id="cedcb-447">显示工作行列表</span><span class="sxs-lookup"><span data-stu-id="cedcb-447">Show work line list</span></span></td>
<td><span data-ttu-id="cedcb-448">选择一个工作人员能够如何查看当前所选的领料工作的行并与之交互的选项。</span><span class="sxs-lookup"><span data-stu-id="cedcb-448">Select an option for how workers will be able to view and interact with the lines for the currently selected picking work.</span></span> <span data-ttu-id="cedcb-449">有关此选项的详细信息，请参阅<a href="pick-line-overview.md">设置移动设备菜单项以提供领料行概览</a>。</span><span class="sxs-lookup"><span data-stu-id="cedcb-449">For more information about this option, see <a href="pick-line-overview.md">Set up a mobile device menu item to provide a pick line overview</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="require-workers-to-confirm-the-product-location-or-quantity-when-they-pick-items"></a><span data-ttu-id="cedcb-450">在工作人员领取物料时，要求他们确定产品、位置或数量</span><span class="sxs-lookup"><span data-stu-id="cedcb-450">Require workers to confirm the product, location, or quantity when they pick items</span></span>
<span data-ttu-id="cedcb-451">您可以设置工作确认，要求工作人员在执行仓库内的工作时，使用移动设备登记位置或数量。</span><span class="sxs-lookup"><span data-stu-id="cedcb-451">You can set up work confirmations that require that a worker use a mobile device to register the location or quantity when they perform work in the warehouse.</span></span> <span data-ttu-id="cedcb-452">工作确认帮助确保工作人员处于正确的位置，或者处理的物料数量正确。</span><span class="sxs-lookup"><span data-stu-id="cedcb-452">Work confirmations help ensure that the worker is at the correct location or is handling the correct quantity of items.</span></span> <span data-ttu-id="cedcb-453">您还可以启用 Supply Chain Management 自动确认工作人员的登记信息。</span><span class="sxs-lookup"><span data-stu-id="cedcb-453">You can also enable Supply Chain Management to automatically confirm the worker’s registration.</span></span> <span data-ttu-id="cedcb-454">如果您启用自动确认，您将不能要求位置或数量的确认。</span><span class="sxs-lookup"><span data-stu-id="cedcb-454">If you enable automatic confirmation, you can't also require confirmations for location or quantity.</span></span> <span data-ttu-id="cedcb-455">工作确认还包括产品和产品变型。</span><span class="sxs-lookup"><span data-stu-id="cedcb-455">Work confirmations also include products and product variants.</span></span> <span data-ttu-id="cedcb-456">另外，您还可以通过扫描条形码登记确认。</span><span class="sxs-lookup"><span data-stu-id="cedcb-456">Additionally, you can register confirmations by scanning a bar code.</span></span> <span data-ttu-id="cedcb-457">若要确定产品和产品变型，您必须输入一个产品或产品变型 ID。</span><span class="sxs-lookup"><span data-stu-id="cedcb-457">To confirm products and product variants, you must enter an ID for the product or product variant.</span></span> <span data-ttu-id="cedcb-458">引 ID 可以是产品 ID、产品搜索 ID、外部 ID、GTIN 或条形码。</span><span class="sxs-lookup"><span data-stu-id="cedcb-458">This ID can be a product ID, product search ID, external ID, GTIN, or bar code.</span></span> <span data-ttu-id="cedcb-459">当您输入 ID 或扫描条形码之后，产品变型的维度将显示在移动设备中。</span><span class="sxs-lookup"><span data-stu-id="cedcb-459">After you enter the ID or scan the bar code, the dimensions for the product variant are displayed on the mobile device.</span></span> 

<span data-ttu-id="cedcb-460">下表介绍可用于工作确认的不同的工作类型。</span><span class="sxs-lookup"><span data-stu-id="cedcb-460">The following table describes the various work types that you can use work confirmations with.</span></span>

| <span data-ttu-id="cedcb-461">选项</span><span class="sxs-lookup"><span data-stu-id="cedcb-461">Option</span></span> | <span data-ttu-id="cedcb-462">描述</span><span class="sxs-lookup"><span data-stu-id="cedcb-462">Description</span></span> |
|------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="cedcb-463">挑选</span><span class="sxs-lookup"><span data-stu-id="cedcb-463">Pick</span></span> | <span data-ttu-id="cedcb-464">领取物料时要求确认。</span><span class="sxs-lookup"><span data-stu-id="cedcb-464">Require confirmation when items are picked.</span></span> |
| <span data-ttu-id="cedcb-465">放入</span><span class="sxs-lookup"><span data-stu-id="cedcb-465">Put</span></span> | <span data-ttu-id="cedcb-466">在位置中放置物料时要求确认。</span><span class="sxs-lookup"><span data-stu-id="cedcb-466">Require confirmation when items are put in a location.</span></span> |
| <span data-ttu-id="cedcb-467">正在盘点</span><span class="sxs-lookup"><span data-stu-id="cedcb-467">Counting</span></span> | <span data-ttu-id="cedcb-468">周期盘点期间要求确认。</span><span class="sxs-lookup"><span data-stu-id="cedcb-468">Require confirmation during cycle counting.</span></span> |
| <span data-ttu-id="cedcb-469">调整</span><span class="sxs-lookup"><span data-stu-id="cedcb-469">Adjustments</span></span> | <span data-ttu-id="cedcb-470">调整库存数量时要求确认。</span><span class="sxs-lookup"><span data-stu-id="cedcb-470">Require confirmation when inventory quantities are adjusted.</span></span> |
| <span data-ttu-id="cedcb-471">自定义</span><span class="sxs-lookup"><span data-stu-id="cedcb-471">Custom</span></span> | <span data-ttu-id="cedcb-472">自定义工作要求确认。</span><span class="sxs-lookup"><span data-stu-id="cedcb-472">Require confirmation for custom work.</span></span> |
| <span data-ttu-id="cedcb-473">检验</span><span class="sxs-lookup"><span data-stu-id="cedcb-473">Quarantine</span></span> | <span data-ttu-id="cedcb-474">将物料转移到检验区域时要求确认。</span><span class="sxs-lookup"><span data-stu-id="cedcb-474">Require confirmation when items are moved to quarantine.</span></span> |
| <span data-ttu-id="cedcb-475">牌照生成</span><span class="sxs-lookup"><span data-stu-id="cedcb-475">License plate building</span></span> | <span data-ttu-id="cedcb-476">合并物料以设立牌照时，要求确认。</span><span class="sxs-lookup"><span data-stu-id="cedcb-476">Require confirmation when items are consolidated to build a license plate.</span></span> |
| <span data-ttu-id="cedcb-477">打印</span><span class="sxs-lookup"><span data-stu-id="cedcb-477">Print</span></span> | <span data-ttu-id="cedcb-478">打印牌照标签时要求确认。</span><span class="sxs-lookup"><span data-stu-id="cedcb-478">Require confirmation when license plate labels are printed.</span></span> |
| <span data-ttu-id="cedcb-479">状态更改</span><span class="sxs-lookup"><span data-stu-id="cedcb-479">Status change</span></span> | <span data-ttu-id="cedcb-480">更改库存状态时要求确认。</span><span class="sxs-lookup"><span data-stu-id="cedcb-480">Require confirmation when the status of inventory is changed.</span></span> |

> [!NOTE]
> <span data-ttu-id="cedcb-481">只能对领料和放置工作类型要求产品确认。</span><span class="sxs-lookup"><span data-stu-id="cedcb-481">You can require product confirmation only for pick and put work types.</span></span>

<a name="additional-resources"></a><span data-ttu-id="cedcb-482">其他资源</span><span class="sxs-lookup"><span data-stu-id="cedcb-482">Additional resources</span></span>
--------

[<span data-ttu-id="cedcb-483">设置用于完成采购订单类型工作的移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="cedcb-483">Set up a mobile device menu item for completing work of type Purchase order</span></span>](tasks/set-up-mobile-device-menu.md)

[<span data-ttu-id="cedcb-484">设置登记已接收物料的移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="cedcb-484">Set up a mobile device menu item to register received items</span></span>](tasks/set-up-mobile-device-menu-item-register-received-items.md)

[<span data-ttu-id="cedcb-485">库存状态</span><span class="sxs-lookup"><span data-stu-id="cedcb-485">Inventory statuses</span></span>](../inventory/inventory-statuses.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
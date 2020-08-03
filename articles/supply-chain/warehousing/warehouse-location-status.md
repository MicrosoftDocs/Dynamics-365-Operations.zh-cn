---
title: 仓库货位状态
description: 本主题概述仓库货位状态功能。
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 128083b22bb14d9b445863a0ba1217f723727ee4
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597498"
---
# <a name="warehouse-location-status"></a><span data-ttu-id="38088-103">仓库货位状态</span><span class="sxs-lookup"><span data-stu-id="38088-103">Warehouse location status</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38088-104">Microsoft Dynamics 365 Supply Chain Management 中有若干货位字段，让您可以灵活地处理和维护货位。</span><span class="sxs-lookup"><span data-stu-id="38088-104">Microsoft Dynamics 365 Supply Chain Management includes several location fields that give you flexibility when you work with and maintain locations.</span></span> <span data-ttu-id="38088-105">可以在货位指令查询中包含货位状态，以便更好地控制仓库流。</span><span class="sxs-lookup"><span data-stu-id="38088-105">You can include location statuses in the location directive query to provide better control over warehouse flow.</span></span>

<span data-ttu-id="38088-106">**货位**页面中的下面四个字段跟踪有关当前货位状态的信息。</span><span class="sxs-lookup"><span data-stu-id="38088-106">The following four fields on the **Locations** page track information about the current status of a location.</span></span> <span data-ttu-id="38088-107">仓库经理可通过这些字段概览仓库货位状态。</span><span class="sxs-lookup"><span data-stu-id="38088-107">These fields let warehouse managers get an overview of the status of the warehouse locations.</span></span> <span data-ttu-id="38088-108">还可以用于进行高级报告和筛选。</span><span class="sxs-lookup"><span data-stu-id="38088-108">They also allow for advanced reporting and filtering.</span></span>

- <span data-ttu-id="38088-109">**物料编号** – 当前位于货位中的物料。</span><span class="sxs-lookup"><span data-stu-id="38088-109">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="38088-110">如果货位中有多个物料，则该字段为空。</span><span class="sxs-lookup"><span data-stu-id="38088-110">If the location contains multiple items, this field is blank.</span></span>
- <span data-ttu-id="38088-111">**最后一个活动的日期和时间** – 上次对货位执行的仓库事务的时间戳。</span><span class="sxs-lookup"><span data-stu-id="38088-111">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="38088-112">**帐龄日期** – 将货位中的库存导入仓库时的日期。</span><span class="sxs-lookup"><span data-stu-id="38088-112">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="38088-113">该值基于牌照的帐龄日期计算。</span><span class="sxs-lookup"><span data-stu-id="38088-113">This value is calculated based on the aging date of the license plate.</span></span> <span data-ttu-id="38088-114">其对牌照跟踪的货位来说是准确的，但是对不是牌照跟踪的货位来说可能不准确。</span><span class="sxs-lookup"><span data-stu-id="38088-114">It's accurate for locations that are license plate–tracked, but it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="38088-115">**货位状态** – 货位的状态。</span><span class="sxs-lookup"><span data-stu-id="38088-115">**Location status** – The status of the location.</span></span> <span data-ttu-id="38088-116">可以有四个值：</span><span class="sxs-lookup"><span data-stu-id="38088-116">There are four possible values:</span></span>

    - <span data-ttu-id="38088-117">**未确定** – 货位模板不能跟踪状态。</span><span class="sxs-lookup"><span data-stu-id="38088-117">**Undetermined** – The location profile can't track status.</span></span> <span data-ttu-id="38088-118">因此，当前状态未知。</span><span class="sxs-lookup"><span data-stu-id="38088-118">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="38088-119">**空** – 货位中当前无库存。</span><span class="sxs-lookup"><span data-stu-id="38088-119">**Empty** – There is currently no inventory in the location.</span></span>
    - <span data-ttu-id="38088-120">**正在领料** – 因为货位最近为空，所以已对其执行了出库事务。</span><span class="sxs-lookup"><span data-stu-id="38088-120">**Picking** – Outbound transactions have been performed against the location since it was last empty.</span></span>
    - <span data-ttu-id="38088-121">**存储** – 因为货位最近为空，所以已对其仅执行了入库事务。</span><span class="sxs-lookup"><span data-stu-id="38088-121">**Storage** – Only inbound transactions have been performed against the location since the location was last empty.</span></span>

## <a name="turn-on-the-warehouse-location-status-feature"></a><span data-ttu-id="38088-122">开启“仓库货位状态”功能</span><span class="sxs-lookup"><span data-stu-id="38088-122">Turn on the Warehouse location status feature</span></span>

<span data-ttu-id="38088-123">*仓库货位状态*功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="38088-123">Before you can use the *Warehouse location status* feature, it must be turned on in your system.</span></span> <span data-ttu-id="38088-124">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="38088-124">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="38088-125">在**功能管理**工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="38088-125">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="38088-126">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="38088-126">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="38088-127">**功能名称**：*仓库货位状态*</span><span class="sxs-lookup"><span data-stu-id="38088-127">**Feature name:** *Warehouse location status*</span></span>

## <a name="set-up-warehouse-location-status"></a><span data-ttu-id="38088-128">设置仓库货位状态</span><span class="sxs-lookup"><span data-stu-id="38088-128">Set up warehouse location status</span></span>

### <a name="prepare-the-sample-data-that-is-required-for-the-example-scenario"></a><span data-ttu-id="38088-129">准备示例场景所需的示例数据</span><span class="sxs-lookup"><span data-stu-id="38088-129">Prepare the sample data that is required for the example scenario</span></span>

<span data-ttu-id="38088-130">开始完成此场景之前，必须按照本部分中的说明激活示例数据和设置功能。</span><span class="sxs-lookup"><span data-stu-id="38088-130">Before you start to work through the scenario, you must activate sample data and set up the feature as described in this section.</span></span> <span data-ttu-id="38088-131">若要完成示例场景，必须使用仓库应用或基于浏览器的模拟器。</span><span class="sxs-lookup"><span data-stu-id="38088-131">To complete the example scenario, you must use either the warehouse app or the browser-based emulator.</span></span> <span data-ttu-id="38088-132">此处提供的步骤使用仓库应用。</span><span class="sxs-lookup"><span data-stu-id="38088-132">The steps that are provided here use the warehouse app.</span></span> <span data-ttu-id="38088-133">基于浏览器的模拟器的步骤类似。</span><span class="sxs-lookup"><span data-stu-id="38088-133">The steps for the browser-based emulator are similar.</span></span>

#### <a name="use-the-usmf-legal-entity"></a><span data-ttu-id="38088-134">使用 USMF 法人</span><span class="sxs-lookup"><span data-stu-id="38088-134">Use the USMF legal entity</span></span>

<span data-ttu-id="38088-135">若要使用此处指定的示例记录和值完成示例场景，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="38088-135">To work through the example scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="38088-136">此外，开始前，还必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="38088-136">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="set-up-location-profiles"></a><span data-ttu-id="38088-137">设置货位模板</span><span class="sxs-lookup"><span data-stu-id="38088-137">Set up location profiles</span></span>

<span data-ttu-id="38088-138">示例场景需要您准备两个货位模板。</span><span class="sxs-lookup"><span data-stu-id="38088-138">The example scenario requires that you prepare two location profiles.</span></span>

1. <span data-ttu-id="38088-139">转到**仓库管理 \> 设置 \> 仓库 \> 货位模板**。</span><span class="sxs-lookup"><span data-stu-id="38088-139">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="38088-140">选择**编辑**将页面设置为编辑模式。</span><span class="sxs-lookup"><span data-stu-id="38088-140">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="38088-141">选择 **BULK-06** 模板。</span><span class="sxs-lookup"><span data-stu-id="38088-141">Select the **BULK-06** profile.</span></span>
1. <span data-ttu-id="38088-142">在**常规**快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="38088-142">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="38088-143">**在货位中启用物料：** 将此选项设置为_是_。</span><span class="sxs-lookup"><span data-stu-id="38088-143">**Enable item in location:** Set this option to _Yes_.</span></span>
    - <span data-ttu-id="38088-144">**启用货位活动日期和时间：** 将此选项设置为_是_。</span><span class="sxs-lookup"><span data-stu-id="38088-144">**Enable location activity date and time:** Set this option to _Yes_.</span></span>
    - <span data-ttu-id="38088-145">**启用货位状态：** 将此选项设置为_是_。</span><span class="sxs-lookup"><span data-stu-id="38088-145">**Enable location status:** Set this option to _Yes_.</span></span>

    <span data-ttu-id="38088-146">这些选项控制货位中的引用字段是否处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="38088-146">These options control whether the reference fields on the location are active.</span></span>

1. <span data-ttu-id="38088-147">对 **PICK-06** 模板重复执行步骤 3 到 4。</span><span class="sxs-lookup"><span data-stu-id="38088-147">Repeat steps 3 through 4 for the **PICK-06** profile.</span></span>

### <a name="scenario"></a><span data-ttu-id="38088-148">应用场景</span><span class="sxs-lookup"><span data-stu-id="38088-148">Scenario</span></span>

1. <span data-ttu-id="38088-149">转到**采购 \> 采购订单 \> 所有采购订单**。</span><span class="sxs-lookup"><span data-stu-id="38088-149">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="38088-150">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="38088-150">Select **New**.</span></span>
1. <span data-ttu-id="38088-151">在**创建采购订单**对话框中**供应商**快速选项卡上**供应商帐户**字段内，选择 *104*。</span><span class="sxs-lookup"><span data-stu-id="38088-151">In the **Create purchase order** dialog box, on the **Vendor** FastTab, in the **Vendor account** field, select *104*.</span></span>
1. <span data-ttu-id="38088-152">在**常规**快速选项卡上的**仓库**字段中，选择 *61*。</span><span class="sxs-lookup"><span data-stu-id="38088-152">On the **General** FastTab, in the **Warehouse** field, select *61*.</span></span>
1. <span data-ttu-id="38088-153">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="38088-153">Select **OK**.</span></span>
1. <span data-ttu-id="38088-154">将打开您的新采购订单 (PO)。</span><span class="sxs-lookup"><span data-stu-id="38088-154">Your new purchase order (PO) is opened.</span></span> <span data-ttu-id="38088-155">将在**采购订单行**网格中添加一个空行。</span><span class="sxs-lookup"><span data-stu-id="38088-155">It includes an empty line in the **Purchase order lines** grid.</span></span> <span data-ttu-id="38088-156">在这个行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="38088-156">On this line, set the following values:</span></span>

    - <span data-ttu-id="38088-157">**物料编号：**_A0002_</span><span class="sxs-lookup"><span data-stu-id="38088-157">**Item number:** _A0002_</span></span>
    - <span data-ttu-id="38088-158">**数量：** _5_</span><span class="sxs-lookup"><span data-stu-id="38088-158">**Quantity:** _5_</span></span>

1. <span data-ttu-id="38088-159">在操作窗格中**采购**选项卡上**操作**组内，选择**确认**确认采购订单。</span><span class="sxs-lookup"><span data-stu-id="38088-159">On the Action Pane, on the **Purchase** tab, in the **Actions** group, select **Confirm** to confirm the purchase order.</span></span>
1. <span data-ttu-id="38088-160">在移动设备上，转到**入库 \> 采购收货**。</span><span class="sxs-lookup"><span data-stu-id="38088-160">On the mobile device, go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="38088-161">选择 **PONUM** 字段，输入采购订单编号，然后确认。</span><span class="sxs-lookup"><span data-stu-id="38088-161">Select the **PONUM** field, enter the PO number, and confirm.</span></span>
1. <span data-ttu-id="38088-162">选择 **ITEM** 字段，为物料编号输入 *A0002*，然后确认。</span><span class="sxs-lookup"><span data-stu-id="38088-162">Select the **ITEM** field, enter *A0002* as the item number, and confirm.</span></span>
1. <span data-ttu-id="38088-163">在**数量**页面中，为数量输入 *5*，然后确认。</span><span class="sxs-lookup"><span data-stu-id="38088-163">On the **QTY** page, enter *5* as the quantity, and confirm.</span></span>

    <span data-ttu-id="38088-164">可以采用以下方法之一输入数量：</span><span class="sxs-lookup"><span data-stu-id="38088-164">You can enter the quantity in either of the following ways:</span></span>

    - <span data-ttu-id="38088-165">选择加号 (**+**) 或减号 (**–**) 按钮增加或减去一个数值。</span><span class="sxs-lookup"><span data-stu-id="38088-165">Select the plus sign (**+**) or minus sign (**–**) button to add or subtract a numerical value.</span></span>
    - <span data-ttu-id="38088-166">选择加号 (**+**) 与减号 (**–**) 按钮之间的空字段打开数字小键盘。</span><span class="sxs-lookup"><span data-stu-id="38088-166">Select the blank field between the plus sign (**+**) and minus sign (**–**) buttons to open the number pad.</span></span>

1. <span data-ttu-id="38088-167">确认所选物料编号 *A0002* 和数量 *5*。</span><span class="sxs-lookup"><span data-stu-id="38088-167">Confirm your selection of item number *A0002* and a quantity of *5*.</span></span> <span data-ttu-id="38088-168">页面底部将显示“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="38088-168">A "Work Completed" message appears at the bottom of the page.</span></span>
1. <span data-ttu-id="38088-169">选择右上角的“菜单”按钮（有时称为汉堡包或汉堡包按钮），然后选择**取消**退出**采购收货**并回到**入库**菜单。</span><span class="sxs-lookup"><span data-stu-id="38088-169">Select the Menu button (sometimes referred to as the hamburger or the hamburger button) in the upper-right corner, and then select **Cancel** to exit **Purchase Receive** and return to the **Inbound** menu.</span></span>
1. <span data-ttu-id="38088-170">在采购订单页中，选择**采购订单行**网格上方的**工作详细信息**。</span><span class="sxs-lookup"><span data-stu-id="38088-170">On the purchase order page, select **Work details** above the **Purchase order lines** grid.</span></span>
1. <span data-ttu-id="38088-171">记下**常规**选项卡上创建的**工作 ID** 和**目标牌照 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="38088-171">On the **General** tab, notice the **Work ID** and **Target license plate ID** values that were created.</span></span>
1. <span data-ttu-id="38088-172">记下**行**部分中*领料*和*放置*工作类型的**货位**值。</span><span class="sxs-lookup"><span data-stu-id="38088-172">In the **Lines** section, notice the **Location** values for the *Pick* and *Put* work types.</span></span>
1. <span data-ttu-id="38088-173">在移动设备上，转到**入库 \> 采购储存**。</span><span class="sxs-lookup"><span data-stu-id="38088-173">On the mobile device, go to **Inbound \> Purchase Put-away**.</span></span>
1. <span data-ttu-id="38088-174">选择 **ID** 字段，输入工作 ID，然后确认。</span><span class="sxs-lookup"><span data-stu-id="38088-174">Select the **ID** field, enter the work ID, and confirm.</span></span>
1. <span data-ttu-id="38088-175">再次确认以完成*领料*条目。</span><span class="sxs-lookup"><span data-stu-id="38088-175">Confirm once more to complete the *Pick* entry.</span></span>
1. <span data-ttu-id="38088-176">选择右上角的“菜单”按钮，然后选择**完成**完成*领料*工作。</span><span class="sxs-lookup"><span data-stu-id="38088-176">Select the Menu button in the upper-right corner, and then select **Done** to complete the *Pick* work.</span></span>
1. <span data-ttu-id="38088-177">记下存储货位，然后确认。</span><span class="sxs-lookup"><span data-stu-id="38088-177">Make a note of the Putaway location, and confirm.</span></span> <span data-ttu-id="38088-178">页面底部将显示“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="38088-178">A "Work Completed" message appears at the bottom of the page.</span></span>
1. <span data-ttu-id="38088-179">选择右上角的“菜单”按钮，然后选择**取消**退出**采购储存**并回到**入库**菜单。</span><span class="sxs-lookup"><span data-stu-id="38088-179">Select the Menu button in the upper-right corner, and then select **Cancel** to exit **Purchase Put-away** and return to the **Inbound** menu.</span></span>
1. <span data-ttu-id="38088-180">选择**后退**回到主菜单。</span><span class="sxs-lookup"><span data-stu-id="38088-180">Select **Back** to return to the main menu.</span></span>
1. <span data-ttu-id="38088-181">在 Dynamics 365 Supply Chain Management 中，转到**仓库管理 \> 设置 \> 仓库 \> 货位**。</span><span class="sxs-lookup"><span data-stu-id="38088-181">In Dynamics 365 Supply Chain Management, go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="38088-182">在**货位**中筛选，然后输入采购订单工作中的储存货位。</span><span class="sxs-lookup"><span data-stu-id="38088-182">Filter on **Location**, and enter the putaway location from the purchase order work.</span></span> <span data-ttu-id="38088-183">应该会看到以下结果：</span><span class="sxs-lookup"><span data-stu-id="38088-183">You should see the following results:</span></span>

    - <span data-ttu-id="38088-184">**货位状态**列显示值*存储*，因为上次对此货位执行的事务为放置。</span><span class="sxs-lookup"><span data-stu-id="38088-184">The **Location status** column shows a value of *Storage*, because the last transaction against this location was a put.</span></span>
    - <span data-ttu-id="38088-185">**物料编号**列显示值 *A0002*，因为收到了物料并放到了货位。</span><span class="sxs-lookup"><span data-stu-id="38088-185">The **Item number** column shows a value of *A0002*, because that item was received and put to the location.</span></span>
    - <span data-ttu-id="38088-186">**最后一个活动的日期和时间**列显示在货位完成工作的日期和时间的时间戳。</span><span class="sxs-lookup"><span data-stu-id="38088-186">The **Last activity date and time** column shows the timestamp for the date and time when the work was completed at the location.</span></span>

1. <span data-ttu-id="38088-187">在移动设备上，转到**质量 \> 移动**。</span><span class="sxs-lookup"><span data-stu-id="38088-187">On the mobile device, go to **Quality \> Movement**.</span></span>
1. <span data-ttu-id="38088-188">选择 **LOC/LP** 字段，然后输入在前面的步骤中记下的货位。</span><span class="sxs-lookup"><span data-stu-id="38088-188">Select the **LOC/LP** field, and enter the location you made note of in the previous steps.</span></span>
1. <span data-ttu-id="38088-189">确认显示的信息。</span><span class="sxs-lookup"><span data-stu-id="38088-189">Confirm the information that is shown.</span></span> <span data-ttu-id="38088-190">记下生成的牌照编号。</span><span class="sxs-lookup"><span data-stu-id="38088-190">Make a note of the license plate number that is generated.</span></span>
1. <span data-ttu-id="38088-191">在**目标信息**屏幕中，选择 **LOC/LP** 字段，然后输入 *06A07R2S1B* 作为物料的移动目标货位。</span><span class="sxs-lookup"><span data-stu-id="38088-191">On the **To Information** screen, select the **LOC/LP** field, and enter *06A07R2S1B* as the location to move the item to.</span></span>
1. <span data-ttu-id="38088-192">在**目标信息**屏幕中，确认 **LP** 值（目标牌照 ID），这是自动生成的。</span><span class="sxs-lookup"><span data-stu-id="38088-192">On the **To Information** screen, confirm the **LP** value (the target license plate ID), which is automatically generated.</span></span> <span data-ttu-id="38088-193">页面底部将显示“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="38088-193">A "Work Completed" message appears at the bottom of the page.</span></span>
1. <span data-ttu-id="38088-194">选择右上角的“菜单”按钮，然后选择**取消**退出**移动**并回到**质量管理**菜单。</span><span class="sxs-lookup"><span data-stu-id="38088-194">Select the Menu button in the upper-right corner, and then select **Cancel** to exit **Movement** and return to the **Quality Management** menu.</span></span>
1. <span data-ttu-id="38088-195">选择**后退**回到主菜单。</span><span class="sxs-lookup"><span data-stu-id="38088-195">Select **Back** to return to the main menu.</span></span>
1. <span data-ttu-id="38088-196">在 Dynamics 365 Supply Chain Management 中，转到**仓库管理 \> 设置 \> 仓库 \> 货位**。</span><span class="sxs-lookup"><span data-stu-id="38088-196">In Dynamics 365 Supply Chain Management, go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="38088-197">刷新**货位**页面，然后再次查看初始储存货位。</span><span class="sxs-lookup"><span data-stu-id="38088-197">Refresh the **Locations** page, and view the original putaway location again.</span></span> <span data-ttu-id="38088-198">请注意，**货位状态**字段现在设置为*空*，并且**物料编号**列为空。</span><span class="sxs-lookup"><span data-stu-id="38088-198">Notice that the **Location status** field is now set to *Empty*, and the **Item number** column is blank.</span></span>
1. <span data-ttu-id="38088-199">查看货位 *06A07R2S1B* 的记录，并注意**状态**值已更改为*存储*，并且已更新了**物料编号**和**最后一个活动的日期和时间**字段。</span><span class="sxs-lookup"><span data-stu-id="38088-199">View the record for location *06A07R2S1B*, and notice that the **Status** value has changed to *Storage*, and the **Item number** and **Last activity date and time** fields have been updated.</span></span>
1. <span data-ttu-id="38088-200">转到**销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="38088-200">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="38088-201">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="38088-201">Select **New**.</span></span>
1. <span data-ttu-id="38088-202">在**创建销售订单**对话框的**客户帐户**字段中，选择 *US-002*。</span><span class="sxs-lookup"><span data-stu-id="38088-202">In the **Create sales order** dialog box, in the **Customer account** field, select *US-002*.</span></span>
1. <span data-ttu-id="38088-203">在**仓库**字段中，选择 *61*。</span><span class="sxs-lookup"><span data-stu-id="38088-203">In the **Warehouse** field, select *61*.</span></span>
1. <span data-ttu-id="38088-204">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="38088-204">Select **OK**.</span></span>
1. <span data-ttu-id="38088-205">将打开您的新销售订单。</span><span class="sxs-lookup"><span data-stu-id="38088-205">Your new sales order is opened.</span></span> <span data-ttu-id="38088-206">将在**销售订单行**网格中添加一个空行。</span><span class="sxs-lookup"><span data-stu-id="38088-206">It includes an empty line in the **Sales order lines** grid.</span></span> <span data-ttu-id="38088-207">在这个行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="38088-207">On this line, set the following values:</span></span>

    - <span data-ttu-id="38088-208">**物料编号：**_A0002_</span><span class="sxs-lookup"><span data-stu-id="38088-208">**Item number:** _A0002_</span></span>
    - <span data-ttu-id="38088-209">**数量：** _1_</span><span class="sxs-lookup"><span data-stu-id="38088-209">**Quantity:** _1_</span></span>

1. <span data-ttu-id="38088-210">在**销售订单行**快速选项卡上的**库存**菜单中，选择**预留**。</span><span class="sxs-lookup"><span data-stu-id="38088-210">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
1. <span data-ttu-id="38088-211">在**预留**页面中，选择**预留批次**预留订单行。</span><span class="sxs-lookup"><span data-stu-id="38088-211">On the **Reservation** page, select **Reserve lot** to reserve the order line.</span></span> <span data-ttu-id="38088-212">然后选择右上角的**关闭**按钮 (**X**) 关闭此页。</span><span class="sxs-lookup"><span data-stu-id="38088-212">Then select the **Close** button (**X**) in the upper-right corner to close the page.</span></span>
1. <span data-ttu-id="38088-213">在“操作窗格”上的**仓库**选项卡上，在**操作**组中，选择**发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="38088-213">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="38088-214">在**销售订单行**部分的**仓库**菜单中，选择**工作详细信息**。</span><span class="sxs-lookup"><span data-stu-id="38088-214">In the **Sales order lines** section, on the **Warehouse** menu, select **Work details**.</span></span>
1. <span data-ttu-id="38088-215">复制创建的**工作 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="38088-215">Copy the **Work ID** value that was created.</span></span>
1. <span data-ttu-id="38088-216">在移动设备上，转到**出库 \> 销售领料**。</span><span class="sxs-lookup"><span data-stu-id="38088-216">On the mobile device, go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="38088-217">选择 **ID** 字段，输入前面复制的工作 ID，然后确认。</span><span class="sxs-lookup"><span data-stu-id="38088-217">Select the **ID** field, enter the work ID that you copied earlier, and confirm.</span></span>
1. <span data-ttu-id="38088-218">在**销售订单: 领料**页面中，**LOC** 字段推荐前面创建的领料货位作为储存货位。</span><span class="sxs-lookup"><span data-stu-id="38088-218">On the **Sales orders: Pick** page, the **LOC** field suggests the picking location as the putaway location that was created earlier.</span></span> <span data-ttu-id="38088-219">记下此货位。</span><span class="sxs-lookup"><span data-stu-id="38088-219">Make a note of the location.</span></span>
1. <span data-ttu-id="38088-220">选择 **LOC** 字段，输入货位，然后确认。</span><span class="sxs-lookup"><span data-stu-id="38088-220">Select the **LOC** field, enter the location, and confirm.</span></span>
1. <span data-ttu-id="38088-221">选择 **LP** 字段，输入移动活动期间记下的牌照编号，然后确认。</span><span class="sxs-lookup"><span data-stu-id="38088-221">Select the **LP** field, enter the license plate number that you made a note of during the Movement activity, and confirm.</span></span>
1. <span data-ttu-id="38088-222">选择**物料**字段，为物料编号输入 *A0002*，然后确认。</span><span class="sxs-lookup"><span data-stu-id="38088-222">Select the **Item** field, enter the *A0002* as the item number, and confirm.</span></span>
1. <span data-ttu-id="38088-223">在**数量**页面中，为数量输入 *1*，然后确认。</span><span class="sxs-lookup"><span data-stu-id="38088-223">On the **QTY** page, enter *1* as the quantity, and confirm.</span></span>

    <span data-ttu-id="38088-224">可以采用以下方法之一输入数量：</span><span class="sxs-lookup"><span data-stu-id="38088-224">You can enter the quantity in either of the following ways:</span></span>

    - <span data-ttu-id="38088-225">选择加号 (**+**) 或减号 (**–**) 按钮增加或减去一个数值。</span><span class="sxs-lookup"><span data-stu-id="38088-225">Select the plus sign (**+**) or minus sign (**–**) button to add or subtract a numerical value.</span></span>
    - <span data-ttu-id="38088-226">选择加号 (**+**) 与减号 (**–**) 按钮之间的空字段打开数字小键盘。</span><span class="sxs-lookup"><span data-stu-id="38088-226">Select the blank field between the plus sign (**+**) and minus sign (**–**) buttons to open the number pad.</span></span>

1. <span data-ttu-id="38088-227">选择**目标牌照**字段，输入用户定义的目标牌照 ID，然后确认。</span><span class="sxs-lookup"><span data-stu-id="38088-227">Select the **TARGET LP** field, enter a user-defined target license plate ID, and confirm.</span></span>
1. <span data-ttu-id="38088-228">再次确认以完成领料工作。</span><span class="sxs-lookup"><span data-stu-id="38088-228">Confirm once more to complete the picking work.</span></span> <span data-ttu-id="38088-229">页面底部将显示“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="38088-229">A "Work Completed" message appears at the bottom of the page.</span></span>
1. <span data-ttu-id="38088-230">选择右上角的“菜单”按钮，然后选择**取消**完成领料活动并回到**出库**菜单。</span><span class="sxs-lookup"><span data-stu-id="38088-230">Select the Menu button in the upper-right corner, and then select **Cancel** to complete the picking activity and return to the **Outbound** menu.</span></span>
1. <span data-ttu-id="38088-231">在 Dynamics 365 Supply Chain Management 中，转到**仓库管理 \> 设置 \> 仓库 \> 货位**。</span><span class="sxs-lookup"><span data-stu-id="38088-231">In Dynamics 365 Supply Chain Management, go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="38088-232">在**货位**中筛选，然后输入销售订单工作中的领料货位。</span><span class="sxs-lookup"><span data-stu-id="38088-232">Filter on **Location**, and enter the pick location from the sales order work.</span></span>
1. <span data-ttu-id="38088-233">请注意，销售订单工作的领料来源货位的**货位状态**字段现在设置为*正在领料*，并且已更新**最后一个活动的日期和时间**字段。</span><span class="sxs-lookup"><span data-stu-id="38088-233">Notice that the **Location status** field for the location that the sales order work picked from is now set to *Picking*, and the **Last activity date and time** field has been updated.</span></span>

> [!NOTE]
> <span data-ttu-id="38088-234">只有仓库事务才会更新货位字段。</span><span class="sxs-lookup"><span data-stu-id="38088-234">The location fields are updated only by warehouse transactions.</span></span> <span data-ttu-id="38088-235">如果使用日记帐或其他非 WHS 流程移动库存，将不更新这些字段。</span><span class="sxs-lookup"><span data-stu-id="38088-235">If you move inventory by using a journal or other non-WHS processes, the fields won't be updated.</span></span>

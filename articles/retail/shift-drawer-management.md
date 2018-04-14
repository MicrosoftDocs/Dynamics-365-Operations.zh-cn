---
title: "班次和银箱管理"
description: "本文介绍了如何设置和使用两种类型的零售销售点 (POS) 班次 - 共享和独立。 共享班次可由多个用户在多个位置使用，而独立班次一次只能由一个工作人员使用。"
author: rubencdelgado
manager: AnnBe
ms.date: 02/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 4b39fafb7fb51ee26bd45fb28ce4b505a91de813
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="shift-and-cash-drawer-management"></a><span data-ttu-id="5b555-104">班次和银箱管理</span><span class="sxs-lookup"><span data-stu-id="5b555-104">Shift and cash drawer management</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="5b555-105">本文介绍了如何设置和使用两种类型的零售销售点 (POS) 班次 - 共享和独立。</span><span class="sxs-lookup"><span data-stu-id="5b555-105">This article explains how to set up and use the two types of retail point of sale (POS) shifts -  shared and stand-alone.</span></span> <span data-ttu-id="5b555-106">共享班次可由多个用户在多个位置使用，而独立班次一次只能由一个工作人员使用。</span><span class="sxs-lookup"><span data-stu-id="5b555-106">Shared shifts can be used by multiple users in multiple places, whereas stand-alone shifts can be used by only one worker at a time.</span></span>

<span data-ttu-id="5b555-107">有两种类型的零售销售点 (POS) 班次︰独立和共享。</span><span class="sxs-lookup"><span data-stu-id="5b555-107">There are two types of retail point of sale (POS) shifts: stand-alone and shared.</span></span> <span data-ttu-id="5b555-108">独立班次一次只能由一名工作人员使用。</span><span class="sxs-lookup"><span data-stu-id="5b555-108">Stand-alone shifts can be used by only one worker at a time.</span></span> <span data-ttu-id="5b555-109">共享班次可以在多个位置由多个用户使用。</span><span class="sxs-lookup"><span data-stu-id="5b555-109">Shared shifts can be used by multiple users in multiple places.</span></span> <span data-ttu-id="5b555-110">因此，它们在商店内为多个工作人员有效地创建一个班次。</span><span class="sxs-lookup"><span data-stu-id="5b555-110">Therefore, they effectively create a single shift for multiple workers in a store.</span></span>

## <a name="standalone-shifts"></a><span data-ttu-id="5b555-111">独立班次</span><span class="sxs-lookup"><span data-stu-id="5b555-111">Standalone shifts</span></span>
<span data-ttu-id="5b555-112">独立班次在传统的固定 POS 情况中使用，在这种情况下，为每个 POS 收银机独立对帐现金。</span><span class="sxs-lookup"><span data-stu-id="5b555-112">Stand-alone shifts are used in a traditional, fixed POS scenario, where cash is reconciled independently for each POS register.</span></span> <span data-ttu-id="5b555-113">例如，在杂货店设置中，通常有几种固定的 POS 收银机，并分配给每个收银机一名出纳。</span><span class="sxs-lookup"><span data-stu-id="5b555-113">For example, in a grocery store setting, there are typically several fixed POS registers, and a cashier is assigned to each register.</span></span> <span data-ttu-id="5b555-114">在这种情况下，可能每个收银机使用一个独立班次，出纳负责收银机的钱盒或实际现金。</span><span class="sxs-lookup"><span data-stu-id="5b555-114">In this case, each register likely uses a stand-alone shift, and the cashier is responsible for the till or physical cash at that register.</span></span> <span data-ttu-id="5b555-115">独立班次在出纳的工作班次期间覆盖该收银机的所有活动。</span><span class="sxs-lookup"><span data-stu-id="5b555-115">A stand-alone shift encompasses all the activity on that register during the cashier’s work shift.</span></span> <span data-ttu-id="5b555-116">活动可以包括存入钱盒的未结金额，通过操作（如银行投箱和浮动条目）进行的所有现金取出和增加，以及班次结束时的钱币清点。</span><span class="sxs-lookup"><span data-stu-id="5b555-116">Activities can include the opening amount that is deposited in the till, all removal and addition of cash through operations such as bank drops and float entry, and the tender declaration at the end of the shift.</span></span>

### <a name="set-up-a-stand-alone-shift"></a><span data-ttu-id="5b555-117">设置独立班次</span><span class="sxs-lookup"><span data-stu-id="5b555-117">Set up a stand-alone shift</span></span>

<span data-ttu-id="5b555-118">在银箱级别指定独立班次。</span><span class="sxs-lookup"><span data-stu-id="5b555-118">A stand-alone shift is designated at the cash drawer level.</span></span> <span data-ttu-id="5b555-119">此过程说明如何在 POS 收银机上设置独立班次。</span><span class="sxs-lookup"><span data-stu-id="5b555-119">This procedure explains how to set up a stand-alone shift on a POS register.</span></span>

1.  <span data-ttu-id="5b555-120">单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **硬件配置文件**。</span><span class="sxs-lookup"><span data-stu-id="5b555-120">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span>
2.  <span data-ttu-id="5b555-121">选择要用于独立班次的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="5b555-121">Select the hardware profile to use for the stand-alone shift.</span></span>
3.  <span data-ttu-id="5b555-122">在**开票人**快速选项卡上，确认**共享班次开票人**选项设置为**无**。</span><span class="sxs-lookup"><span data-stu-id="5b555-122">On the **Drawer** FastTab, confirm that the **Shared shift drawer** option is set to **No**.</span></span>
4.  <span data-ttu-id="5b555-123">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="5b555-123">Click **Save**.</span></span>
5.  <span data-ttu-id="5b555-124">单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **收银机**。</span><span class="sxs-lookup"><span data-stu-id="5b555-124">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span>
6.  <span data-ttu-id="5b555-125">选择需要独立班次的收银机，然后单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="5b555-125">Select the register that requires a stand-alone shift, and then click **Edit**.</span></span>
7.  <span data-ttu-id="5b555-126">在**硬件配置文件**字段中，选择您在步骤 2 中选定的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="5b555-126">In the **Hardware profile** field, select the hardware profile that you selected in step 2.</span></span>
8.  <span data-ttu-id="5b555-127">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="5b555-127">Click **Save**.</span></span>
9.  <span data-ttu-id="5b555-128">单击**零售** &gt; **零售 IT** &gt; **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="5b555-128">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
10. <span data-ttu-id="5b555-129">选择 **1090** 配送计划，然后单击**立即运行**以将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="5b555-129">Select the **1090** distribution schedule, and then click **Run now** to synchronize changes to the POS.</span></span>

### <a name="use-a-stand-alone-shift"></a><span data-ttu-id="5b555-130">使用独立班次</span><span class="sxs-lookup"><span data-stu-id="5b555-130">Use a stand-alone shift</span></span>

1.  <span data-ttu-id="5b555-131">登录到 POS。</span><span class="sxs-lookup"><span data-stu-id="5b555-131">Sign in to the POS.</span></span>
2.  <span data-ttu-id="5b555-132">如果没有班次是打开的，选择**打开新班次**。</span><span class="sxs-lookup"><span data-stu-id="5b555-132">If no shift is open, select **Open a new shift**.</span></span>
3.  <span data-ttu-id="5b555-133">转到**清点初始金额**操作，并指定正在添加到钱盒以开始工作日的现金金额。</span><span class="sxs-lookup"><span data-stu-id="5b555-133">Go to the **Declare start amount** operation, and specify the amount of cash that is being added to the till to start the work day.</span></span>
4.  <span data-ttu-id="5b555-134">执行一些交易。</span><span class="sxs-lookup"><span data-stu-id="5b555-134">Perform some transactions.</span></span>
5.  <span data-ttu-id="5b555-135">在一天结束时，选择**清点钱币**清点银箱中剩余的现金金额。</span><span class="sxs-lookup"><span data-stu-id="5b555-135">At the end of the day, select **Declare tender** to declare the amount of cash that remains in the cash drawer.</span></span>
6.  <span data-ttu-id="5b555-136">输入现金金额，然后单击**保存**保存钱币清点结果。</span><span class="sxs-lookup"><span data-stu-id="5b555-136">Enter the amount of cash, and then click **Save** to save the tender declaration.</span></span>
7.  <span data-ttu-id="5b555-137">选择**结束班次**以关闭班次。</span><span class="sxs-lookup"><span data-stu-id="5b555-137">Select **Close shift** to close the shift.</span></span>

<span data-ttu-id="5b555-138">**注意︰**班次期间还提供其他操作，具体取决于使用的业务流程。</span><span class="sxs-lookup"><span data-stu-id="5b555-138">**Note:** Other operations are available during the shift, depending on the business processes that are in place.</span></span> <span data-ttu-id="5b555-139">**金库投箱**、**银行投箱**和**取钱**操作可用于在一天内或关闭班次之前从钱盒中取钱。</span><span class="sxs-lookup"><span data-stu-id="5b555-139">The **Safe drop**, **Bank drop**, and **Tender removal** operations can be used to remove money from the till during the day or before the shift is closed.</span></span> <span data-ttu-id="5b555-140">如果钱盒现金不足，**浮动条目**操作可用于向钱盒添加现金。</span><span class="sxs-lookup"><span data-stu-id="5b555-140">If a till runs low on cash, the **Float entry** operation can be used to add cash to the till.</span></span>

## <a name="shared-shifts"></a><span data-ttu-id="5b555-141">共享班次</span><span class="sxs-lookup"><span data-stu-id="5b555-141">Shared shifts</span></span>
<span data-ttu-id="5b555-142">共享班次用于以下环境：多个出纳共享银箱或一组银箱全天使用。</span><span class="sxs-lookup"><span data-stu-id="5b555-142">A shared shift is used in an environment where multiple cashiers share a cash drawer or a set of cash drawers throughout the work day.</span></span> <span data-ttu-id="5b555-143">通常情况下，共享班次用于移动 POS 环境。</span><span class="sxs-lookup"><span data-stu-id="5b555-143">Typically, a shared shift is used in mobile POS environments.</span></span> <span data-ttu-id="5b555-144">在移动环境中，不会为单个银箱分配每个出纳，且出纳不负责单个银箱。</span><span class="sxs-lookup"><span data-stu-id="5b555-144">In a mobile environment, each cashier isn’t assigned to and responsible for a single cash drawer.</span></span> <span data-ttu-id="5b555-145">相反，所有出纳都必须能够支付销售并添加现金到任何离他们最近的银箱。</span><span class="sxs-lookup"><span data-stu-id="5b555-145">Instead, all cashiers must be able to tender a sale and add cash to whatever cash drawer is closest to them.</span></span> <span data-ttu-id="5b555-146">在这种情况下，在出纳之间共享的银箱包括在共享班次中。</span><span class="sxs-lookup"><span data-stu-id="5b555-146">In this scenario, the cash drawers that are shared among cashiers are included in a shared shift.</span></span> <span data-ttu-id="5b555-147">共享班次中的所有银箱由于与该班次的现金管理相关的活动被包括在同一个班次中。</span><span class="sxs-lookup"><span data-stu-id="5b555-147">All the cash drawers in a shared shift are included in the same shift for the purpose of activities that are related to cash management for that shift.</span></span> <span data-ttu-id="5b555-148">因此，班次的起始金额应包含共享班次中包含的所有银箱的所有现金之和。</span><span class="sxs-lookup"><span data-stu-id="5b555-148">Therefore, the starting amount for the shift should include the sum of all cash in all the cash drawers that are included in the shared shift.</span></span> <span data-ttu-id="5b555-149">同样，钱币清点应是共享班次中包含的所有银箱的所有现金之和。</span><span class="sxs-lookup"><span data-stu-id="5b555-149">Likewise, the tender declaration will be the sum of all the cash in all the cash drawers that are included in the shared shift.</span></span> <span data-ttu-id="5b555-150">**注意**：每个商店一次只能打开一个共享班次。</span><span class="sxs-lookup"><span data-stu-id="5b555-150">**Note:** Only one shared shift can be open at a time in each store.</span></span> <span data-ttu-id="5b555-151">可以在同一个商店中使用共享班次和独立班次。</span><span class="sxs-lookup"><span data-stu-id="5b555-151">Shared shifts and stand-alone shifts can be used in the same store.</span></span>

### <a name="set-up-a-shared-shift"></a><span data-ttu-id="5b555-152">设置共享班次</span><span class="sxs-lookup"><span data-stu-id="5b555-152">Set up a shared shift</span></span>

1.  <span data-ttu-id="5b555-153">单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **硬件配置文件**。</span><span class="sxs-lookup"><span data-stu-id="5b555-153">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span>
2.  <span data-ttu-id="5b555-154">选择要用于共享班次的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="5b555-154">Select the hardware profile to use for the shared shift.</span></span>
3.  <span data-ttu-id="5b555-155">在**开票人**快速选项卡上，将**共享班次开票人**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="5b555-155">On the **Drawer** FastTab, set the **Shared shift drawer** option to **Yes**.</span></span>
4.  <span data-ttu-id="5b555-156">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="5b555-156">Click **Save**.</span></span>
5.  <span data-ttu-id="5b555-157">单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **收银机**。</span><span class="sxs-lookup"><span data-stu-id="5b555-157">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span>
6.  <span data-ttu-id="5b555-158">选择需要共享班次的收银机，然后单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="5b555-158">Select the register that requires a shared shift, and then click **Edit**.</span></span>
7.  <span data-ttu-id="5b555-159">在**硬件配置文件**字段中，选择您在步骤 2 中选定的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="5b555-159">In the **Hardware profile** field, select the hardware profile that you selected in step 2.</span></span>
8.  <span data-ttu-id="5b555-160">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="5b555-160">Click **Save**.</span></span>
9.  <span data-ttu-id="5b555-161">单击**零售** &gt; **零售 IT** &gt; **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="5b555-161">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
10. <span data-ttu-id="5b555-162">选择 **1090** 配送计划，然后单击**立即运行**以将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="5b555-162">Select the **1090** distribution schedule, and then click **Run now** to synchronize changes to the POS.</span></span>

### <a name="use-a-shared-shift"></a><span data-ttu-id="5b555-163">使用共享班次</span><span class="sxs-lookup"><span data-stu-id="5b555-163">Use a shared shift</span></span>

1.  <span data-ttu-id="5b555-164">登录到 POS。</span><span class="sxs-lookup"><span data-stu-id="5b555-164">Sign in to the POS.</span></span>
2.  <span data-ttu-id="5b555-165">如果 POS 尚未连接到硬件工作站，选择**非开票人操作**，然后选择**选择硬件工作站**操作以使共享班次的硬件工作站处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="5b555-165">If the POS isn’t yet connected to a hardware station, select **Non-drawer operation**, and then select the **Select hardware station** operation to make a hardware station active for the shared shift.</span></span> <span data-ttu-id="5b555-166">仅当收银机第一次添加到共享班次环境时才需要此步骤。</span><span class="sxs-lookup"><span data-stu-id="5b555-166">This step is required only the first time that a register is added to a shared shift environment.</span></span>
3.  <span data-ttu-id="5b555-167">注销 POS，然后重新登录。</span><span class="sxs-lookup"><span data-stu-id="5b555-167">Sign out of the POS, and then sign back in.</span></span>
4.  <span data-ttu-id="5b555-168">选择**创建新班次**。</span><span class="sxs-lookup"><span data-stu-id="5b555-168">Select **Create a new shift**.</span></span>
5.  <span data-ttu-id="5b555-169">选择**声明初始金额**。</span><span class="sxs-lookup"><span data-stu-id="5b555-169">Select **Declare start amount**.</span></span>
6.  <span data-ttu-id="5b555-170">在属于共享班次的商店中输入所有银箱的起始金额，然后单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="5b555-170">Enter the starting amount of all the cash drawers in the store that are part of the shared shift, and then click **Save**.</span></span>
    -   <span data-ttu-id="5b555-171">若要将起始金额的一部分添加到每个后续的银箱，使用**选择硬件工作站**操作以使硬件工作站处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="5b555-171">To add part of the starting amount to each subsequent cash drawer, use the **Select hardware station** operation to make the hardware station active.</span></span>
    -   <span data-ttu-id="5b555-172">若要添加特定的银箱，使用**打开银箱**操作。</span><span class="sxs-lookup"><span data-stu-id="5b555-172">To add a till to a specific cash drawer, use the **Open drawer** operation.</span></span>
    -   <span data-ttu-id="5b555-173">继续，直到共享班次的所有银箱都有其起始金额的一部分。</span><span class="sxs-lookup"><span data-stu-id="5b555-173">Continue until all cash drawers in the shared shift have their part of the starting amount.</span></span>

7.  <span data-ttu-id="5b555-174">在一天结束时，打开每个银箱，取出现金。</span><span class="sxs-lookup"><span data-stu-id="5b555-174">At the end of the day, open each cash drawer, and remove the cash.</span></span>
8.  <span data-ttu-id="5b555-175">从最后一个银箱取出现金后，计算所有银箱中的所有现金。</span><span class="sxs-lookup"><span data-stu-id="5b555-175">After you’ve removed the cash from the last cash drawer, count all the cash from all the cash drawers.</span></span>
9.  <span data-ttu-id="5b555-176">使用**清点钱币**操作来清点共享班次中包含的所有银箱的现金总额。</span><span class="sxs-lookup"><span data-stu-id="5b555-176">Use the **Declare tender** operation to declare the total amount of cash from all the cash drawers that are included in the shared shift.</span></span>
10. <span data-ttu-id="5b555-177">使用**关闭班次**操作来关闭共享班次。</span><span class="sxs-lookup"><span data-stu-id="5b555-177">Use the **Close shift** operation to close the shared shift.</span></span>

## <a name="shift-operations"></a><span data-ttu-id="5b555-178">班次操作</span><span class="sxs-lookup"><span data-stu-id="5b555-178">Shift operations</span></span>
<span data-ttu-id="5b555-179">可以执行各个操作来更改班次状态或者增加或减少银箱中的金额。</span><span class="sxs-lookup"><span data-stu-id="5b555-179">Various actions can be taken to change the state of a shift or to increase or decrease the amount of money in the drawer.</span></span> <span data-ttu-id="5b555-180">下面的部分描述 Dynamics 365 for Retail Modern POS and Cloud POS 的这些班次操作。</span><span class="sxs-lookup"><span data-stu-id="5b555-180">The section below describes these shift operations for Dynamics 365 for Retail Modern POS and Cloud POS.</span></span>

<span data-ttu-id="5b555-181">**未结的班次**</span><span class="sxs-lookup"><span data-stu-id="5b555-181">**Open shift**</span></span>

<span data-ttu-id="5b555-182">POS 要求用户具有有效未结的班次来执行会生成财务交易（如销售、退货或客户订单）的任何操作。</span><span class="sxs-lookup"><span data-stu-id="5b555-182">POS requires that a user has an active, open shift to perform any operations that would result in a financial transaction such as a sale, return, or customer order.</span></span>  

<span data-ttu-id="5b555-183">在登录到 POS 时，系统将首先查看用户在当前的收银机上是否有可用的有效班次。</span><span class="sxs-lookup"><span data-stu-id="5b555-183">When logging into the POS, the system first checks to see if the user has an active shift available on the current register.</span></span> <span data-ttu-id="5b555-184">如果没有，用户随后可以选择打开新的班次、继续现有班次或继续登录“非银箱”模式，具体取决于系统配置及其权限。</span><span class="sxs-lookup"><span data-stu-id="5b555-184">If not, the user can then choose to open a new shift, resume an existing shift, or continue to login in “non-drawer” mode, depending on the system configuration and their permissions.</span></span>

<span data-ttu-id="5b555-185">**声明初始金额**</span><span class="sxs-lookup"><span data-stu-id="5b555-185">**Declare start amount**</span></span>

<span data-ttu-id="5b555-186">此操作通常是为新打开的班次执行的第一个操作。</span><span class="sxs-lookup"><span data-stu-id="5b555-186">This operation is often the first action that is taken a newly opened shift.</span></span> <span data-ttu-id="5b555-187">用户为班次指定银箱中的起始现金金额。</span><span class="sxs-lookup"><span data-stu-id="5b555-187">Users specify the starting cash amount in the drawer for the shift.</span></span> <span data-ttu-id="5b555-188">因为当关闭此金额的班次科目时将发生超交/不足计算，因此这一操作很重要。</span><span class="sxs-lookup"><span data-stu-id="5b555-188">This is important because the over/short calculation that occurs when closing a shift accounts for this amount.</span></span>

<span data-ttu-id="5b555-189">**浮动条目**</span><span class="sxs-lookup"><span data-stu-id="5b555-189">**Float entry**</span></span>

<span data-ttu-id="5b555-190">浮动条目是在有效班次中执行的非销售交易记录，它们将增加银箱中的现金金额。</span><span class="sxs-lookup"><span data-stu-id="5b555-190">Float entries are non-sales transactions that are performed in an active shift and they increase the amount of the cash in the drawer.</span></span> <span data-ttu-id="5b555-191">一个常见示例是，浮动条目会在银箱运行较少时增加对银箱的额外更改。</span><span class="sxs-lookup"><span data-stu-id="5b555-191">A common example of a float entry would be to add additional change to the drawer when it is running low.</span></span>

<span data-ttu-id="5b555-192">**取钱**</span><span class="sxs-lookup"><span data-stu-id="5b555-192">**Tender removal**</span></span>

<span data-ttu-id="5b555-193">取钱是在有效班次中执行的非销售交易记录，其将减少银箱中的现金金额。</span><span class="sxs-lookup"><span data-stu-id="5b555-193">Tender removals are non-sales transactions that are performed in an active shift to reduce the amount of the cash in the drawer.</span></span> <span data-ttu-id="5b555-194">此操作最常与不同班次的浮动条目结合使用。</span><span class="sxs-lookup"><span data-stu-id="5b555-194">This is most commonly used in conjunction with a float entry on a different shift.</span></span> <span data-ttu-id="5b555-195">例如，收银机 1 在更改后运行较少，收银机 2 的用户执行取钱来减少银箱金额。</span><span class="sxs-lookup"><span data-stu-id="5b555-195">For example, Register 1 is running low on change, so the user on Register 2 performs a tender removal to reduce the drawer amount.</span></span> <span data-ttu-id="5b555-196">收银机 1 的用户随后会执行浮动条目来增加其金额。</span><span class="sxs-lookup"><span data-stu-id="5b555-196">The user on Register 1 would then perform a float entry to increase their amount.</span></span>

<span data-ttu-id="5b555-197">**暂停班次**</span><span class="sxs-lookup"><span data-stu-id="5b555-197">**Suspend shift**</span></span>

<span data-ttu-id="5b555-198">用户可以暂停其有效班次以为其他用户释放当前收银机，或者将其班次移到不同的收银机（这通常称为“浮动钱盒”）。</span><span class="sxs-lookup"><span data-stu-id="5b555-198">Users can suspend their active shift to free up the current register for another user, or to move their shift to a different register (this is often referred to as a “floating till”).</span></span> 

<span data-ttu-id="5b555-199">暂停班次将阻止所有新交易记录或对班次的更改，直到恢复。</span><span class="sxs-lookup"><span data-stu-id="5b555-199">Suspending the shift prevents any new transactions or changes to the shift until it resumed.</span></span>

<span data-ttu-id="5b555-200">**恢复班次**</span><span class="sxs-lookup"><span data-stu-id="5b555-200">**Resume shift**</span></span>

<span data-ttu-id="5b555-201">此操作让用户可以恢复已没有有效班次的收银机上之前暂停的班次。</span><span class="sxs-lookup"><span data-stu-id="5b555-201">This operation allows a user to resume a previously suspended shift on a register that does not already have an active shift.</span></span>

<span data-ttu-id="5b555-202">**钱币清点**</span><span class="sxs-lookup"><span data-stu-id="5b555-202">**Tender declaration**</span></span>

<span data-ttu-id="5b555-203">钱币清点是用户指定银箱中当前的总金额时所执行的操作，通常在关闭班次前进行。</span><span class="sxs-lookup"><span data-stu-id="5b555-203">The tender declaration is action the user takes to specify the amount of total money currently in the drawer, most often before closing the shift.</span></span> <span data-ttu-id="5b555-204">这是相对于用于计算超交/不足金额的预期班次的值。</span><span class="sxs-lookup"><span data-stu-id="5b555-204">This is the value that is compared against the expected shift to calculate the over/short amount.</span></span>

<span data-ttu-id="5b555-205">**金库投箱**</span><span class="sxs-lookup"><span data-stu-id="5b555-205">**Safe drop**</span></span>

<span data-ttu-id="5b555-206">金库投箱可以在任何时间在有效班次执行。</span><span class="sxs-lookup"><span data-stu-id="5b555-206">Safe drops can be performed at any time on an active shift.</span></span> <span data-ttu-id="5b555-207">此操作从银箱中取出钱，以便它可以转移到更安全的位置（例如密室内的保险箱）。</span><span class="sxs-lookup"><span data-stu-id="5b555-207">This operation removes money from the drawer, so it can be transferred to a more secure location such as a safe in the back room.</span></span> <span data-ttu-id="5b555-208">为金库投箱记录的总金额仍包括在班次合计中，但不需要在钱币清点时盘点。</span><span class="sxs-lookup"><span data-stu-id="5b555-208">The total amount recorded for safe drops is still included in the shift totals, but doesn't need to be counted as part of the tender declaration.</span></span>

<span data-ttu-id="5b555-209">**银行投箱**</span><span class="sxs-lookup"><span data-stu-id="5b555-209">**Bank drop**</span></span>

<span data-ttu-id="5b555-210">与金库投箱一样，银行投箱也可在有效班次执行。</span><span class="sxs-lookup"><span data-stu-id="5b555-210">Like safe drops, bank drops are also performed on active shifts.</span></span> <span data-ttu-id="5b555-211">此操作取出班次的现金以为银行存款作准备。</span><span class="sxs-lookup"><span data-stu-id="5b555-211">This operation removes money from the shift to prepare for the bank deposit.</span></span>

<span data-ttu-id="5b555-212">**直接结束班次**</span><span class="sxs-lookup"><span data-stu-id="5b555-212">**Blind close shift**</span></span>

<span data-ttu-id="5b555-213">直接结束班次是不再有效，但尚未完全结束的班次。</span><span class="sxs-lookup"><span data-stu-id="5b555-213">A blind closed shift is a shift that is no longer active but has not been fully closed.</span></span> <span data-ttu-id="5b555-214">直接结束班次与暂停班次一样不能恢复，但如清点起始金额和钱币清点等过程可以在晚些时候或从不同收银机执行。</span><span class="sxs-lookup"><span data-stu-id="5b555-214">Blind closed shifts can't be resumed like a suspended shift, but procedures such as declare staring amounts and tender declarations can be performed at a later time or from a different register.</span></span>

<span data-ttu-id="5b555-215">直接结束班次通常用于为新用户或班次释放收银机，而不必先完全盘点、对帐和结束此班次。</span><span class="sxs-lookup"><span data-stu-id="5b555-215">Blind closed shifts are often used to free up a register for a new user or shift, without having to fully count, reconcile, and close this shift first.</span></span> 

<span data-ttu-id="5b555-216">**结束班次**</span><span class="sxs-lookup"><span data-stu-id="5b555-216">**Close shift**</span></span>

<span data-ttu-id="5b555-217">此操作计算班次合计、超交/不足金额，然后完成有效班次或直接结束班次。</span><span class="sxs-lookup"><span data-stu-id="5b555-217">This operation calculates shift totals, over/short amounts, and then finalizes an active or blind closed shift.</span></span> <span data-ttu-id="5b555-218">结束的班次不能恢复或修改。</span><span class="sxs-lookup"><span data-stu-id="5b555-218">Closed shifts cannot be resumed or modified.</span></span>  

<span data-ttu-id="5b555-219">**管理班次**</span><span class="sxs-lookup"><span data-stu-id="5b555-219">**Manage shifts**</span></span>

<span data-ttu-id="5b555-220">此操作允许用户查看商店的所有有效、暂停和直接结束班次。</span><span class="sxs-lookup"><span data-stu-id="5b555-220">This operation allows users to view all active, suspended, and blind closed shifts for the store.</span></span> <span data-ttu-id="5b555-221">根据其权限，用户可以执行其最终结转过程，如钱币清点和结束直接结束班次。</span><span class="sxs-lookup"><span data-stu-id="5b555-221">Depending on their permissions, users can perform their final closing procedures such as tender declaration and close shifts for blind closed shifts.</span></span> <span data-ttu-id="5b555-222">此操作还在极少数情况下允许用户查看和删除无效班次，如班次在切换脱机和联机方式后进入不良状态。</span><span class="sxs-lookup"><span data-stu-id="5b555-222">This operation will also allow users to view and delete invalid shifts in the rare event that a shift is left in a bad state after switching between offline and online modes.</span></span> <span data-ttu-id="5b555-223">这些无效的班次不包含对帐需要的任何财务信息或交易数据。</span><span class="sxs-lookup"><span data-stu-id="5b555-223">These invalid shifts do not contain any financial information or transactional data needed for reconciliation.</span></span> 


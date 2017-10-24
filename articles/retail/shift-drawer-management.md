---
title: "班次和银箱管理"
description: "本文介绍了如何设置和使用两种类型的零售销售点 (POS) 班次 - 共享和独立。 共享班次可由多个用户在多个位置使用，而独立班次一次只能由一个工作人员使用。"
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 72f73404f99330c3ff8b23dabed78477a0cd30cd
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="shift-and-cash-drawer-management"></a><span data-ttu-id="17c3d-104">班次和银箱管理</span><span class="sxs-lookup"><span data-stu-id="17c3d-104">Shift and cash drawer management</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="17c3d-105">本文介绍了如何设置和使用两种类型的零售销售点 (POS) 班次 - 共享和独立。</span><span class="sxs-lookup"><span data-stu-id="17c3d-105">This article explains how to set up and use the two types of retail point of sale (POS) shifts -  shared and stand-alone.</span></span> <span data-ttu-id="17c3d-106">共享班次可由多个用户在多个位置使用，而独立班次一次只能由一个工作人员使用。</span><span class="sxs-lookup"><span data-stu-id="17c3d-106">Shared shifts can be used by multiple users in multiple places, whereas stand-alone shifts can be used by only one worker at a time.</span></span>

<span data-ttu-id="17c3d-107">有两种类型的零售销售点 (POS) 班次︰独立和共享。</span><span class="sxs-lookup"><span data-stu-id="17c3d-107">There are two types of retail point of sale (POS) shifts: stand-alone and shared.</span></span> <span data-ttu-id="17c3d-108">独立班次一次只能由一名工作人员使用。</span><span class="sxs-lookup"><span data-stu-id="17c3d-108">Stand-alone shifts can be used by only one worker at a time.</span></span> <span data-ttu-id="17c3d-109">共享班次可以在多个位置由多个用户使用。</span><span class="sxs-lookup"><span data-stu-id="17c3d-109">Shared shifts can be used by multiple users in multiple places.</span></span> <span data-ttu-id="17c3d-110">因此，它们在商店内为多个工作人员有效地创建一个班次。</span><span class="sxs-lookup"><span data-stu-id="17c3d-110">Therefore, they effectively create a single shift for multiple workers in a store.</span></span>

## <a name="standalone-shifts"></a><span data-ttu-id="17c3d-111">独立班次</span><span class="sxs-lookup"><span data-stu-id="17c3d-111">Standalone shifts</span></span>
<span data-ttu-id="17c3d-112">独立班次在传统的固定 POS 情况中使用，在这种情况下，为每个 POS 收银机独立对帐现金。</span><span class="sxs-lookup"><span data-stu-id="17c3d-112">Stand-alone shifts are used in a traditional, fixed POS scenario, where cash is reconciled independently for each POS register.</span></span> <span data-ttu-id="17c3d-113">例如，在杂货店设置中，通常有几种固定的 POS 收银机，并分配给每个收银机一名出纳。</span><span class="sxs-lookup"><span data-stu-id="17c3d-113">For example, in a grocery store setting, there are typically several fixed POS registers, and a cashier is assigned to each register.</span></span> <span data-ttu-id="17c3d-114">在这种情况下，可能每个收银机使用一个独立班次，出纳负责收银机的钱盒或实际现金。</span><span class="sxs-lookup"><span data-stu-id="17c3d-114">In this case, each register likely uses a stand-alone shift, and the cashier is responsible for the till or physical cash at that register.</span></span> <span data-ttu-id="17c3d-115">独立班次在出纳的工作班次期间覆盖该收银机的所有活动。</span><span class="sxs-lookup"><span data-stu-id="17c3d-115">A stand-alone shift encompasses all the activity on that register during the cashier’s work shift.</span></span> <span data-ttu-id="17c3d-116">活动可以包括存入钱盒的未结金额，通过操作（如银行投箱和浮动条目）进行的所有现金取出和增加，以及班次结束时的钱币清点。</span><span class="sxs-lookup"><span data-stu-id="17c3d-116">Activities can include the opening amount that is deposited in the till, all removal and addition of cash through operations such as bank drops and float entry, and the tender declaration at the end of the shift.</span></span>

### <a name="set-up-a-stand-alone-shift"></a><span data-ttu-id="17c3d-117">设置独立班次</span><span class="sxs-lookup"><span data-stu-id="17c3d-117">Set up a stand-alone shift</span></span>

<span data-ttu-id="17c3d-118">在银箱级别指定独立班次。</span><span class="sxs-lookup"><span data-stu-id="17c3d-118">A stand-alone shift is designated at the cash drawer level.</span></span> <span data-ttu-id="17c3d-119">此过程说明如何在 POS 收银机上设置独立班次。</span><span class="sxs-lookup"><span data-stu-id="17c3d-119">This procedure explains how to set up a stand-alone shift on a POS register.</span></span>

1.  <span data-ttu-id="17c3d-120">单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **硬件配置文件**。</span><span class="sxs-lookup"><span data-stu-id="17c3d-120">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span>
2.  <span data-ttu-id="17c3d-121">选择要用于独立班次的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="17c3d-121">Select the hardware profile to use for the stand-alone shift.</span></span>
3.  <span data-ttu-id="17c3d-122">在**开票人**快速选项卡上，确认**共享班次开票人**选项设置为**无**。</span><span class="sxs-lookup"><span data-stu-id="17c3d-122">On the **Drawer** FastTab, confirm that the **Shared shift drawer** option is set to **No**.</span></span>
4.  <span data-ttu-id="17c3d-123">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="17c3d-123">Click **Save**.</span></span>
5.  <span data-ttu-id="17c3d-124">单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **收银机**。</span><span class="sxs-lookup"><span data-stu-id="17c3d-124">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span>
6.  <span data-ttu-id="17c3d-125">选择需要独立班次的收银机，然后单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="17c3d-125">Select the register that requires a stand-alone shift, and then click **Edit**.</span></span>
7.  <span data-ttu-id="17c3d-126">在**硬件配置文件**字段中，选择您在步骤 2 中选定的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="17c3d-126">In the **Hardware profile** field, select the hardware profile that you selected in step 2.</span></span>
8.  <span data-ttu-id="17c3d-127">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="17c3d-127">Click **Save**.</span></span>
9.  <span data-ttu-id="17c3d-128">单击**零售** &gt; **零售 IT** &gt; **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="17c3d-128">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
10. <span data-ttu-id="17c3d-129">选择 **1090** 配送计划，然后单击**立即运行**以将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="17c3d-129">Select the **1090** distribution schedule, and then click **Run now** to synchronize changes to the POS.</span></span>

### <a name="use-a-stand-alone-shift"></a><span data-ttu-id="17c3d-130">使用独立班次</span><span class="sxs-lookup"><span data-stu-id="17c3d-130">Use a stand-alone shift</span></span>

1.  <span data-ttu-id="17c3d-131">登录到 POS。</span><span class="sxs-lookup"><span data-stu-id="17c3d-131">Sign in to the POS.</span></span>
2.  <span data-ttu-id="17c3d-132">如果没有班次是打开的，选择**打开新班次**。</span><span class="sxs-lookup"><span data-stu-id="17c3d-132">If no shift is open, select **Open a new shift**.</span></span>
3.  <span data-ttu-id="17c3d-133">转到**清点初始金额**操作，并指定正在添加到钱盒以开始工作日的现金金额。</span><span class="sxs-lookup"><span data-stu-id="17c3d-133">Go to the **Declare start amount** operation, and specify the amount of cash that is being added to the till to start the work day.</span></span>
4.  <span data-ttu-id="17c3d-134">执行一些交易。</span><span class="sxs-lookup"><span data-stu-id="17c3d-134">Perform some transactions.</span></span>
5.  <span data-ttu-id="17c3d-135">在一天结束时，选择**清点钱币**清点银箱中剩余的现金金额。</span><span class="sxs-lookup"><span data-stu-id="17c3d-135">At the end of the day, select **Declare tender** to declare the amount of cash that remains in the cash drawer.</span></span>
6.  <span data-ttu-id="17c3d-136">输入现金金额，然后单击**保存**保存钱币清点结果。</span><span class="sxs-lookup"><span data-stu-id="17c3d-136">Enter the amount of cash, and then click **Save** to save the tender declaration.</span></span>
7.  <span data-ttu-id="17c3d-137">选择**结束班次**以关闭班次。</span><span class="sxs-lookup"><span data-stu-id="17c3d-137">Select **Close shift** to close the shift.</span></span>

<span data-ttu-id="17c3d-138">**注意︰**班次期间还提供其他操作，具体取决于使用的业务流程。</span><span class="sxs-lookup"><span data-stu-id="17c3d-138">**Note:** Other operations are available during the shift, depending on the business processes that are in place.</span></span> <span data-ttu-id="17c3d-139">**金库投箱**、**银行投箱**和**取钱**操作可用于在一天内或关闭班次之前从钱盒中取钱。</span><span class="sxs-lookup"><span data-stu-id="17c3d-139">The **Safe drop**, **Bank drop**, and **Tender removal** operations can be used to remove money from the till during the day or before the shift is closed.</span></span> <span data-ttu-id="17c3d-140">如果钱盒现金不足，**浮动条目**操作可用于向钱盒添加现金。</span><span class="sxs-lookup"><span data-stu-id="17c3d-140">If a till runs low on cash, the **Float entry** operation can be used to add cash to the till.</span></span>

## <a name="shared-shifts"></a><span data-ttu-id="17c3d-141">共享班次</span><span class="sxs-lookup"><span data-stu-id="17c3d-141">Shared shifts</span></span>
<span data-ttu-id="17c3d-142">共享班次用于以下环境：多个出纳共享银箱或一组银箱全天使用。</span><span class="sxs-lookup"><span data-stu-id="17c3d-142">A shared shift is used in an environment where multiple cashiers share a cash drawer or a set of cash drawers throughout the work day.</span></span> <span data-ttu-id="17c3d-143">通常情况下，共享班次用于移动 POS 环境。</span><span class="sxs-lookup"><span data-stu-id="17c3d-143">Typically, a shared shift is used in mobile POS environments.</span></span> <span data-ttu-id="17c3d-144">在移动环境中，不会为单个银箱分配每个出纳，且出纳不负责单个银箱。</span><span class="sxs-lookup"><span data-stu-id="17c3d-144">In a mobile environment, each cashier isn’t assigned to and responsible for a single cash drawer.</span></span> <span data-ttu-id="17c3d-145">相反，所有出纳都必须能够支付销售并添加现金到任何离他们最近的银箱。</span><span class="sxs-lookup"><span data-stu-id="17c3d-145">Instead, all cashiers must be able to tender a sale and add cash to whatever cash drawer is closest to them.</span></span> <span data-ttu-id="17c3d-146">在这种情况下，在出纳之间共享的银箱包括在共享班次中。</span><span class="sxs-lookup"><span data-stu-id="17c3d-146">In this scenario, the cash drawers that are shared among cashiers are included in a shared shift.</span></span> <span data-ttu-id="17c3d-147">共享班次中的所有银箱由于与该班次的现金管理相关的活动被包括在同一个班次中。</span><span class="sxs-lookup"><span data-stu-id="17c3d-147">All the cash drawers in a shared shift are included in the same shift for the purpose of activities that are related to cash management for that shift.</span></span> <span data-ttu-id="17c3d-148">因此，班次的起始金额应包含共享班次中包含的所有银箱的所有现金之和。</span><span class="sxs-lookup"><span data-stu-id="17c3d-148">Therefore, the starting amount for the shift should include the sum of all cash in all the cash drawers that are included in the shared shift.</span></span> <span data-ttu-id="17c3d-149">同样，钱币清点应是共享班次中包含的所有银箱的所有现金之和。</span><span class="sxs-lookup"><span data-stu-id="17c3d-149">Likewise, the tender declaration will be the sum of all the cash in all the cash drawers that are included in the shared shift.</span></span> <span data-ttu-id="17c3d-150">**注意**：每个商店一次只能打开一个共享班次。</span><span class="sxs-lookup"><span data-stu-id="17c3d-150">**Note:** Only one shared shift can be open at a time in each store.</span></span> <span data-ttu-id="17c3d-151">可以在同一个商店中使用共享班次和独立班次。</span><span class="sxs-lookup"><span data-stu-id="17c3d-151">Shared shifts and stand-alone shifts can be used in the same store.</span></span>

### <a name="set-up-a-shared-shift"></a><span data-ttu-id="17c3d-152">设置共享班次</span><span class="sxs-lookup"><span data-stu-id="17c3d-152">Set up a shared shift</span></span>

1.  <span data-ttu-id="17c3d-153">单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **硬件配置文件**。</span><span class="sxs-lookup"><span data-stu-id="17c3d-153">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span>
2.  <span data-ttu-id="17c3d-154">选择要用于共享班次的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="17c3d-154">Select the hardware profile to use for the shared shift.</span></span>
3.  <span data-ttu-id="17c3d-155">在**开票人**快速选项卡上，将**共享班次开票人**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="17c3d-155">On the **Drawer** FastTab, set the **Shared shift drawer** option to **Yes**.</span></span>
4.  <span data-ttu-id="17c3d-156">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="17c3d-156">Click **Save**.</span></span>
5.  <span data-ttu-id="17c3d-157">单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **收银机**。</span><span class="sxs-lookup"><span data-stu-id="17c3d-157">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span>
6.  <span data-ttu-id="17c3d-158">选择需要共享班次的收银机，然后单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="17c3d-158">Select the register that requires a shared shift, and then click **Edit**.</span></span>
7.  <span data-ttu-id="17c3d-159">在**硬件配置文件**字段中，选择您在步骤 2 中选定的硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="17c3d-159">In the **Hardware profile** field, select the hardware profile that you selected in step 2.</span></span>
8.  <span data-ttu-id="17c3d-160">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="17c3d-160">Click **Save**.</span></span>
9.  <span data-ttu-id="17c3d-161">单击**零售** &gt; **零售 IT** &gt; **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="17c3d-161">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
10. <span data-ttu-id="17c3d-162">选择 **1090** 配送计划，然后单击**立即运行**以将更改同步到 POS。</span><span class="sxs-lookup"><span data-stu-id="17c3d-162">Select the **1090** distribution schedule, and then click **Run now** to synchronize changes to the POS.</span></span>

### <a name="use-a-shared-shift"></a><span data-ttu-id="17c3d-163">使用共享班次</span><span class="sxs-lookup"><span data-stu-id="17c3d-163">Use a shared shift</span></span>

1.  <span data-ttu-id="17c3d-164">登录到 POS。</span><span class="sxs-lookup"><span data-stu-id="17c3d-164">Sign in to the POS.</span></span>
2.  <span data-ttu-id="17c3d-165">如果 POS 尚未连接到硬件工作站，选择**非开票人操作**，然后选择**选择硬件工作站**操作以使共享班次的硬件工作站处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="17c3d-165">If the POS isn’t yet connected to a hardware station, select **Non-drawer operation**, and then select the **Select hardware station** operation to make a hardware station active for the shared shift.</span></span> <span data-ttu-id="17c3d-166">仅当收银机第一次添加到共享班次环境时才需要此步骤。</span><span class="sxs-lookup"><span data-stu-id="17c3d-166">This step is required only the first time that a register is added to a shared shift environment.</span></span>
3.  <span data-ttu-id="17c3d-167">注销 POS，然后重新登录。</span><span class="sxs-lookup"><span data-stu-id="17c3d-167">Sign out of the POS, and then sign back in.</span></span>
4.  <span data-ttu-id="17c3d-168">选择**创建新班次**。</span><span class="sxs-lookup"><span data-stu-id="17c3d-168">Select **Create a new shift**.</span></span>
5.  <span data-ttu-id="17c3d-169">选择**声明初始金额**。</span><span class="sxs-lookup"><span data-stu-id="17c3d-169">Select **Declare start amount**.</span></span>
6.  <span data-ttu-id="17c3d-170">在属于共享班次的商店中输入所有银箱的起始金额，然后单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="17c3d-170">Enter the starting amount of all the cash drawers in the store that are part of the shared shift, and then click **Save**.</span></span>
    -   <span data-ttu-id="17c3d-171">若要将起始金额的一部分添加到每个后续的银箱，使用**选择硬件工作站**操作以使硬件工作站处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="17c3d-171">To add part of the starting amount to each subsequent cash drawer, use the **Select hardware station** operation to make the hardware station active.</span></span>
    -   <span data-ttu-id="17c3d-172">若要添加特定的银箱，使用**打开银箱**操作。</span><span class="sxs-lookup"><span data-stu-id="17c3d-172">To add a till to a specific cash drawer, use the **Open drawer** operation.</span></span>
    -   <span data-ttu-id="17c3d-173">继续，直到共享班次的所有银箱都有其起始金额的一部分。</span><span class="sxs-lookup"><span data-stu-id="17c3d-173">Continue until all cash drawers in the shared shift have their part of the starting amount.</span></span>

7.  <span data-ttu-id="17c3d-174">在一天结束时，打开每个银箱，取出现金。</span><span class="sxs-lookup"><span data-stu-id="17c3d-174">At the end of the day, open each cash drawer, and remove the cash.</span></span>
8.  <span data-ttu-id="17c3d-175">从最后一个银箱取出现金后，计算所有银箱中的所有现金。</span><span class="sxs-lookup"><span data-stu-id="17c3d-175">After you’ve removed the cash from the last cash drawer, count all the cash from all the cash drawers.</span></span>
9.  <span data-ttu-id="17c3d-176">使用**清点钱币**操作来清点共享班次中包含的所有银箱的现金总额。</span><span class="sxs-lookup"><span data-stu-id="17c3d-176">Use the **Declare tender** operation to declare the total amount of cash from all the cash drawers that are included in the shared shift.</span></span>
10. <span data-ttu-id="17c3d-177">使用**关闭班次**操作来关闭共享班次。</span><span class="sxs-lookup"><span data-stu-id="17c3d-177">Use the **Close shift** operation to close the shared shift.</span></span>





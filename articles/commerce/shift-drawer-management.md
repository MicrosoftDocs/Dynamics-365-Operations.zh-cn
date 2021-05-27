---
title: 班次和银箱管理
description: 此主题介绍如何在商业销售点 (POS) 中设置和使用班次。
author: jblucher
ms.date: 05/10/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d9d36bcb05cf466d34d921d8cd5266b6c12a63d7
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6028243"
---
# <a name="shift-and-cash-drawer-management"></a><span data-ttu-id="6f162-103">班次和银箱管理</span><span class="sxs-lookup"><span data-stu-id="6f162-103">Shift and cash drawer management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6f162-104">此主题介绍如何在商业销售点 (POS) 中设置和使用班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-104">This topic explains how to set up and use shifts in Commerce point of sale (POS).</span></span>

<span data-ttu-id="6f162-105">在 Dynamics 365 Commerce 中，*班次* 描述两个数据点之间对 POS 交易记录数据和活动的收集。</span><span class="sxs-lookup"><span data-stu-id="6f162-105">In Dynamics 365 Commerce, the term *shift* describes the collection of POS transactional data and activities between two points in time.</span></span> <span data-ttu-id="6f162-106">对于每个班次，将把预计金额与盘点和清点的金额进行比较。</span><span class="sxs-lookup"><span data-stu-id="6f162-106">For each shift, the amount of money that is expected is compared against the amount that was counted and declared.</span></span>

<span data-ttu-id="6f162-107">班次通常在营业时间开始时打开。</span><span class="sxs-lookup"><span data-stu-id="6f162-107">Typically, shifts are opened at the start of the business day.</span></span> <span data-ttu-id="6f162-108">此时用户清点银箱内的初始金额。</span><span class="sxs-lookup"><span data-stu-id="6f162-108">At that point, a user declares the starting amount that the cash drawer contains.</span></span> <span data-ttu-id="6f162-109">然后开展全天的销售交易。</span><span class="sxs-lookup"><span data-stu-id="6f162-109">Sales transactions are then performed throughout the day.</span></span> <span data-ttu-id="6f162-110">最后，日结时盘点银箱并清点结束金额。</span><span class="sxs-lookup"><span data-stu-id="6f162-110">Finally, at the end of the day, the drawer is counted, and the closing amounts are declared.</span></span> <span data-ttu-id="6f162-111">班次关闭，生成 Z 报表。</span><span class="sxs-lookup"><span data-stu-id="6f162-111">The shift is closed, and a Z report is generated.</span></span> <span data-ttu-id="6f162-112">Z 报表指示金额是否超交或不足。</span><span class="sxs-lookup"><span data-stu-id="6f162-112">The Z report indicates whether there is an overage or shortage.</span></span>

## <a name="typical-shift-scenarios"></a><span data-ttu-id="6f162-113">典型班次方案</span><span class="sxs-lookup"><span data-stu-id="6f162-113">Typical shift scenarios</span></span>

<span data-ttu-id="6f162-114">Commerce 提供多个配置选项和 POS 操作，为 POS 的各种日结业务流程提供支持。</span><span class="sxs-lookup"><span data-stu-id="6f162-114">Commerce provides several configuration options and POS operations to support a wide range of end-of-day business processes for the POS.</span></span> <span data-ttu-id="6f162-115">此节介绍一些典型班次方案。</span><span class="sxs-lookup"><span data-stu-id="6f162-115">This section describes some typical shift scenarios.</span></span>

### <a name="fixed-till"></a><span data-ttu-id="6f162-116">固定钱盒</span><span class="sxs-lookup"><span data-stu-id="6f162-116">Fixed till</span></span>

<span data-ttu-id="6f162-117">传统上，此方案用得最多。</span><span class="sxs-lookup"><span data-stu-id="6f162-117">Traditionally, this scenario has been used most often.</span></span> <span data-ttu-id="6f162-118">现在仍在广泛使用。</span><span class="sxs-lookup"><span data-stu-id="6f162-118">It's still extensively used.</span></span> <span data-ttu-id="6f162-119">在“固定钱盒”班次中，班次和钱盒与具体收银机关联。</span><span class="sxs-lookup"><span data-stu-id="6f162-119">In a "fixed till" shift, the shift and till are associated with a specific register.</span></span> <span data-ttu-id="6f162-120">不会从一台收银机转移到另一台收银机。</span><span class="sxs-lookup"><span data-stu-id="6f162-120">They aren't moved from one register to another.</span></span> <span data-ttu-id="6f162-121">“固定钱盒”班次可以供一位用户使用，也可以由多位用户共享。</span><span class="sxs-lookup"><span data-stu-id="6f162-121">A "fixed till" shift can be used by a single user or shared among multiple users.</span></span> <span data-ttu-id="6f162-122">“固定钱盒”班次不需要任何特殊配置。</span><span class="sxs-lookup"><span data-stu-id="6f162-122">"Fixed till" shifts don't require any special configuration.</span></span>

### <a name="floating-till"></a><span data-ttu-id="6f162-123">浮动钱盒</span><span class="sxs-lookup"><span data-stu-id="6f162-123">Floating till</span></span>

<span data-ttu-id="6f162-124">在“浮动钱盒”班次中，班次和银箱可以从一台收银机转移到另一台收银机。</span><span class="sxs-lookup"><span data-stu-id="6f162-124">In a "floating till" shift, the shift and cash drawer can be moved from one register to another.</span></span> <span data-ttu-id="6f162-125">尽管一台收银机的每个钱箱只能有一个有效班次，但是可以暂停班次，以后再在另一台收银机上恢复。</span><span class="sxs-lookup"><span data-stu-id="6f162-125">Although a register can have only one active shift per cash drawer, shifts can be suspended and then resumed later or on a different register.</span></span>

<span data-ttu-id="6f162-126">例如，一家商店有两台收银机。</span><span class="sxs-lookup"><span data-stu-id="6f162-126">For example, a store has two registers.</span></span> <span data-ttu-id="6f162-127">每个收银机在每天开始时收银机开启新的班次并提供起始金额时打开。</span><span class="sxs-lookup"><span data-stu-id="6f162-127">Each register is opened at the start of the day when the cashier opens a new shift and provides the starting amount.</span></span> <span data-ttu-id="6f162-128">一台收银机准备好暂停工作时，收银员可以暂停自己的班次，将钱盒从银箱中取出。</span><span class="sxs-lookup"><span data-stu-id="6f162-128">When one cashier is ready to take a break, that cashier suspends their shift and removes the till from the cash drawer.</span></span> <span data-ttu-id="6f162-129">然后，这台收银机就可以供其他收银员使用。</span><span class="sxs-lookup"><span data-stu-id="6f162-129">That register then becomes available to other cashiers.</span></span> <span data-ttu-id="6f162-130">其他收银员可以登录这台收银机并打开自己的班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-130">Another cashier can sign in to and open their own shift on the register.</span></span> <span data-ttu-id="6f162-131">定义为收银员休息结束后，可以在其他收银机之一可用时回复自己的班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-131">After the first cashier's break has ended, that cashier can resume their shift when one of the other registers becomes available.</span></span> <span data-ttu-id="6f162-132">“浮动钱盒”班次不需要任何特殊配置或权限。</span><span class="sxs-lookup"><span data-stu-id="6f162-132">"Floating till" shifts don't require any special configuration or permission.</span></span>

### <a name="single-user"></a><span data-ttu-id="6f162-133">单个用户</span><span class="sxs-lookup"><span data-stu-id="6f162-133">Single user</span></span>

<span data-ttu-id="6f162-134">许多零售商倾向一个班次只有一位用户，以确保银箱中现金最高级别的会计责任。</span><span class="sxs-lookup"><span data-stu-id="6f162-134">Many retailers prefer to allow only one user per shift, to help guarantee the highest level of accountability for the cash in the cash drawer.</span></span> <span data-ttu-id="6f162-135">如果仅允许一位用户使用与某个班次关联的钱盒，则该用户单独负责任何差异。</span><span class="sxs-lookup"><span data-stu-id="6f162-135">If only one user is allowed to use the till that is associated with a shift, that user can be held solely responsible for any discrepancies.</span></span> <span data-ttu-id="6f162-136">如果多位用户使用一个班次，则很难确定谁出错，或者谁可能试图从钱盒偷钱。</span><span class="sxs-lookup"><span data-stu-id="6f162-136">If more than one user uses a shift, it's difficult to determine who made an error, or who might be trying to steal from the till.</span></span>

### <a name="multiple-users"></a><span data-ttu-id="6f162-137">多用户</span><span class="sxs-lookup"><span data-stu-id="6f162-137">Multiple users</span></span>

<span data-ttu-id="6f162-138">某些零售商愿意牺牲单一用户班次的会计责任级别，允许多位用户共用一个班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-138">Some retailers are willing to sacrifice the level of accountability that single-user shifts provide and to allow more than one user per shift.</span></span> <span data-ttu-id="6f162-139">如果用户数量比可用收银机多，对灵活性和速度的需要比潜在损失更重要，通常使用此方法。</span><span class="sxs-lookup"><span data-stu-id="6f162-139">This approach is typical when there are more users than available registers, and the need for flexibility and speed outweighs the potential for loss.</span></span> <span data-ttu-id="6f162-140">以下情况也很常见：商店经理没有自己的班次，但是可以根据需要使用任何下属收银员的班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-140">It's also typical when store managers don't have their own shifts but can, as required, use the shifts of any of their cashiers.</span></span> <span data-ttu-id="6f162-141">用户若要登录并使用另一位用户打开的班次，必须拥有 **允许多班次登录** POS 权限。</span><span class="sxs-lookup"><span data-stu-id="6f162-141">To sign in to and use a shift that was opened by another user, a user must have the **Allow multiple shift logon** POS permission.</span></span>

### <a name="shared-shift"></a><span data-ttu-id="6f162-142">共享班次</span><span class="sxs-lookup"><span data-stu-id="6f162-142">Shared shift</span></span>

<span data-ttu-id="6f162-143">“共享班次”配置让零售商可以使多台收银机、多个银箱和多位用户共用一个班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-143">A "shared shift" configuration lets retailers have a single shift across multiple registers, cash drawers, and users.</span></span> <span data-ttu-id="6f162-144">如果使用共享班次，则所有银箱共用一个起始金额和一个结束金额。</span><span class="sxs-lookup"><span data-stu-id="6f162-144">A shared shift has a single starting amount and a single closing amount that are summarized across all cash drawers.</span></span> <span data-ttu-id="6f162-145">如果使用移动设备，则共享班次最为典型。</span><span class="sxs-lookup"><span data-stu-id="6f162-145">Shared shifts are most typical when mobile devices are used.</span></span> <span data-ttu-id="6f162-146">在此方案中，不为每位收银员保留一个单独的银箱。</span><span class="sxs-lookup"><span data-stu-id="6f162-146">In this scenario, a separate cash drawer isn't reserved for each register.</span></span> <span data-ttu-id="6f162-147">相反，所有收银机可以共用一个银箱。</span><span class="sxs-lookup"><span data-stu-id="6f162-147">Instead, all registers can share one cash drawer.</span></span>

<span data-ttu-id="6f162-148">若要在商店中使用共享班次，必须在 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 硬件配置文件 \> 银箱** 中将银箱配置为“共享班次银箱”。</span><span class="sxs-lookup"><span data-stu-id="6f162-148">For shared shifts to be used in a store, the cash drawer must be configured as a "shared shift drawer" at **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Hardware profiles \> Drawer**.</span></span> <span data-ttu-id="6f162-149">此外，用户还必须拥有共享班次权限（“允许管理共享班次”和“允许使用共享班次”）之一或全部。</span><span class="sxs-lookup"><span data-stu-id="6f162-149">Additionally, users must have one or both of the shared shift permissions (Allow manage shared shift and Allow use shared shift).</span></span>

> [!NOTE]
> <span data-ttu-id="6f162-150">每个商店一次只能打开一个共享班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-150">Only one shared shift can be open at a time in each store.</span></span> <span data-ttu-id="6f162-151">可以在同一个商店中使用共享班次和独立班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-151">Shared shifts and stand-alone shifts can be used in the same store.</span></span>

## <a name="shift-and-drawer-operations"></a><span data-ttu-id="6f162-152">班次和银箱操作</span><span class="sxs-lookup"><span data-stu-id="6f162-152">Shift and drawer operations</span></span>

<span data-ttu-id="6f162-153">可以执行各个操作来更改班次状态或者增加或减少银箱中的金额。</span><span class="sxs-lookup"><span data-stu-id="6f162-153">Various operations can be performed to change the state of a shift, or to increase or decrease the amount of money in the cash drawer.</span></span> <span data-ttu-id="6f162-154">此部分描述 Modern POS 和 Cloud POS 的这些班次操作。</span><span class="sxs-lookup"><span data-stu-id="6f162-154">This section describes these shift operations for Modern POS and Cloud POS.</span></span>

### <a name="open-shift"></a><span data-ttu-id="6f162-155">未结的班次</span><span class="sxs-lookup"><span data-stu-id="6f162-155">Open shift</span></span>

<span data-ttu-id="6f162-156">POS 要求用户具有有效未结的班次来执行会生成财务交易（如销售、退货或客户订单）的任何操作。</span><span class="sxs-lookup"><span data-stu-id="6f162-156">The POS requires that users have an active, open shift in order to perform any operations that will produce a financial transaction, such as a sale, return, or customer order.</span></span>

<span data-ttu-id="6f162-157">用户登录 POS 时，系统首先验证该用户在当前收银机上是否有有效班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-157">When a user signs in to the POS, the system first verifies whether an active shift is available for that user on the current register.</span></span> <span data-ttu-id="6f162-158">如果没有有效班次，用户随后可以选择打开新的班次、继续现有班次或以“非银箱”模式登录，具体取决于系统配置和用户的权限。</span><span class="sxs-lookup"><span data-stu-id="6f162-158">If an active shift isn't available, the user can open a new shift, resume an existing shift, or sign in in "non-drawer" mode, depending on the system configuration and the user's permissions.</span></span>

### <a name="declare-start-amount"></a><span data-ttu-id="6f162-159">声明初始金额</span><span class="sxs-lookup"><span data-stu-id="6f162-159">Declare start amount</span></span>

<span data-ttu-id="6f162-160">此操作通常是为新打开的班次执行的第一个操作。</span><span class="sxs-lookup"><span data-stu-id="6f162-160">This operation is often the first operation that is performed for a newly opened shift.</span></span> <span data-ttu-id="6f162-161">对于此操作，用户为班次指定银箱中的起始现金金额。</span><span class="sxs-lookup"><span data-stu-id="6f162-161">For this operation, users specify the starting cash amount in the cash drawer for the shift.</span></span> <span data-ttu-id="6f162-162">此操作非常重要，因为班次结束时的超交/不足计算视为起始金额。</span><span class="sxs-lookup"><span data-stu-id="6f162-162">This operation is important because the overage/shortage calculation that occurs when a shift is closed considers the start amount.</span></span>

### <a name="float-entry"></a><span data-ttu-id="6f162-163">浮动条目</span><span class="sxs-lookup"><span data-stu-id="6f162-163">Float entry</span></span>

<span data-ttu-id="6f162-164">*浮动录入* 是在有效班次中执行的非销售交易，它们将增加银箱中的现金金额。</span><span class="sxs-lookup"><span data-stu-id="6f162-164">*Float entries* are non-sales transactions that are performed in an active shift to increase the amount of cash in the cash drawer.</span></span> <span data-ttu-id="6f162-165">一个典型示例是，浮动录入是在银箱运行较少时增加对银箱的额外更改的交易。</span><span class="sxs-lookup"><span data-stu-id="6f162-165">A typical example of a float entry is a transaction to add additional change to the drawer when it's running low.</span></span>

### <a name="tender-removal"></a><span data-ttu-id="6f162-166">取钱</span><span class="sxs-lookup"><span data-stu-id="6f162-166">Tender removal</span></span>

<span data-ttu-id="6f162-167">*取钱* 是在有效班次中执行的非销售交易，其将减少银箱中的现金金额。</span><span class="sxs-lookup"><span data-stu-id="6f162-167">*Tender removals* are non-sales transactions that are performed in an active shift to reduce the amount of cash in the cash drawer.</span></span> <span data-ttu-id="6f162-168">此操作通常与不同班次的浮动录入操作结合使用。</span><span class="sxs-lookup"><span data-stu-id="6f162-168">This operation is most often used in conjunction with a Float entry operation on a different shift.</span></span> <span data-ttu-id="6f162-169">例如，因为收银机 1 在更改后运行较少，收银机 2 的用户执行取钱来减少自己的银箱金额。</span><span class="sxs-lookup"><span data-stu-id="6f162-169">For example, because register 1 is running low on change, the user on register 2 does a tender removal to reduce the amount in their cash drawer.</span></span> <span data-ttu-id="6f162-170">然后，收银机 1 的用户执行浮动录入以增加自己银箱中的金额。</span><span class="sxs-lookup"><span data-stu-id="6f162-170">The user on register 1 then does a float entry to increase the amount in their cash drawer.</span></span>

### <a name="suspend-shift"></a><span data-ttu-id="6f162-171">暂停班次</span><span class="sxs-lookup"><span data-stu-id="6f162-171">Suspend shift</span></span>

<span data-ttu-id="6f162-172">用户可以暂停其有效班次以为其他用户释放当前收银机，或者将其班次移到不同的收银机（在此情况下，班次通常称为“浮动钱盒”班次）。</span><span class="sxs-lookup"><span data-stu-id="6f162-172">Users can suspend their active shift to free up the current register for another user, or to move their shift to a different register (in this case, the shift is often referred to as a "floating till" shift).</span></span>

<span data-ttu-id="6f162-173">暂停班次将阻止所有新交易记录或对班次的更改，直到恢复。</span><span class="sxs-lookup"><span data-stu-id="6f162-173">Suspension of a shift prevents any new transactions or changes to the shift until it's resumed.</span></span>

### <a name="resume-shift"></a><span data-ttu-id="6f162-174">恢复班次</span><span class="sxs-lookup"><span data-stu-id="6f162-174">Resume shift</span></span>

<span data-ttu-id="6f162-175">此操作让用户可以恢复已没有有效班次的任何收银机上之前暂停的班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-175">This operation lets users resume a previously suspended shift on any register that doesn't already have an active shift.</span></span>

### <a name="tender-declaration"></a><span data-ttu-id="6f162-176">钱币清点</span><span class="sxs-lookup"><span data-stu-id="6f162-176">Tender declaration</span></span>

<span data-ttu-id="6f162-177">执行此操作是为了指定银箱中的现有现金总额。</span><span class="sxs-lookup"><span data-stu-id="6f162-177">This operation is performed to specify the total amount of money that is currently in the cash drawer.</span></span> <span data-ttu-id="6f162-178">用户经常在结束班次之前执行此操作。</span><span class="sxs-lookup"><span data-stu-id="6f162-178">Users most often perform this operation before they close a shift.</span></span> <span data-ttu-id="6f162-179">指定的金额是相对于用于计算超交/不足金额的预期班次金额。</span><span class="sxs-lookup"><span data-stu-id="6f162-179">The specified amount is compared against the expected shift amount to calculate the overage/shortage amount.</span></span>

### <a name="safe-drop"></a><span data-ttu-id="6f162-180">金库投箱</span><span class="sxs-lookup"><span data-stu-id="6f162-180">Safe drop</span></span>

<span data-ttu-id="6f162-181">金库投箱可以在任何时间在有效班次执行。</span><span class="sxs-lookup"><span data-stu-id="6f162-181">Safe drops can be done on an active shift at any time.</span></span> <span data-ttu-id="6f162-182">此操作从银箱中取出钱，以便将其转移到更安全的位置（例如密室内的保险箱）。</span><span class="sxs-lookup"><span data-stu-id="6f162-182">This operation removes money from the cash drawer so that it can be transferred to a more secure location, such as a safe in the back room.</span></span> <span data-ttu-id="6f162-183">为金库投箱记录的总金额包括在班次合计中，但不需要在钱币清点时盘点。</span><span class="sxs-lookup"><span data-stu-id="6f162-183">The total amount that is recorded for safe drops is included in shift totals, but it doesn't have to be counted as part of the tender declaration.</span></span>

### <a name="bank-drop"></a><span data-ttu-id="6f162-184">银行投箱</span><span class="sxs-lookup"><span data-stu-id="6f162-184">Bank drop</span></span>

<span data-ttu-id="6f162-185">与金库投箱一样，银行投箱可以在有效班次执行。</span><span class="sxs-lookup"><span data-stu-id="6f162-185">Like safe drops, bank drops are done on active shifts.</span></span> <span data-ttu-id="6f162-186">此操作取出班次的现金以为银行存款作准备。</span><span class="sxs-lookup"><span data-stu-id="6f162-186">This operation removes money from the shift to prepare for the bank deposit.</span></span>

### <a name="blind-close-shift"></a><span data-ttu-id="6f162-187">直接结束班次</span><span class="sxs-lookup"><span data-stu-id="6f162-187">Blind close shift</span></span>

<span data-ttu-id="6f162-188">*直接结束班次* 不再处于有效状态，但是尚未完全结束。</span><span class="sxs-lookup"><span data-stu-id="6f162-188">*Blind-closed shifts* are no longer active but haven't been fully closed.</span></span> <span data-ttu-id="6f162-189">与暂停班次不同，不能恢复直接结束班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-189">Unlike suspended shifts, blind-closed shifts can't be resumed.</span></span> <span data-ttu-id="6f162-190">但是，可以在以后或从其他收银机对其执行操作，如“清点起始金额”和“钱币清点”。</span><span class="sxs-lookup"><span data-stu-id="6f162-190">However, operations such as Declare start amount and Tender declaration can be performed on them later or from a different register.</span></span>

<span data-ttu-id="6f162-191">直接结束班次通常用于为新用户或班次释放收银机，而不必先完全盘点、对帐和结束此班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-191">Blind-closed shifts are often used to free up a register for a new user or shift without first having to fully count, reconcile, and close the shift.</span></span>

### <a name="close-shift"></a><span data-ttu-id="6f162-192">结束班次</span><span class="sxs-lookup"><span data-stu-id="6f162-192">Close shift</span></span>

<span data-ttu-id="6f162-193">此操作计算班次合计和超交/不足金额，然后完成有效班次或直接结束班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-193">This operation calculates shift totals and overage/shortage amounts, and then finalizes an active or blind-closed shift.</span></span> <span data-ttu-id="6f162-194">还将为班次打印 Z 报表，具体取决于用户的权限。</span><span class="sxs-lookup"><span data-stu-id="6f162-194">Depending on the user's permissions, a Z report is also printed for the shift.</span></span> <span data-ttu-id="6f162-195">结束的班次不能恢复或修改。</span><span class="sxs-lookup"><span data-stu-id="6f162-195">Closed shifts can't be resumed or modified.</span></span>

### <a name="print-x"></a><span data-ttu-id="6f162-196">打印 X</span><span class="sxs-lookup"><span data-stu-id="6f162-196">Print X</span></span>

<span data-ttu-id="6f162-197">此操作为当前有效班次生成和打印 X 报表。</span><span class="sxs-lookup"><span data-stu-id="6f162-197">This operation generates and prints an X report for the current active shift.</span></span>

### <a name="reprint-z"></a><span data-ttu-id="6f162-198">重印 Z</span><span class="sxs-lookup"><span data-stu-id="6f162-198">Reprint Z</span></span>

<span data-ttu-id="6f162-199">此操作重新打印结束班次时系统生成的最后一个 Z 报表。</span><span class="sxs-lookup"><span data-stu-id="6f162-199">This operation reprints the last Z report that the system generated when a shift was closed.</span></span>

### <a name="manage-shifts"></a><span data-ttu-id="6f162-200">管理班次</span><span class="sxs-lookup"><span data-stu-id="6f162-200">Manage shifts</span></span>

<span data-ttu-id="6f162-201">用户可通过此操作查看商店的所有有效、暂停和直接结束班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-201">This operation lets users view all active, suspended, and blind-closed shifts for the store.</span></span> <span data-ttu-id="6f162-202">根据其权限，用户可以执行其最终结转过程，如钱币清点和结束直接结束班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-202">Depending on their permissions, users can perform their final closing procedures, such as Tender declaration and Close shift operations for blind-closed shifts.</span></span> <span data-ttu-id="6f162-203">在极少数情况下，用户还可以通过此操作查看和删除无效班次，如班次在切换脱机和联机方式后进入不良状态。</span><span class="sxs-lookup"><span data-stu-id="6f162-203">This operation also lets users view and delete invalid shifts, in the rare event that shifts are left in a bad state after a switch between offline and online modes.</span></span> <span data-ttu-id="6f162-204">这些无效的班次不包含对帐需要的任何财务信息或交易数据。</span><span class="sxs-lookup"><span data-stu-id="6f162-204">These invalid shifts don't contain any financial information or transactional data that is required for reconciliation.</span></span>

## <a name="shift-and-drawer-permissions"></a><span data-ttu-id="6f162-205">班次和银箱管理</span><span class="sxs-lookup"><span data-stu-id="6f162-205">Shift and drawer permissions</span></span>

<span data-ttu-id="6f162-206">以下 POS 权限影响用户在各种方案中可执行的操作和不可执行的操作：</span><span class="sxs-lookup"><span data-stu-id="6f162-206">The following POS permissions affect what a user can and can't do in various scenarios:</span></span>

- <span data-ttu-id="6f162-207">**允许直接结束**</span><span class="sxs-lookup"><span data-stu-id="6f162-207">**Allow blind close**</span></span>
- <span data-ttu-id="6f162-208">**允许打印 X 报表**</span><span class="sxs-lookup"><span data-stu-id="6f162-208">**Allow X-report printing**</span></span>
- <span data-ttu-id="6f162-209">**允许打印 Z 报表**</span><span class="sxs-lookup"><span data-stu-id="6f162-209">**Allow Z-report printing**</span></span>
- <span data-ttu-id="6f162-210">**允许钱币清点**</span><span class="sxs-lookup"><span data-stu-id="6f162-210">**Allow tender declaration**</span></span>
- <span data-ttu-id="6f162-211">**允许浮动清点**</span><span class="sxs-lookup"><span data-stu-id="6f162-211">**Allow floating declaration**</span></span>
- <span data-ttu-id="6f162-212">**无销售时开银箱**</span><span class="sxs-lookup"><span data-stu-id="6f162-212">**Open drawer without sale**</span></span>
- <span data-ttu-id="6f162-213">**允许多班次登录** – 此权限允许用户登录和使用其他用户打开的班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-213">**Allow multiple shift logon** – This permission allows the user to sign in to and use a shift that a different user opened.</span></span> <span data-ttu-id="6f162-214">没有此权限的用户只能登录和使用自己打开的班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-214">Users who don't have this permission can sign in to and use only shifts that they have opened.</span></span>
- <span data-ttu-id="6f162-215">**允许管理共享班次** – 用户必须拥有此权限，才能打开或关闭共享班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-215">**Allow manage shared shift** – Users must have this permission to open or close a shared shift.</span></span>
- <span data-ttu-id="6f162-216">**允许使用共享班次** – 用户必须拥有此权限，才能登录和使用共享班次。</span><span class="sxs-lookup"><span data-stu-id="6f162-216">**Allow use shared shift** – Users must have this permission to sign in to and use a shared shift.</span></span>

## <a name="back-office-end-of-day-considerations"></a><span data-ttu-id="6f162-217">后勤办公室日结注意事项</span><span class="sxs-lookup"><span data-stu-id="6f162-217">Back-office end-of-day considerations</span></span>

<span data-ttu-id="6f162-218">POS 中使用班次和银箱对帐的方法与对帐计算期间汇总交易记录数据的方法不同。</span><span class="sxs-lookup"><span data-stu-id="6f162-218">The way that shifts and cash drawer reconciliation are used in the POS differs from the way that transaction data is summarized during statement calculation.</span></span> <span data-ttu-id="6f162-219">请务必了解此项差异。</span><span class="sxs-lookup"><span data-stu-id="6f162-219">It's important that you understand this difference.</span></span> <span data-ttu-id="6f162-220">POS 中的班次数据（Z 报表）和后勤办公室中的计算对帐单可能提供不同结果，具体取决于您的配置和业务流程。</span><span class="sxs-lookup"><span data-stu-id="6f162-220">Depending on your configuration and your business processes, the shift data in the POS (the Z report) and a calculated statement in the back office can give you different results.</span></span> <span data-ttu-id="6f162-221">此项差别未必表示班次数据或计算对帐单不正确，或者数据有问题。</span><span class="sxs-lookup"><span data-stu-id="6f162-221">This difference doesn't necessarily mean that either the shift data or the calculated statement is incorrect, or that there is a problem with the data.</span></span> <span data-ttu-id="6f162-222">只是表示提供的参数中可能包含更多交易记录或更少交易记录，或者交易记录的汇总方法不同。</span><span class="sxs-lookup"><span data-stu-id="6f162-222">It just means that the parameters that are provided might be including additional transaction or fewer transactions, or that the transactions have been summarized differently.</span></span>

<span data-ttu-id="6f162-223">尽管每位零售商的业务需求不同，我们仍然建议您按照下面的方法设置系统，以免出现此类型的差异：</span><span class="sxs-lookup"><span data-stu-id="6f162-223">Although every retailer has different business requirements, we recommend that you set up your system in the following way to avoid situations where differences of this type occur:</span></span>

<span data-ttu-id="6f162-224">转到 **Retail 和 Commerce \> 渠道 \> 商店 \> 所有商店 \> 对帐/结算**，然后为每个商店，将 **对帐方法** 字段和 **结算方法** 字段设置为 **班次**。</span><span class="sxs-lookup"><span data-stu-id="6f162-224">Go to **Retail and Commerce \> Channels \> Stores \> All stores \> Statement/closing**, and for each store, set both the **Statement method** field and the **Closing method** field to **Shift**.</span></span>

<span data-ttu-id="6f162-225">此项设置有助于确保后勤办公室对帐单中包含与 POS 中的班次相同的交易记录，并且按该班次汇总数据。</span><span class="sxs-lookup"><span data-stu-id="6f162-225">This setup helps guarantee that back-office statements include the same transactions as shifts in the POS, and that the data is summarized by that shift.</span></span>

<span data-ttu-id="6f162-226">有关对帐和结算方法的详细信息，请参阅[零售对帐单的商店配置](/dynamics365/unified-operations/retail/tasks/store-configurations-retail-statements)。</span><span class="sxs-lookup"><span data-stu-id="6f162-226">For more information about statement and closing methods, see [Store configurations for Retail statement](/dynamics365/unified-operations/retail/tasks/store-configurations-retail-statements).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
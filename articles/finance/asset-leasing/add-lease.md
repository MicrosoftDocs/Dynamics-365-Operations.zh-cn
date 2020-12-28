---
title: 添加或复制租赁（预览）
description: 本主题描述如何通过在资产租赁中输入新信息或从现有租赁中复制信息来创建新租赁。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 706b245971ba065bae86e31853832f721a6f9aff
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440965"
---
# <a name="add-or-copy-leases-preview"></a><span data-ttu-id="7e1d6-103">添加或复制租赁（预览）</span><span class="sxs-lookup"><span data-stu-id="7e1d6-103">Add or copy leases (Preview)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e1d6-104">本主题说明如何在资产租赁中从头开始创建租赁，以及如何通过复制现有租赁来创建租赁。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-104">This topic explains how to create a lease from scratch in Asset leasing, and also how to create a lease by copying an existing lease.</span></span> <span data-ttu-id="7e1d6-105">从头开始创建租赁的过程涉及输入新租赁的信息，然后创建租赁计划。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-105">The process for creating a lease from scratch involves entering information for the new lease and then creating a lease schedule.</span></span> <span data-ttu-id="7e1d6-106">至少设置了一个租赁之后，您可能会发现从现有租赁复制信息，然后根据需要编辑该信息创建一个新的租赁，这样更容易。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-106">After at least one lease has been set up, you might find it easier to copy the information from an existing lease and then edit that information as you require to create a new lease.</span></span>

## <a name="create-a-lease"></a><span data-ttu-id="7e1d6-107">创建租赁</span><span class="sxs-lookup"><span data-stu-id="7e1d6-107">Create a lease</span></span>

<span data-ttu-id="7e1d6-108">请按照以下步骤在资产租赁中创建租赁。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-108">Follow these steps to create a lease in Asset leasing.</span></span>

1. <span data-ttu-id="7e1d6-109">在 **租赁摘要** 页的“操作窗格”上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-109">On the **Lease summary** page, on the Action Pane, select **New**.</span></span>
2. <span data-ttu-id="7e1d6-110">输入租赁信息。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-110">Enter the lease information.</span></span> <span data-ttu-id="7e1d6-111">必填字段带有红色边框。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-111">Fields that are required have red borders.</span></span>

## <a name="create-a-lease-schedule"></a><span data-ttu-id="7e1d6-112">创建租赁计划</span><span class="sxs-lookup"><span data-stu-id="7e1d6-112">Create a lease schedule</span></span>

<span data-ttu-id="7e1d6-113">输入完租赁信息后，请按照以下步骤创建租赁计划。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-113">After you've finished entering information for the lease, follow these steps to create a lease schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="7e1d6-114">财务维度可能会根据任何自定义财务维度而更改。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-114">The financial dimensions might change based on any custom financial dimensions.</span></span>

1. <span data-ttu-id="7e1d6-115">选择 **创建计划** 生成租赁帐簿。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-115">Select **Create schedules** to generate the lease books.</span></span> <span data-ttu-id="7e1d6-116">租赁帐簿中包含付款、摊销、折旧和费用计划。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-116">The lease books include the payment, amortization, depreciation, and expense schedules.</span></span>
2. <span data-ttu-id="7e1d6-117">要访问租赁帐簿和查看新建的计划，请选择 **帐簿** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-117">To access the lease books and view the newly created schedules, select the **Books** tab.</span></span>

    <span data-ttu-id="7e1d6-118">**帐簿详细资料** 页显示了如何通过已为其分配的帐簿来计算租赁。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-118">The **Book details** page shows how the lease is accounted for by the books that have been allocated to it.</span></span> <span data-ttu-id="7e1d6-119">在这里，您可以查看租赁计划。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-119">From here, you can view the lease schedules.</span></span>

    <span data-ttu-id="7e1d6-120">付款计划中包含在 **添加租赁** 页上的 **付款计划行** 选项卡中进行的输入。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-120">The payment schedule contains the inputs from the **Payment schedule lines** tab on the **Add lease** page.</span></span> <span data-ttu-id="7e1d6-121">您仍然可以更改每个付款金额和可变付款。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-121">You can still change each payment amount and variable payment.</span></span> <span data-ttu-id="7e1d6-122">租赁负债根据修改后的付款计划计算。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-122">The lease liability is calculated based on the modified payment schedule.</span></span>

4. <span data-ttu-id="7e1d6-123">检查完付款计划后，请选择 **确认计划**。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-123">After you've finished reviewing the payment schedule, select **Confirm schedule**.</span></span> <span data-ttu-id="7e1d6-124">确认计划后，该租赁将不再可编辑。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-124">After the schedule is confirmed, the lease is no longer available for editing.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e1d6-125">系统会根据 **添加租赁** 页中的付款计划行自动计算租赁期限。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-125">The system automatically calculates the lease term from the payment schedule lines on the **Add lease** page.</span></span>
    >
    > <span data-ttu-id="7e1d6-126">为了以月为单位计算租赁期限，系统会找到特定付款计划行的开始日期和结束日期之差。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-126">To calculate the lease term in months, the system finds the difference between the start date and the end date for a specific payment schedule line.</span></span> <span data-ttu-id="7e1d6-127">然后移至下一个付款计划行，并再次找到差额。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-127">It then moves to the next payment schedule line and finds the difference again.</span></span> <span data-ttu-id="7e1d6-128">最后，系统将所有数额相加以确定租赁期限（以月为单位）。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-128">Finally, the system sums all the amounts to determine the lease term in months.</span></span>

5. <span data-ttu-id="7e1d6-129">要查看计算的期间利息费用，请打开 **负债摊销计划** 页。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-129">To view the calculated period interest expenses, open the **Liability amortization schedule** page.</span></span> <span data-ttu-id="7e1d6-130">要查看计算的直线折旧，请打开 **资产折旧计划** 页。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-130">To view calculated straight-line depreciation, open the **Asset depreciation schedule** page.</span></span>
6. <span data-ttu-id="7e1d6-131">查看完计算的金额后，您可以在 **初始确认** 页创建初始确认日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-131">After you've finished reviewing the calculated amount, you can create the initial recognition journal entry on the **Initial recognition** page.</span></span> <span data-ttu-id="7e1d6-132">您将收到一条消息，指出已创建日记帐。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-132">You receive a message that states that the journal has been created.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e1d6-133">除非您手动过帐日记帐条目，否则日记帐条目不会过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-133">The journal entry isn't posted to General ledger until you manually post the entry.</span></span>

7. <span data-ttu-id="7e1d6-134">要在发布前查看建议的初始确认条目，请选择 **资产租赁日记帐**。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-134">To review the proposed initial recognition entry before you post it, select **Asset leasing journal**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e1d6-135">不能手动创建资产租赁日记帐。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-135">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="7e1d6-136">它是在创建租赁计划时自动创建的。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-136">It's automatically created when lease schedules are created.</span></span>

8. <span data-ttu-id="7e1d6-137">查看完初始确认日记帐条目并准备好过帐后，请选择 **过帐** 在总账中确认使用权 (ROU) 资产和租赁负债。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-137">When you've finished reviewing the initial recognition journal entry and are ready to post it, select **Post** to recognize the right-of-use (ROU) asset and lease liability in General ledger.</span></span>

## <a name="copy-a-lease"></a><span data-ttu-id="7e1d6-138">复制租赁</span><span class="sxs-lookup"><span data-stu-id="7e1d6-138">Copy a lease</span></span>

<span data-ttu-id="7e1d6-139">资产租赁使您可以复制租赁的详细信息以创建具有相同信息的新租赁。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-139">Asset leasing lets you copy the details of a lease to create a new lease that has the same information.</span></span> <span data-ttu-id="7e1d6-140">然后，您可以在为复制的租赁创建计划之前更改租赁字段。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-140">You can then change the lease fields before you create the schedules for the copied lease.</span></span>

1. <span data-ttu-id="7e1d6-141">在 **租赁摘要** 页面上，选择要复制的租赁，然后在“操作”窗格上选择 **复制租赁**。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-141">On the **Lease summary** page, select the lease to copy, and then, on the Action Pane, select **Copy lease**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e1d6-142">如果关闭了租赁 ID 编号规则的 **手动** 参数，将自动生成序列中的下一个数字来充当所复制租赁的租赁 ID。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-142">If the **Manual** parameter is turned off for the number sequence for lease IDs, the next number in the sequence is automatically generated as the lease ID of the copied lease.</span></span> <span data-ttu-id="7e1d6-143">如果打开了 **手动** 参数，您会收到一条消息，提示您在继续复制租赁之前输入租赁 ID。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-143">If the **Manual** parameter is turned on, you receive a message that prompts you to enter the lease ID before you proceed to copy the lease.</span></span>

2. <span data-ttu-id="7e1d6-144">选择 **复制**。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-144">Select **Copy**.</span></span> <span data-ttu-id="7e1d6-145">将把所选租赁的租赁详细信息复制到新租赁。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-145">The lease details from the selected lease are copied to a new lease.</span></span> <span data-ttu-id="7e1d6-146">然后，您可以在保存新租赁并创建租赁计划之前对其进行编辑。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-146">You can then edit the details of the new lease before you save it and create the lease schedules.</span></span>

## <a name="asset-leasing-journal"></a><span data-ttu-id="7e1d6-147">资产租赁日记帐</span><span class="sxs-lookup"><span data-stu-id="7e1d6-147">Asset leasing journal</span></span>

<span data-ttu-id="7e1d6-148">资产租赁日记帐中包含在资产租赁中创建的所有日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-148">All journal entries that are created in Asset leasing are contained in the Asset leasing journal.</span></span> <span data-ttu-id="7e1d6-149">在 **资产租赁日记帐** 页面（**资产租赁 \> 日记帐条目 \> 资产租赁日记帐**）中，可以按过帐状态进行筛选，查看特定日记帐条目与凭证，以及过帐未过帐的日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-149">On the **Asset leasing journal** page (**Asset leasing \> Journal entries \> Asset leasing journal**), you can filter by posting status, view specific journal entries and the vouchers, and post unposted journal entries.</span></span>

> [!NOTE]
> <span data-ttu-id="7e1d6-150">不能手动创建资产租赁日记帐。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-150">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="7e1d6-151">它是在创建租赁计划时自动创建的。</span><span class="sxs-lookup"><span data-stu-id="7e1d6-151">It's automatically created when lease schedules are created.</span></span>

---
title: 弹性组
description: 此主题介绍考勤管理中如何使用弹性组。
author: johanhoffmann
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgFlexGroup, JmgFlexCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 5b695775b74950d3b5ce7d05d178c24a6bdb5aeb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214882"
---
# <a name="flex-groups"></a><span data-ttu-id="612f4-103">弹性组</span><span class="sxs-lookup"><span data-stu-id="612f4-103">Flex groups</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="612f4-104">弹性工时通过在工作量低时为工作人员提供额外的休假，让公司最大限度地减少加班费用。</span><span class="sxs-lookup"><span data-stu-id="612f4-104">Flexible working hours let companies minimize payments for overtime by offering workers extra time off during periods when the workload is low.</span></span> <span data-ttu-id="612f4-105">此功能与工作量随季节变化的细分市场之类有关。</span><span class="sxs-lookup"><span data-stu-id="612f4-105">This feature is relevant, for example, in segments that experience seasonal changes in workload.</span></span>

<span data-ttu-id="612f4-106">可使用弹性组为工作人员的弹性工时设置以下规则和原则：</span><span class="sxs-lookup"><span data-stu-id="612f4-106">You can use flex groups to set the following rules and principles for a worker's flexible hours:</span></span>

- <span data-ttu-id="612f4-107">弹性调整规则</span><span class="sxs-lookup"><span data-stu-id="612f4-107">Rules for flex regulations</span></span>
- <span data-ttu-id="612f4-108">工作人员弹性结余的计算原则</span><span class="sxs-lookup"><span data-stu-id="612f4-108">Principle for calculating the worker's flex balance</span></span>

## <a name="set-up-flexible-working-hours-in-flex-groups"></a><span data-ttu-id="612f4-109">在弹性组中设置灵活工时</span><span class="sxs-lookup"><span data-stu-id="612f4-109">Set up flexible working hours in flex groups</span></span>

- <span data-ttu-id="612f4-110">选择 **考勤管理** \> **设置** \> **组** \> **弹性组** 为灵活工时设置弹性组。</span><span class="sxs-lookup"><span data-stu-id="612f4-110">Select **Time and attendance** \> **Setup** \> **Groups** \> **Flex groups** to set up flex groups for flexible hours.</span></span>

## <a name="associate-workers-with-flex-groups"></a><span data-ttu-id="612f4-111">将工作人员与弹性组关联</span><span class="sxs-lookup"><span data-stu-id="612f4-111">Associate workers with flex groups</span></span>

- <span data-ttu-id="612f4-112">选择 **考勤管理** \> **设置** \> **时间登记工作人员**。</span><span class="sxs-lookup"><span data-stu-id="612f4-112">Select **Time and attendance** \> **Setup** \> **Time registration workers**.</span></span>

## <a name="rules-for-flex-regulations"></a><span data-ttu-id="612f4-113">弹性调整规则</span><span class="sxs-lookup"><span data-stu-id="612f4-113">Rules for flex regulations</span></span>

<span data-ttu-id="612f4-114">可使用弹性调整规则定义弹性限制或工作人员的弹性科目中允许的最小工时数和最大工时数。</span><span class="sxs-lookup"><span data-stu-id="612f4-114">You can use rules for flex regulations to define flex limits, or the minimum and maximum number of hours that are allowed in the worker's flex account.</span></span> <span data-ttu-id="612f4-115">弹性限制在弹性组中设置。</span><span class="sxs-lookup"><span data-stu-id="612f4-115">The flex limits are set up on the flex group.</span></span> <span data-ttu-id="612f4-116">超出弹性限制时，可以调整工作人员的弹性结余和付薪。</span><span class="sxs-lookup"><span data-stu-id="612f4-116">When the flex limits are exceeded, a worker's flex balance and pay can be adjusted.</span></span>

<span data-ttu-id="612f4-117">如果超出了工作人员的允许弹性最小值（即弹性科目中的工时数低于指定的最小值），则可使用以下方法通过指定弹性调整调整工作人员的弹性结余：</span><span class="sxs-lookup"><span data-stu-id="612f4-117">If a worker's allowed flex minimum is exceeded (that is, if the number of hours in the flex account is below the specified minimum), you can use these methods to adjust the worker's flex balance by making a flex regulation:</span></span>

- <span data-ttu-id="612f4-118">可将工作人员的弹性科目调整为指定的允许最小值，但不扣除工作人员付薪中弹性科目低于允许的最小值的工时数。</span><span class="sxs-lookup"><span data-stu-id="612f4-118">The worker's flex account can be adjusted to the specified allowed minimum, but without deducting the worker's pay for the number of hours that the flex account is below the allowed minimum.</span></span>
- <span data-ttu-id="612f4-119">可扣除工作人员付薪中弹性科目低于允许的最小值的工时数。</span><span class="sxs-lookup"><span data-stu-id="612f4-119">The worker's pay can be deducted for the number of hours that the flex account is below the allowed minimum.</span></span> <span data-ttu-id="612f4-120">扣除方法是为特定付薪类型生成具有负或正付薪单位的付薪项。</span><span class="sxs-lookup"><span data-stu-id="612f4-120">This deduction is done by generating pay items for a specific pay type that have a negative or positive pay unit.</span></span>

<span data-ttu-id="612f4-121">如果超过了工作人员的允许弹性最大值，则可使用以下方法通过创建弹性调整调整工作人员的弹性结余：</span><span class="sxs-lookup"><span data-stu-id="612f4-121">If the worker's allowed flex maximum is exceeded, you can use these methods to adjust the worker's flex balance by making a flex regulation:</span></span>

- <span data-ttu-id="612f4-122">可将工作人员的弹性科目调整回指定的允许最大值，但不补偿工作人员付薪中高于允许的最大值的工时数。</span><span class="sxs-lookup"><span data-stu-id="612f4-122">The worker's flex account can be adjusted back to the specified allowed maximum, but without compensating the worker's pay for the number of hours that the worker worked above the allowed maximum.</span></span>
- <span data-ttu-id="612f4-123">可将高于允许的最大值的工作人员工时数转换为付薪。</span><span class="sxs-lookup"><span data-stu-id="612f4-123">The number of hours that the worker worked above the allowed maximum can be converted to pay.</span></span> <span data-ttu-id="612f4-124">转换方法是生成特定付薪类型的付薪项。</span><span class="sxs-lookup"><span data-stu-id="612f4-124">This conversion is done by generating pay items for a specific pay type.</span></span>

<span data-ttu-id="612f4-125">可在以下情况下调整弹性结余：</span><span class="sxs-lookup"><span data-stu-id="612f4-125">You can adjust a flex balance at the following times:</span></span>

- <span data-ttu-id="612f4-126">使用 **转移付薪** 作业导出了基于工资单数据的付款文件。</span><span class="sxs-lookup"><span data-stu-id="612f4-126">When a payment file that is based on payroll data is exported by using the **Transfer pay** job.</span></span> <span data-ttu-id="612f4-127">从 **审核** 页转换工作人员的登记信息时生成了工资单数据。</span><span class="sxs-lookup"><span data-stu-id="612f4-127">The payroll data is generated when you transfer the worker's registration from the **Approve** page.</span></span>
- <span data-ttu-id="612f4-128">处理了 **调整弹性结余** 作业时。</span><span class="sxs-lookup"><span data-stu-id="612f4-128">When the **Adjust flex balance** job is processed.</span></span>

> [!NOTE]
> <span data-ttu-id="612f4-129">在 **审核** 页上执行工作人员登记信息日审核和转换时不执行弹性调整。</span><span class="sxs-lookup"><span data-stu-id="612f4-129">Flex regulations don't occur during the daily approval and transfer of worker registrations on the **Approve** page.</span></span>

## <a name="principle-for-calculating-a-workers-flex-balance"></a><span data-ttu-id="612f4-130">工作人员弹性结余的计算原则</span><span class="sxs-lookup"><span data-stu-id="612f4-130">Principle for calculating a worker's flex balance</span></span>

<span data-ttu-id="612f4-131">工作人员弹性结余的调整工时计算原则在弹性组中设置。</span><span class="sxs-lookup"><span data-stu-id="612f4-131">The principle for calculating the hours that the worker's flex balance are adjusted by is set up on the flex group.</span></span> <span data-ttu-id="612f4-132">选择 **考勤管理** \> **设置** \> **组** \> **弹性组**。</span><span class="sxs-lookup"><span data-stu-id="612f4-132">Select **Time and attendance** \> **Setup** \> **Groups** \> **Flex groups**.</span></span> 

<span data-ttu-id="612f4-133">可以使用下面的两条原则：</span><span class="sxs-lookup"><span data-stu-id="612f4-133">The following two principles can be used:</span></span>

- <span data-ttu-id="612f4-134">**时间** – 工作人员的弹性工时只能通过工作人员该日登记的时间来计算。</span><span class="sxs-lookup"><span data-stu-id="612f4-134">**Time** – The worker's flexible hours are calculated only from the worker's registered time for the day.</span></span> <span data-ttu-id="612f4-135">计算工作人员的日登记信息时，将通过工作人员时间模板中定义的弹性+ 和弹性- 区域计算该日的弹性+ 和弹性- 工时数。</span><span class="sxs-lookup"><span data-stu-id="612f4-135">When the worker's daily registrations are calculated, the number of Flex+ and Flex- hours for the day is calculated from the Flex+ and Flex- zones that are defined in the worker's time profile.</span></span>
- <span data-ttu-id="612f4-136">**付薪类型** – 工作人员的弹性工时基于工作人员付薪协议中定义的弹性+ 和弹性- 的付薪类型收入来计算。</span><span class="sxs-lookup"><span data-stu-id="612f4-136">**Pay types** – The worker's flexible hours are calculated based on earnings of the pay types for Flex+ and Flex- that are defined in the worker's pay agreement.</span></span> <span data-ttu-id="612f4-137">付薪协议与时间登记工作人员。</span><span class="sxs-lookup"><span data-stu-id="612f4-137">The pay agreement is associated with the time registration worker.</span></span> <span data-ttu-id="612f4-138">您可能希望使用付薪类型管理弹性科目，例如要在一个或多个弹性区域内按特定系数增加工作人员的弹性科目。</span><span class="sxs-lookup"><span data-stu-id="612f4-138">You might want to use pay types to manage flex accounts if, for example, you want to increase a worker's flex account by a specific factor in one or more flex zones.</span></span>

### <a name="scenario-1-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-minimum-is-exceeded"></a><span data-ttu-id="612f4-139">方案 1：因为超出了允许的弹性最小值而调整工作人员的付薪和弹性科目</span><span class="sxs-lookup"><span data-stu-id="612f4-139">Scenario 1: Adjusting a worker's pay and flex account because the allowed flex minimum is exceeded</span></span>

<span data-ttu-id="612f4-140">可弹性工作的工作人员具有负弹性科目。</span><span class="sxs-lookup"><span data-stu-id="612f4-140">A worker who can work flexible hours has a negative flex account.</span></span>

- <span data-ttu-id="612f4-141">**弹性科目：**-4</span><span class="sxs-lookup"><span data-stu-id="612f4-141">**Flex account:** -4</span></span>

<span data-ttu-id="612f4-142">工作人员与具有以下配置的弹性组关联：</span><span class="sxs-lookup"><span data-stu-id="612f4-142">The worker is associated with a flex group that has the following configuration:</span></span>

- <span data-ttu-id="612f4-143">**最小弹性值：**-0.5</span><span class="sxs-lookup"><span data-stu-id="612f4-143">**Flex minimum:** -0.5</span></span>
- <span data-ttu-id="612f4-144">**最小值付薪类型：** 1302</span><span class="sxs-lookup"><span data-stu-id="612f4-144">**Minimum pay type:** 1302</span></span>
- <span data-ttu-id="612f4-145">**付薪类型系数：**-1.00</span><span class="sxs-lookup"><span data-stu-id="612f4-145">**Pay type factor:** -1.00</span></span>

<span data-ttu-id="612f4-146">按照工作人员的弹性科目与允许的弹性最小值之差的指示，超出了工作人员的允许弹性最小值 3.5 个小时。</span><span class="sxs-lookup"><span data-stu-id="612f4-146">As the difference between the worker's flex account and his allowed flex minimum indicates, the worker has exceeded his allowed flex minimum by 3.5 hours.</span></span>

<span data-ttu-id="612f4-147">工作单管理员通过运行 **转移付薪** 或 **弹性调整** 作业转移工作人员的付薪数据时，将执行以下调整：</span><span class="sxs-lookup"><span data-stu-id="612f4-147">When the payroll administrator transfers the worker's pay data by running the **Transfer to pay** or **Flex adjustment** job, the following adjustments are made:</span></span>

- <span data-ttu-id="612f4-148">调整工作人员弹性科目 3.5 个小时。</span><span class="sxs-lookup"><span data-stu-id="612f4-148">The worker's flex account is adjusted by 3.5 hours.</span></span> <span data-ttu-id="612f4-149">因此，-4.0 个小时的弹性结余调整为工作人员的允许弹性最小值 -0.5 小时。</span><span class="sxs-lookup"><span data-stu-id="612f4-149">Therefore, the flex balance of -4.0 hours becomes adjusted to the worker's allowed flex minimum of -0.5 hours.</span></span>
- <span data-ttu-id="612f4-150">将创建付薪类型为 1302 的付薪项。</span><span class="sxs-lookup"><span data-stu-id="612f4-150">A pay item for pay type 1302 is created.</span></span> <span data-ttu-id="612f4-151">此付薪项的付薪单位为 -3.5 小时，将从工作人员的付薪中扣除。</span><span class="sxs-lookup"><span data-stu-id="612f4-151">This pay item has a pay unit of -3.5 hours that will be deducted from the worker's pay.</span></span> <span data-ttu-id="612f4-152">在此情况下，付薪单位为负数，因为 3.5 小时的正调整乘以了弹性组中定义的父付薪类型系数 -1.0。</span><span class="sxs-lookup"><span data-stu-id="612f4-152">In this case, the pay unit is a negative number, because the positive adjustment of 3.5 hours is multiplied by the negative pay type factor of -1.0 that is defined on the flex group.</span></span> <span data-ttu-id="612f4-153">此付薪项属于 **转移付薪** 作业生成的付薪文件。</span><span class="sxs-lookup"><span data-stu-id="612f4-153">This pay item will be part of the pay file that is generated by the **Transfer to pay** job.</span></span>

### <a name="scenario-2-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-maximum-is-exceeded"></a><span data-ttu-id="612f4-154">方案 2：因为超出了允许的弹性最大值而调整工作人员的付薪和弹性科目</span><span class="sxs-lookup"><span data-stu-id="612f4-154">Scenario 2: Adjusting a worker's pay and flex account because the allowed flex maximum is exceeded</span></span>

<span data-ttu-id="612f4-155">可弹性工作的工作人员具有正弹性科目。</span><span class="sxs-lookup"><span data-stu-id="612f4-155">A worker who can work flexible hours has a positive flex account.</span></span>

- <span data-ttu-id="612f4-156">**弹性科目：** 6</span><span class="sxs-lookup"><span data-stu-id="612f4-156">**Flex account:** 6</span></span>

<span data-ttu-id="612f4-157">工作人员与具有以下配置的弹性组关联：</span><span class="sxs-lookup"><span data-stu-id="612f4-157">The worker is associated with a flex group that has the following configuration:</span></span>

- <span data-ttu-id="612f4-158">**最大弹性值：** 2.0</span><span class="sxs-lookup"><span data-stu-id="612f4-158">**Flex maximum:** 2.0</span></span>
- <span data-ttu-id="612f4-159">**最小值付薪类型：** 1302</span><span class="sxs-lookup"><span data-stu-id="612f4-159">**Minimum pay type:** 1302</span></span>
- <span data-ttu-id="612f4-160">**付薪类型系数：**-1.0</span><span class="sxs-lookup"><span data-stu-id="612f4-160">**Pay type factor:** -1.0</span></span>

<span data-ttu-id="612f4-161">按照工作人员的弹性科目与允许的弹性最大值之差的指示，超出了工作人员的允许弹性最大值 4.0 个小时。</span><span class="sxs-lookup"><span data-stu-id="612f4-161">As the difference between the worker's flex account and her allowed flex maximum indicates, the worker has exceeded her allowed flex maximum by 4.0 hours.</span></span>

<span data-ttu-id="612f4-162">工作单管理员通过运行 **转移付薪** 或 **弹性调整** 作业转移工作人员的付薪数据时，将执行以下调整：</span><span class="sxs-lookup"><span data-stu-id="612f4-162">When the payroll administrator transfers the worker's pay data by running the **Transfer to pay** or **Flex adjustment** job, the following adjustments are made:</span></span>

- <span data-ttu-id="612f4-163">调整工作人员弹性科目 -4.0 个小时。</span><span class="sxs-lookup"><span data-stu-id="612f4-163">The worker's flex account is adjusted by -4.0 hours.</span></span> <span data-ttu-id="612f4-164">因此，6.0 个小时的弹性结余调整为工作人员的允许弹性最大值 2.0 小时。</span><span class="sxs-lookup"><span data-stu-id="612f4-164">Therefore, the flex balance of 6.0 hours becomes adjusted to the worker's allowed flex maximum of 2.0 hours.</span></span>
- <span data-ttu-id="612f4-165">将创建付薪类型为 1302 的付薪项。</span><span class="sxs-lookup"><span data-stu-id="612f4-165">A pay item for pay type 1302 is created.</span></span> <span data-ttu-id="612f4-166">此付薪项的付薪单位为 4.0 小时，将添加到工作人员的付薪中。</span><span class="sxs-lookup"><span data-stu-id="612f4-166">This pay item has a pay unit of 4.0 hours that will be added to the worker's pay.</span></span> <span data-ttu-id="612f4-167">在此情况下，付薪单位为正数，因为 4.0 小时的负调整乘以了弹性组中定义的父付薪类型系数 -1.0。</span><span class="sxs-lookup"><span data-stu-id="612f4-167">In this case, the pay unit is a positive number, because the negative adjustment of 4.0 hours is multiplied by the negative pay type factor of -1.0 that is defined on the flex group.</span></span> <span data-ttu-id="612f4-168">此付薪项属于 **转移付薪** 作业生成的付薪文件。</span><span class="sxs-lookup"><span data-stu-id="612f4-168">This pay item will be part of the pay file that is generated by the **Transfer to pay** job.</span></span>

### <a name="scenario-3-managing-a-workers-flex-balance-based-on-pay-types"></a><span data-ttu-id="612f4-169">方案 3：基于付薪类型管理工作人员的弹性结余</span><span class="sxs-lookup"><span data-stu-id="612f4-169">Scenario 3: Managing a worker's flex balance based on pay types</span></span>

<span data-ttu-id="612f4-170">前面介绍过，可基于工作人员时间模板中定义的弹性+ 和弹性- 区域中登记的时间，或基于工作人员付薪协议中定义的付薪类型管理弹性科目。</span><span class="sxs-lookup"><span data-stu-id="612f4-170">As we explained earlier, flex accounts can be managed based either on the time that is registered in the Flex+ and Flex- zones that are defined the worker's time profile, or on the pay types that are defined in the worker's pay agreements.</span></span> <span data-ttu-id="612f4-171">如果使用弹性科目，将按照从 **审核** 页转移工作人员的登记信息时生成的付薪项调整工作人员的弹性科目。</span><span class="sxs-lookup"><span data-stu-id="612f4-171">If pay types are used, a worker's flex account is adjusted by the pay items that are generated when you transfer the worker's registration from the **Approve** page.</span></span> <span data-ttu-id="612f4-172">您可能希望使用付薪类型管理弹性科目，例如要在一个或多个弹性区域内按特定系数增加工作人员的弹性科目。</span><span class="sxs-lookup"><span data-stu-id="612f4-172">You might want to use pay types to manage flex accounts if, for example, you want to increase a worker's flex account by a specific factor in one or more flex zones.</span></span>

<span data-ttu-id="612f4-173">此方案使用以下表示工作日的弹性模板。</span><span class="sxs-lookup"><span data-stu-id="612f4-173">This scenario uses the following flex profile that represents a workday.</span></span>

| <span data-ttu-id="612f4-174">模板类型</span><span class="sxs-lookup"><span data-stu-id="612f4-174">Profile type</span></span>  | <span data-ttu-id="612f4-175">启动</span><span class="sxs-lookup"><span data-stu-id="612f4-175">Start</span></span>    | <span data-ttu-id="612f4-176">结束日期</span><span class="sxs-lookup"><span data-stu-id="612f4-176">End</span></span>      |
|---------------|----------|----------|
| <span data-ttu-id="612f4-177">弹性+</span><span class="sxs-lookup"><span data-stu-id="612f4-177">Flex+</span></span>         | <span data-ttu-id="612f4-178">上午 12:00</span><span class="sxs-lookup"><span data-stu-id="612f4-178">12:00 AM</span></span> | <span data-ttu-id="612f4-179">上午 08:00</span><span class="sxs-lookup"><span data-stu-id="612f4-179">08:00 AM</span></span> |
| <span data-ttu-id="612f4-180">上班打卡</span><span class="sxs-lookup"><span data-stu-id="612f4-180">Clock in</span></span>      | <span data-ttu-id="612f4-181">上午 08:00</span><span class="sxs-lookup"><span data-stu-id="612f4-181">08:00 AM</span></span> | <span data-ttu-id="612f4-182">上午 08:00</span><span class="sxs-lookup"><span data-stu-id="612f4-182">08:00 AM</span></span> |
| <span data-ttu-id="612f4-183">弹性-</span><span class="sxs-lookup"><span data-stu-id="612f4-183">Flex-</span></span>         | <span data-ttu-id="612f4-184">上午 08:00</span><span class="sxs-lookup"><span data-stu-id="612f4-184">08:00 AM</span></span> | <span data-ttu-id="612f4-185">上午 09:00</span><span class="sxs-lookup"><span data-stu-id="612f4-185">09:00 AM</span></span> |
| <span data-ttu-id="612f4-186">标准时间</span><span class="sxs-lookup"><span data-stu-id="612f4-186">Standard time</span></span> | <span data-ttu-id="612f4-187">上午 09:00</span><span class="sxs-lookup"><span data-stu-id="612f4-187">09:00 AM</span></span> | <span data-ttu-id="612f4-188">上午 11:30</span><span class="sxs-lookup"><span data-stu-id="612f4-188">11:30 AM</span></span> |
| <span data-ttu-id="612f4-189">工间休息</span><span class="sxs-lookup"><span data-stu-id="612f4-189">Paid break</span></span>    | <span data-ttu-id="612f4-190">上午 11:30</span><span class="sxs-lookup"><span data-stu-id="612f4-190">11:30 AM</span></span> | <span data-ttu-id="612f4-191">下午 12:00</span><span class="sxs-lookup"><span data-stu-id="612f4-191">12:00 PM</span></span> |
| <span data-ttu-id="612f4-192">弹性-</span><span class="sxs-lookup"><span data-stu-id="612f4-192">Flex-</span></span>         | <span data-ttu-id="612f4-193">下午 12:00</span><span class="sxs-lookup"><span data-stu-id="612f4-193">12:00 PM</span></span> | <span data-ttu-id="612f4-194">下午 04:00</span><span class="sxs-lookup"><span data-stu-id="612f4-194">04:00 PM</span></span> |
| <span data-ttu-id="612f4-195">下班打卡</span><span class="sxs-lookup"><span data-stu-id="612f4-195">Clock out</span></span>     | <span data-ttu-id="612f4-196">下午 04:00</span><span class="sxs-lookup"><span data-stu-id="612f4-196">04:00 PM</span></span> | <span data-ttu-id="612f4-197">下午 04:00</span><span class="sxs-lookup"><span data-stu-id="612f4-197">04:00 PM</span></span> |
| <span data-ttu-id="612f4-198">弹性+</span><span class="sxs-lookup"><span data-stu-id="612f4-198">Flex+</span></span>         | <span data-ttu-id="612f4-199">下午 04:00</span><span class="sxs-lookup"><span data-stu-id="612f4-199">04:00 PM</span></span> | <span data-ttu-id="612f4-200">上午 12:00</span><span class="sxs-lookup"><span data-stu-id="612f4-200">12:00 AM</span></span> |

<span data-ttu-id="612f4-201">在此情况下，您可能希望可以基于付薪类型管理工作人员的弹性结余。</span><span class="sxs-lookup"><span data-stu-id="612f4-201">In this case, you want to be able to manage the worker's flex balance based on pay types.</span></span> <span data-ttu-id="612f4-202">因此，必须在工作人员的弹性组中将 **基于付薪类型** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="612f4-202">Therefore, you must set the **Based on pay types** option to **Yes** on the worker's flex group.</span></span>

<span data-ttu-id="612f4-203">若要解释弹性工时，还必须定义新的付薪类型。</span><span class="sxs-lookup"><span data-stu-id="612f4-203">To account for the flexible hours, you must also define a new pay type.</span></span> <span data-ttu-id="612f4-204">在此方案中，付薪类型命名为 **FlexCnt**。</span><span class="sxs-lookup"><span data-stu-id="612f4-204">For this scenario, the pay type is named **FlexCnt**.</span></span>

| <span data-ttu-id="612f4-205">付薪类型</span><span class="sxs-lookup"><span data-stu-id="612f4-205">Pay type</span></span> | <span data-ttu-id="612f4-206">说明</span><span class="sxs-lookup"><span data-stu-id="612f4-206">Description</span></span>  |
|----------|--------------|
| <span data-ttu-id="612f4-207">FlexCnt</span><span class="sxs-lookup"><span data-stu-id="612f4-207">FlexCnt</span></span>  | <span data-ttu-id="612f4-208">弹性计数器</span><span class="sxs-lookup"><span data-stu-id="612f4-208">Flex counter</span></span> |

<span data-ttu-id="612f4-209">然后，执行以下步骤设置付薪类型并将新类型的行添加到付薪模板。</span><span class="sxs-lookup"><span data-stu-id="612f4-209">Next, follow these steps to set up a pay type and add lines of the new type to a pay profile.</span></span>

1. <span data-ttu-id="612f4-210">选择 **考勤管理** \> **设置** \> **组** \> **弹性组**，然后选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="612f4-210">Select **Time and attendance** \> **Setup** \> **Groups** \> **Flex groups**, and then select **New**.</span></span>
2. <span data-ttu-id="612f4-211">在 **弹性+** 字段和 **弹性-** 字段中，指定新付薪类型 **FlexCnt**。</span><span class="sxs-lookup"><span data-stu-id="612f4-211">In both the **Flex+** field and the **Flex-** field, specify the new pay type, **FlexCnt**.</span></span>
3. <span data-ttu-id="612f4-212">选择 **考勤管理** \> **设置** \> **付薪协议**，然后选择 **协议行**。</span><span class="sxs-lookup"><span data-stu-id="612f4-212">Select **Time and attendance** \> **Setup** \> **Pay agreements**, and then select **Agreement lines**.</span></span>
4. <span data-ttu-id="612f4-213">对于 **星期一**，为 **弹性+** 模板类型添加下面的三行。</span><span class="sxs-lookup"><span data-stu-id="612f4-213">For **Monday**, for the **Flex+** profile type, add the following three lines.</span></span>

    | <span data-ttu-id="612f4-214">付薪类型</span><span class="sxs-lookup"><span data-stu-id="612f4-214">Pay type</span></span> | <span data-ttu-id="612f4-215">说明</span><span class="sxs-lookup"><span data-stu-id="612f4-215">Description</span></span>  | <span data-ttu-id="612f4-216">起始时间</span><span class="sxs-lookup"><span data-stu-id="612f4-216">From time</span></span> | <span data-ttu-id="612f4-217">截止时间</span><span class="sxs-lookup"><span data-stu-id="612f4-217">To time</span></span>  | <span data-ttu-id="612f4-218">最小值</span><span class="sxs-lookup"><span data-stu-id="612f4-218">Minimum</span></span> | <span data-ttu-id="612f4-219">最大值</span><span class="sxs-lookup"><span data-stu-id="612f4-219">Maximum</span></span> | <span data-ttu-id="612f4-220">系数</span><span class="sxs-lookup"><span data-stu-id="612f4-220">Factor</span></span> |
    |----------|--------------|-----------|----------|---------|---------|--------|
    | <span data-ttu-id="612f4-221">FlexCnt</span><span class="sxs-lookup"><span data-stu-id="612f4-221">FlexCnt</span></span>  | <span data-ttu-id="612f4-222">弹性计数器</span><span class="sxs-lookup"><span data-stu-id="612f4-222">Flex counter</span></span> | <span data-ttu-id="612f4-223">上午 12:00</span><span class="sxs-lookup"><span data-stu-id="612f4-223">12:00 AM</span></span>  | <span data-ttu-id="612f4-224">下午 06:00</span><span class="sxs-lookup"><span data-stu-id="612f4-224">06:00 PM</span></span> | <span data-ttu-id="612f4-225">00.00</span><span class="sxs-lookup"><span data-stu-id="612f4-225">00.00</span></span>   | <span data-ttu-id="612f4-226">00.00</span><span class="sxs-lookup"><span data-stu-id="612f4-226">00.00</span></span>   | <span data-ttu-id="612f4-227">1.00</span><span class="sxs-lookup"><span data-stu-id="612f4-227">1.00</span></span>   |
    | <span data-ttu-id="612f4-228">FlexCnt</span><span class="sxs-lookup"><span data-stu-id="612f4-228">FlexCnt</span></span>  | <span data-ttu-id="612f4-229">弹性计数器</span><span class="sxs-lookup"><span data-stu-id="612f4-229">Flex counter</span></span> | <span data-ttu-id="612f4-230">下午 06:00</span><span class="sxs-lookup"><span data-stu-id="612f4-230">06:00 PM</span></span>  | <span data-ttu-id="612f4-231">上午 12:00</span><span class="sxs-lookup"><span data-stu-id="612f4-231">12:00 AM</span></span> | <span data-ttu-id="612f4-232">00.00</span><span class="sxs-lookup"><span data-stu-id="612f4-232">00.00</span></span>   | <span data-ttu-id="612f4-233">02.00</span><span class="sxs-lookup"><span data-stu-id="612f4-233">02.00</span></span>   | <span data-ttu-id="612f4-234">1.50</span><span class="sxs-lookup"><span data-stu-id="612f4-234">1.50</span></span>   |
    | <span data-ttu-id="612f4-235">FlexCnt</span><span class="sxs-lookup"><span data-stu-id="612f4-235">FlexCnt</span></span>  | <span data-ttu-id="612f4-236">弹性计数器</span><span class="sxs-lookup"><span data-stu-id="612f4-236">Flex counter</span></span> | <span data-ttu-id="612f4-237">下午 06:00</span><span class="sxs-lookup"><span data-stu-id="612f4-237">06:00 PM</span></span>  | <span data-ttu-id="612f4-238">上午 12:00</span><span class="sxs-lookup"><span data-stu-id="612f4-238">12:00 AM</span></span> | <span data-ttu-id="612f4-239">02.00</span><span class="sxs-lookup"><span data-stu-id="612f4-239">02.00</span></span>   | <span data-ttu-id="612f4-240">06.00</span><span class="sxs-lookup"><span data-stu-id="612f4-240">06.00</span></span>   | <span data-ttu-id="612f4-241">2.00</span><span class="sxs-lookup"><span data-stu-id="612f4-241">2.00</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="612f4-242">各行用于不同时间间隔，具有不同系数。</span><span class="sxs-lookup"><span data-stu-id="612f4-242">Each line is used for a different time interval and has a different factor.</span></span> <span data-ttu-id="612f4-243">工作人员在时间间隔内的弹性工时将乘以该行的系数。</span><span class="sxs-lookup"><span data-stu-id="612f4-243">The flexible hours that the worker works in a time interval are multiplied by the factor for that line.</span></span> <span data-ttu-id="612f4-244">例如，下午 6 点到晚上 8 点的工时乘以 1.50。</span><span class="sxs-lookup"><span data-stu-id="612f4-244">For example, hours that are worked from 06:00 PM to 08:00 PM are multiplied by 1.50.</span></span> <span data-ttu-id="612f4-245">系数在 **付薪协议行** 页 **常规** 选项卡上的 **系数** 字段中指定。</span><span class="sxs-lookup"><span data-stu-id="612f4-245">The factor is specified in the **Factor** field on the **General** tab of the **Pay agreement lines** page.</span></span>

<span data-ttu-id="612f4-246">工作人员输入该日的以下登记信息。</span><span class="sxs-lookup"><span data-stu-id="612f4-246">The worker enters the following registrations for the day.</span></span>

| <span data-ttu-id="612f4-247">日记帐登记类型</span><span class="sxs-lookup"><span data-stu-id="612f4-247">Journal registration type</span></span> | <span data-ttu-id="612f4-248">启动</span><span class="sxs-lookup"><span data-stu-id="612f4-248">Start</span></span>    | <span data-ttu-id="612f4-249">结束日期</span><span class="sxs-lookup"><span data-stu-id="612f4-249">End</span></span>      |
|---------------------------|----------|----------|
| <span data-ttu-id="612f4-250">上班打卡</span><span class="sxs-lookup"><span data-stu-id="612f4-250">Clock in</span></span>                  | <span data-ttu-id="612f4-251">上午 07:00</span><span class="sxs-lookup"><span data-stu-id="612f4-251">07:00 AM</span></span> | <span data-ttu-id="612f4-252">上午 07:00</span><span class="sxs-lookup"><span data-stu-id="612f4-252">07:00 AM</span></span> |
| <span data-ttu-id="612f4-253">生产作业</span><span class="sxs-lookup"><span data-stu-id="612f4-253">Production job</span></span>            | <span data-ttu-id="612f4-254">上午 07:00</span><span class="sxs-lookup"><span data-stu-id="612f4-254">07:00 AM</span></span> | <span data-ttu-id="612f4-255">下午 09:00</span><span class="sxs-lookup"><span data-stu-id="612f4-255">09:00 PM</span></span> |
| <span data-ttu-id="612f4-256">下班打卡</span><span class="sxs-lookup"><span data-stu-id="612f4-256">Clock out</span></span>                 | <span data-ttu-id="612f4-257">下午 09:00</span><span class="sxs-lookup"><span data-stu-id="612f4-257">09:00 PM</span></span> | <span data-ttu-id="612f4-258">下午 09:00</span><span class="sxs-lookup"><span data-stu-id="612f4-258">09:00 PM</span></span> |

<span data-ttu-id="612f4-259">必须支付的金额在 **审核** 页上根据工作人员的登记信息计算。</span><span class="sxs-lookup"><span data-stu-id="612f4-259">The amount that must be paid is calculated on the **Approve** page, based on the worker's registration.</span></span> <span data-ttu-id="612f4-260">计算登记信息之后，可在 **时间** 选项卡上查看结果。在此方案中，您需要注意以下字段。</span><span class="sxs-lookup"><span data-stu-id="612f4-260">After the registration is calculated, you can view the result on the **Times** tab. For this scenario, you're interested in the following fields.</span></span>

| <span data-ttu-id="612f4-261">弹性+</span><span class="sxs-lookup"><span data-stu-id="612f4-261">Flex +</span></span> | <span data-ttu-id="612f4-262">弹性-</span><span class="sxs-lookup"><span data-stu-id="612f4-262">Flex -</span></span> | <span data-ttu-id="612f4-263">时间</span><span class="sxs-lookup"><span data-stu-id="612f4-263">Time</span></span>  | <span data-ttu-id="612f4-264">带薪时间</span><span class="sxs-lookup"><span data-stu-id="612f4-264">Pay time</span></span> |
|--------|--------|-------|----------|
| <span data-ttu-id="612f4-265">6.00</span><span class="sxs-lookup"><span data-stu-id="612f4-265">6.00</span></span>   | <span data-ttu-id="612f4-266">0.00</span><span class="sxs-lookup"><span data-stu-id="612f4-266">0.00</span></span>   | <span data-ttu-id="612f4-267">13.50</span><span class="sxs-lookup"><span data-stu-id="612f4-267">13.50</span></span> | <span data-ttu-id="612f4-268">08.00</span><span class="sxs-lookup"><span data-stu-id="612f4-268">08.00</span></span>    |

<span data-ttu-id="612f4-269">弹性+ 时间量为六小时，计算基于设计模板中的弹性区域。</span><span class="sxs-lookup"><span data-stu-id="612f4-269">The amount of Flex+ time is six hours, and the calculation is based on the flex zones in the time profile.</span></span> <span data-ttu-id="612f4-270">此数量中包含早上 7 点到 8 点的一小时弹性+ 时间和下午 4 点到晚上 9 点的五小时弹性+ 时间。</span><span class="sxs-lookup"><span data-stu-id="612f4-270">This amount consists of one hour of Flex+ time from 07:00 AM to 08:00 AM and five hours of Flex+ time from 04:00 PM to 09:00 PM.</span></span>

<span data-ttu-id="612f4-271">转移登记信息时，您将发现弹性+ 时间量从 6 小时变为 8 小时。</span><span class="sxs-lookup"><span data-stu-id="612f4-271">When you transfer the registrations, you will notice that the amount of Flex+ time is changed from 6.0 hours to 8.0 hours.</span></span>

| <span data-ttu-id="612f4-272">弹性+</span><span class="sxs-lookup"><span data-stu-id="612f4-272">Flex +</span></span> | <span data-ttu-id="612f4-273">弹性-</span><span class="sxs-lookup"><span data-stu-id="612f4-273">Flex -</span></span> | <span data-ttu-id="612f4-274">时间</span><span class="sxs-lookup"><span data-stu-id="612f4-274">Time</span></span>  | <span data-ttu-id="612f4-275">带薪时间</span><span class="sxs-lookup"><span data-stu-id="612f4-275">Pay time</span></span> |
|--------|--------|-------|----------|
| <span data-ttu-id="612f4-276">8.00</span><span class="sxs-lookup"><span data-stu-id="612f4-276">8.00</span></span>   | <span data-ttu-id="612f4-277">0.00</span><span class="sxs-lookup"><span data-stu-id="612f4-277">0.00</span></span>   | <span data-ttu-id="612f4-278">13.50</span><span class="sxs-lookup"><span data-stu-id="612f4-278">13.50</span></span> | <span data-ttu-id="612f4-279">08.00</span><span class="sxs-lookup"><span data-stu-id="612f4-279">08.00</span></span>    |

<span data-ttu-id="612f4-280">此变化在转移后发生，因为弹性工时的计算方法基于付薪类型，而不是基于时间。</span><span class="sxs-lookup"><span data-stu-id="612f4-280">This change occurs after the transfer because the flexible hours have been calculated based on pay types instead of time.</span></span> <span data-ttu-id="612f4-281">下表显示这八个小时是如何计算出来的。</span><span class="sxs-lookup"><span data-stu-id="612f4-281">The following table shows how the eight hours are calculated.</span></span>

| <span data-ttu-id="612f4-282">发件人</span><span class="sxs-lookup"><span data-stu-id="612f4-282">From</span></span>     | <span data-ttu-id="612f4-283">截止日期</span><span class="sxs-lookup"><span data-stu-id="612f4-283">To</span></span>       | <span data-ttu-id="612f4-284">时间</span><span class="sxs-lookup"><span data-stu-id="612f4-284">Time</span></span> | <span data-ttu-id="612f4-285">系数</span><span class="sxs-lookup"><span data-stu-id="612f4-285">Factor</span></span>    | <span data-ttu-id="612f4-286">弹性科目</span><span class="sxs-lookup"><span data-stu-id="612f4-286">Flex account</span></span> |
|----------|----------|------|-----------|--------------|
| <span data-ttu-id="612f4-287">上午 07:00</span><span class="sxs-lookup"><span data-stu-id="612f4-287">07:00 AM</span></span> | <span data-ttu-id="612f4-288">上午 08:00</span><span class="sxs-lookup"><span data-stu-id="612f4-288">08:00 AM</span></span> | <span data-ttu-id="612f4-289">1</span><span class="sxs-lookup"><span data-stu-id="612f4-289">1</span></span>    | <span data-ttu-id="612f4-290">1</span><span class="sxs-lookup"><span data-stu-id="612f4-290">1</span></span>         | <span data-ttu-id="612f4-291">1</span><span class="sxs-lookup"><span data-stu-id="612f4-291">1</span></span>            |
| <span data-ttu-id="612f4-292">下午 04:00</span><span class="sxs-lookup"><span data-stu-id="612f4-292">04:00 PM</span></span> | <span data-ttu-id="612f4-293">下午 06:00</span><span class="sxs-lookup"><span data-stu-id="612f4-293">06:00 PM</span></span> | <span data-ttu-id="612f4-294">2</span><span class="sxs-lookup"><span data-stu-id="612f4-294">2</span></span>    | <span data-ttu-id="612f4-295">1</span><span class="sxs-lookup"><span data-stu-id="612f4-295">1</span></span>         | <span data-ttu-id="612f4-296">2</span><span class="sxs-lookup"><span data-stu-id="612f4-296">2</span></span>            |
| <span data-ttu-id="612f4-297">下午 06:00</span><span class="sxs-lookup"><span data-stu-id="612f4-297">06:00 PM</span></span> | <span data-ttu-id="612f4-298">下午 08:00</span><span class="sxs-lookup"><span data-stu-id="612f4-298">08:00 PM</span></span> | <span data-ttu-id="612f4-299">2</span><span class="sxs-lookup"><span data-stu-id="612f4-299">2</span></span>    | <span data-ttu-id="612f4-300">1.5</span><span class="sxs-lookup"><span data-stu-id="612f4-300">1.5</span></span>       | <span data-ttu-id="612f4-301">3</span><span class="sxs-lookup"><span data-stu-id="612f4-301">3</span></span>            |
| <span data-ttu-id="612f4-302">下午 08:00</span><span class="sxs-lookup"><span data-stu-id="612f4-302">08:00 PM</span></span> | <span data-ttu-id="612f4-303">下午 09:00</span><span class="sxs-lookup"><span data-stu-id="612f4-303">09:00 PM</span></span> | <span data-ttu-id="612f4-304">1</span><span class="sxs-lookup"><span data-stu-id="612f4-304">1</span></span>    | <span data-ttu-id="612f4-305">2</span><span class="sxs-lookup"><span data-stu-id="612f4-305">2</span></span>         | <span data-ttu-id="612f4-306">2</span><span class="sxs-lookup"><span data-stu-id="612f4-306">2</span></span>            |
|          |          |      | <span data-ttu-id="612f4-307">**合计**</span><span class="sxs-lookup"><span data-stu-id="612f4-307">**Total**</span></span> | <span data-ttu-id="612f4-308">**8**</span><span class="sxs-lookup"><span data-stu-id="612f4-308">**8**</span></span>        |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
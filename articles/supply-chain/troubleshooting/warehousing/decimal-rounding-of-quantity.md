---
title: 实际更新数量的小数舍入不正确
description: 当生成装箱单时，出站负荷包含的数量与在单位中定义的小数精度不匹配。
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1e63440834f516879aa8ad711bd789e62b0ee993
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248769"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a><span data-ttu-id="ed3c7-103">实际更新数量的小数舍入不正确</span><span class="sxs-lookup"><span data-stu-id="ed3c7-103">Decimal rounding of the physical updating quantity is incorrect</span></span>

<span data-ttu-id="ed3c7-104">错误代码：SYS19589</span><span class="sxs-lookup"><span data-stu-id="ed3c7-104">Error code: SYS19589</span></span>

## <a name="symptoms"></a><span data-ttu-id="ed3c7-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="ed3c7-105">Symptoms</span></span>

<span data-ttu-id="ed3c7-106">当生成装箱单时，出站负荷包含的数量与在单位中定义的小数精度不匹配。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-106">When you generate a packing slip, the outbound load contains a quantity that doesn't match the decimal precision that is defined in the unit.</span></span>

<span data-ttu-id="ed3c7-107">当您尝试生成装箱单时，系统显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="ed3c7-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="ed3c7-108">用单位 %1 表示的实际更新数量的小数舍入不正确。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-108">Decimal rounding of the physical updating quantity in the unit %1 is incorrect.</span></span>

<span data-ttu-id="ed3c7-109">因此，您无法为负荷生成装箱单。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="ed3c7-110">原因</span><span class="sxs-lookup"><span data-stu-id="ed3c7-110">Cause</span></span>

<span data-ttu-id="ed3c7-111">系统评估装运数量的小数舍入是否与为装运单位定义的小数精度相对应。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-111">The system evaluates whether the decimal rounding of the shipping quantity corresponds to the decimal precision that is defined for the shipping unit.</span></span> <span data-ttu-id="ed3c7-112">当系统将装运数量舍入到指定的小数位数时，如果发现舍入的装运数量与实际装运数量不匹配，则无法生成装箱单。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-112">When the system rounds the shipping quantity to the specified number of decimal places, if it finds that the rounded shipping quantity doesn't match the actual shipping quantity, you can't generate the packing slip.</span></span> <span data-ttu-id="ed3c7-113">例如，如果销售数量为 1.75 千克 (kg)，但小数精度设置为 *1*，可能会发生此问题。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-113">For example, this issue might occur if the sales quantity is 1.75 kilograms (kg), but the decimal precision is set to *1*.</span></span>

## <a name="resolution"></a><span data-ttu-id="ed3c7-114">解决方法</span><span class="sxs-lookup"><span data-stu-id="ed3c7-114">Resolution</span></span>

<span data-ttu-id="ed3c7-115">负荷或装运当前处于装箱单生成失败的状态。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="ed3c7-116">要解决此问题，请完成以下任务之一：</span><span class="sxs-lookup"><span data-stu-id="ed3c7-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="ed3c7-117">查看您的负荷行，并进行调整以确保可以干净地转换数量，而不会出现小数和任何其他舍入问题。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-117">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>
- <span data-ttu-id="ed3c7-118">查看您的负荷行，并进行调整以确保单位和数量与单位的小数精度一致。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-118">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a><span data-ttu-id="ed3c7-119">查看您的负荷行，并进行调整以确保可以干净地转换数量，而不会出现小数和任何其他舍入问题</span><span class="sxs-lookup"><span data-stu-id="ed3c7-119">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues</span></span>

<span data-ttu-id="ed3c7-120">使用以下过程查看您的负荷行，并进行调整以确保可以干净地转换数量，而不会出现小数和任何其他舍入问题。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-120">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>

1. <span data-ttu-id="ed3c7-121">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="ed3c7-122">选择无法为其生成装箱单的负荷。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-122">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="ed3c7-123">在操作窗格上的 **装运和收货** 选项卡上，在 **冲销** 组中，选择 **冲销装运确认**。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-123">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="ed3c7-124">在 **负荷行** 选项卡上，为导致问题的物料选择负荷行。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-124">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="ed3c7-125">选择 **减少领料数量** 以调整领料数量。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-125">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="ed3c7-126">在  **行详细信息** 选项卡上，选择 **订单**。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-126">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="ed3c7-127">将 **数量** 字段设置为领料数量（即，**工作创建数量** 字段的值），以便可以继续生成装箱单。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-127">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="ed3c7-128">查看您的负荷行，并进行调整以确保单位和数量与单位的小数精度一致</span><span class="sxs-lookup"><span data-stu-id="ed3c7-128">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="ed3c7-129">使用以下过程查看您的负荷行，并进行调整以确保单位和数量与单位的小数精度一致。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-129">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="ed3c7-130">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="ed3c7-131">选择无法为其生成装箱单的负荷。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="ed3c7-132">在 **负荷行** 快速选项卡上，为导致问题的物料选择负荷行。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-132">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="ed3c7-133">记下 **数量** 和 **单位** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-133">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="ed3c7-134">转到 **组织管理 \> 单位 \> 单位**。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-134">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="ed3c7-135">选择无法为其生成装箱单的单位。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-135">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="ed3c7-136">根据需要调整 **小数精度** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="ed3c7-136">Adjust the value of the **Decimal precision** field as required.</span></span>

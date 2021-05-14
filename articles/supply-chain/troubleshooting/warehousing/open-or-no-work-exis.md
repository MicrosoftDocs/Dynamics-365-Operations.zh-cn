---
title: 由于工作不完整或缺失，您无法确认装运
description: 由于工作不完整或缺失，您无法确认装运
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da6388d433d6021a99840ae9781c717db1b540a9
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938428"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a><span data-ttu-id="59574-103">由于工作不完整或缺失，您无法确认装运</span><span class="sxs-lookup"><span data-stu-id="59574-103">You can't confirm a shipment because of incomplete or missing work</span></span>

<span data-ttu-id="59574-104">错误代码：WAX515</span><span class="sxs-lookup"><span data-stu-id="59574-104">Error code: WAX515</span></span>

## <a name="symptoms"></a><span data-ttu-id="59574-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="59574-105">Symptoms</span></span>

<span data-ttu-id="59574-106">当您尝试确认装运时，系统显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="59574-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="59574-107">无法确认负荷 %1 的装运，因为必须完成负荷的所有工作。</span><span class="sxs-lookup"><span data-stu-id="59574-107">The shipment for load %1 could not be confirmed because all work for the load must be complete.</span></span>

<span data-ttu-id="59574-108">因此，您无法确认负荷的装运。</span><span class="sxs-lookup"><span data-stu-id="59574-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="59574-109">原因</span><span class="sxs-lookup"><span data-stu-id="59574-109">Cause</span></span>

<span data-ttu-id="59574-110">负荷或装运当前处于装运确认失败的状态。</span><span class="sxs-lookup"><span data-stu-id="59574-110">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="59574-111">负荷必须至少有一些工作，并且所有工作的状态必须为 *已关闭* 或 *已取消*，然后您才能够确认装运。</span><span class="sxs-lookup"><span data-stu-id="59574-111">Before you can confirm the shipment, at least some work must exist for the load, and all that work must have a status of *Closed* or *Canceled*.</span></span>

## <a name="resolution"></a><span data-ttu-id="59574-112">解决方法</span><span class="sxs-lookup"><span data-stu-id="59574-112">Resolution</span></span>

<span data-ttu-id="59574-113">请检查相关销售订单或转移单的负荷或装运，确保所有相关工作均已完成或取消。</span><span class="sxs-lookup"><span data-stu-id="59574-113">Check the related sales orders or transfer orders for the load or shipment, and make sure that all the related work has been completed or canceled.</span></span>

<span data-ttu-id="59574-114">您可以在几个页面上处理装运和负荷。</span><span class="sxs-lookup"><span data-stu-id="59574-114">You can work with shipments and loads on several pages.</span></span> <span data-ttu-id="59574-115">以下小节提供了一些示例。</span><span class="sxs-lookup"><span data-stu-id="59574-115">The following subsections provide a few examples.</span></span>

### <a name="all-loads-page"></a><span data-ttu-id="59574-116">所有负荷页面</span><span class="sxs-lookup"><span data-stu-id="59574-116">All loads page</span></span>

1. <span data-ttu-id="59574-117">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="59574-117">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="59574-118">选择无法确认装运的负荷。</span><span class="sxs-lookup"><span data-stu-id="59574-118">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="59574-119">在操作窗格的 **负荷** 选项卡上的 **相关信息** 组中，选择 **工作**。</span><span class="sxs-lookup"><span data-stu-id="59574-119">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="59574-120">检查每个工作 ID 的状态。</span><span class="sxs-lookup"><span data-stu-id="59574-120">Inspect the status of each work ID.</span></span> <span data-ttu-id="59574-121">跟进每个状态为 *已关闭* 或 *已取消* 的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="59574-121">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="59574-122">当每个工作 ID 的状态均为 *已关闭* 或 *已取消* 时，请再次尝试确认装运。</span><span class="sxs-lookup"><span data-stu-id="59574-122">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-shipments-page"></a><span data-ttu-id="59574-123">所有装运页面</span><span class="sxs-lookup"><span data-stu-id="59574-123">All shipments page</span></span>

1. <span data-ttu-id="59574-124">转到 **仓库管理 \> 装运 \> 所有装运**。</span><span class="sxs-lookup"><span data-stu-id="59574-124">Go to **Warehouse management \> Shipments\> All shipments**.</span></span>
1. <span data-ttu-id="59574-125">选择无法确认的装运。</span><span class="sxs-lookup"><span data-stu-id="59574-125">Select the shipment that can't be confirmed.</span></span>
1. <span data-ttu-id="59574-126">在操作窗格的 **装运** 选项卡上，在 **工作** 组中，选择 **工作详细信息**。</span><span class="sxs-lookup"><span data-stu-id="59574-126">On the Action Pane, on the **Shipments** tab, in the **Work** group, select **Work details**.</span></span>
1. <span data-ttu-id="59574-127">检查每个工作 ID 的状态。</span><span class="sxs-lookup"><span data-stu-id="59574-127">Inspect the status of each work ID.</span></span> <span data-ttu-id="59574-128">跟进每个状态为 *已关闭* 或 *已取消* 的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="59574-128">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="59574-129">当每个工作 ID 的状态均为 *已关闭* 或 *已取消* 时，请再次尝试确认装运。</span><span class="sxs-lookup"><span data-stu-id="59574-129">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-work-page"></a><span data-ttu-id="59574-130">所有工作页面</span><span class="sxs-lookup"><span data-stu-id="59574-130">All work page</span></span>

1. <span data-ttu-id="59574-131">转到 **仓库管理 \> 工作 \> 所有工作**。</span><span class="sxs-lookup"><span data-stu-id="59574-131">Go to **Warehouse management \> Work\> All work**.</span></span>
1. <span data-ttu-id="59574-132">选择无法确认装运的订单编号的工作。</span><span class="sxs-lookup"><span data-stu-id="59574-132">Select the work for the order number that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="59574-133">在操作窗格上的 **装运** 选项卡上，在 **装运** 组中，选择 **确认装运**。</span><span class="sxs-lookup"><span data-stu-id="59574-133">On the Action Pane, on the **Shipment** tab, in the **Shipment** group, select **Confirm shipment**.</span></span>
1. <span data-ttu-id="59574-134">检查每个工作 ID 的状态。</span><span class="sxs-lookup"><span data-stu-id="59574-134">Inspect the status of each work ID.</span></span> <span data-ttu-id="59574-135">跟进每个状态为 *已关闭* 或 *已取消* 的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="59574-135">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="59574-136">当每个工作 ID 的状态均为 *已关闭* 或 *已取消* 时，请再次尝试确认装运。</span><span class="sxs-lookup"><span data-stu-id="59574-136">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

---
title: 您无法确认装运，因为存在零数量
description: 您无法确认装运，因为存在零数量
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
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938426"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a><span data-ttu-id="9e5d0-103">您无法确认装运，因为存在零数量</span><span class="sxs-lookup"><span data-stu-id="9e5d0-103">You can't confirm a shipment because there is zero quantity</span></span>

<span data-ttu-id="9e5d0-104">错误代码：LoadLineWarningUpdatedToZero</span><span class="sxs-lookup"><span data-stu-id="9e5d0-104">Error code: LoadLineWarningUpdatedToZero</span></span>

## <a name="symptoms"></a><span data-ttu-id="9e5d0-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="9e5d0-105">Symptoms</span></span>

<span data-ttu-id="9e5d0-106">当您尝试确认装运时，系统显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="9e5d0-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="9e5d0-107">由于欠交设置，物料 %1 和装运 %2 的负荷行已更新为数量为零，因此不允许装运任何数量的此物料。</span><span class="sxs-lookup"><span data-stu-id="9e5d0-107">Load line for item %1 and shipment %2 has been updated to have zero quantity due to underdelivery setup allowing not to ship any quantities for this item.</span></span>

<span data-ttu-id="9e5d0-108">因此，您无法确认负荷的装运。</span><span class="sxs-lookup"><span data-stu-id="9e5d0-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="9e5d0-109">原因</span><span class="sxs-lookup"><span data-stu-id="9e5d0-109">Cause</span></span>

<span data-ttu-id="9e5d0-110">系统根据领取的数量、负荷行数量和欠交百分比评估领取数量是否在预期限制内。</span><span class="sxs-lookup"><span data-stu-id="9e5d0-110">The system evaluates whether the picked quantity is within the expected limits, based on the picked quantity, load line quantity, and underdelivery percentage.</span></span> <span data-ttu-id="9e5d0-111">如果系统发现负荷行上的领取数量为 0（零），您将无法确认装运。</span><span class="sxs-lookup"><span data-stu-id="9e5d0-111">If the system finds that the picked quantity on the load line is 0 (zero), you can't confirm the shipment.</span></span> <span data-ttu-id="9e5d0-112">例如，如果工作已取消，并且负荷行上的欠交百分比是 100％，则可能发生此问题。</span><span class="sxs-lookup"><span data-stu-id="9e5d0-112">For example, this issue might occur if work has been canceled, and the underdelivery percentage on the load line is 100 percent.</span></span>

## <a name="resolution"></a><span data-ttu-id="9e5d0-113">解决方法</span><span class="sxs-lookup"><span data-stu-id="9e5d0-113">Resolution</span></span>

<span data-ttu-id="9e5d0-114">检查您的负荷行，确保欠交百分比和数量与领取的工作保持一致。</span><span class="sxs-lookup"><span data-stu-id="9e5d0-114">Check your load lines to make sure that the underdelivery percentage and quantities are aligned with the picked work.</span></span>

1. <span data-ttu-id="9e5d0-115">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="9e5d0-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="9e5d0-116">选择无法确认装运的负荷。</span><span class="sxs-lookup"><span data-stu-id="9e5d0-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="9e5d0-117">在 **负荷行** 快速选项卡上，为超出欠交百分比的物料选择负荷行。</span><span class="sxs-lookup"><span data-stu-id="9e5d0-117">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="9e5d0-118">根据需要调整 **欠交** 字段或 **数量** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="9e5d0-118">Adjust the value of the **Underdelivery** field or the **Quantity** field as required.</span></span>

> [!TIP]
> <span data-ttu-id="9e5d0-119">如果问题仍未解决，您可能必须为相关销售订单或转移单完成更多领料工作，直到可用数量与负荷或装运一致。</span><span class="sxs-lookup"><span data-stu-id="9e5d0-119">If the issue still isn't fixed, you might have to complete more picking work for the related sales orders or transfer orders until the available quantity is aligned with the load or shipment.</span></span>

---
title: 由于日历有问题，您无法确认装运
description: 由于日历有问题，您无法确认装运
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
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938429"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a><span data-ttu-id="7b5a6-103">由于日历有问题，您无法确认装运</span><span class="sxs-lookup"><span data-stu-id="7b5a6-103">You can't confirm a shipment because of an issue with the calendar</span></span>

<span data-ttu-id="7b5a6-104">错误代码：TRX2716</span><span class="sxs-lookup"><span data-stu-id="7b5a6-104">Error code: TRX2716</span></span>

## <a name="symptoms"></a><span data-ttu-id="7b5a6-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="7b5a6-105">Symptoms</span></span>

<span data-ttu-id="7b5a6-106">当您尝试确认装运时，系统显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="7b5a6-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="7b5a6-107">日历类型 %1 需要签入和签出预约 %2。</span><span class="sxs-lookup"><span data-stu-id="7b5a6-107">The calendar type %1 requires the appointment %2 to be checked in and out.</span></span>

<span data-ttu-id="7b5a6-108">因此，您无法确认负荷的装运。</span><span class="sxs-lookup"><span data-stu-id="7b5a6-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="7b5a6-109">原因</span><span class="sxs-lookup"><span data-stu-id="7b5a6-109">Cause</span></span>

<span data-ttu-id="7b5a6-110">负荷存在活动预约。</span><span class="sxs-lookup"><span data-stu-id="7b5a6-110">Active appointments for the load exist.</span></span> <span data-ttu-id="7b5a6-111">例如，有规则要求驾驶员签入。</span><span class="sxs-lookup"><span data-stu-id="7b5a6-111">For example, there is a rule that requires driver check-in.</span></span> <span data-ttu-id="7b5a6-112">因此，负荷当前处于装运确认失败的状态。</span><span class="sxs-lookup"><span data-stu-id="7b5a6-112">Therefore, the load is currently in a state where shipment confirmation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="7b5a6-113">解决方法</span><span class="sxs-lookup"><span data-stu-id="7b5a6-113">Resolution</span></span>

<span data-ttu-id="7b5a6-114">您必须调查并解决链接到负荷的活动预约的所有问题。</span><span class="sxs-lookup"><span data-stu-id="7b5a6-114">You must investigate and fix any issues with the active appointments that are linked to the load.</span></span>

1. <span data-ttu-id="7b5a6-115">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="7b5a6-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="7b5a6-116">选择无法确认装运的负荷。</span><span class="sxs-lookup"><span data-stu-id="7b5a6-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="7b5a6-117">在操作窗格的 **运输** 选项卡上，在 **预约** 组中，选择 **预约计划**。</span><span class="sxs-lookup"><span data-stu-id="7b5a6-117">On the Action Pane, on the **Transportation** tab, in the **Appointments** group, select **Appointment scheduling**.</span></span>
1. <span data-ttu-id="7b5a6-118">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="7b5a6-118">Follow one of these steps:</span></span>

    - <span data-ttu-id="7b5a6-119">确保驾驶员已完成预约的签入/签出。</span><span class="sxs-lookup"><span data-stu-id="7b5a6-119">Make sure that driver check-in/check-out is completed for the appointment.</span></span>
    - <span data-ttu-id="7b5a6-120">完成或取消预约。</span><span class="sxs-lookup"><span data-stu-id="7b5a6-120">Complete or cancel the appointment.</span></span>
    - <span data-ttu-id="7b5a6-121">针对相关预约规则禁用 **需要驾驶员签入** 选项。</span><span class="sxs-lookup"><span data-stu-id="7b5a6-121">Disable the **Driver check-in required** option for the related appointment rule.</span></span>

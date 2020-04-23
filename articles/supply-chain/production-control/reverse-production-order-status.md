---
title: 冲销生产订单状态
description: 此主题描述如何反转生产订单状态。
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParmStatusDecrease
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10816f0a6b651de24fc5b0f9b51a71b1c349e037
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211092"
---
# <a name="reverse-the-production-order-status"></a><span data-ttu-id="33d1a-103">冲销生产订单状态</span><span class="sxs-lookup"><span data-stu-id="33d1a-103">Reverse the production order status</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33d1a-104">此主题描述如何反转生产订单状态。</span><span class="sxs-lookup"><span data-stu-id="33d1a-104">This topic describes how to reverse production order status.</span></span> 

<span data-ttu-id="33d1a-105">如果您反转生产订单的状态，订单以及与工艺路线相关联的所有工序都反转到生产生命周期中的前一个步骤。</span><span class="sxs-lookup"><span data-stu-id="33d1a-105">If you reverse the status of a production order, the order and all operations that are associated with the routes revert to a previous step in the production life cycle.</span></span> <span data-ttu-id="33d1a-106">例如，生产订单状态为**已计划**，您将状态更改回**已创建**。</span><span class="sxs-lookup"><span data-stu-id="33d1a-106">For example, a production order has a status of **Scheduled**, and you change the status back to **Created**.</span></span> <span data-ttu-id="33d1a-107">在这种情况下，系统必须首先将状态更改为**已估计**，此状态将立即位于**已计划**之前。</span><span class="sxs-lookup"><span data-stu-id="33d1a-107">In this case, the system must first change the status to **Estimated**, which is the status that immediately precedes **Scheduled**.</span></span> <span data-ttu-id="33d1a-108">然后可以将状态更改为所需的状态，**已创建**。</span><span class="sxs-lookup"><span data-stu-id="33d1a-108">It can then change the status to the status that you want, **Created**.</span></span> <span data-ttu-id="33d1a-109">**注意：** 如果您的订单已达到状态**完工入库**，您仍然可以将该订单反转回更早的状态。</span><span class="sxs-lookup"><span data-stu-id="33d1a-109">**Note:** If your order has reached the **Report as finished** status, you can still reverse it to an earlier status.</span></span> <span data-ttu-id="33d1a-110">但是，您必须重新运行估计和工序级排产、作业级排产或两类排产同时运行，继续更新有关该订单的信息。</span><span class="sxs-lookup"><span data-stu-id="33d1a-110">However, you must re-run estimation and operations scheduling, job scheduling, or both types of scheduling, to update the information on the order.</span></span> <span data-ttu-id="33d1a-111">需要此步骤的原因在于，也必须重置剩余物料消耗量和运营资源消耗量的任何预留。</span><span class="sxs-lookup"><span data-stu-id="33d1a-111">This step is required, because any reservations of remaining item consumption and operations resource consumption must also be reset.</span></span> <span data-ttu-id="33d1a-112">本文其余部分将说明在反转生产订单的状态时，通过以下方式查看发生的情况：</span><span class="sxs-lookup"><span data-stu-id="33d1a-112">The rest of this article explains what occurs when you reverse the status of a production order in the following ways:</span></span>

-   <span data-ttu-id="33d1a-113">从**已估计**到**已创建**</span><span class="sxs-lookup"><span data-stu-id="33d1a-113">From **Estimated** to **Created**</span></span>
-   <span data-ttu-id="33d1a-114">从**已计划**到**已估计**</span><span class="sxs-lookup"><span data-stu-id="33d1a-114">From **Scheduled** to **Estimated**</span></span>
-   <span data-ttu-id="33d1a-115">从**已发布**到**已计划**</span><span class="sxs-lookup"><span data-stu-id="33d1a-115">From **Released** to **Scheduled**</span></span>
-   <span data-ttu-id="33d1a-116">从**已开始**到**已发布**</span><span class="sxs-lookup"><span data-stu-id="33d1a-116">From **Started** to **Released**</span></span>

## <a name="from-estimated-to-created"></a><span data-ttu-id="33d1a-117">从“已估计”到“已创建”</span><span class="sxs-lookup"><span data-stu-id="33d1a-117">From Estimated to Created</span></span>
<span data-ttu-id="33d1a-118">在您将生产订单的状态从**已估计**返回到**已创建**时，将删除为物料清单 (BOM) 中的物料计算的物料消耗量。</span><span class="sxs-lookup"><span data-stu-id="33d1a-118">When you reverse the status of a production order from **Estimated** to **Created**, the item consumption that was calculated for the items in the bill of materials (BOM) is removed.</span></span> <span data-ttu-id="33d1a-119">生产行上的库存交易记录将被删除，并且生产订单的物料清单行的**余额状态**字段将重置为**已结束**。</span><span class="sxs-lookup"><span data-stu-id="33d1a-119">Inventory transactions on the production line are deleted, and the **Remain status** field on the production order's BOM lines is reset to **Ended**.</span></span> <span data-ttu-id="33d1a-120">当选择**派生采购**和**派生生产**选择时，所有基础采购订单或生产订单都将被删除。</span><span class="sxs-lookup"><span data-stu-id="33d1a-120">When the **Derived purchases** and **Derived production** options are selected, any underlying purchase orders or production orders are deleted.</span></span> <span data-ttu-id="33d1a-121">如果您估计生产订单的成本，或如果您手动预留物料以便它们可以用于生产，也将删除这些交易记录。</span><span class="sxs-lookup"><span data-stu-id="33d1a-121">If you estimated the costs of the production order, or if you manually reserved items so that they could be used in production, those transactions are removed.</span></span>

## <a name="from-scheduled-to-estimated"></a><span data-ttu-id="33d1a-122">从“已计划”到“已估计”</span><span class="sxs-lookup"><span data-stu-id="33d1a-122">From Scheduled to Estimated</span></span>
<span data-ttu-id="33d1a-123">在您将生产订单的状态从**已计划**返回到**已估计**时，将删除计划的开始日期和结束日期以及开始时间和结束时间。</span><span class="sxs-lookup"><span data-stu-id="33d1a-123">When you reverse the status of a production order from **Scheduled** to **Estimated**, the scheduled start and end dates and times are removed.</span></span> <span data-ttu-id="33d1a-124">还将删除排产期间进行的产能预留，并且删除作业级排产期间创建的作业。</span><span class="sxs-lookup"><span data-stu-id="33d1a-124">Capacity reservations that were made during scheduling are removed, and jobs that were created during job scheduling are deleted.</span></span> <span data-ttu-id="33d1a-125">在**生产订单详细信息**页上记录的与工序级排产和作业级排产相关的所有信息将重置。</span><span class="sxs-lookup"><span data-stu-id="33d1a-125">All information that is recorded about operation scheduling and job scheduling on the **Production order details** page is reset.</span></span>

## <a name="from-released-to-scheduled"></a><span data-ttu-id="33d1a-126">从“已发布”到“已计划”</span><span class="sxs-lookup"><span data-stu-id="33d1a-126">From Released to Scheduled</span></span>
<span data-ttu-id="33d1a-127">在您将生产订单的状态从**已发布**返回到**已计划**时，发生的唯一变化是状态字段中的值。</span><span class="sxs-lookup"><span data-stu-id="33d1a-127">When you reverse the status of a production order from **Released** to **Scheduled**, the only change that occurs is the value in the status field.</span></span>

## <a name="from-started-to-released"></a><span data-ttu-id="33d1a-128">从“已开始”到“已发布”</span><span class="sxs-lookup"><span data-stu-id="33d1a-128">From Started to Released</span></span>
<span data-ttu-id="33d1a-129">在您将生产订单的状态从**已开始**返回到**已发布** 时，所有报告为完工入库的物料也将还原。</span><span class="sxs-lookup"><span data-stu-id="33d1a-129">When you reverse the status of a production order from **Started** to **Released**, all items that were reported as finished are reverted.</span></span> <span data-ttu-id="33d1a-130">如果物料已领料或者入库和出库交货已交付生产，则将反转这些设置。</span><span class="sxs-lookup"><span data-stu-id="33d1a-130">If material has been picked, or if inbound and outbound deliveries have been made to production, those settings are reversed.</span></span> <span data-ttu-id="33d1a-131">生产订单的物料清单行上的**余额状态**字段从**已结束**更改为**物料消耗量**。</span><span class="sxs-lookup"><span data-stu-id="33d1a-131">The **Remain status** field on the production order’s BOM lines is changed from **Ended** to **Material consumption**.</span></span> <span data-ttu-id="33d1a-132">如果登记时间或数量已报告为在生产工艺路线中的工序已完工入库，这些设置将撤消。</span><span class="sxs-lookup"><span data-stu-id="33d1a-132">If time has been registered, or if quantities have been reported as finished for the operations in the production route, those settings are reversed.</span></span> <span data-ttu-id="33d1a-133">生产工艺路线中的**余额状态**字段从**已结束**更改为**工艺路线消耗**。</span><span class="sxs-lookup"><span data-stu-id="33d1a-133">The **Remain status** field is changed from **Ended** to **Route consumption** in the production route.</span></span> <span data-ttu-id="33d1a-134">按流程过帐或在制品的所有物料的设置将反转。</span><span class="sxs-lookup"><span data-stu-id="33d1a-134">The settings for all items that are posted as in process or work in process are reversed.</span></span> <span data-ttu-id="33d1a-135">在**生产订单详细信息**页上，显示已开始或完工入库的数量的字段将重置。</span><span class="sxs-lookup"><span data-stu-id="33d1a-135">On the **Production order details** page, fields that show a quantity that was started or reported as finished are reset.</span></span> <span data-ttu-id="33d1a-136">还重置这些交易记录的日期。</span><span class="sxs-lookup"><span data-stu-id="33d1a-136">The dates for those transactions are also reset.</span></span>




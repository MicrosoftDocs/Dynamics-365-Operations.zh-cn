---
title: 将工作订单安排到特定日期和时间
description: 本主题介绍如何在资产管理中将工作订单安排到特定日期和时间。
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 827f4ca16341d29413f1b1d928965aa1919abf59
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822507"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a><span data-ttu-id="89f24-103">将工作订单安排到特定日期和时间</span><span class="sxs-lookup"><span data-stu-id="89f24-103">Schedule work order on specific date and time</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="89f24-104">如果必须将工作订单安排到特定日期 *和* 时间，可在资产管理中替换标准安排流程，并为工作订单创建特定安排。</span><span class="sxs-lookup"><span data-stu-id="89f24-104">If a work order must be scheduled on a specific date *and* time, you can override the standard scheduling process in Asset Management and create a specific schedule for a work order.</span></span>

1. <span data-ttu-id="89f24-105">单击 **资产管理** > **常用** > **工作订单** > **所有工作订单** 或 **有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="89f24-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="89f24-106">在工作订单列表的 **工作订单** 列中，单击工作订单 ID。</span><span class="sxs-lookup"><span data-stu-id="89f24-106">In the work order list, click on the Work order ID in the **Work order** column.</span></span>

3. <span data-ttu-id="89f24-107">单击 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="89f24-107">Click **Edit**.</span></span>

4. <span data-ttu-id="89f24-108">在 **工作订单标题** 快速选项卡上，在 **预计的开始时间** 和 **预计的结束时间** 字段中插入开始和结束日期和时间。</span><span class="sxs-lookup"><span data-stu-id="89f24-108">On the **Work order header** FastTab, insert start and end dates and times in the **Expected start** and **Expected end** fields.</span></span>

    ![图 1](media/05-work-order-scheduling.png)

5. <span data-ttu-id="89f24-110">在 **常规** 选项卡上，单击 **计划** 以使用标准计划流程，如果要将工作订单分配给特定工作人员，则单击 **分派**。</span><span class="sxs-lookup"><span data-stu-id="89f24-110">On the **General** tab, click **Schedule** to use the standard scheduling process, or click **Dispatch** if you want to assign the work order to a specific worker.</span></span>

6. <span data-ttu-id="89f24-111">若要替换任何现有产能预留以确保将工作订单安排在预计期间，请在 **安排工作订单** 对话框 > **有限产能** 部分中按照下图所示进行选择。</span><span class="sxs-lookup"><span data-stu-id="89f24-111">In order to override any existing capacity reservations to ensure that the work order is scheduled in the expected period, make the selections as shown in the figure below in the **Schedule work order** dialog > **Finite capacity** section.</span></span> <span data-ttu-id="89f24-112">这意味着安排流程将忽略现有产能预留，因为此工作订单必须在预计开始时间开始。</span><span class="sxs-lookup"><span data-stu-id="89f24-112">This means that the scheduling process will ignore existing capacity reservations because the work order must start on the expected start time.</span></span>

    ![图 2](media/06-work-order-scheduling.png)

7. <span data-ttu-id="89f24-114">单击 **确定** 开始安排。</span><span class="sxs-lookup"><span data-stu-id="89f24-114">Click **OK** to start scheduling.</span></span>

8. <span data-ttu-id="89f24-115">如果安排流程导致双倍预订，您将在屏幕中看到一条消息，并且可以调整相关工作订单。</span><span class="sxs-lookup"><span data-stu-id="89f24-115">If the scheduling process results in double bookings, you will see a message on the screen, and you can adjust the related work orders.</span></span>

>[!NOTE]
><span data-ttu-id="89f24-116">若要将某位维护工人安排给此工作订单，该维护工人必须在预计开始日期和时间有空。</span><span class="sxs-lookup"><span data-stu-id="89f24-116">In order to schedule a maintenance worker for the work order, that maintenance worker must be available at the expected start date and time.</span></span> <span data-ttu-id="89f24-117">工人可用性在[工人日历](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md)中设置。</span><span class="sxs-lookup"><span data-stu-id="89f24-117">Worker availability is set up in the [worker calendar](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span></span> 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
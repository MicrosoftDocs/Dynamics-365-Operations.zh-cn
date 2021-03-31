---
title: 分派工作订单
description: 本主题介绍如何在资产管理中分派工作订单。
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetScheduledExecution
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cd9965ec8f3c3ff58f16b53abc8b9b114444946d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215002"
---
# <a name="dispatch-work-order"></a><span data-ttu-id="b03d4-103">分派工作订单</span><span class="sxs-lookup"><span data-stu-id="b03d4-103">Dispatch work order</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b03d4-104">可使用 **分派** 功能将一个工作订单或工作订单作业分配给一位工人。</span><span class="sxs-lookup"><span data-stu-id="b03d4-104">You can schedule one work order or work order jobs to one worker using the **Dispatch** functionality.</span></span>

1. <span data-ttu-id="b03d4-105">单击 **资产管理** > **常用** > **工作订单** > **所有工作订单** 或 **有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="b03d4-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="b03d4-106">在列表中选择工作订单。</span><span class="sxs-lookup"><span data-stu-id="b03d4-106">Select the work order in the list.</span></span>

3. <span data-ttu-id="b03d4-107">在 **常规** 选项卡上，单击 **分派**。</span><span class="sxs-lookup"><span data-stu-id="b03d4-107">On the **General** tab, click **Dispatch**.</span></span>

4. <span data-ttu-id="b03d4-108">在 **分派工作订单** 对话框的 **工作人员** 字段中，选择工作人员。</span><span class="sxs-lookup"><span data-stu-id="b03d4-108">In the **Schedule work order** dialog, select the worker in the **Worker** field.</span></span>

5. <span data-ttu-id="b03d4-109">如果预计工时与预测工时不同，可在 **计划工时** 字段中插入预计工时。</span><span class="sxs-lookup"><span data-stu-id="b03d4-109">In the **Schedule hours** field, you can insert expected work hours in case expected work hours differ from forecast hours.</span></span>

6. <span data-ttu-id="b03d4-110">如果需要，可在 **计划开始时间** 字段中编辑开始日期和时间。</span><span class="sxs-lookup"><span data-stu-id="b03d4-110">In the **Scheduled start** field, you can edit start date and time, if required.</span></span>

7. <span data-ttu-id="b03d4-111">如果计划流程应该遵守与已经为其他作业安排的资源有关的产能限制，请确保 **资产**、**工具** 和 **工作人员** 切换按钮设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="b03d4-111">If the scheduling process should observe capacity limitations regarding resources already scheduled on other jobs, make sure that the **Asset**, **Tool**, and **Worker** toggle buttons are set to **Yes**.</span></span> <span data-ttu-id="b03d4-112">如果要查看有关计划流程的详细信息，请在 **详细** 切换按钮上选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="b03d4-112">If you want to see detailed information about the scheduling process, select **Yes** on the **Verbose** toggle button.</span></span> <span data-ttu-id="b03d4-113">这意味着在信息日志中显示有关为工作订单计算出的分数的详细信息。</span><span class="sxs-lookup"><span data-stu-id="b03d4-113">This means detailed information about the calculated scores on the work order is shown in the Infolog.</span></span>

8. <span data-ttu-id="b03d4-114">若要在日历中忽略休息日，请在 **忽略计划** 切换按钮上选择 **是**（适用于资产、工人和工具）。</span><span class="sxs-lookup"><span data-stu-id="b03d4-114">Select **Yes** on the **Ignore schedule** toggle button to ignore closed days in the calendar (applies to asset, worker, and tools).</span></span> <span data-ttu-id="b03d4-115">若要忽略可能在工作订单中已选择的有关计划的限制，请在 **忽略已计划执行** 切换按钮上选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="b03d4-115">Select **Yes** on the **Ignore scheduled execution** toggle button to ignore limitations that may have been selected on the work order regarding scheduling.</span></span> 

    <span data-ttu-id="b03d4-116">有关设置已计划执行的信息，请参阅[已计划执行](../setup-for-work-orders/scheduled-execution.md)部分。</span><span class="sxs-lookup"><span data-stu-id="b03d4-116">For information on the setup of scheduled execution, see the [Scheduled execution](../setup-for-work-orders/scheduled-execution.md) section.</span></span>

9. <span data-ttu-id="b03d4-117">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b03d4-117">Click **OK**.</span></span> <span data-ttu-id="b03d4-118">将把工作订单生命周期状态自动更新为 **已计划** 生命周期状态指定的 **资产管理** > **设置** > **工作订单** > **生命周期模型**。</span><span class="sxs-lookup"><span data-stu-id="b03d4-118">The work order lifecycle state is automatically updated to the **Scheduled** lifecycle state specified **Asset management** > **Setup** > **Work orders** > **Lifecycle models**.</span></span>

<span data-ttu-id="b03d4-119">下图显示 **计划工作订单** 对话框中选择的分派的示例。</span><span class="sxs-lookup"><span data-stu-id="b03d4-119">The figure below shows an example of dispatch selections in the **Schedule work order** dialog.</span></span>

![图 1](media/04-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="b03d4-121">如果要删除对工作订单的计划，在 **所有工作订单** 中选择工作订单，然后单击 **常规** 选项卡上的 **删除计划**。如果删除计划，请记住要手动更新工作订单生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="b03d4-121">If you want to delete the schedule on a work order, select the work order in **All work orders**, and then click **Delete schedule** on the **General** tab. Remember to manually update the work order lifecycle state if you delete the schedule.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
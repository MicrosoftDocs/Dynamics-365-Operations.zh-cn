---
title: 工作仍然处于锁定状态
description: 工作仍然处于锁定状态
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924122"
---
# <a name="work-remains-blocked"></a><span data-ttu-id="9c2f9-103">工作仍然处于锁定状态</span><span class="sxs-lookup"><span data-stu-id="9c2f9-103">Work remains blocked</span></span>

<span data-ttu-id="9c2f9-104">错误代码：WHSWorkBlockingExecutingWaveReason_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="9c2f9-104">Error code: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="9c2f9-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="9c2f9-105">Symptoms</span></span>

<span data-ttu-id="9c2f9-106">系统将显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="9c2f9-106">The system shows the following error message:</span></span>

> <span data-ttu-id="9c2f9-107">工作 %1 仍然受阻，因为相关波次 %2 的状态为 %3。</span><span class="sxs-lookup"><span data-stu-id="9c2f9-107">Work %1 remains blocked because the related wave %2 has status %3.</span></span>

## <a name="cause"></a><span data-ttu-id="9c2f9-108">原因</span><span class="sxs-lookup"><span data-stu-id="9c2f9-108">Cause</span></span>

<span data-ttu-id="9c2f9-109">工作当前正在波次上处理，无法解锁，如以下情况之一所示：</span><span class="sxs-lookup"><span data-stu-id="9c2f9-109">The work is currently being processed on a wave and can't be unblocked, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="9c2f9-110">在 **锁定原因** 选项卡上，一或多行的 **工作锁定原因** 字段设置为 *处理波次*。</span><span class="sxs-lookup"><span data-stu-id="9c2f9-110">On the **Blocking reasons** tab, the **Work blocking reason** field for one or more lines is set to *Processing wave*.</span></span>
- <span data-ttu-id="9c2f9-111">当您在操作窗格的 **相关信息** 选项卡上的 **相关信息** 组中选择 **波次** 时，**波次状态** 字段将设置为 *正在处理*。</span><span class="sxs-lookup"><span data-stu-id="9c2f9-111">When you select **Wave** in the **Related information** group on the **Related information** tab of the Action Pane, the **Wave status** field is set to *Processing*.</span></span>

## <a name="resolution"></a><span data-ttu-id="9c2f9-112">解决方法</span><span class="sxs-lookup"><span data-stu-id="9c2f9-112">Resolution</span></span>

<span data-ttu-id="9c2f9-113">在操作窗格的 **相关信息** 选项卡上的 **相关信息** 组中，选择 **波次**。</span><span class="sxs-lookup"><span data-stu-id="9c2f9-113">On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="9c2f9-114">然后，在 **波次** 页上，在操作窗格上的 **波次** 选项卡上，在 **波次** 组中，选择 **清理波次数据**。</span><span class="sxs-lookup"><span data-stu-id="9c2f9-114">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="9c2f9-115">解决方法</span><span class="sxs-lookup"><span data-stu-id="9c2f9-115">Workaround</span></span>

<span data-ttu-id="9c2f9-116">如果上述步骤不能解决问题，您可以按照以下步骤取消工作。</span><span class="sxs-lookup"><span data-stu-id="9c2f9-116">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="9c2f9-117">转到 **仓库管理 \> 定期任务 \> 清理 \> 取消工作**。</span><span class="sxs-lookup"><span data-stu-id="9c2f9-117">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="9c2f9-118">在 **工作 ID** 字段中，指定您要取消的当前的 **工作状态** 值为 *打开*、*进行中*、*已取消*、*已合并* 或 *已关闭* 的工作的 ID。</span><span class="sxs-lookup"><span data-stu-id="9c2f9-118">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="9c2f9-119">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="9c2f9-119">Select **OK**.</span></span>
1. <span data-ttu-id="9c2f9-120">选择 **是** 确认要取消该工作。</span><span class="sxs-lookup"><span data-stu-id="9c2f9-120">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="9c2f9-121">有关详细信息，请参阅[取消要进行异常处理的仓库工作](../../warehousing/cancel-warehouse-work.md)。</span><span class="sxs-lookup"><span data-stu-id="9c2f9-121">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

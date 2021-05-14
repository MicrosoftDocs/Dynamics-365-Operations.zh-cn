---
title: 波次不符合清理条件
description: 波次不符合清理条件
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924319"
---
# <a name="wave-isnt-eligible-for-cleanup"></a><span data-ttu-id="cbfc7-103">波次不符合清理条件</span><span class="sxs-lookup"><span data-stu-id="cbfc7-103">Wave isn't eligible for cleanup</span></span>

<span data-ttu-id="cbfc7-104">错误代码：WaveNotEligibleForCleanup</span><span class="sxs-lookup"><span data-stu-id="cbfc7-104">Error code: WaveNotEligibleForCleanup</span></span>

## <a name="symptoms"></a><span data-ttu-id="cbfc7-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="cbfc7-105">Symptoms</span></span>

<span data-ttu-id="cbfc7-106">系统将显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="cbfc7-106">The system shows the following error message:</span></span>

> <span data-ttu-id="cbfc7-107">波次 %1 不符合清除条件。</span><span class="sxs-lookup"><span data-stu-id="cbfc7-107">Wave %1 is not eligible for cleanup.</span></span>

<span data-ttu-id="cbfc7-108">波次数据无法清理。</span><span class="sxs-lookup"><span data-stu-id="cbfc7-108">The wave data can't be cleaned up.</span></span>  

## <a name="cause"></a><span data-ttu-id="cbfc7-109">原因</span><span class="sxs-lookup"><span data-stu-id="cbfc7-109">Cause</span></span>

<span data-ttu-id="cbfc7-110">当前正在处理波次，如以下情况之一所示：</span><span class="sxs-lookup"><span data-stu-id="cbfc7-110">The wave is currently being processed, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="cbfc7-111">**波次状态** 字段设置为 *正在执行*。</span><span class="sxs-lookup"><span data-stu-id="cbfc7-111">The **Wave status** field is set to *Executing*.</span></span>
- <span data-ttu-id="cbfc7-112">当您在操作窗格的 **波次** 选项卡上的 **波次** 组中选择 **批处理作业** 时，**状态** 字段未设置为 *已结束*、*错误* 或 *已取消*。</span><span class="sxs-lookup"><span data-stu-id="cbfc7-112">When you select **Batch job** in the **Wave** group on the **Wave** tab of the Action Pane, the **Status** field isn't set to *Ended*, *Error*, or *Canceled*.</span></span> <span data-ttu-id="cbfc7-113">因此，批处理作业当前正在运行。</span><span class="sxs-lookup"><span data-stu-id="cbfc7-113">Therefore, a batch job is currently running.</span></span>

## <a name="resolution"></a><span data-ttu-id="cbfc7-114">解决方法</span><span class="sxs-lookup"><span data-stu-id="cbfc7-114">Resolution</span></span>

<span data-ttu-id="cbfc7-115">在操作窗格上，在 **波次** 选项卡上，在 **波次** 组中，选择 **批处理作业**，然后执行以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="cbfc7-115">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Batch job**, and then follow one of these steps:</span></span>

- <span data-ttu-id="cbfc7-116">如果 **状态** 字段设置为 *正在执行*：在操作窗格上，在 **批处理作业** 选项卡上，在 **批处理作业** 组中，选择 **查看任务**。</span><span class="sxs-lookup"><span data-stu-id="cbfc7-116">If the **Status** field is set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Batch job** group, select **View tasks**.</span></span> <span data-ttu-id="cbfc7-117">您可以刷新 **批处理任务** 页来跟踪进度。</span><span class="sxs-lookup"><span data-stu-id="cbfc7-117">You can follow the progress by refreshing the **Batch tasks** page.</span></span>
- <span data-ttu-id="cbfc7-118">如果 **状态** 字段未设置为 *正在执行*：在操作窗格上，在 **批处理作业** 选项卡上，在 **功能** 组中，选择 **更改状态**。</span><span class="sxs-lookup"><span data-stu-id="cbfc7-118">If the **Status** field isn't set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Functions** group, select **Change status**.</span></span> <span data-ttu-id="cbfc7-119">在 **选择新状态** 字段中，选择 *正在等待*。</span><span class="sxs-lookup"><span data-stu-id="cbfc7-119">In the **Select new status** field, select *Waiting*.</span></span> <span data-ttu-id="cbfc7-120">然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="cbfc7-120">Then select **OK**.</span></span>

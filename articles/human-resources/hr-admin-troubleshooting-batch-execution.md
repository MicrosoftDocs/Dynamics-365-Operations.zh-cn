---
title: 重置卡住的批处理作业
description: 本主题说明如何解决卡住的批处理作业的问题。
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: d0b12908993070a41d21ac57d6fb504fc6e3b06a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053507"
---
# <a name="reset-stuck-batch-jobs"></a><span data-ttu-id="ecc2e-103">重置卡住的批处理作业</span><span class="sxs-lookup"><span data-stu-id="ecc2e-103">Reset stuck batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a><span data-ttu-id="ecc2e-104">签发</span><span class="sxs-lookup"><span data-stu-id="ecc2e-104">Issue</span></span>

<span data-ttu-id="ecc2e-105">Microsoft Dynamics 365 Human Resources 可能遇到批处理作业在 **正在执行** 或 **正在取消** 状态下卡住而无法完成的问题。</span><span class="sxs-lookup"><span data-stu-id="ecc2e-105">Microsoft Dynamics 365 Human Resources can experience issues with batch jobs that are stuck in either an **Executing** or **Canceling** state and don't complete.</span></span>

## <a name="resolution"></a><span data-ttu-id="ecc2e-106">解决方法</span><span class="sxs-lookup"><span data-stu-id="ecc2e-106">Resolution</span></span>

<span data-ttu-id="ecc2e-107">当批处理作业在 **正在执行** 或 **正在取消** 状态下卡主时，您可以通过强制取消作业来重置状态。</span><span class="sxs-lookup"><span data-stu-id="ecc2e-107">When a batch job is stuck in an **Executing** or **Canceling** state, you can reset the status by forcing the cancellation of the job.</span></span> <span data-ttu-id="ecc2e-108">取消后，可以通过将批处理作业设置为 **正在等待** 状态来重置它。</span><span class="sxs-lookup"><span data-stu-id="ecc2e-108">After you cancel it, you can reset the batch job by setting it to a **Waiting** status.</span></span> <span data-ttu-id="ecc2e-109">然后，它将再次提取以在下一个计划的批处理运行中执行。</span><span class="sxs-lookup"><span data-stu-id="ecc2e-109">It will then be picked up again for execution in the next scheduled batch run.</span></span>

1. <span data-ttu-id="ecc2e-110">在 **系统管理** 工作区中，选择 **链接** 页面，然后选择 **批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="ecc2e-110">In the **System administration** workspace, select the **Links** page, and select **Batch jobs**.</span></span>

2. <span data-ttu-id="ecc2e-111">在 **批处理作业** 列表页面上，选择需要重置的作业。</span><span class="sxs-lookup"><span data-stu-id="ecc2e-111">On the **Batch job** list page, select the job that needs to be reset.</span></span>

3. <span data-ttu-id="ecc2e-112">在操作功能区上，选择 **强制取消**，然后确认操作。</span><span class="sxs-lookup"><span data-stu-id="ecc2e-112">On the action ribbon, select **Force cancel**, and confirm the action.</span></span>

   > [!NOTE]
   > <span data-ttu-id="ecc2e-113">**强制取消** 操作仅在所选批处理作业具有 **正在执行** 或 **正在取消** 状态，并且该作业没有运行批处理执行或取消流程时可用。</span><span class="sxs-lookup"><span data-stu-id="ecc2e-113">The **Force cancel** action is only available when the selected batch job has a status of either **Executing** or **Canceling**, and no batch execution or cancellation processes are running for the job.</span></span>

4. <span data-ttu-id="ecc2e-114">在操作功能区上，选择 **更改状态**。</span><span class="sxs-lookup"><span data-stu-id="ecc2e-114">On the action ribbon, select **Change status**.</span></span>

5. <span data-ttu-id="ecc2e-115">在 **选择新状态** 页面上，选择 **正在等待**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="ecc2e-115">On the **Select new status** page, select **Waiting**, and then select **OK**.</span></span>

   ![选择新的批处理作业状态](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a><span data-ttu-id="ecc2e-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="ecc2e-117">See also</span></span>

[<span data-ttu-id="ecc2e-118">通过安排在下班后执行批处理作业而优化性能</span><span class="sxs-lookup"><span data-stu-id="ecc2e-118">Optimize performance by scheduling batch jobs after hours</span></span>](hr-admin-troubleshooting-batch-jobs.md)<br>
[<span data-ttu-id="ecc2e-119">使用自动清理任务优化性能</span><span class="sxs-lookup"><span data-stu-id="ecc2e-119">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

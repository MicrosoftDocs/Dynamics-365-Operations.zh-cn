---
title: 工作已被锁定，无法取消
description: 工作已被锁定，无法取消
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924271"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a><span data-ttu-id="9eecc-103">工作已被锁定，无法取消</span><span class="sxs-lookup"><span data-stu-id="9eecc-103">Work can't be canceled because it's blocked</span></span>

<span data-ttu-id="9eecc-104">错误代码：WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="9eecc-104">Error code: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="9eecc-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="9eecc-105">Symptoms</span></span>

<span data-ttu-id="9eecc-106">系统将显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="9eecc-106">The system shows the following error message:</span></span>

> <span data-ttu-id="9eecc-107">工作 %1 无法取消，因为它由原因类型 %2 锁定。</span><span class="sxs-lookup"><span data-stu-id="9eecc-107">Work %1 cannot be cancelled because it is blocked by reason type %2.</span></span> <span data-ttu-id="9eecc-108">必须先解锁该工作，然后才能取消。</span><span class="sxs-lookup"><span data-stu-id="9eecc-108">The work must be unblocked before it can be cancelled.</span></span>

## <a name="cause"></a><span data-ttu-id="9eecc-109">原因</span><span class="sxs-lookup"><span data-stu-id="9eecc-109">Cause</span></span>

<span data-ttu-id="9eecc-110">工作已被锁定，无法取消。</span><span class="sxs-lookup"><span data-stu-id="9eecc-110">The work is blocked and can't be canceled.</span></span>

<span data-ttu-id="9eecc-111">在 **工作** 页上的 **常规** 选项卡上，**已锁定** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="9eecc-111">On the **Work** page, on the **General** tab, the **Blocked** option is set to *Yes*.</span></span> <span data-ttu-id="9eecc-112">此设置指示工作已被锁定。</span><span class="sxs-lookup"><span data-stu-id="9eecc-112">This setting indicates that the work is blocked.</span></span> <span data-ttu-id="9eecc-113">**锁定原因** 选项卡显示为何工作被锁定。</span><span class="sxs-lookup"><span data-stu-id="9eecc-113">The **Blocking reasons** tab shows why the work was blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="9eecc-114">解决方法</span><span class="sxs-lookup"><span data-stu-id="9eecc-114">Resolution</span></span>

<span data-ttu-id="9eecc-115">要解锁工作，选择 **锁定原因** 选项卡，然后按照下列步骤之一操作：</span><span class="sxs-lookup"><span data-stu-id="9eecc-115">To unblock the work, select the **Blocking reasons** tab, and then follow one of these steps:</span></span>

- <span data-ttu-id="9eecc-116">如果 **工作锁定原因** 字段设置为 *未定义原因*：在操作窗格的 **工作** 选项卡上，在 **工作** 组中，选择 **解锁工作**。</span><span class="sxs-lookup"><span data-stu-id="9eecc-116">If the **Work blocking reason** field is set to *Undefined reason*: On the Action Pane, on the **Work** tab, in the **Work** group, select **Unblock work**.</span></span>
- <span data-ttu-id="9eecc-117">如果 **工作锁定原因** 字段设置为 *处理波次*：在操作窗格的 **相关信息** 选项卡上，在 **相关信息** 组中，选择 **波次**。</span><span class="sxs-lookup"><span data-stu-id="9eecc-117">If the **Work blocking reason** field is set to *Processing wave*: On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="9eecc-118">然后，在 **波次** 页上，在操作窗格上的 **波次** 选项卡上，在 **波次** 组中，选择 **清理波次数据**。</span><span class="sxs-lookup"><span data-stu-id="9eecc-118">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="9eecc-119">解决方法</span><span class="sxs-lookup"><span data-stu-id="9eecc-119">Workaround</span></span>

<span data-ttu-id="9eecc-120">如果上述步骤不能解决问题，您可以按照以下步骤取消工作。</span><span class="sxs-lookup"><span data-stu-id="9eecc-120">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="9eecc-121">转到 **仓库管理 \> 定期任务 \> 清理 \> 取消工作**。</span><span class="sxs-lookup"><span data-stu-id="9eecc-121">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="9eecc-122">在 **工作 ID** 字段中，指定您要取消的当前的 **工作状态** 值为 *打开*、*进行中*、*已取消*、*已合并* 或 *已关闭* 的工作的 ID。</span><span class="sxs-lookup"><span data-stu-id="9eecc-122">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="9eecc-123">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="9eecc-123">Select **OK**.</span></span>
1. <span data-ttu-id="9eecc-124">选择 **是** 确认要取消该工作。</span><span class="sxs-lookup"><span data-stu-id="9eecc-124">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="9eecc-125">有关详细信息，请参阅[取消要进行异常处理的仓库工作](../../warehousing/cancel-warehouse-work.md)。</span><span class="sxs-lookup"><span data-stu-id="9eecc-125">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

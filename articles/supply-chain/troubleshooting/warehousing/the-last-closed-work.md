---
title: 最后关闭的工作行必须为“放置”
description: 最后关闭的工作行必须为“放置”
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924367"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a><span data-ttu-id="c6d8d-103">最后关闭的工作行必须为“放置”</span><span class="sxs-lookup"><span data-stu-id="c6d8d-103">The last closed work line must be a put</span></span>

<span data-ttu-id="c6d8d-104">错误代码：WAX1285</span><span class="sxs-lookup"><span data-stu-id="c6d8d-104">Error code: WAX1285</span></span>

## <a name="symptoms"></a><span data-ttu-id="c6d8d-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="c6d8d-105">Symptoms</span></span>

<span data-ttu-id="c6d8d-106">系统将显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="c6d8d-106">The system shows the following error message:</span></span>

> <span data-ttu-id="c6d8d-107">最后关闭的工作行必须为“放置”。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-107">The last closed work line must be a put.</span></span>

## <a name="cause"></a><span data-ttu-id="c6d8d-108">原因</span><span class="sxs-lookup"><span data-stu-id="c6d8d-108">Cause</span></span>

<span data-ttu-id="c6d8d-109">工作无法在当前状态下取消。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="c6d8d-110">在最后一个工作行上，**工作状态** 字段设置为 *已关闭*，但 **工作类型** 字段未设置为 *放置*。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-110">On the last work line, the **Work status** field is set to *Closed*, but the **Work type** field isn't set to *Put*.</span></span>

## <a name="resolution"></a><span data-ttu-id="c6d8d-111">解决方法</span><span class="sxs-lookup"><span data-stu-id="c6d8d-111">Resolution</span></span>

<span data-ttu-id="c6d8d-112">要取消工作，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="c6d8d-113">转到 **仓库管理 \> 定期任务 \> 清理 \> 取消工作**。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="c6d8d-114">在 **工作 ID** 字段中，指定要取消的工作的 ID。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="c6d8d-115">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-115">Select **OK**.</span></span>
1. <span data-ttu-id="c6d8d-116">选择 **是** 确认要取消该工作。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="c6d8d-117">有关详细信息，请参阅[取消要进行异常处理的仓库工作](../../warehousing/cancel-warehouse-work.md)。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

---
title: 工作由于其状态无法取消
description: 工作由于其状态无法取消
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924247"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a><span data-ttu-id="78f35-103">工作由于其状态无法取消</span><span class="sxs-lookup"><span data-stu-id="78f35-103">Work can't be canceled because of its status</span></span>

<span data-ttu-id="78f35-104">错误代码：WAX2190</span><span class="sxs-lookup"><span data-stu-id="78f35-104">Error code: WAX2190</span></span>

## <a name="symptoms"></a><span data-ttu-id="78f35-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="78f35-105">Symptoms</span></span>

<span data-ttu-id="78f35-106">系统将显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="78f35-106">The system shows the following error message:</span></span>

> <span data-ttu-id="78f35-107">无法取消工作 %1，因为其状态为 %2。</span><span class="sxs-lookup"><span data-stu-id="78f35-107">You cannot cancel work %1 because it has a status of %2.</span></span>

## <a name="cause"></a><span data-ttu-id="78f35-108">原因</span><span class="sxs-lookup"><span data-stu-id="78f35-108">Cause</span></span>

<span data-ttu-id="78f35-109">工作无法在当前状态下取消。</span><span class="sxs-lookup"><span data-stu-id="78f35-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="78f35-110">工作标头或工作行没有预期的 **工作状态** 值。</span><span class="sxs-lookup"><span data-stu-id="78f35-110">The work header or work lines don't have the expected **Work status** value.</span></span> <span data-ttu-id="78f35-111">工作标头上的 **工作状态** 字段未设置为 *打开* 或 *进行中*。</span><span class="sxs-lookup"><span data-stu-id="78f35-111">The **Work status** field on the work header isn't set to *Open* or *In progress*.</span></span>

## <a name="resolution"></a><span data-ttu-id="78f35-112">解决方法</span><span class="sxs-lookup"><span data-stu-id="78f35-112">Resolution</span></span>

<span data-ttu-id="78f35-113">要取消工作，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="78f35-113">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="78f35-114">转到 **仓库管理 \> 定期任务 \> 清理 \> 取消工作**。</span><span class="sxs-lookup"><span data-stu-id="78f35-114">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="78f35-115">在 **工作 ID** 字段中，指定要取消的工作的 ID。</span><span class="sxs-lookup"><span data-stu-id="78f35-115">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="78f35-116">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="78f35-116">Select **OK**.</span></span>
1. <span data-ttu-id="78f35-117">选择 **是** 确认要取消该工作。</span><span class="sxs-lookup"><span data-stu-id="78f35-117">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="78f35-118">有关详细信息，请参阅[取消要进行异常处理的仓库工作](../../warehousing/cancel-warehouse-work.md)。</span><span class="sxs-lookup"><span data-stu-id="78f35-118">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

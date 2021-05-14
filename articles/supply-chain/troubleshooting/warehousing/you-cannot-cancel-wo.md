---
title: 您无法取消用户正在进行的工作
description: 您无法取消用户正在进行的工作
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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924393"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a><span data-ttu-id="8eead-103">您无法取消用户正在进行的工作</span><span class="sxs-lookup"><span data-stu-id="8eead-103">You can't cancel work that is on a user</span></span>

<span data-ttu-id="8eead-104">错误代码：WAX708</span><span class="sxs-lookup"><span data-stu-id="8eead-104">Error code: WAX708</span></span>

## <a name="symptoms"></a><span data-ttu-id="8eead-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="8eead-105">Symptoms</span></span>

<span data-ttu-id="8eead-106">系统将显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="8eead-106">The system shows the following error message:</span></span>

> <span data-ttu-id="8eead-107">无法取消用户正在进行的工作。</span><span class="sxs-lookup"><span data-stu-id="8eead-107">You cannot cancel work that is on a user.</span></span>

## <a name="cause"></a><span data-ttu-id="8eead-108">原因</span><span class="sxs-lookup"><span data-stu-id="8eead-108">Cause</span></span>

<span data-ttu-id="8eead-109">工作已被用户锁定，无法取消。</span><span class="sxs-lookup"><span data-stu-id="8eead-109">The work is locked by a user and can't be canceled.</span></span> <span data-ttu-id="8eead-110">要确认这一点，打开工作 ID，然后打开 **常规** 选项卡。如果工作被锁定，**工作状态** 字段将设置为 *进行中*，**锁定者** 字段将设置为用户 ID。</span><span class="sxs-lookup"><span data-stu-id="8eead-110">To confirm this, open the work ID and then open the **General** tab. If the work is locked, the **Work status** field will be set to *In progress*, and the **Locked by** field will be set to a user ID.</span></span>

## <a name="resolution"></a><span data-ttu-id="8eead-111">解决方法</span><span class="sxs-lookup"><span data-stu-id="8eead-111">Resolution</span></span>

<span data-ttu-id="8eead-112">要取消工作，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="8eead-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="8eead-113">转到 **仓库管理 \> 定期任务 \> 清理 \> 取消工作**。</span><span class="sxs-lookup"><span data-stu-id="8eead-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="8eead-114">在 **工作 ID** 字段中，指定要取消的工作的 ID。</span><span class="sxs-lookup"><span data-stu-id="8eead-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="8eead-115">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="8eead-115">Select **OK**.</span></span>
1. <span data-ttu-id="8eead-116">选择 **是** 确认要取消该工作。</span><span class="sxs-lookup"><span data-stu-id="8eead-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="8eead-117">有关详细信息，请参阅[取消要进行异常处理的仓库工作](../../warehousing/cancel-warehouse-work.md)。</span><span class="sxs-lookup"><span data-stu-id="8eead-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

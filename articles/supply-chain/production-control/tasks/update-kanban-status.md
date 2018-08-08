--- 
title: "更新看板状态"
description: "在看板由错误清空或收到的看板需要清空时，需要更新看板状态。"
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 413f53a9ecc58439d4094d141bab4b510725b76e
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---
# <a name="update-kanban-status"></a><span data-ttu-id="e957a-103">更新看板状态</span><span class="sxs-lookup"><span data-stu-id="e957a-103">Update kanban status</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e957a-104">在看板由错误清空或收到的看板需要清空时，需要更新看板状态。</span><span class="sxs-lookup"><span data-stu-id="e957a-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="e957a-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="e957a-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e957a-106">此过程专门面向车间主管。</span><span class="sxs-lookup"><span data-stu-id="e957a-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="e957a-107">查找看板。</span><span class="sxs-lookup"><span data-stu-id="e957a-107">Find the kanban.</span></span>
1. <span data-ttu-id="e957a-108">转到“生产控制”>“看板”>“看板”。</span><span class="sxs-lookup"><span data-stu-id="e957a-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="e957a-109">打开处理单元状态列筛选器。</span><span class="sxs-lookup"><span data-stu-id="e957a-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="e957a-110">单击“清除”。</span><span class="sxs-lookup"><span data-stu-id="e957a-110">Click Clear.</span></span>
    * <span data-ttu-id="e957a-111">这重置筛选器。</span><span class="sxs-lookup"><span data-stu-id="e957a-111">This resets the filters.</span></span>  
4. <span data-ttu-id="e957a-112">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="e957a-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e957a-113">例如，在“卡号”字段中筛选值 '000149'。</span><span class="sxs-lookup"><span data-stu-id="e957a-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="e957a-114">将“已清空”状态更改为“已收到”状态</span><span class="sxs-lookup"><span data-stu-id="e957a-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="e957a-115">单击“还原空的物料处理单元”。</span><span class="sxs-lookup"><span data-stu-id="e957a-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="e957a-116">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e957a-116">Click OK.</span></span>
    * <span data-ttu-id="e957a-117">请注意，处理单元状态为“已收到”。</span><span class="sxs-lookup"><span data-stu-id="e957a-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="e957a-118">将“已收到”状态更改为“已清空”状态</span><span class="sxs-lookup"><span data-stu-id="e957a-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="e957a-119">单击“空看板”。</span><span class="sxs-lookup"><span data-stu-id="e957a-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="e957a-120">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="e957a-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e957a-121">请注意，处理单元状态为“已清空”。</span><span class="sxs-lookup"><span data-stu-id="e957a-121">Notice that the Handling unit status is Emptied.</span></span>  



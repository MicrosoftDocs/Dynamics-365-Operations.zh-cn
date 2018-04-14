--- 
title: "计算各个法人的固定资产折旧"
description: "此过程显示如何设置和运行多个法人的折旧过程。"
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 662554b1b6bed63e5017aad3a292dad7a2f0bcea
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="713c3-103">计算各个法人的固定资产折旧</span><span class="sxs-lookup"><span data-stu-id="713c3-103">Calculate fixed asset depreciation across legal entities</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="713c3-104">固定资产折旧可以一步跨多个法人运行。</span><span class="sxs-lookup"><span data-stu-id="713c3-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="713c3-105">此过程显示如何设置和运行多个法人的过程。</span><span class="sxs-lookup"><span data-stu-id="713c3-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="713c3-106">它使用会计师角色。</span><span class="sxs-lookup"><span data-stu-id="713c3-106">It uses the accountant role.</span></span>  

<span data-ttu-id="713c3-107">此记录使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="713c3-107">This recording uses the USMF demo company.</span></span>


<span data-ttu-id="713c3-108">步骤 (16) 子任务：设置跨公司折旧运行日记帐。</span><span class="sxs-lookup"><span data-stu-id="713c3-108">Steps (16) Sub-task: Set up cross company depreciation run journals.</span></span> 

1. <span data-ttu-id="713c3-109">首先，必须设置用于在每个法人中运行的跨公司折扣的日记帐。</span><span class="sxs-lookup"><span data-stu-id="713c3-109">First, you must set up the journals to be used in the cross company depreciation run in each legal entity.</span></span> <span data-ttu-id="713c3-110">转到固定资产>设置>固定资产参数。</span><span class="sxs-lookup"><span data-stu-id="713c3-110">Go to Fixed assets > Setup > Fixed assets parameters.</span></span> 
2. <span data-ttu-id="713c3-111">展开“固定资产方案”部分。</span><span class="sxs-lookup"><span data-stu-id="713c3-111">Expand the Fixed asset proposals section.</span></span> 
3. <span data-ttu-id="713c3-112">创建具有要用于法人中的每个过帐层的日记帐名称的记录。</span><span class="sxs-lookup"><span data-stu-id="713c3-112">Create a record with the journal name to be used for each posting layer in the legal entity.</span></span> <span data-ttu-id="713c3-113">如果帐簿不过帐到总帐，则不应选则具有关联日记帐的过帐层。</span><span class="sxs-lookup"><span data-stu-id="713c3-113">If books do not post to the general ledger, then the None posting layer should be selected with the associated journal.</span></span> <span data-ttu-id="713c3-114">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="713c3-114">Click Add.</span></span> 
4. <span data-ttu-id="713c3-115">在“过帐层”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="713c3-115">In the Posting layer field, enter or select a value.</span></span> 
5. <span data-ttu-id="713c3-116">在“日记帐名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="713c3-116">In the Journal name field, enter or select a value.</span></span> 
6. <span data-ttu-id="713c3-117">在每个法人中的固定资产参数页面上重复日记帐设置。</span><span class="sxs-lookup"><span data-stu-id="713c3-117">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span> 

<span data-ttu-id="713c3-118">子任务：计算折旧</span><span class="sxs-lookup"><span data-stu-id="713c3-118">Sub-task: Calculate depreciation</span></span>

1. <span data-ttu-id="713c3-119">使用“创建折旧方案”页开始在法人中运行折旧。</span><span class="sxs-lookup"><span data-stu-id="713c3-119">Use the Create depreciation proposal page to start your depreciation run across legal entities.</span></span> <span data-ttu-id="713c3-120">转到“固定资产”>“日记帐条目”>“创建折旧方案”。</span><span class="sxs-lookup"><span data-stu-id="713c3-120">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span> 
2. <span data-ttu-id="713c3-121">在“过帐层”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="713c3-121">In the Posting layer field, enter or select a value.</span></span> 
3. <span data-ttu-id="713c3-122">日记帐名称默认来自固定资产参数。</span><span class="sxs-lookup"><span data-stu-id="713c3-122">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="713c3-123">当前法人的日记帐名称可以在此处更改。</span><span class="sxs-lookup"><span data-stu-id="713c3-123">It can be changed here for the current legal entity.</span></span> 
4. <span data-ttu-id="713c3-124">在“结束日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="713c3-124">In the To date field, enter a date.</span></span> 
5. <span data-ttu-id="713c3-125">选择要包括在折旧运行中的法人。</span><span class="sxs-lookup"><span data-stu-id="713c3-125">Select the legal entities to be included in the depreciation run.</span></span> <span data-ttu-id="713c3-126">仅具有在固定资产参数页面为固定资产方案设置的日记帐的法人才会在列表中显示。</span><span class="sxs-lookup"><span data-stu-id="713c3-126">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span> 
6. <span data-ttu-id="713c3-127">启用后，“过帐日记帐”选项将在折旧日记帐创建时自动过帐它们。</span><span class="sxs-lookup"><span data-stu-id="713c3-127">When enabled, the Post journals option will automatically post the depreciation journals when they are created.</span></span> <span data-ttu-id="713c3-128">如果未选择，将创建日记帐，但不会过帐，因此，您可以在过帐前查看详细信息。</span><span class="sxs-lookup"><span data-stu-id="713c3-128">When not selected, the journals will be created, but not posted, so you can review the details before posting.</span></span> <span data-ttu-id="713c3-129">在“过帐日记帐”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="713c3-129">Select Yes in the Post journals field.</span></span> 
7. <span data-ttu-id="713c3-130">筛选字段包括为此折旧运行选择的法人的所有固定资产、组和帐簿。</span><span class="sxs-lookup"><span data-stu-id="713c3-130">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span> 
8. <span data-ttu-id="713c3-131">“批处理”选项默认情况下启用。</span><span class="sxs-lookup"><span data-stu-id="713c3-131">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="713c3-132">启用此选项后，折旧日记帐创建和过帐将在后台运行。</span><span class="sxs-lookup"><span data-stu-id="713c3-132">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span> 
9. <span data-ttu-id="713c3-133">单击“创建日记帐”。</span><span class="sxs-lookup"><span data-stu-id="713c3-133">Click Create journal.</span></span> 
10. <span data-ttu-id="713c3-134">您必须查看在各自的法人创建的折旧日记帐。</span><span class="sxs-lookup"><span data-stu-id="713c3-134">You must view the depreciation journals created in the respective legal entities.</span></span> <span data-ttu-id="713c3-135">转到固定资产>流水输入项>固定资产流水。</span><span class="sxs-lookup"><span data-stu-id="713c3-135">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>


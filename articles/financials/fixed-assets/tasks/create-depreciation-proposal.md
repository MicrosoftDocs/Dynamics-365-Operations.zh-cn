--- 
title: "创建折旧方案"
description: "本程序描述了批处理折旧方案的工作原理，并说明了如何为固定资产建议折旧方案。"
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 07d8cf2f1c46b99dfcd1d7c3419fe835f37c5a02
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="f894f-103">创建折旧方案</span><span class="sxs-lookup"><span data-stu-id="f894f-103">Create a depreciation proposal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f894f-104">本程序描述了批处理折旧方案的工作原理，并说明了如何为固定资产建议折旧方案。</span><span class="sxs-lookup"><span data-stu-id="f894f-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="f894f-105">此任务使用 USMF 演示公司和会计角色。</span><span class="sxs-lookup"><span data-stu-id="f894f-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="f894f-106">创建折旧方案</span><span class="sxs-lookup"><span data-stu-id="f894f-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="f894f-107">转到“固定资产”>“日记帐条目”>“创建折旧方案”。</span><span class="sxs-lookup"><span data-stu-id="f894f-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="f894f-108">在“日记帐名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f894f-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f894f-109">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f894f-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f894f-110">在“结束日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="f894f-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="f894f-111">选择“汇总折旧”选项，将按月折旧汇总到一个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="f894f-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="f894f-112">例如，如果“结束日期”值为 2015 年 3 月 31 日，则会生成以下描述：“自 2015 年 1 月 31 日起折旧”。</span><span class="sxs-lookup"><span data-stu-id="f894f-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="f894f-113">建议日记帐行的“日期”字段随后将设置为 2015 年 3 月 31 日。</span><span class="sxs-lookup"><span data-stu-id="f894f-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="f894f-114">使用“筛选”选项，按资产、资产组或其他条件筛选折旧方案。</span><span class="sxs-lookup"><span data-stu-id="f894f-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="f894f-115">如果您为固定资产表格使用“创建购置或折旧方案”，可以批处理折旧方案。</span><span class="sxs-lookup"><span data-stu-id="f894f-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="f894f-116">对于使用较多系统资源的较大方案，建议使用此方案。</span><span class="sxs-lookup"><span data-stu-id="f894f-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="f894f-117">如果选择批处理选项，您仍可以在该期间完成其他任务。</span><span class="sxs-lookup"><span data-stu-id="f894f-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="f894f-118">在您这样建议折旧时，则为固定资产价值模型计算折旧。</span><span class="sxs-lookup"><span data-stu-id="f894f-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="f894f-119">单击“创建日记帐”。</span><span class="sxs-lookup"><span data-stu-id="f894f-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="f894f-120">查看折旧条目</span><span class="sxs-lookup"><span data-stu-id="f894f-120">Review depreciation entries</span></span>
1. <span data-ttu-id="f894f-121">转到固定资产>流水输入项>固定资产流水。</span><span class="sxs-lookup"><span data-stu-id="f894f-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="f894f-122">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f894f-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f894f-123">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="f894f-123">Click Lines.</span></span>
4. <span data-ttu-id="f894f-124">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="f894f-124">Click Post.</span></span>



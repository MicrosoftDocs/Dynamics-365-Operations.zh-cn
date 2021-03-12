---
title: 创建折旧方案
description: 本主题描述折旧批处理建议的工作原理，并说明如何为固定资产建议折旧。
author: abruer
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3d62e982d26afbec7ac04dd80592a73f4a3286f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968895"
---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="f71bc-103">创建折旧方案</span><span class="sxs-lookup"><span data-stu-id="f71bc-103">Create a depreciation proposal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f71bc-104">本主题描述折旧批处理建议的工作原理，并说明如何为固定资产建议折旧。</span><span class="sxs-lookup"><span data-stu-id="f71bc-104">This topic describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="f71bc-105">此任务使用 USMF 演示公司和会计角色。</span><span class="sxs-lookup"><span data-stu-id="f71bc-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-a-depreciation-proposal"></a><span data-ttu-id="f71bc-106">创建折旧方案</span><span class="sxs-lookup"><span data-stu-id="f71bc-106">Create a depreciation proposal</span></span>
1. <span data-ttu-id="f71bc-107">在导航窗格中，转到 **模块 > 固定资产 > 日记帐条目 > 创建折旧方案**。</span><span class="sxs-lookup"><span data-stu-id="f71bc-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Create depreciation proposal**.</span></span>
2. <span data-ttu-id="f71bc-108">在 **日记帐的名称** 字段中，从下拉菜单中选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="f71bc-108">In the **Name of journal** field, select an option from the drop-down menu.</span></span>
3. <span data-ttu-id="f71bc-109">在 **结束日期** 字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="f71bc-109">In the **To date** field, enter a date.</span></span>

    - <span data-ttu-id="f71bc-110">选择 **汇总折旧** 选项，将按月折旧汇总到一个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="f71bc-110">Select the **Summarize depreciation** option to summarize monthly depreciations into one journal line.</span></span>  
    - <span data-ttu-id="f71bc-111">例如，如果“结束日期”值为 2015 年 3 月 31 日，则会生成以下描述：“自 2015 年 1 月 31 日起折旧”。</span><span class="sxs-lookup"><span data-stu-id="f71bc-111">For example, if the To date value is March 31, 2015, the following description is generated: "Depreciation since January 31, 2015."</span></span> <span data-ttu-id="f71bc-112">建议日记帐行的 **日期** 字段随后将设置为 2015 年 3 月 31 日。</span><span class="sxs-lookup"><span data-stu-id="f71bc-112">The **Date** field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    - <span data-ttu-id="f71bc-113">使用 **筛选** 选项，按资产、资产组或其他条件筛选折旧方案。</span><span class="sxs-lookup"><span data-stu-id="f71bc-113">The depreciation proposal can be filtered by asset, asset group, or other criteria using the **Filter** option.</span></span>  
    - <span data-ttu-id="f71bc-114">如果您为固定资产表格使用 **创建购置或折旧方案**，可以批处理折旧方案。</span><span class="sxs-lookup"><span data-stu-id="f71bc-114">When you use the **Create acquisition or depreciation proposals for fixed assets** form, you can propose depreciation in batches.</span></span> <span data-ttu-id="f71bc-115">对于使用较多系统资源的较大方案，建议使用此方案。</span><span class="sxs-lookup"><span data-stu-id="f71bc-115">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="f71bc-116">如果选择批处理选项，您仍可以在该期间完成其他任务。</span><span class="sxs-lookup"><span data-stu-id="f71bc-116">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="f71bc-117">在您这样建议折旧时，则为固定资产价值模型计算折旧。</span><span class="sxs-lookup"><span data-stu-id="f71bc-117">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  

4. <span data-ttu-id="f71bc-118">选择 **创建日记帐**。</span><span class="sxs-lookup"><span data-stu-id="f71bc-118">Select **Create journal**.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="f71bc-119">查看折旧条目</span><span class="sxs-lookup"><span data-stu-id="f71bc-119">Review depreciation entries</span></span>
1. <span data-ttu-id="f71bc-120">在导航窗格中，转到 **模块 > 固定资产 > 日记帐条目 > 固定资产日记帐**。</span><span class="sxs-lookup"><span data-stu-id="f71bc-120">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="f71bc-121">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f71bc-121">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f71bc-122">选择 **行**。</span><span class="sxs-lookup"><span data-stu-id="f71bc-122">Select **Lines**.</span></span>
4. <span data-ttu-id="f71bc-123">选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="f71bc-123">Select **Post**.</span></span>


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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07337063c01f146c72ca6d9e0f9096907cdc9638
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142815"
---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="56bca-103">创建折旧方案</span><span class="sxs-lookup"><span data-stu-id="56bca-103">Create a depreciation proposal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="56bca-104">本主题描述折旧批处理建议的工作原理，并说明如何为固定资产建议折旧。</span><span class="sxs-lookup"><span data-stu-id="56bca-104">This topic describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="56bca-105">此任务使用 USMF 演示公司和会计角色。</span><span class="sxs-lookup"><span data-stu-id="56bca-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-a-depreciation-proposal"></a><span data-ttu-id="56bca-106">创建折旧方案</span><span class="sxs-lookup"><span data-stu-id="56bca-106">Create a depreciation proposal</span></span>
1. <span data-ttu-id="56bca-107">在导航窗格中，转到**模块 > 固定资产 > 日记帐条目 > 创建折旧方案**。</span><span class="sxs-lookup"><span data-stu-id="56bca-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Create depreciation proposal**.</span></span>
2. <span data-ttu-id="56bca-108">在**日记帐的名称**字段中，从下拉菜单中选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="56bca-108">In the **Name of journal** field, select an option from the drop-down menu.</span></span>
3. <span data-ttu-id="56bca-109">在**结束日期**字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="56bca-109">In the **To date** field, enter a date.</span></span>

    - <span data-ttu-id="56bca-110">选择**汇总折旧**选项，将按月折旧汇总到一个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="56bca-110">Select the **Summarize depreciation** option to summarize monthly depreciations into one journal line.</span></span>  
    - <span data-ttu-id="56bca-111">例如，如果“结束日期”值为 2015 年 3 月 31 日，则会生成以下描述：“自 2015 年 1 月 31 日起折旧”。</span><span class="sxs-lookup"><span data-stu-id="56bca-111">For example, if the To date value is March 31, 2015, the following description is generated: "Depreciation since January 31, 2015."</span></span> <span data-ttu-id="56bca-112">建议日记帐行的**日期**字段随后将设置为 2015 年 3 月 31 日。</span><span class="sxs-lookup"><span data-stu-id="56bca-112">The **Date** field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    - <span data-ttu-id="56bca-113">使用**筛选**选项，按资产、资产组或其他条件筛选折旧方案。</span><span class="sxs-lookup"><span data-stu-id="56bca-113">The depreciation proposal can be filtered by asset, asset group, or other criteria using the **Filter** option.</span></span>  
    - <span data-ttu-id="56bca-114">如果您为固定资产表格使用**创建购置或折旧方案**，可以批处理折旧方案。</span><span class="sxs-lookup"><span data-stu-id="56bca-114">When you use the **Create acquisition or depreciation proposals for fixed assets** form, you can propose depreciation in batches.</span></span> <span data-ttu-id="56bca-115">对于使用较多系统资源的较大方案，建议使用此方案。</span><span class="sxs-lookup"><span data-stu-id="56bca-115">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="56bca-116">如果选择批处理选项，您仍可以在该期间完成其他任务。</span><span class="sxs-lookup"><span data-stu-id="56bca-116">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="56bca-117">在您这样建议折旧时，则为固定资产价值模型计算折旧。</span><span class="sxs-lookup"><span data-stu-id="56bca-117">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  

4. <span data-ttu-id="56bca-118">选择**创建日记帐**。</span><span class="sxs-lookup"><span data-stu-id="56bca-118">Select **Create journal**.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="56bca-119">查看折旧条目</span><span class="sxs-lookup"><span data-stu-id="56bca-119">Review depreciation entries</span></span>
1. <span data-ttu-id="56bca-120">在导航窗格中，转到**模块 > 固定资产 > 日记帐条目 > 固定资产日记帐**。</span><span class="sxs-lookup"><span data-stu-id="56bca-120">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="56bca-121">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="56bca-121">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="56bca-122">选择**行**。</span><span class="sxs-lookup"><span data-stu-id="56bca-122">Select **Lines**.</span></span>
4. <span data-ttu-id="56bca-123">选择**过帐**。</span><span class="sxs-lookup"><span data-stu-id="56bca-123">Select **Post**.</span></span>


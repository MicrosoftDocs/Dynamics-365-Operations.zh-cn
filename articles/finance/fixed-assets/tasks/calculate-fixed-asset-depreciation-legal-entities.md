---
title: 计算各个法人的固定资产折旧
description: 固定资产折旧可以一步跨多个法人运行。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 074a1b80584050302920a95c20fb547523a4866c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142907"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="7d89b-103">计算各个法人的固定资产折旧</span><span class="sxs-lookup"><span data-stu-id="7d89b-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7d89b-104">固定资产折旧可以一步跨多个法人运行。</span><span class="sxs-lookup"><span data-stu-id="7d89b-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="7d89b-105">此过程显示如何设置和运行多个法人的过程。</span><span class="sxs-lookup"><span data-stu-id="7d89b-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="7d89b-106">它为 USMF 法人实体使用会计角色和演示数据。</span><span class="sxs-lookup"><span data-stu-id="7d89b-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="7d89b-107">设置跨公司折旧运行日记帐</span><span class="sxs-lookup"><span data-stu-id="7d89b-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="7d89b-108">转到固定资产>设置>固定资产参数。</span><span class="sxs-lookup"><span data-stu-id="7d89b-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="7d89b-109">展开“固定资产方案”部分。</span><span class="sxs-lookup"><span data-stu-id="7d89b-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="7d89b-110">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="7d89b-110">Click Add.</span></span>
4. <span data-ttu-id="7d89b-111">在“过帐层”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7d89b-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="7d89b-112">在“日记帐名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7d89b-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="7d89b-113">在每个法人中的固定资产参数页面上重复日记帐设置。</span><span class="sxs-lookup"><span data-stu-id="7d89b-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="7d89b-114">折旧运行</span><span class="sxs-lookup"><span data-stu-id="7d89b-114">Depreciation run</span></span>
1. <span data-ttu-id="7d89b-115">转到“固定资产”>“日记帐条目”>“创建折旧方案”。</span><span class="sxs-lookup"><span data-stu-id="7d89b-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="7d89b-116">在“过帐层”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7d89b-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="7d89b-117">日记帐名称默认来自固定资产参数。</span><span class="sxs-lookup"><span data-stu-id="7d89b-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="7d89b-118">当前法人的日记帐名称可以在此处更改。</span><span class="sxs-lookup"><span data-stu-id="7d89b-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="7d89b-119">在“结束日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="7d89b-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="7d89b-120">选择要包括在折旧运行中的法人。</span><span class="sxs-lookup"><span data-stu-id="7d89b-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="7d89b-121">仅具有在固定资产参数页面为固定资产方案设置的日记帐的法人才会在列表中显示。</span><span class="sxs-lookup"><span data-stu-id="7d89b-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="7d89b-122">在“过帐日记帐”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="7d89b-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="7d89b-123">筛选字段包括为此折旧运行选择的法人的所有固定资产、组和帐簿。</span><span class="sxs-lookup"><span data-stu-id="7d89b-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="7d89b-124">“批处理”选项默认情况下启用。</span><span class="sxs-lookup"><span data-stu-id="7d89b-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="7d89b-125">启用此选项后，折旧日记帐创建和过帐将在后台运行。</span><span class="sxs-lookup"><span data-stu-id="7d89b-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="7d89b-126">单击“创建日记帐”。</span><span class="sxs-lookup"><span data-stu-id="7d89b-126">Click Create journal.</span></span>
6. <span data-ttu-id="7d89b-127">转到固定资产>流水输入项>固定资产流水。</span><span class="sxs-lookup"><span data-stu-id="7d89b-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>


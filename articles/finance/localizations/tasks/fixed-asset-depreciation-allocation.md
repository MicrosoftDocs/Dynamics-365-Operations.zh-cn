---
title: 设置固定资产折旧费用分配
description: 在日本， 固定资产折旧费用可以被多个部门分摊。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetAllocationRuleSetup_CN,  AssetPosting
audience: Application User
ms.reviewer: kfend
ms.search.region: China (PRC), Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e4207ba1e48ac470d8ebbbf05701453c9c24611
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4984721"
---
# <a name="setup-fixed-asset-depreciation-allocation"></a><span data-ttu-id="544f3-103">设置固定资产折旧费用分配</span><span class="sxs-lookup"><span data-stu-id="544f3-103">Setup fixed asset depreciation allocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="544f3-104">在日本， 固定资产折旧费用可以被多个部门分摊。</span><span class="sxs-lookup"><span data-stu-id="544f3-104">In Japan, the depreciation expenses of a particular fixed asset can be shared among multiple departments.</span></span> 



<span data-ttu-id="544f3-105">这个任务帮你走一遍如何设置固定资产折旧费用分配流程。</span><span class="sxs-lookup"><span data-stu-id="544f3-105">This task walks you through setting up fixed asset depreciation allocation.</span></span> 



<span data-ttu-id="544f3-106">用于创建此任务的演示数据公司是 JPMF。</span><span class="sxs-lookup"><span data-stu-id="544f3-106">This task was created using the demo data company JPMF.</span></span>


## <a name="create-a-fixed-asset-allocation-rule"></a><span data-ttu-id="544f3-107">创建“固定资产分配规则”</span><span class="sxs-lookup"><span data-stu-id="544f3-107">Create a Fixed asset allocation rule</span></span>
1. <span data-ttu-id="544f3-108">选择固定资产>设置>折旧费用分配规则。</span><span class="sxs-lookup"><span data-stu-id="544f3-108">Go to Fixed assets > Setup > Depreciation allocation rules.</span></span>
2. <span data-ttu-id="544f3-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="544f3-109">Click New.</span></span>
3. <span data-ttu-id="544f3-110">在“规则 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="544f3-110">In the Rule ID field, type a value.</span></span>
4. <span data-ttu-id="544f3-111">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="544f3-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="544f3-112">在“维度名称”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="544f3-112">In the Dimension name field, type a value.</span></span>
6. <span data-ttu-id="544f3-113">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="544f3-113">Click Add.</span></span>
7. <span data-ttu-id="544f3-114">在“业务单元”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="544f3-114">In the BusinessUnit field, type a value.</span></span>
    * <span data-ttu-id="544f3-115">输入第一个分配目标的信息。</span><span class="sxs-lookup"><span data-stu-id="544f3-115">Enter the information for the first allocation target.</span></span>  
8. <span data-ttu-id="544f3-116">在“百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="544f3-116">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="544f3-117">所有分配目标的合计总数必须为 100。</span><span class="sxs-lookup"><span data-stu-id="544f3-117">The total of all the allocation target must be 100.</span></span>  
9. <span data-ttu-id="544f3-118">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="544f3-118">In the Offset account field, specify the desired values.</span></span>
10. <span data-ttu-id="544f3-119">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="544f3-119">Click Add.</span></span>
11. <span data-ttu-id="544f3-120">在“业务单元”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="544f3-120">In the BusinessUnit field, type a value.</span></span>
12. <span data-ttu-id="544f3-121">在“百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="544f3-121">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="544f3-122">所有分配目标的合计总数必须为 100。</span><span class="sxs-lookup"><span data-stu-id="544f3-122">The total of all the allocation target must be 100.</span></span>  
13. <span data-ttu-id="544f3-123">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="544f3-123">In the Offset account field, specify the desired values.</span></span>
14. <span data-ttu-id="544f3-124">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="544f3-124">Click Save.</span></span>

## <a name="assign-a-fixed-asset-allocation-rule-to-a-posting-profile"></a><span data-ttu-id="544f3-125">将固定资产分配规则分配给过帐模板。</span><span class="sxs-lookup"><span data-stu-id="544f3-125">Assign a fixed asset allocation rule to a posting profile</span></span>
1. <span data-ttu-id="544f3-126">转到“固定资产”>“设置”>“固定资产过帐模板”。</span><span class="sxs-lookup"><span data-stu-id="544f3-126">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="544f3-127">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="544f3-127">Click Edit.</span></span>
3. <span data-ttu-id="544f3-128">在“交易类型”字段中，选择“折旧”。</span><span class="sxs-lookup"><span data-stu-id="544f3-128">In the Transaction type field, select 'Depreciation'.</span></span>
4. <span data-ttu-id="544f3-129">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="544f3-129">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="544f3-130">选择您想要与分配规则链接的记录。</span><span class="sxs-lookup"><span data-stu-id="544f3-130">Select the record that you want to link the allocation rule to.</span></span>  
5. <span data-ttu-id="544f3-131">展开“折旧费用分配规则”部分。</span><span class="sxs-lookup"><span data-stu-id="544f3-131">Expand the Depreciation allocation rules section.</span></span>
6. <span data-ttu-id="544f3-132">在“资产折旧费用分配”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="544f3-132">In the Asset allocation rule for depreciation field, type a value.</span></span>
7. <span data-ttu-id="544f3-133">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="544f3-133">Click Save.</span></span>


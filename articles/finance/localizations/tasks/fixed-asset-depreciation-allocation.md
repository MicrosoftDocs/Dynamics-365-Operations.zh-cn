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
ms.search.scope: Core, Operations
ms.search.region: China (PRC), Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6df80ed27c45416df9ae66c5471e053969b77a0
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139029"
---
# <a name="setup-fixed-asset-depreciation-allocation"></a><span data-ttu-id="d8f9f-103">设置固定资产折旧费用分配</span><span class="sxs-lookup"><span data-stu-id="d8f9f-103">Setup fixed asset depreciation allocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8f9f-104">在日本， 固定资产折旧费用可以被多个部门分摊。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-104">In Japan, the depreciation expenses of a particular fixed asset can be shared among multiple departments.</span></span> 



<span data-ttu-id="d8f9f-105">这个任务帮你走一遍如何设置固定资产折旧费用分配流程。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-105">This task walks you through setting up fixed asset depreciation allocation.</span></span> 



<span data-ttu-id="d8f9f-106">用于创建此任务的演示数据公司是 JPMF。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-106">This task was created using the demo data company JPMF.</span></span>


## <a name="create-a-fixed-asset-allocation-rule"></a><span data-ttu-id="d8f9f-107">创建“固定资产分配规则”</span><span class="sxs-lookup"><span data-stu-id="d8f9f-107">Create a Fixed asset allocation rule</span></span>
1. <span data-ttu-id="d8f9f-108">选择固定资产>设置>折旧费用分配规则。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-108">Go to Fixed assets > Setup > Depreciation allocation rules.</span></span>
2. <span data-ttu-id="d8f9f-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-109">Click New.</span></span>
3. <span data-ttu-id="d8f9f-110">在“规则 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-110">In the Rule ID field, type a value.</span></span>
4. <span data-ttu-id="d8f9f-111">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d8f9f-112">在“维度名称”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-112">In the Dimension name field, type a value.</span></span>
6. <span data-ttu-id="d8f9f-113">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-113">Click Add.</span></span>
7. <span data-ttu-id="d8f9f-114">在“业务单元”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-114">In the BusinessUnit field, type a value.</span></span>
    * <span data-ttu-id="d8f9f-115">输入第一个分配目标的信息。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-115">Enter the information for the first allocation target.</span></span>  
8. <span data-ttu-id="d8f9f-116">在“百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-116">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="d8f9f-117">所有分配目标的合计总数必须为 100。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-117">The total of all the allocation target must be 100.</span></span>  
9. <span data-ttu-id="d8f9f-118">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-118">In the Offset account field, specify the desired values.</span></span>
10. <span data-ttu-id="d8f9f-119">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-119">Click Add.</span></span>
11. <span data-ttu-id="d8f9f-120">在“业务单元”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-120">In the BusinessUnit field, type a value.</span></span>
12. <span data-ttu-id="d8f9f-121">在“百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-121">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="d8f9f-122">所有分配目标的合计总数必须为 100。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-122">The total of all the allocation target must be 100.</span></span>  
13. <span data-ttu-id="d8f9f-123">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-123">In the Offset account field, specify the desired values.</span></span>
14. <span data-ttu-id="d8f9f-124">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-124">Click Save.</span></span>

## <a name="assign-a-fixed-asset-allocation-rule-to-a-posting-profile"></a><span data-ttu-id="d8f9f-125">将固定资产分配规则分配给过帐模板。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-125">Assign a fixed asset allocation rule to a posting profile</span></span>
1. <span data-ttu-id="d8f9f-126">转到“固定资产”>“设置”>“固定资产过帐模板”。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-126">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="d8f9f-127">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-127">Click Edit.</span></span>
3. <span data-ttu-id="d8f9f-128">在“交易类型”字段中，选择“折旧”。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-128">In the Transaction type field, select 'Depreciation'.</span></span>
4. <span data-ttu-id="d8f9f-129">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-129">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d8f9f-130">选择您想要与分配规则链接的记录。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-130">Select the record that you want to link the allocation rule to.</span></span>  
5. <span data-ttu-id="d8f9f-131">展开“折旧费用分配规则”部分。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-131">Expand the Depreciation allocation rules section.</span></span>
6. <span data-ttu-id="d8f9f-132">在“资产折旧费用分配”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-132">In the Asset allocation rule for depreciation field, type a value.</span></span>
7. <span data-ttu-id="d8f9f-133">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d8f9f-133">Click Save.</span></span>


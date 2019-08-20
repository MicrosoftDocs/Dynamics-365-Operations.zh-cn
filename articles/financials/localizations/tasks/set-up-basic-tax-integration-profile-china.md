---
title: 设置中国的基本税务集成模板
description: 此过程显示如何设置税务集成模板，更新有关颁发增值税发票的客户设置，以及为中国设置增值税发票说明。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxProfileTable_CN, HcmWorkerLookUp, UnitOfMeasureLookup, CustTable, LogisticsPostalAddress, TaxGroupLookup, VATInvoiceDescTable_CN
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: China (PRC)
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aba6a772cd390eb4eca63d4c6a1c7bd9c1d09580
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848757"
---
# <a name="set-up-basic-tax-integration-profile-for-china"></a><span data-ttu-id="c59ce-103">设置中国的基本税务集成模板</span><span class="sxs-lookup"><span data-stu-id="c59ce-103">Set up basic tax integration profile for China</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c59ce-104">此过程显示如何设置税务集成模板，更新有关颁发增值税发票的客户设置，以及为中国设置增值税发票说明。</span><span class="sxs-lookup"><span data-stu-id="c59ce-104">This procedure shows how to set up a tax integration profile, update customer settings for issuing VAT invoices, and set up VAT invoice descriptions for China.</span></span>

<span data-ttu-id="c59ce-105">必须先完成“金税集成导入设置”过程和“维护金税导出格式”过程，才能完成此过程。</span><span class="sxs-lookup"><span data-stu-id="c59ce-105">Before you can complete this procedure, you must complete the Golden tax integration import setup procedure and the Maintain golden tax export format procedure.</span></span>

<span data-ttu-id="c59ce-106">本流程是用演示公司 CNMF 数据生成的。</span><span class="sxs-lookup"><span data-stu-id="c59ce-106">This procedure was created using the demo data company CNMF.</span></span> <span data-ttu-id="c59ce-107">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="c59ce-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="c59ce-108">转到“税金”>“设置”>“税务集成”>“税务集成模板”。</span><span class="sxs-lookup"><span data-stu-id="c59ce-108">Go to Tax > Setup > Tax integration > Tax integration profiles.</span></span>
2. <span data-ttu-id="c59ce-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="c59ce-109">Click New.</span></span>
3. <span data-ttu-id="c59ce-110">在“模板 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c59ce-110">In the Profile ID field, type a value.</span></span>
4. <span data-ttu-id="c59ce-111">在“模板名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c59ce-111">In the Profile name field, type a value.</span></span>
5. <span data-ttu-id="c59ce-112">在“销售税代码”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c59ce-112">In the Sales tax code field, enter or select a value.</span></span>
6. <span data-ttu-id="c59ce-113">在“验证金额限制”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="c59ce-113">Select Yes in the Validate amount limit field.</span></span>
7. <span data-ttu-id="c59ce-114">在“最大发票金额”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="c59ce-114">In the Maximum invoice amount field, enter a number.</span></span>
8. <span data-ttu-id="c59ce-115">在“含税”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="c59ce-115">Select Yes in the Include tax field.</span></span>
9. <span data-ttu-id="c59ce-116">在“默认商品”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c59ce-116">In the Default commodity field, type a value.</span></span>
10. <span data-ttu-id="c59ce-117">在“复核”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c59ce-117">In the Invoice auditor field, enter or select a value.</span></span>
11. <span data-ttu-id="c59ce-118">在“收款”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c59ce-118">In the Payment collector field, enter or select a value.</span></span>
12. <span data-ttu-id="c59ce-119">在“格式映射”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c59ce-119">In the Format mapping field, enter or select a value.</span></span>
13. <span data-ttu-id="c59ce-120">在“普通增值税发票”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="c59ce-120">Select Yes in the Non-deductible VAT invoices field.</span></span>
14. <span data-ttu-id="c59ce-121">展开“描述和单位的缺省值”部分。</span><span class="sxs-lookup"><span data-stu-id="c59ce-121">Expand the Default value of description and unit section.</span></span>
15. <span data-ttu-id="c59ce-122">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="c59ce-122">Click New.</span></span>
16. <span data-ttu-id="c59ce-123">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="c59ce-123">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="c59ce-124">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c59ce-124">In the Description field, type a value.</span></span>
18. <span data-ttu-id="c59ce-125">在“单位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c59ce-125">In the Unit field, enter or select a value.</span></span>
19. <span data-ttu-id="c59ce-126">转到“应付账款”>“客户”>“所有客户”。</span><span class="sxs-lookup"><span data-stu-id="c59ce-126">Go to Accounts receivable > Customers > All customers.</span></span>
20. <span data-ttu-id="c59ce-127">选择一个客户。</span><span class="sxs-lookup"><span data-stu-id="c59ce-127">Select a customer.</span></span>
21. <span data-ttu-id="c59ce-128">单击“登记 ID”。</span><span class="sxs-lookup"><span data-stu-id="c59ce-128">Click Registration IDs.</span></span>
22. <span data-ttu-id="c59ce-129">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="c59ce-129">Click Add.</span></span>
23. <span data-ttu-id="c59ce-130">在“登记类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c59ce-130">In the Registration type field, enter or select a value.</span></span>
24. <span data-ttu-id="c59ce-131">改变登记类型。</span><span class="sxs-lookup"><span data-stu-id="c59ce-131">ResolveChanges the Registration type.</span></span>
25. <span data-ttu-id="c59ce-132">在“登记编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c59ce-132">In the Registration number field, type a value.</span></span>
26. <span data-ttu-id="c59ce-133">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="c59ce-133">Click Save.</span></span>
27. <span data-ttu-id="c59ce-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c59ce-134">Close the page.</span></span>
28. <span data-ttu-id="c59ce-135">展开“发票和交货”部分。</span><span class="sxs-lookup"><span data-stu-id="c59ce-135">Expand the Invoice and delivery section.</span></span>
29. <span data-ttu-id="c59ce-136">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="c59ce-136">Click Edit.</span></span>
30. <span data-ttu-id="c59ce-137">在“销售税组”字段，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c59ce-137">In the Sales tax group field, enter or select a value.</span></span>
31. <span data-ttu-id="c59ce-138">转到“税金”“设置”>“税务集成”>“增值税发票描述”。</span><span class="sxs-lookup"><span data-stu-id="c59ce-138">Go to Tax > Setup > Tax integration > VAT invoice description.</span></span>
32. <span data-ttu-id="c59ce-139">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="c59ce-139">Click New.</span></span>
33. <span data-ttu-id="c59ce-140">在“增值税发票描述 ID”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="c59ce-140">In the VAT invoice description ID field, type a value.</span></span>
34. <span data-ttu-id="c59ce-141">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="c59ce-141">In the Description field, type a value.</span></span>
35. <span data-ttu-id="c59ce-142">在“单位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c59ce-142">In the Unit field, enter or select a value.</span></span>
36. <span data-ttu-id="c59ce-143">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="c59ce-143">Click Save.</span></span>


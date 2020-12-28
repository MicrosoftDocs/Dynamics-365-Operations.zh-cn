---
title: 成批创建销售报价单
description: 该过程演示如何有效创建发送一组产品或服务给多个客户的报价单。
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm, SalesQuickQuote
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 227ff0dd03f8917f4551ce08067ef26c6204b059
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422798"
---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="a8b07-103">成批创建销售报价单</span><span class="sxs-lookup"><span data-stu-id="a8b07-103">Mass create sales quotations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a8b07-104">该过程演示如何有效创建发送一组产品或服务给多个客户的报价单。</span><span class="sxs-lookup"><span data-stu-id="a8b07-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="a8b07-105">此成批报价单创建基于报价单模板。</span><span class="sxs-lookup"><span data-stu-id="a8b07-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="a8b07-106">您可以使用演示数据公司 USMF 或您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="a8b07-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="a8b07-107">创建报价单模板</span><span class="sxs-lookup"><span data-stu-id="a8b07-107">Create a quotation template</span></span>
1. <span data-ttu-id="a8b07-108">转到“销售和市场”>“设置”>“报价单”>“模板组”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="a8b07-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-109">Click New.</span></span>
3. <span data-ttu-id="a8b07-110">在“组 ID”字段中，键入您所选择的 ID。</span><span class="sxs-lookup"><span data-stu-id="a8b07-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="a8b07-111">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a8b07-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a8b07-112">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-112">Click Save.</span></span>
6. <span data-ttu-id="a8b07-113">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a8b07-113">Close the page.</span></span>
7. <span data-ttu-id="a8b07-114">转到“销售和市场营销”>“销售报价单”>“所有报价单”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="a8b07-115">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-115">Click New.</span></span>
9. <span data-ttu-id="a8b07-116">在“帐户类型”字段中选择“客户”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="a8b07-117">在“客户帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a8b07-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="a8b07-118">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-118">Click OK.</span></span>
    * <span data-ttu-id="a8b07-119">对于用作模板的报价单，您必须在报价单标题执行设置步骤。</span><span class="sxs-lookup"><span data-stu-id="a8b07-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="a8b07-120">这必须在您添加行到报价单前完成。</span><span class="sxs-lookup"><span data-stu-id="a8b07-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="a8b07-121">在“操作窗格”上，单击“选项”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="a8b07-122">单击“更改”视图。</span><span class="sxs-lookup"><span data-stu-id="a8b07-122">Click Change view.</span></span>
14. <span data-ttu-id="a8b07-123">单击“标题”视图。</span><span class="sxs-lookup"><span data-stu-id="a8b07-123">Click Header view.</span></span>
15. <span data-ttu-id="a8b07-124">展开“设置”部分。</span><span class="sxs-lookup"><span data-stu-id="a8b07-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="a8b07-125">在“组 ID”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a8b07-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="a8b07-126">在“模板名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a8b07-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="a8b07-127">在“有效”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="a8b07-128">在您应用模板到新销售报价单时，仅可使用有效的模板。</span><span class="sxs-lookup"><span data-stu-id="a8b07-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="a8b07-129">在“操作窗格”上，单击“选项”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="a8b07-130">单击“更改”视图。</span><span class="sxs-lookup"><span data-stu-id="a8b07-130">Click Change view.</span></span>
21. <span data-ttu-id="a8b07-131">单击“查看行”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-131">Click Line view.</span></span>
22. <span data-ttu-id="a8b07-132">在“物料”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a8b07-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="a8b07-133">在“物料”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a8b07-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="a8b07-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a8b07-134">Close the page.</span></span>
25. <span data-ttu-id="a8b07-135">在“折扣百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a8b07-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="a8b07-136">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-136">Click Add line.</span></span>
27. <span data-ttu-id="a8b07-137">在“物料”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a8b07-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="a8b07-138">在“物料”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a8b07-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="a8b07-139">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a8b07-139">Close the page.</span></span>
30. <span data-ttu-id="a8b07-140">在“单位价格”字段中，输入新价格或更改当前价格。</span><span class="sxs-lookup"><span data-stu-id="a8b07-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="a8b07-141">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-141">Click Add line.</span></span>
32. <span data-ttu-id="a8b07-142">在“物料”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a8b07-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="a8b07-143">在“物料”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a8b07-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="a8b07-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a8b07-144">Close the page.</span></span>
35. <span data-ttu-id="a8b07-145">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a8b07-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="a8b07-146">在“折扣”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a8b07-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="a8b07-147">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="a8b07-148">使用该模板创建单个报价单</span><span class="sxs-lookup"><span data-stu-id="a8b07-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="a8b07-149">转到“销售和市场营销”>“销售报价单”>“所有报价单”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="a8b07-150">请注意，您刚刚创建的报价单标记为了模板。</span><span class="sxs-lookup"><span data-stu-id="a8b07-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="a8b07-151">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-151">Click New.</span></span>
3. <span data-ttu-id="a8b07-152">在“帐户类型”字段中选择“客户”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="a8b07-153">在“客户帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a8b07-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="a8b07-154">展开“模板”部分。</span><span class="sxs-lookup"><span data-stu-id="a8b07-154">Expand the Template section.</span></span>
6. <span data-ttu-id="a8b07-155">在“组 ID”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a8b07-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="a8b07-156">在“模板名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a8b07-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="a8b07-157">在“计算方法”字段中，选择“基于模板的值”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="a8b07-158">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-158">Click OK.</span></span>
    * <span data-ttu-id="a8b07-159">新报价单已根据模板的数据和条款创建。</span><span class="sxs-lookup"><span data-stu-id="a8b07-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="a8b07-160">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a8b07-160">Close the page.</span></span>
11. <span data-ttu-id="a8b07-161">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a8b07-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="a8b07-162">使用该模板批量创建报价单</span><span class="sxs-lookup"><span data-stu-id="a8b07-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="a8b07-163">转到“销售和市场”>“销售报价单”>“报价单更新”>“批量创建报价单”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="a8b07-164">在“帐户类型”字段中选择“客户”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="a8b07-165">在“组 ID”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a8b07-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="a8b07-166">在“模板名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a8b07-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="a8b07-167">在“计算方法”字段中，选择“基于模板的值”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="a8b07-168">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="a8b07-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="a8b07-169">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-169">Click Filter.</span></span>
8. <span data-ttu-id="a8b07-170">在“条件”字段中，设置筛选器，使其涵盖您想加入到批量报价单创建中的各种客户。</span><span class="sxs-lookup"><span data-stu-id="a8b07-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="a8b07-171">使用以下格式“客户 1……客户 N”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="a8b07-172">例如，您可以设置筛选器为：US-001..US-004</span><span class="sxs-lookup"><span data-stu-id="a8b07-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="a8b07-173">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-173">Click OK.</span></span>
10. <span data-ttu-id="a8b07-174">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-174">Click OK.</span></span>
11. <span data-ttu-id="a8b07-175">转到“销售和市场营销”>“销售报价单”>“所有报价单”。</span><span class="sxs-lookup"><span data-stu-id="a8b07-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="a8b07-176">核实已根据所选的模板，为成批更新程序中指定的所有客户创建报价单。</span><span class="sxs-lookup"><span data-stu-id="a8b07-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  


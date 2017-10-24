--- 
title: "针对电子申报 (ER) 修改模型和映射以通过更新应用程序生成单据"
description: "若要完成此过程中的步骤，首先必须完成“ER 使用应用程序数据更新生成单据（第 2 部分 - 生成单据）”这一过程。"
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a29e273e5ef377826c0002a9a0a956defef6aa77
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="modify-model-and-mapping-to-generate-documents-with-application-data-update-for-electronic-reporting-er"></a><span data-ttu-id="add8c-103">针对电子申报 (ER) 修改模型和映射以通过更新应用程序生成单据</span><span class="sxs-lookup"><span data-stu-id="add8c-103">Modify model and mapping to generate documents with application data update for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="add8c-104">若要完成此过程中的步骤，首先必须完成“ER 使用应用程序数据更新生成单据（第 2 部分：生成单据）”这一过程。</span><span class="sxs-lookup"><span data-stu-id="add8c-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 2: Generate documents)”.</span></span> 

<span data-ttu-id="add8c-105">此过程中的步骤介绍如何设计电子申报 (ER) 配置以生成电子单据和更新应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="add8c-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="add8c-106">在此过程中，您将修改 ER 配置以开始将其用于生成电子单据和更新应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="add8c-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="add8c-107">此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。</span><span class="sxs-lookup"><span data-stu-id="add8c-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="add8c-108">可使用 DEMF 数据集完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="add8c-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="add8c-109">修改数据模型</span><span class="sxs-lookup"><span data-stu-id="add8c-109">Modify data model</span></span>
1. <span data-ttu-id="add8c-110">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="add8c-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="add8c-111">在树中，选择“内部统计(模型)”。</span><span class="sxs-lookup"><span data-stu-id="add8c-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="add8c-112">您将扩展数据模型的使用方式。</span><span class="sxs-lookup"><span data-stu-id="add8c-112">You will extend how you use the data model.</span></span> <span data-ttu-id="add8c-113">除了将其用作源以生成内部统计报表，数据模型还将用于收集有关内部统计报告流程的详细信息。</span><span class="sxs-lookup"><span data-stu-id="add8c-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="add8c-114">然后将把此详细信息用于更新应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="add8c-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="add8c-115">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="add8c-115">Click Designer.</span></span>
4. <span data-ttu-id="add8c-116">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="add8c-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="add8c-117">在“作为以下项的新节点”字段中，输入“模型根”。</span><span class="sxs-lookup"><span data-stu-id="add8c-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="add8c-118">在“名称”字段中，键入“用于应用程序数据更新”。</span><span class="sxs-lookup"><span data-stu-id="add8c-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="add8c-119">对于应用程序数据更新</span><span class="sxs-lookup"><span data-stu-id="add8c-119">For application data update</span></span>  
7. <span data-ttu-id="add8c-120">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="add8c-120">Click Add.</span></span>
8. <span data-ttu-id="add8c-121">在树中，选择“用于应用程序数据更新”。</span><span class="sxs-lookup"><span data-stu-id="add8c-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="add8c-122">将添加这个新根项以指定将来自内部统计报表（用作数据源）的数据移到应用程序表（更新目标）的数据流。</span><span class="sxs-lookup"><span data-stu-id="add8c-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="add8c-123">必须为获取过帐到传出单据的数据和为从用于更新应用程序数据的单据获取数据使用不同的根项。</span><span class="sxs-lookup"><span data-stu-id="add8c-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="add8c-124">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="add8c-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="add8c-125">在“名称”字段中，键入“存档标题”。</span><span class="sxs-lookup"><span data-stu-id="add8c-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="add8c-126">存档标题</span><span class="sxs-lookup"><span data-stu-id="add8c-126">Archive header</span></span>  
11. <span data-ttu-id="add8c-127">在“物料类型”字段中，选择“记录列表”。</span><span class="sxs-lookup"><span data-stu-id="add8c-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="add8c-128">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="add8c-128">Click Add.</span></span>
    * <span data-ttu-id="add8c-129">因为您将为生成的每个内部统计报表创建一个记录，所以必须为其创建一个新项。</span><span class="sxs-lookup"><span data-stu-id="add8c-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="add8c-130">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="add8c-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="add8c-131">在“名称”字段中，键入“文件名”。</span><span class="sxs-lookup"><span data-stu-id="add8c-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="add8c-132">文件名</span><span class="sxs-lookup"><span data-stu-id="add8c-132">File name</span></span>  
15. <span data-ttu-id="add8c-133">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="add8c-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="add8c-134">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="add8c-134">Click Add.</span></span>
17. <span data-ttu-id="add8c-135">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="add8c-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="add8c-136">在“名称”字段中，键入“行数”。</span><span class="sxs-lookup"><span data-stu-id="add8c-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="add8c-137">行数</span><span class="sxs-lookup"><span data-stu-id="add8c-137">Number of lines</span></span>  
19. <span data-ttu-id="add8c-138">在“物料类型”字段中，选择“整数”。</span><span class="sxs-lookup"><span data-stu-id="add8c-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="add8c-139">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="add8c-139">Click Add.</span></span>
    * <span data-ttu-id="add8c-140">添加此项以表示当前报告流程期间报告的内部统计交易记录数量。</span><span class="sxs-lookup"><span data-stu-id="add8c-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="add8c-141">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="add8c-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="add8c-142">在“名称”字段中，键入“存档行”。</span><span class="sxs-lookup"><span data-stu-id="add8c-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="add8c-143">存档行</span><span class="sxs-lookup"><span data-stu-id="add8c-143">Archive lines</span></span>  
23. <span data-ttu-id="add8c-144">在“物料类型”字段中，选择“记录列表”。</span><span class="sxs-lookup"><span data-stu-id="add8c-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="add8c-145">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="add8c-145">Click Add.</span></span>
    * <span data-ttu-id="add8c-146">添加此项以表示当前报告流程期间报告的内部统计交易记录列表。</span><span class="sxs-lookup"><span data-stu-id="add8c-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="add8c-147">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="add8c-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="add8c-148">在“名称”字段中，键入“金额”。</span><span class="sxs-lookup"><span data-stu-id="add8c-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="add8c-149">本币金额</span><span class="sxs-lookup"><span data-stu-id="add8c-149">Amount</span></span>  
27. <span data-ttu-id="add8c-150">在“物料类型”字段中，选择“实时”。</span><span class="sxs-lookup"><span data-stu-id="add8c-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="add8c-151">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="add8c-151">Click Add.</span></span>
29. <span data-ttu-id="add8c-152">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="add8c-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="add8c-153">在“名称”字段中，键入“商品记录标识”。</span><span class="sxs-lookup"><span data-stu-id="add8c-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="add8c-154">商品记录标识</span><span class="sxs-lookup"><span data-stu-id="add8c-154">Commodity rec id</span></span>  
31. <span data-ttu-id="add8c-155">在“物料类型”字段中，选择“Int64”。</span><span class="sxs-lookup"><span data-stu-id="add8c-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="add8c-156">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="add8c-156">Click Add.</span></span>
33. <span data-ttu-id="add8c-157">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="add8c-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="add8c-158">在“名称”字段中，键入“物料编号”。</span><span class="sxs-lookup"><span data-stu-id="add8c-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="add8c-159">物料编号</span><span class="sxs-lookup"><span data-stu-id="add8c-159">Item number</span></span>  
35. <span data-ttu-id="add8c-160">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="add8c-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="add8c-161">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="add8c-161">Click Add.</span></span>
37. <span data-ttu-id="add8c-162">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="add8c-162">Click Save.</span></span>
38. <span data-ttu-id="add8c-163">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="add8c-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="add8c-164">修改模型映射</span><span class="sxs-lookup"><span data-stu-id="add8c-164">Modify model mapping</span></span>
1. <span data-ttu-id="add8c-165">在树中，展开“内部统计(模型)”。</span><span class="sxs-lookup"><span data-stu-id="add8c-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="add8c-166">在树中，选择“内部统计(模型)\内部统计(映射)”。</span><span class="sxs-lookup"><span data-stu-id="add8c-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="add8c-167">修改现有模型映射，以便开始讲起用于应用程序数据更新和存档内部统计报告详细信息。</span><span class="sxs-lookup"><span data-stu-id="add8c-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="add8c-168">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="add8c-168">Click Designer.</span></span>
4. <span data-ttu-id="add8c-169">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="add8c-169">Click New.</span></span>
5. <span data-ttu-id="add8c-170">在“名称”字段中，键入“更新存档”。</span><span class="sxs-lookup"><span data-stu-id="add8c-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="add8c-171">更新存档</span><span class="sxs-lookup"><span data-stu-id="add8c-171">Update archive</span></span>  
6. <span data-ttu-id="add8c-172">在“方向”字段中，选择“截止目标”。</span><span class="sxs-lookup"><span data-stu-id="add8c-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="add8c-173">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="add8c-173">Click Save.</span></span>
    * <span data-ttu-id="add8c-174">这个新映射指定将来自数据模型的数据（内部统计报告详细信息）移到应用程序表（更新目标）的数据流。</span><span class="sxs-lookup"><span data-stu-id="add8c-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="add8c-175">请注意，必须使用不同模型的根项来为报告流程从应用程序获取数据，然后将来自数据模型的数据用于应用程序数据更新。</span><span class="sxs-lookup"><span data-stu-id="add8c-175">Note that different model’s root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="add8c-176">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="add8c-176">Click Designer.</span></span>
9. <span data-ttu-id="add8c-177">在树结构中，选择“数据模型\数据模型”。</span><span class="sxs-lookup"><span data-stu-id="add8c-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="add8c-178">添加所需数据源。</span><span class="sxs-lookup"><span data-stu-id="add8c-178">Add the required data source.</span></span> <span data-ttu-id="add8c-179">这是其中包含必须存档的所报告内部统计交易记录详细信息的数据模型。</span><span class="sxs-lookup"><span data-stu-id="add8c-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="add8c-180">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="add8c-180">Click Add root.</span></span>
11. <span data-ttu-id="add8c-181">在“名称”字段中，键入“模型”。</span><span class="sxs-lookup"><span data-stu-id="add8c-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="add8c-182">模型</span><span class="sxs-lookup"><span data-stu-id="add8c-182">model</span></span>  
12. <span data-ttu-id="add8c-183">在“定义”字段中，输入或选择值“用于应用程序数据更新”。</span><span class="sxs-lookup"><span data-stu-id="add8c-183">In the Definition field, enter or select the value ‘For application data update’.</span></span>
    * <span data-ttu-id="add8c-184">对于应用程序数据更新</span><span class="sxs-lookup"><span data-stu-id="add8c-184">For application data update</span></span>  
13. <span data-ttu-id="add8c-185">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="add8c-185">Click OK.</span></span>
14. <span data-ttu-id="add8c-186">在树结构中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="add8c-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="add8c-187">在树结构中，选择“功能\计算字段”。</span><span class="sxs-lookup"><span data-stu-id="add8c-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="add8c-188">在树中，选择“模型\存档标题”。</span><span class="sxs-lookup"><span data-stu-id="add8c-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="add8c-189">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="add8c-189">Click Add.</span></span>
    * <span data-ttu-id="add8c-190">因为需要为存档枚举所报告内部统计交易记录，所以必须添加相应的数据源。</span><span class="sxs-lookup"><span data-stu-id="add8c-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="add8c-191">在“名称”字段中，键入“枚举行”。</span><span class="sxs-lookup"><span data-stu-id="add8c-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="add8c-192">枚举行</span><span class="sxs-lookup"><span data-stu-id="add8c-192">Enumerated lines</span></span>  
19. <span data-ttu-id="add8c-193">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="add8c-193">Click Edit formula.</span></span>
20. <span data-ttu-id="add8c-194">在树中，选择“列表\ENUMERATE”。</span><span class="sxs-lookup"><span data-stu-id="add8c-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="add8c-195">单击“添加”功能。</span><span class="sxs-lookup"><span data-stu-id="add8c-195">Click Add function.</span></span>
22. <span data-ttu-id="add8c-196">在树结构中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="add8c-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="add8c-197">在树中，展开“模型\存档标题”。</span><span class="sxs-lookup"><span data-stu-id="add8c-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="add8c-198">在树中，选择“模型\存档标题\存档行”。</span><span class="sxs-lookup"><span data-stu-id="add8c-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="add8c-199">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="add8c-199">Click Add data source.</span></span>
26. <span data-ttu-id="add8c-200">在“公式”字段中，输入“ENUMERATE(model.'Archive header'.'Archive lines')”。</span><span class="sxs-lookup"><span data-stu-id="add8c-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="add8c-201">ENUMERATE(model.'Archive header'.'Archive lines')</span><span class="sxs-lookup"><span data-stu-id="add8c-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="add8c-202">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="add8c-202">Click Save.</span></span>
28. <span data-ttu-id="add8c-203">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="add8c-203">Close the page.</span></span>
29. <span data-ttu-id="add8c-204">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="add8c-204">Click OK.</span></span>
30. <span data-ttu-id="add8c-205">单击”添加目标“。</span><span class="sxs-lookup"><span data-stu-id="add8c-205">Click Add destination.</span></span>
    * <span data-ttu-id="add8c-206">将应用程序表添加为需要更新以存档所报告内部统计交易记录详细信息的必需目标。</span><span class="sxs-lookup"><span data-stu-id="add8c-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="add8c-207">在“名称”字段中，键入“存档”。</span><span class="sxs-lookup"><span data-stu-id="add8c-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="add8c-208">存档</span><span class="sxs-lookup"><span data-stu-id="add8c-208">Archive</span></span>  
32. <span data-ttu-id="add8c-209">在“表名”字段中，键入“IntrastatArchiveGeneral”。</span><span class="sxs-lookup"><span data-stu-id="add8c-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="add8c-210">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="add8c-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="add8c-211">保留记录操作“插入”，以便在存档各内部统计报告流程详细信息期间添加记录。</span><span class="sxs-lookup"><span data-stu-id="add8c-211">Keep the record action ‘Insert’ so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="add8c-212">在“记录信息日志”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="add8c-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="add8c-213">选择“是”以获取有关应用程序数据更新问题的信息。</span><span class="sxs-lookup"><span data-stu-id="add8c-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="add8c-214">在“跳过记录操作验证”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="add8c-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="add8c-215">选择“是”以禁止有关空“内部统计存档标识”字段的验证错误。</span><span class="sxs-lookup"><span data-stu-id="add8c-215">Select Yes to suppress validation errors about the empty ‘Intrastat archive ID’ field.</span></span> <span data-ttu-id="add8c-216">这将在添加记录后，基于“外贸参数”窗体中为此表配置的序号完成。</span><span class="sxs-lookup"><span data-stu-id="add8c-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="add8c-217">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="add8c-217">Click OK.</span></span>
    * <span data-ttu-id="add8c-218">绑定所添加数据源（基于所选根项过滤后的模型）的元素和来自所添加目标的元素。</span><span class="sxs-lookup"><span data-stu-id="add8c-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="add8c-219">在树中，展开“存档”。</span><span class="sxs-lookup"><span data-stu-id="add8c-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="add8c-220">在树中，展开“存档\<关系”。</span><span class="sxs-lookup"><span data-stu-id="add8c-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="add8c-221">在树结构中，展开“存档\<关系\IntrastatArchiveDetail”。</span><span class="sxs-lookup"><span data-stu-id="add8c-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="add8c-222">在树中，选择“存档\<关系\IntrastatArchiveDetail\Amount(AmountMST)”。</span><span class="sxs-lookup"><span data-stu-id="add8c-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="add8c-223">在树中，展开“模型\存档标题\枚举行”。</span><span class="sxs-lookup"><span data-stu-id="add8c-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="add8c-224">在树中，展开“模型\存档标题\枚举行\值”。</span><span class="sxs-lookup"><span data-stu-id="add8c-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="add8c-225">在树中，选择“模型\存档标题\枚举行\值\金额”。</span><span class="sxs-lookup"><span data-stu-id="add8c-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="add8c-226">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="add8c-226">Click Bind.</span></span>
44. <span data-ttu-id="add8c-227">在树中，选择“存档\<关系\IntrastatArchiveDetail\Commodity(IntrastatCommodity)”。</span><span class="sxs-lookup"><span data-stu-id="add8c-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="add8c-228">在树中，选择“模型\存档标题\枚举行\值\商品记录标识”。</span><span class="sxs-lookup"><span data-stu-id="add8c-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="add8c-229">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="add8c-229">Click Bind.</span></span>
47. <span data-ttu-id="add8c-230">在树中，选择“存档\<关系\IntrastatArchiveDetail\物料编号(ItemId)”。</span><span class="sxs-lookup"><span data-stu-id="add8c-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="add8c-231">在树中，选择“模型\存档标题\枚举行\值\物料编号”。</span><span class="sxs-lookup"><span data-stu-id="add8c-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="add8c-232">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="add8c-232">Click Bind.</span></span>
50. <span data-ttu-id="add8c-233">在树中，选择“存档\<关系\IntrastatArchiveDetail\行号(LineNumber)”。</span><span class="sxs-lookup"><span data-stu-id="add8c-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="add8c-234">在树中，选择“模型\存档标题\枚举行\编号”。</span><span class="sxs-lookup"><span data-stu-id="add8c-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="add8c-235">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="add8c-235">Click Bind.</span></span>
53. <span data-ttu-id="add8c-236">在树中，选择“存档\<关系\IntrastatArchiveDetail”。</span><span class="sxs-lookup"><span data-stu-id="add8c-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="add8c-237">在树中，选择“模型\存档标题\枚举行”。</span><span class="sxs-lookup"><span data-stu-id="add8c-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="add8c-238">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="add8c-238">Click Bind.</span></span>
56. <span data-ttu-id="add8c-239">在树中，选择“存档\文件名(FileName)”。</span><span class="sxs-lookup"><span data-stu-id="add8c-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="add8c-240">在树中，选择“模型\存档标题\文件名”。</span><span class="sxs-lookup"><span data-stu-id="add8c-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="add8c-241">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="add8c-241">Click Bind.</span></span>
59. <span data-ttu-id="add8c-242">在树中，选择“存档\行数(NumberOfLines)“。</span><span class="sxs-lookup"><span data-stu-id="add8c-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="add8c-243">在树中，选择“模型\存档标题\行数”。</span><span class="sxs-lookup"><span data-stu-id="add8c-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="add8c-244">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="add8c-244">Click Bind.</span></span>
62. <span data-ttu-id="add8c-245">在树中，选择“存档”。</span><span class="sxs-lookup"><span data-stu-id="add8c-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="add8c-246">在树中，选择“模型\存档标题”。</span><span class="sxs-lookup"><span data-stu-id="add8c-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="add8c-247">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="add8c-247">Click Bind.</span></span>
65. <span data-ttu-id="add8c-248">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="add8c-248">Click Save.</span></span>
66. <span data-ttu-id="add8c-249">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="add8c-249">Close the page.</span></span>
67. <span data-ttu-id="add8c-250">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="add8c-250">Close the page.</span></span>



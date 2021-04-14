---
title: 修改模型和映射以生成包含应用程序数据的单据
description: 本主题介绍如何设计报告配置以生成电子文档与更新应用程序数据。 （第 2 部分 - 生成文档）。
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78b1771d0e01702162192ff20c03facbba4f3513
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751598"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="9c1da-104">修改模型和映射以生成包含应用程序数据的单据</span><span class="sxs-lookup"><span data-stu-id="9c1da-104">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9c1da-105">若要完成此过程中的步骤，首先必须完成“ER 使用应用程序数据更新生成单据（第 2 部分：生成单据）”这一过程。</span><span class="sxs-lookup"><span data-stu-id="9c1da-105">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="9c1da-106">此过程中的步骤介绍如何设计电子申报 (ER) 配置以生成电子单据和更新应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="9c1da-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="9c1da-107">在此过程中，您将修改 ER 配置以开始将其用于生成电子单据和更新应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="9c1da-107">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="9c1da-108">此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。</span><span class="sxs-lookup"><span data-stu-id="9c1da-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="9c1da-109">可使用 DEMF 数据集完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="9c1da-109">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="9c1da-110">修改数据模型</span><span class="sxs-lookup"><span data-stu-id="9c1da-110">Modify data model</span></span>
1. <span data-ttu-id="9c1da-111">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="9c1da-112">在树中，选择“内部统计(模型)”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-112">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="9c1da-113">您将扩展数据模型的使用方式。</span><span class="sxs-lookup"><span data-stu-id="9c1da-113">You will extend how you use the data model.</span></span> <span data-ttu-id="9c1da-114">除了将其用作源以生成内部统计报表，数据模型还将用于收集有关内部统计报告流程的详细信息。</span><span class="sxs-lookup"><span data-stu-id="9c1da-114">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="9c1da-115">然后将把此详细信息用于更新应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="9c1da-115">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="9c1da-116">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-116">Click Designer.</span></span>
4. <span data-ttu-id="9c1da-117">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="9c1da-117">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="9c1da-118">在“作为以下项的新节点”字段中，输入“模型根”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-118">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="9c1da-119">在“名称”字段中，键入“用于应用程序数据更新”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-119">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="9c1da-120">对于应用程序数据更新</span><span class="sxs-lookup"><span data-stu-id="9c1da-120">For application data update</span></span>  
7. <span data-ttu-id="9c1da-121">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-121">Click Add.</span></span>
8. <span data-ttu-id="9c1da-122">在树中，选择“用于应用程序数据更新”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-122">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="9c1da-123">将添加这个新根项以指定将来自内部统计报表（用作数据源）的数据移到应用程序表（更新目标）的数据流。</span><span class="sxs-lookup"><span data-stu-id="9c1da-123">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="9c1da-124">必须为获取过帐到传出单据的数据和为从用于更新应用程序数据的单据获取数据使用不同的根项。</span><span class="sxs-lookup"><span data-stu-id="9c1da-124">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="9c1da-125">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="9c1da-125">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="9c1da-126">在“名称”字段中，键入“存档标题”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-126">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="9c1da-127">存档标题</span><span class="sxs-lookup"><span data-stu-id="9c1da-127">Archive header</span></span>  
11. <span data-ttu-id="9c1da-128">在“物料类型”字段中，选择“记录列表”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-128">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="9c1da-129">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-129">Click Add.</span></span>
    * <span data-ttu-id="9c1da-130">因为您将为生成的每个内部统计报表创建一个记录，所以必须为其创建一个新项。</span><span class="sxs-lookup"><span data-stu-id="9c1da-130">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="9c1da-131">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="9c1da-131">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="9c1da-132">在“名称”字段中，键入“文件名”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-132">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="9c1da-133">文件名</span><span class="sxs-lookup"><span data-stu-id="9c1da-133">File name</span></span>  
15. <span data-ttu-id="9c1da-134">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-134">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="9c1da-135">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-135">Click Add.</span></span>
17. <span data-ttu-id="9c1da-136">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="9c1da-136">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="9c1da-137">在“名称”字段中，键入“行数”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-137">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="9c1da-138">行数</span><span class="sxs-lookup"><span data-stu-id="9c1da-138">Number of lines</span></span>  
19. <span data-ttu-id="9c1da-139">在“物料类型”字段中，选择“整数”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-139">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="9c1da-140">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-140">Click Add.</span></span>
    * <span data-ttu-id="9c1da-141">添加此项以表示当前报告流程期间报告的内部统计交易记录数量。</span><span class="sxs-lookup"><span data-stu-id="9c1da-141">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="9c1da-142">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="9c1da-142">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="9c1da-143">在“名称”字段中，键入“存档行”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-143">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="9c1da-144">存档行</span><span class="sxs-lookup"><span data-stu-id="9c1da-144">Archive lines</span></span>  
23. <span data-ttu-id="9c1da-145">在“物料类型”字段中，选择“记录列表”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-145">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="9c1da-146">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-146">Click Add.</span></span>
    * <span data-ttu-id="9c1da-147">添加此项以表示当前报告流程期间报告的内部统计交易记录列表。</span><span class="sxs-lookup"><span data-stu-id="9c1da-147">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="9c1da-148">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="9c1da-148">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="9c1da-149">在“名称”字段中，键入“金额”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-149">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="9c1da-150">本币金额</span><span class="sxs-lookup"><span data-stu-id="9c1da-150">Amount</span></span>  
27. <span data-ttu-id="9c1da-151">在“物料类型”字段中，选择“实时”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-151">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="9c1da-152">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-152">Click Add.</span></span>
29. <span data-ttu-id="9c1da-153">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="9c1da-153">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="9c1da-154">在“名称”字段中，键入“商品记录标识”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-154">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="9c1da-155">商品记录标识</span><span class="sxs-lookup"><span data-stu-id="9c1da-155">Commodity rec id</span></span>  
31. <span data-ttu-id="9c1da-156">在“物料类型”字段中，选择“Int64”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-156">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="9c1da-157">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-157">Click Add.</span></span>
33. <span data-ttu-id="9c1da-158">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="9c1da-158">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="9c1da-159">在“名称”字段中，键入“物料编号”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-159">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="9c1da-160">物料编号</span><span class="sxs-lookup"><span data-stu-id="9c1da-160">Item number</span></span>  
35. <span data-ttu-id="9c1da-161">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-161">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="9c1da-162">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-162">Click Add.</span></span>
37. <span data-ttu-id="9c1da-163">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-163">Click Save.</span></span>
38. <span data-ttu-id="9c1da-164">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9c1da-164">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="9c1da-165">修改模型映射</span><span class="sxs-lookup"><span data-stu-id="9c1da-165">Modify model mapping</span></span>
1. <span data-ttu-id="9c1da-166">在树中，展开“内部统计(模型)”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-166">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="9c1da-167">在树中，选择“内部统计(模型)\内部统计(映射)”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-167">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="9c1da-168">修改现有模型映射，以便开始讲起用于应用程序数据更新和存档内部统计报告详细信息。</span><span class="sxs-lookup"><span data-stu-id="9c1da-168">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="9c1da-169">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-169">Click Designer.</span></span>
4. <span data-ttu-id="9c1da-170">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-170">Click New.</span></span>
5. <span data-ttu-id="9c1da-171">在“名称”字段中，键入“更新存档”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-171">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="9c1da-172">更新存档</span><span class="sxs-lookup"><span data-stu-id="9c1da-172">Update archive</span></span>  
6. <span data-ttu-id="9c1da-173">在“方向”字段中，选择“截止目标”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-173">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="9c1da-174">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-174">Click Save.</span></span>
    * <span data-ttu-id="9c1da-175">这个新映射指定将来自数据模型的数据（内部统计报告详细信息）移到应用程序表（更新目标）的数据流。</span><span class="sxs-lookup"><span data-stu-id="9c1da-175">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="9c1da-176">请注意，必须使用不同模型的根项来为报告流程从应用程序获取数据，然后将来自数据模型的数据用于应用程序数据更新。</span><span class="sxs-lookup"><span data-stu-id="9c1da-176">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="9c1da-177">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-177">Click Designer.</span></span>
9. <span data-ttu-id="9c1da-178">在树结构中，选择“数据模型\数据模型”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-178">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="9c1da-179">添加所需数据源。</span><span class="sxs-lookup"><span data-stu-id="9c1da-179">Add the required data source.</span></span> <span data-ttu-id="9c1da-180">这是其中包含必须存档的所报告内部统计交易记录详细信息的数据模型。</span><span class="sxs-lookup"><span data-stu-id="9c1da-180">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="9c1da-181">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-181">Click Add root.</span></span>
11. <span data-ttu-id="9c1da-182">在“名称”字段中，键入“模型”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-182">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="9c1da-183">模型</span><span class="sxs-lookup"><span data-stu-id="9c1da-183">model</span></span>  
12. <span data-ttu-id="9c1da-184">在“定义”字段中，输入或选择值“用于应用程序数据更新”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-184">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="9c1da-185">对于应用程序数据更新</span><span class="sxs-lookup"><span data-stu-id="9c1da-185">For application data update</span></span>  
13. <span data-ttu-id="9c1da-186">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-186">Click OK.</span></span>
14. <span data-ttu-id="9c1da-187">在树中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-187">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="9c1da-188">在树结构中，选择“功能\计算字段”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-188">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="9c1da-189">在树中，选择“模型\存档标题”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-189">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="9c1da-190">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-190">Click Add.</span></span>
    * <span data-ttu-id="9c1da-191">因为需要为存档枚举所报告内部统计交易记录，所以必须添加相应的数据源。</span><span class="sxs-lookup"><span data-stu-id="9c1da-191">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="9c1da-192">在“名称”字段中，键入“枚举行”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-192">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="9c1da-193">枚举行</span><span class="sxs-lookup"><span data-stu-id="9c1da-193">Enumerated lines</span></span>  
19. <span data-ttu-id="9c1da-194">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-194">Click Edit formula.</span></span>
20. <span data-ttu-id="9c1da-195">在树中，选择“列表\ENUMERATE”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-195">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="9c1da-196">单击“添加”功能。</span><span class="sxs-lookup"><span data-stu-id="9c1da-196">Click Add function.</span></span>
22. <span data-ttu-id="9c1da-197">在树结构中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-197">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="9c1da-198">在树中，展开“模型\存档标题”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-198">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="9c1da-199">在树中，选择“模型\存档标题\存档行”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-199">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="9c1da-200">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-200">Click Add data source.</span></span>
26. <span data-ttu-id="9c1da-201">在“公式”字段中，输入“ENUMERATE(model.'Archive header'.'Archive lines')”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-201">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="9c1da-202">ENUMERATE(model.'Archive header'.'Archive lines')</span><span class="sxs-lookup"><span data-stu-id="9c1da-202">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="9c1da-203">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-203">Click Save.</span></span>
28. <span data-ttu-id="9c1da-204">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9c1da-204">Close the page.</span></span>
29. <span data-ttu-id="9c1da-205">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-205">Click OK.</span></span>
30. <span data-ttu-id="9c1da-206">单击”添加目标“。</span><span class="sxs-lookup"><span data-stu-id="9c1da-206">Click Add destination.</span></span>
    * <span data-ttu-id="9c1da-207">将应用程序表添加为需要更新以存档所报告内部统计交易记录详细信息的必需目标。</span><span class="sxs-lookup"><span data-stu-id="9c1da-207">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="9c1da-208">在“名称”字段中，键入“存档”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-208">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="9c1da-209">存档</span><span class="sxs-lookup"><span data-stu-id="9c1da-209">Archive</span></span>  
32. <span data-ttu-id="9c1da-210">在“表名”字段中，键入“IntrastatArchiveGeneral”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-210">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="9c1da-211">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="9c1da-211">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="9c1da-212">保留记录操作“插入”，以便在存档各内部统计报告流程详细信息期间添加记录。</span><span class="sxs-lookup"><span data-stu-id="9c1da-212">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="9c1da-213">在“记录信息日志”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-213">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="9c1da-214">选择“是”以获取有关应用程序数据更新问题的信息。</span><span class="sxs-lookup"><span data-stu-id="9c1da-214">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="9c1da-215">在“跳过记录操作验证”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-215">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="9c1da-216">选择“是”以禁止有关空“内部统计存档标识”字段的验证错误。</span><span class="sxs-lookup"><span data-stu-id="9c1da-216">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="9c1da-217">这将在添加记录后，基于“外贸参数”窗体中为此表配置的序号完成。</span><span class="sxs-lookup"><span data-stu-id="9c1da-217">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="9c1da-218">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-218">Click OK.</span></span>
    * <span data-ttu-id="9c1da-219">绑定所添加数据源（基于所选根项过滤后的模型）的元素和来自所添加目标的元素。</span><span class="sxs-lookup"><span data-stu-id="9c1da-219">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="9c1da-220">在树中，展开“存档”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-220">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="9c1da-221">在树中，展开“存档\<关系”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-221">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="9c1da-222">在树结构中，展开“存档\<关系\IntrastatArchiveDetail”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-222">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="9c1da-223">在树中，选择“存档\<关系\IntrastatArchiveDetail\Amount(AmountMST)”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-223">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="9c1da-224">在树中，展开“模型\存档标题\枚举行”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-224">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="9c1da-225">在树中，展开“模型\存档标题\枚举行\值”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-225">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="9c1da-226">在树中，选择“模型\存档标题\枚举行\值\金额”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-226">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="9c1da-227">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-227">Click Bind.</span></span>
44. <span data-ttu-id="9c1da-228">在树中，选择“存档\<关系\IntrastatArchiveDetail\Commodity(IntrastatCommodity)”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-228">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="9c1da-229">在树中，选择“模型\存档标题\枚举行\值\商品记录标识”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-229">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="9c1da-230">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-230">Click Bind.</span></span>
47. <span data-ttu-id="9c1da-231">在树中，选择“存档\<关系\IntrastatArchiveDetail\物料编号(ItemId)”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-231">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="9c1da-232">在树中，选择“模型\存档标题\枚举行\值\物料编号”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-232">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="9c1da-233">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-233">Click Bind.</span></span>
50. <span data-ttu-id="9c1da-234">在树中，选择“存档\<关系\IntrastatArchiveDetail\行号(LineNumber)”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-234">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="9c1da-235">在树中，选择“模型\存档标题\枚举行\编号”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-235">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="9c1da-236">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-236">Click Bind.</span></span>
53. <span data-ttu-id="9c1da-237">在树中，选择“存档\<关系\IntrastatArchiveDetail”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-237">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="9c1da-238">在树中，选择“模型\存档标题\枚举行”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-238">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="9c1da-239">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-239">Click Bind.</span></span>
56. <span data-ttu-id="9c1da-240">在树中，选择“存档\文件名(FileName)”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-240">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="9c1da-241">在树中，选择“模型\存档标题\文件名”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-241">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="9c1da-242">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-242">Click Bind.</span></span>
59. <span data-ttu-id="9c1da-243">在树中，选择“存档\行数(NumberOfLines)“。</span><span class="sxs-lookup"><span data-stu-id="9c1da-243">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="9c1da-244">在树中，选择“模型\存档标题\行数”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-244">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="9c1da-245">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-245">Click Bind.</span></span>
62. <span data-ttu-id="9c1da-246">在树中，选择“存档”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-246">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="9c1da-247">在树中，选择“模型\存档标题”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-247">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="9c1da-248">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-248">Click Bind.</span></span>
65. <span data-ttu-id="9c1da-249">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="9c1da-249">Click Save.</span></span>
66. <span data-ttu-id="9c1da-250">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9c1da-250">Close the page.</span></span>
67. <span data-ttu-id="9c1da-251">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9c1da-251">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
---
title: 修改模型和映射以生成包含应用程序数据的单据
description: 若要完成此过程中的步骤，首先必须完成“ER 使用应用程序数据更新生成单据（第 2 部分 - 生成单据）”这一过程。
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3401ec98ac1b61572d07fbb30d4465de78473fca
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684563"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="a0a92-103">修改模型和映射以生成包含应用程序数据的单据</span><span class="sxs-lookup"><span data-stu-id="a0a92-103">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0a92-104">若要完成此过程中的步骤，首先必须完成“ER 使用应用程序数据更新生成单据（第 2 部分：生成单据）”这一过程。</span><span class="sxs-lookup"><span data-stu-id="a0a92-104">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="a0a92-105">此过程中的步骤介绍如何设计电子申报 (ER) 配置以生成电子单据和更新应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="a0a92-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="a0a92-106">在此过程中，您将修改 ER 配置以开始将其用于生成电子单据和更新应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="a0a92-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="a0a92-107">此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。</span><span class="sxs-lookup"><span data-stu-id="a0a92-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="a0a92-108">可使用 DEMF 数据集完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="a0a92-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="a0a92-109">修改数据模型</span><span class="sxs-lookup"><span data-stu-id="a0a92-109">Modify data model</span></span>
1. <span data-ttu-id="a0a92-110">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a0a92-111">在树中，选择“内部统计(模型)”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="a0a92-112">您将扩展数据模型的使用方式。</span><span class="sxs-lookup"><span data-stu-id="a0a92-112">You will extend how you use the data model.</span></span> <span data-ttu-id="a0a92-113">除了将其用作源以生成内部统计报表，数据模型还将用于收集有关内部统计报告流程的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a0a92-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="a0a92-114">然后将把此详细信息用于更新应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="a0a92-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="a0a92-115">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-115">Click Designer.</span></span>
4. <span data-ttu-id="a0a92-116">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="a0a92-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="a0a92-117">在“作为以下项的新节点”字段中，输入“模型根”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="a0a92-118">在“名称”字段中，键入“用于应用程序数据更新”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="a0a92-119">对于应用程序数据更新</span><span class="sxs-lookup"><span data-stu-id="a0a92-119">For application data update</span></span>  
7. <span data-ttu-id="a0a92-120">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-120">Click Add.</span></span>
8. <span data-ttu-id="a0a92-121">在树中，选择“用于应用程序数据更新”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="a0a92-122">将添加这个新根项以指定将来自内部统计报表（用作数据源）的数据移到应用程序表（更新目标）的数据流。</span><span class="sxs-lookup"><span data-stu-id="a0a92-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="a0a92-123">必须为获取过帐到传出单据的数据和为从用于更新应用程序数据的单据获取数据使用不同的根项。</span><span class="sxs-lookup"><span data-stu-id="a0a92-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="a0a92-124">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="a0a92-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="a0a92-125">在“名称”字段中，键入“存档标题”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="a0a92-126">存档标题</span><span class="sxs-lookup"><span data-stu-id="a0a92-126">Archive header</span></span>  
11. <span data-ttu-id="a0a92-127">在“物料类型”字段中，选择“记录列表”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="a0a92-128">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-128">Click Add.</span></span>
    * <span data-ttu-id="a0a92-129">因为您将为生成的每个内部统计报表创建一个记录，所以必须为其创建一个新项。</span><span class="sxs-lookup"><span data-stu-id="a0a92-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="a0a92-130">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="a0a92-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="a0a92-131">在“名称”字段中，键入“文件名”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="a0a92-132">文件名</span><span class="sxs-lookup"><span data-stu-id="a0a92-132">File name</span></span>  
15. <span data-ttu-id="a0a92-133">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="a0a92-134">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-134">Click Add.</span></span>
17. <span data-ttu-id="a0a92-135">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="a0a92-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="a0a92-136">在“名称”字段中，键入“行数”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="a0a92-137">行数</span><span class="sxs-lookup"><span data-stu-id="a0a92-137">Number of lines</span></span>  
19. <span data-ttu-id="a0a92-138">在“物料类型”字段中，选择“整数”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="a0a92-139">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-139">Click Add.</span></span>
    * <span data-ttu-id="a0a92-140">添加此项以表示当前报告流程期间报告的内部统计交易记录数量。</span><span class="sxs-lookup"><span data-stu-id="a0a92-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="a0a92-141">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="a0a92-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="a0a92-142">在“名称”字段中，键入“存档行”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="a0a92-143">存档行</span><span class="sxs-lookup"><span data-stu-id="a0a92-143">Archive lines</span></span>  
23. <span data-ttu-id="a0a92-144">在“物料类型”字段中，选择“记录列表”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="a0a92-145">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-145">Click Add.</span></span>
    * <span data-ttu-id="a0a92-146">添加此项以表示当前报告流程期间报告的内部统计交易记录列表。</span><span class="sxs-lookup"><span data-stu-id="a0a92-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="a0a92-147">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="a0a92-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="a0a92-148">在“名称”字段中，键入“金额”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="a0a92-149">本币金额</span><span class="sxs-lookup"><span data-stu-id="a0a92-149">Amount</span></span>  
27. <span data-ttu-id="a0a92-150">在“物料类型”字段中，选择“实时”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="a0a92-151">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-151">Click Add.</span></span>
29. <span data-ttu-id="a0a92-152">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="a0a92-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="a0a92-153">在“名称”字段中，键入“商品记录标识”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="a0a92-154">商品记录标识</span><span class="sxs-lookup"><span data-stu-id="a0a92-154">Commodity rec id</span></span>  
31. <span data-ttu-id="a0a92-155">在“物料类型”字段中，选择“Int64”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="a0a92-156">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-156">Click Add.</span></span>
33. <span data-ttu-id="a0a92-157">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="a0a92-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="a0a92-158">在“名称”字段中，键入“物料编号”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="a0a92-159">物料编号</span><span class="sxs-lookup"><span data-stu-id="a0a92-159">Item number</span></span>  
35. <span data-ttu-id="a0a92-160">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="a0a92-161">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-161">Click Add.</span></span>
37. <span data-ttu-id="a0a92-162">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-162">Click Save.</span></span>
38. <span data-ttu-id="a0a92-163">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a0a92-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="a0a92-164">修改模型映射</span><span class="sxs-lookup"><span data-stu-id="a0a92-164">Modify model mapping</span></span>
1. <span data-ttu-id="a0a92-165">在树中，展开“内部统计(模型)”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="a0a92-166">在树中，选择“内部统计(模型)\内部统计(映射)”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="a0a92-167">修改现有模型映射，以便开始讲起用于应用程序数据更新和存档内部统计报告详细信息。</span><span class="sxs-lookup"><span data-stu-id="a0a92-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="a0a92-168">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-168">Click Designer.</span></span>
4. <span data-ttu-id="a0a92-169">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-169">Click New.</span></span>
5. <span data-ttu-id="a0a92-170">在“名称”字段中，键入“更新存档”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="a0a92-171">更新存档</span><span class="sxs-lookup"><span data-stu-id="a0a92-171">Update archive</span></span>  
6. <span data-ttu-id="a0a92-172">在“方向”字段中，选择“截止目标”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="a0a92-173">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-173">Click Save.</span></span>
    * <span data-ttu-id="a0a92-174">这个新映射指定将来自数据模型的数据（内部统计报告详细信息）移到应用程序表（更新目标）的数据流。</span><span class="sxs-lookup"><span data-stu-id="a0a92-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="a0a92-175">请注意，必须使用不同模型的根项来为报告流程从应用程序获取数据，然后将来自数据模型的数据用于应用程序数据更新。</span><span class="sxs-lookup"><span data-stu-id="a0a92-175">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="a0a92-176">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-176">Click Designer.</span></span>
9. <span data-ttu-id="a0a92-177">在树结构中，选择“数据模型\数据模型”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="a0a92-178">添加所需数据源。</span><span class="sxs-lookup"><span data-stu-id="a0a92-178">Add the required data source.</span></span> <span data-ttu-id="a0a92-179">这是其中包含必须存档的所报告内部统计交易记录详细信息的数据模型。</span><span class="sxs-lookup"><span data-stu-id="a0a92-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="a0a92-180">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-180">Click Add root.</span></span>
11. <span data-ttu-id="a0a92-181">在“名称”字段中，键入“模型”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="a0a92-182">模型</span><span class="sxs-lookup"><span data-stu-id="a0a92-182">model</span></span>  
12. <span data-ttu-id="a0a92-183">在“定义”字段中，输入或选择值“用于应用程序数据更新”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-183">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="a0a92-184">对于应用程序数据更新</span><span class="sxs-lookup"><span data-stu-id="a0a92-184">For application data update</span></span>  
13. <span data-ttu-id="a0a92-185">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-185">Click OK.</span></span>
14. <span data-ttu-id="a0a92-186">在树中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="a0a92-187">在树结构中，选择“功能\计算字段”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="a0a92-188">在树中，选择“模型\存档标题”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="a0a92-189">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-189">Click Add.</span></span>
    * <span data-ttu-id="a0a92-190">因为需要为存档枚举所报告内部统计交易记录，所以必须添加相应的数据源。</span><span class="sxs-lookup"><span data-stu-id="a0a92-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="a0a92-191">在“名称”字段中，键入“枚举行”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="a0a92-192">枚举行</span><span class="sxs-lookup"><span data-stu-id="a0a92-192">Enumerated lines</span></span>  
19. <span data-ttu-id="a0a92-193">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-193">Click Edit formula.</span></span>
20. <span data-ttu-id="a0a92-194">在树中，选择“列表\ENUMERATE”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="a0a92-195">单击“添加”功能。</span><span class="sxs-lookup"><span data-stu-id="a0a92-195">Click Add function.</span></span>
22. <span data-ttu-id="a0a92-196">在树结构中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="a0a92-197">在树中，展开“模型\存档标题”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="a0a92-198">在树中，选择“模型\存档标题\存档行”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="a0a92-199">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-199">Click Add data source.</span></span>
26. <span data-ttu-id="a0a92-200">在“公式”字段中，输入“ENUMERATE(model.'Archive header'.'Archive lines')”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="a0a92-201">ENUMERATE(model.'Archive header'.'Archive lines')</span><span class="sxs-lookup"><span data-stu-id="a0a92-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="a0a92-202">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-202">Click Save.</span></span>
28. <span data-ttu-id="a0a92-203">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a0a92-203">Close the page.</span></span>
29. <span data-ttu-id="a0a92-204">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-204">Click OK.</span></span>
30. <span data-ttu-id="a0a92-205">单击”添加目标“。</span><span class="sxs-lookup"><span data-stu-id="a0a92-205">Click Add destination.</span></span>
    * <span data-ttu-id="a0a92-206">将应用程序表添加为需要更新以存档所报告内部统计交易记录详细信息的必需目标。</span><span class="sxs-lookup"><span data-stu-id="a0a92-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="a0a92-207">在“名称”字段中，键入“存档”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="a0a92-208">存档</span><span class="sxs-lookup"><span data-stu-id="a0a92-208">Archive</span></span>  
32. <span data-ttu-id="a0a92-209">在“表名”字段中，键入“IntrastatArchiveGeneral”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="a0a92-210">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="a0a92-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="a0a92-211">保留记录操作“插入”，以便在存档各内部统计报告流程详细信息期间添加记录。</span><span class="sxs-lookup"><span data-stu-id="a0a92-211">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="a0a92-212">在“记录信息日志”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="a0a92-213">选择“是”以获取有关应用程序数据更新问题的信息。</span><span class="sxs-lookup"><span data-stu-id="a0a92-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="a0a92-214">在“跳过记录操作验证”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="a0a92-215">选择“是”以禁止有关空“内部统计存档标识”字段的验证错误。</span><span class="sxs-lookup"><span data-stu-id="a0a92-215">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="a0a92-216">这将在添加记录后，基于“外贸参数”窗体中为此表配置的序号完成。</span><span class="sxs-lookup"><span data-stu-id="a0a92-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="a0a92-217">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-217">Click OK.</span></span>
    * <span data-ttu-id="a0a92-218">绑定所添加数据源（基于所选根项过滤后的模型）的元素和来自所添加目标的元素。</span><span class="sxs-lookup"><span data-stu-id="a0a92-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="a0a92-219">在树中，展开“存档”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="a0a92-220">在树中，展开“存档\<关系”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="a0a92-221">在树结构中，展开“存档\<关系\IntrastatArchiveDetail”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="a0a92-222">在树中，选择“存档\<关系\IntrastatArchiveDetail\Amount(AmountMST)”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="a0a92-223">在树中，展开“模型\存档标题\枚举行”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="a0a92-224">在树中，展开“模型\存档标题\枚举行\值”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="a0a92-225">在树中，选择“模型\存档标题\枚举行\值\金额”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="a0a92-226">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-226">Click Bind.</span></span>
44. <span data-ttu-id="a0a92-227">在树中，选择“存档\<关系\IntrastatArchiveDetail\Commodity(IntrastatCommodity)”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="a0a92-228">在树中，选择“模型\存档标题\枚举行\值\商品记录标识”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="a0a92-229">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-229">Click Bind.</span></span>
47. <span data-ttu-id="a0a92-230">在树中，选择“存档\<关系\IntrastatArchiveDetail\物料编号(ItemId)”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="a0a92-231">在树中，选择“模型\存档标题\枚举行\值\物料编号”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="a0a92-232">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-232">Click Bind.</span></span>
50. <span data-ttu-id="a0a92-233">在树中，选择“存档\<关系\IntrastatArchiveDetail\行号(LineNumber)”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="a0a92-234">在树中，选择“模型\存档标题\枚举行\编号”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="a0a92-235">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-235">Click Bind.</span></span>
53. <span data-ttu-id="a0a92-236">在树中，选择“存档\<关系\IntrastatArchiveDetail”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="a0a92-237">在树中，选择“模型\存档标题\枚举行”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="a0a92-238">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-238">Click Bind.</span></span>
56. <span data-ttu-id="a0a92-239">在树中，选择“存档\文件名(FileName)”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="a0a92-240">在树中，选择“模型\存档标题\文件名”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="a0a92-241">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-241">Click Bind.</span></span>
59. <span data-ttu-id="a0a92-242">在树中，选择“存档\行数(NumberOfLines)“。</span><span class="sxs-lookup"><span data-stu-id="a0a92-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="a0a92-243">在树中，选择“模型\存档标题\行数”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="a0a92-244">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-244">Click Bind.</span></span>
62. <span data-ttu-id="a0a92-245">在树中，选择“存档”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="a0a92-246">在树中，选择“模型\存档标题”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="a0a92-247">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-247">Click Bind.</span></span>
65. <span data-ttu-id="a0a92-248">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a0a92-248">Click Save.</span></span>
66. <span data-ttu-id="a0a92-249">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a0a92-249">Close the page.</span></span>
67. <span data-ttu-id="a0a92-250">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a0a92-250">Close the page.</span></span>


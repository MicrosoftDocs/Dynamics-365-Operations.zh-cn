--- 
title: "针对电子申报 (ER) 修改格式以通过更新应用程序生成单据"
description: "若要完成此过程中的步骤，首先必须完成“ER 使用应用程序数据更新生成单据（第 3 部分 - 修改模型和映射）”这一过程。"
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
ms.openlocfilehash: 47a1fe9cbfc80adbd5d375221912a2fa9787af19
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="modify-format-to-generate-documents-with-application-data-update-for-electronic-reporting-er"></a><span data-ttu-id="5144e-103">针对电子申报 (ER) 修改格式以通过更新应用程序生成单据</span><span class="sxs-lookup"><span data-stu-id="5144e-103">Modify format to generate documents with application data update for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5144e-104">若要完成此过程中的步骤，首先必须完成“ER 使用应用程序数据更新生成单据（第 3 部分：修改模型和映射）”这一过程。</span><span class="sxs-lookup"><span data-stu-id="5144e-104">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 3: Modify model and mapping)".</span></span>

<span data-ttu-id="5144e-105">此过程中的步骤介绍如何设计电子申报 (ER) 配置以生成电子单据和更新应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="5144e-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="5144e-106">在此过程中，您将修改 ER 配置以不仅将其用于生成电子单据，还用于更新应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="5144e-106">In this procedure, you will modify the ER configurations to not just use them to generate electronic documents, but also to update application data.</span></span> <span data-ttu-id="5144e-107">此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。</span><span class="sxs-lookup"><span data-stu-id="5144e-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="5144e-108">可使用 DEMF 数据集完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="5144e-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-format-to-collect-details-of-reporting"></a><span data-ttu-id="5144e-109">修改格式以收集报告的详细信息</span><span class="sxs-lookup"><span data-stu-id="5144e-109">Modify format to collect details of reporting</span></span>
1. <span data-ttu-id="5144e-110">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="5144e-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="5144e-111">在树中，展开“内部统计(模型)”。</span><span class="sxs-lookup"><span data-stu-id="5144e-111">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="5144e-112">在树中，选择“内部统计(模型)\内部统计(格式)”。</span><span class="sxs-lookup"><span data-stu-id="5144e-112">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="5144e-113">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="5144e-113">Click Designer.</span></span>
5. <span data-ttu-id="5144e-114">在树中，展开“文件”。</span><span class="sxs-lookup"><span data-stu-id="5144e-114">In the tree, expand 'File'.</span></span>
6. <span data-ttu-id="5144e-115">在树中，展开“文件\申报”。</span><span class="sxs-lookup"><span data-stu-id="5144e-115">In the tree, expand 'File\Declaration'.</span></span>
7. <span data-ttu-id="5144e-116">在树中，选择“文件\申报\数据”。</span><span class="sxs-lookup"><span data-stu-id="5144e-116">In the tree, select 'File\Declaration\Data'.</span></span>
8. <span data-ttu-id="5144e-117">在“多样性”字段中，选择“一个 多个”。</span><span class="sxs-lookup"><span data-stu-id="5144e-117">In the Multiplicity field, select 'One many'.</span></span>
    * <span data-ttu-id="5144e-118">配置此格式元素以存档内部统计报告流程的详细信息。</span><span class="sxs-lookup"><span data-stu-id="5144e-118">Configure this format element to archive details of the Intrastat reporting process.</span></span> <span data-ttu-id="5144e-119">此项表示存档的标题记录。</span><span class="sxs-lookup"><span data-stu-id="5144e-119">This item represents the archive’s header record.</span></span>  
9. <span data-ttu-id="5144e-120">在树中，展开“文件\申报\数据”。</span><span class="sxs-lookup"><span data-stu-id="5144e-120">In the tree, expand 'File\Declaration\Data'.</span></span>
10. <span data-ttu-id="5144e-121">在树中，选择“文件\申报\数据\物料”。</span><span class="sxs-lookup"><span data-stu-id="5144e-121">In the tree, select 'File\Declaration\Data\Item'.</span></span>
11. <span data-ttu-id="5144e-122">在“多样性”字段中，选择“零个 多个”。</span><span class="sxs-lookup"><span data-stu-id="5144e-122">In the Multiplicity field, select 'Zero many'.</span></span>
    * <span data-ttu-id="5144e-123">配置此格式元素以存档内部统计报告流程的详细信息。</span><span class="sxs-lookup"><span data-stu-id="5144e-123">Configure this format element to archive details of the Intrastat reporting process.</span></span> <span data-ttu-id="5144e-124">此项将表示存档的行的列表。</span><span class="sxs-lookup"><span data-stu-id="5144e-124">This item will represent the list of archived lines.</span></span>  
12. <span data-ttu-id="5144e-125">在树中，展开“文件\申报\数据\物料”。</span><span class="sxs-lookup"><span data-stu-id="5144e-125">In the tree, expand 'File\Declaration\Data\Item'.</span></span>
13. <span data-ttu-id="5144e-126">在树中，选择“文件\申报\数据\物料\Dim1”。</span><span class="sxs-lookup"><span data-stu-id="5144e-126">In the tree, select 'File\Declaration\Data\Item\Dim1'.</span></span>
14. <span data-ttu-id="5144e-127">在“已排除”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="5144e-127">Select Yes in the Excluded field.</span></span>
    * <span data-ttu-id="5144e-128">您将不存档此数据，所以可从内部统计报告详细信息的数据源排除此格式元素。</span><span class="sxs-lookup"><span data-stu-id="5144e-128">You will not archive this data, so you can exclude this format element from the data source of Intrastat reporting details.</span></span>  
15. <span data-ttu-id="5144e-129">在树中，展开“文件\申报\数据\物料\Dim1”。</span><span class="sxs-lookup"><span data-stu-id="5144e-129">In the tree, expand 'File\Declaration\Data\Item\Dim1'.</span></span>
16. <span data-ttu-id="5144e-130">在树中，选择“文件\申报\数据\物料\Dim1\属性”。</span><span class="sxs-lookup"><span data-stu-id="5144e-130">In the tree, select 'File\Declaration\Data\Item\Dim1\property'.</span></span>
17. <span data-ttu-id="5144e-131">在“已排除”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="5144e-131">Select Yes in the Excluded field.</span></span>
18. <span data-ttu-id="5144e-132">在树中，选择“文件\申报\数据\物料\Dim1\日期”。</span><span class="sxs-lookup"><span data-stu-id="5144e-132">In the tree, select 'File\Declaration\Data\Item\Dim1\date'.</span></span>
19. <span data-ttu-id="5144e-133">在“已排除”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="5144e-133">Select Yes in the Excluded field.</span></span>
20. <span data-ttu-id="5144e-134">在树中，选择“文件\申报\数据\物料\Dim2”。</span><span class="sxs-lookup"><span data-stu-id="5144e-134">In the tree, select 'File\Declaration\Data\Item\Dim2'.</span></span>
21. <span data-ttu-id="5144e-135">在“已排除”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="5144e-135">Select Yes in the Excluded field.</span></span>
22. <span data-ttu-id="5144e-136">在树中，展开“文件\申报\数据\物料\Dim2”。</span><span class="sxs-lookup"><span data-stu-id="5144e-136">In the tree, expand 'File\Declaration\Data\Item\Dim2'.</span></span>
23. <span data-ttu-id="5144e-137">在树中，选择“文件\申报\数据\物料\Dim2\属性”。</span><span class="sxs-lookup"><span data-stu-id="5144e-137">In the tree, select 'File\Declaration\Data\Item\Dim2\property'.</span></span>
24. <span data-ttu-id="5144e-138">在“已排除”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="5144e-138">Select Yes in the Excluded field.</span></span>
25. <span data-ttu-id="5144e-139">在树中，选择“文件\申报\数据\物料\Dim2\代码”。</span><span class="sxs-lookup"><span data-stu-id="5144e-139">In the tree, select 'File\Declaration\Data\Item\Dim2\code'.</span></span>
26. <span data-ttu-id="5144e-140">在“已排除”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="5144e-140">Select Yes in the Excluded field.</span></span>
27. <span data-ttu-id="5144e-141">在树中，选择“文件\申报\数据\物料\Dim3”。</span><span class="sxs-lookup"><span data-stu-id="5144e-141">In the tree, select 'File\Declaration\Data\Item\Dim3'.</span></span>
    * <span data-ttu-id="5144e-142">多个格式元素的名称可以相同。</span><span class="sxs-lookup"><span data-stu-id="5144e-142">Several format elements can have the same name.</span></span> <span data-ttu-id="5144e-143">例如，Dim。将此格式用作存档内部统计报告详细信息的数据源时，不能明确识别它们，所以需要为这些格式元素定义备用名称。</span><span class="sxs-lookup"><span data-stu-id="5144e-143">For example, Dim. You cannot explicitly recognize them when you use this format as a data source for archiving Intrastat reporting details, so you need to define the alternative names for these format elements.</span></span>   
28. <span data-ttu-id="5144e-144">在“名称”字段中，键入“金额”。</span><span class="sxs-lookup"><span data-stu-id="5144e-144">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="5144e-145">本币金额</span><span class="sxs-lookup"><span data-stu-id="5144e-145">Amount</span></span>  
29. <span data-ttu-id="5144e-146">在“多样性”字段中，选择“正好一个”。</span><span class="sxs-lookup"><span data-stu-id="5144e-146">In the Multiplicity field, select 'Exactly one'.</span></span>
30. <span data-ttu-id="5144e-147">在树中，选择“文件\申报\数据\物料\Dim4”。</span><span class="sxs-lookup"><span data-stu-id="5144e-147">In the tree, select 'File\Declaration\Data\Item\Dim4'.</span></span>
31. <span data-ttu-id="5144e-148">在“名称”字段中，键入“物料”。</span><span class="sxs-lookup"><span data-stu-id="5144e-148">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="5144e-149">项目</span><span class="sxs-lookup"><span data-stu-id="5144e-149">Item</span></span>  
32. <span data-ttu-id="5144e-150">在“多样性”字段中，选择“正好一个”。</span><span class="sxs-lookup"><span data-stu-id="5144e-150">In the Multiplicity field, select 'Exactly one'.</span></span>
    * <span data-ttu-id="5144e-151">除了设计格式元素，还必须存档以下内部统计报告详细信息：报告的各商品物料的唯一记录标识和所生成文件的名称。</span><span class="sxs-lookup"><span data-stu-id="5144e-151">In addition to the design format elements, the following Intrastat reporting details must be archived: unique record identification of each reported commodity item and name of the generated file.</span></span> <span data-ttu-id="5144e-152">因为将不在内部统计报表中填充此数据，所以您需要将与这些详细信息元素有关的格式作为数据源项添加。</span><span class="sxs-lookup"><span data-stu-id="5144e-152">Because this data will not be populated in the Intrastat report, you need to add the format that is related to these detail elements as data source items.</span></span>  
33. <span data-ttu-id="5144e-153">在树中，选择“文件\申报\数据”。</span><span class="sxs-lookup"><span data-stu-id="5144e-153">In the tree, select 'File\Declaration\Data'.</span></span>
34. <span data-ttu-id="5144e-154">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="5144e-154">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="5144e-155">在树中，选择“数据源\物料”。</span><span class="sxs-lookup"><span data-stu-id="5144e-155">In the tree, select 'Data source\Item'.</span></span>
36. <span data-ttu-id="5144e-156">在“名称”字段中，键入“文件名”。</span><span class="sxs-lookup"><span data-stu-id="5144e-156">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="5144e-157">文件名</span><span class="sxs-lookup"><span data-stu-id="5144e-157">File name</span></span>  
37. <span data-ttu-id="5144e-158">在“数据类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="5144e-158">In the Data type field, select 'String'.</span></span>
38. <span data-ttu-id="5144e-159">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5144e-159">Click OK.</span></span>
39. <span data-ttu-id="5144e-160">在树中，选择“文件\申报\数据\物料”。</span><span class="sxs-lookup"><span data-stu-id="5144e-160">In the tree, select 'File\Declaration\Data\Item'.</span></span>
40. <span data-ttu-id="5144e-161">单击“添加物料”。</span><span class="sxs-lookup"><span data-stu-id="5144e-161">Click Add Item.</span></span>
41. <span data-ttu-id="5144e-162">在“名称”字段中，键入“商品记录标识”。</span><span class="sxs-lookup"><span data-stu-id="5144e-162">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="5144e-163">商品记录标识</span><span class="sxs-lookup"><span data-stu-id="5144e-163">Commodity rec id</span></span>  
42. <span data-ttu-id="5144e-164">在“数据类型”字段中，选择“Int64”。</span><span class="sxs-lookup"><span data-stu-id="5144e-164">In the Data type field, select 'Int64'.</span></span>
43. <span data-ttu-id="5144e-165">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5144e-165">Click OK.</span></span>
44. <span data-ttu-id="5144e-166">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="5144e-166">Click the Mapping tab.</span></span>
45. <span data-ttu-id="5144e-167">在树中，选择“文件\申报\数据\文件名”。</span><span class="sxs-lookup"><span data-stu-id="5144e-167">In the tree, select 'File\Declaration\Data\File name'.</span></span>
46. <span data-ttu-id="5144e-168">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="5144e-168">Click Bind.</span></span>
47. <span data-ttu-id="5144e-169">在树结构中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="5144e-169">In the tree, expand 'model'.</span></span>
48. <span data-ttu-id="5144e-170">在树中，展开“模型\交易记录”。</span><span class="sxs-lookup"><span data-stu-id="5144e-170">In the tree, expand 'model\Transactions'.</span></span>
49. <span data-ttu-id="5144e-171">在树中，选择“文件\申报\数据\物料 = model.Transactions\商品记录标识”。</span><span class="sxs-lookup"><span data-stu-id="5144e-171">In the tree, select 'File\Declaration\Data\Item =  model.Transactions\Commodity rec id'.</span></span>
50. <span data-ttu-id="5144e-172">在树结构中，选择“模型\交易记录\商品记录标识”。</span><span class="sxs-lookup"><span data-stu-id="5144e-172">In the tree, select 'model\Transactions\Commodity rec id'.</span></span>
51. <span data-ttu-id="5144e-173">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="5144e-173">Click Bind.</span></span>
52. <span data-ttu-id="5144e-174">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="5144e-174">Click Save.</span></span>

## <a name="modify-format-to-memorize-details-of-reporting"></a><span data-ttu-id="5144e-175">修改格式以记住报告的详细信息</span><span class="sxs-lookup"><span data-stu-id="5144e-175">Modify format to memorize details of reporting</span></span>
1. <span data-ttu-id="5144e-176">单击”将格式映射到模型“。</span><span class="sxs-lookup"><span data-stu-id="5144e-176">Click Map format to model.</span></span>
2. <span data-ttu-id="5144e-177">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="5144e-177">Click New.</span></span>
3. <span data-ttu-id="5144e-178">在“定义”字段中，输入或选择“用于应用程序数据更新”根项。</span><span class="sxs-lookup"><span data-stu-id="5144e-178">In the Definition field, enter or select the ‘For application data update’ root item.</span></span>
    * <span data-ttu-id="5144e-179">对于应用程序数据更新</span><span class="sxs-lookup"><span data-stu-id="5144e-179">For application data update</span></span>  
4. <span data-ttu-id="5144e-180">在“名称”字段中，键入“映射以更新数据”。</span><span class="sxs-lookup"><span data-stu-id="5144e-180">In the Name field, type 'Mapping to update data'.</span></span>
    * <span data-ttu-id="5144e-181">映射以更新数据</span><span class="sxs-lookup"><span data-stu-id="5144e-181">Mapping to update data</span></span>  
5. <span data-ttu-id="5144e-182">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="5144e-182">Click Save.</span></span>
    * <span data-ttu-id="5144e-183">此映射定义如何在数据模型（其结构由所选根项“用于应用程序数据更新”指定）中收集内部统计报表的详细信息。</span><span class="sxs-lookup"><span data-stu-id="5144e-183">This mapping defines how the details of the Intrastat report are collected in the data model, the structure of which is specified by the selected root item ‘For application data update’.</span></span> <span data-ttu-id="5144e-184">这些详细信息、具有相同根项“用于应用程序数据更新”的模型映射和方向“截止目标”将用于应用程序数据更新。</span><span class="sxs-lookup"><span data-stu-id="5144e-184">These details, the model mapping with same root item ‘For application data update’, and the direction ‘To destination’ will be used for the application data update.</span></span> <span data-ttu-id="5144e-185">生成传出内部统计报表之后立即开始执行应用程序数据更新。</span><span class="sxs-lookup"><span data-stu-id="5144e-185">The application data update starts immediately after the outgoing Intrastat report is generated.</span></span> <span data-ttu-id="5144e-186">请注意，运行时可跳过应用程序数据更新，但是数据模型必须为空（包含空记录列表）。</span><span class="sxs-lookup"><span data-stu-id="5144e-186">Note that the application data update can be skipped at run-time, but the data model must be empty (containing empty record list).</span></span>   
6. <span data-ttu-id="5144e-187">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="5144e-187">Click Designer.</span></span>
    * <span data-ttu-id="5144e-188">请注意，传出内部统计报表格式添加为此模型映射的数据源。</span><span class="sxs-lookup"><span data-stu-id="5144e-188">Note that the outgoing Intrastat report format is added by default as a data source for this model mapping.</span></span>  
    * <span data-ttu-id="5144e-189">将设计的报表（表示为数据源）的元素绑定到数据模型（基于所选模型的根项过滤）的元素。</span><span class="sxs-lookup"><span data-stu-id="5144e-189">Bind elements of the designed report (presented as data source) to elements of the data model, which is filtered based on the selected model’s root item.</span></span>  
7. <span data-ttu-id="5144e-190">在树中，展开“存档标题”。</span><span class="sxs-lookup"><span data-stu-id="5144e-190">In the tree, expand 'Archive header'.</span></span>
8. <span data-ttu-id="5144e-191">在树中，展开“存档标题\存档行”。</span><span class="sxs-lookup"><span data-stu-id="5144e-191">In the tree, expand 'Archive header\Archive lines'.</span></span>
9. <span data-ttu-id="5144e-192">在树中，展开“格式”。</span><span class="sxs-lookup"><span data-stu-id="5144e-192">In the tree, expand 'format'.</span></span>
10. <span data-ttu-id="5144e-193">在树中，展开“格式\申报: XML 元素(申报)”。</span><span class="sxs-lookup"><span data-stu-id="5144e-193">In the tree, expand 'format\Declaration: XML Element(Declaration)'.</span></span>
11. <span data-ttu-id="5144e-194">在树中，展开“格式\申报: XML 元素(申报)\数据: XML 元素 1..* (数据)”。</span><span class="sxs-lookup"><span data-stu-id="5144e-194">In the tree, expand 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)'.</span></span>
12. <span data-ttu-id="5144e-195">在树中，展开“格式\申报: XML 元素(申报)\数据: XML 元素 1..* (数据)\物料: XML 元素 0..* (物料)”。</span><span class="sxs-lookup"><span data-stu-id="5144e-195">In the tree, expand 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)'.</span></span>
13. <span data-ttu-id="5144e-196">在树中，展开“格式\申报: XML 元素(申报)\数据: XML 元素 1..* (数据)\物料: XML 元素 0..* (物料)\Dim3: XML 元素 1..1 (金额)”。</span><span class="sxs-lookup"><span data-stu-id="5144e-196">In the tree, expand 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)'.</span></span>
14. <span data-ttu-id="5144e-197">在树中，展开“格式\申报: XML 元素(申报)\数据: XML 元素 1..* (数据)\物料: XML 元素 0..* (物料)\Dim4: XML 元素 1..1 (物料)”。</span><span class="sxs-lookup"><span data-stu-id="5144e-197">In the tree, expand 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)'.</span></span>
15. <span data-ttu-id="5144e-198">在树中，选择“存档标题\行数”。</span><span class="sxs-lookup"><span data-stu-id="5144e-198">In the tree, select 'Archive header\Number of lines'.</span></span>
16. <span data-ttu-id="5144e-199">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="5144e-199">Click Edit.</span></span>
17. <span data-ttu-id="5144e-200">在树中，选择“列表\COUNT”。</span><span class="sxs-lookup"><span data-stu-id="5144e-200">In the tree, select 'List\COUNT'.</span></span>
18. <span data-ttu-id="5144e-201">单击“添加”功能。</span><span class="sxs-lookup"><span data-stu-id="5144e-201">Click Add function.</span></span>
19. <span data-ttu-id="5144e-202">在树中，展开“格式”。</span><span class="sxs-lookup"><span data-stu-id="5144e-202">In the tree, expand 'format'.</span></span>
20. <span data-ttu-id="5144e-203">在树中，展开“格式\申报: XML 元素(申报)”。</span><span class="sxs-lookup"><span data-stu-id="5144e-203">In the tree, expand 'format\Declaration: XML Element(Declaration)'.</span></span>
21. <span data-ttu-id="5144e-204">在树中，展开“格式\申报: XML 元素(申报)\数据: XML 元素 1..* (数据)”。</span><span class="sxs-lookup"><span data-stu-id="5144e-204">In the tree, expand 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)'.</span></span>
22. <span data-ttu-id="5144e-205">在树中，选择“格式\申报: XML 元素(申报)\数据: XML 元素 1..* (数据)\物料: XML 元素 0..* (物料)”。</span><span class="sxs-lookup"><span data-stu-id="5144e-205">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)'.</span></span>
23. <span data-ttu-id="5144e-206">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="5144e-206">Click Add data source.</span></span>
24. <span data-ttu-id="5144e-207">在“公式”字段中，输入“COUNT(format.Declaration.Data.Item)”。</span><span class="sxs-lookup"><span data-stu-id="5144e-207">In the Formula field, enter 'COUNT(format.Declaration.Data.Item)'.</span></span>
    * <span data-ttu-id="5144e-208">COUNT(format.Declaration.Data.Item)</span><span class="sxs-lookup"><span data-stu-id="5144e-208">COUNT(format.Declaration.Data.Item)</span></span>  
25. <span data-ttu-id="5144e-209">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="5144e-209">Click Save.</span></span>
26. <span data-ttu-id="5144e-210">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="5144e-210">Close the page.</span></span>
27. <span data-ttu-id="5144e-211">在树中，选择“存档标题\文件名”。</span><span class="sxs-lookup"><span data-stu-id="5144e-211">In the tree, select 'Archive header\File name'.</span></span>
28. <span data-ttu-id="5144e-212">在树中，选择“格式\申报: XML 元素(申报)\数据: XML 元素 1..* (数据)\文件名: 物料字符串(文件名)”。</span><span class="sxs-lookup"><span data-stu-id="5144e-212">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\File name: Item String(File name)'.</span></span>
29. <span data-ttu-id="5144e-213">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="5144e-213">Click Bind.</span></span>
30. <span data-ttu-id="5144e-214">在树中，选择“格式\申报: XML 元素(申报)\数据: XML 元素 1..* (数据)\物料: XML 元素 0..* (物料)\Dim4: XML 元素 1..1 (物料)\编号: 字符串(编号)”。</span><span class="sxs-lookup"><span data-stu-id="5144e-214">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)\number: String(number)'.</span></span>
31. <span data-ttu-id="5144e-215">在树中，选择“存档标题\存档行\物料编号”。</span><span class="sxs-lookup"><span data-stu-id="5144e-215">In the tree, select 'Archive header\Archive lines\Item number'.</span></span>
32. <span data-ttu-id="5144e-216">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="5144e-216">Click Bind.</span></span>
33. <span data-ttu-id="5144e-217">在树中，选择“格式\申报: XML 元素(申报)\数据: XML 元素 1..* (数据)\物料: XML 元素 0..* (物料)\Dim3: XML 元素 1..1 (金额)\值: 实数(值)”。</span><span class="sxs-lookup"><span data-stu-id="5144e-217">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)\value: Numeric Real(value)'.</span></span>
34. <span data-ttu-id="5144e-218">在树中，选择“存档标题\存档行\金额”。</span><span class="sxs-lookup"><span data-stu-id="5144e-218">In the tree, select 'Archive header\Archive lines\Amount'.</span></span>
35. <span data-ttu-id="5144e-219">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="5144e-219">Click Bind.</span></span>
36. <span data-ttu-id="5144e-220">在树中，选择“格式\申报: XML 元素(申报)\数据: XML 元素 1..* (数据)\物料: XML 元素 0..* (物料)\商品记录标识: 物料 Int64(商品记录标识)”。</span><span class="sxs-lookup"><span data-stu-id="5144e-220">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Commodity rec id: Item Int64(Commodity rec id)'.</span></span>
37. <span data-ttu-id="5144e-221">在树中，选择“存档标题\存档行\商品记录标识”。</span><span class="sxs-lookup"><span data-stu-id="5144e-221">In the tree, select 'Archive header\Archive lines\Commodity rec id'.</span></span>
38. <span data-ttu-id="5144e-222">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="5144e-222">Click Bind.</span></span>
39. <span data-ttu-id="5144e-223">在树中，选择“存档标题\存档行”。</span><span class="sxs-lookup"><span data-stu-id="5144e-223">In the tree, select 'Archive header\Archive lines'.</span></span>
40. <span data-ttu-id="5144e-224">在树中，选择“格式\申报: XML 元素(申报)\数据: XML 元素 1..* (数据)\物料: XML 元素 0..* (物料)”。</span><span class="sxs-lookup"><span data-stu-id="5144e-224">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)'.</span></span>
41. <span data-ttu-id="5144e-225">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="5144e-225">Click Bind.</span></span>
42. <span data-ttu-id="5144e-226">在树中，选择“存档标题”。</span><span class="sxs-lookup"><span data-stu-id="5144e-226">In the tree, select 'Archive header'.</span></span>
43. <span data-ttu-id="5144e-227">在树中，选择“格式\申报: XML 元素(申报)\数据: XML 元素 1..* (数据)”。</span><span class="sxs-lookup"><span data-stu-id="5144e-227">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)'.</span></span>
44. <span data-ttu-id="5144e-228">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="5144e-228">Click Bind.</span></span>
45. <span data-ttu-id="5144e-229">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="5144e-229">Click Save.</span></span>
46. <span data-ttu-id="5144e-230">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="5144e-230">Close the page.</span></span>
47. <span data-ttu-id="5144e-231">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="5144e-231">Close the page.</span></span>
48. <span data-ttu-id="5144e-232">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="5144e-232">Close the page.</span></span>


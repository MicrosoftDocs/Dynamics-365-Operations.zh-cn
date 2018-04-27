--- 
title: "导入配置以使用应用程序数据生成单据"
description: "为了完成此过程中的步骤，您必须首先完成“ER 创建配置提供商并标记为有效”这一过程。"
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 87352293a78d6a356db49deffb930016a1bf836c
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="import-configurations-to-generate-documents-with-application-data"></a><span data-ttu-id="4707c-103">导入配置以使用应用程序数据生成单据</span><span class="sxs-lookup"><span data-stu-id="4707c-103">Import configurations to generate documents with application data</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4707c-104">为了完成此过程中的步骤，您必须首先完成“ER 创建配置提供商并标记为有效”这一过程。</span><span class="sxs-lookup"><span data-stu-id="4707c-104">To complete the steps in this procedure, you must first complete the procedure, “ER Create a configuration provider and mark it as active”.</span></span>

<span data-ttu-id="4707c-105">此过程中的步骤介绍如何设计电子申报 (ER) 配置以生成电子单据。</span><span class="sxs-lookup"><span data-stu-id="4707c-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="4707c-106">在此过程中，将导入已为示例公司 Litware 公司创建的所需 ER 配置，并用于生成电子单据。</span><span class="sxs-lookup"><span data-stu-id="4707c-106">In this procedure, you will import the required ER configurations that have been created for the sample company, Litware, Inc. and use them to generate electronic documents.</span></span> <span data-ttu-id="4707c-107">此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。</span><span class="sxs-lookup"><span data-stu-id="4707c-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="4707c-108">可使用 DEMF 数据集完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="4707c-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="4707c-109">首先，下载并保存帮助主题“使用 ER 工具生成电子单据和更新应用程序数据”(generate-electronic-documents-update-application-data/) 中列出的文件。</span><span class="sxs-lookup"><span data-stu-id="4707c-109">Before you begin, download and save the files listed in the Help topic, “Generate electronic documents and update application data with ER tool” (generate-electronic-documents-update-application-data/).</span></span> <span data-ttu-id="4707c-110">这些文件是内部统计（模型）.xml、内部统计（映射）.xml 和内部统计（格式）.xml。</span><span class="sxs-lookup"><span data-stu-id="4707c-110">The files are Intrastat (model).xml, Intrastat (mapping).xml, and Intrastat (format).xml.</span></span>

1. <span data-ttu-id="4707c-111">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="4707c-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="4707c-112">确保示例公司 Litware 公司的配置提供程序可用且标记为“有效”。</span><span class="sxs-lookup"><span data-stu-id="4707c-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="4707c-113">如果没有看到此配置提供程序，请首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="4707c-113">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
    * <span data-ttu-id="4707c-114">此过程中的步骤显示如何使用 ER 功能完成应用程序数据更新和如何生成内部统计报告。</span><span class="sxs-lookup"><span data-stu-id="4707c-114">The steps in this procedure show how to use ER capabilities to complete an application data update and how to generate an Intrastat report.</span></span> <span data-ttu-id="4707c-115">报告流程的详细信息存档到应用程序表中。</span><span class="sxs-lookup"><span data-stu-id="4707c-115">The details of the reporting process are archived in the application tables.</span></span> <span data-ttu-id="4707c-116">目前从内部统计窗体激活内部统计报告流程时，将基于现有源代码中编程的逻辑完成存档。</span><span class="sxs-lookup"><span data-stu-id="4707c-116">Currently, when the Intrastat reporting process is activated from the Intrastat form, archiving is done based on the logic programmed in the existing source code.</span></span> <span data-ttu-id="4707c-117">在此过程中，将仅使用 ER 框架配置相似但经过简化的应用程序数据逻辑。</span><span class="sxs-lookup"><span data-stu-id="4707c-117">In this procedure, you will configure a similar yet simplified logic of application data using only the ER framework.</span></span> <span data-ttu-id="4707c-118">将不更改源代码。</span><span class="sxs-lookup"><span data-stu-id="4707c-118">No changes will be made to the source code.</span></span>   

## <a name="import-er-configurations"></a><span data-ttu-id="4707c-119">导入 ER 配置</span><span class="sxs-lookup"><span data-stu-id="4707c-119">Import ER configurations</span></span>
1. <span data-ttu-id="4707c-120">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="4707c-120">Click Reporting configurations.</span></span>
2. <span data-ttu-id="4707c-121">单击“交换”。</span><span class="sxs-lookup"><span data-stu-id="4707c-121">Click Exchange.</span></span>
3. <span data-ttu-id="4707c-122">单击“从 XML 文件加载”。</span><span class="sxs-lookup"><span data-stu-id="4707c-122">Click Load from XML file.</span></span>
    * <span data-ttu-id="4707c-123">导入 ER 模型配置，其中包含一个数据模型，设计为用作生成内部统计报告的数据源。</span><span class="sxs-lookup"><span data-stu-id="4707c-123">Import the ER model configuration that contains the data model that is designed to be used as the data source for generating the Intrastat report.</span></span> <span data-ttu-id="4707c-124">然后，您将扩展此数据模型定义，以便将其用于应用程序数据更新来存档内部统计报告流程的详细信息。</span><span class="sxs-lookup"><span data-stu-id="4707c-124">Later, you will extend this data model definition to use it for an application data update to archive details of the Intrastat reporting process.</span></span>   
    * <span data-ttu-id="4707c-125">单击“浏览”并选择内部统计（模型）.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="4707c-125">Click Browse and select the Intrastat (model).xml file.</span></span>  
4. <span data-ttu-id="4707c-126">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4707c-126">Click OK.</span></span>
5. <span data-ttu-id="4707c-127">在树中，选择“内部统计(模型)”。</span><span class="sxs-lookup"><span data-stu-id="4707c-127">In the tree, select 'Intrastat (model)'.</span></span>
6. <span data-ttu-id="4707c-128">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="4707c-128">Click Designer.</span></span>
7. <span data-ttu-id="4707c-129">在树中，展开“用于传出单据”。</span><span class="sxs-lookup"><span data-stu-id="4707c-129">In the tree, expand 'For outgoing document'.</span></span>
8. <span data-ttu-id="4707c-130">在树中，展开“用于传出单据\交易记录”。</span><span class="sxs-lookup"><span data-stu-id="4707c-130">In the tree, expand 'For outgoing document\Transactions'.</span></span>
    * <span data-ttu-id="4707c-131">检查所导入数据模型的结构。</span><span class="sxs-lookup"><span data-stu-id="4707c-131">Review the structure of the imported data model.</span></span> <span data-ttu-id="4707c-132">请注意，定义根项“用于传出单据”是为了指定用于从应用程序获取数据并将其用作数据源以生成内部统计报告的数据流。</span><span class="sxs-lookup"><span data-stu-id="4707c-132">Note that the root item ‘For outgoing document’ is defined to specify the data flow for getting data from the application and using it as data source to generate the Intrastat report.</span></span> <span data-ttu-id="4707c-133">“交易记录(记录列表)”用于表示必须报告的内部统计交易记录的列表。</span><span class="sxs-lookup"><span data-stu-id="4707c-133">The ‘Transactions (Record list)’ is used to represent the list of Intrastat transactions that must be reported.</span></span> <span data-ttu-id="4707c-134">由于您将存档报告的商品代码，所以此数据流中需要单个商品代码“商品记录标识(Int64)”的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="4707c-134">Because you will archive reported commodity codes, the unique identifier of a single commodity code ‘Commodity rec id (Int64)’ is needed in this data flow.</span></span>   
9. <span data-ttu-id="4707c-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4707c-135">Close the page.</span></span>
10. <span data-ttu-id="4707c-136">单击“交换”。</span><span class="sxs-lookup"><span data-stu-id="4707c-136">Click Exchange.</span></span>
11. <span data-ttu-id="4707c-137">单击“从 XML 文件加载”。</span><span class="sxs-lookup"><span data-stu-id="4707c-137">Click Load from XML file.</span></span>
    * <span data-ttu-id="4707c-138">导入用于指定以下用途的 ER 映射配置：从应用程序获取数据，然后将其用于生成内部统计报表。</span><span class="sxs-lookup"><span data-stu-id="4707c-138">Import the ER mapping configuration that specifies the data flow for getting data from the application and then using it to generate the Intrastat report.</span></span> <span data-ttu-id="4707c-139">然后，您将扩展此模型映射定义，以便从内部统计报表获取数据，并将其用于应用程序数据更新来存档内部统计报告流程的详细信息。</span><span class="sxs-lookup"><span data-stu-id="4707c-139">Later, you will extend this model mapping definition to get data from the Intrastat report and use it for the application data update to archive details of Intrastat reporting process.</span></span>   
    * <span data-ttu-id="4707c-140">单击“浏览”并选择内部统计（映射）.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="4707c-140">Click Browse and select the Intrastat (mapping).xml file.</span></span>  
12. <span data-ttu-id="4707c-141">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4707c-141">Click OK.</span></span>
13. <span data-ttu-id="4707c-142">在树中，展开“内部统计(模型)”。</span><span class="sxs-lookup"><span data-stu-id="4707c-142">In the tree, expand 'Intrastat (model)'.</span></span>
14. <span data-ttu-id="4707c-143">在树中，选择“内部统计(模型)\内部统计(映射)”。</span><span class="sxs-lookup"><span data-stu-id="4707c-143">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
15. <span data-ttu-id="4707c-144">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="4707c-144">Click Designer.</span></span>
    * <span data-ttu-id="4707c-145">请注意，当前模型映射中的“方向”字段内包含值“截止模型”。</span><span class="sxs-lookup"><span data-stu-id="4707c-145">Note that the current model mapping contains the value ‘To model’ in the Direction field.</span></span> <span data-ttu-id="4707c-146">这意味着此模型映射已设计为从应用程序获取数据，然后将其存储到数据模型中。</span><span class="sxs-lookup"><span data-stu-id="4707c-146">This means that this model mapping has been designed for getting data from the application and storing it in the data model.</span></span>  
16. <span data-ttu-id="4707c-147">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="4707c-147">Click Designer.</span></span>
17. <span data-ttu-id="4707c-148">在树中，展开“列表”。</span><span class="sxs-lookup"><span data-stu-id="4707c-148">In the tree, expand 'List'.</span></span>
18. <span data-ttu-id="4707c-149">在树中，展开“交易记录 = 列表”。</span><span class="sxs-lookup"><span data-stu-id="4707c-149">In the tree, expand 'Transactions= List'.</span></span>
    * <span data-ttu-id="4707c-150">检查使用基于根项“用于传出单据”筛选的数据模型的模型映射的结构。</span><span class="sxs-lookup"><span data-stu-id="4707c-150">Review the structure of the model mapping that uses the data model that is filtered based on the root item, ‘For outgoing document.’</span></span> <span data-ttu-id="4707c-151">请注意，添加的数据源“列表”提供对所需应用程序的访问权限，这是来自内部统计表的记录的列表。</span><span class="sxs-lookup"><span data-stu-id="4707c-151">Note that the added data source, ‘List’ provides access to the required application data, which is the list of records from the Intrastat table.</span></span>  
19. <span data-ttu-id="4707c-152">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4707c-152">Close the page.</span></span>
20. <span data-ttu-id="4707c-153">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4707c-153">Close the page.</span></span>
21. <span data-ttu-id="4707c-154">单击“交换”。</span><span class="sxs-lookup"><span data-stu-id="4707c-154">Click Exchange.</span></span>
22. <span data-ttu-id="4707c-155">单击“从 XML 文件加载”。</span><span class="sxs-lookup"><span data-stu-id="4707c-155">Click Load from XML file.</span></span>
    * <span data-ttu-id="4707c-156">导入用于指定内部统计报表的布局和将数据填充到报表的流程的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="4707c-156">Import the ER format configuration that specifies the layout of the Intrastat report and the process of populating data to the report.</span></span> <span data-ttu-id="4707c-157">然后，您将扩展此格式定义，以便将来自内部统计报表的数据放入数据模型，并将其用于更新应用程序数据更新来存档内部统计报告流程的详细信息。</span><span class="sxs-lookup"><span data-stu-id="4707c-157">Later, you will extend this format definition to put data from the Intrastat report in to the data model and then use it to update application data to archive the details of Intrastat reporting process.</span></span>   
    * <span data-ttu-id="4707c-158">单击“浏览”并选择内部统计（格式）.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="4707c-158">Click Browse and select the Intrastat (format).xml file.</span></span>  
23. <span data-ttu-id="4707c-159">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4707c-159">Click OK.</span></span>
24. <span data-ttu-id="4707c-160">在树中，选择“内部统计(模型)\内部统计(格式)”。</span><span class="sxs-lookup"><span data-stu-id="4707c-160">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
25. <span data-ttu-id="4707c-161">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="4707c-161">Click Designer.</span></span>
26. <span data-ttu-id="4707c-162">单击”展开/折叠“。</span><span class="sxs-lookup"><span data-stu-id="4707c-162">Click Expand/collapse.</span></span>
27. <span data-ttu-id="4707c-163">在树中，选择“文件\申报”。</span><span class="sxs-lookup"><span data-stu-id="4707c-163">In the tree, select 'File\Declaration'.</span></span>
28. <span data-ttu-id="4707c-164">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="4707c-164">Click the Mapping tab.</span></span>
29. <span data-ttu-id="4707c-165">在树中，选择“文件”。</span><span class="sxs-lookup"><span data-stu-id="4707c-165">In the tree, select 'File'.</span></span>
    * <span data-ttu-id="4707c-166">检查用于生成内部统计报表的格式的结构。</span><span class="sxs-lookup"><span data-stu-id="4707c-166">Review the structure of the format used to generate the Intrastat report.</span></span> <span data-ttu-id="4707c-167">请注意，这设计为通过填充来自数据模型的数据生成 XML 文件，该文件基于根项“用于传出单据”。</span><span class="sxs-lookup"><span data-stu-id="4707c-167">Note that it is designed to generate an XML file by populating data from the data model, which is based on the root item ‘For outgoing document’.</span></span> <span data-ttu-id="4707c-168">验证用户对话框窗体（为其使用了“fn”数据源）中是否定义了所生成文件的名称。</span><span class="sxs-lookup"><span data-stu-id="4707c-168">Verify that the name for generated file is defined on the user dialog form (‘fn’ data source is used for that).</span></span>   
30. <span data-ttu-id="4707c-169">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4707c-169">Close the page.</span></span>



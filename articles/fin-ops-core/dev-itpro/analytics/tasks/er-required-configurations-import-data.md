---
title: ER 创建从外部文件导入数据所需配置
description: 本主题介绍如何设计电子报告配置，以将数据从外部文件导入到 Microsoft Dynamics 365 Finance 应用。
author: NickSelin
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERSolutionCreateDropDialog, EROperationDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula, Tax1099Summary, VendSettlementTax1099
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2194bdc918035bf3aebe9b90ddc8a30f9937bb0c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751454"
---
# <a name="er-create-required-configurations-to-import-data-from-an-external-file"></a><span data-ttu-id="4d226-103">ER 创建从外部文件导入数据所需配置</span><span class="sxs-lookup"><span data-stu-id="4d226-103">ER Create required configurations to import data from an external file</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4d226-104">以下步骤说明属于系统管理员或电子报表开发人员的用户如何设计电子报表 (ER) 配置，以便将数据从外部文件导入应用程序中。</span><span class="sxs-lookup"><span data-stu-id="4d226-104">The following steps explain how a user in the System administrator or Electronic reporting developer role can design Electronic reporting (ER) configurations to import data in to the application from an external file.</span></span> <span data-ttu-id="4d226-105">在此示例中，将为示例公司 Litware 公司创建所需 ER 配置。若要完成这些步骤，您必须首先完成任务指南“ER 创建一个配置提供程序，并标记其为当前运行的”中的步骤。</span><span class="sxs-lookup"><span data-stu-id="4d226-105">In this example, you will create the required ER configurations for the sample company, Litware, Inc. To complete these steps, you must first complete the steps in the Task guide, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="4d226-106">可使用 USMF 数据集完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="4d226-106">These steps can be completed using the USMF data set.</span></span> <span data-ttu-id="4d226-107">还必须下载并在本地保存以下文件：</span><span class="sxs-lookup"><span data-stu-id="4d226-107">You must also download and save the following files locally:</span></span> 

| <span data-ttu-id="4d226-108">内容描述</span><span class="sxs-lookup"><span data-stu-id="4d226-108">Content description</span></span>                       | <span data-ttu-id="4d226-109">文件名</span><span class="sxs-lookup"><span data-stu-id="4d226-109">File name</span></span>                                     |
|-------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="4d226-110">ER 数据模型配置 - 1099</span><span class="sxs-lookup"><span data-stu-id="4d226-110">ER data model configuration - 1099</span></span> | [<span data-ttu-id="4d226-111">1099model,xml</span><span class="sxs-lookup"><span data-stu-id="4d226-111">1099model,xml</span></span>](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)                  |
| <span data-ttu-id="4d226-112">ER 格式配置 - 1099</span><span class="sxs-lookup"><span data-stu-id="4d226-112">ER format configuration - 1099</span></span>    | [<span data-ttu-id="4d226-113">1099format.xml</span><span class="sxs-lookup"><span data-stu-id="4d226-113">1099format.xml</span></span>](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)                  |
| <span data-ttu-id="4d226-114">XML 格式的传入文档示例</span><span class="sxs-lookup"><span data-stu-id="4d226-114">Sample of the incoming document in XML format</span></span>                          | [<span data-ttu-id="4d226-115">1099entries.xml</span><span class="sxs-lookup"><span data-stu-id="4d226-115">1099entries.xml</span></span>](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)        |
| <span data-ttu-id="4d226-116">管理传入文档数据的工作簿的示例</span><span class="sxs-lookup"><span data-stu-id="4d226-116">Sample of the workbook to manage data of incoming document</span></span>                          | [<span data-ttu-id="4d226-117">1099entries.xlsx</span><span class="sxs-lookup"><span data-stu-id="4d226-117">1099entries.xlsx</span></span>](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx) |

<span data-ttu-id="4d226-118">ER 让用户可以配置将外部数据文件以 .XML 或 .TXT 格式导入表的过程。</span><span class="sxs-lookup"><span data-stu-id="4d226-118">ER offers business users the ability to configure the process of importing external data files to tables in either .XML or .TXT format.</span></span> <span data-ttu-id="4d226-119">首先，必须设计抽象数据模型和 ER 数据模型配置来表示要导入的数据。</span><span class="sxs-lookup"><span data-stu-id="4d226-119">First, an abstract data model and an ER data model configuration must be designed to represent the data that you are importing.</span></span> <span data-ttu-id="4d226-120">接下来，需要定义要导入的文件的结构和将用于把数据从文件移植到抽象数据模型的方法。</span><span class="sxs-lookup"><span data-stu-id="4d226-120">Next, you need to define the structure of the file that you are importing and the method that you will use to port the data from the file to the abstract data model.</span></span> <span data-ttu-id="4d226-121">必须为该抽象数据模型创建映射到设计的数据模型的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="4d226-121">The ER format configuration that maps to the designed data model must be created for that abstract data model.</span></span> <span data-ttu-id="4d226-122">然后，必须使用映射扩展数据模型，该映射介绍导入的数据如何作为抽象数据模型长期存在和如何用于更新表。</span><span class="sxs-lookup"><span data-stu-id="4d226-122">Then, the data model configuration must be extended with a mapping that describes how the imported data is persisted as abstract data model data and how it is used to update tables.</span></span>  <span data-ttu-id="4d226-123">必须为 ER 数据模型配置追加一个新模型映射，该映射介绍如何将数据模型绑定到应用程序的目标。</span><span class="sxs-lookup"><span data-stu-id="4d226-123">The ER data model configuration must be appended with a new model mapping that describes the binding of the data model to the application's destinations.</span></span>  

<span data-ttu-id="4d226-124">以下方案演示 ER 数据导入功能。</span><span class="sxs-lookup"><span data-stu-id="4d226-124">The following scenario shows the ER data import capabilities.</span></span> <span data-ttu-id="4d226-125">其中包括在外部跟踪，然后导入，以便以后在 1099 的供应商结算中报告的供应商交易。</span><span class="sxs-lookup"><span data-stu-id="4d226-125">This includes vendor transactions that are tracked externally and then imported to be reported later in Vendor's settlement for 1099's.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="4d226-126">添加新 ER 模型配置</span><span class="sxs-lookup"><span data-stu-id="4d226-126">Add a new ER model configuration</span></span>
1. <span data-ttu-id="4d226-127">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="4d226-127">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="4d226-128">验证示例公司“Litware 公司”的配置提供程序</span><span class="sxs-lookup"><span data-stu-id="4d226-128">Verify that the configuration provider for sample company 'Litware, Inc.'</span></span> <span data-ttu-id="4d226-129">可用且标记为有效。</span><span class="sxs-lookup"><span data-stu-id="4d226-129">is available and marked as active.</span></span> <span data-ttu-id="4d226-130">如果没有看到此配置提供程序，您必须首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="4d226-130">If you don't see this configuration provider, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   

2. <span data-ttu-id="4d226-131">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="4d226-131">Click Reporting configurations.</span></span>

    <span data-ttu-id="4d226-132">加载前面下载的 1099model.xml 文件，而不是创建新模型。</span><span class="sxs-lookup"><span data-stu-id="4d226-132">Instead of creating of a new model to support data import, load the file, 1099model.xml, that you previously downloaded.</span></span> <span data-ttu-id="4d226-133">此文件中包含供应商的交易的自定义数据模型。</span><span class="sxs-lookup"><span data-stu-id="4d226-133">This file contains the custom data model of vendors' transactions.</span></span> <span data-ttu-id="4d226-134">此数据模型映射到 AOT 数据实体中的数据组件。</span><span class="sxs-lookup"><span data-stu-id="4d226-134">This data model is mapped to the data components that are in the AOT data entity.</span></span>   

3. <span data-ttu-id="4d226-135">单击“交换”。</span><span class="sxs-lookup"><span data-stu-id="4d226-135">Click Exchange.</span></span>
4. <span data-ttu-id="4d226-136">单击“从 XML 文件加载”。</span><span class="sxs-lookup"><span data-stu-id="4d226-136">Click Load from XML file.</span></span>

    <span data-ttu-id="4d226-137">单击“浏览”并导航到前面下载的 1099model.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="4d226-137">Click Browse and navigate to the 1099model.xml file that you previously downloaded.</span></span>  

5. <span data-ttu-id="4d226-138">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4d226-138">Click OK.</span></span>
6. <span data-ttu-id="4d226-139">在树结构中，选择“1099 付款模型”。</span><span class="sxs-lookup"><span data-stu-id="4d226-139">In the tree, select '1099 Payments model'.</span></span>

## <a name="review-data-model-settings"></a><span data-ttu-id="4d226-140">检查数据模型设置</span><span class="sxs-lookup"><span data-stu-id="4d226-140">Review data model settings</span></span>
1. <span data-ttu-id="4d226-141">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="4d226-141">Click Designer.</span></span>

    <span data-ttu-id="4d226-142">此模型设计为从业务角度表示供应商的交易，并且这些交易独立于实施。</span><span class="sxs-lookup"><span data-stu-id="4d226-142">This model is designed to represent vendors' transactions from the business standpoint and are separate from the implementation.</span></span>   

2. <span data-ttu-id="4d226-143">在树结构中，展开“1099-MISC”。</span><span class="sxs-lookup"><span data-stu-id="4d226-143">In the tree, expand '1099-MISC'.</span></span>
3. <span data-ttu-id="4d226-144">在树结构中，选择“1099-MISC\交易”。</span><span class="sxs-lookup"><span data-stu-id="4d226-144">In the tree, select '1099-MISC\Transactions'.</span></span>
4. <span data-ttu-id="4d226-145">在树结构中，展开“1099-MISC\交易”。</span><span class="sxs-lookup"><span data-stu-id="4d226-145">In the tree, expand '1099-MISC\Transactions'.</span></span>

    <span data-ttu-id="4d226-146">此模型的“交易”元素表示单笔交易。</span><span class="sxs-lookup"><span data-stu-id="4d226-146">The Transactions element of this model represents individual transactions.</span></span> <span data-ttu-id="4d226-147">子元素则用于指定所需的详细信息，如每笔交易的供应商帐户和交易日期。</span><span class="sxs-lookup"><span data-stu-id="4d226-147">The child elements are used to specify required details, such as vendor account and transaction date, for each transaction.</span></span>   

5. <span data-ttu-id="4d226-148">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4d226-148">Close the page.</span></span>

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a><span data-ttu-id="4d226-149">添加支持导入数据的新 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="4d226-149">Add a new ER format configuration that supports data import</span></span>
<span data-ttu-id="4d226-150">此子任务中的步骤演示可如何创建新格式配置来管理数据从外部文件的导入。</span><span class="sxs-lookup"><span data-stu-id="4d226-150">The steps in this subtask show you how a new format configuration can be created to manage data import from external files.</span></span>   
1. <span data-ttu-id="4d226-151">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="4d226-151">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="4d226-152">在“新建”字段中，输入“基于数据模型 1099 付款模型的格式”。</span><span class="sxs-lookup"><span data-stu-id="4d226-152">In the New field, enter 'Format based on data model 1099 Payments model'.</span></span>
3. <span data-ttu-id="4d226-153">在“支持数据导入”字段中选择"是"。</span><span class="sxs-lookup"><span data-stu-id="4d226-153">Select Yes in the Supports data import field.</span></span>
4. <span data-ttu-id="4d226-154">按 ESC 键关闭此页。</span><span class="sxs-lookup"><span data-stu-id="4d226-154">Press ESC key to close this page.</span></span>

    <span data-ttu-id="4d226-155">加载前面下载的文件 1099format.xml 文件，而不是创建新格式来支持数据导入。</span><span class="sxs-lookup"><span data-stu-id="4d226-155">Instead of creating a new format to support data import, load the 1099format.xml file that you previously downloaded.</span></span> <span data-ttu-id="4d226-156">此文件中包含为要导入的文件定义的结构和该结构到供应商交易的自定义数据模型的映射。</span><span class="sxs-lookup"><span data-stu-id="4d226-156">This file contains the defined structure of the file you are importing and the mapping of the structure to the custom data model of vendors' transactions.</span></span>   
5. <span data-ttu-id="4d226-157">单击“交换”。</span><span class="sxs-lookup"><span data-stu-id="4d226-157">Click Exchange.</span></span>
6. <span data-ttu-id="4d226-158">单击“从 XML 文件加载”。</span><span class="sxs-lookup"><span data-stu-id="4d226-158">Click Load from XML file.</span></span>
    <span data-ttu-id="4d226-159">单击“浏览”并导航到前面下载的 1099format.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="4d226-159">Click Browse and navigate to the 1099format.xml file that you previously downloaded.</span></span>  
7. <span data-ttu-id="4d226-160">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4d226-160">Click OK.</span></span>
8. <span data-ttu-id="4d226-161">在树结构中，展开“1099 付款模型”。</span><span class="sxs-lookup"><span data-stu-id="4d226-161">In the tree, expand '1099 Payments model'.</span></span>
9. <span data-ttu-id="4d226-162">在树结构中，选择“”1099 付款模型\用于导入供应商的交易的格式“。</span><span class="sxs-lookup"><span data-stu-id="4d226-162">In the tree, select '1099 Payments model\Format for importing vendors' transactions'.</span></span>

## <a name="review-format-settings"></a><span data-ttu-id="4d226-163">检查格式设置</span><span class="sxs-lookup"><span data-stu-id="4d226-163">Review format settings</span></span>
1. <span data-ttu-id="4d226-164">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="4d226-164">Click Designer.</span></span>
2. <span data-ttu-id="4d226-165">打开”显示详细信息“。</span><span class="sxs-lookup"><span data-stu-id="4d226-165">Toggle 'Show details' on.</span></span>
3. <span data-ttu-id="4d226-166">单击”展开/折叠“。</span><span class="sxs-lookup"><span data-stu-id="4d226-166">Click Expand/collapse.</span></span>
4. <span data-ttu-id="4d226-167">单击”展开/折叠“。</span><span class="sxs-lookup"><span data-stu-id="4d226-167">Click Expand/collapse.</span></span>

    <span data-ttu-id="4d226-168">设计的格式表示外部文件的预期结构。</span><span class="sxs-lookup"><span data-stu-id="4d226-168">The designed format represents the expected structure of the external file.</span></span> <span data-ttu-id="4d226-169">此文件必须为 XML 格式且具有结算根元素。</span><span class="sxs-lookup"><span data-stu-id="4d226-169">This file must be in XML format and have the settlement root element.</span></span> <span data-ttu-id="4d226-170">每个供应商的交易通过交易元素表示，交易元素定义为拥有零对多多重性。</span><span class="sxs-lookup"><span data-stu-id="4d226-170">Each vendor's transaction is represented by the transaction element that is defined as having zero-to-many multiplicity.</span></span> <span data-ttu-id="4d226-171">这意味着传入的文件可能包含从零到多笔交易的任何位置。</span><span class="sxs-lookup"><span data-stu-id="4d226-171">This means that the incoming file may contain anywhere from zero to multiple transactions.</span></span> <span data-ttu-id="4d226-172">“交易”元素的嵌套元素表示单笔交易的属性。</span><span class="sxs-lookup"><span data-stu-id="4d226-172">Nested elements of the 'transaction' element represent a single transaction's attributes.</span></span> <span data-ttu-id="4d226-173">请注意，除国家/地区外的所有属性都标记为必需项，也就是说导入文件中必须包含这些属性。</span><span class="sxs-lookup"><span data-stu-id="4d226-173">Note that all attributes, except country, are marked as mandatory, meaning that it is required to have them in the importing file.</span></span>   

## <a name="review-the-settings-of-the-format-mapping-to-the-data-model"></a><span data-ttu-id="4d226-174">检查格式到数据模型的映射的设置</span><span class="sxs-lookup"><span data-stu-id="4d226-174">Review the settings of the format mapping to the data model</span></span>
1. <span data-ttu-id="4d226-175">单击”将格式映射到模型“。</span><span class="sxs-lookup"><span data-stu-id="4d226-175">Click Map format to model.</span></span>

    <span data-ttu-id="4d226-176">“对于导入供应商的交易”这一映射中包含从传入的 XML 文件到所选自定义数据模型部分的数据传输规则，该规则通过选择 1099-MISC 定义来定义。</span><span class="sxs-lookup"><span data-stu-id="4d226-176">The mapping 'For importing vendors' transactions' contains the data transfer rules from the incoming XML file to the selected part of the custom data model, which is defined by selecting the1099-MISC definition.</span></span>  

2. <span data-ttu-id="4d226-177">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="4d226-177">Click Designer.</span></span>
3. <span data-ttu-id="4d226-178">打开”显示详细信息“。</span><span class="sxs-lookup"><span data-stu-id="4d226-178">Toggle 'Show details' on.</span></span>
4. <span data-ttu-id="4d226-179">在树形图中，展开“格式: 记录”。</span><span class="sxs-lookup"><span data-stu-id="4d226-179">In the tree, expand 'format: Record'.</span></span>
5. <span data-ttu-id="4d226-180">在树结构中，选择“格式: 记录”。</span><span class="sxs-lookup"><span data-stu-id="4d226-180">In the tree, select 'format: Record'.</span></span>

    <span data-ttu-id="4d226-181">请注意，设计的格式在此处表示为数据源组件。</span><span class="sxs-lookup"><span data-stu-id="4d226-181">Note that the designed format is presented here as a data source component.</span></span>  

6. <span data-ttu-id="4d226-182">在树中，展开 `format: Record\*settlement: XML Element 1..1 (settlement): Record`。</span><span class="sxs-lookup"><span data-stu-id="4d226-182">In the tree, expand `format: Record\*settlement: XML Element 1..1 (settlement): Record`.</span></span>
7. <span data-ttu-id="4d226-183">在树中，展开 `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list`。</span><span class="sxs-lookup"><span data-stu-id="4d226-183">In the tree, expand `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list`.</span></span>
8. <span data-ttu-id="4d226-184">在树中，展开 `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record`。</span><span class="sxs-lookup"><span data-stu-id="4d226-184">In the tree, expand `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record`.</span></span>
9. <span data-ttu-id="4d226-185">在树中，展开 `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\country: XML Element 0..1 (country): Record`。</span><span class="sxs-lookup"><span data-stu-id="4d226-185">In the tree, expand `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\country: XML Element 0..1 (country): Record`.</span></span>
10. <span data-ttu-id="4d226-186">在树中，选择 `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record`。</span><span class="sxs-lookup"><span data-stu-id="4d226-186">In the tree, select `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record`.</span></span>

    <span data-ttu-id="4d226-187">请注意，在预定义的“格式”数据源组件中，必需格式元素和可选格式元素的表示形式不同。</span><span class="sxs-lookup"><span data-stu-id="4d226-187">Note that the presentation of mandatory and optional format elements is different in the predefined 'format' data source component.</span></span>  
11. <span data-ttu-id="4d226-188">在树结构中，展开“交易: 记录列表= format.settlement.'$enumerated'”。</span><span class="sxs-lookup"><span data-stu-id="4d226-188">In the tree, expand 'Transactions: Record list= format.settlement.'$enumerated''.</span></span>

    <span data-ttu-id="4d226-189">请注意，用于定义所导入文件的结构的格式的元素绑定到自定义数据模型的元素。</span><span class="sxs-lookup"><span data-stu-id="4d226-189">Note that the elements of the format that defines the structure of the imported file are bound to the elements of the custom data model.</span></span> <span data-ttu-id="4d226-190">所导入 XML 文件的内容将在运行时在现有数据模型中根据这些绑定排序。</span><span class="sxs-lookup"><span data-stu-id="4d226-190">Based on these bindings, the content of the imported XML file will be stored at run-time in the existing data model.</span></span> <span data-ttu-id="4d226-191">请注意国家/地区元素的绑定。</span><span class="sxs-lookup"><span data-stu-id="4d226-191">Pay attention to the binding of the country element.</span></span> <span data-ttu-id="4d226-192">对于无此类元素的传入文件中的任何交易元素，将在数据模型中填充默认国家/地区代码“USA”。</span><span class="sxs-lookup"><span data-stu-id="4d226-192">For any transaction element in the incoming file that has no such element, the default country code 'USA' will be populated in the data model.</span></span>  

12. <span data-ttu-id="4d226-193">单击“验证”选项卡。</span><span class="sxs-lookup"><span data-stu-id="4d226-193">Click the Validations tab.</span></span>

    <span data-ttu-id="4d226-194">此格式映射中可以包含用户定义的逻辑，用于从业务角度验证导入的数据的精确性。</span><span class="sxs-lookup"><span data-stu-id="4d226-194">This format mapping may contain user-defined logic to validate the accuracy of the imported data from a business standpoint.</span></span> <span data-ttu-id="4d226-195">例如，将根据此设置为所导入文件中未定义国家/地区代码的任何交易在信息日志中生成一条警告消息，通知用户该情况，并指示交易的序列号。</span><span class="sxs-lookup"><span data-stu-id="4d226-195">For example, based on the setting, for any transaction in the importing file without a defined country code, a warning message will be generated in the Infolog informing the user about the case and indicating the transaction's sequence number.</span></span>  

13. <span data-ttu-id="4d226-196">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4d226-196">Close the page.</span></span>

## <a name="run-the-format-mapping-to-the-data-model"></a><span data-ttu-id="4d226-197">运行格式到数据模型的映射</span><span class="sxs-lookup"><span data-stu-id="4d226-197">Run the format mapping to the data model</span></span>
<span data-ttu-id="4d226-198">请为测试目的执行此格式映射。</span><span class="sxs-lookup"><span data-stu-id="4d226-198">Execute this format mapping for testing purposes.</span></span> <span data-ttu-id="4d226-199">使用前面下载的 1099entries.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="4d226-199">Use the file 1099entries.xml that you previously downloaded.</span></span> <span data-ttu-id="4d226-200">可以从用于管理供应商交易的 1099entries.xlsx 工作簿导出此文件。</span><span class="sxs-lookup"><span data-stu-id="4d226-200">You can export this file from the 1099entries.xlsx workbook that is used to manage vendor transactions.</span></span> <span data-ttu-id="4d226-201">生成的输出将从所选 XML 文件导入，并在实际导入时填充自定义数据模型。</span><span class="sxs-lookup"><span data-stu-id="4d226-201">The generated output will be imported from the selected XML file and populate the custom data model at real import.</span></span>  

1. <span data-ttu-id="4d226-202">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="4d226-202">Click Run.</span></span>

    <span data-ttu-id="4d226-203">单击“浏览”并导航到前面下载的 1099entries.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="4d226-203">Click Browse and navigate to the 1099entries.xml file that you previously downloaded.</span></span>  

2. <span data-ttu-id="4d226-204">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4d226-204">Click OK.</span></span>

    <span data-ttu-id="4d226-205">请注意关于导入的文件中某笔交易缺少国家/地区代码的警告消息。</span><span class="sxs-lookup"><span data-stu-id="4d226-205">Note the warning message about a missing country code for a transaction in the imported file.</span></span>  
    
    <span data-ttu-id="4d226-206">检查 XML 格式的输出，该输出表示已从所选文件导入并移植到数据模型的数据。</span><span class="sxs-lookup"><span data-stu-id="4d226-206">Review the output in XML format, which represents the data that has been imported from the selected file and ported to the data model.</span></span>   

3. <span data-ttu-id="4d226-207">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4d226-207">Close the page.</span></span>
4. <span data-ttu-id="4d226-208">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4d226-208">Close the page.</span></span>

## <a name="review-the-settings-for-the-model-mapping-to-the-destinations"></a><span data-ttu-id="4d226-209">检查模型到目标的映射的设置</span><span class="sxs-lookup"><span data-stu-id="4d226-209">Review the settings for the model mapping to the destinations</span></span>
1. <span data-ttu-id="4d226-210">在树结构中，选择“1099 付款模型”。</span><span class="sxs-lookup"><span data-stu-id="4d226-210">In the tree, select '1099 Payments model'.</span></span>
2. <span data-ttu-id="4d226-211">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="4d226-211">Click Designer.</span></span>
3. <span data-ttu-id="4d226-212">单击“映射模型到数据源”。</span><span class="sxs-lookup"><span data-stu-id="4d226-212">Click Map model to datasource.</span></span>

    <span data-ttu-id="4d226-213">已为“对于 1099 手动交易导入”这一映射定义了“截止目标”方向类型。</span><span class="sxs-lookup"><span data-stu-id="4d226-213">The mapping For 1099 manual transactions import has been defined with the To destination direction type.</span></span> <span data-ttu-id="4d226-214">这意味着输入它是为了支持数据导入，并且其中包含有关导入并以抽象数据模型数据的形式长期存在的外部文件如何用于填充应用程序中的表的规则的设置。</span><span class="sxs-lookup"><span data-stu-id="4d226-214">This means that it has been entered to support data import and contains the setting of rules defining how the imported external file and persisted as abstract data model data is used to update tables in the application.</span></span>  

4. <span data-ttu-id="4d226-215">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="4d226-215">Click Designer.</span></span>
5. <span data-ttu-id="4d226-216">在树结构中，展开“模型: 数据模型 1099 付款模型”。</span><span class="sxs-lookup"><span data-stu-id="4d226-216">In the tree, expand 'model: Data model 1099 Payments model'.</span></span>
6. <span data-ttu-id="4d226-217">在树结构中，展开“模型: 数据模型 1099 付款模型\交易: 记录列表”。</span><span class="sxs-lookup"><span data-stu-id="4d226-217">In the tree, expand 'model: Data model 1099 Payments model\Transactions: Record list'.</span></span>

    <span data-ttu-id="4d226-218">请注意，设计的模型在此处表示为数据源元素。</span><span class="sxs-lookup"><span data-stu-id="4d226-218">Note that the designed model is presented here as a data source element.</span></span> <span data-ttu-id="4d226-219">在运行时，其中将包含从外部文件导入的数据。</span><span class="sxs-lookup"><span data-stu-id="4d226-219">At runtime, it will contain the data that is imported from the external file.</span></span> <span data-ttu-id="4d226-220">添加了若干表来充当数据源元素，以便确保导入的数据与当前应用程序的数据一致，包括导入交易供应商帐户是否在系统中可用，导入国家/地区和省/直辖市/自治州代码的组合是否存在等。</span><span class="sxs-lookup"><span data-stu-id="4d226-220">Several tables were added as data source elements to ensure that the imported data is compliant with the data of the current application, including whether the importing transaction vendor account is available in the system, whether the combination of the importing country and state codes exists, etc.</span></span>  

7. <span data-ttu-id="4d226-221">在树结构中，选择“模型: 数据模型 1099 付款模型\交易: 记录列表\$failed: 计算字段 = IF(OR(ISEMPTY(model.Transactions.'$refs'.vendor), ISEMPTY(model.Transactions.'$refs'.vendor1099), ISEMPTY(model.Transactions.'$refs'.box1099), ISEMPTY(model.Transactions.'$refs'.country), ISEMPTY(model.Transactions.'$refs'.state), ISEMPTY(model.Transactions.'$refs'.location)), true, false): Boolean”。</span><span class="sxs-lookup"><span data-stu-id="4d226-221">In the tree, select 'model: Data model 1099 Payments model\Transactions: Record list\$failed: Calculated field = IF(OR(ISEMPTY(model.Transactions.'$refs'.vendor), ISEMPTY(model.Transactions.'$refs'.vendor1099), ISEMPTY(model.Transactions.'$refs'.box1099), ISEMPTY(model.Transactions.'$refs'.country), ISEMPTY(model.Transactions.'$refs'.state), ISEMPTY(model.Transactions.'$refs'.location)), true, false): Boolean'.</span></span>
8. <span data-ttu-id="4d226-222">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="4d226-222">Click Edit.</span></span>
9. <span data-ttu-id="4d226-223">单击“编辑公式”。</span><span class="sxs-lookup"><span data-stu-id="4d226-223">Click Edit formula.</span></span>

    <span data-ttu-id="4d226-224">当导入的单笔交易至少一项验证失败，数据源属性“$failed”将把该交易标记为失败。</span><span class="sxs-lookup"><span data-stu-id="4d226-224">When at least one validation fails for a single imported transaction, this transaction will be marked as failed by the data source attribute '$failed'.</span></span>  

10. <span data-ttu-id="4d226-225">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4d226-225">Close the page.</span></span>
11. <span data-ttu-id="4d226-226">单击“取消”。</span><span class="sxs-lookup"><span data-stu-id="4d226-226">Click Cancel.</span></span>
12. <span data-ttu-id="4d226-227">在树结构中，选择“tax1099trans: 表 'VendSettlementTax1099' 记录= model.Validated“。</span><span class="sxs-lookup"><span data-stu-id="4d226-227">In the tree, select 'tax1099trans: Table 'VendSettlementTax1099' records= model.Validated'.</span></span>
13. <span data-ttu-id="4d226-228">单击”编辑目标“。</span><span class="sxs-lookup"><span data-stu-id="4d226-228">Click Edit destination.</span></span>

    <span data-ttu-id="4d226-229">添加此 ER 目标是为了指定导入的数据将如何更新应用程序表。</span><span class="sxs-lookup"><span data-stu-id="4d226-229">This ER destination was added to specify how the imported data will update the application tables.</span></span> <span data-ttu-id="4d226-230">在此案例中，已选择了数据表 VendSettlementTax1099。</span><span class="sxs-lookup"><span data-stu-id="4d226-230">In this case, the data table VendSettlementTax1099 has been selected.</span></span> <span data-ttu-id="4d226-231">由于已选择了记录操作插入，所以将把导入的交易插入到表 VendSettlementTax1099 中。</span><span class="sxs-lookup"><span data-stu-id="4d226-231">Because the record action Insert has been selected, the imported transactions will be inserted in the table VendSettlementTax1099.</span></span> <span data-ttu-id="4d226-232">请注意，一个模型映射中可以包含多个目标。</span><span class="sxs-lookup"><span data-stu-id="4d226-232">Note that a single model mapping may contain several destinations.</span></span> <span data-ttu-id="4d226-233">这意味着导入的数据可用于一次更新应用程序的多个表。</span><span class="sxs-lookup"><span data-stu-id="4d226-233">This means that the imported data can be used to update multiple application's tables at once.</span></span> <span data-ttu-id="4d226-234">表、视图和数据实体可用作 ER 目标。</span><span class="sxs-lookup"><span data-stu-id="4d226-234">Tables, views, and data entities can be used as ER destinations.</span></span>   

    <span data-ttu-id="4d226-235">如果将从应用程序中专门为此操作设计的某个点（如按钮或菜单项）调用映射，应将 ER 目标标记为集成点。</span><span class="sxs-lookup"><span data-stu-id="4d226-235">If the mapping will be called from a point in the application (such as button or menu item) that was specifically designed for this action, the ER destination should be marked as the integration point.</span></span> <span data-ttu-id="4d226-236">在此示例中，为 ERTableDestination#VendSettlementTax1099 点。</span><span class="sxs-lookup"><span data-stu-id="4d226-236">In this example this is the ERTableDestination#VendSettlementTax1099 point.</span></span>  

14. <span data-ttu-id="4d226-237">单击“取消”。</span><span class="sxs-lookup"><span data-stu-id="4d226-237">Click Cancel.</span></span>
15. <span data-ttu-id="4d226-238">单击“全部显示”。</span><span class="sxs-lookup"><span data-stu-id="4d226-238">Click Show all.</span></span>
16. <span data-ttu-id="4d226-239">单击”只显示映射的“。</span><span class="sxs-lookup"><span data-stu-id="4d226-239">Click Show mapped only.</span></span>
17. <span data-ttu-id="4d226-240">在树结构中，展开“tax1099trans: 表 'VendSettlementTax1099' 记录= model.Validated“。</span><span class="sxs-lookup"><span data-stu-id="4d226-240">In the tree, expand 'tax1099trans: Table 'VendSettlementTax1099' records= model.Validated'.</span></span>

    <span data-ttu-id="4d226-241">请注意，仅包含已验证交易的数据源元素绑定到创建的目标。</span><span class="sxs-lookup"><span data-stu-id="4d226-241">Note that the data source element that contains the only validated transactions is bound to the created destination.</span></span> <span data-ttu-id="4d226-242">您可以筛选导入的交易，以便跳过与应用程序的数据不兼容的交易。</span><span class="sxs-lookup"><span data-stu-id="4d226-242">You can filter the imported transactions to skip the ones that are incompatible with the applications' data.</span></span>  

18. <span data-ttu-id="4d226-243">在树结构中，选择“failed: 表 'VendSettlementTax1099Entity' 记录 = model.Failed“。</span><span class="sxs-lookup"><span data-stu-id="4d226-243">In the tree, select 'failed: Table 'VendSettlementTax1099Entity' records= model.Failed'.</span></span>
19. <span data-ttu-id="4d226-244">单击“验证”选项卡。</span><span class="sxs-lookup"><span data-stu-id="4d226-244">Click the Validations tab.</span></span>

    <span data-ttu-id="4d226-245">此模型映射中可以包含用户定义的逻辑，用于验证从现有应用程序数据导入的数据的正确性。</span><span class="sxs-lookup"><span data-stu-id="4d226-245">This model mapping may contain user-defined logic to validate the correctness of the imported data from the existing application data.</span></span> <span data-ttu-id="4d226-246">例如，将根据现有设置为位于所导入文件中但在系统中不存在的任何交易生成一条警告消息，通知用户并指示不正确的供应商帐户代码。</span><span class="sxs-lookup"><span data-stu-id="4d226-246">For example, based on the present setting, for any transaction in the imported file with a vendor account that is not in the system, a warning message will be generated informing the user and indicating the incorrect vendor account code.</span></span>  

    <span data-ttu-id="4d226-247">请注意，“验证后操作”选项可用于各项验证后，以指定是继续还是停止导入过程，以及可以保留还是回滚已执行的插入/更新。</span><span class="sxs-lookup"><span data-stu-id="4d226-247">Note that the Post validation action option can be used for each validation, to specify whether the import process must be continued or stopped, as well as if the already performed inserts/updates can be kept or rolled back.</span></span>  

20. <span data-ttu-id="4d226-248">单击”只显示映射的“。</span><span class="sxs-lookup"><span data-stu-id="4d226-248">Click Show mapped only.</span></span>
21. <span data-ttu-id="4d226-249">单击“全部显示”。</span><span class="sxs-lookup"><span data-stu-id="4d226-249">Click Show all.</span></span>
22. <span data-ttu-id="4d226-250">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4d226-250">Close the page.</span></span>

    <span data-ttu-id="4d226-251">执行此模型映射以测试设计的格式和模型映射。</span><span class="sxs-lookup"><span data-stu-id="4d226-251">Execute this model mapping to test the designed format and model mappings.</span></span> <span data-ttu-id="4d226-252">使用文件 1099entries.xml。</span><span class="sxs-lookup"><span data-stu-id="4d226-252">Use the file 1099entries.xml.</span></span> <span data-ttu-id="4d226-253">将把所选文件中的数据导入系统。</span><span class="sxs-lookup"><span data-stu-id="4d226-253">The data from the selected file will be imported in to the system.</span></span>  

23. <span data-ttu-id="4d226-254">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="4d226-254">Click Run.</span></span>

    <span data-ttu-id="4d226-255">请注意，此对话框中包含有关必须用于解析所导入文件，然后将数据移植到数据模型的格式映射的更多问题。</span><span class="sxs-lookup"><span data-stu-id="4d226-255">Note that the dialog box contains no additional questions about the format mapping that must be used to parse the imported file and then port the data to the data model.</span></span> <span data-ttu-id="4d226-256">这是因为现在只有一种格式在使用此模型，这种格式标记为已设计是为了支持数据导入。</span><span class="sxs-lookup"><span data-stu-id="4d226-256">This is because there is currently only one format that uses this model, which is marked as designed to support data import.</span></span>  
    
    <span data-ttu-id="4d226-257">定义凭证 ID 以区分导入的交易和可能已手动输入或导入的其他交易。</span><span class="sxs-lookup"><span data-stu-id="4d226-257">Define the voucher ID to differentiate the imported transactions from other transactions that may already have been entered manually or imported.</span></span>  

24. <span data-ttu-id="4d226-258">在“输入凭证 ID”字段中，键入“IMPORT-001”。</span><span class="sxs-lookup"><span data-stu-id="4d226-258">In the Enter voucher id field, type 'IMPORT-001'.</span></span>

    <span data-ttu-id="4d226-259">浏览以找到“1099entries.xml”文件。</span><span class="sxs-lookup"><span data-stu-id="4d226-259">Browse to get the '1099entries.xml' file.</span></span>  

25. <span data-ttu-id="4d226-260">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4d226-260">Click OK.</span></span>

    <span data-ttu-id="4d226-261">所生成警告的列表提供有关错误供应商帐户、错误税 1099 栏代码、缺少的国家/地区代码等的信息。请将此警告列表与执行 XML 文件中包含的内容比较。</span><span class="sxs-lookup"><span data-stu-id="4d226-261">The list of generated warnings provides information about incorrect vendor accounts, an incorrect tax 1099 box code, missing country codes, etc. Compare this list of warnings to the content that is included in the execution XML file.</span></span>  

26. <span data-ttu-id="4d226-262">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4d226-262">Close the page.</span></span>
27. <span data-ttu-id="4d226-263">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4d226-263">Close the page.</span></span>
28. <span data-ttu-id="4d226-264">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4d226-264">Close the page.</span></span>
29. <span data-ttu-id="4d226-265">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4d226-265">Close the page.</span></span>
30. <span data-ttu-id="4d226-266">转至“应付帐款 > 定期任务 > 1099 税 > 用于 1099 的供应商结算”。</span><span class="sxs-lookup"><span data-stu-id="4d226-266">Go to Accounts payable > Periodic tasks > Tax 1099 > Vendor settlement for 1099s.</span></span>

    <span data-ttu-id="4d226-267">此窗体显示根据所导入交易创建的 Tax1099Summary 表中的累计交易。</span><span class="sxs-lookup"><span data-stu-id="4d226-267">This form shows the cumulative transactions in the Tax1099Summary table that have been created based on imported transactions.</span></span>  

31. <span data-ttu-id="4d226-268">在“开始日期”字段中，将日期设置为“2000-01-01”。</span><span class="sxs-lookup"><span data-stu-id="4d226-268">In the From date field, set the date to '2000-01-01'.</span></span>
32. <span data-ttu-id="4d226-269">单击“手动 1099 交易记录”。</span><span class="sxs-lookup"><span data-stu-id="4d226-269">Click Manual 1099 transactions.</span></span>

    <span data-ttu-id="4d226-270">此窗体中包含手动添加的交易和我们刚才导入的交易的列表。</span><span class="sxs-lookup"><span data-stu-id="4d226-270">This form contains the list of transactions that were added manually and those that we just imported.</span></span>  

33. <span data-ttu-id="4d226-271">打开凭证列筛选器。</span><span class="sxs-lookup"><span data-stu-id="4d226-271">Open Voucher column filter.</span></span>
34. <span data-ttu-id="4d226-272">使用 "开头为" 筛选器运算符在 "凭证" 字段上输入筛选器值 "IMPORT-001"。</span><span class="sxs-lookup"><span data-stu-id="4d226-272">Enter a filter value of "IMPORT-001" on the "Voucher" field using the "begins with" filter operator.</span></span>

## <a name="review-the-relationship-between-model-and-format-mappings"></a><span data-ttu-id="4d226-273">检查模型与格式之间的映射的关系</span><span class="sxs-lookup"><span data-stu-id="4d226-273">Review the relationship between model and format mappings</span></span>
1. <span data-ttu-id="4d226-274">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4d226-274">Close the page.</span></span>
2. <span data-ttu-id="4d226-275">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4d226-275">Close the page.</span></span>
3. <span data-ttu-id="4d226-276">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="4d226-276">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="4d226-277">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="4d226-277">Click Reporting configurations.</span></span>
5. <span data-ttu-id="4d226-278">在树结构中，选择“1099 付款模型”。</span><span class="sxs-lookup"><span data-stu-id="4d226-278">In the tree, select '1099 Payments model'.</span></span>

    <span data-ttu-id="4d226-279">假设您希望支持导入相同数据，但是通过 .TXT 文件格式导入。</span><span class="sxs-lookup"><span data-stu-id="4d226-279">Assume that you want to support importing the same data but from a .TXT file format.</span></span>   

6. <span data-ttu-id="4d226-280">单击“创建配置”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="4d226-280">Click Create configuration to open the dialog box.</span></span> 
7. <span data-ttu-id="4d226-281">在“新建”字段中，输入“基于数据模型 1099 付款模型的格式”。</span><span class="sxs-lookup"><span data-stu-id="4d226-281">In the New field, enter 'Format based on data model 1099 Payments model'.</span></span>
8. <span data-ttu-id="4d226-282">在“名称”字段中，键入“从 TXT 文件导入数据”。</span><span class="sxs-lookup"><span data-stu-id="4d226-282">In the Name field, type 'Import data from TXT file'.</span></span>
9. <span data-ttu-id="4d226-283">在“支持数据导入”字段中选择"是"。</span><span class="sxs-lookup"><span data-stu-id="4d226-283">Select Yes in the Supports data import field.</span></span>
10. <span data-ttu-id="4d226-284">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="4d226-284">Click Create configuration.</span></span>
11. <span data-ttu-id="4d226-285">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="4d226-285">Click Designer.</span></span>
12. <span data-ttu-id="4d226-286">单击”将格式映射到模型“。</span><span class="sxs-lookup"><span data-stu-id="4d226-286">Click Map format to model.</span></span>
13. <span data-ttu-id="4d226-287">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="4d226-287">Click New.</span></span>
14. <span data-ttu-id="4d226-288">在“定义”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4d226-288">In the Definition field, enter or select a value.</span></span>

    <span data-ttu-id="4d226-289">选择“1099-MISC”选项。</span><span class="sxs-lookup"><span data-stu-id="4d226-289">Select '1099-MISC' option.</span></span>  

15. <span data-ttu-id="4d226-290">在“名称”字段中，键入“从 TXT 文件导入数据”。</span><span class="sxs-lookup"><span data-stu-id="4d226-290">In the Name field, type 'Import data from TXT file'.</span></span>
16. <span data-ttu-id="4d226-291">在“描述”字段中，键入“从 TXT 文件导入数据”。</span><span class="sxs-lookup"><span data-stu-id="4d226-291">In the Description field, type 'Import data from TXT file'.</span></span>
17. <span data-ttu-id="4d226-292">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="4d226-292">Click Save.</span></span>
18. <span data-ttu-id="4d226-293">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4d226-293">Close the page.</span></span>
19. <span data-ttu-id="4d226-294">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4d226-294">Close the page.</span></span>
20. <span data-ttu-id="4d226-295">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="4d226-295">Click Edit.</span></span>

    <span data-ttu-id="4d226-296">如果您安装了修补程序“KB 4012871 在单独的配置中支持 GER 模型映射，以便可以为在不同版本的 Dynamics 365 Finance 上部署指定不同类型的先决条件”([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871))，请为输入的格式配置执行下一步“开启标记‘模型映射的默认值’”。</span><span class="sxs-lookup"><span data-stu-id="4d226-296">If you installed the hotfix "KB 4012871 Support of GER model mappings in separated configurations with an ability to specify different kinds of prerequisites for deploying them on different versions of Dynamics 365 Finance" ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)), execute the next step "Turn the flag 'Default for model mapping' on" for the entered format configuration.</span></span> <span data-ttu-id="4d226-297">否则跳过下一步。</span><span class="sxs-lookup"><span data-stu-id="4d226-297">Skip the next step otherwise.</span></span>  

21. <span data-ttu-id="4d226-298">在“模型映射的默认值”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="4d226-298">Select Yes in the Default for model-mapping field.</span></span>
22. <span data-ttu-id="4d226-299">在树结构中，选择“1099 付款模型”。</span><span class="sxs-lookup"><span data-stu-id="4d226-299">In the tree, select '1099 Payments model'.</span></span>
23. <span data-ttu-id="4d226-300">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="4d226-300">Click Designer.</span></span>
24. <span data-ttu-id="4d226-301">单击“映射模型到数据源”。</span><span class="sxs-lookup"><span data-stu-id="4d226-301">Click Map model to datasource.</span></span>
25. <span data-ttu-id="4d226-302">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="4d226-302">Click Run.</span></span>

    <span data-ttu-id="4d226-303">如果您安装了修补程序“KB 4012871 在单独的配置中支持 GER 模型映射，以便可以为在不同版本上部署指定不同类型的先决条件 ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871))，请在查找字段中选择首选模型映射。</span><span class="sxs-lookup"><span data-stu-id="4d226-303">If you installed the hotfix, KB 4012871 Support of GER model mappings in separated configurations with an ability to specify different kinds of prerequisites for deploying them on different versions ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)), select the preferred model mapping in the lookup field.</span></span> <span data-ttu-id="4d226-304">如果您尚未安装此修补程序，请跳至下一步，因为默认格式配置的定义已选择了映射。</span><span class="sxs-lookup"><span data-stu-id="4d226-304">If you haven't installed the hotfix yet, skip to the next step as the mapping has already been selected by the definition of the default format configuration.</span></span>  
    
    <span data-ttu-id="4d226-305">如果您尚未安装修补程序 KB 4012871，请注意对话框中还包含一个模型映射问题，用于解析您要导入的文件。</span><span class="sxs-lookup"><span data-stu-id="4d226-305">If you have not installed the hotfix, KB 4012871, notice that the dialog box contains an additional model-mapping question that is used to parse the file that you are importing.</span></span> <span data-ttu-id="4d226-306">然后将数据从对话框移植到数据模型。</span><span class="sxs-lookup"><span data-stu-id="4d226-306">The data is then ported from the dialog box to the data model.</span></span> <span data-ttu-id="4d226-307">目前，您可以根据计划导入的文件类型选择必须使用哪种格式映射。</span><span class="sxs-lookup"><span data-stu-id="4d226-307">Currently, you can choose which format mapping must be used depending on the type of file that you plan to import.</span></span>  
    
    <span data-ttu-id="4d226-308">如果您计划从应用程序中专为此操作设计的某一点调用此模型映射，则必须将 ER 目标和格式映射标记为集成的组成部分。</span><span class="sxs-lookup"><span data-stu-id="4d226-308">If you plan to call this model mapping from a point in the application that is specifically designed for the action, the ER destination and the format mapping must be marked as part of the integration.</span></span>  

26. <span data-ttu-id="4d226-309">单击“取消”。</span><span class="sxs-lookup"><span data-stu-id="4d226-309">Click Cancel.</span></span>
27. <span data-ttu-id="4d226-310">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4d226-310">Close the page.</span></span>
28. <span data-ttu-id="4d226-311">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4d226-311">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

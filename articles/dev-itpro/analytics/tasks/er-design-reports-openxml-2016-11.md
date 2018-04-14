--- 
title: "针对电子申报 (ER) 设计用于生成 OpenXML 格式的报表的配置"
description: "以下步骤说明属于系统管理员或电子报表开发人员的用户如何创建新电子报表 (ER) 配置，使其包含用于生成 OPENXML 格式的电子文档的模板。"
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.openlocfilehash: 882799e12daf9a3b7b530201c913b8f921fb2ed3
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="00936-103">针对电子申报 (ER) 设计用于生成 OpenXML 格式的报表的配置</span><span class="sxs-lookup"><span data-stu-id="00936-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="00936-104">以下步骤说明属于系统管理员或电子报表开发人员的用户如何创建新电子报表 (ER) 配置，使其包含用于生成 OPENXML 格式的电子文档的模板。</span><span class="sxs-lookup"><span data-stu-id="00936-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="00936-105">此配置将用于处理供应商付款。</span><span class="sxs-lookup"><span data-stu-id="00936-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="00936-106">在此示例中，您将创建示例公司 Litware 公司的配置。这些步骤可以在 GBSI 公司执行。</span><span class="sxs-lookup"><span data-stu-id="00936-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="00936-107">为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="00936-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="00936-108">您还必须下载和保存 Microsoft Excel 文件[付款报表模板](https://go.microsoft.com/fwlink/?linkid=862266)。</span><span class="sxs-lookup"><span data-stu-id="00936-108">You must also download and save the Microsoft Excel file, [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 

## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="00936-109">上载付款数据模型配置</span><span class="sxs-lookup"><span data-stu-id="00936-109">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="00936-110">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="00936-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="00936-111">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="00936-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="00936-112">为示例公司选择配置供应商“Litware 公司”。如果没有看到此配置供应商，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="00936-112">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="00936-113">单击“设置有效”。</span><span class="sxs-lookup"><span data-stu-id="00936-113">Click Set active.</span></span>
4. <span data-ttu-id="00936-114">单击“存储库”。</span><span class="sxs-lookup"><span data-stu-id="00936-114">Click Repositories.</span></span>
    * <span data-ttu-id="00936-115">为运营资源类型选择存储库（如果有）。</span><span class="sxs-lookup"><span data-stu-id="00936-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="00936-116">如果可用，跳过有关创建新存储库的以下步骤。</span><span class="sxs-lookup"><span data-stu-id="00936-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="00936-117">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="00936-117">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="00936-118">在“配置存储库类型”字段中，输入“运营资源”。</span><span class="sxs-lookup"><span data-stu-id="00936-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="00936-119">单击“创建存储库”。</span><span class="sxs-lookup"><span data-stu-id="00936-119">Click Create repository.</span></span>
8. <span data-ttu-id="00936-120">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="00936-120">Click OK.</span></span>
9. <span data-ttu-id="00936-121">单击“打开”。</span><span class="sxs-lookup"><span data-stu-id="00936-121">Click Open.</span></span>
10. <span data-ttu-id="00936-122">在树结构中，选择“付款模型”。</span><span class="sxs-lookup"><span data-stu-id="00936-122">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="00936-123">单击“导入”。</span><span class="sxs-lookup"><span data-stu-id="00936-123">Click Import.</span></span>
    * <span data-ttu-id="00936-124">导入此数据模型。</span><span class="sxs-lookup"><span data-stu-id="00936-124">Import this data model.</span></span> <span data-ttu-id="00936-125">将它用作新格式配置中的数据源。</span><span class="sxs-lookup"><span data-stu-id="00936-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="00936-126">如果已经导入了此配置则跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="00936-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="00936-127">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="00936-127">Click Yes.</span></span>
13. <span data-ttu-id="00936-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="00936-128">Close the page.</span></span>
14. <span data-ttu-id="00936-129">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="00936-129">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="00936-130">创建新的格式配置</span><span class="sxs-lookup"><span data-stu-id="00936-130">Create a new format configuration</span></span>
1. <span data-ttu-id="00936-131">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="00936-131">Click Reporting configurations.</span></span>
2. <span data-ttu-id="00936-132">在树结构中，选择“付款模型”。</span><span class="sxs-lookup"><span data-stu-id="00936-132">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="00936-133">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="00936-133">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="00936-134">在“新建”字段中，输入“基于数据模型付款模型的格式”。</span><span class="sxs-lookup"><span data-stu-id="00936-134">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="00936-135">创建一个基于 PaymentModel 数据模型的格式。</span><span class="sxs-lookup"><span data-stu-id="00936-135">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="00936-136">在“名称”字段中，键入“示例工作表报表”。</span><span class="sxs-lookup"><span data-stu-id="00936-136">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="00936-137">示例工作表报表</span><span class="sxs-lookup"><span data-stu-id="00936-137">Sample worksheet report</span></span>  
6. <span data-ttu-id="00936-138">在“描述”字段中，键入“供应商付款的示例工作表报表”。</span><span class="sxs-lookup"><span data-stu-id="00936-138">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="00936-139">供应商付款的示例工作表报表。</span><span class="sxs-lookup"><span data-stu-id="00936-139">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="00936-140">在“数据模型定义”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="00936-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="00936-141">选择“客户贷方转帐发起”定义。</span><span class="sxs-lookup"><span data-stu-id="00936-141">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="00936-142">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="00936-142">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="00936-143">以 OPENXML 工作表格式设计新文档</span><span class="sxs-lookup"><span data-stu-id="00936-143">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="00936-144">在树结构中，选择“付款模型\示例工作表报表”。</span><span class="sxs-lookup"><span data-stu-id="00936-144">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="00936-145">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="00936-145">Click Designer.</span></span>
3. <span data-ttu-id="00936-146">在“操作”窗格上，单击“导入”。</span><span class="sxs-lookup"><span data-stu-id="00936-146">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="00936-147">单击“从 Excel 导入”。</span><span class="sxs-lookup"><span data-stu-id="00936-147">Click Import from Excel.</span></span>
5. <span data-ttu-id="00936-148">单击“附加”。</span><span class="sxs-lookup"><span data-stu-id="00936-148">Click Attachments.</span></span>
    * <span data-ttu-id="00936-149">作为模板附加现有 Excel 文档。</span><span class="sxs-lookup"><span data-stu-id="00936-149">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="00936-150">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="00936-150">Click New.</span></span>
7. <span data-ttu-id="00936-151">单击“文件”。</span><span class="sxs-lookup"><span data-stu-id="00936-151">Click File.</span></span>
    * <span data-ttu-id="00936-152">指向现有 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="00936-152">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="00936-153">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="00936-153">Close the page.</span></span>
9. <span data-ttu-id="00936-154">在“模板”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="00936-154">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="00936-155">选择用作模板的附加的 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="00936-155">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="00936-156">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="00936-156">Click OK.</span></span>
    * <span data-ttu-id="00936-157">请注意，ER 格式组件已基于引用 MS Excel 文档的结构以设计格式创建（指定范围）。</span><span class="sxs-lookup"><span data-stu-id="00936-157">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="00936-158">创建新的数据源以按币种代码计算总计</span><span class="sxs-lookup"><span data-stu-id="00936-158">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="00936-159">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="00936-159">Click the Mapping tab.</span></span>
2. <span data-ttu-id="00936-160">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="00936-160">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="00936-161">在树结构中，选择“功能\分组依据”。</span><span class="sxs-lookup"><span data-stu-id="00936-161">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="00936-162">在“名称”字段中，键入 'PaymentByCurrency'。</span><span class="sxs-lookup"><span data-stu-id="00936-162">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="00936-163">付款币种</span><span class="sxs-lookup"><span data-stu-id="00936-163">PaymentByCurrency</span></span>  
5. <span data-ttu-id="00936-164">单击“编辑分组依据”。</span><span class="sxs-lookup"><span data-stu-id="00936-164">Click Edit group by.</span></span>
6. <span data-ttu-id="00936-165">在树结构中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="00936-165">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="00936-166">在树结构中，选择“模型\付款”。</span><span class="sxs-lookup"><span data-stu-id="00936-166">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="00936-167">单击“将字段添加到”。</span><span class="sxs-lookup"><span data-stu-id="00936-167">Click Add field to.</span></span>
9. <span data-ttu-id="00936-168">单击“什么要分组”。</span><span class="sxs-lookup"><span data-stu-id="00936-168">Click What to group.</span></span>
10. <span data-ttu-id="00936-169">在树结构中，展开“模型\付款”。</span><span class="sxs-lookup"><span data-stu-id="00936-169">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="00936-170">在树结构中，选择“模型\付款\货币”。</span><span class="sxs-lookup"><span data-stu-id="00936-170">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="00936-171">单击“将字段添加到”。</span><span class="sxs-lookup"><span data-stu-id="00936-171">Click Add field to.</span></span>
13. <span data-ttu-id="00936-172">单击“分组字段”。</span><span class="sxs-lookup"><span data-stu-id="00936-172">Click Grouped fields.</span></span>
14. <span data-ttu-id="00936-173">在树结构中，选择“模型\付款\指示金额(InstructedAmount)”。</span><span class="sxs-lookup"><span data-stu-id="00936-173">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="00936-174">单击“将字段添加到”。</span><span class="sxs-lookup"><span data-stu-id="00936-174">Click Add field to.</span></span>
16. <span data-ttu-id="00936-175">单击“合并字段”。</span><span class="sxs-lookup"><span data-stu-id="00936-175">Click Aggregation fields.</span></span>
17. <span data-ttu-id="00936-176">在“方法”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="00936-176">In the Method field, select an option.</span></span>
    * <span data-ttu-id="00936-177">选择 SUM 合并功能。</span><span class="sxs-lookup"><span data-stu-id="00936-177">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="00936-178">在“名称”字段中，键入 'TotalInstructuredAmount'。</span><span class="sxs-lookup"><span data-stu-id="00936-178">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="00936-179">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="00936-179">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="00936-180">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="00936-180">Click Save.</span></span>
20. <span data-ttu-id="00936-181">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="00936-181">Close the page.</span></span>
21. <span data-ttu-id="00936-182">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="00936-182">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="00936-183">将格式组件映射到数据源</span><span class="sxs-lookup"><span data-stu-id="00936-183">Map format components to data sources</span></span>
1. <span data-ttu-id="00936-184">在树结构中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="00936-184">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="00936-185">在树结构中，展开“模型\付款”。</span><span class="sxs-lookup"><span data-stu-id="00936-185">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="00936-186">在树结构中，展开“模型\付款\发起方(InitiatingParty)”。</span><span class="sxs-lookup"><span data-stu-id="00936-186">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="00936-187">在树结构中，选择“模型\付款\发起方(InitiatingParty)名称”。</span><span class="sxs-lookup"><span data-stu-id="00936-187">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="00936-188">在树结构中，展开或折叠“Excel\报表页眉”。</span><span class="sxs-lookup"><span data-stu-id="00936-188">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="00936-189">在树结构中，选择“Excel\报表页眉\公司名称”。</span><span class="sxs-lookup"><span data-stu-id="00936-189">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="00936-190">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="00936-190">Click Bind.</span></span>
8. <span data-ttu-id="00936-191">在树结构中，展开“模型\付款\贷方”。</span><span class="sxs-lookup"><span data-stu-id="00936-191">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="00936-192">在树结构中，展开“模型\付款\贷方\身份证明”。</span><span class="sxs-lookup"><span data-stu-id="00936-192">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="00936-193">在树结构中，选择“模型\付款\贷方\身份证明\源 ID(SourceID)”。</span><span class="sxs-lookup"><span data-stu-id="00936-193">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="00936-194">在树结构中，展开或折叠“Excel\付款方式行”。</span><span class="sxs-lookup"><span data-stu-id="00936-194">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="00936-195">在树结构中，选择“Excel\付款方式行\供应商帐户名称”。</span><span class="sxs-lookup"><span data-stu-id="00936-195">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="00936-196">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="00936-196">Click Bind.</span></span>
14. <span data-ttu-id="00936-197">在树结构中，展开“模型\付款\贷方\名称”。</span><span class="sxs-lookup"><span data-stu-id="00936-197">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="00936-198">在树结构中，选择“Excel\付款方式行\供应商名称”。</span><span class="sxs-lookup"><span data-stu-id="00936-198">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="00936-199">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="00936-199">Click Bind.</span></span>
17. <span data-ttu-id="00936-200">在树结构中，展开“模型\付款\贷方代理(CreditorAgent)”。</span><span class="sxs-lookup"><span data-stu-id="00936-200">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="00936-201">在树结构中，选择“模型\付款\贷方代理(CreditorAgent)\名称”。</span><span class="sxs-lookup"><span data-stu-id="00936-201">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="00936-202">在树结构中，选择“Excel\付款方式行\银行”。</span><span class="sxs-lookup"><span data-stu-id="00936-202">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="00936-203">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="00936-203">Click Bind.</span></span>
21. <span data-ttu-id="00936-204">在树结构中，选择“模型\付款\贷方代理(CreditorAgent)\银行代号(RoutingNumber)”。</span><span class="sxs-lookup"><span data-stu-id="00936-204">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="00936-205">在树结构中，选择“Excel\付款方式行\银行代号”。</span><span class="sxs-lookup"><span data-stu-id="00936-205">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="00936-206">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="00936-206">Click Bind.</span></span>
24. <span data-ttu-id="00936-207">在树结构中，展开“模型\付款\贷方科目(CreditorAccount)”。</span><span class="sxs-lookup"><span data-stu-id="00936-207">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="00936-208">在树结构中，展开“模型\付款\贷方科目(CreditorAccount)\标识”。</span><span class="sxs-lookup"><span data-stu-id="00936-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="00936-209">在树结构中，选择“模型\付款\贷方科目(CreditorAccount)\身份证明\编号”。</span><span class="sxs-lookup"><span data-stu-id="00936-209">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="00936-210">在树结构中，选择“Excel\付款方式行\帐号”。</span><span class="sxs-lookup"><span data-stu-id="00936-210">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="00936-211">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="00936-211">Click Bind.</span></span>
29. <span data-ttu-id="00936-212">在树结构中，选择“模型\付款\指示金额(InstructedAmount)”。</span><span class="sxs-lookup"><span data-stu-id="00936-212">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="00936-213">在树结构中，选择“Excel\付款方式行\借方”。</span><span class="sxs-lookup"><span data-stu-id="00936-213">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="00936-214">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="00936-214">Click Bind.</span></span>
32. <span data-ttu-id="00936-215">在树结构中，展开“模型\付款\贷方”。</span><span class="sxs-lookup"><span data-stu-id="00936-215">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="00936-216">在树结构中，展开“模型\付款\贷方科目(CreditorAccount)”。</span><span class="sxs-lookup"><span data-stu-id="00936-216">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="00936-217">在树结构中，展开“模型\付款\贷方代理(CreditorAgent)”。</span><span class="sxs-lookup"><span data-stu-id="00936-217">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="00936-218">在树结构中，选择“模型\付款\货币”。</span><span class="sxs-lookup"><span data-stu-id="00936-218">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="00936-219">在树结构中，选择“Excel\付款方式行\货币”。</span><span class="sxs-lookup"><span data-stu-id="00936-219">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="00936-220">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="00936-220">Click Bind.</span></span>
38. <span data-ttu-id="00936-221">在树结构中，展开 'PaymentByCurrency'。</span><span class="sxs-lookup"><span data-stu-id="00936-221">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="00936-222">在树结构中，展开 'PaymentByCurrency\grouped'。</span><span class="sxs-lookup"><span data-stu-id="00936-222">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="00936-223">在树结构中，选择“PaymentByCurrency\已分组\货币”。</span><span class="sxs-lookup"><span data-stu-id="00936-223">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="00936-224">在树结构中，展开或折叠“Excel\汇总行”。</span><span class="sxs-lookup"><span data-stu-id="00936-224">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="00936-225">在树结构中，选择“Excel\汇总行\汇总货币”。</span><span class="sxs-lookup"><span data-stu-id="00936-225">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="00936-226">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="00936-226">Click Bind.</span></span>
44. <span data-ttu-id="00936-227">在树结构中，展开 'PaymentByCurrency\aggregated'。</span><span class="sxs-lookup"><span data-stu-id="00936-227">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="00936-228">在树结构中，选择 'PaymentByCurrency\aggregated\TotalInstructuredAmount'。</span><span class="sxs-lookup"><span data-stu-id="00936-228">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="00936-229">在树结构中，选择“Excel\汇总行\汇总金额”。</span><span class="sxs-lookup"><span data-stu-id="00936-229">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="00936-230">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="00936-230">Click Bind.</span></span>
48. <span data-ttu-id="00936-231">在树结构中，选择 'PaymentByCurrency'。</span><span class="sxs-lookup"><span data-stu-id="00936-231">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="00936-232">在树中，选择“Excel\汇总行”。</span><span class="sxs-lookup"><span data-stu-id="00936-232">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="00936-233">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="00936-233">Click Bind.</span></span>
51. <span data-ttu-id="00936-234">在树结构中，选择“模型\付款”。</span><span class="sxs-lookup"><span data-stu-id="00936-234">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="00936-235">在树结构中，选择“Excel\付款方式行”。</span><span class="sxs-lookup"><span data-stu-id="00936-235">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="00936-236">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="00936-236">Click Bind.</span></span>
54. <span data-ttu-id="00936-237">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="00936-237">Click Save.</span></span>
55. <span data-ttu-id="00936-238">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="00936-238">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="00936-239">将创建的配置用于处理付款</span><span class="sxs-lookup"><span data-stu-id="00936-239">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="00936-240">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="00936-240">Click Change status.</span></span>
2. <span data-ttu-id="00936-241">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="00936-241">Click Complete.</span></span>
3. <span data-ttu-id="00936-242">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="00936-242">Click OK.</span></span>
4. <span data-ttu-id="00936-243">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="00936-243">Close the page.</span></span>
5. <span data-ttu-id="00936-244">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="00936-244">Close the page.</span></span>
6. <span data-ttu-id="00936-245">转至“应付账款”>“付款设置”>“付款方式”。</span><span class="sxs-lookup"><span data-stu-id="00936-245">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="00936-246">使用快速筛选来筛选带“电子”值的“付款方式”字段。</span><span class="sxs-lookup"><span data-stu-id="00936-246">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="00936-247">电子</span><span class="sxs-lookup"><span data-stu-id="00936-247">Electronic</span></span>  
8. <span data-ttu-id="00936-248">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="00936-248">Click Edit.</span></span>
9. <span data-ttu-id="00936-249">展开“文件格式”部分。</span><span class="sxs-lookup"><span data-stu-id="00936-249">Expand the File formats section.</span></span>
10. <span data-ttu-id="00936-250">在“普通电子申报”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="00936-250">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="00936-251">在“导出格式配置”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="00936-251">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="00936-252">选择“示例工作表报表”配置。</span><span class="sxs-lookup"><span data-stu-id="00936-252">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="00936-253">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="00936-253">Click Save.</span></span>
13. <span data-ttu-id="00936-254">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="00936-254">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="00936-255">使用创建的配置进行付款日记帐处理测试</span><span class="sxs-lookup"><span data-stu-id="00936-255">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="00936-256">转至“应付账款”>“付款”>“付款日记帐”。</span><span class="sxs-lookup"><span data-stu-id="00936-256">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="00936-257">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="00936-257">Click New.</span></span>
    * <span data-ttu-id="00936-258">新建付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="00936-258">Create a new payment journal.</span></span>  
3. <span data-ttu-id="00936-259">在“名称”字段中，键入“VendPay”。</span><span class="sxs-lookup"><span data-stu-id="00936-259">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="00936-260">VendPay</span><span class="sxs-lookup"><span data-stu-id="00936-260">VendPay</span></span>  
4. <span data-ttu-id="00936-261">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="00936-261">Click Lines.</span></span>
5. <span data-ttu-id="00936-262">在“帐户”字段中，指定值 'GB_SI_000001'。</span><span class="sxs-lookup"><span data-stu-id="00936-262">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="00936-263">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="00936-263">GB_SI_000001</span></span>  
6. <span data-ttu-id="00936-264">将“借方”设置为 '1000'。</span><span class="sxs-lookup"><span data-stu-id="00936-264">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="00936-265">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="00936-265">Click New.</span></span>
8. <span data-ttu-id="00936-266">在“帐户”字段中，指定值 'GB_SI_000005'。</span><span class="sxs-lookup"><span data-stu-id="00936-266">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="00936-267">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="00936-267">GB_SI_000005</span></span>  
9. <span data-ttu-id="00936-268">将“借方”设置为 '2000'。</span><span class="sxs-lookup"><span data-stu-id="00936-268">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="00936-269">在“货币”字段中，键入 'EUR'。</span><span class="sxs-lookup"><span data-stu-id="00936-269">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="00936-270">欧元</span><span class="sxs-lookup"><span data-stu-id="00936-270">EUR</span></span>  
11. <span data-ttu-id="00936-271">在“对方科目”字段中，指定值为 'GBSI OPER'。</span><span class="sxs-lookup"><span data-stu-id="00936-271">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="00936-272">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="00936-272">GBSI OPER</span></span>  
12. <span data-ttu-id="00936-273">在“付款方式”字段中，键入“电子”。</span><span class="sxs-lookup"><span data-stu-id="00936-273">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="00936-274">电子</span><span class="sxs-lookup"><span data-stu-id="00936-274">Electronic</span></span>  
13. <span data-ttu-id="00936-275">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="00936-275">Click Save.</span></span>
14. <span data-ttu-id="00936-276">点击”生成付款“。</span><span class="sxs-lookup"><span data-stu-id="00936-276">Click Generate payments.</span></span>
15. <span data-ttu-id="00936-277">在“付款方式”字段中，键入“电子”。</span><span class="sxs-lookup"><span data-stu-id="00936-277">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="00936-278">电子</span><span class="sxs-lookup"><span data-stu-id="00936-278">Electronic</span></span>  
16. <span data-ttu-id="00936-279">在“文件名”字段中，键入“付款”。</span><span class="sxs-lookup"><span data-stu-id="00936-279">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="00936-280">例如，键入“付款”。</span><span class="sxs-lookup"><span data-stu-id="00936-280">For example, type Payments.</span></span>  
17. <span data-ttu-id="00936-281">在“银行帐户”字段中，键入 'GBSI OPER'。</span><span class="sxs-lookup"><span data-stu-id="00936-281">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="00936-282">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="00936-282">GBSI OPER</span></span>  
18. <span data-ttu-id="00936-283">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="00936-283">Click OK.</span></span>
19. <span data-ttu-id="00936-284">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="00936-284">Click OK.</span></span>
    * <span data-ttu-id="00936-285">审查已创建的工作表，包括付款行详细信息以及用于此付款消息的每个币种代码的总计。</span><span class="sxs-lookup"><span data-stu-id="00936-285">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  



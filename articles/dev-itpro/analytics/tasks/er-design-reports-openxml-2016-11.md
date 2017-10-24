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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 04def14ddf9b079005bf11acbcaf64b21aa80fdb
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="8165f-103">针对电子申报 (ER) 设计用于生成 OpenXML 格式的报表的配置</span><span class="sxs-lookup"><span data-stu-id="8165f-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8165f-104">以下步骤说明属于系统管理员或电子报表开发人员的用户如何创建新电子报表 (ER) 配置，使其包含用于生成 OPENXML 格式的电子文档的模板。</span><span class="sxs-lookup"><span data-stu-id="8165f-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="8165f-105">此配置将用于处理供应商付款。</span><span class="sxs-lookup"><span data-stu-id="8165f-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="8165f-106">在此示例中，您将创建示例公司 Litware 公司的配置。这些步骤可以在 GBSI 公司执行。</span><span class="sxs-lookup"><span data-stu-id="8165f-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="8165f-107">为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="8165f-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="8165f-108">您还必须具有在创建模板时将导入的 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="8165f-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="8165f-109">此文件可以从以下位置访问：https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span><span class="sxs-lookup"><span data-stu-id="8165f-109">This file can be accessed from:  https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="8165f-110">上载付款数据模型配置</span><span class="sxs-lookup"><span data-stu-id="8165f-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="8165f-111">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="8165f-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="8165f-112">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="8165f-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8165f-113">为示例公司选择配置供应商“Litware 公司”。如果没有看到此配置供应商，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="8165f-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="8165f-114">单击“设置有效”。</span><span class="sxs-lookup"><span data-stu-id="8165f-114">Click Set active.</span></span>
4. <span data-ttu-id="8165f-115">单击“存储库”。</span><span class="sxs-lookup"><span data-stu-id="8165f-115">Click Repositories.</span></span>
    * <span data-ttu-id="8165f-116">为运营资源类型选择存储库（如果有）。</span><span class="sxs-lookup"><span data-stu-id="8165f-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="8165f-117">如果可用，跳过有关创建新存储库的以下步骤。</span><span class="sxs-lookup"><span data-stu-id="8165f-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="8165f-118">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="8165f-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="8165f-119">在“配置存储库类型”字段中，输入“运营资源”。</span><span class="sxs-lookup"><span data-stu-id="8165f-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="8165f-120">单击“创建存储库”。</span><span class="sxs-lookup"><span data-stu-id="8165f-120">Click Create repository.</span></span>
8. <span data-ttu-id="8165f-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8165f-121">Click OK.</span></span>
9. <span data-ttu-id="8165f-122">单击“打开”。</span><span class="sxs-lookup"><span data-stu-id="8165f-122">Click Open.</span></span>
10. <span data-ttu-id="8165f-123">在树结构中，选择“付款模型”。</span><span class="sxs-lookup"><span data-stu-id="8165f-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="8165f-124">单击“导入”。</span><span class="sxs-lookup"><span data-stu-id="8165f-124">Click Import.</span></span>
    * <span data-ttu-id="8165f-125">导入此数据模型。</span><span class="sxs-lookup"><span data-stu-id="8165f-125">Import this data model.</span></span> <span data-ttu-id="8165f-126">将它用作新格式配置中的数据源。</span><span class="sxs-lookup"><span data-stu-id="8165f-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="8165f-127">如果已经导入了此配置则跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="8165f-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="8165f-128">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="8165f-128">Click Yes.</span></span>
13. <span data-ttu-id="8165f-129">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8165f-129">Close the page.</span></span>
14. <span data-ttu-id="8165f-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8165f-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="8165f-131">创建新的格式配置</span><span class="sxs-lookup"><span data-stu-id="8165f-131">Create a new format configuration</span></span>
1. <span data-ttu-id="8165f-132">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="8165f-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="8165f-133">在树结构中，选择“付款模型”。</span><span class="sxs-lookup"><span data-stu-id="8165f-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="8165f-134">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="8165f-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="8165f-135">在“新建”字段中，输入“基于数据模型付款模型的格式”。</span><span class="sxs-lookup"><span data-stu-id="8165f-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="8165f-136">创建一个基于 PaymentModel 数据模型的格式。</span><span class="sxs-lookup"><span data-stu-id="8165f-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="8165f-137">在“名称”字段中，键入“示例工作表报表”。</span><span class="sxs-lookup"><span data-stu-id="8165f-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="8165f-138">示例工作表报表</span><span class="sxs-lookup"><span data-stu-id="8165f-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="8165f-139">在“描述”字段中，键入“供应商付款的示例工作表报表”。</span><span class="sxs-lookup"><span data-stu-id="8165f-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="8165f-140">供应商付款的示例工作表报表。</span><span class="sxs-lookup"><span data-stu-id="8165f-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="8165f-141">在“数据模型定义”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8165f-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="8165f-142">选择“客户贷方转帐发起”定义。</span><span class="sxs-lookup"><span data-stu-id="8165f-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="8165f-143">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="8165f-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="8165f-144">以 OPENXML 工作表格式设计新文档</span><span class="sxs-lookup"><span data-stu-id="8165f-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="8165f-145">在树结构中，选择“付款模型\示例工作表报表”。</span><span class="sxs-lookup"><span data-stu-id="8165f-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="8165f-146">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="8165f-146">Click Designer.</span></span>
3. <span data-ttu-id="8165f-147">在“操作”窗格上，单击“导入”。</span><span class="sxs-lookup"><span data-stu-id="8165f-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="8165f-148">单击“从 Excel 导入”。</span><span class="sxs-lookup"><span data-stu-id="8165f-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="8165f-149">单击“附加”。</span><span class="sxs-lookup"><span data-stu-id="8165f-149">Click Attachments.</span></span>
    * <span data-ttu-id="8165f-150">作为模板附加现有 Excel 文档。</span><span class="sxs-lookup"><span data-stu-id="8165f-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="8165f-151">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8165f-151">Click New.</span></span>
7. <span data-ttu-id="8165f-152">单击“文件”。</span><span class="sxs-lookup"><span data-stu-id="8165f-152">Click File.</span></span>
    * <span data-ttu-id="8165f-153">指向现有 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="8165f-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="8165f-154">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8165f-154">Close the page.</span></span>
9. <span data-ttu-id="8165f-155">在“模板”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8165f-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="8165f-156">选择用作模板的附加的 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="8165f-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="8165f-157">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8165f-157">Click OK.</span></span>
    * <span data-ttu-id="8165f-158">请注意，ER 格式组件已基于引用 MS Excel 文档的结构以设计格式创建（指定范围）。</span><span class="sxs-lookup"><span data-stu-id="8165f-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="8165f-159">创建新的数据源以按币种代码计算总计</span><span class="sxs-lookup"><span data-stu-id="8165f-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="8165f-160">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="8165f-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="8165f-161">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="8165f-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="8165f-162">在树结构中，选择“功能\分组依据”。</span><span class="sxs-lookup"><span data-stu-id="8165f-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="8165f-163">在“名称”字段中，键入 'PaymentByCurrency'。</span><span class="sxs-lookup"><span data-stu-id="8165f-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="8165f-164">付款币种</span><span class="sxs-lookup"><span data-stu-id="8165f-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="8165f-165">单击“编辑分组依据”。</span><span class="sxs-lookup"><span data-stu-id="8165f-165">Click Edit group by.</span></span>
6. <span data-ttu-id="8165f-166">在树结构中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="8165f-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="8165f-167">在树结构中，选择“模型\付款”。</span><span class="sxs-lookup"><span data-stu-id="8165f-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="8165f-168">单击“将字段添加到”。</span><span class="sxs-lookup"><span data-stu-id="8165f-168">Click Add field to.</span></span>
9. <span data-ttu-id="8165f-169">单击“什么要分组”。</span><span class="sxs-lookup"><span data-stu-id="8165f-169">Click What to group.</span></span>
10. <span data-ttu-id="8165f-170">在树结构中，展开“模型\付款”。</span><span class="sxs-lookup"><span data-stu-id="8165f-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="8165f-171">在树结构中，选择“模型\付款\货币”。</span><span class="sxs-lookup"><span data-stu-id="8165f-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="8165f-172">单击“将字段添加到”。</span><span class="sxs-lookup"><span data-stu-id="8165f-172">Click Add field to.</span></span>
13. <span data-ttu-id="8165f-173">单击“分组字段”。</span><span class="sxs-lookup"><span data-stu-id="8165f-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="8165f-174">在树结构中，选择“模型\付款\指示金额(InstructedAmount)”。</span><span class="sxs-lookup"><span data-stu-id="8165f-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="8165f-175">单击“将字段添加到”。</span><span class="sxs-lookup"><span data-stu-id="8165f-175">Click Add field to.</span></span>
16. <span data-ttu-id="8165f-176">单击“合并字段”。</span><span class="sxs-lookup"><span data-stu-id="8165f-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="8165f-177">在“方法”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="8165f-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="8165f-178">选择 SUM 合并功能。</span><span class="sxs-lookup"><span data-stu-id="8165f-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="8165f-179">在“名称”字段中，键入 'TotalInstructuredAmount'。</span><span class="sxs-lookup"><span data-stu-id="8165f-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="8165f-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="8165f-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="8165f-181">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="8165f-181">Click Save.</span></span>
20. <span data-ttu-id="8165f-182">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8165f-182">Close the page.</span></span>
21. <span data-ttu-id="8165f-183">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8165f-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="8165f-184">将格式组件映射到数据源</span><span class="sxs-lookup"><span data-stu-id="8165f-184">Map format components to data sources</span></span>
1. <span data-ttu-id="8165f-185">在树结构中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="8165f-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="8165f-186">在树结构中，展开“模型\付款”。</span><span class="sxs-lookup"><span data-stu-id="8165f-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="8165f-187">在树结构中，展开“模型\付款\发起方(InitiatingParty)”。</span><span class="sxs-lookup"><span data-stu-id="8165f-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="8165f-188">在树结构中，选择“模型\付款\发起方(InitiatingParty)名称”。</span><span class="sxs-lookup"><span data-stu-id="8165f-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="8165f-189">在树结构中，展开或折叠“Excel\报表页眉”。</span><span class="sxs-lookup"><span data-stu-id="8165f-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="8165f-190">在树结构中，选择“Excel\报表页眉\公司名称”。</span><span class="sxs-lookup"><span data-stu-id="8165f-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="8165f-191">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="8165f-191">Click Bind.</span></span>
8. <span data-ttu-id="8165f-192">在树结构中，展开“模型\付款\贷方”。</span><span class="sxs-lookup"><span data-stu-id="8165f-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="8165f-193">在树结构中，展开“模型\付款\贷方\身份证明”。</span><span class="sxs-lookup"><span data-stu-id="8165f-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="8165f-194">在树结构中，选择“模型\付款\贷方\身份证明\源 ID(SourceID)”。</span><span class="sxs-lookup"><span data-stu-id="8165f-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="8165f-195">在树结构中，展开或折叠“Excel\付款方式行”。</span><span class="sxs-lookup"><span data-stu-id="8165f-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="8165f-196">在树结构中，选择“Excel\付款方式行\供应商帐户名称”。</span><span class="sxs-lookup"><span data-stu-id="8165f-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="8165f-197">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="8165f-197">Click Bind.</span></span>
14. <span data-ttu-id="8165f-198">在树结构中，展开“模型\付款\贷方\名称”。</span><span class="sxs-lookup"><span data-stu-id="8165f-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="8165f-199">在树结构中，选择“Excel\付款方式行\供应商名称”。</span><span class="sxs-lookup"><span data-stu-id="8165f-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="8165f-200">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="8165f-200">Click Bind.</span></span>
17. <span data-ttu-id="8165f-201">在树结构中，展开“模型\付款\贷方代理(CreditorAgent)”。</span><span class="sxs-lookup"><span data-stu-id="8165f-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="8165f-202">在树结构中，选择“模型\付款\贷方代理(CreditorAgent)\名称”。</span><span class="sxs-lookup"><span data-stu-id="8165f-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="8165f-203">在树结构中，选择“Excel\付款方式行\银行”。</span><span class="sxs-lookup"><span data-stu-id="8165f-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="8165f-204">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="8165f-204">Click Bind.</span></span>
21. <span data-ttu-id="8165f-205">在树结构中，选择“模型\付款\贷方代理(CreditorAgent)\银行代号(RoutingNumber)”。</span><span class="sxs-lookup"><span data-stu-id="8165f-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="8165f-206">在树结构中，选择“Excel\付款方式行\银行代号”。</span><span class="sxs-lookup"><span data-stu-id="8165f-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="8165f-207">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="8165f-207">Click Bind.</span></span>
24. <span data-ttu-id="8165f-208">在树结构中，展开“模型\付款\贷方科目(CreditorAccount)”。</span><span class="sxs-lookup"><span data-stu-id="8165f-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="8165f-209">在树结构中，展开“模型\付款\贷方科目(CreditorAccount)\标识”。</span><span class="sxs-lookup"><span data-stu-id="8165f-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="8165f-210">在树结构中，选择“模型\付款\贷方科目(CreditorAccount)\身份证明\编号”。</span><span class="sxs-lookup"><span data-stu-id="8165f-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="8165f-211">在树结构中，选择“Excel\付款方式行\帐号”。</span><span class="sxs-lookup"><span data-stu-id="8165f-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="8165f-212">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="8165f-212">Click Bind.</span></span>
29. <span data-ttu-id="8165f-213">在树结构中，选择“模型\付款\指示金额(InstructedAmount)”。</span><span class="sxs-lookup"><span data-stu-id="8165f-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="8165f-214">在树结构中，选择“Excel\付款方式行\借方”。</span><span class="sxs-lookup"><span data-stu-id="8165f-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="8165f-215">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="8165f-215">Click Bind.</span></span>
32. <span data-ttu-id="8165f-216">在树结构中，展开“模型\付款\贷方”。</span><span class="sxs-lookup"><span data-stu-id="8165f-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="8165f-217">在树结构中，展开“模型\付款\贷方科目(CreditorAccount)”。</span><span class="sxs-lookup"><span data-stu-id="8165f-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="8165f-218">在树结构中，展开“模型\付款\贷方代理(CreditorAgent)”。</span><span class="sxs-lookup"><span data-stu-id="8165f-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="8165f-219">在树结构中，选择“模型\付款\货币”。</span><span class="sxs-lookup"><span data-stu-id="8165f-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="8165f-220">在树结构中，选择“Excel\付款方式行\货币”。</span><span class="sxs-lookup"><span data-stu-id="8165f-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="8165f-221">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="8165f-221">Click Bind.</span></span>
38. <span data-ttu-id="8165f-222">在树结构中，展开 'PaymentByCurrency'。</span><span class="sxs-lookup"><span data-stu-id="8165f-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="8165f-223">在树结构中，展开 'PaymentByCurrency\grouped'。</span><span class="sxs-lookup"><span data-stu-id="8165f-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="8165f-224">在树结构中，选择“PaymentByCurrency\已分组\货币”。</span><span class="sxs-lookup"><span data-stu-id="8165f-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="8165f-225">在树结构中，展开或折叠“Excel\汇总行”。</span><span class="sxs-lookup"><span data-stu-id="8165f-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="8165f-226">在树结构中，选择“Excel\汇总行\汇总货币”。</span><span class="sxs-lookup"><span data-stu-id="8165f-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="8165f-227">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="8165f-227">Click Bind.</span></span>
44. <span data-ttu-id="8165f-228">在树结构中，展开 'PaymentByCurrency\aggregated'。</span><span class="sxs-lookup"><span data-stu-id="8165f-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="8165f-229">在树结构中，选择 'PaymentByCurrency\aggregated\TotalInstructuredAmount'。</span><span class="sxs-lookup"><span data-stu-id="8165f-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="8165f-230">在树结构中，选择“Excel\汇总行\汇总金额”。</span><span class="sxs-lookup"><span data-stu-id="8165f-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="8165f-231">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="8165f-231">Click Bind.</span></span>
48. <span data-ttu-id="8165f-232">在树结构中，选择 'PaymentByCurrency'。</span><span class="sxs-lookup"><span data-stu-id="8165f-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="8165f-233">在树中，选择“Excel\汇总行”。</span><span class="sxs-lookup"><span data-stu-id="8165f-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="8165f-234">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="8165f-234">Click Bind.</span></span>
51. <span data-ttu-id="8165f-235">在树结构中，选择“模型\付款”。</span><span class="sxs-lookup"><span data-stu-id="8165f-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="8165f-236">在树结构中，选择“Excel\付款方式行”。</span><span class="sxs-lookup"><span data-stu-id="8165f-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="8165f-237">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="8165f-237">Click Bind.</span></span>
54. <span data-ttu-id="8165f-238">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="8165f-238">Click Save.</span></span>
55. <span data-ttu-id="8165f-239">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8165f-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="8165f-240">将创建的配置用于处理付款</span><span class="sxs-lookup"><span data-stu-id="8165f-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="8165f-241">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="8165f-241">Click Change status.</span></span>
2. <span data-ttu-id="8165f-242">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="8165f-242">Click Complete.</span></span>
3. <span data-ttu-id="8165f-243">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8165f-243">Click OK.</span></span>
4. <span data-ttu-id="8165f-244">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8165f-244">Close the page.</span></span>
5. <span data-ttu-id="8165f-245">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8165f-245">Close the page.</span></span>
6. <span data-ttu-id="8165f-246">转至“应付账款”>“付款设置”>“付款方式”。</span><span class="sxs-lookup"><span data-stu-id="8165f-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="8165f-247">使用快速筛选来筛选带“电子”值的“付款方式”字段。</span><span class="sxs-lookup"><span data-stu-id="8165f-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="8165f-248">电子</span><span class="sxs-lookup"><span data-stu-id="8165f-248">Electronic</span></span>  
8. <span data-ttu-id="8165f-249">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="8165f-249">Click Edit.</span></span>
9. <span data-ttu-id="8165f-250">展开“文件格式”部分。</span><span class="sxs-lookup"><span data-stu-id="8165f-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="8165f-251">在“普通电子申报”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="8165f-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="8165f-252">在“导出格式配置”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8165f-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="8165f-253">选择“示例工作表报表”配置。</span><span class="sxs-lookup"><span data-stu-id="8165f-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="8165f-254">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="8165f-254">Click Save.</span></span>
13. <span data-ttu-id="8165f-255">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8165f-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="8165f-256">使用创建的配置进行付款日记帐处理测试</span><span class="sxs-lookup"><span data-stu-id="8165f-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="8165f-257">转至“应付账款”>“付款”>“付款日记帐”。</span><span class="sxs-lookup"><span data-stu-id="8165f-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="8165f-258">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8165f-258">Click New.</span></span>
    * <span data-ttu-id="8165f-259">新建付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="8165f-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="8165f-260">在“名称”字段中，键入“VendPay”。</span><span class="sxs-lookup"><span data-stu-id="8165f-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="8165f-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="8165f-261">VendPay</span></span>  
4. <span data-ttu-id="8165f-262">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="8165f-262">Click Lines.</span></span>
5. <span data-ttu-id="8165f-263">在“帐户”字段中，指定值 'GB_SI_000001'。</span><span class="sxs-lookup"><span data-stu-id="8165f-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="8165f-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="8165f-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="8165f-265">将“借方”设置为 '1000'。</span><span class="sxs-lookup"><span data-stu-id="8165f-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="8165f-266">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8165f-266">Click New.</span></span>
8. <span data-ttu-id="8165f-267">在“帐户”字段中，指定值 'GB_SI_000005'。</span><span class="sxs-lookup"><span data-stu-id="8165f-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="8165f-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="8165f-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="8165f-269">将“借方”设置为 '2000'。</span><span class="sxs-lookup"><span data-stu-id="8165f-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="8165f-270">在“货币”字段中，键入 'EUR'。</span><span class="sxs-lookup"><span data-stu-id="8165f-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="8165f-271">欧元</span><span class="sxs-lookup"><span data-stu-id="8165f-271">EUR</span></span>  
11. <span data-ttu-id="8165f-272">在“对方科目”字段中，指定值为 'GBSI OPER'。</span><span class="sxs-lookup"><span data-stu-id="8165f-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="8165f-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="8165f-273">GBSI OPER</span></span>  
12. <span data-ttu-id="8165f-274">在“付款方式”字段中，键入“电子”。</span><span class="sxs-lookup"><span data-stu-id="8165f-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="8165f-275">电子</span><span class="sxs-lookup"><span data-stu-id="8165f-275">Electronic</span></span>  
13. <span data-ttu-id="8165f-276">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="8165f-276">Click Save.</span></span>
14. <span data-ttu-id="8165f-277">点击”生成付款“。</span><span class="sxs-lookup"><span data-stu-id="8165f-277">Click Generate payments.</span></span>
15. <span data-ttu-id="8165f-278">在“付款方式”字段中，键入“电子”。</span><span class="sxs-lookup"><span data-stu-id="8165f-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="8165f-279">电子</span><span class="sxs-lookup"><span data-stu-id="8165f-279">Electronic</span></span>  
16. <span data-ttu-id="8165f-280">在“文件名”字段中，键入“付款”。</span><span class="sxs-lookup"><span data-stu-id="8165f-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="8165f-281">例如，键入“付款”。</span><span class="sxs-lookup"><span data-stu-id="8165f-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="8165f-282">在“银行帐户”字段中，键入 'GBSI OPER'。</span><span class="sxs-lookup"><span data-stu-id="8165f-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="8165f-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="8165f-283">GBSI OPER</span></span>  
18. <span data-ttu-id="8165f-284">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8165f-284">Click OK.</span></span>
19. <span data-ttu-id="8165f-285">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8165f-285">Click OK.</span></span>
    * <span data-ttu-id="8165f-286">审查已创建的工作表，包括付款行详细信息以及用于此付款消息的每个币种代码的总计。</span><span class="sxs-lookup"><span data-stu-id="8165f-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  



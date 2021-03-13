---
title: ER 设计以 OPENXML 格式生成报表的配置（2016 年 11 月）
description: 本主题介绍如何创建一个新的电子报告配置，其中包含用于生成 OPENXML 格式的电子文档的模板。
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3b832961061d05e3f1ae046f820bc7a37baaf90c
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092658"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="56d70-103">ER 设计以 OPENXML 格式生成报表的配置（2016 年 11 月）</span><span class="sxs-lookup"><span data-stu-id="56d70-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="56d70-104">此主题介绍系统管理员或电子报表开发人员角色的用户如何创建新电子报表 (ER) 配置，使其包含用于生成 OPENXML 格式的电子文档的模板。</span><span class="sxs-lookup"><span data-stu-id="56d70-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="56d70-105">此配置将用于处理供应商付款。</span><span class="sxs-lookup"><span data-stu-id="56d70-105">This configuration will be used for processing vendor payments.</span></span>

<span data-ttu-id="56d70-106">在此示例中，您将创建示例公司 Litware 公司的配置。这些步骤可以在 GBSI 公司执行。</span><span class="sxs-lookup"><span data-stu-id="56d70-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>

<span data-ttu-id="56d70-107">为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="56d70-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="56d70-108">您还必须具有在创建模板时将导入的 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="56d70-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="56d70-109">可从[付款报表模板](https://go.microsoft.com/fwlink/?linkid=862266)访问此文件。</span><span class="sxs-lookup"><span data-stu-id="56d70-109">This file can be accessed from the [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="56d70-110">上载付款数据模型配置</span><span class="sxs-lookup"><span data-stu-id="56d70-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="56d70-111">在导航窗格中，转到 **模块 > 组织管理 > 工作区 > 电子申报**。</span><span class="sxs-lookup"><span data-stu-id="56d70-111">In the navigation pane, go to **Modules > Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="56d70-112">在列表中，标记示例公司“Litware 公司”的配置供应商。如果没有看到此配置供应商，您必须首先完成[创建配置提供程序并将其标记为有效](er-configuration-provider-mark-it-active-2016-11.md)这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="56d70-112">In the list, mark the configuration provider for sample company, Litware, Inc. If you don't see this configuration provider, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="56d70-113">选择 **设置有效**。</span><span class="sxs-lookup"><span data-stu-id="56d70-113">Select **Set active**.</span></span>
4. <span data-ttu-id="56d70-114">选择 **存储库**。</span><span class="sxs-lookup"><span data-stu-id="56d70-114">Select **Repositories**.</span></span> <span data-ttu-id="56d70-115">为运营资源类型选择存储库（如果有）。</span><span class="sxs-lookup"><span data-stu-id="56d70-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="56d70-116">如果可用，跳过有关创建新存储库的以下步骤。</span><span class="sxs-lookup"><span data-stu-id="56d70-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="56d70-117">选择 **添加** 以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="56d70-117">Select **Add** to open the drop dialog.</span></span>
6. <span data-ttu-id="56d70-118">在 **配置存储库类型** 字段中，输入 `Operations resourcesdd`。</span><span class="sxs-lookup"><span data-stu-id="56d70-118">In the **Configuration repository type** field, enter `Operations resourcesdd`.</span></span>
7. <span data-ttu-id="56d70-119">选择 **创建存储库**。</span><span class="sxs-lookup"><span data-stu-id="56d70-119">Select **Create repository**.</span></span>
8. <span data-ttu-id="56d70-120">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="56d70-120">Select **OK**.</span></span>
9. <span data-ttu-id="56d70-121">选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="56d70-121">Select **Open**.</span></span>
10. <span data-ttu-id="56d70-122">在树结构中，选择 **付款模型**。</span><span class="sxs-lookup"><span data-stu-id="56d70-122">In the tree, select **Payment model**.</span></span>
11. <span data-ttu-id="56d70-123">选择 **导入**。</span><span class="sxs-lookup"><span data-stu-id="56d70-123">Select **Import**.</span></span> <span data-ttu-id="56d70-124">导入此数据模型。</span><span class="sxs-lookup"><span data-stu-id="56d70-124">Import this data model.</span></span> <span data-ttu-id="56d70-125">将它用作新格式配置中的数据源。</span><span class="sxs-lookup"><span data-stu-id="56d70-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="56d70-126">如果已经导入了此配置则跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="56d70-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="56d70-127">选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="56d70-127">Select **Yes**.</span></span>
13. <span data-ttu-id="56d70-128">关闭此页面，直到返回到“电子申报”页面。</span><span class="sxs-lookup"><span data-stu-id="56d70-128">Close the pages until you return to the Electronic reporting page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="56d70-129">创建新的格式配置</span><span class="sxs-lookup"><span data-stu-id="56d70-129">Create a new format configuration</span></span>
1. <span data-ttu-id="56d70-130">选择 **申报配置**。</span><span class="sxs-lookup"><span data-stu-id="56d70-130">Select **Reporting configurations**.</span></span>
2. <span data-ttu-id="56d70-131">在树结构中，选择 **付款模型**。</span><span class="sxs-lookup"><span data-stu-id="56d70-131">In the tree, select **Payment model**.</span></span>
3. <span data-ttu-id="56d70-132">选择 **创建配置**，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="56d70-132">Select **Create configuration** to open the drop dialog.</span></span>
4. <span data-ttu-id="56d70-133">在 **新建** 字段中，输入 `Format based on data model PaymentModel`。</span><span class="sxs-lookup"><span data-stu-id="56d70-133">In the **New** field, enter `Format based on data model PaymentModel`.</span></span> <span data-ttu-id="56d70-134">创建一个基于 PaymentModel 数据模型的格式。</span><span class="sxs-lookup"><span data-stu-id="56d70-134">Create a format that is based on the PaymentModel data model.</span></span>
5. <span data-ttu-id="56d70-135">在 **名称** 字段中，键入 `Sample worksheet report`。</span><span class="sxs-lookup"><span data-stu-id="56d70-135">In the **Name** field, type `Sample worksheet report`.</span></span> <span data-ttu-id="56d70-136">示例工作表报表</span><span class="sxs-lookup"><span data-stu-id="56d70-136">Sample worksheet report</span></span>  
6. <span data-ttu-id="56d70-137">在 **描述** 字段中键入 `Sample worksheet report for vendors' payments`。</span><span class="sxs-lookup"><span data-stu-id="56d70-137">In the **Description** field, type `Sample worksheet report for vendors' payments`.</span></span> <span data-ttu-id="56d70-138">供应商付款的示例工作表报表。</span><span class="sxs-lookup"><span data-stu-id="56d70-138">Sample worksheet report for vendors' payments.</span></span>  
7. <span data-ttu-id="56d70-139">在 **数据模型定义** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="56d70-139">In the **Data model definition** field, enter or select a value.</span></span> <span data-ttu-id="56d70-140">选择 **CustomerCreditTransferInitiation** 定义。</span><span class="sxs-lookup"><span data-stu-id="56d70-140">Select the **CustomerCreditTransferInitiation** definition.</span></span>  
8. <span data-ttu-id="56d70-141">选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="56d70-141">Select **Create configuration**.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="56d70-142">以 OPENXML 工作表格式设计新文档</span><span class="sxs-lookup"><span data-stu-id="56d70-142">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="56d70-143">在树结构中，选择 **付款模型\示例工作表报表**。</span><span class="sxs-lookup"><span data-stu-id="56d70-143">In the tree, select **Payment model\Sample worksheet report**.</span></span>
2. <span data-ttu-id="56d70-144">选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="56d70-144">Select **Designer**.</span></span>
3. <span data-ttu-id="56d70-145">在操作窗格上，选择 **导入**。</span><span class="sxs-lookup"><span data-stu-id="56d70-145">On the Action Pane, select **Import**.</span></span>
4. <span data-ttu-id="56d70-146">选择 **从 Excel 导入**。</span><span class="sxs-lookup"><span data-stu-id="56d70-146">Select **Import from Excel**.</span></span>
5. <span data-ttu-id="56d70-147">选择 **附件**。</span><span class="sxs-lookup"><span data-stu-id="56d70-147">Select **Attachments**.</span></span> <span data-ttu-id="56d70-148">作为模板附加现有 Excel 文档。</span><span class="sxs-lookup"><span data-stu-id="56d70-148">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="56d70-149">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="56d70-149">Select **New**.</span></span>
7. <span data-ttu-id="56d70-150">选择 **文件**。</span><span class="sxs-lookup"><span data-stu-id="56d70-150">Select **File**.</span></span> <span data-ttu-id="56d70-151">指向现有 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="56d70-151">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="56d70-152">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="56d70-152">Close the page.</span></span>
9. <span data-ttu-id="56d70-153">在 **模板** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="56d70-153">In the **Template** field, enter or select a value.</span></span> <span data-ttu-id="56d70-154">选择用作模板的附加的 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="56d70-154">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="56d70-155">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="56d70-155">Select **OK**.</span></span> <span data-ttu-id="56d70-156">请注意，ER 格式组件已基于引用 MS Excel 文档的结构以设计格式创建（指定范围）。</span><span class="sxs-lookup"><span data-stu-id="56d70-156">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="56d70-157">创建新的数据源以按币种代码计算总计</span><span class="sxs-lookup"><span data-stu-id="56d70-157">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="56d70-158">选择 **映射** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="56d70-158">Select the **Mapping** tab.</span></span>
2. <span data-ttu-id="56d70-159">选择 **添加根** 以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="56d70-159">Select **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="56d70-160">在树结构中，选择 **功能\分组依据**。</span><span class="sxs-lookup"><span data-stu-id="56d70-160">In the tree, select **Functions\Group by**.</span></span>
4. <span data-ttu-id="56d70-161">在 **名称** 字段中，键入 `PaymentByCurrency`。</span><span class="sxs-lookup"><span data-stu-id="56d70-161">In the **Name** field, type `PaymentByCurrency`.</span></span>
5. <span data-ttu-id="56d70-162">选择 **编辑分组依据**。</span><span class="sxs-lookup"><span data-stu-id="56d70-162">Select **Edit group by**.</span></span>
6. <span data-ttu-id="56d70-163">在树中，展开 **模型**，然后选择 **模型\付款**。</span><span class="sxs-lookup"><span data-stu-id="56d70-163">In the tree, expand **model**, then select **model\Payments**.</span></span>
7. <span data-ttu-id="56d70-164">选择 **将字段添加到**。</span><span class="sxs-lookup"><span data-stu-id="56d70-164">Select **Add field to**.</span></span>
8. <span data-ttu-id="56d70-165">选择 **什么要分组**。</span><span class="sxs-lookup"><span data-stu-id="56d70-165">Select **What to group**.</span></span>
9. <span data-ttu-id="56d70-166">在树中，展开 **模型\付款**，然后选择 **模型\付款\货币**。</span><span class="sxs-lookup"><span data-stu-id="56d70-166">In the tree, expand **model\Payments**, then select **model\Payments\Currency**.</span></span>
10. <span data-ttu-id="56d70-167">选择 **将字段添加到**。</span><span class="sxs-lookup"><span data-stu-id="56d70-167">Select **Add field to**.</span></span>
11. <span data-ttu-id="56d70-168">选择 **分组字段**。</span><span class="sxs-lookup"><span data-stu-id="56d70-168">Select **Grouped fields**.</span></span>
12. <span data-ttu-id="56d70-169">在树结构中，选择 **模型\付款\指示金额(InstructedAmount)**。</span><span class="sxs-lookup"><span data-stu-id="56d70-169">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)**.</span></span>
13. <span data-ttu-id="56d70-170">选择 **将字段添加到**，然后选择 **合并字段**。</span><span class="sxs-lookup"><span data-stu-id="56d70-170">Select **Add field to**, then select **Aggregation fields**.</span></span>
14. <span data-ttu-id="56d70-171">在 **方法** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="56d70-171">In the **Method** field, select an option.</span></span> <span data-ttu-id="56d70-172">选择 **SUM 合并** 功能。</span><span class="sxs-lookup"><span data-stu-id="56d70-172">Select the **SUM aggregation** function.</span></span>  
15. <span data-ttu-id="56d70-173">在 **名称** 字段中，键入 `TotalInstructuredAmount`。</span><span class="sxs-lookup"><span data-stu-id="56d70-173">In the **Name** field, type `TotalInstructuredAmount`.</span></span>
16. <span data-ttu-id="56d70-174">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="56d70-174">Select **Save**.</span></span>
17. <span data-ttu-id="56d70-175">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="56d70-175">Close the page.</span></span>
18. <span data-ttu-id="56d70-176">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="56d70-176">Select **OK**.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="56d70-177">将格式组件映射到数据源</span><span class="sxs-lookup"><span data-stu-id="56d70-177">Map format components to data sources</span></span>
1. <span data-ttu-id="56d70-178">在树结构中，选择 **模型\付款\发起方(InitiatingParty)\名称** 和 **Excel\ReportHeader\CompanyName**。</span><span class="sxs-lookup"><span data-stu-id="56d70-178">In the tree, select **model\Payments\Initiating Party(InitiatingParty)\Name** and **Excel\ReportHeader\CompanyName**.</span></span>
2. <span data-ttu-id="56d70-179">选择 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="56d70-179">Select **Bind**.</span></span>
3. <span data-ttu-id="56d70-180">在树结构中，选择 **模型\付款\贷方\身份证明\源 ID(SourceID)** 和 **Excel\PaymLines\VendAccountName**。</span><span class="sxs-lookup"><span data-stu-id="56d70-180">In the tree, select **model\Payments\Creditor\Identification\Source ID(SourceID)** and **Excel\PaymLines\VendAccountName**.</span></span>
4. <span data-ttu-id="56d70-181">选择 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="56d70-181">Select **Bind**.</span></span>
5. <span data-ttu-id="56d70-182">在树中，选择 **模型\付款\贷方\名称** 和 **Excel\PaymLines\VendName**。</span><span class="sxs-lookup"><span data-stu-id="56d70-182">In the tree, select **model\Payments\Creditor\Name** and **Excel\PaymLines\VendName**.</span></span>
6. <span data-ttu-id="56d70-183">选择 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="56d70-183">Select **Bind**.</span></span>
7. <span data-ttu-id="56d70-184">在树中，选择 **模型\付款\贷方代理(CreditorAgent)\名称** 和 **Excel\PaymLines\银行**。</span><span class="sxs-lookup"><span data-stu-id="56d70-184">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Name** and **Excel\PaymLines\Bank**.</span></span>
8. <span data-ttu-id="56d70-185">选择 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="56d70-185">Select **Bind**.</span></span>
9. <span data-ttu-id="56d70-186">在树中，选择 **模型\付款\贷方代理(CreditorAgent)\银行代号(RoutingNumber)** 和 **Excel\PaymLines\RoutingNumber**。</span><span class="sxs-lookup"><span data-stu-id="56d70-186">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** and **Excel\PaymLines\RoutingNumber**.</span></span>
10. <span data-ttu-id="56d70-187">选择 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="56d70-187">Select **Bind**.</span></span>
11. <span data-ttu-id="56d70-188">在树结构中，选择 **模型\付款\贷方帐号(CreditorAccount)\证件\编号** 和 **Excel\PaymLines\VendAccountName**。</span><span class="sxs-lookup"><span data-stu-id="56d70-188">In the tree, select **model\Payments\Creditor Account(CreditorAccount)\Identification\Number** and **Excel\PaymLines\AccountNumber**.</span></span>
12. <span data-ttu-id="56d70-189">选择 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="56d70-189">Select **Bind**.</span></span>
13. <span data-ttu-id="56d70-190">在树结构中，选择 **模型\付款\指示金额(InstructedAmount)** 和 **Excel\PaymLines\Debit**。</span><span class="sxs-lookup"><span data-stu-id="56d70-190">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)** and **Excel\PaymLines\Debit**.</span></span>
14. <span data-ttu-id="56d70-191">选择 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="56d70-191">Select **Bind**.</span></span>
15. <span data-ttu-id="56d70-192">在树中，选择 **模型\付款\货币** 和 **Excel\PaymLines\货币**。</span><span class="sxs-lookup"><span data-stu-id="56d70-192">In the tree, select **model\Payments\Currency** and **Excel\PaymLines\Currency**.</span></span>
16. <span data-ttu-id="56d70-193">选择 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="56d70-193">Select **Bind**.</span></span>
17. <span data-ttu-id="56d70-194">在树中，选择 **PaymentByCurrency\grouped\Currency** 和 **Excel\SummaryLines\SummaryCurrency**。</span><span class="sxs-lookup"><span data-stu-id="56d70-194">In the tree, select **PaymentByCurrency\grouped\Currency** and **Excel\SummaryLines\SummaryCurrency**.</span></span>
18. <span data-ttu-id="56d70-195">选择 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="56d70-195">Select **Bind**.</span></span>
19. <span data-ttu-id="56d70-196">在树中，选择 **PaymentByCurrency\aggregated\TotalInstructuredAmount** 和 **Excel\SummaryLines\SummaryAmount**。</span><span class="sxs-lookup"><span data-stu-id="56d70-196">In the tree, select **PaymentByCurrency\aggregated\TotalInstructuredAmount** and **Excel\SummaryLines\SummaryAmount**.</span></span>
20. <span data-ttu-id="56d70-197">选择 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="56d70-197">Select **Bind**.</span></span>
21. <span data-ttu-id="56d70-198">在树中，选择 **PaymentByCurrency** 和 **Excel\SummaryLines**。</span><span class="sxs-lookup"><span data-stu-id="56d70-198">In the tree, select **PaymentByCurrency** and **Excel\SummaryLines**.</span></span>
22. <span data-ttu-id="56d70-199">选择 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="56d70-199">Select **Bind**.</span></span>
23. <span data-ttu-id="56d70-200">在树中，选择 **模型\付款** 和 **Excel\PaymLines**。</span><span class="sxs-lookup"><span data-stu-id="56d70-200">In the tree, select **model\Payments** and **Excel\PaymLines**.</span></span>
24. <span data-ttu-id="56d70-201">选择 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="56d70-201">Select **Bind**.</span></span>
25. <span data-ttu-id="56d70-202">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="56d70-202">Select **Save**, then close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="56d70-203">将创建的配置用于处理付款</span><span class="sxs-lookup"><span data-stu-id="56d70-203">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="56d70-204">选择 **更改状态**。</span><span class="sxs-lookup"><span data-stu-id="56d70-204">Select **Change status**.</span></span>
2. <span data-ttu-id="56d70-205">选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="56d70-205">Select **Complete**.</span></span>
3. <span data-ttu-id="56d70-206">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="56d70-206">Select **OK**.</span></span>
4. <span data-ttu-id="56d70-207">在导航窗格中，转到 **模块 > 应付帐款 > 付款设置 > 付款方式**。</span><span class="sxs-lookup"><span data-stu-id="56d70-207">In the navigation pane, go to **Modules > Accounts payable > Payment setup > Methods of payment**.</span></span>
5. <span data-ttu-id="56d70-208">使用快速筛选来筛选带 **电子** 值的 **付款方式** 字段。</span><span class="sxs-lookup"><span data-stu-id="56d70-208">Use the Quick Filter to filter on the **Method of payment** field with a value of **Electronic**.</span></span>
6. <span data-ttu-id="56d70-209">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="56d70-209">Select **Edit**.</span></span>
7. <span data-ttu-id="56d70-210">展开 **文件格式** 部分。</span><span class="sxs-lookup"><span data-stu-id="56d70-210">Expand the **File formats** section.</span></span>
8. <span data-ttu-id="56d70-211">在 **普通电子申报** 字段中，选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="56d70-211">Select **Yes** in the **Generic electronic reporting** field.</span></span>
9. <span data-ttu-id="56d70-212">在 **导出格式配置** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="56d70-212">In the **Export format configuration** field, enter or select a value.</span></span> <span data-ttu-id="56d70-213">选择 **示例工作表报表** 配置。</span><span class="sxs-lookup"><span data-stu-id="56d70-213">Select the **Sample worksheet report** configuration.</span></span>  
10. <span data-ttu-id="56d70-214">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="56d70-214">Select **Save**.</span></span>
11. <span data-ttu-id="56d70-215">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="56d70-215">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="56d70-216">使用创建的配置进行付款日记帐处理测试</span><span class="sxs-lookup"><span data-stu-id="56d70-216">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="56d70-217">在导航窗格中，转到 **模块 > 应付帐款 > 付款 > 付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="56d70-217">In the navigation pane, go to **Modules > Accounts payable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="56d70-218">选择 **新建** 以创建新付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="56d70-218">Select **New** to create a new payment journal.</span></span>
3. <span data-ttu-id="56d70-219">在 **名称** 字段中，键入 **VendPay**。</span><span class="sxs-lookup"><span data-stu-id="56d70-219">In the **Name** field, type **VendPay**.</span></span>
4. <span data-ttu-id="56d70-220">选择 **行**。</span><span class="sxs-lookup"><span data-stu-id="56d70-220">Select **Lines**.</span></span>
5. <span data-ttu-id="56d70-221">在 **帐户** 字段中，指定值 `GB_SI_000001`。</span><span class="sxs-lookup"><span data-stu-id="56d70-221">In the **Account** field, specify the values `GB_SI_000001`.</span></span>
6. <span data-ttu-id="56d70-222">将 **借方** 设置为 `1000`。</span><span class="sxs-lookup"><span data-stu-id="56d70-222">Set **Debit** to `1000`.</span></span>
7. <span data-ttu-id="56d70-223">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="56d70-223">Select **New**.</span></span>
8. <span data-ttu-id="56d70-224">在 **帐户** 字段中，指定值 `GB_SI_000005`。</span><span class="sxs-lookup"><span data-stu-id="56d70-224">In the **Account** field, specify the values `GB_SI_000005`.</span></span>
9. <span data-ttu-id="56d70-225">将 **借方** 设置为 `2000`。</span><span class="sxs-lookup"><span data-stu-id="56d70-225">Set **Debit** to `2000`.</span></span>
10. <span data-ttu-id="56d70-226">在 **货币** 字段中，键入 `EUR`。</span><span class="sxs-lookup"><span data-stu-id="56d70-226">In the **Currency** field, type `EUR`.</span></span>
11. <span data-ttu-id="56d70-227">在 **抵消帐户** 字段中，指定值 `GBSI OPER`。</span><span class="sxs-lookup"><span data-stu-id="56d70-227">In the **Offset account** field, specify the values `GBSI OPER`.</span></span>
12. <span data-ttu-id="56d70-228">在 **付款方式** 字段中，键入 `Electronic`。</span><span class="sxs-lookup"><span data-stu-id="56d70-228">In the **Method of payment** field, type `Electronic`.</span></span>
13. <span data-ttu-id="56d70-229">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="56d70-229">Select **Save**.</span></span>
14. <span data-ttu-id="56d70-230">选择 **生成付款**。</span><span class="sxs-lookup"><span data-stu-id="56d70-230">Select **Generate payments**.</span></span>
15. <span data-ttu-id="56d70-231">在 **付款方式** 字段中，键入 `Electronic`。</span><span class="sxs-lookup"><span data-stu-id="56d70-231">In the **Method of payment** field, type `Electronic`.</span></span>
16. <span data-ttu-id="56d70-232">在 **文件名** 字段中，键入 `Payments`。</span><span class="sxs-lookup"><span data-stu-id="56d70-232">In the **File name** field, type `Payments`.</span></span>
17. <span data-ttu-id="56d70-233">在 **银行帐户** 字段中，键入 `GBSI OPER`。</span><span class="sxs-lookup"><span data-stu-id="56d70-233">In the **Bank account** field, type `GBSI OPER`.</span></span>
18. <span data-ttu-id="56d70-234">选择 **确定**，然后再次选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="56d70-234">Select **OK**, then select **OK** again.</span></span> <span data-ttu-id="56d70-235">审查已创建的工作表，包括付款行详细信息以及用于此付款消息的每个币种代码的总计。</span><span class="sxs-lookup"><span data-stu-id="56d70-235">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


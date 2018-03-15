--- 
title: "设计表达式以调用应用类方法 (ER)"
description: "本指南提供有关如何通过在 ER 表达式中调用必需的应用类方法来在电子报告 (ER) 配置中重用现有应用逻辑的信息。"
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: b0a1dba5afbd7beba45149340f637223f6ecedcf
ms.contentlocale: zh-cn
ms.lasthandoff: 02/07/2018

---
# <a name="design-expressions-to-call-application-class-methods-er"></a><span data-ttu-id="edd16-103">设计表达式以调用应用类方法 (ER)</span><span class="sxs-lookup"><span data-stu-id="edd16-103">Design expressions to call application class methods (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="edd16-104">本指南提供有关如何通过在 ER 表达式中调用必需的应用类方法来在电子报告 (ER) 配置中重用现有应用逻辑的信息。</span><span class="sxs-lookup"><span data-stu-id="edd16-104">This guide provides information about how to reuse the existing application logic in Electronic reporting (ER) configurations by calling required methods of application classes in ER expressions.</span></span> <span data-ttu-id="edd16-105">用于调用类的参数值可以在运行时动态定义：例如，根据分析文档中的信息确保其正确性。</span><span class="sxs-lookup"><span data-stu-id="edd16-105">Values of arguments for calling classes can be defined dynamically at run-time: for example, based on information in the parsing document to ensure its correctness.</span></span> <span data-ttu-id="edd16-106">在此指南中，将为示例公司 Litware 公司创建所需 ER 配置。此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。</span><span class="sxs-lookup"><span data-stu-id="edd16-106">In this guide, you will create the required ER configurations for the sample company, Litware, Inc. This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> 

<span data-ttu-id="edd16-107">可使用任何数据集完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="edd16-107">These steps can be completed using any data set.</span></span> <span data-ttu-id="edd16-108">您还必须下载并在本地保存以下文件：(https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt。</span><span class="sxs-lookup"><span data-stu-id="edd16-108">You must also download and save the following file locally: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span></span>

<span data-ttu-id="edd16-109">为了完成这些步骤，您必须首先完成“ER 创建配置提供商并标记为有效”这一过程。</span><span class="sxs-lookup"><span data-stu-id="edd16-109">To complete these steps, you must first complete the steps in the procedure, “ER Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="edd16-110">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="edd16-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="edd16-111">验证示例公司 Litware 公司的配置提供程序可用且标记为有效。</span><span class="sxs-lookup"><span data-stu-id="edd16-111">Verify that the configuration provider for sample company, Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="edd16-112">如果没有看到此配置提供程序，您必须首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="edd16-112">If you don’t see this configuration provider, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>   
    * <span data-ttu-id="edd16-113">我们假定您设计一个流程，用于分析传入的银行对帐单以进行应用程序数据更新。</span><span class="sxs-lookup"><span data-stu-id="edd16-113">Let’s assume that you are designing a process for parsing incoming bank statements for an application data update.</span></span> <span data-ttu-id="edd16-114">您将以包含 IBAN 代码的 TXT 文件形式收到传入的银行对帐单。</span><span class="sxs-lookup"><span data-stu-id="edd16-114">You will receive the incoming bank statements as TXT files that contain IBAN codes.</span></span> <span data-ttu-id="edd16-115">作为银行对帐单导入过程的一部分，您需要使用 Dynamics 365 for Finance and Operations, Enterprise edition 中已经提供的逻辑验证此 IBAN 代码的更正。</span><span class="sxs-lookup"><span data-stu-id="edd16-115">As part of the bank statement import process, you need to validate the correctness of this IBAN codes using the logic that is already available in Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>   

## <a name="import-a-new-er-model-configuration"></a><span data-ttu-id="edd16-116">导入新 ER 模型配置</span><span class="sxs-lookup"><span data-stu-id="edd16-116">Import a new ER model configuration</span></span>
1. <span data-ttu-id="edd16-117">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="edd16-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="edd16-118">选择 Microsoft 提供程序磁贴。</span><span class="sxs-lookup"><span data-stu-id="edd16-118">Select the Microsoft provider tile.</span></span>  
2. <span data-ttu-id="edd16-119">单击“存储库”。</span><span class="sxs-lookup"><span data-stu-id="edd16-119">Click Repositories.</span></span>
3. <span data-ttu-id="edd16-120">单击“显示筛选器”。</span><span class="sxs-lookup"><span data-stu-id="edd16-120">Click Show filters.</span></span>
4. <span data-ttu-id="edd16-121">添加筛选器字段“类型名称”。</span><span class="sxs-lookup"><span data-stu-id="edd16-121">Add a filter field ‘Type name’.</span></span> <span data-ttu-id="edd16-122">在“名称”字段中，输入值“资源”，选择“包含”筛选器运算符，然后单击“应用”。</span><span class="sxs-lookup"><span data-stu-id="edd16-122">In the Name field, enter the value “resources”, select the “contains” filter operator, and then click Apply.</span></span>
5. <span data-ttu-id="edd16-123">单击“打开”。</span><span class="sxs-lookup"><span data-stu-id="edd16-123">Click Open.</span></span>
6. <span data-ttu-id="edd16-124">在树结构中，选择“付款模型”。</span><span class="sxs-lookup"><span data-stu-id="edd16-124">In the tree, select 'Payment model'.</span></span>
    * <span data-ttu-id="edd16-125">如果“版本”快速选项卡上的“导入”按钮未启用，说明您已导入了一个 ER 配置“付款模型”的版本 1。</span><span class="sxs-lookup"><span data-stu-id="edd16-125">If the Import button on the Versions FastTab is not enabled, you have already imported the version 1 one of the ER configuration ‘Payment model’.</span></span> <span data-ttu-id="edd16-126">您可以跳过此子任务的其余步骤。</span><span class="sxs-lookup"><span data-stu-id="edd16-126">You can skip the rest steps in this sub-task.</span></span>   
7. <span data-ttu-id="edd16-127">单击“导入”。</span><span class="sxs-lookup"><span data-stu-id="edd16-127">Click Import.</span></span>
8. <span data-ttu-id="edd16-128">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="edd16-128">Click Yes.</span></span>
9. <span data-ttu-id="edd16-129">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="edd16-129">Close the page.</span></span>
10. <span data-ttu-id="edd16-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="edd16-130">Close the page.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="edd16-131">添加新 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="edd16-131">Add a new ER format configuration</span></span>
1. <span data-ttu-id="edd16-132">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="edd16-132">Click Reporting configurations.</span></span>
    * <span data-ttu-id="edd16-133">添加新的 ER 格式来分析 TXT 格式的传入银行对帐单。</span><span class="sxs-lookup"><span data-stu-id="edd16-133">Add a new ER format to parse incoming bank statements in TXT format.</span></span>  
2. <span data-ttu-id="edd16-134">在树结构中，选择“付款模型”。</span><span class="sxs-lookup"><span data-stu-id="edd16-134">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="edd16-135">单击“创建配置”，以打开对话框菜单。</span><span class="sxs-lookup"><span data-stu-id="edd16-135">Click Create configuration to open the dialog menu.</span></span>
4. <span data-ttu-id="edd16-136">在“新建”字段中，输入“基于数据模型付款模型的格式”。</span><span class="sxs-lookup"><span data-stu-id="edd16-136">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
5. <span data-ttu-id="edd16-137">在“名称”字段中，键入“银行对帐单导入格式（示例）”。</span><span class="sxs-lookup"><span data-stu-id="edd16-137">In the Name field, type 'Bank statement import format (sample)'.</span></span>
    * <span data-ttu-id="edd16-138">银行对帐单的导入格式（示例）</span><span class="sxs-lookup"><span data-stu-id="edd16-138">Bank statement import format (sample)</span></span>  
6. <span data-ttu-id="edd16-139">在“支持数据导入”字段中选择"是"。</span><span class="sxs-lookup"><span data-stu-id="edd16-139">Select Yes in the Supports data import field.</span></span>
7. <span data-ttu-id="edd16-140">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="edd16-140">Click Create configuration.</span></span>

## <a name="design-the-er-format-configuration---format"></a><span data-ttu-id="edd16-141">设计 ER 格式配置 - 格式</span><span class="sxs-lookup"><span data-stu-id="edd16-141">Design the ER format configuration - format</span></span>
1. <span data-ttu-id="edd16-142">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="edd16-142">Click Designer.</span></span>
    * <span data-ttu-id="edd16-143">设计的格式表示 TXT 格式的外部文件的预期结构。</span><span class="sxs-lookup"><span data-stu-id="edd16-143">The designed format represents the expected structure of the external file in TXT format.</span></span>  
2. <span data-ttu-id="edd16-144">单击“添加根”以打开对话框菜单。</span><span class="sxs-lookup"><span data-stu-id="edd16-144">Click Add root to open the dialog menu.</span></span>
3. <span data-ttu-id="edd16-145">在树中，选择“文本\序列”。</span><span class="sxs-lookup"><span data-stu-id="edd16-145">In the tree, select 'Text\Sequence'.</span></span>
4. <span data-ttu-id="edd16-146">在“名称”字段中，键入“根”。</span><span class="sxs-lookup"><span data-stu-id="edd16-146">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="edd16-147">根</span><span class="sxs-lookup"><span data-stu-id="edd16-147">Root</span></span>  
5. <span data-ttu-id="edd16-148">在"特殊字符"字段中，选择“换行 - Windows (CR LF)”。</span><span class="sxs-lookup"><span data-stu-id="edd16-148">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
    * <span data-ttu-id="edd16-149">已在“特殊字符”字段中选择选项“新行 - Windows (CR LF)”。</span><span class="sxs-lookup"><span data-stu-id="edd16-149">The option ‘New line - Windows (CR LF)’ has been selected in the ‘Special characters’ field.</span></span> <span data-ttu-id="edd16-150">基于此设置，分析文件中的每一行均被视为单独的记录。</span><span class="sxs-lookup"><span data-stu-id="edd16-150">Based on this setting, each line in the parsing file is considered a separate record.</span></span>  
6. <span data-ttu-id="edd16-151">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="edd16-151">Click OK.</span></span>
7. <span data-ttu-id="edd16-152">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="edd16-152">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="edd16-153">在树中，选择“文本\序列”。</span><span class="sxs-lookup"><span data-stu-id="edd16-153">In the tree, select 'Text\Sequence'.</span></span>
9. <span data-ttu-id="edd16-154">在“名称”字段中键入“Rows”。</span><span class="sxs-lookup"><span data-stu-id="edd16-154">In the Name field, type 'Rows'.</span></span>
    * <span data-ttu-id="edd16-155">行</span><span class="sxs-lookup"><span data-stu-id="edd16-155">Rows</span></span>  
10. <span data-ttu-id="edd16-156">在“多样性”字段中，选择“一个 多个”。</span><span class="sxs-lookup"><span data-stu-id="edd16-156">In the Multiplicity field, select 'One many'.</span></span>
    * <span data-ttu-id="edd16-157">已选择“多样性”字段中的选项“一个 多个”。</span><span class="sxs-lookup"><span data-stu-id="edd16-157">The option ‘One many’ has been selected in the ‘Multiplicity’ field.</span></span> <span data-ttu-id="edd16-158">基于此设置，应该至少在分析文件中存在一个行。</span><span class="sxs-lookup"><span data-stu-id="edd16-158">Based on this setting, it is expected that at least one line will be presented in the parsing file.</span></span>  
11. <span data-ttu-id="edd16-159">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="edd16-159">Click OK.</span></span>
12. <span data-ttu-id="edd16-160">在树中，选择“Root\Rows”。</span><span class="sxs-lookup"><span data-stu-id="edd16-160">In the tree, select 'Root\Rows'.</span></span>
13. <span data-ttu-id="edd16-161">单击“添加序列”。</span><span class="sxs-lookup"><span data-stu-id="edd16-161">Click Add Sequence.</span></span>
14. <span data-ttu-id="edd16-162">在“名称”字段中，键入“Fields”。</span><span class="sxs-lookup"><span data-stu-id="edd16-162">In the Name field, type 'Fields'.</span></span>
    * <span data-ttu-id="edd16-163">字段</span><span class="sxs-lookup"><span data-stu-id="edd16-163">Fields</span></span>  
15. <span data-ttu-id="edd16-164">在“多样性”字段中，选择“正好一个”。</span><span class="sxs-lookup"><span data-stu-id="edd16-164">In the Multiplicity field, select 'Exactly one'.</span></span>
16. <span data-ttu-id="edd16-165">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="edd16-165">Click OK.</span></span>
17. <span data-ttu-id="edd16-166">在树中，选择“Root\Rows\Fields”。</span><span class="sxs-lookup"><span data-stu-id="edd16-166">In the tree, select 'Root\Rows\Fields'.</span></span>
18. <span data-ttu-id="edd16-167">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="edd16-167">Click Add to open the drop dialog.</span></span>
19. <span data-ttu-id="edd16-168">在树结构中，选择“文本\字符串”。</span><span class="sxs-lookup"><span data-stu-id="edd16-168">In the tree, select 'Text\String'.</span></span>
20. <span data-ttu-id="edd16-169">在“名称”字段中，键入“IBAN”。</span><span class="sxs-lookup"><span data-stu-id="edd16-169">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="edd16-170">IBAN / 国际银行帐号</span><span class="sxs-lookup"><span data-stu-id="edd16-170">IBAN</span></span>  
21. <span data-ttu-id="edd16-171">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="edd16-171">Click OK.</span></span>
    * <span data-ttu-id="edd16-172">已配置为分析文件的每一行只包含一个 IBAN 代码。</span><span class="sxs-lookup"><span data-stu-id="edd16-172">It has been configured that each line in the parsing file contains the only IBAN code.</span></span>  
22. <span data-ttu-id="edd16-173">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="edd16-173">Click Save.</span></span>

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a><span data-ttu-id="edd16-174">设计 ER 格式配置 – 数据模型映射</span><span class="sxs-lookup"><span data-stu-id="edd16-174">Design the ER format configuration – mapping to data model</span></span>
1. <span data-ttu-id="edd16-175">单击”将格式映射到模型“。</span><span class="sxs-lookup"><span data-stu-id="edd16-175">Click Map format to model.</span></span>
2. <span data-ttu-id="edd16-176">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="edd16-176">Click New.</span></span>
3. <span data-ttu-id="edd16-177">在“定义”字段中，键入“BankToCustomerDebitCreditNotificationInitiation”。</span><span class="sxs-lookup"><span data-stu-id="edd16-177">In the Definition field, type 'BankToCustomerDebitCreditNotificationInitiation'.</span></span>
    * <span data-ttu-id="edd16-178">BankToCustomerDebitCreditNotificationInitiation</span><span class="sxs-lookup"><span data-stu-id="edd16-178">BankToCustomerDebitCreditNotificationInitiation</span></span>  
4. <span data-ttu-id="edd16-179">改变定义。</span><span class="sxs-lookup"><span data-stu-id="edd16-179">ResolveChanges the Definition.</span></span>
5. <span data-ttu-id="edd16-180">在“名称”字段中，键入“数据模型映射”。</span><span class="sxs-lookup"><span data-stu-id="edd16-180">In the Name field, type 'Mapping to data model'.</span></span>
    * <span data-ttu-id="edd16-181">数据模型映射</span><span class="sxs-lookup"><span data-stu-id="edd16-181">Mapping to data model</span></span>  
6. <span data-ttu-id="edd16-182">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="edd16-182">Click Save.</span></span>
7. <span data-ttu-id="edd16-183">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="edd16-183">Click Designer.</span></span>
8. <span data-ttu-id="edd16-184">在树结构中，选择“Dynamics 365 for Operations\类”。</span><span class="sxs-lookup"><span data-stu-id="edd16-184">In the tree, select 'Dynamics 365 for Operations\Class'.</span></span>
9. <span data-ttu-id="edd16-185">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="edd16-185">Click Add root.</span></span>
    * <span data-ttu-id="edd16-186">添加新的数据源以调用 IBAN 代码验证使用的现有应用程序逻辑。</span><span class="sxs-lookup"><span data-stu-id="edd16-186">Add a new data source to call the existing application logic for IBAN codes validation.</span></span>  
10. <span data-ttu-id="edd16-187">在“名称”字段中，键入“check_codes”。</span><span class="sxs-lookup"><span data-stu-id="edd16-187">In the Name field, type 'check_codes'.</span></span>
    * <span data-ttu-id="edd16-188">check_codes</span><span class="sxs-lookup"><span data-stu-id="edd16-188">check_codes</span></span>  
11. <span data-ttu-id="edd16-189">在“类”字段中，键入“ISO7064”。</span><span class="sxs-lookup"><span data-stu-id="edd16-189">In the Class field, type 'ISO7064'.</span></span>
    * <span data-ttu-id="edd16-190">ISO7064</span><span class="sxs-lookup"><span data-stu-id="edd16-190">ISO7064</span></span>  
12. <span data-ttu-id="edd16-191">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="edd16-191">Click OK.</span></span>
13. <span data-ttu-id="edd16-192">在树中，展开“格式”。</span><span class="sxs-lookup"><span data-stu-id="edd16-192">In the tree, expand 'format'.</span></span>
14. <span data-ttu-id="edd16-193">在树中，展开“format\Root: Sequence(Root)”。</span><span class="sxs-lookup"><span data-stu-id="edd16-193">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
15. <span data-ttu-id="edd16-194">在树中，选择“format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)”。</span><span class="sxs-lookup"><span data-stu-id="edd16-194">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
16. <span data-ttu-id="edd16-195">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="edd16-195">Click Bind.</span></span>
17. <span data-ttu-id="edd16-196">在树中，展开“format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)”。</span><span class="sxs-lookup"><span data-stu-id="edd16-196">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
18. <span data-ttu-id="edd16-197">在树中，展开“format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)”。</span><span class="sxs-lookup"><span data-stu-id="edd16-197">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
19. <span data-ttu-id="edd16-198">在树中，选择“format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)”。</span><span class="sxs-lookup"><span data-stu-id="edd16-198">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
20. <span data-ttu-id="edd16-199">在树中，展开“付款 = format.Root.Rows”。</span><span class="sxs-lookup"><span data-stu-id="edd16-199">In the tree, expand 'Payments = format.Root.Rows'.</span></span>
21. <span data-ttu-id="edd16-200">在树结构中，展开“付款 = format.Root.Rows\Creditor Account(CreditorAccount)”。</span><span class="sxs-lookup"><span data-stu-id="edd16-200">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)'.</span></span>
22. <span data-ttu-id="edd16-201">在树结构中，展开“付款 = format.Root.Rows\Creditor Account(CreditorAccount)\Identification”。</span><span class="sxs-lookup"><span data-stu-id="edd16-201">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification'.</span></span>
23. <span data-ttu-id="edd16-202">在树中，选择“付款 = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN”。</span><span class="sxs-lookup"><span data-stu-id="edd16-202">In the tree, select 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN'.</span></span>
24. <span data-ttu-id="edd16-203">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="edd16-203">Click Bind.</span></span>
25. <span data-ttu-id="edd16-204">单击“验证”选项卡。</span><span class="sxs-lookup"><span data-stu-id="edd16-204">Click the Validations tab.</span></span>
26. <span data-ttu-id="edd16-205">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="edd16-205">Click New.</span></span>
    * <span data-ttu-id="edd16-206">增加新的验证规则，其显示包含无效的 IBAN 代码的分析文件中任何行的错误。</span><span class="sxs-lookup"><span data-stu-id="edd16-206">Add a new validation rule that displays an error for any line in the parsing file that contains invalid IBAN code.</span></span>  
27. <span data-ttu-id="edd16-207">单击“编辑条件”。</span><span class="sxs-lookup"><span data-stu-id="edd16-207">Click Edit condition.</span></span>
28. <span data-ttu-id="edd16-208">在树结构中，展开“check_codes”。</span><span class="sxs-lookup"><span data-stu-id="edd16-208">In the tree, expand 'check_codes'.</span></span>
29. <span data-ttu-id="edd16-209">在树中，选择“check_codes\verifyMOD1271_36”。</span><span class="sxs-lookup"><span data-stu-id="edd16-209">In the tree, select 'check_codes\verifyMOD1271_36'.</span></span>
30. <span data-ttu-id="edd16-210">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="edd16-210">Click Add data source.</span></span>
31. <span data-ttu-id="edd16-211">在“公式”字段中，输入“check_codes.verifyMOD1271_36(”。</span><span class="sxs-lookup"><span data-stu-id="edd16-211">In the Formula field, enter 'check_codes.verifyMOD1271_36('.</span></span>
    * <span data-ttu-id="edd16-212">check_codes.verifyMOD1271_36(</span><span class="sxs-lookup"><span data-stu-id="edd16-212">check_codes.verifyMOD1271_36(</span></span>  
32. <span data-ttu-id="edd16-213">在树中，展开“格式”。</span><span class="sxs-lookup"><span data-stu-id="edd16-213">In the tree, expand 'format'.</span></span>
33. <span data-ttu-id="edd16-214">在树中，展开“format\Root: Sequence(Root)”。</span><span class="sxs-lookup"><span data-stu-id="edd16-214">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
34. <span data-ttu-id="edd16-215">在树中，展开“format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)”。</span><span class="sxs-lookup"><span data-stu-id="edd16-215">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
35. <span data-ttu-id="edd16-216">在树中，展开“format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)”。</span><span class="sxs-lookup"><span data-stu-id="edd16-216">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
36. <span data-ttu-id="edd16-217">在树中，选择“format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)”。</span><span class="sxs-lookup"><span data-stu-id="edd16-217">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
37. <span data-ttu-id="edd16-218">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="edd16-218">Click Add data source.</span></span>
38. <span data-ttu-id="edd16-219">在“公式”字段中，输入“check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)”。</span><span class="sxs-lookup"><span data-stu-id="edd16-219">In the Formula field, enter 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="edd16-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="edd16-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span></span>  
39. <span data-ttu-id="edd16-221">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="edd16-221">Click Save.</span></span>
40. <span data-ttu-id="edd16-222">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="edd16-222">Close the page.</span></span>
    * <span data-ttu-id="edd16-223">验证条件已配置为通过调用应用程序类“ISO7064”的现有方法“verifyMOD1271_36”为任何无效的 IBAN 代码返回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="edd16-223">The validation condition has been configured to return FALSE for any invalid IBAN code by calling the existing method ‘verifyMOD1271_36’ of the application class ‘ISO7064’.</span></span> <span data-ttu-id="edd16-224">请注意，IBAN 代码的值在运行时被动态定义为基于分析 TXT 文件的内容调用方法的参数。</span><span class="sxs-lookup"><span data-stu-id="edd16-224">Note that the value of the IBAN code is defined dynamically at run-time as the argument of the calling method based on the content of the parsing TXT file.</span></span>   
41. <span data-ttu-id="edd16-225">单击“编辑消息”。</span><span class="sxs-lookup"><span data-stu-id="edd16-225">Click Edit message.</span></span>
42. <span data-ttu-id="edd16-226">在“公式”字段中，输入“CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)”。</span><span class="sxs-lookup"><span data-stu-id="edd16-226">In the Formula field, enter 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="edd16-227">CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="edd16-227">CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)</span></span>  
43. <span data-ttu-id="edd16-228">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="edd16-228">Click Save.</span></span>
44. <span data-ttu-id="edd16-229">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="edd16-229">Close the page.</span></span>
45. <span data-ttu-id="edd16-230">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="edd16-230">Click Save.</span></span>
46. <span data-ttu-id="edd16-231">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="edd16-231">Close the page.</span></span>

## <a name="run-the-format-mapping"></a><span data-ttu-id="edd16-232">运行格式映射</span><span class="sxs-lookup"><span data-stu-id="edd16-232">Run the format mapping</span></span>
<span data-ttu-id="edd16-233">为了测试，请使用以前下载的 SampleIncomingMessage.txt 文件执行格式映射。</span><span class="sxs-lookup"><span data-stu-id="edd16-233">For testing purposes, execute the format mapping using the SampleIncomingMessage.txt file that you downloaded.</span></span> <span data-ttu-id="edd16-234">生成的输出包含将从所选 TXT 文件导入，并在实际导入时填充到自定义数据模型的数据。</span><span class="sxs-lookup"><span data-stu-id="edd16-234">The generated output includes data that will be imported from the selected TXT file and populated to the custom data model during the real import.</span></span>   
1. <span data-ttu-id="edd16-235">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="edd16-235">Click Run.</span></span>
    * <span data-ttu-id="edd16-236">单击“浏览”并导航到前面下载的 SampleIncomingMessage.txt 文件。</span><span class="sxs-lookup"><span data-stu-id="edd16-236">Click Browse and navigate to the SampleIncomingMessage.txt file that you previously downloaded.</span></span>  
2. <span data-ttu-id="edd16-237">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="edd16-237">Click OK.</span></span>
    * <span data-ttu-id="edd16-238">检查 XML 格式的输出，该输出表示已从所选文件导入并移植到数据模型的数据。</span><span class="sxs-lookup"><span data-stu-id="edd16-238">Review the output in XML format that represents the data that has been imported from the selected file and ported to the data model.</span></span> <span data-ttu-id="edd16-239">请注意，导入的 TXT 文件只有 3 行被处理。</span><span class="sxs-lookup"><span data-stu-id="edd16-239">Note that only 3 lines of the imported TXT file were processed.</span></span> <span data-ttu-id="edd16-240">无效的第 4 行中的 IBAN 代码已跳过，并在信息日志中提供错误消息。</span><span class="sxs-lookup"><span data-stu-id="edd16-240">The IBAN code on line 4 that is not valid was skipped and an error message is provided in the Infolog.</span></span>  



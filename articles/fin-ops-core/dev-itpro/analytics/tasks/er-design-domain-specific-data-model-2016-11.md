---
title: ER 设计域特定数据模型
description: 以下步骤说明属于系统管理员或电子报表开发人员的用户如何创建新电子报表 (ER) 配置，使其包含电子付款文件中的数据模型。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 268f661079b80551b36ad2e1877615d878350051
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681941"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="ff385-103">ER 设计域特定数据模型</span><span class="sxs-lookup"><span data-stu-id="ff385-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff385-104">以下步骤说明属于系统管理员或电子报表开发人员的用户如何创建新电子报表 (ER) 配置，使其包含电子付款文件中的数据模型。</span><span class="sxs-lookup"><span data-stu-id="ff385-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="ff385-105">此数据模型稍后将用于您创建付款文件的格式时的数据源。</span><span class="sxs-lookup"><span data-stu-id="ff385-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="ff385-106">在此示例中，您将创建示例公司 Litware，Inc. 的配置。这些步骤可在任何公司执行，因为公司之间共享 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="ff385-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="ff385-107">为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="ff385-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="ff385-108">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="ff385-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="ff385-109">为示例公司“Litware 公司”选择配置提供程序。</span><span class="sxs-lookup"><span data-stu-id="ff385-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="ff385-110">如果没有看到此配置提供程序，您必须首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="ff385-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="ff385-111">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="ff385-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="ff385-112">您要创建含有电子付款文件的数据模型的模板。</span><span class="sxs-lookup"><span data-stu-id="ff385-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="ff385-113">此数据模型稍后将用于您创建付款文件的格式时的数据源。</span><span class="sxs-lookup"><span data-stu-id="ff385-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="ff385-114">创建新的数据模型配置</span><span class="sxs-lookup"><span data-stu-id="ff385-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="ff385-115">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="ff385-116">在“名称”字段中，键入“付款（简化模型）”。</span><span class="sxs-lookup"><span data-stu-id="ff385-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="ff385-117">在“描述”字段，键入“付款模式配置”。</span><span class="sxs-lookup"><span data-stu-id="ff385-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="ff385-118">有效配置提供商将自动在此输入。</span><span class="sxs-lookup"><span data-stu-id="ff385-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="ff385-119">此提供商可以维护此配置。</span><span class="sxs-lookup"><span data-stu-id="ff385-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="ff385-120">其他提供商可以使用此配置，但不能对其进行维护。</span><span class="sxs-lookup"><span data-stu-id="ff385-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="ff385-121">单击“创建配置”按钮以完成配置创建任务</span><span class="sxs-lookup"><span data-stu-id="ff385-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="ff385-122">创建数据模型</span><span class="sxs-lookup"><span data-stu-id="ff385-122">Create a data model</span></span>
<span data-ttu-id="ff385-123">您正在为所选配置创建新的数据模型。</span><span class="sxs-lookup"><span data-stu-id="ff385-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="ff385-124">此配置版本将为“草稿”状态。</span><span class="sxs-lookup"><span data-stu-id="ff385-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="ff385-125">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="ff385-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="ff385-126">定义参与付款流程的当事方的结构</span><span class="sxs-lookup"><span data-stu-id="ff385-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="ff385-127">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="ff385-128">在“名称”字段中，键入“当事方”。</span><span class="sxs-lookup"><span data-stu-id="ff385-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="ff385-129">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-129">Click Add.</span></span>
4. <span data-ttu-id="ff385-130">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="ff385-131">在“名称”字段中，键入“名称”。</span><span class="sxs-lookup"><span data-stu-id="ff385-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="ff385-132">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="ff385-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="ff385-133">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-133">Click Add.</span></span>
8. <span data-ttu-id="ff385-134">在“查找”字段中，键入“当事方”。</span><span class="sxs-lookup"><span data-stu-id="ff385-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="ff385-135">单击“查找上一个”。</span><span class="sxs-lookup"><span data-stu-id="ff385-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="ff385-136">定义此模型的银行结构</span><span class="sxs-lookup"><span data-stu-id="ff385-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="ff385-137">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="ff385-138">在“名称”字段中，键入“代理”。</span><span class="sxs-lookup"><span data-stu-id="ff385-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="ff385-139">在“物料类型”字段中，选择“记录”。</span><span class="sxs-lookup"><span data-stu-id="ff385-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="ff385-140">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-140">Click Add.</span></span>
5. <span data-ttu-id="ff385-141">在“描述”字段，输入“负责维护当事方（借方/贷方）帐户的金融机构（例如银行）”。</span><span class="sxs-lookup"><span data-stu-id="ff385-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="ff385-142">负责维护当事方（贷方/借方）帐户的金融机构（例如银行）。</span><span class="sxs-lookup"><span data-stu-id="ff385-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="ff385-143">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="ff385-144">在“名称”字段中，键入“名称”。</span><span class="sxs-lookup"><span data-stu-id="ff385-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="ff385-145">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="ff385-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="ff385-146">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-146">Click Add.</span></span>
10. <span data-ttu-id="ff385-147">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="ff385-148">在“名称”字段中，键入“SWIFT”。</span><span class="sxs-lookup"><span data-stu-id="ff385-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="ff385-149">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-149">Click Add.</span></span>
13. <span data-ttu-id="ff385-150">在“描述”字段中，输入“银行标识代码”。</span><span class="sxs-lookup"><span data-stu-id="ff385-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="ff385-151">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="ff385-152">在“名称”字段中，键入“银行代号”。</span><span class="sxs-lookup"><span data-stu-id="ff385-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="ff385-153">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-153">Click Add.</span></span>
17. <span data-ttu-id="ff385-154">在“描述”字段中，输入“银行代号”。</span><span class="sxs-lookup"><span data-stu-id="ff385-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="ff385-155">单击“查找上一个”。</span><span class="sxs-lookup"><span data-stu-id="ff385-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="ff385-156">定义此模型的银行帐户结构</span><span class="sxs-lookup"><span data-stu-id="ff385-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="ff385-157">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="ff385-158">在“名称”字段中，键入“帐户”。</span><span class="sxs-lookup"><span data-stu-id="ff385-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="ff385-159">在“物料类型”字段中，选择“记录”。</span><span class="sxs-lookup"><span data-stu-id="ff385-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="ff385-160">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-160">Click Add.</span></span>
5. <span data-ttu-id="ff385-161">在“描述”字段中，输入“当事方在金融机构（如银行）中的帐户的标识。”。</span><span class="sxs-lookup"><span data-stu-id="ff385-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="ff385-162">当事方在金融机构（如银行）中的帐户的标识。</span><span class="sxs-lookup"><span data-stu-id="ff385-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="ff385-163">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="ff385-164">在“名称”字段中，键入“货币”。</span><span class="sxs-lookup"><span data-stu-id="ff385-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="ff385-165">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="ff385-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="ff385-166">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-166">Click Add.</span></span>
10. <span data-ttu-id="ff385-167">在“描述”字段中，输入“货币代码”。</span><span class="sxs-lookup"><span data-stu-id="ff385-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="ff385-168">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="ff385-169">在“名称”字段中，键入“数字”。</span><span class="sxs-lookup"><span data-stu-id="ff385-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="ff385-170">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-170">Click Add.</span></span>
14. <span data-ttu-id="ff385-171">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="ff385-172">在“名称”字段中，键入“IBAN”。</span><span class="sxs-lookup"><span data-stu-id="ff385-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="ff385-173">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-173">Click Add.</span></span>
17. <span data-ttu-id="ff385-174">在“描述”字段中，输入“国际银行帐号”。</span><span class="sxs-lookup"><span data-stu-id="ff385-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="ff385-175">定义贷方转帐付款类型的付款消息结构</span><span class="sxs-lookup"><span data-stu-id="ff385-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="ff385-176">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="ff385-177">在“作为以下项的新节点”字段中，输入“模型根”。</span><span class="sxs-lookup"><span data-stu-id="ff385-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="ff385-178">在“名称”字段中，键入“客户贷方转帐发起”。</span><span class="sxs-lookup"><span data-stu-id="ff385-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="ff385-179">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-179">Click Add.</span></span>
5. <span data-ttu-id="ff385-180">在“查找”字段中，键入“客户贷方转帐发起”。</span><span class="sxs-lookup"><span data-stu-id="ff385-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="ff385-181">单击“查找上一个”。</span><span class="sxs-lookup"><span data-stu-id="ff385-181">Click Find previous.</span></span>
7. <span data-ttu-id="ff385-182">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="ff385-183">在“名称”字段中，键入“消息标识”。</span><span class="sxs-lookup"><span data-stu-id="ff385-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="ff385-184">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-184">Click Add.</span></span>
10. <span data-ttu-id="ff385-185">在“描述”字段，输入“由指示方分配（并发送给下一个当事方）以标识消息的点对点引用。”。</span><span class="sxs-lookup"><span data-stu-id="ff385-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="ff385-186">点对点引用由指示方分配（并发送给下一个当事方）以明确消息。</span><span class="sxs-lookup"><span data-stu-id="ff385-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="ff385-187">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="ff385-188">在“名称”字段中，键入“处理日期时间”“。</span><span class="sxs-lookup"><span data-stu-id="ff385-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="ff385-189">在“物料类型”字段中，选择“日期时间”。</span><span class="sxs-lookup"><span data-stu-id="ff385-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="ff385-190">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-190">Click Add.</span></span>
15. <span data-ttu-id="ff385-191">在“描述”字段中，输入“创建付款消息的日期和时间。”。</span><span class="sxs-lookup"><span data-stu-id="ff385-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="ff385-192">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="ff385-193">定义此模型的付款交易结构。</span><span class="sxs-lookup"><span data-stu-id="ff385-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="ff385-194">在“名称”字段中，键入“付款”。</span><span class="sxs-lookup"><span data-stu-id="ff385-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="ff385-195">在“物料类型”字段中，选择“记录列表”。</span><span class="sxs-lookup"><span data-stu-id="ff385-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="ff385-196">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-196">Click Add.</span></span>
20. <span data-ttu-id="ff385-197">在“描述”字段中，输入“当前消息付款行”。</span><span class="sxs-lookup"><span data-stu-id="ff385-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="ff385-198">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="ff385-199">在“名称”字段中，键入“贷方”。</span><span class="sxs-lookup"><span data-stu-id="ff385-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="ff385-200">在“物料类型”字段中，选择“记录”。</span><span class="sxs-lookup"><span data-stu-id="ff385-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="ff385-201">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-201">Click Add.</span></span>
25. <span data-ttu-id="ff385-202">在“描述”字段中，输入“应将金额支付给的当事方。”。</span><span class="sxs-lookup"><span data-stu-id="ff385-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="ff385-203">单击“切换项引用”。</span><span class="sxs-lookup"><span data-stu-id="ff385-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="ff385-204">在“查找”字段中，键入“当事方”。</span><span class="sxs-lookup"><span data-stu-id="ff385-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="ff385-205">单击“查找下一个”。</span><span class="sxs-lookup"><span data-stu-id="ff385-205">Click Find next.</span></span>
29. <span data-ttu-id="ff385-206">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ff385-206">Click OK.</span></span>
30. <span data-ttu-id="ff385-207">在“查找”字段中，键入“付款”。</span><span class="sxs-lookup"><span data-stu-id="ff385-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="ff385-208">单击“查找下一个”。</span><span class="sxs-lookup"><span data-stu-id="ff385-208">Click Find next.</span></span>
32. <span data-ttu-id="ff385-209">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="ff385-210">在“名称”字段中，键入“借方”。</span><span class="sxs-lookup"><span data-stu-id="ff385-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="ff385-211">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-211">Click Add.</span></span>
35. <span data-ttu-id="ff385-212">在“描述”字段，输入“欠(最终)贷方款项的当事方。”。</span><span class="sxs-lookup"><span data-stu-id="ff385-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="ff385-213">单击“切换项引用”。</span><span class="sxs-lookup"><span data-stu-id="ff385-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="ff385-214">在“查找”字段中，键入“当事方”。</span><span class="sxs-lookup"><span data-stu-id="ff385-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="ff385-215">单击“查找下一个”。</span><span class="sxs-lookup"><span data-stu-id="ff385-215">Click Find next.</span></span>
39. <span data-ttu-id="ff385-216">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ff385-216">Click OK.</span></span>
40. <span data-ttu-id="ff385-217">单击“查找下一个”。</span><span class="sxs-lookup"><span data-stu-id="ff385-217">Click Find next.</span></span>
41. <span data-ttu-id="ff385-218">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="ff385-219">在“名称”字段中，键入“描述”。</span><span class="sxs-lookup"><span data-stu-id="ff385-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="ff385-220">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="ff385-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="ff385-221">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-221">Click Add.</span></span>
45. <span data-ttu-id="ff385-222">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="ff385-223">在“名称”字段中，键入“货币”。</span><span class="sxs-lookup"><span data-stu-id="ff385-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="ff385-224">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-224">Click Add.</span></span>
48. <span data-ttu-id="ff385-225">在“描述”字段中，输入“货币代码”。</span><span class="sxs-lookup"><span data-stu-id="ff385-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="ff385-226">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="ff385-227">在“名称”字段中，键入“交易记录日期”。</span><span class="sxs-lookup"><span data-stu-id="ff385-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="ff385-228">在“物料类型”字段中，选择“日期”。</span><span class="sxs-lookup"><span data-stu-id="ff385-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="ff385-229">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-229">Click Add.</span></span>
53. <span data-ttu-id="ff385-230">在“描述”字段中，输入“交易日期”。</span><span class="sxs-lookup"><span data-stu-id="ff385-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="ff385-231">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="ff385-232">在“名称”字段中，键入“指示金额”。</span><span class="sxs-lookup"><span data-stu-id="ff385-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="ff385-233">在“物料类型”字段中，选择“实时”。</span><span class="sxs-lookup"><span data-stu-id="ff385-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="ff385-234">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-234">Click Add.</span></span>
58. <span data-ttu-id="ff385-235">在“描述”字段，输入“在借方和贷方之间移动的扣除费用前的金额。</span><span class="sxs-lookup"><span data-stu-id="ff385-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="ff385-236">该金额应以发起方指定的币种表示”。</span><span class="sxs-lookup"><span data-stu-id="ff385-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="ff385-237">在借方和贷方之间移动的扣除费用前的金额。</span><span class="sxs-lookup"><span data-stu-id="ff385-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="ff385-238">该金额应以发起方指定的币种表示。</span><span class="sxs-lookup"><span data-stu-id="ff385-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="ff385-239">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ff385-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="ff385-240">在“名称”字段中，键入“End2EndID”。</span><span class="sxs-lookup"><span data-stu-id="ff385-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="ff385-241">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="ff385-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="ff385-242">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ff385-242">Click Add.</span></span>
63. <span data-ttu-id="ff385-243">在“描述”字段中，输入“输入发起方分配的唯一标识。</span><span class="sxs-lookup"><span data-stu-id="ff385-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="ff385-244">该标识在整个端对端链中传递，无更改”。</span><span class="sxs-lookup"><span data-stu-id="ff385-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="ff385-245">在“名称”字段中，键入“付款模型”。</span><span class="sxs-lookup"><span data-stu-id="ff385-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="ff385-246">付款模型名称与付款形式的预定义接口相符。</span><span class="sxs-lookup"><span data-stu-id="ff385-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="ff385-247">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ff385-247">Click Save.</span></span>
66. <span data-ttu-id="ff385-248">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ff385-248">Close the page.</span></span>


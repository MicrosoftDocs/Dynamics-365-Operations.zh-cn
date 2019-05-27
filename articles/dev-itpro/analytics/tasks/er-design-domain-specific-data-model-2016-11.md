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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0debb7276c4f3e41c2e85ce6bc63b8df5bc159f8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551509"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="5436d-103">ER 设计域特定数据模型</span><span class="sxs-lookup"><span data-stu-id="5436d-103">ER Design domain specific data model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5436d-104">以下步骤说明属于系统管理员或电子报表开发人员的用户如何创建新电子报表 (ER) 配置，使其包含电子付款文件中的数据模型。</span><span class="sxs-lookup"><span data-stu-id="5436d-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="5436d-105">此数据模型稍后将用于您创建付款文件的格式时的数据源。</span><span class="sxs-lookup"><span data-stu-id="5436d-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="5436d-106">在此示例中，您将创建示例公司 Litware，Inc. 的配置。这些步骤可在任何公司执行，因为公司之间共享 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="5436d-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="5436d-107">为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="5436d-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="5436d-108">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="5436d-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="5436d-109">为示例公司“Litware 公司”选择配置提供程序。</span><span class="sxs-lookup"><span data-stu-id="5436d-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="5436d-110">如果没有看到此配置提供程序，您必须首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="5436d-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="5436d-111">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="5436d-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="5436d-112">您要创建含有电子付款文件的数据模型的模板。</span><span class="sxs-lookup"><span data-stu-id="5436d-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="5436d-113">此数据模型稍后将用于您创建付款文件的格式时的数据源。</span><span class="sxs-lookup"><span data-stu-id="5436d-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="5436d-114">创建新的数据模型配置</span><span class="sxs-lookup"><span data-stu-id="5436d-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="5436d-115">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="5436d-116">在“名称”字段中，键入“付款（简化模型）”。</span><span class="sxs-lookup"><span data-stu-id="5436d-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="5436d-117">付款（简化模型）</span><span class="sxs-lookup"><span data-stu-id="5436d-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="5436d-118">在“描述”字段，键入“付款模式配置”。</span><span class="sxs-lookup"><span data-stu-id="5436d-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="5436d-119">付款模型配置</span><span class="sxs-lookup"><span data-stu-id="5436d-119">Payment model configuration</span></span>  
    * <span data-ttu-id="5436d-120">有效配置提供商将自动在此输入。</span><span class="sxs-lookup"><span data-stu-id="5436d-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="5436d-121">此提供商可以维护此配置。</span><span class="sxs-lookup"><span data-stu-id="5436d-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="5436d-122">其他提供商可以使用此配置，但不能对其进行维护。</span><span class="sxs-lookup"><span data-stu-id="5436d-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="5436d-123">单击“创建配置”按钮以完成配置创建任务</span><span class="sxs-lookup"><span data-stu-id="5436d-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="5436d-124">创建数据模型</span><span class="sxs-lookup"><span data-stu-id="5436d-124">Create a data model</span></span>
    * <span data-ttu-id="5436d-125">您正在为所选配置创建新的数据模型。</span><span class="sxs-lookup"><span data-stu-id="5436d-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="5436d-126">此配置版本将为“草稿”状态。</span><span class="sxs-lookup"><span data-stu-id="5436d-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="5436d-127">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="5436d-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="5436d-128">定义参与付款流程的当事方的结构</span><span class="sxs-lookup"><span data-stu-id="5436d-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="5436d-129">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="5436d-130">在“名称”字段中，键入“当事方”。</span><span class="sxs-lookup"><span data-stu-id="5436d-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="5436d-131">当事方</span><span class="sxs-lookup"><span data-stu-id="5436d-131">Party</span></span>  
3. <span data-ttu-id="5436d-132">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-132">Click Add.</span></span>
4. <span data-ttu-id="5436d-133">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="5436d-134">在“名称”字段中，键入“名称”。</span><span class="sxs-lookup"><span data-stu-id="5436d-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="5436d-135">姓名</span><span class="sxs-lookup"><span data-stu-id="5436d-135">Name</span></span>  
6. <span data-ttu-id="5436d-136">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="5436d-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="5436d-137">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-137">Click Add.</span></span>
8. <span data-ttu-id="5436d-138">在“查找”字段中，键入“当事方”。</span><span class="sxs-lookup"><span data-stu-id="5436d-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="5436d-139">当事方</span><span class="sxs-lookup"><span data-stu-id="5436d-139">Party</span></span>  
9. <span data-ttu-id="5436d-140">单击“查找上一个”。</span><span class="sxs-lookup"><span data-stu-id="5436d-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="5436d-141">定义此模型的银行结构</span><span class="sxs-lookup"><span data-stu-id="5436d-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="5436d-142">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="5436d-143">在“名称”字段中，键入“代理”。</span><span class="sxs-lookup"><span data-stu-id="5436d-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="5436d-144">代理</span><span class="sxs-lookup"><span data-stu-id="5436d-144">Agent</span></span>  
3. <span data-ttu-id="5436d-145">在“物料类型”字段中，选择“记录”。</span><span class="sxs-lookup"><span data-stu-id="5436d-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="5436d-146">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-146">Click Add.</span></span>
5. <span data-ttu-id="5436d-147">在“描述”字段，输入“负责维护当事方（借方/贷方）帐户的金融机构（例如银行）”。</span><span class="sxs-lookup"><span data-stu-id="5436d-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="5436d-148">负责维护当事方（贷方/借方）帐户的金融机构（例如银行）。</span><span class="sxs-lookup"><span data-stu-id="5436d-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="5436d-149">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="5436d-150">在“名称”字段中，键入“名称”。</span><span class="sxs-lookup"><span data-stu-id="5436d-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="5436d-151">姓名</span><span class="sxs-lookup"><span data-stu-id="5436d-151">Name</span></span>  
8. <span data-ttu-id="5436d-152">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="5436d-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="5436d-153">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-153">Click Add.</span></span>
10. <span data-ttu-id="5436d-154">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="5436d-155">在“名称”字段中，键入“SWIFT”。</span><span class="sxs-lookup"><span data-stu-id="5436d-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="5436d-156">SWIFT</span><span class="sxs-lookup"><span data-stu-id="5436d-156">SWIFT</span></span>  
12. <span data-ttu-id="5436d-157">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-157">Click Add.</span></span>
13. <span data-ttu-id="5436d-158">在“描述”字段中，输入“银行标识代码”。</span><span class="sxs-lookup"><span data-stu-id="5436d-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="5436d-159">银行的标识代码</span><span class="sxs-lookup"><span data-stu-id="5436d-159">Bank identification code</span></span>  
14. <span data-ttu-id="5436d-160">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="5436d-161">在“名称”字段中，键入“银行代号”。</span><span class="sxs-lookup"><span data-stu-id="5436d-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="5436d-162">银行代号</span><span class="sxs-lookup"><span data-stu-id="5436d-162">RoutingNumber</span></span>  
16. <span data-ttu-id="5436d-163">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-163">Click Add.</span></span>
17. <span data-ttu-id="5436d-164">在“描述”字段中，输入“银行代号”。</span><span class="sxs-lookup"><span data-stu-id="5436d-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="5436d-165">工商登记号</span><span class="sxs-lookup"><span data-stu-id="5436d-165">Routing number</span></span>  
18. <span data-ttu-id="5436d-166">单击“查找上一个”。</span><span class="sxs-lookup"><span data-stu-id="5436d-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="5436d-167">定义此模型的银行帐户结构</span><span class="sxs-lookup"><span data-stu-id="5436d-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="5436d-168">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="5436d-169">在“名称”字段中，键入“帐户”。</span><span class="sxs-lookup"><span data-stu-id="5436d-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="5436d-170">科目</span><span class="sxs-lookup"><span data-stu-id="5436d-170">Account</span></span>  
3. <span data-ttu-id="5436d-171">在“物料类型”字段中，选择“记录”。</span><span class="sxs-lookup"><span data-stu-id="5436d-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="5436d-172">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-172">Click Add.</span></span>
5. <span data-ttu-id="5436d-173">在“描述”字段中，输入“当事方在金融机构（如银行）中的帐户的标识。”。</span><span class="sxs-lookup"><span data-stu-id="5436d-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="5436d-174">当事方在金融机构（如银行）中的帐户的标识。</span><span class="sxs-lookup"><span data-stu-id="5436d-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="5436d-175">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="5436d-176">在“名称”字段中，键入“货币”。</span><span class="sxs-lookup"><span data-stu-id="5436d-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="5436d-177">币种</span><span class="sxs-lookup"><span data-stu-id="5436d-177">Currency</span></span>  
8. <span data-ttu-id="5436d-178">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="5436d-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="5436d-179">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-179">Click Add.</span></span>
10. <span data-ttu-id="5436d-180">在“描述”字段中，输入“货币代码”。</span><span class="sxs-lookup"><span data-stu-id="5436d-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="5436d-181">币种代码</span><span class="sxs-lookup"><span data-stu-id="5436d-181">Currency code</span></span>  
11. <span data-ttu-id="5436d-182">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="5436d-183">在“名称”字段中，键入“数字”。</span><span class="sxs-lookup"><span data-stu-id="5436d-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="5436d-184">数字</span><span class="sxs-lookup"><span data-stu-id="5436d-184">Number</span></span>  
13. <span data-ttu-id="5436d-185">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-185">Click Add.</span></span>
14. <span data-ttu-id="5436d-186">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="5436d-187">在“名称”字段中，键入“IBAN”。</span><span class="sxs-lookup"><span data-stu-id="5436d-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="5436d-188">IBAN / 国际银行帐号</span><span class="sxs-lookup"><span data-stu-id="5436d-188">IBAN</span></span>  
16. <span data-ttu-id="5436d-189">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-189">Click Add.</span></span>
17. <span data-ttu-id="5436d-190">在“描述”字段中，输入“国际银行帐号”。</span><span class="sxs-lookup"><span data-stu-id="5436d-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="5436d-191">国际银行帐号</span><span class="sxs-lookup"><span data-stu-id="5436d-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="5436d-192">定义贷方转帐付款类型的付款消息结构</span><span class="sxs-lookup"><span data-stu-id="5436d-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="5436d-193">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="5436d-194">在“作为以下项的新节点”字段中，输入“模型根”。</span><span class="sxs-lookup"><span data-stu-id="5436d-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="5436d-195">在“名称”字段中，键入“客户贷方转帐发起”。</span><span class="sxs-lookup"><span data-stu-id="5436d-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="5436d-196">客户贷方转帐发起</span><span class="sxs-lookup"><span data-stu-id="5436d-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="5436d-197">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-197">Click Add.</span></span>
5. <span data-ttu-id="5436d-198">在“查找”字段中，键入“客户贷方转帐发起”。</span><span class="sxs-lookup"><span data-stu-id="5436d-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="5436d-199">客户贷方转帐发起</span><span class="sxs-lookup"><span data-stu-id="5436d-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="5436d-200">单击“查找上一个”。</span><span class="sxs-lookup"><span data-stu-id="5436d-200">Click Find previous.</span></span>
7. <span data-ttu-id="5436d-201">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="5436d-202">在“名称”字段中，键入“消息标识”。</span><span class="sxs-lookup"><span data-stu-id="5436d-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="5436d-203">消息标识</span><span class="sxs-lookup"><span data-stu-id="5436d-203">MessageIdentification</span></span>  
9. <span data-ttu-id="5436d-204">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-204">Click Add.</span></span>
10. <span data-ttu-id="5436d-205">在“描述”字段，输入“由指示方分配（并发送给下一个当事方）以标识消息的点对点引用。”。</span><span class="sxs-lookup"><span data-stu-id="5436d-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="5436d-206">点对点引用由指示方分配（并发送给下一个当事方）以明确消息。</span><span class="sxs-lookup"><span data-stu-id="5436d-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="5436d-207">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="5436d-208">在“名称”字段中，键入“处理日期时间”“。</span><span class="sxs-lookup"><span data-stu-id="5436d-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="5436d-209">处理日期时间</span><span class="sxs-lookup"><span data-stu-id="5436d-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="5436d-210">在“物料类型”字段中，选择“日期时间”。</span><span class="sxs-lookup"><span data-stu-id="5436d-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="5436d-211">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-211">Click Add.</span></span>
15. <span data-ttu-id="5436d-212">在“描述”字段中，输入“创建付款消息的日期和时间。”。</span><span class="sxs-lookup"><span data-stu-id="5436d-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="5436d-213">创建消息的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="5436d-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="5436d-214">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="5436d-215">定义此模型的付款交易结构。</span><span class="sxs-lookup"><span data-stu-id="5436d-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="5436d-216">在“名称”字段中，键入“付款”。</span><span class="sxs-lookup"><span data-stu-id="5436d-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="5436d-217">付款</span><span class="sxs-lookup"><span data-stu-id="5436d-217">Payments</span></span>  
18. <span data-ttu-id="5436d-218">在“物料类型”字段中，选择“记录列表”。</span><span class="sxs-lookup"><span data-stu-id="5436d-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="5436d-219">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-219">Click Add.</span></span>
20. <span data-ttu-id="5436d-220">在“描述”字段中，输入“当前消息付款行”。</span><span class="sxs-lookup"><span data-stu-id="5436d-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="5436d-221">当前消息的付款行</span><span class="sxs-lookup"><span data-stu-id="5436d-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="5436d-222">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="5436d-223">在“名称”字段中，键入“贷方”。</span><span class="sxs-lookup"><span data-stu-id="5436d-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="5436d-224">贷方</span><span class="sxs-lookup"><span data-stu-id="5436d-224">Creditor</span></span>  
23. <span data-ttu-id="5436d-225">在“物料类型”字段中，选择“记录”。</span><span class="sxs-lookup"><span data-stu-id="5436d-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="5436d-226">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-226">Click Add.</span></span>
25. <span data-ttu-id="5436d-227">在“描述”字段中，输入“应将金额支付给的当事方。”。</span><span class="sxs-lookup"><span data-stu-id="5436d-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="5436d-228">应将金额支付给的当事方。</span><span class="sxs-lookup"><span data-stu-id="5436d-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="5436d-229">单击“切换项引用”。</span><span class="sxs-lookup"><span data-stu-id="5436d-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="5436d-230">在“查找”字段中，键入“当事方”。</span><span class="sxs-lookup"><span data-stu-id="5436d-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="5436d-231">当事方</span><span class="sxs-lookup"><span data-stu-id="5436d-231">Party</span></span>  
28. <span data-ttu-id="5436d-232">单击“查找下一个”。</span><span class="sxs-lookup"><span data-stu-id="5436d-232">Click Find next.</span></span>
29. <span data-ttu-id="5436d-233">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5436d-233">Click OK.</span></span>
30. <span data-ttu-id="5436d-234">在“查找”字段中，键入“付款”。</span><span class="sxs-lookup"><span data-stu-id="5436d-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="5436d-235">付款</span><span class="sxs-lookup"><span data-stu-id="5436d-235">Payments</span></span>  
31. <span data-ttu-id="5436d-236">单击“查找下一个”。</span><span class="sxs-lookup"><span data-stu-id="5436d-236">Click Find next.</span></span>
32. <span data-ttu-id="5436d-237">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="5436d-238">在“名称”字段中，键入“借方”。</span><span class="sxs-lookup"><span data-stu-id="5436d-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="5436d-239">借方</span><span class="sxs-lookup"><span data-stu-id="5436d-239">Debtor</span></span>  
34. <span data-ttu-id="5436d-240">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-240">Click Add.</span></span>
35. <span data-ttu-id="5436d-241">在“描述”字段，输入“欠(最终)贷方款项的当事方。”。</span><span class="sxs-lookup"><span data-stu-id="5436d-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="5436d-242">欠(最终)贷方款项的当事方。</span><span class="sxs-lookup"><span data-stu-id="5436d-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="5436d-243">单击“切换项引用”。</span><span class="sxs-lookup"><span data-stu-id="5436d-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="5436d-244">在“查找”字段中，键入“当事方”。</span><span class="sxs-lookup"><span data-stu-id="5436d-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="5436d-245">当事方</span><span class="sxs-lookup"><span data-stu-id="5436d-245">Party</span></span>  
38. <span data-ttu-id="5436d-246">单击“查找下一个”。</span><span class="sxs-lookup"><span data-stu-id="5436d-246">Click Find next.</span></span>
39. <span data-ttu-id="5436d-247">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5436d-247">Click OK.</span></span>
40. <span data-ttu-id="5436d-248">单击“查找下一个”。</span><span class="sxs-lookup"><span data-stu-id="5436d-248">Click Find next.</span></span>
41. <span data-ttu-id="5436d-249">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="5436d-250">在“名称”字段中，键入“描述”。</span><span class="sxs-lookup"><span data-stu-id="5436d-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="5436d-251">说明</span><span class="sxs-lookup"><span data-stu-id="5436d-251">Description</span></span>  
43. <span data-ttu-id="5436d-252">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="5436d-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="5436d-253">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-253">Click Add.</span></span>
45. <span data-ttu-id="5436d-254">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="5436d-255">在“名称”字段中，键入“货币”。</span><span class="sxs-lookup"><span data-stu-id="5436d-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="5436d-256">币种</span><span class="sxs-lookup"><span data-stu-id="5436d-256">Currency</span></span>  
47. <span data-ttu-id="5436d-257">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-257">Click Add.</span></span>
48. <span data-ttu-id="5436d-258">在“描述”字段中，输入“货币代码”。</span><span class="sxs-lookup"><span data-stu-id="5436d-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="5436d-259">币种代码</span><span class="sxs-lookup"><span data-stu-id="5436d-259">Currency code</span></span>  
49. <span data-ttu-id="5436d-260">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="5436d-261">在“名称”字段中，键入“交易记录日期”。</span><span class="sxs-lookup"><span data-stu-id="5436d-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="5436d-262">交易记录日期</span><span class="sxs-lookup"><span data-stu-id="5436d-262">TransactionDate</span></span>  
51. <span data-ttu-id="5436d-263">在“物料类型”字段中，选择“日期”。</span><span class="sxs-lookup"><span data-stu-id="5436d-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="5436d-264">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-264">Click Add.</span></span>
53. <span data-ttu-id="5436d-265">在“描述”字段中，输入“交易日期”。</span><span class="sxs-lookup"><span data-stu-id="5436d-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="5436d-266">交易记录日期</span><span class="sxs-lookup"><span data-stu-id="5436d-266">Transaction date</span></span>  
54. <span data-ttu-id="5436d-267">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="5436d-268">在“名称”字段中，键入“指示金额”。</span><span class="sxs-lookup"><span data-stu-id="5436d-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="5436d-269">指示金额</span><span class="sxs-lookup"><span data-stu-id="5436d-269">InstructedAmount</span></span>  
56. <span data-ttu-id="5436d-270">在“物料类型”字段中，选择“实时”。</span><span class="sxs-lookup"><span data-stu-id="5436d-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="5436d-271">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-271">Click Add.</span></span>
58. <span data-ttu-id="5436d-272">在“描述”字段，输入“在借方和贷方之间移动的扣除费用前的金额。</span><span class="sxs-lookup"><span data-stu-id="5436d-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="5436d-273">该金额应以发起方指定的币种表示”。</span><span class="sxs-lookup"><span data-stu-id="5436d-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="5436d-274">在借方和贷方之间移动的扣除费用前的金额。</span><span class="sxs-lookup"><span data-stu-id="5436d-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="5436d-275">该金额应以发起方指定的币种表示。</span><span class="sxs-lookup"><span data-stu-id="5436d-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="5436d-276">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="5436d-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="5436d-277">在“名称”字段中，键入“End2EndID”。</span><span class="sxs-lookup"><span data-stu-id="5436d-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="5436d-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="5436d-278">End2EndID</span></span>  
61. <span data-ttu-id="5436d-279">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="5436d-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="5436d-280">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="5436d-280">Click Add.</span></span>
63. <span data-ttu-id="5436d-281">在“描述”字段中，输入“输入发起方分配的唯一标识。</span><span class="sxs-lookup"><span data-stu-id="5436d-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="5436d-282">该标识在整个端对端链中传递，无更改”。</span><span class="sxs-lookup"><span data-stu-id="5436d-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="5436d-283">发起方分配的唯一标识。</span><span class="sxs-lookup"><span data-stu-id="5436d-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="5436d-284">该标识在整个端对端链中传递，无更改。</span><span class="sxs-lookup"><span data-stu-id="5436d-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="5436d-285">在“名称”字段中，键入“付款模型”。</span><span class="sxs-lookup"><span data-stu-id="5436d-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="5436d-286">付款模型名称与付款形式的预定义接口相符。</span><span class="sxs-lookup"><span data-stu-id="5436d-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="5436d-287">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="5436d-287">Click Save.</span></span>
66. <span data-ttu-id="5436d-288">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="5436d-288">Close the page.</span></span>


---
title: ER 通过采用该格式的新的基本版本升级格式
description: 以下步骤说明属于系统管理员或电子报表开发人员的用户如何维护电子申报 (ER) 格式配置。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 648b750b311f902555eba4536767788b64a1ea1e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184638"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a><span data-ttu-id="e0255-103">ER 通过采用该格式的新的基本版本升级格式</span><span class="sxs-lookup"><span data-stu-id="e0255-103">ER Upgrade your format by adopting a new, base version of that format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e0255-104">以下步骤说明属于系统管理员或电子报表开发人员的用户如何维护电子申报 (ER) 格式配置。</span><span class="sxs-lookup"><span data-stu-id="e0255-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can maintain an Electronic reporting (ER) format configuration.</span></span> <span data-ttu-id="e0255-105">此过程说明如何基于配置提供程序 (CP) 接收的格式创建格式的自定义版本。</span><span class="sxs-lookup"><span data-stu-id="e0255-105">This procedure explains how a custom version of a format can be created based on the format received from a configuration provider (CP).</span></span> <span data-ttu-id="e0255-106">它还说明如何采用该格式的新的基本版本。</span><span class="sxs-lookup"><span data-stu-id="e0255-106">It also explains how to adopt a new, base version of that format.</span></span>



<span data-ttu-id="e0255-107">为了完成这些步骤，您必须首先完成“创建配置提供程序并标记其为有效“和“使用创建的格式生成电子付款单据”过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="e0255-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” and “Use created format to generate electronic documents for payments” procedures.</span></span> <span data-ttu-id="e0255-108">这些步骤可以在 GBSI 公司执行。</span><span class="sxs-lookup"><span data-stu-id="e0255-108">These steps can be performed in the GBSI company.</span></span>


## <a name="select-format-configuration-for-customization"></a><span data-ttu-id="e0255-109">选择自定义格式配置</span><span class="sxs-lookup"><span data-stu-id="e0255-109">Select format configuration for customization</span></span>
1. <span data-ttu-id="e0255-110">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="e0255-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="e0255-111">在此示例中，示例公司 Litware 公司 (https://www.litware.com) 将充当支持特定国家/地区的电子付款的格式配置的配置提供商。</span><span class="sxs-lookup"><span data-stu-id="e0255-111">In this example, sample company Litware, Inc. (https://www.litware.com) will act as a configuration provider that supports format configurations for electronic payments for a particular country.</span></span>    <span data-ttu-id="e0255-112">示例公司 Proseware 公司 (http://www.proseware.com) 将充当 Litware 公司提供的格式配置的使用者。</span><span class="sxs-lookup"><span data-stu-id="e0255-112">Sample company Proseware, Inc. (http://www.proseware.com) will act as a consumer of the format configuration that Litware, Inc. provided.</span></span> <span data-ttu-id="e0255-113">Proseware 公司在该国家/地区的某些地区使用格式。</span><span class="sxs-lookup"><span data-stu-id="e0255-113">Proseware, Inc. uses formats in certain regions of that country.</span></span>  
2. <span data-ttu-id="e0255-114">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="e0255-114">Click Reporting configurations.</span></span>
3. <span data-ttu-id="e0255-115">单击“显示筛选器”。</span><span class="sxs-lookup"><span data-stu-id="e0255-115">Click Show filters.</span></span>
4. <span data-ttu-id="e0255-116">应用以下筛选器：使用“开头为”筛选器运算符在“名称”字段中输入筛选器值“BACS（英国虚构）”。</span><span class="sxs-lookup"><span data-stu-id="e0255-116">Apply the following filters: Enter a filter value of "BACS (UK fictitious)" on the "Name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="e0255-117">银行自动对帐系统（英国虚构）</span><span class="sxs-lookup"><span data-stu-id="e0255-117">BACS (UK fictitious)</span></span>  
    * <span data-ttu-id="e0255-118">提供商 Litware 公司拥有所选格式配置 BACS（英国虚构）。</span><span class="sxs-lookup"><span data-stu-id="e0255-118">The selected format configuration BACS (UK fictitious) is owned by provider Litware, Inc.</span></span>  
5. <span data-ttu-id="e0255-119">单击“显示筛选器”。</span><span class="sxs-lookup"><span data-stu-id="e0255-119">Click Show filters.</span></span>
6. <span data-ttu-id="e0255-120">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="e0255-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e0255-121">状态为“已完成”的格式的版本将由 Proseware, Inc 用于 自定义。</span><span class="sxs-lookup"><span data-stu-id="e0255-121">The version of the format with the status of Completed will be used by Proseware, Inc. for customization.</span></span>  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a><span data-ttu-id="e0255-122">为您的电子单据自定义格式创建新配置</span><span class="sxs-lookup"><span data-stu-id="e0255-122">Create a new configuration for your custom format of electronic document</span></span>
    * <span data-ttu-id="e0255-123">Proseware 公司收到包含初始格式的 BACS（英国虚构）配置的版本 1.1 以根据其服务订阅从 Litware 公司生成电子付款单据。</span><span class="sxs-lookup"><span data-stu-id="e0255-123">Proseware, Inc. received version 1.1 of BACS (UK fictitious) configuration that contains the initial format to generate electronic payment documents from Litware, Inc. in accordance to their service subscription.</span></span> <span data-ttu-id="e0255-124">Proseware 公司想要开始使用此作为他们的国家/地区的标准，但支持特定的地区要求需要部分自定义。</span><span class="sxs-lookup"><span data-stu-id="e0255-124">Proseware, Inc. wants to start using this as a standard for their country but some customization is required to support specific regional requirements.</span></span> <span data-ttu-id="e0255-125">Proseware 公司还想要保留 Litware 公司一提供自定义格式的新版本（通过对支持新国家/地区特定要求的更改）即升级自定义格式的能力，并希望以最低的成本执行此项升级。</span><span class="sxs-lookup"><span data-stu-id="e0255-125">Proseware, Inc. also wants to keep the ability to upgrade a custom format as soon as a new version of it (with changes to support new country-specific requirements) comes from Litware, Inc. and they want to perform this upgrade with the lowest cost.</span></span>  <span data-ttu-id="e0255-126">因此，Proseware 公司需要以 Litware 公司配置 BACS（英国虚构）为基础创建配置。</span><span class="sxs-lookup"><span data-stu-id="e0255-126">To do this, Proseware, Inc. needs to create a configuration using the Litware, Inc. configuration BACS (UK fictitious) as a base.</span></span>  
1. <span data-ttu-id="e0255-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e0255-127">Close the page.</span></span>
2. <span data-ttu-id="e0255-128">选择 Proseware 公司将其设置为有效的提供商。</span><span class="sxs-lookup"><span data-stu-id="e0255-128">Select Proseware, Inc. to make it an active provider.</span></span>
3. <span data-ttu-id="e0255-129">单击“设置有效”。</span><span class="sxs-lookup"><span data-stu-id="e0255-129">Click Set active.</span></span>
4. <span data-ttu-id="e0255-130">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="e0255-130">Click Reporting configurations.</span></span>
5. <span data-ttu-id="e0255-131">在树结构中，展开“付款（简化模型）”。</span><span class="sxs-lookup"><span data-stu-id="e0255-131">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="e0255-132">在树结构中，选择“付款（简化模型）\BACS（英国虚构）”。</span><span class="sxs-lookup"><span data-stu-id="e0255-132">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="e0255-133">选择 Litware 公司的 BACS（英国虚构）配置。Proseware 公司将使用版本 1.1 作为自定义版本的基础。</span><span class="sxs-lookup"><span data-stu-id="e0255-133">Select the BACS (UK fictitious) configuration from Litware, Inc.     Proseware, Inc. will use version 1.1 as a base for the custom version.</span></span>  
7. <span data-ttu-id="e0255-134">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="e0255-134">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="e0255-135">可供您创建自定义付款格式的新配置。</span><span class="sxs-lookup"><span data-stu-id="e0255-135">This lets you create a new configuration for a custom payment format.</span></span>  
8. <span data-ttu-id="e0255-136">在“新建”字段中，输入“从名称派生：BACS（英国虚构），Litware 公司”。</span><span class="sxs-lookup"><span data-stu-id="e0255-136">In the New field, enter 'Derive from Name: BACS (UK fictitious), Litware, Inc.'.</span></span>
    * <span data-ttu-id="e0255-137">选择“派生”选项以确认使用 BACS（英国虚构）作为创建自定义版本的基础。</span><span class="sxs-lookup"><span data-stu-id="e0255-137">Select the Derive option to confirm the usage of BACS (UK fictitious) as the base for creating the custom version.</span></span>  
9. <span data-ttu-id="e0255-138">在“名称”字段中，键入“BACS（英国虚构自定义）”。</span><span class="sxs-lookup"><span data-stu-id="e0255-138">In the Name field, type 'BACS (UK fictitious custom)'.</span></span>
    * <span data-ttu-id="e0255-139">BACS（英国虚构自定义）</span><span class="sxs-lookup"><span data-stu-id="e0255-139">BACS (UK fictitious custom)</span></span>  
10. <span data-ttu-id="e0255-140">在“描述”字段中，键入“银行自动对帐系统供应商付款（英国虚拟自定义）”。</span><span class="sxs-lookup"><span data-stu-id="e0255-140">In the Description field, type 'BACS vendor payment (UK fictitious custom)'.</span></span>
    * <span data-ttu-id="e0255-141">BACS 供应商付款（英国虚构自定义）。</span><span class="sxs-lookup"><span data-stu-id="e0255-141">BACS vendor payment (UK fictitious custom)</span></span>  
    * <span data-ttu-id="e0255-142">有效配置提供商 (Proseware, Inc.) 将自动在此输入。</span><span class="sxs-lookup"><span data-stu-id="e0255-142">The active configuration provider (Proseware, Inc.) is automatically entered here.</span></span> <span data-ttu-id="e0255-143">此提供商可以维护此配置。</span><span class="sxs-lookup"><span data-stu-id="e0255-143">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="e0255-144">其他提供商可以使用此配置，但不能对其进行维护。</span><span class="sxs-lookup"><span data-stu-id="e0255-144">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
11. <span data-ttu-id="e0255-145">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="e0255-145">Click Create configuration.</span></span>

## <a name="customize-your-format-for-the-electronic-document"></a><span data-ttu-id="e0255-146">自定义电子单据格式</span><span class="sxs-lookup"><span data-stu-id="e0255-146">Customize your format for the electronic document</span></span>
1. <span data-ttu-id="e0255-147">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="e0255-147">Click Designer.</span></span>
2. <span data-ttu-id="e0255-148">单击”展开/折叠“。</span><span class="sxs-lookup"><span data-stu-id="e0255-148">Click Expand/collapse.</span></span>
3. <span data-ttu-id="e0255-149">单击”展开/折叠“。</span><span class="sxs-lookup"><span data-stu-id="e0255-149">Click Expand/collapse.</span></span>
4. <span data-ttu-id="e0255-150">在树结构中，选择“Xml\消息\付款\项\供应商\银行”。</span><span class="sxs-lookup"><span data-stu-id="e0255-150">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="e0255-151">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="e0255-151">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="e0255-152">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="e0255-152">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="e0255-153">在“名称”字段中，键入“IBAN”。</span><span class="sxs-lookup"><span data-stu-id="e0255-153">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="e0255-154">IBAN / 国际银行帐号</span><span class="sxs-lookup"><span data-stu-id="e0255-154">IBAN</span></span>  
8. <span data-ttu-id="e0255-155">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e0255-155">Click OK.</span></span>
9. <span data-ttu-id="e0255-156">在树结构中，选择“Xml\消息\付款\项\供应商\银行\IBAN”。</span><span class="sxs-lookup"><span data-stu-id="e0255-156">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.</span></span>
10. <span data-ttu-id="e0255-157">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="e0255-157">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="e0255-158">在树结构中，选择“文本\字符串”。</span><span class="sxs-lookup"><span data-stu-id="e0255-158">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="e0255-159">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e0255-159">Click OK.</span></span>
13. <span data-ttu-id="e0255-160">在树结构中，选择“Xml\消息\付款\项\供应商\名称\字符串”。</span><span class="sxs-lookup"><span data-stu-id="e0255-160">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="e0255-161">在“最大长度”字段中，输入 '60'。</span><span class="sxs-lookup"><span data-stu-id="e0255-161">In the Maximum length field, enter '60'.</span></span>
15. <span data-ttu-id="e0255-162">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="e0255-162">Click the Mapping tab.</span></span>
16. <span data-ttu-id="e0255-163">在树结构中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="e0255-163">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="e0255-164">在树结构中，展开“模型\付款”。</span><span class="sxs-lookup"><span data-stu-id="e0255-164">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="e0255-165">在树结构中，展开“模型\付款\贷方”。</span><span class="sxs-lookup"><span data-stu-id="e0255-165">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="e0255-166">在树结构中，展开“模型\付款\贷方\金额”。</span><span class="sxs-lookup"><span data-stu-id="e0255-166">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
20. <span data-ttu-id="e0255-167">在树结构中，选择“模型\付款\贷方\帐户\IBAN”。</span><span class="sxs-lookup"><span data-stu-id="e0255-167">In the tree, select 'model\Payments\Creditor\Account\IBAN'.</span></span>
21. <span data-ttu-id="e0255-168">在树结构中，选择“Xml\消息\付款\项 = 模型.付款\供应商\银行\IBAN\字符串”。</span><span class="sxs-lookup"><span data-stu-id="e0255-168">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\IBAN\String'.</span></span>
22. <span data-ttu-id="e0255-169">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="e0255-169">Click Bind.</span></span>
23. <span data-ttu-id="e0255-170">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="e0255-170">Click Save.</span></span>

## <a name="validate-the-customized-format"></a><span data-ttu-id="e0255-171">验证自定义格式</span><span class="sxs-lookup"><span data-stu-id="e0255-171">Validate the customized format</span></span>
1. <span data-ttu-id="e0255-172">单击“验证”。</span><span class="sxs-lookup"><span data-stu-id="e0255-172">Click Validate.</span></span>
    * <span data-ttu-id="e0255-173">验证自定义的格式布局和数据映射更改，以确保所有绑定正常。</span><span class="sxs-lookup"><span data-stu-id="e0255-173">Validate the customized format layout and data mapping changes to make sure that all bindings are okay.</span></span>  
2. <span data-ttu-id="e0255-174">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e0255-174">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a><span data-ttu-id="e0255-175">更改自定义格式配置的当前版本状态</span><span class="sxs-lookup"><span data-stu-id="e0255-175">Change the status of the current version of the custom format configuration</span></span>
    * <span data-ttu-id="e0255-176">将设计的格式配置的状态从“草稿”更改为“已完成”，以使得可供付款单据生成使用。</span><span class="sxs-lookup"><span data-stu-id="e0255-176">Change the status of the designed format configuration from Draft to Completed to make it available for payment document generation.</span></span>  
1. <span data-ttu-id="e0255-177">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="e0255-177">Click Change status.</span></span>
    * <span data-ttu-id="e0255-178">请注意，所选配置的当前版本为“草稿”状态。</span><span class="sxs-lookup"><span data-stu-id="e0255-178">Note that the current version of the selected configuration is in Draft status.</span></span>  
2. <span data-ttu-id="e0255-179">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="e0255-179">Click Complete.</span></span>
3. <span data-ttu-id="e0255-180">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e0255-180">In the Description field, type a value.</span></span>
4. <span data-ttu-id="e0255-181">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e0255-181">Click OK.</span></span>
5. <span data-ttu-id="e0255-182">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="e0255-182">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e0255-183">请注意已创建配置保存为已完成版本 1.1.1。</span><span class="sxs-lookup"><span data-stu-id="e0255-183">Note that the created configuration is saved as completed version 1.1.1.</span></span> <span data-ttu-id="e0255-184">这意味着它是自定义 BACS（英国虚构自定义）格式的版本 1，其基于 BACS（英国虚构）格式的版本 1，且基于付款（简化模型）数据模型的版本 1。</span><span class="sxs-lookup"><span data-stu-id="e0255-184">This means it is version 1 of the custom BACS (UK fictitious custom) format, which is based on version 1 of the BACS (UK fictitious) format, which is based on version 1 of the Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-to-generate-payment-files"></a><span data-ttu-id="e0255-185">测试自定义格式以生成付款文件</span><span class="sxs-lookup"><span data-stu-id="e0255-185">Test the customized format to generate payment files</span></span>
    * <span data-ttu-id="e0255-186">在一个并行 Finance and Operations 会话中完成“使用创建的格式生成付款电子单据”过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="e0255-186">Complete the steps in the “Use created format to generate electronic documents for payments” procedure in a parallel Finance and Operations session.</span></span> <span data-ttu-id="e0255-187">在电子付款方式参数中选择 BACS（英国虚构自定义）格式。</span><span class="sxs-lookup"><span data-stu-id="e0255-187">Select the BACS (UK fictitious custom) format in electronic payment method parameters.</span></span> <span data-ttu-id="e0255-188">确保创建的付款文件包含最近引入的根据区域要求呈现 IBAN 代码的 XML 代码。</span><span class="sxs-lookup"><span data-stu-id="e0255-188">Make sure that the created payment file contains the recently introduced XML node presenting IBAN code in accordance to regional requirements.</span></span>  

## <a name="update-the-existing-country-specific-configuration"></a><span data-ttu-id="e0255-189">更新现有国家/地区特定配置</span><span class="sxs-lookup"><span data-stu-id="e0255-189">Update the existing country-specific configuration</span></span>
    * <span data-ttu-id="e0255-190">Litware 公司需要更新 BACS（英国虚构）配置并采用管理电子单据格式的新的国家/地区要求。</span><span class="sxs-lookup"><span data-stu-id="e0255-190">Litware, Inc. needs to update the BACS (UK fictitious) configuration and adopt new country requirements for managing the format of the electronic document.</span></span> <span data-ttu-id="e0255-191">随后，这将包括在将为服务订阅者（包括 Proseware, Inc.）提供的此配置的新版本中。</span><span class="sxs-lookup"><span data-stu-id="e0255-191">Later, this will be enclosed in a new version of this configuration that will be offered for service subscribers, including Proseware, Inc.</span></span>  
    * <span data-ttu-id="e0255-192">在实际的服务设置相关流程中，BACS（英国虚构）的每个新版本可由 Proseware 公司从 Litware 公司配置的 LCS 存储库导入。</span><span class="sxs-lookup"><span data-stu-id="e0255-192">In real service provision related processes, each new version of BACS (UK fictitious) can be imported by Proseware, Inc. from Litware, Inc. configurations’ LCS repository.</span></span> <span data-ttu-id="e0255-193">在此过程中，我们将通过代表服务提供商更新 BACS（英国虚构）来模拟此操作。</span><span class="sxs-lookup"><span data-stu-id="e0255-193">In this procedure we will simulate this by updating BACS (UK fictitious) on behalf of a service provider.</span></span>  
1. <span data-ttu-id="e0255-194">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e0255-194">Close the page.</span></span>
2. <span data-ttu-id="e0255-195">选择 Litware 公司 提供程序。</span><span class="sxs-lookup"><span data-stu-id="e0255-195">Select Litware, inc. provider.</span></span>
3. <span data-ttu-id="e0255-196">单击“设置有效”。</span><span class="sxs-lookup"><span data-stu-id="e0255-196">Click Set active.</span></span>
4. <span data-ttu-id="e0255-197">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="e0255-197">Click Reporting configurations.</span></span>
5. <span data-ttu-id="e0255-198">在树结构中，展开“付款（简化模型）”。</span><span class="sxs-lookup"><span data-stu-id="e0255-198">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="e0255-199">在树结构中，选择“付款（简化模型）\BACS（英国虚构）”。</span><span class="sxs-lookup"><span data-stu-id="e0255-199">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="e0255-200">Litware 公司提供商 BACS（英国虚构）拥有的草稿版本被选择引入更改以支持新的特定于国家/地区的要求。</span><span class="sxs-lookup"><span data-stu-id="e0255-200">The draft version owned by Litware, Inc. provider BACS (UK fictitious) is selected to bring in changes to support new country-specific requirements.</span></span>  

## <a name="localize-the-base-format-of-the-electronic-document"></a><span data-ttu-id="e0255-201">本地化电子单据的基本格式</span><span class="sxs-lookup"><span data-stu-id="e0255-201">Localize the base format of the electronic document</span></span>
    * <span data-ttu-id="e0255-202">假定具有某些由 Litware 公司支持的新的国家/地区特定要求：- 每个付款交易记录中的贷方银行 SWIFT 代码的值。</span><span class="sxs-lookup"><span data-stu-id="e0255-202">Assume that there are new country-specific requirements to be supported by Litware, Inc.:  - A value for the creditor’s bank SWIFT code in each payment transaction.</span></span>  <span data-ttu-id="e0255-203">- 生成文件时供应商名称的文本长度限制为 100 个字符。</span><span class="sxs-lookup"><span data-stu-id="e0255-203">- A limit of 100 characters for the length of text for the vendor’s name in a generating file.</span></span>  
    * <span data-ttu-id="e0255-204">新国家/地区特定要求</span><span class="sxs-lookup"><span data-stu-id="e0255-204">New country-specific requirements</span></span>  
    * <span data-ttu-id="e0255-205">选择所需配置的草稿版本以引入所需的更改。</span><span class="sxs-lookup"><span data-stu-id="e0255-205">Select the draft version of the desired configuration to introduce required changes.</span></span>  
1. <span data-ttu-id="e0255-206">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="e0255-206">Click Designer.</span></span>
2. <span data-ttu-id="e0255-207">单击”展开/折叠“。</span><span class="sxs-lookup"><span data-stu-id="e0255-207">Click Expand/collapse.</span></span>
3. <span data-ttu-id="e0255-208">单击”展开/折叠“。</span><span class="sxs-lookup"><span data-stu-id="e0255-208">Click Expand/collapse.</span></span>
4. <span data-ttu-id="e0255-209">在树结构中，选择“Xml\消息\付款\项\供应商\银行”。</span><span class="sxs-lookup"><span data-stu-id="e0255-209">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="e0255-210">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="e0255-210">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="e0255-211">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="e0255-211">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="e0255-212">在“名称”字段中，键入“SWIFT”。</span><span class="sxs-lookup"><span data-stu-id="e0255-212">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="e0255-213">SWIFT</span><span class="sxs-lookup"><span data-stu-id="e0255-213">SWIFT</span></span>  
8. <span data-ttu-id="e0255-214">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e0255-214">Click OK.</span></span>
9. <span data-ttu-id="e0255-215">在树结构中，选择“Xml\消息\付款\项\供应商\银行\SWIFT”。</span><span class="sxs-lookup"><span data-stu-id="e0255-215">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.</span></span>
10. <span data-ttu-id="e0255-216">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="e0255-216">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="e0255-217">在树结构中，选择“文本\字符串”。</span><span class="sxs-lookup"><span data-stu-id="e0255-217">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="e0255-218">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e0255-218">Click OK.</span></span>
13. <span data-ttu-id="e0255-219">在树结构中，选择“Xml\消息\付款\项\供应商\名称\字符串”。</span><span class="sxs-lookup"><span data-stu-id="e0255-219">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="e0255-220">在“最大长度”字段中，输入 '100'。</span><span class="sxs-lookup"><span data-stu-id="e0255-220">In the Maximum length field, enter '100'.</span></span>
15. <span data-ttu-id="e0255-221">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="e0255-221">Click the Mapping tab.</span></span>
16. <span data-ttu-id="e0255-222">在树结构中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="e0255-222">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="e0255-223">在树结构中，展开“模型\付款”。</span><span class="sxs-lookup"><span data-stu-id="e0255-223">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="e0255-224">在树结构中，展开“模型\付款\贷方”。</span><span class="sxs-lookup"><span data-stu-id="e0255-224">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="e0255-225">在树结构中，展开“模型\付款\贷方\代理”。</span><span class="sxs-lookup"><span data-stu-id="e0255-225">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
20. <span data-ttu-id="e0255-226">在树结构中，选择“模型\付款\贷方\代理\SWIFT”。</span><span class="sxs-lookup"><span data-stu-id="e0255-226">In the tree, select 'model\Payments\Creditor\Agent\SWIFT'.</span></span>
21. <span data-ttu-id="e0255-227">在树结构中，选择“Xml\消息\付款\项 = 模型.付款\供应商\银行\SWIFT\字符串”。</span><span class="sxs-lookup"><span data-stu-id="e0255-227">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\SWIFT\String'.</span></span>
22. <span data-ttu-id="e0255-228">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="e0255-228">Click Bind.</span></span>
23. <span data-ttu-id="e0255-229">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="e0255-229">Click Save.</span></span>

## <a name="validate-the-localized-format"></a><span data-ttu-id="e0255-230">验证本地化格式</span><span class="sxs-lookup"><span data-stu-id="e0255-230">Validate the localized format</span></span>
1. <span data-ttu-id="e0255-231">单击“验证”。</span><span class="sxs-lookup"><span data-stu-id="e0255-231">Click Validate.</span></span>
2. <span data-ttu-id="e0255-232">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e0255-232">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a><span data-ttu-id="e0255-233">更改基本格式配置的当前版本状态</span><span class="sxs-lookup"><span data-stu-id="e0255-233">Change the status of the current version of the base format configuration</span></span>
    * <span data-ttu-id="e0255-234">将更新的基本格式配置的状态从“草稿”更改为“已完成”，以使它可用于付款单据的生成以及从其派生的格式配置的更新。</span><span class="sxs-lookup"><span data-stu-id="e0255-234">Change the status of the updated base format configuration from Draft to Completed to make it available for generation of payment documents and updates of format configurations derived from it.</span></span>  
1. <span data-ttu-id="e0255-235">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="e0255-235">Click Change status.</span></span>
    * <span data-ttu-id="e0255-236">请注意，所选配置的当前版本为“草稿”状态。</span><span class="sxs-lookup"><span data-stu-id="e0255-236">Note that the current version of the selected configuration is in Draft status.</span></span>  
2. <span data-ttu-id="e0255-237">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="e0255-237">Click Complete.</span></span>
3. <span data-ttu-id="e0255-238">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e0255-238">In the Description field, type a value.</span></span>
4. <span data-ttu-id="e0255-239">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e0255-239">Click OK.</span></span>
5. <span data-ttu-id="e0255-240">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="e0255-240">In the list, find and select the desired record.</span></span>

## <a name="change-the-base-version-for-the-custom-format-configuration"></a><span data-ttu-id="e0255-241">更改自定义格式配置的基本版本</span><span class="sxs-lookup"><span data-stu-id="e0255-241">Change the base version for the custom format configuration</span></span>
    * <span data-ttu-id="e0255-242">Proseware 公司获知 BACS（英国虚构）配置的新版本 1.2 可用于根据最近颁布的特定于国家/地区的要求生成电子付款单据。</span><span class="sxs-lookup"><span data-stu-id="e0255-242">Proseware, Inc. is informed that a new version 1.2 of BACS (UK fictitious) configuration is available to generate electronic payment documents in accordance to recently announced country-specific requirements.</span></span> <span data-ttu-id="e0255-243">Proseware 公司想要开始使用其作为国家/地区的标准。</span><span class="sxs-lookup"><span data-stu-id="e0255-243">Proseware, Inc. wants to start using it as a standard for the country.</span></span>  <span data-ttu-id="e0255-244">因此，Proseware 公司需要更改自定义配置 BACS（英国虚构自定义）的基本配置版本。</span><span class="sxs-lookup"><span data-stu-id="e0255-244">To do this, Proseware, Inc. needs to change the base configuration version for the custom configuration BACS (UK fictitious custom).</span></span> <span data-ttu-id="e0255-245">使用新版本 1.2，而不是 BACS（英国虚构）的版本 1.1。</span><span class="sxs-lookup"><span data-stu-id="e0255-245">Instead of version 1.1 of BACS (UK fictitious) use new version 1.2.</span></span>  
1. <span data-ttu-id="e0255-246">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="e0255-246">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e0255-247">选择 Proseware 公司提供商将其设置为有效的提供商。</span><span class="sxs-lookup"><span data-stu-id="e0255-247">Select the Proseware, Inc. provider to mark it as active.</span></span>
3. <span data-ttu-id="e0255-248">单击“设置有效”。</span><span class="sxs-lookup"><span data-stu-id="e0255-248">Click Set active.</span></span>
4. <span data-ttu-id="e0255-249">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="e0255-249">Click Reporting configurations.</span></span>
5. <span data-ttu-id="e0255-250">在树结构中，展开“付款（简化模型）”。</span><span class="sxs-lookup"><span data-stu-id="e0255-250">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="e0255-251">在树结构中，展开“付款（简化模型）\BACS（英国虚构）”。</span><span class="sxs-lookup"><span data-stu-id="e0255-251">In the tree, expand 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
7. <span data-ttu-id="e0255-252">在树结构中，选择“付款（简化模型）\BACS（英国虚构）\BACS（英国虚构自定义）”。</span><span class="sxs-lookup"><span data-stu-id="e0255-252">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)'.</span></span>
    * <span data-ttu-id="e0255-253">选择 Proseware, Inc 拥有的 BACS（英国虚构）配置。</span><span class="sxs-lookup"><span data-stu-id="e0255-253">Select the BACS (UK fictitious custom) configuration, which is owned by Proseware, Inc.</span></span>  
    * <span data-ttu-id="e0255-254">使用所选配置的草稿版本以引入所需的更改。</span><span class="sxs-lookup"><span data-stu-id="e0255-254">Use the draft version of the selected configuration to introduce required changes.</span></span>  
8. <span data-ttu-id="e0255-255">单击“重定基本值”。</span><span class="sxs-lookup"><span data-stu-id="e0255-255">Click Rebase.</span></span>
    * <span data-ttu-id="e0255-256">选择基本配置的新版本 1.2 用作更新配置的新基准。</span><span class="sxs-lookup"><span data-stu-id="e0255-256">Select the new version 1.2 of the base configuration to be applied as a new base for updating the configuration.</span></span>  
9. <span data-ttu-id="e0255-257">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e0255-257">Click OK.</span></span>
    * <span data-ttu-id="e0255-258">请注意，已在合并自定义版本和表示不能自动合并的一些格式更改的新基本版本之间发现某些冲突。</span><span class="sxs-lookup"><span data-stu-id="e0255-258">Note that some conflicts have been discovered between merging the custom version and a new base version representing some format changes that can’t be merged automatically.</span></span>  

## <a name="resolve-rebase-conflicts"></a><span data-ttu-id="e0255-259">解决重定基本值冲突</span><span class="sxs-lookup"><span data-stu-id="e0255-259">Resolve rebase conflicts</span></span>
1. <span data-ttu-id="e0255-260">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="e0255-260">Click Designer.</span></span>
    * <span data-ttu-id="e0255-261">请注意，无法自动解决对供应商名称文本长度限制的更改。</span><span class="sxs-lookup"><span data-stu-id="e0255-261">Note that changes to the vendor’s name text length limit couldn’t be resolved automatically.</span></span> <span data-ttu-id="e0255-262">因此，这在冲突列表中呈现。</span><span class="sxs-lookup"><span data-stu-id="e0255-262">Therefore, this is presented in a conflicts list.</span></span> <span data-ttu-id="e0255-263">对于每个“更新”类型的冲突，提供以下选项：- 应用之前的基值（网格顶部的按钮）以引入以前的基本版本值（我们的案例中是 0）。</span><span class="sxs-lookup"><span data-stu-id="e0255-263">For each conflict of type Update, the following options are available:  - Apply a prior base value (button on top of the grid) to bring in the previous base version value (0 in our case).</span></span>  <span data-ttu-id="e0255-264">- 应用基值（网格顶部的按钮）以引入新的基本版本值（我们的案例中是 100）。</span><span class="sxs-lookup"><span data-stu-id="e0255-264">- Apply a base value (button on top of the grid) to bring in the new base version value (100 in our case).</span></span>  <span data-ttu-id="e0255-265">- 保留自己的（自定义）值（我们的示例值为 60）。</span><span class="sxs-lookup"><span data-stu-id="e0255-265">- Keep your own (custom) value (60 in our case).</span></span>  <span data-ttu-id="e0255-266">单击“应用基值”为供应商名称文本长度应用 100 个字符的国家/地区特定限制。</span><span class="sxs-lookup"><span data-stu-id="e0255-266">Click Apply base value to apply a country-specific limit of 100 characters for vendor’s name text length.</span></span>  
    * <span data-ttu-id="e0255-267">请注意，Proseware 公司和 Litware 公司具有使用 IBAN 和 SWIFT 代码（具有以管理格式自动合并的相关组件）的此格式的自定义和本地版本。</span><span class="sxs-lookup"><span data-stu-id="e0255-267">Note that Proseware, Inc. and Litware, Inc. have custom and local versions of this format using IBAN and SWIFT codes with related components that are automatically merged in the managing format.</span></span>  
2. <span data-ttu-id="e0255-268">单击“应用基值”。</span><span class="sxs-lookup"><span data-stu-id="e0255-268">Click Apply base value.</span></span>
    * <span data-ttu-id="e0255-269">单击“应用基值”为供应商名称应用 100 个字符的国家/地区特定限制。</span><span class="sxs-lookup"><span data-stu-id="e0255-269">Click Apply base value to apply the country-specific limit of 100 characters for vendor names.</span></span>  
3. <span data-ttu-id="e0255-270">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="e0255-270">Click Save.</span></span>
    * <span data-ttu-id="e0255-271">保存该格式将从冲突列表中删除已解决的冲突。</span><span class="sxs-lookup"><span data-stu-id="e0255-271">Saving the format will remove resolved conflicts from the conflicts list.</span></span>  
4. <span data-ttu-id="e0255-272">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e0255-272">Close the page.</span></span>

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a><span data-ttu-id="e0255-273">更改自定义格式配置的新版本状态</span><span class="sxs-lookup"><span data-stu-id="e0255-273">Change the status of the new version of the custom format configuration</span></span>
1. <span data-ttu-id="e0255-274">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="e0255-274">Click Change status.</span></span>
    * <span data-ttu-id="e0255-275">将更新的自定义格式配置的状态从“草稿”更改为“已完成”。</span><span class="sxs-lookup"><span data-stu-id="e0255-275">Change the status of the updated, custom format configuration from Draft to Completed.</span></span> <span data-ttu-id="e0255-276">这将使格式配置可用于生成付款单据。</span><span class="sxs-lookup"><span data-stu-id="e0255-276">This will make the format configuration available for generating payment documents.</span></span> <span data-ttu-id="e0255-277">请注意，所选配置的当前版本为“草稿”状态。</span><span class="sxs-lookup"><span data-stu-id="e0255-277">Note that the current version of the selected configuration is in Draft status.</span></span>  
2. <span data-ttu-id="e0255-278">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="e0255-278">Click Complete.</span></span>
3. <span data-ttu-id="e0255-279">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e0255-279">In the Description field, type a value.</span></span>
4. <span data-ttu-id="e0255-280">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e0255-280">Click OK.</span></span>
    * <span data-ttu-id="e0255-281">请注意，已创建的配置保存为已完成的版本 1.2.2：基本 BACS（英国虚构自定义）格式的版本 2，基于基本 BACS（英国虚构）格式的版本 2，基于付款（简化模型）数据模型的版本 1。</span><span class="sxs-lookup"><span data-stu-id="e0255-281">Note that the created configuration is saved as completed version 1.2.2: version 2 of base BACS (UK fictitious custom) format, which is based on version 2 of base BACS (UK fictitious) format, which is based on version 1 of Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-for-payment-files-generation"></a><span data-ttu-id="e0255-282">测试付款文件生成的自定义格式</span><span class="sxs-lookup"><span data-stu-id="e0255-282">Test the customized format for payment files generation</span></span>
    * <span data-ttu-id="e0255-283">在一个并行 Finance and Operations 会话中完成“使用创建的格式生成付款电子单据”过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="e0255-283">Complete the steps in the “Use created format to generate electronic documents for payments” procedure in parallel Finance and Operations session.</span></span> <span data-ttu-id="e0255-284">在电子付款方式参数中选择已创建的“BACS（英国虚构自定义）”格式。</span><span class="sxs-lookup"><span data-stu-id="e0255-284">Select the created ‘BACS (UK fictitious custom)’ format in electronic payment method parameters.</span></span> <span data-ttu-id="e0255-285">确保创建的付款文件包含 Proseware 公司最近引入的根据区域要求呈现 IBAN 帐户代码的 XML 代码。</span><span class="sxs-lookup"><span data-stu-id="e0255-285">Make sure that the created payment file contains recently introduced by Proseware, Inc. XML node presenting IBAN account code in accordance to regional requirements.</span></span> <span data-ttu-id="e0255-286">该文件还应包含 Litware 公司近期根据国家/地区要求引入的 呈现 SWIFT 银行代码到的 XML 节点。</span><span class="sxs-lookup"><span data-stu-id="e0255-286">The file also should contain the recently introduced by Litware, Inc. XML node presenting SWIFT bank code in accordance to country requirements.</span></span>  


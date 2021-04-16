---
title: ER 在格式输出中使用票据管理文件（第 3 部分 - 创建格式）
description: 本主题介绍如何配置电子报告格式以在 ER 输出中使用文档管理文件。 （第 3 部分）
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99a286b4e40ddeb7f4ff37c1ece3c678b26c838b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755002"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="d0655-104">ER 在格式输出中使用票据管理文件（第 3 部分 - 创建格式）</span><span class="sxs-lookup"><span data-stu-id="d0655-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d0655-105">以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。</span><span class="sxs-lookup"><span data-stu-id="d0655-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="d0655-106">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="d0655-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="d0655-107">若要完成这些步骤，必须首先完成“ER 在格式输出中使用票据管理文件（第 2 部分：扩展数据模型）”过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="d0655-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="d0655-108">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="d0655-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="d0655-109">创建用于处理发票的格式</span><span class="sxs-lookup"><span data-stu-id="d0655-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="d0655-110">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="d0655-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="d0655-111">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="d0655-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="d0655-112">在树中，展开“客户发票模型”。</span><span class="sxs-lookup"><span data-stu-id="d0655-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="d0655-113">在树中，选择“客户发票模型\客户发票模型(自定义)”。</span><span class="sxs-lookup"><span data-stu-id="d0655-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="d0655-114">您将创建格式，以便使用有关已附加到与以电子方式处理发票的销售订单的任何文件有关的信息生成电子消息。</span><span class="sxs-lookup"><span data-stu-id="d0655-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="d0655-115">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d0655-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="d0655-116">在“新建”字段中，输入“格式基于数据模型客户发票模型（自定义）”。</span><span class="sxs-lookup"><span data-stu-id="d0655-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="d0655-117">在“名称”字段中，键入“电子发票示例消息”。</span><span class="sxs-lookup"><span data-stu-id="d0655-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="d0655-118">电子发票示例消息</span><span class="sxs-lookup"><span data-stu-id="d0655-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="d0655-119">在“数据模型定义”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d0655-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="d0655-120">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="d0655-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="d0655-121">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="d0655-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="d0655-122">设计格式以将附件填充到生成的 MIME 格式的消息中</span><span class="sxs-lookup"><span data-stu-id="d0655-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="d0655-123">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="d0655-123">Click Designer.</span></span>
2. <span data-ttu-id="d0655-124">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d0655-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="d0655-125">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="d0655-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="d0655-126">在“名称”字段中，键入“发票”。</span><span class="sxs-lookup"><span data-stu-id="d0655-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="d0655-127">开票</span><span class="sxs-lookup"><span data-stu-id="d0655-127">Invoice</span></span>  
5. <span data-ttu-id="d0655-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d0655-128">Click OK.</span></span>
6. <span data-ttu-id="d0655-129">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d0655-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="d0655-130">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="d0655-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="d0655-131">在“名称”字段中，键入“SalesOrder”。</span><span class="sxs-lookup"><span data-stu-id="d0655-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="d0655-132">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="d0655-132">SalesOrder</span></span>  
9. <span data-ttu-id="d0655-133">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d0655-133">Click OK.</span></span>
10. <span data-ttu-id="d0655-134">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="d0655-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="d0655-135">在“名称”字段中，键入“InvoiceNumber”。</span><span class="sxs-lookup"><span data-stu-id="d0655-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="d0655-136">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="d0655-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="d0655-137">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d0655-137">Click OK.</span></span>
13. <span data-ttu-id="d0655-138">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="d0655-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="d0655-139">在“名称”字段中，键入“InvoiceAmount”。</span><span class="sxs-lookup"><span data-stu-id="d0655-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="d0655-140">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="d0655-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="d0655-141">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d0655-141">Click OK.</span></span>
16. <span data-ttu-id="d0655-142">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d0655-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="d0655-143">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="d0655-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="d0655-144">在“名称”字段中，键入“EnclosedDocs”。</span><span class="sxs-lookup"><span data-stu-id="d0655-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="d0655-145">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="d0655-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="d0655-146">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d0655-146">Click OK.</span></span>
20. <span data-ttu-id="d0655-147">在树中，选择“发票\EnclosedDocs”。</span><span class="sxs-lookup"><span data-stu-id="d0655-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="d0655-148">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="d0655-148">Click Add Element.</span></span>
22. <span data-ttu-id="d0655-149">在“名称”字段中，键入“票据”。</span><span class="sxs-lookup"><span data-stu-id="d0655-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="d0655-150">原始凭证</span><span class="sxs-lookup"><span data-stu-id="d0655-150">Document</span></span>  
23. <span data-ttu-id="d0655-151">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d0655-151">Click OK.</span></span>
24. <span data-ttu-id="d0655-152">在树中，选择“发票\EnclosedDocs\票据”。</span><span class="sxs-lookup"><span data-stu-id="d0655-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="d0655-153">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d0655-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="d0655-154">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="d0655-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="d0655-155">在“名称”字段中，键入“FileName”。</span><span class="sxs-lookup"><span data-stu-id="d0655-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="d0655-156">FileName</span><span class="sxs-lookup"><span data-stu-id="d0655-156">FileName</span></span>  
28. <span data-ttu-id="d0655-157">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d0655-157">Click OK.</span></span>
29. <span data-ttu-id="d0655-158">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d0655-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="d0655-159">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="d0655-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="d0655-160">在“名称”字段中，键入“FileContent”。</span><span class="sxs-lookup"><span data-stu-id="d0655-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="d0655-161">FileContent</span><span class="sxs-lookup"><span data-stu-id="d0655-161">FileContent</span></span>  
32. <span data-ttu-id="d0655-162">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d0655-162">Click OK.</span></span>
33. <span data-ttu-id="d0655-163">在树中，选择“发票\EnclosedDocs\票据\FileContent”。</span><span class="sxs-lookup"><span data-stu-id="d0655-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="d0655-164">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d0655-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="d0655-165">在树中，选择“文本\Base64”。</span><span class="sxs-lookup"><span data-stu-id="d0655-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="d0655-166">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d0655-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="d0655-167">将格式元素映射到数据模型充当数据源</span><span class="sxs-lookup"><span data-stu-id="d0655-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="d0655-168">在树中，选择“发票\SalesOrder”。</span><span class="sxs-lookup"><span data-stu-id="d0655-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="d0655-169">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="d0655-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="d0655-170">在树中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="d0655-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="d0655-171">在树中，选择“模型\销售订单编号(SalesId)”。</span><span class="sxs-lookup"><span data-stu-id="d0655-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="d0655-172">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="d0655-172">Click Bind.</span></span>
6. <span data-ttu-id="d0655-173">在树中，选择“发票\InvoiceNumber”。</span><span class="sxs-lookup"><span data-stu-id="d0655-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="d0655-174">在树中，展开“模型\基础发票(InvoiceBase)”。</span><span class="sxs-lookup"><span data-stu-id="d0655-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="d0655-175">在树中，选择“模型\基础发票(InvoiceBase)\发票编号(Id)”。</span><span class="sxs-lookup"><span data-stu-id="d0655-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="d0655-176">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="d0655-176">Click Bind.</span></span>
10. <span data-ttu-id="d0655-177">在树中，选择“发票\InvoiceAmount”。</span><span class="sxs-lookup"><span data-stu-id="d0655-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="d0655-178">在树中，选择“模型\基础发票(InvoiceBase)\发票金额(Amount)”。</span><span class="sxs-lookup"><span data-stu-id="d0655-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="d0655-179">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="d0655-179">Click Bind.</span></span>
13. <span data-ttu-id="d0655-180">在树中，展开“模型\发票附件”。</span><span class="sxs-lookup"><span data-stu-id="d0655-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="d0655-181">在树中，选择“模型\发票附件\文件内容”。</span><span class="sxs-lookup"><span data-stu-id="d0655-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="d0655-182">在树中，选择“发票\EnclosedDocs\票据\FileContent\Base64”。</span><span class="sxs-lookup"><span data-stu-id="d0655-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="d0655-183">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="d0655-183">Click Bind.</span></span>
17. <span data-ttu-id="d0655-184">在树中，选择“模型\发票附件\文件名”。</span><span class="sxs-lookup"><span data-stu-id="d0655-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="d0655-185">在树中，选择“发票\EnclosedDocs\票据\FileName”。</span><span class="sxs-lookup"><span data-stu-id="d0655-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="d0655-186">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="d0655-186">Click Bind.</span></span>
20. <span data-ttu-id="d0655-187">在树中，选择“模型\发票附件”。</span><span class="sxs-lookup"><span data-stu-id="d0655-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="d0655-188">在树中，选择“发票\EnclosedDocs\票据”。</span><span class="sxs-lookup"><span data-stu-id="d0655-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="d0655-189">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="d0655-189">Click Bind.</span></span>
23. <span data-ttu-id="d0655-190">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d0655-190">Click Save.</span></span>
24. <span data-ttu-id="d0655-191">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d0655-191">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
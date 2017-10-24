--- 
title: "针对电子申报 (ER) 创建在格式输出中使用票据管理文件的格式"
description: "以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。"
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.openlocfilehash: 71e40351e8b54092d1bbcbc73c6da69073791b74
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="d4504-103">针对电子申报 (ER) 创建在格式输出中使用票据管理文件的格式</span><span class="sxs-lookup"><span data-stu-id="d4504-103">Create format to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4504-104">以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。</span><span class="sxs-lookup"><span data-stu-id="d4504-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="d4504-105">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="d4504-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="d4504-106">若要完成这些步骤，必须首先完成“ER 在格式输出中使用票据管理文件（第 2 部分：扩展数据模型）”过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="d4504-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="d4504-107">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="d4504-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="d4504-108">创建用于处理发票的格式</span><span class="sxs-lookup"><span data-stu-id="d4504-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="d4504-109">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="d4504-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="d4504-110">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="d4504-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="d4504-111">在树中，展开“客户发票模型”。</span><span class="sxs-lookup"><span data-stu-id="d4504-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="d4504-112">在树中，选择“客户发票模型\客户发票模型(自定义)”。</span><span class="sxs-lookup"><span data-stu-id="d4504-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="d4504-113">您将创建格式，以便使用有关已附加到与以电子方式处理发票的销售订单的任何文件有关的信息生成电子消息。</span><span class="sxs-lookup"><span data-stu-id="d4504-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="d4504-114">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d4504-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="d4504-115">在“新建”字段中，输入“格式基于数据模型客户发票模型（自定义）”。</span><span class="sxs-lookup"><span data-stu-id="d4504-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="d4504-116">在“名称”字段中，键入“电子发票示例消息”。</span><span class="sxs-lookup"><span data-stu-id="d4504-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="d4504-117">电子发票示例消息</span><span class="sxs-lookup"><span data-stu-id="d4504-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="d4504-118">在“数据模型定义”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d4504-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="d4504-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="d4504-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="d4504-120">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="d4504-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="d4504-121">设计格式以将附件填充到生成的 MIME 格式的消息中</span><span class="sxs-lookup"><span data-stu-id="d4504-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="d4504-122">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="d4504-122">Click Designer.</span></span>
2. <span data-ttu-id="d4504-123">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d4504-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="d4504-124">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="d4504-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="d4504-125">在“名称”字段中，键入“发票”。</span><span class="sxs-lookup"><span data-stu-id="d4504-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="d4504-126">开票</span><span class="sxs-lookup"><span data-stu-id="d4504-126">Invoice</span></span>  
5. <span data-ttu-id="d4504-127">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d4504-127">Click OK.</span></span>
6. <span data-ttu-id="d4504-128">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d4504-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="d4504-129">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="d4504-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="d4504-130">在“名称”字段中，键入“SalesOrder”。</span><span class="sxs-lookup"><span data-stu-id="d4504-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="d4504-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="d4504-131">SalesOrder</span></span>  
9. <span data-ttu-id="d4504-132">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d4504-132">Click OK.</span></span>
10. <span data-ttu-id="d4504-133">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="d4504-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="d4504-134">在“名称”字段中，键入“InvoiceNumber”。</span><span class="sxs-lookup"><span data-stu-id="d4504-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="d4504-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="d4504-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="d4504-136">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d4504-136">Click OK.</span></span>
13. <span data-ttu-id="d4504-137">单击“添加属性”。</span><span class="sxs-lookup"><span data-stu-id="d4504-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="d4504-138">在“名称”字段中，键入“InvoiceAmount”。</span><span class="sxs-lookup"><span data-stu-id="d4504-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="d4504-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="d4504-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="d4504-140">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d4504-140">Click OK.</span></span>
16. <span data-ttu-id="d4504-141">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d4504-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="d4504-142">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="d4504-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="d4504-143">在“名称”字段中，键入“EnclosedDocs”。</span><span class="sxs-lookup"><span data-stu-id="d4504-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="d4504-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="d4504-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="d4504-145">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d4504-145">Click OK.</span></span>
20. <span data-ttu-id="d4504-146">在树中，选择“发票\EnclosedDocs”。</span><span class="sxs-lookup"><span data-stu-id="d4504-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="d4504-147">单击“添加元素”。</span><span class="sxs-lookup"><span data-stu-id="d4504-147">Click Add Element.</span></span>
22. <span data-ttu-id="d4504-148">在“名称”字段中，键入“票据”。</span><span class="sxs-lookup"><span data-stu-id="d4504-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="d4504-149">原始凭证</span><span class="sxs-lookup"><span data-stu-id="d4504-149">Document</span></span>  
23. <span data-ttu-id="d4504-150">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d4504-150">Click OK.</span></span>
24. <span data-ttu-id="d4504-151">在树中，选择“发票\EnclosedDocs\票据”。</span><span class="sxs-lookup"><span data-stu-id="d4504-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="d4504-152">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d4504-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="d4504-153">在树结构中，选择“Xml：文件\属性”。</span><span class="sxs-lookup"><span data-stu-id="d4504-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="d4504-154">在“名称”字段中，键入“FileName”。</span><span class="sxs-lookup"><span data-stu-id="d4504-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="d4504-155">FileName</span><span class="sxs-lookup"><span data-stu-id="d4504-155">FileName</span></span>  
28. <span data-ttu-id="d4504-156">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d4504-156">Click OK.</span></span>
29. <span data-ttu-id="d4504-157">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d4504-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="d4504-158">在树结构中，选择“XML\元素”。</span><span class="sxs-lookup"><span data-stu-id="d4504-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="d4504-159">在“名称”字段中，键入“FileContent”。</span><span class="sxs-lookup"><span data-stu-id="d4504-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="d4504-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="d4504-160">FileContent</span></span>  
32. <span data-ttu-id="d4504-161">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d4504-161">Click OK.</span></span>
33. <span data-ttu-id="d4504-162">在树中，选择“发票\EnclosedDocs\票据\FileContent”。</span><span class="sxs-lookup"><span data-stu-id="d4504-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="d4504-163">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d4504-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="d4504-164">在树中，选择“文本\Base64”。</span><span class="sxs-lookup"><span data-stu-id="d4504-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="d4504-165">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d4504-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="d4504-166">将格式元素映射到数据模型充当数据源</span><span class="sxs-lookup"><span data-stu-id="d4504-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="d4504-167">在树中，选择“发票\SalesOrder”。</span><span class="sxs-lookup"><span data-stu-id="d4504-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="d4504-168">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="d4504-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="d4504-169">在树中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="d4504-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="d4504-170">在树中，选择“模型\销售订单编号(SalesId)”。</span><span class="sxs-lookup"><span data-stu-id="d4504-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="d4504-171">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="d4504-171">Click Bind.</span></span>
6. <span data-ttu-id="d4504-172">在树中，选择“发票\InvoiceNumber”。</span><span class="sxs-lookup"><span data-stu-id="d4504-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="d4504-173">在树中，展开“模型\基础发票(InvoiceBase)”。</span><span class="sxs-lookup"><span data-stu-id="d4504-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="d4504-174">在树中，选择“模型\基础发票(InvoiceBase)\发票编号(Id)”。</span><span class="sxs-lookup"><span data-stu-id="d4504-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="d4504-175">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="d4504-175">Click Bind.</span></span>
10. <span data-ttu-id="d4504-176">在树中，选择“发票\InvoiceAmount”。</span><span class="sxs-lookup"><span data-stu-id="d4504-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="d4504-177">在树中，选择“模型\基础发票(InvoiceBase)\发票金额(Amount)”。</span><span class="sxs-lookup"><span data-stu-id="d4504-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="d4504-178">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="d4504-178">Click Bind.</span></span>
13. <span data-ttu-id="d4504-179">在树中，展开“模型\发票附件”。</span><span class="sxs-lookup"><span data-stu-id="d4504-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="d4504-180">在树中，选择“模型\发票附件\文件内容”。</span><span class="sxs-lookup"><span data-stu-id="d4504-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="d4504-181">在树中，选择“发票\EnclosedDocs\票据\FileContent\Base64”。</span><span class="sxs-lookup"><span data-stu-id="d4504-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="d4504-182">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="d4504-182">Click Bind.</span></span>
17. <span data-ttu-id="d4504-183">在树中，选择“模型\发票附件\文件名”。</span><span class="sxs-lookup"><span data-stu-id="d4504-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="d4504-184">在树中，选择“发票\EnclosedDocs\票据\FileName”。</span><span class="sxs-lookup"><span data-stu-id="d4504-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="d4504-185">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="d4504-185">Click Bind.</span></span>
20. <span data-ttu-id="d4504-186">在树中，选择“模型\发票附件”。</span><span class="sxs-lookup"><span data-stu-id="d4504-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="d4504-187">在树中，选择“发票\EnclosedDocs\票据”。</span><span class="sxs-lookup"><span data-stu-id="d4504-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="d4504-188">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="d4504-188">Click Bind.</span></span>
23. <span data-ttu-id="d4504-189">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d4504-189">Click Save.</span></span>
24. <span data-ttu-id="d4504-190">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d4504-190">Close the page.</span></span>


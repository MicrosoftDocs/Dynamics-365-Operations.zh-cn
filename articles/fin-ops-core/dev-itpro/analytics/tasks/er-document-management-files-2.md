---
title: ER 在格式输出中使用票据管理文件（第 2 部分 - 扩展数据模型）
description: 本主题介绍如何配置电子报告 (ER) 格式以在 ER 输出中使用文档管理文件（附件）。 （第 2 部分）
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd06cdfd9bae57577c2e3ec97848e319b197f41
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092582"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="87c2d-104">ER 在格式输出中使用票据管理文件（第 2 部分 - 扩展数据模型）</span><span class="sxs-lookup"><span data-stu-id="87c2d-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="87c2d-105">以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。</span><span class="sxs-lookup"><span data-stu-id="87c2d-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="87c2d-106">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="87c2d-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="87c2d-107">若要完成这些步骤，必须首先完成“ER 在格式输出中使用票据管理文件（第 1 部分：准备数据模型）”任务指南中的步骤。</span><span class="sxs-lookup"><span data-stu-id="87c2d-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="87c2d-108">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="87c2d-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="87c2d-109">展开数据模型以在其中显示票据管理文件</span><span class="sxs-lookup"><span data-stu-id="87c2d-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="87c2d-110">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="87c2d-111">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="87c2d-112">在树中，展开“客户发票模型”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="87c2d-113">在树中，选择“客户发票模型\客户发票模型(自定义)”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="87c2d-114">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-114">Click Designer.</span></span>
6. <span data-ttu-id="87c2d-115">在树中，选择“客户发票(InvoiceCustomer)”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="87c2d-116">您将扩展此数据模型以在其中显示已附加到与电子方式处理的发票有关的销售订单的任何文件。</span><span class="sxs-lookup"><span data-stu-id="87c2d-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="87c2d-117">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="87c2d-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="87c2d-118">在“名称”字段中，键入“发票附件”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="87c2d-119">发票附件</span><span class="sxs-lookup"><span data-stu-id="87c2d-119">Invoice attachments</span></span>  
9. <span data-ttu-id="87c2d-120">在“物料类型”字段中，选择“记录列表”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="87c2d-121">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-121">Click Add.</span></span>
11. <span data-ttu-id="87c2d-122">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="87c2d-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="87c2d-123">在“名称”字段中，键入“文件内容”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="87c2d-124">文件内容</span><span class="sxs-lookup"><span data-stu-id="87c2d-124">File content</span></span>  
13. <span data-ttu-id="87c2d-125">在“物料类型”字段中，选择“集装箱”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="87c2d-126">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-126">Click Add.</span></span>
15. <span data-ttu-id="87c2d-127">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="87c2d-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="87c2d-128">在“名称”字段中，键入“文件名”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="87c2d-129">文件名</span><span class="sxs-lookup"><span data-stu-id="87c2d-129">File name</span></span>  
17. <span data-ttu-id="87c2d-130">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="87c2d-131">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="87c2d-132">将新数据模型元素映射到数据源</span><span class="sxs-lookup"><span data-stu-id="87c2d-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="87c2d-133">单击“映射模型到数据源”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="87c2d-134">使用快速筛选来筛选值为“InvoiceCustomer”的“定义”字段。</span><span class="sxs-lookup"><span data-stu-id="87c2d-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="87c2d-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="87c2d-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="87c2d-136">我们将把新模型元素映射到相应数据源。</span><span class="sxs-lookup"><span data-stu-id="87c2d-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="87c2d-137">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-137">Click Designer.</span></span>
4. <span data-ttu-id="87c2d-138">在树中，选择“发票附件”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="87c2d-139">在树中，展开“发票附件”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="87c2d-140">在树中，选择“发票附件\文件名”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="87c2d-141">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-141">Click Edit.</span></span>
8. <span data-ttu-id="87c2d-142">在“公式”字段中，输入“CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="87c2d-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="87c2d-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="87c2d-144">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-144">Click Save.</span></span>
10. <span data-ttu-id="87c2d-145">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="87c2d-145">Close the page.</span></span>
11. <span data-ttu-id="87c2d-146">在树中，选择“发票附件\文件内容”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="87c2d-147">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-147">Click Edit.</span></span>
13. <span data-ttu-id="87c2d-148">在“公式”字段中，输入“CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="87c2d-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="87c2d-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="87c2d-150">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-150">Click Save.</span></span>
15. <span data-ttu-id="87c2d-151">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="87c2d-151">Close the page.</span></span>
16. <span data-ttu-id="87c2d-152">在树中，选择“发票附件”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="87c2d-153">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-153">Click Edit.</span></span>
18. <span data-ttu-id="87c2d-154">在“公式”字段中，输入“CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="87c2d-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="87c2d-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="87c2d-156">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-156">Click Save.</span></span>
20. <span data-ttu-id="87c2d-157">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="87c2d-157">Close the page.</span></span>
21. <span data-ttu-id="87c2d-158">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-158">Click Save.</span></span>
22. <span data-ttu-id="87c2d-159">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="87c2d-159">Close the page.</span></span>
23. <span data-ttu-id="87c2d-160">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="87c2d-160">Close the page.</span></span>
24. <span data-ttu-id="87c2d-161">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="87c2d-161">Close the page.</span></span>
25. <span data-ttu-id="87c2d-162">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-162">Click Change status.</span></span>
26. <span data-ttu-id="87c2d-163">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-163">Click Complete.</span></span>
27. <span data-ttu-id="87c2d-164">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="87c2d-164">Click OK.</span></span>


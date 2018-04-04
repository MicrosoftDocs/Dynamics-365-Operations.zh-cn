--- 
title: "针对电子申报 (ER) 将数据模型扩展为在格式输出中使用票据管理文件"
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ebbd442c9f69290dc995c05462ca70b554f7d9f2
ms.contentlocale: zh-cn
ms.lasthandoff: 03/26/2018

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="57c6f-103">针对电子申报 (ER) 将数据模型扩展为在格式输出中使用票据管理文件</span><span class="sxs-lookup"><span data-stu-id="57c6f-103">Extend data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="57c6f-104">以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。</span><span class="sxs-lookup"><span data-stu-id="57c6f-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="57c6f-105">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="57c6f-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="57c6f-106">若要完成这些步骤，必须首先完成“ER 在格式输出中使用票据管理文件（第 1 部分：准备数据模型）”任务指南中的步骤。</span><span class="sxs-lookup"><span data-stu-id="57c6f-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="57c6f-107">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="57c6f-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="57c6f-108">展开数据模型以在其中显示票据管理文件</span><span class="sxs-lookup"><span data-stu-id="57c6f-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="57c6f-109">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="57c6f-110">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="57c6f-111">在树中，展开“客户发票模型”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="57c6f-112">在树中，选择“客户发票模型\客户发票模型(自定义)”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="57c6f-113">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-113">Click Designer.</span></span>
6. <span data-ttu-id="57c6f-114">在树中，选择“客户发票(InvoiceCustomer)”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="57c6f-115">您将扩展此数据模型以在其中显示已附加到与电子方式处理的发票有关的销售订单的任何文件。</span><span class="sxs-lookup"><span data-stu-id="57c6f-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="57c6f-116">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="57c6f-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="57c6f-117">在“名称”字段中，键入“发票附件”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="57c6f-118">发票附件</span><span class="sxs-lookup"><span data-stu-id="57c6f-118">Invoice attachments</span></span>  
9. <span data-ttu-id="57c6f-119">在“物料类型”字段中，选择“记录列表”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="57c6f-120">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-120">Click Add.</span></span>
11. <span data-ttu-id="57c6f-121">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="57c6f-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="57c6f-122">在“名称”字段中，键入“文件内容”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="57c6f-123">文件内容</span><span class="sxs-lookup"><span data-stu-id="57c6f-123">File content</span></span>  
13. <span data-ttu-id="57c6f-124">在“物料类型”字段中，选择“集装箱”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="57c6f-125">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-125">Click Add.</span></span>
15. <span data-ttu-id="57c6f-126">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="57c6f-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="57c6f-127">在“名称”字段中，键入“文件名”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="57c6f-128">文件名</span><span class="sxs-lookup"><span data-stu-id="57c6f-128">File name</span></span>  
17. <span data-ttu-id="57c6f-129">在“物料类型”字段中，选择“字符串”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="57c6f-130">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a><span data-ttu-id="57c6f-131">将新数据模型元素映射到 Dynamics 365 for Finance and Operations 数据源</span><span class="sxs-lookup"><span data-stu-id="57c6f-131">Map new data model elements to Dynamics 365 for Finance and Operations data sources</span></span>
1. <span data-ttu-id="57c6f-132">单击“映射模型到数据源”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="57c6f-133">使用快速筛选来筛选值为“InvoiceCustomer”的“定义”字段。</span><span class="sxs-lookup"><span data-stu-id="57c6f-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="57c6f-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="57c6f-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="57c6f-135">我们将把新模型元素映射到相应数据源。</span><span class="sxs-lookup"><span data-stu-id="57c6f-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="57c6f-136">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-136">Click Designer.</span></span>
4. <span data-ttu-id="57c6f-137">在树中，选择“发票附件”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="57c6f-138">在树中，展开“发票附件”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="57c6f-139">在树中，选择“发票附件\文件名”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="57c6f-140">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-140">Click Edit.</span></span>
8. <span data-ttu-id="57c6f-141">在“公式”字段中，输入“CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="57c6f-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="57c6f-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="57c6f-143">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-143">Click Save.</span></span>
10. <span data-ttu-id="57c6f-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="57c6f-144">Close the page.</span></span>
11. <span data-ttu-id="57c6f-145">在树中，选择“发票附件\文件内容”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="57c6f-146">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-146">Click Edit.</span></span>
13. <span data-ttu-id="57c6f-147">在“公式”字段中，输入“CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="57c6f-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="57c6f-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="57c6f-149">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-149">Click Save.</span></span>
15. <span data-ttu-id="57c6f-150">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="57c6f-150">Close the page.</span></span>
16. <span data-ttu-id="57c6f-151">在树中，选择“发票附件”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="57c6f-152">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-152">Click Edit.</span></span>
18. <span data-ttu-id="57c6f-153">在“公式”字段中，输入“CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="57c6f-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="57c6f-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="57c6f-155">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-155">Click Save.</span></span>
20. <span data-ttu-id="57c6f-156">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="57c6f-156">Close the page.</span></span>
21. <span data-ttu-id="57c6f-157">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-157">Click Save.</span></span>
22. <span data-ttu-id="57c6f-158">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="57c6f-158">Close the page.</span></span>
23. <span data-ttu-id="57c6f-159">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="57c6f-159">Close the page.</span></span>
24. <span data-ttu-id="57c6f-160">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="57c6f-160">Close the page.</span></span>
25. <span data-ttu-id="57c6f-161">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-161">Click Change status.</span></span>
26. <span data-ttu-id="57c6f-162">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-162">Click Complete.</span></span>
27. <span data-ttu-id="57c6f-163">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="57c6f-163">Click OK.</span></span>



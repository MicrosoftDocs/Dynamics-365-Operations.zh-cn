---
title: ER 在格式输出中使用票据管理文件（第 4 部分 - 运行格式）
description: 本主题介绍如何配置电子报告格式以在 ER 输出中使用文档管理文件。 （第 4 部分）
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ede71118f64eec27b150a4c575aead97d3174509
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559717"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a><span data-ttu-id="ac32c-104">ER 在格式输出中使用票据管理文件（第 4 部分 - 运行格式）</span><span class="sxs-lookup"><span data-stu-id="ac32c-104">ER Use Document Management files in format outputs (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ac32c-105">以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。</span><span class="sxs-lookup"><span data-stu-id="ac32c-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="ac32c-106">这些步骤可以在 DEMF 公司执行。</span><span class="sxs-lookup"><span data-stu-id="ac32c-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="ac32c-107">若要完成这些步骤，必须首先完成“ER 在格式输出中使用票据管理文件（第 3 部分：创建格式）”过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="ac32c-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 3: Create format)" procedure.</span></span>

<span data-ttu-id="ac32c-108">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="ac32c-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="ac32c-109">添加单张发票的销售订单的必要附件</span><span class="sxs-lookup"><span data-stu-id="ac32c-109">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="ac32c-110">转至“应收帐款”>“发票”>“未结客户发票”。</span><span class="sxs-lookup"><span data-stu-id="ac32c-110">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="ac32c-111">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="ac32c-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ac32c-112">例如，在“发票”字段中用值“CIV-000148”进行筛选。</span><span class="sxs-lookup"><span data-stu-id="ac32c-112">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="ac32c-113">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="ac32c-113">CIV-000148</span></span>  
3. <span data-ttu-id="ac32c-114">单击以访问所选发票的链接。</span><span class="sxs-lookup"><span data-stu-id="ac32c-114">Click to follow the selected invoice's link.</span></span>
    * <span data-ttu-id="ac32c-115">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="ac32c-115">CIV-000148</span></span>  
4. <span data-ttu-id="ac32c-116">单击以访问“销售订单”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="ac32c-116">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="ac32c-117">000148</span><span class="sxs-lookup"><span data-stu-id="ac32c-117">000148</span></span>  
5. <span data-ttu-id="ac32c-118">在“行或标题”字段中，选择“标题”选项。</span><span class="sxs-lookup"><span data-stu-id="ac32c-118">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="ac32c-119">选择“标题”以表示这将是添加附件的目标。</span><span class="sxs-lookup"><span data-stu-id="ac32c-119">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="ac32c-120">单击“附加”。</span><span class="sxs-lookup"><span data-stu-id="ac32c-120">Click Attach.</span></span>
    * <span data-ttu-id="ac32c-121">将一些文件添加为此销售订单的附件。</span><span class="sxs-lookup"><span data-stu-id="ac32c-121">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="ac32c-122">使用票据管理支持的票据类型的文件（文件扩展名为 DOCX、DPF、XML、JPG 等）。</span><span class="sxs-lookup"><span data-stu-id="ac32c-122">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="ac32c-123">浏览并选择要附加并使用 ER 电子消息中的相关发票进一步处理的文件。</span><span class="sxs-lookup"><span data-stu-id="ac32c-123">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="ac32c-124">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ac32c-124">Click New.</span></span>
8. <span data-ttu-id="ac32c-125">单击“文件”。</span><span class="sxs-lookup"><span data-stu-id="ac32c-125">Click File.</span></span>
9. <span data-ttu-id="ac32c-126">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ac32c-126">Click New.</span></span>
10. <span data-ttu-id="ac32c-127">单击“文件”。</span><span class="sxs-lookup"><span data-stu-id="ac32c-127">Click File.</span></span>
11. <span data-ttu-id="ac32c-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ac32c-128">Close the page.</span></span>
12. <span data-ttu-id="ac32c-129">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ac32c-129">Close the page.</span></span>
13. <span data-ttu-id="ac32c-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ac32c-130">Close the page.</span></span>
14. <span data-ttu-id="ac32c-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ac32c-131">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="ac32c-132">运行为所选发票设计的报表</span><span class="sxs-lookup"><span data-stu-id="ac32c-132">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="ac32c-133">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="ac32c-133">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ac32c-134">在树中，展开“客户发票模型”。</span><span class="sxs-lookup"><span data-stu-id="ac32c-134">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="ac32c-135">在树中，展开“客户发票模型\客户发票模型(自定义)”。</span><span class="sxs-lookup"><span data-stu-id="ac32c-135">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="ac32c-136">在树中，选择“客户发票模型\客户发票模型(自定义)\电子发票示例消息”。</span><span class="sxs-lookup"><span data-stu-id="ac32c-136">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="ac32c-137">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="ac32c-137">Click Run.</span></span>
6. <span data-ttu-id="ac32c-138">展开“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="ac32c-138">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="ac32c-139">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="ac32c-139">Click Filter.</span></span>
8. <span data-ttu-id="ac32c-140">选择“客户发票日记帐”的行和“销售订单”字段。</span><span class="sxs-lookup"><span data-stu-id="ac32c-140">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="ac32c-141">在“标准”字段中，键入“000148”。</span><span class="sxs-lookup"><span data-stu-id="ac32c-141">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="ac32c-142">在条件的“销售订单”字段中，键入订单编号 000148。</span><span class="sxs-lookup"><span data-stu-id="ac32c-142">In the criteria "Sales order" field, type the order number 000148.</span></span>  
10. <span data-ttu-id="ac32c-143">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ac32c-143">Click OK.</span></span>
11. <span data-ttu-id="ac32c-144">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ac32c-144">Click OK.</span></span>
    * <span data-ttu-id="ac32c-145">检查生成的输出。</span><span class="sxs-lookup"><span data-stu-id="ac32c-145">Review the generated output.</span></span> <span data-ttu-id="ac32c-146">请注意，已经为每个附件创建了一个 XML 节点。</span><span class="sxs-lookup"><span data-stu-id="ac32c-146">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="ac32c-147">附件的内容填充到 MIME (base64) 文本格式的 XML 输出中。</span><span class="sxs-lookup"><span data-stu-id="ac32c-147">The attachment's content is populated to the XML output in MIME (base64) text format.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
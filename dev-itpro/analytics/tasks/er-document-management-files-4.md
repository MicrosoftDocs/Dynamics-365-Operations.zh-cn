--- 
title: "针对电子申报 (ER) 运行在格式输出中使用票据管理文件的格式"
description: "以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。"
author: NickSelin
manager: AnnBe
ms.date: 10/31/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 09eaf28b0f4ed93d602f84688369614c17502d95
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="run-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="6a181-103">针对电子申报 (ER) 运行在格式输出中使用票据管理文件的格式</span><span class="sxs-lookup"><span data-stu-id="6a181-103">Run format to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6a181-104">以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。</span><span class="sxs-lookup"><span data-stu-id="6a181-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="6a181-105">这些步骤可以在 DEMF 公司执行。</span><span class="sxs-lookup"><span data-stu-id="6a181-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="6a181-106">若要完成这些步骤，必须首先完成“ER 在格式输出中使用票据管理文件（第 3 部分：创建格式）”过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="6a181-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 3: Create format)” procedure.</span></span>

<span data-ttu-id="6a181-107">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="6a181-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="6a181-108">添加单张发票的销售订单的必要附件</span><span class="sxs-lookup"><span data-stu-id="6a181-108">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="6a181-109">转至“应收帐款”>“发票”>“未结客户发票”。</span><span class="sxs-lookup"><span data-stu-id="6a181-109">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="6a181-110">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="6a181-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6a181-111">例如，在“发票”字段中用值“CIV-000148”进行筛选。</span><span class="sxs-lookup"><span data-stu-id="6a181-111">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="6a181-112">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="6a181-112">CIV-000148</span></span>  
3. <span data-ttu-id="6a181-113">单击以访问所选发票的链接。</span><span class="sxs-lookup"><span data-stu-id="6a181-113">Click to follow the selected invoice’s link.</span></span>
    * <span data-ttu-id="6a181-114">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="6a181-114">CIV-000148</span></span>  
4. <span data-ttu-id="6a181-115">单击以访问“销售订单”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="6a181-115">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="6a181-116">000148</span><span class="sxs-lookup"><span data-stu-id="6a181-116">000148</span></span>  
5. <span data-ttu-id="6a181-117">在“行或标题”字段中，选择“标题”选项。</span><span class="sxs-lookup"><span data-stu-id="6a181-117">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="6a181-118">选择“标题”以表示这将是添加附件的目标。</span><span class="sxs-lookup"><span data-stu-id="6a181-118">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="6a181-119">单击“附加”。</span><span class="sxs-lookup"><span data-stu-id="6a181-119">Click Attach.</span></span>
    * <span data-ttu-id="6a181-120">将一些文件添加为此销售订单的附件。</span><span class="sxs-lookup"><span data-stu-id="6a181-120">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="6a181-121">使用票据管理支持的票据类型的文件（文件扩展名为 DOCX、DPF、XML、JPG 等）。</span><span class="sxs-lookup"><span data-stu-id="6a181-121">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="6a181-122">浏览并选择要附加并使用 ER 电子消息中的相关发票进一步处理的文件。</span><span class="sxs-lookup"><span data-stu-id="6a181-122">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="6a181-123">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="6a181-123">Click New.</span></span>
8. <span data-ttu-id="6a181-124">单击“文件”。</span><span class="sxs-lookup"><span data-stu-id="6a181-124">Click File.</span></span>
9. <span data-ttu-id="6a181-125">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="6a181-125">Click New.</span></span>
10. <span data-ttu-id="6a181-126">单击“文件”。</span><span class="sxs-lookup"><span data-stu-id="6a181-126">Click File.</span></span>
11. <span data-ttu-id="6a181-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6a181-127">Close the page.</span></span>
12. <span data-ttu-id="6a181-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6a181-128">Close the page.</span></span>
13. <span data-ttu-id="6a181-129">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6a181-129">Close the page.</span></span>
14. <span data-ttu-id="6a181-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6a181-130">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="6a181-131">运行为所选发票设计的报表</span><span class="sxs-lookup"><span data-stu-id="6a181-131">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="6a181-132">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="6a181-132">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="6a181-133">在树中，展开“客户发票模型”。</span><span class="sxs-lookup"><span data-stu-id="6a181-133">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="6a181-134">在树中，展开“客户发票模型\客户发票模型(自定义)”。</span><span class="sxs-lookup"><span data-stu-id="6a181-134">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="6a181-135">在树中，选择“客户发票模型\客户发票模型(自定义)\电子发票示例消息”。</span><span class="sxs-lookup"><span data-stu-id="6a181-135">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="6a181-136">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="6a181-136">Click Run.</span></span>
6. <span data-ttu-id="6a181-137">展开“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="6a181-137">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="6a181-138">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="6a181-138">Click Filter.</span></span>
8. <span data-ttu-id="6a181-139">选择“客户发票日记帐”的行和“销售订单”字段。</span><span class="sxs-lookup"><span data-stu-id="6a181-139">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="6a181-140">在“标准”字段中，键入“000148”。</span><span class="sxs-lookup"><span data-stu-id="6a181-140">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="6a181-141">在条件的“销售订单”字段中，键入订单编号 000148。</span><span class="sxs-lookup"><span data-stu-id="6a181-141">In the criteria “Sales order” field, type the order number 000148.</span></span>  
10. <span data-ttu-id="6a181-142">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6a181-142">Click OK.</span></span>
11. <span data-ttu-id="6a181-143">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6a181-143">Click OK.</span></span>
    * <span data-ttu-id="6a181-144">检查生成的输出。</span><span class="sxs-lookup"><span data-stu-id="6a181-144">Review the generated output.</span></span> <span data-ttu-id="6a181-145">请注意，已经为每个附件创建了一个 XML 节点。</span><span class="sxs-lookup"><span data-stu-id="6a181-145">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="6a181-146">附件的内容填充到 MIME (base64) 文本格式的 XML 输出中。</span><span class="sxs-lookup"><span data-stu-id="6a181-146">The attachment’s content is populated to the XML output in MIME (base64) text format.</span></span>  



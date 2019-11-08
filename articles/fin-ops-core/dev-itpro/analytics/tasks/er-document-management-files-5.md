---
title: ER 在格式输出中使用票据管理文件（第 5 部分 - 修改和运行格式）
description: 以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: de075899547d194fb9eb0e68947efd005c101851
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550686"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="ee673-103">ER 在格式输出中使用票据管理文件（第 5 部分 - 修改和运行格式）</span><span class="sxs-lookup"><span data-stu-id="ee673-103">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ee673-104">以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。</span><span class="sxs-lookup"><span data-stu-id="ee673-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="ee673-105">这些步骤可以在 DEMF 公司执行。</span><span class="sxs-lookup"><span data-stu-id="ee673-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="ee673-106">若要完成这些步骤，必须首先完成“ER 在格式输出中使用票据管理文件（第 4 部分：运行格式）”过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="ee673-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4: Run format)” procedure.</span></span>

<span data-ttu-id="ee673-107">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="ee673-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="ee673-108">修改格式以将附件填充到生成的二进制格式的消息中</span><span class="sxs-lookup"><span data-stu-id="ee673-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="ee673-109">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="ee673-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ee673-110">在树中，展开“客户发票模型”。</span><span class="sxs-lookup"><span data-stu-id="ee673-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="ee673-111">在树中，展开“客户发票模型\客户发票模型(自定义)”。</span><span class="sxs-lookup"><span data-stu-id="ee673-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="ee673-112">在树中，选择“客户发票模型\客户发票模型(自定义)\电子发票示例消息”。</span><span class="sxs-lookup"><span data-stu-id="ee673-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="ee673-113">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="ee673-113">Click Designer.</span></span>
    * <span data-ttu-id="ee673-114">您将使用 UNICODE 编码在生成的格式为 XML 文件的输出中填充发票消息。</span><span class="sxs-lookup"><span data-stu-id="ee673-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="ee673-115">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ee673-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="ee673-116">在树结构中，选择“常见\文件”。</span><span class="sxs-lookup"><span data-stu-id="ee673-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="ee673-117">在“名称”字段中，键入“Xml 消息”。</span><span class="sxs-lookup"><span data-stu-id="ee673-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="ee673-118">Xml 消息</span><span class="sxs-lookup"><span data-stu-id="ee673-118">Xml message</span></span>  
9. <span data-ttu-id="ee673-119">在“编码”字段中，键入“UTF-8”。</span><span class="sxs-lookup"><span data-stu-id="ee673-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="ee673-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="ee673-120">UTF-8</span></span>  
10. <span data-ttu-id="ee673-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee673-121">Click OK.</span></span>
    * <span data-ttu-id="ee673-122">将生成的输出配置为压缩文件。</span><span class="sxs-lookup"><span data-stu-id="ee673-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="ee673-123">单击“添加根”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ee673-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="ee673-124">在树中，选择“常见\文件夹”。</span><span class="sxs-lookup"><span data-stu-id="ee673-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="ee673-125">在“名称”字段中，键入“压缩输出”。</span><span class="sxs-lookup"><span data-stu-id="ee673-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="ee673-126">压缩输出</span><span class="sxs-lookup"><span data-stu-id="ee673-126">Zip output</span></span>  
14. <span data-ttu-id="ee673-127">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee673-127">Click OK.</span></span>
15. <span data-ttu-id="ee673-128">在树中，选择“压缩输出”。</span><span class="sxs-lookup"><span data-stu-id="ee673-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="ee673-129">将附件作为采用原始名称和扩展名的文件添加到生成的压缩文件中。</span><span class="sxs-lookup"><span data-stu-id="ee673-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="ee673-130">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ee673-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="ee673-131">在树结构中，选择“常见\文件”。</span><span class="sxs-lookup"><span data-stu-id="ee673-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="ee673-132">在“名称”字段中，键入“附加文件”。</span><span class="sxs-lookup"><span data-stu-id="ee673-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="ee673-133">附加文件</span><span class="sxs-lookup"><span data-stu-id="ee673-133">Attached file</span></span>  
19. <span data-ttu-id="ee673-134">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee673-134">Click OK.</span></span>
20. <span data-ttu-id="ee673-135">在树中，选择“压缩输出\附加文件”。</span><span class="sxs-lookup"><span data-stu-id="ee673-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="ee673-136">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ee673-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="ee673-137">在树中，选择“文本\Base64”。</span><span class="sxs-lookup"><span data-stu-id="ee673-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="ee673-138">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee673-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="ee673-139">将新格式元素映射到数据模型</span><span class="sxs-lookup"><span data-stu-id="ee673-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="ee673-140">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ee673-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="ee673-141">在树结构中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="ee673-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="ee673-142">在树中，展开“模型\发票附件”。</span><span class="sxs-lookup"><span data-stu-id="ee673-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="ee673-143">在树中，选择“压缩输出\附加文件\Base64”。</span><span class="sxs-lookup"><span data-stu-id="ee673-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="ee673-144">在树中，选择“模型\发票附件\文件内容”。</span><span class="sxs-lookup"><span data-stu-id="ee673-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="ee673-145">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="ee673-145">Click Bind.</span></span>
7. <span data-ttu-id="ee673-146">在树中，选择“压缩输出\附加文件”。</span><span class="sxs-lookup"><span data-stu-id="ee673-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="ee673-147">单击“编辑文件名”。</span><span class="sxs-lookup"><span data-stu-id="ee673-147">Click Edit filename.</span></span>
9. <span data-ttu-id="ee673-148">在树中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="ee673-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="ee673-149">在树中，展开“模型\发票附件”。</span><span class="sxs-lookup"><span data-stu-id="ee673-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="ee673-150">在树中，选择“模型\发票附件\文件名”。</span><span class="sxs-lookup"><span data-stu-id="ee673-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="ee673-151">单击“添加数据源”。</span><span class="sxs-lookup"><span data-stu-id="ee673-151">Click Add data source.</span></span>
13. <span data-ttu-id="ee673-152">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ee673-152">Click Save.</span></span>
14. <span data-ttu-id="ee673-153">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ee673-153">Close the page.</span></span>
15. <span data-ttu-id="ee673-154">在树中，选择“模型\发票附件”。</span><span class="sxs-lookup"><span data-stu-id="ee673-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="ee673-155">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="ee673-155">Click Bind.</span></span>
17. <span data-ttu-id="ee673-156">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ee673-156">Click Save.</span></span>
18. <span data-ttu-id="ee673-157">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ee673-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="ee673-158">运行为所选发票设计的报表</span><span class="sxs-lookup"><span data-stu-id="ee673-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="ee673-159">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="ee673-159">Click Run.</span></span>
2. <span data-ttu-id="ee673-160">展开“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="ee673-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="ee673-161">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="ee673-161">Click Filter.</span></span>
4. <span data-ttu-id="ee673-162">选择“客户发票日记帐”的行和“销售订单”字段。</span><span class="sxs-lookup"><span data-stu-id="ee673-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="ee673-163">在"条件"字段中，在条件的“销售订单”字段中，键入订单编号 000148。</span><span class="sxs-lookup"><span data-stu-id="ee673-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="ee673-164">000148</span><span class="sxs-lookup"><span data-stu-id="ee673-164">000148</span></span>  
6. <span data-ttu-id="ee673-165">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee673-165">Click OK.</span></span>
7. <span data-ttu-id="ee673-166">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee673-166">Click OK.</span></span>
    * <span data-ttu-id="ee673-167">检查生成的输出。</span><span class="sxs-lookup"><span data-stu-id="ee673-167">Review the generated output.</span></span> <span data-ttu-id="ee673-168">请注意，除了 XML 格式的发票，还为每个附件创建了一个文件。</span><span class="sxs-lookup"><span data-stu-id="ee673-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="ee673-169">附件文件使用二进制格式的压缩输出填充。</span><span class="sxs-lookup"><span data-stu-id="ee673-169">The attachment files are populated with the zipped output in binary format.</span></span>  


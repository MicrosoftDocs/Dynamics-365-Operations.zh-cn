--- 
title: "针对电子申报 (ER) 创建 Microsoft Office 格式的包含嵌入图像的报表（第 1 部分）"
description: "以下步骤说明“系统管理员”或“电子申报开发人员”角色的用户如何设计电子申报 (ER) 配置，以便生成包含嵌入图像的 MS office 格式（Excel 和 Word）的电子单据。"
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.openlocfilehash: bfc3d09017b864e6b2811cab9d7f4b05b048148b
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="make-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er--part-1"></a><span data-ttu-id="e8899-103">针对电子申报 (ER) 创建 Microsoft Office 格式的包含嵌入图像的报表（第 1 部分）</span><span class="sxs-lookup"><span data-stu-id="e8899-103">Make reports in Microsoft Office formats with embedded images for electronic reporting (ER)  (Part 1)</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e8899-104">以下步骤说明“系统管理员”或“电子申报开发人员”角色的用户如何设计电子申报 (ER) 配置，以便生成包含嵌入图像的 MS office 格式（Excel 和 Word）的电子单据。</span><span class="sxs-lookup"><span data-stu-id="e8899-104">The following steps explain how a user playing either ‘System administrator’ or ‘Electronic reporting developer’ role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="e8899-105">在此示例中，您将把创建的 ER 配置用于示例公司“Litware 公司”。</span><span class="sxs-lookup"><span data-stu-id="e8899-105">In this example, you will use created ER configurations for sample company, ‘Litware, Inc.’.</span></span>  <span data-ttu-id="e8899-106">若要完成这些步骤，必须首先完成“ER 创建包含嵌入图像的 MS Office 格式报表（第 2 部分：审查配置）”任务指南中的步骤。</span><span class="sxs-lookup"><span data-stu-id="e8899-106">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)” task guide.</span></span> <span data-ttu-id="e8899-107">这些步骤可以在“USMF”公司执行。</span><span class="sxs-lookup"><span data-stu-id="e8899-107">These steps can be performed in ‘USMF’ company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="e8899-108">使用初始模型映射运行格式</span><span class="sxs-lookup"><span data-stu-id="e8899-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="e8899-109">转至“现金和银行管理”>“银行帐户”>“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="e8899-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="e8899-110">使用“快速筛选器”以筛选含有 'USMF OPER' 值的“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="e8899-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="e8899-111">单击“操作窗格”上的“设置”。</span><span class="sxs-lookup"><span data-stu-id="e8899-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="e8899-112">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="e8899-112">Click Check.</span></span>
5. <span data-ttu-id="e8899-113">单击“打印测试”。</span><span class="sxs-lookup"><span data-stu-id="e8899-113">Click Print test.</span></span>
    * <span data-ttu-id="e8899-114">出于测试目的运行格式。</span><span class="sxs-lookup"><span data-stu-id="e8899-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="e8899-115">在“可转让支票格式”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="e8899-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="e8899-116">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e8899-116">Click OK.</span></span>
    * <span data-ttu-id="e8899-117">检查创建的输出。</span><span class="sxs-lookup"><span data-stu-id="e8899-117">Review the created output.</span></span> <span data-ttu-id="e8899-118">请注意，公司徽标在报表和授权人员的签名中显示。</span><span class="sxs-lookup"><span data-stu-id="e8899-118">Note that the company logo is presented in the report as well as the authorized person’s signature.</span></span> <span data-ttu-id="e8899-119">签名图像取自与所选银行帐户关联的支票布局记录的“容器”数据类型的字段。</span><span class="sxs-lookup"><span data-stu-id="e8899-119">The signature image is taken from the field of the ‘Container’ data type of the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="e8899-120">展开“份数”部分。</span><span class="sxs-lookup"><span data-stu-id="e8899-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="e8899-121">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="e8899-121">Click Edit.</span></span>
10. <span data-ttu-id="e8899-122">在“水印”字段中，输入“将水印打印为失效”。</span><span class="sxs-lookup"><span data-stu-id="e8899-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="e8899-123">更改水印布局设置以通过 Excel 形状元素在生成单据时显示水印文本。</span><span class="sxs-lookup"><span data-stu-id="e8899-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="e8899-124">单击“打印测试”。</span><span class="sxs-lookup"><span data-stu-id="e8899-124">Click Print test.</span></span>
12. <span data-ttu-id="e8899-125">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e8899-125">Click OK.</span></span>
    * <span data-ttu-id="e8899-126">检查创建的输出。</span><span class="sxs-lookup"><span data-stu-id="e8899-126">Review the created output.</span></span> <span data-ttu-id="e8899-127">请注意，水印根据选择选项在创建的报表中显示。</span><span class="sxs-lookup"><span data-stu-id="e8899-127">Note that the watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="e8899-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e8899-128">Close the page.</span></span>
14. <span data-ttu-id="e8899-129">在“操作窗格”上，单击“管理付款”。</span><span class="sxs-lookup"><span data-stu-id="e8899-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="e8899-130">单击“支票”。</span><span class="sxs-lookup"><span data-stu-id="e8899-130">Click Checks.</span></span>
16. <span data-ttu-id="e8899-131">单击“显示筛选器”。</span><span class="sxs-lookup"><span data-stu-id="e8899-131">Click Show filters.</span></span>
17. <span data-ttu-id="e8899-132">应用以下筛选器：使用“之一”筛选器运算符在“支票编号”字段中输入筛选器值“381”、“385”、“389”之一。</span><span class="sxs-lookup"><span data-stu-id="e8899-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="e8899-133">在列表中，标记所有行。</span><span class="sxs-lookup"><span data-stu-id="e8899-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="e8899-134">单击“打印支票副本”。</span><span class="sxs-lookup"><span data-stu-id="e8899-134">Click Print check copy.</span></span>
    * <span data-ttu-id="e8899-135">运行格式以重新打印所选支票。</span><span class="sxs-lookup"><span data-stu-id="e8899-135">Run the format to re-print the selected cheques.</span></span>  
    * <span data-ttu-id="e8899-136">检查创建的输出。</span><span class="sxs-lookup"><span data-stu-id="e8899-136">Review the created output.</span></span> <span data-ttu-id="e8899-137">请注意，已重新打印了所选支票。</span><span class="sxs-lookup"><span data-stu-id="e8899-137">Note that the selected cheques have been re-printed.</span></span> <span data-ttu-id="e8899-138">不打印公司徽标和标签，因为它们位于预打印表上。</span><span class="sxs-lookup"><span data-stu-id="e8899-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="e8899-139">修改所导入数据模型的映射</span><span class="sxs-lookup"><span data-stu-id="e8899-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="e8899-140">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e8899-140">Close the page.</span></span>
2. <span data-ttu-id="e8899-141">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e8899-141">Close the page.</span></span>
3. <span data-ttu-id="e8899-142">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="e8899-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="e8899-143">在树中，选择“支票的模型”。</span><span class="sxs-lookup"><span data-stu-id="e8899-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="e8899-144">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="e8899-144">Click Designer.</span></span>
6. <span data-ttu-id="e8899-145">单击“映射模型到数据源”。</span><span class="sxs-lookup"><span data-stu-id="e8899-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="e8899-146">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="e8899-146">Click Designer.</span></span>
    * <span data-ttu-id="e8899-147">我们将更改数据模型的签名项的绑定，以便从已附加到与所选银行帐户关联的支票布局记录的文件获取签名图像。</span><span class="sxs-lookup"><span data-stu-id="e8899-147">We will change the binding of the data model’s signature item to get the signature image from the file that has been attached to the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="e8899-148">关闭“显示详细信息”。</span><span class="sxs-lookup"><span data-stu-id="e8899-148">Turn Show details off.</span></span>
9. <span data-ttu-id="e8899-149">在树中，展开“布局”。</span><span class="sxs-lookup"><span data-stu-id="e8899-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="e8899-150">在树中，展开“布局\签名”。</span><span class="sxs-lookup"><span data-stu-id="e8899-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="e8899-151">在树中，选择“布局\签名\图像 = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp”。</span><span class="sxs-lookup"><span data-stu-id="e8899-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="e8899-152">在树中，展开“支票金额”。</span><span class="sxs-lookup"><span data-stu-id="e8899-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="e8899-153">在树中，展开“支票金额\<关系”。</span><span class="sxs-lookup"><span data-stu-id="e8899-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="e8899-154">在树中，展开“支票金额\<关系\银行支票布局”。</span><span class="sxs-lookup"><span data-stu-id="e8899-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="e8899-155">在树中，展开“支票金额\<关系\银行支票布局\<关系”。</span><span class="sxs-lookup"><span data-stu-id="e8899-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="e8899-156">在树中，展开“支票金额\<关系\银行支票布局\<关系\<单据”。</span><span class="sxs-lookup"><span data-stu-id="e8899-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="e8899-157">在树中，选择“支票金额\<关系\银行支票布局\<关系\<单据\getFileContentAsContainer()”。</span><span class="sxs-lookup"><span data-stu-id="e8899-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="e8899-158">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="e8899-158">Click Bind.</span></span>
19. <span data-ttu-id="e8899-159">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="e8899-159">Click Save.</span></span>
20. <span data-ttu-id="e8899-160">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e8899-160">Close the page.</span></span>
21. <span data-ttu-id="e8899-161">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e8899-161">Close the page.</span></span>
22. <span data-ttu-id="e8899-162">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e8899-162">Close the page.</span></span>
23. <span data-ttu-id="e8899-163">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e8899-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="e8899-164">使用调整后的模型映射运行格式</span><span class="sxs-lookup"><span data-stu-id="e8899-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="e8899-165">转至“现金和银行管理”>“银行帐户”>“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="e8899-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="e8899-166">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="e8899-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e8899-167">例如，在“银行帐户”字段中用一个值“USMF OPER”进行筛选。</span><span class="sxs-lookup"><span data-stu-id="e8899-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="e8899-168">单击“操作窗格”上的“设置”。</span><span class="sxs-lookup"><span data-stu-id="e8899-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="e8899-169">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="e8899-169">Click Check.</span></span>
5. <span data-ttu-id="e8899-170">单击“打印测试”。</span><span class="sxs-lookup"><span data-stu-id="e8899-170">Click Print test.</span></span>
6. <span data-ttu-id="e8899-171">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e8899-171">Click OK.</span></span>
    * <span data-ttu-id="e8899-172">检查创建的输出。</span><span class="sxs-lookup"><span data-stu-id="e8899-172">Review the created output.</span></span> <span data-ttu-id="e8899-173">请注意，来自“单据管理附件”的图像表示为授权人员的签名。</span><span class="sxs-lookup"><span data-stu-id="e8899-173">Note that the image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="e8899-174">将 MS Word 文档用作所导入格式的模板</span><span class="sxs-lookup"><span data-stu-id="e8899-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="e8899-175">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e8899-175">Close the page.</span></span>
2. <span data-ttu-id="e8899-176">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e8899-176">Close the page.</span></span>
3. <span data-ttu-id="e8899-177">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="e8899-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="e8899-178">在树中，展开“支票的模型”。</span><span class="sxs-lookup"><span data-stu-id="e8899-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="e8899-179">在树中，展开“支票的模型\支票打印格式“。</span><span class="sxs-lookup"><span data-stu-id="e8899-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="e8899-180">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="e8899-180">Click Designer.</span></span>
7. <span data-ttu-id="e8899-181">单击“附加”。</span><span class="sxs-lookup"><span data-stu-id="e8899-181">Click Attachments.</span></span>
8. <span data-ttu-id="e8899-182">单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="e8899-182">Click Delete.</span></span>
9. <span data-ttu-id="e8899-183">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="e8899-183">Click Yes.</span></span>
10. <span data-ttu-id="e8899-184">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e8899-184">Click New.</span></span>
11. <span data-ttu-id="e8899-185">单击“文件”。</span><span class="sxs-lookup"><span data-stu-id="e8899-185">Click File.</span></span>
    * <span data-ttu-id="e8899-186">单击“浏览”并选择提前下载的“支票模板 Word.docx”文件。</span><span class="sxs-lookup"><span data-stu-id="e8899-186">Click Browse and select the downloaded in advance ‘Cheque template Word.docx’ file.</span></span>  
12. <span data-ttu-id="e8899-187">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e8899-187">Close the page.</span></span>
13. <span data-ttu-id="e8899-188">在“模板”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e8899-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="e8899-189">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="e8899-189">Click Save.</span></span>
15. <span data-ttu-id="e8899-190">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e8899-190">Close the page.</span></span>
16. <span data-ttu-id="e8899-191">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="e8899-191">Click Edit.</span></span>
17. <span data-ttu-id="e8899-192">在“运行草稿”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="e8899-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="e8899-193">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e8899-193">Close the page.</span></span>
19. <span data-ttu-id="e8899-194">转至“现金和银行管理”>“银行帐户”>“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="e8899-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="e8899-195">使用“快速筛选器”以筛选含有 'USMF OPER' 值的“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="e8899-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="e8899-196">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="e8899-196">Click Check.</span></span>
22. <span data-ttu-id="e8899-197">单击“打印测试”。</span><span class="sxs-lookup"><span data-stu-id="e8899-197">Click Print test.</span></span>
23. <span data-ttu-id="e8899-198">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e8899-198">Click OK.</span></span>
    * <span data-ttu-id="e8899-199">检查创建的输出。</span><span class="sxs-lookup"><span data-stu-id="e8899-199">Review the created output.</span></span> <span data-ttu-id="e8899-200">请注意，已将输出生成为带有嵌入图像（用于显示公司徽标、授权人员的签名和所选水印文本）的 MS Word 文档。</span><span class="sxs-lookup"><span data-stu-id="e8899-200">Note that the output has been generated as a MS Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  


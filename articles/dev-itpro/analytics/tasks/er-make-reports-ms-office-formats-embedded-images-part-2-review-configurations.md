--- 
title: "针对电子申报 (ER) 检查配置以创建 Microsoft Office 格式的包含嵌入图像的报表"
description: "若要完成这些步骤，必须首先完成“ER 创建包含嵌入图像的 MS Office 格式报表（第 1 部分 - 设置参数）”任务指南中的步骤。"
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: dcc162a4c0ba81079eefb7564ab037c1287acd92
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="review-configurations-to-make-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er"></a><span data-ttu-id="bb02f-103">针对电子申报 (ER) 检查配置以创建 Microsoft Office 格式的包含嵌入图像的报表</span><span class="sxs-lookup"><span data-stu-id="bb02f-103">Review configurations to make reports in Microsoft Office formats with embedded images for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb02f-104">若要完成这些步骤，必须首先完成“ER 创建包含嵌入图像的 MS Office 格式报表（第 1 部分：设置参数）”任务指南中的步骤。</span><span class="sxs-lookup"><span data-stu-id="bb02f-104">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)” task guide.</span></span>

<span data-ttu-id="bb02f-105">此过程显示如何设计电子申报 (ER) 配置，以便在 Microsoft Excel 和 Microsoft Word 中生成包含嵌入图像的电子单据。</span><span class="sxs-lookup"><span data-stu-id="bb02f-105">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="bb02f-106">在此示例中，您将查看示例公司 Litware 公司 的 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="bb02f-106">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="bb02f-107">此过程针对向其分配了系统管理员角色或电子申报开发人员角色的用户。</span><span class="sxs-lookup"><span data-stu-id="bb02f-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="bb02f-108">可使用 USMF 数据集完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="bb02f-108">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="bb02f-109">查看导入的数据模型</span><span class="sxs-lookup"><span data-stu-id="bb02f-109">Review the imported data model</span></span>
1. <span data-ttu-id="bb02f-110">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="bb02f-111">在树中，选择“支票的模型”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-111">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="bb02f-112">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-112">Click Designer.</span></span>
    * <span data-ttu-id="bb02f-113">此模型设计为从业务角度表示付款支票和将此模型映射到应用程序的数据源。</span><span class="sxs-lookup"><span data-stu-id="bb02f-113">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application’s data sources.</span></span> <span data-ttu-id="bb02f-114">按 ER Operations 设计器检查此模型。</span><span class="sxs-lookup"><span data-stu-id="bb02f-114">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="bb02f-115">注意显示的模型元素属性：结构、名称、描述、数据类型等。</span><span class="sxs-lookup"><span data-stu-id="bb02f-115">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="bb02f-116">在树中，展开“根”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-116">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="bb02f-117">在树中，选择“根\支票”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-117">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="bb02f-118">在树中，展开“根\支票”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-118">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="bb02f-119">在树中，展开“根\支票\属性”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-119">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="bb02f-120">在树中，展开“根\付款人”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-120">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="bb02f-121">在树中，选择“根\istestrun“.</span><span class="sxs-lookup"><span data-stu-id="bb02f-121">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="bb02f-122">在树中，选择”根\布局“。</span><span class="sxs-lookup"><span data-stu-id="bb02f-122">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="bb02f-123">此模型的布局元素表示所选银行帐户的打印支票表布局的详细信息。</span><span class="sxs-lookup"><span data-stu-id="bb02f-123">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="bb02f-124">还包括“容器”数据类型的两个节点，用于存储图像。</span><span class="sxs-lookup"><span data-stu-id="bb02f-124">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="bb02f-125">在树中，展开”根\布局“。</span><span class="sxs-lookup"><span data-stu-id="bb02f-125">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="bb02f-126">在树中，选择”根\布局\公司徽标“。</span><span class="sxs-lookup"><span data-stu-id="bb02f-126">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="bb02f-127">在树中，展开”根\布局\公司徽标“。</span><span class="sxs-lookup"><span data-stu-id="bb02f-127">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="bb02f-128">在树中，选择”根\布局\公司徽标\图像“。</span><span class="sxs-lookup"><span data-stu-id="bb02f-128">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="bb02f-129">在树中，选择”根\布局\公司徽标\isprinted“。</span><span class="sxs-lookup"><span data-stu-id="bb02f-129">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="bb02f-130">在树中，选择”根\布局\签名“。</span><span class="sxs-lookup"><span data-stu-id="bb02f-130">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="bb02f-131">在树中，展开“根\布局\签名”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-131">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="bb02f-132">在树中，选择”根\布局\签名\图像“。</span><span class="sxs-lookup"><span data-stu-id="bb02f-132">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="bb02f-133">在树中，选择”根\布局\签名\isprinted“。</span><span class="sxs-lookup"><span data-stu-id="bb02f-133">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="bb02f-134">请注意，已将两个图像数据模型元素绑定到其中包含二进制格式的公司徽标图像和授权人员签名图像的表的字段。</span><span class="sxs-lookup"><span data-stu-id="bb02f-134">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person’s signature in binary format.</span></span>  
20. <span data-ttu-id="bb02f-135">在树中，展开“根\布局\水印”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-135">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="bb02f-136">单击“映射模型到数据源”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-136">Click Map model to datasource.</span></span>
22. <span data-ttu-id="bb02f-137">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-137">Click Designer.</span></span>
23. <span data-ttu-id="bb02f-138">在树中，展开“chequesselected”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-138">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="bb02f-139">在树中，展开“布局”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-139">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="bb02f-140">在树中，展开”布局\公司徽标“。</span><span class="sxs-lookup"><span data-stu-id="bb02f-140">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="bb02f-141">在树中，展开“布局\签名”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-141">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="bb02f-142">在树中，展开“布局\水印”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-142">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="bb02f-143">打开”显示详细信息“。</span><span class="sxs-lookup"><span data-stu-id="bb02f-143">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="bb02f-144">请注意，已将支票数据模型元素绑定到 TmpChequePrintout 表，该表在运行时将包含用户已收集来打印的支票的记录。</span><span class="sxs-lookup"><span data-stu-id="bb02f-144">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="bb02f-145">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="bb02f-145">Close the page.</span></span>
30. <span data-ttu-id="bb02f-146">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="bb02f-146">Close the page.</span></span>
31. <span data-ttu-id="bb02f-147">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="bb02f-147">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="bb02f-148">查看导入的格式</span><span class="sxs-lookup"><span data-stu-id="bb02f-148">Review the imported format</span></span>
1. <span data-ttu-id="bb02f-149">在树中，展开“支票的模型”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-149">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="bb02f-150">在树中，展开“支票的模型\支票打印格式“。</span><span class="sxs-lookup"><span data-stu-id="bb02f-150">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="bb02f-151">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-151">Click Designer.</span></span>
4. <span data-ttu-id="bb02f-152">单击“附加”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-152">Click Attachments.</span></span>
5. <span data-ttu-id="bb02f-153">单击“打开”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-153">Click Open.</span></span>
    * <span data-ttu-id="bb02f-154">在 Excel 中打开附加报表的模板。</span><span class="sxs-lookup"><span data-stu-id="bb02f-154">Open the attached report’s template in Excel.</span></span>  
    * <span data-ttu-id="bb02f-155">查看附加的报表的将用于打印支票的 Excel 模板。</span><span class="sxs-lookup"><span data-stu-id="bb02f-155">Review the attached report’s Excel template that will be used to print cheques.</span></span> <span data-ttu-id="bb02f-156">此模板中每页包含两张支票，并设计为将支票打印到预打印的表。</span><span class="sxs-lookup"><span data-stu-id="bb02f-156">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="bb02f-157">请注意嵌入了两个空白图像。</span><span class="sxs-lookup"><span data-stu-id="bb02f-157">Note that two blank images are embedded.</span></span> <span data-ttu-id="bb02f-158">这些空白图像用于公司徽标和为付款授权的人员的签名。</span><span class="sxs-lookup"><span data-stu-id="bb02f-158">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="bb02f-159">在 Excel 中分别验证名称为 CompLogo 和 SignatureImage 的图像。</span><span class="sxs-lookup"><span data-stu-id="bb02f-159">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="bb02f-160">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="bb02f-160">Close the page.</span></span>
7. <span data-ttu-id="bb02f-161">在树中，展开“报表”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-161">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="bb02f-162">在树中，展开“报表\ChequeLines”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-162">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="bb02f-163">在树中，选择”报表\ChequeLines\CompLogo“。</span><span class="sxs-lookup"><span data-stu-id="bb02f-163">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="bb02f-164">打开”显示详细信息“。</span><span class="sxs-lookup"><span data-stu-id="bb02f-164">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="bb02f-165">请注意，“CompLogo”格式的单元格元素表示用于在报表中填充公司徽标图像的 Excel 项。</span><span class="sxs-lookup"><span data-stu-id="bb02f-165">Note that the ‘CompLogo’ format’s cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="bb02f-166">此格式元素绑定到在运行时包含二进制格式的公司徽标图像的图像数据模型元素。</span><span class="sxs-lookup"><span data-stu-id="bb02f-166">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="bb02f-167">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="bb02f-167">Click the Mapping tab.</span></span>
12. <span data-ttu-id="bb02f-168">单击“已启用编辑”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-168">Click Edit enabled.</span></span>
    * <span data-ttu-id="bb02f-169">请注意，可以创建“CompLogo”格式的单元格元素，以便不再启用该格式。</span><span class="sxs-lookup"><span data-stu-id="bb02f-169">Note that you can make the ‘CompLogo’ format’s cell element so that it’s no longer enabled.</span></span> <span data-ttu-id="bb02f-170">在此示例中，关联的 Excel 图像元素将隐藏所生成报表中的公司徽标。</span><span class="sxs-lookup"><span data-stu-id="bb02f-170">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="bb02f-171">如果启用的表达式返回 TRUE，并且定义的绑定不提供图像，关联的 Excel 图像元素将显示已在 Excel 模板中保存的图像。</span><span class="sxs-lookup"><span data-stu-id="bb02f-171">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="bb02f-172">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="bb02f-172">Close the page.</span></span>
14. <span data-ttu-id="bb02f-173">在树中，展开“标签: 容器”。</span><span class="sxs-lookup"><span data-stu-id="bb02f-173">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="bb02f-174">出于测试目的创建报表时，其中将包含预打印支票表中的一些标签。</span><span class="sxs-lookup"><span data-stu-id="bb02f-174">Some labels that are presented in the preprinted cheque form will be included in the report when it’s created for testing purposes.</span></span> <span data-ttu-id="bb02f-175">但是实际打印时将不打印这些标签，因为预打印的表已包含这些标签。</span><span class="sxs-lookup"><span data-stu-id="bb02f-175">However, those labels won’t be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="bb02f-176">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="bb02f-176">Close the page.</span></span>


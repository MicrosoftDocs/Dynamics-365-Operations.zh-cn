---
title: 设计配置以生成 Office 格式的包含嵌入图像的报表
description: 本主题介绍如何设计生成包含嵌入图像的 Excel 和 Word 格式的电子文档的配置。
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eea178a351716425706f481ae66c5b5183a52e5
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944549"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="c32ac-103">设计配置以生成 Office 格式的包含嵌入图像的报表</span><span class="sxs-lookup"><span data-stu-id="c32ac-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c32ac-104">为了完成此过程中的步骤，首先完成“ER 创建配置提供商并标记为有效”这一过程。</span><span class="sxs-lookup"><span data-stu-id="c32ac-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="c32ac-105">此过程介绍如何设计电子申报 (ER) 配置，以便生成包含嵌入图像的 Microsoft Excel 或 Word 文档。</span><span class="sxs-lookup"><span data-stu-id="c32ac-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="c32ac-106">在此过程中，将为示例公司 Litware, Inc. 创建所需 ER 配置。可使用 USMF 数据集完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="c32ac-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="c32ac-107">此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。</span><span class="sxs-lookup"><span data-stu-id="c32ac-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="c32ac-108">在开始之前，请下载并保存以下文件：</span><span class="sxs-lookup"><span data-stu-id="c32ac-108">Before you begin, download and save the following files:</span></span> 

| <span data-ttu-id="c32ac-109">说明</span><span class="sxs-lookup"><span data-stu-id="c32ac-109">Description</span></span>                                          | <span data-ttu-id="c32ac-110">文件名</span><span class="sxs-lookup"><span data-stu-id="c32ac-110">File name</span></span>                   |
|------------------------------------------------------|-----------------------------|
| <span data-ttu-id="c32ac-111">ER 数据模型配置</span><span class="sxs-lookup"><span data-stu-id="c32ac-111">ER data model configuration</span></span>                          | [<span data-ttu-id="c32ac-112">Model for cheques.xml</span><span class="sxs-lookup"><span data-stu-id="c32ac-112">Model for cheques.xml</span></span>](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| <span data-ttu-id="c32ac-113">ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="c32ac-113">ER format configuration</span></span>                              | [<span data-ttu-id="c32ac-114">Cheques printing format.xml</span><span class="sxs-lookup"><span data-stu-id="c32ac-114">Cheques printing format.xml</span></span>](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| <span data-ttu-id="c32ac-115">公司徽标图像</span><span class="sxs-lookup"><span data-stu-id="c32ac-115">Company logo image</span></span>                                   | [<span data-ttu-id="c32ac-116">Company logo.png</span><span class="sxs-lookup"><span data-stu-id="c32ac-116">Company logo.png</span></span>](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| <span data-ttu-id="c32ac-117">签名图像</span><span class="sxs-lookup"><span data-stu-id="c32ac-117">Signature image</span></span>                                      | [<span data-ttu-id="c32ac-118">Signature image.png</span><span class="sxs-lookup"><span data-stu-id="c32ac-118">Signature image.png</span></span>](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| <span data-ttu-id="c32ac-119">替代签名图像</span><span class="sxs-lookup"><span data-stu-id="c32ac-119">Alternative signature image</span></span>                          | [<span data-ttu-id="c32ac-120">Signature image 2.png</span><span class="sxs-lookup"><span data-stu-id="c32ac-120">Signature image 2.png</span></span>](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| <span data-ttu-id="c32ac-121">用于打印付款支票的 Microsoft Word 模板</span><span class="sxs-lookup"><span data-stu-id="c32ac-121">Microsoft Word template for printing payment checks</span></span>  | [<span data-ttu-id="c32ac-122">Cheque template Word.docx</span><span class="sxs-lookup"><span data-stu-id="c32ac-122">Cheque template Word.docx</span></span>](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a><span data-ttu-id="c32ac-123">验证先决条件</span><span class="sxs-lookup"><span data-stu-id="c32ac-123">Verify prerequisites</span></span>  
 1. <span data-ttu-id="c32ac-124">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-124">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="c32ac-125">确保示例公司 Litware 公司的配置提供程序可用且标记为“有效”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-125">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="c32ac-126">如果没有看到此配置提供程序，请首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="c32ac-126">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="c32ac-127">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-127">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="c32ac-128">添加新 ER 模型配置</span><span class="sxs-lookup"><span data-stu-id="c32ac-128">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="c32ac-129">不是创建新模型，您可以加载之前保存的 ER 模型配置文件 (Model for cheques.xml)。</span><span class="sxs-lookup"><span data-stu-id="c32ac-129">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="c32ac-130">此文件包含付款支票的示例数据模型和数据模型到 Dynamics 365 for Operations 应用程序的数据组件的映射。</span><span class="sxs-lookup"><span data-stu-id="c32ac-130">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="c32ac-131">在“版本”快速选项卡上，单击“交换”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-131">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="c32ac-132">单击“从 XML 文件加载”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-132">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="c32ac-133">单击“浏览”，然后选择 Model for cheques.xml。</span><span class="sxs-lookup"><span data-stu-id="c32ac-133">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="c32ac-134">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-134">Click OK.</span></span>  
 6. <span data-ttu-id="c32ac-135">加载的模块将用作生成在 Excel 和 Word 中包含图像的文档的信息数据源。</span><span class="sxs-lookup"><span data-stu-id="c32ac-135">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="c32ac-136">添加新 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="c32ac-136">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="c32ac-137">不是创建新格式，您可以加载之前保存的 ER 格式配置文件 (Cheques printing format.xml)。</span><span class="sxs-lookup"><span data-stu-id="c32ac-137">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="c32ac-138">此文件包含使用预打印表打印支票的格式的示例布局以及此格式到“支票模型”数据模型的映射。</span><span class="sxs-lookup"><span data-stu-id="c32ac-138">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="c32ac-139">单击“交换”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-139">Click Exchange.</span></span>  
 3. <span data-ttu-id="c32ac-140">单击“从 XML 文件加载”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-140">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="c32ac-141">单击“浏览”并选择 Cheques printing format.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="c32ac-141">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="c32ac-142">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-142">Click OK.</span></span>  
 6. <span data-ttu-id="c32ac-143">在树中，展开“支票的模型”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-143">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="c32ac-144">在树中，展开“支票的模型\支票打印格式“。</span><span class="sxs-lookup"><span data-stu-id="c32ac-144">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="c32ac-145">加载的格式将用于生成在 Excel 和 Word 中包含图像的文档。</span><span class="sxs-lookup"><span data-stu-id="c32ac-145">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="c32ac-146">配置 ER 用户参数</span><span class="sxs-lookup"><span data-stu-id="c32ac-146">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="c32ac-147">在操作窗格上，单击“配置”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-147">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="c32ac-148">单击“用户参数”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-148">Click User parameters.</span></span>  
 3. <span data-ttu-id="c32ac-149">在“运行设置”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-149">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="c32ac-150">打开“运行草稿”标志以启动所选格式的草稿版（而不是已完成格式）。</span><span class="sxs-lookup"><span data-stu-id="c32ac-150">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="c32ac-151">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-151">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="c32ac-152">配置现金和银行管理参数</span><span class="sxs-lookup"><span data-stu-id="c32ac-152">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="c32ac-153">转至“现金和银行管理”>“银行帐户”>“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-153">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="c32ac-154">使用“快速筛选器”以筛选含有 'USMF OPER' 值的“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-154">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="c32ac-155">单击“操作窗格”上的“设置”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-155">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="c32ac-156">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-156">Click Check.</span></span>  
 5. <span data-ttu-id="c32ac-157">展开“设置”部分。</span><span class="sxs-lookup"><span data-stu-id="c32ac-157">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="c32ac-158">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-158">Click Edit.</span></span>  
 7. <span data-ttu-id="c32ac-159">在“公司徽标”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-159">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="c32ac-160">单击“公司徽标”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-160">Click Company logo.</span></span>  
 9. <span data-ttu-id="c32ac-161">单击“更改”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-161">Click Change.</span></span>  
 10. <span data-ttu-id="c32ac-162">单击“浏览”并选择您之前下载的文件 Company logo.png。</span><span class="sxs-lookup"><span data-stu-id="c32ac-162">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="c32ac-163">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-163">Click Save.</span></span>  
 12. <span data-ttu-id="c32ac-164">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c32ac-164">Close the page.</span></span>  
 13. <span data-ttu-id="c32ac-165">展开“签名”部分。</span><span class="sxs-lookup"><span data-stu-id="c32ac-165">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="c32ac-166">在“打印第一个签名”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-166">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="c32ac-167">单击“更改”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-167">Click Change.</span></span>  
 16. <span data-ttu-id="c32ac-168">单击“浏览”并选择您之前下载的文件 Signature image.png。</span><span class="sxs-lookup"><span data-stu-id="c32ac-168">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="c32ac-169">展开“份数”部分。</span><span class="sxs-lookup"><span data-stu-id="c32ac-169">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="c32ac-170">在“水印”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="c32ac-170">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="c32ac-171">在“普通电子导出格式”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-171">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="c32ac-172">选择“支票打印格式”配置。</span><span class="sxs-lookup"><span data-stu-id="c32ac-172">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="c32ac-173">现在所选的 ER 格式将用于打印支票。</span><span class="sxs-lookup"><span data-stu-id="c32ac-173">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="c32ac-174">单击“附加”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-174">Click Attach.</span></span>  
 23. <span data-ttu-id="c32ac-175">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-175">Click New.</span></span>  
 24. <span data-ttu-id="c32ac-176">单击“文件”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-176">Click File.</span></span>  
 25. <span data-ttu-id="c32ac-177">单击“浏览”并选择您之前下载的文件 Signature image 2.png。</span><span class="sxs-lookup"><span data-stu-id="c32ac-177">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="c32ac-178">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c32ac-178">Close the page.</span></span>  
 27. <span data-ttu-id="c32ac-179">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c32ac-179">Close the page.</span></span>  
 28. <span data-ttu-id="c32ac-180">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c32ac-180">Close the page.</span></span>  
 29. <span data-ttu-id="c32ac-181">转到“现金和银行管理”>“设置”>“现金和管理银行参数”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-181">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="c32ac-182">在“允许在无效银行帐户上进行预验证创建:”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-182">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="c32ac-183">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="c32ac-183">Click Save.</span></span>  
 32. <span data-ttu-id="c32ac-184">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c32ac-184">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

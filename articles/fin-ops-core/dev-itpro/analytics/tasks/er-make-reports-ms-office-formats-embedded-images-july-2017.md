---
title: 设计配置以生成 Office 格式的包含嵌入图像的报表
description: 本主题中的步骤提供有关如何设计电子申报 (ER) 配置，以便生成 Microsoft Office 格式（Excel 和 Word）且包含嵌入图像的电子单据的信息。
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 143782413359d87f3d4c46940f9a699fbf0e8f90
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769801"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="03486-103">设计配置以生成 Office 格式的包含嵌入图像的报表</span><span class="sxs-lookup"><span data-stu-id="03486-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="03486-104">为了完成此过程中的步骤，首先完成“ER 创建配置提供商并标记为有效”这一过程。</span><span class="sxs-lookup"><span data-stu-id="03486-104">To complete the steps in this procedure, first complete the procedure, “ER Create a configuration provider and mark it as active.”</span></span> <span data-ttu-id="03486-105">此过程介绍如何设计电子申报 (ER) 配置，以便生成包含嵌入图像的 Microsoft Excel 或 Word 文档。</span><span class="sxs-lookup"><span data-stu-id="03486-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="03486-106">在此过程中，将为示例公司 Litware, Inc. 创建所需 ER 配置。可使用 USMF 数据集完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="03486-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="03486-107">此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。</span><span class="sxs-lookup"><span data-stu-id="03486-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="03486-108">首先，下载并保存“帮助”主题[使用 ER 在您生成的文档中嵌入图像和形状](../electronic-reporting-embed-images-shapes.md)中列举的文件。</span><span class="sxs-lookup"><span data-stu-id="03486-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in documents that you generate by using ER](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="03486-109">这些文件是：Model for cheques.xml、Cheques printing format.xml、Company logo.png、Signature image.png、Signature image 2.png 和 Cheque template Word.docx。</span><span class="sxs-lookup"><span data-stu-id="03486-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="03486-110">验证先决条件</span><span class="sxs-lookup"><span data-stu-id="03486-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="03486-111">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="03486-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="03486-112">确保示例公司 Litware 公司的配置提供程序可用且标记为“有效”。</span><span class="sxs-lookup"><span data-stu-id="03486-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="03486-113">如果没有看到此配置提供程序，请首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="03486-113">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>   
 3. <span data-ttu-id="03486-114">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="03486-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="03486-115">添加新 ER 模型配置</span><span class="sxs-lookup"><span data-stu-id="03486-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="03486-116">不是创建新模型，您可以加载之前保存的 ER 模型配置文件 (Model for cheques.xml)。</span><span class="sxs-lookup"><span data-stu-id="03486-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="03486-117">此文件包含付款支票的示例数据模型和数据模型到 Dynamics 365 for Operations 应用程序的数据组件的映射。</span><span class="sxs-lookup"><span data-stu-id="03486-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="03486-118">在“版本”快速选项卡上，单击“交换”。</span><span class="sxs-lookup"><span data-stu-id="03486-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="03486-119">单击“从 XML 文件加载”。</span><span class="sxs-lookup"><span data-stu-id="03486-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="03486-120">单击“浏览”，然后选择 Model for cheques.xml。</span><span class="sxs-lookup"><span data-stu-id="03486-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="03486-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="03486-121">Click OK.</span></span>  
 6. <span data-ttu-id="03486-122">加载的模块将用作生成在 Excel 和 Word 中包含图像的文档的信息数据源。</span><span class="sxs-lookup"><span data-stu-id="03486-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="03486-123">添加新 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="03486-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="03486-124">不是创建新格式，您可以加载之前保存的 ER 格式配置文件 (Cheques printing format.xml)。</span><span class="sxs-lookup"><span data-stu-id="03486-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="03486-125">此文件包含使用预打印表打印支票的格式的示例布局以及此格式到“支票模型”数据模型的映射。</span><span class="sxs-lookup"><span data-stu-id="03486-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the ‘Model for cheques’ data model.</span></span>   
 2. <span data-ttu-id="03486-126">单击“交换”。</span><span class="sxs-lookup"><span data-stu-id="03486-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="03486-127">单击“从 XML 文件加载”。</span><span class="sxs-lookup"><span data-stu-id="03486-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="03486-128">单击“浏览”并选择 Cheques printing format.xml 文件。</span><span class="sxs-lookup"><span data-stu-id="03486-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="03486-129">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="03486-129">Click OK.</span></span>  
 6. <span data-ttu-id="03486-130">在树中，展开“支票的模型”。</span><span class="sxs-lookup"><span data-stu-id="03486-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="03486-131">在树中，展开“支票的模型\支票打印格式“。</span><span class="sxs-lookup"><span data-stu-id="03486-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="03486-132">加载的格式将用于生成在 Excel 和 Word 中包含图像的文档。</span><span class="sxs-lookup"><span data-stu-id="03486-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="03486-133">配置 ER 用户参数</span><span class="sxs-lookup"><span data-stu-id="03486-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="03486-134">在操作窗格上，单击“配置”。</span><span class="sxs-lookup"><span data-stu-id="03486-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="03486-135">单击“用户参数”。</span><span class="sxs-lookup"><span data-stu-id="03486-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="03486-136">在“运行设置”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="03486-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="03486-137">打开“运行草稿”标志以启动所选格式的草稿版（而不是已完成格式）。</span><span class="sxs-lookup"><span data-stu-id="03486-137">Turn on the ‘Run draft’ flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="03486-138">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="03486-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="03486-139">配置现金和银行管理参数</span><span class="sxs-lookup"><span data-stu-id="03486-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="03486-140">转至“现金和银行管理”>“银行帐户”>“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="03486-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="03486-141">使用“快速筛选器”以筛选含有 'USMF OPER' 值的“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="03486-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="03486-142">单击“操作窗格”上的“设置”。</span><span class="sxs-lookup"><span data-stu-id="03486-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="03486-143">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="03486-143">Click Check.</span></span>  
 5. <span data-ttu-id="03486-144">展开“设置”部分。</span><span class="sxs-lookup"><span data-stu-id="03486-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="03486-145">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="03486-145">Click Edit.</span></span>  
 7. <span data-ttu-id="03486-146">在“公司徽标”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="03486-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="03486-147">单击“公司徽标”。</span><span class="sxs-lookup"><span data-stu-id="03486-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="03486-148">单击“更改”。</span><span class="sxs-lookup"><span data-stu-id="03486-148">Click Change.</span></span>  
 10. <span data-ttu-id="03486-149">单击“浏览”并选择您之前下载的文件 Company logo.png。</span><span class="sxs-lookup"><span data-stu-id="03486-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="03486-150">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="03486-150">Click Save.</span></span>  
 12. <span data-ttu-id="03486-151">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="03486-151">Close the page.</span></span>  
 13. <span data-ttu-id="03486-152">展开“签名”部分。</span><span class="sxs-lookup"><span data-stu-id="03486-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="03486-153">在“打印第一个签名”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="03486-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="03486-154">单击“更改”。</span><span class="sxs-lookup"><span data-stu-id="03486-154">Click Change.</span></span>  
 16. <span data-ttu-id="03486-155">单击“浏览”并选择您之前下载的文件 Signature image.png。</span><span class="sxs-lookup"><span data-stu-id="03486-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="03486-156">展开“份数”部分。</span><span class="sxs-lookup"><span data-stu-id="03486-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="03486-157">在“水印”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="03486-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="03486-158">在“普通电子导出格式”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="03486-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="03486-159">选择“支票打印格式”配置。</span><span class="sxs-lookup"><span data-stu-id="03486-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="03486-160">现在所选的 ER 格式将用于打印支票。</span><span class="sxs-lookup"><span data-stu-id="03486-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="03486-161">单击“附加”。</span><span class="sxs-lookup"><span data-stu-id="03486-161">Click Attach.</span></span>  
 23. <span data-ttu-id="03486-162">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="03486-162">Click New.</span></span>  
 24. <span data-ttu-id="03486-163">单击“文件”。</span><span class="sxs-lookup"><span data-stu-id="03486-163">Click File.</span></span>  
 25. <span data-ttu-id="03486-164">单击“浏览”并选择您之前下载的文件 Signature image 2.png。</span><span class="sxs-lookup"><span data-stu-id="03486-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="03486-165">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="03486-165">Close the page.</span></span>  
 27. <span data-ttu-id="03486-166">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="03486-166">Close the page.</span></span>  
 28. <span data-ttu-id="03486-167">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="03486-167">Close the page.</span></span>  
 29. <span data-ttu-id="03486-168">转到“现金和银行管理”>“设置”>“现金和管理银行参数”。</span><span class="sxs-lookup"><span data-stu-id="03486-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="03486-169">在“允许在无效银行帐户上进行预验证创建:”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="03486-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="03486-170">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="03486-170">Click Save.</span></span>  
 32. <span data-ttu-id="03486-171">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="03486-171">Close the page.</span></span>  

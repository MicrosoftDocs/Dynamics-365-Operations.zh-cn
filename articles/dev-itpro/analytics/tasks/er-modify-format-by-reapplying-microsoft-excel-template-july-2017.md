---
title: 通过重新应用 Excel 模板修改格式
description: 为了完成此过程中的步骤，您首先必须完成“ER - 设计用于以 OPENXML 格式生成报表的配置”这一过程中的步骤。
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.openlocfilehash: 3d5752caba9327475bb28c7bc6b0ee7e072f44f3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551153"
---
# <a name="modify-formats-by-reapplying-excel-templates"></a><span data-ttu-id="f55f7-103">通过重新应用 Excel 模板修改格式</span><span class="sxs-lookup"><span data-stu-id="f55f7-103">Modify formats by reapplying Excel templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f55f7-104">为了完成此过程中的步骤，您首先必须完成“ER - 设计用于以 OPENXML 格式生成报表的配置”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="f55f7-104">To complete the steps in this procedure, you must first complete the procedure, ER - Design a configuration for generating reports in OPENXML format.</span></span>

<span data-ttu-id="f55f7-105">此过程介绍如何通过重新应用已修改的 Microsoft Excel 模板，修改电子申报 (ER) 格式配置。</span><span class="sxs-lookup"><span data-stu-id="f55f7-105">This procedure explains how to modify an Electronic reporting (ER) format configuration by reapplying a Microsoft Excel template that has been modified.</span></span> <span data-ttu-id="f55f7-106">在此过程中，将把一个修改后的 Excel 模板导入已为示例公司 Litware 公司创建的 ER 格式配置，然后生成电子单据。</span><span class="sxs-lookup"><span data-stu-id="f55f7-106">In this procedure, you will import a modified Excel template into ER format configurations that have been created for the sample company, Litware, Inc., and then generate electronic documents.</span></span> <span data-ttu-id="f55f7-107">此过程针对具有系统管理员角色或电子申报开发人员角色的用户。</span><span class="sxs-lookup"><span data-stu-id="f55f7-107">This procedure is intended for users who have the system administrator or electronic reporting developer role.</span></span> <span data-ttu-id="f55f7-108">可通过使用 GBSI 数据集完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="f55f7-108">These steps can be completed by using the GBSI dataset.</span></span> <span data-ttu-id="f55f7-109">在您开始之前，请下载并保存“通过重新应用 Excel 模板修改电子申报格式”(modify-electronic-reporting-format-reapply-excel-template/) 这一帮助主题中列出的文件 SampleVendPaymWsReport2.xlsx。</span><span class="sxs-lookup"><span data-stu-id="f55f7-109">Before you begin, download and save the file, SampleVendPaymWsReport2.xlsx, which is listed in the Help topic, Modify Electronic reporting format by reapplying an Excel template (modify-electronic-reporting-format-reapply-excel-template/).</span></span>

1. <span data-ttu-id="f55f7-110">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="f55f7-111">确保示例公司 Litware 公司的配置提供程序可用且标记为“有效”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="f55f7-112">如果没有看到此配置提供程序，请首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="f55f7-112">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  

## <a name="select-the-er-format"></a><span data-ttu-id="f55f7-113">选择 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="f55f7-113">Select the ER format</span></span>
1. <span data-ttu-id="f55f7-114">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-114">Click Reporting configurations.</span></span>
2. <span data-ttu-id="f55f7-115">在树结构中，展开“付款模型”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-115">In the tree, expand 'Payment model'.</span></span>
3. <span data-ttu-id="f55f7-116">在树结构中，选择“付款模型\示例工作表报表”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-116">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
4. <span data-ttu-id="f55f7-117">单击“附加”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-117">Click Attachments.</span></span>
    * <span data-ttu-id="f55f7-118">请注意，SampleVendPaymWsReport.xlsx Excel 文件当前用作处理付款日记帐的模板。</span><span class="sxs-lookup"><span data-stu-id="f55f7-118">Note that the SampleVendPaymWsReport.xlsx Excel file is currently used as a template for payment journal processing.</span></span>   
5. <span data-ttu-id="f55f7-119">单击“打开”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-119">Click Open.</span></span>
    * <span data-ttu-id="f55f7-120">单击“打开”以浏览 Excel 模板的布局。</span><span class="sxs-lookup"><span data-stu-id="f55f7-120">Click Open to explore the layout of the Excel template.</span></span>  
    * <span data-ttu-id="f55f7-121">查看模板。</span><span class="sxs-lookup"><span data-stu-id="f55f7-121">Review the template.</span></span> <span data-ttu-id="f55f7-122">请注意，其中现在包含各付款行的以下详细信息：供应商帐号、供应商名称、银行、银行代号、帐号、借方、贷方和币种。</span><span class="sxs-lookup"><span data-stu-id="f55f7-122">Note that it currently includes the following details for each payment line: vendor account number, vendor name, bank, routing number, account number, debit, credit, and currency.</span></span> <span data-ttu-id="f55f7-123">在此示例中，我们将通过添加有关付款日期的详细信息扩展此列表。</span><span class="sxs-lookup"><span data-stu-id="f55f7-123">For this example, we want to extend this list by adding details about the payment date.</span></span>   
6. <span data-ttu-id="f55f7-124">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f55f7-124">Close the page.</span></span>

## <a name="reapply-a-new-excel-template-to-er-format"></a><span data-ttu-id="f55f7-125">对 ER 格式重新应用新 Excel 模板。</span><span class="sxs-lookup"><span data-stu-id="f55f7-125">Reapply a new Excel template to ER format</span></span>
1. <span data-ttu-id="f55f7-126">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-126">Click Designer.</span></span>
    * <span data-ttu-id="f55f7-127">打开所选 ER 格式的草稿版本以进行编辑。</span><span class="sxs-lookup"><span data-stu-id="f55f7-127">Open the draft version of the selected ER format for editing.</span></span>  
2. <span data-ttu-id="f55f7-128">在“操作”窗格上，单击“导入”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-128">On the Action Pane, click Import.</span></span>
3. <span data-ttu-id="f55f7-129">单击“Excel 的更新”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-129">Click Update from Excel.</span></span>
    * <span data-ttu-id="f55f7-130">单击“更新模板”，然后选择文件 SampleVendPaymWsReport2.xlsx。</span><span class="sxs-lookup"><span data-stu-id="f55f7-130">Click ‘Update template’, and then select the file, SampleVendPaymWsReport2.xlsx.</span></span>  
    * <span data-ttu-id="f55f7-131">单击“更新模板”并浏览以获取前面下载的 SampleVendPaymWsReport2.xlsx 文件。</span><span class="sxs-lookup"><span data-stu-id="f55f7-131">Click Update template and browse to get the downloaded earlier SampleVendPaymWsReport2.xlsx file.</span></span>  
4. <span data-ttu-id="f55f7-132">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-132">Click OK.</span></span>
    * <span data-ttu-id="f55f7-133">将应用模板 SampleVendPaymWsReport2.xlsx。</span><span class="sxs-lookup"><span data-stu-id="f55f7-133">The SampleVendPaymWsReport2.xlsx template is applied.</span></span> <span data-ttu-id="f55f7-134">将把 ER 格式的结构与模板内容同步，并将后者的元素添加到该 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="f55f7-134">The structure of the ER format is synchronized with the content of the template, whose elements are added to the ER format.</span></span> <span data-ttu-id="f55f7-135">将从格式定义中删除模板中不包含，但在 ER 格式中存在的所有现有元素。</span><span class="sxs-lookup"><span data-stu-id="f55f7-135">Any existing elements in the ER format that aren’t included in the template are removed from the format definition.</span></span>  
5. <span data-ttu-id="f55f7-136">在树中，选择“Excel”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-136">In the tree, select 'Excel'.</span></span>
    * <span data-ttu-id="f55f7-137">请注意，“模板”字段中现在包含对新模板的引用。</span><span class="sxs-lookup"><span data-stu-id="f55f7-137">Note that the Template field now contains a reference to the new template.</span></span>   
6. <span data-ttu-id="f55f7-138">单击“附加”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-138">Click Attachments.</span></span>
7. <span data-ttu-id="f55f7-139">单击“打开”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-139">Click Open.</span></span>
    * <span data-ttu-id="f55f7-140">单击“打开”以浏览修改后的 Excel 模板的布局。</span><span class="sxs-lookup"><span data-stu-id="f55f7-140">Click Open to explore the layout of the modified Excel template.</span></span>  
    * <span data-ttu-id="f55f7-141">查看模板。</span><span class="sxs-lookup"><span data-stu-id="f55f7-141">Review the template.</span></span> <span data-ttu-id="f55f7-142">请注意，其中现在包含付款日期行。</span><span class="sxs-lookup"><span data-stu-id="f55f7-142">Note that it now contains a line for the payment date.</span></span>   
8. <span data-ttu-id="f55f7-143">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f55f7-143">Close the page.</span></span>
9. <span data-ttu-id="f55f7-144">在树中，展开“Excel”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-144">In the tree, expand 'Excel'.</span></span>
10. <span data-ttu-id="f55f7-145">在树结构中，展开或折叠“Excel\付款方式行”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-145">In the tree, expand 'Excel\PaymLines'.</span></span>
11. <span data-ttu-id="f55f7-146">在树中，选择从“Excel\付款方式行\付款日期”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-146">In the tree, select 'Excel\PaymLines\PaymDate'.</span></span>
    * <span data-ttu-id="f55f7-147">请注意，ER 格式中现在包含多项。</span><span class="sxs-lookup"><span data-stu-id="f55f7-147">Note that the ER format now contains one more item.</span></span> <span data-ttu-id="f55f7-148">已向 Excel 添加了单元格 PaymDate。</span><span class="sxs-lookup"><span data-stu-id="f55f7-148">A cell, PaymDate, has been added to the Excel template.</span></span>  
12. <span data-ttu-id="f55f7-149">单击“映射”选项卡。</span><span class="sxs-lookup"><span data-stu-id="f55f7-149">Click the Mapping tab.</span></span>
13. <span data-ttu-id="f55f7-150">在树结构中，展开“模型”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-150">In the tree, expand 'model'.</span></span>
14. <span data-ttu-id="f55f7-151">在树结构中，展开“模型\付款”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-151">In the tree, expand 'model\Payments'.</span></span>
15. <span data-ttu-id="f55f7-152">在树结构中，选择“模型\付款\交易日期”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-152">In the tree, select 'model\Payments\Transaction date(TransactionDate)'.</span></span>
16. <span data-ttu-id="f55f7-153">单击“绑定”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-153">Click Bind.</span></span>
    * <span data-ttu-id="f55f7-154">指定在运行时向新单元格添加哪些数据。</span><span class="sxs-lookup"><span data-stu-id="f55f7-154">Specify what data is added to the new cell at runtime.</span></span>  
17. <span data-ttu-id="f55f7-155">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-155">Click Save.</span></span>
18. <span data-ttu-id="f55f7-156">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f55f7-156">Close the page.</span></span>

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a><span data-ttu-id="f55f7-157">启用修改后的 ER 格式草稿版本，以便在付款日记帐处理中使用。</span><span class="sxs-lookup"><span data-stu-id="f55f7-157">Enable the modified draft version of the ER format for use in payment journal processing</span></span>
1. <span data-ttu-id="f55f7-158">在操作窗格上，单击“配置”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-158">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="f55f7-159">单击“用户参数”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-159">Click User parameters.</span></span>
3. <span data-ttu-id="f55f7-160">在“运行设置”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-160">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="f55f7-161">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-161">Click OK.</span></span>
5. <span data-ttu-id="f55f7-162">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-162">Click Edit.</span></span>
6. <span data-ttu-id="f55f7-163">在“运行草稿”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="f55f7-163">Select Yes in the Run Draft field.</span></span>

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a><span data-ttu-id="f55f7-164">将修改后的 ER 格式草稿版本用于付款日记帐处理。</span><span class="sxs-lookup"><span data-stu-id="f55f7-164">Use the modified draft version of the ER format for payment journal processing</span></span>
    * <span data-ttu-id="f55f7-165">查看创建的工作表，包括付款日期这一付款行的新详细信息。</span><span class="sxs-lookup"><span data-stu-id="f55f7-165">Review the created worksheet, including new detail of payment lines – payment date.</span></span>  


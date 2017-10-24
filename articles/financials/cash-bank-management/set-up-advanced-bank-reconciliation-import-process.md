---
title: "设置高级银行对帐导入流程"
description: "高级银行对帐功能允许您在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中导入电子银行对账单，并与银行交易记录自动对帐。 本文介绍如何设置银行对账单的导入功能。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 785da18a851c4d040843f49ca9f1b9ae12d701d3
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a><span data-ttu-id="2e65f-104">设置高级银行对帐导入流程</span><span class="sxs-lookup"><span data-stu-id="2e65f-104">Set up the advanced bank reconciliation import process</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2e65f-105">高级银行对帐功能允许您在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中导入电子银行对账单，并与银行交易记录自动对帐。</span><span class="sxs-lookup"><span data-stu-id="2e65f-105">The Advanced bank reconciliation feature lets you import electronic bank statements and automatically reconcile them with bank transactions in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="2e65f-106">本文介绍如何设置银行对账单的导入功能。</span><span class="sxs-lookup"><span data-stu-id="2e65f-106">This article explains how to set up the import functionality for your bank statements.</span></span> 

<span data-ttu-id="2e65f-107">银行对账单导入设置因您电子银行对账单的格式的不同而不同。</span><span class="sxs-lookup"><span data-stu-id="2e65f-107">The setup for bank statement import varies, depending on the format of your electronic bank statement.</span></span> <span data-ttu-id="2e65f-108">Finance and Operations 支持三个现成的银行对账单格式︰ISO20022、MT940 和 BAI2。</span><span class="sxs-lookup"><span data-stu-id="2e65f-108">Finance and Operations supports three bank statement formats out of the box: ISO20022, MT940, and BAI2.</span></span>

## <a name="sample-files"></a><span data-ttu-id="2e65f-109">示例文件</span><span class="sxs-lookup"><span data-stu-id="2e65f-109">Sample files</span></span>
<span data-ttu-id="2e65f-110">对于所有三种格式，您必须有将电子银行对账单的原始格式转换为 Finance and Operations 可以使用的格式的文件。</span><span class="sxs-lookup"><span data-stu-id="2e65f-110">For all three formats, you must have files that translate the electronic bank statement from the original format to a format that Finance and Operations can use.</span></span> <span data-ttu-id="2e65f-111">您可以在 Microsoft Visual Studio 中应用程序资源管理器的**资源**节点下找到所需资源文件。</span><span class="sxs-lookup"><span data-stu-id="2e65f-111">You can find the required resource files under the **Resources** node in Application Explorer in Microsoft Visual Studio.</span></span> <span data-ttu-id="2e65f-112">找到文件后，将它们复制到一个已知位置，以便您可以更轻松地在设置流程中上载它们。</span><span class="sxs-lookup"><span data-stu-id="2e65f-112">After you find the files, copy them to a single known location, so that you can more easily upload them during the setup process.</span></span>

| <span data-ttu-id="2e65f-113">资源名称</span><span class="sxs-lookup"><span data-stu-id="2e65f-113">Resource name</span></span>                                           | <span data-ttu-id="2e65f-114">文件名</span><span class="sxs-lookup"><span data-stu-id="2e65f-114">File name</span></span>                            |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="2e65f-115">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="2e65f-115">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>              | <span data-ttu-id="2e65f-116">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="2e65f-116">BAI2CSV-to-BAI2XML.xslt</span></span>              |
| <span data-ttu-id="2e65f-117">BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="2e65f-117">BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt</span></span>       | <span data-ttu-id="2e65f-118">BAI2XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="2e65f-118">BAI2XML-to-Reconciliation.xslt</span></span>       |
| <span data-ttu-id="2e65f-119">BankStmtImport\_BankReconciliation\_to\_Composite\_xslt</span><span class="sxs-lookup"><span data-stu-id="2e65f-119">BankStmtImport\_BankReconciliation\_to\_Composite\_xslt</span></span> | <span data-ttu-id="2e65f-120">BankReconciliation-to-Composite.xslt</span><span class="sxs-lookup"><span data-stu-id="2e65f-120">BankReconciliation-to-Composite.xslt</span></span> |
| <span data-ttu-id="2e65f-121">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="2e65f-121">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span>   | <span data-ttu-id="2e65f-122">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="2e65f-122">ISO20022XML-to-Reconciliation.xslt</span></span>   |
| <span data-ttu-id="2e65f-123">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="2e65f-123">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>            | <span data-ttu-id="2e65f-124">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="2e65f-124">MT940TXT-to-MT940XML.xslt</span></span>            |
| <span data-ttu-id="2e65f-125">BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="2e65f-125">BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt</span></span>      | <span data-ttu-id="2e65f-126">MT940XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="2e65f-126">MT940XML-to-Reconciliation.xslt</span></span>      |
| <span data-ttu-id="2e65f-127">BankStmtImport\_SampleBankCompositeEntity\_xml</span><span class="sxs-lookup"><span data-stu-id="2e65f-127">BankStmtImport\_SampleBankCompositeEntity\_xml</span></span>          | <span data-ttu-id="2e65f-128">SampleBankCompositeEntity.xml</span><span class="sxs-lookup"><span data-stu-id="2e65f-128">SampleBankCompositeEntity.xml</span></span>        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="2e65f-129">银行对账单格式和技术布局的示例</span><span class="sxs-lookup"><span data-stu-id="2e65f-129">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="2e65f-130">下面是高级银行对帐导入文件技术布局定义的示例和三个相关银行对账单示例文件：https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="2e65f-130">Below are examples of the advanced bank reconciliation import file technical layout definitions and three related bank statement example files: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  

| <span data-ttu-id="2e65f-131">技术布局定义</span><span class="sxs-lookup"><span data-stu-id="2e65f-131">Technical layout definition</span></span>                             | <span data-ttu-id="2e65f-132">银行对账单示例文件</span><span class="sxs-lookup"><span data-stu-id="2e65f-132">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="2e65f-133">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="2e65f-133">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="2e65f-134">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="2e65f-134">MT940StatementExample</span></span>                |
| <span data-ttu-id="2e65f-135">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="2e65f-135">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="2e65f-136">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="2e65f-136">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="2e65f-137">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="2e65f-137">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="2e65f-138">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="2e65f-138">BAI2StatementExample</span></span>                 |

 

## <a name="set-up-the-import-of-iso20022-bank-statements"></a><span data-ttu-id="2e65f-139">设置 ISO20022 银行对账单的导入</span><span class="sxs-lookup"><span data-stu-id="2e65f-139">Set up the import of ISO20022 bank statements</span></span>
<span data-ttu-id="2e65f-140">首先，您必须通过使用数据实体框架定义 ISO20022 银行对账单的银行对账单格式处理组。</span><span class="sxs-lookup"><span data-stu-id="2e65f-140">First, you must define the bank statement format processing group for ISO20022 bank statements by using the data entity framework.</span></span>

1.  <span data-ttu-id="2e65f-141">转到**工作区** &gt; **数据管理**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-141">Go to **Workspaces** &gt; **Data management**.</span></span>
2.  <span data-ttu-id="2e65f-142">单击**导入**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-142">Click **Import**.</span></span>
3.  <span data-ttu-id="2e65f-143">为格式输入名称，如 **ISO20022**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-143">Enter a name for the format, such as **ISO20022**.</span></span>
4.  <span data-ttu-id="2e65f-144">将**源数据格式**字段设置为 **XML-元素**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-144">Set the **Source data format** field to **XML-Element**.</span></span>
5.  <span data-ttu-id="2e65f-145">将**实体名称**字段设置为**银行对账单**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-145">Set the **Entity name** field to **Bank statements**.</span></span>
6.  <span data-ttu-id="2e65f-146">若要上载导入文件，请单击**上载**，然后浏览以选择以前保存的 **SampleBankCompositeEntity.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="2e65f-146">To upload the import files, click **Upload**, and then browse to select the **SampleBankCompositeEntity.xml** file that you saved earlier.</span></span>
7.  <span data-ttu-id="2e65f-147">银行对账单实体上载且映射完成后，请单击实体的**查看地图**操作。</span><span class="sxs-lookup"><span data-stu-id="2e65f-147">After the Bank statements entity is uploaded and the mapping is completed, click the **View map** action for the entity.</span></span>
8.  <span data-ttu-id="2e65f-148">银行对账单实体是由四个单独的实体组成一个复合实体。</span><span class="sxs-lookup"><span data-stu-id="2e65f-148">The Bank statements entity is a composite entity that consists of four separate entities.</span></span> <span data-ttu-id="2e65f-149">在列表中，选择 **BankStatementDocumentEntity**，然后单击**查看地图**操作。</span><span class="sxs-lookup"><span data-stu-id="2e65f-149">In the list, select **BankStatementDocumentEntity**, and then click the **View map** action.</span></span>
9.  <span data-ttu-id="2e65f-150">在**转换**选项卡上，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-150">On the **Transformations** tab, click **New**.</span></span>
10. <span data-ttu-id="2e65f-151">对于序列号 1，请单击**上载文件**，并选择以前保存的 **ISO20022XML-to-Reconciliation.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="2e65f-151">For sequence number 1, click **Upload file**, and select the **ISO20022XML-to-Reconciliation.xslt** file that you saved earlier.</span></span> <span data-ttu-id="2e65f-152">**注意︰**Finance and Operations 转换文件使用标准格式构建。</span><span class="sxs-lookup"><span data-stu-id="2e65f-152">**Note:** Finance and Operations transformation files are built for the standard format.</span></span> <span data-ttu-id="2e65f-153">因为银行经常偏离这种格式，您可能必须更新要映射到您的银行帐单格式的转换文件。</span><span class="sxs-lookup"><span data-stu-id="2e65f-153">Because banks often diverge from this format, you may have to update the transformation file to map to your bank statement format.</span></span> <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. <span data-ttu-id="2e65f-154">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-154">Click **New**.</span></span>
12. <span data-ttu-id="2e65f-155">对于序列号 2，请单击**上载文件**，并选择以前保存的 **BankReconciliation-to-Composite.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="2e65f-155">For sequence number 2, click **Upload file**, and select the **BankReconciliation-to-Composite.xslt** file that you saved earlier.</span></span>
13. <span data-ttu-id="2e65f-156">单击**应用转换**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-156">Click **Apply transforms**.</span></span>

<span data-ttu-id="2e65f-157">设置格式处理组后，下一步是定义 ISO20022 银行对账单的银行对账单格式规则。</span><span class="sxs-lookup"><span data-stu-id="2e65f-157">After the format processing group is set up, the next step is to define the bank statement format rules for ISO20022 bank statements.</span></span>

1.  <span data-ttu-id="2e65f-158">转到**现金和银行管理** &gt; **设置** &gt; **高级银行对帐设置** &gt; **银行对账单格式**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-158">Go to **Cash and bank management** &gt; **Setup** &gt; **Advanced bank reconciliation setup** &gt; **Bank statement format**.</span></span>
2.  <span data-ttu-id="2e65f-159">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-159">Click **New**.</span></span>
3.  <span data-ttu-id="2e65f-160">指定对账单格式，如 **ISO20022**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-160">Specify a statement format, such as **ISO20022**.</span></span>
4.  <span data-ttu-id="2e65f-161">输入格式名称。</span><span class="sxs-lookup"><span data-stu-id="2e65f-161">Enter a name for the format.</span></span>
5.  <span data-ttu-id="2e65f-162">将**处理组**字段设置为之前定义的组，如 **ISO20022**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-162">Set the **Processing group** field to the group that you defined earlier, such as **ISO20022**.</span></span>
6.  <span data-ttu-id="2e65f-163">选中 **XML 文件**复选框。</span><span class="sxs-lookup"><span data-stu-id="2e65f-163">Select the **XML file** check box.</span></span>

<span data-ttu-id="2e65f-164">最后一步是启用高级银行对帐并设置银行帐户的对账单格式。</span><span class="sxs-lookup"><span data-stu-id="2e65f-164">The last step is to enable Advanced bank reconciliation and set the statement format on the bank account.</span></span>

1.  <span data-ttu-id="2e65f-165">转**“现金和银行管理** &gt; **银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-165">Go to **Cash and bank management** &gt; **Bank accounts**.</span></span>
2.  <span data-ttu-id="2e65f-166">选择银行帐户并打开帐户以查看详细信息。</span><span class="sxs-lookup"><span data-stu-id="2e65f-166">Select the bank account, and open it to view the details.</span></span>
3.  <span data-ttu-id="2e65f-167">在**对帐**选项卡上，设置**高级银行对帐**选项为**是**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-167">On the **Reconciliation** tab, set the **Advanced bank reconciliation** option to **Yes**.</span></span>
4.  <span data-ttu-id="2e65f-168">将**对账单格式**字段设置为之前创建的格式，如 **ISO20022**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-168">Set the **Statement format** field to the format that you created earlier, such as **ISO20022**.</span></span>

## <a name="set-up-the-import-of-mt940-bank-statements"></a><span data-ttu-id="2e65f-169">设置 MT940 银行对账单的导入</span><span class="sxs-lookup"><span data-stu-id="2e65f-169">Set up the import of MT940 bank statements</span></span>
<span data-ttu-id="2e65f-170">首先，您必须通过使用数据实体框架定义 MT940 银行对账单的银行对账单格式处理组。</span><span class="sxs-lookup"><span data-stu-id="2e65f-170">First, you must define the bank statement format processing group for MT940 bank statements by using the data entity framework.</span></span>

1.  <span data-ttu-id="2e65f-171">转到**工作区** &gt; **数据管理**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-171">Go to **Workspaces** &gt; **Data management**.</span></span>
2.  <span data-ttu-id="2e65f-172">单击**导入**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-172">Click **Import**.</span></span>
3.  <span data-ttu-id="2e65f-173">为格式输入名称，如 **MT940**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-173">Enter a name for the format, such as **MT940**.</span></span>
4.  <span data-ttu-id="2e65f-174">将**源数据格式**字段设置为 **XML-元素**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-174">Set the **Source data format** field to **XML-Element**.</span></span>
5.  <span data-ttu-id="2e65f-175">将**实体名称**字段设置为**银行对账单**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-175">Set the **Entity name** field to **Bank statements**.</span></span>
6.  <span data-ttu-id="2e65f-176">若要上载导入文件，请单击**上载**，然后浏览以选择以前保存的 **SampleBankCompositeEntity.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="2e65f-176">To upload import files, click **Upload**, and then browse to select the **SampleBankCompositeEntity.xml** file that you saved earlier.</span></span>
7.  <span data-ttu-id="2e65f-177">银行对账单实体上载且映射完成后，请单击实体的**查看地图**操作。</span><span class="sxs-lookup"><span data-stu-id="2e65f-177">After the Bank statements entity is uploaded and the mapping is completed, click the **View map** action for the entity.</span></span>
8.  <span data-ttu-id="2e65f-178">银行对账单实体是由四个单独的实体组成一个复合实体。</span><span class="sxs-lookup"><span data-stu-id="2e65f-178">The Bank statements entity is a composite entity that consists of four separate entities.</span></span> <span data-ttu-id="2e65f-179">在列表中，选择 **BankStatementDocumentEntity**，然后单击**查看地图**操作。</span><span class="sxs-lookup"><span data-stu-id="2e65f-179">In the list, select **BankStatementDocumentEntity**, and then click the **View map** action.</span></span>
9.  <span data-ttu-id="2e65f-180">在**转换**选项卡上，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-180">On the **Transformations** tab, click **New**.</span></span>
10. <span data-ttu-id="2e65f-181">对于序列号 1，请单击**上载文件**，并选择以前保存的 **MT940TXT-to-MT940XML.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="2e65f-181">For sequence number 1, click **Upload file**, and select the **MT940TXT-to-MT940XML.xslt** file that you saved earlier.</span></span>
11. <span data-ttu-id="2e65f-182">单击“**新建**”。</span><span class="sxs-lookup"><span data-stu-id="2e65f-182">Click **New**.</span></span>
12. <span data-ttu-id="2e65f-183">对于序列号 2，请单击**上载文件**，并选择以前保存的 **MT940XML-to-Reconciliation.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="2e65f-183">For sequence number 2, click **Upload file**, and select the **MT940XML-to-Reconciliation.xslt** file that you saved earlier.</span></span> <span data-ttu-id="2e65f-184">**注意︰**Finance and Operations 转换文件使用标准格式构建。</span><span class="sxs-lookup"><span data-stu-id="2e65f-184">**Note:** Finance and Operations transformation files are built for the standard format.</span></span> <span data-ttu-id="2e65f-185">因为银行经常偏离这种格式，您可能必须更新要映射到您的银行帐单格式的转换文件。</span><span class="sxs-lookup"><span data-stu-id="2e65f-185">Because banks often diverge from this format, you may have to update the transformation file to map to your bank statement format.</span></span> <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. <span data-ttu-id="2e65f-186">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-186">Click **New**.</span></span>
14. <span data-ttu-id="2e65f-187">对于序列号 3，请单击**上载文件**，并选择以前保存的 **BankReconciliation-to-Composite.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="2e65f-187">For sequence number 3, click **Upload file**, and select the **BankReconciliation-to-Composite.xslt** file that you saved earlier.</span></span>
15. <span data-ttu-id="2e65f-188">单击**应用转换**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-188">Click **Apply transforms**.</span></span>

<span data-ttu-id="2e65f-189">设置格式处理组后，下一步是定义 MT940 银行对账单的银行对账单格式规则。</span><span class="sxs-lookup"><span data-stu-id="2e65f-189">After the format processing group is set up, the next step is to define the bank statement format rules for MT940 bank statements.</span></span>

1.  <span data-ttu-id="2e65f-190">转到**现金和银行管理** &gt; **设置** &gt; **高级银行对帐设置** &gt; **银行对账单格式**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-190">Go to **Cash and bank management** &gt; **Setup** &gt; **Advanced bank reconciliation setup** &gt; **Bank statement format**.</span></span>
2.  <span data-ttu-id="2e65f-191">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-191">Click **New**.</span></span>
3.  <span data-ttu-id="2e65f-192">指定对账单格式，如 **MT940**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-192">Specify a statement format, such as **MT940**.</span></span>
4.  <span data-ttu-id="2e65f-193">输入格式名称。</span><span class="sxs-lookup"><span data-stu-id="2e65f-193">Enter a name for the format.</span></span>
5.  <span data-ttu-id="2e65f-194">将**处理组**字段设置为之前定义的组，如 **MT940**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-194">Set the **Processing group** field to the group that you defined earlier, such as **MT940**.</span></span>
6.  <span data-ttu-id="2e65f-195">将**文件类型**字段设置为 **txt**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-195">Set the **File type** field to **txt**.</span></span>

<span data-ttu-id="2e65f-196">最后一步是启用高级银行对帐并设置银行帐户的对账单格式。</span><span class="sxs-lookup"><span data-stu-id="2e65f-196">The last step is to enable Advanced bank reconciliation and set the statement format on the bank account.</span></span>

1.  <span data-ttu-id="2e65f-197">转**“现金和银行管理** &gt; **银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-197">Go to **Cash and bank management** &gt; **Bank accounts**.</span></span>
2.  <span data-ttu-id="2e65f-198">选择银行帐户并打开帐户以查看详细信息。</span><span class="sxs-lookup"><span data-stu-id="2e65f-198">Select the bank account, and open it to view the details.</span></span>
3.  <span data-ttu-id="2e65f-199">在**对帐**选项卡上，设置**高级银行对帐**选项为**是**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-199">On the **Reconciliation** tab, set the **Advanced bank reconciliation** option to **Yes**.</span></span>
4.  <span data-ttu-id="2e65f-200">当提示您确认您的选择并启用高级银行对帐时，请单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-200">When you're prompted to confirm your selection and enable Advanced bank reconciliation, click **OK**.</span></span>
5.  <span data-ttu-id="2e65f-201">将**对账单格式**字段设置为之前创建的格式，如 **MT940**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-201">Set the **Statement format** field to the format that you created earlier, such as **MT940**.</span></span>

## <a name="set-up-the-import-of-bai2-bank-statements"></a><span data-ttu-id="2e65f-202">设置 BAI2 银行对账单的导入</span><span class="sxs-lookup"><span data-stu-id="2e65f-202">Set up the import of BAI2 bank statements</span></span>
<span data-ttu-id="2e65f-203">首先，您必须通过使用数据实体框架定义 BAI2 银行对账单的银行对账单格式处理组。</span><span class="sxs-lookup"><span data-stu-id="2e65f-203">First, you must define the bank statement format processing group for BAI2 bank statements by using the data entity framework.</span></span>

1.  <span data-ttu-id="2e65f-204">转到**工作区** &gt; **数据管理**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-204">Go to **Workspaces** &gt; **Data management**.</span></span>
2.  <span data-ttu-id="2e65f-205">单击**导入**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-205">Click **Import**.</span></span>
3.  <span data-ttu-id="2e65f-206">为格式输入名称，如 **BAI2**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-206">Enter a name for the format, such as **BAI2**.</span></span>
4.  <span data-ttu-id="2e65f-207">将**源数据格式**字段设置为 **XML-元素**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-207">Set the **Source data format** field to **XML-Element**.</span></span>
5.  <span data-ttu-id="2e65f-208">将**实体名称**字段设置为**银行对账单**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-208">Set the **Entity name** field to **Bank statements**.</span></span>
6.  <span data-ttu-id="2e65f-209">若要上载导入文件，请单击**上载**，然后浏览以选择以前保存的 **SampleBankCompositeEntity.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="2e65f-209">To upload import files, click **Upload**, and then browse to select the **SampleBankCompositeEntity.xml** file that you saved earlier.</span></span>
7.  <span data-ttu-id="2e65f-210">银行对账单实体上载且映射完成后，请单击实体的**查看地图**操作。</span><span class="sxs-lookup"><span data-stu-id="2e65f-210">After the Bank statements entity is uploaded and the mapping is completed, click the **View map** action for the entity.</span></span>
8.  <span data-ttu-id="2e65f-211">银行对账单实体是由四个单独的实体组成一个复合实体。</span><span class="sxs-lookup"><span data-stu-id="2e65f-211">The Bank statements entity is a composite entity that consists of four separate entities.</span></span> <span data-ttu-id="2e65f-212">在列表中，选择 **BankStatementDocumentEntity**，然后单击**查看地图**操作。</span><span class="sxs-lookup"><span data-stu-id="2e65f-212">In the list, select **BankStatementDocumentEntity**, and then click the **View map** action.</span></span>
9.  <span data-ttu-id="2e65f-213">在**转换**选项卡上，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-213">On the **Transformations** tab, click **New**.</span></span>
10. <span data-ttu-id="2e65f-214">对于序列号 1，请单击**上载文件**，并选择以前保存的 **BAI2CSV-to-BAI2XML.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="2e65f-214">For sequence number 1, click **Upload file**, and select the **BAI2CSV-to-BAI2XML.xslt** file that you saved earlier.</span></span>
11. <span data-ttu-id="2e65f-215">单击“**新建**”。</span><span class="sxs-lookup"><span data-stu-id="2e65f-215">Click **New**.</span></span>
12. <span data-ttu-id="2e65f-216">对于序列号 2，请单击**上载文件**，并选择以前保存的 **BAI2XML-to-Reconciliation.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="2e65f-216">For sequence number 2, click **Upload file**, and select the **BAI2XML-to-Reconciliation.xslt** file that you saved earlier.</span></span> <span data-ttu-id="2e65f-217">**注意︰**Finance and Operations 转换文件使用标准格式构建。</span><span class="sxs-lookup"><span data-stu-id="2e65f-217">**Note:** Finance and Operations transformation files are built for the standard format.</span></span> <span data-ttu-id="2e65f-218">因为银行经常偏离这种格式，您可能必须更新要映射到您的银行帐单格式的转换文件。</span><span class="sxs-lookup"><span data-stu-id="2e65f-218">Because banks often diverge from this format, and you may have to update the transformation file to map to your bank statement format.</span></span> <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. <span data-ttu-id="2e65f-219">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-219">Click **New**.</span></span>
14. <span data-ttu-id="2e65f-220">对于序列号 3，请单击**上载文件**，并选择以前保存的 **BankReconciliation-to-Composite.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="2e65f-220">For sequence number 3, click **Upload file**, and select the **BankReconciliation-to-Composite.xslt** file that you saved earlier.</span></span>
15. <span data-ttu-id="2e65f-221">单击**应用转换**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-221">Click **Apply transforms**.</span></span>

<span data-ttu-id="2e65f-222">设置格式处理组后，下一步是定义 BAI2 银行对账单的银行对账单格式规则。</span><span class="sxs-lookup"><span data-stu-id="2e65f-222">After the format processing group is set up, the next step is to define the bank statement format rules for BAI2 bank statements.</span></span>

1.  <span data-ttu-id="2e65f-223">转到**现金和银行管理** &gt; **设置** &gt; **高级银行对帐设置** &gt; **银行对账单格式**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-223">Go to **Cash and bank management** &gt; **Setup** &gt; **Advanced bank reconciliation setup** &gt; **Bank statement format**.</span></span>
2.  <span data-ttu-id="2e65f-224">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-224">Click **New**.</span></span>
3.  <span data-ttu-id="2e65f-225">指定对账单格式，如 **BAI2**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-225">Specify a statement format, such as **BAI2**.</span></span>
4.  <span data-ttu-id="2e65f-226">输入格式名称。</span><span class="sxs-lookup"><span data-stu-id="2e65f-226">Enter a name for the format.</span></span>
5.  <span data-ttu-id="2e65f-227">将**处理组**字段设置为之前定义的组，如 **BAI2**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-227">Set the **Processing group** field to the group that you defined earlier, such as **BAI2**.</span></span>
6.  <span data-ttu-id="2e65f-228">将**文件类型**字段设置为 **txt**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-228">Set the **File type** field to **txt**.</span></span>

<span data-ttu-id="2e65f-229">最后一步是启用高级银行对帐并设置银行帐户的对账单格式。</span><span class="sxs-lookup"><span data-stu-id="2e65f-229">The last step is to enable Advanced bank reconciliation and set the statement format on the bank account.</span></span>

1.  <span data-ttu-id="2e65f-230">转**“现金和银行管理** &gt; **银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-230">Go to **Cash and bank management** &gt; **Bank accounts**.</span></span>
2.  <span data-ttu-id="2e65f-231">选择银行帐户并打开帐户以查看详细信息。</span><span class="sxs-lookup"><span data-stu-id="2e65f-231">Select the bank account, and open it to view the details.</span></span>
3.  <span data-ttu-id="2e65f-232">在**对帐**选项卡上，设置**高级银行对帐**选项为**是**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-232">On the **Reconciliation** tab, set the **Advanced bank reconciliation** option to **Yes**.</span></span>
4.  <span data-ttu-id="2e65f-233">当提示您确认您的选择并启用高级银行对帐时，请单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-233">When you're prompted to confirm your selection and enable Advanced bank reconciliation, click **OK**.</span></span>
5.  <span data-ttu-id="2e65f-234">将**对账单格式**字段设置为之前创建的格式，如 **BAI2**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-234">Set the **Statement format** field to the format that you created earlier, such as **BAI2**.</span></span>

## <a name="test-the-bank-statement-import"></a><span data-ttu-id="2e65f-235">测试银行对账单导入</span><span class="sxs-lookup"><span data-stu-id="2e65f-235">Test the bank statement import</span></span>
<span data-ttu-id="2e65f-236">最后一步是测试您是否可以导入银行对账单。</span><span class="sxs-lookup"><span data-stu-id="2e65f-236">The final step is to test that you can import your bank statement.</span></span>

1.  <span data-ttu-id="2e65f-237">转**“现金和银行管理** &gt; **银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-237">Go to **Cash and bank management** &gt; **Bank accounts**.</span></span>
2.  <span data-ttu-id="2e65f-238">选择为其启用高级银行对帐功能的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="2e65f-238">Select the bank account that Advanced bank reconciliation functionality is enabled for.</span></span>
3.  <span data-ttu-id="2e65f-239">在**对帐**选项卡上，单击**银行对账单**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-239">On the **Reconcile** tab, click **Bank statements**.</span></span>
4.  <span data-ttu-id="2e65f-240">在**银行对账单**页面上，单击**导入对账单**。</span><span class="sxs-lookup"><span data-stu-id="2e65f-240">On the **Bank statement** page, click **Import statement**.</span></span>
5.  <span data-ttu-id="2e65f-241">将**银行帐户**字段设置为所选银行帐户。</span><span class="sxs-lookup"><span data-stu-id="2e65f-241">Set the **Bank account** field to the selected bank account.</span></span> <span data-ttu-id="2e65f-242">**对账单格式**字段会自动设置，根据银行帐户的设置。</span><span class="sxs-lookup"><span data-stu-id="2e65f-242">The **Statement format** field will be set automatically, based on the setting on the bank account.</span></span>
6.  <span data-ttu-id="2e65f-243">单击**浏览**，然后选择您的电子银行对账单文件。</span><span class="sxs-lookup"><span data-stu-id="2e65f-243">Click **Browse**, and select your electronic bank statement file.</span></span>
7.  <span data-ttu-id="2e65f-244">单击“**上载**”。</span><span class="sxs-lookup"><span data-stu-id="2e65f-244">Click **Upload**.</span></span>
8.  <span data-ttu-id="2e65f-245">单击“**OK**”。</span><span class="sxs-lookup"><span data-stu-id="2e65f-245">Click **OK**.</span></span>

<span data-ttu-id="2e65f-246">如果导入成功，您将收到一条消息，指出您的对账单被导入。</span><span class="sxs-lookup"><span data-stu-id="2e65f-246">If the import is successful, you will receive a message that states that your statement was imported.</span></span> <span data-ttu-id="2e65f-247">如果导入不成功，在**数据管理**工作区，在**作业历史记录**部分，找到该作业。</span><span class="sxs-lookup"><span data-stu-id="2e65f-247">If the import wasn't successful, in the **Data management** workspace, in the **Job history** section, find the job.</span></span> <span data-ttu-id="2e65f-248">单击作业的**执行详细信息**打开**执行摘要**页，然后单击**查看执行日志**查看导入错误。</span><span class="sxs-lookup"><span data-stu-id="2e65f-248">Click **Execution details** for the job to open the **Execution summary** page, and then click **View execution log** to view the import errors.</span></span>




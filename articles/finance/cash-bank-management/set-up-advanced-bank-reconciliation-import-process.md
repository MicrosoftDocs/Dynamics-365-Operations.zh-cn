---
title: 设置高级银行对帐导入流程
description: 高级银行对帐功能让您可以导入电子银行对帐单，并可以将其与 Microsoft Dynamics 365 Finance 中的银行交易记录自动对帐。 本文介绍如何设置银行对账单的导入功能。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aba85b63abc11c9f32023e8499a02728dfc86bd1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188249"
---
# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a><span data-ttu-id="eba0c-104">设置高级银行对帐导入流程</span><span class="sxs-lookup"><span data-stu-id="eba0c-104">Set up the advanced bank reconciliation import process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eba0c-105">高级银行对帐功能让您可以导入电子银行对帐单，并可以将其与 Dynamics 365 Finance 中的银行交易记录自动对帐。</span><span class="sxs-lookup"><span data-stu-id="eba0c-105">The Advanced bank reconciliation feature lets you import electronic bank statements and automatically reconcile them with bank transactions in Dynamics 365 Finance.</span></span> <span data-ttu-id="eba0c-106">本文介绍如何设置银行对账单的导入功能。</span><span class="sxs-lookup"><span data-stu-id="eba0c-106">This article explains how to set up the import functionality for your bank statements.</span></span> 

<span data-ttu-id="eba0c-107">银行对账单导入设置因您电子银行对账单的格式的不同而不同。</span><span class="sxs-lookup"><span data-stu-id="eba0c-107">The setup for bank statement import varies, depending on the format of your electronic bank statement.</span></span> <span data-ttu-id="eba0c-108">Finance 支持三个现成的银行对账单格式︰ISO20022、MT940 和 BAI2。</span><span class="sxs-lookup"><span data-stu-id="eba0c-108">Finance supports three bank statement formats out of the box: ISO20022, MT940, and BAI2.</span></span>

## <a name="set-time-zone-preference"></a><span data-ttu-id="eba0c-109">设置时区首选项</span><span class="sxs-lookup"><span data-stu-id="eba0c-109">Set time zone preference</span></span>
<span data-ttu-id="eba0c-110">配置银行对帐单导入设置时，务必注意将导入的银行对帐单文件内的日期时间数据的时区。</span><span class="sxs-lookup"><span data-stu-id="eba0c-110">When you configure the bank statement import settings, it can be important to consider the time zone of the date-time data within the bank statement files that will be imported.</span></span> <span data-ttu-id="eba0c-111">默认假设所有日期和时间值均为协调世界时 (UTC)，因此导入数据时不应用时区转换。</span><span class="sxs-lookup"><span data-stu-id="eba0c-111">The default is to assume any date and time values are already in Coordinated Universal Time (UTC) and so no time zone conversion will be applied when you import the data.</span></span> 

<span data-ttu-id="eba0c-112">提供了一个选项，用于指定导入数据时要使用的时区。</span><span class="sxs-lookup"><span data-stu-id="eba0c-112">There is an option available to specify a time zone to use for importing data.</span></span> <span data-ttu-id="eba0c-113">此选项位于每个**源数据格式详细信息**页（**数据管理工作区 > 配置数据源 > 选择数据格式 > 区域设置**快速选项卡）中的**时区首选项**字段内。</span><span class="sxs-lookup"><span data-stu-id="eba0c-113">This option is availble in the **Time zone preference** field on each **Source data format details** page (**Data management workspace > Configure data sources > Select a data format > Regional settings** FastTab).</span></span> <span data-ttu-id="eba0c-114">您输入的这个时区首选项将应用于所有使用该源数据格式的导入。</span><span class="sxs-lookup"><span data-stu-id="eba0c-114">This time zone preference you enter will apply to all the imports that use that source data format.</span></span> <span data-ttu-id="eba0c-115">可根据从多个时区导入数据的需要创建任意数量的数据源格式。</span><span class="sxs-lookup"><span data-stu-id="eba0c-115">You can create as many data source formats as needed for importing data from multiple time zones.</span></span> <span data-ttu-id="eba0c-116">时区首选项应该是导入文件中的日期和时间数据的本地时区。</span><span class="sxs-lookup"><span data-stu-id="eba0c-116">The time zone preference should be the local time zone of the date and time data in the import file.</span></span> <span data-ttu-id="eba0c-117">时区首选项应该是导入文件中的日期时间数据的本地时区。</span><span class="sxs-lookup"><span data-stu-id="eba0c-117">The time zone preference should be the local time zone of the date-time data in the import file.</span></span> 

<span data-ttu-id="eba0c-118">此时区可能与用户或公司的时区不同，因此请务必分辨清楚日期和时间数据正在使用哪个时区。</span><span class="sxs-lookup"><span data-stu-id="eba0c-118">This time zone might not be the same as a user’s or company’s time zone, so be sure to clarify what time zone the date and time data is using.</span></span> <span data-ttu-id="eba0c-119">建议在设置时区首选项时注意以下事项。</span><span class="sxs-lookup"><span data-stu-id="eba0c-119">We recommend that you consider the following points when setting a time zone preference.</span></span> 

 - <span data-ttu-id="eba0c-120">时区首选项将应用于所有使用该源数据格式的导入。</span><span class="sxs-lookup"><span data-stu-id="eba0c-120">The time zone preference will apply to all imports using that source data format.</span></span> <span data-ttu-id="eba0c-121">可根据处理从多个时区导入数据的需要创建任意数量的数据源格式。</span><span class="sxs-lookup"><span data-stu-id="eba0c-121">You can create as many data source formats as needed to handle importing data from multiple time zones.</span></span> 
 
 - <span data-ttu-id="eba0c-122">时区首选项应该是导入文件中的日期和时间数据的本地时区。</span><span class="sxs-lookup"><span data-stu-id="eba0c-122">The time zone preference should be the local time zone of the date and time data in the import file.</span></span> 
 
 - <span data-ttu-id="eba0c-123">日期和时间数据的时区可能与用户或公司的时区不同。</span><span class="sxs-lookup"><span data-stu-id="eba0c-123">The time zone of the date and time data might not be the same as a user’s or company’s time zone.</span></span>
 
 - <span data-ttu-id="eba0c-124">用户可以使用**用户选项**调整自己的时区。</span><span class="sxs-lookup"><span data-stu-id="eba0c-124">Users can adjust their own time zone using their **User options**.</span></span>

<span data-ttu-id="eba0c-125">请注意，导入银行对帐单时，以下操作可帮助将潜在的日期和时间冲突降到最少。</span><span class="sxs-lookup"><span data-stu-id="eba0c-125">Note that the following actions can help minimize potential date and time conflicts when you import bank statements.</span></span> 

 - <span data-ttu-id="eba0c-126">避免更改已经导入了对帐单的任何银行帐户的时区首选项。</span><span class="sxs-lookup"><span data-stu-id="eba0c-126">Avoid changing the time zone preferences for any bank accounts that have already had statements imported.</span></span> <span data-ttu-id="eba0c-127">因为时区调整，更改时区首选项可能会影响新对帐单相对现有对帐单的排序。</span><span class="sxs-lookup"><span data-stu-id="eba0c-127">Changing the time zone preference could impact the ordering of new statements relative to existing statements due to the time zone adjustment.</span></span> 
 
 - <span data-ttu-id="eba0c-128">查看所有使用所选数据源格式的导入。</span><span class="sxs-lookup"><span data-stu-id="eba0c-128">Review all the imports that use the selected data source format.</span></span> <span data-ttu-id="eba0c-129">为该格式指定的时区首选项将应用于所有使用该格式的导入项目。</span><span class="sxs-lookup"><span data-stu-id="eba0c-129">The time zone preference specified for the format will apply to all the import projects that use that format.</span></span> <span data-ttu-id="eba0c-130">验证时区首选项适合所有使用该格式的导入项目。</span><span class="sxs-lookup"><span data-stu-id="eba0c-130">Verify that the time zone preference is appropriate for all the import projects that use that format.</span></span>

## <a name="sample-files"></a><span data-ttu-id="eba0c-131">示例文件</span><span class="sxs-lookup"><span data-stu-id="eba0c-131">Sample files</span></span>
<span data-ttu-id="eba0c-132">对于所有三种格式，您必须有将电子银行对帐单的原始格式转换为 Finance 可以使用的格式的文件。</span><span class="sxs-lookup"><span data-stu-id="eba0c-132">For all three formats, you must have files that translate the electronic bank statement from the original format to a format that Finance can use.</span></span> <span data-ttu-id="eba0c-133">您可以在 Microsoft Visual Studio 中应用程序资源管理器的**资源**节点下找到所需资源文件。</span><span class="sxs-lookup"><span data-stu-id="eba0c-133">You can find the required resource files under the **Resources** node in Application Explorer in Microsoft Visual Studio.</span></span> <span data-ttu-id="eba0c-134">找到文件后，将它们复制到一个已知位置，以便您可以更轻松地在设置流程中上载它们。</span><span class="sxs-lookup"><span data-stu-id="eba0c-134">After you find the files, copy them to a single known location, so that you can more easily upload them during the setup process.</span></span>

| <span data-ttu-id="eba0c-135">资源名称</span><span class="sxs-lookup"><span data-stu-id="eba0c-135">Resource name</span></span>                                           | <span data-ttu-id="eba0c-136">文件名</span><span class="sxs-lookup"><span data-stu-id="eba0c-136">File name</span></span>                            |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="eba0c-137">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="eba0c-137">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>              | <span data-ttu-id="eba0c-138">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="eba0c-138">BAI2CSV-to-BAI2XML.xslt</span></span>              |
| <span data-ttu-id="eba0c-139">BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="eba0c-139">BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt</span></span>       | <span data-ttu-id="eba0c-140">BAI2XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="eba0c-140">BAI2XML-to-Reconciliation.xslt</span></span>       |
| <span data-ttu-id="eba0c-141">BankStmtImport\_BankReconciliation\_to\_Composite\_xslt</span><span class="sxs-lookup"><span data-stu-id="eba0c-141">BankStmtImport\_BankReconciliation\_to\_Composite\_xslt</span></span> | <span data-ttu-id="eba0c-142">BankReconciliation-to-Composite.xslt</span><span class="sxs-lookup"><span data-stu-id="eba0c-142">BankReconciliation-to-Composite.xslt</span></span> |
| <span data-ttu-id="eba0c-143">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="eba0c-143">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span>   | <span data-ttu-id="eba0c-144">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="eba0c-144">ISO20022XML-to-Reconciliation.xslt</span></span>   |
| <span data-ttu-id="eba0c-145">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="eba0c-145">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>            | <span data-ttu-id="eba0c-146">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="eba0c-146">MT940TXT-to-MT940XML.xslt</span></span>            |
| <span data-ttu-id="eba0c-147">BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="eba0c-147">BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt</span></span>      | <span data-ttu-id="eba0c-148">MT940XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="eba0c-148">MT940XML-to-Reconciliation.xslt</span></span>      |
| <span data-ttu-id="eba0c-149">BankStmtImport\_SampleBankCompositeEntity\_xml</span><span class="sxs-lookup"><span data-stu-id="eba0c-149">BankStmtImport\_SampleBankCompositeEntity\_xml</span></span>          | <span data-ttu-id="eba0c-150">SampleBankCompositeEntity.xml</span><span class="sxs-lookup"><span data-stu-id="eba0c-150">SampleBankCompositeEntity.xml</span></span>        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="eba0c-151">银行对账单格式和技术布局的示例</span><span class="sxs-lookup"><span data-stu-id="eba0c-151">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="eba0c-152">下面是高级银行对帐导入文件技术布局定义的示例和三个相关银行对帐单示例文件：https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="eba0c-152">Below are examples of the advanced bank reconciliation import file technical layout definitions and three related bank statement example files: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  

| <span data-ttu-id="eba0c-153">技术布局定义</span><span class="sxs-lookup"><span data-stu-id="eba0c-153">Technical layout definition</span></span>                             | <span data-ttu-id="eba0c-154">银行对账单示例文件</span><span class="sxs-lookup"><span data-stu-id="eba0c-154">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="eba0c-155">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="eba0c-155">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="eba0c-156">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="eba0c-156">MT940StatementExample</span></span>                |
| <span data-ttu-id="eba0c-157">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="eba0c-157">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="eba0c-158">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="eba0c-158">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="eba0c-159">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="eba0c-159">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="eba0c-160">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="eba0c-160">BAI2StatementExample</span></span>                 |



## <a name="set-up-the-import-of-iso20022-bank-statements"></a><span data-ttu-id="eba0c-161">设置 ISO20022 银行对账单的导入</span><span class="sxs-lookup"><span data-stu-id="eba0c-161">Set up the import of ISO20022 bank statements</span></span>
<span data-ttu-id="eba0c-162">首先，您必须通过使用数据实体框架定义 ISO20022 银行对账单的银行对账单格式处理组。</span><span class="sxs-lookup"><span data-stu-id="eba0c-162">First, you must define the bank statement format processing group for ISO20022 bank statements by using the data entity framework.</span></span>

1.  <span data-ttu-id="eba0c-163">转到**工作区** &gt; **数据管理**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-163">Go to **Workspaces** &gt; **Data management**.</span></span>
2.  <span data-ttu-id="eba0c-164">单击**导入**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-164">Click **Import**.</span></span>
3.  <span data-ttu-id="eba0c-165">为格式输入名称，如 **ISO20022**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-165">Enter a name for the format, such as **ISO20022**.</span></span>
4.  <span data-ttu-id="eba0c-166">将**源数据格式**字段设置为 **XML-元素**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-166">Set the **Source data format** field to **XML-Element**.</span></span>
5.  <span data-ttu-id="eba0c-167">将**实体名称**字段设置为**银行对账单**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-167">Set the **Entity name** field to **Bank statements**.</span></span>
6.  <span data-ttu-id="eba0c-168">若要上载导入文件，请单击**上载**，然后浏览以选择以前保存的 **SampleBankCompositeEntity.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="eba0c-168">To upload the import files, click **Upload**, and then browse to select the **SampleBankCompositeEntity.xml** file that you saved earlier.</span></span>
7.  <span data-ttu-id="eba0c-169">银行对账单实体上载且映射完成后，请单击实体的**查看地图**操作。</span><span class="sxs-lookup"><span data-stu-id="eba0c-169">After the Bank statements entity is uploaded and the mapping is completed, click the **View map** action for the entity.</span></span>
8.  <span data-ttu-id="eba0c-170">银行对账单实体是由四个单独的实体组成一个复合实体。</span><span class="sxs-lookup"><span data-stu-id="eba0c-170">The Bank statements entity is a composite entity that consists of four separate entities.</span></span> <span data-ttu-id="eba0c-171">在列表中，选择 **BankStatementDocumentEntity**，然后单击**查看地图**操作。</span><span class="sxs-lookup"><span data-stu-id="eba0c-171">In the list, select **BankStatementDocumentEntity**, and then click the **View map** action.</span></span>
9.  <span data-ttu-id="eba0c-172">在**转换**选项卡上，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-172">On the **Transformations** tab, click **New**.</span></span>
10. <span data-ttu-id="eba0c-173">对于序列号 1，请单击**上载文件**，并选择以前保存的 **ISO20022XML-to-Reconciliation.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="eba0c-173">For sequence number 1, click **Upload file**, and select the **ISO20022XML-to-Reconciliation.xslt** file that you saved earlier.</span></span> <span data-ttu-id="eba0c-174">**注意︰** 转换文件使用标准格式构建。</span><span class="sxs-lookup"><span data-stu-id="eba0c-174">**Note:** Transformation files are built for the standard format.</span></span> <span data-ttu-id="eba0c-175">因为银行经常偏离这种格式，您可能必须更新要映射到您的银行帐单格式的转换文件。</span><span class="sxs-lookup"><span data-stu-id="eba0c-175">Because banks often diverge from this format, you may have to update the transformation file to map to your bank statement format.</span></span> <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. <span data-ttu-id="eba0c-176">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-176">Click **New**.</span></span>
12. <span data-ttu-id="eba0c-177">对于序列号 2，请单击**上载文件**，并选择以前保存的 **BankReconciliation-to-Composite.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="eba0c-177">For sequence number 2, click **Upload file**, and select the **BankReconciliation-to-Composite.xslt** file that you saved earlier.</span></span>
13. <span data-ttu-id="eba0c-178">单击**应用转换**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-178">Click **Apply transforms**.</span></span>

<span data-ttu-id="eba0c-179">设置格式处理组后，下一步是定义 ISO20022 银行对账单的银行对账单格式规则。</span><span class="sxs-lookup"><span data-stu-id="eba0c-179">After the format processing group is set up, the next step is to define the bank statement format rules for ISO20022 bank statements.</span></span>

1.  <span data-ttu-id="eba0c-180">转到**现金和银行管理** &gt; **设置** &gt; **高级银行对帐设置** &gt; **银行对账单格式**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-180">Go to **Cash and bank management** &gt; **Setup** &gt; **Advanced bank reconciliation setup** &gt; **Bank statement format**.</span></span>
2.  <span data-ttu-id="eba0c-181">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-181">Click **New**.</span></span>
3.  <span data-ttu-id="eba0c-182">指定对账单格式，如 **ISO20022**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-182">Specify a statement format, such as **ISO20022**.</span></span>
4.  <span data-ttu-id="eba0c-183">输入格式名称。</span><span class="sxs-lookup"><span data-stu-id="eba0c-183">Enter a name for the format.</span></span>
5.  <span data-ttu-id="eba0c-184">将**处理组**字段设置为之前定义的组，如 **ISO20022**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-184">Set the **Processing group** field to the group that you defined earlier, such as **ISO20022**.</span></span>
6.  <span data-ttu-id="eba0c-185">选中 **XML 文件**复选框。</span><span class="sxs-lookup"><span data-stu-id="eba0c-185">Select the **XML file** check box.</span></span>

<span data-ttu-id="eba0c-186">最后一步是启用高级银行对帐并设置银行帐户的对账单格式。</span><span class="sxs-lookup"><span data-stu-id="eba0c-186">The last step is to enable Advanced bank reconciliation and set the statement format on the bank account.</span></span>

1.  <span data-ttu-id="eba0c-187">转**现金和银行管理** &gt; **银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-187">Go to **Cash and bank management** &gt; **Bank accounts**.</span></span>
2.  <span data-ttu-id="eba0c-188">选择银行帐户并打开帐户以查看详细信息。</span><span class="sxs-lookup"><span data-stu-id="eba0c-188">Select the bank account, and open it to view the details.</span></span>
3.  <span data-ttu-id="eba0c-189">在**对帐**选项卡上，设置**高级银行对帐**选项为**是**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-189">On the **Reconciliation** tab, set the **Advanced bank reconciliation** option to **Yes**.</span></span>
4.  <span data-ttu-id="eba0c-190">将**对账单格式**字段设置为之前创建的格式，如 **ISO20022**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-190">Set the **Statement format** field to the format that you created earlier, such as **ISO20022**.</span></span>

## <a name="set-up-the-import-of-mt940-bank-statements"></a><span data-ttu-id="eba0c-191">设置 MT940 银行对账单的导入</span><span class="sxs-lookup"><span data-stu-id="eba0c-191">Set up the import of MT940 bank statements</span></span>
<span data-ttu-id="eba0c-192">首先，您必须通过使用数据实体框架定义 MT940 银行对账单的银行对账单格式处理组。</span><span class="sxs-lookup"><span data-stu-id="eba0c-192">First, you must define the bank statement format processing group for MT940 bank statements by using the data entity framework.</span></span>

1.  <span data-ttu-id="eba0c-193">转到**工作区** &gt; **数据管理**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-193">Go to **Workspaces** &gt; **Data management**.</span></span>
2.  <span data-ttu-id="eba0c-194">单击**导入**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-194">Click **Import**.</span></span>
3.  <span data-ttu-id="eba0c-195">为格式输入名称，如 **MT940**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-195">Enter a name for the format, such as **MT940**.</span></span>
4.  <span data-ttu-id="eba0c-196">将**源数据格式**字段设置为 **XML-元素**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-196">Set the **Source data format** field to **XML-Element**.</span></span>
5.  <span data-ttu-id="eba0c-197">将**实体名称**字段设置为**银行对账单**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-197">Set the **Entity name** field to **Bank statements**.</span></span>
6.  <span data-ttu-id="eba0c-198">若要上载导入文件，请单击**上载**，然后浏览以选择以前保存的 **SampleBankCompositeEntity.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="eba0c-198">To upload import files, click **Upload**, and then browse to select the **SampleBankCompositeEntity.xml** file that you saved earlier.</span></span>
7.  <span data-ttu-id="eba0c-199">银行对账单实体上载且映射完成后，请单击实体的**查看地图**操作。</span><span class="sxs-lookup"><span data-stu-id="eba0c-199">After the Bank statements entity is uploaded and the mapping is completed, click the **View map** action for the entity.</span></span>
8.  <span data-ttu-id="eba0c-200">银行对账单实体是由四个单独的实体组成一个复合实体。</span><span class="sxs-lookup"><span data-stu-id="eba0c-200">The Bank statements entity is a composite entity that consists of four separate entities.</span></span> <span data-ttu-id="eba0c-201">在列表中，选择 **BankStatementDocumentEntity**，然后单击**查看地图**操作。</span><span class="sxs-lookup"><span data-stu-id="eba0c-201">In the list, select **BankStatementDocumentEntity**, and then click the **View map** action.</span></span>
9.  <span data-ttu-id="eba0c-202">在**转换**选项卡上，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-202">On the **Transformations** tab, click **New**.</span></span>
10. <span data-ttu-id="eba0c-203">对于序列号 1，请单击**上载文件**，并选择以前保存的 **MT940TXT-to-MT940XML.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="eba0c-203">For sequence number 1, click **Upload file**, and select the **MT940TXT-to-MT940XML.xslt** file that you saved earlier.</span></span>
11. <span data-ttu-id="eba0c-204">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-204">Click **New**.</span></span>
12. <span data-ttu-id="eba0c-205">对于序列号 2，请单击**上载文件**，并选择以前保存的 **MT940XML-to-Reconciliation.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="eba0c-205">For sequence number 2, click **Upload file**, and select the **MT940XML-to-Reconciliation.xslt** file that you saved earlier.</span></span> <span data-ttu-id="eba0c-206">**注意︰** 转换文件使用标准格式构建。</span><span class="sxs-lookup"><span data-stu-id="eba0c-206">**Note:** Transformation files are built for the standard format.</span></span> <span data-ttu-id="eba0c-207">因为银行经常偏离这种格式，您可能必须更新要映射到您的银行帐单格式的转换文件。</span><span class="sxs-lookup"><span data-stu-id="eba0c-207">Because banks often diverge from this format, you may have to update the transformation file to map to your bank statement format.</span></span> <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. <span data-ttu-id="eba0c-208">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-208">Click **New**.</span></span>
14. <span data-ttu-id="eba0c-209">对于序列号 3，请单击**上载文件**，并选择以前保存的 **BankReconciliation-to-Composite.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="eba0c-209">For sequence number 3, click **Upload file**, and select the **BankReconciliation-to-Composite.xslt** file that you saved earlier.</span></span>
15. <span data-ttu-id="eba0c-210">单击**应用转换**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-210">Click **Apply transforms**.</span></span>

<span data-ttu-id="eba0c-211">设置格式处理组后，下一步是定义 MT940 银行对账单的银行对账单格式规则。</span><span class="sxs-lookup"><span data-stu-id="eba0c-211">After the format processing group is set up, the next step is to define the bank statement format rules for MT940 bank statements.</span></span>

1.  <span data-ttu-id="eba0c-212">转到**现金和银行管理** &gt; **设置** &gt; **高级银行对帐设置** &gt; **银行对账单格式**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-212">Go to **Cash and bank management** &gt; **Setup** &gt; **Advanced bank reconciliation setup** &gt; **Bank statement format**.</span></span>
2.  <span data-ttu-id="eba0c-213">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-213">Click **New**.</span></span>
3.  <span data-ttu-id="eba0c-214">指定对账单格式，如 **MT940**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-214">Specify a statement format, such as **MT940**.</span></span>
4.  <span data-ttu-id="eba0c-215">输入格式名称。</span><span class="sxs-lookup"><span data-stu-id="eba0c-215">Enter a name for the format.</span></span>
5.  <span data-ttu-id="eba0c-216">将**处理组**字段设置为之前定义的组，如 **MT940**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-216">Set the **Processing group** field to the group that you defined earlier, such as **MT940**.</span></span>
6.  <span data-ttu-id="eba0c-217">将**文件类型**字段设置为 **txt**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-217">Set the **File type** field to **txt**.</span></span>

<span data-ttu-id="eba0c-218">最后一步是启用高级银行对帐并设置银行帐户的对账单格式。</span><span class="sxs-lookup"><span data-stu-id="eba0c-218">The last step is to enable Advanced bank reconciliation and set the statement format on the bank account.</span></span>

1.  <span data-ttu-id="eba0c-219">转**现金和银行管理** &gt; **银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-219">Go to **Cash and bank management** &gt; **Bank accounts**.</span></span>
2.  <span data-ttu-id="eba0c-220">选择银行帐户并打开帐户以查看详细信息。</span><span class="sxs-lookup"><span data-stu-id="eba0c-220">Select the bank account, and open it to view the details.</span></span>
3.  <span data-ttu-id="eba0c-221">在**对帐**选项卡上，设置**高级银行对帐**选项为**是**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-221">On the **Reconciliation** tab, set the **Advanced bank reconciliation** option to **Yes**.</span></span>
4.  <span data-ttu-id="eba0c-222">当提示您确认您的选择并启用高级银行对帐时，请单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-222">When you're prompted to confirm your selection and enable Advanced bank reconciliation, click **OK**.</span></span>
5.  <span data-ttu-id="eba0c-223">将**对账单格式**字段设置为之前创建的格式，如 **MT940**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-223">Set the **Statement format** field to the format that you created earlier, such as **MT940**.</span></span>

## <a name="set-up-the-import-of-bai2-bank-statements"></a><span data-ttu-id="eba0c-224">设置 BAI2 银行对账单的导入</span><span class="sxs-lookup"><span data-stu-id="eba0c-224">Set up the import of BAI2 bank statements</span></span>
<span data-ttu-id="eba0c-225">首先，您必须通过使用数据实体框架定义 BAI2 银行对账单的银行对账单格式处理组。</span><span class="sxs-lookup"><span data-stu-id="eba0c-225">First, you must define the bank statement format processing group for BAI2 bank statements by using the data entity framework.</span></span>

1.  <span data-ttu-id="eba0c-226">转到**工作区** &gt; **数据管理**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-226">Go to **Workspaces** &gt; **Data management**.</span></span>
2.  <span data-ttu-id="eba0c-227">单击**导入**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-227">Click **Import**.</span></span>
3.  <span data-ttu-id="eba0c-228">为格式输入名称，如 **BAI2**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-228">Enter a name for the format, such as **BAI2**.</span></span>
4.  <span data-ttu-id="eba0c-229">将**源数据格式**字段设置为 **XML-元素**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-229">Set the **Source data format** field to **XML-Element**.</span></span>
5.  <span data-ttu-id="eba0c-230">将**实体名称**字段设置为**银行对账单**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-230">Set the **Entity name** field to **Bank statements**.</span></span>
6.  <span data-ttu-id="eba0c-231">若要上载导入文件，请单击**上载**，然后浏览以选择以前保存的 **SampleBankCompositeEntity.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="eba0c-231">To upload import files, click **Upload**, and then browse to select the **SampleBankCompositeEntity.xml** file that you saved earlier.</span></span>
7.  <span data-ttu-id="eba0c-232">银行对账单实体上载且映射完成后，请单击实体的**查看地图**操作。</span><span class="sxs-lookup"><span data-stu-id="eba0c-232">After the Bank statements entity is uploaded and the mapping is completed, click the **View map** action for the entity.</span></span>
8.  <span data-ttu-id="eba0c-233">银行对账单实体是由四个单独的实体组成一个复合实体。</span><span class="sxs-lookup"><span data-stu-id="eba0c-233">The Bank statements entity is a composite entity that consists of four separate entities.</span></span> <span data-ttu-id="eba0c-234">在列表中，选择 **BankStatementDocumentEntity**，然后单击**查看地图**操作。</span><span class="sxs-lookup"><span data-stu-id="eba0c-234">In the list, select **BankStatementDocumentEntity**, and then click the **View map** action.</span></span>
9.  <span data-ttu-id="eba0c-235">在**转换**选项卡上，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-235">On the **Transformations** tab, click **New**.</span></span>
10. <span data-ttu-id="eba0c-236">对于序列号 1，请单击**上载文件**，并选择以前保存的 **BAI2CSV-to-BAI2XML.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="eba0c-236">For sequence number 1, click **Upload file**, and select the **BAI2CSV-to-BAI2XML.xslt** file that you saved earlier.</span></span>
11. <span data-ttu-id="eba0c-237">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-237">Click **New**.</span></span>
12. <span data-ttu-id="eba0c-238">对于序列号 2，请单击**上载文件**，并选择以前保存的 **BAI2XML-to-Reconciliation.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="eba0c-238">For sequence number 2, click **Upload file**, and select the **BAI2XML-to-Reconciliation.xslt** file that you saved earlier.</span></span> <span data-ttu-id="eba0c-239">**注意︰** 转换文件使用标准格式构建。</span><span class="sxs-lookup"><span data-stu-id="eba0c-239">**Note:** Transformation files are built for the standard format.</span></span> <span data-ttu-id="eba0c-240">因为银行经常偏离这种格式，您可能必须更新要映射到您的银行帐单格式的转换文件。</span><span class="sxs-lookup"><span data-stu-id="eba0c-240">Because banks often diverge from this format, and you may have to update the transformation file to map to your bank statement format.</span></span> <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. <span data-ttu-id="eba0c-241">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-241">Click **New**.</span></span>
14. <span data-ttu-id="eba0c-242">对于序列号 3，请单击**上载文件**，并选择以前保存的 **BankReconciliation-to-Composite.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="eba0c-242">For sequence number 3, click **Upload file**, and select the **BankReconciliation-to-Composite.xslt** file that you saved earlier.</span></span>
15. <span data-ttu-id="eba0c-243">单击**应用转换**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-243">Click **Apply transforms**.</span></span>

<span data-ttu-id="eba0c-244">设置格式处理组后，下一步是定义 BAI2 银行对账单的银行对账单格式规则。</span><span class="sxs-lookup"><span data-stu-id="eba0c-244">After the format processing group is set up, the next step is to define the bank statement format rules for BAI2 bank statements.</span></span>

1.  <span data-ttu-id="eba0c-245">转到**现金和银行管理** &gt; **设置** &gt; **高级银行对帐设置** &gt; **银行对账单格式**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-245">Go to **Cash and bank management** &gt; **Setup** &gt; **Advanced bank reconciliation setup** &gt; **Bank statement format**.</span></span>
2.  <span data-ttu-id="eba0c-246">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-246">Click **New**.</span></span>
3.  <span data-ttu-id="eba0c-247">指定对账单格式，如 **BAI2**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-247">Specify a statement format, such as **BAI2**.</span></span>
4.  <span data-ttu-id="eba0c-248">输入格式名称。</span><span class="sxs-lookup"><span data-stu-id="eba0c-248">Enter a name for the format.</span></span>
5.  <span data-ttu-id="eba0c-249">将**处理组**字段设置为之前定义的组，如 **BAI2**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-249">Set the **Processing group** field to the group that you defined earlier, such as **BAI2**.</span></span>
6.  <span data-ttu-id="eba0c-250">将**文件类型**字段设置为 **txt**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-250">Set the **File type** field to **txt**.</span></span>

<span data-ttu-id="eba0c-251">最后一步是启用高级银行对帐并设置银行帐户的对账单格式。</span><span class="sxs-lookup"><span data-stu-id="eba0c-251">The last step is to enable Advanced bank reconciliation and set the statement format on the bank account.</span></span>

1.  <span data-ttu-id="eba0c-252">转**现金和银行管理** &gt; **银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-252">Go to **Cash and bank management** &gt; **Bank accounts**.</span></span>
2.  <span data-ttu-id="eba0c-253">选择银行帐户并打开帐户以查看详细信息。</span><span class="sxs-lookup"><span data-stu-id="eba0c-253">Select the bank account, and open it to view the details.</span></span>
3.  <span data-ttu-id="eba0c-254">在**对帐**选项卡上，设置**高级银行对帐**选项为**是**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-254">On the **Reconciliation** tab, set the **Advanced bank reconciliation** option to **Yes**.</span></span>
4.  <span data-ttu-id="eba0c-255">当提示您确认您的选择并启用高级银行对帐时，请单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-255">When you're prompted to confirm your selection and enable Advanced bank reconciliation, click **OK**.</span></span>
5.  <span data-ttu-id="eba0c-256">将**对账单格式**字段设置为之前创建的格式，如 **BAI2**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-256">Set the **Statement format** field to the format that you created earlier, such as **BAI2**.</span></span>

## <a name="test-the-bank-statement-import"></a><span data-ttu-id="eba0c-257">测试银行对账单导入</span><span class="sxs-lookup"><span data-stu-id="eba0c-257">Test the bank statement import</span></span>
<span data-ttu-id="eba0c-258">最后一步是测试您是否可以导入银行对账单。</span><span class="sxs-lookup"><span data-stu-id="eba0c-258">The final step is to test that you can import your bank statement.</span></span>

1.  <span data-ttu-id="eba0c-259">转**现金和银行管理** &gt; **银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-259">Go to **Cash and bank management** &gt; **Bank accounts**.</span></span>
2.  <span data-ttu-id="eba0c-260">选择为其启用高级银行对帐功能的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="eba0c-260">Select the bank account that Advanced bank reconciliation functionality is enabled for.</span></span>
3.  <span data-ttu-id="eba0c-261">在**对帐**选项卡上，单击**银行对账单**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-261">On the **Reconcile** tab, click **Bank statements**.</span></span>
4.  <span data-ttu-id="eba0c-262">在**银行对账单**页面上，单击**导入对账单**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-262">On the **Bank statement** page, click **Import statement**.</span></span>
5.  <span data-ttu-id="eba0c-263">将**银行帐户**字段设置为所选银行帐户。</span><span class="sxs-lookup"><span data-stu-id="eba0c-263">Set the **Bank account** field to the selected bank account.</span></span> <span data-ttu-id="eba0c-264">**对账单格式**字段会自动设置，根据银行帐户的设置。</span><span class="sxs-lookup"><span data-stu-id="eba0c-264">The **Statement format** field will be set automatically, based on the setting on the bank account.</span></span>
6.  <span data-ttu-id="eba0c-265">单击**浏览**，然后选择您的电子银行对账单文件。</span><span class="sxs-lookup"><span data-stu-id="eba0c-265">Click **Browse**, and select your electronic bank statement file.</span></span>
7.  <span data-ttu-id="eba0c-266">单击**上载**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-266">Click **Upload**.</span></span>
8.  <span data-ttu-id="eba0c-267">单击**OK**。</span><span class="sxs-lookup"><span data-stu-id="eba0c-267">Click **OK**.</span></span>

<span data-ttu-id="eba0c-268">如果导入成功，您将收到一条消息，指出您的对账单被导入。</span><span class="sxs-lookup"><span data-stu-id="eba0c-268">If the import is successful, you will receive a message that states that your statement was imported.</span></span> <span data-ttu-id="eba0c-269">如果导入不成功，在**数据管理**工作区，在**作业历史记录**部分，找到该作业。</span><span class="sxs-lookup"><span data-stu-id="eba0c-269">If the import wasn't successful, in the **Data management** workspace, in the **Job history** section, find the job.</span></span> <span data-ttu-id="eba0c-270">单击作业的**执行详细信息**打开**执行摘要**页，然后单击**查看执行日志**查看导入错误。</span><span class="sxs-lookup"><span data-stu-id="eba0c-270">Click **Execution details** for the job to open the **Execution summary** page, and then click **View execution log** to view the import errors.</span></span>




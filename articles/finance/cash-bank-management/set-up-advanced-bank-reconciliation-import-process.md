---
title: 设置高级银行对帐导入流程
description: 高级银行对帐功能让您可以导入电子银行对帐单，并可以将其与 Microsoft Dynamics 365 Finance 中的银行交易记录自动对帐。 本文介绍如何设置银行对账单的导入功能。
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22d173f6ced2af3e8023bd40f70ca70728c3a0a7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834972"
---
# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a><span data-ttu-id="bde6f-104">设置高级银行对帐导入流程</span><span class="sxs-lookup"><span data-stu-id="bde6f-104">Set up the advanced bank reconciliation import process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bde6f-105">高级银行对帐功能让您可以导入电子银行对帐单，并可以将其与 Dynamics 365 Finance 中的银行交易记录自动对帐。</span><span class="sxs-lookup"><span data-stu-id="bde6f-105">The Advanced bank reconciliation feature lets you import electronic bank statements and automatically reconcile them with bank transactions in Dynamics 365 Finance.</span></span> <span data-ttu-id="bde6f-106">本文介绍如何设置银行对账单的导入功能。</span><span class="sxs-lookup"><span data-stu-id="bde6f-106">This article explains how to set up the import functionality for your bank statements.</span></span> 

<span data-ttu-id="bde6f-107">银行对账单导入设置因您电子银行对账单的格式的不同而不同。</span><span class="sxs-lookup"><span data-stu-id="bde6f-107">The setup for bank statement import varies, depending on the format of your electronic bank statement.</span></span> <span data-ttu-id="bde6f-108">Finance 支持三个现成的银行对账单格式︰ISO20022、MT940 和 BAI2。</span><span class="sxs-lookup"><span data-stu-id="bde6f-108">Finance supports three bank statement formats out of the box: ISO20022, MT940, and BAI2.</span></span>

## <a name="set-time-zone-preference"></a><span data-ttu-id="bde6f-109">设置时区首选项</span><span class="sxs-lookup"><span data-stu-id="bde6f-109">Set time zone preference</span></span>
<span data-ttu-id="bde6f-110">配置银行对帐单导入设置时，务必注意将导入的银行对帐单文件内的日期时间数据的时区。</span><span class="sxs-lookup"><span data-stu-id="bde6f-110">When you configure the bank statement import settings, it can be important to consider the time zone of the date-time data within the bank statement files that will be imported.</span></span> <span data-ttu-id="bde6f-111">默认假设所有日期和时间值均为协调世界时 (UTC)，因此导入数据时不应用时区转换。</span><span class="sxs-lookup"><span data-stu-id="bde6f-111">The default is to assume any date and time values are already in Coordinated Universal Time (UTC) and so no time zone conversion will be applied when you import the data.</span></span> 

<span data-ttu-id="bde6f-112">提供了一个选项，用于指定导入数据时要使用的时区。</span><span class="sxs-lookup"><span data-stu-id="bde6f-112">There is an option available to specify a time zone to use for importing data.</span></span> <span data-ttu-id="bde6f-113">此选项位于每个 **源数据格式详细信息** 页（**数据管理工作区 > 配置数据源 > 选择数据格式 > 区域设置** 快速选项卡）中的 **时区首选项** 字段内。</span><span class="sxs-lookup"><span data-stu-id="bde6f-113">This option is available in the **Time zone preference** field on each **Source data format details** page (**Data management workspace > Configure data sources > Select a data format > Regional settings** FastTab).</span></span> <span data-ttu-id="bde6f-114">您输入的这个时区首选项将应用于所有使用该源数据格式的导入。</span><span class="sxs-lookup"><span data-stu-id="bde6f-114">This time zone preference you enter will apply to all the imports that use that source data format.</span></span> <span data-ttu-id="bde6f-115">可根据从多个时区导入数据的需要创建任意数量的数据源格式。</span><span class="sxs-lookup"><span data-stu-id="bde6f-115">You can create as many data source formats as needed for importing data from multiple time zones.</span></span>  

<span data-ttu-id="bde6f-116">此时区可能与用户或公司的时区不同，因此请务必分辨清楚日期和时间数据正在使用哪个时区。</span><span class="sxs-lookup"><span data-stu-id="bde6f-116">This time zone might not be the same as a user’s or company’s time zone, so be sure to clarify what time zone the date and time data is using.</span></span> <span data-ttu-id="bde6f-117">建议在设置时区首选项时注意以下事项。</span><span class="sxs-lookup"><span data-stu-id="bde6f-117">We recommend that you consider the following points when setting a time zone preference.</span></span> 

 - <span data-ttu-id="bde6f-118">时区首选项将应用于所有使用该源数据格式的导入。</span><span class="sxs-lookup"><span data-stu-id="bde6f-118">The time zone preference will apply to all imports using that source data format.</span></span> <span data-ttu-id="bde6f-119">可根据处理从多个时区导入数据的需要创建任意数量的数据源格式。</span><span class="sxs-lookup"><span data-stu-id="bde6f-119">You can create as many data source formats as needed to handle importing data from multiple time zones.</span></span> 
 
 - <span data-ttu-id="bde6f-120">时区首选项应该是导入文件中的日期和时间数据的本地时区。</span><span class="sxs-lookup"><span data-stu-id="bde6f-120">The time zone preference should be the local time zone of the date and time data in the import file.</span></span> 
 
 - <span data-ttu-id="bde6f-121">日期和时间数据的时区可能与用户或公司的时区不同。</span><span class="sxs-lookup"><span data-stu-id="bde6f-121">The time zone of the date and time data might not be the same as a user’s or company’s time zone.</span></span>
 
 - <span data-ttu-id="bde6f-122">用户可以使用 **用户选项** 调整自己的时区。</span><span class="sxs-lookup"><span data-stu-id="bde6f-122">Users can adjust their own time zone using their **User options**.</span></span>

<span data-ttu-id="bde6f-123">请注意，导入银行对帐单时，以下操作可帮助将潜在的日期和时间冲突降到最少。</span><span class="sxs-lookup"><span data-stu-id="bde6f-123">Note that the following actions can help minimize potential date and time conflicts when you import bank statements.</span></span> 

 - <span data-ttu-id="bde6f-124">避免更改已经导入了对帐单的任何银行帐户的时区首选项。</span><span class="sxs-lookup"><span data-stu-id="bde6f-124">Avoid changing the time zone preferences for any bank accounts that have already had statements imported.</span></span> <span data-ttu-id="bde6f-125">因为时区调整，更改时区首选项可能会影响新对帐单相对现有对帐单的排序。</span><span class="sxs-lookup"><span data-stu-id="bde6f-125">Changing the time zone preference could impact the ordering of new statements relative to existing statements due to the time zone adjustment.</span></span> 
 
 - <span data-ttu-id="bde6f-126">查看所有使用所选数据源格式的导入。</span><span class="sxs-lookup"><span data-stu-id="bde6f-126">Review all the imports that use the selected data source format.</span></span> <span data-ttu-id="bde6f-127">为该格式指定的时区首选项将应用于所有使用该格式的导入项目。</span><span class="sxs-lookup"><span data-stu-id="bde6f-127">The time zone preference specified for the format will apply to all the import projects that use that format.</span></span> <span data-ttu-id="bde6f-128">验证时区首选项适合所有使用该格式的导入项目。</span><span class="sxs-lookup"><span data-stu-id="bde6f-128">Verify that the time zone preference is appropriate for all the import projects that use that format.</span></span>

## <a name="sample-files"></a><span data-ttu-id="bde6f-129">示例文件</span><span class="sxs-lookup"><span data-stu-id="bde6f-129">Sample files</span></span>
<span data-ttu-id="bde6f-130">对于所有三种格式，您必须有将电子银行对帐单的原始格式转换为 Finance 可以使用的格式的文件。</span><span class="sxs-lookup"><span data-stu-id="bde6f-130">For all three formats, you must have files that translate the electronic bank statement from the original format to a format that Finance can use.</span></span> <span data-ttu-id="bde6f-131">您可以在 Microsoft Visual Studio 中应用程序资源管理器的 **资源** 节点下找到所需资源文件。</span><span class="sxs-lookup"><span data-stu-id="bde6f-131">You can find the required resource files under the **Resources** node in Application Explorer in Microsoft Visual Studio.</span></span> <span data-ttu-id="bde6f-132">找到文件后，将它们复制到一个已知位置，以便您可以更轻松地在设置流程中上载它们。</span><span class="sxs-lookup"><span data-stu-id="bde6f-132">After you find the files, copy them to a single known location, so that you can more easily upload them during the setup process.</span></span>

| <span data-ttu-id="bde6f-133">资源名称</span><span class="sxs-lookup"><span data-stu-id="bde6f-133">Resource name</span></span>                                           | <span data-ttu-id="bde6f-134">文件名</span><span class="sxs-lookup"><span data-stu-id="bde6f-134">File name</span></span>                            |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="bde6f-135">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="bde6f-135">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>              | <span data-ttu-id="bde6f-136">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="bde6f-136">BAI2CSV-to-BAI2XML.xslt</span></span>              |
| <span data-ttu-id="bde6f-137">BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="bde6f-137">BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt</span></span>       | <span data-ttu-id="bde6f-138">BAI2XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="bde6f-138">BAI2XML-to-Reconciliation.xslt</span></span>       |
| <span data-ttu-id="bde6f-139">BankStmtImport\_BankReconciliation\_to\_Composite\_xslt</span><span class="sxs-lookup"><span data-stu-id="bde6f-139">BankStmtImport\_BankReconciliation\_to\_Composite\_xslt</span></span> | <span data-ttu-id="bde6f-140">BankReconciliation-to-Composite.xslt</span><span class="sxs-lookup"><span data-stu-id="bde6f-140">BankReconciliation-to-Composite.xslt</span></span> |
| <span data-ttu-id="bde6f-141">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="bde6f-141">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span>   | <span data-ttu-id="bde6f-142">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="bde6f-142">ISO20022XML-to-Reconciliation.xslt</span></span>   |
| <span data-ttu-id="bde6f-143">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="bde6f-143">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>            | <span data-ttu-id="bde6f-144">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="bde6f-144">MT940TXT-to-MT940XML.xslt</span></span>            |
| <span data-ttu-id="bde6f-145">BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="bde6f-145">BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt</span></span>      | <span data-ttu-id="bde6f-146">MT940XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="bde6f-146">MT940XML-to-Reconciliation.xslt</span></span>      |
| <span data-ttu-id="bde6f-147">BankStmtImport\_SampleBankCompositeEntity\_xml</span><span class="sxs-lookup"><span data-stu-id="bde6f-147">BankStmtImport\_SampleBankCompositeEntity\_xml</span></span>          | <span data-ttu-id="bde6f-148">SampleBankCompositeEntity.xml</span><span class="sxs-lookup"><span data-stu-id="bde6f-148">SampleBankCompositeEntity.xml</span></span>        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="bde6f-149">银行对账单格式和技术布局的示例</span><span class="sxs-lookup"><span data-stu-id="bde6f-149">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="bde6f-150">下面是高级银行对帐导入文件技术布局定义的示例和三个相关银行对帐单示例文件：[导入文件示例](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span><span class="sxs-lookup"><span data-stu-id="bde6f-150">Below are examples of the advanced bank reconciliation import file technical layout definitions and three related bank statement example files: [Import file examples](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span></span>  

| <span data-ttu-id="bde6f-151">技术布局定义</span><span class="sxs-lookup"><span data-stu-id="bde6f-151">Technical layout definition</span></span>                             | <span data-ttu-id="bde6f-152">银行对账单示例文件</span><span class="sxs-lookup"><span data-stu-id="bde6f-152">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="bde6f-153">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="bde6f-153">DynamicsAXMT940Layout</span></span>                                   | [<span data-ttu-id="bde6f-154">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="bde6f-154">MT940StatementExample</span></span>](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| <span data-ttu-id="bde6f-155">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="bde6f-155">DynamicsAXISO20022Layout</span></span>                                | [<span data-ttu-id="bde6f-156">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="bde6f-156">ISO20022StatementExample</span></span>](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| <span data-ttu-id="bde6f-157">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="bde6f-157">DynamicsAXBAI2Layout</span></span>                                    | [<span data-ttu-id="bde6f-158">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="bde6f-158">BAI2StatementExample</span></span>](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |



## <a name="set-up-the-import-of-iso20022-bank-statements"></a><span data-ttu-id="bde6f-159">设置 ISO20022 银行对账单的导入</span><span class="sxs-lookup"><span data-stu-id="bde6f-159">Set up the import of ISO20022 bank statements</span></span>
<span data-ttu-id="bde6f-160">首先，您必须通过使用数据实体框架定义 ISO20022 银行对账单的银行对账单格式处理组。</span><span class="sxs-lookup"><span data-stu-id="bde6f-160">First, you must define the bank statement format processing group for ISO20022 bank statements by using the data entity framework.</span></span>

1.  <span data-ttu-id="bde6f-161">转到 **工作区** &gt; **数据管理**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-161">Go to **Workspaces** &gt; **Data management**.</span></span>
2.  <span data-ttu-id="bde6f-162">单击 **导入**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-162">Click **Import**.</span></span>
3.  <span data-ttu-id="bde6f-163">为格式输入名称，如 **ISO20022**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-163">Enter a name for the format, such as **ISO20022**.</span></span>
4.  <span data-ttu-id="bde6f-164">将 **源数据格式** 字段设置为 **XML-元素**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-164">Set the **Source data format** field to **XML-Element**.</span></span>
5.  <span data-ttu-id="bde6f-165">将 **实体名称** 字段设置为 **银行对账单**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-165">Set the **Entity name** field to **Bank statements**.</span></span>
6.  <span data-ttu-id="bde6f-166">若要上载导入文件，请单击 **上载**，然后浏览以选择以前保存的 **SampleBankCompositeEntity.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="bde6f-166">To upload the import files, click **Upload**, and then browse to select the **SampleBankCompositeEntity.xml** file that you saved earlier.</span></span>
7.  <span data-ttu-id="bde6f-167">银行对账单实体上载且映射完成后，请单击实体的 **查看地图** 操作。</span><span class="sxs-lookup"><span data-stu-id="bde6f-167">After the Bank statements entity is uploaded and the mapping is completed, click the **View map** action for the entity.</span></span>
8.  <span data-ttu-id="bde6f-168">银行对账单实体是由四个单独的实体组成一个复合实体。</span><span class="sxs-lookup"><span data-stu-id="bde6f-168">The Bank statements entity is a composite entity that consists of four separate entities.</span></span> <span data-ttu-id="bde6f-169">在列表中，选择 **BankStatementDocumentEntity**，然后单击 **查看地图** 操作。</span><span class="sxs-lookup"><span data-stu-id="bde6f-169">In the list, select **BankStatementDocumentEntity**, and then click the **View map** action.</span></span>
9.  <span data-ttu-id="bde6f-170">在 **转换** 选项卡上，单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-170">On the **Transformations** tab, click **New**.</span></span>
10. <span data-ttu-id="bde6f-171">对于序列号 1，请单击 **上载文件**，并选择以前保存的 **ISO20022XML-to-Reconciliation.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="bde6f-171">For sequence number 1, click **Upload file**, and select the **ISO20022XML-to-Reconciliation.xslt** file that you saved earlier.</span></span> <span data-ttu-id="bde6f-172">**注意︰** 转换文件使用标准格式构建。</span><span class="sxs-lookup"><span data-stu-id="bde6f-172">**Note:** Transformation files are built for the standard format.</span></span> <span data-ttu-id="bde6f-173">因为银行经常偏离这种格式，您可能必须更新要映射到您的银行帐单格式的转换文件。</span><span class="sxs-lookup"><span data-stu-id="bde6f-173">Because banks often diverge from this format, you may have to update the transformation file to map to your bank statement format.</span></span> <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. <span data-ttu-id="bde6f-174">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-174">Click **New**.</span></span>
12. <span data-ttu-id="bde6f-175">对于序列号 2，请单击 **上载文件**，并选择以前保存的 **BankReconciliation-to-Composite.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="bde6f-175">For sequence number 2, click **Upload file**, and select the **BankReconciliation-to-Composite.xslt** file that you saved earlier.</span></span>
13. <span data-ttu-id="bde6f-176">单击 **应用转换**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-176">Click **Apply transforms**.</span></span>

<span data-ttu-id="bde6f-177">设置格式处理组后，下一步是定义 ISO20022 银行对账单的银行对账单格式规则。</span><span class="sxs-lookup"><span data-stu-id="bde6f-177">After the format processing group is set up, the next step is to define the bank statement format rules for ISO20022 bank statements.</span></span>

1.  <span data-ttu-id="bde6f-178">转到 **现金和银行管理** &gt; **设置** &gt; **高级银行对帐设置** &gt; **银行对账单格式**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-178">Go to **Cash and bank management** &gt; **Setup** &gt; **Advanced bank reconciliation setup** &gt; **Bank statement format**.</span></span>
2.  <span data-ttu-id="bde6f-179">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-179">Click **New**.</span></span>
3.  <span data-ttu-id="bde6f-180">指定对账单格式，如 **ISO20022**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-180">Specify a statement format, such as **ISO20022**.</span></span>
4.  <span data-ttu-id="bde6f-181">输入格式名称。</span><span class="sxs-lookup"><span data-stu-id="bde6f-181">Enter a name for the format.</span></span>
5.  <span data-ttu-id="bde6f-182">将 **处理组** 字段设置为之前定义的组，如 **ISO20022**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-182">Set the **Processing group** field to the group that you defined earlier, such as **ISO20022**.</span></span>
6.  <span data-ttu-id="bde6f-183">选中 **XML 文件** 复选框。</span><span class="sxs-lookup"><span data-stu-id="bde6f-183">Select the **XML file** check box.</span></span>

<span data-ttu-id="bde6f-184">最后一步是启用高级银行对帐并设置银行帐户的对账单格式。</span><span class="sxs-lookup"><span data-stu-id="bde6f-184">The last step is to enable Advanced bank reconciliation and set the statement format on the bank account.</span></span>

1.  <span data-ttu-id="bde6f-185">转 **现金和银行管理** &gt; **银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-185">Go to **Cash and bank management** &gt; **Bank accounts**.</span></span>
2.  <span data-ttu-id="bde6f-186">选择银行帐户并打开帐户以查看详细信息。</span><span class="sxs-lookup"><span data-stu-id="bde6f-186">Select the bank account, and open it to view the details.</span></span>
3.  <span data-ttu-id="bde6f-187">在 **对帐** 选项卡上，设置 **高级银行对帐** 选项为 **是**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-187">On the **Reconciliation** tab, set the **Advanced bank reconciliation** option to **Yes**.</span></span>
4.  <span data-ttu-id="bde6f-188">将 **对账单格式** 字段设置为之前创建的格式，如 **ISO20022**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-188">Set the **Statement format** field to the format that you created earlier, such as **ISO20022**.</span></span>

## <a name="set-up-the-import-of-mt940-bank-statements"></a><span data-ttu-id="bde6f-189">设置 MT940 银行对账单的导入</span><span class="sxs-lookup"><span data-stu-id="bde6f-189">Set up the import of MT940 bank statements</span></span>
<span data-ttu-id="bde6f-190">首先，您必须通过使用数据实体框架定义 MT940 银行对账单的银行对账单格式处理组。</span><span class="sxs-lookup"><span data-stu-id="bde6f-190">First, you must define the bank statement format processing group for MT940 bank statements by using the data entity framework.</span></span>

1.  <span data-ttu-id="bde6f-191">转到 **工作区** &gt; **数据管理**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-191">Go to **Workspaces** &gt; **Data management**.</span></span>
2.  <span data-ttu-id="bde6f-192">单击 **导入**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-192">Click **Import**.</span></span>
3.  <span data-ttu-id="bde6f-193">为格式输入名称，如 **MT940**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-193">Enter a name for the format, such as **MT940**.</span></span>
4.  <span data-ttu-id="bde6f-194">将 **源数据格式** 字段设置为 **XML-元素**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-194">Set the **Source data format** field to **XML-Element**.</span></span>
5.  <span data-ttu-id="bde6f-195">将 **实体名称** 字段设置为 **银行对账单**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-195">Set the **Entity name** field to **Bank statements**.</span></span>
6.  <span data-ttu-id="bde6f-196">若要上载导入文件，请单击 **上载**，然后浏览以选择以前保存的 **SampleBankCompositeEntity.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="bde6f-196">To upload import files, click **Upload**, and then browse to select the **SampleBankCompositeEntity.xml** file that you saved earlier.</span></span>
7.  <span data-ttu-id="bde6f-197">银行对账单实体上载且映射完成后，请单击实体的 **查看地图** 操作。</span><span class="sxs-lookup"><span data-stu-id="bde6f-197">After the Bank statements entity is uploaded and the mapping is completed, click the **View map** action for the entity.</span></span>
8.  <span data-ttu-id="bde6f-198">银行对账单实体是由四个单独的实体组成一个复合实体。</span><span class="sxs-lookup"><span data-stu-id="bde6f-198">The Bank statements entity is a composite entity that consists of four separate entities.</span></span> <span data-ttu-id="bde6f-199">在列表中，选择 **BankStatementDocumentEntity**，然后单击 **查看地图** 操作。</span><span class="sxs-lookup"><span data-stu-id="bde6f-199">In the list, select **BankStatementDocumentEntity**, and then click the **View map** action.</span></span>
9.  <span data-ttu-id="bde6f-200">在 **转换** 选项卡上，单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-200">On the **Transformations** tab, click **New**.</span></span>
10. <span data-ttu-id="bde6f-201">对于序列号 1，请单击 **上载文件**，并选择以前保存的 **MT940TXT-to-MT940XML.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="bde6f-201">For sequence number 1, click **Upload file**, and select the **MT940TXT-to-MT940XML.xslt** file that you saved earlier.</span></span>
11. <span data-ttu-id="bde6f-202">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-202">Click **New**.</span></span>
12. <span data-ttu-id="bde6f-203">对于序列号 2，请单击 **上载文件**，并选择以前保存的 **MT940XML-to-Reconciliation.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="bde6f-203">For sequence number 2, click **Upload file**, and select the **MT940XML-to-Reconciliation.xslt** file that you saved earlier.</span></span> <span data-ttu-id="bde6f-204">**注意︰** 转换文件使用标准格式构建。</span><span class="sxs-lookup"><span data-stu-id="bde6f-204">**Note:** Transformation files are built for the standard format.</span></span> <span data-ttu-id="bde6f-205">因为银行经常偏离这种格式，您可能必须更新要映射到您的银行帐单格式的转换文件。</span><span class="sxs-lookup"><span data-stu-id="bde6f-205">Because banks often diverge from this format, you may have to update the transformation file to map to your bank statement format.</span></span> <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. <span data-ttu-id="bde6f-206">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-206">Click **New**.</span></span>
14. <span data-ttu-id="bde6f-207">对于序列号 3，请单击 **上载文件**，并选择以前保存的 **BankReconciliation-to-Composite.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="bde6f-207">For sequence number 3, click **Upload file**, and select the **BankReconciliation-to-Composite.xslt** file that you saved earlier.</span></span>
15. <span data-ttu-id="bde6f-208">单击 **应用转换**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-208">Click **Apply transforms**.</span></span>

<span data-ttu-id="bde6f-209">设置格式处理组后，下一步是定义 MT940 银行对账单的银行对账单格式规则。</span><span class="sxs-lookup"><span data-stu-id="bde6f-209">After the format processing group is set up, the next step is to define the bank statement format rules for MT940 bank statements.</span></span>

1.  <span data-ttu-id="bde6f-210">转到 **现金和银行管理** &gt; **设置** &gt; **高级银行对帐设置** &gt; **银行对账单格式**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-210">Go to **Cash and bank management** &gt; **Setup** &gt; **Advanced bank reconciliation setup** &gt; **Bank statement format**.</span></span>
2.  <span data-ttu-id="bde6f-211">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-211">Click **New**.</span></span>
3.  <span data-ttu-id="bde6f-212">指定对账单格式，如 **MT940**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-212">Specify a statement format, such as **MT940**.</span></span>
4.  <span data-ttu-id="bde6f-213">输入格式名称。</span><span class="sxs-lookup"><span data-stu-id="bde6f-213">Enter a name for the format.</span></span>
5.  <span data-ttu-id="bde6f-214">将 **处理组** 字段设置为之前定义的组，如 **MT940**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-214">Set the **Processing group** field to the group that you defined earlier, such as **MT940**.</span></span>
6.  <span data-ttu-id="bde6f-215">将 **文件类型** 字段设置为 **txt**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-215">Set the **File type** field to **txt**.</span></span>

<span data-ttu-id="bde6f-216">最后一步是启用高级银行对帐并设置银行帐户的对账单格式。</span><span class="sxs-lookup"><span data-stu-id="bde6f-216">The last step is to enable Advanced bank reconciliation and set the statement format on the bank account.</span></span>

1.  <span data-ttu-id="bde6f-217">转 **现金和银行管理** &gt; **银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-217">Go to **Cash and bank management** &gt; **Bank accounts**.</span></span>
2.  <span data-ttu-id="bde6f-218">选择银行帐户并打开帐户以查看详细信息。</span><span class="sxs-lookup"><span data-stu-id="bde6f-218">Select the bank account, and open it to view the details.</span></span>
3.  <span data-ttu-id="bde6f-219">在 **对帐** 选项卡上，设置 **高级银行对帐** 选项为 **是**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-219">On the **Reconciliation** tab, set the **Advanced bank reconciliation** option to **Yes**.</span></span>
4.  <span data-ttu-id="bde6f-220">当提示您确认您的选择并启用高级银行对帐时，请单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-220">When you're prompted to confirm your selection and enable Advanced bank reconciliation, click **OK**.</span></span>
5.  <span data-ttu-id="bde6f-221">将 **对账单格式** 字段设置为之前创建的格式，如 **MT940**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-221">Set the **Statement format** field to the format that you created earlier, such as **MT940**.</span></span>

## <a name="set-up-the-import-of-bai2-bank-statements"></a><span data-ttu-id="bde6f-222">设置 BAI2 银行对账单的导入</span><span class="sxs-lookup"><span data-stu-id="bde6f-222">Set up the import of BAI2 bank statements</span></span>
<span data-ttu-id="bde6f-223">首先，您必须通过使用数据实体框架定义 BAI2 银行对账单的银行对账单格式处理组。</span><span class="sxs-lookup"><span data-stu-id="bde6f-223">First, you must define the bank statement format processing group for BAI2 bank statements by using the data entity framework.</span></span>

1.  <span data-ttu-id="bde6f-224">转到 **工作区** &gt; **数据管理**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-224">Go to **Workspaces** &gt; **Data management**.</span></span>
2.  <span data-ttu-id="bde6f-225">单击 **导入**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-225">Click **Import**.</span></span>
3.  <span data-ttu-id="bde6f-226">为格式输入名称，如 **BAI2**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-226">Enter a name for the format, such as **BAI2**.</span></span>
4.  <span data-ttu-id="bde6f-227">将 **源数据格式** 字段设置为 **XML-元素**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-227">Set the **Source data format** field to **XML-Element**.</span></span>
5.  <span data-ttu-id="bde6f-228">将 **实体名称** 字段设置为 **银行对账单**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-228">Set the **Entity name** field to **Bank statements**.</span></span>
6.  <span data-ttu-id="bde6f-229">若要上载导入文件，请单击 **上载**，然后浏览以选择以前保存的 **SampleBankCompositeEntity.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="bde6f-229">To upload import files, click **Upload**, and then browse to select the **SampleBankCompositeEntity.xml** file that you saved earlier.</span></span>
7.  <span data-ttu-id="bde6f-230">银行对账单实体上载且映射完成后，请单击实体的 **查看地图** 操作。</span><span class="sxs-lookup"><span data-stu-id="bde6f-230">After the Bank statements entity is uploaded and the mapping is completed, click the **View map** action for the entity.</span></span>
8.  <span data-ttu-id="bde6f-231">银行对账单实体是由四个单独的实体组成一个复合实体。</span><span class="sxs-lookup"><span data-stu-id="bde6f-231">The Bank statements entity is a composite entity that consists of four separate entities.</span></span> <span data-ttu-id="bde6f-232">在列表中，选择 **BankStatementDocumentEntity**，然后单击 **查看地图** 操作。</span><span class="sxs-lookup"><span data-stu-id="bde6f-232">In the list, select **BankStatementDocumentEntity**, and then click the **View map** action.</span></span>
9.  <span data-ttu-id="bde6f-233">在 **转换** 选项卡上，单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-233">On the **Transformations** tab, click **New**.</span></span>
10. <span data-ttu-id="bde6f-234">对于序列号 1，请单击 **上载文件**，并选择以前保存的 **BAI2CSV-to-BAI2XML.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="bde6f-234">For sequence number 1, click **Upload file**, and select the **BAI2CSV-to-BAI2XML.xslt** file that you saved earlier.</span></span>
11. <span data-ttu-id="bde6f-235">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-235">Click **New**.</span></span>
12. <span data-ttu-id="bde6f-236">对于序列号 2，请单击 **上载文件**，并选择以前保存的 **BAI2XML-to-Reconciliation.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="bde6f-236">For sequence number 2, click **Upload file**, and select the **BAI2XML-to-Reconciliation.xslt** file that you saved earlier.</span></span> <span data-ttu-id="bde6f-237">**注意︰** 转换文件使用标准格式构建。</span><span class="sxs-lookup"><span data-stu-id="bde6f-237">**Note:** Transformation files are built for the standard format.</span></span> <span data-ttu-id="bde6f-238">因为银行经常偏离这种格式，您可能必须更新要映射到您的银行帐单格式的转换文件。</span><span class="sxs-lookup"><span data-stu-id="bde6f-238">Because banks often diverge from this format, and you may have to update the transformation file to map to your bank statement format.</span></span> <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. <span data-ttu-id="bde6f-239">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-239">Click **New**.</span></span>
14. <span data-ttu-id="bde6f-240">对于序列号 3，请单击 **上载文件**，并选择以前保存的 **BankReconciliation-to-Composite.xslt** 文件。</span><span class="sxs-lookup"><span data-stu-id="bde6f-240">For sequence number 3, click **Upload file**, and select the **BankReconciliation-to-Composite.xslt** file that you saved earlier.</span></span>
15. <span data-ttu-id="bde6f-241">单击 **应用转换**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-241">Click **Apply transforms**.</span></span>

<span data-ttu-id="bde6f-242">设置格式处理组后，下一步是定义 BAI2 银行对账单的银行对账单格式规则。</span><span class="sxs-lookup"><span data-stu-id="bde6f-242">After the format processing group is set up, the next step is to define the bank statement format rules for BAI2 bank statements.</span></span>

1.  <span data-ttu-id="bde6f-243">转到 **现金和银行管理** &gt; **设置** &gt; **高级银行对帐设置** &gt; **银行对账单格式**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-243">Go to **Cash and bank management** &gt; **Setup** &gt; **Advanced bank reconciliation setup** &gt; **Bank statement format**.</span></span>
2.  <span data-ttu-id="bde6f-244">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-244">Click **New**.</span></span>
3.  <span data-ttu-id="bde6f-245">指定对账单格式，如 **BAI2**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-245">Specify a statement format, such as **BAI2**.</span></span>
4.  <span data-ttu-id="bde6f-246">输入格式名称。</span><span class="sxs-lookup"><span data-stu-id="bde6f-246">Enter a name for the format.</span></span>
5.  <span data-ttu-id="bde6f-247">将 **处理组** 字段设置为之前定义的组，如 **BAI2**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-247">Set the **Processing group** field to the group that you defined earlier, such as **BAI2**.</span></span>
6.  <span data-ttu-id="bde6f-248">将 **文件类型** 字段设置为 **txt**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-248">Set the **File type** field to **txt**.</span></span>

<span data-ttu-id="bde6f-249">最后一步是启用高级银行对帐并设置银行帐户的对账单格式。</span><span class="sxs-lookup"><span data-stu-id="bde6f-249">The last step is to enable Advanced bank reconciliation and set the statement format on the bank account.</span></span>

1.  <span data-ttu-id="bde6f-250">转 **现金和银行管理** &gt; **银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-250">Go to **Cash and bank management** &gt; **Bank accounts**.</span></span>
2.  <span data-ttu-id="bde6f-251">选择银行帐户并打开帐户以查看详细信息。</span><span class="sxs-lookup"><span data-stu-id="bde6f-251">Select the bank account, and open it to view the details.</span></span>
3.  <span data-ttu-id="bde6f-252">在 **对帐** 选项卡上，设置 **高级银行对帐** 选项为 **是**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-252">On the **Reconciliation** tab, set the **Advanced bank reconciliation** option to **Yes**.</span></span>
4.  <span data-ttu-id="bde6f-253">当提示您确认您的选择并启用高级银行对帐时，请单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-253">When you're prompted to confirm your selection and enable Advanced bank reconciliation, click **OK**.</span></span>
5.  <span data-ttu-id="bde6f-254">将 **对账单格式** 字段设置为之前创建的格式，如 **BAI2**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-254">Set the **Statement format** field to the format that you created earlier, such as **BAI2**.</span></span>

## <a name="test-the-bank-statement-import"></a><span data-ttu-id="bde6f-255">测试银行对账单导入</span><span class="sxs-lookup"><span data-stu-id="bde6f-255">Test the bank statement import</span></span>
<span data-ttu-id="bde6f-256">最后一步是测试您是否可以导入银行对账单。</span><span class="sxs-lookup"><span data-stu-id="bde6f-256">The final step is to test that you can import your bank statement.</span></span>

1.  <span data-ttu-id="bde6f-257">转 **现金和银行管理** &gt; **银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-257">Go to **Cash and bank management** &gt; **Bank accounts**.</span></span>
2.  <span data-ttu-id="bde6f-258">选择为其启用高级银行对帐功能的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="bde6f-258">Select the bank account that Advanced bank reconciliation functionality is enabled for.</span></span>
3.  <span data-ttu-id="bde6f-259">在 **对帐** 选项卡上，单击 **银行对账单**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-259">On the **Reconcile** tab, click **Bank statements**.</span></span>
4.  <span data-ttu-id="bde6f-260">在 **银行对账单** 页面上，单击 **导入对账单**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-260">On the **Bank statement** page, click **Import statement**.</span></span>
5.  <span data-ttu-id="bde6f-261">将 **银行帐户** 字段设置为所选银行帐户。</span><span class="sxs-lookup"><span data-stu-id="bde6f-261">Set the **Bank account** field to the selected bank account.</span></span> <span data-ttu-id="bde6f-262">**对账单格式** 字段会自动设置，根据银行帐户的设置。</span><span class="sxs-lookup"><span data-stu-id="bde6f-262">The **Statement format** field will be set automatically, based on the setting on the bank account.</span></span>
6.  <span data-ttu-id="bde6f-263">单击 **浏览**，然后选择您的电子银行对账单文件。</span><span class="sxs-lookup"><span data-stu-id="bde6f-263">Click **Browse**, and select your electronic bank statement file.</span></span>
7.  <span data-ttu-id="bde6f-264">单击 **上载**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-264">Click **Upload**.</span></span>
8.  <span data-ttu-id="bde6f-265">单击 **OK**。</span><span class="sxs-lookup"><span data-stu-id="bde6f-265">Click **OK**.</span></span>

<span data-ttu-id="bde6f-266">如果导入成功，您将收到一条消息，指出您的对账单被导入。</span><span class="sxs-lookup"><span data-stu-id="bde6f-266">If the import is successful, you will receive a message that states that your statement was imported.</span></span> <span data-ttu-id="bde6f-267">如果导入不成功，在 **数据管理** 工作区，在 **作业历史记录** 部分，找到该作业。</span><span class="sxs-lookup"><span data-stu-id="bde6f-267">If the import wasn't successful, in the **Data management** workspace, in the **Job history** section, find the job.</span></span> <span data-ttu-id="bde6f-268">单击作业的 **执行详细信息** 打开 **执行摘要** 页，然后单击 **查看执行日志** 查看导入错误。</span><span class="sxs-lookup"><span data-stu-id="bde6f-268">Click **Execution details** for the job to open the **Execution summary** page, and then click **View execution log** to view the import errors.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

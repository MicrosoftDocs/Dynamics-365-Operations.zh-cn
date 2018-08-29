---
title: "配置从 SharePoint 的数据导入"
description: "本主题介绍如何从 Microsoft SharePoint 导入数据。"
author: NickSelin
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 4285db9c71208bce45d64933e692a25ef3f46b26
ms.contentlocale: zh-cn
ms.lasthandoff: 08/08/2018

---
# <a name="configure-data-import-from-sharepoint"></a><span data-ttu-id="5f964-103">配置从 SharePoint 的数据导入</span><span class="sxs-lookup"><span data-stu-id="5f964-103">Configure data import from SharePoint</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5f964-104">若要使用电子申报 (ER) 框架从传入文件导入数据，必须配置用于为导入提供支持的 ER 格式，然后运行将该格式用作数据源且类型为**截止目标**的模型映射。</span><span class="sxs-lookup"><span data-stu-id="5f964-104">To import data from an incoming file by using the Electronic reporting (ER) framework, you must configure an ER format that supports the import and then run a model mapping of the **To destination** type that uses that format as a data source.</span></span> <span data-ttu-id="5f964-105">若要导入数据，您必须导航到要导入的文件。</span><span class="sxs-lookup"><span data-stu-id="5f964-105">To import data, you must navigate to the file that you want to import.</span></span> <span data-ttu-id="5f964-106">用户可以手动选择传入文件。</span><span class="sxs-lookup"><span data-stu-id="5f964-106">The incoming file can be manually selected by user.</span></span> <span data-ttu-id="5f964-107">在新的 ER 功能中，为了为从 Microsoft SharePoint 导入数据提供支持，可将此过程配置为无人值守过程。</span><span class="sxs-lookup"><span data-stu-id="5f964-107">With the new ER capability to support importing data from Microsoft SharePoint, this process can be configured as the unattended one.</span></span> <span data-ttu-id="5f964-108">您可以使用 ER 配置从 Microsoft SharePoint 文件夹中存储的文件导入数据。</span><span class="sxs-lookup"><span data-stu-id="5f964-108">You can use ER configurations to perform data import from files that are stored in Microsoft SharePoint folders.</span></span> <span data-ttu-id="5f964-109">本主题介绍如何完成导入从 SharePoint 到 Microsoft Dynamics 365 for Finance and Operations 的导入。</span><span class="sxs-lookup"><span data-stu-id="5f964-109">This topic explains how to complete the import from SharePoint to Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="5f964-110">示例将供应商交易记录用作业务数据。</span><span class="sxs-lookup"><span data-stu-id="5f964-110">The examples use vendor transactions as business data.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5f964-111">必备项</span><span class="sxs-lookup"><span data-stu-id="5f964-111">Prerequisites</span></span>
<span data-ttu-id="5f964-112">要完成本主题中的示例，您必须具有以下访问权限：</span><span class="sxs-lookup"><span data-stu-id="5f964-112">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="5f964-113">访问 Finance and Operations 的以下其中一个角色：</span><span class="sxs-lookup"><span data-stu-id="5f964-113">Access to Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="5f964-114">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="5f964-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="5f964-115">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="5f964-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="5f964-116">系统管理员</span><span class="sxs-lookup"><span data-stu-id="5f964-116">System administrator</span></span>

- <span data-ttu-id="5f964-117">已针对与 Finance and Operations 配合使用配置了 Microsoft SharePoint Server 实例的访问权限。</span><span class="sxs-lookup"><span data-stu-id="5f964-117">Access to the instance of Microsoft SharePoint Server that is configured for use with Finance and Operations</span></span>
- <span data-ttu-id="5f964-118">1099 付款的 ER 格式和模型配置</span><span class="sxs-lookup"><span data-stu-id="5f964-118">ER format and model configurations for 1099 payments</span></span>

### <a name="create-required-er-configurations"></a><span data-ttu-id="5f964-119">创建所需的 ER 配置</span><span class="sxs-lookup"><span data-stu-id="5f964-119">Create required ER configurations</span></span>
<span data-ttu-id="5f964-120">播放 **ER 从 Microsoft Excel 文件导入数据**任务指南，该任务指南属于 **7.5.4.3 获取/开发 IT 服务/解决方案产品 (10677)** 业务流程。.</span><span class="sxs-lookup"><span data-stu-id="5f964-120">Play the **ER Import data from a Microsoft Excel file** task guides, which are part of the **7.5.4.3 Acquire/Develop IT service/solution components (10677)** business process.</span></span> <span data-ttu-id="5f964-121">这些任务指南将引导您完成设计和使用 ER 配置以便以交互方式从外部 Microsoft Excel 文件导入供应商交易记录这一过程。</span><span class="sxs-lookup"><span data-stu-id="5f964-121">These task guides walk you through the process of designing and using ER configurations to interactively import vendor transactions from external Microsoft Excel files.</span></span> <span data-ttu-id="5f964-122">有关详细信息，请参阅[分析 Microsoft Excel 格式的传入文档](parse-incoming-documents-excel.md)。</span><span class="sxs-lookup"><span data-stu-id="5f964-122">For more information, see [Parse incoming documents in Microsoft Excel](parse-incoming-documents-excel.md).</span></span> <span data-ttu-id="5f964-123">最后，您将获得：</span><span class="sxs-lookup"><span data-stu-id="5f964-123">Fianlly, you will have:</span></span>

- <span data-ttu-id="5f964-124">ER 配置：</span><span class="sxs-lookup"><span data-stu-id="5f964-124">ER configurations:</span></span>

    - <span data-ttu-id="5f964-125">ER 模型配置 **1099 付款模型**</span><span class="sxs-lookup"><span data-stu-id="5f964-125">ER model configuration, **1099 Payments model**</span></span>
    - <span data-ttu-id="5f964-126">ER 格式配置**用于从 Excel 导入供应商的交易记录的格式**</span><span class="sxs-lookup"><span data-stu-id="5f964-126">ER format configuration, **Format for importing vendors' transactions from Excel**</span></span>

<span data-ttu-id="5f964-127">[![用于从 SharePoint 导入数据的 ER 配置](./media/GERImportFromSharePoint-01-Configurations.PNG)](./media/GERImportFromSharePoint-01-Configurations.PNG)</span><span class="sxs-lookup"><span data-stu-id="5f964-127">[![ER configurations for importing data from SharePoint](./media/GERImportFromSharePoint-01-Configurations.PNG)](./media/GERImportFromSharePoint-01-Configurations.PNG)</span></span>

- <span data-ttu-id="5f964-128">用于数据导入的传入文件示例：</span><span class="sxs-lookup"><span data-stu-id="5f964-128">Sample of the incoming file for data import:</span></span>

    - <span data-ttu-id="5f964-129">Excel 文件 **1099import-data.xlsx**，其中包含应导入 Finance and Operations 的供应商交易记录</span><span class="sxs-lookup"><span data-stu-id="5f964-129">Excel file **1099import-data.xlsx**, with vendor transactions that should be imported into Finance and Operations</span></span>

<span data-ttu-id="5f964-130">[![要从 SharePoint 导入的 Microsoft Excel 示例文件](./media/GERImportFromSharePoint-02-Excel.PNG)](./media/GERImportFromSharePoint-02-Excel.PNG)</span><span class="sxs-lookup"><span data-stu-id="5f964-130">[![Sample Microsoft Excel file for importing from SharePoint](./media/GERImportFromSharePoint-02-Excel.PNG)](./media/GERImportFromSharePoint-02-Excel.PNG)</span></span>

> [!NOTE]
> <span data-ttu-id="5f964-131">将选择用于导入供应商交易记录的格式作为默认模型映射。</span><span class="sxs-lookup"><span data-stu-id="5f964-131">The format for importing vendor transactions is selected as the default model mapping.</span></span> <span data-ttu-id="5f964-132">因此，如果运行 **1099 付款模型**的模型映射，并且该模型映射类型为**截止目标**，则该模型映射运行此格式以从外部文件导入数据。</span><span class="sxs-lookup"><span data-stu-id="5f964-132">Therefore, if you run a model mapping of the **1099 Payments model**, and that model mapping is of the **To destination** type, the model mapping runs this format to import data from external files.</span></span> <span data-ttu-id="5f964-133">然后使用这些数据更新申请表。</span><span class="sxs-lookup"><span data-stu-id="5f964-133">It then uses that data to update application tables.</span></span>

## <a name="configure-document-management-parameters"></a><span data-ttu-id="5f964-134">配置文档管理参数</span><span class="sxs-lookup"><span data-stu-id="5f964-134">Configure Document management parameters</span></span>
1. <span data-ttu-id="5f964-135">在**文档管理参数**页面上，配置您登录的公司中使用的 SharePoint Server 实例访问权限。</span><span class="sxs-lookup"><span data-stu-id="5f964-135">On the **Document management parameters** page, configure access to the SharePoint Server instance that will be used by the company that you're currently signed in to.</span></span> <span data-ttu-id="5f964-136">在此示例中，该公司为 USMF。</span><span class="sxs-lookup"><span data-stu-id="5f964-136">In this example, the company is USMF.</span></span>
2. <span data-ttu-id="5f964-137">测试与 SharePoint Server 实例的连接性，确保您已被授予访问权限。</span><span class="sxs-lookup"><span data-stu-id="5f964-137">Test the connection to the SharePoint Server instance to make sure that you've been granted access.</span></span>

<span data-ttu-id="5f964-138">[![文档管理设置 – SharePoint 服务器](./media/GERImportFromSharePoint-03-SharePointSetup.png)](./media/GERImportFromSharePoint-03-SharePointSetup.png)</span><span class="sxs-lookup"><span data-stu-id="5f964-138">[![Document management setting – SharePoint server](./media/GERImportFromSharePoint-03-SharePointSetup.png)](./media/GERImportFromSharePoint-03-SharePointSetup.png)</span></span>

3. <span data-ttu-id="5f964-139">打开配置的 SharePoint 站点，然后创建以下文件夹，用于存储传入的文件：</span><span class="sxs-lookup"><span data-stu-id="5f964-139">Open the configured SharePoint site, and create the following folders where the incoming files can be stored:</span></span>

    - <span data-ttu-id="5f964-140">文件导入源（主）</span><span class="sxs-lookup"><span data-stu-id="5f964-140">Files import source (main)</span></span>
    - <span data-ttu-id="5f964-141">文件导入源（备用）</span><span class="sxs-lookup"><span data-stu-id="5f964-141">Files import source (alternative)</span></span>

<span data-ttu-id="5f964-142">[![文档管理设置 – SharePoint 服务器](./media/GERImportFromSharePoint-04-SharePointFolder1.png)](./media/GERImportFromSharePoint-04-SharePointFolder1.png)</span><span class="sxs-lookup"><span data-stu-id="5f964-142">[![Document management setting – SharePoint server](./media/GERImportFromSharePoint-04-SharePointFolder1.png)](./media/GERImportFromSharePoint-04-SharePointFolder1.png)</span></span>

<span data-ttu-id="5f964-143">[![文档管理设置 – SharePoint 服务器](./media/GERImportFromSharePoint-05-SharePointFolder2.png)](./media/GERImportFromSharePoint-05-SharePointFolder2.png)</span><span class="sxs-lookup"><span data-stu-id="5f964-143">[![Document management setting – SharePoint server](./media/GERImportFromSharePoint-05-SharePointFolder2.png)](./media/GERImportFromSharePoint-05-SharePointFolder2.png)</span></span>

4. <span data-ttu-id="5f964-144">在 Finance and Operations 中的**文档类型**页面上创建将用来访问您刚才创建的 SharePoint 文件夹的以下文档类型：</span><span class="sxs-lookup"><span data-stu-id="5f964-144">In Finance and Operations, on the **Document types** page, create the following document types that will be used to access the SharePoint folders that you just created:</span></span>

    - <span data-ttu-id="5f964-145">SP 主</span><span class="sxs-lookup"><span data-stu-id="5f964-145">SP Main</span></span>
    - <span data-ttu-id="5f964-146">SP 备用</span><span class="sxs-lookup"><span data-stu-id="5f964-146">SP Alternative</span></span>

5. <span data-ttu-id="5f964-147">对于创建的文档类型，在**组**字段中输入**文件**，在**位置**字段中输入 **SharePoint**。</span><span class="sxs-lookup"><span data-stu-id="5f964-147">For created document types, in the **Group** field, enter **File** and in the **Location** field, enter **SharePoint**.</span></span> <span data-ttu-id="5f964-148">然后输入 SharePoint 文件夹的地址：</span><span class="sxs-lookup"><span data-stu-id="5f964-148">Then enter the address of the SharePoint folder:</span></span>

    - <span data-ttu-id="5f964-149">对于 **SP 主**文档类型：文件导入源（主）</span><span class="sxs-lookup"><span data-stu-id="5f964-149">For the **SP Main** document type: Files import source (main)</span></span>
    - <span data-ttu-id="5f964-150">对于 **SP 备用**文档类型：文件导入源（备用）</span><span class="sxs-lookup"><span data-stu-id="5f964-150">For the **SP Alternative** document type: Files import source (alternative)</span></span>

<span data-ttu-id="5f964-151">[![SharePoint 设置 – 新文档类型](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)</span><span class="sxs-lookup"><span data-stu-id="5f964-151">[![SharePoint setting – new document type](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)</span></span>

## <a name="configure-er-sources-for-the-er-format"></a><span data-ttu-id="5f964-152">为 ER 格式配置 ER 源</span><span class="sxs-lookup"><span data-stu-id="5f964-152">Configure ER sources for the ER format</span></span>
1. <span data-ttu-id="5f964-153">单击**组织管理** > **电子申报** > **电子申报来源**。</span><span class="sxs-lookup"><span data-stu-id="5f964-153">Click **Organization administration** > **Electronic reporting** > **Electronic reporting source**.</span></span>
2. <span data-ttu-id="5f964-154">在**电子申报来源**页面中，使用配置的 ER 格式为数据导入配置源文件。</span><span class="sxs-lookup"><span data-stu-id="5f964-154">On the **Electronic reporting source** page, configure the source files for data import by using the configured ER format.</span></span>
3. <span data-ttu-id="5f964-155">定义一个文件名掩码，以便导入 .xlsx 扩展名的文件。</span><span class="sxs-lookup"><span data-stu-id="5f964-155">Define a file name mask, so that only files with the .xlsx extension are imported.</span></span> <span data-ttu-id="5f964-156">该文件名掩码可选，仅当定义了才使用。</span><span class="sxs-lookup"><span data-stu-id="5f964-156">The file name mask is optional and is used only when it has been defined.</span></span> <span data-ttu-id="5f964-157">只能为每个 ER 定义一种掩码。</span><span class="sxs-lookup"><span data-stu-id="5f964-157">You can define only one mask for each ER format.</span></span>
4. <span data-ttu-id="5f964-158">选择前面创建的两个 SharePoint 文件夹。</span><span class="sxs-lookup"><span data-stu-id="5f964-158">Select both SharePoint folders that you created earlier.</span></span>

<span data-ttu-id="5f964-159">[![ER 文件来源设置](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)</span><span class="sxs-lookup"><span data-stu-id="5f964-159">[![ER files source setting](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)</span></span>

> [!NOTE]
><span data-ttu-id="5f964-160">将为每家申请公司分别定义 ER *来源*。</span><span class="sxs-lookup"><span data-stu-id="5f964-160">The ER *source* is defined for each application company individually.</span></span> <span data-ttu-id="5f964-161">相反，ER *配置*则由多家公司共用。</span><span class="sxs-lookup"><span data-stu-id="5f964-161">By contrast, ER *configurations* are shared across companies.</span></span>

> [!NOTE]
> <span data-ttu-id="5f964-162">如果删除 ER 格式的 ER 来源设置，也将删除所有连接的文件的状态（见下文）。</span><span class="sxs-lookup"><span data-stu-id="5f964-162">When you delete an ER source setting for an ER format, all connected file states (see below) are also deleted.</span></span>

## <a name="review-the-files-states-for-the-er-format"></a><span data-ttu-id="5f964-163">检查 ER 格式的文件状态</span><span class="sxs-lookup"><span data-stu-id="5f964-163">Review the files states for the ER format</span></span>
1. <span data-ttu-id="5f964-164">在**电子申报来源**页中，选择**来源的文件状态**检查为当前 ER 格式配置的文件来源的内容。</span><span class="sxs-lookup"><span data-stu-id="5f964-164">On the **Electronic reporting source** page, select **File states for the sources** to review the content of the configured file sources for the current ER format.</span></span>
2. <span data-ttu-id="5f964-165">在**文件** 部分，检查文件的列表。</span><span class="sxs-lookup"><span data-stu-id="5f964-165">In the **Files** section, review the list of files.</span></span> <span data-ttu-id="5f964-166">此列表提供以下信息：</span><span class="sxs-lookup"><span data-stu-id="5f964-166">This list presents the following:</span></span>

    - <span data-ttu-id="5f964-167">根据文件名掩码（如果定义了文件名掩码）适用且已准备就绪可导入的源文件。</span><span class="sxs-lookup"><span data-stu-id="5f964-167">Source files that are applicable, based on the file name mask (if a file name mask is defined), and that are ready for data import.</span></span> <span data-ttu-id="5f964-168">对于这些文件，**导入格式的源日志**部分为空。</span><span class="sxs-lookup"><span data-stu-id="5f964-168">For these files, the **Sources log for the import format** section is blank.</span></span>
    - <span data-ttu-id="5f964-169">以前导入的文件。</span><span class="sxs-lookup"><span data-stu-id="5f964-169">Previously imported files.</span></span> <span data-ttu-id="5f964-170">对于每个这样的文件，可在**导入格式的源日志**部分中检查该文件的导入历史记录。</span><span class="sxs-lookup"><span data-stu-id="5f964-170">For each of these files, in the **Sources log for the import format** section, you can review the history of import of this file.</span></span>

<span data-ttu-id="5f964-171">也可以打开**源的文件状态**页，方法是选择**组织管理** \> **电子申报** \> **源的文件状态**。</span><span class="sxs-lookup"><span data-stu-id="5f964-171">You can also open the **File states for the sources** page by selecting **Organization administration** \> **Electronic reporting** \> **File states for the sources**.</span></span> <span data-ttu-id="5f964-172">这样，该页就提供了有关在您当前登录的公司中已经为其配置了文件来源的所有 ER 格式的文件来源的信息。</span><span class="sxs-lookup"><span data-stu-id="5f964-172">In this case, the page provides information about file sources for all ER formats that file sources have been configured for in the company that you're currently signed in to.</span></span>

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a><span data-ttu-id="5f964-173">从 SharePoint 文件夹中的 Excel 文件导入数据</span><span class="sxs-lookup"><span data-stu-id="5f964-173">Import data from Excel files that are in a SharePoint folder</span></span>
1. <span data-ttu-id="5f964-174">在 SharePoint 中，将包含供应商交易记录的 Microsoft Excel 文件 **1099import-data.xlsx** 上传到您前面创建的**文件导入源（主）** SharePoint 文件夹。</span><span class="sxs-lookup"><span data-stu-id="5f964-174">In SharePoint, upload the Microsoft Excel file **1099import-data.xlsx** that contains vendor transactions to the **Files import source (main)** SharePoint folder that you created earlier.</span></span>

<span data-ttu-id="5f964-175">[![SharePoint 内容 – 要导入的 Microsoft Excel 文件](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)</span><span class="sxs-lookup"><span data-stu-id="5f964-175">[![SharePoint content – Microsoft Excel file for importing](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)</span></span>

2. <span data-ttu-id="5f964-176">在 Finance and Operations 中的**源的文件状态**页上，选择**刷新**以刷新页面。</span><span class="sxs-lookup"><span data-stu-id="5f964-176">In Finance and Operations, on the **File states for the sources** page, select **Refresh** to refresh the page.</span></span> <span data-ttu-id="5f964-177">请注意，此窗体中将显示已上传到 SharePoint 的 Excel 文件，其状态为**就绪**。</span><span class="sxs-lookup"><span data-stu-id="5f964-177">Note that the Excel file that was uploaded to SharePoint appeared in this form with the status **Ready**.</span></span> <span data-ttu-id="5f964-178">现在支持以下状态：</span><span class="sxs-lookup"><span data-stu-id="5f964-178">The following statuses are currently supported:</span></span>

    - <span data-ttu-id="5f964-179">**就绪** - 为 SharePoint 文件夹中的每个新文件自动分配的状态。</span><span class="sxs-lookup"><span data-stu-id="5f964-179">**Ready** - Assigned automatically for each new file in a SharePoint folder.</span></span> <span data-ttu-id="5f964-180">此状态表示该文件已准备就绪，可以导入。</span><span class="sxs-lookup"><span data-stu-id="5f964-180">This status means that the file is ready for import.</span></span>
    - <span data-ttu-id="5f964-181">**正在导入** - 导入过程（如果正在同时运行多个过程）将锁定文件以防其他过程使用时 ER 报表自动分配的状态。</span><span class="sxs-lookup"><span data-stu-id="5f964-181">**Importing** - Assigned automatically by an ER report when the file will be locked by the import process to prevent its usage by other processes (if many of them are running simultaneously).</span></span>
    - <span data-ttu-id="5f964-182">**已导入** - 文件导入成功完成时 ER 报表自动分配的状态。</span><span class="sxs-lookup"><span data-stu-id="5f964-182">**Imported** - Assigned automatically by an ER report when the file import is successfully completed.</span></span> <span data-ttu-id="5f964-183">此状态表示已从配置的文件来源（SharePoint 文件夹）删除了导入的文件。</span><span class="sxs-lookup"><span data-stu-id="5f964-183">This status means that the imported file has been deleted from the configured files source (SharePoint folder).</span></span>
    - <span data-ttu-id="5f964-184">**失败** - 文件导入完成，但出现错误或异常时，ER 报表自动分配的状态。</span><span class="sxs-lookup"><span data-stu-id="5f964-184">**Failed** - Assigned automatically by an ER report when the file import completed with errors or exceptions.</span></span>
    - <span data-ttu-id="5f964-185">**保留** - 用户在此窗体中手动分配的状态。</span><span class="sxs-lookup"><span data-stu-id="5f964-185">**On hold** - Assigned manually by user on this form.</span></span> <span data-ttu-id="5f964-186">此状态表示暂时不导入该文件。</span><span class="sxs-lookup"><span data-stu-id="5f964-186">This status means that the file will not be imported for now.</span></span> <span data-ttu-id="5f964-187">此状态可用于推迟导入某些文件。</span><span class="sxs-lookup"><span data-stu-id="5f964-187">This status can be used to postpone the import of some files.</span></span>

<span data-ttu-id="5f964-188">[![所选来源的 ER 文件状态页](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)</span><span class="sxs-lookup"><span data-stu-id="5f964-188">[![ER file states page for the selected sources](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)</span></span>

## <a name="import-data-from-sharepoint-files"></a><span data-ttu-id="5f964-189">从 SharePoint 文件导入数据</span><span class="sxs-lookup"><span data-stu-id="5f964-189">Import data from SharePoint files</span></span>
1. <span data-ttu-id="5f964-190">打开 ER 配置树，选择 **1099 付款模型**，然后展开 ER 模型组件列表。</span><span class="sxs-lookup"><span data-stu-id="5f964-190">Open the ER configurations tree, select the **1099 Payment model**, and expand the list of ER model components.</span></span>
2. <span data-ttu-id="5f964-191">选择模型映射名称以打开所选 ER 模型配置的模型映射列表。</span><span class="sxs-lookup"><span data-stu-id="5f964-191">Select the name of the model mapping to open the list of model mappings of the selected ER model configuration.</span></span>

<span data-ttu-id="5f964-192">[![所选来源的 ER 文件状态页](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)</span><span class="sxs-lookup"><span data-stu-id="5f964-192">[![ER file states page for the selected sources](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)</span></span>

3. <span data-ttu-id="5f964-193">选择**运行**以运行所选模型映射。</span><span class="sxs-lookup"><span data-stu-id="5f964-193">Select **Run** to run the selected model mapping.</span></span> <span data-ttu-id="5f964-194">因为您为 ER 格式配置了文件源，所以可以根据需要更改**文件源**选项的设置。</span><span class="sxs-lookup"><span data-stu-id="5f964-194">Because you configured file sources for the ER format, you can change the setting of the **File source** option as you require.</span></span> <span data-ttu-id="5f964-195">如果保留此选项的设置，将从配置的源（本示例中为 SharePoint 文件夹）导入 .xslx 文件。</span><span class="sxs-lookup"><span data-stu-id="5f964-195">If you keep the setting of this option, the .xslx files are imported from the configured sources (the SharePoint folders, in this example).</span></span>

    <span data-ttu-id="5f964-196">在本示例中，仅导入一个文件。</span><span class="sxs-lookup"><span data-stu-id="5f964-196">In this example, you're importing only one file.</span></span> <span data-ttu-id="5f964-197">但是，如果有多个文件，将按这些文件添加到 SharePoint 文件夹的顺序选择导入。</span><span class="sxs-lookup"><span data-stu-id="5f964-197">However, if there are multiple files, they are selected for importing in the order in which they were added to the SharePoint folder.</span></span> <span data-ttu-id="5f964-198">每次运行 ER 格式都将导入选择的一个文件。</span><span class="sxs-lookup"><span data-stu-id="5f964-198">Every run of an ER format imports a single selected file.</span></span>

<span data-ttu-id="5f964-199">[![运行 ER 模型映射](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)</span><span class="sxs-lookup"><span data-stu-id="5f964-199">[![Run ER model mapping](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)</span></span>

4. <span data-ttu-id="5f964-200">该模型映射可以以无人值守模式运行。</span><span class="sxs-lookup"><span data-stu-id="5f964-200">The model mapping can run unattended in batch mode.</span></span> <span data-ttu-id="5f964-201">在这种情况下，只要批处理运行该 ER 格式，都将从配置的文件源导入一个文件。</span><span class="sxs-lookup"><span data-stu-id="5f964-201">In this case, every time that a batch runs this ER format, a single file is imported from the configured file sources.</span></span> <span data-ttu-id="5f964-202">使用以下代码实施此批处理运行。</span><span class="sxs-lookup"><span data-stu-id="5f964-202">Use the following code to implement this batch run.</span></span>

    ```
    ERObjectsFactory::createMappingDestinationRunByImportFormatMappingId().run()
    ```

    <span data-ttu-id="5f964-203">如果将一个文件从 SharePoint 文件夹成功导入，将在该文件夹中删除这个文件。</span><span class="sxs-lookup"><span data-stu-id="5f964-203">When a file is successfully imported from the SharePoint folder, it's deleted from that folder.</span></span>

5. <span data-ttu-id="5f964-204">输入凭证 ID（如 **V-00001**），然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="5f964-204">Enter the voucher ID, such as **V-00001**, and then select **OK**.</span></span>

<span data-ttu-id="5f964-205">[![运行 ER 模型映射](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)</span><span class="sxs-lookup"><span data-stu-id="5f964-205">[![Run ER model mapping](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)</span></span>

6. <span data-ttu-id="5f964-206">在**源的文件状态**页中，选择**刷新**以刷新页面。</span><span class="sxs-lookup"><span data-stu-id="5f964-206">On the **File states for the sources** page, select **Refresh** to refresh the page.</span></span>

<span data-ttu-id="5f964-207">[![所选来源的 ER 文件状态页](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)</span><span class="sxs-lookup"><span data-stu-id="5f964-207">[![ER file states page for the selected sources](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)</span></span>

7. <span data-ttu-id="5f964-208">在**文件** 部分，检查文件的列表。</span><span class="sxs-lookup"><span data-stu-id="5f964-208">In the **Files** section, review the list of files.</span></span> <span data-ttu-id="5f964-209">**导入格式的源日志**部分提供 Excel 文件导入历史记录。</span><span class="sxs-lookup"><span data-stu-id="5f964-209">The **Sources log for the import format** section provides the history of the Excel file import.</span></span> <span data-ttu-id="5f964-210">由于该文件已成功导入，所以在 SharePoint 文件夹中标记为**已删除**。</span><span class="sxs-lookup"><span data-stu-id="5f964-210">Because this file was successfully imported, it's marked as **Deleted** in the SharePoint folder.</span></span>
8. <span data-ttu-id="5f964-211">检查**文件导入源（主）** SharePoint 文件夹。</span><span class="sxs-lookup"><span data-stu-id="5f964-211">Review the **Files import source (main)** SharePoint folder.</span></span> <span data-ttu-id="5f964-212">已从该文件夹删除了成功导入的 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="5f964-212">The Excel files that were successfully imported have been deleted from this folder.</span></span>
9. <span data-ttu-id="5f964-213">在 Finance and Operations 中，选择**应付帐款** \> **定期任务** \> **1099 税** \> **用于 1099 的供应商结算**。</span><span class="sxs-lookup"><span data-stu-id="5f964-213">In Finance and Operations, select **Accounts payable** \> **Periodic tasks** \> **Tax 1099** \> **Vendor settlement for 1099s**.</span></span>
10. <span data-ttu-id="5f964-214">在**开始日期**和**结束日期**字段中，输入相应值。</span><span class="sxs-lookup"><span data-stu-id="5f964-214">In the **From date** and **To date** fields, enter appropriate values.</span></span> <span data-ttu-id="5f964-215">然后选择**手动 1099 交易记录**。</span><span class="sxs-lookup"><span data-stu-id="5f964-215">Then select **Manual 1099 transactions**.</span></span>

    <span data-ttu-id="5f964-216">此页面中将显示在 SharePoint 上为凭证 **V-00001** 通过 Excel 文件导入的供应商交易记录。</span><span class="sxs-lookup"><span data-stu-id="5f964-216">The vendor transactions that were imported from the Excel files on SharePoint for voucher **V-00001**, are presented on the page.</span></span>

<span data-ttu-id="5f964-217">[![1099 供应商交易记录页](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)</span><span class="sxs-lookup"><span data-stu-id="5f964-217">[![1099 vendor transactions page](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)</span></span>

## <a name="prepare-an-excel-file-for-import"></a><span data-ttu-id="5f964-218">准备要导入的 Excel 文件</span><span class="sxs-lookup"><span data-stu-id="5f964-218">Prepare an Excel file for import</span></span>
1. <span data-ttu-id="5f964-219">打开以前使用过的 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="5f964-219">Open the Excel file that you previously used.</span></span> <span data-ttu-id="5f964-220">在第 3 行第 1 列，添加一个申请中没有的供应商代码。</span><span class="sxs-lookup"><span data-stu-id="5f964-220">In row 3 column 1, add a vendor code that doesn't exist in the application.</span></span> <span data-ttu-id="5f964-221">为该行添加更多虚假的供应商信息。</span><span class="sxs-lookup"><span data-stu-id="5f964-221">Add additional false vendor information to the row.</span></span>

<span data-ttu-id="5f964-222">[![要从 SharePoint 导入的 Microsoft Excel 示例文件](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)</span><span class="sxs-lookup"><span data-stu-id="5f964-222">[![Sample Microsoft Excel file for importing from SharePoint](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)</span></span>

2. <span data-ttu-id="5f964-223">将已更新且包含供应商交易记录的 Excel 文件上传到**文件导入源（主）** SharePoint 文件夹。</span><span class="sxs-lookup"><span data-stu-id="5f964-223">Upload the updated Excel file that contains vendors transactions to the **Files import source (main)** SharePoint folder.</span></span>
3. <span data-ttu-id="5f964-224">在 Finance and Operations 中，打开 ER 配置树，选择 **1099 付款模型**，然后展开 ER 模型组件列表。</span><span class="sxs-lookup"><span data-stu-id="5f964-224">In Finance and Operations, open the ER configurations tree, select the **1099 Payment model**, and expand the list of ER model components.</span></span>
4. <span data-ttu-id="5f964-225">选择模型映射的名称以更新该模型映射，从而在数据导入过程中将不正确的供应商代码视为错误。</span><span class="sxs-lookup"><span data-stu-id="5f964-225">Select the name of the model mapping to update the model mapping so that the incorrect vendor code is considered an error during the data import process.</span></span>
5. <span data-ttu-id="5f964-226">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="5f964-226">Select **Designer**.</span></span>
6. <span data-ttu-id="5f964-227">在**验证**选项卡上，必须更改为了评估应用程序中是否存在导入的供应商科目而配置的验证规则的验证后操作。</span><span class="sxs-lookup"><span data-stu-id="5f964-227">On the **Validations** tab, you must change the post-validation action for the validation rule that was configured to evaluate whether the vendor account that is imported exists in the application.</span></span> <span data-ttu-id="5f964-228">将**验证后操作**字段的值更改为**停止执行**，保存更改，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="5f964-228">Update the value of the **Post-validation action** field to **Stop execution**, save your changes, and close the page.</span></span>

<span data-ttu-id="5f964-229">[![ER 模型映射设计器页面](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)</span><span class="sxs-lookup"><span data-stu-id="5f964-229">[![ER model mapping designer page](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)</span></span>

7. <span data-ttu-id="5f964-230">保存更改，然后关闭 ER 模型映射设计器。</span><span class="sxs-lookup"><span data-stu-id="5f964-230">Save your changes, and close the ER model mapping designer.</span></span>
8. <span data-ttu-id="5f964-231">选择**运行**以运行修改后的 ER 模型映射。</span><span class="sxs-lookup"><span data-stu-id="5f964-231">Select **Run** to run the modified ER model mapping.</span></span>
9. <span data-ttu-id="5f964-232">输入凭证 ID（如 **V-00002**），然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="5f964-232">Enter the voucher ID, such as **V-00002**, and then select **OK**.</span></span>

    <span data-ttu-id="5f964-233">请注意，信息日志中包含用于说明 SharePoint folder 文件夹中的文件包含不正确的供应商科目，因此不能导入的通知。</span><span class="sxs-lookup"><span data-stu-id="5f964-233">Note that the Infolog contains the notification informing that residing in SharePoint folder file contains incorrect vendor account and can’t be imported.</span></span>

<span data-ttu-id="5f964-234">[![运行 ER 模型映射](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)</span><span class="sxs-lookup"><span data-stu-id="5f964-234">[![Run ER model mapping](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)</span></span>

10. <span data-ttu-id="5f964-235">在**源的文件状态**页，选择**刷新**，然后在**文件**部分中查看文件列表。</span><span class="sxs-lookup"><span data-stu-id="5f964-235">On the **File states for the sources** page, select **Refresh**, and then, in the **Files** section, review the list of files.</span></span>

<span data-ttu-id="5f964-236">[![所选来源的 ER 文件状态页](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)</span><span class="sxs-lookup"><span data-stu-id="5f964-236">[![ER file states page for the selected sources](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)</span></span>

<span data-ttu-id="5f964-237">**导入格式的源日志**部分指示导入过程失败，文件仍然在 SharePoint 文件夹中（**已删除**复选框未选中）。</span><span class="sxs-lookup"><span data-stu-id="5f964-237">The **Sources log for the import format** section indicates that the import process failed and that the file is still in the SharePoint folder (the **Is deleted** checkbox is not selected).</span></span> <span data-ttu-id="5f964-238">如果在 SharePoint 中通过添加正确的供应商代码修改该文件，然后在**导入格式的源日志**部分中将该文件的状态从**失败**更改为**就绪**，则可再次导入该文件。</span><span class="sxs-lookup"><span data-stu-id="5f964-238">If you fix this file on SharePoint by adding the proper vendor code and then change the status of the file from **Failed** to **Ready** in the **Sources log for the import format** section, you can import the file again.</span></span>

11. <span data-ttu-id="5f964-239">检查**文件导入源（主）** SharePoint 文件夹。</span><span class="sxs-lookup"><span data-stu-id="5f964-239">Review the **Files import source (main)** SharePoint folder.</span></span> <span data-ttu-id="5f964-240">请注意，未导入的 Excel file 文件仍在该文件夹中。</span><span class="sxs-lookup"><span data-stu-id="5f964-240">Notice that the Excel file that wasn't imported is still in this folder.</span></span>
12. <span data-ttu-id="5f964-241">在 Finance and Operations 中，选择**应付帐款** \> **定期任务** \> **1099税** \> **1099 的供应商结算**，在**开始日期**和**结束日期**字段中输入相应值，然后选择**手动 1099 交易记录**。</span><span class="sxs-lookup"><span data-stu-id="5f964-241">In Finance and Operations, select **Accounts payable** \> **Periodic tasks** \> **Tax 1099** \> **Vendor settlement for 1099s**, enter appropriate values in the **From date** and **To date** fields, and then select **Manual 1099 transactions**.</span></span>

    <span data-ttu-id="5f964-242">只有凭证 V-00001 的交易记录。</span><span class="sxs-lookup"><span data-stu-id="5f964-242">Only transactions for voucher V-00001 are available.</span></span> <span data-ttu-id="5f964-243">即使在 Excel 文件中发现了上次导入的交易记录的错误，也没有凭证 V-00002 的交易记录。</span><span class="sxs-lookup"><span data-stu-id="5f964-243">No transactions for voucher V-00002 are available even though the error for the last imported transaction has been found in the Excel file.</span></span>


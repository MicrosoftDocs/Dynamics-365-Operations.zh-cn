---
title: 配置电子申报 (ER) 以便将数据导入 Power BI
description: 本主题说明您可以如何使用您的电子申报 (ER) 配置安排数据从您的实例转移至 Power BI 服务。
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b37bc608b3b987016622d9cd0abc66e420025d26
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944429"
---
# <a name="configure-electronic-reporting-er-to-pull-data-into-power-bi"></a><span data-ttu-id="6ef8c-103">配置电子申报 (ER) 以便将数据导入 Power BI</span><span class="sxs-lookup"><span data-stu-id="6ef8c-103">Configure Electronic reporting (ER) to pull data into Power BI</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ef8c-104">本主题说明您可以如何使用您的电子申报 (ER) 配置安排数据从您的实例转移至 Power BI 服务。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-104">This topic explains how you can use your Electronic reporting (ER) configuration to arrange the transfer of data from your instance to Power BI services.</span></span> <span data-ttu-id="6ef8c-105">例如，本主题使用内部统计交易记录作为必须转移的业务数据。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-105">As an example, this topic uses Intrastat transactions as business data that must be transferred.</span></span> <span data-ttu-id="6ef8c-106">Power BI 地图可视化使用此内部统计交易记录数据显示 Power BI 报表上的公司导入/导出活动的分析视图。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-106">The Power BI map visualization uses this Intrastat transaction data to present a view for analysis of company import/export activities on the Power BI report.</span></span>

## <a name="overview"></a><span data-ttu-id="6ef8c-107">概览</span><span class="sxs-lookup"><span data-stu-id="6ef8c-107">Overview</span></span>

<span data-ttu-id="6ef8c-108">Microsoft Power BI 是一组软件服务、应用和连接器的集合，它们共同将外部数据源转换为一致、直观和交互的见解。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-108">Microsoft Power BI is a collection of software services, apps, and connectors that work together to turn external sources of data into coherent, visually immersive, and interactive insights.</span></span> <span data-ttu-id="6ef8c-109">电子申报 (ER) 允许用户轻松配置数据源和安排数据从应用程序转移到 Power BI。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-109">Electronic reporting (ER) lets users easily configure data sources and arrange the transfer of data from the application to Power BI.</span></span> <span data-ttu-id="6ef8c-110">数据作为 OpenXML 工作表（Microsoft Excel 工作簿文件）格式的文件传输。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-110">The data is transferred as files in the OpenXML worksheet (Microsoft Excel workbook file) format.</span></span> <span data-ttu-id="6ef8c-111">转移的文件存储在为该目的而配置的 Microsoft SharePoint Server 上。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-111">The transferred files are stored on a Microsoft SharePoint Server that has been configured for that purpose.</span></span> <span data-ttu-id="6ef8c-112">存储的文件在 Power BI 中用来制作包含可视化项（表格、图标、地图等）的报表。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-112">The stored files are used in Power BI to make reports that include visualizations (tables, charts, maps, and so on).</span></span> <span data-ttu-id="6ef8c-113">Power BI 报表与 Power BI 用户共享，因为他们在 Power BI 仪表板和应用程序页面上访问。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-113">Power BI reports are shared with Power BI users, and they are accessed in Power BI dashboards and on the application pages.</span></span> <span data-ttu-id="6ef8c-114">本主题对以下任务进行解释：</span><span class="sxs-lookup"><span data-stu-id="6ef8c-114">This topic explains the following tasks:</span></span>

- <span data-ttu-id="6ef8c-115">配置 Microsoft Dynamics 365 Finance。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-115">Configure Microsoft Dynamics 365 Finance.</span></span>
- <span data-ttu-id="6ef8c-116">准备您的 ER 格式配置，以从 Finance 应用程序获取数据。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-116">Prepare your ER format configuration to get data from the Finance application.</span></span>
- <span data-ttu-id="6ef8c-117">配置将数据转移至 Power BI 的 ER 环境。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-117">Configure the ER environment to transfer data to Power BI.</span></span>
- <span data-ttu-id="6ef8c-118">使用转移的数据创建 Power BI 报表。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-118">Use transferred data to create a Power BI report.</span></span>
- <span data-ttu-id="6ef8c-119">使 Power BI 报表在 Finance 中可访问。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-119">Make the Power BI report accessible in Finance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6ef8c-120">先决条件</span><span class="sxs-lookup"><span data-stu-id="6ef8c-120">Prerequisites</span></span>
<span data-ttu-id="6ef8c-121">要完成本主题中的示例，您必须具有以下访问权限：</span><span class="sxs-lookup"><span data-stu-id="6ef8c-121">To complete the example in this topic, you must have the following access:</span></span>

- <span data-ttu-id="6ef8c-122">以下其中一个角色的访问权限：</span><span class="sxs-lookup"><span data-stu-id="6ef8c-122">Access for one of the following roles:</span></span>

    - <span data-ttu-id="6ef8c-123">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="6ef8c-123">Electronic reporting developer</span></span>
    - <span data-ttu-id="6ef8c-124">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="6ef8c-124">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="6ef8c-125">系统管理员</span><span class="sxs-lookup"><span data-stu-id="6ef8c-125">System administrator</span></span>

- <span data-ttu-id="6ef8c-126">为了与应用程序一起使用而配置的 SharePoint Server 的访问权限</span><span class="sxs-lookup"><span data-stu-id="6ef8c-126">Access to the SharePoint Server that is configured for use with the application</span></span>
- <span data-ttu-id="6ef8c-127">访问 Power BI 框架</span><span class="sxs-lookup"><span data-stu-id="6ef8c-127">Access to the Power BI framework</span></span>

## <a name="configure-document-management-parameters"></a><span data-ttu-id="6ef8c-128">配置文档管理参数</span><span class="sxs-lookup"><span data-stu-id="6ef8c-128">Configure document management parameters</span></span>
1. <span data-ttu-id="6ef8c-129">在 **文档管理参数** 页面上，配置您登录的公司中使用的 SharePoint Server 访问权限为（在此示例中为 DEMF 公司）。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-129">On the **Document management parameters** page, configure access to the SharePoint Server that will be used in the company that you're signed in to (the DEMF company in this example).</span></span>
2. <span data-ttu-id="6ef8c-130">测试与 SharePoint Server 的连接性，确保您已被授予访问权限。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-130">Test the connection to the SharePoint Server to make sure that you've been granted access.</span></span>

    <span data-ttu-id="6ef8c-131">[![文档管理参数页面](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-131">[![Document management parameters page](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)</span></span>

3. <span data-ttu-id="6ef8c-132">打开配置的 SharePoint 站点。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-132">Open the configured SharePoint site.</span></span> <span data-ttu-id="6ef8c-133">创建 ER 将存储 Excel 文件的新文件夹，这些 Excel 文件中含有 Power BI 报表要求用作 Power BI 数据集源的业务数据。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-133">Create a new folder where ER will store Excel files that have the business data that the Power BI reports require as a source of Power BI datasets.</span></span>
4. <span data-ttu-id="6ef8c-134">在 **文档类型** 页面上创建将用来访问您刚才创建的 SharePoint 文件夹的新文档类型。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-134">On the **Document types** page, create a new document type that will be used to access the SharePoint folder that you just created.</span></span> <span data-ttu-id="6ef8c-135">在 **组** 字段中输入 **文件**，在 **位置** 字段中输入 **SharePoint**，然后输入 SharePoint 文件夹的地址。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-135">Enter **File** in the **Group** field and **SharePoint** in the **Location** field, and then enter the address of the SharePoint folder.</span></span>

    <span data-ttu-id="6ef8c-136">[![文档类型页面](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-136">[![Document types page](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)</span></span>

## <a name="configure-er-parameters"></a><span data-ttu-id="6ef8c-137">配置 ER 参数</span><span class="sxs-lookup"><span data-stu-id="6ef8c-137">Configure ER parameters</span></span>
1. <span data-ttu-id="6ef8c-138">在 **电子申报** 工作区中，单击 **电子申报参数** 链接。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-138">In the **Electronic reporting** workspace, click the **Electronic reporting parameters** link.</span></span>
2. <span data-ttu-id="6ef8c-139">在 **附件** 选项卡上，对所有字段选择 **文件** 文档类型。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-139">On the **Attachments** tab, select the **File** document type for all the fields.</span></span>
3. <span data-ttu-id="6ef8c-140">在 **电子申报** 工作区中，通过单击 **设置有效** 使所需的提供商有效。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-140">In the **Electronic reporting** workspace, make the required provider active by clicking **Set active**.</span></span> <span data-ttu-id="6ef8c-141">有关详细信息，请播放 **ER 选择服务提供商** 任务指南。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-141">For more information, play the **ER Select service provider** task guide.</span></span>

## <a name="use-an-er-data-model-as-the-source-of-data"></a><span data-ttu-id="6ef8c-142">使用 ER 数据模型作为数据源</span><span class="sxs-lookup"><span data-stu-id="6ef8c-142">Use an ER data model as the source of data</span></span>
<span data-ttu-id="6ef8c-143">您必须具有作为业务数据源在 Power BI 报表上使用的 ER 数据模型。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-143">You must have an ER data model as the source of business data that will be used on Power BI reports.</span></span> <span data-ttu-id="6ef8c-144">此数据模型从 ER 配置库上载。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-144">This data model is uploaded from the ER configurations repository.</span></span> <span data-ttu-id="6ef8c-145">有关详细信息，请参阅 [从 Lifecycle Services 下载电子申报配置](download-electronic-reporting-configuration-lcs.md)或播放 **ER 从 Lifecycle Services 导入配置** 任务指南。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-145">For more information, see [Download Electronic reporting configurations from Lifecycle Services](download-electronic-reporting-configuration-lcs.md), or play the **ER Import a configuration from Lifecycle Services** task guide.</span></span> <span data-ttu-id="6ef8c-146">选择 **内部统计** 作为从选定的 ER 配置库中上载的数据模型。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-146">Select **Intrastat** as the data model that will be uploaded from the selected ER configurations repository.</span></span> <span data-ttu-id="6ef8c-147">（在此示例中，使用模型的版本 1。）然后可以访问 **配置** 页面上的 **内部统计** ER 模型配置。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-147">(In this example, version 1 of the model is used.) You can then access the **Intrastat** ER model configuration on the **Configurations** page.</span></span>

<span data-ttu-id="6ef8c-148">[![配置页面上的内部统计 ER 模型配置](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-148">[![Intrastat ER model cofiguration on the Configurations page](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)</span></span>

## <a name="design-an-er-format-configuration"></a><span data-ttu-id="6ef8c-149">设计 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="6ef8c-149">Design an ER format configuration</span></span>
<span data-ttu-id="6ef8c-150">您必须创建使用 **内部统计** 数据模型作为业务数据源的新 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-150">You must create a new ER format configuration that uses the **Intrastat** data model as the source of business data.</span></span> <span data-ttu-id="6ef8c-151">此格式配置必须将输出结果生成为 OpenXML（Excel 文件）格式的电子文档。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-151">This format configuration must generate output results as electronic documents in OpenXML (Excel file) format.</span></span> <span data-ttu-id="6ef8c-152">有关详细信息，请播放 **ER 创建 OPENXML 格式的报表配置** 任务指南。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-152">For more information, play the **ER Create a configuration for reports in OPENXML format** task guide.</span></span> <span data-ttu-id="6ef8c-153">将新配置命名为 **导入/导出活动**，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-153">Name the new configuration **Import / export activities**, as shown in the following illustration.</span></span> <span data-ttu-id="6ef8c-154">使用[ER 数据导入和导出详细信息](https://download.microsoft.com/download/f/7/5/f755c0fd-025c-4aa9-920b-909abb8302ad/ER-data-import-and-export-details.xlsx)Excel 文件作为设计 ER 格式时的模板。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-154">Use the [ER data - import and export details](https://download.microsoft.com/download/f/7/5/f755c0fd-025c-4aa9-920b-909abb8302ad/ER-data-import-and-export-details.xlsx) Excel file as a template when you design the ER format.</span></span> <span data-ttu-id="6ef8c-155">（有关如何导入格式模板的信息，请播放任务指南。）</span><span class="sxs-lookup"><span data-stu-id="6ef8c-155">(For information about how to import a format template, play the task guide.)</span></span>

<span data-ttu-id="6ef8c-156">[![导入/导出活动配置](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-156">[![Import / export activities configuration](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png)</span></span>

<span data-ttu-id="6ef8c-157">要修改 **导入/导出活动** 格式配置，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-157">To modify the **Import / export activities** format configuration, follow these steps.</span></span>

1. <span data-ttu-id="6ef8c-158">单击 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-158">Click **Designer**.</span></span>
2. <span data-ttu-id="6ef8c-159">在 **格式** 选项卡上，将此格式的文件元素命名为 **Excel 输出文件**。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-159">On the **Format** tab, name the file element for this format **Excel output file**.</span></span>

    <span data-ttu-id="6ef8c-160">[![Excel 输出文件元素](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-160">[![Excel output file element](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)</span></span>

3. <span data-ttu-id="6ef8c-161">在 **映射** 选项卡上，指定在任何时候运行此格式时将生成的 Excel 文件名。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-161">On the **Mapping** tab, specify the name of the Excel file that will be generated whenever this format is run.</span></span> <span data-ttu-id="6ef8c-162">将相关表达式配置为返回值 **导入和导出详细信息**（将自动添加 .xlsx 文件扩展名）。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-162">Configure the related expression to return the value **Import and export details** (the .xlsx file name extension will be added automatically).</span></span>

    <span data-ttu-id="6ef8c-163">[![格式设计器](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-163">[![Format designer](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)</span></span>

4. <span data-ttu-id="6ef8c-164">为此格式添加新的数据源项目。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-164">Add a new data source item for this format.</span></span> <span data-ttu-id="6ef8c-165">（进一步绑定数据将需要此枚举。）</span><span class="sxs-lookup"><span data-stu-id="6ef8c-165">(This enumeration will be required for further data binding.)</span></span>

    1. <span data-ttu-id="6ef8c-166">将数据源命名为 **direction\_enum**。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-166">Name the data source **direction\_enum**.</span></span>
    2. <span data-ttu-id="6ef8c-167">选择 **数据模型枚举** 作为数据源类型。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-167">Select **Data model enumeration** as the data source type.</span></span>
    3. <span data-ttu-id="6ef8c-168">请参阅 **方向** 数据模型枚举。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-168">Refer to the **Direction** data model enumeration.</span></span>

    <span data-ttu-id="6ef8c-169">[![direction_enum](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-169">[![direction_enum](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)</span></span>

5. <span data-ttu-id="6ef8c-170">完成 **内部统计** 数据模型元素与设计格式元素的绑定，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-170">Complete the binding of elements of the **Intrastat** data model and elements of the designed format, as shown in the following illustration.</span></span>

    <span data-ttu-id="6ef8c-171">[![完成绑定](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-171">[![Completing the binding](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)</span></span>

<span data-ttu-id="6ef8c-172">在运行后，ER 格式将生成 Excel 格式的输出结果。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-172">After it's run, the ER format generates the output result in Excel format.</span></span> <span data-ttu-id="6ef8c-173">它将内部统计交易记录的详细信息发送至输出结果，并通过将交易记录描述为导入活动或导出活动的方式对它们进行区分。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-173">It sends the details of the Intrastat transactions to the output result, and separates them as transactions that describe either import activities or export activities.</span></span> <span data-ttu-id="6ef8c-174">单击 **运行** 为 **内部统计** 页面上的内部统计交易记录列表测试新的 ER 格式（**税金** &gt; **申报** &gt; **外贸** &gt; **内部统计**）。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-174">Click **Run** to test the new ER format for the list of Intrastat transactions on the **Intrastat** page (**Tax** &gt; **Declarations** &gt; **Foreign trade** &gt; **Intrastat**).</span></span>

<span data-ttu-id="6ef8c-175">[![内部统计页面](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-175">[![Intrastat page](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png)</span></span>

<span data-ttu-id="6ef8c-176">生成以下输出结果。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-176">The following output result is generated.</span></span> <span data-ttu-id="6ef8c-177">文件命名为 **导入和导出详细信息.xlsx**，正如您在格式设置中所指定的。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-177">The file is named **Import and export details.xlsx**, as you specified in the format settings.</span></span>

<span data-ttu-id="6ef8c-178">[![导入和导出详细信息.xlsx](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-178">[![Import and export details.xlsx](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)</span></span>

## <a name="configure-the-er-destination"></a><span data-ttu-id="6ef8c-179">配置 ER 目标</span><span class="sxs-lookup"><span data-stu-id="6ef8c-179">Configure the ER destination</span></span>
<span data-ttu-id="6ef8c-180">您必须将 ER 框架配置为以特殊方式发送新 ER 格式配置的输出结果。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-180">You must configure the ER framework to send the output result of the new ER format configuration in a special way.</span></span>

- <span data-ttu-id="6ef8c-181">输出结果必须发送至选定的 SharePoint Server 的文件夹。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-181">The output result must be sent to the folder of the selected SharePoint Server.</span></span>
- <span data-ttu-id="6ef8c-182">每次执行格式配置必须创建相同 Excel 文件的新版本。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-182">Each execution of the format configuration must create a new version of same Excel file.</span></span>

<span data-ttu-id="6ef8c-183">在 **电子申报** 页面（**组织管理** &gt; **电子申报**）上，单击 **电子申报目标** 项目，然后添加新目标。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-183">On the **Electronic reporting** page (**Organization administration** &gt; **Electronic reporting**), click the **Electronic reporting destination** item, and add a new destination.</span></span> <span data-ttu-id="6ef8c-184">在 **参考** 字段中，选择您之前创建的 **导入/导出活动** 格式配置。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-184">In the **Reference** field, select the **Import / export activities** format configuration that you created earlier.</span></span> <span data-ttu-id="6ef8c-185">按照以下步骤为参考添加新的文件目标记录。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-185">Follow these steps to add a new file destination record for the reference.</span></span>

1. <span data-ttu-id="6ef8c-186">在 **命名** 字段中，输入文件目标的标题。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-186">In the **Name** field, enter the title of the file destination.</span></span>
2. <span data-ttu-id="6ef8c-187">在 **文件名** 字段中，为 Excel 文件格式组件选择名称 **Excel 输出文件**。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-187">In the **File name** field, select the name **Excel output file** for the Excel file format component.</span></span>

<span data-ttu-id="6ef8c-188">单击新目标记录的 **设置** 按钮。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-188">Click the **Settings** button for the new destination record.</span></span> <span data-ttu-id="6ef8c-189">然后在 **目标设置** 对话框中执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-189">Then, in the **Destination settings** dialog box, follow these steps.</span></span>

1. <span data-ttu-id="6ef8c-190">在 **Power BI** 选项卡上，将 **已启用** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-190">On the **Power BI** tab, set the **Enabled** option to **Yes**.</span></span>
2. <span data-ttu-id="6ef8c-191">在 **SharePoint** 字段中，选择您先前创建的 **共享** 文档类型。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-191">In the **SharePoint** field, select the **Shared** document type that you created earlier.</span></span>

## <a name="schedule-execution-of-the-configured-er-format"></a><span data-ttu-id="6ef8c-192">计划配置的 ER 格式的执行</span><span class="sxs-lookup"><span data-stu-id="6ef8c-192">Schedule execution of the configured ER format</span></span>
1. <span data-ttu-id="6ef8c-193">在 **配置** 页面（**组织管理** &gt; **电子申报** &gt; **配置**）上的配置树中，选择您先前创建的 **导入/导出活动** 配置。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-193">On the **Configurations** page (**Organization administration** &gt; **Electronic reporting** &gt; **Configurations**), in the configurations tree, select the **Import / export activities** configuration that you created earlier.</span></span>
2. <span data-ttu-id="6ef8c-194">将版本 1.1 的状态从 **草稿** 更改为 **完成**，使此格式可使用。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-194">Change the status of version 1.1 from **Draft** to **Complete** to make this format available for use.</span></span>

    <span data-ttu-id="6ef8c-195">[![配置页面上的导入/导出活动配置](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-195">[![Import/export activities configuration on the Configurations page](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png)</span></span>

3. <span data-ttu-id="6ef8c-196">选择 **导入/导出活动** 配置的已完成版本，然后点击 **运行**。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-196">Select the completed version of the **Import / export activities** configuration, and then click **Run**.</span></span> <span data-ttu-id="6ef8c-197">注意配置目标应用到以 Excel 格式生成的输出结果。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-197">Note that the configured destination is applied to the output result that is generated in Excel format.</span></span>
4. <span data-ttu-id="6ef8c-198">将 **批处理** 选项设置为 **是**，从而以未看管模式运行此报表。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-198">Set the **Batch processing** option to **Yes** to run this report in unattended mode.</span></span>
5. <span data-ttu-id="6ef8c-199">单击 **重复执行** 以计划此批处理执行所需的重复周期。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-199">Click **Recurrence** to schedule the required recurrence of this batch execution.</span></span> <span data-ttu-id="6ef8c-200">重复周期定义了更新数据转移至 Power BI 的频率。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-200">The recurrence defines how often the updated data will be transferred to Power BI.</span></span>

    <span data-ttu-id="6ef8c-201">[![电子报表参数对话框](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-201">[![Electronic report parameters dialog box](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png)</span></span>

6. <span data-ttu-id="6ef8c-202">在配置后，您可以在 **批处理作业** 页面上找到 ER 报表执行作业（**系统管理 &gt; 查询 &gt; 批处理作业**）。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-202">After it's configured, you can find the ER report execution job on the **Batch jobs** page (**System administration &gt; Inquiries &gt; Batch jobs**).</span></span>

    <span data-ttu-id="6ef8c-203">[![批处理作业页面](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-203">[![Batch jobs page](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png)</span></span>

7. <span data-ttu-id="6ef8c-204">第一次运行此作业时，目标创建的新 Excel 文件具有在选定的 SharePoint 文件夹中配置的名称。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-204">When this job is run for the first time, the destination creates a new Excel file that has the configured name in the selected SharePoint folder.</span></span> <span data-ttu-id="6ef8c-205">以后每次运行作业时，目标都会创建此 Excel 文件的新版本。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-205">Every subsequent time that the job is run, the destination creates a new version of this Excel file.</span></span>

    <span data-ttu-id="6ef8c-206">[![Excel 文件的新版本](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-206">[![New version of the Excel file](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)</span></span>

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a><span data-ttu-id="6ef8c-207">使用 ER 格式的输出结果创建 Power BI 数据集</span><span class="sxs-lookup"><span data-stu-id="6ef8c-207">Create a Power BI dataset by using the output result of the ER format</span></span>
1. <span data-ttu-id="6ef8c-208">登录 Power BI，打开现有 Power BI 组（工作区）或新建组。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-208">Sign in to Power BI, and either open an existing Power BI group (workspace) or create a new group.</span></span> <span data-ttu-id="6ef8c-209">单击 **导入或连接数据** 部分的 **文件** 下的 **添加**，或者单击左窗格中的 **数据集** 旁边的加号 (**+**)。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-209">Either click **Add** under **Files** in the **Import or Connect to Data** section, or click the plus sign (**+**) next to **Datasets** in the left pane.</span></span>

    <span data-ttu-id="6ef8c-210">[![创建数据集](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-210">[![Creating a dataset](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png)</span></span>

2. <span data-ttu-id="6ef8c-211">选择 **SharePoint - 团队站点** 选项，然后输入您正在使用的 SharePoint Server 的路径（在我们的示例中为 `https://ax7partner.litware.com`）。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-211">Select the **SharePoint – Team sites** option, and then enter the path of SharePoint Server that you're using (`https://ax7partner.litware.com` in our example).</span></span>
3. <span data-ttu-id="6ef8c-212">浏览到 **/Shared Documents/GER data/PowerBI** 文件夹，再选择您作为新 Power BI 数据集的数据源创建的 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-212">Browse to the **/Shared Documents/GER data/PowerBI** folder, and select the Excel file that you created as the source of data for the new Power BI dataset.</span></span>

    <span data-ttu-id="6ef8c-213">[![选择 Excel 文件](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-213">[![Selecting the Excel file](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png)</span></span>

4. <span data-ttu-id="6ef8c-214">单击 **连接**，然后单击 **导入**。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-214">Click **Connect**, and then click **Import**.</span></span> <span data-ttu-id="6ef8c-215">基于选择的 Excel 文件创建新的数据集。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-215">A new dataset is created that is based on the selected Excel file.</span></span> <span data-ttu-id="6ef8c-216">数据集也可以自动添加到新创建的仪表板。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-216">The dataset can also be added automatically to the newly created dashboard.</span></span>

    <span data-ttu-id="6ef8c-217">[![仪表板上的数据集](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-217">[![Dataset on the dashboard](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png)</span></span>

5. <span data-ttu-id="6ef8c-218">为此数据集配置强制定期更新的刷新计划。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-218">Configure the refresh schedule for this dataset to force a periodic update.</span></span> <span data-ttu-id="6ef8c-219">定期更新允许通过定期执行 ER 报表的新业务数据通过在 SharePoint Server 上创建的 Excel 文件的新版本消耗。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-219">Periodic updates enable the consumption of new business data that comes via periodic execution of the ER report through new versions of the Excel file that are created on the SharePoint Server.</span></span>

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a><span data-ttu-id="6ef8c-220">使用新的数据集创建 Power BI 报表</span><span class="sxs-lookup"><span data-stu-id="6ef8c-220">Create a Power BI report by using the new dataset</span></span>
1. <span data-ttu-id="6ef8c-221">单击您创建的 **导入和导出详细信息** Power BI 数据集。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-221">Click the **Import and export details** Power BI dataset that you created.</span></span>
2. <span data-ttu-id="6ef8c-222">配置可视化。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-222">Configure the visualization.</span></span> <span data-ttu-id="6ef8c-223">例如，选择 **填充的地图** 可视化，然后进行以下配置：</span><span class="sxs-lookup"><span data-stu-id="6ef8c-223">For example, select the **Filled map** visualization, and configure it as follows:</span></span>

    - <span data-ttu-id="6ef8c-224">将 **CountryOrigin** 数据集字段分配到地图可视化的 **位置** 字段。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-224">Assign the **CountryOrigin** dataset field to the **Location** field of the map visualization.</span></span>
    - <span data-ttu-id="6ef8c-225">将 **量** 数据集字段分配到地图可视化的 **色饱和度** 字段。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-225">Assign the **Amount** dataset field to the **Color saturation** field of the map visualization.</span></span>
    - <span data-ttu-id="6ef8c-226">将 **活动** 和 **年度** 数据集字段添加到地图可视化的 **筛选器** 字段集合。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-226">Add the **Activity** and **Year** dataset fields to the **Filters** fields collection of the map visualization.</span></span>

3. <span data-ttu-id="6ef8c-227">将 Power BI 报表保存为 **导入和导出详细报表**。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-227">Save the Power BI report as **Import and export details report**.</span></span>

    <span data-ttu-id="6ef8c-228">[![导入和导出详细报表](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-228">[![Import and export details report](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png)</span></span>

    <span data-ttu-id="6ef8c-229">注意地图显示 Excel 文件中提及的国家/地区（在此示例中为奥地利和瑞士）。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-229">Note that the map shows the countries/regions that are mentioned in the Excel file (Austria and Switzerland in this example).</span></span> <span data-ttu-id="6ef8c-230">这些国家/地区通过颜色显示每个国家/地区开票金额的比例。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-230">These countries/regions are colored to show the proportion of invoiced amounts for each.</span></span>

4. <span data-ttu-id="6ef8c-231">更新内部统计交易记录列表。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-231">Update the list of Intrastat transactions.</span></span> <span data-ttu-id="6ef8c-232">添加由意大利发起的导出交易记录。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-232">The export transaction that originated from Italy is added.</span></span>

    <span data-ttu-id="6ef8c-233">[![内部统计交易记录列表](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-233">[![Intrastat transactions list](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png)</span></span>

5. <span data-ttu-id="6ef8c-234">等待下一次计划的 ER 报表执行和下一次计划的 Power BI 数据集更新。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-234">Wait for the next scheduled execution of the ER report and the next scheduled update of the Power BI dataset.</span></span> <span data-ttu-id="6ef8c-235">然后查看 Power BI 报表（选择仅显示导入交易记录）。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-235">Then review the Power BI report (select to show import transactions only).</span></span> <span data-ttu-id="6ef8c-236">更新地图现在仅显示意大利。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-236">The updated map now shows Italy.</span></span>

    <span data-ttu-id="6ef8c-237">[![更新地图](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-237">[![Updated map](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)</span></span>

## <a name="access-power-bi-report-in-finance"></a><span data-ttu-id="6ef8c-238">在 Finance 中访问 Power BI 报表</span><span class="sxs-lookup"><span data-stu-id="6ef8c-238">Access Power BI report in Finance</span></span>
<span data-ttu-id="6ef8c-239">设置与 Power BI 的集成。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-239">Set up the integration with Power BI.</span></span> <span data-ttu-id="6ef8c-240">有关详细信息，请参阅[配置工作区的 Power BI 集成](configure-power-bi-integration.md)。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-240">For more information, see [Configure Power BI integration for workspaces](configure-power-bi-integration.md).</span></span>

1. <span data-ttu-id="6ef8c-241">在支持 Power BI 集成的 **电子申报** 工作区页面上（**组织管理** &gt; **工作区s** &gt; **电子申报工作区**），单击 **选项** &gt; **打开报表目录**。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-241">On the **Electronic reporting** workspace page that supports Power BI integration (**Organization administration** &gt; **Workspaces** &gt; **Electronic reporting workspace**), click **Options** &gt; **Open report catalog**.</span></span>
2. <span data-ttu-id="6ef8c-242">选择您创建的 **导入和导出详细信息** Power BI 报表使报表在选择的页面上显示为操作项。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-242">Select the **Import and export details** Power BI report that you created, to show that report as an action item on the selected page.</span></span>
3. <span data-ttu-id="6ef8c-243">单击操作项以打开显示您在 Power BI 中设计的报表的页面。</span><span class="sxs-lookup"><span data-stu-id="6ef8c-243">Click the action item to open the page that shows the report that you designed in Power BI.</span></span>

    <span data-ttu-id="6ef8c-244">[![在 Power BI 中设计的导入和导出详细报表](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)</span><span class="sxs-lookup"><span data-stu-id="6ef8c-244">[![Import and export details report designed in Power BI](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ef8c-245">其他资源</span><span class="sxs-lookup"><span data-stu-id="6ef8c-245">Additional resources</span></span>

[<span data-ttu-id="6ef8c-246">电子报告 (ER) 目标</span><span class="sxs-lookup"><span data-stu-id="6ef8c-246">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)

[<span data-ttu-id="6ef8c-247">电子申报 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="6ef8c-247">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

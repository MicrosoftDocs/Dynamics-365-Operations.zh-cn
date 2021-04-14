---
title: 业务文档管理概览
description: 本主题介绍有关如何使用 ER 框架的业务文档管理功能的信息。
author: NickSelin
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERSecurityAccessEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f5589925b7bfba3d9315c3828fd1ec5993a09a59
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749529"
---
# <a name="business-document-management-overview"></a><span data-ttu-id="80c19-103">业务文档管理概览</span><span class="sxs-lookup"><span data-stu-id="80c19-103">Business document management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80c19-104">业务用户使用[电子申报 (ER)](general-electronic-reporting.md) 框架根据各个国家/地区的法律要求配置传出文档的格式。</span><span class="sxs-lookup"><span data-stu-id="80c19-104">Business users use the [Electronic reporting (ER)](general-electronic-reporting.md) framework to configure formats for outbound documents in accordance with the legal requirements of various countries/regions.</span></span> <span data-ttu-id="80c19-105">用户也可以定义数据流，以便指定在生成的文档中放置哪些数据。</span><span class="sxs-lookup"><span data-stu-id="80c19-105">Users can also define the dataflow to specify what application data is placed in generated documents.</span></span> <span data-ttu-id="80c19-106">ER 框架使用预定义的模板生成 Microsoft Office 格式（Excel 工作簿或 Word 文档）格式的传出文档。</span><span class="sxs-lookup"><span data-stu-id="80c19-106">The ER framework generates outbound documents in Microsoft Office formats (Excel workbooks or Word documents) by using predefined templates.</span></span> <span data-ttu-id="80c19-107">将根据生成所需文档时配置的数据流使用必需数据填充模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-107">The templates are populated with required data in accordance to configured dataflow while required documents are generated.</span></span> <span data-ttu-id="80c19-108">可以在 ER 解决方案中发布配置的每种格式，以便生成特定传出文档。</span><span class="sxs-lookup"><span data-stu-id="80c19-108">Each configured format can be published as part of an ER solution to generate specific outbound documents.</span></span> <span data-ttu-id="80c19-109">这通过 ER 格式配置表示，其中可包含可用于生成不同传出文档的模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-109">This is represented by an ER format configuration that can contain templates you can use to generate different outbound documents.</span></span> <span data-ttu-id="80c19-110">业务用户可使用此框架管理所需业务文档。</span><span class="sxs-lookup"><span data-stu-id="80c19-110">Business users can use this framework to manage required business documents.</span></span>

<span data-ttu-id="80c19-111">**业务文档管理** 建立在 ER 框架的基础上，可供业务用户使用 Microsoft 365 服务或相应的 Microsoft Office 桌面应用程序编辑业务文档模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-111">**Business document management** is built on top of the ER framework and enables business users to edit business document templates by using Microsoft 365 service or appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="80c19-112">对此类文档的编辑包括在不执行源代码更改和不进行新部署的情况下，更改业务文档设计和为更多数据添加占位符。</span><span class="sxs-lookup"><span data-stu-id="80c19-112">Edits to the documents might include changing business document designs and adding placeholders for additional data without source code changes and new deployments.</span></span> <span data-ttu-id="80c19-113">若要更新业务文档模板，无需了解 ER 框架。</span><span class="sxs-lookup"><span data-stu-id="80c19-113">No knowledge of the ER framework is required to update templates of business documents.</span></span>

> [!NOTE]
> <span data-ttu-id="80c19-114">请注意，可通过业务文档管理修改用于生成订单、发票等之类业务文档的模板。修改模板和发布模板新版本之后，此版本用于生成必需的业务文档。</span><span class="sxs-lookup"><span data-stu-id="80c19-114">Be aware that Business document management allows you to modify templates that are used to produce business documents such as orders, invoices, etc. While a template has been modified and a new version of it has been published, this version is used to generate required business documents.</span></span> <span data-ttu-id="80c19-115">业务文档管理不可用于修改已生成的业务文档。</span><span class="sxs-lookup"><span data-stu-id="80c19-115">Business document management cannot be used to modify already generated business documents.</span></span>

## <a name="supported-deployments"></a><span data-ttu-id="80c19-116">支持的部署</span><span class="sxs-lookup"><span data-stu-id="80c19-116">Supported deployments</span></span>

<span data-ttu-id="80c19-117">现在，只能针对云部署实施业务文档管理功能。</span><span class="sxs-lookup"><span data-stu-id="80c19-117">Currently, the Business document management feature is implemented only for cloud deployments.</span></span> <span data-ttu-id="80c19-118">如果此功能对您的本地部署至关重要，请通过在[灵感](https://experience.dynamics.com/ideas/)站点提供反馈来告知我们。</span><span class="sxs-lookup"><span data-stu-id="80c19-118">If this feature is critical to your on-premises deployment, let us know by providing feedback on the [Ideas](https://experience.dynamics.com/ideas/) site.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="80c19-119">支持的 Microsoft Office 应用程序</span><span class="sxs-lookup"><span data-stu-id="80c19-119">Supported Microsoft Office applications</span></span>

<span data-ttu-id="80c19-120">若要使用业务文档管理和 Microsoft Office 桌面应用程序以 Excel 或 Word 格式编辑文档，则必须安装 Microsoft Office 2010 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="80c19-120">To use Business document management for editing templates in Excel or Word formats by using Microsoft Office desktop applications, you must have Microsoft Office 2010 or later installed.</span></span> <span data-ttu-id="80c19-121">这在云和本地部署中受支持。</span><span class="sxs-lookup"><span data-stu-id="80c19-121">This is supported in cloud and on-premises deployments.</span></span>

<span data-ttu-id="80c19-122">若要使用业务文档管理通过 Microsoft 365 应用程序以 Excel 或 Word 格式编辑模板，您必须有 Microsoft 365 Office 以获取 Web 订阅。</span><span class="sxs-lookup"><span data-stu-id="80c19-122">To use Business document management for editing templates in Excel or Word formats by using Microsoft 365 applications, you must have Microsoft 365 Office for the web subscription.</span></span> <span data-ttu-id="80c19-123">这在云部署中受支持。</span><span class="sxs-lookup"><span data-stu-id="80c19-123">This is supported in cloud deployment.</span></span>

## <a name="business-document-availability"></a><span data-ttu-id="80c19-124">业务文档可用性</span><span class="sxs-lookup"><span data-stu-id="80c19-124">Business document availability</span></span>

<span data-ttu-id="80c19-125">要获取为 2019 年 10 月发行版计划的所有报表的完整列表，请参阅 [Word 和 Excel 中的可配置业务文档报告](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details)。</span><span class="sxs-lookup"><span data-stu-id="80c19-125">For a complete list of all the reports planned for the October 2019 release, see [Configurable business documents reporting in Word and Excel](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details).</span></span>

<span data-ttu-id="80c19-126">要获取为 2020 年 10 月发行版计划的所有报表的完整列表，请参阅[可配置业务文档 – Word 模板](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-finance/configurable-business-documents-word-templates)。</span><span class="sxs-lookup"><span data-stu-id="80c19-126">For a complete list of all the reports planned for the October 2020 release, see [Configurable business documents – Word templates](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-finance/configurable-business-documents-word-templates).</span></span>

<span data-ttu-id="80c19-127">将来的发行版中将提供更多报表。</span><span class="sxs-lookup"><span data-stu-id="80c19-127">More reports will become available in future releases.</span></span> <span data-ttu-id="80c19-128">将单独发送有关更多报告的特殊通知。</span><span class="sxs-lookup"><span data-stu-id="80c19-128">Special notifications about additional reports will be sent separately.</span></span> <span data-ttu-id="80c19-129">要了解如何查看当前可用报表的列表，请参阅下面的 [Finance 中发布的支持可配置业务文档的 ER 配置列表](#list-of-configurations-cbd)一节。</span><span class="sxs-lookup"><span data-stu-id="80c19-129">To learn how to review the list of currently available reports, see the section [List of ER configurations that have been released in Finance to support configurable business documents](#list-of-configurations-cbd) below.</span></span>

<span data-ttu-id="80c19-130">若要了解有关此功能的详细信息，请完成本主题中的示例。</span><span class="sxs-lookup"><span data-stu-id="80c19-130">To learn more about this feature, complete the example in this topic.</span></span>

## <a name="configure-er-parameters"></a><span data-ttu-id="80c19-131">配置 ER 参数</span><span class="sxs-lookup"><span data-stu-id="80c19-131">Configure ER parameters</span></span>

<span data-ttu-id="80c19-132">因为业务文档管理建立在 ER 框架的基础上，所以必须配置 ER 参数，才能开始使用业务文档管理。</span><span class="sxs-lookup"><span data-stu-id="80c19-132">Because Business document management is built on top of the ER framework, you must configure the ER parameters to start working with Business document management.</span></span> <span data-ttu-id="80c19-133">为此，需要按照[配置电子报告 (ER) 框架](electronic-reporting-er-configure-parameters.md)中的说明设置 ER 参数。</span><span class="sxs-lookup"><span data-stu-id="80c19-133">To do this, you need to set up the ER parameters as described in [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md).</span></span> <span data-ttu-id="80c19-134">还需要按照[创建配置提供商并将其标记为有效](tasks/er-configuration-provider-mark-it-active-2016-11.md)中的说明添加新的配置提供商。</span><span class="sxs-lookup"><span data-stu-id="80c19-134">You also need to add a new configuration provider as described in [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

![ER 工作区](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a><span data-ttu-id="80c19-136">导入 ER 解决方案</span><span class="sxs-lookup"><span data-stu-id="80c19-136">Import ER solutions</span></span>

<span data-ttu-id="80c19-137">在此过程的示例中使用了示例 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="80c19-137">Sample ER configurations are used in the example of this procedure.</span></span> <span data-ttu-id="80c19-138">您必须将包含业务文档模板的 ER 配置导入到 Dynamics 365 Finance 的当前实例中，模板可以使用业务文档管理进行编辑。</span><span class="sxs-lookup"><span data-stu-id="80c19-138">You must import, into your current instance of Dynamics 365 Finance, the ER configurations that contain the business document templates that can be edited by using Business document management.</span></span> <span data-ttu-id="80c19-139">下载以下文件，然后存储在本地，以完成此过程。</span><span class="sxs-lookup"><span data-stu-id="80c19-139">Download, and then locally store the following files to complete this procedure.</span></span>

<span data-ttu-id="80c19-140">**示例 ER 客户开票解决方案**</span><span class="sxs-lookup"><span data-stu-id="80c19-140">**Sample ER customer invoicing solution**</span></span>

| <span data-ttu-id="80c19-141">文件</span><span class="sxs-lookup"><span data-stu-id="80c19-141">File</span></span>                                      | <span data-ttu-id="80c19-142">内容</span><span class="sxs-lookup"><span data-stu-id="80c19-142">Content</span></span> |
|-------------------------------------------|---------|
| <span data-ttu-id="80c19-143">Customer invoicing model.version.2.xml</span><span class="sxs-lookup"><span data-stu-id="80c19-143">Customer invoicing model.version.2.xml</span></span>    | [<span data-ttu-id="80c19-144">ER 数据模型配置</span><span class="sxs-lookup"><span data-stu-id="80c19-144">ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="80c19-145">Customer FTI report (GER).version.2.3.xml</span><span class="sxs-lookup"><span data-stu-id="80c19-145">Customer FTI report (GER).version.2.3.xml</span></span> | [<span data-ttu-id="80c19-146">普通发票 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="80c19-146">Free text invoice ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

<span data-ttu-id="80c19-147">**示例 ER 付款检查解决方案**</span><span class="sxs-lookup"><span data-stu-id="80c19-147">**Sample ER payment checks solution**</span></span>

| <span data-ttu-id="80c19-148">文件</span><span class="sxs-lookup"><span data-stu-id="80c19-148">File</span></span>                                     | <span data-ttu-id="80c19-149">内容</span><span class="sxs-lookup"><span data-stu-id="80c19-149">Content</span></span> |
|------------------------------------------|---------|
| <span data-ttu-id="80c19-150">Model for cheques.version.10.xml</span><span class="sxs-lookup"><span data-stu-id="80c19-150">Model for cheques.version.10.xml</span></span>         | [<span data-ttu-id="80c19-151">ER 数据模型配置</span><span class="sxs-lookup"><span data-stu-id="80c19-151">ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="80c19-152">Cheques printing format.version.10.9.xml</span><span class="sxs-lookup"><span data-stu-id="80c19-152">Cheques printing format.version.10.9.xml</span></span> | [<span data-ttu-id="80c19-153">付款支票 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="80c19-153">Payment cheque ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

<span data-ttu-id="80c19-154">**示例 ER 外贸解决方案**</span><span class="sxs-lookup"><span data-stu-id="80c19-154">**Sample ER foreign trade solution**</span></span>

| <span data-ttu-id="80c19-155">文件</span><span class="sxs-lookup"><span data-stu-id="80c19-155">File</span></span>                             | <span data-ttu-id="80c19-156">内容</span><span class="sxs-lookup"><span data-stu-id="80c19-156">Content</span></span> |
|----------------------------------|---------|
| <span data-ttu-id="80c19-157">Intrastat model.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="80c19-157">Intrastat model.version.1.xml</span></span>    | [<span data-ttu-id="80c19-158">ER 数据模型配置</span><span class="sxs-lookup"><span data-stu-id="80c19-158">ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="80c19-159">Intrastat report.version.1.9.xml</span><span class="sxs-lookup"><span data-stu-id="80c19-159">Intrastat report.version.1.9.xml</span></span> | [<span data-ttu-id="80c19-160">内部统计控制报表 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="80c19-160">Intrastat control report ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

<span data-ttu-id="80c19-161">使用以下过程导入每个文件。</span><span class="sxs-lookup"><span data-stu-id="80c19-161">Use the following procedure to import each file.</span></span> <span data-ttu-id="80c19-162">导入相应 ER *格式* 配置之前，导入上表中每个 ER 解决方案的 ER *数据模型* 配置。</span><span class="sxs-lookup"><span data-stu-id="80c19-162">Import the ER *data model* configuration of each ER solution in the tables above before you import the corresponding ER *format* configuration.</span></span>

1. <span data-ttu-id="80c19-163">打开 **组织管理** \> **电子申报** \> **配置** 页面。</span><span class="sxs-lookup"><span data-stu-id="80c19-163">Open the **Organization administration** \> **Electronic reporting** \> **Configurations** page.</span></span>
2. <span data-ttu-id="80c19-164">在页面顶部，选择 **交易**。</span><span class="sxs-lookup"><span data-stu-id="80c19-164">On the top of the page, select **Exchange**.</span></span>
3. <span data-ttu-id="80c19-165">选择 **从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="80c19-165">Select **Load from XML file**.</span></span>
4. <span data-ttu-id="80c19-166">选择 **浏览** 以加载所需的 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="80c19-166">Select **Browse** to load the required XML file.</span></span>
5. <span data-ttu-id="80c19-167">选择 **确定** 以确认导入配置。</span><span class="sxs-lookup"><span data-stu-id="80c19-167">Select **OK** to confirm configuration's import.</span></span>

![确认配置导入的 ER 配置页面](./media/BDM-Overview-ERSolutions.png)

<span data-ttu-id="80c19-169">或者，您可以从 Microsoft Dynamics Lifecycle Service (LCS) 导入正式发布的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="80c19-169">Alternatively, you can import the officially published ER format configurations from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="80c19-170">例如，要完成此过程，您可以导入 **普通发票(Excel)** ER 格式配置的最新版本。</span><span class="sxs-lookup"><span data-stu-id="80c19-170">For example, to complete this procedure you can import the latest version of the **Free text invoice (Excel)** ER format configuration.</span></span> <span data-ttu-id="80c19-171">相应的 ER 数据模型和 ER 模型映射配置将自动导入。</span><span class="sxs-lookup"><span data-stu-id="80c19-171">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

![LCS 共享资产库内容页面](./media/BDM-Overview-SharedAssetLibrary.png)

<span data-ttu-id="80c19-173">有关导入 ER 配置的详细信息，请参阅[管理 ER 配置生命周期](general-electronic-reporting-manage-configuration-lifecycle.md)。</span><span class="sxs-lookup"><span data-stu-id="80c19-173">For more information about importing ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

## <a name="enable-business-document-management"></a><span data-ttu-id="80c19-174">启用业务文档管理</span><span class="sxs-lookup"><span data-stu-id="80c19-174">Enable Business document management</span></span>

<span data-ttu-id="80c19-175">若要启动业务文档管理，需要打开 **功能管理** 工作区，并启用 **业务文档管理** 功能。</span><span class="sxs-lookup"><span data-stu-id="80c19-175">To start Business document management, you need to open the **Feature management** workspace and enable the **Business document management** feature.</span></span>

<span data-ttu-id="80c19-176">使用以下过程为所有法人启用业务文档管理。</span><span class="sxs-lookup"><span data-stu-id="80c19-176">Use the following procedure to enable Business document management functionality for all legal entities.</span></span>

1. <span data-ttu-id="80c19-177">打开 **功能管理** 工作区。</span><span class="sxs-lookup"><span data-stu-id="80c19-177">Open the **Feature management** workspace.</span></span>
2. <span data-ttu-id="80c19-178">在 **新建** 选项卡上，选择列表中的 **业务文档管理** 功能。</span><span class="sxs-lookup"><span data-stu-id="80c19-178">On the **New** tab, select the **Business document management** feature in the list.</span></span>
3. <span data-ttu-id="80c19-179">选择 **立即启用** 以打开所选功能。</span><span class="sxs-lookup"><span data-stu-id="80c19-179">Select **Enable now** to turn on the selected feature.</span></span>
4. <span data-ttu-id="80c19-180">刷新页面以访问新功能。</span><span class="sxs-lookup"><span data-stu-id="80c19-180">Refresh the page to access the new feature.</span></span>

> [!NOTE]
> <span data-ttu-id="80c19-181">有关使用业务文档管理中的新文档用户界面的更多信息，请参见[业务文档管理中的新文档用户界面](er-business-document-management-new-template-ui.md)。</span><span class="sxs-lookup"><span data-stu-id="80c19-181">For more information about using the new document user interface in Business document management, see [New document user interface in Business document management](er-business-document-management-new-template-ui.md).</span></span>

![“功能管理”工作区](./media/BDM-Overview-FMEnabling.png)

<span data-ttu-id="80c19-183">有关激活新功能的详细信息，请参阅[功能管理概述](../../fin-ops/get-started/feature-management/feature-management-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="80c19-183">For more information about activating new features, see [Feature management overview](../../fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-parameters"></a><span data-ttu-id="80c19-184">配置参数</span><span class="sxs-lookup"><span data-stu-id="80c19-184">Configure parameters</span></span>

<span data-ttu-id="80c19-185">使用以下部分中的信息为业务文档管理设置基本参数。</span><span class="sxs-lookup"><span data-stu-id="80c19-185">Use the information in the following sections to set up the basic parameters for Business document management.</span></span>

### <a name="prerequisites-for-parameter-setup"></a><span data-ttu-id="80c19-186">参数设置的先决条件</span><span class="sxs-lookup"><span data-stu-id="80c19-186">Prerequisites for parameter setup</span></span>

<span data-ttu-id="80c19-187">必须先在文档管理框架中设置必需的文档类型，才能设置业务文档管理。</span><span class="sxs-lookup"><span data-stu-id="80c19-187">Before you can set up Business document management, you must set up the required document type in the Document management framework.</span></span> <span data-ttu-id="80c19-188">此文档类型用于指定 Office 格式（Excel 和 Word）文档的临时存储，用作 ER 报表的模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-188">This document type is used to specify a temporary storage of documents in Office formats (Excel and Word) that are used as templates for ER reports.</span></span> <span data-ttu-id="80c19-189">可使用 Office 桌面应用程序编辑临时存储模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-189">The temporary storage template can be edited by using the Office desktop applications.</span></span>

<span data-ttu-id="80c19-190">对于此文档类型，必须选择以下属性值。</span><span class="sxs-lookup"><span data-stu-id="80c19-190">For this document type, the following attribute values must be selected.</span></span>

| <span data-ttu-id="80c19-191">属性名称</span><span class="sxs-lookup"><span data-stu-id="80c19-191">Attribute name</span></span> | <span data-ttu-id="80c19-192">属性值</span><span class="sxs-lookup"><span data-stu-id="80c19-192">Attribute value</span></span> |
|----------------|-----------------|
| <span data-ttu-id="80c19-193">分类</span><span class="sxs-lookup"><span data-stu-id="80c19-193">Class</span></span>          | <span data-ttu-id="80c19-194">附加文件</span><span class="sxs-lookup"><span data-stu-id="80c19-194">Attach file</span></span>     |
| <span data-ttu-id="80c19-195">组合</span><span class="sxs-lookup"><span data-stu-id="80c19-195">Group</span></span>          | <span data-ttu-id="80c19-196">文件</span><span class="sxs-lookup"><span data-stu-id="80c19-196">File</span></span>            |
| <span data-ttu-id="80c19-197">场所</span><span class="sxs-lookup"><span data-stu-id="80c19-197">Location</span></span>       | <span data-ttu-id="80c19-198">SharePoint</span><span class="sxs-lookup"><span data-stu-id="80c19-198">SharePoint</span></span>      |

<span data-ttu-id="80c19-199">有关如何设置必需文档管理参数和文档类型的信息，请参阅[配置文档管理](../../fin-ops/organization-administration/configure-document-management.md)。</span><span class="sxs-lookup"><span data-stu-id="80c19-199">For information about how to set up the required document management parameters and document types, see [Configure document management](../../fin-ops/organization-administration/configure-document-management.md).</span></span>

![设置文档管理文档类型](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a><a name="SetupBdmParameters"></a><span data-ttu-id="80c19-201">设置参数</span><span class="sxs-lookup"><span data-stu-id="80c19-201">Set up parameters</span></span>

<span data-ttu-id="80c19-202">可在 **业务文档参数** 页设置基本业务文档管理参数。</span><span class="sxs-lookup"><span data-stu-id="80c19-202">Basic Business document management parameters can be set up on the **Business document parameters** page.</span></span> <span data-ttu-id="80c19-203">只有特定用户才可以访问此页。</span><span class="sxs-lookup"><span data-stu-id="80c19-203">Only specific users can access the page.</span></span> <span data-ttu-id="80c19-204">这包括：</span><span class="sxs-lookup"><span data-stu-id="80c19-204">This includes:</span></span>

- <span data-ttu-id="80c19-205">已为其分配了 **系统管理员** 角色的用户。</span><span class="sxs-lookup"><span data-stu-id="80c19-205">Users who are assigned to the **System administrator** role.</span></span>
- <span data-ttu-id="80c19-206">已为其分配了为执行 **维护业务文档管理参数**（AOT 名称为 **ERBDMaintainParameters**）职责而配置的任何角色的用户。</span><span class="sxs-lookup"><span data-stu-id="80c19-206">Users who are assigned to any role that is configured to perform the duty, **Maintain Business document management parameters** (AOT name **ERBDMaintainParameters**).</span></span>

<span data-ttu-id="80c19-207">使用以下过程为所有法人设置基本参数。</span><span class="sxs-lookup"><span data-stu-id="80c19-207">Use the following procedure to set up the basic parameters for all legal entities.</span></span>

1. <span data-ttu-id="80c19-208">以具有 **业务文档参数** 页面访问权限的用户的身份登录。</span><span class="sxs-lookup"><span data-stu-id="80c19-208">Sign in as a user with access to the **Business document parameters** page.</span></span>
2. <span data-ttu-id="80c19-209">转到 **组织管理** \> **电子申报** \> **业务文档管理** \> **业务文档参数**。</span><span class="sxs-lookup"><span data-stu-id="80c19-209">Go to **Organization administration** \> **Electronic reporting** \> **Business document management** \> **Business document parameters**.</span></span>
3. <span data-ttu-id="80c19-210">在 **业务文档参数** 页 **附件** 选项卡的 **SharePoint 文档类型** 字段中，定义应该用于在使用 Office 桌面应用程序编辑 Office 格式的模板时，临时存储此类模板的文档类型。</span><span class="sxs-lookup"><span data-stu-id="80c19-210">On the **Business document parameters** page, on the **Attachments** tab, in the **SharePoint document type** field, define the document type that should be used to temporarily store templates in Office formats while they are edited using the Office desktop applications.</span></span> 

> [!NOTE]
> <span data-ttu-id="80c19-211">此参数仅支持使用 SharePoint 位置配置的文档类型。</span><span class="sxs-lookup"><span data-stu-id="80c19-211">Only document types that are configured using a SharePoint location are available for this parameter.</span></span>

![设置业务文档管理参数](./media/BDM-Overview-BDMSetting.png)

<span data-ttu-id="80c19-213">所选文档类型特定于公司，将在当用户在为其配置了所选文档类型的公司中使用业务文档管理时使用。</span><span class="sxs-lookup"><span data-stu-id="80c19-213">The selected document type is company-specific and will be used when the user is working with Business document management in the company for which the selected document type is configured.</span></span> <span data-ttu-id="80c19-214">当用户在另一家公司使用业务文档管理时，如果尚未为此公司配置文档类型，将使用选择的同一个文档类型。</span><span class="sxs-lookup"><span data-stu-id="80c19-214">When the user is working with Business document management in another company, the same selected document type will be used if one has not been configured for this company.</span></span> <span data-ttu-id="80c19-215">如果已配置了文档类型，则使用此文档类型，而不是在 **SharePoint 文档类型** 字段中选择的文档类型。</span><span class="sxs-lookup"><span data-stu-id="80c19-215">When a document type has been configured, it will be used instead of the one selected in the **SharePoint document type** field.</span></span>

> [!NOTE]
> <span data-ttu-id="80c19-216">**SharePoint 文档类型** 参数将 SharePoint 文件夹定义为可使用 Microsoft Excel 或 Word 进行编辑的模板的临时存储。</span><span class="sxs-lookup"><span data-stu-id="80c19-216">The **SharePoint document type** parameter defines a SharePoint folder as temporary storage for templates that are editable using either Microsoft Excel or Word.</span></span> <span data-ttu-id="80c19-217">如果打算使用这些 Office 桌面应用程序来编辑模板，则需要设置此参数。</span><span class="sxs-lookup"><span data-stu-id="80c19-217">You need to set up this parameter if you plan to use these Office desktop applications for editing templates.</span></span> <span data-ttu-id="80c19-218">有关更多信息，请参见[在 Office 桌面应用程序中编辑模板](#EditInOfficeDesktopApp)。</span><span class="sxs-lookup"><span data-stu-id="80c19-218">For more information, see [Edit a template in the Office desktop application](#EditInOfficeDesktopApp).</span></span> <span data-ttu-id="80c19-219">如果您打算仅使用 Microsoft 365 中的功能来修改模板，则可以将此参数保留为空白。</span><span class="sxs-lookup"><span data-stu-id="80c19-219">You can keep this parameter blank if you plan to modify the template by only using the functionality in Microsoft 365.</span></span> <span data-ttu-id="80c19-220">有关详细信息，请参阅[在 Microsoft 365 中编辑模板](#EditInOffice365)。</span><span class="sxs-lookup"><span data-stu-id="80c19-220">For more information, see [Edit a template in Microsoft 365](#EditInOffice365).</span></span>

## <a name="configure-access-permissions"></a><span data-ttu-id="80c19-221">配置访问权限</span><span class="sxs-lookup"><span data-stu-id="80c19-221">Configure access permissions</span></span>

<span data-ttu-id="80c19-222">默认情况下，在未启用业务文档管理权限的访问时，每位可访问业务文档管理工作区的用户都可以看到所有可用 ER 解决方案模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-222">By default, when access to Business document management permissions is not enabled, every user with access to the Business document management workspace will see all of the ER solution templates that are available.</span></span> <span data-ttu-id="80c19-223">业务文档管理工作区将仅显示 ER 格式配置中的模板和带有 **业务文档类型** 标记的模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-223">The Business document management workspace will show only those templates that reside in ER format configurations and that are marked by a **Business document type** tag.</span></span>

![带有业务文档类型标记的 ER 配置页面](./media/BDM-Overview-ERFormatTags.png)

<span data-ttu-id="80c19-225">可通过配置访问权限来限制业务文档管理工作区中的可用模板的列表。</span><span class="sxs-lookup"><span data-stu-id="80c19-225">The list of templates available in the Business document management workspace can be restricted by configuring access permissions.</span></span> <span data-ttu-id="80c19-226">这在以下情况下可能非常重要：使用不同模板为不同业务域（功能区）生成业务文档，并且要允许特定用户访问要在业务文档管理工作区中进行编辑的不同模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-226">This may be important when different templates are used to produce business documents for different business domains (functional areas), and you want to allow specific users access to different templates for editing in the Business document management workspace.</span></span>

<span data-ttu-id="80c19-227">可在 **配置权限的配置器** 中设置业务文档管理访问权限。</span><span class="sxs-lookup"><span data-stu-id="80c19-227">Business document management access permissions can be set on the **Configurator of access permissions**.</span></span> <span data-ttu-id="80c19-228">只有以下用户才可以访问此页：</span><span class="sxs-lookup"><span data-stu-id="80c19-228">Only the following users can access the page:</span></span>

- <span data-ttu-id="80c19-229">已为其分配了 **系统管理员** 角色的用户。</span><span class="sxs-lookup"><span data-stu-id="80c19-229">Users assigned to the **System administrator** role.</span></span>
- <span data-ttu-id="80c19-230">已为其分配了为执行 **配置权限以访问要编辑的业务文档模板**（AOT 名称为 **ERBDTemplatesSecurity**）职责而配置的其他任何角色的用户。</span><span class="sxs-lookup"><span data-stu-id="80c19-230">Users assigned to any other role that is configured to perform the duty, **Configure permissions to access Business document templates for editing** (AOT name **ERBDTemplatesSecurity**).</span></span>

<span data-ttu-id="80c19-231">使用以下过程为所有法人设置业务文档管理访问权限。</span><span class="sxs-lookup"><span data-stu-id="80c19-231">Use the following procedure to set up the access Business document management permissions for all legal entities.</span></span>

1. <span data-ttu-id="80c19-232">以具有 **访问权限配置器** 页面访问权限的用户的身份登录。</span><span class="sxs-lookup"><span data-stu-id="80c19-232">Sign in as a user with access to the **Configurator of access permissions** page.</span></span>
2. <span data-ttu-id="80c19-233">转到 **组织管理** \> **电子申报** \> **业务文档管理** \> **管理访问权限**。</span><span class="sxs-lookup"><span data-stu-id="80c19-233">Go to **Organization administration** \> **Electronic reporting** \> **Business document management** \> **Manage access permissions**.</span></span>

    <span data-ttu-id="80c19-234">请注意有关当前未启用业务文档管理访问权限的使用的通知。</span><span class="sxs-lookup"><span data-stu-id="80c19-234">Pay attention to the notification informing you that the usage of access permissions for Business document management is currently not enabled.</span></span>

    ![“业务文档管理访问权限配置器”页面](./media/BDM-Overview-TemplatesAccess1.png)

    <span data-ttu-id="80c19-236">通过此设置，已为其分配了为执行 **管理业务文档模板**（AOT 名称为 **ERBDManageTemplates**）职责而配置的任何安全角色的每位用户都可以打开业务文档管理工作区，并可编辑所有可用模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-236">With this setting, every user assigned to any security role that is configured to perform the **Manage Business document templates** (AOT name **ERBDManageTemplates**) duty is able to open the Business document management workspace and can edit any template that is available.</span></span>

    <span data-ttu-id="80c19-237">下图显示业务文档管理工作区中为其分配了 **应收帐款员** 角色的用户的可用模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-237">The following graphic shows what is available in the Business document management workspace for users assigned to the **Accounts receivable clerk** role.</span></span> <span data-ttu-id="80c19-238">通过使用当前访问权限设置，用户可从不同功能区（包括开票、法规报告和付款）编辑业务文档模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-238">With the current access permissions setting, the user can edit business document templates from different functional areas including invoicing, regulatory reporting, and payments.</span></span>

    ![应收帐款员的业务文档管理工作区页面](./media/BDM-Overview-TemplatesForAlice1.png)

3. <span data-ttu-id="80c19-240">在 **访问权限配置器** 页，选择 **访问权限设置**。</span><span class="sxs-lookup"><span data-stu-id="80c19-240">On the **Configurator of access permissions** page, select **Access permissions setting**.</span></span>
4. <span data-ttu-id="80c19-241">在 **用于编辑模板的访问权限的设置** 对话框中，启用 **应用已配置的访问权限** 选项。</span><span class="sxs-lookup"><span data-stu-id="80c19-241">In the **Settings of access permissions to edit templates** dialog box, enable the **Apply configured access permissions** option.</span></span>
5. <span data-ttu-id="80c19-242">选择 **确定** 以确认已启用业务文档管理访问权限。</span><span class="sxs-lookup"><span data-stu-id="80c19-242">Select **OK** to confirm that Business document management access permissions have been enabled.</span></span>

    ![确认业务文档管理访问权限](./media/BDM-Overview-TemplatesAccess2.png)

6. <span data-ttu-id="80c19-244">选择 **添加** 以输入必须要为其配置用于访问业务文档管理模板的权限的新业务角色。</span><span class="sxs-lookup"><span data-stu-id="80c19-244">Select **Add** to enter a new business role for which permissions to access Business document management templates must be configured.</span></span>
7. <span data-ttu-id="80c19-245">在 **安全角色** 对话框中，选择 **应收帐款员** 角色，然后选择 **确定** 以确认选择的角色。</span><span class="sxs-lookup"><span data-stu-id="80c19-245">In the **Security roles** dialog box, select the **Accounts receivable clerk** role and then select **OK** to confirm the role selection.</span></span>
8. <span data-ttu-id="80c19-246">在 **每个配置标记的访问权限** 选项卡上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="80c19-246">On the **Access permissions per tags of configurations** tab, select **New**.</span></span>
9. <span data-ttu-id="80c19-247">在 **标记类型** 字段中，选择 **功能区**，然后在 **ID** 字段中选择 **开票**。</span><span class="sxs-lookup"><span data-stu-id="80c19-247">In the **Tag type** field, select **Functional area**, and in the **ID** field, select **Invoicing**.</span></span>
10. <span data-ttu-id="80c19-248">选择 **保存** 以存储为所选角色配置的访问权限。</span><span class="sxs-lookup"><span data-stu-id="80c19-248">Select **Save** to store configured access permissions for the selected role.</span></span>

    <span data-ttu-id="80c19-249">当前设置意味着对于为其分配了 **应收帐款员** 角色且正在执行 **管理业务文档模板**（AOT 名称为 **ERBDManageTemplates**）职责的任何用户，可在业务文档管理工作区中编辑 **功能区** 标记值为 **开票** 的 ER 格式配置模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-249">The current setting means that for any user who is assigned to the **Accounts receivable clerk** role and performing the duty, **Manage Business document templates** (AOT name **ERBDManageTemplates**), ER format configuration templates that have the **Invoicing** value for the **Functional area** tag will be available to edit in the Business document management workspace.</span></span>

11. <span data-ttu-id="80c19-250">从当前页右侧切换 **相关信息** 窗格。</span><span class="sxs-lookup"><span data-stu-id="80c19-250">Switch the **Related information** pane from the right side of the current page.</span></span> <span data-ttu-id="80c19-251">**相关信息** 窗格显示如何应用配置的访问权限，包括为其分配了 **应收帐款员** 角色的用户可使用哪些 ER 配置模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-251">The **Related information** pane shows how the configured access permissions will be applied, including what ER configuration templates will be available for users that are assigned to the **Accounts receivable clerk** role.</span></span>

    ![访问权限配置器页上的“相关信息”窗格](./media/BDM-Overview-TemplatesAccess3.png)

12. <span data-ttu-id="80c19-253">在 **每个配置的访问权限** 选项卡上，选择 **添加** 选项。</span><span class="sxs-lookup"><span data-stu-id="80c19-253">On the **Access permissions per configurations** tab, select the **Add** option.</span></span>
13. <span data-ttu-id="80c19-254">在 **选择配置** 对话框中，标记 **内部统计报表** ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="80c19-254">In the **Select configuration** dialog box, mark the **Intrastat report** ER format configuration.</span></span>
14. <span data-ttu-id="80c19-255">选择 **确定** 以确认所选配置的条目，然后选择 **保存** 以存储为所选角色配置的访问权限。</span><span class="sxs-lookup"><span data-stu-id="80c19-255">Select **OK** to confirm the entry of the selected configurations and then select **Save** to store the configured access permissions for the selected role.</span></span>

<span data-ttu-id="80c19-256">当前设置意味着对于为其分配了 **应收帐款员** 角色且正在执行 **管理业务文档模板**（AOT 名称为 **ERBDManageTemplates**）职责的任何用户，可在业务文档管理工作区中编辑以下模板：</span><span class="sxs-lookup"><span data-stu-id="80c19-256">The current setting means that for any user assigned to the **Accounts receivable clerk** role and performing the duty, **Manage Business document templates** (AOT name **ERBDManageTemplates**), the following templates will be available to edit in the Business document management workspace:</span></span>

- <span data-ttu-id="80c19-257">**功能区** 标记的值为 **开票** 的模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-257">Templates that have the value, **Invoicing** for the **Functional area** tag.</span></span>
- <span data-ttu-id="80c19-258">来自 **每个配置的访问权限** 选项卡上列出的 ER 格式配置的模板（此示例中，为来自 **法定申报** 域的 **内部统计报表** 格式配置的模板）。</span><span class="sxs-lookup"><span data-stu-id="80c19-258">Templates from ER format configurations that are listed on the **Access permissions per configurations** tab (templates from the **Intrastat report** format configuration of the **Statutory reporting** domain in this example).</span></span>

![访问权限配置器页上的“访问权限”快速选项卡](./media/BDM-Overview-TemplatesAccess4.png)

<span data-ttu-id="80c19-260">下图显示业务文档管理工作区向为其分配了 **应收帐款员** 角色的用户提供的模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-260">The following graphic shows what the Business document management workspace provides to a user assigned to the **Accounts receivable clerk** role.</span></span> <span data-ttu-id="80c19-261">采用当前业务文档管理访问权限设置的用户可编辑 **开票** 域和 **内部统计报表** ER 格式配置中的业务文档模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-261">With the current Business document management access permissions setting, the user can edit business document templates from the **Invoicing** domain and the **Intrastat report** ER format configuration.</span></span> <span data-ttu-id="80c19-262">**应收帐款员** 角色不可访问 **付款** 域中的模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-262">Templates from the **Payments** domain are not accessible for the **Accounts receivable clerk** role.</span></span>

![在业务文档管理工作区页上编辑业务文档模板](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> <span data-ttu-id="80c19-264">**每个配置的访问权限** 规则通过使用 ER 格式配置的唯一标识 ID 来存储。</span><span class="sxs-lookup"><span data-stu-id="80c19-264">The **Access permissions per configurations** rules are stored by using the unique identification ID of an ER format configuration.</span></span> <span data-ttu-id="80c19-265">这意味着如果删除引用这些规则的 ER 配置，不会删除这些规则。</span><span class="sxs-lookup"><span data-stu-id="80c19-265">This means that these rules will not be deleted when an ER configuration that refers to them are deleted.</span></span> <span data-ttu-id="80c19-266">将删除的配置导入回此实例时，这些规则将再次引用这些配置。</span><span class="sxs-lookup"><span data-stu-id="80c19-266">When you import deleted configurations back to this instance, these rules will refer to them again.</span></span> <span data-ttu-id="80c19-267">再次导入删除的配置之后，无需再次设置规则。</span><span class="sxs-lookup"><span data-stu-id="80c19-267">There is no need to set up the rules again after the deleted configurations are imported again.</span></span>

## <a name="use-business-document-management-to-edit-templates"></a><span data-ttu-id="80c19-268">使用业务文档管理编辑模板</span><span class="sxs-lookup"><span data-stu-id="80c19-268">Use Business document management to edit templates</span></span>

<span data-ttu-id="80c19-269">业务用户可在业务文档管理工作区中访问要编辑的业务文档模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-269">Business users can access business document templates for editing in the Business document management workspace.</span></span> <span data-ttu-id="80c19-270">只有以下用户可访问业务文档管理工作区：</span><span class="sxs-lookup"><span data-stu-id="80c19-270">Only the following users can access the Business document management workspace:</span></span>

- <span data-ttu-id="80c19-271">已为其分配了 **系统管理员** 角色的用户。</span><span class="sxs-lookup"><span data-stu-id="80c19-271">Users assigned to the role, **System administrator**.</span></span>
- <span data-ttu-id="80c19-272">已为其分配了为执行 **管理业务文档模板**（AOT 名称为 **ERBDManageTemplates**）职责而配置的任何角色的用户。</span><span class="sxs-lookup"><span data-stu-id="80c19-272">Users assigned to any role that is configured to perform the duty, **Manage Business document templates** (AOT name **ERBDManageTemplates**).</span></span>

<span data-ttu-id="80c19-273">在业务文档管理工作区中使用以下过程编辑普通发票模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-273">Use the following procedure to edit free text invoice templates in the Business document management workspace.</span></span> <span data-ttu-id="80c19-274">完成此过程之前，必须先完成本主题中前文的所有过程。</span><span class="sxs-lookup"><span data-stu-id="80c19-274">Before you complete this procedure, you must have completed all of the preceding procedures in this topic.</span></span>

1. <span data-ttu-id="80c19-275">以具有业务文档管理工作区访问权限的用户的身份登录。</span><span class="sxs-lookup"><span data-stu-id="80c19-275">Sign in as a user with access to the Business document management workspace.</span></span>
2. <span data-ttu-id="80c19-276">打开业务文档管理工作区。</span><span class="sxs-lookup"><span data-stu-id="80c19-276">Open the Business document management workspace.</span></span>

<span data-ttu-id="80c19-277">在 **功能管理** 工作区中关闭了 **类似于 Office 的业务文档管理 UI 体验** 功能之后，**业务文档管理** 工作区的主网格中将显示以下模板：</span><span class="sxs-lookup"><span data-stu-id="80c19-277">When the **Office-like UI experience for Business document management** feature is turned off in the **Feature management** workspace, the main grid in the **Business document management** workspace shows the following templates:</span></span>

- <span data-ttu-id="80c19-278">ER 配置提供商（即 **电子申报** 工作区中当前标记为可用的提供商）负责的模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-278">Templates that are owned by your ER configuration provider (that is, the provider that is currently marked as active in the **Electronic reporting** workspace).</span></span> <span data-ttu-id="80c19-279">选择这些模板之一后，可以选择 **编辑模板** 开始或继续编辑该模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-279">After you select one of these templates, you can select **Edit template** to start or continue to edit it.</span></span>
- <span data-ttu-id="80c19-280">其他 ER 配置提供商负责的模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-280">Templates that are owned by other ER configuration providers.</span></span> <span data-ttu-id="80c19-281">选择这些模板之一后，可以选择 **新建文档** 创建 ER 配置提供商负责的模板的副本，然后开始编辑该副本。</span><span class="sxs-lookup"><span data-stu-id="80c19-281">After you select one of these templates, you can select **New document** to create a copy of it that is owned by your ER configuration provider, and then start to edit the copy.</span></span>

![业务文档管理工作区页上的模板列表](./media/BDM-Overview-EditingTemplate1.png)

<span data-ttu-id="80c19-283">**模板** 选项卡中提供所选模板的内容。</span><span class="sxs-lookup"><span data-stu-id="80c19-283">The **Template** tab presents the content of the selected template.</span></span> <span data-ttu-id="80c19-284">选择 **详细信息** 选项卡以查看所选模板的详细信息，以及此模板所在 ER 格式配置的详细信息。</span><span class="sxs-lookup"><span data-stu-id="80c19-284">Select the **Details** tab to review details of the selected template as well as details of an ER format configuration this template resides in.</span></span> <span data-ttu-id="80c19-285">请注意，所有模板的状态均为 **已发布**，并且其 **修订** 列中不包含任何详细信息。</span><span class="sxs-lookup"><span data-stu-id="80c19-285">Notice that all of the templates have a status of **Published**, and contain no details in the **Revision** column.</span></span> <span data-ttu-id="80c19-286">这表示当前未在编辑这些模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-286">This means that these templates are not currently being edited.</span></span>

<span data-ttu-id="80c19-287">如果在 **功能管理** 中开启了 **类似于 Office 的业务文档管理 UI 体验** 功能，则 **业务文档管理** 工作区中的主网格显示您的 ER 配置提供商（即 **电子申报** 工作区中标记为可用的提供商）负责的模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-287">When the **Office-like UI experience for Business document management** feature is turned on in the **Feature management** workspace, the main grid in the **Business document management** workspace shows templates that are owned by your ER configuration provider (that is, the provider that is currently marked as active in the **Electronic reporting** workspace).</span></span> <span data-ttu-id="80c19-288">选择这些模板之一后，可以选择 **编辑模板** 开始或继续编辑该模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-288">After you select one of these templates, you can select **Edit template** to start or continue to edit it.</span></span>

<span data-ttu-id="80c19-289">若要使用其他 ER 配置提供商负责的模板，请选择 **新建文档** 创建您的 ER 提供商负责的模板的副本。</span><span class="sxs-lookup"><span data-stu-id="80c19-289">To work with templates that are owned by other ER configuration providers, select **New document** to create a copy of the template that is owned by your ER provider.</span></span> <span data-ttu-id="80c19-290">然后就可以开始编辑该副本。</span><span class="sxs-lookup"><span data-stu-id="80c19-290">You can then start to edit the copy.</span></span> <span data-ttu-id="80c19-291">有关详细信息，请参阅[业务文档管理中的新文档用户界面](er-business-document-management-new-template-ui.md)。</span><span class="sxs-lookup"><span data-stu-id="80c19-291">For more information, see [New document user interface in Business document management](er-business-document-management-new-template-ui.md).</span></span>

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a><span data-ttu-id="80c19-292">开始编辑配置提供商负责的模板</span><span class="sxs-lookup"><span data-stu-id="80c19-292">Initiate editing templates owned by your configuration provider</span></span>

1. <span data-ttu-id="80c19-293">在业务文档管理工作区中，选择列表中的 **Cheques printing format** 模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-293">In the Business document management workspace, select the **Cheques printing format** template in the list.</span></span>
2. <span data-ttu-id="80c19-294">选择 **详细信息** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="80c19-294">Select the **Details** tab.</span></span>

![业务文档管理工作区页，“详细信息”选项卡](./media/BDM-Overview-EditingTemplate2.png)

<span data-ttu-id="80c19-296">将为所选模板提供 **编辑模板** 选项。</span><span class="sxs-lookup"><span data-stu-id="80c19-296">The **Edit template** option is available for the selected template.</span></span> <span data-ttu-id="80c19-297">有效 ER 配置提供商（此示例中为 **Litware, Inc.**）负责的 ER 格式配置中的模板始终可使用此选项。</span><span class="sxs-lookup"><span data-stu-id="80c19-297">This option is always available for a template in an ER format configuration that is owned by the active ER configuration provider (**Litware, Inc.** in this example).</span></span> <span data-ttu-id="80c19-298">如果选择了 **编辑模板**，则可编辑基础 ER 格式配置草稿版本中的现有模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-298">When **Edit template** is selected, the existing template from the draft version of the underlying ER format configuration will be available to edit.</span></span>

### <a name="initiate-editing-templates-owned-by-other-providers"></a><span data-ttu-id="80c19-299">开始编辑其他提供商负责的模板</span><span class="sxs-lookup"><span data-stu-id="80c19-299">Initiate editing templates owned by other providers</span></span>

1. <span data-ttu-id="80c19-300">在业务文档管理工作区中，选择要用作模板的文档。</span><span class="sxs-lookup"><span data-stu-id="80c19-300">In the Business document management workspace, select the document that you want to use as a template.</span></span>

    ![在业务文档管理工作区页上选择文档](./media/BDM-Overview-EditingTemplate3.png)

2. <span data-ttu-id="80c19-302">选择 **新建文档**，并在 **标题** 字段中，根据需要更改可编辑模板的标题。</span><span class="sxs-lookup"><span data-stu-id="80c19-302">Select **New document**, and in the **Title** field, change the title of the editable template if needed.</span></span> <span data-ttu-id="80c19-303">将把此文本用于命名自动创建的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="80c19-303">The text will be used to name the ER format configuration that is automatically created.</span></span> <span data-ttu-id="80c19-304">请注意，将自动标记此配置 (**Customer FTI report (GER) Copy**) 的草稿版本（其中将包含编辑后的模板），以便为当前用户运行此 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="80c19-304">Note that the draft version of this configuration (**Customer FTI report (GER) Copy**) that will contain the edited template will automatically be marked to run this ER format for the current user.</span></span> <span data-ttu-id="80c19-305">同时，将使用来自基本 ER 格式配置的未经修改原始模板为其他任何用户运行此 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="80c19-305">At the same time, the non-modified original template from the base ER format configuration will be used to run this ER format for any other user.</span></span>
3. <span data-ttu-id="80c19-306">在 **名称** 字段中，更改将自动创建的可编辑模板第一个修订的名称。</span><span class="sxs-lookup"><span data-stu-id="80c19-306">In the **Name** field, change the name of the first revision of the editable template that will be created automatically.</span></span>
4. <span data-ttu-id="80c19-307">在 **注释** 字段中，更改自动创建的可编辑模板修订的备注。</span><span class="sxs-lookup"><span data-stu-id="80c19-307">In the **Comment** field, change the comment for the automatically created revision of the editable template.</span></span>
5. <span data-ttu-id="80c19-308">选择 **确定** 以确认开始执行编辑流程。</span><span class="sxs-lookup"><span data-stu-id="80c19-308">Select **OK** to confirm the start of the editing process.</span></span>

![确认开始编辑流程以创建新模板](./media/BDM-Overview-EditingTemplate4.png)

<span data-ttu-id="80c19-310">当前和另一个提供商（此示例中为 Microsoft）提供的 ER 格式配置中的模板（没有任何修订）始终可使用 **新建文档** 选项。</span><span class="sxs-lookup"><span data-stu-id="80c19-310">The **New document** option is always available for a template in an ER format configuration provided by current and another provider (Microsoft in this example) that doesn't have any revision.</span></span> <span data-ttu-id="80c19-311">然后将把编辑后的模板存储在自动生成的新 ER 格式配置中。</span><span class="sxs-lookup"><span data-stu-id="80c19-311">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

### <a name="start-editing-a-template"></a><span data-ttu-id="80c19-312">开始编辑模板</span><span class="sxs-lookup"><span data-stu-id="80c19-312">Start editing a template</span></span>

1. <span data-ttu-id="80c19-313">从所选模板选择 **编辑文档**。</span><span class="sxs-lookup"><span data-stu-id="80c19-313">From the selected template, select **Edit document**.</span></span>
2. <span data-ttu-id="80c19-314">在 **名称** 字段中，更改将自动创建的可编辑模板第一个修订的名称。</span><span class="sxs-lookup"><span data-stu-id="80c19-314">In the **Name** field, change the name of the first revision of the editable template that will be created automatically.</span></span>
3. <span data-ttu-id="80c19-315">在 **注释** 字段中，更改自动创建的可编辑模板修订的注解。</span><span class="sxs-lookup"><span data-stu-id="80c19-315">In the **Comment** field, change the remark for the automatically created revision of the editable template.</span></span>

    ![在业务文档管理工作区页上编辑模板](./media/BDM-Overview-EditingTemplate5.png)

4. <span data-ttu-id="80c19-317">选择 **确定** 以确认开始执行编辑流程。</span><span class="sxs-lookup"><span data-stu-id="80c19-317">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="80c19-318">将打开 **BDM 模板编辑器** 页。</span><span class="sxs-lookup"><span data-stu-id="80c19-318">The **BDM template editor** page will open.</span></span> <span data-ttu-id="80c19-319">可通过使用 Microsoft 365 在线编辑所选模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-319">The selected template will be available for online editing by using Microsoft 365.</span></span>

![业务文档管理模板编辑器页面](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-microsoft-365"></a><a name="EditInOffice365"></a><span data-ttu-id="80c19-321">在 Microsoft 365 中编辑模板</span><span class="sxs-lookup"><span data-stu-id="80c19-321">Edit a template in Microsoft 365</span></span>

<span data-ttu-id="80c19-322">您可以使用 Microsoft 365 修改模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-322">You can modify the template using Microsoft 365.</span></span> <span data-ttu-id="80c19-323">例如，在 Office Online 中，将模板标题中的字段提示的字体从 **常规** 更改为 **加粗**。</span><span class="sxs-lookup"><span data-stu-id="80c19-323">For example, in Office online, change the font of the field prompts in the template header from **Regular** to **Bold**.</span></span> <span data-ttu-id="80c19-324">这些更改会自动存储在主模板存储（默认情况下为 Azure blob 存储）中存储的可编辑模板中。</span><span class="sxs-lookup"><span data-stu-id="80c19-324">These changes are automatically stored in the editable template that is stored in the primary template's storage (by default, the Azure blob storage).</span></span> <span data-ttu-id="80c19-325">已为 ER 框架配置此项。</span><span class="sxs-lookup"><span data-stu-id="80c19-325">This is configured for the ER framework.</span></span>

![在业务文档管理模板编辑器页上的模板标题中将字体更改为粗体](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a><a name="EditInOfficeDesktopApp"></a><span data-ttu-id="80c19-327">在 Office 桌面应用程序中编辑模板</span><span class="sxs-lookup"><span data-stu-id="80c19-327">Edit a template in the Office desktop application</span></span>

> [!NOTE]
> <span data-ttu-id="80c19-328">此功能仅在正确配置 **SharePoint 文件类型** 参数后可用。</span><span class="sxs-lookup"><span data-stu-id="80c19-328">This function is only available when the **SharePoint document type** parameter is properly configured.</span></span> <span data-ttu-id="80c19-329">有关详细信息，请参阅[配置参数](#SetupBdmParameters)。</span><span class="sxs-lookup"><span data-stu-id="80c19-329">For more information, see [Configure parameters](#SetupBdmParameters).</span></span>

1. <span data-ttu-id="80c19-330">选择 **在桌面应用程序中打开** 选项，以便使用 Office 桌面应用程序的功能（此示例中为 Excel）修改模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-330">Select the **Open in Desktop App** option to modify the template by using the functionality of the Office desktop application (Excel in this example).</span></span> <span data-ttu-id="80c19-331">将把可编辑模板从永久存储复制到业务文档管理参数中配置为 SharePoint 文件夹的临时存储。</span><span class="sxs-lookup"><span data-stu-id="80c19-331">The editable template is copied from the permanent storage to the temporary storage configured in the Business document management parameters as a SharePoint folder.</span></span>
2. <span data-ttu-id="80c19-332">确认要在 Office 桌面的 Excel 应用程序中从临时文件存储打开模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-332">Confirm that you want to open the template from the temporary file storage in the Office desktop Excel application.</span></span>

    ![在桌面 Excel 应用程序中打开的模板](./media/BDM-Overview-EditingLayout3.png)

3. <span data-ttu-id="80c19-334">修改模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-334">Modify the template.</span></span> <span data-ttu-id="80c19-335">例如，通过将颜色从 **黑色** 更改为 **蓝色**，更改模板标题中的字段提示的字体。</span><span class="sxs-lookup"><span data-stu-id="80c19-335">For example, change the font of the fields prompts in the template header by updating color from **Black** to **Blue**.</span></span>

    ![使用桌面 Excel 应用程序修改模板标题中的字体颜色](./media/BDM-Overview-EditingLayout4.png)

4. <span data-ttu-id="80c19-337">在 Excel 桌面应用程序中选择 **保存** 以将模板更改存储到临时存储中。</span><span class="sxs-lookup"><span data-stu-id="80c19-337">Select **Save** in the Excel desktop application to store the template changes in the temporary storage.</span></span>

    ![使用桌面 Excel 应用程序将更改保存到业务文档管理模板编辑器页](./media/BDM-Overview-EditingLayout5.png)

5. <span data-ttu-id="80c19-339">关闭 Excel 桌面应用程序。</span><span class="sxs-lookup"><span data-stu-id="80c19-339">Close the Excel desktop application.</span></span>
6. <span data-ttu-id="80c19-340">选择 **同步已存储副本** 将临时模板存储同步到永久模板存储。</span><span class="sxs-lookup"><span data-stu-id="80c19-340">Select **Sync stored copy** to synchronize the temporary template storage to the permanent template storage.</span></span>

> [!NOTE]
> <span data-ttu-id="80c19-341">临时文件存储中的可编辑模板副本将仅保留在当前模板编辑会话中。</span><span class="sxs-lookup"><span data-stu-id="80c19-341">The copy of the editable template in the temporary file storage is kept for only the current session of template editing.</span></span> <span data-ttu-id="80c19-342">通过关闭 **BDM 模板编辑器** 页完成会话时，将删除此副本。</span><span class="sxs-lookup"><span data-stu-id="80c19-342">When you finish this session by closing the **BDM template editor** page, this copy will be deleted.</span></span> <span data-ttu-id="80c19-343">如果调整了临时文件存储中的模板，但是未选择 **同步已存储副本**，则在尝试关闭 **BDM 模板编辑器** 页时，将有一条消息询问您是否要存储引入的更改。</span><span class="sxs-lookup"><span data-stu-id="80c19-343">If you adjusted the template in the temporary file storage and did not select **Sync stored copy**, when you try to close the **BDM template editor** page, a message will ask whether you want to store introduced changes.</span></span> <span data-ttu-id="80c19-344">如果要将对模板的更改保存到永久文件存储，请选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="80c19-344">Select **Yes** if you want to save your changes to the template in the permanent file location.</span></span>

### <a name="validate-a-template"></a><span data-ttu-id="80c19-345">验证模板</span><span class="sxs-lookup"><span data-stu-id="80c19-345">Validate a template</span></span>

1. <span data-ttu-id="80c19-346">在 **BDM 模板编辑器** 页中，选择 **检查问题** 以针对基础 ER 格式配置验证修改后的模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-346">On the **BDM template editor** page, select **Check for issues** to validate the modified template against the underlying ER format configuration.</span></span> <span data-ttu-id="80c19-347">按照建议（如果有）让模板与基本 ER 格式配置中的格式结构一致。</span><span class="sxs-lookup"><span data-stu-id="80c19-347">Follow the recommendations (if any) to align the template with the structure of the format from the base ER format configuration.</span></span>
2. <span data-ttu-id="80c19-348">选择 **显示格式** 以查看基本 ER 格式配置中必须与可编辑模板一致的当前格式结构。</span><span class="sxs-lookup"><span data-stu-id="80c19-348">Select **Show format** to view the current structure of the format from the base ER format configuration that must be aligned with the editable template.</span></span> 
3. <span data-ttu-id="80c19-349">选择 **隐藏格式** 以关闭窗格。</span><span class="sxs-lookup"><span data-stu-id="80c19-349">Select **Hide format** to close the pane.</span></span>

    ![BDM 模板编辑器页面](./media/BDM-Overview-EditingTemplate6.png)

4. <span data-ttu-id="80c19-351">关闭 **BDM 模板编辑器** 页。</span><span class="sxs-lookup"><span data-stu-id="80c19-351">Close the **BDM template editor** page.</span></span>

<span data-ttu-id="80c19-352">将在 **模板** 选项卡上显示更新后的模板。请注意，现在，编辑后的模板的状态为 **草稿**，并且当前修订不再为空。</span><span class="sxs-lookup"><span data-stu-id="80c19-352">The updated template is shown on the **Template** tab. Notice that the status of the edited template is now **Draft** and the current revision is no longer empty.</span></span> <span data-ttu-id="80c19-353">这意味着此模板的编辑过程已开始。</span><span class="sxs-lookup"><span data-stu-id="80c19-353">This means that the process of this template's editing has been started.</span></span>

![在业务文档管理工作区页上查看更新的模板](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a><span data-ttu-id="80c19-355">测试修改后的模板</span><span class="sxs-lookup"><span data-stu-id="80c19-355">Test the modified template</span></span> 

1. <span data-ttu-id="80c19-356">在应用程序中，切换到公司 **USMF**。</span><span class="sxs-lookup"><span data-stu-id="80c19-356">In the application, change to the company, **USMF**.</span></span>
2. <span data-ttu-id="80c19-357">转至 **应收帐款** \> **发票** \> **所有普通发票**。</span><span class="sxs-lookup"><span data-stu-id="80c19-357">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
3. <span data-ttu-id="80c19-358">选择 **FTI-00000002** 发票，然后选择 **打印管理**。</span><span class="sxs-lookup"><span data-stu-id="80c19-358">Select the **FTI-00000002** invoice, and then select **Print management**.</span></span>
4. <span data-ttu-id="80c19-359">选择 **模块 - 应收帐款** \> **文档** \> **普通发票** \> **原始凭证** 级别以指定要处理的发票范围。</span><span class="sxs-lookup"><span data-stu-id="80c19-359">Select the **Module - accounts receivable** \> **Documents** \> **Free text invoice** \> **Original document** level to specify the scope of invoices for processing.</span></span>
5. <span data-ttu-id="80c19-360">在 **报表格式** 字段中，为指定的文档级别选择 **Customer FTI report (GER) Copy** ER 格式。</span><span class="sxs-lookup"><span data-stu-id="80c19-360">In the **Report format** field, select the **Customer FTI report (GER) Copy** ER format for the specified document level.</span></span>

    ![打印管理设置页](./media/BDM-Overview-TestRun1.png)

6. <span data-ttu-id="80c19-362">按 **Escape** 关闭当前页。</span><span class="sxs-lookup"><span data-stu-id="80c19-362">Press **Escape** to close the current page.</span></span>
7. <span data-ttu-id="80c19-363">选择 **打印**，然后选择 **已选择**。</span><span class="sxs-lookup"><span data-stu-id="80c19-363">Select **Print**, and then select **Selected**.</span></span>
8. <span data-ttu-id="80c19-364">下载文档，然后使用 Excel 桌面应用程序打开。</span><span class="sxs-lookup"><span data-stu-id="80c19-364">Download the document and open it using the Excel desktop application.</span></span>

![普通发票页面](./media/BDM-Overview-TestRun2.png)

<span data-ttu-id="80c19-366">修改后的模板将用于为所选物料生成普通发票报表。</span><span class="sxs-lookup"><span data-stu-id="80c19-366">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="80c19-367">若要分析为模板进行的更改对此报表造成了哪些影响，可以在一个应用程序会话中修改模板之后，立即在另一个应用程序会话中运行此报表。</span><span class="sxs-lookup"><span data-stu-id="80c19-367">To analyze how this report is affected by the changes that you introduced to the template, you can run this report in one application session right after you modified the template in another application session.</span></span>

### <a name="create-an-alternative-template-revision"></a><span data-ttu-id="80c19-368">创建备用模板修订</span><span class="sxs-lookup"><span data-stu-id="80c19-368">Create an alternative template revision</span></span>

1. <span data-ttu-id="80c19-369">打开 **BDM 模板编辑器** 页，然后选择 **Customer FTI report (GER) Copy** 模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-369">Open the **BDM template editor** page and select the **Customer FTI report (GER) Copy** template.</span></span>
2. <span data-ttu-id="80c19-370">在 **修订** 选项卡上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="80c19-370">On the **Revisions** tab, select **New**.</span></span>
3. <span data-ttu-id="80c19-371">如果需要，在 **名称** 字段中，更改第二个修订的名称，并以当前第一个有效修订为基础。</span><span class="sxs-lookup"><span data-stu-id="80c19-371">If needed, in the **Name** field, change the name of the second revision and base it on the currently active first revision.</span></span>
4. <span data-ttu-id="80c19-372">如果需要，在 **注释** 字段中，更改自动创建的可编辑模板修订的注解。</span><span class="sxs-lookup"><span data-stu-id="80c19-372">If needed, in the **Comment** field, change the remark for the automatically created revision of the editable template.</span></span>

    ![在业务文档管理工作区页上创建模板的修订](./media/BDM-Overview-AddRevision.png)

    <span data-ttu-id="80c19-374">您创建了永久模板存储中已存储的模板的新修订。</span><span class="sxs-lookup"><span data-stu-id="80c19-374">You created a new revision of your template that has been stored in the permanent template's storage.</span></span> <span data-ttu-id="80c19-375">现在可以继续编辑当前选择为活动的第二个修订的模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-375">Now you can continue editing the template of the second revision that is currently selected as active.</span></span>

5. <span data-ttu-id="80c19-376">选择第一个修订，然后选择 **设置有效**。</span><span class="sxs-lookup"><span data-stu-id="80c19-376">Select the first revision and then select **Set active**.</span></span> <span data-ttu-id="80c19-377">任何时候如果要返回为模板的另一个修订，可选择此修订为有效。</span><span class="sxs-lookup"><span data-stu-id="80c19-377">You can select another revision as active if at any time you want to return to that revision of the template.</span></span>
6. <span data-ttu-id="80c19-378">选择第二个修订，然后选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="80c19-378">Select the second revision, and then select **Delete**.</span></span>
7. <span data-ttu-id="80c19-379">选择 **确定** 以确认您要删除所选修订。</span><span class="sxs-lookup"><span data-stu-id="80c19-379">Select **OK** to confirm that you want to delete the selected revision.</span></span> <span data-ttu-id="80c19-380">可删除任何不再需要的非有效修订。</span><span class="sxs-lookup"><span data-stu-id="80c19-380">You can delete any of the non-active revisions when they are no longer needed.</span></span>

### <a name="delete-a-modified-template"></a><span data-ttu-id="80c19-381">删除修改后的模板</span><span class="sxs-lookup"><span data-stu-id="80c19-381">Delete a modified template</span></span>

1. <span data-ttu-id="80c19-382">在 **BDM 模板编辑器** 页中，选择 **模板** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="80c19-382">On the **BDM template editor** page, select the **Template** tab.</span></span>
2. <span data-ttu-id="80c19-383">选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="80c19-383">Select **Delete**.</span></span>
3. <span data-ttu-id="80c19-384">如果选择 **确定** 以确认删除，将删除采用修改后模板的 **Customer FTI report (GER) Copy** ER 格式。</span><span class="sxs-lookup"><span data-stu-id="80c19-384">If you select **OK** to confirm deletion, the **Customer FTI report (GER) Copy** ER format with the modified template will be deleted.</span></span> <span data-ttu-id="80c19-385">选择 **取消** 以浏览其他选项。</span><span class="sxs-lookup"><span data-stu-id="80c19-385">Select **Cancel** to explore other options.</span></span>

### <a name="revoke-changes-of-template"></a><span data-ttu-id="80c19-386">撤消对模板的更改</span><span class="sxs-lookup"><span data-stu-id="80c19-386">Revoke changes of template</span></span>

<span data-ttu-id="80c19-387">编辑当前有效提供程序负责的 ER 格式中的模板时，将为您提供用于撤消对模板的更改的选项。</span><span class="sxs-lookup"><span data-stu-id="80c19-387">When you edit the template from an ER format that is owned by the current active provider, you will be offered the option to revoke changes introduced for the template.</span></span>

![在业务文档管理工作区页上拒绝对模板的更改](./media/BDM-Overview-RevokeChanges.png)

1. <span data-ttu-id="80c19-389">在 **BDM 模板编辑器** 页中，选择 **模板** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="80c19-389">On the **BDM template editor** page, select the **Template** tab.</span></span>
2. <span data-ttu-id="80c19-390">选择 **撤消**。</span><span class="sxs-lookup"><span data-stu-id="80c19-390">Select **Undo**.</span></span>
3. <span data-ttu-id="80c19-391">如果选择 **确定** 以撤消对模板的更改，将把修改后的模板替换为原始模板，并删除所有更改。</span><span class="sxs-lookup"><span data-stu-id="80c19-391">If you select **OK** to revoke the changes introduced for the template, the modified template will be replaced by the original template and all changes will be removed.</span></span> <span data-ttu-id="80c19-392">撤消对模板的更改之后，可以删除模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-392">When you revoke changes to the template, you will be able to delete the template.</span></span> <span data-ttu-id="80c19-393">选择 **取消** 以浏览其他选项。</span><span class="sxs-lookup"><span data-stu-id="80c19-393">Select **Cancel** to explore other options.</span></span>

### <a name="publish-a-modified-template"></a><span data-ttu-id="80c19-394">发布修改后的模板</span><span class="sxs-lookup"><span data-stu-id="80c19-394">Publish a modified template</span></span>

1. <span data-ttu-id="80c19-395">在 **BDM 模板编辑器** 页中的 **模板** 选项卡上，选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="80c19-395">On the **BDM template editor** page, on the **Template** tab, select **Publish**.</span></span>
2. <span data-ttu-id="80c19-396">如果选择 **确定** 以确认发布，将把包含修改后的模板的派生 **Customer FTI report (GER) Copy** ER 格式的草稿版本标记为已完成。</span><span class="sxs-lookup"><span data-stu-id="80c19-396">If you select **OK** to confirm publishing, the draft version of the derived **Customer FTI report (GER) Copy** ER format that contains the modified template will be marked as completed.</span></span> <span data-ttu-id="80c19-397">其他用户将可使用修改后的模板。</span><span class="sxs-lookup"><span data-stu-id="80c19-397">The modified template becomes available for other users.</span></span> <span data-ttu-id="80c19-398">此 ER 格式的完成版本将仅保留模板的最后一个有效版本。</span><span class="sxs-lookup"><span data-stu-id="80c19-398">The completed versions of this ER format will keep only the last active revision of your template.</span></span> <span data-ttu-id="80c19-399">将删除其他修订。</span><span class="sxs-lookup"><span data-stu-id="80c19-399">Other revisions will be deleted.</span></span> <span data-ttu-id="80c19-400">选择 **取消** 以浏览其他选项。</span><span class="sxs-lookup"><span data-stu-id="80c19-400">Select **Cancel** to explore other options.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="80c19-401">常见问题</span><span class="sxs-lookup"><span data-stu-id="80c19-401">Frequently asked questions</span></span>

### <a name="i-selected-edit-document-but-instead-of-going-to-the-bdm-template-editor-page-in-finance-i-was-sent-to-the-microsoft-365-webpage"></a><span data-ttu-id="80c19-402">我选择了编辑文档，但是结果不是转到 Finance 中的 BDM 模板编辑器页，而是转到了 Microsoft 365 网页。</span><span class="sxs-lookup"><span data-stu-id="80c19-402">I selected Edit document, but instead of going to the BDM template editor page in Finance, I was sent to the Microsoft 365 webpage.</span></span>

<span data-ttu-id="80c19-403">此问题是一个涉及 Microsoft 365 重定向的已知问题。</span><span class="sxs-lookup"><span data-stu-id="80c19-403">This issue is a known issue that involves Microsoft 365 redirection.</span></span> <span data-ttu-id="80c19-404">首次登录 Microsoft 365 时会出现此问题。</span><span class="sxs-lookup"><span data-stu-id="80c19-404">It occurs when you sign to Microsoft 365 for the first time.</span></span> <span data-ttu-id="80c19-405">要解决此问题，在浏览器中选择 **返回** 返回上一页。</span><span class="sxs-lookup"><span data-stu-id="80c19-405">To work around this issue, select **Back** in your browser to return to the previous page.</span></span>

### <a name="i-understand-how-to-edit-a-template-by-using-microsoft-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-and-adjust-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-use-the-office-desktop-application-in-the-same-way"></a><span data-ttu-id="80c19-406">我知道如何在第一个应用程序会话中通过使用 Microsoft 365 编辑模板，以及如何在第二个应用程序会话中使用模板，并调整模板来查看我的更改对生成的业务文档有何影响。</span><span class="sxs-lookup"><span data-stu-id="80c19-406">I understand how to edit a template by using Microsoft 365 in the first application session, and how to use the template in the second application session and adjust the template to see how my changes affect the generated business document.</span></span> <span data-ttu-id="80c19-407">我能否以相同方式使用 Office 桌面应用程序？</span><span class="sxs-lookup"><span data-stu-id="80c19-407">Can I use the Office desktop application in the same way?</span></span>

<span data-ttu-id="80c19-408">是的，可以。</span><span class="sxs-lookup"><span data-stu-id="80c19-408">Yes, you can.</span></span> <span data-ttu-id="80c19-409">在第一个应用程序会话中，选择 **在桌面应用程序中打开**。</span><span class="sxs-lookup"><span data-stu-id="80c19-409">In the first application session, select **Open in Desktop App**.</span></span> <span data-ttu-id="80c19-410">将把您的模板存储到临时文件存储中，并在 Office 桌面应用程序中打开。</span><span class="sxs-lookup"><span data-stu-id="80c19-410">Your template will be stored in the temporary file storage and opened in the Office desktop application.</span></span> <span data-ttu-id="80c19-411">接下来，完成以下步骤在生成的业务文档中预览模板更改：</span><span class="sxs-lookup"><span data-stu-id="80c19-411">Next, complete the following steps to preview your template changes in the generated business document:</span></span>

1. <span data-ttu-id="80c19-412">通过使用 Office 桌面应用程序在模板中进行更改。</span><span class="sxs-lookup"><span data-stu-id="80c19-412">Make changes in the template by using the Office desktop application.</span></span>
2. <span data-ttu-id="80c19-413">在 Office 桌面应用程序中选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="80c19-413">Select **Save** in the Office desktop application.</span></span>
3. <span data-ttu-id="80c19-414">在第一个应用程序会话的 **BDM 模板编辑器** 页中，选择 **同步已存储副本**。</span><span class="sxs-lookup"><span data-stu-id="80c19-414">On the **BDM template editor** page of the first application session, select **Sync stored copy**.</span></span>
4. <span data-ttu-id="80c19-415">在第二个应用程序会话中执行此模板 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="80c19-415">Execute this template ER format in the second application session.</span></span>

### <a name="when-i-select-open-in-desktop-app-i-receive-the-following-error-message-value-cannot-be-null-parameter-name-externalid-how-do-i-work-around-this-issue"></a><span data-ttu-id="80c19-416">当我选择“在桌面应用中打开”时，我收到以下错误消息：“值不能为空。</span><span class="sxs-lookup"><span data-stu-id="80c19-416">When I select Open in Desktop App, I receive the following error message: "Value cannot be null.</span></span> <span data-ttu-id="80c19-417">参数名称：externalId。”</span><span class="sxs-lookup"><span data-stu-id="80c19-417">Parameter name: externalId."</span></span> <span data-ttu-id="80c19-418">应该如何解决这个问题？</span><span class="sxs-lookup"><span data-stu-id="80c19-418">How do I work around this issue?</span></span>

<span data-ttu-id="80c19-419">您当前登录的应用程序实例所在 Azure AD 域很可能不是用于部署此实例的 Azure AD 域。</span><span class="sxs-lookup"><span data-stu-id="80c19-419">Most likely you signed in to the current instance of the app of the Azure AD domain which differs from the Azure AD domain that was used to deploy this instance.</span></span> <span data-ttu-id="80c19-420">因为 SharePoint 服务（用于存储模板来使其可通过使用 Office 桌面应用程序进行编辑）属于相同域，所以我们无权访问 SharePoint 服务。</span><span class="sxs-lookup"><span data-stu-id="80c19-420">Because the SharePoint service, which is used to store templates for making them available for editing by using the Office desktop applications, belongs to the same domain, we have no permissions to access the SharePoint service.</span></span> <span data-ttu-id="80c19-421">若要解决此问题，请使用具有正确 Azure AD 域的用户的凭据登录当前实例。</span><span class="sxs-lookup"><span data-stu-id="80c19-421">To resolve this issue, sign in to the current instance using the credentials of a user with the correct Azure AD domain.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="80c19-422">其他资源</span><span class="sxs-lookup"><span data-stu-id="80c19-422">Additional resources</span></span>

[<span data-ttu-id="80c19-423">电子申报 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="80c19-423">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="80c19-424">ER 设计以 OPENXML 格式生成报表的配置（2016 年 11 月）</span><span class="sxs-lookup"><span data-stu-id="80c19-424">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>](tasks/er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="80c19-425">设计 ER 配置以生成 Word 格式的报表</span><span class="sxs-lookup"><span data-stu-id="80c19-425">Design ER configurations to generate reports in Word format</span></span>](tasks/er-design-configuration-word-2016-11.md)

[<span data-ttu-id="80c19-426">使用 ER 在您生成的文档中嵌入图像和形状</span><span class="sxs-lookup"><span data-stu-id="80c19-426">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="80c19-427">配置电子报告 (ER) 以便将数据导入 Power BI</span><span class="sxs-lookup"><span data-stu-id="80c19-427">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)

## <a name="list-of-er-configurations-that-have-been-released-in-finance-to-support-configurable-business-documents"></a><a name="list-of-configurations-cbd"></a><span data-ttu-id="80c19-428">Finance 中发布的支持可配置业务文档的 ER 配置列表</span><span class="sxs-lookup"><span data-stu-id="80c19-428">List of ER configurations that have been released in Finance to support configurable business documents</span></span>

<span data-ttu-id="80c19-429">Finance 的 ER 配置[列表](general-electronic-reporting.md#list-of-configurations)会不断更新。</span><span class="sxs-lookup"><span data-stu-id="80c19-429">The [list](general-electronic-reporting.md#list-of-configurations) of ER configurations for Finance is constantly updated.</span></span> <span data-ttu-id="80c19-430">打开[全局存储库](er-download-configurations-global-repo.md)查看当前支持的 ER 配置列表。</span><span class="sxs-lookup"><span data-stu-id="80c19-430">Open the [Global repository](er-download-configurations-global-repo.md) to review the list of ER configurations that are currently supported.</span></span> <span data-ttu-id="80c19-431">您可以[筛选](https://docs.microsoft.com/dynamics365/finance/localizations/enhanced-filtering-global-repo)全局存储库，来查看用于支持可配置业务文档的 ER 配置列表。</span><span class="sxs-lookup"><span data-stu-id="80c19-431">You can [filter](https://docs.microsoft.com/dynamics365/finance/localizations/enhanced-filtering-global-repo) the Global repository to review the list of ER configurations that are used to support configurable business documents.</span></span>

![在配置存储库页筛选全局存储库的内容](./media/bdm-overview-filterglobalrepo.gif)

<span data-ttu-id="80c19-433">下表显示了 ER 配置的列表，这些配置支持可配置业务文档，已在 2020 年 12 月前在 Finance 中发布。</span><span class="sxs-lookup"><span data-stu-id="80c19-433">The following table shows the list of ER configurations that support configurable business documents and that have been released in Finance up until December 2020.</span></span>

| <span data-ttu-id="80c19-434">数据模型配置</span><span class="sxs-lookup"><span data-stu-id="80c19-434">Data model configuration</span></span>    | <span data-ttu-id="80c19-435">格式配置</span><span class="sxs-lookup"><span data-stu-id="80c19-435">Format configurations</span></span>                           |
|-----------------------------|-------------------------------------------------|
| <span data-ttu-id="80c19-436">提单模型</span><span class="sxs-lookup"><span data-stu-id="80c19-436">Bill of lading model</span></span>        | <span data-ttu-id="80c19-437">提单 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-437">Bill of lading (Excel)</span></span>                          |
|                             | <span data-ttu-id="80c19-438">提单 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-438">Bill of lading (Word)</span></span>                           |
| <span data-ttu-id="80c19-439">原产地证书模型</span><span class="sxs-lookup"><span data-stu-id="80c19-439">Certificate of origin model</span></span> | <span data-ttu-id="80c19-440">原产地证书 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-440">Certificate of origin (Excel)</span></span>                   |
|                             | <span data-ttu-id="80c19-441">原产地证书 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-441">Certificate of origin (Word)</span></span>                    |
| <span data-ttu-id="80c19-442">发票模型</span><span class="sxs-lookup"><span data-stu-id="80c19-442">Invoice model</span></span>               | <span data-ttu-id="80c19-443">客户借方通知单和贷方通知单 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-443">Customer Debit and Credit Note (Excel)</span></span>          |
|                             | <span data-ttu-id="80c19-444">客户借方通知单和贷方通知单 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-444">Customer Debit and Credit Note (Word)</span></span>           |
|                             | <span data-ttu-id="80c19-445">普通发票 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-445">Free text invoice (Excel)</span></span>                       |
|                             | <span data-ttu-id="80c19-446">普通发票 (Excel) (BH)</span><span class="sxs-lookup"><span data-stu-id="80c19-446">Free text invoice (Excel) (BH)</span></span>                  |
|                             | <span data-ttu-id="80c19-447">普通发票 (FR) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-447">Free text invoice (FR) (Excel)</span></span>                  |
|                             | <span data-ttu-id="80c19-448">普通发票 (LT) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-448">Free text invoice (LT) (Excel)</span></span>                  |
|                             | <span data-ttu-id="80c19-449">普通发票 (LV) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-449">Free text invoice (LV) (Excel)</span></span>                  |
|                             | <span data-ttu-id="80c19-450">普通发票 (PL) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-450">Free text invoice (PL) (Excel)</span></span>                  |
|                             | <span data-ttu-id="80c19-451">普通发票 (CZ) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-451">Free text invoice (CZ) (Excel)</span></span>                  |
|                             | <span data-ttu-id="80c19-452">普通发票 (EE) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-452">Free text invoice (EE) (Excel)</span></span>                  |
|                             | <span data-ttu-id="80c19-453">普通发票 (HU) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-453">Free text invoice (HU) (Excel)</span></span>                  |
|                             | <span data-ttu-id="80c19-454">普通发票 (TH) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-454">Free text invoice (TH) (Excel)</span></span>                  |
|                             | <span data-ttu-id="80c19-455">普通发票 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-455">Free text invoice (Word)</span></span>                        |
|                             | <span data-ttu-id="80c19-456">项目合同行项 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-456">Project contract line items (Excel)</span></span>             |
|                             | <span data-ttu-id="80c19-457">项目合同行项 (CZ) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-457">Project contract line items (CZ) (Excel)</span></span>        |
|                             | <span data-ttu-id="80c19-458">项目合同行项 (Excel) (BH)</span><span class="sxs-lookup"><span data-stu-id="80c19-458">Project contract line items (Excel) (BH)</span></span>        |
|                             | <span data-ttu-id="80c19-459">项目合同行项 (HU) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-459">Project contract line items (HU) (Excel)</span></span>        |
|                             | <span data-ttu-id="80c19-460">项目合同行项 (LT) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-460">Project contract line items (LT) (Excel)</span></span>        |
|                             | <span data-ttu-id="80c19-461">项目合同行项 (PL) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-461">Project contract line items (PL) (Excel)</span></span>        |
|                             | <span data-ttu-id="80c19-462">项目合同行项 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-462">Project contract line items (Word)</span></span>              |
|                             | <span data-ttu-id="80c19-463">项目客户保留发布 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-463">Project customer retention release (Excel)</span></span>      |
|                             | <span data-ttu-id="80c19-464">项目客户保留发布 (CZ) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-464">Project customer retention release (CZ) (Excel)</span></span> |
|                             | <span data-ttu-id="80c19-465">项目客户保留发布 (HU) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-465">Project customer retention release (HU) (Excel)</span></span> |
|                             | <span data-ttu-id="80c19-466">项目客户保留发布 (LT) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-466">Project customer retention release (LT) (Excel)</span></span> |
|                             | <span data-ttu-id="80c19-467">项目客户保留发布 (PL) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-467">Project customer retention release (PL) (Excel)</span></span> |
|                             | <span data-ttu-id="80c19-468">项目客户保留发布 (TH) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-468">Project customer retention release (TH) (Excel)</span></span> |
|                             | <span data-ttu-id="80c19-469">项目客户保留发布 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-469">Project customer retention release (Word)</span></span>       |
|                             | <span data-ttu-id="80c19-470">项目发票 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-470">Project invoice (Excel)</span></span>                         |
|                             | <span data-ttu-id="80c19-471">项目发票 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-471">Project Invoice (Word)</span></span>                          |
|                             | <span data-ttu-id="80c19-472">项目发票 (AE) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-472">Project invoice (AE) (Excel)</span></span>                    |
|                             | <span data-ttu-id="80c19-473">项目发票 (CZ) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-473">Project invoice (CZ) (Excel)</span></span>                    |
|                             | <span data-ttu-id="80c19-474">项目发票 (Excel) (BH)</span><span class="sxs-lookup"><span data-stu-id="80c19-474">Project invoice (Excel) (BH)</span></span>                    |
|                             | <span data-ttu-id="80c19-475">项目发票 (HU) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-475">Project invoice (HU) (Excel)</span></span>                    |
|                             | <span data-ttu-id="80c19-476">项目发票 (JP) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-476">Project invoice (JP) (Excel)</span></span>                    |
|                             | <span data-ttu-id="80c19-477">项目发票 (LT) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-477">Project invoice (LT) (Excel)</span></span>                    |
|                             | <span data-ttu-id="80c19-478">项目发票 (PL) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-478">Project invoice (PL) (Excel)</span></span>                    |
|                             | <span data-ttu-id="80c19-479">项目发票 (TH) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-479">Project invoice (TH) (Excel)</span></span>                    |
|                             | <span data-ttu-id="80c19-480">项目发票（全额）(MY) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-480">Project invoice full (MY) (Excel)</span></span>               |
|                             | <span data-ttu-id="80c19-481">项目发票（简单）(MY) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-481">Project invoice simple (MY) (Excel)</span></span>             |
|                             | <span data-ttu-id="80c19-482">项目管理发票 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-482">Project manage invoice (Excel)</span></span>                  |
|                             | <span data-ttu-id="80c19-483">项目管理发票 (CZ) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-483">Project manage invoice (CZ) (Excel)</span></span>             |
|                             | <span data-ttu-id="80c19-484">项目管理发票 (Excel) (BH)</span><span class="sxs-lookup"><span data-stu-id="80c19-484">Project manage invoice (Excel) (BH)</span></span>             |
|                             | <span data-ttu-id="80c19-485">项目管理发票 (HU) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-485">Project manage invoice (HU) (Excel)</span></span>             |
|                             | <span data-ttu-id="80c19-486">项目管理发票 (JP) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-486">Project manage invoice (JP) (Excel)</span></span>             |
|                             | <span data-ttu-id="80c19-487">项目管理发票 (LT) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-487">Project manage invoice (LT) (Excel)</span></span>             |
|                             | <span data-ttu-id="80c19-488">项目管理发票 (PL) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-488">Project manage invoice (PL) (Excel)</span></span>             |
|                             | <span data-ttu-id="80c19-489">项目管理发票 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-489">Project manage invoice (Word)</span></span>                   |
|                             | <span data-ttu-id="80c19-490">采购预付款发票 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-490">Purchase advance invoice (Excel)</span></span>                |
|                             | <span data-ttu-id="80c19-491">采购预付款发票 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-491">Purchase advance invoice (Word)</span></span>                 |
|                             | <span data-ttu-id="80c19-492">销售预付款发票 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-492">Sales advance invoice (Excel)</span></span>                   |
|                             | <span data-ttu-id="80c19-493">销售预付款发票 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-493">Sales advance invoice (Word)</span></span>                    |
|                             | <span data-ttu-id="80c19-494">销售预付款发票 (PL) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-494">Sales advance invoice (PL) (Excel)</span></span>              |
|                             | <span data-ttu-id="80c19-495">销售发票 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-495">Sales invoice (Excel)</span></span>                           |
|                             | <span data-ttu-id="80c19-496">销售发票 (Excel) (BH)</span><span class="sxs-lookup"><span data-stu-id="80c19-496">Sales invoice (Excel) (BH)</span></span>                      |
|                             | <span data-ttu-id="80c19-497">销售发票 (Excel) (CZ)</span><span class="sxs-lookup"><span data-stu-id="80c19-497">Sales invoice (Excel) (CZ)</span></span>                      |
|                             | <span data-ttu-id="80c19-498">销售发票 (Excel) (EE)</span><span class="sxs-lookup"><span data-stu-id="80c19-498">Sales invoice (Excel) (EE)</span></span>                      |
|                             | <span data-ttu-id="80c19-499">销售发票 (Excel) (FR)</span><span class="sxs-lookup"><span data-stu-id="80c19-499">Sales invoice (Excel) (FR)</span></span>                      |
|                             | <span data-ttu-id="80c19-500">销售发票 (Excel) (HU)</span><span class="sxs-lookup"><span data-stu-id="80c19-500">Sales invoice (Excel) (HU)</span></span>                      |
|                             | <span data-ttu-id="80c19-501">销售发票 (Excel) (IN)</span><span class="sxs-lookup"><span data-stu-id="80c19-501">Sales invoice (Excel) (IN)</span></span>                      |
|                             | <span data-ttu-id="80c19-502">销售发票 (Excel) (LT)</span><span class="sxs-lookup"><span data-stu-id="80c19-502">Sales invoice (Excel) (LT)</span></span>                      |
|                             | <span data-ttu-id="80c19-503">销售发票 (Excel) (LV)</span><span class="sxs-lookup"><span data-stu-id="80c19-503">Sales invoice (Excel) (LV)</span></span>                      |
|                             | <span data-ttu-id="80c19-504">销售发票 (Excel) (PL)</span><span class="sxs-lookup"><span data-stu-id="80c19-504">Sales invoice (Excel) (PL)</span></span>                      |
|                             | <span data-ttu-id="80c19-505">销售发票 (Excel) (TH)</span><span class="sxs-lookup"><span data-stu-id="80c19-505">Sales invoice (Excel) (TH)</span></span>                      |
|                             | <span data-ttu-id="80c19-506">销售发票 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-506">Sales invoice (Word)</span></span>                            |
|                             | <span data-ttu-id="80c19-507">TMS 商业发票 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-507">TMS Commercial Invoice (Excel)</span></span>                  |
|                             | <span data-ttu-id="80c19-508">TMS 商业发票 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-508">TMS Commercial Invoice (Word)</span></span>                   |
|                             | <span data-ttu-id="80c19-509">供应商发票文档 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-509">Vendor invoice document (Excel)</span></span>                 |
|                             | <span data-ttu-id="80c19-510">供应商发票文档 (CZ) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-510">Vendor invoice document (CZ) (Excel)</span></span>            |
|                             | <span data-ttu-id="80c19-511">供应商发票文档 (HU) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-511">Vendor invoice document (HU) (Excel)</span></span>            |
|                             | <span data-ttu-id="80c19-512">供应商发票文档 (IN) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-512">Vendor invoice document (IN) (Excel)</span></span>            |
|                             | <span data-ttu-id="80c19-513">供应商发票文档 (LT) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-513">Vendor invoice document (LT) (Excel)</span></span>            |
|                             | <span data-ttu-id="80c19-514">供应商发票文档 (LV) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-514">Vendor invoice document (LV) (Excel)</span></span>            |
|                             | <span data-ttu-id="80c19-515">供应商发票文档 (MY) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-515">Vendor invoice document (MY) (Excel)</span></span>            |
|                             | <span data-ttu-id="80c19-516">供应商发票文档 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-516">Vendor invoice document (Word)</span></span>                  |
| <span data-ttu-id="80c19-517">订单模型</span><span class="sxs-lookup"><span data-stu-id="80c19-517">Order model</span></span>                 | <span data-ttu-id="80c19-518">协议确认 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-518">Agreement confirmation (Excel)</span></span>                  |
|                             | <span data-ttu-id="80c19-519">协议确认 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-519">Agreement confirmation (Word)</span></span>                   |
|                             | <span data-ttu-id="80c19-520">采购协议确认 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-520">Purchase agreement confirmation (Excel)</span></span>         |
|                             | <span data-ttu-id="80c19-521">采购协议确认 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-521">Purchase agreement confirmation (Word)</span></span>          |
|                             | <span data-ttu-id="80c19-522">采购订单 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-522">Purchase order (Excel)</span></span>                          |
|                             | <span data-ttu-id="80c19-523">采购订单 (CZ) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-523">Purchase order (CZ) (Excel)</span></span>                     |
|                             | <span data-ttu-id="80c19-524">采购订单查询 (CZ) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-524">Purchase order inquiry (CZ) (Excel)</span></span>             |
|                             | <span data-ttu-id="80c19-525">采购订单 (HU) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-525">Purchase order (HU) (Excel)</span></span>                     |
|                             | <span data-ttu-id="80c19-526">采购订单查询 (HU) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-526">Purchase order inquiry (HU) (Excel)</span></span>             |
|                             | <span data-ttu-id="80c19-527">采购订单 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-527">Purchase order (Word)</span></span>                           |
|                             | <span data-ttu-id="80c19-528">采购订单查询 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-528">Purchase order inquiry (Excel)</span></span>                  |
|                             | <span data-ttu-id="80c19-529">采购订单查询 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-529">Purchase order inquiry (Word)</span></span>                   |
|                             | <span data-ttu-id="80c19-530">销售订单确认 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-530">Sales order confirmation (Excel)</span></span>                |
|                             | <span data-ttu-id="80c19-531">销售订单确认 (CZ) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-531">Sales order confirmation (CZ) (Excel)</span></span>           |
|                             | <span data-ttu-id="80c19-532">销售订单确认 (HU) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-532">Sales order confirmation (HU) (Excel)</span></span>           |
|                             | <span data-ttu-id="80c19-533">销售订单确认 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-533">Sales order confirmation (Word)</span></span>                 |
| <span data-ttu-id="80c19-534">装箱单模型</span><span class="sxs-lookup"><span data-stu-id="80c19-534">Packing list model</span></span>          | <span data-ttu-id="80c19-535">容器内容 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-535">Container contents (Excel)</span></span>                      |
|                             | <span data-ttu-id="80c19-536">容器内容 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-536">Container contents (Word)</span></span>                       |
|                             | <span data-ttu-id="80c19-537">负荷列表 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-537">Load list (Excel)</span></span>                               |
|                             | <span data-ttu-id="80c19-538">负荷列表 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-538">Load list (Word)</span></span>                                |
|                             | <span data-ttu-id="80c19-539">领料单 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-539">Picking list (Excel)</span></span>                            |
|                             | <span data-ttu-id="80c19-540">领料单 (CZ) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-540">Picking list (CZ) (Excel)</span></span>                       |
|                             | <span data-ttu-id="80c19-541">领料单 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-541">Picking list (Word)</span></span>                             |
|                             | <span data-ttu-id="80c19-542">生产领料单 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-542">Production pick list (Excel)</span></span>                    |
|                             | <span data-ttu-id="80c19-543">生产领料单 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-543">Production pick list (Word)</span></span>                     |
|                             | <span data-ttu-id="80c19-544">负荷的装运领料单 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-544">Shipping pick list for load (Excel)</span></span>             |
|                             | <span data-ttu-id="80c19-545">负荷的装运领料单 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-545">Shipping pick list for load (Word)</span></span>              |
|                             | <span data-ttu-id="80c19-546">装运的装运领料单 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-546">Shipping pick list for shipment (Excel)</span></span>         |
|                             | <span data-ttu-id="80c19-547">装运的装运领料单 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-547">Shipping pick list for shipment (Word)</span></span>          |
|                             | <span data-ttu-id="80c19-548">波次的装运领料单 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-548">Shipping pick list for wave (Excel)</span></span>             |
|                             | <span data-ttu-id="80c19-549">波次的装运领料单 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-549">Shipping pick list for wave (Word)</span></span>              |
| <span data-ttu-id="80c19-550">付款模型</span><span class="sxs-lookup"><span data-stu-id="80c19-550">Payment model</span></span>               | <span data-ttu-id="80c19-551">客户付款通知 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-551">Customer payment advice (Excel)</span></span>                 |
|                             | <span data-ttu-id="80c19-552">客户付款通知 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-552">Customer payment advice (Word)</span></span>                  |
|                             | <span data-ttu-id="80c19-553">供应商付款通知 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-553">Vendor payment advice (Excel)</span></span>                   |
|                             | <span data-ttu-id="80c19-554">供应商付款通知 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-554">Vendor payment advice (Word)</span></span>                    |
| <span data-ttu-id="80c19-555">报价单模型</span><span class="sxs-lookup"><span data-stu-id="80c19-555">Quotation model</span></span>             | <span data-ttu-id="80c19-556">项目报价单 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-556">Project quotation (Excel)</span></span>                       |
|                             | <span data-ttu-id="80c19-557">项目报价单 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-557">Project quotation (Word)</span></span>                        |
|                             | <span data-ttu-id="80c19-558">询价 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-558">Request for quotation (Excel)</span></span>                   |
|                             | <span data-ttu-id="80c19-559">询价（接受）(Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-559">Request for quotation (Accept) (Excel)</span></span>          |
|                             | <span data-ttu-id="80c19-560">询价（接受）(Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-560">Request for quotation (Accept) (Word)</span></span>           |
|                             | <span data-ttu-id="80c19-561">询价（拒绝）(Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-561">Request for quotation (Reject) (Excel)</span></span>          |
|                             | <span data-ttu-id="80c19-562">询价（拒绝）(Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-562">Request for quotation (Reject) (Word)</span></span>           |
|                             | <span data-ttu-id="80c19-563">询价（退回）(Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-563">Request for quotation (Return) (Excel)</span></span>          |
|                             | <span data-ttu-id="80c19-564">询价（退回）(Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-564">Request for quotation (Return) (Word)</span></span>           |
|                             | <span data-ttu-id="80c19-565">询价 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-565">Request for quotation (Word)</span></span>                    |
|                             | <span data-ttu-id="80c19-566">销售报价单 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-566">Sales quotation (Excel)</span></span>                         |
|                             | <span data-ttu-id="80c19-567">销售报价单 (CZ) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-567">Sales quotation (CZ) (Excel)</span></span>                    |
|                             | <span data-ttu-id="80c19-568">销售报价单 (HU) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-568">Sales quotation (HU) (Excel)</span></span>                    |
|                             | <span data-ttu-id="80c19-569">销售报价单 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-569">Sales quotation (Word)</span></span>                          |
|                             | <span data-ttu-id="80c19-570">销售报价单确认 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-570">Sales quotation confirmation (Excel)</span></span>            |
|                             | <span data-ttu-id="80c19-571">销售报价单确认 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-571">Sales quotation confirmation (Word)</span></span>             |
| <span data-ttu-id="80c19-572">对帐模型</span><span class="sxs-lookup"><span data-stu-id="80c19-572">Reconciliation model</span></span>        | <span data-ttu-id="80c19-573">客户帐户对帐单，外部 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-573">Cust account statement, Ext (Excel)</span></span>             |
|                             | <span data-ttu-id="80c19-574">客户帐户对帐单，外部 (CN) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-574">Cust account statement, Ext (CN) (Excel)</span></span>        |
|                             | <span data-ttu-id="80c19-575">客户帐户对帐单，外部 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-575">Cust account statement, Ext (Word)</span></span>              |
|                             | <span data-ttu-id="80c19-576">客户帐户对帐单，法国 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-576">Cust account statement, France (Excel)</span></span>          |
| <span data-ttu-id="80c19-577">提醒模型</span><span class="sxs-lookup"><span data-stu-id="80c19-577">Reminder model</span></span>              | <span data-ttu-id="80c19-578">催款单 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-578">Collection letter note (Excel)</span></span>                  |
|                             | <span data-ttu-id="80c19-579">催款单 (CN) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-579">Collection letter note (CN) (Excel)</span></span>             |
|                             | <span data-ttu-id="80c19-580">催款单 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-580">Collection letter note (Word)</span></span>                   |
|                             | <span data-ttu-id="80c19-581">客户利息单 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-581">Customer interest note (Excel)</span></span>                  |
|                             | <span data-ttu-id="80c19-582">客户利息单 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-582">Customer interest note (Word)</span></span>                   |
| <span data-ttu-id="80c19-583">运单模型</span><span class="sxs-lookup"><span data-stu-id="80c19-583">Waybill model</span></span>               | <span data-ttu-id="80c19-584">负荷支付方式 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-584">Load tender (Excel)</span></span>                             |
|                             | <span data-ttu-id="80c19-585">负荷支付方式 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-585">Load tender (Word)</span></span>                              |
|                             | <span data-ttu-id="80c19-586">采购订单装箱单 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-586">Purchase order packing slip (Excel)</span></span>             |
|                             | <span data-ttu-id="80c19-587">采购订单装箱单 (CZ) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-587">Purchase order packing slip (CZ) (Excel)</span></span>        |
|                             | <span data-ttu-id="80c19-588">采购订单装箱单 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-588">Purchase order packing slip (Word)</span></span>              |
|                             | <span data-ttu-id="80c19-589">路线 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-589">Route (Excel)</span></span>                                   |
|                             | <span data-ttu-id="80c19-590">路线 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-590">Route (Word)</span></span>                                    |
|                             | <span data-ttu-id="80c19-591">销售订单装箱单 (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-591">Sales order packing slip (Excel)</span></span>                |
|                             | <span data-ttu-id="80c19-592">销售订单装箱单 (CZ) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-592">Sales order packing slip (CZ) (Excel)</span></span>           |
|                             | <span data-ttu-id="80c19-593">销售订单装箱单 (LT) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-593">Sales order packing slip (LT) (Excel)</span></span>           |
|                             | <span data-ttu-id="80c19-594">销售订单装箱单 (PL) (Excel)</span><span class="sxs-lookup"><span data-stu-id="80c19-594">Sales order packing slip (PL) (Excel)</span></span>           |
|                             | <span data-ttu-id="80c19-595">销售订单装箱单 (Word)</span><span class="sxs-lookup"><span data-stu-id="80c19-595">Sales order packing slip (Word)</span></span>                 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
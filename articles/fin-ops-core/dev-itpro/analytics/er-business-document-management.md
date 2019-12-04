---
title: 业务文档管理概览
description: 本主题介绍有关如何使用 ER 框架的业务文档管理功能的信息。
author: NickSelin
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERSecurityAccessEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0a2fa6a7f6efef05862a3727a80122c22d591487
ms.sourcegitcommit: 4162d9ef4239c9d4e5297b8aaa903dd54f9cafc3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2019
ms.locfileid: "2824512"
---
# <a name="business-document-management-overview"></a><span data-ttu-id="a503f-103">业务文档管理概览</span><span class="sxs-lookup"><span data-stu-id="a503f-103">Business document management overview</span></span>

<span data-ttu-id="a503f-104">业务用户使用[电子申报 (ER) 概述](general-electronic-reporting.md)根据各个国家/地区的法律要求配置传出文档的格式。</span><span class="sxs-lookup"><span data-stu-id="a503f-104">Business users use the [Electronic reporting (ER) overview](general-electronic-reporting.md) to configure formats for outbound documents in accordance with the legal requirements of various countries/regions.</span></span> <span data-ttu-id="a503f-105">用户也可以定义数据流，以便指定在生成的文档中放置哪些数据。</span><span class="sxs-lookup"><span data-stu-id="a503f-105">Users can also define the dataflow to specify what application data is placed in generated documents.</span></span> <span data-ttu-id="a503f-106">ER 框架使用预定义的模板生成 Microsoft Office 格式（Excel 工作簿或 Word 文档）格式的传出文档。</span><span class="sxs-lookup"><span data-stu-id="a503f-106">The ER framework generates outbound documents in Microsoft Office formats (Excel workbooks or Word documents) by using predefined templates.</span></span> <span data-ttu-id="a503f-107">将根据生成所需文档时配置的数据流使用必需数据填充模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-107">The templates are populated with required data in accordance to configured dataflow while required documents are generated.</span></span> <span data-ttu-id="a503f-108">可以在 ER 解决方案中发布配置的每种格式，以便生成特定传出文档。</span><span class="sxs-lookup"><span data-stu-id="a503f-108">Each configured format can be published as part of an ER solution to generate specific outbound documents.</span></span> <span data-ttu-id="a503f-109">这通过 ER 格式配置表示，其中可包含可用于生成不同传出文档的模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-109">This is represented by an ER format configuration that can contain templates you can use to generate different outbound documents.</span></span> <span data-ttu-id="a503f-110">业务用户可使用此框架管理所需业务文档。</span><span class="sxs-lookup"><span data-stu-id="a503f-110">Business users can use this framework to manage required business documents.</span></span>

<span data-ttu-id="a503f-111">**业务文档管理**建立在 ER 框架的基础上，可供业务用户使用 Microsoft Office 365 服务或相应 Microsoft Office 桌面应用程序编辑业务文档模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-111">**Business document management** is built on top of the ER framework and enables business users to edit business document templates by using Microsoft Office 365 service or appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="a503f-112">对此类文档的编辑包括在不执行源代码更改和不进行新部署的情况下，更改业务文档设计和为更多数据添加占位符。</span><span class="sxs-lookup"><span data-stu-id="a503f-112">Edits to the documents might include changing business document designs and adding placeholders for additional data without source code changes and new deployments.</span></span> <span data-ttu-id="a503f-113">若要更新业务文档模板，无需了解 ER 框架。</span><span class="sxs-lookup"><span data-stu-id="a503f-113">No knowledge of the ER framework is required to update templates of business documents.</span></span>

> [!NOTE]
> <span data-ttu-id="a503f-114">请注意，可通过业务文档管理修改用于生成订单、发票等之类业务文档的模板。修改模板和发布模板新版本之后，此版本用于生成必需的业务文档。</span><span class="sxs-lookup"><span data-stu-id="a503f-114">Be aware that Business document management allows you to modify templates that are used to produce business documents such as orders, invoices, etc. While a template has been modified and a new version of it has been published, this version is used to generate required business documents.</span></span> <span data-ttu-id="a503f-115">业务文档管理不可用于修改已生成的业务文档。</span><span class="sxs-lookup"><span data-stu-id="a503f-115">Business document management cannot be used to modify already generated business documents.</span></span>

## <a name="supported-deployments"></a><span data-ttu-id="a503f-116">支持的部署</span><span class="sxs-lookup"><span data-stu-id="a503f-116">Supported deployments</span></span>

<span data-ttu-id="a503f-117">现在，只能针对云部署实施业务文档管理功能。</span><span class="sxs-lookup"><span data-stu-id="a503f-117">Currently, the Business document management feature is implemented only for cloud deployments.</span></span> <span data-ttu-id="a503f-118">如果此功能对您的本地部署至关重要，请通过在[灵感](https://experience.dynamics.com/ideas/)站点提供反馈来告知我们。</span><span class="sxs-lookup"><span data-stu-id="a503f-118">If this feature is critical to your on-premises deployment, let us know by providing feedback on the [Ideas](https://experience.dynamics.com/ideas/) site.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="a503f-119">支持的 Microsoft Office 应用程序</span><span class="sxs-lookup"><span data-stu-id="a503f-119">Supported Microsoft Office applications</span></span>

<span data-ttu-id="a503f-120">若要使用业务文档管理和 Microsoft Office 桌面应用程序以 Excel 或 Word 格式编辑文档，则必须安装 Microsoft Office 2010 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="a503f-120">To use Business document management for editing templates in Excel or Word formats by using Microsoft Office desktop applications, you must have Microsoft Office 2010 or later installed.</span></span> <span data-ttu-id="a503f-121">这在云和本地部署中受支持。</span><span class="sxs-lookup"><span data-stu-id="a503f-121">This is supported in cloud and on-premises deployment.</span></span>

## <a name="business-document-availability"></a><span data-ttu-id="a503f-122">业务文档可用性</span><span class="sxs-lookup"><span data-stu-id="a503f-122">Business document availability</span></span>

<span data-ttu-id="a503f-123">公共预览版中支持采用基于 Excel 的模板的以下报告：</span><span class="sxs-lookup"><span data-stu-id="a503f-123">The following reports, with Excel-based templates, will available with the release of the public preview:</span></span>

<span data-ttu-id="a503f-124">**应收帐款**（2019 年 8 月）</span><span class="sxs-lookup"><span data-stu-id="a503f-124">**Accounts receivable** (August 2019)</span></span>

- <span data-ttu-id="a503f-125">销售预付款发票</span><span class="sxs-lookup"><span data-stu-id="a503f-125">Sales advance invoice</span></span>
- <span data-ttu-id="a503f-126">销售订单装箱单</span><span class="sxs-lookup"><span data-stu-id="a503f-126">Sales order packing slip</span></span>

<span data-ttu-id="a503f-127">**应付帐款**（2019 年 8 月）</span><span class="sxs-lookup"><span data-stu-id="a503f-127">**Accounts payable** (August 2019)</span></span>

- <span data-ttu-id="a503f-128">采购预付款发票</span><span class="sxs-lookup"><span data-stu-id="a503f-128">Purchase advance invoice</span></span>
- <span data-ttu-id="a503f-129">采购订单</span><span class="sxs-lookup"><span data-stu-id="a503f-129">Purchase order</span></span>
- <span data-ttu-id="a503f-130">采购订单装箱单</span><span class="sxs-lookup"><span data-stu-id="a503f-130">Purchase order packing slip</span></span>

<span data-ttu-id="a503f-131">将支持更多报告。</span><span class="sxs-lookup"><span data-stu-id="a503f-131">More reports will become available.</span></span> <span data-ttu-id="a503f-132">将单独发送有关更多报告的特殊通知。</span><span class="sxs-lookup"><span data-stu-id="a503f-132">Special notifications about additional reports will be sent separately.</span></span> 

<span data-ttu-id="a503f-133">[Word 和 Excel 中的可配置业务文档报告](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details)中提供了为 2019 年 10 月发行版规划的所有报告的完整列表。</span><span class="sxs-lookup"><span data-stu-id="a503f-133">A complete list of all the reports planned for the October 2019 release can be found in [Configurable business documents reporting in Word and Excel](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details).</span></span> <span data-ttu-id="a503f-134">若要了解有关此功能的详细信息，请完成本主题中的示例。</span><span class="sxs-lookup"><span data-stu-id="a503f-134">To learn more about this feature, complete the example in this topic.</span></span>

## <a name="configure-er-parameters"></a><span data-ttu-id="a503f-135">配置 ER 参数</span><span class="sxs-lookup"><span data-stu-id="a503f-135">Configure ER parameters</span></span>

<span data-ttu-id="a503f-136">因为业务文档管理建立在 ER 框架的基础上，所以必须配置 ER 参数，才能开始使用业务文档管理。</span><span class="sxs-lookup"><span data-stu-id="a503f-136">Because Business document management is built on top of the ER framework, you must configure the ER parameters to start working with Business document management.</span></span> <span data-ttu-id="a503f-137">为此，需要按照[配置电子报告 (ER) 框架](electronic-reporting-er-configure-parameters.md)中的说明设置 ER 参数。</span><span class="sxs-lookup"><span data-stu-id="a503f-137">To do this, you need to set up the ER parameters as described in [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md).</span></span> <span data-ttu-id="a503f-138">还需要按照[创建配置提供商并将其标记为有效](tasks/er-configuration-provider-mark-it-active-2016-11.md)中的说明添加新的配置提供商。</span><span class="sxs-lookup"><span data-stu-id="a503f-138">You also need to add a new configuration provider as described in [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

![ER 工作区](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a><span data-ttu-id="a503f-140">导入 ER 解决方案</span><span class="sxs-lookup"><span data-stu-id="a503f-140">Import ER solutions</span></span>

<span data-ttu-id="a503f-141">在此过程的示例中使用了示例 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="a503f-141">Sample ER configurations are used in the example of this procedure.</span></span> <span data-ttu-id="a503f-142">您必须将包含业务文档模板的 ER 配置导入到 Dynamics 365 Finance 的当前实例中，模板可以使用业务文档管理进行编辑。</span><span class="sxs-lookup"><span data-stu-id="a503f-142">You must import, into your current instance of Dynamics 365 Finance, the ER configurations that contain the business document templates that can be edited by using Business document management.</span></span> <span data-ttu-id="a503f-143">下载以下文件，然后存储在本地，以完成此过程。</span><span class="sxs-lookup"><span data-stu-id="a503f-143">Download, and then locally store the following files to complete this procedure.</span></span>

<span data-ttu-id="a503f-144">**示例 ER 客户开票解决方案**</span><span class="sxs-lookup"><span data-stu-id="a503f-144">**Sample ER customer invoicing solution**</span></span>

| <span data-ttu-id="a503f-145">**文件**</span><span class="sxs-lookup"><span data-stu-id="a503f-145">**File**</span></span>                                  | <span data-ttu-id="a503f-146">**内容**</span><span class="sxs-lookup"><span data-stu-id="a503f-146">**Content**</span></span>                                |
|-------------------------------------------|--------------------------------------------|
| <span data-ttu-id="a503f-147">Customer invoicing model.version.2.xml</span><span class="sxs-lookup"><span data-stu-id="a503f-147">Customer invoicing model.version.2.xml</span></span>    | [<span data-ttu-id="a503f-148">ER 数据模型配置</span><span class="sxs-lookup"><span data-stu-id="a503f-148">ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="a503f-149">Customer FTI report (GER).version.2.3.xml</span><span class="sxs-lookup"><span data-stu-id="a503f-149">Customer FTI report (GER).version.2.3.xml</span></span> | [<span data-ttu-id="a503f-150">普通发票 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="a503f-150">Free text invoice ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

<span data-ttu-id="a503f-151">**示例 ER 付款检查解决方案**</span><span class="sxs-lookup"><span data-stu-id="a503f-151">**Sample ER payment checks solution**</span></span>

| <span data-ttu-id="a503f-152">**文件**</span><span class="sxs-lookup"><span data-stu-id="a503f-152">**File**</span></span>                                  | <span data-ttu-id="a503f-153">**内容**</span><span class="sxs-lookup"><span data-stu-id="a503f-153">**Content**</span></span>                                |
|-------------------------------------------|--------------------------------------------|
| <span data-ttu-id="a503f-154">Model for cheques.version.10.xml</span><span class="sxs-lookup"><span data-stu-id="a503f-154">Model for cheques.version.10.xml</span></span>          | [<span data-ttu-id="a503f-155">ER 数据模型配置</span><span class="sxs-lookup"><span data-stu-id="a503f-155">ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="a503f-156">Cheques printing format.version.10.9.xml</span><span class="sxs-lookup"><span data-stu-id="a503f-156">Cheques printing format.version.10.9.xml</span></span>  | [<span data-ttu-id="a503f-157">付款支票 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="a503f-157">Payment cheque ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

<span data-ttu-id="a503f-158">**示例 ER 外贸解决方案**</span><span class="sxs-lookup"><span data-stu-id="a503f-158">**Sample ER foreign trade solution**</span></span>

| <span data-ttu-id="a503f-159">**文件**</span><span class="sxs-lookup"><span data-stu-id="a503f-159">**File**</span></span>                                  | <span data-ttu-id="a503f-160">**内容**</span><span class="sxs-lookup"><span data-stu-id="a503f-160">**Content**</span></span>                                |
|-------------------------------------------|--------------------------------------------|
| <span data-ttu-id="a503f-161">Intrastat model.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="a503f-161">Intrastat model.version.1.xml</span></span>             | [<span data-ttu-id="a503f-162">ER 数据模型配置</span><span class="sxs-lookup"><span data-stu-id="a503f-162">ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="a503f-163">Intrastat report.version.1.9.xml</span><span class="sxs-lookup"><span data-stu-id="a503f-163">Intrastat report.version.1.9.xml</span></span>          | [<span data-ttu-id="a503f-164">内部统计控制报表 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="a503f-164">Intrastat control report ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

<span data-ttu-id="a503f-165">使用以下过程导入每个文件。</span><span class="sxs-lookup"><span data-stu-id="a503f-165">Use the following procedure to import each file.</span></span> <span data-ttu-id="a503f-166">导入相应 ER *格式*配置之前，导入上表中每个 ER 解决方案的 ER *数据模型*配置。</span><span class="sxs-lookup"><span data-stu-id="a503f-166">Import the ER *data model* configuration of each ER solution in the tables above before you import the corresponding ER *format* configuration.</span></span>

1. <span data-ttu-id="a503f-167">打开**组织管理** \> **电子申报** \> **配置**页面。</span><span class="sxs-lookup"><span data-stu-id="a503f-167">Open the **Organization administration** \> **Electronic reporting** \> **Configurations** page.</span></span>
2. <span data-ttu-id="a503f-168">在页面顶部，选择**交易**。</span><span class="sxs-lookup"><span data-stu-id="a503f-168">On the top of the page, select **Exchange**.</span></span>
3. <span data-ttu-id="a503f-169">选择**从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="a503f-169">Select **Load from XML file**.</span></span>
4. <span data-ttu-id="a503f-170">选择**浏览**以加载所需的 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="a503f-170">Select **Browse** to load the required XML file.</span></span>
5. <span data-ttu-id="a503f-171">选择**确定**以确认导入配置。</span><span class="sxs-lookup"><span data-stu-id="a503f-171">Select **OK** to confirm configuration’s import.</span></span>

![ER 配置页](./media/BDM-Overview-ERSolutions.png)


<span data-ttu-id="a503f-173">或者，您可以从 Microsoft Dynamics Lifecycle Service (LCS) 导入正式发布的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="a503f-173">Alternatively, you can import the officially published ER format configurations from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="a503f-174">例如，要完成此过程，您可以导入**普通发票(Excel)** ER 格式配置的最新版本。</span><span class="sxs-lookup"><span data-stu-id="a503f-174">For example, to complete this procedure you can import the latest version of the **Free text invoice (Excel)** ER format configuration.</span></span> <span data-ttu-id="a503f-175">相应的 ER 数据模型和 ER 模型映射配置将自动导入。</span><span class="sxs-lookup"><span data-stu-id="a503f-175">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

![LCS 共享资产库内容页面](./media/BDM-Overview-SharedAssetLibrary.png)

<span data-ttu-id="a503f-177">有关导入 ER 配置的详细信息，请参阅[管理 ER 配置生命周期](general-electronic-reporting-manage-configuration-lifecycle.md)。</span><span class="sxs-lookup"><span data-stu-id="a503f-177">For more information about importing ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>


## <a name="enable-business-document-management"></a><span data-ttu-id="a503f-178">启用业务文档管理</span><span class="sxs-lookup"><span data-stu-id="a503f-178">Enable Business document management</span></span>

<span data-ttu-id="a503f-179">若要启动业务文档管理，需要打开**功能管理**工作区，并启用**业务文档管理**功能。</span><span class="sxs-lookup"><span data-stu-id="a503f-179">To start Business document management, you need to open the **Feature management** workspace and enable the **Business document management** feature.</span></span>

<span data-ttu-id="a503f-180">使用以下过程为所有法人启用业务文档管理。</span><span class="sxs-lookup"><span data-stu-id="a503f-180">Use the following procedure to enable Business document management functionality for all legal entities.</span></span>

1. <span data-ttu-id="a503f-181">打开**功能管理**工作区。</span><span class="sxs-lookup"><span data-stu-id="a503f-181">Open the **Feature management** workspace.</span></span>
2. <span data-ttu-id="a503f-182">在**新建**选项卡上，选择列表中的**业务文档管理**功能。</span><span class="sxs-lookup"><span data-stu-id="a503f-182">On the **New** tab, select the **Business document management** feature in the list.</span></span>
3. <span data-ttu-id="a503f-183">选择**立即启用**以打开所选功能。</span><span class="sxs-lookup"><span data-stu-id="a503f-183">Select **Enable now** to turn on the selected feature.</span></span>
4. <span data-ttu-id="a503f-184">刷新页面以访问新功能。</span><span class="sxs-lookup"><span data-stu-id="a503f-184">Refresh the page to access the new feature.</span></span>

>[!NOTE]
> <span data-ttu-id="a503f-185">另外，您需要启用**类似于 Office 的业务文档管理 UI 体验**，以使用新的业务文档管理界面</span><span class="sxs-lookup"><span data-stu-id="a503f-185">Also you need to enable **Office-like UI experience for Business document management** for using new business document management interface</span></span>

![“功能管理”工作区](./media/BDM-Overview-FMEnabling.png)

<span data-ttu-id="a503f-187">有关激活新功能的详细信息，请参阅[功能管理概述](../../fin-ops/get-started/feature-management/feature-management-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="a503f-187">For more information about activating new features, see [Feature management overview](../../fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-parameters"></a><span data-ttu-id="a503f-188">配置参数</span><span class="sxs-lookup"><span data-stu-id="a503f-188">Configure parameters</span></span>

<span data-ttu-id="a503f-189">使用以下部分中的信息为业务文档管理设置基本参数。</span><span class="sxs-lookup"><span data-stu-id="a503f-189">Use the information in the following sections to set up the basic parameters for Business document management.</span></span>

### <a name="prerequisites-for-parameter-setup"></a><span data-ttu-id="a503f-190">参数设置的先决条件</span><span class="sxs-lookup"><span data-stu-id="a503f-190">Prerequisites for parameter setup</span></span>
<span data-ttu-id="a503f-191">必须先在文档管理框架中设置必需的文档类型，才能设置业务文档管理。</span><span class="sxs-lookup"><span data-stu-id="a503f-191">Before you can set up Business document management, you must set up the required document type in the Document management framework.</span></span> <span data-ttu-id="a503f-192">此文档类型用于指定 Office 格式（Excel 和 Word）文档的临时存储，用作 ER 报表的模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-192">This document type is used to specify a temporary storage of documents in Office formats (Excel and Word) that are used as templates for ER reports.</span></span> <span data-ttu-id="a503f-193">可使用 Office 桌面应用程序编辑临时存储模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-193">The temporary storage template can be edited by using the Office desktop applications.</span></span>

<span data-ttu-id="a503f-194">对于此文档类型，必须选择以下属性值。</span><span class="sxs-lookup"><span data-stu-id="a503f-194">For this document type, the following attribute values must be selected.</span></span>

| <span data-ttu-id="a503f-195">**属性名称**</span><span class="sxs-lookup"><span data-stu-id="a503f-195">**Attribute name**</span></span>  | <span data-ttu-id="a503f-196">**属性值**</span><span class="sxs-lookup"><span data-stu-id="a503f-196">**Attribute value**</span></span>   |
|---------------------|-----------------------|
| <span data-ttu-id="a503f-197">分类</span><span class="sxs-lookup"><span data-stu-id="a503f-197">Class</span></span>               | <span data-ttu-id="a503f-198">附加文件</span><span class="sxs-lookup"><span data-stu-id="a503f-198">Attach file</span></span>           |
| <span data-ttu-id="a503f-199">组合</span><span class="sxs-lookup"><span data-stu-id="a503f-199">Group</span></span>               | <span data-ttu-id="a503f-200">文件</span><span class="sxs-lookup"><span data-stu-id="a503f-200">File</span></span>                  |
| <span data-ttu-id="a503f-201">场所</span><span class="sxs-lookup"><span data-stu-id="a503f-201">Location</span></span>            | <span data-ttu-id="a503f-202">SharePoint</span><span class="sxs-lookup"><span data-stu-id="a503f-202">SharePoint</span></span>            |

<span data-ttu-id="a503f-203">有关如何设置必需文档管理参数和文档类型的信息，请参阅[配置文档管理](../../fin-ops/organization-administration/configure-document-management.md)。</span><span class="sxs-lookup"><span data-stu-id="a503f-203">For information about how to set up the required document management parameters and document types, see [Configure document management](../../fin-ops/organization-administration/configure-document-management.md).</span></span>

![设置文档管理文档类型](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a><span data-ttu-id="a503f-205">设置参数</span><span class="sxs-lookup"><span data-stu-id="a503f-205">Set up parameters</span></span>

<span data-ttu-id="a503f-206">可在**业务文档参数**页设置基本业务文档管理参数。</span><span class="sxs-lookup"><span data-stu-id="a503f-206">Basic Business document management parameters can be set up on the **Business document parameters** page.</span></span> <span data-ttu-id="a503f-207">只有特定用户才可以访问此页。</span><span class="sxs-lookup"><span data-stu-id="a503f-207">Only specific users can access the page.</span></span> <span data-ttu-id="a503f-208">这包括：</span><span class="sxs-lookup"><span data-stu-id="a503f-208">This includes:</span></span>

- <span data-ttu-id="a503f-209">已为其分配了**系统管理员**角色的用户。</span><span class="sxs-lookup"><span data-stu-id="a503f-209">Users who are assigned to the **System administrator** role.</span></span>
- <span data-ttu-id="a503f-210">已为其分配了为执行**维护业务文档管理参数**（AOT 名称为 **ERBDMaintainParameters**）职责而配置的任何角色的用户。</span><span class="sxs-lookup"><span data-stu-id="a503f-210">Users who are assigned to any role that is configured to perform the duty, **Maintain Business document management parameters** (AOT name **ERBDMaintainParameters**).</span></span>

<span data-ttu-id="a503f-211">使用以下过程为所有法人设置基本参数。</span><span class="sxs-lookup"><span data-stu-id="a503f-211">Use the following procedure to set up the basic parameters for all legal entities.</span></span>

1. <span data-ttu-id="a503f-212">以具有**业务文档参数**页面访问权限的用户的身份登录。</span><span class="sxs-lookup"><span data-stu-id="a503f-212">Sign in as a user with access to the **Business document parameters** page.</span></span>
2. <span data-ttu-id="a503f-213">转到**组织管理** \> **电子申报** \> **业务文档管理** \> **业务文档参数**。</span><span class="sxs-lookup"><span data-stu-id="a503f-213">Go to **Organization administration** \> **Electronic reporting** \> **Business document management** \> **Business document parameters**.</span></span>
3.  <span data-ttu-id="a503f-214">在**业务文档参数**页**附件**选项卡的 **SharePoint 文档类型**字段中，定义应该用于在使用 Office 桌面应用程序编辑 Office 格式的模板时，临时存储此类模板的文档类型。</span><span class="sxs-lookup"><span data-stu-id="a503f-214">On the **Business document parameters** page, on the **Attachments** tab, in the **SharePoint document type** field, define the document type that should be used to temporarily store templates in Office formats while they are edited using the Office desktop applications.</span></span> 

> [!NOTE]
> <span data-ttu-id="a503f-215">此参数仅支持使用 SharePoint 位置配置的文档类型。</span><span class="sxs-lookup"><span data-stu-id="a503f-215">Only document types that are configured using a SharePoint location are available for this parameter.</span></span>

![设置业务文档管理参数](./media/BDM-Overview-BDMSetting.png)

<span data-ttu-id="a503f-217">所选文档类型特定于公司，将在当用户在为其配置了所选文档类型的公司中使用业务文档管理时使用。</span><span class="sxs-lookup"><span data-stu-id="a503f-217">The selected document type is company-specific and will be used when the user is working with Business document management in the company for which the selected document type is configured.</span></span> <span data-ttu-id="a503f-218">当用户在另一家公司使用业务文档管理时，如果尚未为此公司配置文档类型，将使用选择的同一个文档类型。</span><span class="sxs-lookup"><span data-stu-id="a503f-218">When the user is working with Business document management in another company, the same selected document type will be used if one has not been configured for this company.</span></span> <span data-ttu-id="a503f-219">如果已配置了文档类型，则使用此文档类型，而不是在 **SharePoint 文档类型**字段中选择的文档类型。</span><span class="sxs-lookup"><span data-stu-id="a503f-219">When a document type has been configured, it will be used instead of the one selected in the **SharePoint document type** field.</span></span>

## <a name="configure-access-permissions"></a><span data-ttu-id="a503f-220">配置访问权限</span><span class="sxs-lookup"><span data-stu-id="a503f-220">Configure access permissions</span></span>

<span data-ttu-id="a503f-221">默认情况下，在未启用业务文档管理权限的访问时，每位可访问业务文档管理工作区的用户都可以看到所有可用 ER 解决方案模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-221">By default, when access to Business document management permissions is not enabled, every user with access to the Business document management workspace will see all of the ER solution templates that are available.</span></span> <span data-ttu-id="a503f-222">业务文档管理工作区将仅显示 ER 格式配置中的模板和带有**业务文档类型**标记的模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-222">The Business document management workspace will show only those templates that reside in ER format configurations and that are marked by a **Business document type** tag.</span></span>

![ER 配置页](./media/BDM-Overview-ERFormatTags.png)

<span data-ttu-id="a503f-224">可通过配置访问权限来限制业务文档管理工作区中的可用模板的列表。</span><span class="sxs-lookup"><span data-stu-id="a503f-224">The list of templates available in the Business document management workspace can be restricted by configuring access permissions.</span></span> <span data-ttu-id="a503f-225">这在以下情况下可能非常重要：使用不同模板为不同业务域（功能区）生成业务文档，并且要允许特定用户访问要在业务文档管理工作区中进行编辑的不同模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-225">This may be important when different templates are used to produce business documents for different business domains (functional areas), and you want to allow specific users access to different templates for editing in the Business document management workspace.</span></span>

<span data-ttu-id="a503f-226">可在**配置权限的配置器**中设置业务文档管理访问权限。</span><span class="sxs-lookup"><span data-stu-id="a503f-226">Business document management access permissions can be set on the **Configurator of access permissions**.</span></span> <span data-ttu-id="a503f-227">只有以下用户才可以访问此页：</span><span class="sxs-lookup"><span data-stu-id="a503f-227">Only the following users can access the page:</span></span>

- <span data-ttu-id="a503f-228">已为其分配了**系统管理员**角色的用户。</span><span class="sxs-lookup"><span data-stu-id="a503f-228">Users assigned to the **System administrator** role.</span></span>
- <span data-ttu-id="a503f-229">已为其分配了为执行**配置权限以访问要编辑的业务文档模板**（AOT 名称为 **ERBDTemplatesSecurity**）职责而配置的其他任何角色的用户。</span><span class="sxs-lookup"><span data-stu-id="a503f-229">Users assigned to any other role that is configured to perform the duty, **Configure permissions to access Business document templates for editing** (AOT name **ERBDTemplatesSecurity**).</span></span>

<span data-ttu-id="a503f-230">使用以下过程为所有法人设置业务文档管理访问权限。</span><span class="sxs-lookup"><span data-stu-id="a503f-230">Use the following procedure to set up the access Business document management permissions for all legal entities.</span></span>

1. <span data-ttu-id="a503f-231">以具有**访问权限配置器**页面访问权限的用户的身份登录。</span><span class="sxs-lookup"><span data-stu-id="a503f-231">Sign in as a user with access to the **Configurator of access permissions** page.</span></span>
2. <span data-ttu-id="a503f-232">转到**组织管理** \> **电子申报** \> **业务文档管理** \> **管理访问权限**。</span><span class="sxs-lookup"><span data-stu-id="a503f-232">Go to **Organization administration** \> **Electronic reporting** \> **Business document management** \> **Manage access permissions**.</span></span>

    <span data-ttu-id="a503f-233">请注意有关当前未启用业务文档管理访问权限的使用的通知。</span><span class="sxs-lookup"><span data-stu-id="a503f-233">Pay attention to the notification informing you that the usage of access permissions for Business document management is currently not enabled.</span></span>

    ![“业务文档管理访问权限配置器”页面](./media/BDM-Overview-TemplatesAccess1.png)

    <span data-ttu-id="a503f-235">通过此设置，已为其分配了为执行**管理业务文档模板**（AOT 名称为 **ERBDManageTemplates**）职责而配置的任何安全角色的每位用户都可以打开业务文档管理工作区，并可编辑所有可用模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-235">With this setting, every user assigned to any security role that is configured to perform the **Manage Business document templates** (AOT name **ERBDManageTemplates**) duty is able to open the Business document management workspace and can edit any template that is available.</span></span>

    <span data-ttu-id="a503f-236">下图显示业务文档管理工作区中为其分配了**应收帐款员**角色的用户的可用模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-236">The following graphic shows what is available in the Business document management workspace for users assigned to the **Accounts receivable clerk** role.</span></span> <span data-ttu-id="a503f-237">通过使用当前访问权限设置，用户可从不同功能区（包括开票、法规报告和付款）编辑业务文档模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-237">With the current access permissions setting, the user can edit business document templates from different functional areas including invoicing, regulatory reporting, and payments.</span></span>

    ![业务文档管理工作区页](./media/BDM-Overview-TemplatesForAlice1.png)

3. <span data-ttu-id="a503f-239">在**访问权限配置器**页，选择**访问权限设置**。</span><span class="sxs-lookup"><span data-stu-id="a503f-239">On the **Configurator of access permissions** page, select **Access permissions setting**.</span></span>
4. <span data-ttu-id="a503f-240">在**用于编辑模板的访问权限的设置**对话框中，启用**应用已配置的访问权限**选项。</span><span class="sxs-lookup"><span data-stu-id="a503f-240">In the **Settings of access permissions to edit templates** dialog box, enable the **Apply configured access permissions** option.</span></span>
5. <span data-ttu-id="a503f-241">选择**确定**以确认已启用业务文档管理访问权限。</span><span class="sxs-lookup"><span data-stu-id="a503f-241">Select **OK** to confirm that Business document management access permissions have been enabled.</span></span>

    ![“配置业务文档管理访问权限”页面](./media/BDM-Overview-TemplatesAccess2.png)

6. <span data-ttu-id="a503f-243">选择**添加**以输入必须要为其配置用于访问业务文档管理模板的权限的新业务角色。</span><span class="sxs-lookup"><span data-stu-id="a503f-243">Select **Add** to enter a new business role for which permissions to access Business document management templates must be configured.</span></span>
7. <span data-ttu-id="a503f-244">在**安全角色**对话框中，选择**应收帐款员**角色，然后选择**确定**以确认选择的角色。</span><span class="sxs-lookup"><span data-stu-id="a503f-244">In the **Security roles** dialog box, select the **Accounts receivable clerk** role and then select **OK** to confirm the role selection.</span></span>
8. <span data-ttu-id="a503f-245">在**每个配置标记的访问权限**选项卡上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="a503f-245">On the **Access permissions per tags of configurations** tab, select **New**.</span></span>
9. <span data-ttu-id="a503f-246">在**标记类型**字段中，选择**功能区**，然后在 **ID** 字段中选择**开票**。</span><span class="sxs-lookup"><span data-stu-id="a503f-246">In the **Tag type** field, select **Functional area**, and in the **ID** field, select **Invoicing**.</span></span>
10. <span data-ttu-id="a503f-247">选择**保存**以存储为所选角色配置的访问权限。</span><span class="sxs-lookup"><span data-stu-id="a503f-247">Select **Save** to store configured access permissions for the selected role.</span></span>

    <span data-ttu-id="a503f-248">当前设置意味着对于为其分配了**应收帐款员**角色且正在执行**管理业务文档模板**（AOT 名称为 **ERBDManageTemplates**）职责的任何用户，可在业务文档管理工作区中编辑**功能区**标记值为**开票**的 ER 格式配置模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-248">The current setting means that for any user who is assigned to the **Accounts receivable clerk** role and performing the duty, **Manage Business document templates** (AOT name **ERBDManageTemplates**), ER format configuration templates that have the **Invoicing** value for the **Functional area** tag will be available to edit in the Business document management workspace.</span></span>

11. <span data-ttu-id="a503f-249">从当前页右侧切换**相关信息**窗格。</span><span class="sxs-lookup"><span data-stu-id="a503f-249">Switch the **Related information** pane from the right side of the current page.</span></span> <span data-ttu-id="a503f-250">**相关信息**窗格显示如何应用配置的访问权限，包括为其分配了**应收帐款员**角色的用户可使用哪些 ER 配置模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-250">The **Related information** pane shows how the configured access permissions will be applied, including what ER configuration templates will be available for users that are assigned to the **Accounts receivable clerk** role.</span></span>

    ![“配置业务文档管理访问权限”页面](./media/BDM-Overview-TemplatesAccess3.png)

12. <span data-ttu-id="a503f-252">在**每个配置的访问权限**选项卡上，选择**添加**选项。</span><span class="sxs-lookup"><span data-stu-id="a503f-252">On the **Access permissions per configurations** tab, select the **Add** option.</span></span>
13. <span data-ttu-id="a503f-253">在**选择配置**对话框中，标记**内部统计报表** ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="a503f-253">In the **Select configuration** dialog box, mark the **Intrastat report** ER format configuration.</span></span>
14. <span data-ttu-id="a503f-254">选择**确定**以确认所选配置的条目，然后选择**保存**以存储为所选角色配置的访问权限。</span><span class="sxs-lookup"><span data-stu-id="a503f-254">Select **OK** to confirm the entry of the selected configurations and then select **Save** to store the configured access permissions for the selected role.</span></span>

<span data-ttu-id="a503f-255">当前设置意味着对于为其分配了**应收帐款员**角色且正在执行**管理业务文档模板**（AOT 名称为 **ERBDManageTemplates**）职责的任何用户，可在业务文档管理工作区中编辑以下模板：</span><span class="sxs-lookup"><span data-stu-id="a503f-255">The current setting means that for any user assigned to the **Accounts receivable clerk** role and performing the duty, **Manage Business document templates** (AOT name **ERBDManageTemplates**), the following templates will be available to edit in the Business document management workspace:</span></span>

- <span data-ttu-id="a503f-256">**功能区**标记的值为**开票**的模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-256">Templates that have the value, **Invoicing** for the **Functional area** tag.</span></span>
- <span data-ttu-id="a503f-257">来自**每个配置的访问权限**选项卡上列出的 ER 格式配置的模板（此示例中，为来自**法定申报**域的**内部统计报表**格式配置的模板）。</span><span class="sxs-lookup"><span data-stu-id="a503f-257">Templates from ER format configurations that are listed on the **Access permissions per configurations** tab (templates from the **Intrastat report** format configuration of the **Statutory reporting** domain in this example).</span></span>

![“配置业务文档管理访问权限”页面](./media/BDM-Overview-TemplatesAccess4.png)

<span data-ttu-id="a503f-259">下图显示业务文档管理工作区向为其分配了**应收帐款员**角色的用户提供的模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-259">The following graphic shows what the Business document management workspace provides to a user assigned to the **Accounts receivable clerk** role.</span></span> <span data-ttu-id="a503f-260">采用当前业务文档管理访问权限设置的用户可编辑**开票**域和**内部统计报表** ER 格式配置中的业务文档模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-260">With the current Business document management access permissions setting, the user can edit business document templates from the **Invoicing** domain and the **Intrastat report** ER format configuration.</span></span> <span data-ttu-id="a503f-261">**应收帐款员**角色不可访问**付款**域中的模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-261">Templates from the **Payments** domain are not accessible for the **Accounts receivable clerk** role.</span></span>

![业务文档管理工作区页](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> <span data-ttu-id="a503f-263">**每个配置的访问权限**规则通过使用 ER 格式配置的唯一标识 ID 来存储。</span><span class="sxs-lookup"><span data-stu-id="a503f-263">The **Access permissions per configurations** rules are stored by using the unique identification ID of an ER format configuration.</span></span> <span data-ttu-id="a503f-264">这意味着如果删除引用这些规则的 ER 配置，不会删除这些规则。</span><span class="sxs-lookup"><span data-stu-id="a503f-264">This means that these rules will not be deleted when an ER configuration that refers to them are deleted.</span></span> <span data-ttu-id="a503f-265">将删除的配置导入回此实例时，这些规则将再次引用这些配置。</span><span class="sxs-lookup"><span data-stu-id="a503f-265">When you import deleted configurations back to this instance, these rules will refer to them again.</span></span> <span data-ttu-id="a503f-266">再次导入删除的配置之后，无需再次设置规则。</span><span class="sxs-lookup"><span data-stu-id="a503f-266">There is no need to set up the rules again after the deleted configurations are imported again.</span></span>

## <a name="use-business-document-management-to-edit-templates"></a><span data-ttu-id="a503f-267">使用业务文档管理编辑模板</span><span class="sxs-lookup"><span data-stu-id="a503f-267">Use Business document management to edit templates</span></span>

<span data-ttu-id="a503f-268">业务用户可在业务文档管理工作区中访问要编辑的业务文档模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-268">Business users can access business document templates for editing in the Business document management workspace.</span></span> <span data-ttu-id="a503f-269">只有以下用户可访问业务文档管理工作区：</span><span class="sxs-lookup"><span data-stu-id="a503f-269">Only the following users can access the Business document management workspace:</span></span>

- <span data-ttu-id="a503f-270">已为其分配了**系统管理员**角色的用户。</span><span class="sxs-lookup"><span data-stu-id="a503f-270">Users assigned to the role, **System administrator**.</span></span>
- <span data-ttu-id="a503f-271">已为其分配了为执行**管理业务文档模板**（AOT 名称为 **ERBDManageTemplates**）职责而配置的任何角色的用户。</span><span class="sxs-lookup"><span data-stu-id="a503f-271">Users assigned to any role that is configured to perform the duty, **Manage Business document templates** (AOT name **ERBDManageTemplates**).</span></span>

<span data-ttu-id="a503f-272">在业务文档管理工作区中使用以下过程编辑普通发票模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-272">Use the following procedure to edit free text invoice templates in the Business document management workspace.</span></span> <span data-ttu-id="a503f-273">完成此过程之前，必须先完成本主题中前文的所有过程。</span><span class="sxs-lookup"><span data-stu-id="a503f-273">Before you complete this procedure, you must have completed all of the preceding procedures in this topic.</span></span>

1. <span data-ttu-id="a503f-274">以具有业务文档管理工作区访问权限的用户的身份登录。</span><span class="sxs-lookup"><span data-stu-id="a503f-274">Sign in as a user with access to the Business document management workspace.</span></span>
2. <span data-ttu-id="a503f-275">打开业务文档管理工作区。</span><span class="sxs-lookup"><span data-stu-id="a503f-275">Open the Business document management workspace.</span></span>

![业务文档管理工作区页](./media/BDM-Overview-EditingTemplate1.png)

<span data-ttu-id="a503f-277">**模板**选项卡中提供所选模板的内容。</span><span class="sxs-lookup"><span data-stu-id="a503f-277">The **Template** tab presents the content of the selected template.</span></span> <span data-ttu-id="a503f-278">选择**详细信息**选项卡以查看所选模板的详细信息，以及此模板所在 ER 格式配置的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a503f-278">Select the **Details** tab to review details of the selected template as well as details of an ER format configuration this template resides in.</span></span> <span data-ttu-id="a503f-279">请注意，所有模板的状态均为**已发布**，并且其**修订**列中不包含任何详细信息。</span><span class="sxs-lookup"><span data-stu-id="a503f-279">Notice that all of the templates have a status of **Published**, and contain no details in the **Revision** column.</span></span> <span data-ttu-id="a503f-280">这表示当前未在编辑这些模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-280">This means that these templates are not currently being edited.</span></span>

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a><span data-ttu-id="a503f-281">开始编辑配置提供商负责的模板</span><span class="sxs-lookup"><span data-stu-id="a503f-281">Initiate editing templates owned by your configuration provider</span></span>

1. <span data-ttu-id="a503f-282">在业务文档管理工作区中，选择列表中的 **Cheques printing format** 模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-282">In the Business document management workspace, select the **Cheques printing format** template in the list.</span></span>
2. <span data-ttu-id="a503f-283">选择**详细信息**选项卡。</span><span class="sxs-lookup"><span data-stu-id="a503f-283">Select the **Details** tab.</span></span>

![业务文档管理工作区页](./media/BDM-Overview-EditingTemplate2.png)

<span data-ttu-id="a503f-285">将为所选模板提供**编辑模板**选项。</span><span class="sxs-lookup"><span data-stu-id="a503f-285">The **Edit template** option is available for the selected template.</span></span> <span data-ttu-id="a503f-286">有效 ER 配置提供商（此示例中为 **Litware, Inc.**）负责的 ER 格式配置中的模板始终可使用此选项。</span><span class="sxs-lookup"><span data-stu-id="a503f-286">This option is always available for a template in an ER format configuration that is owned by the active ER configuration provider (**Litware, Inc.** in this example).</span></span> <span data-ttu-id="a503f-287">如果选择了**编辑模板**，则可编辑基础 ER 格式配置草稿版本中的现有模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-287">When **Edit template** is selected, the existing template from the draft version of the underlying ER format configuration will be available to edit.</span></span>

### <a name="initiate-editing-templates-owned-by-other-providers"></a><span data-ttu-id="a503f-288">开始编辑其他提供商负责的模板</span><span class="sxs-lookup"><span data-stu-id="a503f-288">Initiate editing templates owned by other providers</span></span>

1. <span data-ttu-id="a503f-289">在业务文档管理工作区中，选择**新建文档**。</span><span class="sxs-lookup"><span data-stu-id="a503f-289">In the Business document management workspace, select the **New document**.</span></span>

![业务文档管理工作区页](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="a503f-291">选择您要用作模板的文档。</span><span class="sxs-lookup"><span data-stu-id="a503f-291">Select the document that you want to use as a template.</span></span>

![业务文档管理工作区页](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="a503f-293">单击**创建文档**</span><span class="sxs-lookup"><span data-stu-id="a503f-293">Click **Create document**</span></span>
4. <span data-ttu-id="a503f-294">如果需要，在**标题**字段中更改可编辑模板的标题。</span><span class="sxs-lookup"><span data-stu-id="a503f-294">In the **Title** field, change the title of the editable template if needed.</span></span> <span data-ttu-id="a503f-295">将把此文本用于命名自动创建的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="a503f-295">The text will be used to name the ER format configuration that is automatically created.</span></span> <span data-ttu-id="a503f-296">请注意，将自动标记此配置 (**Customer FTI report (GER) Copy**) 的草稿版本（其中将包含编辑后的模板），以便为当前用户运行此 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="a503f-296">Note that the draft version of this configuration (**Customer FTI report (GER) Copy**) that will contain the edited template will automatically be marked to run this ER format for the current user.</span></span> <span data-ttu-id="a503f-297">同时，将使用来自基本 ER 格式配置的未经修改原始模板为其他任何用户运行此 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="a503f-297">At the same time, the non-modified original template from the base ER format configuration will be used to run this ER format for any other user.</span></span>
5. <span data-ttu-id="a503f-298">在**名称**字段中，更改将自动创建的可编辑模板第一个修订的名称。</span><span class="sxs-lookup"><span data-stu-id="a503f-298">In the **Name** field, change the name of the first revision of the editable template that will be created automatically.</span></span>
6. <span data-ttu-id="a503f-299">在**注释**字段中，更改自动创建的可编辑模板修订的注解。</span><span class="sxs-lookup"><span data-stu-id="a503f-299">In the **Comment** field, change the remark for the automatically created revision of the editable template.</span></span>
7. <span data-ttu-id="a503f-300">选择**确定**以确认开始执行编辑流程</span><span class="sxs-lookup"><span data-stu-id="a503f-300">Select **OK** to confirm the start of the editing process</span></span>

![业务文档管理工作区页](./media/BDM_overview_new_template3.png)

<span data-ttu-id="a503f-302">另一个提供商（此示例中为 Microsoft）提供的 ER 格式配置中的模板始终可使用**新建文档**选项。</span><span class="sxs-lookup"><span data-stu-id="a503f-302">The **New document** option is always available for a template in an ER format configuration provided by another provider (Microsoft in this example).</span></span> <span data-ttu-id="a503f-303">当您单击**新建文档**时，您会看到当前提供商和其他提供商拥有的所有模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-303">When you click **New document**  you see all templates owned by current and other providers.</span></span> <span data-ttu-id="a503f-304">选择模板后，将打开它进行编辑。</span><span class="sxs-lookup"><span data-stu-id="a503f-304">After you choose the template it will be opened for editing.</span></span> <span data-ttu-id="a503f-305">然后将把编辑后的模板存储在自动生成的新 ER 格式配置中。</span><span class="sxs-lookup"><span data-stu-id="a503f-305">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

### <a name="start-editing-a-template"></a><span data-ttu-id="a503f-306">开始编辑模板</span><span class="sxs-lookup"><span data-stu-id="a503f-306">Start editing a template</span></span>

1. <span data-ttu-id="a503f-307">从所选模板选择**编辑文档**。</span><span class="sxs-lookup"><span data-stu-id="a503f-307">From the selected template, select **Edit document**.</span></span>
2. <span data-ttu-id="a503f-308">在**名称**字段中，更改将自动创建的可编辑模板第一个修订的名称。</span><span class="sxs-lookup"><span data-stu-id="a503f-308">In the **Name** field, change the name of the first revision of the editable template that will be created automatically.</span></span>
3. <span data-ttu-id="a503f-309">在**注释**字段中，更改自动创建的可编辑模板修订的注解。</span><span class="sxs-lookup"><span data-stu-id="a503f-309">In the **Comment** field, change the remark for the automatically created revision of the editable template.</span></span>

    ![业务文档管理工作区页](./media/BDM_overview_new_template4.png)

5. <span data-ttu-id="a503f-311">选择**确定**以确认开始执行编辑流程。</span><span class="sxs-lookup"><span data-stu-id="a503f-311">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="a503f-312">将打开 **BDM 模板编辑器**页。</span><span class="sxs-lookup"><span data-stu-id="a503f-312">The **BDM template editor** page will open.</span></span> <span data-ttu-id="a503f-313">可通过使用 Office 365 在线编辑所选模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-313">The selected template will be available for online editing by using Office 365.</span></span>

![业务文档管理工作区页](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-office-365"></a><span data-ttu-id="a503f-315">在 Office 365 中编辑模板</span><span class="sxs-lookup"><span data-stu-id="a503f-315">Edit a template in Office 365</span></span>

<span data-ttu-id="a503f-316">通过使用 Office 365 的功能修改模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-316">Modify the template by using the functionality of the Office 365.</span></span> <span data-ttu-id="a503f-317">例如，在 Office Online 中，将模板标题中的字段提示的字体从**常规**更改为**加粗**。</span><span class="sxs-lookup"><span data-stu-id="a503f-317">For example, in Office online, change the font of the field prompts in the template header from **Regular** to **Bold**.</span></span> <span data-ttu-id="a503f-318">将自动存储为 ER 框架配置的主模板存储（默认情况下为 Azure blob 存储）中存储的可编辑模板的这些更改。</span><span class="sxs-lookup"><span data-stu-id="a503f-318">These changes are automatically stored for the editable template that is stored in the primary template’s storage (by default, the Azure blob storage) that is configured for the ER framework.</span></span>

![业务文档管理模板编辑器页面](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a><span data-ttu-id="a503f-320">在 Office 桌面应用程序中编辑模板</span><span class="sxs-lookup"><span data-stu-id="a503f-320">Edit a template in the Office desktop application</span></span>

1. <span data-ttu-id="a503f-321">选择**在桌面应用程序中打开**选项，以便使用 Office 桌面应用程序的功能（此示例中为 Excel）修改模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-321">Select the **Open in Desktop App** option to modify the template by using the functionality of the Office desktop application (Excel in this example).</span></span> <span data-ttu-id="a503f-322">将把可编辑模板从永久存储复制到业务文档管理参数中配置为 SharePoint 文件夹的临时存储。</span><span class="sxs-lookup"><span data-stu-id="a503f-322">The editable template is copied from the permanent storage to the temporary storage configured in the Business document management parameters as a SharePoint folder.</span></span>
2. <span data-ttu-id="a503f-323">确认要在 Office 桌面的 Excel 应用程序中从临时文件存储打开模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-323">Confirm that you want to open the template from the temporary file storage in the Office desktop Excel application.</span></span>

    ![业务文档管理工作区页](./media/BDM-Overview-EditingLayout3.png)

3. <span data-ttu-id="a503f-325">修改模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-325">Modify the template.</span></span> <span data-ttu-id="a503f-326">例如，通过将颜色从**黑色**更改为**蓝色**，更改模板标题中的字段提示的字体。</span><span class="sxs-lookup"><span data-stu-id="a503f-326">For example, change the font of the fields prompts in the template header by updating color from **Black** to **Blue**.</span></span>

    ![业务文档管理模板编辑器页面](./media/BDM-Overview-EditingLayout4.png)

4. <span data-ttu-id="a503f-328">在 Excel 桌面应用程序中选择**保存**以将模板更改存储到临时存储中。</span><span class="sxs-lookup"><span data-stu-id="a503f-328">Select **Save** in the Excel desktop application to store the template changes in the temporary storage.</span></span>

    ![业务文档管理模板编辑器页面](./media/BDM-Overview-EditingLayout5.png)

5. <span data-ttu-id="a503f-330">关闭 Excel 桌面应用程序。</span><span class="sxs-lookup"><span data-stu-id="a503f-330">Close the Excel desktop application.</span></span>
6. <span data-ttu-id="a503f-331">选择**同步已存储副本**将临时模板存储同步到永久模板存储。</span><span class="sxs-lookup"><span data-stu-id="a503f-331">Select **Sync stored copy** to synchronize the temporary template storage to the permanent template storage.</span></span>

> [!NOTE]
> <span data-ttu-id="a503f-332">临时文件存储中的可编辑模板副本将仅保留在当前模板编辑会话中。</span><span class="sxs-lookup"><span data-stu-id="a503f-332">The copy of the editable template in the temporary file storage is kept for only the current session of template editing.</span></span> <span data-ttu-id="a503f-333">通过关闭 **BDM 模板编辑器**页完成会话时，将删除此副本。</span><span class="sxs-lookup"><span data-stu-id="a503f-333">When you finish this session by closing the **BDM template editor** page, this copy will be deleted.</span></span> <span data-ttu-id="a503f-334">如果调整了临时文件存储中的模板，但是未选择**同步已存储副本**，则在尝试关闭 **BDM 模板编辑器**页时，将有一条消息询问您是否要存储引入的更改。</span><span class="sxs-lookup"><span data-stu-id="a503f-334">If you adjusted the template in the temporary file storage and did not select **Sync stored copy**, when you try to close the **BDM template editor** page, a message will ask whether you want to store introduced changes.</span></span> <span data-ttu-id="a503f-335">如果要将对模板的更改保存到永久文件存储，请选择**是**。</span><span class="sxs-lookup"><span data-stu-id="a503f-335">Select **Yes** if you want to save your changes to the template in the permanent file location.</span></span>

### <a name="validate-a-template"></a><span data-ttu-id="a503f-336">验证模板</span><span class="sxs-lookup"><span data-stu-id="a503f-336">Validate a template</span></span>

1. <span data-ttu-id="a503f-337">在 **BDM 模板编辑器**页中，选择**检查问题**以针对基础 ER 格式配置验证修改后的模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-337">On the **BDM template editor** page, select **Check for issues** to validate the modified template against the underlying ER format configuration.</span></span> <span data-ttu-id="a503f-338">按照建议（如果有）让模板与基本 ER 格式配置中的格式结构一致。</span><span class="sxs-lookup"><span data-stu-id="a503f-338">Follow the recommendations (if any) to align the template with the structure of the format from the base ER format configuration.</span></span>
2. <span data-ttu-id="a503f-339">选择**显示格式**以查看基本 ER 格式配置中必须与可编辑模板一致的当前格式结构。</span><span class="sxs-lookup"><span data-stu-id="a503f-339">Select **Show format** to view the current structure of the format from the base ER format configuration that must be aligned with the editable template.</span></span> 
3. <span data-ttu-id="a503f-340">选择**隐藏格式**以关闭窗格。</span><span class="sxs-lookup"><span data-stu-id="a503f-340">Select **Hide format** to close the pane.</span></span>

    ![BDM 模板编辑器页面](./media/BDM-Overview-EditingTemplate6.png)

4. <span data-ttu-id="a503f-342">关闭 **BDM 模板编辑器**页。</span><span class="sxs-lookup"><span data-stu-id="a503f-342">Close the **BDM template editor** page.</span></span>

<span data-ttu-id="a503f-343">将在**模板**选项卡上显示更新后的模板。请注意，现在，编辑后的模板的状态为**草稿**，并且当前修订不再为空。</span><span class="sxs-lookup"><span data-stu-id="a503f-343">The updated template is shown on the **Template** tab. Notice that the status of the edited template is now **Draft** and the current revision is no longer empty.</span></span> <span data-ttu-id="a503f-344">这意味着此模板的编辑过程已开始。</span><span class="sxs-lookup"><span data-stu-id="a503f-344">This means that the process of this template’s editing has been started.</span></span>

![业务文档管理工作区页](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a><span data-ttu-id="a503f-346">测试修改后的模板</span><span class="sxs-lookup"><span data-stu-id="a503f-346">Test the modified template</span></span> 

1. <span data-ttu-id="a503f-347">在应用程序中，切换到公司 **USMF**。</span><span class="sxs-lookup"><span data-stu-id="a503f-347">In the application, change to the company, **USMF**.</span></span>
2. <span data-ttu-id="a503f-348">转至**应收帐款** \> **发票** \> **所有普通发票**。</span><span class="sxs-lookup"><span data-stu-id="a503f-348">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
3. <span data-ttu-id="a503f-349">选择 **FTI-00000002** 发票，然后选择**打印管理**。</span><span class="sxs-lookup"><span data-stu-id="a503f-349">Select the **FTI-00000002** invoice, and then select **Print management**.</span></span>
4. <span data-ttu-id="a503f-350">选择**模块 - 应收帐款** \> **文档** \> **普通发票** \> **原始凭证**级别以指定要处理的发票范围。</span><span class="sxs-lookup"><span data-stu-id="a503f-350">Select the **Module - accounts receivable** \> **Documents** \> **Free text invoice** \> **Original document** level to specify the scope of invoices for processing.</span></span>
5. <span data-ttu-id="a503f-351">在**报表格式**字段中，为指定的文档级别选择 **Customer FTI report (GER) Copy** ER 格式。</span><span class="sxs-lookup"><span data-stu-id="a503f-351">In the **Report format** field, select the **Customer FTI report (GER) Copy** ER format for the specified document level.</span></span>

    ![打印管理设置页](./media/BDM-Overview-TestRun1.png)

6. <span data-ttu-id="a503f-353">按 **Escape** 关闭当前页。</span><span class="sxs-lookup"><span data-stu-id="a503f-353">Press **Escape** to close the current page.</span></span>
7. <span data-ttu-id="a503f-354">选择**打印**，然后单击**已选择**。</span><span class="sxs-lookup"><span data-stu-id="a503f-354">Select **Print**, and then click **Selected**.</span></span>
8. <span data-ttu-id="a503f-355">下载文档，然后使用 Excel 桌面应用程序打开。</span><span class="sxs-lookup"><span data-stu-id="a503f-355">Download the document and open it using the Excel desktop application.</span></span>

![普通发票页面](./media/BDM-Overview-TestRun2.png)

<span data-ttu-id="a503f-357">修改后的模板将用于为所选物料生成普通发票报表。</span><span class="sxs-lookup"><span data-stu-id="a503f-357">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="a503f-358">若要分析为模板进行的更改对此报表造成了哪些影响，可以在一个应用程序会话中修改模板之后，立即在另一个应用程序会话中运行此报表。</span><span class="sxs-lookup"><span data-stu-id="a503f-358">To analyze how this report is affected by the changes that you introduced to the template, you can run this report in one application session right after you modified the template in another application session.</span></span>

### <a name="create-an-alternative-template-revision"></a><span data-ttu-id="a503f-359">创建备用模板修订</span><span class="sxs-lookup"><span data-stu-id="a503f-359">Create an alternative template revision</span></span>

1. <span data-ttu-id="a503f-360">打开 **BDM 模板编辑器**页，然后选择 **Customer FTI report (GER) Copy** 模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-360">Open the **BDM template editor** page and select the **Customer FTI report (GER) Copy** template.</span></span>
2. <span data-ttu-id="a503f-361">在**修订**选项卡上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="a503f-361">On the **Revisions** tab, select **New**.</span></span>
3. <span data-ttu-id="a503f-362">如果需要，在**名称**字段中，更改第二个修订的名称，并以当前第一个有效修订为基础。</span><span class="sxs-lookup"><span data-stu-id="a503f-362">If needed, in the **Name** field, change the name of the second revision and base it on the currently active first revision.</span></span>
4. <span data-ttu-id="a503f-363">如果需要，在**注释**字段中，更改自动创建的可编辑模板修订的注解。</span><span class="sxs-lookup"><span data-stu-id="a503f-363">If needed, in the **Comment** field, change the remark for the automatically created revision of the editable template.</span></span>

    ![业务文档管理工作区页](./media/BDM-Overview-AddRevision.png)

    <span data-ttu-id="a503f-365">您创建了永久模板存储中已存储的模板的新修订。</span><span class="sxs-lookup"><span data-stu-id="a503f-365">You created a new revision of your template that has been stored in the permanent template’s storage.</span></span> <span data-ttu-id="a503f-366">现在可以继续编辑当前选择为活动的第二个修订的模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-366">Now you can continue editing the template of the second revision that is currently selected as active.</span></span>

5. <span data-ttu-id="a503f-367">选择第一个修订，然后选择**设置有效**。</span><span class="sxs-lookup"><span data-stu-id="a503f-367">Select the first revision and then select **Set active**.</span></span> <span data-ttu-id="a503f-368">任何时候如果要返回为模板的另一个修订，可选择此修订为有效。</span><span class="sxs-lookup"><span data-stu-id="a503f-368">You can select another revision as active if at any time you want to return to that revision of the template.</span></span>
6. <span data-ttu-id="a503f-369">选择第二个修订，然后选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="a503f-369">Select the second revision, and then select **Delete**.</span></span>
7. <span data-ttu-id="a503f-370">选择**确定**以确认您要删除所选修订。</span><span class="sxs-lookup"><span data-stu-id="a503f-370">Select **OK** to confirm that you want to delete the selected revision.</span></span> <span data-ttu-id="a503f-371">可删除任何不再需要的非有效修订。</span><span class="sxs-lookup"><span data-stu-id="a503f-371">You can delete any of the non-active revisions when they are no longer needed.</span></span>

### <a name="delete-a-modified-template"></a><span data-ttu-id="a503f-372">删除修改后的模板</span><span class="sxs-lookup"><span data-stu-id="a503f-372">Delete a modified template</span></span>

1. <span data-ttu-id="a503f-373">在 **BDM 模板编辑器**页中，选择**模板**选项卡。</span><span class="sxs-lookup"><span data-stu-id="a503f-373">On the **BDM template editor** page, select the **Template** tab.</span></span>
2. <span data-ttu-id="a503f-374">选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="a503f-374">Select **Delete**.</span></span>
3. <span data-ttu-id="a503f-375">如果选择**确定**以确认删除，将删除采用修改后模板的 **Customer FTI report (GER) Copy** ER 格式。</span><span class="sxs-lookup"><span data-stu-id="a503f-375">If you select **OK** to confirm deletion, the **Customer FTI report (GER) Copy** ER format with the modified template will be deleted.</span></span> <span data-ttu-id="a503f-376">选择**取消**以浏览其他选项。</span><span class="sxs-lookup"><span data-stu-id="a503f-376">Select **Cancel** to explore other options.</span></span>

### <a name="revoke-changes-of-template"></a><span data-ttu-id="a503f-377">撤消对模板的更改</span><span class="sxs-lookup"><span data-stu-id="a503f-377">Revoke changes of template</span></span>

<span data-ttu-id="a503f-378">编辑当前有效提供程序负责的 ER 格式中的模板时，将为您提供用于撤消对模板的更改的选项。</span><span class="sxs-lookup"><span data-stu-id="a503f-378">When you edit the template from an ER format that is owned by the current active provider, you will be offered the option to revoke changes introduced for the template.</span></span>

![业务文档管理工作区页](./media/BDM-Overview-RevokeChanges.png)

1. <span data-ttu-id="a503f-380">在 **BDM 模板编辑器**页中，选择**模板**选项卡。</span><span class="sxs-lookup"><span data-stu-id="a503f-380">On the **BDM template editor** page, select the **Template** tab.</span></span>
2. <span data-ttu-id="a503f-381">选择**撤消**。</span><span class="sxs-lookup"><span data-stu-id="a503f-381">Select **Undo**.</span></span>
3. <span data-ttu-id="a503f-382">如果选择**确定**以撤消对模板的更改，将把修改后的模板替换为原始模板，并删除所有更改。</span><span class="sxs-lookup"><span data-stu-id="a503f-382">If you select **OK** to revoke the changes introduced for the template, the modified template will be replaced by the original template and all changes will be removed.</span></span> <span data-ttu-id="a503f-383">撤消对模板的更改之后，可以删除模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-383">When you revoke changes to the template, you will be able to delete the template.</span></span> <span data-ttu-id="a503f-384">选择**取消**以浏览其他选项。</span><span class="sxs-lookup"><span data-stu-id="a503f-384">Select **Cancel** to explore other options.</span></span>

### <a name="publish-a-modified-template"></a><span data-ttu-id="a503f-385">发布修改后的模板</span><span class="sxs-lookup"><span data-stu-id="a503f-385">Publish a modified template</span></span>
1. <span data-ttu-id="a503f-386">在 **BDM 模板编辑器**页中的**模板**选项卡上，选择**发布**。</span><span class="sxs-lookup"><span data-stu-id="a503f-386">On the **BDM template editor** page, on the **Template** tab, select **Publish**.</span></span>
2. <span data-ttu-id="a503f-387">如果选择**确定**以确认发布，将把包含修改后的模板的派生 **Customer FTI report (GER) Copy** ER 格式的草稿版本标记为已完成。</span><span class="sxs-lookup"><span data-stu-id="a503f-387">If you select **OK** to confirm publishing, the draft version of the derived **Customer FTI report (GER) Copy** ER format that contains the modified template will be marked as completed.</span></span> <span data-ttu-id="a503f-388">其他用户将可使用修改后的模板。</span><span class="sxs-lookup"><span data-stu-id="a503f-388">The modified template becomes available for other users.</span></span> <span data-ttu-id="a503f-389">此 ER 格式的完成版本将仅保留模板的最后一个有效版本。</span><span class="sxs-lookup"><span data-stu-id="a503f-389">The completed versions of this ER format will keep only the last active revision of your template.</span></span> <span data-ttu-id="a503f-390">将删除其他修订。</span><span class="sxs-lookup"><span data-stu-id="a503f-390">Other revisions will be deleted.</span></span> <span data-ttu-id="a503f-391">选择**取消**以浏览其他选项。</span><span class="sxs-lookup"><span data-stu-id="a503f-391">Select **Cancel** to explore other options.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="a503f-392">常见问题</span><span class="sxs-lookup"><span data-stu-id="a503f-392">Frequently asked questions</span></span>

#### <a name="i-selected-edit-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-office-365-web-page"></a><span data-ttu-id="a503f-393">我选择了**编辑文档**，但是结果不是在 Finance and Operations 中打开 **BDM 模板编辑器**页，而是转到了 Office 365 网页。</span><span class="sxs-lookup"><span data-stu-id="a503f-393">I selected **Edit document**, but instead of opening the **BDM template editor** page in Finance and Operations, I have been sent to the Office 365 web page.</span></span>
<span data-ttu-id="a503f-394">这是 Office 365 重定向的已知问题。</span><span class="sxs-lookup"><span data-stu-id="a503f-394">This is a known issue with the Office 365 redirection.</span></span> <span data-ttu-id="a503f-395">首次登录 Office 365 时会出现此情况。</span><span class="sxs-lookup"><span data-stu-id="a503f-395">This happens when you sign to Office 365 the first time.</span></span> <span data-ttu-id="a503f-396">若要解决此问题，请选择浏览器的**后退**按钮返回。</span><span class="sxs-lookup"><span data-stu-id="a503f-396">To work around this issue, select the **Back** button of your browser to navigate back.</span></span>

#### <a name="i-understand-how-to-edit-a-template-by-using-office-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-adjusting-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-do-this-using-the-office-desktop-application"></a><span data-ttu-id="a503f-397">我知道如何在第一个应用程序会话中通过使用 Office 365 编辑模板，以及如何在第二个应用程序会话中使用模板，并调整模板来查看我的更改对生成的业务文档有何影响。</span><span class="sxs-lookup"><span data-stu-id="a503f-397">I understand how to edit a template by using Office 365 in the first application session and how to use the template in the second application session adjusting the template to see how my changes affect the generated business document.</span></span> <span data-ttu-id="a503f-398">我可以使用 Office 桌面应用程序执行此操作吗？</span><span class="sxs-lookup"><span data-stu-id="a503f-398">Can I do this using the Office desktop application?</span></span>
<span data-ttu-id="a503f-399">是的，可以。</span><span class="sxs-lookup"><span data-stu-id="a503f-399">Yes, you can.</span></span> <span data-ttu-id="a503f-400">在第一个应用程序会话中，选择**在桌面应用程序中打开**。</span><span class="sxs-lookup"><span data-stu-id="a503f-400">In the first application session, select **Open in Desktop App**.</span></span> <span data-ttu-id="a503f-401">将把您的模板存储到临时文件存储中，并在 Office 桌面应用程序中打开。</span><span class="sxs-lookup"><span data-stu-id="a503f-401">Your template will be stored in the temporary file storage and opened in the Office desktop application.</span></span> <span data-ttu-id="a503f-402">接下来，完成以下步骤在生成的业务文档中预览模板更改：</span><span class="sxs-lookup"><span data-stu-id="a503f-402">Next, complete the following steps to preview your template changes in the generated business document:</span></span>

1. <span data-ttu-id="a503f-403">通过使用 Office 桌面应用程序在模板中进行更改。</span><span class="sxs-lookup"><span data-stu-id="a503f-403">Make changes in the template by using the Office desktop application.</span></span>
2. <span data-ttu-id="a503f-404">在 Office 桌面应用程序中选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="a503f-404">Select **Save** in the Office desktop application.</span></span>
3. <span data-ttu-id="a503f-405">在第一个应用程序会话的 **BDM 模板编辑器**页中，选择**同步已存储副本**。</span><span class="sxs-lookup"><span data-stu-id="a503f-405">On the **BDM template editor** page of the first application session, select **Sync stored copy**.</span></span>
4. <span data-ttu-id="a503f-406">在第二个应用程序会话中执行此模板 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="a503f-406">Execute this template ER format in the second application session.</span></span>

#### <a name="i-get-the-error-value-cannot-be-null-parameter-name-externalid-when-i-select-open-in-desktop-app-how-do-i-work-around-this"></a><span data-ttu-id="a503f-407">我在执行以下操作时，发生了“值不能为空。</span><span class="sxs-lookup"><span data-stu-id="a503f-407">I get the error ‘Value cannot be null.</span></span> <span data-ttu-id="a503f-408">参数名称：externalId”错误：选择**在桌面应用程序中打开**。</span><span class="sxs-lookup"><span data-stu-id="a503f-408">Parameter name: externalId’ when I select **Open in Desktop App**.</span></span> <span data-ttu-id="a503f-409">应该如何解决这个问题？</span><span class="sxs-lookup"><span data-stu-id="a503f-409">How do I work around this?</span></span> 
<span data-ttu-id="a503f-410">您当前登录的应用程序实例所在 Azure AD 域很可能不是用于部署此实例的 Azure AD 域。</span><span class="sxs-lookup"><span data-stu-id="a503f-410">Most likely you signed in to the current instance of the app of the Azure AD domain which differs from the Azure AD domain that was used to deploy this instance.</span></span> <span data-ttu-id="a503f-411">因为 SharePoint 服务（用于存储模板来使其可通过使用 Office 桌面应用程序进行编辑）属于相同域，所以我们无权访问 SharePoint 服务。</span><span class="sxs-lookup"><span data-stu-id="a503f-411">Because the SharePoint service, which is used to store templates for making them available for editing by using the Office desktop applications, belongs to the same domain, we have no permissions to access the SharePoint service.</span></span> <span data-ttu-id="a503f-412">若要解决此问题，请使用具有正确 Azure AD 域的用户的凭据登录当前实例。</span><span class="sxs-lookup"><span data-stu-id="a503f-412">To resolve this issue, sign in to the current instance using the credentials of a user with the correct Azure AD domain.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a503f-413">其他资源</span><span class="sxs-lookup"><span data-stu-id="a503f-413">Additional resources</span></span>

[<span data-ttu-id="a503f-414">电子申报 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="a503f-414">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="a503f-415">ER 设计以 OPENXML 格式生成报表的配置（2016 年 11 月）</span><span class="sxs-lookup"><span data-stu-id="a503f-415">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>](tasks/er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="a503f-416">设计 ER 配置以生成 Word 格式的报表</span><span class="sxs-lookup"><span data-stu-id="a503f-416">Design ER configurations to generate reports in Word format</span></span>](tasks/er-design-configuration-word-2016-11.md)

[<span data-ttu-id="a503f-417">使用 ER 在您生成的文档中嵌入图像和形状</span><span class="sxs-lookup"><span data-stu-id="a503f-417">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="a503f-418">配置电子申报 (ER) 以便将数据导入 Power BI</span><span class="sxs-lookup"><span data-stu-id="a503f-418">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)

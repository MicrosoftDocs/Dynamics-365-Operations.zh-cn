---
title: 生成可打印的 FTI 表单
description: 本主题说明如何使用电子申报 (ER) 框架生成 Microsoft Office 文档格式的可打印普通发票 (FTI) 表单。
author: NickSelin
manager: AnnBe
ms.date: 07/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: da671d7b9302f99fc71860cf41846290d74d11e1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570678"
---
# <a name="generate-printable-fti-forms"></a><span data-ttu-id="31bfa-103">生成可打印的 FTI 窗体</span><span class="sxs-lookup"><span data-stu-id="31bfa-103">Generate printable FTI forms</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="31bfa-104">可使用电子申报 (ER) 框架生成 Microsoft Office 文档格式的可打印普通发票 (FTI) 表单。</span><span class="sxs-lookup"><span data-stu-id="31bfa-104">The Electronic reporting (ER) framework lets you generate printable free text invoice (FTI) forms as Microsoft Office documents.</span></span> <span data-ttu-id="31bfa-105">此主题提供有关如何构建自己的配置的信息和有关可用配置模板的详细信息。</span><span class="sxs-lookup"><span data-stu-id="31bfa-105">This topic provides information about how to build your own configurations as well as details of available configuration templates.</span></span>

## <a name="overview"></a><span data-ttu-id="31bfa-106">概览</span><span class="sxs-lookup"><span data-stu-id="31bfa-106">Overview</span></span>

<span data-ttu-id="31bfa-107">除了通过使用 Microsoft SQL Server Reporting Services (SSRS) 生成可打印 FTI 表单这一项现有功能，现在还可以使用 ER 框架。</span><span class="sxs-lookup"><span data-stu-id="31bfa-107">In addition to the existing capability of generating printable FTI forms by using Microsoft SQL Server Reporting Services (SSRS), you can now use the ER framework.</span></span> <span data-ttu-id="31bfa-108">可在 Microsoft Office Excel 和 Word 中管理可打印 FTI 表单。</span><span class="sxs-lookup"><span data-stu-id="31bfa-108">You can manage printable FTI forms in Microsoft Office Excel and Word.</span></span> <span data-ttu-id="31bfa-109">还可以修改布局、数据流和格式设置以满足特定要求，同时无需更改代码。</span><span class="sxs-lookup"><span data-stu-id="31bfa-109">You can also modify the layout, data flow, and formatting to meet specific requirements without making code changes.</span></span>

> [!NOTE]
> <span data-ttu-id="31bfa-110">如果要从现有 ER 配置的概述开始了解这个可打印 FTI 表单解决方案示例，可直接转至本主题后文的 **下载示例 ER 配置以生成可打印 FTI 表单** 部分。</span><span class="sxs-lookup"><span data-stu-id="31bfa-110">If you want to start with an overview of existing ER configurations for this sample of the printable FTI forms solution, you can go directly to section **Download sample ER configurations to generate printable FTI forms** later in this topic.</span></span>

## <a name="create-customized-configurations-for-fti-printable-forms"></a><span data-ttu-id="31bfa-111">为 FTI 可打印表单创建自定义配置</span><span class="sxs-lookup"><span data-stu-id="31bfa-111">Create customized configurations for FTI printable forms</span></span>
<span data-ttu-id="31bfa-112">在可打印 FTI 表单的自定义解决方案中，必须创建一组 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="31bfa-112">As part of your customized solution for printable FTI forms, you must create a set of ER configurations.</span></span>

### <a name="configure-the-er-data-model"></a><span data-ttu-id="31bfa-113">配置 ER 数据模型</span><span class="sxs-lookup"><span data-stu-id="31bfa-113">Configure the ER data model</span></span>
<span data-ttu-id="31bfa-114">您的应用程序中必须包含 ER 数据模型配置，其中包含一个数据模型，用于描述客户开票业务域。</span><span class="sxs-lookup"><span data-stu-id="31bfa-114">Your application must include the ER data model configuration that contains a data model that describes the customer invoicing business domain.</span></span> <span data-ttu-id="31bfa-115">按照要求，此数据模型的名称必须为 **CustomersInvoicing**。</span><span class="sxs-lookup"><span data-stu-id="31bfa-115">As a requirement, the name of the data model must be **CustomersInvoicing**.</span></span> <span data-ttu-id="31bfa-116">有关如何设计 ER 数据模型的信息，请参阅 [ER 设计域特定数据模型](tasks/er-design-domain-specific-data-model-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="31bfa-116">For information about how to design ER data models, see [ER Design domain specific data model](tasks/er-design-domain-specific-data-model-2016-11.md).</span></span>

### <a name="configure-the-er-model-mapping"></a><span data-ttu-id="31bfa-117">配置 ER 模型映射</span><span class="sxs-lookup"><span data-stu-id="31bfa-117">Configure the ER model mapping</span></span>
<span data-ttu-id="31bfa-118">您的应用程序中必须包含 CustomersInvoicing 数据模型的 ER 模型映射。</span><span class="sxs-lookup"><span data-stu-id="31bfa-118">Your application must include the ER model mapping for the CustomersInvoicing data model.</span></span> <span data-ttu-id="31bfa-119">此模型映射可以为 ER 数据模型配置或 ER 模型映射配置。</span><span class="sxs-lookup"><span data-stu-id="31bfa-119">The model mapping can be in either the ER data model configuration or the ER model mapping configuration.</span></span> <span data-ttu-id="31bfa-120">但是，该模型映射的根描述符的名称必须为 **FreeTextInvoice**。</span><span class="sxs-lookup"><span data-stu-id="31bfa-120">However, the name of the root descriptor of the model mapping must be **FreeTextInvoice**.</span></span>

<span data-ttu-id="31bfa-121">该映射中必须包含以下数据源：</span><span class="sxs-lookup"><span data-stu-id="31bfa-121">The mapping must contain the following data sources:</span></span>

- <span data-ttu-id="31bfa-122">数据源类型：**表记录**</span><span class="sxs-lookup"><span data-stu-id="31bfa-122">Data source type: **Table records**</span></span>

    - <span data-ttu-id="31bfa-123">该数据源的名称必须为 **CustInvoiceJour**。</span><span class="sxs-lookup"><span data-stu-id="31bfa-123">This data source must be named **CustInvoiceJour**.</span></span>
    - <span data-ttu-id="31bfa-124">它必须引用 CustInvoiceJour 应用程序表。</span><span class="sxs-lookup"><span data-stu-id="31bfa-124">It must refer to the CustInvoiceJour application table.</span></span>
    - <span data-ttu-id="31bfa-125">它用于在运行时将已选择打印的发票的列表从应用程序传递到 ER 模型映射。</span><span class="sxs-lookup"><span data-stu-id="31bfa-125">It's used at runtime to pass from the application to the ER model mapping the list of invoices that have been selected for printing.</span></span>

- <span data-ttu-id="31bfa-126">数据源类型：**对象**</span><span class="sxs-lookup"><span data-stu-id="31bfa-126">Data source type: **Object**</span></span>

    - <span data-ttu-id="31bfa-127">该数据源的名称必须为 **PrintMgmtPrintSettingDetail**。</span><span class="sxs-lookup"><span data-stu-id="31bfa-127">This data source must be named **PrintMgmtPrintSettingDetail**.</span></span>
    - <span data-ttu-id="31bfa-128">它必须引用 **PrintMgmtPrintSettingDetail** 应用程序表。</span><span class="sxs-lookup"><span data-stu-id="31bfa-128">It must refer to the **PrintMgmtPrintSettingDetail** application class.</span></span>
    - <span data-ttu-id="31bfa-129">它用于在运行时将运行的 ER 格式的打印管理设置的详细信息从应用程序传递到 ER 模型映射。</span><span class="sxs-lookup"><span data-stu-id="31bfa-129">It's used at runtime to pass from the application to the ER model mapping details of the print management settings for the ER format that is running.</span></span>

<span data-ttu-id="31bfa-130">应用程序源代码的 **ERPrintMgmtReportFormatSubscriber** 类（ER 应用程序套件集成模型）中包含有关应用程序与 ER 框架之间的集成的详细信息。</span><span class="sxs-lookup"><span data-stu-id="31bfa-130">The details of the application integration with the ER framework can be found in the **ERPrintMgmtReportFormatSubscriber** class (ER Application Suite integration model) in the source code of the application.</span></span>

<span data-ttu-id="31bfa-131">有关设计 ER 模型映射的详细信息，请参阅[定义 ER 模型映射并从中选择数据源](tasks/er-define-model-mapping-select-data-sources-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="31bfa-131">For more information about the design of ER model mappings, see [Define ER model mappings and select data sources for them](tasks/er-define-model-mapping-select-data-sources-2016-11.md).</span></span>

### <a name="configure-the-er-format"></a><span data-ttu-id="31bfa-132">配置 ER 格式</span><span class="sxs-lookup"><span data-stu-id="31bfa-132">Configure the ER format</span></span>
<span data-ttu-id="31bfa-133">在您的应用程序实例中，必须设置要用于生成 FTI 表单的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="31bfa-133">In your application instance, you must have the ER format configuration that will be used to generate FTI forms.</span></span> 

> [!NOTE]
> <span data-ttu-id="31bfa-134">必须为 CustomersInvoicing 数据模型创建此格式配置，并且此格式配置必须使用具有 **FreeTextInvoice** 根描述符的模型映射。</span><span class="sxs-lookup"><span data-stu-id="31bfa-134">This format configuration must be created for the CustomersInvoicing data model, and it must use the model mapping that has the **FreeTextInvoice** root descriptor.</span></span>

<span data-ttu-id="31bfa-135">有关如何配置 ER 格式的信息，请参阅 [ER 创建格式配置（2016 年 11 月）](tasks/er-format-configuration-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="31bfa-135">For information about how to configure ER formats, see [ER Create a format configuration (November 2016)](tasks/er-format-configuration-2016-11.md).</span></span> <span data-ttu-id="31bfa-136">有关如何设计 ER 格式以生成 OpenXML 格式的报表的信息，请参阅 [ER 设计以 OPENXML 格式生成报表的配置（2016 年 11 月）](tasks/er-design-reports-openxml-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="31bfa-136">For information about how to design ER formats to generate reports in OpenXML format, see [ER Design a configuration for generating reports in OPENXML format (November 2016)](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="configure-print-management"></a><span data-ttu-id="31bfa-137">配置打印管理</span><span class="sxs-lookup"><span data-stu-id="31bfa-137">Configure print management</span></span>
<span data-ttu-id="31bfa-138">若要通过使用 ER 框架生成 FTI 表单，可以按照分配 SSRS 报表的相同方法分配 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="31bfa-138">To generate FTI forms by using the ER framework, you can assign ER formats in the same way that you assign SSRS reports.</span></span> <span data-ttu-id="31bfa-139">若要将 ER 格式与所有应收帐款 FTI 关联，请转至 **应收帐款** \> **设置** \> **表单** \> **表单设置** \> **常规** \> **打印管理** \> **普通发票** \> **原件**。</span><span class="sxs-lookup"><span data-stu-id="31bfa-139">To associate the ER format with all Accounts receivable FTIs, go to **Accounts receivable** \> **Setup** \> **Forms** \> **Form setup** \> **General** \> **Print management** \> **Free text invoice** \> **Original**.</span></span> <span data-ttu-id="31bfa-140">若要将 ER 格式与特定客户或发票关联，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="31bfa-140">To associate the ER format with a specific customer or invoice, follow these steps.</span></span>

1. <span data-ttu-id="31bfa-141">转至 **应收帐款** \> **发票** \> **所有普通发票**。</span><span class="sxs-lookup"><span data-stu-id="31bfa-141">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="31bfa-142">选择 ER 格式要关联的 FTI，然后打开 **打印管理设置** 页面。</span><span class="sxs-lookup"><span data-stu-id="31bfa-142">Select the FTI to associate the ER format with, and open the **Print management setup** page.</span></span>
3. <span data-ttu-id="31bfa-143">选择文档级别以指定要处理的发票范围。</span><span class="sxs-lookup"><span data-stu-id="31bfa-143">Select the document level to specify the scope of invoices for processing.</span></span>
4. <span data-ttu-id="31bfa-144">为指定的文档级别选择 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="31bfa-144">Select the ER format for the specified document level.</span></span>

![打印管理设置](media/FTIbyGER-PMSetting.png)

> [!NOTE]
> <span data-ttu-id="31bfa-146">所选格式的 **报表格式查找** 字段中仅显示 **CustomersInvoicing** 数据模型的 **FreeTextInvoice** 根描述符。</span><span class="sxs-lookup"><span data-stu-id="31bfa-146">Only ER formats that use the **FreeTextInvoice** root descriptor of the **CustomersInvoicing** data model appear in the **Report format lookup** field for the selected format.</span></span>

## <a name="generate-fti-forms"></a><span data-ttu-id="31bfa-147">生成 FTI 表单</span><span class="sxs-lookup"><span data-stu-id="31bfa-147">Generate FTI forms</span></span>
<span data-ttu-id="31bfa-148">FTI 表单在 ER 框架中按照生成 SSRS 报表的相同方法生成。</span><span class="sxs-lookup"><span data-stu-id="31bfa-148">FTI forms are generated in the ER framework in the same way that SSRS reports are generated.</span></span>

<span data-ttu-id="31bfa-149">若要生成 FTI 表单，可以根据范围或根据选择来选择发票。</span><span class="sxs-lookup"><span data-stu-id="31bfa-149">To generate FTI forms, you can select invoices either by range or by selection.</span></span> 

![发票选择](media/FTIbyGER-InvoiceSelection.png)

![发票预览](media/FTIbyGER-InvoiceExcelPreview.png)

<span data-ttu-id="31bfa-152">按照这种方式使用 ER 格式打印 FTI 表单时，将使用默认 ER 文件目标。</span><span class="sxs-lookup"><span data-stu-id="31bfa-152">When you use ER formats to print FTI forms in this way, the default ER file destinations are used.</span></span> <span data-ttu-id="31bfa-153">不能更改该目标。</span><span class="sxs-lookup"><span data-stu-id="31bfa-153">You can't change the destination.</span></span> <span data-ttu-id="31bfa-154">有关如何为 ER 格式配置 ER 目标的详细信息，请参阅[电子申报 (ER) 目标](electronic-reporting-destinations.md)。</span><span class="sxs-lookup"><span data-stu-id="31bfa-154">For more information about how to configure the ER destinations for ER formats, see [Electronic reporting (ER) destinations](electronic-reporting-destinations.md).</span></span>

<span data-ttu-id="31bfa-155">也可以在发布 FTI 时生成 FTI 表单，方法是开启 **打印发票** 并关闭 **使用打印管理目标**。</span><span class="sxs-lookup"><span data-stu-id="31bfa-155">You can also generate FTI forms when you post an FTI, by turning **Print invoice** on and turning **Use print management destinations** off.</span></span>

> [!NOTE]
> <span data-ttu-id="31bfa-156">按照这种方式使用 ER 格式打印 FTI 表单时，将使用默认 ER 文件目标。</span><span class="sxs-lookup"><span data-stu-id="31bfa-156">When you use ER formats to print FTI forms in this way, the default ER file destinations are used.</span></span> <span data-ttu-id="31bfa-157">如果已经配置了默认目标，则可在运行时更改该目标。</span><span class="sxs-lookup"><span data-stu-id="31bfa-157">You can change the default destination at runtime if the destination has already been configured.</span></span> <span data-ttu-id="31bfa-158">若要更改目标，必须具有以下安全权限：</span><span class="sxs-lookup"><span data-stu-id="31bfa-158">To change the destination, you must have the following security privilege:</span></span>
>
> - <span data-ttu-id="31bfa-159">**名称：** ERFormatDestinationRuntimeMaintain</span><span class="sxs-lookup"><span data-stu-id="31bfa-159">**Name:** ERFormatDestinationRuntimeMaintain</span></span>
> - <span data-ttu-id="31bfa-160">**标签：** 在运行时维护电子报告格式目标</span><span class="sxs-lookup"><span data-stu-id="31bfa-160">**Label:** Maintain electronic reporting format destination during runtime</span></span>

![电子报告目标](media/FTIbyGER-ERFileDestinationSetting.png)

![电子申报格式目标](media/FTIbyGER-ERFileDestinationUsage.png)

<span data-ttu-id="31bfa-163">ER 框架当前支持生成的文档采用以下目标：</span><span class="sxs-lookup"><span data-stu-id="31bfa-163">The ER framework currently supports the following destinations for generated documents:</span></span>

- <span data-ttu-id="31bfa-164">**下载的文件** – 生成的表单以可通过使用浏览器保存的下载的形式提供。</span><span class="sxs-lookup"><span data-stu-id="31bfa-164">**Downloaded file** – Generated forms are offered as downloads that you can save by using the browser.</span></span>
- <span data-ttu-id="31bfa-165">**屏幕** – Microsoft 365 Excel 用于预览生成的 Excel 格式的 FTI 表单。</span><span class="sxs-lookup"><span data-stu-id="31bfa-165">**Screen** – Microsoft 365 Excel is used to preview generated FTI forms in Excel format.</span></span>
- <span data-ttu-id="31bfa-166">**SharePoint 文件夹** – 生成的表单基于文档管理框架的设置存储。</span><span class="sxs-lookup"><span data-stu-id="31bfa-166">**SharePoint folder** – Generated forms are stored based on the settings of the Document management framework.</span></span>
- <span data-ttu-id="31bfa-167">**应用程序存档** – 生成的表单作为执行日志记录的附件存储在 Microsoft Azure 存储中。</span><span class="sxs-lookup"><span data-stu-id="31bfa-167">**Application archive** – Generated forms are stored as attachments of execution log records in the Microsoft Azure Storage.</span></span>
- <span data-ttu-id="31bfa-168">**电子邮件** – 生成的表单作为电子邮件附件发送。</span><span class="sxs-lookup"><span data-stu-id="31bfa-168">**Email** – Generated forms are sent as email attachments.</span></span>

> [!NOTE]
> <span data-ttu-id="31bfa-169">不能将生成的 FTI 表单直接发送到打印机，因为现在不支持直接打印使用动态打印机路由代理。</span><span class="sxs-lookup"><span data-stu-id="31bfa-169">You can't send the FTI forms that are generated directly to the printer, because direct printing that uses the Dynamics Printer Routing Agent isn't currently supported.</span></span>

## <a name="download-sample-er-configurations-to-generate-printable-fti-forms"></a><span data-ttu-id="31bfa-170">下载示例 ER 配置以生成可打印 FTI 表单</span><span class="sxs-lookup"><span data-stu-id="31bfa-170">Download sample ER configurations to generate printable FTI forms</span></span>
<span data-ttu-id="31bfa-171">可下载示例 ER 配置以用作 FTI 解决方案的模板。</span><span class="sxs-lookup"><span data-stu-id="31bfa-171">You can download sample ER configurations to use as a template for your FTI solution.</span></span> <span data-ttu-id="31bfa-172">配置存储在 Microsoft Dynamics Lifecycle Services (LCS) 中的共用资产库内。</span><span class="sxs-lookup"><span data-stu-id="31bfa-172">The configurations are stored in the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="31bfa-173">配置包含：</span><span class="sxs-lookup"><span data-stu-id="31bfa-173">The configurations include:</span></span>

- <span data-ttu-id="31bfa-174">**客户开票模型** 配置中包含所需数据模型和模型映射。</span><span class="sxs-lookup"><span data-stu-id="31bfa-174">The **Customer invoicing model** configuration contains the required data model and model mapping.</span></span>
- <span data-ttu-id="31bfa-175">**客户 FTI 报表 (GER)** 配置中包含示例格式。</span><span class="sxs-lookup"><span data-stu-id="31bfa-175">The **Customer FTI report (GER)** configuration contains the sample format.</span></span>

> [!NOTE]
> <span data-ttu-id="31bfa-176">已将这些配置创建为示例来帮助阐明可能的方案。</span><span class="sxs-lookup"><span data-stu-id="31bfa-176">These configurations have been created as samples to help clarify possible scenarios.</span></span> <span data-ttu-id="31bfa-177">这些配置的未来取决于此项评估的结果和收到的反馈。</span><span class="sxs-lookup"><span data-stu-id="31bfa-177">The future of these configurations depends on the results of this evaluation and any feedback that is received.</span></span>

### <a name="features-that-are-implemented-in-the-sample-er-format"></a><span data-ttu-id="31bfa-178">以示例 ER 格式实施的功能</span><span class="sxs-lookup"><span data-stu-id="31bfa-178">Features that are implemented in the sample ER format</span></span>
<span data-ttu-id="31bfa-179">在示例 ER 格式配置中，Excel 文件用作模板来生成 FTI 表单。</span><span class="sxs-lookup"><span data-stu-id="31bfa-179">In the sample ER format configuration, an Excel file is used as a template to generate FTI forms.</span></span>

![格式设计器](media/FTIbyGER-ERFormat.png)

<span data-ttu-id="31bfa-181">现在，此示例 ER 格式支持以下功能以生成 FTI 表单：</span><span class="sxs-lookup"><span data-stu-id="31bfa-181">Currently, this sample ER format supports the following features to generate FTI forms:</span></span>

- <span data-ttu-id="31bfa-182">FTI 表单同时针对已过帐的原始发票和尚未过帐的原始发票生成。</span><span class="sxs-lookup"><span data-stu-id="31bfa-182">FTI forms are generated for both original invoices that have been posted and original invoices that haven't yet been posted.</span></span> <span data-ttu-id="31bfa-183">不支持经过更正的发票和贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="31bfa-183">Corrected invoices and credit notes aren't supported.</span></span>
- <span data-ttu-id="31bfa-184">FTI 表单以发票语言生成。</span><span class="sxs-lookup"><span data-stu-id="31bfa-184">FTI forms are generated in the invoice language.</span></span> <span data-ttu-id="31bfa-185">生成的表单中的值和日期的格式基于用户的客户端区域设置。</span><span class="sxs-lookup"><span data-stu-id="31bfa-185">The format of values and dates in the generated forms is based on the settings of the user's client locale.</span></span>
- <span data-ttu-id="31bfa-186">如果处理的发票中没有行，则生成的发票显示数据不可用通知。</span><span class="sxs-lookup"><span data-stu-id="31bfa-186">Generated invoices show data unavailability notifications if there are no lines in the invoices that are processed.</span></span>
- <span data-ttu-id="31bfa-187">生成的发票头基于 **应收帐款参数** 页面上为 FTI 表单选择的纸张格式。</span><span class="sxs-lookup"><span data-stu-id="31bfa-187">Generated invoice headers are based on the paper format that has been selected for the FTI form on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="31bfa-188">仅当纸张格式为空白时，生成的发票表单的标题中才显示公司详细信息。</span><span class="sxs-lookup"><span data-stu-id="31bfa-188">Company details appear in the header of the generated invoice form only if the paper format is blank.</span></span>
- <span data-ttu-id="31bfa-189">在 **应收帐款参数** 页中为 FTI 表单选择了相应选项之后，生成的发票表单显示公司和客户免税编号。</span><span class="sxs-lookup"><span data-stu-id="31bfa-189">Generated invoice forms show company and customer tax exempt numbers when the appropriate option has been selected for the FTI form on the **Accounts receivable parameters** page.</span></span>
- <span data-ttu-id="31bfa-190">生成的发票行和发票总计部分以发票登记币种显示默认发票的货币详细信息。</span><span class="sxs-lookup"><span data-stu-id="31bfa-190">The generated invoice lines and invoice totals sections show the default invoice's monetary details in the invoice registration currency.</span></span>
- <span data-ttu-id="31bfa-191">如果在 **应收帐款参数** 页面中启用了 **打印用欧元币种表示的金额** 选项，生成的发票总计部分可以以欧元币种和发票登记币种显示货币详细信息。</span><span class="sxs-lookup"><span data-stu-id="31bfa-191">The generated invoice totals section can show monetary details in the euro currency and the invoice registration currency when the **Print amount in currency representing the euro** option is enabled on the **Accounts receivable parameters** page.</span></span>
- <span data-ttu-id="31bfa-192">生成的发票表单基于 **应收帐款参数** 页面中的设置显示任何可用处理发票通知注释。</span><span class="sxs-lookup"><span data-stu-id="31bfa-192">Generated invoice forms show any process invoice notes that are available, based on settings on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="31bfa-193">整个发票和每个发票行都包含注释。</span><span class="sxs-lookup"><span data-stu-id="31bfa-193">Notes are included for both the whole invoice and each invoice line.</span></span>
- <span data-ttu-id="31bfa-194">如果已在 AR 表单注释列表中配置了客户 FTI 表单和处理发票语言，则生成的发票表单中将包含这两项的注释。</span><span class="sxs-lookup"><span data-stu-id="31bfa-194">Generated invoice forms include notes for the customer FTI form and the processing invoice language when they have been configured in the AR form notes list.</span></span>
- <span data-ttu-id="31bfa-195">如果针对发票语言、ER 格式和 FTI 文档范围配置了自定义页脚文本，则生成的发票表单中将包含这些文本，具体取决于打印管理设置。</span><span class="sxs-lookup"><span data-stu-id="31bfa-195">Depending on the Print management settings, generated invoices include custom footer text when it has been configured for the invoice language, the ER format, and the FTI document scope.</span></span>
- <span data-ttu-id="31bfa-196">生成的发票表单的总计部分中包含所有可用现金折扣信息。</span><span class="sxs-lookup"><span data-stu-id="31bfa-196">The totals section of generated invoice forms includes any cash discount information that is available.</span></span>
- <span data-ttu-id="31bfa-197">生成的发票表单的付款计划部分中包含所有可用付款计划详细信息。</span><span class="sxs-lookup"><span data-stu-id="31bfa-197">The payment schedule section of generated invoice forms includes any payment schedule details that are available.</span></span>
- <span data-ttu-id="31bfa-198">生成的发票表单的加价部分中包含所有可用费用交易记录。</span><span class="sxs-lookup"><span data-stu-id="31bfa-198">The markup section of generated invoice forms includes any charges transactions that are available.</span></span>
- <span data-ttu-id="31bfa-199">生成的发票表单中包含基于 **应收帐款参数** 页面上的 **销售税说明** 设置的销售税详细信息。</span><span class="sxs-lookup"><span data-stu-id="31bfa-199">Generated invoice forms include sales tax details, based on the **Sales tax specification** setting on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="31bfa-200">此部分只能以发票登记币种或同时以发票登记币种和公司记帐币种显示税务详细信息。</span><span class="sxs-lookup"><span data-stu-id="31bfa-200">This section can show tax details either in the invoice registration currency only, or in the invoice registration currency and the company accounting currency at the same time.</span></span>
- <span data-ttu-id="31bfa-201">生成的发票表单显示直接借记通知详细信息。</span><span class="sxs-lookup"><span data-stu-id="31bfa-201">Generated invoice forms show direct debit notification details.</span></span> <span data-ttu-id="31bfa-202">例如，显示具有直接借记授权单 ID 的付款方式是何时为发票选择的，处理发票何时以欧元币种登记的，以及直接借记授权单 ID 是何时为发票定义的。</span><span class="sxs-lookup"><span data-stu-id="31bfa-202">For example, they show when the method of payment that has the mandatory direct debit mandate ID was selected for the invoice, when the processing invoice was registered in the euro currency, and when the direct debit mandate ID was defined for the invoice.</span></span>
- <span data-ttu-id="31bfa-203">生成的发票显示已过帐发票的所有可用预付款详细信息。</span><span class="sxs-lookup"><span data-stu-id="31bfa-203">Generated invoices show any prepayment details that are available for posted invoices.</span></span>
- <span data-ttu-id="31bfa-204">可将生成的发票表单作为电子邮件附件发送给发票客户。</span><span class="sxs-lookup"><span data-stu-id="31bfa-204">Generated invoice forms can be sent to an invoice customer as an email attachment.</span></span> <span data-ttu-id="31bfa-205">应该为所用 ER 格式配置相应 ER 文件目标。</span><span class="sxs-lookup"><span data-stu-id="31bfa-205">The appropriate ER file destination should be configured for the ER format that is being used.</span></span>

### <a name="countryregion-specific-features"></a><span data-ttu-id="31bfa-206">国家/地区特定的功能</span><span class="sxs-lookup"><span data-stu-id="31bfa-206">Country/region-specific features</span></span> 
<span data-ttu-id="31bfa-207">示例 ER 格式中包含以下国家/地区特定的功能，用于显示可以在 ER 配置中如何处理特定要求。</span><span class="sxs-lookup"><span data-stu-id="31bfa-207">The following country/region-specific features are included in the sample ER format to show how specific requirements can be handled in ER configurations.</span></span>

#### <a name="norway"></a><span data-ttu-id="31bfa-208">挪威</span><span class="sxs-lookup"><span data-stu-id="31bfa-208">Norway</span></span>
<span data-ttu-id="31bfa-209">为以下面的方式配置的法人处理发票时，将在生成的发票表单的标题中放入企业登记条款：</span><span class="sxs-lookup"><span data-stu-id="31bfa-209">The Enterprise register term is put on the header of the generated invoice form when the invoice is processed for a legal entity that is configured in the following manner:</span></span>

- <span data-ttu-id="31bfa-210">将使用挪威的国家/地区上下文。</span><span class="sxs-lookup"><span data-stu-id="31bfa-210">The country/region context for Norway is used.</span></span>
- <span data-ttu-id="31bfa-211">**打印 Foretaksregisteret** 参数在销售单据上处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="31bfa-211">The **Print Foretaksregisteret** parameter is active on sales documents.</span></span>

#### <a name="spain"></a><span data-ttu-id="31bfa-212">西班牙</span><span class="sxs-lookup"><span data-stu-id="31bfa-212">Spain</span></span>
<span data-ttu-id="31bfa-213">为以下面的方式配置的法人处理发票时，将在生成的发票表单的标题中放入 **现金会计方法的特别体制** 条款：</span><span class="sxs-lookup"><span data-stu-id="31bfa-213">The **Special regime for cash accounting method** term is put on the header of the generated invoice form when the invoice is processed for a legal entity that is configured in the following manner:</span></span>

- <span data-ttu-id="31bfa-214">将使用西班牙的国家/地区上下文。</span><span class="sxs-lookup"><span data-stu-id="31bfa-214">The country/region context for Spain is used.</span></span>
- <span data-ttu-id="31bfa-215">已在发票处理日期上启用了现金会计方法的特别体制。</span><span class="sxs-lookup"><span data-stu-id="31bfa-215">The special regime for the cash accounting method is enabled on the invoice processing date.</span></span>

<span data-ttu-id="31bfa-216">如果有现金折扣详细信息（如现金折扣金额和发票行净额）,在为以下面的方式配置的法人处理这些详细信息时，生成的发票表单的发票总计部分中将包含这些详细信息：</span><span class="sxs-lookup"><span data-stu-id="31bfa-216">When cash discount details, such as the cash discount amount and invoice line net amount, are available, they are presented in the invoice totals section of the generated invoice form when it has been processed for a legal entity that is configured in the following manner:</span></span>

- <span data-ttu-id="31bfa-217">将使用西班牙的国家/地区上下文。</span><span class="sxs-lookup"><span data-stu-id="31bfa-217">The country/region context for Spain is used.</span></span>
- <span data-ttu-id="31bfa-218">发票选项（**总帐参数** \> **销售税** 部分）中已开启了 **发票中含现金折扣**。</span><span class="sxs-lookup"><span data-stu-id="31bfa-218">**Cash discount is applied in the invoice** is turned on in the invoice option (**General ledger parameters** \> **Sales tax section**).</span></span>

#### <a name="italy"></a><span data-ttu-id="31bfa-219">意大利</span><span class="sxs-lookup"><span data-stu-id="31bfa-219">Italy</span></span>
<span data-ttu-id="31bfa-220">为使用意大利的国家/地区上下文配置的法人处理生成的发票时，该发票的发票行中将包含货物折扣标记。</span><span class="sxs-lookup"><span data-stu-id="31bfa-220">The goods discount mark is included on the invoice lines of the generated invoice when it's being processed for a legal entity that is configured using the country/region context for Italy.</span></span>

#### <a name="finland"></a><span data-ttu-id="31bfa-221">芬兰</span><span class="sxs-lookup"><span data-stu-id="31bfa-221">Finland</span></span>
<span data-ttu-id="31bfa-222">除了生成的发票表单，还可以生成银行转帐单，如下所示：</span><span class="sxs-lookup"><span data-stu-id="31bfa-222">In addition to the generated invoice form, Giro money transfer slips can be generated as follows:</span></span>

- <span data-ttu-id="31bfa-223">为使用芬兰的国家/地区上下文，并且至少有一个银行帐户标记为 **转帐帐户** 和 **银行条码** 的法人。</span><span class="sxs-lookup"><span data-stu-id="31bfa-223">For the legal entity that uses the country/region context for Finland, and that has at least one bank account that is marked as **Giro account** and **Bank bar code**.</span></span> 
- <span data-ttu-id="31bfa-224">为标记为 **芬兰的** 关联付款附件所需的发票。</span><span class="sxs-lookup"><span data-stu-id="31bfa-224">For an invoice that is marked as required for the **Finnish** associated payment attachment.</span></span>

![转帐单](media/FTIbyGER-GiroSlip.PNG)

> [!NOTE]
> <span data-ttu-id="31bfa-226">示例 ER 格式已配置为可选择在单独的工作表中生成银行转帐单。</span><span class="sxs-lookup"><span data-stu-id="31bfa-226">The sample ER format has been configured to optionally generate the Giro money transfer slips in the separate worksheet.</span></span>

> [!NOTE]
> <span data-ttu-id="31bfa-227">必须首先在将用于预览 Excel 格式的所生成发票表单的本地机器上安装用于生成条形码的字体。</span><span class="sxs-lookup"><span data-stu-id="31bfa-227">You must first install the font that is used to generate the bar code on the local machine where the generated invoice form in Excel format will be previewed.</span></span>

### <a name="use-the-sample-er-format-to-configure-email-destinations"></a><span data-ttu-id="31bfa-228">使用示例 ER 格式配置电子邮件目标</span><span class="sxs-lookup"><span data-stu-id="31bfa-228">Use the sample ER format to configure email destinations</span></span>
<span data-ttu-id="31bfa-229">可使用示例 ER 格式的以下元素配置电子邮件目标：</span><span class="sxs-lookup"><span data-stu-id="31bfa-229">Use the following elements of the sample ER format to configure email destinations:</span></span>

- <span data-ttu-id="31bfa-230">可通过以下 ER 表达式访问客户联系人的电子邮件地址：**model.InvoiceBase.Contact.ElectronicMail**。</span><span class="sxs-lookup"><span data-stu-id="31bfa-230">The email address of a customer contact can be accessed through the following ER expression: **model.InvoiceBase.Contact.ElectronicMail**.</span></span>
- <span data-ttu-id="31bfa-231">可通过以下 ER 表达式访问电子邮件主题文本：**Emailing.TxtToUse.Subject**。</span><span class="sxs-lookup"><span data-stu-id="31bfa-231">The email subject text can be accessed through the following ER expression: **Emailing.TxtToUse.Subject**.</span></span>
- <span data-ttu-id="31bfa-232">可通过以下 ER 表达式访问电子邮件正文文本：**Emailing.TxtToUse.Body**。</span><span class="sxs-lookup"><span data-stu-id="31bfa-232">The email body text can be accessed through the following ER expression: **Emailing.TxtToUse.Body**.</span></span>

![目标设置](media/FTIbyGER-ERFileDestinationSettingEmail.png)

<span data-ttu-id="31bfa-234">电子邮件的主题和正文的默认文本以示例 ER 格式定义。</span><span class="sxs-lookup"><span data-stu-id="31bfa-234">The default text of the email's subject and body is defined in the sample ER format.</span></span> <span data-ttu-id="31bfa-235">语言取决于格式的标签。</span><span class="sxs-lookup"><span data-stu-id="31bfa-235">The language depends on the format's labels.</span></span> <span data-ttu-id="31bfa-236">如果尚未添加已预定义了 **ERFTITMP** ID 的自定义组织电子邮件模板，将把这些默认文本用于电子邮件。</span><span class="sxs-lookup"><span data-stu-id="31bfa-236">This default text will be used for emails if a custom organization email template that has the predefined **ERFTITMP** ID hasn't been added.</span></span>

> [!NOTE]
> <span data-ttu-id="31bfa-237">已在示例 ER 格式中定义了 **ERFTITMP** 电子邮件模板 ID。</span><span class="sxs-lookup"><span data-stu-id="31bfa-237">The **ERFTITMP** email template ID has been defined in the sample ER format.</span></span> <span data-ttu-id="31bfa-238">可在从该示例格式创建的新 ER 格式中根据需要更改该 ID。</span><span class="sxs-lookup"><span data-stu-id="31bfa-238">It can be changed as required in a new ER format that is created from this sample format.</span></span>

<span data-ttu-id="31bfa-239">如果已为您要处理其发票的法人添加了具有预定义的 **ERFTITMP** ID 的组织电子邮件模板，将把电子邮件主题和正文的模板用于生成电子邮件。</span><span class="sxs-lookup"><span data-stu-id="31bfa-239">If the organization email template that has the predefined **ERFTITMP** ID has been added for the legal entity that you're processing the invoice for, the template for the email subject and body text will be used to generate the email.</span></span> 

![组织电子邮件模板](media/FTIbyGER-EmailTemplate.png)

![上载电子邮件模板](media/FTIbyGER-EmailTemplateBody.png)

<span data-ttu-id="31bfa-242">将配置示例 ER 格式的 **Emailing.TxtToUse.Subject** ER 表达式，以便通过处理发票 ID 替换出现的所有占位符 %1。</span><span class="sxs-lookup"><span data-stu-id="31bfa-242">The **Emailing.TxtToUse.Subject** ER expression of the sample ER format is configured to replace any occurrences of the placeholder %1 by the processing invoice ID.</span></span>

<span data-ttu-id="31bfa-243">将为占位符的以下替代项配置示例格式的 **Emailing.TxtToUse.Body** 表达式：</span><span class="sxs-lookup"><span data-stu-id="31bfa-243">The **Emailing.TxtToUse.Body** expression of the sample format is configured for the following substitutions for placeholders:</span></span>

- <span data-ttu-id="31bfa-244">将把“%1”替换为客户的联系人的姓名。</span><span class="sxs-lookup"><span data-stu-id="31bfa-244">"%1" is replaced with the name of the customer's contact person.</span></span>
- <span data-ttu-id="31bfa-245">将把“%2”替换为公司名称。</span><span class="sxs-lookup"><span data-stu-id="31bfa-245">"%2" is replaced with the company name.</span></span>
- <span data-ttu-id="31bfa-246">将把“%3”替换为客户名称。</span><span class="sxs-lookup"><span data-stu-id="31bfa-246">"%3" is replaced with the customer name.</span></span>
- <span data-ttu-id="31bfa-247">将把“%4”替换为公司的联系人的姓名。</span><span class="sxs-lookup"><span data-stu-id="31bfa-247">"%4" is replaced with the name of the company's contact person.</span></span>
- <span data-ttu-id="31bfa-248">将把“%5”替换为公司的联系人的职称。</span><span class="sxs-lookup"><span data-stu-id="31bfa-248">"%5" is replaced with the job title of the company's contact person.</span></span>
- <span data-ttu-id="31bfa-249">将把“%6”替换为公司的联系人的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="31bfa-249">"%6" is replaced with the email address of the company's contact person.</span></span>

![电子邮件地址](media/FTIbyGER-Email.PNG)

## <a name="additional-resources"></a><span data-ttu-id="31bfa-251">其他资源</span><span class="sxs-lookup"><span data-stu-id="31bfa-251">Additional resources</span></span>
[<span data-ttu-id="31bfa-252">电子申报 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="31bfa-252">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
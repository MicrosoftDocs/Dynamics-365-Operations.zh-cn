---
title: 自定义电子报告配置以生成电子单据
description: 本主题介绍了如何自定义 Microsoft 提供的电子报告 (ER) 配置，它们用于生成自定义电子单据。
author: NickSelin
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a0cc308e2e3c7f42295a6170c4f709a835c5c84
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566118"
---
# <a name="customize-electronic-reporting-configurations-to-generate-an-electronic-document"></a><span data-ttu-id="6b4b8-103">自定义电子报告配置以生成电子单据</span><span class="sxs-lookup"><span data-stu-id="6b4b8-103">Customize Electronic reporting configurations to generate an electronic document</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6b4b8-104">通过[电子报告 (ER) 框架](general-electronic-reporting.md)，您可以将 Microsoft 提供的 ER [配置](general-electronic-reporting.md#Configuration)上传到 Microsoft Dynamics 365 Finance 实例。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-104">The [Electronic reporting (ER) framework](general-electronic-reporting.md) lets you upload the ER [configurations](general-electronic-reporting.md#Configuration) that Microsoft provides into your Microsoft Dynamics 365 Finance instance.</span></span> <span data-ttu-id="6b4b8-105">通过此方式，Microsoft 提供的配置可以用作 ER 解决方案，用于生成电子客户发票（电子发票）。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-105">In this way, the Microsoft-provided configurations can serve as the ER solution that is used to generate electronic customer invoices (e-invoices).</span></span> <span data-ttu-id="6b4b8-106">您可以使用此 ER 解决方案配置您的自定义 ER 解决方案，以访问您的自定义数据库字段并生成符合您的特定要求的电子发票，而无需编辑源代码。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-106">You can use this ER solution to configure your custom ER solution to access your custom database fields and generate e-invoices that are compliant with your specific requirements, without having to edit the source code.</span></span>

## <a name="overview"></a><span data-ttu-id="6b4b8-107">概览</span><span class="sxs-lookup"><span data-stu-id="6b4b8-107">Overview</span></span>

<span data-ttu-id="6b4b8-108">对于本主题中的示例，您必须指定联邦纳税标识代码作为您开具电子发票的每个客户的新自定义属性。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-108">For the example in this topic, you must specify a federal tax identification code as a new custom attribute of every customer that you electronically invoice.</span></span> <span data-ttu-id="6b4b8-109">因此，必须通过在生成的每个电子发票中添加一个必须用税码填充的新物料来自定义当前使用的发票的结构。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-109">Therefore, you must customize the structure of the invoice that is currently used, by adding a new item that must be filled with the tax code in every e-invoice that is generated.</span></span>

<span data-ttu-id="6b4b8-110">本主题中的过程介绍了系统管理员、电子报告开发人员或电子报告功能顾问角色的用户如何在 Finance 实例中执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="6b4b8-110">The procedures in this topic explain how a user in the System Administrator, Electronic Reporting Developer, or Electronic Reporting Functional Consultant role can perform the following tasks in your Finance instance:</span></span>

- <span data-ttu-id="6b4b8-111">[配置开始使用 ER 框架所需的最低限度的 ER 参数](#ConfigureER)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-111">[Configure the minimal set of ER parameters that is required to start to use the ER framework](#ConfigureER).</span></span>
- <span data-ttu-id="6b4b8-112">[导入提供用于生成电子发票的标准 ER 配置的初始版本](#ImportERConfigurations1)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-112">[Import the initial versions of the standard ER configurations that are provided to generate e-invoices](#ImportERConfigurations1).</span></span>
- <span data-ttu-id="6b4b8-113">[配置应收帐款参数以开始使用标准 ER 配置](#ConfigureAR1)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-113">[Configure the Accounts receivable parameters to start to use the standard ER configurations](#ConfigureAR1).</span></span>
- <span data-ttu-id="6b4b8-114">[配置法人参数以向客户开具发票](#ConfigureLE)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-114">[Configure the legal entity parameters to invoice customers](#ConfigureLE).</span></span>
- <span data-ttu-id="6b4b8-115">[准备用于开具电子发票的客户记录](#ConfigureCustomer1)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-115">[Prepare a customer record for electronic invoicing](#ConfigureCustomer1).</span></span>
- <span data-ttu-id="6b4b8-116">[使用标准 ER 配置添加、过帐和发送客户发票](#ProcessInvoice1)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-116">[Add, post, and send a customer invoice by using the standard ER configurations](#ProcessInvoice1).</span></span>
- <span data-ttu-id="6b4b8-117">[添加自定义数据库字段以管理客户的联邦纳税标识代码](#AddCustomField)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-117">[Add a custom database field to manage a federal tax identification code for customers](#AddCustomField).</span></span>
- <span data-ttu-id="6b4b8-118">[刷新 ER 元数据以启用 ER 模型映射设计器的数据库更改](#RefreshERMetadata)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-118">[Refresh the ER metadata to enable database changes for the ER model mapping designer](#RefreshERMetadata).</span></span>
- <span data-ttu-id="6b4b8-119">[设计自定义 ER 配置以生成包含新税码的电子发票](#DesignCustomERConfigurations)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-119">[Design the custom ER configurations to generate e-invoices that contain the new tax code](#DesignCustomERConfigurations).</span></span>
- <span data-ttu-id="6b4b8-120">[配置应收帐款参数以开始使用自定义 ER 配置](#ConfigureAR2)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-120">[Configure the Accounts receivable parameters to start to use the custom ER configurations](#ConfigureAR2).</span></span>
- <span data-ttu-id="6b4b8-121">[更新用于开具电子发票的客户记录](#ConfigureCustomer2)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-121">[Update a customer record for electronic invoicing](#ConfigureCustomer2).</span></span>
- <span data-ttu-id="6b4b8-122">[使用自定义 ER 配置添加、过帐和发送客户发票](#ProcessInvoice2)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-122">[Add, post, and send a customer invoice by using the custom ER configurations](#ProcessInvoice2).</span></span>
- <span data-ttu-id="6b4b8-123">[导入提供用于生成电子发票的标准 ER 配置的新版本](#ImportERConfigurations2)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-123">[Import the new versions of the standard ER configurations that are provided to generate e-invoices](#ImportERConfigurations2).</span></span>
- <span data-ttu-id="6b4b8-124">[在您的自定义 ER 配置中采用对标准 ER 配置的新版本所做的更改](#RebaseCustomERConfigurations)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-124">[Adopt the changes to the new versions of the standard ER configurations in your custom ER configurations](#RebaseCustomERConfigurations).</span></span>
- <span data-ttu-id="6b4b8-125">[使用自定义 ER 配置的新版本添加、过帐和发送客户发票](#ProcessInvoice3)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-125">[Add, post, and send a customer invoice by using the new versions of the custom ER configurations](#ProcessInvoice3).</span></span>

<span data-ttu-id="6b4b8-126">所有这些过程都可以在 **DEMF** 公司中完成。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-126">All these procedures can be completed in the **DEMF** company.</span></span>

## <a name="configure-the-er-framework"></a><a name="ConfigureER"></a><span data-ttu-id="6b4b8-127">配置 ER 框架</span><span class="sxs-lookup"><span data-stu-id="6b4b8-127">Configure the ER framework</span></span>

<span data-ttu-id="6b4b8-128">作为电子报告功能顾问或电子报告开发人员角色的用户，您必须配置最低限度的 ER 参数。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-128">As a user in the Electronic Reporting Functional Consultant or Electronic Reporting Developer role, you must configure the minimal set of ER parameters.</span></span> <span data-ttu-id="6b4b8-129">然后，您可以开始使用 ER 框架设计用于生成电子发票的 ER 解决方案的标准配置的自定义版本。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-129">You can then start to use the ER framework to design custom versions of the standard configurations of the ER solution that is used to generate e-invoices.</span></span>

### <a name="configure-er-parameters"></a><span data-ttu-id="6b4b8-130">配置 ER 参数</span><span class="sxs-lookup"><span data-stu-id="6b4b8-130">Configure ER parameters</span></span>

1. <span data-ttu-id="6b4b8-131">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-131">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6b4b8-132">在 **本地化配置** 页面的 **相关链接** 部分中，选择 **电子申报参数**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-132">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="6b4b8-133">在 **电子申报参数** 页上，在 **常规** 选项卡上，将 **启用设计模式** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-133">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="6b4b8-134">在 **附件** 选项卡上，在 **配置** 字段中，选择 **文件**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-134">On the **Attachments** tab, in the **Configurations** field, select **File**.</span></span>
5. <span data-ttu-id="6b4b8-135">在 **作业存档**、**临时**、**基准** 和 **其他** 字段中，选择 **文件** 类型。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-135">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="6b4b8-136">有关 ER 参数的详细信息，请参阅[配置 ER 框架](electronic-reporting-er-configure-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-136">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><span data-ttu-id="6b4b8-137">激活 ER 配置提供程序</span><span class="sxs-lookup"><span data-stu-id="6b4b8-137">Activate an ER configuration provider</span></span>

<span data-ttu-id="6b4b8-138">将把添加的每个 ER 配置标记为由 ER 配置提供程序负责。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-138">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="6b4b8-139">在 **电子申报** 工作区中激活的 ER 配置提供程序用于此目的。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-139">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="6b4b8-140">因此，必须先在 **电子申报** 工作区中激活 ER 配置提供程序，才能开始添加或编辑 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-140">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="6b4b8-141">只有 ER 配置的负责人才能对其进行编辑。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-141">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="6b4b8-142">因此，必须先在 **电子申报** 工作区中激活相应 ER 配置提供程序，才能编辑 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-142">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><span data-ttu-id="6b4b8-143">查看 ER 配置提供程序列表</span><span class="sxs-lookup"><span data-stu-id="6b4b8-143">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="6b4b8-144">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-144">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6b4b8-145">在 **本地化配置** 页面的 **相关链接** 部分中，选择 **配置提供程序**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-145">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="6b4b8-146">在 **配置提供程序表** 页面中，每条提供程序记录都有唯一名称和 URL。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-146">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="6b4b8-147">查看此页面的内容。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-147">Review the contents of this page.</span></span> <span data-ttu-id="6b4b8-148">如果已有 **Litware, Inc.** (`https://www.litware.com`) 的记录，请跳过下一过程，即[添加新 ER 配置提供程序](#AddProvider)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-148">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#AddProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a><span data-ttu-id="6b4b8-149">添加新 ER 配置提供程序</span><span class="sxs-lookup"><span data-stu-id="6b4b8-149">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="6b4b8-150">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-150">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6b4b8-151">在 **本地化配置** 页面的 **相关链接** 部分中，选择 **配置提供程序**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-151">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="6b4b8-152">在 **配置提供程序** 页面上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-152">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="6b4b8-153">在 **名称** 字段中，输入 **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="6b4b8-153">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="6b4b8-154">在 **Internet 地址** 字段中，输入 `https://www.litware.com`。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-154">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="6b4b8-155">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-155">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><span data-ttu-id="6b4b8-156">激活 ER 配置提供程序</span><span class="sxs-lookup"><span data-stu-id="6b4b8-156">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="6b4b8-157">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-157">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6b4b8-158">在 **本地化配置** 页面的 **配置提供程序** 部分中，选择 **Litware, Inc.** 磁贴，然后选择 **设置有效**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-158">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="6b4b8-159">有关 ER 配置提供程序的详细信息，请参阅[创建配置提供程序并将其标记为有效](tasks/er-configuration-provider-mark-it-active-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-159">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="import-the-initial-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations1"></a><span data-ttu-id="6b4b8-160">导入标准 ER 配置的初始版本</span><span class="sxs-lookup"><span data-stu-id="6b4b8-160">Import the initial versions of standard ER configurations</span></span>

<span data-ttu-id="6b4b8-161">若要向当前 Finance 实例添加标准 ER 配置，必须从为该实例配置的 ER [存储库](general-electronic-reporting.md#Repository)中导入这些配置。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-161">To add the standard ER configurations to your current Finance instance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="6b4b8-162">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-162">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6b4b8-163">在 **本地化配置** 页面的 **配置提供程序** 部分中，选择 **Microsoft** 磁贴，然后选择 **存储库** 查看 Microsoft 提供程序的存储库列表。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-163">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="6b4b8-164">在 **配置存储库** 页，选择 **全球** 类型的存储库，然后选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-164">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="6b4b8-165">如果提示您进行授权以连接到 Regulatory Configuration Service，请按照授权说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-165">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="6b4b8-166">在 **配置存储库** 页面上，在左侧窗格的配置树中，选择 **Peppol 销售发票** 格式配置。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-166">On the **Configuration repository** page, in the configuration tree in the left pane, select the **Peppol Sales Invoice** format configuration.</span></span>
5. <span data-ttu-id="6b4b8-167">在 **版本** 快速选项卡中，选择版本 **11.2.2**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-167">On the **Versions** FastTab, select version **11.2.2**.</span></span>
6. <span data-ttu-id="6b4b8-168">选择 **导入** 以从全局存储库中下载所选版本。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-168">Select **Import** to download the selected version from the Global repository.</span></span>

![配置存储库页面](./media/er-quick-start3-import-solution1.png)

> [!TIP]
> <span data-ttu-id="6b4b8-170">如果在访问[全球存储库](er-download-configurations-global-repo.md)时遇到问题，可改为从 Microsoft Dynamics Lifecycle Services (LCS)[ 下载配置](download-electronic-reporting-configuration-lcs.md)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-170">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from Microsoft Dynamics Lifecycle Services (LCS) instead.</span></span>

### <a name="review-the-imported-er-configurations"></a><span data-ttu-id="6b4b8-171">查看导入的 ER 配置</span><span class="sxs-lookup"><span data-stu-id="6b4b8-171">Review the imported ER configurations</span></span>

1. <span data-ttu-id="6b4b8-172">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-172">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6b4b8-173">在 **本地化配置** 页面的 **配置** 部分中，选择 **报告配置** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-173">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="6b4b8-174">在 **配置** 页面上，展开 **配置组件** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-174">On the **Configurations** page, expand the **Configuration components** FastTab.</span></span>
4. <span data-ttu-id="6b4b8-175">在左侧窗格的配置树中，展开 **发票模型**，然后展开 **UBL 销售发票**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-175">In the configuration tree in the left pane, expand **Invoice model**, and then expand **UBL Sales invoice**.</span></span>

<span data-ttu-id="6b4b8-176">请注意，除了所选的 **Peppol 销售发票** ER 格式，还导入了其他必需的 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-176">Notice that, in addition to the selected **Peppol Sales Invoice** ER format, other required ER configurations were imported.</span></span> <span data-ttu-id="6b4b8-177">因为将向全局存储库和 LCS 不断发布 ER 配置的新版本以使相应的解决方案符合新要求，因此导入了所需的[数据模型](general-electronic-reporting.md#data-model-and-model-mapping-components)配置及其[模型映射](general-electronic-reporting.md#data-model-and-model-mapping-components)配置的最新版本。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-177">Because new versions of ER configurations are constantly published to the Global repository and LCS to keep the corresponding solutions compliant with new requirements, the latest versions of the required [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) configuration and its [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) configurations were imported.</span></span>

![配置页面](./media/er-quick-start3-imported-solution1a.png)

<span data-ttu-id="6b4b8-179">若要在之前已导入 **Peppol 销售发票** ER 格式的版本 **11.2.2**（例如 2019 年 8 月 7 日）的情况下模拟 ER 配置在当前 Finance 实例中的状态，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-179">To simulate the state that ER configurations in the current Finance instance  would be in if you imported version **11.2.2** of the **Peppol Sales Invoice** ER format in the past (for example, on August 7, 2019), follow these steps.</span></span>

- <span data-ttu-id="6b4b8-180">在“操作”窗格上，选择 **删除** 以删除 2019 年 8 月 7 日之后发布的所有 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-180">On the Action Pane, select **Delete** to delete all ER configurations that were published after August 7, 2019.</span></span> <span data-ttu-id="6b4b8-181">必须仅保留 **发票模型**、**发票模型映射**（最初命名为 **客户发票模型映射**）、**UBL 销售发票** 和 **Peppol 销售发票** 配置。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-181">The only **Invoice model**, **Invoice model mapping** (initially named **Customer invoice model mapping**), **UBL Sales invoice** and **Peppol Sales Invoice** configurations must be left.</span></span>
- <span data-ttu-id="6b4b8-182">对于其余的 ER 配置，请在 **版本** 快速选项卡上，选择 **删除** 以删除 2019 年 8 月 7 日之后发布的 ER 配置的所有版本。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-182">For the remained ER configurations, on the **Versions** FastTab, select **Delete** to delete all versions of ER configurations that were published after August 7, 2019.</span></span>

<span data-ttu-id="6b4b8-183">然后，验证配置树中是否有以下 ER 配置：</span><span class="sxs-lookup"><span data-stu-id="6b4b8-183">Then verify that the following configurations are available in the configuration tree:</span></span>

- <span data-ttu-id="6b4b8-184">**发票模型** ER 数据模型配置（最初命名为 **客户发票模型**）：</span><span class="sxs-lookup"><span data-stu-id="6b4b8-184">**Invoice model** ER data model configuration (initially named **Customer invoice model**):</span></span>

    - <span data-ttu-id="6b4b8-185">版本 11 包含[数据模型](general-electronic-reporting.md#data-model-and-model-mapping-components) ER 组件的版本 10，用于表示开票业务域的数据结构。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-185">Version 11 contains version 10 of the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that represents the data structure of the invoicing business domain.</span></span> <span data-ttu-id="6b4b8-186">此 ER 配置已导入，作为选择导入的 **Peppol 销售发票** ER 格式的上级。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-186">This ER configuration has been imported as an ancestor of the **Peppol Sales Invoice** ER format that was selected for import.</span></span>
    - <span data-ttu-id="6b4b8-187">版本 50 包含数据模型 ER 组件的版本 31。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-187">Version 50 contains version 31 of the data model ER component.</span></span> <span data-ttu-id="6b4b8-188">此 ER 配置已导入，作为 **发票模型映射** ER 模型映射配置的 2019 年 8 月 7 日版本的上级。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-188">This ER configuration has been imported as an ancestor of the August 7, 2019, version of the **Invoice model mapping** ER model mapping configuration.</span></span>

    ![“配置”页面上的发票模型 ER 数据模型配置](./media/er-quick-start3-imported-solution1b1.png)

    > [!TIP]
    > <span data-ttu-id="6b4b8-190">如果看不到该数据模型的版本 50，请打开全局存储库，然后导入 **发票模型映射** ER 配置的版本 50.19。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-190">If you don't see version 50 of this data model, open the Global repository, and import version 50.19 of the **Invoice model mapping** ER configuration.</span></span>

- <span data-ttu-id="6b4b8-191">**发票模型映射** ER 模型映射配置（最初命名为 **客户发票模型映射**）：</span><span class="sxs-lookup"><span data-stu-id="6b4b8-191">**Invoice model mapping** ER model mapping configuration (initially named **Customer invoice model mapping**):</span></span>

    - <span data-ttu-id="6b4b8-192">版本 50.19 已导入，作为 **发票模型** ER 数据模型配置的版本 50 的最新实现。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-192">Version 50.19 has been imported as the latest implementation of version 50 of the **Invoice model** ER data model configuration.</span></span> <span data-ttu-id="6b4b8-193">它包含两个[模型映射](general-electronic-reporting.md#data-model-and-model-mapping-components) ER 组件，用于描述在运行时如何使用应用程序数据填充数据模型。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-193">It contains two [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) ER components that describe how the data model is filled in with application data at runtime.</span></span>

    ![“配置”页面上的发票模型映射 ER 模型映射配置](./media/er-quick-start3-imported-solution1b2.png)

    > [!TIP]
    > <span data-ttu-id="6b4b8-195">如果看不到该模型映射的版本 50.19，请打开全局存储库，然后导入 **发票模型映射** ER 配置的版本 50.19。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-195">If you don't see version 50.19 of this model mapping, open the Global repository, and import version 50.19 of the **Invoice model mapping** ER configuration.</span></span>

- <span data-ttu-id="6b4b8-196">**UBL 销售发票** ER 格式配置：</span><span class="sxs-lookup"><span data-stu-id="6b4b8-196">**UBL Sales invoice** ER format configuration:</span></span>

    - <span data-ttu-id="6b4b8-197">版本 11.2 包含[格式](general-electronic-reporting.md#FormatComponentOutbound)和格式映射 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-197">Version 11.2 contains the [format](general-electronic-reporting.md#FormatComponentOutbound) and format mapping ER components.</span></span> <span data-ttu-id="6b4b8-198">格式组件指定报表布局。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-198">The format component specifies the report layout.</span></span> <span data-ttu-id="6b4b8-199">格式映射组件包含模型数据源，并指定如何在运行时使用此数据源填充报告布局。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-199">The format mapping component contains the model data source and specifies how this data source is used to fill in the report layout at runtime.</span></span> <span data-ttu-id="6b4b8-200">该 ER 格式配置为生成通用商业语言 (UBL) 格式的电子发票。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-200">This ER format was configured to generate e-invoices in Universal Business Language (UBL) format.</span></span> <span data-ttu-id="6b4b8-201">它已导入，作为选择导入的 **Peppol 销售发票** ER 格式的父级。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-201">It has been imported as a parent of the **Peppol Sales Invoice** ER format that was selected for import.</span></span>

- <span data-ttu-id="6b4b8-202">**Peppol 销售发票** ER 格式配置：</span><span class="sxs-lookup"><span data-stu-id="6b4b8-202">**Peppol Sales Invoice** ER format configuration:</span></span>

    - <span data-ttu-id="6b4b8-203">版本 11.2.2 包含格式和格式映射 ER 组件，它们配置为生成泛欧洲 Public Procurement OnLine (PEPPOL) 格式的电子发票。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-203">Version 11.2.2 contains the format and format mapping ER components that were configured to generate e-invoices in Pan-European Public Procurement OnLine (PEPPOL) format.</span></span>

    ![“配置”页面上的 Peppol 销售发票 ER 格式配置](./media/er-quick-start3-imported-solution1b3.png)

## <a name="configure-the-accounts-receivable-parameters"></a><a name="ConfigureAR1"></a><span data-ttu-id="6b4b8-205">配置应收帐款参数</span><span class="sxs-lookup"><span data-stu-id="6b4b8-205">Configure the Accounts receivable parameters</span></span>

1. <span data-ttu-id="6b4b8-206">转到 **应收帐款** \> **设置** \> **应收帐款参数**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-206">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="6b4b8-207">在 **电子单据** 选项卡上，在 **电子报告** 快速选项卡上，在 **销售和普通发票** 字段中，选择 **Peppol 销售发票**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-207">On the **Electronic documents** tab, on the **Electronic reporting** FastTab, in the **Sales and Free text invoice** field, select **Peppol Sales Invoice**.</span></span>
3. <span data-ttu-id="6b4b8-208">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-208">Select **Save**.</span></span>

![应收帐款参数页面上的电子单据选项卡](./media/er-quick-start3-configure-ar1.png)

## <a name="configure-the-legal-entity-parameters"></a><a name="ConfigureLE"></a><span data-ttu-id="6b4b8-210">配置法人参数</span><span class="sxs-lookup"><span data-stu-id="6b4b8-210">Configure the legal entity parameters</span></span>

1. <span data-ttu-id="6b4b8-211">转到 **组织管理** \> **组织** \> **法人**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-211">Go to **Organization administration** \> **Organizations** \> **Legal entities**.</span></span>
2. <span data-ttu-id="6b4b8-212">对于所选的 **DEMF** 公司，在 **银行帐户信息** 快速选项卡上，在 **银行代号** 字段中，输入 **1234**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-212">For the selected **DEMF** company, on the **Bank account information** FastTab, in the **Routing number** field, enter **1234**.</span></span>
3. <span data-ttu-id="6b4b8-213">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-213">Select **Save**.</span></span>
4. <span data-ttu-id="6b4b8-214">关闭 **法人** 页面。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-214">Close the **Legal entities** page.</span></span>

## <a name="prepare-a-customer-record"></a><a name="ConfigureCustomer1"></a><span data-ttu-id="6b4b8-215">准备客户记录</span><span class="sxs-lookup"><span data-stu-id="6b4b8-215">Prepare a customer record</span></span>

1. <span data-ttu-id="6b4b8-216">转到 **应收帐款** \> **客户** \> **所有客户**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-216">Go to **Accounts receivable** \> **Customers** \> **All customers**.</span></span>
2. <span data-ttu-id="6b4b8-217">在 **所有客户** 页面上，选择 **DE-014** 客户帐户链接。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-217">On the **All customers** page, select the **DE-014** customer account link.</span></span>

### <a name="add-a-customer-contact"></a><span data-ttu-id="6b4b8-218">添加客户联系人</span><span class="sxs-lookup"><span data-stu-id="6b4b8-218">Add a customer contact</span></span>

1. <span data-ttu-id="6b4b8-219">转到 **应收帐款** \> **客户** \> **所有客户**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-219">Go to **Accounts receivable** \> **Customers** \> **All customers**.</span></span>
2. <span data-ttu-id="6b4b8-220">在“操作”窗格的 **客户** 选项卡上，在 **帐户** 组中，选择 **联系人**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-220">On the Action Pane, on the **Customer** tab, in the **Accounts** group, select **Contacts**.</span></span>
3. <span data-ttu-id="6b4b8-221">选择 **添加联系人**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-221">Select **Add contacts**.</span></span>
4. <span data-ttu-id="6b4b8-222">在 **联系人** 页面的 **名字** 字段中，打开查找，选择 **Adam Carter**，然后选择 **选择** 以关闭查找。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-222">On the **Contacts** page, in the **First name** field, open the lookup, select **Adam Carter**, and then select **Select** to close the lookup.</span></span>
5. <span data-ttu-id="6b4b8-223">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-223">Select **Save**.</span></span>
6. <span data-ttu-id="6b4b8-224">关闭 **联系人** 页面。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-224">Close the **Contacts** page.</span></span>

### <a name="define-a-primary-contact"></a><span data-ttu-id="6b4b8-225">定义主要联系人</span><span class="sxs-lookup"><span data-stu-id="6b4b8-225">Define a primary contact</span></span>

1. <span data-ttu-id="6b4b8-226">转到 **应收帐款** \> **客户** \> **所有客户**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-226">Go to **Accounts receivable** \> **Customers** \> **All customers**.</span></span>
2. <span data-ttu-id="6b4b8-227">在 **销售人口统计数据** 快速选项卡上，在 **主要联系人** 字段中，选择 **Adam Carter**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-227">On the **Sales demographics** FastTab, in the **Primary contact** field, select **Adam Carter**.</span></span>

### <a name="set-the-e-invoicing-option"></a><span data-ttu-id="6b4b8-228">设置电子开票选项</span><span class="sxs-lookup"><span data-stu-id="6b4b8-228">Set the e-invoicing option</span></span>

1. <span data-ttu-id="6b4b8-229">转到 **应收帐款** \> **客户** \> **所有客户**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-229">Go to **Accounts receivable** \> **Customers** \> **All customers**.</span></span>
2. <span data-ttu-id="6b4b8-230">在 **发票和交货** 快速选项卡上，将 **电子发票** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-230">On the **Invoice and delivery** FastTab, set the **eInvoice** option to **Yes**.</span></span>
3. <span data-ttu-id="6b4b8-231">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-231">Select **Save**.</span></span>
4. <span data-ttu-id="6b4b8-232">关闭 **所有客户** 页面。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-232">Close the **All customers** page.</span></span>

## <a name="process-a-customer-invoice-by-using-the-standard-er-configurations"></a><a name="ProcessInvoice1"></a><span data-ttu-id="6b4b8-233">使用标准 ER 配置处理客户发票</span><span class="sxs-lookup"><span data-stu-id="6b4b8-233">Process a customer invoice by using the standard ER configurations</span></span>

<span data-ttu-id="6b4b8-234">现在，您可以使用导入的标准 ER 配置以电子方式将普通发票发送给客户。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-234">You can now use the standard ER configurations that you imported to electronically send a free text invoice to a customer.</span></span>

### <a name="add-a-new-invoice"></a><span data-ttu-id="6b4b8-235">添加新发票</span><span class="sxs-lookup"><span data-stu-id="6b4b8-235">Add a new invoice</span></span>

1. <span data-ttu-id="6b4b8-236">转至 **应收帐款** \> **发票** \> **所有普通发票**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-236">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="6b4b8-237">在 **普通发票** 页面上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-237">On the **Free text invoice** page, select **New**.</span></span>
3. <span data-ttu-id="6b4b8-238">在 **普通发票标题** 快速选项卡上，在 **客户帐户** 字段中，选择 **DE-014**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-238">On the **Free text invoice header** FastTab, in the **Customer account** field, select **DE-014**.</span></span>
4. <span data-ttu-id="6b4b8-239">在 **发票行** 快速选项卡上，自动添加发票行。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-239">On the **Invoice lines** FastTab, an invoice line is automatically added.</span></span> <span data-ttu-id="6b4b8-240">在此行上，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="6b4b8-240">On this line, set the following fields:</span></span>

    - <span data-ttu-id="6b4b8-241">在 **描述** 字段中，输入 **Notebook**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-241">In the **Description** field, enter **Notebook**.</span></span>
    - <span data-ttu-id="6b4b8-242">在 **主帐户** 字段中，选择 **401100**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-242">In the **Main account** field, select **401100**.</span></span>
    - <span data-ttu-id="6b4b8-243">在 **单位价格** 字段中，输入 **1000**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-243">In the **Unit price** field, enter **1000**.</span></span>

5. <span data-ttu-id="6b4b8-244">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-244">Select **Save**.</span></span>

![普通发票页面](./media/er-quick-start3-add-invoice.png)

<span data-ttu-id="6b4b8-246">有关详细信息，请参阅[创建普通发票](../../../finance/accounts-receivable/create-free-text-invoice-new.md)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-246">For more information, see [Create a free text invoice](../../../finance/accounts-receivable/create-free-text-invoice-new.md).</span></span>

### <a name="post-a-new-invoice"></a><span data-ttu-id="6b4b8-247">过帐新发票</span><span class="sxs-lookup"><span data-stu-id="6b4b8-247">Post a new invoice</span></span>

1. <span data-ttu-id="6b4b8-248">转至 **应收帐款** \> **发票** \> **所有普通发票**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-248">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="6b4b8-249">在 **普通发票** 页面上，在“操作”窗格上，选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-249">On the **Free text invoice** page, on the Action Pane, select **Post**.</span></span>
3. <span data-ttu-id="6b4b8-250">在 **过帐普通发票** 对话框中，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-250">In the **Post free text invoice** dialog box, select **OK**.</span></span>

![普通发票详细信息页面](./media/er-quick-start3-post-invoice.png)

### <a name="send-a-posted-invoice"></a><span data-ttu-id="6b4b8-252">发送一个已过帐发票</span><span class="sxs-lookup"><span data-stu-id="6b4b8-252">Send a posted invoice</span></span>

1. <span data-ttu-id="6b4b8-253">转至 **应收帐款** \> **发票** \> **所有普通发票**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-253">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="6b4b8-254">在 **普通发票** 页面上，在“操作”窗格的 **单据** 组中，选择 **发送** \> **原始**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-254">On the **Free text invoice** page, on the Action Pane, in the **Document** group, select **Send** \> **Original**.</span></span>

    ![原始发票预览](./media/er-quick-start3-send-invoice.png)

3. <span data-ttu-id="6b4b8-256">关闭 **普通发票** 页面。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-256">Close the **Free text invoice** page.</span></span>

### <a name="analyze-a-generated-e-invoice"></a><span data-ttu-id="6b4b8-257">分析生成的电子发票</span><span class="sxs-lookup"><span data-stu-id="6b4b8-257">Analyze a generated e-invoice</span></span>

1. <span data-ttu-id="6b4b8-258">转到 **组织管理** \> **电子报告** \> **电子报告作业**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-258">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>
2. <span data-ttu-id="6b4b8-259">在 **电子报告作业** 页面上，选择具有任务描述 **发送电子发票 XML** 的初始记录。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-259">On the **Electronic reporting jobs** page, select the initial record that has the task description **Send the eInvoice XML**.</span></span>
3. <span data-ttu-id="6b4b8-260">选择 **显示文件** 以访问生成的文件列表。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-260">Select **Show files** to access the list of generated files.</span></span>

    ![电子报告作业页面](./media/er-quick-start3-jobs-list.png)

4. <span data-ttu-id="6b4b8-262">选择 **打开** 以下载生成的电子发票 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-262">Select **Open** to download the e-invoice XML file that is generated.</span></span>
5. <span data-ttu-id="6b4b8-263">分析电子发票 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-263">Analyze the e-invoice XML file.</span></span> <span data-ttu-id="6b4b8-264">请注意，客户税架构当前由 **schemeID** 和 **schemeAgencyID** XML 属性表示。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-264">Notice that the customer tax schema is currently represented by the **schemeID** and **schemeAgencyID** XML attributes.</span></span> <span data-ttu-id="6b4b8-265">另请注意，**cbc:CustomizationID** XML 元素当前包含以下文本：`urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0`。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-265">Also notice that the **cbc:CustomizationID** XML element currently contains the following text: `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0`.</span></span>

    ![生成的电子发票 XML 文件预览](./media/er-quick-start3-e-invoice1.png)

## <a name="add-a-custom-database-field"></a><a name="AddCustomField"></a><span data-ttu-id="6b4b8-267">添加自定义数据库字段</span><span class="sxs-lookup"><span data-stu-id="6b4b8-267">Add a custom database field</span></span>

<span data-ttu-id="6b4b8-268">您可以使用[自定义字段](../../fin-ops/get-started/user-defined-fields.md)功能在当前的 Finance 实例中执行以下自定义：</span><span class="sxs-lookup"><span data-stu-id="6b4b8-268">You can use the [Custom field](../../fin-ops/get-started/user-defined-fields.md) feature to do the following customization in the current Finance instance:</span></span>

- <span data-ttu-id="6b4b8-269">通过添加为每个客户存储联邦纳税标识代码的新自定义数据库字段来自定义数据库结构。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-269">Customize the database structure by adding a new custom database field that stores a federal tax identification code for every customer.</span></span>
- <span data-ttu-id="6b4b8-270">通过添加可用于在新自定义数据库字段中输入税码值的新数据输入字段来自定义 **客户** 页面。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-270">Customize the **Customer** page by adding a new data entry field that can be used to enter a tax code value in the new custom database field.</span></span>

<span data-ttu-id="6b4b8-271">请按照以下步骤进行自定义。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-271">Follow these steps to do the customization.</span></span>

1. <span data-ttu-id="6b4b8-272">转到 **应收帐款** \> **客户** \> **所有客户**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-272">Go to **Accounts receivables** \> **Customers** \> **All customers**.</span></span>
2. <span data-ttu-id="6b4b8-273">在 **所有客户** 页面上，选择 **DE-014** 客户帐户链接。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-273">On the **All customers** page, select the **DE-014** customer account link.</span></span>
3. <span data-ttu-id="6b4b8-274">在 **常规** 快速选项卡上，右键单击 **语言** 字段下的任何空白区域，然后选择 **个性化：UpperGroup**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-274">On the **General** FastTab, right-click in any blank area under the **Language** field, and then select **Personalize: UpperGroup**.</span></span>

    <span data-ttu-id="6b4b8-275">将突出显示 **常规** 快速选项卡的内容并将显示 **个性化** 菜单。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-275">The contents of the **General** FastTab are highlighted, and a **Personalize** menu appears.</span></span>

4. <span data-ttu-id="6b4b8-276">在 **个性化** 菜单上，选择 **添加字段**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-276">On the **Personalize** menu, select **Add a field**.</span></span>
5. <span data-ttu-id="6b4b8-277">在 **添加列** 对话框中，选择 **创建新字段**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-277">In the **Add columns** dialog box, select **Create new field**.</span></span>
6. <span data-ttu-id="6b4b8-278">在 **创建新字段** 对话框中，在 **表单名称** 字段中，选择 **客户**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-278">In the **Create new field** dialog box, in the **Table name** field, select **Customers**.</span></span>
7. <span data-ttu-id="6b4b8-279">在 **名称前缀** 字段中，输入 **FederalTaxID**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-279">In the **Name prefix** field, enter **FederalTaxID**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6b4b8-280">整个字段名称已自动定义为 **FederalTaxID\_Custom**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-280">The whole field name has been automatically defined as **FederalTaxID\_Custom**.</span></span>

8. <span data-ttu-id="6b4b8-281">在 **标签** 字段中，输入 **税号标识**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-281">In the **Label** field, enter **Federal Tax ID**.</span></span>
9. <span data-ttu-id="6b4b8-282">在 **类型** 字段中，选择 **文本**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-282">In the **Type** field, select **Text**.</span></span>
10. <span data-ttu-id="6b4b8-283">在 **长度** 字段中，输入 **20**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-283">In the **Length** field, enter **20**.</span></span>
11. <span data-ttu-id="6b4b8-284">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-284">Select **Save**.</span></span>
12. <span data-ttu-id="6b4b8-285">在显示的消息框中，选择 **是** 以确认您要为 **客户** 表创建新的 **FederalTaxID** 字段输入。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-285">In the message box that appears, select **Yes** to confirm that you want to create a new **FederalTaxID** field entry for the **Customers** table.</span></span>
13. <span data-ttu-id="6b4b8-286">选择 **插入** 以 <a name="insert_custom_field"></a>向当前页面添加 **FederalTaxID\_Custom** 字段。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-286">Select **Insert** to <a name="insert_custom_field"></a>add the **FederalTaxID\_Custom** field to the current page.</span></span>

    ![所有客户页面](./media/er-quick-start3-create-new-field.gif)

14. <span data-ttu-id="6b4b8-288">关闭 **所有客户** 页面。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-288">Close the **All customers** page.</span></span>

## <a name="refresh-the-er-metadata"></a><a name="RefreshERMetadata"></a><span data-ttu-id="6b4b8-289">刷新 ER 元数据</span><span class="sxs-lookup"><span data-stu-id="6b4b8-289">Refresh the ER metadata</span></span>

<span data-ttu-id="6b4b8-290">您必须刷新 ER 元数据，才能使添加的自定义字段在 ER 模型映射设计器中[可见](electronic-reporting-er-configure-parameters.md#frequently-asked-questions)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-290">You must refresh the ER metadata to make the custom field that you added [visible](electronic-reporting-er-configure-parameters.md#frequently-asked-questions) in the ER model mapping designer.</span></span>

1. <span data-ttu-id="6b4b8-291">转到 **组织管理** \> **电子报告** \> **重建表格引用**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-291">Go to **Organization administration** \> **Electronic reporting** \> **Rebuild table references**.</span></span>
2. <span data-ttu-id="6b4b8-292">在 **更新数据模型** 对话框中，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-292">In the **Update data model** dialog box, select **OK**.</span></span>

## <a name="design-the-custom-er-configurations"></a><a name="DesignCustomERConfigurations"></a><span data-ttu-id="6b4b8-293">设计自定义 ER 配置</span><span class="sxs-lookup"><span data-stu-id="6b4b8-293">Design the custom ER configurations</span></span>

<span data-ttu-id="6b4b8-294">您可以使用 Microsoft 提供的 ER 配置来设计自定义 ER 配置，以便它们生成包含新税码的电子发票。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-294">You can use the Microsoft-provided ER configurations to design your custom ER configurations so that they generate e-invoices that contain the new tax code.</span></span>

### <a name="customize-the-data-model-configuration"></a><span data-ttu-id="6b4b8-295">自定义数据模型配置</span><span class="sxs-lookup"><span data-stu-id="6b4b8-295">Customize the data model configuration</span></span>

<span data-ttu-id="6b4b8-296">作为电子报告功能顾问角色的用户，您可以设计自定义 ER 数据模型。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-296">As a user in the Electronic Reporting Functional Consultant role, you can design your custom ER data model.</span></span>

#### <a name="add-a-custom-data-model-configuration"></a><span data-ttu-id="6b4b8-297">添加自定义数据模型配置</span><span class="sxs-lookup"><span data-stu-id="6b4b8-297">Add a custom data model configuration</span></span>

1. <span data-ttu-id="6b4b8-298">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-298">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6b4b8-299">在 **配置** 页面上，在左侧窗格的配置树中，选择 **客户发票模型**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-299">On the **Configurations** page, in the configuration tree in the left pane, select **Customer invoice model**.</span></span>
3. <span data-ttu-id="6b4b8-300">在操作窗格中选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-300">On the Action Pane, select **Create configuration**.</span></span>
4. <span data-ttu-id="6b4b8-301">在下拉对话框的 **新建** 字段中，选择 **从名称派生：客户发票模型，Microsoft** 以表示您的新自定义 ER 数据模型配置应基于 ER 数据模型配置。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-301">In the drop-down dialog box, in the **New** field, select **Derive from Name: Customer invoice model, Microsoft** to indicate that your new custom ER data model configuration should be based on the ER data model configuration.</span></span>
5. <span data-ttu-id="6b4b8-302">在 **名称** 字段中，输入 **发票模型 (Litware)**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-302">In the **Name** field, enter **Invoice model (Litware)**.</span></span>
6. <span data-ttu-id="6b4b8-303">选择 **创建配置** 以添加新 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-303">Select **Create configuration** to add the new ER configuration.</span></span>

<span data-ttu-id="6b4b8-304">现在，您可以使用 ER 数据模型设计器在 **草稿**[状态](general-electronic-reporting.md#component-versioning)下编辑 **发票模型 (Litware)** ER 配置的版本 50.1。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-304">You can now use the ER data model designer to edit version 50.1 of the **Invoice model (Litware)** ER configuration in **Draft** [status](general-electronic-reporting.md#component-versioning).</span></span>

![“配置”页面上的 ER 配置的版本 50.1](./media/er-quick-start3-added-custom-model.png)

#### <a name="configure-a-custom-data-model"></a><span data-ttu-id="6b4b8-306">配置自定义数据模型</span><span class="sxs-lookup"><span data-stu-id="6b4b8-306">Configure a custom data model</span></span>

<span data-ttu-id="6b4b8-307">您必须通过添加新字段以提供联邦纳税标识码的值来修改自定义数据模型。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-307">You must modify your custom data model by adding a new field to provide the value of a federal tax identification code.</span></span> <span data-ttu-id="6b4b8-308">对于每种将使用此数据模型作为数据源的 ER 格式，此代码都是客户数据的一部分。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-308">This code is part of the customer data for every ER format that will use this data model as a data source.</span></span>

1. <span data-ttu-id="6b4b8-309">在 **配置** 页面上，在左侧窗格的配置树中，选择 **发票模型 (Litware)**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-309">On the **Configurations** page, in the configuration tree in the left pane, select **Invoice model (Litware)**.</span></span>
2. <span data-ttu-id="6b4b8-310">在 **版本** 快速选项卡上，在 **草稿** 状态下选择所选 ER 数据模型配置的版本 **50.1**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-310">On the **Versions** FastTab, select version **50.1** of the selected ER data model configuration in **Draft** status.</span></span>
3. <span data-ttu-id="6b4b8-311">在“操作”窗格上，为所选配置版本选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-311">On the Action Pane, select **Designer** for the selected configuration version.</span></span>
4. <span data-ttu-id="6b4b8-312">在 **数据模型设计器** 页面的数据模型树中，选择 **客户信息（客户）**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-312">On the **Data model designer** page, in the data model tree, select **Customer information (Customer)**.</span></span>
5. <span data-ttu-id="6b4b8-313">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-313">Select **New**.</span></span>
6. <span data-ttu-id="6b4b8-314">在下拉对话框中，在 **作为以下项的新节点** 字段中，接受默认值 **活动节点的子节点**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-314">In the drop-down dialog box, in the **New node as a** field, accept the default value, **Child of an active node**.</span></span>
7. <span data-ttu-id="6b4b8-315">在 **名称** 字段中，输入 **FederalTaxID\_Litware**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-315">In the **Name** field, enter **FederalTaxID\_Litware**.</span></span>
8. <span data-ttu-id="6b4b8-316">在 **物料类型** 字段中，接受默认值 **字符串**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-316">In the **Item type** field, accept the default value, **String**.</span></span>
9. <span data-ttu-id="6b4b8-317">选择 **添加**，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-317">Select **Add**, and then select **Save**.</span></span>

    ![数据模型设计器页面](./media/er-quick-start3-add-data-model-field.png)

    > [!NOTE]
    > <span data-ttu-id="6b4b8-319">**标签** 和 **描述** 字段描述了新字段的目的。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-319">The **Label** and **Description** fields describe the purpose of the new field.</span></span> <span data-ttu-id="6b4b8-320">您可以用多种语言填写这些字段。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-320">You can fill in these fields in multiple languages.</span></span> <span data-ttu-id="6b4b8-321">有关详细信息，请参阅[在电子报告中设计多语言报告](er-design-multilingual-reports.md)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-321">For more information, see [Design multilingual reports in Electronic reporting](er-design-multilingual-reports.md).</span></span>

10. <span data-ttu-id="6b4b8-322">关闭 **数据模型设计器** 页。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-322">Close the **Data model designer** page.</span></span>

#### <a name="complete-a-custom-data-model-configuration"></a><span data-ttu-id="6b4b8-323">完成自定义数据模型配置</span><span class="sxs-lookup"><span data-stu-id="6b4b8-323">Complete a custom data model configuration</span></span>

<span data-ttu-id="6b4b8-324">您必须[完成](general-electronic-reporting.md#component-versioning)自定义 ER 数据模型配置的版本 50.1 的工作以使其可用，以便可以添加其他自定义 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-324">You must [complete](general-electronic-reporting.md#component-versioning) your work with version 50.1 of your custom ER data model configuration to make it available so that other custom ER configurations can be added.</span></span>

1. <span data-ttu-id="6b4b8-325">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-325">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6b4b8-326">在 **配置** 页面上，在左侧窗格的配置树中，展开 **发票模型**，然后选择 **发票模型 (Litware)**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-326">On the **Configurations** page, in the configuration tree in the left pane, expand **Invoice model**, and select **Invoice model (Litware)**.</span></span>
3. <span data-ttu-id="6b4b8-327">在 **版本** 快速选项卡上，选择 **更改状态** \> **完成**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-327">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="6b4b8-328">版本 50.1 的状态将从 **草稿** 更改为 **已完成**，并且该版本变为只读。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-328">The status of version 50.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="6b4b8-329">添加了一个新的可编辑版本 50.2，其状态为 **草稿**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-329">A new editable version, 50.2, is added and has a status of **Draft**.</span></span> <span data-ttu-id="6b4b8-330">您可以使用此版本在自定义 ER 数据模型配置中进行进一步更改。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-330">You can use this version to make further changes in your custom ER data model configuration.</span></span>

![在“配置”页面上完成的版本 50.1](./media/er-quick-start3-completed-custom-model1.png)

### <a name="customize-the-model-mapping-configuration"></a><span data-ttu-id="6b4b8-332">自定义模型映射配置</span><span class="sxs-lookup"><span data-stu-id="6b4b8-332">Customize the model mapping configuration</span></span>

<span data-ttu-id="6b4b8-333">作为电子报告开发人员角色的用户，您可以设计自定义 ER 模型映射。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-333">As a user in the Electronic Reporting Developer role, you can design your custom ER model mapping.</span></span>

#### <a name="add-a-custom-model-mapping-configuration"></a><span data-ttu-id="6b4b8-334">添加自定义模型映射配置</span><span class="sxs-lookup"><span data-stu-id="6b4b8-334">Add a custom model mapping configuration</span></span>

1. <span data-ttu-id="6b4b8-335">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-335">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6b4b8-336">在 **配置** 页面上，在左侧窗格的配置树中，展开 **客户发票模型**，然后选择 **客户发票模型映射**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-336">On the **Configurations** page, in the configuration tree in the left pane, expand **Customer invoice model**, and select **Customer invoice model mapping**.</span></span>
3. <span data-ttu-id="6b4b8-337">在操作窗格中选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-337">On the Action Pane, select **Create configuration**.</span></span>
4. <span data-ttu-id="6b4b8-338">在下拉对话框的 **新建** 字段中，选择 **从名称派生：客户发票模型映射，Microsoft** 以表示您的新自定义 ER 模型映射配置应基于 ER 模型映射配置。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-338">In the drop-down dialog box, in the **New** field, select **Derive from Name: Customer invoice model mapping, Microsoft** to indicate that your new custom ER model mapping configuration should be based on the ER model mapping configuration.</span></span>
5. <span data-ttu-id="6b4b8-339">在 **名称** 字段中，输入 **发票模型映射 (Litware)**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-339">In the **Name** field, enter **Invoice model mapping (Litware)**.</span></span>
6. <span data-ttu-id="6b4b8-340">在 **目标模型** 字段中，选择 **发票模型 (Litware)**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-340">In the **Target model** field, select **Invoice model (Litware)**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="6b4b8-341">此步骤非常重要。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-341">This step is very important.</span></span> <span data-ttu-id="6b4b8-342">如果忽略该步骤，将无法在配置的模型映射中使用自定义数据模型。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-342">If you omit it, you won't be able to use your custom data model in the configured model mapping.</span></span>

7. <span data-ttu-id="6b4b8-343">选择 **创建配置** 以添加新 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-343">Select **Create configuration** to add the new ER configuration.</span></span>

![在“配置”页面上添加自定义模型映射配置](./media/er-quick-start3-adding-custom-mapping.png)

#### <a name="configure-a-custom-model-mapping"></a><span data-ttu-id="6b4b8-345">配置自定义模型映射</span><span class="sxs-lookup"><span data-stu-id="6b4b8-345">Configure a custom model mapping</span></span>

<span data-ttu-id="6b4b8-346">您必须修改自定义模型映射并指定应该如何在运行时使用应用程序数据填充自定义数据模型的自定义 **FederalTaxID\_Litware** 字段。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-346">You must modify your custom model mapping and specify how the custom **FederalTaxID\_Litware** field of the custom data model should be filled in with application data at runtime.</span></span>

1. <span data-ttu-id="6b4b8-347">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-347">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6b4b8-348">在 **配置** 页面上，在左侧窗格的配置树中，展开 **客户发票模型** \> **客户发票模型映射**，然后选择 **发票模型映射 (Litware)**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-348">On the **Configurations** page, in the configuration tree in the left pane, expand **Customer invoice model** \> **Customer invoice model mapping**, and select **Invoice model mapping (Litware)**.</span></span>
3. <span data-ttu-id="6b4b8-349">在操作窗格上，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-349">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="6b4b8-350">在 **模型到数据源映射** 页面上，选择 **客户发票** 映射。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-350">On the **Model to datasource mapping** page, select the **Customer invoice** mapping.</span></span>

    ![模型到数据源映射页面](./media/er-quick-start3-select-customer-mapping.png)

5. <span data-ttu-id="6b4b8-352">选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-352">Select **Designer**.</span></span>
6. <span data-ttu-id="6b4b8-353">在 **模型映射设计器** 页面上，在 **数据源** 窗格中，展开表示 **CustInvoiceJour** 应用程序表的 **CustInvoiceJour** 数据源。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-353">On the **Model mapping designer** page, in the **Data sources** pane, expand the **CustInvoiceJour** data source that represents the **CustInvoiceJour** application table.</span></span>
7. <span data-ttu-id="6b4b8-354">在 **CustInvoiceJour** 下，展开 **关系** 以查看 **CustInvoiceJour** 表的多对一 (N:1) 类型的关系列表。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-354">Under **CustInvoiceJour**, expand **Relations** to review the list of relations of the many-to-one (N:1) type for the **CustInvoiceJour** table.</span></span>
8. <span data-ttu-id="6b4b8-355">在 **CustInvoiceJour** \> **关系** 下，展开 **客户 (CustTable)** 以访问 **客户 (CustTable)** 表的字段和关系。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-355">Under **CustInvoiceJour** \> **Relations**, expand **Customers (CustTable)** to access the fields and relations of the **Customers (CustTable)** table.</span></span>
9. <span data-ttu-id="6b4b8-356">选择 [之前](#insert_custom_field)实现的 **FederalTaxID\_Custom** 数据源字段。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-356">Select the **FederalTaxID\_Custom** data source field that you implemented [earlier](#insert_custom_field).</span></span>
10. <span data-ttu-id="6b4b8-357">在 **数据模型** 窗格中，展开 **客户信息（客户）**，然后选择 **FederalTaxID\_Litware** 数据模型字段。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-357">In the **Data model** pane, expand **Customer information (Customer)**, and select the **FederalTaxID\_Litware** data model field.</span></span>
11. <span data-ttu-id="6b4b8-358">选择 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-358">Select **Bind**.</span></span>

    ![模型映射设计器页面](./media/er-quick-start3-customize-model-mapping.gif)

12. <span data-ttu-id="6b4b8-360">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-360">Select **Save**.</span></span>
13. <span data-ttu-id="6b4b8-361">关闭 **模型映射设计器** 页。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-361">Close the **Model mapping designer** page.</span></span>
14. <span data-ttu-id="6b4b8-362">关闭 **模型到数据源映射** 页。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-362">Close the **Model to datasource mapping** page.</span></span>

#### <a name="complete-a-custom-model-mapping-configuration"></a><span data-ttu-id="6b4b8-363">完成自定义模型映射配置</span><span class="sxs-lookup"><span data-stu-id="6b4b8-363">Complete a custom model mapping configuration</span></span>

<span data-ttu-id="6b4b8-364">您必须[完成](general-electronic-reporting.md#component-versioning)自定义 ER 模型映射配置的版本 50.19.1 的工作以使其可供使用。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-364">You must [complete](general-electronic-reporting.md#component-versioning) your work with version 50.19.1 of your custom ER model mapping configuration to make it available for use.</span></span>

1. <span data-ttu-id="6b4b8-365">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-365">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6b4b8-366">在 **配置** 页面上，在左侧窗格的配置树中，展开 **客户发票模型** \> **客户发票模型映射**，然后选择 **发票模型映射 (Litware)**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-366">On the **Configurations** page, in the configuration tree in the left pane, expand **Customer invoice model** \> **Customer invoice model mapping**, and select **Invoice model mapping (Litware)**.</span></span>
3. <span data-ttu-id="6b4b8-367">在 **版本** 快速选项卡上，选择 **更改状态** \> **完成**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-367">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="6b4b8-368">版本 50.19.1 的状态将从 **草稿** 更改为 **已完成**，并且该版本变为只读。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-368">The status of version 50.19.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="6b4b8-369">添加了一个新的可编辑版本 50.19.2，其状态为 **草稿**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-369">A new editable version, 50.19.2, is added and has a status of **Draft**.</span></span> <span data-ttu-id="6b4b8-370">您可以使用此版本在自定义 ER 模型映射配置中进行进一步更改。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-370">You can use this version to make further changes in your custom ER model mapping configuration.</span></span>

![在“配置”页面上完成的版本 50.19.1](./media/er-quick-start3-completed-custom-mapping1.png)

> [!NOTE]
> <span data-ttu-id="6b4b8-372">支持的配置[生命周期](general-electronic-reporting-manage-configuration-lifecycle.md)不包含数据库更改的生命周期。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-372">The supported configuration [lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md) doesn't cover the lifecycle of database changes.</span></span> <span data-ttu-id="6b4b8-373">如果您从当前 Finance 实例中导出 **发票模型映射 (Litware)** 配置的版本 50.19.1，并尝试将其导入在 **CustTable** 表中不包含自定义 **FederalTaxID\_Custom** 字段的另一个实例，将发生异常。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-373">If you export version 50.19.1 of the **Invoice model mapping (Litware)** configuration from the current Finance instance and try to import it into another instance that doesn't contain the custom **FederalTaxID\_Custom** field in the **CustTable** table, an exception will occur.</span></span> <span data-ttu-id="6b4b8-374">该异常指出导入的 ER 配置与目标 Finance 实例的元数据不兼容。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-374">The exception will state that the imported ER configuration isn't compatible with the metadata of the target Finance instance.</span></span>

### <a name="customize-the-format-configuration"></a><span data-ttu-id="6b4b8-375">自定义格式配置</span><span class="sxs-lookup"><span data-stu-id="6b4b8-375">Customize the format configuration</span></span>

<span data-ttu-id="6b4b8-376">作为电子报告功能顾问角色的用户，您可以设计自定义 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-376">As a user in the Electronic Reporting Functional Consultant role, you can design your custom ER format.</span></span>

#### <a name="add-a-custom-format-configuration"></a><span data-ttu-id="6b4b8-377">添加自定义格式配置</span><span class="sxs-lookup"><span data-stu-id="6b4b8-377">Add a custom format configuration</span></span>

1. <span data-ttu-id="6b4b8-378">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-378">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6b4b8-379">在 **配置** 页面上，在左侧窗格的配置树中，展开 **客户发票模型** \> **UBL 销售发票**，然后选择 **Peppol 销售发票**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-379">On the **Configurations** page, in the configuration tree in the left pane, expand **Customer invoice model** \> **UBL Sales invoice**, and select **Peppol Sales Invoice**.</span></span>
3. <span data-ttu-id="6b4b8-380">在操作窗格中选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-380">On the Action Pane, select **Create configuration**.</span></span>
4. <span data-ttu-id="6b4b8-381">在下拉对话框的 **新建** 字段中，选择 **从名称派生：Peppol 销售发票，Microsoft** 以表示您的自定义 ER 格式配置应基于 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-381">In the drop-down dialog box, in the **New** field, select **Derive from Name: Peppol Sales Invoice, Microsoft** to indicate that your custom ER format configuration should be based on the ER format configuration.</span></span>
5. <span data-ttu-id="6b4b8-382">在 **名称** 字段中，输入 **Peppol 销售发票 (Litware)**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-382">In the **Name** field, enter **Peppol Sales Invoice (Litware)**.</span></span>
6. <span data-ttu-id="6b4b8-383">在 **数据模型** 字段中，选择 **发票模型 (Litware)** 以使用自定义数据模型和模型映射组件。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-383">In the **Data model** field, select **Invoice model (Litware)** to use your custom data model and model mapping components.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6b4b8-384">此步骤非常重要。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-384">This step is very important.</span></span> <span data-ttu-id="6b4b8-385">如果忽略该步骤，将无法在配置的格式中使用自定义数据模型。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-385">If you omit it, you won't be able to use your custom data model in the configured format.</span></span>

7. <span data-ttu-id="6b4b8-386">在 **数据模型** 字段中，选择 **InvoiceCustomer** 根定义。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-386">In the **Data model** field, select the **InvoiceCustomer** root definition.</span></span>
8. <span data-ttu-id="6b4b8-387">选择 **创建配置** 以添加新 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-387">Select **Create configuration** to add the new ER configuration.</span></span>

![在“配置”页面上添加自定义格式配置](./media/er-quick-start3-adding-custom-format.png)

<span data-ttu-id="6b4b8-389">现在，您可以使用 ER Operations 设计器在 **草稿**[状态](general-electronic-reporting.md#component-versioning)下编辑 **Peppol 销售发票 (Litware)** ER 配置的版本 11.2.2.1。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-389">You can now use the ER Operations designer to edit version 11.2.2.1 of the **Peppol Sales Invoice (Litware)** ER configuration in **Draft** [status](general-electronic-reporting.md#component-versioning).</span></span>

![“配置”页面上的 ER 配置的版本 11.2.2.1](./media/er-quick-start3-added-custom-format.png)

#### <a name="configure-a-custom-format"></a><span data-ttu-id="6b4b8-391">配置自定义格式</span><span class="sxs-lookup"><span data-stu-id="6b4b8-391">Configure a custom format</span></span>

<span data-ttu-id="6b4b8-392">您必须通过添加新格式元素以填写已开票客户的联邦纳税标识代码的值来修改自定义格式。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-392">You must modify your custom format by adding a new format element to fill in the value of an invoiced customer's federal tax identification code.</span></span>

1. <span data-ttu-id="6b4b8-393">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-393">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6b4b8-394">在 **配置** 页面上，在左侧窗格的配置树中，展开 **客户发票模型** \> **UBL 销售发票** \> **Peppol 销售发票**，然后选择 **Peppol 销售发票 (Litware)**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-394">On the **Configurations** page, in the configuration tree in the left pane, expand **Customer invoice model** \> **UBL Sales invoice** \> **Peppol Sales Invoice**, and select **Peppol Sales Invoice (Litware)**.</span></span>
3. <span data-ttu-id="6b4b8-395">在操作窗格上，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-395">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="6b4b8-396">在格式树中，展开 **XMLHeader** \> **发票** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme**，然后选择 **cbc:ID**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-396">In the format tree, expand **XMLHeader** \> **Invoice** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme**, and select **cbc:ID**.</span></span>
5. <span data-ttu-id="6b4b8-397">选择 **添加**，然后选择 **XML** \> **属性**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-397">Select **Add**, and then select **XML** \> **Attribute**.</span></span>
6. <span data-ttu-id="6b4b8-398">在 **组件属性** 对话框的 **名称** 字段中，输入 **FederalTaxID**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-398">In the **Component property** dialog box, in the **Name** field, enter **FederalTaxID**.</span></span>
7. <span data-ttu-id="6b4b8-399">选择 **确定** 以添加新的格式元素，从而在生成的 XML 文件中创建新的 **FederalTaxID** XML 属性。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-399">Select **OK** to add a new format element to create a new **FederalTaxID** XML attribute in a generated XML file.</span></span>
8. <span data-ttu-id="6b4b8-400">在格式树中，在 **XMLHeader** \> **发票** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** \> **cbc:ID** 下，选择 **FederalTaxID**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-400">In the format tree, under **XMLHeader** \> **Invoice** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** \> **cbc:ID**, select **FederalTaxID**.</span></span>
9. <span data-ttu-id="6b4b8-401">选择 **上移**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-401">Select **Move up**.</span></span>

![格式设计器页面上的新格式元素](./media/er-quick-start3-customized-format.png)

#### <a name="configure-a-custom-format-mapping"></a><span data-ttu-id="6b4b8-403">配置自定义格式映射</span><span class="sxs-lookup"><span data-stu-id="6b4b8-403">Configure a custom format mapping</span></span>

1. <span data-ttu-id="6b4b8-404">在 **格式设计器** 页面的 **映射** 选项卡上，展开 **模型** 类型的 **发票** 数据源。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-404">On the **Format designer** page, on the **Mapping** tab, expand the **Invoice** data source of the **Model** type.</span></span>
2. <span data-ttu-id="6b4b8-405">在 **发票** 下，展开 **客户信息（客户）**，然后选择 **FederalTaxID\_Litware**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-405">Under **Invoice**, expand **Customer information (Customer)**, and select **FederalTaxID\_Litware**.</span></span>
3. <span data-ttu-id="6b4b8-406">选择 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-406">Select **Bind**.</span></span>

    ![“格式设计器”页面](./media/er-quick-start3-customized-format-mapping.png)

4. <span data-ttu-id="6b4b8-408">选择 **模型** 类型的 **发票** 数据源，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-408">Select the **Invoice** data source of the **Model** type, and then select **Edit**.</span></span>
5. <span data-ttu-id="6b4b8-409">在 **版本** 字段中，选择自定义数据模型的版本 **1**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-409">In the **Version** field, select version **1** of your custom data model, and then select **OK**.</span></span>
6. <span data-ttu-id="6b4b8-410">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-410">Select **Save**.</span></span>
7. <span data-ttu-id="6b4b8-411">关闭 **格式设计器** 页。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-411">Close the **Format designer** page.</span></span>

#### <a name="complete-a-custom-format-configuration"></a><span data-ttu-id="6b4b8-412">完成自定义格式配置</span><span class="sxs-lookup"><span data-stu-id="6b4b8-412">Complete a custom format configuration</span></span>

<span data-ttu-id="6b4b8-413">您必须[完成](general-electronic-reporting.md#component-versioning)自定义 ER 格式配置的版本 11.2.2.1 的工作以使其可供使用。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-413">You must [complete](general-electronic-reporting.md#component-versioning) your work with version 11.2.2.1 of your custom ER format configuration to make it available for use.</span></span>

1. <span data-ttu-id="6b4b8-414">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-414">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6b4b8-415">在 **配置** 页面上，在左侧窗格的配置树中，展开 **客户发票模型** \> **UBL 销售发票** \> **Peppol 销售发票**，然后选择 **Peppol 销售发票 (Litware)**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-415">On the **Configurations** page, in the configuration tree in the left pane, expand **Customer invoice model** \> **UBL Sales invoice** \> **Peppol Sales Invoice**, and select **Peppol Sales Invoice (Litware)**.</span></span>
3. <span data-ttu-id="6b4b8-416">在 **版本** 快速选项卡上，选择 **更改状态** \> **完成**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-416">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="6b4b8-417">版本 11.2.2.1 的状态将从 **草稿** 更改为 **已完成**，并且该版本变为只读。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-417">The status of version 11.2.2.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="6b4b8-418">添加了一个新的可编辑版本 11.2.2.2，其状态为 **草稿**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-418">A new editable version, 11.2.2.2, is added and has a status of **Draft**.</span></span> <span data-ttu-id="6b4b8-419">您可以使用此版本在自定义 ER 格式配置中进行进一步更改。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-419">You can use this version to make further changes in your custom ER format configuration.</span></span>

![在“配置”页面上完成的版本 11.2.2.1](./media/er-quick-start3-completed-custom-format1.png)

## <a name="configure-the-accounts-receivable-parameters-to-start-to-use-custom-er-configurations"></a><a name="ConfigureAR2"></a><span data-ttu-id="6b4b8-421">配置应收帐款参数以开始使用自定义 ER 配置</span><span class="sxs-lookup"><span data-stu-id="6b4b8-421">Configure the Accounts receivable parameters to start to use custom ER configurations</span></span>

1. <span data-ttu-id="6b4b8-422">转到 **应收帐款** \> **设置** \> **应收帐款参数**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-422">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="6b4b8-423">在 **电子单据** 选项卡上，在 **电子报告** 快速选项卡上，在 **销售和普通发票** 字段中，选择 **Peppol 销售发票 (Litware)**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-423">On the **Electronic documents** tab, on the **Electronic reporting** FastTab, in the **Sales and Free text invoice** field, select **Peppol Sales Invoice (Litware)**.</span></span>
3. <span data-ttu-id="6b4b8-424">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-424">Select **Save**.</span></span>

![应收帐款参数页面、电子单据选项卡、电子报告快速选项卡](./media/er-quick-start3-configure-ar2.png)

## <a name="update-a-customer-record-by-adding-a-federal-tax-identification-code"></a><a name="ConfigureCustomer2"></a><span data-ttu-id="6b4b8-426">通过添加联邦纳税标识代码来更新客户记录</span><span class="sxs-lookup"><span data-stu-id="6b4b8-426">Update a customer record by adding a federal tax identification code</span></span>

1. <span data-ttu-id="6b4b8-427">转到 **应收帐款** \> **客户** \> **所有客户**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-427">Go to **Accounts receivable** \> **Customers** \> **All customers**.</span></span>
2. <span data-ttu-id="6b4b8-428">在 **所有客户** 页面上，选择 **DE-014** 客户帐户链接。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-428">On the **All customers** page, select the **DE-014** customer account link.</span></span>
3. <span data-ttu-id="6b4b8-429">在 **常规** 快速选项卡上，在 **税号标识** 字段中，输入 **LITWARE-6789**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-429">On the **General** FastTab, in the **Federal Tax ID** field, enter **LITWARE-6789**.</span></span>
4. <span data-ttu-id="6b4b8-430">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-430">Select **Save**.</span></span>

    ![DE-014 客户详细信息页面](./media/er-quick-start3-added-tax-id-value.png)

5. <span data-ttu-id="6b4b8-432">关闭 **所有客户** 页面。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-432">Close the **All customers** page.</span></span>

## <a name="process-a-customer-invoice-by-using-custom-er-configurations"></a><a name="ProcessInvoice2"></a><span data-ttu-id="6b4b8-433">使用自定义 ER 配置处理客户发票</span><span class="sxs-lookup"><span data-stu-id="6b4b8-433">Process a customer invoice by using custom ER configurations</span></span>

### <a name="select-and-send-a-posted-invoice"></a><span data-ttu-id="6b4b8-434">选择并发送已过帐发票</span><span class="sxs-lookup"><span data-stu-id="6b4b8-434">Select and send a posted invoice</span></span>

1. <span data-ttu-id="6b4b8-435">转至 **应收帐款** \> **发票** \> **所有普通发票**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-435">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="6b4b8-436">在 **普通发票** 页面上，选择您之前添加和过帐的发票。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-436">On the **Free text invoice** page, select the invoice that you previously added and posted.</span></span>
3. <span data-ttu-id="6b4b8-437">在“操作”窗格上，在 **单据** 组中，选择 **发送** \> **原始**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-437">On the Action Pane, in the **Document** group, select **Send** \> **Original**.</span></span>
4. <span data-ttu-id="6b4b8-438">关闭 **普通发票** 页面。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-438">Close the **Free text invoice** page.</span></span>

### <a name="analyze-a-generated-e-invoice"></a><span data-ttu-id="6b4b8-439">分析生成的电子发票</span><span class="sxs-lookup"><span data-stu-id="6b4b8-439">Analyze a generated e-invoice</span></span>

1. <span data-ttu-id="6b4b8-440">转到 **组织管理** \> **电子报告** \> **电子报告作业**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-440">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>
2. <span data-ttu-id="6b4b8-441">在 **电子报告作业** 页面上，选择具有任务描述 **发送电子发票 XML** 的最新记录。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-441">On the **Electronic reporting jobs** page, select the latest record that has the task description **Send the eInvoice XML**.</span></span>
3. <span data-ttu-id="6b4b8-442">选择 **显示文件** 以访问生成的文件列表。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-442">Select **Show files** to access the list of generated files.</span></span>
4. <span data-ttu-id="6b4b8-443">选择 **打开** 以下载生成的电子发票 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-443">Select **Open** to download the e-invoice XML file that is generated.</span></span>
5. <span data-ttu-id="6b4b8-444">分析电子发票 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-444">Analyze the e-invoice XML file.</span></span> <span data-ttu-id="6b4b8-445">请注意，根据您的自定义，除了 **schemeID** 和 **schemeAgencyID** XML 属性，客户税架构还包括自定义 **FederalTaxID** XML 属性。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-445">Notice that, in accordance with your customization, the customer tax schema includes the custom **FederalTaxID** XML attribute in addition to the **schemeID** and **schemeAgencyID** XML attributes.</span></span> <span data-ttu-id="6b4b8-446">此新 XML 属性的值由为已开票客户输入的 **LITWARE-6789** 税号标识指定。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-446">The value of this new XML attribute is specified by the **LITWARE-6789** federal tax ID that was entered for an invoiced customer.</span></span>

    ![具有您的自定义的已生成电子发票 XML 文件预览](./media/er-quick-start3-e-invoice2.png)

## <a name="import-the-latest-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations2"></a><span data-ttu-id="6b4b8-448">导入标准 ER 配置的最新版本</span><span class="sxs-lookup"><span data-stu-id="6b4b8-448">Import the latest versions of standard ER configurations</span></span>

<span data-ttu-id="6b4b8-449">若要使一组标准 ER 配置在 Finance 实例中保持[最新](general-electronic-reporting-manage-configuration-lifecycle.md)，只要它们在为该实例配置的 ER [存储库](general-electronic-reporting.md#Repository)中可用，就必须导入它们的新版本。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-449">To keep the set of standard ER configurations in your Finance instance [up to date](general-electronic-reporting-manage-configuration-lifecycle.md), you must import new versions of them whenever they become available in the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="6b4b8-450">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-450">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6b4b8-451">在 **本地化配置** 页面的 **配置提供程序** 部分中，选择 **Microsoft** 磁贴，然后选择 **存储库** 查看 Microsoft 提供程序的存储库列表。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-451">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="6b4b8-452">在 **配置存储库** 页，选择 **全球** 类型的存储库，然后选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-452">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="6b4b8-453">如果提示您进行授权以连接到 Regulatory Configuration Service，请按照授权说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-453">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="6b4b8-454">在 **配置存储库** 页面上，在左侧窗格的配置树中，选择 **Peppol 销售发票** 格式配置。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-454">On the **Configuration repository** page, in the configuration tree in the left pane, select the **Peppol Sales Invoice** format configuration.</span></span>
5. <span data-ttu-id="6b4b8-455">在 **版本** 快速选项卡上，选择所选 ER 格式配置的版本 **32.6.7**，该版本已发布以支持 PEPPOL BIS 3 格式的客户电子发票。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-455">On the **Versions** FastTab, select version **32.6.7** of the selected ER format configuration that has been released to support customer electronic invoices in PEPPOL BIS 3 format.</span></span> <span data-ttu-id="6b4b8-456">有关详细信息，请参阅 [KB4490320](https://support.microsoft.com/help/4490320/an-update-for-european-union-to-support-export-of-customers-electronic)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-456">For more information, see [KB4490320](https://support.microsoft.com/help/4490320/an-update-for-european-union-to-support-export-of-customers-electronic).</span></span>
6. <span data-ttu-id="6b4b8-457">选择 **导入** 将所选版本从全局存储库下载到当前 Finance 实例。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-457">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![在配置存储库页面上选择的版本 32.6.7](./media/er-quick-start3-import-solution2.png)

<span data-ttu-id="6b4b8-459">有关如何自动执行此过程的信息，请参阅[导入 ER 配置的更新版本](er-download-updated-versions-global-repo.md)。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-459">For information about how this process can be automated, see [Import updated versions of ER configurations](er-download-updated-versions-global-repo.md).</span></span>

### <a name="review-the-imported-er-configurations"></a><span data-ttu-id="6b4b8-460">查看导入的 ER 配置</span><span class="sxs-lookup"><span data-stu-id="6b4b8-460">Review the imported ER configurations</span></span>

1. <span data-ttu-id="6b4b8-461">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-461">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6b4b8-462">在 **本地化配置** 页面的 **配置** 部分中，选择 **报告配置** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-462">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="6b4b8-463">展开 **配置组件** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-463">Expand the **Configuration components** FastTab.</span></span>
4. <span data-ttu-id="6b4b8-464">在左侧窗格的配置树中，展开 **发票模型**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-464">In the configuration tree in the left pane, expand **Invoice model**.</span></span> <span data-ttu-id="6b4b8-465">请注意，在导入的 ER 数据模型配置之一中，**客户发票模型** 的名称已更改为 **发票模型**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-465">Notice that the name of **Customer invoice model** has been changed to **Invoice model** in one of the imported ER data model configurations.</span></span>
5. <span data-ttu-id="6b4b8-466">在左侧窗格的配置树中，展开 **发票模型映射**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-466">In the configuration tree in the left pane, expand **Invoice model mapping**.</span></span> <span data-ttu-id="6b4b8-467">请注意，在导入的 ER 模型映射配置之一中，**客户发票模型映射** 的名称已更改为 **发票模型映射**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-467">Notice that the name of **Customer invoice model mapping** has been changed to **Invoice model mapping** in one of the imported ER model mapping configurations.</span></span>
6. <span data-ttu-id="6b4b8-468">展开 **UBL 销售发票** \> **Peppol 销售发票**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-468">Expand **UBL Sales invoice** \> **Peppol Sales Invoice**.</span></span>

<span data-ttu-id="6b4b8-469">请注意，除了所选的 **Peppol 销售发票** ER 格式，还导入了其他必需的 ER 配置的最新版本。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-469">Notice that, in addition to the selected **Peppol Sales Invoice** ER format, the latest versions of other required ER configurations were imported.</span></span> <span data-ttu-id="6b4b8-470">因为将向全局存储库和 LCS 不断发布 ER 配置的新版本以使相应的 ER 解决方案符合新要求，因此导入了所需的数据模型配置及其模型映射配置的最新版本。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-470">Because new versions of ER configurations are constantly published to the Global repository and LCS to keep the corresponding ER solutions compliant with new requirements, the latest versions of the required data model configuration and its model mapping configurations were imported.</span></span>

<span data-ttu-id="6b4b8-471">请确保最终配置树中有以下 ER 配置：</span><span class="sxs-lookup"><span data-stu-id="6b4b8-471">Make sure that the following ER configurations are eventually available in the configuration tree:</span></span>

- <span data-ttu-id="6b4b8-472">**发票模型** ER 数据模型配置：</span><span class="sxs-lookup"><span data-stu-id="6b4b8-472">**Invoice model** ER data model configuration:</span></span>

    - <span data-ttu-id="6b4b8-473">版本 206（或更高版本）包含数据模型 ER 组件的版本 24（或更高版本），用于表示开票业务域的数据结构。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-473">Version 206 (or later) contains version 24 (or later) of the data model ER component that represents the data structure of the invoicing business domain.</span></span> <span data-ttu-id="6b4b8-474">此 ER 配置已导入，作为可用的最新 **发票模型映射** ER 模型映射配置的上级。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-474">This ER configuration has been imported as an ancestor of the latest available **Invoice model mapping** ER model mapping configuration.</span></span>

    ![“配置”页面上的版本 206](./media/er-quick-start3-imported-solution2b1.png)

- <span data-ttu-id="6b4b8-476">**发票模型映射** ER 模型映射配置：</span><span class="sxs-lookup"><span data-stu-id="6b4b8-476">**Invoice model mapping** ER model mapping configuration:</span></span>

    - <span data-ttu-id="6b4b8-477">版本 206.132（或更高版本）已导入，作为 **发票模型** ER 数据模型配置的版本 206 的最新实现。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-477">Version 206.132 (or later) has been imported as the latest implementation of version 206 of the **Invoice model** ER data model configuration.</span></span> <span data-ttu-id="6b4b8-478">它包含若干模型映射 ER 组件，用于描述在运行时如何使用应用程序数据填充数据模型。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-478">It contains several model mapping ER components that describe how the data model is filled in with application data at runtime.</span></span>

    ![“配置”页面上的版本 206.132](./media/er-quick-start3-imported-solution2b2.png)

- <span data-ttu-id="6b4b8-480">**UBL 销售发票** ER 格式配置：</span><span class="sxs-lookup"><span data-stu-id="6b4b8-480">**UBL Sales invoice** ER format configuration:</span></span>

    - <span data-ttu-id="6b4b8-481">版本 32.6 包含格式和格式映射 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-481">Version 32.6 contains the format and format mapping ER components.</span></span> <span data-ttu-id="6b4b8-482">格式组件指定报表布局。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-482">The format component specifies the report layout.</span></span> <span data-ttu-id="6b4b8-483">格式映射组件包含模型数据源，并指定如何在运行时使用此数据源填充报告布局。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-483">The format mapping component contains the model data source and specifies how this data source is used to fill in the report layout at runtime.</span></span> <span data-ttu-id="6b4b8-484">该 ER 格式配置为生成 UBL 格式的电子发票。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-484">This ER format was configured to generate e-invoices in UBL format.</span></span> <span data-ttu-id="6b4b8-485">它已导入，作为选择导入的 **Peppol 销售发票** ER 格式的父级。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-485">It has been imported as a parent of the **Peppol Sales Invoice** ER format that was selected for import.</span></span>

- <span data-ttu-id="6b4b8-486">**Peppol 销售发票** ER 格式配置：</span><span class="sxs-lookup"><span data-stu-id="6b4b8-486">**Peppol Sales Invoice** ER format configuration:</span></span>

    - <span data-ttu-id="6b4b8-487">版本 32.6.7 包含格式和格式映射 ER 组件，它们配置为生成 PEPPOL 格式的电子发票。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-487">Version 32.6.7 contains the format and format mapping ER components that were configured to generate e-invoices in PEPPOL format.</span></span>

    ![“配置”页面上的版本 32.6.7](./media/er-quick-start3-imported-solution2b3.png)

## <a name="adopt-the-changes-to-the-new-standard-er-configurations-in-your-custom-er-configurations"></a><a name="RebaseCustomERConfigurations"></a><span data-ttu-id="6b4b8-489">在您的自定义 ER 配置中采用对新标准 ER 配置所做的更改</span><span class="sxs-lookup"><span data-stu-id="6b4b8-489">Adopt the changes to the new standard ER configurations in your custom ER configurations</span></span>

### <a name="adopt-your-custom-er-data-model"></a><span data-ttu-id="6b4b8-490">采用您的自定义 ER 数据模型</span><span class="sxs-lookup"><span data-stu-id="6b4b8-490">Adopt your custom ER data model</span></span>

1. <span data-ttu-id="6b4b8-491">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-491">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6b4b8-492">在 **配置** 页面上，在左侧窗格的配置树中，展开 **发票模型**，然后选择 **发票模型 (Litware)**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-492">On the **Configurations** page, in the configuration tree in the left pane, expand **Invoice model**, and select **Invoice model (Litware)**.</span></span>
3. <span data-ttu-id="6b4b8-493">在 **版本** 快速选项卡上，对于所选数据模型配置的草稿版本 **50.2**，选择 **重定基本版本**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-493">On the **Versions** FastTab, for draft version **50.2** of the selected data model configuration, select **Rebase**.</span></span>
4. <span data-ttu-id="6b4b8-494">在 **目标版本** 字段中，确认基本 ER 数据模型配置的版本 **206** 的选择，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-494">In the **Target version** field, confirm the selection of version **206** of the base ER data model configuration, and then select **OK**.</span></span>

    <span data-ttu-id="6b4b8-495">自定义 ER 数据模型配置的草稿版本从 **50.2** 重新编号为 **206.2**，以表示它现在包含您的自定义，该自定义已与基本 ER 数据模型配置的最新版本 (206) 中的更改合并。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-495">The draft version of your custom ER data model configuration is renumbered from **50.2** to **206.2** to indicate that it now contains your customization that was merged with the changes in the latest version (206) of the base ER data model configuration.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6b4b8-496">重定操作可逆。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-496">The rebase action is reversible.</span></span> <span data-ttu-id="6b4b8-497">若要取消此重定基本版本，请在 **版本** 快速选项卡上选择 **发票模型 (Litware)** 模型的版本 **50.1**，然后选择 **获取此版本**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-497">To cancel this rebase, select version **50.1** of the **Invoice model (Litware)** model on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="6b4b8-498">将版本 206.2 重新编号回 **50.2**，草稿版本 50.2 的内容将与版本 50.1 的内容匹配。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-498">Version 206.2 will be renumbered back to **50.2**, and the content of draft version 50.2 will match the content of version 50.1.</span></span>

5. <span data-ttu-id="6b4b8-499">在 **版本** 快速选项卡上，选择 **更改状态** \> **完成**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-499">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="6b4b8-500">版本 206.2 的状态将从 **草稿** 更改为 **已完成**，并且该版本变为只读。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-500">The status of version 206.2 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="6b4b8-501">添加了一个新的可编辑版本 206.3，其状态为 **草稿**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-501">A new editable version, 206.3, is added and has a status of **Draft**.</span></span> <span data-ttu-id="6b4b8-502">您可以使用此版本在自定义 ER 数据模型配置中进行进一步更改。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-502">You can use this version to make further changes in your custom ER data model configuration.</span></span>

![在“配置”页面上完成的版本 206.2](./media/er-quick-start3-completed-custom-model2.png)

### <a name="adopt-your-custom-er-model-mapping"></a><span data-ttu-id="6b4b8-504">采用您的自定义 ER 模型映射</span><span class="sxs-lookup"><span data-stu-id="6b4b8-504">Adopt your custom ER model mapping</span></span>

1. <span data-ttu-id="6b4b8-505">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-505">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6b4b8-506">在 **配置** 页面上，在左侧窗格的配置树中，展开 **发票模型** \> **发票模型映射**，然后选择 **发票模型映射 (Litware)**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-506">On the **Configurations** page, in the configuration tree in the left pane, expand **Invoice model** \> **Invoice model mapping**, and select **Invoice model mapping (Litware)**.</span></span>
3. <span data-ttu-id="6b4b8-507">在 **版本** 快速选项卡上，对于所选模型映射配置的草稿版本 **50.19.2**，选择 **重定基本版本**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-507">On the **Versions** FastTab, for draft version **50.19.2** of the selected model mapping configuration, select **Rebase**.</span></span>
4. <span data-ttu-id="6b4b8-508">在 **目标版本** 字段中，确认基本 ER 模型映射配置的版本 **206.132** 的选择，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-508">In the **Target version** field, confirm the selection of version **206.132** of the base ER model mapping configuration, and then select **OK**.</span></span>

    <span data-ttu-id="6b4b8-509">自定义 ER 模型映射配置的草稿版本从 **50.19.2** 重新编号为 **206.132.2**，以表示它现在包含您的自定义，该自定义已与基本 ER 模型映射配置的最新版本 (206.132) 中的更改合并。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-509">The draft version of your custom ER model mapping configuration is renumbered from **50.19.2** to **206.132.2** to indicate that it now contains your customization that was merged with the changes in the latest version (206.132) of the base ER model mapping configuration.</span></span>

    <span data-ttu-id="6b4b8-510">请注意，发现了一些重定基本版本冲突。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-510">Notice that some rebase conflicts were discovered.</span></span> <span data-ttu-id="6b4b8-511">现在，您必须手动解决这些冲突。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-511">You must now manually resolve those conflicts.</span></span>

    ![“配置”页面上的重定基本版本冲突消息](./media/er-quick-start3-rebase-conflicts-model-mapping1.png)

5. <span data-ttu-id="6b4b8-513">在“操作”窗格上，选择 **设计器**，然后在映射列表中，选择 **客户发票**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-513">On the Action Pane, select **Designer**, and then, in the list of mappings, select **Customer Invoice**.</span></span>
6. <span data-ttu-id="6b4b8-514">对于每个重定基本版本冲突，选择 **保留自定义值**，因为您必须为提及的每个组件保留自定义数据模型的版本号。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-514">For each rebase conflict, select **Retain own value**, because you must keep the version number of your custom data model for every component that has been mentioned.</span></span>

    ![模型映射设计器页面上的重定基本版本冲突](./media/er-quick-start3-rebase-conflicts-model-mapping2.png)

7. <span data-ttu-id="6b4b8-516">选择 **保存**，然后关闭 **模型映射设计器** 页面。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-516">Select **Save**, and then close the **Model mapping designer** page.</span></span>
8. <span data-ttu-id="6b4b8-517">在映射列表中，选择 **项目发票**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-517">In the list of mappings, select **Project Invoice**.</span></span>
9. <span data-ttu-id="6b4b8-518">对于每个重定基本版本冲突，选择 **保留自定义值**，因为您必须为提及的每个组件保留自定义数据模型的版本号。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-518">For each rebase conflict, select **Retain own value**, because you must keep the version number of your custom data model for every component that has been mentioned.</span></span>
10. <span data-ttu-id="6b4b8-519">选择 **保存**，然后关闭 **模型映射** 页面。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-519">Select **Save**, and then close the **Model mappings** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6b4b8-520">重定操作可逆。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-520">The rebase action is reversible.</span></span> <span data-ttu-id="6b4b8-521">若要取消此重定基本版本，请在 **版本** 快速选项卡上选择 **发票模型映射 (Litware)** 模型映射的版本 **50.19.1**，然后选择 **获取此版本**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-521">To cancel this rebase, select version **50.19.1** of the **Invoice model mapping (Litware)** model mapping on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="6b4b8-522">将版本 206.132.2 重新编号回 **50.19.2**，草稿版本 50.19.2 的内容将与版本 50.19.1 的内容匹配。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-522">Version 206.132.2 will be renumbered back to **50.19.2**, and the content of draft version 50.19.2 will match the content of version 50.19.1.</span></span>

11. <span data-ttu-id="6b4b8-523">在 **版本** 快速选项卡上，选择 **更改状态** \> **完成**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-523">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="6b4b8-524">版本 206.132.2 的状态将从 **草稿** 更改为 **已完成**，并且该版本变为只读。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-524">The status of version 206.132.2 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="6b4b8-525">添加了一个新的可编辑版本 206.132.3，其状态为 **草稿**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-525">A new editable version, 206.132.3, is added and has a status of **Draft**.</span></span> <span data-ttu-id="6b4b8-526">您可以使用此版本在自定义 ER 模型映射配置中进行进一步更改。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-526">You can use this version to make further changes in your custom ER model mapping configuration.</span></span>

![在“配置”页面上完成的版本 206.132.2](./media/er-quick-start3-completed-custom-mapping2.png)

### <a name="adopt-your-custom-er-format"></a><span data-ttu-id="6b4b8-528">采用您的自定义 ER 格式</span><span class="sxs-lookup"><span data-stu-id="6b4b8-528">Adopt your custom ER format</span></span>

1. <span data-ttu-id="6b4b8-529">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-529">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6b4b8-530">在 **配置** 页面上，在左侧窗格的配置树中，展开 **发票模型** \> **UBL 销售发票** \> **Peppol 销售发票**，然后选择 **Peppol 销售发票 (Litware)**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-530">On the **Configurations** page, in the configuration tree in the left pane, expand **Invoice model** \> **UBL Sales invoice** \> **Peppol Sales Invoice**, and select **Peppol Sales Invoice (Litware)**.</span></span>
3. <span data-ttu-id="6b4b8-531">在 **版本** 快速选项卡上，对于所选格式配置的草稿版本 **11.2.2.2**，选择 **重定基本版本**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-531">On the **Versions** FastTab, for draft version **11.2.2.2** of the selected format configuration, select **Rebase**.</span></span>
4. <span data-ttu-id="6b4b8-532">在 **目标** 版本字段中，确认基本 ER 格式配置的版本 **32.6.7** 的选择，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-532">In the **Target** version field, confirm the selection of version **32.6.7** of the base ER format configuration, and then select **OK**.</span></span>

    <span data-ttu-id="6b4b8-533">自定义 ER 格式配置的草稿版本从 **11.2.2.2** 重新编号为 **32.6.7.2**，以表示它现在包含您的自定义，该自定义已与基本 ER 格式配置的最新版本 (32.6.7) 中的更改合并。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-533">The draft version of your custom ER format configuration is renumbered from **11.2.2.2** to **32.6.7.2** to indicate that it now contains your customization that was merged with the changes in the latest version (32.6.7) of the base ER format configuration.</span></span>

    <span data-ttu-id="6b4b8-534">请注意，发现了一些重定基本版本冲突。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-534">Notice that some rebase conflicts were discovered.</span></span> <span data-ttu-id="6b4b8-535">现在，您必须手动解决这些冲突。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-535">You must now manually resolve those conflicts.</span></span>

5. <span data-ttu-id="6b4b8-536">在操作窗格上，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-536">On the Action Pane, select **Designer**.</span></span>
6. <span data-ttu-id="6b4b8-537">对于每个重定基本版本冲突，选择 **保留自定义值**，因为您必须为提及的每个组件保留自定义数据模型的版本号。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-537">For each rebase conflict, select **Retain own value**, because you must keep the version number of your custom data model for every component that has been mentioned.</span></span>
7. <span data-ttu-id="6b4b8-538">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-538">Select **Save**.</span></span>
8. <span data-ttu-id="6b4b8-539">在 **映射** 选项卡上，选择 **模型** 类型的 **发票** 数据源，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-539">On the **Mapping** tab, select the **Invoice** data source of the **Model** type, and then select **Edit**.</span></span>
9. <span data-ttu-id="6b4b8-540">在 **版本** 字段中，选择自定义数据模型的版本 **2**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-540">In the **Version** field, select version **2** of your custom data model, and then select **OK**.</span></span>
10. <span data-ttu-id="6b4b8-541">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-541">Select **Save**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6b4b8-542">重定操作可逆。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-542">The rebase action is reversible.</span></span> <span data-ttu-id="6b4b8-543">若要取消此重定基本版本，请在 **版本** 快速选项卡上选择 **Peppol 销售发票 (Litware)** 格式的版本 **11.2.2.1**，然后选择 **获取此版本**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-543">To cancel this rebase, select version **11.2.2.1** of the **Peppol Sales Invoice (Litware)** format on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="6b4b8-544">将版本 32.6.7.2 重新编号回 **11.2.2.2**，草稿版本 11.2.2.2 的内容将与版本 11.2.2.1 的内容匹配。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-544">Version 32.6.7.2 will be renumbered back to **11.2.2.2**, and the content of draft version 11.2.2.2 will match the content of version 11.2.2.1.</span></span>

11. <span data-ttu-id="6b4b8-545">关闭 **格式设计器** 页。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-545">Close the **Format designer** page.</span></span>
12. <span data-ttu-id="6b4b8-546">在 **版本** 快速选项卡上，选择 **更改状态** \> **完成**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-546">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="6b4b8-547">版本 32.6.7.2 的状态将从 **草稿** 更改为 **已完成**，并且该版本变为只读。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-547">The status of version 32.6.7.2 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="6b4b8-548">添加了一个新的可编辑版本 32.6.7.3，其状态为 **草稿**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-548">A new editable version, 32.6.7.3, is added and has a status of **Draft**.</span></span> <span data-ttu-id="6b4b8-549">您可以使用此版本在自定义 ER 格式配置中进行进一步更改。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-549">You can use this version to make further changes in your custom ER format configuration.</span></span>

![在“配置”页面上完成的版本 32.6.7.2](./media/er-quick-start3-completed-custom-format2.png)

## <a name="process-a-customer-invoice-by-using-new-versions-of-the-custom-er-configurations"></a><a name="ProcessInvoice3"></a><span data-ttu-id="6b4b8-551">使用自定义 ER 配置的新版本处理客户发票</span><span class="sxs-lookup"><span data-stu-id="6b4b8-551">Process a customer invoice by using new versions of the custom ER configurations</span></span>

### <a name="select-and-send-a-posted-invoice"></a><span data-ttu-id="6b4b8-552">选择并发送已过帐发票</span><span class="sxs-lookup"><span data-stu-id="6b4b8-552">Select and send a posted invoice</span></span>

1. <span data-ttu-id="6b4b8-553">转至 **应收帐款** \> **发票** \> **所有普通发票**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-553">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="6b4b8-554">在 **普通发票** 页面上，选择您之前添加和过帐的发票。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-554">On the **Free text invoice** page, select the invoice that you previously added and posted.</span></span>
3. <span data-ttu-id="6b4b8-555">在“操作”窗格上，在 **单据** 组中，选择 **发送** \> **原始**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-555">On the Action Pane, in the **Document** group, select **Send** \> **Original**.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="6b4b8-556">因为您现在有两个版本的 **Peppol 销售发票 (Litware)** ER 格式配置，并且两个版本都没有[生效日期](general-electronic-reporting.md#component-date-effectivity)值，因此使用最新版本生成电子发票。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-556">Because you now have two versions of the **Peppol Sales Invoice (Litware)** ER format configuration, and neither version has an [effective date](general-electronic-reporting.md#component-date-effectivity) value, the latest version is used to generate an e-invoice.</span></span>

4. <span data-ttu-id="6b4b8-557">关闭 **普通发票** 页面。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-557">Close the **Free text invoice** page.</span></span>

### <a name="analyze-a-generated-e-invoice"></a><span data-ttu-id="6b4b8-558">分析生成的电子发票</span><span class="sxs-lookup"><span data-stu-id="6b4b8-558">Analyze a generated e-invoice</span></span>

1. <span data-ttu-id="6b4b8-559">转到 **组织管理** \> **电子报告** \> **电子报告作业**。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-559">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>
2. <span data-ttu-id="6b4b8-560">在 **电子报告作业** 页面上，选择具有任务描述 **发送电子发票 XML** 的最新记录。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-560">On the **Electronic reporting jobs** page, select the most recent record that has the task description **Send the eInvoice XML**.</span></span>
3. <span data-ttu-id="6b4b8-561">选择 **显示文件** 以访问生成的文件列表。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-561">Select **Show files** to access the list of generated files.</span></span>
4. <span data-ttu-id="6b4b8-562">选择 **打开** 以下载生成的电子发票 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-562">Select **Open** to download the e-invoice XML file that is generated.</span></span>
5. <span data-ttu-id="6b4b8-563">分析电子发票 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-563">Analyze the e-invoice XML file.</span></span> <span data-ttu-id="6b4b8-564">请注意，根据您的自定义，除了 **schemeID** 和 **schemeAgencyID** XML 属性，客户税架构仍然包含自定义 **FederalTaxID** XML 属性。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-564">Notice that, in accordance with your customization, the customer tax schema still contains the custom **FederalTaxID** XML attribute in addition to the **schemeID** and **schemeAgencyID** XML attributes.</span></span> <span data-ttu-id="6b4b8-565">另外，因为基本 **UBL 销售发票** 格式的新版本中的更改已与您的自定义合并，因此 **cbc:CustomizationID** XML 元素的文本已从 `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0` 更改为 `urn:cen.eu:en16931:2017#compliant#urn:fdc:peppol.eu:2017:poacc:billing:3.0`。</span><span class="sxs-lookup"><span data-stu-id="6b4b8-565">Additionally, because the changes in the new version of the base **UBL Sales invoice** format were merged with your customization, the text of the **cbc:CustomizationID** XML element has been changed from `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0` to `urn:cen.eu:en16931:2017#compliant#urn:fdc:peppol.eu:2017:poacc:billing:3.0`.</span></span>

    ![具有自定义的已生成电子发票 XML 文件预览](./media/er-quick-start3-e-invoice3.png)

## <a name="additional-resources"></a><span data-ttu-id="6b4b8-567">其他资源</span><span class="sxs-lookup"><span data-stu-id="6b4b8-567">Additional resources</span></span>

- [<span data-ttu-id="6b4b8-568">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="6b4b8-568">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="6b4b8-569">从 Lifecycle Services 下载 ER 配置</span><span class="sxs-lookup"><span data-stu-id="6b4b8-569">Download ER configurations from Lifecycle Services</span></span>](download-electronic-reporting-configuration-lcs.md)
- [<span data-ttu-id="6b4b8-570">从 Configuration Service 的全局存储库下载 ER 配置</span><span class="sxs-lookup"><span data-stu-id="6b4b8-570">Download ER configurations from Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
- [<span data-ttu-id="6b4b8-571">创建普通账单</span><span class="sxs-lookup"><span data-stu-id="6b4b8-571">Create a free text invoice</span></span>](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/create-free-text-invoice-new)
- [<span data-ttu-id="6b4b8-572">创建并使用自定义字段</span><span class="sxs-lookup"><span data-stu-id="6b4b8-572">Create and work with custom fields</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
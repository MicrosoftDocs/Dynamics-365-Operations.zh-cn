---
title: 调整 ER 格式以生成自定义电子单据
description: 本主题说明如何调整 Microsoft 提供的电子申报 (ER) 格式，以便生成自定义电子单据。
author: NickSelin
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 20e7a32ac5f6ab21f89ed3c11c64458286864c9d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680162"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a><span data-ttu-id="01a9e-103">调整 ER 格式以生成自定义电子单据</span><span class="sxs-lookup"><span data-stu-id="01a9e-103">Adjust an ER format to generate a custom electronic document</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="01a9e-104">本主题中的过程介绍系统管理员或电子申报功能顾问角色的用户如何执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="01a9e-104">The procedures in this topic explain how a user in the System Administrator or Electronic Reporting Functional Consultant role can perform these tasks:</span></span>

- <span data-ttu-id="01a9e-105">配置[电子申报 (ER) 框架](general-electronic-reporting.md)的参数。</span><span class="sxs-lookup"><span data-stu-id="01a9e-105">Configure parameters for the [Electronic reporting (ER) framework](general-electronic-reporting.md).</span></span>
- <span data-ttu-id="01a9e-106">导入由 Microsoft 提供并在处理[供应商付款](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md)期间用于生成付款文件的 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="01a9e-106">Import ER configurations that are provided by Microsoft and used to generate a payment file while a [vendor payment](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) is being processed.</span></span>
- <span data-ttu-id="01a9e-107">创建 Microsoft 提供的标准 ER 格式配置的自定义版本。</span><span class="sxs-lookup"><span data-stu-id="01a9e-107">Create a custom version of a standard ER format configuration that is provided by Microsoft.</span></span>
- <span data-ttu-id="01a9e-108">修改自定义 ER 格式配置，以使其生成满足特定银行要求的付款文件。</span><span class="sxs-lookup"><span data-stu-id="01a9e-108">Modify the custom ER format configuration so that it generates payment files that meets the requirements of a specific bank.</span></span>
- <span data-ttu-id="01a9e-109">在自定义 ER 格式配置中应用对标准 ER 格式配置所做的更改。</span><span class="sxs-lookup"><span data-stu-id="01a9e-109">Adopt changes that are made to the standard ER format configuration in the custom ER format configuration.</span></span>

<span data-ttu-id="01a9e-110">以下所有过程均可在 **GBSI** 公司中完成。</span><span class="sxs-lookup"><span data-stu-id="01a9e-110">All the following procedures can be done in the **GBSI** company.</span></span> <span data-ttu-id="01a9e-111">无需进行编码。</span><span class="sxs-lookup"><span data-stu-id="01a9e-111">No coding is required.</span></span>

- [<span data-ttu-id="01a9e-112">配置 ER 框架</span><span class="sxs-lookup"><span data-stu-id="01a9e-112">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="01a9e-113">配置 ER 参数</span><span class="sxs-lookup"><span data-stu-id="01a9e-113">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="01a9e-114">激活 ER 配置提供程序</span><span class="sxs-lookup"><span data-stu-id="01a9e-114">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="01a9e-115">查看 ER 配置提供程序列表</span><span class="sxs-lookup"><span data-stu-id="01a9e-115">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="01a9e-116">添加新 ER 配置提供程序</span><span class="sxs-lookup"><span data-stu-id="01a9e-116">Add a new ER configuration provider</span></span>](#ActivateProvider)
        - [<span data-ttu-id="01a9e-117">激活 ER 配置提供程序</span><span class="sxs-lookup"><span data-stu-id="01a9e-117">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="01a9e-118">导入标准 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="01a9e-118">Import the standard ER format configurations</span></span>](#ImportERSolution1)

    - [<span data-ttu-id="01a9e-119">导入标准 ER 配置</span><span class="sxs-lookup"><span data-stu-id="01a9e-119">Import the standard ER configurations</span></span>](#ImportERFormat1)
    - [<span data-ttu-id="01a9e-120">查看导入的 ER 配置</span><span class="sxs-lookup"><span data-stu-id="01a9e-120">Review the imported ER configurations</span></span>](#ReviewImportedERSolution)

- [<span data-ttu-id="01a9e-121">准备要处理的供应商付款</span><span class="sxs-lookup"><span data-stu-id="01a9e-121">Prepare a vendor payment for processing</span></span>](#PrepareVendorPayment)

    - [<span data-ttu-id="01a9e-122">添加供应商帐户的银行信息</span><span class="sxs-lookup"><span data-stu-id="01a9e-122">Add bank information for a vendor account</span></span>](#AddBankAccount)
    - [<span data-ttu-id="01a9e-123">输入供应商付款</span><span class="sxs-lookup"><span data-stu-id="01a9e-123">Enter a vendor payment</span></span>](#EnterVendorPayment)

- [<span data-ttu-id="01a9e-124">使用标准 ER 格式处理供应商付款</span><span class="sxs-lookup"><span data-stu-id="01a9e-124">Process a vendor payment by using the standard ER format</span></span>](#ProcessVendorPayment1)

    - [<span data-ttu-id="01a9e-125">设置电子付款方式</span><span class="sxs-lookup"><span data-stu-id="01a9e-125">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment1)
    - [<span data-ttu-id="01a9e-126">处理供应商付款</span><span class="sxs-lookup"><span data-stu-id="01a9e-126">Process a vendor payment</span></span>](#ProcessPayment1)

- [<span data-ttu-id="01a9e-127">自定义标准 ER 格式</span><span class="sxs-lookup"><span data-stu-id="01a9e-127">Customize the standard ER format</span></span>](#CustomizeProvidedFormat)

    - [<span data-ttu-id="01a9e-128">创建自定义格式</span><span class="sxs-lookup"><span data-stu-id="01a9e-128">Create a custom format</span></span>](#DeriveProvidedFormat)
    - [<span data-ttu-id="01a9e-129">编辑自定义格式</span><span class="sxs-lookup"><span data-stu-id="01a9e-129">Edit a custom format</span></span>](#ConfigureDerivedFormat)
    - [<span data-ttu-id="01a9e-130">将自定义格式标记为可运行</span><span class="sxs-lookup"><span data-stu-id="01a9e-130">Mark a custom format as runnable</span></span>](#MarkFormatRunnable)

- [<span data-ttu-id="01a9e-131">使用自定义 ER 格式处理供应商付款</span><span class="sxs-lookup"><span data-stu-id="01a9e-131">Process a vendor payment by using the custom ER format</span></span>](#ProcessVendorPayment2)

    - [<span data-ttu-id="01a9e-132">设置电子付款方式</span><span class="sxs-lookup"><span data-stu-id="01a9e-132">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment2)
    - [<span data-ttu-id="01a9e-133">处理供应商付款</span><span class="sxs-lookup"><span data-stu-id="01a9e-133">Process a vendor payment</span></span>](#ProcessPayment2)

- [<span data-ttu-id="01a9e-134">导入标准 ER 格式配置的新版本</span><span class="sxs-lookup"><span data-stu-id="01a9e-134">Import new versions of the standard ER format configurations</span></span>](#ImportERSolution2)

    - [<span data-ttu-id="01a9e-135">导入标准 ER 配置的新版本</span><span class="sxs-lookup"><span data-stu-id="01a9e-135">Import new versions of the standard ER configurations</span></span>](#ImportERFormat2)
    - [<span data-ttu-id="01a9e-136">查看导入的 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="01a9e-136">Review the imported ER format configurations</span></span>](#ReviewImportedERFormat)

- [<span data-ttu-id="01a9e-137">在自定义格式中采用在所导入格式的新版本中进行的更改</span><span class="sxs-lookup"><span data-stu-id="01a9e-137">Adopt the changes in the new version of an imported format in a custom format</span></span>](#AdoptNewBaseVersion)

    - [<span data-ttu-id="01a9e-138">完成自定义格式的当前草稿版本</span><span class="sxs-lookup"><span data-stu-id="01a9e-138">Complete the current draft version of a custom format</span></span>](#CompleteDerivedFormat)
    - [<span data-ttu-id="01a9e-139">将自定义格式重定为新基本版本</span><span class="sxs-lookup"><span data-stu-id="01a9e-139">Rebase a custom format to a new base version</span></span>](#RebaseDerivedFormat)
    - [<span data-ttu-id="01a9e-140">使用重定 ER 格式处理供应商付款</span><span class="sxs-lookup"><span data-stu-id="01a9e-140">Process a vendor payment by using a rebased ER format</span></span>](#ProcessPayment3)

- [<span data-ttu-id="01a9e-141">其他资源</span><span class="sxs-lookup"><span data-stu-id="01a9e-141">Additional resources</span></span>](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a><span data-ttu-id="01a9e-142">配置 ER 框架</span><span class="sxs-lookup"><span data-stu-id="01a9e-142">Configure the ER framework</span></span>

<span data-ttu-id="01a9e-143">作为电子申报功能顾问角色的用户，您必须至少配置一小组 ER 参数，才能开始使用 ER 框架设计标准 ER 格式的自定义版本。</span><span class="sxs-lookup"><span data-stu-id="01a9e-143">As a user in the Electronic Reporting Functional Consultant role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design a custom version of a standard ER format.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="01a9e-144">配置 ER 参数</span><span class="sxs-lookup"><span data-stu-id="01a9e-144">Configure ER parameters</span></span>

1. <span data-ttu-id="01a9e-145">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-145">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="01a9e-146">在 **本地化配置** 页面的 **相关链接** 部分中，选择 **电子申报参数**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-146">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="01a9e-147">在 **电子申报参数** 页上，在 **常规** 选项卡上，将 **启用设计模式** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-147">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="01a9e-148">在 **附件** 选项卡上，设置以下参数：</span><span class="sxs-lookup"><span data-stu-id="01a9e-148">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="01a9e-149">在 **配置** 字段中，选择 **USMF** 公司的 **文件** 类型。</span><span class="sxs-lookup"><span data-stu-id="01a9e-149">In the **Configurations** field, select the **File** type for the **USMF** company.</span></span>
    - <span data-ttu-id="01a9e-150">在 **作业存档**、**临时**、**基准** 和 **其他** 字段中，选择 **文件** 类型。</span><span class="sxs-lookup"><span data-stu-id="01a9e-150">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="01a9e-151">有关 ER 参数的详细信息，请参阅[配置 ER 框架](electronic-reporting-er-configure-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="01a9e-151">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="01a9e-152">激活 ER 配置提供程序</span><span class="sxs-lookup"><span data-stu-id="01a9e-152">Activate an ER configuration provider</span></span>

<span data-ttu-id="01a9e-153">将把添加的每个 ER 配置标记为由 ER 配置提供程序负责。</span><span class="sxs-lookup"><span data-stu-id="01a9e-153">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="01a9e-154">在 **电子申报** 工作区中激活的 ER 配置提供程序用于此目的。</span><span class="sxs-lookup"><span data-stu-id="01a9e-154">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="01a9e-155">因此，必须先在 **电子申报** 工作区中激活 ER 配置提供程序，才能开始添加或编辑 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="01a9e-155">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="01a9e-156">只有 ER 配置的负责人才能对其进行编辑。</span><span class="sxs-lookup"><span data-stu-id="01a9e-156">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="01a9e-157">因此，必须先在 **电子申报** 工作区中激活相应 ER 配置提供程序，才能编辑 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="01a9e-157">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="01a9e-158">查看 ER 配置提供程序列表</span><span class="sxs-lookup"><span data-stu-id="01a9e-158">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="01a9e-159">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-159">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="01a9e-160">在 **本地化配置** 页面的 **相关链接** 部分中，选择 **配置提供程序**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-160">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="01a9e-161">在 **配置提供程序表** 页面中，每条提供程序记录都有唯一名称和 URL。</span><span class="sxs-lookup"><span data-stu-id="01a9e-161">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="01a9e-162">查看此页面的内容。</span><span class="sxs-lookup"><span data-stu-id="01a9e-162">Review the contents of this page.</span></span> <span data-ttu-id="01a9e-163">如果已有 **Litware, Inc.** (`https://www.litware.com`) 的记录，请跳过下一过程，即[添加新 ER 配置提供程序](#ActivateProvider)。</span><span class="sxs-lookup"><span data-stu-id="01a9e-163">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="01a9e-164">添加新 ER 配置提供程序</span><span class="sxs-lookup"><span data-stu-id="01a9e-164">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="01a9e-165">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-165">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="01a9e-166">在 **本地化配置** 页面的 **相关链接** 部分中，选择 **配置提供程序**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-166">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="01a9e-167">在 **配置提供程序** 页面上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-167">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="01a9e-168">在 **名称** 字段中，输入 **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="01a9e-168">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="01a9e-169">在 **Internet 地址** 字段中，输入 `https://www.litware.com`。</span><span class="sxs-lookup"><span data-stu-id="01a9e-169">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="01a9e-170">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-170">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="01a9e-171">激活 ER 配置提供程序</span><span class="sxs-lookup"><span data-stu-id="01a9e-171">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="01a9e-172">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-172">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="01a9e-173">在 **本地化配置** 页面的 **配置提供程序** 部分中，选择 **Litware, Inc.** 磁贴，然后选择 **设置有效**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-173">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="01a9e-174">有关 ER 配置提供程序的详细信息，请参阅[创建配置提供程序并将其标记为有效](tasks/er-configuration-provider-mark-it-active-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="01a9e-174">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a><span data-ttu-id="01a9e-175">导入标准 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="01a9e-175">Import the standard ER format configurations</span></span>

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a><span data-ttu-id="01a9e-176">导入标准 ER 配置</span><span class="sxs-lookup"><span data-stu-id="01a9e-176">Import the standard ER configurations</span></span>

<span data-ttu-id="01a9e-177">若要向当前 Microsoft Dynamics 365 Finance 实例添加标准 ER 配置，必须从为该实例配置的 ER [存储库](general-electronic-reporting.md#Repository)导入这些配置。</span><span class="sxs-lookup"><span data-stu-id="01a9e-177">To add the standard ER configurations to your current instance of Microsoft Dynamics 365 Finance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="01a9e-178">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-178">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="01a9e-179">在 **本地化配置** 页面的 **配置提供程序** 部分中，选择 **Microsoft** 磁贴，然后选择 **存储库** 查看 Microsoft 提供程序的存储库列表。</span><span class="sxs-lookup"><span data-stu-id="01a9e-179">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="01a9e-180">在 **配置存储库** 页，选择 **全球** 类型的存储库，然后选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-180">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="01a9e-181">如果提示您进行授权以连接到 Regulatory Configuration Service，请按照授权说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="01a9e-181">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="01a9e-182">在 **配置存储库** 页面左侧窗格的配置树中，选择 **BACS (UK)** 格式配置。</span><span class="sxs-lookup"><span data-stu-id="01a9e-182">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="01a9e-183">在 **版本** 快速选项卡上，选择所选 ER 格式配置的版本 **1.1**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-183">On the **Versions** FastTab, select version **1.1** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="01a9e-184">选择 **导入** 将所选版本从全局存储库下载到当前 Finance 实例。</span><span class="sxs-lookup"><span data-stu-id="01a9e-184">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![配置存储库页面](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> <span data-ttu-id="01a9e-186">如果在访问[全球存储库](er-download-configurations-global-repo.md)时遇到问题，可改为从 Microsoft Dynamics Lifecycle Services (LCS)[ 下载配置](download-electronic-reporting-configuration-lcs.md)。</span><span class="sxs-lookup"><span data-stu-id="01a9e-186">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from Microsoft Dynamics Lifecycle Services (LCS) instead.</span></span>

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a><span data-ttu-id="01a9e-187">查看导入的 ER 配置</span><span class="sxs-lookup"><span data-stu-id="01a9e-187">Review the imported ER configurations</span></span>

1. <span data-ttu-id="01a9e-188">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-188">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="01a9e-189">在 **本地化配置** 页面的 **配置** 部分中，选择 **报告配置** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="01a9e-189">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="01a9e-190">在 **配置** 页的左侧窗格的配置树中，展开 **付款模型**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-190">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**.</span></span>
4. <span data-ttu-id="01a9e-191">请注意，除了所选 **BACS (UK)** ER 格式，还导入了其他必需的 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="01a9e-191">Notice that, in addition to the selected **BACS (UK)** ER format, other required ER configurations were imported.</span></span> <span data-ttu-id="01a9e-192">请确保配置树中有以下 ER 配置：</span><span class="sxs-lookup"><span data-stu-id="01a9e-192">Make sure that the following ER configurations are available in the configuration tree:</span></span>

    - <span data-ttu-id="01a9e-193">**付款模型** – 此配置中包含[数据模型](general-electronic-reporting.md#data-model-and-model-mapping-components) ER 组件，用于表示付款业务域的数据结构。</span><span class="sxs-lookup"><span data-stu-id="01a9e-193">**Payment model** – This configuration contains the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that represents the data structure of the payment business domain.</span></span>
    - <span data-ttu-id="01a9e-194">**付款模型映射 1611** – 此配置中包含[模型映射](general-electronic-reporting.md#data-model-and-model-mapping-components) ER 组件，用于描述如何在运行时使用应用程序数据填充数据模型。</span><span class="sxs-lookup"><span data-stu-id="01a9e-194">**Payment model mapping 1611** – This configuration contains the [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that describes how the data model is filled in with application data at runtime.</span></span>
    - <span data-ttu-id="01a9e-195">**BACS (UK)** – 此配置中包含[格式](general-electronic-reporting.md#FormatComponentOutbound)和格式映射 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="01a9e-195">**BACS (UK)** – This configuration contains the [format](general-electronic-reporting.md#FormatComponentOutbound) and format mapping ER components.</span></span> <span data-ttu-id="01a9e-196">格式组件指定报表布局。</span><span class="sxs-lookup"><span data-stu-id="01a9e-196">The format component specifies the report layout.</span></span> <span data-ttu-id="01a9e-197">格式映射组件中包含模型数据源，并指定如何在运行时使用此数据源填充报表布局。</span><span class="sxs-lookup"><span data-stu-id="01a9e-197">The format mapping component contains the model data source and specifies how the report layout is filled in by using this data source at runtime.</span></span>

![配置页面](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a><span data-ttu-id="01a9e-199">准备要处理的供应商付款</span><span class="sxs-lookup"><span data-stu-id="01a9e-199">Prepare a vendor payment for processing</span></span>

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a><span data-ttu-id="01a9e-200">添加供应商帐户的银行信息</span><span class="sxs-lookup"><span data-stu-id="01a9e-200">Add bank information for a vendor account</span></span>

<span data-ttu-id="01a9e-201">必须在等记付款中添加后文将引用的供应商帐户的银行信息。</span><span class="sxs-lookup"><span data-stu-id="01a9e-201">You must add bank information for a vendor account that will be referred to later in a registered payment.</span></span>

1. <span data-ttu-id="01a9e-202">转到 **应付帐款** \> **供应商** \> **所有供应商**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-202">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="01a9e-203">在 **所有供应商** 页面中，选择 **GB_SI_000001** 供应商帐户，然后在操作窗格中 **供应商** 选项卡上的 **设置** 组中，选择 **银行帐户**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-203">On the **All vendors** page, select the **GB_SI_000001** vendor account, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="01a9e-204">在 **供应商银行帐户** 页面上，选择 **新建**，然后输入以下信息：</span><span class="sxs-lookup"><span data-stu-id="01a9e-204">On the **Vendor bank accounts** page, select **New**, and then enter the following information:</span></span>

    1. <span data-ttu-id="01a9e-205">在 **银行帐户** 字段中，输入 **GBP OPER**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-205">In the **Bank account** field, enter **GBP OPER**.</span></span>
    2. <span data-ttu-id="01a9e-206">在 **银行组** 字段中，选择 **BankGBP**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-206">In the **Bank groups** field, select **BankGBP**.</span></span>
    3. <span data-ttu-id="01a9e-207">在 **银行帐号** 字段中，输入 **202015**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-207">In the **Bank account number** field, enter **202015**.</span></span>
    4. <span data-ttu-id="01a9e-208">在 **SWIFT 代码** 字段中，输入 <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-208">In the **SWIFT code** field, enter <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span></span>
    5. <span data-ttu-id="01a9e-209">在 **IBAN** 字段中，输入 **GB33BUKB20201555555555**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-209">In the **IBAN** field, enter **GB33BUKB20201555555555**.</span></span>
    6. <span data-ttu-id="01a9e-210">在 **银行代号** 字段中，保留默认值 <a id="DefineRoutingNumber"></a>**123456**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-210">In the **Routing number** field, keep the default value, <a id="DefineRoutingNumber"></a>**123456**.</span></span>

    ![“供应商银行帐户”页面](./media/er-quick-start2-bank-account.png)

4. <span data-ttu-id="01a9e-212">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-212">Select **Save**.</span></span>
5. <span data-ttu-id="01a9e-213">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="01a9e-213">Close the page.</span></span>
6. <span data-ttu-id="01a9e-214">在 **所有供应商** 页面中，打开 **GB_SI_000001** 供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="01a9e-214">On the **All vendors** page, open the **GB_SI_000001** vendor account.</span></span>
7. <span data-ttu-id="01a9e-215">在供应商详细信息页面上，选择 **编辑** 使页面可编辑（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="01a9e-215">On the vendor details page, select **Edit** to make the page editable, if required.</span></span>
8. <span data-ttu-id="01a9e-216">在 **付款** 快速选项卡的 **银行帐户** 字段中，选择 **GBP OPER**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-216">On the **Payment** FastTab, in the **Bank account** field, select **GBP OPER**.</span></span>

    ![供应商详细信息页面](./media/er-quick-start2-bank-account-reference.png)

9. <span data-ttu-id="01a9e-218">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-218">Select **Save**.</span></span>
10. <span data-ttu-id="01a9e-219">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="01a9e-219">Close the page.</span></span>

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a><span data-ttu-id="01a9e-220">输入供应商付款</span><span class="sxs-lookup"><span data-stu-id="01a9e-220">Enter a vendor payment</span></span>

<span data-ttu-id="01a9e-221">必须使用[付款方案](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal)创建新的供应商付款。</span><span class="sxs-lookup"><span data-stu-id="01a9e-221">You must enter a new vendor payment by using a [payment proposal](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span></span>

1. <span data-ttu-id="01a9e-222">转到 **应付帐款** \> **付款** \> **供应商付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-222">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="01a9e-223">在 **供应商付款日记帐** 页面上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-223">On the **Vendor payment journal** page, select **New**.</span></span>
3. <span data-ttu-id="01a9e-224">在 **名称** 字段中，选择 **VendPay**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-224">In the **Name** field, select **VendPay**.</span></span>
4. <span data-ttu-id="01a9e-225">选择 **行**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-225">Select **Lines**.</span></span>
5. <span data-ttu-id="01a9e-226">选择 **付款方案** \> **创建付款方案**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-226">Select **Payment proposal** \> **Create payment proposal**.</span></span>
6. <span data-ttu-id="01a9e-227">在 **供应商付款方案** 对话框中，将条件配置为仅筛选 **GB_SI_000001** 供应商帐户的记录，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-227">In the **Vendor payment proposal** dialog box, configure conditions to filter for records for the **GB_SI_000001** vendor account only, and then select **OK**.</span></span>
7. <span data-ttu-id="01a9e-228">选择发票 **00000007_Inv** 的行，然后选择 **创建付款**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-228">Select the line for the **00000007_Inv** invoice, and then select **Create payment**.</span></span>

    ![供应商付款方案对话框](./media/er-quick-start2-payment-proposal.png)

8. <span data-ttu-id="01a9e-230">验证是否将输入的付款配置为使用 **电子** 付款方式。</span><span class="sxs-lookup"><span data-stu-id="01a9e-230">Verify that the payment that is entered is configured to use the **Electronic** method of payment.</span></span>

    ![供应商付款页面](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a><span data-ttu-id="01a9e-232">使用标准 ER 格式处理供应商付款</span><span class="sxs-lookup"><span data-stu-id="01a9e-232">Process a vendor payment by using the standard ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a><span data-ttu-id="01a9e-233">设置电子付款方式</span><span class="sxs-lookup"><span data-stu-id="01a9e-233">Set up the electronic payment method</span></span>

<span data-ttu-id="01a9e-234">必须使用电子付款方式，以使其使用导入的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="01a9e-234">You must configure the electronic method of payment so that it uses the imported ER format configuration.</span></span>

1. <span data-ttu-id="01a9e-235">转到 **应付帐款** \> **付款设置** \> **付款方式**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-235">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="01a9e-236">在 **付款方式 - 供应商** 页面中，在左侧窗格中选择 **电子** 付款方式。</span><span class="sxs-lookup"><span data-stu-id="01a9e-236">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="01a9e-237">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-237">Select **Edit**.</span></span>
4. <span data-ttu-id="01a9e-238">在 **文件格式** 快速选项卡上，将 **一般电子导出格式** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-238">On the **File formats** FastTab, set the **General electronic Export format** option to **Yes**.</span></span>
5. <span data-ttu-id="01a9e-239">在 **导出格式配置** 字段中，选择 **BACS (UK)** 格式配置。</span><span class="sxs-lookup"><span data-stu-id="01a9e-239">In the **Export format configuration** field, select the **BACS (UK)** format configuration.</span></span>

    ![付款方式 - 供应商页面](./media/er-quick-start2-method-of-payment1.png)

6. <span data-ttu-id="01a9e-241">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-241">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a><span data-ttu-id="01a9e-242">处理供应商付款</span><span class="sxs-lookup"><span data-stu-id="01a9e-242">Process a vendor payment</span></span>

1. <span data-ttu-id="01a9e-243">转到 **应付帐款** \> **付款** \> **供应商付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-243">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="01a9e-244">在 **供应商付款日记帐** 页面上，选择您先前添加的付款日记帐，然后选择 **行**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-244">On the **Vendor payment journal** page, select the payment journal that you added earlier, and then select **Lines**.</span></span>
3. <span data-ttu-id="01a9e-245">在 **供应商付款** 页面上，选择 **生成付款**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-245">On the **Vendor payments** page, select **Generate payments**.</span></span>
4. <span data-ttu-id="01a9e-246">在 **生成付款** 对话框中，输入以下信息：</span><span class="sxs-lookup"><span data-stu-id="01a9e-246">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="01a9e-247">在 **付款方式** 字段中，选择 **电子**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-247">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="01a9e-248">在 **银行帐户** 字段中，选择 **GBSI OPER**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-248">In the **Bank account** field, select **GBSI OPER**.</span></span>

5. <span data-ttu-id="01a9e-249">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-249">Select **OK**.</span></span>
6. <span data-ttu-id="01a9e-250">在 **电子报表参数** 对话框中，将 **打印控制报表** 选项设置为 **是**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-250">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    ![“电子报表参数对话框”页面](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > <span data-ttu-id="01a9e-252">除了付款文件，现在还可以生成控制报表。</span><span class="sxs-lookup"><span data-stu-id="01a9e-252">In addition to the payment file, you can now generate the control report.</span></span>

7. <span data-ttu-id="01a9e-253">下载 zip 文件，然后从中提取以下文件：</span><span class="sxs-lookup"><span data-stu-id="01a9e-253">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="01a9e-254">Excel 格式的控制报表</span><span class="sxs-lookup"><span data-stu-id="01a9e-254">The control report in Excel format</span></span>
    - <span data-ttu-id="01a9e-255">TXT 格式的付款文件</span><span class="sxs-lookup"><span data-stu-id="01a9e-255">The payment file in TXT format</span></span>

        <span data-ttu-id="01a9e-256">请注意，按照提供的 ER 格式的[结构](#PositionRoutingNumber)，生成的文件中的付款行以为配置的用户帐户[定义的](#DefineRoutingNumber)银行代号开始。</span><span class="sxs-lookup"><span data-stu-id="01a9e-256">Notice that, in accordance with the [structure](#PositionRoutingNumber) of the provided ER format, the payment line in the generated file starts with the routing number that was [defined](#DefineRoutingNumber) for the configured bank account.</span></span>

        ![TXT 格式的付款文件](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a><span data-ttu-id="01a9e-258">自定义标准 ER 格式</span><span class="sxs-lookup"><span data-stu-id="01a9e-258">Customize the standard ER format</span></span>

<span data-ttu-id="01a9e-259">对于此部分中显示的示例，需要使用 Microsoft 提供的 ER 配置生成 BACS 格式的供应商付款文件，但是必须添加自定义来支持特定银行的要求。</span><span class="sxs-lookup"><span data-stu-id="01a9e-259">For the example that is shown in this section, you want to use the ER configurations that are provided by Microsoft to generate vendor payment files in BACS format, but you must add a customization to support the requirements of a specific bank.</span></span> <span data-ttu-id="01a9e-260">还需要可以在新的 ER 配置版本可用时升级自定义格式。</span><span class="sxs-lookup"><span data-stu-id="01a9e-260">You also want to be able to upgrade your custom format when new versions of ER configurations become available.</span></span> <span data-ttu-id="01a9e-261">但是，您希望可以以最低成本进行升级。</span><span class="sxs-lookup"><span data-stu-id="01a9e-261">However, you want to be able to do the upgrade at the lowest cost.</span></span>

<span data-ttu-id="01a9e-262">在此情况下，作为 Litware, Inc. 的代表，您必须以 **BACS (UK)** Microsoft 提供的配置为基础创建（派生）新 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="01a9e-262">In this case, as the representative of Litware, Inc., you must create (derive) a new ER format configuration by using the **BACS (UK)** Microsoft-provided configuration as a base.</span></span>

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a><span data-ttu-id="01a9e-263">创建自定义格式</span><span class="sxs-lookup"><span data-stu-id="01a9e-263">Create a custom format</span></span>

1. <span data-ttu-id="01a9e-264">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-264">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="01a9e-265">在 **配置** 页的左侧窗格的配置树中，展开 **付款模型**，然后选择 **BACS (UK)**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-265">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span> <span data-ttu-id="01a9e-266">Litware, Inc. 将把此 ER 格式配置的版本 1.1 用作自定义版本的基础。</span><span class="sxs-lookup"><span data-stu-id="01a9e-266">Litware, Inc. will use version 1.1 of this ER format configuration as the base for the custom version.</span></span>
3. <span data-ttu-id="01a9e-267">选择 **创建配置**，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="01a9e-267">Select **Create configuration** to open the drop-down dialog box.</span></span> <span data-ttu-id="01a9e-268">可使用此对话框创建自定义付款格式的新配置。</span><span class="sxs-lookup"><span data-stu-id="01a9e-268">You can use this dialog box to create a new configuration for a custom payment format.</span></span>
4. <span data-ttu-id="01a9e-269">在 **新建** 字段组中，选择 **从以下名称派生: BACS (UK), Microsoft** 选项。</span><span class="sxs-lookup"><span data-stu-id="01a9e-269">In the **New** field group, select the **Derive from Name: BACS (UK), Microsoft** option.</span></span>
5. <span data-ttu-id="01a9e-270">在 **名称** 字段中，输入 **BACS（UK 自定义）**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-270">In the **Name** field, enter **BACS (UK custom)**.</span></span>

    ![“创建配置”下拉对话框](./media/er-quick-start2-add-derived-format.png)

6. <span data-ttu-id="01a9e-272">选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-272">Select **Create configuration**.</span></span>

<span data-ttu-id="01a9e-273">将创建 **BACS（UK 自定义）** ER 格式配置的版本 1.1.1。</span><span class="sxs-lookup"><span data-stu-id="01a9e-273">Version 1.1.1 of the **BACS (UK custom)** ER format configuration is created.</span></span> <span data-ttu-id="01a9e-274">此版本的 [状态](general-electronic-reporting.md#component-versioning)为 **草稿**，可以编辑。</span><span class="sxs-lookup"><span data-stu-id="01a9e-274">This version has a [status](general-electronic-reporting.md#component-versioning) of **Draft** and can be edited.</span></span> <span data-ttu-id="01a9e-275">自定义 ER 格式的当前内容与 Microsoft 提供的格式的内容匹配。</span><span class="sxs-lookup"><span data-stu-id="01a9e-275">The current content of your custom ER format matches the content of the format that is provided by Microsoft.</span></span>

![配置页面](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a><span data-ttu-id="01a9e-277">编辑自定义格式</span><span class="sxs-lookup"><span data-stu-id="01a9e-277">Edit a custom format</span></span>

<span data-ttu-id="01a9e-278">必须配置自定义格式，使其满足银行的特定要求。</span><span class="sxs-lookup"><span data-stu-id="01a9e-278">You must configure your custom format so that it meets bank-specific requirements.</span></span> <span data-ttu-id="01a9e-279">例如，一家银行可能要求生成的付款文件中包含银行的国际银行金融电信协会 (SWIFT) 代码，该代码为银行分配所处理供应商付款中的代理角色。</span><span class="sxs-lookup"><span data-stu-id="01a9e-279">For example, a bank might require that payment files that are generated include the Society for Worldwide Interbank Financial Telecommunication (SWIFT) code of a bank that is assigned the agent role in the processed vendor payment.</span></span> <span data-ttu-id="01a9e-280">SWIFT 代码是用于在全球识别特定银行的国际银行代码。</span><span class="sxs-lookup"><span data-stu-id="01a9e-280">SWIFT codes are international bank codes that identify specific banks worldwide.</span></span> <span data-ttu-id="01a9e-281">也称为银行标识符代码 (BIC)。</span><span class="sxs-lookup"><span data-stu-id="01a9e-281">They are also known as Bank Identifier Codes (BICs).</span></span> <span data-ttu-id="01a9e-282">SWIFT 代码的长度必须为 11 个字符，并且必须在生成的付款文件中每个付款行开始处输入。</span><span class="sxs-lookup"><span data-stu-id="01a9e-282">The SWIFT code must be 11 characters long, and it must be entered at the beginning of every payment line in a generated payment file.</span></span>

1. <span data-ttu-id="01a9e-283">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-283">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="01a9e-284">在 **配置** 页的左侧窗格的配置树中，展开 **付款模型**，然后选择 **BACS（UK 自定义）**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-284">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="01a9e-285">在 **版本** 快速选项卡上，选择所选配置的版本 **1.1.1**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-285">On the **Versions** FastTab, select version **1.1.1** of the selected configuration.</span></span>
4. <span data-ttu-id="01a9e-286">选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-286">Select **Designer**.</span></span>
5. <span data-ttu-id="01a9e-287">在 **格式设计器** 页面中，选择 **显示详细信息** 查看有关格式元素的详细信息。</span><span class="sxs-lookup"><span data-stu-id="01a9e-287">On the **Format designer** page, select **Show details** to view more information about the format elements.</span></span>
6. <span data-ttu-id="01a9e-288">展开并查看以下元素：</span><span class="sxs-lookup"><span data-stu-id="01a9e-288">Expand and review the following elements:</span></span>

    - <span data-ttu-id="01a9e-289">**文件夹** 类型的 **BACSReportsFolder** 元素。</span><span class="sxs-lookup"><span data-stu-id="01a9e-289">The **BACSReportsFolder** element of the **Folder** type.</span></span> <span data-ttu-id="01a9e-290">此元素用于生成 ZIP 格式的输出。</span><span class="sxs-lookup"><span data-stu-id="01a9e-290">This element is used to generate output in ZIP format.</span></span>
    - <span data-ttu-id="01a9e-291">**文件** 类型的 **file** 元素。</span><span class="sxs-lookup"><span data-stu-id="01a9e-291">The **file** element of the **File** type.</span></span> <span data-ttu-id="01a9e-292">此元素用于生成 TXT 格式的付款文件。</span><span class="sxs-lookup"><span data-stu-id="01a9e-292">This element is used to generate a payment file in TXT format.</span></span>
    - <span data-ttu-id="01a9e-293">**序列** 类型的 **transactions** 元素。</span><span class="sxs-lookup"><span data-stu-id="01a9e-293">The **transactions** element of the **Sequence** type.</span></span> <span data-ttu-id="01a9e-294">此元素用于在付款文件中生成单个付款行。</span><span class="sxs-lookup"><span data-stu-id="01a9e-294">This element is used to generate a single payment line in a payment file.</span></span>
    - <span data-ttu-id="01a9e-295">**序列** 类型的 **transaction** 元素。</span><span class="sxs-lookup"><span data-stu-id="01a9e-295">The **transaction** element of the **Sequence** type.</span></span> <span data-ttu-id="01a9e-296">此元素用于生成单个付款行的各字段。</span><span class="sxs-lookup"><span data-stu-id="01a9e-296">This element is used to generate individual fields of a single payment line.</span></span>

7. <span data-ttu-id="01a9e-297">选择 **transaction** 元素。</span><span class="sxs-lookup"><span data-stu-id="01a9e-297">Select the **transaction** element.</span></span>

    ![ER Operations 设计器中的 transaction 元素](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > <span data-ttu-id="01a9e-299">将配置提供的报表，使<a id="PositionRoutingNumber"></a>每个付款行以银行代号开头。</span><span class="sxs-lookup"><span data-stu-id="01a9e-299">The provided report is configured so that <a id="PositionRoutingNumber"></a>every payment line starts with the bank routing number.</span></span> <span data-ttu-id="01a9e-300">**vendBankRouteNum** 格式元素用于此目的。</span><span class="sxs-lookup"><span data-stu-id="01a9e-300">The **vendBankRouteNum** format element is used for this purpose.</span></span> 

8. <span data-ttu-id="01a9e-301">选择 **添加**，然后选择添加的格式元素的 **Text\\String** 类型：</span><span class="sxs-lookup"><span data-stu-id="01a9e-301">Select **Add**, and then select the **Text\\String** type of the format element that you're adding:</span></span>

    1. <span data-ttu-id="01a9e-302">在 **名称** 字段中，输入 **vendBankSWIFT**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-302">In the **Name** field, enter **vendBankSWIFT**.</span></span>
    2. <span data-ttu-id="01a9e-303">在 **最小长度** 字段中，输入 **11**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-303">In the **Minimum length** field, enter **11**.</span></span>
    3. <span data-ttu-id="01a9e-304">在 **最大长度** 字段中，输入 **11**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-304">In the **Maximum length** field, enter **11**.</span></span>
    4. <span data-ttu-id="01a9e-305">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-305">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="01a9e-306">**vendBankSWIFT** 元素将用于在生成的文件中输入供应商银行的 SWIFT 代码。</span><span class="sxs-lookup"><span data-stu-id="01a9e-306">The **vendBankSWIFT** element will be used to enter the SWIFT code of a vendor bank in generated files.</span></span>

9. <span data-ttu-id="01a9e-307">在格式结构树中，选择 **vendBankSWIFT**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-307">In the format structure tree, select **vendBankSWIFT**.</span></span>
10. <span data-ttu-id="01a9e-308">选择 **上移** 将所选格式元素上移一级。</span><span class="sxs-lookup"><span data-stu-id="01a9e-308">Select **Move up** to move the selected format element up one level.</span></span> <span data-ttu-id="01a9e-309">重复此步骤，直到 **vendBankSWIFT** 元素成为父 **transaction** 元素下的<a id="PositionSWIFTCode"></a>第一个元素。</span><span class="sxs-lookup"><span data-stu-id="01a9e-309">Repeat this step until the **vendBankSWIFT** element is the <a id="PositionSWIFTCode"></a>first element under the parent **transaction** element.</span></span>

    ![VendBankSWIFT 为 ER Operations 设计器中 transaction 下的第一个元素](./media/er-quick-start2-derived-format1.png)

11. <span data-ttu-id="01a9e-311">格式结构树中 **vendBankSWIFT** 仍处于选中状态时，选择 **映射** 选项卡，然后展开 **模型** 数据源。</span><span class="sxs-lookup"><span data-stu-id="01a9e-311">While the **vendBankSWIFT** is still selected in the format structure tree, select the **Mapping** tab, and then expand the **model** data source.</span></span>
12. <span data-ttu-id="01a9e-312">展开 **model.Payment** \> **model.Payment.CreditorAgent**，然后选择 **model.Payment.CreditorAgent.BICFI** 数据源字段。</span><span class="sxs-lookup"><span data-stu-id="01a9e-312">Expand **model.Payment** \> **model.Payment.CreditorAgent**, and select the **model.Payment.CreditorAgent.BICFI** data source field.</span></span> <span data-ttu-id="01a9e-313">此数据源字段显示供应商银行的 SWIFT 代码，该代码在处理的供应商付款中为银行分配代理角色。</span><span class="sxs-lookup"><span data-stu-id="01a9e-313">This data source field exposes the SWIFT code of a vendor bank that is assigned the agent role in the processed vendor payment.</span></span>
13. <span data-ttu-id="01a9e-314">选择 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-314">Select **Bind**.</span></span> <span data-ttu-id="01a9e-315">**vendBankSWIFT** 格式元素现在已经与 **model.Payment.CreditorAgent.BICFI** 数据源字段绑定，因此将在生成的付款文件中输入 SWIFT 代码。</span><span class="sxs-lookup"><span data-stu-id="01a9e-315">The **vendBankSWIFT** format element is now bound with the **model.Payment.CreditorAgent.BICFI** data source field, so that SWIFT codes will be entered in generated payment files.</span></span>

    ![ER Operations 设计器中 vendBankSWIFT 格式元素与 model.Payment.CreditorAgent.BICFI 数据源字段绑定](./media/er-quick-start2-derived-format2.png)

14. <span data-ttu-id="01a9e-317">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-317">Select **Save**.</span></span>
15. <span data-ttu-id="01a9e-318">关闭设计器页面。</span><span class="sxs-lookup"><span data-stu-id="01a9e-318">Close the designer page.</span></span>

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a><span data-ttu-id="01a9e-319">将自定义格式标记为可运行</span><span class="sxs-lookup"><span data-stu-id="01a9e-319">Mark a custom format as runnable</span></span>

<span data-ttu-id="01a9e-320">已创建自定义格式的第一个版本，并且其状态为 **操作**，您可以针对测试用途运行该版本。</span><span class="sxs-lookup"><span data-stu-id="01a9e-320">Now that the first version of your custom format has been created and has a status of **Draft**, you can run it for testing purposes.</span></span> <span data-ttu-id="01a9e-321">若要运行此报表，必须使用引用自定义 ER 格式的付款方式处理供应商付款。</span><span class="sxs-lookup"><span data-stu-id="01a9e-321">To run the report, you must process a vendor payment by using the payment method that refers to your custom ER format.</span></span> <span data-ttu-id="01a9e-322">默认情况下，从应用程序调用 ER 格式时，仅 [考虑](general-electronic-reporting.md#component-versioning)状态为 **已完成** 或 **已共享** 的版本。</span><span class="sxs-lookup"><span data-stu-id="01a9e-322">By default, when you call an ER format from the application, only versions that have a status of **Completed** or **Shared** are [considered](general-electronic-reporting.md#component-versioning).</span></span> <span data-ttu-id="01a9e-323">此行为有助于避免使用未完成设计的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="01a9e-323">This behavior helps prevent ER formats that have unfinished designs from being used.</span></span> <span data-ttu-id="01a9e-324">但是，对于测试运行，可以强制应用程序使用状态为 **草稿** 的 ER 格式版本。</span><span class="sxs-lookup"><span data-stu-id="01a9e-324">However, for your test runs, you can force the application to use the version of your ER format that has a status of **Draft**.</span></span> <span data-ttu-id="01a9e-325">因此，如果需要进行任何修改，可以调整当前格式版本。</span><span class="sxs-lookup"><span data-stu-id="01a9e-325">In this way, you can adjust the current format version if any modifications are required.</span></span> <span data-ttu-id="01a9e-326">有关详细信息，请参阅[适用性](electronic-reporting-destinations.md#applicability)。</span><span class="sxs-lookup"><span data-stu-id="01a9e-326">For more information, see [Applicability](electronic-reporting-destinations.md#applicability).</span></span>

<span data-ttu-id="01a9e-327">要使用 ER 格式的草稿版本，必须显式标记 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="01a9e-327">To use the draft version of an ER format, you must explicitly mark the ER format.</span></span>

1. <span data-ttu-id="01a9e-328">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-328">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="01a9e-329">在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-329">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="01a9e-330">在 **使用参数** 对话框中，将 **运行设置** 选项设置为 **是**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-330">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
4. <span data-ttu-id="01a9e-331">根据需要，选择 **编辑** 以使当前页面可供编辑。</span><span class="sxs-lookup"><span data-stu-id="01a9e-331">Select **Edit** to make the current page editable, as required.</span></span>
5. <span data-ttu-id="01a9e-332">在左侧窗格的配置树中，选择 **BACS（UK 自定义）**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-332">In the configuration tree in the left pane, select **BACS (UK custom)**.</span></span>
6. <span data-ttu-id="01a9e-333">将 **运行草稿** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-333">Set the **Run Draft** option to **Yes**.</span></span>

    !["配置"页面上的"运行草稿"选项](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a><span data-ttu-id="01a9e-335">使用自定义 ER 格式处理供应商付款</span><span class="sxs-lookup"><span data-stu-id="01a9e-335">Process a vendor payment by using the custom ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a><span data-ttu-id="01a9e-336">设置电子付款方式</span><span class="sxs-lookup"><span data-stu-id="01a9e-336">Set up the electronic payment method</span></span>

<span data-ttu-id="01a9e-337">必须配置电子付款方式，以便使用自定义 ER 格式处理供应商付款。</span><span class="sxs-lookup"><span data-stu-id="01a9e-337">You must configure the electronic method of payment so that your custom ER format is used to process vendor payments.</span></span>

1. <span data-ttu-id="01a9e-338">转到 **应付帐款** \> **付款设置** \> **付款方式**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-338">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="01a9e-339">在 **付款方式 - 供应商** 页面中，在左侧窗格中选择 **电子** 付款方式。</span><span class="sxs-lookup"><span data-stu-id="01a9e-339">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="01a9e-340">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-340">Select **Edit**.</span></span>
4. <span data-ttu-id="01a9e-341">在 **文件格式** 快速选项卡上，将 **一般电子导出格式** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-341">On the **File format** FastTab, set the **General electronic export format** option to **Yes**.</span></span>
5. <span data-ttu-id="01a9e-342">在 **导出格式配置** 字段中，选择 **BACS（UK 自定义）** 格式配置。</span><span class="sxs-lookup"><span data-stu-id="01a9e-342">In the **Export format configuration** field, select the **BACS (UK custom)** format configuration.</span></span>

    ![付款方式 - 供应商页面](./media/er-quick-start2-method-of-payment2.png)

6. <span data-ttu-id="01a9e-344">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-344">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a><span data-ttu-id="01a9e-345">处理供应商付款</span><span class="sxs-lookup"><span data-stu-id="01a9e-345">Process a vendor payment</span></span>

1. <span data-ttu-id="01a9e-346">转到 **应付帐款** \> **付款** \> **供应商付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-346">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="01a9e-347">在 **供应商付款日记帐** 页面上，选择您先前创建的付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="01a9e-347">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="01a9e-348">选择 **行**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-348">Select **Lines**.</span></span>
4. <span data-ttu-id="01a9e-349">在 **供应商付款** 页面中网格上方，选择 **付款状态** \> **无**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-349">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="01a9e-350">选择 **生成付款**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-350">Select **Generate payment**.</span></span>
6. <span data-ttu-id="01a9e-351">在 **生成付款** 对话框中，输入以下信息：</span><span class="sxs-lookup"><span data-stu-id="01a9e-351">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="01a9e-352">在 **付款方式** 字段中，选择 **电子**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-352">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="01a9e-353">在 **银行帐户** 字段中，选择 **GBSI OPER**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-353">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="01a9e-354">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-354">Select **OK**.</span></span>
8. <span data-ttu-id="01a9e-355">在 **电子报表参数** 对话框中，将 **打印控制报表** 选项设置为 **是**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-355">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="01a9e-356">除了付款文件，只能生成控制报表。</span><span class="sxs-lookup"><span data-stu-id="01a9e-356">In addition to the payment file, you can generate only the control report.</span></span>

9. <span data-ttu-id="01a9e-357">下载 zip 文件，然后从中提取以下文件：</span><span class="sxs-lookup"><span data-stu-id="01a9e-357">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="01a9e-358">Excel 格式的控制报表</span><span class="sxs-lookup"><span data-stu-id="01a9e-358">The control report in Excel format</span></span>
    - <span data-ttu-id="01a9e-359">TXT 格式的付款文件</span><span class="sxs-lookup"><span data-stu-id="01a9e-359">The payment file in TXT format</span></span>

        <span data-ttu-id="01a9e-360">请注意，按照自定义 ER 格式的结构，生成的文件中的付款行现在以为处理了其付款的供应商的银行帐户[输入的](#DefineSWIFTCode) SWIFT 代码[开始](#PositionSWIFTCode)。</span><span class="sxs-lookup"><span data-stu-id="01a9e-360">Notice that, in accordance with the structure of your custom ER format, the payment line in the generated file now [starts](#PositionSWIFTCode) with the SWIFT code that was [entered](#DefineSWIFTCode) for the bank account of the vendor whose payment has been processed.</span></span>

        ![TXT 格式的付款文件](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a><span data-ttu-id="01a9e-362">导入标准 ER 格式配置的新版本</span><span class="sxs-lookup"><span data-stu-id="01a9e-362">Import new versions of the standard ER format configurations</span></span>

<span data-ttu-id="01a9e-363">对于本部分中显示的示例，您将收到有关知识库文章 [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046) 的通知。</span><span class="sxs-lookup"><span data-stu-id="01a9e-363">For the example that is shown in this section, you receive a notification about Knowledge Base article [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span></span> <span data-ttu-id="01a9e-364">此通知通知您 Microsoft 已发布的 **BACS (UK)** ER 格式新版本。</span><span class="sxs-lookup"><span data-stu-id="01a9e-364">This notification informs you about the new version of the **BACS (UK)** ER format that has been published by Microsoft.</span></span> <span data-ttu-id="01a9e-365">除了控制报表，用户还可以在处理供应商付款时通过这个新版本生成付款通知报表和出席单报表。</span><span class="sxs-lookup"><span data-stu-id="01a9e-365">In addition to the control report, this new version lets users generate the payment advice report and the attending note report while a vendor payment is being processed.</span></span> <span data-ttu-id="01a9e-366">您希望开始使用此功能。</span><span class="sxs-lookup"><span data-stu-id="01a9e-366">You want to start to use that functionality.</span></span>

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a><span data-ttu-id="01a9e-367">导入标准 ER 配置的新版本</span><span class="sxs-lookup"><span data-stu-id="01a9e-367">Import new versions of the standard ER configurations</span></span>

<span data-ttu-id="01a9e-368">若要向当前 Finance 实例添加新 ER 配置版本，必须从已配置的的 ER [存储库](general-electronic-reporting.md#Repository)导入这些配置。</span><span class="sxs-lookup"><span data-stu-id="01a9e-368">To add new versions of the ER configurations to the current Finance instance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that you've configured.</span></span>

1. <span data-ttu-id="01a9e-369">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-369">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="01a9e-370">在 **本地化配置** 页面的 **配置提供程序** 部分中，选择 **Microsoft** 磁贴，然后选择 **存储库** 查看 Microsoft 提供程序的存储库列表。</span><span class="sxs-lookup"><span data-stu-id="01a9e-370">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="01a9e-371">在 **配置存储库** 页，选择 **全球** 类型的存储库，然后选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-371">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="01a9e-372">如果提示您进行授权以连接到 Regulatory Configuration Service，请按照授权说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="01a9e-372">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="01a9e-373">在 **配置存储库** 页面左侧窗格的配置树中，选择 **BACS (UK)** 格式配置。</span><span class="sxs-lookup"><span data-stu-id="01a9e-373">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="01a9e-374">在 **版本** 快速选项卡上，选择所选 ER 格式配置的版本 **3.3**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-374">On the **Versions** FastTab, select version **3.3** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="01a9e-375">选择 **导入** 将所选版本从全局存储库下载到当前 Finance 实例。</span><span class="sxs-lookup"><span data-stu-id="01a9e-375">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![配置存储库页面](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> <span data-ttu-id="01a9e-377">如果在访问[全球存储库](er-download-configurations-global-repo.md)时遇到问题，可改为从 LCS [下载配置](download-electronic-reporting-configuration-lcs.md)。</span><span class="sxs-lookup"><span data-stu-id="01a9e-377">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from LCS instead.</span></span>

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a><span data-ttu-id="01a9e-378">查看导入的 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="01a9e-378">Review the imported ER format configurations</span></span>

1. <span data-ttu-id="01a9e-379">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-379">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="01a9e-380">在 **本地化配置** 页面的 **配置** 部分中，选择 **报告配置** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="01a9e-380">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="01a9e-381">在 **配置** 页的左侧窗格的配置树中，展开 **付款模型**，然后选择 **BACS (UK)**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-381">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span>
4. <span data-ttu-id="01a9e-382">在 **版本** 快速选项卡中，选择版本 **3.3**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-382">On the **Versions** FastTab, select version **3.3**.</span></span>
5. <span data-ttu-id="01a9e-383">选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-383">Select **Designer**.</span></span>
6. <span data-ttu-id="01a9e-384">在 **格式设计器** 页面中，展开 **BACSReportsFolder** 格式元素。</span><span class="sxs-lookup"><span data-stu-id="01a9e-384">On the **Format designer** page, expand the **BACSReportsFolder** format element.</span></span>
7.  <span data-ttu-id="01a9e-385">请注意，版本 3.3 中包含 **PaymentAdviceReport** 格式元素，用于在处理供应商付款时生成付款通知报表。</span><span class="sxs-lookup"><span data-stu-id="01a9e-385">Notice that version 3.3 contains the **PaymentAdviceReport** format element that is used to generate a payment advice report when a vendor payment is processed.</span></span>

    ![ER Operations 设计器中的 PaymentAdviceReport 格式元素](./media/er-quick-start2-imported-solution2.png)

8. <span data-ttu-id="01a9e-387">关闭设计器页面。</span><span class="sxs-lookup"><span data-stu-id="01a9e-387">Close the designer page.</span></span>

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a><span data-ttu-id="01a9e-388">在自定义格式中采用在所导入格式的新版本中进行的更改</span><span class="sxs-lookup"><span data-stu-id="01a9e-388">Adopt the changes in the new version of an imported format in a custom format</span></span>

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a><span data-ttu-id="01a9e-389">完成自定义格式的当前草稿版本</span><span class="sxs-lookup"><span data-stu-id="01a9e-389">Complete the current draft version of a custom format</span></span>

<span data-ttu-id="01a9e-390">如果要保持自定义格式的当前状态，请通过将状态从 **草稿** 更改为 **已完成** 来完成草稿版本 1.1.1。</span><span class="sxs-lookup"><span data-stu-id="01a9e-390">If you want to keep the current state of your custom format, complete the draft version 1.1.1 by changing its status from **Draft** to **Completed**.</span></span>

1. <span data-ttu-id="01a9e-391">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-391">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="01a9e-392">在 **本地化配置** 页面的 **配置** 部分中，选择 **报告配置** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="01a9e-392">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="01a9e-393">在 **配置** 页的左侧窗格的配置树中，展开 **付款模型**，展开 **BACS (UK)**，然后选择 **BACS（UK 自定义）**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-393">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, expand **BACS (UK)**, and then select **BACS (UK custom)**.</span></span>
4. <span data-ttu-id="01a9e-394">在 **版本** 快速选项卡上，选择 **更改状态** \> **完成**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-394">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="01a9e-395">版本 1.1.1 的状态将从 **草稿** 更改为 **已完成**，并且该版本变为只读。</span><span class="sxs-lookup"><span data-stu-id="01a9e-395">The status of version 1.1.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="01a9e-396">已添加了一个新的可编辑版本 1.1.2，其状态为 **草稿**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-396">A new editable version, 1.1.2, has been added and has a status of **Draft**.</span></span> <span data-ttu-id="01a9e-397">您可以使用此版本在自定义 ER 格式中进行进一步的更改。</span><span class="sxs-lookup"><span data-stu-id="01a9e-397">You can use this version to make further changes in your custom ER format.</span></span>

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a><span data-ttu-id="01a9e-398">将自定义格式重定为新基本版本</span><span class="sxs-lookup"><span data-stu-id="01a9e-398">Rebase a custom format to a new base version</span></span>

<span data-ttu-id="01a9e-399">若要开始在自定义中使用 **BACS (UK)** 格式版本 3.3 的新功能，必须更改自定义配置 **BACS（UK 自定义）** 的基本基本配置版本。</span><span class="sxs-lookup"><span data-stu-id="01a9e-399">To start to use the new functionality of version 3.3 of the **BACS (UK)** format in your customization, you must change the base configuration version for the custom configuration, **BACS (UK custom)**.</span></span> <span data-ttu-id="01a9e-400">此流程称为[重定基本值](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase)。</span><span class="sxs-lookup"><span data-stu-id="01a9e-400">This process is known as [rebasing](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span></span> <span data-ttu-id="01a9e-401">使用 **BACS (UK)** 版本 3.3，而不是版本 1.1。</span><span class="sxs-lookup"><span data-stu-id="01a9e-401">Instead of version 1.1 of **BACS (UK)**, use version 3.3.</span></span>

1. <span data-ttu-id="01a9e-402">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-402">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="01a9e-403">在 **配置** 页的左侧窗格的配置树中，展开 **付款模型**，然后选择 **BACS（UK 自定义）**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-403">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="01a9e-404">在 **版本** 快速选项卡上，选择版本 **1.1.2**，然后选择 **重定**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-404">On the **Versions** FastTab, select version **1.1.2**, and then select **Rebase**.</span></span>
4. <span data-ttu-id="01a9e-405">在 **重定** 对话框的 **目标** 字段中，选择基本配置的版本 **3.3** 将其作为新基础应用，并用于更新配置。</span><span class="sxs-lookup"><span data-stu-id="01a9e-405">In the **Rebase** dialog box, in the **Target version** field, select version **3.3** of the base configuration to apply it as the new base and use it to update the configuration.</span></span>

    ![“重定基本版本”对话框](./media/er-quick-start2-rebase1.png)

5. <span data-ttu-id="01a9e-407">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-407">Select **OK**.</span></span>
6. <span data-ttu-id="01a9e-408">请注意，草稿版本的版本号已经从 **1.1.2** 更改为 **3.3.2** 以体现基本版本中的更改。</span><span class="sxs-lookup"><span data-stu-id="01a9e-408">Notice that the number of the draft version has been changed from **1.1.2** to **3.3.2** to reflect the change in the base version.</span></span>

    <span data-ttu-id="01a9e-409">在合并自定义版本和新基本版本时，可能会发现一些冲突，因为不能自动合并格式更改。</span><span class="sxs-lookup"><span data-stu-id="01a9e-409">When the custom version and a new base version are merged, some conflicts might be discovered because of format changes that can't be merged automatically.</span></span>

    ![“配置”页中存在冲突的重定后配置](./media/er-quick-start2-rebase2.png)

    <span data-ttu-id="01a9e-411">如果发现了冲突，必须在格式设计器中手动解决。</span><span class="sxs-lookup"><span data-stu-id="01a9e-411">If conflicts are discovered, they must be manually resolved in the format designer.</span></span>

7. <span data-ttu-id="01a9e-412">在 **版本** 快速选项卡中，选择版本 **3.3.2**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-412">On the **Versions** FastTab, select version **3.3.2**.</span></span>
8. <span data-ttu-id="01a9e-413">选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-413">Select **Designer**.</span></span>
9. <span data-ttu-id="01a9e-414">在 **格式设计器** 页面的 **详细信息** 快速选项卡上，选择重定冲突记录，然后选择 **应用基值**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-414">On the **Format designer** page, on the **Details** FastTab, select a rebase conflict record, and then select **Apply base value**.</span></span>

    ![ER Operations 设计器中的重定冲突记录](./media/er-quick-start2-rebase3.png)

10. <span data-ttu-id="01a9e-416">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-416">Select **Save**.</span></span>

    <span data-ttu-id="01a9e-417">**详细信息** 快速选项卡中不应再显示重定冲突记录。</span><span class="sxs-lookup"><span data-stu-id="01a9e-417">The rebase conflict record should no longer appear on the **Details** FastTab.</span></span>

    ![ER Operations 设计器中已解决冲突](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > <span data-ttu-id="01a9e-419">您通过确认必须在此 ER 格式中使用基本模型版本 3 解决了冲突。</span><span class="sxs-lookup"><span data-stu-id="01a9e-419">You resolved the conflict by confirming that version 3 of the base model must be used in this ER format.</span></span>

11. <span data-ttu-id="01a9e-420">展开 **BACSReportsFolder** \> **文件** \> **transactions** \> **transaction**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-420">Expand **BACSReportsFolder** \> **file** \> **transactions** \> **transaction**.</span></span>
12. <span data-ttu-id="01a9e-421">在 **映射** 选项卡上，注意自定义 ER 格式版本 3.3.2 中同时包含您的自定义（**vendBankSWIFT** 格式元素及其绑定）和 Microsoft 提供的基本 ER 格式版本 3.3 的新功能（**PaymentAdviceReport** 格式元素及其嵌套元素和配置的绑定）。</span><span class="sxs-lookup"><span data-stu-id="01a9e-421">On the **Mapping** tab, notice that version 3.3.2 of your custom ER format contains both your customization (the **vendBankSWIFT** format element and its binding) and the new functionality of version 3.3 of the base ER format that was provided by Microsoft (the **PaymentAdviceReport** format element together with its nested elements and configured bindings).</span></span> <span data-ttu-id="01a9e-422">您单击了几次鼠标通过将新基本版本的修改与自定义合并，采用了这些修改。</span><span class="sxs-lookup"><span data-stu-id="01a9e-422">In just a few mouse clicks, you adopted the modifications of a new base version by merging them with your customization.</span></span>

    ![ER Operations 设计器中合并后的格式](./media/er-quick-start2-rebase5.png)

13. <span data-ttu-id="01a9e-424">关闭设计器页面。</span><span class="sxs-lookup"><span data-stu-id="01a9e-424">Close the designer page.</span></span>

> [!NOTE]
> <span data-ttu-id="01a9e-425">重定操作可逆。</span><span class="sxs-lookup"><span data-stu-id="01a9e-425">The rebase action is reversible.</span></span> <span data-ttu-id="01a9e-426">若要取消此重定，请在 **版本** 快速选项卡上选择 **BACS（UK 自定义）** 格式版本 **1.1.1**，然后选择 **获取此版本**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-426">To cancel this rebase, select version **1.1.1** of the **BACS (UK custom)** format on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="01a9e-427">然后将把版本 3.3.2 重新编号为 1.1.2，而草稿版本 1.1.2 的内容将与版本 1.1.1 的内容匹配。</span><span class="sxs-lookup"><span data-stu-id="01a9e-427">Version 3.3.2 will then be renumbered 1.1.2, and the content of draft version 1.1.2 will match the content of version 1.1.1.</span></span>

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a><span data-ttu-id="01a9e-428">使用重定 ER 格式处理供应商付款</span><span class="sxs-lookup"><span data-stu-id="01a9e-428">Process a vendor payment by using a rebased ER format</span></span>

1. <span data-ttu-id="01a9e-429">转到 **应付帐款** \> **付款** \> **供应商付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-429">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="01a9e-430">在 **供应商付款日记帐** 页面上，选择您先前创建的付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="01a9e-430">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="01a9e-431">选择 **行**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-431">Select **Lines**.</span></span>
4. <span data-ttu-id="01a9e-432">在 **供应商付款** 页面中网格上方，选择 **付款状态** \> **无**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-432">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="01a9e-433">选择 **生成付款**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-433">Select **Generate payment**.</span></span>
6. <span data-ttu-id="01a9e-434">在 **生成付款** 对话框中，输入以下信息：</span><span class="sxs-lookup"><span data-stu-id="01a9e-434">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="01a9e-435">在 **付款方式** 字段中，选择 **电子**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-435">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="01a9e-436">在 **银行帐户** 字段中，选择 **GBSI OPER**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-436">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="01a9e-437">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-437">Select **OK**.</span></span>
8. <span data-ttu-id="01a9e-438">在 **电子报表参数** 对话框中，输入以下信息：</span><span class="sxs-lookup"><span data-stu-id="01a9e-438">In the **Electronic report parameters** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="01a9e-439">将 **打印控制报表** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-439">Set the **Print control report** option to **Yes**.</span></span>
    - <span data-ttu-id="01a9e-440">将 **打印付款通知** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-440">Set the **Print payment advice** option to **Yes**.</span></span>

    ![电子报表参数对话框](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > <span data-ttu-id="01a9e-442">除了付款文件，现在还可以生成控制报表和付款通知报表。</span><span class="sxs-lookup"><span data-stu-id="01a9e-442">In addition to the payment file, you can now generate both the control report and the payment advice report.</span></span>

9. <span data-ttu-id="01a9e-443">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="01a9e-443">Select **OK**.</span></span>
10. <span data-ttu-id="01a9e-444">下载 zip 文件，然后从中提取以下文件：</span><span class="sxs-lookup"><span data-stu-id="01a9e-444">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="01a9e-445">Excel 格式的控制报表</span><span class="sxs-lookup"><span data-stu-id="01a9e-445">The control report in Excel format</span></span>
    - <span data-ttu-id="01a9e-446">Excel 格式的付款通知报表</span><span class="sxs-lookup"><span data-stu-id="01a9e-446">The payment advice report in Excel format</span></span>

        ![Excel 格式的付款通知报表](./media/er-quick-start2-payment-advice-report.png)

    - <span data-ttu-id="01a9e-448">TXT 格式的付款文件</span><span class="sxs-lookup"><span data-stu-id="01a9e-448">The payment file in TXT format</span></span>

        <span data-ttu-id="01a9e-449">请注意，生成的文件中的付款行以为处理了其付款的供应商的银行帐户输入的 SWIFT 代码开始。</span><span class="sxs-lookup"><span data-stu-id="01a9e-449">Notice that the payment line in the generated file starts  with the SWIFT code that was entered for the bank account of a vendor whose payment has been processed.</span></span>

        ![TXT 格式的付款文件](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a><span data-ttu-id="01a9e-451">其他资源</span><span class="sxs-lookup"><span data-stu-id="01a9e-451">Additional resources</span></span>

- [<span data-ttu-id="01a9e-452">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="01a9e-452">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="01a9e-453">从 Lifecycle Services 下载 ER 配置</span><span class="sxs-lookup"><span data-stu-id="01a9e-453">Download ER configurations from Lifecycle Services</span></span>](download-electronic-reporting-configuration-lcs.md)
- [<span data-ttu-id="01a9e-454">从 Configuration Service 的全局存储库下载 ER 配置</span><span class="sxs-lookup"><span data-stu-id="01a9e-454">Download ER configurations from Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)

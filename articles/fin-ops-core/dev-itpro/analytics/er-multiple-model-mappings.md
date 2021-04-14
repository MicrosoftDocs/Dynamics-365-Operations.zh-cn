---
title: 管理单个模型根的多个派生映射
description: 本主题说明如何管理为单个模型根配置的多个派生映射。
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a774a0edf00a17be674b7a1bb07f6494e90554c3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743671"
---
# <a name="manage-several-derived-mappings-for-a-single-model-root"></a><span data-ttu-id="cb294-103">管理单个模型根的多个派生映射</span><span class="sxs-lookup"><span data-stu-id="cb294-103">Manage several derived mappings for a single model root</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb294-104">[电子报告 (ER)](general-electronic-reporting.md) 数据[模型](general-electronic-reporting.md#data-model-and-model-mapping-components)组件在每个配置的 ER [格式](general-electronic-reporting.md#FormatComponentOutbound)组件中用作生成传出文档的数据源。</span><span class="sxs-lookup"><span data-stu-id="cb294-104">An [Electronic reporting (ER)](general-electronic-reporting.md) data [model](general-electronic-reporting.md#data-model-and-model-mapping-components) component is used in every configured ER [format](general-electronic-reporting.md#FormatComponentOutbound) component as the data source to generate outbound documents.</span></span> <span data-ttu-id="cb294-105">要描述单个业务域，请配置具有多个根定义的数据模型组件。</span><span class="sxs-lookup"><span data-stu-id="cb294-105">To describe a single business domain, configure a data model component that has many root definitions.</span></span> 

<span data-ttu-id="cb294-106">每个根定义让您可以最适合特定报告目的的方式表示该域的数据。</span><span class="sxs-lookup"><span data-stu-id="cb294-106">Every root definition lets you represent data of that domain in the way that is best suited to specific reporting purposes.</span></span> <span data-ttu-id="cb294-107">对于每个根定义，您可以将一个 ER [模型映射](general-electronic-reporting.md#data-model-and-model-mapping-components)组件配置为数据模型的 Microsoft Dynamics 365 Finance 特定实现。</span><span class="sxs-lookup"><span data-stu-id="cb294-107">For every root definition, you can configure an ER [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component as the Microsoft Dynamics 365 Finance–specific implementation of your data model.</span></span> <span data-ttu-id="cb294-108">通过这种方式，您将描述在运行时数据模型如何填充。</span><span class="sxs-lookup"><span data-stu-id="cb294-108">In this way, you describe how your data model will be filled in at runtime.</span></span>

<span data-ttu-id="cb294-109">ER 模型映射组件可以放在 ER 数据模型[配置](general-electronic-reporting.md#Configuration)和 ER 模型映射配置中。</span><span class="sxs-lookup"><span data-stu-id="cb294-109">ER model mapping components can reside in ER data model [configurations](general-electronic-reporting.md#Configuration) and ER model mapping configurations.</span></span> <span data-ttu-id="cb294-110">单个 ER 配置可以包含多个映射组件，每个映射组件针对单个根定义进行配置。</span><span class="sxs-lookup"><span data-stu-id="cb294-110">A single ER configuration can contain many mapping components, each of which is configured for a single root definition.</span></span> <span data-ttu-id="cb294-111">或者，单个 ER 配置可以仅包含为单个根定义配置的一个映射组件。</span><span class="sxs-lookup"><span data-stu-id="cb294-111">Alternatively, a single ER configuration can contain just one mapping component that is configured for a single root definition.</span></span>

<span data-ttu-id="cb294-112">多个配置提供程序可能会为同一个 ER 数据模型提供 ER 模型映射配置。</span><span class="sxs-lookup"><span data-stu-id="cb294-112">Many configuration providers might offer ER model mapping configurations for the same ER data model.</span></span> <span data-ttu-id="cb294-113">这些模型映射配置可能包含不同根定义的映射组件。</span><span class="sxs-lookup"><span data-stu-id="cb294-113">Those model mapping configurations might contain mapping components for different root definitions.</span></span> <span data-ttu-id="cb294-114">您可以对一个[提供程序](general-electronic-reporting.md#Provider)提供的一个根定义使用一个模型映射，对另一个提供程序提供的另一个根定义使用一个模型映射。</span><span class="sxs-lookup"><span data-stu-id="cb294-114">You might use a model mapping for one root definition that is offered by one [provider](general-electronic-reporting.md#Provider) and use a model mapping for another root definition that is offered by another provider.</span></span>

<span data-ttu-id="cb294-115">本主题中的过程说明当 ER 模型映射配置包含为同一个根定义配置的不同模型映射组件时，如何管理 ER 数据模型的多个 ER 模型映射配置。</span><span class="sxs-lookup"><span data-stu-id="cb294-115">The procedures in this topic explain how to manage multiple ER model mapping configurations of an ER data model when they contain different model mapping components configured for the same root definition.</span></span> 

<span data-ttu-id="cb294-116">要完成本主题中的过程，您必须被分配系统管理员或电子报告开发人员角色。</span><span class="sxs-lookup"><span data-stu-id="cb294-116">To complete the procedures in this topic, you must be assigned to the System administrator or Electronic reporting developer role.</span></span>

<span data-ttu-id="cb294-117">以下所有过程均可在 USMF 公司中完成。</span><span class="sxs-lookup"><span data-stu-id="cb294-117">All the following procedures can be done in the USMF company.</span></span> <span data-ttu-id="cb294-118">无需进行编码。</span><span class="sxs-lookup"><span data-stu-id="cb294-118">No coding is required.</span></span>

## <a name="configure-the-er-framework"></a><span data-ttu-id="cb294-119">配置 ER 框架</span><span class="sxs-lookup"><span data-stu-id="cb294-119">Configure the ER framework</span></span>

<span data-ttu-id="cb294-120">作为具有电子报告开发人员角色的用户，在使用 ER 框架生成业务文档之前，请先[配置最小 ER 参数集](er-quick-start2-customize-report.md#ConfigureFramework)。</span><span class="sxs-lookup"><span data-stu-id="cb294-120">As a user in the Electronic reporting developer role, [configure the minimal set](er-quick-start2-customize-report.md#ConfigureFramework) of ER parameters before you use the ER framework to generate business documents.</span></span>

## <a name="import-the-standard-er-format-configurations"></a><span data-ttu-id="cb294-121">导入标准 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="cb294-121">Import the standard ER format configurations</span></span>

<span data-ttu-id="cb294-122">若要向当前 Finance 实例添加标准 ER 配置，必须从为该实例配置的 ER 存储库中导入这些配置。</span><span class="sxs-lookup"><span data-stu-id="cb294-122">To add the standard ER configurations to your current instance of Finance, you must import them from the ER repository that was configured for that instance.</span></span> <span data-ttu-id="cb294-123">按照[从配置服务的全局存储库下载 ER 配置](er-download-configurations-global-repo.md)中的步骤导入以下 ER 格式配置：</span><span class="sxs-lookup"><span data-stu-id="cb294-123">Follow the steps in [Download ER configurations from the Global repository of Configuration service](er-download-configurations-global-repo.md) to import the following ER format configurations:</span></span>

- <span data-ttu-id="cb294-124">**普通发票 (Excel)**，版本 220.106</span><span class="sxs-lookup"><span data-stu-id="cb294-124">**Free text invoice (Excel)**, version 220.106</span></span>
- <span data-ttu-id="cb294-125">**项目发票 (Excel)**，版本 226.27</span><span class="sxs-lookup"><span data-stu-id="cb294-125">**Project invoice (Excel)**, version 226.27</span></span>

## <a name="review-the-imported-er-configurations"></a><span data-ttu-id="cb294-126">查看导入的 ER 配置</span><span class="sxs-lookup"><span data-stu-id="cb294-126">Review the imported ER configurations</span></span>

1. <span data-ttu-id="cb294-127">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="cb294-127">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cb294-128">在 **本地化配置** 页面的 **配置** 部分中，选择 **报告配置** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="cb294-128">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="cb294-129">在 **配置** 页的左侧窗格的配置树中，展开 **发票模型**。</span><span class="sxs-lookup"><span data-stu-id="cb294-129">On the **Configurations** page, in the configuration tree in the left pane, expand **Invoice model**.</span></span>

    ![查看“配置”页上导入的配置](./media/er-multiple-model-mappings-image1.png)

4. <span data-ttu-id="cb294-131">查看 **普通发票 (Excel)** 格式：</span><span class="sxs-lookup"><span data-stu-id="cb294-131">Review the **Free text invoice (Excel)** format:</span></span>

    1. <span data-ttu-id="cb294-132">在左侧窗格的配置树中，选择 **普通发票 (Excel)**。</span><span class="sxs-lookup"><span data-stu-id="cb294-132">In the configuration tree in the left pane, select **Free text invoice (Excel)**.</span></span>
    2. <span data-ttu-id="cb294-133">在操作窗格上，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="cb294-133">On the Action Pane, select **Designer**.</span></span>
    3. <span data-ttu-id="cb294-134">在 **格式设计器** 页上的 **映射** 选项卡上，在数据源列表中，选择 **模型**。</span><span class="sxs-lookup"><span data-stu-id="cb294-134">On the **Format designer** page, on the **Mapping** tab, in the data sources list, select **Model**.</span></span>
    4. <span data-ttu-id="cb294-135">选择 **查看**。</span><span class="sxs-lookup"><span data-stu-id="cb294-135">Select **View**.</span></span>
    
       <span data-ttu-id="cb294-136">当前 ER 格式配置为使用 **发票模型** 的 **InvoiceCustomer** 根定义。</span><span class="sxs-lookup"><span data-stu-id="cb294-136">Thecurrent ER format is configured to use the **InvoiceCustomer** root definition of **Invoice model**.</span></span> <span data-ttu-id="cb294-137">当运行此格式并调用 **模型** 数据源时，为 **InvoiceCustomer** 根定义配置的模型映射用于访问应用程序数据和填充数据模型。</span><span class="sxs-lookup"><span data-stu-id="cb294-137">When this format is run, and the **Model** data source is called, the model mapping that is configured for the **InvoiceCustomer** root definition is used to access application data and fill in the data model.</span></span>

        ![查看“格式设计器”页上的模型数据源](./media/er-multiple-model-mappings-image2.png)

    6. <span data-ttu-id="cb294-139">关闭 **格式设计器** 页。</span><span class="sxs-lookup"><span data-stu-id="cb294-139">Close the **Format designer** page.</span></span>

5. <span data-ttu-id="cb294-140">查看 **发票模型映射** 配置的内容：</span><span class="sxs-lookup"><span data-stu-id="cb294-140">Review the content of the **Invoice model mapping** configuration:</span></span>

    1. <span data-ttu-id="cb294-141">在左侧窗格的配置树中，选择 **发票模型映射**。</span><span class="sxs-lookup"><span data-stu-id="cb294-141">In the configuration tree in the left pane, select **Invoice model mapping**.</span></span>
    2. <span data-ttu-id="cb294-142">在操作窗格上，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="cb294-142">On the Action Pane, select **Designer**.</span></span>
    3. <span data-ttu-id="cb294-143">在 **模型到数据源映射** 页上，注意当前的 ER 模型映射配置包含几个模型映射组件：</span><span class="sxs-lookup"><span data-stu-id="cb294-143">On the **Model to datasource mapping** page, notice that the current ER model mapping configuration contains several model mapping components:</span></span>

        + <span data-ttu-id="cb294-144">**客户发票** 模型映射是为 **发票模型** 的 **InvoiceCustomer** 根定义配置的。</span><span class="sxs-lookup"><span data-stu-id="cb294-144">The **Customer Invoice** model mapping is configured for the **InvoiceCustomer** root definition of **Invoice model**.</span></span> <span data-ttu-id="cb294-145">因此，当 **普通发票 (Excel)** ER 格式运行时，可以选择此 ER 配置的 **客户发票** 模型映射来访问应用程序数据和填充数据模型。</span><span class="sxs-lookup"><span data-stu-id="cb294-145">Therefore, when the **Free text invoice (Excel)** ER format is run, the **Customer Invoice** model mapping of this ER configuration can be chosen to access application data and fill in the data model.</span></span>
        + <span data-ttu-id="cb294-146">**项目发票** 模型映射是为 **发票模型** 的 **InvoiceProject** 根定义配置的。</span><span class="sxs-lookup"><span data-stu-id="cb294-146">The **Project Invoice** model mapping is configured for the **InvoiceProject** root definition of **Invoice model**.</span></span> <span data-ttu-id="cb294-147">因此，当 **项目发票 (Excel)** ER 格式运行时，可以选择此 ER 配置的 **项目发票** 模型映射来访问应用程序数据和填充数据模型。</span><span class="sxs-lookup"><span data-stu-id="cb294-147">Therefore, when the **Project invoice (Excel)** ER format is run, the **Project Invoice** model mapping of this ER configuration can be chosen to access application data and fill in the data model.</span></span>

        ![“模型到数据源映射”页上的发票模型映射](./media/er-multiple-model-mappings-image3.png)

    4. <span data-ttu-id="cb294-149">关闭 **模型到数据源映射** 页。</span><span class="sxs-lookup"><span data-stu-id="cb294-149">Close the **Model to datasource mapping** page.</span></span>
    5. <span data-ttu-id="cb294-150">在 **版本** 快速选项卡上，选择 **删除** 删除此 ER 配置所有晚于 240.175 版本的版本。</span><span class="sxs-lookup"><span data-stu-id="cb294-150">On the **Versions** FastTab, select **Delete** to delete all versions of this ER configuration that are later than version 240.175.</span></span>

6. <span data-ttu-id="cb294-151">查看 **项目发票模型映射(RDP)** 配置的内容：</span><span class="sxs-lookup"><span data-stu-id="cb294-151">Review the content of the **Project invoice model mapping (RDP)** configuration:</span></span>

    1. <span data-ttu-id="cb294-152">在左侧窗格的配置树中，选择 **项目发票模型映射(RDP)**。</span><span class="sxs-lookup"><span data-stu-id="cb294-152">In the configuration tree in the left pane, select **Project invoice model mapping (RDP)**.</span></span>
    2. <span data-ttu-id="cb294-153">在操作窗格上，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="cb294-153">On the Action Pane, select **Designer**.</span></span>
    3. <span data-ttu-id="cb294-154">在 **模型到数据源映射** 页上，注意当前的 ER 模型映射配置包含 **InvoiceProject** 模型映射，并且此模型映射是为 **发票模型** 的 **InvoiceProject** 根定义配置的。</span><span class="sxs-lookup"><span data-stu-id="cb294-154">On the **Model to datasource mapping** page, notice that the current ER model mapping configuration contains the **InvoiceProject** model mapping, and that this model mapping is configured for the **InvoiceProject** root definition of **Invoice model**.</span></span> <span data-ttu-id="cb294-155">当 **项目发票 (Excel)** ER 格式运行时，选择此 ER 配置的 **InvoiceProject** 模型映射来访问应用程序数据和填充数据模型。</span><span class="sxs-lookup"><span data-stu-id="cb294-155">When the **Project invoice (Excel)** ER format is run, select the **InvoiceProject** model mapping of this ER configuration to access application data and fill in the data model.</span></span>

        ![“模型到数据源映射”页上的项目发票模型映射](./media/er-multiple-model-mappings-image4.png)

    4. <span data-ttu-id="cb294-157">关闭 **模型到数据源映射** 页。</span><span class="sxs-lookup"><span data-stu-id="cb294-157">Close the **Model to datasource mapping** page.</span></span>
    5. <span data-ttu-id="cb294-158">在 **版本** 快速选项卡上，选择 **删除** 删除此 ER 配置所有晚于 226.35 版本的版本。</span><span class="sxs-lookup"><span data-stu-id="cb294-158">On the **Versions** FastTab, select **Delete** to delete all versions of this ER configuration that are later than version 226.35.</span></span>

## <a name="customize-the-imported-er-configurations"></a><span data-ttu-id="cb294-159">自定义导入的 ER 配置</span><span class="sxs-lookup"><span data-stu-id="cb294-159">Customize the imported ER configurations</span></span>

<span data-ttu-id="cb294-160">本节说明如何[自定义](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration) Microsoft 提供的模型映射。</span><span class="sxs-lookup"><span data-stu-id="cb294-160">This section explains how to [customize](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration) the model mappings that are provided by Microsoft.</span></span> <span data-ttu-id="cb294-161">例如，可能需要自定义来实现您的自定义逻辑或添加缺少的绑定。</span><span class="sxs-lookup"><span data-stu-id="cb294-161">For example, customization might be required to implement your custom logic or add missing bindings.</span></span>

### <a name="customize-the-invoice-model-mapping-configuration"></a><span data-ttu-id="cb294-162">自定义发票模型映射配置</span><span class="sxs-lookup"><span data-stu-id="cb294-162">Customize the Invoice model mapping configuration</span></span>

1. <span data-ttu-id="cb294-163">在 **配置** 页面上，在左侧窗格的配置树中，选择 **发票模型映射**。</span><span class="sxs-lookup"><span data-stu-id="cb294-163">On the **Configurations** page, in the configuration tree in the left pane, select **Invoice model mapping**.</span></span>
2. <span data-ttu-id="cb294-164">在操作窗格中选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="cb294-164">On the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="cb294-165">在 **创建配置** 下拉对话框的 **新建** 字段中，选择 **从名称派生: 发票模型映射, Microsoft**。</span><span class="sxs-lookup"><span data-stu-id="cb294-165">In the **Create configuration** drop-down dialog box, in the **New** field, select **Derive from Name: Invoice model mapping, Microsoft**.</span></span>
4. <span data-ttu-id="cb294-166">在 **名称** 字段中，输入 **发票模型映射 Litware**。</span><span class="sxs-lookup"><span data-stu-id="cb294-166">In the **Name** field, enter **Invoice model mapping Litware**.</span></span>
5. <span data-ttu-id="cb294-167">选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="cb294-167">Select **Create configuration**.</span></span>
6. <span data-ttu-id="cb294-168">将派生映射的[草稿](general-electronic-reporting.md#component-versioning)版本[标记](er-quick-start2-customize-report.md#MarkFormatRunnable)为可以在运行时使用：</span><span class="sxs-lookup"><span data-stu-id="cb294-168">[Mark](er-quick-start2-customize-report.md#MarkFormatRunnable) the [draft](general-electronic-reporting.md#component-versioning) version of the derived mapping as available for use at runtime:</span></span>

    1. <span data-ttu-id="cb294-169">在操作窗格的 **配置** 选项卡上，在 **高级设置** 组中，选择 **用户参数**。</span><span class="sxs-lookup"><span data-stu-id="cb294-169">On the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
    2. <span data-ttu-id="cb294-170">在 **使用参数** 对话框中，将 **运行设置** 选项设置为 **是**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="cb294-170">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
    3. <span data-ttu-id="cb294-171">根据需要，选择 **编辑** 使页面可供编辑。</span><span class="sxs-lookup"><span data-stu-id="cb294-171">Select **Edit** to make the page editable, as required.</span></span>
    4. <span data-ttu-id="cb294-172">对于配置树中当前选择的 **发票模型映射 Litware** 配置，将 **运行草稿** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="cb294-172">For the **Invoice model mapping Litware** configuration that is currently selected in the configuration tree, set the **Run Draft** option to **Yes**.</span></span>

7. <span data-ttu-id="cb294-173">在操作窗格上，选择 **设计器** 查看此配置的模型映射。</span><span class="sxs-lookup"><span data-stu-id="cb294-173">On the Action Pane, select **Designer** to review the model mappings of this configuration.</span></span>

    ![查看“模型到数据源映射”页上的发票模型映射](./media/er-multiple-model-mappings-image5.png)

    > [!TIP]
    > <span data-ttu-id="cb294-175">现在，您可以在设计器中打开此 ER 配置的任何 ER 模型映射组件，来配置您的自定义逻辑。</span><span class="sxs-lookup"><span data-stu-id="cb294-175">You can now open any of the ER model mapping components of this ER configuration in the designer to configure your custom logic.</span></span> <span data-ttu-id="cb294-176">有关详细信息，请参阅[自定义模型映射配置](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration)。</span><span class="sxs-lookup"><span data-stu-id="cb294-176">For more information, see [Customize the model mapping configuration](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration).</span></span>

8. <span data-ttu-id="cb294-177">关闭 **模型到数据源映射** 页。</span><span class="sxs-lookup"><span data-stu-id="cb294-177">Close the **Model to datasource mapping** page.</span></span>

<span data-ttu-id="cb294-178">现在，您有 **发票模型映射** 和 **发票模型映射 Litware** 配置，每个配置都有为 **InvoiceCustomer** 根定义配置的模型映射。</span><span class="sxs-lookup"><span data-stu-id="cb294-178">You now have **Invoice model mapping** and **Invoice model mapping Litware** configurations, each of which has a model mapping that is configured for the **InvoiceCustomer** root definition.</span></span> <span data-ttu-id="cb294-179">明确指定其中一个模型映射作为任何 ER 格式所使用的默认模型映射，如包含具有 **InvoiceCustomer** 根定义的模型数据源的 **普通发票 (Excel)** 格式。</span><span class="sxs-lookup"><span data-stu-id="cb294-179">Explicitly assign one of the model mappings as the default model mapping that is used by any of the ER formats, such as the **Free text invoice (Excel)** format that contains a model data source that has the **InvoiceCustomer** root definition.</span></span> <span data-ttu-id="cb294-180">否则，当您运行、编辑或验证其中一个 ER 格式时，将引发以下异常，通知您未明确分配默认模型映射：</span><span class="sxs-lookup"><span data-stu-id="cb294-180">Otherwise, when you run, edit, or validate one of the ER formats, the following exception is thrown to notify you that no default model mapping has been explicitly assigned:</span></span>
 
> <span data-ttu-id="cb294-181">配置 \<configuration names separated by commas\> 中的“\<model name\> (\<root descriptor\>)”数据模型存在多个模型映射。</span><span class="sxs-lookup"><span data-stu-id="cb294-181">More than one model mapping exists for the '\<model name\> (\<root descriptor\>)' data model in the configurations \<configuration names separated by commas\>.</span></span> <span data-ttu-id="cb294-182">将其中一个配置设置为默认配置。</span><span class="sxs-lookup"><span data-stu-id="cb294-182">Set one of the configurations as default.</span></span>

![在“配置”页上打开格式进行编辑](./media/er-multiple-model-mappings-image6.gif)

### <a name="customize-the-project-invoice-model-mapping-rdp-configuration"></a><span data-ttu-id="cb294-184">自定义项目发票模型映射 (RDP) 配置</span><span class="sxs-lookup"><span data-stu-id="cb294-184">Customize the Project invoice model mapping (RDP) configuration</span></span>

1. <span data-ttu-id="cb294-185">在 **配置** 页面上，在左侧窗格的配置树中，选择 **项目发票模型映射 (RDP)**。</span><span class="sxs-lookup"><span data-stu-id="cb294-185">On the **Configurations** page, in the configuration tree in the left pane, select **Project invoice model mapping (RDP)**.</span></span>
2. <span data-ttu-id="cb294-186">在操作窗格中选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="cb294-186">On the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="cb294-187">在 **创建配置** 对话框的 **新建** 字段中，选择 **从名称派生: 项目发票模型映射 (RDP), Microsoft**。</span><span class="sxs-lookup"><span data-stu-id="cb294-187">In the **Create configuration** dialog box, in the **New** field, select **Derive from Name: Project invoice model mapping (RDP), Microsoft**.</span></span>
4. <span data-ttu-id="cb294-188">在 **名称** 字段中，输入 **项目发票模型映射 Litware**。</span><span class="sxs-lookup"><span data-stu-id="cb294-188">In the **Name** field, enter **Project invoice model mapping Litware**.</span></span>
5. <span data-ttu-id="cb294-189">选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="cb294-189">Select **Create configuration**.</span></span>
6. <span data-ttu-id="cb294-190">对于配置树中当前选择的 **项目发票模型映射 Litware** 配置，将 **运行草稿** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="cb294-190">For the **Project invoice model mapping Litware** configuration that is currently selected in the configuration tree, set the **Run Draft** option to **Yes**.</span></span>
7. <span data-ttu-id="cb294-191">在操作窗格上，选择 **设计器** 查看此配置的模型映射。</span><span class="sxs-lookup"><span data-stu-id="cb294-191">On the Action Pane, select **Designer** to review the model mappings of this configuration.</span></span>

    ![查看“模型到数据源映射”页上自定义的项目发票模型映射](./media/er-multiple-model-mappings-image7.png)

8. <span data-ttu-id="cb294-193">关闭 **模型到数据源映射** 页。</span><span class="sxs-lookup"><span data-stu-id="cb294-193">Close the **Model to datasource mapping** page.</span></span>

<span data-ttu-id="cb294-194">您现在有 **发票模型映射**、**项目发票模型映射 (RDP)** 和 **项目发票模型映射 Litware** 配置。</span><span class="sxs-lookup"><span data-stu-id="cb294-194">You now have **Invoice model mapping**, **Project invoice model mapping (RDP)**, and **Project invoice model mapping Litware** configurations.</span></span> <span data-ttu-id="cb294-195">这些配置中的每一个都为 **InvoiceProject** 根定义配置了模型映射。</span><span class="sxs-lookup"><span data-stu-id="cb294-195">Each of these configurations has a model mapping configured for the **InvoiceProject** root definition.</span></span> <span data-ttu-id="cb294-196">明确分配其中一个模型映射作为任何 ER 格式使用的默认模型映射。</span><span class="sxs-lookup"><span data-stu-id="cb294-196">Explicitly assign one of the model mappings as the default model mapping that is used by any of the ER formats.</span></span> <span data-ttu-id="cb294-197">例如，使用包含具有 **InvoiceProject** 根定义的模型数据源的 **项目发票 (Excel)** 格式。</span><span class="sxs-lookup"><span data-stu-id="cb294-197">For example, use the **Project invoice (Excel)** format that contains a model data source that has the **InvoiceProject** root definition.</span></span> <span data-ttu-id="cb294-198">否则，当您运行或编辑其中一个 ER 格式时，将引发异常，通知您未明确分配默认模型映射。</span><span class="sxs-lookup"><span data-stu-id="cb294-198">Otherwise, when you run or edit one of the ER formats, an exception is thrown to notify you that no default model mapping has been explicitly assigned.</span></span>

## <a name="select-the-derived-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a><span data-ttu-id="cb294-199">选择派生的“发票模型映射 Litware”配置作为包含默认模型映射的配置</span><span class="sxs-lookup"><span data-stu-id="cb294-199">Select the derived Invoice model mapping Litware configuration as the configuration that contains default model mappings</span></span>

1. <span data-ttu-id="cb294-200">在 **配置** 页面上，在左侧窗格的配置树中，选择 **发票模型映射 Litware**。</span><span class="sxs-lookup"><span data-stu-id="cb294-200">On the **Configurations** page, in the configuration tree in the left pane, select **Invoice model mapping Litware**.</span></span>
2. <span data-ttu-id="cb294-201">将 **模型映射的默认值** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="cb294-201">Set the **Default for model mapping** option to **Yes**.</span></span>

    ![在“配置”页上将模型映射设置为默认模型映射](./media/er-multiple-model-mappings-image8.png)

    <span data-ttu-id="cb294-203">由于此设置，当您运行 **普通发票 (Excel)** 或对其进行编辑或验证时，将使用 **客户发票副本** 模型映射。</span><span class="sxs-lookup"><span data-stu-id="cb294-203">Because of this setting, the **Customer Invoice Copy** model mapping is used when you run the **Free text invoice (Excel)**, or when you edit or validate it.</span></span> <span data-ttu-id="cb294-204">**发票模型映射** 配置中的 **客户发票** 模型映射将被忽略。</span><span class="sxs-lookup"><span data-stu-id="cb294-204">The **Customer invoice** model mapping from the **Invoice model mapping** configuration is ignored.</span></span>

    <span data-ttu-id="cb294-205">您现在可以打开 **普通发票 (Excel)** 格式来在格式设计器中查看。</span><span class="sxs-lookup"><span data-stu-id="cb294-205">You can now open the **Free text invoice (Excel)** format for review in the format designer.</span></span>

## <a name="select-the-derived-project-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a><span data-ttu-id="cb294-206">选择派生的“项目发票模型映射 Litware”配置作为包含默认模型映射的配置</span><span class="sxs-lookup"><span data-stu-id="cb294-206">Select the derived Project invoice model mapping Litware configuration as the configuration that contains default model mappings</span></span>

1. <span data-ttu-id="cb294-207">在 **配置** 页面上，在左侧窗格的配置树中，选择 **项目发票模型映射 Litware**。</span><span class="sxs-lookup"><span data-stu-id="cb294-207">On the **Configurations** page, in the configuration tree in the left pane, select **Project invoice model mapping Litware**.</span></span>
2. <span data-ttu-id="cb294-208">将 **模型映射的默认值** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="cb294-208">Set the **Default for model mapping** option to **Yes**.</span></span>

    <span data-ttu-id="cb294-209">在这种情况下，与上一节中介绍的 **发票模型映射 Litware** 配置的情况不同，您无法从 **项目发票模型映射 Litware** 配置开始使用 **InvoiceProject 副本** 模型映射。</span><span class="sxs-lookup"><span data-stu-id="cb294-209">In this case, unlike the case that is described for the **Invoice model mapping Litware** configuration in the previous section, you can't start to use the **InvoiceProject Copy** model mapping from the **Project invoice model mapping Litware** configuration.</span></span> <span data-ttu-id="cb294-210">包含 **InvoiceProject** 根定义的模型映射的两个配置当前被标记为默认配置。</span><span class="sxs-lookup"><span data-stu-id="cb294-210">Two configurations that contain a model mapping for the **InvoiceProject** root definition are currently marked as the default configuration.</span></span> <span data-ttu-id="cb294-211">因此，它们具有相同的使用优先级。</span><span class="sxs-lookup"><span data-stu-id="cb294-211">Therefore, they have equal priority for use.</span></span> <span data-ttu-id="cb294-212">要解决此问题，请完成此过程的其余步骤。</span><span class="sxs-lookup"><span data-stu-id="cb294-212">To resolve this issue, complete the remaining steps of this procedure.</span></span>

3. <span data-ttu-id="cb294-213">在左侧窗格的配置树中，选择 **发票模型映射 Litware**。</span><span class="sxs-lookup"><span data-stu-id="cb294-213">In the configuration tree in the left pane, select **Invoice model mapping Litware**.</span></span>
4. <span data-ttu-id="cb294-214">在操作窗格上，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="cb294-214">On the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="cb294-215">在 **模型到数据源映射** 页上，根据需要选择 **编辑** 让页面可编辑。</span><span class="sxs-lookup"><span data-stu-id="cb294-215">On the **Model to datasource mapping** page, select **Edit** to make the page editable, as required.</span></span>
6. <span data-ttu-id="cb294-216">选择 **项目发票副本** 模型映射，然后选择它对应的 **已删除** 复选框。</span><span class="sxs-lookup"><span data-stu-id="cb294-216">Select the **Project Invoice Copy** model mapping, and then select the **Is deleted** check box for it.</span></span>

    ![在“模型到数据源映射”页上将模型映射设置为虚拟删除](./media/er-multiple-model-mappings-image9.png)

    <span data-ttu-id="cb294-218">由于此设置，**发票模型映射 Litware** 配置被视为没有 **InvoiceProject** 根定义的模型映射。</span><span class="sxs-lookup"><span data-stu-id="cb294-218">Because of this setting, the **Invoice model mapping Litware** configuration is treated as though it has no model mapping for the **InvoiceProject** root definition.</span></span> <span data-ttu-id="cb294-219">将默认发布 **InvoiceProject 副本** 模型映射。</span><span class="sxs-lookup"><span data-stu-id="cb294-219">The **InvoiceProject Copy** model mapping issued by default.</span></span> <span data-ttu-id="cb294-220">包含此模型映射的配置 **项目发票模型映射 Litware** 被标记为默认配置。</span><span class="sxs-lookup"><span data-stu-id="cb294-220">The configuration, **Project invoice model mapping Litware**, which contains this model mapping, is marked as the default configuration.</span></span> <span data-ttu-id="cb294-221">由于被标记为默认配置，它的优先级高于 **项目发票模型映射 (RDP)** 配置中的 **InvoiceProject** 模型映射。</span><span class="sxs-lookup"><span data-stu-id="cb294-221">Because it is marked as default, it has a higher priority than the **InvoiceProject** model mapping from the **Project invoice model mapping (RDP)** configuration.</span></span>

## <a name="other-considerations"></a><span data-ttu-id="cb294-222">其他注意事项</span><span class="sxs-lookup"><span data-stu-id="cb294-222">Other considerations</span></span>

<span data-ttu-id="cb294-223">**项目发票模型映射 Litware** 配置的 **InvoiceProject 副本** 模型映射被设计为使用 **ReportDataProvider** 数据源。</span><span class="sxs-lookup"><span data-stu-id="cb294-223">The **InvoiceProject Copy** model mapping of the **Project invoice model mapping Litware** configuration is designed to use the **ReportDataProvider** data source.</span></span> <span data-ttu-id="cb294-224">此数据源是引用 **PsaProjInvoiceDP** 应用程序类的 *对象* 类型的一部分。</span><span class="sxs-lookup"><span data-stu-id="cb294-224">The data source is part of the *Object* type that refers to the **PsaProjInvoiceDP** application class.</span></span> <span data-ttu-id="cb294-225">此类作为打印管理框架的项目发票 SQL Server Reporting Services (SSRS) 报表的数据提供程序实现。</span><span class="sxs-lookup"><span data-stu-id="cb294-225">This class is implemented as the data provider for the project invoice SQL Server Reporting Services (SSRS) report of the Print management framework.</span></span> <span data-ttu-id="cb294-226">选择此数据源作为 ER [集成点](er-apis-app10-0-11.md#api-to-run-a-format-mapping-for-the-generation-of-outbound-documents)。</span><span class="sxs-lookup"><span data-stu-id="cb294-226">Select this data source as the ER [integration point](er-apis-app10-0-11.md#api-to-run-a-format-mapping-for-the-generation-of-outbound-documents).</span></span> <span data-ttu-id="cb294-227">打印管理报表的当前 ER 实现会考虑此设置。</span><span class="sxs-lookup"><span data-stu-id="cb294-227">The current ER implementation for Print management reports takes this setting into account.</span></span> <span data-ttu-id="cb294-228">有关更多详细信息，请查看 **ERPrintMgmtDataProviderReport** 应用程序类的源代码。</span><span class="sxs-lookup"><span data-stu-id="cb294-228">For more details, review the source code of the **ERPrintMgmtDataProviderReport** application class.</span></span> <span data-ttu-id="cb294-229">在运行时，将 **ReportDataProvider** 数据源作为模型映射集成点分配，会强制 Finance 将此映射组件视为具有高于 **项目发票模型映射 (RDP)** 配置中的 **InvoiceProject** 映射组件的优先级。</span><span class="sxs-lookup"><span data-stu-id="cb294-229">At runtime, the assignment of the **ReportDataProvider** data source as the model mapping integration point forces Finance to treat this mapping component with a higher priority than the **InvoiceProject** mapping component from the **Project invoice model mapping (RDP)** configuration.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb294-230">请参阅</span><span class="sxs-lookup"><span data-stu-id="cb294-230">See also</span></span>

- [<span data-ttu-id="cb294-231">管理单独电子报告配置中的电子报告模型映射</span><span class="sxs-lookup"><span data-stu-id="cb294-231">Manage ER model mapping in separate ER configurations</span></span>](./tasks/er-manage-model-mapping-configurations-july-2017.md)
- [<span data-ttu-id="cb294-232">配置与国家/地区上下文相关的电子报告模型映射</span><span class="sxs-lookup"><span data-stu-id="cb294-232">Configure country context dependent ER model mappings</span></span>](er-country-dependent-model-mapping.md)
- [<span data-ttu-id="cb294-233">电子报告框架 API 更改</span><span class="sxs-lookup"><span data-stu-id="cb294-233">Electronic reporting framework API changes</span></span>](er-apis-app10-0-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: 设计新的 ER 解决方案打印自定义报表
description: 本主题说明如何设计电子报告 (ER) 解决方案来打印自定义报表。
author: NickSelin
manager: AnnBe
ms.date: 08/10/2020
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
ms.openlocfilehash: c5bbfae36fb15437f2baadc66663cbfdb28691e8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562603"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a><span data-ttu-id="9b235-103">设计新的 ER 解决方案打印自定义报表</span><span class="sxs-lookup"><span data-stu-id="9b235-103">Design a new ER solution to print a custom report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9b235-104">以下步骤说明了具有系统管理员、电子报告开发人员或电子报告功能顾问角色的用户如何配置 ER 框架的参数，设计新 ER 解决方案所需的 ER 配置以访问特定业务域的数据，以及如何以 Microsoft Office 格式生成自定义报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-104">The following steps explain how a user in the System Administrator, Electronic Reporting Developer, or Electronic Reporting Functional Consultant role can configure parameters of the ER framework, design the required ER configurations of a new ER solution to access the data of a particular business domain, and generate a custom report in Microsoft Office format.</span></span> <span data-ttu-id="9b235-105">这些步骤可以在 **USMF** 公司完成。</span><span class="sxs-lookup"><span data-stu-id="9b235-105">These steps can be completed in the **USMF** company.</span></span>

- [<span data-ttu-id="9b235-106">配置 ER 框架</span><span class="sxs-lookup"><span data-stu-id="9b235-106">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="9b235-107">配置 ER 参数</span><span class="sxs-lookup"><span data-stu-id="9b235-107">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="9b235-108">激活 ER 配置提供程序</span><span class="sxs-lookup"><span data-stu-id="9b235-108">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="9b235-109">查看 ER 配置提供程序列表</span><span class="sxs-lookup"><span data-stu-id="9b235-109">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="9b235-110">添加新 ER 配置提供程序</span><span class="sxs-lookup"><span data-stu-id="9b235-110">Add a new ER configuration provider</span></span>](#AddProvider)
        - [<span data-ttu-id="9b235-111">激活 ER 配置提供程序</span><span class="sxs-lookup"><span data-stu-id="9b235-111">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="9b235-112">设计域特定数据模型</span><span class="sxs-lookup"><span data-stu-id="9b235-112">Design a domain-specific data model</span></span>](#DesignModel)

    - [<span data-ttu-id="9b235-113">导入新数据模型配置</span><span class="sxs-lookup"><span data-stu-id="9b235-113">Import a new data model configuration</span></span>](#ImportDataModel)
    - [<span data-ttu-id="9b235-114">创建新的数据模型配置</span><span class="sxs-lookup"><span data-stu-id="9b235-114">Create a new data model configuration</span></span>](#DesignDataModel)

        - [<span data-ttu-id="9b235-115">为数据模型命名</span><span class="sxs-lookup"><span data-stu-id="9b235-115">Name the data model</span></span>](#NameDataModel)
        - [<span data-ttu-id="9b235-116">添加数据模型字段</span><span class="sxs-lookup"><span data-stu-id="9b235-116">Add data model fields</span></span>](#FieldsEntry)
        - [<span data-ttu-id="9b235-117">完成数据模型的设计</span><span class="sxs-lookup"><span data-stu-id="9b235-117">Complete the design of the data model</span></span>](#CompleteDataModel)

- [<span data-ttu-id="9b235-118">为配置的数据模型设计模型映射</span><span class="sxs-lookup"><span data-stu-id="9b235-118">Design a model mapping for the configured data model</span></span>](#DesignMapping)

    - [<span data-ttu-id="9b235-119">导入新模型映射配置</span><span class="sxs-lookup"><span data-stu-id="9b235-119">Import a new model mapping configuration</span></span>](#ImportModelMapping)
    - [<span data-ttu-id="9b235-120">创建新模型映射配置</span><span class="sxs-lookup"><span data-stu-id="9b235-120">Create a new model mapping configuration</span></span>](#CreateModelMapping)

        - [<span data-ttu-id="9b235-121">设计新模型映射组件</span><span class="sxs-lookup"><span data-stu-id="9b235-121">Design a new model mapping component</span></span>](#DesignMappingComponent)
        - [<span data-ttu-id="9b235-122">添加数据源以访问应用程序表</span><span class="sxs-lookup"><span data-stu-id="9b235-122">Add data sources to access application tables</span></span>](#AddMmDataSource1)
        - [<span data-ttu-id="9b235-123">添加数据源以访问应用程序枚举</span><span class="sxs-lookup"><span data-stu-id="9b235-123">Add data sources to access application enumerations</span></span>](#AddMmDataSource2)
        - [<span data-ttu-id="9b235-124">添加 ER 标签以指定语言生成报表</span><span class="sxs-lookup"><span data-stu-id="9b235-124">Add ER labels to generate a report in a specified language</span></span>](#AddMmLabels)
        - [<span data-ttu-id="9b235-125">添加数据源以将比较枚举值的结果转换为文本值</span><span class="sxs-lookup"><span data-stu-id="9b235-125">Add a data source to transform the results of comparing enumeration values to a text value</span></span>](#AddMmDataSource3)
        - [<span data-ttu-id="9b235-126">将数据源与数据模型字段绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-126">Bind data sources to data model fields</span></span>](#AddMmBindings1)
        - [<span data-ttu-id="9b235-127">完成模型映射的设计</span><span class="sxs-lookup"><span data-stu-id="9b235-127">Complete the design of the model mapping</span></span>](#CompleteModelMapping)

- [<span data-ttu-id="9b235-128">为自定义报表设计模板</span><span class="sxs-lookup"><span data-stu-id="9b235-128">Design a template for a custom report</span></span>](#DesignReportTemplate)
- [<span data-ttu-id="9b235-129">设计格式</span><span class="sxs-lookup"><span data-stu-id="9b235-129">Design a format</span></span>](#DesignFormat)

    - [<span data-ttu-id="9b235-130">导入设计的格式配置</span><span class="sxs-lookup"><span data-stu-id="9b235-130">Import a designed format configuration</span></span>](#FormatImport)
    - [<span data-ttu-id="9b235-131">创建新的格式配置</span><span class="sxs-lookup"><span data-stu-id="9b235-131">Create a new format configuration</span></span>](#FormatCreate)

        - [<span data-ttu-id="9b235-132">导入报表模板</span><span class="sxs-lookup"><span data-stu-id="9b235-132">Import a report template</span></span>](#ImportReportTemplate)
        - [<span data-ttu-id="9b235-133">配置格式</span><span class="sxs-lookup"><span data-stu-id="9b235-133">Configure a format</span></span>](#ConfigureFormat)
        - [<span data-ttu-id="9b235-134">定义报表标题的数据绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-134">Define the data binding for a report title</span></span>](#DefineFormatBindings)
        - [<span data-ttu-id="9b235-135">查看模型数据源</span><span class="sxs-lookup"><span data-stu-id="9b235-135">Review the model data source</span></span>](#ReviewModelDataSource)
        - [<span data-ttu-id="9b235-136">将格式元素与数据源字段绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-136">Bind format elements to data source fields</span></span>](#BindFormatElements)

    - [<span data-ttu-id="9b235-137">从 ER 运行设计的格式</span><span class="sxs-lookup"><span data-stu-id="9b235-137">Run a designed format from ER</span></span>](#RunFormatFromER)

- [<span data-ttu-id="9b235-138">调整设计的格式</span><span class="sxs-lookup"><span data-stu-id="9b235-138">Tune a designed format</span></span>](#TuneFormat)

    - [<span data-ttu-id="9b235-139">修改格式以更改生成文档的名称</span><span class="sxs-lookup"><span data-stu-id="9b235-139">Modify a format to change the name of a generated document</span></span>](#ModifyToChangeName)
    - [<span data-ttu-id="9b235-140">修改格式以更改问题的顺序</span><span class="sxs-lookup"><span data-stu-id="9b235-140">Modify a format to change the order of questions</span></span>](#ModifyToOrder)
    - [<span data-ttu-id="9b235-141">从 ER 运行修改的格式</span><span class="sxs-lookup"><span data-stu-id="9b235-141">Run a modified format from ER</span></span>](#RunFormatFromER2)
    - [<span data-ttu-id="9b235-142">完成格式设计</span><span class="sxs-lookup"><span data-stu-id="9b235-142">Complete the format design</span></span>](#CompleteFormat)

- [<span data-ttu-id="9b235-143">开发应用程序伪像以调用设计的报表</span><span class="sxs-lookup"><span data-stu-id="9b235-143">Develop application artefacts to call the designed report</span></span>](#DevelopCustomCode)

    - [<span data-ttu-id="9b235-144">修改源代码</span><span class="sxs-lookup"><span data-stu-id="9b235-144">Modify source code</span></span>](#ModifySourceCode)

        - [<span data-ttu-id="9b235-145">添加数据合同类</span><span class="sxs-lookup"><span data-stu-id="9b235-145">Add a data contract class</span></span>](#DataContractClass)
        - [<span data-ttu-id="9b235-146">添加 UI 构建器类</span><span class="sxs-lookup"><span data-stu-id="9b235-146">Add a UI builder class</span></span>](#UIBuilderClass)
        - [<span data-ttu-id="9b235-147">添加数据提供程序类</span><span class="sxs-lookup"><span data-stu-id="9b235-147">Add a data provider class</span></span>](#DataProviderClass)
        - [<span data-ttu-id="9b235-148">添加标签文件</span><span class="sxs-lookup"><span data-stu-id="9b235-148">Add a labels file</span></span>](#LabelsFile)
        - [<span data-ttu-id="9b235-149">添加报表服务类</span><span class="sxs-lookup"><span data-stu-id="9b235-149">Add a report service class</span></span>](#ServiceClass)
        - [<span data-ttu-id="9b235-150">添加报表控制器类</span><span class="sxs-lookup"><span data-stu-id="9b235-150">Add a report controller class</span></span>](#ControllerClass)
        - [<span data-ttu-id="9b235-151">添加菜单项</span><span class="sxs-lookup"><span data-stu-id="9b235-151">Add a menu item</span></span>](#MenuItem)
        - [<span data-ttu-id="9b235-152">向菜单添加菜单项</span><span class="sxs-lookup"><span data-stu-id="9b235-152">Add a menu item to a menu</span></span>](#Menu)
        - [<span data-ttu-id="9b235-153">构建 Visual Studio 项目</span><span class="sxs-lookup"><span data-stu-id="9b235-153">Build a Visual Studio project</span></span>](#BuildVSProject)

    - [<span data-ttu-id="9b235-154">从应用程序运行格式</span><span class="sxs-lookup"><span data-stu-id="9b235-154">Run a format from the application</span></span>](#RunFormatFromApp)

- [<span data-ttu-id="9b235-155">调整设计的 ER 解决方案</span><span class="sxs-lookup"><span data-stu-id="9b235-155">Tune a designed ER solution</span></span>](#TuneSolution)

    - [<span data-ttu-id="9b235-156">修改模型映射</span><span class="sxs-lookup"><span data-stu-id="9b235-156">Modify a model mapping</span></span>](#ModifyModelMapping)

        - [<span data-ttu-id="9b235-157">添加数据源以访问数据合同对象</span><span class="sxs-lookup"><span data-stu-id="9b235-157">Add data sources to access a data contract object</span></span>](#AddDataSource1)
        - [<span data-ttu-id="9b235-158">添加数据源以访问 ER 格式映射记录</span><span class="sxs-lookup"><span data-stu-id="9b235-158">Add a data source to access ER format mapping records</span></span>](#AddDataSource2)
        - [<span data-ttu-id="9b235-159">添加数据源以访问正在运行的 ER 格式的格式映射记录</span><span class="sxs-lookup"><span data-stu-id="9b235-159">Add a data source to access a format mapping record of a running ER format</span></span>](#AddDataSource3)
        - [<span data-ttu-id="9b235-160">在数据模型中输入正在运行的 ER 格式的名称</span><span class="sxs-lookup"><span data-stu-id="9b235-160">Enter the name of the running ER format in the data model</span></span>](#AddBinding)
        - [<span data-ttu-id="9b235-161">完成模型映射的设计</span><span class="sxs-lookup"><span data-stu-id="9b235-161">Complete the design of the model mapping</span></span>](#CompleteModelMapping2)

    - [<span data-ttu-id="9b235-162">修改格式</span><span class="sxs-lookup"><span data-stu-id="9b235-162">Modify a format</span></span>](#ModifyFormat)

        - [<span data-ttu-id="9b235-163">添加新格式元素</span><span class="sxs-lookup"><span data-stu-id="9b235-163">Add a new format element</span></span>](#AddFormatElement)
        - [<span data-ttu-id="9b235-164">绑定添加的格式元素</span><span class="sxs-lookup"><span data-stu-id="9b235-164">Bind the added format element</span></span>](#BindAddedFormatElement)
        - [<span data-ttu-id="9b235-165">完成格式设计</span><span class="sxs-lookup"><span data-stu-id="9b235-165">Complete the format design</span></span>](#CompleteFormat2)

    - [<span data-ttu-id="9b235-166">从应用程序运行格式</span><span class="sxs-lookup"><span data-stu-id="9b235-166">Run a format from the application</span></span>](#RunFormatFromApp2)
    - [<span data-ttu-id="9b235-167">从 ER 运行格式</span><span class="sxs-lookup"><span data-stu-id="9b235-167">Run a format from ER</span></span>](#RunFormatFromER3)
    - [<span data-ttu-id="9b235-168">为屏幕预览配置格式目标</span><span class="sxs-lookup"><span data-stu-id="9b235-168">Configure a format destination for on-screen preview</span></span>](#ConfigureDestination)
    - [<span data-ttu-id="9b235-169">从应用程序运行格式以作为 PDF 文档预览</span><span class="sxs-lookup"><span data-stu-id="9b235-169">Run a format from the application to preview it as a PDF document</span></span>](#RunFormatFromApp3)

- [<span data-ttu-id="9b235-170">其他资源</span><span class="sxs-lookup"><span data-stu-id="9b235-170">Additional resources</span></span>](#References)

<span data-ttu-id="9b235-171">在此示例中，您将为[调查表](https://docs.microsoft.com/dynamics365/human-resources/hr-learning-questionnaires)模块创建新的 ER 解决方案。</span><span class="sxs-lookup"><span data-stu-id="9b235-171">In this example, you will create a new ER solution for the [Questionnaire](https://docs.microsoft.com/dynamics365/human-resources/hr-learning-questionnaires) module.</span></span> <span data-ttu-id="9b235-172">这个新的 ER 解决方案使您可以使用 Microsoft Excel 工作表作为模板来设计报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-172">This new ER solution lets you design a report by using a Microsoft Excel worksheet as a template.</span></span> <span data-ttu-id="9b235-173">然后，除了生成现有的 SQL Server Reporting Services (SSRS) 报表之外，您还可以生成 Excel 或 PDF 格式的 **调查表** 报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-173">You can then generate the **Questionnaire** report in Excel or PDF format, in addition to generating the existing SQL Server Reporting Services (SSRS) report.</span></span> <span data-ttu-id="9b235-174">您还可以稍后根据要求修改新报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-174">You can also modify the new report later, upon request.</span></span> <span data-ttu-id="9b235-175">无需进行编码。</span><span class="sxs-lookup"><span data-stu-id="9b235-175">No coding is required.</span></span>

1. <span data-ttu-id="9b235-176">要运行现有报表，请转到 **调查表** \> **设计** \> **调查表报表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-176">To run the existing report, go to **Questionnaire** \> **Design** \> **Questionnaires report**.</span></span>

    ![在“调查表”模块中选择“调查表报表”菜项来运行现有 SSRS 报表](./media/er-quick-start1-application-menu-origin.png)

2. <span data-ttu-id="9b235-178">在 **调查表报表** 对话框中，指定选择条件。</span><span class="sxs-lookup"><span data-stu-id="9b235-178">In the **Questionnaires report** dialog box, specify selection criteria.</span></span> <span data-ttu-id="9b235-179">应用筛选器，让报表仅包含 **SBCCrsExam** 调查表。</span><span class="sxs-lookup"><span data-stu-id="9b235-179">Apply a filter so that the report includes only the **SBCCrsExam** questionnaire.</span></span>

    ![在“调查表报表”对话框中指定选择条件](./media/er-quick-start1-ssrs-report-dialog.png)

<span data-ttu-id="9b235-181">下图显示了 **SBCCrsExam** 调查表的 SSRS 报表的生成版本。</span><span class="sxs-lookup"><span data-stu-id="9b235-181">The following illustration shows the generated version of the SSRS report for the **SBCCrsExam** questionnaire.</span></span>

![生成的 SSRS 报表](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a><span data-ttu-id="9b235-183">配置 ER 框架</span><span class="sxs-lookup"><span data-stu-id="9b235-183">Configure the ER framework</span></span>

<span data-ttu-id="9b235-184">作为电子报告开发人员角色的用户，您必须至少配置一组 ER 参数，才能开始使用 ER 框架设计新的 ER 解决方案。</span><span class="sxs-lookup"><span data-stu-id="9b235-184">As a user in the Electronic Reporting Developer role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design your new ER solution.</span></span>

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a><span data-ttu-id="9b235-185">配置 ER 参数</span><span class="sxs-lookup"><span data-stu-id="9b235-185">Configure ER parameters</span></span>

1. <span data-ttu-id="9b235-186">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="9b235-186">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9b235-187">在 **电子申报** 工作区中，选择 **电子申报参数** 链接。</span><span class="sxs-lookup"><span data-stu-id="9b235-187">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="9b235-188">在 **电子申报参数** 页上，在 **常规** 选项卡上，将 **启用设计模式** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="9b235-188">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="9b235-189">在 **附件** 选项卡上，设置以下参数：</span><span class="sxs-lookup"><span data-stu-id="9b235-189">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="9b235-190">将 **USMF** 公司的 **配置** 字段设置为 **文件**。</span><span class="sxs-lookup"><span data-stu-id="9b235-190">Set the **Configurations** field to **File** for the **USMF** company.</span></span>
    - <span data-ttu-id="9b235-191">将 **作业存档**、**临时**、**基准** 和 **其他** 字段设置为 **文件**。</span><span class="sxs-lookup"><span data-stu-id="9b235-191">Set **Job archive**, **Temporary**, **Baseline**, and **Others** fields to **File**.</span></span>

<span data-ttu-id="9b235-192">有关 ER 参数的详细信息，请参阅[配置 ER 框架](electronic-reporting-er-configure-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="9b235-192">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a><span data-ttu-id="9b235-193">激活 ER 配置提供程序</span><span class="sxs-lookup"><span data-stu-id="9b235-193">Activate an ER configuration provider</span></span>

<span data-ttu-id="9b235-194">将把每个 ER 配置标记为由 ER 配置提供程序负责。</span><span class="sxs-lookup"><span data-stu-id="9b235-194">Every ER configuration is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="9b235-195">因此，必须先在 **电子报告** 工作区中激活 ER 配置提供程序，才能开始添加或编辑 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="9b235-195">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit any ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="9b235-196">只有 ER 配置的负责人才能对其进行编辑。</span><span class="sxs-lookup"><span data-stu-id="9b235-196">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="9b235-197">因此，必须先在 **电子申报** 工作区中激活相应 ER 配置提供程序，才能编辑 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="9b235-197">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a><span data-ttu-id="9b235-198">查看 ER 配置提供程序列表</span><span class="sxs-lookup"><span data-stu-id="9b235-198">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="9b235-199">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="9b235-199">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9b235-200">在 **电子报告** 工作区的 **相关链接** 部分，选择 **配置提供程序**。</span><span class="sxs-lookup"><span data-stu-id="9b235-200">In the **Electronic reporting** workspace, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="9b235-201">在 **配置提供程序** 页，每条配置提供程序记录都有唯一名称和 URL。</span><span class="sxs-lookup"><span data-stu-id="9b235-201">On the **Configuration providers** page, each configuration provider record has a unique name and URL.</span></span> <span data-ttu-id="9b235-202">查看此页面的内容。</span><span class="sxs-lookup"><span data-stu-id="9b235-202">Review the contents of this page.</span></span> <span data-ttu-id="9b235-203">如果已有 **Litware, Inc.** (`https://www.litware.com`) 的记录，请跳过下一过程，即[添加新 ER 配置提供程序](#ActivateProvider)。</span><span class="sxs-lookup"><span data-stu-id="9b235-203">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a><span data-ttu-id="9b235-204">添加新 ER 配置提供程序</span><span class="sxs-lookup"><span data-stu-id="9b235-204">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="9b235-205">在 **配置提供程序** 页面上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="9b235-205">On the **Configuration providers** page, select **New**.</span></span>
2. <span data-ttu-id="9b235-206">在 **名称** 字段中，输入 **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="9b235-206">In the **Name** field, enter **Litware, Inc.**</span></span>
3. <span data-ttu-id="9b235-207">在 **Internet 地址** 字段中，输入 `https://www.litware.com`。</span><span class="sxs-lookup"><span data-stu-id="9b235-207">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
4. <span data-ttu-id="9b235-208">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9b235-208">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a><span data-ttu-id="9b235-209">激活 ER 配置提供程序</span><span class="sxs-lookup"><span data-stu-id="9b235-209">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="9b235-210">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="9b235-210">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9b235-211">在 **电子报告** 工作区中，选择 **Litware, Inc.** 配置提供程序。</span><span class="sxs-lookup"><span data-stu-id="9b235-211">In the **Electronic reporting** workspace, select the **Litware, Inc.** configuration provider.</span></span>
3. <span data-ttu-id="9b235-212">选择 **设置有效**。</span><span class="sxs-lookup"><span data-stu-id="9b235-212">Select **Set active**.</span></span>

<span data-ttu-id="9b235-213">有关 ER 配置提供程序的详细信息，请参阅[创建配置提供程序并将其标记为有效](tasks/er-configuration-provider-mark-it-active-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="9b235-213">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a><span data-ttu-id="9b235-214">设计域特定数据模型</span><span class="sxs-lookup"><span data-stu-id="9b235-214">Design a domain-specific data model</span></span>

<span data-ttu-id="9b235-215">您必须为 **调查表** 业务域创建一个包含[数据模型](general-electronic-reporting.md#data-model-and-model-mapping-components)组件的新 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="9b235-215">You must create a new ER configuration that contains a [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** business domain.</span></span> <span data-ttu-id="9b235-216">此数据模型将在以后您设计 ER 格式以生成 **调查表** 报表时用作数据源。</span><span class="sxs-lookup"><span data-stu-id="9b235-216">This data model will later be used as a data source when you design an ER format to generate the **Questionnaire** report.</span></span>

<span data-ttu-id="9b235-217">通过完成[导入新数据模型配置](#ImportDataModel)一节的步骤，可以从提供的 XML 文件导入所需的数据模型。</span><span class="sxs-lookup"><span data-stu-id="9b235-217">By completing the steps in the [Import a new data model configuration](#ImportDataModel) section, you can import the required data model from the provided XML file.</span></span> <span data-ttu-id="9b235-218">或者，您可以完成[创建新数据模型配置](#DesignDataModel)一节的步骤来从头开始设计此数据模型。</span><span class="sxs-lookup"><span data-stu-id="9b235-218">Alternatively, you can complete the steps in the [Create a new data model configuration](#DesignDataModel) section to design this data model from scratch.</span></span>

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a><span data-ttu-id="9b235-219">导入新数据模型配置</span><span class="sxs-lookup"><span data-stu-id="9b235-219">Import a new data model configuration</span></span>

1. <span data-ttu-id="9b235-220">下载 [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) 文件，并将其保存到本地计算机。</span><span class="sxs-lookup"><span data-stu-id="9b235-220">Download the [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="9b235-221">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="9b235-221">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="9b235-222">在 **电子报告** 工作区中，选择 **报告配置**。</span><span class="sxs-lookup"><span data-stu-id="9b235-222">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="9b235-223">在操作窗格上，选择 **交换** \> **从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="9b235-223">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="9b235-224">选择 **浏览**，然后找到并选择 **Questionnaires model.version.1.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="9b235-224">Select **Browse**, and then find and select the **Questionnaires model.version.1.xml** file.</span></span>
6. <span data-ttu-id="9b235-225">选择 **确定** 导入配置。</span><span class="sxs-lookup"><span data-stu-id="9b235-225">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="9b235-226">要继续，跳过下一个过程[创建新的数据模型配置](#DesignDataModel)。</span><span class="sxs-lookup"><span data-stu-id="9b235-226">To continue, skip the next procedure, [Create a new data model configuration](#DesignDataModel).</span></span>

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a><span data-ttu-id="9b235-227">创建新的数据模型配置</span><span class="sxs-lookup"><span data-stu-id="9b235-227">Create a new data model configuration</span></span>

1. <span data-ttu-id="9b235-228">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="9b235-228">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9b235-229">在 **电子报告** 工作区中，选择 **报告配置**。</span><span class="sxs-lookup"><span data-stu-id="9b235-229">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="9b235-230">选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="9b235-230">Select **Create configuration**.</span></span>
4. <span data-ttu-id="9b235-231">在下拉对话框的 **名称** 字段中，输入 **调查表模型**。</span><span class="sxs-lookup"><span data-stu-id="9b235-231">In the drop-down dialog box, in the **Name** field, enter **Questionnaire model**.</span></span>
5. <span data-ttu-id="9b235-232">选择 **创建配置** 以创建配置。</span><span class="sxs-lookup"><span data-stu-id="9b235-232">Select **Create configuration** to create the configuration.</span></span>

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a><span data-ttu-id="9b235-233">为数据模型命名</span><span class="sxs-lookup"><span data-stu-id="9b235-233">Name the data model</span></span>

1. <span data-ttu-id="9b235-234">在 **配置** 页上的配置树中，选择 **调查表模型**。</span><span class="sxs-lookup"><span data-stu-id="9b235-234">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
2. <span data-ttu-id="9b235-235">选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="9b235-235">Select **Designer**.</span></span>
3. <span data-ttu-id="9b235-236">在 **数据模型设计器** 页上的 **常规** 快速选项卡上，在 **名称** 字段中，输入 <a name="DataModeName"></a>**调查表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-236">On the **Data model designer** page, on the **General** FastTab, in the **Name** field, enter <a name="DataModeName"></a>**Questionnaires**.</span></span>

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a><span data-ttu-id="9b235-237">添加新数据模型字段</span><span class="sxs-lookup"><span data-stu-id="9b235-237">Add new data model fields</span></span>

1. <span data-ttu-id="9b235-238">在 **数据模型设计器** 页上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="9b235-238">On the **Data model designer** page, select **New**.</span></span>
2. <span data-ttu-id="9b235-239">在用于添加数据模型节点的下拉对话框中，按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="9b235-239">In the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="9b235-240">选择 **模型根** 作为新节点的类型。</span><span class="sxs-lookup"><span data-stu-id="9b235-240">Select **Model root** as the type of the new node.</span></span>
    2. <span data-ttu-id="9b235-241">在 **名称** 字段中，输入 <a name="RootDefinitionName"></a>**根**。</span><span class="sxs-lookup"><span data-stu-id="9b235-241">In the **Name** field, enter <a name="RootDefinitionName"></a>**Root**.</span></span>
    3. <span data-ttu-id="9b235-242">选择 **添加** 添加新节点。</span><span class="sxs-lookup"><span data-stu-id="9b235-242">Select **Add** to add the new node.</span></span>

    <span data-ttu-id="9b235-243">此根描述符将用于为 **调查表** 报表提供数据。</span><span class="sxs-lookup"><span data-stu-id="9b235-243">This root descriptor will be used to provide data for the **Questionnaire** report.</span></span> <span data-ttu-id="9b235-244">单个数据模型可以有多个描述符。</span><span class="sxs-lookup"><span data-stu-id="9b235-244">A single data model can have multiple descriptors.</span></span> <span data-ttu-id="9b235-245">可以为一个 ER 格式指定每个描述符，来标识生成报表所需的数据。</span><span class="sxs-lookup"><span data-stu-id="9b235-245">Each descriptor can be specified for a single ER format, to identify data that is required to generate the report.</span></span>

3. <span data-ttu-id="9b235-246">再次选择 **新建**，然后，在用于添加数据模型节点的下拉对话框中，按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="9b235-246">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="9b235-247">选择 **活动节点的子节点** 作为新节点的类型。</span><span class="sxs-lookup"><span data-stu-id="9b235-247">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="9b235-248">在 **名称** 字段中，输入 **公司名称**。</span><span class="sxs-lookup"><span data-stu-id="9b235-248">In the **Name** field, enter **CompanyName**.</span></span>
    3. <span data-ttu-id="9b235-249">在 **物料类型** 字段中，选择 **字符串**。</span><span class="sxs-lookup"><span data-stu-id="9b235-249">In the **Item type** field, select **String**.</span></span>
    4. <span data-ttu-id="9b235-250">选择 **添加** 添加新字段。</span><span class="sxs-lookup"><span data-stu-id="9b235-250">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="9b235-251">将当前公司的名称传递到使用此数据模型作为数据源的 ER 报表时，此字段是必需的。</span><span class="sxs-lookup"><span data-stu-id="9b235-251">This field is required to pass the name of the current company to an ER report that consumes this data model as a data source.</span></span>

4. <span data-ttu-id="9b235-252">再次选择 **新建**，然后，在用于添加数据模型节点的下拉对话框中，按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="9b235-252">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="9b235-253">选择 **活动节点的子节点** 作为新节点的类型。</span><span class="sxs-lookup"><span data-stu-id="9b235-253">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="9b235-254">在 **名称** 字段中，输入 **调查表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-254">In the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="9b235-255">在 **物料类型** 字段中，选择 **记录列表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-255">In the **Item type** field, select **Record list**.</span></span>
    4. <span data-ttu-id="9b235-256">选择 **添加** 添加新字段。</span><span class="sxs-lookup"><span data-stu-id="9b235-256">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="9b235-257">此字段将用于将调查表列表传递到使用此数据模型作为数据源的 ER 报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-257">This field will be used to pass the list of questionnaires to an ER report that consumes this data model as a data source.</span></span>

5. <span data-ttu-id="9b235-258">选择 **调查表** 节点。</span><span class="sxs-lookup"><span data-stu-id="9b235-258">Select the **Questionnaire** node.</span></span>
6. <span data-ttu-id="9b235-259">继续以相同方式添加可编辑数据模型的必需字段，直到完成以下数据模型结构。</span><span class="sxs-lookup"><span data-stu-id="9b235-259">Continue to add the required fields of the editable data model in the same manner until you complete the following data model structure.</span></span>

    | <span data-ttu-id="9b235-260">字段路径</span><span class="sxs-lookup"><span data-stu-id="9b235-260">Field path</span></span>                                                    | <span data-ttu-id="9b235-261">数据类型</span><span class="sxs-lookup"><span data-stu-id="9b235-261">Data type</span></span>   | <span data-ttu-id="9b235-262">字段指定/返回值</span><span class="sxs-lookup"><span data-stu-id="9b235-262">Field designation/returned value</span></span> |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | <span data-ttu-id="9b235-263">根</span><span class="sxs-lookup"><span data-stu-id="9b235-263">Root</span></span>                                                          |             | <span data-ttu-id="9b235-264">请求调查表数据的参考点。</span><span class="sxs-lookup"><span data-stu-id="9b235-264">The reference point to request questionnaire data.</span></span> |
    | <span data-ttu-id="9b235-265">根\\公司名称</span><span class="sxs-lookup"><span data-stu-id="9b235-265">Root\\CompanyName</span></span>                                             | <span data-ttu-id="9b235-266">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-266">String</span></span>      | <span data-ttu-id="9b235-267">当前公司的名称。</span><span class="sxs-lookup"><span data-stu-id="9b235-267">The name of the current company.</span></span> |
    | <span data-ttu-id="9b235-268">根\\执行上下文</span><span class="sxs-lookup"><span data-stu-id="9b235-268">Root\\ExecutionContext</span></span>                                        | <span data-ttu-id="9b235-269">录制</span><span class="sxs-lookup"><span data-stu-id="9b235-269">Record</span></span>      | <span data-ttu-id="9b235-270">格式执行详细信息。</span><span class="sxs-lookup"><span data-stu-id="9b235-270">Format execution details.</span></span> |
    | <span data-ttu-id="9b235-271">根\\执行上下文\\格式名称</span><span class="sxs-lookup"><span data-stu-id="9b235-271">Root\\ExecutionContext\\FormatName</span></span>                            | <span data-ttu-id="9b235-272">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-272">String</span></span>      | <span data-ttu-id="9b235-273">正在运行的 ER 格式的名称。</span><span class="sxs-lookup"><span data-stu-id="9b235-273">The name of the ER format that is being run.</span></span> |
    | <span data-ttu-id="9b235-274">根\\调查表</span><span class="sxs-lookup"><span data-stu-id="9b235-274">Root\\Questionnaire</span></span>                                           | <span data-ttu-id="9b235-275">记录列表</span><span class="sxs-lookup"><span data-stu-id="9b235-275">Record list</span></span> | <span data-ttu-id="9b235-276">调查表列表</span><span class="sxs-lookup"><span data-stu-id="9b235-276">The list of questionnaires</span></span> |
    | <span data-ttu-id="9b235-277">根\\调查表\\活动</span><span class="sxs-lookup"><span data-stu-id="9b235-277">Root\\Questionnaire\\Active</span></span>                                   | <span data-ttu-id="9b235-278">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-278">String</span></span>      | <span data-ttu-id="9b235-279">当前调查表的状态。</span><span class="sxs-lookup"><span data-stu-id="9b235-279">The status of the current questionnaire.</span></span> |
    | <span data-ttu-id="9b235-280">根\\调查表\\代码</span><span class="sxs-lookup"><span data-stu-id="9b235-280">Root\\Questionnaire\\Code</span></span>                                     | <span data-ttu-id="9b235-281">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-281">String</span></span>      | <span data-ttu-id="9b235-282">当前调查表的代码。</span><span class="sxs-lookup"><span data-stu-id="9b235-282">The code of the current questionnaire.</span></span> |
    | <span data-ttu-id="9b235-283">根\\调查表\\说明</span><span class="sxs-lookup"><span data-stu-id="9b235-283">Root\\Questionnaire\\Description</span></span>                              | <span data-ttu-id="9b235-284">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-284">String</span></span>      | <span data-ttu-id="9b235-285">当前调查表的说明。</span><span class="sxs-lookup"><span data-stu-id="9b235-285">The description of the current questionnaire.</span></span> |
    | <span data-ttu-id="9b235-286">根\\调查表\\调查表类型</span><span class="sxs-lookup"><span data-stu-id="9b235-286">Root\\Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="9b235-287">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-287">String</span></span>      | <span data-ttu-id="9b235-288">当前调查表的类型。</span><span class="sxs-lookup"><span data-stu-id="9b235-288">The type of the current questionnaire.</span></span> |
    | <span data-ttu-id="9b235-289">根\\调查表\\问题顺序</span><span class="sxs-lookup"><span data-stu-id="9b235-289">Root\\Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="9b235-290">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-290">String</span></span>      | <span data-ttu-id="9b235-291">当前调查表的数字顺序。</span><span class="sxs-lookup"><span data-stu-id="9b235-291">The numerical order of the current questionnaire.</span></span> |
    | <span data-ttu-id="9b235-292">根\\调查表\\结果组</span><span class="sxs-lookup"><span data-stu-id="9b235-292">Root\\Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="9b235-293">录制</span><span class="sxs-lookup"><span data-stu-id="9b235-293">Record</span></span>      | <span data-ttu-id="9b235-294">当前调查表的结果参数。</span><span class="sxs-lookup"><span data-stu-id="9b235-294">The result parameters of the current questionnaire.</span></span> |
    | <span data-ttu-id="9b235-295">根\\调查表\\结果组\\代码</span><span class="sxs-lookup"><span data-stu-id="9b235-295">Root\\Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="9b235-296">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-296">String</span></span>      | <span data-ttu-id="9b235-297">当前结果组的标识代码。</span><span class="sxs-lookup"><span data-stu-id="9b235-297">The identification code of the current result group.</span></span> |
    | <span data-ttu-id="9b235-298">根\\调查表\\结果组\\说明</span><span class="sxs-lookup"><span data-stu-id="9b235-298">Root\\Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="9b235-299">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-299">String</span></span>      | <span data-ttu-id="9b235-300">当前结果组的说明。</span><span class="sxs-lookup"><span data-stu-id="9b235-300">The description of the current result group.</span></span> |
    | <span data-ttu-id="9b235-301">根\\调查表\\结果组\\最高分数</span><span class="sxs-lookup"><span data-stu-id="9b235-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="9b235-302">实数</span><span class="sxs-lookup"><span data-stu-id="9b235-302">Real</span></span>        | <span data-ttu-id="9b235-303">可能获得的最高分数。</span><span class="sxs-lookup"><span data-stu-id="9b235-303">The maximum number of points that could be earned.</span></span> |
    | <span data-ttu-id="9b235-304">根\\调查表\\问题</span><span class="sxs-lookup"><span data-stu-id="9b235-304">Root\\Questionnaire\\Question</span></span>                                 | <span data-ttu-id="9b235-305">记录列表</span><span class="sxs-lookup"><span data-stu-id="9b235-305">Record list</span></span> | <span data-ttu-id="9b235-306">当前调查表的问题列表。</span><span class="sxs-lookup"><span data-stu-id="9b235-306">The list of questions for the current questionnaire.</span></span> |
    | <span data-ttu-id="9b235-307">根\\调查表\\问题\\集合序列号</span><span class="sxs-lookup"><span data-stu-id="9b235-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="9b235-308">整数</span><span class="sxs-lookup"><span data-stu-id="9b235-308">Integer</span></span>     | <span data-ttu-id="9b235-309">当前答案集合的序列号。</span><span class="sxs-lookup"><span data-stu-id="9b235-309">The sequence number of the current answer collection.</span></span> |
    | <span data-ttu-id="9b235-310">根\\调查表\\问题\\ID</span><span class="sxs-lookup"><span data-stu-id="9b235-310">Root\\Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="9b235-311">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-311">String</span></span>      | <span data-ttu-id="9b235-312">当前问题的标识代码。</span><span class="sxs-lookup"><span data-stu-id="9b235-312">The identification code of the current question.</span></span> |
    | <span data-ttu-id="9b235-313">根\\调查表\\问题\\必须完成</span><span class="sxs-lookup"><span data-stu-id="9b235-313">Root\\Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="9b235-314">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-314">String</span></span>      | <span data-ttu-id="9b235-315">指示是否必须回答当前问题的标记。</span><span class="sxs-lookup"><span data-stu-id="9b235-315">A flag that indicates whether the current question must be answered.</span></span> |
    | <span data-ttu-id="9b235-316">根\\调查表\\问题\\主要问题</span><span class="sxs-lookup"><span data-stu-id="9b235-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="9b235-317">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-317">String</span></span>      | <span data-ttu-id="9b235-318">指示当前问题是否是主要问题的标记。</span><span class="sxs-lookup"><span data-stu-id="9b235-318">A flag that indicates whether the current question is primary.</span></span> |
    | <span data-ttu-id="9b235-319">根\\调查表\\问题\\序列号</span><span class="sxs-lookup"><span data-stu-id="9b235-319">Root\\Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="9b235-320">整数</span><span class="sxs-lookup"><span data-stu-id="9b235-320">Integer</span></span>     | <span data-ttu-id="9b235-321">当前问题的序列号。</span><span class="sxs-lookup"><span data-stu-id="9b235-321">The sequence number of the current question.</span></span> |
    | <span data-ttu-id="9b235-322">根\\调查表\\问题\\文本</span><span class="sxs-lookup"><span data-stu-id="9b235-322">Root\\Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="9b235-323">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-323">String</span></span>      | <span data-ttu-id="9b235-324">当前问题的文本。</span><span class="sxs-lookup"><span data-stu-id="9b235-324">The text of the current question.</span></span> |
    | <span data-ttu-id="9b235-325">根\\调查表\\问题\\答案</span><span class="sxs-lookup"><span data-stu-id="9b235-325">Root\\Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="9b235-326">记录列表</span><span class="sxs-lookup"><span data-stu-id="9b235-326">Record list</span></span> | <span data-ttu-id="9b235-327">当前问题的答案列表。</span><span class="sxs-lookup"><span data-stu-id="9b235-327">The list of answers for the current question.</span></span> |
    | <span data-ttu-id="9b235-328">根\\调查表\\问题\\答案\\正确答案</span><span class="sxs-lookup"><span data-stu-id="9b235-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="9b235-329">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-329">String</span></span>      | <span data-ttu-id="9b235-330">指示当前答案是否正确的标记。</span><span class="sxs-lookup"><span data-stu-id="9b235-330">A flag that indicates whether the current answer is correct.</span></span> |
    | <span data-ttu-id="9b235-331">根\\调查表\\问题\\答案\\分数</span><span class="sxs-lookup"><span data-stu-id="9b235-331">Root\\Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="9b235-332">实数</span><span class="sxs-lookup"><span data-stu-id="9b235-332">Real</span></span>        | <span data-ttu-id="9b235-333">选择当前答案获得的分数。</span><span class="sxs-lookup"><span data-stu-id="9b235-333">The points that are earned when the current answer is selected.</span></span> |
    | <span data-ttu-id="9b235-334">根\\调查表\\问题\\答案\\序列号</span><span class="sxs-lookup"><span data-stu-id="9b235-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="9b235-335">整数</span><span class="sxs-lookup"><span data-stu-id="9b235-335">Integer</span></span>     | <span data-ttu-id="9b235-336">当前答案的序列号。</span><span class="sxs-lookup"><span data-stu-id="9b235-336">The sequence number of the current answer.</span></span> |
    | <span data-ttu-id="9b235-337">根\\调查表\\问题\\答案\\文本</span><span class="sxs-lookup"><span data-stu-id="9b235-337">Root\\Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="9b235-338">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-338">String</span></span>      | <span data-ttu-id="9b235-339">当前答案的文本。</span><span class="sxs-lookup"><span data-stu-id="9b235-339">The text of the current answer.</span></span> |

    <span data-ttu-id="9b235-340">下图显示了 **数据模型设计器** 页上完成的可编辑数据模型。</span><span class="sxs-lookup"><span data-stu-id="9b235-340">The following illustration shows the completed editable data model on the **Data model designer** page.</span></span>

    ![ER 数据模型设计器中配置的数据模型](./media/er-quick-start1-model2.png)

7. <span data-ttu-id="9b235-342">保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="9b235-342">Save your changes.</span></span>
8. <span data-ttu-id="9b235-343">关闭 **数据模型设计器** 页。</span><span class="sxs-lookup"><span data-stu-id="9b235-343">Close the **Data model designer** page.</span></span>

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a><span data-ttu-id="9b235-344">完成数据模型的设计</span><span class="sxs-lookup"><span data-stu-id="9b235-344">Complete the design of the data model</span></span>

1. <span data-ttu-id="9b235-345">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="9b235-345">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9b235-346">在 **配置** 页上的配置树中，选择 **调查表模型**。</span><span class="sxs-lookup"><span data-stu-id="9b235-346">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="9b235-347">在 **版本** 快速选项卡上，选择状态为 **草稿** 的配置版本。</span><span class="sxs-lookup"><span data-stu-id="9b235-347">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="9b235-348">选择 **更改状态** \> **完成**。</span><span class="sxs-lookup"><span data-stu-id="9b235-348">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="9b235-349">此配置的版本 1 的状态将从 **草稿** 更改为 **已完成**。</span><span class="sxs-lookup"><span data-stu-id="9b235-349">The status of version 1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="9b235-350">版本 1 不能再更改。</span><span class="sxs-lookup"><span data-stu-id="9b235-350">Version 1 can no longer be changed.</span></span> <span data-ttu-id="9b235-351">此版本包含已配置的数据模型，可以用作其他 ER 配置的基础。</span><span class="sxs-lookup"><span data-stu-id="9b235-351">This version contains the configured data model and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="9b235-352">此配置的版本 2 将创建，状态为 **草稿**。</span><span class="sxs-lookup"><span data-stu-id="9b235-352">Version 2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="9b235-353">您可以编辑此版本来调整 **调查表** 数据模型。</span><span class="sxs-lookup"><span data-stu-id="9b235-353">You can edit this version to adjust the **Questionnaire** data model.</span></span>

![“配置”页上可编辑 ER 配置的版本](./media/er-quick-start1-model-configuration.png)

<span data-ttu-id="9b235-355">有关 ER 配置的版本控制的详细信息，请参阅[电子报告 (ER) 概述](general-electronic-reporting.md#component-versioning)。</span><span class="sxs-lookup"><span data-stu-id="9b235-355">For more information about versioning for ER configurations, see [Electronic reporting (ER) overview](general-electronic-reporting.md#component-versioning).</span></span>

> [!NOTE]
> <span data-ttu-id="9b235-356">配置的数据模型是 **调查表** 业务域的抽象表示，不包含与 Microsoft Dynamics 365 Finance 特定的伪像的关系。</span><span class="sxs-lookup"><span data-stu-id="9b235-356">The configured data model is your abstract representation of the **Questionnaire** business domain and contains no relations to artefacts that are specific to Microsoft Dynamics 365 Finance.</span></span>

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a><span data-ttu-id="9b235-357">为配置的数据模型设计模型映射</span><span class="sxs-lookup"><span data-stu-id="9b235-357">Design a model mapping for the configured data model</span></span>

<span data-ttu-id="9b235-358">作为电子报告开发人员角色的用户，您必须为 **调查表** 数据模型创建一个新的 ER 配置，其中包含[模型映射](general-electronic-reporting.md#data-model-and-model-mapping-components)组件。</span><span class="sxs-lookup"><span data-stu-id="9b235-358">As a user in the Electronic Reporting Developer role, you must create a new ER configuration that contains a [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** data model.</span></span> <span data-ttu-id="9b235-359">由于此组件为 Finance 实现配置的数据模型，因此它是 Finance 特定组件。</span><span class="sxs-lookup"><span data-stu-id="9b235-359">Because this component implements the configured data model for Finance, it's Finance-specific.</span></span> <span data-ttu-id="9b235-360">您必须配置模型映射组件来指定必须用于在运行时使用应用程序数据填充配置的数据模型的应用程序对象。</span><span class="sxs-lookup"><span data-stu-id="9b235-360">You must configure the model mapping component to specify the application objects that must be used to fill in the configured data model with application data at runtime.</span></span> <span data-ttu-id="9b235-361">要完成此任务，您必须了解 Finance 中 **调查表** 业务域的数据结构的实现详细信息。</span><span class="sxs-lookup"><span data-stu-id="9b235-361">To complete this task, you must be aware of the implementation details of the data structure of the **Questionnaire** business domain in Finance.</span></span>

<span data-ttu-id="9b235-362">通过完成后面的[导入新模型映射配置](#ImportModelMapping)一节的步骤，可以从提供的 XML 文件导入所需的模型映射配置。</span><span class="sxs-lookup"><span data-stu-id="9b235-362">By completing the steps in the [Import a new model mapping configuration](#ImportModelMapping) section that follows, you can import the required model mapping configuration from the provided XML file.</span></span> <span data-ttu-id="9b235-363">或者，您可以完成[创建新模型映射配置](#CreateModelMapping)一节的步骤来从头开始设计此模型映射。</span><span class="sxs-lookup"><span data-stu-id="9b235-363">Alternatively, you can complete the steps in the [Create a new model mapping configuration](#CreateModelMapping) section to design this model mapping from scratch.</span></span>

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a><span data-ttu-id="9b235-364">导入新模型映射配置</span><span class="sxs-lookup"><span data-stu-id="9b235-364">Import a new model mapping configuration</span></span>

1. <span data-ttu-id="9b235-365">下载 [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) 文件，并将其保存到本地计算机。</span><span class="sxs-lookup"><span data-stu-id="9b235-365">Download the [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="9b235-366">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="9b235-366">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="9b235-367">在 **电子报告** 工作区中，选择 **报告配置**。</span><span class="sxs-lookup"><span data-stu-id="9b235-367">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="9b235-368">在操作窗格上，选择 **交换** \> **从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="9b235-368">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="9b235-369">选择 **浏览**，然后找到并选择 **Questionnaires mapping.version.1.1.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="9b235-369">Select **Browse**, and then find and select the **Questionnaires mapping.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="9b235-370">选择 **确定** 导入配置。</span><span class="sxs-lookup"><span data-stu-id="9b235-370">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="9b235-371">要继续，跳过下一个过程[创建新模型映射配置](#CreateModelMapping)。</span><span class="sxs-lookup"><span data-stu-id="9b235-371">To continue, skip the next procedure, [Create a new model mapping configuration](#CreateModelMapping).</span></span>

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a><span data-ttu-id="9b235-372">创建新模型映射配置</span><span class="sxs-lookup"><span data-stu-id="9b235-372">Create a new model mapping configuration</span></span>

1. <span data-ttu-id="9b235-373">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="9b235-373">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9b235-374">在 **配置** 页上的配置树中，选择 **调查表模型**。</span><span class="sxs-lookup"><span data-stu-id="9b235-374">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="9b235-375">选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="9b235-375">Select **Create configuration**.</span></span>
4. <span data-ttu-id="9b235-376">在下拉对话框中，执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="9b235-376">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="9b235-377">在 **新建** 字段中，选择 **基于数据模型调查表的模型映射**。</span><span class="sxs-lookup"><span data-stu-id="9b235-377">In the **New** field, select **Model Mapping based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="9b235-378">在 **名称** 字段中输入 **调查表映射**。</span><span class="sxs-lookup"><span data-stu-id="9b235-378">In the **Name** field, enter **Questionnaire mapping**.</span></span>
    3. <span data-ttu-id="9b235-379">在 **数据模型定义** 字段中，选择 **根** 定义。</span><span class="sxs-lookup"><span data-stu-id="9b235-379">In the **Data model definition** field, select the **Root** definition.</span></span>
    4. <span data-ttu-id="9b235-380">选择 **创建配置** 以创建配置。</span><span class="sxs-lookup"><span data-stu-id="9b235-380">Select **Create configuration** to create the configuration.</span></span>

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a><span data-ttu-id="9b235-381">设计新模型映射组件</span><span class="sxs-lookup"><span data-stu-id="9b235-381">Design a new model mapping component</span></span>

1. <span data-ttu-id="9b235-382">在 **配置** 页上的配置树中，选择 **调查表映射**。</span><span class="sxs-lookup"><span data-stu-id="9b235-382">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
2. <span data-ttu-id="9b235-383">选择 **设计器** 来打开映射列表。</span><span class="sxs-lookup"><span data-stu-id="9b235-383">Select **Designer** to open the list of mappings.</span></span>
3. <span data-ttu-id="9b235-384">选择为 **根** 定义自动添加的 **调查表映射** 映射。</span><span class="sxs-lookup"><span data-stu-id="9b235-384">Select the **Questionnaires mapping** mapping that was automatically added for the **Root** definition</span></span>
4. <span data-ttu-id="9b235-385">选择 **设计器** 开始配置选定的映射。</span><span class="sxs-lookup"><span data-stu-id="9b235-385">Select **Designer** to start to configure the selected mapping.</span></span>

<span data-ttu-id="9b235-386">系统会自动为 **根** 定义添加新映射。</span><span class="sxs-lookup"><span data-stu-id="9b235-386">A new mapping is automatically added for the **Root** definition.</span></span> <span data-ttu-id="9b235-387">此映射具有 **到模型** 方向。</span><span class="sxs-lookup"><span data-stu-id="9b235-387">This mapping has the **To model** direction.</span></span> <span data-ttu-id="9b235-388">因此，此映射可用于使用所需数据填充数据模型。</span><span class="sxs-lookup"><span data-stu-id="9b235-388">Therefore, this mapping can be used to fill in a data model with required data.</span></span>

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a><span data-ttu-id="9b235-389">添加数据源以访问应用程序表</span><span class="sxs-lookup"><span data-stu-id="9b235-389">Add data sources to access application tables</span></span>

<span data-ttu-id="9b235-390">您必须配置数据源以访问包含调查表详细信息的应用程序表。</span><span class="sxs-lookup"><span data-stu-id="9b235-390">You must configure data sources to access the application tables that contain questionnaire details.</span></span>

1. <span data-ttu-id="9b235-391">在 **模型映射设计器** 页的 **数据源类型** 窗格中，选择 **Dynamics 365 for Operations\\表记录**。</span><span class="sxs-lookup"><span data-stu-id="9b235-391">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="9b235-392">添加将用于访问 KMCollection 表的新数据源，其中每个记录代表一个调查表：</span><span class="sxs-lookup"><span data-stu-id="9b235-392">Add a new data source that will be used to access the KMCollection table, where every record represents a single questionnaire:</span></span>

    1. <span data-ttu-id="9b235-393">在 **数据源** 窗格中，选择 **添加根**。</span><span class="sxs-lookup"><span data-stu-id="9b235-393">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="9b235-394">在对话框的 **名称** 字段中，输入 **调查表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-394">In dialog box, in the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="9b235-395">在 **表** 字段中，输入 **KMCollection**。</span><span class="sxs-lookup"><span data-stu-id="9b235-395">In the **Table** field, enter **KMCollection**.</span></span>
    4. <span data-ttu-id="9b235-396">将 **要求查询** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="9b235-396">Set the **Ask for query** option to **Yes**.</span></span> <span data-ttu-id="9b235-397">然后，您可以在运行时在系统查询对话框中为此表指定[筛选](../../fin-ops/get-started/advanced-filtering-query-options.md)选项。</span><span class="sxs-lookup"><span data-stu-id="9b235-397">You will then be able to specify [filtering](../../fin-ops/get-started/advanced-filtering-query-options.md) options for this table in the system query dialog box at runtime.</span></span>
    5. <span data-ttu-id="9b235-398">选择 **确定** 添加新数据源。</span><span class="sxs-lookup"><span data-stu-id="9b235-398">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="9b235-399">在 **数据源类型** 窗格中，选择 **Dynamics 365 for Operations\\表记录**。</span><span class="sxs-lookup"><span data-stu-id="9b235-399">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
4. <span data-ttu-id="9b235-400">添加将用于访问 KMQuestion 表的新数据源，其中每个记录代表调查表中的一个问题：</span><span class="sxs-lookup"><span data-stu-id="9b235-400">Add a new data source that will be used to access the KMQuestion table, where every record represents a single question in a questionnaire:</span></span>

    1. <span data-ttu-id="9b235-401">在 **数据源** 窗格中，选择 **添加根**。</span><span class="sxs-lookup"><span data-stu-id="9b235-401">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="9b235-402">在对话框的 **名称** 字段中，输入 **问题**。</span><span class="sxs-lookup"><span data-stu-id="9b235-402">In the dialog box, in the **Name** field, enter **Question**.</span></span>
    3. <span data-ttu-id="9b235-403">在 **表** 字段中，输入 **KMQuestion**。</span><span class="sxs-lookup"><span data-stu-id="9b235-403">In the **Table** field, enter **KMQuestion**.</span></span>
    4. <span data-ttu-id="9b235-404">选择 **确定** 添加新数据源。</span><span class="sxs-lookup"><span data-stu-id="9b235-404">Select **OK** to add the new data source.</span></span>

5. <span data-ttu-id="9b235-405">在 **数据源类型** 窗格中，选择 **Dynamics 365 for Operations\\表记录**。</span><span class="sxs-lookup"><span data-stu-id="9b235-405">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
6. <span data-ttu-id="9b235-406">添加将用于访问 KMAnswer 表的新数据源尝试，其中每个记录代表调查表中问题的一个答案：</span><span class="sxs-lookup"><span data-stu-id="9b235-406">Add a new data source try that will be used to access the KMAnswer table, where every record represents a single answer to a question in a questionnaire:</span></span>

    1. <span data-ttu-id="9b235-407">在 **数据源** 窗格中，选择 **添加根**。</span><span class="sxs-lookup"><span data-stu-id="9b235-407">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="9b235-408">在 **名称** 字段中，输入 **答案**。</span><span class="sxs-lookup"><span data-stu-id="9b235-408">In the **Name** field, enter **Answer**.</span></span>
    3. <span data-ttu-id="9b235-409">在 **表** 字段中，输入 **KMAnswer**。</span><span class="sxs-lookup"><span data-stu-id="9b235-409">In the **Table** field, enter **KMAnswer**.</span></span>
    4. <span data-ttu-id="9b235-410">选择 **确定** 添加新数据源。</span><span class="sxs-lookup"><span data-stu-id="9b235-410">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="9b235-411">在 **数据源类型** 窗格中，选择 **函数\\计算字段**。</span><span class="sxs-lookup"><span data-stu-id="9b235-411">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="9b235-412">添加将用于从父 KMCollection 表的每个记录访问 KMQuestionResultGroup 表的记录的新计算字段：</span><span class="sxs-lookup"><span data-stu-id="9b235-412">Add a new calculated field that will be used to access a record of the KMQuestionResultGroup table from every record of the parent KMCollection table:</span></span>

    1. <span data-ttu-id="9b235-413">在 **数据源** 窗格中，选择 **调查表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-413">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="9b235-414">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="9b235-414">Select **Add**.</span></span>
    3. <span data-ttu-id="9b235-415">在对话框的 **名称** 字段中，输入 **\$ResultGroup**。</span><span class="sxs-lookup"><span data-stu-id="9b235-415">In the dialog box, in the **Name** field, enter **\$ResultGroup**.</span></span>
    4. <span data-ttu-id="9b235-416">选择 **编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="9b235-416">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="9b235-417">在 [ER 公式编辑器](general-electronic-reporting-formula-designer.md)中，在 **公式** 字段中，输入 **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** 以使用 KMCollection 和 KMQuestionResultGroup 表之间的一对多关系的[路径](er-formula-language.md#paths)。</span><span class="sxs-lookup"><span data-stu-id="9b235-417">In the [ER formula editor](general-electronic-reporting-formula-designer.md), in the **Formula** field, enter **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** to use the [path](er-formula-language.md#paths) of the one-to-many relation between the KMCollection and KMQuestionResultGroup tables.</span></span>
    6. <span data-ttu-id="9b235-418">选择 **保存**，然后关闭公式编辑器。</span><span class="sxs-lookup"><span data-stu-id="9b235-418">Select **Save**, and close the formula editor.</span></span>
    7. <span data-ttu-id="9b235-419">选择 **确定** 添加新计算字段。</span><span class="sxs-lookup"><span data-stu-id="9b235-419">Select **OK** to add the new calculated field.</span></span>

9. <span data-ttu-id="9b235-420">在 **数据源类型** 窗格中，选择 **函数\\计算字段**。</span><span class="sxs-lookup"><span data-stu-id="9b235-420">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
10. <span data-ttu-id="9b235-421">添加将用于从父 KMCollectionQuestion 表的每个记录访问 KMQuestion 表的问题记录的新计算字段：</span><span class="sxs-lookup"><span data-stu-id="9b235-421">Add a new calculated field that will be used to access question records of the KMQuestion table from every record of the parent KMCollectionQuestion table:</span></span>

    1. <span data-ttu-id="9b235-422">在 **数据源** 窗格中，选择 **调查表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-422">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="9b235-423">展开包含 KMCollection 表的一对多关系的 **\<Relations** 节点。</span><span class="sxs-lookup"><span data-stu-id="9b235-423">Expand the **\<Relations** node that contains one-to-many relations of the KMCollection table.</span></span>
    3. <span data-ttu-id="9b235-424">选择相关的 **KMCollectionQuestion** 表，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="9b235-424">Select the related **KMCollectionQuestion** table, and then select **Add**.</span></span>
    4. <span data-ttu-id="9b235-425">在对话框的 **名称** 字段中，输入 **\$Question**。</span><span class="sxs-lookup"><span data-stu-id="9b235-425">In the dialog box, in the **Name** field, enter **\$Question**.</span></span>
    5. <span data-ttu-id="9b235-426">选择 **编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="9b235-426">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="9b235-427">在公式编辑器的 **公式** 字段中，输入 **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** 以从 KMQuestion 表返回相应的问题记录。</span><span class="sxs-lookup"><span data-stu-id="9b235-427">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** to return the appropriate question records from the KMQuestion table.</span></span>
    7. <span data-ttu-id="9b235-428">选择 **保存**，然后关闭公式编辑器。</span><span class="sxs-lookup"><span data-stu-id="9b235-428">Select **Save**, and close the formula editor.</span></span>
    8. <span data-ttu-id="9b235-429">选择 **确定** 添加新计算字段。</span><span class="sxs-lookup"><span data-stu-id="9b235-429">Select **OK** to add the new calculated field.</span></span>

11. <span data-ttu-id="9b235-430">在 **数据源类型** 窗格中，选择 **函数\\计算字段**。</span><span class="sxs-lookup"><span data-stu-id="9b235-430">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
12. <span data-ttu-id="9b235-431">添加将用于从父 KMQuestion 表的每个记录访问 KMAnswer 表的答案记录的新计算字段：</span><span class="sxs-lookup"><span data-stu-id="9b235-431">Add a new calculated field that will be used to access answer records of the KMAnswer table from every record of the parent KMQuestion table:</span></span>

    1. <span data-ttu-id="9b235-432">在 **数据源** 窗格中，选择 **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="9b235-432">In the **Data sources** pane, select **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, and then select **Add**.</span></span>
    2. <span data-ttu-id="9b235-433">在对话框的 **名称** 字段中，输入 **\$Answer**。</span><span class="sxs-lookup"><span data-stu-id="9b235-433">In the dialog box, in the **Name** field, enter **\$Answer**.</span></span>
    3. <span data-ttu-id="9b235-434">选择 **编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="9b235-434">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="9b235-435">在公式编辑器的 **公式** 字段中，输入 **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** 以从 KMAnswer 表返回相应的答案记录。</span><span class="sxs-lookup"><span data-stu-id="9b235-435">In the formula editor, in the **Formula** field, enter **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** to return the appropriate answer records from the KMAnswer table.</span></span>
    5. <span data-ttu-id="9b235-436">选择 **保存**，然后关闭公式编辑器。</span><span class="sxs-lookup"><span data-stu-id="9b235-436">Select **Save**, and close the formula editor.</span></span>
    6. <span data-ttu-id="9b235-437">选择 **确定** 添加新计算字段。</span><span class="sxs-lookup"><span data-stu-id="9b235-437">Select **OK** to add the new calculated field.</span></span>

13. <span data-ttu-id="9b235-438">在 **数据源类型** 窗格中，选择 **Dynamics 365 for Operations\\表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-438">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table**.</span></span>
14. <span data-ttu-id="9b235-439">添加将用于访问 CompanyInfo 表的方法的新数据源。</span><span class="sxs-lookup"><span data-stu-id="9b235-439">Add a new data source that will be used to access methods of the CompanyInfo table.</span></span> <span data-ttu-id="9b235-440">请注意，此表的 **find()** 方法将返回一条记录，该记录表示在其上下文中调用此映射的当前 Finance 实例的公司。</span><span class="sxs-lookup"><span data-stu-id="9b235-440">Note that the **find()** method of this table returns a record that represents a company of the current Finance instance that this mapping is called in the context of.</span></span>

    1. <span data-ttu-id="9b235-441">在 **数据源** 窗格中，选择 **添加根**。</span><span class="sxs-lookup"><span data-stu-id="9b235-441">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="9b235-442">在对话框的 **名称** 字段中，输入 **公司信息**。</span><span class="sxs-lookup"><span data-stu-id="9b235-442">In the dialog box, in the **Name** field, enter **CompanyInfo**.</span></span>
    3. <span data-ttu-id="9b235-443">在 **表** 字段中，输入 **公司信息**。</span><span class="sxs-lookup"><span data-stu-id="9b235-443">In the **Table** field, enter **CompanyInfo**.</span></span>
    4. <span data-ttu-id="9b235-444">选择 **确定** 添加新数据源。</span><span class="sxs-lookup"><span data-stu-id="9b235-444">Select **OK** to add the new data source.</span></span>

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a><span data-ttu-id="9b235-445">添加数据源以访问应用程序枚举</span><span class="sxs-lookup"><span data-stu-id="9b235-445">Add data sources to access application enumerations</span></span>

<span data-ttu-id="9b235-446">您必须配置数据源以访问应用程序枚举，并将其值与应用程序表中 **枚举** 类型的字段的值进行比较。</span><span class="sxs-lookup"><span data-stu-id="9b235-446">You must configure data sources to access application enumerations and compare their values with values of fields of the **Enumeration** type in the application tables.</span></span> <span data-ttu-id="9b235-447">您必须使用比较的结果来填充数据模型的相应字段。</span><span class="sxs-lookup"><span data-stu-id="9b235-447">You must use the result of the comparison to fill in appropriate fields of the data model.</span></span>

1. <span data-ttu-id="9b235-448">在 **模型映射设计器** 页的 **数据源类型** 窗格中，选择 **Dynamics 365 for Operations\\枚举**。</span><span class="sxs-lookup"><span data-stu-id="9b235-448">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
2. <span data-ttu-id="9b235-449">添加将用于访问 **EnumAppNoYes** 枚举的值的新数据源。</span><span class="sxs-lookup"><span data-stu-id="9b235-449">Add a new data source that will be used to access values of the **EnumAppNoYes** enumeration:</span></span>

    1. <span data-ttu-id="9b235-450">在 **数据源** 窗格中，选择 **添加根**。</span><span class="sxs-lookup"><span data-stu-id="9b235-450">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="9b235-451">在对话框的 **名称** 字段中，输入 **EnumAppNoYes**。</span><span class="sxs-lookup"><span data-stu-id="9b235-451">In the dialog box, in the **Name** field, enter **EnumAppNoYes**.</span></span>
    3. <span data-ttu-id="9b235-452">在 **枚举** 字段中，输入 **NoYes**。</span><span class="sxs-lookup"><span data-stu-id="9b235-452">In the **Enumeration** field, enter **NoYes**.</span></span>
    4. <span data-ttu-id="9b235-453">选择 **确定** 添加新数据源。</span><span class="sxs-lookup"><span data-stu-id="9b235-453">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="9b235-454">在 **数据源类型** 窗格中，选择 **Dynamics 365 for Operations\\枚举**。</span><span class="sxs-lookup"><span data-stu-id="9b235-454">In the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
4. <span data-ttu-id="9b235-455">添加将用于访问 **KMCollectionQuestionMode** 枚举的值的新数据源。</span><span class="sxs-lookup"><span data-stu-id="9b235-455">Add a new data source that will be used to access the values of the **KMCollectionQuestionMode** enumeration:</span></span>

    1. <span data-ttu-id="9b235-456">在 **数据源** 窗格中，选择 **添加根**。</span><span class="sxs-lookup"><span data-stu-id="9b235-456">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="9b235-457">在对话框的 **名称** 字段中，输入 **EnumAppQuestionOrder**。</span><span class="sxs-lookup"><span data-stu-id="9b235-457">In the dialog box, in the **Name** field, enter **EnumAppQuestionOrder**.</span></span>
    3. <span data-ttu-id="9b235-458">在 **枚举** 字段中，输入 **KMCollectionQuestionMode**。</span><span class="sxs-lookup"><span data-stu-id="9b235-458">In the **Enumeration** field, enter **KMCollectionQuestionMode**.</span></span>
    4. <span data-ttu-id="9b235-459">选择 **确定** 添加新数据源。</span><span class="sxs-lookup"><span data-stu-id="9b235-459">Select **OK** to add the new data source.</span></span>

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a><span data-ttu-id="9b235-460">添加 ER 标签以指定语言生成报表</span><span class="sxs-lookup"><span data-stu-id="9b235-460">Add ER labels to generate a report in a specified language</span></span>

<span data-ttu-id="9b235-461">您可以添加 ER 标签来配置一些数据源以返回取决于在模型映射调用的上下文中定义的语言的值。</span><span class="sxs-lookup"><span data-stu-id="9b235-461">You can add ER labels to configure some of your data sources to return values that depend on the language that is defined in the context of the model mapping's call.</span></span>

1. <span data-ttu-id="9b235-462">在 **模型映射设计器** 页的 **数据源** 窗格中，选择 **答案**，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="9b235-462">On the **Model mapping designer** page, in the **Data sources** pane, select **Answer**, and then select **Edit**.</span></span>
2. <span data-ttu-id="9b235-463">激活 **标签** 字段。</span><span class="sxs-lookup"><span data-stu-id="9b235-463">Activate the **Label** field.</span></span>
3. <span data-ttu-id="9b235-464">选择 **翻译**。</span><span class="sxs-lookup"><span data-stu-id="9b235-464">Select **Translate**.</span></span>
4. <span data-ttu-id="9b235-465">在 **文本翻译** 对话框中，执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="9b235-465">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="9b235-466">在 **标签 ID** 字段中，输入 **PositiveAnswer**。</span><span class="sxs-lookup"><span data-stu-id="9b235-466">In the **Label Id** field, enter **PositiveAnswer**.</span></span>
    2. <span data-ttu-id="9b235-467">在 **语言为默认语言的文本** 字段中，输入 **是**。</span><span class="sxs-lookup"><span data-stu-id="9b235-467">In the **Text in default language** field, enter **Yes**.</span></span>
    3. <span data-ttu-id="9b235-468">选择 **翻译**。</span><span class="sxs-lookup"><span data-stu-id="9b235-468">Select **Translate**.</span></span>
    4. <span data-ttu-id="9b235-469">在 **标签 ID** 字段中，输入 **NegativeAnswer**。</span><span class="sxs-lookup"><span data-stu-id="9b235-469">In the **Label Id** field, enter **NegativeAnswer**.</span></span>
    5. <span data-ttu-id="9b235-470">在 **语言为默认语言的文本** 字段中，输入 **否**。</span><span class="sxs-lookup"><span data-stu-id="9b235-470">In the **Text in default language** field, enter **No**.</span></span>
    6. <span data-ttu-id="9b235-471">选择 **翻译**。</span><span class="sxs-lookup"><span data-stu-id="9b235-471">Select **Translate**.</span></span>

5. <span data-ttu-id="9b235-472">关闭 **文本翻译** 对话框。</span><span class="sxs-lookup"><span data-stu-id="9b235-472">Close the **Text translation** dialog box.</span></span>
6. <span data-ttu-id="9b235-473">选择 **取消**。</span><span class="sxs-lookup"><span data-stu-id="9b235-473">Select **Cancel**.</span></span>

![为可编辑模型映射添加 ER 标签](./media/er-quick-start1-adding-labels.png)

<span data-ttu-id="9b235-475">您仅为默认语言输入了 ER 标签。</span><span class="sxs-lookup"><span data-stu-id="9b235-475">You've entered ER labels only for the default language.</span></span> <span data-ttu-id="9b235-476">有关如何将 ER 标签翻译为其他语言的信息，请参阅[设计多语言报表](er-design-multilingual-reports.md)。</span><span class="sxs-lookup"><span data-stu-id="9b235-476">For information about how ER labels can be translated into other languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a><span data-ttu-id="9b235-477">添加数据源以将比较枚举值的结果转换为文本值</span><span class="sxs-lookup"><span data-stu-id="9b235-477">Add a data source to transform the results of comparing enumeration values to a text value</span></span>

<span data-ttu-id="9b235-478">因为必须为差异源多次转换枚举值和文本值之间的比较结果，所以最好将此逻辑配置为单个数据源。</span><span class="sxs-lookup"><span data-stu-id="9b235-478">Because you must transform the results of the comparison between enumeration values and text values several times for difference sources, it's a good idea to configure this logic as a single data source.</span></span> <span data-ttu-id="9b235-479">但是，要使此数据源可以重用，必须将其配置为参数化数据源。</span><span class="sxs-lookup"><span data-stu-id="9b235-479">However, to make this data source reusable, you must then configure it as the parametrized data source.</span></span> <span data-ttu-id="9b235-480">有关详细信息，请参阅[支持对计算字段类型的 ER 数据源的参数化调用](er-calculated-field-type.md)。</span><span class="sxs-lookup"><span data-stu-id="9b235-480">For more information, see [Support parameterized calls of ER data sources of the Calculated field type](er-calculated-field-type.md).</span></span>

1. <span data-ttu-id="9b235-481">在 **模型映射设计器** 页的 **数据源类型** 窗格中，选择 **常规\\空容器**。</span><span class="sxs-lookup"><span data-stu-id="9b235-481">On the **Model mapping designer** page, in the **Data source types** pane, select **General\\Empty container**.</span></span>
2. <span data-ttu-id="9b235-482">添加新容器数据源：</span><span class="sxs-lookup"><span data-stu-id="9b235-482">Add a new container data source:</span></span>

    1. <span data-ttu-id="9b235-483">在 **数据源** 窗格中，选择 **添加根**。</span><span class="sxs-lookup"><span data-stu-id="9b235-483">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="9b235-484">在对话框的 **名称** 字段中，输入 **帮助程序**。</span><span class="sxs-lookup"><span data-stu-id="9b235-484">In the dialog box, in the **Name** field, enter **Helper**.</span></span>
    3. <span data-ttu-id="9b235-485">选择 **确定** 添加新容器数据源。</span><span class="sxs-lookup"><span data-stu-id="9b235-485">Select **OK** to add the new container data source.</span></span>

3. <span data-ttu-id="9b235-486">在 **数据源类型** 窗格中，选择 **函数\\计算字段**。</span><span class="sxs-lookup"><span data-stu-id="9b235-486">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="9b235-487">添加新数据源：</span><span class="sxs-lookup"><span data-stu-id="9b235-487">Add a new data source:</span></span>

    1. <span data-ttu-id="9b235-488">在 **数据源** 窗格中，选择 **帮助程序**。</span><span class="sxs-lookup"><span data-stu-id="9b235-488">In the **Data sources** pane, select **Helper**.</span></span>
    2. <span data-ttu-id="9b235-489">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="9b235-489">Select **Add**.</span></span>
    3. <span data-ttu-id="9b235-490">在对话框的 **名称** 字段中，输入 **NoYesEnumToString**。</span><span class="sxs-lookup"><span data-stu-id="9b235-490">In the dialog box, in the **Name** field, enter **NoYesEnumToString**.</span></span>
    4. <span data-ttu-id="9b235-491">选择 **编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="9b235-491">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="9b235-492">在公式编辑器中，选择 **参数**。</span><span class="sxs-lookup"><span data-stu-id="9b235-492">In the formula editor, select **Parameters**.</span></span>
    6. <span data-ttu-id="9b235-493">按照以下步骤为配置的表达式指定参数：</span><span class="sxs-lookup"><span data-stu-id="9b235-493">Follow these steps to specify parameters for the configured expression:</span></span>

        1. <span data-ttu-id="9b235-494">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="9b235-494">Select **New**.</span></span>
        2. <span data-ttu-id="9b235-495">在对话框的 **名称** 字段中，输入 **参数**。</span><span class="sxs-lookup"><span data-stu-id="9b235-495">In the dialog box, in the **Name** field, enter **Argument**.</span></span>
        3. <span data-ttu-id="9b235-496">在 **类型** 字段中，选择 **布尔** 数据类型。</span><span class="sxs-lookup"><span data-stu-id="9b235-496">In the **Type** field, select the **Boolean** data type.</span></span>
        4. <span data-ttu-id="9b235-497">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="9b235-497">Select **OK**.</span></span>

    7. <span data-ttu-id="9b235-498">在 **公式** 字段中，输入 **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")**，以根据执行上下文的语言和指定参数的值返回相应的 ER 标签的文本。</span><span class="sxs-lookup"><span data-stu-id="9b235-498">In the **Formula** field, enter **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** to return the text of the appropriate ER label, depending on the language of the execution context and value of the specified parameter.</span></span>
    8. <span data-ttu-id="9b235-499">选择 **保存**，然后关闭公式编辑器。</span><span class="sxs-lookup"><span data-stu-id="9b235-499">Select **Save**, and close the formula editor.</span></span>
    9. <span data-ttu-id="9b235-500">选择 **确定** 添加新数据源。</span><span class="sxs-lookup"><span data-stu-id="9b235-500">Select **OK** to add the new data source.</span></span>

![ER 模型映射设计器中配置的模型映射](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a><span data-ttu-id="9b235-502">将数据源与数据模型字段绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-502">Bind data sources to data model fields</span></span>

<span data-ttu-id="9b235-503">您必须将配置的数据源与数据模型的字段绑定，来指定在运行时如何使用应用程序数据填充数据模型。</span><span class="sxs-lookup"><span data-stu-id="9b235-503">You must bind the configured data sources to the fields of the data model to specify how the data model will by filled in with application data at runtime.</span></span>

1. <span data-ttu-id="9b235-504">在 **模型映射设计器** 页的 **数据模型** 窗格中，选择 **公司名称**。</span><span class="sxs-lookup"><span data-stu-id="9b235-504">On the **Model mapping designer** page, in the **Data model** pane, select **CompanyName**.</span></span>
2. <span data-ttu-id="9b235-505">在 **数据源** 窗格中，展开 **公司信息**，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="9b235-505">In the **Data sources** pane, expand **CompanyInfo**, and then follow these steps:</span></span>

    1. <span data-ttu-id="9b235-506">展开代表“公司信息”表的 **find()** 方法的 **CompanyInfo.find()** 节点。</span><span class="sxs-lookup"><span data-stu-id="9b235-506">Expand the **CompanyInfo.find()** node that represents the **find()** method of the CompanyInfo table.</span></span>
    2. <span data-ttu-id="9b235-507">选择 **CompanyInfo.find().Name**。</span><span class="sxs-lookup"><span data-stu-id="9b235-507">Select **CompanyInfo.find().Name**.</span></span>
    3. <span data-ttu-id="9b235-508">选择 **绑定** 以在运行时的上下文中填写要调用配置的模型映射的公司的名称。</span><span class="sxs-lookup"><span data-stu-id="9b235-508">Select **Bind** to fill in the name of the company that the configured model mapping is called in the context of at runtime.</span></span>

3. <span data-ttu-id="9b235-509">在 **数据模型** 窗格中，选择 **调查表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-509">In the **Data model** pane, select **Questionnaire**.</span></span>
4. <span data-ttu-id="9b235-510">在 **数据源** 窗格中，选择 **调查表**，然后选择 **绑定** 填充调查表记录。</span><span class="sxs-lookup"><span data-stu-id="9b235-510">In the **Data sources** pane, select **Questionnaire**, and then select **Bind** to fill in questionnaire records.</span></span>
5. <span data-ttu-id="9b235-511">在 **数据模型** 窗格中，展开 **调查表**，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="9b235-511">In the **Data model** pane, expand **Questionnaire**, and then follow these steps:</span></span>

    1. <span data-ttu-id="9b235-512">在 **数据模型** 窗格中，选择 **活动**。</span><span class="sxs-lookup"><span data-stu-id="9b235-512">In the **Data model** pane, select **Active**.</span></span>
    2. <span data-ttu-id="9b235-513">在 **数据模型** 窗格中，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="9b235-513">In the **Data model** pane, select **Edit**.</span></span>
    3. <span data-ttu-id="9b235-514">在 **公式** 字段中，输入 **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** 以填充枚举值之间比较的文本相关和语言相关结果。</span><span class="sxs-lookup"><span data-stu-id="9b235-514">In the **Formula** field, enter **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** to fill the text-dependent and language-dependent result of the comparison between enumeration values.</span></span>

6. <span data-ttu-id="9b235-515">继续以相同的方式将数据源绑定到数据模型字段，直到获得以下结果。</span><span class="sxs-lookup"><span data-stu-id="9b235-515">Continue to bind data sources to data model fields in the same manner until you achieve the following result.</span></span>

    | <span data-ttu-id="9b235-516">字段路径</span><span class="sxs-lookup"><span data-stu-id="9b235-516">Field path</span></span>                                              | <span data-ttu-id="9b235-517">数据类型</span><span class="sxs-lookup"><span data-stu-id="9b235-517">Data type</span></span>   | <span data-ttu-id="9b235-518">行动</span><span class="sxs-lookup"><span data-stu-id="9b235-518">Action</span></span> | <span data-ttu-id="9b235-519">绑定表达式</span><span class="sxs-lookup"><span data-stu-id="9b235-519">Binding expression</span></span> |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | <span data-ttu-id="9b235-520">公司名称</span><span class="sxs-lookup"><span data-stu-id="9b235-520">CompanyName</span></span>                                             | <span data-ttu-id="9b235-521">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-521">String</span></span>      | <span data-ttu-id="9b235-522">绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-522">Bind</span></span>   | <span data-ttu-id="9b235-523">CompanyInfo.'find()'.Name</span><span class="sxs-lookup"><span data-stu-id="9b235-523">CompanyInfo.'find()'.Name</span></span> |
    | <span data-ttu-id="9b235-524">调查表</span><span class="sxs-lookup"><span data-stu-id="9b235-524">Questionnaire</span></span>                                           | <span data-ttu-id="9b235-525">记录列表</span><span class="sxs-lookup"><span data-stu-id="9b235-525">Record list</span></span> | <span data-ttu-id="9b235-526">绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-526">Bind</span></span>   | <span data-ttu-id="9b235-527">调查表</span><span class="sxs-lookup"><span data-stu-id="9b235-527">Questionnaire</span></span> |
    | <span data-ttu-id="9b235-528">调查表\\活动</span><span class="sxs-lookup"><span data-stu-id="9b235-528">Questionnaire\\Active</span></span>                                   | <span data-ttu-id="9b235-529">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-529">String</span></span>      | <span data-ttu-id="9b235-530">编辑​​</span><span class="sxs-lookup"><span data-stu-id="9b235-530">Edit</span></span>   | <span data-ttu-id="9b235-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="9b235-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="9b235-532">调查表\\代码</span><span class="sxs-lookup"><span data-stu-id="9b235-532">Questionnaire\\Code</span></span>                                     | <span data-ttu-id="9b235-533">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-533">String</span></span>      | <span data-ttu-id="9b235-534">绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-534">Bind</span></span>   | <span data-ttu-id="9b235-535">\@.kmCollectionId</span><span class="sxs-lookup"><span data-stu-id="9b235-535">\@.kmCollectionId</span></span> |
    | <span data-ttu-id="9b235-536">调查表\\说明</span><span class="sxs-lookup"><span data-stu-id="9b235-536">Questionnaire\\Description</span></span>                              | <span data-ttu-id="9b235-537">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-537">String</span></span>      | <span data-ttu-id="9b235-538">绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-538">Bind</span></span>   | <span data-ttu-id="9b235-539">\@.Description</span><span class="sxs-lookup"><span data-stu-id="9b235-539">\@.Description</span></span> |
    | <span data-ttu-id="9b235-540">调查表\\调查表类型</span><span class="sxs-lookup"><span data-stu-id="9b235-540">Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="9b235-541">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-541">String</span></span>      | <span data-ttu-id="9b235-542">绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-542">Bind</span></span>   | <span data-ttu-id="9b235-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span><span class="sxs-lookup"><span data-stu-id="9b235-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span></span> |
    | <span data-ttu-id="9b235-544">调查表\\问题顺序</span><span class="sxs-lookup"><span data-stu-id="9b235-544">Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="9b235-545">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-545">String</span></span>      | <span data-ttu-id="9b235-546">编辑​​</span><span class="sxs-lookup"><span data-stu-id="9b235-546">Edit</span></span>   | <span data-ttu-id="9b235-547">CASE (\@.questionMode,</span><span class="sxs-lookup"><span data-stu-id="9b235-547">CASE (\@.questionMode,</span></span><br><span data-ttu-id="9b235-548">EnumAppQuestionOrder.Conditional, "Conditional",</span><span class="sxs-lookup"><span data-stu-id="9b235-548">EnumAppQuestionOrder.Conditional, "Conditional",</span></span><br><span data-ttu-id="9b235-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span><span class="sxs-lookup"><span data-stu-id="9b235-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span></span><br><span data-ttu-id="9b235-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span><span class="sxs-lookup"><span data-stu-id="9b235-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span></span><br><span data-ttu-id="9b235-551">EnumAppQuestionOrder.Sequence, "Sequential",</span><span class="sxs-lookup"><span data-stu-id="9b235-551">EnumAppQuestionOrder.Sequence, "Sequential",</span></span><br><span data-ttu-id="9b235-552">"")</span><span class="sxs-lookup"><span data-stu-id="9b235-552">"")</span></span> |
    | <span data-ttu-id="9b235-553">调查表\\结果组</span><span class="sxs-lookup"><span data-stu-id="9b235-553">Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="9b235-554">录制</span><span class="sxs-lookup"><span data-stu-id="9b235-554">Record</span></span>      |        | |
    | <span data-ttu-id="9b235-555">调查表\\结果组\\代码</span><span class="sxs-lookup"><span data-stu-id="9b235-555">Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="9b235-556">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-556">String</span></span>      | <span data-ttu-id="9b235-557">绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-557">Bind</span></span>   | <span data-ttu-id="9b235-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span><span class="sxs-lookup"><span data-stu-id="9b235-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span></span> |
    | <span data-ttu-id="9b235-559">调查表\\结果组\\说明</span><span class="sxs-lookup"><span data-stu-id="9b235-559">Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="9b235-560">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-560">String</span></span>      | <span data-ttu-id="9b235-561">绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-561">Bind</span></span>   | <span data-ttu-id="9b235-562">\@.'\$ResultGroup'.description</span><span class="sxs-lookup"><span data-stu-id="9b235-562">\@.'\$ResultGroup'.description</span></span> |
    | <span data-ttu-id="9b235-563">调查表\\结果组\\最高分数</span><span class="sxs-lookup"><span data-stu-id="9b235-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="9b235-564">实数</span><span class="sxs-lookup"><span data-stu-id="9b235-564">Real</span></span>        | <span data-ttu-id="9b235-565">绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-565">Bind</span></span>   | <span data-ttu-id="9b235-566">\@.'\$ResultGroup'.maxPoint</span><span class="sxs-lookup"><span data-stu-id="9b235-566">\@.'\$ResultGroup'.maxPoint</span></span> |
    | <span data-ttu-id="9b235-567">调查表\\问题</span><span class="sxs-lookup"><span data-stu-id="9b235-567">Questionnaire\\Question</span></span>                                 | <span data-ttu-id="9b235-568">记录列表</span><span class="sxs-lookup"><span data-stu-id="9b235-568">Record list</span></span> | <span data-ttu-id="9b235-569">绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-569">Bind</span></span>   | <span data-ttu-id="9b235-570">\@.'&lt;Relations'.KMCollectionQuestion</span><span class="sxs-lookup"><span data-stu-id="9b235-570">\@.'&lt;Relations'.KMCollectionQuestion</span></span> |
    | <span data-ttu-id="9b235-571">调查表\\问题\\集合序列号</span><span class="sxs-lookup"><span data-stu-id="9b235-571">Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="9b235-572">整数</span><span class="sxs-lookup"><span data-stu-id="9b235-572">Integer</span></span>     | <span data-ttu-id="9b235-573">绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-573">Bind</span></span>   | <span data-ttu-id="9b235-574">\@.answerCollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="9b235-574">\@.answerCollectionSequenceNumber</span></span> |
    | <span data-ttu-id="9b235-575">调查表\\问题\\ID</span><span class="sxs-lookup"><span data-stu-id="9b235-575">Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="9b235-576">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-576">String</span></span>      | <span data-ttu-id="9b235-577">绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-577">Bind</span></span>   | <span data-ttu-id="9b235-578">\@.kmQuestionId</span><span class="sxs-lookup"><span data-stu-id="9b235-578">\@.kmQuestionId</span></span> |
    | <span data-ttu-id="9b235-579">调查表\\问题\\必须完成</span><span class="sxs-lookup"><span data-stu-id="9b235-579">Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="9b235-580">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-580">String</span></span>      | <span data-ttu-id="9b235-581">编辑​​</span><span class="sxs-lookup"><span data-stu-id="9b235-581">Edit</span></span>   | <span data-ttu-id="9b235-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="9b235-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="9b235-583">调查表\\问题\\主要问题</span><span class="sxs-lookup"><span data-stu-id="9b235-583">Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="9b235-584">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-584">String</span></span>      | <span data-ttu-id="9b235-585">绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-585">Bind</span></span>   | <span data-ttu-id="9b235-586">\@.parentQuestionId</span><span class="sxs-lookup"><span data-stu-id="9b235-586">\@.parentQuestionId</span></span> |
    | <span data-ttu-id="9b235-587">调查表\\问题\\序列号</span><span class="sxs-lookup"><span data-stu-id="9b235-587">Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="9b235-588">整数</span><span class="sxs-lookup"><span data-stu-id="9b235-588">Integer</span></span>     | <span data-ttu-id="9b235-589">绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-589">Bind</span></span>   | <span data-ttu-id="9b235-590">\@.SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="9b235-590">\@.SequenceNumber</span></span> |
    | <span data-ttu-id="9b235-591">调查表\\问题\\文本</span><span class="sxs-lookup"><span data-stu-id="9b235-591">Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="9b235-592">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-592">String</span></span>      | <span data-ttu-id="9b235-593">绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-593">Bind</span></span>   | <span data-ttu-id="9b235-594">\@.'\$Question'.text</span><span class="sxs-lookup"><span data-stu-id="9b235-594">\@.'\$Question'.text</span></span> |
    | <span data-ttu-id="9b235-595">调查表\\问题\\答案</span><span class="sxs-lookup"><span data-stu-id="9b235-595">Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="9b235-596">记录列表</span><span class="sxs-lookup"><span data-stu-id="9b235-596">Record list</span></span> | <span data-ttu-id="9b235-597">绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-597">Bind</span></span>   | <span data-ttu-id="9b235-598">\@.'\$Question'.'\$Answer'</span><span class="sxs-lookup"><span data-stu-id="9b235-598">\@.'\$Question'.'\$Answer'</span></span> |
    | <span data-ttu-id="9b235-599">调查表\\问题\\答案\\正确答案</span><span class="sxs-lookup"><span data-stu-id="9b235-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="9b235-600">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-600">String</span></span>      | <span data-ttu-id="9b235-601">编辑​​</span><span class="sxs-lookup"><span data-stu-id="9b235-601">Edit</span></span>   | <span data-ttu-id="9b235-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="9b235-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="9b235-603">调查表\\问题\\答案\\分数</span><span class="sxs-lookup"><span data-stu-id="9b235-603">Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="9b235-604">实数</span><span class="sxs-lookup"><span data-stu-id="9b235-604">Real</span></span>        | <span data-ttu-id="9b235-605">绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-605">Bind</span></span>   | <span data-ttu-id="9b235-606">\@.point</span><span class="sxs-lookup"><span data-stu-id="9b235-606">\@.point</span></span> |
    | <span data-ttu-id="9b235-607">调查表\\问题\\答案\\序列号</span><span class="sxs-lookup"><span data-stu-id="9b235-607">Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="9b235-608">整数</span><span class="sxs-lookup"><span data-stu-id="9b235-608">Integer</span></span>     | <span data-ttu-id="9b235-609">绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-609">Bind</span></span>   | <span data-ttu-id="9b235-610">\@.sequenceNumber</span><span class="sxs-lookup"><span data-stu-id="9b235-610">\@.sequenceNumber</span></span> |
    | <span data-ttu-id="9b235-611">调查表\\问题\\答案\\本文</span><span class="sxs-lookup"><span data-stu-id="9b235-611">Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="9b235-612">字符串</span><span class="sxs-lookup"><span data-stu-id="9b235-612">String</span></span>      | <span data-ttu-id="9b235-613">绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-613">Bind</span></span>   | <span data-ttu-id="9b235-614">\@.text</span><span class="sxs-lookup"><span data-stu-id="9b235-614">\@.text</span></span> |

    <span data-ttu-id="9b235-615">下图显示了 **模型映射设计器** 页面上配置的模型映射的最终状态。</span><span class="sxs-lookup"><span data-stu-id="9b235-615">The following illustration shows the final state of the configured model mapping on the **Model mapping designer** page.</span></span>

    ![ER 模型映射设计器中完全配置的模型映射](./media/er-quick-start1-mapping2.png)

7. <span data-ttu-id="9b235-617">保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="9b235-617">Save your changes.</span></span>
8. <span data-ttu-id="9b235-618">关闭 **模型映射设计器** 页。</span><span class="sxs-lookup"><span data-stu-id="9b235-618">Close the **Model mapping designer** page.</span></span>

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a><span data-ttu-id="9b235-619">完成模型映射的设计</span><span class="sxs-lookup"><span data-stu-id="9b235-619">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="9b235-620">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="9b235-620">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9b235-621">在 **配置** 页上的配置树中，选择 **调查表映射**。</span><span class="sxs-lookup"><span data-stu-id="9b235-621">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="9b235-622">在 **版本** 快速选项卡上，选择状态为 **草稿** 的配置版本。</span><span class="sxs-lookup"><span data-stu-id="9b235-622">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="9b235-623">选择 **更改状态** \> **完成**。</span><span class="sxs-lookup"><span data-stu-id="9b235-623">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="9b235-624">此配置的版本 1.1 的状态将从 **草稿** 更改为 **已完成**。</span><span class="sxs-lookup"><span data-stu-id="9b235-624">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="9b235-625">版本 1.1 不能再更改。</span><span class="sxs-lookup"><span data-stu-id="9b235-625">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="9b235-626">此版本包含已配置的模型映射，可以用作其他 ER 配置的基础。</span><span class="sxs-lookup"><span data-stu-id="9b235-626">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="9b235-627">此配置的版本 1.2 将创建，状态为 **草稿**。</span><span class="sxs-lookup"><span data-stu-id="9b235-627">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="9b235-628">您可以编辑此版本来调整 **调查表映射** 配置。</span><span class="sxs-lookup"><span data-stu-id="9b235-628">You can edit this version to adjust the **Questionnaire mapping** configuration.</span></span>

![“配置”页上可编辑 ER 配置的版本](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> <span data-ttu-id="9b235-630">配置的模型映射是表示 **调查表** 业务域的抽象数据模型的 Finance 特定实现。</span><span class="sxs-lookup"><span data-stu-id="9b235-630">The configured model mapping is your Finance-specific implementation of the abstract data model that represents the **Questionnaire** business domain.</span></span>

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a><span data-ttu-id="9b235-631">为自定义报表设计模板</span><span class="sxs-lookup"><span data-stu-id="9b235-631">Design a template for a custom report</span></span>

<span data-ttu-id="9b235-632">ER 框架使用预定义的模板生成 Microsoft Office 格式（Excel 工作簿或 Word 文档）的报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-632">The ER framework uses predefined templates to generate reports in Microsoft Office formats (Excel workbooks or Word documents).</span></span> <span data-ttu-id="9b235-633">在生成所需报表时，将根据配置的数据流使用所需数据填充模板。</span><span class="sxs-lookup"><span data-stu-id="9b235-633">While the required report is being generated, a template is filled in with required data according to the configured dataflow.</span></span> <span data-ttu-id="9b235-634">因此，您必须首先为自定义报表设计模板。</span><span class="sxs-lookup"><span data-stu-id="9b235-634">Therefore, you must first design a template for your custom report.</span></span> <span data-ttu-id="9b235-635">此模板必须设计为 Excel 工作簿，其结构代表自定义报表的布局。</span><span class="sxs-lookup"><span data-stu-id="9b235-635">This template must be designed as an Excel workbook, the structure of which represents the layout of a custom report.</span></span> <span data-ttu-id="9b235-636">您必须为计划填充所需数据的每个 Excel 项命名。</span><span class="sxs-lookup"><span data-stu-id="9b235-636">You must name every Excel item that you plan to fill in with required data.</span></span>

1. <span data-ttu-id="9b235-637">下载 [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) 文件，并将其保存到本地计算机。</span><span class="sxs-lookup"><span data-stu-id="9b235-637">Download the [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="9b235-638">在 Excel 中打开文件，查看工作簿的结构。</span><span class="sxs-lookup"><span data-stu-id="9b235-638">Open the file in Excel, and review the structure of the workbook.</span></span>

<span data-ttu-id="9b235-639">如下图所示，下载的模板已设计为打印指定的调查表，这些调查表显示调查表的问题以及相应的答案。</span><span class="sxs-lookup"><span data-stu-id="9b235-639">As the following illustration shows, the downloaded template has been designed to print specified questionnaires that present a questionnaire's questions together with appropriate answers.</span></span>

![可打印指定调查表的 Excel 模板](./media/er-quick-start1-template-layout.png)

<span data-ttu-id="9b235-641">Excel 名称已添加到此模板中以填充调查表详细信息。</span><span class="sxs-lookup"><span data-stu-id="9b235-641">Excel names have been added to this template to fill in the questionnaire details.</span></span> <span data-ttu-id="9b235-642">您可以使用名称管理器来查看 Excel 名称。</span><span class="sxs-lookup"><span data-stu-id="9b235-642">You can use Name Manager to review the Excel names.</span></span>

![使用名称管理器查看提供的 Excel 模板中的 Excel 名称](./media/er-quick-start1-template-names.png)

<span data-ttu-id="9b235-644">报表标签已添加为英语的固定文本。</span><span class="sxs-lookup"><span data-stu-id="9b235-644">Report labels have been added as fixed text in the English language.</span></span> <span data-ttu-id="9b235-645">您可以使用 ER 格式[标签](#AddMmLabels)将报表标签替换为将使用语言相关文本填充标签的新的 Excel 名称，就像在配置的模型映射中使用语言相关表达式一样。</span><span class="sxs-lookup"><span data-stu-id="9b235-645">You can replace the report labels with new Excel names that fill in the labels with language-dependent text by using the ER format [labels](#AddMmLabels), as you did for language-dependent expressions in the configured model mapping.</span></span> <span data-ttu-id="9b235-646">在这种情况下，必须以可编辑的 ER 格式添加 ER 标签。</span><span class="sxs-lookup"><span data-stu-id="9b235-646">In this case, ER labels must be added in the editable ER format.</span></span>

<span data-ttu-id="9b235-647">如下图所示，已指定自定义报表标题来使 Excel 能够分页。</span><span class="sxs-lookup"><span data-stu-id="9b235-647">As the following illustration shows, the custom report header has been specified to enable Excel to do paging.</span></span>

![提供的 Excel 模板中的自定义报表标题](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a><span data-ttu-id="9b235-649">设计格式</span><span class="sxs-lookup"><span data-stu-id="9b235-649">Design a format</span></span>

<span data-ttu-id="9b235-650">作为电子报告功能顾问角色的用户，您必须创建一个新的 ER 配置，其中包含[格式](general-electronic-reporting.md#FormatComponentOutbound)组件。</span><span class="sxs-lookup"><span data-stu-id="9b235-650">As a user in the Electronic Reporting Functional Consultant role, you must create a new ER configuration that contains a [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="9b235-651">您必须配置格式组件来指定运行时如何使用所需数据填充报表模板。</span><span class="sxs-lookup"><span data-stu-id="9b235-651">You must configure the format component to specify how a report template will be filled in with required data at runtime.</span></span>

<span data-ttu-id="9b235-652">通过完成[导入设计的格式配置](#FormatImport)一节的步骤，可以从提供的 XML 文件导入所需的格式。</span><span class="sxs-lookup"><span data-stu-id="9b235-652">By completing the steps in the [Import a designed format configuration](#FormatImport) section, you can import the required format from the provided XML file.</span></span> <span data-ttu-id="9b235-653">或者，您可以完成[创建新格式配置](#FormatCreate)一节的步骤来从头开始设计此格式。</span><span class="sxs-lookup"><span data-stu-id="9b235-653">Alternatively, you can complete the steps in the [Create a new format configuration](#FormatCreate) section to design this format from scratch.</span></span>

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a><span data-ttu-id="9b235-654">导入设计的格式配置</span><span class="sxs-lookup"><span data-stu-id="9b235-654">Import a designed format configuration</span></span>

1. <span data-ttu-id="9b235-655">下载 [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) 文件，并将其保存到本地计算机。</span><span class="sxs-lookup"><span data-stu-id="9b235-655">Download the [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="9b235-656">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="9b235-656">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="9b235-657">在 **电子报告** 工作区中，选择 **报告配置**。</span><span class="sxs-lookup"><span data-stu-id="9b235-657">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="9b235-658">在操作窗格上，选择 **交换** \> **从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="9b235-658">On the Action pane, Select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="9b235-659">选择 **浏览**，然后找到并选择 **Questionnaires format.version.1.1.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="9b235-659">Select **Browse**, and then find and select the **Questionnaires format.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="9b235-660">选择 **确定** 导入配置。</span><span class="sxs-lookup"><span data-stu-id="9b235-660">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="9b235-661">要继续，跳过下一个过程[创建新格式配置](#FormatCreate)。</span><span class="sxs-lookup"><span data-stu-id="9b235-661">To continue, skip the next procedure, [Create a new format configuration](#FormatCreate).</span></span>

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a><span data-ttu-id="9b235-662">创建新的格式配置</span><span class="sxs-lookup"><span data-stu-id="9b235-662">Create a new format configuration</span></span>
 
1. <span data-ttu-id="9b235-663">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="9b235-663">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9b235-664">在 **配置** 页上的配置树中，选择 **调查表模型**。</span><span class="sxs-lookup"><span data-stu-id="9b235-664">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="9b235-665">选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="9b235-665">Select **Create configuration**.</span></span>
4. <span data-ttu-id="9b235-666">在下拉对话框中，执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="9b235-666">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="9b235-667">在 **新建** 字段中，选择 **基于数据模型调查表的格式**。</span><span class="sxs-lookup"><span data-stu-id="9b235-667">In the **New** field, select **Format based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="9b235-668">在 **名称** 字段中输入 **调查表报表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-668">In the **Name** field, enter **Questionnaire report**.</span></span>
    3. <span data-ttu-id="9b235-669">在 **数据模型版本** 字段中，选择 **1**。</span><span class="sxs-lookup"><span data-stu-id="9b235-669">In the **Data model version** field, select **1**.</span></span>

        > [!NOTE]
        > - <span data-ttu-id="9b235-670">如果您选择基础数据模型的特定版本，此数据模型的相应版本的结构将以创建的格式以 **模型** 数据源的结构向您呈现。</span><span class="sxs-lookup"><span data-stu-id="9b235-670">If you select a specific version of the base data model, the structure of the corresponding version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span>
        > - <span data-ttu-id="9b235-671">您可以将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="9b235-671">You can leave this field blank.</span></span> <span data-ttu-id="9b235-672">在这种情况下，数据模型 **草稿** 版本的结构将以创建的格式以 **模型** 数据源的结构向您呈现。</span><span class="sxs-lookup"><span data-stu-id="9b235-672">In that case, the structure of the **Draft** version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span> <span data-ttu-id="9b235-673">然后，您可以调整模型，并立即以您的格式查看这些调整。</span><span class="sxs-lookup"><span data-stu-id="9b235-673">You can then adjust your model and immediately see those adjustments in your format.</span></span> <span data-ttu-id="9b235-674">当您同时配置数据模型、模型映射和格式时，此方法可以提高 ER 解决方案设计的效率。</span><span class="sxs-lookup"><span data-stu-id="9b235-674">This approach might improve the efficiency of ER solution design when you configure your data model, model mapping, and format simultaneously.</span></span>
        > - <span data-ttu-id="9b235-675">如果选择基础数据模型的特定版本，以后在开始编辑格式时，可以切换为使用 **草稿** 版本。</span><span class="sxs-lookup"><span data-stu-id="9b235-675">If you select a specific version of the base data model, you can switch to using the **Draft** version later, when you start to edit a format.</span></span>

    4. <span data-ttu-id="9b235-676">在 **数据模型定义** 字段中，选择 **根** 定义。</span><span class="sxs-lookup"><span data-stu-id="9b235-676">In the **Data model definition** field, select the **Root** definition.</span></span>

5. <span data-ttu-id="9b235-677">选择 **创建配置** 以创建配置。</span><span class="sxs-lookup"><span data-stu-id="9b235-677">Select **Create configuration** to create the configuration.</span></span>

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a><span data-ttu-id="9b235-678">导入报表模板</span><span class="sxs-lookup"><span data-stu-id="9b235-678">Import a report template</span></span>

1. <span data-ttu-id="9b235-679">在 **配置** 页上的配置树中，选择 **调查表报表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-679">On the **Configurations** page, in the configuration tree, select **Questionnaire report**.</span></span>
2. <span data-ttu-id="9b235-680">选择 **设计器** 开始配置自定义格式。</span><span class="sxs-lookup"><span data-stu-id="9b235-680">Select **Designer** to start to configure a custom format.</span></span>
3. <span data-ttu-id="9b235-681">在 **格式设计器** 页的操作窗格上，选择 **导入** \> **从 Excel 导入**。</span><span class="sxs-lookup"><span data-stu-id="9b235-681">On the **Format designer** page, on the Action Pane, select **Import** \> **Import from Excel**.</span></span>
4. <span data-ttu-id="9b235-682">在对话框中，执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="9b235-682">In the dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="9b235-683">选择 **添加模板**。</span><span class="sxs-lookup"><span data-stu-id="9b235-683">Select **Add template**.</span></span>
    2. <span data-ttu-id="9b235-684">找到并选择本地保存的 **Questionnaires report template.xslx** 文件，然后选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="9b235-684">Find and select the locally saved **Questionnaires report template.xslx** file, and then select **Open**.</span></span>
    3. <span data-ttu-id="9b235-685">选择 **确定** 导入模板。</span><span class="sxs-lookup"><span data-stu-id="9b235-685">Select **OK** to import the template.</span></span>

    ![导入报表模板](./media/er-quick-start1-template-import.png)

<span data-ttu-id="9b235-687">**Excel\\文件** 格式元素将作为根元素自动添加到可编辑格式中。</span><span class="sxs-lookup"><span data-stu-id="9b235-687">The **Excel\\File** format element is automatically added to the editable format as a root element.</span></span> <span data-ttu-id="9b235-688">此外，将为导入模板的每个确认的 Excel 名称自动添加 **Excel\\范围** 格式元素或 **Excel\\单元格** 格式元素。</span><span class="sxs-lookup"><span data-stu-id="9b235-688">Additionally, either the **Excel\\Range** format element or the **Excel\\Cell** format element is automatically added for every recognized Excel name of the imported template.</span></span> <span data-ttu-id="9b235-689">具有嵌套 **字符串** 元素的 **Excel\\标题** 格式会自动添加，以反映导入模板的标题设置。</span><span class="sxs-lookup"><span data-stu-id="9b235-689">The **Excel\\Header** format that has the nested **String** element is automatically added to reflect the header settings of the imported template.</span></span>

![包括在 ER 操作设计器中自动添加的元素的格式结构](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a><span data-ttu-id="9b235-691">配置格式</span><span class="sxs-lookup"><span data-stu-id="9b235-691">Configure a format</span></span>

1. <span data-ttu-id="9b235-692">在 **格式设计器** 页面的格式树中，选择 **Excel** 根元素。</span><span class="sxs-lookup"><span data-stu-id="9b235-692">On the **Format designer** page, in the format tree, select the **Excel** root element.</span></span>
2. <span data-ttu-id="9b235-693">在页面右侧的 **格式** 选项卡上的 **名称** 字段中，输入 <a name="AddFormatRootElement"></a>**报表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-693">On the **Format** tab on the right side of the page, in the **Name** field, enter <a name="AddFormatRootElement"></a>**Report**.</span></span>
3. <span data-ttu-id="9b235-694">在 **语言首选项** 字段中，选择 **用户首选项** 以用户的首选语言运行报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-694">In the **Language preference** field, select **User preference** to run the report in the user's preferred language.</span></span>
4. <span data-ttu-id="9b235-695">在 **区域性首选项** 字段中，选择 **用户首选项** 以用户的首选区域性运行报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-695">In the **Culture preference** field, select **User preference** to run the report in the user's preferred culture.</span></span>

    <span data-ttu-id="9b235-696">有关如何为 ER 流程指定语言和区域性上下文的信息，请参阅[设计多语言报表](er-design-multilingual-reports.md)。</span><span class="sxs-lookup"><span data-stu-id="9b235-696">For information about how to specify the language and culture contexts for an ER process, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

    ![在 ER 操作设计器中为设计的报表配置语言和区域性设置](./media/er-quick-start1-template-format-structure1.png)

5. <span data-ttu-id="9b235-698">在格式树中，展开根节点，然后选择 **结果组**。</span><span class="sxs-lookup"><span data-stu-id="9b235-698">In the format tree, expand the root node, and then select **ResultsGroup**.</span></span>
6. <span data-ttu-id="9b235-699">在 **格式** 选项卡中，在 **复制方向** 字段中，选择 **不复制**，因为您不希望单个调查表具有多个结果组。</span><span class="sxs-lookup"><span data-stu-id="9b235-699">On the **Format** tab, in the **Replication direction** field, select **No replication**, because you don't expect to have multiple result groups for a single questionnaire.</span></span>

    ![在 ER 操作设计器中定义范围格式元素的复制方向](./media/er-quick-start1-template-format-structure2.png)

7. <span data-ttu-id="9b235-701">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9b235-701">Select **Save**.</span></span>

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a><span data-ttu-id="9b235-702">定义报表标题的数据绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-702">Define the data binding for a report title</span></span>

<span data-ttu-id="9b235-703">您必须为用于填充生成报表的标题的格式元素指定数据绑定。</span><span class="sxs-lookup"><span data-stu-id="9b235-703">You must specify a data binding for a format element that is used to fill in the title of a generated report.</span></span>

1. <span data-ttu-id="9b235-704">在 **格式设计器** 页上右侧的 **映射** 选项卡上，选择 **报表\\报表标题** 元素。</span><span class="sxs-lookup"><span data-stu-id="9b235-704">On the **Format designer** page, on the **Mapping** tab on the right, select the **Report\\ReportTitle** element.</span></span>
2. <span data-ttu-id="9b235-705">选择 **编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="9b235-705">Select **Edit formula**.</span></span>
3. <span data-ttu-id="9b235-706">在公式编辑器中，选择 **翻译**。</span><span class="sxs-lookup"><span data-stu-id="9b235-706">In the formula editor, select **Translate**.</span></span>
4. <span data-ttu-id="9b235-707">在 **文本翻译** 对话框中，执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="9b235-707">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="9b235-708">在 **标签 ID** 字段中，输入 **ReportTitle**。</span><span class="sxs-lookup"><span data-stu-id="9b235-708">In the **Label ID** field, enter **ReportTitle**.</span></span>
    2. <span data-ttu-id="9b235-709">在 **语言为默认语言的文本** 字段中，输入 **调查表报表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-709">In the **Text in default language** field, enter **Questionnaires report**.</span></span>
    3. <span data-ttu-id="9b235-710">选择 **翻译**，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9b235-710">Select **Translate**, and then select **Save**.</span></span>
    4. <span data-ttu-id="9b235-711">选择 **翻译** 关闭 **文本翻译** 对话框。</span><span class="sxs-lookup"><span data-stu-id="9b235-711">Select **Translate** to close the **Text translation** dialog box.</span></span>

5. <span data-ttu-id="9b235-712">关闭公式编辑器。</span><span class="sxs-lookup"><span data-stu-id="9b235-712">Close the formula editor.</span></span>

    ![配置绑定以填充生成报表的标题](./media/er-quick-start1-add-report-title-label.png)

<span data-ttu-id="9b235-714">您可以使用此方法让当前模板的所有其他标签成为语言相关标签。</span><span class="sxs-lookup"><span data-stu-id="9b235-714">You can use this technique to make all other labels of the current template language-dependent.</span></span> <span data-ttu-id="9b235-715">有关如何将单个 ER 配置的已添加标签翻译为所有支持语言的信息，请参阅[设计多语言报表](er-design-multilingual-reports.md)。</span><span class="sxs-lookup"><span data-stu-id="9b235-715">For information about how the added labels of a single ER configuration can be translated into all supported languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a><span data-ttu-id="9b235-716">查看模型数据源</span><span class="sxs-lookup"><span data-stu-id="9b235-716">Review model data source</span></span>

1. <span data-ttu-id="9b235-717">在 **格式设计器** 页的 **映射** 选项卡上，选择表示此 ER 格式的基础数据模型的 <a name="ModelDSName"></a>**模型** 数据源。</span><span class="sxs-lookup"><span data-stu-id="9b235-717">On the **Format designer** page, on the **Mapping** tab, select the <a name="ModelDSName"></a>**model** data source that represents the base data model of this ER format.</span></span>
2. <span data-ttu-id="9b235-718">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="9b235-718">Select **Edit**.</span></span>
3. <span data-ttu-id="9b235-719">查看 **数据源属性** 对话框中的信息。</span><span class="sxs-lookup"><span data-stu-id="9b235-719">Review the information in the **Data source properties** dialog box.</span></span> <span data-ttu-id="9b235-720">此数据源表示位于 **调查表模型** ER 配置中的 **调查表** 数据模型组件的版本 1。</span><span class="sxs-lookup"><span data-stu-id="9b235-720">This data source represents version 1 of the **Questionnaires** data model component that resides in the **Questionnaires model** ER configuration.</span></span>

![ER 操作设计器中模型数据源的属性](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a><span data-ttu-id="9b235-722">将格式元素与数据源字段绑定</span><span class="sxs-lookup"><span data-stu-id="9b235-722">Bind format elements to data source fields</span></span>

<span data-ttu-id="9b235-723">若要指定在运行时如何填充模板，必须将与相应的 Excel 名称相关联的每个格式元素与此格式的数据源的单个字段绑定。</span><span class="sxs-lookup"><span data-stu-id="9b235-723">To specify how a template is filled in at runtime, you must bind every format element that is associated with an appropriate Excel name to a single field of this format's data source.</span></span>

1. <span data-ttu-id="9b235-724">在 **格式设计器** 页面的格式树中，选择 **报表\\公司名称** 格式元素。</span><span class="sxs-lookup"><span data-stu-id="9b235-724">On the **Format designer** page, in the format tree, select the **Report\\CompanyName** format element.</span></span>
2. <span data-ttu-id="9b235-725">在 **映射** 选项卡上，选择 **字符串** 类型的 **model.CompanyName** 数据源字段。</span><span class="sxs-lookup"><span data-stu-id="9b235-725">On the **Mapping** tab, select the **model.CompanyName** data source field of the **String** type.</span></span>
3. <span data-ttu-id="9b235-726">选择 **绑定** 在模板中输入公司名称。</span><span class="sxs-lookup"><span data-stu-id="9b235-726">Select **Bind** to enter a company name in a template.</span></span>
4. <span data-ttu-id="9b235-727">在格式树中，选择 **报表\\调查表** 元素。</span><span class="sxs-lookup"><span data-stu-id="9b235-727">In the format tree, select the **Report\\Questionnaire** element.</span></span>
5. <span data-ttu-id="9b235-728">在 **映射** 选项卡上，选择 **记录列表** 类型的 **model.Questionnaire** 数据源字段。</span><span class="sxs-lookup"><span data-stu-id="9b235-728">On the **Mapping** tab, select the **model.Questionnaire** data source field of the **Record list** type.</span></span>
6. <span data-ttu-id="9b235-729">选择 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="9b235-729">Select **Bind**.</span></span>
7. <span data-ttu-id="9b235-730">选择 **显示详细资料** 查看格式元素的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="9b235-730">Select **Show details** to see more details for format elements.</span></span>

    <span data-ttu-id="9b235-731">**调查表** 范围格式元素已配置为垂直复制。</span><span class="sxs-lookup"><span data-stu-id="9b235-731">The **Questionnaire** range format element is configured as vertically replicated.</span></span> <span data-ttu-id="9b235-732">将其绑定到 **记录列表** 类型的数据源时，将对绑定数据源的每条记录重复 Excel 模板的相应的 **调查表** 范围。</span><span class="sxs-lookup"><span data-stu-id="9b235-732">When it's bound to a data source of the **Record list** type, the appropriate **Questionnaire** range of the Excel template is repeated for every record of the bound data source.</span></span>
 
    ![将调查表范围格式元素绑定到 ER 操作设计器中相应的记录列表数据源](./media/er-quick-start1-bindings1.png)

    <span data-ttu-id="9b235-734">由于 Excel 模板的 **调查表** 范围是在第 5 到 14 行之间定义的，因此每个报告的调查表都将重复这些行。</span><span class="sxs-lookup"><span data-stu-id="9b235-734">Because the **Questionnaire** range of the Excel template is defined between rows 5 through 14, these rows are repeated for every reported questionnaire.</span></span>

    ![生成报表中将为记录列表数据源的每条记录重复的 Excel 模板中的行](./media/er-quick-start1-template-questionnaire-range.png)

8. <span data-ttu-id="9b235-736">为其余格式元素配置类似的绑定，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="9b235-736">Configure similar bindings for the remaining format elements, as described in the following table.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9b235-737">在此表中，“数据源路径”列中的信息假定[相对路径](relative-path-data-bindings-er-models-format.md) ER 功能已打开。</span><span class="sxs-lookup"><span data-stu-id="9b235-737">In this table, the information in the "Data source path" column assumes that the [relative path](relative-path-data-bindings-er-models-format.md) ER feature is turned on.</span></span>

    | <span data-ttu-id="9b235-738">格式元素路径</span><span class="sxs-lookup"><span data-stu-id="9b235-738">Format element path</span></span>                                      | <span data-ttu-id="9b235-739">数据源路径</span><span class="sxs-lookup"><span data-stu-id="9b235-739">Data source path</span></span> |
    |----------------------------------------------------------|------------------|
    | <span data-ttu-id="9b235-740">Excel\\报告标题</span><span class="sxs-lookup"><span data-stu-id="9b235-740">Excel\\ReportTitle</span></span>                                       | <span data-ttu-id="9b235-741">**\@"GER\_LABEL:ReportTitle"**</span><span class="sxs-lookup"><span data-stu-id="9b235-741">**\@"GER\_LABEL:ReportTitle"**</span></span> |
    | <span data-ttu-id="9b235-742">Excel\\公司名称</span><span class="sxs-lookup"><span data-stu-id="9b235-742">Excel\\CompanyName</span></span>                                       | <span data-ttu-id="9b235-743">**model.CompanyName**</span><span class="sxs-lookup"><span data-stu-id="9b235-743">**model.CompanyName**</span></span> |
    | <span data-ttu-id="9b235-744">Excel\\调查表</span><span class="sxs-lookup"><span data-stu-id="9b235-744">Excel\\Questionnaire</span></span>                                     | <span data-ttu-id="9b235-745">**model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="9b235-745">**model.Questionnaire**</span></span> |
    | <span data-ttu-id="9b235-746">Excel\\调查表\\活动</span><span class="sxs-lookup"><span data-stu-id="9b235-746">Excel\\Questionnaire\\Active</span></span>                             | <span data-ttu-id="9b235-747">**\@.Active**，其中 **\@** 是 **model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="9b235-747">**\@.Active**, where **\@** is **model.Questionnaire**</span></span> |
    | <span data-ttu-id="9b235-748">Excel\\调查表\\代码</span><span class="sxs-lookup"><span data-stu-id="9b235-748">Excel\\Questionnaire\\Code</span></span>                               | <span data-ttu-id="9b235-749">**\@.Code**</span><span class="sxs-lookup"><span data-stu-id="9b235-749">**\@.Code**</span></span> |
    | <span data-ttu-id="9b235-750">Excel\\调查表\\说明</span><span class="sxs-lookup"><span data-stu-id="9b235-750">Excel\\Questionnaire\\Description</span></span>                        | <span data-ttu-id="9b235-751">**\@.Description**</span><span class="sxs-lookup"><span data-stu-id="9b235-751">**\@.Description**</span></span> |
    | <span data-ttu-id="9b235-752">Excel\\调查表\\调查表类型</span><span class="sxs-lookup"><span data-stu-id="9b235-752">Excel\\Questionnaire\\QuestionnaireType</span></span>                  | <span data-ttu-id="9b235-753">**\@.QuestionnaireType**</span><span class="sxs-lookup"><span data-stu-id="9b235-753">**\@.QuestionnaireType**</span></span> |
    | <span data-ttu-id="9b235-754">Excel\\调查表\\问题顺序</span><span class="sxs-lookup"><span data-stu-id="9b235-754">Excel\\Questionnaire\\QuestionOrder</span></span>                      | <span data-ttu-id="9b235-755">**\@.QuestionOrder**</span><span class="sxs-lookup"><span data-stu-id="9b235-755">**\@.QuestionOrder**</span></span> |
    | <span data-ttu-id="9b235-756">Excel\\调查表\\结果组\\代码\_</span><span class="sxs-lookup"><span data-stu-id="9b235-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span></span>               | <span data-ttu-id="9b235-757">**\@.ResultsGroup.Code**</span><span class="sxs-lookup"><span data-stu-id="9b235-757">**\@.ResultsGroup.Code**</span></span> |
    | <span data-ttu-id="9b235-758">Excel\\调查表\\结果组\\说明\_</span><span class="sxs-lookup"><span data-stu-id="9b235-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span></span>        | <span data-ttu-id="9b235-759">**\@.ResultsGroup.Description**</span><span class="sxs-lookup"><span data-stu-id="9b235-759">**\@.ResultsGroup.Description**</span></span> |
    | <span data-ttu-id="9b235-760">Excel\\调查表\\结果组\\最高分数</span><span class="sxs-lookup"><span data-stu-id="9b235-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>    | <span data-ttu-id="9b235-761">**\@.ResultsGroup.MaxNumberOfPoint**</span><span class="sxs-lookup"><span data-stu-id="9b235-761">**\@.ResultsGroup.MaxNumberOfPoint**</span></span> |
    | <span data-ttu-id="9b235-762">Excel\\调查表\\问题</span><span class="sxs-lookup"><span data-stu-id="9b235-762">Excel\\Questionnaire\\Question</span></span>                           | <span data-ttu-id="9b235-763">**\@.Question**</span><span class="sxs-lookup"><span data-stu-id="9b235-763">**\@.Question**</span></span> |
    | <span data-ttu-id="9b235-764">Excel\\调查表\\问题\\集合序列号</span><span class="sxs-lookup"><span data-stu-id="9b235-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span></span> | <span data-ttu-id="9b235-765">**\@.CollectionSequenceNumber**，其中 **\@** 是 **model.Questionnaire.Question**</span><span class="sxs-lookup"><span data-stu-id="9b235-765">**\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question**</span></span> |
    | <span data-ttu-id="9b235-766">Excel\\调查表\\问题\\ID</span><span class="sxs-lookup"><span data-stu-id="9b235-766">Excel\\Questionnaire\\Question\\Id</span></span>                       | <span data-ttu-id="9b235-767">**\@.Id**</span><span class="sxs-lookup"><span data-stu-id="9b235-767">**\@.Id**</span></span> |
    | <span data-ttu-id="9b235-768">Excel\\调查表\\问题\\必须完成</span><span class="sxs-lookup"><span data-stu-id="9b235-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span></span>          | <span data-ttu-id="9b235-769">**\@.MustBeCompleted**</span><span class="sxs-lookup"><span data-stu-id="9b235-769">**\@.MustBeCompleted**</span></span> |
    | <span data-ttu-id="9b235-770">Excel\\调查表\\问题\\主要问题</span><span class="sxs-lookup"><span data-stu-id="9b235-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span></span>          | <span data-ttu-id="9b235-771">**\@.PrimaryQuestion**</span><span class="sxs-lookup"><span data-stu-id="9b235-771">**\@.PrimaryQuestion**</span></span> |
    | <span data-ttu-id="9b235-772">Excel\\调查表\\问题\\序列号</span><span class="sxs-lookup"><span data-stu-id="9b235-772">Excel\\Questionnaire\\Question\\SequenceNumber</span></span>           | <span data-ttu-id="9b235-773">**\@.SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="9b235-773">**\@.SequenceNumber**</span></span> |
    | <span data-ttu-id="9b235-774">Excel\\调查表\\问题\\文本</span><span class="sxs-lookup"><span data-stu-id="9b235-774">Excel\\Questionnaire\\Question\\Text</span></span>                     | <span data-ttu-id="9b235-775">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="9b235-775">**\@.Text**</span></span> |
    | <span data-ttu-id="9b235-776">Excel\\调查表\\问题\\答案</span><span class="sxs-lookup"><span data-stu-id="9b235-776">Excel\\Questionnaire\\Question\\Answer</span></span>                   | <span data-ttu-id="9b235-777">**\@.Answer**</span><span class="sxs-lookup"><span data-stu-id="9b235-777">**\@.Answer**</span></span> |
    | <span data-ttu-id="9b235-778">Excel\\调查表\\问题\\答案\\正确答案</span><span class="sxs-lookup"><span data-stu-id="9b235-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>    | <span data-ttu-id="9b235-779">**\@.CorrectAnswer**，其中 **\@** 是 **model.Questionnaire.Answer**</span><span class="sxs-lookup"><span data-stu-id="9b235-779">**\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer**</span></span> |
    | <span data-ttu-id="9b235-780">Excel\\调查表\\问题\\答案\\分数</span><span class="sxs-lookup"><span data-stu-id="9b235-780">Excel\\Questionnaire\\Question\\Answer\\Points</span></span>           | <span data-ttu-id="9b235-781">**\@.Points**</span><span class="sxs-lookup"><span data-stu-id="9b235-781">**\@.Points**</span></span> |
    | <span data-ttu-id="9b235-782">Excel\\调查表\\问题\\答案\\文本</span><span class="sxs-lookup"><span data-stu-id="9b235-782">Excel\\Questionnaire\\Question\\Answer\\Text</span></span>             | <span data-ttu-id="9b235-783">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="9b235-783">**\@.Text**</span></span> |

9. <span data-ttu-id="9b235-784">当您完成时，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9b235-784">When you've finished, select **Save**.</span></span>

<span data-ttu-id="9b235-785">下图显示了 **模式设计器** 页面上配置的数据绑定的最终状态。</span><span class="sxs-lookup"><span data-stu-id="9b235-785">The following illustration shows the final state of the configured data bindings on the **Format designer** page.</span></span>

![ER 操作设计器中配置的数据绑定](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> <span data-ttu-id="9b235-787">指定数据源和绑定的整个集合表示已配置格式的格式映射组件。</span><span class="sxs-lookup"><span data-stu-id="9b235-787">The whole collection of specified data sources and bindings represents a format mapping component of the configured format.</span></span> <span data-ttu-id="9b235-788">当您运行配置的格式以生成报表时，将调用此格式映射。</span><span class="sxs-lookup"><span data-stu-id="9b235-788">This format mapping is called when you run the configured format for report generation.</span></span>

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a><span data-ttu-id="9b235-789">从 ER 运行设计的格式</span><span class="sxs-lookup"><span data-stu-id="9b235-789">Run a designed format from ER</span></span>

<span data-ttu-id="9b235-790">现在，您可以从 **配置** 页面运行设计的格式来进行测试。</span><span class="sxs-lookup"><span data-stu-id="9b235-790">You can now run a designed format for testing purposes from the **Configurations** page.</span></span>

1. <span data-ttu-id="9b235-791">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="9b235-791">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9b235-792">在 **配置** 页的配置树中，展开 **调查表模型**，然后选择 **调查表报表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-792">On the **Configuration** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="9b235-793">为状态为 **草稿** 的格式版本选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="9b235-793">Select **Designer** for the format version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="9b235-794">在 **格式设计器** 页上，选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="9b235-794">On the **Format designer** page, select **Run**.</span></span>
5. <span data-ttu-id="9b235-795">在 **ER 参数** 对话框的 **要包括的记录** 快速选项卡上，配置筛选选项，以仅包括 **SBCCrsExam** 调查表。</span><span class="sxs-lookup"><span data-stu-id="9b235-795">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
6. <span data-ttu-id="9b235-796">选择 **确定** 确认筛选选项。</span><span class="sxs-lookup"><span data-stu-id="9b235-796">Select **OK** to confirm the filtering option.</span></span>
7. <span data-ttu-id="9b235-797">选择 **确定** 运行报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-797">Select **OK** to run the report.</span></span>
8. <span data-ttu-id="9b235-798">查看生成的报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-798">Review the generated report.</span></span>

<span data-ttu-id="9b235-799">[默认](electronic-reporting-destinations.md#default-behavior)情况下，生成的报表以 Excel 文件的形式提供，您可以进行下载。</span><span class="sxs-lookup"><span data-stu-id="9b235-799">By [default](electronic-reporting-destinations.md#default-behavior), a generated report is delivered as an Excel file that you can download.</span></span> <span data-ttu-id="9b235-800">下图以 Excel 格式显示了生成报表的两个页面。</span><span class="sxs-lookup"><span data-stu-id="9b235-800">The following illustrations show two pages of the generated report in Excel format.</span></span>

![Excel 格式的生成报表的示例，第 1 页](./media/er-quick-start1-report1a.png)

![Excel 格式的生成报表的示例，第 2 页](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a><span data-ttu-id="9b235-803">调整设计的格式</span><span class="sxs-lookup"><span data-stu-id="9b235-803">Tune a designed format</span></span>

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a><span data-ttu-id="9b235-804">修改格式以更改生成文档的名称</span><span class="sxs-lookup"><span data-stu-id="9b235-804">Modify a format to change the name of a generated document</span></span>

<span data-ttu-id="9b235-805">默认情况下，使用当前用户的别名来命名生成的文档。</span><span class="sxs-lookup"><span data-stu-id="9b235-805">By default, a generated document is named by using the alias of the current user.</span></span> <span data-ttu-id="9b235-806">通过修改格式，您可以更改此行为，以根据您的自定义逻辑来命名生成的文档。</span><span class="sxs-lookup"><span data-stu-id="9b235-806">By modifying the format, you can change this behavior so that a generated document is named based on your custom logic.</span></span> <span data-ttu-id="9b235-807">例如，生成文档的名称可以基于当前会话的日期和时间以及报表的标题。</span><span class="sxs-lookup"><span data-stu-id="9b235-807">For example, the name of a generated document can be based on the current session date and time, and on the report's title.</span></span>

1. <span data-ttu-id="9b235-808">在 **格式设计器** 页中，选择 **报表** 根项。</span><span class="sxs-lookup"><span data-stu-id="9b235-808">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="9b235-809">在 **映射** 选项卡上，选择 **编辑文件名**。</span><span class="sxs-lookup"><span data-stu-id="9b235-809">On the **Mapping** tab, select **Edit file name**.</span></span>
3. <span data-ttu-id="9b235-810">在 **公式** 字段中，输入 **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**。</span><span class="sxs-lookup"><span data-stu-id="9b235-810">In the **Formula** field, enter **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span></span>
4. <span data-ttu-id="9b235-811">选择 **保存**，然后关闭公式编辑器。</span><span class="sxs-lookup"><span data-stu-id="9b235-811">Select **Save**, and close the formula editor.</span></span>
5. <span data-ttu-id="9b235-812">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9b235-812">Select **Save**.</span></span>

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a><span data-ttu-id="9b235-813">修改格式以更改问题的顺序</span><span class="sxs-lookup"><span data-stu-id="9b235-813">Modify a format to change the order of questions</span></span>

<span data-ttu-id="9b235-814">问题在生成的报表中未正确排序。</span><span class="sxs-lookup"><span data-stu-id="9b235-814">The questions aren't correctly ordered in a generated report.</span></span> <span data-ttu-id="9b235-815">您可以通过修改格式来更改顺序。</span><span class="sxs-lookup"><span data-stu-id="9b235-815">You can change the order by modifying the format.</span></span>

1. <span data-ttu-id="9b235-816">在 **格式设计器** 页中，选择 **报表** 根项。</span><span class="sxs-lookup"><span data-stu-id="9b235-816">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="9b235-817">在 **映射** 选项卡上的格式树中，展开 **报表\\调查表\\问题**。</span><span class="sxs-lookup"><span data-stu-id="9b235-817">On the **Mapping** tab, in the format tree, expand **Report\\Questionnaire\\Question**.</span></span>

    ![ER 操作设计器中范围类型的问题格式元素](./media/er-quick-start1-bindings3.png)

3. <span data-ttu-id="9b235-819">在 **映射** 选项卡上，选择 **model.Questionnaire**。</span><span class="sxs-lookup"><span data-stu-id="9b235-819">On the **Mapping** tab, select **model.Questionnaire**.</span></span>
4. <span data-ttu-id="9b235-820">选择 **添加** \> **函数\\计算字段**，然后在 **名称** 字段中输入 **OrderedQuestions**。</span><span class="sxs-lookup"><span data-stu-id="9b235-820">Select **Add** \> **Functions\\Calculated field**, and then, in the **Name** field, enter **OrderedQuestions**.</span></span>
5. <span data-ttu-id="9b235-821">选择 **编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="9b235-821">Select **Edit formula**.</span></span>
6. <span data-ttu-id="9b235-822">在公式编辑器的 **公式** 字段中，输入 **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)**，以按序列顺序编号对当前调查表的问题列表进行排序。</span><span class="sxs-lookup"><span data-stu-id="9b235-822">In the formula editor, in the **Formula** field, enter **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** to order the list of questions of the current questionnaire by the sequence order number.</span></span>
7. <span data-ttu-id="9b235-823">选择 **保存**，然后关闭公式编辑器。</span><span class="sxs-lookup"><span data-stu-id="9b235-823">Select **Save**, and close the formula editor.</span></span>
8. <span data-ttu-id="9b235-824">选择 **确定** 完成新计算字段的输入。</span><span class="sxs-lookup"><span data-stu-id="9b235-824">Select **OK** to complete the entry of a new calculated field.</span></span>
9. <span data-ttu-id="9b235-825">在 **映射** 选项卡上，选择 **model.Questionnaire.OrderedQuestions**。</span><span class="sxs-lookup"><span data-stu-id="9b235-825">On the **Mapping** tab, select **model.Questionnaire.OrderedQuestions**.</span></span>
10. <span data-ttu-id="9b235-826">在格式树中，选择 **Excel\\调查表\\问题**。</span><span class="sxs-lookup"><span data-stu-id="9b235-826">In the format tree, select **Excel\\Questionnaire\\Question**.</span></span>
11. <span data-ttu-id="9b235-827">选择 **绑定**，然后确认在嵌套元素的所有绑定中，当前的 **model.Questionnaire.Questions** 路径已被新的 **model.Questionnaire.OrderedQuestions** 路径替换。</span><span class="sxs-lookup"><span data-stu-id="9b235-827">Select **Bind**, and then confirm that the current **model.Questionnaire.Questions** path is replaced by the new **model.Questionnaire.OrderedQuestions** path in all bindings of nested elements.</span></span>
12. <span data-ttu-id="9b235-828">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9b235-828">Select **Save**.</span></span>

![将问题格式元素绑定到 ER 操作设计器中配置的 OrderedQuestions 数据源](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a><span data-ttu-id="9b235-830">从 ER 运行修改的格式</span><span class="sxs-lookup"><span data-stu-id="9b235-830">Run a modified format from ER</span></span>

<span data-ttu-id="9b235-831">现在，您可以从 ER 框架运行修改的格式来进行测试。</span><span class="sxs-lookup"><span data-stu-id="9b235-831">You can now run a modified format for testing purposes from the ER framework.</span></span>

1. <span data-ttu-id="9b235-832">在 **格式设计器** 页上，选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="9b235-832">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="9b235-833">在 **ER 参数** 对话框的 **要包括的记录** 快速选项卡上，配置筛选选项，以仅包括 **SBCCrsExam** 调查表。</span><span class="sxs-lookup"><span data-stu-id="9b235-833">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
3. <span data-ttu-id="9b235-834">选择 **确定** 确认筛选选项。</span><span class="sxs-lookup"><span data-stu-id="9b235-834">Select **OK** to confirm the filtering option.</span></span>
4. <span data-ttu-id="9b235-835">选择 **确定** 运行报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-835">Select **OK** to run the report.</span></span>
5. <span data-ttu-id="9b235-836">查看生成的报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-836">Review the generated report.</span></span>

<span data-ttu-id="9b235-837">下图显示了 Excel 格式的生成报表，其中问题已正确排序。</span><span class="sxs-lookup"><span data-stu-id="9b235-837">The following illustration shows a generated report in Excel format where the questions are correctly ordered.</span></span>

![问题已正确排序的 Excel 格式的生成报表](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a><span data-ttu-id="9b235-839">完成格式设计</span><span class="sxs-lookup"><span data-stu-id="9b235-839">Complete the format design</span></span>

1. <span data-ttu-id="9b235-840">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="9b235-840">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9b235-841">在 **配置** 页的配置树中，展开 **调查表模型**，然后选择 **调查表报表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-841">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="9b235-842">在 **版本** 快速选项卡上，选择状态为 **草稿** 的配置版本。</span><span class="sxs-lookup"><span data-stu-id="9b235-842">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="9b235-843">选择 **更改状态** \> **完成**。</span><span class="sxs-lookup"><span data-stu-id="9b235-843">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="9b235-844">此配置的版本 1.1 的状态将从 **草稿** 更改为 **已完成**。</span><span class="sxs-lookup"><span data-stu-id="9b235-844">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="9b235-845">版本 1.1 不能再更改。</span><span class="sxs-lookup"><span data-stu-id="9b235-845">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="9b235-846">此版本包含配置的格式，可用于打印自定义报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-846">This version contains the configured format and can be used to print your custom report.</span></span> <span data-ttu-id="9b235-847">此配置的版本 1.2 将创建，状态为 **草稿**。</span><span class="sxs-lookup"><span data-stu-id="9b235-847">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="9b235-848">您可以编辑此版本来调整 **调查表** 报表的格式。</span><span class="sxs-lookup"><span data-stu-id="9b235-848">You can edit this version to adjust the format of your **Questionnaire** report.</span></span>

![“配置”页上可编辑 ER 配置的版本](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> <span data-ttu-id="9b235-850">配置的格式是您的 **调查表** 报表的设计，不包含与 Finance 特定伪像的关系。</span><span class="sxs-lookup"><span data-stu-id="9b235-850">The configured format is your design of the **Questionnaire** report and contains no relations to the Finance-specific artefacts.</span></span>

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a><span data-ttu-id="9b235-851">开发应用程序伪像以调用设计的报表</span><span class="sxs-lookup"><span data-stu-id="9b235-851">Develop application artefacts to call the designed report</span></span>

<span data-ttu-id="9b235-852">作为系统管理员角色的用户，您必须开发新逻辑，以可以从应用程序用户界面 (UI) 调用配置的 ER 格式来生成自定义报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-852">As a user in the System Administrator role, you must develop new logic so that the configured ER format can be called from the application user interface (UI) to generate your custom report.</span></span> <span data-ttu-id="9b235-853">当前，ER 不提供任何配置此类逻辑的功能。</span><span class="sxs-lookup"><span data-stu-id="9b235-853">Currently, ER doesn't offer any capability for configuring this type of logic.</span></span> <span data-ttu-id="9b235-854">因此，需要一些工程工作。</span><span class="sxs-lookup"><span data-stu-id="9b235-854">Therefore, some engineering work is required.</span></span> 

<span data-ttu-id="9b235-855">要开发新逻辑，必须部署支持连续生成的拓扑。</span><span class="sxs-lookup"><span data-stu-id="9b235-855">To develop the new logic, you must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="9b235-856">有关详细信息，请参阅[部署支持连续生成和测试自动化的拓扑](../perf-test/continuous-build-test-automation.md)。</span><span class="sxs-lookup"><span data-stu-id="9b235-856">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span> <span data-ttu-id="9b235-857">还必须可以访问此拓扑的开发环境。</span><span class="sxs-lookup"><span data-stu-id="9b235-857">You must also have access to the development environment for this topology.</span></span> <span data-ttu-id="9b235-858">有关可用 ER API 的详细信息，请参阅 [ER 框架 API](er-apis-app73.md)。</span><span class="sxs-lookup"><span data-stu-id="9b235-858">For more information about the available ER API, see [ER framework API](er-apis-app73.md).</span></span>

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a><span data-ttu-id="9b235-859">修改源代码</span><span class="sxs-lookup"><span data-stu-id="9b235-859">Modify source code</span></span>

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a><span data-ttu-id="9b235-860">添加数据合同类</span><span class="sxs-lookup"><span data-stu-id="9b235-860">Add a data contract class</span></span>

<span data-ttu-id="9b235-861">将新 **QuestionnairesErReportContract** 类添加到您的 Microsoft Visual Studio 项目中，并编写指定应用于运行配置的 ER 格式的数据合同的代码。</span><span class="sxs-lookup"><span data-stu-id="9b235-861">Add the new **QuestionnairesErReportContract** class to your Microsoft Visual Studio project, and write code that specifies the data contract that should be used to run the configured ER format.</span></span>

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a><span data-ttu-id="9b235-862">添加 UI 构建器类</span><span class="sxs-lookup"><span data-stu-id="9b235-862">Add a UI builder class</span></span>

<span data-ttu-id="9b235-863">将新 **QuestionnairesErReportUIBuilder** 类添加到您的 Visual Studio 项目中，并编写代码以生成将用于查找必须运行的 ER 格式的格式映射 ID 的运行时对话框。</span><span class="sxs-lookup"><span data-stu-id="9b235-863">Add the new **QuestionnairesErReportUIBuilder** class to your Visual Studio project, and write code to generate a runtime dialog box that will be used to look up the format mapping ID of the ER format that must be run.</span></span> <span data-ttu-id="9b235-864">提供的代码仅查找包含引用 **[调查表](#DataModeName)** 数据模型的 **数据模型** 类型的数据源的 ER 格式，查找使用 **[根](#RootDefinitionName)** 定义。</span><span class="sxs-lookup"><span data-stu-id="9b235-864">The provided code looks up only ER formats that contain a data source of the **Data model** type that refers to the **[Questionnaires](#DataModeName)** data model by using the **[Root](#RootDefinitionName)** definition.</span></span>

> [!NOTE]
> <span data-ttu-id="9b235-865">或者，您可以使用 ER 集成点来筛选 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="9b235-865">Alternatively, you can use ER integration points to filter ER formats.</span></span> <span data-ttu-id="9b235-866">有关详细信息，请参阅[用于显示格式映射查找的 API](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup)。</span><span class="sxs-lookup"><span data-stu-id="9b235-866">For more information, see [API to show a format mapping lookup](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span></span>

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a><span data-ttu-id="9b235-867">添加数据提供程序类</span><span class="sxs-lookup"><span data-stu-id="9b235-867">Add a data provider class</span></span>

<span data-ttu-id="9b235-868">将新 **QuestionnairesErReportDP** 类添加到您的 Visual Studio 项目中，并编写引入应用于运行配置的 ER 格式的数据提供程序的代码。</span><span class="sxs-lookup"><span data-stu-id="9b235-868">Add the new **QuestionnairesErReportDP** class to your Visual Studio project, and write code that introduces the data provider that should used to run the configured ER format.</span></span> <span data-ttu-id="9b235-869">提供的代码仅包含此数据提供程序的数据合同。</span><span class="sxs-lookup"><span data-stu-id="9b235-869">The provided code includes only the data contract for this data provider.</span></span>

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a><span data-ttu-id="9b235-870">添加标签文件</span><span class="sxs-lookup"><span data-stu-id="9b235-870">Add a labels file</span></span>

<span data-ttu-id="9b235-871">将新的 **QuestionnairesErReportLabels\_en-US** 标签文件添加到您的 Visual Studio 项目中，并为新的 UI 资源指定以下标签：</span><span class="sxs-lookup"><span data-stu-id="9b235-871">Add the new **QuestionnairesErReportLabels\_en-US** labels file to your Visual Studio project, and specify the following labels for new UI resources:</span></span>

- <span data-ttu-id="9b235-872">包含以下使用美国英语 (en-US) 显示的文本的新菜单项的 **\@QuestionnairesReport** 标签：**Questionnaires report (powered by ER)**</span><span class="sxs-lookup"><span data-stu-id="9b235-872">The **\@QuestionnairesReport** label for a new menu item that contains the following text in US English (en-US): **Questionnaires report (powered by ER)**</span></span>
- <span data-ttu-id="9b235-873">计划将选定的 ER 格式作为批处理作业执行时批处理作业标题的 **\@QuestionnairesReportBatchJobDescription** 标签</span><span class="sxs-lookup"><span data-stu-id="9b235-873">The **\@QuestionnairesReportBatchJobDescription** label for a batch job title if a selected ER format is scheduled for execution as a batch job</span></span>

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a><span data-ttu-id="9b235-874">添加报表服务类</span><span class="sxs-lookup"><span data-stu-id="9b235-874">Add a report service class</span></span>

<span data-ttu-id="9b235-875">将新 **QuestionnairesErReportService** 类添加到您的 Visual Studio 项目中，并编写调用 ER 格式、使用格式映射 ID 加以标识并提供数据合同作为参数的代码。</span><span class="sxs-lookup"><span data-stu-id="9b235-875">Add the new **QuestionnairesErReportService** class to your Visual Studio project, and write code that calls an ER format, identifies it by a format mapping ID, and provides a data contract as a parameter.</span></span>

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

<span data-ttu-id="9b235-876">如果必须使用运行应用程序数据的 ER 格式，则必须在格式映射中配置 **数据模型** 类型的数据源。</span><span class="sxs-lookup"><span data-stu-id="9b235-876">When you must use an ER format that runs application data, you must configure a data source of the **Data model** type in the format mapping.</span></span> <span data-ttu-id="9b235-877">此数据源通过使用单个根定义来引用指定数据模型的特定部分。</span><span class="sxs-lookup"><span data-stu-id="9b235-877">This data source refers to a specific part of the specified data model by using a single root definition.</span></span> <span data-ttu-id="9b235-878">运行 ER 格式时，它将调用此数据源以访问为给定模型和根定义配置的相应 ER 模型映射。</span><span class="sxs-lookup"><span data-stu-id="9b235-878">When the ER format is run, it calls this data source to access the appropriate ER model mapping that is configured for a given model and root definition.</span></span>

<span data-ttu-id="9b235-879">您可以使用此类型的 ER 模型映射，将您可能在源代码中准备并存储为数据合同一部分的所有信息传递到正在运行的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="9b235-879">All the information that you might prepare in the source code and store as part of the data contract can be passed to the running ER format by using an ER model mapping of this type.</span></span> <span data-ttu-id="9b235-880">在 ER 模型映射中，必须配置引用 **[QuestionnairesErReportContract](#DataContractClass)** 类的 **对象** 类型的数据源。</span><span class="sxs-lookup"><span data-stu-id="9b235-880">In the ER model mapping, you must configure a data source of the **Object** type that refers to the **[QuestionnairesErReportContract](#DataContractClass)** class.</span></span> <span data-ttu-id="9b235-881">要标识模型映射，必须指定一个调用此模型映射的数据源。</span><span class="sxs-lookup"><span data-stu-id="9b235-881">To identify a model mapping, you must specify a data source that calls this model mapping.</span></span> <span data-ttu-id="9b235-882">在提供的代码中，此数据源由具有 **[模型](#ModelDSName)** 值的 **ERModelDataSourceName** 常量指定。</span><span class="sxs-lookup"><span data-stu-id="9b235-882">In the provided code, this data source specified by the **ERModelDataSourceName** constant that has the **[model](#ModelDSName)** value.</span></span> <span data-ttu-id="9b235-883">若要标识哪个数据源用于在模型映射中公开数据合同，必须指定一个数据源名称。</span><span class="sxs-lookup"><span data-stu-id="9b235-883">To identify which data source is used to expose the data contract in the model mapping, you must specify a data source name.</span></span> <span data-ttu-id="9b235-884">在提供的代码中，此名称由具有 <a name="DataContractDSName"></a>**RunTimeParameters** 值的 **ParametersDataSourceName** 常量指定。</span><span class="sxs-lookup"><span data-stu-id="9b235-884">In the provided code, this name is specified by the **ParametersDataSourceName** constant that has <a name="DataContractDSName"></a>**RunTimeParameters** value.</span></span>

> [!NOTE]
> <span data-ttu-id="9b235-885">在新环境中，您可能必须刷新 ER 元数据，以可以在 ER 模型映射设计器中使用这种类型的类。</span><span class="sxs-lookup"><span data-stu-id="9b235-885">In a new environment, you might have to refresh the ER metadata so that this type of class is available in the ER model mapping designer.</span></span> <span data-ttu-id="9b235-886">有关详细信息，请参阅[配置 ER 框架](electronic-reporting-er-configure-parameters.md#frequently-asked-questions)。</span><span class="sxs-lookup"><span data-stu-id="9b235-886">For more information, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span></span>

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a><span data-ttu-id="9b235-887">添加报表控制器类</span><span class="sxs-lookup"><span data-stu-id="9b235-887">Add a report controller class</span></span>

<span data-ttu-id="9b235-888">将新 **QuestionnairesErReportController** 类添加到您的 Visual Studio 项目中，并根据您的需要，在基于提供的 **QuestionnairesErReportUIBuilder** 类的逻辑构建的对话框中，编写以同步模式或批处理模式运行 ER 格式的代码。</span><span class="sxs-lookup"><span data-stu-id="9b235-888">Add the new **QuestionnairesErReportController** class to your Visual Studio project, and write code that runs an ER format in either synchronous mode or batch mode, as you prefer, in the dialog box that is built based on the logic of the provided **QuestionnairesErReportUIBuilder** class.</span></span>

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a><span data-ttu-id="9b235-889">添加菜单项</span><span class="sxs-lookup"><span data-stu-id="9b235-889">Add a menu item</span></span>

<span data-ttu-id="9b235-890">将新的 **QuestionnairesErReport** 菜单项添加到您的 Visual Studio 项目中。</span><span class="sxs-lookup"><span data-stu-id="9b235-890">Add the new **QuestionnairesErReport** menu item to your Visual Studio project.</span></span> <span data-ttu-id="9b235-891">在 **对象** 属性中，此菜单项引用 **QuestionnairesErReportController** 类，用于指定选择和运行 ER 格式的用户权限。</span><span class="sxs-lookup"><span data-stu-id="9b235-891">In the **Object** property, this menu item refers to the **QuestionnairesErReportController** class, and it's used to specify a user permission to select and run an ER format.</span></span> <span data-ttu-id="9b235-892">在 **标签** 属性中，此菜单项引用您之前创建的 **\@QuestionnairesReport** 标签，以在应用程序 UI 中呈现正确的文本。</span><span class="sxs-lookup"><span data-stu-id="9b235-892">In the **Label** property, this menu item refers to the **\@QuestionnairesReport** label that you created earlier, so that correct text is presented in the application UI.</span></span>

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a><span data-ttu-id="9b235-893">向菜单添加菜单项</span><span class="sxs-lookup"><span data-stu-id="9b235-893">Add a menu item to a menu</span></span>

<span data-ttu-id="9b235-894">将现有的 **KM** 菜单添加到您的 Visual Studio 项目中。</span><span class="sxs-lookup"><span data-stu-id="9b235-894">Add the existing **KM** menu to your Visual Studio project.</span></span> <span data-ttu-id="9b235-895">您必须在此菜单中添加 **输出** 类型的新 **QuestionnairesErReport** 项目。</span><span class="sxs-lookup"><span data-stu-id="9b235-895">You must add a new **QuestionnairesErReport** item of the **Output** type to this menu.</span></span> <span data-ttu-id="9b235-896">此项目必须引用上一节中介绍的 **QuestionnairesErReport** 菜单项。</span><span class="sxs-lookup"><span data-stu-id="9b235-896">This item must refer to the **QuestionnairesErReport** menu item that is described in the previous section.</span></span>

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a><span data-ttu-id="9b235-897">构建 Visual Studio 项目</span><span class="sxs-lookup"><span data-stu-id="9b235-897">Build a Visual Studio project</span></span>

<span data-ttu-id="9b235-898">构建项目以使新菜单项可供用户使用。</span><span class="sxs-lookup"><span data-stu-id="9b235-898">Build your project to make a new menu item available to users.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a><span data-ttu-id="9b235-899">从应用程序运行格式</span><span class="sxs-lookup"><span data-stu-id="9b235-899">Run a format from the application</span></span>

1. <span data-ttu-id="9b235-900">转到 **调查表** \> **设计** \> **调查表报表(由 ER 提供支持)**。</span><span class="sxs-lookup"><span data-stu-id="9b235-900">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>

    ![在“调查表”模块中选择“调查表报表(由 ER 提供支持)”菜单项来运行配置的 ER 格式](./media/er-quick-start1-application-menu-modified.png)

2. <span data-ttu-id="9b235-902">在对话框中，在 **格式映射** 字段中，选择 **调查表报表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-902">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="9b235-903">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="9b235-903">Select **OK**.</span></span>
4. <span data-ttu-id="9b235-904">在 **电子报表参数** 对话框的 **要包括的记录** 快速选项卡上，配置筛选选项，以仅包括 **SBCCrsExam** 调查表。</span><span class="sxs-lookup"><span data-stu-id="9b235-904">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="9b235-905">选择 **确定** 确认筛选选项。</span><span class="sxs-lookup"><span data-stu-id="9b235-905">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="9b235-906">选择 **确定** 运行报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-906">Select **OK** to run the report.</span></span>

    ![在“电子报表”对话框中指定选择条件](./media/er-quick-start1-report-run-dialog-page.png)

7. <span data-ttu-id="9b235-908">查看生成的报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-908">Review the generated report.</span></span>

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a><span data-ttu-id="9b235-909">调整设计的 ER 解决方案</span><span class="sxs-lookup"><span data-stu-id="9b235-909">Tune a designed ER solution</span></span>

<span data-ttu-id="9b235-910">您可以修改配置的 ER 解决方案，让它使用您开发的数据提供程序类访问正在运行的 ER 格式的详细信息，并在生成的报表中输入此 ER 格式的名称。</span><span class="sxs-lookup"><span data-stu-id="9b235-910">You can modify the configured ER solution so that it uses the data provider class that you developed to access details of the running ER format, and so that it enters the name of this ER format in a generated report.</span></span>

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a><span data-ttu-id="9b235-911">修改模型映射</span><span class="sxs-lookup"><span data-stu-id="9b235-911">Modify a model mapping</span></span>

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a><span data-ttu-id="9b235-912">添加数据源以访问数据合同对象</span><span class="sxs-lookup"><span data-stu-id="9b235-912">Add data sources to access a data contract object</span></span>

1. <span data-ttu-id="9b235-913">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="9b235-913">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9b235-914">在 **配置** 页的配置树中，展开 **调查表模型**，然后选择 **调查表映射**。</span><span class="sxs-lookup"><span data-stu-id="9b235-914">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="9b235-915">选择 **设计器** 打开 **模型到数据源映射** 页面。</span><span class="sxs-lookup"><span data-stu-id="9b235-915">Select **Designer** to open the **Model to datasource mapping** page.</span></span>
4. <span data-ttu-id="9b235-916">选择 **设计器** 在模型映射设计器中打开选定的映射。</span><span class="sxs-lookup"><span data-stu-id="9b235-916">Select **Designer** to open the selected mapping in the model mapping designer.</span></span>
5. <span data-ttu-id="9b235-917">在 **模型映射设计器** 页的 **数据源类型** 窗格中，选择 **Dynamics 365 for Operations\\对象**。</span><span class="sxs-lookup"><span data-stu-id="9b235-917">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Object**.</span></span>
6. <span data-ttu-id="9b235-918">在 **数据源** 窗格中，选择 **添加根**。</span><span class="sxs-lookup"><span data-stu-id="9b235-918">In the **Data sources** pane, select **Add root**.</span></span>
7. <span data-ttu-id="9b235-919">在对话框中，在 **名称** 字段中，输入 **[RunTimeParameters](#DataContractDSName)**，如 **QuestionnairesErReportService** 类的源代码中所定义的。</span><span class="sxs-lookup"><span data-stu-id="9b235-919">In the dialog box, in the **Name** field, enter **[RunTimeParameters](#DataContractDSName)**, as defined in the source code of the **QuestionnairesErReportService** class.</span></span>
8. <span data-ttu-id="9b235-920">在 **类** 字段中，输入 **[QuestionnairesErReportContract](#DataContractClass)**，之前已编码。</span><span class="sxs-lookup"><span data-stu-id="9b235-920">In the **Class** field, enter **[QuestionnairesErReportContract](#DataContractClass)**, which was coded earlier.</span></span>
9. <span data-ttu-id="9b235-921">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="9b235-921">Select **OK**.</span></span>
10. <span data-ttu-id="9b235-922">展开 **RunTimeParameters**。</span><span class="sxs-lookup"><span data-stu-id="9b235-922">Expand **RunTimeParameters**.</span></span>

<span data-ttu-id="9b235-923">添加的数据源提供有关正在运行的 ER 格式映射的记录 ID 的信息。</span><span class="sxs-lookup"><span data-stu-id="9b235-923">The added data source provides information about the record ID of the running ER format mapping.</span></span>

![ER 模型映射设计器中添加的数据源](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a><span data-ttu-id="9b235-925">添加数据源以访问 ER 格式映射记录</span><span class="sxs-lookup"><span data-stu-id="9b235-925">Add a data source to access ER format mapping records</span></span>

<span data-ttu-id="9b235-926">通过添加数据源以访问 ER 格式映射记录，继续编辑所选的模型映射。</span><span class="sxs-lookup"><span data-stu-id="9b235-926">Continue to edit the selected model mapping by adding a data source to access ER format mapping records.</span></span>

1. <span data-ttu-id="9b235-927">在 **模型映射设计器** 页的 **数据源类型** 窗格中，选择 **Dynamics 365 for Operations\\表记录**。</span><span class="sxs-lookup"><span data-stu-id="9b235-927">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="9b235-928">在 **数据源** 窗格中，选择 **添加根**。</span><span class="sxs-lookup"><span data-stu-id="9b235-928">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="9b235-929">在对话框的 **名称** 字段中，输入 **ER1**。</span><span class="sxs-lookup"><span data-stu-id="9b235-929">In the dialog box, in the **Name** field, enter **ER1**.</span></span>
4. <span data-ttu-id="9b235-930">在 **表** 字段中，输入 **ERFormatMappingTable**。</span><span class="sxs-lookup"><span data-stu-id="9b235-930">In the **Table** field, enter **ERFormatMappingTable**.</span></span>
5. <span data-ttu-id="9b235-931">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="9b235-931">Select **OK**.</span></span>

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a><span data-ttu-id="9b235-932">添加数据源以访问正在运行的 ER 格式的格式映射记录</span><span class="sxs-lookup"><span data-stu-id="9b235-932">Add a data source to access a format mapping record of a running ER format</span></span>

<span data-ttu-id="9b235-933">通过添加数据源以访问正在运行的 ER 格式的格式映射记录，继续编辑所选的模型映射。</span><span class="sxs-lookup"><span data-stu-id="9b235-933">Continue to edit the selected model mapping by adding a data source to access the format mapping record of the running ER format.</span></span>

1. <span data-ttu-id="9b235-934">在 **模型映射设计器** 页的 **数据源类型** 窗格中，选择 **函数\\计算字段**。</span><span class="sxs-lookup"><span data-stu-id="9b235-934">On the **Model mapping designer** page, in the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
2. <span data-ttu-id="9b235-935">在 **数据源** 窗格中，选择 **添加根**。</span><span class="sxs-lookup"><span data-stu-id="9b235-935">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="9b235-936">在对话框的 **名称** 字段中，输入 **ER2**。</span><span class="sxs-lookup"><span data-stu-id="9b235-936">In the dialog box, in the **Name** field, enter **ER2**.</span></span>
4. <span data-ttu-id="9b235-937">选择 **编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="9b235-937">Select **Edit formula**.</span></span>
5. <span data-ttu-id="9b235-938">在公式编辑器中的 **公式** 字段中，输入 **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**。</span><span class="sxs-lookup"><span data-stu-id="9b235-938">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span></span>
6. <span data-ttu-id="9b235-939">选择 **保存**，然后关闭公式编辑器。</span><span class="sxs-lookup"><span data-stu-id="9b235-939">Select **Save**, and close the formula editor.</span></span>
7. <span data-ttu-id="9b235-940">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="9b235-940">Select **OK**.</span></span>

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a><span data-ttu-id="9b235-941">在数据模型中输入正在运行的 ER 格式的名称</span><span class="sxs-lookup"><span data-stu-id="9b235-941">Enter the name of the running ER format in the data model</span></span>

<span data-ttu-id="9b235-942">继续编辑所选的模型映射，以在数据模型中输入正在运行的 ER 格式的名称。</span><span class="sxs-lookup"><span data-stu-id="9b235-942">Continue to edit the selected model mapping so that the name of the running ER format is entered in the data model.</span></span>

1. <span data-ttu-id="9b235-943">在 **模型映射设计器** 页的 **数据模型** 窗格中，展开 **ExecutionContext**，然后选择 **ExecutionContext\\FormatName**。</span><span class="sxs-lookup"><span data-stu-id="9b235-943">On the **Model mapping designer** page, in the **Data model** pane, expand **ExecutionContext**, and then select **ExecutionContext\\FormatName**.</span></span>
2. <span data-ttu-id="9b235-944">在 **数据模型** 窗格中，选择 **编辑** 为所选数据模型的字段配置数据绑定。</span><span class="sxs-lookup"><span data-stu-id="9b235-944">In the **Data model** pane, select **Edit** to configure a data binding for the selected data model's field.</span></span>
3. <span data-ttu-id="9b235-945">在公式编辑器中的 **公式** 字段中，输入 **FIRSTORNULL (ER2.'\>Relations'.Format).Name**。</span><span class="sxs-lookup"><span data-stu-id="9b235-945">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span></span>
4. <span data-ttu-id="9b235-946">选择 **保存**，然后关闭公式编辑器。</span><span class="sxs-lookup"><span data-stu-id="9b235-946">Select **Save**, and close the formula editor.</span></span>

<span data-ttu-id="9b235-947">由于您使用了 **FormatName** 字段，配置的模型映射现在公开在执行期间调用此模型映射的 ER 格式的名称。</span><span class="sxs-lookup"><span data-stu-id="9b235-947">Because you used the **FormatName** field, the configured model mapping now exposes the name of an ER format that calls this model mapping during execution.</span></span>

![将数据模型字段绑定到 ER 模型映射设计器中添加的数据源的方法](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a><span data-ttu-id="9b235-949">完成模型映射的设计</span><span class="sxs-lookup"><span data-stu-id="9b235-949">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="9b235-950">在 **模型映射设计器** 页上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9b235-950">On the **Model mapping designer** page, select **Save**.</span></span>
2. <span data-ttu-id="9b235-951">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9b235-951">Close the page.</span></span>
3. <span data-ttu-id="9b235-952">关闭模型映射页。</span><span class="sxs-lookup"><span data-stu-id="9b235-952">Close the model mappings page.</span></span>
4. <span data-ttu-id="9b235-953">在 **配置** 页面的配置树中，确保仍选择 **调查表映射** 配置。</span><span class="sxs-lookup"><span data-stu-id="9b235-953">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire mapping** configuration is still selected.</span></span> <span data-ttu-id="9b235-954">然后，在 **版本** 快速选项卡上，选择状态为 **草稿** 的配置版本。</span><span class="sxs-lookup"><span data-stu-id="9b235-954">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
5. <span data-ttu-id="9b235-955">选择 **更改状态** \> **完成**。</span><span class="sxs-lookup"><span data-stu-id="9b235-955">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="9b235-956">此配置的版本 1.2 的状态将从 **草稿** 更改为 **已完成**。</span><span class="sxs-lookup"><span data-stu-id="9b235-956">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="9b235-957">版本 1.2 不能再更改。</span><span class="sxs-lookup"><span data-stu-id="9b235-957">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="9b235-958">此版本包含已配置的模型映射，可以用作其他 ER 配置的基础。</span><span class="sxs-lookup"><span data-stu-id="9b235-958">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="9b235-959">此配置的版本 1.3 将创建，状态为 **草稿**。</span><span class="sxs-lookup"><span data-stu-id="9b235-959">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="9b235-960">您可以编辑此版本来调整 **调查表** 模型映射。</span><span class="sxs-lookup"><span data-stu-id="9b235-960">You can edit this version to adjust the **Questionnaire** model mapping.</span></span>

### <a name="modify-a-format"></a><a name="ModifyFormat"></a><span data-ttu-id="9b235-961">修改格式</span><span class="sxs-lookup"><span data-stu-id="9b235-961">Modify a format</span></span>

<span data-ttu-id="9b235-962">您可以修改配置的 ER 格式，以使其名称显示在运行 ER 格式时生成的报表的页脚中。</span><span class="sxs-lookup"><span data-stu-id="9b235-962">You can modify the configured ER format so that its name is shown in the footer of a report that is generated when the ER format is run.</span></span>

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a><span data-ttu-id="9b235-963">添加新格式元素</span><span class="sxs-lookup"><span data-stu-id="9b235-963">Add a new format element</span></span>

1. <span data-ttu-id="9b235-964">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="9b235-964">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9b235-965">在 **配置** 页的配置树中，展开 **调查表模型**，然后选择 **调查表报表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-965">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="9b235-966">选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="9b235-966">Select **Designer**.</span></span>
4. <span data-ttu-id="9b235-967">在 **格式设计器** 页中，选择 **报表** 根项。</span><span class="sxs-lookup"><span data-stu-id="9b235-967">On the **Format designer** page, select the **Report** root item.</span></span>
5. <span data-ttu-id="9b235-968">选择 **添加** 为所选的 **报表** 根项添加新的嵌套格式元素。</span><span class="sxs-lookup"><span data-stu-id="9b235-968">Select **Add** to add a new nested format element for the selected **Report** root item.</span></span>
6. <span data-ttu-id="9b235-969">选择 **Excel\\页脚**。</span><span class="sxs-lookup"><span data-stu-id="9b235-969">Select **Excel\\Footer**.</span></span>
7. <span data-ttu-id="9b235-970">在 **名称** 字段中，输入 **页脚**。</span><span class="sxs-lookup"><span data-stu-id="9b235-970">In the **Name** field, enter **Footer**.</span></span>
8. <span data-ttu-id="9b235-971">选择 **报表\页脚**，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="9b235-971">Select **Report\Footer**, and then select **Add**.</span></span>
9. <span data-ttu-id="9b235-972">选择 **文本\\字符串**。</span><span class="sxs-lookup"><span data-stu-id="9b235-972">Select **Text\\String**.</span></span>

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a><span data-ttu-id="9b235-973">绑定添加的格式元素</span><span class="sxs-lookup"><span data-stu-id="9b235-973">Bind the added format element</span></span>

1. <span data-ttu-id="9b235-974">在 **格式设计器** 页面的 **映射** 选项卡上，在格式树中，为活动的 **页脚\\字符串** 元素选择 **编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="9b235-974">On the **Format designer** page, on the **Mapping** tab, in the format tree, for the active **Footer\\String** element, select **Edit formula**.</span></span>
2. <span data-ttu-id="9b235-975">在公式编辑器中的 **公式** 字段中，输入 **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**。</span><span class="sxs-lookup"><span data-stu-id="9b235-975">In the formula editor, in the **Formula** field, enter **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span></span>
3. <span data-ttu-id="9b235-976">选择 **保存**，然后关闭公式编辑器。</span><span class="sxs-lookup"><span data-stu-id="9b235-976">Select **Save**, and close the formula editor.</span></span>
4. <span data-ttu-id="9b235-977">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9b235-977">Select **Save**.</span></span>

<span data-ttu-id="9b235-978">配置的格式现在已经修改，以使用 **页脚\\字符串** 元素将其名称输入到生成报表的页脚中。</span><span class="sxs-lookup"><span data-stu-id="9b235-978">The configured format has now been modified so that its name will be entered in the footer of a generated report by using the **Footer\\String** element.</span></span>

![将页脚格式元素添加到 ER 操作设计器中的配置的格式中](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a><span data-ttu-id="9b235-980">完成格式设计</span><span class="sxs-lookup"><span data-stu-id="9b235-980">Complete the format design</span></span>

1. <span data-ttu-id="9b235-981">关闭 **格式设计器** 页。</span><span class="sxs-lookup"><span data-stu-id="9b235-981">Close the **Format designer** page.</span></span>
2. <span data-ttu-id="9b235-982">在 **配置** 页面的配置树中，确保仍选择 **调查表报表** 配置。</span><span class="sxs-lookup"><span data-stu-id="9b235-982">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire report** configuration is still selected.</span></span> <span data-ttu-id="9b235-983">然后，在 **版本** 快速选项卡上，选择状态为 **草稿** 的配置版本。</span><span class="sxs-lookup"><span data-stu-id="9b235-983">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
3. <span data-ttu-id="9b235-984">选择 **更改状态** \> **完成**。</span><span class="sxs-lookup"><span data-stu-id="9b235-984">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="9b235-985">此配置的版本 1.2 的状态将从 **草稿** 更改为 **已完成**。</span><span class="sxs-lookup"><span data-stu-id="9b235-985">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="9b235-986">版本 1.2 不能再更改。</span><span class="sxs-lookup"><span data-stu-id="9b235-986">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="9b235-987">此版本包含已配置的格式，可以用作其他 ER 配置的基础。</span><span class="sxs-lookup"><span data-stu-id="9b235-987">This version contains the configured format and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="9b235-988">此配置的版本 1.3 将创建，状态为 **草稿**。</span><span class="sxs-lookup"><span data-stu-id="9b235-988">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="9b235-989">您可以编辑此版本来调整 **调查表** 报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-989">You can edit this version to adjust the **Questionnaire** report.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a><span data-ttu-id="9b235-990">从应用程序运行格式</span><span class="sxs-lookup"><span data-stu-id="9b235-990">Run a format from the application</span></span>

1. <span data-ttu-id="9b235-991">转到 **调查表** \> **设计** \> **调查表报表(由 ER 提供支持)**。</span><span class="sxs-lookup"><span data-stu-id="9b235-991">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="9b235-992">在对话框中，在 **格式映射** 字段中，选择 **调查表报表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-992">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="9b235-993">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="9b235-993">Select **OK**.</span></span>
4. <span data-ttu-id="9b235-994">在 **ER 参数** 对话框的 **要包括的记录** 快速选项卡上，配置筛选选项，以仅包括 **SBCCrsExam** 调查表。</span><span class="sxs-lookup"><span data-stu-id="9b235-994">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="9b235-995">选择 **确定** 确认筛选选项。</span><span class="sxs-lookup"><span data-stu-id="9b235-995">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="9b235-996">选择 **确定** 运行报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-996">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="9b235-997">查看生成的 Excel 格式的报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-997">Review the generated report in Excel format.</span></span>

<span data-ttu-id="9b235-998">请注意，生成的报表的页脚包含用于生成报表的 ER 格式的名称。</span><span class="sxs-lookup"><span data-stu-id="9b235-998">Notice that the footer of the generated report contains the name of the ER format that was used to generate it.</span></span>

![以 Excel 格式生成报表](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a><span data-ttu-id="9b235-1000">从 ER 运行格式</span><span class="sxs-lookup"><span data-stu-id="9b235-1000">Run a format from ER</span></span>

1. <span data-ttu-id="9b235-1001">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="9b235-1001">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9b235-1002">在 **配置** 页的配置树中，展开 **调查表模型**，然后选择 **调查表报表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-1002">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="9b235-1003">在操作窗格上，选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="9b235-1003">On the Action Pane, select **Run**.</span></span>
4. <span data-ttu-id="9b235-1004">在 **电子报表参数** 对话框的 **要包括的记录** 快速选项卡上，配置筛选选项，以仅包括 **SBCCrsExam** 调查表。</span><span class="sxs-lookup"><span data-stu-id="9b235-1004">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="9b235-1005">选择 **确定** 确认筛选选项。</span><span class="sxs-lookup"><span data-stu-id="9b235-1005">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="9b235-1006">选择 **确定** 运行报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-1006">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="9b235-1007">查看生成的 Excel 格式的报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-1007">Review the generated report in Excel format.</span></span>

<span data-ttu-id="9b235-1008">请注意，生成的报表的页脚不包含用于生成报表的 ER 格式的名称，因为当数据合同对象被从 ER 运行的 ER 格式调用时，它未被传递到运行的模型映射。</span><span class="sxs-lookup"><span data-stu-id="9b235-1008">Notice that the footer of the generated report doesn't contain the name of ER format that was used to generate it, because the data contract object wasn't passed to the running model mapping when it was called by the ER format that was run from ER.</span></span>

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a><span data-ttu-id="9b235-1009">为屏幕预览配置格式目标</span><span class="sxs-lookup"><span data-stu-id="9b235-1009">Configure a format destination for on-screen preview</span></span>

1. <span data-ttu-id="9b235-1010">转到 **组织管理** \> **电子报告** \> **电子报告目标**。</span><span class="sxs-lookup"><span data-stu-id="9b235-1010">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting destination**.</span></span>
2. <span data-ttu-id="9b235-1011">在 **电子报告目标** 页面上，为已配置的 **调查表报表** ER 格式添加目标记录。</span><span class="sxs-lookup"><span data-stu-id="9b235-1011">On the **Electronic reporting destination** page, add a destination record for the configured **Questionnaire report** ER format.</span></span>
3. <span data-ttu-id="9b235-1012">在 **文件目标** 快速选项卡上，为已作为配置的 **调查表报表** ER 格式的根元素 [添加](#AddFormatRootElement)的 **报表** 格式组件设置 **屏幕**[目标](er-destination-type-screen.md)。</span><span class="sxs-lookup"><span data-stu-id="9b235-1012">On the **File destination** FastTab, set up the **Screen** [destination](er-destination-type-screen.md) for the **Report** format component that has been [added](#AddFormatRootElement) as the root element of the configured **Questionnaire report** ER format.</span></span>
4. <span data-ttu-id="9b235-1013">在 **PDF 转换设置** 快速选项卡上，配置目标以将报表转换为使用 **横向** 页面方向的 [PDF 格式](electronic-reporting-destinations.md#OutputConversionToPDF)。</span><span class="sxs-lookup"><span data-stu-id="9b235-1013">On the **PDF conversion settings** FastTab, configure the destination to convert a report to [PDF format](electronic-reporting-destinations.md#OutputConversionToPDF) that uses the **Landscape** page orientation.</span></span>

![在电子报告目标页面上为 ER 格式配置自定义屏幕目标](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a><span data-ttu-id="9b235-1015">从应用程序运行格式以作为 PDF 文档预览</span><span class="sxs-lookup"><span data-stu-id="9b235-1015">Run a format from the application to preview it as a PDF document</span></span>

1. <span data-ttu-id="9b235-1016">转到 **调查表** \> **设计** \> **调查表报表(由 ER 提供支持)**。</span><span class="sxs-lookup"><span data-stu-id="9b235-1016">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="9b235-1017">在对话框中，在 **格式映射** 字段中，选择 **调查表报表**。</span><span class="sxs-lookup"><span data-stu-id="9b235-1017">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="9b235-1018">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="9b235-1018">Select **OK**.</span></span>
4. <span data-ttu-id="9b235-1019">在 **电子报表参数** 对话框的 **要包括的记录** 快速选项卡上，配置筛选选项，以仅包括 **SBCCrsExam** 调查表。</span><span class="sxs-lookup"><span data-stu-id="9b235-1019">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="9b235-1020">选择 **确定** 确认筛选选项。</span><span class="sxs-lookup"><span data-stu-id="9b235-1020">Select **OK** to confirm the filtering option.</span></span>

    <span data-ttu-id="9b235-1021">在 **目标** 快速选项卡上，注意 **输出** 字段已设置为 **屏幕**。</span><span class="sxs-lookup"><span data-stu-id="9b235-1021">On the **Destinations** FastTab, notice that the **Output** field is set to **Screen**.</span></span> <span data-ttu-id="9b235-1022">如果要更改配置的目标，选择 **更改**。</span><span class="sxs-lookup"><span data-stu-id="9b235-1022">If you want to change the configured destination, select **Change**.</span></span>

    ![您可以在其中更改配置的目标的 ER 报表运行时对话框](./media/er-quick-start1-run-settings.png)

6. <span data-ttu-id="9b235-1024">选择 **确定** 运行报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-1024">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="9b235-1025">查看生成的 PDF 格式的报表。</span><span class="sxs-lookup"><span data-stu-id="9b235-1025">Review the generated report in PDF format.</span></span>

    ![生成的 PDF 格式的报表的屏幕预览](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a><span data-ttu-id="9b235-1027">其他资源</span><span class="sxs-lookup"><span data-stu-id="9b235-1027">Additional resources</span></span>

- [<span data-ttu-id="9b235-1028">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="9b235-1028">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="9b235-1029">电子申报公式语言</span><span class="sxs-lookup"><span data-stu-id="9b235-1029">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="9b235-1030">设计多语言报告</span><span class="sxs-lookup"><span data-stu-id="9b235-1030">Design multilingual reports</span></span>](er-design-multilingual-reports.md)
- [<span data-ttu-id="9b235-1031">电子报告框架 API</span><span class="sxs-lookup"><span data-stu-id="9b235-1031">ER framework API</span></span>](er-apis-app73.md)
- [<span data-ttu-id="9b235-1032">CASE 函数</span><span class="sxs-lookup"><span data-stu-id="9b235-1032">CASE function</span></span>](er-functions-logical-case.md)
- [<span data-ttu-id="9b235-1033">CONCATENATE 函数</span><span class="sxs-lookup"><span data-stu-id="9b235-1033">CONCATENATE function</span></span>](er-functions-text-concatenate.md)
- [<span data-ttu-id="9b235-1034">DATETIMEFORMAT 函数</span><span class="sxs-lookup"><span data-stu-id="9b235-1034">DATETIMEFORMAT function</span></span>](er-functions-datetime-datetimeformat.md)
- [<span data-ttu-id="9b235-1035">FILTER 函数</span><span class="sxs-lookup"><span data-stu-id="9b235-1035">FILTER function</span></span>](er-functions-list-filter.md)
- [<span data-ttu-id="9b235-1036">FIRSTORNULL 函数</span><span class="sxs-lookup"><span data-stu-id="9b235-1036">FIRSTORNULL function</span></span>](er-functions-list-firstornull.md)
- [<span data-ttu-id="9b235-1037">FORMAT 函数</span><span class="sxs-lookup"><span data-stu-id="9b235-1037">FORMAT function</span></span>](er-functions-text-format.md)
- [<span data-ttu-id="9b235-1038">IF 函数</span><span class="sxs-lookup"><span data-stu-id="9b235-1038">IF function</span></span>](er-functions-logical-if.md)
- [<span data-ttu-id="9b235-1039">ORDERBY 函数</span><span class="sxs-lookup"><span data-stu-id="9b235-1039">ORDERBY function</span></span>](er-functions-list-orderby.md)
- [<span data-ttu-id="9b235-1040">SESSIONNOW 函数</span><span class="sxs-lookup"><span data-stu-id="9b235-1040">SESSIONNOW function</span></span>](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
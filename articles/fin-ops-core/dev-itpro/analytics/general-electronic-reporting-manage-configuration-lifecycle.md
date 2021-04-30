---
title: 管理电子申报 (ER) 配置生命周期
description: 本主题介绍如何管理 Dynamics 365 Finance 的电子报告 (ER) 配置的生命周期。
author: NickSelin
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52aba53b5323a9c6c4331cd8de7e932bb9c3547e
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893193"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a><span data-ttu-id="b7287-103">管理电子报告 (ER) 配置生命周期</span><span class="sxs-lookup"><span data-stu-id="b7287-103">Manage the Electronic reporting (ER) configuration lifecycle</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7287-104">本主题介绍如何管理 Dynamics 365 Finance 的电子报告 (ER) 配置的生命周期。</span><span class="sxs-lookup"><span data-stu-id="b7287-104">This topic describes how to manage the lifecycle of Electronic reporting (ER) configurations for Dynamics 365 Finance.</span></span>

## <a name="overview"></a><span data-ttu-id="b7287-105">概览</span><span class="sxs-lookup"><span data-stu-id="b7287-105">Overview</span></span>

<span data-ttu-id="b7287-106">电子申报 (ER) 是一个引擎，可支持法律要求的和国家/地区特定的电子文档。</span><span class="sxs-lookup"><span data-stu-id="b7287-106">Electronic reporting (ER) is an engine that supports statutory required and country-specific electronic documents.</span></span> <span data-ttu-id="b7287-107">一般来说，ER 假设执行一个电子文档的以下任务的能力。</span><span class="sxs-lookup"><span data-stu-id="b7287-107">In general, ER assumes an ability to perform the following tasks for a single electronic document.</span></span> <span data-ttu-id="b7287-108">有关详细信息，请参阅[电子申报 (ER) 概览](general-electronic-reporting.md)。</span><span class="sxs-lookup"><span data-stu-id="b7287-108">For more details, see [Electronic reporting (ER) overview](general-electronic-reporting.md).</span></span>

- <span data-ttu-id="b7287-109">设计电子文件的模板：</span><span class="sxs-lookup"><span data-stu-id="b7287-109">Design a template for an electronic document:</span></span>

    - <span data-ttu-id="b7287-110">标识可在此文档中提供的所需数据源：</span><span class="sxs-lookup"><span data-stu-id="b7287-110">Identify the required sources of data that can be presented in the document:</span></span>

        - <span data-ttu-id="b7287-111">基础数据（如数据表、数据实体和类）。</span><span class="sxs-lookup"><span data-stu-id="b7287-111">Underlying data, such as data tables, data entities, and classes.</span></span>
        - <span data-ttu-id="b7287-112">处理特定的属性（如执行日期和时间，以及时区）。</span><span class="sxs-lookup"><span data-stu-id="b7287-112">Process-specific properties, such as execution date and time, and time zone.</span></span>
        - <span data-ttu-id="b7287-113">用户输入参数（在运行时由最终用户指定）。</span><span class="sxs-lookup"><span data-stu-id="b7287-113">User input parameters, specified by the end user at run time.</span></span>

    - <span data-ttu-id="b7287-114">定义所需文档的元素及其拓扑结构以指定最终文档格式。</span><span class="sxs-lookup"><span data-stu-id="b7287-114">Define the required document elements and their topology to specify a final document format.</span></span>
    - <span data-ttu-id="b7287-115">配置从所选数据源到定义的文档元素的所需数据流（通过绑定到文档格式组件的数据源）并指定流程控制逻辑。</span><span class="sxs-lookup"><span data-stu-id="b7287-115">Configure the desired flow of data from selected data sources to defined document elements (via data source bindings to document format components), and specify process control logic.</span></span>

- <span data-ttu-id="b7287-116">将一个模板变为可用，以便可以在其他实例中使用：</span><span class="sxs-lookup"><span data-stu-id="b7287-116">Make a template available so that it can be used in other instances:</span></span>

    - <span data-ttu-id="b7287-117">将创建的文档模板转换为 ER 配置，并且将当前应用程序实例中的配置导出为可以存储在本地或 Lifecycle Services (LCS) 中的 XML 包。</span><span class="sxs-lookup"><span data-stu-id="b7287-117">Transform a document template that was created into an ER configuration, and export the configuration from the current application instance as an XML package that can be stored either locally or in Lifecycle Services (LCS).</span></span>
    - <span data-ttu-id="b7287-118">将 ER 配置转换为应用程序文档模板。</span><span class="sxs-lookup"><span data-stu-id="b7287-118">Transform an ER configuration into an application document template.</span></span>
    - <span data-ttu-id="b7287-119">将存储在本地或 LCS 中的 XML 包导入到当前实例。</span><span class="sxs-lookup"><span data-stu-id="b7287-119">Import an XML package that is stored either locally or in LCS into the current instance.</span></span>

- <span data-ttu-id="b7287-120">自定义电子文档模板：</span><span class="sxs-lookup"><span data-stu-id="b7287-120">Customize the template of an electronic document:</span></span>

    - <span data-ttu-id="b7287-121">从 LCS 将模板作为 ER 配置导入到当前实例。</span><span class="sxs-lookup"><span data-stu-id="b7287-121">Bring a template from LCS into the current instance as an ER configuration.</span></span>
    - <span data-ttu-id="b7287-122">设计自定义版本的 ER 配置，并保留对其基础版本的引用。</span><span class="sxs-lookup"><span data-stu-id="b7287-122">Design a custom version of an ER configuration, and keep a reference to the base version.</span></span>

- <span data-ttu-id="b7287-123">将模板与特定业务流程集成，以使它在应用程序中可用：</span><span class="sxs-lookup"><span data-stu-id="b7287-123">Integrate a template with a particular business process, so that it's available in the application:</span></span>

    - <span data-ttu-id="b7287-124">通过在流程相关参数中引用该配置来配置设置以便应用程序开始使用 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="b7287-124">Configure settings so that the application starts to use an ER configuration, by referring to that configuration in a process-related parameter.</span></span> <span data-ttu-id="b7287-125">例如，引用特定应付帐款付款方式中的 ER 配置以生成用于处理发票的电子付款消息。</span><span class="sxs-lookup"><span data-stu-id="b7287-125">For example, refer to the ER configuration in a specific Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span>

- <span data-ttu-id="b7287-126">使用特定的业务流程中的模板：</span><span class="sxs-lookup"><span data-stu-id="b7287-126">Use a template in a specific business process:</span></span>

    - <span data-ttu-id="b7287-127">在特定的业务流程中运行 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="b7287-127">Run an ER configuration in a specific business process.</span></span> <span data-ttu-id="b7287-128">例如，要在选择了引用 ER 配置的付款方式时生成用于处理发票的电子付款消息。</span><span class="sxs-lookup"><span data-stu-id="b7287-128">For example, to generate an electronic payment message for processing invoices when a payment method that references the ER configuration is selected.</span></span>

## <a name="concepts"></a><span data-ttu-id="b7287-129">概念</span><span class="sxs-lookup"><span data-stu-id="b7287-129">Concepts</span></span>
<span data-ttu-id="b7287-130">以下角色和相关活动与 ER 配置生命周期相关。</span><span class="sxs-lookup"><span data-stu-id="b7287-130">The following roles and related activities are associated with the ER configuration lifecycle.</span></span>

| <span data-ttu-id="b7287-131">角色</span><span class="sxs-lookup"><span data-stu-id="b7287-131">Role</span></span>                                       | <span data-ttu-id="b7287-132">活动</span><span class="sxs-lookup"><span data-stu-id="b7287-132">Activities</span></span>                                                      | <span data-ttu-id="b7287-133">说明</span><span class="sxs-lookup"><span data-stu-id="b7287-133">Description</span></span> |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| <span data-ttu-id="b7287-134">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="b7287-134">Electronic reporting functional consultant</span></span> | <span data-ttu-id="b7287-135">创建和管理 ER 组件（模型和格式）。</span><span class="sxs-lookup"><span data-stu-id="b7287-135">Create and manage ER components (models and formats).</span></span>           | <span data-ttu-id="b7287-136">设计 ER 域特定数据模型、设计电子文档的所需模板并将它们进行相应绑定的业务人员。</span><span class="sxs-lookup"><span data-stu-id="b7287-136">A business person who designs ER domain–specific data models, designs the required templates for electronic documents, and binds them accordingly.</span></span> |
| <span data-ttu-id="b7287-137">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="b7287-137">Electronic reporting developer</span></span>             | <span data-ttu-id="b7287-138">创建和管理数据模型映射。</span><span class="sxs-lookup"><span data-stu-id="b7287-138">Create and manage data model mappings.</span></span>                          | <span data-ttu-id="b7287-139">选择所需的 Finance 数据源并将它们绑定到 ER 域特定数据模型的专业人员。</span><span class="sxs-lookup"><span data-stu-id="b7287-139">A specialist who selects the required Finance data sources and binds them to ER domain–specific data models.</span></span> |
| <span data-ttu-id="b7287-140">会计主管</span><span class="sxs-lookup"><span data-stu-id="b7287-140">Accounting supervisor</span></span>                      | <span data-ttu-id="b7287-141">配置引用 ER 项目的流程相关设置。</span><span class="sxs-lookup"><span data-stu-id="b7287-141">Configure process-related settings that reference ER artifacts.</span></span> | <span data-ttu-id="b7287-142">例如，允许 ER 配置设置用于特定应付帐款付款方式来生成用于处理发票的电子付款消息的 **会计主管** 角色。</span><span class="sxs-lookup"><span data-stu-id="b7287-142">For example, an **Accounting supervisor** role that allows the settings of an ER configuration to be used in a particular Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span> |
| <span data-ttu-id="b7287-143">应付帐款付款员</span><span class="sxs-lookup"><span data-stu-id="b7287-143">Accounts payable payments clerk</span></span>            | <span data-ttu-id="b7287-144">使用特定业务流程中的 ER 项目。</span><span class="sxs-lookup"><span data-stu-id="b7287-144">Use ER artifacts in a specific business process.</span></span>                | <span data-ttu-id="b7287-145">例如，允许基于为特定付款方式配置的 ER 格式为处理发票生成电子付款消息的 **应付帐款付款员**。</span><span class="sxs-lookup"><span data-stu-id="b7287-145">For example, an **Accounts payable payments clerk** role that allows electronic payment messages to be generated for processing invoices, based on the ER format that is configured for a specific payment method.</span></span> |

## <a name="er-configuration-development-lifecycle"></a><span data-ttu-id="b7287-146">ER 配置开发生命周期</span><span class="sxs-lookup"><span data-stu-id="b7287-146">ER configuration development lifecycle</span></span>
<span data-ttu-id="b7287-147">出于以下与 ER 相关的原因，我们建议您在开发环境中将 ER 配置设计为单独的 Finance and Operations 实例：</span><span class="sxs-lookup"><span data-stu-id="b7287-147">For the following ER-related reasons, we recommend that you design ER configurations in the development environment, as a separate instance of Finance and Operations:</span></span>

- <span data-ttu-id="b7287-148">担当 **电子申报开发人员** 角色或 **电子申报功能顾问** 角色的用户可编辑配置，并运行配置以进行测试。</span><span class="sxs-lookup"><span data-stu-id="b7287-148">Users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can edit configurations and run them for testing purposes.</span></span> <span data-ttu-id="b7287-149">此情况可能会导致调用类和表的方法，可能对业务数据和实例的性能产生负面影响。</span><span class="sxs-lookup"><span data-stu-id="b7287-149">This scenario can cause calls of methods of classes and tables that might harm business data and the performance of the instance.</span></span>
- <span data-ttu-id="b7287-150">在调用作为 ER 配置的 ER 数据源的类和表的方法时，不受入口点和记录的公司内容的限制。</span><span class="sxs-lookup"><span data-stu-id="b7287-150">Calls of methods of classes and tables as ER data sources of ER configurations aren't restricted by entry points and logged company content.</span></span> <span data-ttu-id="b7287-151">因此，担当 **电子申报开发人员** 角色或 **电子申报功能顾问** 角色的用户可访问业务敏感数据。</span><span class="sxs-lookup"><span data-stu-id="b7287-151">Therefore, users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can access business-sensitive data.</span></span>

<span data-ttu-id="b7287-152">在开发环境中设计的 ER 配置可[上传](#data-persistence-consideration)到测试环境以进行配置评估（适当的流程集成、结果的正确性、性能）和质量保证（例如角色驱动的访问权限的正确性和职责划分）。</span><span class="sxs-lookup"><span data-stu-id="b7287-152">ER configurations that are designed in the development environment can be [uploaded](#data-persistence-consideration) to the test environment for the configuration evaluation (proper process integration, correctness of results, and performance) and quality assurance, such as correctness of role-driven access rights and segregation of duties.</span></span> <span data-ttu-id="b7287-153">启用 ER 配置交换的功能可以用于此目的。</span><span class="sxs-lookup"><span data-stu-id="b7287-153">The features that enable ER configuration interchange can be used for this purpose.</span></span> <span data-ttu-id="b7287-154">已审核的 ER 配置可上传到 LCS 以与服务订阅者共享，它们也可[导入](#data-persistence-consideration)到生产环境以供内部使用。</span><span class="sxs-lookup"><span data-stu-id="b7287-154">Proven ER configurations can be uploaded to LCS to share them with service subscribers, or they can be [imported](#data-persistence-consideration) to the production environment for internal use.</span></span>

![ER 配置生命周期](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a><span data-ttu-id="b7287-156"><a name="data-persistence-consideration" />数据持久性注意事项</span><span class="sxs-lookup"><span data-stu-id="b7287-156"><a name="data-persistence-consideration" />Data persistence consideration</span></span>

<span data-ttu-id="b7287-157">您可以将 ER [配置](general-electronic-reporting.md#Configuration)的不同[版本](general-electronic-reporting.md#component-versioning)单独[导入](tasks/er-import-configuration-lifecycle-services.md)到您的 Finance 实例。</span><span class="sxs-lookup"><span data-stu-id="b7287-157">You can individually [import](tasks/er-import-configuration-lifecycle-services.md) different [versions](general-electronic-reporting.md#component-versioning) of an ER [configuration](general-electronic-reporting.md#Configuration) to your Finance instance.</span></span> <span data-ttu-id="b7287-158">导入新版本的 ER 配置时，系统将控制此配置的草稿版本的内容：</span><span class="sxs-lookup"><span data-stu-id="b7287-158">When a new version of an ER configuration is imported, the system controls the content of the draft version of this configuration:</span></span>

   - <span data-ttu-id="b7287-159">当导入的版本低于当前 Finance 实例中此配置的最高版本时，此配置的草稿版本内容将保持不变。</span><span class="sxs-lookup"><span data-stu-id="b7287-159">When the imported version is lower than the highest version of this configuration in the current Finance instance, the content of the draft version of this configuration remains unchanged.</span></span>
   - <span data-ttu-id="b7287-160">当导入的版本高于当前 Finance 实例中此配置的任何其他版本时，导入版本的内容将复制到此配置的草稿版本，以使您可以继续编辑最后完成的版本。</span><span class="sxs-lookup"><span data-stu-id="b7287-160">When the imported version is higher than any other version of this configuration in the current Finance instance, the content of the imported version is copied to the draft version of this configuration to let you continue editing the last completed version.</span></span>

<span data-ttu-id="b7287-161">如果此配置由当前已激活的配置 [提供商](general-electronic-reporting.md#Provider)负责，您可以在 **配置** 页面的 **版本** 快速选项卡上看到此配置的草稿版本（**组织管理** > **电子报告** > **配置**）。</span><span class="sxs-lookup"><span data-stu-id="b7287-161">If this configuration is owned by the configuration [provider](general-electronic-reporting.md#Provider) that is currently activated, the draft version of this configuration is visible to you on the **Versions** FastTab of the **Configurations** page (**Organization administration** > **Electronic reporting** > **Configurations**).</span></span> <span data-ttu-id="b7287-162">您可以选择配置的草稿版本，然后通过使用相关的 ER 设计器[修改](er-quick-start2-customize-report.md#ConfigureDerivedFormat)其内容。</span><span class="sxs-lookup"><span data-stu-id="b7287-162">You can select the draft version of the configuration and [modify](er-quick-start2-customize-report.md#ConfigureDerivedFormat) its content by using the relevant ER designer.</span></span> <span data-ttu-id="b7287-163">在编辑 ER 配置的草稿版本后，其内容不再与当前 Finance 实例中此配置的最高版本的内容相匹配。</span><span class="sxs-lookup"><span data-stu-id="b7287-163">When you have edited the draft version of an ER configuration, its content no longer matches the content of the highest version of this configuration in the current Finance instance.</span></span> <span data-ttu-id="b7287-164">若要防止更改丢失，系统将显示一个错误，即由于此配置的版本高于当前 Finance 实例中此配置的最高版本，因此导入无法继续。</span><span class="sxs-lookup"><span data-stu-id="b7287-164">To prevent the loss of your changes, the system displays an error that the import is unable to continue because the version of this configuration is higher than the highest version of this configuration in the current Finance instance.</span></span> <span data-ttu-id="b7287-165">当发生这种情况时，例如，对于格式配置 **X**，将显示 **格式“X”版本未完成** 错误。</span><span class="sxs-lookup"><span data-stu-id="b7287-165">When this happens, for example with the format configuration **X**, the **Format 'X' version is not completed** error is displayed.</span></span>

<span data-ttu-id="b7287-166">若要撤消在草稿版本中引入的更改，请在 **版本** 快速选项卡上选择 Finance 中 ER 配置的已完成或已共享最高版本，然后选择 **获取此版本** 选项。</span><span class="sxs-lookup"><span data-stu-id="b7287-166">To undo the changes that you introduced in the draft version, select the highest completed or shared version of your ER configuration in Finance on the **Versions** FastTab, and then select the **Get this version** option.</span></span> <span data-ttu-id="b7287-167">所选版本的内容将复制到草稿版本。</span><span class="sxs-lookup"><span data-stu-id="b7287-167">The content of the selected version is copied to the draft version.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b7287-168">其他资源</span><span class="sxs-lookup"><span data-stu-id="b7287-168">Additional resources</span></span>

[<span data-ttu-id="b7287-169">电子报告 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="b7287-169">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

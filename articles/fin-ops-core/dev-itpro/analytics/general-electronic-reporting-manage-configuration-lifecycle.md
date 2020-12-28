---
title: 管理电子申报 (ER) 配置生命周期
description: 本主题介绍如何管理 Microsoft Dynamics 365 Finance 解决方案的电子申报 (ER) 配置的生命周期。
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 1a4741784103817c270c4c7f730753ba59a327d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682615"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a><span data-ttu-id="c52a1-103">管理电子申报 (ER) 配置生命周期</span><span class="sxs-lookup"><span data-stu-id="c52a1-103">Manage the Electronic reporting (ER) configuration lifecycle</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c52a1-104">本主题介绍如何管理 Microsoft Dynamics 365 Finance 解决方案的电子申报 (ER) 配置的生命周期。</span><span class="sxs-lookup"><span data-stu-id="c52a1-104">This topic describes how to manage the lifecycle of Electronic reporting (ER) configurations for Microsoft Dynamics 365 Finance.</span></span>

## <a name="overview"></a><span data-ttu-id="c52a1-105">概览</span><span class="sxs-lookup"><span data-stu-id="c52a1-105">Overview</span></span>

<span data-ttu-id="c52a1-106">电子申报 (ER) 是一个引擎，可支持法律要求的和国家/地区特定的电子文档。</span><span class="sxs-lookup"><span data-stu-id="c52a1-106">Electronic reporting (ER) is an engine that supports statutory required and country-specific electronic documents.</span></span> <span data-ttu-id="c52a1-107">一般来说，ER 假设执行一个电子文档的以下任务的能力。</span><span class="sxs-lookup"><span data-stu-id="c52a1-107">In general, ER assumes an ability to perform the following tasks for a single electronic document.</span></span> <span data-ttu-id="c52a1-108">有关详细信息，请参阅[电子申报 (ER) 概览](general-electronic-reporting.md)。</span><span class="sxs-lookup"><span data-stu-id="c52a1-108">For more details, see [Electronic reporting (ER) overview](general-electronic-reporting.md).</span></span>

- <span data-ttu-id="c52a1-109">设计电子文件的模板：</span><span class="sxs-lookup"><span data-stu-id="c52a1-109">Design a template for an electronic document:</span></span>

    - <span data-ttu-id="c52a1-110">标识可在此文档中提供的所需数据源：</span><span class="sxs-lookup"><span data-stu-id="c52a1-110">Identify the required sources of data that can be presented in the document:</span></span>

        - <span data-ttu-id="c52a1-111">基础数据（如数据表、数据实体和类）。</span><span class="sxs-lookup"><span data-stu-id="c52a1-111">Underlying data, such as data tables, data entities, and classes.</span></span>
        - <span data-ttu-id="c52a1-112">处理特定的属性（如执行日期和时间，以及时区）。</span><span class="sxs-lookup"><span data-stu-id="c52a1-112">Process-specific properties, such as execution date and time, and time zone.</span></span>
        - <span data-ttu-id="c52a1-113">用户输入参数（在运行时由最终用户指定）。</span><span class="sxs-lookup"><span data-stu-id="c52a1-113">User input parameters, specified by the end user at run time.</span></span>

    - <span data-ttu-id="c52a1-114">定义所需文档的元素及其拓扑结构以指定最终文档格式。</span><span class="sxs-lookup"><span data-stu-id="c52a1-114">Define the required document elements and their topology to specify a final document format.</span></span>
    - <span data-ttu-id="c52a1-115">配置从所选数据源到定义的文档元素的所需数据流（通过绑定到文档格式组件的数据源）并指定流程控制逻辑。</span><span class="sxs-lookup"><span data-stu-id="c52a1-115">Configure the desired flow of data from selected data sources to defined document elements (via data source bindings to document format components), and specify process control logic.</span></span>

- <span data-ttu-id="c52a1-116">将一个模板变为可用，以便可以在其他实例中使用：</span><span class="sxs-lookup"><span data-stu-id="c52a1-116">Make a template available so that it can be used in other instances:</span></span>

    - <span data-ttu-id="c52a1-117">将创建的文档模板转换为 ER 配置，并且从当前应用程序实例导出配置为可以存储在本地或 LCS 中的 XML 包。</span><span class="sxs-lookup"><span data-stu-id="c52a1-117">Transform a document template that was created into an ER configuration, and export the configuration from the current application instance as an XML package that can be stored either locally or in LCS.</span></span>
    - <span data-ttu-id="c52a1-118">将 ER 配置转换为应用程序文档模板。</span><span class="sxs-lookup"><span data-stu-id="c52a1-118">Transform an ER configuration into an application document template.</span></span>
    - <span data-ttu-id="c52a1-119">将存储在本地或 LCS 中的 XML 包导入到当前实例。</span><span class="sxs-lookup"><span data-stu-id="c52a1-119">Import an XML package that is stored either locally or in LCS into the current instance.</span></span>

- <span data-ttu-id="c52a1-120">自定义电子文档模板：</span><span class="sxs-lookup"><span data-stu-id="c52a1-120">Customize the template of an electronic document:</span></span>

    - <span data-ttu-id="c52a1-121">从 LCS 将模板作为 ER 配置导入到当前实例。</span><span class="sxs-lookup"><span data-stu-id="c52a1-121">Bring a template from LCS into the current instance as an ER configuration.</span></span>
    - <span data-ttu-id="c52a1-122">设计自定义版本的 ER 配置，并保留对其基础版本的引用。</span><span class="sxs-lookup"><span data-stu-id="c52a1-122">Design a custom version of an ER configuration, and keep a reference to the base version.</span></span>

- <span data-ttu-id="c52a1-123">将模板与特定业务流程集成，以使它在应用程序中可用：</span><span class="sxs-lookup"><span data-stu-id="c52a1-123">Integrate a template with a particular business process, so that it's available in the application:</span></span>

    - <span data-ttu-id="c52a1-124">通过在流程相关参数中引用该配置来配置设置以便应用程序开始使用 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="c52a1-124">Configure settings so that the application starts to use an ER configuration, by referring to that configuration in a process-related parameter.</span></span> <span data-ttu-id="c52a1-125">例如，引用特定应付帐款付款方式中的 ER 配置以生成用于处理发票的电子付款消息。</span><span class="sxs-lookup"><span data-stu-id="c52a1-125">For example, refer to the ER configuration in a specific Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span>

- <span data-ttu-id="c52a1-126">使用特定的业务流程中的模板：</span><span class="sxs-lookup"><span data-stu-id="c52a1-126">Use a template in a specific business process:</span></span>

    - <span data-ttu-id="c52a1-127">在特定的业务流程中运行 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="c52a1-127">Run an ER configuration in a specific business process.</span></span> <span data-ttu-id="c52a1-128">例如，要在选择了引用 ER 配置的付款方式时生成用于处理发票的电子付款消息。</span><span class="sxs-lookup"><span data-stu-id="c52a1-128">For example, to generate an electronic payment message for processing invoices when a payment method that references the ER configuration is selected.</span></span>

## <a name="concepts"></a><span data-ttu-id="c52a1-129">概念</span><span class="sxs-lookup"><span data-stu-id="c52a1-129">Concepts</span></span>
<span data-ttu-id="c52a1-130">以下角色和相关活动与 ER 配置生命周期相关。</span><span class="sxs-lookup"><span data-stu-id="c52a1-130">The following roles and related activities are associated with the ER configuration lifecycle.</span></span>

| <span data-ttu-id="c52a1-131">角色</span><span class="sxs-lookup"><span data-stu-id="c52a1-131">Role</span></span>                                       | <span data-ttu-id="c52a1-132">活动</span><span class="sxs-lookup"><span data-stu-id="c52a1-132">Activities</span></span>                                                      | <span data-ttu-id="c52a1-133">说明</span><span class="sxs-lookup"><span data-stu-id="c52a1-133">Description</span></span> |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| <span data-ttu-id="c52a1-134">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="c52a1-134">Electronic reporting functional consultant</span></span> | <span data-ttu-id="c52a1-135">创建和管理 ER 组件（模型和格式）。</span><span class="sxs-lookup"><span data-stu-id="c52a1-135">Create and manage ER components (models and formats).</span></span>           | <span data-ttu-id="c52a1-136">设计 ER 域特定数据模型、设计电子文档的所需模板并将它们进行相应绑定的业务人员。</span><span class="sxs-lookup"><span data-stu-id="c52a1-136">A business person who designs ER domain–specific data models, designs the required templates for electronic documents, and binds them accordingly.</span></span> |
| <span data-ttu-id="c52a1-137">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="c52a1-137">Electronic reporting developer</span></span>             | <span data-ttu-id="c52a1-138">创建和管理数据模型映射。</span><span class="sxs-lookup"><span data-stu-id="c52a1-138">Create and manage data model mappings.</span></span>                          | <span data-ttu-id="c52a1-139">选择所需的 Finance 数据源并将它们绑定到 ER 域特定数据模型的专业人员。</span><span class="sxs-lookup"><span data-stu-id="c52a1-139">A specialist who selects the required Finance data sources and binds them to ER domain–specific data models.</span></span> |
| <span data-ttu-id="c52a1-140">会计主管</span><span class="sxs-lookup"><span data-stu-id="c52a1-140">Accounting supervisor</span></span>                      | <span data-ttu-id="c52a1-141">配置引用 ER 项目的流程相关设置。</span><span class="sxs-lookup"><span data-stu-id="c52a1-141">Configure process-related settings that reference ER artifacts.</span></span> | <span data-ttu-id="c52a1-142">例如，允许 ER 配置设置用于特定应付帐款付款方式来生成用于处理发票的电子付款消息的 **会计主管** 角色。</span><span class="sxs-lookup"><span data-stu-id="c52a1-142">For example, an **Accounting supervisor** role that allows the settings of an ER configuration to be used in a particular Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span> |
| <span data-ttu-id="c52a1-143">应付帐款付款员</span><span class="sxs-lookup"><span data-stu-id="c52a1-143">Accounts payable payments clerk</span></span>            | <span data-ttu-id="c52a1-144">使用特定业务流程中的 ER 项目。</span><span class="sxs-lookup"><span data-stu-id="c52a1-144">Use ER artifacts in a specific business process.</span></span>                | <span data-ttu-id="c52a1-145">例如，允许基于为特定付款方式配置的 ER 格式为处理发票生成电子付款消息的 **应付帐款付款员**。</span><span class="sxs-lookup"><span data-stu-id="c52a1-145">For example, an **Accounts payable payments clerk** role that allows electronic payment messages to be generated for processing invoices, based on the ER format that is configured for a specific payment method.</span></span> |

## <a name="er-configuration-development-lifecycle"></a><span data-ttu-id="c52a1-146">ER 配置开发生命周期</span><span class="sxs-lookup"><span data-stu-id="c52a1-146">ER configuration development lifecycle</span></span>
<span data-ttu-id="c52a1-147">出于以下与 ER 相关的原因，我们建议您在开发环境中将 ER 配置设计为单独的 Finance and Operations 实例：</span><span class="sxs-lookup"><span data-stu-id="c52a1-147">For the following ER-related reasons, we recommend that you design ER configurations in the development environment, as a separate instance of Finance and Operations:</span></span>

- <span data-ttu-id="c52a1-148">担当 **电子申报开发人员** 角色或 **电子申报功能顾问** 角色的用户可编辑配置，并运行配置以进行测试。</span><span class="sxs-lookup"><span data-stu-id="c52a1-148">Users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can edit configurations and run them for testing purposes.</span></span> <span data-ttu-id="c52a1-149">此情况可能会导致调用类和表的方法，可能对业务数据和实例的性能产生负面影响。</span><span class="sxs-lookup"><span data-stu-id="c52a1-149">This scenario can cause calls of methods of classes and tables that might harm business data and the performance of the instance.</span></span>
- <span data-ttu-id="c52a1-150">在调用作为 ER 配置的 ER 数据源的类和表的方法时，不受入口点和记录的公司内容的限制。</span><span class="sxs-lookup"><span data-stu-id="c52a1-150">Calls of methods of classes and tables as ER data sources of ER configurations aren't restricted by entry points and logged company content.</span></span> <span data-ttu-id="c52a1-151">因此，担当 **电子申报开发人员** 角色或 **电子申报功能顾问** 角色的用户可访问业务敏感数据。</span><span class="sxs-lookup"><span data-stu-id="c52a1-151">Therefore, users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can access business-sensitive data.</span></span>

<span data-ttu-id="c52a1-152">在开发环境中设计的 ER 配置可上传到测试环境以进行配置评估（适当的流程集成、结果的正确性、性能）和质量保证（如角色驱动的访问权限的正确性和职责划分）。</span><span class="sxs-lookup"><span data-stu-id="c52a1-152">ER configurations that are designed in the development environment can be uploaded to the test environment for the configuration evaluation (proper process integration, correctness of results, and performance) and quality assurance, such as correctness of role-driven access rights and segregation of duties.</span></span> <span data-ttu-id="c52a1-153">启用 ER 配置交换的功能可以用于此目的。</span><span class="sxs-lookup"><span data-stu-id="c52a1-153">The features that enable ER configuration interchange can be used for this purpose.</span></span> <span data-ttu-id="c52a1-154">最后，已审核的 ER 配置可上传到 LCS，在其中这些配置可与服务订阅者共享，也可上传到生产环境以供内部使用，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="c52a1-154">Finally, proven ER configurations can be uploaded either to LCS, where they can be shared with service subscribers, or to the production environment for internal use, such as shown in the following illustration.</span></span>

![ER 配置生命周期](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a><span data-ttu-id="c52a1-156">其他资源</span><span class="sxs-lookup"><span data-stu-id="c52a1-156">Additional resources</span></span>

[<span data-ttu-id="c52a1-157">电子申报 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="c52a1-157">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

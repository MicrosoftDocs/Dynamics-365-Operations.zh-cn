---
title: 在 ER 模型映射中使用 JOIN 数据源从多个应用程序表中获取数据
description: 本主题介绍如何在电子申报 (ER) 中使用 JOIN 类型数据源。
author: NickSelin
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: be5646eaf395310c8b34586ef1274a41b5b97029
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944695"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a><span data-ttu-id="84797-103">在电子申报 (ER) 模型映射中使用 JOIN 数据源从多个应用程序表中获取数据</span><span class="sxs-lookup"><span data-stu-id="84797-103">Use JOIN data sources to get data from multiple application tables in Electronic reporting (ER) model mappings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="84797-104">在配置电子申报 (ER) 模型映射或格式时，您可以 [添加](#review) **Join** 类型的必需数据源。</span><span class="sxs-lookup"><span data-stu-id="84797-104">While configuring Electronic reporting (ER) model mappings or formats, you can [add](#review) required data sources of the **Join** type.</span></span> <span data-ttu-id="84797-105">在设计时，将 **Join** 数据源配置为一组数据源，每个数据源都返回记录列表。</span><span class="sxs-lookup"><span data-stu-id="84797-105">At design time, a **Join** data source is configured as a set of several data sources each of which returns a list of records.</span></span> <span data-ttu-id="84797-106">对于除第一个数据源外的每个数据源，您都需要定义必要条件以联接当前和先前数据源的记录。</span><span class="sxs-lookup"><span data-stu-id="84797-106">For every data source except the first one, you need to define necessary conditions to join records of the current and previous data sources.</span></span> <span data-ttu-id="84797-107">在运行时，配置的 **Join** 类型的数据源[返回](#executeERformat)包含嵌套数据源记录中字段的记录的单个联接列表。</span><span class="sxs-lookup"><span data-stu-id="84797-107">At runtime, a configured data source of **Join** type [returns](#executeERformat) a single joined list of records containing fields from the records of nested data sources.</span></span>

<span data-ttu-id="84797-108">当前支持以下联接类型：</span><span class="sxs-lookup"><span data-stu-id="84797-108">The following types of joins are currently supported:</span></span>

- <span data-ttu-id="84797-109">外部（左）联接：</span><span class="sxs-lookup"><span data-stu-id="84797-109">Outer (left) join:</span></span>
    - <span data-ttu-id="84797-110">联接第一个（最左侧）数据源的所有记录，然后联接根据第二个（最右侧）数据源的配置条件记录进行的任何匹配。</span><span class="sxs-lookup"><span data-stu-id="84797-110">Join all records of the first (left-most) data source and then any matching in accordance to configured conditions records of the second (right-most) data source.</span></span>
- <span data-ttu-id="84797-111">内部（右）联接：</span><span class="sxs-lookup"><span data-stu-id="84797-111">Inner (right) join:</span></span>
    - <span data-ttu-id="84797-112">仅联接第一个（最左侧）数据源的记录，并仅联接根据配置的条件相互匹配的第二个（最右侧）数据源的记录。</span><span class="sxs-lookup"><span data-stu-id="84797-112">Join only records of the first (left-most) data source and only records of the second (right-most) data source matching to each other in accordance to configured conditions.</span></span>

<span data-ttu-id="84797-113">在配置的 **Join** 数据源中，当所有数据源均为 **表记录** 类型时，可以使用单个 SQL 语句[在数据库级别执行](#analyze) Join 数据源的执行。</span><span class="sxs-lookup"><span data-stu-id="84797-113">In the configured **Join** data source, when all data sources are the **Table records** type, execution of the Join data source can be [performed at the database level](#analyze) using a single SQL statement.</span></span> <span data-ttu-id="84797-114">此语句将减少数据库调用的次数，从而提高模型映射的性能。</span><span class="sxs-lookup"><span data-stu-id="84797-114">This statement reduces the number of database calls, which improves model-mapping performance.</span></span> <span data-ttu-id="84797-115">否则，将在内存中执行 **Join 数据** 源。</span><span class="sxs-lookup"><span data-stu-id="84797-115">Otherwise, execution of **Join data** source is performed in memory.</span></span>

> [!NOTE]
> <span data-ttu-id="84797-116">目前尚不支持在 ER 表达式中使用 **VALUEIN** 函数来指定联接类型为 Join 的数据源中的记录的条件。</span><span class="sxs-lookup"><span data-stu-id="84797-116">Using the **VALUEIN** function in ER expressions that specify conditions for joining records in data sources of Join type is not supported yet.</span></span> <span data-ttu-id="84797-117">有关此函数的更多详细信息，请访问[电子申报中的配方设计器](general-electronic-reporting-formula-designer.md)页面。</span><span class="sxs-lookup"><span data-stu-id="84797-117">Visit the [Formula designer in Electronic reporting](general-electronic-reporting-formula-designer.md) page for more details about this function.</span></span>

<span data-ttu-id="84797-118">若要了解有关此功能的详细信息，请完成本主题中的示例。</span><span class="sxs-lookup"><span data-stu-id="84797-118">To learn more about this feature, complete the example in this topic.</span></span>

## <a name="example-use-join-data-sources-in-er-model-mappings"></a><span data-ttu-id="84797-119">示例：在 ER 模型映射中使用 JOIN 数据源</span><span class="sxs-lookup"><span data-stu-id="84797-119">Example: Use JOIN data sources in ER model mappings</span></span>

<span data-ttu-id="84797-120">以下步骤说明了系统管理员或电子申报开发人员如何配置电子申报 (ER) 模型映射，以通过使用 **Join** 类型的数据源来一次从多个应用程序表中获取数据，从而提高数据访问性能。</span><span class="sxs-lookup"><span data-stu-id="84797-120">The following steps explain how the System administrator or Electronic reporting developer can configure an Electronic reporting (ER) model mapping to get data from multiple application tables at once by using data sources of the **Join** type to improve data access performance.</span></span> <span data-ttu-id="84797-121">Dynamics 365 Finance 或 Regulatory Configuration Services (RCS) 的任何公司都可以执行这些步骤。</span><span class="sxs-lookup"><span data-stu-id="84797-121">These steps can be performed for any company of Dynamics 365 Finance or Regulatory Configuration Services (RCS).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="84797-122">先决条件</span><span class="sxs-lookup"><span data-stu-id="84797-122">Prerequisites</span></span>

<span data-ttu-id="84797-123">要完成本主题中的示例，您必须有权使用以下服务之一（具体取决于哪个服务用于完成这些步骤）：</span><span class="sxs-lookup"><span data-stu-id="84797-123">To complete the examples in this topic, you must have access to one of the following depending on what service is used to compete these steps:</span></span>

<span data-ttu-id="84797-124">**访问 Finance 的以下其中一个角色：**</span><span class="sxs-lookup"><span data-stu-id="84797-124">**Access to Finance for one of the following roles:**</span></span>

- <span data-ttu-id="84797-125">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="84797-125">Electronic reporting developer</span></span>
- <span data-ttu-id="84797-126">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="84797-126">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="84797-127">系统管理员</span><span class="sxs-lookup"><span data-stu-id="84797-127">System administrator</span></span>

<span data-ttu-id="84797-128">**访问 RCS 的以下其中一个角色：**</span><span class="sxs-lookup"><span data-stu-id="84797-128">**Access to RCS for one of the following roles:**</span></span>

- <span data-ttu-id="84797-129">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="84797-129">Electronic reporting developer</span></span>
- <span data-ttu-id="84797-130">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="84797-130">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="84797-131">系统管理员</span><span class="sxs-lookup"><span data-stu-id="84797-131">System administrator</span></span>

<span data-ttu-id="84797-132">您还必须首先完成[创建配置提供程序并标记为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="84797-132">You also must first complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

<span data-ttu-id="84797-133">事先，您还必须下载并保存以下示例 ER 配置文件：</span><span class="sxs-lookup"><span data-stu-id="84797-133">In advance, you must also download and save the following sample ER configuration files:</span></span>

| <span data-ttu-id="84797-134">**内容描述**</span><span class="sxs-lookup"><span data-stu-id="84797-134">**Content description**</span></span>  | <span data-ttu-id="84797-135">**文件名**</span><span class="sxs-lookup"><span data-stu-id="84797-135">**File name**</span></span>   |
|--------------------------|-----------------|
| <span data-ttu-id="84797-136">示例 **ER 数据模型** 配置文件，用作示例的数据源。</span><span class="sxs-lookup"><span data-stu-id="84797-136">Sample **ER data model** configuration file, which is used as the data source for the examples.</span></span>| [<span data-ttu-id="84797-137">Model to learn JOIN data sources.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="84797-137">Model to learn JOIN data sources.version.1.1.xml</span></span>](https://download.microsoft.com/download/5/c/1/5c1d8a57-6ebd-425b-bc5d-c71dde92c6af/ModeltolearnJOINdatasources.version.1.xml) |
| <span data-ttu-id="84797-138">示例 **ER 模型映射** 配置文件，为示例实现 ER 数据模型。</span><span class="sxs-lookup"><span data-stu-id="84797-138">Sample **ER model mapping** configuration file, which implements the ER data model for the examples.</span></span> | [<span data-ttu-id="84797-139">Mapping to learn JOIN data sources.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="84797-139">Mapping to learn JOIN data sources.version.1.1.xml</span></span>](https://user-images.githubusercontent.com/19827601/115923048-86b10400-a432-11eb-9e57-c37a02effcb4.png)|
| <span data-ttu-id="84797-140">示例 **ER 格式** 配置文件。</span><span class="sxs-lookup"><span data-stu-id="84797-140">Sample **ER format** configuration file.</span></span> <span data-ttu-id="84797-141">此文件介绍用于为示例填充 ER 格式组件的数据。</span><span class="sxs-lookup"><span data-stu-id="84797-141">This file describes the data to populate the ER format component for the examples.</span></span> | [<span data-ttu-id="84797-142">Format to learn JOIN data sources.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="84797-142">Format to learn JOIN data sources.version.1.1.xml</span></span>](https://download.microsoft.com/download/f/f/8/ff8f1b48-14d0-4c73-9145-bcdf8b5265bc/FormattolearnJOINdatasources.version.1.1.xml) |

### <a name="activate-a-configurations-provider"></a><span data-ttu-id="84797-143">启用配置提供程序</span><span class="sxs-lookup"><span data-stu-id="84797-143">Activate a configurations provider</span></span>

1. <span data-ttu-id="84797-144">在 Web 浏览器的第一个会话中访问 Finance 或 RCS。</span><span class="sxs-lookup"><span data-stu-id="84797-144">Access either Finance or RCS in the first session of your web browser.</span></span>
2. <span data-ttu-id="84797-145">转到 **组织管理 \> 工作区 \> 电子申报**。</span><span class="sxs-lookup"><span data-stu-id="84797-145">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
3. <span data-ttu-id="84797-146">在 **本地化配置** 页上的 **配置提供程序** 部分中，确保列出了示例公司 [Litware, Inc.](http://www.litware.com) 的配置提供程序，并将其标记为 **活动状态**。</span><span class="sxs-lookup"><span data-stu-id="84797-146">On the **Localization configurations** page, in the **Configuration providers** section, make sure that the configuration provider for the [Litware, Inc.](http://www.litware.com) sample company is listed, and that it's marked as **Active**.</span></span> <span data-ttu-id="84797-147">如果没有看到此配置提供程序，请执行[创建配置提供程序并标记为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="84797-147">If you don't see this configuration provider, follow the steps in [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

    ![电子申报工作区](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a><span data-ttu-id="84797-149">导入示例 ER 配置文件</span><span class="sxs-lookup"><span data-stu-id="84797-149">Import sample ER configuration files</span></span>

1. <span data-ttu-id="84797-150">选择 **申报配置**。</span><span class="sxs-lookup"><span data-stu-id="84797-150">Select **Reporting configurations**.</span></span>
2. <span data-ttu-id="84797-151">导入 ER 数据模型配置文件。</span><span class="sxs-lookup"><span data-stu-id="84797-151">Import the ER data model configuration file.</span></span>
    1. <span data-ttu-id="84797-152">选择 **交换**。</span><span class="sxs-lookup"><span data-stu-id="84797-152">Select **Exchange**.</span></span>
    2. <span data-ttu-id="84797-153">选择 **从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="84797-153">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="84797-154">选择 **浏览** 找到 **Model to learn JOIN data sources.version.1.1.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="84797-154">Select **Browse** to find the **Model to learn JOIN data sources.version.1.1.xml** file.</span></span>
    4. <span data-ttu-id="84797-155">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="84797-155">Select **OK**.</span></span>
3. <span data-ttu-id="84797-156">导入 ER 模型映射配置文件。</span><span class="sxs-lookup"><span data-stu-id="84797-156">Import the ER model-mapping configuration file.</span></span>
    1. <span data-ttu-id="84797-157">选择 **交换**。</span><span class="sxs-lookup"><span data-stu-id="84797-157">Select **Exchange**.</span></span>
    2. <span data-ttu-id="84797-158">选择 **从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="84797-158">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="84797-159">选择 **浏览** 找到 **Mapping to learn JOIN data sources.version.1.1.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="84797-159">Select **Browse** to find the **Mapping to learn JOIN data sources.version.1.1.xml** file.</span></span>
    4. <span data-ttu-id="84797-160">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="84797-160">Select **OK**.</span></span>
4. <span data-ttu-id="84797-161">导入 ER 格式配置文件。</span><span class="sxs-lookup"><span data-stu-id="84797-161">Import the ER format configuration file.</span></span>
    1. <span data-ttu-id="84797-162">选择 **交换**。</span><span class="sxs-lookup"><span data-stu-id="84797-162">Select **Exchange**.</span></span>
    2. <span data-ttu-id="84797-163">选择 **从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="84797-163">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="84797-164">选择 **浏览** 找到 **Format to learn JOIN data sources.version.1.1.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="84797-164">Select **Browse** to find the **Format to learn JOIN data sources.version.1.1.xml** file.</span></span>
    4. <span data-ttu-id="84797-165">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="84797-165">Select **OK**.</span></span>
5. <span data-ttu-id="84797-166">在配置树中，展开 **用于了解 JOIN 数据源的模型** 项目以及其他模型项目（如果有）。</span><span class="sxs-lookup"><span data-stu-id="84797-166">In the configurations tree, expand the **Model to learn JOIN data sources** item as well as other model items (when available).</span></span>
6. <span data-ttu-id="84797-167">观察树中的 ER 配置列表以及 **版本** 快速选项卡上的版本详细信息 – 它们将用作示例报表的数据源。</span><span class="sxs-lookup"><span data-stu-id="84797-167">Observe the list of ER configurations in the tree as well as version details on the **Versions** FastTab – they will be used as the source of data for your sample report.</span></span>

    ![电子申报配置页面](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a><span data-ttu-id="84797-169">打开执行跟踪选项</span><span class="sxs-lookup"><span data-stu-id="84797-169">Turn on execution trace options</span></span>

1. <span data-ttu-id="84797-170">选择 **配置**。</span><span class="sxs-lookup"><span data-stu-id="84797-170">Select **CONFIGURATIONS**.</span></span>
2. <span data-ttu-id="84797-171">选择 **用户参数**。</span><span class="sxs-lookup"><span data-stu-id="84797-171">Select **User parameters**.</span></span>
3. <span data-ttu-id="84797-172">设置执行跟踪参数，如下面的屏幕截图所示。</span><span class="sxs-lookup"><span data-stu-id="84797-172">Set execution trace parameters as shown on the screenshot below.</span></span>

    ![电子申报用户参数页面](./media/GER-JoinDS-Parameters.PNG)

    <span data-ttu-id="84797-174">启用这些参数后，对于导入的 ER 格式文件的每次执行，都会生成执行跟踪。</span><span class="sxs-lookup"><span data-stu-id="84797-174">With these parameters turned on, for every execution of the imported ER format file, the execution trace will be generated.</span></span> <span data-ttu-id="84797-175">使用生成的执行跟踪的详细信息，您可以分析 ER 格式和 ER 模型映射组件的执行。</span><span class="sxs-lookup"><span data-stu-id="84797-175">Using details of generated execution trace, you can analyze the execution of ER format and ER model-mapping components.</span></span> <span data-ttu-id="84797-176">请访问[跟踪 ER 格式的执行情况以解决性能问题](trace-execution-er-troubleshoot-perf.md)页面，了解有关 ER 执行跟踪功能的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="84797-176">Visit the [Trace execution of ER format to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md) page for more details about ER execution trace feature.</span></span>

### <a name="review-er-model-mapping-part-1"></a><span data-ttu-id="84797-177">查看 ER 模型映射（第 1 部分）</span><span class="sxs-lookup"><span data-stu-id="84797-177">Review ER model mapping (part 1)</span></span>

<span data-ttu-id="84797-178">查看 ER 模型映射组件的设置。</span><span class="sxs-lookup"><span data-stu-id="84797-178">Review settings of the ER model-mapping component.</span></span> <span data-ttu-id="84797-179">该组件配置为访问有关 ER 配置版本、配置详细信息和配置提供程序的信息，而无需使用 **Join** 类型的数据源。</span><span class="sxs-lookup"><span data-stu-id="84797-179">The component is configured to access information about versions of ER configurations, details of configurations and configuration providers without using data sources of the **Join** type.</span></span>

1. <span data-ttu-id="84797-180">选择 **用于了解 JOIN 数据源的映射** 配置。</span><span class="sxs-lookup"><span data-stu-id="84797-180">Select **Mapping to learn JOIN data sources** configuration.</span></span>
2. <span data-ttu-id="84797-181">选择 **设计器** 来打开映射列表。</span><span class="sxs-lookup"><span data-stu-id="84797-181">Select **Designer** to open the list of mappings.</span></span>
3. <span data-ttu-id="84797-182">选择 **设计器** 查看映射详细信息。</span><span class="sxs-lookup"><span data-stu-id="84797-182">Select **Designer** to review the mapping details.</span></span>
4. <span data-ttu-id="84797-183">选择 **显示详细信息**。</span><span class="sxs-lookup"><span data-stu-id="84797-183">Select **Show details**.</span></span>
5. <span data-ttu-id="84797-184">在配置树中，展开 **Set1** 和 **Set1.Details** 数据模型项目：</span><span class="sxs-lookup"><span data-stu-id="84797-184">In the configurations tree, expand the **Set1** and **Set1.Details** data model items:</span></span>

    1. <span data-ttu-id="84797-185">绑定 **Details: Record list = Versions** 表示 **Set1.Details** 项目已绑定到返回 **ERSolutionVersionTable** 表的记录的 **Versions** 数据源。</span><span class="sxs-lookup"><span data-stu-id="84797-185">Binding **Details: Record list = Versions** indicates that the **Set1.Details** item is bound to the **Versions** data source returning records of the **ERSolutionVersionTable** table.</span></span> <span data-ttu-id="84797-186">此表的每个记录代表一个单独版本的 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="84797-186">Each record of this table represents a single version of an ER configuration.</span></span> <span data-ttu-id="84797-187">此表的内容显示在 **配置** 页面上的 **版本** 快速选项卡中。</span><span class="sxs-lookup"><span data-stu-id="84797-187">The content of this table is presented in the **Versions** FastTab on the **Configurations** page.</span></span>
    2. <span data-ttu-id="84797-188">绑定 **ConfigurationVersion: String = @.PublicVersionNumber** 表示每个 ER 配置版本的公共版本的值均取自 **ERSolutionVersionTable** 表的 **PublicVersionNumber** 字段，并放置到 **ConfigurationVersion** 项目中。</span><span class="sxs-lookup"><span data-stu-id="84797-188">Binding **ConfigurationVersion: String = @.PublicVersionNumber** means that the value of the public version of each ER configuration’s version is taken from the **PublicVersionNumber** field of the **ERSolutionVersionTable** table and placed to the **ConfigurationVersion** item.</span></span>
    3. <span data-ttu-id="84797-189">绑定 **ConfigurationTitle: String = @.'>Relations'.Solution.Name** 表示 ER 配置的名称取自 **ERSolutionTable** 表的 **名称** 字段，该表通过使用 **ERSolutionVersionTable** 和 **ERSolutionTable** 表之间的多对一关系 (**'>Relations'**) 评估。</span><span class="sxs-lookup"><span data-stu-id="84797-189">Binding **ConfigurationTitle: String = @.'>Relations'.Solution.Name** indicates that the name of an ER configuration is taken from the **Name** field of the **ERSolutionTable** table assessing by using the many-to-one relation (**'>Relations'**) between the **ERSolutionVersionTable** and **ERSolutionTable** tables.</span></span> <span data-ttu-id="84797-190">当前应用程序实例的 ER 配置的名称显示在 **配置** 页面上的配置树中。</span><span class="sxs-lookup"><span data-stu-id="84797-190">Names of ER configurations of the current application instance are presented in the configurations tree on the **Configurations** page.</span></span>
    4. <span data-ttu-id="84797-191">绑定 **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** 意味着具有当前配置的配置提供程序的名称取自 **ERVendorTable** 表的 **名称** 字段，该表通过使用 **ERSolutionTable** 和 **ERVendorTable** 表之间的多对一关系进行评估。</span><span class="sxs-lookup"><span data-stu-id="84797-191">Binding **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** means that the name of the configuration provider that owns the current configuration is taken from the **Name** field of the **ERVendorTable** table assessing by using the many-to-one relation between **ERSolutionTable** and **ERVendorTable** tables.</span></span> <span data-ttu-id="84797-192">ER 配置提供程序的名称显示在 **配置** 页面上的配置树中，位于每个配置的页标题上。</span><span class="sxs-lookup"><span data-stu-id="84797-192">Names of ER configuration providers are presented in the configurations tree on the **Configurations** page on the page header for each configuration.</span></span> <span data-ttu-id="84797-193">ER 配置提供程序的完整列表可在 **组织管理 \> 电子申报 \> 配置提供程序** 表页面上找到。</span><span class="sxs-lookup"><span data-stu-id="84797-193">The entire list of ER configuration providers can be found on the **Organization administration \> Electronic reporting \> Configuration provider** table page.</span></span>

    ![ER 模型映射设计器页面，绑定数据模型项的列表](./media/GER-JoinDS-Set1Review.PNG)

6. <span data-ttu-id="84797-195">在配置树中，展开 **Set1.Summary** 数据模型项目：</span><span class="sxs-lookup"><span data-stu-id="84797-195">In the configurations tree, expand the **Set1.Summary** data model item:</span></span>

    1. <span data-ttu-id="84797-196">绑定 **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** 表示 **Set1.Summary.VersionsNumber** 项目绑定到 **GroupBy** 类型的 **VersionsSummary** 数据源的 **VersionsNumber** 合并字段，该类型配置为通过 **Versions** 数据源返回 **ERSolutionVersionTable** 表的记录数。</span><span class="sxs-lookup"><span data-stu-id="84797-196">Binding **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** indicates that the **Set1.Summary.VersionsNumber** item is bound to the **VersionsNumber** aggregation field of the **VersionsSummary** data source of the **GroupBy** type that was configured to return the number of records of the **ERSolutionVersionTable** table via the **Versions** data source.</span></span>

    ![编辑“分组依据”参数页面](./media/GER-JoinDS-Set1GroupByReview.PNG)

7. <span data-ttu-id="84797-198">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="84797-198">Close the page.</span></span>

### <a name="review-er-model-mapping-part-2"></a><a name="review"></a><span data-ttu-id="84797-199">查看 ER 模型映射（第 2 部分）</span><span class="sxs-lookup"><span data-stu-id="84797-199">Review ER model mapping (part 2)</span></span>

<span data-ttu-id="84797-200">查看 ER 模型映射组件的设置。</span><span class="sxs-lookup"><span data-stu-id="84797-200">Review settings of the ER model-mapping component.</span></span> <span data-ttu-id="84797-201">该组件配置为使用 **Join** 类型的数据源访问有关 ER 配置版本、配置详细信息和配置提供程序的信息。</span><span class="sxs-lookup"><span data-stu-id="84797-201">The component is configured to access information about versions of ER configurations, details of configurations and configuration providers with using a data source of the **Join** type.</span></span>

1. <span data-ttu-id="84797-202">在配置树中，展开 **Set2** 和 **Set2.Details** 数据模型项目。</span><span class="sxs-lookup"><span data-stu-id="84797-202">In the configurations tree, expand the **Set2** and **Set2.Details** data model items.</span></span> <span data-ttu-id="84797-203">绑定 **Details: Record list = Details** 表示 **Set2.Details** 项目绑定到配置为 **Join** 类型的数据源的 **Details** 数据源。</span><span class="sxs-lookup"><span data-stu-id="84797-203">The binding **Details: Record list = Details** indicates that the **Set2.Details** item is bound to the **Details** data source configured as the data source of the **Join** type.</span></span>

    ![显示展开的 Set2:Record 数据模型项的 ER 模型映射设计器页面](./media/GER-JoinDS-Set2Review.PNG)

    <span data-ttu-id="84797-205">可以通过选择 **Functions\Join** 数据源来添加 **Join** 数据源：</span><span class="sxs-lookup"><span data-stu-id="84797-205">The **Join** data source can be added by selecting the **Functions\Join** data source:</span></span>

    ![ER 模型映射设计器页面，Join 数据源类型](./media/GER-JoinDS-AddJoinDS.PNG)

2. <span data-ttu-id="84797-207">选择 **Details** 数据源。</span><span class="sxs-lookup"><span data-stu-id="84797-207">Select **Detail** s data source.</span></span>
3. <span data-ttu-id="84797-208">在 **数据源** 窗格中选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="84797-208">Select **Edit** in the **Data sources** pane.</span></span>
4. <span data-ttu-id="84797-209">选择 **编辑联接**。</span><span class="sxs-lookup"><span data-stu-id="84797-209">Select **Edit join**.</span></span>
5. <span data-ttu-id="84797-210">选择 **显示详细信息**。</span><span class="sxs-lookup"><span data-stu-id="84797-210">Select **Show details**.</span></span>

    ![JOIN 数据源参数页面](./media/GER-JoinDS-JoinDSEditor.PNG)

    <span data-ttu-id="84797-212">此页面用于设计 **Join 类型** 的必需数据源。</span><span class="sxs-lookup"><span data-stu-id="84797-212">This page is used to design the required data source of the **Join type**.</span></span> <span data-ttu-id="84797-213">在运行时，此数据源将从 **联接列表** 网格中的数据源创建记录的单个联接列表。</span><span class="sxs-lookup"><span data-stu-id="84797-213">At runtime, this data source will create a single joined list of records from the data sources in the **Joined list** grid.</span></span> <span data-ttu-id="84797-214">记录的联接将从作为第一个网格的网格中的 **ConfigurationProviders** 数据源开始（它的 **类型** 列为空白）。</span><span class="sxs-lookup"><span data-stu-id="84797-214">Join of records will start from the **ConfigurationProviders** data source that is in the grid as a first one (the **Type** column is blank for it).</span></span> <span data-ttu-id="84797-215">因此，将根据每个其他数据源在此网格中的顺序将其记录联接到父数据源的记录。</span><span class="sxs-lookup"><span data-stu-id="84797-215">Records of every other data source will be joined consequently to records of the parent data source based on its order in this grid.</span></span> <span data-ttu-id="84797-216">每个联接的数据源都必须配置为嵌套在目标数据源下的数据源（`1Versions` 数据源嵌套在 `1Configurations` 数据源下；`1Configurations` 数据源嵌套在 **ConfigurationProviders** 数据源下）。</span><span class="sxs-lookup"><span data-stu-id="84797-216">Every joining data source must be configured as a data source nested under a target data source (`1Versions` data source is nested under `1Configurations` one; `1Configurations` data source is nested under **ConfigurationProviders** one).</span></span> <span data-ttu-id="84797-217">每个配置的数据源都必须包含联接条件。</span><span class="sxs-lookup"><span data-stu-id="84797-217">Each configured data source must contain the conditions for the join.</span></span> <span data-ttu-id="84797-218">在此 **Join** 的数据源中，定义了以下联接：</span><span class="sxs-lookup"><span data-stu-id="84797-218">In the data source for this particular **Join**, the following joins are defined:</span></span>

    - <span data-ttu-id="84797-219">**ConfigurationProviders** 数据源的每条记录（在 **ERVendorTable** 表中介绍）仅与 **1Configurations** 数据源的记录（在 **ERSolutionTable** 表中介绍）连接，从而在 **SolutionVendor** 和 **RecId** 字段中具有相同的值。</span><span class="sxs-lookup"><span data-stu-id="84797-219">Each record of the **ConfigurationProviders** data source (referred to the **ERVendorTable** table) is joined with only records of the **1Configurations** one (referred to in the **ERSolutionTable** table) having the same value in the **SolutionVendor** and **RecId** fields.</span></span> <span data-ttu-id="84797-220">**内联接** 类型用于此连接，以及用于匹配记录的以下条件：</span><span class="sxs-lookup"><span data-stu-id="84797-220">The **Inner join** type is used for this join as well as the following conditions for matching records:</span></span>

    <span data-ttu-id="84797-221">FILTER（Configurations，Configurations.SolutionVendor = ConfigurationProviders.RecId）</span><span class="sxs-lookup"><span data-stu-id="84797-221">FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)</span></span>

    - <span data-ttu-id="84797-222">**1Configurations** 数据源的每条记录（在 **ERSolutionTable** 表中介绍）仅与 **1Versions** 数据源的记录（在 **ERSolutionVersionTable** 表中介绍）连接，从而在 **Solution** 和 **RecId** 字段中具有相同的值。</span><span class="sxs-lookup"><span data-stu-id="84797-222">Each record of the **1Configurations** data source (referred to the **ERSolutionTable** table) is joined with the only records of the **1Versions** one (referred to the **ERSolutionVersionTable** table) having the same value in the **Solution** and **RecId** fields.</span></span> <span data-ttu-id="84797-223">**内联接** 类型用于此连接以及用于匹配记录的以下条件：</span><span class="sxs-lookup"><span data-stu-id="84797-223">**Inner join** type is used for this join as well as the following conditions for matching records:</span></span>

    <span data-ttu-id="84797-224">FILTER（ConfigurationVersions，ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId）</span><span class="sxs-lookup"><span data-stu-id="84797-224">FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)</span></span>

    - <span data-ttu-id="84797-225">**执行** 选项配置为 **查询**，这意味着此联接数据源将在运行时在数据库级别作为直接 SQL 调用执行。</span><span class="sxs-lookup"><span data-stu-id="84797-225">**Execute** option is configured as **Query** meaning that this join data source will be executed at runtime on database level as a direct SQL call.</span></span>

    <span data-ttu-id="84797-226">对于联接表示应用程序表的数据源的记录，可以使用除描述这些表之间的 AOT 关系中现有字段以外的其他字段对来指定联接条件。</span><span class="sxs-lookup"><span data-stu-id="84797-226">For joining records of data sources representing application tables, you can specify join conditions by using pairs of fields other than ones that describe existing in AOT relations between these tables.</span></span> <span data-ttu-id="84797-227">还可以将此类型的联接配置为在数据库级别执行。</span><span class="sxs-lookup"><span data-stu-id="84797-227">This type of join can be configured to execute at the database level as well.</span></span>

6. <span data-ttu-id="84797-228">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="84797-228">Close the page.</span></span>
7. <span data-ttu-id="84797-229">选择 **取消**。</span><span class="sxs-lookup"><span data-stu-id="84797-229">Select **Cancel**.</span></span>
8. <span data-ttu-id="84797-230">在配置树中，展开 **Set2.Summary** 数据模型项目：</span><span class="sxs-lookup"><span data-stu-id="84797-230">In the configurations tree, expand the **Set2.Summary** data model item:</span></span>

    - <span data-ttu-id="84797-231">绑定 **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** 表示 **Set2.Summary.VersionsNumber** 项目绑定到 **GroupBy** 类型的 **DetailsSummary** 数据源的 **VersionsNumber** 合并字段，该类型配置为返回 **Join** 类型的 **Details** 数据源的联接记录数。</span><span class="sxs-lookup"><span data-stu-id="84797-231">Binding **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** indicates that the **Set2.Summary.VersionsNumber** item is bound to the **VersionsNumber** aggregation field of the **DetailsSummary** data source of the **GroupBy** type that was configured to return the number of joined records of the **Details** data source of the **Join** type.</span></span>
    - <span data-ttu-id="84797-232">**执行** 位置选项配置为 **查询**，这意味着此 **GroupBy** 数据源将在运行时在数据库级别作为直接 SQL 调用运行。</span><span class="sxs-lookup"><span data-stu-id="84797-232">The **Execution** location option is configured as **Query** meaning that this **GroupBy** data source will be run at runtime as a direct SQL call at the database level.</span></span> <span data-ttu-id="84797-233">能够实现此行为是因为 **Join** 类型的基础数据源 **Details** 被配置为在数据库级别执行。</span><span class="sxs-lookup"><span data-stu-id="84797-233">This behavior is possible because the base data source **Details** of the **Join** type is configured as executed at the database level.</span></span>

    ![GROUPBY 数据源参数页面](./media/GER-JoinDS-Set2GroupByReview.PNG)

9. <span data-ttu-id="84797-235">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="84797-235">Close the page.</span></span>
10. <span data-ttu-id="84797-236">选择 **取消**。</span><span class="sxs-lookup"><span data-stu-id="84797-236">Select **Cancel**.</span></span>

### <a name="execute-er-format"></a><a name="executeERformat"></a> <span data-ttu-id="84797-237">执行 ER 格式</span><span class="sxs-lookup"><span data-stu-id="84797-237">Execute ER format</span></span>

1. <span data-ttu-id="84797-238">使用与第一个会话相同的凭据和公司，在 Web 浏览器的第二个会话中访问 Finance 或 RCS。</span><span class="sxs-lookup"><span data-stu-id="84797-238">Access Finance or RCS in the second session of your web browser using same credentials and company as in the first session.</span></span>
2. <span data-ttu-id="84797-239">转到 **组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="84797-239">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="84797-240">展开 **用于了解 JOIN 数据源的模型** 配置。</span><span class="sxs-lookup"><span data-stu-id="84797-240">Expand **Model to learn JOIN data sources** configuration.</span></span>
4. <span data-ttu-id="84797-241">选择 **用于了解 JOIN 数据源的格式** 配置。</span><span class="sxs-lookup"><span data-stu-id="84797-241">Select **Format to learn JOIN data sources** configuration.</span></span>
5. <span data-ttu-id="84797-242">选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="84797-242">Select **Designer**.</span></span>
6. <span data-ttu-id="84797-243">选择 **显示详细信息**。</span><span class="sxs-lookup"><span data-stu-id="84797-243">Select **Show details**.</span></span>
7. <span data-ttu-id="84797-244">选择 **映射**。</span><span class="sxs-lookup"><span data-stu-id="84797-244">Select **Mapping**.</span></span>
8. <span data-ttu-id="84797-245">选择 **展开/折叠**。</span><span class="sxs-lookup"><span data-stu-id="84797-245">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="84797-246">此格式用于为 ER 配置的每个版本使用新行填充生成的文本文件（**版本** 顺序）。</span><span class="sxs-lookup"><span data-stu-id="84797-246">This format is designed to populate a generated text file with a new line for every version of an ER configuration (**Version** sequence).</span></span> <span data-ttu-id="84797-247">每个生成的行将包含拥有当前配置的配置提供程序的名称、配置名称和配置版本，并以分号分隔。</span><span class="sxs-lookup"><span data-stu-id="84797-247">Each generated line will contain the name of a configuration provider owning the current configuration, the configuration name, and the configuration version separated by semicolon mark.</span></span> <span data-ttu-id="84797-248">生成文件的最后一行将包含已发现的 ER 配置的版本数（**摘要** 顺序）。</span><span class="sxs-lookup"><span data-stu-id="84797-248">The final line of generated file will contain the number of discovered versions of ER configurations (**Summary** sequence).</span></span>

    ![ER 格式设计器页面，“格式”选项卡](./media/GER-JoinDS-FormatReview.PNG)

    <span data-ttu-id="84797-250">**Data** 和 **Summary** 数据源用于将配置版本详细信息填充到生成的文件中：</span><span class="sxs-lookup"><span data-stu-id="84797-250">The **Data** and **Summary** data sources are used to populate configuration version details to the generated file:</span></span>

    - <span data-ttu-id="84797-251">在运行 ER 格式时，运行时在用户对话框页面上为 **Selector** 数据源选择 **否** 时，将使用来自 **Set1** 数据模型的信息。</span><span class="sxs-lookup"><span data-stu-id="84797-251">Information from the **Set1** data model is used when you choose **No** for the **Selector** data source at runtime on the user dialog page when running ER format.</span></span>
    - <span data-ttu-id="84797-252">运行时在用户对话框页面上为 **Selector** 数据源选择 **是** 时，将使用来自 **Set2** 数据模型的信息。</span><span class="sxs-lookup"><span data-stu-id="84797-252">Information from the **Set2** data model is used when you choose **Yes** for the **Selector** data source at runtime on the user dialog page.</span></span>

    ![ER 格式设计器页面，“映射”选项卡](./media/GER-JoinDS-FormatMappingReview.PNG)

9. <span data-ttu-id="84797-254">选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="84797-254">Select **Run**.</span></span>
10. <span data-ttu-id="84797-255">在对话框页面上，在 **使用 JOIN 数据源** 字段中选择 **否**。</span><span class="sxs-lookup"><span data-stu-id="84797-255">On the dialog page, select **No** in the **Use JOIN data source** field.</span></span>
11. <span data-ttu-id="84797-256">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="84797-256">Select **OK**.</span></span>
12. <span data-ttu-id="84797-257">查看生成的文件。</span><span class="sxs-lookup"><span data-stu-id="84797-257">Review generated file.</span></span>

    ![未使用 JOIN 数据源的电子报表参数生成文件](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a><span data-ttu-id="84797-259">分析 ER 格式执行跟踪</span><span class="sxs-lookup"><span data-stu-id="84797-259">Analyze ER format execution trace</span></span>

1. <span data-ttu-id="84797-260">在 Finance 或 RCS 的第一个会话中，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="84797-260">In the first session of Finance or RCS, select **Designer**.</span></span>
2. <span data-ttu-id="84797-261">选择 **性能跟踪**。</span><span class="sxs-lookup"><span data-stu-id="84797-261">Select **Performance trac** e.</span></span>
3. <span data-ttu-id="84797-262">在 **性能跟踪** 网格中，选择使用当前模型映射组件的 ER 格式的最新执行跟踪的最上面那条记录。</span><span class="sxs-lookup"><span data-stu-id="84797-262">In the **Performance trace** grid, select the top-most record of the latest execution trace of an ER format that used the current model mapping component.</span></span>
4. <span data-ttu-id="84797-263">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="84797-263">Select **OK**.</span></span>

    <span data-ttu-id="84797-264">执行统计信息会通知您有关应用程序表的重复调用：</span><span class="sxs-lookup"><span data-stu-id="84797-264">Execution statistics informs you about duplicated calls to application tables:</span></span>

    - <span data-ttu-id="84797-265">**ERSolutionTable** 被调用的次数与您在 **ERSolutionVersionTable** 表中的配置版本记录相同，而为提高性能，此类调用的次数可以适时减少。</span><span class="sxs-lookup"><span data-stu-id="84797-265">**ERSolutionTable** has been called as many times as you have configuration version records in the **ERSolutionVersionTable** table, while the number of such calls could be reduced in times for performance improvement.</span></span>
    - <span data-ttu-id="84797-266">对于 **ERSolutionVersionTable** 表中发现的每个配置版本记录，两次调用了 **ERVendorTable**，此类调用的次数也可以减少。</span><span class="sxs-lookup"><span data-stu-id="84797-266">**ERVendorTable** has been called twice for every configuration version record that was discovered in the **ERSolutionVersionTable** table, while the number of such calls could be reduced as well.</span></span>

    ![ER 模型映射设计器页面上的执行统计信息](./media/GER-JoinDS-Set1Run2.PNG)

5. <span data-ttu-id="84797-268">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="84797-268">Close the page.</span></span>

### <a name="execute-er-format"></a><span data-ttu-id="84797-269">执行 ER 格式</span><span class="sxs-lookup"><span data-stu-id="84797-269">Execute ER format</span></span>

1. <span data-ttu-id="84797-270">切换到包含 Finance 或 RCS 的第二个会话的 Web 浏览器选项卡。</span><span class="sxs-lookup"><span data-stu-id="84797-270">Switch to your web browser tab with the second session of Finance or RCS.</span></span>
2. <span data-ttu-id="84797-271">选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="84797-271">Select **Run**.</span></span>
3. <span data-ttu-id="84797-272">在对话框页面上，在 **使用 JOIN 数据源** 字段中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="84797-272">On the dialog page, select **Yes** in the **Use JOIN data source** field.</span></span>
4. <span data-ttu-id="84797-273">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="84797-273">Select **OK**.</span></span>
5. <span data-ttu-id="84797-274">查看生成的文件。</span><span class="sxs-lookup"><span data-stu-id="84797-274">Review generated file.</span></span>

    ![使用 JOIN 数据源的电子报表参数生成文件](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a><a name="analyze"></a><span data-ttu-id="84797-276">分析 ER 格式执行跟踪</span><span class="sxs-lookup"><span data-stu-id="84797-276">Analyze ER format execution trace</span></span>

1. <span data-ttu-id="84797-277">在 Finance 或 RCS 的第一个会话中，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="84797-277">In the first session of Finance or RCS, select **Designer**.</span></span>
2. <span data-ttu-id="84797-278">选择 **性能跟踪**。</span><span class="sxs-lookup"><span data-stu-id="84797-278">Select **Performance trace**.</span></span>
3. <span data-ttu-id="84797-279">在 **性能跟踪** 网格中，选择表示使用当前模型映射组件的 ER 格式的最新执行跟踪的最上面那条记录。</span><span class="sxs-lookup"><span data-stu-id="84797-279">In the **Performance trace** grid, select top-most record representing the latest execution trace of an ER format that used the current model mapping component.</span></span>
4. <span data-ttu-id="84797-280">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="84797-280">Select **OK**.</span></span>

    <span data-ttu-id="84797-281">统计信息会通知您以下内容：</span><span class="sxs-lookup"><span data-stu-id="84797-281">Statistics informs you about the following:</span></span>

    - <span data-ttu-id="84797-282">已调用一次应用程序数据库，以从 **ERVendorTable**、**ERSolutionTable** 和 **ERSolutionVersionTable** 表中获取记录来访问必填字段。</span><span class="sxs-lookup"><span data-stu-id="84797-282">Application database has been called once to get records from **ERVendorTable**, **ERSolutionTable**, and **ERSolutionVersionTable** tables to access required fields.</span></span>

    ![ER 模型映射设计器页面性能统计信息的详细信息](./media/GER-JoinDS-Set2Run2.PNG)

    - <span data-ttu-id="84797-284">已调用一次应用程序数据库，以使用在 **Details** 数据源中配置的联接来计算配置版本数。</span><span class="sxs-lookup"><span data-stu-id="84797-284">Application database has been called once to calculate the number of configuration versions by using joins that were configured in the **Details** data source.</span></span>

    ![显示应用程序数据库调用的 ER 模型映射设计器页面](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="limitations"></a><span data-ttu-id="84797-286">限制</span><span class="sxs-lookup"><span data-stu-id="84797-286">Limitations</span></span>

<span data-ttu-id="84797-287">从本主题的示例中可以看到，可以利用多个数据源构建 **JOIN** 数据源，前者描述了最终必须连接的记录的各个数据集。</span><span class="sxs-lookup"><span data-stu-id="84797-287">As you can see from the example in this topic, the **JOIN** data source can be built from several data sources that describe the individual datasets of the records that must eventually be joined.</span></span> <span data-ttu-id="84797-288">您可以使用内置的 ER [FILTER](er-functions-list-filter.md) 函数来配置这些数据源。</span><span class="sxs-lookup"><span data-stu-id="84797-288">You can configure those data sources by using the built-in ER [FILTER](er-functions-list-filter.md) function.</span></span> <span data-ttu-id="84797-289">当您配置数据源以使其在 **JOIN** 数据源之外被调用时，您可以将公司范围用作数据选择条件的一部分。</span><span class="sxs-lookup"><span data-stu-id="84797-289">When you configure the data source so that it's called beyond the **JOIN** data source, you can use company ranges as part of the condition for data selection.</span></span> <span data-ttu-id="84797-290">**JOIN** 数据源的初始实现不支持这种类型的数据源。</span><span class="sxs-lookup"><span data-stu-id="84797-290">The initial implementation of the **JOIN** data source doesn't support data sources of this type.</span></span> <span data-ttu-id="84797-291">例如，在 **JOIN** 数据源的执行范围内调用基于 [FILTER](er-functions-list-filter.md) 的数据源时，如果被调用的数据源包含公司范围，并将其作为数据选择条件的一部分，则会发生异常。</span><span class="sxs-lookup"><span data-stu-id="84797-291">For example, when you call a [FILTER](er-functions-list-filter.md)-based data source within the scope of execution of a **JOIN** data source, if the called data source contains company ranges as part of the condition for data selection, an exception occurs.</span></span>

<span data-ttu-id="84797-292">在 Microsoft Dynamics 365 Finance 版本 10.0.12（2020 年 8 月）中，可以将公司范围用作在基于 [FILTER](er-functions-list-filter.md) 的数据源中进行数据选择的部分条件，这些数据源在 **JOIN** 数据源的执行范围内被调用。</span><span class="sxs-lookup"><span data-stu-id="84797-292">In Microsoft Dynamics 365 Finance version 10.0.12 (August 2020), you can use company ranges as part of the condition for data selection in [FILTER](er-functions-list-filter.md)-based data sources that are called within the scope of execution of a **JOIN** data source.</span></span> <span data-ttu-id="84797-293">由于应用程序 [查询](../dev-ref/xpp-library-objects.md#query-object-model)生成器限制的缘故，仅对 **JOIN** 数据源的第一个数据源支持公司范围。</span><span class="sxs-lookup"><span data-stu-id="84797-293">Because of the limitations of the application [query](../dev-ref/xpp-library-objects.md#query-object-model) builder, the company ranges are supported only for the first data source of a **JOIN** data source.</span></span>

### <a name="example"></a><span data-ttu-id="84797-294">示例</span><span class="sxs-lookup"><span data-stu-id="84797-294">Example</span></span>

<span data-ttu-id="84797-295">例如，您必须对应用程序数据库进行单次调用，才能获取多个公司的外贸交易列表，以及这些交易中引用的库存项目的详细信息。</span><span class="sxs-lookup"><span data-stu-id="84797-295">For example, you must make a single call to the application database to get the list of foreign trade transactions of multiple companies and the details of the inventory item that is referred to in those transactions.</span></span>

<span data-ttu-id="84797-296">在这种情况下，您可以在 ER 模型映射中配置以下项目：</span><span class="sxs-lookup"><span data-stu-id="84797-296">In this case, you configure the following artifacts in your ER model mapping:</span></span>

- <span data-ttu-id="84797-297">表示 **Intrastat** 表的 **内部统计** 根数据源。</span><span class="sxs-lookup"><span data-stu-id="84797-297">**Intrastat** root data source that represents the **Intrastat** table.</span></span>
- <span data-ttu-id="84797-298">表示 **InventTable** 表的 **项目** 根数据源。</span><span class="sxs-lookup"><span data-stu-id="84797-298">**Items** root data source that represents the **InventTable** table.</span></span>
- <span data-ttu-id="84797-299">**公司** 根数据源，它返回必须在其中访问交易的公司（在此示例中为 **DEMF** 和 **GBSI**）列表。</span><span class="sxs-lookup"><span data-stu-id="84797-299">**Companies** root data source that returns the list of companies (**DEMF** and **GBSI** in this example) where transactions must be accessed.</span></span> <span data-ttu-id="84797-300">公司代码可从 **Companies.Code** 字段获得。</span><span class="sxs-lookup"><span data-stu-id="84797-300">The company code is available from the **Companies.Code** field.</span></span>
- <span data-ttu-id="84797-301">具有 `FILTER (Intrastat, VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code))` 表达式的 **X1** 根数据源。</span><span class="sxs-lookup"><span data-stu-id="84797-301">**X1** root data source that has the expression `FILTER (Intrastat, VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code))`.</span></span> <span data-ttu-id="84797-302">作为数据选择条件的一部分，此表达式包含公司范围 `VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code)` 的定义。</span><span class="sxs-lookup"><span data-stu-id="84797-302">As part of the condition for data selection, this expression contains the definition of company ranges `VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code)`.</span></span>
- <span data-ttu-id="84797-303">作为 **X1** 数据源的嵌套项的 **X2** 数据源。</span><span class="sxs-lookup"><span data-stu-id="84797-303">**X2** data source as a nested item of the **X1** data source.</span></span> <span data-ttu-id="84797-304">它包括 `FILTER (Items, Items.ItemId = X1.ItemId)` 表达式。</span><span class="sxs-lookup"><span data-stu-id="84797-304">It includes the expression `FILTER (Items, Items.ItemId = X1.ItemId)`.</span></span>

<span data-ttu-id="84797-305">最后，您可以配置 **JOIN** 数据源，其中 **X1** 是第一个数据源，**X2** 是第二个数据源。</span><span class="sxs-lookup"><span data-stu-id="84797-305">Finally, you can configure a **JOIN** data source where **X1** is the first data source and **X2** is the second data source.</span></span> <span data-ttu-id="84797-306">您可以将 **查询** 指定为 **执行** 选项，以强制 ER 作为直接 SQL 调用在数据库级别运行此数据源。</span><span class="sxs-lookup"><span data-stu-id="84797-306">You can specify **Query** as the **Execute** option to force ER to run this data source on the database level as a direct SQL call.</span></span>

<span data-ttu-id="84797-307">在[跟踪](trace-execution-er-troubleshoot-perf.md) ER 执行情况期间运行配置的数据源时，以下语句在 ER 模型映射设计器中显示为 ER 性能跟踪的一部分。</span><span class="sxs-lookup"><span data-stu-id="84797-307">When the configured data source is run while the ER execution is [traced](trace-execution-er-troubleshoot-perf.md), the following statement is shown in the ER model mapping designer as part of the ER performance trace.</span></span>

`SELECT ... FROM INTRASTAT T1 CROSS JOIN INVENTTABLE T2 WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF',N'GBSI') )) AND ((T2.PARTITION=?) AND (T2.ITEMID=T1.ITEMID AND (T2.DATAAREAID = T1.DATAAREAID) AND (T2.PARTITION = T1.PARTITION))) ORDER BY T1.DISPATCHID,T1.SEQNUM`

> [!NOTE]
> <span data-ttu-id="84797-308">如果运行已配置的 **JOIN** 数据源，以便该数据源包含数据选择条件，并且这些数据选择条件具有已执行 **JOIN** 数据源的其他数据源的公司范围，则会出现错误。</span><span class="sxs-lookup"><span data-stu-id="84797-308">An error occurs if you run a **JOIN** data source that has been configured so that it contains data selection conditions that have company ranges for additional data sources of the executed **JOIN** data source.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="84797-309">其他资源</span><span class="sxs-lookup"><span data-stu-id="84797-309">Additional resources</span></span>

[<span data-ttu-id="84797-310">电子报告中的配方设计器</span><span class="sxs-lookup"><span data-stu-id="84797-310">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="84797-311">跟踪 ER 格式的执行情况以解决性能问题</span><span class="sxs-lookup"><span data-stu-id="84797-311">Trace execution of ER format to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

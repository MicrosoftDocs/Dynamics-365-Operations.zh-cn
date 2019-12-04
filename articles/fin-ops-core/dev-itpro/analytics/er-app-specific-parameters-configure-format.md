---
title: 配置 ER 格式以使用每个法人指定的参数
description: 本主题说明如何配置电子报告 (ER) 格式以使用每个法人指定的参数。
author: NickSelin
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: d32da76ee46ff5293ae8fefb16d251564b6be21a
ms.sourcegitcommit: d6196d83c7b9166ddb4fe43a91e6bd0ad9da2099
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2019
ms.locfileid: "2694238"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a><span data-ttu-id="1c533-103">配置 ER 格式以使用每个法人指定的参数</span><span class="sxs-lookup"><span data-stu-id="1c533-103">Configure ER formats to use parameters that are specified per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="1c533-104">概览</span><span class="sxs-lookup"><span data-stu-id="1c533-104">Overview</span></span>

<span data-ttu-id="1c533-105">在您将要设计的许多电子报告 (ER) 格式中，您必须使用一组特定于您实例的每个法人的值（例如，用于筛选税收交易记录的一组税码）来筛选数据。</span><span class="sxs-lookup"><span data-stu-id="1c533-105">In many of the Electronic reporting (ER) formats that you will design, you must filter data by using a set of values that are specific to each legal entity of your instance (for example, a set of tax codes to filter tax transactions).</span></span> <span data-ttu-id="1c533-106">当前，以 ER 格式配置这种类型的筛选时，在 ER 格式的表达式中使用依赖于法人的值（例如，税码）来指定数据筛选规则。</span><span class="sxs-lookup"><span data-stu-id="1c533-106">Currently, when filtering of this type is configured in an ER format, values that are dependent on the legal entity (for example, tax codes) are used in expressions of the ER format to specify data filtering rules.</span></span> <span data-ttu-id="1c533-107">因此，将 ER 格式设为特定于法人，要生成所需的报表，必须为必须运行 ER 格式的每个法人创建原始 ER 格式的派生副本。</span><span class="sxs-lookup"><span data-stu-id="1c533-107">Therefore, the ER format is made legal entity–specific, and to generate the required reports, you must create derived copies of the original ER format for each legal entity where you have to run the ER format.</span></span> <span data-ttu-id="1c533-108">必须对每种派生的 ER 格式进行编辑，以将特定于法人的值引入其中，每当原始（基本）版本更新，从测试环境中导出并在必须部署用于生产用途时导入到生产环境中等情况下，都将重定基本值。</span><span class="sxs-lookup"><span data-stu-id="1c533-108">Each derived ER format must be edited to bring legal entity–specific values into it, rebased whenever the original (base) version has been updated, exported from a test environment and imported into a production environment when it must be deployed for production use, and so on.</span></span> <span data-ttu-id="1c533-109">因此，出于以下几个原因，此类已配置的 ER 解决方案的维护非常复杂且耗时：</span><span class="sxs-lookup"><span data-stu-id="1c533-109">Therefore, maintenance of this type of configured ER solution is quite complex and time-consuming for several reasons:</span></span>

-   <span data-ttu-id="1c533-110">法人越多，必须维护的 ER 格式配置就越多。</span><span class="sxs-lookup"><span data-stu-id="1c533-110">The more legal entities there are, the more ER format configurations must be maintained.</span></span>
-   <span data-ttu-id="1c533-111">维护 ER 配置需要业务用户具有 ER 知识。</span><span class="sxs-lookup"><span data-stu-id="1c533-111">Maintenance of ER configurations requires that business users have ER knowledge.</span></span>

<span data-ttu-id="1c533-112">ER 应用程序特定的参数功能使高级用户可以以 ER 格式配置数据筛选，使其基于一组抽象规则。</span><span class="sxs-lookup"><span data-stu-id="1c533-112">The ER application-specific parameters feature lets power users configure data filtering in an ER format so that it's based on a set of abstract rules.</span></span> <span data-ttu-id="1c533-113">可以将这组规则配置为可以使用 ER 格式的数据源。</span><span class="sxs-lookup"><span data-stu-id="1c533-113">This set of rules can be configured to use the data sources that are available in an ER format.</span></span> <span data-ttu-id="1c533-114">然后，业务用户可以使用基于相应 ER 格式的设置，以及将由 ER 格式的数据源访问的当前法人数据自动生成的用户界面 (UI)，来指定 ER 框架之外的实际规则。</span><span class="sxs-lookup"><span data-stu-id="1c533-114">Business users can then specify real rules beyond the ER framework by using the user interface (UI) that is automatically generated based on the settings of the corresponding ER format and the current legal entity data that will be accessed by the ER format's data sources.</span></span> <span data-ttu-id="1c533-115">可以从 Dynamics 365 Finance (Finance) 实例的当前法人导出为 ER 格式指定的规则集。</span><span class="sxs-lookup"><span data-stu-id="1c533-115">The set of rules that is specified for an ER format can be exported from the current legal entity of the Dynamics 365 Finance (Finance) instance.</span></span> <span data-ttu-id="1c533-116">然后可以将其导入与同一 ER 格式的一组规则相同的 Finance 实例或不同实例的另一个法人。</span><span class="sxs-lookup"><span data-stu-id="1c533-116">It can then be imported into another legal entity of either the same Finance instance or a different instance as a set of rules for the same ER format.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1c533-117">先决条件</span><span class="sxs-lookup"><span data-stu-id="1c533-117">Prerequisites</span></span>

<span data-ttu-id="1c533-118">要完成本主题中的示例，您必须有权访问为与以下角色之一的 Finance 相同的租户预配的 Regulatory Configuration Services (RCS) 实例：</span><span class="sxs-lookup"><span data-stu-id="1c533-118">To complete the examples in this topic, you must have access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>

- <span data-ttu-id="1c533-119">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="1c533-119">Electronic reporting developer</span></span>
- <span data-ttu-id="1c533-120">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="1c533-120">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="1c533-121">系统管理员</span><span class="sxs-lookup"><span data-stu-id="1c533-121">System administrator</span></span>

<span data-ttu-id="1c533-122">我们建议您完成[支持对计算字段类型的 ER 数据源的参数化调用](er-calculated-field-type.md)主题中的步骤。</span><span class="sxs-lookup"><span data-stu-id="1c533-122">We recommend that you complete the steps in the [Support parameterized calls of ER data sources of CALCULATED FIELD type](er-calculated-field-type.md) topic.</span></span> <span data-ttu-id="1c533-123">如果您已经完成了这些步骤，则可以跳过后面的**将 ER 配置导入 RCS** 部分中的步骤。</span><span class="sxs-lookup"><span data-stu-id="1c533-123">If you've already completed those steps, you can skip the steps in the **Import ER configurations into RCS** section that follows.</span></span>

## <a name="import-er-configurations-into-rcs"></a><span data-ttu-id="1c533-124">将 ER 配置导入 RCS</span><span class="sxs-lookup"><span data-stu-id="1c533-124">Import ER configurations into RCS</span></span>

<span data-ttu-id="1c533-125">从 [Microsoft 下载中心](https://go.microsoft.com/fwlink/?linkid=851448)，下载**支持对计算字段类型的 ER 数据源的参数化调用** zip 文件。</span><span class="sxs-lookup"><span data-stu-id="1c533-125">From [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=851448), download the **Support parameterized calls of ER data sources of CALCULATED FIELD type** zip file.</span></span> <span data-ttu-id="1c533-126">此 zip 文件包含以下 ER 配置，必须将其提取并存储在本地。</span><span class="sxs-lookup"><span data-stu-id="1c533-126">This zip file contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="1c533-127">**内容描述**</span><span class="sxs-lookup"><span data-stu-id="1c533-127">**Content description**</span></span>                        | <span data-ttu-id="1c533-128">**文件名**</span><span class="sxs-lookup"><span data-stu-id="1c533-128">**File name**</span></span>                                        |
|------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1c533-129">示例 **ER 数据模型**配置文件</span><span class="sxs-lookup"><span data-stu-id="1c533-129">Sample **ER data model** configuration file</span></span>    | <span data-ttu-id="1c533-130">用于了解参数化调用的模型.版本.1.xml</span><span class="sxs-lookup"><span data-stu-id="1c533-130">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="1c533-131">示例 **ER 元数据**配置文件</span><span class="sxs-lookup"><span data-stu-id="1c533-131">Sample **ER metadata** configuration file</span></span>      | <span data-ttu-id="1c533-132">用于了解参数化调用的元数据.版本.1.xml</span><span class="sxs-lookup"><span data-stu-id="1c533-132">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="1c533-133">示例 **ER 模型映射**配置文件</span><span class="sxs-lookup"><span data-stu-id="1c533-133">Sample **ER model mapping** configuration file</span></span> | <span data-ttu-id="1c533-134">用于了解参数化调用的映射.版本.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="1c533-134">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="1c533-135">示例 **ER 格式**配置</span><span class="sxs-lookup"><span data-stu-id="1c533-135">Sample **ER format** configuration</span></span>             | <span data-ttu-id="1c533-136">用于了解参数化调用的格式.版本.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="1c533-136">Format to learn parameterized calls.version.1.1.xml</span></span>  |

<span data-ttu-id="1c533-137">接下来，登录到您的 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="1c533-137">Next, sign in to your RCS instance.</span></span>

<span data-ttu-id="1c533-138">在此示例中，您将为 Litware, Inc 示例公司创建一个配置。</span><span class="sxs-lookup"><span data-stu-id="1c533-138">In this example, you will create a configuration for the Litware, Inc sample company.</span></span> <span data-ttu-id="1c533-139">在完成此过程之前，必须完成 RCS 中[创建一个配置提供程序，并标记其为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)主题中的步骤。</span><span class="sxs-lookup"><span data-stu-id="1c533-139">Before you can complete this procedure, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic in RCS.</span></span>

1.  <span data-ttu-id="1c533-140">在默认仪表板中，选择**电子申报**。</span><span class="sxs-lookup"><span data-stu-id="1c533-140">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="1c533-141">选择**申报配置**。</span><span class="sxs-lookup"><span data-stu-id="1c533-141">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="1c533-142">按照以下顺序将您先前下载的 ER 配置导入到 RCS 中：数据模型、元数据、模型映射、格式。</span><span class="sxs-lookup"><span data-stu-id="1c533-142">Import the ER configurations that you downloaded earlier into RCS, in the following order: data model, metadata, model mapping, and format.</span></span> <span data-ttu-id="1c533-143">对于每个 ER 配置，请按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="1c533-143">For each ER configuration, follow these steps:</span></span>

    1.  <span data-ttu-id="1c533-144">选择**交换**。</span><span class="sxs-lookup"><span data-stu-id="1c533-144">Select **Exchange**.</span></span>
    2.  <span data-ttu-id="1c533-145">选择**从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="1c533-145">Select **Load from XML file**.</span></span>
    3.  <span data-ttu-id="1c533-146">选择**浏览**以 XML 格式选择所需 ER 配置的文件。</span><span class="sxs-lookup"><span data-stu-id="1c533-146">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    4.  <span data-ttu-id="1c533-147">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="1c533-147">Select **OK**.</span></span>

## <a name="review-the-er-solution-that-is-provided"></a><span data-ttu-id="1c533-148">查看提供的 ER 解决方案</span><span class="sxs-lookup"><span data-stu-id="1c533-148">Review the ER solution that is provided</span></span>

1.  <span data-ttu-id="1c533-149">在配置树中，展开**用于了解参数化调用的模型**项的目录。</span><span class="sxs-lookup"><span data-stu-id="1c533-149">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="1c533-150">选择**用于了解参数化调用的格式**项。</span><span class="sxs-lookup"><span data-stu-id="1c533-150">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="1c533-151">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="1c533-151">Select **Designer**.</span></span>
4.  <span data-ttu-id="1c533-152">选择**展开/折叠**。</span><span class="sxs-lookup"><span data-stu-id="1c533-152">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="1c533-153">**用于了解参数化调用的格式** ER 格式旨在生成 XML 格式的税报表，其显示多个征税级别（正常、减税和免税）。</span><span class="sxs-lookup"><span data-stu-id="1c533-153">The **Format to learn parameterized calls** ER format is designed to generate a tax statement in XML format that presents several levels of taxation (regular, reduced, and none).</span></span> <span data-ttu-id="1c533-154">每个级别都有不同数量的详细信息。</span><span class="sxs-lookup"><span data-stu-id="1c533-154">Each level has a different number of details.</span></span>

    ![ER Operation 设计器页](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  <span data-ttu-id="1c533-156">在**映射**选项卡上，展开**模型**、**数据**和**汇总**项目。</span><span class="sxs-lookup"><span data-stu-id="1c533-156">On the **Mapping** tab, expand the **Model**, **Data**, and **Summary** items.</span></span>

    <span data-ttu-id="1c533-157">**Model.Data.Summary** 数据源返回税收交易记录的列表。</span><span class="sxs-lookup"><span data-stu-id="1c533-157">The **Model.Data.Summary** data source returns the list of tax transactions.</span></span> <span data-ttu-id="1c533-158">这些交易记录按税码进行汇总。</span><span class="sxs-lookup"><span data-stu-id="1c533-158">These transactions are summarized by tax code.</span></span> <span data-ttu-id="1c533-159">对于此数据源，已配置 **Model.Data.Summary.Level** 计算字段以返回每个汇总记录的征税级别的代码。</span><span class="sxs-lookup"><span data-stu-id="1c533-159">For this data source, the **Model.Data.Summary.Level** calculated field has been configured to return the code for the taxation level of each summarized record.</span></span> <span data-ttu-id="1c533-160">对于在运行时可以从 **Model.Data.Summary** 数据源中检索到的任何税码，计算字段将作为文本值返回征税级别代码（**正常**、**减税**、**免税**或**其他**）。</span><span class="sxs-lookup"><span data-stu-id="1c533-160">For any tax code that can be retrieved from the **Model.Data.Summary** data source at runtime, the calculated field returns the taxation level code (**Regular**, **Reduced**, **None**, or **Other**) as a text value.</span></span> <span data-ttu-id="1c533-161">**Model.Data.Summary.Level** 计算字段用于筛选 **Model.Data.Summary** 数据源的记录，并通过使用 **Model.Data2.Level1**、**Model.Data2.Level2** 和 **Model.Data2.Level3** 字段来在表示征税级别的每个 XML 元素中输入筛选后的数据。</span><span class="sxs-lookup"><span data-stu-id="1c533-161">The **Model.Data.Summary.Level** calculated field is used to filter records of the **Model.Data.Summary** data source and enter the filtered data in each XML element that represents a taxation level by using the **Model.Data2.Level1**, **Model.Data2.Level2**, and **Model.Data2.Level3** fields.</span></span>

    ![ER Operation 设计器页](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    <span data-ttu-id="1c533-163">已配置 **Model.Data.Summary.Level** 计算字段，使其包含 ER 表达式。</span><span class="sxs-lookup"><span data-stu-id="1c533-163">The **Model.Data.Summary.Level** calculated field has been configured so that it contains an ER expression.</span></span> <span data-ttu-id="1c533-164">请注意，税码（**VAT19**、**InVAT19**、**VAT7**、**InVAT7**、**THIRD** 和 **InVAT0**）被硬编码到此配置中。</span><span class="sxs-lookup"><span data-stu-id="1c533-164">Note that tax codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD**, and **InVAT0**) are hardcoded into this configuration.</span></span> <span data-ttu-id="1c533-165">因此，此 ER 格式取决于配置了这些税码的法人。</span><span class="sxs-lookup"><span data-stu-id="1c533-165">Therefore, this ER format is dependent on the legal entity where these tax codes were configured.</span></span>

    ![ER Operation 设计器页](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    <span data-ttu-id="1c533-167">要为每个法人支持一组不同的税码，您必须执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="1c533-167">To support a different set of tax codes for each legal entity, you must follow these steps:</span></span>

    - <span data-ttu-id="1c533-168">为每个法人创建 ER 格式的派生版本。</span><span class="sxs-lookup"><span data-stu-id="1c533-168">Create a derived version of the ER format for each legal entity.</span></span>
    - <span data-ttu-id="1c533-169">根据法人设置，在 **Model.Data.Summary.Level** 计算字段中更新税码。</span><span class="sxs-lookup"><span data-stu-id="1c533-169">Update the tax codes in the **Model.Data.Summary.Level** calculated field, based on the legal entity setting.</span></span>

6.  <span data-ttu-id="1c533-170">关闭**格式设计器**页。</span><span class="sxs-lookup"><span data-stu-id="1c533-170">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="1c533-171">创建派生格式</span><span class="sxs-lookup"><span data-stu-id="1c533-171">Create a derived format</span></span>

<span data-ttu-id="1c533-172">接下来，您将使用 ER 应用程序特定的参数功能，以单个 ER 格式为每个法人支持一组不同的税码。</span><span class="sxs-lookup"><span data-stu-id="1c533-172">Next, you will use the ER application-specific parameters feature to support a different set of tax codes for each legal entity in a single ER format.</span></span>

1.  <span data-ttu-id="1c533-173">在配置树中，展开**用于了解参数化调用的模型**项的目录。</span><span class="sxs-lookup"><span data-stu-id="1c533-173">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="1c533-174">选择**用于了解参数化调用的格式**项。</span><span class="sxs-lookup"><span data-stu-id="1c533-174">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="1c533-175">选择**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="1c533-175">Select **Create configuration**.</span></span>
4.  <span data-ttu-id="1c533-176">选择**从以下名称派生: 用于了解参数化调用的格式，Microsoft** 选项。</span><span class="sxs-lookup"><span data-stu-id="1c533-176">Select the **Derive from Name: Format to learn parameterized calls, Microsoft** option.</span></span>
5.  <span data-ttu-id="1c533-177">在**名称**字段中，输入**用于了解如何查找 LE 数据的格式**。</span><span class="sxs-lookup"><span data-stu-id="1c533-177">In the **Name** field, enter **Format to learn how to lookup LE data**.</span></span>
6.  <span data-ttu-id="1c533-178">选择**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="1c533-178">Select **Create configuration**.</span></span>

## <a name="configure-a-derived-format"></a><span data-ttu-id="1c533-179">配置派生格式</span><span class="sxs-lookup"><span data-stu-id="1c533-179">Configure a derived format</span></span>

### <a name="add-a-format-enumeration"></a><span data-ttu-id="1c533-180">添加格式枚举</span><span class="sxs-lookup"><span data-stu-id="1c533-180">Add a format enumeration</span></span>

<span data-ttu-id="1c533-181">接下来，您将添加一个新的 ER 格式枚举。</span><span class="sxs-lookup"><span data-stu-id="1c533-181">Next, you will add a new ER format enumeration.</span></span> <span data-ttu-id="1c533-182">此格式枚举的值将提供给业务用户，业务用户将为 ER 格式中使用的各个征税级别指定与法人相关的税码集。</span><span class="sxs-lookup"><span data-stu-id="1c533-182">The values of this format enumeration will be presented to business users, who will specify legal entity–dependent sets of tax codes for the various taxation levels that are used in the ER format.</span></span>

1.  <span data-ttu-id="1c533-183">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="1c533-183">Select **Designer**.</span></span>
2.  <span data-ttu-id="1c533-184">选择**格式枚举**。</span><span class="sxs-lookup"><span data-stu-id="1c533-184">Select **Format enumerations**.</span></span>
3.  <span data-ttu-id="1c533-185">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="1c533-185">Select **Add**.</span></span>
4.  <span data-ttu-id="1c533-186">在**名称**字段中，输入**征税级别列表**。</span><span class="sxs-lookup"><span data-stu-id="1c533-186">In the **Name** field, enter **List of taxation levels**.</span></span>
5.  <span data-ttu-id="1c533-187">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="1c533-187">Select **Save**.</span></span>
6.  <span data-ttu-id="1c533-188">在**格式枚举值**选项卡上，选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="1c533-188">On the **Format enumeration values** tab, select **Add**.</span></span>
7.  <span data-ttu-id="1c533-189">在**名称**字段中，输入**正常税收**。</span><span class="sxs-lookup"><span data-stu-id="1c533-189">In the **Name** field, enter **Regular taxation**.</span></span>
8.  <span data-ttu-id="1c533-190">再次选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="1c533-190">Select **Add** again.</span></span>
9.  <span data-ttu-id="1c533-191">在**名称**字段中，输入**减税**。</span><span class="sxs-lookup"><span data-stu-id="1c533-191">In the **Name** field, enter **Reduced taxation**.</span></span>
10. <span data-ttu-id="1c533-192">再次选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="1c533-192">Select **Add** again.</span></span>
11. <span data-ttu-id="1c533-193">在**名称**字段中，输入**免税**。</span><span class="sxs-lookup"><span data-stu-id="1c533-193">In the **Name** field, enter **No taxation**.</span></span>
12. <span data-ttu-id="1c533-194">再次选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="1c533-194">Select **Add** again.</span></span>
13. <span data-ttu-id="1c533-195">在**名称**字段中，输入**其他**。</span><span class="sxs-lookup"><span data-stu-id="1c533-195">In the **Name** field, enter **Other**.</span></span>

    ![ER Operation 设计器页](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    <span data-ttu-id="1c533-197">由于业务用户可能使用不同的语言来指定与法人相关的税码集，因此我们建议您将此枚举的值翻译为在 Finance 中为那些用户配置为首选语言的语言。</span><span class="sxs-lookup"><span data-stu-id="1c533-197">Because the business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the values of this enumeration into the languages that are configured as the preferred languages for those users in Finance.</span></span>

14. <span data-ttu-id="1c533-198">选择**免税**记录。</span><span class="sxs-lookup"><span data-stu-id="1c533-198">Select the **No taxation** record.</span></span>
15. <span data-ttu-id="1c533-199">单击**标签**字段。</span><span class="sxs-lookup"><span data-stu-id="1c533-199">Click in the **Label** field.</span></span>
16. <span data-ttu-id="1c533-200">选择**翻译**。</span><span class="sxs-lookup"><span data-stu-id="1c533-200">Select **Translate**.</span></span>
17. <span data-ttu-id="1c533-201">在**文本翻译**窗格中的**标签 ID** 字段中，输入 **LBL_LEVELENUM_NO**。</span><span class="sxs-lookup"><span data-stu-id="1c533-201">In the **Text translation** pane, in the **Label Id** field, enter **LBL_LEVELENUM_NO**.</span></span>
18. <span data-ttu-id="1c533-202">在**语言为默认语言的文本**字段中，输入**免税**。</span><span class="sxs-lookup"><span data-stu-id="1c533-202">In the **Text in default language** field, enter **No taxation**.</span></span>
19. <span data-ttu-id="1c533-203">在**语言**字段中，选择 **DE**。</span><span class="sxs-lookup"><span data-stu-id="1c533-203">In the **Language** field, select **DE**.</span></span>
20. <span data-ttu-id="1c533-204">在**已翻译的文本**字段中，输入 **keine Besteuerung**。</span><span class="sxs-lookup"><span data-stu-id="1c533-204">In the **Translated text** field, enter **keine Besteuerung**.</span></span>
21. <span data-ttu-id="1c533-205">选择**翻译**。</span><span class="sxs-lookup"><span data-stu-id="1c533-205">Select **Translate**.</span></span>

    ![ER Operation 设计器页](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. <span data-ttu-id="1c533-207">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="1c533-207">Select **Save**.</span></span>
23. <span data-ttu-id="1c533-208">关闭**格式枚举**页。</span><span class="sxs-lookup"><span data-stu-id="1c533-208">Close the **Format enumerations** page.</span></span>

### <a name="add-a-new-lookup-data-source"></a><span data-ttu-id="1c533-209">添加新的查找数据源</span><span class="sxs-lookup"><span data-stu-id="1c533-209">Add a new lookup data source</span></span>

<span data-ttu-id="1c533-210">接下来，您将添加一个新的数据源，以指定业务用户将如何指定与法人相关的规则，以为每个汇总的交易记录识别正确的征税级别。</span><span class="sxs-lookup"><span data-stu-id="1c533-210">Next, you will add a new data source to specify how business users will specify legal entity–dependent rules to recognize the correct taxation level for each summarized transaction record.</span></span>

1.  <span data-ttu-id="1c533-211">在**映射**选项卡上，选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="1c533-211">On the **Mapping** tab, select **Add**.</span></span>
2.  <span data-ttu-id="1c533-212">选择**格式枚举\查找**。</span><span class="sxs-lookup"><span data-stu-id="1c533-212">Select **Format enumeration\Lookup**.</span></span>

    <span data-ttu-id="1c533-213">您刚刚确定，业务用户为征税级别识别指定的每个规则将返回 ER 格式枚举的值。</span><span class="sxs-lookup"><span data-stu-id="1c533-213">You just identified that each rule that business users specify for taxation level recognition will return a value of an ER format enumeration.</span></span> <span data-ttu-id="1c533-214">请注意，除了**格式枚举**块外，还可以在**数据模型**和 **Dynamics 365 for Operations** 块下访问**查找**数据源类型。</span><span class="sxs-lookup"><span data-stu-id="1c533-214">Notice that the **Lookup** data source type can be accessed under the **Data model** and **Dynamics 365 for Operations** blocks in addition to the **Format enumeration** block.</span></span> <span data-ttu-id="1c533-215">因此，ER 数据模型枚举和应用程序枚举可用于指定为该类型的数据源返回的值的类型。</span><span class="sxs-lookup"><span data-stu-id="1c533-215">Therefore, ER data model enumerations and application enumerations can be used to specify the type of values that is are returned for data sources of that type.</span></span>
    
3.  <span data-ttu-id="1c533-216">在**名称**字段中，输入**选择器**。</span><span class="sxs-lookup"><span data-stu-id="1c533-216">In the **Name** field, enter **Selector**.</span></span>
4.  <span data-ttu-id="1c533-217">在**格式枚举**字段中，选择**征税级别列表**。</span><span class="sxs-lookup"><span data-stu-id="1c533-217">In the **Format enumeration** field, select **List of taxation levels**.</span></span>

    <span data-ttu-id="1c533-218">您刚刚指定，对于此数据源中指定的每个规则，业务用户必须选择**征税级别列表**格式枚举的值之一作为返回值。</span><span class="sxs-lookup"><span data-stu-id="1c533-218">You just specified that, for each rule that is specified in this data source, a business user must select one of the values of the **List of taxation levels** format enumeration as a returned value.</span></span>
    
5.  <span data-ttu-id="1c533-219">选择**编辑查找**。</span><span class="sxs-lookup"><span data-stu-id="1c533-219">Select **Edit lookup**.</span></span>
6.  <span data-ttu-id="1c533-220">选择**列**。</span><span class="sxs-lookup"><span data-stu-id="1c533-220">Select **Columns**.</span></span>
7.  <span data-ttu-id="1c533-221">展开**模型**项。</span><span class="sxs-lookup"><span data-stu-id="1c533-221">Expand the **Model** item.</span></span>
8.  <span data-ttu-id="1c533-222">展开**数据**项。</span><span class="sxs-lookup"><span data-stu-id="1c533-222">Expand the **Data** item.</span></span>
9.  <span data-ttu-id="1c533-223">展开**税务**项。</span><span class="sxs-lookup"><span data-stu-id="1c533-223">Expand the **Tax** item.</span></span>
10. <span data-ttu-id="1c533-224">选择 **Model.Data.Tax.Code** 项。</span><span class="sxs-lookup"><span data-stu-id="1c533-224">Select the **Model.Data.Tax.Code** item.</span></span>
11. <span data-ttu-id="1c533-225">选择**添加**按钮（向右箭头）。</span><span class="sxs-lookup"><span data-stu-id="1c533-225">Select the **Add** button (the right arrow).</span></span>

    ![ER Operation 设计器页](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    <span data-ttu-id="1c533-227">您刚才指定了，对于此数据源中指定的用于征税级别识别的每个规则，业务用户必须选择一个税码作为条件。</span><span class="sxs-lookup"><span data-stu-id="1c533-227">You just specified that, for each rule that is specified in this data source for taxation level recognition, a business user must select one of the tax codes as a condition.</span></span> <span data-ttu-id="1c533-228">业务用户可以选择的税码列表将由 **Model.Data.Tax** 数据源返回。</span><span class="sxs-lookup"><span data-stu-id="1c533-228">The list of tax codes that the business user can select will be returned by the **Model.Data.Tax** data source.</span></span> <span data-ttu-id="1c533-229">因为此数据源包含**名称**字段，所以将在呈现给业务用户的查找中为每个税码值显示税码的名称。</span><span class="sxs-lookup"><span data-stu-id="1c533-229">Because this data source contains the **Name** field, the name of the tax code will be shown for each tax code value in the lookup that is presented to the business user.</span></span>
    
12. <span data-ttu-id="1c533-230">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="1c533-230">Select **OK**.</span></span>

    ![ER Operation 设计器页](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    <span data-ttu-id="1c533-232">业务用户可以添加多个规则作为此数据源的记录。</span><span class="sxs-lookup"><span data-stu-id="1c533-232">Business users can add multiple rules as records of this data source.</span></span> <span data-ttu-id="1c533-233">每个记录将由一个行代码编号。</span><span class="sxs-lookup"><span data-stu-id="1c533-233">Each record will be numbered by a line code.</span></span> <span data-ttu-id="1c533-234">规则将按照行号增加的顺序进行评估。</span><span class="sxs-lookup"><span data-stu-id="1c533-234">Rules will be evaluated in order of increasing line number.</span></span>

    <span data-ttu-id="1c533-235">因为您选择了**税码**字段作为此查找数据源中规则的条件，并且由于**税码**被设置为**字符串**数据类型的字段，所以将在运行时对每个规则进行评估，方法是将传递给数据源的税码与数据源的记录中定义的税码进行比较。</span><span class="sxs-lookup"><span data-stu-id="1c533-235">Because you selected the **Tax code** field as a condition for rules in this lookup data source, and because **Tax code** is set up as a field of the **String** data type, each rule will be evaluated at runtime by comparing the tax code that is passed to the data source with the tax code that is defined in this record of the data source.</span></span>

    <span data-ttu-id="1c533-236">找到满足配置条件的规则时，此数据源将返回在**查找结果**字段中定义的规则的查找值。</span><span class="sxs-lookup"><span data-stu-id="1c533-236">When a rule that satisfies the configured condition is found, this data source returns the lookup value of the rule that is defined in the **Lookup result** field.</span></span> <span data-ttu-id="1c533-237">如果未找到任何规则，则会引发异常以通知用户当前数据源无法返回正确的值。</span><span class="sxs-lookup"><span data-stu-id="1c533-237">If no rule is found, an exception is thrown to notify the user that the current data source can't return a correct value.</span></span>

13. <span data-ttu-id="1c533-238">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="1c533-238">Select **Save**.</span></span>
14. <span data-ttu-id="1c533-239">关闭**查找设计器**页。</span><span class="sxs-lookup"><span data-stu-id="1c533-239">Close the **Lookup designer** page.</span></span>
15. <span data-ttu-id="1c533-240">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="1c533-240">Select **OK**.</span></span>

    <span data-ttu-id="1c533-241">请注意，您添加了一个新的数据源，该数据源将返回征税级别作为任何税码的**征税级别列表**格式枚举的值，该税码将作为**字符串**数据类型的**代码**参数的参数传递给数据源。</span><span class="sxs-lookup"><span data-stu-id="1c533-241">Notice that you added a new data source that will return the taxation level as the value of the **List of taxation levels** format enumeration for any tax code that is passed to the data source as the argument of the **Code** parameter of the **String** data type.</span></span>
    
    ![ER Operation 设计器页](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    <span data-ttu-id="1c533-243">请注意，对配置的规则的评估取决于为定义这些规则的条件而选择的字段的数据类型。</span><span class="sxs-lookup"><span data-stu-id="1c533-243">Note that the evaluation of configured rules depends on the data type of the fields that have been selected to define conditions of those rules.</span></span> <span data-ttu-id="1c533-244">当您选择一个配置为**数字**或**日期**数据类型的字段的字段时，条件将不同于先前针对**字符串**数据类型描述的条件。</span><span class="sxs-lookup"><span data-stu-id="1c533-244">When you select a field that is configured as a field of either the **Numeric** or **Date** data type, the criteria will differ from the criteria that were described earlier for the **String** data type.</span></span> <span data-ttu-id="1c533-245">对于**数字**和**日期**字段，必须将规则指定为值的范围。</span><span class="sxs-lookup"><span data-stu-id="1c533-245">For **Numeric** and **Date** fields, the rule must be specified as a range of values.</span></span> <span data-ttu-id="1c533-246">当传递到数据源的值在配置的范围内时，将认为规则的条件已满足。</span><span class="sxs-lookup"><span data-stu-id="1c533-246">The condition of the rule will then be considered satisfied when a value that is passed to the data source is in the configured range.</span></span>
    
    <span data-ttu-id="1c533-247">下图显示了此类设置的示例。</span><span class="sxs-lookup"><span data-stu-id="1c533-247">The following illustration shows an example of this type of setup.</span></span> <span data-ttu-id="1c533-248">除了**字符串**数据类型的 **Model.Data.Tax.Code** 字段外，**实数**数据类型的 **Model.Tax.Summary.Base** 字段用于指定查找数据源的条件。</span><span class="sxs-lookup"><span data-stu-id="1c533-248">In addition to the **Model.Data.Tax.Code** field of the **String** data type, the **Model.Tax.Summary.Base** field of the **Real** data type is used to specify conditions for a lookup data source.</span></span>
    
    ![ER Operation 设计器页](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    <span data-ttu-id="1c533-250">因为为此查询数据源选择了 **Model.Data.Tax.Code** 和 **Model.Tax.Summary.Base** 字段，所以将以以下方式配置此数据源的每个规则：</span><span class="sxs-lookup"><span data-stu-id="1c533-250">Because the **Model.Data.Tax.Code** and **Model.Tax.Summary.Base** fields are selected for this lookup data source, each rule of this data source will be configured in the following way:</span></span>
    
    -   <span data-ttu-id="1c533-251">在显示的列表中，必须选择**征税级别列表**格式枚举的值作为返回值。</span><span class="sxs-lookup"><span data-stu-id="1c533-251">In the list that is presented, the value of the **List of taxation levels** format enumeration must be selected as a returned value.</span></span>
    -   <span data-ttu-id="1c533-252">必须输入税码作为此规则的条件。</span><span class="sxs-lookup"><span data-stu-id="1c533-252">The tax code must be entered as a condition of this rule.</span></span> <span data-ttu-id="1c533-253">仅适用于 **Model.Data.Tax** 数据源提供的税码。</span><span class="sxs-lookup"><span data-stu-id="1c533-253">Only tax codes that are provided by the **Model.Data.Tax** data source are applicable.</span></span>
    -   <span data-ttu-id="1c533-254">必须将税金基准额的最小值和最大值输入为此规则的条件。</span><span class="sxs-lookup"><span data-stu-id="1c533-254">Minimum and maximum values of the tax base amount must be entered as conditions of this rule.</span></span>

    <span data-ttu-id="1c533-255">这是在运行时如何评估此数据源的每个规则的方法：</span><span class="sxs-lookup"><span data-stu-id="1c533-255">Here is how each rule of this data source will be evaluated at runtime:</span></span>
    -   <span data-ttu-id="1c533-256">传递给此数据源的**字符串**数据类型的代码是否等于规则的税码？</span><span class="sxs-lookup"><span data-stu-id="1c533-256">Does the code of the **String** data type that was passed to this data source equal the tax code of a rule?</span></span>
    -   <span data-ttu-id="1c533-257">传递给此数据源的**实数**数据类型的值是否在特定的最小值和最大值之间？</span><span class="sxs-lookup"><span data-stu-id="1c533-257">Does the value of the **Real** data type that was passed to this data source fall between specific minimum and maximum values?</span></span>

    <span data-ttu-id="1c533-258">当两个条件都满足时，将认为规则适用。</span><span class="sxs-lookup"><span data-stu-id="1c533-258">A rule will be considered applicable when both conditions are satisfied.</span></span>

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a><span data-ttu-id="1c533-259">翻译添加的查找数据源的标签</span><span class="sxs-lookup"><span data-stu-id="1c533-259">Translate the label of the lookup data source that was added</span></span>

<span data-ttu-id="1c533-260">因为业务用户可能使用不同的语言来指定与法人相关的税码集，所以我们建议您翻译添加的任何查找数据源的标签，以便在相应页面上以每个用户的首选语言显示。</span><span class="sxs-lookup"><span data-stu-id="1c533-260">Because business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the label of any lookup data source that you add, so that it's presented in each user's preferred language on the corresponding page.</span></span>

1.  <span data-ttu-id="1c533-261">选择 **Model.Data.Selector** 数据源。</span><span class="sxs-lookup"><span data-stu-id="1c533-261">Select the **Model.Data.Selector** data source.</span></span>
2.  <span data-ttu-id="1c533-262">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="1c533-262">Select **Edit**.</span></span>
3.  <span data-ttu-id="1c533-263">单击**标签**字段。</span><span class="sxs-lookup"><span data-stu-id="1c533-263">Click in the **Label** field.</span></span>
4.  <span data-ttu-id="1c533-264">选择**翻译**。</span><span class="sxs-lookup"><span data-stu-id="1c533-264">Select **Translate**.</span></span>
5.  <span data-ttu-id="1c533-265">在**文本翻译**窗格中的**标签 ID** 字段中，输入 **LBL_SELECTOR_DS**。</span><span class="sxs-lookup"><span data-stu-id="1c533-265">In the **Text translation** pane, in the **Label Id** field, enter **LBL_SELECTOR_DS**.</span></span>
6.  <span data-ttu-id="1c533-266">在**语言为默认语言的文本**字段中，输入**按税码选择征税级别**。</span><span class="sxs-lookup"><span data-stu-id="1c533-266">In the **Text in default language** field, enter **Select tax level by tax code**.</span></span>
7.  <span data-ttu-id="1c533-267">在**语言**字段中，选择 **DE**。</span><span class="sxs-lookup"><span data-stu-id="1c533-267">In the **Language** field, select **DE**.</span></span>
8.  <span data-ttu-id="1c533-268">在**已翻译的文本**字段中，输入 **Steuerebene für Steuerkennzeichen auswählen**。</span><span class="sxs-lookup"><span data-stu-id="1c533-268">In the **Translated text** field, enter **Steuerebene für Steuerkennzeichen auswählen**.</span></span>
9.  <span data-ttu-id="1c533-269">选择**翻译**。</span><span class="sxs-lookup"><span data-stu-id="1c533-269">Select **Translate**.</span></span>
10. <span data-ttu-id="1c533-270">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="1c533-270">Select **OK**.</span></span>

    ![ER Operation 设计器页](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a><span data-ttu-id="1c533-272">添加一个新字段以使用配置的查找</span><span class="sxs-lookup"><span data-stu-id="1c533-272">Add a new field to consume the configured lookup</span></span>

1.  <span data-ttu-id="1c533-273">展开 **Model.Data** 项。</span><span class="sxs-lookup"><span data-stu-id="1c533-273">Expand the **Model.Data** item.</span></span>
2.  <span data-ttu-id="1c533-274">选择 **Model.Data.Summary** 项。</span><span class="sxs-lookup"><span data-stu-id="1c533-274">Select the **Model.Data.Summary** item.</span></span>
3.  <span data-ttu-id="1c533-275">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="1c533-275">Select **Add**.</span></span>
4.  <span data-ttu-id="1c533-276">选择 **Functions/Calculated field**。</span><span class="sxs-lookup"><span data-stu-id="1c533-276">Select **Functions/Calculated field**.</span></span>
5.  <span data-ttu-id="1c533-277">在**名称**字段中，输入 **LevelByLookup**。</span><span class="sxs-lookup"><span data-stu-id="1c533-277">In the **Name** field, enter **LevelByLookup**.</span></span>
6.  <span data-ttu-id="1c533-278">选择**编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="1c533-278">Select **Edit formula**.</span></span>
7.  <span data-ttu-id="1c533-279">在**公式字段**中，输入 **Model.Selector(Model.Data.Summary.Code)**.</span><span class="sxs-lookup"><span data-stu-id="1c533-279">In the **Formula field**, enter **Model.Selector(Model.Data.Summary.Code)**.</span></span>
8.  <span data-ttu-id="1c533-280">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="1c533-280">Select **Save**.</span></span>

    ![ER Operation 设计器页](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  <span data-ttu-id="1c533-282">关闭**公式编辑器**页。</span><span class="sxs-lookup"><span data-stu-id="1c533-282">Close the **Formula editor** page.</span></span>
10. <span data-ttu-id="1c533-283">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="1c533-283">Select **OK**.</span></span>

    ![ER Operation 设计器页](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    <span data-ttu-id="1c533-285">请注意，您添加的 **LevelByLookup** 计算字段将返回征税级别，作为每个汇总的税收交易记录的**征税级别列表**格式枚举的值。</span><span class="sxs-lookup"><span data-stu-id="1c533-285">Notice that the **LevelByLookup** calculated field that you added will return the taxation level as the value of the **List of taxation levels** format enumeration for each summarized tax transactions record.</span></span> <span data-ttu-id="1c533-286">记录的税码将传递到 **Model.Selector** 查找数据源，此数据源的规则集将用于选择正确的征税级别。</span><span class="sxs-lookup"><span data-stu-id="1c533-286">The tax code of the record will be passed to the **Model.Selector** lookup data source, and the set of rules for this data source will be used to select the correct taxation level.</span></span>

### <a name="add-a-new-format-enumeration-based-data-source"></a><span data-ttu-id="1c533-287">添加新的基于格式枚举的数据源</span><span class="sxs-lookup"><span data-stu-id="1c533-287">Add a new format enumeration-based data source</span></span>

<span data-ttu-id="1c533-288">接下来，您将添加一个新数据源，该数据源引用您之前添加的格式枚举。</span><span class="sxs-lookup"><span data-stu-id="1c533-288">Next, you will add a new data source that refers to the format enumeration that you added earlier.</span></span> <span data-ttu-id="1c533-289">稍后将在 ER 格式表达式中使用此数据源的值。</span><span class="sxs-lookup"><span data-stu-id="1c533-289">Values of this data source will be used in an ER format expression later.</span></span>

1.  <span data-ttu-id="1c533-290">选择**添加根**。</span><span class="sxs-lookup"><span data-stu-id="1c533-290">Select **Add root**.</span></span>
2.  <span data-ttu-id="1c533-291">选择**格式枚举\枚举**。</span><span class="sxs-lookup"><span data-stu-id="1c533-291">Select **Format enumerations\Enumeration**.</span></span>
3.  <span data-ttu-id="1c533-292">在**名称**字段中，输入 **TaxationLevel**。</span><span class="sxs-lookup"><span data-stu-id="1c533-292">In the **Name** field, enter **TaxationLevel**.</span></span>
4.  <span data-ttu-id="1c533-293">在**格式枚举**字段中，选择**征税级别列表**。</span><span class="sxs-lookup"><span data-stu-id="1c533-293">In the **Format enumeration** field, select **List of taxation levels**.</span></span>
5.  <span data-ttu-id="1c533-294">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="1c533-294">Select **Save**.</span></span>

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a><span data-ttu-id="1c533-295">修改现有字段以开始使用查找</span><span class="sxs-lookup"><span data-stu-id="1c533-295">Modify an existing field to start to use the lookup</span></span>

<span data-ttu-id="1c533-296">接下来，您将修改现有的计算字段，以使其使用配置的查找数据源根据税码返回正确的征税级别值。</span><span class="sxs-lookup"><span data-stu-id="1c533-296">Next, you will modify the existing calculated field so that it uses the configured lookup data source to return the correct taxation level value, depending on the tax code.</span></span>

1.  <span data-ttu-id="1c533-297">选择 **Model.Data.Summary.Level** 项。</span><span class="sxs-lookup"><span data-stu-id="1c533-297">Select the **Model.Data.Summary.Level** item.</span></span>
2.  <span data-ttu-id="1c533-298">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="1c533-298">Select **Edit**.</span></span>
3.  <span data-ttu-id="1c533-299">选择**编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="1c533-299">Select **Edit formula**.</span></span>

    <span data-ttu-id="1c533-300">请注意，**Model.Data.Summary.Level** 字段的当前表达式包括以下硬编码的税码：</span><span class="sxs-lookup"><span data-stu-id="1c533-300">Notice that the current expression of the **Model.Data.Summary.Level** field includes the following hard-coded tax codes:</span></span>
    
    <span data-ttu-id="1c533-301">CASE（@.Code、“VAT19”、“Regular”、“InVAT19”、“Regular”、“VAT7”、“Reduced”、“InVAT7”、“Reduced”、“THIRD”、“None”、“InVAT0”、“None”、“Other”）</span><span class="sxs-lookup"><span data-stu-id="1c533-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span></span>

4.  <span data-ttu-id="1c533-302">在**公式**字段中，输入 **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**。</span><span class="sxs-lookup"><span data-stu-id="1c533-302">In the **Formula** field, enter **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span></span>

    ![ER Operation 设计器页](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    <span data-ttu-id="1c533-304">请注意，**Model.Data.Summary.Level** 字段的表达式现在将基于当前记录的税码和业务用户在 **Model.Data.Selector** 查找数据源中配置的规则集返回征税级别。</span><span class="sxs-lookup"><span data-stu-id="1c533-304">Notice that the expression of the **Model.Data.Summary.Level** field will now return the taxation level, based on the tax code of the current record and the set of rules that that a business user configures in the **Model.Data.Selector** lookup data source.</span></span>
    
5.  <span data-ttu-id="1c533-305">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="1c533-305">Select **Save**.</span></span>
6.  <span data-ttu-id="1c533-306">关闭**公式设计器**页。</span><span class="sxs-lookup"><span data-stu-id="1c533-306">Close **Formula designer** page.</span></span>
7.  <span data-ttu-id="1c533-307">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="1c533-307">Select **OK**.</span></span>
8.  <span data-ttu-id="1c533-308">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="1c533-308">Select **Save**.</span></span>
9.  <span data-ttu-id="1c533-309">关闭**格式设计器**页。</span><span class="sxs-lookup"><span data-stu-id="1c533-309">Close **Format designer** page.</span></span>

## <a name="complete-the-draft-version-of-a-derived-format"></a><span data-ttu-id="1c533-310">完成派生格式的草稿版本</span><span class="sxs-lookup"><span data-stu-id="1c533-310">Complete the draft version of a derived format</span></span>

1.  <span data-ttu-id="1c533-311">在**版本**快速选项卡上，选择**更改状态**。</span><span class="sxs-lookup"><span data-stu-id="1c533-311">On the **Versions** fast tab, select **Change status**.</span></span>
2.  <span data-ttu-id="1c533-312">选择**完成**。</span><span class="sxs-lookup"><span data-stu-id="1c533-312">Select **Complete**.</span></span>
3.  <span data-ttu-id="1c533-313">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="1c533-313">Select **OK**.</span></span>

## <a name="export-completed-version-of-modified-format"></a><span data-ttu-id="1c533-314">导出修改后格式的完整版本</span><span class="sxs-lookup"><span data-stu-id="1c533-314">Export completed version of modified format</span></span>

1.  <span data-ttu-id="1c533-315">在配置树中，选择**用于了解如何查找 LE 数据的格式**项。</span><span class="sxs-lookup"><span data-stu-id="1c533-315">In the configuration tree, select the **Format to learn how to lookup LE data** item.</span></span>
2.  <span data-ttu-id="1c533-316">在**版本**快速选项卡上，选择状态为**已完成**的记录。</span><span class="sxs-lookup"><span data-stu-id="1c533-316">On the **Versions** fast tab, select the record that has a status of **Completed**.</span></span>
3.  <span data-ttu-id="1c533-317">选择**交换**。</span><span class="sxs-lookup"><span data-stu-id="1c533-317">Select **Exchange**.</span></span>
4.  <span data-ttu-id="1c533-318">选择**导出为 XML 文件**。</span><span class="sxs-lookup"><span data-stu-id="1c533-318">Select **Export as XML file**.</span></span>
5.  <span data-ttu-id="1c533-319">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="1c533-319">Select **OK**.</span></span>
6.  <span data-ttu-id="1c533-320">Web 浏览器下载 **Format to learn how to lookup LE data.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="1c533-320">The web browser downloads a **Format to learn how to lookup LE data.xml** file.</span></span> <span data-ttu-id="1c533-321">将此文件存储在本地。</span><span class="sxs-lookup"><span data-stu-id="1c533-321">Store this file locally.</span></span>

<span data-ttu-id="1c533-322">对**用于了解如何查找 LE 数据的格式**的父项重复本节中的步骤，并在本地存储以下文件：</span><span class="sxs-lookup"><span data-stu-id="1c533-322">Repeat steps in this section for parent items of the **Format to learn how to lookup LE data** format, and store the following files locally:</span></span>

-   <span data-ttu-id="1c533-323">Format to learn parameterized calls.xml</span><span class="sxs-lookup"><span data-stu-id="1c533-323">Format to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="1c533-324">Mapping to learn parameterized calls.xml</span><span class="sxs-lookup"><span data-stu-id="1c533-324">Mapping to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="1c533-325">Model to learn parameterized calls.xml</span><span class="sxs-lookup"><span data-stu-id="1c533-325">Model to learn parameterized calls.xml</span></span>

<span data-ttu-id="1c533-326">要了解如何使用已配置的**用于了解如何查找 LE 数据的格式** ER 格式来设置法人相关的税码集，以按不同征税级别筛选税收交易记录，请完成[为每个法人设置 ER 格式的参数](er-app-specific-parameters-set-up.md)主题中的步骤。</span><span class="sxs-lookup"><span data-stu-id="1c533-326">To learn how to use the configured **Format to learn how to lookup LE data** ER format to set up legal entity–dependent sets of tax codes to filter tax transactions by different taxation levels, complete the steps in the [Set up the parameters of an ER format per legal entity](er-app-specific-parameters-set-up.md) topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c533-327">其他资源</span><span class="sxs-lookup"><span data-stu-id="1c533-327">Additional resources</span></span>

[<span data-ttu-id="1c533-328">电子报告中的配方设计器</span><span class="sxs-lookup"><span data-stu-id="1c533-328">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="1c533-329">为每个法人设置 ER 格式的参数</span><span class="sxs-lookup"><span data-stu-id="1c533-329">Set up the parameters of an ER format per legal entity</span></span>](er-app-specific-parameters-set-up.md)

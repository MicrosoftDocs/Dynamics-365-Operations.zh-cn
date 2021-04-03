---
title: 推迟执行 ER 格式的序列元素
description: 本主题说明如何推迟执行电子报表 (ER) 格式的序列元素。
author: NickSelin
manager: kfend
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-01
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: b1a9bb072330f586799f5cfea676d941739ca818
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562158"
---
# <a name="defer-the-execution-of-sequence-elements-in-er-formats"></a><span data-ttu-id="e7b58-103">推迟执行 ER 格式的序列元素</span><span class="sxs-lookup"><span data-stu-id="e7b58-103">Defer the execution of sequence elements in ER formats</span></span>

[!include [banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="e7b58-104">概览</span><span class="sxs-lookup"><span data-stu-id="e7b58-104">Overview</span></span>

<span data-ttu-id="e7b58-105">您可以使用[电子报表 (ER)](general-electronic-reporting.md) 框架的工序设计器，以[配置](tasks/er-format-configuration-2016-11.md)用于生成文本格式出站文档的 ER 解决方案的[格式组件](general-electronic-reporting.md#FormatComponentOutbound)。</span><span class="sxs-lookup"><span data-stu-id="e7b58-105">You can use the Operations designer of the [Electronic reporting (ER)](general-electronic-reporting.md) framework to [configure](tasks/er-format-configuration-2016-11.md) the [format component](general-electronic-reporting.md#FormatComponentOutbound) of an ER solution that is used to generate outbound documents in a text format.</span></span> <span data-ttu-id="e7b58-106">配置的格式组件的层次结构由各种类型的格式元素组成。</span><span class="sxs-lookup"><span data-stu-id="e7b58-106">The hierarchical structure of the configured format component consists of format elements of various types.</span></span> <span data-ttu-id="e7b58-107">这些格式元素用于在运行时用所需的信息填充生成的文档。</span><span class="sxs-lookup"><span data-stu-id="e7b58-107">These format elements are used to fill generated documents with the required information at runtime.</span></span> <span data-ttu-id="e7b58-108">默认情况下，当您运行 ER 格式时，格式元素的运行顺序与它们在格式层次结构中的显示顺序相同：从上到下一个接一个。</span><span class="sxs-lookup"><span data-stu-id="e7b58-108">By default, when you run an ER format, the format elements are run in the same order as they are presented in the format hierarchy: one by one, from top to bottom.</span></span> <span data-ttu-id="e7b58-109">但是，在设计时，您可以更改已配置格式组件的任何序列元素的执行顺序。</span><span class="sxs-lookup"><span data-stu-id="e7b58-109">However, at design time, you can change the execution order for any sequence elements of the configured format component.</span></span>

<span data-ttu-id="e7b58-110">通过对已配置格式的序列格式元素打开 <a name="DeferredSequenceExecution"></a>**推迟执行** 选项，可以推迟（延迟）执行该元素。</span><span class="sxs-lookup"><span data-stu-id="e7b58-110">By turning on the <a name="DeferredSequenceExecution"></a>**Deferred execution** option for a sequence format element in the configured format, you can defer (postpone) the execution of that element.</span></span> <span data-ttu-id="e7b58-111">在这种情况下，该元素只有在其父元素的所有其他元素都已运行后才能运行。</span><span class="sxs-lookup"><span data-stu-id="e7b58-111">In this case, the element isn't run until all other elements of its parent have been run.</span></span>

<span data-ttu-id="e7b58-112">若要了解有关此功能的详细信息，请完成本主题中的示例。</span><span class="sxs-lookup"><span data-stu-id="e7b58-112">To learn more about this feature, complete the example in this topic.</span></span>

## <a name="limitations"></a><span data-ttu-id="e7b58-113">限制</span><span class="sxs-lookup"><span data-stu-id="e7b58-113">Limitations</span></span>

<span data-ttu-id="e7b58-114">仅针对为 ER 格式（用于生成文本格式的 **出站** 文档）配置的序列元素支持 **推迟执行** 选项。</span><span class="sxs-lookup"><span data-stu-id="e7b58-114">The **Deferred execution** option is supported only for sequence elements that are configured for an ER format that is used to generate **outbound** documents in text format.</span></span>

<span data-ttu-id="e7b58-115">**推迟执行** 选项不适用于已配置为最大长度受限制的修整序列的序列。</span><span class="sxs-lookup"><span data-stu-id="e7b58-115">The **Deferred execution** option isn't applicable to sequences that have been configured as trimmed sequences where the maximum length is limited.</span></span>

## <a name="example-defer-the-execution-of-a-sequence-element-in-an-er-format"></a><a name="Example"></a><span data-ttu-id="e7b58-116">示例：推迟执行 ER 格式的序列元素</span><span class="sxs-lookup"><span data-stu-id="e7b58-116">Example: Defer the execution of a sequence element in an ER format</span></span>

<span data-ttu-id="e7b58-117">以下步骤说明了具有系统管理员或电子报告职能顾问[角色](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles)的用户如何配置一个 ER 格式，以包含执行顺序与格式层次结构中的执行顺序不同的序列元素。</span><span class="sxs-lookup"><span data-stu-id="e7b58-117">The following steps explain how a user in the System administrator or Electronic reporting functional consultant [role](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles) can configure an ER format that contains a sequence element where order of execution differs from the order in the format hierarchy.</span></span>

<span data-ttu-id="e7b58-118">这些步骤可以在 **USMF** 公司内的 Microsoft Dynamics 365 Finance 中执行。</span><span class="sxs-lookup"><span data-stu-id="e7b58-118">These steps can be performed in the **USMF** company in Microsoft Dynamics 365 Finance.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e7b58-119">先决条件</span><span class="sxs-lookup"><span data-stu-id="e7b58-119">Prerequisites</span></span>

<span data-ttu-id="e7b58-120">若要完成本示例，您必须能够用以下角色之一访问 **USMF** 公司的 Finance：</span><span class="sxs-lookup"><span data-stu-id="e7b58-120">To complete this example, you must have access to the **USMF** company in Finance for one of the following roles:</span></span>

- <span data-ttu-id="e7b58-121">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="e7b58-121">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="e7b58-122">系统管理员</span><span class="sxs-lookup"><span data-stu-id="e7b58-122">System administrator</span></span>

<span data-ttu-id="e7b58-123">如果您尚未完成[推迟执行 ER 格式的 XML 元素](er-defer-xml-element.md#Example)主题中的示例，请下载示例 ER 解决方案的以下[配置](general-electronic-reporting.md#Configuration)。</span><span class="sxs-lookup"><span data-stu-id="e7b58-123">If you haven't yet completed the example in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md#Example) topic, download the following [configurations](general-electronic-reporting.md#Configuration) of the sample ER solution.</span></span>

| <span data-ttu-id="e7b58-124">内容描述</span><span class="sxs-lookup"><span data-stu-id="e7b58-124">Content description</span></span>            | <span data-ttu-id="e7b58-125">文件名</span><span class="sxs-lookup"><span data-stu-id="e7b58-125">File name</span></span> |
|--------------------------------|-----------|
| <span data-ttu-id="e7b58-126">ER 数据模型配置</span><span class="sxs-lookup"><span data-stu-id="e7b58-126">ER data model configuration</span></span>    | [<span data-ttu-id="e7b58-127">Model to learn deferred elements.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="e7b58-127">Model to learn deferred elements.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="e7b58-128">ER 模型映射配置</span><span class="sxs-lookup"><span data-stu-id="e7b58-128">ER model mapping configuration</span></span> | [<span data-ttu-id="e7b58-129">Mapping to learn deferred elements.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="e7b58-129">Mapping to learn deferred elements.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

<span data-ttu-id="e7b58-130">在开始之前，您还必须下载并保存示例 ER 解决方案的以下配置。</span><span class="sxs-lookup"><span data-stu-id="e7b58-130">Before you begin, you must also download and save the following configuration of the sample ER solution.</span></span>

| <span data-ttu-id="e7b58-131">内容描述</span><span class="sxs-lookup"><span data-stu-id="e7b58-131">Content description</span></span>     |<span data-ttu-id="e7b58-132">文件名</span><span class="sxs-lookup"><span data-stu-id="e7b58-132">File name</span></span> |
|-------------------------|----------|
| <span data-ttu-id="e7b58-133">ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="e7b58-133">ER format configuration</span></span> | [<span data-ttu-id="e7b58-134">Format to learn deferred sequences.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="e7b58-134">Format to learn deferred sequences.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="import-the-sample-er-configurations"></a><span data-ttu-id="e7b58-135">导入示例 ER 配置</span><span class="sxs-lookup"><span data-stu-id="e7b58-135">Import the sample ER configurations</span></span>

1. <span data-ttu-id="e7b58-136">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-136">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e7b58-137">选择 **申报配置**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-137">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="e7b58-138">在 **配置** 页面上，如果 **用于了解推迟的元素的模型** 配置在配置树中不可用，请导入 ER 数据模型配置：</span><span class="sxs-lookup"><span data-stu-id="e7b58-138">On the **Configurations** page, if the **Model to learn deferred elements** configuration isn't available in the configuration tree, import the ER data model configuration:</span></span>

    1. <span data-ttu-id="e7b58-139">选择 **交换**，然后选择 **从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-139">Select **Exchange**, and then select **Load from XML file**.</span></span>
    2. <span data-ttu-id="e7b58-140">选择 **浏览**，找到并选择 **Model to learn deferred elements.1.xml** 文件，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-140">Select **Browse**, find and select the **Model to learn deferred elements.1.xml** file, and then select **OK**.</span></span>

4. <span data-ttu-id="e7b58-141">如果 **用于了解推迟的元素的映射** 配置在配置树中不可用，请导入 ER 模型映射配置：</span><span class="sxs-lookup"><span data-stu-id="e7b58-141">If the **Mapping to learn deferred elements** configuration isn't available in the configuration tree, import the ER model mapping configuration:</span></span>

    1. <span data-ttu-id="e7b58-142">选择 **交换**，然后选择 **从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-142">Select **Exchange**, and then select **Load from XML file**.</span></span>
    2. <span data-ttu-id="e7b58-143">选择 **浏览**，找到并选择 **Mapping to learn deferred elements.1.1.xml** 文件，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-143">Select **Browse**, find and select the **Mapping to learn deferred elements.1.1.xml** file, and then select **OK**.</span></span>

5. <span data-ttu-id="e7b58-144">导入 ER 格式配置：</span><span class="sxs-lookup"><span data-stu-id="e7b58-144">Import the ER format configuration:</span></span>

    1. <span data-ttu-id="e7b58-145">选择 **交换**，然后选择 **从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-145">Select **Exchange**, and then select **Load from XML file**.</span></span>
    2. <span data-ttu-id="e7b58-146">选择 **浏览**，找到并选择 **Format to learn deferred sequences.1.1.xml** 文件，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-146">Select **Browse**, find and select the **Format to learn deferred sequences.1.1.xml** file, and then select **OK**.</span></span>

6. <span data-ttu-id="e7b58-147">在配置树中，展开 **用于了解推迟的元素的模型**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-147">In the configuration tree, expand **Model to learn deferred elements**.</span></span>
7. <span data-ttu-id="e7b58-148">在配置树中查看导入的 ER 配置的列表。</span><span class="sxs-lookup"><span data-stu-id="e7b58-148">Review the list of imported ER configurations in the configuration tree.</span></span>

    ![“配置”页面上导入的 ER 配置](./media/ER-DeferredSequence-Configurations.png)

### <a name="activate-a-configurations-provider"></a><span data-ttu-id="e7b58-150">启用配置提供程序</span><span class="sxs-lookup"><span data-stu-id="e7b58-150">Activate a configurations provider</span></span>

1. <span data-ttu-id="e7b58-151">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-151">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e7b58-152">在 **本地化配置** 页上的 **配置提供程序** 部分中，确保列出了示例公司 Litware, Inc. (`http://www.litware.com`) 的[配置提供程序](general-electronic-reporting.md#Provider)，并将其标记为活动状态。</span><span class="sxs-lookup"><span data-stu-id="e7b58-152">On the **Localization configurations** page, in the **Configuration providers** section, make sure that the [configuration provider](general-electronic-reporting.md#Provider) for the Litware, Inc. (`http://www.litware.com`) sample company is listed, and that it's marked as active.</span></span> <span data-ttu-id="e7b58-153">如果未列出此配置提供程序，或者未将其标记为活动状态，请按照[创建一个配置提供程序，并标记其为活动状态](./tasks/er-configuration-provider-mark-it-active-2016-11.md)中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="e7b58-153">If this configuration provider isn't listed, or if it isn't marked as active, follow the steps in the [Create a configuration provider and mark it as active](./tasks/er-configuration-provider-mark-it-active-2016-11.md) topic.</span></span>

    ![“本地化配置”页面上的示例公司 Litware, Inc.](./media/ER-DeferredSequence-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a><span data-ttu-id="e7b58-155">查看导入的模型映射</span><span class="sxs-lookup"><span data-stu-id="e7b58-155">Review the imported model mapping</span></span>

<span data-ttu-id="e7b58-156">查看 ER 模型映射组件的设置，该组件配置为根据请求来访问税收交易记录并公开访问的数据。</span><span class="sxs-lookup"><span data-stu-id="e7b58-156">Review the settings of the ER model mapping component that is configured to access tax transactions and expose accessed data on request.</span></span>

1. <span data-ttu-id="e7b58-157">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-157">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e7b58-158">选择 **申报配置**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-158">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="e7b58-159">在 **配置** 页上的配置树中，展开 **用于了解推迟的元素的模型**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-159">On the **Configurations** page, in the configuration tree, expand **Model to learn deferred elements**.</span></span>
4. <span data-ttu-id="e7b58-160">选择 **用于了解推迟的元素的映射** 配置。</span><span class="sxs-lookup"><span data-stu-id="e7b58-160">Select the **Mapping to learn deferred elements** configuration.</span></span>
5. <span data-ttu-id="e7b58-161">选择 **设计器** 来打开映射列表。</span><span class="sxs-lookup"><span data-stu-id="e7b58-161">Select **Designer** to open the list of mappings.</span></span>
6. <span data-ttu-id="e7b58-162">选择 **设计器** 查看映射详细信息。</span><span class="sxs-lookup"><span data-stu-id="e7b58-162">Select **Designer** to review the mapping details.</span></span>
7. <span data-ttu-id="e7b58-163">选择 **显示详细信息**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-163">Select **Show details**.</span></span>
8. <span data-ttu-id="e7b58-164">查看配置为访问税收交易记录的数据源：</span><span class="sxs-lookup"><span data-stu-id="e7b58-164">Review the data sources that are configured to access tax transactions:</span></span>

    - <span data-ttu-id="e7b58-165">*表记录* 类型的 **交易记录** 数据源被配置为访问 **TaxTrans** 应用程序表的记录。</span><span class="sxs-lookup"><span data-stu-id="e7b58-165">The **Transactions** data source of the *Table record* type is configured to access records of the **TaxTrans** application table.</span></span>
    - <span data-ttu-id="e7b58-166">**计算字段** 类型的 *凭证* 数据源被配置为返回所需的凭证代码（**INV-10000349** 和 **INV-10000350**）作为记录列表。</span><span class="sxs-lookup"><span data-stu-id="e7b58-166">The **Vouchers** data source of the *Calculated field* type is configured to return the required voucher codes (**INV-10000349** and **INV-10000350**) as a list of records.</span></span>
    - <span data-ttu-id="e7b58-167">**计算字段** 类型的 *已筛选* 数据源被配置为从 **交易记录** 数据源中仅选择所需凭证的税收交易记录。</span><span class="sxs-lookup"><span data-stu-id="e7b58-167">The **Filtered** data source of the *Calculated field* type is configured to select, from the **Transactions** data source, only tax transactions of the required vouchers.</span></span>
    - <span data-ttu-id="e7b58-168">为 **已筛选** 数据源添加了 *计算字段* 类型的 **\$TaxAmount** 字段，以显示具有相反符号的税收值。</span><span class="sxs-lookup"><span data-stu-id="e7b58-168">The **\$TaxAmount** field of the *Calculated field* type is added for the **Filtered** data source to expose the tax value that has the opposite sign.</span></span>
    - <span data-ttu-id="e7b58-169">**分组依据** 类型的 *已分组* 数据源被配置为将 **已筛选** 数据源的已筛选税收交易记录分组。</span><span class="sxs-lookup"><span data-stu-id="e7b58-169">The **Grouped** data source of the *Group By* type is configured to group filtered tax transactions of the **Filtered** data source.</span></span>
    - <span data-ttu-id="e7b58-170">**已分组** 数据源的 **TotalSum** 聚合字段被配置为针对该数据源的所有已筛选税收交易记录汇总 **已筛选** 数据源的 **\$TaxAmount** 字段值。</span><span class="sxs-lookup"><span data-stu-id="e7b58-170">The **TotalSum** aggregation field of the **Grouped** data source is configured to summarize values of the **\$TaxAmount** field of the **Filtered** data source for all filtered tax transactions of that data source.</span></span>

        ![“编辑‘GroupBy’参数”页面上的 TotalSum 聚合字段](./media/ER-DeferredSequence-GroupByParameters.png)

9. <span data-ttu-id="e7b58-172">查看配置的数据源如何绑定到数据模型，以及它们如何公开访问的数据以使其以 ER 格式可用：</span><span class="sxs-lookup"><span data-stu-id="e7b58-172">Review how the configured data sources are bound to the data model, and how they expose accessed data to make it available in an ER format:</span></span>

    - <span data-ttu-id="e7b58-173">**已筛选** 数据源已绑定到数据模型的 **Data.List** 字段。</span><span class="sxs-lookup"><span data-stu-id="e7b58-173">The **Filtered** data source is bound to the **Data.List** field of the data model.</span></span>
    - <span data-ttu-id="e7b58-174">**已筛选** 数据源的 **\$TaxAmount** 字段已绑定到数据模型的 **Data.List.Value** 字段。</span><span class="sxs-lookup"><span data-stu-id="e7b58-174">The **\$TaxAmount** field of the **Filtered** data source is bound to the **Data.List.Value** field of the data model.</span></span>
    - <span data-ttu-id="e7b58-175">**已分组** 数据源的 **TotalSum** 字段已绑定到数据模型的 **Data.Summary.Total** 字段。</span><span class="sxs-lookup"><span data-stu-id="e7b58-175">The **TotalSum** field of the **Grouped** data source is bound to the **Data.Summary.Total** field of the data model.</span></span>

    ![模型映射设计器页面](./media/ER-DeferredSequence-ModelMapping.png)

10. <span data-ttu-id="e7b58-177">关闭 **模型映射设计器** 和 **模型映射** 页面。</span><span class="sxs-lookup"><span data-stu-id="e7b58-177">Close the **Model mapping designer** and **Model mappings** pages.</span></span>

### <a name="review-the-imported-format"></a><span data-ttu-id="e7b58-178">查看导入的格式</span><span class="sxs-lookup"><span data-stu-id="e7b58-178">Review the imported format</span></span>

1. <span data-ttu-id="e7b58-179">在 **配置** 页面上的配置树中，选择 **用于了解延迟序列的格式** 配置。</span><span class="sxs-lookup"><span data-stu-id="e7b58-179">On the **Configurations** page, in the configuration tree, select the **Format to learn deferred sequences** configuration.</span></span>
2. <span data-ttu-id="e7b58-180">选择 **设计器** 查看格式详细信息。</span><span class="sxs-lookup"><span data-stu-id="e7b58-180">Select **Designer** to review the format details.</span></span>
3. <span data-ttu-id="e7b58-181">选择 **显示详细信息**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-181">Select **Show details**.</span></span>
4. <span data-ttu-id="e7b58-182">查看 ER 格式组件的设置，这些设置被配置为以文本格式生成出站文档，其中包括税收交易记录的详细信息：</span><span class="sxs-lookup"><span data-stu-id="e7b58-182">Review the settings of the ER format components that are configured to generate an outbound document in text format that includes details of the tax transactions:</span></span>

    - <span data-ttu-id="e7b58-183">**报表\\行** 序列格式元素被配置为用嵌套序列元素（**标题**、**记录** 和 **汇总**）生成的单个行填充出站文档。</span><span class="sxs-lookup"><span data-stu-id="e7b58-183">The **Report\\Lines** sequence format element is configured to fill the outbound document with a single line that is generated from the nested sequence elements (**Header**, **Record**, and **Summary**).</span></span>

        ![“格式设计器”页面上的行序列格式元素和嵌套元素](./media/ER-DeferredSequence-Format.png)

    - <span data-ttu-id="e7b58-185">**报表\\行\\标题** 序列格式元素被配置为用单个标题行填充出站文档，以显示处理的开始日期和时间。</span><span class="sxs-lookup"><span data-stu-id="e7b58-185">The **Report\\Lines\\Header** sequence format element is configured to fill the outbound document with a single header line that shows the date and time  when the processing starts.</span></span>
    - <span data-ttu-id="e7b58-186">**报表\\行\\记录** 序列格式元素被配置为用显示各项税收交易记录详细信息的单行填充出站文档。</span><span class="sxs-lookup"><span data-stu-id="e7b58-186">The **Report \\Lines\\Record** sequence format element is configured to fill the outbound document with a single line that shows the details of individual tax transactions.</span></span> <span data-ttu-id="e7b58-187">这些税收交易记录以分号分隔。</span><span class="sxs-lookup"><span data-stu-id="e7b58-187">These tax transactions are separated by a semicolon.</span></span>

        ![记录使用分号作为分隔符的序列格式元素](./media/ER-DeferredSequence-Format1.png)

    - <span data-ttu-id="e7b58-189">**报表\\行\\汇总** 序列格式元素被配置为用包括已处理税收交易记录中税收值总计的单个汇总行填充的出站文档。</span><span class="sxs-lookup"><span data-stu-id="e7b58-189">The **Report\\Lines\\Summary** sequence format element is configured to fill the outbound document with a single summary line that includes the sum of the tax values from the processed tax transactions.</span></span>

4. <span data-ttu-id="e7b58-190">在 **映射** 选项卡上，查看以下详细信息：</span><span class="sxs-lookup"><span data-stu-id="e7b58-190">On the **Mapping** tab, review the following details:</span></span>

    - <span data-ttu-id="e7b58-191">**报表\\行\\标题** 元素不必绑定到数据源即可在出站文档中生成单行。</span><span class="sxs-lookup"><span data-stu-id="e7b58-191">The **Report\\Lines\\Header** element doesn't have to be bound to a data source to generate a single line in an outbound document.</span></span>
    - <span data-ttu-id="e7b58-192">**Prefix1** 元素生成 **P1** 符号以表明添加的行是报表标题行。</span><span class="sxs-lookup"><span data-stu-id="e7b58-192">The **Prefix1** element generates **P1** symbols to indicate that the line that is added is the report header line.</span></span>
    - <span data-ttu-id="e7b58-193">**ExecutionDateTime** 元素会生成标题行的添加日期和时间（包括毫秒）。</span><span class="sxs-lookup"><span data-stu-id="e7b58-193">The **ExecutionDateTime** element generates the date and time (including milliseconds) when the header line is added.</span></span>
    - <span data-ttu-id="e7b58-194">**报表\\行\\记录** 元素已绑定到 **model.Data.List** 列表，以为绑定列表中的每条记录生成一行。</span><span class="sxs-lookup"><span data-stu-id="e7b58-194">The **Report\\Lines\\Record** element is bound to the **model.Data.List** list to generate a single line for every record from the bound list.</span></span>
    - <span data-ttu-id="e7b58-195">**Prefix2** 元素生成 **P2** 符号以表明添加的行适用于税收交易记录明细。</span><span class="sxs-lookup"><span data-stu-id="e7b58-195">The **Prefix2** element generates **P2** symbols to indicate that the line that is added is for the tax transaction details.</span></span>
    - <span data-ttu-id="e7b58-196">**TaxAmount** 元素已绑定到 **model.Data.List.Value**（在相对路径视图中显示为 **\@.Value**）以生成当前税收交易记录的税收值。</span><span class="sxs-lookup"><span data-stu-id="e7b58-196">The **TaxAmount** element is bound to **model.Data.List.Value** (which is shown as **\@.Value** in the relative path view) to generate the tax value of the current tax transaction.</span></span>
    - <span data-ttu-id="e7b58-197">**RunningTotal** 元素是税收值累计总额的占位符。</span><span class="sxs-lookup"><span data-stu-id="e7b58-197">The **RunningTotal** element is a placeholder for the running total of the tax values.</span></span> <span data-ttu-id="e7b58-198">当前，此元素没有输出，因为没有为其配置绑定或默认值。</span><span class="sxs-lookup"><span data-stu-id="e7b58-198">Currently, this element has no output, because neither a binding nor a default value is configured for it.</span></span>
    - <span data-ttu-id="e7b58-199">**ExecutionDateTime** 元素生成在此报表中处理当前交易时的日期和时间（包括毫秒）。</span><span class="sxs-lookup"><span data-stu-id="e7b58-199">The **ExecutionDateTime** element generates the date and time (including milliseconds) when the current transaction is processed in this report.</span></span>
    - <span data-ttu-id="e7b58-200">**报表\\行\\汇总** 元素不必绑定到数据源即可在出站文档中生成单行。</span><span class="sxs-lookup"><span data-stu-id="e7b58-200">The **Report\\Lines\\Summary** element doesn't have to be bound to a data source to generate a single line in an outbound document.</span></span>
    - <span data-ttu-id="e7b58-201">**Prefix3** 元素生成 **P3** 符号以表明添加的行包含总税收值。</span><span class="sxs-lookup"><span data-stu-id="e7b58-201">The **Prefix3** element generates **P3** symbols to indicate that the line that is added contains the total tax value.</span></span>
    - <span data-ttu-id="e7b58-202">**TotalTaxAmount** 元素已绑定到 **model.Data.Summary.Total** 以生成已处理税收交易记录的税收值总和。</span><span class="sxs-lookup"><span data-stu-id="e7b58-202">The **TotalTaxAmount** element is bound to **model.Data.Summary.Total** to generate the sum of the tax values of the processed tax transactions.</span></span>
    - <span data-ttu-id="e7b58-203">**ExecutionDateTime** 元素会生成汇总行的添加日期和时间（包括毫秒）。</span><span class="sxs-lookup"><span data-stu-id="e7b58-203">The **ExecutionDateTime** element generates the date and time (including milliseconds) when the summary line is added.</span></span>

    ![“格式设计器”页上的“映射”选项卡](./media/ER-DeferredSequence-Format2.png)

### <a name="run-the-imported-format"></a><span data-ttu-id="e7b58-205">运行导入的格式</span><span class="sxs-lookup"><span data-stu-id="e7b58-205">Run the imported format</span></span>

1. <span data-ttu-id="e7b58-206">在 **格式设计器** 页上，选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-206">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="e7b58-207">下载 Web 浏览器提供的文件，然后将其打开以进行检查。</span><span class="sxs-lookup"><span data-stu-id="e7b58-207">Download the file that the web browser offers, and open it for review.</span></span>

    ![下载的文件](./media/ER-DeferredSequence-Run.png)

<span data-ttu-id="e7b58-209">请注意，汇总行 22 显示了已处理交易记录的税收值总和。</span><span class="sxs-lookup"><span data-stu-id="e7b58-209">Notice that summary line 22 presents the sum of the tax values for the processed transactions.</span></span> <span data-ttu-id="e7b58-210">由于该格式已配置为使用 **model.Data.Summary.Total** 绑定返回此总和，所以通过调用使用模型映射的 **GroupBy** 类型的 **已分组** 数据源 *TotalSum* 汇总计算了此总和。</span><span class="sxs-lookup"><span data-stu-id="e7b58-210">Because the format is configured to use the **model.Data.Summary.Total** binding to return this sum, the sum is calculated by calling the **TotalSum** aggregation of the **Grouped** data source of the *GroupBy* type that uses the model mapping.</span></span> <span data-ttu-id="e7b58-211">为了计算此汇总，模型映射会在 **已筛选** 数据源中选择的所有交易记录上迭代。</span><span class="sxs-lookup"><span data-stu-id="e7b58-211">To calculate this aggregation, model mapping iterates over all transactions that have been selected in the **Filtered** data source.</span></span> <span data-ttu-id="e7b58-212">通过比较第 21 行和第 22 行的执行时间，可以确定计算总和用了 10 毫秒 (ms)。</span><span class="sxs-lookup"><span data-stu-id="e7b58-212">By comparing the execution times of lines 21 and 22, you can determine that calculation of the sum took 10 milliseconds (ms).</span></span> <span data-ttu-id="e7b58-213">通过比较第 2 行和第 21 行的执行时间，可以确定生成所有交易记录行用了 7 ms。</span><span class="sxs-lookup"><span data-stu-id="e7b58-213">By comparing the execution times of lines 2 and 21, you can determine that generation of all transactional lines took 7 ms.</span></span> <span data-ttu-id="e7b58-214">因此，总共需要 17 ms。</span><span class="sxs-lookup"><span data-stu-id="e7b58-214">Therefore, a total of 17 ms was required.</span></span>

### <a name="modify-the-format-so-that-the-summing-is-based-on-generated-output"></a><span data-ttu-id="e7b58-215">修改格式，以便根据生成的输出来求和</span><span class="sxs-lookup"><span data-stu-id="e7b58-215">Modify the format so that the summing is based on generated output</span></span>

<span data-ttu-id="e7b58-216">如果交易记录量远大于当前示例中的交易记录量，则求和时间可能会增加并导致性能问题。</span><span class="sxs-lookup"><span data-stu-id="e7b58-216">If the volume of transactions is much larger than the volume in the current example, the summing time might increase and cause performance issues.</span></span> <span data-ttu-id="e7b58-217">通过更改格式设置，可以帮助防止这些性能问题。</span><span class="sxs-lookup"><span data-stu-id="e7b58-217">By changing the setting of the format, you can help prevent these performance issues.</span></span> <span data-ttu-id="e7b58-218">因为您访问税收值以将其包括在生成的报表中，所以您可以重复使用此信息来求税收值总计。</span><span class="sxs-lookup"><span data-stu-id="e7b58-218">Because you access tax values to include them in the generated report, you can reuse this information to sum tax values.</span></span> <span data-ttu-id="e7b58-219">有关更多信息，请参见[配置格式以进行计数和求和](./tasks/er-format-counting-summing-1.md)。</span><span class="sxs-lookup"><span data-stu-id="e7b58-219">For more information, see [Configure format to do counting and summing](./tasks/er-format-counting-summing-1.md).</span></span>

1. <span data-ttu-id="e7b58-220">在 **格式设计师** 页面上的 **格式** 选项卡上，选择格式树中的 **报表** 文件元素。</span><span class="sxs-lookup"><span data-stu-id="e7b58-220">On the **Format designer** page, on the **Format** tab, select the **Report** file element in the format tree.</span></span>
2. <span data-ttu-id="e7b58-221">将 **收集输出详细信息** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-221">Set the **Collect output details** option to **Yes**.</span></span> <span data-ttu-id="e7b58-222">现在，您可以使用现有报表的内容作为数据源来配置此格式，该数据源可以通过使用[数据收集](er-functions-category-data-collection.md)类别中的内置 ER 函数来访问。</span><span class="sxs-lookup"><span data-stu-id="e7b58-222">You can now configure this format by using the content of an existing report as a data source that can be accessed by using the built-in ER functions in the [Data collection](er-functions-category-data-collection.md) category.</span></span>
3. <span data-ttu-id="e7b58-223">在 **映射** 选项卡上，选择 **报表\\行** 序列元素。</span><span class="sxs-lookup"><span data-stu-id="e7b58-223">On the **Mapping** tab, select the **Report\\Lines** sequence element.</span></span>
4. <span data-ttu-id="e7b58-224">将 **收集的数据密钥名称** 表达式配置为 `WsColumn`。</span><span class="sxs-lookup"><span data-stu-id="e7b58-224">Configure the **Collected data key name** expression as `WsColumn`.</span></span>
5. <span data-ttu-id="e7b58-225">将 **收集的数据密钥值** 表达式配置为 `WsRow`。</span><span class="sxs-lookup"><span data-stu-id="e7b58-225">Configure the **Collected data key value** expression as `WsRow`.</span></span>

    ![“格式设计器”页面上的行序列元素](./media/ER-DeferredSequence-Format3.png)

6. <span data-ttu-id="e7b58-227">选择 **报表\\行\\记录\\TaxAmount** 数字元素。</span><span class="sxs-lookup"><span data-stu-id="e7b58-227">Select the **Report\\Lines\\Record\\TaxAmount** numeric element.</span></span>
7. <span data-ttu-id="e7b58-228">将 **收集的数据密钥名称** 表达式配置为 `SummingAmountKey`。</span><span class="sxs-lookup"><span data-stu-id="e7b58-228">Configure the **Collected data key name** expression as `SummingAmountKey`.</span></span>

    ![“格式设计器”页面上的 TaxAmount 数字元素](./media/ER-DeferredSequence-Format4.png)

    <span data-ttu-id="e7b58-230">您可以考虑使用此设置来实现虚拟工作表，其中单元格 A1 的值将附加来自每个已处理税收交易记录的税额值。</span><span class="sxs-lookup"><span data-stu-id="e7b58-230">You can consider this setting the fulfillment of a virtual worksheet, where the value of cell A1 is appended with the value of the tax amount from every processed tax transaction.</span></span>

8. <span data-ttu-id="e7b58-231">选择 **报表\\行\\记录\\RunningTotal** 数字元素，然后选择 **编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-231">Select the **Report\\Lines\\Record\\RunningTotal** numeric element, and then select **Edit formula**.</span></span>
9. <span data-ttu-id="e7b58-232">使用内置 [SUMIF](er-functions-datacollection-sumif.md) ER 函数配置 `SUMIF(SummingAmountKey, WsColumn, WsRow)` 表达式。</span><span class="sxs-lookup"><span data-stu-id="e7b58-232">Configure the `SUMIF(SummingAmountKey, WsColumn, WsRow)` expression by using the built-in [SUMIF](er-functions-datacollection-sumif.md) ER function.</span></span>
10. <span data-ttu-id="e7b58-233">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-233">Select **Save**.</span></span>

    ![SUMIF 表达式](./media/ER-DeferredSequence-FormulaDesigner.png)

11. <span data-ttu-id="e7b58-235">关闭 **公式设计器** 页。</span><span class="sxs-lookup"><span data-stu-id="e7b58-235">Close the **Formula designer** page.</span></span>
12. <span data-ttu-id="e7b58-236">选择 **保存**，然后选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-236">Select **Save**, and then select **Run**.</span></span>
13. <span data-ttu-id="e7b58-237">下载并查看 Web 浏览器提供的文件。</span><span class="sxs-lookup"><span data-stu-id="e7b58-237">Download and review the file that the web browser offers.</span></span>

    ![下载的文件](./media/ER-DeferredSequence-Run1.png)

    <span data-ttu-id="e7b58-239">第 21 行包含使用生成的输出作为数据源为所有已处理交易记录计算的税值累计总和。</span><span class="sxs-lookup"><span data-stu-id="e7b58-239">Line 21 contains the running total of tax values that is calculated for all processed transactions by using the generated output as a data source.</span></span> <span data-ttu-id="e7b58-240">此数据源从报表的开头开始，一直持续到最后一个税收交易记录。</span><span class="sxs-lookup"><span data-stu-id="e7b58-240">This data source starts from the beginning of the report and continues through the last tax transaction.</span></span> <span data-ttu-id="e7b58-241">第 22 行包含使用 *GroupBy* 类型数据源在模型映射中计算的所有已处理交易记录的税值总和。</span><span class="sxs-lookup"><span data-stu-id="e7b58-241">Line 22 contains the sum of the tax values for all processed transactions that are calculated in the model mapping by using the data source of the *GroupBy* type.</span></span> <span data-ttu-id="e7b58-242">请注意，这些值相等。</span><span class="sxs-lookup"><span data-stu-id="e7b58-242">Notice that these values are equal.</span></span> <span data-ttu-id="e7b58-243">因此，可以使用基于输出的求和来代替 **GroupBy**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-243">Therefore, the output-based summing can be used instead of **GroupBy**.</span></span> <span data-ttu-id="e7b58-244">通过比较第 2 行和第 21 行的执行时间，可以确定生成所有交易记录行和总和用了 9 ms。</span><span class="sxs-lookup"><span data-stu-id="e7b58-244">By comparing the execution times of lines 2 and 21, you can determine that generation of all the transactional lines and summing took 9 ms.</span></span> <span data-ttu-id="e7b58-245">因此，就生成明细行和税值总和而言，修改后的格式大约比原始格式快两倍。</span><span class="sxs-lookup"><span data-stu-id="e7b58-245">Therefore, as far as the generation of detailed lines and the summing of tax values are concerned, the modified format is approximately two times faster than the original format.</span></span>

14. <span data-ttu-id="e7b58-246">选择 **报表\\行\\汇总\\TotalTaxAmount** 数字元素，然后选择 **编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-246">Select the **Report\\Lines\\Summary\\TotalTaxAmount** numeric element, and then select **Edit formula**.</span></span>
15. <span data-ttu-id="e7b58-247">输入 `SUMIF(SummingAmountKey, WsColumn, WsRow)` 表达式而不是现有表达式。</span><span class="sxs-lookup"><span data-stu-id="e7b58-247">Enter the `SUMIF(SummingAmountKey, WsColumn, WsRow)` expression instead of the existing expression.</span></span>
16. <span data-ttu-id="e7b58-248">选择 **保存**，然后选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-248">Select **Save**, and then select **Run**.</span></span>
17. <span data-ttu-id="e7b58-249">下载并查看 Web 浏览器提供的文件。</span><span class="sxs-lookup"><span data-stu-id="e7b58-249">Download and review the file that the web browser offers.</span></span>

    ![下载的文件](./media/ER-DeferredSequence-Run2.png)

    <span data-ttu-id="e7b58-251">请注意，最后一个交易记录明细行上的税收值累计总和现在等于汇总行上的总和。</span><span class="sxs-lookup"><span data-stu-id="e7b58-251">Notice that the running total of tax values on the last transaction details line now equals the sum on the summary line.</span></span>

### <a name="put-values-of-output-based-summing-in-the-report-header"></a><span data-ttu-id="e7b58-252">将基于输出的总和的值放在报表标题中</span><span class="sxs-lookup"><span data-stu-id="e7b58-252">Put values of output-based summing in the report header</span></span>

<span data-ttu-id="e7b58-253">例如，如果您必须在报表的标题中显示税值总和，则可以修改格式。</span><span class="sxs-lookup"><span data-stu-id="e7b58-253">If, for example, you must present the sum of tax values in the header of your report, you can modify your format.</span></span>

1. <span data-ttu-id="e7b58-254">在 **格式设计器** 页面的 **格式** 选项卡上，选择 **报表\\行\\汇总** 序列元素。</span><span class="sxs-lookup"><span data-stu-id="e7b58-254">On the **Format designer** page, on the **Format** tab, select the **Report\\Lines\\Summary** sequence element.</span></span>
2. <span data-ttu-id="e7b58-255">选择 **上移**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-255">Select **Move up**.</span></span>
3. <span data-ttu-id="e7b58-256">选择 **保存**，然后选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-256">Select **Save**, and then select **Run**.</span></span>
4. <span data-ttu-id="e7b58-257">下载并查看 Web 浏览器提供的文件。</span><span class="sxs-lookup"><span data-stu-id="e7b58-257">Download and review the file that the web browser offers.</span></span>

    ![下载的文件](./media/ER-DeferredSequence-Run3.png)

    <span data-ttu-id="e7b58-259">请注意，汇总行 2 上的税收值总和现在等于 0（零），因为此总和现在是基于生成的输出计算的。</span><span class="sxs-lookup"><span data-stu-id="e7b58-259">Notice that the sum of tax values on summary line 2 now equals 0 (zero), because this sum is now calculated based on the generated output.</span></span> <span data-ttu-id="e7b58-260">生成第 2 行时，生成的输出尚不包含具有交易记录明细的行。</span><span class="sxs-lookup"><span data-stu-id="e7b58-260">When line 2 is generated, the generated output doesn't yet contain lines that have transaction details.</span></span> <span data-ttu-id="e7b58-261">您可以配置此格式以延迟执行 **报表\\行\\汇总** 序列元素，直到已经为所有税收交易记录运行了 **报表\\行\\记录** 序列元素为止。</span><span class="sxs-lookup"><span data-stu-id="e7b58-261">You can configure this format to defer the execution of the **Report\\Lines\\Summary** sequence element until the **Report\\Lines\\Record** sequence element has been run for all tax transactions.</span></span>

### <a name="defer-the-execution-of-the-summary-sequence-so-that-the-calculated-total-is-used"></a><span data-ttu-id="e7b58-262">推迟执行汇总序列，以便使用计算出的总和</span><span class="sxs-lookup"><span data-stu-id="e7b58-262">Defer the execution of the summary sequence so that the calculated total is used</span></span>

1. <span data-ttu-id="e7b58-263">在 **格式设计器** 页面的 **格式** 选项卡上，选择 **报表\\行\\汇总** 序列元素。</span><span class="sxs-lookup"><span data-stu-id="e7b58-263">On the **Format designer** page, on the **Format** tab, select the **Report\\Lines\\Summary** sequence element.</span></span>
2. <span data-ttu-id="e7b58-264">将 **推迟执行** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-264">Set the **Deferred execution** option to **Yes**.</span></span>

    ![“格式设计器”页面上“汇总”序列元素的推迟执行选项](./media/ER-DeferredSequence-Format5.png)

3. <span data-ttu-id="e7b58-266">选择 **保存**，然后选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="e7b58-266">Select **Save**, and then select **Run**.</span></span>
4. <span data-ttu-id="e7b58-267">下载并查看 Web 浏览器提供的文件。</span><span class="sxs-lookup"><span data-stu-id="e7b58-267">Download and review the file that the web browser offers.</span></span>

    ![下载的文件](./media/ER-DeferredSequence-Run4.png)

    <span data-ttu-id="e7b58-269">**报表\\行\\汇总** 序列元素现在仅在其父元素 **报表\\行** 下嵌套的所有其他项目运行之后才运行。</span><span class="sxs-lookup"><span data-stu-id="e7b58-269">The **Report\\Lines\\Summary** sequence element is now run only after all other items that are nested under its parent element, **Report\\Lines**, have been run.</span></span> <span data-ttu-id="e7b58-270">因此，它在针对 **model.Data.List** 数据源的所有税收交易记录运行 **报表\\行\\记录** 序列元素后运行。</span><span class="sxs-lookup"><span data-stu-id="e7b58-270">Therefore, it's run after the **Report\\Lines\\Record** sequence element has been run for all tax transactions of the **model.Data.List** data source.</span></span> <span data-ttu-id="e7b58-271">第 1、2 和 3 行以及最后第 22 行的执行时间揭示了这一事实。</span><span class="sxs-lookup"><span data-stu-id="e7b58-271">The execution times of lines 1, 2, and 3, and of the last line, 22, reveal this fact.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7b58-272">其他资源</span><span class="sxs-lookup"><span data-stu-id="e7b58-272">Additional resources</span></span>

- [<span data-ttu-id="e7b58-273">配置格式以执行计数和合计</span><span class="sxs-lookup"><span data-stu-id="e7b58-273">Configure format to do counting and summing</span></span>](./tasks/er-format-counting-summing-1.md)
- [<span data-ttu-id="e7b58-274">跟踪 ER 格式的执行情况以解决性能问题</span><span class="sxs-lookup"><span data-stu-id="e7b58-274">Trace execution of ER format to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="e7b58-275">推迟执行 ER 格式的 XML 元素</span><span class="sxs-lookup"><span data-stu-id="e7b58-275">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md#Example)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
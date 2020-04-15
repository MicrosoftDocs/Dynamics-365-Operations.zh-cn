---
title: 推迟执行 ER 格式的 XML 元素
description: 本主题说明如何推迟执行电子报告 (ER) 格式的 XML 元素。
author: NickSelin
manager: kfend
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58381f491cda199d77e555e5d3da04714b6a5f8f
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138915"
---
# <a name="defer-the-execution-of-xml-elements-in-er-formats"></a><span data-ttu-id="6dc33-103">推迟执行 ER 格式的 XML 元素</span><span class="sxs-lookup"><span data-stu-id="6dc33-103">Defer the execution of XML elements in ER formats</span></span>

[!include [banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="6dc33-104">概览</span><span class="sxs-lookup"><span data-stu-id="6dc33-104">Overview</span></span>

<span data-ttu-id="6dc33-105">您可以使用[电子报表 (ER)](general-electronic-reporting.md) 框架的工序设计器，以[配置](./tasks/er-format-configuration-2016-11.md)用于生成 XML 格式出站文档的 ER 解决方案的[格式组件](general-electronic-reporting.md#FormatComponentOutbound)。</span><span class="sxs-lookup"><span data-stu-id="6dc33-105">You can use the Operations designer of the [Electronic reporting (ER)](general-electronic-reporting.md) framework to [configure](./tasks/er-format-configuration-2016-11.md) the [format component](general-electronic-reporting.md#FormatComponentOutbound) of an ER solution that is used to generate outbound documents in XML format.</span></span> <span data-ttu-id="6dc33-106">配置的格式组件的层次结构由各种类型的格式元素组成。</span><span class="sxs-lookup"><span data-stu-id="6dc33-106">The hierarchical structure of the configured format component consists of format elements of various types.</span></span> <span data-ttu-id="6dc33-107">这些格式元素用于在运行时用所需的信息填充生成的文档。</span><span class="sxs-lookup"><span data-stu-id="6dc33-107">These format elements are used to fill generated documents with the required information at runtime.</span></span> <span data-ttu-id="6dc33-108">默认情况下，当您运行 ER 格式时，格式元素的运行顺序与它们在格式层次结构中的显示顺序相同：从上到下一个接一个。</span><span class="sxs-lookup"><span data-stu-id="6dc33-108">By default, when you run an ER format, the format elements are run in the same order as they are presented in the format hierarchy: one by one, from top to bottom.</span></span> <span data-ttu-id="6dc33-109">但是，在设计时，您可以更改已配置格式组件的任何 XML 元素的执行顺序。</span><span class="sxs-lookup"><span data-stu-id="6dc33-109">However, at design time, you can change the execution order for any XML elements of the configured format component.</span></span>

<span data-ttu-id="6dc33-110">通过对已配置格式的 XML 元素打开<a name="DeferredXmlElementExecution"></a>**推迟执行**选项，可以推迟（延迟）执行该元素。</span><span class="sxs-lookup"><span data-stu-id="6dc33-110">By turning on the <a name="DeferredXmlElementExecution"></a>**Deferred execution** option for an XML element in the configured format, you can defer (postpone) the execution of that element.</span></span> <span data-ttu-id="6dc33-111">在这种情况下，该元素只有在其父元素的所有其他元素都已运行后才能运行。</span><span class="sxs-lookup"><span data-stu-id="6dc33-111">In this case, the element isn't run until all other elements of its parent have been run.</span></span>

<span data-ttu-id="6dc33-112">若要了解有关此功能的详细信息，请完成本主题中的示例。</span><span class="sxs-lookup"><span data-stu-id="6dc33-112">To learn more about this feature, complete the example in this topic.</span></span>

## <a name="limitations"></a><span data-ttu-id="6dc33-113">限制</span><span class="sxs-lookup"><span data-stu-id="6dc33-113">Limitations</span></span>

<span data-ttu-id="6dc33-114">仅为 ER 格式（用于生成 XML 格式的**出站**文档）配置的 XML 元素支持**推迟执行**选项。</span><span class="sxs-lookup"><span data-stu-id="6dc33-114">The **Deferred execution** option is supported only for XML elements that are configured for an ER format that is used to generate **outbound** documents in XML format.</span></span>

<span data-ttu-id="6dc33-115">仅位于一个其他 XML 元素中的 XML 元素支持**推迟执行**选项。</span><span class="sxs-lookup"><span data-stu-id="6dc33-115">The **Deferred execution** option is supported only for XML elements that reside in only one other XML element.</span></span> <span data-ttu-id="6dc33-116">因此，它不适用于位于其他类型的格式元素中（例如位于 **XML 序列**元素中）的 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="6dc33-116">Therefore, it isn't applicable to XML elements that reside in other types of format elements (for example, in an **XML sequence** element).</span></span>

<span data-ttu-id="6dc33-117">如果**拆分文件**选项设置为**是**，则位于**通用\\文件**格式元素中的 XML 元素不支持**推迟执行**选项。</span><span class="sxs-lookup"><span data-stu-id="6dc33-117">The **Deferred execution** option isn't supported for XML elements that reside in the **Common\\File** format element when the **Split file** option is set to **Yes**.</span></span> <span data-ttu-id="6dc33-118">有关如何拆分 XML 文件的详细信息，请参阅[基于文件大小和内容数量拆分生成的 XML 文件](er-split-files.md)。</span><span class="sxs-lookup"><span data-stu-id="6dc33-118">For more information about how to split XML files, see [Split generated XML files based on file size and content quantity](er-split-files.md).</span></span>

## <a name="example-defer-the-execution-of-an-xml-element-in-an-er-format"></a><a name="Example"></a><span data-ttu-id="6dc33-119">示例：推迟执行 ER 格式的 XML 元素</span><span class="sxs-lookup"><span data-stu-id="6dc33-119">Example: Defer the execution of an XML element in an ER format</span></span>

<span data-ttu-id="6dc33-120">以下步骤说明了具有系统管理员或电子报告职能顾问[角色](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles)的用户如何配置一个 ER 格式，以包含执行顺序与格式层次结构中的执行顺序不同的 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="6dc33-120">The following steps explain how a user in the System administrator or Electronic reporting functional consultant [role](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles) can configure an ER format that contains an XML element where the order of execution differs from the order in the format hierarchy.</span></span>

<span data-ttu-id="6dc33-121">这些步骤可以在 **USMF**公司内的 Microsoft Dynamics 365 Finance 中执行。</span><span class="sxs-lookup"><span data-stu-id="6dc33-121">These steps can be performed in the **USMF** company in Microsoft Dynamics 365 Finance.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="6dc33-122">先决条件</span><span class="sxs-lookup"><span data-stu-id="6dc33-122">Prerequisites</span></span>

<span data-ttu-id="6dc33-123">若要完成本示例，您必须能够用以下角色之一访问 **USMF** 公司的 Finance：</span><span class="sxs-lookup"><span data-stu-id="6dc33-123">To complete this example, you must have access to the **USMF** company in Finance for one of the following roles:</span></span>

- <span data-ttu-id="6dc33-124">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="6dc33-124">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="6dc33-125">系统管理员</span><span class="sxs-lookup"><span data-stu-id="6dc33-125">System administrator</span></span>

<span data-ttu-id="6dc33-126">如果您尚未完成[推迟执行 ER 格式的序列元素](er-defer-sequence-element.md#Example)主题中的示例，请下载示例 ER 解决方案的以下[配置](general-electronic-reporting.md#Configuration)。</span><span class="sxs-lookup"><span data-stu-id="6dc33-126">If you haven't yet completed the example in the [Defer the execution of sequence elements in ER formats](er-defer-sequence-element.md#Example) topic, download the following [configurations](general-electronic-reporting.md#Configuration) of the sample ER solution.</span></span>

| <span data-ttu-id="6dc33-127">内容描述</span><span class="sxs-lookup"><span data-stu-id="6dc33-127">Content description</span></span>            | <span data-ttu-id="6dc33-128">文件名</span><span class="sxs-lookup"><span data-stu-id="6dc33-128">File name</span></span> |
|--------------------------------|-----------|
| <span data-ttu-id="6dc33-129">ER 数据模型配置</span><span class="sxs-lookup"><span data-stu-id="6dc33-129">ER data model configuration</span></span>    | [<span data-ttu-id="6dc33-130">Model to learn deferred elements.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="6dc33-130">Model to learn deferred elements.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="6dc33-131">ER 模型映射配置</span><span class="sxs-lookup"><span data-stu-id="6dc33-131">ER model mapping configuration</span></span> | [<span data-ttu-id="6dc33-132">Mapping to learn deferred elements.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="6dc33-132">Mapping to learn deferred elements.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

<span data-ttu-id="6dc33-133">在开始之前，您还必须将示例 ER 解决方案的以下配置下载并保存到本地计算机上。</span><span class="sxs-lookup"><span data-stu-id="6dc33-133">Before you begin, you must also download and save the following configuration of the sample ER solution to your local computer.</span></span>

| <span data-ttu-id="6dc33-134">内容描述</span><span class="sxs-lookup"><span data-stu-id="6dc33-134">Content description</span></span>     | <span data-ttu-id="6dc33-135">文件名</span><span class="sxs-lookup"><span data-stu-id="6dc33-135">File name</span></span> |
|-------------------------|-----------|
| <span data-ttu-id="6dc33-136">ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="6dc33-136">ER format configuration</span></span> | [<span data-ttu-id="6dc33-137">Format to learn deferred XML elements.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="6dc33-137">Format to learn deferred XML elements.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="import-the-sample-er-configurations"></a><span data-ttu-id="6dc33-138">导入示例 ER 配置</span><span class="sxs-lookup"><span data-stu-id="6dc33-138">Import the sample ER configurations</span></span>

1. <span data-ttu-id="6dc33-139">转到**组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-139">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6dc33-140">选择**申报配置**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-140">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="6dc33-141">在**配置**页面上，如果**用于了解推迟的元素的模型**配置在配置树中不可用，请导入 ER 数据模型配置：</span><span class="sxs-lookup"><span data-stu-id="6dc33-141">On the **Configurations** page, if the **Model to learn deferred elements** configuration isn't available in the configuration tree, import the ER data model configuration:</span></span>

    1. <span data-ttu-id="6dc33-142">选择**交换**，然后选择**从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-142">Select **Exchange**, and then select **Load from XML file**.</span></span>
    2. <span data-ttu-id="6dc33-143">选择**浏览**，找到并选择 **Model to learn deferred elements.1.xml** 文件，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-143">Select **Browse**, find and select the **Model to learn deferred elements.1.xml** file, and then select **OK**.</span></span>

4. <span data-ttu-id="6dc33-144">如果**用于了解推迟的元素的映射**配置在配置树中不可用，请导入 ER 模型映射配置：</span><span class="sxs-lookup"><span data-stu-id="6dc33-144">If the **Mapping to learn deferred elements** configuration isn't available in the configuration tree, import the ER model mapping configuration:</span></span>

    1. <span data-ttu-id="6dc33-145">选择**交换**，然后选择**从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-145">Select **Exchange**, and then select **Load from XML file**.</span></span>
    2. <span data-ttu-id="6dc33-146">选择**浏览**，找到并选择 **Mapping to learn deferred elements.1.1.xml** 文件，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-146">Select **Browse**, find and select the **Mapping to learn deferred elements.1.1.xml** file, and then select **OK**.</span></span>

5. <span data-ttu-id="6dc33-147">导入 ER 格式配置：</span><span class="sxs-lookup"><span data-stu-id="6dc33-147">Import the ER format configuration:</span></span>

    1. <span data-ttu-id="6dc33-148">选择**交换**，然后选择**从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-148">Select **Exchange**, and then select **Load from XML file**.</span></span>
    2. <span data-ttu-id="6dc33-149">选择**浏览**，找到并选择 **Format to learn deferred XML elements.1.1.xml** 文件，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-149">Select **Browse**, find and select the **Format to learn deferred XML elements.1.1.xml** file, and then select **OK**.</span></span>

6. <span data-ttu-id="6dc33-150">在配置树中，展开**用于了解推迟的元素的模型**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-150">In the configuration tree, expand **Model to learn deferred elements**.</span></span>
7. <span data-ttu-id="6dc33-151">在配置树中查看导入的 ER 配置的列表。</span><span class="sxs-lookup"><span data-stu-id="6dc33-151">Review the list of imported ER configurations in the configuration tree.</span></span>

    ![“配置”页面上导入的 ER 配置](./media/ER-DeferredXml-Configurations.png)

### <a name="activate-a-configuration-provider"></a><span data-ttu-id="6dc33-153">激活配置提供程序</span><span class="sxs-lookup"><span data-stu-id="6dc33-153">Activate a configuration provider</span></span>

1. <span data-ttu-id="6dc33-154">转到**组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-154">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6dc33-155">在**本地化配置**页上的**配置提供程序**部分中，确保列出了示例公司 Litware, Inc. (`http://www.litware.com`) 的[配置提供程序](general-electronic-reporting.md#Provider)，并将其标记为活动状态。</span><span class="sxs-lookup"><span data-stu-id="6dc33-155">On the **Localization configurations** page, in the **Configuration providers** section, make sure that the [configuration provider](general-electronic-reporting.md#Provider) for the Litware, Inc. (`http://www.litware.com`) sample company is listed, and that it's marked as active.</span></span> <span data-ttu-id="6dc33-156">如果未列出此配置提供程序，或者未将其标记为活动状态，请按照[创建一个配置提供程序，并标记其为活动状态](./tasks/er-configuration-provider-mark-it-active-2016-11.md)中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="6dc33-156">If this configuration provider isn't listed, or if it isn't marked as active, follow the steps in the [Create a configuration provider and mark it as active](./tasks/er-configuration-provider-mark-it-active-2016-11.md) topic.</span></span>

    ![“本地化配置”页面上的示例公司 Litware, Inc.](./media/ER-DeferredXml-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a><span data-ttu-id="6dc33-158">查看导入的模型映射</span><span class="sxs-lookup"><span data-stu-id="6dc33-158">Review the imported model mapping</span></span>

<span data-ttu-id="6dc33-159">查看 ER 模型映射组件的设置，该组件配置为根据请求来访问税收交易记录并公开访问的数据。</span><span class="sxs-lookup"><span data-stu-id="6dc33-159">Review the settings of the ER model mapping component that is configured to access tax transactions and expose accessed data on request.</span></span>

1. <span data-ttu-id="6dc33-160">转到**组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-160">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6dc33-161">选择**申报配置**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-161">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="6dc33-162">在**配置**页上的配置树中，展开**用于了解推迟的元素的模型**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-162">On the **Configurations** page, in the configuration tree, expand **Model to learn deferred elements**.</span></span>
4. <span data-ttu-id="6dc33-163">选择**用于了解推迟的元素的映射**配置。</span><span class="sxs-lookup"><span data-stu-id="6dc33-163">Select the **Mapping to learn deferred elements** configuration.</span></span>
5. <span data-ttu-id="6dc33-164">选择**设计器**来打开映射列表。</span><span class="sxs-lookup"><span data-stu-id="6dc33-164">Select **Designer** to open the list of mappings.</span></span>
6. <span data-ttu-id="6dc33-165">选择**设计器**查看映射详细信息。</span><span class="sxs-lookup"><span data-stu-id="6dc33-165">Select **Designer** to review the mapping details.</span></span>
7. <span data-ttu-id="6dc33-166">选择**显示详细信息**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-166">Select **Show details**.</span></span>
8. <span data-ttu-id="6dc33-167">查看配置为访问税收交易记录的数据源：</span><span class="sxs-lookup"><span data-stu-id="6dc33-167">Review the data sources that are configured to access tax transactions:</span></span>

    - <span data-ttu-id="6dc33-168">*表记录*类型的**交易记录**数据源被配置为访问 **TaxTrans** 应用程序表的记录。</span><span class="sxs-lookup"><span data-stu-id="6dc33-168">The **Transactions** data source of the *Table record* type is configured to access records of the **TaxTrans** application table.</span></span>
    - <span data-ttu-id="6dc33-169">**计算字段**类型的*凭证*数据源被配置为返回所需的凭证代码（**INV-10000349** 和 **INV-10000350**）作为记录列表。</span><span class="sxs-lookup"><span data-stu-id="6dc33-169">The **Vouchers** data source of the *Calculated field* type is configured to return the required voucher codes (**INV-10000349** and **INV-10000350**) as a list of records.</span></span>
    - <span data-ttu-id="6dc33-170">**计算字段**类型的*已筛选*数据源被配置为从**交易记录**数据源中仅选择所需凭证的税收交易记录。</span><span class="sxs-lookup"><span data-stu-id="6dc33-170">The **Filtered** data source of the *Calculated field* type is configured to select, from the **Transactions** data source, only tax transactions of the required vouchers.</span></span>
    - <span data-ttu-id="6dc33-171">为**已筛选**数据源添加了*计算字段*类型的 **\$TaxAmount** 字段，以显示具有相反符号的税收值。</span><span class="sxs-lookup"><span data-stu-id="6dc33-171">The **\$TaxAmount** field of the *Calculated field* type is added for the **Filtered** data source to expose the tax value that has the opposite sign.</span></span>
    - <span data-ttu-id="6dc33-172">**分组依据**类型的*已分组*数据源被配置为将**已筛选**数据源的已筛选税收交易记录分组。</span><span class="sxs-lookup"><span data-stu-id="6dc33-172">The **Grouped** data source of the *Group By* type is configured to group filtered tax transactions of the **Filtered** data source.</span></span>
    - <span data-ttu-id="6dc33-173">**已分组**数据源的 **TotalSum** 聚合字段被配置为针对该数据源的所有已筛选税收交易记录汇总**已筛选**数据源的 **\$TaxAmount** 字段值。</span><span class="sxs-lookup"><span data-stu-id="6dc33-173">The **TotalSum** aggregation field of the **Grouped** data source is configured to summarize values of the **\$TaxAmount** field of the **Filtered** data source for all filtered tax transactions of that data source.</span></span>

        ![“编辑‘GroupBy’参数”页面上的 TotalSum 聚合字段](./media/ER-DeferredXml-GroupByParameters.png)

9. <span data-ttu-id="6dc33-175">查看配置的数据源如何绑定到数据模型，以及它们如何公开访问的数据以使其以 ER 格式可用：</span><span class="sxs-lookup"><span data-stu-id="6dc33-175">Review how the configured data sources are bound to the data model, and how they expose accessed data to make it available in an ER format:</span></span>

    - <span data-ttu-id="6dc33-176">**已筛选**数据源已绑定到数据模型的 **Data.List** 字段。</span><span class="sxs-lookup"><span data-stu-id="6dc33-176">The **Filtered** data source is bound to the **Data.List** field of the data model.</span></span>
    - <span data-ttu-id="6dc33-177">**已筛选**数据源的 **\$TaxAmount** 字段已绑定到数据模型的 **Data.List.Value** 字段。</span><span class="sxs-lookup"><span data-stu-id="6dc33-177">The **\$TaxAmount** field of the **Filtered** data source is bound to the **Data.List.Value** field of the data model.</span></span>
    - <span data-ttu-id="6dc33-178">**已分组**数据源的 **TotalSum** 字段已绑定到数据模型的 **Data.Summary.Total** 字段。</span><span class="sxs-lookup"><span data-stu-id="6dc33-178">The **TotalSum** field of the **Grouped** data source is bound to the **Data.Summary.Total** field of the data model.</span></span>

    ![模型映射设计器页面](./media/ER-DeferredXml-ModelMapping.png)

10. <span data-ttu-id="6dc33-180">关闭**模型映射设计器**和**模型映射**页面。</span><span class="sxs-lookup"><span data-stu-id="6dc33-180">Close the **Model mapping designer** and **Model mappings** pages.</span></span>

### <a name="review-the-imported-format"></a><span data-ttu-id="6dc33-181">查看导入的格式</span><span class="sxs-lookup"><span data-stu-id="6dc33-181">Review the imported format</span></span>

1. <span data-ttu-id="6dc33-182">在**配置**页面上的配置树中，选择**用于了解延迟 XML 元素的格式**配置。</span><span class="sxs-lookup"><span data-stu-id="6dc33-182">On the **Configurations** page, in the configuration tree, select the **Format to learn deferred XML elements** configuration.</span></span>
2. <span data-ttu-id="6dc33-183">选择**设计器**查看格式详细信息。</span><span class="sxs-lookup"><span data-stu-id="6dc33-183">Select **Designer** to review the format details.</span></span>
3. <span data-ttu-id="6dc33-184">选择**显示详细信息**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-184">Select **Show details**.</span></span>
4. <span data-ttu-id="6dc33-185">查看 ER 格式组件的设置，这些设置被配置为以 XML 格式生成出站文档，其中包括税收交易记录的详细信息：</span><span class="sxs-lookup"><span data-stu-id="6dc33-185">Review the settings of the ER format components that are configured to generate an outbound document in XML format that includes details of the tax transactions:</span></span>

    - <span data-ttu-id="6dc33-186">**报表\\消息** XML 元素被配置为使用包含嵌套 XML 元素（**标题**、**记录**和**汇总**）的单个节点填充出站文档。</span><span class="sxs-lookup"><span data-stu-id="6dc33-186">The **Report\\Message** XML element is configured to fill the outbound document with a single node that includes the nested XML elements (**Header**, **Record**, and **Summary**).</span></span>
    - <span data-ttu-id="6dc33-187">**报表\\消息\\标题** XML 元素被配置为用单个标题节点填充出站文档，以显示处理的开始日期和时间。</span><span class="sxs-lookup"><span data-stu-id="6dc33-187">The **Report\\Message\\Header** XML element is configured to fill the outbound document with a single header node that shows the date and time when the processing starts.</span></span>
    - <span data-ttu-id="6dc33-188">**报表\\消息\\记录** XML 元素被配置为用显示单项税收交易记录详细信息的单个记录节点填充出站文档。</span><span class="sxs-lookup"><span data-stu-id="6dc33-188">The **Report \\Message\\Record** XML element is configured to fill the outbound document with a single record node that shows the details of a single tax transaction.</span></span>
    - <span data-ttu-id="6dc33-189">**报表\\消息\\汇总** XML 元素被配置为用包括已处理税收交易记录中税收值总计的单个汇总节点填充的出站文档。</span><span class="sxs-lookup"><span data-stu-id="6dc33-189">The **Report\\Message\\Summary** XML element is configured to fill the outbound document with a single summary node that includes the sum of the tax values from the processed tax transactions.</span></span>

    ![“格式设计器”页面上的消息 XML 元素和嵌套 XML 元素](./media/ER-DeferredXml-Format.png)

5. <span data-ttu-id="6dc33-191">在**映射**选项卡上，查看以下详细信息：</span><span class="sxs-lookup"><span data-stu-id="6dc33-191">On the **Mapping** tab, review the following details:</span></span>

    - <span data-ttu-id="6dc33-192">**报表\\消息\\标题**元素不必绑定到源即可在出站文档中生成单个节点。</span><span class="sxs-lookup"><span data-stu-id="6dc33-192">The **Report\\Message\\Header** element doesn't have to be bound to a source to generate a single node in an outbound document.</span></span>
    - <span data-ttu-id="6dc33-193">**ExecutionDateTime** 属性会生成标题节点的添加日期和时间（包括毫秒）。</span><span class="sxs-lookup"><span data-stu-id="6dc33-193">The **ExecutionDateTime** attribute generates the date and time (including milliseconds) when the header node is added.</span></span>
    - <span data-ttu-id="6dc33-194">**报表\\消息\\记录**元素已绑定到 **model.Data.List** 列表，以为绑定列表中的每条记录生成单个记录节点。</span><span class="sxs-lookup"><span data-stu-id="6dc33-194">The **Report\\Message\\Record** element is bound to the **model.Data.List** list to generate a single record node for every record from the bound list.</span></span>
    - <span data-ttu-id="6dc33-195">**TaxAmount** 属性已绑定到 **model.Data.List.Value**（在相对路径视图中显示为 **\@.Value**）以生成当前税收交易记录的税收值。</span><span class="sxs-lookup"><span data-stu-id="6dc33-195">The **TaxAmount** attribute is bound to **model.Data.List.Value** (which is shown as **\@.Value** in the relative path view) to generate the tax value of the current tax transaction.</span></span>
    - <span data-ttu-id="6dc33-196">**RunningTotal** 属性是税收值累计总额的占位符。</span><span class="sxs-lookup"><span data-stu-id="6dc33-196">The **RunningTotal** attribute is a placeholder for the running total of the tax values.</span></span> <span data-ttu-id="6dc33-197">当前，此属性没有输出，因为没有为其配置绑定或默认值。</span><span class="sxs-lookup"><span data-stu-id="6dc33-197">Currently, this attribute has no output, because neither a binding nor a default value is configured for it.</span></span>
    - <span data-ttu-id="6dc33-198">**ExecutionDateTime** 属性生成在此报表中处理当前交易时的日期和时间（包括毫秒）。</span><span class="sxs-lookup"><span data-stu-id="6dc33-198">The **ExecutionDateTime** attribute generates the date and time (including milliseconds) when the current transaction is processed in this report.</span></span>
    - <span data-ttu-id="6dc33-199">**报表\\消息\\汇总**元素不必绑定到数据源即可在出站文档中生成单个节点。</span><span class="sxs-lookup"><span data-stu-id="6dc33-199">The **Report\\Message\\Summary** element doesn't have to be bound to a data source to generate a single node in an outbound document.</span></span>
    - <span data-ttu-id="6dc33-200">**TotalTaxAmount** 属性已绑定到 **model.Data.Summary.Total** 以生成已处理税收交易记录的税收值总和。</span><span class="sxs-lookup"><span data-stu-id="6dc33-200">The **TotalTaxAmount** attribute is bound to **model.Data.Summary.Total** to generate the sum of the tax values of the processed tax transactions.</span></span>
    - <span data-ttu-id="6dc33-201">**ExecutionDateTime** 属性会生成汇总节点的添加日期和时间（包括毫秒）。</span><span class="sxs-lookup"><span data-stu-id="6dc33-201">The **ExecutionDateTime** attribute generates the date and time (including milliseconds) when the summary node is added.</span></span>

    ![“格式设计器”页上的“映射”选项卡](./media/ER-DeferredXml-Format2.png)

### <a name="run-the-imported-format"></a><span data-ttu-id="6dc33-203">运行导入的格式</span><span class="sxs-lookup"><span data-stu-id="6dc33-203">Run the imported format</span></span>

1. <span data-ttu-id="6dc33-204">在**格式设计器**页上，选择**运行**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-204">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="6dc33-205">下载 Web 浏览器提供的文件，然后将其打开以进行检查。</span><span class="sxs-lookup"><span data-stu-id="6dc33-205">Download the file that the web browser offers, and open it for review.</span></span>

    ![下载的文件](./media/ER-DeferredXml-Run.png)

<span data-ttu-id="6dc33-207">请注意，汇总节点显示了已处理交易记录的税收值总和。</span><span class="sxs-lookup"><span data-stu-id="6dc33-207">Notice that the summary node presents the sum of the tax values for the processed transactions.</span></span> <span data-ttu-id="6dc33-208">由于该格式已配置为使用 **model.Data.Summary.Total** 绑定返回此总和，所以通过调用模型映射中 **GroupBy** 类型的**已分组**数据源 *TotalSum* 汇总计算了此总和。</span><span class="sxs-lookup"><span data-stu-id="6dc33-208">Because the format is configured to use the **model.Data.Summary.Total** binding to return this sum, the sum is calculated by calling the **TotalSum** aggregation of the **Grouped** data source of the *GroupBy* type in the model mapping.</span></span> <span data-ttu-id="6dc33-209">为了计算此汇总，模型映射会在**已筛选**数据源中选择的所有交易记录上迭代。</span><span class="sxs-lookup"><span data-stu-id="6dc33-209">To calculate this aggregation, the model mapping iterates over all transactions that have been selected in the **Filtered** data source.</span></span> <span data-ttu-id="6dc33-210">通过比较汇总节点和最后一个记录节点的执行时间，可以确定计算总和用了 12 毫秒 (ms)。</span><span class="sxs-lookup"><span data-stu-id="6dc33-210">By comparing the execution times of the summary node and the last record node, you can determine that calculation of the sum took 12 milliseconds (ms).</span></span> <span data-ttu-id="6dc33-211">通过比较第一个和最后一个记录节点的执行时间，可以确定生成所有记录节点用了 9 ms。</span><span class="sxs-lookup"><span data-stu-id="6dc33-211">By comparing the execution times of the first and last record nodes, you can determine that generation of all record nodes took 9 ms.</span></span> <span data-ttu-id="6dc33-212">因此，总共需要 21 ms。</span><span class="sxs-lookup"><span data-stu-id="6dc33-212">Therefore, a total of 21 ms was required.</span></span>

### <a name="modify-the-format-so-that-the-calculation-is-based-on-generated-output"></a><span data-ttu-id="6dc33-213">修改格式，以便根据生成的输出来进行计算</span><span class="sxs-lookup"><span data-stu-id="6dc33-213">Modify the format so that the calculation is based on generated output</span></span>

<span data-ttu-id="6dc33-214">如果交易记录量远大于当前示例中的交易记录量，则计算时间可能会增加并导致性能问题。</span><span class="sxs-lookup"><span data-stu-id="6dc33-214">If the volume of transaction is much larger than the volume in the current example, the calculation time might increase and cause performance issues.</span></span> <span data-ttu-id="6dc33-215">通过更改格式设置，可以帮助防止这些性能问题。</span><span class="sxs-lookup"><span data-stu-id="6dc33-215">By changing the setting of the format, you can help prevent these performance issues.</span></span> <span data-ttu-id="6dc33-216">因为您访问税收值以将其包括在生成的报表中，所以您可以重复使用此信息来计算税收值。</span><span class="sxs-lookup"><span data-stu-id="6dc33-216">Because you access tax values to include them in the generated report, you can reuse this information to calculate tax values.</span></span> <span data-ttu-id="6dc33-217">有关更多信息，请参见[配置格式以进行计数和求和](./tasks/er-format-counting-summing-1.md)。</span><span class="sxs-lookup"><span data-stu-id="6dc33-217">For more information, see [Configure format to do counting and summing](./tasks/er-format-counting-summing-1.md).</span></span>

1. <span data-ttu-id="6dc33-218">在**格式设计师**页面上的**格式**选项卡上，选择格式树中的**报表**文件元素。</span><span class="sxs-lookup"><span data-stu-id="6dc33-218">On the **Format designer** page, on the **Format** tab, select the **Report** file element in the format tree.</span></span>
2. <span data-ttu-id="6dc33-219">将**收集输出详细信息**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-219">Set the **Collect output details** option to **Yes**.</span></span> <span data-ttu-id="6dc33-220">现在，您可以使用已生成报表的内容作为数据源来配置此格式，该数据源可以通过使用[数据收集](er-functions-category-data-collection.md)类别中的内置 ER 函数来访问。</span><span class="sxs-lookup"><span data-stu-id="6dc33-220">You can now configure this format by using the content of a generated report as a data source that can be accessed by using the built-in ER functions in the [Data collection](er-functions-category-data-collection.md) category.</span></span>
3. <span data-ttu-id="6dc33-221">在**映射**选项卡上，选择**报表\\消息\\记录** XML 元素。</span><span class="sxs-lookup"><span data-stu-id="6dc33-221">On the **Mapping** tab, select the **Report\\Message\\Record** XML element.</span></span>
4. <span data-ttu-id="6dc33-222">将**收集的数据密钥名称**表达式配置为 `WsColumn`。</span><span class="sxs-lookup"><span data-stu-id="6dc33-222">Configure the **Collected data key name** expression as `WsColumn`.</span></span>
5. <span data-ttu-id="6dc33-223">将**收集的数据密钥值**表达式配置为 `WsRow`。</span><span class="sxs-lookup"><span data-stu-id="6dc33-223">Configure the **Collected data key value** expression as `WsRow`.</span></span>

    ![“格式设计器”页面上的记录 XML 元素](./media/ER-DeferredXml-Format3.png)

6. <span data-ttu-id="6dc33-225">选择**报表\\消息\\记录\\TaxAmount** 属性。</span><span class="sxs-lookup"><span data-stu-id="6dc33-225">Select the **Report\\Message\\Record\\TaxAmount** attribute.</span></span>
7. <span data-ttu-id="6dc33-226">将**收集的数据密钥名称**表达式配置为 `SummingAmountKey`。</span><span class="sxs-lookup"><span data-stu-id="6dc33-226">Configure the **Collected data key name** expression as `SummingAmountKey`.</span></span>

    ![“格式设计器”页面上的 TaxAmount 属性](./media/ER-DeferredXml-Format4.png)

    <span data-ttu-id="6dc33-228">您可以考虑使用此设置来实现虚拟工作表，其中单元格 A1 的值将附加来自每个已处理税收交易记录的税额值。</span><span class="sxs-lookup"><span data-stu-id="6dc33-228">You can consider this setting the fulfillment of a virtual worksheet, where the value of cell A1 is appended with the value of the tax amount from every processed tax transaction.</span></span>

8. <span data-ttu-id="6dc33-229">选择**报表\\消息\\记录\\RunningTotal** 属性，然后选择**编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-229">Select the **Report\\Message\\Record\\RunningTotal** attribute, and then select **Edit formula**.</span></span>
9. <span data-ttu-id="6dc33-230">使用内置 [SUMIF](er-functions-datacollection-sumif.md) ER 函数配置 `SUMIF(SummingAmountKey, WsColumn, WsRow)` 表达式，然后选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-230">Configure the `SUMIF(SummingAmountKey, WsColumn, WsRow)` expression by using the built-in [SUMIF](er-functions-datacollection-sumif.md) ER function, and then select **Save**.</span></span>

    ![SUMIF 表达式](./media/ER-DeferredXml-FormulaDesigner.png)

10. <span data-ttu-id="6dc33-232">关闭**公式设计器**页。</span><span class="sxs-lookup"><span data-stu-id="6dc33-232">Close the **Formula designer** page.</span></span>
11. <span data-ttu-id="6dc33-233">选择**保存**，然后选择**运行**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-233">Select **Save**, and then select **Run**.</span></span>
12. <span data-ttu-id="6dc33-234">下载并查看 Web 浏览器提供的文件。</span><span class="sxs-lookup"><span data-stu-id="6dc33-234">Download and review the file that the web browser offers.</span></span>

    ![下载的文件](./media/ER-DeferredXml-Run1.png)

    <span data-ttu-id="6dc33-236">最后一个记录节点包含使用生成的输出作为数据源为所有已处理交易记录计算的税值累计总和。</span><span class="sxs-lookup"><span data-stu-id="6dc33-236">The last record node contains the running total of tax values that is calculated for all processed transactions by using the generated output as a data source.</span></span> <span data-ttu-id="6dc33-237">此数据源从报表的开头开始，一直持续到最后一个税收交易记录。</span><span class="sxs-lookup"><span data-stu-id="6dc33-237">This data source starts from the beginning of the report and continues through the last tax transaction.</span></span> <span data-ttu-id="6dc33-238">汇总节点包含使用 *GroupBy* 类型数据源在模型映射中计算的所有已处理交易记录的税值总和。</span><span class="sxs-lookup"><span data-stu-id="6dc33-238">The summary node contains the sum of the tax values for all processed transactions that are calculated in the model mapping by using the data source of the *GroupBy* type.</span></span> <span data-ttu-id="6dc33-239">请注意，这些值相等。</span><span class="sxs-lookup"><span data-stu-id="6dc33-239">Notice that these values are equal.</span></span> <span data-ttu-id="6dc33-240">因此，可以使用基于输出的求和来代替 **GroupBy**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-240">Therefore, the output-based summing can be used instead of **GroupBy**.</span></span> <span data-ttu-id="6dc33-241">通过比较第一个记录节点和汇总节点的执行时间，可以确定生成所有记录节点并进行汇总用了 11 ms。</span><span class="sxs-lookup"><span data-stu-id="6dc33-241">By comparing the execution times of the first record node and the summary node, you can determine that generation of all the record nodes and summing took 11 ms.</span></span> <span data-ttu-id="6dc33-242">因此，就生成记录节点和税值总和而言，修改后的格式大约比原始格式快两倍。</span><span class="sxs-lookup"><span data-stu-id="6dc33-242">Therefore, as far as the generation of record nodes and the summing of tax values are concerned, the modified format is approximately two times faster than the original format.</span></span>

13. <span data-ttu-id="6dc33-243">选择**报表\\消息\\汇总\\TotalTaxAmount** 属性，然后选择**编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-243">Select the **Report\\Message\\Summary\\TotalTaxAmount** attribute, and then select **Edit formula**.</span></span>
14. <span data-ttu-id="6dc33-244">输入 `SUMIF(SummingAmountKey, WsColumn, WsRow)` 表达式而不是现有表达式。</span><span class="sxs-lookup"><span data-stu-id="6dc33-244">Enter the `SUMIF(SummingAmountKey, WsColumn, WsRow)` expression instead of the existing expression.</span></span>
15. <span data-ttu-id="6dc33-245">选择**保存**，然后选择**运行**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-245">Select **Save**, and then select **Run**.</span></span>
16. <span data-ttu-id="6dc33-246">下载并查看 Web 浏览器提供的文件。</span><span class="sxs-lookup"><span data-stu-id="6dc33-246">Download and review the file that the web browser offers.</span></span>

    ![下载的文件](./media/ER-DeferredXml-Run2.png)

    <span data-ttu-id="6dc33-248">请注意，最后一个记录节点中的税收值累计总和现在等于汇总节点上的总和。</span><span class="sxs-lookup"><span data-stu-id="6dc33-248">Notice that the running total of tax values in the last record node now equals the sum in the summary node.</span></span>

### <a name="put-values-of-output-based-summing-in-the-report-header"></a><span data-ttu-id="6dc33-249">将基于输出的总和的值放在报表标题中</span><span class="sxs-lookup"><span data-stu-id="6dc33-249">Put values of output-based summing in the report header</span></span>

<span data-ttu-id="6dc33-250">例如，如果您必须在报表的标题中显示税值总和，则可以修改格式。</span><span class="sxs-lookup"><span data-stu-id="6dc33-250">If, for example, you must present the sum of tax values in the header of your report, you can modify your format.</span></span>

1. <span data-ttu-id="6dc33-251">在**格式设计器**页面的**格式**选项卡上，选择**报表\\消息\\汇总** XML 元素。</span><span class="sxs-lookup"><span data-stu-id="6dc33-251">On the **Format designer** page, on the **Format** tab, select the **Report\\Message\\Summary** XML element.</span></span>
2. <span data-ttu-id="6dc33-252">选择**上移**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-252">Select **Move up**.</span></span>
3. <span data-ttu-id="6dc33-253">选择**保存**，然后选择**运行**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-253">Select **Save**, and then select **Run**.</span></span>
4. <span data-ttu-id="6dc33-254">下载并查看 Web 浏览器提供的文件。</span><span class="sxs-lookup"><span data-stu-id="6dc33-254">Download and review the file that the web browser offers.</span></span>

    ![下载的文件](./media/ER-DeferredXml-Run3.png)

    <span data-ttu-id="6dc33-256">请注意，汇总节点中的税收值总和现在等于 0（零），因为此总和现在是基于生成的输出计算的。</span><span class="sxs-lookup"><span data-stu-id="6dc33-256">Notice that the sum of tax values in the summary node now equals 0 (zero), because this sum is now calculated based on the generated output.</span></span> <span data-ttu-id="6dc33-257">生成第一个记录节点时，生成的输出尚不包含具有交易记录明细的记录节点。</span><span class="sxs-lookup"><span data-stu-id="6dc33-257">When the first record node is generated, the generated output doesn't yet contain record nodes that have transaction details.</span></span> <span data-ttu-id="6dc33-258">您可以配置此格式以延迟执行**报表\\消息\\汇总**元素，直到已经为所有税收交易记录运行了**报表\\消息\\记录**元素为止。</span><span class="sxs-lookup"><span data-stu-id="6dc33-258">You can configure this format to defer the execution of the **Report\\Message\\Summary** element until the **Report\\Message\\Record** element has been run for all tax transactions.</span></span>

### <a name="defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used"></a><span data-ttu-id="6dc33-259">推迟执行汇总 XML 元素，以便使用计算出的总和</span><span class="sxs-lookup"><span data-stu-id="6dc33-259">Defer the execution of the summary XML element so that the calculated total is used</span></span>

1. <span data-ttu-id="6dc33-260">在**格式设计器**页面的**格式**选项卡上，选择**报表\\消息\\汇总** XML 元素。</span><span class="sxs-lookup"><span data-stu-id="6dc33-260">On the **Format designer** page, on the **Format** tab, select the **Report\\Message\\Summary** XML element.</span></span>
2. <span data-ttu-id="6dc33-261">将**推迟执行**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-261">Set the **Deferred execution** option to **Yes**.</span></span>

    ![“格式设计器”页面上“汇总”XML 元素的推迟执行选项](./media/ER-DeferredXml-Format5.png)

3. <span data-ttu-id="6dc33-263">选择**保存**，然后选择**运行**。</span><span class="sxs-lookup"><span data-stu-id="6dc33-263">Select **Save**, and then select **Run**.</span></span>
4. <span data-ttu-id="6dc33-264">下载并查看 Web 浏览器提供的文件。</span><span class="sxs-lookup"><span data-stu-id="6dc33-264">Download and review the file that the web browser offers.</span></span>

    ![下载的文件](./media/ER-DeferredXml-Run4.png)

    <span data-ttu-id="6dc33-266">**报表\\消息\\汇总**元素现在仅在其父元素**报表\\消息**下嵌套的所有其他项目运行之后才运行。</span><span class="sxs-lookup"><span data-stu-id="6dc33-266">The **Report\\Message\\Summary** element is now run only after all other items that are nested under its parent element, **Report\\Message**, have been run.</span></span> <span data-ttu-id="6dc33-267">因此，它在针对 **model.Data.List** 数据源的所有税收交易记录运行**报表\\消息\\记录**元素后运行。</span><span class="sxs-lookup"><span data-stu-id="6dc33-267">Therefore, it's run after the **Report\\Message\\Record** element has been run for all tax transactions of the **model.Data.List** data source.</span></span> <span data-ttu-id="6dc33-268">第一个和最后一个记录节点的执行时间以及标题和汇总节点的执行时间揭示了这一事实。</span><span class="sxs-lookup"><span data-stu-id="6dc33-268">The execution times of the first and last record nodes, and of the header and summary nodes, reveal this fact.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6dc33-269">其他资源</span><span class="sxs-lookup"><span data-stu-id="6dc33-269">Additional resources</span></span>

- [<span data-ttu-id="6dc33-270">配置格式以执行计数和合计</span><span class="sxs-lookup"><span data-stu-id="6dc33-270">Configure format to do counting and summing</span></span>](./tasks/er-format-counting-summing-1.md)
- [<span data-ttu-id="6dc33-271">跟踪 ER 格式的执行情况以解决性能问题</span><span class="sxs-lookup"><span data-stu-id="6dc33-271">Trace execution of ER format to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="6dc33-272">推迟执行 ER 格式的序列元素</span><span class="sxs-lookup"><span data-stu-id="6dc33-272">Defer the execution of sequence elements in ER formats</span></span>](er-defer-sequence-element.md#Example)

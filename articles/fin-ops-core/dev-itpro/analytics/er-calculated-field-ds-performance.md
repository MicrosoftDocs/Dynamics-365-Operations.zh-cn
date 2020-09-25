---
title: 通过添加参数化的计算字段数据源提高 ER 解决方案的性能
description: 此主题介绍如何通过添加参数化的计算字段数据源提高电子申报 (ER) 解决方案的性能。
author: NickSelin
manager: AnnBe
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a87098e82284a4951f3a4de050f6ba3f587fd20a
ms.sourcegitcommit: 5472005274f2f94fba82dda90de128f39d8b8390
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760074"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a><span data-ttu-id="adee0-103">通过添加参数化的计算字段数据源提高 ER 解决方案的性能</span><span class="sxs-lookup"><span data-stu-id="adee0-103">Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="adee0-104">此主题介绍如何通过配置参数化的**计算字段**数据源，对使用的[电子申报 (ER)](general-electronic-reporting.md) 格式进行[性能跟踪](trace-execution-er-troubleshoot-perf.md)，然后使用这些跟踪的信息帮助提高性能。</span><span class="sxs-lookup"><span data-stu-id="adee0-104">This topic explains how you can take [performance traces](trace-execution-er-troubleshoot-perf.md) of [Electronic reporting (ER)](general-electronic-reporting.md) formats that are run, and then use the information from those traces to help improve performance by configuring a parameterized **Calculated field** data source.</span></span>

<span data-ttu-id="adee0-105">在设计 ER 配置以生成业务文档的过程中，您将定义用于从应用程序检索数据并在生成的输出中输入的方法。</span><span class="sxs-lookup"><span data-stu-id="adee0-105">As part of the process of designing ER configurations to generate business documents, you define the method that is used to retrieve data from the application and enter it in the generated output.</span></span> <span data-ttu-id="adee0-106">通过设计**计算字段**类型的参数化 ER 数据源，可以减少数据库调用数量，从而减少收集 ER 格式执行详细信息所需时间和成本。</span><span class="sxs-lookup"><span data-stu-id="adee0-106">By designing a parametrized ER data source of the **Calculated field** type, you can reduce the number of database calls, and significantly reduce the time and cost that are involved in collecting the details of ER format execution.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="adee0-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="adee0-107">Prerequisites</span></span>

- <span data-ttu-id="adee0-108">要完成本主题中的示例，您必须具有以下其中一个[角色](../sysadmin/tasks/assign-users-security-roles.md)的访问权限：</span><span class="sxs-lookup"><span data-stu-id="adee0-108">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="adee0-109">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="adee0-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="adee0-110">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="adee0-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="adee0-111">系统管理员</span><span class="sxs-lookup"><span data-stu-id="adee0-111">System administrator</span></span>

- <span data-ttu-id="adee0-112">公司必须设置为 **DEMF**。</span><span class="sxs-lookup"><span data-stu-id="adee0-112">The company must be set to **DEMF**.</span></span>
- <span data-ttu-id="adee0-113">执行本主题的[附录 1](#appendix1) 中的步骤，以下载完成本主题中的示例所需的示例 Microsoft ER 解决方案的组件。</span><span class="sxs-lookup"><span data-stu-id="adee0-113">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the sample Microsoft ER solution that is required to complete the examples in this topic.</span></span>
- <span data-ttu-id="adee0-114">执行本主题的[附录 2](#appendix2) 中的步骤，以配置使用 ER 框架提高示例 Microsoft ER 解决方案性能所需的最少 ER 参数。</span><span class="sxs-lookup"><span data-stu-id="adee0-114">Follow the steps in [Appendix 2](#appendix2) of this topic to configure the minimal set of ER parameters that is required to use the ER framework to help improve the performance of the sample Microsoft ER solution.</span></span>

## <a name="import-the-sample-er-solution"></a><span data-ttu-id="adee0-115">导入示例 ER 解决方案</span><span class="sxs-lookup"><span data-stu-id="adee0-115">Import the sample ER solution</span></span>

<span data-ttu-id="adee0-116">假设必须设计一种 ER 解决方案来生成新报表以显示供应商交易记录。</span><span class="sxs-lookup"><span data-stu-id="adee0-116">Imagine that you must design an ER solution to generate a new report that shows vendor transactions.</span></span> <span data-ttu-id="adee0-117">现在，您可以在**供应商交易记录**页（转至**应付帐款** \> **供应商** \> **所有供应商**，选择供应商，然后在操作窗格中**供应商**选项卡上**交易记录**组中选择**交易记录**）中找到所选供应商的交易记录。</span><span class="sxs-lookup"><span data-stu-id="adee0-117">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable** \> **Vendors** \> **All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="adee0-118">但是，您希望让所有供应商交易记录都包含在一个 XML 格式的电子申报文档中。</span><span class="sxs-lookup"><span data-stu-id="adee0-118">However, you want to have all vendor transactions together in one electronic document in XML format.</span></span> <span data-ttu-id="adee0-119">此解决方案将由多个 ER 配置构成，这些配置中包含所需数据模型、模型映射和格式组件。</span><span class="sxs-lookup"><span data-stu-id="adee0-119">This solution will consist of several ER configurations that contain the required data model, model mapping, and format components.</span></span>

<span data-ttu-id="adee0-120">第一步是导入示例 ER 解决方案以生成供应商交易记录报表。</span><span class="sxs-lookup"><span data-stu-id="adee0-120">The first step is to import the sample ER solution to generate a vendor transactions report.</span></span>

1. <span data-ttu-id="adee0-121">登录为贵公司预配的 Microsoft Dynamics 365 Finance 实例。</span><span class="sxs-lookup"><span data-stu-id="adee0-121">Sign in to the instance of Microsoft Dynamics 365 Finance that is provisioned for your company.</span></span>
2. <span data-ttu-id="adee0-122">在此主题中，将为示例公司 **Litware, Inc.** 创建并修改配置。</span><span class="sxs-lookup"><span data-stu-id="adee0-122">In this topic, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="adee0-123">请确保已经将该配置提供程序添加到了您的 Finance 实例并标记为有效。</span><span class="sxs-lookup"><span data-stu-id="adee0-123">Make sure that this configuration provider has been added to your Finance instance and is marked as active.</span></span> <span data-ttu-id="adee0-124">有关详细信息，请参阅[创建配置提供程序并将其标记为有效](tasks/er-configuration-provider-mark-it-active-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="adee0-124">For more information, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="adee0-125">在**电子申报**工作区中，选择**报告配置**磁贴。</span><span class="sxs-lookup"><span data-stu-id="adee0-125">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="adee0-126">在**配置**页中，按照下面的顺序将作为先决条件下载的 ER 配置导入 Finance 中：数据模型、模型映射、格式。</span><span class="sxs-lookup"><span data-stu-id="adee0-126">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into Finance, in the following order: data model, model mapping, format.</span></span> <span data-ttu-id="adee0-127">为每个配置执行下列步骤:</span><span class="sxs-lookup"><span data-stu-id="adee0-127">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="adee0-128">在操作窗格上，选择**交换** \> **从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="adee0-128">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="adee0-129">选择**浏览**并为 ER 配置选择 XML 格式的相应文件。</span><span class="sxs-lookup"><span data-stu-id="adee0-129">Select **Browse**, and select the appropriate file for the ER configuration in XML format.</span></span>
    3. <span data-ttu-id="adee0-130">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="adee0-130">Select **OK**.</span></span>

![“配置”页面上导入的配置](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a><span data-ttu-id="adee0-132">检查示例 ER 解决方案</span><span class="sxs-lookup"><span data-stu-id="adee0-132">Review the sample ER solution</span></span>

### <a name="review-the-model-mapping"></a><span data-ttu-id="adee0-133">查看模型映射</span><span class="sxs-lookup"><span data-stu-id="adee0-133">Review the model mapping</span></span>

1. <span data-ttu-id="adee0-134">在**配置**页的配置树中，展开**性能改进模型**，然后选择**性能改进映射**。</span><span class="sxs-lookup"><span data-stu-id="adee0-134">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="adee0-135">在操作窗格上，选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="adee0-135">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="adee0-136">在**模型到数据源映射**页面的操作窗格中，选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="adee0-136">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>

    <span data-ttu-id="adee0-137">此 ER 模型映射用于执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="adee0-137">This ER model mapping is designed to perform the following actions:</span></span>

    - <span data-ttu-id="adee0-138">提取 VendTrans 表中存储的供应商交易记录列表（**Trans** 数据源）。</span><span class="sxs-lookup"><span data-stu-id="adee0-138">Fetch the list of vendor transactions that are stored in the VendTrans table (**Trans** data source).</span></span>
    - <span data-ttu-id="adee0-139">对于每笔交易记录，从 VendTable 表提取已经为其过帐的供应商的记录（**\#Vend** 数据源）。</span><span class="sxs-lookup"><span data-stu-id="adee0-139">For every transaction, fetch, from the VendTable table, the record of a vendor that the transaction has been posted for (**\#Vend** data source).</span></span>

    > [!NOTE]
    > <span data-ttu-id="adee0-140">**\#Vend** 数据源配置为使用现有的多对一关系 **\@.'\>Relations'.VendTable\_AccountNum** 提取对应的供应商记录。</span><span class="sxs-lookup"><span data-stu-id="adee0-140">The **\#Vend** data source is configured to fetch the corresponding vendor record by using the existing many-to-one relation **\@.'\>Relations'.VendTable\_AccountNum**.</span></span>

    <span data-ttu-id="adee0-141">此配置中的模型映射实施为此模型创建并在 Finance 中运行的任何 ER 格式的基本数据模型。</span><span class="sxs-lookup"><span data-stu-id="adee0-141">The model mapping in this configuration implements the base data model for any ER formats that are created for this model and run in Finance.</span></span> <span data-ttu-id="adee0-142">因此，**Trans** 数据源的内容将对抽象 **model** 数据源之类 ER 格式公开。</span><span class="sxs-lookup"><span data-stu-id="adee0-142">Therefore, the content of the **Trans** data source is exposed for ER formats such as abstract **model** data sources.</span></span>

    ![“模型映射设计器”页面中的 Trans 数据源](media/er-calculated-field-ds-performance-mapping-1.png)

4. <span data-ttu-id="adee0-144">关闭**模型映射设计器**页。</span><span class="sxs-lookup"><span data-stu-id="adee0-144">Close the **Model mapping designer** page.</span></span>
5. <span data-ttu-id="adee0-145">关闭**模型到数据源映射**页。</span><span class="sxs-lookup"><span data-stu-id="adee0-145">Close the **Model to datasource mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="adee0-146">查看格式</span><span class="sxs-lookup"><span data-stu-id="adee0-146">Review format</span></span>

1. <span data-ttu-id="adee0-147">在**配置**页的配置树中，展开**性能改进模型**，然后选择**性能改进格式**。</span><span class="sxs-lookup"><span data-stu-id="adee0-147">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement format**.</span></span>
2. <span data-ttu-id="adee0-148">在操作窗格上，选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="adee0-148">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="adee0-149">在**格式设计器**页中**映射**选项卡上，选择**展开/折叠**。</span><span class="sxs-lookup"><span data-stu-id="adee0-149">On the **Format designer** page, on the **Mapping** tab, select **Expand/Collapse**.</span></span>
4. <span data-ttu-id="adee0-150">展开**模型**、**数据**和**交易记录**项。</span><span class="sxs-lookup"><span data-stu-id="adee0-150">Expand the **Model**, **Data,** and **Transaction** items.</span></span>

    <span data-ttu-id="adee0-151">此 ER 格式用于生成 XML 格式的供应商交易记录报表。</span><span class="sxs-lookup"><span data-stu-id="adee0-151">This ER format is designed to generate a vendor transactions report in XML format.</span></span>

    ![“格式设计器”页面中的 Format 数据源和配置的格式元素绑定](media/er-calculated-field-ds-performance-format.png)

5. <span data-ttu-id="adee0-153">关闭**格式设计器**页。</span><span class="sxs-lookup"><span data-stu-id="adee0-153">Close the **Format designer** page.</span></span>

## <a name="run-the-sample-er-solution-to-trace-execution"></a><span data-ttu-id="adee0-154">运行示例 ER 解决方案以跟踪执行情况</span><span class="sxs-lookup"><span data-stu-id="adee0-154">Run the sample ER solution to trace execution</span></span>

<span data-ttu-id="adee0-155">假设您已经完成了 ER 解决方案第一版的设计。</span><span class="sxs-lookup"><span data-stu-id="adee0-155">Imagine that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="adee0-156">现在希望在 Finance 实例中测试解决方案并分析执行性能。</span><span class="sxs-lookup"><span data-stu-id="adee0-156">You now want to test the solution in your Finance instance and analyze the execution performance.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="adee0-157">开启 ER 性能跟踪</span><span class="sxs-lookup"><span data-stu-id="adee0-157">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="adee0-158">选择 **DEMF** 公司。</span><span class="sxs-lookup"><span data-stu-id="adee0-158">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="adee0-159">执行[开启 ER 性能跟踪](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace)中的步骤，以便在运行 ER 格式时生成性能跟踪。</span><span class="sxs-lookup"><span data-stu-id="adee0-159">Follow the steps in [Turn on the ER performance trace](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) to generate a performance trace while an ER format is run.</span></span>

    ![“用户参数”选项卡](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a><span data-ttu-id="adee0-161">运行 ER 格式</span><span class="sxs-lookup"><span data-stu-id="adee0-161">Run the ER format</span></span>

1. <span data-ttu-id="adee0-162">转到**组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="adee0-162">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="adee0-163">在**配置**页的配置树中，选择**性能改进格式**。</span><span class="sxs-lookup"><span data-stu-id="adee0-163">On the **Configurations** page, in the configuration tree, select **Performance improvement format**.</span></span>
3. <span data-ttu-id="adee0-164">在操作窗格上，选择**运行**。</span><span class="sxs-lookup"><span data-stu-id="adee0-164">On the Action Pane, select **Run**.</span></span>

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a><span data-ttu-id="adee0-165">使用性能跟踪分析模型映射性能</span><span class="sxs-lookup"><span data-stu-id="adee0-165">Use the performance trace to analyze model mapping performance</span></span>

1. <span data-ttu-id="adee0-166">在**配置**页的配置树中，选择**性能改进映射**。</span><span class="sxs-lookup"><span data-stu-id="adee0-166">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="adee0-167">在操作窗格上，选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="adee0-167">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="adee0-168">在**模型映射**页面的操作窗格中，选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="adee0-168">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="adee0-169">在**模型映射设计器**页的操作窗格上，选择**性能跟踪**。</span><span class="sxs-lookup"><span data-stu-id="adee0-169">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="adee0-170">选择最近生成的跟踪，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="adee0-170">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="adee0-171">新信息现在可用于当前模型映射的部分数据源项：</span><span class="sxs-lookup"><span data-stu-id="adee0-171">New information is now available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="adee0-172">使用数据源获取数据实际所用时间</span><span class="sxs-lookup"><span data-stu-id="adee0-172">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="adee0-173">表示为占运行整个模型映射所用时间总量的百分比的相同时间</span><span class="sxs-lookup"><span data-stu-id="adee0-173">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

![“模型映射设计器”页面上的执行时间详细信息](./media/er-calculated-field-ds-performance-mapping-2.png)

<span data-ttu-id="adee0-175">**性能统计信息**网格显示 **Trans** 数据源调用一次 VendTrans 表。</span><span class="sxs-lookup"><span data-stu-id="adee0-175">The **Performance statistics** grid shows that the **Trans** data source calls the VendTrans table one time.</span></span> <span data-ttu-id="adee0-176">**Trans** 数据源的值 **\[265\]\[Q:265\]** 说明已从应用程序表提取了 265 笔供应商交易记录并返回到了数据模型。</span><span class="sxs-lookup"><span data-stu-id="adee0-176">The value **\[265\]\[Q:265\]** of the **Trans** data source indicates that 265 vendor transactions have been fetched from the application table and returned to the data model.</span></span>

<span data-ttu-id="adee0-177">**性能统计信息**网格显示运行 **\#Vend** 数据源时当前模型映射复制了数据源请求。</span><span class="sxs-lookup"><span data-stu-id="adee0-177">The **Performance statistics** grid also shows that the current model mapping duplicates database requests while the **\#Vend** data source is run.</span></span> <span data-ttu-id="adee0-178">执行此项复制是因为：</span><span class="sxs-lookup"><span data-stu-id="adee0-178">This duplication occurs for the following reasons:</span></span>

- <span data-ttu-id="adee0-179">将为这 265 个迭代供应商交易记录中的每一个调用供应商表两次，总计调用 530 次：</span><span class="sxs-lookup"><span data-stu-id="adee0-179">The vendor table is called two times for each of the 265 iterated vendor transactions, for a total of 530 calls:</span></span>

    - <span data-ttu-id="adee0-180">调用一次以输入供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="adee0-180">One call is made to enter the vendor account number.</span></span>
    - <span data-ttu-id="adee0-181">调用一次以输入供应商名称。</span><span class="sxs-lookup"><span data-stu-id="adee0-181">One call is made to enter the vendor name.</span></span>

- <span data-ttu-id="adee0-182">将为每个迭代供应商记录调用供应商表，即使已经仅为五个供应商过帐了提取的交易记录也不例外。</span><span class="sxs-lookup"><span data-stu-id="adee0-182">The vendor table is called for each iterated vendor transaction, even though the fetched transactions have been posted for only five vendors.</span></span> <span data-ttu-id="adee0-183">这 530 个调用中的 525 是重复的。</span><span class="sxs-lookup"><span data-stu-id="adee0-183">Of the 530 calls, 525 are duplicates.</span></span> <span data-ttu-id="adee0-184">下图显示收到的有关重复调用（数据库请求）的消息。</span><span class="sxs-lookup"><span data-stu-id="adee0-184">The following illustration shows the message that you receive about duplicate calls (database requests).</span></span>

![“模型映射设计器”页上有关重复数据库请求的消息](./media/er-calculated-field-ds-performance-mapping-2a.png)

<span data-ttu-id="adee0-186">请注意，已使用了模型映射总执行时间（大约八秒）中超过 80%（大约六秒）从 VendTable 应用程序表检索值。</span><span class="sxs-lookup"><span data-stu-id="adee0-186">Of the total model mapping execution time (approximately eight seconds), notice that more than 80 percent (approximately six seconds) has been spent retrieving values from the VendTable application table.</span></span> <span data-ttu-id="adee0-187">与 VendTrans 应用程序表中的信息量相比，此百分比对于五个供应商的两个属性而言太大。</span><span class="sxs-lookup"><span data-stu-id="adee0-187">That percentage is too large for two attributes of five vendors, compared with the volume of information from the VendTrans application table.</span></span>

<span data-ttu-id="adee0-188">若要减少为获取每个交易记录的供应商详细信息需要进行的调用数量和提高模型映射性能，可对 **\#Vend** 数据源使用缓存。</span><span class="sxs-lookup"><span data-stu-id="adee0-188">To reduce the number of calls that are made to get the vendor details for every transaction, and to improve the performance of the model mapping, you can use caching for the **\#Vend** data source.</span></span>

> [!NOTE]
> <span data-ttu-id="adee0-189">运行时，将在 **Trans** 数据源的当前交易记录范围中缓存 **Trans\\\#Vend** 数据源。</span><span class="sxs-lookup"><span data-stu-id="adee0-189">The **Trans\\\#Vend** data source will be cached in the scope of the current transaction of the **Trans** data source at runtime.</span></span>

<span data-ttu-id="adee0-190">可通过缓存 **\#Vend** 将重复调用数量从 525 减少到 260，但是不能完全消除重复。</span><span class="sxs-lookup"><span data-stu-id="adee0-190">By caching the **\#Vend** data source, you reduce the number of duplicated calls from 525 to 260, but you don't completely eliminate the duplication.</span></span> <span data-ttu-id="adee0-191">若要完全消除重复，可以配置**计算字段**类型的新参数化数据源。</span><span class="sxs-lookup"><span data-stu-id="adee0-191">To completely eliminate duplication, you can configure a new parameterized data source of the **Calculated field** type.</span></span>

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="adee0-192">根据来自执行跟踪的信息改善模型映射</span><span class="sxs-lookup"><span data-stu-id="adee0-192">Improve the model mapping based on information from the execution trace</span></span>

### <a name="change-the-logic-of-the-model-mapping"></a><span data-ttu-id="adee0-193">更改模型映射的逻辑</span><span class="sxs-lookup"><span data-stu-id="adee0-193">Change the logic of the model mapping</span></span>

<span data-ttu-id="adee0-194">执行以下步骤以使用缓存和**计算字段**类型的数据源避免重复调用数据库。</span><span class="sxs-lookup"><span data-stu-id="adee0-194">Follow these steps to use caching and a data source of the **Calculated field** type, to help prevent duplicate calls to the database.</span></span>

1. <span data-ttu-id="adee0-195">在**配置**页的配置树中，选择**性能改进映射**。</span><span class="sxs-lookup"><span data-stu-id="adee0-195">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="adee0-196">在操作窗格上，选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="adee0-196">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="adee0-197">在**模型映射**页面的操作窗格中，选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="adee0-197">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="adee0-198">在**模型映射设计器**页面上，执行以下步骤添加**表记录**类型的数据源以访问 VendTable 应用程序表中的记录：</span><span class="sxs-lookup"><span data-stu-id="adee0-198">On the **Model mapping designer** page, follow these steps to add a data source of the **Table records** type to access records in the VendTable application table:</span></span>

    1. <span data-ttu-id="adee0-199">在**数据源类型**窗格中，展开 **Dynamics 365 for Operations**，然后选择**表记录**。</span><span class="sxs-lookup"><span data-stu-id="adee0-199">In the **Data source types** pane, expand **Dynamics 365 for Operations**, and select **Table records**.</span></span>
    2. <span data-ttu-id="adee0-200">选择**添加根**。</span><span class="sxs-lookup"><span data-stu-id="adee0-200">Select **Add root**.</span></span>
    3. <span data-ttu-id="adee0-201">在对话框的**名称**字段中，输入 **Vend**。</span><span class="sxs-lookup"><span data-stu-id="adee0-201">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    4. <span data-ttu-id="adee0-202">在**表**字段中，输入 **VendTable**。</span><span class="sxs-lookup"><span data-stu-id="adee0-202">In the **Table** field, enter **VendTable**.</span></span>
    5. <span data-ttu-id="adee0-203">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="adee0-203">Select **OK**.</span></span>

5. <span data-ttu-id="adee0-204">仅当**计算字段**类型的数据源位于容器中，才能初始化对这些数据源的调用。</span><span class="sxs-lookup"><span data-stu-id="adee0-204">You can parameterize calls to data sources of the **Calculated field** type only if those data sources reside in a container.</span></span> <span data-ttu-id="adee0-205">因此，请执行以下步骤添加**空容器**类型的数据源以保存**计算字段**类型的新参数化数据源：</span><span class="sxs-lookup"><span data-stu-id="adee0-205">Therefore, follow these steps to add a data source of the **Empty container** type to hold a new parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="adee0-206">在**数据源类型**窗格中，展开**常规**，然后选择**空容器**。</span><span class="sxs-lookup"><span data-stu-id="adee0-206">In the **Data source types** pane, expand **General**, and select **Empty container**.</span></span>
    2. <span data-ttu-id="adee0-207">选择**添加根**。</span><span class="sxs-lookup"><span data-stu-id="adee0-207">Select **Add root**.</span></span>
    3. <span data-ttu-id="adee0-208">在对话框的**名称**字段中，输入 **Box**。</span><span class="sxs-lookup"><span data-stu-id="adee0-208">In the dialog box, in the **Name** field, enter **Box**.</span></span>
    3. <span data-ttu-id="adee0-209">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="adee0-209">Select **OK**.</span></span>

    ![“模型映射设计器”页面中的 Box 数据源](./media/er-calculated-field-ds-performance-mapping-3.png)

6. <span data-ttu-id="adee0-211">执行以下步骤添加**计算字段**类型的参数化数据源：</span><span class="sxs-lookup"><span data-stu-id="adee0-211">Follow these steps to add a parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="adee0-212">在**数据源**窗格中选择 **Box**。</span><span class="sxs-lookup"><span data-stu-id="adee0-212">In the **Data sources** pane, select **Box**.</span></span>
    2. <span data-ttu-id="adee0-213">在**数据源类型**窗格中，展开**函数**，然后选择**计算字段**。</span><span class="sxs-lookup"><span data-stu-id="adee0-213">In the **Data source types** pane, expand **Functions**, and select **Calculated field**.</span></span>
    3. <span data-ttu-id="adee0-214">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="adee0-214">Select **Add**.</span></span>
    4. <span data-ttu-id="adee0-215">在对话框的**名称**字段中，输入 **Vend**。</span><span class="sxs-lookup"><span data-stu-id="adee0-215">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    5. <span data-ttu-id="adee0-216">选择**编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="adee0-216">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="adee0-217">在**公式设计器**页面中，选择**参数**指定调用此数据源时必须提供的参数。</span><span class="sxs-lookup"><span data-stu-id="adee0-217">On the **Formula designer** page, select **Parameters** to specify the parameters that must be provided when this data source is called.</span></span>
    7. <span data-ttu-id="adee0-218">在**参数**对话框中，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="adee0-218">In the **Parameters** dialog box, select **New**.</span></span>
    8. <span data-ttu-id="adee0-219">在**名称**字段中，输入 **parmVendAccNumber**。</span><span class="sxs-lookup"><span data-stu-id="adee0-219">In the **Name** field, enter **parmVendAccNumber**.</span></span>
    9. <span data-ttu-id="adee0-220">在**类型**字段中，选择**字符串**。</span><span class="sxs-lookup"><span data-stu-id="adee0-220">In the **Type** field, select **String**.</span></span>
    10. <span data-ttu-id="adee0-221">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="adee0-221">Select **OK**.</span></span>
    11. <span data-ttu-id="adee0-222">在**公式**字段中，输入 **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**。</span><span class="sxs-lookup"><span data-stu-id="adee0-222">In the **Formula** field, enter **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span></span>
    12. <span data-ttu-id="adee0-223">选择**保存**，然后关闭**公式设计器**页面。</span><span class="sxs-lookup"><span data-stu-id="adee0-223">Select **Save**, and close the **Formula designer** page.</span></span>
    13. <span data-ttu-id="adee0-224">选择**确定**添加新数据源。</span><span class="sxs-lookup"><span data-stu-id="adee0-224">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="adee0-225">执行以下步骤将添加的数据源标记为在执行期间缓存：</span><span class="sxs-lookup"><span data-stu-id="adee0-225">Follow these steps to mark the added data source as cached during the execution:</span></span>

    1. <span data-ttu-id="adee0-226">在**数据源**窗格中，选择 **Box\\Vend**。</span><span class="sxs-lookup"><span data-stu-id="adee0-226">In the **Data sources** pane, select **Box\\Vend**.</span></span>
    2. <span data-ttu-id="adee0-227">选择**高速缓存**。</span><span class="sxs-lookup"><span data-stu-id="adee0-227">Select **Cache**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="adee0-228">运行时，将在 **Trans** 数据源的所有供应商交易记录范围中缓存 **Box\\Vend** 数据源。</span><span class="sxs-lookup"><span data-stu-id="adee0-228">The **Box\\Vend** data source will be cached in the scope of all vendor transactions of the **Trans** data source at runtime.</span></span>

8. <span data-ttu-id="adee0-229">执行以下步骤更新嵌套的 **Trans\\\#Vend** 数据源，以使其使用 **Box\\Vend** 数据源：</span><span class="sxs-lookup"><span data-stu-id="adee0-229">Follow these steps to update the nested **Trans\\\#Vend** data source so that it uses the **Box\\Vend** data source:</span></span>

    1. <span data-ttu-id="adee0-230">在**数据源**窗格中，展开 **Trans**。</span><span class="sxs-lookup"><span data-stu-id="adee0-230">In the **Data sources** pane, expand **Trans**.</span></span>
    2. <span data-ttu-id="adee0-231">选择 **Trans\\\#Vend** 数据源，然后选择**编辑** \> **编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="adee0-231">Select the **Trans\\\#Vend** data source, and then select **Edit** \> **Edit formula**.</span></span>
    3. <span data-ttu-id="adee0-232">在**公式设计器**页面的**公式**字段中，输入 **Box.Vend(\@.AccountNum)**。</span><span class="sxs-lookup"><span data-stu-id="adee0-232">On the **Formula designer** page, in the **Formula** field, enter **Box.Vend(\@.AccountNum)**.</span></span>
    4. <span data-ttu-id="adee0-233">选择**保存**，然后关闭**公式设计器**页。</span><span class="sxs-lookup"><span data-stu-id="adee0-233">Select **Save**, and then close the **Formula designer** page.</span></span>
    5. <span data-ttu-id="adee0-234">选择**确定**完成对所选数据源的更改。</span><span class="sxs-lookup"><span data-stu-id="adee0-234">Select **OK** to complete your changes to the selected data source.</span></span>

9. <span data-ttu-id="adee0-235">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="adee0-235">Select **Save**.</span></span>

    ![“模型映射设计器”页面中的 Vend 数据源](./media/er-calculated-field-ds-performance-mapping-4.png)

10. <span data-ttu-id="adee0-237">关闭**模型映射设计器**页。</span><span class="sxs-lookup"><span data-stu-id="adee0-237">Close the **Model mapping designer** page.</span></span>
11. <span data-ttu-id="adee0-238">关闭**模型映射**页。</span><span class="sxs-lookup"><span data-stu-id="adee0-238">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="adee0-239">完成修改后的 ER 模型映射版本</span><span class="sxs-lookup"><span data-stu-id="adee0-239">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="adee0-240">在**配置**页**版本**快速选项卡上，选择**性能改进映射**配置版本 **1.2**。</span><span class="sxs-lookup"><span data-stu-id="adee0-240">On the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance improvement mapping** configuration.</span></span>
2. <span data-ttu-id="adee0-241">选择**更改状态** \> **完成**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="adee0-241">Select **Change status** \> **Complete**, and then select **OK**.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="adee0-242">运行修改后的 ER 解决方案以跟踪执行情况</span><span class="sxs-lookup"><span data-stu-id="adee0-242">Run the modified ER solution to trace execution</span></span>

<span data-ttu-id="adee0-243">重复本主题前面的[运行 ER 格式](#run-format)部分中的步骤生成一个新的性能跟踪。</span><span class="sxs-lookup"><span data-stu-id="adee0-243">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a><span data-ttu-id="adee0-244">使用性能跟踪分析对映射性能的调整</span><span class="sxs-lookup"><span data-stu-id="adee0-244">Use the performance trace to analyze adjustments to the model mapping</span></span> 

1. <span data-ttu-id="adee0-245">在**配置**页的配置树中，选择**性能改进映射**。</span><span class="sxs-lookup"><span data-stu-id="adee0-245">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="adee0-246">在操作窗格上，选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="adee0-246">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="adee0-247">在**模型映射**页面的操作窗格中，选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="adee0-247">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="adee0-248">在**模型映射设计器**页的操作窗格上，选择**性能跟踪**。</span><span class="sxs-lookup"><span data-stu-id="adee0-248">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="adee0-249">选择最近生成的跟踪，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="adee0-249">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="adee0-250">请注意，您对模型映射进行的调整消除了对数据库的重复查询。</span><span class="sxs-lookup"><span data-stu-id="adee0-250">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="adee0-251">还减少了对此模型映射的数据库表和数据源的调用数量。</span><span class="sxs-lookup"><span data-stu-id="adee0-251">The number of calls to database tables and data sources for this model mapping has also been reduced.</span></span>

![跟踪“模型映射设计器”页面 1 中的信息](./media/er-calculated-field-ds-performance-mapping-5.png)

<span data-ttu-id="adee0-253">总执行时间已缩短了大约 20 倍（从大约 8 秒到大约 400 毫秒）。</span><span class="sxs-lookup"><span data-stu-id="adee0-253">The total execution time has been reduced about 20 times (from about 8 seconds to about 400 milliseconds).</span></span> <span data-ttu-id="adee0-254">因此提高了整个 ER 解决方案的性能。</span><span class="sxs-lookup"><span data-stu-id="adee0-254">Therefore, the performance of the whole ER solution has been improved.</span></span>

![跟踪“模型映射设计器”页面 2 中的信息](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a><span data-ttu-id="adee0-256">附录 1：下载示例 Microsoft ER 解决方案的组件</span><span class="sxs-lookup"><span data-stu-id="adee0-256">Appendix 1: Download the components of the sample Microsoft ER solution</span></span>

<span data-ttu-id="adee0-257">必须下载以下文件并存储在本地。</span><span class="sxs-lookup"><span data-stu-id="adee0-257">You must download the following files and store them locally.</span></span>

| <span data-ttu-id="adee0-258">文件</span><span class="sxs-lookup"><span data-stu-id="adee0-258">File</span></span>                                        | <span data-ttu-id="adee0-259">内容</span><span class="sxs-lookup"><span data-stu-id="adee0-259">Content</span></span> |
|---------------------------------------------|---------|
| <span data-ttu-id="adee0-260">Performance improvement model.version.1</span><span class="sxs-lookup"><span data-stu-id="adee0-260">Performance improvement model.version.1</span></span>     | [<span data-ttu-id="adee0-261">示例 ER 数据模型配置</span><span class="sxs-lookup"><span data-stu-id="adee0-261">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="adee0-262">Performance improvement mapping.version.1.1</span><span class="sxs-lookup"><span data-stu-id="adee0-262">Performance improvement mapping.version.1.1</span></span> | [<span data-ttu-id="adee0-263">示例 ER 模型映射配置</span><span class="sxs-lookup"><span data-stu-id="adee0-263">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="adee0-264">Performance improvement format.version.1.1</span><span class="sxs-lookup"><span data-stu-id="adee0-264">Performance improvement format.version.1.1</span></span>  | [<span data-ttu-id="adee0-265">示例 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="adee0-265">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a><span data-ttu-id="adee0-266">附录 2：配置 ER 框架</span><span class="sxs-lookup"><span data-stu-id="adee0-266">Appendix 2: Configure the ER framework</span></span>

<span data-ttu-id="adee0-267">必须先配置最低限度的 ER 参数，才能开始使用 ER 框架提高示例 Microsoft ER 解决方案的性能。</span><span class="sxs-lookup"><span data-stu-id="adee0-267">Before you can start to use the ER framework to improve the performance of the sample Microsoft ER solution, you must configure the minimal set of ER parameters.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="adee0-268">配置 ER 参数</span><span class="sxs-lookup"><span data-stu-id="adee0-268">Configure ER parameters</span></span>

1. <span data-ttu-id="adee0-269">转到**组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="adee0-269">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="adee0-270">在**本地化配置**页面的**相关链接**部分中，选择**电子申报参数**。</span><span class="sxs-lookup"><span data-stu-id="adee0-270">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="adee0-271">在**电子申报参数**页上，在**常规**选项卡上，将**启用设计模式**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="adee0-271">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="adee0-272">在**附件**选项卡上，设置以下参数：</span><span class="sxs-lookup"><span data-stu-id="adee0-272">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="adee0-273">在**配置**字段中，选择 **DEMF** 公司的**文件**类型。</span><span class="sxs-lookup"><span data-stu-id="adee0-273">In the **Configurations** field, select the **File** type for the **DEMF** company.</span></span>
    - <span data-ttu-id="adee0-274">在**作业存档**、**临时**、**基准**和**其他**字段中，选择**文件**类型。</span><span class="sxs-lookup"><span data-stu-id="adee0-274">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="adee0-275">有关 ER 参数的详细信息，请参阅[配置 ER 框架](electronic-reporting-er-configure-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="adee0-275">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="adee0-276">激活 ER 配置提供程序</span><span class="sxs-lookup"><span data-stu-id="adee0-276">Activate an ER configuration provider</span></span>

<span data-ttu-id="adee0-277">将把添加的每个 ER 配置标记为由 ER 配置提供程序负责。</span><span class="sxs-lookup"><span data-stu-id="adee0-277">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="adee0-278">在**电子申报**工作区中激活的 ER 配置提供程序用于此目的。</span><span class="sxs-lookup"><span data-stu-id="adee0-278">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="adee0-279">因此，必须先在**电子申报**工作区中激活 ER 配置提供程序，才能开始添加或编辑 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="adee0-279">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="adee0-280">只有 ER 配置的负责人才能编辑此配置。</span><span class="sxs-lookup"><span data-stu-id="adee0-280">Only the owner of an ER configuration can edit the configuration.</span></span> <span data-ttu-id="adee0-281">因此，必须先在**电子申报**工作区中激活相应 ER 配置提供程序，才能编辑 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="adee0-281">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="adee0-282">查看 ER 配置提供程序列表</span><span class="sxs-lookup"><span data-stu-id="adee0-282">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="adee0-283">转到**组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="adee0-283">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="adee0-284">在**本地化配置**页面的**相关链接**部分中，选择**配置提供程序**。</span><span class="sxs-lookup"><span data-stu-id="adee0-284">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="adee0-285">在**配置提供程序表**页面中，每条提供程序记录都有唯一名称和 URL。</span><span class="sxs-lookup"><span data-stu-id="adee0-285">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="adee0-286">查看此页面的内容。</span><span class="sxs-lookup"><span data-stu-id="adee0-286">Review the contents of this page.</span></span> <span data-ttu-id="adee0-287">如果已有 **Litware, Inc.** 的记录，请跳过下一过程，即[添加新 ER 配置提供程序](#ActivateProvider)。</span><span class="sxs-lookup"><span data-stu-id="adee0-287">If a record for **Litware, Inc.** already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="adee0-288">添加新 ER 配置提供程序</span><span class="sxs-lookup"><span data-stu-id="adee0-288">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="adee0-289">转到**组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="adee0-289">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="adee0-290">在**本地化配置**页面的**相关链接**部分中，选择**配置提供程序**。</span><span class="sxs-lookup"><span data-stu-id="adee0-290">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="adee0-291">在**配置提供程序**页面上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="adee0-291">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="adee0-292">在**名称**字段中，输入 **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="adee0-292">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="adee0-293">在 **Internet 地址**字段中，输入 `https://www.litware.com`。</span><span class="sxs-lookup"><span data-stu-id="adee0-293">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="adee0-294">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="adee0-294">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="adee0-295">激活 ER 配置提供程序</span><span class="sxs-lookup"><span data-stu-id="adee0-295">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="adee0-296">转到**组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="adee0-296">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="adee0-297">在**本地化配置**页面的**配置提供程序**部分中，选择 **Litware, Inc.** 磁贴，然后选择**设置有效**。</span><span class="sxs-lookup"><span data-stu-id="adee0-297">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="adee0-298">有关 ER 配置提供程序的详细信息，请参阅[创建配置提供程序并将其标记为有效](tasks/er-configuration-provider-mark-it-active-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="adee0-298">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="adee0-299">其他资源</span><span class="sxs-lookup"><span data-stu-id="adee0-299">Additional resources</span></span>

- [<span data-ttu-id="adee0-300">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="adee0-300">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="adee0-301">跟踪电子申报格式的执行以解决性能问题</span><span class="sxs-lookup"><span data-stu-id="adee0-301">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="adee0-302">支持对计算字段类型的 ER 数据源执行参数化调用</span><span class="sxs-lookup"><span data-stu-id="adee0-302">Support parameterized calls of ER data sources of the Calculated field type</span></span>](er-calculated-field-type.md)

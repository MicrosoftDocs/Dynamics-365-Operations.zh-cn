---
title: 跟踪电子申报格式的执行以解决性能问题
description: 此主题介绍如何使用电子申报 (ER) 中的性能跟踪功能以解决性能问题。
author: NickSelin
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7fbec962fea374afdbabaad48a42dad380708678
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295565"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="d6a83-103">跟踪 ER 格式的执行情况以解决性能问题</span><span class="sxs-lookup"><span data-stu-id="d6a83-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d6a83-104">在设计电子申报 (ER) 配置过程中，您将定义用于从应用程序获取数据并在生成的输出中输入的方法。</span><span class="sxs-lookup"><span data-stu-id="d6a83-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="d6a83-105">ER 性能跟踪功能有助于显著减少收集 ER 格式执行情况并将其用于解决性能问题的时间和成本。</span><span class="sxs-lookup"><span data-stu-id="d6a83-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="d6a83-106">本教程提供有关如何对执行的 ER 格式进行性能跟踪和如何使用来自这些跟踪的信息帮助提高性能的说明。</span><span class="sxs-lookup"><span data-stu-id="d6a83-106">This tutorial provides guidelines about how to take performance traces for executed ER formats, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d6a83-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="d6a83-107">Prerequisites</span></span>

<span data-ttu-id="d6a83-108">要完成本教程中的示例，您必须具有以下访问权限：</span><span class="sxs-lookup"><span data-stu-id="d6a83-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="d6a83-109">访问以下其中一个角色：</span><span class="sxs-lookup"><span data-stu-id="d6a83-109">Access to one of the following roles:</span></span>

    - <span data-ttu-id="d6a83-110">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="d6a83-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="d6a83-111">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="d6a83-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="d6a83-112">系统管理员</span><span class="sxs-lookup"><span data-stu-id="d6a83-112">System administrator</span></span>

- <span data-ttu-id="d6a83-113">对于下列角色之一，已为与应用程序相同的租户配置的 Regulatory Configuration Services (RCS) 的实例：</span><span class="sxs-lookup"><span data-stu-id="d6a83-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as the application, for one of the following roles:</span></span>

    - <span data-ttu-id="d6a83-114">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="d6a83-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="d6a83-115">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="d6a83-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="d6a83-116">系统管理员</span><span class="sxs-lookup"><span data-stu-id="d6a83-116">System administrator</span></span>

<span data-ttu-id="d6a83-117">还必须下载并在本地存储以下文件。</span><span class="sxs-lookup"><span data-stu-id="d6a83-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="d6a83-118">文件</span><span class="sxs-lookup"><span data-stu-id="d6a83-118">File</span></span>                                  | <span data-ttu-id="d6a83-119">内容</span><span class="sxs-lookup"><span data-stu-id="d6a83-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="d6a83-120">Performance trace model.version.1</span><span class="sxs-lookup"><span data-stu-id="d6a83-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="d6a83-121">示例 ER 数据模型配置</span><span class="sxs-lookup"><span data-stu-id="d6a83-121">Sample ER data model configuration</span></span>](https://download.microsoft.com/download/0/a/a/0aa84e48-8040-4c46-b542-e3bf15c9b2ad/Performancetracemodelversion.1.xml)    |
| <span data-ttu-id="d6a83-122">Performance trace metadata.version.1</span><span class="sxs-lookup"><span data-stu-id="d6a83-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="d6a83-123">示例 ER 元数据配置</span><span class="sxs-lookup"><span data-stu-id="d6a83-123">Sample ER metadata configuration</span></span>](https://download.microsoft.com/download/a/9/3/a937e8c4-1f8a-43e4-83ee-7d599cf7d983/Performancetracemetadataversion.1.xml)      |
| <span data-ttu-id="d6a83-124">Performance trace mapping.version.1.1</span><span class="sxs-lookup"><span data-stu-id="d6a83-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="d6a83-125">示例 ER 模型映射配置</span><span class="sxs-lookup"><span data-stu-id="d6a83-125">Sample ER model mapping configuration</span></span>](https://download.microsoft.com/download/7/7/3/77379bdc-7b22-4cfc-9b64-a9147599f931/Performancetracemappingversion1.1.xml) |
| <span data-ttu-id="d6a83-126">Performance trace format.version.1.1</span><span class="sxs-lookup"><span data-stu-id="d6a83-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="d6a83-127">示例 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="d6a83-127">Sample ER format configuration</span></span>](https://download.microsoft.com/download/8/6/8/868ba581-5a06-459e-b173-fb00f038b37f/Performancetraceformatversion1.1.xml)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="d6a83-128">配置 ER 参数</span><span class="sxs-lookup"><span data-stu-id="d6a83-128">Configure ER parameters</span></span>

<span data-ttu-id="d6a83-129">应用程序中生成的每个 Er 性能跟踪都作为执行日志记录的附件存储。</span><span class="sxs-lookup"><span data-stu-id="d6a83-129">Each ER performance trace that is generated in the application is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="d6a83-130">文档管理 (DM) 框架用于管理这些附件。</span><span class="sxs-lookup"><span data-stu-id="d6a83-130">The Document management (DM) framework is used to manage these attachments.</span></span> <span data-ttu-id="d6a83-131">必须提前配置 ER 参数，以便指定应该用于附加性能跟踪的 DM 文档类型。</span><span class="sxs-lookup"><span data-stu-id="d6a83-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="d6a83-132">在 **电子申报** 工作区中，选择 **电子申报参数** 链接。</span><span class="sxs-lookup"><span data-stu-id="d6a83-132">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="d6a83-133">然后在 **电子申报参数** 页 **附件** 选项卡上的 **其他** 字段中，选择要用于性能跟踪的 DM 文档类型。</span><span class="sxs-lookup"><span data-stu-id="d6a83-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![“电子申报参数”页面](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="d6a83-135">若要让某个 DM 文档类型出现在 **其他** 查找字段中，必须在 **文档类型** 页（**组织管理 \> 文档管理 \> 文档类型**）中以下面的方式对其进行配置：</span><span class="sxs-lookup"><span data-stu-id="d6a83-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="d6a83-136">**类：** 附加文件</span><span class="sxs-lookup"><span data-stu-id="d6a83-136">**Class:** Attach file</span></span>
- <span data-ttu-id="d6a83-137">**组：** 文件</span><span class="sxs-lookup"><span data-stu-id="d6a83-137">**Group:** File</span></span>

![“单据类型”页面](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="d6a83-139">所选文档类型必须在当前实例中的每个公司内可用，因为 DM 附件特定于公司。</span><span class="sxs-lookup"><span data-stu-id="d6a83-139">The selected document type must be available in every company of the current instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="d6a83-140">配置 RCS 参数</span><span class="sxs-lookup"><span data-stu-id="d6a83-140">Configure RCS parameters</span></span>

<span data-ttu-id="d6a83-141">将通过使用 ER 格式设计器和 ER 映射设计器把生成的 ER 性能跟踪导入 RCS 中进行分析。</span><span class="sxs-lookup"><span data-stu-id="d6a83-141">ER performance traces that are generated will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="d6a83-142">因为 ER 性能跟踪以与 ER 格式有关的执行日志记录附件形式存储，所以必须提前配置 RCS 参数，以便指定应该用于附加性能跟踪的 DM 文档类型。</span><span class="sxs-lookup"><span data-stu-id="d6a83-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="d6a83-143">在已经针对贵公司进行过配置的 RCS 实例中的 **电子申报** 工作区中，选择 **电子申报参数**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="d6a83-144">然后在 **电子申报参数** 页 **附件** 选项卡上的 **其他** 字段中，选择要用于性能跟踪的 DM 文档类型。</span><span class="sxs-lookup"><span data-stu-id="d6a83-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![RCS 中的“电子申报参数”页](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="d6a83-146">若要让某个 DM 文档类型出现在 **其他** 查找字段中，必须在 **文档类型** 页（**组织管理 \> 文档管理 \> 文档类型**）中以下面的方式对其进行配置：</span><span class="sxs-lookup"><span data-stu-id="d6a83-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="d6a83-147">**类：** 附加文件</span><span class="sxs-lookup"><span data-stu-id="d6a83-147">**Class:** Attach file</span></span>
- <span data-ttu-id="d6a83-148">**组：** 文件</span><span class="sxs-lookup"><span data-stu-id="d6a83-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="d6a83-149">设计 ER 解决方案</span><span class="sxs-lookup"><span data-stu-id="d6a83-149">Design an ER solution</span></span>

<span data-ttu-id="d6a83-150">假设您已开始设计一种新的 ER 解决方案来生成新报表以表示供应商交易记录。</span><span class="sxs-lookup"><span data-stu-id="d6a83-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="d6a83-151">现在，您可以在 **供应商交易记录** 页（转至 **应付帐款 \> 供应商 \> 所有供应商**，选择供应商，然后在操作窗格中 **供应商** 选项卡上 **交易记录** 组中选择 **交易记录**）中找到所选供应商的交易记录。</span><span class="sxs-lookup"><span data-stu-id="d6a83-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="d6a83-152">但是，您希望同时让所有供应商交易记录都包含在一个 XML 格式的电子申报文档中。</span><span class="sxs-lookup"><span data-stu-id="d6a83-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="d6a83-153">此解决方案将由多个 ER 配置构成，这些配置中包含所需数据模型、元数据、模型映射和格式组件。</span><span class="sxs-lookup"><span data-stu-id="d6a83-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="d6a83-154">登录已经针对贵公司进行过配置的 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="d6a83-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="d6a83-155">在此教程中，将为示例公司 **Litware, Inc.** 创建并修改配置。</span><span class="sxs-lookup"><span data-stu-id="d6a83-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="d6a83-156">因此，请确保已经将该配置提供程序添加到了 RCS 并选择为有效。</span><span class="sxs-lookup"><span data-stu-id="d6a83-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="d6a83-157">有关说明，请参阅[创建配置提供程序并将其标记为有效](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程。</span><span class="sxs-lookup"><span data-stu-id="d6a83-157">For instructions, see the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>
3. <span data-ttu-id="d6a83-158">在 **电子申报** 工作区中，选择 **报告配置** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="d6a83-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="d6a83-159">在 **配置** 页中，按照下面的顺序将作为先决条件下载的 ER 配置导入 RCS 中：数据模型、元数据、模型映射、格式。</span><span class="sxs-lookup"><span data-stu-id="d6a83-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="d6a83-160">为每个配置执行下列步骤:</span><span class="sxs-lookup"><span data-stu-id="d6a83-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="d6a83-161">在操作窗格上，选择 **交换 \> 从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="d6a83-162">选择 **浏览** 为所需 ER 配置选择 XML 格式的相应文件。</span><span class="sxs-lookup"><span data-stu-id="d6a83-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="d6a83-163">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-163">Select **OK**.</span></span>

    ![RCS 中的“配置”页](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="d6a83-165">运行 ER 解决方案以跟踪执行情况</span><span class="sxs-lookup"><span data-stu-id="d6a83-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="d6a83-166">假设您已经完成了 ER 解决方案第一版的设计。</span><span class="sxs-lookup"><span data-stu-id="d6a83-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="d6a83-167">现在希望在实例中进行测试并分析执行性能。</span><span class="sxs-lookup"><span data-stu-id="d6a83-167">You now want to test it in your instance and analyze execution performance.</span></span>

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a><span data-ttu-id="d6a83-168">将 ER 配置从 RCS 导入 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d6a83-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="d6a83-169">登录您的应用程序实例。</span><span class="sxs-lookup"><span data-stu-id="d6a83-169">Sign in to your application instance.</span></span>
2. <span data-ttu-id="d6a83-170">对于本教程，您将把配置从 RCS 实例（即您设计 ER 组件的位置）导入实例（即测试并最终使用这些实例的位置）。</span><span class="sxs-lookup"><span data-stu-id="d6a83-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your instance (where you test and finally use them).</span></span> <span data-ttu-id="d6a83-171">因此，您必须确保已准备好所有必需的项目。</span><span class="sxs-lookup"><span data-stu-id="d6a83-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="d6a83-172">有关说明，请参阅[从监管配置服务 (RCS) 导入电子申报 (ER) 配置](rcs-download-configurations.md)过程。</span><span class="sxs-lookup"><span data-stu-id="d6a83-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md) procedure.</span></span>
3. <span data-ttu-id="d6a83-173">执行下列步骤将配置从 RCS 导入应用程序中：</span><span class="sxs-lookup"><span data-stu-id="d6a83-173">Follow these steps to import the configurations from RCS into the application:</span></span>

    1. <span data-ttu-id="d6a83-174">在 **电子申报** 工作区 **Litware, Inc.** 配置提供程序的磁贴中，选择 **存储库**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="d6a83-175">在 **配置存储库** 页，选择 **RCS** 类型的存储库，然后选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="d6a83-176">在 **配置** 快速选项卡上，选择 **性能跟踪格式** 配置。</span><span class="sxs-lookup"><span data-stu-id="d6a83-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="d6a83-177">在 **版本** 快速选项卡上，选择所选配置的版本 **1.1**，然后选择 **导入**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![配置存储库页面](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="d6a83-179">将把相应的数据模型和模型映射配置版本作为所导入 ER 格式配置的先决条件自动导入。</span><span class="sxs-lookup"><span data-stu-id="d6a83-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="d6a83-180">开启 ER 性能跟踪</span><span class="sxs-lookup"><span data-stu-id="d6a83-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="d6a83-181">转到 **组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-181">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="d6a83-182">在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="d6a83-183">在 **用户参数** 对话框的 **执行跟踪** 部分中，执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="d6a83-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="d6a83-184">在 **执行跟踪格式** 字段中，为 ER 格式和映射元素指定应该用于存储执行详细信息的所生成性能跟踪的格式。</span><span class="sxs-lookup"><span data-stu-id="d6a83-184">In the **Execution trace format** field, specify the format of the generated performance trace that the execution details should be stored in for ER format and mapping elements:</span></span>

        - <span data-ttu-id="d6a83-185">**调试跟踪格式** – 如果您计划以交互方式运行执行时间较短的 ER 格式，请选择此值。</span><span class="sxs-lookup"><span data-stu-id="d6a83-185">**Debug trace format** – Select this value if you plan to interactively run an ER format that has a short execution time.</span></span> <span data-ttu-id="d6a83-186">然后，开始收集有关 ER 格式执行的详细信息。</span><span class="sxs-lookup"><span data-stu-id="d6a83-186">The collection of details about ER format execution is then started.</span></span> <span data-ttu-id="d6a83-187">选择此值后，性能跟踪将收集有关以下操作所用时间的信息：</span><span class="sxs-lookup"><span data-stu-id="d6a83-187">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="d6a83-188">在调用来获取数据的模型映射中运行每个数据源</span><span class="sxs-lookup"><span data-stu-id="d6a83-188">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="d6a83-189">处理每个格式项以在生成的输出中输入数据</span><span class="sxs-lookup"><span data-stu-id="d6a83-189">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="d6a83-190">如果您选择 **调试跟踪格式** 值，可以在 ER 操作设计器中分析跟踪的内容。</span><span class="sxs-lookup"><span data-stu-id="d6a83-190">If you select the **Debug trace format** value, you can analyze the content of the trace in the ER Operation designer.</span></span> <span data-ttu-id="d6a83-191">在那里，您可以查看跟踪中提到的 ER 格式或映射元素。</span><span class="sxs-lookup"><span data-stu-id="d6a83-191">There, you can view the ER format or mapping elements that are mentioned in the trace.</span></span>

        - <span data-ttu-id="d6a83-192">**聚合跟踪格式** – 如果您计划在批处理模式下运行执行时间较长的 ER 格式，请选择此值。</span><span class="sxs-lookup"><span data-stu-id="d6a83-192">**Aggregated trace format** – Select this value if you plan to run an ER format that has a long execution time in batch mode.</span></span> <span data-ttu-id="d6a83-193">然后，开始收集有关 ER 格式执行的聚合详细信息。</span><span class="sxs-lookup"><span data-stu-id="d6a83-193">The collection of the aggregated details about ER format execution is then started.</span></span> <span data-ttu-id="d6a83-194">选择此值后，性能跟踪将收集有关以下操作所用时间的信息：</span><span class="sxs-lookup"><span data-stu-id="d6a83-194">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="d6a83-195">在调用来获取数据的模型映射中运行每个数据源</span><span class="sxs-lookup"><span data-stu-id="d6a83-195">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="d6a83-196">在调用来获取数据的格式映射中运行每个数据源</span><span class="sxs-lookup"><span data-stu-id="d6a83-196">Running each data source in the format mapping that is called to get data</span></span>
            - <span data-ttu-id="d6a83-197">处理每个格式项以在生成的输出中输入数据</span><span class="sxs-lookup"><span data-stu-id="d6a83-197">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="d6a83-198">**聚合跟踪格式** 值在 Microsoft Dynamics 365 Finance 版本 10.0.20 及更高版本中可用。</span><span class="sxs-lookup"><span data-stu-id="d6a83-198">The **Aggregated trace format** value is available in Microsoft Dynamics 365 Finance version 10.0.20 and later.</span></span>

            <span data-ttu-id="d6a83-199">在 ER 格式设计器和 ER 模型映射设计器中，您可以查看单个组件的总执行时间。</span><span class="sxs-lookup"><span data-stu-id="d6a83-199">In the ER format designer and ER model mapping designer, you can view the total execution time for a single component.</span></span> <span data-ttu-id="d6a83-200">此外，跟踪包含有关执行的详细信息，例如执行次数以及单次执行的最短和最长时间。</span><span class="sxs-lookup"><span data-stu-id="d6a83-200">Additionally, the trace contains details about the execution, such as the number of executions, and the minimum and maximum time of a single execution.</span></span>

            > [!NOTE]
            > <span data-ttu-id="d6a83-201">此跟踪基于跟踪的组件路径收集。</span><span class="sxs-lookup"><span data-stu-id="d6a83-201">This trace is collected based on the traced components path.</span></span> <span data-ttu-id="d6a83-202">因此，当单个父组件包含多个未命名的子组件或多个子组件具有相同名称时，统计信息可能不正确。</span><span class="sxs-lookup"><span data-stu-id="d6a83-202">Therefore, the statistics might be incorrect when a single parent component contains several unnamed child components, or when several child components have the same name.</span></span>

    2. <span data-ttu-id="d6a83-203">将下列选项设置为 **是** 以收集 ER 模型映射和 ER 格式组件执行情况的具体详细信息：</span><span class="sxs-lookup"><span data-stu-id="d6a83-203">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="d6a83-204">**收集查询统计信息** – 如果开启此选项，性能跟踪将收集以下信息：</span><span class="sxs-lookup"><span data-stu-id="d6a83-204">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="d6a83-205">数据源执行的数据库调用数量</span><span class="sxs-lookup"><span data-stu-id="d6a83-205">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="d6a83-206">数据库的重复调用数量</span><span class="sxs-lookup"><span data-stu-id="d6a83-206">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="d6a83-207">用于执行数据库调用的 SQL 语句的详细信息</span><span class="sxs-lookup"><span data-stu-id="d6a83-207">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="d6a83-208">**跟踪缓存访问** – 如果开启此选项，性能跟踪将收集有关 ER 模型映射的缓存使用情况的信息。</span><span class="sxs-lookup"><span data-stu-id="d6a83-208">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="d6a83-209">**跟踪数据访问** – 如果开启此选项，性能跟踪将收集有关对所执行记录列表类型数据源的数据库的调用数量的信息。</span><span class="sxs-lookup"><span data-stu-id="d6a83-209">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="d6a83-210">**跟踪列表枚举** – 如果开启此选项，性能跟踪将收集有关从记录列表类型数据源请求的记录数量的信息。</span><span class="sxs-lookup"><span data-stu-id="d6a83-210">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6a83-211">**用户参数** 对话框中的参数特定于用户和当前公司。</span><span class="sxs-lookup"><span data-stu-id="d6a83-211">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![“用户参数”选项卡](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a><span data-ttu-id="d6a83-213">运行 ER 格式</span><span class="sxs-lookup"><span data-stu-id="d6a83-213">Run the ER format</span></span>

1. <span data-ttu-id="d6a83-214">选择 **DEMF** 公司。</span><span class="sxs-lookup"><span data-stu-id="d6a83-214">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="d6a83-215">转到 **组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-215">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="d6a83-216">在 **配置** 页的配置树中，选择 **性能跟踪格式** 项。</span><span class="sxs-lookup"><span data-stu-id="d6a83-216">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="d6a83-217">在操作窗格上，选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-217">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="d6a83-218">请注意，生成的文件中提供有关六个供应商的 265 个交易记录的信息。</span><span class="sxs-lookup"><span data-stu-id="d6a83-218">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="d6a83-219">查看执行跟踪</span><span class="sxs-lookup"><span data-stu-id="d6a83-219">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a><span data-ttu-id="d6a83-220">从应用程序导出生成的跟踪</span><span class="sxs-lookup"><span data-stu-id="d6a83-220">Export the generated trace from the application</span></span>

<span data-ttu-id="d6a83-221">性能跟踪将从源 ER 格式分离，并可序列化为外部 zip 文件。</span><span class="sxs-lookup"><span data-stu-id="d6a83-221">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="d6a83-222">转到 **组织管理 \> 电子申报 \> 配置调试日志**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-222">Go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="d6a83-223">在 **电子申报运行日志** 页左窗格中 **配置名称** 字段中，选择 **性能跟踪格式** 查找已通过执行 **性能跟踪格式** 配置生成的日志记录。</span><span class="sxs-lookup"><span data-stu-id="d6a83-223">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="d6a83-224">选择页面右上角的 **附件** 按钮（回形针符号），或按 **Ctrl+Shift+A**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-224">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![“电子申报运行日志”页上的“附件”按钮](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="d6a83-226">在 **电子申报运行日志的附件** 页上操作窗格中，选择 **打开** 获取 zip 文件格式的性能跟踪并存储在本地。</span><span class="sxs-lookup"><span data-stu-id="d6a83-226">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![电子申报运行日志的附件](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="d6a83-228">生成的跟踪只有对源 ER 报表通过 **GUID** 格式的唯一报表标识进行的引用。</span><span class="sxs-lookup"><span data-stu-id="d6a83-228">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="d6a83-229">不考虑格式的版本编号。</span><span class="sxs-lookup"><span data-stu-id="d6a83-229">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="d6a83-230">请注意，已经为所执行 ER 格式生成的性能跟踪与 ER 模型映射之间的关联基于所用根描述符和常用数据模型。</span><span class="sxs-lookup"><span data-stu-id="d6a83-230">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="d6a83-231">不考虑格式和模型映射的版本编号。</span><span class="sxs-lookup"><span data-stu-id="d6a83-231">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="d6a83-232">也不考虑模型映射的 **模型映射默认值** 标记的设置。</span><span class="sxs-lookup"><span data-stu-id="d6a83-232">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a><span data-ttu-id="d6a83-233">将生成的跟踪导入 RCS</span><span class="sxs-lookup"><span data-stu-id="d6a83-233">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="d6a83-234">在 RCS 的 **电子申报** 工作区中，选择 **报告配置** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="d6a83-234">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="d6a83-235">在 **配置** 页的配置树中，展开 **性能跟踪模型** 项，然后选择 **性能跟踪格式** 项。</span><span class="sxs-lookup"><span data-stu-id="d6a83-235">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="d6a83-236">在操作窗格上，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-236">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="d6a83-237">在 **格式设计器** 页的操作窗格上，选择 **性能跟踪**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-237">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="d6a83-238">在 **性能跟踪结果配置** 对话框中，选择 **导入性能跟踪**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-238">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="d6a83-239">选择 **浏览** 以选择之前导出的 zip 文件。</span><span class="sxs-lookup"><span data-stu-id="d6a83-239">Select **Browse** to select the zip file that you exported earlier.</span></span>
7. <span data-ttu-id="d6a83-240">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-240">Select **OK**.</span></span>

    ![RCS 中的“性能跟踪结果设置”对话框](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="d6a83-242">在 RCS 中使用性能跟踪进行分析 – 格式执行</span><span class="sxs-lookup"><span data-stu-id="d6a83-242">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="d6a83-243">在 RCS 的 **格式设计器** 页中，选择 **展开/折叠** 以展开所有格式项的目录。</span><span class="sxs-lookup"><span data-stu-id="d6a83-243">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="d6a83-244">请注意，当前格式的某些项会显示更多信息：</span><span class="sxs-lookup"><span data-stu-id="d6a83-244">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="d6a83-245">通过使用格式项在生成的输出中输入数据实际所用时间</span><span class="sxs-lookup"><span data-stu-id="d6a83-245">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="d6a83-246">表示为占生成整个输出所用时间总量的百分比的相同时间</span><span class="sxs-lookup"><span data-stu-id="d6a83-246">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![RCS 中的“格式设计器”页](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="d6a83-248">关闭 **格式设计器** 页。</span><span class="sxs-lookup"><span data-stu-id="d6a83-248">Close **Format designer** page.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a><span data-ttu-id="d6a83-249">在 RCS 中使用性能跟踪进行分析 – 模型映射</span><span class="sxs-lookup"><span data-stu-id="d6a83-249">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="d6a83-250">在 RCS 的 **配置** 页的配置树中，选择 **性能跟踪映射** 项。</span><span class="sxs-lookup"><span data-stu-id="d6a83-250">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="d6a83-251">在操作窗格上，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-251">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="d6a83-252">选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-252">Select **Designer**.</span></span>
4. <span data-ttu-id="d6a83-253">在 **模型映射设计器** 页的操作窗格上，选择 **性能跟踪**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-253">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="d6a83-254">选择之前导入的跟踪。</span><span class="sxs-lookup"><span data-stu-id="d6a83-254">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="d6a83-255">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-255">Select **OK**.</span></span>

<span data-ttu-id="d6a83-256">请注意，新信息将可用于当前模型映射的部分数据源项：</span><span class="sxs-lookup"><span data-stu-id="d6a83-256">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="d6a83-257">使用数据源获取数据实际所用时间</span><span class="sxs-lookup"><span data-stu-id="d6a83-257">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="d6a83-258">表示为占运行整个模型映射所用时间总量的百分比的相同时间</span><span class="sxs-lookup"><span data-stu-id="d6a83-258">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="d6a83-259">请注意，ER 将在运行 VendTable/\<Relations/VendTrans.VendTable\_AccountNum 数据源时通知您数据库请求的当前模型映射重复项。</span><span class="sxs-lookup"><span data-stu-id="d6a83-259">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="d6a83-260">出现此重复项的原因是为每个迭代的供应商记录调用了两次供应商交易记录列表：</span><span class="sxs-lookup"><span data-stu-id="d6a83-260">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="d6a83-261">一次调用是为了根据配置的绑定在数据模型中输入每个交易记录的详细信息。</span><span class="sxs-lookup"><span data-stu-id="d6a83-261">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="d6a83-262">一次调用是为了在数据模型中输入为每个供应商计算出的交易记录数量。</span><span class="sxs-lookup"><span data-stu-id="d6a83-262">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![RCS 中“模型映射设计器”页上有关重复数据库请求的消息](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="d6a83-264">值 **\[Q:530\]** 表示 VendTrans 表被调用了 530 次以将一个记录从该表返回到 VendTable/\<Relations/VendTrans.VendTable\_AccountNum 数据源。</span><span class="sxs-lookup"><span data-stu-id="d6a83-264">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="d6a83-265">值 **\[530\]** 表示 VendTable/\<Relations/VendTrans.VendTable\_AccountNum 数据源被调用了 530 次以从该数据源返回一个记录并在数据模型中输入来自该记录的详细信息。</span><span class="sxs-lookup"><span data-stu-id="d6a83-265">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="d6a83-266">建议使用 VendTable/\<Relations/VendTrans.VendTable\_AccountNum 数据源的高速缓存减少为了获取 265 个交易记录所执行调用的数量，并帮助提高模型映射的性能。</span><span class="sxs-lookup"><span data-stu-id="d6a83-266">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="d6a83-267">减少对 LedgerTransTypeList 数据源执行的调用数量可能也很有用。</span><span class="sxs-lookup"><span data-stu-id="d6a83-267">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="d6a83-268">此数据源用于将 **LedgerTransType** 枚举的每个值与其标签关联。</span><span class="sxs-lookup"><span data-stu-id="d6a83-268">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="d6a83-269">可通过使用此数据源找到相应标签并在每个供应商交易记录的数据模型中输入。</span><span class="sxs-lookup"><span data-stu-id="d6a83-269">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="d6a83-270">相对 265 个交易记录而言，对此数据源的当前调用数量 (9,027) 相当高。</span><span class="sxs-lookup"><span data-stu-id="d6a83-270">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![RCS 中的“模型映射设计器”页，其中显示了对数据源的 9,027 个调用](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="d6a83-272">根据来自执行跟踪的信息改善模型映射</span><span class="sxs-lookup"><span data-stu-id="d6a83-272">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="d6a83-273">修改模型映射的逻辑</span><span class="sxs-lookup"><span data-stu-id="d6a83-273">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="d6a83-274">请执行以下步骤使用高速缓存来帮助避免重复调用数据库：</span><span class="sxs-lookup"><span data-stu-id="d6a83-274">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="d6a83-275">在 RCS 的 **模型映射设计器** 页 **数据源** 窗格中，选择 **VendTable** 项。</span><span class="sxs-lookup"><span data-stu-id="d6a83-275">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="d6a83-276">选择 **高速缓存**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-276">Select **Cache**.</span></span>
    3. <span data-ttu-id="d6a83-277">展开 **VendTable** 向，展开 VendTable 数据源的一对多关系列表（即 **\<Relations** 项），然后选择 **VendTrans.VendTable\_AccountNum** 项。</span><span class="sxs-lookup"><span data-stu-id="d6a83-277">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="d6a83-278">选择 **高速缓存**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-278">Select **Cache**.</span></span>

    ![用于帮助避免重复调用的高速缓存设置](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="d6a83-280">执行以下步骤将 LedgerTransTypeList 数据源纳入 VendTable 数据源的范围内：</span><span class="sxs-lookup"><span data-stu-id="d6a83-280">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="d6a83-281">在 **数据源类型** 窗格中，展开 **函数** 项，然后选择 **计算字段** 项。</span><span class="sxs-lookup"><span data-stu-id="d6a83-281">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="d6a83-282">在 **数据源** 窗格中，选择 **VendTable** 项。</span><span class="sxs-lookup"><span data-stu-id="d6a83-282">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="d6a83-283">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-283">Select **Add**.</span></span>
    4. <span data-ttu-id="d6a83-284">在 **名称** 字段中，输入 **\$TransType**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-284">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="d6a83-285">选择 **编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-285">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="d6a83-286">在 **公式** 字段中，输入 **LedgerTransTypeList**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-286">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="d6a83-287">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-287">Select **Save**.</span></span>
    8. <span data-ttu-id="d6a83-288">关闭 **公式编辑器** 页。</span><span class="sxs-lookup"><span data-stu-id="d6a83-288">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="d6a83-289">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-289">Click **OK**.</span></span>

3. <span data-ttu-id="d6a83-290">执行下列步骤对 **\$TransType** 字段执行高速缓存：</span><span class="sxs-lookup"><span data-stu-id="d6a83-290">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="d6a83-291">选择 **LedgerTransTypeList** 项。</span><span class="sxs-lookup"><span data-stu-id="d6a83-291">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="d6a83-292">选择 **高速缓存**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-292">Select **Cache**.</span></span>
    3. <span data-ttu-id="d6a83-293">选择 **VendTable.\$TransType** 项。</span><span class="sxs-lookup"><span data-stu-id="d6a83-293">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="d6a83-294">选择 **高速缓存**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-294">Select **Cache**.</span></span>

    ![$TransType 字段的高速缓存设置](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="d6a83-296">执行以下步骤更改 **\$TransTypeRecord** 字段，使其开始使用高速缓存的 **\$TransType** 字段：</span><span class="sxs-lookup"><span data-stu-id="d6a83-296">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="d6a83-297">在 **数据源** 窗格中，依次展开 **VendTable**、**\<Relations** 和 **VendTrans.VendTable\_AccountNum** 项，然后选择 **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** 项。</span><span class="sxs-lookup"><span data-stu-id="d6a83-297">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="d6a83-298">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-298">Select **Edit**.</span></span>
    3. <span data-ttu-id="d6a83-299">选择 **编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-299">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="d6a83-300">在 **公式** 字段中，找到下面的表达式：</span><span class="sxs-lookup"><span data-stu-id="d6a83-300">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="d6a83-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="d6a83-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="d6a83-302">在 **公式** 字段中，输入下面的表达式：</span><span class="sxs-lookup"><span data-stu-id="d6a83-302">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="d6a83-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType))。</span><span class="sxs-lookup"><span data-stu-id="d6a83-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="d6a83-304">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-304">Select **Save**.</span></span>
    7. <span data-ttu-id="d6a83-305">关闭 **公式编辑器** 页。</span><span class="sxs-lookup"><span data-stu-id="d6a83-305">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="d6a83-306">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-306">Select **OK**.</span></span>

5. <span data-ttu-id="d6a83-307">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-307">Select **Save**.</span></span>
6. <span data-ttu-id="d6a83-308">关闭 **模型映射设计器** 页。</span><span class="sxs-lookup"><span data-stu-id="d6a83-308">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="d6a83-309">关闭 **模型映射** 页。</span><span class="sxs-lookup"><span data-stu-id="d6a83-309">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="d6a83-310">完成修改后的 ER 模型映射版本</span><span class="sxs-lookup"><span data-stu-id="d6a83-310">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="d6a83-311">在 RCS 中的 **配置** 页 **版本** 快速选项卡上，选择 **性能跟踪映射** 配置版本 **1.2**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-311">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="d6a83-312">选择 **更改状态**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-312">Select **Change status**.</span></span>
3. <span data-ttu-id="d6a83-313">选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-313">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a><span data-ttu-id="d6a83-314">将修改后的 ER 模型映射配置从 RCS 导入应用程序中</span><span class="sxs-lookup"><span data-stu-id="d6a83-314">Import the modified ER model mapping configuration from RCS into the application</span></span>

<span data-ttu-id="d6a83-315">重复本主题前面的 [将 ER 配置从 RCS 导入 Finance and Operations](#import-configuration) 部分中的步骤导入 **性能跟踪映射** 配置版本 1.2。</span><span class="sxs-lookup"><span data-stu-id="d6a83-315">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="d6a83-316">运行修改后的 ER 解决方案以跟踪执行情况</span><span class="sxs-lookup"><span data-stu-id="d6a83-316">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="d6a83-317">运行 ER 格式</span><span class="sxs-lookup"><span data-stu-id="d6a83-317">Run the ER format</span></span>

<span data-ttu-id="d6a83-318">重复本主题前面的[运行 ER 格式](#run-format)部分中的步骤生成一个新的性能跟踪。</span><span class="sxs-lookup"><span data-stu-id="d6a83-318">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="work-with-the-execution-trace"></a><span data-ttu-id="d6a83-319">使用执行跟踪</span><span class="sxs-lookup"><span data-stu-id="d6a83-319">Work with the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><span data-ttu-id="d6a83-320">从应用程序导出生成的跟踪</span><span class="sxs-lookup"><span data-stu-id="d6a83-320">Export the generated trace from the application</span></span>

<span data-ttu-id="d6a83-321">重复本主题前面的[从应用程序导出生成的跟踪](#export-trace)部分中的步骤在本地保存新的性能跟踪。</span><span class="sxs-lookup"><span data-stu-id="d6a83-321">Repeat the steps in the [Export the generated trace from the application](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="d6a83-322">将生成的跟踪导入 RCS</span><span class="sxs-lookup"><span data-stu-id="d6a83-322">Import the generated trace into RCS</span></span>

<span data-ttu-id="d6a83-323">重复本主题前面的[将生成的跟踪导入 RCS](#import-trace) 部分中的步骤将新的性能跟踪导入 RCS。</span><span class="sxs-lookup"><span data-stu-id="d6a83-323">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="d6a83-324">在 RCS 中使用性能跟踪进行分析 – 模型映射</span><span class="sxs-lookup"><span data-stu-id="d6a83-324">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="d6a83-325">重复本主题前面的[在 RCS 中使用性能跟踪进行分析 – 模型映射](#use-trace)部分中的步骤分析最新性能跟踪。</span><span class="sxs-lookup"><span data-stu-id="d6a83-325">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="d6a83-326">请注意，您对模型映射进行的调整消除了对数据库的重复查询。</span><span class="sxs-lookup"><span data-stu-id="d6a83-326">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="d6a83-327">还减少了对此模型映射的数据库表和数据源的调用数量。</span><span class="sxs-lookup"><span data-stu-id="d6a83-327">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="d6a83-328">因此提高了整个 ER 解决方案的性能。</span><span class="sxs-lookup"><span data-stu-id="d6a83-328">Therefore, the performance of the whole ER solution has improved.</span></span>

![在 RCS 的“模型映射设计器”页中跟踪 VendTable 数据源的信息](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="d6a83-330">在跟踪信息中，VendTable 数据源的值 **\[12\]** 表示此数据源被调用了 12 次。</span><span class="sxs-lookup"><span data-stu-id="d6a83-330">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="d6a83-331">值 **\[Q:6\]** 表示六个调用被转换为了对 VendTable 表的数据库调用。</span><span class="sxs-lookup"><span data-stu-id="d6a83-331">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="d6a83-332">值 **\[C:6\]** 表示已缓存了从数据库获取的记录，并且通过使用高速缓存还除了另外六个调用。</span><span class="sxs-lookup"><span data-stu-id="d6a83-332">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="d6a83-333">请注意，对 LedgerTransTypeList 数据源的调用数量已从 9,027 降低到了 240。</span><span class="sxs-lookup"><span data-stu-id="d6a83-333">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![在 RCS 的“模型映射设计器”页中跟踪 LedgerTransTypeList 数据源的信息](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a><span data-ttu-id="d6a83-335">检查应用程序中的执行跟踪</span><span class="sxs-lookup"><span data-stu-id="d6a83-335">Review the execution trace in the application</span></span>

<span data-ttu-id="d6a83-336">除了 RCS，还有一些版本可能提供针对 ER 框架设计器体验的功能。</span><span class="sxs-lookup"><span data-stu-id="d6a83-336">In addition to RCS, some versions might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="d6a83-337">这些版本有一个可开启的 **启用设计模式** 选项。</span><span class="sxs-lookup"><span data-stu-id="d6a83-337">These versions have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="d6a83-338">可以在 **电子申报参数** 页（可从 **电子申报** 工作区打开该页）中的 **常规** 选项卡上找到此选项。</span><span class="sxs-lookup"><span data-stu-id="d6a83-338">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![在“电子申报参数”页面中启用设计模式选项](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="d6a83-340">如果使用这些版本中的一个，您可以直接在应用程序中分析生成的性能跟踪的详细信息。</span><span class="sxs-lookup"><span data-stu-id="d6a83-340">If you use one of these versions, you can analyze the details of generated performance traces directly in the application.</span></span> <span data-ttu-id="d6a83-341">无需将其从应用程序中导出，再导入 RCS。</span><span class="sxs-lookup"><span data-stu-id="d6a83-341">You don't have to export them from the application and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="d6a83-342">通过使用外部工具查看执行跟踪</span><span class="sxs-lookup"><span data-stu-id="d6a83-342">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="d6a83-343">配置用户参数</span><span class="sxs-lookup"><span data-stu-id="d6a83-343">Configure user parameters</span></span>

1. <span data-ttu-id="d6a83-344">转到 **组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-344">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="d6a83-345">在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="d6a83-346">在 **用户参数** 对话框 **执行跟踪** 部分的 **执行跟踪格式** 字段中，选择 **PerfView XML**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-346">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="d6a83-347">运行 ER 格式</span><span class="sxs-lookup"><span data-stu-id="d6a83-347">Run the ER format</span></span>

<span data-ttu-id="d6a83-348">重复本主题前面的[运行 ER 格式](#run-format)部分中的步骤生成一个新的性能跟踪。</span><span class="sxs-lookup"><span data-stu-id="d6a83-348">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="d6a83-349">请注意，Web 浏览器提供一个可供下载的 zip 文件。</span><span class="sxs-lookup"><span data-stu-id="d6a83-349">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="d6a83-350">这个文件中包含 PerfView 格式的性能跟踪。</span><span class="sxs-lookup"><span data-stu-id="d6a83-350">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="d6a83-351">然后可使用 PerfView 性能分析工具分析 ER 格式执行情况的详细信息。</span><span class="sxs-lookup"><span data-stu-id="d6a83-351">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![PerfView 格式的性能跟踪信息](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="d6a83-353">使用外部工具查看其中包含数据库查询的执行跟踪</span><span class="sxs-lookup"><span data-stu-id="d6a83-353">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="d6a83-354">因为已改进了 ER 框架，所以以 PerfView 格式生成的绩效跟踪现在提供更多有关 ER 格式执行的详细信息。</span><span class="sxs-lookup"><span data-stu-id="d6a83-354">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="d6a83-355">在 Microsoft Dynamics 365 for Finance and Operations 版本 10.0.4（2019 年 7 月）中，此跟踪中也可以包含对执行的 SQL 查询的详细信息。</span><span class="sxs-lookup"><span data-stu-id="d6a83-355">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="d6a83-356">配置用户参数</span><span class="sxs-lookup"><span data-stu-id="d6a83-356">Configure user parameters</span></span>

1. <span data-ttu-id="d6a83-357">转到 **组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-357">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="d6a83-358">在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-358">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="d6a83-359">在 **用户参数** 对话框的 **执行跟踪** 部分中，设置以下参数：</span><span class="sxs-lookup"><span data-stu-id="d6a83-359">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="d6a83-360">在 **执行跟踪格式** 字段中，选择 **PerfView XML**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-360">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="d6a83-361">将 **收集查询统计信息** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-361">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="d6a83-362">将 **跟踪查询** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="d6a83-362">Set the **Trace query** option to **Yes**.</span></span>

    ![执行跟踪部分，“用户参数”对话框](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="d6a83-364">运行 ER 格式</span><span class="sxs-lookup"><span data-stu-id="d6a83-364">Run the ER format</span></span>

<span data-ttu-id="d6a83-365">重复本主题前面的[运行 ER 格式](#run-format)部分中的步骤生成一个新的性能跟踪。</span><span class="sxs-lookup"><span data-stu-id="d6a83-365">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="d6a83-366">请注意，Web 浏览器提供一个可供下载的 zip 文件。</span><span class="sxs-lookup"><span data-stu-id="d6a83-366">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="d6a83-367">这个文件中包含 PerfView 格式的性能跟踪。</span><span class="sxs-lookup"><span data-stu-id="d6a83-367">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="d6a83-368">然后可使用 PerfView 性能分析工具分析 ER 格式执行情况的详细信息。</span><span class="sxs-lookup"><span data-stu-id="d6a83-368">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="d6a83-369">执行 ER 格式期间，此跟踪中现在包含 SQL 数据库访问权限的详细信息。</span><span class="sxs-lookup"><span data-stu-id="d6a83-369">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![在 PerfView 中跟踪执行的 ER 格式的信息](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a><span data-ttu-id="d6a83-371">其他资源</span><span class="sxs-lookup"><span data-stu-id="d6a83-371">Additional resources</span></span>

- [<span data-ttu-id="d6a83-372">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="d6a83-372">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="d6a83-373">通过添加参数化的计算字段数据源提高 ER 解决方案的性能</span><span class="sxs-lookup"><span data-stu-id="d6a83-373">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

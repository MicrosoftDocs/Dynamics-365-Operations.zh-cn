---
title: 跟踪 ER 格式的执行情况以解决性能问题
description: 此主题介绍如何使用电子申报 (ER) 中的性能跟踪功能以解决性能问题。
author: NickSelin
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 55f3fd95a87bcf62824021ebfbf3bcd11af6013f
ms.sourcegitcommit: f6581bab16225a027f4fbfad25fdef45bd286489
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/27/2019
ms.locfileid: "1703867"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="7b91a-103">跟踪 ER 格式的执行情况以解决性能问题</span><span class="sxs-lookup"><span data-stu-id="7b91a-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7b91a-104">在设计电子申报 (ER) 配置过程中，您将定义用于从 Microsoft Dynamics 365 for Finance and Operations 获取数据并在生成的输出中输入的方法。</span><span class="sxs-lookup"><span data-stu-id="7b91a-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of Microsoft Dynamics 365 for Finance and Operations and enter it in the output that is generated.</span></span> <span data-ttu-id="7b91a-105">ER 性能跟踪功能有助于显著减少收集 ER 格式执行情况并将其用于解决性能问题的时间和成本。</span><span class="sxs-lookup"><span data-stu-id="7b91a-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="7b91a-106">本教程提供有关如何对 Finance and Operations 中执行的 ER 格式进行性能跟踪和如何使用来自这些跟踪的信息帮助提高性能的说明。</span><span class="sxs-lookup"><span data-stu-id="7b91a-106">This tutorial provides guidelines about how to take performance traces for executed ER formats in Finance and Operations, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7b91a-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="7b91a-107">Prerequisites</span></span>

<span data-ttu-id="7b91a-108">要完成本教程中的示例，您必须具有以下访问权限：</span><span class="sxs-lookup"><span data-stu-id="7b91a-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="7b91a-109">访问 Finance and Operations 的以下其中一个角色：</span><span class="sxs-lookup"><span data-stu-id="7b91a-109">Access to Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="7b91a-110">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="7b91a-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="7b91a-111">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="7b91a-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="7b91a-112">系统管理员</span><span class="sxs-lookup"><span data-stu-id="7b91a-112">System administrator</span></span>

- <span data-ttu-id="7b91a-113">对于下列角色之一，已为与 Finance and Operations 相同的租户配置的Regulatory Configuration Services (RCS) 的实例：</span><span class="sxs-lookup"><span data-stu-id="7b91a-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance and Operations, for one of the following roles:</span></span>

    - <span data-ttu-id="7b91a-114">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="7b91a-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="7b91a-115">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="7b91a-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="7b91a-116">系统管理员</span><span class="sxs-lookup"><span data-stu-id="7b91a-116">System administrator</span></span>

<span data-ttu-id="7b91a-117">还必须下载并在本地存储以下文件。</span><span class="sxs-lookup"><span data-stu-id="7b91a-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="7b91a-118">文件</span><span class="sxs-lookup"><span data-stu-id="7b91a-118">File</span></span>                                  | <span data-ttu-id="7b91a-119">内容</span><span class="sxs-lookup"><span data-stu-id="7b91a-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="7b91a-120">Performance trace model.version.1</span><span class="sxs-lookup"><span data-stu-id="7b91a-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="7b91a-121">示例 ER 数据模型配置</span><span class="sxs-lookup"><span data-stu-id="7b91a-121">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| <span data-ttu-id="7b91a-122">Performance trace metadata.version.1</span><span class="sxs-lookup"><span data-stu-id="7b91a-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="7b91a-123">示例 ER 元数据配置</span><span class="sxs-lookup"><span data-stu-id="7b91a-123">Sample ER metadata configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| <span data-ttu-id="7b91a-124">Performance trace mapping.version.1.1</span><span class="sxs-lookup"><span data-stu-id="7b91a-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="7b91a-125">示例 ER 模型映射配置</span><span class="sxs-lookup"><span data-stu-id="7b91a-125">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="7b91a-126">Performance trace format.version.1.1</span><span class="sxs-lookup"><span data-stu-id="7b91a-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="7b91a-127">示例 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="7b91a-127">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="7b91a-128">配置 ER 参数</span><span class="sxs-lookup"><span data-stu-id="7b91a-128">Configure ER parameters</span></span>

<span data-ttu-id="7b91a-129">Finance and Operations 中生成的每个 Er 性能跟踪都作为执行日志记录的附件存储。</span><span class="sxs-lookup"><span data-stu-id="7b91a-129">Each ER performance trace that is generated in Finance and Operations is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="7b91a-130">Finance and Operations 的文档管理 (DM) 框架用于管理这些附件。</span><span class="sxs-lookup"><span data-stu-id="7b91a-130">The Document management (DM) framework of Finance and Operations is used to manage these attachments.</span></span> <span data-ttu-id="7b91a-131">必须提前配置 ER 参数，以便指定应该用于附加性能跟踪的 DM 文档类型。</span><span class="sxs-lookup"><span data-stu-id="7b91a-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="7b91a-132">在 Finance and Operation 的**电子申报**工作区中，选择**电子申报参数**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-132">In Finance and Operation, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="7b91a-133">然后在**电子申报参数**页**附件**选项卡上的**其他**字段中，选择要用于性能跟踪的 DM 文档类型。</span><span class="sxs-lookup"><span data-stu-id="7b91a-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Finance and Operations 中的“电子申报参数”页](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="7b91a-135">若要让某个 DM 文档类型出现在**其他**查找字段中，必须在**文档类型**页（**组织管理 \> 文档管理 \> 文档类型**）中以下面的方式对其进行配置：</span><span class="sxs-lookup"><span data-stu-id="7b91a-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="7b91a-136">**类：** 附加文件</span><span class="sxs-lookup"><span data-stu-id="7b91a-136">**Class:** Attach file</span></span>
- <span data-ttu-id="7b91a-137">**组：** 文件</span><span class="sxs-lookup"><span data-stu-id="7b91a-137">**Group:** File</span></span>

![Finance and Operations 中的“文档类型”页](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="7b91a-139">所选文档类型必须在当前 Finance and Operations 实例中的每个公司内可用，因为 DM 附件特定于公司。</span><span class="sxs-lookup"><span data-stu-id="7b91a-139">The selected document type must be available in every company of the current Finance and Operations instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="7b91a-140">配置 RCS 参数</span><span class="sxs-lookup"><span data-stu-id="7b91a-140">Configure RCS parameters</span></span>

<span data-ttu-id="7b91a-141">将通过使用 ER 格式设计器和 ER 映射设计器把 Finance and Operations 中生成的 Er 性能跟踪导入 RCS 中进行分析。</span><span class="sxs-lookup"><span data-stu-id="7b91a-141">ER performance traces that are generated in Finance and Operations will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="7b91a-142">因为 ER 性能跟踪以与 ER 格式有关的执行日志记录附件形式存储，所以必须提前配置 RCS 参数，以便指定应该用于附加性能跟踪的 DM 文档类型。</span><span class="sxs-lookup"><span data-stu-id="7b91a-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="7b91a-143">在已经针对贵公司进行过配置的 RCS 实例中的**电子申报**工作区中，选择**电子申报参数**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="7b91a-144">然后在**电子申报参数**页**附件**选项卡上的**其他**字段中，选择要用于性能跟踪的 DM 文档类型。</span><span class="sxs-lookup"><span data-stu-id="7b91a-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![RCS 中的“电子申报参数”页](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="7b91a-146">若要让某个 DM 文档类型出现在**其他**查找字段中，必须在**文档类型**页（**组织管理 \> 文档管理 \> 文档类型**）中以下面的方式对其进行配置：</span><span class="sxs-lookup"><span data-stu-id="7b91a-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="7b91a-147">**类：** 附加文件</span><span class="sxs-lookup"><span data-stu-id="7b91a-147">**Class:** Attach file</span></span>
- <span data-ttu-id="7b91a-148">**组：** 文件</span><span class="sxs-lookup"><span data-stu-id="7b91a-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="7b91a-149">设计 ER 解决方案</span><span class="sxs-lookup"><span data-stu-id="7b91a-149">Design an ER solution</span></span>

<span data-ttu-id="7b91a-150">假设您已开始设计一种新的 ER 解决方案来生成新报表以表示供应商交易记录。</span><span class="sxs-lookup"><span data-stu-id="7b91a-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="7b91a-151">现在，您可以在**供应商交易记录**页（转至**应付帐款 \> 供应商 \> 所有供应商**，选择供应商，然后在操作窗格中**供应商**选项卡上**交易记录**组中选择**交易记录**）中找到所选供应商的交易记录。</span><span class="sxs-lookup"><span data-stu-id="7b91a-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="7b91a-152">但是，您希望同时让所有供应商交易记录都包含在一个 XML 格式的电子申报文档中。</span><span class="sxs-lookup"><span data-stu-id="7b91a-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="7b91a-153">此解决方案将由多个 ER 配置构成，这些配置中包含所需数据模型、元数据、模型映射和格式组件。</span><span class="sxs-lookup"><span data-stu-id="7b91a-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="7b91a-154">登录已经针对贵公司进行过配置的 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="7b91a-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="7b91a-155">在此教程中，将为示例公司 **Litware, Inc.** 创建并修改配置。</span><span class="sxs-lookup"><span data-stu-id="7b91a-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="7b91a-156">因此，请确保已经将该配置提供程序添加到了 RCS 并选择为有效。</span><span class="sxs-lookup"><span data-stu-id="7b91a-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="7b91a-157">有关说明，请参阅[创建配置提供程序并将其标记为有效](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)过程。</span><span class="sxs-lookup"><span data-stu-id="7b91a-157">For instructions, see the [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) procedure.</span></span>
3. <span data-ttu-id="7b91a-158">在**电子申报**工作区中，选择**报告配置**磁贴。</span><span class="sxs-lookup"><span data-stu-id="7b91a-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="7b91a-159">在**配置**页中，按照下面的顺序将作为先决条件下载的 ER 配置导入 RCS 中：数据模型、元数据、模型映射、格式。</span><span class="sxs-lookup"><span data-stu-id="7b91a-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="7b91a-160">为每个配置执行下列步骤:</span><span class="sxs-lookup"><span data-stu-id="7b91a-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="7b91a-161">在操作窗格上，选择**交换 \> 从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="7b91a-162">选择**浏览**为所需 ER 配置选择 XML 格式的相应文件。</span><span class="sxs-lookup"><span data-stu-id="7b91a-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="7b91a-163">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-163">Select **OK**.</span></span>

    ![RCS 中的“配置”页](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="7b91a-165">运行 ER 解决方案以跟踪执行情况</span><span class="sxs-lookup"><span data-stu-id="7b91a-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="7b91a-166">假设您已经完成了 ER 解决方案第一版的设计。</span><span class="sxs-lookup"><span data-stu-id="7b91a-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="7b91a-167">现在希望在 Finance and Operations instance 中进行测试并分析执行性能。</span><span class="sxs-lookup"><span data-stu-id="7b91a-167">You now want to test it in your Finance and Operations instance and analyze execution performance.</span></span>

### <a id='import-configuration'></a><span data-ttu-id="7b91a-168">将 ER 配置从 RCS 导入 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7b91a-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="7b91a-169">登录到 Finance and Operations 实例。</span><span class="sxs-lookup"><span data-stu-id="7b91a-169">Sign in to your Finance and Operations instance.</span></span>
2. <span data-ttu-id="7b91a-170">对于本教程，您将把配置从 RCS 实例（即您设计 ER 组件的位置）导入 Finance and Operations 实例（即测试并最终使用这些实例的位置）。</span><span class="sxs-lookup"><span data-stu-id="7b91a-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your Finance and Operations instance (where you test and finally use them).</span></span> <span data-ttu-id="7b91a-171">因此，您必须确保已准备好所有必需的项目。</span><span class="sxs-lookup"><span data-stu-id="7b91a-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="7b91a-172">有关说明，请参阅[从监管配置服务 (RCS) 导入电子申报 (ER) 配置](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)过程。</span><span class="sxs-lookup"><span data-stu-id="7b91a-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations) procedure.</span></span>
3. <span data-ttu-id="7b91a-173">执行下列步骤将配置从 RCS 导入 Finance and Operations：</span><span class="sxs-lookup"><span data-stu-id="7b91a-173">Follow these steps to import the configurations from RCS into Finance and Operations:</span></span>

    1. <span data-ttu-id="7b91a-174">在**电子申报**工作区 **Litware, Inc.** 配置提供程序的磁贴中，选择**存储库**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="7b91a-175">在**配置存储库**页，选择 **RCS** 类型的存储库，然后选择**打开**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="7b91a-176">在**配置**快速选项卡上，选择**性能跟踪格式**配置。</span><span class="sxs-lookup"><span data-stu-id="7b91a-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="7b91a-177">在**版本**快速选项卡上，选择所选配置的版本 **1.1**，然后选择**导入**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Finance and Operations 中的“配置存储库”页](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="7b91a-179">将把相应的数据模型和模型映射配置版本作为所导入 ER 格式配置的先决条件自动导入。</span><span class="sxs-lookup"><span data-stu-id="7b91a-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="7b91a-180">开启 ER 性能跟踪</span><span class="sxs-lookup"><span data-stu-id="7b91a-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="7b91a-181">在 Finance and Operations 中，转到**组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-181">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="7b91a-182">在**配置**页操作窗格中**配置**选项卡的**高级设置**组中，选择**用户参数**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="7b91a-183">在**用户参数**对话框的**执行跟踪**部分中，执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="7b91a-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="7b91a-184">在**执行跟踪格式**字段中，选择**调试跟踪格式**开始收集 ER 格式执行情况的详细信息。</span><span class="sxs-lookup"><span data-stu-id="7b91a-184">In the **Execution trace format** field, select **Debug trace format** to start to collect the details of ER format execution.</span></span> <span data-ttu-id="7b91a-185">选择此值后，性能跟踪将收集有关以下操作所用时间的信息：</span><span class="sxs-lookup"><span data-stu-id="7b91a-185">When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</span></span>

        - <span data-ttu-id="7b91a-186">在调用来获取数据的模型映射中运行每个数据源</span><span class="sxs-lookup"><span data-stu-id="7b91a-186">Running each data source in the model mapping that is called to get data</span></span>
        - <span data-ttu-id="7b91a-187">处理每个格式项以在生成的输出中输入数据</span><span class="sxs-lookup"><span data-stu-id="7b91a-187">Processing each format item to enter data in the output that is generated</span></span>

        <span data-ttu-id="7b91a-188">使用**执行跟踪格式**字段为 ER 格式和映射元素指定用于存储执行详细信息的所生成性能跟踪的格式。</span><span class="sxs-lookup"><span data-stu-id="7b91a-188">You use the **Execution trace format** field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</span></span> <span data-ttu-id="7b91a-189">通过选择**调试跟踪格式**作为值，您可以在 ER Operation 设计器中分析跟踪内容，并查看跟踪中介绍的 ER 格式或映射元素。</span><span class="sxs-lookup"><span data-stu-id="7b91a-189">By selecting **Debug trace format** as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</span></span>

    2. <span data-ttu-id="7b91a-190">将下列选项设置为**是**以收集 ER 模型映射和 ER 格式组件执行情况的具体详细信息：</span><span class="sxs-lookup"><span data-stu-id="7b91a-190">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="7b91a-191">**收集查询统计信息** – 如果开启此选项，性能跟踪将收集以下信息：</span><span class="sxs-lookup"><span data-stu-id="7b91a-191">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="7b91a-192">数据源执行的数据库调用数量</span><span class="sxs-lookup"><span data-stu-id="7b91a-192">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="7b91a-193">数据库的重复调用数量</span><span class="sxs-lookup"><span data-stu-id="7b91a-193">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="7b91a-194">用于执行数据库调用的 SQL 语句的详细信息</span><span class="sxs-lookup"><span data-stu-id="7b91a-194">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="7b91a-195">**跟踪缓存访问** – 如果开启此选项，性能跟踪将收集有关 ER 模型映射的缓存使用情况的信息。</span><span class="sxs-lookup"><span data-stu-id="7b91a-195">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="7b91a-196">**跟踪数据访问** – 如果开启此选项，性能跟踪将收集有关对所执行记录列表类型数据源的数据库的调用数量的信息。</span><span class="sxs-lookup"><span data-stu-id="7b91a-196">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="7b91a-197">**跟踪列表枚举** – 如果开启此选项，性能跟踪将收集有关从记录列表类型数据源请求的记录数量的信息。</span><span class="sxs-lookup"><span data-stu-id="7b91a-197">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7b91a-198">**用户参数**对话框中的参数特定于用户和当前公司。</span><span class="sxs-lookup"><span data-stu-id="7b91a-198">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Finance and Operations 中的“用户参数”对话框](./media/GER-PerfTrace-GER-UserParameters.png)

### <a id='run-format'></a><span data-ttu-id="7b91a-200">运行 ER 格式</span><span class="sxs-lookup"><span data-stu-id="7b91a-200">Run the ER format</span></span>

1. <span data-ttu-id="7b91a-201">在 Finance and Operations 中，选择 **DEMF** 公司。</span><span class="sxs-lookup"><span data-stu-id="7b91a-201">In Finance and Operations, select the **DEMF** company.</span></span>
2. <span data-ttu-id="7b91a-202">转到**组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-202">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="7b91a-203">在**配置**页的配置树中，选择**性能跟踪格式**项。</span><span class="sxs-lookup"><span data-stu-id="7b91a-203">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="7b91a-204">在操作窗格上，选择**运行**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-204">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="7b91a-205">请注意，生成的文件中提供有关六个供应商的 265 个交易记录的信息。</span><span class="sxs-lookup"><span data-stu-id="7b91a-205">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="7b91a-206">查看执行跟踪</span><span class="sxs-lookup"><span data-stu-id="7b91a-206">Review the execution trace</span></span>

### <a id='export-trace'></a><span data-ttu-id="7b91a-207">从 Finance and Operations 导出生成的跟踪</span><span class="sxs-lookup"><span data-stu-id="7b91a-207">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="7b91a-208">性能跟踪将从源 ER 格式分离，并可序列化为外部 zip 文件。</span><span class="sxs-lookup"><span data-stu-id="7b91a-208">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="7b91a-209">在 Finance and Operations 中，转到**组织管理 \> 电子申报 \> 配置调试日志**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-209">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="7b91a-210">在**电子申报运行日志**页左窗格中**配置名称**字段中，选择**性能跟踪格式**查找已通过执行**性能跟踪格式**配置生成的日志记录。</span><span class="sxs-lookup"><span data-stu-id="7b91a-210">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="7b91a-211">选择页面右上角的**附件**按钮（回形针符号），或按 **Ctrl+Shift+A**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-211">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Finance and Operations 中“电子申报运行日志”页上的“附件”按钮](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="7b91a-213">在**电子申报运行日志的附件**页上操作窗格中，选择**打开**获取 zip 文件格式的性能跟踪并存储在本地。</span><span class="sxs-lookup"><span data-stu-id="7b91a-213">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Finance and Operations 中的“电子申报运行日志的附件”页](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="7b91a-215">生成的跟踪只有对源 ER 报表通过 **GUID** 格式的唯一报表标识进行的引用。</span><span class="sxs-lookup"><span data-stu-id="7b91a-215">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="7b91a-216">不考虑格式的版本编号。</span><span class="sxs-lookup"><span data-stu-id="7b91a-216">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="7b91a-217">请注意，已经为所执行 ER 格式生成的性能跟踪与 ER 模型映射之间的关联基于所用根描述符和常用数据模型。</span><span class="sxs-lookup"><span data-stu-id="7b91a-217">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="7b91a-218">不考虑格式和模型映射的版本编号。</span><span class="sxs-lookup"><span data-stu-id="7b91a-218">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="7b91a-219">也不考虑模型映射的**模型映射默认值**标记的设置。</span><span class="sxs-lookup"><span data-stu-id="7b91a-219">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a id='import-trace'></a><span data-ttu-id="7b91a-220">将生成的跟踪导入 RCS</span><span class="sxs-lookup"><span data-stu-id="7b91a-220">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="7b91a-221">在 RCS 的**电子申报**工作区中，选择**报告配置**磁贴。</span><span class="sxs-lookup"><span data-stu-id="7b91a-221">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="7b91a-222">在**配置**页的配置树中，展开**性能跟踪模型**项，然后选择**性能跟踪格式**项。</span><span class="sxs-lookup"><span data-stu-id="7b91a-222">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="7b91a-223">在操作窗格上，选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-223">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="7b91a-224">在**格式设计器**页的操作窗格上，选择**性能跟踪**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-224">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="7b91a-225">在**性能跟踪结果配置**对话框中，选择**导入性能跟踪**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-225">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="7b91a-226">选择**浏览**以选择之前从 Finance and Operations 导出的 zip 文件。</span><span class="sxs-lookup"><span data-stu-id="7b91a-226">Select **Browse** to select the zip file that you exported from Finance and Operations earlier.</span></span>
7. <span data-ttu-id="7b91a-227">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-227">Select **OK**.</span></span>

    ![RCS 中的“性能跟踪结果设置”对话框](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="7b91a-229">在 RCS 中使用性能跟踪进行分析 – 格式执行</span><span class="sxs-lookup"><span data-stu-id="7b91a-229">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="7b91a-230">在 RCS 的**格式设计器**页中，选择**展开/折叠**以展开所有格式项的目录。</span><span class="sxs-lookup"><span data-stu-id="7b91a-230">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="7b91a-231">请注意，当前格式的某些项会显示更多信息：</span><span class="sxs-lookup"><span data-stu-id="7b91a-231">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="7b91a-232">通过使用格式项在生成的输出中输入数据实际所用时间</span><span class="sxs-lookup"><span data-stu-id="7b91a-232">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="7b91a-233">表示为占生成整个输出所用时间总量的百分比的相同时间</span><span class="sxs-lookup"><span data-stu-id="7b91a-233">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![RCS 中的“格式设计器”页](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="7b91a-235">关闭**格式设计器**页。</span><span class="sxs-lookup"><span data-stu-id="7b91a-235">Close **Format designer** page.</span></span>

### <a id='use-trace'></a><span data-ttu-id="7b91a-236">在 RCS 中使用性能跟踪进行分析 – 模型映射</span><span class="sxs-lookup"><span data-stu-id="7b91a-236">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="7b91a-237">在 RCS 的**配置**页的配置树中，选择**性能跟踪映射**项。</span><span class="sxs-lookup"><span data-stu-id="7b91a-237">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="7b91a-238">在操作窗格上，选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-238">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="7b91a-239">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-239">Select **Designer**.</span></span>
4. <span data-ttu-id="7b91a-240">在**模型映射设计器**页的操作窗格上，选择**性能跟踪**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-240">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="7b91a-241">选择之前导入的跟踪。</span><span class="sxs-lookup"><span data-stu-id="7b91a-241">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="7b91a-242">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-242">Select **OK**.</span></span>

<span data-ttu-id="7b91a-243">请注意，新信息将可用于当前模型映射的部分数据源项：</span><span class="sxs-lookup"><span data-stu-id="7b91a-243">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="7b91a-244">使用数据源获取数据实际所用时间</span><span class="sxs-lookup"><span data-stu-id="7b91a-244">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="7b91a-245">表示为占运行整个模型映射所用时间总量的百分比的相同时间</span><span class="sxs-lookup"><span data-stu-id="7b91a-245">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="7b91a-246">请注意，ER 将在运行 VendTable/\<Relations/VendTrans.VendTable\_AccountNum 数据源时通知您数据库请求的当前模型映射重复项。</span><span class="sxs-lookup"><span data-stu-id="7b91a-246">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="7b91a-247">出现此重复项的原因是为每个迭代的供应商记录调用了两次供应商交易记录列表：</span><span class="sxs-lookup"><span data-stu-id="7b91a-247">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="7b91a-248">一次调用是为了根据配置的绑定在数据模型中输入每个交易记录的详细信息。</span><span class="sxs-lookup"><span data-stu-id="7b91a-248">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="7b91a-249">一次调用是为了在数据模型中输入为每个供应商计算出的交易记录数量。</span><span class="sxs-lookup"><span data-stu-id="7b91a-249">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![RCS 中“模型映射设计器”页上有关重复数据库请求的消息](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="7b91a-251">值 **\[Q:530\]** 表示 VendTrans 表被调用了 530 次以将一个记录从该表返回到 VendTable/\<Relations/VendTrans.VendTable\_AccountNum 数据源。</span><span class="sxs-lookup"><span data-stu-id="7b91a-251">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="7b91a-252">值 **\[530\]** 表示 VendTable/\<Relations/VendTrans.VendTable\_AccountNum 数据源被调用了 530 次以从该数据源返回一个记录并在数据模型中输入来自该记录的详细信息。</span><span class="sxs-lookup"><span data-stu-id="7b91a-252">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="7b91a-253">建议使用 VendTable/\<Relations/VendTrans.VendTable\_AccountNum 数据源的高速缓存减少为了获取 265 个交易记录所执行调用的数量，并帮助提高模型映射的性能。</span><span class="sxs-lookup"><span data-stu-id="7b91a-253">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="7b91a-254">减少对 LedgerTransTypeList 数据源执行的调用数量可能也很有用。</span><span class="sxs-lookup"><span data-stu-id="7b91a-254">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="7b91a-255">此数据源用于将 **LedgerTransType** 枚举的每个值与其标签关联。</span><span class="sxs-lookup"><span data-stu-id="7b91a-255">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="7b91a-256">可通过使用此数据源找到相应标签并在每个供应商交易记录的数据模型中输入。</span><span class="sxs-lookup"><span data-stu-id="7b91a-256">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="7b91a-257">相对 265 个交易记录而言，对此数据源的当前调用数量 (9,027) 相当高。</span><span class="sxs-lookup"><span data-stu-id="7b91a-257">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![RCS 中的“模型映射设计器”页，其中显示了对数据源的 9,027 个调用](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="7b91a-259">根据来自执行跟踪的信息改善模型映射</span><span class="sxs-lookup"><span data-stu-id="7b91a-259">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="7b91a-260">修改模型映射的逻辑</span><span class="sxs-lookup"><span data-stu-id="7b91a-260">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="7b91a-261">请执行以下步骤使用高速缓存来帮助避免重复调用数据库：</span><span class="sxs-lookup"><span data-stu-id="7b91a-261">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="7b91a-262">在 RCS 的**模型映射设计器**页**数据源**窗格中，选择 **VendTable** 项。</span><span class="sxs-lookup"><span data-stu-id="7b91a-262">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="7b91a-263">选择**高速缓存**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-263">Select **Cache**.</span></span>
    3. <span data-ttu-id="7b91a-264">展开 **VendTable** 向，展开 VendTable 数据源的一对多关系列表（即 **\<Relations** 项），然后选择 **VendTrans.VendTable\_AccountNum** 项。</span><span class="sxs-lookup"><span data-stu-id="7b91a-264">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="7b91a-265">选择**高速缓存**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-265">Select **Cache**.</span></span>

    ![用于帮助避免重复调用的高速缓存设置](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="7b91a-267">执行以下步骤将 LedgerTransTypeList 数据源纳入 VendTable 数据源的范围内：</span><span class="sxs-lookup"><span data-stu-id="7b91a-267">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="7b91a-268">在**数据源类型**窗格中，展开**函数**项，然后选择**计算字段**项。</span><span class="sxs-lookup"><span data-stu-id="7b91a-268">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="7b91a-269">在**数据源**窗格中，选择 **VendTable** 项。</span><span class="sxs-lookup"><span data-stu-id="7b91a-269">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="7b91a-270">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-270">Select **Add**.</span></span>
    4. <span data-ttu-id="7b91a-271">在**名称**字段中，输入 **\$TransType**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-271">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="7b91a-272">选择**编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-272">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="7b91a-273">在**公式**字段中，输入 **LedgerTransTypeList**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-273">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="7b91a-274">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-274">Select **Save**.</span></span>
    8. <span data-ttu-id="7b91a-275">关闭**公式编辑器**页。</span><span class="sxs-lookup"><span data-stu-id="7b91a-275">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="7b91a-276">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-276">Click **OK**.</span></span>

3. <span data-ttu-id="7b91a-277">执行下列步骤对 **\$TransType** 字段执行高速缓存：</span><span class="sxs-lookup"><span data-stu-id="7b91a-277">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="7b91a-278">选择 **LedgerTransTypeList** 项。</span><span class="sxs-lookup"><span data-stu-id="7b91a-278">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="7b91a-279">选择**高速缓存**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-279">Select **Cache**.</span></span>
    3. <span data-ttu-id="7b91a-280">选择 **VendTable.\$TransType** 项。</span><span class="sxs-lookup"><span data-stu-id="7b91a-280">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="7b91a-281">选择**高速缓存**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-281">Select **Cache**.</span></span>

    ![$TransType 字段的高速缓存设置](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="7b91a-283">执行以下步骤更改 **\$TransTypeRecord** 字段，使其开始使用高速缓存的 **\$TransType** 字段：</span><span class="sxs-lookup"><span data-stu-id="7b91a-283">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="7b91a-284">在**数据源**窗格中，依次展开 **VendTable**、**\<Relations** 和 **VendTrans.VendTable\_AccountNum** 项，然后选择 **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** 项。</span><span class="sxs-lookup"><span data-stu-id="7b91a-284">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="7b91a-285">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-285">Select **Edit**.</span></span>
    3. <span data-ttu-id="7b91a-286">选择**编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-286">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="7b91a-287">在**公式**字段中，找到下面的表达式：</span><span class="sxs-lookup"><span data-stu-id="7b91a-287">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="7b91a-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="7b91a-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="7b91a-289">在**公式**字段中，输入下面的表达式：</span><span class="sxs-lookup"><span data-stu-id="7b91a-289">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="7b91a-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType))。</span><span class="sxs-lookup"><span data-stu-id="7b91a-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="7b91a-291">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-291">Select **Save**.</span></span>
    7. <span data-ttu-id="7b91a-292">关闭**公式编辑器**页。</span><span class="sxs-lookup"><span data-stu-id="7b91a-292">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="7b91a-293">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-293">Select **OK**.</span></span>

5. <span data-ttu-id="7b91a-294">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-294">Select **Save**.</span></span>
6. <span data-ttu-id="7b91a-295">关闭**模型映射设计器**页。</span><span class="sxs-lookup"><span data-stu-id="7b91a-295">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="7b91a-296">关闭**模型映射**页。</span><span class="sxs-lookup"><span data-stu-id="7b91a-296">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="7b91a-297">完成修改后的 ER 模型映射版本</span><span class="sxs-lookup"><span data-stu-id="7b91a-297">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="7b91a-298">在 RCS 中的**配置**页**版本**快速选项卡上，选择**性能跟踪映射**配置版本 **1.2**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-298">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="7b91a-299">选择**更改状态**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-299">Select **Change status**.</span></span>
3. <span data-ttu-id="7b91a-300">选择**完成**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-300">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-finance-and-operations"></a><span data-ttu-id="7b91a-301">将修改后的 ER 模型映射配置从 RCS 导入 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7b91a-301">Import the modified ER model mapping configuration from RCS into Finance and Operations</span></span>

<span data-ttu-id="7b91a-302">重复本主题前面的[将 ER 配置从 RCS 导入 Finance and Operations](#import-configuration) 部分中的步骤将**性能跟踪映射**配置版本 1.2 导入 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="7b91a-302">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration into Finance and Operations.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="7b91a-303">运行修改后的 ER 解决方案以跟踪执行情况</span><span class="sxs-lookup"><span data-stu-id="7b91a-303">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="7b91a-304">运行 ER 格式</span><span class="sxs-lookup"><span data-stu-id="7b91a-304">Run the ER format</span></span>

<span data-ttu-id="7b91a-305">重复本主题前面的[运行 ER 格式](#run-format)部分中的步骤生成一个新的性能跟踪。</span><span class="sxs-lookup"><span data-stu-id="7b91a-305">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="7b91a-306">查看执行跟踪</span><span class="sxs-lookup"><span data-stu-id="7b91a-306">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-finance-and-operations"></a><span data-ttu-id="7b91a-307">从 Finance and Operations 导出生成的跟踪</span><span class="sxs-lookup"><span data-stu-id="7b91a-307">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="7b91a-308">重复本主题前面的[从 Finance and Operations 导出生成的跟踪](#export-trace)部分中的步骤在本地保存新的性能跟踪。</span><span class="sxs-lookup"><span data-stu-id="7b91a-308">Repeat the steps in the [Export the generated trace from Finance and Operations](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="7b91a-309">将生成的跟踪导入 RCS</span><span class="sxs-lookup"><span data-stu-id="7b91a-309">Import the generated trace into RCS</span></span>

<span data-ttu-id="7b91a-310">重复本主题前面的[将生成的跟踪导入 RCS](#import-trace) 部分中的步骤将新的性能跟踪导入 RCS。</span><span class="sxs-lookup"><span data-stu-id="7b91a-310">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="7b91a-311">在 RCS 中使用性能跟踪进行分析 – 模型映射</span><span class="sxs-lookup"><span data-stu-id="7b91a-311">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="7b91a-312">重复本主题前面的[在 RCS 中使用性能跟踪进行分析 – 模型映射](#use-trace)部分中的步骤分析最新性能跟踪。</span><span class="sxs-lookup"><span data-stu-id="7b91a-312">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="7b91a-313">请注意，您对模型映射进行的调整消除了对数据库的重复查询。</span><span class="sxs-lookup"><span data-stu-id="7b91a-313">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="7b91a-314">还减少了对此模型映射的数据库表和数据源的调用数量。</span><span class="sxs-lookup"><span data-stu-id="7b91a-314">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="7b91a-315">因此提高了整个 ER 解决方案的性能。</span><span class="sxs-lookup"><span data-stu-id="7b91a-315">Therefore, the performance of the whole ER solution has improved.</span></span>

![在 RCS 的“模型映射设计器”页中跟踪 VendTable 数据源的信息](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="7b91a-317">在跟踪信息中，VendTable 数据源的值 **\[12\]** 表示此数据源被调用了 12 次。</span><span class="sxs-lookup"><span data-stu-id="7b91a-317">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="7b91a-318">值 **\[Q:6\]** 表示六个调用被转换为了对 VendTable 表的数据库调用。</span><span class="sxs-lookup"><span data-stu-id="7b91a-318">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="7b91a-319">值 **\[C:6\]** 表示已缓存了从数据库获取的记录，并且通过使用高速缓存还除了另外六个调用。</span><span class="sxs-lookup"><span data-stu-id="7b91a-319">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="7b91a-320">请注意，对 LedgerTransTypeList 数据源的调用数量已从 9,027 降低到了 240。</span><span class="sxs-lookup"><span data-stu-id="7b91a-320">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![在 RCS 的“模型映射设计器”页中跟踪 LedgerTransTypeList 数据源的信息](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-finance-and-operations"></a><span data-ttu-id="7b91a-322">在 Finance and Operations 中查看执行跟踪</span><span class="sxs-lookup"><span data-stu-id="7b91a-322">Review the execution trace in Finance and Operations</span></span>

<span data-ttu-id="7b91a-323">除了 RCS，还有一些 Finance and Operations 版本可能提供针对 ER 框架设计器体验的功能。</span><span class="sxs-lookup"><span data-stu-id="7b91a-323">In addition to RCS, some versions of Finance and Operations might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="7b91a-324">这些 Finance and Operations 版本有一个可开启的**启用设计模式**选项。</span><span class="sxs-lookup"><span data-stu-id="7b91a-324">These versions of Finance and Operations have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="7b91a-325">可以在**电子申报参数**页（可从**电子申报**工作区打开该页）中的**常规**选项卡上找到此选项。</span><span class="sxs-lookup"><span data-stu-id="7b91a-325">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![在 Finance and Operations 的“电子申报参数”页中启用设计模式选项](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="7b91a-327">如果使用这些 Finance and Operations 版本中的一个，您可以直接在 Finance and Operations 中分析生成的性能跟踪的详细信息。</span><span class="sxs-lookup"><span data-stu-id="7b91a-327">If you use one of these versions of Finance and Operations, you can analyze the details of generated performance traces directly in Finance and Operations.</span></span> <span data-ttu-id="7b91a-328">无需将其从 Finance and Operation 中导出，再导入 RCS。</span><span class="sxs-lookup"><span data-stu-id="7b91a-328">You don't have to export them from Finance and Operation and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="7b91a-329">通过使用外部工具查看执行跟踪</span><span class="sxs-lookup"><span data-stu-id="7b91a-329">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="7b91a-330">配置用户参数</span><span class="sxs-lookup"><span data-stu-id="7b91a-330">Configure user parameters</span></span>

1. <span data-ttu-id="7b91a-331">在 Finance and Operations 中，转到**组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-331">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="7b91a-332">在**配置**页操作窗格中**配置**选项卡的**高级设置**组中，选择**用户参数**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-332">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="7b91a-333">在**用户参数**对话框**执行跟踪**部分的**执行跟踪格式**字段中，选择 **PerfView XML**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-333">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="7b91a-334">运行 ER 格式</span><span class="sxs-lookup"><span data-stu-id="7b91a-334">Run the ER format</span></span>

<span data-ttu-id="7b91a-335">重复本主题前面的[运行 ER 格式](#run-format)部分中的步骤生成一个新的性能跟踪。</span><span class="sxs-lookup"><span data-stu-id="7b91a-335">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="7b91a-336">请注意，Web 浏览器提供一个可供下载的 zip 文件。</span><span class="sxs-lookup"><span data-stu-id="7b91a-336">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="7b91a-337">这个文件中包含 PerfView 格式的性能跟踪。</span><span class="sxs-lookup"><span data-stu-id="7b91a-337">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="7b91a-338">然后可使用 PerfView 性能分析工具分析 ER 格式执行情况的详细信息。</span><span class="sxs-lookup"><span data-stu-id="7b91a-338">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![在 PerfView 中跟踪执行的 ER 格式的信息](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="7b91a-340">使用外部工具查看其中包含数据库查询的执行跟踪</span><span class="sxs-lookup"><span data-stu-id="7b91a-340">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="7b91a-341">因为已改进了 ER 框架，所以以 PerfView 格式生成的绩效跟踪现在提供更多有关 ER 格式执行的详细信息。</span><span class="sxs-lookup"><span data-stu-id="7b91a-341">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="7b91a-342">在 Microsoft Dynamics 365 for Finance and Operations 版本 10.0.4（2019 年 7 月）中，此跟踪中也可以包含对执行的 SQL 查询的详细信息。</span><span class="sxs-lookup"><span data-stu-id="7b91a-342">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="7b91a-343">配置用户参数</span><span class="sxs-lookup"><span data-stu-id="7b91a-343">Configure user parameters</span></span>

1. <span data-ttu-id="7b91a-344">在 Finance and Operations 中，转到**组织管理** \> **电子申报** \> **配置**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-344">In Finance and Operations, go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7b91a-345">在**配置**页操作窗格中**配置**选项卡的**高级设置**组中，选择**用户参数**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="7b91a-346">在**用户参数**对话框的**执行跟踪**部分中，设置以下参数：</span><span class="sxs-lookup"><span data-stu-id="7b91a-346">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="7b91a-347">在**执行跟踪格式**字段中，选择 **PerfView XML**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-347">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="7b91a-348">将**收集查询统计信息**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-348">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="7b91a-349">将**跟踪查询**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="7b91a-349">Set the **Trace query** option to **Yes**.</span></span>

    ![Finance and Operations 中的“用户参数”对话框](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="7b91a-351">运行 ER 格式</span><span class="sxs-lookup"><span data-stu-id="7b91a-351">Run the ER format</span></span>

<span data-ttu-id="7b91a-352">重复本主题前面的[运行 ER 格式](#run-format)部分中的步骤生成一个新的性能跟踪。</span><span class="sxs-lookup"><span data-stu-id="7b91a-352">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="7b91a-353">请注意，Web 浏览器提供一个可供下载的 zip 文件。</span><span class="sxs-lookup"><span data-stu-id="7b91a-353">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="7b91a-354">这个文件中包含 PerfView 格式的性能跟踪。</span><span class="sxs-lookup"><span data-stu-id="7b91a-354">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="7b91a-355">然后可使用 PerfView 性能分析工具分析 ER 格式执行情况的详细信息。</span><span class="sxs-lookup"><span data-stu-id="7b91a-355">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="7b91a-356">执行 ER 格式期间，此跟踪中现在包含 SQL 数据库访问权限的详细信息。</span><span class="sxs-lookup"><span data-stu-id="7b91a-356">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![在 PerfView 中跟踪执行的 ER 格式的信息](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

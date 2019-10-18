---
title: 使用电子申报自动执行测试
description: 本主题介绍如何使用电子申报 (ER) 框架的基准功能自动测试功能。
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 6da9447386e8e56e20507d985ebcdbfce934debd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181603"
---
# <a name="automate-testing-with-electronic-reporting"></a><span data-ttu-id="3a0c5-103">自动测试电子报告</span><span class="sxs-lookup"><span data-stu-id="3a0c5-103">Automate testing with Electronic reporting</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3a0c5-104">本主题介绍如何使用电子申报 (ER) 框架自动测试某些功能。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-104">This topic explains how you can use the Electronic reporting (ER) framework to automate testing of some functionality.</span></span> <span data-ttu-id="3a0c5-105">本主题中的示例演示如何自动测试供应商付款处理。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-105">The example in this topic shows how to automate the testing of vendor payment processing.</span></span>

<span data-ttu-id="3a0c5-106">供应商付款处理期间，应用程序使用 ER 框架生成付款文件和相应单据。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-106">The application uses the ER framework to generate payment files and corresponding documents during vendor payment processing.</span></span> <span data-ttu-id="3a0c5-107">ER 框架中包含数据模型、模型映射，以及格式组件，它们支持对不同付款类型进行付款处理和生成不同格式的单据。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-107">The ER framework consists of a data model, model mappings, and format components that support payment processing for different payment types and the generation of documents in different formats.</span></span> <span data-ttu-id="3a0c5-108">可以从 Microsoft Dynamics Lifecycle Services (LCS) 下载这些组件并导入到实例中。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-108">These components can be downloaded from Microsoft Dynamics Lifecycle Services (LCS) and imported into the instance.</span></span>

<span data-ttu-id="3a0c5-109">还可以自定义每个 Microsoft 组件，并将其用作您自己的自定义组件的基础。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-109">You also can customize each Microsoft component and use it as the basis of your own custom component.</span></span> <span data-ttu-id="3a0c5-110">通过创建自定义版本，您可以进行支持特定要求的更改。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-110">By creating a custom version, you can make changes that support specific requirements.</span></span> <span data-ttu-id="3a0c5-111">例如，可调整 ER 数据模型和 ER 模型映射以访问客户特定的应用程序数据，也可以更改 ER 格式以修改所生成单据的布局。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-111">For example, you can adjust the ER data model and ER model mapping to access customer-specific application data, or you can change an ER format to modify the layout of a generated document.</span></span>

<span data-ttu-id="3a0c5-112">可使用自定义的 ER 格式处理用于生成供应商付款的付款文件，以及处理控制报表。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-112">You can use customized ER formats to process payment files that generate vendor payments and also to process control reports.</span></span> <span data-ttu-id="3a0c5-113">ER 组件中支持版本控制。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-113">Versioning is supported in ER components.</span></span> <span data-ttu-id="3a0c5-114">因此，Microsoft 可以提供更新后的 ER 解决方案版本来处理供应商付款，而您可以通过为其重定基本值来自动将更新后的版本与自定义的组件合并。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-114">Therefore, Microsoft can provide updated versions of ER solutions for vendor payment processing, and you can automatically merge the updated version with your customized component by rebasing it.</span></span> <span data-ttu-id="3a0c5-115">但是，必须测试重定基本值后的版本，以确保其正常工作。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-115">However, you must test the rebased version to make sure that it works as you expect.</span></span>

<span data-ttu-id="3a0c5-116">ER 数据模型和 ER 模型映射支持大量 ER 格式，用于处理不同类型的付款和生成国家/地区特定的付款单据。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-116">ER data models and ER model mappings are common for many ER formats that are used to process payments of different types and to generate country/region-specific payment documents.</span></span> <span data-ttu-id="3a0c5-117">因此，非常需要自动执行用户接受度与集成测试，以便在多家公司中自动完成此操作，但是请注意各目标公司的国家/地区上下文，使用不同数据集，等等。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-117">Therefore, it's highly desirable to automate user acceptance and integration testing so that it's automatically done in multiple companies but considers the country/region context of each target company, uses different datasets, and so on.</span></span>

<span data-ttu-id="3a0c5-118">有关如何使用基于从配置提供程序收到的格式的自定义格式版本的详细信息，请参阅 [ER 通过采用该格式的新的基本版本升级格式](./tasks/er-upgrade-format.md)。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-118">For more information about how to create a custom version of a format that is based on the format that you received from a configuration provider, see [ER Upgrade your format by adopting a new, base version of that format](./tasks/er-upgrade-format.md).</span></span>

## <a name="key-concepts"></a><span data-ttu-id="3a0c5-119">重要概念</span><span class="sxs-lookup"><span data-stu-id="3a0c5-119">Key concepts</span></span>

<span data-ttu-id="3a0c5-120">高级功能用户不必编写源代码即可创作接受度和集成测试。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-120">Functional power users can author user acceptance and integration testing without having to write source code.</span></span>

- <span data-ttu-id="3a0c5-121">使用 ER 基准功能将生成的单据与主副本进行比较。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-121">Use the ER baseline feature to compare generated documents to master copies.</span></span> <span data-ttu-id="3a0c5-122">有关详细信息，请参阅[跟踪生成的报告结果并将其与基准值进行比较](er-trace-reports-compare-baseline.md)。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-122">For more information, see [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md).</span></span>
- <span data-ttu-id="3a0c5-123">使用任务录制器录制测试用例，并包含基准评估。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-123">Use Task recorder to record test cases, and include baseline assessment.</span></span> <span data-ttu-id="3a0c5-124">有关详细信息，请参阅[任务录制器](../user-interface/task-recorder.md)。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-124">For more information, see [Task recorder](../user-interface/task-recorder.md).</span></span>
- <span data-ttu-id="3a0c5-125">针对所需测试场景为测试用例分组。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-125">Group test cases for required test scenarios.</span></span> <span data-ttu-id="3a0c5-126">有关详细信息，请参阅[使用任务录制和 BPM 创建用户接受度测试库](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-126">For more information, see [Create user acceptance test libraries by using task recordings and BPM](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span></span>

    - <span data-ttu-id="3a0c5-127">使用 LCS 中的业务流程建模器 (BPM) 为用户接受度测试创建库。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-127">Use Business process modeler (BPM) in LCS to make libraries for user acceptance tests.</span></span>
    - <span data-ttu-id="3a0c5-128">在 Microsoft Azure DevOps Services (Azure DevOps) 中使用 BPM 测试库创建测试计划和测试套件。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-128">Use BPM test libraries to create a test plan and test suites in Microsoft Azure DevOps Services (Azure DevOps).</span></span>

<span data-ttu-id="3a0c5-129">高级功能用户可运行用户接受度和集成测试。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-129">Functional power users can run user acceptance and integration tests.</span></span>

- <span data-ttu-id="3a0c5-130">使用 Regression Suite Automation Tool (RSAT) 运行所需测试套件的测试用例。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-130">Use Regression suite automation tool (RSAT) to run test cases of the desired test suite.</span></span>
- <span data-ttu-id="3a0c5-131">将测试结果导出到 Azure DevOps，以及使用此服务调查这些结果。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-131">Report the results of the testing to Azure DevOps, and use this service to investigate those results.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3a0c5-132">先决条件</span><span class="sxs-lookup"><span data-stu-id="3a0c5-132">Prerequisites</span></span>

<span data-ttu-id="3a0c5-133">必须先完成以下先决条件，才能完成本主题中的任务：</span><span class="sxs-lookup"><span data-stu-id="3a0c5-133">Before you can complete the tasks in this topic, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="3a0c5-134">部署支持测试自动化的拓扑。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-134">Deploy a topology that supports test automation.</span></span> <span data-ttu-id="3a0c5-135">必须可以访问**系统管理员**角色的此拓扑的实例。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-135">You must have access to the instance of this topology for the **System administrator** role.</span></span> <span data-ttu-id="3a0c5-136">此拓扑中必须包含此示例中将使用的演示数据。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-136">This topology must contain the demo data that will be used in this example.</span></span> <span data-ttu-id="3a0c5-137">有关详细信息，请参阅[部署支持连续生成和测试自动化的拓扑](../perf-test/continuous-build-test-automation.md)。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-137">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span>
- <span data-ttu-id="3a0c5-138">若要自动运行用户接受度和集成测试，必须在要测试的拓扑中安装 RSAT，并以适当方式配置。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-138">To run user acceptance and integration tests automatically, you must install RSAT in the topology that you're using and configure it in the appropriate manner.</span></span> <span data-ttu-id="3a0c5-139">有关如何安装和配置 RSAT 以支持 Finance and Operations 应用程序和 Azure DevOps 的信息，请参阅 [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357)。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-139">For information about how to install and configure RSAT and configure it to work with Finance and Operations apps and Azure DevOps, see [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span></span> <span data-ttu-id="3a0c5-140">请注意有关使用此工具的先决条件。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-140">Pay attention to the prerequisites for using the tool.</span></span> <span data-ttu-id="3a0c5-141">下图显示 RSAT 设置的示例。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-141">The following illustration shows an example of the RSAT settings.</span></span> <span data-ttu-id="3a0c5-142">蓝色方框中的是用于指定 Azure DevOps 的访问权限的参数。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-142">The blue rectangle encloses the parameters that specify access to Azure DevOps.</span></span> <span data-ttu-id="3a0c5-143">蓝色方框内的是用于指定实例的访问权限的参数。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-143">The green rectangle encloses the parameters that specify access to the instance.</span></span>

    <span data-ttu-id="3a0c5-144">![RSAT 设置](media/GER-Configure.png "“RSAT 设置”对话框的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-144">![RSAT settings](media/GER-Configure.png "Screenshot of the RSAT Settings dialog box")</span></span>

- <span data-ttu-id="3a0c5-145">若要组织套件中的测试用例以帮助确保正确的执行顺序，以便收集测试的执行日志来进一步报告和调查，必须可以从部署的拓扑访问 Azure DevOps。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-145">To organize test cases in suites to help guarantee the correct execution sequence, so that you can collect logs of test executions for further reporting and investigation, you must have access to Azure DevOps from the deployed topology.</span></span>
- <span data-ttu-id="3a0c5-146">若要完成本主题中的示例，建议下载 [ER RSAT 测试的用法](https://go.microsoft.com/fwlink/?linkid=874684)。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-146">To complete the example in this topic, we recommend that you download [ER usage for RSAT tests](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="3a0c5-147">这个 zip 文件中包含以下任务指南：</span><span class="sxs-lookup"><span data-stu-id="3a0c5-147">This zip file contains the following task guides:</span></span>

    | <span data-ttu-id="3a0c5-148">内容</span><span class="sxs-lookup"><span data-stu-id="3a0c5-148">Content</span></span>                                           | <span data-ttu-id="3a0c5-149">文件名和位置</span><span class="sxs-lookup"><span data-stu-id="3a0c5-149">File name and location</span></span> |
    |---------------------------------------------------|------------------------|
    | <span data-ttu-id="3a0c5-150">用于为测试准备数据的示例任务录制</span><span class="sxs-lookup"><span data-stu-id="3a0c5-150">Sample task recording to prepare data for testing</span></span> | <span data-ttu-id="3a0c5-151">Prepare\\Recording.xml</span><span class="sxs-lookup"><span data-stu-id="3a0c5-151">Prepare\\Recording.xml</span></span> |
    | <span data-ttu-id="3a0c5-152">用于处理供应商付款的示例任务录制</span><span class="sxs-lookup"><span data-stu-id="3a0c5-152">Sample task recording to process vendor payment</span></span>   | <span data-ttu-id="3a0c5-153">Process\\Recording.xml</span><span class="sxs-lookup"><span data-stu-id="3a0c5-153">Process\\Recording.xml</span></span> |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a><span data-ttu-id="3a0c5-154">准备应付帐款模块以处理供应商付款</span><span class="sxs-lookup"><span data-stu-id="3a0c5-154">Prepare the Accounts payable module to process vendor payments</span></span>

1. <span data-ttu-id="3a0c5-155">登录您的实例。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-155">Sign in to your instance.</span></span>
2. <span data-ttu-id="3a0c5-156">从 LCS 下载以下 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-156">Download the following ER configurations from LCS.</span></span> <span data-ttu-id="3a0c5-157">有关说明，请参阅 [ER 从 Lifecycle Services 导入配置](./tasks/er-import-configuration-lifecycle-services.md)。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-157">For instructions, see [ER Import a configuration from Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).</span></span>

    - <span data-ttu-id="3a0c5-158">**付款模型** ER 模型配置</span><span class="sxs-lookup"><span data-stu-id="3a0c5-158">**Payment model** ER model configuration</span></span>
    - <span data-ttu-id="3a0c5-159">**付款模型映射 1611** ER 模型映射配置</span><span class="sxs-lookup"><span data-stu-id="3a0c5-159">**Payment model mapping 1611** ER model mapping configuration</span></span>
    - <span data-ttu-id="3a0c5-160">**BACS (UK)** ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="3a0c5-160">**BACS (UK)** ER format configuration</span></span>

    <span data-ttu-id="3a0c5-161">![电子申报配置](media/GER-Configurations.png "电子申报中的“配置”页的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-161">![Electronic reporting configurations](media/GER-Configurations.png "Screenshot of the Configurations page in Electronic reporting")</span></span>

3. <span data-ttu-id="3a0c5-162">选择 **GBSI** 演示数据公司，该公司在英国拥有国家/地区上下文。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-162">Select the **GBSI** demo data company, which has a country/region context in Great Britain.</span></span>
4. <span data-ttu-id="3a0c5-163">配置应付帐款参数：</span><span class="sxs-lookup"><span data-stu-id="3a0c5-163">Configure Accounts payable parameters:</span></span>

    1. <span data-ttu-id="3a0c5-164">转至**应付帐款 \> 付款设置 \> 付款方式**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-164">Go to **Accounts payable \> Payment setup \> Methods of payment**.</span></span>
    2. <span data-ttu-id="3a0c5-165">选择**电子**付款方式。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-165">Select the **Electronic** method of payment.</span></span>
    3. <span data-ttu-id="3a0c5-166">配置所选付款方式，以便使用您之前下载的 **BACS (UK)** ER 格式处理客户付款：</span><span class="sxs-lookup"><span data-stu-id="3a0c5-166">Configure the selected method of payment so that it uses the **BACS (UK)** ER format that you downloaded earlier for vendor payment processing:</span></span>

        1. <span data-ttu-id="3a0c5-167">在**文件格式**快速选项卡上，将**一般电子导出格式**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-167">On the **File formats** FastTab, set the **Generic electronic Export format** option to **Yes**.</span></span>
        2. <span data-ttu-id="3a0c5-168">在**导出格式配置**字段中，选择 **BACS (UK)**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-168">In the **Export format configuration** field, select **BACS (UK)**.</span></span>

    <span data-ttu-id="3a0c5-169">![“付款方式”页](media/GER-APParameters.png "“付款方式”页的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-169">![Methods of payment page](media/GER-APParameters.png "Screenshot of the Methods of payment page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a0c5-170">如果有为了支持自定义设置而为此 ER 格式创建的派生版本，可以在**电子**付款方式中选择此配置。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-170">If you have the derived version of this ER format that was created to support customizations, you can select this configuration in the **Electronic** method of payment.</span></span>

5. <span data-ttu-id="3a0c5-171">创建示例供应商付款：</span><span class="sxs-lookup"><span data-stu-id="3a0c5-171">Create an example vendor payment:</span></span>

    1. <span data-ttu-id="3a0c5-172">转到**应付帐款 \> 付款 \> 付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-172">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
    2. <span data-ttu-id="3a0c5-173">确保尚未过帐付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-173">Make sure that you haven't posted the payment journal.</span></span>

        <span data-ttu-id="3a0c5-174">![“付款日记帐”页](media/GER-APJournal.png "“付款日记帐”页的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-174">![Payment journal page](media/GER-APJournal.png "Screenshot of the Payment journal page")</span></span>

    3. <span data-ttu-id="3a0c5-175">选择**行**。然后输入包含以下信息的行。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-175">Select **Lines**, and enter a line that has the following information.</span></span>

        | <span data-ttu-id="3a0c5-176">字段</span><span class="sxs-lookup"><span data-stu-id="3a0c5-176">Field</span></span>               | <span data-ttu-id="3a0c5-177">示例值</span><span class="sxs-lookup"><span data-stu-id="3a0c5-177">Example value</span></span>   |
        |---------------------|-----------------|
        | <span data-ttu-id="3a0c5-178">供应商名称</span><span class="sxs-lookup"><span data-stu-id="3a0c5-178">Vendor name</span></span>         | <span data-ttu-id="3a0c5-179">GB\_SI\_000001</span><span class="sxs-lookup"><span data-stu-id="3a0c5-179">GB\_SI\_000001</span></span>  |
        | <span data-ttu-id="3a0c5-180">借记</span><span class="sxs-lookup"><span data-stu-id="3a0c5-180">Debit</span></span>               | <span data-ttu-id="3a0c5-181">1,000.00</span><span class="sxs-lookup"><span data-stu-id="3a0c5-181">1,000.00</span></span>        |
        | <span data-ttu-id="3a0c5-182">货币</span><span class="sxs-lookup"><span data-stu-id="3a0c5-182">Currency</span></span>            | <span data-ttu-id="3a0c5-183">GBP</span><span class="sxs-lookup"><span data-stu-id="3a0c5-183">GBP</span></span>             |
        | <span data-ttu-id="3a0c5-184">对方科目类型</span><span class="sxs-lookup"><span data-stu-id="3a0c5-184">Offset account type</span></span> | <span data-ttu-id="3a0c5-185">银行</span><span class="sxs-lookup"><span data-stu-id="3a0c5-185">Bank</span></span>            |
        | <span data-ttu-id="3a0c5-186">对方科目</span><span class="sxs-lookup"><span data-stu-id="3a0c5-186">Offset account</span></span>      | <span data-ttu-id="3a0c5-187">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="3a0c5-187">GBSI OPER</span></span>       |
        | <span data-ttu-id="3a0c5-188">付款方式</span><span class="sxs-lookup"><span data-stu-id="3a0c5-188">Method of payment</span></span>   | <span data-ttu-id="3a0c5-189">电子</span><span class="sxs-lookup"><span data-stu-id="3a0c5-189">Electronic</span></span>      |

    <span data-ttu-id="3a0c5-190">![“供应商付款”页](media/GER-APJournalLines.png "“供应商付款”页的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-190">![Vendor payments page](media/GER-APJournalLines.png "Screenshot of the Vendor payments page")</span></span>

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a><span data-ttu-id="3a0c5-191">准备 ER 框架以测试供应商付款处理</span><span class="sxs-lookup"><span data-stu-id="3a0c5-191">Prepare the ER framework to test vendor payment processing</span></span>

### <a name="configure-er-parameters"></a><span data-ttu-id="3a0c5-192">配置 ER 参数</span><span class="sxs-lookup"><span data-stu-id="3a0c5-192">Configure ER parameters</span></span>

1. <span data-ttu-id="3a0c5-193">转到**组织管理 \> 电子报表 \> 电子报表参数**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-193">Go to **Organization administration \> Electronic reporting \> Electronic reporting parameters**.</span></span>
2. <span data-ttu-id="3a0c5-194">在**附件**选项卡上**基准**字段中，选择**文件**作为文档管理 (DM) 框架用于保留作为 DM 附件与基准功能有关的单据的单据类型。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-194">On the **Attachments** tab, in the **Baseline** field, select **File** as the document type that the Document management (DM) framework uses to keep documents that are related to the baseline feature as DM attachments.</span></span>

    <span data-ttu-id="3a0c5-195">![“电子申报参数”页](media/GER-ERParameters.png "“电子申报参数”页的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-195">![Electronic reporting parameters page](media/GER-ERParameters.png "Screenshot of the Electronic reporting parameters page")</span></span>

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a><span data-ttu-id="3a0c5-196">生成与供应商付款有关的单据的基准副本</span><span class="sxs-lookup"><span data-stu-id="3a0c5-196">Generate baseline copies of vendor payment–related documents</span></span>

1. <span data-ttu-id="3a0c5-197">转到**应付帐款 \> 付款 \> 付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-197">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="3a0c5-198">选择**行**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-198">Select **Lines**.</span></span>
3. <span data-ttu-id="3a0c5-199">选择**生成付款**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-199">Select **Generate payments**.</span></span>
4. <span data-ttu-id="3a0c5-200">选择**电子**付款方式。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-200">Select the **Electronic** method of payment.</span></span>
5. <span data-ttu-id="3a0c5-201">选择 **GBSI OPER** 银行帐户。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-201">Select the **GBSI OPER** bank account.</span></span>
6. <span data-ttu-id="3a0c5-202">将**打印控制报表**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-202">Set the **Print control report** option to **Yes**.</span></span>
7. <span data-ttu-id="3a0c5-203">将生成的输出作为 zip 文件下载。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-203">Download the generated output as a zip file.</span></span>
8. <span data-ttu-id="3a0c5-204">打开下载的文件。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-204">Open the downloaded file.</span></span>
9. <span data-ttu-id="3a0c5-205">从下载的文件提取以下文件：</span><span class="sxs-lookup"><span data-stu-id="3a0c5-205">Extract following files from the downloaded file:</span></span>

    - <span data-ttu-id="3a0c5-206">**File** 文本格式的付款文件</span><span class="sxs-lookup"><span data-stu-id="3a0c5-206">**File** payment file in text format</span></span>
    - <span data-ttu-id="3a0c5-207">**ERVendOutPaymControlReport** XLSX 格式的控制报表文件</span><span class="sxs-lookup"><span data-stu-id="3a0c5-207">**ERVendOutPaymControlReport** control report file in XLSX format</span></span>

    <span data-ttu-id="3a0c5-208">![提取的文件](media/GER-APJournalProcessed.png "Windows 资源管理器中提取的文件名的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-208">![Extracted files](media/GER-APJournalProcessed.png "Screenshot of extracted file names in Windows explorer")</span></span>

### <a name="turn-on-the-er-baseline-feature"></a><span data-ttu-id="3a0c5-209">开启 ER 基准功能</span><span class="sxs-lookup"><span data-stu-id="3a0c5-209">Turn on the ER baseline feature</span></span>

1. <span data-ttu-id="3a0c5-210">转到**组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-210">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="3a0c5-211">在操作窗格上的**配置**选项卡上，选择**用户参数**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-211">On the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
3. <span data-ttu-id="3a0c5-212">将**以调试模式运行**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-212">Set the **Run in debug mode** option to **Yes**.</span></span>

<span data-ttu-id="3a0c5-213">通过开启**以调试模式运行**参数，在执行用于生成传出单据的任何 ER 格式之后强制 ER 框架执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="3a0c5-213">By turning on the **Run in debug mode** parameter, you force the ER framework to perform the following actions after the execution of any ER format that generates outgoing documents:</span></span>

1. <span data-ttu-id="3a0c5-214">确定是否为所执行 ER 格式的任何组件配置了基准。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-214">Determine whether a baseline was configured for any of components of the executed ER format.</span></span>
2. <span data-ttu-id="3a0c5-215">确定配置的每个基准（已登录公司的公司代码、生成的输出的文件名和文件扩展名等）在当前条件中是否适用。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-215">Determine whether each configured baseline is applicable in the current conditions (company code of the signed-in company, file name and file name extension of the generated output, and so on).</span></span>
3. <span data-ttu-id="3a0c5-216">对每个适用的基准执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="3a0c5-216">For each applicable baseline, perform the following actions:</span></span>

    1. <span data-ttu-id="3a0c5-217">将执行 ER 格式期间生成的输出与相应基准进行比较。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-217">Compare the output that is generated during execution of the ER format with the corresponding baseline.</span></span>
    2. <span data-ttu-id="3a0c5-218">将比较结果存储到 ER 配置调试日志中。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-218">Store the results of the comparison in the ER configurations debug log.</span></span>

### <a name="configure-er-baselines-for-vendor-payment-processing"></a><span data-ttu-id="3a0c5-219">为供应商付款处理配置 ER 基准</span><span class="sxs-lookup"><span data-stu-id="3a0c5-219">Configure ER baselines for vendor payment processing</span></span>

1. <span data-ttu-id="3a0c5-220">转到**组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-220">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="3a0c5-221">选择**基准**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-221">Select **Baselines**.</span></span>
3. <span data-ttu-id="3a0c5-222">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-222">Select **New**.</span></span>
4. <span data-ttu-id="3a0c5-223">在**引用**字段中，选择 **BACS (UK)** 格式。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-223">In the **Reference** field, select the **BACS (UK)** format.</span></span>
5. <span data-ttu-id="3a0c5-224">选择**附件**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-224">Select **Attachments**.</span></span>
6. <span data-ttu-id="3a0c5-225">为供应商付款文件添加新基准：</span><span class="sxs-lookup"><span data-stu-id="3a0c5-225">Add a new baseline for the vendor payment file:</span></span>

    1. <span data-ttu-id="3a0c5-226">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-226">Select **New**.</span></span>
    2. <span data-ttu-id="3a0c5-227">在**类型**字段中，选择您在 ER 参数中配置 DM 文档类型**文件**以存储基准项目。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-227">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="3a0c5-228">浏览并选择本地存储的文本格式的付款文件 **File**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-228">Browse to select the locally saved **File** payment file in text format.</span></span>
    4. <span data-ttu-id="3a0c5-229">在**说明**字段中，输入**付款 TXT 文件**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-229">In the **Description** field, enter **Payment TXT file**.</span></span>

7. <span data-ttu-id="3a0c5-230">为供应商付款的控制报表添加新基准：</span><span class="sxs-lookup"><span data-stu-id="3a0c5-230">Add a new baseline for the control report for the vendor payment:</span></span>

    1. <span data-ttu-id="3a0c5-231">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-231">Select **New**.</span></span>
    2. <span data-ttu-id="3a0c5-232">在**类型**字段中，选择您在 ER 参数中配置 DM 文档类型**文件**以存储基准项目。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-232">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="3a0c5-233">浏览并选择本地存储的 XLSX 格式的 **ERVendOutPaymControlReport** 控制报表文件。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-233">Browse to select the locally saved **ERVendOutPaymControlReport** control report file in XLSX format.</span></span>
    4. <span data-ttu-id="3a0c5-234">在**说明**字段中，输入**付款 XLSX 控制报表**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-234">In the **Description** field, enter **Payment XLSX control report**.</span></span>

    <span data-ttu-id="3a0c5-235">![供应商付款文件和控制报表的基准](media/GER-BaselineAttachments.png "已选择了付款 XLSX 控制报表的“配置”页的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-235">![Baselines for the vendor payment file and control report](media/GER-BaselineAttachments.png "Screenshot of the Configurations page with the Payment XLSX control report selected")</span></span>

8. <span data-ttu-id="3a0c5-236">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-236">Close the page.</span></span>
9. <span data-ttu-id="3a0c5-237">在**基准**快速选项卡上，选择**新建**为付款文件配置一个基准：</span><span class="sxs-lookup"><span data-stu-id="3a0c5-237">On the **Baselines** FastTab, select **New** to configure a baseline for the payment file:</span></span>

    1. <span data-ttu-id="3a0c5-238">将行命名为**付款文件的基准设置**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-238">Name the line **Baseline setting for payment file**.</span></span>
    2. <span data-ttu-id="3a0c5-239">在**文件组件名称**字段中，选择**文件**将此基准应用于 ER 格式输出以生成 BACS (UK) 文本格式的付款文件。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-239">In the **File component name** field, select **file** to apply this baseline to the ER format output that generates the payment file in BACS (UK) text format.</span></span>
    3. <span data-ttu-id="3a0c5-240">在**公司**字段中，选择 **GBSI**，以便在 GBSI 公司中运行 **BACS (UK)** ER 格式时应用此基准。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-240">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="3a0c5-241">在**文件名掩码**字段中，输入 **\*.TXT**，以便将此基准仅应用于**文件**格式组件的具有 **.txt** 文件扩展名的输出。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-241">In **File name mask** field, enter **\*.TXT** to apply this baseline only to outputs of the **file** format component that have the **.txt** file name extension.</span></span>
    5. <span data-ttu-id="3a0c5-242">在**基准**字段中，选择**付款 TXT 文件**，以便将此基准用于与生成的输出进行比较。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-242">In the **Baseline** field, select **Payment TXT file** so that this baseline is used for comparison with the generated output.</span></span>

10. <span data-ttu-id="3a0c5-243">选择**新建**为控制报表配置基准：</span><span class="sxs-lookup"><span data-stu-id="3a0c5-243">Select **New** to configure a baseline for the control report:</span></span>

    1. <span data-ttu-id="3a0c5-244">将行命名为**控制报表的基准设置**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-244">Name the line **Baseline setting for control report**.</span></span>
    2. <span data-ttu-id="3a0c5-245">在**文件组件名称**字段中，选择 **ERVendOutPaymControlReport** 将此基准应用于 ER 格式输出以生成控制报表。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-245">In the **File component name** field, select **ERVendOutPaymControlReport** to apply this baseline to the ER format output that generates the control report.</span></span>
    3. <span data-ttu-id="3a0c5-246">在**公司**字段中，选择 **GBSI**，以便在 GBSI 公司中运行 **BACS (UK)** ER 格式时应用此基准。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-246">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="3a0c5-247">在**文件名掩码**字段中，输入 **\*.XLSX**，以便将此基准仅应用于 **ERVendOutPaymControlReport** 格式组件的具有 **.xslx** 文件扩展名的输出。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-247">In **File name mask** field, enter **\*.XLSX** to apply this baseline only to outputs of the **ERVendOutPaymControlReport** format component that have the **.xslx** file name extension.</span></span>
    5. <span data-ttu-id="3a0c5-248">在**基准**字段中，选择**付款 XLSX 控制报表**，以便将此基准用于与生成的输出进行比较。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-248">In the **Baseline** field, select **Payment XLSX control report** so that this baseline is used for comparison with the generated output.</span></span>

    <span data-ttu-id="3a0c5-249">![“配置”页上的“基准”快速选项卡](media/GER-BaselineRules.png "“配置”页上的“基准”快速选项卡的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-249">![Baselines FastTab on the Configurations page](media/GER-BaselineRules.png "Screenshot of the Baselines FastTab on the Configurations page")</span></span>

## <a name="record-tests-to-validate-vendor-payment-processing"></a><span data-ttu-id="3a0c5-250">录制测试以验证供应商付款处理</span><span class="sxs-lookup"><span data-stu-id="3a0c5-250">Record tests to validate vendor payment processing</span></span>

<span data-ttu-id="3a0c5-251">高级功能用户可录制自己的步骤以测试供应商付款处理。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-251">As a functional power user, you can record your own steps to test vendor payment processing.</span></span> <span data-ttu-id="3a0c5-252">建议播放（如果需要，并编辑）之前下载的**Prepare\\Recording.xml** 任务录制。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-252">We recommend that you play (and edit, as required) the **Prepare\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="3a0c5-253">此录制用于将所有测试数据设置为正确状态。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-253">This recording is used to set all testing data to the correct state.</span></span> <span data-ttu-id="3a0c5-254">需要执行此步骤，因为可以多次进行测试，并且每次测试都必须使用同一种状态的数据。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-254">That step is required because the testing can be done many times, and every test must use data that is in the same state.</span></span>

### <a name="reset-user-settings"></a><span data-ttu-id="3a0c5-255">重置用户设置</span><span class="sxs-lookup"><span data-stu-id="3a0c5-255">Reset user settings</span></span>

1. <span data-ttu-id="3a0c5-256">打开默认仪表板。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-256">Open the default dashboard.</span></span>
2. <span data-ttu-id="3a0c5-257">选择**设置**按钮（齿轮符号）。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-257">Select the **Settings** button (the gear symbol).</span></span>
3. <span data-ttu-id="3a0c5-258">选择**用户选项**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-258">Select **User options**.</span></span>
4. <span data-ttu-id="3a0c5-259">选择**应用数据**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-259">Select **Usage data**.</span></span>
5. <span data-ttu-id="3a0c5-260">选择**重置**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-260">Select **Reset**.</span></span>
6. <span data-ttu-id="3a0c5-261">选择**是**确认要重置应用数据。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-261">Select **Yes** to confirm that you want to reset usage data.</span></span>
7. <span data-ttu-id="3a0c5-262">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-262">Close the page.</span></span>

### <a name="record-the-steps-to-prepare-data-for-testing"></a><span data-ttu-id="3a0c5-263">录制步骤为测试准备数据</span><span class="sxs-lookup"><span data-stu-id="3a0c5-263">Record the steps to prepare data for testing</span></span>

1. <span data-ttu-id="3a0c5-264">选择**设置**按钮（齿轮符号）。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-264">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="3a0c5-265">选择**任务录制器**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-265">Select **Task recorder**.</span></span>
3. <span data-ttu-id="3a0c5-266">选择**播放录制**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-266">Select **Playback recording**.</span></span>
4. <span data-ttu-id="3a0c5-267">选择**从此 PC 中打开**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-267">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="3a0c5-268">选择**浏览**，然后选择本地保存的 **Prepare\\Recording.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-268">Select **Browse**, and select the locally save **Prepare\\Recording.xml** file.</span></span>
6. <span data-ttu-id="3a0c5-269">选择**开始**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-269">Select **Start**.</span></span>
7. <span data-ttu-id="3a0c5-270">重复选择**播放下一个等待步骤**，直到播放完录制中的所有步骤。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-270">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="3a0c5-271">此任务录制执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="3a0c5-271">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="3a0c5-272">将处理付款行的状态设置为**无**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-272">Set the status of the processed payment line to **None**.</span></span>

    <span data-ttu-id="3a0c5-273">![任务录制步骤 3 到 4](media/GER-Recording1Review1.png "任务录制步骤 3 到 4 的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-273">![Task recording steps 3 through 4](media/GER-Recording1Review1.png "Screenshot of task recording steps 3 through 4")</span></span>

2. <span data-ttu-id="3a0c5-274">开启**以调试模式运行** ER 用户参数。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-274">Turn on the **Run in debug mode** ER user parameter.</span></span>

    <span data-ttu-id="3a0c5-275">![任务录制步骤 9 到 10](media/GER-Recording1Review2.png "任务录制步骤 9 到 10 的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-275">![Task recording steps 9 through 10](media/GER-Recording1Review2.png "Screenshot of task recording steps 9 through 10")</span></span>

3. <span data-ttu-id="3a0c5-276">清除其中包含所生成文件与基准的比较结果的 ER 调试日志。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-276">Clean up the ER debug log that contains the results of the comparison of generated files to baselines.</span></span>

    <span data-ttu-id="3a0c5-277">![任务录制步骤 13 到 15](media/GER-Recording1Review3.png "任务录制步骤 13 到 15 的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-277">![Task recording steps 13 through 15](media/GER-Recording1Review3.png "Screenshot of task recording steps 13 through 15")</span></span>

### <a name="record-the-steps-to-test-vendor-payment-processing"></a><span data-ttu-id="3a0c5-278">录制这些步骤以测试供应商付款处理</span><span class="sxs-lookup"><span data-stu-id="3a0c5-278">Record the steps to test vendor payment processing</span></span>

<span data-ttu-id="3a0c5-279">建议播放（如果需要，并编辑）之前下载的 **Process\\Recording.xml** 任务录制。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-279">We recommend that you play (and edit, as required) the **Process\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="3a0c5-280">此录制用于处理供应商付款和验证生成的单据与相应基准的比较结果。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-280">This recording is used to process vendor payments and validate the results of the comparison of generated documents to corresponding baselines.</span></span>

1. <span data-ttu-id="3a0c5-281">选择**设置**按钮（齿轮符号）。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-281">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="3a0c5-282">选择**任务录制器**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-282">Select **Task recorder**.</span></span>
3. <span data-ttu-id="3a0c5-283">选择**播放录制**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-283">Select **Playback recording**.</span></span>
4. <span data-ttu-id="3a0c5-284">选择**从此 PC 中打开**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-284">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="3a0c5-285">选择**浏览**，然后选择本地保存的 **Process\\Recording.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-285">Select **Browse**, and select the locally saved **Process\\Recording.xml** file.</span></span>
6. <span data-ttu-id="3a0c5-286">选择**开始**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-286">Select **Start**.</span></span>
7. <span data-ttu-id="3a0c5-287">重复选择**播放下一个等待步骤**，直到播放完录制中的所有步骤。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-287">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="3a0c5-288">此任务录制执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="3a0c5-288">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="3a0c5-289">启动供应商付款处理。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-289">Start vendor payment processing.</span></span>
2. <span data-ttu-id="3a0c5-290">选择正确的运行时参数，然后开启控制报表的生成。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-290">Select the correct runtime parameters, and turn on generation of a control report.</span></span>

    <span data-ttu-id="3a0c5-291">![任务录制步骤 3 到 8](media/GER-Recording2Review1.png "任务录制步骤 3 到 8 的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-291">![Task recording steps 3 through 8](media/GER-Recording2Review1.png "Screenshot of task recording steps 3 through 8")</span></span>

3. <span data-ttu-id="3a0c5-292">访问 ER 调试日志以录制所生成输出与相应基准的比较结果。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-292">Access the ER debug log to record the results of the comparison of generated outputs to corresponding baselines.</span></span>

    <span data-ttu-id="3a0c5-293">在 ER 调试日志中，**生成的文本**字段中将显示比较结果。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-293">In the ER debug log, the results of the comparison appear in the **Generated text** field.</span></span> <span data-ttu-id="3a0c5-294">**格式组件**和**生成日志条目的格式路径**字段引用为其比较所生成输出与基准的文件组件。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-294">The **Format component** and **Format path that caused a log entry** fields refer to the file component for which the generated output has been compared to the baseline.</span></span>

    <span data-ttu-id="3a0c5-295">![“电子申报运行日志”页上的条目](media/GER-ERDebugLog.png "“电子申报运行日志”页上的条目的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-295">![Entries on the Electronic reporting run logs page](media/GER-ERDebugLog.png "Screenshot of entries on the Electronic reporting run logs page")</span></span>

4. <span data-ttu-id="3a0c5-296">将使用**验证**任务录制器选项和选择 **当前值**录制当前输出与基准的比较。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-296">The comparison of the current output to the baseline is recorded by using the **Validate** Task recorder option and selecting  **Current Value**.</span></span>

    <span data-ttu-id="3a0c5-297">![使用“验证”选项比较当前值](media/GER-TRRecordValidation.png "使用“验证”选项比较当前值的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-297">![Using the Validate option for comparison with the current value](media/GER-TRRecordValidation.png "Screenshot of using the Validate option for comparison with the current value")</span></span>

    <span data-ttu-id="3a0c5-298">下图显示任务录制中录制的验证步骤的情况。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-298">The following illustration shows what the recorded validation steps look like in the task recording.</span></span>

    <span data-ttu-id="3a0c5-299">![任务录制步骤 13 和 15](media/GER-Recording2Review2.png "任务录制步骤 13 和 15 的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-299">![Task recording steps 13 and 15](media/GER-Recording2Review2.png "Screenshot of task recording steps 13 and 15")</span></span>

## <a name="add-the-recorded-tests-to-azure-devops"></a><span data-ttu-id="3a0c5-300">将录制的测试添加到 Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="3a0c5-300">Add the recorded tests to Azure DevOps</span></span>

1. <span data-ttu-id="3a0c5-301">打开 Azure DevOps 环境。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-301">Open the Azure DevOps environment.</span></span>
2. <span data-ttu-id="3a0c5-302">选择[配置工具时](#prerequisites)在 RSAT 参数中定义的项目。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-302">Select the project that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
3. <span data-ttu-id="3a0c5-303">选择[配置工具时](#prerequisites)在 RSAT 参数中定义的测试计划。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-303">Select the test plan that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
4. <span data-ttu-id="3a0c5-304">为所选测试计划创建新测试用例：</span><span class="sxs-lookup"><span data-stu-id="3a0c5-304">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="3a0c5-305">将测试用例命名为**准备数据以测试供应商对电子付款的处理**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-305">Name the test case **Prepare data to test processing of vendor's electronic payment**.</span></span>
    2. <span data-ttu-id="3a0c5-306">附加 **Prepare** 文件夹中您之前下载的 **Recording.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-306">Attach the **Recording.xml** file from the **Prepare** folder that you downloaded earlier.</span></span>

5. <span data-ttu-id="3a0c5-307">为所选测试计划创建新测试用例：</span><span class="sxs-lookup"><span data-stu-id="3a0c5-307">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="3a0c5-308">将测试用例命名为**使用 ER 格式 BACS (UK) 测试对供应商付款的处理**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-308">Name the test case **Test processing of vendor payments by using ER format BACS (UK)**.</span></span>
    2. <span data-ttu-id="3a0c5-309">附加 **Process** 文件夹中您之前下载的 **Recording.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-309">Attach the **Recording.xml** file from the **Process** folder that you downloaded earlier.</span></span>

    <span data-ttu-id="3a0c5-310">![所选测试计划的新测试用例](media/GER-RSAT-DevOps-Tests-Passed.png "所选测试计划的新测试用例的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-310">![New test cases for the selected test plan](media/GER-RSAT-DevOps-Tests-Passed.png "Screenshot of the new test cases for the selected test plan")</span></span>

> [!NOTE]
> <span data-ttu-id="3a0c5-311">注意所添加测试的正确执行顺序。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-311">Pay attention to the correct execution order of the tests that are added.</span></span>

## <a name="prepare-rsat-to-run-the-recorded-tests"></a><span data-ttu-id="3a0c5-312">准备 RSAT 以运行录制的测试</span><span class="sxs-lookup"><span data-stu-id="3a0c5-312">Prepare RSAT to run the recorded tests</span></span>

### <a name="load-the-tests-from-azure-devops-to-rsat"></a><span data-ttu-id="3a0c5-313">将测试从 Azure DevOps 加载到 RSAT</span><span class="sxs-lookup"><span data-stu-id="3a0c5-313">Load the tests from Azure DevOps to RSAT</span></span>

1. <span data-ttu-id="3a0c5-314">打开当前拓扑中的本地 RSAT 应用程序。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-314">Open the local RSAT application in the current topology.</span></span>
2. <span data-ttu-id="3a0c5-315">选择**加载**以将 Azure DevOps 中的当前测试加载到 RSAT 中。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-315">Select **Load** to load the tests that currently reside in Azure DevOps into RSAT.</span></span>

    <span data-ttu-id="3a0c5-316">![加载到 RSAT 中的测试](media/GER-RSAT-RSAT-Tests-Loaded.png "加载到 RSAT 中的测试的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-316">![Tests loaded into RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "Screenshot of the tests loaded into RSAT")</span></span>

### <a name="create-automation-and-parameters-files"></a><span data-ttu-id="3a0c5-317">创建自动化和参数文件</span><span class="sxs-lookup"><span data-stu-id="3a0c5-317">Create automation and parameters files</span></span>

1. <span data-ttu-id="3a0c5-318">在 RSAT 中，选择从 Azure DevOps 加载的测试。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-318">In RSAT, select the tests that you loaded from Azure DevOps.</span></span>
2. <span data-ttu-id="3a0c5-319">选择**新建**以创建 RSAT 自动化和参数文件。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-319">Select **New** to create RSAT automation and parameters files.</span></span>

    <span data-ttu-id="3a0c5-320">![在 RSAT 汇总创建的 RSAT 自动化和参数文件](media/GER-RSAT-RSAT-Tests-Initiated.png "在 RSAT 汇总创建的 RSAT 自动化和参数文件的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-320">![RSAT automation and parameters files created in RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "Screenshot of the RSAT automation and parameters files created in RSAT")</span></span>

### <a name="modify-the-parameters-files"></a><span data-ttu-id="3a0c5-321">修改参数文件</span><span class="sxs-lookup"><span data-stu-id="3a0c5-321">Modify the parameters files</span></span>

1. <span data-ttu-id="3a0c5-322">在 RSAT 中，选择**准备数据以测试供应商对电子付款的处理**测试用例。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-322">In RSAT, select the **Prepare data to test processing of vendor's electronic payment** test case.</span></span>
2. <span data-ttu-id="3a0c5-323">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-323">Select **Edit**.</span></span>
3. <span data-ttu-id="3a0c5-324">在打开的 Microsoft Excel 工作簿中 **General** 工作表上，将公司代码更改为 **GBSI**，因为此公司将用于执行测试。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-324">In the Microsoft Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**, because this company will be used for test execution.</span></span>
4. <span data-ttu-id="3a0c5-325">在 RSAT 中，选择**使用 ER 格式 BACS (UK) 测试对供应商付款的处理**测试用例。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-325">In RSAT, select the **Test processing of vendor payments by using ER format BACS (UK)** test case.</span></span>
5. <span data-ttu-id="3a0c5-326">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-326">Select **Edit**.</span></span>
6. <span data-ttu-id="3a0c5-327">在打开的 Excel 工作簿中 **General** 工作表上，将公司代码更改为 **GBSI**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-327">In the Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**.</span></span>
7. <span data-ttu-id="3a0c5-328">请注意，**ERFormatMappingRunLogTable** 工作表上的单元格 A:3 和 C:3 中包含 ER 调试日志表中用于验证输出和基准比较结果的字段的文本。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-328">On the **ERFormatMappingRunLogTable** worksheet, notice that cells A:3 and C:3 contain the text of the fields in the ER debug log table that are used to validate the results of the comparison of the output to the baseline.</span></span> <span data-ttu-id="3a0c5-329">这些文本将用于评估执行测试期间创建的 ER 调试日志记录。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-329">These texts will be used to evaluate ER debug log records that are created during test execution.</span></span>

    <span data-ttu-id="3a0c5-330">![ERFormatMappingRunLogTable 工作表](media/GER-RSAT-RSAT-ExcelParameters.png "ERFormatMappingRunLogTable 工作表的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-330">![ERFormatMappingRunLogTable worksheet](media/GER-RSAT-RSAT-ExcelParameters.png "Screenshot of the ERFormatMappingRunLogTable worksheet")</span></span>

## <a name="run-the-tests-and-analyze-the-results"></a><span data-ttu-id="3a0c5-331">执行测试和分析结果</span><span class="sxs-lookup"><span data-stu-id="3a0c5-331">Run the tests and analyze the results</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="3a0c5-332">在 RSAT 中运行测试</span><span class="sxs-lookup"><span data-stu-id="3a0c5-332">Run the tests in RSAT</span></span>

1. <span data-ttu-id="3a0c5-333">在 RSAT 中，选择加载的测试。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-333">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="3a0c5-334">选择**运行**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-334">Select **Run**.</span></span>

<span data-ttu-id="3a0c5-335">请注意，将使用 Web 浏览器在应用程序中自动运行测试用例。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-335">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="3a0c5-336">分析测试的执行结果</span><span class="sxs-lookup"><span data-stu-id="3a0c5-336">Analyze the results of test execution</span></span>

<span data-ttu-id="3a0c5-337">测试的执行结果存储在 RSAT 中。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-337">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="3a0c5-338">请注意，两项测试均已通过。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-338">Notice that both tests were passed.</span></span>

<span data-ttu-id="3a0c5-339">![RSAT 中通过了的测试](media/GER-RSAT-RSAT-Tests-Passed.png "RSAT 中通过了的测试的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-339">![Tests that passed in RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "Screenshot of tests that passed in RSAT")</span></span>

<span data-ttu-id="3a0c5-340">请注意，还会将测试的执行结果发送到 Azure DevOps，以便执行进一步的分析。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-340">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="3a0c5-341">![Azure DevOps 中的测试执行结果](media/GER-RSAT-DevOps-Tests-Added.png "Azure DevOps 中的测试执行结果的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-341">![Results of test execution in Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Screenshot of the results of test execution in Azure DevOps")</span></span>

### <a name="simulate-a-situation-where-tests-fail"></a><span data-ttu-id="3a0c5-342">模拟测试失败的情况</span><span class="sxs-lookup"><span data-stu-id="3a0c5-342">Simulate a situation where tests fail</span></span>

<span data-ttu-id="3a0c5-343">如果生成的输出中至少一个与相应基准不匹配，则此测试套件必定会失败。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-343">This test suite must fail when at least one of the generated outputs doesn't match the corresponding baseline.</span></span> <span data-ttu-id="3a0c5-344">若要实现此情况，则可使用 **BACS (UK)** 格式的派生版本，以便生成内容与相应基准不匹配的付款文件。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-344">To achieve this situation, you can use your derived version of the **BACS (UK)** format that will generate a payment file that has different content than the corresponding baseline.</span></span> <span data-ttu-id="3a0c5-345">若要模拟此情况，则可使用同一个 **BACS (UK)** 格式，但更改所处理付款行中的付款金额。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-345">To simulate this situation, you can use the same **BACS (UK)** format but change the payment amount on the processed payment line.</span></span>

1. <span data-ttu-id="3a0c5-346">打开应用程序，然后转到**应付帐款 \> 付款 \> 付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-346">Open the application and go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="3a0c5-347">选择**行**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-347">Select **Lines**.</span></span>
3. <span data-ttu-id="3a0c5-348">选择付款行，然后选择**付款状态 \> 无**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-348">Select the payment line, and then select **Payment status \> None**.</span></span>
4. <span data-ttu-id="3a0c5-349">在**借记**字段中，将值从 **1,000.00** 更改为 **2,000.00**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-349">In the **Debit** field, change the value from **1,000.00** to **2,000.00**.</span></span>
5. <span data-ttu-id="3a0c5-350">选择**保存**以保存您的更改。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-350">Select **Save** to save your changes.</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="3a0c5-351">在 RSAT 中运行测试</span><span class="sxs-lookup"><span data-stu-id="3a0c5-351">Run the tests in RSAT</span></span>

1. <span data-ttu-id="3a0c5-352">在 RSAT 中，选择加载的测试。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-352">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="3a0c5-353">选择**运行**。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-353">Select **Run**.</span></span>

<span data-ttu-id="3a0c5-354">请注意，将使用 Web 浏览器在应用程序中自动运行测试用例。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-354">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="3a0c5-355">分析测试的执行结果</span><span class="sxs-lookup"><span data-stu-id="3a0c5-355">Analyze the results of test execution</span></span>

<span data-ttu-id="3a0c5-356">测试的执行结果存储在 RSAT 中。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-356">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="3a0c5-357">请注意，第二次执行时，第二项测试失败。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-357">Notice that the second test failed during the second execution.</span></span>

<span data-ttu-id="3a0c5-358">![RSAT 中的失败测试结果](media/GER-RSAT-RSAT-Tests-Failed.png "RSAT 中的失败测试结果的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-358">![Failed test results in RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Screenshot of the failed test results in RSAT")</span></span>

<span data-ttu-id="3a0c5-359">请注意，还会将测试的执行结果发送到 Azure DevOps，以便执行进一步的分析。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-359">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="3a0c5-360">![Azure DevOps 中的失败测试结果](media/GER-RSAT-DevOps-Tests-Failed.png "Azure DevOps 中的失败测试结果的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-360">![Failed test results in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Screenshot of the failed test results in Azure DevOps")</span></span>

<span data-ttu-id="3a0c5-361">可访问每个测试的状态。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-361">You can access the status of each test.</span></span> <span data-ttu-id="3a0c5-362">也可以访问执行日志，以便分析任何失败的原因。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-362">You can also access the execution log so that you analyze the reasons for any failure.</span></span> <span data-ttu-id="3a0c5-363">在下图中，执行日志显示失败的原因是所生成付款文件与其基准之间内容不同。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-363">In the following illustration, the execution log shows that the failure occurred because of the difference in content between the generated payment file and its baseline.</span></span>

<span data-ttu-id="3a0c5-364">![Azure DevOps 中用于分析失败原因的执行日志](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Azure DevOps 中用于分析失败原因的执行日志的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="3a0c5-364">![Execution log for analyzing failure in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Screenshot of the execution log for analyzing failure in Azure DevOps")</span></span>

<span data-ttu-id="3a0c5-365">因此，如您所见，可以通过将 RSAT 用作测试平台和使用基于任务录制器且使用 ER 基准功能的测试用例自动评估任何 ER 格式的运行。</span><span class="sxs-lookup"><span data-stu-id="3a0c5-365">Therefore, as you've seen, the functioning of any ER format can be evaluated automatically by using RSAT as the testing platform and by using Task recorder-based test cases that use the ER baseline feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a0c5-366">其他资源</span><span class="sxs-lookup"><span data-stu-id="3a0c5-366">Additional resources</span></span>

- [<span data-ttu-id="3a0c5-367">任务录制器</span><span class="sxs-lookup"><span data-stu-id="3a0c5-367">Task recorder</span></span>](../user-interface/task-recorder.md)
- [<span data-ttu-id="3a0c5-368">Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="3a0c5-368">Regression suite automation tool</span></span>](https://www.microsoft.com/download/details.aspx?id=57357)
- [<span data-ttu-id="3a0c5-369">通过使用任务录制和 BPM 创建用户接受度测试库</span><span class="sxs-lookup"><span data-stu-id="3a0c5-369">Create user acceptance test libraries by using task recordings and BPM</span></span>](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [<span data-ttu-id="3a0c5-370">部署支持持续构建和测试自动化的拓扑</span><span class="sxs-lookup"><span data-stu-id="3a0c5-370">Deploy topologies that support continuous build and test automation</span></span>](../perf-test/continuous-build-test-automation.md)
- [<span data-ttu-id="3a0c5-371">跟踪生成的报表结果并将其与 ER 基准值进行比较</span><span class="sxs-lookup"><span data-stu-id="3a0c5-371">Trace generated report results and compare them with ER baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="3a0c5-372">通过采用该格式的新的基本版本升级 ER 格式</span><span class="sxs-lookup"><span data-stu-id="3a0c5-372">Upgrade your ER format by adopting a new, base version of that format</span></span>](tasks/er-upgrade-format.md)
- [<span data-ttu-id="3a0c5-373">从 Lifecycle Services 导入 ER 配置</span><span class="sxs-lookup"><span data-stu-id="3a0c5-373">Import ER configuration from Lifecycle Services</span></span>](tasks/er-import-configuration-lifecycle-services.md)
